---
summary: Path of the file to open is either null or empty.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: d0fcaf60-5ffc-4363-8bcf-b0620d6f737b
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

# OS-PLUG-FLVW-0006

## Error message

Path of the file to open is either null or empty.

## Platform

iOS and Android

## Cause

The file path parameter passed to the plugin was provided as an empty Text.

## Impact

The document cannot be opened.

## Recommended action

Ensure a valid, non-empty file path is passed to the plugin action. Check the logic that builds or retrieves the file path and confirm it is populated before invoking the File Viewer action.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0006).
