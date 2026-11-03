---
summary: OS-MABS-UPLD-40016 error occurs when the Google Cloud service account is not allowed to upload releases of this app to the Google Play Console.
tags:
  - Android
  - Authorization
  - Deploy
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - fix-play-service-account
audience:
  - Developer
  - Platform administrator
guid: b330f2f5-afd1-469f-826a-fa7cce75775f
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40016

## Error message

`The Google Cloud service account is not allowed to upload releases for this app. Invite the service account to your Google Play Console instance and give it the permissions needed to release to testing tracks.`

## Cause

ODC uses your Google Cloud service account to upload your app bundle build to your Google Play Console instance. This error occurs when the service account isn't a user of the Google Play Console instance that owns the app, or when the service account is a user but doesn't have permission to release app bundle builds to the testing tracks.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

* Invite the Google Cloud service account as a user to your Google Play Console instance.
* Provide the service account with the following permissions at either the account level or for the specific app associated with the app bundle build:
    * View app information (read-only)
    * Release apps to testing tracks

For more information, refer to the official Google Play Console documentation on how to [Add developer account users and manage permissions](https://support.google.com/googleplay/android-developer/answer/9844686?hl=en#zippy=%2Cview-app-information-read-only).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40016).
