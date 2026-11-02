---
summary: Version <version_number> (<version_code>) for app identifier '<app_identifier>' has already been used. Use a different mobile version number or mobile version code and try again.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 3ada7b91-0d45-42af-b040-0b9ae8037eff
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
audience:
  - Developer
outsystems-tools:
  - odc portal
coverage-type:
  - unblock
topic:
---

# OS-MABS-UPLD-40025

## Error message

`Version <version_number> (<version_code>) for app identifier '<app_identifier>' has already been used. Use a different mobile version number or mobile version code and try again.`

The message includes the following values:

* `version_number`: the mobile version number of the build.
* `version_code`: the mobile version code of the build.
* `app_identifier`: the app identifier of the build, which is the bundle identifier on iOS and the package name on Android.

## Cause

ODC already uploaded, or is uploading, a build with the same app identifier, mobile version number, and mobile version code. A store doesn't accept two builds with the same version, so ODC stops the upload before it contacts the store.

Failed uploads don't count. A version stays available after an upload of it fails.

## Impact

ODC doesn't start the upload.

## Recommended action

Change the mobile version number or the mobile version code of the app, generate the app again, and upload the new build.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40025).
