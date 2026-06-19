---
summary: The URL you are trying to open is malformed.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: db0409e4-e963-41aa-8805-2d5953880e60
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

# OS-PLUG-FLVW-0005

## Error message

"The URL you are trying to open is malformed - `<url>`."

## Platform

iOS and Android

## Cause

The URL provided to open or download the document is not a valid URL. This can be caused by typos, a missing protocol (such as `https://`), incorrect encoding, or passing a local file path instead of a URL.

## Impact

The document cannot be opened or downloaded from the given URL.

## Recommended action

Verify the URL is properly formatted (for example, `https://example.com/document.pdf`). Check for typos, missing protocol, or encoding issues in the URL value being passed to the plugin action.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0005).
