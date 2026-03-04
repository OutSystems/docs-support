---
summary: This article explains the cause, impact, and recommended action for a deadline exceeded error that occurs while connecting to the destination server.
tags: error handling, connection issues, log streaming, outsystems platform, troubleshooting
guid: 4612a96c-c741-4b79-9912-b01f8a05475a
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
  - service studio
coverage-type:
  - unblock
---

# OS-DP-STREAM-00004

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`The deadline exceeded before the operation could complete.`

## Cause

The error occurs when testing the connection and the destination server has responds with gRPC 4 (Deadline exceeded) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

Check if the destination or APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`The deadline exceeded before the operation could complete.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server responds with a gRPC 4 (Deadline exceeded) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

Check if the destination or APM tool works correctly and re-establish the connection. If the problem persists, contact OutSystems Support.

</details>
