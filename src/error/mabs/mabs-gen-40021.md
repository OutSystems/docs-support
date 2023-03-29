---
summary: Couldn't generate your app. Kotlin version <used_version> isn't compatible with this app. Update it to <minimum_version> or higher.
tags:
guid: 95ca1b7b-faec-4f9c-a88b-6316f0e19a88
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-GEN-40021

## Error message

`Couldn't generate your app. Kotlin version <used_version> isn't compatible with this app. Update it to <minimum_version> or higher.`

## Cause

The Kotlin version is not compatible with the plugins used in the app. This version is usually defined in the `GradlePluginKotlinVersion` preference in the Extensibility Configurations or in a plugin's specialised hook.

## Impact

Users can't generate the application package.

## Recommended action

Check if the main module of your app includes the `GradlePluginKotlinVersion` preference in the Extensibility Configurations and remove it or replace it for a compatible version.

Check also if a plugin is modifying the used Kotlin version.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40021).
