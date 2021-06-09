---
summary:
tags:
en_title: OS-INBL-API-00070
---

# OS-INBL-API-00070 - There was an error contacting an internal service.

## Error message

`There was an error contacting an internal service.`

## Cause

This error usually occurs when there’s an error calling an internal service through HTTPS.  
Typically, this can happen if the server's address (configured in Service Center) can’t be resolved through DNS,
or if the server’s certificate doesn’t match that address.

## Impact

Integration Manager is not able to contact or navigate to Integration Builder.

## Recommended action

Make sure that your server's address is correcly configured in Service Center and make sure that it matches the one in the HTTPS certificate.  
Additionaly you can check the Service Center Error logs for more details.
