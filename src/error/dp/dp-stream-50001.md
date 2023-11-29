---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server. 
tags:
guid: ac049693-902b-4a08-b48a-7be166c5a65a
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-DP-STREAM-50001

## Error message

`There was an unexpected error on your APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An unexpected error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server since the server is unreachable or has encountered unexpected conditions. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

The destination server has responded with an **HTTP 501** error. Therefore, check if the APM tool works correctly and re-establish the connection.  
