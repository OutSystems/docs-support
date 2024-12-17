---
summary: The milestone has already been achieved.
tags: case management framework, error handling, debugging, outsystems development, application lifecycle management
locale: en-us
guid: 69d7003c-fe01-4ac7-8df9-2122cbe0e90d
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - full stack developers
  - frontend developers
  - backend developers
  - architects
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-00012

## Error message

`The milestone has already been achieved.`

## Cause

While trying to execute the **Milestone_SetAchieved** action, the Case Management framework detected that the milestone which was input is already set to the achieved status.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
