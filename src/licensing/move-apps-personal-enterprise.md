---
summary: OutSystems 11 (O11) facilitates the transfer of applications from Personal or Trial environments to a paid subscription.
locale: en-us
guid: 2505a258-5861-4143-8251-a39e03821bf7
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/TzqCbVlN2j4nadunA7q8VU/Licensing?node-id=0:1
tags: application migration, environment management, outsystems deployment, solution management
audience:
  - full stack developers
  - platform administrators
outsystems-tools:
  - service center
coverage-type:
  - apply
---

# Move apps from your Personal environment to a subscription license

You can transfer applications when you upgrade from a Personal or Trial Edition to a paid subscription.

To transfer applications from a Personal or Trial environment to an enterprise environment, follow these steps:

1. Go to Service Center in the Personal Environment.  

1. Go to **Factory** > **Solutions**.

1. Click the **New Solution** link.

    ![Screenshot of the Service Center showing the Solutions tab with a highlighted 'New Solution' link.](images/moveapp-solutions-sc.png "Service Center Solutions Screen")

1. Enter a name for the Solution and click **Save**.

    ![Screenshot of the 'Create Solution' form in Service Center with fields for Name and Description and a highlighted 'Save' button.](images/moveapp-createsol-sc.png "Create New Solution Form")

1. On the **Solution** screen, select the **Components** tab.

1. In the **Associate Components with Solution** field, enter the module you want to transfer. Enter all of the applicable modules.

    ![Screenshot of the 'Associate Components with Solution' section in Service Center with a field to enter the module name.](images/moveapp-associate-sc.png "Associate Components with Solution")

1. If the component is dependent on other modules that are not in the destination environment, ensure that the **Include dependencies as components** checkbox is selected and click **Associate**.

    ![Screenshot showing the option to 'Include dependencies as components' checked in the 'Associate Components with Solution' section.](images/moveapp-include-dep-sc.png "Include Dependencies Option")

1. Click **Save**

    You are brought back to the **Solution** screen.

1. Click **Download** on the **Current Running Version** of the solution. This will compile a file with the .osp extension that you will be able to Download.

1. To remove IP protections, upload this file to [Intellectual Property Protection](https://www.outsystems.com/IPP).

    ![Screenshot of the Intellectual Property Protection (IPP) Rights Validation page with fields for Email, Destination Activation Code, and file upload.](images/moveapp-ipp.png "Intellectual Property Protection Rights Validation")

    You will receive an email with a link to download the version of the file that can be installed in the new environment.

1. Once you have this file, in the Enterprise Environment, go to the development environment instance of Service Center and go to **Factory** > **Solutions**.

1. Click **Upload and Publish a Solution**.

1. Choose the file and upload it.

    This uploads and publishes all of the components of the solution into the new environment.

    **Note**: This does not transfer data, only the modules themselves.

**FAQs**

_Can I transfer more apps from my Personal Edition in the future?_

Following the terms of use for the Personal Edition, you can share your apps with the Community through the Forge. If you don't intend to share your apps with the Community, develop them in your paid Enterprise Edition.

**Note**: OutSystems reserves the right of preventing transfer requests that are not meant to be part of the one-time migration process from a Personal Environment to a paid subscription.
