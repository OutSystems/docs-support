---
locale: en-us
guid: 9a1c0394-1a0a-4371-9a26-d22decf48b1c
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

<div class="hidden" id="odcstudio-1.0.33_start"></div>

<h2 id="odcstudio_1.0.33" >ODCStudio 1.0.33</h2>
<div class="info"><p>Released on Dec 21, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_odcstudio_1.0.33" >Bug Fixing</h3>
<ul>
<li>Fixed an issue in Code Mentor logic suggestions where pasting text would cause an extra V character to be added. (RAID-1565)</li>
</ul>

<div class="hidden" id="odcstudio-1.0.33_end"></div><div class="hidden" id="odcstudio-1.0.32_start"></div>

<h2 id="odcstudio_1.0.32" >ODCStudio 1.0.32</h2>
<div class="info"><p>Released on Dec 12, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_odcstudio_1.0.32" >New in ODCStudio 1.0.32</h3>
<ul>
<li>Changed the order on Data Type dropdown so that the "Other" data types category appear immediately after the Basic Types. (RDOIAT-383)</li>
<li>Now, in the first publish after opening an app/library using the "Open from other revisions" command, the Version Conflict Dialog will often appear. Enabling users to properly override a revision, even when there are no conflicts with the published version.

Updated Version Conflict Dialog text to use the word "override" instead of "overwrite" to better describe its functionality. (RDPMBT-2237)</li>
</ul>
<h3 id="bug_fixing_odcstudio_1.0.32" >Bug Fixing</h3>
<ul>
<li>Fix properties scroll blocked on compare and merge editor. (RMAC-10591)</li>
<li>Fix losing focus while navigating the differences through keyboard in compare and merge editor. (RMAC-10623)</li>
<li>Fixed an issue that was causing Service Studio to open in another Windows user session.
This occurred when another windows user has Service Studio open, and the current one tries to open Service Studio as Administrator. (RMAC-10670)</li>
</ul>

<div class="hidden" id="odcstudio-1.0.32_end"></div><div class="hidden" id="odcstudio-1.0.31_start"></div>

<h2 id="odcstudio_1.0.31" >ODCStudio 1.0.31</h2>
<div class="info"><p>Released on Dec 05, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_odcstudio_1.0.31" >New in ODCStudio 1.0.31</h3>
<ul>
<li>Developers can now easily find embedded examples to help them create Aggregates using natural language. (RAID-1689)</li>
<li>While publishing a mobile app that already had a mobile package generated and the publish has changes that require a new mobile package generation, a message indicating that the new mobile package is being generated is shown during the publish process. (RDPMBT-2129)</li>
<li>Now the user will be prompted with the version conflict dialog during the publishing process after opening the current app or library from the "Open other revisions" command. This will happen when the user is not merging with himself and there are any change between revisions. (RDPMBT-2207)</li>
<li>Auto-generated comments for OnBeforeRequest and OnAfterResponse REST callbacks have been improved. (RTAFB-6061)</li>
</ul>
<h3 id="bug_fixing_odcstudio_1.0.31" >Bug Fixing</h3>
<ul>
<li>Fix a silent crash on the Code Mentor logic suggestions. (RAID-1746)</li>
<li>Fixed an issue affecting AI-powered suggestions. (RAID-1750)</li>
</ul>

<div class="hidden" id="odcstudio-1.0.31_end"></div><div class="hidden" id="odcstudio-1.0.30_start"></div>

<h2 id="odcstudio_1.0.30" >ODCStudio 1.0.30</h2>
<div class="info"><p>Released on Nov 24, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_odcstudio_1.0.30" >New in ODCStudio 1.0.30</h3>
<ul>
<li>Developers are now able to disable the Aggregates generation based on natural language, from the Preferences menu. (RAID-1693)</li>
<li>It is now possible to automatically convert a JSON Deserialize node data type from Record to Structure. (RDEV-5145)</li>
<li>ODC Studio now displays an informative message during a 1-Click Publish when the changes performed in said publish require a new mobile package to be generated. (RDPMBT-2009)</li>
</ul>
<h3 id="bug_fixing_odcstudio_1.0.30" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the ODC icon to appear in the About dialog without the lighter border. (RDEV-5146)</li>
</ul>

<div class="hidden" id="odcstudio-1.0.30_end"></div><div class="hidden" id="odcstudio-1.0.29_start"></div>

<h2 id="odcstudio_1.0.29" >ODCStudio 1.0.29</h2>
<div class="info"><p>Released on Nov 21, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_odcstudio_1.0.29" >Bug Fixing</h3>
<ul>
<li>Fixed typo on the Smart Guidance screen (RAID-1732)</li>
<li>Fixed an issue when comparing modules from LifeTime where the running Service Studio would not be reused. (RMAC-10076)</li>
</ul>

<div class="hidden" id="odcstudio-1.0.29_end"></div><div class="hidden" id="odcstudio-1.0.28_start"></div>

<h2 id="odcstudio_1.0.28" >ODCStudio 1.0.28</h2>
<div class="info"><p>Released on Nov 15, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_odcstudio_1.0.28" >New in ODCStudio 1.0.28</h3>
<ul>
<li>It is now possible to access Add Public Elements dialog through Database's context menu. (RDPMBT-2016)</li>
</ul>
<h3 id="bug_fixing_odcstudio_1.0.28" >Bug Fixing</h3>
<ul>
<li>Fixed the add public elements dialog size. (RDEV-5094)</li>
<li>Fixed an issue that caused the Theme Editor dialog to have the wrong width. (RDEV-5100)</li>
<li>Fixed issues with Copy, Paste and Delete shortcuts stopping working in some editors after executing undo operations (RMAC-10205)</li>
</ul>

<div class="hidden" id="odcstudio-1.0.28_end"></div><div class="hidden" id="service-studio-neo-1.0.27_start"></div>

<h2 id="service_studio_neo_1.0.27" >Service Studio Neo 1.0.27</h2>
<div class="info"><p>Released on Nov 04, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_service_studio_neo_1.0.27" >Bug Fixing</h3>
<ul>
<li>Fixed a bug that caused Service Studio to become irresponsible while clicking on widgets or flow nodes. (RMAC-10204)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.27_end"></div><div class="hidden" id="service-studio-neo-1.0.26_start"></div>

<h2 id="service_studio_neo_1.0.26" >Service Studio Neo 1.0.26</h2>
<div class="info"><p>Released on Oct 31, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.26" >New in Service Studio Neo 1.0.26</h3>
<ul>
<li>External connections now appear under the Entities folder on the Merge Dialog (RDPMBT-1822)</li>
</ul>

</ul>

<div class="hidden" id="service-studio-neo-1.0.26_end"></div><div class="hidden" id="service-studio-neo-1.0.25_start"></div>

<h2 id="service_studio_neo_1.0.25" >Service Studio Neo 1.0.25</h2>
<div class="info"><p>Released on Oct 24, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.25_end"></div><div class="hidden" id="service-studio-neo-1.0.24_start"></div>

<h2 id="service_studio_neo_1.0.24" >Service Studio Neo 1.0.24</h2>
<div class="info"><p>Released on Oct 13, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.24_end"></div><div class="hidden" id="service-studio-neo-1.0.23_start"></div>

<h2 id="service_studio_neo_1.0.23" >Service Studio Neo 1.0.23</h2>
<div class="info"><p>Released on Oct 10, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_service_studio_neo_1.0.23" >Bug Fixing</h3>
<ul>
<li>Fixed a bug in which the Widgets tree stopped responding when the opened screen was renamed. (RDPMBT-1870)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.23_end"></div><div class="hidden" id="service-studio-neo-1.0.22_start"></div>

<h2 id="service_studio_neo_1.0.22" >Service Studio Neo 1.0.22</h2>
<div class="info"><p>Released on Oct 03, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.22_end"></div><div class="hidden" id="service-studio-neo-1.0.21_start"></div>

<h2 id="service_studio_neo_1.0.21" >Service Studio Neo 1.0.21</h2>
<div class="info"><p>Released on Sep 26, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.21" >New in Service Studio Neo 1.0.21</h3>
<ul>
<li>Apple and Google stores only accept PNG app icons, so Studio is now enforcing that file format for Mobile App icons. (RDEV-4914)</li>
</ul>

</ul>

<div class="hidden" id="service-studio-neo-1.0.21_end"></div><div class="hidden" id="service-studio-neo-1.0.20_start"></div>

<h2 id="service_studio_neo_1.0.20" >Service Studio Neo 1.0.20</h2>
<div class="info"><p>Released on Sep 19, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.20" >New in Service Studio Neo 1.0.20</h3>
<ul>
<li>It is now possible to search for a specific shortcut in the keyboard shortcuts list (Help > Keyboard Shortcuts). (RDOIBT-817)</li>
<li>It is now possible to search for a specific shortcut in the keyboard shortcuts list (Help > Keyboard Shortcuts). (RDPMBT-1707)</li>
<li>Adds a new system server action UpdateUserProfile to update the logged in user name and photo on the identity provider. (RRCT-4621)</li>
</ul>
<h3 id="bug_fixing_service_studio_neo_1.0.20" >Bug Fixing</h3>
<ul>
<li>Fixed an issue with Logic Assistant where a crash would occur after a long period of unavailability. (RAID-1662)</li>
<li>Fixed crash when closing some dialog windows. (RDPMBT-1771)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.20_end"></div><div class="hidden" id="service-studio-neo-1.0.19_start"></div>

<h2 id="service_studio_neo_1.0.19" >Service Studio Neo 1.0.19</h2>
<div class="info"><p>Released on Sep 12, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.19" >New in Service Studio Neo 1.0.19</h3>
<ul>
<li>You will now be able to debug apps that redirect to external login providers, without losing the debug session. (RDPMBT-1516)</li>
<li>Updated the "Merge Conflicts Found" dialog's title, message, and buttons.
Now, the users are presented to three actions - "Overwrite with my revision", "Compare revisions" and "Cancel". 
The messages and title of the dialog were updated to have a more concise information about the merge process. (RDPMBT-1525)</li>
<li>It is now possible to copy Service Studio version information from the "About Service Studio" dialog. (RDPMBT-1705)</li>
</ul>
<h3 id="bug_fixing_service_studio_neo_1.0.19" >Bug Fixing</h3>
<ul>
<li>Fixed an issue with proxy authentication settings being ignored on requests made by some editors. (RDPMBT-1696)</li>
<li>Fixed an issue that caused image previews to overlap other properties. (RDPMBT-1697)</li>
<li>Fixed an issue that would hang the merge editor after un-resolving a textual conflict. (RDPMBT-1701)</li>
<li>Fixed and issue that caused widgets to always be pasted as the last child of the parent container, not respecting the caret position. (RMAC-10160)</li>
<li>Fixed an issue that would block certain users (with Identity Service Integration) from login into the OS environments through Service Studio 11.53.13.61176. (RMAC-10291)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.19_end"></div><div class="hidden" id="service-studio-neo-1.0.18_start"></div>

<h2 id="service_studio_neo_1.0.18" >Service Studio Neo 1.0.18</h2>
<div class="info"><p>Released on Sep 05, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.18" >New in Service Studio Neo 1.0.18</h3>
<ul>
<li>The merge experience is now smoother and will only ask your input to resolve conflicts when there are actually conflicts that need resolving. If Service Studio can do the merge automatically, it will happen automatically during the publish process and not need your intervention as before. (RDPMBT-1471)</li>
</ul>
<h3 id="bug_fixing_service_studio_neo_1.0.18" >Bug Fixing</h3>
<ul>
<li>Fixed an issue when opening an app or library (RDEV-4861)</li>
<li>Fix issue when opening module (RMAC-10163)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.18_end"></div><div class="hidden" id="service-studio-neo-1.0.17_start"></div>

<h2 id="service_studio_neo_1.0.17" >Service Studio Neo 1.0.17</h2>
<div class="info"><p>Released on Aug 29, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.17" >New in Service Studio Neo 1.0.17</h3>
<ul>
<li>Now, if you are working on both Producer and Consumer apps, on publishing the Producer, dependencies will be automatically refreshed in respective the Consumer apps. (RDEV-4482)</li>
</ul>

</ul>

<div class="hidden" id="service-studio-neo-1.0.17_end"></div><div class="hidden" id="service-studio-neo-1.0.16_start"></div>

<h2 id="service_studio_neo_1.0.16" >Service Studio Neo 1.0.16</h2>
<div class="info"><p>Released on Aug 22, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_service_studio_neo_1.0.16" >Bug Fixing</h3>
<ul>
<li>Fix issues on undo after a merge operation (RDPMBT-1604)</li>
<li>Fixed the dropping of a setting on an assign node. (RDPMBT-1666)</li>
<li>Fixed an issue that caused pasting old texts from the clipboard when pasting over button widgets. (RMAC-10146)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.16_end"></div><div class="hidden" id="service-studio-neo-1.0.15_start"></div>

<h2 id="service_studio_neo_1.0.15" >Service Studio Neo 1.0.15</h2>
<div class="info"><p>Released on Aug 15, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.15" >New in Service Studio Neo 1.0.15</h3>
<ul>
<li>It is now possible to use checkRole action in client actions and control UI logic based on permissions according to the role assigned (RDMST-1116)</li>
<li>It is now possible to use Grant and revoke action in server actions (RDMST-1133)</li>
<li>It is now possible to resize properties pane labels and input fields. (RDPMBT-1587)</li>
</ul>
<h3 id="bug_fixing_service_studio_neo_1.0.15" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented the menu box of some dropdown options to be closed when clicking in the arrow indicator.  (RDPMBT-1534)</li>
<li>Fixed an issue that prevented the user to type some special characters. (RMAC-10114)</li>
<li>Fixed an issue that caused double click on elements to not work (RMAC-10136)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.15_end"></div><div class="hidden" id="service-studio-neo-1.0.14_start"></div>

<h2 id="service_studio_neo_1.0.14" >Service Studio Neo 1.0.14</h2>
<div class="info"><p>Released on Aug 08, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_service_studio_neo_1.0.14" >New in Service Studio Neo 1.0.14</h3>
<ul>
<li>View Data now shows the icon of the type of Entity being viewed. (RIMPT-2870)</li>
</ul>
<h3 id="bug_fixing_service_studio_neo_1.0.14" >Bug Fixing</h3>
<ul>
<li>Dark Theme Dialogs now have for prominent border (RMAC-8342)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.14_end"></div><div class="hidden" id="service-studio-neo-1.0.13_start"></div>

<h2 id="service_studio_neo_1.0.13" >Service Studio Neo 1.0.13</h2>
<div class="info"><p>Released on Aug 01, 2022</p></div>

<h3 id="new_in_service_studio_neo_1.0.13" >New in Service Studio Neo 1.0.13</h3>
<ul>
<li>You can now test your REST consumption straight from Service Studio, just go to the "Test" tab inside your REST connection/action. (RDEV-4465)</li>
</ul>

</ul>

<div class="hidden" id="service-studio-neo-1.0.13_end"></div><div class="hidden" id="service-studio-neo-1.0.12_start"></div>

<h2 id="service_studio_neo_1.0.12" >Service Studio Neo 1.0.12</h2>
<div class="info"><p>Released on Jul 25, 2022</p></div>

<h3 id="bug_fixing_service_studio_neo_1.0.12" >Bug Fixing</h3>
<ul>
<li>Now tab's tooltip is hide when tab is closed (RMAC-10006)</li>
<li>Fixed an issue related with the comment's visibility in referenced screens. (RMAC-9059)</li>
<li>Fixed an issue that caused false positive warnings to be shown in JavaScript editor. (RMAC-9963)</li>
<li>Fixed an issue that caused the keyboard shortcuts CTRL+O and SHIFT+CTRL+O to not work when used within a module context. (RMAC-9995)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.12_end"></div><div class="hidden" id="service-studio-neo-1.0.11_start"></div>

<h2 id="service_studio_neo_1.0.11" >Service Studio Neo 1.0.11</h2>
<div class="info"><p>Released on Jul 18, 2022</p></div>

<h3 id="bug_fixing_service_studio_neo_1.0.11" >Bug Fixing</h3>
<ul>
<li>Fixed a crash in the Translations Editor when filtering translations. (RMAC-9977)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.11_end"></div><div class="hidden" id="service-studio-neo-1.0.10_start"></div>

<h2 id="service_studio_neo_1.0.10" >Service Studio Neo 1.0.10</h2>
<div class="info"><p>Released on Jul 11, 2022</p></div>

<h3 id="bug_fixing_service_studio_neo_1.0.10" >Bug Fixing</h3>
<ul>
<li>Fixed an error on Compare&Merge dialog when trying to merge and cancel at the same time. (RMAC-9731)</li>
<li>Fixed an issue on flow comments in which the text cursor would not be shown after clicking to edit the text. (RMAC-9935)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.10_end"></div><div class="hidden" id="service-studio-neo-1.0.9_start"></div>

<h2 id="service_studio_neo_1.0.9" >Service Studio Neo 1.0.9</h2>
<div class="info"><p>Released on Jul 04, 2022</p></div>

<h3 id="bug_fixing_service_studio_neo_1.0.9" >Bug Fixing</h3>
<ul>
<li>Fixed some content not being rendered in Service Studio like the content of the Tabs pattern (RMAC-9691)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.9_end"></div><div class="hidden" id="service-studio-neo-1.0.8_start"></div>

<h2 id="service_studio_neo_1.0.8" >Service Studio Neo 1.0.8</h2>
<div class="info"><p>Released on Jun 27, 2022</p></div>

<h3 id="bug_fixing_service_studio_neo_1.0.8" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a crash when a record or a list literal expression changes with the expression editor still open. (RMAC-9687)</li>
<li>The debugging session now prompts to stop if the user chooses to switch environments. (RMAC-9689)</li>
<li>Fixed an issue that caused the cursor to jump when editing names in the Properties panel. (RMAC-9813)</li>
</ul>

<div class="hidden" id="service-studio-neo-1.0.8_end"></div><div class="hidden" id="service-studio-neo-1.0.7_start"></div>

<h2 id="service_studio_neo_1.0.7" >Service Studio Neo 1.0.7</h2>
<div class="info"><p>Released on Jun 20, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.7_end"></div><div class="hidden" id="service-studio-neo-1.0.6_start"></div>

<h2 id="service_studio_neo_1.0.6" >Service Studio Neo 1.0.6</h2>
<div class="info"><p>Released on Jun 13, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.6_end"></div><div class="hidden" id="service-studio-neo-1.0.5_start"></div>

<h2 id="service_studio_neo_1.0.5" >Service Studio Neo 1.0.5</h2>
<div class="info"><p>Released on Jun 06, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.5_end"></div><div class="hidden" id="service-studio-neo-1.0.4_start"></div>

<h2 id="header-service-studio-neo-1.0.4" >Service Studio Neo 1.0.4</h2>
<div class="info"><p>Released on May 30, 2022</p></div>

This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.<div class="hidden" id="service-studio-neo-1.0.4_end"></div><h1>Service Studio Neo</h1>
<h2 id="service_studio_neo_1.0.0">Service Studio Neo 1.0.0</h2>
<div class="info"><p>Released on May 04, 2022</p></div>
<h3 id="bug_fixing_0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the dates in the "Changed" column to not be displayed in local time when the versions' table from the "Open other Version" window is loaded. (RDPMBT-1120)</li>
<li>Fix an issue that could occur when closing a module tab while the flow suggestions popup was about to be shown. (RMAC-9528)</li>
</ul>
<h2 id="service_studio_neo_0.9.9">Service Studio Neo 0.9.9</h2>
<div class="info"><p>Released on Apr 27, 2022</p></div>
<p>This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.</p>
<h2 id="service_studio_neo_0.9.8">Service Studio Neo 0.9.8</h2>
<div class="info"><p>Released on Apr 22, 2022</p></div>
<h3 id="bug_fixing_1">Bug Fixing</h3>
<ul>
<li>Fixed a crash when doing an automatic merge with changes on expressions with Text Literals (RMAC-9411)</li>
</ul>
<h2 id="service_studio_neo_0.9.7">Service Studio Neo 0.9.7</h2>
<div class="info"><p>Released on Apr 22, 2022</p></div>
<h3 id="bug_fixing_2">Bug Fixing</h3>
<ul>
<li>Fixed a crash when doing an automatic merge with changes on expressions with Text Literals (RMAC-9411)</li>
</ul>
<h2 id="service_studio_neo_0.9.6">Service Studio Neo 0.9.6</h2>
<div class="info"><p>Released on Apr 18, 2022</p></div>
<h3 id="new_in_service_studio_neo_0.9.6">New in Service Studio Neo 0.9.6</h3>
<ul>
<li>Improved icons in Entities and Structures. (RDEV-4277)</li>
<li>Users are now able to find all usages of a public element in all apps and libraries in their organization. (RDPMBT-559)</li>
<li>Service Studio Project Neo now allows users to clone an already existing app or library. (RDPMBT-921)</li>
</ul>
<h2 id="service_studio_neo_0.9.5">Service Studio Neo 0.9.5</h2>
<div class="info"><p>Released on Apr 08, 2022</p></div>
This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster.
Your work shouldn't be impacted by these changes.
<h2 id="service_studio_neo_0.9.4">Service Studio Neo 0.9.4</h2>
<div class="info"><p>Released on Mar 28, 2022</p></div>
<h3 id="new_in_service_studio_neo_0.9.4">New in Service Studio Neo 0.9.4</h3>
<ul>
<li>Fixed an issue that caused new static entity records to don't have the auto-increment id filled it. (RDEV-4183)</li>
<li>You are now able to zoom in and out in the flow editor by using Ctrl + the mouse scroll wheel. (RDEV-4225)</li>
<li>Fixed an issue that caused publish conflicts when the app doesn't exist in the server (RDEV-4232)</li>
<li>Users are now able to identify merge differences on screens &amp; blocks through widgets visual hints/decorations. (RDOIAT-301)</li>
<li>Improved overall memory consumption. (RDOIAT-474)</li>
<li>Editing application details (name, description, icon and primary color) is now accessible while editing the application, instead of from the applications list. (RICT-4341)</li>
</ul>
<h3 id="bug_fixing_3">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Static Records to keep the duplicated error indicator when no duplicated errors exists. (RDEV-4187)</li>
<li>Fixed an issue that caused the styles properties tab to not render when switching the focused widget. (RDEV-4224)</li>
<li>Fixed an issue that caused application templates to have wrong labels in the application creation wizard. (RDEV-4237)</li>
<li>Merge&amp;Compare icon added back in the toolbar (RDPMBT-912)</li>
</ul>
<h2 id="service_studio_neo_0.9.3">Service Studio Neo 0.9.3</h2>
<div class="info"><p>Released on Mar 15, 2022</p></div>
<h3 id="bug_fixing_4">Bug Fixing</h3>
<ul>
<li>Fixed an issue that prevented warnings and errors to have correspondent orange and red colors in tooltips.  (RDEV-4167)</li>
<li>Fix an issue that prevented RichWidgets' Icon to be propperly rendered (RMAC-9202)</li>
</ul>
<h2 id="service_studio_neo_0.9.2">Service Studio Neo 0.9.2</h2>
<div class="info"><p>Released on Mar 02, 2022</p></div>
<h3 id="new_in_service_studio_neo_0.9.2">New in Service Studio Neo 0.9.2</h3>
<ul>
<li>It's now possible to use text shortcuts in Flow editor (Cut, Copy, Paste, Delete). (RDOIBT-213)</li>
<li>It's now possible to use text shortcuts in right pane tree (Cut, Copy, Paste, Delete). (RDOIBT-220)</li>
<li>New App flow User Experience improvements (App list and App preview sidebar). (RDPMBT-306)</li>
<li>Name conflict workflow implementation in app's creation or edition. (RDPMBT-382)</li>
</ul>
<h2 id="service_studio_neo_0.9.1">Service Studio Neo 0.9.1</h2>
<div class="info"><p>Released on Feb 18, 2022</p></div>
<h3 id="new_in_service_studio_neo_0.9.1">New in Service Studio Neo 0.9.1</h3>
<ul>
<li>There's now a notification for new developers, telling them they can use the Smart Guidance feature to find help when developing apps. (RAID-883)</li>
</ul>
<h3 id="bug_fixing_5">Bug Fixing</h3>
<ul>
<li>Fixed a crash while exposing a Server Action as a Service Action. (RDEV-4093)</li>
<li>Fixed an issue that prevented the correct message to be shown while creating a new library. (RDEV-4094)</li>
<li>Fixed an issue where finding usages would not work if the consumer module was already open in another tab. (RMAC-9040)</li>
<li>Fix intermittent crash when opening Service Studio. (RMAC-9105)</li>
</ul>
<h2 id="service_studio_neo_0.9.0">Service Studio Neo 0.9.0</h2>
<div class="info"><p>Released on Feb 09, 2022</p></div>
<h3 id="new_in_service_studio_neo_0.9.0">New in Service Studio Neo 0.9.0</h3>
<ul>
<li>Drastically improved the response time of the Application List screen. (RDEV-4029)</li>
<li>It is now possible to Reset a timer's schedule, allowing you to have a timer that isn't scheduled to run. (RDEV-4048)</li>
</ul>
<h3 id="bug_fixing_6">Bug Fixing</h3>
<ul>
<li>CMD+Q Shortcut now works as expected in MacOS (RDPIM-78)</li>
</ul>
