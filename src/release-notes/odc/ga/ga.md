---
locale: en-us
guid: 0ac836fd-7a90-4086-a096-5d5a8263b8c5
app_type: mobile apps, reactive web apps
platform-version: odc
---

<div class="hidden"><h1>OutSystems Developer Cloud</h1></div>

<div class="hidden" id="outsystems-developer-cloud-2023-02-04_start"></div>

<h2 id="outsystems_developer_cloud_2023-02-04" >OutSystems Developer Cloud 2023-02-04</h2>
<div class="info"><p>Released on Feb 04, 2023</p></div>

<ul><li>This release of the OutSystems Developer Cloud focuses on internal improvements. Your work shouldn't be impacted by these changes.</li></ul><div class="hidden" id="outsystems-developer-cloud-2023-02-04_end"></div><div class="hidden" id="outsystems-developer-cloud-2023-02-03_start"></div>

<h2 id="outsystems_developer_cloud_2023-02-03" >OutSystems Developer Cloud 2023-02-03</h2>
<div class="info"><p>Released on Feb 03, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_outsystems_developer_cloud_2023-02-03" > New</h3>
<ul>
<li>Apps - Improved the Apps list performance when loading the page after 5 minutes of inactivity. This improvement will be more noticeable on APAC region, where it was taking longer to load. (RDPP-1067)</li>
<li>ODC Portal users can now use Apple IdP accelerator to configure a new external IdP. This accelerator requires Client ID (Identifier), Key ID, Team ID and the Client secret (Secret .p8) and can be quickly used to set up this new provider. (RDPP-975)</li>
</ul>

<div class="hidden" id="outsystems-developer-cloud-2023-02-03_end"></div><div class="hidden" id="outsystems-developer-cloud-2023-01-31_start"></div>

<h2 id="outsystems_developer_cloud_2023-01-31" >OutSystems Developer Cloud 2023-01-31</h2>
<div class="info"><p>Released on Jan 31, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_outsystems_developer_cloud_2023-01-31" >Bug Fixing</h3>
<ul>
<li>Apps - Removed the 'Open in ODC Studio' option from extension libraries. (RDLOT-1479)</li>
<li>Apps - Added an informative text on App detail configurations, explaining that the timer schedule is presented in UTC time.   (RDLOT-1523)</li>
<li>Apps - The 'Delete' feature is now also available for non-deployed apps. (RDLOT-1564)</li>
<li>Apps - The App Identifier validation for Android was reviewed and it no longer allows the underscore character, which was generating some issues on the mobile package creation. (RDLOT-1591)</li>
</ul>

<div class="hidden" id="outsystems-developer-cloud-2023-01-31_end"></div><div class="hidden" id="outsystems-developer-cloud-2023-01-24_start"></div>

<h2 id="outsystems_developer_cloud_2023-01-24" >OutSystems Developer Cloud 2023-01-24</h2>
<div class="info"><p>Released on Jan 24, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_outsystems_developer_cloud_2023-01-24" >Bug Fixing</h3>
<ul>
<li>Fixed GetRequestURL action returning different values when the request was made during a debug session (RTAFB-6318)</li>
</ul>

<div class="hidden" id="outsystems-developer-cloud-2023-01-24_end"></div><div class="hidden" id="outsystems-developer-cloud-2023-01-20_start"></div>

<h2 id="outsystems_developer_cloud_2023-01-20" >OutSystems Developer Cloud 2023-01-20</h2>
<div class="info"><p>Released on Jan 20, 2023</p></div>

<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_outsystems_developer_cloud_2023-01-20" > New</h3>
<ul>
<li>Monitoring - Added missing elements to the Element filter on the Traces page, namely ‘Entity Action', ‘Server Action', and 'Consumed REST API'. (RDLOT-1463)</li>
<li>ODC Portal user can now have the user photo that is sent by default in the picture claim when integrated with external IdPs.

The ODC User with Manage organization roles can change the mapping from picture to another alternative mapping inside the External IdP configuration screen.

The picture is now available in the ODC profile and user list, and will be soon available in the Apps as well. (RDPP-818)</li>
</ul>
<h3 id="bug_fixing_outsystems_developer_cloud_2023-01-20" >Bug Fixing</h3>
<ul>
<li>Monitoring - Fixed the User filter behavior on the Traces and Logs pages, which was breaking on smaller screen resolutions. (RDLOT-1487)</li>
<li>Monitoring - Improved the 'Show more' behavior on the Span details section under the Trace detail page, which sometimes was appearing even when there was no more information to show. (RDLOT-1496)</li>
</ul>
<div class="hidden" id="outsystems-developer-cloud-2023-01-20_end"></div><div class="hidden" id="outsystems-developer-cloud-2023-01-13_start"></div>

<h2 id="outsystems_developer_cloud_2023-01-13" >OutSystems Developer Cloud 2023-01-13</h2>
<div class="info"><p>Released on Jan 13, 2023</p></div>


<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="new_in_outsystems_developer_cloud_2023-01-13" > New</h3>
<ul>
<li>Forge governance and user experience improvements:
<ul>
<li>Forge - Users without an Install &amp; Update permissions don't have the Install button available.</li>
<li>Forge - Users without an Submission permissions cannot start the submit process nor can edit assets submitted by others from their Organization.</li>
<li>Forge - Redesign of the asset detail page, to allow a better experience when using smaller screen resolutions.</li>
</ul> (RDFNO-132)</li>
<li>Improvements in the Forge Submit experience:
<ul>
<li>Forge - It's now possible to submit the last versioned App revision while new revisions are being created in ODC Studio.</li>
<li>Forge - New pop-up when dependencies are missing in Forge, detailing the status of each asset.</li>
<li>Forge - New option to add links in the detailed description, Limitations, and Documentation.</li>
<li>Forge - New Image uploader component, consistent inside ODC Portal.</li>
</ul> (RMKPT-2218)</li>
</ul>
<h3 id="bug_fixing_outsystems_developer_cloud_2023-01-13" >Bug Fixing</h3>
<ul>
<li>Forge - Fixed an issue that was not allowing the users to see the assets listed in both tabs of the My Assets page in Forge. (RMKPT-2188)</li>
</ul>

<div class="hidden" id="outsystems-developer-cloud-2023-01-13_end"></div><div class="hidden" id="outsystems-developer-cloud-2023-01-05_start"></div>

<h2 id="outsystems_developer_cloud_2023-01-05" >OutSystems Developer Cloud 2023-01-05</h2>
<div class="info"><p>Released on Jan 05, 2023</p></div>

<style>.cattag {background: #f4f2ff; color: #6a6581; padding: 4px 10px;}</style>
<h3 id="bug_fixing_outsystems_developer_cloud_2023-01-05" >Bug Fixing</h3>
<ul>
<li>Fixed an issue where the user could be blocked during the impact analysis step in the deployment of a mobile app due to permission configurations. (RDEL-1171)</li>
<li>Monitoring - Fixed an issue that was throwing an error message when the previous time range selected had an invalid search period (i.e. start date was prior to 30 days, and the selected period exceeded the 14 days). (RDLOT-1488)</li>
</ul>
<div class="hidden" id="outsystems-developer-cloud-2023-01-05_end"></div><div class="hidden"><h1>OutSystems Developer Cloud</h1></div>
