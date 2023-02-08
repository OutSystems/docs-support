---
summary: Couldn't install the Cordova plugin <plugin_name> because the required dependency for the '<dependency_name>' node module in a plugin hook was missing. Check the product documentation on how to ensure all your plugins node dependencies.
tags: mabs plg error_codes
locale: en-us
app_type: mobile apps
guid: 70fb8768-b218-4aa3-9f2b-d9a600aa0436
platform-version: o11
---

# OS-MABS-PLG-20000

## Error message

`Couldn't install the Cordova plugin <plugin_name> because the required
dependency for the '<dependency_name>' node module in a plugin hook was
missing. Check the product documentation on how to ensure all your plugins node
dependencies.`

## Cause

This error occurs when MABS fails to run a hook, on the installation phase of
Plugin **&lt;plugin_name&gt;**, due to the build environment lacking the needed
dependencies for the hook to function.

## Impact

Users can't generate the application package.

## Recommended action

Change your plugin to have its hook dependencies installed by declaring all the
hook dependencies in its package.json.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-20000).
