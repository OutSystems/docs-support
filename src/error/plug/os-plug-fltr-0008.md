---
summary: "OS-PLUG-FLTR-0008 OutSystems platform error: file transfer plugin fails when the device cannot connect to the server due to network or URL issues."
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 5e5e9b93-a708-4a97-b3cd-aedd765e2f1f
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

# OS-PLUG-FLTR-0008

## Error message

Failed to connect to server.

## Platform

iOS, Android, and PWA

## Cause

The plugin could not establish a network connection to the remote server. Common causes include no internet connectivity on the device, the server being unreachable or offline, an incorrect server URL, DNS resolution failure, or a network timeout.

## Impact

The file transfer operation fails. No data is transferred.

## Recommended action

Check the device's network connectivity and verify the server URL is correct. Confirm the server is online and reachable. If using a private or internal server, ensure the device has access to that network.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0008).
