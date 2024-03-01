---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server. 
tags:
guid: d02885d3-84f9-48a0-bc4a-29576356ebc6
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-DP-STREAM-50002

## Error message

`There was an internal or gateway communication error reported by the destination APM tool. If the problem persists, contact OutSystems Support.`

## Cause

An internal or gateway communication error occurred while connecting to the APM tool server.

## Impact

Unable to connect to the destination server due to internal or gateway communication error. Therefore, logs are not streamed to the APM tool.

## Recommended action

The destination server has responded with an **HTTP 502** error. Therefore, check if the APM tool works correctly and re-establish the connection.
