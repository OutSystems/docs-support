---
locale: en-us
guid: 7ddf30aa-3be8-48c3-80fb-d2efdf1222cd
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

<div class="hidden"><h1>Cross-platform Service Studio</h1></div>

<div class="hidden" id="cross-platform-service-studio-11.53.38_start"></div>

<h2 id="cross-platform_service_studio_11.53.38" >Cross-platform Service Studio 11.53.38</h2>
<div class="info"><p>Released on Feb 06, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.38" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that was causing name editions in tree nodes to be lost when using the Ctrl+N / ⌘+N shortcut while still in edition. (RMAC-10821)</li>
<li>Fixed an issue with the HTML Element widget that caused Service Studio to hang with iframe tags. (RMAC-10889)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.38_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.37_start"></div>

<h2 id="cross-platform_service_studio_11.53.37" >Cross-platform Service Studio 11.53.37</h2>
<div class="info"><p>Released on Jan 30, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.37" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused mappings to break when refreshing REST API.
This occurred in a dropdown when the values of the dropdown would be mapped to a REST API.<br/>
Now, the REST refreshes and the mappings are still valid. (RMAC-10722)</li>
<li>Fixed an issue that caused Service Studio to display suggestions in SQL and JS editors when editing text inside comments. (RMAC-10865)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.37_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.36_start"></div>

<h2 id="cross-platform_service_studio_11.53.36" >Cross-platform Service Studio 11.53.36</h2>
<div class="info"><p>Released on Jan 23, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.36" >New in Cross-platform Service Studio 11.53.36</h3>
<ul>
<li>The filename property of an upload widget (mobile applications) being empty will not trigger a True-change error. (RDOIAT-824)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.36" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a crash when closing an app (it could also happen in other scenarios). (RDMST-1543)</li>
<li>Fixed an issue that caused a crash when opening the "Styles" tab in a screen or block with external stylesheets. (RMAC-10782)</li>
<li>Fixed an issue that caused a crash when deleting an object right after an edition. (RMAC-10881)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.36_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.35_start"></div>

<h2 id="cross-platform_service_studio_11.53.35" >Cross-platform Service Studio 11.53.35</h2>
<div class="info"><p>Released on Jan 16, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.35" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to lose information when closing any language editor (Expression editor, CSS editor, Javascript editor or SQL editor) immediately after adding text. (RMAC-10815)</li>
<li>Fixed an issue that prevented users from opening and editing an aggregate of certain screens or actions, in which the editor seemed very slow and sometimes irresponsive. (RPM-3493) <span class="cattag">Service Studio</span>  <span class="cattag">Data Access and Manipulation</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.35_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.34_start"></div>

<h2 id="cross-platform_service_studio_11.53.34" >Cross-platform Service Studio 11.53.34</h2>
<div class="info"><p>Released on Jan 09, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.34" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to be unresponsive when the user double clicked in the top bar (to maximize or resize). (RMAC-10752)</li>
<li>Fixed an issue that caused the debugger toolbar icons to be miss-aligned when debugging an application. (RMAC-10800)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.34_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.33_start"></div>

<h2 id="cross-platform_service_studio_11.53.33" >Cross-platform Service Studio 11.53.33</h2>
<div class="info"><p>Released on Jan 04, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.33" >Bug Fixing</h3>
<ul>
<li>Fixed the position of the "Show value" button in the debugger variables (e.g. "In Use", "Locals"). (RMAC-10088)</li>
<li>Improved the message shown on Aggregates when all attributes are hidden so that is distinguishable from the cases where there are no records to shown. (RMAC-10381)</li>
<li>Removed unnecessary empty lines from the Tooltips shown on Assign nodes.  (RMAC-10639)</li>
<li>Fixed an issue in the Merge editor that caused a crash during item selection if module versions had different links in a flow. (RMAC-10690)</li>
<li>Fixed an issue that caused a module to be marked as changed when canceling a source rename in an aggregate. (RMAC-10718)</li>
<li>Fixed an issue that caused new text to be created at the bottom of the screens when typing new text in placeholders. (RMAC-10738)</li>
<li>Fixed the source picker in the sort tab of grouped Aggregates to only allow picking grouped attributes. (RMAC-10753)</li>
<li>Fixed an issue that cause the Service Studio to freeze when clicking in the Table Record widget toolbar options. (RMAC-10756)</li>
<li>Fixed an issue that prevented widgets placed inside a Tabs widget content to be dragged to another position. (RMAC-10762)</li>
<li>Fixed an issue that caused Service Studio to freeze when changing the display mode of an If element. (RMAC-10766)</li>
<li>Fixed an issue that caused an incorrect behavior when double clicking Placeholders in a Screen or Block.<br/>
The double click was not navigating to the Placeholder's parent Block and when typing after that, the text was being added in the bottom of the Screen.<br/>
Now, the double click correctly navigates to the Placeholder's parent Block. (RMAC-10775)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.33_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.32_start"></div>

<h2 id="cross-platform_service_studio_11.53.32" >Cross-platform Service Studio 11.53.32</h2>
<div class="info"><p>Released on Jan 03, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.32" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Aggregates created using natural language to include entities that can't be used in Aggregates. This occurred even if those entities were not mentioned in the sentence. (RAID-1702)</li>
<li>Fixed an issue that prevented the user from copying multiple buttons at once. (RMAC-10713)</li>
<li>Fixed an issue that caused the properties panel being readonly when dropping a node in an action. (RMAC-10732)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.32_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.31_start"></div>

<h2 id="cross-platform_service_studio_11.53.31" >Cross-platform Service Studio 11.53.31</h2>
<div class="info"><p>Released on Dec 26, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.31" >New in Cross-platform Service Studio 11.53.31</h3>
<ul>
<li>It is now possible to change the display mode of placeholders inside web blocks. (RDOIAT-694)</li>
<li>Reduced the spacing between attribute names in Entity Diagrams. (RDOIAT-696)</li>
<li>In the right pane, some tabs now have reduced height so that more information can be shown in the same space. (RDOIAT-704)</li>
<li>Now, the context menu option 'Export [Diagram] to image' appears after the 'Paste' option. (RDOIAT-761)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.31" >Bug Fixing</h3>
<ul>
<li>Fixed an issue causing the delete shortcut to affect elements that are not selected. (RMAC-10462)</li>
<li>Fix an issue with properties being read-only unduly. (RMAC-10652)</li>
<li>Fixed an issue causing non-mandatory entity attributes to be marked as an error when empty and referring entities without records. (RMAC-10677)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.31_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.30_start"></div>

<h2 id="cross-platform_service_studio_11.53.30" >Cross-platform Service Studio 11.53.30</h2>
<div class="info"><p>Released on Dec 19, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.30" >New in Cross-platform Service Studio 11.53.30</h3>
<ul>
<li>An information banner is now shown when editing screen templates. (RDOIAT-695)</li>
<li>Reduced the spacing between attribute names in Entity Diagrams. (RDOIAT-696)</li>
<li>Now, the context menu option 'Export [Diagram] to image' appears after the 'Paste' option. (RDOIAT-761)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.30" >Bug Fixing</h3>
<ul>
<li>Fixed an issue in Code Mentor logic suggestions where pasting text would cause an extra V character to be added. (RAID-1565)</li>
<li>Fixed an issue when using Service Studio's command line arguments -importSettings and -exportSettings. (RMAC-10579)</li>
<li>Fixed a bug when importing a SOAP web service with restrictions. (RPM-508) <span class="cattag">Service Studio</span>  <span class="cattag">Logic</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.30_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.29_start"></div>

<h2 id="cross-platform_service_studio_11.53.29" >Cross-platform Service Studio 11.53.29</h2>
<div class="info"><p>Released on Dec 12, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.29" >New in Cross-platform Service Studio 11.53.29</h3>
<ul>
<li>An information banner is now shown when editing screen templates. (RDOIAT-695)</li>
<li>Now, the context menu option 'Export [Diagram] to image' appears after the 'Paste' option. (RDOIAT-761)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.29" >Bug Fixing</h3>
<ul>
<li>Fixed issue in Code Mentor logic suggestions that caused the "Whoops, my brain just froze!" message to appear when creating nodes in quick succession. (RAID-1751)</li>
<li>Fixed an issue that was causing Service Studio to open in another Windows user session.
This occurred when another windows user has Service Studio open, and the current one tries to open Service Studio as Administrator. (RMAC-10670)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.29_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.28_start"></div>

<h2 id="cross-platform_service_studio_11.53.28" >Cross-platform Service Studio 11.53.28</h2>
<div class="info"><p>Released on Dec 05, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.28" >New in Cross-platform Service Studio 11.53.28</h3>
<ul>
<li>Developers can now easily find embedded examples to help them create Aggregates using natural language. (RAID-1689)</li>
<li>The Service Studio properties dropdowns now focus the exact match while searching if one exists. (RDOIAT-522)</li>
<li>It is now possible to export any Flow (UI, Logic and Processes) or Entity Diagram to an image. (RDOIAT-686)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.28" >Bug Fixing</h3>
<ul>
<li>Fix properties scroll blocked on compare and merge editor. (RMAC-10591)</li>
<li>Fix losing focus while navigating the differences through keyboard in compare and merge editor. (RMAC-10623)</li>
<li>Fixed an issue that caused complete words not to be deleted when in Undo operations of adding text. (RMAC-10640)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.28_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.27_start"></div>

<h2 id="cross-platform_service_studio_11.53.27" >Cross-platform Service Studio 11.53.27</h2>
<div class="info"><p>Released on Nov 28, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.27" >New in Cross-platform Service Studio 11.53.27</h3>
<ul>
<li>Developers are now able to disable the Aggregates generation based on natural language, from the Preferences menu. (RAID-1693)</li>
<li>Changed the order on Data Type dropdown so that the "Other" data types category appear immediately after the Basic Types. (RDOIAT-383)</li>
<li>You will now be able to debug apps that redirect to external login providers, without losing the debug session. (RDOIBT-1009)</li>
<li>Improved readability of code comments when using dark theme. (RDOIBT-901)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.27" >Bug Fixing</h3>
<ul>
<li>Fixed an issue affecting AI-powered suggestions. (RAID-1750)</li>
<li>Fixed an issue that caused an empty filename on a upload widget to not give a True Change error in mobile applications. Filename is a mandatory field and should not be empty. (RMAC-10409)</li>
<li>Fixed and issue that caused the Custom url advanced properties to sometimes be shown when connected to Personal environments. (RMAC-10600)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.27_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.26_start"></div>

<h2 id="cross-platform_service_studio_11.53.26" >Cross-platform Service Studio 11.53.26</h2>
<div class="info"><p>Released on Nov 21, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.26" >New in Cross-platform Service Studio 11.53.26</h3>
<ul>
<li>It is now possible to automatically convert a JSON Deserialize node data type from Record to Structure. (RDOIAT-680)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.26" >Bug Fixing</h3>
<ul>
<li>Fixed typo on the Smart Guidance screen (RAID-1732)</li>
<li>Fixed an issue with horizontal scroll in web blocks. (RMAC-10582)</li>
<li>Fixed an issue that caused certain characters to be cropped on comment nodes. (RMAC-7499)</li>
<li>Fixed an issue causing the text cursor to be cropped while editing comment nodes. (RMAC-7631)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.26_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.25_start"></div>

<h2 id="cross-platform_service_studio_11.53.25" >Cross-platform Service Studio 11.53.25</h2>
<div class="info"><p>Released on Nov 14, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.25" >New in Cross-platform Service Studio 11.53.25</h3>
<ul>
<li>The default base background color is now white for both Service Studio themes (Light and Dark). (RDOIAT-658)</li>
<li>Improved contrast of the small arrows in the icons for Entities and Structures attributes. (RDOIBT-969)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.25" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that could cause Service Studio main window to open with its content cropped on MacOS. (RMAC-10534)</li>
<li>Fixed an issue causing vertical scroll to not work when editing screens with sidebars (RMAC-10544)</li>
<li>Fixed a bug when importing a SOAP web service that imported an external schema as a WSDL (RPM-3044) <span class="cattag">Service Studio</span>  <span class="cattag">Logic</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.25_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.24_start"></div>

<h2 id="cross-platform_service_studio_11.53.24" >Cross-platform Service Studio 11.53.24</h2>
<div class="info"><p>Released on Nov 07, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.24" >New in Cross-platform Service Studio 11.53.24</h3>
<ul>
<li>Native Menus from MacOS now include an icon as a visual aid to help distinguish between commands. (RTAFB-5870)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.24" >Bug Fixing</h3>
<ul>
<li>Fixed issues with Copy, Paste and Delete shortcuts stopping working in some editors after executing undo operations (RMAC-10205)</li>
<li>Fixed an issue that could cause Service Studio to open mostly outside the visible screen. (RMAC-10451)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.24_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.23_start"></div>

<h2 id="cross-platform_service_studio_11.53.23" >Cross-platform Service Studio 11.53.23</h2>
<div class="info"><p>Released on Oct 31, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.23" >Bug Fixing</h3>
<ul>
<li>Fixed a bug that caused Service Studio to become irresponsible while clicking on widgets or flow nodes. (RMAC-10204)</li>
<li>Fixed an issue that prevented navigation to the action when double-clicking a button of a screen/block. (RMAC-10427)</li>
<li>Fixed an issue related with compound data types that was causing some crashes when editing properties and considering them readonly when they should be editable (RMAC-10475)</li>
<li>Fixed an issue that caused wrong selection of text when several selecting text widgets that were placed consecutively. (RMAC-9753)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.23_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.22_start"></div>

<h2 id="cross-platform_service_studio_11.53.22" >Cross-platform Service Studio 11.53.22</h2>
<div class="info"><p>Released on Oct 24, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.22" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that could cause Service Studio to hang when opening the About or Preferences dialog while another message dialog was being displayed in the Applications List. (RMAC-10433)</li>
<li>Fixed an issue that caused tooltip values to be truncated when they contained pipe characters. (RMAC-9201)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.22_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.21_start"></div>

<h2 id="cross-platform_service_studio_11.53.21" >Cross-platform Service Studio 11.53.21</h2>
<div class="info"><p>Released on Oct 17, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.21" >New in Cross-platform Service Studio 11.53.21</h3>
<ul>
<li>Now it's possible to use the ⌘⌫ keyboard shortcut in MacOS to Delete Assignment row within an Assign. (RDOIBT-423)</li>
<li>Now it's possible to use ⇧⌘J / Ctrl + J keyboard shortcut to toggle between Properties and Styles tabs. (RDOIBT-706)</li>
<li>Now it's possible to use Cmd + Click in MacOS to navigate to an element in the Expression editor.  (RDOIBT-772)</li>
<li>Now it's possible to use the ⌘. keyboard shortcut in MacOS to Select the active element in the elements tree. (RDOIBT-787)</li>
<li>Mobile applications build failures warnings/errors in Service Studio now have a direct link to error-specific documentation. (RDOIBT-794)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.21" >Bug Fixing</h3>
<ul>
<li>Fixed an issue, when clearing the name of a module, that caused the name to fallback to ‘eSpace’ instead of ‘Module’. (RMAC-10333)</li>
<li>Fixed some issues when closing modules during its loading (RMAC-10334)</li>
<li>Fixed an issue that would cause screens to appear blank when they were complex and had deep nested widgets. (RMAC-10365)</li>
<li>Fixed a bug in which Service Studio occasionally crashed after double-clicking Screens, Flows, or Variables several times. (RMAC-10383)</li>
<li>Fixed an issue with selection synchronisation with Properties editor that happened when the current object in edition was outside of the visible area of the App layer tabs (RMAC-10386)</li>
<li>Fixed an issue that was causing Service Studio to stop responding when some crashes occur. (RMAC-10387)</li>
<li>Fixed an issue that caused the Integration Studio registry to have the wrong version when installing Service Studio in the development environment. (RMAC-10391)</li>
<li>Fixed an issue with columns width on the bottom pane. (RMAC-10398)</li>
<li>Fixed an issue with images in the REST Consume dialog. (RMAC-10406)</li>
<li>Fixed SAP dialog text and button labels. (RMAC-9791)</li>
<li>Fixed a bug in which exporting definition files of SOAP services resulted in wrong output encoding. Now, original encoding of SOAP services is kept when exporting definition files. (RO11IT-51)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.21_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.20_start"></div>

<h2 id="cross-platform_service_studio_11.53.20" >Cross-platform Service Studio 11.53.20</h2>
<div class="info"><p>Released on Oct 10, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.20" >New in Cross-platform Service Studio 11.53.20</h3>
<ul>
<li>Now it's possible to use Cmd + Click in MacOS to navigate to an element in the Expression editor.  (RDOIBT-772)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.20" >Bug Fixing</h3>
<ul>
<li>Fixed an issue, when clearing the name of a module, that caused the name to fallback to ‘eSpace’ instead of ‘Module’. (RMAC-10333)</li>
<li>Fixed an issue that would cause screens to appear blank when they were complex and had deep nested widgets. (RMAC-10365)</li>
<li>Fixed a bug in which Service Studio occasionally crashed after double-clicking Screens, Flows, or Variables several times. (RMAC-10383)</li>
<li>Fixed an issue with selection synchronisation with Properties editor that happened when the current object in edition was outside of the visible area of the App layer tabs (RMAC-10386)</li>
<li>Fixed an issue that was causing X-IDE to stop responding when some crashes occur. (RMAC-10387)</li>
<li>Fixed an issue that caused the Integration Studio registry to have the wrong version when installing Service Studio in the development environment. (RMAC-10391)</li>
<li>Fixed an issue that would cause screens to appear blank when they were complex and had deep nested widgets. (RPM-3050) <span class="cattag">Service Studio</span>  <span class="cattag">Interface</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.20_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.19_start"></div>

<h2 id="cross-platform_service_studio_11.53.19" >Cross-platform Service Studio 11.53.19</h2>
<div class="info"><p>Released on Oct 03, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.19" >New in Cross-platform Service Studio 11.53.19</h3>
<ul>
<li>Now it's possible to use the ⇧⌘E keyboard shortcut in MacOS to Search Widgets or blocks in the toolbox. (RDOIBT-678)</li>
<li>Now it's possible to use the ⇧⌘H keyboard shortcut in MacOS to Replace all text occurrences or element usages. (RDOIBT-685)</li>
<li>Now it's possible to use the ⌘D keyboard shortcut in MacOS to open the Manage Dependencies dialog. (RDOIBT-713)</li>
<li>Now it's possible to use ⇧⌘H keyboard shortcut in MacOS to Show/Hide a warning in the TrueChange (in Development tabs). (RDOIBT-720)</li>
<li>Now it's possible to use ⇧⌘M keyboard shortcut in MacOS to Compare and Merge a module with the published version. (RDOIBT-727)</li>
<li>Now it's possible to use ⇧⌘D keyboard shortcut in MacOS to show/hide development tabs (Errors/warnings, Debugger, etc). (RDOIBT-749)</li>
<li>Now it's possible to use ⌘T keyboard shortcut in MacOS to show/hide the Widget tree. (RDOIBT-756)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.19" >Bug Fixing</h3>
<ul>
<li>Fixed a bug in which the Widgets tree stopped responding when the opened screen was renamed. (RMAC-10309)</li>
<li>Fixed some inconsistencies in the SQL capitalization when converting an aggregate into an AdvancedSQL node. (RMAC-10329)</li>
<li>You can now use Y and N keys as shortcuts in "IsAutoNumber" property of entities. (RMAC-10357)</li>
<li>Fixed an issue when validating Javascript nodes ending with a single line comment. (RMAC-10362)</li>
<li>Fixed an issue that was causing SS to stop responding when some crashes occur. (RMAC-10387)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.19_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.18_start"></div>

<h2 id="cross-platform_service_studio_11.53.18" >Cross-platform Service Studio 11.53.18</h2>
<div class="info"><p>Released on Sep 26, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.18" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused ServiceStudio to freeze when resizing an empty form or list (RMAC-10336)</li>
<li>Fixed the Refresh SQL node icon. (RMAC-9899)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.18_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.17_start"></div>

<h2 id="cross-platform_service_studio_11.53.17" >Cross-platform Service Studio 11.53.17</h2>
<div class="info"><p>Released on Sep 19, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.17" >New in Cross-platform Service Studio 11.53.17</h3>
<ul>
<li>You now have a frame to provide visual feedback that a block is being edited. (RDOIAT-523)</li>
<li>It is now possible to select the operators "and", "or" and "not" from the autocomplete suggestions in expression editor. (RDOIBT-540)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.17" >Bug Fixing</h3>
<ul>
<li>Fixed an issue with Logic Assistant where a crash would occur after a long period of unavailability. (RAID-1662)</li>
<li>Fixed "Open from Environment" and "Open other Version" dialogs to be resizable (RMAC-10085)</li>
<li>Fixed an issue that caused wrong behavior when hovering a numeric or date attribute in the Edit Data view. (RMAC-10319)</li>
<li>Fixed an issue that caused top menu icons to be shown as disabled when they were not. (RMAC-10327)</li>
<li>Fixed some issues when rendering the tests' output data in the SQL editor. (RMAC-10339)</li>
<li>Fixed an issue that caused Service Studio installer to ignore the `/D` parameter when executed via command line. (RMAC-10353)</li>
<li>Styles properties will be correctly updated. (RPM-3004) <span class="cattag">Service Studio</span>  <span class="cattag">Windows and Editors</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.17_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.16_start"></div>

<h2 id="cross-platform_service_studio_11.53.16" >Cross-platform Service Studio 11.53.16</h2>
<div class="info"><p>Released on Sep 12, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.16" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the "full-height" class not to work when editing blocks (RMAC-10075)</li>
<li>Fixed an issue where the new modules' theme didn't receive the App's default color and the login screen's background image was wrongly initialized on Theme Editor. (RMAC-10140)</li>
<li>Fixed an issue that caused the keyboard shortcut to Refresh Aggregate's data preview to not work as expected when selecting rows on preview data. (RMAC-10237)</li>
<li>Fixed a crash in Service Studio when accessing invalid objects. (RMAC-10246)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.16_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.15_start"></div>

<h2 id="cross-platform_service_studio_11.53.15" >Cross-platform Service Studio 11.53.15</h2>
<div class="info"><p>Released on Sep 06, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.15" >New in Cross-platform Service Studio 11.53.15</h3>
<ul>
<li>It is now possible to interact with widget breadcrumbs using Double-click, Right-click and Drag and Drop. (RDOIAT-505)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.15" >Bug Fixing</h3>
<ul>
<li>Fixed and issue that caused widgets to always be pasted as the last child of the parent container, not respecting the caret position. (RMAC-10160)</li>
<li>Fixed an issue that caused image previews to overlap other properties.  (RMAC-10243)</li>
<li>Fixed an issue that caused OSPTool to not be included during the Service Studio installation. (RMAC-10252)</li>
<li>Fixed an issue that would block certain users (with Identity Service Integration) from login into the OS environments through Service Studio 11.53.13.61176. (RMAC-10291)</li>
<li>Fixed an issue that caused a crash when consuming external databases. (RMAC-10307)</li>
<li>Fixed an issue that caused users not being able select "Connect Anyway" when connecting to unsecure environments. (RMAC-10326)</li>
<li>Fixed an issue that caused an arrow to be lost in a switch condition after moving a screen (RPM-2682) <span class="cattag">Service Studio</span>  <span class="cattag">Interface</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.15_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.14_start"></div>

<h2 id="cross-platform_service_studio_11.53.14" >Cross-platform Service Studio 11.53.14</h2>
<div class="info"><p>Released on Aug 29, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.14" >New in Cross-platform Service Studio 11.53.14</h3>
<ul>
<li>It is now possible to resize the Debugger Entry Module drop-down by adjusting the Debugger splitter position. (RDOIAT-666)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.14" >Bug Fixing</h3>
<ul>
<li>The request body is now omitted from GET request tests when consuming REST APIs. (RMAC-10157)</li>
<li>Fixed an issue that caused translations to be lost in merge operations. (RMAC-10229)</li>
<li>Fixed an issue that would hang the merge editor after un-resolving a textual conflict. (RMAC-10256)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.14_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.13_start"></div>

<h2 id="cross-platform_service_studio_11.53.13" >Cross-platform Service Studio 11.53.13</h2>
<div class="info"><p>Released on Aug 22, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.13" >New in Cross-platform Service Studio 11.53.13</h3>
<ul>
<li>It is now possible to search for a specific shortcut in the keyboard shortcuts list (Help > Keyboard Shortcuts). (RDOIBT-817)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.13" >Bug Fixing</h3>
<ul>
<li>Fixed an issue with proxy authentication settings being ignored on requests made by some editors (RMAC-10056)</li>
<li>Fixed and issue that caused caret miss-placement after paste operations. (RMAC-10109)</li>
<li>Fixed an issue with breaklines being ignored causing losses of breaklines in text and malfunctioning of Paste in text elements with breaklines. (RMAC-10213)</li>
<li>Fixed an issue that caused a slow response in properties pane when editing items with multiple properties. (RMAC-10234)</li>
<li>Fixed an issue when opening OML directly from file explorer. (RMAC-9909)</li>
<li>Fixed an issue that caused an arrow to be lost in a switch condition after moving a screen (RPM-2682) <span class="cattag">Service Studio</span>  <span class="cattag">Interface</span> </li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.13_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.12_start"></div>

<h2 id="cross-platform_service_studio_11.53.12" >Cross-platform Service Studio 11.53.12</h2>
<div class="info"><p>Released on Aug 16, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.12" >New in Cross-platform Service Studio 11.53.12</h3>
<ul>
<li>It is now possible to do Find and Replace within the Expression Editor and the Advanced Query Editor. (RDOIBT-826)</li>
<li>It is now possible to copy Service Studio version information from the "About Service Studio" dialog. (RDOIBT-827)</li>
<li>All Server Actions created by Integration Builder will 
now also appear in the Logic Tab, under the Integrate With External System menu item. (RIMPT-2131)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.12" >Bug Fixing</h3>
<ul>
<li>Fix issues on undo after a merge operation (RMAC-10121)</li>
<li>Fixed an issue that was causing repetition of the clipboard content when pasting in the Styles Classes input in the Styles tab (RMAC-10145)</li>
<li>Fixed an issue that caused loss of some values of the dropdown widgets with structures when doing a copy/paste (RMAC-10222)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.12_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.11_start"></div>

<h2 id="cross-platform_service_studio_11.53.11" >Cross-platform Service Studio 11.53.11</h2>
<div class="info"><p>Released on Aug 08, 2022</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_cross-platform_service_studio_11.53.11" >New in Cross-platform Service Studio 11.53.11</h3>
<ul>
<li>When naming an attribute of a Record data type, the data type is now automatically suggested, analogically to what happens in attributes of a Structure. (RDOIAT-375)</li>
<li>Now the widgets' selection is recovered after undo and redo operations, as well as when opening a module. (RDOIBT-604)</li>
<li>Reminder comments are now displayed in a different color. Inspired by <a href="https://www.outsystems.com/ideas/1961/reminder-comments-with-a-different-color/" target="_blank" rel="noopener noreferrer">Hermínio Mira's idea</a>. (RIMPT-2954)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.11" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the impossibility of copying Text Widgets when no selection on the text inside the widget was being done. (RMAC-10104)</li>
<li>Fixed an issue that prevented the user to type some special characters. (RMAC-10114)</li>
<li>Fixed indentation for properties in bold in the properties pane. (RMAC-10119)</li>
<li>Fixed drop of files in Service Studio (RMAC-10127)</li>
<li>Fixed an issue that caused pasting old texts from the clipboard when pasting over button widgets. (RMAC-10146)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.11_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.10_start"></div>

<h2 id="cross-platform_service_studio_11.53.10" >Cross-platform Service Studio 11.53.10</h2>
<div class="info"><p>Released on Aug 01, 2022</p></div>

<h3 id="new_in_cross-platform_service_studio_11.53.10" >New in Cross-platform Service Studio 11.53.10</h3>
<ul>
<li>It is now possible to change the app logo by clicking the current logo in the New Application dialog. (RIMPT-2778)</li>
<li>View Data now shows the icon of the type of Entity being viewed. (RIMPT-2870)</li>
<li>It is now possible to fix a new Entity error by right-clicking the message and choosing "Create new Entity Attribute". (RIMPT-2881)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.10" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the creation of the first module to open with a blank screen (RMAC-10012)</li>
<li>Fixed an issue that caused icon errors when using some regional settings. (RMAC-10113)</li>
<li>Fixed an issue that caused double click on elements to not work (RMAC-10136)</li>
<li>Dark Theme Dialogs now have for prominent border (RMAC-8342)</li>
<li>Fixed a performance issue in the SQL editor. (RMAC-9137)</li>
<li>Fixed a crash in Merge when selecting to merge an attribute from a deleted entity. (RMAC-9564)</li>
<li>Fixed a crash when refreshing a reference of a folder. (RMAC-9780)</li>
<li>Fix label property of dropdown widget not being correctly set after copy/paste or drag/drop (RMAC-9944)</li>
<li>Fixed a bug where ShiftInsert and ShiftDelete shortcutKeys, were causing double pasting/cutting the values on ServiceStudio editors.  (RMAC-9961)</li>
<li>Fixed an issue where right-clicking a true change message was mentioning another element. (RMAC-9965)</li>
<li>Fixed an error that would cause the 'Edit Data' editor to go blank when modifying a dropdown value on an entity record. (RPM-2791)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.10_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.9_start"></div>

<h2 id="cross-platform_service_studio_11.53.9" >Cross-platform Service Studio 11.53.9</h2>
<div class="info"><p>Released on Jul 25, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.53.9" >Bug Fixing</h3>
<ul>
<li>Now it's possible to open the Forge tab when using an HTTP proxy with authentication. (RMAC-10057)</li>
<li>The cursor is now placed in the correct position when starting to type in an empty container of a screen. (RMAC-9938)</li>
<li>Fixed a crash on manage dependencies when closing it while having pending background tasks. (RMAC-9978)</li>
<li>Fixed an issue that caused the keyboard shortcuts CTRL+O and SHIFT+CTRL+O to not work when used within a module context. (RMAC-9995)</li>
<li>Fixed an issue in Manage Dependencies progress indicator preventing it to surpass 0% for several seconds. (RMAC-9996)</li>
<li>Fixed the occasional blank rendering of the references list in Manage Dependencies after processing. (RMAC-9997)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.9_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.8_start"></div>

<h2 id="cross-platform_service_studio_11.53.8" >Cross-platform Service Studio 11.53.8</h2>
<div class="info"><p>Released on Jul 18, 2022</p></div>

<h3 id="new_in_cross-platform_service_studio_11.53.8" >New in Cross-platform Service Studio 11.53.8</h3>
<ul>
<li>It is now possible to resize properties pane labels and input fields. (RDOIBT-620)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.8" >Bug Fixing</h3>
<ul>
<li>Fixed an issue in the high code editors, in which the usage of the Shift+Enter shortcut would close those editors' dialogs. Also fixed the Ctrl+Enter shortcut usage on macOS for the same high code editors, not closing the dialogs anymore - on this Operative System the proper confirmation shortcut is ⌘+Enter. (RMAC-8502)</li>
<li>The error messages that appear whenever the command of Scaffolding Screens from entities has a problem are now more specific for the different scenarios of errors. (RMAC-9786)</li>
<li>Fixed a crash when closing manage dependencies while it is being loaded. (RMAC-9953)</li>
<li>Fixed an issue that caused false positive warnings to be shown in JavaScript editor. (RMAC-9963)</li>
<li>Fixed a crash in the Translations Editor when filtering translations. (RMAC-9977)</li>
<li>Fixed an issue that caused the keyboard shortcuts CTRL+O and SHIFT+CTRL+O to not work when used within a module context. (RMAC-9995)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.8_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.7_start"></div>

<h2 id="cross-platform_service_studio_11.53.7" >Cross-platform Service Studio 11.53.7</h2>
<div class="info"><p>Released on Jul 11, 2022</p></div>

<h3 id="new_in_cross-platform_service_studio_11.53.7" >New in Cross-platform Service Studio 11.53.7</h3>
<ul>
<li>The SAP Connection parameters "Route" and "System ID" are no longer mandatory. (RDOIBT-641)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.7" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused flow nodes to be deleted when using the Delete keyboard shortcut to delete breakpoints. (RMAC-9707)</li>
<li>Fixed an issue with tabs navigation in Windows. (RMAC-9799)</li>
<li>Fixed a crash when using the Refresh all open Consumers operation. (RMAC-9837)</li>
<li>Fixed a crash when pasting a text widget using the shortcut (ctrl+v) inside of another text widget. (RMAC-9892)</li>
<li>Fixed an issue that would cause a crash when manipulating widgets. (RMAC-9932)</li>
<li>Fixed an issue on flow comments in which the text cursor would not be shown after clicking to edit the text. (RMAC-9935)</li>
<li>Fixed an issue when previewing aggregates data in Service Studio that would display a 'No data' message when there was actually data. (RPM-2673)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.7_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.6_start"></div>

<h2 id="cross-platform_service_studio_11.53.6" >Cross-platform Service Studio 11.53.6</h2>
<div class="info"><p>Released on Jul 04, 2022</p></div>

<h3 id="new_in_cross-platform_service_studio_11.53.6" >New in Cross-platform Service Studio 11.53.6</h3>
<ul>
<li>It is now possible to check for service updates in SOAP Web Services. (R11DT-1259)</li>
<li>Converting Text to an Expression now brings the text to the Expression's Value property. Inspired by <a href="https://www.outsystems.com/ideas/6204/convert-text-to-expression-expression-default-value/" target="_blank" rel="noopener noreferrer">Hanno's idea</a>. (RIMPT-2693)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.6" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that would show a second login dialog when failing to connect to an environment. (RIMPT-2589)</li>
<li>Fixed an issue that caused Service Studio to freeze after selecting Apply in the Manage Dependencies dialog while a publish operation was being performed. (RMAC-9830)</li>
<li>Fixed an issue in flow editor in which it wasn't possible to drag multiple nodes. (RMAC-9913)</li>
<li>Fixed an issue that caused References not to be updated on a specific edge case. (RPM-2650)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.6_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.5_start"></div>

<h2 id="cross-platform_service_studio_11.53.5" >Cross-platform Service Studio 11.53.5</h2>
<div class="info"><p>Released on Jun 27, 2022</p></div>

<h3 id="new_in_cross-platform_service_studio_11.53.5" >New in Cross-platform Service Studio 11.53.5</h3>
<ul>
<li>You can now use Y and N keys as shortcuts to select Yes or No in Yes/No properties. (RMAC-9826)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.53.5" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the text widget to crash in traditional web applications. (RMAC-9346)</li>
<li>Fixed a crash in Manage Dependencies when clicking in Cancel multiple times in a row. (RMAC-9779)</li>
<li>Solved a bug on Manage dependencies where some cached references would not be properly decorated. (RMAC-9784)</li>
<li>Fixed crash when trying to drag a "Trigger event" element from the left pane (RMAC-9883)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.5_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.4_start"></div>

<h2 id="cross-platform_service_studio_11.53.4" >Cross-platform Service Studio 11.53.4</h2>
<div class="info"><p>Released on Jun 23, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.53.4" >Bug Fixing</h3>
<ul>
<li>Fixed an error on Compare&Merge dialog when trying to merge and cancel at the same time. (RMAC-9731)</li>
<li>Fixed an issue in the JavaScript validation. (RMAC-9795)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.4_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.3_start"></div>

<h2 id="cross-platform_service_studio_11.53.3" >Cross-platform Service Studio 11.53.3</h2>
<div class="info"><p>Released on Jun 13, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.53.3" >Bug Fixing</h3>
<ul>
<li>Fix an issue on the UIEditor list widget where there were missing ancestors on ancestors stack (RMAC-9142)</li>
<li>Fixes a bug with debugging mobile breakpoint not stopping in breakpoints. (RMAC-9677)</li>
<li>Fixed concurrent merge operations. (RMAC-9735)</li>
<li>Fixed an issue with links in comment nodes. (RMAC-9781)</li>
<li>Fixed an issue that could lead to a conflicting version to overwrite the latest one without warning. (RMAC-9801)</li>
<li>Fixed an issue that caused all Dialog windows to have the minimize button  (RMAC-9805)</li>
<li>Fixed an issue that caused the cursor to jump when editing names in the Properties panel. (RMAC-9813)</li>
<li>Fixed a bug when importing WSDL (in the SOAP consume use case) from an URL and as a consequence the "Choose one Binding" window had no options available.  (RPM-1297)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.3_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.2_start"></div>

<h2 id="cross-platform_service_studio_11.53.2" >Cross-platform Service Studio 11.53.2</h2>
<div class="info"><p>Released on Jun 08, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.53.2" >Bug Fixing</h3>
<ul>
<li>Fixed a bug when using the Export Definition Files command in consumed SOAP Web Services. (R11DT-1206)</li>
<li>Fixed an issue when creating a node in the tree that would prevent it from being renamed immediately. (RMAC-9354)</li>
<li>Fixed an issue that caused a crash when a record or a list literal expression changes with the expression editor still open. (RMAC-9687)</li>
<li>Fixed some content not being rendered in Service Studio like the content of the Tabs pattern (RMAC-9691)</li>
<li>Fix issue when publishing with broken references (RMAC-9702)</li>
<li>Fixed an issue that could lead to a conflicting version to overwrite the latest one without warning. (RMAC-9801)</li>
<li>Fixed an issue that would hide communication errors when fetching application updates from Forge. (RMAC-9811)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.2_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.1_start"></div>

<h2 id="cross-platform_service_studio_11.53.1" >Cross-platform Service Studio 11.53.1</h2>
<div class="info"><p>Released on Jun 06, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.53.1" >Bug Fixing</h3>
<ul>
<li>Fixed an issue where opening the Aggregates editor in a new window could cause Service Studio to crash. (RAID-1401)</li>
<li>Fixed an issue when trying to Run and Debug in a Personal Area. (RMAC-9587)</li>
<li>Fixes crash when navigating back to previously deleted application (RMAC-9662)</li>
<li>Fix a concurrency issue when performing Extract To Action command (RMAC-9684)</li>
<li>Enable Compare with published version command when opening a module from a saved file (RMAC-9700)</li>
<li>Fix refresh/delete of references on Manage Dependencies when element is not selected (RMAC-9703)</li>
<li>Fixed an issue where the Max. Length property of a Text Area was being cleared when moving the widget to a different location. (RMAC-9705)</li>
<li>Fix an issue that was forcing SS to close after a specific crash (RMAC-9721)</li>
<li>Fixes bug where Input Parameters of Referenced Web blocks were not visible. (RPM-2632)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.1_end"></div><div class="hidden" id="cross-platform-service-studio-11.53.0_start"></div>

<h2 id="cross-platform_service_studio_11.53.0" >Cross-platform Service Studio 11.53.0</h2>
<div class="info"><p>Released on May 30, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.53.0" >Bug Fixing</h3>
<ul>
<li>Fixed an issue where opening the Aggregates editor in a new window could cause Service Studio to crash. (RAID-1401)</li>
<li>Fix xss vulnerability on EULA resources (RMAC-9049)</li>
<li>Improved the CTRL+Z experience to undo full words. (RMAC-9449)</li>
<li>Improved the dropdown experience inside the properties panel. (RMAC-9591)</li>
<li>Fix issue when connection to android devices is lost when debugging (RMAC-9595)</li>
<li>Fixed a crash in Manage Dependencies when selecting different producer modules. (RMAC-9633)</li>
<li>Fixed an issue when having multiple instances of Service Studio connected to different environments that caused some operations to execute on the incorrect environment. (RMAC-9657)</li>
<li>Fixes crash when navigating back to previously deleted application (RMAC-9662)</li>
<li>Improve performance of copy paste in Aggregates (RMAC-9668)</li>
<li>Fix an issue with timeout exception and avoid unnecessary server connection in some occasions (RMAC-9670)</li>
<li>Fixes a bug that removed the Service Studio stable from the menu shortcuts when uninstalling the Service Studio Beta (RMAC-9672)</li>
<li>Fix a problem that make Service Studio unresponsive the first time its connect to an environment and try to create a new screen (RMAC-9676)</li>
<li>Fix xss vulnerability on Smart Guidance services (RMAC-9681)</li>
<li>Fix concurrency issues on some Manage Dependencies use cases (RMAC-9682)</li>
<li>Fix issue that happens when closing dialogs in specific situations (RMAC-9688)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.53.0_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.7_start"></div>

<h2 id="cross-platform_service_studio_11.52.7" >Cross-platform Service Studio 11.52.7</h2>
<div class="info"><p>Released on May 23, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.52.7" >Bug Fixing</h3>
<ul>
<li>Improved the CTRL+Z experience to undo full words. (RMAC-9449)</li>
<li>Improved the dropdown experience inside the properties panel. (RMAC-9591)</li>
<li>Fixed a crash in Manage Dependencies when selecting different producer modules. (RMAC-9633)</li>
<li>Fixed an issue when having multiple instances of Service Studio connected to different environments that caused some operations to execute on the incorrect environment. (RMAC-9657)</li>
<li>Improve performance of copy paste in Aggregates (RMAC-9668)</li>
<li>Fix an issue with timeout exception and avoid unnecessary server connection in some occasions (RMAC-9670)</li>
<li>Fixes a bug that removed the Service Studio stable from the menu shortcuts when uninstalling the Service Studio Beta (RMAC-9672)</li>
<li>Improve performance of copy paste operations in complex Aggregates (RPM-2544)</li>
<li>Fixed a XSS vulnerability on EULA. CVSSv3.1 score 5.6 (Medium). (RPM-2337)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.52.7_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.6_start"></div>

<h2 id="cross-platform_service_studio_11.52.6">Cross-platform Service Studio 11.52.6</h2>
<div class="info"><p>Released on May 16, 2022</p></div>
<h3 id="bug_fixing_11.52.6">Bug Fixing</h3>
<ul>
<li>Fixed a crash when loading screen templates. (RMAC-9576)</li>
<li>Fixed a crash when dragging a client action to a screen. (RMAC-9588)</li>
<li>Fix an issue when navigating back/forward in the history that caused a crash in some situations (RMAC-9590)</li>
</ul><div class="hidden" id="cross-platform-service-studio-11.52.6_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.5_start"></div>

<h2 id="cross-platform_service_studio_11.52.5" >Cross-platform Service Studio 11.52.5</h2>
<div class="info"><p>Released on May 09, 2022</p></div>

<h3 id="bug_fixing_cross-platform_service_studio_11.52.5" >Bug Fixing</h3>
<ul>
<li>Avoid crash opening Screen Template Dialog for first time without connection to an environment (RMAC-9580)</li>
<li>Fixed an issue when having multiple instances of Service Studio connected to different environments that caused some operations to execute on the incorrect environment. (RMAC-9657)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.52.5_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.4_start"></div>

<h2 id="cross-platform_service_studio_11.52.4">Cross-platform Service Studio 11.52.4</h2>
<div class="info"><p>Released on Apr 29, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.52.4">New in Cross-platform Service Studio 11.52.4</h3>
<ul>
<li>Refresh ServiceStudio UI while a progress dialog is loading (RDOIAT-545)</li>
</ul>
<h3 id="bug_fixing_11.52.4">Bug Fixing</h3>
<ul>
<li>Fixed an issue that was forcing Service Studio to not respect IPP UnProtected environment setting (RMAC-9422)</li>
<li>Fixed Service Studio crash when applying changes to the References of a module (RMAC-9439)</li>
<li>Fix an issue that could occur when closing a module tab while the flow suggestions popup was about to be shown. (RMAC-9528)</li>
<li>Use Expression Editor for complex expressions referring Static Entities instead of the Record Picker (RMAC-9532)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.52.4_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.3_start"></div>

<h2 id="cross-platform_service_studio_11.52.3">Cross-platform Service Studio 11.52.3</h2>
<div class="info"><p>Released on Apr 21, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.52.3">New in Cross-platform Service Studio 11.52.3</h3>
<ul>
<li>It is now possible to open Aggregates and Edit Data in a separate window. This way, you can compare Aggregates and Entities while seeing your screens or logic flows. (RTAFA-449)</li>
</ul>
<h3 id="bug_fixing_11.52.3">Bug Fixing</h3>
<ul>
<li>Improved Aggregate's data preview experience (RAID-1394)</li>
<li>Fix a crash when trying to open multiple AddRemoveReferences dialogs at once (RMAC-9022)</li>
<li>Fixed an error that occurred when spanning out a new Service Studio instance by dragging a module tab of a disconnected environment. (RMAC-9371)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.52.3_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.2_start"></div>

<h2 id="cross-platform_service_studio_11.52.2">Cross-platform Service Studio 11.52.2</h2>
<div class="info"><p>Released on Apr 06, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.52.2">New in Cross-platform Service Studio 11.52.2</h3>
<ul>
<li>You can now use SOAP Refresh option to quickly change the services consumed from a SOAP Web Service or modify the list of consumed methods. (RDOIBT-80)</li>
</ul>
<h3 id="bug_fixing_11.52.2">Bug Fixing</h3>
<ul>
<li>Fix an issue that caused the Widget tree to immediately appear (in Windows OS only) when starting to drag elements from other right pane trees. (RMAC-8520)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.52.2_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.1_start"></div>

<h2 id="cross-platform_service_studio_11.52.1">Cross-platform Service Studio 11.52.1</h2>
<div class="info"><p>Released on Mar 22, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.52.1">New in Cross-platform Service Studio 11.52.1</h3>
<ul>
<li>Service Studio is not be able to connect to Project Neo anymore. Service Studio Project Neo should be used instead. (RDEV-3959)</li>
<li>Improved the experience of using copy, paste, cut, and delete keyboard shortcuts when editing text in Service Studio. For more information about keyboard shortcuts, go to Help -&gt; Keyboard Shortcuts in Service Studio. (RDOIBT-206)</li>
<li>You can now use SOAP Refresh option to quickly change the services consumed from a SOAP Web Service or modify the list of consumed methods. (RDOIBT-80)</li>
<li>Now on text widgets the UnDo and ReDo operations are done with text aggregation for more efficient execution. (RTAFB-5584)</li>
</ul>
<h3 id="bug_fixing_11.52.1">Bug Fixing</h3>
<ul>
<li>Improved an error message by adding relevant information when an array lacks the items definition while importing a REST Web Service. (R11DT-382)</li>
<li>Fixed an issue that caused the installation of a sample app to fail. (RIMPT-1653)</li>
<li>Fix issue that prevents the iterator from being updated after typing inside a TextWidget (RMAC-8345)</li>
<li>Solves a problem in a semaphore where some promises could hang forever. (RMAC-9258)</li>
<li>Solves problem when the user starts typing in a container and the SS freezes (RMAC-9259)</li>
<li>RichWidget Icon preview shows the icon selected. (RPM-2106)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.52.1_end"></div><div class="hidden" id="cross-platform-service-studio-11.52.0_start"></div>

<h2 id="cross-platform_service_studio_11.52.0">Cross-platform Service Studio 11.52.0</h2>
<div class="info"><p>Released on Mar 18, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.52.0">New in Cross-platform Service Studio 11.52.0</h3>
<ul>
<li>It is now possible to export the definition files from a consumed SOAP Web Service. (R11DT-911)</li>
<li>Service Studio is not be able to connect to Project Neo anymore. Service Studio Project Neo should be used instead. (RDEV-3959)</li>
<li>Enabled zoom capabilities in logic flows and entities diagram. (RDOIAT-324)</li>
<li>Improved overall memory consumption. (RDOIAT-474)</li>
<li>Improved the experience of using copy, paste, cut, and delete keyboard shortcuts when editing text in Service Studio. For more information about keyboard shortcuts, go to Help -&gt; Keyboard Shortcuts in Service Studio. (RDOIBT-206)</li>
<li>Now on text widgets the UnDo and ReDo operations are done with text aggregation for more efficient execution. (RTAFB-5584)</li>
</ul>
<h3 id="bug_fixing_11.52.0">Bug Fixing</h3>
<ul>
<li>Fixed an issue that gave an incorrect length attribute when importing a SOAP web service. (RPD-5047)</li>
<li>Fix missing horizontal scroll bar on traditional web apps when no device is selected. (RPM-2045)</li>
<li>Fixed an issue that prevented debugging from starting when connected with older Platform Server versions. (RPM-2198)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.52.0_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.9_start"></div>

<h2 id="cross-platform_service_studio_11.51.9">Cross-platform Service Studio 11.51.9</h2>
<div class="info"><p>Released on Mar 03, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.51.9">New in Cross-platform Service Studio 11.51.9</h3>
<ul>
<li>Users are now able to identify merge differences on screens &amp; blocks through widgets visual hints/decorations. (RDOIAT-301)</li>
</ul>
<h3 id="bug_fixing_11.51.9">Bug Fixing</h3>
<ul>
<li>Fixed an issue that gave an incorrect length attribute when importing a SOAP web service. (RPD-5047)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.9_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.8_start"></div>

<h2 id="cross-platform_service_studio_11.51.8">Cross-platform Service Studio 11.51.8</h2>
<div class="info"><p>Released on Feb 23, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.51.8">New in Cross-platform Service Studio 11.51.8</h3>
<ul>
<li>Now Table widgets can be collapsed using the display toggle button. (RTAFA-278)</li>
</ul>
<h3 id="bug_fixing_11.51.8">Bug Fixing</h3>
<ul>
<li>Fix intermittent crash when opening Service Studio. (RMAC-9105)</li>
<li>Fixed expression editor visual glitch when synchronizing with scope tree. (RMAC-9153)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.8_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.7_start"></div>

<h2 id="cross-platform_service_studio_11.51.7">Cross-platform Service Studio 11.51.7</h2>
<div class="info"><p>Released on Feb 15, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.51.7">New in Cross-platform Service Studio 11.51.7</h3>
<ul>
<li>It's now possible to use text shortcuts in Flow editor (Cut, Copy, Paste, Delete). (RDOIBT-213)</li>
<li>It's now possible to use text shortcuts in right pane tree (Cut, Copy, Paste, Delete). (RDOIBT-220)</li>
<li>Improved the design-time appearance of the List and Table widgets. The second and third iterator element now have reduced opacity to show you can't edit them. (RTAFA-276)</li>
<li>Now List widgets can be collapsed using display toggle button. (RTAFA-279)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.7_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.6_start"></div>

<h2 id="cross-platform_service_studio_11.51.6">Cross-platform Service Studio 11.51.6</h2>
<div class="info"><p>Released on Feb 09, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.51.6">New in Cross-platform Service Studio 11.51.6</h3>
<ul>
<li>Now ListItem widgets can be collapsed using display toggle button. (RTAFA-272)</li>
<li>Now If Widgets have a unique icon per toggle value to better distinguish which branch is visible  (RTAFA-275)</li>
</ul>
<h3 id="bug_fixing_11.51.6">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused manage dependencies stays loading indefinitely when Apply all option is chosen. (RDMST-894)</li>
<li>. (RICT-4268)</li>
<li>Fix issue that prevents the iterator from being updated after typing inside a TextWidget (RMAC-8345)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.6_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.5_start"></div>

<h2 id="cross-platform_service_studio_11.51.5">Cross-platform Service Studio 11.51.5</h2>
<div class="info"><p>Released on Feb 01, 2022</p></div>
<h3 id="new_in_cross-platform_service_studio_11.51.5">New in Cross-platform Service Studio 11.51.5</h3>
<ul>
<li>It is now possible to expose REST web services with the character "-" on the URL.
Inspired by <a href="https://www.outsystems.com/ideas/5205/allow-hyphen-in-url-path-of-an-exposed-api-web-method/" target="_blank" rel="noopener noreferrer">João Marques' idea</a>. (R11DT-870)</li>
</ul>
<h3 id="bug_fixing_11.51.5">Bug Fixing</h3>
<ul>
<li>Removed double error message when trying to set public blocks or screens to be reused in other modules, for Mobile Apps. (RMAC-9002)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.5_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.4_start"></div>

<h2 id="cross-platform_service_studio_11.51.4">Cross-platform Service Studio 11.51.4</h2>
<div class="info">
<p>Released on Jan 21, 2022</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.51.4">New in Cross-platform Service Studio 11.51.4</h3>
<ul>
<li>It is now possible to search for toolbox nodes using the Intelligent Quick Search feature (in Logic Assistant). (RAID-931)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.4_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.3_start"></div>

<h2 id="cross-platform_service_studio_11.51.3">Cross-platform Service Studio 11.51.3</h2>
<div class="info">
<p>Released on Jan 10, 2022</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.51.3">New in Cross-platform Service Studio 11.51.3</h3>
<ul>
<li>It is now possible to consume SOAP Web Services in your applications. (RDOIBT-194)</li>
</ul>
<h3 id="bug_fixing_11.51.3">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to become unresponsive after closing Search In Other Modules window. (RMAC-8718)</li>
<li>Fixed an issue that caused Service Studio to consider all possible dependencies invalid and the need of being republished when using manage dependencies. (RMAC-8722)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.3_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.2_start"></div>

<h2 id="cross-platform_service_studio_11.51.2">Cross-platform Service Studio 11.51.2</h2>
<div class="info">
<p>Released on Dec 28, 2021</p>
</div>
<h3 id="bug_fixing_11.51.2">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused Service Studio to become unresponsive after closing Search In Other Modules window. (RMAC-8718)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.2_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.1_start"></div>

<h2 id="cross-platform_service_studio_11.51.1">Cross-platform Service Studio 11.51.1</h2>
<div class="info">
<p>Released on Dec 21, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.51.1">New in Cross-platform Service Studio 11.51.1</h3>
<ul>
<li>Now it's possible to configure a new Database integration through the following shortcut: go to Data tab &gt; right-click on Databases &gt; select Integrate with External Databases (RDEPT-112)</li>
<li>You can now evolve your traditional web applications using the added capabilities to customize widgets on web screens. (RTAFB-5483)</li>
</ul>
<h3 id="bug_fixing_11.51.1">Bug Fixing</h3>
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
<h3 id="known_issues_11.51.1">Known Issues</h3>
<ul>
<li>In macOS Catalina, Service Studio shows a red shadow when opening dialogs. The shadow disappears after some milliseconds and doesn't affect Service Studio functionality.</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.51.1_end"></div><div class="hidden" id="cross-platform-service-studio-11.51.0_start"></div>

<h2 id="cross-platform_service_studio_11.51.0" >Cross-platform Service Studio 11.51.0</h2>
<div class="info"><p>Released on Dec 14, 2021</p></div>

<h3 id="new_in_cross-platform_service_studio_11.51.0" >New in Cross-platform Service Studio 11.51.0</h3>
<ul>
<li>Features related to emails for Mobile and Reactive Web Apps are now generally available in Service Studio. You could use the features previously in technical the previews "Emails for Mobile and Reactive" and "Attachments in Mobile and Reactive emails". (RTAFA-77)</li>
</ul>
<h3 id="bug_fixing_cross-platform_service_studio_11.51.0" >Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused a communication error when publishing a cloned app. (RDEV-3878)</li>
<li>Fixed the lack of feedback on whether a widget can be dropped or not while dragging in Service Studio Hybrid. (RDOICT-81)</li>
<li>Fixed an issue that caused Service Studio to replace the current environment connection with a different environment when the connection to that different environment is finalized in another Service Studio instance.
Fixed a crash when performing server operations while not connected to an environment. (RMAC-8544)</li>
<li>Fixed an issue where the True Change panel would appear empty after opening an older version of a module. (RMAC-8617)</li>
<li>Fixed an issue that caused the wrong feedback message to be displayed when removing unused references. (RMAC-8715)</li>
</ul>

<div class="hidden" id="cross-platform-service-studio-11.51.0_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.19_start"></div>

<h2 id="cross-platform_service_studio_11.50.19">Cross-platform Service Studio 11.50.19</h2>
<div class="info">
<p>Released on Dec 03, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.19">New in Cross-platform Service Studio 11.50.19</h3>
<ul>
<li>Installing a template (sample app) just got simpler. No dependency dialog is shown during installation. (RDEPT-3)</li>
<li>Ability to refresh existing REST Integrations, enabling additional productivity to users. (RDOIBT-83)</li>
<li>The validation rule for a mobile App Identifier in Service Center is now aligned with iOS and Android app stores. The validation messages were also updated accordingly. (RMAC-7346)</li>
<li>You can now use the grid columns to accurately resize the elements of a screen in a fixed or fluid layout. Instead of previously resizing without seeing parent's available space nor knowing the grid layout width, you now have a better idea of the available space in elements because the IDE UI shows the column number. This change makes the process of the UI design more efficient. (RTAFA-146)</li>
<li>Now you can configure friendly URLs in your Reactive Web Apps. Go to Service Center &gt; Administration &gt; SEO URLs to set up the site rules and redirects. Configure the page rules in Service Studio, by setting Custom URLs to Yes in the Screen properties. (RTAFB-4453)</li>
</ul>
<h3 id="bug_fixing_11.50.19">Bug Fixing</h3>
<ul>
<li>Fixed an issue when using the Delete shortcut on an "Unused Element" warning, which was deleting the selected element in the right pane tree instead of the "Unused Element". (RMAC-8054)</li>
<li>Fix crash when creating a new Screen through a destination node in a Screen Action. (RMAC-8282)</li>
<li>Fixed crash when opening "Manage Environments" from Login. (RMAC-8519)</li>
<li>Fixed a crash when closing Service Studio while accessing closed dialogs. (RMAC-8545)</li>
</ul>
<ul>
<li>Fixed a remote code execution vulnerability exploitable via phishing. CVSSv3.1 score 7.5 (High). (RPM-1054)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.19_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.18_start"></div>

<h2 id="cross-platform_service_studio_11.50.18">Cross-platform Service Studio 11.50.18</h2>
<div class="info">
<p>Released on Nov 23, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.18">New in Cross-platform Service Studio 11.50.18</h3>
<ul>
<li>Ability to refresh existing REST Integrations, enabling additional productivity to users. (RDOIBT-83)</li>
<li>Now it’s easier to find OutSystems UI components in Service Studio toolbox. (RIMPT-970)</li>
</ul>
<h3 id="bug_fixing_11.50.18">Bug Fixing</h3>
<ul>
<li>Service Studio no longer crashes when, after changing a 'Run Client Actions's action, the 'Expand Element' of a list argument is clicked. (RDMST-812)</li>
<li>Fixed the lack of feedback on whether a widget can be dropped or not while dragging in Service Studio. (RDOICT-81)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.18_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.17_start"></div>

<h2 id="cross-platform_service_studio_11.50.17">Cross-platform Service Studio 11.50.17</h2>
<div class="info">
<p>Released on Nov 08, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.17">New in Cross-platform Service Studio 11.50.17</h3>
<ul>
<li>Added support for WebWidget.HeaderCell in Service Studio X-Platform. (RTAFB-5331)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.17_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.16_start"></div>

<h2 id="cross-platform_service_studio_11.50.16">Cross-platform Service Studio 11.50.16</h2>
<div class="info">
<p>Released on Oct 28, 2021</p>
</div>
<p>This release of Service Studio focuses on internal improvements ― this will help our team improve Service Studio faster. Your work shouldn't be impacted by these changes.</p>
<div class="hidden" id="cross-platform-service-studio-11.50.16_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.15_start"></div>

<h2 id="cross-platform_service_studio_11.50.15">Cross-platform Service Studio 11.50.15</h2>
<div class="info">
<p>Released on Oct 26, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.15">New in Cross-platform Service Studio 11.50.15</h3>
<ul>
<li>It's now easier to select data for Table and List widgets. Click "Select Data" in the Source property dropdown to fetch and bind data from an entity in a single operation. (RIMPT-846)</li>
</ul>
<h3 id="bug_fixing_11.50.15">Bug Fixing</h3>
<ul>
<li>Fixed an issue caused by the rendering of an HTML Element widget with invalid Tag property value. (RMAC-8197)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.15_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.14_start"></div>

<h2 id="cross-platform_service_studio_11.50.14">Cross-platform Service Studio 11.50.14</h2>
<div class="info">
<p>Released on Oct 06, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.14">New in Cross-platform Service Studio 11.50.14</h3>
<ul>
<li>It's now easier to use data from your System of Records in your apps. In the "Logic" tab, open the context menu for "Integration with external systems" and select "New integration". (RIMPT-742)</li>
<li>Improved the integration of REST APIs allowing users to select methods to be imported. (RMAC-6641)</li>
</ul>
<h3 id="bug_fixing_11.50.14">Bug Fixing</h3>
<ul>
<li>Fixed a crash when trying to refresh dependencies on Manage Dependencies dialog under some circumstances (RDMST-760)</li>
<li>Fixed an issue that causes the Manage Dependencies window to open twice when using shortcuts. (RICT-3568)</li>
<li>Fixed a bug on Entity properties' dropdown that prevented the user from typing or deleting text. (RMAC-7728)</li>
<li>Fixed a crash on aggregate when an entity attribute used in a group by year column is deleted. (RMAC-8113)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.14_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.13_start"></div>

<h2 id="cross-platform_service_studio_11.50.13">Cross-platform Service Studio 11.50.13</h2>
<div class="info">
<p>Released on Sep 21, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.13">New in Cross-platform Service Studio 11.50.13</h3>
<ul>
<li>Soap Introspection testing is setup and will be triggered when prc-soap-introspection label is present on pull request. (R11DT-513)</li>
<li>You can now use expressions to set titles of Screens. This lets you change the page title dynamically, and set unique values that show in the browser tabs, bookmarks, and results from the search engines. When using this feature, it is recomended that all developers in the same organization update Service Studio. (RTAF-5082)</li>
</ul>
<h3 id="bug_fixing_11.50.13">Bug Fixing</h3>
<ul>
<li>Fixed an issue that caused the "Limit Exceeded" error to have an empty message. (RDEV-3585)</li>
<li>Added support for opening the context menu with Ctrl+Left Click on Mac. (RMAC-6068)</li>
<li>Right pane tree tabs tooltips now display the correct shortcut on macOS. (RMAC-7632)</li>
<li>Added support for dragging text from other windows to the language editors. (RMAC-7727)</li>
<li>Fixed an issue that, under certain conditions, kept the last SOAP expose item visible in the tree after being deleted, causing a crash if another deletion try occurred. (RMAC-7876)</li>
<li>Editing complex screens is now faster. (RMAC-8024)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.13_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.12_start"></div>

<h2 id="cross-platform_service_studio_11.50.12">Cross-platform Service Studio 11.50.12</h2>
<div class="info">
<p>Released on Sep 15, 2021</p>
</div>
<h3 id="bug_fixing_11.50.12">Bug Fixing</h3>
<ul>
<li>Now the Edit shortcuts are always applied to currently focused window in ServiceStudio on Mac (RICT-3706)</li>
<li>Fixed an issue that was preventing from seeing if an element was created or deleted in a merge scenario. (RMAC-7624)</li>
<li>Right pane tree tabs tooltips now display the correct shortcut on macOS. (RMAC-7632)</li>
<li>Fixed the "Open in Browser" command so it opens page with a custom URL when the technical preview "SEO-friendly URLs for Reactive Web Apps" is on. (RTAF-5032)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.12_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.11_start"></div>

<h2 id="cross-platform_service_studio_11.50.11">Cross-platform Service Studio 11.50.11</h2>
<div class="info">
<p>Released on Aug 16, 2021</p>
</div>
<h3 id="new_in_cross-platform_service_studio_11.50.11">New in Cross-platform Service Studio 11.50.11</h3>
<ul>
<li>Improved tooltip text on Publish button when with errors. (RDEV-3449)</li>
<li>Now users have a link and dedicated FAQ session in case they have difficulties in the Sign in with email. (RDRGT-92)</li>
<li>Support for new features in the email technical preview for Mobile and Reactive Web Apps, including attachments and new widgets. (RTAF-4812)</li>
</ul>
<h3 id="bug_fixing_11.50.11">Bug Fixing</h3>
<ul>
<li>Fixed template cache concurrent access issue. (RIMPT-539)</li>
<li>Improved the experience of reading and selecting text in the properties with syntax highlighting. (RMAC-4587)</li>
<li>Fixed an issue that prevented the drag of the tutorial dialog in Windows. (RMAC-7406)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.11_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.10_start"></div>

<h2 id="cross-platform_service_studio_11.50.10">Cross-platform Service Studio 11.50.10</h2>
<div class="info">
<p>Released on Aug 09, 2021</p>
</div>
<h3 id="bug_fixing_11.50.10">Bug Fixing</h3>
<ul>
<li>Fixed a bug causing the window to become maximized upon startup. Window state is now properly restored. (RICT-3776)</li>
<li>Fixed a bug that allowed zooming in Service Studio using the trackpad pinch zoom. (RMAC-7183)</li>
<li>Fix module freeze when trying to navigate from a warning message. (RMAC-7390)</li>
<li>Avoid crash when DoubleClick aggregate filter. (RMAC-7408)</li>
</ul>
<div class="hidden" id="cross-platform-service-studio-11.50.10_end"></div><div class="hidden" id="cross-platform-service-studio-11.50.9_start"></div>

<h2 id="cross-platform_service_studio_11.50.9">Cross-platform Service Studio 11.50.9</h2>
<div class="info">
<p>Released on Jul 29, 2021</p>
</div>
<h3 id="new_in_service_studio_11.50.9">New in Service Studio 11.50.9</h3>
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
<h3 id="known_issues">Known issues</h3>
<ul>
<li>Certain UI editor interactions may cause a crash and freeze that module. Please include as much information as possible whenever you submit feedback.</li>
<li>The Styles Sheet Editor button on the toolbar isn't present when selecting a widget.</li>
<li>Mobile app generation not working for Platform Server versions below 11.8.0.</li>
<li>Tooltips flicker in certain situations, you may encounter issues in styling, rendering or stealing focus.</li>
</ul>
<h3 id="features_currently_unavailable">Features currently unavailable</h3>
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
<div class="hidden" id="cross-platform-service-studio-11.50.9_end"></div><div class="hidden"><h1>Cross-platform Service Studio</h1></div>
