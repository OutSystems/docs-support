---
summary: OS-PLUG-KSTR-0016 Keystore plugin error occurs when the OutSystems platform runs in a web or PWA context where Cordova or Capacitor APIs are unavailable.
tags:
  - Android
  - Capacitor
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: c1bd7524-6e1b-4691-8422-5dcfbc845ad8
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

# OS-PLUG-KSTR-0016

## Error message

Cordova is not defined.

## Platform

Web

## Cause

The cause differs depending on the platform version.

### Cause on O11

The Keystore plugin relies on Cordova APIs to access the native device secure storage. When the app runs in a web browser or PWA instead of on a mobile device, the Cordova runtime is not available, causing this error.

### Cause on ODC

The Keystore plugin relies on Capacitor APIs to access the native device secure storage. Since the Keystore plugin only supports native mobile apps on ODC, running it in a web browser context causes this error.

## Impact

The Keystore plugin cannot be initialized and no data can be stored or retrieved through it.

## Recommended action

The Keystore plugin is only supported on mobile devices (iOS and Android). Use the `CheckKeyStorePlugin` action before calling any Keystore operations and handle the unavailability gracefully in your app logic when running in a web browser context.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0016).
