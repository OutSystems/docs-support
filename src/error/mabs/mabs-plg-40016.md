---
summary: Couldn't install the Cordova plugin due to a missing dependency in module <node_module>. Check your plugin dependencies and try again.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: fc687c8b-e95e-4241-9995-48bf3ec6c96d
platform-version: o11, odc
---

# OS-MABS-PLG-40016

## Error message

`Couldn't install the Cordova plugin due to a missing dependency in module
<node_module>. Check your plugin dependencies and try again.`

## Cause

This error happened because the installation of the plugin requires the node
module **&lt;node_module&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center to confirm which custom plugin requires
the missing node module and fix the dependency.

From MABS 7 upwards (see
[here](https://success.outsystems.com/Support/Release_Notes/Mobile_Apps_Build_Service_Versions/MABS_7_Release_notes#:~:text=Xcode%20required%20in%20package.json)),
plugins are installed using Cordova fetch and they need the hooks
dependencies declared on the plugin package.json.

Learn more about generating mobile apps and how to get the build logs
[here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40016).
