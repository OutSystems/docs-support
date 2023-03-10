---
summary: Could not get InputStream while trying to get cache resource 
locale: en-us
guid: E91A6136-86E0-48EC-94B0-AD38D06A203D
app_type: mobile apps
platform-version: o11
---

# Could not get InputStream while trying to get cache resource  

## What are the errors?

``Could not get InputStream while trying to get cache resource.``

## Where is this occurring and what does it mean?

These logs mean that, while the resources are being requested by the WebView to be loaded on the mobile device, the associated file is missing on the file system. When this happens, the healing mechanism kicks in which leads to the Healing logs appearing around the same timeframe. This is a common error when there is a lack of storage space available.

## What is the impact of this error on the mobile application?

The impact on end users depends on the outcome of the healing process. If that fails, the following error is observed in the logs Healing resource ``<Resource> from prebundle: FAILED``. This means the device might be in a state where only an update from the stores can rectify the problem.

## How to overcome this issue?

Check the device storage available and try to reload the App. If the issue remains, reinstall the App from the app store.
