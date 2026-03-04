---
summary: This article explains the cause, impact, and recommended action for a failed precondition error that occurs while connecting to the destination server.
tags: error handling, log streaming, debugging, grpc errors
guid: 2b3be8a1-a0e6-4ba0-8ff1-37539177e915
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11, odc
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - lifetime
  - service center
coverage-type:
  - unblock
---

# OS-DP-STREAM-00009

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was a 'failed precondition' response from your destination server.`

## Cause

The error occurs when testing the connection and the destination server responds with a gRPC 9 (Failed precondition) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was a 'failed precondition' response from your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server responds with a gRPC 9 (Failed precondition) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the APM tool works correctly and re-establish the connection.

</details>
