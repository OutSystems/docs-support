---
summary: Preference key <key> in <context> has a wrong type.
tags:
guid: 4eaf6851-f4c7-4770-b005-805cf8ed8bac
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-PREF-40002

## Error message

`Preference key <key> in <context> has a wrong type.`

## Cause

This error occurs when the application's extensibility configuration has key named **&lt;key&gt;** that is of the wrong type in the context **&lt;context&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

Fix the application extensibility configuration by fixing the key value type and retry rebuilding your application. You can find more information about the Property Schema [in our public documentation](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema#property-schema).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PREF-40002).
