---
summary: "OS-PLUG-FLTR-0010 HTTP error in the OutSystems platform File Transfer plugin: causes, impact, and fixes for 401, 403, 404, and 5xx status codes."
tags: Cordova,Mobile app,Plugins,Troubleshooting
locale: en-us
guid: 46c3c3d1-a01c-484b-a7ff-29e1dbb37811
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

# OS-PLUG-FLTR-0010

## Error message

HTTP error: `RESPONSE_CODE` - `MESSAGE`

## Platform

iOS, Android, and PWA

## Cause

The remote server returned an HTTP error status code (non-2xx, except 304 which is handled separately). Common causes include authentication failures (401 Unauthorized, 403 Forbidden), resource not found (404 Not Found), or server-side errors (5xx).

## Impact

The file transfer operation fails. The file won't be uploaded or downloaded.

## Recommended action

Review the HTTP status code and error message returned in the error object. Common fixes include:

* **401 / 403**: Verify authentication credentials and that the user has permission to access the resource.
* **404**: Check that the target URL exists and is correct.
* **5xx**: Contact the server administrator, as the issue is on the server side.

If the problem persists, open a support case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FLTR-0010).
