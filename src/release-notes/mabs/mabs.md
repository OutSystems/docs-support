---
summary:
guid: B1341BF3-3BC3-4E07-B06F-8BD292160229
locale: en-us
---

# Mobile Apps Build Service

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).
</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).
</div>

## MABS Version 8.1

<div class="info">

**First release:** 2022-04-06 17:00:00 UTC<br />
**Last update:** 2022-04-12 17:00:00 UTC.
</div>

<div class="warning">

If you are migrating from a previous Major version you should check the release notes, breaking changes, and system requirements from previous versions<br />
See “[System requirements](#system-requirements) and [Breaking Changes](#breaking-changes-and-known-limitations)” in MABS 8.0 Release Notes
</div>

### What's New

This minor version is focused on internal improvements, mainly around logging and security.

**iOS**

* Upgrade to Xcode 13.3


## MABS Version 8.0

<div class="info">

**First release:** 2021-10-11 17:00:00 UTC<br/>
**Last update:** 2022-03-16 16:00:00 UTC
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

## MABS Version 7.2

<div class="info">

**First release:** 2021-09-01 15:40:00 UTC<br/>
**Last update:** 2022-03-03 10:25:00 UTC
</div>

<div class="warning">

If you are migrating from a previous **Major** version you should check the release notes, breaking changes and system requirements from previous **versions**.<br/>
See “System requirements and Breaking Changes” in MABS 7.0 Release Notes
</div>

### What's New

* Improved Logger API that now receives a flexible log record to properly send all log info with predefined timestamps to the server. (RPM-1172)

* Added the device UUID to the HTTP request headers to improve troubleshooting.

### Bug Fixing

* [2021-09-01 14:30:00 UTC] We improved MABS error messages so they guide you better in fixing the issues (RNMT-4946)
* [2021-09-01 14:30:00 UTC] Fixed an issue that could lead to resource exhaustion in Android apps. CVSSv3.1 score 4.8 (Medium) (RPM-740)
* [2021-10-20 15:00:00 UTC] Fixed an issue that caused the splash screen to take too long to disappear when being manually dismissed in iOS apps (RPM-983)
* [2021-12-02 12:00:00 UTC] The MABS version has been added to the supported plugins validation error message.  (RNMT-5248)
* [2021-12-02 12:00:00 UTC] Fixed an issue that prevented the provisioning profile entitlement com.apple.application-identifier being considered as a valid entitlement.  (RNMT-5244)
* [2021-12-02 12:00:00 UTC] Improved the error message shown when a build error related to AppShield occurs.  (RNMT-5252)
* [2022-03-03 09:45:00 UTC] You can now enable [touch filtering](https://developer.android.com/reference/android/view/View#security) on Android builds of apps, using the [Extensibility Configuration](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema) "FilterTouchesWhenObscured". (RPM-1749)

## MABS Version 7.1

<div class="info">

**First release:** 2021-06-16 14:00:00 UTC<br/>
**Last update:** 2021-09-01 15:40:00 UTC
</div>

<div class="warning">

If you are migrating from a previous **Major** version you should check the release notes, breaking changes and system requirements from previous **versions**.<br/>
See “[System requirements](#system-requirements-for-mabs-70) and [Breaking Changes](#breaking-changes-and-known-limitations-for-mabs-70)” in MABS 7.0 Release Notes
</div>

For minimum System Requirements, see “[About System requirements for MABS 7.0 and later](#system-requirements-for-mabs-70)”

### What's New

* With MABS 7.1 you can define the Usage Descriptions required for the iOS apps at Application level (see the section **[iOS Usage Descriptions](#ios-usage-descriptions)**). (RPM-326)

* We added the option to remove unwanted permissions when building applications without the Upload widget (see the section **[Upload Widget Permissions](#upload-widget-permissions)**). (RPM-471)

* In the iOS debug builds, you can now turn off the notification "Heads up! Enable OutSystems Developer Tools..." by setting the `DisableInspectorNotification` preference to `true` in the Extensibility Configurations. (RPM-968)

#### iOS Usage Descriptions

Add the Usage Descriptions to the JSON of Extensibility Configurations by inserting a **name / value** key pair, where the **name** ends in **UsageDescription**. MABS searches for preferences that end in **UsageDescription** and adds them to the **Info.plist** of your iOS app. For the available descriptions see [Information Property List Key Reference](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/CocoaKeys.html) by Apple.

**Example**

To override the CameraPlugin Usage Description in an app, add the following to the Extensibility Configurations JSON of the app home module:

```
{
    "preferences": {
        "ios": [{
            "name": "NSCameraUsageDescription",
            "value": "This application makes use of the Camera because"
        }]
    }
}
```

#### Upload Widget Permissions

All OutSystems apps can use the Upload widget. The consequence of this is that the native mobile apps require some default permissions, even without adding other plugins. In the apps without the Upload widget the requirements for the default permissions can sometimes add extra permissions to the app, such as the Camera permission. In MABS 7.1 you can use a new option to remove such permissions, by adding the **AddUploadWidgetPermissions** setting to the Extensibility Configurations JSON :

```
{
    "preferences": {
        "global": [{
            "name": "AddUploadWidgetPermissions",
            "value": "false"
        }]
    }
}
```

Set the **AddUploadWidgetPermissions** to **false** only in the apps that don't use the Upload widget. If you later need the Upload widget in the app, add the widget and then set **AddUploadWidgetPermissions** to **true** and create a new build.

 

### Bug Fixing

* [2021-06-30 16:00:00 UTC] Fixed wrong log messages for the self-healing mechanism. (RNMT-4923)
* [2021-06-30 16:00:00 UTC] Fixed mobile apps getting stuck on the splash screen when opening the app via a deeplink. (RPM-1226)
* [2021-06-30 16:00:00 UTC] Fixed the logging mechanism so it correctly shows "Failed to store downloaded resource ... File is corrupt or invalid" in the logs for the iOS apps. (RNMT-4921)
* [2021-06-30 16:00:00 UTC] Fixed the logging mechanism so it correctly shows "Failed to load cache manifest" in the logs for the iOS apps. Also, improved the consistency of logs for both iOS and Android. (RNMT-4917)
* [2021-06-30 16:00:00 UTC] Improved the load of the related requests by optimizing the logger distribution functions. (RPM-994)
* [2021-07-01 11:30:00 UTC] Added validation to prevent native mobile apps from using SSL Pinning Plugin to pin to OutSystems managed certificates. For more information, [check the documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#important-note-about-certificates).
* [2021-07-14 12:30:00 UTC] Fixed invalid prebundle resource indexing in the OSCache healing process that caused the error "Could not get InputStream".  (RNMT-4922)]
* [2021-07-14 12:30:00 UTC] Fixed a bug that caused some builds to fail when installing the cordova-whitelist-plugin with the message "An unexpected error has occurred while installing the Cordova plugins. Please try again. If the problem persists, contact OutSystems Support." (RNMT-4983)
* [2021-07-28 15:00:00 UTC] Added more details about the validations to the build log file. The logs now contain additional information about each validation step, which can better assist you in troubleshooting and monitoring the build of your mobile apps.
* [2021-08-04 11:00:00 UTC] Fixed invalid comparison of product version tokens to prevent the error “Generation failed due to plugin version incompatibility with MABS” showing for compatible versions.
* [2021-08-18 14:00:00 UTC] We improved the text of some error messages to make them more helpful. This applies to the errors about supported plugins, certificates, shielding, app preferences, app bundles, and resources. (RNMT-4942)
* [2021-08-18 14:00:00 UTC] We fixed the issue that prevented users from installing the app generated with MABS 7 on devices with iOS 15 beta. The device showed the error "The developer of this app needs to update it to work with this version of iOS" and blocked the installation. The error occurred because Apple changed code signing in Xcode and MABS needed to adjust. (RPM-1390)
* [2021-09-01 14:30:00 UTC] We improved MABS error messages so they guide you better in fixing the issues (RNMT-4946)
* [2021-09-01 14:30:00 UTC] Fixed an issue that could lead to resource exhaustion in Android apps. CVSSv3.1 score 4.8 (Medium) (RPM-740)


## MABS Version 7.0

<div class="info">

**First release:** 2020-12-09 14:00:00 UTC<br/>
**Last update:** 2021-07-14 12:30:00 UTC.
</div>

MABS 7.0 is an important milestone for all developers who publish on App Store and Play Store. This new MABS version uses Android 11 with the API level 30, iOS 14, and Cordova CLI 10. This stack lets you continue submitting your Android and iOS apps to the stores.

### What's New

* Mobile Apps Build Service (MABS) now uses the iOS SDK 14.2. This means that you can continue submitting your iOS apps to the App Store while complying with the requirements by Apple.

* AndroidX is enabled by default. Fore more information see [Building apps with AndroidX](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Mobile_Apps_Build_Service/Building_apps_with_AndroidX)

* Latest Android API level 30. This lets you submit your Android apps with the most recent target SDK to Google Play.

* iOS apps now support iPhone 12, iPhone 12 Pro, and iPhone 12 Mini. 

* Cordova iOS engine 6.1.1 for iOS apps. We highly recommend you revise your plugins for compatibility with this version.

* Cordova Android engine 9.0.0 for Android apps. It is highly recommended that you ensure your plugins are compatible with this version.

* Cordova Command Line Tool (CLI) 10.0.0. We highly recommend you revise your plugins for compatibility with this version.

* CocoaPods version 1.10.0. You should revise your plugins that have dependencies for CocoaPods.

* We improved the overall stability and security, with a focus on the mobile apps that use plugins with hooks. We recommend rebuilding your mobile apps and confirming they are working as expected.

* Removed the [network inspector](https://success.outsystems.com/Documentation/11/Developing_an_Application/Troubleshooting_Applications/Inspect_the_HTTP_requests_in_Mobile_Apps_for_iOS) from the Android builds. It’s now available for iOS only, as this is a feature specific for the iOS builds.

* Dropped support for iOS 11.

* Dropped support for Android 5 and 5.1

### Bug fixing

* [2021-01-15 14:00:00 UTC] Improved the robustness of the build process in scenarios with potential permission errors. (RNMT-4586)
* [2021-02-17 18:30:00 UTC] Improved a build error message when using requireCordovaModule from a plugin hook to load non-Cordova modules. (RNMT-4668)
* [2021-02-17 18:30:00 UTC] Fixed iOS build process for apps with custom Cordova plugins. (RNMT-4669)
* [2021-02-17 18:30:00 UTC] Fixed iOS debug builds that have CocoaPods with the dynamic framework dependencies. (RNMT-4687)
* [2021-02-19 15:30:00 UTC] We fixed an Android issue related to the SSL Pinning Plugin that was causing apps to show an error screen at startup. (RNMT-4710)
* [2021-03-17 10:30:00 UTC] Improved the feedback messages about the following errors: timeouts, Swift compilation, and the plugin installation. (RNMT-4585)
* [2021-04-06 08:00:00 UTC] MABS now validates the iOS certificates and provision profiles in the initial phase of the build pipeline. This lets you see and fix potential errors early in the build process. (RNMT-4739)
* [2021-04-21 15:00:00 UTC] You can now add the Referer header to the custom scheme requests (iOS only). (RNMT-4762)
* [2021-04-21 15:00:00 UTC] Fixed a typo in some logs on the OSCache component for the Android platform. Where before was ‘File is corrput or invalid’ is now ‘File is corrupt or invalid’. (RNMT-4765)
* [2021-04-21 15:00:00 UTC] Improved OSCache plugin logging when there is a hash mismatch between cached file and the remote version of the same file (RNMT-4767)
* [2021-05-05 00:30:00 UTC] Workaround to mitigate [JitPack downtime Incident](https://status.outsystems.com/incidents/pnslqmryvz9g) applied, using some OutSystems core packages locally instead of fetching from JitPack (RNMT-4895)
* [2021-05-12 15:00:00 UTC] We changed the priority of the MavenCentral repository to be higher than the JCenter repository. This will reduce the impact of the JCenter sunset in OutSystems mobile apps for Android. (RNMT-4821)
* [2021-05-19 15:30:00 UTC] Fixed an issue that was causing the Native Logger to perform concurrent network requests to the server on iOS (RNMT-4892)
* [2021-06-02 10:00:00 UTC] You can now remove user-added certificates from the custom trust anchors in the Android builds. Set RemoveUserCertificates to true in the Android preferences section of the Extensibility Configuration to let MABS remove `<certificates src="user" />` from the build. This overrides a default setting of the OutSystems Android apps and lets you build mobile apps that trust only the default CAs, and exclude the CAs the users might add. (RNMT-4905)
* [2021-06-30 14:00:00 UTC] Fixed wrong log messages for the self-healing mechanism. (RNMT-4923)
* [2021-06-30 14:00:00 UTC] Fixed mobile apps getting stuck on the splash screen when opening the app via a deeplink. (RPM-1226)
* [2021-06-30 14:00:00 UTC] Fixed the logging mechanism so it correctly shows "Failed to store downloaded resource ... File is corrupt or invalid" in the logs for the iOS apps. (RNMT-4921)
* [2021-06-30 14:00:00 UTC] Fixed the logging mechanism so it correctly shows "Failed to load cache manifest" in the logs for the iOS apps. Also, improved the consistency of logs for both iOS and Android. (RNMT-4917)
* [2021-07-01 11:30:00 UTC] Added validation to prevent native mobile apps from using SSL Pinning Plugin to pin to OutSystems managed certificates. For more information, [check the documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#important-note-about-certificates).
* [2021-07-14 12:30:00 UTC] Fixed invalid prebundle resource indexing in the OSCache healing process that caused the error "Could not get InputStream".  (RNMT-4922)]
* [2021-07-14 12:30:00 UTC] Fixed a bug that caused some builds to fail when installing the cordova-whitelist-plugin with the message "An unexpected error has occurred while installing the Cordova plugins. Please try again. If the problem persists, contact OutSystems Support." (RNMT-4983)
 

### System Requirements for MABS 7.0

Some plugin requirements for **MABS**.

|Plugin|Required minimum version|MABS
|:--|:--|:--|
|[SSL Pinning](https://www.outsystems.com/forge/component-versions/1873)|6.0.0 or later|MABS 7.0 and later|
|[InAppBrowser](https://www.outsystems.com/forge/component-versions/1558)|2.4.0 or later|MABS 7.0 and later|
|[Camera](https://www.outsystems.com/forge/component-versions/1390)|6.2.0 or later|MABS 7.0 and later|
|[Ciphered Local Storage](https://www.outsystems.com/forge/component-versions/1500)|3.1.0 or later|MABS 7.0 and later|
|[OneSignal](https://www.outsystems.com/forge/component-versions/2119)|3.5.0 or later|MABS 7.0 and later|

 

### Breaking Changes and Known Limitations for MABS 7.0

Here is the list of issues that may appear when building your apps with MABS 7.0.

#### All plugins are now installed using npm

With Cordova CLI 10, the platform uses the npm-install command to install the plugins. If you're using hosted git providers, you may need to adjust the protocol from **http/https** to **git**, as **http/https** is not supported by some hosted git providers. See the [npm-install documentation](https://docs.npmjs.com/cli/v7/commands/npm-install) and change your plugin configuration as needed.

**Workaround**

Prefix url protocol with **git+**

**Examples:**

* `git+https://[repo]`

#### Commit or subdir element no longer effects dependency definition

The commit or subdir element no longer has any effect on dependency definition For example, `<dependency id="..." url="https://x.git" commit="y" />` no longer installs `https://x.git#y`, but instead plain `https://x.git`.

**Workaround**

Put the complete URL in the url element.

#### context.requireCordovaModule no longer supported for loading non-Cordova modules

Using **context.requireCordovaModule** to load non-cordova modules is not supported anymore. Trying to build an app on MABS 7 with a plugin that uses **context.requireCordovaModule**, causes a message similar to:

Error installing Cordova plugin: {0}. Using "requireCordovaModule" to load non-cordova modules {PLUGIN NAME} is not supported. Instead, add this module to your dependencies and use regular "require" to load it.

**Workaround**

Replace **context.requireCordovaModule** with **require** and define the dependencies on **package.json**. Skip this for modules that belong to **Node**.

#### Xcode required in package.json

Hooks in plugins requiring modules need to add modules such as “xcode” to the package.json

When a build fails with, logs similar to this are shown: Cannot find module 'xcode'

**Workaround**

Define the dependencies in package.json.

#### Value user-agent no longer available through CDVUserAgentUtil

With the new **cordova-ios engine 6.1.1**, any Cordova plugin that requires **user-agent** no longer can get it through the **CDVUserAgentUtil** component.

**Workaround**

Or any Cordova plugin that requires **user-agent**, ensure the following:

* The plugin no longer depends on the **CDVUserAgentUtil** component.

* The plugin is no longer retrieving the **user-agent** from the **CDVPlugin** or the **CDVViewController** components.

* The plugin can programmatically retrieve **user-agent** from the WebView instance.


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
  

## MABS Version 5.2

<div class="info">

**First release:** 2019-12-26 13:30:00 UTC<br/>
**Last update:** 2021-09-29 14:00:00 UTC.
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

### Known Issue

* The issue with the screen flickering on iPhones running iOS 12, identified in MABS 4.0, when a user selects an input field in a screen with many inputs - occurs in MABS 5 as well, due to the same stack. The flickering happens when the viewport meta tag called “viewport-fit” is set to “cover”. [Here are the instructions on how to fix the issue](#known-issue-in-mabs-4).


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

* The issue with the screen flickering on iPhones running iOS 12, identified in MABS 4.0, when a user selects an input field in a screen with many inputs - occurs in MABS 5 as well, due to the same stack. The flickering happens when the viewport meta tag called “viewport-fit” is set to “cover”. [Here are the instructions on how to fix the issue](#known-issue-in-mabs-4).


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

* The issue with the screen flickering on iPhones running iOS 12, identified in MABS 4.0, when a user selects an input field in a screen with many inputs - occurs in MABS 5 as well, due to the same stack. The flickering happens when the viewport meta tag called “viewport-fit” is set to “cover”. [Here are the instructions on how to fix the issue](#known-issue-in-mabs-4).


## MABS Version 4.2

<div class="info">

**First release:** 2019-04-08 14:00:00 UTC<br/>
**Last update:** 2019-08-21 19:00:00 UTC.
</div>

### New in this version 

* Updated SQLite to version 3.26.0 to fix security issues and improve performance. Learn more [about the changes in SQLite](http://www.sqlite.org/changes.html). (RNMT-2682)

### Bug fixing 

* [2019-04-08 14:00:00 UTC] Fixed an issue where iOS application builds failed when using plugins that require a deployment target higher than iOS 8.0. (RNMT-2741)
* [2019-04-22 16:00:00 UTC] Fixed a missing configuration so that iOS applications will no longer be rejected by the App Store. (RNMT-2763)
* [2019-05-06 10:00:00 UTC] Fixed an issue that causes iOS app crashes when a new application version is available. (RNMT-2802)
* [2019-08-21 19:00:00 UTC] Fixed an issue with images failing to load with SSL Pinning plug-in. (RNMT-3176)
* [2019-08-21 19:00:00 UTC] Improved detection of the build errors, so the iOS application builds no longer fail due to CocoaPods repository update errors. (RNMT-3073)


## MABS Version 4.1

<div class="info">

**First release:** 2019-03-20 14:00:00 UTC<br/>
**Last update:** 2019-04-08 14:00:00 UTC.
</div>

### New in this version

* Android apps now support reverse proxy with NGINX and HTTP/2. To support HTTP/2 in Android 4.x devices, your platform server's SSL configuration must support one of these cipher suites:

    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA

    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA

    TLS_RSA_WITH_AES_128_CBC_SHA

    TLS_RSA_WITH_AES_256_CBC_SHA

    SSL_RSA_WITH_3DES_EDE_CBC_SHA

    (RNMT-2404).

* Mobile error logs now include the application version code and version name for easier troubleshooting. (RNMT-2640).
* Android support libraries are normalized in the version 26.1.0. (RNMT-2025).

### Bug fixing

* [2019-03-20 14:00:00 UTC] Fixed an issue that incorrectly encoded spaces in application resource names in iOS. (RNMT-2552)
* [2019-03-20 14:00:00 UTC] Fixed an issue where log dates were generating errors because they were considering the device locale. (RNMT-2641)
* [2019-04-08 14:00:00 UTC] Fixed an issue where iOS application builds failed when using plugins that require a deployment target higher than iOS 8.0. (RNMT-2741)
* [2019-04-22 16:00:00 UTC] Fixed a missing configuration so that iOS applications will no longer be rejected by the App Store. (RNMT-2763)
* [2019-05-06 10:00:00 UTC] Fixed an issue that causes iOS app crashes when a new application version is available (RNMT-2802)


## MABS Version 4.0

<div class="info">

**First release:** 2019-01-21 09:00:00 UTC<br/>
**Last update:** 2019-01-21 09:00:00 UTC.
</div>
 
### New in this version 

* Mobile Apps Build Service now uses the latest iOS SDK 12, so you will be able to continue submitting your iOS apps to the App Store, in line with the recent Apple announcement.
* Mobile Apps Build Service now uses Cordova iOS engine 4.5.5 for iOS apps. We highly recommend you revise your plugins for compatibility with this version.
* The definition of Splash Screens for iOS apps was replaced from Launch Images to Launch Storyboard Images. Learn more about [defining Splash Screens for iOS in MABS 4.0](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Use_Custom_Splash_Screens#for-ios).
* iOS apps now support iPhone Xr/Xs/Xs Max and iPad Pro.

### Bug fixing 

* [2019-02-27 15:00:00 UTC] Improved handling of UI glitch due to the injection of the "viewport-fit" meta tag. You can now disable the injection of the meta tag for iOS 12 devices and change the background color of the app at runtime. (RNMT-2628)

#### Known issue in MABS 4
When a user selects an input field in a mobile app screen with many inputs, the screen flickers. This occurs in iPhones running iOS 12 when the viewport meta tag called “viewport-fit” is set to “cover”. This “viewport-fit” value is used by the WebView to fill the entire screen. 

To fix this issue, add the preference “DisableViewportFitForiOS12” to the [Extensibility Configurations property](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App) and set it to “true”. This will disable the “viewport-fit” meta tag for all iPhone devices running iOS 12.

```
{
    "preferences": {
        "ios": [{
            "name": "DisableViewportFitForiOS12",
            "value": "true"
        }]
    }
}
```

However this causes the app to stop using the entire screen, and an empty bottom bar appears over the “home” button area in iPhone X devices. Check out the [Support KB article on styling the Status Bar and setting the WebView background color](https://success.outsystems.com/Support/Troubleshooting/Application_runtime/Further_Recommendations_on_the_MABS_4.0_Viewport-Fit_Issue_in_iOS_12_Phones). 

## MABS Version 3.3

<div class="info">

**First release:** 2018-08-22 14:00:00 UTC<br/>
**Last update:** 2020-08-25 12:00:00 UTC.
</div>

### New in this version 

* Android apps are now able to support servers with certificates from a private CA. (RNMT-1888)

### Bug fixing 

* [2018-12-19 18:00:00 UTC] Fixed iOS crash when network state changes. (RNMT-2284)
* [2018-12-19 18:00:00 UTC] Fixed Java 6/7/8 concurrent map compatibility. (RNMT-2291)
* [2018-08-22 14:00:00 UTC] Fixed an issue that causes app crashes on startup whenever the app is unable to connect to the server. (RNMT-1890)
* [2019-08-21 19:00:00 UTC] Fixed an issue with images failing to load with SSL Pinning plug-in. (RNMT-3176)
* [2019-08-21 19:00:00 UTC] Improved detection of the build errors, so the iOS application builds no longer fail due to CocoaPods repository update errors. (RNMT-3073)
* [2020-08-25 12:00:00 UTC] The build logs in Service Center now have more details to help you troubleshoot faster when an app fails to build.
 

## Older releases
Release notes for older MABS versions are available at [Mobile Apps Build Service (older versions)](older-releases.md).
