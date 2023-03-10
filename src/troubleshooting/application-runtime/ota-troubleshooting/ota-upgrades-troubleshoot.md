---
summary: Common issues related to over-the-air upgrades
locale: en-us
guid: 7AAE6C3B-FDB6-4187-A493-EF62F925AFFC
app_type: mobile apps
platform-version: o11
---

# Troubleshooting over-the-air upgrades

When doing over-the-air (OTA) upgrades, there are some scenarios under which the upgrade may not be successful. This article describes some common issues related to the OTA process.

If an OTA upgrade fails, the upgrade is rolled back and the application continues running the version that was previously cached (before the upgrade started). While this rollback allows the user to continue using the app, runtime issues may occur. For example, when calling a server action that had its structure changed (modifications in its name or in the input/output parameters). 

If the OTA upgrade fails and is rolled back to when some new resources were already successfully downloaded, the app keeps those. The next time the app tries to perform the OTA upgrade, not all resources need to be downloaded. To ensure this, a checkpoint mechanism  is triggered several times during the upgrade.

The errors that are detailed in the following sections are observed in the Service Center Error logs except for the [Unable to find resource](ota-mobile-device-logs.md) error that is found in the device itself. 
