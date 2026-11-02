---
summary: This build has no app identifier set. Wait for a build with an app identifier before uploading it to the store.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 82726935-7f1c-47a7-90a7-2de7cf4ba1c8
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

# OS-MABS-UPLD-40026

## Error message

`This build has no app identifier set. Wait for a build with an app identifier before uploading it to the store.`

## Cause

The build has no app identifier. The app identifier is the bundle identifier on iOS and the package name on Android. A store uses the app identifier to match a build to an app, so ODC can't upload a build without one.

## Impact

ODC doesn't start the upload.

## Recommended action

Generate the app again, and then upload the new build.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40026).
