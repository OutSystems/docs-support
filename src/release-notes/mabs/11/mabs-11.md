---
summary: MABS 11 release notes
guid: eea78c31-f3f9-4b0a-a843-4e9d9a80b434
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# MABS 11 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](../mabs-versions.md).

</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).

</div>

MABS 11 is an important milestone for all mobile developers who publish on App Store and Play Store. MABS 11 targets iOS 18 and Android 15, letting you continue submitting your Android and iOS apps to the stores while taking advantage of the new features that new iOS and Android versions bring.

<div class="warning">

It's recommended to update all supported plugins to the latest version available on the Forge. For more details, please check the [System Requirements](#system-requirements) below.

</div>

## MABS 11 release

* [MABS 11.0 release notes](11.0/11.0.md)

## System Requirements

Plugin requirements for **MABS 11**. For more details, please check the Forge by clicking on the plugin name.

|Plugin|Required minimum version for O11|Required minimum version for ODC|
|:---|---|---|
|[Barcode](https://www.outsystems.com/forge/component-versions/1403)|5.5.7 or later|1.2.7 or later|
|[Camera](https://www.outsystems.com/forge/component-versions/1390)|7.6.4 or later|1.1.4 or later|
|[Card IO](https://www.outsystems.com/forge/component-versions/1438)|3.2.3 or later|-|
|[Calendar](https://www.outsystems.com/forge/component-versions/1566)|3.1.6 or later|1.0.2 or later|
|[Ciphered Local Storage](https://www.outsystems.com/forge/component-versions/1500)|3.2.4 or later|1.0.2 or later|
|[File](https://www.outsystems.com/forge/component-versions/1633)|3.0.7 or later|1.0.3 or later|
|[File Viewer](https://www.outsystems.com/forge/component-versions/1606)|2.0.10 or later|1.0.2 or later|
|[Health & Fitness](https://www.outsystems.com/forge/component-versions/11715)|2.2.1 or later|1.2.1 or later|
|[InAppBrowser](https://www.outsystems.com/forge/component-versions/1558)|3.1.0 or later|2.1.0 or later|

The table below contains the list of plugins and their supported versions. It is important to note that it is recommended to always use the latest version available of a plugin.

|Plugin|Supported minimum version for O11|Supported minimum version for ODC|
|:---|---|---|
|[Contacts](https://www.outsystems.com/forge/component-versions/1394)|4.0.6 or later|1.0.1 or later|
|[File Transfer](https://www.outsystems.com/forge/component-versions/1409)|2.1.7 or later|1.0.2 or later|
|[Key Store](https://www.outsystems.com/forge/component-versions/1550)|2.4.1 or later|1.1.1 or later|
|[Location](https://www.outsystems.com/forge/component-overview/1395/location-plugin)|5.2.2 or later|1.1.2 or later|
|[Local Notifications](https://www.outsystems.com/forge/component-overview/1541/local-notifications-plugin)|7.2.1 or later|1.0.2 or later|
|[Analytics (Firebase)](https://www.outsystems.com/forge/component-versions/10704)|2.2.2 or later|1.2.1 or later|
|[Cloud Messaging (Firebase)](https://www.outsystems.com/forge/component-versions/12174)|4.4.0 or later|2.2.0 or later|
|[Crash Reporting (Firebase)](https://www.outsystems.com/forge/component-versions/10705)|2.1.1 or later|1.1.2 or later|
|[Dynamic Links (Firebase)](https://www.outsystems.com/forge/component-versions/10988)|2.1.1 or later|1.1.2 or later|
|[Performance Monitoring (Firebase)](https://www.outsystems.com/forge/component-versions/10706)|2.1.1 or later|1.1.2 or later|
|[Touch ID](https://www.outsystems.com/forge/component-versions/1431)|3.3.9 or later|1.1.1 or later|
|[OneSignal](https://www.outsystems.com/forge/component-versions/2119)|3.7.5 or later|1.1.1 or later|
|[SSL Pinning](https://www.outsystems.com/forge/component-versions/1873)|7.0.2 or later|1.0.2 or later|
|[Social Login Mobile](https://www.outsystems.com/forge/component-versions/7895)|4.2.2 or later|-|
|[Payments](https://www.outsystems.com/forge/component-versions/13678)|1.2.2 or later|1.1.2 or later|

-----

## Breaking Changes

Here is the list of changes made to MABS 11 that may affect the building of your apps.

* Changed the `AddUploadWidgetPermissions` property default value from `true` to `false`. The Android permissions associated with the upload widget are no longer added out of the box.
* Changed the `StatusBarOverlaysWebView` property default value from `false` to `true`.
* Added the `StatusBarStyle` property default value as `default`.
----- 
