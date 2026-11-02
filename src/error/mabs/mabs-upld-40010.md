---
summary: The App Store Connect API key isn't allowed to upload for this app. Give the key at least the App Manager role on the team that owns the app, and check that the team membership is active.
tags:
  - Authorization
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: ec6ab668-fb60-4951-8822-dbdfe1028bc0
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

# OS-MABS-UPLD-40010

## Error message

`The App Store Connect API key isn't allowed to upload for this app. Give the key at least the App Manager role on the team that owns the app, and check that the team membership is active.`

## Cause

App Store Connect accepted the API key and then refused the upload because of the key's role. The key holds a role that doesn't permit uploads, or the team membership that the key belongs to is no longer active.

The key itself is valid, which separates this error from the errors that report credentials App Store Connect can't accept at all.

## Impact

The upload to App Store Connect fails.

## Recommended action

In App Store Connect, give the API key at least the App Manager role on the team that owns the app, and confirm that the team membership is active. Then upload again.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40010).
