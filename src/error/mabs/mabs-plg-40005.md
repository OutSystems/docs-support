---
summary: Couldn't install the Cordova plugin <plugin_name> due to an error in the plugin.xml file. The Spec attribute in the Framework element related to CocoaPods is invalid.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 6ed71f5f-bef6-4a82-a1f3-9d977224a5a0
platform-version: o11, odc
---

# OS-MABS-PLG-40005

## Error message

`Couldn't install the Cordova plugin <plugin_name> due to an error in the
plugin.xml file. The Spec attribute in the Framework element that is related to
CocoaPods is invalid.`

## Cause

This error occurs when the provided plugin has an invalid configuration in the
iOS platform. The Spec attribute in the Framework element related to CocoaPods
is invalid.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and after fixing the
affected plugin, try to generate your application again.

You can follow the official Cordova plugin documentation on the [plugin.xml
configurations](https://cordova.apache.org/docs/en/latest/plugin_ref/spec.html).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40005).
