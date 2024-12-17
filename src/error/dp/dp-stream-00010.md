---
summary: This article explains the cause, impact, and recommended action for an aborted error that occurs while connecting to the destination server.
tags: error handling, log streaming, server connection, troubleshooting, support services
guid: a428b0f1-d7fd-47ba-9b4f-529dc92c6b21
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11
audience:
  - full stack developers
  - platform administrators
  - backend developers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-00010

## Error message

`The operation was aborted.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 10 (Aborted) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.
