---
summary: For OutSystems cloud, when you need to consume webservices that require authentication using client-side certificates, request OutSystems Support to install the certificates on the front-end servers.
tags: support-Cloud_Platform
---

# Requesting to install client-side certificates on OutSystems cloud

When consuming webservices external to the OutSystems servers and considering the [Client-server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model), the OutSystems servers are, in this scenario, the **client-side**, and the servers that host the webservice, the **server-side**.

## Applicable use case

When the server-side requires authentication via a certificate, the client-side needs to be configured so that it bears the certificate to be able to send it on it’s requests to the server.

 All the front-ends of the environment need to have the certificate configured.
For OutSystems cloud environments, this operation is performed by OutSystems support. 

This option is available depending on your subscription, check here for more details about [Cloud service delivery requiring direct assistance from OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Cloud_services_catalogue).

## Requesting the service

You’ll need to [open a support case](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/02_How_to_Open_a_Support_Case) and:

* Provide the client-side certificate:
    * in .PFX format, with password
    * any other required root certificates, in .CER format, if not yet included in the .PFX

* Make sure to be clear about what environments should the certificate be installed in.

## What will OutSystems deliver 

OutSystems staff installs the certificate in all the front-ends and notifies you once the operation is complete. 
The path to the certificate is provided so that you can use it in your integrations. 


## Using the certificate on integrations
For instructions on how to secure your integrations with client side certificates authentication check:

[Secure Rest APIs with client side authentication](https://success.outsystems.com/Support/Security/Secure_Rest_APIs_with_client_side_authentication)

[SOAP: Authenticate using a client certificate](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Use_Advanced_Extensibility/Example%3A_Authenticate_using_a_client_certificate)
