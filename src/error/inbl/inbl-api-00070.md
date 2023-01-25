---
summary: There was an error contacting an internal service.
tags:
locale: en-us
guid: ec9fa64a-a83a-4879-8f07-360d407d6cad
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-INBL-API-00070

## Error message

`There was an error contacting an internal service.`

## Cause

This error usually occurs when there’s an error calling an internal service through HTTPS.  
Typically, this can happen if the server's address (configured in Service Center) can’t be resolved through DNS,
or if the server’s certificate doesn’t match that address.

## Impact

Integration Manager is not able to contact or navigate to Integration Builder.

## Recommended action

Make sure that your server's address is correctly configured in Service Center and make sure that it matches the one in the HTTPS certificate.  
Additionally, you can check the Service Center Error logs for more details.
