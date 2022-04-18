---
summary: WorkingHourStart must be set to a time before WorkingHourEnd.
tags:
locale: en-us
guid: 9891f258-6e5f-4aed-a866-30d0e46241fc
app_type: traditional web apps, mobile apps, reactive web apps
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
