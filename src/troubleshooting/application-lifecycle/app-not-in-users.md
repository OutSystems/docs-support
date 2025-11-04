---
summary: OutSystems 11 (O11) applications may not appear in the Users app if they lack a defined "Home" module.
locale: en-us
guid: 7f3b01b4-47f6-42f1-b3f0-6b152794c516
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3330:2692
tags: application configuration, user management, troubleshooting, application deployment
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# Application is not present in the Users app

## Symptoms

When acessing the **Users** application at `https://<environment_address>/Users`, on the **Applications** tab, you notice that one of your created apps isn't showing on the list.

![Screenshot showing the absence of an application in the Users app's Applications tab.](images/app-not-in-users.png "Missing Application in Users App")

As a consequence, you also can't assign the app's role to an user.

![Screenshot depicting the inability to assign roles to a user due to the missing application.](images/app-not-in-users-role.png "Unable to Assign Roles for Missing Application")

## Cause

This happens when a given app doesn't have a "Home" module defined. You can confirm if this is the case either in Service Studio or in Service Center.

### Identifying the app doesn't have a home module in Service Studio

Connect Service Studio to your environment and click the affected app.
When it doesn't have a "Home" module defined you'll notice that:

* the **Open in browser** button is disabled
* all it's modules with show with the "Set as Home" icon ![Icon indicating the option to set a module as the Home module in Service Studio.](images/app-not-in-users-set-home-ss.png "Set as Home Icon in Service Studio")

![Screenshot of Service Studio with the Open in Browser button disabled due to no Home module being set.](images/app-not-in-users-home-disabled-ss.png "Disabled Open in Browser Button in Service Studio")

Once you have confirmed in Service Studio that your app doesn't have a home module defined, you can proceed to the resolution.

### Identifying the app doesn't have a home module in Service Center

Another way to confirm the cause is by accessing Service Center > Factory > Applications and click the affected app.

Examine the **Modules** list: an app that has a home module defined will display "(home)" after one of the modules' name.

This is how it looks when a home module is defined:

![Screenshot showing a module marked as (home) in the Service Center, indicating it is set as the Home module.](images/app-not-in-users-home-sc.png "Home Module Defined in Service Center")

If your app doesn't have a home module it won't show the **(home)** tag in any of the modules.

![Screenshot of the Service Center with no modules marked as (home), indicating a missing Home module.](images/app-not-in-users-sc.png "No Home Module in Service Center")

Once you have confirmed this is the case, you can proceed to the resolution.

## Resolution

Define a home module for the app.

Connect Service Studio to your environment and click the app you wish to set the home module.
In front of the module that should be the home module, click the "Set as Home" icon ![Icon indicating the option to set a module as the Home module in Service Studio.](images/app-not-in-users-set-home-ss.png "Set as Home Icon in Service Studio")

The **Open in browser** button becomes enabled:

![Screenshot of Service Studio after setting a Home module, with the Open in Browser button now enabled.](images/app-not-in-users-home-ss.png "Home Module Set in Service Studio")

Go back to the Users application and on the **Applications** tab, your app now shows on the list and you can assign it's role to users.
