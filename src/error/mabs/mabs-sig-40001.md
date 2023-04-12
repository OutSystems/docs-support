---
summary: The APS Environment &lt;value&gt; doesn't match your provisioning profile.
tags: mabs sig error_code
guid: 794dfe3a-7086-4b35-bc0f-3b8a03415799
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-SIG-40001

## Error message

`The APS Environment <value> doesn't match your provisioning profile.`

## Cause

This error occurs when generating an iOS app that uses the APS environment entitlement with a value that doesn't match the value of the APS Environment entitlement declared in the provisioning profile in use.
This usually happens when a plugin is making use of push notification services, requiring the APS environment but having a mismatch in this value and in the provisioning profile used. This can happen, for instance, if the value used is debug but the provisioning profile is a in-house or distribution provisioning profile.

## Impact

Users can't generate the application package.

## Recommended action


Fix the mismatch and retry.

You can find more information about the APS Environment entitlement in the [official iOS Apple documentation](https://developer.apple.com/documentation/bundleresources/entitlements/aps-environment).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40001).
