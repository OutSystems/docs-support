---
summary: OS-PLUG-FLTR-0002 error in OutSystems mobile apps occurs when the File Transfer Plugin was updated but the mobile package wasn't regenerated.
tags:
  - Android
  - Cordova
  - Deploy
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 93b8f06a-8358-4e6c-bb3c-2908e83b742e
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

# OS-PLUG-FLTR-0002

## Error message

The app is running with an old version of the plugin. Please create a new mobile package.

## Platform

iOS and Android

## Cause

The `CheckFileTransferPlugin` client action found the legacy plugin clobber (old version) but not the new unified File Transfer Plugin. This happens when the plugin was updated in Service Studio or ODC Studio, but the app's mobile package wasn't regenerated. The device is running an old build that still has the previous plugin version.

## Impact

File transfer operations won't work with the new client actions. The `IsAvailable` output of `CheckFileTransferPlugin` is `False`. This is returned as a warning, so the app won't crash, but the plugin functionality is unavailable until the app is updated.

## Recommended action

Generate a new mobile package and distribute it to your users. After installing the updated package, `CheckFileTransferPlugin` will recognize the new plugin and return `IsAvailable` as `True`.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0002).
