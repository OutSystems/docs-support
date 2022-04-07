---
summary: Check how you can fix some of the mobile app build errors after upgrading from MABS 4 to MABS 5.
locale: en-us
guid: 882d32b2-39e0-4d08-9d40-e30f80cd467f
---


# MABS Upgrade Troubleshooting Guide - Android

When you start building your apps with a different version of Mobile Apps Build Service (MABS), you may encounter some errors. This document can help you troubleshoot those errors after upgrading from MABS 4 to MABS 5.

MABS 5 raises the target SDK of the generated Android apps to the Android P target, which is API 28, while MABS 4 uses API 26. To achieve this, multiple components have been updated, which in return causes some breaking changes.

If you can't find here the error you're getting, or the error explanation is not helpful, check the log file for more troubleshooting information. Search for parts that start with "What went wrong". This is usually the place with helpful details. Or, look for information near the end of the log file. If you still cannot resolve the issue and you're getting stuck with the error, contact OutSystems Support.

## Cordova-android

One of the updated components is the Cordova-android package, from version 6.4.0 to 8.0.0. This update changes the Android project structure. When using version 6.4.0 the application code is placed in the root project. In the newer version it is placed in a new project named `:app`.

This changes the directory tree of the project. Many files that were located in the root of the Android project are moved to the directory of the `:app` project. This includes source files, resources, assets and more.

Some plugins copy files or try to access files from these directories. The directories are different between these Cordova-android versions and some plugins may only work in some Cordova-android versions. This means they may only work in either MABS 4 or MABS 5.

Regarding OutSystems supported plugins, the only plugin that is affected by this is OneSignal Plugin. To prevent the errors, please refer to the table in the section Supported Plugins Versions.

Some plugins can perform these directory-dependent tasks in both Cordova-android versions by assessing which version is used and adapting the directory based on it.

## Android Support Libraries

There are five supported plugins that are affected by change in the libraries:

* Barcode Plugin
* Camera Plugin
* Local Notifications Plugin
* OneSignal Plugin
* PushWoosh Plugin

Plugins that use Android support libraries version 28 are not compatible with MABS 4. Older versions can work with MABS 5 but it is not guaranteed. Check the table in the section Supported Plugins Versions to prevent gradle resolution issues.

To accompany the update of the target SDK to 28 the Android support libraries have also been updated to version 28, both in the OutSystems applications core and in the supported plugins. This can cause gradle resolution issues between some plugins. You can read more about this topic in in [Android Support Library Versions for MABS](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Mobile_Apps_Build_Service/Android_Support_Library_Versions_for_MABS).

## Supported Plugins Versions

You should use the following versions for the supported OutSystems plugins:

| Plugin Name                | Version for MABS 4 | Version for MABS 5 |
|----------------------------|--------------------|--------------------|
| Barcode Plugin             | 3.x.x              | 4.x.x              |
| Camera Plugin              | 4.x.x              | 5.x.x              |
| Local Notifications Plugin | 5.x.x              | 6.x.x              |
| OneSignal Plugin           | 2.x.x              | 3.x.x              |
| PushWoosh Plugin           | 3.x.x              | 4.x.x              |

## Frequent errors

In this section you can find descriptions of some common errors and how to fix them.

### File was not found

#### Symptoms

When requesting a build, you're getting an error similar to:

* Error generating application. This happened because script 'platforms/android/app/cordova-android-support-gradle-release/properties.gradle' was not found. Please check your script path and try again.

* Error installing Cordova plugin: cordova-plugin-firebase': Error: ENOENT: no such file or directory, scandir 'platforms/android/assets/www/google-services.

#### Cause

This error occurs when building an app with a plugin that tries to access a file that cannot be found. This can be caused by multiple reasons:

* A plugin is not compatible with the MABS version that is being used due to the Cordova-android version

* A plugin has not been configured correctly

* There is an error in the plugin code

If you are using the OneSignal Plugin and the file that was not found is `platforms/android/app/cordova-android-support-gradle-release/properties.gradle` then it is highly likely that you are not using the correct OneSignal Plugin version.

#### Resolution

If you are using the OneSignal Plugin:

* Refer to the table in the section Supported Plugins Versions

If the previous step does not fix it:

* Check your plugins documentation to make sure they are correctly configured

* Try to upgrade your plugins to more recent versions that may support newer Cordova-android versions

If the issue remains:

* Modify the plugin(s) to account for the Cordova-android directory changes (refer to the directory changes explained in this section)

### Plugin not compatible with an older MABS version

#### Symptoms

When requesting a build with MABS 4 or older, you're getting an error similar to:

* Error generating application. At least one Cordova plugin used in the build is only compatible with MABS 5 or higher (Android support library 28). Either downgrade the plugin or build the application using MABS 5 or higher.

* Error compiling Cordova plugin: intermediates/incremental/mergeDebugResources/merged.dir/values/values.xml:87: error: resource android:attr/fontVariationSettings not found.

#### Cause

This error occurs when building an app with MABS 4 or prior that is using at least one plugin that references an Android support library version 28.

The log file should contain something similar to this error, where support libraries try to use resources that cannot be found because they only exist in Android target SDK 28 or newer:
```
platforms/android/build/intermediates/incremental/mergeDebugResources/merged.dir/values/values.xml:90: error: resource android:attr/fontVariationSettings not found.
platforms/android/build/intermediates/incremental/mergeDebugResources/merged.dir/values/values.xml:90: error: resource android:attr/ttcIndex not found.
```
#### Resolution

There are two things you can try:

* Use a newer MABS version

* Change the versions of the supported plugins (refer to the table in the section Supported Plugins Versions)

If the issue remains:

* Modify the plugin(s) to lower the support library versions (this may cause build or runtime issues)

### AndroidX support library usage

#### Symptoms

When requesting a build, you're getting the following error:

* Error generating application. At least one Cordova plugin used in the build requires an AndroidX library, which is not currently compatible with MABS. Check your plugins configuration.

#### Cause

This error occurs when building an app with a plugin that uses an AndroidX support library or a dependency that uses one. AndroidX is currently not compatible with MABS. There is a conflict caused by using AndroidX support libraries together with older Android support libraries. A common example of the dependency issue is Google Mobile Services (GMS) dependencies.

The log file should contain something similar to:
```
* What went wrong:
Execution failed for task ':app:processReleaseManifest'.
> Manifest merger failed : Attribute application@appComponentFactory value=(android.support.v4.app.CoreComponentFactory) from [com.android.support:support-compat:28.0.0] AndroidManifest.xml:22:18-91
    is also present at [androidx.core:core:1.0.0] AndroidManifest.xml:22:18-86 value=(androidx.core.app.CoreComponentFactory).
    Suggestion: add 'tools:replace="android:appComponentFactory"' to <application> element at AndroidManifest.xml:5:5-20:19 to override.
```
#### Resolution

Check your plugins code and look for gradle dependencies that may use AndroidX. Dependencies related to Google that don't have their versions locked (so the latest version is always used) are the most likely culprits.

An example:

* `implementation "com.google.android.gms:play-services-maps:+"`

After you find the plugin(s) with the problematic dependencies you can:

* Try to upgrade/downgrade the plugin(s) to another version that may lock these dependencies

If the issue remains:

* Modify the plugin(s) to lock the problematic dependency versions

### Incorrect Google Services usage

#### Symptoms

When requesting a build, you're getting the following error:

* Error generating application. Some plugins are using Google Services but their usage is not being correctly configured. Check your plugins documentation to ensure their setup is correct.

#### Cause

This error occurs when building an app that uses Google Services but the app's configuration is not correct. These apps require specific JSON (for Android) or Plist (for iOS) configuration files located in the correct directories. For most of the plugins that use Google Services you need to have the correctly configured files as a resource in Service Studio.

Regarding the supported plugins, PushWoosh requires you to provide a ZIP file with the configuration JSON file for Android. Check the plugin documentation for more information.

The log file should contain something similar to this, where the google-services.json file was not found in the correct directory:
```
Execution failed for task ':app:processDebugGoogleServices'.
> File google-services.json is missing. The Google Services Plugin cannot function without it.
```
Or, when the google-services.json file was found in the correct directory but is not correctly filled (package name in the JSON file does not match the package name of the application):

```
Execution failed for task ':app:processDebugGoogleServices'.
> No matching client found for package name 'com.some.some'
```
#### Resolution

There are two things you can try:

* Check your plugins documentation to make sure they are being correctly configured

* Make sure the JSON and/or Plist files are correctly filled

If this doesn't solve it:

* Try using different versions of the problematic plugin

If the issue remains:

* Modify the plugin(s) to account for the Cordova-android directory changes (refer to the directory changes explained in this section)

### Android support libraries incompatibility

#### Symptoms

When requesting a build, you're getting an error similar to:

* Error generating application. Conflicting versions of Android support libraries are being used (25.4.0 and 26.1.0). Check your plugins configuration.

#### Cause

This error occurs when building an app that uses multiple Android support library dependencies that target different versions. Such dependencies can cause errors.

The log file should contain something similar to this example, a condition when there is a conflict caused by multiple support libraries defining the android.support.VERSION meta-data tag with different values:

```
* What went wrong:
> Manifest merger failed : Attribute meta-data#android.support.VERSION@value value=(25.4.0) from [com.android.support:exifinterface:25.4.0] AndroidManifest.xml:25:13-35
    is also present at [com.android.support:support-v4:26.1.0] AndroidManifest.xml:28:13-35 value=(26.1.0).
    Suggestion: add 'tools:replace="android:value"' to <meta-data> element at AndroidManifest.xml:23:9-25:38 to override.
```

#### Resolution

There are two things you can try:

* Try to upgrade/downgrade plugins that can be causing this issue

* Use a newer version of MABS

If the issue remains:

* Modify the plugin(s) to change the problematic dependency versions

### Meta-data tag defined more than once

#### Symptoms

When requesting a build, you're getting an error similar to:

* Error generating application. Meta-data SOME_APP_KEY is being defined more than once. Check your plugins documentation to ensure their setup is correct.

#### Cause

This error occurs when building an app that defines the same meta-data tag more than once with different values. It is typically caused by the usage of some plugins that modify or create a new AndroidManifest.xml file that redefines or overrides the meta-data value.

The log file should contain something similar to this log example, that shows a conflict caused by a plugin overriding the SOME_APP_KEY meta-data value that was already defined by its own library as a string resource:

```
* What went wrong:
> Manifest merger failed : Attribute meta-data#SOME_APP_KEY@value value=(1234567890) from AndroidManifest.xml:18:54-130
    is also present at [com.some.some:library:1.2.3] AndroidManifest.xml:22:13-47 value=(@string/some_app_key).
    Suggestion: add 'tools:replace="android:value"' to <meta-data> element at AndroidManifest.xml:18:9-133 to override.
```

#### Resolution

This is what you can try:

* Check your plugins documentation to make sure they are being correctly configured

If the issue remains:

* Modify the plugin(s) to change how the meta-data value is defined

### Google Play services dependency incompatibility

#### Symptoms

When requesting a build, you're getting the following error:

* Error generating application. Some plugins are using dependencies of Google Play services that conflict with each other. Check your plugins configuration.

#### Cause

This error occurs when building an app that uses multiple dependencies of Google Play Services whose versions conflict with each other.

The log file should contain something similar to this example, where the application tries to use at least two Google Play services library dependencies whose versions are not compatible with each other:
```
Failed to capture fingerprint of input files for task ':app:preDebugBuild' property 'compileManifests' during up-to-date check.
> In project 'app' a resolved Google Play services library dependency depends on another at an exact version (e.g. "[11.0.
  0]", but isn't being resolved to that version. Behavior exhibited by the library will be unknown.
```
#### Resolution

You can try to:

* Use different versions of the plugins that use Google Play services

If the issue remains:

* Modify the plugin(s) to change the versions of the dependencies as needed

### Minimum Android SDK incompatibility

#### Symptoms

When requesting a build, you're getting an error similar to:

* Error generating application. Library :some-lib: requires minimum Android SDK 21, which is higher than the 16 that is required by the application. Check if this value is being overridden in your Extensibility Configurations.

#### Cause

This error occurs when building an app that uses a library that requires a minimum SDK that is higher than the one required by the application. This app fails to build because the library may try to use classes, methods, resources, etc. that are not available in the minimum SDK of the application.

This can be caused by having overridden this value in the Extensibility Configurations of your application.

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

* Check if the minimum SDK value is being defined in your Extensibility Configurations

If the issue remains:

* Try using a different version of the plugin that uses the problematic library

