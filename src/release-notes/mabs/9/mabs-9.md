---
summary: MABS 9 release notes
guid: 344d5857-80d1-4207-87fc-cc5772c058ef
locale: en-us
app_type: mobile apps
---

# MABS 9 Release notes

<div class="info">

Check the mobile stack details for each available MABS version in [Mobile Apps Build Service Versions](../mabs-versions.md).
</div>

<div class="info">

For common issues and solutions check also [Troubleshooting the Mobile Apps Generation](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation).
</div>

MABS 9 is an important milestone for all mobile developers who publish on App Store and Play Store. MABS 9 uses iOS 16, and Android 13 with the API level 33. The stack lets you continue submitting your Android and iOS apps to the stores while taking advantage of the new features that new iOS and Android bring.

<div class="warning">

It's recommended to update all supported plugins to the latest version available on the Forge. If you're upgrading from MABS 8, all plugins should already be compliant. From MABS 7 or previous, it's **MANDATORY** to upgrade to the latest version. For more details, please check the [System Requirements](#system-requirements) below.

</div>

## MABS 9 release

* [MABS 9.0 release notes](9.0/9.0.md)

## System Requirements

Plugin requirements for **MABS 9**. For more details, please check the Forge by clicking on the plugin name

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

## Breaking Changes

Here is the list of changes made to MABS 9 that may affect the building of your apps.

<li>Deeplinks now use screen navigations instead of reloading the app. The behaviour can be configured via the <a href="https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Customize_Deeplink_Behavior">DeepLinksHandlerType</a> preference.</li>
<li>Default value of the <a href="https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema">FilterTouchesWhenObscured</a> preference is now "true".</li>
<li>Default value of the <a href="https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema">RemoveUserCertificates</a> preference is now "true".</li>
<li>MABS 9 uses Node 16 and NPM 8, which can affect the behaviour of plugin hooks.</li>
<li>Versions of Android dependencies OkHttp3 and GSON are now updated. OkHttp3 to version 4.9.3. GSON to version 2.10.</li>
<li>CocoaLumberjack dependency is no longer present in iOS applications.</li>
<li>Obsolete navigator.network.connection clobber is no longer available.</li>

-----

## Known Limitations

Here is the list of side effects from changes made to MABS 9 that might affect the building of your apps.

<li>Android applications now use the Android SplashScreen API. This internally uses a theme to configure the splash screen, that can be found at target res/values/themes.xml. This file cannot be replaced. In case it is modified, the original theme must be kept.</li>

-----
