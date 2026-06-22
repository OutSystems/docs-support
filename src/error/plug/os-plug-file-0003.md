---
summary: The File plugin is not defined. Make sure the mobile package is valid.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: dea144e5-b34a-4cb1-8dcb-beab6ac5f3e0
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

# OS-PLUG-FILE-0003

## Error message

The File plugin is not defined. Make sure the mobile package is valid.

## Platform

iOS and Android

## Cause

The File plugin isn't available at runtime in the current mobile package. The `CheckFilePlugin` client action runs before every filesystem operation and detected that neither the new plugin bridge nor the legacy bridge is present. This indicates the mobile package doesn't include the plugin, or was built incorrectly.

Common causes include:

* The mobile package was generated without the File plugin dependency.
* The plugin was removed from the app's dependencies before the package was built.
* The mobile package build process completed with errors that silently excluded the plugin.

## Impact

All filesystem operations will fail. No file reads, writes, or directory operations can be performed.

## Recommended action

Verify the File plugin is correctly included in the app and regenerate the mobile package:

1. Confirm the File plugin is listed as a dependency in your OutSystems app.
1. Publish the app and generate a new mobile package.
1. Verify the build completed successfully without errors.
1. Distribute and install the new package.

If the issue persists after regenerating the package, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0003) and include the build logs for further investigation.
