---
summary: Build version <build_version> has already been uploaded to App Store Connect for this app. Increase the build version and upload again.
tags:
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: a8a8fa7b-8639-4444-91f7-40b7649faed5
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
  - fix-duplicate-version
---

# OS-MABS-UPLD-40009

## Error message

`Build version <build_version> has already been uploaded to App Store Connect for this app. Increase the build version and upload again.`

When App Store Connect doesn't report the version that caused the conflict, the message names no version:

`The build version has already been uploaded to App Store Connect for this app. Increase the build version and upload again.`

## Cause

App Store Connect already holds a build for this app whose version is the same as, or higher than, the version `build_version` you uploaded. Every upload for an app must carry a version higher than each version uploaded before it.

## Impact

App Store Connect doesn't accept the build.

## Recommended action

Increase the version of your app, generate the app again, and upload the new build.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40009).
