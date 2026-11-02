---
summary: Resolve MABS Kotlin metadata version errors by identifying incompatible plugins and aligning Kotlin with your MABS version.
tags:
  - Android
  - Cordova
  - Libraries
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
guid: b11d34c6-48dc-4a74-bf7e-cb6a82a090b8
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - Developer
outsystems-tools:
  - service studio
  - odc studio
coverage-type:
  - unblock
topic:
  - kotlin-metadata-version-error
isautopublish: true
---

# OS-MABS-GEN-40024

## Error message

`Couldn't generate your app. A library used by your app was compiled with Kotlin metadata version <library_version>, but your app expects version <expected_version>. Check if your plugins are compatible with the Kotlin version used to build your app.`

## Cause

Generating the Android application package fails because a library was compiled with a Kotlin version that isn't compatible with the Kotlin version used to build the app. The library is usually a dependency of a plugin. The MABS version defines the Kotlin version used to build the app. The Kotlin metadata version matches the major and minor numbers of the Kotlin version. For example, metadata version `2.1.0` corresponds to Kotlin 2.1.

## Impact

The application package can't be generated.

## Recommended action

Search the build log for `incompatible version of Kotlin` to identify the affected library and the plugin that includes it. Then use one of the following options:

* Update or replace the plugin with a version compiled with a Kotlin version that your MABS version supports.

* In Cordova apps, set the `GradlePluginKotlinVersion` preference in the extensibility configurations of your app to a Kotlin version that the library supports. Set it for the Android platform only, because a global value has no effect. The preference changes the Kotlin version of the whole app. Check that your other plugins support it.

* Select a MABS version whose Kotlin version the library supports. For the Kotlin version supported by each MABS version, refer to [MABS versions](../../release-articles/mabs/mabs-versions.md).

For more information about downloading build logs, refer to [Generate and distribute your mobile app](https://www.outsystems.com/tk/redirect?g=1aacc771-f914-4f95-889a-31f1dde06a38) in OutSystems 11 or [Create mobile app package](https://www.outsystems.com/tk/redirect?g=4e816fa7-fffc-48c4-b205-13f7165d3775) in ODC.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40024).
