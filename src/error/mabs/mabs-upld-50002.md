---
summary: OutSystems Developer Cloud (ODC) signed app upload errors occur when the build infrastructure cannot retrieve the signed package; retry the upload.
tags:
  - Android
  - iOS
  - Mobile app
  - Troubleshooting
guid: 802dfde5-f6e8-474e-ab06-563675d57884
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
  - 1-click-publish-errors
---

# OS-MABS-UPLD-50002

## Error message

`Couldn't retrieve your signed app to upload it. Try again.`

## Cause

The upload started, but the build infrastructure couldn't download the signed package of the build. The download failed, or ODC didn't provide a location for the signed package.

## Impact

The upload fails before ODC contacts the store. ODC sends nothing to the store.

## Recommended action

Upload the build again.

If the upload keeps failing with this error, generate the app again, and then upload the new build.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50002).
