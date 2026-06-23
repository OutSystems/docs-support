---
summary: "OS-MABS-PRJ-50005 in OutSystems Developer Cloud (ODC) occurs when a Cordova plugin dependency can't be resolved during the build."
tags:
  - Cordova
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
guid: ab4f1470-f0ce-4e1d-836d-86af3377df86
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
audience:
  - Developer
outsystems-tools:
  - odc portal
coverage-type:
  - unblock
isautopublish: true
---

# OS-MABS-PRJ-50005

## Error message

`An error occurred while resolving Cordova plugin dependencies. If the problem persists, open a support case.`

## Cause

This is an internal error. A Cordova plugin declared for the build wasn't found among the installed dependencies, or the dependency manifest is missing or unreadable.

## Impact

The app package can't be generated.

## Recommended action

Regenerate the app package. This might be a temporary issue that resolves on its own.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PRJ-50005).
