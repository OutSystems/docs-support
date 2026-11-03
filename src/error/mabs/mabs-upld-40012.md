---
summary: OS-MABS-UPLD-40012 error occurs when the Google Cloud service account JSON contains an invalid private key. Configure the store upload with a valid service account JSON key from your Google Cloud project and try again.
tags:
  - Android
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - fix-google-play-key-error
audience:
  - Developer
guid: 769c0df5-b3b9-461a-9a0d-10af0d61f5b9
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40012

## Error message

`The Google Cloud service account JSON contains an invalid private key. Configure the store upload with a valid service account JSON key from your Google Cloud project and try again.`

## Cause

ODC uses a Google Cloud service account JSON to authenticate with the Google Play Developer API associated with your Google Play Console instance to upload your app bundle build to the internal release track. This error occurs when the JSON file contains a value in its `private_key` key that is not a valid RSA private key.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

* Confirm if the value of the `private_key` key inside the JSON file has been modified.
* If `private_key` has been modified, set up a new Google Cloud service account JSON in your Google Cloud project and in the Google Play Console.
* Upload the new JSON key as the `Service Account JSON` in ODC and attempt another store upload.

For more information, refer to Google's official documentation on using a [Google Cloud service account JSON with Google Play Console](https://developers.google.com/android-publisher/getting_started#service-account).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40012).
