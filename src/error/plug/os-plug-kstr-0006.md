---
summary: A Keychain item with the same key already exists in the iOS Keychain for the specified store.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 6cf211b3-2378-4394-b3b3-48d007b82206
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

# OS-PLUG-KSTR-0006

## Error message

The specified item already exists in the Keychain.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecDuplicateItem` status when attempting to add a new item. The plugin tries to update existing items when a key already exists, but if the initial lookup and the subsequent write are interrupted (for example, due to a race condition), the Keychain may report a duplicate entry.

## Impact

The data was not saved to the Keychain.

## Recommended action

Remove the existing item using the `remove` operation and then save the data again using the `set` operation.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0006).
