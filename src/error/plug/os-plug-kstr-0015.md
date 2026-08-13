---
summary: 'OS-PLUG-KSTR-0015 Keystore plugin error on Android: fix an EncryptedSharedPreferences access failure caused by a corrupted key or hardware security issue.'
tags:
  - Android
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 4f41278c-9e9d-47e3-a72a-089a0b11d012
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

# OS-PLUG-KSTR-0015

## Error message

There was an error accessing the KeyStore.

## Platform

Android

## Cause

An unexpected error occurred while reading from or writing to the Android encrypted storage (`EncryptedSharedPreferences`). This can happen due to a corrupted encryption key in the Android Keystore, a hardware security module issue, or an unexpected Android system state that prevents access to the encrypted storage.

## Impact

The requested Keystore operation (`set`, `get`, or `remove`) cannot be performed.

## Recommended action

Try the operation again. If the error occurs consistently, it may indicate corruption in the encrypted storage. In that case, clearing the app's data in **Settings > Apps > `APP_NAME` > Storage > Clear Data** may resolve the issue. Replace `APP_NAME` with the name of your app. Note that clearing the app's data will result in the loss of all data stored by the Keystore plugin.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0015).
