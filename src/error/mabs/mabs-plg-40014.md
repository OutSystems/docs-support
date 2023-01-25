---
summary: There was an issue fetching the Cordova plugin: <plugin_name>. We couldn't access the resource (http error <http_error_code>). Please review your plugin and server configurations.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 6cf861b8-b5cf-4fcc-9f0f-1e7c774424b2
---

# OS-MABS-PLG-40014

## Error message

`There was an issue fetching the Cordova plugin: <plugin_name>. We couldn't
access the resource (http error <http_error_code>). Please review your plugin
and server configurations.`

## Cause

This error occurs when MABS receives a http error **&lt;http_error_code&gt;** when
trying to fetch the plugin **&lt;plugin_name&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and validate the plugin
extensibility configurations. If you are hosting the plugin, validate that MABS
can access it. Then try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40014).
