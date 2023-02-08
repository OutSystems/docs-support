---
summary: Couldn't install the Cordova plugin <plugin_name> because the plugin dependency <plugin_dependency> doesn't support this Cordova version.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: b050a69e-17e6-46a8-aef5-d1c21a4f1c1f
platform-version: o11
---

# OS-MABS-PLG-40017

## Error message

`Couldn't install the Cordova plugin <plugin_name> because the plugin
dependency <plugin_dependency> doesn't support this Cordova version.`

## Cause

This error occurs when the plugin **&lt;plugin_name&gt;** has a dependency declared
which is incompatible with the Cordova version (or Cordova platform version)
this MABS version is using.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center and fix the plugin dependency to match
the Cordova version or change the MABS version to a version compatible with the
plugin. Then, try to generate your application again.

You can check the [release
notes](https://success.outsystems.com/Support/Release_Notes/Mobile_Apps_Build_Service_Versions)
page of the MABS version you are using to validate the versions for Cordova CLI
or Cordova engine (android/ios).

Learn more about generating mobile apps and how to get the build logs
[here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40017).
