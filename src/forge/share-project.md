---
summary: Know the details of sharing a project in the OutSystems Forge.
tags: forge_support_sharing
---

# Sharing a project

## What project format should I use? { #formats }

The recommended format to share a project in Forge is using an **OutSystems Application Package** (.oap).

OutSystems Application Packages (.oap) are fully functional applications or components. They have automatic installation and dependency management capabilities that provide the best possible experience for others in the community.

If you want to share a simple component or snippet that's not ready to run on its own (for example, a how-to, a coding pattern, or a small widget), share a single **OutSystems Module** (.oml). A module allows other users to easily open and inspect its content for reuse.

## How do I export an OutSystems Application Package for sharing? { #export-oap }

In Service Studio, on the main Development tab where the list of applications appears, click the application you want to open. On the application page where the modules appear, click **Download**.

Alternatively, you can download the application in the Service Center console:

1. To access Service Center, open the application in Service Studio, click the **Environment** menu, and select **Application Management in Service Center...**. This redirects you to the application details page in Service Center, under the **Factory** section.

2. On the application details page, click the **Download** button.

## How do I export an OutSystems Module for sharing? { #export-oml }

Open the module in Service Studio, click the **Module** menu and select the **Export > Save As...** option.

Alternatively, you can download the module in the Service Center console:

1. To access Service Center, open the module in Service Studio, click the **Module** menu and select **Module Management in Service Center...**. This redirects you to the module details page in Service Center, under the **Factory** section.

2. On the module details page, click the **Download Published Version** button.

## How do I publish a component? { #publish }

Before publishing your OutSystems component to Forge, make sure it follows [the best practices](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices).

Once your component is ready, follow the steps below to publish it to Forge.

### Before you publish

1. Make sure you [remove the unused dependencies](https://success.outsystems.com/Documentation/11/Getting_started/Service_Studio_Tips_and_Tricks#Make_sure_you_Remove_Unused_Dependencies) from your component.

1. [Download the application package (.oap)](#export-oap) for your component. If you're sharing a very simple component that's not ready to run on its own, you can opt to [download only the module (.oml)](#export-oml); otherwise, the [recommended format](#formats) is an application package (.oap). If the file is too big, consider compressing any used image files or resources. The maximum file size you can upload to Forge is 256MB.

1. [Download the application package (.oap)](#export-oap) of the [demo application](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices#demo). Again, consider compressing any used image files or resources if the file is too big.

### Publish the component to Forge

Having the component and demo files, publish your component to the Forge:

1. Log into [Forge](https://www.outsystems.com/forge/) and click **New Component**.

1. Upload the **Component file** that you downloaded previously.

1. Upload the **Demo application file** that you downloaded previously.

1. Provide the component **Details**. By default, the **component name**, the **icon**, and the **description** are the ones defined during the development. You can change these descriptions after you publish.

1. In **Preview URL**, enter the URL for the **Try Now** option. The URL should display a sample, a demo, or tutorial screens that can also be available inside the demo application. Host your preview on a public server, such as a [Personal Environment](../personal/whats-a-personal.md).

1. Upload **screenshots** that best illustrate a component's features, main use cases, and behavior.

1. Enter a **Detailed description** for your component. Follow the [best practices](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices#name-desc) and make sure it fully describes the component's features and options.

1. Enter the project **Version**. Keep in mind that the numbers are unique. Forge suggests a version number, but you can change it. The version is visible on the main page and in the versions tab. Assign an incremental number for each new version update so people can easily identify the latest version.

1. Under **Requirements**, Forge indicates the corresponding **Platform Version**. You can select the **Stack** and the **Supported Database**. This information helps users know if their environment is compatible with your component.

1. Select at least one **Category/Subcategory** for your component. The category helps users find your component.

1. Add any relevant **Tags**. Tags help users to find your component and to filter published components.

1. Review the component's **dependencies**.

1. If your component has a complete first version and is ready for use in production, click **Publish** to publish a stable release. Alternatively, you can select **Publish as Under Development** if you are still building and improving the component, but you want to make it available for community testing.

After publishing your component, make sure you add [clear and concise documentation](https://success.outsystems.com/Documentation/Best_Practices/Development/Forge_components_best_practices#docs) to guide developers using it.
