---
summary: This article explains the cause, impact, and recommended action for an invalid argument error that occurs while connecting to the destination server.
tags:
guid: a8049b5c-fee5-4f3b-90e9-37ae82ed006f
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma: 
platform-version: o11
---

# OS-DP-STREAM-00003

## Error message

`The client specified an invalid argument. Please review the connection.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 3 (Invalid argument) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. The authentication credentials, endpoint URL, or both, may be incorrect. If the problem persists, contact OutSystems Support.
