---
summary: The selected Tag and Case belong to different Case Definitions.
tags:
locale: en-us
guid: 00419394-e881-4fe4-a946-41bdf2a010f8
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-GEN-00010

## Error message

`The selected Tag and Case belong to different Case Definitions.`

## Cause

While trying to execute the **CaseTag_Create** action the Case Management framework detected that the tag and case which were input belong to different case definitions.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure the tag and case you are trying to associate belong to the same case definition.

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
