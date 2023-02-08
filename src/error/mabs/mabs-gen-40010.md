---
summary: There was an issue generating the app. Some plugins are using conflicting dependencies from Google Play services. Check your plugin configurations and try again.
tags:
guid: 01eaf9bb-abf4-40ef-862d-92541ac78355
locale: en-us
app_type: mobile apps
platform-version: o11
---

# OS-MABS-GEN-40010

## Error message

`There was an issue generating the app. Some plugins are using conflicting dependencies from Google Play services. Check your plugin configurations and try again.`

## Cause

Generating the Android application package failed due to conflicting dependencies from Google Play services on custom plugins.

## Impact

The Android application package can't be generated.

## Recommended action

Identify which custom plugins have Google Play services dependencies and fix the conflicts on the plugin side.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40010).
