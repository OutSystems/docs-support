---
summary: Couldn't install the Cordova plugin <plugin_name> due to an error in the plugin.xml file. The specified pod wasn't found in the CocoaPods repository.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 3c42415f-71e0-49ac-8626-52a23d2fd05a
---

# OS-MABS-PLG-40006

## Error message

`Couldn't install the Cordova plugin <plugin_name> due to an error in the
plugin.xml file. The specified pod wasn't found in the CocoaPods repository.`

## Cause

This error occurs when the provided plugin is pointing to a pod that doesn't
exist in the CocoaPods repository.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and after fixing the
pod dependency on the affected plugin, try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://success.outsystems.com/Support).
