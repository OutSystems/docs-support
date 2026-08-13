---
summary: The Keystore plugin attempted a Keychain operation that is not implemented on the current iOS version or device.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 01cfc035-54cc-49b6-90a9-db2a7cd30267
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

# OS-PLUG-KSTR-0002

## Error message

Function or operation not implemented.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecUnimplemented` status, indicating that the requested Keychain function or operation is not available on the current iOS version or device configuration.

## Impact

The requested Keystore operation cannot be performed.

## Recommended action

Verify that the iOS version running on the device meets the minimum requirements for the Keystore plugin. Ensure the plugin version in use is compatible with the target iOS version.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0002).
