---
summary: Couldn't install the Cordova plugin <plugin_name> because your plugin doesn't support this Cordova version.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: b5e10182-7b82-440f-9892-0cebd7e29755
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-40009

## Error message

`Couldn't install the Cordova plugin <plugin_name> because your plugin doesn't
support this Cordova version.`

## Cause

This error occurs when the plugin **&lt;plugin_name&gt;** isn't compatible with the
Cordova version (or Cordova platform version) this MABS version is using.

## Impact

Users can't generate the application package.

## Recommended action

Check the build log for more details and fix the plugin to match the Cordova
version or change the MABS version to a version compatible with the plugin.
Then, try to generate your application again.

You can check the [release
notes](https://success.outsystems.com/Support/Release_Notes/Mobile_Apps_Build_Service_Versions)
page of the MABS version you are using to validate the versions for Cordova cli
or Cordova engine (android/ios).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40009).
