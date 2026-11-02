---
summary: MABS upload error OS-MABS-UPLD-50001 helps you resolve missing App Store Connect or Google Play credentials by retrying the build.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: a4c5cabe-57b7-47ad-8c29-8132b618ddef
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

# OS-MABS-UPLD-50001

## Error message

`Couldn't retrieve the credentials needed to upload your app. Try again.`

## Cause

The upload started, but the build infrastructure couldn't read the store credentials saved for the app. The credentials are the App Store Connect API key for an iOS build, or the Google Play service account key for an Android build.

This error doesn't mean the credentials aren't valid. A store that rejects the credentials returns a different error.

## Impact

The upload fails before ODC contacts the store.

## Recommended action

Upload the build again.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50001).
