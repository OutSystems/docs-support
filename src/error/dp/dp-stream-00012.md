---
summary: This article explains the cause, impact, and recommended action for an unimplemented error that occurs while connecting to the destination server.
tags: log streaming, error handling, grpc errors, server configuration, outsystems platform
guid: 1b01900c-30d3-49fc-a562-3c6a51982738
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

# OS-DP-STREAM-00012

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was an 'unimplemented' response from your destination server.`

## Cause

The error occurs when testing the connection and the destination server responds with a gRPC 12 (Unimplemented) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

In the ODC Portal, review the destination server configuration. Check if the APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was an 'unimplemented' response from your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server responds with a gRPC 12 (Unimplemented) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. Check if the APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.

</details>
