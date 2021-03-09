# Mobile Apps Build Service with updated stack starting on Feb 4

Starting March 2019, Apple will require that all mobile apps published to the App Store [are built using iOS 12 SDK](https://developer.apple.com/news/?id=09122018c).

On February 4 OutSystems will release a new MABS (Mobile Apps Build Service) version that uses the latest Cordova engine version supporting iOS 12 SDK. With this version, you can use the latest mobile capabilities and features in your OutSystems mobile apps, but it will not support iOS 8 and 9. However, after installing a Platform Server update, Service Center will allow you to select either this new MABS version or the previous version, for each mobile operating system in each mobile app. 

By default, iOS mobile apps will be built with this new MABS version, meaning that from this date, mobile apps will be compatible with the upcoming App Store publishing requirements. After March 2019, if you must keep support for iOS 8 or 9, you will be able to build your mobile apps using the previous MABS version, but you will not be able to publish them to the App Store.

The following table summarizes the main changes regarding the support for a new iOS stack in the new MABS version:

<table>
<tr>
<th></th>
<th style="text-align: center">MABS 3.x</th>
<th style="text-align: center">MABS 4.x<br/>(default from Feb 4 onwards)</th>
</tr>
<tr>
<th>Target iOS SDK</th>
<td style="text-align: center">iOS SDK 11</td>
<td style="text-align: center">iOS SDK 12</td>
</tr>
<tr>
<th>Supported iOS Versions</th>
<td style="text-align: center">8 to 12</td>
<td style="text-align: center">10 to 12</td>
</tr>
</table>

The Android stack will not change in this new version.

The OutSystems update required for selecting a MABS version will be available for both OutSystems 10 and 11 individually according to your infrastructure type:

* For **on-premises customers**, Platform Server and LifeTime binary packages will be available on January 15.  

* **Cloud customers** can request updates from January 2, to be scheduled from January 15 onwards.

![](images/mabs-versioning-timeline.png?width=950)

## Using the latest mobile capabilities on your mobile apps

If you wish to have the latest available features of mobile operating systems on your mobile apps you will benefit from using the new MABS version as early as possible; this will allow you to prepare your apps for the new version in time for the new App Store requirements. This preparation might consist of updating the versions of plugins your mobile apps are using (both supported by OutSystems and third-party) and testing your mobile apps built using the new iOS 12 SDK. If you encounter any issues, you will be able to address them until March 2019.

We recommend that you get ready for the new MABS version as early as January 21. To do so, update your OutSystems installation and select the Beta version of MABS to build your mobile apps using the new stack. All customers with updated Platform Server installations will be able to select the Beta version of MABS from January 21.

## Keeping mobile app support for the iOS 8 and 9 versions

It’s recommended to always use the latest MABS version. However, if you must continue supporting iOS 8 and 9 and you do not publish your mobile apps to the App Store, you must keep building your mobile apps using the old stack after February 4. To do so, update your Platform Server installation, which will allow you to select the MABS version that uses the older iOS stack to generate mobile apps. Note that, from March 2019, mobile apps built with this older stack cannot be published to the App Store.

## Impacts of not upgrading Platform Server

If you do not upgrade Platform Server to the new version with MABS versioning support you **will not have full control** of your mobile app lifecycle from Development to Production.

As soon as a new MABS version is released by OutSystems, the (non-upgraded) OutSystems platform will start making mobile app package generation requests to the **new MABS version**, regardless of where that request is being made in the application lifecycle: Development, Pre-Production or even Production. This means that you might develop and test a mobile app generated with a given MABS version and have a package generated in Production with a newer version of MABS, **which might cause build or runtime errors**.

If you do not upgrade, the tagged versions of your applications will not carry  information stating the MABS version that was used to build the app to the next environments in the infrastructure (the "MABS Version" information will be empty). **This puts your development lifecycle at risk** if there's a new version of MABS released by OutSystems between the package generation in Development and in Production.

Check the timeline below for an example of what might happen in an environment with a **non-upgraded** Platform Server:

![](<images/timeline-new-mabs-no-upgrade.png>)

As soon as MABS 4.0 is released, all mobile app package generation requests will use this new version, and this happened precisely when generating the package in Production.

### New behavior in upgraded environments

The new behavior when you select the option to always use the **latest** MABS version in Development is the following:

![](<images/mabs-use-latest-new-release.png>)

In this case, you are still getting the benefits of having a recent MABS version, but you are in full control of that change. You will be able to develop your mobile app with the latest MABS version in Development and keep it for PP and PROD. The MABS version used in Development will be the latest MABS version available after you tag your mobile app and this version information will be propagated to PP and PROD.

The new behavior when you select a **specific version** of MABS for a mobile app in Development is the following:

![](<images/mabs-use-specific-new-release.png>)

Regardless of the option you select in the MABS version setting in the new Platform Server release, you can be assured that **the MABS version used to build your mobile app package in Development is the same that will be used to build it** in every environment you deploy your mobile app.

For a full understanding of the impacts of these new options check [Understanding MABS Versions](<https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Mobile_Apps_Build_Service#understanding-mabs-versions>).
