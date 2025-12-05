---
summary: This guide details the process for installing a license file in OutSystems 11 (O11) on-premises environments.
locale: en-us
guid: 901b198a-6fac-460e-b661-9a76c2e1093b
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise%20Customers?node-id=3215:460
tags: license management, outsystems service center, on-premises environment, environment configuration
audience:
  - platform administrators
outsystems-tools:
  - service center
coverage-type:
  - apply
---

# How to install a license file

<div class="info" markdown="1">

This article applies to on-premises environments. For OutSystems Cloud, the services team manages the license installation automatically, updating it or renewing it as necessary.

</div>

Follow these steps to install the license file on your environment:

1. Navigate to the environment management console at `http://<yourenvironment>/ServiceCenter`;

1. Click the '**Administration**' tab, and navigate to the '**Licensing**' submenu;

1. Use the '**Backup License**' (1) link to download the license currently installed. It's always a good idea to keep backups;

1. Click the '**Upload New License**' (2) link, to install the new license.

![Screenshot of the OutSystems Service Center Licensing page highlighting the 'Backup License' and 'Upload New License' options.](images/licensing-update-ss.png "OutSystems Service Center Licensing Screen")

<div class="info" markdown="1">

License files are bound to a given environment / Serial Number and if you try to install them on other environments you'll get an error.

If that happens you should confirm that you have the correct file by comparing the Serial Numbers shown in Service Center and Licensing Portal.
</div>

## More information

You should also check:

* [How to get a license file for an environment](get-license-for-env.md)

* [Identify OutSystems infrastructure and runtime environments](https://success.outsystems.com/support/licensing/identify_outsystems_infrastructure_and_runtime_environments/)
