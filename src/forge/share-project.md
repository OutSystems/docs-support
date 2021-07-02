---
summary: Know the details of sharing a project in the OutSystems Forge.
tags: forge_support_sharing
---

# Sharing a Project

## What project formats are accepted? { #formats }

The recommended format to share a project in Forge is using an **OutSystems Application Package** (.oap).

By using OutSystems Application Packages (.oap) to share fully functional applications or components, you benefit from the OutSystems automatic installation and dependency management capabilities, thus providing the best possible experience for others in the community.

If you want to share a simple component or snippet that's not ready-to-run on its own (for example, a how-to, a coding pattern, or a small widget), sharing a single **OutSystems Module** (.oml) is the way to go. This allows other users to easily open and inspect its content for reuse.

## How do I export an OutSystems Application Package for sharing? { #export-oap }

Open the application in Service Studio and click the **DOWNLOAD** button.

Alternatively, you can download the application in the Service Center console:

1. To access Service Center, open the application in Service Studio, click the **Environment** menu and select **Application Management in Service Center...**. This redirects you to the application details' page in Service Center, under the **Factory** section.

2. On the application details' page, click the **Download** button.

## How do I export an OutSystems Module for sharing? { #export-oml }

Open the module in Service Studio, click the **Module** menu and select the **Export > Save As...** option.

Alternatively, you can download the module in the Service Center console:

1. To access Service Center, open the module in Service Studio, click the **Module** menu and select **Module Management in Service Center...**. This redirects you to the module details' page in Service Center, under the **Factory** section.

2. On the module details' page, click the **Download Published Version** button.

## How do I publish a component? { #publish }

Before publishing your OutSystems component to the Forge, make sure it follows [the best practices](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices).

Once your component is ready, follow the steps below to publish your component to the Forge.

### Before you publish

1. Make sure you [remove the unused dependencies](https://success.outsystems.com/Documentation/11/Getting_started/Service_Studio_Tips_and_Tricks#Make_sure_you_Remove_Unused_Dependencies) from your component.

1. [Download the application package (.oap)](#export-oap) of your component. If you're sharing a very simple component that's not ready-to-run on its own, you can opt to [download only the module (.oml)](#export-oml), otherwise the [recommended format](#formats) is an application package (.oap). If the file is too big, consider compressing any used image files or resources. The maximum file size you can upload to the Forge is 256MB.

1. [Download the application package (.oap)](#export-oap) of the [demo application](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices#demo). Again, consider compressing any used image files or resources if the file is too big.

### Publish the component to the Forge

Having the component and demo files, publish your component to the Forge:

1. Log into the [Forge](https://www.outsystems.com/forge/) and click **New Component**.

1. Upload the **Component's file** you downloaded previously.

1. Upload the **Demo application's file** you downloaded previously.

1. Provide the component's **Details**. By default, the **component name**, the **icon**, and **description** are the ones defined during the development of your component. These descriptions can be changed after publication.

1. In the **Preview URL**, enter the URL that will feed the **Try Now** option. This URL should link to either a sample, demo, or tutorial screens, that can also be made available inside the demo application. Your link should be hosted in a public server, such as a [Personal Environment](../personal/whats-a-personal.md).

1. Upload **screenshots** that best illustrate your component's features, the main use cases, and behavior. You should provide images with the size 500/600 x 280 px.

1. Enter the **Detailed description** of your component. Follow the [best practices](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices#name-desc) and make sure it fully describes your component's features and options.

1. Enter the project **Version**. Keep in mind that numbers are unique. The Forge will suggest a version number, but you can change it. Since this number will be visible in the versions of your component, you should assign incremental numbers to each new version update, so people easily know which is the most recent version.

1. Under **Requirements**, Forge indicates the corresponding **Platform Version**. You can select the **Stack** and the **Supported Database**. This will help users to know if they meet all the conditions to download and use your component.

1. Select at least one **Category/Subcategory** that best matches what your component is. This categorization will help users to find your component.

1. Add any relevant **Tags**. Tags help users find your component, and they also allow to filter published components.

1. Review the component's **dependencies**.

1. If your component has a complete first version and it's ready to be used by production applications, click **PUBLISH** to publish a stable release. You can opt by **PUBLISH AS UNDER DEVELOPMENT** if you are still building and improving the component and you want to make it available for community testing.

After publishing, make sure you add [clear and concise documentation](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices#docs) to better guide your fellow developers using your component.
