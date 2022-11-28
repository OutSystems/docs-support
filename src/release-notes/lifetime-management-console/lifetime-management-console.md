---
locale: en-us
guid: 997c4a3d-c659-40ae-a3b8-2a6b61489fe8
app_type: traditional web apps, mobile apps, reactive web apps
---

<h1>Lifetime Management Console</h1>
<h2 id="LifeTime_Management_Console_11.12.0">LifeTime Management Console 11.12.0</h2>
<div class="info"><p>Released on Apr 20, 2022</p></div>
<h3 id="Bug_Fixing_0">Bug Fixing</h3>
<ul>
<li>The LifeTime Installation Checklist now includes the supported Oracle versions in the database software combo box. (RPM-2034)</li>
<li>Fixed an issue for cloud infrastructures causing an "Unauthorized operation" error in the Environments screen and preventing the database storage information to be displayed. (RPM-2279)</li>
<li>Improved LifeTime performance when creating new deployment plans in large factories. (RPM-583)</li>
</ul>

<h2 id="LifeTime_Management_Console_11.11.0">LifeTime Management Console 11.11.0</h2>
<div class="info"><p>Released on Mar 08, 2022</p></div>
<h3 id="New_in_LifeTime_Management_Console_11.11.0">New in LifeTime Management Console 11.11.0</h3>
<ul>
<li>It's now possible to register and unregister environments in LifeTime using the LifeTime API v2. (R11CT-850)</li>
<li>Updated the Platform Server version to 11.14.0. (RDOI-33)</li>
</ul>
<h3 id="Bug_Fixing_1">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a recursive iteration exception when accessing the Applications screen or the Application's detail screen. (R11CT-842)</li>
<li>Fixed a performance issue in Teams' synchronization. (RPM-2013)</li>
<li>Fixed an issue that caused a deployment to fail when the deployment plan included a new app with the staging option set to "Do Nothing" and that app required the selection of a deployment zone in the target environment. (RPM-2112)</li>
<li>Fixed an issue that caused the Top Browsers card on the Analytics screen to retrieve an empty list when clicking the pagination buttons for the card. (RPM-2121)</li>
<li>Now the Close_Staging_Process activity takes less time to finish preventing to timeout during a staging. (RPM-2148)</li>
<li>Solved a performance in staging screens that caused the staging edit, staging summary, and staging progress screens to have an increased load time. (RPM-2154)</li>
</ul>

<h2 id="LifeTime_Management_Console_11.10.8">LifeTime Management Console 11.10.8</h2>
<div class="info"><p>Released on Feb 02, 2022</p></div>
<h3 id="Bug_Fixing_2">Bug Fixing</h3>
<ul>
<li>The LifeTime Installation Checklist now includes information about the "Install Prerequisites" option. (RPM-1242)</li>
<li>Fixed an error generating mobile apps when the custom Extensibility Configurations defined in the LifeTime settings include malformed or incorrect JSON. (RPM-1544)</li>
<li>Fixed an issue causing the failure of a deployment plan validation when the server has low memory available. (RPM-1589)</li>
<li>Fixed an issue causing deployment plans to fail due to lack of permissions to reference dependencies not included in the deployment plan. (RPM-1689)</li>
<li>The LifeTime Installation Checklist now correctly displays the step to install .NET Core 3.1 Runtime &amp; Hosting Bundle for Windows when updating to a new release or cumulative patch. (RPM-1998)</li>
<li>Added traceability to updates of the "Enable HTTP Strict Transport Security (HSTS)" setting. (RPM-908)</li>
</ul>
<h3 id="Known_Issue">Known Issue</h3>
<ul>
<li>This LifeTime version suffers from poor access times when users navigate to staging related pages (e.g. Staging_Edit, Staging_Summary and Staging_Progress). This issue has been fully addressed from LifeTime version 11.11.0 onwards. The performance degradation is more notable when a large number of applications are staged.
</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.7">LifeTime Management Console 11.10.7</h2>
<div class="info"><p>Released on Jan 06, 2022</p></div>
<h3 id="Bug_Fixing_3">Bug Fixing</h3>
<ul>
<li>Fixed a typo in the placeholder text of date fields on the Staging list page. (R11CT-396)</li>
<li>Fixed an issue in the synchronization queue that prevented some events from being processed. (R11CT-699)</li>
<li>Fixed an issue that was blocking the user to access the Create a Plugin popup. (R11CT-760)</li>
<li>Fixed an issue that caused errors when deploying several applications with different versions that contain the same module. This issue occurred while using features from a LifeTime private EAP. (RPM-1769)</li>
</ul>
<h3 id="Known_Issue">Known Issue</h3>
<ul>
<li>This LifeTime version suffers from poor access times when users navigate to staging related pages (e.g. Staging_Edit, Staging_Summary and Staging_Progress). This issue has been fully addressed from LifeTime version 11.11.0 onwards. The performance degradation is more notable when a large number of applications are staged.
</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.6">LifeTime Management Console 11.10.6</h2>
<div class="info">
<p>Released on Dec 07, 2021</p>
</div>
<h3 id="Bug_Fixing_4">Bug Fixing</h3>
<ul>
<li>Fixed an issue synchronizing teams with many IT users. (R11CT-618)</li>
<li>Fixed a performance issue by replacing the deprecated action VerifySqlLiteral() from Sanitization API with the corresponding BuildSafe_InClause*() action. (R11CT-73)</li>
<li>Fixed an issue when configuring the deployment zone during the application deployment. This issue was preventing the selection of a deployment zone different from the default for new applications containing an existing module previously deployed in the target environment. (RPM-1683)</li>
<li>Fixed .Net Core version in Installation Checklist. (RPM-1697)</li>
<li>Fixed a database error during deployment when the message stored in the AuditEvent entity exceeded 2000 characters. (RPM-1734)</li>
<li>The Team Edit screen now has a filter to display only active or inactive users. (RPM-1746)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.5">LifeTime Management Console 11.10.5</h2>
<div class="info">
<p>Released on Nov 12, 2021</p>
</div>
<h3 id="Bug_Fixing_5">Bug Fixing</h3>
<ul>
<li>Fixed a very remote scenario where an IT user may lose permissions after an environment synchronization. (RPM-1729)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.4">LifeTime Management Console 11.10.4</h2>
<div class="info">
<p>Released on Nov 03, 2021</p>
</div>
<h3 id="Bug_Fixing_6">Bug Fixing</h3>
<ul>
<li>Fixed an error occurring in some scenarios during the setup of the Secure Endpoint for Cloud environments. (R11CT-522)</li>
<li>Fixed a high severity vulnerability by upgrading the packaged RabbitMQ to 3.8.21. (RPM-1278)</li>
<li>The Timer Cleanup_ModuleCaches now runs daily instead of weekly. (RPM-1326)</li>
<li>Solved an upgrading issue that prevented the publishing of LifeTimeMiniHub module in ISV licensed environments. (RPM-1547)</li>
<li>Fixed an issue causing the option "Continue with errors" to be hidden when staging applications using the LifeTime console. This issue occurred only in Cloud environments. (RPM-1558)</li>
</ul>
<h3 id="Known_Issues_0">Known Issues</h3>
<ul>
<li>The Installation Checklist for LifeTime 11.10.4 incorrectly states that the product requires ".NET Core 2.1 Runtime Hosting Bundle for Windows". Instead, from this version onwards, the product requires ".NET Core 3.1 Runtime Hosting Bundle for Windows"</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.3">LifeTime Management Console 11.10.3</h2>
<div class="info">
<p>Released on Sep 29, 2021</p>
</div>
<h3 id="Bug_Fixing_7">Bug Fixing</h3>
<ul>
<li>Fixed an issue when tagging applications that would hide the Tag button when an error occurs on version validation. (R11CT-330)</li>
<li>Changing the status of an IT user (active/inactive) is now logged in Service Center's General Log. (RPD-5169)</li>
<li>Fixed an issue in the users' synchronization process that was causing delay in the synchronization of applications. (RPM-1247)</li>
<li>Fixed a problem in the staging progress screen causing the Abort button to be incorrectly disabled. (RPM-1538)</li>
<li>Fixed an issue causing performance degradation during system timers execution for OutSystems Cloud infrastructures in timezones misaligned with the customer business hours. (RPM-398)</li>
<li>It's now possible to apply and get Content Security Policy (CSP) settings to and from an environment through LifeTime API v2. (RPM-438)</li>
<li>Fixed an issue for OutSystems hybrid infrastructures preventing environments already removed from the infrastructure from being self-managed. (RPM-809)</li>
</ul>
<ul>
<li>Fixed an access control vulnerability in a popup screen. CVSSv3.1 score 4.3 (Medium) (RPM-1097)</li>
<li>Fixed HTML Injection vulnerabilities in multiple screens. CVSSv3.1 score 3.4 (Low) (RPM-1180)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.2">LifeTime Management Console 11.10.2</h2>
<div class="info">
<p>Released on Aug 31, 2021</p>
</div>
<h3 id="Bug_Fixing_8">Bug Fixing</h3>
<ul>
<li>Fixed the validation of mandatory version tags related to the mobile apps. (R11CT-246)</li>
<li>Fixed deployment process getting stuck in "Retrieving application from version control" when synchronizing users in batches. (R11CT-266)</li>
<li>Fixed the app name display in the Application list for apps that belong to a team. (R11CT-283)</li>
<li>Fixed the LifeTime installation checklist by removing the step to install the system components, as they are no longer required in the process. (R11CT-287)</li>
<li>Fixed an issue affecting cloud environments that generated the error "You don't have permission to get application" in the error logs during sync. (R11CT-319)</li>
<li>Fixed miscalculation of the outdated applications for deployment in big factories. The issue could affect deployment plans in big factories when LifeTime needed to check many outdated apps. (RPM-1148)</li>
<li>Fixed protocol in links to Service Studio. (RPM-985)</li>
</ul>
<h3 id="Known_Issues_1">Known Issues</h3>
<ul>
<li>In some advanced scenarios, LifeTime may consume an excessive amount of memory when validating a staging plan. In extreme scenarios, this may prevent the staging from being validated successfully. The problem is fixed in all LifeTime versions starting from 11.10.3.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.1">LifeTime Management Console 11.10.1</h2>
<div class="info">
<p>Released on Jul 29, 2021</p>
</div>
<h3 id="Bug_Fixing_9">Bug Fixing</h3>
<ul>
<li>Improved the spacing and alignment between the application update options on the Distribution tab in the deployment wizard for mobile applications. This configuration is only available when the "Configure Mobile application updates distribution" Technical Preview feature is enabled. (R11CT-131)</li>
<li>Fixed an issue in the endpoint "POST /deployments/{DeploymentKey}/{Command}/" of LifeTime API v2 causing a 500 Internal Server Error response when setting the "RedeployOutdated" parameter to false. (R11CT-186)</li>
<li>Fixed an issue causing deployment plans to keep their status as Running after being forcefully terminated. (RPD-4852)</li>
</ul>
<h3 id="Known_Issues_2">Known Issues</h3>
<ul>
<li>In some advanced scenarios, LifeTime may consume an excessive amount of memory when validating a staging plan. In extreme scenarios, this may prevent the staging from being validated successfully. The problem is fixed in all LifeTime versions starting from 11.10.3.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.10.0">LifeTime Management Console 11.10.0</h2>
<div class="info">
<p>Released on Jul 01, 2021</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.10.0">New in LifeTime Management Console 11.10.0</h3>
<ul>
<li>LifeTime installation checklist now reflects the new modules preparation step introduced in Platform Server 11.12.0. (R11CT-150)</li>
<li>The Email property is now mandatory when creating or updating an user through the User Management screen in Lifetime. This change doesn't affect existing users, unless you update them. (RIDT-835)</li>
</ul>
<h3 id="Bug_Fixing_10">Bug Fixing</h3>
<ul>
<li>Reusing a plan deployed with the Deploy Custom option now correctly keeps all the settings used in the original plan. (R11CT-137)</li>
<li>The list of entities from external databases configured during the deployment plan is no longer limited to 50 entries. (RPM-1123)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.12.0. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.12.0">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.9.1">LifeTime Management Console 11.9.1</h2>
<div class="info">
<p>Released on Jun 02, 2021</p>
</div>
<h3 id="Bug_Fixing_11">Bug Fixing</h3>
<ul>
<li>Fixed an issue preventing the development of LifeTime plugins in an environment where LifeTime had been previously installed. (R11CT-34)</li>
<li>Fixed the moment when runtime settings are applied during application deployment. (R11CT-44)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.11.2. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.11.2">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.9.0">LifeTime Management Console 11.9.0</h2>
<div class="info">
<p>Released on May 07, 2021</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.9.0">New in LifeTime Management Console 11.9.0</h3>
<ul>
<li>Improved LifeTime performance by optimizing the execution of the synchronization processes related to environments. These improvements are more noticeable in large factories. (RLIT-4244)</li>
<li>Removed the old environment registration experience. (RLIT-4348)</li>
<li>Added the ability to search by applications on the deployment plans screen. Also, improved the experience by separating the advanced filters. Inspired by <a href="https://www.outsystems.com/ideas/10076/search-for-application-on-deployment-plans-of-lifetime">Rebecca Hall's idea</a>. (RLIT-4446)</li>
<li>You can now use the Maintenance Mode feature to set an environment into a special state that will prevent connections between LifeTime and that specific environment. (RLIT-4562)</li>
</ul>
<h3 id="Bug_Fixing_12">Bug Fixing</h3>
<ul>
<li>Fixed a UI issue causing the LifeTime header to overlap popup windows. (RLIT-4293)</li>
<li>Fixed a missing feedback message during the environment registration wizard, when the total number of users exceeds the license limit. (RLIT-4311)</li>
<li>Fixed an issue that was causing LifeTime to throw an error when pressing the "Add to Deployment Plan" button. (RLIT-4493)</li>
<li>Fixed an issue when removing the on-prem environment in a hybrid infrastructure. (RLIT-4498)</li>
<li>Fixed an issue causing a deployment to abort when two different users try to continue the deployment at the same time. (RLIT-4509)</li>
<li>Fixed an issue causing the environment names to be duplicated on the feedback message when saving the Technical Preview features. (RLIT-4510)</li>
<li>Fixed an issue causing the synchronization icon not to show when an environment is synchronizing the User Management screens. (RLIT-4512)</li>
<li>Fixed screen elements misalignments on the Add Domain Certificate screen, for cloud environments. (RLIT-4525)</li>
<li>Fixed screen elements misalignments on the User's detail screen. (RLIT-4526)</li>
<li>Reviewed the Brazilian Portuguese (pt-BR) translations in IT users management and permissions, environment registration wizard, and staging flow screens. (RLIT-4552)</li>
<li>The number of server-side events discarded by LifeTime Analytics during the group data phase is now being correctly accounted for in the logs. (RLIT-4612)</li>
<li>Fixed the "App Feedback" and "End-user Management" links on the Applications screen, to consider the public hostname (when applicable). (RPD-3448)</li>
<li>Fixed an issue that prevents the overriding of the "Execute deployments in two stages" setting when re-registering an environment previously registered in LifeTime. (RPD-3805)</li>
<li>Fixed the "Manage User and Roles" permission tooltip on Roles list screen for cloud infrastructures. (RPD-3894)</li>
<li>Removed dependency from LifeTimeSDK to modules of LifeTime application (preventing the development of new plugins). (RPM-1023)</li>
<li>Drastically reduced the likelihood of LifeTime environment synchronization processes entering into deadlock. (RPM-1429)</li>
<li>Fixed an issue that caused the staging slot to be locked when the staging throws an error. Now the staging is marked as aborted. (RPM-595)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.8.4">LifeTime Management Console 11.8.4</h2>
<div class="info">
<p>Released on Apr 21, 2021</p>
</div>
<h3 id="Bug_Fixing_13">Bug Fixing</h3>
<ul>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.10.4. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.10.4">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.8.3">LifeTime Management Console 11.8.3</h2>
<div class="info">
<p>Released on Mar 03, 2021</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.8.3">New in LifeTime Management Console 11.8.3</h3>
<ul>
<li>Improved the messages returned if some error occurs when using LifeTime self-service VPN connection to OutSystems Cloud. (RCFT-5073)</li>
<li>Lifetime now enforces secure (HTTPS) connections with the managed environments. This will not be applied to infrastructures that already have registered environments using HTTP. (RLIT-3539)</li>
</ul>
<h3 id="Bug_Fixing_14">Bug Fixing</h3>
<ul>
<li>Fixed a missing warning during the environment registration, when the environment being registered is already registered in another LifeTime. (RLIT-4312)</li>
<li>Fixed an issue that caused duplicated roles to be displayed in the environment registration screen. (RLIT-4313)</li>
<li>Fixed an issue that caused Team's unique key (GUID) to be lost when editing a Team in LifeTime user interface. (RLIT-4426)</li>
<li>Fixed an issue that caused LifeTime Analytics to start processing indefinitely when there are invalid events being collected from the monitored environments. (RLIT-4435)</li>
<li>Fixed an issue in LifeTime Analytics that caused request events generated by non Traditional applications to be invalid. (RLIT-4439)</li>
<li>Improved the environment registration process for cloud infrastructures. (RPD-4820)</li>
<li>Platform users no longer impact the user pool. (RPM-597)</li>
<li>Fixed an issue in POST /users of LlifeTime API v2 where the incorrect error code was returned. CVSSv3.1 score 4.3 (Medium). (RPM-684)</li>
<li>Fixed restrictions on LifeTime for unprivileged users. CVSSv3.1 score 4.3 (Medium). (RPM-707)</li>
<li>Fixed a security issue that could allow a brute force attack while changing passwords. CVSSv3.1 score 2.8 (Low). (RPM-727)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.8.2">LifeTime Management Console 11.8.2</h2>
<div class="info">
<p>Released on Jan 21, 2021</p>
</div>
<h3 id="Bug_Fixing_15">Bug Fixing</h3>
<ul>
<li>Fixed an issue in LifeTime API v2 that caused an error when obtaining and using the link to download the binary file of reactive applications. (RPM-631)</li>
<li>Fixed an issue for cloud infrastructures that prevented the display of all the environments in the Shared Database Usage area of the Environments page. It's now possible to scroll the complete list of environments. (RPM-666)</li>
<li>Improved the environment registration process for cloud infrastructures. (RPD-4820)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.10.2. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.10.2">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.8.1">LifeTime Management Console 11.8.1</h2>
<div class="info">
<p>This is a preliminary version of the document.</p>
</div>
<h3 id="Bug_Fixing_16">Bug Fixing</h3>
<ul>
<li>Improved environment registration for cloud environments (RPD-4820)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.1. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.1">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.8.0">LifeTime Management Console 11.8.0</h2>
<div class="info">
<p>Released on Dec 09, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.8.0">New in LifeTime Management Console 11.8.0</h3>
<ul>
<li>On the Applications screen, LifeTime now shows a link to the documentation on how to deploy an application in case there are no deployments finished yet. (RLIT-4218)</li>
<li>Added functionality to create deployment plans through the Deployment Plans screen, by clicking the "Create new deployment plan" button and choosing the source and target environments. (RLIT-4167)</li>
<li>Improved LifeTime performance by optimizing the execution of the synchronization processes related to applications, users, and roles. These improvements are more noticeable in large factories. (RLIT-4127)</li>
</ul>
<h3 id="Bug_Fixing_17">Bug Fixing</h3>
<ul>
<li>Fixed the missing scroll of the popup displayed when selecting "Deploy Custom" or "Show Details" option after creating a deployment plan. This issue was preventing the usage of these options for applications with more than five modules. (RLIT-4215)</li>
<li>Fixed an environment setting that prevented LifeTime Analytics to retrieve analytics data from that environment. (RLIT-4080)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.1. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.1">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.7.5">LifeTime Management Console 11.7.5</h2>
<div class="info">
<p>Released on Nov 11, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.7.5">New in LifeTime Management Console 11.7.5</h3>
<ul>
<li>You can now request database users in LifeTime to improve troubleshooting and manipulate data. These users are temporary and nominal, ensuring that only legitimate users can carry on with this privileged access to data. (RCVT-909)</li>
</ul>
<h3 id="Bug_Fixing_18">Bug Fixing</h3>
<ul>
<li>Fixed an issue causing the date filters on the Deployment Plans page to be displayed incorrectly. (RLIT-4182)</li>
<li>Fixed Japanese translation for the Technical Preview link. (RPD-5179)</li>
<li>Fixed an issue occurring in Azure infrastructures that caused a false positive flag on the firewall when selecting the Discard plan functionality. (RLIT-4161)</li>
<li>Fixed an issue that was preventing the usage of the Reuse Plan feature. (RPD-5253)</li>
<li>Fixed an issue on the Technical Preview screen that prevented the environment toggles to assume the correct value when toggled more than once. (RLIT-4146)</li>
<li>Fixed a visual bug causing an unnecessary scroll on the tag details popup while editing a staging. (RLIT-4145)</li>
<li>Fixed an issue in endpoint DELETE /applications/{ApplicationKey}/versions/{VersionKey}/ of LifeTime API v2 that was preventing the deletion of old application versions. (RPD-5172)</li>
<li>Fixed an issue preventing checkboxes to appear correctly when configuring domain certificates in OutSystems Cloud. (RLIT-4101)</li>
<li>Fixed an issue in LifeTime SDK that prevented sample data to be imported in some cases. (RLIT-4100)</li>
</ul>
<h3 id="Know_Issues">Know Issues</h3>
<ul>
<li>Wrong environment setting may prevent LifeTime Analytics to retrieve analytics data from that environment.</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.1. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.1">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.7.4">LifeTime Management Console 11.7.4</h2>
<div class="info">
<p>Released on Oct 23, 2020</p>
</div>
<h3 id="Bug_Fixing_19">Bug Fixing</h3>
<ul>
<li>Fixed issue on validation that blocks deployment execution. This issue was found in LifeTime Management Console - 11.7.3 (Build 778). (RLIT-4177)</li>
</ul>
<h3 id="Know_Issues">Know Issues</h3>
<ul>
<li>Wrong environment setting may prevent LifeTime Analytics to retrieve analytics data from that environment.</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.1. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.1">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.7.3">LifeTime Management Console 11.7.3</h2>
<div class="info">
<p>Released on Oct 14, 2020</p>
</div>
<h3 id="Bug_Fixing_20">Bug Fixing</h3>
<ul>
<li>Fixed an issue in Lifetime SDK that was preventing to add or refresh Lifetime SDK dependencies in LifeTime Plugins. (RLIT-4066)</li>
<li>Fixed small visual bugs: long environment names are now being trimmed; in the deployment options, the label "Tagged by" now doesn't overflow out of the popup; the refresh applications tooltip now shows correctly in front of the header. (RLIT-4034)</li>
<li>Fixed an issue that caused the reset of the tag version to 0.1 or 0.1.1 when syncing an environment. (RLIT-3913)</li>
<li>Fixed an issue that was preventing the certificate options to be selected when adding a domain certificate in OutSystems Cloud. (RLIT-4067)</li>
<li>Fixed an issue where LifeTime could mark incorrectly a module to be deleted when re-validating a deployment plan. (RLIT-4040)</li>
<li>Fixed issue in LifeTimeSDK that prevented Sample Data to be imported in some cases. (RLIT-4100)</li>
</ul>
<h3 id="Know_Issues">Know Issues</h3>
<ul>
<li>Wrong environment setting may prevent LifeTime Analytics to retrieve analytics data from that environment.</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.1. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.1">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.7.1">LifeTime Management Console 11.7.1</h2>
<div class="info">
<p>Released on Sep 24, 2020</p>
</div>
<h3 id="Bug_Fixing_21">Bug Fixing</h3>
<ul>
<li>Fixed an issue causing applications containing only extensions to be deployed to the wrong deployment zone. (RPD-5136)</li>
<li>Fixed several visual issues in the interface: the display of the environment warning/error messages; the size of the environment cards; the display of the environment registration wizard when the scroll is active; scroll in "Add application role" popup. (RLIT-4008)</li>
<li>Fixed issue on LifetimeSDK preventing the refreshing of Plugins references (RLIT-4066)</li>
<li>The endpoint GET /deployments/{deployment_key} of LifeTime API v2 now obtains also any module that will be deleted if that deployment is executed. (RLIT-4000)</li>
<li>Fixed issue preventing certificate options to be selected when adding a domain certificate in the cloud. (RLIT-4067)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.1. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.1">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.7.0">LifeTime Management Console 11.7.0</h2>
<div class="info">
<p>Released on Aug 26, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.7.0">New in LifeTime Management Console 11.7.0</h3>
<ul>
<li>You can now change your VPN routes in self-service without the need to contact OutSystems support. (RCVT-421)</li>
<li>Changed the term "Early Access Features" to "Technical Preview". (RLIT-3930)</li>
<li>LifeTime interface now has a cleaner and updated look and feel. (RLIT-3939)</li>
</ul>
<h3 id="Bug_Fixing_22">Bug Fixing</h3>
<ul>
<li>Fixed an issue occurring while validating the deployment plan, which was preventing the deployment operation. (RLIT-3644)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.9.0. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.9.0">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.6.2">LifeTime Management Console 11.6.2</h2>
<div class="info">
<p>Released on Apr 27, 2021</p>
</div>
<h3 id="Bug_Fixing_23">Bug Fixing</h3>
<ul>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.8.4. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.8.4">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.6.1">LifeTime Management Console 11.6.1</h2>
<div class="info">
<p>Released on Jul 29, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.6.1">New in LifeTime Management Console 11.6.1</h3>
<ul>
<li>OutSystems Cloud VPN provisioning is now automated. It's also possible to retrieve the VPN configuration file from LifeTime. (RCVT-107)</li>
<li>Added two new early access features that will optimize the synchronization of users, roles, and applications. These features are Optimize users and roles synchronization process and Optimize app synchronization process. (RLIT-3627)</li>
<li>Improved LifeTime performance in factories with a high volume of data. (RLIT-3867)</li>
</ul>
<h3 id="Bug_Fixing_24">Bug Fixing</h3>
<ul>
<li>Fixed an error when defining custom Extensibility Configurations for an environment using a long JSON. This fix applies to OutSystems environments running Platform Server 11.10.0 or higher. (RLIT-3796)</li>
<li>Fixed a visual glitch in User and Service Account pages when changing the selected role associated with the User or Service Account. (RLIT-3903)</li>
<li>Fixed issue where it was possible to download the error report by an anonymous user. CVSSv3.0 score 5.3 (Medium). (RLIT-3901)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.8.2.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.6.0">LifeTime Management Console 11.6.0</h2>
<div class="info">
<p>Released on Jul 08, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.6.0">New in LifeTime Management Console 11.6.0</h3>
<ul>
<li>Added capabilities to support the platform in Mumbai AWS region. (RCVT-370)</li>
<li>Improved the performance of the synchronization processes for applications status in factories with a large number of environments and applications. (RLIT-3830)</li>
</ul>
<h3 id="Bug_Fixing_25">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the data migration popup to be launched when opening the Analytics page in new installations. (RLIT-3797)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.8.2.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.5.4">LifeTime Management Console 11.5.4</h2>
<div class="info">
<p>Released on Apr 27, 2021</p>
</div>
<h3 id="Bug_Fixing_26">Bug Fixing</h3>
<ul>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.7.6. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.7.6">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.5.3">LifeTime Management Console 11.5.3</h2>
<div class="info">
<p>Released on Jun 05, 2020</p>
</div>
<h3 id="Bug_Fixing_27">Bug Fixing</h3>
<ul>
<li>Fixed a bug that was causing the LifeTime to show wrong information about permissions in the user screen in some scenarios. (RPD-5046)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.7.3.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.5.2">LifeTime Management Console 11.5.2</h2>
<div class="info">
<p>Released on May 15, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.5.2">New in LifeTime Management Console 11.5.2</h3>
<ul>
<li>The setting to enable the PWA is now kept when staging an app between environments. This means that when you enable/disable the PWA distribution for an app in the development environment, the setting is the same in the next environment after the staging. (RTAF-1908)</li>
</ul>
<h3 id="Bug_Fixing_28">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was preventing users with "Monitor and Add Dependencies" permission level over a Team from accessing the Analytics data for that Team's applications. (RPD-3676)</li>
<li>Fixed an issue that revealed system modules in the environments. (RLIT-3492) (RLIT-3648)</li>
<li>Fixed an issue in LifeTime SDK that caused a database lock when invoking the action Deployment_Get with an empty DeploymentKey. (RLIT-3657)</li>
<li>Fixed an issue in LifeTime API v2 that caused the endpoint /users/{UserKey}/ to return a 405 error. (RLIT-3659)</li>
<li>Fixed the list of available roles when setting the user's role for a team or application. (RLIT-3718)</li>
<li>The link for Security Settings now appears correctly for on-premise environments in OutSystems Cloud LifeTime. (RPD-4788)</li>
<li>Fixed an issue that prevented roles with character '+' to synchronize properly. (RLIT-3642)</li>
<li>Due to an issue with the synchronization of the settings between LifeTime and Service Center, we removed the newly introduced single sign-on (SSO) setting from LifeTime. Please use Service Center of the environment to manage the SSO settings (go to Service Center &gt; Administration &gt; Security &gt; Applications authentication &gt; Common login settings). (RTAF-2729)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.7.3.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.5.1">LifeTime Management Console 11.5.1</h2>
<div class="info">
<p>Released on Apr 13, 2020</p>
</div>
<h3 id="Bug_Fixing_29">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused LifeTime to make applications with no differences available to be added in Deployment plans. (RLIT-3570)</li>
<li>Fixed an error when selecting a role during the creation of a new service account. (RLIT-3572)</li>
<li>Now the logged-in user can't change his/her own roles. (RLIT-3575)</li>
<li>The link "Delete Team" is no longer displayed when the logged-in user has no permission to delete teams. (RLIT-3577)</li>
<li>The link "New User" is no longer displayed when the logged-in user has no permission to create new users. (RLIT-3580)</li>
<li>Fixed an error in the new deployment plan wizard to configure application settings (Early Access) occurring when selecting a deployment zone and there is only one application in the deployment. (RLIT-3589)</li>
<li>Fixed a layout issue in the Environments section of Options menu for cloud environments. (RLIT-3616)</li>
<li>Improved the performance of LifeTime synchronization process in factories with a large number of environments and applications. (RPD-3870), (RLIT-3606), (RPD-3605)</li>
<li>Fixed an issue that was preventing users with "Monitor and Add Dependencies" permission level over a Team from accessing the Analytics data for that Team's applications. (RPD-3676)</li>
<li>Fixed an issue that caused some errors, related to REST calls in the LifeTime environment, to be created in the Error Log without an error message. (RPD-4826)</li>
<li>Fixed an issue that caused a deployment to become stuck in some specific situations. For example, after using the Retry Plan option for a plan that failed during compilation or when configuring deployment zones for the first time for an application. (RPD-4851)</li>
<li>Fixed an issue in the old deployment wizard that was preventing the "Save Plan Notes" button from saving the deployment plan. (RPM-1716)</li>
<li>Fixed an issue that occurred when validating a deployment plan. The problematic scenario involved a new Structure attribute whose type is an Entity identifier from another module. This happened when there were consumer applications for the Structure which weren't included in the plan. (RSBO-1271)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.5.0">LifeTime Management Console 11.5.0</h2>
<div class="info">
<p>Released on Mar 12, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.5.0">New in LifeTime Management Console 11.5.0</h3>
<ul>
<li>Added a new API method to LifeTime API v2 (former LifeTime Deployment API v2) to retrieve application templates available in a given environment. (RLIT-3390)</li>
<li>Added a new API method to LifeTime API v2 (former LifeTime Deployment API v2) to create an application in a given environment. (RLIT-3391)</li>
<li>Added a new set of API methods to LifeTime API v2 (former LifeTime Deployment API v2) to manage users. These include: List all users, create a user, update a user, get the details of a user, set the password for a user, grant/revoke a role in an application to a user. (RLIT-3392)</li>
<li>Added a new set of API methods to LifeTime API v2 (former LifeTime Deployment API v2) to manage Teams. These include: List all teams, create a team, update a team, get the details of a team, delete a team, add/remove an application to a team, add/remove a user to a team. (RLIT-3393)</li>
<li>Added a new set of API methods to LifeTime API v2 (former LifeTime Deployment API v2) to manage Roles. These include: List all roles, create a role, update a role, get the details of a role, delete a role and get the available permission levels. (RLIT-3388)</li>
</ul>
<h3 id="Bug_Fixing_30">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a timeout while creating a deployment plan containing an application with an extension connecting to external databases. (RDEV-1356)</li>
<li>Changed the process of cleaning up the outdated modules of a staging to avoid cleaning up records from stagings that are still in use. (RLIT-3520)</li>
<li>Fixed method User_GetApplicationPermissions from LifeTime Services API, that was not filtering the result by the given ApplicationKey. (RPD-4821)</li>
<li>Fixed a bug that makes the application appears with broken references in LifeTime when tagging application in an Environment using OutSystems 10. (RPD-4094)</li>
<li>Added missing permissions information in My Settings screen. Fixed a bug that allowed the user to add permissions in Teams but not in Applications, in some specific cases. (RLIT-3423)</li>
<li>Fixed an issue that caused an error during the step “Upgrading and refreshing modules of '&lt;Application Name&gt;' while publishing a solution in Service Center. (RPC-810)</li>
<li>Fixed a bug that occurred when validating a plan. The problematic scenario involved a new Structure attribute whose type is an entity identifier from another module. This happened when there were consumer applications for the Structure which weren't included in the plan. (RSBO-1271)</li>
<li>Fixed an issue that caused an error when trying to access Deployment Summary when someone changes the deployment at the same time. (RLIT-3552)</li>
<li>Fixed issue that caused a deployment to become stuck in certain situations (after Reusing a plan that failed during compilation or when configuring deployment zones for the first time for an application) (RPD-4851)</li>
<li>Fixed error that appeared when selecting a deployment zone and there was only one application in the deployment. (RLIT-3589)</li>
<li>Improved the message shown when an error occurs registering an on-premises environment in hybrid infrastructure in cloud and it is not possible to connect using HTTPS. (RPD-4152)</li>
<li>Fixed an error related with user permissions that could occur when LifeTime is installed during an existing synchronization process. (RLIT-3425)</li>
<li>Fixed Users and Roles details screens crashing when the role permissions in one or more environments are not defined. (RPD-4787)</li>
<li>Fixed issue that could cause deployments to be stuck when the LifeTime environment does not have connection to the Internet. (RLIT-3547)</li>
<li>Removed misleading error log when LifeTime is not able to create an Application version in an environment due to the absence of some modules. (RLIT-3550)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.4.4">LifeTime Management Console 11.4.4</h2>
<div class="info">
<p>Released on May 13, 2021</p>
</div>
<h3 id="Bug_Fixing_31">Bug Fixing</h3>
<ul>
<li>Fixed issue with Popup_Editor_init when adding applications to a deployment. (RPM-1070)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.0.615. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.0.615">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.4.3">LifeTime Management Console 11.4.3</h2>
<div class="info">
<p>Released on Apr 27, 2021</p>
</div>
<ul>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue that could cause unavailability of the platform. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.0.615. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.0.615">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.4.2">LifeTime Management Console 11.4.2</h2>
<div class="info">
<p>Released on Jan 31, 2020</p>
</div>
<h3 id="Bug_Fixing_32">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a timeout while creating a deployment plan containing an application with an extension connecting to external databases. (RDEV-1356)</li>
<li>Fixed an issue that caused an error during the step “Upgrading and refreshing modules of '&lt;Application Name&gt;' while publishing a solution in Service Center. (RPC-810)</li></ul>

<h2 id="LifeTime_Management_Console_11.4.0">LifeTime Management Console 11.4.0</h2>
<div class="info">
<p>Released on Jan 30, 2020</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.4.0">New in LifeTime Management Console 11.4.0</h3>
<ul>
<li>Added impact capacity when editing a Role: on save, LifeTime now warns about what users will be affected by the changes in that Role. (RLIT-3112)</li>
<li>Added visibility in permission screens to the "Create Applications" and "Add Dependencies to System" options, when they are activated. (RLIT-3111)</li>
<li>Added a preview on User_Edit / ServiceAccount_Edit pages of the permissions the User / Service Account will have when creating a new User / Service Account or changing its default role. (RLIT-3079)</li>
<li>It’s now possible to configure Entities from external databases during deployment. (RDEV-1244)</li>
<li>Reviewed Brazilian Portuguese (pt-BR) translations in all screens related to IT users management and permissions. (RLIT-3076)</li>
</ul>
<h3 id="Bug_Fixing_33">Bug Fixing</h3>
<ul>
<li>The popup to add users to a team is now correctly showing the default role of the listed users. (RLIT-3365)</li>
<li>Fixed UI issues when resizing the screen to resolutions under 1024px. (RLIT-3366)</li>
<li>The display of user permissions in the Application_Permissions screen is now showing the correct labels for Full Control and Access permission levels instead of the equivalent application permission levels. (RLIT-3403)</li>
<li>Fixed an issue in LifeTime Deployment API v1 that was preventing to tag a mobile application using the native platform name, e.g. Android (v1). (RLIT-3395)</li>
<li>Fixed the create application feature inside the Team_edit screen, that was requesting the user to select a team again, instead of selecting the team automatically. (RLIT-3367)</li>
<li>Fixed an issue that was causing some applications to not be presented in the applications list. (RLIT-3120)</li>
<li>Corrected the permissions for DBConnections and DBCatalogs screens so they can be accessed with the same permission level, i.e, "Monitor and Reference Applications" or higher. (RLIT-2977)</li>
<li>Fixed an issue that caused an error when deploying old application tags. (RPD-3745)</li>
</ul>
<h3 id="Known_Issues_3">Known Issues</h3>
<ul>
<li>Creating a deployment plan containing modules with entities from external databases can fail during the "Configure applications settings" step.</li>
<li>In some scenarios when publishing a Solution in Service Center an error occurs during the “Upgrading and refreshing modules of '&lt;Application Name&gt;'" step. (RPC-810)</li>
</ul>
<h2 id="LifeTime_Management_Console_11.0.329">LifeTime Management Console 11.0.329</h2>
<div class="info">
<p>Released on May 13, 2021</p>
</div>
<h3 id="Bug_Fixing_34">Bug Fixing</h3>
<ul>
<li>Fixed issue with Popup_Editor_init when adding applications to a deployment. (RPM-1070)</li>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.0.615. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.0.615">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_11.0.328">LifeTime Management Console 11.0.328</h2>
<div class="info">
<p>Released on Apr 27, 2021</p>
</div>
<ul>
<li>Fixed a security issue related to CVE-2019-11358 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-621)</li>
<li>Fixed a security issue related to CVE-2015-9251 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-622)</li>
<li>Fixed a security issue related to CVE-2020-7656 that could affect the behavior of client-side runtime. CVSSv3.1 score 6.1 (Medium). (RPM-623)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.3 (High)." (RPM-657)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 9.9 (Critical). (RPM-683)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPM-786)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.2 (High) (RPM-813)</li>
</ul>
<strong>Compatibility and Additional Resources</strong>
<ul>
<li>Includes Platform Server 11.0.615. Check the <a href="https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.0.615">release notes</a> and <a href="https://www.outsystems.com/Downloads/search/Platform-Server/11/">additional resources</a> for that Platform Server.</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Dec.2019">LifeTime Management Console Release Dec.2019</h2>
<div class="info">
<p>Released on Dec 30, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Dec.2019">New in LifeTime Management Console Release Dec.2019</h3>
<ul>
<li>It is now possible to add one IT user to multiple teams with the same role. (RLIT-3161)</li>
<li>Improved the name of some permissions and the permissions' description on the Role's detail screen. Also, the permission levels displayed on the User's detail screen now match the permission levels displayed on the Role's detail screen. (RLIT-2813)</li>
<li>Improved the detail screen for Users and Service Accounts to display more clearly the default role and roles assigned through teams/applications. Added also the ability to change the assigned roles directly on this detail screen. (RLIT-3113)</li>
<li>Added new environment security options to force Secure and SameSite properties in cookies generated by the platform. Check the document <a href="https://success.outsystems.com//Support/Enterprise_Customers/Maintenance_and_Operations/Upcoming_changes_in_cookie_handling_in_Google_Chrome#Release_schedule">Upcoming changes in cookie handling in Google Chrome</a> for more information. (RTAF-1866)</li>
</ul>
<h3 id="Bug_Fixing_35">Bug Fixing</h3>
<ul>
<li>Fixed an issue in the Role's detail screen that was incorrectly listing users as being assigned to the role. (RLIT-3143)</li>
<li>Fixed a crash when trying to create a new deployment plan due to duplicate records. (RPD-4076)</li>
<li>Fixed an issue that caused the Secure Endpoint feature to be visible in on-premise environments registered in cloud infrastructures. (RPD-4229)</li>
</ul>
<h3 id="Known_Issues_4">Known Issues</h3>
<ul>
<li>In some scenarios when publishing a Solution in Service Center an error occurs during the “Upgrading and refreshing modules of '<application name="name">&lt;Application Name&gt;'" step. For more information check <a href="https://success.outsystems.com//Support/Unlisted/Support_Team/Unsorted/Invalid_login_when_publishing_a_solution_in_Service_Center_-_Known_Issue">documentation</a>. (RPC-810)</application></li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Nov.2019">LifeTime Management Console Release Nov.2019</h2>
<div class="info">
<p>Released on Nov 21, 2019</p>
</div>
<h3 id="Bug_Fixing_36">Bug Fixing</h3>
<ul>
<li>Fixed an issue for hybrid infrastructures after a failure when registering an on-premises environment. After the failure, the Applications screen and the Environments screen were displaying a different set of environments. (RLIT-3266)</li>
<li>Fixed an issue that was causing existing synchronization processes to keep running after unregistering an environment. (RLIT-3265)</li>
<li>Fixed an issue in the logic of the clean-up process for old module versions that was preventing the deletion of some data. (RPD-4208)</li>
<li>Fixed an issue that was preventing the execution of the clean-up process for old module versions when the timer had reached the maximum number of retries. (RPD-4514)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Oct.2019_CP1">LifeTime Management Console Release Oct.2019 CP1</h2>
<div class="info">
<p>Released on Oct 30, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Oct.2019_CP1">New in LifeTime Management Console Release Oct.2019 CP1</h3>
<ul>
<li>Added a new permission, "Add References to System", to configure who can add new dependencies to public elements of System module. This permission is applicable when granted in the user default role. (RLIT-3160) (RLIT-3160)</li>
<li>We have split the permission level “Reuse and Monitor Applications” into two permission levels, “Open and Debug Applications” and “Monitor and Reference Applications”. This way you have a more granular permission model, as you can now give permission to monitor applications without the permission to open and debug. During the upgrade, the previous role “Reuse and Monitor Applications” is mapped to “Open and Debug Applications”. (RLIT-2804)</li>
<li>Added a new permission, "Create Applications", to configure who can create applications and associate them directly to a team. During the upgrade, this new permission is set to ON for the roles having “Change Deploy Applications” permission level. (RLIT-2796)</li>
<li>Added a new permission level, “Access to Environment”, which allows users to log in to an environment without the permission to see the applications. (RLIT-2790)</li>
</ul>
<h3 id="Bug_Fixing_37">Bug Fixing</h3>
<ul>
<li>Fixed an issue in the environment registration wizard that was limiting to 50 the list of roles to map and the users to import. This issue was also limiting the list of environments to 50 when choosing the environment position in the infrastructure. (RLIT-3235)</li>
<li>Fixed an issue in LifeTime that could cause the deploy of the incorrect application versions when using option "Refresh Applications" in "Create Deployment Plan" screen. (RLIT-3212)</li>
<li>Fixed a cross-site scripting vulnerability. CVSSv3.0 score 4.8 (Medium). (RLIT-3166)</li>
<li>Fixed repeated requests to publish a solution in the target environment when there's a timeout in the publish operation. (RPD-4400)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Sep.2019_CP1">LifeTime Management Console Release Sep.2019 CP1</h2>
<div class="info">
<p>Released on Oct 16, 2019</p>
</div>
<h3 id="Bug_Fixing_38">Bug Fixing</h3>
<ul>
<li>Fixed issue in LifeTime that may cause the deploy of wrong versions when using Refresh Applications feature. (RLIT-3212)</li>
</ul>
<h3 id="Known_Issues_5">Known Issues</h3>
<ul>
<li>Using the option "Refresh Applications" in "Create Deployment Plan" screen may not include new modules or remove deleted modules when using Tag and Deploy options. As a workaround, if you need to refresh the applications by this time because there are new modules or modules were removed, discard the deployment plan and create a new one.</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Sep.2019">LifeTime Management Console Release Sep.2019</h2>
<div class="info">
<p>Released on Oct 03, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Sep.2019">New in LifeTime Management Console Release Sep.2019</h3>
<ul>
<li>Fixed an issue where LifeTime environment registration would make a HTTP request when using an HTTPS only configuration. (RPD-4238)</li>
<li>Improved performance of the Early Access Features configuration page in LifeTime. (RLIT-2938)</li>
</ul>
<h3 id="Bug_Fixing_39">Bug Fixing</h3>
<ul>
<li>Fixed issue that prevents using "Continue with errors" option while executing a deployment that has settings to configure. (RLIT-2936)</li>
<li>Fixed issue in LifeTime that prevented on-premises environments registered in Cloud Infrastructure to sync properly due to multiple users with a specific Administrator role. (RPD-3582)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Jul.2019">LifeTime Management Console Release Jul.2019</h2>
<div class="info">
<p>Released on Jul 30, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Jul.2019">New in LifeTime Management Console Release Jul.2019</h3>
<ul>
<li>Finished deployment plans can now be reused. There's a new link in the deployment execution screen and in the deployments list allowing you to create a new plan based on a previous plan. You can choose which environments you want to execute the new deployment plan to/from and whether you want to keep the same versions as the previous plan, or just the same applications. (RLIT-2697)</li>
<li>Deployment plans can now be accessed in the Applications tab by clicking the "Deployment Plans" link. In this screen, view and search the deployment plans, their current status, as well as access their details and available actions. (RLIT-2698)</li>
<li>Created a screen to easily manage the Early Access Features for environments and LifeTime. (RLIT-2780)</li>
<li>Capability to allow administrators to reschedule automatic updates in cloud infrastructures to a new suggested date. (RLIT-2824)</li>
<li>When retrying or reusing a deployment plan you can now understand if some applications were removed from the previous plan due to unavailability. (RLIT-2837)</li>
</ul>
<h3 id="Bug_Fixing_40">Bug Fixing</h3>
<ul>
<li>Fixed an issue in LifeTime that caused cleanup old data to only remove partial data. (RLIT-2840)</li>
<li>Fixed an issue in the validation details screen where an error icon would be shown even if the validation issue is only a warning. (RLIT-2853)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Jun.2019">LifeTime Management Console Release Jun.2019</h2>
<div class="info">
<p>Released on Jul 11, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Jun.2019">New in LifeTime Management Console Release Jun.2019</h3>
<ul>
<li>Aborted deployment plans can now be easily retried. There's a new link in the deployment execution screen allowing you to create a new plan with the same applications and versions as the aborted plan. (RLIT-2696)</li>
<li>You can now refresh the applications in a deployment plan while the plan is being edited. This allows you to include new application changes done after plan creation, as well as having an up-to-date view on the environments and their applications and versions, without needing to recreate the deployment plan. (RLIT-2695)</li>
</ul>
<h3 id="Bug_Fixing_41">Bug Fixing</h3>
<ul>
<li>Fixed the navigation to Service Center when you need to enter configurations before proceeding with the execution of a deployment plan. (RLIT-2775)</li>
<li>Fixed display of Abort button while executing a deployment plan. (RLIT-2774)</li>
<li>Fixed the displayed running version in the source environment when editing a deployment plan, when refreshing the plan editing screen or when returning to a saved deployment plan. Note: This issue is only fixed for newly created deployment plans. (RLIT-2748)</li>
<li>Fixed an issue in LifeTime that returned an incorrect message when the user was checking for new updates in Personal or Trial cloud environments. (RLIT-2768)</li>
<li>Improved queries using a full join in LifeTime deployment validation stage. Affects only Oracle and SQL Server. (RPD-4147)</li>
</ul>
<h3 id="Known_Issues_6">Known Issues</h3>
<ul>
<li>Using the option "Refresh Applications" in "Create Deployment Plan" screen may cause the deploy of the incorrect application versions. As a workaround, if you need to refresh the applications by this time, discard the deployment plan and create a new one. Fixed in LifeTime Management Console Release Sep.2019 CP1.</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_May.2019">LifeTime Management Console Release May.2019</h2>
<div class="info">
<p>Released on May 27, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_May.2019">New in LifeTime Management Console Release May.2019</h3>
<ul>
<li>Added a new Early Access Feature in LifeTime that enables you to configure the value of application Site Properties while planning a deployment. (RLIT-2644)</li>
<li>Added support to enable or disable Early Access Features. (RLIT-2641)</li>
</ul>
<h3 id="Bug_Fixing_42">Bug Fixing</h3>
<ul>
<li>Fixed an issue for OutSystems hybrid infrastructures that was preventing the registration of on-premises environments when the environment connects to LifeTime using HTTPS. (RPD-3781)</li>
<li>For OutSystems hybrid infrastructures, it's now possible to set the maintenance window for the LifeTime environment by setting the maintenance window for the leftmost cloud environment in the infrastructure. Previously it wasn't possible to do this if the leftmost environment registered was on-premise. (RLIT-2613)</li>
<li>Improved the performance of LifeTime synchronization process when there are multiple applications being published at the same time. (RPD-3183)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Apr.2019">LifeTime Management Console Release Apr.2019</h2>
<div class="info">
<p>This is a preliminary version of the document.</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Apr.2019">New in LifeTime Management Console Release Apr.2019</h3>
<ul>
<li>We have now added support to enable or disable early access features at the environment level. (RSCT-1810)</li>
</ul>
<h3 id="Bug_Fixing_43">Bug Fixing</h3>
<ul>
<li>Fixed an issue for OutSystems hybrid infrastructures that was preventing the registration of on-premises environments when the environment connects to LifeTime using HTTPS. (RPD-3781)</li>
<li>For OutSystems hybrid infrastructures, it's now possible to set the maintenance window for the LifeTime environment by setting the maintenance window for the leftmost cloud environment in the infrastructure. Previously it wasn't possible to do this if the leftmost environment registered was on-premise. (RLIT-2613)</li>
<li>Improved performance of LifeTime synchronization process when there are multiple applications being published at the same time. (RPD-3183)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Mar.2019">LifeTime Management Console Release Mar.2019</h2>
<div class="info">
<p>Released on Mar 18, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Mar.2019">New in LifeTime Management Console Release Mar.2019</h3>
<ul>
<li>You can now see application warnings (for example, indicating that an application is outdated) in the deployment edit screen when planning a deployment. (RLIT-1315)</li>
<li>The Deployment Status method in LifeTime Deployment APIs v1 and v2 will only return the deployment status 'finished' after the completion of the sync operation. (RLIT-2249)</li>
<li>Updated the embedded platform server to Platform Server 11 - Release Jan.2019 Cumulative Patch 2. (RLIT-2489)</li>
</ul>
<h3 id="Bug_Fixing_44">Bug Fixing</h3>
<ul>
<li>Fixed an issue in LifeTime that automatically set the purpose of the environment incorrectly in cloud environments. (RLIT-2415)</li>
<li>Fixed an issue when choosing "Mark Hotfix as Solved" for mobile apps if the application hadn't been deployed to the next environment yet. (RPD-3871)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Feb.2019">LifeTime Management Console Release Feb.2019</h2>
<div class="info">
<p>Released on Feb 25, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_Release_Feb.2019">New in LifeTime Management Console Release Feb.2019</h3>
<ul>
<li>Improved LifeTime cleanup process to also remove unused data from completed stagings. (RLIT-2287)</li>
<li>Added change log information to the output structure "ApplicationVersion" for methods "GET /applications/{ApplicationKey}/versions/" and "GET /applications/{ApplicationKey}/versions/{VersionKey}/" in LifeTime Deployment API v2. Added also the optional input "ChangeLogFilter" to method "GET /applications/{ApplicationKey}/versions/" to filter the returned list of versions by change logs containing the required keyword. (RLIT-2395)</li>
<li>It is now possible to delete application versions (LifeTime tags) using the new method "DELETE /applications/{ApplicationKey}/versions/{VersionKey}/" of LifeTime Deployment API v2. This feature will allow to delete in the environments the old module versions previously tagged by LifeTime. It requires Platform Server 10.0.912.0 (OutSystems 10 environments) or Platform Server 11 - Release Sep.2018 Cumulative Patch 1 (OutSystems 11 environments). Inspired by <a href="https://www.outsystems.com/ideas/3562/">Harlin Setiadarma's idea</a>. (RLIT-2399)</li>
<li>A new API method is now available in LifeTime Deployment API v2 for downloading the .oap file of a specific application version, "GET /applications/{ApplicationKey}/versions/{VersionKey}/content/". This method can be used to backup the code of an application version before deleting it. It requires Platform Server 10.0.1005.0 (OutSystems 10 environments) or Platform Server 11 - Release Jan.2019 Cumulative Patch 1 (OutSystems 11 environments). (RLIT-2169)</li>
<li>Added new input "TargetEnvironmentKey" to the API method "GET /deployments/" of LifeTime Deployment API v1 and v2 that allows to filter the deployments list by target environment. Improved also the return codes to differ the case when the user does not have permissions to view the requested deployments from the case when there are no deployments that match the search. (RLIT-2368)</li>
<li>In LifeTime Deployment API v2, the attribute “ModuleVersionKeys” of structure "ApplicationVersionCreate" has been deprecated and is now optional. When creating a new application version using the method "POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/", passing a value in attribute “ModuleVersionKeys” will behave as previously, validating the module versions. (RLIT-2369)</li>
</ul>
<h3 id="Bug_Fixing_45">Bug Fixing</h3>
<ul>
<li>Fixed an issue in API method "POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/" of LifeTime Deployment API v2 that was preventing the creation of mobile apps versions. (RLIT-2410)</li>
<li>Fixed a security vulnerability. CVSS v3.0 score 7.1 (High) - Full details to be released in May 2019 (RLIT-2388)</li>
<li>Fixed an issue in LifeTime synchronization that could cause environment features to be unavailable. (RLIT-2381)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Jan.2019_(Sentry)">LifeTime Management Console Release Jan.2019 (Sentry)</h2>
<div class="info">
<p>Released on Jan 15, 2019</p>
</div>
<h3 id="New_in_LifeTime_Release_Jan.2019_(Sentry)">New in LifeTime Release Jan.2019 (Sentry)</h3>
<ul>
<li>When deploying a mobile application to the next staging environment, LifeTime now uses the Mobile Apps Build Service (MABS) version associated with the application tag being deployed. The mobile app version and the MABS version for the deployed application are now displayed during the staging, as well as in the Application Version History page. (RLIT-2380)</li>
<li>Upgraded SharpZipLib library to version 1.0.0. (RRCT-2144)</li>
</ul>
<h3 id="Bug_Fixing_46">Bug Fixing</h3>
<ul>
<li>Fixed a security vulnerability. CVSS v3.0 score 7.1 (High). (RLIT-2388)</li>
<li>Fixed an error when applying the security settings for an application. (RLIT-2329)</li>
<li>The information on the available database storage for cloud environments is now showing correctly. (RLIT-2332)</li>
<li>Updated the version of Charts application distributed with LifeTime. (RLIT-2357)</li>
<li>We fixed a bug in Lifetime Analytics that caused low performance and time-outs in scenarios where more than one environment has monitoring enabled. We did this by correcting an internal timer responsible for harvesting and grouping data used in Lifetime Analytics. (RPD-3600)</li>
<li>The unattended installation and upgrade process now validates the prerequisites. (RSAT-1023)</li>
<li>Fixed an issue in the installation process that was accepting as valid certain unsupported .Net Framework versions. (RSAT-1169)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Jan.2019">LifeTime Management Console Release Jan.2019</h2>
<div class="info">
<p>Released on Jan 15, 2019</p>
</div>
<h3 id="New_in_LifeTime_Release_Jan.2019">New in LifeTime Release Jan.2019</h3>
<ul>
<li>When deploying a mobile application to the next staging environment, LifeTime now uses the Mobile Apps Build Service (MABS) version associated with the application tag being deployed. The mobile app version and the MABS version for the deployed application are now displayed during the staging, as well as in the Application Version History page. (RLIT-2380)</li>
</ul>
<h3 id="Bug_Fixing_47">Bug Fixing</h3>
<ul>
<li>Increased visibility on how to access a deployment plan that propagates hotfixes backward. (RPD-2789)</li>
<li>Fixed issue in LifeTime synchronization process that blocks applications from being synced. (RLIT-2379)</li>
<li>Improved the environment registration wizard UI for lower screen sizes, avoiding the overlap of screen elements. (RLIT-2374)</li>
<li>The summary step of the environment registration wizard now shows the correct value for the "Environment Position in Infrastructure". (RLIT-2372)</li>
<li>Fixed an issue in the synchronization process of environment features to LifeTime which could cause LifeTime misbehavior. (RLIT-2365)</li>
<li>Fixed a "Module with key <key> was not found" error during the environment synchronization. (RPD-3662)</key></li>
<li>Decreased the time that LifeTime takes to display the error message of deployments that failed to generate the mobile app package. (RPD-3064)</li>
<li>Updated the version of Charts application distributed with LifeTime. (RLIT-2357)</li>
<li>Fixed an error in LifeTime Deployment API v2 while deploying applications to containers. (RLIT-2338)</li>
<li>We fixed a bug in Lifetime Analytics that caused low performance and time-outs in scenarios where more than one environment has monitoring enabled. We did this by correcting an internal timer responsible for harvesting and grouping data used in Lifetime Analytics. (RPD-3600)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Dec.2018">LifeTime Management Console Release Dec.2018</h2>
<div class="info">
<p>Released on Dec 20, 2018</p>
</div>
<h3 id="New_in_LifeTime_Release_Dec.2018">New in LifeTime Release Dec.2018</h3>
<ul>
<li>Improved the environment registration wizard to better guide the user when registering their environments in LifeTime. (RLIT-2285)</li>
<li>Added support for defining Mobile Extensibility Configurations in LifeTime, per Application and Environment. It requires Platform Server Release Sep.2018 CP1 or higher. (RLIT-1503)</li>
<li>Added support for redeploying outdated applications using the LifeTime Deployment API v2. (RLIT-1981)</li>
<li>Improved LifeTime UI by replacing the shadows between environments with borders. (RLIT-2239)</li>
<li>When listing the applications that a user can access, Lifetime now lists also the applications that the user has been granted with access for being member of a team. (RLIT-2200)</li>
<li>Added more information in ApplicationVersion structure in LifeTime Deployment API. (RLIT-2168)</li>
</ul>
<h3 id="Bug_Fixing_48">Bug Fixing</h3>
<ul>
<li>Users filter in the Audit Logs page is not displaying duplicated users anymore. (RLIT-2335)</li>
<li>The environments information displayed in Roles tab of User Management section is now reflecting users permissions. (RLIT-2334)</li>
<li>Fixed an issue that was causing the incorrect registration of on-premises environments in a cloud infrastructure. (RLIT-2333)</li>
<li>The information on the available database storage for cloud environments is now showing correctly. (RPD-3432)</li>
<li>Fixed an error when applying the security settings for an application. (RPD-3651)</li>
<li>The change log screen of an application is now correctly showing the name of the user that performed the change. (RLIT-2327)</li>
<li>Fixed an issue in the environment synchronization process that was incorrectly removing modules from LifeTime cache. (RPD-3607)</li>
<li>Fixed the number of applications displayed in the staging summary when the deployment plan contains more than 50 applications. (RLIT-2320)</li>
<li>Fixed the action User_ChangeUsername of LifeTime Services API that was incorrectly re-encrypting the password of the user. (RPD-3531)</li>
<li>Fixed an issue that was causing the "Deploy Now" message to be incorrectly displayed when two-stages deployment was enabled. (RLIT-2346)</li>
<li>Fixed security issue in LifeTime that allow a user to change its own username. (RPD-3595)</li>
<li>LifeTime does not log expected errors anymore when synchronizing an environment. (RLIT-2211)</li>
<li>Fixed the error message in LifeTime Deployment API about unsuccessful request for the Create Version call. (RLIT-2195)</li>
<li>Fixed the LifeTime error screen related to the missing user session. (RLIT-2191)</li>
<li>Fixed an error in accessing the LifeTime audits when a username is not defined. (RLIT-2190)</li>
<li>Fixed an error that happened after choosing the Synchronise Now option from an Environment in LifeTime, in cases where the user didn't have the correct permissions. (RLIT-2189)</li>
<li>Fixed a bug related to checking the Nativizer status that caused LifeTime to crash. (RLIT-2188)</li>
<li>Fixed the bug in LifeTime Analytics that prevented actions with long names to appear in the Screen Details. (RPD-3427)</li>
<li>Fixed a wrong message in the LifeTime staging. The users now see the correct message “you have no permission to deploy” instead of the incorrect “you have no permissions to tag”. (RPD-3319)</li>
<li>Fixed the default browser behavior to ask to save the login credentials. Now the password fields in OutSystems applications such as Service Center or LifeTime have the "autocomplete" property set to "off" by default. (RPD-3464)</li>
<li>Fixed an issue that caused an unspecified error in LifeTime when registering an environment with a higher version than LifeTime. LifeTime now prevents adding environments to the infrastructure if the environment that is being added has higher version. (RPD-3347)</li>
<li>Fixed issue in LifeTime that prevented a user with 'Reuse Monitor' role to validate a deployment plan. (RPD-3480)</li>
<li>Fixed issue in LifeTime Deployment API that caused inconsistent data in a deployment with Tag Deploy optioons. (RLIT-2251)</li>
<li>Fixed inconclusive exception message when there was an error creating a user in LifeTime (RLIT-2257)</li>
<li>Fixed message when there was an invalid request while creating a deployment. (RLIT-2250)</li>
<li>Changing the password of the current logged in user now requires typing the current password. (RLIT-2237)</li>
<li>Fixed an issue that was causing LifeTime not to detect missing dependencies in upgrade scenarios. (RLIT-2224)</li>
<li>Fixed an issue that was preventing the restore of LifeTime communication with an environment after changing the environment properties. (RLIT-2216)</li>
<li>Fixed a navigation error in accessing the environment change log when the environment is not defined. (RLIT-2205)</li>
<li>Fixed the lifetime bootstrap process that was failing in white labeling environments. (RPD-3523)</li>
<li>Timer to delete data from old module versions will now finish properly (without an error). (RPD-3583)</li>
<li>Fixed URL used by LifeTime to redirect users to configurations pages of environments. (RPD-3302)</li>
<li>Improved the performance of application data synchronization after 1-Click Publish. (RLIT-2236)</li>
<li>Fixed URL used by LifeTime to redirect users to configurations pages of environments. Requires Environments running Platform Server Release Jan.2019 or later. (RLIT-2281)</li>
</ul>
<h2 id="LifeTime_Management_Console_Release_Sep.2018">LifeTime Management Console Release Sep.2018</h2>
<div class="info">
<p>Released on Sep 26, 2018</p>
</div>
<h3 id="New_in_Release_Sep.2018">New in Release Sep.2018</h3>
<ul>
<li>From this version, LifeTime needs to be installed in a dedicated environment.</li>
<li>LifeTime can manage environments with Platform Server release 10 or 11.</li>
<li>Improved the add application to a staging in LifeTime to select a default option by default. (RLIT-1993)</li>
<li>Added support for deployment to containers using LifeTime. (RLIT-1537)</li>
<li>The LifeTime Analytics has been updated so the device database information now includes recent devices, operating systems, and browsers. (RLIT-2152)</li>
<li>When an application is associated to a Deployment Zone configured to use containers as hosting technology, OutSystems platform will generate a bundle with all the assets needed to allow build and run your application in a container. (RSAT-385)</li>
<li>Added Role_GetEnvironmentPermissionsLevels method to RoleManagementService API from LifeTimeServices. Removed deprecated EnvironmentManagementService and ApplicationManagementService APIS, as well as UserManagementService\User_UpdateApplicationPermission method from LifeTimeServices. (RLIT-1561)</li>
<li>Improved LifeTime validations performance by adding a new weekly timer which deletes older cached module versions that are not longer required in the infrastructure (RLIT-1797)</li>
</ul>
<h3 id="Bug_Fixing_49">Bug Fixing</h3>
<ul>
<li>Fixed the bug that caused the “Continue Deployment” button not to show in LifeTime. It occurred in some scenarios when multiple users were logged-in to the same Staging_Progress page. (RPD-3290)</li>
<li>Improved the description of PlatformTeams parameter of Team_List action, in TeamManagementService. (RLIT-2079)</li>
</ul>
<h3 id="Breaking_Changes_0">Breaking Changes</h3>
<ul>
<li>LifeTime is now only supported when installed in a dedicated environment.
<ul>
<li><strong>Rationale:</strong> LifeTime now has its own release cycle to allow for better and faster improvements in LifeTime. To achieve this, LifeTime must be run, installed and maintained in a separate environment from the development pipeline environments in customer infrastructures.</li>
</ul>
</li>
<li>LifeTime Analytics now has a historical data retention policy. This means that, by default, LifeTime Analytics will start deleting data older than 365 days.
<ul>
<li><strong>Rationale:</strong> To optimize the performance of LifeTime Analytics, OutSystems introduced a mechanism to limit the amount of data kept by Analytics in the database. This was achieved by including a clean-up process that deletes data older than N days.</li>
<li><strong>Workaround:</strong> This policy can be removed by setting the <code>LifeTime.Analytics.DataRetentionPeriod</code> parameter to <code>0</code> in the OSSYS_PARAMETER table after the upgrade and before timers are switched on. Disabling data retention policy is not recommended and can cause performance degradation in Lifetime Analytics.</li>
</ul>
</li>
<li>The Frontend Name used in Performance Monitor no longer follows the configuration defined in Service Center; it will always be the Machine Name in uppercase.
<ul>
<li><strong>Rationale:</strong> This change was made to improve information consistency across other monitoring and log sources. It also became a required change with the introduction of containers support, since the platform no longer has control over what servers have which applications running and applications do not depend on the servers they are running on.</li>
<li><strong>Workaround:</strong> This information is not used by any of the built-in analytics components. Any custom modules using analytics information that might be using the Frontend Name may need to be adapted.</li>
</ul>
</li>
<li>The configuration parameter <code>LifeTime.AddApplicationsExplicitly</code>, along with the previous deployment planning implementation in LifeTime which used this parameter, were removed. From now on, LifeTime only supports the new deployment planning functionality.
<ul>
<li><strong>Rationale:</strong> The new deployment planning functionality is mature and has been widely adopted. As such, the previous deployment planning implementation in LifeTime is no longer available and the configuration parameter <code>LifeTime.AddApplicationsExplicitly</code> is no longer needed.</li>
</ul>
</li>
</ul>
<h2 id="LifeTime_Management_Console_11.0.307.0">LifeTime Management Console 11.0.307.0</h2>
<div class="info">
<p>Released on Feb 25, 2019</p>
</div>
<h3 id="New_in_LifeTime_Management_Console_11.0.307.0">New in LifeTime Management Console 11.0.307.0</h3>
<ul>
<li>Improved LifeTime cleanup process to also remove unused data from completed stagings. (RLIT-2287)</li>
<li>Added change log information to the output structure "ApplicationVersion" for methods "GET /applications/{ApplicationKey}/versions/" and "GET /applications/{ApplicationKey}/versions/{VersionKey}/" in LifeTime Deployment API v2. Added also the optional input "ChangeLogFilter" to method "GET /applications/{ApplicationKey}/versions/" to filter the returned list of versions by change logs containing the required keyword. (RLIT-2395)</li>
<li>It is now possible to delete application versions (LifeTime tags) using the new method "DELETE /applications/{ApplicationKey}/versions/{VersionKey}/" of LifeTime Deployment API v2. This feature will allow to delete in the environments the old module versions previously tagged by LifeTime. It requires Platform Server 10.0.912.0 (OutSystems 10 environments) or Platform Server 11 - Release Sep.2018 Cumulative Patch 1 (OutSystems 11 environments). Inspired by <a href="https://www.outsystems.com/ideas/3562/">Harlin Setiadarma's idea</a>. (RLIT-2399)</li>
<li>A new API method is now available in LifeTime Deployment API v2 for downloading the .oap file of a specific application version, "GET /applications/{ApplicationKey}/versions/{VersionKey}/content/". This method can be used to backup the code of an application version before deleting it. It requires Platform Server 10.0.1005.0 (OutSystems 10 environments) or Platform Server 11 - Release Jan.2019 Cumulative Patch 3 (OutSystems 11 environments) on the managed environments. (RLIT-2169)</li>
<li>Added new input "TargetEnvironmentKey" to the API method "GET /deployments/" of LifeTime Deployment API v1 and v2 that allows to filter the deployments list by target environment. Improved also the return codes to differ the case when the user does not have permissions to view the requested deployments from the case when there are no deployments that match the search. (RLIT-2368)</li>
<li>In LifeTime Deployment API v2, the attribute “ModuleVersionKeys” of structure "ApplicationVersionCreate" has been deprecated and is now optional. When creating a new application version using the method "POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/", passing a value in attribute “ModuleVersionKeys” will behave as previously, validating the module versions. (RLIT-2369)</li>
</ul>
<h3 id="Bug_Fixing_50">Bug Fixing</h3>
<ul>
<li>Fixed an issue in API method "POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/" of LifeTime Deployment API v2 that was preventing the creation of mobile apps versions. (RLIT-2410)</li>
<li>Fixed a security vulnerability. CVSS v3.0 score 7.1 (High) - Full details to be released in May 2019 (RLIT-2388)</li>
<li>Fixed an issue in LifeTime synchronization that could cause environment features to be unavailable. (RLIT-2381)</li>
</ul>

