---
summary: Common issues related to over-the-air upgrades.
locale: en-us
guid: 7AAE6C3B-FDB6-4187-A493-EF62F925AFFC
app_type: mobile apps
platform-version: o11
figma:
---

# Troubleshooting over-the-air upgrades

When doing over-the-air (OTA) upgrades, there are some scenarios under which the upgrade may not be successful. This article describes some common issues related to the OTA process.

If an OTA upgrade fails, the upgrade is rolled back and the application continues running the version that was previously cached (before the upgrade started). While this rollback allows the user to continue using the app, runtime issues may occur. For example, when calling a server action that had its structure changed (modifications in its name or in the input/output parameters). 

If the OTA upgrade fails and is rolled back to when some new resources were already successfully downloaded, the app keeps those. The next time the app tries to perform the OTA upgrade, not all resources need to be downloaded. To ensure this, a checkpoint mechanism  is triggered several times during the upgrade.

The errors that are detailed in this section's child articles are observed in the Service Center Error logs except for the [Unable to find resource](ota-mobile-device-logs.md) error that is found in the device itself.

If you are experiencing one of these errors, click on the corresponding link to access the error troubleshooting guide:

- [Timeout while downloading resources](ota-timeout-downloading.md)
- [Downloaded resources do not match the resources listed in the moduleinfo](ota-mismatched-resources-moduleinfo.md)
- [Failed changes in the Local Storage Metamodel due to integrity checks](ota-failed-changes.md)
- [Changes in Local Entity Attributes data types when they have data in the device](ota-changed-local-entities.md)
- [Unable to find resource `<resource>`](ota-mobile-device-logs.md)
- [Could not get InputStream while trying to get cache resource](ota-service-error-logs.md)
- [Healing resource `<Resouce>` from prebundle: FAILED](ota-healing-resource.md)
- [Cache manifest file is corrupt or invalid](ota-manifest-file-corrupt.md)
- [Unable to switch to cache version](ota-switch-cache-version.md)
- [Failed to load cache manifest: File `<FilePath>` not found. The file was never created](ota-cache-load-fail.md)
- [Failed to close database cannot be closed while a transaction is in progress](ota-database-close-fail.md)