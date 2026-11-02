---
summary: OS-MABS-UPLD-50005 error occurs when ODC fails to provide the app identifier as the package name for the Google Play Console upload process.
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
guid: b79bbf86-11a3-4b7b-a520-9062092997c2
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-50005

## Error message

`Failed to provide app identifier as the package name for upload to Google Play Console.`

## Cause

ODC uses the Google Play Developer API associated with your Google Cloud service account to upload app bundle builds to the Google Play Console. The API requires a package name that maps to the app identifier assigned to the app bundle build. This error occurs when ODC has failed to provide the app identifier to that API because of an internal issue.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

* Check that an app identifier / app ID has been assigned to the app bundle build that was used in the upload attempt.
* Create a new app bundle build configured with an app identifier corresponding to the package name for the app in the Google Play Console that the Google Cloud service account has permissions to release to.
* Attempt to upload the new app bundle build to the Google Play Console.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50005).
