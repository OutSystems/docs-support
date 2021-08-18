---
summary: Unknown activity action. It must match one from ActivityAction.
tags:
---

# OS-CMFR-GEN-00032

## Error message

`Unknown activity action. It must match one from ActivityAction.`

## Cause

While trying to execute the **Case_PerformActionActivity** action, the Case Management framework detected that the **ActivityActionId** input doesn't match any known activity action.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the value that is being passed as input to the Case Management framework action is correct and belongs to the **ActivityAction** static entity **CM_ProcessServices_BL** module. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
