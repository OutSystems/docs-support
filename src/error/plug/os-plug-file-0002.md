---
summary: OS-PLUG-FILE-0002 error occurs when the OutSystems File plugin is outdated in a mobile package. Regenerate the native build to fix it.
tags:
  - Android
  - iOS
  - Mobile app
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

The `CheckFilePlugin` client action detected a File plugin version older than 2.0.0 (ODC) / 4.0.0 (O11) instead of the current version. This typically happens when the app receives an over-the-air (OTA) update to its web layer, for example when you update the plugin in Service Studio or ODC Studio, without generating and distributing a new native build. The device keeps running the native build already installed on it, which still bundles the earlier plugin version.

<div class="info" markdown="1">

Before File plugin version 2.2.2 (ODC) / 4.1.3 (O11), a bug in `CheckFilePlugin` meant this scenario wasn't detected correctly. It incorrectly returned an `Error` with code [OS-PLUG-FILE-0003](os-plug-file-0003.md) instead of this warning. This was fixed in version 2.2.2 (ODC) / 4.1.3 (O11). If you're on an earlier version and see `OS-PLUG-FILE-0003` in this same OTA scenario, that's this bug, not the cause described on that page.

</div>

## Impact

New client actions introduced in the updated plugin (2.0.0 for ODC, 4.0.0 for O11) don't work in this app - the native plugin bundled in it doesn't implement them. The deprecated client actions (marked with `DEPRECATED_` in their name) keep working, since they still call the native plugin actions available in this older build.

## Workaround

If you can't immediately generate and distribute a new mobile package, or need the app to keep working on installs that haven't updated yet, keep using the `DEPRECATED_` client actions in the affected parts of your logic. They're guaranteed to keep working for as long as apps built with this older native plugin are in use. There are no plans to remove them, since doing so would break apps that can't be rebuilt with the new native plugin.

To detect this situation at runtime, call `CheckFilePlugin` and check `Warning.WarningCode` for `OS-PLUG-FILE-0002` before deciding whether to use the new or deprecated client actions.

For more on choosing between these paths, refer to the File Plugin migration guide ([ODC guide for version 2](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/use_mobile_plugins/outsystems_supported_mobile_plugins/file_plugin_version_2/file_plugin_migration_guide_from_version_1_to_version_2) / [O11 guide for version 4](https://success.outsystems.com/documentation/11/integration_with_external_systems/mobile_plugins/file_plugin_version_4/file_plugin_migration_guide_from_version_3_to_version_4/)).

## Recommended action

Generate a new mobile package that includes the updated version of the File plugin and distribute it to end users:

1. In OutSystems Service Studio or ODC Studio, publish the app with the updated plugin.
1. Generate a new mobile package (native build).
1. Distribute the new package through your app distribution channel (app store or enterprise distribution).

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0002).
