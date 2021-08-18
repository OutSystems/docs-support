---
summary: FromDate must be set to a date before ToDate.
tags:
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
