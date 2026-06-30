---
summary: OS-PLUG-FILE-0011 in the OutSystems File plugin means a parent directory is missing; pass Recursive=True to CreateDirectory to fix it.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 517b14ed-1125-4ca5-916e-82525f8f9708
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

# OS-PLUG-FILE-0011

## Error message

Missing parent directory – possibly recursive=false was passed or parent directory creation failed.

## Platform

iOS and Android

## Cause

The operation could not complete because one or more intermediate (parent) directories in the target path do not exist. Common scenarios that trigger this error include:

* Calling `CreateDirectory` with `Recursive=False` on a path whose parent directories don't exist yet.
* Calling a copy or rename operation where the destination's parent directory does not exist.
* An internal parent directory creation step failed during a recursive `CreateDirectory` call.

## Impact

The filesystem operation won't be executed.

## Recommended action

Ensure all parent directories in the target path exist before performing the operation:

* When creating directories with nested paths, pass `Recursive=True` to `CreateDirectory` so that all intermediate directories are created automatically.
* For copy and rename operations, create the destination's parent directory first if it doesn't already exist.
* If the error occurs during a `Recursive=True` call, verify that the path is well-formed and that you have write access to the parent locations.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0011).
