---
summary: 
locale: en-us
guid: eafe431f-ca4d-4305-93bc-0b964fb9efc6
app_type: traditional web apps, mobile apps, reactive web apps
---

# Known issue - Number of local storage entity attributes limited by SQLite on Android

It came to our attention that mobile applications built using OutSystems were having problems when Local Storage entities have a large number of attributes on Android devices.

**Am I affected by this?**

This issue happens if you have an Android mobile app with local storage entities, with a large number of attributes or whenever a complex SQL query (several joins for instance) results in a large set of attributes.

**Technical Information**

Internally, the SQLite plugin makes use of Android built-in JSON libraries, which have been known to leak memory as seen here and here.

From our internal tests, we’ve identified that when using a large amount of attributes in an entity, or whenever a SQL query results in a large set of attributes, an Out Of Memory exception is thrown due to the way JSON Objects are being handled internally in Android.

**What we did and are doing**

We’ll add warnings to the development experience to warn the developer whenever an entity with more than 50 attributes is created or whenever a query result exceeds 50 attributes.

This is an underlying technology problem, and we are limited in what we can do to fix the problem. Therefore, by introducing this limitation, we’re solving the issue.
