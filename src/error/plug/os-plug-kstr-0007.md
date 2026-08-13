---
summary: OS-PLUG-KSTR-0007 error on iOS occurs when the Keychain key is not found. Verify the store name and key were saved before calling get or remove.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 81e0e924-e09e-4af3-b588-bd66968a124f
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

# OS-PLUG-KSTR-0007

## Error message

The specified item could not be found in the Keychain.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecItemNotFound` status, indicating the requested key does not exist in the Keychain for the specified service (store). This occurs when calling `get` or `remove` for a key that was never stored, was previously deleted, or when the store name does not match the one used when the item was saved.

## Impact

The `get` or `remove` operation cannot retrieve data for the requested key.

## Recommended action

Verify that:

1. The key was previously saved using the `set` operation.
1. The store name (`service`) used in the operation matches the one used when the item was saved.
1. The item has not been previously removed.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0007).
