---
summary: Couldn't install the Cordova plugin <plugin_name> due to an error in the plugin.xml file. The Spec attribute in the Framework element related to CocoaPods is invalid.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 896b87e9-3200-4c79-bc48-f06de30c6b0f
---

# OS-MABS-PLG-40004

## Error message

`Couldn't install the Cordova plugin <plugin_name> due to an error in the
plugin.xml file. There's a missing Spec attribute in the Framework element
related to CocoaPods.`

## Cause

This error occurs when the provided plugin has an invalid configuration in the
iOS platform. There's a missing Spec attribute in the Framework element related
to CocoaPods.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and after fixing the
affected plugin, try to generate your application again.

You can follow the official Cordova plugin documentation on the [plugin.xml
configurations](https://cordova.apache.org/docs/en/latest/plugin_ref/spec.html).

If the problem persists, create a case with [OutSystems
support](https://success.outsystems.com/Support).
