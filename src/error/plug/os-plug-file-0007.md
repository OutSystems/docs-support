---
summary: OS-PLUG-FILE-0007 error on Android occurs when the user denies file access permission to the OutSystems Cordova File plugin.
tags:
  - Android
  - Cordova
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
locale: en-us
guid: 87b5efc4-043b-43ba-95f2-0fb48d785d76
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

# OS-PLUG-FILE-0007

## Error message

Unable to do file operation, user denied permission request.

## Platform

Android

## Cause

The user denied the file access permission required to perform the operation. On Android, certain filesystem operations on external storage or shared directories require explicit runtime permissions to be granted by the user.

This doesn't occur on recent Android versions that use scoped storage, where these storage permissions are no longer required.

## Impact

The requested filesystem operation won't be executed.

## Recommended action

Ensure your app requests the necessary file access permissions before performing filesystem operations. If the user denies the permission:

* Provide context explaining why the permission is needed before requesting it.
* Handle the denial gracefully and avoid retrying the operation without user interaction.
* Guide users to manually grant the required permissions through the device's app settings if they have permanently denied the request.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0007).
