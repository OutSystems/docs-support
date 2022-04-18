---
summary: Causes and resolutions for the error ORA-00054 whem publishinh an OutSystems app via LifeTime, Service Center or Service Studio.
locale: en-us
guid: 16f6f208-8be4-4dc1-b5ac-2beff690af36
app_type: traditional web apps, mobile apps, reactive web apps
---

# ORA-00054 error when deploying an OutSystems app

## Symptoms

When trying to publish an module (via LifeTime, Service Center or Service Studio) the following error is presented.

`ORA-00054: resource busy and acquire with NOWAIT specified or timeout expired`

The error may also present in other situations where the platform needs to change the data model.

The environment runs on an Oracle database. 

## Cause

This error happens when a ALTER statement is run in an Oracle database and other transactions hold locks to that object. It can happen if you are trying to change a heavily used table during peak hours, or simply because the database is slightly slow.

## Resolution

To resolve this issue, one should increase the Oracle DDL Timeout setting. This can be done in the platform configuration, and must be done in all front-ends of the same environment:

### Method 1:

1. Open file server.hsconf in a text editor (for example, notepad or vim). This file can be found in the platform installation folder:

    * For .NET, typically `C:\Program Files\OutSystems\Platform Server`

    * For Java, typically `/opt/outsystems/platform`
 
2. Locate setting DDLLockTimeout under `<PlatformDatabaseConfiguration ProviderKey="Oracle">`. You should find a line similar to this:
`<DDLLockTimeout encrypted="false">600</DDLLockTimeout>`

Note that there is a similar setting for `<SessionDatabaseConfiguration ProviderKey="Oracle">`. Typically you don't want to change this one. 

3. Increase the value in the setting. For example, change `600` to `1200` or `1800`

4. Run the configuration tool:

    * For .NET, locate the shortcut in the Start menu. After opening the Configuration Tool, click "Apply and Exit". Allow restart of all services. You don't need to execute installation of Service Center;

    * For Java, run /opt/outsystems/platform/configurationtool.sh. Don't change any settings. Allow restart of all services. You don't need to execute installation of Service Center.

## More information

For more information on this topic, we suggest the following article on ORA-00054:

* [http://www.dba-oracle.com/t_ora_00054_locks.htm](http://www.dba-oracle.com/t_ora_00054_locks.htm)

## Properties

Applies to Platform 9 and above, .NET and Java stack running on Oracle database.

Last reviewed under 10.0.105.0
