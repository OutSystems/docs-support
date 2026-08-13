---
summary: The Keystore plugin operation failed because one or more required arguments are missing or invalid.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 9c8d4637-9a1b-4c02-8290-4a2210829363
app_type: mobile apps
platform-version: odc,o11
figma:
audience:
  - Developer
  - Front-end developer
outsystems-tools:
  - service studio
  - odc studio
coverage-type:
  - unblock
topic:
  - using-cordova-plugins
  - wrap-cordova-plugin
isautopublish: true
---

# OS-PLUG-KSTR-0001

## Error message

Some of the arguments are not valid.

## Platform

iOS

## Cause

One or more required arguments passed to the Keystore plugin operation are missing or empty. This happens when the plugin's `get`, `set`, `remove`, `keys`, or `clear` methods are called without providing all the required Text parameters (such as `service` or `key`).

## Impact

The requested Keystore operation cannot be performed.

## Recommended action

Check that all required parameters for the plugin method are provided and are valid non-empty Text values. Refer to the plugin documentation for the expected parameters for each operation.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0001).
