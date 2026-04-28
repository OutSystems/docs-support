---
summary:
tags: email enforcement, external identity provider
guid: a20a16f3-9092-4032-8bdb-e10b93b0438e
locale: en-us
app_type: mobile apps, reactive web apps
platform-version: odc
figma:
outsystems-tools:
coverage-type:
  - unblock
audience:
topic:
isautopublish: true
---

# OS-xxxx-xxxx-xxxxx

## Error message

`Couldn't authenticate you because your email isn't verified or the identity provider configuration is incorrect. Try again. If the problem persists, contact your administrator. Displayed with “error code OS-xxxx-xxxx-xxxxx.`

## Cause

An end user attempts to log in with an external Identity Provider (IdP) using the **Trust identity provider** setting, but the **email_verified** claim is invalid or missing.

## Impact

The user cannot log in or access the app.

## Recommended action

To resolve this error, you should:

* **Verify IdP configuration**: Check the external IdP settings to ensure the email_verified claim mapping is present and is sending the correct data.

* For detailed guidance, refer to the documentation: [Email Verification and Profile Matching for External Identity Providers](https://success.outsystems.com/documentation/outsystems_developer_cloud/user_management/configuring_authentication_with_external_identity_providers/email_verification_and_profile_matching_for_external_identity_providers/#email-verification-logic).
