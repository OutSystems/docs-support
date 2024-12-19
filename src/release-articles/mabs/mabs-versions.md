---
summary: The article details the lifecycle and support policy for various versions of the Mobile Apps Build Service (MABS), including major and minor releases, deprecation schedules, and compatibility with Android and iOS versions.
guid: 61CB98BF-3C28-4590-9E19-0C1C7B7F0408
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# Mobile Apps Build Service Versions

<div class="info" markdown="1">

Applies only to **Mobile Apps**.

</div>

**Mobile Apps Build Service (MABS)** is an out-of-the-box **cloud service** designed to eliminate the complexities of managing a build process. To find out more about MABS, its versioning, and its lifecycle, refer to [MABS versioning and lifecycle](mabs-versioning-and-lifecycle.md).

These are the available MABS versions:

## Beta

See [Support provided for beta versions](mabs-beta-support.md) for details on OutSystems' policy regarding new mobile operating system support.

<div class="info" markdown="1">

## **Version 11.0** - [See Release Notes](../../release-notes/mabs/11/11.0/11.0.md)<br/>
Released as Beta on November 20th, 2024 <br/>

</div>

<div class="warning" markdown="1">

It's recommended to update all supported plugins to the latest version available on the Forge. For more details, please check the **[release notes](https://success.outsystems.com/Support/Release_Notes/Mobile_Apps_Build_Service_Versions/MABS_11_Release_notes#mabs-version-11.0)**.

</div>

This version can run your apps on:

<small>![Icon representing the Android operating system.](images/android-icon.png "Android Icon") Android 10 to 15</small>

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
            <td style="width:231px;">Build Tools 35.0.0<br/>
            Gradle 8.5<br/>
            Android Gradle Plugin 8.3<br/>
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


## Supported

You can get full support and bug fixes through OutSystems support requests mechanism.

<div class="info" markdown="1">

## **Version 10.0** - [See Release Notes](../../release-notes/mabs/10/10.0/10.0.md)<br/>
Released as Beta on October 26, 2023 <br/>
Released to GA on December 27, 2023 <br/>
Deprecation date to be announced

</div>

<div class="warning" markdown="1">

It's recommended to update all supported plugins to the latest version available on the Forge. For more details, please check the **[release notes](https://success.outsystems.com/Support/Release_Notes/Mobile_Apps_Build_Service_Versions/MABS_10_Release_notes#mabs-version-10.0)**.

</div>

This version can run your apps on:

<small>![Icon representing the Android operating system.](images/android-icon.png "Android Icon") Android 9 to 15</small>

<small>![Icon representing the iOS operating system.](images/iOS-icon.png "iOS Icon") iOS 14 to 18</small>

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
            <td style="width:231px;">14 (API Level 34)<br/></td>
            <td>17.2<br/></td>
        </tr>
        <tr>
            <td style="vertical-align:middle;width:156px;">Tools</td>
            <td style="width:231px;">Build Tools 34.0.0<br/>
            Gradle 8.5<br/>
            Android Gradle Plugin 8.2.0<br/>
            Kotlin 1.9.21<br/>
            Cordova CLI 12.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-android/tree/outsystems/12.0.x">Cordova Android 12.0</a></td>
            <td>Xcode 15.1<br/>
            CocoaPods 1.14.3<br/>
            Swift 5.9.2<br/>
            Cordova CLI 12.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-ios/tree/outsystems/7.0.x">Cordova iOS 7.0</a></td>
        </tr>
    </tbody>
</table>


## Deprecated

You can select this version in the configuration and create a mobile package using it, but you receive limited support. Limited support means that you receive advice and workarounds through support requests, but there are no bug fixes for the version.

<div class="warning" markdown="1">

## **Version 9.0** - [See Release Notes](../../release-notes/mabs/9/9.0/9.0.md)<br/>
Released on November 23, 2022<br/>
Deprecated on April 29, 2024
</div>

<div class="warning" markdown="1">

It's recommended to update all supported plugins to the latest version available on the Forge. If you upgrade from MABS 8, all plugins should already be compliant. From MABS 7 or previous, it's **MANDATORY** to upgrade to the latest version. For more details, please check the **[release notes](https://success.outsystems.com/Support/Release_Notes/Mobile_Apps_Build_Service_Versions/MABS_9_Release_notes#mabs-version-9.0)**.

</div>

This version can run your apps on:

<small>![Icon representing the Android operating system.](images/android-icon.png "Android Icon") Android 8 (9 for ODC) to 14</small>

<small>![Icon representing the iOS operating system.](images/iOS-icon.png "iOS Icon") iOS 13 to 17</small>

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
            <td style="width:231px;">14 (API Level 33)<br/></td>
            <td>16<br/></td>
        </tr>
        <tr>
            <td style="vertical-align:middle;width:156px;">Tools</td>
            <td style="width:231px;">Build Tools 33.0.0<br/>
            Gradle 7.5<br/>
            Android Gradle Plugin 7.3.0<br/>
            Kotlin 1.6.20 (Default) to 1.7.X<br/>
            Cordova CLI 11.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-android/tree/outsystems/11.0.x">Cordova Android 11.0</a></td>
            <td>Xcode 14.1<br/>
            Cocoa Pods 1.11.2<br/>
            Swift 5.7.1<br/>
            Cordova CLI 11.0.0<br/>
            <a href="https://github.com/OutSystems/cordova-ios/tree/outsystems/6.2.x">Cordova iOS 6.2</a></td>
        </tr>
    </tbody>
</table>

