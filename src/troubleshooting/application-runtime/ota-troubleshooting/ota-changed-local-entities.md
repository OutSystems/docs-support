---
summary: Changes in Local Entity Attributes data types when they have data in the device
locale: en-us
guid: 27F1C7DD-2290-4391-8A9E-64569AAEACAB
app_type: mobile apps
platform-version: o11
---

# Changes in Local Entity Attributes data types when they have data in the device

## What are the errors?

* ``Upgrade failed - rolling back to previous application version``

* ``Unable to upgrade attribute '<DataTypeA>' data type to <DataTypeB>:``

* ``Unable to convert databaseValue:'<Value>  (length:X)'/deserializedValue:' <Value> (length:X)' from type <DataTypeA> to <DataTypeB>``

## Where is this occurring and what does it mean?

This occurs when a change in the Metamodel of a Local Entity can’t be performed. This is because an Attribute Data Type in the Local Entity can’t be converted into another Data Type (for example, changing an attribute data type from Binary to Text) for local entities that already contain Data. 

**Note**: This only affects devices that contain data in the affected Local Entities.


## What is the impact of this error on the mobile application?

* The mobile application won't be upgraded and will be rolled back to the previous version cached in the device. Errors in runtime may be expected depending on the changes introduced.

* The upgrade of the App Resources and the Upgrade Local DB Metamodel occur at the same time. Only after both are successfully upgraded will the app be upgraded.  

## How to overcome this issue?

* Roll the app back to the version previously published in the environment and reassess the changes.

* To rectify the issue in affected devices:
    * Clean the cache and data from the app.
    * Reinstall the app.
