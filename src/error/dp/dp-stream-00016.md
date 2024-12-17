---
summary: This article explains the cause, impact, and recommended action for an unauthenticated error that occurs while connecting to the destination server.
tags: authentication errors, server connectivity, log streaming, error handling, grpc
guid: e0979b47-f97c-4a5e-8938-093d0f7d3515
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

# OS-DP-STREAM-00016

## Error message

`There was an authentication error when reaching your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server has responded with gRPC 16 (Unauthenticated) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. The authentication credentials, endpoint URL, or both, may be incorrect.
