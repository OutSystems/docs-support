---
locale: en-us
guid: 93380812-9b02-4134-b942-de90c9395f9e
app_type: traditional web apps, mobile apps, reactive web apps
---

<h1>Platform Server</h1>
<h2 id="Platform_Server_11.15.0">Platform Server 11.15.0</h2>
<div class="info"><p>Released on Mar 07, 2022</p></div>
<h3 id="New_in_Platform_Server_11.15.0">New in Platform Server 11.15.0</h3>
<ul>
<li>Upgraded RabbitMQ Server to 3.9.11 and Erlang to 24.2. These components are used by the OutSystems Cache Invalidation Service. (R11PIT-518)</li>
<li>Added support for integrating with PostgreSQL / Aurora PostgreSQL as external database connections via Service Center. (RDV-277)</li>
</ul>
<h3 id="Bug_Fixing_0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused 1-Click Publish to incorrectly trigger the native build of a mobile app when the previous build had an error and there were no changes in the app. (R11PBT-122)</li>
<li>Fixed an issue preventing 1-Click Publish to trigger the native build of a mobile app after significant changes. (R11PBT-235)</li>
<li>Fixed an issue preventing the DBCleaner API from deleting sequences in Oracle databases. (R11PBT-374)</li>
<li>Fixed the Deploy Service log message when preparing to deploy. The log message now includes only the modules to be deployed. (R11PBT-409)</li>
<li>Fixed an issue that prevented the Deploy Service from undeploying modules that were deleted while the service was down. (R11PBT-410)</li>
<li>Fixed an issue causing invalid tenant views after dropping the Tenant_Id attribute of Entities that are no longer multi-tenant. (R11PBT-415)</li>
<li>Fixed Server.API and Server.Identity failing to start with error "Cannot access a disposed object. Object name: 'IServiceProvider'." (R11PIT-481)</li>
<li>Added a validation to prevent the publishing of the same solution simultaneously. (R11PIT-63)</li>
<li>Fixed an issue in the DropDownMenu widget of RichWidgets that forced the end user to click twice when collapsing the dropdown. Applies only to Traditional Web apps. (ROU-615)</li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1092" rel="custom">Fixed an issue preventing Processes that are launched on the creation of new Entity records from being triggered for specific tenants after changing the Entity to multi-tenant. (RPM-1092)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1441" rel="custom">Fixed an issue that caused records to be deleted from OSSYS_MODULEFRONTEND table if duplicates were found, when upgrading the Platform Server component to 11.12.2 or later. (RPM-1441)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1527" rel="custom">Improved the End-Users Configuration screen of Service Center to clarify the metrics shown for the Total Internal and Total External Users. (RPM-1527)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1551" rel="custom">Fixed an issue that caused the 1-Click Publish to fail with an error "Invalid compiler output. Unknown reference expression type Email" when publishing a module that references a Static Entity which has an Attribute of type Email. (RPM-1551)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1577" rel="custom">Fixed an issue that caused the starvation of Scheduler Service activities in Personal Environments. (RPM-1577)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1653" rel="custom">Fixed an issue that caused the 1-Click Publish to fail with a compilation error when publishing a module that references a Static Entity which has an Attribute value that needs an implicit conversion to match the defined type.  (RPM-1653)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1715" rel="custom">Fixed an issue in the Input_AutoComplete widget of RichWidgets when used with a text widget under specific conditions. Applies only to Traditional Web apps. (RPM-1715)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1874" rel="custom">When using LDAP authentication, the end user's last login information is now is properly updated. (RPM-1874)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1876" rel="custom">Fixed a runtime error that occurred when adding or deleting attributes to a multi-tenant Entity and the publishing of the corresponding change is aborted during the execution of the DB scripts. Applies only to Oracle databases. (RPM-1876)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1902" rel="custom">Improved the role validation of the end user accessing the Users application. (RPM-1902)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1934" rel="custom">Fixed an issue that caused the application publishing operation to hang when the application definitions in the database are in an invalid state. (RPM-1934)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-1980" rel="custom">Fixed an issue that caused the Scheduler Service to timeout earlier than expected when running Light Processes. (RPM-1980)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-2061" rel="custom">The Tuning and Security section of the Installation Checklist now refers to the supported scenario of configuring the cache invalidation service with high availability. (RPM-2061)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-2075" rel="custom">Added information to the Installation Checklist regarding the expected values for Oracle Asynchronous Commit parameters. (RPM-2075)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-564" rel="custom">Fixed an error occurring in Oracle environments when filtering the email logs by Status in Service Center. (RPM-564)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-999" rel="custom">Fixed the Japanese translations of some labels in the Users application. (RPM-999)</a></li>
</ul>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.15.0#RPM-726" rel="custom">Fixed a CSP related issue in Service Center console. CVSSv3.1 score 2.3 (Low). (RPM-726)</a></li>

<h3 id="Known_Issues_0">Known Issues</h3>
<ul>
<li>Third party PostgreSQL connectors that use "npgsql.dll", like "ardoPostgreSQL Database Connector", may work incorrectly.
This Platform Server version introduces a supported PostgreSQL / Aurora PostgreSQL connector that uses a custom version of "npgsql.dll". Even thought this custom dll version is design to be backwards compatible, OutSystems can't guarantee that unsupported third-party connectors behave as expected while using it.
OutSystems recommends migrating from third party PostgreSQL connectors to the OutSystems PostgreSQL / Aurora PostgreSQL connector by following the <a href="https://success.outsystems.com/Documentation/How-to_Guides/Integrations/Migrate_from_ardoPostgreSQL_to_supported_PostgreSQL_connector">migration guide</a>.</li>
</ul><style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style><div class="moreDetailsDiv"><h3 id="More_details_0">More details</h3><p><a id="RPM-1092"><strong>RPM-1092</strong></a><br/><b>Fixed an issue preventing Processes that are launched on the creation of new Entity records from being triggered for specific tenants after changing the Entity to multi-tenant.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>After changing a single-tenant module and a module's Entity to multi-tenant, Processes that are launched on the creation of new records in that Entity are not triggered for users of a new tenant. Those Processes are triggered only for users of the default tenant.</p><p><a id="RPM-1441"><strong>RPM-1441</strong></a><br/><b>Fixed an issue that caused records to be deleted from OSSYS_MODULEFRONTEND table if duplicates were found, when upgrading the Platform Server component to 11.12.2 or later.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>While upgrading the Platform Server component to version 11.12.2 or later, clicking the "Create/Upgrade Database" button in the Configuration Tool would cause all records to be deleted from OSSYS_MODULEFRONTEND table if there were duplicates in that table. This issue would prevent Timers and Processes to run.</p><p><a id="RPM-1527"><strong>RPM-1527</strong></a><br/><b>Improved the End-Users Configuration screen of Service Center to clarify the metrics shown for the Total Internal and Total External Users.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>On the Administration &gt; Licensing &gt; End-Users Configuration screen of the Service Center console, the Total Internal Users and Total External Users values don't match the sum of the users listed in the User Distribution Per User Provider list. Although the values follow the calculation rules for internal and external users, the screen UI suggests a mismatch of values. We have improved this Service Center screen to make those values clear.</p><p><a id="RPM-1551"><strong>RPM-1551</strong></a><br/><b>Fixed an issue that caused the 1-Click Publish to fail with an error "Invalid compiler output. Unknown reference expression type Email" when publishing a module that references a Static Entity which has an Attribute of type Email.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>When referencing a Static Entity which has an Attribute of type Email, the consumer module would fail to compile with the error "Unknown reference expression type Email".</p><p><a id="RPM-1577"><strong>RPM-1577</strong></a><br/><b>Fixed an issue that caused the starvation of Scheduler Service activities in Personal Environments.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">OutSystems Services</span> <br/><br/><u>Fix Details:</u><br/>OutSystems Personal Environments run in a shared infrastructure. One environment with heavy Processes usage may cause database contention and accumulation of the Activities to process. In this situation, other environments may experience starvation of the Scheduler Service, namely, Process Activities are queued and stay in “Created” state for a long time.</p><p><a id="RPM-1653"><strong>RPM-1653</strong></a><br/><b>Fixed an issue that caused the 1-Click Publish to fail with a compilation error when publishing a module that references a Static Entity which has an Attribute value that needs an implicit conversion to match the defined type. </b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>When referencing a Static Entity which has an Attribute value that needs an implicit conversion to match the defined type, the consumer module would fail to compile. This would happen in the following scenarios:
<ul>
<li>Having an Integer or Long Integer type with a Decimal, Boolean or Identifier value</li>
<li>Having a DateTime type with a Date or Time value</li>
<li>Having a Date type with a DateTime value</li>
<li>Having a Time type with a DateTime value</li>
</ul>
An error could also happen while compiling a module containing a Static Entity with a Long Integer type and a Boolean value, without the need to actually reference it.</p><p><a id="RPM-1715"><strong>RPM-1715</strong></a><br/><b>Fixed an issue in the Input_AutoComplete widget of RichWidgets when used with a text widget under specific conditions. Applies only to Traditional Web apps.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>In Traditional Web apps, using an Input_AutoComplete widget of RichWidget with a text widget, such as the Input widget, that has a Max. Length value and the Text Lines property is greater than 1, causes an error when selecting the value from the Input_AutoComplete widget.</p><p><a id="RPM-1874"><strong>RPM-1874</strong></a><br/><b>When using LDAP authentication, the end user's last login information is now is properly updated.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>An issue in the Users application was preventing the end user's last login information to be updated in the database when using LDAP authentication.</p><p><a id="RPM-1876"><strong>RPM-1876</strong></a><br/><b>Fixed a runtime error that occurred when adding or deleting attributes to a multi-tenant Entity and the publishing of the corresponding change is aborted during the execution of the DB scripts. Applies only to Oracle databases.</b><br/><span class="cattag">Application Runtime</span> <br/><br/><u>Fix Details:</u><br/>This issue occurs only in Oracle databases, when you change the structure of a multi-tenant Entity, by adding or deleting attributes, and the module fails to publish during the execution of the DB scripts. In this situation, the multi-tenant views are not updated, causing ORA-00904 errors in runtime.</p><p><a id="RPM-1902"><strong>RPM-1902</strong></a><br/><b>Improved the role validation of the end user accessing the Users application.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>Using a specific development pattern, this issue would allow an anonymous session to access and modify information in the Users application.</p><p><a id="RPM-1934"><strong>RPM-1934</strong></a><br/><b>Fixed an issue that caused the application publishing operation to hang when the application definitions in the database are in an invalid state.</b><br/><span class="cattag">Publish Operation</span> <br/><br/><u>Fix Details:</u><br/>This issue causes the application publishing operation to hang in step "Creating Application" with no errors being returned, and the application pool stops working.</p><p><a id="RPM-1980"><strong>RPM-1980</strong></a><br/><b>Fixed an issue that caused the Scheduler Service to timeout earlier than expected when running Light Processes.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Processes</span> <br/><br/><u>Fix Details:</u><br/>When a Light Process reaches the default timeout, 180s, the request in the IIS is not aborted. After some time, when a new attempt is made to run the Light Process, the new request also shows up in the IIS. The original request only disappears from the pool after 300s, which is the default timeout of regular Processes.</p><p><a id="RPM-2061"><strong>RPM-2061</strong></a><br/><b>The Tuning and Security section of the Installation Checklist now refers to the supported scenario of configuring the cache invalidation service with high availability.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Installation Checklist</span> <br/><br/><u>Fix Details:</u><br/>For customers requiring that <a href="https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Cache_Invalidation_in_OutSystems_11#when-ha">the cache invalidation service is always available</a>, it's possible to configure RabbitMQ to work as a cluster. This information has now been included in the Tuning and Security section of the Installation Checklist to give visibility of this option.</p><p><a id="RPM-2075"><strong>RPM-2075</strong></a><br/><b>Added information to the Installation Checklist regarding the expected values for Oracle Asynchronous Commit parameters.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Data Access and Manipulation</span> <br/><br/><u>Fix Details:</u><br/>In Oracle databases, having the Asynchronous Commit feature enabled may lead to runtime errors related to integrity constraints violation or null pointers. To prevent these errors, we added to the Installation Checklist the supported values for the Oracle Asynchronous Commit parameters.</p><p><a id="RPM-564"><strong>RPM-564</strong></a><br/><b>Fixed an error occurring in Oracle environments when filtering the email logs by Status in Service Center.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>This issue occurs in Oracle environments, on the Service Center &gt; Monitoring &gt; Email screen. Filtering the email logs by Status causes the error " ORA-01843: not a valid month".</p><p><a id="RPM-726"><strong>RPM-726</strong></a><br/><b>Fixed a CSP related issue in Service Center console. CVSSv3.1 score 2.3 (Low).</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">LifeTime</span> <br/><br/><u>Fix Details:</u><br/>Service Center console was failing to include Content Security Policy directives.</p><p><a id="RPM-999"><strong>RPM-999</strong></a><br/><b>Fixed the Japanese translations of some labels in the Users application.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>*Symptoms*
Incorrect labels in Users application in Japanese locale.

*How to reproduce*
Change the locale to "ja-jp" and access the Users module</p>
</div>
<h2 id="Platform_Server_11.14.1">Platform Server 11.14.1</h2>
<div class="info"><p>Released on Feb 14, 2022</p></div>
<h3 id="New_in_Platform_Server_11.14.1">New in Platform Server 11.14.1</h3>
<ul>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1942" rel="custom">Improved the performance of the LDAP actions in the Authentication extension, Authentication.xif, when using the LDAPS protocol. (RPM-1942)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1977" rel="custom">Improved the performance of IT users login operation using Active Directory authentication when there is a significant number of AD groups with specific configurations. (RPM-1977)</a></li>
</ul>
<h3 id="Bug_Fixing_1">Bug Fixing</h3>
<ul>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1184" rel="custom">Fixed an error when publishing a module in Service Studio caused by a DLL file being locked by another process. (RPM-1184)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1240" rel="custom">Removed the "Republish all modules" step from the Installation Checklist for Oracle configuration. (RPM-1240)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1263" rel="custom">Fixed an issue that prevented editing entity data in Service Studio when the module is published in a catalog different from the main catalog. (RPM-1263)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1309" rel="custom">Fixed an issue allowing to update non-editable fields in an Editable Table widget when saving the record with an open Data Picker. Applies to Traditional Web Apps. (RPM-1309)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1398" rel="custom">The default value of the session timeout for Reactive Web Apps now matches the default value of the session timeout for Traditional Web Apps (20m). (RPM-1398)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1440" rel="custom">Fixed the error "ORA-00911: invalid character" occurring in the Configuration Tool when clicking "Create/Upgrade Database" for the platform or logging database. This error applies to Oracle installations in farm configuration. (RPM-1440)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1469" rel="custom">Fixed an issue causing the System Components installation to fail during upgrades in farm installations with a pure Deployment Controller setup. (RPM-1469)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1634" rel="custom">Fixed an error causing the Platform Server installation or upgrade to fail in environments with customized IIS Site Bindings. (RPM-1634)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1675" rel="custom">SAML authentication is now more resilient to session variables issues during the logout operation. (RPM-1675)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1798" rel="custom">Fixed an issue that could cause a native app to receive the application manifest for the browser version and vice-versa. (RPM-1798)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1890" rel="custom">Fixed a memory leak occurring on each first request that is done on a module. (RPM-1890)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1896" rel="custom">Fixed an issue when consuming a SOAP Wsdl with an inheritance pattern. (RPM-1896)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1997" rel="custom">Fixed an error during a Platform Server major upgrade from version 10 to version 11.13.2 or 11.14.0 occurring in the preparation step of System Components dependencies. (RPM-1997)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-2006" rel="custom">Fixed performance degradation when running the platform database in some Azure configurations. (RPM-2006)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-670" rel="custom">Fixed an issue causing the Server.Identity service to timeout when getting refresh tokens from the database in Oracle. (RPM-670)</a></li>
</ul>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1515" rel="custom">Fixed a configuration in Factory Configuration that could lead to DoS attacks. CVSSv3.1 score 5.3 (Medium). (RPM-1515)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1696" rel="custom">Fixed an XSS issue in the Label widget for Traditional Web Apps. CVSSv3.0 score 5.9 (Medium). (RPM-1696)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.1#RPM-1781" rel="custom">Fixed a security vulnerability preventing non-body parameters of a consumed REST API to be redacted. CVSSv3.1 score 4.9 (Medium). (RPM-1781)</a></li>

<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style><div class="moreDetailsDiv"><h3 id="More_details_1">More details</h3><p><a id="RPM-1184"><strong>RPM-1184</strong></a><br/><b>Fixed an error when publishing a module in Service Studio caused by a DLL file being locked by another process.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>Publishing a module in Service Studio failed with the error "Internal Error: Cannot delete the file '<dll file="">'. Please check if a third-party program is using it and try again". Republishing the module would overcome the issue.</dll></p><p><a id="RPM-1240"><strong>RPM-1240</strong></a><br/><b>Removed the "Republish all modules" step from the Installation Checklist for Oracle configuration.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Installation Checklist</span> <br/><br/><u>Fix Details:</u><br/>The Installation Checklist of Platform Server 11.13.2 or later still included the step "Republish all modules" for Oracle configuration, although that step is not required anymore.</p><p><a id="RPM-1263"><strong>RPM-1263</strong></a><br/><b>Fixed an issue that prevented editing entity data in Service Studio when the module is published in a catalog different from the main catalog.</b><br/><span class="cattag">Service Studio</span> <span class="cattag">Data Access and Manipulation</span> <br/><br/><u>Fix Details:</u><br/>For modules published in a catalog different from the main catalog, editing the entity data in Service Studio using the "View or Edit Data" option failed with the error "Invalid object name '<table_physical_name>'" for SQL Server or "ORA-00942 - Table or View does not exist" for Oracle databases.</table_physical_name></p><p><a id="RPM-1309"><strong>RPM-1309</strong></a><br/><b>Fixed an issue allowing to update non-editable fields in an Editable Table widget when saving the record with an open Data Picker. Applies to Traditional Web Apps.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Interface</span> <br/><br/><u>Fix Details:</u><br/>This issue occurs in Traditional Web Apps when using an Editable Table widget with the Date Picker UI Pattern. If the Date Picker is open when saving a new or updated record, the non-editable fields of that record become editable. It only happens for the specific record that was updated with the Date Picker open. Updating the record again with the Date Picker closed makes the field non-editable again.</p><p><a id="RPM-1398"><strong>RPM-1398</strong></a><br/><b>The default value of the session timeout for Reactive Web Apps now matches the default value of the session timeout for Traditional Web Apps (20m).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Authentication and Authorization</span> <br/><br/><u>Fix Details:</u><br/>When Single Sign-On Between App Types is enabled in Service Center, having different session timeout values for Traditional Web and Reactive Web applications can lead to a redirect loop during the authentication flow, preventing end-users to use the applications.</p><p><a id="RPM-1440"><strong>RPM-1440</strong></a><br/><b>Fixed the error "ORA-00911: invalid character" occurring in the Configuration Tool when clicking "Create/Upgrade Database" for the platform or logging database. This error applies to Oracle installations in farm configuration.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>In Oracle installations, clicking the "Create/Upgrade Database" button in the Platform tab or in the Log tab would cause the error "ORA-00911: invalid character". This scenario occurred in installations with farm configuration.</p><p><a id="RPM-1469"><strong>RPM-1469</strong></a><br/><b>Fixed an issue causing the System Components installation to fail during upgrades in farm installations with a pure Deployment Controller setup.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Installer</span> <br/><br/><u>Fix Details:</u><br/>This issue occurs when upgrading the Platform Server in farm installations having a pure Deployment Controller setup - only the Deployment Controller Service is enabled in the machine. In this scenario, the installation of the System Components through the Configuration Tool fails with the following message: "There was an error while contacting the server. HTTP not found".</p><p><a id="RPM-1515"><strong>RPM-1515</strong></a><br/><b>Fixed a configuration in Factory Configuration that could lead to DoS attacks. CVSSv3.1 score 5.3 (Medium).</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Application Server</span> <br/><br/><u>Fix Details:</u><br/>*Symptoms*
A malicious user can send HTTP requests for a resource inside a server using a property of the request's header called "Range."
This "Range" property allows selecting a different number of byte ranges from the resource that is being requested.
So a single request can recover the entire content of the resource a hundred times, enforcing a response with a considerable amount of data growing geometrically for every range requested. 
With a sufficient number of requests with many "Ranges," it is possible to coordinate a Denial of Service Attack.

*How to reproduce*
Steps to replicate / Proof of Concept
Create an application in an OutSystems environment
Open a browser (Firefox, for instance) and open the inspector/Developer Tools
Turn off caching in the inspector/Developer Tools
Click on the Network tab in the inspector and access the login page of the app (no need to log in)
Find a successful request in the network activity, manipulate the request, and resend it.
In Firefox, right-click the request &gt; Edit and Resend &gt; add the Range header with the values seen in the screenshot above &gt; click send
If you compare the responses, you will notice the response to the request containing the Range header will have a larger size proportionate to the number of "0-" added to the Range header on the request:

There is also a video capture inside the https://outsystemsrd.atlassian.net/browse/VUL-232 explaining how to reproduce the problem using the firefox browser.
but </p><p><a id="RPM-1634"><strong>RPM-1634</strong></a><br/><b>Fixed an error causing the Platform Server installation or upgrade to fail in environments with customized IIS Site Bindings.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Installer</span> <br/><br/><u>Fix Details:</u><br/>When installing or upgrading the Platform Server component in an environment having customized IIS Site Bindings, the installer hangs in the last step, "Starting Microsoft Internet Information Services", and has to be terminated manually.</p><p><a id="RPM-1675"><strong>RPM-1675</strong></a><br/><b>SAML authentication is now more resilient to session variables issues during the logout operation.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>When doing a logout operation, the end user sometimes is redirected to the IIS default page (for self-managed environments) or to Service Center (for OutSystems Cloud). The issue occurs because the value of the session cookie storing the destination URL after logout is lost. It happens intermittently and there is no service loss. Some browsers seem more susceptible to the occurrence.</p><p><a id="RPM-1696"><strong>RPM-1696</strong></a><br/><b>Fixed an XSS issue in the Label widget for Traditional Web Apps. CVSSv3.0 score 5.9 (Medium).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Interface</span> <br/><br/><u>Fix Details:</u><br/>In Traditional Web Apps, the Label widget was not escaped by default. This could lead to XSS code injection when using the widget with an expression.</p><p><a id="RPM-1781"><strong>RPM-1781</strong></a><br/><b>Fixed a security vulnerability preventing non-body parameters of a consumed REST API to be redacted. CVSSv3.1 score 4.9 (Medium).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>This issue caused the redaction of non-body parameters of a consumed REST API not to be applied when the Logging Level was set to Full or Troubleshoot.</p><p><a id="RPM-1798"><strong>RPM-1798</strong></a><br/><b>Fixed an issue that could cause a native app to receive the application manifest for the browser version and vice-versa.</b><br/><span class="cattag">Application Runtime</span> <br/><br/><u>Fix Details:</u><br/>The app is trying to fetch the .IDB.js files even when is running in a native shell. This means that the app is receiving the wrong manifest. </p><p><a id="RPM-1890"><strong>RPM-1890</strong></a><br/><b>Fixed a memory leak occurring on each first request that is done on a module.</b><br/><span class="cattag">Application Runtime</span> <br/><br/><u>Fix Details:</u><br/>In environments running Platform Server 11.9.0 or later, the resources associated with the first request that loads a module in IIS are never released, adding extra constant memory overhead associated with each module loaded. The memory leak can be observed using debugger tools for Microsoft Windows, such as WinDbg.</p><p><a id="RPM-1896"><strong>RPM-1896</strong></a><br/><b>Fixed an issue when consuming a SOAP Wsdl with an inheritance pattern.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>Compilation error: Sequence contains no matching element After Platform upgrade to 11.13.2</p><p><a id="RPM-1942"><strong>RPM-1942</strong></a><br/><b>Improved the performance of the LDAP actions in the Authentication extension, Authentication.xif, when using the LDAPS protocol.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Authentication and Authorization</span> <br/><br/><u>Fix Details:</u><br/>When using LDAP authentication, calls to LDAP actions of the Authentication.xif extension are very slow. Also, each LDAP action will cause the log message "Fallback to use user domain". This scenario occurs when using the LDAPS protocol.</p><p><a id="RPM-1977"><strong>RPM-1977</strong></a><br/><b>Improved the performance of IT users login operation using Active Directory authentication when there is a significant number of AD groups with specific configurations.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>When using Active Directory for IT users authentication, the login operation is very slow, affecting the access to the development tools, such as Service Studio. This situation can generate slow execution log entries of the Authentication.ActiveDirectory_GetAccountGroups action in the Extension logs. This happens when there is a significant number of groups in the Active Directory and the authentication configuration requires users to belong to specific AD group(s). The AD groups associated with users can now be cached, speeding up the login process.</p><p><a id="RPM-1997"><strong>RPM-1997</strong></a><br/><b>Fixed an error during a Platform Server major upgrade from version 10 to version 11.13.2 or 11.14.0 occurring in the preparation step of System Components dependencies.</b><br/><span class="cattag">Platform Installation</span> <br/><br/><u>Fix Details:</u><br/>When executing a major Platform Server upgrade from version 10 to version 11.13.2 or 11.14.0, the preparation step of System Components dependencies, running in the Configuration Tool, failed with the error "Value cannot be null". This issue prevents the upgrade operation to the indicated versions.</p><p><a id="RPM-2006"><strong>RPM-2006</strong></a><br/><b>Fixed performance degradation when running the platform database in some Azure configurations.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Data Access and Manipulation</span> <br/><br/><u>Fix Details:</u><br/>Self-managed environments with SQL Server platform database being hosted as an Azure Managed Instance would experience significant performance degradation on database access when running Platform Server 11.12.2 or later.</p><p><a id="RPM-670"><strong>RPM-670</strong></a><br/><b>Fixed an issue causing the Server.Identity service to timeout when getting refresh tokens from the database in Oracle.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Authentication and Authorization</span> <br/><br/><u>Fix Details:</u><br/>In Oracle environments, IT users are not able to login in OutSystems tools, such as the Workflow Builder, Experience Builder, or Service Center. The issue is caused by a timeout of the Server.Identity service when the OSSYS_REFRESH_TOKENS database table has hundreds of thousands of records, preventing this service to provide a new access token to the tools.</p>
</div>
<h2 id="Platform_Server_11.14.0">Platform Server 11.14.0</h2>
<div class="info"><p>Released on Dec 06, 2021</p></div>
<h3 id="New_in_Platform_Server_11.14.0">New in Platform Server 11.14.0</h3>
<ul>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1677" rel="custom">Changes to REST APIs or SOAP Web Services settings executed via Service Center on the module's Integrations tab are now recorded in the General Log. (RPM-1677)</a></li>
<li>Features related to emails for Mobile and Reactive Web Apps are now generally available in Platform Server. You could use the features previously in technical the previews "Emails for Mobile and Reactive" and "Attachments in Mobile and Reactive emails". (RTAFA-75)</li>
<li>Now you can configure friendly URLs in your Reactive Web Apps. Go to Service Center &gt; Administration &gt; SEO URLs to set up the site rules and redirects. Configure the page rules in Service Studio, by setting Custom URLs to Yes in the Screen properties. (RTAFB-5050)</li>
</ul>
<h3 id="Bug_Fixing_2">Bug Fixing</h3>
<ul>
<li>Fixed issues that occurred when clicking "Apply and Exit" in the Configuration Tool after changing database configurations. (R11PBT-231)</li>
<li>Fixed missing detailed stacks in the error logs of the Deployment Controller service. (R11PBT-347)</li>
<li>Deleting a Static Entity from a Library module no longer causes an upgrade error when publishing the compiled code. (R11PBT-359)</li>
<li>Fixed an issue that prevented the Configuration Tool to modify certain configuration files when they had been changed by an external source. (R11PIT-259)</li>
<li>The validation rule for a mobile App Identifier in Service Center is now aligned with iOS and Android app stores. The validation messages were also updated accordingly. (RNMT-5047)</li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1024" rel="custom">Fixed the validation of user Roles in Reactive Web Apps to ensure this step is performed only after loading the Roles information from the server. (RPM-1024)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1041" rel="custom">Fixed an issue when consuming a SOAP Web Service with HTTP transport binding. (RPM-1041)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1075" rel="custom">Now, using DbCleaner API to delete a multi-tenant entity, event entity, or a multilingual static entity, also deletes the database objects associated with those entities. (RPM-1075)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1115" rel="custom">Fixed an issue that was blocking the activation/deactivation of Timers in cloned modules. (RPM-1115)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1118" rel="custom">Fixed an issue that could cause incorrect code generation for SQL nodes with expand inline parameters in Oracle databases, after upgrading the Platform Server component to 11.12.0 or later. (RPM-1118)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1125" rel="custom">Fixed an issue that could cause modules to have outdated dependencies after a Platform Server upgrade. (RPM-1125)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1177" rel="custom">The Roles screen of the Users application is now correctly listing only the end users having that role. (RPM-1177)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1190" rel="custom">Fixed an issue that could cause incorrect code generation for SQL nodes with expand inline parameters in SQL Server databases, after upgrading the Platform Server component to 11.12.0 or later. (RPM-1190)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1198" rel="custom">Fixed an error when publishing the System Components solution during the upgrade to Platform Server 11.12.0 or later caused by producer modules not being prepared. (RPM-1198)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1260" rel="custom">Fixed an issue that prevented Timers, Emails, and Processes from running after changing the name of the Server. (RPM-1260)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1272" rel="custom">Fixed the "Unable to find the specified file" error when publishing the System Components solution during a Platform Server upgrade. (RPM-1272)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1296" rel="custom">Fixed an issue that could cause a timeout when publishing the Service Center component through the Configuration Tool using an Oracle database. (RPM-1296)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1325" rel="custom">Fixed an error when publishing the Service Center component during a Platform Server installation or upgrade using an Oracle database. This error occurred only when the user OSADMIN had no permissions to execute the DBMS_RANDOM Oracle package. (RPM-1325)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1374" rel="custom">Fixed the "Error getting publication state" error when publishing the System Components solution during a Platform Server upgrade. (RPM-1374)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1420" rel="custom">Fixed application deployment issues when Dynatrace was enabled in the environment. (RPM-1420)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1421" rel="custom">Fixed an issue that led to 404 Traditional Web app screens using an SEO Page Rule that started with "rest". (RPM-1421)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1456" rel="custom">Updated the installation checklist instructions for integration with IBM Db2 databases. (RPM-1456)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1522" rel="custom">Fixed the error "ORA-01489: result of string concatenation is too long" when publishing a module with an Action which description exceeds 4000 bytes. This issue occurred only in Oracle databases. (RPM-1522)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1526" rel="custom">Fixed an issue that caused third-party components that used click events to not work as expected in PWA Mobile apps. (RPM-1526)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1561" rel="custom">The Configuration Tool no longer proceeds with the Apply and Exit operation if the Platform Administrator password is empty. (RPM-1561)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1575" rel="custom">Fixed the Test Connection validation in the Configuration Tool when using Windows Authentication. (RPM-1575)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1608" rel="custom">The Platform Server installer no longer installs .Net Core 2.1. (RPM-1608)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1623" rel="custom">Fixed an issue that cause Reactive Web Apps to show a blank screen when opening them through a URL with a hash (#). (RPM-1623)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1644" rel="custom">Fixed the "c is not a function" runtime error occurring on some occasions for Reactive Web Apps and Mobile Apps distributed as a PWA after a Platform Server upgrade. (RPM-1644)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1684" rel="custom">Link widgets that match the current screen are now correctly added the "active" CSS class. (RPM-1684)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1917" rel="custom">Removed the service account that was causing errors during publication of System Components in environments with Active Directory authentication configured. (RPM-1917)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1923" rel="custom">Fixed several missing logs in Service Center (e.g. Error and General logs). (RPM-1923)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-2022" rel="custom">Fixed issues that occurred when clicking "Apply and Exit" in the Configuration Tool after changing database configurations. (RPM-2022)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-478" rel="custom">Fixed an issue that caused Entity_DropTable and Attribute_DropColumn actions of DbCleaner API to throw an ORA-00942 error when dropping entities or attributes in modules created in Oracle database schemas other than the main one. (RPM-478)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-542" rel="custom">Now, it's not possible to delete the active External Authentication Provider plugin. (RPM-542)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-546" rel="custom">Fixed an issue that caused timeout when accessing the solution publish screen when the publish report has a very high number of messages. (RPM-546)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-593" rel="custom">Fixed the error message returned when publishing a module after trying to modify the length of a Text Id attribute of an Entity. (RPM-593)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-714" rel="custom">Fixed an issue blocking the external authentication of IT users using then AD authentication provider when using multiple deployment zones and not having the System Components deployed in the Default zone. Improved also the error message shown in this scenario. (RPM-714)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-741" rel="custom">As a security improvement, extensions are no longer automatically recompiled on upgrade. (RPM-741)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-754" rel="custom">Fixed an issue that prevented DbCleaner API to delete attributes of multitenant database views. (RPM-754)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-768" rel="custom">The actions Entity_DropTable and Attribute_DropColumn from DbCleaner API now have a success output indicating if the drop operation was performed or not. (RPM-768)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-939" rel="custom">Fixed an issue that was causing Service Center to throw an error when exporting to excel the Screen Requests logs filtered by Application. (RPM-939)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-945" rel="custom">Fixed an issue that could cause modules to have outdated dependencies after a Platform Server upgrade. (RPM-945)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-952" rel="custom">Fixed an issue that occurred in Reactive Web apps and that prevented clearing an invalid value from a Text, Phone, or Email variable. (RPM-952)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-977" rel="custom">Fixed the warning "Resource Not Versioned" when deploying Reactive Web Apps. (RPM-977)</a></li>
<li>Fixed an issue that didn't show the result at runtime of expressions CurrTime(), and CurrDateTime() in the Title of screens of Reactive Web and Mobile apps. This issue occurred only after publishing using Windows-only Service Studio and using these functions in the Title property of the screen. (RTAFB-4791)</li>
<li>Fixed runtime errors in Mobile and Reactive Web Apps when directly assigning an Attachment data type variable with an Attachment data type value returned by a Producer module. Attachments in Mobile and Reactive emails is a Technical Preview feature. (RTAFB-4792)</li>
</ul>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1093" rel="custom">Fixed data vulnerability due to excessive logging. CVSSv3.1 score 4.4 (Medium). (RPM-1093)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1584" rel="custom">Fixed a broken access control vulnerability in some buttons of Service Center. CVSSv3.0 score 5.4 (Medium). (RPM-1584)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-1804" rel="custom">Fixed a security issue that could allow users to view Application details in Service Center to which they don't have permissions. Only affects environments not connected to LifeTime. CVSSv3.1 score 4.3 (Medium) (RPM-1804)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-447" rel="custom">Fixed multiple cross-site scripting (XSS) vulnerabilities in Popup_Editor, Popup_EditorForUpload, or Popup_EditorVanilla titles. CVSSv3.1 score 3.1 (Low) (RPM-447)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-747" rel="custom">Fixed a security vulnerability on an internal Service Center API permission requirement. CVSSv3.1 score 6.3 (Medium). (RPM-747)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.14.0#RPM-966" rel="custom">Fixed a security issue that could lead to session fixation problems. CVSSv3.1 score 5.4 (Medium). (RPM-966)</a></li>

<h3 id="Breaking_Change_0">Breaking Change</h3>
<ul>
<li>The title of the Popup_Editor, Popup_EditorForUpload, and Popup_EditorVanilla is now encoded to prevent cross-site scripting (XSS) attacks. This may cause it to appear garbled in very specific scenarios.<br/>
Check <a href="https://success.outsystems.com/Support/Archive/11/OutSystems_Platform_side_effects_and_breaking_changes" rel="internal">OutSystems 11 side effects and breaking changes</a> for more details on the breaking change and a possible workaround. </li>
</ul>
<h3 id="Known_Issues_1">Known Issues</h3>
<ul>
<li>This Platform Server version suffers from an issue where factories with more than 1000 application permissions have their platform users (e.g. LifeTime, Service Center and Service Studio) losing permissions over the applications of an environment. This issue was introduced with Platform Server 11.14.0 and has been mitigated in Platform Server 11.16.0.</li>
</ul><style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style><div class="moreDetailsDiv"><h3 id="More_details_2">More details</h3><p><a id="RPM-1024"><strong>RPM-1024</strong></a><br/><b>Fixed the validation of user Roles in Reactive Web Apps to ensure this step is performed only after loading the Roles information from the server.</b><br/><span class="cattag">Application Runtime</span> <br/><br/><u>Fix Details:</u><br/>When the Single Sign-On Between App Types feature is on, end users performing the login on a Traditional Web App and then moving to a Reactive Web App might be redirected to the Invalid Permissions Screen, if the Default Screen is more restricted than the Registered Role.</p><p><a id="RPM-1041"><strong>RPM-1041</strong></a><br/><b>Fixed an issue when consuming a SOAP Web Service with HTTP transport binding.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>When consuming a SOAP Web Service, the expected protocol transport element was not being fetched correctly. This happened specifically for the "http://www.w3.org/2003/05/soap/bindings/HTTP/” transport element.</p><p><a id="RPM-1075"><strong>RPM-1075</strong></a><br/><b>Now, using DbCleaner API to delete a multi-tenant entity, event entity, or a multilingual static entity, also deletes the database objects associated with those entities.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>When deleting an entity using the DbCleaner API several database  objects associated with the entity weren't deleted.
This issue occurred in the following cases:
<ul>
<li>Deleting a static entity containing translations, kept the multilingual tables and views.</li>
<li>Deleting an entity containing events, kept the event related tables.</li>
<li>Deleting a multi-tenant entity, kept the tenant views.</li>
</ul>
Now, when deleting these entities, DbCleaner deletes the associated database objects.</p><p><a id="RPM-1093"><strong>RPM-1093</strong></a><br/><b>Fixed data vulnerability due to excessive logging. CVSSv3.1 score 4.4 (Medium).</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Installer</span> <br/><br/><u>Fix Details:</u><br/>Fixed an SSRF vulnerability that could cause information exposure through log files. To protect our customers, we're not providing further details on this fix.</p><p><a id="RPM-1115"><strong>RPM-1115</strong></a><br/><b>Fixed an issue that was blocking the activation/deactivation of Timers in cloned modules.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>When trying to Activate/Deactivate a Timer of a module in the Service Center console, the operation has no effect and the NextRun value remains unchanged, although the feedback message confirms the change. This issue occurred only for modules that were cloned from modules with Timers.</p><p><a id="RPM-1118"><strong>RPM-1118</strong></a><br/><b>Fixed an issue that could cause incorrect code generation for SQL nodes with expand inline parameters in Oracle databases, after upgrading the Platform Server component to 11.12.0 or later.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>When upgrading an environment using an Oracle database to Platform Server 11.12.0 or later, the System Components installation failed with an HTTP NotFound error. After that, when trying to open the Service Center console, you would get ORA-00903 and ORA-00936 errors. Any use of expand inline parameters in SQL nodes would result in application errors. This issue only happened in some specific scenarios.</p><p><a id="RPM-1125"><strong>RPM-1125</strong></a><br/><b>Fixed an issue that could cause modules to have outdated dependencies after a Platform Server upgrade.</b><br/><span class="cattag">Service Studio</span> <span class="cattag">References</span> <br/><br/><u>Fix Details:</u><br/>After upgrading from a Platform Server version prior to 11.10.0 to Platform Server 11.10.0 or later, performing the Apply Settings operation before republishing the applications would cause modules with renamed or deleted Site Properties to be outdated. This issue could cause the application to be unavailable.</p><p><a id="RPM-1177"><strong>RPM-1177</strong></a><br/><b>The Roles screen of the Users application is now correctly listing only the end users having that role.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>In the Users application, when selecting a specific Role to see its details, you should see the list of end-users with that role. Instead, the screen listed all end-users in the environment.</p><p><a id="RPM-1190"><strong>RPM-1190</strong></a><br/><b>Fixed an issue that could cause incorrect code generation for SQL nodes with expand inline parameters in SQL Server databases, after upgrading the Platform Server component to 11.12.0 or later.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>When upgrading an environment using a SQL Server database to Platform Server 11.12.0 or later, the System Components installation failed with an HTTP InternalServerError. After that, when trying to open the Service Center console, you would get query execution errors. Any use of expand inline parameters in SQL nodes would result in application errors. This issue only happened in some specific scenarios.</p><p><a id="RPM-1198"><strong>RPM-1198</strong></a><br/><b>Fixed an error when publishing the System Components solution during the upgrade to Platform Server 11.12.0 or later caused by producer modules not being prepared.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>When upgrading the Platform Server component to version 11.12.0 or later, publishing the System Components fails with the error "Old Producer: Producer module 'EnterpriseManager' hasn't been prepared for the the current OutSystems environment version".
This error occurred only while upgrading environments that were originally created with very early Platform Server versions, having the effective User Provider of the Users module set to the Enterprise Manager deprecated module. As the Enterprise Manager module is not included in the solution anymore, the publishing failed.</p><p><a id="RPM-1260"><strong>RPM-1260</strong></a><br/><b>Fixed an issue that prevented Timers, Emails, and Processes from running after changing the name of the Server.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Processes</span> <br/><br/><u>Fix Details:</u><br/>When changing the name of a registered front-end Server, a new Server record is automatically registered in the Service Center console after restarting the OutSystems Deployment service. This operation was lacking the update of the Timers, Processes, and Emails executed by that Server to reference the new record. This issue has been solved, and all references are now updated to match the new Server record when the Server name changes.</p><p><a id="RPM-1272"><strong>RPM-1272</strong></a><br/><b>Fixed the "Unable to find the specified file" error when publishing the System Components solution during a Platform Server upgrade.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>When publishing the System Components solution during a Platform Server upgrade, the following error is thrown for each module of the solution: "An error occurred in task 'Building Oml with Empty Proxies for espace [module_name]': Unable to find the specified file". This issue would happen because the user associated with the OutSystems Deployment Controller service lacked the permissions to create symbolic links.</p><p><a id="RPM-1296"><strong>RPM-1296</strong></a><br/><b>Fixed an issue that could cause a timeout when publishing the Service Center component through the Configuration Tool using an Oracle database.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>For some specific Oracle versions, the database engine is not choosing the most efficient plan to execute a specific query that runs during the compilation phase when using the default IntrospectionMethod key value defined in the Server.hsconf file. This was causing a timeout when publishing the Service Center component through the Configuration Tool.</p><p><a id="RPM-1325"><strong>RPM-1325</strong></a><br/><b>Fixed an error when publishing the Service Center component during a Platform Server installation or upgrade using an Oracle database. This error occurred only when the user OSADMIN had no permissions to execute the DBMS_RANDOM Oracle package.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>While installing or upgrading the Platform Server in environments using an Oracle database, the publishing of the Service Center component failed with a "Could not create foreign key constraint." error. The issue only occurred in environments where the DBMS_RANDOM Oracle package was removed from the Public user group, resulting in the lack of permissions for the user OSADMIN to execute that package.</p><p><a id="RPM-1374"><strong>RPM-1374</strong></a><br/><b>Fixed the "Error getting publication state" error when publishing the System Components solution during a Platform Server upgrade.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>When upgrading the Platform Server component, publishing the System Components failed with the error "Error getting publication state". This was an issue when the Configuration Tool retrieves information from the Server.API and it's now fixed. </p><p><a id="RPM-1420"><strong>RPM-1420</strong></a><br/><b>Fixed application deployment issues when Dynatrace was enabled in the environment.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Deployment stage</span> <br/><br/><u>Fix Details:</u><br/>The Dynatrace tool injects customized code in some platform internal files, causing the OutSystems Deployment service to fail the integrity check after publishing a module. Having this tool enabled prompted the OutSystems Deployment service into error state and application deployments to fail with the error "Deployment failed: Ping validation failed".</p><p><a id="RPM-1421"><strong>RPM-1421</strong></a><br/><b>Fixed an issue that led to 404 Traditional Web app screens using an SEO Page Rule that started with "rest".</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">SEO Friendly URLs</span> <br/><br/><u>Fix Details:</u><br/>The issue led to a 404 when accessing screens that used an SEO Page Rule.
This issue occurred when using Platform Server version 11.12.1 or later and affected Traditional Web app screens using SEO Page Rule with a URL Pattern that started with "rest".</p><p><a id="RPM-1456"><strong>RPM-1456</strong></a><br/><b>Updated the installation checklist instructions for integration with IBM Db2 databases.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Installation Checklist</span> <br/><br/><u>Fix Details:</u><br/>In environments with integration with IBM Db2 databases, attempting to access the Db2 database after installing the Platform Server resulted in the error “The ConnectionString property is invalid“, with error stack “Unable to load DLL ‘cwbdc.dll’". This happens because IBM i Access for Windows has been replaced by IBM iAccess Client Solutions (ACS), therefore the required file "cwbdc.dll" is not installed anymore when following the previous installation checklist instructions. The checklist was updated to provide the correct instructions for integration with IBM Db2 databases.</p><p><a id="RPM-1522"><strong>RPM-1522</strong></a><br/><b>Fixed the error "ORA-01489: result of string concatenation is too long" when publishing a module with an Action which description exceeds 4000 bytes. This issue occurred only in Oracle databases.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>Starting from Platform Server 11.0.422.0, the Action's description is saved in the database with a limit of 2000 characters, which represents a maximum of 4000 bytes in Oracle databases. This issue occurred when the description of an Action had less than 2000 characters, but more than 4000 bytes, which can happen, for example, for Japanese characters. In this scenario, publishing the module resulted in the error "ORA-01489: result of string concatenation is too long".</p><p><a id="RPM-1526"><strong>RPM-1526</strong></a><br/><b>Fixed an issue that caused third-party components that used click events to not work as expected in PWA Mobile apps.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Interface</span> <br/><br/><u>Fix Details:</u><br/>The issue caused third-party components that used click events to not work as expected.
This occurred in Mobile apps distributed as PWAs.
The issue no longer occurs after the removal of the FastClick.js  from Mobile apps.</p><p><a id="RPM-1561"><strong>RPM-1561</strong></a><br/><b>The Configuration Tool no longer proceeds with the Apply and Exit operation if the Platform Administrator password is empty.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>In environments using Windows Authentication, when you open the Configuration Tool the passwords are empty, which is the expected behavior. However, when clicking the Apply and Exit button, the Configuration Tool would execute the apply operation and attempt to connect with the database. In some cases, the failed login attempt to the database could lock the account.</p><p><a id="RPM-1575"><strong>RPM-1575</strong></a><br/><b>Fixed the Test Connection validation in the Configuration Tool when using Windows Authentication.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>In environments using Windows Authentication, using the Test Connection returned a successful result when using an incorrect password.</p><p><a id="RPM-1584"><strong>RPM-1584</strong></a><br/><b>Fixed a broken access control vulnerability in some buttons of Service Center. CVSSv3.0 score 5.4 (Medium).</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>In the tenant details of a module, the Timers tab was not properly validating the user permissions. It could allow an IT user to run timers without the proper permissions. The permissions are now properly validated.</p><p><a id="RPM-1608"><strong>RPM-1608</strong></a><br/><b>The Platform Server installer no longer installs .Net Core 2.1.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>As of Platform Server 11.12.2, .NET Core 3.1 Runtime &amp; Hosting Bundle for Windows is part of the system requirements, replacing the previously used .NET Core 2.1, which is no longer supported. However, the installer of Platform Server 11.13.0 or later installed both versions. Removing the .NET Core 2.1 from the environment after the Platform Server installation would cause some OutSystems services to fail.</p><p><a id="RPM-1623"><strong>RPM-1623</strong></a><br/><b>Fixed an issue that cause Reactive Web Apps to show a blank screen when opening them through a URL with a hash (#).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Mobile Application Update</span> <br/><br/><u>Fix Details:</u><br/>The issue caused screens to show a blank screen when the screen URL included a hash (#).
This occurred in Reactive Web apps in environments with the SEO-friendly URLs for Reactive Web Apps technical preview enabled.</p><p><a id="RPM-1644"><strong>RPM-1644</strong></a><br/><b>Fixed the "c is not a function" runtime error occurring on some occasions for Reactive Web Apps and Mobile Apps distributed as a PWA after a Platform Server upgrade.</b><br/><span class="cattag">Publish Operation</span> <br/><br/><u>Fix Details:</u><br/>After upgrading from a Platform Server version prior to 11.12.0 to Platform Server 11.12.0 or later, the runtime error "c is not a function" would sometimes occur for Reactive Web Apps and Mobile Apps distributed as a PWA. This issue was related to the Modified Date of the Client Runtime resources, which is <a href="https://github.com/npm/npm/issues/20439"> set by the npm package manager</a> with the same pre-defined date for any client runtime bundle. This was preventing IIS to detect the need to update the cache, serving old client runtime bundles instead.</p><p><a id="RPM-1677"><strong>RPM-1677</strong></a><br/><b>Changes to REST APIs or SOAP Web Services settings executed via Service Center on the module's Integrations tab are now recorded in the General Log.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>There was no logging information in the General Logs when changing the settings of REST APIs or SOAP Web Services via Service Center on the module's Integrations tab. This issue had a low impact on OutSystems Sentry environments, as they include compliant level auditing on request.</p><p><a id="RPM-1684"><strong>RPM-1684</strong></a><br/><b>Link widgets that match the current screen are now correctly added the "active" CSS class.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Interface</span> <br/><br/><u>Fix Details:</u><br/>In Reactive Web and Mobile apps, Link widgets that pointed to the current screen weren't set with the "active" CSS class. For example, this meant that a link in the menu that pointed to the current screen wasn't highlighted.
This issue occurred in environments using Platform Server version 11.12.0 or higher.</p><p><a id="RPM-1804"><strong>RPM-1804</strong></a><br/><b>Fixed a security issue that could allow users to view Application details in Service Center to which they don't have permissions. Only affects environments not connected to LifeTime. CVSSv3.1 score 4.3 (Medium)</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>*Symptoms*

*How to reproduce*</p><p><a id="RPM-1917"><strong>RPM-1917</strong></a><br/><b>Removed the service account that was causing errors during publication of System Components in environments with Active Directory authentication configured.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>The process of installation of System Components fails with HTTP error code 400 due to a misconfiguration of the ConfigurationTool_OperationsSA system account</p><p><a id="RPM-1923"><strong>RPM-1923</strong></a><br/><b>Fixed several missing logs in Service Center (e.g. Error and General logs).</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>On new Oracle installations with 11.14.0.33133 have no logs available in Service Center screens. On upgraded platform versions the log rotations will not work correctly, so only old weeks will be available once the logs rotate.

Request event log tables are not affected by this issue.</p><p><a id="RPM-2022"><strong>RPM-2022</strong></a><br/><b>Fixed issues that occurred when clicking "Apply and Exit" in the Configuration Tool after changing database configurations.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>*Symptoms*
When changing database configuration is Configuration Tool and clicking ‘Apply and Exit’, this results in database or connection string errors. The error stack trace mentions get_NodeAwareSettingInConfigFilesFT() and PlatformSettings.isServiceConfigSetting.

*How to reproduce*
* Change the password of the OutSystems users. It should be enough to change the Administrator and Runtime user passwords.
* Open Configuration Tool, update the password fields with the newly defined passwords and click ‘Apply and Exit’
Configuration Tool should use the new credentials and run without errors, but instead an error similar to mentioned above will be returned.</p><p><a id="RPM-447"><strong>RPM-447</strong></a><br/><b>Fixed multiple cross-site scripting (XSS) vulnerabilities in Popup_Editor, Popup_EditorForUpload, or Popup_EditorVanilla titles. CVSSv3.1 score 3.1 (Low)</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>The titles of the widgets Popup_Editor, Popup_EditorForUpload, and Popup_EditorVanilla were not encoded by default, making them vulnerable to cross-site scripting attacks. The Title property is now encoded however, this may introduce a breaking change. Find more information about this breaking change <a href="https://success.outsystems.com/Support/Archive/11/OutSystems_Platform_side_effects_and_breaking_changes#Introduced_in_Platform_Server_11.14.0">here.</a> </p><p><a id="RPM-478"><strong>RPM-478</strong></a><br/><b>Fixed an issue that caused Entity_DropTable and Attribute_DropColumn actions of DbCleaner API to throw an ORA-00942 error when dropping entities or attributes in modules created in Oracle database schemas other than the main one.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>Fixed an issue that caused an ORA-00942 error to show after dropping entities or attributes using DbCleaner API.
This occurred when using an Oracle platform database and after using Entity_DropTable and Attribute_DropColumn actions with modules created in schemas other than the (Main) schema. Even after the ORA-00942 error, the entities or attributes were dropped.
Now, the error is not shown after successfully dropping the entities or attributes.</p><p><a id="RPM-542"><strong>RPM-542</strong></a><br/><b>Now, it's not possible to delete the active External Authentication Provider plugin.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">LifeTime</span> <br/><br/><u>Fix Details:</u><br/>Fixed an issue that prevented IT users from logging in environments or infrastructures while using a custom External Authentication Provider plugin.
This occurred after deleting the active Authentication Provider plugin, and prevented the activation of the OutSystems Built-In Authentication in LifeTime.
Now, it's not possible to delete the active External Authentication Provider plugin.</p><p><a id="RPM-546"><strong>RPM-546</strong></a><br/><b>Fixed an issue that caused timeout when accessing the solution publish screen when the publish report has a very high number of messages.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>The issue prevented publishing a solution, due to a timeout in the solution publish screen that made it impossible to select 'Continue' button to proceed with the publish.
This issue occurred when publishing large solutions.</p><p><a id="RPM-593"><strong>RPM-593</strong></a><br/><b>Fixed the error message returned when publishing a module after trying to modify the length of a Text Id attribute of an Entity.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Compilation</span> <br/><br/><u>Fix Details:</u><br/>The attempt of modifying the length of an Entity's Id attribute with Text data type can result in errors due to limitations on the database engine side. In those scenarios, the error message returned by the platform when publishing the module could be misleading and sometimes incorrect.</p><p><a id="RPM-714"><strong>RPM-714</strong></a><br/><b>Fixed an issue blocking the external authentication of IT users using then AD authentication provider when using multiple deployment zones and not having the System Components deployed in the Default zone. Improved also the error message shown in this scenario.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>In an environment with multiple deployment zones where the System Components are not deployed in the Default zone, activating the AD authentication provider (ADAuthProvider) would result in the following error: "Test failed: Module must be available for all front ends (in global zone)". This issue prevented the activation of AD authentication for IT users. Also, the error message was misleading.</p><p><a id="RPM-741"><strong>RPM-741</strong></a><br/><b>As a security improvement, extensions are no longer automatically recompiled on upgrade.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Application Server</span> <br/><br/><u>Fix Details:</u><br/>Compilation during extension upgrades allows arbitrary code to be executed remotely in the server.

This vulnerability has been classified as Critical with a cvss score of 9.1</p><p><a id="RPM-747"><strong>RPM-747</strong></a><br/><b>Fixed a security vulnerability on an internal Service Center API permission requirement. CVSSv3.1 score 6.3 (Medium).</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>Service Center APIs used by Service Studio to create and delete apps would allow deleting system modules when they shouldn't. Deleting system modules can impact a running environment, ultimately causing misbehaviors or unavailability. The internal APIs were hardened and no longer allow deleting system modules.</p><p><a id="RPM-754"><strong>RPM-754</strong></a><br/><b>Fixed an issue that prevented DbCleaner API to delete attributes of multitenant database views.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Public APIs</span> <br/><br/><u>Fix Details:</u><br/>Using the Attribute_DropColumn of DbCleaner API to delete an attribute of a multitenant entity would return the error: "Error executing query. View or function has more column names specified".  The DbCleaner API now properly deletes the attribute.</p><p><a id="RPM-768"><strong>RPM-768</strong></a><br/><b>The actions Entity_DropTable and Attribute_DropColumn from DbCleaner API now have a success output indicating if the drop operation was performed or not.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>In the scenario of active columns and entities, the actions Entity_DropTable and Attribute_DropColumn from DbCleaner API don't perform the drop operation. However, no feedback was being returned about the effectiveness of the operation.</p><p><a id="RPM-939"><strong>RPM-939</strong></a><br/><b>Fixed an issue that was causing Service Center to throw an error when exporting to excel the Screen Requests logs filtered by Application.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>When trying to Export to excel the Screen Requests logs from the Service Center, if the logs were filtered by any Application, the following error would be thrown: "There was an error while exporting data. Redefine log filters to retrieve less data and try again."</p><p><a id="RPM-945"><strong>RPM-945</strong></a><br/><b>Fixed an issue that could cause modules to have outdated dependencies after a Platform Server upgrade.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Data Access and Manipulation</span> <br/><br/><u>Fix Details:</u><br/>After upgrading from a Platform Server version prior to 11.10.0 to Platform Server 11.10.0 or later, performing the Apply Settings operation before republishing the applications would cause modules with renamed or deleted Site Properties to be outdated. This issue could cause the application to be unavailable.</p><p><a id="RPM-952"><strong>RPM-952</strong></a><br/><b>Fixed an issue that occurred in Reactive Web apps and that prevented clearing an invalid value from a Text, Phone, or Email variable.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Interface</span> <br/><br/><u>Fix Details:</u><br/>The issue prevented clearing the value of a Text, Phone, or Email  variable in Reactive Web apps.
This occurred if the value was invalid with Form.Valid runtime property set to False.</p><p><a id="RPM-966"><strong>RPM-966</strong></a><br/><b>Fixed a security issue that could lead to session fixation problems. CVSSv3.1 score 5.4 (Medium).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Authentication and Authorization</span> <br/><br/><u>Fix Details:</u><br/>In certain situations there is session fixation validations made on recent logins.</p><p><a id="RPM-977"><strong>RPM-977</strong></a><br/><b>Fixed the warning "Resource Not Versioned" when deploying Reactive Web Apps.</b><br/><span class="cattag">Publish Operation</span> <span class="cattag">Deployment stage</span> <br/><br/><u>Fix Details:</u><br/>When deploying Reactive Web Apps, the staging report included the following warning for some Reactive Web modules: "Resource Not Versioned: The resource [resource_file] of the producer module [module_name] was not found in the application cache. Please republish [module_name] to prevent runtime errors". This issue had no impact on the running applications.</p>
</div>
<h2 id="Platform_Server_11.13.2">Platform Server 11.13.2</h2>
<div class="info"><p>Released on Oct 18, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2"><span id="New_in_Platform_Server_11.13.2"></span><h3 id="New_in_Platform_Server_11.13.2">New in Platform Server 11.13.2</h3>
<ul>
<li>Flexible Upgrades is now available for Platform installations running over Oracle. (R11PIT-315)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2"><span id="Bug_Fixing_4"></span><h3 id="Bug_Fixing_3">Bug Fixing</h3>
<ul>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1066" rel="custom">Fixed an issue in the Users application preventing end-users from logging in when using standard LDAP authentication. (RPM-1066)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1078" rel="custom">Fixed an upgrade schema error when clicking "Create/Upgrade Database" in the Configuration Tool while upgrading the Platform Server from version 10 to version 11.11.1 or later. This issue applies only to self-managed environments. (RPM-1078)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1128" rel="custom">Improved the performance of the modules preparation phase executed during the upgrade process. (RPM-1128)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1278" rel="custom">Fixed a high severity vulnerability by upgrading the packaged RabbitMQ to 3.8.21. (RPM-1278)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1434" rel="custom">Fixed an issue that caused the incorrect calculation of the average time in Service Actions Performance report. (RPM-1434)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1466" rel="custom">Fixed a malformed login URL for SAML 2.0 when using an external IdP with SSO login URL containing query parameters. (RPM-1466)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1487" rel="custom">Fixed an issue that occurred when clicking "Apply and Exit" in the Configuration Tool after changing the Platform, Log, or Session database configurations. (RPM-1487)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1502" rel="custom">Fixed an issue that might cause the Configuration Tool to lock the Administrator or Runtime Active Directory accounts when using Windows Authentication. (RPM-1502)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1509" rel="custom">Fixed a licensing query that would generate "Licensing error" entries in Service Center Error logs. (RPM-1509)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-1537" rel="custom">Fixed an issue where the Configuration Tool UI was not disabling Log and Session database credential fields when using Windows Authentication. (RPM-1537)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2#RPM-912" rel="custom">Fixed a compilation issue when consuming a SOAP Web Service containing a type and a subtype with the same name. (RPM-912)</a></li>
</ul>
<style>/*<![CDATA[*/.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}/*]]>*/</style><div class="moreDetailsDiv"><div class="mt-section" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.2"><span id="More_details_4"></span><h3 id="More_details_3">More details</h3><p><a id="RPM-1066"><strong>RPM-1066</strong></a><br/><b>Fixed an issue in the Users application preventing end-users from logging in when using standard LDAP authentication.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>End users configured with standard LDAP authentication were not able to log in due to an "Invalid username or password" error.
This was an error in Users application related to the encrypt/decrypt password algorithm. The issue was found in version 11.7.3 and it's now fixed.</p><p><a id="RPM-1078"><strong>RPM-1078</strong></a><br/><b>Fixed an upgrade schema error when clicking "Create/Upgrade Database" in the Configuration Tool while upgrading the Platform Server from version 10 to version 11.11.1 or later. This issue applies only to self-managed environments.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>While upgrading the Platform Server component in a self-managed environment from version 10 to version 11.11.1 or later, clicking the "Create/Upgrade Database" button in the Configuration Tool caused the upgrade schema error "Unable to obtain the connection string". Besides blocking the upgrade process, this issue didn't cause downtime or loss of service.</p><p><a id="RPM-1128"><strong>RPM-1128</strong></a><br/><b>Improved the performance of the modules preparation phase executed during the upgrade process.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>The <a href="https://success.outsystems.com/Support/Enterprise_Customers/Upgrading/Modules_preparation_step_during_Platform_Server_upgrade" rel="internal">module preparation phase</a> after a Platform Server upgrade could take a long time to complete, increasing the time a development team would have to go without being able to publish any modules. This is especially noticeable in large factories and it would only occur in Platform Server 11.12.0 or later.
The module preparation was improved to be more performant.</p><p><a id="RPM-1278"><strong>RPM-1278</strong></a><br/><b>Fixed a high severity vulnerability by upgrading the packaged RabbitMQ to 3.8.21.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>All versions of RabbitMQ prior to 3.8.16 are prone to a denial of service vulnerability.  The packaged RabbitMQ was upgraded. You can check more details in this <a href="https://success.outsystems.com/Support/Security/Vulnerabilities/Vulnerability_RPM-1278" rel="internal">security bulletin.</a></p><p><a id="RPM-1434"><strong>RPM-1434</strong></a><br/><b>Fixed an issue that caused the incorrect calculation of the average time in Service Actions Performance report.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>The Service Actions Performance report in Service Center showed incorrect values for  "Avg. Time". 
When generating or exporting a Service Actions Performance report from the Analytics tabs of Service Center, the report showed the same value for both "Avg. Time" and "Total Time" columns.</p><p><a id="RPM-1466"><strong>RPM-1466</strong></a><br/><b>Fixed a malformed login URL for SAML 2.0 when using an external IdP with SSO login URL containing query parameters.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Authentication and Authorization</span> <br/><br/><u>Fix Details:</u><br/>After setting up SAML 2.0 in Users, app end users that try to log in get redirected to the User app with a permission denied message.
The issue occurred due to a malformed login URL when using SAML 2.0 with a Single Sign-On URL that contained a query parameter.</p><p><a id="RPM-1487"><strong>RPM-1487</strong></a><br/><b>Fixed an issue that occurred when clicking "Apply and Exit" in the Configuration Tool after changing the Platform, Log, or Session database configurations.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>Configuration Tool was not respecting alterations to the databases connection details (Platform, Log, and Session). Changes done in the Configuration Tool UI were not effectively saved. Upon clicking "Apply an Exit", older values (for example: database address, authentication mode and credentials) would be used, ultimately causing connection errors or operations to be attempted with the old values.
The issue was fixed, and values changed in the UI are now fully respected.</p><p><a id="RPM-1502"><strong>RPM-1502</strong></a><br/><b>Fixed an issue that might cause the Configuration Tool to lock the Administrator or Runtime Active Directory accounts when using Windows Authentication.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>When using Windows Authentication, opening the Configuration Tool could lock the Administrator or Runtime user accounts in the Active Directory. This would happen under a strict security policy to lock user accounts on first failed login attempt.
This issue occurred because the Configuration Tool was attempting to login to the database with the Administrator and Runtime users as soon as the UI is opened, which doesn't apply to Windows Authentication.</p><p><a id="RPM-1509"><strong>RPM-1509</strong></a><br/><b>Fixed a licensing query that would generate "Licensing error" entries in Service Center Error logs.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Licensing Runtime Checks</span> <br/><br/><u>Fix Details:</u><br/>In Service Center error logs, an entry with the message: "Licensing Error: An error occurred while validating feature 'InternalExternalUsersCounter': ORA-00972" would happen frequently. Appart from log polution, there was no futher impact. It would happen only when all of the following conditions are true:
</p><ul><li>the Platform Server version is 11.11.3 or later</li>
<li>the platform database is Oracle 12.1c</li>
<li>the license was purchased after January 2020</li></ul>
<br/>
The issue was fixed in an OutSystems internal query to no longer result in such an error.<p><a id="RPM-1537"><strong>RPM-1537</strong></a><br/><b>Fixed an issue where the Configuration Tool UI was not disabling Log and Session database credential fields when using Windows Authentication.</b><br/><span class="cattag">Infrastructure Management</span> <span class="cattag">Platform Configuration</span> <br/><br/><u>Fix Details:</u><br/>In the Configuration Tool, when authentication is set to Windows Authentication on the Platform tab, login errors could occur.

The Administrator, Runtime, and Session credential fields in the Log and Session tabs should be disabled. The issue would cause the fields to be editable. This would force the user to fill in those fields, and, when the credentials didn't match, would cause a login error.</p><p><a id="RPM-912"><strong>RPM-912</strong></a><br/><b>Fixed a compilation issue when consuming a SOAP Web Service containing a type and a subtype with the same name.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>A compilation error occurred after publishing a module which consumed a SOAP Web Service with polymorphism.
This only occurred when one of the possible subtypes declares an anonymous type with the name as the subtype.</p>
</div></div></div><span id="Platform_Server_11.13.1"></span><h2 id="Platform_Server_11.13.1">Platform Server 11.13.1</h2><br/><div class="mt-include" id="s35640">
<div class="os-note os-info style-wrap"><p>Released on Sep 22, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1"><span id="New_in_Platform_Server_11.13.1"></span><h3 id="New_in_Platform_Server_11.13.1">New in Platform Server 11.13.1</h3>
<ul>
<li>We improved the UI and overall user experience of the Preview in Devices. We also added support for a modern variety of devices. (ROU-2177)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1"><span id="Bug_Fixing_5"></span><h3 id="Bug_Fixing_4">Bug Fixing</h3>
<ul>
<li>The Modules screen in Service Center now displays the correct modules list when filtering by Status "with errors and warnings". (R11CT-121)</li>
<li>Fixed the deployment error "Module [module name] is not available for deployment". (R11PBT-176)</li>
<li>Fixed an issue that could cause an error in the logs during publish and prevent correct disk cleanup, while having another ongoing publish of a module with missing references. (R11PBT-177)</li>
<li>Fixed an issue in the Deployment Service that was causing incorrect log information of the modules to be undeployed/deleted from a frontend. (R11PIT-250)</li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-1172" rel="custom">Fixed an issue that caused the logs of mobile apps to have an incorrect timestamp. (RPM-1172)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-1265" rel="custom">Fixed an issue that sometimes caused the Environment Information not to be filled in the Service Center error logs. (RPM-1265)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-1308" rel="custom">Fixed an issue in PWA applications where splash screens would hang on iOS 14.6 devices. (RPM-1308)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-1352" rel="custom">Fixed broken references errors to indirect producers after an upgrade to Platform Server 11.12.1 or higher. (RPM-1352)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-1371" rel="custom">Fixed an issue that caused navigations to the previous screen to go back more screens than it should. (RPM-1371)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-599" rel="custom">Fixed an issue that caused disabled Scheduler services to pick up events and email tasks that they would not process. This also caused a permanent warning displayed on the monitoring pages. (RPM-599)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-921" rel="custom">Fixed an issue that was preventing developers from using the Distribute tab in Service Studio. The issue would only manifest when Active Directory authentication was enabled for IT users. (RPM-921)</a></li>
</ul>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-1098" rel="custom">Fixed a server-side request forgery (SSRF) vulnerability on custom handlers. CVSSv3.1 score 6.5 (Medium). (RPM-1098)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-728" rel="custom">Fixed an integrated authentication vulnerability in OutSystem Cloud environments. CVSSv3.1 score 5.5 (Medium). (RPM-728)</a></li>
<li><a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1#RPM-997" rel="custom">Fixed multiple security risks on the documentation of a REST API by raising the handlebars.js used in the swagger UI. CVSSv3.1 score 6.5 (Medium). (RPM-997)</a></li>
<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style><div class="moreDetailsDiv"><div class="mt-section" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.1"><span id="More_details_5"></span><h3 id="More_details_4">More details</h3><p><a id="RPM-1098"><strong>RPM-1098</strong></a><br/><b>Fixed a server-side request forgery (SSRF) vulnerability on custom handlers. CVSSv3.1 score 6.5 (Medium).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Data Access and Manipulation</span> <br/><br/><u>Fix Details:</u><br/>To protect our customers we're not providing further details on the issue.</p><p><a id="RPM-1172"><strong>RPM-1172</strong></a><br/><b>Fixed an issue that caused the logs of mobile apps to have an incorrect timestamp.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logging</span> <br/><br/><u>Fix Details:</u><br/>The logs related to mobile apps, as shown in Service Center, were sometimes presenting a  timestamp that was deviated from the actual time the event occurred. This could cause the events on the logs not to reflect the order in which they actually occurred, making it harder to understand the logs and troubleshoot a mobile app.
The behavior was fixed and the timestamp of the logs now reflects the exact time of the event.</p><p><a id="RPM-1265"><strong>RPM-1265</strong></a><br/><b>Fixed an issue that sometimes caused the Environment Information not to be filled in the Service Center error logs.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logging</span> <br/><br/><u>Fix Details:</u><br/>The issue would sometimes manifest when the device running the mobile app was offline and an error occurred. When the device comes online, the information is sent to the server to log. The log was written, however, the Environment Information field as seen in the error log detail didn't contain any data.
Such information is useful to provide the runtime context in which the error occurred.
This issue didn't cause any impact on the mobile app's normal usage nor on the end-user experience.</p><p><a id="RPM-1308"><strong>RPM-1308</strong></a><br/><b>Fixed an issue in PWA applications where splash screens would hang on iOS 14.6 devices.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Application Distribution</span> <br/><br/><u>Fix Details:</u><br/>According to <a class="link-https" href="https://www.theregister.com/2021/06/16/apple_safari_indexeddb_bug/" rel="external noopener nofollow" target="_blank" title="https://www.theregister.com/2021/06/16/apple_safari_indexeddb_bug/">https://www.theregister.com/2021/06/...indexeddb_bug/</a>  Apple's WebKit team has managed to break the popular IndexedDB JavaScript API in the latest version of Safari (14.1.1) on macOS 11.4 and iOS 14.6.</p><p><a id="RPM-1352"><strong>RPM-1352</strong></a><br/><b>Fixed broken references errors to indirect producers after an upgrade to Platform Server 11.12.1 or higher.</b><br/><span class="cattag">Publish Operation</span> <br/><br/><u>Fix Details:</u><br/>After upgrading to 11.12.1 and publishing a module, runtime errors due to incompatible definitions might occur.
The issue would occur when a consumer module A is using a producer module B and that producer, in turn, has a producer C that references an extension E. In that case, module A would have errors about incompatibility with an Action from extension E.</p><p><a id="RPM-1371"><strong>RPM-1371</strong></a><br/><b>Fixed an issue that caused navigations to the previous screen to go back more screens than it should.</b><br/><span class="cattag">Application Runtime</span> <br/><br/><u>Fix Details:</u><br/>On a Mobile or Reactive Web app, a screen that has a link that navigates to the previous screen would go instead to the screen before that. Effectively the navigation would send users to 2 screens before the screen they were on. More specifically, the wrong previous screen navigation occurs only after a navigation is performed on an OnInitialize event of a screen.
The issue happens only with applications compiled on Platform Server version 11.12.0 or higher. It may happen on previous Platform Server versions, if the environment had the React 16 Technical Preview feature activated.

The issue was fixed in this version and the wrong redirect will no longer occur.</p><p><a id="RPM-599"><strong>RPM-599</strong></a><br/><b>Fixed an issue that caused disabled Scheduler services to pick up events and email tasks that they would not process. This also caused a permanent warning displayed on the monitoring pages.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Service Center</span> <br/><br/><u>Fix Details:</u><br/>When configuring the servers it is possible to disable BPT processing for specific servers. This issue caused some events to be picked up during the disabled schedulers startup but never processed.
The issue does not exist if all servers are allowed to execute BPT.</p><p><a id="RPM-728"><strong>RPM-728</strong></a><br/><b>Fixed an integrated authentication vulnerability in OutSystem Cloud environments. CVSSv3.1 score 5.5 (Medium).</b><br/><span class="cattag">Cloud Paas</span> <br/><br/><u>Fix Details:</u><br/>Fixed a vulnerability that would allow, in the OutSystems Cloud, users with access to the underlying infrastructure to be able to access applications developed in the environment.
The vulnerability was fixed so that it no longer allows privileged users with infrastructure access to log in to applications.</p><p><a id="RPM-921"><strong>RPM-921</strong></a><br/><b>Fixed an issue that was preventing developers from using the Distribute tab in Service Studio. The issue would only manifest when Active Directory authentication was enabled for IT users.</b><br/><span class="cattag">Service Studio</span> <span class="cattag">Distribute</span> <br/><br/><u>Fix Details:</u><br/>For Mobile apps, accessing Distribute tab in Service Studio in an environment with Active Directory enabled for IT users, would result in an "Invalid user credentials" error, even if the credentials were correct. The issue would occur with a combination of a Platform Server version higher than 11.10.2 and Service Studio version 11.10.06 or higher.</p><p><a id="RPM-997"><strong>RPM-997</strong></a><br/><b>Fixed multiple security risks on the documentation of a REST API by raising the handlebars.js used in the swagger UI. CVSSv3.1 score 6.5 (Medium).</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>The auto-generated documentation of a REST API was using an outdated version of handlebars.js that has known vulnerabilities. Security tests would flag this. The handlebars.js version was raised to an updated version.</p>
</div></div></div></div>
<h2 id="Platform_Server_11.13.0">Platform Server 11.13.0</h2>
<div class="info"><p>Released on Aug 09, 2021</p></div>
<h3 id="New_in_Platform_Server_11.13.0">New in Platform Server 11.13.0</h3>
<ul>
<li>We improved the experience of the "SEO-friendly URLs for Reactive Web Apps" technical preview. The platform now shows a compilation error when ISAPI Filter, one of the prerequisites, is missing from the installation. (RTAFB-4270)</li>
<li>New features in emails for Mobile and Reactive Web Apps. Attach files to emails. In addition to the existing widgets, design content with Table, List, and If. The Image widget now supports adding binary content from the database. To use the new widgets, update Platform Server and keep "Emails for Mobile and Reactive" on. To add attachments, update Platform Server and turn on "Attachments in Mobile and Reactive emails".  (RTAFB-4602)</li>
<li>You can now use expressions to set titles of Screens. This lets you change the page title dynamically, and set unique values that show in the browser tabs, bookmarks, and results from the search engines. When using this feature, it is recomended that all developers in the same organization update Service Studio. (RTAFB-4738)</li>
</ul>
<h3 id="Bug_Fixing_5">Bug Fixing</h3>
<ul>
<li>The Basic Authentication option of REST Integrations is now correctly removed after the user clears the credentials in Service Center. (R11CT-115)</li>
<li>Fixed an issue in the OutSystemsReactWidgets.css file that prevented the loading of Font Awesome. (R11DT-363)</li>
<li>Fixed an issue in the "apply permissions" step during installation or upgrade. This issue could cause that step to take longer than needed or fail if some conditions were not met, leaving the system in an inconsistent state. (R11PBT-158)</li>
<li>Fixed an issue causing the modules of a Solution to be incorrectly locked with a "Locked Module" error after the Solution publishing aborted abruptly (for example, due to a restart of the Service Center application pool or lack of database space). (R11PIT-240)</li>
<li>Fixed an issue where using Filters over Calculated Attributes on Local Storage Aggregates in PWAs could cause the query to return no results.  (RAR-677)</li>
<li>Fixed an issue that could cause the log file downloaded from the Integration Detail screen in Service Center to be empty. (RPD-3909)</li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-1038" rel="custom">Fixed an issue that was causing headers not to be applied correctly in applications. (RPM-1038)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-1052" rel="custom"> Fixed an issue with SEO Friendly Urls, that caused a 404 when the module alias had the same name as the module. (RPM-1052)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-1245" rel="custom">Fixed an issue that caused the login action to take a long time in Traditional Web apps using SAML 2.0 authentication when the user has many active sessions. (RPM-1245)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-341" rel="custom"> Fixed an issue with SEO Friendly Urls, that caused a 404 when the module alias had the same name as the module. (RPM-341)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-365" rel="custom">Fixed an issue that caused the join between the system tables Sent_Email and Email_Status not to retrieve any results. (RPM-365)</a></li>
<li>Fixed an issue that caused a timeout when executing the Timer BPT_CleanUp. (RPM-436)</li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-638" rel="custom">Fixed an issue in the Security exceptions of Mobile apps that caused incorrect exception handling. (RPM-638)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-905" rel="custom">Fixed the client-side exception mechanism so it properly manages handlers from the parent exception.  (RPM-905)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-954" rel="custom">Fixed an issue that prevented end users from closing Popover Menu used inside a Tabs OutSystems UI pattern. (RPM-954)</a></li>
<li><a href="/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-972" rel="custom">Fixed an issue where scrolling doesn't work in Popover Menu widget when it's opened inside a Tabs pattern. (RPM-972)</a></li>
<li>Fixed an issue terminating a Process instance when some Activities are still being executed but those Activities no longer exist in the Process definition (for example, they were deleted or moved to another module). In those cases, an error is now logged regarding the missing Activities definition and it's possible to terminate the Process instance. (RRCT-3784)</li>
<li>Fixed a runtime error that showed with "SEO-friendly URLs for Reactive Web Apps" tech preview on in apps that didn't use any site rules. (RTAFB-4577)</li>
<li>Fixed "Collection was modified; enumeration operation may not execute" that occurred after adding an Email to module and trying to publish. This bug is related to the technical preview "Emails for Mobile and Reactive". (RTAFB-4654)</li>
<li>Fixed the error "Error creating Email. Execution Timeout Expired" in Personal Environments, related to the technical preview "Emails for Mobile and Reactive". (RTAFB-4709)</li>
<li>Fixed the prioritization of the custom URLs. A page with the static custom URL is now shown to users when the URL is partially similar to the URL of another page with a custom parameterized URL. (RTAFB-4717)</li>
<li>Fixed a compilation crash when some Screens have custom URLs and others don't. (RTAFB-4798)</li>
</ul>
<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style><div class="moreDetailsDiv"><h3 id="More_details_5">More details</h3><p><a id="RPM-1038"><strong>RPM-1038</strong></a><br/><b>Fixed an issue that was causing headers not to be applied correctly in applications.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">System Components</span> <br/><br/><u>Fix Details:</u><br/>Headers added using the AddHeader action of <a href="https://success.outsystems.com/Documentation/11_x_platform/Reference/OutSystems_APIs/HTTPRequestHandler_API">HTTPRequestHandler</a> weren't being applied to the applications. The symptoms may vary according to the type of header that was added. 
The issue can happen from Platform Server version 11.9.0 onwards and was fixed in this version to restore the proper behavior, adding the defined headers.</p><p><a id="RPM-1052"><strong>RPM-1052</strong></a><br/><b> Fixed an issue with SEO Friendly Urls, that caused a 404 when the module alias had the same name as the module.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">SEO Friendly URLs</span> <br/><br/><u>Fix Details:</u><br/>The issue occurs in modules that have the same name as the module alias. This created 2 entries in the database table every time you publish, overflowing, in the long run, the 10000 lines DB table limit.
To prevent this issue, the DB table limit was increased above the 10000 lines, and there's an automatic cleanup on duplicated entries.</p><p><a id="RPM-1245"><strong>RPM-1245</strong></a><br/><b>Fixed an issue that caused the login action to take a long time in Traditional Web apps using SAML 2.0 authentication when the user has many active sessions.</b><br/><span class="cattag">Application Lifecycle</span> <span class="cattag">Users</span> <br/><br/><u>Fix Details:</u><br/>When using SAML 2.0 authentication in Traditional Web apps, the action of logging in is taking a very long time. This happens for very active users with hundreds of active sessions, most typically, users used for testing or automation. 
The issue resides in the RegisterUserSession action that's not performant in this edge case. This action was improved so that's no longer subject to performance degradation.</p><p><a id="RPM-341"><strong>RPM-341</strong></a><br/><b> Fixed an issue with SEO Friendly Urls, that caused a 404 when the module alias had the same name as the module.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">SEO Friendly URLs</span> <br/><br/><u>Fix Details:</u><br/>This issue has the same cause as <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server/Platform_Server_11.13.0#RPM-1052">RPM-1052</a>. Refer to it to understand the impacts and changes.</p><p><a id="RPM-365"><strong>RPM-365</strong></a><br/><b>Fixed an issue that caused the join between the system tables Sent_Email and Email_Status not to retrieve any results.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logging</span> <br/><br/><u>Fix Details:</u><br/>This issue caused a join between the system tables Sent_Email and Email_Status not to retrieve any results. This has no impact on the OutSystems capability to send emails, but if you're using the <a href="https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/Emails_API">Emails API</a> in your logic, your application can be affected. The fix restored the proper behavior and the results of that join are now correctly retrieved.</p><p><a id="RPM-638"><strong>RPM-638</strong></a><br/><b>Fixed an issue in the Security exceptions of Mobile apps that caused incorrect exception handling.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>The issue resided in the "Invalid Login" and "Not Registered" exceptions of Mobile apps that were not caught by their parent handler, <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Implement_Application_Logic/Handle_Exceptions">Security exception</a>. Instead, they were bubbling up to "All exceptions", ultimately causing the wrong exception message to appear to the end-user.</p><p><a id="RPM-905"><strong>RPM-905</strong></a><br/><b>Fixed the client-side exception mechanism so it properly manages handlers from the parent exception. </b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Logic Execution</span> <br/><br/><u>Fix Details:</u><br/>In Reactive Web or Mobile apps, user exceptions were not properly following the <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Implement_Application_Logic/Handle_Exceptions">hierarchy of exceptions</a>. Any "parent node" exception, such as User Exception, should be able to handle any "children node" exception, for example, UserException1. Due to this issue, a UserException1 on client-side logic was not being handled by the User Exception parent node, and instead, it was bubbling up to AllExceptions, ultimately causing the wrong exception message to appear to the end-user. In fixing this bug the other exceptions subgroups (Database, Security, Communication, and Abort Activity Change) are now handled as expected.</p><p><a id="RPM-954"><strong>RPM-954</strong></a><br/><b>Fixed an issue that prevented end users from closing Popover Menu used inside a Tabs OutSystems UI pattern.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Interface</span> <br/><br/><u>Fix Details:</u><br/>In Mobile apps, end users couldn't close a Popover Menu by selecting an area outside the popover menu.
This occurred with Popover Menu widgets used inside the Tabs OutSystems UI pattern, except for Popover Menus in the first tab.</p><p><a id="RPM-972"><strong>RPM-972</strong></a><br/><b>Fixed an issue where scrolling doesn't work in Popover Menu widget when it's opened inside a Tabs pattern.</b><br/><span class="cattag">Application Runtime</span> <span class="cattag">Supported Forge Component</span> <br/><br/><u>Fix Details:</u><br/>When a Popover Menu widget is used inside a Tabs pattern, the end-user wasn't able to scroll the page if the Popover was opened. The issue would occur with previous Platform Server versions and OutSystems UI version 2.5.8 or higher.
The issue was fixed and it's now possible to scroll properly using any OutSystems UI version.</p>
</div>
<span id="Platform_Server_11.12.2"></span><h2 id="Platform_Server_11.12.2">Platform Server 11.12.2</h2><br/><div class="mt-include" id="s33530">
<div class="info"><p>Released on Jul 13, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.12.2"><span id="Bug_Fixing_7"></span><h3 id="Bug_Fixing_6">Bug Fixing</h3>
<ul>
<li>Fixed an issue where linking to a screen with a custom URL defined caused a crash if mandatory inputs were empty or invalid.  (RAR-782)</li>
<li>Fixed an issue on progressive web apps (PWAs) where data from an aggregate populated by local storage did not display. This issue occurred when a consuming module used a different entity name than the producer module. (RPM-896)</li>
<li>Raised the required Microsoft .NET Core Windows Server Hosting from 2.1 to 3.1. The checklist and documentation instruction links have been updated to reflect this. (RPM-1105)</li>
<li>Fixed an issue with Multilingual Locales that caused the following error message to display: "Problem fetching the current Locale. The returned Locale is either null or undefined." (RPM-1161)</li>
<li>For a REST Expose Action, the swagger.json file now correctly reflects the "Name in Response" value when you specify that the output parameter must 
be sent in the header. Previously, the "Name in Response" was ignored when specified for the output parameter.  (RPM-1181)</li>
<li>Fixed an issue that removed page rules of Traditional Web applications when they were republished. (RPM-1324)</li>
<li>Fixed a performance issue with compiling modules. The fix reduces the number of database queries required when computing server-to-client data transfer optimization. (RTAF-4754)</li>
<li>Fixed a performance issue with SQL Server by eliminating unnecessary executions of the SERVERPROPERTY function. (RPLAT-650)</li>
<li>Fixed a SSRF security vulnerability on RestDevService. CVSSv3.1 score 4.3 (Medium). (RPM-996)</li>
<li>Fixed a SSRF security vulnerability on SoapDevService. CVSSv3.1 score 6.5 (Medium). (RPM-998)</li>
</ul>
</div></div><span id="Platform_Server_11.12.1"></span><h2 id="Platform_Server_11.12.1">Platform Server 11.12.1</h2><br/><div class="mt-include" id="s33088">
<div class="info"><p>Released on Jun 21, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.12.1"><span id="Bug_Fixing_8"></span><h3 id="Bug_Fixing_7">Bug Fixing</h3>
<ul>
<li>When browsing application edit screens, Service Center no longer redirects you to the home page after a period of inactivity. (R11PIT-177)</li>
<li>Fixed an issue where it was not possible to send an e-mail using an SMTP provider that sends a non-supported command to authenticate. (RPM-1063)</li>
<li>Fixed an issue that removed page rules of Traditional Web applications when they were republished. (RPM-1324)</li>
<li>Fixed an issue causing unnecessary connections to the database. This fix prevents a performance impact in environments with SQL Server or Azure SQL Database. (RPM-993)</li>
<li>We fixed an error in Reactive Web Apps, in environments with the technical preview "SEO-friendly URLs for
Reactive Web Apps". An error occurred when users accessed Screens that contain a Custom URL and an empty 
Page Name value or a Screen Name value equal to the Page Name value. This naming limitation no longer exists. (RTAF-4618)</li>
<li>We fixed an issue causing 404 errors in Reactive Web Apps. Screens configured with path parameters had 404 
errors after upgrading an application.  (RTAF-4646)</li>
<li>Fixed an issue where application runtime errors could occur under high concurrency conditions. This occurred with Static Entities defined in Libraries or when modules referenced Static Entities defined in Libraries. (RPLAT-751)</li>
</ul></div></div>

<h2 id="Platform_Server_11.12.0">Platform Server 11.12.0</h2>
<div class="info"><p>Released on May 24, 2021</p></div>
<h3 id="New_in_Platform_Server_11.12.0">New in Platform Server 11.12.0</h3>
<ul>
<li>You can now Expose REST webservices using the PATCH verb. This capability is a technical preview feature and you need to activate the option "PATCH method in exposed REST APIs" in LifeTime. (R11DT-89)</li>
<li>It is no longer possible to concurrently publish the same modules in Solutions and individually. Modules in Solutions remain locked for the duration of the Solution publish. (R11PIT-176)</li>
<li>Upgraded to React 16. The platform runtime in Platform Server 11.12.0 and later uses the upgraded version of React, React 16. Although we’ve been testing this with help of multiple customers in multiple scenarios, we know that on rare occasions this upgrade may break some JavaScript extensibility code not compliant with React 16 so we recommend you fully test your Web Reactive and Mobile applications after the upgrade. This upgrade may also break the following components, so make sure you update to the latest versions from Forge: Multilingual Component, Input Masks Library, Input Masks Mobile. (RAR-174)</li>
<li>We improved the accessibility of the Table. The Table widget now has the following ARIA attributes: role="grid" and aria-rowcount. The cells in the Table have aria-colindex and aria-rowindex, while the header cell has aria-sort. (RAR-316)</li>
<li>We improved the Button Group widget accessibility by adding the following ARIA attributes: role="radiogroup", aria-activedescendant, role="radio", and aria-checked (if required by the item state). (RAR-319)</li>
<li>Improved the performance of Aggregates in PWAs when you use Join Conditions or Filters with more than one comparison. (RAR-381)</li>
<li>We improved the Radio Group widget accessibility by adding the following ARIA attributes: role="radiogroup", aria-activedescendant, role="radio", and aria-checked (if required by the item state). (RAR-433)</li>
<li>Native build now uses timeout returned by MABS instead of predefined value. (RLIT-4329)</li>
<li>With OutSystems Now being deprecated, the WebScreenClientExecuted event from PerformanceMonitoring API no longer retrieves properties related to applications running on mobile devices (DMan, Dmod, Dplat, DPlatV, NT, CN, CCC, CNT). (RLIT-4405)</li>
<li>When distributing an Android application using MABS 7, it is now possible to choose an Android App Bundle build type to generate an .aab file to upload to the Play store. (RNMT-4579) (RNMT-4579)</li>
<li>Redesigned the download page for mobile applications generated by MABS. (RNMT-4615)</li>
<li>Added support for SQL Server 2019 and compatibility level 150. This applies to the platform database, as well as external databases. (RPLAT-418)</li>
<li>Upgrading to the Oracle Managed Driver (19.10.1), fixes the ORA-12514 error in the Oracle Rac (Real Application Cluster). For more information on this and other fixes, see the Oracle release notes.  (RPLAT-542)</li>
<li>Now, with Flexible Upgrades, after upgrading the Platform Server, you can opt to publish your applications gradually, following your teams' pace, instead of being required to publish all your applications directly after the upgrade. Not yet available in Platform installations running over Oracle, only for SQL Server. (RSUPT-705)</li>
<li>Now you can configure friendly URLs in your Reactive Web Apps. Go to  Service Center &gt; Administration &gt; SEO URLs to set up the site rules and redirects. Configure the page rules in Service Studio, by setting Custom URLs to Yes in the Screen properties. SEO Friendly URLs is a technical preview feature, and you need to activate the option "SEO Friendly URLs" in LifeTime.  (RTAFB-3869)</li>
<li>Inside Service Studio, you can now translate the UI for Reactive Web and Mobile Apps. (RTAFB-4112)</li>
<li>Added the server-to-client data transfer optimization for the Mobile and Reactive Web Apps. The optimization works for Screen Aggregates, Data Actions, and for the Server Actions in the logic flows of Screen Client Actions. (RTAFB-4331)</li>
<li>Now you can, in Mobile and Reactive Web Apps, create lightweight emails with basic navigation and styling. Emails in Reactive and Mobile is a technical preview feature, so you need to activate the option "Emails for Mobile and Reactive" in LifeTime. (RTAFB-4361)</li>
</ul>
<h3 id="Bug_Fixing_8">Bug Fixing</h3>
<ul>
<li>Fixed the client-side logs not being sent to the server after an upgrade rollback in a native mobile app. (RAR-123)</li>
<li>Fixed the client-side logs created offline not being sent to the server when reopening the app with the connection restored. (RAR-124)</li>
<li>The Dropdown now selects the correct item when the list contains default values for OutSystems data types.  (RAR-610)</li>
<li>The default font in some factories, now loads correctly on users apps. 



 (RLIT-4295)</li>
<li>Improved the feedback message when configuring Android Mobile Apps. (RLIT-4428)</li>
<li>The correct link now displays in the the Mobile Application description in Service Center.  (RLIT-4434)</li>
<li>Fixed an issue in Service Center preventing the dependencies in a Solution to be properly shown. (RLIT-4457)</li>
<li>Fixed an issue that prevented the validation messages from appearing when a Form widget was used inside a Popup widget. This fix was done with the upgrade to React 16 of the runtime libraries. (RPD-3637)</li>
<li>Fixed a timeout error when deploying large modules or extensions. (RPD-3695)</li>
<li>Fixed an issue that could cause some application screens to crash and not recover, when there are database problems while loading Static Entities. (RPLAT-537)</li>
<li>We fixed the EPA Taskbox to correctly show content in the production environment. The Taskbox didn't send the UserId in the requests, causing an empty Activity Details Page. (RPM-1007)</li>
<li>Scheduler Service and Deployment Controller Service now run with a user with lower privileges. If during an upgrade you encounter any issues while setting the permissions for OutSystems services, <a href="https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Service_permissions_error_when_installing_or_upgrading_to_Platform_Server_11.12.0_or_later">check this article</a>. (RPM-330)</li>
<li>Fixed an issue in the configuration of SAML authentication that prevented uploading a custom KeyStore. (RPM-339)</li>
<li>Fixed an issue causing a SBOX_FATAL_MEMORY_EXCEEDED error when having complex local storage Aggregates in PWAs. (RPM-427)</li>
<li>Fixed an issue in Service Center preventing the dependencies in a Solution to be properly shown. (RPM-490)</li>
<li>Fixed an issue that caused SSO to fail with some Identity Providers. (RPM-510)</li>
<li>Fixed an issue that caused an error when logging out from all applications using SAML authentication. This issue occurred only in on-premises infrastructures using Oracle databases. (RPM-530)</li>
<li>Triggers are now enabled in Oracle Databases if the compilation fails at the "Updating column default values" step. (RPM-541)</li>
<li>Fixed an issue on PWAs that caused Aggregates having a With or Without Join and a Filter over the joined Entity comparing its Id Attribute with NullIdentifier() to return no results. (RPM-565)</li>
<li>Fixed a Platform Server upgrade issue while running the Configuration Tool when the connection to MABS server fails. (RPM-592)</li>
<li>Fixed an issue that could cause the Service Center to become unavailable when using "servicecenter" as an alias of an application. (RPM-641)</li>
<li>Fixed a publishing error in public screens where producers were not exporting the default values of input parameters. (RPM-648)</li>
<li>Fixed an issue in the DiffDays client-side function that wasn't taking the time zone into consideration. (RPM-655)</li>
<li>Fixed issue that caused the filter on applications in Email Logs page to be lost when changing page. (RPM-696)</li>
<li>Fixed app runtime crashes after upgrading to Platform Server version 11.10.0 and later, when accessing Site Properties of a particular set of modules. (RPM-706) (RPM-706)</li>
<li>Fixed an issue that was causing the Traditional Web App Feedback balloon to be hidden whenever a screen's preparation calls to the Taskbox_Hide action.  (RPM-709)</li>
<li>Fixed a Mobile App issue related to the triggering of the OnApplicationReady action before the app reloads to perform an upgrade. (RPM-799)</li>
<li>Added instructions to the install the check list to remove a Pure Deployment Controller from the Load Balancer, as well as disable the OutSystemsApplications app pool on IIS. to avoid requests being served by that server (RPM-804)</li>
<li>Fixed an issue which could cause degradation of the publish performance under certain circumstances. (RPM-810)</li>
<li>Fixed a BPT performance issue where ended events wouldn't get deleted after the process or the activity was closed. (RPM-814)</li>
<li>We improved the Service Center error "Invalid call of the [action name] client action of the [screen name] since the latter is not currently active". The error now has more details about the action and screen. Additionally, the verbosity of the error now depends on the context. (RPM-858)</li>
<li>Fixed a bug where the platform asked a user to login twice when using Integrated Windows Authentication (IWA). (RPM-924)</li>
<li>Fixed issue causing users to get the "Error loading original references" message when loading Modules that consume entities that have at least one attribute whose type is an identifier for an entity that is missing. (RPST-1305)</li>
<li>Improvements to module deletion logging now includes the time it takes for each operation to complete. 

 (RPST-1346)</li>
<li>Fixed an issue that prevented Scheduler service errors from being registered in Service Center and Event Viewer. (RRCT-3554)</li>
<li>Fixed a Traditional Web App compilation crash that involved Trigger Event node and a type conversion in the Inputs of the Web Block event. (RTAFB-3598)</li>
<li>Fixed app runtime crashes after upgrading to Platform Server version 11.10.0 and later, when accessing Site Properties of a particular set of modules. (RTAFB-4142)</li>
<li>Fixed a performance issue with compiling modules. The fix reduces the number of database queries required when computing server-to-client data transfer optimization. (RTAFB-4754)</li>
</ul>
<h3 id="Known_Issues_2">Known Issues</h3>
<ul>
<li>Publishing Mobile or Reactive Web apps that use very complex structures in screen logic may take longer than usual or fail due to a timeout during compilation. It might also result in a memory consumption higher than usual while publishing.</li>


    To disable this for a specific module you can follow this procedure:

    <ol>
<li>Install Factory Settings Module in the environment (skip if already installed);</li>
<li>Access Factory Settings Application; - Select "eSpaces" in the top of the app;</li>
<li>Select your module from the list;</li>
<li>Add a new configuration with the name "ClientSideOptimizerDisabled" and the value "True";</li>
<li>Press "Define".</li>
</ol>

    To disable this for the whole environment you can follow this procedure:

    <ol>
<li>Install Factory Settings Module in the environment (skip if already installed);</li>
<li>Access Factory Settings Application;</li>
<li>Select "Platform Configurations" in the top of the app;</li>
<li>Tick the options "Disable client-side optimizations for Reactive Web Apps" and "Disable client-side optimizations for Mobile Apps";</li>
<li>Go to the bottom of the page and press "Apply".</li>
</ol>
<li>Concurrent usage of Static Entities defined in Libraries can lead to transient application runtime errors.</li>
</ul>
<h2 id="Platform_Server_11.11.3">Platform Server 11.11.3</h2>
<div class="info"><p>Released on Apr 21, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.11.3"><span id="Bug_Fixing_10"></span><h3 id="Bug_Fixing_9">Bug Fixing</h3>
<ul>
<li>Expression values in widgets are now correctly translated when the locale changes. (RAR-603)</li>
<li>Fixed the Input widget so it doesn't lose the focus when inside the Popup widget. Applies to the Technical Preview - Reactive Web and Mobile runtime on React 16. (RAR-623)</li>
<li>Classification of end-users of OutSystems applications will now consider users with repeated accounts (same email or username) on different default tenants to consume only one license slot per user. (RPM-473)</li>
<li>2-Stage deployment no longer skips the "finalize deploy" step. If for example, a solution contains a Producer and an outdated consumer module, the solution successfully completes and uses the updated modules. (RPM-538)</li>
<li>Fixed an issue that was causing memory leaks in Google Chrome browser when applying settings to the factory. (RPM-611)</li>
<li>Zip extension fixed to support unicode characters. (RPM-841)</li>
<li>Fixed an issue that prevented images from being displayed when Client-side optimizations Technical Preview feature was enabled. (RPM-848)</li>
<li>2-Stage deployment no longer skips the "finalize deploy" step. If for example, a solution contains a Producer and an outdated consumer module, the solution successfully completes and uses the updated modules. (RPST-1444)</li>
</ul>
</div><span id="Platform_Server_11.11.2"></span><h2 id="Platform_Server_11.11.2">Platform Server 11.11.2</h2><br/><div class="mt-include" id="s32044">
<div class="info"><p>Released on Apr 21, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.11.2"><span id="Bug_Fixing_11"></span><h3 id="Bug_Fixing_10">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the deploy of modules with outdated references when deploying the running version of a solution with 2-Stage deploy on. (RPM-914)</li>
</ul>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that  could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li> Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</div></div><span id="Platform_Server_11.11.1"></span><h2 id="Platform_Server_11.11.1">Platform Server 11.11.1</h2><br/><div class="mt-include" id="s31958">
<div class="info">
<p>Released on Mar 15, 2021</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.11.1"><span id="New_in_Platform_Server_11.11.1"></span><h3 id="New_in_Platform_Server_11.11.1">New in Platform Server 11.11.1</h3>
<ul>
<li>This improvement fixes the table headers not being re-rendered when the locale changes. (RAR-456)</li>
<li>The Scheduler Service now runs in an isolated folder inside the Platform Server installation folder, "{Platform Server folder}/Scheduler". (RPOT-989)</li>
<li>Significantly improved the deployment time when a new attribute is added to an entity with millions of entries. (SQLServer Enterprise and Oracle) (RSAT-1049)</li>
<li>You can now override the extensibility configurations of your PWA application through LifeTime and you can also include your configurations in any module of the application. (RTAFB-2611)</li>
<li>Now the apps properly show content for the right-to-left (RTL) languages. (RTAFB-4062)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.11.1"><span id="Bug_Fixing_12"></span><h3 id="Bug_Fixing_11">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the id attribute in the Widgets to be placed in the wrong HTML element in runtime. Applies to the Technical Preview - Reactive Web and Mobile runtime on React 16. (RAR-436)</li>
<li>Fixed an issue that caused a screen not to be updated after changing a Client Variable or the Current Locale from within a Block. (RAR-597)</li>
<li>Fixed error in Service Actions when "Force HTTPS for exposed integrations in Web Applications" setting is enabled without HTTPS being used on internal communications. (RPD-4116)</li>
<li>Fixed an issue that caused emails to be sent more than once when there are multiple front-end servers registered. (RPD-4844)</li>
<li>Fixed an issue that caused Service Center's Default Document setting in IIS to be disabled after upgrading the Platform Server. (RPD-5061)</li>
<li>Fixed an issue that prevented Timers to run after changing the module's name. (RPD-5119)</li>
<li>Fixed an issue on the Gathering Dependencies step when publishing a solution that caused "An item with the same key has already been added." error. (RPD-5120)</li>
<li>Fixed the user experience when navigating on Service Center listing screens. Now, the selected filters are kept after navigating away and using the browser Back button to return to the screen. (RPD-5139)</li>
<li>Fixed connection errors in Service Studio when enabling Progressive Web Apps (PWA) feature. (RPD-5163)</li>
<li>Fixed a compilation error in Oracle when publishing a module having an Entity attribute defined as Decimal (20,0). (RPD-5206)</li>
<li>Fixed messages that appear when configuring MDC using case sensitive catalogs to give the correct error information. (RPLAT-64)</li>
<li>Fixed an issue that caused deadlock errors while dequeuing events in Error Log, by adding the OSAIX_OSSYS_BPM_EVENT_DEQUEUE_FOR_FRONT index on the table OSSYS_BPM_EVENT to the platform. This index is created outside the main database create or upgrade process due to its creation impact. (RPM-315)</li>
<li>Fixed an issue that caused LifeTime API to return an expired license error after installing a valid license. (RPM-421)</li>
<li>Fixed an issue that caused an "Unable to save the deployment plan" error when deploying an application that consumes an SC Extension, between environments on LifeTime. (RPM-458)</li>
<li>Back navigations on Mobile Apps and Reactive Web Apps now correctly initialize the input values after an upgrade of the application. (RPM-485)</li>
<li>Fixed an issue assigning complex variables in Client Actions when using the cache mechanism. (RPM-489)</li>
<li>Removed the 2000 character limit in the Service Center Internal User classification rule (RPM-514)</li>
<li>Fixed an issue where SEO Page Rules were cleared in a first redirect from an HTTP URL to an HTTPS URL. (RPM-534)</li>
<li>Mappings being used on ListAppend and ListInsert actions now return all the expected records. (RPM-556)</li>
<li>Fixed an issue in method unregisteredBackNavigationHandler of JavaScript Navigation API causing all registered back navigation handlers to be removed from the queue. (RPM-557)</li>
<li>Fixed a compiler error when a structure list with the attributes of the Entity type was used as a Source Record List in the ComboBox widget of a Traditional Web App. (RPM-558)</li>
<li>Fixed an issue that could cause errors in PWAs (progressive web apps) running offline, if the PWAs were staged to a new environment in LifeTime or published from a solution. (RPM-582)</li>
<li>Fixed an issue that prevented the value of a Foreign Key Attribute in a Static Entity Record that was deleted in Service Studio from being deleted from the database. (RPM-591)</li>
<li>Fixed an issue where SLOWSQL entries for IsUserActive always had the column UserId set to zero. (RPM-713)</li>
<li>Fixed a runtime behavior causing Ajax requests to block for users having Kaspersky anti-virus software installed. (RPM-752)</li>
<li>Fixed Client Actions set as functions so they use the default parameters when those functions are used inline. Previously the Client Actions set as functions ignored the default values in the inline calls. (RPM-760)</li>
<li>Configuration Tool always launches Service Center installation on every execution (RPM-815)</li>
<li>Fixed an issue with the calculation of the next run date for BPT events that failed with errors. Previously the next run date was set after months instead of after minutes. (RPM-877)</li>
<li>Fixed problem executing aggregates due to optimizations not replacing the table names. (RPM-948)</li>
<li>Fixed an issue in Service Center that caused a redirection to a Submit Error page when a site property was assigned a value not compatible with its data type. (RPST-1155)</li>
<li>Improved the Configuration Tool logging of errors while giving folder permissions. (RPST-931)</li>
<li>Fixed an issue with the calculation of the next run date for BPT events that failed with errors. Previously the next run date was set after months instead of after minutes. (RRCT-3319)</li>
<li>Fixed a memory leak that occurred with BPT in modules with debug mode disabled and that caused application pools to grow unexpectedly. (RRCT-3336)</li>
<li>Fixed connections from REST Consume integrations that weren't properly closed at runtime, in some situations. (RSBO-1538)</li>
<li>Fixed the Global Actions and Exception Flows in the Multilingual feature to correctly return the translations as set by the locale. (RTAFB-3531)</li>
<li>Fixed the inline records inside the widget input properties, to make the widgets work correctly and without runtime errors. (RTAFB-3604)</li>
<li>Fixed SetCurrentLocale Server Action so the locale changes correctly when you use this Action. We discovered this bug in the Multilingual technical preview feature for Mobile Apps and Reactive Web Apps. (RTAFB-3775)</li>
<li>Fixed an issue that could cause errors in PWAs (progressive web apps) running offline, if the PWAs were staged to a new environment in LifeTime or published from a solution. (RTAFB-3789)</li>
<li>Fixed a compiler error when a structure list with the attributes of the Entity type was used as a Source Record List in the ComboBox widget of a Traditional Web App. (RTAFB-3797)</li>
</ul>
<ul>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 4.1 (Medium). (RPD-4611)</li>
<li>Extension resources are no longer copied to consumers when there are only weak dependencies. CVSSv3.1 score 5.1 (Medium) (RTAFB-3511)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.11.1"><span id="Breaking_Change_2"></span><h3 id="Breaking_Change_1">Breaking Change</h3>
<ul>
<li>Now, HTTP responses from Consumed REST API integrations are closed more aggressively. Previously, when doing numerous Consumed REST API requests, the number of used ports could increase rapidly and lead to port exhaustion problems. The new behaviour prevents this situation and helps avoid leaking resources, but can also cause runtime changes in some edge cases.<br/>
Check <a class="link-https" href="https://www.outsystems.com/goto/breaking-changes-11#introduced-in-platform-server-11111" rel="external noopener nofollow" target="_blank">OutSystems 11 side effects and breaking changes</a> for more details on the breaking change and on a possible workaround.</li>
</ul>
</div></div><span id="Platform_Server_11.10.4"></span><h2 id="Platform_Server_11.10.4">Platform Server 11.10.4</h2><br/><div class="mt-include" id="s32957">
<div class="info"><p>Released on Apr 21, 2021</p></div>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that  could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li> Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</div><span id="Platform_Server_11.10.3"></span><h2 id="Platform_Server_11.10.3">Platform Server 11.10.3</h2><br/><div class="mt-include" id="s31759">
<div class="info"><p>Released on Feb 08, 2021</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.3"><span id="Bug_Fixing_14"></span><h3 id="Bug_Fixing_12">Bug Fixing</h3>
<ul>
<li>Fixed application downtime in Farm environments due to missing DLLs in the Frontend servers, caused by running Configuration Tool from a location different than the first time it was executed, e.g through a symbolic link. (RPM-776)</li>
</ul> </div></div><span id="Platform_Server_11.10.2"></span><h2 id="Platform_Server_11.10.2">Platform Server 11.10.2</h2><br/><div class="mt-include" id="s31565">
<div class="info"><p>Released on Dec 28, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.2"><span id="New_in_Platform_Server_11.10.2"></span><h3 id="New_in_Platform_Server_11.10.2">New in Platform Server 11.10.2</h3>
<ul>
<li>When using React 16, render loop check now redirects to the Error Screen when a loop is avoided to prevent presenting incorrect data to the user.  (RAR-441)</li>
<li>The locale is now added to the lang HTML element and corresponds to the same locale defined by the application. This is particularly important for accessibility purposes. (RTAF-3037)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.2"><span id="Bug_Fixing_15"></span><h3 id="Bug_Fixing_13">Bug Fixing</h3>
<ul>
<li>Fixed the text of the error message that shows when the app uses an unknown locale identifier. (RAR-330)</li>
<li>Registering a back navigation handler now correctly blocks a back navigation on React 16. (RAR-333)</li>
<li>Fixed the animation that is triggered by the event of leaving screen when using React 16. (RAR-439)</li>
<li>Fixed an issue that caused "None" type screen transitions to be animated in React 16. (RAR-445)</li>
<li>Fixed the on-screen keyboard so the search button shows for the inputs with the search type. (RPD-4843)</li>
<li>Fixed error that could prevent opening the Manage Dependencies window in Service Studio. (RPC-581)</li>
<li>Fixed an issue in Local Storage that led to a compilation timeout and prevented publishing apps.  (RPM-467)</li>
<li>Fixed the cookies generated by Embedded Process Automation (EPA) taskbox so they use valid characters. (RPM-404)</li>
<li>Fixed the error screen that failed to initialize properly in PWAs. The bug also caused a popup to show that the browser didn't support Local Storage on iOS. This was happening because the error screen tried using WebSQL by default, instead of IndexedDB. (RPM-430)</li>
<li>Fixed error that could prevent opening the Manage Dependencies window in Service Studio (regarding extensions). (RPST-1122)</li>
<li>Fixed Service Center and System Components install being repeated by Configuration Tool even when their currently published version is already up-to-date. (RSUPT-558)</li>
<li>Fixed the cookies generated by Embedded Process Automation (EPA) taskbox so they use valid characters. (RTAF-3466)</li>
<li>Fix for connections left open in the database when modules start (RRCT-3274)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 5.4 (Medium). (RPD-4842)</li>
<li>Fixed a security issue. CVSSv3.0 score 5.3 (Medium). (RPD-4670)</li>
<li>Fixed a security issue. CVSSv3.0 score 5.8 (Medium). (RTAF-3479)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.2"><span id="Known_Issues_5"></span><h3 id="Known_Issues_3">Known Issues</h3>
<ul>
<li>In farm environments, if there is a symbolic link to the Platform Server folder, it’s possible for the Configuration Tool to be executed from different locations. e.g “F:\Program Files\OutSystems\Platform Server” is the platform installation folder and “C:\Program Files\OutSystems\” is a symbolic link. Every time Configuration Tool is run from a different location, it will corrupt some platform settings and it will cause DLLs to be wrongly deleted from the front-end.<br/>
More details <a class="link-https" href="https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Known_issue_in_11.10.0_-_possible_downtime_after_running_Configuration_Tool" rel="external nofollow" target="_blank">here</a>.</li>
</ul></div></div><span id="Platform_Server_11.10.1"></span><h2 id="Platform_Server_11.10.1">Platform Server 11.10.1</h2><br/><div class="mt-include" id="s31453">
<div class="info"><p>Released on Nov 30, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.1"><span id="New_in_Platform_Server_11.10.1"></span><h3 id="New_in_Platform_Server_11.10.1">New in Platform Server 11.10.1</h3>
<ul>
<li>Multilingual for Mobile and Reactive now maintains the selected locale between applications. (RAR-338)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.1"><span id="Bug_Fixing_16"></span><h3 id="Bug_Fixing_14">Bug Fixing</h3>
<ul>
<li>Fixed "No Default Screen" error screen when no default screen is selected. Now the app uses the first screen of the module and there's no error. (RAR-356)</li>
<li>Fixed navigation after a pending refresh. Now the screen redirects to the destination screen if there's a pending refresh when the user refreshes the page. Previously the app showed the origin screen after the refresh. (RAR-422)</li>
<li>Fixed an issue with the message after an upgrade is rolled back. The message that notifies the user that the upgrade failed now correctly shows. (RAR-423)</li>
<li>Added a new NameId format option in SAML configuration of the Users module (&lt;Ignore field&gt;). This new option allows you not to send the NameId format field. (RIDT-355)</li>
<li>Now, having a file named "Program" inside C:\ no longer causes errors when accessing Server.Identity and Server.API. (RPM-343)</li>
<li>Fixed an issue that caused the render loop protection to be triggered when multiple client variables were assigned in a client screen action flow. (RPM-380)</li>
<li>Fixed incorrect redirect to Users module after login using SAML Authentication for end-users.  (RPM-395)</li>
<li>Configuration Tool is now able to detect the installation of .NET Hosting Bundle in order to diagnose problems related to its misconfiguration. (RPM-399)</li>
<li>Fixed PWAs crashing in OutSystems on iOS when accessing Local Storage. The crash was introduced by a bug in WebKit (<a class="link-https" href="https://bugs.webkit.org/show_bug.cgi?id=216769" rel="external noopener nofollow" target="_blank" title="https://bugs.webkit.org/show_bug.cgi?id=216769">https://bugs.webkit.org/show_bug.cgi?id=216769</a>). (RPM-429)</li>
<li>Fixed a rare issue where publishing an extension would impact the database tables used by another module. (RPM-498)</li>
<li>Fixed issue where some database connections would be left open when starting a module. (RPM-504)</li>
<li>Fixed potential deadlock in OutSystems services when generating error logs while persisting logs in the database. (RRCT-3222)</li>
<li>Using .Net Framework  4.7.2 Oracle DB Provider. (RSAT-2481)</li>
<li>Validation and Upgrade messages can now be properly translated in Reactive and Mobile applications. (RTAF-3427)</li>
<li>The page title is now correctly translated in the runtime of Reactive Web Apps and Mobile Apps. (RTAF-3505)</li>
</ul>
<li>Fixed an issue that allowed code injection on the description of exposed SOAP Web Services. CVSSv3.1 score 4.8 (Medium). (RBIT-37)</li>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.1"><span id="Known_Issues_6"></span><h3 id="Known_Issues_4">Known Issues</h3>
<ul>
<li>In farm environments, if there is a symbolic link to the Platform Server folder, it's possible for the Configuration Tool to be executed from different locations. e.g “F:\Program Files\OutSystems\Platform Server” is the platform installation folder and “C:\Program Files\OutSystems\” is a symbolic link. Every time Configuration Tool is run from a different location, it will corrupt some platform settings and it will cause DLLs to be wrongly deleted from the front-end.<br/>
More details <a class="link-https" href="https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Known_issue_in_11.10.0_-_possible_downtime_after_running_Configuration_Tool" rel="external nofollow" target="_blank">here</a>.</li>
</ul></div></div><span id="Platform_Server_11.10.0"></span><h2 id="Platform_Server_11.10.0">Platform Server 11.10.0</h2><br/><div class="mt-include" id="s31137">
<div class="info"><p>Released on Nov 09, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.0"><span id="New_in_Platform_Server_11.10.0"></span><h3 id="New_in_Platform_Server_11.10.0">New in Platform Server 11.10.0</h3>
<ul>
<li>The error logs about the server responses in Mobile/Reactive apps now have information about the endpoint in use. (RAR-259)</li>
<li>You can now try out the Reactive and Mobile applications using the React 16 version. Start by enabling this technical preview feature in LifeTime. (RAR-270)</li>
<li>Fixed a bug that was blocking the user to set big extensibility configurations on LifeTime.
It depends on LifeTime version 11.6.1. (RLIT-3938)</li>
<li>Added support for email SMTP servers using implicit SSL connections on port 465. (RPD-4025)</li>
<li>It is now possible to apply settings to the OutSystems factory using a command-line flag of Configuration Tool. (RPD-4862)</li>
<li>Added a retry mechanism for database deadlocks that occur while obtaining user information from the database. (RPST-374)</li>
<li>Now, when the Purpose of an environment changes a log entry is added. (RPST-883)</li>
<li>Added support for PLAIN authentication when connecting to email SMTP servers. OutSystems uses PLAIN authentication when LOGIN authentication is not available. (RRCT-2935)</li>
<li>Upgraded NLog libraries to version 4.7.2. (RRCT-2965)</li>
<li>Improved the third-party libraries version algorithm added in the previous Platform Server versions to be more resilient regarding extensions that were created incorrectly. (RRCT-3102)</li>
<li>Platform Server installation logs are now placed on the %localappdata%\OutSystems\PlatformInstaller folder. (RSAT-2289)</li>
<li>You can now optimize the amount of data transferred from the server side to the client side of Mobile and Reactive Web Apps. The optimization works for Screen Aggregates, Data Actions, and for the Server Actions in the logic flows of Screen Client Actions. This is a technical preview feature and you need to activate the option "Client-side optimizations for Reactive Web Apps" or "Client-side optimizations for Mobile Apps". (RTAFB-3260)</li>
<li>You can now translate the UI of your Reactive Web Apps and Mobile Apps directly inside Service Studio. Multilingual is a technical preview feature and you need to activate the option "Multilingual for Mobile and Reactive" in LifeTime. After enabling the feature, use the new Multilingual Locales folder and new SetCurrentLocale system client action. (RTAFB-3388)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.10.0"><span id="Bug_Fixing_17"></span><h3 id="Bug_Fixing_15">Bug Fixing</h3>
<ul>
<li>Fixed the app upgrade mechanism when technical preview "Configure Mobile application updates distribution" is on. Previously, a native mobile app would still use the hybrid updates on the first load. (RAR-219)</li>
<li>Improved the error message when the app requires local storage access and IndexedDB isn't supported. (RAR-220)</li>
<li>Fixed authenticated user losing the roles while navigating from a Traditional to a Reactive app, with Single Sign-On activated. (RAR-307)</li>
<li>Fixed the CSS for the Dropdown widget. Now the CSS rules apply correctly. (RAR-332)</li>
<li>Fixed the scroll behavior of the Dropdown widget with Options Content set to Custom, in Reactive/Mobile apps. Previously the content scrolled down when users selected an item. (RAR-341)</li>
<li>Fixed a bug that caused Service Center to incorrectly count Internal and External Users from disabled User Providers as active users. (RIDT-95)</li>
<li>Action User_CreateOrUpdate of Users API now prevents the creation of new users with an existing username. (RLIT-3711)</li>
<li>Fixed an issue that was setting the wrong application description when creating the application through LifeTime. (RLIT-3888)</li>
<li>Fixed an issue in Service Center that was causing a weird behavior on the application edit screen when the setting .NET Globalization/UI Culture in IIS was set to pt-BR. (RLIT-3895)</li>
<li>We made several improvements in Service Center's Request Log screen (still in beta version): fixed an exception thrown when opening the Request Log screen through the Request Key link on the Error Log screen in Oracle databases; fixed an issue that caused the Timer details link to always redirect to the wrong screen; now the Request Logs screen works better for large factories. (RLIT-3904)</li>
<li>Fixed error "[OSNOP5].DBO.[OSSYS_CLOUDPROVIDERTYPE] with key 0 was not found" in Service Center. (RLIT-3982)</li>
<li>Fixed Expressions linked to the show-default-value attribute in Input widgets to reevaluate correctly after change. (RPD-4850)</li>
<li>Now you can choose the NameId format from a list of options when configuring SAML 2.0 Authentication for end users in the Users application. (RPD-5000)</li>
<li>Fixed compilation error that occurred when there was a new attribute in a producer structure with a default value that wasn't refreshed in a consumer. (RPD-5039)</li>
<li>Changed IIS configurations to define the minWorkerThreads. This change will not be applied if this value is already configured. (RPD-5040)</li>
<li>Fixed an issue where some SQL scripts for SQL Server did not contain schema information. (RPD-5090)</li>
<li>Fixed broken image links to images in Mobile Apps and Reactive Web Apps when using a referenced action from another module to get the image. (RPD-5111)</li>
<li>Fixed an issue where the Popup_Editor block from RichWidgets was largely increasing the ViewState size by deprecating it into the Deprecated_Popup_Editor block and splitting it into two new blocks: The Popup_EditorForUpload to be used for the Popup_Upload screen, which requires some data on the ViewState; and the Popup_Editor to be used with any other screen, which does not require data on the ViewState. (RPD-5221)</li>
<li>Fixed an issue that occurred while using Oracle as the platform database that recreated indexes of entities on every publish of the module. (RPM-310)</li>
<li>Fixed SSO between different app types so the roles are correctly updated and users are no longer blocked from accessing the screens in the session. (RPM-312)</li>
<li>Fixed an issue that caused the static entities that shared the same first 10 characters to have the same translation table. This only affects Platform's that use Oracle database. (RPM-313)</li>
<li>Fixed compilation error that occurred when there was a new attribute in a producer structure with a default value that wasn't refreshed in a consumer. (RPD-5039) (RPM-316)</li>
<li>Fixed compilation of the local storage Aggregates with a Count over a Date/Time/DateTime attribute.  (RPM-320)</li>
<li>Fixed an issue that was preventing you from deactivating App Feedback, once you activated it for Reactive Web Apps. (RPM-362)</li>
<li>Fixed issue that caused width of a Dropdown widget defined in Service Studio to be ignored in runtime. (RPM-413)</li>
<li>Fixed database error in Oracle when publishing a module whose extended configurations exceed 4000 chars. (RPM-465)</li>
<li>Fixed an issue that caused System Components installation via Configuration Tool to timeout when the Platform Server is under heavy use (RSUPT-292). The fix consists of changing the 20 minutes timeout on the entire System Component installation, to 5 minutes timeout on each module. (RPM-500)</li>
<li>Fixed database error in Oracle when publishing a module whose extended configurations exceed 4000 chars. (RPM-539)</li>
<li>Improved the error message shown when a module is not found while publishing a solution. Now the message states "Module <module-name> with version <version-number> not found" instead of "The given key was not present in the dictionary". (RPST-363)</version-number></module-name></li>
<li>Fixed an issue in re-deploy operations that, in some situations, reused the folder of the currently running application. (RPST-371)</li>
<li>Fixed database error in oracle when publishing a module whose extended configurations exceed 4000 characters. (RPST-926)</li>
<li>Fixed issue in extension compilation during upgrades when the extension used deprecated internal methods. (RRCT-2956)</li>
<li>Fixed an error while upgrading the Cache Invalidation Service (RabbitMQ) where having a momentary lock on the old version's folder would cause a failure. (RRCT-2962)</li>
<li>The module compilation process now provides detailed error messages when there are Missing Role exceptions. (RRCT-2971)</li>
<li>Now, Configuration Tool allows special characters on the password used for the Cache Invalidation Service (RabbitMQ). (RRCT-2980)</li>
<li>Fixed runtime errors when deploying a module version that renames or deletes site properties. (RRCT-2981)</li>
<li>Fixed an issue in Configuration Tool that caused runtime errors and temporary app downtime while recreating a SQL Server session database. (RRCT-2982)</li>
<li>Fixed an issue that could prevent the Deployment Controller service from starting or rotating the log tables correctly. (RRCT-2983)</li>
<li>We added support for logging request events of server-side executions in Mobile and Reactive Web Apps. The logging of these request events is disabled by default. (RRCT-2985)</li>
<li>Timestamps used for session fixation protection are now stored using the UTC time zone. This prevents checks from being too aggressive during Daylight Saving Time transitions. (RRCT-3051)</li>
<li>Fixed an issue where applications became unavailable while publishing solutions due to License Validations. (RRCT-3215)</li>
<li>Updated the MySQL driver to version 8.0.20 and updated its dependencies. (RSAT-1965)</li>
<li>Improvement on performance for session model in Oracle. To take advantage of this improvement, you will need to upgrade the Session Database in Configuration Tool. (RSAT-1977)</li>
<li>Fixed an issue that prevented users from logging in to Service Center after installing the platform. (RSAT-2228)</li>
<li>Fixed an issue that prevented using special characters such as ";" (semicolon) in database passwords. (RSAT-2239)</li>
<li>Fixed an issue that caused Binary Data in records not to be stored in Oracle databases. (RSAT-2305)</li>
<li>Fixed an issue that occurred while using Oracle as the platform database that recreated indexes of entities on every publish of the module. (RSAT-2336)</li>
<li>Fixed an issue that prevented applications from loading DLL providers correctly, which caused errors such as "No provider registered for key ...". (RSAT-2436)</li>
<li>Improved the performance on the count of activities in the EPA Taskbox application. (RSBO-1300)</li>
<li>Fixed a solution publish error that occurred when compiling outdated dependencies to a structure having new attributes with complex data types. (RSBO-1521)</li>
<li>Fixed an issue that caused runtime calls of Service Actions to not dispose of resources (connections) at runtime. (RSBO-1539)</li>
<li>Fixed module deletion not cleaning up the module's compilation result (its "share" folder) from the file system, leading to unnecessary disk space usage. (RSUPT-252)</li>
<li>Fixed an issue that caused System Components installation via Configuration Tool to timeout when the Platform Server is under heavy use. (RSUPT-292)</li>
<li>Fixed "Cannot read property 'setAttribute' of undefined" error when creating nested tables with Table Records widget in Reactive Web App. (RTAFB-2995)</li>
<li>We fixed the issues in SSO between app types causing "invalidating espace caches" error messages in Service Center, by improving the lifecycle of cookies involved in SSO between app types. (RTAFB-3153)</li>
<li>Fixed SSO between different app types so the roles are correctly updated and users are no longer blocked from accessing the screens in the session. (RTAFB-3182)</li>
<li>Fixed a glitch in the UI that redirected users to a PopupUpload.aspx page after they pressed Enter in an Input widget, on the screen with a Popup Editor Rich Widget. (RTAFB-3184)</li>
<li>Fixed the ListClear action so Traditional Web Apps transfer less data between the server and web browser. This improves the data transfer optimization mechanism. (RTAFB-3335)</li>
<li>We fixed a compilation error when using a Client Variable as the value for the Max Records property of a Screen Aggregate. (RTAFB-3336)</li>
<li>Fixed an issue that prevented the "Distribute as PWA" toggle value to be persisted between environments when staging an app in LifeTime. (RTAFB-3411)</li>
</ul>
</div></div><span id="Platform_Server_11.9.2"></span><h2 id="Platform_Server_11.9.2">Platform Server 11.9.2</h2><br/><div class="mt-include" id="s32971">
<div class="info"><p>Released on Apr 27, 2021</p></div>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that  could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li> Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</div><span id="Platform_Server_11.9.1"></span><h2 id="Platform_Server_11.9.1">Platform Server 11.9.1</h2><br/><div class="mt-include" id="s31124">
<div class="info"><p>Released on Sep 24, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.9.1"><span id="Bug_Fixing_18"></span><h3 id="Bug_Fixing_16">Bug Fixing</h3>
<ul>
<li>Fixed crash on Chrome while uploading files bigger than 100MB in Reactive Web and Mobile Apps. (RPD-5151)</li>
<li>Solved issue that could cause timeouts in Configuration Tool, on SQL servers (RIDT-211)</li>
<li>Fixed Oracle database upgrade scripts from O10 to O11 that caused a missing table to allow BPT Events to work correctly after the upgrade to 11.9. (RPM-387)</li>
<li>Generated applications now correctly identify and load all third party library versions in order to prevent inconsistent runtime behaviors. This behavior is disabled by default. (RRCT-3106)</li>
<li>Fixed a compilation error in Oracle when an Entity attribute type was changed from Long Integer to Decimal (20,0). The system will no longer consider this a change in the database. (RPD-5206)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.4 (High). (RTAF-3379)</li>
</ul>
</div></div><span id="Platform_Server_11.9.0"></span><h2 id="Platform_Server_11.9.0">Platform Server 11.9.0</h2><br/><div class="mt-include" id="s30387">
<div class="info">
<p>Released on Jul 28, 2020</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.9.0"><span id="New_in_Platform_Server_11.9.0"></span><h3 id="New_in_Platform_Server_11.9.0">New in Platform Server 11.9.0</h3>
<ul>
<li>Improved locking on IndexedDB allowing operations that use different entities to execute simultaneously. (RAR-142)</li>
<li>Added capabilities to support the platform in Mumbai AWS region. (RCVT-370)</li>
<li>This version of Platform Server brings the early access feature "Configure mobile apps updates distribution" to manage how mobile apps update on user devices. After you activate the feature for all environments in LifeTime, control which of your apps receive updates only through the app store, and which apps receive hybrid updates. Look for the new DEPLOYMENT tab in the "Mobile app update preferences" step of a deployment plan. (RNMT-4223)</li>
<li>Added an option to only automatically refresh references during solution publish operations when there are broken references, instead of on any differences. Configurable using Factory Configuration. (RPC-1177)</li>
<li>Applications created with OutSystems now correctly identify and load all third-party library versions to prevent inconsistent runtime behaviors. (RRCT-2687)</li>
<li>Upgraded Microsoft.AspNetCore and Microsoft.Extension libraries to the latest 2.1 LTS (Long-Term Support) versions. (RRCT-2896)</li>
<li>Moved SAML-related actions from the Authentication extension to the new SAMLAuthentication extension. If you're using any SAML actions outside the Users module, we recommend that you add the SAMLAuthentication extension as a dependency and update all references to the Authentication extension. (RSAT-2104)</li>
<li>Added an option in SAML configuration to only accept signed login responses from the Identity Provider server. (RSBO-1535)</li>
<li>Progressive Web Apps (PWAs) are now generally available (GA), after a period of early access (EA). Create a mobile app, and then turn on the toggle "Distribute as PWA" in the Distribute tab. To create a mobile app, select either Phone or Tablet App in the dialog for a new app. (RTAFB-2977)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.9.0"><span id="Bug_Fixing_19"></span><h3 id="Bug_Fixing_17">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was preventing the Dropdown widget to be in dark mode. (RAR-145)</li>
<li>Fixed an issue where widgets with property values defined by an expanded record were re-rendered with every change to the screen data. (RAR-154)</li>
<li>Fixed a bug where the functions to execute the UI Block Aggregates over indexedDB could be generated with different names on their definition and usage, leading to a runtime error. (RAR-161)</li>
<li>Fixed an issue that was preventing the Daily Activity Report to be generated. (RLIT-3417)</li>
<li>Fixed a bug where sometimes extensions wouldn't sync. (RLIT-3669)</li>
<li>Fixed an issue that caused lost configuration to mobile application on LifeTime when publishing an extensibility configuration. (RLIT-3820)</li>
<li>Fixed an issue that caused an infinite loop when trying to logout using integrated authentication. (RLIT-3846)</li>
<li>Fixed vulnerability in PreviewInDevices regarding URL manipulation and Base64 encoding. (ROU-1116)</li>
<li>Upgraded Erlang to version 22.3 and RabbitMQ to version 3.8.3. Fixes occasional connection hangs on TLS connections. The Configuration Tool performs the upgrade when you click the "Create/Upgrade Service" button. (RPC-1131)</li>
<li>Fixed an issue that caused compilation errors when using long strings in Assign elements. (RPC-1132)</li>
<li>Fixed error "Object reference not set to an instance of an object." when attempting to delete an entity from a deleted Module using the DbCleaner API. (RPC-1156)</li>
<li>Fixed the Solution Upload in ServiceCenter to use less database connections. Previously it needed at least 2 connections for each application in the solution being uploaded. (RPC-1166)</li>
<li>We fixed Editable Table so it reverts the checkbox (boolean) values after users click Cancel. (RPD-3238)</li>
<li>Dropdown with custom property selected now automatically scrolls into selected item. (RPD-3459)</li>
<li>Fixed an issue that caused the incorrect render of List widgets items when the position of the list item changed. (RPD-3585)</li>
<li>Fixed an issue where sometimes when listing users in a role associated with an app the second page would show no users. (RPD-4987)</li>
<li>Fixed "ID" attribute from being placed on the container element instead of element the select on Dropdown widget. (RPD-5019)</li>
<li>OutSystems no longer generates three-part names in object definitions for SQL Azure. For more information check <a class="link-https" href="https://docs.microsoft.com/en-us/archive/blogs/ssdt/windows-azure-importexport-service-and-external-references" rel="external noopener nofollow" target="_blank">Windows Azure Import/Export Service and External References</a> in Microsoft documentation. (RPD-5024)</li>
<li>Fixed NullReferenceException when deploying a Module using 'Run As' configuration. (RPD-5093)</li>
<li>Fixed an issue that would allow changing the Deployment Zone of an application consisting of extensions. (RPD-5113)</li>
<li>Fixed issue where pages were generated with meta tag Strict-Transport-Security displaying warnings in browsers console. (RPD-5124)</li>
<li>Fixed setup issue caused by compilation path not being node aware (RPD-5132)</li>
<li>Fixed an issue that logged false positive warnings in the server's Event Viewer and Service Center General Logs. (RPM-1719)</li>
<li>Fixed a compilation error when a local storage Aggregate had a Group By with a field of the Binary Data type. (RPM-317)</li>
<li>Improvements to the GetUserApplications query in the ApplicationSwitcher from RichWidgets in order to reduce the timeout or slow load time on Oracle stacks. (RPM-483)</li>
<li>Fixed a crash in the publishing step that was caused by invalid Theme names. (RPM-550)</li>
<li>Fixed an issue that caused System modules to not be visible in Manage Dependencies by users with List Applications permission assigned as default role. (RRCT-2890)</li>
<li>Fixed Scheduler Service becomes unstoppable when it starts with Deployment Controller down. (RRCT-2892)</li>
<li>Fixed a crash in the extension publishing process when attempting to delete temporary files used for validating the extension. (RRCT-2897)</li>
<li>Fixed assembly exclusion rules in extensions to allow discontinued platform assemblies to be included as resources. (RRCT-2915)</li>
<li>Fixed a situation where the Deploy Service could get stuck for 20 minute periods when failing to deploy applications to IIS. (RRCT-2936)</li>
<li>Fixed an issue in the Authentication extension that allowed customers to inadvertently call unsupported APIs. (RSAT-2173)</li>
<li>Fixed an issue that prevented using special characters such as ";" (semicolon) in database passwords. (RSAT-2239)</li>
<li>Fixed an error in External Authentication after a platform upgrade due to a change in the encryption mechanism. (RSBO-1437)</li>
<li>Fixed an issue in the timer that cleans SAML authentication logs due to a syntax error in Oracle Databases. (RSBO-1481)</li>
<li>Fixed a solution publish error that occurred when compiling outdated dependencies to a structure having new attributes with complex data types. (RSBO-1521)</li>
<li>We improved the robustness of the IDE to better understand occasional crashes due to invalid object referencing. (RTAFB-2880)</li>
<li>Fixed the data replacement crash when Entity that was supposed to be replaced had been deleted. (RTAFB-2968)</li>
<li>Resolving this issue fixed opening the Distribute panel in cases when PWA was activated. The error occurred because the PWA assets for the native mobile apps were generated, which caused Service Worker requests issues and related errors. (RTAFB-3050)</li>
<li>Fixed an error in the Preview in Devices component that was preventing the PWA panel with the QR code to show correctly. (RTAFB-3087)</li>
</ul>
<ul>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.6 (Critical). (RPM-329)</li>
<li>The session is now logged out when there's a session fixation mismatch error. CVSSv3.1 score 3.7 (Low). (RRCT-2893)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.4 (High). (RTAFB-2226)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.9.0"><span id="Breaking_Changes"></span><h3 id="Breaking_Changes_2">Breaking Changes</h3>
<ul>
<li>The platform now gives preference to usage of specific versions of third-party assemblies that are included in extensions. As a consequence, extensions that incorrectly include .NET Framework assemblies can prevent applications from working correctly due to conflicts between the included assemblies and the assemblies of the .NET Framework installed in the machine. In particular, including the extensions System.Net.Http.dll or System.Runtime.InteropServices.RuntimeInformation.dll causes issues in logging, login, and JSON serialization. (RPM-383) (RPM-386)<br/>
Check how you can determine the affected extensions and how to adapt them to the new assembly loading behavior in <a class="link-https" href="https://www.outsystems.com/goto/breaking-changes-11#introduced-in-platform-server-1190" rel="external noopener nofollow" target="_blank">OutSystems 11 side effects and breaking changes</a>.</li>
<li>The KeyStore and SAML actions were moved from the Authentication extension, Authentication.xif, to the SAMLAuthentication extension, SAMLAuthentication.xif. This can cause some broken references when using methods from Authentication.xif that moved to the new module. (RSAT-2104)<br/>
To fix this behavior, replace dependencies to KeyStore and SAML actions from Authentication to the corresponding actions from SAMLAuthentication.</li>
</ul>
</div><div class="mt-section" id="section_4" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.9.0"><span id="Known_Issues_7"></span><h3 id="Known_Issues_5">Known Issues</h3>
<ul>
<li>Deploying a Mobile App from an environment where you enabled the toggle "Distribute as PWA" doesn't automatically enable the same toggle in the target environment. The toggle in the target environment keeps its pre-deployment value. The runtime behavior of these apps may also be affected if the apps are opened in a browser, using PWA or Preview in Devices. You must manually activate the toggle "Distribute as PWA" for the Mobile App in the target environment.</li>
</ul>
<p> </p>
<p><b>Disclaimer: </b><i>QR CODE is a registered trademark of Denso Wave Incorporated.</i></p>
<style type="text/css">.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}
</style>
</div></div><span id="Platform_Server_11.8.4"></span><h2 id="Platform_Server_11.8.4">Platform Server 11.8.4</h2><br/><div class="mt-include" id="s32970">
<div class="info"><p>Released on Apr 27, 2021</p></div>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that  could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li> Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</div><span id="Platform_Server_11.8.2"></span><h2 id="Platform_Server_11.8.2">Platform Server 11.8.2</h2><br/><div class="mt-include" id="s29745">
<div class="info"><p>Released on May 26, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.2"><span id="New_in_Platform_Server_11.8.2"></span><h3 id="New_in_Platform_Server_11.8.2">New in Platform Server 11.8.2</h3>
<ul>
<li>Improved the overall performance of compilation and runtime of local storage for PWAs. (RAR-98)</li>
<li>We improved the performance of the client-side Aggregates in the PWAs and the apps running in the browser. (RTAF-2160)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.2"><span id="Bug_Fixing_20"></span><h3 id="Bug_Fixing_18">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented the preview of the Upload widget to display the correct image. (RAR-106)</li>
<li>Fixed a bug where aggregates that contained a Binary Data attribute failed to execute in mobile apps when running on the browser/PWA on iOS/macOS. (RAR-135)</li>
<li>Fixed a security vulnerability in login. CVSSv3.0 score 5.3 (Medium) (RPD-5021)</li>
<li>Fixed cross-site scripting vulnerability. CVSSv3.0 score 6.5 (Medium). (RPD-4832)</li>
<li>Fixed a security issue that allows a user to backup a license when he was not suppose to. CVSSv3.0 score 4.9 (Medium) (RPD-4982)</li>
<li>Fixed the deserialization of "simpleContent" data in consumed SOAP Web Services due to an issue in generated internal classes. (RSBO-1380)</li>
<li>Reduced the number of IIS threads necessary for the asynchronous logging to work. (RPC-1259)</li>
</ul></div></div><span id="Platform_Server_11.8.1"></span><h2 id="Platform_Server_11.8.1">Platform Server 11.8.1</h2><br/><div class="mt-include" id="s29581">
<div class="info"><p>Released on May 18, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.1"><span id="New_in_Platform_Server_11.8.1"></span><h3 id="New_in_Platform_Server_11.8.1">New in Platform Server 11.8.1</h3>
<ul>
<li>We improved the user experience for activating Single Sign-On Between App Types (SSO) in Service Center &gt; Administration &gt; Security &gt; Applications Authentication. Service Center now checks the requirements beforehand and determines whether security is managed in LifeTime. (RTAF-2459)</li>
<li>We improved the user experience for deactivating Single Sign-On Between App Types (SSO) in Service Center &gt; Administration &gt; Security &gt; Applications Authentication. Now there's a message informing you which options need to be off when deactivating SSO. (RTAF-2535)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.1"><span id="Bug_Fixing_21"></span><h3 id="Bug_Fixing_19">Bug Fixing</h3>
<ul>
<li>Fixed an error while using Upload wiget with property capture on Android devices (RPD-4841)</li>
<li>We fixed the page scrolling up in Reactive Web App when users open a Popup widget. (RTAF-2550)</li>
<li>Fixed an issue where list iterations on functions raised an error when the function was called from an Expression in a widget. (RPD-3756)</li>
<li>Fixed SAP service generated code dumping the password not encrypted. (RSBO-1346)</li>
<li>Fixed bug where Internal and External Users features count was not coherent with the sum of users per User Provider in Oracle. (RSBO-1298)</li>
<li>We improved the robustness of the PWA caching mechanism by removing the unnecessary handling of the static resources. (RTAF-2150)</li>
<li>Fix issue that could cause all other applications to reload in IIS when a new or renamed module was published. (RPC-1168)</li>
<li>Fixed issue in Users application when filling Authentication configuration manually. (RSBO-1324)</li>
<li>Fixed visual hint on labels for mandatory RadioGroup and ButtonGroup widgets. (RAR-95)</li>
<li>Fixed ListDistinct System Action by tweaking the optimization algorithm. In certain cases, when the list came from an Aggregate of the same Action, the algorithm incorrectly removed duplicate list items. (RPD-4840)</li>
<li>Fixed an issue on the compiler optimization logic related to the basic list operations. The issue sometimes caused incorrect runtime behaviors. (RTAF-2027)</li>
<li>Fixed an issue that increased solution publication time when OSSYS_SOL_PUB_UNIT table had many entries. (RPD-4188)</li>
<li>Fixed issue preventing the creating of users in Service Center in environments not connected to LifeTime when there is an external authentication provider defined. (RLIT-3660)</li>
<li>Removed fallback JavaScript code in Service Center for features not supported in older browsers. (RLIT-3707)</li>
<li>Fixed bug on Service Center that was keeping the Mobile Apps tab on Monitoring from opening. (RLIT-3857)</li>
<li>Improved performance of Service Center's page that lists modules on large factories. (RLIT-3709)</li>
<li>Fixed an issue that was preventing Service Center to report the correct information about Extensibility Configurations to LifeTime, causing these configurations to always revert to Default when a module was published. (RTAF-2502)</li>
</ul></div></div><span id="Platform_Server_11.8.0"></span><h2 id="Platform_Server_11.8.0">Platform Server 11.8.0</h2><br/><div class="mt-include" id="s28942">
<div class="info"><p>Released on Apr 13, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.0"><span id="New_in_Platform_Server_11.8.0"></span><h3 id="New_in_Platform_Server_11.8.0">New in Platform Server 11.8.0</h3>
<ul>
<li>Added a progress bar to Service Center operation pages, such as publish or apply settings, in order to improve the visibility of the progress and status of the operation. (RLIT-3565)</li>
<li>Reviewed the sections for granting security levels to Users or Roles in several screens, improving the copy and pattern used.  (RLIT-3119)</li>
<li>Upgraded Oracle Driver to Oracle.ManagedDataAccess.Core version 2.19.60. (RPC-825)</li>
<li>Updated MySQL driver to version 8.0.18. (RPD-4645)</li>
<li>The built-in Service Studio tutorial (Help &gt; Build an App in 5 min) now shows how to use the <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Implement_Application_Logic/AI-assisted_development" rel="internal">suggestions by the AI-assisted development feature</a>. (RAID-484)</li>
<li>The configuration of Deployment Zones is now only available at application level. Applications with modules in different deployment zones are still supported but this is a deprecated configuration, which we will drop in the future. If you have applications with modules in different deployment zones, you must refactor and reorganize them to meet this restriction. (RLIT-3574)</li>
<li>Now you can use the new "Apply Settings to the Factory" button in Service Center to set runtime settings of an Environment, instead of creating and publishing a Solution containing all Modules.<br/>
You'll also see a new warning in the sidebar whenever the environment has pending configurations. (RLIT-3632)</li>
<li>The QR Code now uses AppKey, instead of AppName, to generate the Application link. (ROU-890)</li>
<li>Improved error handling in threads created by OutSystems services to prevent potential crashes in error scenarios. (RPC-757)</li>
<li>You can now use SAML 2.0 authentication in your Reactive Web Apps. (RSBO-1318)</li>
<li>Now you can use Radio Button Widget in your Reactive Web and Mobile apps. To build and deploy an app with this widget in UI, you also need to update Service Studio and OutSystems UI. (RTAF-2143)</li>
<li>Now you can use Human Activity Destination property in Reactive Web Apps. (RTAF-2304)</li>
<li>We fixed the reloading of screens while navigating back in Mobile Apps and Reactive Web Apps. This was caused by a glitch in the way the apps handle the list of visited pages, in particular the Screens marked as default. (RTAF-2328)</li>
<li>We improved the preview of the Table Widget. The Table now displays more example records and you can hide/show the rows. (RTAF-1789)</li>
<li>Local storage for PWAs now takes advantage of IndexedDB. IndexedDB ensures better compatibility with modern browsers. IMPORTANT: The change of the database engine deletes the browser app data in your existing PWAs. If you notice runtime issues in PWAs, delete the site storage for the app domain. (RTAF-1188)</li>
<li>We implemented the single sign-on (SSO) for Traditional, Reactive Web and Progressive Web Apps (PWAs). Your users now sign in to one app and switch to the other apps without having to sign in again. (RTAF-1874)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.0"><span id="Bug_Fixing_22"></span><h3 id="Bug_Fixing_20">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused registering duplicated Application Templates. (RTAF-1847)</li>
<li>Fixed error detection in the compilation process. Subsequent errors could hide the original error cause. (RPC-888)</li>
<li>Fixed the execute permissions of the stored procedure that removes BPT events from the queue to enable no-downtime upgrades. (RSBO-1203)</li>
<li>Fixed a compiler crash when publishing a Solution that occurred when an Attribute from a producer Entity or Structure was deleted and a new attribute with the same name was added. (RSBO-1053)</li>
<li>Fixed a compiler crash when publishing a Solution that occurred when changing the Identifier of a Static Entity. (RSBO-1049)</li>
<li>Fixed an issue that caused unnecessary redeploys of apps in machines set to a non-UTC timezone, causing some app downtime. (RPC-1158)</li>
<li>Fixed an issue that published the most recent version of a Module while trying to republish the currently running version of that Module. (RPC-1192)</li>
<li>Internal logging now also includes the information sent to the Event Viewer to ease troubleshooting. (RPC-952)</li>
<li>Improved the session handling mechanism for OutSystems applications. (RPC-950)</li>
<li>Fixed Static Entities translations not preserving unicode characters when a translation is not defined. (RSBO-1043)</li>
<li>We improved the stability of the 1-Click Publish feature by fixing a bug related to the setting of a Style Property to a Web Block. (RTAF-2024)</li>
<li>Fixed an issue with timers and processes not running during balanced upgrades from OutSystems 10 to OutSystems 11. (RPC-390)</li>
<li>Improved startup time of Deployment Controller Service in large factories by removing redundant license validations. (RPC-381)</li>
<li>Fixed a bug that made it impossible to go back to a Timer's default timeout. (RPC-669)</li>
<li>Fixed error that could prevent opening the Manage Dependencies window in Service Studio. (RPC-581)</li>
<li>Fixed an issue in Configuration Tool when there's an incomplete SAML configuration, occurring in Oracle Databases. (RSBO-1222)</li>
<li>Fixed an issue that occurred during the publishing of a solution in an environment using SEO.
The issue caused the following error: "A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond". (RPD-4770)</li>
<li>Fixed error when resetting Authentication configuration in the Users application after upgrading from previous Platform Server 11.7.x versions. (RSBO-1110)</li>
<li>Fixed version number inconsistency in platform libraries used by Integration Studio. (RPC-975)</li>
<li>Fixed a bug in the Online Monitoring screen of Service Center that caused Timers with no schedule to have their Next Run date set to "01-01-3000". (RPC-681)</li>
<li>Improved the performance of LifeTime synchronization process. (RLIT-3553)</li>
<li>Fixed an issue that was blocking the generation of mobile apps in some specific cases. (RLIT-3508)</li>
<li>Fixed an issue that could cause some screens to be incorrectly accessed outside of an internal network. (RLIT-3457)</li>
<li>Fixed authorization checks during module publication events that generate some error logs. (RPC-691)</li>
<li>Fixed an issue that was preventing the display of the icon to download the mobile generation log. (RLIT-3443)</li>
<li>Fixed an issue with DateTime data type in Input widget which prevented submitting valid DateTimes on iOS. (RPD-2841)</li>
<li>Now a True Change error tells you if there's an invalid sort expression in Reactive Table. Previously such an invalid expression broke the publishing step. (RTAF-1981)</li>
<li>Fixed an issue that prevented the logging database from being created or updated a second time when the platform database wasn't previously initialized. (RSAT-1907)</li>
<li>Fixed an issue that was preventing mobile apps with special characters in their names from installing on iOS. (RNMT-3842)</li>
<li>Fixed an issue that caused the lost of Client Variables values every time an iOS mobile app built with MABS 6 initializes. (RTAF-2213)</li>
<li>Added missing logging information to the Configuration Tool to help troubleshoot issues in database upgrade operations. (RPC-818)</li>
<li>Fixed an issue in Service Center Analytics that was causing the generation of empty Queries Performance reports. (RPC-862)</li>
<li>Fixed the timeout calculation of compilation operations. (RPC-679)</li>
<li>Fixed an issue that was preventing some environment runtime settings to be applied. Now you must use the new "Apply Settings to the Factory" button in Service Center to apply those settings. (RPD-3795)</li>
<li>Fixed an issue that caused a runtime error while using the ListClear action on the list of an Aggregate. (RPD-4566)</li>
<li>Fixed a compiler crash when introspecting the database index without the corresponding column. This fix makes the staging of apps between environments more resilient. (RPD-4602)</li>
<li>Improved the performance of Solution_Edit screen in Service Center. (RPD-3912)</li>
<li>Fixed a bug where granting/revoking Roles in the Mobile and Reactive Web apps failed to be sent immediately to the client-side cookie. The roles cookie is now updated during the next server call. (RPC-626)</li>
<li>Corrected the permissions for DBConnections and DBCatalogs screens so they can be accessed with the same permission level, i.e, "Monitor and Reference Applications" or higher. (RLIT-2977)</li>
<li>We improved the Error_Log screen search experience by allowing you to reduce the timeouts in large factories. You can now use a checkbox to enable the search of the stack trace, as it's no longer enabled by default. (RPD-2538)</li>
<li>Fixed an issue that caused Scheduler Service errors while using  Processes or Emails in an Environment with multiple Deployment Zones and using an Oracle platform database. (RSBO-1211)</li>
<li>Fixed a bug that occurred while using Multiple Database Catalogs (MDC) that caused a Wait activity to crash due to a missing database catalog prefix. (RSBO-1210)</li>
<li>Fixed the count of Internal Users, for licensing purposes, when there are inactive Users. (RSBO-1251)</li>
<li>Fixed a compilation error when importing SOAP Web Services containing choices with repeated element names and complex types defined inline. (RSBO-1117)</li>
<li>The Configuration Tool no longer incorrectly overrides the Logging Database configuration with the Platform Database configuration when using TNS Names. (RPD-4201)</li>
<li>We fixed a logging issue after Platform upgrade, related to the Configuration Tool. The Configuration Tool config files weren't upgraded fully, preventing errors to be logged. (RSAT-1930)</li>
<li>Is now possible in SOAP to have a  simpleContent with an extension element inside.

(RPD-4624)</li>
<li>Fixed OS Traces template in Factory Configuration. (RPD-4638)</li>
<li>Fixed a bug that occurred while editing several rows in an Editable Table in quick succession that caused the table to show wrong data. (RPD-4745)</li>
<li>Fixed issue that prevented debugging while using multiple tabs in Service Studio. (RPD-4979)</li>
<li>Fixed an optimization bug that caused a compilation error while publishing a Module with Service Actions that don't query a database. (RPD-4695)</li>
<li>Fixed an error that stopped publishing a solution with more than 1000 Modules in an environment with an Oracle platform database. (RPD-4773)</li>
<li>Improved cleanup operations when upgrading to this version and there are custom "Protect" delete rules affecting OutSystems metamodel entities. (RPC-1086)</li>
<li>Fixed a bug that could crash an app while accessing a list leading to an Internal Error with a "Duplicate is not a valid operation inside a StartIteration/EndIteration block" logged error message. (RPC-977)</li>
<li> Fixed an issue with the "Retry" and "Skip" buttons of activities with errors in Service Center&gt;Monitoring&gt;Processes. (RPC-737)</li>
<li>Fixed slow first-time loading of apps that have a large appSettings.config file. (RPC-870)</li>
<li>Fixed an incorrect warning of no permissions when changing the Site Property value of a module. (RLIT-3442)</li>
<li>Fixed a problem synchronizing roles in a hybrid infrastructure on Cloud, when a new on-premises OutSystems 11 environment is added. (RLIT-3452)</li>
<li>Fixed an issue in input parameters of Service Actions with Decimal data type when the precision is longer than 14 digits. (RSBO-1194)</li>
<li>Fixed Mobile Generation Logs screen to only show the Applications the user has access to.
Fixed Applications screens to only allow access to users that have access to the Application. (RPD-4800)</li>
<li>Fixed a security issue that allowed decrypting sensitive information. CVSSv3.0 score 5.3 (Medium). (RLIT-3562)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RDEV-2256)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.8.0"><span id="Known_Issues_8"></span><h3 id="Known_Issues_6">Known Issues</h3>
<ul>
<li> Publishing Mobile apps that use local storage may take longer than usual or fail due to a timeout.<br/>
The runtime behavior of these apps may also be affected if the apps are opened in a browser, using PWA or Preview in Devices.<br/>
To overcome this issue, use <a class="link-https" href="https://www.outsystems.com/forge/component-overview/25/factory-configuration" rel="external noopener nofollow" target="_blank">Factory Configuration</a> to disable "IndexedDB For Local Storage data on PWAs/Browsers".</li>
</ul>
<br/>
<p><b>Disclaimer: </b><i>QR CODE is a registered trademark of Denso Wave Incorporated.</i></p>
</div></div><span id="Platform_Server_11.7.6"></span><h2 id="Platform_Server_11.7.6">Platform Server 11.7.6</h2><br/><div class="mt-include" id="s32969">
<div class="info"><p>Released on Apr 27, 2021</p></div>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that  could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li> Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</div><span id="Platform_Server_11.7.3"></span><h2 id="Platform_Server_11.7.3">Platform Server 11.7.3</h2><br/><div class="mt-include" id="s28503">
<div class="info"><p>Released on Feb 17, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.3"><span id="Bug_Fixing_23"></span><h3 id="Bug_Fixing_21">Bug Fixing</h3>
<ul>
<li>Fixed error when resetting Authentication configuration in the Users application after upgrading from previous Platform Server 11.7.x versions. (RSBO-1110)</li>
<li>Fixed an issue in Configuration Tool when there's an incomplete SAML configuration, occurring in Oracle Databases. (RSBO-1222)</li>
<li>Fixed an issue that caused a link that should open a popup window would not work depending of the order of the widgets. (RTAF-2216)</li>
<li> Fixed an issue with the "Retry" and "Skip" buttons of activities with errors in Service Center&gt;Monitoring&gt;Processes. (RPC-737)</li>
<li>Fixed an optimization bug that caused a compilation error while publishing a Module with Service Actions that don't query a database. (RPD-4695)</li>
<li>Mitigates MySQL connector bug by not disposing SQL commands. (RPD-4782)</li>
<li>Headers are now sent in consumed SOAP Web Services requests. (RSBO-1040)</li>
<li>Fixed an issue that occurred while deleting applications. CVSS v3.0 score 3.8 (Low). (RPC-607)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 9.1 (Critical). (RLIT-3368)</li>
</ul>
</div></div><span id="Platform_Server_11.7.2"></span><h2 id="Platform_Server_11.7.2">Platform Server 11.7.2</h2><br/><div class="mt-include" id="s28492">
<div class="info">
<p>Released on Jan 20, 2020</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.2"><span id="Bug_Fixing_24"></span><h3 id="Bug_Fixing_22">Bug Fixing</h3>
<ul>
<li>Fixed the triggering of the onclick event with a Rich Widget Popup Editor on a Screen/Block that would cause the onclick event handlers of its parents to trigger during the screen rendering. (RTAF-2089)</li>
</ul>
</div></div><span id="Platform_Server_11.7.1"></span><h2 id="Platform_Server_11.7.1">Platform Server 11.7.1</h2><br/><div class="mt-include" id="s28387">
<div class="info">
<p>Removed from availability on Jan 20, 2020</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.1"><span id="Bug_Fixing_25"></span><h3 id="Bug_Fixing_23">Bug Fixing</h3>
<ul>
<li>Fixed a bug related to the Rich Widgets Pop-Up pattern and the List Bulk Select widget, where a link/button triggered a pop-up and had the link/button associated with the List Bulk Select widget. (RTAF-2062)</li>
<li>Fixed the multiple executions of Screen Preparation Action that occurred when you used Rich Widgets File Upload in the Screen. (RTAF-2064)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.1"><span id="Known_Issues_9"></span><h3 id="Known_Issues_7">Known Issues</h3>
<ul>
<li>In Screens or Blocks with a nested Popup_Editor Rich Widget, the onclick event handlers of its parents can be triggered during the screen rendering, leading to unexpected runtime behavior.</li>
</ul>
</div></div><span id="Platform_Server_11.7.0"></span><h2 id="Platform_Server_11.7.0">Platform Server 11.7.0</h2><br/><div class="mt-include" id="s28350">
<div class="info">
<p>Removed from availability on Jan 17, 2020</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.0"><span id="New_in_Platform_Server_11.7.0"></span><h3 id="New_in_Platform_Server_11.7.0">New in Platform Server 11.7.0</h3>
<ul>
<li>It is now possible to consume REST APIs using Swagger specifications that have enum elements. (RSBO-872)</li>
<li>Added support for accent-sensitive Linguistic sorts on Oracle databases. (RSAT-1844)</li>
<li>You can now distribute your app as a Progressive Web App (PWA). Start by enabling this early access feature in LifeTime. Then, create a mobile or tablet app, publish it, navigate to the "Distribute" tab and toggle on "Distribute as the PWA" (no republish needed). You can try your PWA out by installing it through Android Chrome and iOS Safari. The <a href="https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Distribute_as_a_progressive_web_app" rel="internal">early access PWA documentation</a> explains how to enable PWA on iOS 13, as well as how to edit the manifest. Check also the blog post. Have fun and share your feedback with us on the forum! (RTAF-1831)</li>
<li>Service Center has a new look and feel, among with several improvements and bug fixes:<br/>
- Added search ability to dropdowns with long lists, such as modules in filters<br/>
- Replaced filters and navigation actions from submit to ajax submit<br/>
- Improved responsiveness in mobile devices<br/>
- Revamped Operation (publish/upload/download/apply settings) pages, now showing collapsible lines and displaying the status for each main step<br/>
- Replaced references to "Module" in Monitoring screens by "Source" to avoid confusion with the actual "Module"<br/>
- Added Applications to the search results screen<br/>
- Added auto refresh ability in the Timer detail screen when the timer is running<br/>
- Added links to Solution detail screen in Modules detail screen Solutions tab<br/>
- Added date picker to date filters in Reports and Daily History Screens<br/>
- Added a confirmation message in "apply settings" action in the Solution detail Screen<br/>
- Added a confirmation message when downloading an application with broken or outdated references, in Application detail screen<br/>
- Fixed “Check all modules" option not working in Solution detail screen<br/>
- Fixed “Uploaded by me” filter in Extensions list page not working<br/>
- Fixed Analytics and Administration menu entries not allowing opening in new tabs (RLIT-2821)</li>
<li>Improved the accessibility features of several Rich Widgets, for better WCAG compliance. (ROU-576)</li>
<li>Added new parameters to the Configuration Tool Command-Line Interface (CLI). These parameters (/EnableServerAPI and /DisableServerAPI) allow users to enable and disable Server.API and Server.Identity. (RPC-79)</li>
<li>The Platform Server releases now follow a new versioning format. Check <a class="link-https" href="https://www.outsystems.com/forums/discussion/56089/platform-server-now-follows-the-new-versioning-format/" rel="external noopener nofollow" target="_blank">this forum post</a> for more information about this change.<br/>
Factory Configuration was also updated to version 11.0.4 to be compatible with the new versioning. (RRET-1269)</li>
<li>Added three optional input parameters to configure additional Cookie settings in HTTPRequestHandler. (RTAF-1774)</li>
<li>End-users of OutSystems applications are now classified as Internal Users or External Users, based on the domain of their email addresses. You can configure the classification rules in the Licensing screen of Service Center. (RSBO-1016)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.0"><span id="Bug_Fixing_26"></span><h3 id="Bug_Fixing_24">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was incorrectly triggering the "Required Field" validation message for a Button Group. (RPD-3591)</li>
<li>The QR code to test a mobile app using OutSystems Now wasn't being generated when the URL contained special characters (e.g. ç, à, á, í, etc). (RPD-4435)</li>
<li>Fixed a compilation error after deleting all Client Variables from a module. (RTAF-1610)</li>
<li>Fixed an issue in SEO Friendly URLs that was preventing new alias rules for modules to work properly in Oracle stack. (RPD-4436)</li>
<li>Fixed a runtime error when using Server actions in Exception Handlers. (RTAF-1672)</li>
<li>We fixed the compilation of a Screen Aggregate for local storage Entities with a dynamic sort. (RTAF-1645)</li>
<li>Fixed an issue that caused any module that had anywhere in the name "template_" to be registered as a template. (RTAF-1846)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.0 score 4.1 (Medium). (RPD-4389)</li>
<li>Fixed triggering of On Scroll Ending in Reactive List Widget. We also improved the rendering of the elements inside lists. (RTAF-1805)</li>
<li>Fixed the automatic refresh of references that wasn't triggered after publishing the latest version of a module in an environment with Deployment Controller role only. (RPC-172)</li>
<li>Fixed cache invalidation service installation messages to avoid unnecessary output text when creating folders. (RPC-449)</li>
<li>Fixed the "Submit Feedback" screen displayed when opening the "Edit Site Property" screen in Service Center without any inputs. It now correctly displays the "Not Found" page. (RPC-450)</li>
<li>Fixed issue that caused unnecessary error logs to be generated during Service Center operations. (RPC-319)</li>
<li>Removed unnecessary accesses to the session database that could happen on Reactive Applications and REST Services. (RPC-347)</li>
<li>Fixed the search when looking for apps to configure AppFeedback so Reactive Apps that have AppFeedback enabled show in the configuration screen. (RTAF-1766)</li>
<li>Fixed multiple error logs being generated when there were problems rendering EPA Taskbox or App Feedback elements. (RPC-286)</li>
<li>Fixed a compiler error when using a local Screen variable in a complex Dynamic Sort of a Screen Aggregate. (RTAF-1740)</li>
<li>Now in a Solution detail screen in Service Center, both the list of Components and the list of Dependencies are ordered alphabetically. (RPD-4176)</li>
<li>The database scripts of the Configuration Tool now take into account schema owners in Oracle databases. (RPD-4468)</li>
<li>Now in Service Center, all search results are shown in alphabetical order. (RLIT-2057)</li>
<li>Fixed cross-site scripting vulnerability. CVSSv3.0 score 4.8 (Medium). (RLIT-3164)</li>
<li>Fixed an issue that could cause Configuration Tool to fail when installing over Azure SQL databases. (RSAT-1868)</li>
<li>Added a server.hsconf parameter named "ServiceInitializationTimeoutInSeconds" to configure the default timeout of services restart (in seconds) for the Configuration Tool. The default value is 180 seconds. (RSAT-1790)</li>
<li>It is now possible to use Unicode Support toggle in advanced configurations for SQL Server external database connections. (RPD-3665)</li>
<li>Fixed the scenarios where the "Add Query Origin to Generated SQL" setting wasn't applied. (RSBO-498)</li>
<li>Fixed the ISAPI filters for a pure controller farm scenario. (RPD-4124)</li>
<li>Improved the performance of ECT_Provider with a big number of user groups. (RPD-4407)</li>
<li>The integration logs now use an updated SOAP service endpoint when changed on a callback. (RPD-4585)</li>
<li>Fixed a crash publishing a solution with two-stage deployment when the solution contains modules that belong also to another solution that was previously prepared for deploy. (RPD-4502)</li>
<li>Fixed a compilation error caused by the implicit conversion of Client Variable. The error happened despite the fact the types were compatible. (RTAF-1506)</li>
<li>Fixed the Service Center application pool crashes in error request scenarios. (RPD-4486)</li>
<li>We fixed a memory performance issue related to Aggregates, SQL elements, and Entity Actions. The connection objects in the generated source code by the platform are now correctly disposed of and do not take up the resources. (RPD-4443)</li>
<li>Fixed a security vulnerability that allowed an adversary to know if a user with a given username exists in the OutSystems Platform. CVSS3.0 score of 5.3 (Medium). (RSAT-1818)</li>
<li>Fixed an issue in Platform Server installer that prevented the installation process due to inability to detect Microsoft Build Tools with Update 1 or with Update 2. (RSAT-1855)</li>
<li>Fixed share folders being deleted between the first stage and the second stage of a solution publish when a module is being published for the first time. (RPD-4503)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.0"><span id="Breaking_Change_3"></span><h3 id="Breaking_Change_3">Breaking Change</h3>
<ul>
<li>Upgraded SharpZipLib library to version 1.1.0. It is recommended to test application features related to Zip and Excel files. Note that third party-Excel components based on old versions of NPOI may need to be upgraded to work correctly. (RRCT-2368)</li>
</ul>
</div><div class="mt-section" id="section_4" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.7.0"><span id="Known_Issues_10"></span><h3 id="Known_Issues_8">Known Issues</h3>
<ul>
<li>When using the File Upload Rich Widget in a Screen that includes assigns to local variables shared between Preparation and OnNotify actions, Preparation runs multiple times, which may result in data corruption or unexpected runtime behavior.</li>
</ul>
<p> </p>
<p><b>Disclaimer: </b><i>QR CODE is a registered trademark of Denso Wave Incorporated.</i></p>
<p> </p>
</div></div><span id="Platform_Server_11.0.615"></span><h2 id="Platform_Server_11.0.615">Platform Server 11.0.615</h2><br/><div class="mt-include" id="s32968">
<div class="info">
<p>Released on Apr 27, 2021</p>
</div>
<ul>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High). (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
</div><span id="Platform_Server_Release_Oct.2019_CP6"></span><h2 id="Platform_Server_Release_Oct.2019_CP6">Platform Server Release Oct.2019 CP6</h2><br/><div class="mt-include" id="s28501">
<div class="info"><p>Released on Jan 20, 2020</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP6"><span id="Bug_Fixing_27"></span><h3 id="Bug_Fixing_25">Bug Fixing</h3>
<ul>
<li>Fixed an error that showed that triggered an onclick event when a nested Rich Widget Popup Editor was present. (RTAF-2089)</li>
</ul></div></div><span id="Platform_Server_Release_Oct.2019_CP5"></span><h2 id="Platform_Server_Release_Oct.2019_CP5">Platform Server Release Oct.2019 CP5</h2><br/><div class="mt-include" id="s28484">
<div class="info">
<p>Removed from availability on Jan 20, 2020</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP5"><span id="Bug_Fixing_28"></span><h3 id="Bug_Fixing_26">Bug Fixing</h3>
<ul>
<li>Fixed an error that showed when using the Rich Widgets Pop-Up pattern with the List Bulk Select widget, where a link/button triggered a pop-up and had the link/button associated with the List Bulk Select widget. (RTAF-2062)</li>
<li>Fixed the multiple executions of Screen Preparation Action that occurred when you used Rich Widgets File Upload in the Screen. (RTAF-2064)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP5"><span id="Known_Issues_11"></span><h3 id="Known_Issues_9">Known Issues</h3>
<ul>
<li>In Screens or Blocks with a nested Popup_Editor Rich Widget, the onclick event handlers of its parents can be triggered during the screen rendering, leading to unexpected runtime behavior.</li>
</ul>
</div></div><span id="Platform_Server_Release_Oct.2019_CP4"></span><h2 id="Platform_Server_Release_Oct.2019_CP4">Platform Server Release Oct.2019 CP4</h2><br/><div class="mt-include" id="s28271">
<div class="info">
<p>Removed from availability on Jan 17, 2020</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP4"><span id="New_in_Platform_Server_Release_Oct.2019_CP4"></span><h3 id="New_in_Platform_Server_Release_Oct.2019_CP4">New in Platform Server Release Oct.2019 CP4</h3>
<ul>
<li>Added new environment security options to force Secure and SameSite properties in cookies generated by the platform. Check the document <a href="https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Upcoming_changes_in_cookie_handling_in_Google_Chrome#Release_schedule" rel="internal">Upcoming changes in cookie handling in Google Chrome</a> for more information. (RPC-502)</li>
<li>Added three optional input parameters to configure additional Cookie settings in HTTPRequestHandler. (RTAF-1774)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP4"><span id="Bug_Fixing_29"></span><h3 id="Bug_Fixing_27">Bug Fixing</h3>
<ul>
<li>Fixed a security vulnerability. CVSSv3.0 score 7.2 (High). (RPD-4310)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 7.6 (High). (RPD-4260)</li>
<li>Fixed an issue that occurred while deleting applications. CVSS v3.0 score 3.8 (Low). (RPC-607)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP4"><span id="Known_Issues_12"></span><h3 id="Known_Issues_10">Known Issues</h3>
<ul>
<li>When using the File Upload Rich Widget in a Screen that includes assigns to local variables shared between Preparation and OnNotify actions, Preparation runs multiple times, which may result in data corruption or unexpected runtime behavior.</li>
</ul>
</div></div><span id="Platform_Server_Release_Oct.2019_CP3"></span><h2 id="Platform_Server_Release_Oct.2019_CP3">Platform Server Release Oct.2019 CP3</h2><br/><div class="mt-include" id="s27775">
<div class="info"><p>Released on Nov 25, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP3"><span id="New_in_Platform_Server_Release_Oct.2019_CP3"></span><h3 id="New_in_Platform_Server_Release_Oct.2019_CP3">New in Platform Server Release Oct.2019 CP3</h3>
<ul>
<li>Added support for Oracle 19c. This applies to the platform database, as well as external databases. (RSAT-1859)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP3"><span id="Bug_Fixing_30"></span><h3 id="Bug_Fixing_28">Bug Fixing</h3>
<ul>
<li>Fixed an issue in SEO Friendly URLs that was preventing new alias rules for modules to work properly in Oracle stack. (RPD-4436)</li>
<li>Fixed an issue that was incorrectly triggering the "Required Field" validation message for a Button Group. (RPD-3591)</li>
<li>We fixed the compilation of a Screen Aggregate for local storage Entities with a dynamic sort. (RTAF-1645)</li>
<li>Fixed share folders being deleted between the first stage and the second stage of a solution publish when a module is being published for the first time. (RPD-4503)</li>
<li>Fixed a crash publishing a solution with two-stage deployment when the solution contains modules that belong also to another solution that was previously prepared for deploy. (RPD-4502)</li>
<li>Command objects are now disposed in generated code for Aggregates, SQL elements, and Entity Actions. (RPD-4443)</li>
<li>Fixed Service Center application pool crashes in error request scenarios. (RPD-4486)</li>
</ul> </div></div><span id="Platform_Server_Release_Oct.2019_CP2"></span><h2 id="Platform_Server_Release_Oct.2019_CP2">Platform Server Release Oct.2019 CP2</h2><br/><div class="mt-include" id="s27332">
<div class="info"><p>Released on Nov 07, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP2"><span id="New_in_Platform_Server_Release_Oct.2019_CP2"></span><h3 id="New_in_Platform_Server_Release_Oct.2019_CP2">New in Platform Server Release Oct.2019 CP2</h3>
<ul>
<li>Added support for Oracle 18c. This applies both to the platform database and to external databases. (RSAT-1860)</li>
<li>It's now possible to use Client Variables in Aggregates. (RTAF-1334)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP2"><span id="Bug_Fixing_31"></span><h3 id="Bug_Fixing_29">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was preventing mobile apps from installing on iPadOS 13. (RNMT-3294)</li>
<li>Button Group widget now gets the selected value style when the value's data type is different from text or number. (RTAF-1260)</li>
<li>Removed unnecessary audits from the TemplateManager module that could cause high number of requests after solution publications. (RPC-285)</li>
<li>The Table in Reactive Web now highlights which column is being sorted. (RTAF-1413)</li>
<li>Fixed issues with applying configurations, finalizing solutions, and apps publication in environments with a high number of modules. (RPC-355)</li>
<li>Fixed an issue preventing users of different tenants from submitting feedback. (RPD-4419)</li>
<li>Fixed Scheduler service to make it more resilient to being stopped while it is still processing jobs or with queued jobs to be processed. (RPD-4356)</li>
<li>Fixed an issue with Platform license becoming invalid in after machine restarts in recent versions of Windows due to serial number changing. (RPD-4216)</li>
<li>Improves performance of ECT_Provider when we have huge number of user groups. (RPD-4407)</li>
<li>Fixed an issue in the "LDAP_Search" action, included in the Authentication extension of the Users application, that was limiting the returned results to a maximum of 1000 entries. (RPD-4379)</li>
<li>Fixed redirecting users to the Service Center homepage when trying to view a module detail with an External Authentication provider enabled. (RPC-445)</li>
<li>Fixed a compilation error when publishing a solution with applications using a custom user provider that is not included in the solution and has compatibility issues. If the user provider is either missing in the environment or it is incompatible, you will now get a warning about this situation. (RPD-4368)</li>
<li>Fixed compilation error when an effective user provider is not included in a solution. (RPD-4361)</li>
<li>Fixed last_login not being updated when users login in Mobile Applications or from within a Web Service request. (RPD-4332)</li>
<li>Fixed the error "Circular attribute group reference" when executing the XMLDocument_Load action of the Xml extension. (RPD-3742)</li>
<li>Optimized Configuration Tool load time on scenarios where the database does not exist. (RSAT-1787)</li>
<li>Fixed incorrect tenant for eSpaces using an overridden effective user provider. (RPD-4377)</li>
</ul></div></div><span id="Platform_Server_Release_Oct.2019_CP1"></span><h2 id="Platform_Server_Release_Oct.2019_CP1">Platform Server Release Oct.2019 CP1</h2><br/><div class="mt-include" id="s27287">
<div class="info"><p>Released on Oct 09, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP1"><span id="Bug_Fixing_32"></span><h3 id="Bug_Fixing_30">Bug Fixing</h3>
<ul>
<li>We deactivated the data fetching optimization in Reactive Web Apps, after identifying a severe issue. If you are using Platform Server 11 Release Oct.2019 we strongly advise that you upgrade Platform Server and republish your apps, as instructed in the Installation Checklist. (RTAF-1537)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019_CP1"><span id="Known_Issues_13"></span><h3 id="Known_Issues_11">Known Issues</h3>
<ul>
<li>When using an External Authentication provider (Active Directory or LDAP), if a user tries to view the details of a module in Service Center, he is redirected to the Service Center homepage.</li>
</ul></div></div><span id="Platform_Server_Release_Oct.2019"></span><h2 id="Platform_Server_Release_Oct.2019">Platform Server Release Oct.2019</h2><br/><div class="mt-include" id="s26778">
<div class="info"><p>Released on Oct 02, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019"><span id="New_in_Platform_Server_Release_Oct.2019"></span><h3 id="New_in_Platform_Server_Release_Oct.2019">New in Platform Server Release Oct.2019</h3>
<ul>
<li>You can now create a new type of app, <a class="link-https" href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30195" rel="external noopener nofollow" target="_blank">Reactive Web App</a>. This type of app is based on the client-side development paradigm. Reactive App comes with its own new features: Table Widget, server-side pagination, and Public Screens. (RTAF-115)</li>
<ul>
<li style="margin-left:35px;">
<a class="link-https" href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30198" rel="external noopener nofollow" target="_blank">Table Widget</a>, available in the <a class="link-https" href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30195" rel="external noopener nofollow" target="_blank">Reactive Web</a> apps, comes with an accelerator: drag an Entity on it to create a table with sorting and pagination. Use tables to show data in cells distributed in rows and columns. (RTAF-204)</li>
<li style="margin-left:35px;">Use the server-side pagination feature of the Screen Aggregates to build faster apps that need to handle large data sets. Enter the Start Index and fetch the number of records you define in Max Records. (RTAF-630)</li>
<li style="margin-left:35px;">Public Screens will allow you to reuse UI across different Reactive Web modules and apps. Because the UI can be modular, you can now have more complex UI modules that you can maintain efficiently. You can collaborate better without merge conflicts, as one team can be working on the logic module, while the other is updating the UI module. (RTAF-198)</li>
<li style="margin-left:35px;">Download Tool is available in Reactive Apps. Now you can drag a Download Tool to your Flow and create a node which, when executed, sends a file for download to the end-user. (RTAF-993)</li>
</ul>
<li>You can now create <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Reuse_and_Refactor/Libraries" rel="internal">Libraries</a> in Mobile and Reactive Web apps. This new module type is especially tailored for building highly reusable logic and UI and fits directly in the Foundation layer of the 4 Layer Canvas. (RSBO-708)</li>
<li>The checklist and documentation instruction links now include the required steps for the Microsoft .NET Core 2.1 Windows Server Hosting. Additionally, the recommended version has been raised to 2.1.12. (RPC-254)</li>
<li>Improved the solution publication messages regarding the database update to have more details about each step (RRCT-2429)</li>
<li>We improved Data Sources and made asynchronous data fetching straightforward to use in Mobile and Reactive Apps. Screen Aggregates and Data Actions are now available in the scope of other Screen Aggregates and Data Actions. We also added the Fetch property with On Start and On Demand options. Now you can <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Query_Data/Implement_asynchronous_data_fetching_using_Aggregates" rel="internal">implement patterns such as master/detail</a> with an excellent performance and user experience. (RTAF-990)</li>
<li>Now you can create <a href="https://success.outsystems.com/Documentation/11/Reference/OutSystems_Language/Data/Handling_Data/Client_Variable" rel="internal">Client Variables</a> in Mobile and Reactive Apps. Use Client Variables to store Basic Data Types locally or share the values across apps through public Blocks and public Client Actions. (RTAF-1051)</li>
<li>The <a class="link-https" href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30208" rel="external noopener nofollow" target="_blank">Dropdown Widget</a> has a new property Options Content, which you can set to Text Only or Custom. Text Only gives a native look and feel of the drop-down lists in your Reactive and Mobile apps. Use Options Content property set to Custom to build a list of images or other Widgets. (RTAF-1207)</li>
<li>Button Widgets in Mobile and Reactive Apps now have the Is Form Default property, which you can set to Yes and make the App submit the data from the related form when the end-user presses the Enter key. (RTAF-652)</li>
<li>The Users application now includes specific configurations for OKTA, for authenticating the end-users of your OutSystems applications. (RSBO-791)</li>
<li>Added Server.Identity service to support platform authentication. (RPC-82)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019"><span id="Bug_Fixing_33"></span><h3 id="Bug_Fixing_31">Bug Fixing</h3>
<ul>
<li>Fixed a bug on Mobile Cookies validations where the HTTP response would return an internal error instead 403 status code (Forbidden)  (RRCT-2601)</li>
<li>Improved some queries during Service Center publication to avoid timeouts on large factories. (RRCT-2598)</li>
<li>Fixed the recovery of connections to the cache invalidation service after the RabbitMQ server is restarted or the connection is lost. (RRCT-2509)</li>
<li>Fixed a concurency problem when stopping OutSystems services that could cause a large amount of errors to be sent to the event viewer logs. (RRCT-2510)</li>
<li>Fixed misbehavior when using confirmation message with pop-up editor screens. (RPD-4242)</li>
<li>Fixed an issue that prevented mobile applications from loading in Production environments when a producer module was published in Debug mode. (RPD-3596)</li>
<li>Fixed an issue where JPEG images (of type database in OutSystems application) would not correctly render in IE11. (RPD-4363)</li>
<li>Configuration Tool is able to proceed installation when the logging database is in availability group (SQL Server only) (RPD-4257)</li>
<li>Fixed an issue that caused the configuration of the internal network to block the access from the IP sources that match both the trusted proxies addresses and the internal network addresses. (RPD-4362)</li>
<li>NLS_LANGUAGE field is now also available while in advanced mode for Oracle external database connections (RPD-3717)</li>
<li>Fixed a crash in 1-Click Publish when the trace log level for the Deployment Controller Service was set to 4 (Debug). (RSCT-2054)</li>
<li>Fixed a problem when compiling modules if they contain widgets whose width or margin properties are not in a numeric format. (RTAF-1054)</li>
<li>Fixed stored procedure DEQUEUE_EMAILS_FOR_FRONTEND so it doesn't return duplicate email statuses in farm scenarios. (RPD-4350)</li>
<li>Fixed compilation problem in modules with a large number of entities in Oracle. (RPD-4268)</li>
<li>Fixed an issue that caused LifeTime Analytics to have no data on newly created applications. (RPC-177)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019"><span id="Breaking_Change_4"></span><h3 id="Breaking_Change_4">Breaking Change</h3>
<ul>
<li>Upgraded Oracle Data Provider for .NET, Managed driver to version 19.3.1 (4.122.19.1:20190703).

According to the <a class="link-https" href="https://docs.oracle.com/en/database/oracle/oracle-database/19/odpnt/InstallSystemRequirements.html#GUID-A6405CAD-C0E9-45E0-9C38-26B7ED214479" rel="external noopener nofollow" target="_blank">official documentation</a>, this driver allows applications to connect to Oracle Database 11g Release 2 or later.<b>If you have integrations with earlier versions of Oracle Database, they will not work. You will need to upgrade your Oracle engine to version 11g Release 2 or later, in order to continue using those integrations.</b>

This driver supports native encryption, meaning that you can set up your database to require encryption and this means all connections will be encrypted between the server and the database (applicable for the platform and external databases). (RSAT-1723)</li>
</ul>
</div><div class="mt-section" id="section_4" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Oct.2019"><span id="Known_Issues_14"></span><h3 id="Known_Issues_12">Known Issues</h3>
<ul>
<li>When using an External Authentication provider (Active Directory or LDAP), if a user tries to view the details of a module in Service Center, he is redirected to the Service Center homepage.</li>
</ul> </div></div><span id="Platform_Server_Release_Jul.2019_CP2"></span><h2 id="Platform_Server_Release_Jul.2019_CP2">Platform Server Release Jul.2019 CP2</h2><br/><div class="mt-include" id="s26662">
<div class="info"><p>Released on Aug 23, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Jul.2019_CP2"><span id="New_in_Platform_Server_Release_Jul.2019_CP2"></span><h3 id="New_in_Platform_Server_Release_Jul.2019_CP2">New in Platform Server Release Jul.2019 CP2</h3>
<ul>
<li>The installation checklist now includes the instructions to disable Adaptive Optimizer features (OPTIMIZER_ADAPTIVE_PLANS, OPTIMIZER_ADAPTIVE_STATISTICS) in Oracle 12c R2. (RSAT-1623)</li>
<li>The Users application now supports SAML 2.0 authentication out of the box, including specific configurations for Azure AD, for authenticating the end-users of your OutSystems applications. (RSBO-540)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Jul.2019_CP2"><span id="Bug_Fixing_34"></span><h3 id="Bug_Fixing_32">Bug Fixing</h3>
<ul>
<li>Fixed brute force login check that blocked all logins behind a proxy when the X-Forwarded-For header field included a port number. (RPD-4272)</li>
<li>Fixed issue so inputs inside forms properly create an anchor element with text (conforming with WCAG21 AAA). (RPD-4274)</li>
<li>Fixed the installation with OEM licenses to allow installation of the Forge components from the installation checklist. (RPD-4276)</li>
<li>Fixed Platform DB recovery mode being set to Simple when the same DB is used for both Platform and Logging. (RPD-4282)</li>
</ul></div></div><span id="Platform_Server_Release_Jul.2019_CP1"></span><h2 id="Platform_Server_Release_Jul.2019_CP1">Platform Server Release Jul.2019 CP1</h2><br/><div class="mt-include" id="s26504">
<div class="info">
<p>Released on Jul 25, 2019</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Jul.2019_CP1"><span id="New_in_Platform_Server_Release_Jul.2019_CP1"></span><h3 id="New_in_Platform_Server_Release_Jul.2019_CP1">New in Platform Server Release Jul.2019 CP1</h3>
<ul>
<li>Added support for TLS 1.1 and TLS 1.2 on MySQL external database connections. Warning: OutSystems now distributes BouncyCastle (v1.8.3) and Google.Protobuf (v.3.6.1.0) alongside the MySQL driver - this may impact the existing extensions that use different versions. (RSAT-1258)</li>
<li>Downloading a mobile app by scanning the QR code in Service Studio is now possible on iOS 13. (RTAF-628)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Jul.2019_CP1"><span id="Bug_Fixing_35"></span><h3 id="Bug_Fixing_33">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented some Dependencies to be added in Search in other Modules. (RDEV-413)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 7.5 (High). (RNMT-2812)</li>
<li>Fixed an issue in the Spanish translation of RichWidgets. (RPD-3132)</li>
<li>Fixed compilation error that occurred when SOAP Faults were using types based on the .NET CLR (Common Language Runtime). (RPD-3979)</li>
<li>Fixed bug where attributes of structures created by an Integration Plugin which had default values could not be consumed in another module. (RPD-3862)</li>
<li>Fixed compilation error when removing Entity or Structure attributes that are still used in consumer modules. (RSBO-630)</li>
<li>Description of entities using Japanese characters will be saved using Unicode correctly after first publish. (RPD-4258)</li>
<li>Fixed incorrect advanced query GetUsersByRoleId in the Users application. (RPD-4220)</li>
<li>Fixed missing producers when consuming/refreshing references while logged in using a composite user name (domain\username). (RPD-4185)</li>
<li>Fixed an issue in 1-Click Publish when a module is renamed changing only the case (e.g. from ModuleName to ModuleNAME), which was causing the module to be incorrectly undeployed. (RSCT-2042)</li>
<li>Fixed an issue in the pre-requisites checking stage of the Platform Server installer so it doesn't fail for Windows installations using Japanese language. (RPD-4212)</li>
</ul>
<br/>
<p><b>Disclaimer: </b><i>QR CODE is a registered trademark of Denso Wave Incorporated.</i></p></div></div><span id="Platform_Server_Release_Jul.2019"></span><h2 id="Platform_Server_Release_Jul.2019">Platform Server Release Jul.2019</h2><br/><div class="mt-include" id="s26435">
<div class="info">
<p>Released on Jul 11, 2019</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Jul.2019"><span id="New_in_Platform_Server_Release_Jul.2019"></span><h3 id="New_in_Platform_Server_Release_Jul.2019">New in Platform Server Release Jul.2019</h3>
<ul>
<li>Added a new option in the "Single Sign-On" tab in Service Center. It allows you to bootstrap the admin password for the user provider. (RLIT-2571)</li>
<li>When configuring a mobile application, it is now possible to choose the version of the Mobile Apps Build Service (MABS) that will be used to generate the mobile app package. (RNMT-2296)</li>
<li>It is now possible to hide mobile app upgrade notifications by setting an empty message on the "Upgrade Messages" properties of the module. (RTAF-610)</li>
<li>The Platform Server installation/update/upgrade now requires you to define the password for the Platform Server admin user, which is done via Configuration Tool. If you have any installation automation in place you will need to adjust the server configuration file (server.hsconf) or command-line options and arguments.</li>
<li>Added support for TLS 1.1 and TLS 1.2 on MySQL external database connections. Warning: OutSystems now distributes BouncyCastle (v1.8.3) and Google.Protobuf (v.3.6.1.0) alongside the MySQL driver - this may impact the existing extensions that use different versions. (RSAT-1258)</li>
<li>Added support for Windows Server 2019. (RSAT-1199)</li>
<li>Added Server.API service to enable platform operations and application lifecycle management. (RSCT-1835)</li>
<li>Minor improvements in the font and UI of the Users application. (RLIT-2592)</li>
<li>Added support for SOAP Actions containing special characters. (RSBO-384)</li>
<li>It is now possible to consume SOAP services that have sequences with duplicated elements. (RPD-3898)</li>
<li>You will need to install the latest version of the Development Environment in the Deployment Controller Server to ensure that you can benefit from the latest features and developments. This is now a <strong>required step</strong> when installing Platform Server feature patches and cumulative patches. (RSCT-1898)</li>
<li>Early access: We are working on new capabilities that will accelerate the development of web applications. (RTAF-115)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Jul.2019"><span id="Bug_Fixing_36"></span><h3 id="Bug_Fixing_34">Bug Fixing</h3>
<ul>
<li>Fixed compilation error that occurred when SOAP Faults were using types based on the .NET CLR (Common Language Runtime). (RPD-3979)</li>
<li>Fixed bug where it was not possible to use negative Ids for records of Static Entities. (RPD-3263)</li>
<li>It is now possible to consume SOAP services that have elements with spaces in the name. (RSBO-438)</li>
<li>Fixed the BPT automatic cleanup process that was marking newly created activities as closed. (RPD-3891)</li>
<li>Fixed a Service Studio crash that occurred when introspecting WSDL with types having a single attribute with the same name. (RSBO-249)</li>
<li>Fixed cache invalidations on Personal Environments (RRCT-2522)</li>
<li>Fixed an issue in Service Center that returns an error when users try to export Mobile Requests Logs. (RPD-3982)</li>
<li>The MABS version tag of a mobile application is now correctly updated in Service Center for all environments, including the ones not connected to LifeTime. (RPD-3851)</li>
<li>Fixed a permission error that caused users with Change &amp; Deploy permissions to be unable to publish a new extension with database connection entities. (RPD-4103)</li>
<li>Fixed an issue that could cause a user with the correct set of permissions to fail to publish using Integration Studio. Instead, they would get the following error "You don't have enough permissions over the database connections that own the following external entities." (RPD-4162)</li>
<li>Improved the performance of the Process Monitoring page in environments with a large number of activities. (RPD-4080)</li>
<li>Fixed an issue in AddAttributeToHtmlTag action that could lead to an ArgumentOutOfRange exception in runtime. (RPD-3931)</li>
<li>Fixed an issue that caused the scheduler to stop handling Processes for a while when updating an existing license via "ConfigurationTool /UploadLicense." (RSAT-1398)</li>
<li>Fixed error when publishing a module containing a SOAP Web Service with Structures with special names, such as Assembly. (RSBO-414)</li>
<li>Fixed an issue that caused Configuration Tool to crash when executing scripts on SQL Azure when the databases were being created. (RPD-3956)</li>
<li>Fixed ListBox widget variable being empty inside OnChange handler in specific scenarios. (RPD-3983)</li>
<li>Fixed compilation error when using aggregates with cache inside data actions. (RPD-4039)</li>
<li>Fixed a problem in the code generation of SOAP service methods containing '.' in their names. (RPD-3948)</li>
<li>Fixed a lock on a file by Compiler Service after a second stage compilation error in Service Studio publication. (RPD-4024)</li>
<li>Fixed a rare 'The process cannot access the file' error that occurred during deployments. (RPD-4166)</li>
<li>Fixed incorrect advanced query GetUsersByRoleId in the Users application. (RPD-4220)</li>
<li>Fixed an issue that would cause Configuration Tool to crash if the database was not accessible. (RSAT-1387)</li>
<li>Fixed a crash that occurred when importing SOAP Web Services that had invalid WSDL definition with missing portType elements. (RSBO-356)</li>
<li>Fixed an issue with Input_AutoComplete being triggered in IE11 due to an unexpected 'keydown' event. (RPD-3866)</li>
</ul>
</div><span id="Platform_Server_Release_Apr.2019_CP1"></span><h2 id="Platform_Server_Release_Apr.2019_CP1">Platform Server Release Apr.2019 CP1</h2><br/><div class="mt-include" id="s25840">
<div class="info"><p>Released on May 17, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Apr.2019_CP1"><span id="New_in_Platform_Server_Release_Apr.2019_CP1"></span><h3 id="New_in_Platform_Server_Release_Apr.2019_CP1">New in Platform Server Release Apr.2019 CP1</h3>
<ul>
<li>Added warning when no user is configured for Users app. Removed note saying default admin password. (RLIT-2574)</li>
<li>Added a new public action (Popup_Editor_GetMessage) to RichWidgets to get the Notify Popup message. (ROU-142)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_Release_Apr.2019_CP1"><span id="Bug_Fixing_37"></span><h3 id="Bug_Fixing_35">Bug Fixing</h3>
<ul>
<li>Fixed a problem when using ListAppend and ListInsert functions containing an If expression in the List input parameter. (RPD-3984)</li>
<li>Fixed bug where sometimes when starting the Deploy Service, applications were not deployed automatically (RSCT-1761)</li>
<li>Fixes an issue where the Viewstate did not store nested web blocks for triggered events. (RPD-4070)</li>
</ul> </div></div><span id="Platform_Server_Release_Apr.2019"></span><h2 id="Platform_Server_Release_Apr.2019">Platform Server Release Apr.2019</h2><br/><div class="mt-include" id="s25673">
<div class="info">
<p>Released on May 06, 2019</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/604_Platform_Server_Release_Apr.2019"><span id="New_in_Platform_Server_Release_Apr.2019"></span><h3 id="New_in_Platform_Server_Release_Apr.2019">New in Platform Server Release Apr.2019</h3>
<ul>
<li>Clicking Environment/Module Management in the toolbar now opens Service Center in the default browser instead of render it directly inside Service Studio. (RICT-825)</li>
<li>We changed the SQL Injection warning message to advise you not to set the use of Expand Inline option to "Yes". The warning helps to follow solid SQL security practices. (RRCT-2128)</li>
<li>Improved the experience of the Users application. We gave it a new look and feel and made the following usability improvements:<br/>
— Page-specific links/actions were moved to inside the pages; the sidebar will now only display fixed links and recent items<br/>
— Added breadcrumbs to pages and pagination and records counter to all pages showing lists<br/>
— Added text filter in users sub-lists<br/>
— When a user does not have a username defined it appears as "Not Defined" in the lists so that you can click it<br/>
— Roles, Groups and Users dropdowns don't show the records already added to the lists; however, roles still show when they were inherited by group to allow overriding<br/>
— When a role is inherited by a group, it does not show the option to remove the role, since this operation is not possible<br/>
— Added the list of users able to access the application to the Application_List page – inspired by <a class="link-https" href="https://www.outsystems.com/ideas/4962/Users+Application+Bugs%2fImprovements" rel="external noopener nofollow" target="_blank">Rebecca Hall's idea</a> (RLIT-2343)</li>
<li>Added a new action Session_GetWebAppLoginInfo to the PlatformRuntime API that allows you to get user information in advanced REST authentication scenarios. (RRCT-2274)</li>
<li>The VerifySqlLiteral action from Sanitization API was deprecated in favor of BuildSafe_InClauseIntegerList and BuildSafe_InClauseTextList. These new actions are available in Platform Server 10.0.1005.0 and in Platform Server 11.0.422.0. (RRCT-2108)</li>
<li>Added instructions on importing the server configuration file (exported from the Deployment Controller) in the Front-end servers when upgrading to a new release. Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/6327/v11-installation-checklist-improvement" rel="external noopener nofollow" target="_blank">Kurt Vandevelde's idea</a>. (RSAT-1314)</li>
<li>The Platform Installer will now automate most of the prerequisites and performance tuning setup. The GUI has screens that guide you through this new step. Also, a new flag (/InstallPrerequisites=True) was added to unattended installation that is needed to signal explicitly that the installer should try to automate the prerequisites and performance tuning setup. (RSAT-1308)</li>
<li>Platform Server now requires Microsoft .NET Framework version 4.7.2. We recommend that you check both the "Runtime Changes" and "Retargeting Changes" pages in the <a class="link-https" href="https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/runtime/4.6.1-4.7.2" rel="external noopener nofollow" target="_blank" title="https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/runtime/4.6.1-4.7.2">Microsoft .NET Framework documentation</a> to identify any possible impacts that this update might have on your OutSystems applications. Installing this version will require you to reboot your server. (RSAT-1396)</li>
<li>The base image required for OutSystems applications running on Docker Containers Deployment Technology is now "microsoft/dotnet-framework:4.7.2-runtime". (RSAT-1397)</li>
<li>Upgraded RabbitMQ Client library to version 5.1.0. (RRCT-2142)</li>
<li>Upgraded Microsoft.AspNet.WebApi libraries to version 5.2.7. (RRCT-2143)</li>
<li>Replaced the OWASP HTML Sanitizer in Sanitization.xif by the <a class="link-https" href="https://github.com/mganss/HtmlSanitizer" rel="external noopener nofollow" target="_blank">HtmlSanitizer NuGet package</a>.<br/>
The SanitizeHtml action has the following differences when compared with the previous version:<br/>
— The <tt>&lt;noscript&gt;</tt> HTML tag is no longer allowed<br/>
— Some HTML attributes are no longer allowed: <tt>onfocus</tt>, <tt>onblur</tt>, <tt>onclick</tt>, <tt>onmousedown</tt>, <tt>onmouseup</tt>, <tt>noresize</tt>, <tt>background</tt><br/>
— The <tt>style</tt> attribute is now accepted (check the <a class="link-https" href="https://github.com/mganss/HtmlSanitizer#css-properties-allowed-by-default" rel="external noopener nofollow" target="_blank">list of CSS attributes allowed by default</a>)<br/>
— The sanitization of attribute values is less restrictive, with no security implications (e.g. the <tt>color</tt> attribute now accepts a wider range of different values)<br/>
— There might be some slight differences in the sanitized output, with no security implications (e.g. the new sanitizer replaces <tt>&lt;br/&gt;</tt> elements with <tt>&lt;br&gt;</tt>)<br/>
— The new sanitizer does not add a <tt>nofollow</tt> attribute to anchor elements (RRCT-2161)</li>
<li>Updated the following JavaScript libraries used by the mobile application runtime: 'decimal.js' to version 10.0.1, 'toformat' to version 2.0.0. (RTAF-91)</li>
<li>Implemented several optimizations that reduced the load time of "List Modules" and "Solution Details" pages in Service Center. (RSCT-1852)</li>
<li>On a first install, ServiceCenter will now be deployed into a dedicated application pool in IIS named "ServiceCenterAppPool". On upgrade, if ServiceCenter exists in "OutSystemsApplications" application pool in IIS, ServiceCenter will be moved to a dedicated application pool named "ServiceCenterAppPool". If ServiceCenter is already in some other application pool, it will not be moved. (RSAT-1338)</li>
<li>Added to FactoryConfiguration the option to include X-Content-Type-Options header with nosniff as a method of preventing MIME sniffing from older browser versions. (RRCT-2270)</li>
<li>Service Center now links to the detach process documentation instead of launching the No Lock-in tutorial. (RICT-1199)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/604_Platform_Server_Release_Apr.2019"><span id="Bug_Fixing_38"></span><h3 id="Bug_Fixing_36">Bug Fixing</h3>
<ul>
<li>Fixed incorrect character encoding in packaging of mobile applications. (RRCT-2216)</li>
<li>Fixed runtime error in client-side Aggregates with dynamic Order By's containing more than one attribute. (RSBO-54)</li>
<li>Fixed an issue that caused the Application 1-Click Publish to fail consistently when a previous 1-Click Publish aborted with an error. (RSCT-1693)</li>
<li>Fixed NullBinary() comparisons in client side with binaries being returned from server side aggregates. Previously it always returned "false" even when the binaries had no content. (RRCT-2279)</li>
<li>Fixed SOAP introspection not detecting some unsupported features. (RSBO-246)</li>
<li>Fixed the creation of Blank and Service modules to have the correct user provider set, instead of having the Template marked as user provider. (RRCT-2296)</li>
<li>Fixed an issue that prevented some OutSystems services from stopping when the Deployment Controller service was not running. (RRCT-2295)</li>
<li>Fixed an issue that caused Service Center to crash when changing the configuration of a mobile application. (RLIT-2490)</li>
<li>Fixed the errors related to retrieving mobile app authentication configuration that happened in some environments after upgrading to OutSystems 11 or after regenerating the authentication and encryption keys in Service Center. The error prevented mobile applications from working. (RPD-3794)</li>
<li>The User_Login action of the Users API no longer logs errors when the authentication is set to Active Directory or LDAP and the login is successful. (RLIT-2387)</li>
<li>Fixed the default action on the Create / Edit solution page on Service Center. Now the default action is to save the solution instead of searching. (RPD-3953)</li>
<li>Fixed query errors in some Users screens. (RPD-4015)</li>
<li>Fixed a problem when using ListAppend and ListInsert functions containing an If expression in the List input parameter. (RPD-3984)</li>
<li>The User_Login action of the Users API no longer aborts database transactions when an exception occurs. (RRCT-2189)</li>
<li>Fixed a rare problem that prevented custom Application and Screen Templates from being registered. (RSCT-1753)</li>
<li>Fixed an issue that was causing the error "Duplicate is not a valid operation inside a StartIteration/EndIteration block" when using cached actions. (RPD-3698)</li>
<li>Fixed a security issue that could cause session ids to be leaked with access to the Platform logs. CVSSv3.0 score 4.9 (Medium). (RRCT-2277)</li>
<li>Fixed a rare runtime error while running Aggregates when the Entity internal name was a reserved keyword. (RSBO-29)</li>
<li>Fixed SOAP introspection and compilation of WSDLs with enumerations inside &lt;list&gt; elements. (RSBO-272)</li>
<li>Changed how the machine memory is calculated in installation tuning scripts (when configuring worker process optimizations). Previous method could fail in some scenarios. (RPD-3685)</li>
<li>Fixed a runtime error while filtering booleans and date type in BPT tables. (RSBO-299)</li>
<li>Fixed a problem with Single Sign On on some scenarios with multiple frontends or containers. This could also lead to "Session fixation mismatch" errors. All existing sessions from applications in containers will be lost in the upgrade process. (RRCT-2214)</li>
<li>Fixed an issue with SanitizeHTML when sanitizing URLs with = characters. (RPD-3978)</li>
<li>Fixed Configuration Tool error 'The device is not ready' during upgrades from previous versions. (RPD-3880)</li>
<li>Fixed an error during publish caused by using SOAP Web Services with enumerations in Mobile modules. (RSBO-219)</li>
<li>Japanese characters are now correctly saved to the database when used in the default value of site properties. (RPD-3775)</li>
<li>Fixed an issue where added or updated fields in an editable table were not being enabled after an Ajax refresh of a row. (RPD-3879)</li>
<li>Fixed an issue in the JSON Serialize widget that affected the serialization of Date and Time values. This was causing the JSON Deserialize widget to return empty values. (RPD-3970)</li>
<li>Fixed an issue while generating service code when a SOAP operation contained headers in its input/output parameters. (RPD-4030)</li>
<li>Fixed Invalid numeric precision/scale error when reading -2^96 Decimal value in SQL Server. (RPD-4059)</li>
<li>Fixed issue farm environments when the platform is installed on different disk locations. (RPD-3896)</li>
<li>Fixed bug that occurred when consuming SOAP Web Services that use the same schema type as request/response and fault. (RSBO-306)</li>
<li>Improved the warning message in wizard "Create Action to Bootstrap Data from Excel" when the attributes are not going to be included in the bootstrap. (RSBO-53)</li>
<li>Fixed an issue when bulk changing the Test Values of several attributes in an Aggregate that were reverting to their original value. This was only happening when the original value was not null. (RSBO-71)</li>
<li>Fixed compilation error caused by a missing validation for the Combo Box variable type. (RICT-1320)</li>
<li>Removed unused CSS code that could cause browsers to generate a 404 error when retrieving some resources used in the configuration console of AD and LDAP providers. Embedded a font that was previously being downloaded at execution time. (RSAT-1328)</li>
<li>Removed incorrect warnings that were shown in Configuration Tool when clicking on 'Test Connection' for database users. (RPD-3691)</li>
<li>Using the List_SortColumn_GetOrderBy function from RichWidgets in a SQL Query Parameter with the Expand Inline property enabled will no longer trigger a SQL Injection Warning. (RRCT-2106)</li>
<li>Fixed a visual glitch in the Native Platforms Tab of Service Studio. (RNMT-2430)</li>
<li>Fixed occasional crash when merging Web Screens. (RICT-1237)</li>
<li>Fixed an error that prevented you from upgrading a module with the dynamic join logic to OutSystems 11. (RPD-3674)</li>
<li>Fixed a problem which caused SOAP Web Services imported in version 11 to have incorrect information. This happened when the WSDL had an enumeration defined in a top-level element that is used directly in an input part. (RSBO-360)</li>
<li>Fixed occasional crash using the Search in several tabs at the same time. (RTAF-108)</li>
</ul>
</div></div><span id="Platform_Server_Release_Jan.2019_CP3"></span><h2 id="Platform_Server_Release_Jan.2019_CP3">Platform Server Release Jan.2019 CP3</h2><br/><div class="mt-include" id="s25793">
<div class="info"><p>Released on May 06, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/526_Platform_Server_Release_Jan.2019_CP3"><span id="Bug_Fixing_39"></span><h3 id="Bug_Fixing_37">Bug Fixing</h3>
<ul>
<li>Fixed the BPT automatic cleanup process that was marking newly created activities as closed. (RPD-3891)</li>
<li>The MABS version tag of a mobile application is now correctly updated in Service Center for all environments, including the ones not connected to LifeTime. (RPD-3851)</li>
<li>Fixed an issue in AddAttributeToHtmlTag action that could lead to an ArgumentOutOfRange exception in runtime. (RPD-3931)</li>
<li>Fixed a problem in the code generation of SOAP service methods containing '.' in their names. (RPD-3948)</li>
<li>Fixed an issue with Input_AutoComplete being triggered in IE11 due to an unexpected 'keydown' event. (RPD-3866)</li>
</ul> </div></div><span id="Platform_Server_Release_Jan.2019_CP2"></span><h2 id="Platform_Server_Release_Jan.2019_CP2">Platform Server Release Jan.2019 CP2</h2><br/><div class="mt-include" id="s23808">
<div class="info"><p>Released on Mar 14, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/525_Platform_Server_Release_Jan.2019_CP2"><span id="Bug_Fixing_40"></span><h3 id="Bug_Fixing_38">Bug Fixing</h3>
<ul>
<li>We fixed a compilation error in the SOAP web services that prevented module publishing when an array of enums is used directly as output. This affected only applications with the new SOAP implementation. (RINT-3289)</li>
<li>We fixed a compilation error in the SOAP web services that prevented module publishing in some cases of single unbounded attributes. This affected only applications with the new SOAP implementation. (RINT-3303)</li>
<li>Now you can use the forward slash ("/") in the Name fields of the pictures in your mobile app without getting the 404 error once you save them to the back end and try loading them. (RPD-3638)</li>
<li>Fixed a runtime problem in consuming services when there is a complex type with a single element with maxOccurs &gt; 1 and that type is used as an element inside another type with maxOccurs &gt; 1.  (RINT-3224)</li>
<li>Updated the version of Charts application distributed with LifeTime. (RLIT-2357)</li>
<li>Fixed a security vulnerability. CVSS v3.0 score 7.1 (High) - Full details to be released in May 2019 (RLIT-2388)</li>
<li>Fixed issue in LifeTime when downloading a specific Application Version. (RLIT-2416)</li>
<li>Fixed the deployment error "Could not find a part of the path" that appeared when publishing a solution through OSPTool when eSpaces were moved across database catalogs. (RPD-3863)</li>
<li>Fixed an issue that was closing the DatePicker widget on iOS devices in web applications. (RPD-3852)</li>
<li>Fixed a security vulnerability (reported by Mina Edwar from Verizon). CVSS v3.0 score 8.1 (High) - Full details to be released in May 2019 (RPD-3849)</li>
<li>Fixed SAP introspection corruption that prevented you from consuming some methods dealing with multi-level tables. (RPD-3773)</li>
<li>Fixed an issue in the deployment service that was undeploying modules after upgrading from version 10. (RSCT-1773)</li>
<li>Fixed an issue in the Oracle driver that was preventing a query from aborting when a HTTP request timeout occurred while session data was being manipulated. (RPD-3726)</li>
<li>Fixed a bug that allowed Light Processes to have Input Parameters but would cause a compilation error when publishing. (RPD-3358)</li>
<li>Fixed an image rendering issue in Image widgets using binary data when Content Security Policy (CSP) is enabled. (RRCT-2186)</li>
<li>We fixed a bug that occasionally prevented Configuration Tool to modify the machine.config file because the file was used by another process. (RSAT-1226)</li>
<li>We fixed the href values in the Email links generated by the GetEntryURL Action of the HTTPRequestHandler extension. (RRCT-2254)</li>
<li>Fixed the error "Circular attribute group reference" when executing the XMLDocument_Load action of the Xml extension. (RPD-3742)</li>
<li>Fixed issue where "_" (underscore) characters were removed from email attachment filenames. (RPD-3690)</li>
<li>We fixed the SynchronizePublishMetrics error messages that appeared in the Error Log of some upgraded environments. (RPD-3729)</li>
<li>Fixed an issue with Input_AutoComplete being triggered in IE11 due to an unexpected 'keydown' event. (RPD-3866)</li>
</ul> </div></div><span id="Platform_Server_Release_Jan.2019_CP1"></span><h2 id="Platform_Server_Release_Jan.2019_CP1">Platform Server Release Jan.2019 CP1</h2><br/><div class="mt-include" id="s22822">
<div class="info">
<p>Released on Jan 22, 2019</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/522_Platform_Server_Release_Jan.2019_CP1"><span id="New_in_Platform_Server_Release_Jan.2019_CP1"></span><h3 id="New_in_Platform_Server_Release_Jan.2019_CP1">New in Platform Server Release Jan.2019 CP1</h3>
<ul>
<li>Added support for Service Actions in Service Center analytics reports. (ABE-618)</li>
<li>Enabled slow Service Action calls to be displayed in Lifetime's analytics. (ABE-619)</li>
<li>It is now possible to consume SOAP Web Services with binary type inputs. (RINT-3228)</li>
<li>You can now customize the mobile app version code in Service Center. This number is used by app stores to determine whether one version is more recent than another. To set the version code, navigate to Service Center &gt; Factory &gt; your mobile app &gt; Native Platforms, then click the Change link in the Code column. (RLIT-2106)</li>
<li>Cache invalidation service binaries are now fetched from the official repository. (RRCT-2050)</li>
<li>Improved the UI of the Deployment Zones screen in Service Center. (RSAT-1132)</li>
<li>Added README files that guide the user to more specific documentation on container deployment. These files are automatically added to the configured "Target Output" folder of the container hosting technology on the first deployment to the container. (RSAT-1078)</li>
<li>The base FROM image for Docker-based container hosting technologies - Amazon ECS, Azure Container Service, Docker Containers - has been changed from "microsoft/iis:latest" to "microsoft/dotnet-framework:4.7.1-runtime". The Deployment Zones associated with these container hosting technologies and using "microsoft/iis:latest" as the FROM image will be upgraded to use "microsoft/dotnet-framework:4.7.1-runtime". Deployment Zones that are already using a different FROM image will be kept unchanged. This change will increase the time of the first application deployment to containers, as the first layers of the OutSystems application image will need to be rebuilt. (RSAT-1105)</li>
<li>Deployment timeouts for Container Deployment Zones are now configurable in Service Center. (RSAT-1103)</li>
<li>Modified the default paths for Amazon ECS and Azure Container Service hosting technologies. (RSAT-1100)</li>
<li>The unattended installation and upgrade process now validates the prerequisites. (RSAT-1023)</li>
<li>When configuring a mobile application, it is now possible to choose the version of the Mobile Apps Build Service (MABS) that will be used to generate the mobile app package. (RNMT-2296)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/522_Platform_Server_Release_Jan.2019_CP1"><span id="Bug_Fixing_41"></span><h3 id="Bug_Fixing_39">Bug Fixing</h3>
<ul>
<li>Fixed a security vulnerability. CVSSv3.0 score 7.1 (High) (RLIT-2388)</li>
<li>Fixed an issue in the deployment service that was undeploying modules after upgrading from version 10. (RSCT-1773)</li>
<li>We fixed a bug that prevented you from installing Charts or OutSystems Now from Forge in some situations, causing the message "Application cannot be safely installed in your environment" to show. (ABE-1289)</li>
<li>Fixed an issue deploying multiple module applications to containers when the publish order of the modules was interleaved, causing the deployment to containers to fail. (RSAT-1171)</li>
<li>Fixed an issue in the installation process where the CPU cores were incorrectly counted when the core count was bigger than 9. (RSAT-1172)</li>
<li>Fixed "Failed to parse JSON request content" server-side exception triggered after mobile app upgrade rollback and navigation to modified screens. (RPD-3118)</li>
<li>Improved the application recovery in scenarios where the cache invalidation service is down and starts running again. (RRCT-2036)</li>
<li>When updating the cache invalidation service settings in the Configuration Tool, the user password is now also updated. (RRCT-2048)</li>
<li>The server configuration template for the unattended installation process now sets to false by default the encrypted attributes within the cache invalidation configuration. (RRCT-2049)</li>
<li>The log message from system action EspaceInvalidateCache now includes the name of the eSpace. (RRCT-2055)</li>
<li>Fixed an issue in the Oracle driver that was preventing to abort a query when a HTTP request timeout occurred while session data was being manipulated. (RPD-3726)</li>
<li>Queries to LDAP can now fallback to LdapConnection objects when using basic authentication. (RPD-3624)</li>
<li>App Feedback application is now more resilient to feedback submitted from screens having frames injected dynamically or resources with zero content length. (RPD-3588)</li>
<li>Fixed an issue that was changing the strings within brackets passed to an SQL element via an expand inline parameter. (RPD-3565)</li>
<li>Fixed an issue in the clean up process for old login attempts in Service Center. (RPD-3061)</li>
<li>Fixed an error occurring when a user with no permission tried to access Service Center log screens. (RLIT-2321)</li>
<li>The Users application now shows the correct number of users with a role in an application. (RLIT-2274)</li>
<li>Fixed broken links for the Roles in the Users application. (RPD-2833)</li>
<li>We fixed a UI bug in Users application &gt; Groups &gt; Roles. Now you'll have the correct links for the groups you add in Roles. (RPD-3055)</li>
<li>The "Publish all consumers" button in Service Center eSpace details page now publishes only the consumer modules that have references to the producer module in the current running version. (RPD-3355)</li>
<li>Enable container deployment info messages to be displayed in LifeTime. (RLIT-2261)</li>
<li>Fixed a compilation issue consuming SOAP Web Services that have a WSDL with GUID types. (RINT-2757)</li>
<li>Fixed the incorrect serialization of input parameters of Date, Time and DateTime data types in consumed SOAP Web Services. This might have caused data corruption on some scenarios. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Known_Issues-21552" rel="internal">Known Issues</a> section in the Platform Server Release Sep.2018 Release Notes for more information. (RINT-3069)</li>
<li>Fixed a publishing issue consuming SOAP Web Services when a SOAP Structure is used both inside a <choice> element and a List. (RINT-3190)</choice></li>
<li>Consuming SOAP services that include Time outputs no longer causes a compilation error. (RINT-3203)</li>
<li>Fixed a publishing issue consuming SOAP Web Services when the SOAP Structure contain only a single attribute of type List. (RINT-3217)</li>
<li>Fixed an issue consuming SOAP Web Services that contain the <include> element. (RINT-3229)</include></li>
<li>Fixed the conversion of nil values for numerical types when consuming SOAP Web Services. (RINT-3287)</li>
<li>Fixed a runtime error occurring when a List Box is inside a Table Records. (RAFT-1703)</li>
<li>Fixed an issue in the installation process that was accepting as valid certain unsupported .Net Framework versions. (RSAT-1169)</li>
<li>Fixed a problem in the Configuration Tool that was not updating the Logs tab correctly when changing the Authentication type to Windows in the Platform tab. (RSAT-1108)</li>
<li>Fixed URL used by LifeTime to redirect users to configurations pages of environments. (RPD-3302)</li>
<li>Fixed issue when trying to connect to an invalid service on port 12003. (RPD-3626)</li>
<li>Fixed an issue causing a "Not Found" error in the Configuration Tool that occurred in clean installations of OutSystems 11 using Windows Authentication. (RRCT-2068)</li>
</ul>
</div></div><span id="Platform_Server_Release_Jan.2019"></span><h2 id="Platform_Server_Release_Jan.2019">Platform Server Release Jan.2019</h2><br/><div class="mt-include" id="s22287">
<div class="info">
<p>Removed from availability on Mar 21, 2019</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/510_Platform_Server_Release_Jan.2019"><span id="New_in_Platform_Server_Release_Jan.2019"></span><h3 id="New_in_Platform_Server_Release_Jan.2019">New in Platform Server Release Jan.2019</h3>
<ul>
<li>Added support for Service Actions in Service Center analytics reports. (ABE-618)</li>
<li>Enabled slow Service Action calls to be displayed in Lifetime's analytics. (ABE-619)</li>
<li>It is now possible to consume SOAP Web Services with binary type inputs. (RINT-3228)</li>
<li>You can now customize the mobile app version code in Service Center. This number is used by app stores to determine whether one version is more recent than another. To set the version code, navigate to Service Center &gt; Factory &gt; your mobile app &gt; Native Platforms, then click the Change link in the Code column. (RLIT-2106)</li>
<li>When configuring a mobile application, it is now possible to choose the version of the Mobile Apps Build Service (MABS) that will be used to generate the mobile app package. (RNMT-2296)</li>
<li>Cache invalidation service binaries are now fetched from the official repository. (RRCT-2050)</li>
<li>Improved the UI of the Deployment Zones screen in Service Center. (RSAT-1132)</li>
<li>Added README files that guide the user to more specific documentation on container deployment. These files are automatically added to the configured "Target Output" folder of the container hosting technology on the first deployment to the container. (RSAT-1078)</li>
<li>The base FROM image for Docker-based container hosting technologies - Amazon ECS, Azure Container Service, Docker Containers - has been changed from "microsoft/iis:latest" to "microsoft/dotnet-framework:4.7.1-runtime". The Deployment Zones associated with these container hosting technologies and using "microsoft/iis:latest" as the FROM image will be upgraded to use "microsoft/dotnet-framework:4.7.1-runtime". Deployment Zones that are already using a different FROM image will be kept unchanged. This change will increase the time of the first application deployment to containers, as the first layers of the OutSystems application image will need to be rebuilt. (RSAT-1105)</li>
<li>Deployment timeouts for Container Deployment Zones are now configurable in Service Center. (RSAT-1103)</li>
<li>Modified the default paths for Amazon ECS and Azure Container Service hosting technologies. (RSAT-1100)</li>
<li>The unattended installation and upgrade process now validates the prerequisites. (RSAT-1023)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/510_Platform_Server_Release_Jan.2019"><span id="Bug_Fixing_42"></span><h3 id="Bug_Fixing_40">Bug Fixing</h3>
<ul>
<li>We fixed a bug that prevented you from installing Charts or OutSystems Now from Forge in some situations, causing the message "Application cannot be safely installed in your environment" to show. (ABE-1289)</li>
<li>Fixed an issue in the installation process that was accepting as valid certain unsupported .Net Framework versions. (RSAT-1169)</li>
<li>Fixed an issue deploying multiple module applications to containers when the publish order of the modules was interleaved, causing the deployment to containers to fail. (RSAT-1171)</li>
<li>Fixed an issue in the installation process where the CPU cores were incorrectly counted when the core count was bigger than 9. (RSAT-1172)</li>
<li>Fixed "Failed to parse JSON request content" server-side exception triggered after mobile app upgrade rollback and navigation to modified screens. (RPD-3118)</li>
<li>Improved the application recovery in scenarios where the cache invalidation service is down and starts running again. (RRCT-2036)</li>
<li>When updating the cache invalidation service settings in the Configuration Tool, the user password is now also updated. (RRCT-2048)</li>
<li>The server configuration template for the unattended installation process now sets to false by default the encrypted attributes within the cache invalidation configuration. (RRCT-2049)</li>
<li>The log message from system action EspaceInvalidateCache now includes the name of the eSpace. (RRCT-2055)</li>
<li>Fixed an issue in the Oracle driver that was preventing a query from aborting when a HTTP request timeout occurred while session data was being manipulated. (RPD-3726)</li>
<li>Queries to LDAP can now fallback to LdapConnection objects when using basic authentication. (RPD-3624)</li>
<li>App Feedback application is now more resilient to feedback submitted from screens having frames injected dynamically or resources with zero content length. (RPD-3588)</li>
<li>Fixed an issue that was changing the strings within brackets passed to an SQL element via an expand inline parameter. (RPD-3565)</li>
<li>Fixed an issue in the clean up process for old login attempts in Service Center. (RPD-3061)</li>
<li>Fixed a problem in the Configuration Tool that was not updating the Logs tab correctly when changing the Authentication type to Windows in the Platform tab. (RSAT-1108)</li>
<li>Fixed an error occurring when a user with no permission tried to access Service Center log screens. (RLIT-2321)</li>
<li>Fixed broken links for the Roles in the Users application. (RPD-2833)</li>
<li>We fixed a UI bug in Users application &gt; Groups &gt; Roles. Now you'll have the correct links for the groups you add in Roles. (RPD-3055)</li>
<li>The "Publish all consumers" button in Service Center eSpace details page now publishes only the consumer modules that have references to the producer module in the current running version. (RPD-3355)</li>
<li>Enable container deployment info messages to be displayed in LifeTime. (RLIT-2261)</li>
<li>Fixed a compilation issue consuming SOAP Web Services that have a WSDL with GUID types. (RINT-2757)</li>
<li>Fixed the incorrect serialization of input parameters of Date, Time and DateTime data types in consumed SOAP Web Services. This might have caused data corruption on some scenarios. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Known_Issues-21552" rel="internal">Known Issues</a> section in the Platform Server Release Sep.2018 Release Notes for more information. (RINT-3069)</li>
<li>Fixed a publishing issue consuming SOAP Web Services when a SOAP Structure is used both inside a <choice> element and a List. (RINT-3190)</choice></li>
<li>Fixed a publishing issue consuming SOAP Web Services when the SOAP Structure contain only a single attribute of type List. (RINT-3217)</li>
<li>Consuming SOAP services that include Time outputs no longer causes a compilation error. (RINT-3203)</li>
<li>Fixed an issue consuming SOAP Web Services that contain the xsd:include element. (RINT-3229)</li>
<li>Fixed the conversion of nil values for numerical types when consuming SOAP Web Services. (RINT-3287)</li>
<li>Fixed a runtime error occurring when a List Box is inside a Table Records. (RAFT-1703)</li>
<li>The Users application now shows the correct number of users with a role in an application. (RLIT-2274)</li>
<li>Fixed a rare over-optimization issue occurring in implicit conversions for List Records. (RSCT-1705)</li>
<li>Fixed an issue causing a "Not Found" error in the Configuration Tool that occurred in clean installations of OutSystems 11 using Windows Authentication. (RRCT-2068)</li>
<li>Allow HTTP connections from Service Studio to the Templates Manager (RAFT-1792)</li>
</ul>
</div></div><span id="Platform_Server_Release_Sep.2018_CP2"></span><h2 id="Platform_Server_Release_Sep.2018_CP2">Platform Server Release Sep.2018 CP2</h2><br/><div class="mt-include" id="s22236">
<div class="info">
<p>Released on Jan 04, 2019</p>
</div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/495_Platform_Server_Release_Sep.2018_CP2"><span id="New_in_Platform_Server_Release_Sep.2018_CP2"></span><h3 id="New_in_Platform_Server_Release_Sep.2018_CP2">New in Platform Server Release Sep.2018 CP2</h3>
<ul>
<li>Added a comment in the generated SQL of Advanced Queries and Aggregates with the location of the query in OutSystems applications. Configurable using Factory Configuration. Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/4817/reverse-tracking-sql" rel="external noopener nofollow" target="_blank">Neil Munro's idea</a>. (ABE-1151)</li>
<li>Improved the 1-Click Publish performance of modules containing references without entities or structures. (ABE-1275)</li>
<li>The automatic trigger URLs for the Deployment Zone of Container hosting technologies now send the module names (as a JSON array) of the application being deployed. (RSAT-1118)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/495_Platform_Server_Release_Sep.2018_CP2"><span id="Bug_Fixing_43"></span><h3 id="Bug_Fixing_41">Bug Fixing</h3>
<ul>
<li>Fixed the incorrect serialization of input parameters of Date, Time and DateTime data types in consumed SOAP Web Services. This might have caused data corruption on some scenarios. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Known_Issues-21552" rel="internal">Known Issues</a> section in the Platform Server Release Sep.2018 Release Notes for more information. (RINT-3069)</li>
<li>We fixed an array compilation error in the SOAP web services that prevented module publishing. This affected only applications with the new SOAP implementation. (RPD-3627)</li>
<li>Fixed SAP connection testing in Service Center that always failed with an invalid login error. (RPD-3847)</li>
<li>Fixed an issue that was causing the error "Duplicate is not a valid operation inside a StartIteration/EndIteration block" when using cached actions. (RPD-3698)</li>
<li>Fixed an issue that was causing high memory consumption when using complex structures with several lists. (RPD-3633)</li>
<li>Fixed an issue that caused JSON Deserialize to fail when deserializing Null DateTimes "1900-01-01T00:00:00" in Mobile Devices with Negative Timezones offsets. (RPD-3661)</li>
<li>Added module information to some Scheduler error logs where this information was missing. (RRCT-2072)</li>
<li>Fixed an issue deploying multiple module applications to containers when the publish order of the modules was interleaved, causing the deployment to containers to fail. (RSAT-1171)</li>
<li>Fixed an issue in the Configuration Tool that was incorrectly checking log permissions when clicking the "Create/Upgrade Database" button for the platform database. (RSAT-1110)</li>
<li>Fixed an issue that prevented applications running in containers from picking up changes to the configuration files when configuration files are mounted in containers using SMB volumes or Kubernetes ConfigMaps. (RSAT-1117)</li>
<li>Changes in the license of an environment now correctly propagate to applications running in containers. (RSCT-1378)</li>
<li>Fixed an issue that sometimes prevented users from publishing a module after debugging it in a personal area. (RSCT-1656)</li>
</ul>
</div></div><span id="Platform_Server_Release_Sep.2018_CP1"></span><h2 id="Platform_Server_Release_Sep.2018_CP1">Platform Server Release Sep.2018 CP1</h2><br/><div class="mt-include" id="s22024">
<div class="info"><p>Released on Dec 20, 2018</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/479_Platform_Server_Release_Sep.2018_CP1"><span id="New_in_Platform_Server_Release_Sep.2018_CP1"></span><h3 id="New_in_Platform_Server_Release_Sep.2018_CP1">New in Platform Server Release Sep.2018 CP1</h3>
<ul>
<li>Added a comment in the generated SQL of Advanced Queries and Aggregates with the location of the query in OutSystems applications. Configurable using Factory Configuration. Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/4817/reverse-tracking-sql" rel="external noopener nofollow" target="_blank">Neil Munro's idea</a>. (ABE-1151)</li>
<li>We removed the obsolete "referrer" directive from the Content Security Policy (CSP) configuration screens. (RLIT-2270)</li>
<li>The timeout for building mobile applications has been increased to 30 minutes when launched from Service Studio. (RLIT-2095)</li>
<li>The logs of query errors from Aggregates and Advanced SQL now contain more details. (RRCT-1918)</li>
<li>We fixed an issue with the compiler optimizer that sometimes caused long compilation times. (RSCT-1302)</li>
<li>Now there's a warning during an introspection of a WSDL, if it contains an attributeGroups element. (RINT-2759)</li>
<li>Added support for SOAP Arrays in consumed SOAP Web Services. (RINT-956)</li>
<li>Added support for "any" elements in consumed SOAP Web Services. (RINT-1439)</li>
<li>Added support for Polymorphism in consumed SOAP Web Services. (RINT-1972)</li>
<li>The SSL offload is now on by default for applications running in containers. (RSAT-1073)</li>
<li>The container deploy process no longer leaves behind old result files. (RSAT-887)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/479_Platform_Server_Release_Sep.2018_CP1"><span id="Bug_Fixing_44"></span><h3 id="Bug_Fixing_42">Bug Fixing</h3>
<ul>
<li>Changing an input parameter of a Service Action from optional to mandatory will now trigger an exception at runtime when the parameter value is not set. (ABE-949)</li>
<li>We fixed an issue related to the Oracle driver not being able to abort a query when a HTTP request timeout occurs. (RPD-3426)</li>
<li>Now the system entities in the Oracle databases create the correct indexes for primary keys of the Text type. (RPD-3528)</li>
<li>User information is no longer propagated in BPT actions (e.g. ActivityClose) when the process is defined in a module with a different User Provider. (RRCT-1969)</li>
<li>In the modules with multi-tenant tables, the compilation time no longer scales up with the number of existing tenants. (RPD-3085)</li>
<li>Fixed a bug that prevented CSP (Content Security Policy) violation logs from reaching the endpoint specified by the "report-to" header field. Now the violation logs are saved properly. (RRCT-1982)</li>
<li>You can now set OutSystems to reject the requests for non-supported image formats. In "Factory Configuration" Forge component, go to Security and check the option "Enforce Valid Image Formats on Image and Binary Endpoints". The valid image formats are GIF, PNG, and JPEG. The setting applies to the images the end-users upload through the applications created in OutSystems. (RRCT-2002)</li>
<li>Fixed issue that prevented unblocking operations on blocked IP Addresses in the Users application when using Oracle as the database platform. (RPD-3537)</li>
<li>Fixed a bug that caused a "Cannot read property 'type' of null" JavaScript error when removing a radio button via an AJAX call. (RPD-3490)</li>
<li>Fixed PerformanceMonitoring API returning a TTLB (Time To First Byte) value lower than the TTFB (Time To Last Byte) value for Submit requests. (RPD-3497)</li>
<li>Fixed Feedback Message in Screen Preparation being shown twice. (RPD-3516)</li>
<li>Fixed high database load caused by the "GetDevEffort" query during LifeTime synchronization operations. (RPD-3542)</li>
<li>Now the AJAX Request no longer fails when a Web Screen has multiple HTML Forms. (RPD-3558)</li>
<li>We fixed the listing of the database connections for the extension configuration, so it can show more than 100 server connection. (RPD-3571)</li>
<li>Now you can set an empty Timer schedule in Service Center. This was already possible in Service Studio. (RPD-3580)</li>
<li>Fixed the default browser behavior to ask to save the login credentials. Now the password fields in OutSystems applications such as Service Center or LifeTime have the "autocomplete" property set to "off" by default. (RPD-3464)</li>
<li>We fixed the OsVisitor cookies so they are now properly set to expire, and no longer lost when the browser is closed. (RPD-3590)</li>
<li>Now you won't have an empty item in Service Center "Recent items" sidebar list when you publish an existing eSpace through Service Center. (RLIT-2277)</li>
<li>Now your unattended platform installations have the Debug Mode enabled. We fixed a bug that deactivated Environment Debug Mode when uploading the first license.  (RLIT-2262)</li>
<li>Fixed issue that left applications as outdated after synchronization. (RLIT-2244)</li>
<li>Some previously missing administrative operations are now allowed in on-premises environments in hybrid infrastructures. (RPD-3449)</li>
<li>We corrected an issue with the Oracle introspection in Integration Studio. Integration Studio was unable to find tables if the schema was not explicit. Now there's a fallback to use the schema configured in the database connection. (RPD-2938)</li>
<li>Fixed the Service Center mobile request logs so they now have a unit of time.  (RLIT-2170)</li>
<li>Fixed the name of the export file obtained after clicking the "Export to Excel" link from the Integrations Log page in Service Studio. (RLIT-2153)</li>
<li>Fixed spacing issues between links in the Tenant tab of the eSpace details screen in Service Center. (RLIT-2193)</li>
<li>Fixed the "Expected ';'" JavaScript error that appeared after an AJAX Refresh in some scenarios. (RPD-3511)</li>
<li>Fixed a compilation error that occurred when using a Web Service containing action with single outputs of type Structure. (RINT-2775)</li>
<li>The Configuration Tool command-line parameter "/ModifyDeploymentZone" now fails gracefully when trying to modify a non-existing deployment zone. (RSAT-1042)</li>
<li>Due to the specifics of deploying applications into containers, we disabled the Delete button for those applications. This is to prevent OutSystems Deployment Controller Service, for the application you are trying to delete, from a lock during the 30 minutes timeout in some scenarios. Otherwise, you'd need to restart the OutSystems Deployment Controller Service to resume normal operations before the timeout. Additionally, the messages related to container deployment are now correctly shown in LifeTime. Check <a class="new" href="https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Deleting_an_application_that_is_manually_deployed_to_a_container" rel="internal">"Deleting an application that is manually deployed to a container"</a> for the instructions. (RSAT-1077)</li>
<li>Fixed deprecation warning due to the usage of 'buildpack' attribute in Pivotal Cloud Foundry (PCF) manifest files, which are used for PCF deployments. (RSAT-1055)</li>
<li>We fixed a resource disposal issue that might cause errors while contacting external container deployment tools. (RSAT-1104)</li>
<li>Fixed the incorrect serialization of input parameters of Date, Time and DateTime data types in consumed SOAP Web Services. This might have caused data corruption on some scenarios. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Known_Issues-21552" rel="internal">Known Issues</a> section in the Platform Server Release Sep.2018 Release Notes for more information. (RINT-3069)</li>
<li>Fixed incorrect packaging of the Caching and Logging libs for the Container Application Scheduler. (RSAT-1074)</li>
<li>Consuming SOAP services that include Time outputs no longer causes a compilation error. (RINT-3203)</li>
<li>Fixed Service Center so it now ignores the database incoherences that can cause timers to appear to be running indefinitely. (RPD-2999)</li>
<li>Fixed an issue where database images containing trailing white spaces were not being rendered. (RRCT-1967)</li>
<li>Fixed an inconsistency in the Null binary parsing when serialized. Now a Null binary returned by the server actions is always serialized to '{}'. (RRCT-1968)</li>
<li>Fixed compilation error when WSDL anonymous types were not found. (RINT-2699)</li>
<li>Fixed rare deadlock in OutSystems Services. (RPD-3584)</li>
<li>Improved the flush of logs to the database when stopping the platform services to prevent the loss of some logs during shutdown. (RRCT-1989)</li>
<li>We fixed a performance bug in the database connection related to the login mechanism. You should see improvement in the applications that run many queries during the initialization phase. (RRCT-2033)</li>
<li>The RabbitMQ client now supports TLS 1.1 and TLS 1.2. (RRCT-2013)</li>
<li>Fixed Configuration Tool making it reference the Cache Invalidation Service script relative to its path. (RRCT-2003)</li>
<li>Oracle hints are no longer removed from queries supplied to Advanced SQL elements through input parameters. (RPD-3457)</li>
<li>Fixed a bug in LifeTime and Service Center that was marking modules as successfully published after the deployment failure.  (RSCT-1222)</li>
<li>Now the custom handlers render correctly in the applications deployed to containers. (RRCT-1972)</li>
<li>Fixed the error about the 'precache.manifest' file not found that appeared when publishing a mobile module. (RSCT-1638)</li>
</ul></div></div><span id="Platform_Server_Release_Sep.2018"></span><h2 id="Platform_Server_Release_Sep.2018">Platform Server Release Sep.2018</h2><br/><div class="mt-include" id="s21552"><div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="New_in_Release_Sep.2018"></span><h3 id="New_in_Release Sep.2018">New in Release Sep.2018</h3>
<div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="Architecture"></span><h6 id="Architecture-21552">Architecture</h6>
<ul>
<li dir="ltr">Added a new application and module type (Services) to promote a better application segmentation and governance. (ABE-1276)</li>
<li dir="ltr">Added a new language element (Service Action) which is a loosely coupled action (REST underneath) with impact analysis and security by default. (ABE-1277)</li>
<li dir="ltr">Optional parameters and attributes do not require refreshing consumers, making larger systems more loosely coupled and allowing independent teams to release more often without impacting each other. (ABE-1278)</li>
<li dir="ltr">Public Screens are now loosely coupled, avoiding circular references in dependency analysis. (ABE-1279)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="Containers"></span><h6 id="Containers-21552">Containers</h6>
<ul>
<li dir="ltr">It's now possible to deploy and run OutSystems applications using Windows Docker Container in an on-premise Docker container environment, or in a cloud environment like Amazon (in Elastic Container Service) or Azure (in Azure Container Service). (RSAT-505)</li>
<li dir="ltr">The concept of Zones was revamped and it's now called Deployment Zones and have them associated to a hosting technology when application will be deployed. (RSAT-612)</li>
<li dir="ltr">A set of tools is now available to collect information about the Docker container and application health in order to help the troubleshoot or gather relevant information to the analysis. Check these troubleshooting tools <a class="link-https" href="https://github.com/OutSystems/OutSystems-CollectInfo-wdocker" rel="external noopener nofollow" target="_blank"><u>here</u></a>. (RSAT-829)</li>
<li dir="ltr">"Automatic" in the Deployment Mode section. For more info on how to configure the URLs that trigger the deployment actions, check <a class="new" href="https://success.outsystems.com/Documentation/Development_FAQs/How_to_automate_Docker_container_deployment_with_Jenkins" rel="internal"><u>How to automate Docker container deployment with Jenkins</u></a>. (RSAT-395)</li>
<li dir="ltr">When an application is associated to a Deployment Zone configured to use containers as hosting technology, OutSystems platform will generate a bundle with all the assets needed to allow build and run your application in a container. (RSAT-385)</li>
<li dir="ltr">Fixed a container-related issue that left temporary files behind after aborting a solution that was published in the two steps mode. (RSCT-1379)</li>
<li dir="ltr">OutSystems Management Consoles gives you the possibility to defined the hosting technology for your applications. That technology is now visible though their logos in Lifetime animations. (RSAT-769)</li>
<li dir="ltr">Provided an hosting technology associated to Pivotal Cloud Foundry. When applications associated to a Deployment Zone with this kind of hosting technology are deployed, a bundle with all the assets are generated in order to deploy and run OutSystems applications in Pivotal Application Service (PAS). (RSAT-694)</li>
<li dir="ltr">It is now possible to define the desired Deployment Zone for an application during the preparation of a staging operation in LifeTime. (RSAT-744)</li>
</ul>
</div><div class="mt-section" id="section_4" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="SOAP"></span><h6 id="SOAP-21552">SOAP</h6>
<ul>
<li dir="ltr">SOAP Web Service Methods now support default values in Input Parameters, Output Parameters and Structure Attributes of SOAP Web Services. The minOccurs/nillable WSDL attributes are now taken into consideration when determining mandatory Input Parameters and Structure Attributes. (RINT-1833)</li>
<li dir="ltr">Added support for consuming SOAP web services with Enumerations. (RINT-1764)</li>
<li dir="ltr">Introspect a WSDL that requires the basic authentication by passing the username and password into the URL (e.g. <a class="link-https" href="https://username:password@server/example.com?wsdl" rel="external noopener nofollow" target="_blank"><u>https://username:password@server/example.com?wsdl</u></a>). Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/3284/" rel="external noopener nofollow" target="_blank"><u>Darren Conroy's idea</u></a>. (RINT-1656)</li>
<li dir="ltr">It is now possible to define the authentication type and the corresponding credentials for an imported SOAP 1.2 web service. (RINT-1225)</li>
<li dir="ltr">It is now possible to dynamically authenticate with different credentials per SOAP 1.2 web service method. (RINT-900)</li>
<li dir="ltr">It is now possible to override the authentication credentials for a SOAP 1.2 web service in Service Center. (RINT-897)</li>
<li dir="ltr">It's now possible to configure and see logs of consumed SOAP 1.2 web services in Service Center. (RINT-841)</li>
<li dir="ltr">Added support for consuming SOAP web services with nillable attributes. (RINT-835)</li>
<li dir="ltr">It is now possible to override the default service endpoint for a SOAP 1.2 web service in Service Center. (RINT-899)</li>
</ul>
</div><div class="mt-section" id="section_5" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="Logging"></span><h6 id="Logging-21552">Logging</h6>
<ul>
<li dir="ltr">It's now possible to store logs in a separate database from the one storing the data used by business applications and the data that supports the platform runtime (thanks to <a class="link-https" href="https://www.outsystems.com/ideas/132/Log+database+catalog" rel="external noopener nofollow" target="_blank"><u>Didier Miller for highlighting this need as an idea</u></a>). (RRCT-1472)</li>
<li dir="ltr">Applications are now self sufficient regarding logging their own information. From now on the logging mechanism do not rely on an external service (LogService). (RRCT-839)</li>
<li dir="ltr">The logs of the query errors from Aggregates and Advanced SQL now contain more details. (RRCT-1918)</li>
<li dir="ltr">Unattended Installation API was updated to take in consideration a possible split between platform database and logging database (RRCT-1783)</li>
</ul>
</div><div class="mt-section" id="section_6" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="More"></span><h6 id="More-21552">More</h6>
<ul>
<li dir="ltr">We improved the 1-Click Publish performance of the published modules by making the deploy phase differential. The smaller the number of modified resources, the more noticeable the speed improvement is. (RSCT-1436)</li>
<li dir="ltr">Application debug mode no longer depends on environment type (e.g. DEV, QA), making it possible to debug applications in all environments. Introduced new types of environments to allow for more flexible management of infrastructures. (RSCT-1148)</li>
<li dir="ltr">Web Blocks now support Events and Event Handlers to propagate changes to their parent element. (RAFT-1371)</li>
<li dir="ltr">You can now use ListDistinct, a new client and server action. The action removes duplicates from the list. Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/2830/" rel="external noopener nofollow" target="_blank"><u>Carlos Henriques' idea</u></a>. (RCOT-1108)</li>
<li dir="ltr">Inputs now have aria-required and aria-invalid attributes in web runtime applications. (RAFT-1292)</li>
<li dir="ltr">HTTPS is now maintained even when navigating to a Screen not explicitly marked as requiring HTTPS. (RRCT-1399)</li>
<li dir="ltr">Binary Resources referenced by Web Applications now have a 'by-copy' semantic and are automatically copied to relevant consumer Modules. (RRCT-1155)</li>
<li dir="ltr">New method registerDeviceClassGetter added to JS Public API allows to change the default behavior of adapting the css classes applied to the device resolution. By default, resolution higher than 1024px are considered tablets. (RAFT-1296)</li>
<li dir="ltr">To achieve higher performance, you can now create stateless BAPI calls to the SAP servers. (RINT-1934)</li>
<li dir="ltr">Changed the default User Provider for blank modules to match the provider of the Application Template in use. (RRCT-1858)</li>
<li dir="ltr">Configuration Tool now automatically changes the pipeline mode to "Integrated" in IIS Application Pools that only contain OutSystems applications. (RSAT-295)</li>
<li dir="ltr">OutSystems caching mechanism now uses RabbitMQ system to forward cache invalidation notifications to OutSystems applications. (RRCT-835)</li>
<li dir="ltr">You can now use Configuration Tool, via UI or Unattended Installation API, to install and configure the Cache Invalidation Service (RabbitMQ). (RRCT-1728)</li>
<li dir="ltr">To prevent runtime problems, the Session Database upgrade step is now mandatory during the Platform updates. (RSAT-974)</li>
<li dir="ltr">Removed support for SMS feature. (RRCT-1639)</li>
<li dir="ltr">Deprecated BeginReadUncommittedTransaction and BeginTransaction methods from RuntimePublic.Db API. (RSAT-791)</li>
</ul>
</div></div><div class="mt-section" id="section_7" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="Bug_Fixing_45"></span><h3 dir="ltr" id="Bug_Fixing_43">Bug Fixing</h3>
<ul>
<li dir="ltr">Fixed a bug that caused the processing of error logs to fail with long Action names. (RPD-1769)</li>
<li dir="ltr">Fixed the bug that caused "Could not login to 127.0.0.1" error while publishing the "Current Running Version" of a Solution in Service Center. This caused issues in some upgrades. (RPD-2415)</li>
<li dir="ltr">Improved the Resources error message about paths that are too long. (ABE-1214)</li>
<li dir="ltr">Fixed invalid login error when using Integrated Authentication for both database and web service consumption. (RPD-3417)</li>
<li dir="ltr">Fixed an error related to the generation of the application icons when uploading an icon or creating a solution by uploading an OSP or OAP. (RPD-3444)</li>
<li dir="ltr">Fixed splash screen hanging in iOS when Content Security Policies are enabled. (RPD-3428)</li>
<li dir="ltr">Fixed an installation problem that was recreating the default Global Zone even after you had deleted it. (RSCT-1412)</li>
<li dir="ltr">Fixed an issue that was keeping unnecessary files in the "repository" folder on the server, increasing the folder size. (RSCT-1227)</li>
<li dir="ltr">Fixed problem that caused a module publish operation to fail due to a concurrent publish even when that module was not being published anywhere else. (RSCT-1267)</li>
<li dir="ltr">Fixed a problem where publishing simultaneously modules with identical names in different personal environments would result in having future publication attempts of those modules blocked. (RSCT-1287)</li>
<li dir="ltr">Fixed a bug that caused invalid generation of the CSP HTTP headers when using the default values from the Service Center settings. This prevented a small number of iOS apps from loading after the splash screen. (RRCT-1966)</li>
</ul>
</div><div class="mt-section" id="section_8" mt-section-origin="Support/Release_Notes/11/Platform_Server/400_Platform_Server_Release_Sep.2018"><span id="Known_Issues_15"></span><h3 id="Known_Issues_13">Known Issues</h3>
<ul>
<li>
<p>In some situations, the new SOAP implementation in OutSystems 11 incorrectly serializes input parameters of Date, Time and DateTime data types for consumed Web Services, which might cause data corruption (namely losing time offsets for Time and DateTime data types) when sending values of these data types. This new implementation is used for all consumed SOAP Web Service elements created in version 11.</p>
<p>The previous behavior (in OutSystems 10) is the following:<br/>
— Values of Time data type are sent without date information and with timezone information (offset).<br/>
— Values of DateTime data type are sent with timezone information (offset).<br/>
— Values of Date data type are sent without time information.</p>
<p>In OutSystems 11 up to version 11.0.128.0 the incorrect behavior is the following:<br/>
— Values of Time data type are sent with (unnecessary) date information and without timezone information (offset).<br/>
— Values of DateTime data type are sent without timezone information (offset).<br/>
— Values of Date data type are sent with (unnecessary) time information.</p>
<p>The incorrect behavior has been fixed in version 11.0.128.0 to match the OutSystems 10 behavior.</p>
</li>
</ul>
</div></div><span id="Platform_Server_11.0.539.0"></span><h2 id="Platform_Server_11.0.539.0">Platform Server 11.0.539.0</h2><br/><div class="mt-include" id="s33673">
<div class="info"><p>Released on Jul 25, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.0.539.0"><span id="New_in_Platform_Server_Release_Jul.2019_CP1_2"></span><h3 id="New_in_Platform_Server_Release_Jul.2019_CP1">New in Platform Server Release Jul.2019 CP1</h3>
<ul>
<li>Added support for TLS 1.1 and TLS 1.2 on MySQL external database connections. 
Warning: OutSystems now distributes BouncyCastle (v1.8.3) and Google.Protobuf (v.3.6.1.0) alongside the MySQL driver - this may impact the existing extensions that use different versions. (RSAT-1258)</li>
<li>Downloading a mobile app by scanning the QR code in Service Studio is now possible on iOS 13. (RTAF-628)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.0.539.0"><span id="Bug_Fixing_46"></span><h3 id="Bug_Fixing_44">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented some Dependencies to be added in Search in other Modules. (RDEV-413)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 7.5 (High). (RNMT-2812)</li>
<li>Fixed an issue in the Spanish translation of RichWidgets. (RPD-3132)</li>
<li>Fixed compilation error that occurred when SOAP Faults were using types based on the .NET CLR (Common Language Runtime). (RPD-3979)</li>
<li>Fixed bug where attributes of structures created by an Integration Plugin which had default values could not be consumed in another module. (RPD-3862)</li>
<li>Fixed compilation error when removing Entity or Structure attributes that are still used in consumer modules. (RSBO-630)</li>
<li>Description of entities using Japanese characters will be saved using Unicode correctly after first publish. (RPD-4258)</li>
<li>Fixed incorrect advanced query GetUsersByRoleId in the Users application. (RPD-4220)</li>
<li>Fixed missing producers when consuming/refreshing references while logged in using a composite user name (domain\username). (RPD-4185)</li>
<li>Fixed an issue in 1-Click Publish when a module is renamed changing only the case (e.g. from ModuleName to ModuleNAME), which was causing the module to be incorrectly undeployed. (RSCT-2042)</li>
<li>Fixed an issue in the pre-requisites checking stage of the Platform Server installer so it doesn't fail for Windows installations using Japanese language. (RPD-4212)</li>
</ul>
<br/>
<p><b>Disclaimer: </b><i>QR CODE is a registered trademark of Denso Wave Incorporated.</i></p></div></div><span id="Platform_Server_11.0.424.3"></span><h2 id="Platform_Server_11.0.424.3">Platform Server 11.0.424.3</h2><br/><div class="mt-include" id="s30761">
<div class="info"><p>Released on May 17, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.0.424.3"><span id="New_in_Platform_Server_Release_Apr.2019_CP1_2"></span><h3 id="New_in_Platform_Server_Release_Apr.2019_CP1">New in Platform Server Release Apr.2019 CP1</h3>
<ul>
<li>Added warning when no user is configured for Users app. Removed note saying default admin password. (RLIT-2574)</li>
<li>Added a new public action (Popup_Editor_GetMessage) to RichWidgets to get the Notify Popup message. (ROU-142)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.0.424.3"><span id="Bug_Fixing_47"></span><h3 id="Bug_Fixing_45">Bug Fixing</h3>
<ul>
<li>Fixed a problem when using ListAppend and ListInsert functions containing an If expression in the List input parameter. (RPD-3984)</li>
<li>Fixed bug where sometimes when starting the Deploy Service, applications were not deployed automatically (RSCT-1761)</li>
<li>Fixes an issue where the Viewstate did not store nested web blocks for triggered events. (RPD-4070)</li>
</ul> </div></div><span id="Platform_Server_11.0.422.0"></span><h2 id="Platform_Server_11.0.422.0">Platform Server 11.0.422.0</h2><br/><div class="mt-include" id="s30760">
<div class="info"><p>Released on May 06, 2019</p></div>
<div class="mt-section" id="section_1" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.0.422.0"><span id="New_in_Platform_Server_Release_Apr.2019_2"></span><h3 id="New_in_Platform_Server_Release_Apr.2019">New in Platform Server Release Apr.2019</h3>
<ul>
<li>Clicking Environment/Module Management in the toolbar now opens Service Center in the default browser instead of render it directly inside Service Studio. (RICT-825)</li>
<li>We changed the SQL Injection warning message to advise you not to set the use of Expand Inline option to "Yes". The warning helps to follow solid SQL security practices. (RRCT-2128)</li>
<li>Improved the experience of the Users application. We gave it a new look and feel and made the following usability improvements:<br/>
— Page-specific links/actions were moved to inside the pages; the sidebar will now only display fixed links and recent items<br/>
— Added breadcrumbs to pages and pagination and records counter to all pages showing lists<br/>
— Added text filter in users sub-lists<br/>
— When a user does not have a username defined it appears as "Not Defined" in the lists so that you can click it<br/>
— Roles, Groups and Users dropdowns don't show the records already added to the lists; however, roles still show when they were inherited by group to allow overriding<br/>
— When a role is inherited by a group, it does not show the option to remove the role, since this operation is not possible<br/>
— Added the list of users able to access the application to the Application_List page – inspired by <a class="link-https" href="https://www.outsystems.com/ideas/4962/Users+Application+Bugs%2fImprovements" rel="external noopener nofollow" target="_blank">Rebecca Hall's idea</a> (RLIT-2343)</li>
<li>Added a new action Session_GetWebAppLoginInfo to the PlatformRuntime API that allows you to get user information in advanced REST authentication scenarios. (RRCT-2274)</li>
<li>The VerifySqlLiteral action from Sanitization API was deprecated in favor of BuildSafe_InClauseIntegerList and BuildSafe_InClauseTextList. These new actions are available in Platform Server 10.0.1005.0 and in Platform Server 11.0.422.0. (RRCT-2108)</li>
<li>Added instructions on importing the server configuration file (exported from the Deployment Controller) in the Front-end servers when upgrading to a new release. Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/6327/v11-installation-checklist-improvement" rel="external noopener nofollow" target="_blank">Kurt Vandevelde's idea</a>. (RSAT-1314)</li>
<li>The Platform Installer will now automate most of the prerequisites and performance tuning setup. The GUI has screens that guide you through this new step. Also, a new flag (/InstallPrerequisites=True) was added to unattended installation that is needed to signal explicitly that the installer should try to automate the prerequisites and performance tuning setup. (RSAT-1308)</li>
<li>Platform Server now requires Microsoft .NET Framework version 4.7.2. Installing this version will require you to reboot your server. (RSAT-1396)</li>
<li>The base image required for OutSystems applications running on Docker Containers Deployment Technology is now "microsoft/dotnet-framework:4.7.2-runtime". (RSAT-1397)</li>
<li>Upgraded RabbitMQ Client library to version 5.1.0. (RRCT-2142)</li>
<li>Upgraded Microsoft.AspNet.WebApi libraries to version 5.2.7. (RRCT-2143)</li>
<li>Replaced the OWASP HTML Sanitizer in Sanitization.xif by the <a class="link-https" href="https://github.com/mganss/HtmlSanitizer" rel="external noopener nofollow" target="_blank">HtmlSanitizer NuGet package</a>.<br/>
The SanitizeHtml action has the following differences when compared with the previous version:<br/>
— The <tt>&lt;noscript&gt;</tt> HTML tag is no longer allowed<br/>
— Some HTML attributes are no longer allowed: <tt>onfocus</tt>, <tt>onblur</tt>, <tt>onclick</tt>, <tt>onmousedown</tt>, <tt>onmouseup</tt>, <tt>noresize</tt>, <tt>background</tt><br/>
— The <tt>style</tt> attribute is now accepted (check the <a class="link-https" href="https://github.com/mganss/HtmlSanitizer#css-properties-allowed-by-default" rel="external noopener nofollow" target="_blank">list of CSS attributes allowed by default</a>)<br/>
— The sanitization of attribute values is less restrictive, with no security implications (e.g. the <tt>color</tt> attribute now accepts a wider range of different values)<br/>
— There might be some slight differences in the sanitized output, with no security implications (e.g. the new sanitizer replaces <tt>&lt;br/&gt;</tt> elements with <tt>&lt;br&gt;</tt>)<br/>
— The new sanitizer does not add a <tt>nofollow</tt> attribute to anchor elements (RRCT-2161)</li>
<li>Updated the following JavaScript libraries used by the mobile application runtime: 'decimal.js' to version 10.0.1, 'toformat' to version 2.0.0. (RTAF-91)</li>
<li>Implemented several optimizations that reduced the load time of "List Modules" and "Solution Details" pages in Service Center. (RSCT-1852)</li>
<li>On a first install, ServiceCenter will now be deployed into a dedicated application pool in IIS named "ServiceCenterAppPool".
On upgrade, if ServiceCenter exists in "OutSystemsApplications" application pool in IIS, ServiceCenter will be moved to a dedicated application pool named "ServiceCenterAppPool". If ServiceCenter is already in some other application pool, it will not be moved. (RSAT-1338)</li>
<li>Added to FactoryConfiguration the option to include X-Content-Type-Options header with nosniff as a method of preventing MIME sniffing from older browser versions. (RRCT-2270)</li>
<li>Service Center now links to the detach process documentation instead of launching the No Lock-in tutorial. (RICT-1199)</li>
<li>Header 'X-Content-Type-Options' with value 'nosniff' is now added by default to all server responses. Applications with custom solutions to achieve the same outcome should be reviewed to ensure compatibility with the new solution, or disable it using Factory Configuration (not recommended). (RRCT-2082)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/Platform_Server_11.0.422.0"><span id="Bug_Fixing_48"></span><h3 id="Bug_Fixing_46">Bug Fixing</h3>
<ul>
<li>Fixed incorrect character encoding in packaging of mobile applications. (RRCT-2216)</li>
<li>Fixed runtime error in client-side Aggregates with dynamic Order By's containing more than one attribute. (RSBO-54)</li>
<li>Fixed an issue that caused the Application 1-Click Publish to fail consistently when a previous 1-Click Publish aborted with an error. (RSCT-1693)</li>
<li>Fixed NullBinary() comparisons in client side with binaries being returned from server side aggregates. Previously it always returned "false" even when the binaries had no content. (RRCT-2279)</li>
<li>Fixed SOAP introspection not detecting some unsupported features. (RSBO-246)</li>
<li>Fixed the creation of Blank and Service modules to have the correct user provider set, instead of having the Template marked as user provider. (RRCT-2296)</li>
<li>Fixed an issue that prevented some OutSystems services from stopping when the Deployment Controller service was not running. (RRCT-2295)</li>
<li>Fixed an issue that caused Service Center to crash when changing the configuration of a mobile application. (RLIT-2490)</li>
<li>Fixed the errors related to retrieving mobile app authentication configuration that happened in some environments after upgrading to OutSystems 11 or after regenerating the authentication and encryption keys in Service Center. The error prevented mobile applications from working. (RPD-3794)</li>
<li>The User_Login action of the Users API no longer logs errors when the authentication is set to Active Directory or LDAP and the login is successful. (RLIT-2387)</li>
<li>Fixed the default action on the Create / Edit solution page on Service Center. Now the default action is to save the solution instead of searching. (RPD-3953)</li>
<li>Fixed query errors in some Users screens. (RPD-4015)</li>
<li>Fixed a problem when using ListAppend and ListInsert functions containing an If expression in the List input parameter. (RPD-3984)</li>
<li>The User_Login action of the Users API no longer aborts database transactions when an exception occurs. (RRCT-2189)</li>
<li>Fixed a rare problem that prevented custom Application and Screen Templates from being registered. (RSCT-1753)</li>
<li>Fixed an issue that was causing the error "Duplicate is not a valid operation inside a StartIteration/EndIteration block" when using cached actions. (RPD-3698)</li>
<li>Fixed a security issue that could cause session ids to be leaked with access to the Platform logs. CVSSv3.0 score 4.9 (Medium). (RRCT-2277)</li>
<li>Fixed a rare runtime error while running Aggregates when the Entity internal name was a reserved keyword. (RSBO-29)</li>
<li>Fixed SOAP introspection and compilation of WSDLs with enumerations inside &lt;list&gt; elements. (RSBO-272)</li>
<li>Changed how the machine memory is calculated in installation tuning scripts (when configuring worker process optimizations). Previous method could fail in some scenarios. (RPD-3685)</li>
<li>Fixed a runtime error while filtering booleans and date type in BPT tables. (RSBO-299)</li>
<li>Fixed a problem with Single Sign On on some scenarios with multiple frontends or containers. This could also lead to "Session fixation mismatch" errors. All existing sessions from applications in containers will be lost in the upgrade process.

(RRCT-2214)</li>
<li>Fixed an issue with SanitizeHTML when sanitizing URLs with = characters. (RPD-3978)</li>
<li>Fixed Configuration Tool error 'The device is not ready' during upgrades from previous versions. (RPD-3880)</li>
<li>Fixed an error during publish caused by using SOAP Web Services with enumerations in Mobile modules. (RSBO-219)</li>
<li>Japanese characters are now correctly saved to the database when used in the default value of site properties. (RPD-3775)</li>
<li>Fixed an issue where added or updated fields in an editable table were not being enabled after an Ajax refresh of a row. (RPD-3879)</li>
<li>Fixed an issue in the JSON Serialize widget that affected the serialization of Date and Time values. This was causing the JSON Deserialize widget to return empty values. (RPD-3970)</li>
<li>Fixed an issue while generating service code when a SOAP operation contained headers in its input/output parameters. (RPD-4030)</li>
<li>Fixed Invalid numeric precision/scale error when reading -2^96 Decimal value in SQL Server. (RPD-4059)</li>
<li>Fixed issue farm environments when the platform is installed on different disk locations. (RPD-3896)</li>
<li>Fixed bug that occurred when consuming SOAP Web Services that use the same schema type as request/response and fault. (RSBO-306)</li>
<li>Improved the warning message in wizard "Create Action to Bootstrap Data from Excel" when the attributes are not going to be included in the bootstrap. (RSBO-53)</li>
<li>Fixed an issue when bulk changing the Test Values of several attributes in an Aggregate that were reverting to their original value. This was only happening when the original value was not null. (RSBO-71)</li>
<li>Fixed compilation error caused by a missing validation for the Combo Box variable type. (RICT-1320)</li>
<li>Removed unused CSS code that could cause browsers to generate a 404 error when retrieving some resources used in the configuration console of AD and LDAP providers. Embedded a font that was previously being downloaded at execution time. (RSAT-1328)</li>
<li>Removed incorrect warnings that were shown in Configuration Tool when clicking on 'Test Connection' for database users. (RPD-3691)</li>
<li>Using the List_SortColumn_GetOrderBy function from RichWidgets in a SQL Query Parameter with the Expand Inline property enabled will no longer trigger a SQL Injection Warning. (RRCT-2106)</li>
<li>Fixed a visual glitch in the Native Platforms Tab of Service Studio. (RNMT-2430)</li>
<li>Fixed occasional crash when merging Web Screens. (RICT-1237)</li>
<li>Fixed an error that prevented you from upgrading a module with the dynamic join logic to OutSystems 11. (RPD-3674)</li>
<li>Fixed a problem which caused SOAP Web Services imported in version 11 to have incorrect information. This happened when the WSDL had an enumeration defined in a top-level element that is used directly in an input part. (RSBO-360)</li>
<li>Fixed occasional crash using the Search in several tabs at the same time. (RTAF-108)</li>
</ul>
<ul>
<li>The Entity right-click menu option "Advanced &gt; Import Image for 'EntityNamePicture' Entity" no longer appears in Service modules. (ABE-987)</li>
<li>The Module menu option "Import &gt; Image from File..." no longer appears in Service modules. (ABE-986)</li>
<li>"Service API" folder is no longer displayed in Web and Mobile modules that do not include referenced Service APIs. (ABE-1038)</li>
<li>The option "Add Resource as an Image" no longer appears when adding an image file to the resources of a Service module. (ABE-798)</li>
<li>Check Box, Combo Box, Input, Input Password, List Box and Radio Button Web widgets will now be created with new default classes. (RAFT-1297)</li>
<li>Dragging and dropping an Entity over a widget will accelerate the replacement of the widget data sources. Service Studio automatically replaces the Attribute and Entity names in the relevant properties. The substitution algorithm guesses the best match between the new data source and the Screen Template elements. (RAFT-1086)</li>
<li>Block events are now available in web applications. (RAFT-1090)</li>
<li>Improved experience when browsing and choosing screen templates. (RAFT-1201)</li>
<li>Added information on our privacy policy to the Submit Feedback window in Integration Studio and to the Consume SOAP Web Service error report window in Service Studio. (RINT-1864)</li>
<li>The creation of Docker container Deployment Zones is blocked in environments with Development purpose. (RLIT-1644)</li>
<li>Removed name clashing when promoting a style to a class in Styles Editor. (RICT-675)</li>
<li>Able to move LifeTime to a dedicated environment following a documented procedure. (RLIT-1887)</li>
<li>The LifeTime interface now marks applications that are deployed to containers with a badge so it's easy to distinguish them. (RLIT-1535)</li>
<li>It's now possible to define the Environment purpose using Service Center. (RLIT-1536)</li>
<li>For Each flow elements now use the Record List being iterated as their display name when the Label property is empty (Inspired by <a class="link-https" href="https://www.outsystems.com/ideas/3699/" rel="external noopener nofollow" target="_blank">Caio Santana's idea</a>). (RIUT-309)</li>
<li>New application icon for Service Applications. (ABE-978)</li>
<li>Improved the process to delete old deployment data in LifeTime. (RLIT-1718)</li>
<li>Improved reference model reflected in Lifetime Deployment Plan validation. (RLIT-1723)</li>
<li>Charts Mobile and Web are no longer part of the System Components and will start being distributed on Forge. (RSUT-1221)</li>
<li>Publishing the current version of a solution refreshes module references only in development environments. (ABE-1045)</li>
<li>The version of Highcharts web and mobile has been upgraded from version 4 to 6. (RSUT-1222)</li>
<li>Improved popup to add an application to a staging in LifeTime to have a default option selected by default. (RLIT-1993)</li>
<li>Improved the ability to access deployment plans to previous environments. (RLIT-1863)</li>
<li>Consumers of Service API Methods, Entities, Structures and Web Screens are no longer marked as outdated if their public API didn't change. (ABE-477)</li>
<li>It is now possible to override the default service endpoint for a SOAP 1.2 web service in Service Center. (RINT-899)</li>
<li>It is now possible to define the authentication type and the corresponding credentials for an imported SOAP 1.2 web service. (RINT-1225)</li>
<li>It is now possible to dynamically authenticate with different credentials per SOAP 1.2 web service method. (RINT-900)</li>
<li>Non-SOAP bindings (e.g. HTTP bindings) are now ignored when present in the WSDL file of a consumed SOAP 1.2 web service. (RINT-885)</li>
<li>Added SOAP 1.2 support for types created via "restriction", usually of the same type as the original type. Only the "maxLength" and "fractionDigits" restrictions are considered when creating the appropriate data types, and these restrictions will not be enforced at runtime. (RINT-854)</li>
<li>Added Integration Studio support for Visual Studio 2017. (RINT-490)</li>
<li>It is now possible to override the authentication credentials for a SOAP 1.2 web service in Service Center. (RINT-897)</li>
<li>Added support for consuming SOAP web services with nillable attributes. (RINT-835)</li>
<li>Device detection logic now supports devices with resolutions bigger than 1024px and iPhone X. (RAFT-1296)</li>
<li>The LifeTime experience for deploying applications with dependencies was revised to warn about possible runtime errors if the inconsistent consumer applications are not republished. (ABE-893)</li>
<li>It's no longer necessary to include "= True" or "= False" in boolean join conditions of Aggregates. (ABE-556)</li>
<li>Applications are now self sufficient regarding logging their own information and the logging mechanism do not rely on an external service (LogService). (RRCT-839)</li>
<li>OutSystems caching mechanism now uses RabbitMQ system to forward cache invalidation notifications to OutSystems applications. (RRCT-835)</li>
<li>It's now possible to store logs in a separate database from the one storing the data used by business applications and the data that supports the platform runtime (thanks to <a class="link-https" href="https://www.outsystems.com/ideas/132/Log+database+catalog" rel="external noopener nofollow" target="_blank">Didier Miller for highlighting this need as an idea</a>). (RRCT-1472)</li>
<li>Applications running on Docker containers can leverage Docker logs and Docker logging drivers to have visibility from logs that were sent to the event viewer or OSTraces. (RSAT-854)</li>
<li>Deprecated BeginReadUncommittedTransaction and BeginTransaction methods from RuntimePublic.Db API. (RSAT-791)</li>
<li>It's now possible to configure and see logs of consumed SOAP 1.2 web services in Service Center. (RINT-841)</li>
<li>Users are now notified when attempting to consume SOAP web services that contain unsupported features. (RINT-1299)</li>
<li>Added support for consuming SOAP web services with Choices. (RINT-1776)</li>
<li>Added support for custom virtual hosts in RabbitMQ (RRCT-1754)</li>
<li>The usage of SMS Flows in applications deployed to containers is now blocked. (RSAT-932)</li>
<li>OutSystems Management Consoles gives you the possibility to defined the hosting technology for you applications. That technology is now well visibility though their logos in Lifetime animations. (RSAT-769)</li>
<li>Moving an application from the "Classic Virtual Machines" to any hosting technology based on containers is blocked in case there are any SEO rules defined to that applications. (RSAT-820)</li>
<li>It's now blocked the configuration of SEO rules to applications set to any hosting technology based on containers. (RSAT-796)</li>
<li>Application debug mode no longer depends on environment type (e.g. DEV, QA), making it possible to debug applications in all environments. Introduced new types of environments to allow for more flexible management of infrastructures. (RSCT-1148)</li>
<li>Service Studio now shows a warning for modules that are set as self user provider but don't have "Is User Provider" set to "Yes" (RRCT-1584)</li>
<li>Renaming a Service API no longer makes consumer Modules incompatible but outdated instead. (ABE-967)</li>
<li>Renaming a Service API's Input or Output Parameter no longer makes consumer Modules incompatible but outdated instead. (ABE-969)</li>
<li>SOAP Web Service Methods now support default values in Input Parameters, Output Parameters and Structure Attributes of SOAP Web Services. The minOccurs/nillable WSDL attributes are now taken into consideration when determining mandatory Input Parameters and Structure Attributes. (RINT-1833)</li>
<li>Removed support for SMS feature. (RRCT-1639)</li>
<li>Application set to be deployed using Docker containers are now running using Hosted Web Core (HWC) instead of IIS. (RSAT-867)</li>
<li>Unattended Installation API was updated to take in consideration a possible split between platform database and logging database (RRCT-1783)</li>
<li>Entity and structure attributes, output parameters, and static entity records that are not used can now be deleted without forcing a refresh reference. (ABE-982)</li>
<li>Fix a problem while installing RabbitMQ using 32 bits command lines (RRCT-1810)</li>
<li>When creating new screens, developers can browse and use a pre-defined set of templates to accelerate the screen bootstrap (RAFT-1022)</li>
<li>Added support for consuming SOAP web services with Enumerations. (RINT-1764)</li>
<li>SOAP Enumerations are represented as Static Entities under the Data tab. (RINT-1489)</li>
<li>Inputs now have aria-required and aria-invalid attributes in web runtime applications. (RAFT-1292)</li>
<li>It's now possible to check the status of the invalidation cache mechanism for each front-end server in Service Center's Environment Health tab. (RRCT-1678)</li>
<li>Applications set to be deployed on Pivotal Cloud Foundry are now generated configured to be deployed in Pivotal Application Service running on Windows 2016. (RSAT-962)</li>
</ul>
</div><div class="mt-section" id="section_2" mt-section-origin="Support/Release_Notes/11/Platform_Server/397_Platform_Server_11.0.0.209"><span id="Bug_Fixing_49"></span><h3 id="Bug_Fixing_47">Bug Fixing</h3>
<ul>
<li>Fixed a security issue related to cached pages. (RPD-3270)</li>
<li>Fixed an issue that allowed disabled buttons to trigger inputs with the Enter key in IE browsers. (RPD-3151)</li>
<li>Hybrid infrastructures now allow on premises machines to edit front end servers. (RPD-2993)</li>
<li>Fixed an issue in LifeTime for cloud hybrid infrastructures that made the security settings inaccessible for all environments. (RPD-2827)</li>
<li>Fixed LDAP injection vulnerability. (RPD-3194)</li>
<li>Fixed an issue in iOS 11.3 mobile apps where the virtual keyboard did not open when the end-user touched an input very fast. (RPD-3198)</li>
<li>Fixed mobile apps becoming unresponsive after resuming from background in iOS 11.3. (RPD-3203)</li>
<li>Fixed an issue in iOS mobile apps that was causing one click to trigger two click events. (RPD-3204)</li>
<li>Fixed invalid call to client action error at aggregate's On After Fetch calls. (RPD-3216)</li>
<li>Deployment Controller service is shown as being down whenever stored procedure 'DeleteExpiredSessionVarsReturningDeletedRows' does not exist. (RPD-3304)</li>
<li>Fixed mobile eSpace list first and last element getting a height of 0 when the data source is an aggregate (RPD-3300)</li>
<li>Hybrid infrastructures now allow on premises machines to create zones. (RPD-3272)</li>
<li>Fixed issue that prevented Feedback Messages from being displayed if the screen action triggering the message ended with a Destination element navigating to the current screen. (RPD-3102)</li>
<li>Fixed issue in the Input_AutoComplete RichWidget that caused the screen to scroll to the top when using touch devices. (RPD-3093)</li>
<li>Improved Staging Process in LifeTime to always sync after a deployment plan execution. (RLIT-1885)</li>
<li>Blocked LifeTime environment from being registered on cloud. (RPD-3027)</li>
<li>Improved the discovering of the environment stack when LifeTime is on cloud. (RPD-3258)</li>
<li>Fixed issue that blocks users from login when their username is longer than 250 chars. (RPD-3234)</li>
<li>Fixed limitation in Service Center that blocked listing all the consumers and producers in the details of each eSpace. (RPD-3157)</li>
<li>Fixed error when using Integration Studio to import Entities with one or more columns with user-defined data types from an external SQL Server database. (RPD-2549)</li>
<li>Fixed a bug that prevented saving the list of records into the database. This is a reverted fix to #ABE-705 introduced in 10.0.804.0 to prevent infinite loops in compiling screen actions that have type conversion ListAppends. This fixes the issue that caused in-memory changes and failure to properly save the list of records into the database. They only way to save them was to use changed record attributes by elements other than the ListAppend operation and the entity actions. (RSCT-1399)</li>
<li>Fixed "Invalid key" runtime error after compiling a solution where a producer module added new Entity or Structure attributes and the consumer modules were not refreshed. (ABE-984)</li>
<li>Fixed bug that would sometimes cause infinite loops while compiling List Appends that performed type conversions contained in screen actions. (ABE-1003)</li>
<li>Fixed an issue while deploying native applications related to tagging native platforms. (RPD-3261)</li>
<li>Fixed Configuration Tool crash when SQL Server usernames have special characters. (RSAT-959)</li>
<li>Fixed problem where a process of Configuration Tool was stuck in background after exiting (RRCT-1823)</li>
<li>Fixed Configuration Tool not returning an error code when running in unattended mode and installation of ServiceCenter fails. (RSAT-955)</li>
<li>Fixed a problem where publishing simultaneously modules with identical names in different personal environments would result in having future publication attempts of those modules blocked. (RSCT-1287)</li>
<li>The debugger now works correctly for Service API Methods when the developer is not in the same network as the server. (ABE-980)</li>
<li>Fixed issue where false incompatibilities to extension entities/structures would be shown on the Manage Dependencies window. (ABE-1009)</li>
<li>Email's attachment's filenames are now correctly encoded. (RPD-3275)</li>
<li>Fixed an issue while generating database constraint names that sometimes would end with zeros instead of with a pseudo-random number. (RPD-3182)</li>
<li>Fixed RichWidgets InputAutoComplete/ListNavigation/ListOrderBy not working if the page was accessed using an URL that contained a different casing from the original page name. (RPD-2379)</li>
<li>Show RabbitMQ installation instructions for Platform upgrades (RPD-3327)</li>
<li>Fixed error while handling null SOAP 1.2 web service responses. (RINT-2336)</li>
<li>Fixed an issue that was keeping unnecessary files in the "repository" folder on the server, increasing the folder size. (RSCT-1227)</li>
<li>Fixed an issue with new classes created using "Save changes to reusable class" in Styles Editor. New classes that are created using already existing class names are not automatically renamed anymore. (RICT-786)</li>
<li>Fixed Service Studio crash when merging deleted widgets customized with the Styles Editor. (RICT-794)</li>
<li>Attributes in Record types are no longer marked as mandatory. (RPD-3226)</li>
<li>Fixed an issue that resulted in Service Studio crashing during merge. (RICT-787)</li>
<li>Fixed an issue that caused Service Studio to perform a DNS query for "host.servicestudio" when rendering Form or Editable Table widgets. (RPD-3177)</li>
</ul>
</div><div class="mt-section" id="section_3" mt-section-origin="Support/Release_Notes/11/Platform_Server/397_Platform_Server_11.0.0.209"><span id="Known_Issues_16"></span><h3 id="Known_Issues_14">Known Issues</h3>
<ul>
<li>Deployment Zones set to work with Amazon ECS and Azure Container Service don't show the From Image value stored when they were created.</li>
<li>
<p>Applications that call the built-in function CheckRole in Aggregates or SQL elements trigger the runtime error "The EXECUTE permission was denied on the object 'CheckRole'".</p>
<p>To overcome this issue, you have two alternative workarounds:</p>
<p>- Open the tab Platform in Configuration Tool and click the button Create/Update Database. This will set the correct permissions on the Platform Server database.<br/>
- Change the application logic to avoid calling CheckRole inside Aggregates and SQL elements.</p>
<p>This issue will be fixed in the GA version of OutSystems 11.</p>
</li>
</ul>
</div></div>
</div>
