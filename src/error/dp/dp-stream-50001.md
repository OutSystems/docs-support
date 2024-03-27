---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server. 
tags:
guid: ac049693-902b-4a08-b48a-7be166c5a65a
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-DP-STREAM-50001

## Error message

`There was a 'not implemented' response from your destination server.`

## Cause

The destination server has responded with an **HTTP 501** error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. Check if the APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.
