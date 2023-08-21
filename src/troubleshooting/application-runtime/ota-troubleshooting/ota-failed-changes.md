---
summary: Failed changes in the Local Storage Metamodel due to integrity checks
locale: en-us
guid: 5D8B648B-356D-4A9C-BBFD-61308633C8A3
app_type: mobile apps
platform-version: o11
figma:
---

# Failed changes in the Local Storage Metamodel due to integrity checks 

## What are the errors?

* ``sqlite3_step failure: UNIQUE constraint failed: <LocalEntity_PhysicalTable>.<LocalEntity_Attribute>``

* ``Upgrade failed - rolling back to the previous application version.``

## Where is this occurring and what does it mean?

This occurs when a change in the Metamodel of a Local Entity can’t be performed due to a Local DB Integrity Check (for example, changes to the Identifier or a DataType) for entities that already contain Data. This only affects devices that contain data in the affected Local Entities.

## What is the impact of this error on the mobile application?

* The mobile application won't be upgraded and will be rolled back to the previous version cached in the device. Errors in runtime may be expected depending on the changes introduced.

* The upgrade of the App Resources and the Upgrade Local DB Metamodel occur at the same time. Only after both are successfully upgraded will the app be upgraded.  

## How to overcome this issue?

* Roll the app back to the version previously published in the environment and reassess the changes.

* To rectify the issue in affected devices:
    * Clean the cache and data from the app.
    * Reinstall the app.
