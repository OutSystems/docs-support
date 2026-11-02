---
summary: Something went wrong and we couldn't start the store upload. Try again, and if the problem persists, contact OutSystems Support.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: f4d1699c-fb7b-4290-a654-7e173906ba13
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

# OS-MABS-UPLD-50006

## Error message

`Something went wrong and we couldn't start the store upload. Try again, and if the problem persists, contact OutSystems Support.`

## Cause

ODC accepted the upload request but couldn't start sending the build to the store. A temporary problem in ODC can cause this, or the build can be missing information that the upload needs.

## Impact

The upload fails before ODC contacts the store.

## Recommended action

Upload the build again.

If the upload fails again, generate the app again, and then upload the new build.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50006).
