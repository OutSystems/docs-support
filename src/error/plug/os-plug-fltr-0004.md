---
summary: OS-PLUG-FLTR-0004 error occurs in the OutSystems File Transfer plugin when the file path parameter is empty; check that it's a non-empty text value.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 6e483119-6234-4c1b-af05-eac1a8689938
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

# OS-PLUG-FLTR-0004

## Error message

The method's input parameters aren't valid.

## Platform

iOS and Android

## Cause

The file path provided to the file transfer operation is empty. The native library validates all input parameters before executing the transfer and throws this error when a required path value is missing or blank.

## Impact

The file transfer operation doesn't execute.

## Recommended action

Check that the file path parameter passed to the plugin method is a non-empty Text value. Ensure all required parameters are properly set before calling the file transfer method.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0004).
