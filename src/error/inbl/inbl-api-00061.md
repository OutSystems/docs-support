---
summary: Internal server error. If this problem persists, contact OutSystems support.
tags:
locale: en-us
guid: 1bd71502-9292-4c96-810d-b233baa24794
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-INBL-API-00061

## Error message

`Internal server error. If this problem persists, contact OutSystems support.`

## Cause

This error occurs when there's an unexpected error on Integration Manager's API.
The most frequent cause for such errors are broken references between Integration Manager and the components it uses.

## Impact

Users are not able to sign into Integration Manager.

## Recommended action

Use Service Center to republish the Integration Manager application and any modules it consumes. A good way to ensure that all modules are published in the correct order is to create a Solution in Service Center, add the "OsIntegrationManager" module to the components and check the "include dependencies as components" checkbox. Then publish the running version of the Solution.
