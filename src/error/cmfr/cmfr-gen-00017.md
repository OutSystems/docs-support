---
summary: There's already an active Case Status defined as initial.
tags:
locale: en-us
guid: 00538b23-fecd-47ed-91c1-cee49b2c5b33
app_type: traditional web apps, mobile apps, reactive web apps
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
