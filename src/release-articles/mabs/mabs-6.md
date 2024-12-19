---
summary:
guid: BDA4BE15-1C6E-4CAE-B8FF-95DD58F6C711
locale: en-us
app_type: mobile apps
platform-version: o11
---

# MABS 6 Release notes

<div class="info" markdown="1">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).
    
</div>

<div class="info" markdown="1">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).

</div>

## MABS Version 6.3

First release: 2020-09-23 16:00:00 UTC
Last update: 2021-09-29 14:00:00 UTC

If you are migrating from a previous Major version you should check the release notes, breaking changes and system requirements from previous versions.
See “System requirements and Breaking Changes” in MABS 6.0 Release Notes

### What's New

* In MABS 6.3 we introduce the option to compile the Android apps using AndroidX instead of the legacy Android Support Library. AndroidX is optional, so you need to enable the AndroidX support in your apps. For more information see [Building apps with AndroidX](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Mobile_Apps_Build_Service/Building_apps_with_AndroidX).

### Bug fixing

* [2020-10-07 16:00:00 UTC] Fixed an issue with the initialization of the HTTP clients for the cache mechanism of the Android apps. (RNMT-4344)
* [2020-11-03 17:45:00 UTC] We fixed an issue that was blocking the builds from having AndroidX enabled. (RNMT-4493)
* [2020-11-06 10:30:00 UTC] We fixed the logging mechanism to prevent it from sending logs before the SSL Pinning plugin is loaded. (RNMT-4499)
* [2020-11-26 19:00:00 UTC] We fixed an issue that was causing apps to show an error screen at startup when the SSL Pinning Plugin configurations were incorrect. (RNMT-4514)
* [2020-11-27 20:10:00 UTC] We fixed app crashes in Android related to SSL Pinning Plugin. An app could crash when there was an exception without a message while the app was obtaining a pinned resource. (RNMT-4520)
* [2020-12-21 15:00:00 UTC] We improved the overall stability and security, with a focus on the **Android** mobile apps that use plugins with hooks. We recommend rebuilding your mobile apps and confirming they are working as expected. In cases where there are errors due to these security improvements, you'll see the error codes ERR-PLG-1017  (Error installing Cordova plugin) and ERR-GEN-1016 (Error generating application).
* [2020-12-23 15:00:00 UTC] Adds a new error message in the error handler for plugins with missing dependencies for node modules due to the security improvements. 
* [2020-12-23 15:00:00 UTC] Added a new error message in the error handler for plugins with missing dependencies for node modules due to the security improvements. 
* [2020-12-23 15:00:00 UTC] We fixed error messages in the error handler for maven repository operations. (RNMT-4542)
* [2020-12-28 14:30:00 UTC] We improved the overall stability and security, with a focus on the iOS mobile apps that use plugins with hooks. We recommend rebuilding your mobile apps and confirming they are working as expected. In cases where there are errors due to these security improvements, you'll see the error codes ERR-PLG-1017  (Error installing Cordova plugin) and ERR-GEN-1016 (Error generating application).
* [2021-01-15 09:30:00 UTC] Improved the robustness of the build process in scenarios with potential permission errors. (RNMT-4586)
* [2021-02-17 15:30:00 UTC] Fixed iOS debug builds that have CocoaPods with the dynamic framework dependencies. (RNMT-4687)
* [2021-02-19 15:30:00 UTC] We fixed an Android issue related to the SSL Pinning Plugin that was causing apps to show an error screen at startup. (RNMT-4710)
* [2021-03-31 11:30:00 UTC] You can now add the Referer header to the custom scheme requests (iOS only). (RNMT-4762)
* [2021-03-31 10:30:00 UTC] Fixed some Android apps crashing after removing the splash screen. (RNMT-4755)
* [2021-04-06 08:00:00 UTC] MABS now validates the iOS certificates and provision profiles in the initial phase of the build pipeline. This lets you see and fix potential errors early in the build process. (RNMT-4739)
* [2021-04-14 15:00:00 UTC] Fixed a typo in some logs on the OSCache component for the Android platform. Where before was ‘File is corrput or invalid’ is now ‘File is corrupt or invalid’. (RNMT-4765)
* [2021-04-21 14:10:00 UTC] Improved OSCache plugin logging when there is a hash mismatch between cached file and the remote version of the same file (RNMT-4767)
* [2021-05-05 01:30:00 UTC] Workaround to mitigate [JitPack downtime Incident](https://status.outsystems.com/incidents/pnslqmryvz9g) applied, using some OutSystems core packages locally instead of fetching from JitPack. Inspector plugin was disabled to allow for builds to finish successfuly (RNMT-4895). This workaround was reverted after the JitPack incident was resolved [2021-05-05 09:20:00 UTC]
* [2021-05-12 15:00:00 UTC] We changed the priority of the MavenCentral repository to be higher than the JCenter repository. This will reduce the impact of the JCenter sunset in OutSystems mobile apps for Android. (RNMT-4821)
* [2021-05-19 15:30:00 UTC] Fixed an issue that was causing the Native Logger to perform concurrent network requests to the server on iOS (RNMT-4892)
* [2021-07-01 11:30:00 UTC] Added validation to prevent native mobile apps from using SSL Pinning Plugin to pin to OutSystems managed certificates. For more information, [check the documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#important-note-about-certificates).
* [2021-09-29 14:00:00 UTC] Fixed an issue that potentially leads to resource exhaustion in Android apps in MABS 6. CVSSv3.1 score 4.8 (Medium) (RPM-740)
 

### How to fix "Error installing a Cordova plugin"

Some customers started getting the following error in MABS 6, after MABS security improvements in December 2020:

*Error installing a Cordova plugin. Due to security concerns, the required dependency for the '{0}' node module in a plugin hook was missing. For more details, check the product documentation on how to ensure your plugins node dependencies.*

MABS no longer uses a shared cache for NPM dependencies, which means that you need to make sure that MABS has all the available dependencies for the build. Do this by installing the dependencies for the hooks.

For example, if you’re getting an error because the build cannot find the dependency **elementtree**, fix the error by following these steps:

1. Add a **package.json** file with the required dependencies for your hooks in their folders. [Here is a package.json example](https://github.com/OutSystems/outsystems-plugin-disable-backup/blob/master/hooks/package.json).
1. To install the dependencies, create a JavaScript file to run the **npm install** command. [Check out an example here](https://github.com/OutSystems/outsystems-plugin-disable-backup/blob/master/hooks/dependencyInstaller.js).
1. Add the JavaScript file to the **plugin.xml** as a hook of the type **before_plugin_install**. [See this code for an example](https://github.com/OutSystems/outsystems-plugin-disable-backup/blob/master/plugin.xml#L14).

## MABS Version 6.2

<div class="info">

**First release:** 2020-05-20 16:00:00 UTC<br/>
**Last update:** 2020-10-07 16:00:00 UTC.

</div>

### What's New

* Fixed occasional out of memory crashes when fetching large data from the server.

* We improved the cache system log level to exclude invalid entries from being logged in Service Center.

* Fixed an issue where the native shell was communicating with the default HTTPS port when the host of the app indicated a different port. (RNMT-4013)

### Bug fixing

* [2020-07-01 17:00:00 UTC] We fixed a glitch that caused the screen to scroll up after closing the keyboard. Note that this fix is applicable to iOS versions earlier than iOS 13.4, as Apple fixed it in iOS 13.4 and later. (RNMT-4155)
* [2020-07-06 10:00:00 UTC] General improvements for internal orchestration of MABS Builds
* [2020-07-15 14:30:00 UTC] Fixed an issue when copying prebundled resources to the cache mechanism that could cause caching operations to fail. (RNMT-4163)
* [2020-07-15 14:30:00 UTC] We fixed an issue with the cache mechanism that prevented some users from using the iOS app generated by MABS, as the apps didn't load past the splash screen. Additionally, error logs showed "Failed to handle request / The Internet connection appears to be offline".  (RNMT-4160)
* [2020-07-15 14:30:00 UTC] Fixed the generation of Android apps when the app name starts with non-letter characters. A bug in Cordova caused this issue. (RNMT-4133)
* [2020-07-29 15:30:00 UTC] Fixed occasional failures in server actions, in Android, when the app was handling multiple HTTP requests simultaneously. (RNMT-4220)
* [2020-08-12 14:30:00 UTC] Fixed Server Actions so they finish execution properly and don't block flows from reaching the end. There was an issue with the HTTP requests on Android WebViews in versions earlier than 39. (RNMT-4224)
* [2020-08-26 11:30:00 UTC] The build logs in Service Center now have more details to help you troubleshoot faster when an app fails to build.
* [2020-08-26 11:30:00 UTC] Fixed the camera permission request on Android. Now the app asks for the camera permission when the user taps the upload button, and not for the storage permission. This bug blocked the camera from opening. (RNMT-4236)
* [2020-09-09 15:30:00 UTC] Fixed an issue that prevented users from logging in iOS apps when the environment was hosted in a port that is not the default HTTPS port. (RNMT-4279)
* [2020-10-07 16:00:00 UTC] Fixed an issue with the initialization of the HTTP clients for the cache mechanism of the Android apps. (RNMT-4344)

## MABS Version 6.1

<div class="info">

**First release:** 2020-02-05 15:00:00 UTC<br/>
**Last update:** 2020-08-26 14:30:00 UTC.

</div>

### What's New

* MABS now uses Cordova iOS engine 5.1.1 for the iOS apps. We recommend you revise your plugins to ensure compatibility with this version.

* The iOS apps generated with MABS 6.1 now contain references only to WKWebView, as we removed the UIWebView references. This also means you will no longer see the the ITMS-90809: Deprecated API Usage warning when you submit your app to the App Store. The removal of UIWebView API comes following [Apple's instructions and announcement](https://developer.apple.com/news/?id=12232019b) that `"[t]he App Store will no longer accept new apps using UIWebView as of April 2020 and app updates using UIWebView as of December 2020."`

* The InAppBrowser plugin is updated to remove the references to UIWebView. If you are using the InAppBrowser plugin, you should update to version 2.3.0. Note that this version of the plugin is retrocompatible with MABS 5 which still uses UIWebView.

### Bug fixing

* [2020-02-05 15:00:00 UTC] Fixed an issue with the custom scheme handler for the WKWebView that was causing iOS apps to crash.
* [2020-02-26 14:30:00 UTC] We fixed an issue with the cache that prevented the app from starting correctly. Upon closing the app, the app would not launch again after the native cache failed to cache a new app version. (RNMT-3841)
* [2020-03-11 16:00:00 UTC] We fixed the Network Inspector notifications on Android versions Android N and earlier, so the push notification title now shows correctly. (RNMT-3764) 
* [2020-03-11 16:00:00 UTC] Minor improvements to increase the robustness of the cache mechanism. (RNMT-3788)
* [2020-03-11 16:00:00 UTC] We fixed an issue where MABS was not correctly handling Git URLs from less common domains. (RNMT-3897)
* [2020-03-24 12:30:00 UTC] Fixed OneSignal registration for the push notifications. (RNMT-3855)
* [2020-03-24 12:30:00 UTC] We changed the copy of the Network Inspector push notification. (RNMT-3844)
* [2020-03-24 12:30:00 UTC] Now there's a delay before Network Inspector shows the push notification asking for the permission. This improves the user experience as it's less distracting. (RNMT-3845)
* [2020-04-08 14:30:00 UTC] Apps no longer crash on launch after installing a new version. A bug related to the WKWebView engine implementation was causing the crash. (RNMT-3992)
* [2020-04-14 13:30:00 UTC] General improvements for internal traceability of MABS
* [2020-04-22 14:00:00 UTC] Fixes an issue with Cookies synchronization that was causing network connections to fail on iOS apps, when Cookies with quoted values were used. (RNMT-4000)
* [2020-04-29 15:30:00 UTC] We fixed the download of the iOS app cache resources that terminated unexpectedly after a download of a resource failed. (RNMT-4029)
* [2020-04-29 15:30:00 UTC] We fixed an issue with the cache system that was causing the download of app resources to fail with the timeout errors on iOS apps. (RNMT-4030)
* [2020-07-01 17:00:00 UTC] We fixed a glitch that caused the screen to scroll up after closing the keyboard. Note that this fix is applicable to iOS versions earlier than iOS 13.4, as Apple fixed it in iOS 13.4 and later. (RNMT-4155)
* [2020-07-06 10:00:00 UTC] General improvements for internal orchestration of MABS Builds
* [2020-07-15 14:30:00 UTC] Fixed an issue when copying prebundled resources to the cache mechanism that could cause caching operations to fail. (RNMT-4163)
* [2020-07-15 14:30:00 UTC] We fixed an issue with the cache mechanism that prevented some users from using the iOS app generated by MABS, as the apps didn't load past the splash screen. Additionally, error logs showed "Failed to handle request / The Internet connection appears to be offline".  (RNMT-4160)
* [2020-07-15 14:30:00 UTC] Fixed the generation of Android apps when the app name starts with non-letter characters. A bug in Cordova caused this issue. (RNMT-4133)
* [2020-08-26 11:30:00 UTC] The build logs in Service Center now have more details to help you troubleshoot faster when an app fails to build.

### System Requirements

**InAppBrowser Plugin**

InAppBrowser plugin must be the latest version (2.3.0 or later) to be supported correctly in MABS 6.1.

## MABS Version 6.0

<div class="info">

**First release:** 2019-09-18 14:00:00 UTC<br/>
**Last update:** 2020-02-26 14:30:00 UTC.

</div>

MABS 6.0 is an important milestone for all developers who publish on App Store and Play Store. This new MABS version uses Android 10 (API level 29), iOS 13 and iOS WkWebview engine, allowing you to continue to submit your iOS apps to the App Store and your Android apps to the Play store.

### What's New

* We introduce WKWebView as the default WebView to load web content in Mobile Apps. This ensures your apps are compliant with Apple Requirements to accept mobile applications to the store.
* New Cordova Native Plugin for Network requests.
* iOS applications now load from `outsystems://` instead of `https://`. This enables the offline support with WKWebView.
* Dropped support for iOS 10.
* Mobile Apps Build Service now uses the latest iOS SDK 13, so you will be able to continue submitting your iOS apps to the App Store, in line with the recent Apple announcement.
* Mobile Apps Build Service now uses Cordova iOS engine 5.0.1 for iOS apps. We highly recommend you revise your plugins for compatibility with this version.
* Mobile Apps Build Service now uses CocoaPods version 1.7.5. You should revise your plugins that have dependencies for CocoaPods.
* iOS apps now support iPhone11/11 Pro/11 Pro Max and iPad (7th generation).
* The workaround we provided for a [known issue in MABS 4 to disable the viewport-fit tag](#known-issue-in-mabs-4) is no longer needed. The workaround is now ignored, even if you’re using it.
* MABS 6.0 Beta 3 introduces Android API level 29. This enables you to submit your Android apps to Google Play with the most recent target SDK.
* MABS 6.0 Beta 3 uses Cordova Android engine 8.1.0 for Android apps. It is highly recommended that you ensure your plugins are compatible with the version 8.1.0.
* The build process now has a more robust validation for the supported plugins. If the app is not using the minimum supported plugin version, the build request fails early with details available in the error output.
* You can now check the network requests in iOS and Android by using the tool available in the debug builds created with MABS 6.0. For more information, see [Inspect the HTTP requests in Mobile Apps for iOS](https://success.outsystems.com/Documentation/11/Developing_an_Application/Troubleshooting_Applications/Inspect_the_HTTP_requests_in_Mobile_Apps_for_iOS).

### Bug fixing

* [2020-02-05 12:00:00 UTC] Fixed an issue with the custom scheme handler for the WKWebView that was causing iOS apps to crash.
* [2020-02-26 14:30:00 UTC] We fixed an issue with the cache that prevented the app from starting correctly. Upon closing the app, the app would not launch again after the native cache failed to cache a new app version. (RNMT-3841)

### System Requirements

**Platform Server**

To have access to MABS 6.0 you need the following versions of Platform Server:

* OutSystems 10 - 10.0.1016.0 or later
* OutSystems 11 - 11.0.539.0 or later

**Service Studio**

The minimal version of Service Studio that ensures proper work of the Mobile Debugger with MABS 6.0: 

* Service Studio 10 - 10.0.1017.0 or later
* Service Studio 11 - 11.5.44.2557 or later

**SSL Pinning **

SSL Pinning plugin must be the latest version (4.0.0 or later) to be supported correctly in MABS 6.0.

**InAppBrowser Plugin**

InAppBrowser plugin must be the latest version (2.2.0 or later) to be supported correctly in MABS 6.0.

**OneSignal Plugin**

OneSignal plugin must be the latest version (3.1.0 or later) to be supported correctly in MABS 6.0.

**Local Notifications Plugin**

Local Notifications plugin must be the latest version (6.1.0 or later) to be supported correctly in MABS 6.0.

### Breaking Changes and Known Limitations

Here is the list of issues that may appear when building your apps with MABS 6.0 Beta 2. Check [MABS 6.0 Breaking Changes and Known Limitations](troubleshoot-issues-with-mabs-6.md) for information on how to resolve potential issues.

* XHR / Fetch requests to OutSystems servers don't work
* Cookies from OutSystems servers are not accessible from document.cookie
* RedirectToURL Event fails
* Web Inspector doesn't show Network information
* Content-Security-Policy may incur new violations in iOS. Android is unaffected.
