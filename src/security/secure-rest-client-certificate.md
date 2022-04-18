---
summary: Configure you application to secure Rest APIs with client side certificates authentication
Tags: 
locale: en-us
guid: 54604809-efce-4a72-b05a-2459b4ba5aa9
app_type: traditional web apps, mobile apps, reactive web apps
---

# Secure Rest APIs with client side authentication

To secure a consumed REST APIs with authentication via client side certificates you’ll need to send the client side certificate on the request to the server.
 
## Configuring your application

This can be achieved with the use of the [REST Extensibility API](https://success.outsystems.com/Documentation/11/Reference/OutSystems_APIs/REST_Extensibility_API):

1. Create an extension and develop application code to use the client-side certificate.
1. In the extension you'll need to include the installation path of your client certificates:
    * For OutSystems cloud, check [this document](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Requesting_to_install_client-side_certificates_on_OutSystems_PaaS) on how to request the certificate installation and obtain the path from OutSystems Support.
    * For self-managed environments, check [here](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Installing_client_side_certificates_on_on-premises_environments) for the instructions to install the certificate.
1. Customize the request with the [OnBeforeRequest](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs/Advanced_Customizations) property of your REST API before making the web request call. 
1. If necessary, force the usage of a specific TLS version by using `ServicePointManager.SecurityProtocol = System.Net.SecurityProtocolType`. Check the code sample for details on the **SetTLSVersion** action. This might necessary when connecting to legacy servers.


## Sample code

An example of this implementation is available at OutSystems Forge, on the [HTTPS Consumer component](https://www.outsystems.com/forge/component-overview/3591/https-consumer) that already reflects the actions above.



