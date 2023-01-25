---
summary: We couldn't find any entities.
tags:
locale: en-us
guid: 80d3e7fa-7c18-4554-8d22-fddcf981fd0f
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-GEN-00016

## Error message

`We couldn't find any entities.`

## Cause

While trying to execute the **GetBusinessEntityAttributes**, **Email_ProcessPlaceholders**, or the **Email_Send** actions, the Case Management framework detected that the case definition which was passed as input doesn't have any entities associated with it.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
