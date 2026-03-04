---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server.
tags: error handling, troubleshooting, outsystems platform, http errors
guid: 39bf1b0d-e7a6-48b8-aece-5bc20b49e0ff
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

# OS-DP-STREAM-50003

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was an unknown error reaching your APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An unknown error occurred while connecting your APM tool server.

## Impact

Unable to establish a connection with the destination server since the server is unreachable or has encountered unexpected conditions. Therefore, observability data isn't streamed to the destination/APM tool.

## Recommended action

The destination server has responded with an **HTTP 503** error. Therefore, check that the APM tool works correctly and re-establish the connection.  

</details>

<details>
<summary> <strong> Log streaming in ODC</strong></summary>

## Error message

`There was an unknown error reaching your APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An unknown error occurred while connecting your APM tool server.

## Impact

Unable to establish a connection with the destination server since the server is unreachable or has encountered unexpected conditions. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

The destination server has responded with an **HTTP 503** error. Therefore, check that the APM tool works correctly and re-establish the connection.  

</details>
