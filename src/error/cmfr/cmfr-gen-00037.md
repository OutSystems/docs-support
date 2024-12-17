---
summary: FromDate must be set to a date before ToDate.
tags: error handling, date validation, input parameter validation, case management, debugging
locale: en-us
guid: c5e09327-2de9-4a50-b69e-f5fa6b6a55b6
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

# OS-CMFR-GEN-00037

## Error message

`FromDate must be set to a date before ToDate.`

## Cause

While trying to execute the **Delegation_Create** or **Delegation_Update** actions, the Case Management framework detected that the **FromDate** and **ToDate** input parameter values aren't properly set.

## Impact

The Case Management framework isn't able to successfully execute the action.

## Recommended action

Make sure that the **FromDate** value is set to a date before the **ToDate** value. Use Service Studio's Debugger to check the input parameter's value at the date of execution.
