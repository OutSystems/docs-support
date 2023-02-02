---
summary: MABS <currentBuildVersion> doesn't support Android App Bundles. To generate an Android App Bundle, please use MABS <minVersion> or higher.
tags:
guid: 5a812ad2-a89e-426c-a49d-44c5d8ea65f3
locale: en-us
app_type: mobile apps
---

# OS-MABS-AAB-40000

## Error message

`MABS <currentBuildVersion> doesn't support Android App Bundles. To generate an Android App Bundle, please use MABS <minVersion> or higher.`

## Cause

This error occurs when you are trying to build an application package of type `bundle` (Android App Bundle) but are using an older MABS version.

## Impact

Users can't generate the application package.

## Recommended action

Select a higher MABS version that complies with the minimum required version and retry building your application.

Find more information about the bundle type in [our public documentation page](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-AAB-40000).
