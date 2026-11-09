---
summary: Explore how to resolve access issues in OutSystems 11 (O11) when personal environments fall asleep due to inactivity.
locale: en-us
guid: 61c16e5f-94d2-4a3e-ba75-c40ead245a3c
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:404
tags:
  - Troubleshooting
audience:
  - Developer
  - Front-end developer
outsystems-tools:
  - none
coverage-type:
  - unblock
topic:
  - wake-sleeping-pe-o11
isautopublish: true
---

# Cannot reach apps on my personal environment

<div class="info" markdown="1">

This article applies to OutSystems 11 (O11) personal environments only.

</div>

## Symptoms

You're trying to access an app running on your O11 personal environment, but you're redirected to [http://www.outsystems.com/home/](http://www.outsystems.com/home/). A message tells you that your personal environment fell asleep or was deleted.

## Cause

Your O11 personal environment is asleep. This occurs when:

* You stopped developing for a while.
* Your apps aren't being used.

This happens as part of the recycling mechanism that saves resources for active personal environments.

## Resolution

Go to the [Trial Portal](https://www.outsystems.com/Portal/Trial_Portal) and log in with your OutSystems Community account. Select **Wake up** and wait a few seconds while the personal environment is restored.

![Screenshot of the OutSystems personal environment page with a notification that the environment fell asleep and a 'Wake up' button highlighted.](images/pe-sleep-usr.png "OutSystems Personal Environment Wake Up Interface")

## More information

OutSystems sends you an email letting you know that your personal environment will be recycled.

If you need your personal environment running 24/7, check your emails regularly. A couple of visits per week to your apps is enough to keep the environment active.
