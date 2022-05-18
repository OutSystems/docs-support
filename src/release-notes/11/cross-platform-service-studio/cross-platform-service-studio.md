---
locale: en-us
guid: 7ddf30aa-3be8-48c3-80fb-d2efdf1222cd
app_type: traditional web apps, mobile apps, reactive web apps
---

<h1>Cross-platform Service Studio</h1>
<h2 id="Cross-platform_Service_Studio_11.52.6">Cross-platform Service Studio 11.52.6</h2>
<div class="info"><p>Released on May 16, 2022</p></div>
<h3 id="Bug_Fixing_0">Bug Fixing</h3>
<ul>
<li>Fixed a crash when loading screen templates. (RMAC-9576)</li>
<li>Fixed a crash when dragging a client action to a screen. (RMAC-9588)</li>
<li>Fix an issue when navigating back/forward in the history that caused a crash in some situations (RMAC-9590)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.52.5">Cross-platform Service Studio 11.52.5</h2>
<div class="info"><p>Released on May 12, 2022</p></div>
<h3 id="Bug_Fixing_1">Bug Fixing</h3>
<ul>
<li>Fixed a crash when loading screen templates. (RMAC-9576)</li>
<li>Crash happens after deleting multiple Client Actions when expanding/collapsing Client Actions. Can't always be reproduced. (RMAC-9579)</li>
<li>Avoid crash opening Screen Template Dialog for first time without connection to an environment (RMAC-9580)</li>
<li>Fixed an issue when having multiple instances of Service Studio connected to different environments that caused some operations to execute on the incorrect environment. (RMAC-9657)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.52.4">Cross-platform Service Studio 11.52.4</h2>
<div class="info"><p>Released on Apr 29, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.52.4">New in Cross-platform Service Studio 11.52.4</h3>
<ul>
<li>Refresh ServiceStudio UI while a progress dialog is loading (RDOIAT-545)</li>
</ul>
<h3 id="Bug_Fixing_2">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was forcing Service Studio to not respect IPP UnProtected environment setting (RMAC-9422)</li>
<li>Fixed Service Studio crash when applying changes to the References of a module (RMAC-9439)</li>
<li>Fix an issue that could occur when closing a module tab while the flow suggestions popup was about to be shown. (RMAC-9528)</li>
<li>Use Expression Editor for complex expressions referring Static Entities instead of the Record Picker (RMAC-9532)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.52.3">Cross-platform Service Studio 11.52.3</h2>
<div class="info"><p>Released on Apr 21, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.52.3">New in Cross-platform Service Studio 11.52.3</h3>
<ul>
<li>It is now possible to open Aggregates and Edit Data in a separate window. This way, you can compare Aggregates and Entities while seeing your screens or logic flows. (RTAFA-449)</li>
</ul>
<h3 id="Bug_Fixing_3">Bug Fixing</h3>
<ul>
<li>Improved Aggregate's data preview experience (RAID-1394)</li>
<li>Fix a crash when trying to open multiple AddRemoveReferences dialogs at once (RMAC-9022)</li>
<li>Fixed an error that occurred when spanning out a new Service Studio instance by dragging a module tab of a disconnected environment. (RMAC-9371)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.52.2">Cross-platform Service Studio 11.52.2</h2>
<div class="info"><p>Released on Apr 06, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.52.2">New in Cross-platform Service Studio 11.52.2</h3>
<ul>
<li>You can now use SOAP Refresh option to quickly change the services consumed from a SOAP Web Service or modify the list of consumed methods. (RDOIBT-80)</li>
</ul>
<h3 id="Bug_Fixing_4">Bug Fixing</h3>
<ul>
<li>Fix an issue that caused the Widget tree to immediately appear (in Windows OS only) when starting to drag elements from other right pane trees. (RMAC-8520)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.52.1">Cross-platform Service Studio 11.52.1</h2>
<div class="info"><p>Released on Mar 22, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.52.1">New in Cross-platform Service Studio 11.52.1</h3>
<ul>
<li>Service Studio is not be able to connect to Project Neo anymore. Service Studio Project Neo should be used instead. (RDEV-3959)</li>
<li>Improved the experience of using copy, paste, cut, and delete keyboard shortcuts when editing text in Service Studio. For more information about keyboard shortcuts, go to Help -&gt; Keyboard Shortcuts in Service Studio. (RDOIBT-206)</li>
<li>You can now use SOAP Refresh option to quickly change the services consumed from a SOAP Web Service or modify the list of consumed methods. (RDOIBT-80)</li>
<li>Now on text widgets the UnDo and ReDo operations are done with text aggregation for more efficient execution. (RTAFB-5584)</li>
</ul>
<h3 id="Bug_Fixing_5">Bug Fixing</h3>
<ul>
<li>Improved an error message by adding relevant information when an array lacks the items definition while importing a REST Web Service. (R11DT-382)</li>
<li>Fixed an issue that caused the installation of a sample app to fail. (RIMPT-1653)</li>
<li>Fix issue that prevents the iterator from being updated after typing inside a TextWidget (RMAC-8345)</li>
<li>Solves a problem in a semaphore where some promises could hang forever. (RMAC-9258)</li>
<li>Solves problem when the user starts typing in a container and the SS freezes (RMAC-9259)</li>
<li>RichWidget Icon preview shows the icon selected. (RPM-2106)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.52.0">Cross-platform Service Studio 11.52.0</h2>
<div class="info"><p>Released on Mar 18, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.52.0">New in Cross-platform Service Studio 11.52.0</h3>
<ul>
<li>It is now possible to export the definition files from a consumed SOAP Web Service. (R11DT-911)</li>
<li>Service Studio is not be able to connect to Project Neo anymore. Service Studio Project Neo should be used instead. (RDEV-3959)</li>
<li>Enabled zoom capabilities in logic flows and entities diagram. (RDOIAT-324)</li>
<li>Improved overall memory consumption. (RDOIAT-474)</li>
<li>Improved the experience of using copy, paste, cut, and delete keyboard shortcuts when editing text in Service Studio. For more information about keyboard shortcuts, go to Help -&gt; Keyboard Shortcuts in Service Studio. (RDOIBT-206)</li>
<li>Now on text widgets the UnDo and ReDo operations are done with text aggregation for more efficient execution. (RTAFB-5584)</li>
</ul>
<h3 id="Bug_Fixing_6">Bug Fixing</h3>
<ul>
<li>Fixed an issue that gave an incorrect length attribute when importing a SOAP web service. (RPD-5047)</li>
<li>Fix missing horizontal scroll bar on traditional web apps when no device is selected. (RPM-2045)</li>
<li>Fixed an issue that prevented debugging from starting when connected with older Platform Server versions. (RPM-2198)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.51.9">Cross-platform Service Studio 11.51.9</h2>
<div class="info"><p>Released on Mar 03, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.9">New in Cross-platform Service Studio 11.51.9</h3>
<ul>
<li>Users are now able to identify merge differences on screens &amp; blocks through widgets visual hints/decorations. (RDOIAT-301)</li>
</ul>
<h3 id="Bug_Fixing_7">Bug Fixing</h3>
<ul>
<li>Fixed an issue that gave an incorrect length attribute when importing a SOAP web service. (RPD-5047)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.51.8">Cross-platform Service Studio 11.51.8</h2>
<div class="info"><p>Released on Feb 23, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.8">New in Cross-platform Service Studio 11.51.8</h3>
<ul>
<li>Now Table widgets can be collapsed using the display toggle button. (RTAFA-278)</li>
</ul>
<h3 id="Bug_Fixing_8">Bug Fixing</h3>
<ul>
<li>Fix intermittent crash when opening Service Studio. (RMAC-9105)</li>
<li>Fixed expression editor visual glitch when synchronizing with scope tree. (RMAC-9153)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.51.7">Cross-platform Service Studio 11.51.7</h2>
<div class="info"><p>Released on Feb 15, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.7">New in Cross-platform Service Studio 11.51.7</h3>
<ul>
<li>It's now possible to use text shortcuts in Flow editor (Cut, Copy, Paste, Delete). (RDOIBT-213)</li>
<li>It's now possible to use text shortcuts in right pane tree (Cut, Copy, Paste, Delete). (RDOIBT-220)</li>
<li>Improved the design-time appearance of the List and Table widgets. The second and third iterator element now have reduced opacity to show you can't edit them. (RTAFA-276)</li>
<li>Now List widgets can be collapsed using display toggle button. (RTAFA-279)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.51.6">Cross-platform Service Studio 11.51.6</h2>
<div class="info"><p>Released on Feb 09, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.6">New in Cross-platform Service Studio 11.51.6</h3>
<ul>
<li>Now ListItem widgets can be collapsed using display toggle button. (RTAFA-272)</li>
<li>Now If Widgets have a unique icon per toggle value to better distinguish which branch is visible  (RTAFA-275)</li>
</ul>
<h3 id="Bug_Fixing_9">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused manage dependencies stays loading indefinitely when Apply all option is chosen. (RDMST-894)</li>
<li>. (RICT-4268)</li>
<li>Fix issue that prevents the iterator from being updated after typing inside a TextWidget (RMAC-8345)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.51.5">Cross-platform Service Studio 11.51.5</h2>
<div class="info"><p>Released on Feb 01, 2022</p></div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.5">New in Cross-platform Service Studio 11.51.5</h3>
<ul>
<li>It is now possible to expose REST web services with the character "-" on the URL.
Inspired by <a href="https://www.outsystems.com/ideas/5205/allow-hyphen-in-url-path-of-an-exposed-api-web-method/">João Marques' idea</a>. (R11DT-870)</li>
</ul>
<h3 id="Bug_Fixing_10">Bug Fixing</h3>
<ul>
<li>Removed double error message when trying to set public blocks or screens to be reused in other modules, for Mobile Apps. (RMAC-9002)</li>
</ul>

<h2 id="Cross-platform_Service_Studio_11.51.4">Cross-platform Service Studio 11.51.4</h2>
<div class="info">
<p>Released on Jan 21, 2022</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.4">New in Cross-platform Service Studio 11.51.4</h3>
<ul>
<li>It is now possible to search for toolbox nodes using the Intelligent Quick Search feature (in Logic Assistant). (RAID-931)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.51.3">Cross-platform Service Studio 11.51.3</h2>
<div class="info">
<p>Released on Jan 10, 2022</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.3">New in Cross-platform Service Studio 11.51.3</h3>
<ul>
<li>It is now possible to consume SOAP Web Services in your applications. (RDOIBT-194)</li>
</ul>
<h3 id="Bug_Fixing_11">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to become unresponsive after closing Search In Other Modules window. (RMAC-8718)</li>
<li>Fixed an issue that caused Service Studio to consider all possible dependencies invalid and the need of being republished when using manage dependencies. (RMAC-8722)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.51.2">Cross-platform Service Studio 11.51.2</h2>
<div class="info">
<p>Released on Dec 28, 2021</p>
</div>
<h3 id="Bug_Fixing_12">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to become unresponsive after closing Search In Other Modules window. (RMAC-8718)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.51.1">Cross-platform Service Studio 11.51.1</h2>
<div class="info">
<p>Released on Dec 21, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.1">New in Cross-platform Service Studio 11.51.1</h3>
<ul>
<li>Now it's possible to configure a new Database integration through the following shortcut: go to Data tab &gt; right-click on Databases &gt; select Integrate with External Databases (RDEPT-112)</li>
<li>You can now evolve your traditional web applications using the added capabilities to customize widgets on web screens. (RTAFB-5483)</li>
</ul>
<h3 id="Bug_Fixing_13">Bug Fixing</h3>
<ul>
<li>Fixed the lack of feedback on whether a widget can be dropped or not while dragging in Service Studio Hybrid. (RDOICT-81)</li>
<li>Fix issue of window size being smaller than desired resulting in cropped content. (RMAC-8669)</li>
<li>Fixed not being able to restore the Service Studio window in Windows after it was minimized to the Taskbar (RMAC-8719)</li>
<li>Fixed an issue that caused Service Studio to consider all possible dependencies invalid and the need of being republished when using manage dependencies. (RMAC-8722)</li>
<li>Fixed a crash in Service Studio while performing a merge that envolves screen variables used in screen actions (RMAC-8735)</li>
</ul>
<ul>
<li>Fixed a security vulnerability in diff command. CVSSv3.0 score 5.8 (Medium) (RPM-686)</li>
</ul>
<h3 id="Known_Issues_0">Known Issues</h3>
<ul>
<li>In macOS Catalina, Service Studio shows a red shadow when opening dialogs. The shadow disappears after some milliseconds and doesn't affect Service Studio functionality.</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.51.0">Cross-platform Service Studio 11.51.0</h2>
<div class="info">
<p>Released on Dec 14, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.51.0">New in Cross-platform Service Studio 11.51.0</h3>
<ul>
<li>Infrastructure for SAUCE tutorials - enhancing existing Guided Tour infrastructure to support specifying substeps in code, no impact should happen in existing tutorials. (RIMPT-1000)</li>
<li>Features related to emails for Mobile and Reactive Web Apps are now generally available in Service Studio. You could use the features previously in technical the previews "Emails for Mobile and Reactive" and "Attachments in Mobile and Reactive emails". (RTAFA-77)</li>
</ul>
<h3 id="Bug_Fixing_14">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a communication error when publishing a cloned app. (RDEV-3878)</li>
<li>Fixed the lack of feedback on whether a widget can be dropped or not while dragging in Service Studio Hybrid. (RDOICT-81)</li>
<li>Fixed an issue that caused Service Studio to replace the current environment connection with a different environment when the connection to that different environment is finalized in another Service Studio instance. Fixed a crash when performing server operations while not connected to an environment. (RMAC-8544)</li>
<li>Fixed an issue where the True Change panel would appear empty after opening an older version of a module. (RMAC-8617)</li>
<li>Fixed an issue that caused the wrong feedback message to be displayed when removing unused references. (RMAC-8715)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.19">Cross-platform Service Studio 11.50.19</h2>
<div class="info">
<p>Released on Dec 03, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.19">New in Cross-platform Service Studio 11.50.19</h3>
<ul>
<li>Installing a template (sample app) just got simpler. No dependency dialog is shown during installation. (RDEPT-3)</li>
<li>Ability to refresh existing REST Integrations, enabling additional productivity to users. (RDOIBT-83)</li>
<li>The validation rule for a mobile App Identifier in Service Center is now aligned with iOS and Android app stores. The validation messages were also updated accordingly. (RMAC-7346)</li>
<li>You can now use the grid columns to accurately resize the elements of a screen in a fixed or fluid layout. Instead of previously resizing without seeing parent's available space nor knowing the grid layout width, you now have a better idea of the available space in elements because the IDE UI shows the column number. This change makes the process of the UI design more efficient. (RTAFA-146)</li>
<li>Now you can configure friendly URLs in your Reactive Web Apps. Go to Service Center &gt; Administration &gt; SEO URLs to set up the site rules and redirects. Configure the page rules in Service Studio, by setting Custom URLs to Yes in the Screen properties. (RTAFB-4453)</li>
</ul>
<h3 id="Bug_Fixing_15">Bug Fixing</h3>
<ul>
<li>Fixed an issue when using the Delete shortcut on an "Unused Element" warning, which was deleting the selected element in the right pane tree instead of the "Unused Element". (RMAC-8054)</li>
<li>Fix crash when creating a new Screen through a destination node in a Screen Action. (RMAC-8282)</li>
<li>Fixed crash when opening "Manage Environments" from Login. (RMAC-8519)</li>
<li>Fixed a crash when closing Service Studio while accessing closed dialogs. (RMAC-8545)</li>
</ul>
<ul>
<li>Fixed a remote code execution vulnerability exploitable via phishing. CVSSv3.1 score 7.5 (High). (RPM-1054)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.18">Cross-platform Service Studio 11.50.18</h2>
<div class="info">
<p>Released on Nov 23, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.18">New in Cross-platform Service Studio 11.50.18</h3>
<ul>
<li>Ability to refresh existing REST Integrations, enabling additional productivity to users. (RDOIBT-83)</li>
<li>Now it’s easier to find OutSystems UI components in Service Studio toolbox. (RIMPT-970)</li>
</ul>
<h3 id="Bug_Fixing_16">Bug Fixing</h3>
<ul>
<li>Service Studio no longer crashes when, after changing a 'Run Client Actions's action, the 'Expand Element' of a list argument is clicked. (RDMST-812)</li>
<li>Fixed the lack of feedback on whether a widget can be dropped or not while dragging in Service Studio. (RDOICT-81)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.17">Cross-platform Service Studio 11.50.17</h2>
<div class="info">
<p>Released on Nov 08, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.17">New in Cross-platform Service Studio 11.50.17</h3>
<ul>
<li>Added support for WebWidget.HeaderCell in Service Studio X-Platform. (RTAFB-5331)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.16">Cross-platform Service Studio 11.50.16</h2>
<div class="info">
<p>Released on Oct 28, 2021</p>
</div>
<p>This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes.</p>
<h2 id="Cross-platform_Service_Studio_11.50.15">Cross-platform Service Studio 11.50.15</h2>
<div class="info">
<p>Released on Oct 26, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.15">New in Cross-platform Service Studio 11.50.15</h3>
<ul>
<li>It's now easier to select data for Table and List widgets. Click "Select Data" in the Source property dropdown to fetch and bind data from an entity in a single operation. (RIMPT-846)</li>
</ul>
<h3 id="Bug_Fixing_17">Bug Fixing</h3>
<ul>
<li>Fixed an issue caused by the rendering of an HTML Element widget with invalid Tag property value. (RMAC-8197)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.14">Cross-platform Service Studio 11.50.14</h2>
<div class="info">
<p>Released on Oct 06, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.14">New in Cross-platform Service Studio 11.50.14</h3>
<ul>
<li>It's now easier to use data from your System of Records in your apps. In the "Logic" tab, open the context menu for "Integration with external systems" and select "New integration". (RIMPT-742)</li>
<li>Improved the integration of REST APIs allowing users to select methods to be imported. (RMAC-6641)</li>
</ul>
<h3 id="Bug_Fixing_18">Bug Fixing</h3>
<ul>
<li>Fixed a crash when trying to refresh dependencies on Manage Dependencies dialog under some circumstances (RDMST-760)</li>
<li>Fixed an issue that causes the Manage Dependencies window to open twice when using shortcuts. (RICT-3568)</li>
<li>Fixed a bug on Entity properties' dropdown that prevented the user from typing or deleting text. (RMAC-7728)</li>
<li>Fixed a crash on aggregate when an entity attribute used in a group by year column is deleted. (RMAC-8113)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.13">Cross-platform Service Studio 11.50.13</h2>
<div class="info">
<p>Released on Sep 21, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.13">New in Cross-platform Service Studio 11.50.13</h3>
<ul>
<li>Soap Introspection testing is setup and will be triggered when prc-soap-introspection label is present on pull request. (R11DT-513)</li>
<li>You can now use expressions to set titles of Screens. This lets you change the page title dynamically, and set unique values that show in the browser tabs, bookmarks, and results from the search engines. When using this feature, it is recomended that all developers in the same organization update Service Studio. (RTAF-5082)</li>
</ul>
<h3 id="Bug_Fixing_19">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the "Limit Exceeded" error to have an empty message. (RDEV-3585)</li>
<li>Added support for opening the context menu with Ctrl+Left Click on Mac. (RMAC-6068)</li>
<li>Right pane tree tabs tooltips now display the correct shortcut on macOS. (RMAC-7632)</li>
<li>Added support for dragging text from other windows to the language editors. (RMAC-7727)</li>
<li>Fixed an issue that, under certain conditions, kept the last SOAP expose item visible in the tree after being deleted, causing a crash if another deletion try occurred. (RMAC-7876)</li>
<li>Editing complex screens is now faster. (RMAC-8024)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.12">Cross-platform Service Studio 11.50.12</h2>
<div class="info">
<p>Released on Sep 15, 2021</p>
</div>
<h3 id="Bug_Fixing_20">Bug Fixing</h3>
<ul>
<li>Now the Edit shortcuts are always applied to currently focused window in ServiceStudio on Mac (RICT-3706)</li>
<li>Fixed an issue that was preventing from seeing if an element was created or deleted in a merge scenario. (RMAC-7624)</li>
<li>Right pane tree tabs tooltips now display the correct shortcut on macOS. (RMAC-7632)</li>
<li>Fixed the "Open in Browser" command so it opens page with a custom URL when the technical preview "SEO-friendly URLs for Reactive Web Apps" is on. (RTAF-5032)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.11">Cross-platform Service Studio 11.50.11</h2>
<div class="info">
<p>Released on Aug 16, 2021</p>
</div>
<h3 id="New_in_Cross-platform_Service_Studio_11.50.11">New in Cross-platform Service Studio 11.50.11</h3>
<ul>
<li>Improved tooltip text on Publish button when with errors. (RDEV-3449)</li>
<li>Now users have a link and dedicated FAQ session in case they have difficulties in the Sign in with email. (RDRGT-92)</li>
<li>Support for new features in the email technical preview for Mobile and Reactive Web Apps, including attachments and new widgets. (RTAF-4812)</li>
</ul>
<h3 id="Bug_Fixing_21">Bug Fixing</h3>
<ul>
<li>Fixed template cache concurrent access issue. (RIMPT-539)</li>
<li>Improved the experience of reading and selecting text in the properties with syntax highlighting. (RMAC-4587)</li>
<li>Fixed an issue that prevented the drag of the tutorial dialog in Windows. (RMAC-7406)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.10">Cross-platform Service Studio 11.50.10</h2>
<div class="info">
<p>Released on Aug 09, 2021</p>
</div>
<h3 id="Bug_Fixing_22">Bug Fixing</h3>
<ul>
<li>Fixed a bug causing the window to become maximized upon startup. Window state is now properly restored. (RICT-3776)</li>
<li>Fixed a bug that allowed zooming in Service Studio using the trackpad pinch zoom. (RMAC-7183)</li>
<li>Fix module freeze when trying to navigate from a warning message. (RMAC-7390)</li>
<li>Avoid crash when DoubleClick aggregate filter. (RMAC-7408)</li>
</ul>
<h2 id="Cross-platform_Service_Studio_11.50.9">Cross-platform Service Studio 11.50.9</h2>
<div class="info">
<p>Released on Jul 29, 2021</p>
</div>
<h3 id="New_in_Service_Studio_11.50.9">New in Service Studio 11.50.9</h3>
<ul>
<li>Use the new text editor when you need to CSS or JS snippets that includes the following improvements:
<ul>
<li>Autocomplete</li>
<li>Syntax highlighting</li>
<li>Find and replace</li>
<li>Line numbering</li>
<li>Compatibility with JavaScript ES6</li>
</ul>
</li>
<li>You can now choose between a dark and light theme.</li>
</ul>
<h3 id="Known_issues">Known issues</h3>
<ul>
<li>Certain UI editor interactions may cause a crash and freeze that module. Please include as much information as possible whenever you submit feedback.</li>
<li>The Styles Sheet Editor button on the toolbar isn't present when selecting a widget.</li>
<li>Mobile app generation not working for Platform Server versions below 11.8.0.</li>
<li>Tooltips flicker in certain situations, you may encounter issues in styling, rendering or stealing focus.</li>
</ul>
<h3 id="Features_currently_unavailable">Features currently unavailable</h3>
<p>There are some feature differences between this new version and your existing Service Studio.</p>
<ul>
<li>Developing Traditional Web apps isn't possible yet.</li>
<li>The rendering of outlines that show up when you are dropping widgets into tight places isn't available yet. Hint: if you encounter issues, use the Widget Tree.</li>
<li>In the UI main editor, the toggles for some widgets (for example, List or Table widgets) don't have the final experience.</li>
<li>Context menus icons, display and styling are still under development.</li>
<li>The following features of the flow editor for actions, processes, and UI flows aren't available yet:
<ul>
<li>Zoom.</li>
<li>Export to an Image.</li>
</ul>
</li>
<li>Configuring apps with multi-language isn't possible yet.</li>
<li>Integrations: Consuming SOAP web services and SAP Remote Functions isn't supported.</li>
<li>Interactive tutorials aren't available yet.</li>
</ul>

