---
summary: There was an issue generating the app. Using “requireCordovaModule” to load non-cordova module {0} is not supported. Instead, add this module to your dependencies and use regular “require” to load it.
tags:
guid: 9e1ac667-436a-488a-bfa5-9dd2c4ad2de9
locale: en-us
app_type: mobile apps
---

# OS-MABS-GEN-40013

## Error message

`There was an issue generating the app. Using “requireCordovaModule” to load non-cordova module {0} is not supported. Instead, add this module to your dependencies and use regular “require” to load it.`

## Cause

Generating the application package failed because “requireCordovaModule” can’t be used to load a non-cordova module.

## Impact

The application package can't be generated.

## Recommended action

Check the build logs on Service Center to confirm which custom plugin is using “requireCordovaModule” to load a non-cordova module; replace “requireCordovaModule” with “require” in the plugin.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://success.outsystems.com/Support).
