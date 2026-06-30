---
summary: OS-PLUG-FLTR-0007 in the OutSystems platform File Transfer plugin occurs when the upload source file is missing or unreachable on iOS and Android.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 9bb948ff-2890-4c5d-a739-e6a63ef905d9
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

# OS-PLUG-FLTR-0007

## Error message

Operation failed because file does not exist.

## Platform

iOS and Android

## Cause

The file specified in the upload operation doesn't exist at the provided path. This typically happens when the file path is incorrect, the file was deleted after the path was obtained, or the file was never created.

## Impact

The file transfer operation fails. The upload can't proceed without the source file.

## Recommended action

Verify the file exists at the specified path before initiating the upload. Check that the file path is correct and the file hasn't been moved or deleted.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0007).
