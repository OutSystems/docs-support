---
summary: OS-MABS-UPLD-40028 error occurs when the app bundle's target SDK version does not meet the Google Play target API level requirement.
tags:
  - Android
  - Mobile app
  - Native App
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - google-play-console-upload-errors
audience:
  - Developer
  - Platform administrator
guid: 9c35c9e0-4652-4b50-861e-e851fe6e002d
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40028

## Error message

`The app bundle's target SDK version (<sdk version>) does not meet the Google Play target API level requirement. Create a new app bundle build with a MABS version containing a valid target SDK version and upload again.`

## Cause

The Google Play Console requires an app to be compatible with Google's preferred Android versions. The minimum version to fulfill this requirement is called the target SDK version or target API Level. This error occurs because the app bundle build used in the upload attempt was created using a Mobile Apps Build Service (MABS) version that does not meet this target API level.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

1. Refer to the official Android Developer documentation on the [target API level requirement](https://developer.android.com/google/play/requirements/target-sdk) to find the current target API Level.
1. Refer to the OutSystem documentation on [Mobile Apps Build Service versions](https://success.outsystems.com/support/release_notes/mobile_apps_build_service_versions/) to determine the MABS version with the target SDK / API Level.
1. In ODC, create a new app bundle build configured to use the MABS version that has the target API level.
1. Attempt an upload to the Google Play Console using the newly created app bundle build.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40028).
