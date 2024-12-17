---
summary: This user doesn't have any active delegations for you at the moment.
tags: error handling, case management, debugging, outsystems
locale: en-us
guid: e67333aa-8437-43df-b048-441b5a5f30bd
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - full stack developers
  - frontend developers
  - mobile developers
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-20007

## Error message

`This user doesn't have any active delegations for you at the moment.`

## Cause

While trying to execute the **DEPRECATED_Case_GetActivities** or **DEPRECATED_Case_GetCases** service actions, the Case Management framework detected that the **DelegatedBy** input parameter didn't evaluate to a valid delegation for the user making the request.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
