---
summary: The Keystore plugin passed one or more invalid parameters to the iOS Keychain API.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 2985cf1e-1959-4df2-911e-2368263887e4
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

# OS-PLUG-KSTR-0003

## Error message

One or more parameters passed to a function are not valid.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecParam` status, indicating that one or more parameters passed to the Keychain query are invalid. This can occur when the `service` (store name) or `key` values contain characters or formats not accepted by the Keychain API.

## Impact

The requested Keystore operation cannot be performed.

## Recommended action

Check the `service` (store name) and `key` values used in the plugin operation. Ensure they are non-empty Text values with valid characters. Avoid using special characters or excessively long strings.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0003).
