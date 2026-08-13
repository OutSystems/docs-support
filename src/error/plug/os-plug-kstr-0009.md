---
summary: The data stored in the iOS Keychain could not be decoded, possibly due to corruption.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: a4dfdd10-bb06-4cae-a456-40298f32a96c
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

# OS-PLUG-KSTR-0009

## Error message

Unable to decode the provided data.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecDecode` status, indicating the data retrieved from the Keychain cannot be decoded. This can happen when the stored data is corrupted, was stored with a different encoding, or the Keychain entry is in an inconsistent state.

## Impact

The stored data cannot be retrieved from the Keychain.

## Recommended action

Remove the affected item using the `remove` operation and save the data again using the `set` operation. If clearing individual items does not resolve the issue, try clearing the entire store using the `clear` operation.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0009).
