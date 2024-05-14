---
summary: This article explains the cause, impact, and recommended action for an operation cancelled error that occurs while connecting to the destination server.
tags:
guid: 1bf25d7e-40f0-4250-83b6-873a691b6820
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma: 
platform-version: o11
---

# OS-DP-STREAM-00001

## Error message

`The operation was cancelled.`

## Cause

The destination server cancelled the connection.

## Impact

Unable to establish a connection with the destination server. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

The destination server has responded with gRPC 1 (Cancelled) error. Therefore, check if the APM tool works correctly and re-establish the connection.
