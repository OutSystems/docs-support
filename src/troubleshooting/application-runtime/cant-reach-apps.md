---
summary: If you can't access the apps on your personal environment, go to www.outsystems.com/home and check if your environment has been recycled.
locale: en-us
guid: 61c16e5f-94d2-4a3e-ba75-c40ead245a3c
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:404
---

# Cannot reach apps on my personal environment

## Symptoms

You're trying to access an application running on your personal environment, but you're being redirected to [http://www.outsystems.com/home/](http://www.outsystems.com/home/) with a message telling you that your personal environment fell asleep or has been deleted.

## Cause

Your personal environment is asleep. This occurs if:

* you've stopped developing for a while or

* your apps aren't being used.

This happens as part the recycling mechanism to save resources for active personal environments.

## Resolution

Go to [http://www.outsystems.com/home/](http://www.outsystems.com/home/) and login with your OutSystems credentials. Click the **Wake up** button and wait a few seconds while the personal environment is restored.

![](images/pe-sleep.png)

## More information

OutSystems sends you an email letting you know that your personal environment will be recycled.

If you need your personal environment running 24/7, check your emails regularly. A couple of visits per week to your apps is enough to keep the environment active.

