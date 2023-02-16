---
summary: "Cannot remove case application version since it's not in Draft : <ApplicationVersionId>."
tags:
locale: en-us
guid: 6c71b7e6-874f-4565-98ef-df60259a491f
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-WFBL-GEN-00001

## Error message

`Cannot remove case application version since it's not in Draft : <ApplicationVersionId>.`

## Cause

This error occurs when you try to delete an application on Workflow Builder but it fails due to an application version status validation.
The &lt;ApplicationVersionId&gt; includes the version id of the application you're trying to delete.

## Impact

You ccan't delete the selected application from Workflow Builder when the delete option is available.

## Recommended action

Logout and login again from Workflow Builder. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
