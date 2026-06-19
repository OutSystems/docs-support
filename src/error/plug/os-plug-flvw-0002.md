---
summary: The app is running with an old version of the plugin. Please create a new mobile package.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 6115255f-b7fd-4cbe-aaff-8ede574ce52e
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

# OS-PLUG-FLVW-0002

## Error message

"The app is running with an old version of the plugin. Please create a new mobile package."

## Platform

iOS and Android

## Cause

The OutSystems mobile app package installed on the device was generated with an older version of the File Viewer plugin. The client action being called does not exist in the plugin version bundled in the installed app, causing a mismatch between the server-side definition and the mobile package.

## Impact

The File Viewer client action cannot execute. The file or media content will not be opened.

## Recommended action

Generate a new mobile package in Service Studio or ODC Studio and reinstall the app on the device. This ensures the latest version of the File Viewer plugin is bundled with the app.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0002).
