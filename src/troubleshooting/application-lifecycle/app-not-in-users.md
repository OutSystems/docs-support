---
summary: How to act when your application isn't showing in the Users app.
Tags:
locale: en-us
guid: 7f3b01b4-47f6-42f1-b3f0-6b152794c516
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Application is not present in the Users app

## Symptoms

When acessing the **Users** application at `https://<environment_address>/Users`, on the **Applications** tab, you notice that one of your created apps isn't showing on the list.

![application list in users](images/app-not-in-users.png?width=400)


As a consequence, you also can't assign the app's role to an user.

![application not listed in the roles](images/app-not-in-users-role.png?width=400)


## Cause

This happens when a given app doesn't have a "Home" module defined. You can confirm if this is the case either in Service Studio or in Service Center.

### Identifying the app doesn't have a home module in Service Studio

Connect Service Studio to your environment and click the affected app.
When it doesn't have a "Home" module defined you'll notice that:

* the **Open in browser** button is disabled
* all it's modules with show with the "Set as Home" icon ![set home icon](images/app-not-in-users-set-home-ss.png)


![App detail in Service Studio](images/app-not-in-users-ss.png?width=400)

Once you have confirmed in Service Studio that your app doesn't have a home module defined, you can proceed to the resolution.


### Identifying the app doesn't have a home module in Service Center

Another way to confirm the cause is by accessing Service Center > Factory > Applications and click the affected app.

Examine the **Modules** list: an app that has a home module defined will display "(home)" after one of the modules' name.

This is how it looks when a home module is defined:

![Home module in Service Center](images/app-not-in-users-home-sc.png?width=400)

If your app doesn't have a home module it won't show the **(home)** tag in any of the modules.

![No home module in Service Center](images/app-not-in-users-sc.png?width=400)

Once you have confirmed this is the case, you can proceed to the resolution.

## Resolution

Define a home module for the app. 

Connect Service Studio to your environment and click the app you wish to set the home module.
In front of the module that should be the home module, click the "Set as Home" icon ![set home icon](images/app-not-in-users-set-home-ss.png)

The **Open in browser** button becomes enabled:

![Home module set in Service Studio](images/app-not-in-users-home-ss.png?width=400)

Go back to the Users application and on the **Applications** tab, your app now shows on the list and you can assign it's role to users.
