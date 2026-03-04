---
summary: This article explains the cause, impact, and recommended action for a permission denied error that occurs while connecting to the destination server.
tags: error handling, log streaming, security, configuration, troubleshooting
guid: 31062f99-3a03-4a8a-8a9c-70e950043509
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
coverage-type:
  - unblock
---

# OS-DP-STREAM-00007

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was a permission denied error when reaching your destination server.`

## Cause

The error occurs when testing the connection and the destination server responds with a gRPC 7 (Permission denied) error.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination.

## Recommended action

In the ODC Portal, review the destination server configuration. The authentication credentials, endpoint URL, or both, may be incorrect.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was a permission denied error when reaching your destination server.`

## Cause

The error occurs when testing the connection after [Configuring the log streaming service in LifeTime](https://www.outsystems.com/tk/redirect?g=172ac547-add4-4cc5-9adf-d72fbe379d35) or when checking Log Streaming health and the destination server responds with a gRPC 7 (Permission denied) error.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination.

## Recommended action

In LifeTime Log Streaming, review the destination server configuration. The authentication credentials, endpoint URL, or both, may be incorrect.

</details>
