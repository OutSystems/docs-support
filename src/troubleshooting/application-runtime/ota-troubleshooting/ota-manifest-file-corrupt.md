---
summary: Cache manifest file is corrupt or invalid
locale: en-us
guid: 03D119E4-EA0B-4593-B258-FA9CF41CA76C
app_type: mobile apps
platform-version: o11
figma:
---

# Cache manifest file is corrupt or invalid

## What are the errors?

``Cache manifest file is corrupt or invalid.``

## Where is this occurring and what does it mean?

The **cache manifest** file corresponds to a local and internal representation of the native cache within the app. The cache manifest file is not the **manifest.json** from prebundle or the content obtained from moduleinfo route ``(https://<app-domain>/<home-eSpace>/moduleservices/moduleinfo)`` on the server. 

The cache manifest file is created on-demand by OSCache and is a persistent state of the cache on a device at a given time. This error occurs if this file gets corrupted, for example, if there is a lack of disk space on the device.

## What is the impact of this error on the mobile application?

The App stops working or fails to start, particularly if it's not the first time the app is run.

## How to overcome this issue?

Check the storage available on the device and reinstall the App from the app store.
