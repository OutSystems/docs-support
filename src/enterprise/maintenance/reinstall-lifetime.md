---
summary: This article describes how to remove the infrastructure management console (LifeTime) from a shared environment and installing it in a new dedicated environment.
tags:
---
# Reinstall the infrastructure management console in a dedicated environment

This article describes how to remove the infrastructure management console (LifeTime) from a shared environment and installing it in a new dedicated environment.

![](images/reinstall-lifetime-dedicated-env-diag.png?width=700)

This operation applies only to **on-premises installations**.

<div class="info" markdown="1">

Once LifeTime is installed in an existing environment, reinstalling LifeTime in a dedicated environment will cause the loss of LifeTime specific data (Performance Monitor data, application tagging history and change log).

</div>

## Prerequisites

To reinstall LifeTime in a new dedicated environment the following requirements must be met:

* Have an **on-premises** installation.

* Have an [available licensing slot](https://www.outsystems.com/licensing) to register the new LifeTime dedicated environment.

* The **LifeTime version** you are installing must be able to manage the **Platform Server version** running in your OutSystems environments.

* The operation is performed by a user with the built-in **Administrator** role in Service Center.

* All the environments registered in the original LifeTime (eg. Development, Test, Production) are **synchronized** and no synchronization is on-going.

* The original LifeTime environment must have **no LifeTime plugins installed**, otherwise, you might not be able to remove LifeTime’s applications.

## Remarks

* Reinstalling LifeTime in a different environment **keeps all application data in the environments controlled by LifeTime** (eg. Development, Test, Production).

* The following **LifeTime specific data will be lost**:

    * LifeTime Analytics data / Performance Monitor
    * Application tagging history
    * Change log

* During the whole LifeTime reinstall operation, guarantee that **no one executes the following actions**:

    * Stage applications using LifeTime.
    * Any operation within User Management (Users, Teams, Roles, Authentication Mode, Service Accounts).

* You will need to **manually configure** the following information in the new LifeTime dedicated environment:

    * Users Roles and Teams.
    * Authentication Mode and Service Accounts, if used.

* The migration of any **LifeTime plugin** you might have is **not in the scope of this operation**. Make sure to backup and remove any LifeTime plugin from the original LifeTime environment before you start this operation. You can install your LifeTime plugins again after LifeTime reinstall operation is completed.

* From version OutSystems 11 onwards, **LifeTime doesn't support farm configuration**. You must install a single server with both Deployment Controller and Server roles.

## Reinstall LifeTime in a dedicated environment

### Step 1. Prepare a new dedicated environment for LifeTime

1. Download the latest [LifeTime Management Console binaries](https://www.outsystems.com/goto/lifetime-installer) from the downloads area.

1. Follow [LifeTime's installation checklist](https://www.outsystems.com/goto/checklist-lifetime) to install LifeTime in a new dedicated environment. As LifeTime **doesn't support farm configuration**, you must select the combination "Deployment Controller + Server" in the checklist to install a single server with both roles.

1. Get a [license file](https://www.outsystems.com/licensing) for the new LifeTime dedicated environment and apply the license in the new environment.

<div class="info" markdown="1">

We recommend installing the latest LifeTime version.

If you need to install LifeTime component of OutSystems 10 or previous version, you must download and install LifeTime from the Platform Server binaries.

</div>

### Step 2. Save original LifeTime configurations

1. Go to the original LifeTime, `https://<original-lifetime-environment>/lifetime`.

1. Login as Administrator.

1. Write down all your User Management configurations - it will be needed later to replicate the same structure in the new LifeTime dedicated environment:

    * Users, Roles and Teams
    * Authentication Mode
    * Service Accounts

<div class="info" markdown="1">

Tip: You can use [LifeTime Services API](<https://success.outsystems.com/Documentation/10/Reference/OutSystems_APIs/LifeTime_Services_API>) to retrieve Users, Roles and Teams from the original LifeTime environment.

</div>

### Step 3. Disable LifeTime from the original environment

1. Go to the **INFRASTRUCTURE** tab and choose **Manage Environments**.

1. For all registered environments, choose **Edit** and select **Unregister environment**. After unregistering all environments, you will see the following screen:

    ![](images/reinstall-lifetime-02.png)
 
1. Go to the Service Center console of the original LifeTime environment and log in as Administrator, `https://<original-lifetime-environment>/ServiceCenter`.

1. Go to the **Factory** section and choose **LifeTimePerformanceMonitor** application from the Applications list.

1. Disable **LifeTimePerformanceMonitor** application.

    ![](images/reinstall-lifetime-03.png)
 
1. From the Applications list, choose **LifeTime** application and **Disable** it.

1. From the Applications list, choose **LifeTimeSDK** application and **Disable** it.

### Step 4. Configure new LifeTime dedicated environment

1. Go to the new LifeTime dedicated environment, `https://<new-lifetime-environment>/lifetime`.

1. Login as Administrator.

1. Go to the **USER MANAGEMENT** area and [create the Roles](<https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Teams/Create_an_IT_Role>) you had in the original LifeTime environment, configuring the corresponding permissions.

    <div class="info" markdown="1">

    Tip: If you used LifeTime Services API to retrieve the Roles from the original LifeTime environment, use the retrieved data to create the Roles in the new dedicated environment. Check [BackupLTPermissions](<https://www.outsystems.com/forge/4043/>) component in OutSystems Forge as an example on how to retrieve these data from LifeTime.
    
    </div>

1. Go to the **INFRASTRUCTURE** area and [register all your OutSystems environments](<https://success.outsystems.com/Support/Enterprise_Customers/Installation/Configure_the_infrastructure_management_console>).

1. Now that all the environments are registered, configure your [Teams](<https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Teams/Create_an_IT_Team>) and [specific application Roles](<https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Teams/Grant_IT_Roles_for_a_Specific_Application>) as you had in the original LifeTime environment.

1. Configure the Authentication Mode setting and Service Accounts as you had in the original LifeTime environment.

### Step 5. Delete LifeTime’s applications from the original environment

If the original LifeTime environment version is **lower than Platform Server 10.0.804.0**, you won't be able to delete LifeTime’s applications. In this case, skip the steps below, leaving the applications disabled.  

If the original LifeTime environment version is **Platform Server 10.0.804.0 or upper**, do the following to delete LifeTime’s applications:

1. Go to the Service Center console of the original LifeTime environment and log in as Administrator, `https://<original-lifetime-environment>/ServiceCenter`.

1. Go to the **Factory** section and choose **LifeTimePerformanceMonitor** application from the Applications list.

1. Delete **LifeTimePerformanceMonitor** application.

    ![](images/reinstall-lifetime-07.png)
 
1. From the Applications list, choose **LifeTime** application and **Delete** it. 

1. From the Applications list, choose **LifeTimeSDK** application and **Delete** it.

LifeTime is now reinstalled in a dedicated environment.
