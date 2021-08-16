---
summary: Module error. <OriginalErrorMessage>.
tags:
---

# OS-WFBL-GEN-00009

## Error message

`Module error. <OriginalErrorMessage>.`

## Cause

This error occurs when users try to publish an application and the system can't obtain the external dependencies that are needed from the users infrastructure.
The &lt;OriginalErrorMessage&gt;should include information about the cause of the error. 

## Impact

Users can't publish the application.

## Recommended action

Verify that for all form/case fields of type "Database entity" defined in the application, the respective Entity and Module in the  users infrastructure are correct, and the logged in user on Workflow Builder has download permission on those modules (in the users infrastructure).
