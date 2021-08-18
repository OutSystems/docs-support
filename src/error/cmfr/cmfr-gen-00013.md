---
summary: It's not possible to fill in both UserId and GroupId attributes.
tags:
---

# OS-CMFR-GEN-00013

## Error message

`It's not possible to fill in both UserId and GroupId attributes.`

## Cause

The Case Management framework detected that both the **UserId** and **GroupId** inputs were filled in an internal action regarding access control, which prevents access control from functioning correctly.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if you're using the correct actions regarding access control and not an internal action. The correct actions are the ones available in the **CaseServices_API** module. If you're already referencing the correct actions, please create a case with [OutSystems Support](https://success.outsystems.com/Support).

## More info

For information on access permissions, see [Managing access to cases](https://success.outsystems.com/Documentation/Case_Management/Managing_access_to_cases).
