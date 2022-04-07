---
summary:
tags:
locale: en-us
guid: c7a43888-5a32-42f9-ab2a-f479c076ad79
---

# Migrate an Environment Using a Database Clone

**This article applies to:**[OutSystems 11](https://success.outsystems.com/Support/Archive/What_version_of_OutSystems_Platform_am_I_using)              **Other versions available:**[10.0](https://success.outsystems.com/Support/Archive/10.0/Migrate_an_Environment_Using_a_Database_Clone)   [9.1](https://success.outsystems.com/Support/Archive/9.1/Migrate_an_Environment_Using_a_Database_Clone)   [9.0](https://success.outsystems.com/Support/Archive/9.0/Migrate_an_Environment_Using_a_Database_Clone)

<div class="info" markdown="1">
This procedure applies only to On-Premise Infrastructures 
</div>

During the application development life cycle there is often the need to use real data to properly test the applications. A common use case is using the data from the Production environment in a Pre-Production environment, ensuring the two environments have the same applications, data and other resources for adequate testing.

This guide describes how to clone an environment database to create an environment where you can test your applications.

**This guide does not address disaster recovery scenarios. Using the procedures detailed in this guide for disaster recovery might result in data loss.**

As it includes several steps, you may find it useful to print this guide to help you follow the procedure.

## Migrate an Environment with SQL Server Database

### Prepare the Database

#### Clone the Databases

For systems running OutSystems Platform with a Microsoft SQL Server database engine we recommend the use of database backup/restore operations before moving a database to another server or cloning a database to the same or another server. This will ensure a consistent state on every step of the process.

You may also use the detach/attach operations if you are simply changing the location of a database – details for this operation are not covered in this document. The final result should be a new database set up on the same or another database instance. In both cases, it’s important to understand if Platform and Log data are living in the same database. If not, cloning must be done for both Platform and Logging databases.

When restoring a database please consider the following important details (depending on the database engine and versions):

* Specify a different target catalog during the restore to avoid restoring over an existing and active database;

* Specify different database files during the restore to avoid errors when restoring existing files;

* Set the recommended database files growth configurations.

* Since the source database may bring information with it from the source environment, there are also some major issues to be taken into account:

    * The database server security context: it may or may not exist in the destination database server;

    * The Environment security context: we need to clean the Environment security context since it needs to be private for each Environment;

    * Selective Deployment Zones: there may exist Zones referencing Front-ends which won’t exist in the new environment;

    * The deployment Front Ends listing: it may be referring other Front-ends than the ones used by the environment that is being set up;

    * LifeTime registration information: the database may bring LifeTime configurations that needs to be removed;

After have successfully restored the database, some cleanup may be required to prepare for a new configuration. The following sections cover these topics. 

#### Clean up the security context

After restoring the database all users and security configurations will also be restored along with it. You will need to reconfigure the new security contexts.

Clean up the restored security contexts, as follows: 

***
1. In the database, expand the ‘Security’ folder and delete the Admin and Runtime users for both Platform and Logging databases (typically OSADMIN, and OSRUNTIME for Platform, and OSADMIN_LOG, OSRUNTIME_LOG for Logging). **Note that in Microsoft SQL Server 2008 you will need to delete the correspondent schemas first on the same database.**
***

<div class="warning" markdown="1">
Note that if there are still any objects (views, tables, stored procedures, etc.) in the restored database that depend on any of these users then you will need to change the object owner to dbo (evaluate the application level impact of this change) before being able to delete the users. 
</div>

#### Clean up the Environment security context

After restoring the database some Environment security context will also be restored along with it. Clean up the Environment security contexts, as follows:
***

1. Open SQL Server Management Studio (or another query editor), connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned database >  to use the appropriate database):

```
delete from ossys_parameter where name = 'ClientApplicationToken';
delete from ossys_parameter where name = 'privateKeyValidation';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.MobileLogin_AuthenticationHMACKey';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.MobileLogin_AuthenticationEncryptKey';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.References.AuthenticationEncryptKey';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.References.HashKey';
delete from ossys_Parameter where name = 'OutSystems.SystemComponents.Users.AuthenticationEncryptKey';
delete from ossys_Parameter where name = 'OutSystems.SystemComponents.Users.HashKey';
```

***

#### Clean up the configuration of mobile apps

If the environment you cloned had mobile apps already configured for iOS or Android, you will need to perform a cleanup and configure the mobile apps again. You will only be able to generate the mobile apps after you [configure their specific iOS and/or Android settings](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App), which you can do when it best suits your needs.

Do the following to clean up the existing mobile apps configuration:

***
1. Open SQL Server Management Studio (or another query editor), connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned database >  to use the appropriate database):

```
delete from ossys_App_Mobile_Config;
delete from ossys_Mobile_Certificate;
delete from ossys_Mobile_Config_Data;
```
***

#### Clean up Selective Deployment Zones

Configurations of Zones for deploying applications are stored in the Platform database. When copying the database from one environment to another with different Front-Ends your applications will not be deployed in the new environment.

As an example, imagine the following scenario:

* A Pre-Production environment with a single Front-End node

* A Production environment: a farm with 2 Front-End nodes and 2 Zones: an Internal zone for one Front-End node and an External zone for the other Front-End node.

When cloning the database of the Production environment, the Zones configuration is also cloned. Therefore, after restoring the database to set up the Pre-Production environment, the Zones configuration will not match the single Front-End node. This will cause applications not to be deployed in the Pre-Production environment.

To fix this all Zone configurations must be cleaned up from the restored databases. This will cause all modules to deploy to all front-ends in the Pre-Production environment. After the environment is running you may choose to recreate the zones if needed.
***
1. Open SQL Server Management Studio (or another query editor), connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned database >  to use the appropriate database):

```
delete from ossys_modulefrontend;
delete from ossys_moduleinternaladdress;
delete from ossys_platformconfig where name in (
    'Application Deployment Configuration',
    'Default Application Deploy Instance',
    'Previous Deployment Zone Used',
    'Previous Deployment Zone Key',
    'Configured Application Deploy');
```
***

#### Clean up the Front-End listing

The restored database will bring the list of Front-Ends from the source environment. When cloning the database for use in another environment those configurations must be cleaned up to prevent the platform from deploying to incorrect Front-Ends and cause misbehaviors and failure.

As an example, if you are restoring a clone of a Production environment into the Pre-Production environments and they are in the same network, not executing this cleanup will cause a deployment in Pre-Production to try to deploy applications to the Front-Ends of the Production environment, potentially causing application downtime and eventually runtime errors in that environment.

To avoid this you must always clean up the Front-End listing from the cloned database. This list is automatically populated when you reinstall the platform later on. 

***
1. Open SQL Server Management Studio (or another query editor), connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned database >  to use the appropriate database):

```
delete from ossys_server;
```
***

#### Clean Up the Multiple Database Schemas Configurations

In case your applications are being deployed in multiple schemas, you need to clean up the multiple schemas configurations. This will prevent your applications to connect to a wrong database once the OutSystems Platform is installed.
***
1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement:

```
update ossys_dbcatalog set password = ' ',username =' ' where name <> '(Main)';
```
***

#### Clean up Database Connections

If you have database connections defined, it's advisable that you save their configurations (e.g.: in text files) before performing the migration. You need to perform the Database Connections clean-up because the platform won't be able to open the configurations after the migration.
***
1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement: 

```
delete from ossys_dbconnection where NAME <>'$OS_LOG_DB_7e3e8ce0';
```
***

##### Extensions with Database Connections

If you have Extensions with Database Connections, you must change the Database Connection for the Extension Logical Databases, to remove records from the OSSYS_EXTENSION_DBCONNECTION. This will allow you to clean up all Database Connections afterward.

To do it: 

1. Go to Service Center

2. Select Factory > Extensions > Operation tab

3. In the Logical Databases change the Database Connection to *(not configured).*

4. Apply the changes.

    ![ ](images/migrate-env-db-clone_0.png)

 
<div class="warning" markdown="1">
Note that if you don't change the Database Connection you will incur an integrity constraint error related to the OSSYS_EXTENSION_DBCONNECTION.
</div>

#### Clean up an environment managed by LifeTime

When an environment is managed by LifeTime and its database is restored, LifeTime configurations need to be cleaned up. These configurations are used by LifeTime to identify the environment; keeping them in the cloned Platform database will cause misbehaviors in LifeTime.

As an example, imagine you have cloned the Production database into a Pre-Production environment. LifeTime already has a unique identifier for the Production environment. However, when you clone the database to Pre-Production you will have both environments, Production, and Pre-Production, with the same identifier, thus causing LifeTime to misbehave.

As such, you must always clean up that information and re-register the cloned environment in LifeTime. 
***
1. Open SQL Server Management Studio (or another query editor), connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned_database >  to use the appropriate database):

```
if exists (select * from information_schema.columns where table_name = 'ossys_PlatformSvcs_Observer') delete from ossys_PlatformSvcs_Observer;
if exists (select * from information_schema.columns where table_name = 'ossys_cloudservices_observer') delete from ossys_cloudservices_observer;
```
***

2. Open SQL Server Management Studio (or another query editor), connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned_database >  to use the appropriate database):

```
update ossys_Site_Property_Shared set property_value='' where site_property_definition_id in (
    	select site_property_definition_id
    from ossys_Site_Property_Shared
    inner join ossys_Site_Property_Definition on site_property_definition_id = ossys_Site_Property_Definition.id
    where ss_key = '1aaec1be-d60f-43d4-ba32-391f4c3080a6' or
    ss_key = '441f6eef-9c7f-4bb4-b3dd-7220272269ad'
);
```
***

3. In LifeTime:
1. Go to your LifeTime to unregister the environment in which the database was restored
2. Click in the ‘Infrastructure’ tab
3. Click in the ‘Manage Environments’ link
4. ‘Edit’ the environment in which the database was restored and click on the ‘Unregister environment’ link
 ***

In LifeTime:
1. Go to your LifeTime to register the environment in which the database was restored
2. Click in the ‘Infrastructure’ tab
3. Click in the ‘Manage Environments’ link
4. Click on the ‘Register Another Environment’ link and follow the instructions presented in LifeTime

***


#### ​Clean up an environment running LifeTime

If the environment you cloned is running Lifetime all of its configurations must be cleaned up to avoid the usage of the incorrect LifeTime instance.

As an example, if you have LifeTime running in the Production environment and you are copying the Production database to a Pre-Production environment, when restoring the database in Pre-Production LifeTime will be brought along too and it could be used by mistake.

To prevent this you must always clean up all LifeTime configuration in the cloned Platform database. 
***
1. Open SQL Server Management Studio (or another query editor), connect to the restored database and execute the following SQL statement on the newly restored Platform database (if needed run use < cloned_database >  to use the appropriate database):

```
select 'update ' + physical_table_name + ' set isactive=0' from ossys_entity inner join ossys_espace on espace_id = ossys_espace.id and ossys_espace.is_active = 1 where ossys_entity.ss_key = '3312b1cd-b12e-4a29-bcdc-51edcdd86ef1'
```
***

2. Copy the result of the previous SQL statement and run it.

***
3. Optionally, you can disable LifeTime from the environment to ensure it is no longer accessible. Simply go to Service Center, click the ‘Factory’ tab and in the application list click on the ‘LifeTime’ application. Once you are in the LifeTime details, click the ‘Take Offline’ button.
***

### Fresh Installation Using a Restored Database

This section focuses on scenarios in which you have to install a new OutSystems Platform from scratch on a single-node server (a server with both the Deployment Controller and Front-End services). The new installation is to use the restored database catalog. 

***
**1. Install the pre-requirements**
[Check the OutSystems Platform Installation guide](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems "OutSystems Platform Installation guide")
This will ensure software pre-requirements installation and correct configuration of the Platform Server
***
**2. Install OutSystems Platform**
Run OutSystems Platform installer to install OutSystems Platform.

***

**3. Configure the Platform Database**

  * Run the Configuration Tool and in the Platform tab configure the following properties according to the restored catalog:
 * The hostname of the database server (and instance name if required, e.g. mydbserver.mydomain\CORP);
 * The Platform database name of the restored catalog;
 * For each login account (Platform database Admin and Runtime), set a new username and password;
 * Press the ‘Grant Permissions’ button;
 * You’ll be prompted to enter the login credentials: use your SQL Server Administrative login (typically sa) and password;
 * For each login account, press the ‘Test Connection’ link. The connection to the database should be successful, otherwise review the credentials you have just entered above.
Finally, press the ‘Create/Update Database’ button.
**Don’t close the configuration tool yet.**

***

**4. Configure the Log Database**
In the Log tab of the Configuration Tool configure the following properties according to the restored catalog:
 * The hostname of the database server (and instance name if required, e.g. mydbserver.mydomain\CORP_LOG);
 * The Log database name of the restored catalog;
 * For each login account (Log database Admin and Runtime), set a new username and password;
 * Press the ‘Grant Permissions’ button;
 * You’ll be prompted to enter the login credentials: use your SQL Server Administrative login (typically sa) and password;
 * For each login account, press the ‘Test Connection’ link. The connection to the database should be successful, otherwise review the credentials you have just entered above.
Finally, press the ‘Create/Update Database’ button.
**Don’t close the configuration tool yet.**

***

**5. Configure the Platform Session Database**
In the Session tab of the Configuration Tool proceed as follows:
 * Set the hostname of the database server;
 * Set the catalog to a new ASPState catalog (or an existing one);
 * Set the Session User username and password to new values or existing ones;
 * Press the ‘Configure Session Database’ button. If you’re using an existing session database, all sessions in that database will be lost.
Finally, press the ‘Apply and Exit’ button of the Configuration Tool to apply all changes and exit. 

***

**6. Install Service Center**
In the dialog that shows up for installing Service Center, choose ‘Yes’ to make sure you will be running a fully compatible version of Service Center.
If a dialog asking to start the OutSystems Scheduler service and OutSystems SMS Connector service shows up, answer ‘No’ and proceed. 

***
**7. Upload your new environment license**
In the Administration section of Service Center, open the Licensing page, and request a new license for this environment, which should have a different serial number. Upon receiving the license, upload it in the Licensing page. 

***

**8. In Service Center, set the server to the desired purpose (Development, Non-Production or Production)**
Launch Service Center, log in as 'admin' user using the password of the restored environment, go to the Administration tab, open the ‘Environment Configuration’ page, and select ‘Development’, ‘Non-Production’  or ‘Production’ purpose. You may have to set the Default DNS Name of the environment, if not already set.
**It is strongly recommended to set the same name for the Default DNS Name and the Environment Name, to rapidly identify the environment in Service Center.** 

***

**9. Install Service Studio**
Run the ‘ServiceStudio-M.m.b.r.exe’ installation file and follow the instructions on screen.

***

**10. Install Integration Studio**
Run the ‘IntegrationStudio-M.m.b.r.exe’ installation file and follow the instructions on screen. 

***

**11. Multiple Database Schemas**
In case your applications are being deployed in multiple catalogs, you need to change Service Center configurations to start using the cloned catalogs.
In Service Center, go to ‘Administration’, and click ‘Database Catalogs’. For each catalog listed, change its configurations.

***

**12. Application Configurations Changes**
In case of environment replication, check the effective value of each Web Reference (in the module details page) and all Site Properties containing URLs or values pointing to other environments. If pointing to invalid or other environments, then update them accordingly. Cover also any other application level configurations stored on the database.

***

**13. Republish the entire factory**
Since the database brings its own factory, you should publish all modules to properly deploy them to the application server. Create a whole content solution (with all of the factory’s components) and publish it. 

***

**14. Start the Remaining OutSystems Services (optional)**
After all changes to the applications configuration are done, ensuring that connections to wrong environments do not occur, you may start OutSystems Scheduler Service.
**Please note that to avoid timers to run in this environment, the OutSystems Scheduler Service should be stopped and disabled which is done in the Services console of the Administrative Tools, or this front-end must have the ‘Execute Timers’ option disabled in the Front-End Lists in Service Center.**

***

### Reconfigure an Installation to Use a Restored Database

This section focuses on scenarios in which you’ll have to reconfigure an existing OutSystems Platform installation to use the newly restored database on a single-node server (server with both the Deployment Controller and Front-End services). 

***

1. Stop the OutSystems Services
Open the Services console of the Administrative Tools and stop the following OutSystems Services:
 * OutSystems Scheduler;
 * OutSystems SMS Connector;
 * OutSystems Deployment; 
 * OutSystems Deployment Controller;
 * OutSystems Log.

***

2. Stop IIS
Open a command prompt window and stop the IIS using the following command:
```
1. iisreset /stop
```

***

3. Configure the Platform Database
Run the Configuration Tool and in the Platform tab configure the following properties according to the restored catalog:
 * The hostname of the database server;
 * The Platform database catalog name of the restored catalog;
 * For each login account (Platform database Admin and Runtime), set a new username and password;
 * Press the ‘Grant Permissions’ button;
 * You’ll be prompted to enter the login credentials: use your SQL Server Administrative login (typically sa) and password;
 * For each login account, press the ‘Test Connection’ link. The connection to the database should be successful, otherwise review the credentials you have just entered above.
Finally, press the ‘Create/Update Database’ button.
**Don’t close the configuration tool yet.**

***

4. Configure the Log Database
In the Log tab of the Configuration Tool configure the following properties according to the restored catalog:
 * The hostname of the database server;
 * The Log database catalog name of the restored catalog;
 * For each login account (Log database Admin and Runtime), set a new username and password;
 * Press the ‘Grant Permissions’ button;
 * You’ll be prompted to enter the login credentials: use your SQL Server Administrative login (typically sa) and password;
 * For each login account, press the ‘Test Connection’ link. The connection to the database should be successful, otherwise review the credentials you have just entered above.
Finally, press the ‘Create/Update Database’ button.
**Don’t close the configuration tool yet.**

***

5. Configure the Platform Session Database
In the Session tab of the Configuration Tool proceed as follows:
 * Set the hostname of the database server;
 * Set the catalog to a new ASPState catalog (or an existing one);
 * Set the Session User username and password to new values or existing ones;
 * Press the ‘Configure Session Database’ button. **If you’re using an existing session database, all sessions in that database will be lost.**
**Don’t close the configuration tool yet.**

***

**6. Start IIS**
Open a command prompt window and start IIS using the following command:

```
iisreset /start
```

***

**7. Apply the changes and exit**
Press the ‘Apply and Exit’ button of the Configuration Tool to apply all changes and exit.

***

**8. Upload your new environment license**
In the Administration section of Service Center, open the Licensing page, and request a new license for this environment. Upon receiving the license, upload it in the Licensing page.

***

**9. In Service Center, set the server to the desired purpose (Development, Non-Production or Production)**
Launch Service Center, log in as ‘admin’ user using the password of the restored environment, go to the Administration tab, open the ‘Environment Configuration’ page, and select the ‘Development’, ‘Non-Production’ or ‘Production’ purpose. You may have to set the Default DNS Name of the environment, if not already set.
**We strongly recommend you to set the same name for the Default DNS Name and the Environment Name, to rapidly identify the environment on Service Center.** 

***

**10. Multiple Database Schemas**
In case your applications are being deployed in multiple catalogs, you need to change Service Center configurations to start using the cloned catalogs.
In Service Center, go to ‘Administration’, and click ‘Database Catalogs’. For each catalog listed, change its configurations. 

***

**11.Application Configurations Changes**
In case of environment replication, check the effective value of each Web Reference (in the module details page) and all Site Properties containing URLs or values pointing to other environments. If pointing to invalid or other environments, then update them accordingly. 

***

**12. Republish the entire Factory**
Since the database brings its own factory, you should publish all modules to properly deploy them to the application server. Create a solution with the whole content (with all of the factory’s components) and publish it. 

***

**13. Start the Remaining OutSystems Services (optional)**
After all changes to the applications configuration are done, ensuring that connections to wrong environments do not occur, you may start OutSystems Scheduler Service.
**Please note that to avoid the timer to run in this environment the OutSystems Scheduler Service should be stopped and disabled which is done in the Services console of the Administrative Tools, or this front-end must have the ‘Execute Timers’ option disabled in the Front-End Lists in Service Center.**

***

## Migrate an Environment with Oracle Database

### Prepare the Database

#### Export the Schemas

It is recommended to use Oracle Data Pump to export the platform schemas and import them back on an existing database. You can find further information on how to use the Oracle Data Pump technology in the following white papers:

* [Data Pump in Oracle Database 11g Release2](http://download.oracle.com/otndocs/products/database/enterprise_edition/utilities/pdf/datapump11gr2_techover_1009.pdf)

***

**1. Find Out the Schemas that Need to be Cloned**
Before using the expdp Data Pump client, you need to find out which schemas need to be cloned.
In the ‘Platform and Log’ tabs of the Configuration Tool you can find out the users that the OutSystems Platform uses for both Application and Log data. By default these are:
 * Platform database:
    * OSADMIN
    * OSRUNTIME
 * Log database:
    * OSADMIN_LOG
    * OSRUNTIME_LOG
If you are deploying your applications to multiple schemas, you will also need to find out the schemas containing the application data.
Go to the ‘Administration’ > ‘Database Schemas’ area in Service Center to find out what schemas need to be cloned. 

***

**2. Clone the Schemas**
Using the expdp Data Pump client, clone the schemas identified in the previous step.
As an example, the following command creates a clone of the OSADMIN and OSRUNTIME schemas into the ‘production.dmp’ file:

```
expdp \"/ as sysdba\" DUMPFILE=production.dmp schemas=\('OSADMIN','OSRUNTIME'\)
```

***

**3. Check the Logs**
Ensure that the export process has been successful by inspecting the expdp Data Pump client output.

***


#### Import the Schemas

Once you have the dump file with the clone of the schemas, you need to import them into an existing database.  

If you are importing the schema to the same database instance that you exported the schema from, you must revoke the permissions of the cloned schema user over the original schema.

***

**1. Create the Tablespaces and Schemas**
Before using the impdb Data Pump client, you need to ensure the table spaces and schemas exist in the destination database.
**Customize the Platform Server database creation script.**
You can find it in the Deployment Controller Server under OutSystems Platform Server Installation directory, in dB\runtime_oracle_creation.sql.
This file allows you to create users, tablespaces and grants the necessary permissions. By default, when executing this file, the following objects will be created:
 * Users: OSADMIN, OSRUNTIME
 * Tablespaces: OSSYS, OSIDX, OSUSR
 * Grants:
    * OSADMIN: Create Session, Create View, Create Table, Alter Session, Create Sequence, Create Procedure, Create Trigger
    * OSRUNTIME: Create Session
**Customize the Log Server database creation script**
You can find it in the Deployment Controller Server under OutSystems Platform Server Installation directory, in dB\logging_creation_oracle.sql.
This file allows you to create users, tablespaces and grants the necessary permissions. By default, when executing this file, the following objects will be created:
 * Users: OSADMIN_LOG, OSRUNTIME_LOG
 * Tablespaces: OSSYS_LOG, OSIDX_LOG, OSUSR_LOG
 * Grants:
    * OSADMIN_LOG: Create Session, Create View, Create Table, Alter Session, Create Sequence, Create Procedure, Create Trigger
    * OSRUNTIME_LOG: Create Session
 
If you are deploying your applications to multiple schemas, you will also need to create the necessary tablespaces, schemas and grants in the destination database. Go to the ‘Administration’ > ‘Database Schemas’ area in Service Center and click ‘Download Creation Script’ to download the necessary schemas creation scripts. Customize the creation scripts and execute them in the destination database.
Please check with your Database Administrator how to do this according to your database environment. At the very least, you should make sure the file paths, tablespaces and users don't clash with existing objects in the database. You'll need the usernames, passwords and tablespaces used in this script to configure Platform Server later on.

***

**2. Import the Schemas**
Import all schemas and tablespaces at the same time, using the impdp Data Pump client. In this command you need to **indicate how the cloned tablespaces and schemas are mapped** in the destination database.
As an example, the following command imports the cloned schemas, and remaps the old table spaces and schemas into new ones. 

```
impdp \"/ as sysdba\" DUMPFILE=production.dmp REMAP_SCHEMA=OSADMIN:NEW_OSADMIN REMAP_SCHEMA=OSRUNTIME:NEW_OSRUNTIME REMAP_SCHEMA=OSLOG:NEW_OSLOG REMAP_TABLESPACE=OSUSR:NEW_OSUSR REMAP_TABLESPACE=OSSYS:NEW_OSSYS REMAP_TABLESPACE=OSIDX:NEW_OSIDX REMAP_TABLESPACE=OSLOG:NEW_OSLOG
```

Notice that since the tablespaces and schemas were already created in the previous step, the impdb Data Pump client will display a warning, but succeeds in restoring the schemas.

***

#### Clean up the Environment security context

Some Environment security context is stored in the Platform database and when moving the database from one environment to another with need to clean it.

Clean up the Environment security contexts, as follows:

***

1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement:

```
delete from ossys_parameter where name = 'ClientApplicationToken';
delete from ossys_parameter where name = 'privateKeyValidation';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.MobileLogin_AuthenticationHMACKey';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.MobileLogin_AuthenticationEncryptKey';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.References.AuthenticationEncryptKey';
delete from ossys_Parameter where name = 'OutSystems.HubEdition.References.HashKey';
delete from ossys_Parameter where name = 'OutSystems.SystemComponents.Users.AuthenticationEncryptKey';
delete from ossys_Parameter where name = 'OutSystems.SystemComponents.Users.HashKey';
COMMIT;
```
***

#### Clean up the configuration of mobile apps

If the environment you cloned had mobile apps already configured for iOS or Android, you will need to perform a cleanup and configure the mobile apps again. You will only be able to generate the mobile apps after you [configure their specific iOS and/or Android settings](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App), which you can do when it best suits your needs.

Do the following to clean up the existing mobile apps configuration:

***

1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement on the newly restored database (if needed run use < cloned database >  to use the appropriate database):

```
delete from ossys_App_Mobile_Config;
delete from ossys_Mobile_Certificate;
delete from ossys_Mobile_Config_Data;
COMMIT;
```

***


#### Clean Up Selective Deployment Zones

Configurations of Zones for deploying applications are stored in the Platform database and when moving the database from one environment to another with a different configuration of Front-Ends, your applications won’t be deployed in the new environment.

As an example, imagine that you’re setting up a Quality environment with a single Front-End node from a clone of a Production environment which is a farm with 2 Front-End nodes and 2 Selective Deployment Zones: an Internal zone for one Front-End node and an External zone for the other Front-End node. When cloning the schemas of the Production environment, the Zones configuration is also cloned.

Therefore, after restoring the schemas to set up the Quality environment, the Zones configuration won’t match with the single Front-End node, thus causing applications not to be deployed in the Quality environment.

As such, the Zones configurations must be cleaned up from the restored database schemas, to make sure that applications are deployed to the right Front-Ends in the target environment.

***

1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement

    ```
    ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;
    ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

    delete from ossys_modulefrontend;
    delete from ossys_moduleinternaladdress;
    delete from ossys_platformconfig where name in (
        'Application Deployment Configuration',
        'Default Application Deploy Instance',
        'Previous Deployment Zone Used',
        'Previous Deployment Zone Key',
        'Configured Application Deploy');
    COMMIT;
    ```

    **Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.

***


#### Clean Up the Front-Ends Listing

Since the restored database schemas may bring deployment configurations of Front-Ends from the source environment, those configurations must be cleaned up to avoid the applications deployment to use incorrect Front-Ends and cause misbehaviors and failure.

As an example, imagine that you’re restoring a clone of a Production environment into a Pre-Production or Quality environments, which are in the same network. Keeping the Production deployment configurations in the Pre-Production/Quality databases would cause the deployment process of these environments to deploy applications to the Front-Ends of the Production environment, thus causing application downtime and eventually runtime errors.

As such, you must always clean up the Front-End listing that is what identifies the existing Front-Ends in an environment - the list is automatically populated.

***

1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement: 
```
1. ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;

2. ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

3. delete from ossys_server;

4. COMMIT;

5. /


```
**Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.

***


####  Clean Up the Multiple Database Schemas Configurations

In case your applications are being deployed in multiple schemas, you need to clean up the multiple schemas configurations. This will prevent your applications to connect to a wrong database once OutSystems Platform is installed.

***

1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement: 
```
1. ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;

2. ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

3. 
 
4. update ossys_dbcatalog set password = ' ',username =' ' where name <> '(Main)';

5. COMMIT;

6. /

  ```
 ** Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.
  
  ***
 

#### Clean up Database Connections

If you have database connections defined, it's advisable that you save their configurations (e.g.: in text files) before performing the migration. You need to perform the Database Connections clean-up because the platform won't be able to open the configurations after the migration.

***
1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement: 
```
1. ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;

2. ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

3. 
  
4. delete from ossys_dbconnection where NAME <>'$OS_LOG_DB_7e3e8ce0';

5. COMMIT;

6. /

 ```
** Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.
 
 ***


#### Clean Up an Environment Managed by LifeTime

When your environment is managed by LifeTime and you restore its database you need to clean up some configuration that was done by LifeTime. This information is used by LifeTime to identify the environment and keeping it cloned from the original database will origin some misbehavior in LifeTime.

As an example, imagine you have cloned the Production database schemas into a Pre-Production environment. LifeTime already has a unique identifier for the Production environment. However, when you clone the database to Pre-Production you will have both environments, Production and Pre-Production, with the same identifier, thus causing LifeTime to misbehave.

As such, you must always clean up that information and re-register the cloned environment in LifeTime.

***

1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement: 
```
01. ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;

02. ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

03. 
 
04. DECLARE v_exists NUMBER(10,0);

05. BEGIN

06.
 
07. select Count(*) INTO v_exists

08. from user_tables where table_name = 'OSSYS_PLATFORMSVCS_OBSERVER';

09. 
 
10. IF v_exists > 0 THEN

11. EXECUTE IMMEDIATE 'delete from OSSYS_PLATFORMSVCS_OBSERVER';

12. END IF;

13. 
 
14. COMMIT;

15. 
 
16. END;

17. /

  ```
 **Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.
  
  ***
  
2. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement: 
```
01. ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;

02. ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

03.
 
04. update ossys_Site_Property_Shared set property_value=' ' where site_property_definition_id in (

05. 
 
06. select site_property_definition_id

07. from ossys_Site_Property_Shared

08. inner join ossys_Site_Property_Definition on site_property_definition_id = ossys_Site_Property_Definition.id

09. where ss_key = '1aaec1be-d60f-43d4-ba32-391f4c3080a6' or ss_key = '441f6eef-9c7f-4bb4-b3dd-7220272269ad'

10. 
 
11. );

12. 

13. COMMIT;

14. /

```
**Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.

  ***
  
3. In LifeTime:
1.Go to your LifeTime to unregister the environment in which the database was restored
2.Click in the ‘Infrastructure’ tab
3.Click in the ‘Manage Environments’ link ‘
4.Edit’ the environment in which the database was restored and click on the ‘Unregister environment’ link.

***

4. In LifeTime:
1.Go to your LifeTime to unregister the environment in which the database was restored
2.Click in the ‘Infrastructure’ tab
3.Click in the ‘Manage Environments’ link
4.Click on the ‘Register Another Environment’ link and follow the instructions presented in LifeTime.

***


#### Clean up an Environment Running LifeTime

Since the restored database schema may bring configurations of a LifeTime installation, configurations must be cleaned up to avoid the usage of the incorrect LifeTime instance. As an example, suppose you have LifeTime running in the Production environment and you are migrating that Production environment to a Pre-Production environment. When restoring the database in PreProduction, LifeTime will be brought along too and it could be used by mistake.

As such, you must always clean up the cloned LifeTime. 

***
1. Open a query editor tool, connect to the restored Platform database and execute the following SQL statement:
```
1. ALTER SESSION SET NLS_COMP=LINGUISTIC NLS_SORT=BINARY_AI;

2. ALTER SESSION SET CURRENT_SCHEMA = OSADMIN;

3.
 
4. select 'update ' || physical_table_name || ' set isactive=0'

5. from ossys_entity inner join ossys_espace on espace_id = ossys_espace.id and ossys_espace.is_active = 1

6. where ossys_entity.ss_key = '3312b1cd-b12e-4a29-bcdc-51edcdd86ef1'

```
**Note**: Replace OSADMIN with your Admin user for the Platform database if you changed the default value.

***
 
2. Copy the result of the previous SQL statement and run it.
  
***

3. Optionally, you can disable LifeTime from the environment to ensure it is no longer accessible. Simply go to Service Center, click the ‘Factory’ tab and in the application list click on the ‘LifeTime’ application. Once you are in the LifeTime details, click the ‘Take Offline’ button.

***


### Fresh Installation Using a Restored Database

This section focuses on scenarios in which you have to install a new OutSystems Platform from scratch on a single-node server (a server with both the Deployment Controller and Front-End services running). The new installation is to use the restored database schemas. 

***

**1. Install the pre-requirements**
Check the OutSystems Platform Installation guide.
This will ensure software pre-requirements installation and correct configuration of the Platform Server
 
***
**2. Install the OutSystems Platform**
Run the Platform installer to install the Platform
  
***

3. Configure the Platform Database
Run the Configuration Tool and in the Platform tab configure the following properties according to the restored database:
 * Set **‘Oracle Database’** in the drop-down list **DBMS**;
 * Set the Oracle database to be used by configuring the **Server Instance field**;
 * Fill in **Admin user** in the Admin section using the database login previously created for the Admin role in the Platform database
 * Fill in **Tablespace** and **Index Tablespace** fields in the Admin section with the System Tablespace and the Index Tablespace previously created
 * Fill in **Runtime user** in the Runtime section using the database login previously created for the Runtime role in the Platform database
 * Fill in **Tablespace** field in the Runtime section with the Runtime Tablespace previously created
 * Test all users to confirm correct connectivity. For this, click Test Connection for each of the users configured.
 * Create the Platform Database schema by clicking the Create/Upgrade Database button. 
 Do not close the Configuration Tool at this point - further tasks are to be performed.

***

**4. Configure the Log Database**

In the Log tab of the Configuration Tool configure the following properties according to the restored database:
 * Set **‘Oracle Database’** in the drop-down list **DBMS**;
 * Set the Oracle database to be used by configuring the Server Instance field;
 * Fill in **Admin user** in the Admin section using the database login previously created for the Admin role in the Log database
 * Fill in **Tablespace** and **Index Tablespace** fields in the Admin section with the System Tablespace and the Index Tablespace previously created
 * Fill in **Runtime user** in the Runtime section using the database login previously created for the Runtime role in the Log database
 * Fill in **Tablespace field** in the Runtime section with the Runtime Tablespace previously created
 * Test all users to confirm correct connectivity. For this, click Test Connection for each of the users configured.
 * Create the Log Database schema by clicking the Create/Upgrade Database button. 
 **Do not close the Configuration Tool at this point** - further tasks are to be performed.
 
 ***
 
**5. Configure the Platform Session Database**
In the Session tab of the Configuration Tool proceed as follows:
 * Set the hostname of the database server;
 * Set the Session User username and password for the imported user;
 * Set the Tablespace to use;
 * Press the ‘Configure Session Database’ button. **If you’re using an existing session database, all sessions in that database will be lost.**
Finally, press the ‘Apply and Exit’ button of the Configuration Tool to apply all changes and exit.
 
***

6. Install the Service Center
In the dialog that shows up for installing Service Center, choose ‘Yes’ to make sure you will be running a fully compatible version of Service Center.
If a dialog asking to start the OutSystems Scheduler service and OutSystems SMS Connector service shows up, answer ‘No’ and proceed.

***

**7. Upload your new environment license**
In the Administration section of Service Center, open the Licensing page, and request a new license for this environment, which should have a different serial number. Upon receiving the license, upload it in the Licensing page.
 
***

**8. In Service Center, set the server to the desired purpose (Development, Non-Production or Production)**
Launch Service Center, log in as 'admin' user using the password of the restored environment, go to the Administration tab, open the ‘Environment Configuration’ page, and select ‘Development’, ‘Non-Production’ or ‘Production’ purpose. You may have to set the Default DNS Name of the environment, if not already set.
**It is strongly recommended to set the same name for the Default DNS Name and the Environment Name, to rapidly identify the environment in Service Center.**
 
***

**9. Install Service Studio**
Run the ‘ServiceStudio-M.m.b.r.exe’ installation file and follow the instructions on screen.
 
***

**10. Install Integration Studio**
Run the ‘IntegrationStudio-M.m.b.r.exe’ installation file and follow the instructions on screen.
 
***

**11. Application Configurations Changes**
In case of environment replication, check the effective value of each Web Reference (in the module details page) and all Site Properties containing URLs or values pointing to other environments. If pointing to invalid or other environments, then update them accordingly.
Cover also any other application level configurations stored on the database.

***

**12. Multiple Database Schemas**
In case your applications are being deployed in multiple schemas, you need to change Service Center configurations to start using the cloned schemas.
In Service Center, go to ‘Administration’, and click ‘Database Schemas’. For each schema listed, change the configurations, to specify the new schema and tablespaces

***

**13. Republish the entire Factory**
Since the database brings its own factory, you should publish all spaces to properly deploy them to the application server. Create a whole content solution (with all of the factory’s components) and publish it. 

***
**14. Start the Remaining OutSystems Services (optional)**
After all changes to the applications configuration are done, ensuring that connections to wrong environments do not occur, you may start OutSystems Scheduler Service.
**Please note that to avoid timers to run in this environment, the OutSystems Scheduler Service should be stopped and disabled which is done in the Services console of the Administrative Tools, or this front-end must have the ‘Execute Timers’ option disabled in the Front-End Lists in Service Center.**

***


### Reconfigure an Installation to Use a Restored Database

This section focuses on scenarios in which you’ll have to reconfigure an existing OutSystems Platform installation to use the newly restored database on a single-node server (server with both the Deployment Controller and Front-End services). 

***

**1. Stop the OutSystems Services**
Open the Services console of the Administrative Tools and stop the following OutSystems Services:
 * OutSystems Scheduler;
 * OutSystems SMS Connector;
 * OutSystems Deployment;
 * OutSystems Deployment Controller;
 * OutSystems Log.

***

**2. Stop the IIS**
Open a command prompt window and stop the IIS using the following command:
```
1. iisreset /stop
```

***

**3. Configure the Platform Database**
Run the Configuration Tool and in the Platform tab configure the following properties according to the restored database:
 * The hostname of the database server ;
 * For each login account (Platform Admin and Runtime), specify the imported username and password;
 * For each login account, press the ‘Test Connection’ link. The connection to the database should be successful, otherwise review the credentials you have just entered above.
Finally, press the ‘Create/Update Database’ button.
**Don’t close the configuration tool yet.**

***

**4. Configure the Log Database**
In the Log tab of the Configuration Tool configure the following properties according to the restored database:
 * The hostname of the database server ;
 * For each login account (Log Admin Runtime), specify the imported username and password;
 * For each login account, press the ‘Test Connection’ link. The connection to the database should be successful, otherwise review the credentials you have just entered above.
Finally, press the ‘Create/Update Database’ button.
**Don’t close the configuration tool yet.**

***

**5. Configure the Platform Session Database**
In the Session tab of the Configuration Tool proceed as follows:
 * Set the hostname of the database server;
 * Set the Session User username and password for the imported user;
 * Set the Tablespace to use;
 * Press the ‘Configure Session Database’ button. **If you’re using an existing session database, all sessions in that database will be lost.**
**Don’t close the configuration tool yet.**

***

**6. Start IIS**
Open a command prompt window and start IIS using the following command:
```
1. iisreset /start
```

***

**7. Apply the changes and exit**
Press the ‘Apply and Exit’ button of the Configuration Tool to apply all changes and exit.

***

**8. Upload your new environment license**
In the Administration section of Service Center, open the Licensing page, and request a new license for this environment. Upon receiving the license, upload it in the Licensing page. 

***

**9. In Service Center, set the server to the desired purpose (Development, Non-Production or Production)**
Launch Service Center, log in as ‘admin’ user using the password of the restored environment, go to the Administration tab, open the ‘Environment Configuration’ page, and select the ‘Development’, ‘Non-Production’ or ‘Production’ purpose. You may have to set the Default DNS Name of the environment, if not already set.
**We strongly recommend you to set the same name for the Default DNS Name and the Environment Name, to rapidly identify the environment on Service Center.** 

***

**10. Application Configurations Changes**
In case of environment replication, check the effective value of each Web Reference (in the module details page) and all Site Properties containing URLs or values pointing to other environments. If pointing to invalid or other environments, then update them accordingly.

***

 **11. Multiple Database Schemas**
In case your applications are being deployed in multiple schemas, you need to change Service Center configurations to start using the cloned schemas.
In Service Center, go to ‘Administration’, and click ‘Database Schemas’. For each schema listed, change the configurations, to specify the new schema and tablespaces

***

**12. Republish the entire Factory**
Since the database brings its own factory, you should publish all spaces to properly deploy them to the application server. Create a solution with the whole content (with all of the factory’s components) and publish it.

***

**13. Start the Remaining OutSystems Services (optional)**
After all changes to the applications configuration are done, ensuring that connections to wrong environments do not occur, you may start OutSystems Scheduler Service.
Please note that to avoid the timer to run in this environment the OutSystems Scheduler Service should be stopped and disabled which is done in the Services console of the Administrative Tools, or this front-end must have the ‘Execute Timers’ option disabled in the Front-End Lists in Service Center.

***


