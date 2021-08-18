---
summary: The activity must be assigned to a user before it can be released.
tags:
---

# OS-CMFR-GEN-20004

## Error message

`The activity must be assigned to a user before it can be released.`

## Cause

While trying to execute the **Case_ReleaseActivity** action, the Case Management framework detected that the activity passed as input is not currently assigned to any user, therefore making it impossible to be released.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the activity to be passed as input to the **Case_ReleaseActivity** action is assigned to a user.

To assign the activity to a user, use the **Activity_AssignToUser** action from the **CaseServices_API** module.
