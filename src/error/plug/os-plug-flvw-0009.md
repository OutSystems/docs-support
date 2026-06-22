---
summary: Invalid parameters.
tags: error handling,troubleshooting,system messages,user experience,application deployment
locale: en-us
guid: c01f84cb-556b-4c62-90f7-b146682231e1
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

# OS-PLUG-FLVW-0009

## Error message

Invalid parameters.

## Platform

iOS and Android

## Cause

The parameters passed to the plugin are invalid. This error can occur in two situations:

* On Android, when a file path is provided but is not a valid path.
* When using the `OpenDocumentFromResources` or `PreviewMediaContentFromResources` client actions, the path must start with `resources/`. Providing a path that does not follow this convention causes this error.

## Impact

The document or media content cannot be opened.

## Recommended action

When using resource-based actions, make sure the path starts with `resources/` (for example, `resources/myfile.pdf`). For other actions, verify that all parameters are valid and correctly formatted before invoking the File Viewer action.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0009).
