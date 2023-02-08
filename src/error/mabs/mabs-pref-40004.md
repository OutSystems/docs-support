---
summary: Preferences must have the format {}.
tags:
guid: 32d1797b-e3e5-4c00-bb48-1b0513977e9b
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-PREF-40004

## Error message

`Preferences must have the format {}.`

## Cause

This error occurs when the application's extensibility configuration preferences is not a JSON object.

## Impact

Users can't generate the application package.

## Recommended action

Fix the application extensibility configuration, following the [Property Schema](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema#property-schema) and try rebuilding your application.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PREF-40004).
