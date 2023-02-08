---
summary: The activity couldn't be closed, either because you're missing the required access or it was already closed.
tags:
locale: en-us
guid: 3f78f979-3c62-4f73-a331-09781baf2ee5
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-CMFR-GEN-20008

## Error message

`The activity couldn't be closed, either because you're missing the required access or it was already closed.`

## Cause

While trying to execute the **Case_CloseActivity** action, the Case Management framework detected that either the user making the request doesn't have access to perform the action or the activity was already closed.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the user has access to the activity before using the **Activity_ValidateUserAccess** action of the **CaseServices_API** module.

If the user is performing the action under delegation, make sure to pass into the **DelegatedBy** input parameter the identifier of the user that is delegating.
