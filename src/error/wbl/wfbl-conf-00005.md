---
summary: Invalid application data. <OriginalErrorMessage>.
tags: error handling, data consistency, user authentication, application troubleshooting
locale: en-us
guid: f062e40f-49f4-4628-84d5-6c0fbaa655ee
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - frontend developers
  - full stack developers
  - platform administrators
outsystems-tools:
  - workflow builder
coverage-type:
  - unblock
---

# OS-WFBL-CONF-00005

## Error message

`Invalid application data. <OriginalErrorMessage>.`

## Cause

This error occurs when users try to update an application that has inconsistent data.
The &lt;OriginalErrorMessage&gt; includes information about the cause of the error.

## Impact

Workflow Builder can't save the application because of inconsistencies.

## Recommended action

Logout and login again from Workflow Builder. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
