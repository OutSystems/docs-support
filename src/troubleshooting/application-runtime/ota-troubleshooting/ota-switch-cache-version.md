---
summary: Unable to switch to cache version
locale: en-us
guid: 7A2E41BB-9F8D-457B-A519-19AA00BE98E3
app_type: mobile apps
platform-version: o11
figma:
---

# Unable to switch to cache version

## What are the errors?

``Unable to switch to cache version.``

## Where is this occurring and what does it mean?

The action **switchToVersion** is initiated by the client runtime running on the WebView, that calls the action to the native side to switch to a specific version/cache frame. This is triggered by the **OnFinish** event (native cache) when all application resources are cached.

These errors can occur whenever the client runtime decides to call the **switchToVersion** action with a version that is not the running version on the native side. In other words, this means a state mismatch between the client runtime and the native side.

## What is the impact of this error on the mobile application?

The mobile app won't be upgraded and the version will be rolled back to the previous version cached in the device. Errors in runtime may be expected depending on the changes introduced.

## How to overcome this issue?

* Reload the App  to trigger a new application Upgrade OTA. 
* Check the available storage device and reinstall the App from the app store.
