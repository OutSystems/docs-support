---
summary: Understand, troubleshoot and resolve the error 'Could not establish trust relationship for the SSL/TLS secure channel' in webservices.
---

# 'Could not establish trust relationship' in webservices

## Symptoms

When **consuming** a web service, you're getting the following error:

```Server was unable to process request. ---> The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel.```

<div class="info" markdown="1">

OutSystems servers must have a valid SSL certificate issued by a public Certificate Authority, as described in [OutSystems system requirements](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_system_requirements).
If you encounter this error while **exposing** a webservice, make sure that your OutSystems servers have that type of certificate.
</div>

## Cause

This is caused by an invalid or untrusted certificate on the server that exposes the webservice you're trying to consume.

It happens often when integrating in non-productive environments, since the certificates installed on those webservers are usually self-signed.

### Identify the cause

* Navigate to the service URL using a browser, and check for certificate errors. The error message displayed by the browser will help you troubleshoot what's causing the error. If you don't see any certificate error on your local browser, repeat the test using a browser installed on the server with the problem.

    The following example shows an invalid certificate:

    ![Invalid Certificate](images/no-trust-relationship-ssltls.png)

* Click on **Certificate** to see the details.

    The following example shows a certificate that is invalid because it expired:

    ![Expired Certificate](images/no-trust-relationship-ssltls_1.png?width=350)

## Resolution

The resolution depends on the what's causing the SSL certificate validation to fail. The most common reasons and their resolutions are:

| Cause | Resolution |
|:------|:-----------|
| The hostname used in the URL doesn't match the name that's on certificate. | Make sure the URL you're using and the URL on the **Issued to** field of the certificate are the same. |
| The certificate expired. | Install a valid certificate, or contact the support of the system you're trying to integrate with. |
| The Certificate Root Authority that issued the certificate is not trusted by the server. | Make sure to add the certificate to the trusted store on OutSystems servers. Check the instructions:<ul><li>[For OutSystems cloud](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Add_certificate_to_trusted_root_store_in_OutSystems_cloud).</li><li>[For self managed environments](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Add_self_signed_certificate_to_trusted_root_store_on_OutSystems).</li></ul> |
| The certificate is self-signed. | Make sure to install the certificate as trusted. Check the instructions:<ul><li>[For OutSystems cloud](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Add_certificate_to_trusted_root_store_in_OutSystems_cloud).</li><li>[For self managed environments](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Add_self_signed_certificate_to_trusted_root_store_on_OutSystems).</li></ul> |

