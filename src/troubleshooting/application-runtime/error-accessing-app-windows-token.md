---
summary: Resolve the "Could not create Windows user token" error in OutSystems 11 (O11) by adjusting 'Run As' settings.
locale: en-us
guid: 6d5b466c-0819-4e81-a080-6089039c0394
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=620:33
tags: error resolution, .net framework, application deployment, user authentication, platform operations
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - service studio
  - service center
coverage-type:
  - unblock
---

# Error accessing application - Could not create Windows user token from the credentials specified in the config file

## Symptoms

In an OutSystems Platform running on .NET stack, one (or more) of the following happens in a specific eSpace:

* It is not possible to access any screens in the eSpace

* It is not possible to call any web-services from the eSpace

* All BPT processes are stuck and giving errors

* All timers are stuck and giving errors.

* A publication error occurs in the final stage

When looking at the error log, the error message is generic, but the details show the below detail:

![Screenshot of a parser error message indicating inability to create a Windows user token due to logon failure.](images/error-accessing-app-windows-token_0.png "Parser Error Message Detail")

  `<b> Parser Error Message: </b>Could not create Windows user token from the credentials specified in the config file. Error from the operating system 'Logon failure: unknown user name or bad password.<br>'<br><br>`

## Cause

This error is thrown because you have configured a "Run As" user for your eSpace that does not exist, or doesn't have sufficient privileges to run in the server

## Resolution

Solving this problem involves either:

1. Removing the "Run As" credentials, if they are not needed. This is the solution for all cloud customers, since "Run As" is not available for cloud customers.

2. Fixing the privileges for the user.

### Method 1:

To remove the "Run As" credentials, access the details of the eSpace, and check the Operation tab. You will see the username set up. To remove these credentials, simply delete the value, click **Apply Run As settings**. 

![Screenshot of the Operation tab in OutSystems Service Center showing where to remove 'Run As' credentials.](images/error-accessing-app-windows-token_1.png "eSpace Operation Tab")

After this change, Service Center informs you that you need to republish the eSpace so the change gets effective.

![Notification message indicating that the eSpace needs to be republished to use new settings after removing 'Run As' credentials.](images/error-accessing-app-windows-token_2.png "eSpace Republish Notification")

### Method 2:

To fix the user credentials, first identify the user that is running the eSpace. In our example, it is jpi90871

![Screenshot highlighting the 'Run As' username field in the eSpace configuration settings.](images/error-accessing-app-windows-token_3.png "Run As User Configuration")

After you have found the user, log in to your server, and in Manage Users and Roles, open the IIS_IUSRS group and add the user to it:

 ![Screenshot of the Computer Management window showing the process of adding a user to the IIS_IUSRS group.](images/error-accessing-app-windows-token_4.png "Adding User to IIS_IUSRS Group")

## Properties

Applies to OutSystems Platform for .NET, all versions.

