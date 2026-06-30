---
summary: OS-PLUG-FLTR-0011 is a catch-all OutSystems platform File Transfer plugin error caused by I/O failures, missing directories, or stream errors.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: e2aa1cf6-3b84-4a2e-8abf-71f20ef5bca0
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

# OS-PLUG-FLTR-0011

## Error message

The operation failed with an error.

## Platform

iOS, Android, and PWA

## Cause

An unexpected error occurred that isn't covered by a more specific error code. This is a catch-all error that can be triggered by I/O errors, failures to create the destination directory for downloaded files, errors during the transfer stream, or other internal library errors.

## Impact

The file transfer operation fails.

## Recommended action

Check the `exception` field in the error object for more details about the underlying error. Review device logs for additional context.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0011).
