---
summary: OS-MABS-UPLD-40018 error occurs when the Google Play Console rejects your app release for a reason that doesn't match a more specific ODC error.
tags:
    - Android
    - Google Play
    - Mobile app
    - Troubleshooting
coverage-type:
    - unblock
topic:
    - google-play-console-upload-errors
audience:
    - Developer
guid: 43cd412b-b26d-44c4-96fe-6763233c55e8
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40018

## Error message

`Google Play rejected the release: <reason>`

## Cause

ODC reports this error when the Google Play Developer API rejects your app release for a reason that isn't covered by a more specific ODC error.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

Review the `<reason>` included in the error message to determine why Google Play rejected the release, then address it before uploading your app again.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40018).
