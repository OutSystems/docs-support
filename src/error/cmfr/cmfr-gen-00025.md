---
summary: Not all <records> reference the same <record>. Change them accordingly.
tags:
locale: en-us
guid: fc9d78d9-1345-411d-91f8-72b2d8652cab
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-GEN-00025

## Error message

`Not all <records> reference the same <record>. Change them accordingly.`

## Cause

While executing one of the **Bootstrap** actions, the Case Management framework detected that not all records reference the same case definition.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the **CaseDefinitionId** attribute of all records that are passed into the action as input reference the same case definition.
