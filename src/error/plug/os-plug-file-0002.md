---
summary: OS-PLUG-FILE-0002 error occurs when the OutSystems File plugin is outdated in a mobile package. Regenerate the native build to fix it.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
locale: en-us
guid: 9928cd76-530f-4368-8bc7-2825a9e5a9a3
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

# OS-PLUG-FILE-0002

## Error message

The app is running with an old version of the plugin. Please create a new mobile package.

## Platform

iOS and Android

## Cause

The app is running a mobile package that was built with an older version of the File plugin. The plugin asset was updated on the OutSystems side, but a new mobile package hasn't been generated and distributed yet.

## Impact

The app continues to run using the deprecated plugin client actions. New plugin features and fixes introduced in the updated version won't be available until a new mobile package is generated and installed.

## Recommended action

Generate a new mobile package that includes the updated version of the File plugin and distribute it to end users:

1. In OutSystems Service Studio or ODC Studio, publish the app with the updated plugin.
1. Generate a new mobile package (native build).
1. Distribute the new package through your app distribution channel (app store or enterprise distribution).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0002).
