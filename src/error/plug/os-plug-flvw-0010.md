---
summary: There is no app to open this document.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: 4da5bce3-ae49-475d-abee-56381d51dc71
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

# OS-PLUG-FLVW-0010

## Error message

"There is no app to open this document."

## Platform

Android

## Cause

There is no app installed on the Android device capable of handling the file type being opened. Android relies on other apps (via intents) to open documents, so if no compatible viewer app is installed, the document cannot be opened.

## Impact

The document cannot be opened.

## Recommended action

Install an app that supports the file type you're trying to open (for example, a PDF reader for `.pdf` files). Also verify that the file extension is correct, as an incorrect extension may prevent Android from finding a compatible app.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0010).
