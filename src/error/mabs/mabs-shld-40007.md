---
summary: The 'GooglePlayAppSigningCertificate' AppShield preference is deprecated
  and no longer supported. Use 'ApplicationSignerCertificate' instead.
tags:
  - Mobile app
  - Native App
  - Plugins
  - Security
  - Troubleshooting
guid: 1df4d22e-47fb-4a36-8010-837d781a07fa
locale: en-us
app_type: mobile apps
platform-version: o11
figma:
audience:
  - Developer
outsystems-tools:
  - service studio
coverage-type:
  - unblock
topic:
  - deprecated-signer-cert-error
isautopublish: true
---

# OS-MABS-SHLD-40007

## Error message

`The 'GooglePlayAppSigningCertificate' AppShield preference is deprecated and no longer supported. Use 'ApplicationSignerCertificate' instead.`

## Cause

This error occurs when the preference GooglePlayAppSigningCertificate is in the extensibility configurations of your app with the AppShield plugin.

## Impact

The application package can't be generated.

## Recommended action

Use the ApplicationSignerCertificate preference instead according to the [documentation](https://success.outsystems.com/documentation/11/security_and_compliance/harden_the_protection_of_mobile_apps_with_appshield/#how-to-whitelist-the-signing-certificate) and retry building the app.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SHLD-40007).
