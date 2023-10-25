---
summary: There was an issue generating the app. At least one Cordova plugin uses Android Support Library components, which are not compatible with MABS 10 and onwards. Check your plugin configurations and try again.
tags:
guid: 7aa8edd7-5d70-4fec-92d7-1a524db83f1e
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-40006

## Error message

`There was an issue generating the app. At least one Cordova plugin uses Android Support Library components, which are not compatible with MABS 10 and onwards. Check your plugin configurations and try again.`

## Cause

Generating the Android application package failed because a custom plugin is using Android Support libraries. This is no longer possible in MABS 10 onwards. AndroidX must be used instead.

## Impact

The Android application package can't be generated.

## Recommended action

Update all plugins to their latest versions.

Find out which plugin(s) are using Android Support libraries. You can do this by looking for `com.android.support` instances in the plugin code. Migrate any Android Support libraries to the equivalent AndroidX packages. For more information about AndroidX migration, refer to [Migrating to AndroidX](https://developer.android.com/jetpack/androidx/migrate) and [Migrating to AndroidX: tips, tricks, and guidance](https://medium.com/androiddevelopers/migrating-to-androidx-tip-tricks-and-guidance-88d5de238876) by Android Developers.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40006).
