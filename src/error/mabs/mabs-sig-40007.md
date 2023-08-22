---
summary: Your provisioning profile is invalid. Please choose another .mobileprovision file.
tags: mabs sig error_code
guid: a37c9452-1bcc-4ea4-9256-262fe83c9e91
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40007

## Error message

`Your provisioning profile is invalid. Please choose another .mobileprovision file.`

## Cause

This error occurs when generating an iOS app and the provisioning profile isn't valid.

## Impact

Users can't generate the application package.

## Recommended action

Check if the provisioning profile is valid and if it has the correct format (only `.mobileprovision` extension is valid). Otherwise, replace it and retry.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40007).
