---
summary: Adding a certificate to the trusted root store of your OutSystems cloud. This is necessary when integrating with external systems that bear self signed certificates.
tags: support-Cloud_Platform
locale: en-us
guid: 94fe2273-28c4-448f-8c54-cf699d40f9f1
app_type: traditional web apps, mobile apps, reactive web apps
---
# Add certificate to trusted root store in OutSystems Cloud


When integrating with external systems such as, for example, consuming webservices, integrating with external databases or with an Active Directory, there is often the requirement to do so over HTTPS.

When those external servers possess an SSL certificate issued by a public certificate authority (CA), the HTTPS connection is successfully established without the need for further configuration. 

## Applicable use case

It may be the case that those external servers bear certificates that aren't signed by a public CA, namely self-signed certificates.

These certificates aren't trusted by the client servers (in this case, the OutSystems servers), and therefore must be added to their trusted root store. When that step isn't executed, it leads to errors such as:

```Could not establish trust relationship for the SSL/TLS```. 

For OutSystems Cloud environments, this operation is performed by OutSystems support. This option is available depending on your subscription, check more details at the [Cloud services catalog](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Cloud_services_catalog).

<div class="info" markdown="1">

For self-managed environments, check [this article](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Add_self_signed_certificate_to_trusted_root_store_on_OutSystems) instead.

</div>

## Requesting the service

For OutSystems Cloud environments, you’ll need to [open a support case](https://www.outsystems.com/goto/submit-support-case) and:

* Provide the certificate, in .CER format.
* Make sure to be clear on what environments should we install the certificate.

## What will OutSystems deliver

OutSystems staff installs the certificates in all the front ends and notifies you once the operation is complete.

Please note that OutSystems doesn't monitor your certificates expiration date. Make sure to request this service ahead of time,  taking into account the [SLA for this service](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Cloud_services_catalog).
