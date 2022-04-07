---
summary: Couldn't complete the Takeover. Either the user is missing access or the activity isn't assigned to anyone.
tags:
locale: en-us
guid: 8c226258-db91-4ac9-93b0-ff5ed273daf2
---

# OS-CMFR-GEN-20005

## Error message

`Couldn't complete the Takeover. Either the user is missing access or the activity isn't assigned to anyone.`

## Cause

While trying to execute the **Case_TakeoverActivity** action, the Case Management framework detected that either the user making the request doesn't have access to the activity or the activity isn't currently assigned to any user.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the user has access to the activity before using the **Activity_ValidateUserAccess** action of the **CaseServices_API** module.

To assign the activity to a user, use the **Activity_AssignToUser** action from the **CaseServices_API** module instead.
