---
summary: Couldn't compile the Cordova plugin <plugin_name>. Review your plugin configurations and check our documentation for more information if the problem persists.
tags:
guid: aa28c280-cf1b-4279-802f-456617bbb753
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-40019

## Error message

`Couldn't compile the Cordova plugin <plugin_name>. Review your plugin configurations and check our documentation for more information if the problem persists.`

## Cause

The plugin source code failed to compile, during the compilation phase of the application package. The most frequent cause for this error is a malformed plugin's resource.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center and confirm if any of the plugin's resources are malformed.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40019).
