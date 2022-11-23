# MABS 9 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](mabs-versions.md).
</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).
</div>

## MABS Version 9.0 (Beta)

<div class="info">

**First release:** 2022-11-23 12:00:00 UTC<br/>
**Last update:** 2022-11-23 12:00:00 UTC
</div>

MABS 9.0 is an important milestone for all mobile developers who publish on App Store and Play Store. MABS 9 uses **iOS 16**, and **Android 13** with the **API level 33**. The stack lets you continue submitting your Android and iOS apps to the stores while taking advantage of the new features that new iOS and Android bring.

<div class="warning">

It's recommended to update all supported plugins to the latest version available on the Forge. If you're upgrading from MABS 8.0, all plugins should already be compliant. From MABS 7 or previous, it's **MANDATORY** to upgrade to the latest version. For more details, please check the [System Requirements](#system-requirements) below.

</div>

### What's New

* Android
    * Targets Android SDK 33
    * Android Cordova Engine updated to 11.0.0
    * Gradle version increased to 7.5.1
* iOS
    * Xcode 14.1
* General
    * Cordova CLI 11

* All OutSystems applications are now using SQLite 3.32.3. (RPM-2258)
* It is now possible to obtain the application package identifier using the js method `OSApplicationInfo.getAppPackageIdentifier`. (RNMT-5784)
* Deeplinks now use screen navigations instead of reloading the app. The behavior can be configured via the [DeepLinksHandlerType preference](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Customize_Deeplink_Behavior). (RPM-420, RPM-576)
* You can now authenticate OutSystems mobile apps via SSO. (RNMT-5810)
* On Android, the Splash Screen API is now supported. For more information, please check the [Cordova documentation](https://cordova.apache.org/docs/en/latest/core/features/splashscreen/index.html). (RNMT-5730)
* Kotlin version is now 1.6.20 by default. This is the minimum supported version. It can overriden via the `GradlePluginKotlinVersion` extensibility configuration [inherited from Cordova](https://cordova.apache.org/announcements/2020/06/29/cordova-android-9.0.0.html).
* The obsolete `navigator.network.connection` clobber is no longer available. (RNMT-5882)

### Bug Fixing

* [2022-11-23 12:00:00 UTC] HTTP plugin now synchronizes cookies when following redirects. (RNMT-5868)
### System Requirements

Plugin requirements for **MABS 9.0**. For more details, please check the Forge by clicking on the plugin name
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

-----

### Breaking Changes and Known Limitations

Here is the list of issues that may affect the building of your apps with MABS 9.0.

- None

-----
