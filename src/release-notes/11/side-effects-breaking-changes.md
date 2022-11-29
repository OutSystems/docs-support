---
summary:
tags: version-11
en_title: OutSystems Platform side effects and breaking changes
locale: en-us
guid: 2cfe6cf6-118b-41dc-b4f3-a36ed20a3841
app_type: traditional web apps, mobile apps, reactive web apps
---

# OutSystems 11 side effects and breaking changes

This document lists the side effects and breaking changes introduced in the different versions of OutSystems 11.

OutSystems is committed to minimizing your effort when upgrading to a new release of OutSystems.

As such, before introducing a breaking change for a new release, OutSystems carefully analyzes its impact, namely, the expected number of occurrences in its customers' installations. A breaking change is introduced only if it affects a small number of customers.



## Breaking Changes 

### Introduced in Platform Server Sep.2018

#### LifeTime and Service Center

1\. <a name="bc-1"></a>

**Issue**: LifeTime is now only supported when installed in a dedicated environment.

**Runtime**: Mobile, Web

**Rationale**: LifeTime now has its own release cycle to allow for better and faster improvements in LifeTime. To achieve this, LifeTime must be run, installed and maintained in a separate environment from the development pipeline environments in customer infrastructures. Check [LifeTime release notes and breaking changes](https://success.outsystems.com/Support/Release_Notes/LifeTime_Management_Console).

**Workaround**: None.

---

2\. <a name="bc-2"></a>

**Issue**: The following actions are no longer available after uploading an Module in Service Center: "Publish in debug mode", "Publish step by step" and "Publish step by step in debug mode".

**Runtime**: Mobile, Web

**Rationale**: These features were removed since they were infrequently used.

**Workaround**: None.

#### SMS

3\. <a name="bc-3"></a>

**Issue**: Removed support for the SMS feature. Publishing modules with SMS Flows will fail.

**Runtime**: Web

**Rationale**: The built-in SMS feature was removed due to low adoption and since it is no longer aligned with the product vision.

**Workaround**: Remove any SMS flows from your modules and any related dependencies before publishing them.

#### Database 

4\. <a name="bc-4"></a>

**Issue**: The Configuration Tool shows an error when it detects a previous configuration using MySQL.

**Runtime**: Mobile, Web

**Rationale**: MySQL is not supported as the platform database in OutSystems 11 and Configuration Tool will issue an error when it detects a previous configuration using MySQL. MySQL is now only supported as an external database.

**Workaround**: None.

---

5\. <a name="bc-5"></a>

**Issue**: Publishing an Module with a text entity attribute whose length is longer than 2000 characters but for which the metamodel says its length is exactly 2000 characters causes an error in Oracle, stating that the column's underlying data type cannot be changed.

**Runtime**: Mobile, Web

**Rationale**: There was issue when developers changed the size of a Text attribute from 2000 characters to a larger value. In this case, the platform changed the metamodel for the attribute but not the database column itself, which might have led to data corruption at runtime.

**Workaround**: Open the Module, find the column, change its size back to 2000 characters and publish the Module.

To check which Modules are affected, run the following query against your Oracle database:

    select distinct esp.name espace, ent.physical_table_name, ent.name entity, eattr.name attribute_name, length 
    from ossys_entity_attr eattr
        left join ossys_entity ent on(eattr.entity_id = ent.id)
        left join ossys_espace esp on(ent.espace_id = esp.id)
        left join dba_tab_cols cols on (upper(eattr.name) = cols.column_name and upper(ent.physical_table_name) = cols.table_name)
    where eattr.type = 'rtText' and eattr.is_active=1 and eattr.length > 2000 and ent.is_active=1 and ent.is_system=0 and ent.is_external=0 and esp.is_active=1 and esp.name not in ('ECT_Provider') and cols.data_type <> 'CLOB';

#### Logs

6\. <a name="bc-6"></a>

**Issue**: Joins between log tables and other tables are no longer allowed.

**Runtime**: Mobile, Web 

**Rationale**: Log tables may now be on a different physical database and in such scenarios it is not possible to do a database join.

**Workaround**: Use the new additional columns available in each log table or create application logic to replace the previously existing database join. Log entities are now available through the PlatformLogs extension.

---

7\. <a name="bc-7"></a>

**Issue**: Log entities without "Show Tenant Identifier" will no longer be filtered automatically.

**Runtime**: Mobile, Web

**Rationale**: Since logs can now be stored on a separate physical database, it is not possible to define a table as Multi-Tenant, and the platform will not be able to create the filter automatically.

**Workaround**: Explicitly add a filter by the current tenant identifier using the "Tenant_Id" column.

---

8\. <a name="bc-8"></a>

**Issue**: Log entities are now only accessible as read-only.

**Runtime**: Mobile, Web

**Rationale**: The runtime logging database user has no additional permissions, to prevent log tampering.

**Workaround**: None.

---

9\. <a name="bc-9"></a>

**Issue**: The OutSystems Log Service is no longer installed in OutSystems 11 first installations. Any automation scripts relying on the existence of this service may issue errors.

**Runtime**: Mobile, Web 

**Rationale**: The OutSystems Log Service is not used by OutSystems 11 applications, but any applications that were not upgraded to OutSystems 11 still need this service to log errors. The service is not removed when upgrading Platform Server to version 11, but it's no longer installed in first installations. Follow the instructions in [Log Service Cleanup](https://success.outsystems.com/Documentation/How-to_Guides/DevOps/Log_Service_Cleanup) to remove the service, if no longer needed.

**Workaround**: If you have any automation scripts that rely on the existence of the OutSystems Log Service, you must update those scripts to handle the fact that the service may not exist.

#### REST APIs

10\. <a name="bc-10"></a>

**Issue**: Name clashes are now detected in REST structures when attributes have the same "Name in JSON" property value. The TrueChange pane will now show an error in this situation.

**Runtime**: Mobile, Web

**Rationale**: Although it is possible that regular structures and structures created from Consumed REST APIs have attributes with the same "Name in JSON", using these structures in Consume REST, Expose REST, JSON Serialize or JSON Deserialize elements causes serialization errors.

**Workaround**: Change the 'Name in JSON' of the attributes causing the error so that there are no duplicate values.

#### SOAP Web Services

11\. <a name="bc-11"></a>

**Issue**: Methods in EnhancedWebReferences API to customize consumed SOAP Web Services (all GetWebReference\* and SetWebReference\* methods) are now deprecated for imported SOAP Web Services created in OutSystems 11 and calls to those methods will be ignored. They can still be used for existing web services, i.e. for SOAP Web Services created in a version older than OutSystems 11 and then upgraded to this version.

**Runtime**: Mobile, Web

**Rationale**: In OutSystems 11 there's a new implementation for consumed SOAP Web Services that are created in OutSystems 11, supporting SOAP 1.2 and some additional features. One of the biggest improvements is in terms of extensibility, by providing a powerful API similar to the one available for REST integrations, able to solve more use cases and provide more customization possibilities. Due to this fact, the EnhancedWebReferences API is **not** compatible with this new implementation and is now deprecated for consumed SOAP Web Services. However, the EnhancedWebReferences API is still the official (non-deprecated) API for customizing exposed SOAP Web Services in OutSystems.

**Workaround**: Use the [SOAP Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/SOAP_Extensibility_API) to customize requests of consumed SOAP Web Services created in OutSystems 11.

---

12\. <a name="bc-12"></a>

**Issue**: Certificates configured in Service Center (Administration > Certificates) can't be used with consumed SOAP Web Services that were created in OutSystems 11. They can still be used for existing web services, i.e. for SOAP Web Services created in a version older than OutSystems 11 and upgraded to this version.

**Runtime**: Mobile, Web

**Rationale**: There's a new implementation for consumed SOAP Web Services in OutSystems 11 supporting SOAP 1.2 and some additional features. Along with this implementation, OutSystems provided a new [SOAP Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/SOAP_Extensibility_API) that can be used to use client-side certificates, among other use cases.

**Workaround**: Use the [SOAP Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/SOAP_Extensibility_API) to authenticate requests using client-side certificates in consumed SOAP web services that were created in OutSystems 11. Check the [client certificate authentication example](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Use_Advanced_Extensibility/Example%3A_Authenticate_using_a_client_certificate) provided in the API documentation.

#### Web Server Configuration (IIS) 

13\. <a name="bc-13"></a>

**Issue**: IIS application pools that only have OutSystems applications will have their pipeline mode changed from Classic to Integrated.

**Runtime**: Mobile, Web

**Rationale**: Integrated pipeline mode is the recommended pipeline mode for IIS. It should enable OutSystems applications to serve more users concurrently. This helps to avoid the thread pool limits of Classic mode.

**Workaround**: None. You should check if all the applications in those application pools work in Integrated mode. Issues will only arise if you have included settings that are only applicable to Classic mode in `web.config` files.

#### Built-in Functions

14\. <a name="bc-14"></a>

**Issue**: Built-in time and data comparison functions `DiffHours`, `DiffMinutes`, and `DiffSeconds` now ignore the milliseconds.
    
**Runtime**: Mobile, Web

**Rationale**: OutSystems enables you to manipulate time values on a second-level granularity. Some integrations introduce values at the millisecond-level granularity and these milliseconds could not be properly handled by the built-in functions, causing them to return an incorrect value in some cases. Ignoring the milliseconds part in the data values will prevent time manipulation functions from returning possibly incorrect values.

**Workaround**: None.  

#### JavaScript and HTML Rendering

15\. <a name="bc-15"></a>

**Issue**: Having a JavaScript flow element with asynchronous code in a Client Action that is marked as a function returns an error, and it is not possible to publish the module.

**Runtime**: Mobile

**Rationale**: The usage of asynchronous JavaScript code in Client Actions that are marked as functions can have an unpredictable behavior at runtime.

**Workaround**: Move the JavaScript flow element containing asynchronous JavaScript code to the "On Initialize" event of the screen and store the result you need in a variable of the same screen. In the Client Action, use that variable instead of the JavaScript element.  

---

16\. <a name="bc-16"></a>

**Issue**: Removed 'alt' attribute from the HTML rendering of links in Web Applications. 

**Runtime**: Web

**Rationale**: This attribute was used for compatibility in old browsers that are no longer supported. The 'alt' attribute only makes sense in image tags.

**Workaround**: If the 'alt' attribute in any element is still required, it can be inserted using Extended Properties.

---

17\. <a name="bc-17"></a>

**Issue**: Removed 'scheme' attribute from the rendering of meta elements in Web Applications.

**Runtime**: Web

**Rationale**: According to W3C the 'scheme' attribute on the meta element is obsolete.

**Workaround**: If you are using the AddPostProcessingFilter action of the HTTPRequestHandler extension to add filters that somehow rely on the presence of the 'scheme' attribute of meta elements, you should adapt your source regular expression of the action to improve its handling of optional attributes of meta tags.

#### Custom Handlers

18\. <a name="bc-18"></a>

**Issue**: Custom Handlers is a folder where you can define custom pages for common runtime errors.  
From OutSystems 11 onwards, if a default language is not defined in the Custom Handler folder's `web.config` file, it will be automatically set to "VB" (Visual Basic).
    
**Runtime**: Web

**Rationale**: The Custom Handlers folder is now deployed along with every application (to a sub-folder of the application folder), while previously the Custom Handlers folder was referenced by applications as needed from its location inside the Platform Server installation folder.  

OutSystems provides default Custom Handlers pages and some of those default pages include Visual Basic code, e.g. `internalerror.aspx`. Additionally, if no default language is defined in the `web.config` file in the Custom Handlers folder, the default language defined in the application's `web.config`, which is C#, will be used during the Custom Handlers pages' compilation and cause errors.

**Workaround**: Modify the Custom Handlers `web.config` file to explicitly state the language used in your Custom Handlers pages.

#### OutSystems APIs

19\. <a name="bc-19"></a>

**Issue**: Removed deprecated ApplicationManagementService and EnvironmentManagementService APIs from LifeTime Services.

**Runtime**: Mobile, Web

**Rationale**: These Web Services were marked as deprecated in OutSystems 10 because the same version introduced new and more complete REST APIs.

**Workaround**: Change the integrations on your applications to consume the new LifeTime REST APIs.  

---

20\. <a name="bc-20"></a>

**Issue**: Removed the ElementVersionInfo structure from LifeTime SDK module.

**Runtime**: Mobile, Web

**Rationale**: It was necessary to perform some changes in the current implementation of exposed APIs due to changes related with the new Reference Model. This included removing the ElementVersionInfo structure, which will not be available in the LifeTime metamodel anymore.

**Workaround**: None.

---

21\. <a name="bc-21"></a>

**Issue**: The `getFrontendKey()` method of the outsystems.api.requestInfo API might return a different key value in OutSystems 11.

**Runtime**: Web

**Rationale**: The Frontend Name was made more consistent throughout monitoring and log sources. Since the Frontend Key value is based on the Frontend Name, the value returned by the `getFrontendKey()` method might also change.

**Workaround**: None.

#### Extensions

22\. <a name="bc-22"></a>

**Issue**: Removed obsolete database access APIs from the RuntimePlatform .NET library.

**Runtime**: Mobile, Web

**Rationale**: These APIs are deprecated since 9.0 and OutSystems provides alternative ways of achieving the same functionality.

**Workaround**: Use the new database access APIs available in the RuntimePublic.Db API.

---

23\. <a name="bc-23"></a>

**Issue**: The Settings class in the RuntimePlatform .NET library is now deprecated and all methods that allowed you to modify settings inside applications were removed.

**Runtime**: Mobile, Web

**Rationale**: Configurations affecting the runtime of applications are now an integral part of an application and can no longer be manipulated in runtime. Additionally, the previously existing classes were internal and not meant for public usage.

**Workaround**: Any existing extensions taking advantage of this internal class must be modified to stop using it.

#### Security

24\. <a name="bc-24"></a>

**Issue**: Screen navigation done in HTTPS will not downgrade the protocol to HTTP even when the destination screen is not explicitly marked as requiring HTTPS.

**Runtime**: Web

**Rationale**: In previous versions it was difficult to ensure that an application always used HTTPS when some of its screens did not require HTTPS.

**Workaround**: For those rare situations where you need to redirect the user to an HTTP address, change the application to use an External Site element with an explicit HTTP URL.

---

25\. <a name="bc-25"></a>

**Issue**: HTTPS is now enforced for all screens and integrations (REST and SOAP) in mobile modules. There is no opt-out from this behavior.

**Runtime**: Mobile

**Rationale**: The previous behavior did not make applications secure by default. Exposed SOAP web services were unable to enforce HTTPS.

**Workaround**: None.

---

26\. <a name="bc-26"></a>

**Issue**: Image URLs generated in the previous platform versions will no longer be valid.

**Runtime**: Web

**Rationale**: The previously existing image endpoint used a shared key across all clients to encrypt the image details. The new endpoint uses the unique private key of each client to encrypt the image details, thus preventing other clients from tampering with the URL content.

**Workaround**: To keep the old behavior, set the `OutSystems.Images.UsePrivateKeyEncryptionForURL` parameter to `false` in the OSSYS_PARAMETER database table.  
Note: The support for this setting will be dropped on the next major platform version and the new behavior will be used by default.

---

27\. <a name="bc-27"></a>

**Issue**: Full SQL commands are no longer displayed to the end-user when an error occurs in a SQL element.  
This behavior only occurred in versions earlier than 10.0.723.0; upgrades from a later OutSystems 10 version to OutSystems 11 are not affected by this change of behavior.

**Runtime**: Mobile, Web

**Rationale**: Previously, when an error occurred in a SQL element, the error message could be shown to the end-user if the exception was not properly handled. This message would include the query where the error occurred and it would expose some details about the application entities. Now, the error and the query are still logged and displayed in the environment management console, but the end-user will only see a generic error message.

**Workaround**: None.

#### System Entities

28\. <a name="bc-28"></a>

**Issue**: Removed the Zone and Zone_Server system entities, as well as the "Zone_Id" attribute from the Espace system entity.  
Upgrading a module in Service Studio will remove any dependencies on these entities and attribute. You will get validation errors if these deleted objects were being used.

**Runtime**: Mobile, Web

**Rationale**: In OutSystems 11 the concept of Zones has been replaced by Deployment Zones and these system entities and attribute are no longer used.

**Workaround**: None.

---

29\. <a name="bc-29"></a>

**Issue**: Removed entities Entity_Usage and Entity_Usage_Sample from the "(System)" reference.

**Runtime**: Mobile, Web

**Rationale**: These were internal entities that were not being used.

**Workaround**: None.

#### Emails

30\. <a name="bc-30"></a>

**Issue**: Queued emails from disabled applications are no longer processed by the Scheduler Service.

**Runtime**: Mobile, Web

**Rationale**: Make the behavior of pending emails consistent with the behavior of newly created emails.

**Workaround**: None.

---

31\. <a name="bc-31"></a>

**Issue**: Emails now require that there is at least one server in the Deployment Zone of the module configured to "Send Emails".

**Runtime**: Web

**Rationale**: Previously, emails could be sent by any server in the environment, regardless of the module that created them. This broke the isolation between servers, causing misbehaved modules to have impact in the email processing of modules in other servers. The new behavior is now consistent with the execution of Processes and Timers.

**Workaround**: Ensure that there is at least one server in each Deployment Zone that is able to "Send Emails", if it contains modules with Email screens. You can set this configuration in Service Center (Administration > Servers).


#### Resources

32\. <a name="bc-32"></a>

**Issue**: Changing binary resources now triggers a references update and a recompilation of consumers.

**Runtime**: Mobile, Web

**Rationale**: It was possible to change a binary resource in a producer without consumers recompiling the resource after the change. In some cases, this made the resource to be apparently working in the consumer without any issues. However, if developers changed the resource name or its target directory this would cause consumers to break.

**Workaround**: None. We changed the reference semantics in binary resources: they are now copied to the consumers and will trigger a recompilation when a binary resource is changed.

#### OSP Tool 

33\. <a name="bc-33"></a>

**Issue**: The "Upload" button in OSP Tool no longer publishes the solution.

**Runtime**: Mobile, Web

**Rationale**: The "Upload" button was also publishing the solution and not just uploading it, as it should. This behavior was fixed. 

**Workaround**: Click the "1-Click Publish" button to publish the solution.

#### Mobile Apps

34\. <a name="bc-34"></a>

**Issue**: If you upgrade to OutSystems 11 and you have old mobile apps published before September 2018 your applications will break with an error screen after the upgrade of Platform. Only apps that use App Feedback and that were built before September 2018 are affected by this breaking change.

**Runtime**: Mobile

**Rationale**: In OutSystems 11 we introduce new improvements to our App Feedback feature that are not compatible with the older versions of mobile apps.

**Workaround**: If you haven't generated and distributed mobile apps since September 2018, and the apps have App Feedback enabled, generate those mobile apps again and then distribute them to the users before upgrading.

35\. <a name="bc-35"></a>

**Issue**: If you upgrade to OutSystems 11, and you previously distributed mobile apps that were generated between July 31, 2019 and October 9, 2019, those apps will break with an error screen after the upgrade.

**Runtime**: Mobile

**Rationale**: In July 2019 we fixed a Query Parameters issue related to opening apps with deep links. However, this fix broke the upgrade process.

**Workaround**: If you generated and distributed mobile apps between July 31, 2019 and October 9, 2019, generate those mobile apps again and then distribute them to the users before upgrading.

#### Mobile Runtime

36\. <a name="bc-36"></a>

**Issue**: Iterating a list recursively throws a runtime error.

**Runtime**: Mobile

**Rationale**: Keep the client-side and server-side models consistent between each other, since the server-side code always had this limitation. We introduced this change in OutSystems 11 to prevent breaking changes during the OutSystems 10's release cycle.

**Workaround**: Change the application logic to ensure that there are no recursive iterations of a list.

#### Logic

37\. <a name="bc-37"></a>

**Issue**: JSONDeserialize widget no longer truncates Decimals that are parsed to Text.

**Runtime**: Mobile, Web

**Rationale**: When using JSONDeserialized widget in Server Actions to deserialize a JSON string data to a record or list. If the deserialized data type contains a Text attribute but in the JSON string data that attribute value is sent as a Decimal, the trailing zeros are preserved when deserializing that Decimal attribute to Text. 

For example, the sent decimal values `10.000` and `10.1000` are deserialized to `10.000` and `10.1000` and not to `10` and `10.1`. 

**Workaround**: To truncate a value, change the deserialized attribute data type to Decimal instead of  Text. 

### Introduced in Platform Server Oct.2019

**Issue**:  Integrations with external databases that use Oracle Database 10g Release 2 will stop working.

**Runtime**: Mobile, Web

**Rationale**: We upgraded Oracle Data Provider for .NET, Managed driver to version 19.3.1 (4.122.19.1:20190703) and, according to the [official documentation](https://docs.oracle.com/en/database/oracle/oracle-database/19/odpnt/InstallSystemRequirements.html#GUID-A6405CAD-C0E9-45E0-9C38-26B7ED214479), this driver allows applications to connect to Oracle Database 11g Release 2 or later. This driver supports native encryption, meaning that you can set up your database to require encryption and this means all connections will be encrypted between the server and the database (applicable to both platform and external databases).

**Workaround**: Upgrade your Oracle engine to version 11g Release 2 or later.

### Introduced in Platform Server 11.7.0

**Issue**:  Upgraded SharpZipLib library to version 1.1.0. The new version of the library can cause compatibility problems with custom components used in extensions. For example, when using the [OfficeUtils](https://www.outsystems.com/forge/component-overview/687/officeutils) Forge component you must upgrade to a recent version of the component, since it previously used a library version (NPOI 2.2, an Excel reader library) that depended on the previous SharpZipLib library version.

**Runtime**:  Mobile, Web

**Rationale**: The new version of the library contains several performance improvements and security fixes. It's also a necessary change to be able to use recent versions of third-party libraries, like recent versions of NPOI that have a dependency on this library.

**Workaround**: This change has an impact on extensions that are using SharpZipLib to read ZIP files, or in extensions using libraries that have SharpZipLib as a dependency (like NPOI). It's recommended that you test any Zip and Excel-related functionalities of your applications after upgrading. If you find any issues, you must change any OutSystems extensions using third-party libraries that depend on SharpZipLib version 0.86.0. In the extensions, update the version of these third-party libraries to a version that uses SharpZipLib version 1.1.0.

### Introduced in Platform Server 11.9.0
1\. <a name="bc119-1"></a>

**Issue**: The platform now gives preference to usage of specific versions of third-party assemblies that are included in extensions. As a consequence, extensions that incorrectly include .NET Framework assemblies can prevent applications from working correctly due to conflicts between the included assemblies and the assemblies of the .NET Framework installed in the machine.

In particular, including the extensions `System.Net.Http.dll` or `System.Runtime.InteropServices.RuntimeInformation.dll` causes issues in **logging**, **login** and **JSON serialization**.

**Runtime**:  Mobile, Web

**Rationale**: With the increased usage and adoption of open source libraries and systems like NuGet, it's an impossible task to ensure that all third-party assemblies used in an application have exactly the same versions. This applies to both the OutSystems platform, to extensions, and to any other .NET applications.

To improve the compatibility between multiple third-party libraries and different extensions used together, OutSystems apps now force the load of the assembly versions placed in the application directory. If the assembly available in the application folder has a higher version than the required one, it will work instead of the exact version specified at compile time. This is a similar behavior to the one currently present in the new .NET Core apps.

**Fix**: Open and remove all problematic system assemblies from affected extensions.

Before doing the Platform Server upgrade, check and fix the affected extensions. To do that, run the following query against your platform database:

    select distinct ossys_extension.Name, ossys_Extension_Dependency.Filename, ossys_Extension_Dependency.Compile_Action
    from ossys_Extension_Dependency inner join ossys_extension on ossys_extension.id = ossys_Extension_Dependency.extension_id
    where (ossys_Extension_Dependency.Filename like 'System.Runtime.InteropServices.RuntimeInformation.dll'
        or ossys_Extension_Dependency.Filename like 'System.Net.Http.dll')
        and ossys_extension.Version_Id = ossys_Extension_Dependency.Extension_Version_Id

You can adapt this query to list all 'System.%' assembly dependencies, but many of those assemblies aren't distributed with the .NET Framework. Therefore, it's difficult to make an extensive assembly list, apart from the following two known problematic assemblies: `System.Runtime.InteropServices.RuntimeInformation.dll` and `System.Net.Http.dll`. OutSystems recommends that you keep as few `System.*` included dependencies as possible.

Some commonly used applications from the Forge, like "Time Zone" and "Ultimate PDF", are known to have the issues outlined above. Remember to check the Forge for updated versions of these applications.

This issue happens mostly in extensions with its target framework set to 4.6.1 and that are referencing .NET Standard dependencies.  
This was never a supported configuration. Check [How to Use .NET Standard libraries in OutSystems extensions](https://success.outsystems.com/Documentation/How-to_Guides/Integrations/How_to_Use_.NET_Standard_libraries_in_OutSystems_extensions) for more information on referencing .NET Standard dependencies correctly. You can also find instructions on how to clean up unnecessary dependencies.

**Workaround**: As a temporary workaround for Platform Server 11.9.0, OutSystems added a new setting to the [Factory Configuration](https://www.outsystems.com/forge/component-overview/25/factory-configuration) application: "Force apps to use existing versions of third party libraries". When this setting is disabled, the platform reverts to the previous behavior.  
You should only use this workaround if it's not viable to fix all the affected extensions in a timely fashion. This setting will be ignored in all platform versions above 11.9, so it's important that you fix the root causes of this issue.

2\. <a name="bc119-2"></a>

**Issue**: The KeyStore and SAML actions were moved from the **Authentication** extension, `Authentication.xif`, to the **SAMLAuthentication** extension, `SAMLAuthentication.xif`. This can cause some broken references when using methods from Authentication.xif that moved to the new module.

**Runtime**: Mobile, Web

**Rationale**: This refactoring was necessary to support architectural changes to the SAML authentication.

**Fix**: Replace dependencies to KeyStore and SAML actions from **Authentication** to the corresponding actions from **SAMLAuthentication**.

### Introduced in Platform Server 11.11.1

**Issue**: HTTP responses from Consumed REST API integrations now are closed more aggressively.

**Runtime**: Mobile, Web

**Rationale**: When doing a large number of Consumed REST API requests, the number of used ports can increase rapidly and lead to port exhaustion problems. The new behavior prevents this situation and generally helps avoid leaking resources. However, this new behavior can also cause runtime changes in some edge cases. A known situation takes place when consuming an Exposed REST API in OutSystems that returns HTTP status code 204 (No Content), but sends data in the body, thus sending a "Content-Length" header with a value greater than zero. Although this is [invalid according to RFC 7230](https://httpwg.org/specs/rfc7230.html#header.content-length), it previously didn't cause an error. Additionally, you should validate other scenarios that might be affected by this breaking change.

**Workaround**: For the example stated above, the workaround is to change the returned status code from 204 (No Content) to a different status code, if you wish to include data in the body. Alternatively, keep returning the 204 status code but don't include any content in the response body.

### Introduced in Platform Server 11.14.0

**Issue**: The Title of a Popup_Editor, Popup_EditorForUpload or Popup_EditorVanilla widget appears garbled in the application when all the following conditions are true:

* The title is dynamically generated through an input parameter.
* The value of the input parameter contains special characters.
* The value of the input parameter is encoded.
    
**Runtime**: Traditional web

**Rationale**: These widgets now encode the Title by default to prevent cross site scripting (XSS) attacks.

**Fix**: Remove the encoding of the input parameter value before sending it to the Title of the Popup.

**Workaround**: In Service Center, set the site property 'PopupTitle_ForceHTMLEncode' to False in the site properties of the RichWidgets module. This isn't recommended, as it leaves the popup vulnerable to XSS attacks.

### Introduced in Platform Server 11.17.0

**Issue**: The HTML code in the `MessageText` parameter of the Feedback_Message Server Action displays as plain text in the Feedback_Message widget of RichWidgets, instead of rendered HTML.

**Runtime**: Traditional web

**Rationale**: The Feedback_Message widget now encodes the message by default to prevent cross site scripting (XSS) attacks.

**Fix**: Don't add HTML code to the Feedback_Message's text.

**Workaround**: In Service Center, set the site property `FeedBackMessage_ForceHTMLEncode` to False in the site properties of the RichWidgets module. This isn't recommended, as it leaves the Feedback_Message widget vulnerable to XSS attacks.


### Introduced in Platform Server 11.18.0

1\. <a name="bc-11180-1"></a>

**Issue**: The installer was modified to delete specific third-party DLLs from the `\plugins\database` folder and recreate them in new subfolders. This can prevent third-party/custom external Database Connectors from functioning.

Follows the list of affected files along wth the folder they're recreated on:

* **iDB2** DLLs are recreated in folder `\plugins\database\iDB2\`:
    * IBM.Data.DB2.iSeries.dll
    * Recreated in \plugins\database\Oracle\
    * Oracle.ManagedDataAccess.dll

* **MySQL** DLLs are recreated in folder `\plugins\database\MySQL\`:
    * BouncyCastle.Crypto.dll
    * Google.Protobuf.dll
    * K4os.Compression.LZ4.dll
    * K4os.Compression.LZ4.Streams.dll
    * K4os.Hash.xxHash.dll
    * MySql.Data.dll
    * Renci.SshNet.dll
    * System.Buffers.dll
    * System.Memory.dll
    * System.Numerics.Vectors.dll
    * System.Runtime.CompilerServices.Unsafe.dll
    * Ubiety.Dns.Core.dll
    * Zstandard.Net.dll

* **PostgreSQL** DLLs are recreated in folder `\plugins\database\PostgreSQL\`:
    * Microsoft.Bcl.AsyncInterfaces.dll
    * Npgsql.dll
    * System.Buffers.dll
    * System.Memory.dll
    * System.Numerics.Vectors.dll
    * System.Runtime.CompilerServices.Unsafe.dll
    * System.Text.Encodings.Web.dll
    * System.Text.Json.dll
    * System.Threading.Channels.dll
    * System.Threading.Tasks.Extensions.dll

**Runtime**: Mobile, Web

**Rationale**: This file/folder reorganization was necessary to allow finer control over which DLLs are referenced, as well as their versions. This file/folder reorganization improves compatibility between current and future Database Connectors.

**Fix**:

After running the Platform Installer and before running the Configuration Tool, move or install any third-party or custom Database Connectors to their respective folders. This move ensures that none of the DLLs needed by those custom Database Connectors will be deleted. You only need to make this move once.

For example, consider a third-party Database Provider named `ExampleDB`. It consists of three DLLs:

* `ACME.DatabaseProvider.ExampleDB.dll` (Database Connector plugin)
* `ExampleDB.Driver.dll` (Driver DLL)
* `Google.Protobuf.dll` (Dependency of Driver DLL)

Before Platform Server 11.18.0, these DLLs are placed under the `Platform Server\plugins\database` folder.

With the new changes, the `Google.Protobuf.dll` are deleted and recreated in the MySQL subfolder, which can make the `ExampleDB` Database Connector non-functional (depending on the configured external Database Connections).

To prevent this, when upgrading to Platform Server 11.18.0 or higher, complete the following steps after running the Platform installer and before selecting **Apply & Exit** in the Configuration Tool:

* Create an `ExampleDB` folder in `plugins\database`, and place all the relevant DLLs there.
* Optionally, create a new `manifest.json` file with all the references required by the plugin. This is only required if you identify version mismatches between what's needed for the plugin and the current supported DLLs.

**Note**: OutSystems services must be restarted, and Service Center republished for the plugin to be detected. The Configuration Tool does this automatically on an upgrade.

2\. <a name="bc-11180-2"></a>

**Issue**: As a side effect of [breaking change number 1](#bc-11180-1), applications that use custom database connections can start to have runtime errors such as `Could not load file or assembly 'Google.Protobuf, Version=3.12.3.0, Culture=neutral, PublicKeyToken=a7d26565bac4d604' or one of its dependencies. The system cannot find the file specified.`

**Runtime**: Mobile, Web

**Rationale**: This file/folder reorganization was necessary to allow finer control over which DLLs are referenced, as well as their versions. This file/folder reorganization improves compatibility between current and future Database Connectors.

**Fix**: 

<!--If you're using the Forge asset [Secret Manager Local Service](https://www.outsystems.com/forge/component-overview/13476/secret-manager-local-service), update it to the latest version.-->

If you're using a custom database connector packed in an extension, add the DLL to the extension and publish it. Refresh the references on the consumers and republish them.

**Workaround**: In case you can't use any of the above fixes, do the following:

1. Identify the assembly that's failing to be loaded in the list of [breaking change number 1](#bc-11180-1).
1. Create a new [External Database Connection](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Integrate_with_an_External_Database/Integrate_with_an_external_database_using_Integration_Studio) and chose the DBMS identified on the list.
1. Don't test it and then save it. This will be a dummy connection, used only to recreate the files. It doesn't need to be assigned to an extension.
1. Republish the app that was having the errors.

## Side Effects

### Introduced in Platform Server Sep.2018

#### OutSystems APIs

1\. <a name="se-1"></a>

**Issue**: `BeginReadUncommittedTransaction` and `BeginTransaction` methods from RuntimePublic.Db API are now deprecated.

**Runtime**: Mobile, Web

**Rationale**: These methods would crash because connections are already inside the context of a transaction.

**Workaround**: None.

#### User Provider

2\. <a name="se-2"></a>

**Issue**: A Performance Suggestion warning will be added to all modules that do not have 'Is User Provider' set and have the 'User Provider' as 'Current Module'.

**Runtime**: Mobile, Web

**Rationale**: It's recommended that all modules specify a User Provider to reduce the amount of work necessary in application's first load times and to avoid communications between applications and the Deployment Controller Service.

**Workaround**: Determine what should be the User Provider of your factory (by default it should be 'Users') and set the 'User Provider' property accordingly. If a module is supposed to be a User Provider, change the 'Is User Provider' property value to 'Yes'.  
Note: It's not recommended to change the User Provider of modules with Processes or Multi-tenant Entities/Timers/Site Properties.

#### Custom Handlers

3\. <a name="se-3"></a>

**Issue**: The Custom Handlers directory is now deployed along with every application. Previously, the Custom Handlers directory existed in the Platform Server installation directory and every application referenced it when needed.

**Runtime**: Web

**Rationale**:  This change makes applications more self-contained in order to enable deployment to containers.

**Workaround**: None.

#### Debug Mode

4\. <a name="se-4"></a>

**Issue**: After turning off the environment Debug Mode configuration, some modules will show a warning saying that they need to be republished, when in fact they do not.

**Runtime**: Mobile, Web

**Rationale**: When disabling the Debug Mode for the environment, all modules will have a warning stating that they need to be republished. In fact, the modules that already had Debug Mode disabled do not need to be republished since their configuration matches the configuration of the environment.

**Workaround**: None.

#### Solution Publish

5\. <a name="se-5"></a>

**Issue**: The refresh of references when publishing a solution (when publishing the current running version of its components) in Service Center was reviewed. Publishing the current version of a solution will now only refresh module references when the publish operation is performed in an environment whose purpose is set to Development.

**Runtime**: Mobile, Web

**Rationale**: In environments whose purpose is not Development it is important that the actual published versions are kept; refreshing references would create different "fake" versions.

**Workaround**: Refresh references manually.

### Introduced in Platform Server 11.14.0

#### Identity Service

1\. <a name="se1114-1"></a>

**Issue**: The login for IT apps (apps that use Service Center as their user provider) no longer uses the traditional login screen from the app itself. Instead, it uses a centralized login screen. This only affects applications that use the **User_GetUnifiedLoginUrl** action to validate if there is an external login URL. The centralized login screen shows the app name that you can provide in the **ToolName** of the **User_GetUnifiedLoginUrl** optional parameter.

**Runtime**: Web

**Rationale**: This change provides a consistent login experience throughout the different applications that use Service Center as their user provider.

**Workaround**: None.
