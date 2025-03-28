---
summary: Learn how to release an environment serial number in OutSystems 11 (O11) via the Customer Portal for operations like upgrades and server transfers.
locale: en-us
guid: 22ff6d6a-ab3a-4c2d-8c5a-13ce0d118750
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise%20Customers?node-id=616:0
tags: licensing, environment management, server upgrades, platform server administration, outsystems operations
audience:
  - platform administrators
  - tech leads
  - infrastructure managers
outsystems-tools:
  - none
coverage-type:
  - apply
---

# How to free up an existing environment in licensing

This article explains how you can release an environment serial number in the [Customer Portal](https://www.outsystems.com/licensing/), which may be necessary when performing the following operations:

* upgrade the OutSystems Platform Server; 

* transfer an OutSystems environment across servers;

* change server hardware;

* sunset an existing OutSystems environment.

On any of these operations, it's possible that the serial number of the environment changes. If that's the case, you'll need to release the serial number associated with the environment and register a new one. Once you've done that, you can download an updated license file.

<div class="info" markdown="1">

If you need assistance while installing and managing your server licenses [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support).

</div>

## Releasing an existing environment

Access the [Customer Portal](https://www.outsystems.com/licensing/) and select your infrastructure:

![Screenshot of the Customer Portal showing the infrastructure selection dropdown menu.](images/free-up-environment-portal.png "Customer Portal Infrastructure Selection")

Look up the environment to release (making sure that the serial number matches):

![Screenshot highlighting the 'Release Environment' option for a development environment in the Customer Portal.](images/free-up-environment-release.png "Release Environment Option")

1. Click **Release Environment**.

1. Fill in the reason for the release.

1. Click **Release**.

<div class="info" markdown="1">

If your infrastructure has been flagged for abuse the environment release won't be immediate: it will trigger a request to OutSystems to review your request.

</div>
