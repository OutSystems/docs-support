---
summary: If you request a license for an environment, we'll send an email with it. Go to the environment management console to install the new license.
en_title: 04 How to install a license file
locale: en-us
guid: 901b198a-6fac-460e-b661-9a76c2e1093b
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise%20Customers?node-id=3215:460
---

# How to install a license file

<div class="info" markdown="1">

This article applies to on-premises environments. For OutSystems Cloud, the services team manages the license installation automatically, updating it or renewing it as necessary.

</div>

Follow these steps to install the license file on your environment:

1. Navigate to the environment management console at `http://<yourenvironment>/ServiceCenter`;

2. Click the '**Administration**' tab, and navigate to the '**Licensing**' submenu;

3. Use the '**Backup License**' (1) link to download the license currently installed. It's always a good idea to keep backups;

4. Click the '**Upload New License**' (2) link, to install the new license.

![](images/licensing-update-ss.png)

<div class="info" markdown="1">

License files are bound to a given environment / Serial Number and if you try to install them on other environments you'll get an error.

If that happens you should confirm that you have the correct file by comparing the Serial Numbers shown in Service Center and Licensing Portal.
</div>

## More information

You should also check:

* [How to get a license file for an environment](get-license-for-env.md)

* [Identify OutSystems infrastructure and runtime environments](https://success.outsystems.com/support/licensing/identify_outsystems_infrastructure_and_runtime_environments/)
