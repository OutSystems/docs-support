---
summary: This article explains the cause, impact, and recommended action for a deadline exceeded error that occurs while connecting to the destination server.
tags:
guid: 4612a96c-c741-4b79-9912-b01f8a05475a
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma: 
platform-version: o11
---

# OS-DP-STREAM-00004

## Error message

`The deadline exceeded before the operation could complete.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 4 (Deadline exceeded) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the destination or APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.
