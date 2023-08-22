---
summary: Couldn't install the Cordova plugin <plugin_name>. You must set a higher minimum iOS deployment target for a specific pod in the Extensibility Configurations property of your home module.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 333bc8b1-0225-448f-bbc5-fb27842ee8be
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-40007

## Error message

`Couldn't install the Cordova plugin <plugin_name>. You must set a higher
minimum iOS deployment target for a specific pod in the Extensibility
Configurations property of your home module.`

## Cause

This error occurs when the provided plugin needs a higher minimum iOS
deployment target than the one in use.

## Impact

Users can't generate the application package.

## Recommended action

Check the build log for more details and either change the minimum iOS
deployment target using the Cordova preference `deployment-target` or change
the referenced plugin. Then, try to generate your application again.

Check the official Cordova documentation about the `deployment-target`
preference
[here](https://cordova.apache.org/docs/en/11.x/config_ref/#:~:text=deployment%2Dtarget(string))

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40007).
