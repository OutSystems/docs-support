---
summary: Check what's the installed version of the several components of OutSystems - Service Studio, Integration Studio, LifeTime and Platform Server.
tags:
locale: en-us
guid: 98a6a460-e03e-4610-ab03-d9e1eda2239c
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Check what OutSystems version you are using

In the context of a support case, or when exploring the OutSystems documentation, it's useful to know what version and revision of OutSystems you have. This article explains how to obtain such information from the OutSystems components.

## Service Studio and Integration Studio

To display the version of Service Studio and Integration Studio click **Help** > **About**.

![Service Studio version](images/what-version-ss.png)


## LifeTime

Once logged into LifeTime, the version will display at the bottom of the page.

![LifeTime version](images/what-version-lt.png)

## Platform Server

At Platform Server, three pieces compose a healthy instalation: the Platform Server binaries instaled, Service Center and System Components.

In a proper instalation, all these components will have the same version. You can however, check their version separately.

### Platform Server binaries

In the OutSystems Cloud, this version will always be the same that's seen in Service Center. 
If, in a self-managed instalation, you suspect there's any inconsistency, you can check the installed version of the Platform Server by accessing the server remotely and opening Configuration Tool. Go to **Help** > **About** to see the version.

### Service Center

To obtain the Service Center version, login and check the right sidebar.

![Service Center version](images/what-version-sc.png)

### System Components

Obtain the System Components version by logging in to Service Center, clicking **Factory**, then **Applications**, and search for **System Components**. Check the version on the description.

![System Components version](images/what-version-sys-sc.png)

You can also check the version of each module that's a part of System Components by clicking the application to see the modules list.

![Version of the modules of System Components](images/what-version-module-sc.png)
