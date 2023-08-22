---
summary: Couldn't install the Cordova plugin <plugin_name> because it's not supported by MABS 6.0 and later versions. Please update your plugin.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: be6c801f-e6cb-4e9e-b858-caea2d8700d1
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-40012

## Error message

`Couldn't install the Cordova plugin <plugin_name> because it's not supported
by MABS 6.0 and later versions. Please update your plugin.`

## Cause

This error occurs when the plugin **&lt;plugin_name&gt;** is trying to change the tag
`<uses-sdk>` on the AndroidManifest.xml file. From MABS 6 versions onwards
this is no longer possible.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and change the plugin
or the MABS version. Then, try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40012).
