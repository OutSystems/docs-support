---
summary: URL to open is either null or empty.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 481c7cb4-5eb5-403e-a111-fc3dc8ea99b7
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

# OS-PLUG-FLVW-0007

## Error message

URL to open is either null or empty.

## Platform

iOS and Android

## Cause

The URL parameter passed to the plugin was provided as an empty Text.

## Impact

The document cannot be opened or downloaded.

## Recommended action

Ensure a valid, non-empty URL is passed to the plugin action. Check the logic that builds or retrieves the URL and confirm it is populated before invoking the File Viewer action.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0007).
