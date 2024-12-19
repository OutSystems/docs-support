---
tags:
summary:
locale: en-us
guid: CBEDB43A-1C6A-4EB2-A0C5-1FBC5DD2A0BC
app_type: mobile apps
platform-version: o11
---

# MABS older versions

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


<h2>2018-07-31</h2>

<div class="info">
<p>Released on 2018-07-31 10:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Mobile Apps Build Service Cordova stack for both iOS and Android was updated to CLI version 7.1.0; this means we highly recommend you revise your plugins to compatible, otherwise app generation may fail;</li>
<li>Android applications will be built targeting API level 26, so you will be able to continue deploying your apps on the Play Store, inline with recent Google's announcement. (RNMT-1047).</li>
</ul>

<h2>2018-07-11</h2>

<div class="info">
<p>Released on 2018-07-11 15:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Due to privacy constraints, generated apps no longer contain the cordova-plugin-sim by default (RNMT-1784)</li>
</ul>

<h2>2018-07-04</h2>

<div class="info">
<p>Released on 2018-07-04 15:00:00 UTC</p>
</div>

<h3>Bug Fixing</h3>

<ul>
<li>The built-in deeplinks plugin will now search for deep links on Intent extras (RNMT-1783)</li>
</ul>

<h2>2018-06-21</h2>

<div class="info">
<p>Released on 2018-06-21 14:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Upgraded play-services-gcm and play-services-location dependencies versions (RNMT-1751)</li>
</ul>

<h2>2018-05-30</h2>

<div class="info">
<p>Released on 2018-05-30 15:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Updated cordova-outsystems-logger plugin used by the native application shell to the latest version. (RNMT-1622)</li>
</ul>

<h2>2018-03-28</h2>

<div class="info">
<p>Released on 2018-03-28 10:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>OutSystems has got you covered. We have already taken some steps in preparation for this change with a new Silk UI Mobile version. From April onward iOS applications will be built using the latest iOS SDK 11, so you will be able to continue deploying your apps on Apples App Store, inline with recent Apple announcement. (RNMT-1311)</li>
</ul>

<h2>2018-01-29</h2>

<div class="info">
<p>Released on 2018-01-29, 2018</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Added a new native logging mechanism to OutSystems mobile apps allowing full visibility of any errors occurring on end-users devices. (RNMT-1287)</li>
</ul>

<h2>2017-11-08</h2>

<div class="info">
<p>Released on 2017-11-08 14:01:51 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Updated the cordova-plugin-sim used by the native application shell to the latest version. (RPD-2851)</li>
</ul>

<h2>2017-10-30</h2>

<div class="info">
<p>Released on 2017-10-30 12:31:02 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Added more detailed error messages to improve troubleshooting during the app build process. (RPD-2291)</li>
</ul>

<h2>2017-10-16</h2>

<div class="info">
<p>Released on 2017-10-16 15:00:00 UTC</p>
</div>

<h3>Bug Fixing</h3>

<ul>
<li>Fixed mobile app crashes when using an upload widget of type video in iOS. (RPD-2544)</li>
</ul>

<h2>2017-09-20</h2>

<div class="info">
<p>Released on 2017-09-20 16:00:00 UTC</p>
</div>

<h3>Bug Fixing</h3>

<ul>
<li>Fixed an issue that blocked mobile apps in the white screen. (RPD-2586)</li>
</ul>

<h2>2017-08-30</h2>

<div class="info">
<p>Released on 2017-08-30 15:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Added support for CocoaPods in iOS. (RNMT-470)</li>
</ul>

<h2>2017-08-16</h2>

<div class="info">
<p>Released on 2017-08-16 15:00:00 UTC</p>
</div>

<h3>Bug Fixing</h3>

<ul>
<li>Fixed a Deep Link issue for iOS that was showing blue or white screens. (RPD-2410)</li>
<li>Fixed an SSL Pinning Plugin crash on Android 4.4.2. (RPD-2521)</li>
<li>Fixed an issue with the Android soft keyboard that was open and did not allow scrolling. (RPD-2534)</li>
</ul>

<h2>2017-07-26</h2>

<div class="info">
<p>Released on 2017-07-26 15:00:00 UTC</p>
</div>

<h3>New in Mobile Apps Build Service</h3>

<ul>
<li>Improved the cache to be more resilient to errors and network issues. (RNMT-795)</li>
</ul>
