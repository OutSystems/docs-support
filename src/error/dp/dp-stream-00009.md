---
summary: This article explains the cause, impact, and recommended action for a failed precondition error that occurs while connecting to the destination server.
tags:
guid: 2b3be8a1-a0e6-4ba0-8ff1-37539177e915
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma: 
platform-version: o11
---

# OS-DP-STREAM-00009

## Error message

`There was a 'failed precondition' response from your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 9 (Failed precondition) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection.
