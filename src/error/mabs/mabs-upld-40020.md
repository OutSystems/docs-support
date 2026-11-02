---
summary: MABS upload error in OutSystems Developer Cloud (ODC) identifies duplicate build uploads and when to retry after the earlier upload finishes.
tags:
  - Mobile app
  - Native App
  - Troubleshooting
guid: 4f7b053e-36c0-43a5-ab05-ce4ddc38ea13
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

# OS-MABS-UPLD-40020

## Error message

`An upload to the store is already in progress.`

## Cause

An earlier upload of the same build to the store hasn't finished. ODC runs one upload at a time for each build, so it doesn't start another upload of the build until the earlier one finishes or fails.

## Impact

ODC doesn't start the upload. The earlier upload continues.

## Recommended action

Wait for the earlier upload to finish, and then check its result:

* If the earlier upload succeeded, the build is already in the store. You don't need to upload the build again.
* If the earlier upload failed, fix the cause that its error reports, and then upload the build again.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40020).
