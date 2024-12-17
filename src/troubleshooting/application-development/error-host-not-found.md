---
summary: OutSystems 11 (O11) troubleshooting guide for resolving the "Host not found" error when connecting to a personal environment.
locale: en-us
guid: 1772e0b0-ad78-4f95-851f-89323b298934
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:559
tags: troubleshooting, connectivity issues, outsystems cloud, environment management, error handling
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# There was an error contacting outsystemscloud.com - Host not found

## Symptom

When trying to connect to your personal environment from the IDE, you get the following error:

`There was an error contacting [my].outsystemscloud.com. Host not found.`

## Cause

* Bad internet connection

* Your personal environment has been recycled after a long period of inactivity

## Resolution

Since you're reading this, you can assume your internet connection is working fine. On your IDE, try reconnecting to your personal environment again.

If the problem has not been solved yet, it's probable that you haven't used your personal environment in quite some time, so it fell asleep or was deleted. 

### Step 1 

Go to `https://<yourpersonal>.outsystemscloud.com` and check the state of your environment.

* If you can see your applications, then your personal environment is up and running and you **should** be able to connect to it from the IDE.

* If you are redirected to [https://www.outsystems.com/home/](https://www.outsystems.com/home/), then your personal environment fell asleep or was deleted.


### Step 2

If your personal environment fell asleep, you just need to wake it up. Click the **Wake up** button.

![OutSystems dashboard showing a notification that the personal environment fell asleep with a 'Wake up' button highlighted.](images/pe-sleep.png "OutSystems Personal Environment Sleep State")

If your personal environment is deleted due to a long period of inactivity, click the **Fetch me a new environment** button.

![OutSystems dashboard indicating the personal environment was deleted due to inactivity with a 'Fetch a new environment' button highlighted.](images/pe-del.png "OutSystems Personal Environment Deletion Notice")

A new environment will be provisioned for you, with the same URL you had before. However, your applications will not be available in the new environment. After you create a new personal environment, you can re-publish your apps.
