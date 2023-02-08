---
platform-version: o11
summary: Recomended actions for the error "An error occurred while getting a token from the Microsoft Identity Platform" in Integration Builder.
tags:
locale: en-us
guid: 70184542-5898-4a4d-aac5-13733efe603a
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-INBL-API-00038

## Error message

`An error occurred while getting a token from the Microsoft Identity Platform: <error details>`

## Cause

A Dataverse, Dynamics or SharePoint connection in Integration Manager has a matching **App Registrations** in Azure AD. Typically, this error is caused by a configuration problem on the **App Registration** in Azure AD.

Common configuration problems are:

* The App Registration's certificate has expired.
* For connections that were created manually, the App Registration's certificate doesn't match the certificate uploaded in Integration Manager.

## Impact

The Dataverse, Dynamics, or SharePoint connector fails to get data from the external system.

## Recommended action

* If you are an Azure AD administrator, in Integration Manager, create a new connection automatically. This should ensure its configuration is correct.
* If you created the connection manually:
	1. Ensure the Azure AD App Registration's Application, Object and Tenant IDs, match the values of the connection in Integration Manager.
	1. Ensure that the certificate uploaded to the App Registration is the public part of the certificate uploaded to Integration Manager.
