---
summary: "OS-CMFR-GEN-00001 OutSystems 11 (O11) error: fix incorrect or null input parameters in Case Management Framework actions."
tags:
  - Case Management framework
  - Debugging
  - Troubleshooting
locale: en-us
guid: 1c906e50-cee0-4a8a-a135-152791ce2492
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - Front-end developer
  - Developer
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
topic:
  - fix-invalid-input
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
