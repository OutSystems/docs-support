---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server.
tags: apm integration, http errors, troubleshooting, server communication, error handling
guid: d02885d3-84f9-48a0-bc4a-29576356ebc6
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11, odc
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - none
coverage-type:
  - unblock
---

# OS-DP-STREAM-50002

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was an internal or gateway communication error reported by the destination APM tool. If the problem persists, contact OutSystems Support.`

## Cause

An internal or gateway communication error occurred while connecting to the APM tool server.

## Impact

Unable to connect to the destination server due to internal or gateway communication error. Therefore, observability data isn't streamed to the APM tool.

## Recommended action

The destination server has responded with an **HTTP 502** error. Therefore, check that the APM tool works correctly and re-establish the connection.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was an internal or gateway communication error reported by the destination APM tool. If the problem persists, contact OutSystems Support.`

## Cause

An internal or gateway communication error occurred while connecting to the APM tool server.

## Impact

Unable to connect to the destination server due to internal or gateway communication error. Therefore, logs are not streamed to the APM tool.

## Recommended action

The destination server has responded with an **HTTP 502** error. Therefore, check that the APM tool works correctly and re-establish the connection.

</details>
