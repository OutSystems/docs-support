---
summary: OS-PLUG-FILE-0010 OutSystems File plugin error occurs when CreateDirectory targets an existing path. Check the path or delete the directory first.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 5f6a543c-74da-4920-ae24-d7d6e859c6bd
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

# OS-PLUG-FILE-0010

## Error message

"Directory at `<path>` already exists, cannot be overwritten."

## Platform

iOS and Android

## Cause

An attempt was made to create a directory at a path where a directory already exists. The `CreateDirectory` operation does not overwrite existing directories. This error also occurs in copy and rename operations when the destination path already points to an existing directory.

## Impact

The directory creation, copy, or rename operation won't be executed.

## Recommended action

Check whether a directory already exists at the target path before attempting to create it:

* If the directory already existing is an acceptable state for your use case, catch this specific error and treat it as a non-failure scenario.
* If you intend to replace the directory, delete it first using `DeleteDirectory` before recreating it.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0010).
