---
summary: Your provisioning profile <provision_profile> is missing the <entitlement> entitlement.
tags: ios provisioning, application packaging, error handling, mobile app distribution, entitlements management
guid: fa25cf31-dfed-4142-97f9-da8cfbc6317f
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

# OS-MABS-SIG-40016

## Error message

* `Your provisioning profile <provision_profile> is missing the <entitlement> entitlement. Review your provisioning profile entitlements.`

or

* `Your provisioning profile <provision_profile> is missing multiple entitlements. Check the build log for details and review your provisioning profile entitlements.`

## Cause

This error occurs when the provisioning profile used to generate the iOS app does not contain the necessary entitlements. If only one entitlement is missing, it is depicted in the error message as `<entitlement>`. If more than one entitlement is missing, check the build logs for the full details.

## Impact

Users can't generate the application package.

## Recommended action

Check the capabilities of the provisioning profile and ensure they match the entitlements needed to generate the application. Otherwise, fix the provisioning profile entitlements and retry. A list of Apple's entitlements can be found [here](https://developer.apple.com/documentation/bundleresources/entitlements).

For more information about generating your provisioning profile, refer to [Create a provisioning profile](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#create-a-provisioning-profile).
