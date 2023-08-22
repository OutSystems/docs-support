---
summary: Couldn't install the Cordova plugin <plugin_name>. Using "requireCordovaModule" to load a non-Cordova module <node_module> is not supported. Add this module to your dependencies and use the regular "require" to load it.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 93b1a435-7e75-4617-a687-9e41697beef6
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-40015

## Error message

`Couldn't install the Cordova plugin <plugin_name>. Using
"requireCordovaModule" to load a non-Cordova module <node_module> is not
supported. Add this module to your dependencies and use the regular "require"
to load it.`

## Cause

This error happened because the plugin **&lt;plugin_name&gt;** was trying to use
“requireCordovaModule” to load the non-Cordova module **&lt;node_module&gt;** on an
installation hook.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center to confirm which custom plugin is using
requireCordovaModule to load a non-Cordova module. Then, go to that plugin and
replace “requireCordovaModule” with “require”.

Learn more about generating mobile apps and how to get the build logs
[here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40015).
