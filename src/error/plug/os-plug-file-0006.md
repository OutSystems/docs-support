---
summary: "OS-PLUG-FILE-0006 File plugin error on iOS and Android caused by an invalid path: how to resolve it using GetFileUri."
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 9fbcdc50-e56e-440d-8321-12f4f4adbcb5
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

# OS-PLUG-FILE-0006

## Error message

"Invalid `<path>` path."

## Platform

iOS and Android

## Cause

The path provided for the operation is invalid or cannot be resolved to a valid filesystem location. This can occur when the path is malformed, when a URI (such as a `content://` URI on Android) cannot be resolved to an actual file, or when the path references a location that is inaccessible.

## Impact

The requested filesystem operation won't be executed.

## Recommended action

Verify that the path you are providing is well-formed and points to an accessible location:

* Don't build paths manually. Use the plugin's directory location values and the `GetFileUri` client action to obtain valid paths.
* When you pass a URI obtained from another source, such as an image picker, make sure it still points to an existing file.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0006).
