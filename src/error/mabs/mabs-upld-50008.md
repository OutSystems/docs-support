---
summary: OutSystems Developer Cloud (ODC) MABS upload errors block App Store Connect or Google Play builds; retry the upload and check its log.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 4cf697d3-337a-4ddf-89cd-fadf5ff2c19e
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

# OS-MABS-UPLD-50008

## Error message

The message names the store you're uploading to.

For an upload to App Store Connect:

`Couldn't upload your app to App Store Connect. If the problem persists, check our documentation for more information.`

For an upload to Google Play:

`Couldn't upload your app to Google Play. If the problem persists, check our documentation for more information.`

## Cause

The upload failed with an error that doesn't match any known store upload error. ODC reports this generic error because it can't map the failure to a specific cause.

## Impact

The upload fails, and the store doesn't receive the build.

## Recommended action

Upload the build again.

If the upload keeps failing, check the upload log of the operation. The log holds the output of the upload, including messages from the store that the error doesn't carry.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50008).
