---
summary: It looks like you don't have access to the activity.
tags:
locale: en-us
guid: 37fba356-87fc-4e24-b795-944b0ba1dedb
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-GEN-20003

## Error message

`It looks like you don't have access to the activity.`

## Cause

While trying to execute an action related to an activity, the Case Management framework detected that the user making the request doesn't have access to the activity. This happened because of one of these reasons:

* The user isn't assigned to the activity.
* The user doesn't belong to the group the activity is assigned to.
* There isn't a valid delegation that would allow the user to access the activity.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the user has access to the activity before using the **Activity_ValidateUserAccess** action of the **CaseServices_API** module.

If the user is performing the action under delegation, make sure to pass into the **DelegatedBy** input parameter the identifier of the user that is delegating.
