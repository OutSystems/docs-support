---
summary: OS-MABS-UPLD-40002 error occurs when the Google Cloud service account JSON is not valid. Configure the store upload with a valid service account JSON key from your Google Cloud project and try again.
tags:
  - Android
  - Authentication
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
audience:
  - Developer
  - Platform administrator
guid: 3a6f0f6b-074e-4a9a-a863-18475b017119
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40002

## Error message

`The Google Cloud service account JSON is not valid. Configure the store upload with a valid service account JSON key from your Google Cloud project and try again.`

## Cause

ODC uses a Google Cloud service account JSON to authenticate with the Google Play Developer API associated with your Google Play Console instance to upload your app bundle build to the internal release track.

The file uploaded as the `Service Account JSON` for the store operation is not a valid Google Cloud service account JSON either because the file is not a valid JSON or is missing required fields.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

* Confirm if the `type`, `private_key`, and `client_email` keys have been removed from the Google Cloud service account JSON file.
* If they have been removed, set up a new Google Cloud service account JSON key in your Google Cloud Platform Project and in the Google Play Console.
* Upload the new JSON key as the `Service Account JSON` in ODC and attempt another store upload.

For more information, refer to Google's official documentation on using a [Google Cloud service account JSON with Google Play Console](https://developers.google.com/android-publisher/getting_started#service-account).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40002).
