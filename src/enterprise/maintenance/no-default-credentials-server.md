---
summary:
tags:
---

# No default credentials in Platform Server

Starting with Platform Server versions 10.0.1014.0 and 11.0.528.0, in most cases, you will need to define the password of the environment's Platform Server Administrator User ("admin") when installing/upgrading Platform Server.

This will be a required step in the following situations:

* When performing a new installation of a standalone environment.

* When upgrading Platform Server from a version older than the ones specified above and you're still using the default password of the Platform Server Administrator User.

## Changes in Platform Server installation/upgrade

### Installing a new standalone environment

After installing Platform Server, when running Configuration Tool either using the graphical user interface (GUI) or in unattended mode, you will need to define the password for the Platform Server Administrator User.

To set the password, do one of the following:

* If you're running Configuration Tool in GUI mode, follow the instructions provided in the Installation Checklist after installing Platform Server.

* If you're running Configuration Tool in unattended mode, use the command-line parameter SetPlatformServerAdminPassword described in the [Configuration Tool Command Line Reference](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/Unattended_Installation_and_Upgrade/Configuration_Tool_Command_Line_Reference).

Configuration Tool will update the environment database with an encrypted version of the password.

Note: If you're going to register this new environment in LifeTime, **make sure you set the password to the same password of LifeTime's "admin" user.** Due to LifeTime's regular [data synchronization process](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle#lifetime-synchronization-process), you may find issues if these passwords do not match.

### Upgrading a standalone environment

Note: You must upgrade the LifeTime environment **before** upgrading any other environment.

After installing Platform Server, when running Configuration Tool either using the graphical user interface (GUI) or in unattended mode, you will need to define the password for the Platform Server Administrator User **if you're still using the default password** for the Platform Server Administrator User.

To set the password, do one of the following:

* If you're running Configuration Tool in GUI mode, follow the instructions provided in the Installation Checklist after installing Platform Server.

* If you're running Configuration Tool in unattended mode, use the command-line parameter SetPlatformServerAdminPassword described in the [Configuration Tool Command Line Reference](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/Unattended_Installation_and_Upgrade/Configuration_Tool_Command_Line_Reference).

Configuration Tool will update the environment database with an encrypted version of the password.

**Make sure you set the password to the same password of LifeTime's "admin" user.** Due to LifeTime's regular [data synchronization process](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle#lifetime-synchronization-process), you may find issues if these passwords do not match.

## Farm Installations

The requirement of defining a new password is not applicable when you are installing/upgrading a new server in a farm environment since the new server will connect to the same database as other servers in the farm and they will also use a copy of the server.hsconf configuration file, common to all environment servers.

