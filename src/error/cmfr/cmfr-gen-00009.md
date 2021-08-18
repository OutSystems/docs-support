---
summary: This combination of Case and Tag already exists.
tags:
---

# OS-CMFR-GEN-00009

## Error message

`This combination of Case and Tag already exists.`

## Cause

While trying to execute the **CaseTag_Create** action, the Case Management framework detected that the tag which was input was already associated with the case.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
