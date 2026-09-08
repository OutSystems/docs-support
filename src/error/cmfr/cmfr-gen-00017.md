---
summary: "OS-CMFR-GEN-00017 in OutSystems 11 Case Management Framework: two case statuses have IsInitial True. Set one to False to resolve it."
tags: case management, error handling, isinitial attribute, case status configuration, caseconfigurations_api
locale: en-us
guid: 00538b23-fecd-47ed-91c1-cee49b2c5b33
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
topic:
  - fix-duplicate-case-status
---

# OS-CMFR-GEN-00017

## Error message

`There's already an active Case Status defined as initial.`

## Cause

While trying to create or update a case status with the attribute **IsInitial** set as **True**, the Case Management framework detected that an existing status is already set as initial. There can only be one case status set as initial for each case definition.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Before executing the action again:

* Update the existing case status and set its **IsInitial** attribute to **False**.
* Delete the existing case status using the **CaseStatus_Delete** action of the **CaseConfigurations_API** module.
