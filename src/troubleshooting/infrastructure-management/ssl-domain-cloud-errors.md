---
summary: Check here the possible errors that you can get when validating your SSL domain certificate in OutSystems Cloud and how to proceed for each case.
tags:
locale: en-us
guid: 7a4d2b58-5b42-4f33-be80-e3734d161ea8
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Possible errors when validating your SSL domain certificate

During the process to set up [your own SSL domain in OutSystem Cloud](https://success.outsystems.com/Documentation/11/Setup_and_maintain_your_OutSystems_infrastructure/Setting_Up_OutSystems/Use_your_SSL_domain_in_OutSystems_Cloud) you must add the new domain certificate on LifeTime for validation.

This article describes the possible errors that you can get during the [validation step of your certificate](https://success.outsystems.com/Documentation/11/Setup_and_maintain_your_OutSystems_infrastructure/Setting_Up_OutSystems/Use_your_SSL_domain_in_OutSystems_Cloud#validate-certificate), and the guidelines on how to proceed for each case.

## Errors description

Message
:   `Unable to extract the public key certificate from the uploaded file. Make sure you upload a valid .PFX file.`

Cause
:   There was an error extracting the public key certificate from the .PFX certificate file you have uploaded.

Recommendation
:   Make sure you upload a .PFX certificate file correctly generated with your public key certificate, private key and chain.

---

Message
:   `Unable to extract the private key from the uploaded file. Make sure you upload a valid .PFX file.`

Cause
:   There was an error extracting the private key from the .PFX certificate file you have uploaded.

Recommendation
:   Make sure you upload a .PFX certificate file correctly generated with your public key certificate, private key and chain.

---

Message
:   `The password for the uploaded file is missing or incorrect. Make sure you provide the correct password.`

Cause
:   The .PFX certificate file you have uploaded is protected with a password, and you didn’t provide the correct password or the password is empty.

Recommendation
:   Make sure you provide the correct password for your .PFX certificate file. Otherwise, generate another .PFX certificate file that’s not protected with a password.

---

Message
:   `The password for the certificate’s private key is incorrect. Make sure you provide the correct password.`

Cause
:   The private key of your .PEM certificate is protected with a password, and you didn’t provide the correct password.

Recommendation
:   Make sure you provide the correct password for the private key of your .PEM certificate.

---

Message
:   `The password for the certificate’s private key is missing. Make sure you provide the PEM password.`

Cause
:   The private key of your .PEM certificate is protected with a password, and you didn’t provide the password.

Recommendation
:   Make sure you provide the password for the private key of your .PEM certificate.

---

Message
:   `The certificate you uploaded has expired. Make sure you upload a valid certificate.`

Cause
:   The certificate you have provided has already expired.

Recommendation
:   Make sure you provide a valid certificate. To validate the expiration date of your certificate, contact the Certificate Authority that issued your certificate.

---

Message
:   `Unable to find the private key. Make sure the private key file has a recommended format.`

Cause
:   We could't find the private key in the certificate you uploaded.

Recommendation
:   Make sure to provide the private key in the correct format. If you uploaded a ZIP file, make sure the private key file has the correct file type.

---

Message
:   `The private key doesn’t match the public key certificate. Make sure you provide a matching key pair.`

Cause
:   The public key certificate and the private key you provided don’t match.

Recommendation
:   Make sure you provide a valid key pair: the private key must match your public key certificate.

---

Message
:   `There are invalid files in the uploaded file. Make sure the ZIP file contains only the necessary files.`

Cause
:   The ZIP file you uploaded contains files that we're not able to read.

Recommendation
:   To avoid issues related to the certificate format, use PEM or PFX certificates. If that’s not suitable and you need to submit a ZIP bundle, make sure you exclude all the unnecessary files from the ZIP file.

---

Message
:   `Unable to find the public key certificate. Make sure you provide a valid public key certificate.`

Cause
:   We could't find the public key certificate.

Recommendation
:   Make sure you provide the public key certificate. To avoid issues related to the certificate format, use PEM or PFX certificates. If that’s not suitable and you need to submit a ZIP bundle, make sure you upload the public key certificate.

---

Message
:   `Chain error: <error description>`

Cause
:   The certificate chain isn't correct.

Recommendation
:   Make sure the intermediate and root certificates are complete and correct.
