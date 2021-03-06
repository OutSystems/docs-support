---
summary: <record> wasn't found.
tags:
---

# OS-CMFR-GEN-00002

## Error message

`<record> wasn't found.`

## Cause

While trying to execute an action, the Case Management framework wasn't able to find the data record the input parameter refers to.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the value that is being passed as input to the Case Management framework action is correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution. If that doesn't solve the issue, try to reference the entity that matches the input parameter and check if the record exists, otherwise, create the record. For example, if the input is **CaseId** (case Identifier), reference the entity case.
