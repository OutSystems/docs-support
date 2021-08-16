---
summary: Specified application version do not exists or the status update is invalid: <ApplicationVersionId>.
tags:
---

# OS-WFBL-GEN-00004

## Error message

`Specified application version do not exists or the status update is invalid: <ApplicationVersionId>.`

## Cause

This error occurs when users try to perform an operation that requires an update to the application status and the application doesn't exist or its current status isn't compliant with the desired operation.
The &lt;ApplicationVersionId&gt; includes the application version id that's causing the issue.

## Impact

The system can't read or modify the application status.

## Recommended action

Logout and Login again from Workflow Builder. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
