---
summary: The process is still running.
tags:
locale: en-us
guid: a31308f8-ce4e-4e83-b7d1-5440deec8bb3
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-BPT-00001

## Error message

`The process is still running.`

## Cause

The BPT process that manages events inside the Case Management framework triggered this exception to keep itself open since there are still events running/pending. The process checks whether or not it should close itself, and if it should not close it takes advantage of the BPT Wait activity's auto-retry feature after an unhandeled exception.

## Impact

No impact. The exception was triggered as part of the natural flow of the **ProcessActivityEvent** process.

## Recommended action

No actions required.
