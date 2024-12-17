---
summary: Invalid {0} type in your extensibility configurations. Review it and try again.
tags: extensibility configurations, error resolution, configuration management, mobile app development
guid: 53eb9fbf-6dc5-43ad-ab70-69a709bfc9b4
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
  - platform administrators
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# OS-MABS-CNF-40005

## Error message

`Invalid {0} type in your extensibility configurations. Review it and try again.`

## Cause

This error occurs when some property in the extensibility configuration is invalid.

If in ODC you use Settings on your app, this error occurs when you are referencing Secret and/or Binary Settings in extensibility configurations with no value set.

## Impact

The application package can't be generated.

## Recommended action

Check the extensibility configurations of your app and ensure that there are no invalid properties.

If you are in ODC, ensure each Setting referenced in the extensibility configurations has a value defined. Find more information about settings [here](https://success.outsystems.com/documentation/outsystems_developer_cloud/configuration_management/#managing-settings)

Find more information about the extensibility configuration [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-CNF-40005).
