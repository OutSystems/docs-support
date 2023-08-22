---
summary: <record> wasn't found.
tags:
locale: en-us
guid: 0dfe737e-6cb9-41a0-87ff-3be28aaf5b1a
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-CMFR-GEN-00002

## Error message

`<record> wasn't found.`

## Cause

While trying to execute an action, the Case Management framework wasn't able to find the data record the input parameter refers to.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the value that is being passed as input to the Case Management framework action is correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution. If that doesn't solve the issue, try to reference the entity that matches the input parameter and check if the record exists, otherwise, create the record. For example, if the input is **CaseId** (case Identifier), reference the entity case.
