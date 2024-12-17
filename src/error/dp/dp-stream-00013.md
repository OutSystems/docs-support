---
summary: This article explains the cause, impact, and recommended action for an internal error that occurs while connecting to the destination server.
tags: log streaming, error handling, connection issues, grpc, application performance management
guid: 1b6ec9da-271f-450b-9ae3-da4202959284
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11
audience:
  - platform administrators
  - full stack developers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-00013

## Error message

`There was an internal error on your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 13 (Internal) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection. 
