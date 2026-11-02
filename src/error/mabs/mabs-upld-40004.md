---
summary: OutSystems Developer Cloud (ODC) MABS error OS-MABS-UPLD-40004 requires an AAB build type and matching Google Play keystore.
tags:
  - Android
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
audience:
  - Developer
guid: 26e29b8f-fa91-4e7d-8eba-9fe2d79a895d
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40004

## Error message

`Invalid build type used for build uploaded to the Google Play Console. Create an app bundle build and try again.`

## Cause

Google Play Console requires that modern app releases use the `aab` file format. The android package build was not assigned the `Google Play (App Bundle)` build type during new build configuration so an `aab` file was not created.

## Impact

ODC can't upload this mobile package build to the Google Play Console.

## Recommended action

* Open the configurations for creating a new android package build.
* Configure the new build with a build type of `Google Play (App Bundle)`.
* Configure the new build with a keystore file, keystore password, key alias, and key alias password to match the key associated with the app in the Google Play Console.
* After the app bundle build is created, attempt another upload to the Google Play Console.

For more information, refer to Google's official post on [requiring aab for store uploads](https://android-developers.googleblog.com/2021/06/the-future-of-android-app-bundles-is.html).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40004).
