---
summary: "OS-PLUG-FILE-0008 from the OutSystems File Plugin fires when the target file or directory path doesn't exist, blocking the filesystem operation."
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
locale: en-us
guid: 44f00121-0704-46d3-bd19-2287c93d4678
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

# OS-PLUG-FILE-0008

## Error message

`<method-name>` failed because file at `<path>` does not exist.

## Platform

iOS and Android

## Cause

The file or directory at the specified path does not exist. This error occurs when attempting an operation (such as reading, deleting, renaming, copying, or getting the URI) on a path that hasn't been created yet or has already been deleted.

## Impact

The requested filesystem operation won't be executed.

## Recommended action

Verify that the file or directory exists at the specified path before attempting the operation:

* There's currently no dedicated client action to check for existence. The `GetMetadata` action returns this same error when the file is missing. Ensure the resource was created by a previous step before operating on it.
* If the resource is expected to be created by a previous step, ensure that step completed successfully before proceeding.
* Handle the not-found case in your application logic to provide a meaningful experience to the user.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0008).
