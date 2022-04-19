---
locale: en-us
guid: c51058a5-946f-4f12-8acc-8d4d3f695057
app_type: traditional web apps, mobile apps, reactive web apps
---

<h1>Integration Builder</h1>
<h2 id="Integration_Builder_1.33.1">Integration Builder 1.33.1</h2>
<div class="info"><p>Released on Apr 11, 2022</p></div>
<h3>Bug Fixing</h3>
<ul>
<li>Fixed an error that would occur when trying to quickly republish several connectors, using the contextual menu on the integrations list. (RCNT-4458)</li>
<li>Fixed: when installing the MongoDB Integration Manager Plugin, the text incorrectly stated an "integration" was being published. (RCNT-4725)</li>
<li>Fixed: For MongoDB connectors, an error message saying the connector had been changed was being displayed incorrectly when a publish operation had to wait for a dependency update process to finish. (RCNT-4729)</li>
<li>Fixed: For relational database connectors, an error message saying the connector had been changed was being displayed incorrectly when a publish operation had to wait for a dependency update process to finish. (RCNT-4771)</li>
<li>Fixed Integration Manager not being updated from version 1 to version 2 when there were no published integrations. This would prevent the installation of the MongoDB Integration Manager Plugin. (RPM-2329)</li>
<li>Now, Integration Builder won't ignore the value of the "Allow editing in Service Studio" property when generating MongoDB connectors. (RPM-2382)</li>
<li>Fixed: A "Connection timeout" error was displayed when listing relational database connections, if there were many connections in Service Center. (RPM-2403)</li>
</ul>

<h2 id="Integration_Builder_1.33.0">Integration Builder 1.33.0</h2>
<div class="info"><p>Released on Apr 05, 2022</p></div>
<h3>New in Integration Builder 1.33.0</h3>
<ul>
<li>Moved the null value handling options to a new "Advanced settings" section of the "Review integration" screen, on the Relation Database integration wizard. (RCNT-4267)</li>
<li>Salesforce connectors created by the Integration Builder now use Salesforce API version 54. (RCNT-4373)</li>
<li>Improved the visibility of a hint about the "DNS SRV" checkbox, on the MongoDB connection creation screens. (RCNT-4671)</li>
<li>Integrations with external databases in Integration Builder are now generally available and fully supported by OutSystems. Integrate with SQL, Server, Azure SQL, Oracle, MySQL, iDB2, and PostgreSQL and do with Integration Builder what you used to do with Integration Studio, only with an improved experience. Find more about it in our <a href="https://www.outsystems.com/goto/ib-external-db">documentation</a>. (RCNT-4741)</li>
</ul>
<h3>Bug Fixing</h3>
<ul>
<li>Now, in Integration Manager, when creating/editing an SAP connection, the 'Test connection' button is disabled when there isn't an integration selected. (RCNT-4695)</li>
<li>Changed the loading animation of cards on the "Create Integration" screen. (RCNT-4700)</li>
<li>Improved the message displayed when a MongoDB connector fails to publish because its connection is no longer available. (RCNT-4722)</li>
<li>Fixed an error that prevented the deletion of relational database connections that were being used. (RCNT-4734)</li>
<li>When starting a PostgreSQL integration from Service Studio, Integration Builder now lets you know if the environment doesn't have the required Platform Server  version. (RCNT-4737)</li>
</ul>

<h2 id="Integration_Builder_1.32.0">Integration Builder 1.32.0</h2>
<div class="info"><p>Released on Mar 22, 2022</p></div>
<h3>New in Integration Builder 1.32.0</h3>
<ul>
<li>Improved the layout of the "Review" screen for Microsoft Dataverse, Microsoft Dynamics 365, Salesforce, SAP OData, and Sharepoint Online integrations. (RCNT-4278)</li>
<li>Added a visual indicator that table rows can be clicked on the "Add tables" step of the integration creation wizard for relational databases. (RCNT-4576)</li>
<li>A MongoDB integration is now available, as a Technical Preview.
This new integration allows you to easily connect your apps with the most popular no-SQL database, MongoDB. 
The MongoDB integrations are available exclusively in the latest version of Integration Builder and are fully supported by the OutSystems platform. Find out more about MongoDB integrations in our <a href="https://www.outsystems.com/goto/ib-mongodb-doc">documentation</a>.  (RCNT-4673)</li>
</ul>
<h3>Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused an error that occurred in the generation step while publishing integrations. The issue occurred when object names included special characters leading to the duplication of object names. (RCNT-4602)</li>
<li>Improved the experience on the  "Add tables" step of the integration creation wizard for relational databases. Now, long table names don't cause a horizontal scroll. (RCNT-4662)</li>
<li>Fixed an issue that caused an  OS-INBL-GEN -50009 error while publishing integrations with Salesforce.  The issue prevented the generation of integrations that included object names that didn't contain any roman alphabet characters. (RPM-2266)</li>
</ul>

<h2 id="Integration_Builder_1.31.0">Integration Builder 1.31.0</h2>
<div class="info"><p>Released on Mar 08, 2022</p></div>
<h3>New in Integration Builder 1.31.0</h3>
<ul>
<li>Now integrations with Salesforce, SharePoint, Microsoft Dataverse, and Microsoft Dynamics 365 include a new "Get<object name="">BasicOrderById" Server Action. This action enables the sorting of data and is available in the library module of these integrations. (RCNT-4098)</object></li>
</ul>
<h3>Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused an "IntegrationBuilderUser role required" error message. This error message appeared after clicking an action button after your session expired. (RCNT-4444)</li>
<li>Fixed an issue that caused a  "Missing value for mandatory input"  error message. This issue occurred when an Integration Builder dependency didn't have the version number in its description. (RCNT-4557)</li>
<li>Fixed an issue that caused errors when generating Microsoft Dataverse or Dynamics 365 integrations during the publishing process.
Breaking change: For Dataverse/Dynamics 365 integrations, the static entities that listed all entity attributes will now only list readable attributes. (RCNT-4580)</li>
<li>Fixed an issue that prevented Integration Builder from installing/updating dependencies in some complicated circumstances. Integration Builder would not install needed components automatically when other components needed to be updated. (RCNT-4581)</li>
</ul>

<h2 id="Integration_Builder_1.30">Integration Builder 1.30</h2>
<div class="info"><p>Released on Feb 21, 2022</p></div>
<h3>New in Integration Builder 1.30</h3>
<ul>
<li>Improvement on the Sharepoint Search Server Action. A new structure was added, as an input parameter, to filter by folder and also include/exclude sub-folders files. (RCNT-4219)</li>
<li>Added support for relational database integrations when each environment has a different catalog. In the "Select database" step of the wizard, there is a new option "Connection's default database". When this option is selected, the default database that was input when the external database connection was created will be used by the connector. This allows you to have different default databases per environment. (RCNT-4372)</li>
</ul>
<h3>Bug Fixing</h3>
<ul>
<li>Integration Builder doesn't prompt users to update dependencies that don't affect integrations published to the customer's environment anymore. (RCNT-4490)</li>
<li>Fixed an issue that caused errors when generating an SAP OData connector and the request structure contains sub-structures. (RCNT-4506)</li>
<li>Fixed an issue that caused Integration Builder to update integrations that weren't selected on the Settings page. (RCNT-4526)</li>
</ul>

<h2 id="Integration_Builder_1.29.0">Integration Builder 1.29.0</h2>
<div class="info">
<p>Released on February 8, 2022</p>
</div>
<h3>New in Integration Builder 1.29.0</h3>
<ul>
<li>Integration Manager 2.0 is available. Integration Manager, is now split into several plugins for each system of records provider.<br/>
From now on, you only need to install the Integration Manager Plugins for the system of records you are integrating with.<br/>
Furthermore, Integration Builder warns you when you have unused plugins installed.</li>
</ul>
<h3>Bug fixing</h3>
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
<h2 id="Integration_Builder_1.28.0">Integration Builder 1.28.0</h2>
<div class="info">
<p>Released on January 24, 2021</p>
</div>
<h3>New in Integration Builder 1.28.0</h3>
<ul>
<li>Now, when you delete an Integration in Integration Builder, the connector is also deleted from your environment.</li>
</ul>
<h3>Bug fixing</h3>
<ul>
<li>Improved the error message displayed when Integration Builder needs users to re-authorize it to connect to Salesforce.</li>
<li>Microsoft Dataverse and Microsoft Dynamics 365 now have different entries in Integration Manager's "New connector" screen.</li>
<li>Improved the Salesforce "Add Objects" screen to ensure consistency on the entity's table across all providers.</li>
</ul>
<h2 id="Integration_Builder_1.27.0">Integration Builder 1.27.0</h2>
<div class="info">
<p>Released on January 17, 2021</p>
</div>
<h3>Bug fixing</h3>
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
<h2 id="Integration_Builder_1.26.0">Integration Builder 1.26.0</h2>
<div class="info">
<p>Released on December 20, 2021</p>
</div>
<h3>New in Integration Builder 1.26.0</h3>
<ul>
<li>Now, you can set tables/entities/lists of integrations as read-only or read-write. This feature is available when integrating with the following systems of records: SAP OData, Salesforce, SharePoint Online, Microsoft Dataverse, and Microsoft Dynamics.</li>
<li>SAP OData "Get" actions now have an output specifying which attributes are null on SAP's side. "Search" actions will no longer return "Integration Builder null" values; If an attribute is null on SAP's side, a Search action will assign the OutSystems platform's default value to that attribute.</li>
<li>SAP OData Create and Update actions now have an input to specify which attributes will be sent in a request and an output specifying which attributes are null on SAP's side.</li>
</ul>
<h3>Bug fixing</h3>
<ul>
<li>Now, newly created SAP OData integrations include the ExpandNavigationProperties input for the Get and Search actions.</li>
<li>Fixed an issue that prevented LifeTime from listing Integration Builder relational database integrations.</li>
<li>Fixed an issue in Integration Manager's connections list that caused the spinner to still show even after the list items loaded.</li>
<li>Fixed an issue that caused an error while accessing Integration Builder after being redirected from Service Studio. This issue affected users that never logged in to Integration Builder, or hadn't logged in for a while.</li>
<li>The "Review" button on Integration Builder's "Review" wizard step was removed. You can still navigate to previous wizard steps by clicking the "Previous" button, or by clicking the wizard navigation bar.</li>
<li>Fixed visual issues on the "Select provider" screen, when creating new connections in the Integration Manager. Now the providers are listed alphabetically.</li>
</ul>
<h3>Breaking change</h3>
<ul>
<li>We have changed the behavior of NULL values in SAP OData integrations.<br/>
Existing SAP OData integrations will continue to work until they are republished.<br/>
Integration Builder helps you with the republishing process, listing all integrations that should be republished.<br/>
Once you republish existing SAP OData integrations with Integration Builder, you must open the consumer apps in Service Studio, refresh their dependencies to the integration, and then republish these apps.</li>
</ul>
<h2 id="Integration_Builder_1.25.0">Integration Builder 1.25.0</h2>
<div class="info">
<p>Released on December 6, 2021</p>
</div>
<h3>New in Integration Builder 1.25.0</h3>
<ul>
<li>You can now integrate with external databases using an Integration Builder Technical Preview. The external databases providers available are SQL Server/Azure SQL, Oracle, MySQL, and iDB2.</li>
</ul>
<h2 id="Integration_Builder_1.24.0">Integration Builder 1.24.0</h2>
<div class="info">
<p>Released on November 22, 2021</p>
</div>
<h3>Bug fixing</h3>
<ul>
<li>Made some under-the-hood changes to navigation to and from SAP OData connections.</li>
<li>Fixed an error contacting internal APIs.</li>
</ul>
<h2 id="Integration_Builder_1.23.0">Integration Builder 1.23.0</h2>
<div class="info">
<p>Released on November 8, 2021</p>
</div>
<h3>New in Integration Builder 1.23.0</h3>
<ul>
<li>Added more exception details on SAP OData service methods.</li>
</ul>
<h3>Bug fixing</h3>
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
<h2 id="Integration_Builder_1.22.1">Integration Builder 1.22.1</h2>
<div class="info">
<p>Released on Oct 7, 2021</p>
</div>
<h3>Bug fixing</h3>
<ul>
<li>Fixed an error that prevented the creation of a SharePoint connection in Integration Manager.</li>
</ul>
<h2 id="Integration_Builder_1.22.0">Integration Builder 1.22.0</h2>
<div class="info">
<p>Released on Oct 4, 2021</p>
</div>
<h3>New in Integration Builder 1.22.0</h3>
<ul>
<li>Now, Integration Manager lists external database connections.</li>
</ul>
<h3>Bug fixing</h3>
<ul>
<li>Fixed an issue that caused a wrong number of SAP entities and actions when publishing similar specifications with different formats, EDMX and JSON.</li>
<li>Fixed a misalignment on the details screen for SAP integrations.</li>
<li>Fixed an issue that caused a misalignment on SAP specification name when the specification's name is long.</li>
<li>Fixed misalignment in the wizard bar of Salesforce integration creation screens.</li>
</ul>
<h2 id="Integration_Builder_1.21.0">Integration Builder 1.21.0</h2>
<div class="info">
<p>Released on Sep 20, 2021</p>
</div>
<h3>Bug fixing</h3>
<ul>
<li>Fixed an issue that prevented Integration Builder to publish SAP integrations when specifications contained URL parameters in the <strong>CreateURLAsAttachment </strong>method.</li>
<li>Fixed wrong formatting for SAP attributes with decimal data type. This was happening for SAP OData v2 services.</li>
<li>On the Integration Manager application, made clearer the title of the Associate connection screen.</li>
</ul>
<h2 id="Integration_Builder_1.20.0">Integration Builder 1.20.0</h2>
<div class="info">
<p>Released on Sep 6, 2021</p>
</div>
<h3>Bug fixing</h3>
<ul>
<li>Fixed an issue that caused errors in Sharepoint integrations when SharePoint lists have special characters.</li>
<li>Fixed an issue that prevented Integration Builder from generating Dataverse/Dynamics integrations when a selected table didn’t have a plural label.</li>
<li>Fixed an issue that prevented Integration Builder from publishing updates on the integrations with outdated dependencies.</li>
<li>Fixed an issue that caused a wrong sort by Provider on Integrations and Connections list in Integration Manager.</li>
<li>Improvement on error message when navigating to an outdated Integration Manager.</li>
<li>Added favicon in a few screens that didn’t have them.</li>
<li>Improvements in one illustration on the Publish screen success state.</li>
</ul>
<h2 id="Integration_Builder_1.19.0">Integration Builder 1.19.0</h2>
<div class="info">
<p>Released on Aug 23, 2021</p>
</div>
<h3>New in Integration Builder 1.19.0</h3>
<ul>
<li>Improved the layout of the screens where you create connections for Dataverse/Dynamics 365, Salesforce, and SharePoint.</li>
</ul>
<h3>Bug fixing</h3>
<ul>
<li>Fixed an issue that caused an incorrect redirect when denying Salesforce authorization in Integration Manager.</li>
<li>Fixed an issue that caused an incorrect redirect from the landing page when opening an integration that failed to publish.</li>
<li>Fixed an issue that prevented users from managing integrations in an invalid state that was caused by errors in the publishing process.</li>
<li>Fixed an issue that caused incorrect mandatory classifications on Microsoft Dataverse attributes.</li>
<li>Fixed an issue that prevented Integration Builder from listing all the entity attributes for some SAP specifications.</li>
<li>Fixed an issue generating Dataverse/Dynamic 365 integrations when an attribute is related to several tables.</li>
<li>Fixed an issue where users could create Salesforce connections with lower permissions than intended.</li>
</ul>
<h2 id="Integration_Builder_1.18.0">Integration Builder 1.18.0</h2>
<div class="info">
<p>Released on Aug 9, 2021</p>
</div>
<h3>Bug fixing</h3>
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
<h2 id="Integration_Builder_1.17.0">Integration Builder 1.17.0</h2>
<div class="info">
<p>Released on July 28, 2021</p>
</div>
<h3>New in Integration Builder 1.17.0</h3>
<ul>
<li>In Integration Manager, it's now possible to delete connections with the draft status.</li>
</ul>
<h3>Bug fixing</h3>
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
<h2 id="Integration_Builder_1.16.0">Integration Builder 1.16.0</h2>
<div class="info">
<p>Released on July 19, 2021</p>
</div>
<h3>New in Integration Builder 1.16.0</h3>
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

