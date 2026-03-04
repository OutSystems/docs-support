---
summary: View the causes and recommended actions for the OS-DP-STREAM-00002 error when testing a Log streaming connection
tags: error handling, log streaming, debugging, application performance monitoring, grpc
guid: 1497f58c-2a4c-4816-b7f2-7d8c782fd5b2
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

# OS-DP-STREAM-00002

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was an unknown error reaching your destination server.`

## Cause

The error occurs when testing the connection and the destination server responded with gRPC 2 (Unknown) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

Check if the destination/APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was an unknown error reaching your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health, and the destination server responds with a gRPC 2 (Unknown) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the destination/APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.

</details>
