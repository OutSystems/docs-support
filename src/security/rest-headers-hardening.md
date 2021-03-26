---
summary:
tags:
---

# REST Headers security hardening

When customizing the request headers of a consumed REST API the list of headers sent in the request is not the same as the final state of the ```CustomizedRequest``` list of headers.

Although the headers are being observed to be removed when debugging the application in the Service Studio, it is impossible to remove headers in the ```OnBeforeRequest``` callback of consumed REST services.

## Why is this important?

This can cause potential security vulnerability, because  if you use the headers to pass sensitive information, it becomes visible to the server, in logs and potentially during network transit, if sent over HTTP.

## Potential impact on applying the security hardening solution

The potential impact of the applying the mentioned fix can be that consumed REST services can expect problems during calling the REST methods in runtime, since before the fix,  the headers removal operations are not executed correctly.

This can produce differences only visible at runtime. Depending on how the invoked service is implemented, and whether it was using the supposably removed headers or not, some changes in behavior can occur. 

Please do the following validations before changing this in Production environments.

### Verify if you can proceed with the security hardening

In order to verify if you can apply the security hardening , follow the next steps:

1. Go through all REST consumption services. For each REST consumption service, check if the ```OnBeforeRequest``` callback is included.

1. If the ```OnBeforeRequest``` callback is used, check if there were removed headers in the flow: 
    1. Analyse if the ```CustomizedRequest.headers``` list does not have headers that are present  in  the input headers of the flow, present in the list ```Request.headers```. This can be done by using the ```ListRemove``` action, for instance.

1. If there’s no REST consumption service in this situation, it should be safe to activate the security hardening parameter. 

1. Otherwise, it is recommended to test affected services to detect any potential impact and do the necessary changes.

## How to apply the security hardening on REST headers
To make sure that the headers are removed:

1. Access the Forge component [Factory Configuration](https://www.outsystems.com/forge/component-overview/25/factory-configuration).

1. Change the **Allow headers removal inside onBeforeRequest REST callback** setting to  **Enabled**. 

1. Republish your modules to respect the new value.
