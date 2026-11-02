---
summary: OS-MABS-UPLD-40015 error occurs when there is no app in the Google Play Console with the package name <package_name>, or the service account cannot see it
tags:
  - Android
  - Mobile app
  - Native App
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - google-play-console-upload-errors
audience:
  - Developer
  - Platform administrator
guid: 7f196f04-3d12-4ca0-bc68-882631c9b7d2
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40015

## Error message

`There is no app in the Google Play Console with the package name <package_name>, or the service account cannot see it. Create the app in the Google Play Console and invite the service account to upload releases for this app.`

## Cause

The app identifier specified in the configuration used to create the app bundle build does not match any package name that the Google Cloud service account has access to within your Google Play Console instance. This can happen because:

1. The Google Cloud service account does not have the correct permissions to find the app in the Google Play Console with that package name.
1. The service account has the correct account level permissions to upload for any app in the Google Play Console instance, but the package name has not been registered.
1. The package name has been registered and the Google Cloud service account has the correct account level permissions. However, no app is assigned to that package name.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

### Check the Google Cloud service account

* Confirm that the Google Cloud service account is invited as a user to your Google Play Console instance.
* Check that the service account has the following permissions at either the account level or for the specific app associated with the app bundle build:
    * View app information (read-only)
    * Release apps to testing tracks

For more information, refer to the official Google Play Console documentation on how to [Add developer account users and manage permissions](https://support.google.com/googleplay/android-developer/answer/9844686?hl=en#zippy=%2Cview-app-information-read-only).

### Check package name registration and app creation in Google Play Console

* In the ODC Portal, find the app identifier / app ID of the app bundle build used in the store upload attempt.
* In the Google Play Console, check the Android Developer Verification page contains a registered package name corresponding to the app identifier in ODC.
* If the package name is not present on this page, confirm that the app corresponding to this package name exists in the Google Play Console Home page.
* If the app does not exist, create the app with the package name matching the app identifier in ODC.
* If the app does exist, update the app identifier in ODC to match the package name of the app in the Google Play Console.

For more information, refer to the official Google Play Console documentation on how to [Register Android package names](https://support.google.com/googleplay/android-developer/answer/16761053?hl=en) and how to [Create and set up your app](https://support.google.com/googleplay/android-developer/answer/9859152?hl=en&sjid=12297974155048842979-NA).

### Contact support

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40015).
