---
summary: This build has build type '<build_type>', but App Store Connect accepts only AppStore builds. Generate the app again as an AppStore build and upload it.
tags:
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 781ade77-8415-4672-aaab-1be89668e8ee
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

# OS-MABS-UPLD-40003

## Error message

`This build has build type '<build_type>', but App Store Connect accepts only AppStore builds. Generate the app again as an AppStore build and upload it.`

## Cause

The build you selected was generated with the build type `build_type`, and App Store Connect accepts only builds generated with the AppStore build type. The other iOS build types, such as Development and Adhoc, produce packages for direct installation on registered devices, and App Store Connect rejects them.

The build type is fixed when you generate the app, so an existing build can't be converted.

## Impact

The upload to App Store Connect doesn't start.

## Recommended action

Generate the app again with the AppStore build type, and then upload the resulting build to App Store Connect.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40003).
