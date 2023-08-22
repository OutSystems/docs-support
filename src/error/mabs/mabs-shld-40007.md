---
summary: The value of ‘GooglePlayAppSigningCertificate’ AppShield preference isn’t valid. Check if its format is a valid base64.
tags:
guid: 1df4d22e-47fb-4a36-8010-837d781a07fa
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SHLD-40007

## Error message

`The value of ‘GooglePlayAppSigningCertificate’ AppShield preference isn’t valid. Check if its format is a valid base64.`

## Cause

This error occurs when the preference, GooglePlayAppSigningCertificate, in the extensibility configurations of your app has an invalid base64.

## Impact

The application package can't be generated.

## Recommended action

Review the preference value by using the [documentation](https://success.outsystems.com/documentation/11/delivering_mobile_apps/harden_the_protection_of_mobile_apps_with_appshield/#Google-Play-App-Signing) about the generation of the base64 value and retry building the app.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SHLD-40007).
