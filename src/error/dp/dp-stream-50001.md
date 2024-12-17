---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server.
tags: http errors, server configuration, log streaming, error handling, outsystems platform
guid: ac049693-902b-4a08-b48a-7be166c5a65a
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-50001

## Error message

`There was a 'not implemented' response from your destination server.`

## Cause

The destination server responded with an **HTTP 501** error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination or APM tool.

## Recommended action

[In LifeTime Log Streaming](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35), review the destination server configuration. Check if the destination or APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.
