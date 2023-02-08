---
locale: en-us
guid: c51058a5-946f-4f12-8acc-8d4d3f695057
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

<div class="hidden"><h1>Integration Builder</h1></div>

<div class="hidden" id="integration-builder-1.43.0_start"></div>

<h2 id="integration_builder_1.43.0" >Integration Builder 1.43.0</h2>
<div class="info"><p>Released on Jan 24, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.43.0" >New in Integration Builder 1.43.0</h3>
<ul>
<li>It's now possible to rename entities and attributes when creating Salesforce integrations. (RCNT-5370)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.43.0" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that disabled the delete button for draft connections. (RCNT-5061)</li>
<li>Fixed an issue where the release notes for integrations could push the “Close” button out of the viewport if they were too long. (RCNT-5526)</li>
<li>Fixed an 'Index out of bounds' error when clicking the "Next" button without selecting a SharePoint site. (RCNT-5576)</li>
</ul>

<div class="hidden" id="integration-builder-1.43.0_end"></div><div class="hidden" id="integration-builder-1.42.1_start"></div>

<h2 id="integration_builder_1.42.1" >Integration Builder 1.42.1</h2>
<div class="info"><p>Released on Dec 22, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_integration_builder_1.42.1" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused basic filters using boolean values not to work, for SharePoint connectors created with the Integration Builder. (RPM-3383) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
<li>Fixed an issue that caused the Integration Builder to duplicate attributes in external database connectors. (RPM-3453) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
</ul>

<div class="hidden" id="integration-builder-1.42.1_end"></div><div class="hidden" id="integration-builder-1.42.0_start"></div>

<h2 id="integration_builder_1.42.0" >Integration Builder 1.42.0</h2>
<div class="info"><p>Released on Dec 12, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.42.0" >New in Integration Builder 1.42.0</h3>
<ul>
<li>It's now possible to rename entities and attributes when creating SharePoint integrations. (RCNT-5369)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.42.0" >Bug Fixing</h3>
<ul>
<li>Fixed a security vulnerability in Integration Manager. (RCNT-5512)</li>
</ul>

<div class="hidden" id="integration-builder-1.42.0_end"></div><div class="hidden" id="integration-builder-1.41.0_start"></div>

<h2 id="integration_builder_1.41.0" >Integration Builder 1.41.0</h2>
<div class="info"><p>Released on Nov 15, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.41.0" >New in Integration Builder 1.41.0</h3>
<ul>
<li>You can now specify the SAP Client parameter in SAP OData connections. (RCNT-3720)</li>
<li>Now, when the structure format is selected, MongoDB integrations only read the attributes that are part of the structure. This can result in performance improvements. (RCNT-5427)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.41.0" >Bug Fixing</h3>
<ul>
<li>Fixed an issue where arrays of primitive types were not correctly mapped in SAP OData integrations. (RCNT-5164)</li>
<li>Fixed a timeout error when deleting connectors in Integration Builder. (RCNT-5417)</li>
<li>Fixed an issue where deleting Salesforce objects that had been selected for integration would cause an internal server error when trying to publish. (RCNT-5418)</li>
<li>Fixed an issue where the Integration Builder would only update a table's definition when that table's attributes were viewed on the user interface. (RCNT-5450)</li>
<li>Fixed an issue where the links in Integration Manager's "Support" menu were clickable while the menu was collapsed. (RCNT-5474)</li>
<li>Fixed an error, affecting only relational database integrations, where entity attributes that hadn't been selected in Integration Builder were still included in the generated connector. (RPM-3248) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
<li>Fixed an issue where renamed columns, in Relational DB integrations, would revert back to their original names after editing an integration. (RPM-3261) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
</ul>

<div class="hidden" id="integration-builder-1.41.0_end"></div><div class="hidden" id="integration-builder-1.40.0_start"></div>

<h2 id="integration_builder_1.40.0" >Integration Builder 1.40.0</h2>
<div class="info"><p>Released on Oct 25, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.40.0" >New in Integration Builder 1.40.0</h3>
<ul>
<li>Added a link to the release notes to the Integration Builder's "Support" menu. (RCNT-5126)</li>
<li>Added a link to the support portal to the Integration Builder's "Support" menu. (RCNT-5207)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.40.0" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Integration Builder not to detect that attributes that had been selected when creating an integration had been deleted from the external system. (RCNT-5042)</li>
<li>Fixed an error deselecting a table when the filter by selected tables was active. (RCNT-5232)</li>
<li>Fixed an issue that caused the first table to be deselected when renaming a table. (RCNT-5298)</li>
<li>Fixed an issue where a "Next" button would be stuck spinning after using the browser's "back" function. (RCNT-5411)</li>
<li>Fixed an issue that caused the Integration Manager login not to work when LDAP is configured as an external identity provider in Lifetime. (RPM-3115) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
<li>Changed the way SharePoint sites are loaded so that the list doesn't timeout when the authorized Microsoft account has access to many sites. (RPM-3125) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
</ul>

<div class="hidden" id="integration-builder-1.40.0_end"></div><div class="hidden" id="integration-builder-1.39.1_start"></div>

<h2 id="integration_builder_1.39.1" >Integration Builder 1.39.1</h2>
<div class="info"><p>Released on Oct 14, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_integration_builder_1.39.1" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused errors when publishing a Sharepoint connector with more than 25 lists. (RCNT-5159)</li>
<li>Deleting a relational database integration from Integration Builder will not leave an extension behind anymore. (RCNT-5250)</li>
<li>Fixed an issue that caused dates after 2032 to be converted to wrong values, when calling SAP OData v2 services. (RCNT-5257)</li>
<li>Integration Builder will no longer allow selecting relational database tables that don't contain any supported attributes. (RCNT-5288)</li>
<li>MongoDB structures that only contain attributes that aren't supported by Integration Builder will no longer be selectable. (RCNT-5317)</li>
<li>Fixed an error when retrieving the platform version that prevented the use of Integration Builder (an error message saying "index 1 is out of range" was displayed). (RPM-3161) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
</ul>

<div class="hidden" id="integration-builder-1.39.1_end"></div><div class="hidden" id="integration-builder-1.39.0_start"></div>

<h2 id="integration_builder_1.39.0" >Integration Builder 1.39.0</h2>
<div class="info"><p>Released on Sep 21, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.39.0" >New in Integration Builder 1.39.0</h3>
<ul>
<li>It's now possible to rename entities and attributes when creating relational database connectors (SQL Server, Azure SQL, Oracle Database, MySQL, iDB2, PostgreSQL, Aurora PostgreSQL, Azure PostgreSQL). (RCNT-4002)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.39.0" >Bug Fixing</h3>
<ul>
<li>Fixed: Azure PostgreSQL integration connections status in Integration Manager was always "not assigned". (RCNT-5189)</li>
<li>Fixed an error generating MongoDB connectors when an _id attribute had the "String" type. (RCNT-5199)</li>
<li>Fixed an issue where only 200 SharePoint sites would be listed on the Integration Builder. (RPM-3065) <span class="cattag">Extended Product</span>  <span class="cattag">Integrations Builder</span> </li>
</ul>

<div class="hidden" id="integration-builder-1.39.0_end"></div><div class="hidden" id="integration-builder-1.38.0_start"></div>

<h2 id="integration_builder_1.38.0" >Integration Builder 1.38.0</h2>
<div class="info"><p>Released on Aug 23, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.38.0" >New in Integration Builder 1.38.0</h3>
<ul>
<li>Breaking change: Added support for expanded attributes in OData "create" and "update" actions. This update may require consumer applications to be adapted, as existing actions might have new inputs after being republished. (RCNT-4513)</li>
<li>Added support for integrations with Azure PostgreSQL, on versions 12 or 13. (RCNT-5063)</li>
<li>External IT Users Authentication with OpenID Connect: Integration Builder and Manager's login will now use the external identity provider configured in Lifetime. (RCNT-5182)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.38.0" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented signing into Integration Manager when an external authentication provider was configured in Lifetime. (RCNT-5129)</li>
<li>Fixed an issue that caused an error generating SharePoint connectors when multiple lists with similar long names were selected. (RCNT-5137)</li>
<li>Fixed an issue that forced users that opened Integration Builder from Service Studio to input their credentials. (RCNT-5150)</li>
<li>Fixed an issue where SAP connectors can be published despite having an invalid Base URL. (RCNT-5156)</li>
<li>Fixed an issue that caused a "This integration was changed by &lt;username&gt; since you started editing it." error when updating dependencies. (RCNT-5158)</li>
</ul>

<div class="hidden" id="integration-builder-1.38.0_end"></div><div class="hidden" id="integration-builder-1.37.0_start"></div>

<h2 id="integration_builder_1.37.0" >Integration Builder 1.37.0</h2>
<div class="info"><p>Released on Aug 09, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_integration_builder_1.37.0" >New in Integration Builder 1.37.0</h3>
<ul>
<li>Fixed a security issue in Integration Manager. (RCNT-4891)</li>
<li>Integration Builder now accepts synonyms of the "server" and "catalog" keywords in advanced SQL Server connections. (RCNT-4915)</li>
<li>Added information about which external system versions are supported to the "Create Integration" screen. (RCNT-4972)</li>
<li>Added an explanation of the "External certificate" option that's on the Dataverse and SharePoint connection creation screens. (RCNT-5070)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.37.0" >Bug Fixing</h3>
<ul>
<li>Improved the error message displayed when Integration Manager fails to acquire an authentication token for Dataverse or SharePoint. (RCNT-5068)</li>
<li>Fixed an issue where the Integration Builder wouldn't allow users to change the connection for a relational database integration if the new connection didn't have a database with the same name as the previous. (RCNT-5108)</li>
<li>Fixed an issue where the Integration Builder would not generate structures for MongoDB integrations. (RCNT-5115)</li>
</ul>

<div class="hidden" id="integration-builder-1.37.0_end"></div><div class="hidden" id="integration-builder-1.36.0_start"></div>

<h2 id="integration_builder_1.36.0" >Integration Builder 1.36.0</h2>
<div class="info"><p>Released on Jul 18, 2022</p></div>

<h3 id="new_in_integration_builder_1.36.0" >New in Integration Builder 1.36.0</h3>
<ul>
<li>Now, if Integration Manager is installed on an infrastructure that's not registered on Integration Builder, it will disable the features that require an integration Builder account. (RCNT-3604)</li>
<li>Added a short text explaining the purpose of the "Environments Setup" section of the "Settings" page. (RCNT-4770)</li>
<li>Integration Manager will now display an onboarding modal on a user's first login. (RCNT-4905)</li>
<li>Moving modules from an integration application generated by the Integration Builder to another application no longer will make the integration disappear from the Integration Manager. (RCNT-4923)</li>
<li>Added a tooltip to Oracle Connection forms, reminding users that in order to avoid errors when converting dates and numbers, the NLS_LANGUAGE field has to be configured according to the NLS_LANGUAGE parameter of the external database. (RCNT-4962)</li>
</ul>
<h3 id="bug_fixing_integration_builder_1.36.0" >Bug Fixing</h3>
<ul>
<li>Fixed an error where Salesforce authorization tokens would expire immediately if the OutSystems server was behind the UTC timezone. (RCNT-4984)</li>
<li>Fixed an issue that caused tooltips inside tables now to be displayed correctly. (RCNT-4995)</li>
<li>Blocked the selection of SharePoint's Managed Metadata type columns because the connector generated by Integration Builder can't handle them. (RCNT-5014)</li>
<li>Fixed an error generating MySQL connectors that included a column that has a foreign key to a column that's not an identifier. (RCNT-5032)</li>
</ul>

<div class="hidden" id="integration-builder-1.36.0_end"></div><div class="hidden" id="integration-builder-1.35.0_start"></div>

<h2 id="integration_builder_1.35.0" >Integration Builder 1.35.0</h2>
<div class="info"><p>Released on Jun 02, 2022</p></div>

<h3 id="bug_fixing_integration_builder_1.35.0" >Bug Fixing</h3>
<ul>
<li>Fixed an error selecting SQL Server connections that used integrated authentication. (RCNT-4911)</li>
<li>Fixed a security vulnerability in Integration Manager. (RCNT-4920)</li>
<li>Fixed a generation error when SharePoint objects' labels were composed exclusively of non-latin characters. (RPM-2307)</li>
</ul>

<div class="hidden" id="integration-builder-1.35.0_end"></div><div class="hidden" id="integration-builder-1.34.3_start"></div>

<h2 id="header-integration-builder-1.34.3" >Integration Builder 1.34.3</h2>
<div class="info"><p>Released on May 23, 2022</p></div>

<h3 id="new-in-integration-builder-1.34.3" >New in Integration Builder 1.34.3</h3>
<ul>
<li>Improved the time it takes to validate user's access permissions to relational database connections. (RCNT-4803)</li>
</ul>
<h3 id="bug-fixing-integration-builder-1.34.3" >Bug Fixing</h3>
<ul>
<li>Objects with long names no longer overflow the table layout on the "Select objects" wizard step. (RCNT-4663)</li>
<li>Fixed: On the "Select objects" step of the integration wizard, selecting a field would be slow when there were many objects listed. (RCNT-4851)</li>
<li>Fixed an issue where permissions assigned to a user for a given database connection were being ignored, if they resulted in a permission level below that which the user's default role granted. (RCNT-4862)</li>
</ul>

<div class="hidden" id="integration-builder-1.34.3_end"></div><div class="hidden" id="integration-builder-1.34.2_start"></div>

<h2 id="integration_builder_1.34.2">Integration Builder 1.34.2</h2>
<div class="info"><p>Released on May 13, 2022</p></div>
<h3 id="bug_fixing_1.34.2">Bug Fixing</h3>
<ul>
<li>The "www." part of a domain is no longer removed automatically from values typed into the Environment input on the Login screen. (RPM-2543)</li>
</ul>
<div class="hidden" id="integration-builder-1.34.2_end"></div><div class="hidden" id="integration-builder-1.34.0_start"></div>

<h2 id="integration_builder_1.34.0">Integration Builder 1.34.0</h2>
<div class="info"><p>Released on May 05, 2022</p></div>
<h3 id="new_in_integration_builder_1.34.0">New in Integration Builder 1.34.0</h3>
<ul>
<li>Added a hint to help fill port information on relational database connections. (RCNT-4701)</li>
<li>MongoDB integrations just got easier with the new version of the MongoDB connector. Now, collections can be represented in structure format, meaning Integration Builder inspects the collection schema and generates Structures. You can still choose to use the JSON output format. MongoDB integrations are available exclusively in the latest version of Integration Builder and are fully supported by OutSystems. Find out more about MongoDB integrations in <a href="https://www.outsystems.com/goto/ib-mongodb-docs" target="_blank" rel="noopener noreferrer">our documentation</a>. (RCNT-4854)</li>
</ul>
<h3 id="bug_fixing_1.34.0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused invalid connections to show in Integration Manager after deleting and then reinstalling an Integration Manager plugin. Now, when you delete a plugin, the connections that use that plugin are deleted. (RCNT-4731)</li>
<li>Fixed an issue that caused MongoDB integrations to show a "Pending changes" warning even after the integrations are published. (RCNT-4794)</li>
<li>Fixed an issue that allowed users to attempt republishing integrations while the dependency update process was running, causing concurrency errors. (RCNT-4809)</li>
</ul>
<div class="hidden" id="integration-builder-1.34.0_end"></div><div class="hidden" id="integration-builder-1.33.1_start"></div>

<h2 id="integration_builder_1.33.1">Integration Builder 1.33.1</h2>
<div class="info"><p>Released on Apr 11, 2022</p></div>
<h3 id="bug_fixing_1.33.1">Bug Fixing</h3>
<ul>
<li>Fixed an error that would occur when trying to quickly republish several connectors, using the contextual menu on the integrations list. (RCNT-4458)</li>
<li>Fixed: when installing the MongoDB Integration Manager Plugin, the text incorrectly stated an "integration" was being published. (RCNT-4725)</li>
<li>Fixed: For MongoDB connectors, an error message saying the connector had been changed was being displayed incorrectly when a publish operation had to wait for a dependency update process to finish. (RCNT-4729)</li>
<li>Fixed: For relational database connectors, an error message saying the connector had been changed was being displayed incorrectly when a publish operation had to wait for a dependency update process to finish. (RCNT-4771)</li>
<li>Fixed Integration Manager not being updated from version 1 to version 2 when there were no published integrations. This would prevent the installation of the MongoDB Integration Manager Plugin. (RPM-2329)</li>
<li>Now, Integration Builder won't ignore the value of the "Allow editing in Service Studio" property when generating MongoDB connectors. (RPM-2382)</li>
<li>Fixed: A "Connection timeout" error was displayed when listing relational database connections, if there were many connections in Service Center. (RPM-2403)</li>
</ul>
<div class="hidden" id="integration-builder-1.33.1_end"></div><div class="hidden" id="integration-builder-1.33.0_start"></div>

<h2 id="integration_builder_1.33.0">Integration Builder 1.33.0</h2>
<div class="info"><p>Released on Apr 05, 2022</p></div>
<h3 id="new_in_integration_builder_1.33.0">New in Integration Builder 1.33.0</h3>
<ul>
<li>Moved the null value handling options to a new "Advanced settings" section of the "Review integration" screen, on the Relation Database integration wizard. (RCNT-4267)</li>
<li>Salesforce connectors created by the Integration Builder now use Salesforce API version 54. (RCNT-4373)</li>
<li>Improved the visibility of a hint about the "DNS SRV" checkbox, on the MongoDB connection creation screens. (RCNT-4671)</li>
<li>Integrations with external databases in Integration Builder are now generally available and fully supported by OutSystems. Integrate with SQL, Server, Azure SQL, Oracle, MySQL, iDB2, and PostgreSQL and do with Integration Builder what you used to do with Integration Studio, only with an improved experience. Find more about it in our <a href="https://www.outsystems.com/goto/ib-external-db" target="_blank" rel="noopener noreferrer">documentation</a>. (RCNT-4741)</li>
</ul>
<h3 id="bug_fixing_1.33.0">Bug Fixing</h3>
<ul>
<li>Now, in Integration Manager, when creating/editing an SAP connection, the 'Test connection' button is disabled when there isn't an integration selected. (RCNT-4695)</li>
<li>Changed the loading animation of cards on the "Create Integration" screen. (RCNT-4700)</li>
<li>Improved the message displayed when a MongoDB connector fails to publish because its connection is no longer available. (RCNT-4722)</li>
<li>Fixed an error that prevented the deletion of relational database connections that were being used. (RCNT-4734)</li>
<li>When starting a PostgreSQL integration from Service Studio, Integration Builder now lets you know if the environment doesn't have the required Platform Server  version. (RCNT-4737)</li>
</ul>
<div class="hidden" id="integration-builder-1.33.0_end"></div><div class="hidden" id="integration-builder-1.32.0_start"></div>

<h2 id="integration_builder_1.32.0">Integration Builder 1.32.0</h2>
<div class="info"><p>Released on Mar 22, 2022</p></div>
<h3 id="new_in_integration_builder_1.32.0">New in Integration Builder 1.32.0</h3>
<ul>
<li>Improved the layout of the "Review" screen for Microsoft Dataverse, Microsoft Dynamics 365, Salesforce, SAP OData, and Sharepoint Online integrations. (RCNT-4278)</li>
<li>Added a visual indicator that table rows can be clicked on the "Add tables" step of the integration creation wizard for relational databases. (RCNT-4576)</li>
<li>A MongoDB integration is now available, as a Technical Preview.
This new integration allows you to easily connect your apps with the most popular no-SQL database, MongoDB. 
The MongoDB integrations are available exclusively in the latest version of Integration Builder and are fully supported by the OutSystems platform. Find out more about MongoDB integrations in our <a href="https://www.outsystems.com/goto/ib-mongodb-doc" target="_blank" rel="noopener noreferrer">documentation</a>.  (RCNT-4673)</li>
</ul>
<h3 id="bug_fixing_1.32.0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused an error that occurred in the generation step while publishing integrations. The issue occurred when object names included special characters leading to the duplication of object names. (RCNT-4602)</li>
<li>Improved the experience on the  "Add tables" step of the integration creation wizard for relational databases. Now, long table names don't cause a horizontal scroll. (RCNT-4662)</li>
<li>Fixed an issue that caused an  OS-INBL-GEN -50009 error while publishing integrations with Salesforce.  The issue prevented the generation of integrations that included object names that didn't contain any roman alphabet characters. (RPM-2266)</li>
</ul>
<div class="hidden" id="integration-builder-1.32.0_end"></div><div class="hidden" id="integration-builder-1.31.0_start"></div>

<h2 id="integration_builder_1.31.0">Integration Builder 1.31.0</h2>
<div class="info"><p>Released on Mar 08, 2022</p></div>
<h3 id="new_in_integration_builder_1.31.0">New in Integration Builder 1.31.0</h3>
<ul>
<li>Now integrations with Salesforce, SharePoint, Microsoft Dataverse, and Microsoft Dynamics 365 include a new "Get<object name="">BasicOrderById" Server Action. This action enables the sorting of data and is available in the library module of these integrations. (RCNT-4098)</object></li>
</ul>
<h3 id="bug_fixing_1.31.0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused an "IntegrationBuilderUser role required" error message. This error message appeared after clicking an action button after your session expired. (RCNT-4444)</li>
<li>Fixed an issue that caused a  "Missing value for mandatory input"  error message. This issue occurred when an Integration Builder dependency didn't have the version number in its description. (RCNT-4557)</li>
<li>Fixed an issue that caused errors when generating Microsoft Dataverse or Dynamics 365 integrations during the publishing process.
Breaking change: For Dataverse/Dynamics 365 integrations, the static entities that listed all entity attributes will now only list readable attributes. (RCNT-4580)</li>
<li>Fixed an issue that prevented Integration Builder from installing/updating dependencies in some complicated circumstances. Integration Builder would not install needed components automatically when other components needed to be updated. (RCNT-4581)</li>
</ul>
<div class="hidden" id="integration-builder-1.31.0_end"></div><div class="hidden" id="integration-builder-1.30.0_start"></div>

<h2 id="integration_builder_1.30">Integration Builder 1.30</h2>
<div class="info"><p>Released on Feb 21, 2022</p></div>
<h3 id="new_in_integration_builder_1.30">New in Integration Builder 1.30</h3>
<ul>
<li>Improvement on the Sharepoint Search Server Action. A new structure was added, as an input parameter, to filter by folder and also include/exclude sub-folders files. (RCNT-4219)</li>
<li>Added support for relational database integrations when each environment has a different catalog. In the "Select database" step of the wizard, there is a new option "Connection's default database". When this option is selected, the default database that was input when the external database connection was created will be used by the connector. This allows you to have different default databases per environment. (RCNT-4372)</li>
</ul>
<h3 id="bug_fixing_1.30">Bug Fixing</h3>
<ul>
<li>Integration Builder doesn't prompt users to update dependencies that don't affect integrations published to the customer's environment anymore. (RCNT-4490)</li>
<li>Fixed an issue that caused errors when generating an SAP OData connector and the request structure contains sub-structures. (RCNT-4506)</li>
<li>Fixed an issue that caused Integration Builder to update integrations that weren't selected on the Settings page. (RCNT-4526)</li>
</ul>
<div class="hidden" id="integration-builder-1.30.0_end"></div><div class="hidden" id="integration-builder-1.29.0_start"></div>

<h2 id="integration_builder_1.29.0">Integration Builder 1.29.0</h2>
<div class="info">
<p>Released on February 8, 2022</p>
</div>
<h3 id="new_in_integration_builder_1.29.0">New in Integration Builder 1.29.0</h3>
<ul>
<li>Integration Manager 2.0 is available. Integration Manager, is now split into several plugins for each system of records provider.<br/>
From now on, you only need to install the Integration Manager Plugins for the system of records you are integrating with.<br/>
Furthermore, Integration Builder warns you when you have unused plugins installed.</li>
</ul>
<h3 id="bug_fixing_1.29.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused errors when generating a SharePoint Online integration that includes objects with labels longer than 50 characters. In Service Studio, refresh the dependencies of apps that consume SharePoint Online integrations that include objects with labels longer than 50 characters.</li>
<li>Fixed an issue that caused errors when generating a Microsoft Dataverse or Dynamics 365 integrations that includes objects with labels longer than 50 characters. In Service Studio, refresh the dependencies of apps that consume Microsoft Dataverse or Dynamics 365 integrations that include objects with labels longer than 50 characters.</li>
<li>Fixed an issue that caused errors when creating a Salesforce connection using an administrator username containing a plus, "+".</li>
<li>Fixed an issue that caused the "Setup" widget to never stop spinning after logging in.</li>
<li>Fixed an issue that incorrectly showed the "Build your first integration" empty state in the "My integrations" screen, even if integrations exist. This occurred after using the search and getting no integration results.</li>
<li>Improved the "Settings" screen. When a dependency or integration update fails, you can now check the error message.</li>
<li>Improved the "Connections" screen in Integration Builder. Now, if Integration Manager isn't installed, you see a button to install Integration Manager. Previously, you could try to navigate Integration Manager and got an error saying that Integration Manager is not installed.</li>
<li>Improved Integration Builder contextual menu links, by making them easier to click with an increased clickable area.</li>
</ul>
<div class="hidden" id="integration-builder-1.29.0_end"></div><div class="hidden" id="integration-builder-1.28.0_start"></div>

<h2 id="integration_builder_1.28.0">Integration Builder 1.28.0</h2>
<div class="info">
<p>Released on January 24, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.28.0">New in Integration Builder 1.28.0</h3>
<ul>
<li>Now, when you delete an Integration in Integration Builder, the connector is also deleted from your environment.</li>
</ul>
<h3 id="bug_fixing_1.28.0">Bug fixing</h3>
<ul>
<li>Improved the error message displayed when Integration Builder needs users to re-authorize it to connect to Salesforce.</li>
<li>Microsoft Dataverse and Microsoft Dynamics 365 now have different entries in Integration Manager's "New connector" screen.</li>
<li>Improved the Salesforce "Add Objects" screen to ensure consistency on the entity's table across all providers.</li>
</ul>
<div class="hidden" id="integration-builder-1.28.0_end"></div><div class="hidden" id="integration-builder-1.27.0_start"></div>

<h2 id="integration_builder_1.27.0">Integration Builder 1.27.0</h2>
<div class="info">
<p>Released on January 17, 2021</p>
</div>
<h3 id="bug_fixing_1.27.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused errors when generating a Salesforce integration that includes objects with labels longer than 50 characters. In Service Studio, refresh the dependencies of apps that consume Salesforce integrations that include objects with labels longer than 50 characters.</li>
<li>Fixed an issue that caused runtime errors when there are spaces in an SAP OData service URL.</li>
<li>Fixed an issue that caused errors in connections to external databases after editing the connection name.</li>
<li>Fixed an issue that caused timeouts when generating a Salesforce integration and when there are too many selected pick-list fields.</li>
<li>Fixed an issue that caused the Setup popup to show again after you closed it.</li>
<li>Improvement in the publishing integrations experience. Now, developers can see how long the publishing of integration will take and also check the progress of the publishing.</li>
<li>Integrations that were changed after being published now have an icon marking them as having pending changes.</li>
<li>Improvement in the "Choose a provider" screen. In small resolution screens, it was not clear for the developer that there were more providers available when the developer scrolls down.</li>
<li>Changed the behavior of the Review button on the "Review" screen for the external database providers. The button now opens a modal to list selected entities, instead of navigating to the "Add entities" screen.</li>
<li>Improvement on the "Add entities" screen to keep consistency on the entities table across all providers.</li>
</ul>
<div class="hidden" id="integration-builder-1.27.0_end"></div><div class="hidden" id="integration-builder-1.26.0_start"></div>

<h2 id="integration_builder_1.26.0">Integration Builder 1.26.0</h2>
<div class="info">
<p>Released on December 20, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.26.0">New in Integration Builder 1.26.0</h3>
<ul>
<li>Now, you can set tables/entities/lists of integrations as read-only or read-write. This feature is available when integrating with the following systems of records: SAP OData, Salesforce, SharePoint Online, Microsoft Dataverse, and Microsoft Dynamics.</li>
<li>SAP OData "Get" actions now have an output specifying which attributes are null on SAP's side. "Search" actions will no longer return "Integration Builder null" values; If an attribute is null on SAP's side, a Search action will assign the OutSystems platform's default value to that attribute.</li>
<li>SAP OData Create and Update actions now have an input to specify which attributes will be sent in a request and an output specifying which attributes are null on SAP's side.</li>
</ul>
<h3 id="bug_fixing_1.26.0">Bug fixing</h3>
<ul>
<li>Now, newly created SAP OData integrations include the ExpandNavigationProperties input for the Get and Search actions.</li>
<li>Fixed an issue that prevented LifeTime from listing Integration Builder relational database integrations.</li>
<li>Fixed an issue in Integration Manager's connections list that caused the spinner to still show even after the list items loaded.</li>
<li>Fixed an issue that caused an error while accessing Integration Builder after being redirected from Service Studio. This issue affected users that never logged in to Integration Builder, or hadn't logged in for a while.</li>
<li>The "Review" button on Integration Builder's "Review" wizard step was removed. You can still navigate to previous wizard steps by clicking the "Previous" button, or by clicking the wizard navigation bar.</li>
<li>Fixed visual issues on the "Select provider" screen, when creating new connections in the Integration Manager. Now the providers are listed alphabetically.</li>
</ul>
<h3 id="breaking_change">Breaking change</h3>
<ul>
<li>We have changed the behavior of NULL values in SAP OData integrations.<br/>
Existing SAP OData integrations will continue to work until they are republished.<br/>
Integration Builder helps you with the republishing process, listing all integrations that should be republished.<br/>
Once you republish existing SAP OData integrations with Integration Builder, you must open the consumer apps in Service Studio, refresh their dependencies to the integration, and then republish these apps.</li>
</ul>
<div class="hidden" id="integration-builder-1.26.0_end"></div><div class="hidden" id="integration-builder-1.25.0_start"></div>

<h2 id="integration_builder_1.25.0">Integration Builder 1.25.0</h2>
<div class="info">
<p>Released on December 6, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.25.0">New in Integration Builder 1.25.0</h3>
<ul>
<li>You can now integrate with external databases using an Integration Builder Technical Preview. The external databases providers available are SQL Server/Azure SQL, Oracle, MySQL, and iDB2.</li>
</ul>
<div class="hidden" id="integration-builder-1.25.0_end"></div><div class="hidden" id="integration-builder-1.24.0_start"></div>

<h2 id="integration_builder_1.24.0">Integration Builder 1.24.0</h2>
<div class="info">
<p>Released on November 22, 2021</p>
</div>
<h3 id="bug_fixing_1.24.0">Bug fixing</h3>
<ul>
<li>Made some under-the-hood changes to navigation to and from SAP OData connections.</li>
<li>Fixed an error contacting internal APIs.</li>
</ul>
<div class="hidden" id="integration-builder-1.24.0_end"></div><div class="hidden" id="integration-builder-1.23.0_start"></div>

<h2 id="integration_builder_1.23.0">Integration Builder 1.23.0</h2>
<div class="info">
<p>Released on November 8, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.23.0">New in Integration Builder 1.23.0</h3>
<ul>
<li>Added more exception details on SAP OData service methods.</li>
</ul>
<h3 id="bug_fixing_1.23.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused errors on some requests to the SAP S4HANA server due to encoded single quotes and commas.</li>
<li>Fixed an issue that prevented SAP OData 4.0 specifications from being published.</li>
<li>Fixed an issue that caused an endless republish process when updating dependencies.</li>
<li>Fixed an issue that prevented Integration Builder from publishing a Dataverse/Dynamics integration when selected attributes have long names.</li>
<li>Fixed an issue that caused refresh issues on the UI of Setup bubble when a republish of integration with outdated dependencies finishes.</li>
<li>Fixed an issue that prevented users from closing the error message modal when the message is very long.</li>
<li>Fixed an issue that allowed users to edit unlocked integrations in Integration Builder.</li>
<li>Fixed an issue where changing the account of an existing Salesforce connector didn't change its Base URL.</li>
<li>Improved the default icons for all connectors.</li>
</ul>
<div class="hidden" id="integration-builder-1.23.0_end"></div><div class="hidden" id="integration-builder-1.22.1_start"></div>

<h2 id="integration_builder_1.22.1">Integration Builder 1.22.1</h2>
<div class="info">
<p>Released on Oct 7, 2021</p>
</div>
<h3 id="bug_fixing_1.22.1">Bug fixing</h3>
<ul>
<li>Fixed an error that prevented the creation of a SharePoint connection in Integration Manager.</li>
</ul>
<div class="hidden" id="integration-builder-1.22.1_end"></div><div class="hidden" id="integration-builder-1.22.0_start"></div>

<h2 id="integration_builder_1.22.0">Integration Builder 1.22.0</h2>
<div class="info">
<p>Released on Oct 4, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.22.0">New in Integration Builder 1.22.0</h3>
<ul>
<li>Now, Integration Manager lists external database connections.</li>
</ul>
<h3 id="bug_fixing_1.22.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused a wrong number of SAP entities and actions when publishing similar specifications with different formats, EDMX and JSON.</li>
<li>Fixed a misalignment on the details screen for SAP integrations.</li>
<li>Fixed an issue that caused a misalignment on SAP specification name when the specification's name is long.</li>
<li>Fixed misalignment in the wizard bar of Salesforce integration creation screens.</li>
</ul>
<div class="hidden" id="integration-builder-1.22.0_end"></div><div class="hidden" id="integration-builder-1.21.0_start"></div>

<h2 id="integration_builder_1.21.0">Integration Builder 1.21.0</h2>
<div class="info">
<p>Released on Sep 20, 2021</p>
</div>
<h3 id="bug_fixing_1.21.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that prevented Integration Builder to publish SAP integrations when specifications contained URL parameters in the <strong>CreateURLAsAttachment </strong>method.</li>
<li>Fixed wrong formatting for SAP attributes with decimal data type. This was happening for SAP OData v2 services.</li>
<li>On the Integration Manager application, made clearer the title of the Associate connection screen.</li>
</ul>
<div class="hidden" id="integration-builder-1.21.0_end"></div><div class="hidden" id="integration-builder-1.20.0_start"></div>

<h2 id="integration_builder_1.20.0">Integration Builder 1.20.0</h2>
<div class="info">
<p>Released on Sep 6, 2021</p>
</div>
<h3 id="bug_fixing_1.20.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused errors in Sharepoint integrations when SharePoint lists have special characters.</li>
<li>Fixed an issue that prevented Integration Builder from generating Dataverse/Dynamics integrations when a selected table didn’t have a plural label.</li>
<li>Fixed an issue that prevented Integration Builder from publishing updates on the integrations with outdated dependencies.</li>
<li>Fixed an issue that caused a wrong sort by Provider on Integrations and Connections list in Integration Manager.</li>
<li>Improvement on error message when navigating to an outdated Integration Manager.</li>
<li>Added favicon in a few screens that didn’t have them.</li>
<li>Improvements in one illustration on the Publish screen success state.</li>
</ul>
<div class="hidden" id="integration-builder-1.20.0_end"></div><div class="hidden" id="integration-builder-1.19.0_start"></div>

<h2 id="integration_builder_1.19.0">Integration Builder 1.19.0</h2>
<div class="info">
<p>Released on Aug 23, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.19.0">New in Integration Builder 1.19.0</h3>
<ul>
<li>Improved the layout of the screens where you create connections for Dataverse/Dynamics 365, Salesforce, and SharePoint.</li>
</ul>
<h3 id="bug_fixing_1.19.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused an incorrect redirect when denying Salesforce authorization in Integration Manager.</li>
<li>Fixed an issue that caused an incorrect redirect from the landing page when opening an integration that failed to publish.</li>
<li>Fixed an issue that prevented users from managing integrations in an invalid state that was caused by errors in the publishing process.</li>
<li>Fixed an issue that caused incorrect mandatory classifications on Microsoft Dataverse attributes.</li>
<li>Fixed an issue that prevented Integration Builder from listing all the entity attributes for some SAP specifications.</li>
<li>Fixed an issue generating Dataverse/Dynamic 365 integrations when an attribute is related to several tables.</li>
<li>Fixed an issue where users could create Salesforce connections with lower permissions than intended.</li>
</ul>
<div class="hidden" id="integration-builder-1.19.0_end"></div><div class="hidden" id="integration-builder-1.18.0_start"></div>

<h2 id="integration_builder_1.18.0">Integration Builder 1.18.0</h2>
<div class="info">
<p>Released on Aug 9, 2021</p>
</div>
<h3 id="bug_fixing_1.18.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that prevented Integration Builder from storing changes to SAP integrations after navigating to the Review screen and then back to the Checkout screen.</li>
<li>Fixed an issue that prevented Integration Builder from uploading a SAP specification with variables on the Server URL.</li>
<li>Fixed an issue that allowed users to select entities without attributes when creating a SAP integration. Now, you can't select those entities.</li>
<li>Improved the look and feel of the Setup popover. Now it is not attached to the Setup button.</li>
<li>Fixed an issue that caused an unhandled "Value cannot be null." exception while publishing Dataverse integrations in specific scenarios.</li>
<li>Improved the copy of the error message shown when the SAP specification is invalid.</li>
<li>Improved the look and feel of the Onboarding modal.</li>
<li>Changed the format of error messages. The new format now is: "&lt;error-message.&gt; (&lt;erro-code&gt;)".</li>
<li>Improved the copy of a tooltip related to "Allow editing in Service Studio".</li>
</ul>
<div class="hidden" id="integration-builder-1.18.0_end"></div><div class="hidden" id="integration-builder-1.17.0_start"></div>

<h2 id="integration_builder_1.17.0">Integration Builder 1.17.0</h2>
<div class="info">
<p>Released on July 28, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.17.0">New in Integration Builder 1.17.0</h3>
<ul>
<li>In Integration Manager, it's now possible to delete connections with the draft status.</li>
</ul>
<h3 id="bug_fixing_1.17.0">Bug fixing</h3>
<ul>
<li>Fixed an issue that caused a "Sequence contains no matching element" error while publishing a Dataverse integration that included all the columns of the Action Card table.</li>
<li>Fixed an issue that caused an "Upload failed" error while creating a SAP OData integration that occurred after trying to return to the "Upload specification" step from the "Add entities" step.</li>
<li>Fixed an issue that caused time out errors while trying to publish an integration.</li>
<li>Fixed an issue that caused already published connectors to not include the publishing status on the "Publish" screen.</li>
<li>Fixed an issue that occurred after an integration failed to publish and that prevented the solution file from being available for download.</li>
<li>Fixed an issue that prevented Integration Builder from showing an error message when the publishing of an integration failed while generating integration modules.</li>
<li>Fixed an issue related to name clash detection for modules. Now, detection is not case sensitive.</li>
<li>Fixed an issue that showed a wrong dependency being published when publishing an integration.</li>
<li>Fixed an issue that caused broken UI on the convert to Service Studio popup when the screen was resized to a smaller resolution.</li>
<li>Improved the position and alignment of Dependencies Popover on the landing page.</li>
<li>Improved the look and feel of the SAP OData version popup, and added a warning message to clarify the impact of selecting a wrong SAP OData version.</li>
<li>Improved the updating dependencies process by adding the username that triggers the update process, whenever a connector publication is blocked by the update dependencies process started by another user.</li>
<li>Improved the cursor pointer when hovering the wizard steps. Now, non-editable steps don’t show cursor pointer, on hover.</li>
<li>Changed the visual format of error and warning messages shown in the Connection Details screen.</li>
<li>Aligned provider icons in Integration Builder and Integration Manager applications, in order to be consistent.</li>
<li>Improved the copy in several parts of Integration Builder and Integration Manager.</li>
</ul>
<div class="hidden" id="integration-builder-1.17.0_end"></div><div class="hidden" id="integration-builder-1.16.0_start"></div>

<h2 id="integration_builder_1.16.0">Integration Builder 1.16.0</h2>
<div class="info">
<p>Released on July 19, 2021</p>
</div>
<h3 id="new_in_integration_builder_1.16.0">New in Integration Builder 1.16.0</h3>
<ul>
<li>Create integrations using a wizard-like interface that allow you to access data from the following enterprise Systems of Records:
<ul>
<li>Salesforce</li>
<li>SAP OData</li>
<li>Microsoft Dataverse</li>
<li>Microsoft Dynamics 365</li>
<li>SharePoint Online</li>
</ul>
</li>
<li>Edit previously created integrations to add support to additional entities and attributes of the external system.</li>
<li>The generated integrations are OutSystems apps that have the following features:
<ul>
<li>Follow the OutSystems development best practices.</li>
<li>You can choose to make it editable in Service Studio for further customization.</li>
<li>Support several authentication methods out-of-the-box (for now, only available for SAP OData).</li>
</ul>
</li>
</ul>
<div class="hidden" id="integration-builder-1.16.0_end"></div><div class="hidden"><h1>Integration Builder</h1></div>
