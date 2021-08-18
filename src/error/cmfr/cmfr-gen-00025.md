---
summary: Not all <records> reference the same <record>. Change them accordingly.
tags:
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
