---
summary: Set a destination to send the email.
tags:
---

# OS-CMFR-GEN-00027

## Error message

`Set a destination to send the email.`

## Cause

While trying to execute the **Email_Send** action, the Case Management framework detected that none of the destination inputs were filled in.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure you fill in at least one of the destination inputs and try again.

The destination inputs are:

* **To**
* **Cc**
* **Bcc**
* **ToGroupId**
* **CcGroupId**
* **BccGroupId**
