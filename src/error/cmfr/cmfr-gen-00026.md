---
summary: Access permissions for that Case Definition have already been granted to that <user/group>.
tags:
locale: en-us
guid: 96307f01-fa1c-4478-b43f-aea3e54655e5
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-CMFR-GEN-00026

## Error message

`Access permissions for that Case Definition have already been granted to that <user/group>.`

## Cause

While trying to create an access control record for a case definition, the Case Management framework detected that the user/group has already been granted access to the selected case definition.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
