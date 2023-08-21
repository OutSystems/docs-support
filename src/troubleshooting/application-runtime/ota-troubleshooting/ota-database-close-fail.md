---
summary: Failed to close database cannot be closed while a transaction is in progress.
locale: en-us
guid: BEA72D64-7BE3-4509-BFFC-7DE599AA2703
app_type: mobile apps
platform-version: o11
figma:
---

# Failed to close database cannot be closed while a transaction is in progress

## What are the errors?

``Database <Local_DB_Id> failed to close database cannot be closed while a transaction is in progress.``

## Where is this occurring and what does it mean?

This error occurs when the app tries to close the database connection on window unload (when the app is closed). Sometimes, when this kind of event happens, a transaction may still be happening and this error occurs.

This error is just informative and its existence should not impact the app. This situation occurs more frequently in apps with complex database logic or high data volumes.

## What is the impact of this error on the mobile application?

No impact on the application is expected.

## How to overcome this issue?

No action necessary.
