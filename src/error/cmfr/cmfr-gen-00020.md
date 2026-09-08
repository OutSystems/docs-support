---
summary: "OS-CMFR-GEN-00020 OutSystems 11 (O11) error: fix the Case Management Framework issue where CaseStatusId and NextCaseStatusId belong to different case definitions."
tags:
  - Case Management framework
  - Troubleshooting
locale: en-us
guid: cdb9315b-c576-4202-93f3-b5e69683c95b
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - Developer
  - Architect
outsystems-tools:
  - service studio
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-00020

## Error message

`Both statuses must belong to the same Case Definition.`

## Cause

While trying to create or update a case state machine, the Case Management framework detected that the **CaseStatusId** and **NextCaseStatusId** attributes match case statuses that belong to different case definitions.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the case status identifiers sent in the **CaseStatusId** and **NextCaseStatusId** attributes reference statuses that belong to the same case definition.
