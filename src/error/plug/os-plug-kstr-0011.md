---
summary: OS-PLUG-KSTR-0011 is an iOS Keychain catch-all error from the Keystore plugin. Restart the device to reset the Keychain state.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 0b36bed8-68fe-4e8f-a057-7fbc009ee81c
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

# OS-PLUG-KSTR-0011

## Error message

An error just occurred.

## Platform

iOS

## Cause

An unexpected error occurred in the iOS Keychain that is not covered by any specific error type. This is a catch-all error returned when the iOS Security framework returns a status code not explicitly handled by the plugin. It may be caused by an inconsistent Keychain state, a system-level issue, or an unexpected iOS behavior.

## Impact

The requested Keystore operation cannot be performed.

## Recommended action

Try the operation again. If the error occurs consistently, restart the device to reset the Keychain state.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0011).
