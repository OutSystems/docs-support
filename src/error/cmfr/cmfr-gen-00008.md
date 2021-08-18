---
summary: There's no access control for that <user/group>/<case/case definition> pairing.
tags:
---

# OS-CMFR-GEN-00008

## Error message

`There's no access control for that <user/group>/<case/case definition> pairing.`

## Cause

When trying to update or revoke the user or group access to a case or case definition, the Case Management framework detected there was no access control record matching the provided pairing.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
