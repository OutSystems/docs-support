---
summary: The article details the lifecycle and support policy for various versions of the Mobile Apps Build Service (MABS), including major and minor releases, deprecation schedules, and compatibility with Android and iOS versions.
guid: 61CB98BF-3C28-4590-9E19-0C1C7B7F0408
locale: en-us
app_type: mobile apps
platform-version: o11, odc
tags: mobile apps build service, mabs, versioning, android compatibility, ios compatibility
audience:
  - mobile developers
outsystems-tools:
  - forge
---
# Mobile apps build service versions

<div class="info" markdown="1">

Applies only to **Mobile apps**.

</div>

**Mobile Apps Build Service (MABS)** is an out-of-the-box **cloud service** designed to eliminate the complexities of managing a build process. To find out more about MABS, its versioning, and its lifecycle, refer to [MABS versioning and lifecycle](mabs-versioning-and-lifecycle.md).

These are the available MABS versions:

<!--
## Beta

See [Support provided for beta versions](mabs-beta-support.md) for details on the OutSystems policy regarding new mobile operating system support. -->

## Supported

You can get full support and bug fixes through OutSystems support requests mechanism.

<div class="info" markdown="1">

## **Version 12.0**

[See release notes](../../release-notes/mabs/12/12.0/12.0.md)<br/>

Released as Beta on October 15th, 2025 <br/>
Released to GA on December 15th, 2025 <br/>
Deprecation date to be announced <br/>
Obsolete date to be announced <br/>

</div>

<div class="warning" markdown="1">

It's recommended to update all supported plugins to the latest version available on the Forge. For more details, please check the **[release notes](https://success.outsystems.com/support/release_notes/mobile_apps_build_service_versions/mabs_12_release_notes/#mabs-version-12-0)**.

</div>

This version can run your apps on:

<small>![Icon representing the Android operating system.](images/android-icon.png "Android Icon") Android 9 to 16</small>

<small>![Icon representing the iOS operating system.](images/iOS-icon.png "iOS Icon") iOS 15 to 26</small>

**More details:**

<table style="width: 632px; table-layout: fixed">
    <tbody class="RegularLightText">
        <tr>
            <td style="width:156px;"></td>
            <td style="width:231px;">Android</td>
            <td>iOS</td>
        </tr>
        <tr>
            <td style="vertical-align:middle;width:156px;">Target SDK</td>
            <td style="width:231px;">16 (API Level 36)<br/></td>
            <td>26.0<br/></td>
        </tr>
        <tr>
            <td style="vertical-align:middle;width:156px;">Tools</td>
            <td style="width:231px;">Build Tools 35.0.0<br/>
            Gradle 8.14.3<br/>
            Android Gradle Plugin 8.7.2<br/>
            Kotlin 1.9.24<br/>
            Cordova CLI 12.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-android/tree/outsystems/13.0.x">Cordova Android 13.0</a></td>
            <td>Xcode 26.0<br/>
            CocoaPods 1.16.2<br/>
            Swift 6.2<br/>
            Cordova CLI 12.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-ios/tree/outsystems/7.1.x">Cordova iOS 7.1</a></td>
        </tr>
    </tbody>
</table>

<div class="info" markdown="1">

## **Version 11.2**

[See release notes](../../release-notes/mabs/11/11.2/11.2.md)<br/>

Released as Beta on October 15th, 2025 <br/>
Released to GA on October 30th, 2025 <br/>
Deprecation on April 15th, 2026 <br/>
Obsolete date to be announced <br/>

</div>

<div class="warning" markdown="1">

It's recommended to update all supported plugins to the latest version available on the Forge. For more details, please check the **[release notes](https://success.outsystems.com/support/release_notes/mobile_apps_build_service_versions/mabs_11_release_notes/#mabs-version-11-2)**.

</div>

This version can run your apps on:

<small>![Icon representing the Android operating system.](images/android-icon.png "Android Icon") Android 9 to 15</small>

<small>![Icon representing the iOS operating system.](images/iOS-icon.png "iOS Icon") iOS 15 to 18</small>

**More details:**

<table style="width: 632px; table-layout: fixed">
    <tbody class="RegularLightText">
        <tr>
            <td style="width:156px;"></td>
            <td style="width:231px;">Android</td>
            <td>iOS</td>
        </tr>
        <tr>
            <td style="vertical-align:middle;width:156px;">Target SDK</td>
            <td style="width:231px;">15 (API Level 35)<br/></td>
            <td>18.0<br/></td>
        </tr>
        <tr>
            <td style="vertical-align:middle;width:156px;">Tools</td>
            <td style="width:231px;">Build Tools 36.0.0<br/>
            Gradle 8.11.1<br/>
            Android Gradle Plugin 8.7.2<br/>
            Kotlin 1.9.24<br/>
            Cordova CLI 12.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-android/tree/outsystems/13.0.x">Cordova Android 13.0</a></td>
            <td>Xcode 16.0<br/>
            CocoaPods 1.15.2<br/>
            Swift 6.0<br/>
            Cordova CLI 12.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-ios/tree/outsystems/7.1.x">Cordova iOS 7.1</a></td>
        </tr>
    </tbody>
</table>

## Deprecated

<div class="info" markdown="1">

CUrrently, there are no deprecated MABS versions.

</div>

You can select a deprecated MABS version when creating a mobile package, but you will receive limited support. Limited support means that you receive advice and workarounds through support requests, but there are no bug fixes for the version.
