---
summary:
guid: B954C234-277C-412D-AD66-578F98FEE428
locale: en-us
app_type: mobile apps
platform-version: o11
---

# MABS 5 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).
</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).
</div>

## MABS Version 5.2

<div class="info">

**First release:** 2019-12-26 13:30:00 UTC<br/>
**Last update:** 2022-09-21 09:00:00 UTC.
</div>

### New in this version

* Added support for HTTP redirects when using SSL Pinning.

### Bug fixing

* [2020-02-26 14:30:00 UTC] We fixed an issue with the cache that prevented the app from starting correctly. Upon closing the app, the app would not launch again after the native cache failed to cache a new app version. (RNMT-3841)
* [2020-03-11 16:00:00 UTC] We fixed an issue where MABS was not correctly handling Git URLs from less common domains. (RNMT-3897)
* [2020-04-14 13:30:00 UTC] General improvements for internal traceability of MABS
* [2020-04-29 14:30:00 UTC] We fixed the download of the iOS app cache resources that terminated unexpectedly after a download of a resource failed. (RNMT-4029)
* [2020-04-29 14:30:00 UTC] We fixed an issue with the cache system that was causing the download of app resources to fail with the timeout errors on iOS apps. (RNMT-4030)
* [2020-08-25 14:30:00 UTC] The build logs in Service Center now have more details to help you troubleshoot faster when an app fails to build.
* [2020-10-07 16:00:00 UTC] Fixed an issue with the initialization of the HTTP clients for the cache mechanism of the Android apps. (RNMT-4344)
* [2020-12-16 15:20:00 UTC] We improved the overall stability and security, with a focus on the mobile apps that use plugins with hooks. We recommend rebuilding your mobile apps and confirming they are working as expected. In cases where there are errors due to these security improvements, you'll see the error codes ERR-PLG-1017  (Error installing Cordova plugin) and ERR-GEN-1016 (Error generating application).
* [2021-01-15 15:30:00 UTC] Improved the robustness of the build process in scenarios with potential permission errors. (RNMT-4586)
* [2021-04-06 08:00:00 UTC] MABS now validates the iOS certificates and provision profiles in the initial phase of the build pipeline. This lets you see and fix potential errors early in the build process. (RNMT-4739)
* [2021-07-01 11:30:00 UTC] Added validation to prevent native mobile apps from using SSL Pinning Plugin to pin to OutSystems managed certificates. For more information, [check the documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#important-note-about-certificates).
* [2021-09-29 14:00:00 UTC] Fixed an issue that potentially leads to resource exhaustion in Android apps in MABS 5. CVSSv3.1 score 4.8 (Medium) (RPM-740)
* [2022-09-21 09:00:00 UTC] Changed the minimum supported TLS version from 1.0 to 1.2. (RPM-2764)

### Known Issue

* The issue with the screen flickering on iPhones running iOS 12, identified in MABS 4.0, when a user selects an input field in a screen with many inputs - occurs in MABS 5 as well, due to the same stack. The flickering happens when the viewport meta tag called “viewport-fit” is set to “cover”. [Here are the instructions on how to fix the issue](../../release-notes/mabs/older-releases.md#known-issue-in-mabs-4).


## MABS Version 5.1

<div class="info">

**First release:** 2019-11-06 18:30:00 UTC<br/>
**Last update:** 2019-11-12 17:00:00 UTC.
</div>

### New in this version 

* Performance improvements in the update mechanism of the apps.

* We fixed caching so apps no longer get stuck in the splashscreen.

* We improved the cache troubleshooting by adding new logs to track how the cache works.

### Bug fixing 

* [2019-11-12 17:00:00 UTC] Fixed an issue that causes iOS applications, whose name is composed of a single word, to not open successfully. (RNMT-3550)

### Known Issue

* The issue with the screen flickering on iPhones running iOS 12, identified in MABS 4.0, when a user selects an input field in a screen with many inputs - occurs in MABS 5 as well, due to the same stack. The flickering happens when the viewport meta tag called “viewport-fit” is set to “cover”. [Here are the instructions on how to fix the issue](../../release-notes/mabs/older-releases.md#known-issue-in-mabs-4).


## MABS Version 5.0

<div class="info">

**First release:** 2019-05-06 16:00:00 UTC<br/>
**Last update:** 2019-10-23 14:00:00 UTC.
</div>
 
**On 2019-10-10 we released an important fix for the Native apps that we strongly advise to request a new build of your Mobile App to get those fixes.**

## New in this version 

* MABS 5.0 uses the Android API level 28, so you will be able to continue submitting your Android apps to Google Play, in line with the recent Google announcement.

* MABS 5.0 uses Cordova Android engine 8.0.0 for Android apps. It is highly recommended that you revise your plugins to be compatible with this version.

* MABS 5.0 now uses [version 28 of Android support libraries](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Mobile_Apps_Build_Service/Android_Support_Library_Versions_for_MABS). This may cause breaking changes. If your builds have errors, check the document [MABS Upgrade Troubleshooting Guide](https://success.outsystems.com/Support/Troubleshooting/Application_development/MABS_Upgrade_Troubleshooting_Guide_-_Android). 

* With this release, we have dropped support for Android 4.4.

### Bug fixing 

* [2019-06-18 14:00:00 UTC] Fixed an issue where some Android applications with bad extensibility configuration were not showing the correct error message after a build failed. (RNMT-2957)
* [2019-06-18 17:00:00 UTC] Fixed an issue that caused iOS apps that use CocoaPods not to deploy to the correct target target. (RNMT-2965)
* [2019-07-01 17:00:00 UTC] Improved the installation of the plug-ins to make it more stable. (RNMT-2959)
* [2019-07-01 17:00:00 UTC] Improved the detection of errors related to the files required for the Android builds. (RNMT-2845)
* [2019-07-01 17:00:00 UTC] Improved the errors about AndroidX libraries. These libraries are currently not compatible with MABS. (RNMT-2788)
* [2019-07-01 17:00:00 UTC] Improved the detection of errors related to the plugin dependency conflicts in the Android builds. (RNMT-3029)
* [2019-07-01 17:00:00 UTC] Improved the detection of errors related to the Google Play Services dependency conflicts in the Android builds. (RNMT-3046)
* [2019-07-01 17:00:00 UTC] Improved the detection of errors when Google Services is not correctly configured for the Android builds. (RNMT-2927)
* [2019-07-31 14:00:00 UTC] We fixed an issue that caused an error screen when using deep links to open other apps. (RNMT-3080)
* [2019-07-31 14:00:00 UTC] The users no longer end up on an error screen when navigating between screens, in some conditions when there's no Internet connectivity or when the connectivity is poor. We fixed an issue related to caching and the offline mode. (RNMT-3056)
* [2019-08-21 19:00:00 UTC] Fixed an issue with images failing to load with SSL Pinning plug-in. (RNMT-3176)
* [2019-08-21 19:00:00 UTC] Improved detection of the build errors, so the iOS application builds no longer fail due to CocoaPods repository update errors. (RNMT-3073)
* [2019-09-11 14:00:00 UTC] We fixed the back button, so it correctly navigates to the previous content in all platforms. Due to this bug, the back button closed a full-screen app on Android. (RNMT-3244)
* [2019-09-25 14:00:00 UTC]  Removed xcconfig build flag that may builds using pods no longer fail with linker
* [2019-10-09 11:00:00 UTC] Fixed a native cache bug that prevented the cache invalidation on application update. (RNMT-3331)
* [2019-10-10 14:00:00 UTC] Fixed the cache frame recovery for the current application version. (RNMT-3389)
* [2019-10-10 14:00:00 UTC] Fixed the cache healing mechanism so it no longer creates infinite download tasks to recover a resource. (RNMT-3386)
* [2019-10-10 14:00:00 UTC] Fixed an issue that was preventing the cache from getting the files from the Web when those files were not available in the prebundle. (RNMT-3390)
* [2019-10-10 14:00:00 UTC] Fixed an issue that was causing apps to sometimes stop responding in the splash screen. (RNMT-3394)
* [2019-10-17 11:00:00 UTC] We fixed the Jitpack URL for the core plugins. This issue was causing conflicts with other plugins that made use of the Jitpack repository to import libraries. (RNMT-3405)
* [2019-10-23 14:00:00 UTC] Now all network requests contain the User-Agent header from the WebView instance. This means that every request carries information about the version of the app, which you can use to implement behavior based on the version. (RNMT-3428)

### Known Issue 

* The issue with the screen flickering on iPhones running iOS 12, identified in MABS 4.0, when a user selects an input field in a screen with many inputs - occurs in MABS 5 as well, due to the same stack. The flickering happens when the viewport meta tag called “viewport-fit” is set to “cover”. [Here are the instructions on how to fix the issue](../../release-notes/mabs/older-releases.md#known-issue-in-mabs-4).


## Older releases
Release notes for older MABS versions are available at [Mobile Apps Build Service (older versions)](older-releases.md).