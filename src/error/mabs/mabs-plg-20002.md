---
summary: Couldn't fetch the Cordova plugin <plugin_name> due to an authentication error. Please review your server and plugin access permissions.
app_type: mobile apps
tags: mabs; plg; error_codes
locale: en-us
guid: fb510c78-2deb-4083-be98-d4211406cba4
platform-version: o11
---

# OS-MABS-PLG-20002

## Error message

`Couldn't fetch the Cordova plugin <plugin_name> due to an authentication
error. Please review your server and plugin access permissions.`

## Cause

This error occurs when MABS isn't able to fetch a plugin due to an
authentication error.

## Impact

Users can't generate the application package.

## Recommended action

Check if the configured authentication to fetch the plugin is correct. In the
case of trying to fetch the plugin from another owned repository, validate that
MABS can access it. After fixing the issue, try to generate your application
again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-20002).
