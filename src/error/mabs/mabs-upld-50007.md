---
summary: ODC MABS store upload failures require checking upload logs and resolving OS-MABS errors before retrying.
tags:
  - Logging
  - Mobile app
  - Native App
  - Troubleshooting
guid: 618ac045-89ff-46b0-9c68-dab6a1089a1e
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

# OS-MABS-UPLD-50007

## Error message

`Something went wrong during the store upload. Try again, and if the problem persists, contact OutSystems Support.`

## Cause

The upload started but didn't finish successfully. The upload ran past its time limit, or it stopped with an error because the store rejected the build or a step of the upload failed.

## Impact

The upload fails.

## Recommended action

Check the upload log of the operation before you try again. If the log reports an OS-MABS-UPLD error code, follow the recommended action for that code first, because uploading the same build again without a change fails the same way.

If the log reports no error, upload the build again. A slow connection to the store can make the upload run out of time, and a later attempt often succeeds with no change to the app.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50007).
