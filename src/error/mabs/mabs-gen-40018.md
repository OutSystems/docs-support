---
summary: There was an issue generating the app. Whitelist Plugin was renamed AllowList in newer Cordova Android engine versions. Check your plugin code and try again.
tags:
guid: 0fdc2abc-b67c-43f0-bb3d-3bdcfcdd5496
locale: en-us
app_type: mobile apps
---

# OS-MABS-GEN-40018

## Error message

`There was an issue generating the app. Whitelist Plugin was renamed AllowList in newer Cordova Android engine versions. Check your plugin code and try again.`

## Cause

This error occurs when you generate an Android package with MABS 8 or higher because, with Cordova Android version 10.0.0 and higher, the Whitelist plugin was renamed to AllowList, which broke all references to Whitelist-related classes.

## Impact

The Android application package can't be generated.

## Recommended action

Check the build logs on Service Center to identify the affected custom plugin and change `Whitelist` references for `Allowlist`.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://success.outsystems.com/Support).
