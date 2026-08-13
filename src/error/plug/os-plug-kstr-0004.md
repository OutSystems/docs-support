---
summary: The iOS system failed to allocate enough memory to perform the Keystore operation.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 4e6170c4-8f6d-42cf-89b3-86cef5c3fb9d
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

# OS-PLUG-KSTR-0004

## Error message

Failed to allocate memory.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecAllocate` status, indicating that the system was unable to allocate the memory needed to complete the Keychain operation. This is typically caused by insufficient available memory on the device.

## Impact

The requested Keystore operation cannot be performed.

## Recommended action

Free device memory by closing background applications and try again. If the issue persists after freeing memory, restart the device.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0004).
