---
summary: This article explains the cause, impact, and recommended action for a not found error that occurs while connecting to the destination server.
tags: error handling, server configuration, log streaming, grpc, connectivity issues
guid: 00a6b51c-e815-4e68-83fc-e51d58eab8b8
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11, odc
audience:
  - platform administrators
  - full stack developers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-00005

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was a 'not found' response from your destination server.`

## Cause

The error occurs when testing the connection and the destination server has responds with gRPC 5 (Not found) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

In the ODC Portal, review the destination server configuration. The endpoint URL may be incorrect.

</details>

<details>
<summary> <strong> Log steaming in O11</strong></summary>

## Error message

`There was a 'not found' response from your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server responds with a gRPC 5 (Not found) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. The endpoint URL may be incorrect.

</details>
