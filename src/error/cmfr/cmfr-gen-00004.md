---
summary: <record> with the Id "<input-parameter-value>" already exists.
tags:
locale: en-us
guid: 206291d7-5a4d-436b-b320-d82d28e0861b
---

# OS-CMFR-GEN-00004

## Error message

`<record> with the Id "<input-parameter-value>" already exists.`

## Cause

While trying to execute a create action, the Case Management framework detected that the identifier that was passed as an input parameter matches an existing record.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the value that's being passed as input to the Case Management framework action is correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.

If the action you're trying to execute is an update, change the action to its update, or create or update, counterpart.
