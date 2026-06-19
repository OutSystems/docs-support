---
summary: The file you are trying to open does not exist.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 506043ba-e5e6-4ec8-9a2a-4bffa976f873
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

# OS-PLUG-FLVW-0004

## Error message

"The file you are trying to open does not exist."

## Platform

iOS and Android

## Cause

The file path passed to the plugin points to a file that does not exist on the device's file system. The file may not have been downloaded yet, may have been deleted after download, or the path may be incorrect.

## Impact

The document cannot be opened.

## Recommended action

Verify that the file exists at the specified path before calling the plugin action. If the file should be downloaded first, ensure the download completed successfully before invoking the File Viewer action.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0004).
