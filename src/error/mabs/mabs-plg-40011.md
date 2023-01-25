---
summary: Couldn't install the Cordova plugin <plugin_name> due to an issue with the plugin specification. Check the plugin name, version, and URL in both the plugin.xml and package.json files.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 31def9a5-0a39-4ab8-bf51-bf46d8898ab1
---

# OS-MABS-PLG-40011

## Error message

`Couldn't install the Cordova plugin <plugin_name> due to an issue with the
plugin specification. Check the plugin name, version, and URL in both the
plugin.xml and package.json files.`

## Cause

This error occurs when the plugin **&lt;plugin_name&gt;** isn't well defined.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and verify the plugin
name, version, and URL in both the plugin.xml and package.json files. After fixing
it, try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40011).
