---
summary: Your provisioning profile has an unknown format.
tags: mabs sig error_code
guid: 559f997f-6e3f-4cbb-acf6-3e1d6eff703e
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-SIG-40006

## Error message

`Your provisioning profile has an unknown format.`

## Cause

This error occurs when generating an iOS app and MABS is not able to parse the provisioning profile file.

## Impact

Users can't generate the application package.

## Recommended action
Check if the provisioning profile has the correct format (only `.mobileprovision` extension is valid). Otherwise, replace it and retry.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40006).
