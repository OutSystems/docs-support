---
summary: This article explains the cause, impact, and recommended action for a not found error that occurs while connecting to the destination server.
tags:
guid: 00a6b51c-e815-4e68-83fc-e51d58eab8b8
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma: 
platform-version: o11
---

# OS-DP-STREAM-00005

## Error message

`There was a 'not found' response from your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 5 (Not found) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. The endpoint URL may be incorrect.
