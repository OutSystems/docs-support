---
summary: The Android device does not have a secure screen lock configured, which is required by the Keystore plugin.
tags:
  - Android
  - Mobile app
  - Plugins
  - Security
  - Troubleshooting
locale: en-us
guid: 35613f08-3459-4708-8e65-6e8d0b36c684
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

# OS-PLUG-KSTR-0014

## Error message

Device is not secure.

## Platform

Android

## Cause

The Android device does not have a secure screen lock configured (PIN, pattern, password, fingerprint, or face recognition). The Keystore plugin requires device security to protect data stored with authentication enabled, as the Android Keystore system relies on the device's lock screen credentials to secure the encryption keys.

## Impact

The Keystore operation cannot be completed because the device does not meet the minimum security requirements.

## Recommended action

Ask the user to set up a secure screen lock on the device by going to **Settings > Security > Screen Lock** and selecting a secure option (PIN, pattern, password, fingerprint, or face recognition). After setting up the lock screen, retry the operation.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0014).
