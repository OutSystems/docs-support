---
summary: It looks like you don't have access. Make sure you're logged in with a registered user.
tags:
locale: en-us
guid: bb0bbe53-0079-4942-8ebf-8885804c910f
---

# OS-CMFR-GEN-20001

## Error message

`It looks like you don't have access. Make sure you're logged in with a registered user.`

## Cause

While trying to execute a **Get** service action from the **CaseServices_API**, the Case Management framework detected that there wasn't a user with an active session in the platform. These service actions require a logged-in user for security reasons.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the user logs in before executing these actions.
