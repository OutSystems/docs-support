---
summary: "Healing resource <Resource> from prebundle failed"
locale: en-us
guid: 9784BD95-44FB-4231-A892-78A363BE2F54
app_type: mobile apps
platform-version: o11
---

# Healing resource build from prebundle: FAILED

## What are the errors?

``Healing resource <Resource> from prebundle: FAILED``

## Where is this occurring and what does it mean?

An attempt to heal a resource is performed by falling back to the resource present in the prebundle.

There's another variant of these logs that shows healing from the web instead of from the prebundle. Depending on if the version of the downloaded resource, as it is known on the server, differs from what the local version of the app expects, this type of log may be accompanied by a checksum validation error, ``File is corrupt or invalid``.

## What is the impact of this error on the mobile application?

The app is in an invalid state and may only recover with an app store update and not an OTA. 

## How to overcome this issue?

* Try to reload the App. 
* If the issue remains, reinstall the App from the app store.



