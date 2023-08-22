---
summary: The AppShield plugin has more than one reference in your app.
tags:
guid: 23dda976-243f-411b-86bf-4447d15755a1
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SHLD-40001

## Error message

`The AppShield plugin has more than one reference in your app.`

## Cause

This error occurs when there is more than one reference of the AppShield plugin in your app.

## Impact

The application package can't be generated.

## Recommended action

Check if there's any duplicated reference to the AppShield plugin in your app and/or on its dependencies in the extensibility configurations and remove them. There can only be one reference to the plugin and it should be on the AppShield plugin retrieved from the Forge.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SHLD-40001).
