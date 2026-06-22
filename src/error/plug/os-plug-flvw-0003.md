---
summary: File Viewer Plugin is not loaded.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 337a269c-d6ae-4b23-8f7e-9c8281f08462
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

# OS-PLUG-FLVW-0003

## Error message

File Viewer Plugin is not loaded.

## Platform

iOS and Android

## Cause

The File Viewer plugin was not available when the client action was called. This can happen if the plugin was not correctly included in the mobile app package, or if it failed to initialize during app startup.

## Impact

The File Viewer client action cannot execute. The file or media content will not be opened.

## Recommended action

Verify that the File Viewer plugin is correctly added to your OutSystems app. If the error persists, regenerate the mobile package in Service Studio or ODC Studio and reinstall the app on the device.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0003).
