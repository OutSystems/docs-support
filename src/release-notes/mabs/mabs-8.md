---
summary:
guid: B1341BF3-3BC3-4E07-B06F-8BD292160229
locale: en-us
app_type: mobile apps
---

# MABS 8 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).
</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).
</div>

## MABS Version 8.1

<div class="info">

**First release:** 2022-04-06 17:00:00 UTC<br />
**Last update:** 2022-09-22 15:00:00 UTC.
</div>

<div class="warning">

If you are migrating from a previous Major version you should check the release notes, breaking changes, and system requirements from previous versions<br />
See “[System requirements](#system-requirements) and [Breaking Changes](#breaking-changes-and-known-limitations)” in MABS 8.0 Release Notes
</div>

### What's New

This minor version is focused on internal improvements, mainly around logging and security.

* Added more information to the build logs, to aid the process of troubleshooting failed builds.
* Improved validation of Extensibility Configurations preferences.
* Removed Plugin installation and compilation operation specific timeouts. Now the timeout is applied to the whole build, and no timeout exists for a specific operation.


**iOS**

* iOS builds now use Xcode 13.3.

### Bug fixing
* [2022-05-20 14:00:00 UTC] Fixed a bug where apps with & or ' in their names, or & in their extensibility configurations failed to build. (RPM-1891)
* [2022-05-20 14:00:00 UTC] Updated NPM version to overcome github changes related to the usage of the `git://` protocol. [More info here](https://github.blog/2021-09-01-improving-git-protocol-security-github/)
* [2022-06-22 15:00:00 UTC] We added new build errors that uniquely identify build failures caused by CocoaPods CDN problems. (RNMT-5601)
* [2022-06-22 15:00:00 UTC] We fixed a bug that caused builds to fail when custom icons or splash screens were only provided for the platform that was not being built. (RPM-2644)
* [2022-07-04 19:20:00 UTC] We fixed a problem with AppShield builds not finishing successfully on Android. (RPM-2747)
* [2022-07-04 19:20:00 UTC] We fixed an issue that was causing log lines to be missed in the build log file. (RPM-2744)
* [2022-07-04 19:20:00 UTC] We updated some build error messages to improve troubleshooting. (RNMT-5634)
* [2022-07-21 14:00:00 UTC] Fixed the minimum supported iOS version that was incorrectly set to 13.3 instead of 13.0 after bumping the xCode version to 13.3. (RPM-2782)
* [2022-09-21 09:00:00 UTC] Changed the minimum supported TLS version from 1.0 to 1.2. (RPM-2764)
* [2022-09-22 09:00:00 UTC] We fixed a bug where a wrong Xcode version was being used on `cordova platform add` and `cordova plugin add` commands for some iOS builds. These could lead to Pods being installed and configured with different Xcode tools than the ones used for the build process. (RNMT-5717)
* [2022-09-22 09:00:00 UTC] We made small security improvements in the MABS build process. (RNMT-5820)

## MABS Version 8.0

<div class="info">

**First release:** 2021-10-11 17:00:00 UTC<br/>
**Last update:** 2022-05-19 13:00:00 UTC
</div>

MABS 8.0 is an important milestone for all mobile developers who publish on App Store and Play Store. MABS 8 uses **iOS 15**, and **Android 12** with the **API level 31**. The stack lets you continue submitting your Android and iOS apps to the stores while taking advantage of the new features that new iOS and Android bring.

<div class="warning">

**It’s MANDATORY to upgrade all supported plugins to the latest version available on the Forge in order to use MABS 8.0. For more details, please check the [System Requirements](#system-requirements) below.**

</div>

### What's New 

* Android

    * Android Cordova Engine updated to 10.1.1

    * Gradle version increased to 7.1.1

    * Android Gradle Plugin (AGP) version updated to 7.0.0

    * Java version updated to 11

* iOS

    * iOS Cordova Engine updated to 6.2.0

* Dropped support for iOS 12

* Dropped support for Android 6, 7.0 and 7.1

* We added new error mappings for Android and iOS when a build fails. Please see [Breaking Changes](#breaking-changes-and-known-limitations) for details

* We upgraded the infrastructure for iOS builds so the infrastructure now runs on M1 architecture with Rosetta enabled

* Mobile build requests that failed due to requiring an updated plugin version will now display an error message containing the plugin name and version as defined in the Forge

### Bug Fixing 

* [2021-12-02 12:00:00 UTC] The MABS version has been added to the supported plugins validation error message. (RNMT-5248)
* [2021-12-02 12:00:00 UTC] Fixed an issue that prevented the provisioning profile entitlement com.apple.application-identifier being considered as a valid entitlement. (RNMT-5244)
* [2021-12-02 12:00:00 UTC] Improved the error message shown when a build error related to AppShield occurs. (RNMT-5252)
* [2022-02-16 12:00:00 UTC] Fixed a known issue that prevented MABS from building Android apps with the character "&" on the app name. (RPM-1666)
* [2022-03-03 09:30:00 UTC] You can now enable [touch filtering](https://developer.android.com/reference/android/view/View#security) on Android builds of apps, using the [Extensibility Configuration](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema) "FilterTouchesWhenObscured". (RPM-1749)
* [2022-03-16 15:30:00 UTC] Fixed an issue with the Upload Widget that prevented end users from receiving a request for capture and storage access permission. This occurred on the first app usage of Android builds, preventing the upload from being used. (RPM-2099)
* [2022-05-19 13:00:00 UTC] Updated NPM version to overcome github changes related to the usage of the `git://` protocol. [More info here](https://github.blog/2021-09-01-improving-git-protocol-security-github/)

### System Requirements 

Plugin requirements for **MABS**. For more details, please check the Forge by clicking on the plugin name

|Plugin|Required minimum version|
|:--|---|
|[SSL Pinning](https://www.outsystems.com/forge/component-versions/1873)|6.0.2 or later|
|[InAppBrowser](https://www.outsystems.com/forge/component-versions/1558)|2.4.5 or later|
|[Camera](https://www.outsystems.com/forge/component-versions/1390)|7.1.4 or later|
|[Ciphered Local Storage](https://www.outsystems.com/forge/component-versions/1500)|3.1.1 or later|
|[OneSignal](https://www.outsystems.com/forge/component-versions/2119)|3.5.6 or later|
|[Location](https://www.outsystems.com/forge/component-overview/1395/location-plugin)|5.1.7 or later|
|[Local Notifications](https://www.outsystems.com/forge/component-overview/1541/local-notifications-plugin)|7.0.7 or later|
|[Barcode](https://www.outsystems.com/forge/component-overview/1403/barcode-plugin)|5.0.3 or later|
|[File](https://www.outsystems.com/forge/component-versions/1633)|3.0.2 or later|
|[Touch ID](https://www.outsystems.com/forge/component-versions/1431)|3.3.2 or later|
|[Key Store](https://www.outsystems.com/forge/component-versions/1550)|2.2.1 or later|
|[Calendar](https://www.outsystems.com/forge/component-versions/1566)|3.1.3 or later|
|[Contacts](https://www.outsystems.com/forge/component-versions/1394)|4.0.5 or later|
|[Card IO](https://www.outsystems.com/forge/component-versions/1438)|3.2.1 or later|
|[Analytics (Firebase)](https://www.outsystems.com/forge/component-versions/10704)|1.0.3 or later|
|[Dynamic Links (Firebase)](https://www.outsystems.com/forge/component-versions/10988)|1.0.3 or later|
|[Performance Monitoring (Firebase)](https://www.outsystems.com/forge/component-versions/10706)|1.0.2 or later|
|[Crash Reporting (Firebase)](https://www.outsystems.com/forge/component-versions/10705)|1.0.3 or later|
|[File Viewer](https://www.outsystems.com/forge/component-versions/1606)|2.0.4 or later|
|[Health and Fitness](https://www.outsystems.com/forge/component-versions/11715.)|1.0.1 or later|
|[File Transfer](https://www.outsystems.com/forge/component-versions/1409)|2.1.3 or later|

### Breaking Changes and Known Limitations 

Here is the list of issues that may affect the building of your apps with MABS 8.0.

#### App installation fails due to safer component exporting in Android 

On MABS 8, due to targeting Android 12, apps that have activities, services or broadcast receivers that use intent filters must explicitly declare the **android:exported** attribute for these components in AndroidManifest.xml. Any case where the attribute is missing leads to a failed build with the error "Apps targeting Android 12 and higher are required to specify an explicit value for android:exported when the corresponding component has an intent filter defined".

If this error occurs to you, it means that you have a non-supported plugin with a breaking change. To fix the issue, set the **android:exported** attribute in AndroidManifest.xml to **true** or **false**. Set to **true** depending so any device can start the affected components. 

This is required not only for the AndroidManifest.xml file in the app but also in **every dependency**, such as the ones declared via Gradle.

If you have plugins that declare these elements in the** plugin.xml**, review the settings and add the attribute. Dependent plugins may also need reviewing. If builds are still failing after adding the attribute to  plugin.xml files, the issue most likely lies in AndroidManifest.xml files of other dependencies, such as Gradle dependencies declared in plugins (including dependent plugins). These dependencies can include their own AndroidManifest.xml files which must also comply with this requirement.

For more information see the section [Safer component exporting](https://developer.android.com/about/versions/12/behavior-changes-12#exported) in the document [Behavior changes: Apps targeting Android 12](https://developer.android.com/about/versions/12/behavior-changes-12) by Android.

#### Gradle compile() configuration is now obsolete 

If a plugin uses **compile** configuration in the Gradle files, the build fails. On MABS 8, due to using Gradle 7.1.1 on Android builds, the **compile** configuration to declare dependencies is no longer available. 

As an alternative, use **implementation** and **api** configurations. The **api** has the same behavior as the deprecated **compile**.

For more information see [Removal of compile and runtime configurations](https://docs.gradle.org/current/userguide/upgrading_version_6.html#sec:configuration_removal) by Gradle.

#### Whitelist Plugin is now to AllowList in newer Cordova Android engine versions 

Before MABS 8, the Cordova Android engine didn’t include logic to allow a list of URLs, intents and navigations. To handle that, a plugin called Whitelist Plugin was used. This plugin was included in all MABS builds.

The Whitelist Plugin is no longer present in MABS 8 builds as it was deprecated. The new Cordova AllowList Plugin Android engine now includes the same functionality as the deprecated plugin in other packages and classes.

For plugins that directly import the classes of the deprecated plugin, update the code so the plugins use the AllowList Plugin.

For more details about the plugin deprecation see [Apache Cordova - Whitelist Plugin](https://github.com/apache/cordova-plugin-whitelist#deprecation-notice). To have a look at a pull request that adds AllowList to Cordova Android can  see this [pull request](https://github.com/apache/cordova-android/pull/1138).

#### Plugin Installation Timeout (RPM-2222) 

There’s currently a known issue with some plugins that may cause the app build to time out and fail.
The issue is associated with a pattern of bad performance when plugins have big files (for example, ios .frameworks, .a libs, or android .so libraries). Since these files are binary files, when they are committed to a Git repository, they increase the history size exponentially.Depending on the situation, try the following to mitigate the performance issues:

* Push the plugin to a repository with no history.
* Point the plugin to the main branch. This will effectively make a shallow clone, with depth one of the tip of the master, pulling in only one commit and not all the history of the repo
* Separate the plugin into two distinct plugins, one for each platform (android and iOS).

#### Android 12 Native SplashScreen 

With Android 12, Google introduced a dedicated splash screen API in order to unify the look across all apps. This means that all apps system-wide running on Android 12 now show a native splash screen which by default is set by background color and the application icon. To improve the user experience, MABS 8 will update the Android native splash screen to have the same background as defined in cordova-plugin-splashscreen while also hiding the icon so that the end-user doesn't have two different loading experiences.
