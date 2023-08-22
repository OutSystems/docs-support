---
summary: Your provisioning profile <provision_profile> is missing the aps-environment entitlement.
tags: mabs sig error_code
guid: fa25cf31-dfed-4142-97f9-da8cfbc6317f
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40016

## Error message

`Your provisioning profile <provision_profile> is missing the aps-environment entitlement.`

## Cause

This error occurs when generating an iOS app and the provisioning profile file does not contain the aps-environment entitlement.

## Impact

Users can't generate the application package.

## Recommended action

Check the capabilities of the provisioning profile and ensure they match the capabilities needed to generate the application. Otherwise, fix the provisioning profile capabilities and retry.

Find more information about generating your provisioning profile [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#create-a-provisioning-profile).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40016).
