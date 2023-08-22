---
summary: There was an issue generating the app. Library {2} requires minimum Android SDK {1}, which is higher than the {0} required by the app. Check if this value is being overridden in your extensibility configurations.
tags:
guid: 596468f6-899f-40c4-94d4-1d9a8e33e88a
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-40009

## Error message

`There was an issue generating the app. Library {2} requires minimum Android SDK {1}, which is higher than the {0} required by the app. Check if this value is being overridden in your extensibility configurations.`

## Cause

Generating the Android application package failed because a custom plugin library requires the minimum Android SDK to be higher than the one used by the application.

## Impact

The Android application package can't be generated.

## Recommended action

Check if the minimum Android SDK is being overridden in your extensibility configurations; change it to a higher Android SDK and/or replace the custom plugin affected library. Learn more about this [here](https://cordova.apache.org/docs/en/11.x/config_ref/#:~:text=android%2DminSdkVersion(integer)).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40009).
