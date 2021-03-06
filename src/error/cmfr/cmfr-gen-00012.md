---
summary: The milestone has already been achieved.
tags:
---

# OS-CMFR-GEN-00012

## Error message

`The milestone has already been achieved.`

## Cause

While trying to execute the **Milestone_SetAchieved** action, the Case Management framework detected that the milestone which was input is already set to the achieved status.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
