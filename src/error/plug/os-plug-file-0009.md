---
summary: OS-PLUG-FILE-0009 error on Android when a file plugin operation uses an unsupported method on a content:// URI or mismatched target type.
tags:
  - Android
  - Cordova
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: c360dc25-3b30-4089-aec7-75f70b0b5dcf
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

# OS-PLUG-FILE-0009

## Error message

"`<method-name>` not supported for `<target>`."

## Platform

Android

## Cause

The requested operation is not supported for the type of target provided. Common scenarios that trigger this error include:

* Attempting to perform a file operation on a `content://` URI (for example, a media file selected from the gallery). These URIs have limited operation support and generally only allow reading.
* Calling a file-specific operation (such as `ReadFile`) on a directory target, or calling a directory-specific operation (such as `ListDirectory`) on a file target.
* Attempting to copy from a local path to a `content://` URI, or between two `content://` URIs.

## Impact

The requested filesystem operation won't be executed.

## Recommended action

Ensure the operation is compatible with the target type:

* For `content://` URIs, use only read operations (for example, `ReadFile`). Avoid write, delete, rename, or copy operations targeting these URIs.
* When calling file operations, confirm the target is a file and not a directory, and vice versa. Use the `GetMetadata` client action to inspect the `PathType` beforehand.
* For copy operations, ensure that at least the destination uses a local (non-content scheme) path.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0009).
