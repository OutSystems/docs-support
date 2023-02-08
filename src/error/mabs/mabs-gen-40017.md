---
summary: There was an issue generating the app. Gradle now requires you to declare dependencies using “implementation” or “api” instead of “compile”. The dependency being incorrectly declared is “{0}”. Check your plugin configurations and try again.
tags:
guid: 90030a88-ff2b-40c8-b0d8-e8a7bc20966e
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-GEN-40017

## Error message

`There was an issue generating the app. Gradle now requires you to declare dependencies using “implementation” or “api” instead of “compile”. The dependency being incorrectly declared is “{0}”. Check your plugin configurations and try again.`

## Cause

This error occurs when you are generating an Android package with MABS 8 or higher because Gradle 7 or higher doesn't support `compile` as a way to declare dependencies.

## Impact

The Android application package can't be generated.

## Recommended action

Check the build logs on Service Center to identify the affected custom plugin and replace `compile` dependencies in Gradle files with `implementation` or `api`.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40017).
