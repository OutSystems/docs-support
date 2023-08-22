---
summary: Couldn't install the Cordova plugin <plugin_name> because we couldn't fetch its dependencies due to a CocoaPods server error. Please try again.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: f51bbdd7-5738-4e2c-ad6d-5f5106307c64
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-50005

## Error message

`Couldn't install the Cordova plugin <plugin_name> because we couldn't fetch its dependencies due to a CocoaPods server error. Please try again.`

## Cause

This error occurs when MABS can't install the plugin **&lt;plugin_name&gt;** because it
fails to fetch a Pod from the CocoaPods CDN.

This may be due to downtime on the CocoaPods CDN.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details about the error. Then,
try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-50005).
