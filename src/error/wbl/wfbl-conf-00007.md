---
summary: OutSystems 11 (O11) Workflow Builder group creation errors occur when member operations fail; retry the operation or contact support.
tags:
  - Groups
  - Troubleshooting
  - Workflows
locale: en-us
guid: c5884356-f8a8-439b-8810-1a1bcd0ef996
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
coverage-type:
  - unblock
topic:
  - wfb-group-create-error
audience:
  - Developer
---

# OS-WFBL-CONF-00007

## Error message

`Cannot create Group: <OriginalErrorMessage>.`

## Cause

This error occurs when you try to create a group and for some members of the group, the operation fails.
The &lt;OriginalErrorMessage&gt; includes information about the cause of the error.

## Impact

Workflow Builder can't save the Group defined, therefore that group can't be used in the application workflow.

## Recommended action

Try to repeat the operation. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
