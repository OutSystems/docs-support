---
summary: OS-PLUG-FILE-0001 occurs when the Cordova or Capacitor bridge is unavailable for the OutSystems File plugin in a non-native or PWA context.
tags:
  - Android
  - Capacitor
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: d89cb737-8a22-4a5e-a163-6f758789d434
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
helpids:
---

# OS-PLUG-FILE-0001

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

The Cordova framework isn't available at runtime when a filesystem plugin method is called. This error is detected by the `CheckFilePlugin` client action, which verifies the native bridge availability before any filesystem operation is executed. It typically occurs when the app is running in a browser or PWA context where the Cordova bridge isn't present.

### Cause on ODC

Neither Cordova nor Capacitor is available at runtime when a filesystem plugin method is called. This error is detected by the `CheckFilePlugin` client action, which verifies the native bridge availability before any filesystem operation is executed. It typically occurs when the mobile shell hasn't finished loading the required bridges.

## Impact

The filesystem operation won't be executed and the plugin reports that it's unavailable.

## Recommended action

Ensure the app is running as a native mobile application with a valid mobile package that includes the File plugin:

* Confirm the mobile package was generated and distributed correctly.
* Do not call filesystem plugin methods in web-only or PWA contexts where the native bridge is unavailable.
* If the error occurs in a native app, regenerate the mobile package and verify that the plugin is included in the build.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0001).
