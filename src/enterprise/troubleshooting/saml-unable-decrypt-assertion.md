---
summary: Common error when authenticating using SAML. Check the cause and the resolution.
locale: en-us
guid: 9807d569-fb06-45bd-8c68-ae204ee2aa8c
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Error processing SAML response - Unable to decrypt the assertion

## Symptoms

You configured end-users authentication [to use SAML](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_Users/End_Users_Authentication/Configure_SAML_2.0_Authentication) and you get the following error when the end users attempt to login:

`Error processing response. Unable to decrypt the assertion. Probably the IdP server did not encrypt it with the expect certificate. Check with IdP server admin if has configured the correct IdP connector public certificate.​`

## Cause

This error means that the Service Provider (SP) wasn't able to decrypt the assertion created by the Identity Provider (IdP), which causes the authentication process to fail. Thus, the certificate configuration might haven't been performed correctly.

## Resolution

To solve this problem, do the following:

1. In the Users application (`https://<environment_address>/Users`), click **Configure Authentication** in the sidebar.

1. In the **Service Provider Connector Settings** section, click the **Auto generate KeyStore** button.

1. Click the **Download KeyStore** link and save the keystore file locally.

1. Click the **DOWNLOAD SP METADATA XML** button and save the metadata XML file locally.

1. Click the **Save** button to ensure you save the new configuration.

1. On your SAML Identity Provider side, upload both the keystore file and the metadata XML file that you saved previously.
