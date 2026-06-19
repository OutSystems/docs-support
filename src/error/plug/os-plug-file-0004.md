---
summary: OS-PLUG-FILE-0004 error occurs on iOS when a filesystem plugin method is called before the Cordova or Capacitor bridge initializes in OutSystems.
tags:
  - Capacitor
  - Cordova
  - iOS
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
locale: en-us
guid: a0d1b0ac-73d2-4f1c-94f9-f36ffa02f49a
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

# OS-PLUG-FILE-0004

## Error message

The error message differs depending on the platform version.

### Error message on O11

"Cordova bridge isn't initialized."

### Error message on ODC

"Cordova / Capacitor bridge isn't initialized."

## Platform

iOS

## Cause

The cause differs depending on the platform version.

### Cause on O11

The Cordova native bridge wasn't fully initialized when a filesystem plugin method was invoked. This typically happens if a plugin method is called too early in the app lifecycle, before the Cordova bridge has completed its setup.

### Cause on ODC

The Cordova or Capacitor native bridge wasn't fully initialized when a filesystem plugin method was invoked. This typically happens if a plugin method is called too early in the app lifecycle, before the bridge has completed its setup.

## Impact

The filesystem operation won't be executed.

## Recommended action

Ensure that filesystem plugin methods are only called after the native bridge has fully initialized.

### Recommended action on O11

Call plugin methods only after the screen or block is ready, for example in the **OnReady** event, and use the `CheckFilePlugin` client action to confirm the plugin is available before calling other actions. Avoid invoking plugin methods during the earliest stages of app startup.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0004).

### Recommended action on ODC

Call plugin methods only after the app is fully mounted and Cordova or Capacitor has been initialized. Avoid invoking plugin methods during the earliest stages of app startup.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0004).
