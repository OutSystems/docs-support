---
summary: We'll help you transfer applications when you upgrade. Contact your account manager for help in getting this process started.
locale: en-us
guid: 2505a258-5861-4143-8251-a39e03821bf7
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Move apps from your Personal to a subscription license

You can transfer applications when you upgrade from a Personal or Trial Edition to a paid subscription.

In order to transfer applications from a Personal or Trial environment to an enterprise environment:

 * Go to Service Center in the Personal Environment.  

 * Go to Factory > Solutions

 * Select “New Solution”

 * Enter a name for the Solution and click “Save.”

 * This will bring up the Solution screen.  Click on the “Components” tab.

 * In the “Associate Components with Solution” input, enter a module you wish to transfer.  Enter all of the applicable modules.

 * If the component is dependent on other modules that are not in the destination environment, make sure  “Include dependencies as components” is checked and click “Associate.”

 * Click “Save”  You will then go back to the Solution screen.

 * Click “Download” on the “Current Running Version” of the Solution. This will compile a file with the .osp extension that you will be able to Download.


* Upload this file to the [IP Portal](https://www.outsystems.com/homeIpp/IPP_Page.aspx) in order to remove IP protections.  This will then email you a link to download the version of the file that can be installed in the new environment.

* Once you have this file, in the Enterprise Environment, go to the development environment instance of Service Center and go to Factory > Solutions

* Click “Upload and Publish a Solution” 

* Choose the file and upload it - this will upload and publish all of the components of the solution into the new environment

 

Note that this does not transfer data, only the modules themselves.

**FAQs:**

*Can I transfer more apps from my Personal Edition in the future?*

Following the terms of use for the Personal Edition, you can share your apps with the Community, through the Forge. If you do not intend to share your apps with the Community, develop them in your paid Enterprise Edition. OutSystems evaluates each transfer request, and only considers one request for each new customer.
