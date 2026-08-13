---
summary: The biometric or passcode authentication required to access the Keychain item failed.
tags:
  - Authentication
  - End-user Authentication
  - iOS
  - Mobile app
  - Plugins
  - Security
  - Troubleshooting
locale: en-us
guid: 4d757101-1575-4439-b18d-b3596c3343e0
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

# OS-PLUG-KSTR-0010

## Error message

The user name or passphrase you entered is not correct.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecAuthFailed` status, indicating that the authentication required to access a protected Keychain item failed. This occurs when the user provides incorrect biometric data (Face ID or Touch ID), an incorrect passcode, or when the maximum number of failed authentication attempts has been exceeded.

## Impact

The protected Keychain item cannot be accessed, and the `get` or `set` operation with access control cannot be completed.

## Recommended action

Ask the user to retry the operation and authenticate using the correct biometric credentials or passcode. If biometric authentication is locked due to too many failed attempts, the user may need to enter their device passcode to unlock it.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0010).
