---
summary: You need <write/read> access to the Case to perform the <action-name> action.
tags:
locale: en-us
guid: cade7016-3ae2-4851-99e7-712814be071c
---

# OS-CMFR-GEN-20002

## Error message

`You need <write/read> access to the Case to perform the <action-name> action.`

## Cause

While trying to execute an action, the Case Management framework detected that the access control feature is turned on and the user making the request doesn't have the correct level of permissions to perform the action.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Grant the user the appropriate level of permissions using one of the following actions of the **CaseServices_API**:

* **CaseDefinition_GrantAccessToGroup**
* **CaseDefinition_GrantAccessToUser**
* **Case_GrantAccessToGroup**
* **Case_GrantAccessToUser**

## More info

For information about access permissions, see [Managing access to cases](https://success.outsystems.com/Documentation/Case_Management/Managing_access_to_cases).
