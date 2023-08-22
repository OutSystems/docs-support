---
summary: There's no access control for that <user/group>/<case/case definition> pairing.
tags:
locale: en-us
guid: ea7908f7-0891-47cf-bb24-63e201da0baa
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
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
