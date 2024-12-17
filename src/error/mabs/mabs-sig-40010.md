---
summary: Your certificate and provisioning profile don't match. Confirm the information for both of them.
tags: error resolution, certificate management, provisioning profile, application packaging, mobile application deployment
guid: 344fa10a-3f35-41d2-b92c-1430074d69fd
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# OS-MABS-SIG-40010

## Error message

`There are no certificates that match the provisioning profile. Make sure you include the desired certificate in the provisioning profile.`

## Cause

This error occurs when the pair certificate and provisioning profile don't match. This could happen if there's incorrect information about the certificate, the provision profile, or both.

## Impact

Users can't generate the application package.

## Recommended action

Confirm and update the certificate and provision information and make sure that they match each other.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40010).
