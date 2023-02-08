---
summary: There was an error contacting an internal service.
tags:
locale: en-us
guid: 3890e4cb-b087-4422-9e09-c7e2337add12
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-INBL-API-00069

## Error message

`There was an error contacting an internal service.`

## Cause

Integration Manager failed to access an internal service using HTTPS.
This can happen if the server's address (configured in Service Center) can’t be resolved through DNS, or if the server’s certificate doesn’t match that address. 

## Impact

Integration Manager is not able to contact or navigate to Integration Builder.

## Recommended action

Make sure that your server's address is correctly configured in Service Center and make sure that it matches the one in the HTTPS certificate.
Additionally, you can check the Service Center Error logs for more details.
