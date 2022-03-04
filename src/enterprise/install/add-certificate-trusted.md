---
summary: Learn how to install certificates, so that you can make HTTPS requests to servers that use self-signed certificates or certificates not trusted by your operating system.
---


# Add self signed certificate to trusted root store on OutSystems

<div class="info" markdown="1">

We've been working on this article, give us your feedback by voting.

</div>

When consuming a web service integrating with other systems over HTTPS, the server hosting such service may be using a self signed certificate (for example, for non productive web services).

Self signed certificates or any type of certificate that isn't universally recognized (such as certificates issued by a public certificate authority are) must be added to the trusted root store of the servers that host the Platform Server.
This will allow to successfully establish the trust relationship.

When this step isn't done, errors like ```Could not establish trust relationship for the SSL/TLS``` may occur.

<div class="info" markdown="1">

OutSystems **Production** servers must have a valid SSL certificate issued by a public Certificate Authority, as described in [OutSystems system requirements](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_system_requirements).
</div>

For OutSystems Cloud environments check [this article](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Add_certificate_to_trusted_root_store_in_OutSystems_PaaS) instead.


## Certificate installation

1. Open the Microsoft Management Console (Start > MMC);
1. Provide the self-signed certificate:
    1. Choose **File** > **Add/Remove Snap-in**;
    1. in the standalone tab, choose Add;
    1. choose the Certificates snap-in > **Add**;
    1. in the wizard, choose the **Computer Account** > **Local Computer**;
    1. press **Finish** to end the wizard;
    1. close the Add/Remove Snap-in dialog;
    1. Navigate to **Certificates (Local Computer)**;
        1. choose the Trusted Root Certification Authorities store to import the certificate;
        1. right click the store and choose **All Tasks** > **Import**  ;
        1. Follow the wizard and provide the certificate file you have.


## Export the certificate

Export the public certificate to the following path: D:\Certificates:

1. Still on the Microsoft Management Console;
1. choose **Certificates (Local Computer)** > select the folder where the certificate was installed > **Certificates**;
1. right-click on the certificate > **All Tasks** > **Export**;
1. choose to export the certificate without the private key;
1. choose the format to be DER encoded binary X.509 (CER);
1. save the file into D:\Certificates.

For environments with more than one front-end, these instructions must be followed on all front-end servers.



