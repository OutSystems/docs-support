---
summary: Timeout reached when downloading resources during over-the-air upgrade
locale: en-us
guid: 6C1A3620-6882-45B1-A08D-965FB2D3864B
app_type: mobile apps
platform-version: o11
---

# Timeout while downloading resources

## What are the errors?

* ``Aborting resources download. Failed to download resource <Resource_Path>?<Resource_Hash> with error: The request timed out.``

* ``Upgrade failed - rolling back to the previous application version.``

## Where is this occurring and what does it mean?

This scenario typically occurs in step 8 (see OTA upgrade process diagram) when the mobile device is using a poor network connection and/or the OTA upgrade involves downloading large resources. 

OutSystems mobile applications have a 30 second download timeout per resource. This means that the upgrade will fail with a timeout if a single resource takes longer than 30 seconds to download. 

**Note**: This value cannot be changed.

## What is the impact of this error on the mobile application?

In most cases, the mobile app is rolled back to the previous version cached in the device. Runtime issues may occur depending on the changes introduced in the new version.

## How to overcome this issue?

* Reload the mobile app. This triggers the upgrade OTA again.

* In this scenario, if the new application published in the server includes new and heavy resources, which are consistently failing to download due to timeouts, you can generate a new application package and distribute it to the end-users. The application package will include all the necessary resources.

