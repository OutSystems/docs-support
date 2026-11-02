---
summary: OS-MABS-UPLD-40017 error occurs when an upload contains a version code used in a previous release of this app in the Google Play Console.
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
guid: d5d200dc-5835-4785-a7dd-9ce0ef50667f
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40017

## Error message

`The version code has been used in a previous release of this app in the Google Play Console. Create a new app bundle build with a new version code and upload again.`

## Cause

The Google Play Console requires that every new release has a version code that is unique and larger than the previous release to prevent a release from accidentally downgrading the app. The app bundle build used in the upload attempt was configured with a version code that has already been used.

For more information, refer to the official Google Play Console documentation on [Version codes](https://support.google.com/googleplay/android-developer/answer/17367361?hl=en).

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

* In the Google Play Console, find the version code of the latest release associated with your app.
* In ODC, create a new app bundle build configured with a version code that is higher than the latest release.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40017).
