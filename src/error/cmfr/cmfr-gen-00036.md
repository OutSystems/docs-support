---
summary: The Case Definition must have an initial status defined.
tags:
locale: en-us
guid: bc90f398-4ce3-4ad8-a047-c8777a949a81
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-CMFR-GEN-00036

## Error message

`The Case Definition must have an initial status defined.`

## Cause

While trying to execute the **Case_Initialize** action, the Case Management framework detected that the case definition for which it was trying to initialize a case instance doesn't have a case status defined as initial.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Fill in the **CaseStatusId** input parameter of the **Case_Initialize** action.

Use the **CaseStatus_CreateOrUpdate** action from the **CaseConfigurations_API** module to create or update a case status with the attribute **IsInitial** set to **True**.
