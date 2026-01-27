---
summary: There was an issue generating the app. A plugin is trying to access an XML file that was renamed in Cordova Android 14. The files strings.xml, colors.xml, and themes.xml are now named with a 'cdv_' prefix.
tags: cordova android, mobile app build and deployment, error handling, plugins, debugging, cordova android 14
guid: a4c8f5e2-9d3b-4f1e-8e7a-2b6c9d4f1e3a
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
outsystems-tools:
  - service center
coverage-type:
  - unblock
---

# OS-MABS-GEN-40023

## Error message

`There was an issue generating the app. Plugin '{plugin-name}' is trying to access '{filename}.xml', but this file was renamed in Cordova Android 14. The files strings.xml, colors.xml, and themes.xml are now named with a 'cdv_' prefix (cdv_strings.xml, cdv_colors.xml, cdv_themes.xml). Update your plugin to use the new file names.`

## Cause

Generating the app package failed because a custom plugin is trying to access one of the following XML files that were renamed in Cordova Android 14:

* `strings.xml` → `cdv_strings.xml`
* `colors.xml` → `cdv_colors.xml`
* `themes.xml` → `cdv_themes.xml`

The plugin is using the old file name, which no longer exists in Cordova Android 14 and later versions.

## Impact

The app package can't be generated.

## Recommended action

Update your plugin to use the new file names.

Learn more about [generating mobile apps and downloading build logs](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40023).
