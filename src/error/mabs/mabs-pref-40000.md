---
summary: Preference key <key> in the context <context> is not recognized.
tags:
guid: f36093fe-b533-42bb-a844-16117e6742dc
locale: en-us
app_type: mobile apps
---

# OS-MABS-PREF-40000

## Error message

`Preference key <key> in the context <context> is not recognized.`

## Cause

This error occurs when the application's extensibility configuration contains an invalid schema, containing an invalid key named **&lt;key&gt;** in the context **&lt;context&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

Fix the application extensibility configuration, following the [Property Schema](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema#property-schema) and try rebuilding your application.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PREF-40000).
