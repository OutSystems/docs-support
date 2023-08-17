---
summary: This document presents all the certificate related options in OutSystems. It also clarifies on certificate ownership and responsibilities.
locale: en-us
guid: 5790c5c1-1cc3-4598-a2a9-b247fd26a9a0
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OutSystems certificate management

This article describes how certificates are managed in the OutSystems cloud and self-managed deployments.

## Application server certificates

According to [OutSystems system requirements](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_system_requirements), the application server must be configured with a valid SSL certificate emitted by a public Certificate Authority.

### OutSystems cloud

This section describes how certificates are managed in the OutSystems cloud. The information present here can describe a process different from your past experience as it's intended to adapt to the short-lived certificate limitations implemented by the browser vendors owning most of the web browser market share.

#### Default OutSystems cloud server certificate

Your OutSystems cloud environments are automatically deployed with the default and valid SSL `outsystemsenterprise.com` wild card certificate. This certificate and it's domain are owned and managed by OutSystems. It can only be used by OutSystems.

Furthermore, on September 1, 2020, most browser vendors will no longer trust certificates that are valid for more than 398 days. To accomodate these changes OutSystems will regularly rotate the `outsystemsenterprise.com` certificate, check [here](https://success.outsystems.com/Support/Security/OutSystems_Cloud_certificate_rotation) for more details.

<div class="warning" markdown="1">

OutSystems will communicate the certificate change whenever possible. However, OutSystems reserves the right to change the certificate without prior communication or in short notice.

</div>

#### Using your own domain and certificate in OutSystems cloud servers

It's possible, and **highly advisable**, to [customize your environment hostname and SSL certificate](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Enable_Custom_SSL_Domain_In_OutSystems_PaaS). This will allow you to be independent when implementing certificate related features, such as [SSL pinning](https://www.outsystems.com/forge/Component_Documentation.aspx?ProjectId=1873&ProjectName=ssl-pinning-plugin). 

In this situation, the certificate and it's associated domain are owned by the customer. OutSystems is responsible for the certificate instalation but it's the customer's responsibility to monitor it's expiration and submit a request for the renewal.

### Self-managed environments

On the road to fast development and deployment of applications make sure to consult this [article](https://success.outsystems.com/Support/Enterprise_Customers/Installation/How_to_install_an_SSL_Certificate_for_the_OutSystems_platform) for instructions on how to install a certificate in your application server. This allows your OutSystems applications to use secure connections via HTTPS.

The server certificate, it's associated domain and the instalation are of the customer's responsibility.

## Add certificate to trusted root store

When integrating with external systems (for example: when consuming webservices, integrating with external databases or with an Active Directory), there is often the requirement to do so over HTTPS.

When those external servers possess a certificate that isn't trusted (such as a self signed certificate) it's necessary to add it to the clients' (in this case the Platform Server) trusted root store. 

### OutSystems cloud

Find [here](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Add_certificate_to_trusted_root_store_in_OutSystems_cloud) the instructions to add certificates to the trusted root store in the OutSystems Cloud.

In this situation, the certificate is owned by the customer. OutSystems is responsible for the certificate instalation but it's the customer's responsibility to monitor it's expiration and submit a request for the renewal.

### Self-managed environments

You'll also need to add the certificate to the trusted root store for the cenarios described. Follow the instructions of your current operating system.
The certificate, and the instalation are both of the customer's responsibility.


## Client-side certificates

When consuming a web service it's often necessary that the request is authenticated. Or of the possible authentication forms is using client side certificates. The client side certificate then needs to be configured in each front-end of the environment that will consume the Web Service. 

The client certificate is owned by entity that owns the webservice (that provides it to the customer). Developers are responsible to make sure that the certificate is sent on the requests.

### OutSystems cloud

OutSystems is responsible for the certificate instalation but it's the customer's responsibility to monitor it's expiration and submit a request for the renewal. 

To install a client-side certificate on OutSystems Cloud please follow these [instructions](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Requesting_to_install_client-side_certificates_on_OutSystems_cloud).

### Self-managed environments

Follow this [article](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Add_self_signed_certificate_to_trusted_root_store_on_OutSystems) for instructions on adding the self-signed ceritificate to the trusted root store.

The customer is both responsible for installing the certificate and monitoring it's expiration date.

