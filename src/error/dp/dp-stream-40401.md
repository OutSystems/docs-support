---
summary: This article explains the cause, impact, and recommended action for a connection error that occurs while connecting to the APM tool server.
tags: error handling, connection issues, apm integration, authorization errors, configuration management
guid: 4215f2bc-42a9-4691-8b52-16081feec796
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11, odc
audience:
  - platform administrators
  - full stack developers
  - infrastructure managers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-40401

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was an error trying to reach the APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An authorization error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination/APM tool.

## Recommended action

* In the ODC Portal, review the APM server configuration details. Verify that the server URL is valid and correct.

</details>

<details>
<summary> <strong> Log streaming in O11</strong></summary>

## Error message

`There was an error trying to reach the APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An authorization error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

* In LifeTime, Click **Review destination information**, and on the Destination tool screen, review the APM server configuration. Verify if the server URL is valid and correct.

</details>
