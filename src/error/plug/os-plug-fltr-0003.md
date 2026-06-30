---
summary: The File Transfer plugin is not loaded. Make sure the mobile package is valid.
tags:
  - Android
  - Capacitor
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 74fe90a6-f649-48ed-97d6-55e347eaa101
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

# OS-PLUG-FLTR-0003

## Error message

The File Transfer plugin is not loaded. Make sure the mobile package is valid.

## Platform

iOS and Android

## Cause

The cause differs depending on the platform version.

### Cause on O11

The `CheckFileTransferPlugin` client action detected a Cordova environment, but couldn't find any version of the File Transfer Plugin. Neither the new unified plugin nor the legacy one was present, meaning the plugin is missing from the native build entirely.

### Cause on ODC

The `CheckFileTransferPlugin` client action detected a Capacitor / Cordova environment, but couldn't find any version of the File Transfer Plugin. This means the plugin is missing from the native build entirely.

## Impact

File transfer operations can't be performed. The `IsAvailable` output of `CheckFileTransferPlugin` is `False`.

## Recommended action

Add the File Transfer Plugin to your app in Service Studio or ODC Studio, then generate and distribute a new mobile package.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0003).
