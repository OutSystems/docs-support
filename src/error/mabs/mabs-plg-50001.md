---
summary: Couldn't install the Cordova plugin <plugin_name> because the plugin dependency <plugin_dependency> doesn't support this Cordova version.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 1f5c03a7-c755-4379-a594-3a0ccd7890b6
---

# OS-MABS-PLG-50001

## Error message

`There was an issue fetching the Cordova plugin <plugin_name> because the
connection to the server was lost. This might be caused by server downtime.`

## Cause

This error occurs when MABS loses the connection while fetching the
**&lt;plugin_name&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and, if possible,
validate the connection to the server hosting the plugin. Then, try to generate
your application again.

Learn more about generating mobile apps and how to get the build logs
[here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems
support](https://success.outsystems.com/Support).
