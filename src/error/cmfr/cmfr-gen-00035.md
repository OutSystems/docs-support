---
summary: ExternalRequesterDetails and CaseRequesterUserId input parameters cannot be both filled in. Send the CaseRequesterUserId parameter when the requester is an internal user and the ExternalRequesterDetails when the requester is external.
tags:
locale: en-us
guid: dd233fe7-e622-4998-ad2c-0973db37670a
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-CMFR-GEN-00035

## Error message

`ExternalRequesterDetails and CaseRequesterUserId input parameters cannot be both filled in. Send the CaseRequesterUserId parameter when the requester is an internal user and the ExternalRequesterDetails when the requester is external.`

## Cause

While trying to execute the **Case_Initialize** action, the Case Management framework detected that both the **ExternalRequesterDetails** input structure and **CaseRequesterUserId** input were filled in. Only one of them should be filled in.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Fill in the **CaseRequesterUserId** input parameter when the requester is an internal user or the **ExternalRequesterDetails** input structure when the requester is external.

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
