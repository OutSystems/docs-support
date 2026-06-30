---
summary: OS-PLUG-FILE-0012 occurs in OutSystems File plugin when DeleteDirectory is called with Recursive=False on a non-empty directory.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: f0c09064-2cfa-4646-9b2e-523bb4484a68
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

# OS-PLUG-FILE-0012

## Error message

Cannot delete directory with children; received recursive=false but directory has contents.

## Platform

iOS and Android

## Cause

An attempt was made to delete a directory that still contains files or subdirectories, but `Recursive=False` was passed to the `DeleteDirectory` operation. The plugin refuses to delete a non-empty directory without explicit confirmation via the recursive flag, in order to prevent accidental data loss.

## Impact

The directory deletion operation won't be executed. The directory and all its contents remain unchanged.

## Recommended action

Choose the approach that suits your use case:

* To delete the directory along with all its contents, call `DeleteDirectory` with `Recursive=True`.
* To delete only an empty directory, first delete all files and subdirectories within it individually before calling `DeleteDirectory`.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0012).
