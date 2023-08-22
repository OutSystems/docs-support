---
summary: <record/attribute> already exists for that <record/attribute>.
tags:
locale: en-us
guid: 2810c5b9-4ce4-4ac9-b221-cfbe70ee32f1
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-CMFR-GEN-00007

## Error message

`<record/attribute> already exists for that <record/attribute>.`

## Cause

While trying to exectute a create or update action, the Case Management framework detected that a record already exists with the same attribute/record.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
