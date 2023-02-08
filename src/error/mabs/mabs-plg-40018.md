---
summary: <plugin_id> version <plugin_version> must be <plugin_min_version> or higher.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 817de060-a43d-41aa-96d1-61dda2855929
platform-version: o11, odc
---

# OS-MABS-PLG-40018

## Error message

`<plugin_id> version <plugin_version> must be <plugin_min_version> or higher.`

## Cause

This error occurs when a Cordova plugin isn't compatible with a specific MABS
version (MABS 7 or higher). The **&lt;plugin_id&gt;** refers to the plugin
identifier on the repository. The **&lt;plugin_version&gt;** refers to the
version of the plugin you are trying to use. The **&lt;plugin_min_version&gt;**
refers to the minimum plugin version compatible with the MABS version
that you are trying to use.

## Impact

Users can't generate the application package.

## Recommended action

Update your plugin version to **&lt;plugin_min_version&gt;** or higher. Check
the [plugin’s
documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins)
for more information.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40018).
