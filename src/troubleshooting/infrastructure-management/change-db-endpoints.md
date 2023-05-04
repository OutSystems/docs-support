---
summary:
locale: en-us
guid: ADFE09B6-85D4-48B0-84D6-30E2DF16CA2C
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# How to change the OutSystems database endpoints used by applications

<div class=”info” markdown=”1”>

This procedure applies only to self managed infrastructures on OutSystems 11.

</div>

## Context

Upon the Platform Server installation, the OutSystems applications will access the database using the connection details inserted in the [Configuration Tool](https://success.outsystems.com/Documentation/11/Reference/Configuration_Tool) for each database.
The Platform Server requires three databases to be configured, namely:

* [Platform database](https://success.outsystems.com/Documentation/11/Reference/Configuration_Tool/Platform_Tab);
* [Log database](https://success.outsystems.com/Documentation/11/Reference/Configuration_Tool/Log_Tab);
* [Session database user](https://success.outsystems.com/Documentation/11/Reference/Configuration_Tool/Session_Tab).

## Use case

You simply want to change the database address (e.g., the domain name needs to be updated) and want the OutSystems applications to connect to the new address.
If you were looking for a different use case, please check the other documented articles we have related to database:

* [Restore OutSystems database to a different DB Server](https://success.outsystems.com/support/enterprise_customers/maintenance_and_operations/restore_outsystems_database_to_a_different_db_server/) to move from a database server A to a database server B using an exact clone

* [Migrate an Environment Using a Database Clone](https://success.outsystems.com/support/enterprise_customers/maintenance_and_operations/migrate_an_environment_using_a_database_clone/) if you want to create a new OutSystems environment with a clone of the data from an existing database.

## Procedure
This document guides you through the necessary steps to change the database endpoints and make those effective on the OutSystems applications.

<div class= “warning” markdown =”1”>

This procedure assumes that both old/current database address and new address are accessible. Otherwise, the procedure will cause downtime from the moment the old/current database address is unavailable or not responding until the procedure finishes.

</div>

In each application server (servers with roles Front-End or Deployment Controller), execute the following steps:

1. Open the Configuration Tool.
1. Change the database server address in the Database related tabs (**Platform**, **Session** and **Log**).
1. Click **Apply and Exit**.
1. If you are prompted to run Service Center installation, answer **Yes**.
1. If you are prompted to restart OutSystems Services, answer **Yes**.
1. Ensure all OutSystems Services are running

After configuring the new database addresses in all servers:

1. Access Service Center > Factory > Solutions and create a solution with all modules. Fore more details on how to achieve this, check the [Creating and using an All Components solution](https://success.outsystems.com/documentation/how_to_guides/devops/creating_and_using_an_all_components_solution/) article.

1. [Apply settings](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Applying_Configurations_in_Service_Center#Apply_Pending_Settings_to_a_Set_of_Modules) to all modules of the solution.

1. If there is a warning to republish the modules, publish the solution by clicking **Publish** for the **Current Running Version**.
