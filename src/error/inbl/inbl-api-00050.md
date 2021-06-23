---
summary: This is an automated message returned by the external system The session ID or OAuth token used has expired or is invalid. The response body contains the message and errorCode.
tags:
---

# OS-INBL-API-00050

## Error message

`This is an automated message returned by the external system: The session ID or OAuth token used has expired or is invalid. The response body contains the message and errorCode.`

## Cause


This is a Salesforce error message returned when Integration Builder tried to call Salesforce API. 
Typically, this means the authorization to access Salesforce that was granted to Integration builder by the user has expired, or was revoked.

## Impact

Integration Builder can't create the integration since it's unable to retrieve metadata from Salesforce.

## Recommended action

Repeat the Authorization step for a Salesforce integration, in the Integration Builder. If that doesn't solve the issue, contact a Salesforce system administrator.
