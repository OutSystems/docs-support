---
summary: OutSystems Developer Cloud (ODC) store operation key errors require a matching upload record before you request status or logs.
tags:
  - Android
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 16297282-dcb3-4a23-9e6f-4cde38043830
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

# OS-MABS-UPLD-40019

## Error message

`The store upload wasn't found. Check the key in your request and try again.`

## Cause

ODC has no store upload with the key in your request. ODC keeps a record, called a store operation, for each upload of a build to App Store Connect or Google Play, and identifies the record by its store operation key.

ODC returns this error when you request the status or the log messages of a store operation through the API, and the key doesn't match any store operation in your organization.

## Impact

ODC doesn't return the status or the log messages. The error doesn't change any upload.

## Recommended action

Check that the request uses the store operation key that ODC returned when you started the upload, and then send the request again.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40019).
