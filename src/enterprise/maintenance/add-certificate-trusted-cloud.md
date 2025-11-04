---
summary: Learn how to add certificates to the trusted root store in OutSystems 11 (O11) Cloud environments to ensure secure HTTPS connections with external systems.
tags: ssl/tls, https, certificate management, cloud services, trusted root store
locale: en-us
guid: 94fe2273-28c4-448f-8c54-cf699d40f9f1
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - platform administrators
  - full stack developers
outsystems-tools:
  - service center
coverage-type:
  - remember
---

# Add certificate to trusted root store in OutSystems Cloud

<div class="warning" markdown="1">

This article applies to O11 Cloud Environments only.

</div>

When integrating with external systems such as, for example, consuming webservices, integrating with external databases or with an Active Directory, there is often the requirement to do so over HTTPS.

When those external servers possess an SSL certificate issued by a public certificate authority (CA), the HTTPS connection is successfully established without the need for further configuration.

## Applicable use case

It may be the case that those external servers bear certificates that aren't signed by a public CA, namely self-signed certificates.

These certificates aren't trusted by the client servers (in this case, the OutSystems servers), and therefore must be added to their trusted root store. When that step isn't executed, it leads to errors such as:

`Could not establish trust relationship for the SSL/TLS`.

For OutSystems Cloud environments, this operation is performed by OutSystems support. This option is available depending on your subscription. For more information, refer to the [Cloud services catalog](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Cloud_services_catalog).

Refer to [TLS Cipher Suites in Windows 10 v1607](https://learn.microsoft.com/en-us/windows/win32/secauthn/tls-cipher-suites-in-windows-10-v1607) for the supported encryptions.

<div class="info" markdown="1">

For self-managed environments, check [this article](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Add_self_signed_certificate_to_trusted_root_store_on_OutSystems) instead.

</div>

## Requesting the service

For OutSystems Cloud environments, you'll need to [open a support case](https://www.outsystems.com/goto/submit-support-case) and:

* Provide the certificate, in .CER format.
* Ensure you're clear about the environments on which the certificate should be installed.

## What will OutSystems deliver

OutSystems staff installs the certificates in all the front ends and notifies you once the operation is complete.

Please note that OutSystems doesn't monitor your certificates expiration date. Make sure to request this service ahead of time,  taking into account the [SLA for this service](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Cloud_services_catalog).
