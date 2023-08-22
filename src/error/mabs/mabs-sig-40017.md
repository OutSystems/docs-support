---
summary: Signing settings require a manually managed profile, but your provisioning profile <provision_profile> is Xcode managed.
tags: mabs sig error_code
guid: a13df32f-10f3-4585-90fe-015f448ad93b
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40017

## Error message

`Signing settings require a manually managed profile, but your provisioning profile <provision_profile> is Xcode managed.`

## Cause

This error occurs when generating an iOS app and the provisioning profile file is an Xcode managed provisioning profile.

## Impact

Users can't generate the application package.

## Recommended action

Replace the Xcode managed provisioning profile for a manually created provisioning profile and retry.

Find more information about generating your provisioning profile [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#create-a-provisioning-profile).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40017).
