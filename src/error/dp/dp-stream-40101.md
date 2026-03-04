---
summary: This article explains the cause, impact, and recommended action for an authentication error that occurs while connecting to the APM tool server.
tags: authentication errors, apm integration, error handling, server configuration, troubleshooting
guid: dc20e2a7-e5a2-4ef3-91b9-adfc0c905209
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

# OS-DP-STREAM-40101

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was an authentication error when reaching the APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An authentication error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination/APM tool.

## Recommended action

In the ODC Portal, review the APM server configuration details. Authentication credentials or endpoint URL or both may be incorrect.configuration.
</details>

<details>
<summary> <strong>Log streaming in O11</strong></summary>

## Error message

`There was an authentication error when reaching the APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An authentication error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

In LifeTime, click **Review destination information**, and on the **Destination tool** screen, review the APM server configuration. Authentication credentials or endpoint URL or both may be incorrect.

</details>
