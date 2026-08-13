---
summary: 'OS-PLUG-KSTR-0017: Key Store Plugin unavailable in OutSystems mobile apps — check plugin installation and use CheckKeyStorePlugin before Keystore operations.'
tags:
  - Android
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 511b9448-5cdb-4719-8d71-e860f5856a4d
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

# OS-PLUG-KSTR-0017

## Error message

Key Store Plugin is unavailable.

## Platform

iOS and Android

## Cause

The Keystore plugin is not available on the current device or the device does not meet the requirements to use it. This can happen if the plugin is not properly included in the mobile build, or if the device configuration prevents the plugin from initializing.

## Impact

Keystore operations (`get`, `set`, `remove`) cannot be performed.

## Recommended action

Use the `CheckKeyStorePlugin` action before calling any Keystore operations and handle the unavailability in your app logic. Ensure the plugin is properly installed and that the mobile build includes it.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0017).
