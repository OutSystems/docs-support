---
summary: There was an issue reading the certificate keys.
tags: mabs sig error_code
guid: 95cb4024-e26a-4fe7-9775-ee5a0885cd72
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40008

## Error message

`There was an issue reading the certificate keys.`

## Cause

This error occurs when MABS can't process or find the necessary information in the provisioning profile.

## Impact

Users can't generate the application package.

## Recommended action

Check if the provisioning profile is valid and if it has the correct format (only `.mobileprovision` extension is valid). Otherwise, replace it and retry.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40008).
