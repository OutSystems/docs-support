---
summary: There was an issue generating the app. Please check if your app identifier, certificate, and provisioning profile match the Development application type.
tags: mabs sig error_code
guid: 4f6e76b1-ffcf-4099-a247-d3c4b4238b84
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40011

## Error message

`There was an issue generating the app. Please check if your app identifier, certificate, and provisioning profile match the Development application type.`

## Cause

This error occurs when the information that connects the provisioning profile, certificate, and application identifier don't match.

## Impact

Users can't generate the application package.

## Recommended action

Check the information provided and review the provisioning profile, certificate and application identifier to ensure that the information is matching. Otherwise, replace it and retry.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40011).
