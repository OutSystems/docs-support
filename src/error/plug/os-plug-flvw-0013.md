---
summary: The file has no extension.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 2816fe8e-7366-4e7a-9682-45c5d837d8ed
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

# OS-PLUG-FLVW-0013

## Error message

The file has no extension.

## Platform

iOS

## Cause

The file being opened has no file extension. iOS requires a file extension to determine which app should handle the file. Without an extension, the system cannot identify the file type.

## Impact

The document cannot be opened on iOS.

## Recommended action

Ensure the file has a proper extension (for example, `.pdf`, `.docx`, `.jpg`). If downloading the file from a URL, verify the filename in the URL or the server response includes the correct file extension.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0013).
