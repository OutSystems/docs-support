---
summary: Something happened on our side while packaging your app. Please try again.
tags:
guid: 8b3f6a2b-5fb0-44a4-9380-fac1d4c76d1e
locale: en-us
app_type: mobile apps
platform-version: o11
---

# OS-MABS-KEY-50000

## Error message

`Something happened on our side while packaging your app. Please try again.`

## Cause

This error occurs when MABS fails to create the signing assets in the build process.

## Impact

Users can't generate the application package.

## Recommended action
Validate the correctness of your signing assets and try to repeat the operation and check the build logs on Service Center.

Find more information about the signing assets needed for iOS [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#for-ios) and for Android [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#for-android).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-KEY-50000).
