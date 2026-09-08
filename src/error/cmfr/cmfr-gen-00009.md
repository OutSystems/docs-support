---
summary: OS-CMFR-GEN-00009 error in OutSystems 11 (O11) Case Management Framework occurs when CaseTag_Create finds the tag already linked to the case.
tags:
  - Case Management framework
  - Debugging
  - Troubleshooting
locale: en-us
guid: 2eebed55-459b-454d-8208-4eaf9aa123f9
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
---

# OS-CMFR-GEN-00009

## Error message

`This combination of Case and Tag already exists.`

## Cause

While trying to execute the **CaseTag_Create** action, the Case Management framework detected that the tag which was input was already associated with the case.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
