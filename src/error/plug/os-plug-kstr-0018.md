---
summary: 'OS-PLUG-KSTR-0018: Keystore plugin running in browser falls back to unencrypted local storage. Avoid storing sensitive data in web context.'
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Security
  - Troubleshooting
locale: en-us
guid: df0ff6f9-fa03-47ec-9000-5824e6775344
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

# OS-PLUG-KSTR-0018

## Error message

Not running on device. Will fallback to browser local storage but unencrypted.

## Platform

Web

## Cause

The Keystore plugin detected the app is running in a web browser instead of on a mobile device. Because native secure storage is not available in this context, the plugin falls back to the browser's local storage, which stores data without encryption.

## Impact

Data is stored in unencrypted browser local storage instead of the device's secure keystore. Sensitive information stored this way may be exposed.

## Recommended action

Avoid storing sensitive data when the app is running in a web browser context. Use the `CheckKeyStorePlugin` action to detect this scenario and handle it appropriately in your app logic, for example by warning the user or disabling features that depend on secure storage.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0018).
