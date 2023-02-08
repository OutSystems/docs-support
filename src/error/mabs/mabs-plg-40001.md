---
summary: Invalid Cordova plugin <plugin_name>.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 5df80ef3-c2c1-4bd6-be71-d4e8a59b30bc
platform-version: o11
---

# OS-MABS-PLG-40001

## Error message

`Invalid Cordova plugin <plugin_name>.`

## Cause

This error occurs when the identifier, URL, or resource provided in the
extensibility configurations isn't a valid Cordova plugin. One usual issue is
that the plugin is missing a package.json.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and after fixing it,
try to generate your application again.

You can follow this documentation on [how to use Cordova
plugins](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/Using_Cordova_Plugins).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40001).
