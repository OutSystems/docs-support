---
summary: There was an issue generating the app. At least one Cordova plugin used in the build requires Swift, but no ”Swift Language Version” build setting was defined. Check your plugin configurations and try again.
tags:
guid: dcef6454-300b-4c9a-a6ae-4bbca583a32a
locale: en-us
app_type: mobile apps
---

# OS-MABS-GEN-40003

## Error message

`There was an issue generating the app. At least one Cordova plugin used in the build requires Swift, but no ”Swift Language Version” build setting was defined. Check your plugin configurations and try again.`

## Cause

Generating the iOS application package failed because at least one custom plugin requires Swift, but no configuration was defined for the iOS project.

## Impact

The iOS application package can't be generated.

## Recommended action

Check the build logs on Service Center and confirm which plugin requires Swift language configuration.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40003).
