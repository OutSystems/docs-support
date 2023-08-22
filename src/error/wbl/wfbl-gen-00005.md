---
summary: "Application version icon is larger than <MaxSize> for application version: <ApplicationVersionId>."
tags:
locale: en-us
guid: 0fdba693-c956-410e-b4ce-e4f917c57620
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-WFBL-GEN-00005

## Error message

`Application version icon is larger than <MaxSize> for application version: <ApplicationVersionId>.`

## Cause

This error occurs when users try to set an icon to an application that exceeds the allowed max size (in bytes).
The &lt;MaxSize&gt; includes the max size allowed for the icon file (in bytes), and &lt;ApplicationVersionId&gt; refers to the application version id that caused the issue.

## Impact

Users can't update the application icon if it exceeds the max size allowed.

## Recommended action

The users interface logic should prevent this error. However, if the operation is allowed to be performed, try again. If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
