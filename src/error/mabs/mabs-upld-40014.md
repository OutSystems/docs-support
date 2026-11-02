---
summary: OS-MABS-UPLD-40014 error occurs when the Google Play Developer API isn't enabled for the service account's Google Cloud project.
tags:
  - Android
  - Deploy
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - google-play-console-upload-errors
audience:
  - Developer
guid: 253bbaf3-71da-446e-b0fa-d624cfd1d60e
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40014

## Error message

`The Google Play Developer API isn't enabled for the service account's Google Cloud project. Enable it in the Google Cloud Console and try again.`

## Cause

ODC uses the Google Play Developer API to upload your app bundle build to the Google Play Console. This error occurs when the API isn't enabled for the Google Cloud project that owns the service account.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

Enable the Google Play Developer API for the service account's Google Cloud project. Then upload your app bundle build again. For more information, refer to the official Google Play Developer API documentation on how to [Enable the API](https://developers.google.com/android-publisher/getting_started#enable).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40014).
