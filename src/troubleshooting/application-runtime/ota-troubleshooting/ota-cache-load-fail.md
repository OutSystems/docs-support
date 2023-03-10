---
summary: "Failed to load cache manifest. File <FilePath> not found. The file was never created."
locale: en-us
guid: 51BD8983-3791-4EBE-8132-2D20EB1F366A
app_type: mobile apps
platform-version: o11
---

# Failed to load cache manifest: File "FilePath" not found. The file was never created

## What are the errors?

``Failed to load cache manifest: File <FilePath> not found. The file was never created.``

## Where is this occurring and what does it mean?

This error occurs when the **Cache Manifest** file is missing on the device. This can be caused by an error during the write operation or a prior error that resulted in the writing step not being reached.

A potential scenario that can lead to this state is when the app attempts to perform an OTA upgrade to a new version on the server during the first run (which takes place during the splash screen animation, before the cache manifest file is written) but somehow gets stuck on splash screen, possibly due to faulty business logic, a frontend serving the wrong upgrade information, or poor network conditions (or any combination of the three).

# What is the impact of this error on the mobile application?

The app gets stuck on the splash screen of the application.

# How to overcome this issue?

* Reload the App to trigger a new application Upgrade OTA. 
* Check the available device storage and reinstall the App from the app store.
