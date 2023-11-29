---
summary: This article explains the cause, impact, and recommended action for a connection error that occurs while connecting to the APM tool server.
tags:
guid: 4215f2bc-42a9-4691-8b52-16081feec796
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-DP-STREAM-40401

## Error message

`There was an error trying to reach the APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An authorization error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

* In LifeTime, Click **Review destination information**, and on the Destination tool screen, review the APM server configuration. Verify if the server URL is valid and correct.
