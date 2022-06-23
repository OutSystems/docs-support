---
summary: Couldn't fetch the Cordova plugin <plugin_name>. If the problem persists, check our documentation for more information.
tags:
guid: 70d94ff5-ef07-4793-80a5-d5fbb1a9299b
locale: en-us
app_type: mobile apps
---

# OS-MABS-PLG-50002

## Error message

`Couldn't fetch the Cordova plugin <plugin_name>. If the problem persists, check our documentation for more information.`

## Cause

This error indicates that something wrong happened when trying to access the plugin's source URL, for example the URL can't be found or isn't reachable. The **&lt;plugin_name&gt;** refers to the Cordova plugin name. The most frequent causes for this error to occur are the following: 

* Connection interrupted while fetching the plugin.
* Connection interrupted due to timeout issue while fetching the plugin.
* Other network issues.

## Impact

Users can't generate the application package.

## Recommended action

Check if plugin's source URL is correct and make sure that your connection is stable. After that, try to repeat the operation.

If the problem persists, create a case with [OutSystems support](https://success.outsystems.com/Support).
