---
summary: Cordova bridge isn't initialized.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: c2b12d6a-503d-4d94-a4e4-1538e9d20f89
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

# OS-PLUG-FLVW-0011

## Error message

Cordova bridge isn't initialized.

## Platform

iOS

## Cause

The Cordova bridge had not been fully initialized when the plugin method was invoked. This can happen if a File Viewer action is called very early during app startup, before the device-ready event has fired and the bridge is ready.

## Impact

The plugin cannot communicate with the native iOS layer and the file cannot be opened.

## Recommended action

Ensure File Viewer client actions are only called after the app is fully initialized. Under normal usage of the OutSystems client actions, this error should not occur. If you encounter it, check whether there is custom logic calling the plugin at startup before initialization completes.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0011).
