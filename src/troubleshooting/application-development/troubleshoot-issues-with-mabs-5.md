---
summary: Check how you can fix some of the mobile app build issues after upgrading to MABS 5.0.
tags:
locale: en-us
guid: c17b230d-07c0-4dd2-b977-a794555d8ba2
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Troubleshooting issues with MABS 5.0

When you start building your apps with Mobile Apps Build Service (MABS) version 5.0 you might encounter some issues. This document is intended to help in the resolution of issues for this specific version.

In MABS 5.0 the target SDK of the generated Android apps was raised to Android P with API 28 while, for example, it was API 26 in MABS 4.0. In this sense, multiple components have been updated and it may cause some breaking changes.

To understand the issue, check the log file for troubleshooting information. Search for "What went wrong" and below it there may be helpful details. Or, look for information close to the end of the log file.

If you can't find the issue in this article, check [Troubleshooting Mobile Generation](troubleshoot-mobile-apps-generation.md).

Finally, if you still can't resolve the issue, contact OutSystems Support.

## New directory structure in the Cordova-android package

One of the updated components is the Cordova-android package (to version 8.0.0). This update changes the Android project structure and the application code is now placed in a new project called `:app`.

This changes the directory tree of the project. Many files that were located in the root of the Android project are now in the directory of the `:app` project. This includes source files, resources, assets, and more (including Resources imported via Service Studio).

Some plugins copy files or try to access files from these directories. Since the directory is now different in this new Cordova-android version, some plugins may not work properly with MABS 5.0.

Regarding the plugins supported by OutSystems, the only one that's affected by this is the OneSignal plugin. To prevent issues, please refer to the table in the section Supported Plugins Versions.

Some plugins can perform these directory-dependent tasks in the new Cordova-android version by assessing which version is used and adapting the directory based on it.

## New Android support libraries versions and OutSystems plugins

From the plugins supported by OutSystems, there are five affected by a change in the libraries versions, namely:

- Barcode Plugin
- Camera Plugin
- Local Notifications Plugin
- OneSignal Plugin
- PushWoosh Plugin

Older versions can work with MABS 5.0 but it's not guaranteed. On the other hand, plugins using Android support libraries version 28 aren't compatible with previous MABS versions. Check the table in the section Supported Plugins Versions to prevent gradle resolution issues.

With the update of the target SDK to 28, the Android support libraries have also been updated to version 28, both in the OutSystems applications core and in the supported plugins. This can cause Gradle resolution issues between some plugins. You can read more about this topic in [Android Support Library Versions for MABS](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Mobile_Apps_Build_Service/Android_Support_Library_Versions_for_MABS).

## Supported plugins versions

You should use the following versions for the supported OutSystems plugins:

| Plugin Name                | Version for MABS 4 | Version for MABS 5 |
| -------------------------- | :----------------: | :----------------: |
| Barcode Plugin             | 3.x.x              | 4.x.x              |
| Camera Plugin              | 4.x.x              | 5.x.x              |
| Local Notifications Plugin | 5.x.x              | 6.x.x              |
| OneSignal Plugin           | 2.x.x              | 3.x.x              |
| PushWoosh Plugin           | 3.x.x              | 4.x.x              |


## Frequent errors

In this section you can find descriptions of some common errors and how to fix them.

### File wasn't found

#### Symptoms

When requesting a build, you're getting an error similar to:

 - Error generating application. This happened because script 'platforms/android/app/cordova-android-support-gradle-release/properties.gradle' wasn't found. Please check your script path and try again.
 - Error installing Cordova plugin: cordova-plugin-firebase': Error: ENOENT: no such file or directory, scandir 'platforms/android/assets/www/google-services.

#### Cause

This error occurs when building an app with a plugin that tries to access a file that can't be found. This can be caused by multiple reasons:

- A plugin isn't compatible with the MABS version that's used due to the Cordova-android version
- A plugin isn't configured correctly
- There is an error in the plugin code

If you are using the OneSignal Plugin and the file that wasn't found is `platforms/android/app/cordova-android-support-gradle-release/properties.gradle` then it's highly likely that you aren't using the correct OneSignal Plugin version.

#### Resolution

If you are using the OneSignal Plugin:

- Refer to the table in the section Supported Plugins Versions

If the previous step doesn't fix it:

- Check your plugins documentation to make sure they're correctly configured
- Try to upgrade your plugins to more recent versions that may support newer Cordova-android versions

If the issue remains:

- Modify the plugin(s) to account for the Cordova-android directory changes (refer to the directory changes explained in this section)

### Minimum Android SDK incompatibility

#### Symptoms

When requesting a build, you're getting an error similar to:

- Error generating application. Library :some-lib: requires minimum Android SDK 21, which is higher than the 16 that's required by the application. Check if this value is being overridden in your Extensibility Configurations.

#### Cause

This error occurs when building an app that uses a library that requires a minimum SDK that's higher than the one required by the application. This app fails to build because the library may try to use classes, methods, resources, etc. that aren't available in the minimum SDK of the application.

This can be caused by overriding this value in the Extensibility Configurations of your application.

The log file should contain something similar to this, when the application has a minimum SDK of 16 but uses a library some-lib that has a minimum SDK of 21:

```
* What went wrong:
> Manifest merger failed : uses-sdk:minSdkVersion 16 cannot be smaller than version 21 declared in library [:some-lib:] .gradle/caches/transforms-1/files-1.1/some-debug.aar/0123456790abcdef0123456789abcdef/AndroidManifest.xml as the library might be using APIs not available in 16
   Suggestion: use a compatible library with a minSdk of at most 16,
   or increase this project's minSdk version to at least 21,
   or use tools:overrideLibrary="com.some.api.some" to force usage (may lead to runtime failures)
```


#### Resolution

You can try to:

- Check if the minimum SDK value is defined in your Extensibility Configurations

If the issue remains:

- Try using a different version of the plugin that uses the problematic library
