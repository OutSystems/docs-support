---
summary: OutSystems Developer Cloud (ODC) MABS upload errors, configure App Store Connect or Google Play credentials.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: ccd9da3c-f187-4fc5-8a47-3ff43e8b3d99
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
audience:
  - Developer
  - Platform administrator
outsystems-tools:
  - odc portal
coverage-type:
  - unblock
topic:
---

# OS-MABS-UPLD-40022

## Error message

The message names the store you're uploading to.

For an upload to App Store Connect:

`No App Store Connect store configuration is set for this app. Configure it before uploading to the store.`

For an upload to Google Play:

`No Google Play store configuration is set for this app. Configure it before uploading to the store.`

## Cause

The app has no credentials saved for the store that matches the platform of the build:

* To upload an iOS build, ODC needs the App Store Connect API key of the app.
* To upload an Android build, ODC needs the Google Play service account key of the app.

ODC checks for the credentials when you start the upload, and again before it sends the build to the store.

## Impact

ODC doesn't start the upload. If the second check fails, the upload fails before ODC contacts the store.

## Recommended action

Save the store credentials for the app, and then upload the build again:

* For an iOS build, save the App Store Connect API key, including the .p8 file, the key ID, and the issuer ID.
* For an Android build, save the JSON key file of the Google Play service account.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40022).
