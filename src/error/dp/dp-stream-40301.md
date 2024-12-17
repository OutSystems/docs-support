---
summary: This article explains the cause, impact, and recommended action for an authorization error that occurs while connecting to the APM tool server.
tags: authorization errors, error handling, server configuration, technical support
guid: f234f28c-ba08-47d8-8a69-4e918ae3ab8c
locale: en-us
app_type: traditional web apps, mobile apps, reactive web apps
figma:
platform-version: o11
audience:
  - platform administrators
  - full stack developers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# OS-DP-STREAM-40301

## Error message

`There was an authorization error when reaching the APM tool server. If the problem persists, contact OutSystems Support.`

## Cause

An authorization error occurred while connecting to the APM tool server.

## Impact

Unable to establish a connection with the destination server. Therefore, logs are not streamed to the destination/APM tool.

## Recommended action

* In LifeTime, Click **Review destination information**, and on the Destination tool screen, review the APM server configuration. 
* Go to the APM tool and verify that the credentials provided have the correct permissions. 
