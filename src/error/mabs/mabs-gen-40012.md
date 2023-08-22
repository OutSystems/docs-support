---
summary: There was an issue generating the app. Some plugins using CocoaPods aren’t correctly configured or a pod wasn’t found in the repository. Check your plugin configurations and try again.
tags:
guid: 971cea53-2f31-4a83-91aa-c413944cd3c1
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-40012

## Error message

`There was an issue generating the app. Some plugins using CocoaPods aren’t correctly configured or a pod wasn’t found in the repository. Check your plugin configurations and try again.`

## Cause

Generating the iOS application package failed because Cocoapods aren't configured correctly or a pod can’t be found in the repository.

## Impact

The iOS application package can't be generated.

## Recommended action

Check the build logs on Service Center to confirm which pod is affected and identify which custom plugin is introducing it. Then, check the plugin Cocoapods configuration.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40012
).
