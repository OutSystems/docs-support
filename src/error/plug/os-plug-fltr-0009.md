---
summary: "OS-PLUG-FLTR-0009 HTTP 304 Not Modified error in OutSystems mobile plugins: fix by reviewing If-None-Match and Cache-Control headers."
tags:
  - Android
  - Caching
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 343063a0-556c-4d55-962d-a9ee99f7e3cd
app_type: mobile apps
platform-version: odc,o11
figma:
audience:
  - Developer
  - Front-end developer
outsystems-tools:
  - service studio
  - odc studio
coverage-type:
  - unblock
topic:
  - using-cordova-plugins
  - wrap-cordova-plugin
isautopublish: true
---

# OS-PLUG-FLTR-0009

## Error message

The server responded with HTTP 304 Not Modified. If you want to avoid this, check your headers related to HTTP caching.

## Platform

iOS and Android

## Cause

The server returned an HTTP 304 Not Modified response, indicating the requested resource hasn't changed since the last request. This happens when the request includes caching-related headers such as `If-None-Match` or `If-Modified-Since` and the server determines the content is still current.

## Impact

The file download operation doesn't retrieve new content, as the server signals that the locally cached version is still valid.

## Recommended action

Review the HTTP headers sent with the request. If you need to force a fresh download, remove or adjust caching-related headers (for example, `If-None-Match`, `If-Modified-Since`, or `Cache-Control`) in the plugin's request configuration.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0009).
