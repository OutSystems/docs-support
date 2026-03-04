---
summary: This article explains the cause, impact, and recommended action for a resource exhausted error that occurs while connecting to the destination server.
tags: error handling, logging, server connectivity, performance issues, application monitoring
guid: 8a776202-d9d4-4a64-adcc-bac23d58ac49
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11, odc
audience:
  - full stack developers
  - platform administrators
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-00008

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was a 'resource exhausted' response from your destination server.`

## Cause

The error occurs when testing the connection and the destination server responds with a gRPC 8 (Resource exhausted) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was a 'resource exhausted' response from your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server responds with a gRPC 8 (Resource exhausted) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection.

</details>
