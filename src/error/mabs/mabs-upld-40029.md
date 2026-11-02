---
summary: ODC MABS upload error 40029, create a 25-year keystore and register its SHA-256 fingerprint in Google Play.
tags:
  - Android
  - Mobile app
  - Troubleshooting
coverage-type:
  - apply
  - unblock
topic:
  - google-play-console-upload-errors
audience:
  - Developer
guid: 363a6658-b94f-4c3a-92b4-3b0e8e0313f2
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40029

## Error message

`The certificate used to sign the app bundle expires too soon for Google Play to accept it. Re-sign the app with a certificate that is valid for at least 25 years.`

## Cause

The Google Play Console requires a release to be signed with a key that remains valid for at least a 25 year period. This error occurs because the app bundle build used in the upload attempt was signed with a key that has a shorter lifespan.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

Generate a new keystore file with the correct validity duration using one of the following methods:

### Android studio

Create a new keystore file in [Android Studio](https://developer.android.com/studio/publish/app-signing#register_upload_key) with a validity set to at least `25` years.

### Command line

Create a new keystore file using the [keytool command](https://developer.android.com/build/building-cmdline#sign_cmdline) with a validity set to at least `10000` days

### Updating dependencies

After creating the keystore file, retrieve the SHA-256 certificate fingerprint from the key inside the keystore file using one of the methods described in the Google Play Console support page for [obtaining your app's SHA-256 certificate fingerprint](https://support.google.com/googleplay/android-developer/answer/16641489?hl=en)

Add the SHA-256 certificate fingerprint to the package name registration in the Google Play Console. For more information, refer to the Play Console support page on [registering Android package names](https://support.google.com/googleplay/android-developer/answer/16761053?hl=en).

In ODC, configure a new app bundle build using the new keystore file and key alias corresponding to the new key registered in the Google Play Console. Then attempt an upload to the Google Play Console using the newly created app bundle build.

For more information, refer to the official Android Developer documentation on [signing your app for release to Google Play](https://developer.android.com/studio/publish/app-signing#sign-apk).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40029).
