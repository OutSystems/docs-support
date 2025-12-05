---
summary: Learn how to resolve launch issues in OutSystems 11 (O11) due to missing permissions for configuration folders on both MacOS and Windows.
locale: en-us
guid: 8EE47E91-1685-47CA-8A64-50C4A5CD8150
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=2616:4337
tags: ide usage, reactive web apps, troubleshooting, permissions errors, cross-platform development
audience:
  - mobile developers
  - frontend developers
  - full stack developers
  - platform administrators
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# Cross-platform Service Studio cannot be launched due to missing permissions to create the configuration folder

## Symptoms

Cross-platform Service Studio doesn't load properly. The splash screen doesn’t disappear and a dialog is shown to warn users about missing permissions in the configuration folder.

![Error dialog indicating Service Studio cannot start due to missing configuration folder permissions.](images/permission-error-ss.png "Service Studio Permission Error Dialog")

## Cause

OutSystems cross-platform Service Studio needs a local directory to store configurations and other files. This directory is located in the user’s home area, therefore, the cross-platform environment must have permissions to create and read it (both in Windows and MacOS). However, in some cases, those permissions are lost.  

## Solution

Set the correct permissions to create the configuration folder.

### MacOS

#### **Using Terminal**

1. Search for **Terminal.app** in MacOS Spotlight and open it.

    ![MacOS Spotlight search showing Terminal.app as the top result.](images/terminal-mac.png "MacOS Terminal Search Result")

1. Go to the `~/.config` folder.

1. Set the owner and permissions for the **OutSystems** folder where `user` corresponds to the current `username`.

    * `sudo chown -R <user> Outsystems`

    * `sudo chmod -R 700 OutSystems`

1. Repeat steps 2 and 3 for the **Directory** folder.

    * `~/.local/share/OutSystems`

1. Open the cross-platform Service Studio again.

#### **Using Finder**

1. Search for **Finder.app** in MacOS Spotlight and open it.

    ![MacOS Spotlight search showing Finder.app as the top result.](images/finder-mac.png "MacOS Finder Search Result")

1. In the top menu, choose go to **Go** -> **Go to the folder**.

1. Enter `~/.config` and click **Go**.

    ![Dialog box for navigating to the '~/.config' folder in MacOS.](images/config-mac.png "MacOS Go to Folder Dialog")

1. Select the **OutSystems** folder.

1. Go to **File** -> **Get info**.

1. In the Sharing & Permissions section, select the line that corresponds to your username and change the **Privilege** value to **Read & Write**.

    ![Privilege dropdown menu showing 'Read & Write' selected for custom access.](images/privilage-mac.png "MacOS Folder Privilege Settings")

    If your username isn’t listed in the Name column:

    a. Click the lock icon and enter your password.

    b. Click the **Add+** button to add a new user.

    ![Dialog box for adding a new user to the Sharing & Permissions section in MacOS.](images/newuser-mac.png "MacOS Add New User Dialog")

    c. Select the line that corresponds to your username and change the **Privilege** value to **Read & Write**.

1. Click the ![The action icon used in MacOS context menus, resembling three horizontal dots.](images/actionicon.png "MacOS Action Icon")icon and choose **Make __ the owner**.

1. Click the ![The action icon used in MacOS context menus, resembling three horizontal dots.](images/actionicon.png "MacOS Action Icon") icon and choose **Apply to enclosed items**.

    ![Context menu in MacOS with the option 'Apply to enclosed items' highlighted.](images/encloseditems-mac.png "MacOS Apply to Enclosed Items Option")

1. Repeat steps a-c for the Directory folder `~/.local/share/OutSystems`.

1. Open the cross-platform Service Studio again.

For more information, see [Apple’s official guide to change permissions for files and folders on Mac](https://support.apple.com/en-ie/guide/mac-help/mchlp1203/mac).

### Windows

1. Open File Explorer and go to the ``C:\Users\<user>\AppData\Local`` folder changing ``user`` to your username.

1. Right click the **OutSystems** folder.

1. Select the **Security** tab.

    ![Security tab in Windows folder properties showing permissions for the OutSystems folder.](images/security-win.png "Windows Folder Security Properties")

1. In the **Group or username** section, select your username.

1. In the **Permissions** section, ensure that the **Modify** and **Read & execute** permissions have the **Allow** setting enabled.Otherwise, click the **Edit** button and enable the missing privileges.

1. Open the File Explorer again and go to the ``C:\ProgramData`` folder.

1. Right click the **OutSystems** folder and select **Properties**.

1. Select the **Security** tab.

1. Ensure that the **Users** group has the **Read & execute**, **List folder contents**, and **Read** permissions.

    ![Security tab in Windows showing the Users group with specific permissions for the OutSystems folder.](images/usersgroup-win.png "Windows Users Group Permissions")

1. Open the cross-platform Service Studio again.
