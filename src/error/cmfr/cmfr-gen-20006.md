---
summary: Couldn't log in. Make sure you're accessing as a sample user.
tags:
locale: en-us
guid: bc46ebc1-9248-41d3-92f5-b3f53afc304c
---

# OS-CMFR-GEN-20006

## Error message

`Couldn't log in. Make sure you're accessing as a sample user.`

## Cause

While trying to execute the **SampleUser_Login** action, the Case Management framework detected that the user identifier passed as input to this action belongs to a user that isn't a sample user.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure the user identifier passed in the **UserId** input parameter of the action belongs to a sample user.

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
