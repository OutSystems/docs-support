---
summary: Troubleshoot a permissions-related error when you upgrade or install the Platform Server.
tags: 
---

# Installation fails with service permissions error

## Symptoms

Your on-premises installation fails when you install or upgrade to Platform Server 11.12.0 or later. You see the following message about a failure to change permissions of services.

![](images/install-fail-permissions.png)

## Cause

In earlier versions, the Platform Server runs the Deployment Control service and the Scheduler service in the context of the Windows Local System account. This account has higher permissions than these services require. Starting with Platform Server 11.12.0, installation includes a powershell script that creates two new user accounts with lower permissions. The Deployment Control and Scheduler services then run within the context of these lower-privilege accounts. See the table below for account details.

Active Directory settings can block the installation script from creating users and from changing policies associated with them. If the script finds that these services run with the Local System account, and it can't create new accounts, you see this error message. 

## Resolution

Change your Active Directory settings to allow user and policy changes. You can use the Group Policy manager in Windows to change settings.

Notes: 
* The Deployment Service requires higher privileges and continues to run in the context of the Local System account. 
* To check your current settings, open the Windows Services application and locate the Deployment Controller Service and Scheduler Service. Check the account name in the Log On As column. 
* In your current environment, if the Deployment Control Service and Scheduler Service don’t run in the context of the Local System user, then the script doesn't try to create new users. It assumes you’ve already changed permissions manually, and the installation completes. 

## Service and user details
The following table summarizes permissions for the new user accounts for each impacted service.

 OutSystems Service   |      New user associated with service      |  User permissions |
|----------|:-------------:|------|
| Deployment Control Service |  OSControllerUser | Full control on the platform folder <br/>Local policies added:<ul><li>Log on as service</li><li>Log on as batch job</li><li>Create symbolic links</li></ul>  |
| Scheduler Service |    OSSchedulerUser   | Full control on the platform folder <br/>Local policies added:<ul><li>Log on as service</li><li>Log on as batch job</li><li>Create symbolic links</li></ul>  | |

