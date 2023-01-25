---
summary: There was an issue generating the app. The Cordova plugin {0} is not compatible with the ”Swift Language Version” build setting that was defined. Check your plugin configurations and try again.
tags:
guid: f98cf59e-ed4f-4b06-9f97-e755adc0c2d9
locale: en-us
app_type: mobile apps
---

# OS-MABS-GEN-40014

## Error message

`There was an issue generating the app. The Cordova plugin {0} is not compatible with the ”Swift Language Version” build setting that was defined. Check your plugin configurations and try again.`

## Cause

Generating the iOS application package failed because a custom plugin is incompatible with the defined ”Swift Language Version”.

## Impact

The iOS application package can't be generated.

## Recommended action

Check the build logs on Service Center and identify the affected custom plugin configuration. Then, update the configuration to ensure they are compatible with the defined ”Swift Language Version”.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40014).
