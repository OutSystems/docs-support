---
summary: "OS-CMFR-GEN-00022 error in OutSystems 11 (O11) Case Management framework occurs when a duplicate case status transition is detected between CaseStatusId values."
tags:
  - Case Management framework
  - Debugging
  - Troubleshooting
locale: en-us
guid: 52d4bebb-194e-43c8-ac48-70cf94ae22dc
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - Developer
  - Front-end developer
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-00022

## Error message

`That Case Status transition already exists.`

## Cause

While trying to create or update a case state machine record, the Case Management framework detected that a transition between the selected **CaseStatusId** and **NextCaseStatusId** attributes already exists.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
