---
summary: This certificate expired on <expiration_date>. Create a new certificate or check our documentation to know how.
tags: mabs sig error_code
guid: 3696cb6f-2ac5-47f4-a678-71b729b6fa01
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-SIG-40018

## Error message

`This certificate expired on <expiration_date>. Create a new certificate or check our documentation to know how.`

## Cause

This error occurs when generating an iOS app and the certificate is expired.

## Impact

Users can't generate the application package.

## Recommended action

Renew the certificate used to sign the application or upload a valid one (ensuring it has a valid expiring date) and retry.

Find more information about generating your certificate file [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#create-a-certificate).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40018).
