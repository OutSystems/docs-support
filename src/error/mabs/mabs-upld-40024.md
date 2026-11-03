---
summary: A build of this app for the same platform has not finished yet. Wait for it to complete before uploading to the store.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: fa791a36-34fe-4143-a4b0-f8587add12b5
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
  - fix-running-build
---

# OS-MABS-UPLD-40024

## Error message

The message names the platform of the build you're uploading.

For an iOS build:

`The iOS build of this app has not finished yet. Wait for it to complete before uploading to the store.`

For an Android build:

`The Android build of this app has not finished yet. Wait for it to complete before uploading to the store.`

## Cause

A build of the app for the same platform is still running. ODC doesn't upload a build to the store while the latest build for that platform is running. The running build can be a different build from the one you're uploading.

## Impact

ODC doesn't start the upload.

## Recommended action

Wait for the running build to finish, and then upload again.

If the running build finishes successfully, ODC deletes the signed package of older builds. In that case, upload the build that finished.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40024).
