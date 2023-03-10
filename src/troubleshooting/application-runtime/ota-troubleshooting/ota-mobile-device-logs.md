---
summary: "Unable to find the <Resource> resource"
locale: en-us
guid: FD2F492E-7BEF-41F8-A4F9-4C765026C5C6
app_type: mobile apps
platform-version: o11
---

# Unable to find resource 

## What is the error?

`Unable to find resource <Resource>`

This error can only be observed in the Mobile Device Logs.

## Where is this occurring and what does it mean?

* These are debugging logs that can be observed directly on the Device Logs and aren’t sent over to Service Center. 

* The error occurs whenever WebView requests to load some specific resource that isn’t part of a cache frame and thus, the cache will ignore it and allows the request to continue for the remaining interested parts that may be able to respond back with content. 

* Special cases are Cordova resources, such as JavaScript from Cordova plugins. These resources aren’t served by a cache frame nor from the web, but are served locally from the shell.

## What is the impact of this error on the mobile application?

These logs are merely informative and only accessible through Android Debug Bridge (ADB). No impact on the end-user is expected.

## How to overcome this issue?

This is just informative and no impact is expected.
