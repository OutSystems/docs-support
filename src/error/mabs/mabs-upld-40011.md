---
summary: App Store Connect blocks uploads because a required agreement is missing or has expired. Sign the outstanding agreement and upload again.
tags:
  - Blocks
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 026322e7-91df-4adc-8423-324a42654c29
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
  - fix-agreement-error
---

# OS-MABS-UPLD-40011

## Error message

`App Store Connect blocks uploads because a required agreement is missing or has expired. Sign the outstanding agreement and upload again.`

## Cause

An agreement that Apple requires for your developer account isn't signed, or it expired. App Store Connect refuses uploads for the account until the agreement is in effect. Neither the build nor the API key is the cause.

Agreements expire on Apple's schedule, so an account that uploaded without trouble before can start returning this error with no change on your side.

## Impact

App Store Connect blocks the upload.

## Recommended action

Sign the outstanding agreement in App Store Connect, and then upload again. Signing an agreement requires an account with the Account Holder role.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40011).
