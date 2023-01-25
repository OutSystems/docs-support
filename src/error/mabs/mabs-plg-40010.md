---
summary: Couldn't install the Cordova plugin <plugin_name>. Your plugin must have a package.json file that matches the configurations in the plugin.xml file.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: d74a2381-a1ff-45a3-9d98-40e1ce28ab1e
---

# OS-MABS-PLG-40010

## Error message

`Couldn't install the Cordova plugin <plugin_name>. Your plugin must have a
package.json file that matches the configurations in the plugin.xml file.`

## Cause

This error occurs when the plugin **&lt;plugin_name&gt;** has mismatches between the
package.json and the plugin.xml files.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details and after fixing the
plugin configuration, try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40010).
