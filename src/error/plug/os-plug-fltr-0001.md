---
summary: OS-PLUG-FLTR-0001 error in OutSystems platform occurs when the Cordova or Capacitor bridge isn't loaded before the File Transfer plugin action runs.
tags:
  - Android
  - Capacitor
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 7b5c027d-f9ee-4562-b04a-4f30006e7566
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

# OS-PLUG-FLTR-0001

## Error message

The error message differs depending on the platform version.

### Error message on O11

Cordova isn't defined.

### Error message on ODC

Cordova / Capacitor isn't defined.

## Platform

iOS, Android, and PWA

## Cause

The runtime bridge required by the File Transfer client action isn't available when the action is called. On O11 this bridge is Cordova; on ODC it can be either Capacitor or Cordova.

This typically happens when the action runs before the mobile shell has finished loading the required bridges, or when the app runs in a context where the bridge isn't present (for example, a browser preview).

## Impact

File transfer operations can't be performed. The `IsAvailable` output of `CheckFileTransferPlugin` is `False`.

## Recommended action

Verify the plugin is correctly installed and the app is running in a supported environment. If the app targets native mobile, ensure a mobile package has been generated that includes the plugin.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0001).
