---
summary: ODC MABS upload error 40008 explains App Store Connect rejections, apple_detail messages, and how to correct and rebuild the mobile app.
tags:
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: a99e9c14-16f4-42d2-95a9-9b20ec99df46
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

# OS-MABS-UPLD-40008

## Error message

`App Store Connect rejected the build. <apple_detail>`

## Cause

App Store Connect validated the build and refused it. The reason that App Store Connect returned appears in the message as `apple_detail`, for example `The provided entity is missing a required attribute.`

This error covers the rejections that don't have an error code of their own, so `apple_detail` is the only description of what App Store Connect objected to.

## Impact

App Store Connect doesn't accept the build.

## Recommended action

Correct what `apple_detail` reports, generate the app again, and upload the build.

If `apple_detail` doesn't identify the problem, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40008).
