---
locale: en-us
guid: 7269c108-4294-41a9-ae2a-93464a7c8da5
app_type: traditional web apps, mobile apps, reactive web apps
---

<div class="hidden"><h1>Development Environment</h1></div>

<div class="info">

Release notes for newer Service Studio release are now under [Cross-Plarform Service Studio](../cross-platform-service-studio/cross-platform-service-studio.md).

</div>

<div class="hidden" id="development-environment-11.14.16_start"></div>
<h2 id="development_environment_11.14.16">Development Environment 11.14.16</h2>
<div class="info"><p>Released on May 16, 2022</p></div>
<h3 id="bug_fixing_11.14.16">Bug Fixing</h3>
<ul>
<li>It's now easier to use your own data in your apps. After integrating with external systems through Integration Builder, go to the "Logic" tab, choose a server action, drag and drop it to a list, table or accelerator to open "SELECT DATA" and decide what entity/attribute to use. (RIMPT-2246)</li>
</ul><div class="hidden" id="development-environment-11.14.16_end"></div><div class="hidden" id="development-environment-11.14.15_start"></div>
<h2 id="development_environment_11.14.15">Development Environment 11.14.15</h2>
<div class="info"><p>Released on May 02, 2022</p></div>
<h3 id="bug_fixing_11.14.15">Bug Fixing</h3>
<ul>
<li>Fixed issue where Service Studio would freeze when moving the cursor in content editor. (RMAC-9577)</li>
</ul>
<div class="hidden" id="development-environment-11.14.15_end"></div><div class="hidden" id="development-environment-11.14.14_start"></div>

<h2 id="development_environment_11.14.14">Development Environment 11.14.14</h2>
<div class="info"><p>Released on Apr 18, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="development-environment-11.14.14_end"></div><div class="hidden" id="development-environment-11.14.13_start"></div>

<h2 id="development_environment_11.14.13">Development Environment 11.14.13</h2>
<div class="info"><p>Released on Apr 11, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="development-environment-11.14.13_end"></div><div class="hidden" id="development-environment-11.14.12_start"></div>

<h2 id="development_environment_11.14.12">Development Environment 11.14.12</h2>
<div class="info"><p>Released on Apr 04, 2022</p></div>
This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="development-environment-11.14.12_end"></div><div class="hidden" id="development-environment-11.14.11_start"></div>

<h2 id="development_environment_11.14.11">Development Environment 11.14.11</h2>
<div class="info"><p>Released on Mar 24, 2022</p></div>
<h3 id="new_in_development_environment_11.14.11">New in Development Environment 11.14.11</h3>
<ul>
<li>When using Service Studio Stable for Windows on a Parallels virtual machine, you'll be prompted to install the Service Studio Stable version for MacOS. (RTAFB-5610)</li>
</ul>
<div class="hidden" id="development-environment-11.14.11_end"></div><div class="hidden" id="development-environment-11.14.10_start"></div>

<h2 id="development_environment_11.14.10">Development Environment 11.14.10</h2>
<div class="info"><p>Released on Mar 21, 2022</p></div>
<h3 id="new_in_development_environment_11.14.10">New in Development Environment 11.14.10</h3>
<ul>
<li>It is now possible to export the definition files from a consumed SOAP Web Service. (R11DT-911)</li>
</ul>
<h3 id="bug_fixing_11.14.10">Bug Fixing</h3>
<ul>
<li>Improved an error message by adding relevant information when an array lacks the items definition while importing a REST Web Service. (R11DT-382)</li>
<li>Fixed an issue that caused the installation of a sample app to fail. (RIMPT-1653)</li>
<li>Fixed an issue that gave an incorrect length attribute when importing a SOAP web service. (RPD-5047)</li>
<li>Fixed an issue when trying to connect to environment on Integration Studio. (RPM-1700)</li>
<li>Fixed an issue when consuming a SOAP web service with multiple headers, which were being ignored. (RPM-314)</li>
</ul>
<div class="hidden" id="development-environment-11.14.10_end"></div><div class="hidden" id="development-environment-11.14.8_start"></div>

<h2 id="development_environment_11.14.8">Development Environment 11.14.8</h2>
<div class="info"><p>Released on Feb 28, 2022</p></div>
<h3 id="bug_fixing_11.14.8">Bug Fixing</h3>
<ul>
<li>Fixed an issue that gave an incorrect length attribute when importing a SOAP web service. (RPD-5047)</li>
</ul>
<div class="hidden" id="development-environment-11.14.8_end"></div><div class="hidden" id="development-environment-11.14.7_start"></div>

<h2 id="development_environment_11.14.7">Development Environment 11.14.7</h2>
<div class="info"><p>Released on Feb 14, 2022</p></div>
<h3 id="new_in_development_environment_11.14.7">New in Development Environment 11.14.7</h3>
<ul>
<li>It is now possible to expose REST web services with the character "-" on the URL.
Inspired by <a href="https://www.outsystems.com/ideas/5205/allow-hyphen-in-url-path-of-an-exposed-api-web-method/" target="_blank" rel="noopener noreferrer">João Marques' idea</a>. (R11DT-870)</li>
</ul>
<h3 id="bug_fixing_11.14.7">Bug Fixing</h3>
<ul>
<li>Removed double error message when trying to set public blocks or screens to be reused in other modules, for Mobile Apps. (RMAC-9002)</li>
<li>Fixed an issue in which it was not possible to clone a module when there was multiple themes with similar names (RPM-2073)</li>
</ul>
<div class="hidden" id="development-environment-11.14.7_end"></div><div class="hidden" id="development-environment-11.14.5_start"></div>

<h2 id="development_environment_11.14.5">Development Environment 11.14.5</h2>
<div class="info"><p>Released on Jan 24, 2022</p></div>
<h3 id="new_in_development_environment_11.14.5">New in Development Environment 11.14.5</h3>
<ul>
<li>The 1-Click-Publish button received a new look for improved clarity, with action names now added to the button ('Publish', 'Open in browser', 'Errors found'). (RDEPT-64)</li>
</ul>
<div class="hidden" id="development-environment-11.14.5_end"></div><div class="hidden" id="development-environment-11.14.4_start"></div>

<h2 id="development_environment_11.14.4">Development Environment 11.14.4</h2>
<div class="info"><p>Released on Jan 17, 2022</p></div>
<h3 id="new_in_development_environment_11.14.4">New in Development Environment 11.14.4</h3>
<ul>
<li>It is now possible to expose REST web services with the character "-" on the URL.
Inspired by <a href="https://www.outsystems.com/ideas/5205/allow-hyphen-in-url-path-of-an-exposed-api-web-method/" target="_blank" rel="noopener noreferrer">João Marques' idea</a>. (R11DT-870)</li>
</ul>
<div class="hidden" id="development-environment-11.14.4_end"></div><div class="hidden" id="development-environment-11.14.3_start"></div>

<h2 id="development_environment_11.14.3">Development Environment 11.14.3</h2>
<div class="info"><p>Released on Jan 10, 2022</p></div>
<h3 id="new_in_development_environment_11.14.3">New in Development Environment 11.14.3</h3>
<ul>
<li>The 1-Click-Publish button received a new look for improved clarity, with action names now added to the button ('Publish', 'Open in browser', 'Errors found'). (RDEPT-64)</li>
</ul>
<div class="hidden" id="development-environment-11.14.3_end"></div><div class="hidden" id="development-environment-11.14.2_start"></div>

<h2 id="development_environment_11.14.2">Development Environment 11.14.2</h2>
<div class="info"><p>Released on Jan 03, 2022</p></div>
<h3 id="bug_fixing_11.14.2">Bug Fixing</h3>
<ul>
<li>Fixed not being able to restore the Service Studio window in Windows after it was minimized to the Taskbar (RMAC-8719)</li>
<li>Fixed a crash in Service Studio while performing a merge that envolves screen variables used in screen actions (RMAC-8735)</li>
<li>Fixed an issue where screens created from a template would not keep the chosen name. (RMAC-8745)</li>
</ul>
<div class="hidden" id="development-environment-11.14.2_end"></div><div class="hidden" id="development-environment-11.14.1_start"></div>

<h2 id="development_environment_11.14.1">Development Environment 11.14.1</h2>
<div class="info"><p>Released on Dec 20, 2021</p></div>
<h3 id="bug_fixing_11.14.1">Bug Fixing</h3>
<ul>
<li>Fixed an issue where Attachment Structures were incorrectly saved in the module preventing its publication. (RPM-1663)</li>
</ul>
<div class="hidden" id="development-environment-11.14.1_end"></div><div class="hidden" id="development-environment-11.14.0_start"></div>

<h2 id="development_environment_11.14.0">Development Environment 11.14.0</h2>
<div class="info"><p>Released on Dec 13, 2021</p></div>
<h3 id="new_in_development_environment_11.14.0">New in Development Environment 11.14.0</h3>
<ul>
<li>Features related to emails for Mobile and Reactive Web Apps are now generally available in Service Studio. You could use the features previously in technical the previews "Emails for Mobile and Reactive" and "Attachments in Mobile and Reactive emails". (RTAFA-77)</li>
</ul>
<div class="hidden" id="development-environment-11.14.0_end"></div><div class="hidden" id="development-environment-11.13.1_start"></div>

<h2 id="development_environment_11.13.1">Development Environment 11.13.1</h2>
<div class="info">
<p>Released on Dec 06, 2021</p></div>
<p>This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes.</p>
<div class="hidden" id="development-environment-11.13.1_end"></div><div class="hidden" id="development-environment-11.13.0_start"></div>

<h2 id="development_environment_11.13.0">Development Environment 11.13.0</h2>
<div class="info">
<p>Released on Nov 29, 2021</p></div>
<h3 id="new_in_development_environment_11.13.0">New in Development Environment 11.13.0</h3>
<ul>
<li>Now you can configure friendly URLs in your Reactive Web Apps. Go to Service Center &gt; Administration &gt; SEO URLs to set up the site rules and redirects. Configure the page rules in Service Studio, by setting Custom URLs to Yes in the Screen properties. (RTAFB-4453)</li>
</ul>
<li>Fixed a remote code execution vulnerability exploitable via phishing. CVSSv3.1 score 7.5 (High). (RPM-1054)</li>
<div class="hidden" id="development-environment-11.13.0_end"></div><div class="hidden" id="development-environment-11.12.8_start"></div>

<h2 id="development_environment_11.12.8">Development Environment 11.12.8</h2>
<div class="info">
<p>Released on Nov 22, 2021</p></div>
<h3 id="new_in_development_environment_11.12.8">New in Development Environment 11.12.8</h3>
<ul>
<li>Now it’s easier to find OutSystems UI components in Service Studio toolbox. (RIMPT-970)</li>
</ul>
<div class="hidden" id="development-environment-11.12.8_end"></div><div class="hidden" id="development-environment-11.12.7_start"></div>

<h2 id="development_environment_11.12.7">Development Environment 11.12.7</h2>
<div class="info">
<p>Released on Nov 08, 2021</p></div>
<h3 id="bug_fixing_11.12.7">Bug Fixing</h3>
<ul>
<li>Service Studio no longer crashes when, after changing a 'Run Client Actions's action, the 'Expand Element' of a list argument is clicked. (RDMST-812)</li>
</ul>
<div class="hidden" id="development-environment-11.12.7_end"></div><div class="hidden" id="development-environment-11.12.6_start"></div>

<h2 id="development_environment_11.12.6">Development Environment 11.12.6</h2>
<div class="info">
<p>Released on Nov 01, 2021</p></div>
<p>This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes.</p>
<div class="hidden" id="development-environment-11.12.6_end"></div><div class="hidden" id="development-environment-11.12.5_start"></div>

<h2 id="development_environment_11.12.5">Development Environment 11.12.5</h2>
<div class="info">
<p>Released on Oct 25, 2021</p></div>
<h3 id="new_in_development_environment_11.12.5">New in Development Environment 11.12.5</h3>
<ul>
<li>It's now easier to select data for Table and List widgets. Click "Select Data" in the Source property dropdown to fetch and bind data from an entity in a single operation. (RIMPT-846)</li>
</ul>
<div class="hidden" id="development-environment-11.12.5_end"></div><div class="hidden" id="development-environment-11.12.4_start"></div>

<h2 id="development_environment_11.12.4">Development Environment 11.12.4</h2>
<div class="info">
<p>Released on Oct 18, 2021</p></div>
<h3 id="new_in_development_environment_11.12.4">New in Development Environment 11.12.4</h3>
<ul>
<li>Fixed an issue that caused Service Studio to get stuck when using a custom color profile on Windows. (RICT-3947)</li>
</ul>
<div class="hidden" id="development-environment-11.12.4_end"></div><div class="hidden" id="development-environment-11.12.3_start"></div>

<h2 id="development_environment_11.12.3">Development Environment 11.12.3</h2>
<div class="info">
<p>Released on Oct 11, 2021</p></div>
<h3 id="new_in_development_environment_11.12.3">New in Development Environment 11.12.3</h3>
<ul>
<li>Installing a template (sample app) just got simpler. No dependency dialog is shown during installation. (RDRGT-181)</li>
</ul>
<h3 id="bug_fixing_11.12.3">Bug Fixing</h3>
<ul>
<li>Fixed a crash on aggregate when an entity attribute used in a group by year column is deleted. (RMAC-8113)</li>
</ul>
<div class="hidden" id="development-environment-11.12.3_end"></div><div class="hidden" id="development-environment-11.12.2_start"></div>

<h2 id="development_environment_11.12.2">Development Environment 11.12.2</h2>
<div class="info">
<p>Released on Oct 04, 2021</p></div>
<h3 id="new_in_development_environment_11.12.2">New in Development Environment 11.12.2</h3>
<ul>
<li>It's now easier to use data from your System of Records in your apps. In the "Logic" tab, open the context menu for "Integration with external systems" and select "New integration". (RIMPT-742)</li>
</ul>
<div class="hidden" id="development-environment-11.12.2_end"></div><div class="hidden" id="development-environment-11.12.1_start"></div>

<h2 id="development_environment_11.12.1">Development Environment 11.12.1</h2>
<div class="info">
<p>Released on Sep 27, 2021</p></div>
<h3 id="new_in_development_environment_11.12.1">New in Development Environment 11.12.1</h3>
<ul>
<li>Fixed an issue that caused Service Studio occasionally to crash when opening new windows. (RICT-3917)</li>
</ul>
<h3 id="bug_fixing_11.12.1">Bug Fixing</h3>
<ul>
<li>Fixed an issue that, under certain conditions, kept the last SOAP expose item visible in the tree after being deleted, causing a crash if another deletion try occurred. (RMAC-7876)</li>
</ul>
<div class="hidden" id="development-environment-11.12.1_end"></div><div class="hidden" id="development-environment-11.12.0_start"></div>

<h2 id="development_environment_11.12.0">Development Environment 11.12.0</h2>
<div class="info">
<p>Released on Sep 13, 2021</p></div>
<h3 id="new_in_development_environment_11.12.0">New in Development Environment 11.12.0</h3>
<ul>
<li>You can now use expressions to set titles of Screens. This lets you change the page title dynamically, and set unique values that show in the browser tabs, bookmarks, and results from the search engines. When using this feature, it is recomended that all developers in the same organization update Service Studio. (RTAFB-5082)</li>
</ul>
<div class="hidden" id="development-environment-11.12.0_end"></div><div class="hidden" id="development-environment-11.11.15_start"></div>

<h2 id="development_environment_11.11.15">Development Environment 11.11.15</h2>
<div class="info">
<p>Released on Sep 06, 2021</p></div>
<p>This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes.</p>
<div class="hidden" id="development-environment-11.11.15_end"></div><div class="hidden" id="development-environment-11.11.14_start"></div>

<h2 id="development_environment_11.11.14">Development Environment 11.11.14</h2>
<div class="info">
<p>Released on Aug 30, 2021</p>
</div>
<h3 id="new_in_development_environment_11.11.14">New in Development Environment 11.11.14</h3>
<ul>
<li>Now users have a link and dedicated FAQ session in case they have difficulties in the Sign in with email. (RDRGT-92)</li>
</ul>
<h3 id="bug_fixing_11.11.14">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented Integration Studio from connecting to some environments. (RDEV-3485)</li>
<li>Fix an issue in Service Studio that would cause Platform Server to fail to publish a solution due to an invalid certificate. (RPM-1208)</li>
<li>Fixed a bug when consuming a WSDL with an xsd:element and a xsd:complexType with the same name. (RPM-1337)</li>
<li>Fixed a bug that was removing translations when the dynamic page titles were on. (RTAFB-4999</li>
</ul>
<div class="hidden" id="development-environment-11.11.14_end"></div><div class="hidden" id="development-environment-11.11.13_start"></div>

<h2 id="development_environment_11.11.13">Development Environment 11.11.13</h2>
<div class="info">
<p>Released on Aug 17, 2021</p></div>
<h3 id="new_in_development_environment_11.11.13">New in Development Environment 11.11.13</h3>
<ul>
<li>Improved tooltip text on Publish button when with errors. (RDEV-3449)</li>
<li>Now users have a link and dedicated FAQ session in case they have difficulties in the Sign in with email. (RDRGT-92)</li>
<li>Support for new features in the email technical preview for Mobile and Reactive Web Apps, including attachments and new widgets. (RTAF-4812)</li>
</ul>
<h3 id="bug_fixing_11.11.13">Bug Fixing</h3>
<ul>
<li>Fixed template cache concurrent access issue. (RIMPT-539)</li>
</ul>
<div class="hidden" id="development-environment-11.11.13_end"></div><div class="hidden" id="development-environment-11.11.12_start"></div>

<h2 id="development_environment_11.11.12">Development Environment 11.11.12</h2>
<div class="info">
<p>Released on Aug 09, 2021</p></div>
<h3 id="new_in_development_environment_11.11.12">New in Development Environment 11.11.12</h3>
<ul>
<li>Support for new features in the email technical preview for Mobile and Reactive Web Apps, including attachments and new widgets. (RTAF-4812)</li>
</ul>
<h3 id="bug_fixing_11.11.12">Bug Fixing</h3>
<ul>
<li>Fixed a bug causing the window to become maximized upon startup. Window state is now properly restored. (RICT-3776)</li>
<li>Avoid crash when DoubleClick aggregate filter. (RMAC-7408)</li>
<li>Fix module freeze when trying to navigate from a warning message. (RMAC-7390)</li>
</ul>
<div class="hidden" id="development-environment-11.11.12_end"></div><div class="hidden" id="development-environment-11.11.11_start"></div>

<h2 id="development_environment_11.11.11">Development Environment 11.11.11</h2>
<div class="info">
<p>Released on Aug 02, 2021</p></div>
<h3 id="bug_fixing_11.11.11">Bug Fixing</h3>
<ul>
<li>Quick fix to make sure the entire text shows up on the node that have the letter Y or W to start or finish. (RMAC-7158)</li>
</ul>
<div class="hidden" id="development-environment-11.11.11_end"></div><div class="hidden" id="development-environment-11.11.10_start"></div>

<h2 id="development_environment_11.11.10">Development Environment 11.11.10</h2>
<div class="info">
<p>Released on Jul 26, 2021</p></div>
<h3 id="bug_fixing_11.11.10">Bug Fixing</h3>
<ul>
<li>Fixed the "Open in Browser" command so it opens page with a custom URL when the technical preview "SEO-friendly URLs for Reactive Web Apps" is on. (RTAF-4497)</li>
</ul>
<div class="hidden" id="development-environment-11.11.10_end"></div><div class="hidden" id="development-environment-11.11.9_start"></div>

<h2 id="development_environment_11.11.9">Development Environment 11.11.9</h2>
<div class="info"><p>Released on Jul 19, 2021</p></div>
<h3 id="bug_fixing_11.11.9">Bug Fixing</h3>
<ul>
<li>Fixed an issue on Aggregates that prevented the "Show hidden attributes" label from appearing. (RMAC-6458)</li>
<li>Fix issue that caused SS to crash when opening under certain conditions (RMAC-7104)</li>
</ul>
<div class="hidden" id="development-environment-11.11.9_end"></div><div class="hidden" id="development-environment-11.11.8_start"></div>

<h2 id="development_environment_11.11.8">Development Environment 11.11.8</h2>
<div class="info">Released on Jul 12, 2021</div>
<h3 id="new_in_development_environment_11.11.8">New in Development Environment 11.11.8</h3>
<ul>
<li>Now it's easier to find Widget information, with a help icon right from the widget properties panel. (RDRGT-80)</li>
<li>Improve the warning message when Preview Data is not available. (RTAF-4576)</li>
</ul>
<h3 id="bug_fixing_11.11.8">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused wrong colors in text cells while hovering a table column in an aggregate. (RDEV-3367)</li>
<li>Fixed an issue that prevented SQL nodes to be opened when the SQL query was empty. (RRCT-3804)</li>
</ul>
<div class="hidden" id="development-environment-11.11.8_end"></div><div class="hidden" id="development-environment-11.11.7_start"></div>

<h2 id="development_environment_11.11.7">Development Environment 11.11.7</h2>
<div class="info">

Released on Jul 05, 2021</div>
<h3 id="new_in_development_environment_11.11.7">New in Development Environment 11.11.7</h3>
<ul>
<li>When right-clicking on an Action node, a menu option to learn how to test actions is now available. (RDEV-3178)</li>
<li>Now, the debugger is also available in macOS, enabling you to find issues in your app logic. (RTAFB-4768)</li>
</ul>
<h3 id="bug_fixing_11.11.7">Bug Fixing</h3>
<ul>
<li>Added a minimum width to the Debugger panels on Service Studio to prevent them from being shrunk all the way and disappearing (RTAFB-4785)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.5 (High). (RPM-689)</li>
</ul>
<h3 id="more_details_11.11.7">More details</h3>
<strong>RPM-689</strong><br/><b>Fixed a security vulnerability. CVSSv3.1 score 8.5 (High).</b><br/><br/><br/><u>Fix Details:</u><br/>Service Studio and Integration Studio weren't properly validating the TLS connections. It was possible to perform a MITM attack using a self-signed certificate after the initial connection is established without the developer noticing. This vulnerability was classified as High with a risk score of 8.5. Check more details about the vulnerability in <a href="https://success.outsystems.com/Support/Security/Vulnerabilities/Vulnerability_RPM-689" target="_blank" rel="noopener noreferrer">this security bulletin</a>.

<div class="hidden" id="development-environment-11.11.7_end"></div><div class="hidden" id="development-environment-11.11.6_start"></div>

<h2 id="development_environment_11.11.6">Development Environment 11.11.6</h2>
<div class="info">

Released on Jun 28, 2021
</div>
<h3 id="new_in_development_environment_11.11.6">New in Development Environment 11.11.6</h3>
<ul>
<li>Improved error messages when logging into unavailable free environments, according to their current state (asleep, stopped, in maintenance, or being created). (RDEV-3029)</li>
<li>It's now possible to set the Page Name property with a screen name, a module name, a flow name, or a block name. (RTAF-4656)</li>
</ul>
<h3 id="bug_fixing_11.11.6">Bug Fixing</h3>
<ul>
<li>Fix for issue causing the unexpected behavior of showing the Entity attributes with extra margin on Client Entity From Database dialog when copying multiple Entities from the Database and pasting to the Local Storage. (RMAC-6728)</li>
<li>Fix a bug that was preventing showing all the Native Platform tab when connected to a Platform Server with version below 11.8.* (RMAC-6791)</li>
<li>Fixed a bug on Service Studio REST Consume of methods using 'application/x-www-form-urlencoded'. (RPM-531)</li>
</ul>
<div class="hidden" id="development-environment-11.11.6_end"></div><div class="hidden" id="development-environment-11.11.5_start"></div>

<h2 id="development_environment_11.11.5">Development Environment 11.11.5</h2>
<div class="info">

Released on Jun 22, 2021</div>
<h3 id="new_in_development_environment_11.11.5">New in Development Environment 11.11.5</h3>
<ul>
<li>Now, while editing data, the apply and discard buttons are closer to the records. (RDEV-3306)</li>
</ul>
<h3 id="bug_fixing_11.11.5">Bug Fixing</h3>
<ul>
<li>Fixed an issue that allowed Sorts to be removed while refreshing preview data during data edition. (RDEV-3275)</li>
<li>Fixed an issue that prevented Aggregates from having a spacing between the tabs and the table. (RDEV-3319)</li>
<li>Fixed an issue that mislead the user applying bold, italic and underline format on Text interface element when using the keys combination ctrl+b, ctrl+i, ctrl+u, command+b, command+i, command+u are pressed. (RMAC-6727)</li>
<li>Fix an issue that caused a broken display of preview data in Aggregates when showing previously hidden attributes and using groups (RMAC-6731)</li>
</ul>
<div class="hidden" id="development-environment-11.11.5_end"></div><div class="hidden" id="development-environment-11.11.4_start"></div>

<h2 id="development_environment_11.11.4">Development Environment 11.11.4</h2>
<div class="info">Released on Jun 14, 2021</div>
<h3 id="new_in_development_environment_11.11.4">New in Development Environment 11.11.4</h3>
<ul>
<li>Now, when creating an application based on a sample app, Service Studio gives the ability to preview the app being installed. (RDEV-3295)</li>
<li>Now, when resetting styles in Theme Editor, it's easier to undo them. (RDEV-3034)</li>
<li>Improved the suggestion list for the "New Attribute" accelerator on Nodes and Widgets.  (RTAF-4689)</li>
</ul>
<h3 id="bug_fixing_11.11.4">Bug Fixing</h3>
<ul>
<li>Add missing descriptions to every attribute within the Request/CustomizedRequest parameters and Response/CustomizedResponse parameters. (R11DT-72)</li>
<li>Fixed issue preventing the user to see the preview images and text from a screen created using the Product Catalog screen template. (RMAC-6666)</li>
<li>Fixed an issue that sometimes caused an error in a hidden property and, when the user tried to navigate to the error, Service Studio would crash. (RMAC-6526)</li>
<li>Improve the reuse of existing Google Chrome windows when starting a debugging session on Reactive and Mobile applications (RTAF-4713)</li>
</ul>
<div class="hidden" id="development-environment-11.11.4_end"></div><div class="hidden" id="development-environment-11.11.3_start"></div>

<h2 id="development_environment_11.11.3">Development Environment 11.11.3</h2>
<div class="info">

Released on Jun 07, 2021

</div>
<h3 id="new_in_development_environment_11.11.3">New in Development Environment 11.11.3</h3>
<ul>
<li>Changed the icon for the "show in tree" aggregates' functionality. (RDEV-3264)</li>
<li>Improved the help text for the PWA applications. (RDEV-3277)</li>
</ul>
<h3 id="bug_fixing_11.11.3">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Aggregates to allow creating a Filter while editing data. (RDEV-2936)</li>
<li>Fixed an issue that caused Aggregates to go blank while discarding changes with added rows. (RDEV-3267)</li>
<li>Fixed an issue that was preventing Edit Data row operations to work. (RDEV-3268)</li>
<li>Fixed an issue on Service Studio that could cause a crash trying to merge widgets in placeholders on some circumstances. (RDMST-597)</li>
<li>Fixed UI issues in the debugger pane that occurred while using Service Studio in dark mode. (RMAC-3198)</li>
<li>Fixed issue that prevented the creation of an empty screen while the Screen Templates Dialog was checking for new templates. (RMAC-4324)</li>
<li>Fixed an issue that occurred in macOS while using the "Open from Environment" dialog related to opening a module by pressing the Return key. This issue occurred when you filtered the list of modules until you only had one module in the list. (RMAC-5050)</li>
<li>Referenced screens can no longer be assigned to the Default or Splash Screen properties of the Module. This unsupported scenario was possible and lead to compilation crashes. (RPM-1135)</li>
<li>Fixed a crash on merge operation that was caused by duplicated keys when objects changed their parent under some circumstances. (RPM-377)</li>
</ul>
<div class="hidden" id="development-environment-11.11.3_end"></div><div class="hidden" id="development-environment-11.11.2_start"></div>

<h2 id="development_environment_11.11.2">Development Environment 11.11.2</h2>
<div class="info">

Released on May 31, 2021</div>
<h3 id="new_in_development_environment_11.11.2">New in Development Environment 11.11.2</h3>
<ul>
<li>Now, default screens can be set on screen flows. (RDEV-3038)</li>
<li>Updated URL when opening a screen in browser to use the Screen's Page Name when SEO Friendly-URLs are used. (RTAF-3963)</li>
</ul>
<h3 id="bug_fixing_11.11.2">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the Upload icon to don't appear while Editing Data in Aggregates. (RDEV-2795)</li>
<li>Increased the size of the radio button on ServiceStudio (RMAC-3312)</li>
</ul>
<div class="hidden" id="development-environment-11.11.2_end"></div><div class="hidden" id="development-environment-11.11.0_start"></div>

<h2 id="development_environment_11.11.0">Development Environment 11.11.0</h2>
<div class="info">

Released on May 25, 2021</div>
<h3 id="new_in_development_environment_11.11.0">New in Development Environment 11.11.0</h3>
<ul>
<li>Refresh a consumed REST service importing a new OpenAPI 2.0 (swagger) or OpenAPI 3.0 specification. Inspired by <a href="https://www.outsystems.com/ideas/2376/consume-rest-services-update-api-methods/" target="_blank" rel="noopener noreferrer"> Laura Petrisor's idea </a>. (R11DT-274)</li>
<li>Now aggregates Sources tab is expanded by default. (RDEV-3045)</li>
<li>Now you can configure friendly URLs in your Reactive Web Apps. Go to Service Center &gt; Administration &gt; SEO URLs to set up the site rules and redirects. Configure the page rules in Service Studio, by setting Custom URLs to Yes in the Screen properties. SEO Friendly URLs is a technical preview feature, and you need to activate the option "SEO Friendly URLs" in LifeTime. (RTAF-4116)</li>
<li>You can now translate the UI of your Reactive Web Apps and Mobile Apps directly inside Service Studio. (RTAF-4332)</li>
<li>Now you can, in Mobile and Reactive Web Apps, create lightweight emails with basic navigation and styling. Emails in Reactive and Mobile is a technical preview feature, so you need to activate the option "Emails for Mobile and Reactive" in LifeTime. (RTAF-4378)</li>
</ul>
<h3 id="bug_fixing_11.11.0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash when discarding pending actions in Edit Data. (RDEV-3191)</li>
<li>Fixed issue regarding the delete icon position on filters and sorts in Aggregates. (RMAC-6465)</li>
<li>Fixed an issue that showed invalid options of join types on client side Aggregates. (RMAC-6474)</li>
<li>Updated the debugger pane to change at what size the of the horizontal scrollbar should appear. (RMAC-5967)</li>
</ul>
<div class="hidden" id="development-environment-11.11.0_end"></div><div class="hidden" id="development-environment-11.10.22_start"></div>

<h2 id="development_environment_11.10.22">Development Environment 11.10.22</h2>
<div class="info">

Released on May 10, 2021</div>
<h3 id="new_in_development_environment_11.10.22">New in Development Environment 11.10.22</h3>
<ul>
<li>Now, it's easier to understand what to do when the incompatible dependencies warning pops up. (RDEV-3176)</li>
<li>Now, it is easier to find the Theme editor in StyleSheet editor. (RDEV-3035)</li>
</ul>
<h3 id="bug_fixing_11.10.22">Bug Fixing</h3>
<ul>
<li>Fixed a typo in the Edit Data success message. (RDEV-3189)</li>
<li>Fixed issue regarding the group header beeing shown when groups are hidden in Aggregates. (RMAC-6432)</li>
<li>Fixed issues regarding sub-editors content width in Aggregates. (RMAC-6318)</li>
<li>Fixed issue regarding the missing double click on table calculated columns header in Aggregates. (RMAC-6174)</li>
<li>Fixed an issue that changed the selection when clicking on the scrollbar inside the Aggregate. (RMAC-6172)</li>
<li>Fixed issue regarding the table columns adjustment in Aggregates. (RMAC-6184)</li>
<li>Fixed an issue that caused a new calculated attribute in the aggregates not to refresh after being edited. (RMAC-6133)</li>
<li>Fixed issue regarding the empty aggregate image size. (RMAC-6027)</li>
<li>Fix issue on aggregates where empty cells were incorrectly shown after unhide of attributes (RMAC-6409)</li>
</ul>
<div class="hidden" id="development-environment-11.10.22_end"></div><div class="hidden" id="development-environment-11.10.20_start"></div>

<h2 id="development_environment_11.10.20">Development Environment 11.10.20</h2>
<div class="info">

Released on Apr 26, 2021</div>
<h3 id="bug_fixing_11.10.20">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio not to be opened when trying to open it from LifeTime. (RICT-3325)</li>
<li>Fix aggregates auto-refresh option disabled not tacking effect.</li>
<li>Fix reorder of columns while requesting preview data to the server (RMAC-5895)</li>
</ul>
<div class="hidden" id="development-environment-11.10.20_end"></div><div class="hidden" id="development-environment-11.10.19_start"></div>

<h2 id="development_environment_11.10.19">Development Environment 11.10.19</h2>
<div class="info">

Released on Apr 19, 2021</div>
<h3 id="bug_fixing_11.10.19">Bug Fixing</h3>
<ul>
<li>Fixed an error when importing SOAP services with an element and a ComplexType with the same name and namespace. (RBIT-42)</li>
<li>Fixed an issue that was preventing an account to be created inside Service Studio. (RIMPT-298)</li>
<li>Fixed an issue that prevents selecting an Aggregate in pop-out mode when clicking anywhere in the window. (RMAC-5986)</li>
<li>Fixed an issue that occasionally caused dropdown menus not to open in Aggregates. (RMAC-6002)</li>
<li>Fixed issues regarding the scroll and width adjustments in Aggregates. (RMAC-6010)</li>
<li>Fixed an issue that prevents the user to read the full Entities' name in Aggregates' joins (RMAC-6021)</li>
</ul>
<div class="hidden" id="development-environment-11.10.19_end"></div><div class="hidden" id="development-environment-11.10.18_start"></div>

<h2 id="development_environment_11.10.18">Development Environment 11.10.18</h2>
<div class="info">

Released on Apr 12, 2021</div>
<h3 id="new_in_development_environment_11.10.18">New in Development Environment 11.10.18</h3>
<ul>
<li>Now, the Aggregates Test Values input boxes are bigger and easier to use. (RDEV-2969)</li>
<li>Improve aggregates' tab title to meet the number of elements in that tab (e.g. 1 Filter, 2 Filters). (RDEV-2962)</li>
<li>It is now possible to resize and maximize the Debug Variable Data Grid dialog. (RDEV-2951)</li>
</ul>
<h3 id="bug_fixing_11.10.18">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the aggregates to automatically refresh preview data when the user had the option disabled.  (RDEV-2960)</li>
<li>Fixed an issue that caused the Service Studio to crash when clicking on the "Aggregates is disabled" link, in Aggregates. (RDEV-2958)</li>
<li>Fixed an issue that caused error messages to appear duplicated in Aggregates. (RDEV-2959)</li>
<li>Fixed an issue that was preventing an account to be created inside Service Studio. (RIMPT-298)</li>
<li>Fixed an issue that prevents selecting an Aggregate in pop-out mode when clicking anywhere in the window. (RMAC-5986)</li>
<li>Fixed an issue that caused Service Studio to crash when dropping some elements into an If widget. (RTAF-4363)</li>
</ul>
<h3 id="side_effects">Side Effects</h3>
<ul>
<li>
<b>Issue</b>: After updating to this version, opening an older version of Service Studio 11 in the same machine resets local Service Studio settings. These settings include the Service Studio preferences, the list of environments and recently opened modules, and login information.<br/>
<b>Rationale</b>: We changed the syntax of the local settings file (C:\Users\{user}\AppData\Local\OutSystems\ServiceStudio 11.0\Settings.xml) to support upcoming features.<br/>
<b>Workaround</b>: Before opening this version of Service Studio 11, please backup the settings files located in (C:\Users\{user}\AppData\Local\OutSystems\ServiceStudio 11.0\Settings.xml).
</li>
</ul>
<div class="hidden" id="development-environment-11.10.18_end"></div><div class="hidden" id="development-environment-11.10.17_start"></div>

<h2 id="development_environment_11.10.17">Development Environment 11.10.17</h2>
<div class="info">

Released on Apr 07, 2021</div>
<h3 id="bug_fixing_11.10.17">Bug Fixing</h3>
<ul>
<li>Fixed Service Studio not connecting to a device when starting a Debug Session using the Android option (RPM-961)</li>
<li>Fixed an intermittent crash that can occur when dragging and dropping widgets onto a form. (RTAF-4293)</li>
</ul>
<div class="hidden" id="development-environment-11.10.17_end"></div><div class="hidden" id="development-environment-11.10.16_start"></div>

<h2 id="development_environment_11.10.16">Development Environment 11.10.16</h2>
<div class="info">

Released on Mar 29, 2021</div>
<h3 id="new_in_development_environment_11.10.16">New in Development Environment 11.10.16</h3>
<ul>
<li>Upgraded OutSystems.Spreadsheet library. (RRCT-3540)</li>
<li>Improved the Theme Editor colors display for a clear understanding of colors in use. (RDEV-2537)</li>
<li>Now you can quickly create, update, and delete your entities' data when connected to environments with "Development" or "Non-Production" purpose. Inspired by <a href="https://www.outsystems.com/ideas/5407/edit-data-directly-in-viewdata-editor-inside-service-studio" target="_blank" rel="noopener noreferrer">Marios Tofarides' idea</a>. Platform Server 11.11.1 or higher required. (RDEV-2769)</li>
<li>We updated the Aggregates look &amp; feel — it is now cleaner and more modern-looking, consistent with the rest of the Service Studio interface. (RDEV-2963)</li>
<li>Now, when running the tutorial, Service Studio does not delete previous tutorial applications. (RIMPT-122)</li>
</ul>
<div class="hidden" id="development-environment-11.10.16_end"></div><div class="hidden" id="development-environment-11.10.15_start"></div>

<h2 id="development_environment_11.10.15">Development Environment 11.10.15</h2>
<div class="info">

Released on Mar 22, 2021</div>
<h3 id="bug_fixing_11.10.15">Bug Fixing</h3>
<ul>
<li>Fixed a bug in Service Studio while using Graphic Hardware Acceleration and that caused render and usability issues. This issue could prevent you from entering your credentials in the "Sign in" dialog. (RICT-3169)</li>
</ul>
<div class="hidden" id="development-environment-11.10.15_end"></div><div class="hidden" id="development-environment-11.10.14_start"></div>

<h2 id="development_environment_11.10.14">Development Environment 11.10.14</h2>
<div class="info">

Released on Mar 15, 2021</div>
<h3 id="new_in_development_environment_11.10.14">New in Development Environment 11.10.14</h3>
<ul>
<li>Now, when editing the environment name, it is possible to end the edition by pressing "Enter", setting the new name. (RDEV-2806)</li>
<li>Improved the right-click menus by moving the Help option to the bottom. Inspired by <a href="https://www.outsystems.com/ideas/Idea_View.aspx?IdeaID=10285" target="_blank" rel="noopener noreferrer">Luis Filipe Oliveira's idea</a>. (RDEV-2799)</li>
<li>Improved the look and feel of the "Distribute" tab shown in the app detail screen of  Mobile apps. (RMAC-5398)</li>
</ul>
<h3 id="bug_fixing_11.10.14">Bug Fixing</h3>
<ul>
<li>Fixed an issue when consuming a SOAP web service that includes schemas with an empty targetNamespace. (RBIT-158)</li>
<li>Fixed an issue when consuming a REST API from a swagger with a application/json response format but a simple type. (RBIT-168)</li>
<li>Fixed an issue that caused the environment custom name to be set when connecting to a new environment. (RDEV-2796)</li>
<li>Fixed an issue that caused the port number to not be displayed when selecting a hostname in the Login. (RDEV-2794)</li>
<li>Fixed a bug in Service Studio while using Graphic Hardware Acceleration and that caused render and usability issues. This issue could prevent you from entering your credentials in the "Sign in" dialog. (RICT-3169)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.8 (High). (RPST-1330)</li>
</ul>
<div class="hidden" id="development-environment-11.10.14_end"></div><div class="hidden" id="development-environment-11.10.13_start"></div>

<h2 id="development_environment_11.10.13">Development Environment 11.10.13</h2>
<div class="info">

Released on Mar 08, 2021</div>
<h3 id="bug_fixing_11.10.13">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a compile error when assigning a Boolean to a long integer.  Boolean values will now be implicitly converted to long integers. (RTAF-4173)</li>
<li>Fixed an issue in Service Studio that was causing window misalignment when opening Submit Feedback window (RICT-3103)</li>
</ul>
<div class="hidden" id="development-environment-11.10.13_end"></div><div class="hidden" id="development-environment-11.10.12_start"></div>

<h2 id="development_environment_11.10.12">Development Environment 11.10.12</h2>
<div class="info">

Released on Mar 01, 2021</div>
<h3 id="new_in_development_environment_11.10.12">New in Development Environment 11.10.12</h3>
<ul>
<li>Now, you don't need to log in to the Forge while accessing it inside the Service Studio. (RDEV-2557)</li>
<li>Added a hotkey to access "Add Dependency" via Module menu. (RIMPT-92)</li>
<li>Updated Oracle Managed Driver from 19.3.1 to 19.10.1 (RPLAT-542)</li>
</ul>
<h3 id="bug_fixing_11.10.12">Bug Fixing</h3>
<ul>
<li>Fixed a Service Studio crash when debugging a mobile application with external links using an iOS device (RPM-453)</li>
<li>Fixed an issue that caused screen template categories to appear at the bottom edge of the New Screen dialog when the list is too long to fit within the available space.  Added a scroll bar so that the entire list can be viewed and displayed properly. (RTAF-3971)</li>
<li>Fixed an issue where an application could get stuck on shutdown or reload operations waiting for RabbitMQ requests. (RRCT-3467)</li>
</ul>
<div class="hidden" id="development-environment-11.10.12_end"></div><div class="hidden" id="development-environment-11.10.11_start"></div>

<h2 id="development_environment_11.10.11">Development Environment 11.10.11</h2>
<div class="info">

Released on Feb 22, 2021</div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes. 

<div class="hidden" id="development-environment-11.10.11_end"></div><div class="hidden" id="development-environment-11.10.10_start"></div>

<h2 id="development_environment_11.10.10">Development Environment 11.10.10</h2>
<div class="info">

Released on Feb 15, 2021</div>
<h3 id="new_in_development_environment_11.10.10">New in Development Environment 11.10.10</h3>
<ul>
<li>The Smart Guidance feature will now try to display contextual suggestions. (RAID-791)</li>
<li>- Capture the metrics about visitors and visits for Reactive/Mobile applications using the cookies that we already use for Traditional Web.
- The metrics captured are correlated with Traditional Web applications if using the same browser/device. (RAR-538)</li>
</ul>
<h3 id="bug_fixing_11.10.10">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio popups to appear in an incorrect position when using more than one screen. (RICT-3069)</li>
<li>Service Studio no longer crashes when you work with Blocks hidden by the "Show true / false branch only" option of an If widget. (RTAF-4154)</li>
</ul>
<div class="hidden" id="development-environment-11.10.10_end"></div><div class="hidden" id="development-environment-11.10.9_start"></div>

<h2 id="development_environment_11.10.9">Development Environment 11.10.9</h2>
<div class="info">

Released on Feb 08, 2021</div>
<h3 id="bug_fixing_11.10.9">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to present a wrong display name while dragging Exceptions to a Flow. (RDEV-2713)</li>
<li>Fixed an issue displaying text with quotes and hashes on Aggregates and View Data. (RIMPT-3)</li>
</ul>
<div class="hidden" id="development-environment-11.10.9_end"></div><div class="hidden" id="development-environment-11.10.8_start"></div>

<h2 id="development_environment_11.10.8">Development Environment 11.10.8</h2>
<div class="info">

Released on Feb 01, 2021</div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes. 

<div class="hidden" id="development-environment-11.10.8_end"></div><div class="hidden" id="development-environment-11.10.7_start"></div>

<h2 id="development_environment_11.10.7">Development Environment 11.10.7</h2>
<div class="info">

Released on Jan 25, 2021</div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes. 

<div class="hidden" id="development-environment-11.10.7_end"></div><div class="hidden" id="development-environment-11.10.6_start"></div>

<h2 id="development_environment_11.10.6">Development Environment 11.10.6</h2>
<div class="info">

Released on Jan 18, 2021</div>
<h3 id="bug_fixing_11.10.6">Bug Fixing</h3>
<ul>
<li>Fixed an issue where the debugger didn't work for Client Actions with Android devices. (RPM-664)</li>
</ul>
<div class="hidden" id="development-environment-11.10.6_end"></div><div class="hidden" id="development-environment-11.10.5_start"></div>

<h2 id="development_environment_11.10.5">Development Environment 11.10.5</h2>
<div class="info">

Released on Jan 11, 2021</div>
<h3 id="new_in_development_environment_11.10.5">New in Development Environment 11.10.5</h3>
<ul>
<li>Now you can open the Entity data viewer by selecting an Entity in the tree and pressing the Enter key. Inspired by <a href="https://www.outsystems.com/ideas/6282/shortcut-for-view-data" target="_blank" rel="noopener noreferrer">Willem Markus' idea</a>. (RDEV-2534)</li>
</ul>
<h3 id="bug_fixing_11.10.5">Bug Fixing</h3>
<ul>
<li>Fixed a crash when consuming a WSDL with a choice that contains a reference to a previously declared group. (RBIT-121)</li>
</ul>
<div class="hidden" id="development-environment-11.10.5_end"></div><div class="hidden" id="development-environment-11.10.4_start"></div>

<h2 id="development_environment_11.10.4">Development Environment 11.10.4</h2>
<div class="info">

Released on Dec 28, 2020</div>
<h3 id="new_in_development_environment_11.10.4">New in Development Environment 11.10.4</h3>
<ul>
<li>Now you can give an alias to your environments to help you identify them in the Login dialog. You can also delete the ones you don't use. Inspired by <a href="https://www.outsystems.com/ideas/3433/manage-saved-environments-option-to-clear-environment-details-from-drop-down-an" target="_blank" rel="noopener noreferrer">Suraj Borade's idea</a>. (RDEV-2509)</li>
</ul>
<div class="hidden" id="development-environment-11.10.4_end"></div><div class="hidden" id="development-environment-11.10.3_start"></div>

<h2 id="development_environment_11.10.3">Development Environment 11.10.3</h2>
<div class="info">

Released on Dec 21, 2020</div>
<h3 id="new_in_development_environment_11.10.3">New in Development Environment 11.10.3</h3>
<ul>
<li>Fixed an issue that caused Service Studio to take several seconds to load an OML when contain screens with thousand of nodes. (RICT-2920)</li>
<li>Fixed a compilation error by adding the missing validations for updated Trigger Event nodes, for example when you copy and paste a Trigger Event between Blocks. Now Service Studio timely warns you about invalid expressions and prevents you from trying to run 1-Click Publish. (RTAF-3793)</li>
</ul>
<div class="hidden" id="development-environment-11.10.3_end"></div><div class="hidden" id="development-environment-11.10.2_start"></div>

<h2 id="development_environment_11.10.2">Development Environment 11.10.2</h2>
<div class="info">

Released on Dec 15, 2020</div>
<h3 id="new_in_development_environment_11.10.2">New in Development Environment 11.10.2</h3>
<ul>
<li>Now we automatically reference the SetCurrentLocale Client System action when adding a new locale in Mobile or Reactive Apps. (RTAF-3226)</li>
<li>There's now a notification for new developers, telling them they can use the Smart Guidance feature to find help when developing apps. (RAID-883)</li>
</ul>
<h3 id="bug_fixing_11.10.2">Bug Fixing</h3>
<ul>
<li>Added the option to view a producer Entity details in a consumer module. (RDEV-2495)</li>
</ul>
<div class="hidden" id="development-environment-11.10.2_end"></div><div class="hidden" id="development-environment-11.10.1_start"></div>

<h2 id="development_environment_11.10.1">Development Environment 11.10.1</h2>
<div class="info">

Released on Dec 07, 2020</div>
<h3 id="bug_fixing_11.10.1">Bug Fixing</h3>
<ul>
<li>Provide detailed information to the user about the Service Studio  crash when getting access denied error on filesystem while saving the OML in the local machine. (RDEV-2456)</li>
<li>Fixed several crashes that occurred when using Service Studio's -diff command line (RDMST-168)</li>
<li>Fixed a null reference exception when importing/exporting translations. (RTAF-3766)</li>
<li>We updated ADB to version 30.0.5, to improve debugging native apps in Service Studio and fix the "No Data to read" error. (RTAF-3733)</li>
</ul>
<div class="hidden" id="development-environment-11.10.1_end"></div><div class="hidden" id="development-environment-11.10.0_start"></div>

<h2 id="development_environment_11.10.0">Development Environment 11.10.0</h2>
<div class="info">

Released on Nov 30, 2020</div>
<h3 id="bug_fixing_11.10.0">Bug Fixing</h3>
<ul>
<li>Fixed a bug that did not allow to import a service when there was ambiguity in "xsd:any" wildcard (RPD-5255)</li>
<li>Fixed an issue where the commands to Import/Export Language resources where not available in the module menu for Reactive and Mobile Apps with the Multilingual technical preview feature enabled. (RTAF-3373)</li>
<li>Fixed an issue that caused Service Studio to crash when dropping an Entity into an If widget. (RTAF-3435)</li>
</ul>
<div class="hidden" id="development-environment-11.10.0_end"></div><div class="hidden" id="development-environment-11.9.2_start"></div>

<h2 id="development_environment_11.9.2">Development Environment 11.9.2</h2>
<div class="info">

Released on Nov 24, 2020</div>
<h3 id="new_in_development_environment_11.9.2">New in Development Environment 11.9.2</h3>
<ul>
<li>Improved the Service Studio accuracy of asking for feedback while creating a new application based on a sample app. (RDEV-2380)</li>
</ul>
<h3 id="bug_fixing_11.9.2">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the labels of condition connectors of a Switch to show incorrect values after reordering the conditions. (RDEV-2381)</li>
<li>Fixed an issue that caused Service Studio to crash when opening a Web Block. (RICT-2881)</li>
<li>Fixed a crash while opening a Screen using a Web Block. (RICT-2884)</li>
</ul>
<div class="hidden" id="development-environment-11.9.2_end"></div><div class="hidden" id="development-environment-11.9.0_start"></div>

<h2 id="development_environment_11.9.0">Development Environment 11.9.0</h2>
<div class="info">

Released on Nov 09, 2020</div>
<h3 id="new_in_development_environment_11.9.0">New in Development Environment 11.9.0</h3>
<ul>
<li>Service Studio will now require installation of .NET 4.7.2 (as stated in System Requirements). (RICT-2083)</li>
<li>You can now translate the UI of your Reactive Web Apps and Mobile Apps directly inside Service Studio. Multilingual is a technical preview feature and you need to activate the option "Multilingual for Mobile and Reactive" in LifeTime. After enabling the feature, use the new Multilingual Locales folder and new SetCurrentLocale system client action. (RTAF-3387)</li>
<li>Fixed an issue that caused Service Studio to crash while opening modules that contain expressions that rely on implicit conversions between different data types. (RICT-2859)</li>
<li>When importing a REST Web Service through a Swagger specification, it is now possible to choose what methods to import. Inspired by <a href="https://www.outsystems.com/ideas/4849/rest-consume-all-select-which-methods" target="_blank" rel="noopener noreferrer">Kilian Hekhuis's idea</a>.</li>
</ul>
<h3 id="bug_fixing_11.9.0">Bug Fixing</h3>
<ul>
<li>Addressed a discrepancy in the documented behavior of ExcelToRecordList when the SheetName parameter is left empty. Now it correctly indicates that the method will attempt to import a sheet called "Sheet1" and only if that is not available will it import the first sheet of the document. (RDEV-2311)</li>
</ul>
<div class="hidden" id="development-environment-11.9.0_end"></div><div class="hidden" id="development-environment-11.9.1_start"></div>

<h2 id="development_environment_11.9.1">Development Environment 11.9.1</h2>
<div class="info">Released on Nov 16, 2020</div>
<h3 id="bug_fixing_11.9.1">Bug Fixing</h3>
<ul>
<li>Added a description to the IgnoreCase input of the Index built-in function. (RDEV-2359)</li>
<li>Fixed an issue that caused some Shortcut Keys to not being presented correctly. (RDEV-2355)</li>
<li>Fixed an issue that caused the Find and Replace dialog to not focus on the "find" input. Thanks to <a href="https://www.outsystems.com/ideas/9647/" target="_blank" rel="noopener noreferrer">Pedro Oliveira's idea</a>. (RDEV-2354)</li>
<li>Fixed an issue that caused auto-assign data types to have wrong values. (RDEV-2360)</li>
<li>Fixed an issue that caused a crash in 'Search in other Modules' after selecting 'Open' to open an element in the producer module. (RDEV-2148)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 8.2 (High). (RICT-2855)</li>
</ul>
<div class="hidden" id="development-environment-11.9.1_end"></div><div class="hidden" id="development-environment-11.8.14_start"></div>
<div class="hidden" id="development-environment-11.8.14_end"></div><div class="hidden" id="development-environment-11.8.13_start"></div>

<h2 id="development_environment_11.8.13">Development Environment 11.8.13</h2>
<div class="info">

Released on Nov 02, 2020</div>
<h3 id="new_in_development_environment_11.8.13">New in Development Environment 11.8.13</h3>
<ul>
<li>Introduced a new way to get guidance to overcome problems by searching our documentation in a tailored way. (RAID-784)</li>
<li>It is now possible to close all modules at once. (RDEV-2316)</li>
</ul>
<h3 id="bug_fixing_11.8.13">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a "404 not found" error when trying to consume some REST API by URL. (RBIT-74)</li>
<li>We fixed pasting logic with lists of structures from client to server. Now the pasted logic works correctly on the server side. (RTAF-3582)</li>
<li>Fixed a security vulnerability. CVSSv3.1 score 7.9 (High). (RICT-2849)</li>
</ul>
<div class="hidden" id="development-environment-11.8.13_end"></div><div class="hidden" id="development-environment-11.8.12_start"></div>

<h2 id="development_environment_11.8.12">Development Environment 11.8.12</h2>
<div class="info">

Released on Oct 26, 2020</div>
<h3 id="new_in_development_environment_11.8.12">New in Development Environment 11.8.12</h3>
<ul>
<li>Supported mobile plugins are now hidden in the Application List and can be made visible via Preferences Menu. (RDEV-2092)</li>
</ul>
<h3 id="bug_fixing_11.8.12">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while trying to manage Dependencies during a 1-Click Publish. (RICT-2828)</li>
<li>Improve loading time of items picker dialog. (RMAC-4168)</li>
<li>We added support for debugging sessions on devices running iOS version 14. Now the debugging sessions in Service Studio work correctly. (RPM-444)</li>
</ul>
<div class="hidden" id="development-environment-11.8.12_end"></div><div class="hidden" id="development-environment-11.8.11_start"></div>

<h2 id="development_environment_11.8.11">Development Environment 11.8.11</h2>
<div class="info">

Released on Oct 19, 2020</div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes. 

<div class="hidden" id="development-environment-11.8.11_end"></div><div class="hidden" id="development-environment-11.8.10_start"></div>

<h2 id="development_environment_11.8.10">Development Environment 11.8.10</h2>
<div class="info">

Released on Oct 13, 2020</div>
<h3 id="bug_fixing_11.8.10">Bug Fixing</h3>
<ul>
<li>Fixed a bug that caused Service Center to incorrectly count Internal and External Users from disabled User Providers as active users. (RIDT-95)</li>
</ul>
<div class="hidden" id="development-environment-11.8.10_end"></div><div class="hidden" id="development-environment-11.8.9_start"></div>

<h2 id="development_environment_11.8.9">Development Environment 11.8.9</h2>
<div class="info">

Released on Oct 06, 2020</div>
<h3 id="new_in_development_environment_11.8.9">New in Development Environment 11.8.9</h3>
<ul>
<li>Fixed an issue in Library Modules, which was about showing the references to entities in the dependencies managers that could not be used. (RBIT-26)</li>
<li>Now, the double-click on a Database Entity will open the View Data. (RDEV-2149)</li>
</ul>
<h3 id="bug_fixing_11.8.9">Bug Fixing</h3>
<ul>
<li>In some situations, parameters and structure attributes created during import of SOAP services had incorrect types, leading to publication errors. This has been fixed. (RBIT-25)</li>
<li>Fixed an issue that caused the Create Application Wizard to open in new application mode before changing to edit mode when editing the app's basic info. (RDEV-2135)</li>
<li>Fixed an issue that caused Service Studio to crash while running the tutorial. (RDEV-2117)</li>
<li>Fixed issue when closing new blank eSpace. (RICT-2764)</li>
<li>Fixed crash when dragging Text widget to itself. (RICT-2770)</li>
<li>Fix to "divide by zero exception" in Expression Editor. (RICT-2750)</li>
<li>In some situations, parameters and structure attributes created during import of SOAP services had incorrect types, leading to publication errors. This has been fixed. (RPM-402)</li>
<li>Fixed the "error creating tenant view" database errors when publishing multitenant apps that have local entities. (RTAF-3317)</li>
<li>Fixed bug where Internal and External Users count was considering disabled User Providers. (RIDT-95)</li>
</ul>
<div class="hidden" id="development-environment-11.8.9_end"></div><div class="hidden" id="development-environment-11.8.8_start"></div>

<h2 id="development_environment_11.8.8">Development Environment 11.8.8</h2>
<div class="info">

Released on Sep 23, 2020</div>
<h3 id="new_in_development_environment_11.8.8">New in Development Environment 11.8.8</h3>
<ul>
<li>Fixed an issue in Library Modules, which was about showing the references to entities in the dependencies managers that could not be used. (RBIT-26)</li>
</ul>
<h3 id="bug_fixing_11.8.8">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while running the tutorial. (RDEV-2117)</li>
<li>Fixed an issue that caused the Create Application Wizard to open in new application mode before changing to edit mode when editing the app's basic info. (RDEV-2135)</li>
<li>Fixed issue when closing new blank eSpace. (RICT-2764)</li>
<li>Fixed crash when dragging Text widget to itself. (RICT-2770)</li>
<li>Fix to "divide by zero exception" in Expression Editor. (RICT-2750)</li>
<li>Fixed the "error creating tenant view" database errors when publishing multitenant apps that have local entities. (RTAF-3317)</li>
<li>Fixed bug where Internal and External Users count was considering disabled User Providers. (RIDT-95)</li>
</ul>
<div class="hidden" id="development-environment-11.8.8_end"></div><div class="hidden" id="development-environment-11.8.7_start"></div>

<h2 id="development_environment_11.8.7">Development Environment 11.8.7</h2>
<div class="info">

Released on Sep 07, 2020</div>
<h3 id="new_in_development_environment_11.8.7">New in Development Environment 11.8.7</h3>
<ul>
<li>Now, the title of the Input's Expression editor displays the name of the input being edited. (RDEV-2065)</li>
<li>Increased the maximum number of saved environment credentials from 10 to 50. (RDEV-1974)</li>
<li>Now, while creating an application based on an existing one, these applications can have a Live Preview that can be accessed from Service Studio. (RDEV-1943)</li>
<li>Now, the title of the Assign's Expression editor displays the name of the variable being edited.  Inspired by <a href="https://www.outsystems.com/ideas/1597/add-variable-name-to-assign-window?IsFromAdvancedSearch=True" target="_blank" rel="noopener noreferrer">Wayne Hodgson's idea</a>. (RDEV-1877)</li>
<li>Revamped Icon widget dialog look and feel. (RMAC-2818)</li>
</ul>
<h3 id="bug_fixing_11.8.7">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while running the tutorial. (RDEV-2117)</li>
<li>Fixed a security vulnerability in Service Studio. (RPD-5212)</li>
<li>Fixed an issue that caused some variable names to result in wrongly guessed data types by Service Studio. (RDEV-2034)</li>
<li>Fixed crash when consuming extensive swagger file that caused Service Studio to close unexpectedly. (RSBO-1529)</li>
<li>Fix error installing applications when database catalog configurations are required. (RPST-903)</li>
</ul>
<div class="hidden" id="development-environment-11.8.7_end"></div><div class="hidden" id="development-environment-11.8.6_start"></div>

<h2 id="development_environment_11.8.6">Development Environment 11.8.6</h2>
<div class="info">

Released on Aug 24, 2020</div>
<h3 id="new_in_development_environment_11.8.6">New in Development Environment 11.8.6</h3>
<ul>
<li>We updated the user interface of the dropdown list that shows the AI suggestions. (RAID-670)</li>
<li>Now, while creating an application based on an existing one, these applications can have a Live Preview that can be accessed from Service Studio. (RDEV-1943)</li>
<li>In Personal Environments, you now get a guided tour when you create your first app from an existing app. (RDEV-1788)</li>
</ul>
<h3 id="bug_fixing_11.8.6">Bug Fixing</h3>
<ul>
<li>Fixed an issue with the AI-Assisted Development's Actions suggestions that improves arguments auto filling. (RAID-699)</li>
<li>Fixed a security vulnerability in Service Studio. (RPD-5212)</li>
<li>Fixed an issue in the 5 min tutorial that caused the arrow to disappear after creating a task detail screen. (RDEV-1868)</li>
<li>Fixed crash when consuming extensive swagger file that caused Service Studio to close unexpectedly. (RSBO-1529)</li>
<li>Fixed "Cannot read property 'setAttribute' of undefined" error when creating nested tables with Table Records widget in Reactive Web App. (RTAF-2995)</li>
<li>Fixed Expressions linked to the show-default-value attribute in Input widgets to reevaluate correctly after change. (RPD-4850)</li>
<li>Fix error installing applications when database catalog configurations are required. (RPST-903)</li>
</ul>
<div class="hidden" id="development-environment-11.8.6_end"></div><div class="hidden" id="development-environment-11.8.4_start"></div>

<h2 id="development_environment_11.8.4">Development Environment 11.8.4</h2>
<div class="info">

Released on Aug 10, 2020</div>
<h3 id="new_in_development_environment_11.8.4">New in Development Environment 11.8.4</h3>
<ul>
<li>We updated the user interface of the dropdown list that shows the AI suggestions. (RAID-670)</li>
<li>Removed the spell checker for a new module's name. (RDEV-1929)</li>
<li>Converting a variable from a Record Data Type is now also available for List of Record variable Types.  (RDEV-1923)</li>
<li>Now, the title of the Assign's Expression editor displays the name of the variable being edited.  Inspired by <a href="https://www.outsystems.com/ideas/1597/add-variable-name-to-assign-window?IsFromAdvancedSearch=True" target="_blank" rel="noopener noreferrer">Wayne Hodgson's idea</a>. (RDEV-1877)</li>
<li>Now, when opening a module in Service Studio, the Preview mode is turned off by default. Inspired by <a href="https://www.outsystems.com/ideas/7948/reset-preview-option-when-closes-the-module-and-or-service-studio" target="_blank" rel="noopener noreferrer">Otavio Souza's idea</a> (RDEV-1876)</li>
<li>Now, the Widget Tree doesn't clip the name of elements when there isn't enough space to show the full name. Inspired by <a href="https://www.outsystems.com/ideas/8993/widget-tree-dont-cut-off-names-when-theres-enough-room" target="_blank" rel="noopener noreferrer">Kilian Hekhuis' idea</a>. (RDEV-1875)</li>
<li>Now, copy pasting an element in the tree, such as a user action, will open the duplicated element. Inspired by <a href="https://www.outsystems.com/ideas/517/when-copying-an-user-action-be-redirected-to-the-new-created-action" target="_blank" rel="noopener noreferrer"> Diogo Cordeiro's idea. </a>
(RDEV-1878)</li>
</ul>
<h3 id="bug_fixing_11.8.4">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while clicking in Manage Environments without being connected to an environment. (RDEV-1925)</li>
<li>Fixed an issue that prevented Manage Dependencies from focusing on one of the search boxes after opening. (RDEV-1922)</li>
</ul>
<div class="hidden" id="development-environment-11.8.4_end"></div><div class="hidden" id="development-environment-11.8.3_start"></div>

<h2 id="development_environment_11.8.3">Development Environment 11.8.3</h2>
<div class="info">Released on Aug 03, 2020</div>
<h3 id="bug_fixing_11.8.3">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the Give Us Feedback to lose the outer spacing.  (RDEV-1899)</li>
</ul>
<div class="hidden" id="development-environment-11.8.3_end"></div><div class="hidden" id="development-environment-11.8.2_start"></div>

<h2 id="development_environment_11.8.2">Development Environment 11.8.2</h2>
<div class="info">

Released on Jul 27, 2020</div>
<h3 id="new_in_development_environment_11.8.2">New in Development Environment 11.8.2</h3>
<ul>
<li>You can now use the Create Structure from Type to generate a structure from an anonymous structure type that will be used in the original variable. 
Inspired by <a href="https://www.outsystems.com/ideas/6044/" target="_blank" rel="noopener noreferrer">Maycon Oleczinski's idea</a>. (RDEV-1532)</li>
</ul>
<h3 id="bug_fixing_11.8.2">Bug Fixing</h3>
<ul>
<li>Fix issue that would lead to an exception while merging widgets (RAOT-125)</li>
<li>Fixed the debugger when working with Client Variables in Assigns. The bug interrupted the debugging and caused a communication error with the message "There's a case missing in this switch". (RPD-5060)</li>
<li>Fixed library modules invalid (system) database entity referencing (RSBO-892). (RSBO-892)</li>
<li>Fixed an issue that caused Service Studio to crash while adding a dependency. (RDEV-1866)</li>
<li>Fixed an issue that caused Service Studio to crash while executing an action from TrueChange messages. (RDEV-1857)</li>
<li>Fixed an issue that caused Service Studio to crash while getting documentation links. (RDEV-1858)</li>
<li>Fixed an issue that caused SS to crash while validating the cache. (RDEV-1860)</li>
<li>Fixed an issue that caused Service Studio to crash while editing multiple objects at the same time. (RDEV-1864)</li>
<li>Fixed an issue that caused Service Studio to crash while checking references compatibility. (RDEV-1865)</li>
<li>Fixed an issue that caused Service Studio to crash while setting the dialog position. (RDEV-1885)</li>
<li>Fixed an issue that caused Service Studio to crash when dropping items in the Menu container.  (RDEV-1883)</li>
<li>Fixed an issue that caused Service Studio to crash while calculating references compatibility. (RDEV-1884)</li>
<li>Fixed an issue that caused Service Studio to crash while fixing the quotation in expressions. (RDEV-1886)</li>
<li>Fixed an issue that caused Service Studio to crash while verifying the module cache. (RDEV-1887)</li>
<li>Fixed an issue that caused Service Studio to crash while positioning the tutorial help window. (RDEV-1888)</li>
<li>Fixed an issue that caused Service Studio to crash while adding a filter to an aggregate.  (RDEV-1893)</li>
<li>Fix issue when closing expression editor that would try to change a non editable property (RAOT-135)</li>
<li>Fixed issue that would lead to a crash while merging group by attributes in aggregate nodes (RAOT-131)</li>
<li>Fixed an issue that caused Serice Studio to crash while changing a node's description. (RDEV-1871)</li>
<li>Fixed a crash in Service Studio when refreshing screen templates. (RTAF-3107)</li>
</ul>
<div class="hidden" id="development-environment-11.8.2_end"></div><div class="hidden" id="development-environment-11.8.1_start"></div>

<h2 id="development_environment_11.8.1">Development Environment 11.8.1</h2>
<div class="info">

Released on Jul 20, 2020</div>
<h3 id="new_in_development_environment_11.8.1">New in Development Environment 11.8.1</h3>
<ul>
<li>Improved the way Service Studio guesses the type of new variables based on their names. Inspired by <a href="https://www.outsystems.com/ideas/3479/" target="_blank" rel="noopener noreferrer">Frans Moquette's idea</a>. (RDEV-1531)</li>
</ul>
<h3 id="bug_fixing_11.8.1">Bug Fixing</h3>
<ul>
<li>Fixed a bug that allows users to be created with a repeated username when using the User_CreateOrUpdate API (RLIT-3711)</li>
</ul>
<div class="hidden" id="development-environment-11.8.1_end"></div><div class="hidden" id="development-environment-11.7.15_start"></div>

<h2 id="development_environment_11.7.15">Development Environment 11.7.15</h2>
<div class="info">

Released on Jul 13, 2020</div>
<h3 id="new_in_development_environment_11.7.15">New in Development Environment 11.7.15</h3>
<ul>
<li>Fixed issue that would lead to an error message in bottom pane related with 1CP (RAOT-111)</li>
</ul>
<h3 id="bug_fixing_11.7.15">Bug Fixing</h3>
<ul>
<li>Fixed a solution publish error that occurred when compiling outdated dependencies to a structure having new attributes with complex data types. (RSBO-1521)</li>
</ul>
<div class="hidden" id="development-environment-11.7.15_end"></div><div class="hidden" id="development-environment-11.7.14_start"></div>

<h2 id="development_environment_11.7.14">Development Environment 11.7.14</h2>
<div class="info">

Released on Jul 06, 2020</div>
<h3 id="new_in_development_environment_11.7.14">New in Development Environment 11.7.14</h3>
<ul>
<li>In Personal Environments, you can now create a new app based on an existing app curated by OutSystems. (RDEV-1652)</li>
</ul>
<div class="hidden" id="development-environment-11.7.14_end"></div><div class="hidden" id="development-environment-11.7.13_start"></div>

<h2 id="development_environment_11.7.13">Development Environment 11.7.13</h2>
<div class="info">

Released on Jun 29, 2020</div>
<h3 id="bug_fixing_11.7.13">Bug Fixing</h3>
<ul>
<li>Fixed a runtime error in generated Android apps when a new version of the app was available. (RPD-5137)</li>
<li>Fix bug when synchronizing tabs during the merge of aggregates (RMAC-3014)</li>
</ul>
<div class="hidden" id="development-environment-11.7.13_end"></div><div class="hidden" id="development-environment-11.7.12_start"></div>

<h2 id="development_environment_11.7.12">Development Environment 11.7.12</h2>
<div class="info">

Released on Jun 22, 2020</div>
<h3 id="new_in_development_environment_11.7.12">New in Development Environment 11.7.12</h3>
<ul>
<li>Avoid doing unnecessary requests when native tab of Application details is not opened (RMAC-2953)</li>
</ul>
<h3 id="bug_fixing_11.7.12">Bug Fixing</h3>
<ul>
<li>Fixed solution publish error when compiling dependencies (not refreshed) to a structure that has new attributes with complex types (RSBO-1521)</li>
<li>We fixed a glitch in the launch of the debugger from Reactive Apps. The Chrome window for debugging now opens in a desktop mode, without resizing to the mobile form factor. (RTAF-2996)</li>
<li>Fix error when deleting object with editor dialog open (RMAC-2822)</li>
<li>We fixed a publishing error by improving the scope of widgets inside Placeholders. You still can reference, from widgets inside Placeholders, the elements that are in Blocks/Screens. However, you can't, from Blocks/Screens/Client Actions, reference the elements that are inside Placeholders. The invalid referencing broke the publishing step and caused a generic "object not found" error. (RTAF-2889)</li>
</ul>
<div class="hidden" id="development-environment-11.7.12_end"></div><div class="hidden" id="development-environment-11.7.10_start"></div>

<h2 id="development_environment_11.7.10">Development Environment 11.7.10</h2>
<div class="info">

Released on Jun 15, 2020</div>
<h3 id="new_in_development_environment_11.7.10">New in Development Environment 11.7.10</h3>
<ul>
<li>Upgraded Microsoft.AspNetCore and Microsoft.Extension libraries to the latest 2.1 LTS versions. (RRCT-2896)</li>
</ul>
<h3 id="bug_fixing_11.7.10">Bug Fixing</h3>
<ul>
<li>Fixed a bug in Open API 3.0 import, that caused some types defined inside oneOf constructs to not be created. (RSBO-1462)</li>
<li>Fixed an issue that caused Service Studio to crash while logging in the environment for publishing. (RDEV-1707)</li>
<li>Fixed an issue that causes poor visibility because of windows overlapping during the mobile tutorial. (RDEV-1551)</li>
<li>Fixed an issue that caused Service Studio verify errors when renaming used images in Theme Editor. (RDEV-1602)</li>
<li>Fixed an issue that causes Service Studio to be unable to connect to enterprise cloud environments.  (RDEV-1708)</li>
<li>Fix error blocking the user in a merge operation (RMAC-2912)</li>
<li>Fixed the data replacement crash when Entity that was supposed to be replaced had been deleted. (RTAF-2968)</li>
</ul>
<div class="hidden" id="development-environment-11.7.10_end"></div><div class="hidden" id="development-environment-11.7.9_start"></div>

<h2 id="development_environment_11.7.9">Development Environment 11.7.9</h2>
<div class="info">

Released on Jun 01, 2020</div>
<h3 id="new_in_development_environment_11.7.9">New in Development Environment 11.7.9</h3>
<ul>
<li>It's now possible to consume a REST API importing a REST API specification with lists of parameters that are applicable for all the operations described under a given path. (RSBO-1175)</li>
<li>It's now possible to consume a REST API importing a REST API specification that contains the "allOf" keyword. (RSBO-1176)</li>
<li>It's now possible to consume a REST API importing a REST API specification with enums defined in non-body parameters. (RSBO-1177)</li>
<li>It's now possible to consume a REST API specification that includes an array of servers, allowing the user to specify which one to use. (RSBO-1179)</li>
<li>It's now possible to consume a REST API importing a REST API specification with remote URL references. (RSBO-1205)</li>
<li>It's now possible to consume a REST API importing a REST API specification that contains the "oneOf" keyword. (RSBO-1268)</li>
</ul>
<h3 id="bug_fixing_11.7.9">Bug Fixing</h3>
<ul>
<li>Fixed "ID" attribute from being placed on the container element instead of element the select on Dropdown widget. (RPD-5019)</li>
<li>Dropdown with custom property selected now automatically scrolls into selected item (RPD-3459)</li>
</ul>
<div class="hidden" id="development-environment-11.7.9_end"></div><div class="hidden" id="development-environment-11.7.8_start"></div>

<h2 id="development_environment_11.7.8">Development Environment 11.7.8</h2>
<div class="info">

Released on May 25, 2020</div>
<h3 id="bug_fixing_11.7.8">Bug Fixing</h3>
<ul>
<li>We fixed an occasional glitch in the UI part of AI-assisted development related to the navigation of the suggestions.  (RAID-565)</li>
<li>Fixed an issue that caused Service Studio to crash when using the arrows keys to navigate around an empty Text Widget. (RTAF-2890)</li>
<li>It is now possible to use screen scaffolding for extension entities (RTAF-2532)</li>
<li>Fixed an issue that caused Service Studio to crash while deleting an empty Text Widget using the Backspace key. (RTAF-2882)</li>
<li>Fixed a crash when selecting the entire content of a Text Widget and then dragging it next to itself. (RTAF-2903)</li>
</ul>
<div class="hidden" id="development-environment-11.7.8_end"></div><div class="hidden" id="development-environment-11.7.7_start"></div>

<h2 id="development_environment_11.7.7">Development Environment 11.7.7</h2>
<div class="info">

Released on May 18, 2020</div>
<h3 id="new_in_development_environment_11.7.7">New in Development Environment 11.7.7</h3>
<ul>
<li>When consuming REST with external refs, a new message was added a message to show the external references that will be downloaded. (RSBO-1293)</li>
<li>We updated the preview of the empty Screen in the list of Screen Templates for Reactive Web  and Mobile Apps. (RTAF-2683)</li>
</ul>
<h3 id="bug_fixing_11.7.7">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the re-render of list widgets to render the transient state of an item in the wrong item when the item position changed. (RPD-3585)</li>
<li>Fixed scaffolding of the details Screen. The related Entity now filters the records list in Aggregate by the identifier. (RTAF-2529)</li>
<li>Fixed debugging mobile apps on an Android device. The bug was caused by issues in a version of the ADB driver. (RTAF-2592)</li>
<li>Fixed a crash of the IDE when deleting a widget. This was caused by a glitch in the widget preview. (RTAF-2628)</li>
<li>Fixed a bug that caused the import of SOAP Web Services to fail if the WSDL definition contained HTTP bindings. (RPD-4860)</li>
</ul>
<div class="hidden" id="development-environment-11.7.7_end"></div><div class="hidden" id="development-environment-11.7.6_start"></div>

<h2 id="development_environment_11.7.6">Development Environment 11.7.6</h2>
<div class="info">

Released on May 11, 2020</div>
<h3 id="new_in_development_environment_11.7.6">New in Development Environment 11.7.6</h3>
<ul>
<li>Fixed a problem with Service Studio that would result in public processes in a module being incorrectly exposed to other modules. (RICT-2463)</li>
<li>It is now possible to check the publish status through a visual cue in the module tab. 
inspired by <a href="https://www.outsystems.com/ideas/2466/" target="_blank" rel="noopener noreferrer">João Martins' idea</a>. (RDEV-1529)</li>
<li>It's now possible to quickly identify disabled elements in your search results through their greyed out icon. (RDEV-1530)</li>
<li>We updated the preview of the empty Screen in the list of Screen Templates for Reactive Web  and Mobile Apps. (RTAF-2683)</li>
</ul>
<h>Bug Fixing
<ul>
<li>Fixed an issue that caused the re-render of list widgets to render the transient state of an item in the wrong item when the item position changed. (RPD-3585)</li>
<li>Fixed a crash of the IDE when deleting a widget. This was caused by a glitch in the widget preview. (RTAF-2628)</li>
<li>Fixed scaffolding of the details Screen. The related Entity now filters the records list in Aggregate by the identifier. (RTAF-2529)</li>
<li>Fixed debugging mobile apps on an Android device. The bug was caused by issues in a version of the ADB driver. (RTAF-2592)</li>
<li>Fixed a bug that caused the import of SOAP Web Services to fail if the WSDL definition contained HTTP bindings. (RPD-4860)</li>
</ul>
</h><div class="hidden" id="development-environment-11.7.6_end"></div><div class="hidden" id="development-environment-11.7.4_start"></div>

<h2 id="development_environment_11.7.4">Development Environment 11.7.4</h2>
<div class="info">

Released on Apr 27, 2020</div>
<h3 id="new_in_development_environment_11.7.4">New in Development Environment 11.7.4</h3>
<ul>
<li>Fixed a problem with Service Studio that would result in public processes in a module being incorrectly exposed to other modules. (RICT-2463)</li>
<li>It's now possible to quickly identify disabled elements in your search results through their greyed out icon. (RDEV-1530)</li>
<li>It is now possible to check the publish status through a visual cue in the module tab. 
inspired by <a href="https://www.outsystems.com/ideas/2466/" target="_blank" rel="noopener noreferrer">João Martins' idea</a>. (RDEV-1529)</li>
</ul>
<h3 id="bug_fixing_11.7.4">Bug Fixing</h3>
<ul>
<li>Fixed and improved the AI-assisted suggestions with the boolean values in If nodes. (RAID-548)</li>
<li>Fixed crash when having enums in Swagger files with empty values. (RSBO-1352)</li>
<li>We fixed the names of the Screens and labels of the menus that get created when you drag Entity to a flow. If you have the Task Entity, for example, the menus that are created after the scaffolding are Tasks and Task Detail, and not Task List and Task Detail. (RTAF-2530)</li>
<li>Fixed a crash of the IDE when deleting a widget. This was caused by a glitch in the widget preview. (RTAF-2628)</li>
</ul>
<div class="hidden" id="development-environment-11.7.4_end"></div><div class="hidden" id="development-environment-11.7.3_start"></div>

<h2 id="development_environment_11.7.3">Development Environment 11.7.3</h2>
<div class="info">

Released on Apr 20, 2020</div>
<h3 id="new_in_development_environment_11.7.3">New in Development Environment 11.7.3</h3>
<ul>
<li>When copying a structure or entity, now you'll be able to paste it as an action’s input, output, or local parameter just by selecting Paste as. Inspired by <a href="https://www.outsystems.com/ideas/5845/" target="_blank" rel="noopener noreferrer">Evert van der Zalm's idea</a>. (RDEV-1526)</li>
</ul>
<h3 id="bug_fixing_11.7.3">Bug Fixing</h3>
<ul>
<li>Fixed and improved the AI-assisted suggestions with the boolean values in If nodes. (RAID-548)</li>
<li>Fixed and improved the AI-assisted suggestions for Aggregates in scenarios that require filtering by ID. (RAID-549)</li>
<li>Fixed an issue that caused a reference always being needed to be refreshed in Manage Dependencies. (RICT-2420)</li>
<li>Fixed crash when having enums in Swagger files with empty values (RSBO-1352)</li>
<li>We fixed the names of the Screens and labels of the menus that get created when you drag Entity to a flow. If you have the Task Entity, for example, the menus that are created after the scaffolding are Tasks and Task Detail, and not Task List and Task Detail. (RTAF-2530)</li>
<li>Fixed Service Studio crash when moving a Screen/Block between Flows. (RTAF-2541)</li>
<li>Fixed a Service Studio crash when publishing or saving a module with a private Block that is used by a referenced public Theme. The bug prevented proper calculation and handling of the references between the Theme and the Block. (RTAF-2552)</li>
</ul>
<div class="hidden" id="development-environment-11.7.3_end"></div><div class="hidden" id="development-environment-11.7.2_start"></div>

<h2 id="development_environment_11.7.2">Development Environment 11.7.2</h2>
<div class="info">

Released on Apr 13, 2020
</div>
<h3 id="new_in_development_environment_11.7.2">New in Development Environment 11.7.2</h3>
<ul>
<li>When copying a structure or entity, now you'll be able to paste it as an action’s input, output, or local parameter just by selecting Paste as. Inspired by <a href="https://www.outsystems.com/ideas/5845/" target="_blank" rel="noopener noreferrer">Evert van der Zalm's idea</a>. (RDEV-1526)</li>
<li>Now you can use Radio Button Widget in your Reactive Web and Mobile apps. To build and deploy an app with this widget in UI, you also need Platform Server that supports Radio Button and updated OutSystems UI. (RTAF-2144)</li>
<li>Now you can use Human Activity Destination property in Reactive Web Apps. (RTAF-2197)</li>
</ul>
<h3 id="bug_fixing_11.7.2">Bug Fixing</h3>
<ul>
<li>Fixed and improved the AI-assisted suggestions for Aggregates in scenarios that require filtering by ID. (RAID-549)</li>
<li>Fixed and improved the AI-assisted suggestions with the boolean values in If nodes. (RAID-548)</li>
<li>Fixed an issue that caused a reference always being needed to be refreshed in Manage Dependencies. (RICT-2420)</li>
</ul>
<div class="hidden" id="development-environment-11.7.2_end"></div><div class="hidden" id="development-environment-11.7.1_start"></div>

<h2 id="development_environment_11.7.1">Development Environment 11.7.1</h2>
<div class="info">

Released on Apr 06, 2020</div>
<h3 id="new_in_development_environment_11.7.1">New in Development Environment 11.7.1</h3>
<ul>
<li>We added a tooltip to the AI-assisted development radar that shows in the flow. Now it's more clear what the radar does. (RAID-525)</li>
<li>It is now possible to double-click the condition arrow to access both its conditions.
Inspired by <a href="https://www.outsystems.com/ideas/3128/" target="_blank" rel="noopener noreferrer">Menno Hoogsteen's idea</a>. (RDEV-1252)</li>
<li>It is now possible to go directly to a widget in the Widget Tree by right-clicking it and selecting the See in Widget Tree option. Inspired by <a href="https://www.outsystems.com/ideas/6288/" target="_blank" rel="noopener noreferrer">Robert B's idea</a>.
(RDEV-1253)</li>
<li>It is now possible to clear the text filtering of the applications in the Application List. 
Inspired by <a href="https://www.outsystems.com/ideas/7845/" target="_blank" rel="noopener noreferrer">Daniël Kuhlmann's idea</a>. (RDEV-1274)</li>
<li>You’ll now be able to track the number of conflicts that are left to solve when facing conflicting module versions in Service Studio publish process! Additionally, we’ve increased the overall experience of the process, giving the option to ignore all conflicts and accept the local version right away. (RMAC-1400)</li>
<li>Now you can use the Table widget in your Mobile applications. Fetch data to your Screen, drop Table to the Screen and select the data in the Source property. Then, drop Attributes to the Table. Add sorting by creating a new OnSort Action that triggers an accelerator with the logic. (RTAFB-2155)</li>
<li>Screen Events in Mobile App are now in a drop-down list box, just like in Reactive Web App. This UI tweak makes your developing experience more consistent. (RTAFB-2491)</li>
</ul>
<h3 id="bug_fixing_11.7.1">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while deleting text in an expression. (RDEV-1466)</li>
<li>Fixed broken icons on some editors (RICT-2405)</li>
<li>Fixed an issue that caused an error when referencing a web block.  (RICT-2417)</li>
<li>Fixed issue where copying entity attributes from an Extension was also copying the Original Name and Type properties, resulting in runtime errors. (RPD-3815)</li>
<li>Fixed a problem where navigation from the OnAfterFetch event handler rendered the current Screen instead of the destination Screen. (RTAFB-2472)</li>
<li>Fixed a crash after drop an entity over a dropdown. (RUDOF-928)</li>
</ul>
<div class="hidden" id="development-environment-11.7.1_end"></div><div class="hidden" id="development-environment-11.6.32_start"></div>

<h2 id="development_environment_11.6.32">Development Environment 11.6.32</h2>
<div class="info">

Released on Mar 23, 2020</div>
<h3 id="new_in_development_environment_11.6.32">New in Development Environment 11.6.32</h3>
<ul>
<li>The AI-assisted development feature will now also consider Service Actions with Boolean outputs in advanced IF suggestions (RAID-473)</li>
<li>We tweaked the AI-assisted development feature so it does a better job automatically filling actions' arguments (RAID-520)</li>
<li>It is now possible to clear the text filtering of the applications in the Application List. 
Inspired by <a href="https://www.outsystems.com/ideas/7845/" target="_blank" rel="noopener noreferrer">Daniël Kuhlmann's idea</a>. (RDEV-1274)</li>
</ul>
<h3 id="bug_fixing_11.6.32">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while deleting text in an expression. (RDEV-1466)</li>
<li>Fixed an issue that caused the corruption of one of the Login Screen background images available in Theme Editor. (RDEV-1444)</li>
<li>Fixed a typo in 5-min tutorial. (RDEV-1442)</li>
<li>Fixed a compilation error related to the OnAfterFetch Event. The OnAfterFetch Event was incorrectly letting block Events to be set as its handlers, which caused a compilation error. (RTAF-2450)</li>
<li>We fixed the Screen Template list from loading indefinitely when the list contained a template with a missing field. (RTAF-2451)</li>
<li>Fixed an issue where list iterations on functions raised an error when the function was called from an Expression in a widget. (RPD-3756)</li>
<li>Fixed broken icons on some editors (RICT-2405)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 9.6 (Critical). (RPC-988)</li>
</ul>
<div class="hidden" id="development-environment-11.6.32_end"></div><div class="hidden" id="development-environment-11.6.31_start"></div>

<h2 id="development_environment_11.6.31">Development Environment 11.6.31</h2>
<div class="info">

Released on Mar 17, 2020</div>
<h3 id="new_in_development_environment_11.6.31">New in Development Environment 11.6.31</h3>
<ul>
<li>We improved the user experience of the AI-assisted development feature. Now the suggestions show less often when you're just connecting two nodes. (RAID-343)</li>
<li>Now the AI-assisted development feature is better at recommending the right side of assignments because the suggestion algorithm uses the names available in the scope. (RAID-463)</li>
</ul>
<h3 id="bug_fixing_11.6.31">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the corruption of one of the Login Screen background images available in Theme Editor. (RDEV-1444)</li>
<li>Fixed a typo in 5-min tutorial. (RDEV-1442)</li>
<li>Fixed an issue that caused Service Studio to crash when importing a Resource as Image.  (RDEV-1415)</li>
<li>Fixed a compilation error related to the OnAfterFetch Event. The OnAfterFetch Event was incorrectly letting block Events to be set as its handlers, which caused a compilation error. (RTAF-2450)</li>
<li>We fixed the Screen Template list from loading indefinitely when the list contained a template with a missing field. (RTAF-2451)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 9.6 (Critical). (RPC-988) (RPC-988)</li>
</ul>
<div class="hidden" id="development-environment-11.6.31_end"></div><div class="hidden" id="development-environment-11.6.30_start"></div>

<h2 id="development_environment_11.6.30">Development Environment 11.6.30</h2>
<div class="info">

Released on Mar 09, 2020</div>
<h3 id="new_in_development_environment_11.6.30">New in Development Environment 11.6.30</h3>
<ul>
<li>Now the AI-assisted development feature is better at recommending the right side of assignments because the suggestion algorithm uses the names available in the scope. (RAID-463)</li>
<li>Now you can enter only text when providing feedback, as selecting a smiley is optional in the "Give us feedback" window. (RDEV-1408)</li>
</ul>
<h3 id="bug_fixing_11.6.30">Bug Fixing</h3>
<ul>
<li>Fixed a compilation error when importing SOAP Web Services containing choices with repeated element names and complex types defined inline. (RSBO-1117)</li>
</ul>
<div class="hidden" id="development-environment-11.6.30_end"></div><div class="hidden" id="development-environment-11.6.29_start"></div>

<h2 id="development_environment_11.6.29">Development Environment 11.6.29</h2>
<div class="info">

Released on Mar 02, 2020
</div>
<h3 id="new_in_development_environment_11.6.29">New in Development Environment 11.6.29</h3>
<ul>
<li>The built-in Service Studio tutorial (Help &gt; Build an App in 5 min) now shows how to use the <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Implement_Application_Logic/AI-assisted_development" target="_blank" rel="noopener noreferrer">suggestions by the AI-assisted development feature</a>. (RAID-484)</li>
<li>Forge accesses from within Service Studio are authenticated automatically for users connected to their Personal Environments. This will not work if the user's environment credentials are different from the ones they use to access the community site. Inspired b <a href="https://www.outsystems.com/ideas/5611/" target="_blank" rel="noopener noreferrer">Jitendra Yadav's idea</a>. (RDEV-1347)</li>
<li>We improved the Data Replacement feature. You can now drag local Entities to Flows to scaffold Screens in Mobile Apps. Also, dragging a different Entity to an existing List, Table or Form Widget now produces better results, with less TrueChange errors. (RTAF-1991)</li>
</ul>
<h3 id="bug_fixing_11.6.29">Bug Fixing</h3>
<ul>
<li>Solved an issue that prevented "remember me" Forge login option from working after restarting Service Studio. (RDEV-1360)</li>
<li>We fix an issue that occurs when someone tries to import a swagger 2.0 definition from a local file and without the schema property defined (RSBO-1180)</li>
</ul>
<div class="hidden" id="development-environment-11.6.29_end"></div><div class="hidden" id="development-environment-11.6.27_start"></div>

<h2 id="development_environment_11.6.27">Development Environment 11.6.27</h2>
<div class="info">

Released on Feb 26, 2020</div>
<h3 id="bug_fixing_11.6.27">Bug Fixing</h3>
<ul>
<li>Fixed a crash when right-clicking the AI-assisted development radar in the flow while holding a shortcut key. (RAID-470)</li>
<li>Fixed an issue that caused a crash while changing the color of an application whose Home module has a Default Theme that is a dependency. (RDEV-1337)</li>
<li>Fixed internal logging to always include information that is sent to EventViewer to improve troubleshooting. (RPC-952)</li>
<li>Fixed a crash when scaffolding a Screen on a Web Flow from a weak Entity (Entity with the identifier pointing to another Entity). (RTAF-2182)</li>
<li>Fixed a crash when trying to scaffold a Table inside another Table. (RTAF-2161)</li>
<li>Fixed an issue in input parameters of Service Actions with Decimal data type when the precision is longer than 14 digits. (RSBO-1194)</li>
<li>Fixed a crash when reordering sorted attributes in Aggregates with Group By's. (RSBO-1041)</li>
</ul>
<div class="hidden" id="development-environment-11.6.27_end"></div><div class="hidden" id="development-environment-11.6.26_start"></div>

<h2 id="development_environment_11.6.26">Development Environment 11.6.26</h2>
<div class="info">

Released on Feb 10, 2020</div>
<h3 id="bug_fixing_11.6.26">Bug Fixing</h3>
<ul>
<li>Fixed a crash when trying to enclose multiple Placeholders in a Container. (RTAF-2157)</li>
</ul>
<div class="hidden" id="development-environment-11.6.26_end"></div><div class="hidden" id="development-environment-11.6.25_start"></div>

<h2 id="development_environment_11.6.25">Development Environment 11.6.25</h2>
<div class="info">

Released on Feb 03, 2020</div>
<h3 id="new_in_development_environment_11.6.25">New in Development Environment 11.6.25</h3>
<ul>
<li>It is now possible to see OutSystems supported apps in the Application List. (RDEV-1270)</li>
<li>When consuming empty used structures, will no long view a message box stating OutSystems does not support this properties, instead there will be errors in TrueChange (RSBO-1202)</li>
</ul>
<h3 id="bug_fixing_11.6.25">Bug Fixing</h3>
<ul>
<li>Fixed the crash caused by special characters in the search field of the widgets icon picker window. (RTAF-2088)</li>
<li>Fixed multiple executions of Screen Preparation Action that occurred when Rich Widgets File Upload was used in the Screen. (RTAF-2064)</li>
<li>Fixed an error that showed when using the Rich Widgets Pop-Up pattern with the List Bulk Select widget, where a link/button triggered a pop-up and had the link/button associated with the List Bulk Select widget. (RTAF-2062)</li>
<li>Fixed a crash in Service Studio that occurred occasionally when creating attributes in Structures from REST services. (RSBO-1199)</li>
</ul>
<div class="hidden" id="development-environment-11.6.25_end"></div><div class="hidden" id="development-environment-11.6.24_start"></div>

<h2 id="development_environment_11.6.24">Development Environment 11.6.24</h2>
<div class="info">

Released on Jan 27, 2020</div>
<h3 id="bug_fixing_11.6.24">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the creation of duplicated Static Entities when used more than once in a consumed REST API definition. (RSBO-853)</li>
<li>Fixed OML corruption triggered by the removing a Structure used in a SQL node that is source to a ListBox or ComboBox widget (RSBO-865)</li>
<li>Now it's no longer possible to drop a Table Widget into smaller widgets such as ButtonGroup. (RTAF-2030)</li>
</ul>
<div class="hidden" id="development-environment-11.6.24_end"></div><div class="hidden" id="development-environment-11.6.23_start"></div>

<h2 id="development_environment_11.6.23">Development Environment 11.6.23</h2>
<div class="info">

Released on Jan 20, 2020</div>
<h3 id="new_in_development_environment_11.6.23">New in Development Environment 11.6.23</h3>
<ul>
<li>We improved the alignment of the cell content and the header of the Table Widget that you get after you drag an Entity to a Screen. (RTAF-1787)</li>
</ul>
<h3 id="bug_fixing_11.6.23">Bug Fixing</h3>
<ul>
<li>Fixed a typo on the Is Form Default warning message. (RTAF-2019)</li>
<li>Now a True Change error tells you if there's an invalid sort expression in Reactive Table. Previously such an invalid expression broke the publishing step. (RTAF-1981)</li>
<li>Fixed an issue on Input widget for DateTime type preventing from submiting valid DateTimes on iOS. (RPD-2841)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 9.8 (Critical). (RPD-4636)</li>
</ul>
<div class="hidden" id="development-environment-11.6.23_end"></div><div class="hidden" id="development-environment-11.6.22_start"></div>

<h2 id="development_environment_11.6.22">Development Environment 11.6.22</h2>
<div class="info">

Released on Jan 13, 2020</div>
<h3 id="bug_fixing_11.6.22">Bug Fixing</h3>
<ul>
<li>When you now drop an Entity to a Flow, a link is created in the menu. (RTAF-1937)</li>
</ul>
<div class="hidden" id="development-environment-11.6.22_end"></div><div class="hidden" id="development-environment-11.6.21_start"></div>

<h2 id="development_environment_11.6.21">Development Environment 11.6.21</h2>
<div class="info">

Released on Jan 06, 2020</div>
<h3 id="new_in_development_environment_11.6.21">New in Development Environment 11.6.21</h3>
<ul>
<li>You can now distribute your app as a Progressive Web App (PWA). Start by enabling this early access feature in LifeTime. Then, create a mobile or tablet app, publish it, navigate to the "Distribute" tab and toggle on "Distribute as the PWA" (no republish needed). You can try your PWA out by installing it through Android Chrome and iOS Safari. The <a href="https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Distribute_as_a_progressive_web_app" target="_blank" rel="noopener noreferrer">early access PWA documentation</a> explains how to enable PWA on iOS 13, as well as how to edit the manifest. Try out the PWAs and <a href="https://www.outsystems.com/forums/71/early-access-features/" target="_blank" rel="noopener noreferrer">share your feedback with us</a> on the forum! (RTAF-1939)</li>
</ul>
<h3 id="bug_fixing_11.6.21">Bug Fixing</h3>
<ul>
<li>Fixed an issue with the maximum message size quota that prevented Service Studio from opening some applications correctly. (RPD-4679)</li>
<li>Fixed a security vulnerability. CVSSv3.0 score 9.8 (Critical). (RPD-4618)</li>
</ul>
<div class="hidden" id="development-environment-11.6.21_end"></div><div class="hidden" id="development-environment-11.6.18_start"></div>

<h2 id="development_environment_11.6.18">Development Environment 11.6.18</h2>
<div class="info">

Released on Dec 30, 2019</div>
<h3 id="new_in_development_environment_11.6.18">New in Development Environment 11.6.18</h3>
<ul>
<li>Improved the look of dark themes generated by Theme Editor. (RDEV-1193)</li>
</ul>
<h3 id="bug_fixing_11.6.18">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused to Application Creation Wizard to appear without images. (RTAF-1906)</li>
<li>Now dragging an identifier Attribute from a Data Action Structure to a Table Widget works correctly and creates a column. Previously the widget ignored this type of identifier. (RTAF-1790)</li>
<li>Fixed crash that occurred when scaffolding an entity without a plural name (RTAF-1950)</li>
<li>Fixed an issue that caused Service Studio to hang when trying to type ':root' selector in CSS Editor. (RDEV-1210)</li>
<li>Now it's possible to consume a REST API importing a swagger file with methods whose response doesn't include a schema. (RSBO-1138)</li>
<li>Now it's possible to consume a REST API importing a swagger file with methods with large descriptions.  (RSBO-1139)</li>
<li>Added support for headers in consumed SOAP Web Services. (RSBO-1040)</li>
</ul>
<div class="hidden" id="development-environment-11.6.18_end"></div><div class="hidden" id="development-environment-11.6.17_start"></div>

<h2 id="development_environment_11.6.17">Development Environment 11.6.17</h2>
<div class="info">Released on Dec 20, 2019</div>
<h3 id="new_in_development_environment_11.6.17">New in Development Environment 11.6.17</h3>
<ul>
<li>Redesigned the version conflict dialog to make it more difficult for less experienced users to overwrite changes made by others. (RMAC-48)</li>
<li>It is now possible to report feedback from the "Search in Other Modules" window. (RDEV-820)</li>
<li>Timeouts are now configured via “Short Operations timeout” (open and close connection) and “Long Operations timeout” (send and receive), which are accessible via Preferences Menu → Environment Connection, and not via .bindings files like before. (RICT-2258)</li>
<li>Now you can open and publish modules that are larger than 32 MB. You can't change this setting in the .bindings file anymore. (RICT-2112)</li>
<li>We improved the preview of the Table Widget. The Table now displays more example records and you can hide/show the rows. (RTAF-1789)</li>
</ul>
<h3 id="bug_fixing_11.6.17">Bug Fixing</h3>
<ul>
<li>Fixed a scaffolding bug that crashed Service Studio after dragging an Aggregate without a defined source. (RTAF-1878)</li>
<li>Now dragging an identifier Attribute from a Data Action Structure to a Table Widget works correctly and creates a column. Previously the widget ignored this type of identifier. (RTAF-1790)</li>
<li>Fixed an issue that caused to have duplicated Application templates registered. (RTAF-1847)</li>
<li>Is now possible in SOAP to have a  simpleContent with an extension element inside. (RPD-4624)</li>
<li>Fixed a crash that occurred after opening a context menu when multiple assign nodes are selected. (RUDOF-798)</li>
</ul>
<div class="hidden" id="development-environment-11.6.17_end"></div><div class="hidden" id="development-environment-11.6.16_start"></div>

<h2 id="development_environment_11.6.16">Development Environment 11.6.16</h2>
<div class="info">

Released on Dec 16, 2019</div>
<h3 id="new_in_development_environment_11.6.16">New in Development Environment 11.6.16</h3>
<ul>
<li>It is now possible to scaffold list and detail screens in Reactive Web simply by dragging an entity to a UI flow. (RTAF-1658)</li>
</ul>
<h3 id="bug_fixing_11.6.16">Bug Fixing</h3>
<ul>
<li>Fixed an issue when creating an empty screen the inserted name wasn't taken into consideration. (RTAF-1871)</li>
</ul>
<div class="hidden" id="development-environment-11.6.16_end"></div><div class="hidden" id="development-environment-11.6.14_start"></div>

<h2 id="development_environment_11.6.14">Development Environment 11.6.14</h2>
<div class="info">

Released on Dec 09, 2019</div>
<h3 id="new_in_development_environment_11.6.14">New in Development Environment 11.6.14</h3>
<ul>
<li>It is now possible to open a support case in the Help menu. (RDEV-728)</li>
<li>Data Sources now support dependency chaining. This enables you to create data sequences to form a more complex behavior with efficient asynchronous and parallel database queries. (RTAF-1764)</li>
</ul>
<h3 id="bug_fixing_11.6.14">Bug Fixing</h3>
<ul>
<li>Fixed crash that happened while applying  AI flow assistant suggestions for new connectors. (RAID-384)</li>
<li>Fixed an issue that caused a crash when calculating color suggestions in Theme Editor. (RDEV-1082)</li>
<li>Fixed an issue that caused Service Studio to crash when showing Styles Editor for Placeholder widgets. (RDEV-1065)</li>
<li>Deleting a column in a Table Widget now leaves the next available cell selected, and not the entire table. (RTAF-1788)</li>
</ul>
<div class="hidden" id="development-environment-11.6.14_end"></div><div class="hidden" id="development-environment-11.6.13_start"></div>

<h2 id="development_environment_11.6.13">Development Environment 11.6.13</h2>
<div class="info">

Released on Dec 02, 2019</div>
<h3 id="new_in_development_environment_11.6.13">New in Development Environment 11.6.13</h3>
<ul>
<li>Data Sources now support dependency chaining. This enables you to create data sequences to form a more complex behavior with efficient asynchronous and parallel database queries. (RTAF-1764)</li>
<li>Added warning message when publishing and a Security Warning is present in the module. (RTAF-1713)</li>
<li>Added a warning message when a server action is being used in an anonymous screen in a Mobile or Reactive application. (RTAF-1711)</li>
<li>Added a warning message when Entity Actions are being directly used in client side. (RTAF-1710)</li>
<li>We improved the warnings in the TrueChange pane to remind you to refresh data sources that use Only On Demand settings. (RTAF-1500)</li>
</ul>
<h3 id="bug_fixing_11.6.13">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a crash after opening Theme Editor in a clone of an OutSystems UI module. (RDEV-1068)</li>
<li>Fixed an issue that caused a user-defined hexadecimal Color value to be different in Style Sheets Editor and Styles Editor. (RPD-3419)</li>
<li>Fixed an issue that caused the appropriate built-in functions to not be generated when converting an identifier primitive type to Identifier type while bootstrapping an entity from excel. (RDEV-1062)</li>
<li>Fixed an issue that caused a crash while setting the Width of a data Cell on a Show Records widget using Styles Editor. (RDEV-1058)</li>
<li>Fixed an issue that caused Service Studio to crash after trying to use Theme Editor to edit a referenced Theme. (RDEV-1053)</li>
<li>Fixed an issue that caused a tree element to lose focus when renaming that element without any modifications. (RDEV-1055)</li>
<li>Fixed an issue that caused a crash after losing access to the internet during the 'Build an App in 5-min' tutorial. (RDEV-944)</li>
<li>Fixed an issue that caused Theme Editor to not re-render sliders and checkboxes after using 'Reset Theme Editor'. (RDEV-1020)</li>
<li>Fixed an issue where the "refresh references" automated process was skipped when publishing a module's running version in an environment that only has the Deployment Controller role. (RPC-172)</li>
<li>Fixed drag and drop of a Screen to the Menu Block in Mobile and Reactive modules. (RTAF-1763)</li>
<li>Fixed an issue that caused a crash after deleting a Data Action Output parameter of the type List. (RTAF-1754)</li>
<li>Fixed preview of referenced Expressions without an Example property value. (RTAF-251)</li>
</ul>
<div class="hidden" id="development-environment-11.6.13_end"></div><div class="hidden" id="development-environment-11.6.11_start"></div>

<h2 id="development_environment_11.6.11">Development Environment 11.6.11</h2>
<div class="info">

Released on Nov 25, 2019</div>
<h3 id="new_in_development_environment_11.6.11">New in Development Environment 11.6.11</h3>
<ul>
<li>It is now possible to disable or enable multiple elements in an Action flow when the selection contains both disabled and enabled elements. Inspired by <a href="https://www.outsystems.com/ideas/7573/" target="_blank" rel="noopener noreferrer">Cláudia Capitão's idea</a>. (RDEV-1021)</li>
<li>Improved Table widget for Reactive OnSort generated action. (RTAF-1700)</li>
<li>Now, you can easily customize the look of your app without CSS by using <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Design_UI/Look_and_Feel/Customize_the_look_of_your_app_with_Theme_Editor" target="_blank" rel="noopener noreferrer">Theme Editor</a>. (RDEV-468)</li>
</ul>
<h3 id="bug_fixing_11.6.11">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to crash while closing Module tabs. (RDEV-1041)</li>
<li>Now, if the Widget Tree is open, selecting "Go to &lt;element&gt;" switches to the Elements tree and highlights the &lt;element&gt;. Reported by <a href="https://www.outsystems.com/ideas/6636/" target="_blank" rel="noopener noreferrer">João Barata</a>. (RDEV-490)</li>
<li>Fixed issue causing a TrueChange error to be displayed when using Binary Data expressions in calculated attributes in an Aggregate. (RSBO-1025)</li>
<li>Fixed an issue when using scaffolding with a custom menu. (RTAF-1733)</li>
<li>Fixed a crash when deleting a Data Source that is a dependency of another Data Source. (RTAF-1707)</li>
<li>All pending requests are now canceled when the user navigates to a new screen. (RTAF-1631)</li>
<li>Fixed an issue that caused a crash that occurred during a Compare and Merge while comparing Aggregates. (RICT-2100)</li>
<li>Fixed an issue that was causing Entity Actions and Service Actions to be set with the incorrect icon when dragged to a flow.
(RUDOF-697)</li>
<li>Service Studio now limits the number of Keyboard Shortcuts dialog windows to one per tab. (RUDOF-704)</li>
<li>We fixed the scaffolding of forms. Now the scaffolded forms have Checkbox Widgets instead of the Switch Widget for boolean values. This makes the forms work better in modern browsers. (RTAF-1731)</li>
</ul>
<div class="hidden" id="development-environment-11.6.11_end"></div><div class="hidden" id="development-environment-11.6.9_start"></div>

<h2 id="development_environment_11.6.9">Development Environment 11.6.9</h2>
<div class="info">

Released on Nov 20, 2019</div>
<h3 id="new_in_development_environment_11.6.9">New in Development Environment 11.6.9</h3>
<ul>
<li>Now, you are asked for confirmation before publishing a module that is being debugged. (RDEV-978)</li>
<li>Now, Service Studio only works with 64-bit operating systems. (RICT-2119)</li>
<li>You can now verify the type of Module your're developing in Service Studio. Check the Module Properties pane. (RTAF-1687)</li>
</ul>
<h3 id="bug_fixing_11.6.9">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to show multiple arrows during the 'Build an App in 5-min' tutorial. (RDEV-920)</li>
<li>Fixed a Service Studio crash when referencing Blocks with a placeholder and sample content that contains a Dropdown Widget. (RTAF-1671)</li>
<li>Fixed an issue that caused a crash while loading Mobile or Reactive Web modules. (RPD-4314)</li>
</ul>
<div class="hidden" id="development-environment-11.6.9_end"></div><div class="hidden" id="development-environment-11.6.7_start"></div>

<h2 id="development_environment_11.6.7">Development Environment 11.6.7</h2>
<div class="info">

Released on Nov 12, 2019</div>
<h3 id="new_in_development_environment_11.6.7">New in Development Environment 11.6.7</h3>
<ul>
<li>Improved the default REST API method names when the URLs contain parenthesis characters. (RSBO-903)</li>
<li>Added support for Visual Studio 2019 in Integration Studio. (RPC-446)</li>
<li>It is now possible to easily add a screen to the menu in Reactive Web simply by dragging it to menu. (RTAF-1486)</li>
</ul>
<h3 id="bug_fixing_11.6.7">Bug Fixing</h3>
<ul>
<li>Fixed the ".Net Compiler Tool" detection in Integration Studio when using Visual Studio 2019.  In installations with incorrect values, you can click "Reset Defaults" in the Options dialog box to determine the correct values. (RPC-447)</li>
<li>Fixed compiler error after changing the name of an entity attribute being used in aggregate functions. (RSBO-925)</li>
</ul>
<div class="hidden" id="development-environment-11.6.7_end"></div><div class="hidden" id="development-environment-11.6.6_start"></div>

<h2 id="development_environment_11.6.6">Development Environment 11.6.6</h2>
<div class="info">

Released on Oct 28, 2019</div>
<h3 id="new_in_development_environment_11.6.6">New in Development Environment 11.6.6</h3>
<ul>
<li>It is now possible to consume REST APIs using Swagger specifications that have enum elements.  (RSBO-872)</li>
<li>It's now possible to open the documentation page of exposed SOAP Web Services directly from Service Studio, similarly to the existing option for exposed REST APIs. Inspired by <a href="https://www.outsystems.com/ideas/5375/open-documentation-of-soap-web-service" target="_blank" rel="noopener noreferrer">Kilian's idea</a>. (RSBO-612)</li>
<li>Entity View Data now adds a 'Sort by Id Desc' by default (RSBO-611)</li>
</ul>
<h3 id="bug_fixing_11.6.6">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a crash when you tried to open a hidden element from Find Usages. (RDEV-908)</li>
<li>Fixed a bug when trying to go to an element while aggregate with a group by is fetching data. (RSBO-837)</li>
<li>Fixed an issue that prevented the creation of a new module when Application Template no longer existed. (RTAF-1073)</li>
<li>We fixed the help link in the Manage Dependencies dialog. Now the link points to the correct page. (RTAF-1229)</li>
</ul>
<div class="hidden" id="development-environment-11.6.6_end"></div><div class="hidden" id="development-environment-11.6.5_start"></div>

<h2 id="development_environment_11.6.5">Development Environment 11.6.5</h2>
<div class="info">

This is a preliminary version of the document.</div>
<h3 id="new_in_development_environment_11.6.5">New in Development Environment 11.6.5</h3>
<ul>
<li>It's now possible to use Client Variables on Aggregates. (RTAF-1334)</li>
</ul>
<div class="hidden" id="development-environment-11.6.5_end"></div><div class="hidden" id="development-environment-11.6.2_start"></div>

<h2 id="development_environment_11.6.2">Development Environment 11.6.2</h2>
<div class="info">

Released on Oct 14, 2019</div>
<h3 id="new_in_development_environment_11.6.2">New in Development Environment 11.6.2</h3>
<ul>
<li>We updated icons on the Reactive Web App's Table toolbar. (RTAF-1345)</li>
<li>Screen and Block LifeCycle event parameters are now only visible when used. With client variables, screen aggregate scope improvements and the fetch property, they should not be used only for more advanced scenarios. (RTAF-1505)</li>
</ul>
<h3 id="bug_fixing_11.6.2">Bug Fixing</h3>
<ul>
<li>Fixed an issue in the Style Sheet Editor that caused a crash after opening a stylesheet that includes CSS variables. (RDEV-913)</li>
<li>Fixed an issue that caused Service Studio to crash during the 'Build a Web/Mobile App in 5 min' tutorials while calculating the position of the tutorial arrows. (RDEV-915)</li>
<li>Fixed an issue in the 1-Click Publish tab that duplicated the 'RETRY PUBLISH' and 'CLOSE' buttons for each publishing error. (RDEV-901)</li>
<li>Fixed Reactive Screen/Block event getting hidden when the handler action was deleted but still assigned. (RTAF-1507)</li>
<li>Fixed invalid logo images in newly created modules. (RTAF-1498)</li>
</ul>
<div class="hidden" id="development-environment-11.6.2_end"></div><div class="hidden" id="development-environment-11.6.1_start"></div>

<h2 id="development_environment_11.6.1">Development Environment 11.6.1</h2>
<div class="info">
Released on Oct 02, 2019
</div>
<h3 id="new_in_development_environment_11.6.1">New in Development Environment 11.6.1</h3>
<ul>
<li><b>You can now create a new type of app, <a href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30195" target="_blank" rel="noopener noreferrer">Reactive Web App</a>.</b> This type of app is based on the client-side development paradigm. Reactive App comes with its own new features: Table Widget, server-side pagination, and Public Screens. (RTAF-115)</li>
<ul>
<li><a href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30198" target="_blank" rel="noopener noreferrer">Table Widget</a>, available in the <a href="https://www.outsystems.com/DocRouter/Router.aspx?PlatformToolName=ServiceStudio&amp;PlatformVersionNumber=11.0&amp;HelpId=30195" target="_blank" rel="noopener noreferrer">Reactive Web</a> apps, comes with an accelerator: drag an Entity on it to create a table with sorting and pagination. Use tables to show data in cells distributed in rows and columns. (RTAF-204)</li>
<li>Use the server-side pagination feature of the Screen Aggregates to build faster apps that need to handle large data sets. Enter the Start Index and fetch the number of records you define in Max Records. (RTAF-630)</li>
<li>Public Screens will allow you to reuse UI across different Reactive Web modules and apps. Because the UI can be modular, you can now have more complex UI modules that you can maintain efficiently. You can collaborate better without merge conflicts, as one team can be working on the logic module, while the other is updating the UI module. (RTAF-198)</li>
<li>Download Tool is available in Reactive Apps. Now you can drag a Download Tool to your Flow and create a node which, when executed, sends a file for download to the end-user. (RTAF-993)</li>
</ul>
<li>You can now create <a href="https://success.outsystems.com/Documentation/11/Developing_an_Application/Reuse_and_Refactor/Libraries" target="_blank" rel="noopener noreferrer">Libraries</a> in Mobile and Reactive Web apps. This new module type is specially tailored for building highly reusable logic and UI and fits directly in the Foundation layer of the 4 Layer Canvas. This feature requires OutSystems Platform Server 11 Release Oct.2019. (RSBO-811)</li>
<li>The Dropdown Widget has a new property Options Content, which you can set to Text Only or Custom. Text Only gives a native look and feel of the drop-down lists in your Reactive and Mobile apps. Use Options Content property set to Custom to build a list of images or other Widgets. (RTAF-1208)</li>
<li>Button Widgets in Mobile and Reactive Apps now have the Is Form Default property, which you can set to Yes and make the App submit the data from the related form when the end-user presses the Enter key. (RTAF-943)</li>
<li>Now you can create <a href="https://success.outsystems.com/Documentation/11/Reference/OutSystems_Language/Data/Handling_Data/Client_Variable" target="_blank" rel="noopener noreferrer">Client Variables</a> in Mobile and Reactive Apps. Use Client Variables to store Basic Data Types locally or share the values across apps through public Blocks and public Client Actions. (RTAF-1052)</li>
<li>We improved Data Sources and made asynchronous data fetching straightforward to use in Mobile and Reactive Apps. Screen Aggregates and Data Actions are now available in the scope of other Screen Aggregates and Data Actions. We also added the Fetch property with On Start and On Demand options. Now you can implement patterns such as master/detail with excellent performance and user experience. (RTAF-992)</li>
<li>Added mobile debugger support to iOS13. (RTAF-1349)</li>
</ul>
<h3 id="bug_fixing_11.6.1">Bug Fixing</h3>
<ul>
<li>Fixed crash while loading modules with Dropdown widgets that contain direct children like IF, Web Block Instance, or Text. (RTAF-1433)</li>
<li>Fixed the text formatting of the "More Information" field in dialog boxes. (RMAC-1392)</li>
<li>Fixed rare crash when scrolling through the screen editor. (RTAF-999)</li>
</ul>
<div class="hidden" id="development-environment-11.6.1_end"></div><div class="hidden" id="development-environment-11.5.45_start"></div>

<h2 id="development_environment_11.5.45">Development Environment 11.5.45</h2>
<div class="info">Released on Sep 24, 2019</div>
<h3 id="new_in_development_environment_11.5.45">New in Development Environment 11.5.45</h3>
<ul>
<li>Added mobile debugger support to iOS13 (RTAF-1349)</li>
</ul>
<h3 id="bug_fixing_11.5.45">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused icons to be displayed with the wrong size on Add Local Entity From Database.
(RDEV-830)</li>
<li>Fixed a crash when clicking too fast or going back in the Applications List (RICT-1971)</li>
<li>Fixed crash navigating to an error message that appeared after replacing data on a screen created from a template (RTAF-1337)</li>
<li>Fixed the error "Circular attribute group reference" when executing the XMLDocument_Load action of the Xml extension. (RPD-3742)</li>
<li>Fixed crash that occurred when removing unused references or finding usages in a module containing inline records (RICT-1976)</li>
<li>Fixed Service Studio crash while saving module with unused placeholder arguments inside public Web Blocks. (RICT-1968)</li>
<li>Fixed crash that occurred when removing unused references or finding usages in a module containing inline records (RPD-4403)</li>
<li>Fixed a problem where, when having Service Studio connected to multiple environments, converting a module to another type (such as converting a module to a Service module) would open it on a window from another environment. (RSBO-838)</li>
</ul>
<div class="hidden" id="development-environment-11.5.45_end"></div><div class="hidden" id="development-environment-11.5.44_start"></div>

<h2 id="development_environment_11.5.44">Development Environment 11.5.44</h2>
<div class="info">
Released on Sep 11, 2019
</div>
<h3 id="new_in_development_environment_11.5.44">New in Development Environment 11.5.44</h3>
<ul>
<li>It is now possible to consume REST APIs using a Swagger specification from a local file system path. (RSBO-829)</li>
</ul>
<h3 id="bug_fixing_11.5.44">Bug Fixing</h3>
<ul>
<li>Fixed the tooltip text for List Box widget. (RDEV-811)</li>
<li>Fixed an issue that caused a crash when editing Style Classes in Style Editor. (RDEV-835)</li>
<li>Fixed an issue that caused an overlay text to appear over the mouse cursor when dragging an element inside an Aggregate. (RICT-1836)</li>
<li>Fixed the upgrade of mobile applications via Service Center when the module was not upgraded previously nor had its referenced refreshed. (RTAF-1290)</li>
<li>Fixed an issue that caused a crash when opening Service Studio with an invalid command-line argument. (RICT-1927)</li>
</ul>
<div class="hidden" id="development-environment-11.5.44_end"></div><div class="hidden" id="development-environment-11.5.43_start"></div>

<h2 id="development_environment_11.5.43">Development Environment 11.5.43</h2>
<div class="info">

Released on Sep 04, 2019
</div>
<h3 id="new_in_development_environment_11.5.43">New in Development Environment 11.5.43</h3>
<ul>
<li>We updated the part of the UI about the New Module panel in application details to improve usability. (RMAC-1138)</li>
</ul>
<h3 id="bug_fixing_11.5.43">Bug Fixing</h3>
<ul>
<li>RichWidgets reference is no longer added on Mobile modules when replacing data. (RTAF-1145)</li>
<li>Fix crashes when dropping Structures to a Consume REST integration. (RSBO-737)</li>
</ul>
<div class="hidden" id="development-environment-11.5.43_end"></div><div class="hidden" id="development-environment-11.5.42_start"></div>

<h2 id="development_environment_11.5.42">Development Environment 11.5.42</h2>
<div class="info">

Released on Aug 26, 2019
</div>
<h3 id="new_in_development_environment_11.5.42">New in Development Environment 11.5.42</h3>
<ul>
<li>Improved efficiency of opening support cases from IDE by pre-filling form fields. (RDEV-562)</li>
<li>You can now restart your Personal Environment in the <a href="https://www.outsystems.com/goto/home" target="_blank" rel="noopener noreferrer">Platform Home page</a>. This allows you to recover from a 503 error (server unavailable) when creating a new Application or during a 1-Click Publish. (RDEV-706)</li>
<li>Now, you can quickly search and add a dependency by right-clicking on a folder in a tree (e.g. Server Actions folder) and selecting "Add Dependency". (RDEV-712)</li>
</ul>
<h3 id="bug_fixing_11.5.42">Bug Fixing</h3>
<ul>
<li>Fixed an issue that made Service Studio crash if your last interaction before closing a module was a selection popup (e.g. select from RunServerAction). (RICT-1903)</li>
<li>Fixed a problem when compiling modules if they contain widgets whose width or margin properties are not in a numeric format. (RTAF-1054)</li>
</ul>
<div class="hidden" id="development-environment-11.5.42_end"></div><div class="hidden" id="development-environment-11.5.40_start"></div>

<h2 id="development_environment_11.5.40">Development Environment 11.5.40</h2>
<div class="info">

Released on Aug 12, 2019
</div>
<h3 id="new_in_development_environment_11.5.40">New in Development Environment 11.5.40</h3>
<ul>
<li>From now on, Local Variables created from the Variable property of an Input widget inherit the Variable name. Inspired by <a href="https://www.outsystems.com/ideas/6056/" target="_blank" rel="noopener noreferrer">Johan's idea</a>. (RDEV-702)</li>
<li>The property Values from Dropdown widget was renamed to Options Value. (RTAF-904)</li>
</ul>
<h3 id="bug_fixing_11.5.40">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the scroll of the Forge Updates (bell) to not work. (RDEV-714)</li>
<li>Fixed an issue that caused a crash when double clicking filter conditions in Aggregates. (RDEV-686)</li>
<li>Fixed an issue that caused Service Studio to crash while changing Style Classes. (RDEV-685)</li>
<li>Fixed an issue that crashed Service Studio when closing the Manage Dependencies window before it was fully loaded. (RICT-1867)</li>
<li>Fixed an issue that caused Entity relationships not to be shown after dragging an Entity to an Entity Diagram containing related Entities. (RDEV-700)</li>
<li>Fixed crash in Manage Dependencies window after selecting a producer module. (RUDOF-480)</li>
</ul>
<div class="hidden" id="development-environment-11.5.40_end"></div><div class="hidden" id="development-environment-11.5.39_start"></div>

<h2 id="development_environment_11.5.39">Development Environment 11.5.39</h2>
<div class="info">

Released on Jul 31, 2019
</div>
<h3 id="new_in_development_environment_11.5.39">New in Development Environment 11.5.39</h3>
<ul>
<li>We updated the part of the UI about the application details, to improve usability and give it a fresher look and feel. (RMAC-1045)</li>
<li>We improved the experience of creating custom Screen Templates from the existing Screen Templates. Now the resulting Screen Template has the base Layout upon creation. (RTAF-877)</li>
<li>On new installations of Service Studio, the install folder is now "\Program Files\OutSystems\Development Environment 11". (RRET-1296)</li>
<li>The Development Environment releases now follow a new versioning format. Check <a href="https://www.outsystems.com/forums/discussion/50621/were-changing-how-we-version-outsystems-11-releases/#Post187886" target="_blank" rel="noopener noreferrer">this forum post</a> for more information about this change. (RRET-1317)</li>
</ul>
<h3 id="bug_fixing_11.5.39">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the mouse cursor (icon) to be wrongly displayed while dragging elements over Entity Diagram or Aggregates. (RDEV-564)</li>
<li>Fixed an issue that caused changed app details not to be updated. This happened after you’d change the app icon, name, description or color in the application details and then returned to the application list. (RMAC-1035)</li>
<li>Fixed a crash while loading modules that were previously saved with web editor opened and text selected. (RTAF-949)</li>
<li>Fixed an issue that prevented the usage of preview data on Aggregates and Test Queries by always requesting a publish of the module. (RTAF-913)</li>
<li>Fixed an issue in Integration Studio that prevented setting a default value for a column of type Long Integer. (RPD-4289)</li>
<li>Now the messages get always centered and do not show up in the wrong tab. (RMAC-1050)</li>
</ul>
<div class="hidden" id="development-environment-11.5.39_end"></div><div class="hidden" id="development-environment-r.29_start"></div>

<h2 id="development_environment_release_29">Development Environment Release 29</h2>
<div class="info">

Released on Jul 18, 2019
</div>
<h3 id="bug_fixing_release_29">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented the usage of Preview Data on Aggregates and Test Query by always requesting a publish of the module. (RTAF-913)</li>
<li>Fixed an issue that caused Service Studio to crash when dragging text in the expression editor. (RDEV-566)</li>
<li>Fixed bug that prevented mobile applications from loading in production when a producer was published in debug mode. (RPD-3596)</li>
</ul><div class="hidden" id="development-environment-r.29_end"></div><div class="hidden" id="development-environment-r.28_start"></div>

<h2 id="development_environment_release_28">Development Environment Release 28</h2>
<div class="info">

Released on Jul 15, 2019
</div>
<h3 id="bug_fixing_release_28">Bug Fixing</h3>
<ul>
<li>Fixed crash when using static entities from a SOAP service more than once in a SQL node statement. (RSBO-628)</li>
<li>Fixed crash when using Static Entities from a SOAP service more than once in an Aggregate. (RSBO-627)</li>
<li>Fixed issue when removing a reference to used Entity. (RTAF-783)</li>
</ul><div class="hidden" id="development-environment-r.28_end"></div><div class="hidden" id="development-environment-r.27_start"></div>

<h2 id="development_environment_release_27">Development Environment Release 27</h2>
<div class="info">

Released on Jul 08, 2019
</div>
<h3 id="new_in_development_environment_release_27">New in Development Environment Release 27</h3>
<ul>
<li>It is now possible to find public elements across all Modules in an Environment and add them as dependencies. Inspired by <a href="https://www.outsystems.com/ideas/1177/" target="_blank" rel="noopener noreferrer">Gerry's idea</a>. (RDEV-303)</li>
<li>Now, the Style Classes property of widgets provides suggestions based on most used styles on widgets of the same type (for example, Button, Container, ...). (RDEV-567)</li>
</ul>
<h3 id="bug_fixing_release_27">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the Forge Updates pop-up not to close when clicking the bell icon. (RDEV-572)</li>
<li>Fixed an issue that caused the text within Comment elements in entity diagrams disappear when clicking outside the comment box. (RDEV-550)</li>
<li>Fixed crash while rendering Mobile screens that included the HTML Element widget. (RICT-1667)</li>
<li>Fixed a crash when manipulating screens containing OutSystems UI blocks. (RICT-1650)</li>
<li>Fixed the text merge operation in SQL elements that was adding stars to entities without any user modification. (RMAC-820)</li>
<li>Fixed icon alignment in several Service Studio windows. (RMAC-828)</li>
<li>Fixed the background color of the Licenses window. (RMAC-885)</li>
<li>Forge dependency analysis no longer requires you to perform a "Force Install" for components with compatible changes like adding optional inputs or attributes. This only applies to changes in producer modules used by the application being installed. (RSBO-621)</li>
<li>Double-clicking inside an Aggregate editor will no longer open the Add Source picker twice. This behavior was allowing you to add an invalid Data Source. (RSBO-622)</li>
</ul><div class="hidden" id="development-environment-r.27_end"></div><div class="hidden" id="development-environment-r.26_start"></div>

<h2 id="development_environment_release_26">Development Environment Release 26</h2>
<div class="info">

Released on Jul 01, 2019
</div>
<h3 id="new_in_development_environment_release_26">New in Development Environment Release 26</h3>
<ul>
<li>It's now possible to import REST APIs using Swagger/OpenAPI with an "Example" field value for complex objects. (RSBO-84)</li>
<li>Added a new error message stating that you cannot use the EnhancedWebReferences API together with a consumed SOAP Web Service created in OutSystems 11 (you must use the SOAP Extensibility API instead). (RSBO-536)</li>
</ul>
<h3 id="bug_fixing_release_26">Bug Fixing</h3>
<ul>
<li>We fixed a crash related to certain conditions when navigating to a Variable value during a debug session. (RTAF-619)</li>
</ul><div class="hidden" id="development-environment-r.26_end"></div><div class="hidden" id="development-environment-r.25_start"></div>

<h2 id="development_environment_release_25">Development Environment Release 25</h2>
<div class="info">

Released on Jun 19, 2019
</div>
<h3 id="new_in_development_environment_release_25">New in Development Environment Release 25</h3>
<ul>
<li>Added support for TLS 1.1 and TLS 1.2 on MySQL external database connections. Warning: OutSystems now distributes BouncyCastle (v1.8.3) and Google.Protobuf (v.3.6.1.0) alongside the MySQL driver - this may impact the existing extensions that use different versions. (RSAT-1258)</li>
</ul>
<h3 id="bug_fixing_release_25">Bug Fixing</h3>
<ul>
<li>We fixed a crash related to certain conditions when dragging and dropping text in Expression Editor. (RTAF-611)</li>
</ul><div class="hidden" id="development-environment-r.25_end"></div><div class="hidden" id="development-environment-r.24_start"></div>

<h2 id="development_environment_release_24">Development Environment Release 24</h2>
<div class="info">

Released on Jun 11, 2019
</div>
<h3 id="new_in_development_environment_release_24">New in Development Environment Release 24</h3>
<ul>
<li>It is now possible to hide mobile app upgrade notifications by setting an empty message on the "Upgrade Messages" properties of the module. (RTAF-610)</li>
<li>Added support for TLS 1.1 and TLS 1.2 on MySQL external database connections. (RSAT-1258)</li>
<li>You can now convert an Aggregate to SQL in the window that displays the executed SQL. This option is only available if the Aggregate does not contain any of the following scenarios:<br/>
— Structures in Source<br/>
— Calculated attributes<br/>
— Group By attributes<br/>
— Dynamic Sorts<br/>
This feature requires OutSystems Platform Server 11 Release Apr.2019 CP1. (RSBO-535)</li>
<li>Addresses used to previously import SOAP Web Services are now saved and can be reused. (RSBO-426)</li>
<li>When refreshing a SOAP Web Service, it's now possible to select a location for the definition other than the one used initially to import the service. (RSBO-434)</li>
<li>Added 'Deprecated' information to EnhancedWebReferences actions. (RSBO-424)</li>
<li>It is now possible to consume SOAP services that have sequences with duplicated elements. (RPD-3898)</li>
<li>Added support for SOAP Actions containing special characters. (RSBO-384)</li>
</ul>
<h3 id="bug_fixing_release_24">Bug Fixing</h3>
<ul>
<li>Fixed an issue that set the wrong Output Entity/Structure name in SQL node. (RDEV-496)</li>
<li>Fixed an issue that caused the properties dropdowns not to be shown when pressing F4. (RDEV-471)</li>
<li>Fixed an issue that caused Give Us Feedback popup to lose focus after changing the score. (RDEV-437)</li>
<li>Fixed wrong help URLs in Integration Studio and it now opens the documentation on the default system browser. Removed offline documentation. (RSBO-416)</li>
<li>Fixed a crash that occurred when adding a variable to the Debug Watches list. (RTAF-530)</li>
<li>Fixed a crash in Expression Editor drag dropping text (RTAF-592)</li>
<li>Fixed an issue that caused the scheduler to stop handling Processes for a while when updating an existing license via "ConfigurationTool /UploadLicense." (RSAT-1398)</li>
<li>Fixed an issue in the CSS Editor and Styles Editor where the values of CSS variables were not being considered. (RDEV-450)</li>
<li>Fixed an issue that affected text within comment nodes in entity diagrams when moving the nodes in edit mode and in some other situations while typing. (RDEV-412)</li>
<li>Improved performance of CSS Editor in large Stylesheets. (RPD-3249)</li>
</ul><div class="hidden" id="development-environment-r.24_end"></div><div class="hidden" id="development-environment-r.23_start"></div>

<h2 id="development_environment_release_23">Development Environment Release 23</h2>
<div class="info">

Released on May 20, 2019
</div>
<h3 id="new_in_development_environment_release_23">New in Development Environment Release 23</h3>
<ul>
<li>You can now add multiple customized Style Classes (Style and Properties tab) to widgets using autocomplete suggestions. (RDEV-146)</li>
</ul>
<h3 id="bug_fixing_release_23">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a crash while trying to import Entities from an Excel file that was already being used by another application or process. (RDEV-426)</li>
<li>Fixed an issue where Open from Environment window search filter couldn't find a Module if the search string had a space at the end. (RDEV-428)</li>
<li>Fixed an issue that caused the wrong icon to be shown while dragging the Run Server Action element to an Action Flow. (RDEV-435)</li>
<li>Fixed compilation error that occurred when SOAP Faults were using types based on the .NET CLR (Common Language Runtime). (RPD-3979)</li>
<li>It is now possible to consume SOAP services that have elements with spaces in the name. (RSBO-438)</li>
<li>It is now possible to consume SOAP services that have sequences with duplicated elements. (RPD-3898)</li>
<li>Added support for SOAP Actions containing special characters. (RSBO-384)</li>
<li>Improved performance of CSS Editor in large Stylesheets. (RPD-3249)</li>
</ul><div class="hidden" id="development-environment-r.23_end"></div><div class="hidden" id="development-environment-r.22_start"></div>

<h2 id="development_environment_release_22">Development Environment Release 22</h2>
<div class="info">

Released on May 13, 2019
</div>
<h3 id="new_in_development_environment_release_22">New in Development Environment Release 22</h3>
<ul>
<li>Improved visibility of Styles Editor by showing it as a tab in the Properties Area. (RDEV-325)</li>
</ul>
<h3 id="bug_fixing_release_22">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented Entity relationships from being displayed in Entity Diagrams with a large number of Entities. (RDEV-411)</li>
<li>Fixed an issue with Service Studio '-publish' command line option. (RDEV-415)</li>
</ul><div class="hidden" id="development-environment-r.22_end"></div><div class="hidden" id="development-environment-r.21_start"></div>

<h2 id="development_environment_release_21">Development Environment Release 21</h2>
<div class="info">

Released on Apr 30, 2019
</div>
<h3 id="bug_fixing_release_21">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to lose focus after closing a dialog window. (RDEV-331)</li>
<li>Fixed a crash when executing tutorials. (RICT-1511)</li>
</ul><div class="hidden" id="development-environment-r.21_end"></div><div class="hidden" id="development-environment-r.20_start"></div>
<h2 id="development_environment_release_20">Development Environment Release 20</h2>
<div class="info">

Released on May 29, 2019

</div>
<h3 id="new_in_development_environment_release_20">New in Development Environment Release 20</h3>
<ul>
<li>From now on, we will periodically ask you how you feel about Service Studio. (RDEV-258)</li>
</ul>
<h3 id="bug_fixing_release_20">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented some Built-in Functions from being highlighted in expressions. (RDEV-384)</li>
<li>Fixed an issue that caused the wrong icon to be shown while dragging a client-side element on top of another element in a Client Action flow. (RDEV-393)</li>
</ul>
<div class="hidden" id="development-environment-r.20_end"></div><div class="hidden" id="development-environment-r.19_start"></div>

<h2 id="development_environment_release_19">Development Environment Release 19</h2>
<div class="info">

Released on Apr 22, 2019
</div>
<h3 id="new_in_development_environment_release_19">New in Development Environment Release 19</h3>
<ul>
<li>Now, opening Manage Dependencies is on average 2x quicker. (RDEV-397)</li>
</ul>
<h3 id="bug_fixing_release_19">Bug Fixing</h3>
<ul>
<li>We fixed an occasional crash while debugging an app in instances where the debugger variables changed. (RICT-1481)</li>
<li>Fixed an issue in the Spanish translation of RichWidgets. (RPD-3132)</li>
<li>Fixed a Service Studio crash that occurred when introspecting WSDL with types having a single attribute with the same name. (RSBO-249)</li>
<li>Fixed an issue in WSDL introspection to enable the use of input/output structures without any attributes in the service definition. (RSBO-273)</li>
<li>Now Service Studio doesn't crash when you continue the debug session several consecutive times (for example, by pressing F10). (RTAF-342)</li>
<li>Now, connections between Entities are shown correctly after dragging and zooming an Entity Diagram. (RDEV-352)</li>
<li>Fixed an issue that prevented you from selecting text and from setting the cursor in the search field of the Toolbox. (RPD-2804)</li>
<li>Fixed an issue that changed the Column property of a List_SortColumn when that property referenced an Entity that belonged to another module. The issue occurred after modifying an Entity Attribute in the producer Module and refreshing the consumer module. (RPD-4014)</li>
<li>Fixed an issue that caused elements inside Folders not to be deleted when managing dependencies. (RICT-1471)</li>
<li>Fixed Service Studio hang when changing complex SQL argument expressions. (RPD-3974)</li>
<li>Fixed the scroll bar that shows while you browse Screen Templates in the New Screen window. (RTAF-339)</li>
</ul><div class="hidden" id="development-environment-r.19_end"></div><div class="hidden" id="development-environment-r.18_start"></div>

<h2 id="development_environment_release_18">Development Environment Release 18</h2>
<div class="info">

Released on Apr 15, 2019
</div>
<h3 id="new_in_development_environment_release_18">New in Development Environment Release 18</h3>
<ul>
<li>Now, the label of an Assign is automatically set after dragging a Variable with a data type of Entity, Structure, or Record to an Action Flow. Inspired by <a href="https://www.outsystems.com/ideas/5918/" target="_blank" rel="noopener noreferrer">Nelson's idea</a>. (RDEV-56)</li>
<li>From now on it is possible to open a Screen in browser when the Widget Tree is enabled. Inspired by <a href="https://www.outsystems.com/ideas/6344/" target="_blank" rel="noopener noreferrer"> Johan's idea</a>. (RDEV-172)</li>
<li>We have now added support to enable or disable early access features at the environment level. (RSCT-1810)</li>
<li>Updated the following JavaScript library used by the mobile application runtime: 'decimal.js' to version 10.0.1, 'toformat' to version 2.0.0. (RTAF-91)</li>
<li>Now you can go to the documentation for "How to Integrate With an External Database" from the context menu of Databases, in the Data tab. (RDEV-318)</li>
<li>Now you can quickly tell us how you feel about Service Studio. Click the megaphone icon on the toolbar, rate, and click Send. Try it out and tell us what you think! (RDEV-253)</li>
<li>Improved visibility of True Change messages' suggestions and help documentation. Suggestions to fix the message are shown as a light bulb and a link to the documentation is shown as a question mark. (RDEV-230)</li>
<li>It is now possible to fix a mobile List widget that has an invalid source by dragging and dropping a valid source on top of the List. (RDEV-176)</li>
<li>It is now possible to use Ctrl+Down/Ctrl+Up to reorder assignments when the focus is on the Value property of an Assign. Inspired by <a href="https://www.outsystems.com/ideas/6051/" target="_blank" rel="noopener noreferrer"> PJ M's idea</a>. (RDEV-174)</li>
</ul>
<h3 id="bug_fixing_release_18">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented adding "{EntityName}.*" automatically to a SQL query by dragging an Entity to the SQL element. (RDEV-351)</li>
<li>Fixed a Service Studio crash that occurred when introspecting WSDL with types having a single attribute with the same name. (RSBO-249)</li>
<li>Fixed an issue in WSDL introspection to correctly identify attributes with types declared in place via restriction. (RSBO-281)</li>
<li>Fixed an issue where the "Widget" property on "Ajax Refresh" nodes showed multiple "Select Widget" options. (RDEV-320)</li>
<li>Fixed the icon of the Run Server Action element shown in the Toolbox when editing Actions with a custom Icon. (RDEV-335)</li>
<li>Fixed an issue with generating structures in SOAP services that use the "unbounded" qualifier in group references. (RPD-4020)</li>
<li>Fixed a crash that occurred when importing SOAP Web Services that had invalid WSDL definition with missing portType elements. (RSBO-356)</li>
</ul><div class="hidden" id="development-environment-r.18_end"></div><div class="hidden" id="development-environment-r.17_start"></div>

<h2 id="development_environment_release_17">Development Environment Release 17</h2>
<div class="info">

Released on Mar 18, 2019
</div>
<h3 id="bug_fixing_release_17">Bug Fixing</h3>
<ul>
<li>Fixed an issue in the JSON Serialize widget that affected the serialization of Date and Time values. This was causing the JSON Deserialize widget to return empty values. (RPD-3970)</li>
</ul><div class="hidden" id="development-environment-r.17_end"></div><div class="hidden" id="development-environment-r.16_start"></div>

<h2 id="development_environment_release_16">Development Environment Release 16</h2>
<div class="info">

Released on Mar 12, 2019
</div>
<h3 id="new_in_development_environment_release_16">New in Development Environment Release 16</h3>
<ul>
<li>The widget selection window for the Ajax Refresh element now shows a notification banner stating 'This window only shows widgets that have the Name property defined.'. (RDEV-26)</li>
<li>We improved the discoverability of the Widget Tree: Added animation to the widget tree when you are dragging a widget to a Screen or Block, and changed the widget tree button. (RDEV-177)</li>
<li>Caption buttons now change color on hover. (RDEV-158)</li>
<li>Improved the error messages shown when opening unsupported Modules saved in newer Service Studio versions or when opening Modules containing unknown elements. (RDEV-163)</li>
<li>Service Studio no longer fills-in the default element name as soon as the name of the element gets erased. (RDEV-162)</li>
<li>Improved focus when editing styles in mobile applications. (RMAC-204)</li>
</ul>
<h3 id="bug_fixing_release_16">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was causing Open Source Licenses window to lose focus when minimizing Service Studio. (RICT-1419)</li>
<li>SOAP introspection now supports enumerator values with more than 50 characters. (RSBO-259)</li>
<li>Fixed SOAP introspection and compilation of WSDLs with enumerations inside &lt;list&gt; elements. (RSBO-272)</li>
<li>Fixed an issue with the number of usages in consumers shown when using the "Find Usages in All Modules" in Service Modules. (RDEV-232)</li>
<li>Fixed a crash when adding a dependency in the application detail screen. (RICT-1393)</li>
<li>Fixed a compilation error when using some patterns in a Dynamic Sort of an Aggregate. (RICT-1398)</li>
<li>Fixed a problem which caused SOAP Web Services imported in version 11 to have incorrect information. This happened when the WSDL had an enumeration defined in a top-level element that is used directly in an input part. (RSBO-360)</li>
</ul><div class="hidden" id="development-environment-r.16_end"></div><div class="hidden" id="development-environment-r.15_start"></div>

<h2 id="development_environment_release_15">Development Environment Release 15</h2>
<div class="info">

Released on Mar 04, 2019
</div>
<h3 id="new_in_development_environment_release_15">New in Development Environment Release 15</h3>
<ul>
<li>Expression Editor now has buttons for True and False boolean values. Inspired by <a href="https://www.outsystems.com/ideas/2339/" target="_blank" rel="noopener noreferrer"> Hans Bruins' idea</a>. (RDEV-160)</li>
<li>Service Studio can now be updated automatically. Go to Settings and select "Update Service Studio automatically" to turn on the feature. The auto-update is disabled if you're running Service Studio on Windows Server. Inspired by <a href="https://www.outsystems.com/ideas/1352/" target="_blank" rel="noopener noreferrer">André Ramos' idea</a>. (RICT-1351)</li>
<li>Added German translations to RichWidgets. (ROU-40)</li>
<li>You can now add a preview image to your Screen Template in the metadata section. (RTAF-134)</li>
<li>Upgraded SharpZipLib library to version 1.1.0. (RRCT-2292)</li>
<li>Updated the following JavaScript libraries used by the mobile applications runtime: 'decimal.js' to version 10.0.1, 'toformat' to version 2.0.0. (RTAF-91)</li>
</ul>
<h3 id="bug_fixing_release_15">Bug Fixing</h3>
<ul>
<li>Fixed an issue when copy-pasting actions ListAppend and ListAppendAll from a module to another that was causing some type conversion mappings to be deleted. (RICT-1354)</li>
<li>Fixed SOAP introspection not detecting some unsupported features. (RSBO-246)</li>
<li>Now there's no crash when you add a link from a web screen to an external web site. (RTAF-106)</li>
<li>Fixed a bug that allowed Light Processes to have Input Parameters but would cause a compilation error when publishing. (RPD-3358)</li>
<li>Improved the warning message in wizard "Create Action to Bootstrap Data from Excel" when the attributes are not going to be included in the bootstrap. (RSBO-53)</li>
<li>Fixed an issue that was incorrectly throwing an error when using a referenced Entity with Expose Read Only as a trigger to Processes or Activities. (RSBO-303)</li>
<li>Now all of the conditions are updated accordingly when you change a source inside the Aggregate Join section. (RSBO-72)</li>
<li>Fixed a crash when importing a SOAP Web Service without any service definition. (RSBO-305)</li>
<li>Service Studio no longer changes the Last Modified By property of unmodified elements. (RPD-3881)</li>
<li>Fixed a GUI bug that allowed you to select Client Entities and Read-Only Reference Entities as Event Triggers. (ABE-1351)</li>
<li>We fixed an error that prevented you from upgrading a module with the dynamic join logic to OutSystems 11. (RPD-3674)</li>
<li>Fixed crash that occurred when changing the type of a structure attribute to a structured type (entity, structure, list, or anonymous structure) when the attribute was used by a Combo Box widget. (RICT-1308)</li>
<li>Fixed a crash when pasting logic from a Client Action in a mobile module to a Server Action in a web module. (RICT-1307)</li>
<li>We fixed the compilation error caused by a missing validation for the Combo Box variable type. (RICT-1320)</li>
<li>Clicking the Close button while Service Studio is closing no longer crashes the program. (RICT-1371)</li>
<li>Fixed a crash that occurred when double-clicking a verify message. (RICT-1258)</li>
<li>Fixed occasional crash using the Search in several tabs at the same time. (RTAF-108)</li>
</ul><div class="hidden" id="development-environment-r.15_end"></div><div class="hidden" id="development-environment-r.14_start"></div>

<h2 id="development_environment_release_14">Development Environment Release 14</h2>
<div class="info">

Released on Feb 11, 2019
</div>
<h3 id="new_in_development_environment_release_14">New in Development Environment Release 14</h3>
<ul>
<li>Now you can open the Application details in the Application search results without resetting the search. Inspired by <a href="https://www.outsystems.com/ideas/5137/" target="_blank" rel="noopener noreferrer">Tiago's idea</a>. (RIUT-650)</li>
<li>Updated the following JavaScript libraries used by the mobile applications runtime: 'requirejs' to version 2.3.6, 'es6-promise' to version 4.2.5, 'long' to version 4.0.0, 'decimal.js' to version 10.0.1, 'toformat' to version 2.0.0. (RTAF-91)</li>
</ul>
<h3 id="bug_fixing_release_14">Bug Fixing</h3>
<ul>
<li>We fixed a crash in the Mobile Tutorial that happened when you created the first Screen. (RICT-1275)</li>
<li>We fixed a crash in creating the first Screen in a Flow that already had an Entry node. (RPD-3731)</li>
<li>We fixed an error that prevented you from upgrading a module with the dynamic join logic to OutSystems 11. (RPD-3674)</li>
<li>Now all of the conditions are updated accordingly when you change a source inside the Aggregate Join section. (RSBO-72)</li>
<li>Now there's no crash when you browse the Screen Template categories while doing the tutorials. (RTAF-98)</li>
<li>We fixed the Aggregate icon for the local storage. (RTAF-102)</li>
</ul><div class="hidden" id="development-environment-r.14_end"></div><div class="hidden" id="development-environment-r.13_start"></div>

<h2 id="development_environment_release_13">Development Environment Release 13</h2>
<div class="info">

Released on Feb 05, 2019
</div>
<h3 id="new_in_development_environment_release_13">New in Development Environment Release 13</h3>
<ul>
<li>Improved the identification of screens and blocks differences in Compare and Merge window. (RCOT-2139)</li>
<li>You can now use a Text Editor to edit attributes and variables' default value. Inspired by <a href="https://www.outsystems.com/ideas/5934/" target="_blank" rel="noopener noreferrer">Ricardo Reis' idea</a>. (RIUT-591)</li>
<li>Deprecated VerifySqlLiteral action from Sanitization.xif in favor of BuildSafe_InClauseIntegerList and BuildSafe_InClauseTextList. Both actions will be available in Platform Server Release Jan.2019 CP2. (RRCT-2108)</li>
<li>Improved Integration Studio icons. (RINT-3338)</li>
<li>Added a warning when the argument passed to a SQL Query Parameter with the Expand Inline set starts with "EncodeSql". Also added a warning when the argument passed to a SQL Query Parameter with the Expand Inline set uses the built-in function Replace. Both scenarios are prone to cause runtime errors. (RRCT-2116)</li>
</ul>
<h3 id="bug_fixing_release_13">Bug Fixing</h3>
<ul>
<li>Fixed a crash when dragging text to the end of an expression or CSS. (RICT-1257)</li>
<li>Fixed an issue that caused the cursor to misbehave while editing the name of an Aggregate. (RICT-1254)</li>
<li>Fixed a crash when editing a module while Service Studio was stopped in a breakpoint. (RICT-1278)</li>
<li>Fixed a security vulnerability. CVSS v3.0 score 7.1 (High) (RLIT-2388)</li>
<li>Fixed a runtime error running Aggregates for very rare situations when the Entity internal name is a reserved keyword. (RSBO-29)</li>
<li>Fixed a bug that occasionally crashed Service Studio while upgrading an OML. (RCOT-2128)</li>
<li>Fixed a crash in the Compare and Merge window when opening a SQL element. (RCOT-2153)</li>
<li>Fixed a crash that occurred when double-clicking a verify message. (RICT-1258)</li>
<li>Improved the stability by fixing an occasional bug when selecting the cells of Widgets. (RICT-1250)</li>
<li>Fixed a crash that happened while undoing the delete of a widget having the Input Widget property set. (RICT-1243)</li>
<li>Fixed a crash in the preview of Service Studio when manipulating List Record widgets. (RICT-1240)</li>
<li>Improved the stability by fixing the Web Screens merge, related to several scenarios. (RICT-1237)</li>
<li>Fixed an issue in the SQL window that was causing part of the window to be hidden after resizing its sections. (RIUT-618)</li>
<li>Fixed an issue that was causing the Search box to close unexpectedly right after opening. (RIUT-648)</li>
<li>Fixed a crash editing Aggregates when using option "Show <n> hidden". (RPD-3842)</n></li>
<li>Improved the experience when there is a problem contacting the server to fetch the latest Application Templates. (RTAF-88)</li>
</ul><div class="hidden" id="development-environment-r.13_end"></div><div class="hidden" id="development-environment-r.12_start"></div>

<h2 id="development_environment_release_12">Development Environment Release 12</h2>
<div class="info">

Released on Jan 25, 2019
</div>
<h3 id="new_in_development_environment_release_12">New in Development Environment Release 12</h3>
<ul>
<li>There's now a warning dialog if you try to create a Screen based on an incompatible Screen Template. (RAFT-1737)</li>
<li>Improved the experience of adding a preview image to a custom template screen. (RAFT-1756)</li>
<li>New screen icons while developing screen templates in Service Studio. (RAFT-1657)</li>
<li>We improved the incompatibility warning message in the New Screen window. There are now more details about the Theme that you need to use with the selected Screen Template. (RAFT-1736)</li>
<li>Deprecated VerifySqlLiteral action from Sanitization.xif in favor of BuildSafe_InClauseIntegerList and BuildSafe_InClauseTextList. Both actions will be available in the next release of Platform Server. (RRCT-2108)</li>
<li>Forge Updates popup now better shows application names and has tooltips for more details. (RIUT-603)</li>
<li>Added a warning when the argument passed to a SQL Query Parameter with the Expand Inline set starts with "EncodeSql". Also added a warning when the argument passed to a SQL Query Parameter with the Expand Inline set uses the built-in function Replace. Both scenarios are prone to cause runtime errors. (RRCT-2116)</li>
</ul>
<h3 id="bug_fixing_release_12">Bug Fixing</h3>
<ul>
<li>Fixed unescaped strings in the generated translated javascript code. (RPD-3483)</li>
<li>Solved a problem that resulted in corrupted expressions. (RICT-1230)</li>
<li>Fixed an issue that occurred when performing Step Over multiple times while debugging. (RICT-1226)</li>
<li>Fixed a runtime error consuming SOAP Web Services that was causing the value of <simplecontent> elements to be ignored. (RINT-3275)</simplecontent></li>
<li>Adding an optional attribute to a Structure is now correctly identified as an incompatible change if that attribute is a Structure, Entity, Record or List. (ABE-1335)</li>
<li>Fixed a bug that allowed Client Entities and Read-Only Reference Entities to be used as Event Trigger. (ABE-1351)</li>
<li>Fixed a bug that allowed Client Entities to be used as Destination in Human Activities. (ABE-1354)</li>
<li>Fixed a crash occurring after editing the style of an element using Styles Editor. (ABE-1355)</li>
<li>Fixed a crash when opening the "Test Inputs" tab of a SQL element. (RAFT-1767)</li>
<li>Fixed a crash when selecting text while comparing and merging screens or blocks. (RCOT-2134)</li>
<li>Fixed a crash in the preview of Service Studio when manipulating List Record widgets. (RICT-1240)</li>
<li>Fixed a crash when merging web screens. (RICT-1237)</li>
</ul><div class="hidden" id="development-environment-r.12_end"></div><div class="hidden" id="development-environment-r.11_start"></div>

<h2 id="development_environment_release_11">Development Environment Release 11</h2>
<div class="info">

Released on Jan 17, 2019
</div>
<h3 id="new_in_development_environment_release_11">New in Development Environment Release 11</h3>
<ul>
<li>You can now create your own Screen Templates. Clone Custom Screen Templates Module for <a href="https://www.outsystems.com/forge/component-overview/5089/custom-screen-templates-web" target="_blank" rel="noopener noreferrer">web</a> or <a href="https://www.outsystems.com/forge/component-overview/5060/custom-screen-templates-mobile" target="_blank" rel="noopener noreferrer">mobile</a> from Forge, add Screen Templates to a Flow and publish. (RAFT-1765)</li>
</ul>
<h3 id="bug_fixing_release_11">Bug Fixing</h3>
<ul>
<li>Fixed a bug that allowed Client Entities to be used as Destination in Human Activities. (ABE-1354)</li>
<li>There's no crash now when you move the mouse pointer over Table Headers during merge. (RCOT-2119)</li>
</ul><div class="hidden" id="development-environment-r.11_end"></div><div class="hidden" id="development-environment-r.10_start"></div>

<h2 id="development_environment_release_10">Development Environment Release 10</h2>
<div class="info">

Released on Jan 07, 2019
</div>
<h3 id="new_in_development_environment_release_10">New in Development Environment Release 10</h3>
<ul>
<li>We removed the focus border around the list of the Screen Templates in the New Screen window. (RAFT-1750)</li>
<li>There's now a warning dialog if you try to create a Screen based on an incompatible Screen Template. (RAFT-1737)</li>
<li>We improved the incompatibility warning message in the New Screen window. There are now more details about the Theme that you need to use with the selected Screen Template. (RAFT-1736)</li>
<li>We improved the look and feel of the Service Studio dialog boxes, which now have a cleaner and lighter design. (RIUT-568)</li>
<li>You can now quickly identify and update the Forge components used in your factory from the applications list in Service Studio. Inspired by <a href="https://www.outsystems.com/ideas/1970/" target="_blank" rel="noopener noreferrer">Carlos' idea</a>. (RIUT-357)</li>
<li>You can now use the List_SortColumn_GetOrderBy function from RichWidgets in a SQL Query Parameter with the Expand Inline property enabled without triggering a SQL Injection warning message. (RRCT-2106)</li>
<li>We changed the SQL Injection warning message to advise you not to set the use of Expand Inline option to "Yes". The warning helps to follow solid SQL security practices. (RRCT-2128)</li>
<li>Upgraded SharpZipLib library to version 1.0.0. (RRCT-2144)</li>
</ul>
<h3 id="bug_fixing_release_10">Bug Fixing</h3>
<ul>
<li>We improved the stability of Service Studio by fixing an occasional crash related to the Run Server Action node. (ABE-1352)</li>
<li>We added the debugging support for the new iPhone devices (XR, XS, XS Max). (RAFT-1748)</li>
<li>Now it's again possible to set the name of a Block to empty. (RAFT-1680)</li>
<li>We fixed a bug that prevented the referenced elements in the merge window not to be selectable. (RCOT-1877)</li>
<li>Now resizing window when the screen DPI is configured over 100% no longer causes a glitch. (RICT-1216)</li>
<li>Fixed a crash when dropping an Entity Attribute of the picture binary type over a Form widget. (RICT-1211)</li>
<li>The introspection of the SOAP services containing the xsd:choice Element now works correctly. (RINT-3189)</li>
<li>Fixed a compilation error when publishing eSpaces with more that one SOAP consumes with complex types containing the same name. (RPD-3730)</li>
<li>Fixed 'RangeError: Maximum call stack size exceeded' when opening a Web Block or Web Screen. (RPD-3724)</li>
</ul><div class="hidden" id="development-environment-r.10_end"></div><div class="hidden" id="development-environment-r.9_start"></div>

<h2 id="development_environment_release_9">Development Environment Release 9</h2>
<div class="info">

Released on Jan 02, 2019
</div>
<h3 id="new_in_development_environment_release_9">New in Development Environment Release 9</h3>
<ul>
<li>Clicking Environment/Module Management in the toolbar now opens Service Center in the default browser instead of render it directly inside Service Studio. (RICT-825)</li>
<li>Upgraded SharpZipLib library to version 1.0.0. (RRCT-2144)</li>
<li>Upgraded Microsoft.AspNet.WebApi libraries to version 5.2.7. (RRCT-2143)</li>
</ul>
<h3 id="bug_fixing_release_9">Bug Fixing</h3>
<ul>
<li>Fixed a runtime error deserializing the body of a SOAP Web Service reply message when the element type inherits by restriction. (RINT-3239)</li>
<li>Fixed the conversion of nil values for numerical types when consuming SOAP Web Services. (RINT-3287)</li>
<li>Pressing F1 on UI Flows now redirects to the correct documentation page. (RAFT-1740)</li>
<li>Fixed a crash when importing SOAP Web Services with xsd:attributes used by reference. (RINT-3220)</li>
</ul><div class="hidden" id="development-environment-r.9_end"></div><div class="hidden" id="development-environment-r.8_start"></div>

<h2 id="development_environment_release_8">Development Environment Release 8</h2>
<div class="info">

Released on Dec 27, 2018
</div>
<h3 id="new_in_development_environment_release_8">New in Development Environment Release 8</h3>
<ul>
<li>Improved message shown after cloning a module. (RAFT-1658)</li>
</ul>
<h3 id="bug_fixing_release_8">Bug Fixing</h3>
<ul>
<li>When consuming SOAP web services, WSDL files with anyType elements are now correctly detected as unsupported. (RINT-2176)</li>
<li>Fixed an issue that caused Service Studio to crash when you imported a WSDL file containing include elements. (RINT-3124)</li>
<li>Fixed an issue that caused Service Studio to crash when you imported a WSDL file containing choice elements with sequence elements inside. (RINT-3235)</li>
<li>Changes in the license of an environment now correctly propagate to applications running in containers. (RSCT-1378)</li>
<li>Fixed an issue that caused Service Studio to crash when you opened a module with another module already open. (RAFT-1711)</li>
<li>Using an invalid HTML attribute name as a Widget's Extended Property no longer causes Service Studio to crash. (RICT-1183)</li>
</ul><div class="hidden" id="development-environment-r.8_end"></div><div class="hidden" id="development-environment-r.7_start"></div>

<h2 id="development_environment_release_7">Development Environment Release 7</h2>
<div class="info">

Released on Dec 19, 2018
</div>
<h3 id="new_in_development_environment_release_7">New in Development Environment Release 7</h3>
<ul>
<li>The shortcut Ctrl+N executed in a Flow now creates an empty Screen. Previously this shortcut opened the New Screen window. (RAFT-1616)</li>
<li>The icon picker in the Web application development is now the same as the one in Mobile. Plus, you'll get this new experience when selecting a Static Record item, both in Web and Mobile. Inspired by <a href="https://www.outsystems.com/ideas/2999/icon-picking-in-web-application-just-like-the-mobile-one" target="_blank" rel="noopener noreferrer">Bruno Fonte's idea</a>. (RAFT-1607)</li>
<li>You can now use the arrows keys and the Tab key to navigate the Screen Templates inside the New Screen window. (RAFT-1673)</li>
<li>Improved the 1-Click Publish performance of modules containing references without entities or structures. (ABE-1275)</li>
</ul>
<h3 id="bug_fixing_release_7">Bug Fixing</h3>
<ul>
<li>We fixed an array compilation error in the SOAP web services that prevented module publishing. This affected only applications with the new SOAP implementation. (RPD-3627)</li>
<li>Fixed crash that sometimes happened when using Test in the SQL node. (ABE-1322)</li>
<li>We improved the stability of Service Studio by resolving an issue that sometimes crashed the IDE after creating a local variable. The fix involved changing the underlying enumeration. (ABE-1323)</li>
<li>We improved the stability by fixing the way Service Studio handles errors in communicating with the server. (ABE-1330)</li>
<li>Now Service Studio doesn't crash after running Ctrl+F in the Executed SQL aggregate window. Thanks to Matheus Medeiros for <a href="https://www.outsystems.com/ideas/5925/" target="_blank" rel="noopener noreferrer">reporting the bug</a>. (ABE-1331)</li>
<li>Fixed a crash that happened when quickly deleting several sources in an Aggregate. (ABE-1333)</li>
<li>Fix a crash that occurred when changing the width from "auto" to other value in Styles Editor. (RAFT-1720)</li>
<li>Now Service Studio doesn't crash while you're on an Android device debugging an app that opens the external links within the in-app browser. (RAFT-1712)</li>
<li>Fixed a bug that crashed Service Studio while offline and trying to select a module in the Debugger &gt; Debug Setup &gt; Entry Module. (RAFT-1702)</li>
<li>Now it's possible to merge translation messages because we fixed the related UI issues. (RCOT-1964)</li>
<li>Fixed a bug to improve stability during the auto-save. (RICT-1146)</li>
<li>Fixed a bug that crashed Service Studio after opening a context menu with the Assign tools selected. (RIUT-549)</li>
</ul><div class="hidden" id="development-environment-r.7_end"></div><div class="hidden" id="development-environment-r.6_start"></div>

<h2 id="development_environment_release_6">Development Environment Release 6</h2>
<div class="info">

Released on Dec 03, 2018
</div>
<h3 id="new_in_development_environment_release_6">New in Development Environment Release 6</h3>
<ul>
<li>You can now use "Find Usages in All Modules" with Role Actions. Inspired by <a href="https://www.outsystems.com/ideas/5807/" target="_blank" rel="noopener noreferrer"> Carlos Alfaro's idea</a>. (RIUT-533)</li>
<li>From now on, double-clicking an Assign element containing a single assignment opens the expression editor and lets you edit that assignment. Inspired by <a href="https://www.outsystems.com/ideas/5299/" target="_blank" rel="noopener noreferrer"> Nicolaas' idea</a>. (RIUT-479)</li>
<li>Simplified the experience of opening a consumer module from a publish warning. Now Manage Dependencies window only opens if needed. (RIUT-481)</li>
</ul>
<h3 id="bug_fixing_release_6">Bug Fixing</h3>
<ul>
<li>Publishing a module with TrueChange errors in View Data aggregated attributes no longer causes a compilation error. (RPD-3568)</li>
<li>Publishing a Module after using the Disable Element feature to disable an Aggregate/SQL query that uses a deleted Entity as a Source no longer causes a crash. (RPD-3549)</li>
<li>You can now use Tab and arrows keys to navigate inside the Screen Templates browser. (RAFT-1673)</li>
<li>Textual merge capability is now extended to translation messages. Fixed display issues with translations in merge context. (RCOT-1964)</li>
<li>Fixed a bug that caused a crash while comparing WebBlock instances. (RCOT-1879)</li>
<li>Solved Service Studio freezes when debugging applications. (RICT-902)</li>
<li>Fixed an issue that caused Service Studio to freeze when testing Aggregates or SQL queries. (RICT-1139)</li>
</ul><div class="hidden" id="development-environment-r.6_end"></div><div class="hidden" id="development-environment-r.5_start"></div>

<h2 id="development_environment_release_5">Development Environment Release 5</h2>
<div class="info">

Released on Nov 26, 2018
</div>
<h3 id="new_in_development_environment_release_5">New in Development Environment Release 5</h3>
<ul>
<li>It's no longer possible to select MySQL as the database platform when creating an extension in Integration Studio since MySQL is only supported in OutSystems 11 as an external database. (RINT-2872)</li>
</ul>
<h3 id="bug_fixing_release_5">Bug Fixing</h3>
<ul>
<li>Fixed a crash in mobile apps when dropping over a widget and the modifier keys Shift or Control were pressed. (RICT-1119)</li>
<li>We fixed a bug that prevented you from installing Charts or OutSystems Now from Forge in some situations, causing the message "Application cannot be safely installed in your environment" to show. (ABE-1289)</li>
<li>You can now set OutSystems to reject the requests for non-supported image formats. In "Factory Configuration" Forge component, go to Security and check the option "Enforce Valid Image Formats on Image and Binary Endpoints". The valid image formats are GIF, PNG, and JPEG. The setting applies to the images the end-users upload through the applications created in OutSystems. (RRCT-2002)</li>
<li>Recovering a module will now correctly validate calculated attributes that reference a group by attribute in an aggregate. (RPD-3599)</li>
<li>Fixed an issue that would override the name of a new screen when created through a "link to new screen" within a List Item. (RAFT-1670)</li>
<li>Extended the search of widgets to support keywords so that the search "textarea" or "text area" returns the widget Text Area for web applications and the Text Area and Input widgets for mobile applications. (RAFT-1671)</li>
<li>Textual merge capability is now extended to translation messages. Fixed display issues with translations in merge context. (RCOT-1964)</li>
<li>Service Studio no longer crashes when you convert a REST variable (Local Variable, Input Parameter or Output Parameter) to another type of REST variable. (RICT-1125)</li>
<li>In the Aggregate editor, it is now possible to click the "navigate to"/eye icon for a Source that no longer exists in the Module without causing a crash. (RICT-1124)</li>
<li>Dragging multiple Entities to an Entity Diagram that contains a Comment element no longer causes a crash. (RICT-1123)</li>
<li>Using Manage Dependencies to add a reference to a nested Web Block no longer adds unnecessary references. (RPD-3521)</li>
<li>Fixed an intermittent merge issue that caused a crash while merging an action with errors. (RICT-1072)</li>
<li>Solved Service Studio freezes when debugging applications. (RICT-902)</li>
<li>Fixed a crash opening the context menu in a selected part of a flow when a connector was selected before a node. (RIUT-532)</li>
<li>Fixed Service Studio hang when opening Manage Dependencies window. (RPD-3612)</li>
</ul><div class="hidden" id="development-environment-r.5_end"></div><div class="hidden" id="development-environment-r.4_start"></div>

<h2 id="development_environment_release_4">Development Environment Release 4</h2>
<div class="info">

Released on Nov 07, 2018
</div>
<h3 id="new_in_development_environment_release_4">New in Development Environment Release 4</h3>
<ul>
<li>Removed the "Choose template" step for the creation of Service Applications. (ABE-1203)</li>
<li>You can now create a Static Record, a Parameter or a Variable by pressing Ctrl+N when an element of the same type is selected, or by right-clicking on an existing element of the desired type. Inspired by <a href="https://www.outsystems.com/ideas/4926/" target="_blank" rel="noopener noreferrer">Johan den Ouden's idea</a>. (ABE-1282)</li>
<li>We improved the tooltip that shows when you hover over the tree toggle button. It now says "Show Widget Tree" or "Show Elements Tree", depending on the action if performs. (ABE-1287)</li>
<li>The flow now reconnects whenever possible after you use the Disable Elements command to "comment out" parts of the flow. Inspired by <a href="https://www.outsystems.com/ideas/5639/" target="_blank" rel="noopener noreferrer"> Eric Bulters' idea</a>. (RIUT-488)</li>
<li>If the text value of a property has several lines, there's now a multiline indicator in form of a downwards arrow in the Properties Pane. Inspired by <a href="https://www.outsystems.com/ideas/3667/" target="_blank" rel="noopener noreferrer">Takeshi Kurimoto's idea</a>. (RIUT-466)</li>
<li>You can now save multiple items from the Resources to your computer. Select the elements you want to export in Data &gt; Resources, right-click and choose "Save Resources As…". Inspired by <a href="https://www.outsystems.com/ideas/700/" target="_blank" rel="noopener noreferrer">Pedro Gonçalves' idea</a>. (RIUT-467)</li>
<li>Now labels in flow connectors are shown in the middle of the arrow. Inspired by <a href="https://www.outsystems.com/ideas/5106/" target="_blank" rel="noopener noreferrer">João Pedro Bernardes' idea</a>. (RIUT-465)</li>
<li>We made the label for splitting of the Assign values more explicit, so now it says "Split all below into new Assign". Thanks for your continuous feedback! (RIUT-462)</li>
<li>Now publishing a module to a Production environment requires confirmation. Inspired by <a href="https://www.outsystems.com/ideas/1709/" target="_blank" rel="noopener noreferrer">Justin James' idea</a>. (RIUT-420)</li>
<li>The User and Role exceptions are now sorted alphabetically. Inspired by <a href="https://www.outsystems.com/ideas/5103/" target="_blank" rel="noopener noreferrer">Rebecca Hall's idea</a>. (RIUT-480)</li>
<li>Now there's a warning during an introspection of a WSDL, if it contains an attributeGroups element. (RINT-2759)</li>
</ul>
<h3 id="bug_fixing_release_4">Bug Fixing</h3>
<ul>
<li>We fixed a bug that prevented you from installing Charts or OutSystems Now from Forge in some situations, causing the message "Application cannot be safely installed in your environment" to show. (ABE-1289)</li>
<li>Fixed a user interface glitch that prevented the "Executed SQL" pane to shows when you run a query through the SQL tool in Service Studio connected to a non-production environment. (ABE-1297)</li>
<li>The Users application now shows the correct number of users with a role in an application. (RLIT-2274)</li>
<li>The label of the SQL tool under the output element now shows "Output Entity" or "Output Structure", depending on what you select in the pane. (ABE-1280)</li>
<li>Fixed a crash that happened after you used '@' within quotations in an SQL expression of the SQL tool. (ABE-1291)</li>
<li>We fixed an issue with the New Screen window, so it's now possible to create an Empty Screen even when the fetching of the Screen Templates fails. (RAFT-1653)</li>
<li>Fixed a crash that happened occasionally after performing an operation (e.g. right-click) on the HTML Element widget that had a Tag property that did not support children (e.g. "input"). (RAFT-885)</li>
<li>Fixed a problem with parsing the command line arguments when the command line contains paths with spaces (e.g: when Service Studio tries to recover a module after a crash). (RICT-1117)</li>
<li>Fixed a problem that prevented a module from being saved when a public web block used the identifier of a non-public entity. (RPD-3544)</li>
<li>Fixed a crash that happened when you tried to use a referenced Action in the Expression Editor. (RICT-1118)</li>
<li>The target installation environment now remains the same during the installation of apps from Forge, even if you change the environment in Service Studio in the middle of the installation process. (RIUT-483)</li>
<li>We fixed a bug that sometimes caused an error after submitting feedback. (RIUT-504)</li>
<li>We fixed a crash that happened after you searched for Attributes that were not refreshed in modules that consumed the parent Entity or Structure. (RIUT-503)</li>
<li>Fixed a bug that caused new lines to be removed in comments after editing. (RIUT-485)</li>
<li>Fixed an issue that caused a crash when using "Find Usages in all Modules" and when a consumer module is opened in more than one tab. (RIUT-482)</li>
<li>Fixed Service Studio hang while opening Manage Dependencies in a Mobile module. (RPD-3569)</li>
</ul><div class="hidden" id="development-environment-r.4_end"></div><div class="hidden" id="development-environment-r.3_start"></div>

<h2 id="development_environment_release_3">Development Environment Release 3</h2>
<div class="info">

Released on Oct 22, 2018
</div>
<h3 id="new_in_development_environment_release_3">New in Development Environment Release 3</h3>
<ul>
<li>We improved the tooltip text that shows while you are dragging Entity Attributes over widgets. It's now more clear what you can do if you drop an Attribute onto, for example, a Table Record or Edit Record. (RAFT-1600)</li>
</ul>
<h3 id="bug_fixing_release_3">Bug Fixing</h3>
<ul>
<li>The label of the SQL tool under the output element now shows "Output Entity" or "Output Structure", depending on what you select in the pane. (ABE-1280)</li>
<li>Fixed the folder tree in Service Studio so it no longer shows Client Actions after converting a mobile module to a Service module. (ABE-1281)</li>
<li>Fixed drag drop of an entity or attribute to the screen in a mobile module. (RAFT-1650)</li>
<li>Improved the preview image of the Empty Screen Template. (RAFT-1635)</li>
<li>Fixed a crash that occurred after you refreshed the references and the refresh resulted in the the removal of a block. (RAFT-1609)</li>
<li>Fixed an issue that caused the text cursor to disappear in some situations. (RAFT-1613)</li>
<li>Fixed an issue that caused a crash during merge operations while inspecting 'Database' element from consumed SOAP Services. (RCOT-2001)</li>
<li>Fixed a bug that caused a crash while comparing Web Block instances. (RCOT-1879)</li>
<li>Fixed an issue with Service Studio '-cleanup' command line option. Additionally, fixed the report generated when removing unused elements. (RPD-3526)</li>
</ul><div class="hidden" id="development-environment-r.3_end"></div><div class="hidden" id="development-environment-r.2_start"></div>
<h2 id="development_environment_release_2">Development Environment Release 2</h2>
<div class="info">

Released on Oct 09, 2018
</div>
<h3 id="new_in_development_environment_release_2">New in Development Environment Release 2</h3>
<ul>
<li>From now on, you can quickly create a new screen when defining a button or link destination. Inspired by <a href="https://www.outsystems.com/ideas/5432/create-new-screen-when-adding-destination-node" target="_blank" rel="noopener noreferrer">Russell Codd's idea</a>. (RAFT-1605)</li>
</ul>
<h3 id="bug_fixing_release_2">Bug Fixing</h3>
<ul>
<li>Fixed a bug that sometimes caused an aggregate's preview data that contained Group Bys to grow horizontally instead of vertically. (ABE-1267)</li>
<li>Improved Empty Template's preview image. (RAFT-1635)</li>
<li>Fixed Service Studio crash after refreshing references that caused block's placeholders to be removed. (RAFT-1609)</li>
<li>Empty flow suggestion is no longer shown in a screen action. (RAFT-1602)</li>
<li>Fixed an issue that caused the Extensibility Configuration property in mobile modules to have an error in True Change when empty. (RAFT-1598)</li>
<li>On some situations related with Aggregate sources manipulation, a conflict would appear on merge in the Actions containing the Aggregate, but drilling down, nothing appeared to be changed. With this fix, merge will not consider these "false" conflicts. (RCOT-1941)</li>
<li>Fixed a bug that caused a crash while comparing WebBlock instances. (RCOT-1879)</li>
<li>Fixed a bug related with not being able to correctly match elements in merge. (RCOT-1375)</li>
<li>Fixed a bug where merging a hidden reference only present on base version would crash merge operation. (RPD-3173)</li>
<li>Fixed bug that did not recover resolution on textual conflicts when restoring a merge operation. (RCOT-1755)</li>
</ul>
<div class="hidden" id="development-environment-r.2_end"></div><div class="hidden" id="development-environment-r.1_start"></div>

<h2 id="development_environment_release_1">Development Environment Release 1</h2>
<div class="info">

Released on Sept 26, 2018
</div>
<h3 id="new_in_development_environment_release_1">New in Development Environment Release 1</h3>
<h4 id="highlights_release_1">Highlights</h4>
<ul>
<li>Developers are able to create new screens based on templates that were previously made available in the factory. (RAFT-1023)</li>
<li>Now you can quickly replace a UI data source by dragging other entity to the corresponding widget, such as a List or a Form. (RAFT-1388)</li>
<li>You can now disable part of the logic flow. Select some elements of the flow, right-click and choose "Disable Elements". Inspired by <a href="https://www.outsystems.com/ideas/57/" target="_blank" rel="noopener noreferrer"><u>Joost's idea</u></a>. (RIUT-7)</li>
<li>Now it's possible to organize the application elements such as Entities, Structures, Images, and Resources into folders. Inspired by <a href="https://www.outsystems.com/ideas/784/" target="_blank" rel="noopener noreferrer"><u>Robert's idea</u></a>. (RIUT-319)</li>
<li>You can now move Actions to a different folder without breaking the consumer references. Inspired by <a href="https://www.outsystems.com/ideas/1393/" target="_blank" rel="noopener noreferrer"><u>Justin James' idea</u></a>. (RICT-800)</li>
<li>You can now use inline values as inputs for the structured types. This enables you to conveniently provide, for example, sample values to charts. Inspired by <a href="https://www.outsystems.com/ideas/2738/" target="_blank" rel="noopener noreferrer"><u>Hans Dollen's idea</u></a>. (RICT-821)</li>
<li>After publishing your module, you can now quickly open the outdated consumer modules by right-clicking the warning. Inspired by <a href="https://www.outsystems.com/ideas/250/" target="_blank" rel="noopener noreferrer"><u>Robert's idea</u></a>.</li>
<li>You can now use ListDistinct, a new client and server action. The action removes duplicates from the list. Inspired by <a href="https://www.outsystems.com/ideas/2830/" target="_blank" rel="noopener noreferrer"><u>Carlos Henriques' idea</u></a>. (RCOT-1108)</li>
<li>Service Studio now runs on 64-bit. This improves performance and enables you to use your computer resources more efficiently when working with many modules. (RICT-140)</li>
<li>Mac users can now use a new Technical Preview of Service Studio for Mac. Inspired by <a href="https://www.outsystems.com/ideas/1036/" target="_blank" rel="noopener noreferrer"><u>Miguel's idea</u></a>. (RICT-908)</li>
</ul>
<h4 id="architecture_release_1">Architecture</h4>
<ul>
<li>Added a new application and module type (Services) to promote a better application segmentation and governance. (ABE-1276)</li>
<li>Added a new language element (Service Action) which is a loosely coupled action (REST underneath) with impact analysis and security by default. (ABE-1277)</li>
<li>Optional parameters and attributes do not require refreshing consumers, making larger systems more loosely coupled and allowing independent teams to release more often without impacting each other. (ABE-1278)</li>
<li>Public Screens are now loosely coupled that results in no circular references in dependency analysis. (ABE-1279)</li>
</ul>
<h4 id="interface_release_1">Interface</h4>
<ul>
<li>Web Blocks now support Events and Event Handlers to propagate changes to their parent element. Inspired by <a href="https://www.outsystems.com/ideas/1549/Notify+improvements" target="_blank" rel="noopener noreferrer"><u>Joost Landgraf's idea</u></a>. (RAFT-1371)</li>
<li>You can now drag an Entity attribute to an Expression inside a widget with a data source (e.g. TableRecords) to update the Expression automatically. (RAFT-1505)</li>
<li>We improved the visibility of the indicator that shows where the widget will be dropped while you are dragging it. (RAFT-1403)</li>
<li>Check Box, Combo Box, Input, Input Password, List Box and Radio Button Web widgets will now be created with new default classes. (RAFT-1297)</li>
<li>UI blocks can now have sample content in their placeholders to accelerate the development and make them easier to use. (RAFT-1069)</li>
<li>New method registerDeviceClassGetter added to JS Public API allows to change the default behavior of adapting the css classes applied to the device resolution. By default, resolution higher than 1024px are considered tablets. (RAFT-1296)</li>
<li>Styles Editor now supports grid units (e.g. "2 col") and you can use it without a local theme. Also, the widget styles are now generated as the inline CSS, which gives you more freedom when editing a module. (RICT-663)</li>
<li>We upgraded the internal browser of Service Studio. This improves the WYSIWYG editor and enables you to have a more accurate preview of screens and blocks. (RICT-35)</li>
</ul>
<h4 id="compare and merge_release_1">Compare and Merge</h4>
<ul>
<li>Revamped the look and feel of the merge feature. The "Compare and Merge" window brings a new user experience and more powerful options. (RCOT-1332)</li>
<li>The navigation buttons of the "Compare and Merge" window now have look and feel similar to the other parts of Service Studio. (RCOT-1637)</li>
<li>When you resolve conflicts in "Compare and Merge" window by clicking the check box, the highlight changes to blue to confirm the resolution. (RCOT-1606)</li>
<li>The values of the properties inside elements (for example, a variable value in the Assign tool, SQL expressions, descriptions, text in widgets...) are now accessible during the merge process. (RCOT-1556)</li>
<li>“Highlight all differences” check box in the text merge pane to toggle between showing all differences and conflicts only. (RCOT-1179)</li>
<li>Textual elements in the merge process have the “merged” or “merged with conflicts” description tag that indicates the merge status. (RCOT-1241)</li>
</ul>
<h4 id="soap_release_1">SOAP</h4>
<ul>
<li>Added support for SOAP 1.2 web services.  Inspired by <a href="https://www.outsystems.com/ideas/2281/" target="_blank" rel="noopener noreferrer"><u>Carlos's idea</u></a>. (RINT-618)</li>
<li>The SOAP 1.2 implementation now has an extensibility callback. Inspired by <a href="https://www.outsystems.com/ideas/784/" target="_blank" rel="noopener noreferrer"><u>Matthias's idea</u></a>. (RINT-1539)</li>
<li>It is now possible to see and select available methods to import when configuring the consumption of a SOAP Web Service. Inspired by <a href="https://www.outsystems.com/ideas/1692/" target="_blank" rel="noopener noreferrer"><u>Davide's idea</u></a>. (RINT-1027)</li>
<li>It is now possible to define the authentication type and the corresponding credentials for an imported SOAP 1.2 web service. <a href="https://www.outsystems.com/ideas/3284/" target="_blank" rel="noopener noreferrer"><u>Darren's idea</u></a>. (RINT-1225)</li>
<li>Experience for SOAP 1.2 web services consume improved. Inspired by <a href="https://www.outsystems.com/ideas/137/" target="_blank" rel="noopener noreferrer"><u>João's idea</u></a>. (RINT-1025)</li>
<li>SOAP Web Service Methods now support default values in Input Parameters, Output Parameters and Structure Attributes of SOAP Web Services. The minOccurs/nillable WSDL attributes are now taken into consideration when determining mandatory Input Parameters and Structure Attributes. (RINT-1833)</li>
<li>Users are now notified when attempting to consume SOAP web services that contain unsupported features. (RINT-1299)</li>
<li>It is now possible to refresh a SOAP Web Service by right-clicking it in Service Studio to have access to the updated list of Methods. (RINT-1139)</li>
<li>It is now possible to see and select available services and bindings to import when configuring the consumption of a SOAP Web Service. (RINT-1026)</li>
<li>It is now possible to dynamically authenticate with different credentials per SOAP 1.2 web service method. (RINT-900)</li>
<li>Added support for consuming SOAP web services with Choices. (RINT-1776)</li>
<li>Added SOAP 1.2 support for types created via "restriction", usually of the same type as the original type. Only the "maxLength" and "fractionDigits" restrictions are considered when creating the appropriate data types, and these restrictions will not be enforced at runtime. (RINT-854)</li>
<li>Added support for consuming SOAP web services with nillable attributes. (RINT-835)</li>
</ul>
<h4 id="more_release_1">More</h4>
<ul>
<li>Added capability of sorting filter conditions in Aggregates. Inspired by <a href="https://www.outsystems.com/ideas/1932" title="https://www.outsystems.com/ideas/1932" target="_blank" rel="noopener noreferrer">Justin James' idea</a>. (ABE-846)</li>
<li>Moved Multilingual Locales folder from Interface Tab to Data Tab (ABE-1193)</li>
<li>Removed the need for writing '=True' (or '=False') for boolean variables in Aggregates. (e.g.: before: User.Is_Active = True --&gt; after: User.Is_Active). Inspired by <a href="https://www.outsystems.com/ideas/1556/" target="_blank" rel="noopener noreferrer"><u>Kilian's idea</u></a> (ABE-554)</li>
<li>Service Studio now shows a warning for modules that are set as self user provider but don't have "Is User Provider" set to "Yes" (RRCT-1584)</li>
<li>When editing the source code of extensions in Visual Studio, Integration Studio will now package the correct version of all runtime libraries (e.g. RuntimePlatform) with the code (the one used when the extension is published). (RSCT-1119)</li>
<li>Now you can override resources by name when importing resources via the command line ("-override"). (RICT-984)</li>
</ul>
<h3 id="bug_fixing_release_1">Bug Fixing</h3>
<ul>
<li>Fixed intermittent "Concurrent publication" error when following the "Build a Mobile/Web App in 5 min" tutorials. (RSCT-1357)</li>
</ul><div class="hidden" id="development-environment-r.1_end"></div><div class="hidden"><h1>Development Environment</h1></div>
