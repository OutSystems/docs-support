---
summary: Either CanView or CanEdit must be set to True.
tags:
locale: en-us
guid: 862516ae-30d5-4353-8c6a-db12a33a37b3
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-CMFR-GEN-00014

## Error message

`Either CanView or CanEdit must be set to True.`

## Cause

While trying to execute the **DEPRECATED_Case_AddAccessToGroup** or **DEPRECATED_Case_AddAccessToUser** actions, the Case Management framework detected that both the **CanView** and **CanEdit** inputs were set as **False**.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that at least one of the inputs is set to **True**. Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
