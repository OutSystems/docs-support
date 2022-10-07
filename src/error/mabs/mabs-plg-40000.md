---
summary: We couldn't find Cordova plugin <plugin_name>.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: c8f61a0e-3ea3-49c4-9c7a-7ddae7c6ff1f
---

# OS-MABS-PLG-40000

## Error message

`We couldn't find Cordova plugin <plugin_name>.`

## Cause

This error occurs when MABS isn't able to resolve the provided Cordova plugin,
whether in the NPM registry or at the URL provided.

## Impact

Users can't generate the application package.

## Recommended action

Check the build log for more details and the extensibility configurations of
your plugin. After fixing it, try to generate your application again.

You can follow this documentation on [how to use Cordova
plugins](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/Using_Cordova_Plugins).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40000).
