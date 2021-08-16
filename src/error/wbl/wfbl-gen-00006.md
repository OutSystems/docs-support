---
summary: Unable to discard version. It has published versions: <ApplicationVersionId>.
tags:
---

# OS-WFBL-GEN-00006

## Error message

`Unable to discard version. It has published versions: <ApplicationVersionId>.`

## Cause

This error occurs when users try to delete an application that's already published, but still displays as unpublished.
The &lt;ApplicationVersionId&gt; refers to the application version id that caused the issue.

## Impact

Users can't delete the application from Workflow Builder.

## Recommended action

Logout and Login again from Workflow Builder. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
