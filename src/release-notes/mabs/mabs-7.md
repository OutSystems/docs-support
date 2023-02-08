---
summary:
locale: en-us
guid: 8D6C234D-4B36-424C-8A41-7813025ADF11
app_type: mobile apps
platform-version: o11
---

# MABS 7 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).
</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).
</div>

## MABS Version 7.2

<div class="info">

**First release:** 2021-09-01 15:40:00 UTC<br/>
**Last update:** 2022-09-21 09:00:00 UTC.
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
* [2022-05-19 13:00:00 UTC] Updated NPM version to overcome github changes related to the usage of the `git://` protocol. [More info here](https://github.blog/2021-09-01-improving-git-protocol-security-github/)
* [2022-09-21 09:00:00 UTC] Changed the minimum supported TLS version from 1.0 to 1.2. (RPM-2764)


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
