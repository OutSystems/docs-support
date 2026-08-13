---
summary: The iOS Keychain is not available. The device may need to be unlocked or restarted.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 6c619ca6-5f8e-4e84-9377-29e22608a9f4
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

# OS-PLUG-KSTR-0005

## Error message

No Keychain is available. A restart may be needed.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecNotAvailable` status, indicating the Keychain is temporarily inaccessible. This commonly occurs when the device has recently started but the user has not yet unlocked it for the first time (before first unlock), which is a state where the Keychain is protected and unavailable to apps.

## Impact

The requested Keystore operation cannot be performed.

## Recommended action

Ensure the device is fully unlocked before using the Keystore plugin. If the error occurs after the first unlock, restart the device and try again.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0005).
