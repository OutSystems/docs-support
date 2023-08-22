---
summary: This certificate has an unknown file format.
tags: mabs sig error_code
guid: 2c20cf31-4e34-414e-b8f4-50af2377c802
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40004

## Error message

`This certificate has an unknown file format.`

## Cause

This error occurs when generating an iOS app and MABS isn't able to parse the certificate file.

## Impact

Users can't generate the application package.

## Recommended action

Check if the certificate has the correct format (only `.p12` extension is valid). Otherwise, replace it and retry.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40004).
