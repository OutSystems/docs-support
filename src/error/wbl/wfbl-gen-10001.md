---
summary: OutSystems 11 (O11) Workflow Builder invalid access error occurs when a user lacks permission to perform an operation.
tags: error handling, permission issues, security, troubleshooting, support
locale: en-us
guid: d528800d-d929-49dd-9ea3-8378debe4043
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - Platform administrator
  - Developer
outsystems-tools:
  - workflow builder
coverage-type:
  - unblock
topic:
  - wfb-invalid-access-error
---

# OS-WFBL-GEN-10001

## Error message

`Invalid access. <OriginalErrorMessage>.`

## Cause

This error occurs when users don't have permission to perform the operation.
The &lt;OriginalErrorMessage&gt; indicates the cause of the permission error.

## Impact

Users can't execute the operation.

## Recommended action

Verify the user has the permission to perform the operation. If the user has permission for the operation, Logout and Login again from Workflow Builder. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
