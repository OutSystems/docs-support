---
summary: Activity with Id "<activity-identifier-value>" does not belong to Case with Id "<case-identifier-value>".
tags:
locale: en-us
guid: c48ed6a6-4265-46d8-af5d-1135f764e7ea
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-CMFR-GEN-00034

## Error message

`Activity with Id "<activity-identifier-value>" does not belong to Case with Id "<case-identifier-value>".`

## Cause

While trying to execute the **Case_DiscardActivity** action, the Case Management framework detected that the **Activity** Identifier passed as input doesn't belong to a process associated with the case which has the Identifier &lt;case-identifier-value&gt;.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
