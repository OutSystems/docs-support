---
summary: The requested key does not exist in the Android encrypted storage for the specified store.
tags:
  - Android
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 7ba10287-0b8f-4763-86ba-fe8ee8b9da4f
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

# OS-PLUG-KSTR-0012

## Error message

Key does not exist.

## Platform

Android

## Cause

The requested key does not exist in the Android encrypted storage (`EncryptedSharedPreferences`) for the specified store. This occurs when calling `get` or `remove` for a key that was never stored, was previously removed, or when the store name does not match the one used when saving the item.

## Impact

The `get` or `remove` operation cannot retrieve data for the requested key.

## Recommended action

Verify that:

1. The key was previously saved using the `set` operation.
1. The store name used in the operation matches the one used when the item was saved.
1. The item has not been previously removed.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0012).
