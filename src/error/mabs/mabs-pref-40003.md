---
summary: <context> must have the format [].
tags:
guid: 6ea6b45d-c137-42e4-ab53-aaffa911759c
locale: en-us
app_type: mobile apps
---

# OS-MABS-PREF-40003

## Error message

`<context> must have the format [].`

## Cause

This error occurs when the application's extensibility configuration has some property named **&lt;context&gt;** that should be a json array ( [] ) but isn't.

## Impact

Users can't generate the application package.

## Recommended action

Fix the application extensibility configuration, following the [Property Schema](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema#property-schema) and try rebuilding your application.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PREF-40003).
