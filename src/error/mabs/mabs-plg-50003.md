---
summary: Couldn't install the Cordova plugin <plugin_name>. If the problem persists, check our documentation for more information.
tags:
guid: fcec27c7-4587-482f-95be-594c3c6502e2
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-50003

## Error message

`Couldn't install the Cordova plugin <plugin_name>. If the problem persists, check our documentation for more information.`

## Cause

This error indicates that the installation of a specific Cordova plugin failed. The &lt;plugin_name&gt; refers to the Cordova plugin name. The most frequent causes for this error to occur are the following:

* Issues related to plugin's hook.
* Malformed plugin with missing information (configurations or files are missing).

## Impact

Users can't generate the application package.

## Recommended action

Confirm that the Cordova plugin hooks have the correct information and ensure there's no missing configurations or files for the plugin. If this is related to an OutSystems supported plugin, check the [plugin's documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins) for more information.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-50003).
