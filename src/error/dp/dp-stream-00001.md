---
summary: This article explains the cause, impact, and recommended action for an operation cancelled error that occurs while connecting to the destination server.
tags: error handling, server configuration, logging, grpc, connection issues
guid: 1bf25d7e-40f0-4250-83b6-873a691b6820
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11, odc
audience:
  - full stack developers
  - platform administrators
outsystems-tools:
  - lifetime
  - ODC Portal
coverage-type:
  - unblock
---

# OS-DP-STREAM-00001

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`The operation was cancelled.`

## Cause

The error occurs when testing the connection, and the destination server canceled responds with a gRPC 1 (Cancelled) error.

## Impact

Unable to establish a connection with the destination server, therefore observability data isn't streamed to the destination.

## Recommended action

Check if the destination works correctly and re-establish the connection.

</details>

<details>
<summary> <strong>Log streaming in O11</strong></summary>

## Error message

`The operation was cancelled.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) and the destination server responds with a gRPC 1 (Cancelled) error.

## Impact

Unable to establish a connection with the destination server, therefore, logs aren't streamed to the destination.

## Recommended action

Check if the destination works correctly and re-establish the connection.

</details>
