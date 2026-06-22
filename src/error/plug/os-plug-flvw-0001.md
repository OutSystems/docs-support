---
summary: Cordova / Capacitor isn't defined
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 508a2b0f-cd31-42bb-8685-a24a03c8a877
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

# OS-PLUG-FLVW-0001

## Error message

The error message differs depending on the platform version.

### Error message on O11

Cordova isn't defined.

### Error message on ODC

Cordova / Capacitor isn't defined.

## Platform

iOS and Android

## Cause

The cause differs depending on the platform version.

### Cause on O11

Cordova isn't available in the JavaScript runtime when the File Viewer client action is called. This can happen when the app is running in a browser or PWA context, where the Cordova bridge isn't present, or when the mobile shell hasn't finished loading the required bridges.

### Cause on ODC

Neither Cordova nor Capacitor are available in the JavaScript runtime when the File Viewer client action is called. Since the File Viewer Plugin only supports native mobile apps on ODC, this typically happens when the mobile shell hasn't finished loading the required bridges.

## Impact

The File Viewer client action cannot execute. The file or media content will not be opened.

## Recommended action

Make sure the app is running as a native mobile application on a real device or emulator, not in a browser preview. If the error occurs on a mobile device, regenerate the mobile package in Service Studio or ODC Studio and reinstall the app.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0001).
