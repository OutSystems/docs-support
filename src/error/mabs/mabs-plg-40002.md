---
summary: Couldn't install the Cordova plugin <plugin_name> because one or more plugin variables are missing
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 71e5b5d3-235f-4a68-90ee-c2d7b74d9f21
---

# OS-MABS-PLG-40002

## Error message

`Couldn't install the Cordova plugin <plugin_name> because one or more plugin
variables are missing.`

## Cause

This error occurs when the provided plugin requires some variables that are
missing in the extensibility configurations of the plugin module.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and after fixing it,
try to generate your application again.

You can follow this documentation on [how to use Cordova
plugins](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/Using_Cordova_Plugins).

If the problem persists, create a case with [OutSystems
support](https://success.outsystems.com/Support).
