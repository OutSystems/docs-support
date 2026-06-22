---
summary: Could not open the document.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 6ce56132-97ab-41ae-8b45-ae02588456fb
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

# OS-PLUG-FLVW-0008

## Error message

Could not open the document.

## Platform

iOS and Android

## Cause

A generic error occurred while attempting to open the document. Possible causes include a corrupted file, an unsupported file format, or an unexpected system error.

## Impact

The document cannot be opened.

## Recommended action

Implement a retrying mechanism to try to open the file a second time. Re-create or re-download the file again and attempt opening it with the File Viewer Plugin again.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0008).
