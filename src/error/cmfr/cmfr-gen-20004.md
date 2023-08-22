---
summary: The activity must be assigned to a user before it can be released.
tags:
locale: en-us
guid: 7994c79c-d2d7-42f3-b874-e2131968d78c
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
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
