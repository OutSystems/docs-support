---
summary: Unable to create SAML signature
locale: en-us
guid: 0304263d-9ae2-41dd-8cdf-b766e79613f1
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Unable to create SAML signature

## Symptoms

You configured end-user authentication [to use SAML](https://success.outsystems.com/documentation/11/developing_an_application/secure_the_application/end_users/end_users_authentication/configure_saml_2.0_authentication/) and you get the following error when the end users attempt to logout: ``Unable to process request. Unable to create SAML signature``.

## Cause

Due to [Personal environment hosting infrastructure under the hood](https://success.outsystems.com/support/licensing/personal_environment_hosting_infrastructure_under_the_hood/) and security constraints, this error is thrown during the logout.

<div class="info" markdown="1">

This applies to the free offering of personal environments only.

</div>

### Related articles
[What is an OutSystems Personal Environment](../../licensing/whats-a-personal.md)
