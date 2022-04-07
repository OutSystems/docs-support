---
summary: We found more than one record for this transition.
tags:
locale: en-us
guid: 758ad019-6558-49bb-92ea-40581bfbca9e
---

# OS-CMFR-GEN-00024

## Error message

`We found more than one record for this transition.`

## Cause

While executing the **CaseStateMachine_GetByTransition** action the Case Management framework detected more than one record matching the given **CaseStatusId** and **NextCaseStatusId** attributes.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Reference the **CaseStateMachine** entity, view data, and filter the results with the same **CaseStatusId** and **NextCaseStatusId** pair that triggered this error message. Select one of the results and call the **CaseStateMachine_Update** action with that identifier, changing the **IsActive** attribute to **False**.

If this doesn't work or you are not able to perform this action, please create a case with [OutSystems Support](https://success.outsystems.com/Support).
