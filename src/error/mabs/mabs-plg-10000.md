---
summary: There was an issue fetching the Cordova plugin <plugin_name> because the connection timed out. Please try again.
tags: mabs plg error_codes
locale: en-us
app_type: mobile apps
guid: 74f4c22e-1523-44ec-8192-2c0852aeb774
platform-version: o11
---

# OS-MABS-PLG-10000

## Error message

`There was an issue fetching the Cordova plugin <plugin_name> because the
connection timed out. Please try again.`

## Cause

This error occurs when MABS timed out when trying to fetch your plugin.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for the cause of the error and also
where the hosts build logs for the plugin and retry building the application.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-10000).
