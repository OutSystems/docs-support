---
summary: OutSystems Developer Cloud (ODC) MABS app bundle signing errors require the Google Play Console key registered for the package name.
tags:
  - Android
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - google-play-console-upload-errors
audience:
  - Developer
  - Platform administrator
guid: a243abb7-e16e-4ef1-b239-a96a6e202c19
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40027

## Error message

`The app bundle was signed with the wrong key. Sign the bundle with the key expected by Google Play Console and upload again.`

## Cause

The Google Play Console requires proof of ownership of an app to upload an app bundle build as a new release of that app. This is done by having the app bundle build signed with a key registered in your Google Play Console instance. The keystore file used in the configuration for creating a new app bundle build contains the key expected by the Google Play Console. This error occurs when that keystore file contains an invalid key.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

Create a new app bundle build configured with the keystore file containing the key that was registered in Google Play Console to the package name under the Android developer verification page. For more information, refer to the official Android Developers documentation on [registering Android package names](https://developer.android.com/developer-verification/guides/developer-console-api).

If that keystore file cannot be obtained, generate a new keystore file and register it in the Google Play Console using one of the following methods:

### Android studio

Create a new keystore file in [Android Studio](https://developer.android.com/studio/publish/app-signing#register_upload_key).

### Command line

Create a new keystore file using the [keytool command](https://developer.android.com/build/building-cmdline#sign_cmdline).

### Updating dependencies

After creating the keystore file, retrieve the SHA-256 certificate fingerprint from the key inside the keystore file using one of the methods described in the Google Play Console support page for [obtaining your app's SHA-256 certificate fingerprint](https://support.google.com/googleplay/android-developer/answer/16641489?hl=en)

Add the SHA-256 certificate fingerprint to the package name registration in the Google Play Console. For more information, refer to the Play Console support page on [registering Android package names](https://support.google.com/googleplay/android-developer/answer/16761053?hl=en).

In ODC, configure a new app bundle build using the new keystore file and key alias corresponding to the new key registered in the Google Play Console. Then attempt an upload to the Google Play Console using the newly created app bundle build.

For more information, refer to the official Android Developer documentation on [signing your app for release to Google Play](https://developer.android.com/studio/publish/app-signing#sign-apk).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40027).
