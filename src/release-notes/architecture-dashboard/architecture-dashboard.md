---
locale: en-us
guid: fc98d44a-606c-4621-9485-117c73864484
app_type: traditional web apps, mobile apps, reactive web apps
---

<h1>Architecture Dashboard</h1>
<h2 id="Architecture_Dashboard_1.16">Architecture Dashboard 1.16</h2>
<div class="info">
<p>Released on May 5, 2022</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.16">New in Architecture Dashboard 1.16</h3>
<ul>
<li>Improved the Ignored Modules functionality under the Maintenance area when choosing modules to ignore or to analyze. (RADRT-1987)</li>
<li>You can now use the new Architecture Dashboard API to integrate Architecture Dashboard data with external tools. The API uses an API key to authenticate requests. You can generate and manage your API keys using Architecture Dashboard’s Maintenance menu. (RADRT-1849)</li>
<li>It is now possible to navigate to the findings report page of a specific application using a direct link, by passing its GUID parameter in the URL. You can get the GUID of an application using the Architecture Dashboard API. (RADRT-2035)</li>
</ul>
<h3 id="Bug_fixing">Bug fixing</h3>
<ul>
<li>Fixed an issue that was preventing user information from being synced when, due to some LifeTime operation, the LifeTime user's identifier changed. (RADRT-1980)</li>
<li>Fixed an issue that caused resolved findings to automatically reopen after 6 months when they were marked as "False positive" or "Won't fix". (RADRT-2040)</li>
</ul>

<h2 id="Architecture_Dashboard_1.15">Architecture Dashboard 1.15</h2>
<div class="info">
<p>Released on April 18, 2022</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.15">New in Architecture Dashboard 1.15</h3>
<ul>
<li>Now, on the Maintenance area, you can easily configure applications and modules to be ignored during technical debt analysis with the possibility of using bulk selection. (RADRT-1851)</li>
<li>Now, on the Maintenance area, you can easily filter and configure Forge components to be ignored during technical debt analysis. (RADRT-1853)</li>
<li>Now, the Infrastructure Overview dashboard data is in sync with the findings Report data. The sync of the Infrastructure Overview dashboard data no longer has one day of delay. (RADRT-1946)</li>
</ul>
<h3 id="Bug_fixing">Bug fixing</h3>
<ul>
<li>Fixed a performance issue when loading the findings Report screen. (RADRT-1873)</li>
<li>Fixed an issue on the Infrastructure Overview dashboard that caused the loading of the "Apps by highest technical debt" chart to fail. (RADRT-1906)</li>
</ul>
<h2 id="Architecture_Dashboard_1.14">Architecture Dashboard 1.14</h2>
<div class="info">
<p>Released on Feb 28, 2022</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.14">New in Architecture Dashboard 1.14</h3>
<ul>
<li>Revamped the findings report screen to present the information in a more organized and clear way. Among other improvements, it's now possible to filter the findings by team, clear the filter values, and see the percentage of technical debt on each code pattern. (RADRT-1840)</li>
</ul>
<h3 id="Bug_fixing">Bug fixing</h3>
<ul>
<li>Fixed an issue preventing the download of the probes when using the URL sent in the "Architecture Dashboard Probes Download" email. (RADRT-1888)</li>
</ul>
<h2 id="Architecture_Dashboard_1.13">Architecture Dashboard 1.13</h2>
<div class="info">
<p>Released on Feb 11, 2022</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.13">New in Architecture Dashboard 1.13</h3>
<ul>
<li>Now, all users with permission to access the findings report are able to export the report to Excel. (RADRT-1817)</li>
<li>Updated the documentation of the main features permissions to reflect the new access model to the export findings report operation (RADRT-1817) and improved the content readability. (RPM-1648)</li>
<li>Now, the LifeTime administrator account can't be associated with Architecture Dashboard as an IT user. (RADRT-1841)</li>
<li>Improved the data loading performance of the Infrastructure Overview dashboard. (RADRT-1828)</li>
</ul>
<h3 id="Bug_fixing">Bug fixing</h3>
<ul>
<li>The findings report is now correctly listing the code patterns when ordering by "Findings count". (RADRT-1758)</li>
<li>Fixed an issue in the App canvas preventing the color of the modules from being refreshed when selecting a different snapshot date. (RADRT-1624)</li>
<li>Fixed an issue that was reopening resolved findings set as "Resolve as won't fix" after 6 months. (RPM-1938)</li>
<li>Fixed an issue causing incorrect user information to be displayed when associating an IT user to the Architecture Dashboard over an existing association. (RADRT-1820)</li>
<li>Fixed a redirect loop preventing users from logging in the Architecture Dashboard after a session timeout. (RADRT-1872)</li>
</ul>
<h2 id="Architecture_Dashboard_1.12">Architecture Dashboard 1.12</h2>
<div class="info">
<p>Released on Dec 23, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.12">New in Architecture Dashboard 1.12</h3>
<ul>
<li>Released a new Infrastructure Overview dashboard. This new area gives an overall glimpse of the technical debt across your apps and enables the detailed analysis of the categories and code patterns that contribute most to that technical debt. (RPOR-5299)</li>
<li>Replaced the concept "Agility" by "Technical debt" on the Apps canvas. (RADRT-1766)</li>
</ul>
<h3 id="Bug_fixing">Bug fixing</h3>
<ul>
<li>Fixed an issue causing some IT users to be redirected to the old experience after being associated with the Architecture Dashboard. (RADRT-1650)</li>
<li>Exporting the findings report to Excel no longer causes an Invalid Parameters error when the selected language is not English. (RADRT-1718)</li>
<li>Fixed an issue that caused Duplicated Code findings set to a "Resolved" status to still show as "Opened".<br/>
This could lead to a "This fact has already been resolved by a different user" error message if you tried to set these findings to a "Resolved" status. (RPM-1884)</li>
</ul>
<h2 id="Architecture_Dashboard_1.11">Architecture Dashboard 1.11</h2>
<div class="info">
<p>Released on Sept 16, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.11">New in Architecture Dashboard 1.11</h3>
<ul>
<li>Released version 4.1 of the probes. This new version removes the runtime performance analysis from the probe installation steps and includes new warnings to help troubleshoot the most common installation issues. (RADRT-1539)</li>
</ul>
<h3 id="Bug_fixing">Bug fixing</h3>
<ul>
<li>Fixed an issue that stopped user permissions being received by Architecture Dashboard and prevented users accessing data in Architecture Dashboard. Instead, a "We're gathering your profile data" message was displayed to the user. This issue was specific to infrastructures with a different time zone to UTC." (RADRT-1391)</li>
<li>Fixed an issue that occurred when gathering module information from the probe and prevented some modules and applications being displayed on the canvas. (RADRT-1580)</li>
<li>Fixed an issue that caused apps to not show up on the Architecture Dashboard canvas. The issue occurred with infrastructures using a timezone different from UTC+0. (RPM-1732)</li>
<li>Fixed the counter in the Report screen for the "Duplicated Code" pattern when an application including that pattern has been deleted. (RPM-1465)</li>
</ul>
<h2 id="Architecture_Dashboard_1.10">Architecture Dashboard 1.10</h2>
<div class="info">
<p>Released on August 26, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.10">New in Architecture Dashboard 1.10</h3>
<ul>
<li>Improved the "Avoid Anonymous and/or Registered access Screens" pattern by reducing the number of false positives. The pattern now ignores anonymous screens created by default ("Login", "InternalError", "InvalidPermissions", and "NoPermissions").</li>
<li>Now, the "Missing description on public element" pattern ignores attributes of entities and structures that don't have descriptions.</li>
<li>Now, the "Unlimited Records in Aggregate" pattern ignores aggregates with a single source filtered by entity primary key without "Max. Records" defined.</li>
<li>Removed the "Not checking if the mobile device is compromised" pattern.</li>
<li>Removed the "Image widgets without width" pattern.</li>
<li>Removed the "Prefix Timer actions" pattern.</li>
<li>Improved the message that tells you when the last synchronization occurred and when the next one should occur. Now, you'll also see a warning if the last synchronization occurred more than 12 hours ago.</li>
</ul>
<h3 id="Bug_Fixing_0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a timeout while loading the list of Duplicated Code findings. (RADRT-1478)</li>
<li>Fixed an issue that prevented the toggling of the "AI auto-classification" feature. (RPM-1256)</li>
<li>Fixed an issue that prevented opening findings in the cross-platform Service Studio. (RADRT-1551)</li>
<li>Fixed an issue that occurred while using Discovery for the architecture analysis that prevented the creation of architecture findings.</li>
<li>Fixed an issue that occurred after enabling the "AI auto-classification", and that caused Discovery-specific architecture patterns (that included architecture sublayers) to still show. (RADRT-1212)</li>
</ul>
<h2 id="Architecture_Dashboard_1.8">Architecture Dashboard 1.8</h2>
<div class="info">
<p>Released on July 9, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.8">New in Architecture Dashboard 1.8</h3>
<ul>
<li>Added a new security code pattern showing you when an automatically generated REST endpoint for a Server Action is exposed in a screen using the Anonymous Role. (RADRT-1315)</li>
<li>Now, the heatmap shows the technical debt based on the size of each module or app. This change helps you have a clearer and more accurate picture of the overall state of your factory. (RADRT-859)</li>
<li>Improved the synchronization of data between the Architecture Dashboard LifeTime plugin and the Architecture Dashboard SaaS. (RADRT-1401)</li>
<li>Now, the report screen shows the information about the last synchronization at the top of the page, right after the title. (RADRT-1401)</li>
<li>Now, in the reports screen, the "how to fix" section of patterns include information about setting the state of findings. (RADRT-1461)</li>
</ul>
<h3 id="Bug_Fixing_1">Bug Fixing</h3>
<ul>
<li>Fixed an issue that occurred after changing the layer of a module and that caused incorrect findings to be shown. (RADRT-1449)</li>
<li>Fixed an issue that occurred after synchronizing with environments with a timezone other than UTC that caused issue with permissions. (RADRT-1391)</li>
<li>Fixed an issue that occurred while trying to process modules with recent OutSystems features, such as client side "setlocale". (RADRT-1421)</li>
<li>Fixed an issue that caused an Invalid Activation Code message to be shown after a successful infrastructure registration process. (RADRT-1426)</li>
</ul>
<h2 id="Architecture_Dashboard_1.7">Architecture Dashboard 1.7</h2>
<div class="info">
<p>Released on May 14, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.7">New in Architecture Dashboard 1.7</h3>
<ul>
<li>Now, you can use the duplicated code pattern to help you refactor your code. Using artificial intelligence, Architecture Dashboard finds logic patterns that are repeated in different action flows across your environment. Use this information to guide your refactoring and reduce maintenance costs. You can change the state of duplicated code findings the same way you do for other findings. (RADRT-1107)</li>
<li>Improved the synchronization of data between the Architecture Dashboard LifeTime plugin and the Architecture Dashboard SaaS. From now on, a synchronization will take less time to complete. (RADRT-1250)</li>
<li>Improved the readability of long names of apps and modules in the canvas. (RADRT-1303)</li>
<li>Improved the UX of the canvas while interacting with the team dropdown. Now clicking outside the dropdown closes it. (RADRT-1304)</li>
</ul>
<h3 id="Bug_Fixing_2">Bug Fixing</h3>
<ul>
<li>Fixed an issue that occurred while registering a new infrastructure and that caused errors when the plugin tried to connect to the Architecture Dashboard SaaS. (RADRT-1254)</li>
<li>Fixed an issue that sometimes prevented the change of a module's architectural layer. (RADRT-1291)</li>
<li>Fixed an issue that occurred after changing the language to Japanese and that caused some code patterns content to be shown in English. (RADRT-1293)</li>
<li>Fixed an issue that occurred after a session timed out while on the report screen and that caused the report list to be empty after logging in. (RADRT-1294)</li>
<li>Fixed an issue while registering a new infrastructure that occurred if an environment address without the scheme ("http" or "https") was used and that caused the link provided in the instructions to be incorrect. (RADRT-1295)</li>
</ul>
<h2 id="Architecture_Dashboard_1.6">Architecture Dashboard 1.6</h2>
<div class="info">
<p>Released on Apr 9, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.6">New in Architecture Dashboard 1.6</h3>
<ul>
<li>Now you can filter the findings report by time interval to track your recent findings. Filter findings created in the past week, past fortnights, or past quarter. (RADRT-1246)</li>
<li>Now your filter selections on the findings report screen are saved between sessions. (RADRT-1211)</li>
<li>Now, findings marked as false positive aren't automatically reopened after a period of time. (RADRT-1210)</li>
</ul>
<h3 id="Bug_Fixing_3">Bug Fixing</h3>
<ul>
<li>Fixed an issue that triggered multiple server requests after every single scroll done on the findings list (RADRT-1253)</li>
<li>Fixed an issue on the "Export to Excel" functionality, where in some cases the exported file returned an empty list (RADRT-1263)</li>
<li>Fixed an issue that occurred after solving all the findings of a code pattern that caused the code pattern to still show with an empty findings list. (RADRT-1268)</li>
<li>Fixed an issue that occurred after an older snapshot that made the canvas unresponsive. (RADRT-1244)</li>
<li>Fixed an issue that sometimes occurred while navigating between the findings report and the canvas that showed a "We are gathering your infrastructure data" blank slate. (RADRT-1249)</li>
<li>Fixed an issue that occurred after changing a module layer classification that caused the old layer classification to be shown in the architecture pattern details view. (RADRT-1270)</li>
</ul>
<h2 id="Architecture_Dashboard_1.5">Architecture Dashboard 1.5</h2>
<div class="info">
<p>Released on Mar 5, 2021</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.5">New in Architecture Dashboard 1.5</h3>
<ul>
<li>Now you can check the list of dependencies for architecture findings in Architecture Dashboard. (RADRT-1174)</li>
<li>Improved the experience of the login screen, making it consistent with other OutSystems tools. (RADRT-926)</li>
<li>Improved the validation messages shown during the registration of a new infrastructure in Architecture Dashboard. (RADRT-1051)</li>
<li>Updated AI Auto Classification model with improved accuracy. (RCDNAT-37)</li>
<li>Now a warning message is shown in the login screen during maintenance periods. (RADRT-1175)<br/>
Performance improvements accessing the report pattern findings (RADRT-1177)<br/>
Removed Application Objects from the Architecture Dashboard probe modules (RADRT-1102)</li>
</ul>
<h3 id="Bug_Fixing_4">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the "Core module is providing services to sublayers" pattern to be incorrectly identified when using the AI Auto Classification model. (RADRT-1066)</li>
<li>Fixed an issue that occurred when filtering the report by "Me" option that caused no findings to be shown. (RADRT-1019)</li>
<li>Fixed an issue that caused some sessions to time out after five minutes. (RADRT-1176)</li>
<li>Fixed an issue that caused ignored modules to still be considered for the architecture findings analysis. (RADRT-1185)</li>
<li>Fixed an issue that occurred while using probe version 4 that caused some users with the correct permissions to always see a blank canvas with a "gathering information" message.</li>
<li>Fixed several bugs related to user permissions.</li>
</ul>
<h2 id="Architecture_Dashboard_1.4">Architecture Dashboard 1.4</h2>
<div class="info">
<p>Released on Dec 22, 2020</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.4">New in Architecture Dashboard 1.4</h3>
<ul>
<li>Released version 4.0 of the probes. This new version adds the ability to collect the LifeTime permissions for known users, and allows the configuration of a proxy while connecting to the Architecture Dashboard SaaS. (RADRT-871)</li>
<li>Now the permissions that IT users have while using Architecture Dashboard are mapped from the permissions set in LifeTime for the code analysis environment. This feature is available on probe version 4.0. (RADRT-840)</li>
<li>Added a new REST endpoint (<code>https://architecture.outsystems.com/Broker_API/rest/ArchitectureDashboard</code>) to the Architecture Dashboard SaaS with security improvements. To connect to the new REST endpoint you must use probe version 4.0. (RADRT-865)</li>
<li>Improved the export to Excel of the findings report thanks to your feedback. (RADRT-947)</li>
<li>Improved the message shown when a new probe version is available. (RADRT-984)</li>
<li>Improved the visual theme of the Architecture Dashboard. (RADRT-808)</li>
<li>You can now use the OutSystems hub to navigate to other OutSystems tools. (RADRT-872)</li>
</ul>
<h3 id="Bug_Fixing_5">Bug Fixing</h3>
<ul>
<li>Fixed an issue that occurred while associating an IT User with Architecture Dashboard that caused you to be redirected to the wrong Architecture Dashboard screen after forcing you to log in twice. (RADRT-906)</li>
<li>Fixed and issue that caused warnings to appear in the wrong location in the canvas screen. (RADRT-963)</li>
<li>Fixed an issue that caused false positive findings for the "Large Image/Large Resource" pattern. (RADRT-925)</li>
</ul>
<h2 id="Architecture_Dashboard_1.3">Architecture Dashboard 1.3</h2>
<div class="info">
<p>Released on Oct 22, 2020</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.3">New in Architecture Dashboard 1.3</h3>
<ul>
<li>Improved the visual theme of the Architecture Dashboard. (RADRT-808)</li>
</ul>
<h3 id="Bug_Fixing_6">Bug Fixing</h3>
<ul>
<li>Fixed the behavior of considering ignored modules while repositioning the Application Layer using Architecture Discovery. (RADRT-813)</li>
<li>Fixed the behavior of opening the wrong object in some patterns. (RADRT-814)</li>
</ul>
<h2 id="Architecture_Dashboard_1.2">Architecture Dashboard 1.2</h2>
<div class="info">
<p>Released on Sep 14, 2020</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.2">New in Architecture Dashboard 1.2</h3>
<ul>
<li>You can now select several apps and modules in the report screen's filter.(RADRT-695)</li>
<li>You can now open the report screen without selecting an app in the canvas. (RADRT-696)</li>
<li>The default user finding's filter has been improved and its status is now kept during a session. (RADRT-729)</li>
<li>Guided refactoring: added a new code pattern that lists duplicated code in the code analysis environment. (RADRT-706)</li>
<li>Improved the synchronization queue mechanism by making it react quicker to incoming requests. (RADRT-744)</li>
<li>The new version of the probes can now collect information that enables the detection of duplicated code in the code analysis environment. (RADRT-702)</li>
</ul>
<h3 id="Bug_Fixing_7">Bug Fixing</h3>
<ul>
<li>Improved the Architecture Discovery feature by making it properly wait for the AI model response. (RADRT-735)</li>
<li>Fixed an issue that redirected a user to the new experience automatically upon session timeout. (RADRT-726)</li>
<li>Fixed a bug that caused app classification not to change after modifying the classification of one of its module. (RADRT-776)</li>
</ul>
<h2 id="Architecture_Dashboard_1.1">Architecture Dashboard 1.1</h2>
<div class="info">
<p>Released on Aug 13, 2020</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.1">New in Architecture Dashboard 1.1</h3>
<ul>
<li>Now, Architecture Dashboard defines the architecture layer classification of a module using AI. You can override the layer classification of a module that was auto-classified using AI. This feature is available on probe version 3.0. (RADRT-615)</li>
<li>Now, Discovery doesn't need to be installed during setup, but you can still use Discovery to do the architecture analysis. This feature is available on probe version 3.0. (RADRT-612)</li>
<li>Added tooltips to the Technical Debt Trends chart. (RADRT-602)</li>
<li>Performance improvements on Architecture Dashboard canvas.(RADRT-600)</li>
</ul>
<h3 id="Bug_Fixing_8">Bug Fixing</h3>
<ul>
<li>Fixed an issue while downloading the probes on Safari browser. (RADRT-605)</li>
<li>Fixed an issue with the zoom to fit on Architecture Dashboard canvas when selecting a team. (RADRT-603)</li>
<li>Fixed issue that sometimes prevented the user from downloading the probes that were sent by email. (RADRT-590)</li>
<li>Fixed the presentation of the "Latest sync date" on canvas that wasn't always being shown in UTC. (RADRT-571)</li>
<li>Fixed issue with the old experience that caused some duplicate findings. (RADRT-638)</li>
</ul>
<h2 id="Architecture_Dashboard_1.0">Architecture Dashboard 1.0</h2>
<div class="info">
<p>Released on May 28, 2020</p>
</div>
<h3 id="New_in_Architecture_Dashboard_1.0">New in Architecture Dashboard 1.0</h3>
<ul>
<li>
<p>View technical debt in the apps of an infrastructure to find the apps that cause most technical debt.</p>
</li>
<li>
<p>View trends and snapshots of technical debt in your infrastructure and apps to know how technical debt has changed with time.</p>
</li>
<li>View dependencies between apps in your infrastructure.</li>
<li>View technical debt in the modules of an app to find the modules that cause most technical debt.</li>
<li>Check which team owns an app and filter app visibility by team.</li>
<li>Find code patterns that cause technical debt in all the modules of an app or in a single module.</li>
<li>Understand why each code pattern impacts technical debt.</li>
<li>Know where and how to fix each code pattern finding.</li>
</ul>

