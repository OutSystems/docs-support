---
guid: A4910443-3665-402E-AD55-0ADE98073729
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise-Customers?type=design&node-id=3361-267&mode=design
summary: Discover the manual license verification process for OutSystems 11 (O11) in self-managed environments.
tags: license compliance, self-managed environments, telemetry communication, network setup
audience:
  - platform administrators
  - full stack developers
outsystems-tools:
  - service center
coverage-type:
  - unblock
  - remember
---

# License verification

## What is the license verification process?

The license verification process allows customers to manually upload license consumption information to OutSystems using the Customer Portal.

License verification is for customers with self-managed environments using production servers that do not automatically communicate telemetry to OutSystems due to their network setup. This online verification site allows the secure transfer of usage data. As stated in the [OutSystems Subscription Agreement](https://www.outsystems.com/legal/master-subscription-agreement/#3) Clause 3.6: Verification of License Compliance, customers are intended to complete their compliance verification once per calendar quarter.

[This article](https://success.outsystems.com/documentation/11/setup_and_maintain_your_outsystems_infrastructure/setting_up_outsystems/outsystems_network_requirements/) details the ports you must open to enable automatic telemetry communication.

## How do I download the license verification file for my production server?

You can download the license verification file for a production service by doing the following:

1. Open **Service Center** for your production server, with Administrator rights.
1. In Service Center, go to **Administration** and then **Licensing**.
1. From the **Licensing** menu, select **Audit License** option as shown in the image below:

    ![Screenshot highlighting the Audit License option in the Service Center's Licensing menu.](images/license-audit-sc.png "Service Center Audit License Option")

    A file with the name `OutSystems.Audit.txt` is downloaded.

1. Access your **Customer Portal** and **upload** the file in the **License Verification** panel:

    ![Screenshot of the License Verification panel in the Customer Portal with an upload option.](images/license-verification.png "Customer Portal License Verification Panel")

<div class="info" markdown="1">    

Make sure you download the file from the production server with the same activation code you want to verify in the Customer Portal.

</div>

After you upload the file, the Customer Portal will validate and securely register the license consumption information. You can track the history of all the license verification files you uploaded to the Customer Portal in the **Upload History** tab above.
