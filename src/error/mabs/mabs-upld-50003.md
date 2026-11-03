---
summary: Couldn't deliver your app to App Store Connect. Try again.
tags:
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 23db5d03-a90f-4038-be8b-e8c904ddcd6b
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
  - mabs-build-errors
---

# OS-MABS-UPLD-50003

## Error message

`Couldn't deliver your app to App Store Connect. Try again.`

## Cause

The delivery to App Store Connect failed without a reason that identifies what went wrong. App Store Connect returned no rejection detail, so ODC can't map the failure to a specific cause.

A connectivity problem between the build infrastructure and App Store Connect produces this error, which is why a later attempt often succeeds with no change to the app or the credentials.

## Impact

The upload to App Store Connect fails.

## Recommended action

Upload the app again.

If the upload keeps failing, check the upload log of the operation. The log holds the output of the delivery, including messages that the error doesn't carry.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50003).
