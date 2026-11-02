---
summary: App Store Connect rejected the API key. Check that the Key ID and Issuer ID match the .p8 file, and that the key is still active.
tags:
  - Authentication
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 6965d5a6-254d-41d3-a4f0-e5b9a166851a
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

# OS-MABS-UPLD-40006

## Error message

`App Store Connect rejected the API key. Check that the Key ID and Issuer ID match the .p8 file, and that the key is still active.`

## Cause

App Store Connect didn't accept the credentials that authenticate the upload. Either the Key ID or the Issuer ID doesn't belong to the .p8 file in the configuration, or the key was revoked. App Store Connect returns the same response in both cases, so the error doesn't tell you which one applies.

## Impact

The upload to App Store Connect fails.

## Recommended action

In App Store Connect, confirm that the API key is still active and copy its Key ID and Issuer ID. Update the App Store Connect configuration so that the Key ID, the Issuer ID, and the .p8 file all belong to the same key, and then upload again.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40006).
