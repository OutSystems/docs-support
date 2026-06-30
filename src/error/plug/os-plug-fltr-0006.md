---
summary: OS-PLUG-FLTR-0006 error on Android means the OutSystems platform file transfer plugin failed because the user denied storage permissions.
tags:
  - Android
  - Cordova
  - Mobile app
  - Plugins
  - Security
  - Troubleshooting
locale: en-us
guid: a3c26cad-0952-4388-9696-e292e042b1a7
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

# OS-PLUG-FLTR-0006

## Error message

Unable to perform operation, user denied permission request.

## Platform

Android

## Cause

On Android, accessing the device's file system requires storage permissions. This error occurs when the user denies the permission request, causing the Android OS to throw a `SecurityException` that the plugin catches and maps to this error.

This doesn't occur on recent Android versions (Android 13 and later), where scoped storage is used and these storage permissions are no longer required.

## Impact

The file transfer operation fails. The file won't be uploaded or downloaded.

## Recommended action

Ensure the app requests storage permissions before calling file transfer operations. If the user previously denied the permission, guide them to grant it manually from the device's app settings under **Settings > Apps > `APP_NAME` > Permissions**.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0006).
