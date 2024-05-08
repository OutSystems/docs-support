---
summary: This article explains the cause, impact, and recommended action for an HTTP server error on the APM tool server. 
tags:
guid: 39bf1b0d-e7a6-48b8-aece-5bc20b49e0ff
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma: 
platform-version: o11
---

# OS-DP-STREAM-50003

## Error message

`There was an unknown error reaching your APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An unknown error occurred while connecting your APM tool server.

## Impact

Unable to establish a connection with the destination server since the server is unreachable or has encountered unexpected conditions. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

The destination server has responded with an **HTTP 503** error. Therefore, check if the APM tool works correctly and re-establish the connection.  
