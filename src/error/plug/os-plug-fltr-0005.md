---
summary: OS-PLUG-FLTR-0005 in the OutSystems file transfer plugin occurs when the server URL is empty or invalid, blocking file transfer operations.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: e29cd59f-df59-4a57-b390-dc9724f751e0
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

# OS-PLUG-FLTR-0005

## Error message

URL to connect to is either null or empty

or

Invalid server URL was provided - `URL`

## Platform

iOS, Android, and PWA

## Cause

The server URL provided to the file transfer operation is either empty or has an invalid format. The plugin validates the URL before attempting the connection and returns this error when the value is missing or can't be parsed as a valid URL.

## Impact

The file transfer operation doesn't execute.

## Recommended action

Verify the server URL is a valid, non-empty Text value before calling the file transfer method. Ensure the URL starts with `http://` or `https://` and follows the correct format (for example, `https://example.com/upload`).

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0005).
