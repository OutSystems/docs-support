---
summary: This article explains the cause, impact, and recommended action for an error that occurs when trying to establish a connection with the destination server.
tags: authentication errors, apm integration, error handling, server configuration, troubleshooting
guid: 042164ed-3061-4065-aab9-6ee49b6ea162
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

# OS-DP-STREAM-30101

<details>
<summary> <strong> Streaming audit and observability data in ODC</strong></summary>

## Error message

`There was a 'moved permanently' response from your destination server.`

## Cause

The server has moved resources to a different destination and is responding with HTTP 301 `moved permanently` redirection status code.

## Impact

Unable to establish a connection with the destination server. Therefore, observability data isn't streamed to the destination or APM tool.

## Recommended action

Check the new location to be used as the endpoint URL. In the ODC Portal, review the destination information, and update the endpoint URL.

</details>

<details>
<summary> <strong>Log streaming in O11</strong></summary>

## Error message

`There was a 'moved permanently' response from your destination server.`

## Cause

The server has moved resources to a different destination and is responding with HTTP 301 `moved permanently` redirection status code.

## Impact

Unable to establish a connection with the destination server. Therefore, logs aren't streamed to the destination or APM tool.

## Recommended action

Check the new location to be used as the endpoint URL. In LifeTime, click Review destination information, and on the Destination tool screen, update the endpoint URL.

</details>
