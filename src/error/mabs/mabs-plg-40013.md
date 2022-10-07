---
summary: Couldn't install the Cordova plugin <plugin_name> because the plugin tried to edit a missing XML node <xml_node>.
tags: mabs; plg; error_codes
locale: en-us
app_type: mobile apps
guid: 3a786d63-2283-4abe-8842-894d0ce6cf1b
---

# OS-MABS-PLG-40013

## Error message

`Couldn't install the Cordova plugin <plugin_name> because the plugin tried to
edit a missing XML node <xml_node>.`

## Cause

This error occurs when the plugin **&lt;plugin_name&gt;** is trying to change a tag
or attribute on an XML file but the selector isn't finding the node
**&lt;xml_node&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

This usually happens when a plugin is trying, for instance, to edit the tag
`tagC` under the path `file->tagA->tagB->tagC` but `tagB` doesn't exist, making
this an impossible path. Check the build logs on Service Center for more
details and fix the selector. Then, try to generate your application again.

You can find more documentation about editing XML files in the Cordova plugins
in the [official Apache Cordova
documentation](https://cordova.apache.org/docs/en/latest/plugin_ref/spec.html#config-file).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40013).
