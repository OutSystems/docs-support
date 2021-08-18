---
summary: WorkingHourStart must be set to a time before WorkingHourEnd.
tags:
---

# OS-CMFR-GEN-00005

## Error message

`WorkingHourStart must be set to a time before WorkingHourEnd.`

## Cause

While trying to execute the **Calendar_Create** or **Calendar_Update** actions, the Case Management framework detected that the **WorkingHourStart** and **WorkingHourEnd** input parameter values weren't properly set. This happened because of one of these reasons:

* **WorkingHourStart** is set to a time after the **WorkingHourEnd** time.
* **WorkingHourEnd** is set to a time before the **WorkingHourStart** time.

## Impact

The Case Management framework isn't able to successfully execute the action.

## Recommended action

Make sure the **WorkingHourStart** is set to a time before the **WorkingHourEnd**. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
