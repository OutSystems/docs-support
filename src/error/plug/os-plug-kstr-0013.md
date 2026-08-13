---
summary: The biometric authentication required to access the Android encrypted storage failed or was cancelled.
tags:
  - Android
  - Authentication
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 23b8edf7-0c0b-44d6-bd0d-ea01feb6d8c2
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

# OS-PLUG-KSTR-0013

## Error message

Failed to authenticate user.

## Platform

Android

## Cause

The biometric authentication required to complete a Keystore operation with authentication enabled failed or was cancelled. This occurs when the user dismisses the biometric prompt, provides incorrect biometric data, or fails authentication too many times, causing the system to lock the biometric prompt.

## Impact

The Keystore operation (`set`, `get`, or `remove`) that requires biometric authentication cannot be completed.

## Recommended action

Ask the user to retry the operation and complete the biometric authentication when the prompt appears. If biometric authentication fails repeatedly, the user can authenticate using their device credentials (PIN, pattern, or password).

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0013).
