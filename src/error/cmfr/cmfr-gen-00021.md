---
summary: We couldn't find a pairing for <case/case definition> and Milestone Definition.
tags:
---

# OS-CMFR-GEN-00021

## Error message

`We couldn't find a pairing for <case/case definition> and Milestone Definition.`

## Cause

While trying to execute the **Case_IsMilestoneAchieved** or **CaseDefinition_UnlinkFromMilestoneDefinition** actions, the Case Management framework wasn't able to find a record matching the case/case definition and milestone definition which were input.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
