---
summary: The number of minutes must be greater than or equal to zero.
tags: error handling, debugging, case management framework, calendar management, input validation
locale: en-us
guid: b97679ee-618c-4492-a00d-6f9d8435b13d
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-00006

## Error message

`The number of minutes must be greater than or equal to zero.`

## Cause

While trying to execute the **Calendar_GetEndDate** action, the Case Management framework detected that the **Minutes** input parameter value was set to a value below zero.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the **Minutes** value is set to a value equal to or greater than zero. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
