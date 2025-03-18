---
summary: MABS 10 release notes
guid: d7a23497-14cd-434f-8364-6f9949a02ff2
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# MABS 10 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).

</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).

</div>

MABS 10 is an important milestone for all mobile developers who publish on App Store and Play Store. MABS 10 targets iOS 17 and Android 14, letting you continue submitting your Android and iOS apps to the stores while taking advantage of the new features that new iOS and Android versions bring.

<div class="warning">

It's recommended to update all supported plugins to the latest version available on the Forge. For more details, please check the [System Requirements](#system-requirements) below.

</div>

## MABS 10 release

* [MABS 10.0 release notes](../../release-notes/mabs/10/10.0/10.0.md)

## System Requirements

Plugin requirements for **MABS 10**. For more details, please check the Forge by clicking on the plugin name.

|Plugin|Required minimum version for O11|Required minimum version for ODC|
|:---|---|---|
|[Camera](https://www.outsystems.com/forge/component-versions/1390)|7.5.0 or later|0.1.15 or later|
|[OneSignal](https://www.outsystems.com/forge/component-versions/2119)|3.6.0 or later|0.1.1 or later|
|[Location](https://www.outsystems.com/forge/component-overview/1395/location-plugin)|5.2.0 or later|1.0.1 or later|
|[Local Notifications](https://www.outsystems.com/forge/component-overview/1541/local-notifications-plugin)|7.2.0 or later|0.1.3 or later|
|[Barcode](https://www.outsystems.com/forge/component-overview/1403/barcode-plugin)|5.3.1 or later|0.1.9 or later|
|[Calendar](https://www.outsystems.com/forge/component-versions/1566)|3.1.5 or later|0.1.2 or later|
|[Social Login Mobile](https://www.outsystems.com/forge/component-versions/7895)|4.0.1 or later|-|

The table below contains the list of plugins and their supported versions. It is important to note that it is recommended to always use the latest version available of a plugin.

|Plugin|Supported minimum version for O11|Supported minimum version for ODC|
|:---|---|---|
|[SSL Pinning](https://www.outsystems.com/forge/component-versions/1873)|7.0.0 or later|0.1.0 or later|
|[InAppBrowser](https://www.outsystems.com/forge/component-versions/1558)|2.4.10 or later|0.1.2 or later|
|[Ciphered Local Storage](https://www.outsystems.com/forge/component-versions/1500)|3.2.2 or later|0.1.2 or later|
|[File](https://www.outsystems.com/forge/component-versions/1633)|3.0.5 or later|0.1.0 or later|
|[File Viewer](https://www.outsystems.com/forge/component-versions/1606)|2.0.8 or later|0.1.0 or later|
|[File Transfer](https://www.outsystems.com/forge/component-versions/1409)|2.1.5 or later|0.1.2 or later|
|[Touch ID](https://www.outsystems.com/forge/component-versions/1431)|3.3.8 or later|0.1.2 or later|
|[Key Store](https://www.outsystems.com/forge/component-versions/1550)|2.3.2 or later|0.1.2 or later|
|[Contacts](https://www.outsystems.com/forge/component-versions/1394)|4.0.6 or later|0.1.0 or later|
|[Card IO](https://www.outsystems.com/forge/component-versions/1438)|3.2.1 or later|-|
|[Analytics (Firebase)](https://www.outsystems.com/forge/component-versions/10704)|2.0.0 or later|0.1.0 or later|
|[Dynamic Links (Firebase)](https://www.outsystems.com/forge/component-versions/10988)|2.0.0 or later|0.1.0 or later|
|[Performance Monitoring (Firebase)](https://www.outsystems.com/forge/component-versions/10706)|2.0.0 or later|0.1.0 or later|
|[Crash Reporting (Firebase)](https://www.outsystems.com/forge/component-versions/10705)|2.0.0 or later|0.1.0 or later|
|[Cloud Messaging (Firebase)](https://www.outsystems.com/forge/component-versions/12174)|3.0.0 or later|0.1.1 or later|
|[Health and Fitness](https://www.outsystems.com/forge/component-versions/11715)|1.4.0 or later|0.1.4 or later|
|[Payments](https://www.outsystems.com/forge/component-versions/13678)|1.1.0 or later|0.1.2 or later|

-----

## Breaking Changes

Here is the list of changes made to MABS 10 that may affect the building of your apps.

* The legacy Android Support Libraries (`com.android.support`) are no longer supported. Builds containing these packages will fail until they are migrated to [their respective AndroidX counterpart](https://developer.android.com/jetpack/androidx/migrate/artifact-mappings). Owners of non-supported plugins using Android Support Libraries must migrate their plugins to work with MABS 10. (RNMT-6187)
* The `AndroidXEnabled` preference no longer takes any effect and can be removed from Extensibility Configurations, since usage of `AndroidX` packages is now mandatory. (RNMT-6187)
* Removed functionality that was specifically adding `aps-environments` to plist when present in the provisioning profile. This should be handled by each plugin making use of the `aps-environment` entitlement, and not generically by MABS since not all applications need this. (RNMT-5935)


-----
