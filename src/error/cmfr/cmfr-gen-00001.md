---
summary: The <input-parameter> you've entered is either incorrect or null.
tags: error handling, debugging, case management framework, parameter validation, application troubleshooting
locale: en-us
guid: 1c906e50-cee0-4a8a-a135-152791ce2492
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - frontend developers
  - full stack developers
  - backend developers
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-00001

## Error message

`The <input-parameter> you've entered is either incorrect or null.`

## Cause

While trying to execute an action, the Case Management framework detected an incorrect or null input parameter.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the value that's being passed as input to the Case Management framework's action is correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
