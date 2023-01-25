---
summary: This article describes how to restore the OutSystems database to a different database server.
tags:
locale: en-us
guid: 346a4452-9ede-4346-aeb3-9455a48e99cc
app_type: traditional web apps, mobile apps, reactive web apps
---

# Restore OutSystems database to a different DB Server

This article explains the necessary steps to execute in OutSystems Platform Server when you need to restore the database to a new server.

It doesn't cover the necessary steps to execute on the database. For detailed instructions on how to backup and restore the database, please refer to the documentation of your database management system.


## Prerequisites

To apply this procedure, the following requirements must be met:

* Have an **on-premises** installation in **.NET stack**.

* The old database server replaced **hosts only the database**.

* The database was on server A and will be moved to server B.

* The database remains intact, without alterations to the data or database users.

* No changes will be done to the application servers.


If you are looking to create a copy of an existing environment while maintaining the original environment, check [this article](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Migrate_an_Environment_Using_a_Database_Clone) instead.


<div class="info" markdown="1">

It is advisable that you keep the old database server running until the operation is complete, in case you need to rollback.

</div>

## Restoring Process

### Step 1. Prepare for the restoring process

Start the process by backing up the old database and restoring it to the new database server:

1. Prepare the new database server by executing the steps of the installation checklist (Task: First Install, Role: Database).

1. Stop the IIS and the OutSystems Services in all front-ends.

1. Back up the old database.

1. Restore the backup to the new database server.

### Step 2. Update the OutSystems application servers to use the new database server

After restoring the database to the new database server, you need to run the [Configuration Tool](https://success.outsystems.com/Documentation/11/Reference/Configuration_Tool) in all the OutSystems application servers.

<div class="info" markdown="1">

In **farm environments**, start by executing the steps below in the **deployment controller** server, and then repeat the same steps for each **front-end server**.

</div>

#### For OutSystems 10

In each application server, execute the following steps:

1. Open the Configuration Tool.

1. Confirm the database connection details in **Database** and  tabs, and change them if necessary.

1. Click **Apply and Exit**.

1. When prompted to run Service Center installation, answer **No**.

1. When prompted to restart OutSystems Services, answer **Yes**.

1. Start IIS and ensure all OutSystems Services are running.

#### For OutSystems 11

In each application server, execute the following steps:

1. Open the Configuration Tool.

1. Confirm the database connection details in Database related tabs (**Platform**, **Session** and **Log**) and change them if necessary.

1. Start IIS.

1. Click **Apply and Exit**.

1. When prompted to run Service Center installation, answer **Yes**.

1. When prompted to restart OutSystems Services, answer **Yes**.

1. Ensure all OutSystems Services are running.

1. Create a solution with all the modules and click [**Apply settings**](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Applying_Configurations_in_Service_Center#Apply_Pending_Settings_to_a_Set_of_Modules).

1. If there is a warning to republish the modules, publish the solution by clicking **Publish** for the **Current Running Version**.


### Step 3. Decommission the old database server 

After making sure that everything is working as expected, you can decommission the old database server.
