---
summary: Not all <records> reference the same <record>. Change them accordingly.
tags: error handling, case management, data consistency, troubleshooting, bootstrap actions
locale: en-us
guid: fc9d78d9-1345-411d-91f8-72b2d8652cab
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - full stack developers
  - backend developers
  - platform administrators
outsystems-tools:
  - case management framework
coverage-type:
  - unblock
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
