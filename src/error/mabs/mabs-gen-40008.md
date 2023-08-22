---
summary: There was an issue generating the app. Meta-data {0} is being defined more than once. Check the plugin documentation to ensure the setup is right.
tags:
guid: 375d8fd7-8061-4086-920a-e76ba2941f57
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-40008

## Error message

`There was an issue generating the app. Meta-data {0} is being defined more than once. Check the plugin documentation to ensure the setup is right.`

## Cause

Generating the Android application package failed because a custom plugin is overriding a metadata tag attribute in AndroidManifest.xml more than once.

## Impact

The Android application package can't be generated.

## Recommended action

Identify which custom plugins are overriding the metadata attribute more than once. Note that a metadata tag attribute can only be set once across the project. 

Learn more about managing these conflicts [here](https://cordova.apache.org/docs/en/latest/plugin_ref/spec.html#managing-edit-config-conflicts).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40008).
