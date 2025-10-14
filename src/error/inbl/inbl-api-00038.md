---
platform-version: o11
summary: Recomended actions for the error "An error occurred while getting a token from the Microsoft Identity Platform" in Integration Builder.
tags: azure ad, app registration, certificate management, token authentication, error handling
locale: en-us
guid: 70184542-5898-4a4d-aac5-13733efe603a
app_type: traditional web apps, mobile apps, reactive web apps
figma:
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - integration builder
coverage-type:
  - unblock
---

# OS-INBL-API-00038

## Error message

`An error occurred while getting a token from the Microsoft Identity Platform: <error details>`

## Cause

A Dataverse, Dynamics or SharePoint connection in Integration Manager has a matching **App Registrations** in Microsoft Entra. Typically, this error is caused by a configuration problem on the **App Registration** in Microsoft Entra.

Common configuration problems are:

* The App Registration's certificate has expired.
* For connections that were created manually, the App Registration's certificate doesn't match the certificate uploaded in Integration Manager.

## Impact

The Dataverse, Dynamics, or SharePoint connector fails to get data from the external system.

## Recommended action

* If you are an Microsoft Entra administrator, in Integration Manager, create a new connection automatically. This should ensure its configuration is correct.
* If you created the connection manually:

  1. Ensure the Microsoft Entra App Registration's Application, Object and Tenant IDs, match the values of the connection in Integration Manager.
  1. Ensure that the certificate uploaded to the App Registration is the public part of the certificate uploaded to Integration Manager.
