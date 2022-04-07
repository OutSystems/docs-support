---
summary: This is an automated message returned by the external system "The request has been refused. Verify that the logged-in user has appropriate permissions. If the error code is REQUEST_LIMIT_EXCEEDED, you’ve exceeded API request limits in your org.
tags:
locale: en-us
guid: 0f597359-a284-4333-9c8d-188d2bca134f
---

# OS-INBL-API-00021

## Error message

`This is an automated message returned by the external system: "The request has been refused. Verify that the logged-in user has appropriate permissions. If the error code is REQUEST_LIMIT_EXCEEDED, you’ve exceeded API request limits in your org."`

## Cause

This is a Salesforce error message returned when Integration Builder tried to confirm the Salesforce user information entered in the Connection creation form.
This usually means the Salesforce account used to create the Connection doesn't have the necessary permissions.

## Impact

Can't connect to Salesforce to verify the user information and create the connection.

## Recommended action

Either authorize Integration Manager using another Salesforce account, or set up a Connected App in Salesforce manually and create a connection by filling in the necessary information in a form in Integration Manager.
