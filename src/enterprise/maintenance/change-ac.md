---
summary: Instructions to replace the license of one existing infrastructure from one Activation Code to another.
locale: en-us
guid: 4a4212cb-75d1-4b18-bdfb-a1b4cdc6b1b6
app_type: traditional web apps, mobile apps, reactive web apps
---

# How to change the Activation Code of your infrastructure

<div class="info" markdown="1">

This procedure applies to self-managed environments only.

</div>

During the lifecycle of your subscription, you may need to replace the license of an existing infrastructure from one activation code to another. This could be for a number of reasons, including the following:

* Organization splitting
* Company mergers
* Changes to the license agreement with OutSystems

Changing the Activation Code of your infrastructure ensures that downtime is avoided and that your development activities continue as usual.

This article covers a scenario where a full infrastructure, including LifeTime, is moved from a source activation code AAA to a destination activation code BBB. It also covers a [rollback procedure](#rollback) in case of any problems. 

In this scenario, we begin with a single infrastructure containing the following environments:

* 1 LifeTime
* 1 Development
* 1 Quality
* 1 Production

![Infrastructure](images/change-ac-system.png)

This scenario still applies if you have more environments than the ones depicted, as long as the requirements of the following scenario are met:

* You're changing the activation of a full infrastructure, including LifeTime

* All the environments of that infrastructure are registered in LifeTime

<div class="warning" markdown="1">

Don't change your Activation Code if **any** of the following apply:

* Your infrastructure has environments that are either not registered in LifeTime or are registered in another LifeTime. 
* You don’t want to change the Activation Code of one or more environments controlled by this LifeTime.
* You don’t want to change the Activation Code of the LifeTime environment.

</div>

## Changing the Activation Code

Before changing the Activation Code,  read the complete procedure first. If you have any questions, contact [OutSystems Support](https://success.outsystems.com/Support). 

To move from the previous Activation Code (AAA in this text) to the new Activation Code (BBB in this text), follow these steps:

1. Pause all deployments to Production. Development activities in other environments can continue.

1. For all environments, backup the license file for the Activation Code AAA.

    a. Go to the [Licensing Portal](https://www.outsystems.com/licensing) and enter your old Production environment Activation Code AAA.

    b. Navigate to the serial number of the Production environment and obtain the license file. Keep the file for backup purposes.

    c. Save the file to disk and rename it to match the name of the environment.

1. Check if you have any modules with intellectual property protection:

    a. Install the OutSystems **ActivationCodeCheck** application.

      * For OutSystems 11, install [ActivationCodeCheck](./files/ActivationCodeCheck-O11.oap)

      * For OutSystems 10, install [ActivationCodeCheck](./files/ActivationCodeCheck-O10.oap)

    b. Open the application and log in with your IT user.

    c. If the message **IP protected modules present in the factory. Are you executing a license change?** is displayed , click **Start Wizard**. If this message is not displayed, proceed to step 4.  

1. For all environments, register and obtain the license file for Activation Code BBB from the [Licensing Portal](https://www.outsystems.com/licensing):

    a. Go to [Licensing Portal](https://www.outsystems.com/licensing) and enter your new Activation Code BBB.

    b. Register the serial number of the environment you’re currently working with and obtain the license file.

    c. In Service Center for the relevant environment, navigate to **Administration** > **Licensing**, and choose **Upload New License**. Upload the license file that you requested.

    d. Still on the licensing page, filter for the **Intellectual Property** feature.

    ![Check Intellectual Property feature in Service Center](images/change-ac-ipp-sc.png)

    If the Intellectual Property is **Protected** or **Unprotected**, continue to the next environment. 

    If not, your license is not prepared for the migration. For more information, see  [FAQ 3](#faqs) below.

### Test the changes 

To test if changing the Activation Code was successful, republish a module, for example, the ECT_Provider module.

1. Go to **Factory** > **Modules** and filter by **ECT_Provider**. 

1. Open the details of the module, locate the version that's currently published, and click **Publish** for that version.

    ![Publish a module](images/change-ac-publish-sc.png)

1. If it publishes successfully, you can repeat the procedure for the following environments. If you get any errors related to Intellectual Property, immediately pause the procedure for the other environments and jump to the [rollback procedure](#rollback).

### Rollback { #rollback }

Before rolling back, read the complete procedure first. If you have any questions, contact [OutSystems Support](https://success.outsystems.com/Support). 

To move to the previous Activation Code (AAA in this text), follow these steps:

1. Pause all deployments to the Production environment. 
Development activities on the other environments can continue.

1. Restore all license files (including those backed up in step 2 above), for all environments that have licenses from Activation Code BBB.

    a. In Service Center, for each environment, go to **Administration** > **Licensing**, and choose **Upload New License**. Upload each environment’s backed-up license file.

    b. Confirm that the Activation Code displayed is the old Activation Code AAA.

    ![Confirm you see the old Activation Code](images/change-ac-rollback-sc.png)

#### Test the rollback

After rolling back, test if the procedure was successful by republishing any module, for example, the ECT_Provider module.

1. Go to **Factory** > **Modules** and filter by **ECT_Provider**. 

1. Open the details of the module, locate the version that's currently published, and click **Publish** for that version.

    ![Publish a module](images/change-ac-publish-sc.png)

1. If you're rolling back, you likely encountered an issue while changing your Activation Code. Contact [OutSystems Support](https://success.outsystems.com/Support) to report the issues and to obtain assistance to change your Activation Code.

### FAQs { #faqs }

If something unexpected happens, refer to the Frequently Asked Questions below or reach out to [OutSystems Support](https://success.outsystems.com/Support), referencing this article and indicating the step at which something unexpected happened.

1. **I cannot find the serial number of my environment in the old Activation Code**

    Please contact OutSystems Support to obtain a license file in a different way. Before contacting Support, please confirm all environments which don't appear in the old Activation Code (AAA in the script) so you can ask for help for all those environments all at once.

1. **The license I uploaded from the old Activation Code AAA is not prepared for the migration**

    Please contact OutSystems Support to obtain a license file in a different way. Before contacting Support, please finish uploading all licenses to the environments, so you can provide the complete list of environments that don't mention "Intellectual Property: Ignore" so we can help assist for all environments at once.
    
1. **The license I uploaded from the new Activation Code BBB is not prepared for the migration**

    Please contact OutSystems Support so we can correct the license definition. Following that, you'll need to repeat the obtaining of the licenses for all environments under Activation Code BBB.
