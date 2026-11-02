---
summary: There's no app in App Store Connect with the bundle identifier <bundle_id>, or the API key can't access it. Create the app record and give the key at least the App Manager role.
tags:
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: fb31ef24-0a09-4134-bfd6-7f1f8c17b9a1
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

# OS-MABS-UPLD-40007

## Error message

`There's no app in App Store Connect with the bundle identifier <bundle_id>, or the API key can't access it. Create the app record and give the key at least the App Manager role.`

## Cause

App Store Connect has no app record for the bundle identifier `bundle_id` of your app, or the API key doesn't have access to that record. App Store Connect reports both situations the same way, because a record the key can't read is indistinguishable from a record that doesn't exist.

Uploading a build doesn't create the app record. You create the record in App Store Connect before the first upload.

## Impact

The upload to App Store Connect fails.

## Recommended action

In App Store Connect, confirm that an app exists with the bundle identifier `bundle_id`, and create it if it doesn't. Give the API key at least the App Manager role on the team that owns the app, and then upload again.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40007).
