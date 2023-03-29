---
summary: Couldn't generate your app. It's configured to use Android Build Tools version <used_version>, but the version can't be modified. Check if it's being overridden in your extensibility configurations or via a plugin.
tags:
guid: 72dac8b4-2950-4aa6-a249-bd7fd75b9e4a
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-GEN-40020

## Error message

`Couldn't generate your app. It's configured to use Android Build Tools version <used_version>, but the version can't be modified. Check if it's being overridden in your extensibility configurations or via a plugin.`

## Cause

MABS doesn't allow the used Android Build Tools version to be modified. This version may be being modified using the `android-buildToolsVersion` preference in the Extensibility Configurations or in a specialized hook (Gradle plugin/script or more) inside a Cordova plugin.

## Impact

Users can't generate the application package.

## Recommended action

Check if the main module of your app includes the `android-buildToolsVersion` preference in the Extensibility Configurations and remove it.

Check also if a plugin is modifying the used Android Build Tools version.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40020).
