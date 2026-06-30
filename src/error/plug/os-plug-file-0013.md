---
summary: OS-PLUG-FILE-0013 means the OutSystems File Plugin native filesystem operation failed on iOS or Android, often due to storage or OS restrictions.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
locale: en-us
guid: b14f727f-5258-49c7-85b2-63118af5c7b3
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

# OS-PLUG-FILE-0013

## Error message

`METHOD_NAME` failed with: `ERROR_DETAILS`.

## Platform

iOS and Android

## Cause

An unexpected error occurred during the execution of the filesystem operation. This is a catch-all error that surfaces when the underlying native operation fails for a reason not covered by the more specific error codes (OS-PLUG-FILE-0005 through OS-PLUG-FILE-0012). The error message will include native error details that can help diagnose the root cause.

Common underlying causes include:

* Insufficient available storage on the device.
* Operating system restrictions preventing the operation.
* Unexpected filesystem state (for example, a partially written file or a corrupted directory).

## Impact

The requested filesystem operation won't be executed.

## Recommended action

Check the `ERROR_DETAILS` portion of the error message for more information about the specific failure. Based on those details:

* If storage is the issue, guide the user to free up space on the device.
* If the issue appears to be a transient OS or permission problem, retry the operation.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0013).
