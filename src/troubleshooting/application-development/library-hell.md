---
summary: 
locale: en-us
guid: cefe3ea0-ea56-405d-8863-f2b366f442a3
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3082:479
---

# Library hell - why are changes in a producer not reflected in the consumers

If you're developing in multiple modules at a time, it may happen that a change is made to a producer module (for example, at an integration level) and there is the need to see the change reflected in a consumer module. In some situations, simply republishing the consumer module solves the problem. But in others, the changes don't get reflected in the consumers. 

This situation can be time-consuming and lead to frustration by the developer - who may believe there is a problem with their code and trigger a wild goose chase. 

Most times, this problem happens because of a reason: Library hell. This is something that can happen as your OutSystems app becomes more complex, with more levels of consumer/producer modules. Library Hell is a generalization of concepts already in use in the software industry, which are the root cause of the behavior (particularly DLL hell and Jar hell).

This article explains:

- What the concept means (both in the context of the native technologies and from an OutSystems app's perspective)

- Common pitfalls and dealing with them;

- Avoiding or dealing with the problem.

## The basics of deployment for an OutSystems app

OutSystems apps are `standard .NET or Java applications`. In .NET, apps are deployed in IIS by deploying each module as a separate Virtual Directory or VDir; in Java, they're deployed in either JBoss or Weblogic by deploying each module as a separate WAR app.

## Understanding how the platform deploys modules

In OutSystems, it's possible to create dependencies between apps by creating references between modules; it's also possible to use Extensions to create integrations with native code and import data from external systems.

When using references, the module or Extension that exposes the references is called a **Producer**; the module that imports the references is called a **Consumer**.

When you deploy an OutSystems app using references, the libraries of each producer are deployed with the consumer. In .NET, libraries are DLL files - a set for each producer; in Java, libraries are JAR files - again, a set for each producer.

## A practical example

This example uses a sample app with producers and consumers. The sample app is available [here](resources/LibraryHellDemo.osp).

The structure of the app is as follows:

![App structure](images/library-hell_0.png)

Image 1: Application structure

Explaining the app:

- **APIProvider** is a bottom-line producer: it exposes calls to public API

- **DataLayer** is a bottom-line producer: it exposes the data of the app

- **BrokerLogic** consumes both **APIProvider** and **DataLayer** to provide actions to list products

- **Purchasing** consumes both **APIProvider** and **DataLayer** to provide actions to buy products

- **UI_Public** is the front end used by customers 

Based on the example above, we'll describe some scenarios and explain what happens when the platform deploys the above app.

### What libraries exist in each module?

In an IIS VDir / Java WAR, for each module of the sample app, the following libraries are present:

- **APIProvider**: only itself

- **DataLayer**: only itself

- **BrokerLogic**: itself, APIProvider, DataLayer

- **Purchasing**: itself, APIProvider, DataLayer

- **UI_Public**: itself, APIProvider, DataLayer, BrokerLogic, Purchasing

A library being present means that the DLL (.NET) or JAR (Java) are present in the deployment unit (IIS VDir / Java WAR).

Below are three examples:

* **APIProvider**: its library is inside the running folder for APIProvider, inside **bin**:

    ![APIProvider library in the module's IIS VDir / Java WAR](images/library-hell_1.png)

    Image 2: APIProvider library in the module's IIS VDir / Java WAR

* **BrokerLogic**: in a consumer, producer libraries are inside a **bin2** folder. Here you can see that the libraries for **APIProvider** and **DataLayer** , the producers for **BrokerLogic**:

    ![Producer modules' libraries in BrokerLogic module's IIS VDir / Java WAR](images/library-hell_2.png)

    Image 3: Producer modules' libraries in BrokerLogic module's IIS VDir / Java WAR

* **UI_Public**: again in the **bin2** folder; in this one, all the libraries are there (for **APIProvider,** **DataLayer**,  **BrokerLogic** and **Purchasing**):

    ![Producer modules' libraries in UI_Public module's IIS VDir / Java WAR](images/library-hell_3.png)

    Image 4: Producer modules' libraries in UI_Public module's IIS VDir / Java WAR

In conclusion, you can find libraries for any module in the system:

* For the own module IIS VDir / Java WAR, in the **bin** folder (IIS VDir) or under **WEB-INF/lib**(Java WAR);

* In each of the consumer modules IIS VDir / Java WAR, in the **bin2** folder (IIS VDir) or under **WEB-INF/lib**(Java WAR).

When a request runs in the context of a consumer module, calls to actions from the producers use the local copies of libraries (under bin2) and not the original copy in the producer module's IIS VDir / Java War. In the example above, a call to APIProvider from BrokerLogic uses the file in Image 3; but if that call is made from UI_Public, then the file in Image 4 is used instead. If you delete the APIProvider file from Image 4, calls to APIProvider logic from UI_Public start to fail, but calls from BrokerLogic will still work.

### Changing producers

Because of how code from producers is called, if you change the code of a producer, the change is only reflected in a consumer after that consumer has been republished.

**Meaning**: if you change **APIProvider** and publish it, **UI_Public** doesn't get refreshed automatically - it's still using the previous library for it. Technically, only the IIS VDir / Java WAR for **APIProvider** was changed; the IIS VDir / Java WAR for **UI_Public** remains unchanged, with the previous versions of all libraries.

To test this scenario using the sample app:

* Access `http://<myserver>/UI_Public/`. There's an option to purchase items. Upon purchase, a feedback message displays. This message is obtained from using the **Echo** action from **APIProvider**.
In this version, **Echo** returns the input as output.

* Change the output of **Echo** in **APIProvider** to prepend "Simon says:" at the beginning of the output. Publish the new version of APIProvider;

* Access `http://<myserver>/UI_Public/` again. A new purchase still doesn't echo "Simon says". This happens because the library used in **UI_Public** is still the previous one.

To try to fix this scenario, the obvious solution would be to simply publish **UI_Public** again, so the change gets reflected. However, this isn't true.

You can test it yourself:

* In Service Center, republish the latest version of UI_Public.

* Access `http://<myserver>/UI_Public/` again. The echo still doesn't have the "Simon says" part.

You can repeat publish a few more times - it doesn't change anything.

## Multiple levels of producers

The reason republishing **UI_Public** doesn't fix this problem is because: **UI_Public** isn't a direct consumer of **APIProvider**.

This is relevant because of the way the platform obtains libraries of producer modules:

* When the platform publishes an module, it obtains dependency libraries from its direct producers.

    **In our example**: since the two producers of **UI_Public** are **BrokerLogic** and **Purchasing**, the platform will obtain libraries from them;

* If the platform needs further libraries (producer of producer) they will be obtained from the direct producers.

    **In our example**: all the libraries needed by **UI_Public** will be obtained directly from either **BrokerLogic** and **Purchasing**, not anywhere else.

Since there was no republish of **BrokerLogic** or **Purchasing**, their version of **APIProvider** library is still the old one. That version is the one included in **UI_Public** when it's published, and so it continues to use the outdated version.

Service Center warns about this: when republishing **UI_Public**, you get warnings that both **BrokerLogic** and **Purchasing** are outdated. You also get the warning that **UI_Public** will be outdated when you publish **APIProvider** initially.

An important question arises:

**From which producer (BrokerLogic or Purchasing) is the platform obtaining the libraries for APIProvider?**

The answer is: in this case, **it's undefined**.

How does it work generically for the platform?

* If a module/extension is a direct producer, the library is obtained directly from it;

* If a module/extension isn't a direct producer, but only a producer of one of the direct producers, that's the place where the library comes from.

    **In our example**: if only **BrokerLogic** consumed **APIProvider**, the library for APIProvider would come from **BrokerLogic**.

* If (*as our example*) the module / Extension isn't a direct producer and is a producer of more than one of the direct producers, then **the library can come from any of the producers that consume it**.

    **In our example**: since there are only two direct producers, if you republish the two and then republish **UI_Public** the change gets reflected and purchases start echoing "Simon says".

But in more complex reference scenarios, this may be extremely complex or even impossible (for example, in certain scenarios of circular references, which OutSystems allows using).
 
## How to solve a producer library inconsistency?

### What is a **DLL Hell**?

A **DLL Hell** scenario happens whenever you share DLLs that use different versions of the same library. This can be easy to identify when you only have two or three libraries, but if the number of libraries gets bigger, it can turn into a "hell".

### When does this happen in OutSystems?

A **DLL Hell** usually happens when you're dealing with .NET extensions. For example, if an app uses multiple AWS services, like DynamoDB and S3 but both of those extensions use a different version of the AWS SDK.

### How can you identify a DLL Hell?

While the symptoms can be triggered by different root causes, usually errors similar to these will display to end users, or you'll be able to see them in Service Center logs:

``Could not load file or assembly 'Namespace, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null' or one of its dependencies. The system cannot find the file specified.``

``Could not load type 'Microsoft.IdentityModel.Tokens.TokenHandler' from assembly 'Microsoft.IdentityModel.Tokens, Version=5.2.2.0, Culture=neutral, PublicKeyToken=885c28607f98e604 ``

### Troubleshooting steps

There are some options to fix the issue:

#### Check dependencies

1. Look for the producers of the app where the error is happening.
    
1. If you have outdated dependencies, refresh them.

#### Open similar extensions

1. Check if the same DLL is being used by those extensions. To do this, check the **Resources** tab in **Integration Studio**, or go to **Visual Studio** > **Solution Explorer** > **References** tree.

1. Check the version of each DLL.
    
    You can find all DLLs currently in use inside the platform folder, within the repository folder. Alternatively:
    
    1. Open the extension in **Integration Studio**.
    
    1. In the **Resources** tab, right-click the folder where the conflicting DLL is and select **Open**.

        ![Open the folder of the conflicting DLL](images/open-conflicting-dll-usr.png)

    1. Right-click the DLL file and select **Properties**.

        ![Open the DLL properties](images/file-version-value-usr.png)

    1. In the **Details** tab, check the **File version** value.

        ![Check file version](images/file-version-usr.png)

1. Ensure that all the extensions reference the same version of the DLL in use.

#### Update versions

1. Understand which DLL version should be used:

    * If one of the extensions is from a system component, keep the DLL version from that component as the base from now on. 

    * If none of the extensions is from a system component, check the differences between each version to understand which one to use.

1. After choosing the right version, update other extensions to the chosen version.
    
    If the DLL was added using NuGet: open the package manager, go to the **Installed** tab and update to the desired version.

    If not, copy the chosen DLL to the same folder in other extensions and publish the extension.

#### Publish all consumers of the changed extensions, 

If all other options failed, publish an [all components solution](https://success.outsystems.com/documentation/how_to_guides/devops/creating_and_using_an_all_components_solution/) with full compilation enabled to ensure each module and extension is recompiled.

## Dealing with frequent changes to "core producers"

There are development scenarios in which one needs to frequently change a "core producer" (in our example, **APIProvider**) and need to see the change reflected in the top-level Consumers (in our example, **UI_Public**).

The appropriate solution is using "solutions packs". This can however be time-consuming and impractical.

To avoid constantly publishing solution packs in these scenarios, there are two options:

1. **The architecture change**: deal with these dependencies as independent "micro-services" by using loose referencing.
From an architecture standpoint, this means treating the dependency as an external micro-service with a separate lifecycle, rather than a simple dependency of your project. [This article](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Designing_the_architecture_of_your_OutSystems_applications/Microservices_Architecture_in_OutSystems) explains how to obtain a Micro-services architecture in OutSystems.
In practical terms, instead of referencing through public action, this means referencing by consuming a web-service / REST service call. That way, one simply need to publish the service producer and the change is immediately reflected in the consumer - no publish required. From a platform perspective, a web-service/REST service call is an external integration - so the consumer isn't referencing any libraries of the producer.

This solution may pose other concerns: it's not transactional (the web-service logic runs in a separate transaction, so uncommitted changes from the original logic won't be visible), and can incur a performance penalty for the web-service call (especially if the service is called multiple times in the same request).

2. **The temporary hack**: add a direct reference from your top-level consumer (for example, **UI_Public**) to your core producer (for example, **APIProvider**).
Even if that reference isn't used in your code, by having this reference the platform is forced to obtain the library directly from the producer.
This should be seen as an emergency solution only: widespread use will make the reference model unmanageable. Wear with care!

