---
summary: The user you are trying to delegate from is not a member of the selected group.
tags:
---

# OS-CMFR-GEN-00038

## Error message

`The user you are trying to delegate from is not a member of the selected group.`

## Cause

While trying to execute the **Delegation_Create** or **Delegation_Update** actions, the Case Management framework detected that the **FromUserId** input value belongs to a user that isn't a member of the **FromGroupId** that was input.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure the user passed in the **FromUserId** input parameter is a member of the group passed in the **FromGroupId** input parameter. Use Service Studio's Debugger to check the input parameter's value at the date of execution.
