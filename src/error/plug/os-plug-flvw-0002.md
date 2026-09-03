---
summary: OS-PLUG-FLVW-0002 File Viewer plugin error occurs when an OTA update mismatches the native build. Regenerate the mobile package to fix it.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
locale: en-us
guid: 6115255f-b7fd-4cbe-aaff-8ede574ce52e
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
  - apply
  - unblock
topic:
  - using-cordova-plugins
  - wrap-cordova-plugin
isautopublish: true
---

# OS-PLUG-FLVW-0002

## Error message

The app is running with an old version of the plugin. Please create a new mobile package.

## Platform

iOS and Android

## Cause

The `CheckFileViewerPlugin` client action detected a File Viewer plugin version older than 2.0.0 (ODC) / 3.0.0 (O11) instead of the current version. This typically happens when the app receives an over-the-air (OTA) update to its web layer, for example when you update the plugin in Service Studio or ODC Studio, without generating and distributing a new native build. The device keeps running the native build already installed on it, which still bundles the earlier plugin version.

To confirm which File Viewer plugin version your app depends on, check the plugin's version in the dependency manager in Service Studio or ODC Studio.

## Impact

From File Viewer plugin 2.1.3 (ODC) / 3.0.5 (O11) onwards, `CheckFileViewerPlugin` returns this warning, but `IsAvailable` is `True`, and all client actions, deprecated and non-deprecated, continue to work against the older native plugin.

In File Viewer plugin versions before 2.1.3 (ODC) / 3.0.5 (O11), the `IsAvailable` output of `CheckFileViewerPlugin` is `False`, and the new (non-deprecated) client actions don't work at all. Only the deprecated **CheckPlugin**, **OpenDocument**, and **PreviewMediaContent** actions keep working.

## Workaround

If you're on a File Viewer plugin version before 2.1.3 (ODC) / 3.0.5 (O11), or can't immediately generate and distribute a new mobile package, keep using the deprecated **CheckPlugin**, **OpenDocument**, and **PreviewMediaContent** client actions in the affected parts of your logic. They're guaranteed to keep working for as long as apps built with this older native plugin are in use. There are no plans to remove them, since doing so would break apps that can't be rebuilt with the new native plugin.

To detect this situation at runtime, call `CheckFileViewerPlugin` and check `Warning.WarningCode` for `OS-PLUG-FLVW-0002`.

## Recommended action

Generate a new mobile package that includes the updated version of the File Viewer plugin and distribute it to end users:

1. In OutSystems Service Studio or ODC Studio, publish the app with the updated plugin.
1. Generate a new mobile package (native build).
1. Distribute the new package through your app distribution channel (app store or enterprise distribution).

After installing the updated package, `CheckFileViewerPlugin` recognizes the new plugin and returns `IsAvailable` as `True` without any warning.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLVW-0002).
