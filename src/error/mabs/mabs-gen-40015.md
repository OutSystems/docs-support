---
summary: There was an issue generating the app. At least one Cordova plugin is not compatible with the ”Swift Language Version” build setting that was defined. Check your plugin configurations and try again.
tags:
guid: 845308e6-f01c-4b24-be56-0924158c7db8
locale: en-us
app_type: mobile apps
platform-version: o11
---

# OS-MABS-GEN-40015

## Error message

`There was an issue generating the app. At least one Cordova plugin is not compatible with the ”Swift Language Version” build setting that was defined. Check your plugin configurations and try again.`

## Cause

Generatign the iOS application package failed because at least one custom plugin is incompatible with the defined ”Swift Language Version”.

## Impact

The iOS application package can't be generated.

## Recommended action

Check the build logs on Service Center and identify the affected custom plugin configuration. Then, update the configuration to ensure they are compatible with the defined ”Swift Language Version”.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40015).
