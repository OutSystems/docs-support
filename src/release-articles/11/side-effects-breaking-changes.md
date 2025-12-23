---
summary: The article details the side effects and breaking changes in OutSystems 11
tags: 
locale: en-us
guid: 2cfe6cf6-118b-41dc-b4f3-a36ed20a3841
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---
# OutSystems 11 side effects and breaking changes

This document lists the side effects and breaking changes introduced in the different versions of OutSystems 11.

OutSystems is committed to minimizing your effort when upgrading to a new release of OutSystems.

As such, before introducing a breaking change for a new release, OutSystems carefully analyzes its impact, namely, the expected number of occurrences in its customers' installations. A breaking change is introduced only if it affects a small number of customers.

## Breaking Changes

### Introduced in Platform Server 11.40.0

1\. <a id="bc-11400-1"></a>

**Issue**: Dropped support PostgreSQL versions 13.x and below as external databases.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: PostgreSQL no longer supports version 13. As such, we are aligning our supported external databases to that of the PostgreSQL Community.

In the future, OutSystems may, at its own discretion, drop support for other database engines and versions that are no longer supported by the database engine provider.

**Fix**: Update PostgreSQL version. Ensure that any applicable databases are set to a supported range as per OutSystems system requirements. OutSystems advises customers to choose a Long Term Release version that is both supported by PostgreSQL and OutSystems.

### Introduced in Platform Server 11.38.0

1\. <a id="bc-11380-1"></a>

**Issue**: Applications using either Regex_Search or Regex_Replace methods from Text extensions may have incorrect results if the regex expression used takes more than the defined default timeout.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: This is part of a mitigation strategy for RPM-5921, to prevent catastrophic backtracking during a regex match operation which in turn could lead to DoS.

**Fix**: Introduced a default regex timeout setting of 20s used in Regex_Search and Regex_Replace methods of Text extension. This setting is configurable via Factory Configuration. For specific use cases, where a different value might be needed, the new methods Regex_SearchWithTimeout and Regex_ReplaceWithTimeout should be used instead of changing the global default timeout value.

2\. <a id="bc-11380-2"></a>

**Issue**: Dropped support PostgreSQL versions 12.x and below as external databases.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: PostgreSQL no longer supports version 12. As such, we are aligning our supported external databases to that of the PostgreSQL Community.

In the future, OutSystems may, at its own discretion, drop support for other database engines and versions that are no longer supported by the database engine provider.

**Fix**: Update PostgreSQL version. Ensure that any applicable databases are set to a supported range as per OutSystems system requirements. OutSystems advises customers to choose a Long Term Release version that is both supported by PostgreSQL and OutSystems.

### Introduced in Platform Server 11.34.0

1\. <a id="bc-11340-1"></a>

**Issue**: Logical Database configuration of Extensions failed on first Solution Deployment attempt.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: During a solution publish, Logical Database configurations were fetched by ExtensionID at a deployment stage where that value could be `NULL`, causing configurations to not be set correctly.

**Fix**: Updated the `Async_Operation_LogicalDatabase` entity to include the SS_Key attribute, and updated the solution publish process to use it to fetch the Logical Database configuration. It is advised that customers who have referenced `Async_Operation_LogicalDatabase` in a module must refresh their module's dependency on the `(System)` reference.

### Introduced in Platform Server 11.33.0

1\. <a id="bc-11330-1"></a>

**Issue**: Dropped support for SQL Server 2014 (and corresponding compatibility level) as the Platform server's database management system.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Microsoft no longer supports SQL Server 2014. As such, we are aligning our supported databases to that of Microsoft.

Furthermore, support for compatibility levels equivalent or lower to that of SQL Server 2014 (120 and lower) will be dropped as these will no longer be tested.

In the future, OutSystems may, at its own discretion, drop support for other database engines and versions that are no longer supported by the database engine provider.

**Fix**: Update SQL Server engine version. Ensure that the compatibility level of any applicable databases is set to a supported range as per OutSystems system requirements. OutSystems advises customers to choose a Long Term Release version that is both supported by Microsoft and OutSystems.

2\. <a id="bc-11330-2"></a>

**Issue**: Dropped support SQL Server versions 2014 and below (as well as corresponding compatibility levels) as external databases.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Microsoft no longer supports SQL Server 2014. As such, we are aligning our supported external databases to that of Microsoft.

Furthermore, support for compatibility levels equivalent or lower to that of SQL Server 2014 (120 and lower) will be dropped as these will no longer be tested.

In the future, OutSystems may, at its own discretion, drop support for other database engines and versions that are no longer supported by the database engine provider.

**Fix**: Update SQL Server engine version. Ensure that the compatibility level of any applicable databases is set to a supported range as per OutSystems system requirements. OutSystems advises customers to choose a Long Term Release version that is both supported by Microsoft and OutSystems.

### Introduced in Platform Server 11.32.0

1\. <a id="bc-11320-1"></a>

**Issue**: The serial number of OutSystems Platform Server installed in EC2 machines using EC2 Launch v2 was incorrectly calculated.

**Fix**: The minimum supported version for OutSystems Platform Server installations in EC2 machines using EC2 Launch v2 was bumped from version 11.29.0 to 11.32.0.

The fix to the serial number calculation done will result in a new serial number for that Platform installation which will require a new license.

2\. <a id="bc-11320-1"></a>

**Issue**: Dropped support for MySQL 5.x as an external database version.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Due to the update of the MySQL driver to a supported version(9.0.0), we are forced to drop support for MySQL databases which the driver no longer supports connecting.

As such, MySQL 5.7 or lower is no longer supported as external databases.

In the future, OutSystems may, at its own discretion, drop support for other database engines and versions that are no longer suported by the database engine provider.

**Fix**: Update MySQL engine version. OutSystems advises customers to choose a Long Term Release version that is both supported by MySQL and OutSystems.

### Introduced in Platform Server 11.28.0

1\. <a id="bc-11280-1"></a>

**Issue**: The **forbidden.aspx** and **app_offline.aspx** custom handlers are replaced by new versions. Any previous configurations are overwritten.

**Runtime**:  Traditional web, Reactive web, Mobile

**Rationale**: Based on template files that are distributed with the platform, custom handlers are deployed to all apps. So that the forbidden.aspx and app_offline.aspx custom handlers don’t contain inline scripts or styles prior versions of the files are overwritten with compliant versions. All customized versions of these files are overwritten during the upgrade process.

**Workaround**: If you have a customized version of these custom handlers, you should back them up before the upgrade and customize the new versions after the upgrade.

### Introduced in LifeTime 11.22.0

1\. <a id="bc-11220-1"></a>

**Issue**: Using the ``PUT /deployments/{DeploymentKey}/`` method from the LifeTime API to remove apps from a deployment plan sets their status as **Do Nothing**, but they still appear in the deployment details. Now, the apps are removed from the deployment plan

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The ``PUT /deployments/{DeploymentKey}/`` method was changed to be consistent with the logic that runs when using the UI to remove apps from a deployment plan.

**Fix**: Implemented scenarios that take the output of the ``PUT /deployments/{DeploymentKey}/`` method as their source of data must be validated.

### Introduced in Platform Server 11.27.0

1\. <a id="bc-11270-1"></a>

**Issue**: Publishing the Current Running Version of a solution in Development environments now, by default, refreshes only broken dependencies with either runtime issues or broken reference warnings.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The _Refresh only broken dependencies_ in Solution Publish Factory Configuration parameter determines the conditions on which the Platform decides to refresh all references for each module, during the update components step of a solution publication.

When disabled it checks if there are any **different** signatures in the referenced elements of a consumer module and refreshes all of them (within that module) in case it finds one, which can unnecessarily increase publishing times.

However, when the parameter is enabled it checks if there are any **incompatible** signatures in the referenced elements of a consumer module and only refreshes all of them (within that module) in case it finds one. Making this the new default behaviour shouldn’t cause any disruption in the solution publication experience, and will overall result in better publishing times.

**Fix**: This behaviour can be changed back by installing version 11.2.0 of the Factory Configuration application or higher and unchecking the option “Refresh only broken dependencies in solution publish” under the Platform Configurations screen.

### Introduced in Platform Server 11.25.0

1\. <a id="bc-11250-1"></a>

**Issue**: Dropped support for Oracle 11g as an external database version.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Due to a security vulnerability in the Oracle Data Provider for .NET Managed driver, OutSystems 11 is now using Oracle Data Provider for .NET Managed driver in version 19.21.0. Starting with version 19.19 of that driver, Oracle calculates timezones based on regions (Europe, America, etc). This change in behaviour of the driver may cause "failure to connect" issues when the driver identifies regions (for example: UTC for Oracle 11g R2) that don't match any region on the Oracle server's timezone files.

OutSystems Platform 11 no longer supported Oracle 11g as the platform database. Starting with Platform Server version 11.25, OutSystems drops the support for Oracle 11g as an external database. Since Oracle 11g reached the end of Extended Support in 2020 ([official Oracle documentation](https://support.oracle.com/knowledge/Oracle%20Cloud/2068368_1.html)), customers who are using Oracle 11g are strongly advised to upgrade their database engine.

In the future, OutSystems may, at its own discretion, drop support for other database engines and versions that are no longer supported by the database engine provider.

**Fix**: Update Oracle engine version. OutSystems advises customers to choose a Long Term Release version that is both supported by Oracle and OutSystems, which at this moment is Oracle 19c.

### Introduced in Platform Server 11.24.0

1\. <a id="bc-11240-1"></a>

**Issue**: Some patterns in Excel files now have different behaviors.

* When a **DateTime** cell only contains the time (for example, 14:30), it will be converted to 1900-01-01 14:30 instead of 1900-01-02 14:30
* Cells that have more than 32767 chars will be trimmed on both formats (xls and xlsx)
* The date 29/Feb/1900 will appear as 1/Mar/1900 instead of 28/Feb/1900
* The default font of the document changed from Arial to Calibri

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: An upgrade was made in the Excel file processing library used in OutSystems 11. This upgrade comes with some breaking changes when compared to the version previously used.

**Fix**: Change the Excel files content so that it is compliant with the breaking changes related to value differences.

2\. <a id="bc-11240-2"></a>

**Issue**: Compilation errors occur in modules integrating with SAP services when the machine installed the SAP Connector for Microsoft.NET 3.0.x for Windows 64bit. This breaking change applies only to self-managed infrastructures. In the OutSystems Cloud the installation of all the necessary components is ensured.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The SAP Connector for Microsoft.NET 3.0.x for Windows 64bit depended on Microsoft C++ Runtime DLLs version 10.x, which reached its EOS.

**Fix**: Install SAP Connector for Microsoft.NET 3.1.x for Windows 64bit, as explained in the Platform installation checklist. This new version depends on Microsoft C++ Runtime DLLs version 14.x, which Microsoft still supports.

3\. <a id="bc-11240-3"></a>

**Issue**: It is not possible to bootstrap data from an excel file saved with the Strict Open XML format.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: An upgrade was made in the Excel file processing that is used in OutSystems 11. Now, it is not possible to use the Strict Open XML format.

**Fix**: Save the file using the **Excel Workbook** option.

### Introduced in Platform Server 11.21.0 { #bc-11210-1 }

**Issue**: Default values of parameters in consumed REST, SOAP and SAP methods are no longer translated.

**Runtime**: Traditional web

**Rationale**: The code generated for the multilingual translation of these values resulted in compilation errors, causing the publication to fail. There was a pattern which did not cause errors though, and will require applying the fix outlined below: input parameters with the **Send Default Value** property set to "Yes", if their default value has translations defined through the Multilingual feature.

This change affects only Traditional Web apps. For Reactive Web and Mobile apps, Service Studio already did not allow defining translations for default values.

**Fix**: During the upgrade, if any module was affected by the breaking change, then a warning message saying "Cannot translate default values in consumed integrations", and including the location of the default value, will be shown in the [modules preparation step](https://success.outsystems.com/documentation/11/setup_and_maintain_your_outsystems_infrastructure/upgrade_outsystems_platform/modules_preparation_step_during_platform_server_upgrade/) or when publishing it as part of a solution with full compilations. In order to preserve the behavior, move the default value and its translations to a new intermediate action which in turn calls the consumed method.

Note that the Locale settings are not propagated through the REST/SOAP/SAP integrations, so there is no automated way of knowing if the values sent through the Request have been translated.

### Introduced in Platform Server 11.20.0 { #bc-11200-1 }

**Issue**: In SQL Server, when importing or using external entities targeting views with DB linked tables, the platform will now treat those views as local views instead of attempting to perform operations directly on the underlying tables.

This can lead to Update, Delete and GetForUpdate operations, which were previously possible on those views, to stop working.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: When importing external views in SQL Server, the platform had inconsistent behaviors if the view definition contained DB linked tables. In these situations, if the connection user had "VIEW DEFINITION" permissions over the view, Integration Studio would import the columns of the first table used in the view definition instead of the columns of the view. It would also perform Update, Delete and GetForUpdate operations directly to that table, bypassing the view completely.

In most cases, this situation would cause runtime errors in Aggregates or SQL nodes, since the requested columns did not match. However, it would allow some other operations to succeed if the view only had a single table and made no changes to the columns definition. Having this capability also required connectivity and extra introspection queries when compiling modules that referenced those entities, causing runtime errors and incorrectly generated query code if there was a temporary unavailability of the external databases.

The old behavior was added to the platform to make it easier to import and modify tables accessed via DB links when there were no capabilities to directly connect to the destination databases. Currently, with the Database Connection feature available, there are alternatives to perform these integrations directly without having to rely on remote views.

**Fix**: The situations that require attention are when using views with DB linked tables to perform Update, Delete and GetForUpdate operations. This requires knowing what external entities are being imported via extensions and if they are views using DB Links. These changes only apply to SQL Server databases, so other databases are not affected.

The possible fixes are the following:

* Import the tables directly in Integration Studio again, without using the view. To do this in Integration Studio, open the extension and change the "Table or View Default Name" on the correspondent entity to have the fully qualified name of the table, including the DB Link (Ex: dblink.catalog.schema). Then, perform a "Refresh" to get the new definition. Validate and manually fix the "Identifier" attribute and any types on foreign keys, since view introspection cannot determine either of those.

* Use the Database Connection feature to create a new connection directly to the target database. In this situation, you need to import the entities again in Integration Studio using the new Database Connection without using the views or DB links. This requires updating the modules that use those entities to have the new references.

* If the views are being used to join data with other local entities or if the view definitions are complex (note that in most situations, this would be currently causing runtime errors, so it's unlikely), and there is also a need to perform update operations, OutSystems recommends importing two separate entities. One entity would still use the views to be used in Aggregates and joining data with other entities. The other entity would be used only for the update operations, using either the first or the second fix.

It is possible to enable the configuration "Allow introspection of views using DB linked tables in SQL Server" via Factory Configuration. This configuration is provided as a backward compatibility option and can be applied before the version upgrade. OutSystems doesn't recommend using it as a permanent fix since its behavior is inconsistent and can lead to runtime errors.

### Introduced in Platform Server 11.19.0 { #bc-11190-1 }

#### Solution Publish

**Issue**: In a Solution Publish, if a module references (directly or indirectly) multiple extensions and those extensions contain different versions of the same DLL, the Publish process chooses one of those DLLs to deploy. There was never a guarantee that the final application would work if those DLLs or their dependencies were incompatible with each other. In version 11.19.0, the algorithm that chooses the DLLs to deploy changed. It's possible that applications that were previously working, because the algorithm picked one DLL, stop working because it now picks another.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The algorithm now gives precedence to the DLLs from the most recent extension published to account for some scenarios with loosely coupled dependencies, instead of the previous dependencies alphabetical order.

**Fix**: Ensure the environment's extensions don’t have different incompatible versions of the same DLL. You can use the following query to identify multiple extensions that contain the same DLL. If you can see your extensions on this list, we recommend you ensure they use a single version of the conflicting DLL or make sure they are compatible. The query lists some OutSystems extensions, which are compatible between them.

    SELECT REPDLLEXT.Filename DLL, ossys_Extension.Name EXTENSION FROM 
        (SELECT ossys_Extension_Dependency.Filename, ossys_Extension_Dependency.Extension_Id FROM  
            (SELECT Filename FROM
                (SELECT Filename, Extension_Id FROM
                ossys_Extension_Dependency
                JOIN ossys_Extension on ossys_Extension_Dependency.Extension_Id = ossys_Extension.Id
                WHERE Filename LIKE '%.dll'
                AND ossys_Extension.IS_ACTIVE = 1
                AND ossys_Extension.Name NOT IN 
                ('OMLProcessor', 'IntegrationStudio', 'DeviceDetectionWithWURFL',
                'SAPDevServiceExtension', 'RESTDevServiceExtension',
                'SOAPDevServiceExtension', 'SCBootstrap', 'UsersSecurity')
                GROUP BY Filename, Extension_Id) DLLEXT
            GROUP BY Filename
            HAVING count(*) > 1) REPDLL
        JOIN ossys_Extension_Dependency on ossys_Extension_Dependency.Filename = REPDLL.Filename
        GROUP BY ossys_Extension_Dependency.Filename, ossys_Extension_Dependency.Extension_Id) REPDLLEXT
    LEFT JOIN ossys_Extension on REPDLLEXT.Extension_Id = ossys_Extension.Id
    where ossys_Extension.IS_ACTIVE = 1
    order by DLL

### Introduced in Platform Server 11.18.0

1\. <a id="bc-11180-1"></a>

**Issue**: The installer was modified to delete specific third-party DLLs from the `\plugins\database` folder and recreate them in new subfolders. This can prevent extensions or custom database connectors that expect the below DLLs to exist in the Platform Server. An example of those extensions are custom database connectors. Apps that consume those extensions can start to have runtime errors such as `Could not load file or assembly 'Google.Protobuf, Version=3.12.3.0, Culture=neutral, PublicKeyToken=a7d26565bac4d604' or one of its dependencies. The system cannot find the file specified.`
External database connections and extensions built using [OutSystems out-of-the box mechanisms](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Integrate_with_an_External_Database) **are not** affected by this breaking change.

Follows the list of affected files:

* **iDB2**:
    * IBM.Data.DB2.iSeries.dll

* **Oracle**:
    * Oracle.ManagedDataAccess.dll

* **MySQL**:
    * BouncyCastle.Crypto.dll
    * Google.Protobuf.dll
    * K4os.Compression.LZ4.dll
    * K4os.Compression.LZ4.Streams.dll
    * K4os.Hash.xxHash.dll
    * MySql.Data.dll
    * Renci.SshNet.dll
    * System.Buffers.dll
    * System.Memory.dll
    * System.Numerics.Vectors.dll
    * System.Runtime.CompilerServices.Unsafe.dll
    * Ubiety.Dns.Core.dll
    * Zstandard.Net.dll

* **PostgreSQL**:
    * Microsoft.Bcl.AsyncInterfaces.dll
    * Npgsql.dll
    * System.Buffers.dll
    * System.Memory.dll
    * System.Numerics.Vectors.dll
    * System.Runtime.CompilerServices.Unsafe.dll
    * System.Text.Encodings.Web.dll
    * System.Text.Json.dll
    * System.Threading.Channels.dll
    * System.Threading.Tasks.Extensions.dll

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: This file/folder reorganization was necessary to allow finer control over which DLLs are referenced, as well as their versions. This file/folder reorganization improves compatibility between current and future Database Connectors.

**Fix**:

* If you're using the [Secret Manager Local Service](https://www.outsystems.com/forge/component-overview/13476/secret-manager-local-service) Forge asset, update it to the latest version. Then, refresh the dependencies on the consumers and republish them.

* If you have an extension that expect the above DLLs to exist in the Platform Server, modify the extension ensuring that the necessary DLLs are imported to the extension.

* If you're using a custom database connector built using the Database Connector SDK, you'll need to ensure that the DLLs of that connector are in a dedicated folder. For example, `Google.Protobuf.dll` is used in the `ExampleDB` connector , place this DLL in the `\plugins\database\ExampleDB` folder. This is a very rare scenario. To minimize downtime ensure that this is done after running the Platform Installer and before running the Configuration Tool.

**Workaround**:

In case you can't use any of the above fixes, do the following:

1. Identify the assembly that's failing to be loaded in the list above.
1. Create a new [External Database Connection](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Integrate_with_an_External_Database/Integrate_with_an_external_database_using_Integration_Studio) and chose the DBMS identified on the list.
1. Don't test it and then save it. This will be a dummy connection, used only to recreate the files. It doesn't need to be assigned to an extension.
1. Republish the app that was having the errors.

2\. <a id="bc-11180-2"></a>

**Issue**: The `ActiveDirectory_GetAccountDetails` server action from the **Authentication** extension (part of System Components) now returns a new boolean parameter called `UserExists` to inform that an end user doesn't exist in the Active Directory, instead of throwing an exception.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The previous behavior of this server action used an exception to handle an expected use case, not following programming best practices and causing log pollution.

**Fix**: Change your logic to check for the value of the `UserExists` parameter instead of expecting for an exception to be thrown as the evidence that a user doesn't exist in the Active Directory.

3\. <a id="bc-11180-3"></a>

**Issue**: When using Active Directory authentication, OutSystems only supports configuring a default domain that ensures all traversed paths between domains are bidirectional in terms of trust.  

The Active Directory APIs used by the Platform require all traversed paths between domains during the search process to be bidirectional in terms of trust between said domains. If this is not possible, all the synchronization and access to users' details from the external system are unavailable. Some of the issues of using  a default domain with restricted access are:

* Users deactivated in the external system will still be active on the Platform.

* Metadata changed in the external system will not be synced to the Platform.

From Platform Server 11.18.0, users get errors when using this unsupported setup.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Using Active Directory authentication with a default domain with restricted access has always been problematic. However, it would malfunction silently. From version 11.18.0, users will get errors when using this setup.

**Fix**: Configure the default domain in your Active Directory infrastructure with a domain that ensures all traversed paths between domains are bidirectional in terms of trust.  

If this is not possible, you have to upgrade to Platform Server 11.21.0  or above and enable the `BypassADUsersSynchronization` site property in the Users module. Enabling this site property will avoid getting errors, but won't fix the issues of using a default domain with restricted access.

### Introduced in Platform Server 11.17.0

1\. <a id="bc-11170-1"></a>

**Issue**: Platform Server now only supports one active end-user authentication mechanism when using SAML-based authentication. This means you can no longer configure a SAML provider (Microsoft Entra, Okta, SAML2.0) authentication and still use the built-in mechanism. An `Invalid username or password error` message is thrown when trying to authenticate using a built-in user while a SAML provider is configured.

**Runtime**: Traditional web, Reactive web, Mobile  

**Rationale**: This is a security fix to ensure that our customers do not have a backdoor in their business applications once they configure a Federated SSO mechanism in their environments. Disallowing local users is the intended behaviour of the SAML authentication feature (for example, OKTA, Microsoft Entra, and SAML 2.0) when configured as the authentication mechanism.  

**Workaround**: This security fix can be disabled in Factory Configuration to allow built-in authentication fallback when using SAML providers. The security fix will be enabled by default to ensure customers are aware of the implications and the decision to turn it off should be a well-thought decision. Any customer that decides to opt-out of this security fix is responsible to ensure that the backdoor they have in their business applications is protected with the right permissions in their environments.
The Factory Configuration setting is called **Disable built-in authentication fallback when using SAML** and can be found under **Platform Configurations**.

2\. <a id="bc-11170-2"></a>

**Issue**: The HTML code in the `MessageText` parameter of the Feedback_Message Server Action displays as plain text in the Feedback_Message widget of RichWidgets, instead of rendered HTML.

**Runtime**: Traditional web

**Rationale**: The Feedback_Message widget now encodes the message by default to prevent cross site scripting (XSS) attacks.

**Fix**: Don't add HTML code to the Feedback_Message's text.

**Workaround**: In Service Center, set the site property `FeedBackMessage_ForceHTMLEncode` to False in the site properties of the RichWidgets module. This isn't recommended, as it leaves the Feedback_Message widget vulnerable to XSS attacks.

### Introduced in Platform Server 11.14.0

**Issue**: The Title of a Popup_Editor, Popup_EditorForUpload or Popup_EditorVanilla widget appears garbled in the application when all the following conditions are true:

* The title is dynamically generated through an input parameter.
* The value of the input parameter contains special characters.
* The value of the input parameter is encoded.

**Runtime**: Traditional web

**Rationale**: These widgets now encode the Title by default to prevent cross site scripting (XSS) attacks.

**Fix**: Remove the encoding of the input parameter value before sending it to the Title of the Popup.

**Workaround**: In Service Center, set the site property 'PopupTitle_ForceHTMLEncode' to False in the site properties of the RichWidgets module. This isn't recommended, as it leaves the popup vulnerable to XSS attacks.

### Introduced in Platform Server 11.12.0

1\. <a id="bc-11120-1"></a>

**Issue**: Widgets ignore tampered events. Widgets ignore events that you create or change by JavaScript. For example, OnChange Event Handlers fail to execute if you change the event before reaching the widget. This typically impacts scenarios where an input is having its value filtered / formatted / masked with JavaScript extensibility.
This issue affects the following Forge components:

* [Input Masks Library](https://www.outsystems.com/forge/component-overview/2258/input-masks-library)
* [Input Masks Mobile](https://www.outsystems.com/forge/component-overview/5289/input-mask-mobile)

**Runtime**: Reactive web, Mobile

**Rationale**: Upgrading to React 16 allows to take advantage of performance and security improvements while keeping an updated framework.

**Fix**: For related React documentation see [Improving inputs](https://reactjs.org/blog/2017/06/13/react-v15.6.0.html#improving-inputs).

2\. <a id="bc-11120-2"></a>

**Issue**: All unknown HTML attributes now show in the resulting HTML. React previously removed all attributes except data- from the output. Due to this change, the runtime now applies the CSS rules that were ignored.

**Runtime**: Reactive web, Mobile

**Rationale**: Upgrading to React 16 allows to take advantage of performance and security improvements while keeping an updated framework.

**Fix**: For related React documentation see [DOM Attributes in React 16](https://reactjs.org/blog/2017/09/08/dom-attributes-in-react-16.html).

3\. <a id="bc-11120-3"></a>

**Issue**:  By definition, the option HTML element only allows text as children. This is now enforced by React 16 and all children of an option element are now stringified, which may result in rendering `[object Object]` when that children is another HTML element, like a `span`.

This affects custom implementations of a native dropdown making use of HTML Element widgets with an option tag. This pattern can instead be implemented using a Dropdown widget with the "Options Content" property set to `Text Only`.

**Runtime**: Reactive web, Mobile

**Rationale**: Upgrading to React 16 allows to take advantage of performance and security improvements while keeping an updated framework.

**Fix**: A temporary workaround is to remove the children of the option element and create a `label` attribute with the desired text.

### Introduced in Platform Server 11.11.1

**Issue**: HTTP responses from Consumed REST API integrations now are closed more aggressively.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: When doing a large number of Consumed REST API requests, the number of used ports can increase rapidly and lead to port exhaustion problems. The new behavior prevents this situation and generally helps avoid leaking resources. However, this new behavior can also cause runtime changes in some edge cases. A known situation takes place when consuming an Exposed REST API in OutSystems that returns HTTP status code 204 (No Content), but sends data in the body, thus sending a "Content-Length" header with a value greater than zero. Although this is [invalid according to RFC 7230](https://httpwg.org/specs/rfc7230.html#header.content-length), it previously didn't cause an error. Additionally, you should validate other scenarios that might be affected by this breaking change.

**Workaround**: For the example stated above, the workaround is to change the returned status code from 204 (No Content) to a different status code, if you wish to include data in the body. Alternatively, keep returning the 204 status code but don't include any content in the response body.

### Introduced in Platform Server 11.9.0

1\. <a id="bc119-1"></a>

**Issue**: The platform now gives preference to usage of specific versions of third-party assemblies that are included in extensions. As a consequence, extensions that incorrectly include .NET Framework assemblies can prevent applications from working correctly due to conflicts between the included assemblies and the assemblies of the .NET Framework installed in the machine.

In particular, including the extensions `System.Net.Http.dll` or `System.Runtime.InteropServices.RuntimeInformation.dll` causes issues in **logging**, **login** and **JSON serialization**.

**Runtime**:  Traditional web, Reactive web, Mobile

**Rationale**: With the increased usage and adoption of open source libraries and systems like NuGet, it's an impossible task to ensure that all third-party assemblies used in an application have exactly the same versions. This applies to both the OutSystems platform, to extensions, and to any other .NET applications.

To improve the compatibility between multiple third-party libraries and different extensions used together, OutSystems apps now force the load of the assembly versions placed in the application directory. If the assembly available in the application folder has a higher version than the required one, it will work instead of the exact version specified at compile time. This is a similar behavior to the one currently present in the new .NET Core apps.

**Fix**: Open and remove all problematic system assemblies from affected extensions.

Before doing the Platform Server upgrade, check and fix the affected extensions. To do that, run the following query against your platform database:

    select distinct ossys_extension.Name, ossys_Extension_Dependency.Filename, ossys_Extension_Dependency.Compile_Action
    from ossys_Extension_Dependency inner join ossys_extension on ossys_extension.id = ossys_Extension_Dependency.extension_id
    where (ossys_Extension_Dependency.Filename like 'System.Runtime.InteropServices.RuntimeInformation.dll'
        or ossys_Extension_Dependency.Filename like 'System.Net.Http.dll')
        and ossys_extension.Version_Id = ossys_Extension_Dependency.Extension_Version_Id

You can adapt this query to list all 'System.%' assembly dependencies, but many of those assemblies aren't distributed with the .NET Framework. Therefore, it's difficult to make an extensive assembly list, apart from the following two known problematic assemblies: `System.Runtime.InteropServices.RuntimeInformation.dll` and `System.Net.Http.dll`. OutSystems recommends that you keep as few `System.*` included dependencies as possible.

Some commonly used applications from the Forge, like "Time Zone" and "Ultimate PDF", are known to have the issues outlined above. Remember to check the Forge for updated versions of these applications.

This issue happens mostly in extensions with its target framework set to 4.6.1 and that are referencing .NET Standard dependencies.  
This was never a supported configuration. Check [How to Use .NET Standard libraries in OutSystems extensions](https://success.outsystems.com/Documentation/How-to_Guides/Integrations/How_to_Use_.NET_Standard_libraries_in_OutSystems_extensions) for more information on referencing .NET Standard dependencies correctly. You can also find instructions on how to clean up unnecessary dependencies.

**Workaround**: As a temporary workaround for Platform Server 11.9.0, OutSystems added a new setting to the [Factory Configuration](https://www.outsystems.com/forge/component-overview/25/factory-configuration) application: "Force apps to use existing versions of third party libraries". When this setting is disabled, the platform reverts to the previous behavior.  
You should only use this workaround if it's not viable to fix all the affected extensions in a timely fashion. This setting will be ignored in all platform versions above 11.9, so it's important that you fix the root causes of this issue.

2\. <a id="bc119-2"></a>

**Issue**: The KeyStore and SAML actions were moved from the **Authentication** extension, `Authentication.xif`, to the **SAMLAuthentication** extension, `SAMLAuthentication.xif`. This can cause some broken references when using methods from Authentication.xif that moved to the new module.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: This refactoring was necessary to support architectural changes to the SAML authentication.

**Fix**: Replace dependencies to KeyStore and SAML actions from **Authentication** to the corresponding actions from **SAMLAuthentication**.

### Introduced in Platform Server 11.7.0

**Issue**:  Upgraded SharpZipLib library to version 1.1.0. The new version of the library can cause compatibility problems with custom components used in extensions. For example, when using the [OfficeUtils](https://www.outsystems.com/forge/component-overview/687/officeutils) Forge component you must upgrade to a recent version of the component, since it previously used a library version (NPOI 2.2, an Excel reader library) that depended on the previous SharpZipLib library version.

**Runtime**:  Traditional web, Reactive web, Mobile

**Rationale**: The new version of the library contains several performance improvements and security fixes. It's also a necessary change to be able to use recent versions of third-party libraries, like recent versions of NPOI that have a dependency on this library.

**Workaround**: This change has an impact on extensions that are using SharpZipLib to read ZIP files, or in extensions using libraries that have SharpZipLib as a dependency (like NPOI). It's recommended that you test any Zip and Excel-related functionalities of your applications after upgrading. If you find any issues, you must change any OutSystems extensions using third-party libraries that depend on SharpZipLib version 0.86.0. In the extensions, update the version of these third-party libraries to a version that uses SharpZipLib version 1.1.0.

### Introduced in Platform Server Oct.2019

**Issue**:  Integrations with external databases that use Oracle Database 10g Release 2 will stop working.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: We upgraded Oracle Data Provider for .NET, Managed driver to version 19.3.1 (4.122.19.1:20190703) and, according to the [official documentation](https://docs.oracle.com/en/database/oracle/oracle-database/19/odpnt/InstallSystemRequirements.html#GUID-A6405CAD-C0E9-45E0-9C38-26B7ED214479), this driver allows applications to connect to Oracle Database 11g Release 2 or later. This driver supports native encryption, meaning that you can set up your database to require encryption and this means all connections will be encrypted between the server and the database (applicable to both platform and external databases).

**Workaround**: Upgrade your Oracle engine to version 11g Release 2 or later.

### Introduced in Platform Server Sep.2018

#### LifeTime and Service Center

1\. <a id="bc-1"></a>

**Issue**: LifeTime is now only supported when installed in a dedicated environment.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: LifeTime now has its own release cycle to allow for better and faster improvements in LifeTime. To achieve this, LifeTime must be run, installed and maintained in a separate environment from the development pipeline environments in customer infrastructures. Check [LifeTime release notes and breaking changes](https://success.outsystems.com/Support/Release_Notes/LifeTime_Management_Console).

**Workaround**: None.

---

2\. <a id="bc-2"></a>

**Issue**: The following actions are no longer available after uploading an Module in Service Center: "Publish in debug mode", "Publish step by step" and "Publish step by step in debug mode".

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: These features were removed since they were infrequently used.

**Workaround**: None.

#### SMS

3\. <a id="bc-3"></a>

**Issue**: Removed support for the SMS feature. Publishing modules with SMS Flows will fail.

**Runtime**: Traditional Web

**Rationale**: The built-in SMS feature was removed due to low adoption and since it is no longer aligned with the product vision.

**Workaround**: Remove any SMS flows from your modules and any related dependencies before publishing them.

#### Database

4\. <a id="bc-4"></a>

**Issue**: The Configuration Tool shows an error when it detects a previous configuration using MySQL.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: MySQL is not supported as the platform database in OutSystems 11 and Configuration Tool will issue an error when it detects a previous configuration using MySQL. MySQL is now only supported as an external database.

**Workaround**: None.

---

5\. <a id="bc-5"></a>

**Issue**: Publishing an Module with a text entity attribute whose length is longer than 2000 characters but for which the metamodel says its length is exactly 2000 characters causes an error in Oracle, stating that the column's underlying data type cannot be changed.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: There was issue when developers changed the size of a Text attribute from 2000 characters to a larger value. In this case, the platform changed the metamodel for the attribute but not the database column itself, which might have led to data corruption at runtime.

**Workaround**: Open the Module, find the column, change its size back to 2000 characters and publish the Module.

To check which Modules are affected, run the following query against your Oracle database:

    select distinct esp.name espace, ent.physical_table_name, ent.name entity, eattr.name attribute_name, length 
    from ossys_entity_attr eattr
        left join ossys_entity ent on(eattr.entity_id = ent.id)
        left join ossys_espace esp on(ent.espace_id = esp.id)
        left join dba_tab_cols cols on (upper(eattr.name) = cols.column_name and upper(ent.physical_table_name) = cols.table_name)
    where eattr.type = 'rtText' and eattr.is_active=1 and eattr.length > 2000 and ent.is_active=1 and ent.is_system=0 and ent.is_external=0 and esp.is_active=1 and esp.name not in ('ECT_Provider') and cols.data_type <> 'CLOB';

#### Logs

6\. <a id="bc-6"></a>

**Issue**: Joins between log tables and other tables are no longer allowed.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Log tables may now be on a different physical database and in such scenarios it is not possible to do a database join.

**Workaround**: Use the new additional columns available in each log table or create application logic to replace the previously existing database join. Log entities are now available through the PlatformLogs extension.

---

7\. <a id="bc-7"></a>

**Issue**: Log entities without "Show Tenant Identifier" will no longer be filtered automatically.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Since logs can now be stored on a separate physical database, it is not possible to define a table as Multi-Tenant, and the platform will not be able to create the filter automatically.

**Workaround**: Explicitly add a filter by the current tenant identifier using the "Tenant_Id" column.

---

8\. <a id="bc-8"></a>

**Issue**: Log entities are now only accessible as read-only.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The runtime logging database user has no additional permissions, to prevent log tampering.

**Workaround**: None.

---

9\. <a id="bc-9"></a>

**Issue**: The OutSystems Log Service is no longer installed in OutSystems 11 first installations. Any automation scripts relying on the existence of this service may issue errors.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The OutSystems Log Service is not used by OutSystems 11 applications, but any applications that were not upgraded to OutSystems 11 still need this service to log errors. The service is not removed when upgrading Platform Server to version 11, but it's no longer installed in first installations. Follow the instructions in [Log Service Cleanup](https://success.outsystems.com/Documentation/How-to_Guides/DevOps/Log_Service_Cleanup) to remove the service, if no longer needed.

**Workaround**: If you have any automation scripts that rely on the existence of the OutSystems Log Service, you must update those scripts to handle the fact that the service may not exist.

#### REST APIs

10\. <a id="bc-10"></a>

**Issue**: Name clashes are now detected in REST structures when attributes have the same "Name in JSON" property value. The TrueChange pane will now show an error in this situation.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Although it is possible that regular structures and structures created from Consumed REST APIs have attributes with the same "Name in JSON", using these structures in Consume REST, Expose REST, JSON Serialize or JSON Deserialize elements causes serialization errors.

**Workaround**: Change the 'Name in JSON' of the attributes causing the error so that there are no duplicate values.

#### SOAP Web Services

11\. <a id="bc-11"></a>

**Issue**: Methods in EnhancedWebReferences API to customize consumed SOAP Web Services (all GetWebReference\* and SetWebReference\* methods) are now deprecated for imported SOAP Web Services created in OutSystems 11 and calls to those methods will be ignored. They can still be used for existing web services, i.e. for SOAP Web Services created in a version older than OutSystems 11 and then upgraded to this version.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: In OutSystems 11 there's a new implementation for consumed SOAP Web Services that are created in OutSystems 11, supporting SOAP 1.2 and some additional features. One of the biggest improvements is in terms of extensibility, by providing a powerful API similar to the one available for REST integrations, able to solve more use cases and provide more customization possibilities. Due to this fact, the EnhancedWebReferences API is **not** compatible with this new implementation and is now deprecated for consumed SOAP Web Services. However, the EnhancedWebReferences API is still the official (non-deprecated) API for customizing exposed SOAP Web Services in OutSystems.

**Workaround**: Use the [SOAP Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/SOAP_Extensibility_API) to customize requests of consumed SOAP Web Services created in OutSystems 11.

---

12\. <a id="bc-12"></a>

**Issue**: Certificates configured in Service Center (Administration > Certificates) can't be used with consumed SOAP Web Services that were created in OutSystems 11. They can still be used for existing web services, i.e. for SOAP Web Services created in a version older than OutSystems 11 and upgraded to this version.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: There's a new implementation for consumed SOAP Web Services in OutSystems 11 supporting SOAP 1.2 and some additional features. Along with this implementation, OutSystems provided a new [SOAP Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/SOAP_Extensibility_API) that can be used to use client-side certificates, among other use cases.

**Workaround**: Use the [SOAP Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/SOAP_Extensibility_API) to authenticate requests using client-side certificates in consumed SOAP web services that were created in OutSystems 11. Check the [client certificate authentication example](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Use_Advanced_Extensibility/Example%3A_Authenticate_using_a_client_certificate) provided in the API documentation.

#### Web Server Configuration (IIS)

13\. <a id="bc-13"></a>

**Issue**: IIS application pools that only have OutSystems applications will have their pipeline mode changed from Classic to Integrated.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Integrated pipeline mode is the recommended pipeline mode for IIS. It should enable OutSystems applications to serve more users concurrently. This helps to avoid the thread pool limits of Classic mode.

**Workaround**: None. You should check if all the applications in those application pools work in Integrated mode. Issues will only arise if you have included settings that are only applicable to Classic mode in `web.config` files.

#### Built-in Functions

14\. <a id="bc-14"></a>

**Issue**: Built-in time and data comparison functions `DiffHours`, `DiffMinutes`, and `DiffSeconds` now ignore the milliseconds.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: OutSystems enables you to manipulate time values on a second-level granularity. Some integrations introduce values at the millisecond-level granularity and these milliseconds could not be properly handled by the built-in functions, causing them to return an incorrect value in some cases. Ignoring the milliseconds part in the data values will prevent time manipulation functions from returning possibly incorrect values.

**Workaround**: None.  

#### JavaScript and HTML Rendering

15\. <a id="bc-15"></a>

**Issue**: Having a JavaScript flow element with asynchronous code in a Client Action that is marked as a function returns an error, and it is not possible to publish the module.

**Runtime**: Reactive web, Mobile

**Rationale**: The usage of asynchronous JavaScript code in Client Actions that are marked as functions can have an unpredictable behavior at runtime.

**Workaround**: Move the JavaScript flow element containing asynchronous JavaScript code to the "On Initialize" event of the screen and store the result you need in a variable of the same screen. In the Client Action, use that variable instead of the JavaScript element.  

---

16\. <a id="bc-16"></a>

**Issue**: Removed 'alt' attribute from the HTML rendering of links.

**Runtime**: Traditional web

**Rationale**: This attribute was used for compatibility in old browsers that are no longer supported. The 'alt' attribute only makes sense in image tags.

**Workaround**: If the 'alt' attribute in any element is still required, it can be inserted using Extended Properties.

---

17\. <a id="bc-17"></a>

**Issue**: Removed 'scheme' attribute from the rendering of meta elements.

**Runtime**: Traditional web

**Rationale**: According to W3C the 'scheme' attribute on the meta element is obsolete.

**Workaround**: If you are using the AddPostProcessingFilter action of the HTTPRequestHandler extension to add filters that somehow rely on the presence of the 'scheme' attribute of meta elements, you should adapt your source regular expression of the action to improve its handling of optional attributes of meta tags.

#### Custom Handlers

18\. <a id="bc-18"></a>

**Issue**: Custom Handlers is a folder where you can define custom pages for common runtime errors.  
From OutSystems 11 onwards, if a default language is not defined in the Custom Handler folder's `web.config` file, it will be automatically set to "VB" (Visual Basic).

**Runtime**: Traditional web

**Rationale**: The Custom Handlers folder is now deployed along with every application (to a sub-folder of the application folder), while previously the Custom Handlers folder was referenced by applications as needed from its location inside the Platform Server installation folder.  

OutSystems provides default Custom Handlers pages and some of those default pages include Visual Basic code, e.g. `internalerror.aspx`. Additionally, if no default language is defined in the `web.config` file in the Custom Handlers folder, the default language defined in the application's `web.config`, which is C#, will be used during the Custom Handlers pages' compilation and cause errors.

**Workaround**: Modify the Custom Handlers `web.config` file to explicitly state the language used in your Custom Handlers pages.

#### OutSystems APIs

19\. <a id="bc-19"></a>

**Issue**: Removed deprecated ApplicationManagementService and EnvironmentManagementService APIs from LifeTime Services.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: These Web Services were marked as deprecated in OutSystems 10 because the same version introduced new and more complete REST APIs.

**Workaround**: Change the integrations on your applications to consume the new LifeTime REST APIs.  

---

20\. <a id="bc-20"></a>

**Issue**: Removed the ElementVersionInfo structure from LifeTime SDK module.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: It was necessary to perform some changes in the current implementation of exposed APIs due to changes related with the new Reference Model. This included removing the ElementVersionInfo structure, which will not be available in the LifeTime metamodel anymore.

**Workaround**: None.

---

21\. <a id="bc-21"></a>

**Issue**: The `getFrontendKey()` method of the outsystems.api.requestInfo API might return a different key value in OutSystems 11.

**Runtime**: Traditional web

**Rationale**: The Frontend Name was made more consistent throughout monitoring and log sources. Since the Frontend Key value is based on the Frontend Name, the value returned by the `getFrontendKey()` method might also change.

**Workaround**: None.

#### Extensions

22\. <a id="bc-22"></a>

**Issue**: Removed obsolete database access APIs from the RuntimePlatform .NET library.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: These APIs are deprecated since 9.0 and OutSystems provides alternative ways of achieving the same functionality.

**Workaround**: Use the new database access APIs available in the RuntimePublic.Db API.

---

23\. <a id="bc-23"></a>

**Issue**: The Settings class in the RuntimePlatform .NET library is now deprecated and all methods that allowed you to modify settings inside applications were removed.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Configurations affecting the runtime of applications are now an integral part of an application and can no longer be manipulated in runtime. Additionally, the previously existing classes were internal and not meant for public usage.

**Workaround**: Any existing extensions taking advantage of this internal class must be modified to stop using it.

#### Security

24\. <a id="bc-24"></a>

**Issue**: Screen navigation done in HTTPS will not downgrade the protocol to HTTP even when the destination screen is not explicitly marked as requiring HTTPS.

**Runtime**: Traditional web

**Rationale**: In previous versions it was difficult to ensure that an application always used HTTPS when some of its screens did not require HTTPS.

**Workaround**: For those rare situations where you need to redirect the user to an HTTP address, change the application to use an External Site element with an explicit HTTP URL.

---

25\. <a id="bc-25"></a>

**Issue**: HTTPS is now enforced for all screens and integrations (REST and SOAP) in mobile modules. There is no opt-out from this behavior.

**Runtime**: Reactive web, Mobile

**Rationale**: The previous behavior did not make applications secure by default. Exposed SOAP web services were unable to enforce HTTPS.

**Workaround**: None.

---

26\. <a id="bc-26"></a>

**Issue**: Image URLs generated in the previous platform versions will no longer be valid.

**Runtime**: Traditional web

**Rationale**: The previously existing image endpoint used a shared key across all clients to encrypt the image details. The new endpoint uses the unique private key of each client to encrypt the image details, thus preventing other clients from tampering with the URL content.

**Workaround**: To keep the old behavior, set the `OutSystems.Images.UsePrivateKeyEncryptionForURL` parameter to `false` in the OSSYS_PARAMETER database table.  
Note: The support for this setting will be dropped on the next major platform version and the new behavior will be used by default.

---

27\. <a id="bc-27"></a>

**Issue**: Full SQL commands are no longer displayed to the end-user when an error occurs in a SQL element.  
This behavior only occurred in versions earlier than 10.0.723.0; upgrades from a later OutSystems 10 version to OutSystems 11 are not affected by this change of behavior.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Previously, when an error occurred in a SQL element, the error message could be shown to the end-user if the exception was not properly handled. This message would include the query where the error occurred and it would expose some details about the application entities. Now, the error and the query are still logged and displayed in the environment management console, but the end-user will only see a generic error message.

**Workaround**: None.

#### System Entities

28\. <a id="bc-28"></a>

**Issue**: Removed the Zone and Zone_Server system entities, as well as the "Zone_Id" attribute from the Espace system entity.  
Upgrading a module in Service Studio will remove any dependencies on these entities and attribute. You will get validation errors if these deleted objects were being used.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: In OutSystems 11 the concept of Zones has been replaced by Deployment Zones and these system entities and attribute are no longer used.

**Workaround**: None.

---

29\. <a id="bc-29"></a>

**Issue**: Removed entities Entity_Usage and Entity_Usage_Sample from the "(System)" reference.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: These were internal entities that were not being used.

**Workaround**: None.

#### Emails

30\. <a id="bc-30"></a>

**Issue**: Queued emails from disabled applications are no longer processed by the Scheduler Service.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: Make the behavior of pending emails consistent with the behavior of newly created emails.

**Workaround**: None.

---

31\. <a id="bc-31"></a>

**Issue**: Emails now require that there is at least one server in the Deployment Zone of the module configured to "Send Emails".

**Runtime**: Traditional web

**Rationale**: Previously, emails could be sent by any server in the environment, regardless of the module that created them. This broke the isolation between servers, causing misbehaved modules to have impact in the email processing of modules in other servers. The new behavior is now consistent with the execution of Processes and Timers.

**Workaround**: Ensure that there is at least one server in each Deployment Zone that is able to "Send Emails", if it contains modules with Email screens. You can set this configuration in Service Center (Administration > Servers).

#### Resources

32\. <a id="bc-32"></a>

**Issue**: Changing binary resources now triggers a references update and a recompilation of consumers.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: It was possible to change a binary resource in a producer without consumers recompiling the resource after the change. In some cases, this made the resource to be apparently working in the consumer without any issues. However, if developers changed the resource name or its target directory this would cause consumers to break.

**Workaround**: None. We changed the reference semantics in binary resources: they are now copied to the consumers and will trigger a recompilation when a binary resource is changed.

#### OSP Tool

33\. <a id="bc-33"></a>

**Issue**: The "Upload" button in OSP Tool no longer publishes the solution.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: The "Upload" button was also publishing the solution and not just uploading it, as it should. This behavior was fixed.

**Workaround**: Click the "1-Click Publish" button to publish the solution.

#### Mobile Apps

34\. <a id="bc-34"></a>

**Issue**: If you upgrade to OutSystems 11 and you have old mobile apps published before September 2018 your applications will break with an error screen after the upgrade of Platform. Only apps that use App Feedback and that were built before September 2018 are affected by this breaking change.

**Runtime**: Mobile

**Rationale**: In OutSystems 11 we introduce new improvements to our App Feedback feature that are not compatible with the older versions of mobile apps.

**Workaround**: If you haven't generated and distributed mobile apps since September 2018, and the apps have App Feedback enabled, generate those mobile apps again and then distribute them to the users before upgrading.

35\. <a id="bc-35"></a>

**Issue**: If you upgrade to OutSystems 11, and you previously distributed mobile apps that were generated between July 31, 2019 and October 9, 2019, those apps will break with an error screen after the upgrade.

**Runtime**: Mobile

**Rationale**: In July 2019 we fixed a Query Parameters issue related to opening apps with deep links. However, this fix broke the upgrade process.

**Workaround**: If you generated and distributed mobile apps between July 31, 2019 and October 9, 2019, generate those mobile apps again and then distribute them to the users before upgrading.

#### Mobile Runtime

36\. <a id="bc-36"></a>

**Issue**: Iterating a list recursively throws a runtime error.

**Runtime**: Reactive web, Mobile

**Rationale**: Keep the client-side and server-side models consistent between each other, since the server-side code always had this limitation. We introduced this change in OutSystems 11 to prevent breaking changes during the OutSystems 10's release cycle.

**Workaround**: Change the application logic to ensure that there are no recursive iterations of a list.

#### Logic

37\. <a id="bc-37"></a>

**Issue**: JSONDeserialize widget no longer truncates Decimals that are parsed to Text.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: When using JSONDeserialized widget in Server Actions to deserialize a JSON string data to a record or list. If the deserialized data type contains a Text attribute but in the JSON string data that attribute value is sent as a Decimal, the trailing zeros are preserved when deserializing that Decimal attribute to Text.

For example, the sent decimal values `10.000` and `10.1000` are deserialized to `10.000` and `10.1000` and not to `10` and `10.1`.

**Workaround**: To truncate a value, change the deserialized attribute data type to Decimal instead of  Text.

## Side Effects

### Introduced in Platform Server 11.14.0

#### Identity Service

1\. <a id="se1114-1"></a>

**Issue**: The login for IT apps (apps that use Service Center as their user provider) no longer uses the traditional login screen from the app itself. Instead, it uses a centralized login screen. This only affects applications that use the **User_GetUnifiedLoginUrl** action to validate if there is an external login URL. The centralized login screen shows the app name that you can provide in the **ToolName** of the **User_GetUnifiedLoginUrl** optional parameter.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: This change provides a consistent login experience throughout the different applications that use Service Center as their user provider.

**Workaround**: None.

### Introduced in Platform Server Sep.2018

#### OutSystems APIs

1\. <a id="se-1"></a>

**Issue**: `BeginReadUncommittedTransaction` and `BeginTransaction` methods from RuntimePublic.Db API are now deprecated.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: These methods would crash because connections are already inside the context of a transaction.

**Workaround**: None.

#### User Provider

2\. <a id="se-2"></a>

**Issue**: A Performance Suggestion warning will be added to all modules that do not have 'Is User Provider' set and have the 'User Provider' as 'Current Module'.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: It's recommended that all modules specify a User Provider to reduce the amount of work necessary in application's first load times and to avoid communications between applications and the Deployment Controller Service.

**Workaround**: Determine what should be the User Provider of your factory (by default it should be 'Users') and set the 'User Provider' property accordingly. If a module is supposed to be a User Provider, change the 'Is User Provider' property value to 'Yes'.  
Note: It's not recommended to change the User Provider of modules with Processes or Multi-tenant Entities/Timers/Site Properties.

#### Custom Handlers

3\. <a id="se-3"></a>

**Issue**: The Custom Handlers directory is now deployed along with every application. Previously, the Custom Handlers directory existed in the Platform Server installation directory and every application referenced it when needed.

**Runtime**: Traditional web

**Rationale**:  This change makes applications more self-contained in order to enable deployment to containers.

**Workaround**: None.

#### Debug Mode

4\. <a id="se-4"></a>

**Issue**: After turning off the environment Debug Mode configuration, some modules will show a warning saying that they need to be republished, when in fact they do not.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: When disabling the Debug Mode for the environment, all modules will have a warning stating that they need to be republished. In fact, the modules that already had Debug Mode disabled do not need to be republished since their configuration matches the configuration of the environment.

**Workaround**: None.

#### Solution Publish

5\. <a id="se-5"></a>

**Issue**: The refresh of references when publishing a solution (when publishing the current running version of its components) in Service Center was reviewed. Publishing the current version of a solution will now only refresh module references when the publish operation is performed in an environment whose purpose is set to Development.

**Runtime**: Traditional web, Reactive web, Mobile

**Rationale**: In environments whose purpose is not Development it is important that the actual published versions are kept; refreshing references would create different "fake" versions.

**Workaround**: Refresh references manually.
