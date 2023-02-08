---
summary: Couldn't install the Cordova plugin <plugin_name> because CocoaPods built in Swift are not supported.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: f46dbb03-8652-4c48-983c-52611e3515d3
platform-version: o11
---

# OS-MABS-PLG-40008

## Error message

`Couldn't install the Cordova plugin <plugin_name> because CocoaPods built in
Swift are not supported.`

## Cause

This error occurs when a pod is using Swift but not importing it as a
framework.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details. To fix this issue, you
need to import your pod as a framework and try to generate your application
again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40008).
