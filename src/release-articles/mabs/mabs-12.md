---
summary: MABS 12 introduces Capacitor support, iOS 26 and Android API 36 SDKs, breaking changes, and plugin requirements for the OutSystems platform.
guid: 26d0470e-56c4-4e62-aa69-7170e8bfc180
locale: en-us
app_type: mobile apps
platform-version: o11, odc
isautopublish: true
audience:
  - Developer
  - Tech lead
coverage-type:
  - remember
  - understand
tags:
  - Android
  - Capacitor
  - Cordova
  - Forge
  - iOS
  - Mobile app
  - Plugins
outsystems-tools:
  - forge
  - odc studio
  - odc portal
---
# MABS 12 release notes

<div class="info" markdown="1">

For information about mobile stack details for each available MABS version, refer to [Mobile Apps Build Service Versions](mabs-versions.md).

For detailed information about common issues and solutions, refer to [Troubleshooting the Mobile Apps Generation](../../troubleshooting/application-development/troubleshoot-mobile-apps-generation.md).

</div>

OutSystems is excited to announce the release of [MABS 12](https://www.outsystems.com/tk/redirect?g=6b8e1729-3b16-4945-bf72-c22628e71421). This version helps you stay ahead of the latest mobile requirements. It also allows you to try the next-generation mobile runtime, **Capacitor**, for enhanced performance and flexibility. In addition, MABS 12 supports the latest SDKs from iOS and Android to meet the store submission compliance needs for 2026.

<div class="warning" markdown="1">

OutSystems recommends updating all supported plugins to the latest version available on the Forge. For more details, refer to [System Requirements](#system-requirements).

</div>

## MABS 12.1 { #mabs-version-12-1 }

<div class="info" markdown="1">

**First release:** 2026-05-26 10:30:00 UTC<br />

</div>

### What's new

MABS 12.1 release introduces the following new features and enhancements:

* Support for Swift Package Manager (SPM) in OutSystems Developer Cloud (ODC). For more details, refer to [`spmPreview`](https://www.outsystems.com/tk/redirect?g=fc8b0661-525c-4f75-8217-4d9aec2cd312#spmPreview) in  [App extensibility configuration JSON schema](https://www.outsystems.com/tk/redirect?g=fc8b0661-525c-4f75-8217-4d9aec2cd312).
* A true native splash screen now replaces the web-rendered approach for Capacitor apps, eliminating startup blinks on both iOS and Android. For more details, refer to [Customize splash screen](https://www.outsystems.com/tk/redirect?g=b7c4e8f2-1a3d-4e5f-9b6c-8d7e2f1a0b9c)
* Added support for Xcode 26.3

For additonal details, refer to [MABS 12.1 release notes](../../release-notes/mabs/12/12.1/12.1.md)

## System requirements

The table below contains a list of plugins and their supported versions for **MABS 12.1**. For more details, click the plugin name on the Forge.

| Plugin | Required minimum version for ODC |
| --- | --- |
| [Analytics (Firebase)](https://www.outsystems.com/forge/component-versions/10704) | 1.7.0 or later |
| [Cloud Messaging (Firebase)](https://www.outsystems.com/forge/component-versions/12174) | 3.3.0 or later |
| [Crash Reporting (Firebase)](https://www.outsystems.com/forge/component-versions/10705) | 1.5.0 or later |
| [OneSignal](https://www.outsystems.com/forge/component-versions/2119) | 1.2.0 or later |
| [Payments](https://www.outsystems.com/forge/component-versions/13678) | 1.2.0 or later |
| [Performance Monitoring (Firebase)](https://www.outsystems.com/forge/component-versions/10706) | 1.4.0 or later |

## Changes

Here's the list of changes that apply to MABS 12.1 for building Capacitor apps.

* [Splash screens](https://www.outsystems.com/tk/redirect?g=b7c4e8f2-1a3d-4e5f-9b6c-8d7e2f1a0b9c) are now driven by a new OutSystems implementation that replaces the @capacitor/splash-screen plugin, providing a refreshed UX and an expanded set of configuration options in the IDE.
* [Splash screen settings](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/configure_mobile_apps/) are now configured in the IDE rather than through extensibility configurations. The app settings defined in the IDE always take precedence over any values defined in the extensibility. This affects appConfigurations.backgroundColor and buildConfigurations.splashscreens.*.logo.
* The splash screen lifecycle is now controlled by the app runtime. As a consequence, the `autoHide` and `duration` entries under `appConfigurations` no longer have any effect.
* The branding image must be a 1024×1024 file, with PNG recommended. Other sizes are rejected at build time, and some formats may be as well.
* The full branding image is now used as the splash logo, instead of only the inner 2/3 of the canvas dictated by the Android convention. As a result, the app icon is no longer downscaled to fit the smaller circular area.
* On iOS, the branding image is no longer cropped to a circle. On Android, the image continues to be circle-masked, in line with the platform's splash screen guidelines.
* [`spmPreview`](https://www.outsystems.com/tk/redirect?g=fc8b0661-525c-4f75-8217-4d9aec2cd312#spmPreview) boolean is available under `buildConfigurations` in app extensibility to enable iOS builds with Swift Package Manager.

Here's the list of changes that apply to all other mobile apps, meaning anything that isn't a MABS 12.1 Capacitor app: MABS 11 Cordova, MABS 12.0 Cordova or Capacitor, and MABS 12.1 Cordova.

* Since the splash screen lifecycle is now controlled by the app runtime.The **Splash screen type** setting applies to every mobile app, regardless of mobile framework or MABS version. The **Native** splash screen option only produces a true native splash screen when building a Capacitor app with MABS 12.1 or later. In all other configurations, including older MABS versions and Cordova-based apps, selecting **Native** displays a web-based splash screen styled to visually provide a native experience. The remaining splash screen settings, however, still apply and control the appearance of that web-based screen.

## Known issues

Here's the list of known issues:

* Building a Capacitor app with MABS 12.1 and with the `spmPreview` extensibility configuration set to `true` with Cocoapods-only Cordova plugins results in a generic [OS-MABS-GEN-5000 error](../../error/mabs/mabs-gen-50000.md). Review the build logs to get additional information on plugin incompatibility.

## MABS 12.0 { #mabs-version-12-0 }

<div class="info" markdown="1">

**First release:** 2025-10-15 10:30:00 UTC<br />
**Last update:** 2025-12-15 10:30:00 UTC

</div>

### What's new

MABS 12.0 comes packed with new features and enhancements.

* Introduction of Capacitor, next generation hybrid mobile framework offering great performance and flexibility
* Support for the iOS 26 SDKs and Android API level 36, aligning with the upcoming Apple and Google app store requirements for 2026
* Introduction of modern concepts, such as [build actions](https://www.outsystems.com/tk/redirect?g=35892a80-96be-43bf-a89f-8d535b5b6f09) and [universal extensibility](https://www.outsystems.com/tk/redirect?g=941e56cf-aacf-43bf-9d1c-f131565036e6), giving you more control over building your Capacitor apps.
* Access to a highly active Capacitor developer community with a growing library of [plugins](https://capacitorjs.com/docs/plugins) to use
* Ability to customize the status bar for Android on the Mobile Tab - Requires ODC Studio version 1.5.28-8307 or later
* Auto-complete and syntactical validation for preferences and values when using universal extensibility schema. Requires ODC Studio version 1.5.28-8307 or later

For additonal details please refer to: [MABS 12 release notes](../../release-notes/mabs/12/12.0/12.0.md)

## System requirements

Plugin requirements for **MABS 12**. For more details, click the plugin name on the Forge.

|Plugin|Required minimum version for O11|Required minimum version for ODC|
|---|---|---|
|[Analytics (Firebase)](https://www.outsystems.com/forge/component-versions/10704)|-|1.3.0 or later|
|[Barcode](https://www.outsystems.com/forge/component-versions/1403)|5.5.7 or later|1.3.0 or later|
|[Camera](https://www.outsystems.com/forge/component-versions/1390)|7.6.4 or later|1.3.3 or later|
|[Card IO](https://www.outsystems.com/forge/component-versions/1438)|3.2.3 or later|-|
|[Calendar](https://www.outsystems.com/forge/component-versions/1566)|3.1.6 or later|1.0.6 or later|
|[Ciphered Local Storage](https://www.outsystems.com/forge/component-versions/1500)|3.2.6 or later|1.1.4 or later|
|[Contacts](https://www.outsystems.com/forge/component-versions/1394)|-|1.0.3 or later|
|[Cloud Messaging (Firebase)](https://www.outsystems.com/forge/component-versions/12174)|4.4.2 or later|3.0.1 or later|
|[Crash Reporting (Firebase)](https://www.outsystems.com/forge/component-versions/10705)|-|1.2.0 or later|
|[File](https://www.outsystems.com/forge/component-versions/1633)|3.0.7 or later|2.0.0 or later|
|[File Transfer](https://www.outsystems.com/forge/component-versions/1409)|-|2.0.0 or later|
|[File Viewer](https://www.outsystems.com/forge/component-versions/1606)|2.0.10 or later|2.0.0 or later|
|[Health & Fitness](https://www.outsystems.com/forge/component-versions/11715)|2.2.1 or later|1.4.2 or later|
|[Key Store](https://www.outsystems.com/forge/component-versions/1550)|2.4.3 or later|1.2.5 or later|
|[InAppBrowser](https://www.outsystems.com/forge/component-versions/1558)|-|2.2.0 or later|
|[Local Notifications](https://www.outsystems.com/forge/component-overview/1541/local-notifications-plugin)|-|1.0.5 or later|
|[Location](https://www.outsystems.com/forge/component-overview/1395/location-plugin)|-|2.0.1 or later|
|[OneSignal](https://www.outsystems.com/forge/component-versions/2119)|-|1.1.9 or later|
|[Payments](https://www.outsystems.com/forge/component-versions/13678)|1.2.5 or later|1.1.12 or later|
|[Performance Monitoring (Firebase)](https://www.outsystems.com/forge/component-versions/10706)|-|1.2.0 or later|
|[SSL Pinning](https://www.outsystems.com/forge/component-versions/1873)|-|1.2.0 or later|
|[Touch ID](https://www.outsystems.com/forge/component-versions/1431)|-|1.2.0 or later|
|[OutSystems AppShield](https://www.outsystems.com/forge/component-overview/9379/outsystems-appshield-o11)|1.15.0 or later|1.0.0 or later|

The table below contains the list of plugins and their supported versions. It is important to note that it is recommended to always use the latest version available of a plugin.

|Plugin|Supported minimum version for O11|Supported minimum version for ODC|
|---|---|---|
|[Analytics (Firebase)](https://www.outsystems.com/forge/component-versions/10704)|2.2.2 or later|1.3.0 or later|
|[Contacts](https://www.outsystems.com/forge/component-versions/1394)|4.0.6 or later|1.0.3 or later|
|[Crash Reporting (Firebase)](https://www.outsystems.com/forge/component-versions/10705)|2.1.1 or later|1.2.0 or later|
|[File Transfer](https://www.outsystems.com/forge/component-versions/1409)|2.1.7 or later|2.0.0 or later|
|[Haptics](https://www.outsystems.com/forge/component-overview/22851/haptics-plugin-odc)|-|1.2.0 or later|
|[Keyboard](https://www.outsystems.com/forge/component-overview/22852/keyboard-plugin-odc)|-|1.2.2 or later|
|[InAppBrowser](https://www.outsystems.com/forge/component-versions/1558)|2.4.10 or later|2.2.0 or later|
|[Local Notifications](https://www.outsystems.com/forge/component-overview/1541/local-notifications-plugin)|7.2.1 or later|1.0.5 or later|
|[Location](https://www.outsystems.com/forge/component-overview/1395/location-plugin)|5.2.2 or later|2.0.1 or later|
|[OneSignal](https://www.outsystems.com/forge/component-versions/2119)|3.7.5 or later|1.1.9 or later|
|[Performance Monitoring (Firebase)](https://www.outsystems.com/forge/component-versions/10706)|2.1.1 or later|1.2.0 or later|
|[Social Login Mobile](https://www.outsystems.com/forge/component-versions/7895)|4.2.2 or later|-|
|[SSL Pinning](https://www.outsystems.com/forge/component-versions/1873)|7.0.1 or later|1.2.0 or later|
|[Touch ID](https://www.outsystems.com/forge/component-versions/1431)|3.3.9 or later|1.2.0 or later|

## Breaking changes

Here's the list of breaking changes that apply to MABS 12 for building **Capacitor** apps.

* WebView version 102 or higher is required for mobile applications to run on Android devices. Ensure your WebView is up to date by visiting the Play Store.
* The Inspector is no longer available for iOS debug builds. If you need to inspect the network requests you can set one of the many interactive HTTPS proxies available.
* The `DeepLinksHandlerType` configuration no longer has any effect. Deeplinks are only customizable via the `window.handleOpenURL` function, which must be defined in a script that is loaded by the application module. If not defined, the application navigates to the deeplink URL by default.

Here's a list of breaking changes that apply to MABS 12 for building **Cordova** apps.

* On Android apps, the WebView no longer takes up the entire screen out of the box and instead respects the system bars, such as the status bar and navigation bar.
    * The status bar background color defaults to the app's primary color. You can customize it using `StatusBarBackgroundColor`.
* OutSystems [cordova-plugin-statusbar](https://github.com/OutSystems/cordova-plugin-statusbar/) is no longer available in Android and iOS apps.
    * The preferences `StatusBarOverlaysWebView`, `StatusBarStyle`, and `StatusBarDefaultScrollToTop` are no longer supported and have no effect.
* CSS custom property `--status-bar-height` is no longer available in Android apps.
* Android Cordova template has some file names changed, and it may impact customer hooks:
    * strings.xml file has been renamed to cdv_strings.xml
    * colors.xml file has been renamed to cdv_colors.xml
    * themes.xml file has been renamed to cdv_themes.xml

## Known issues

Here's the list of known issues:

* Updates over the air fail for apps that use build actions YAML file provided as OutSystems app resources **(Capacitor only)**.
* Back navigation with back button or gesture navigation doesn't affect in-app navigation when running in Android 16 **(Capacitor only)**.
