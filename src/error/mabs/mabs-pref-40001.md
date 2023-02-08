---
summary: Preference key <key> in <context> wasn't found.
tags:
guid: b93a43d1-d235-4798-8b13-4e62687aeead
locale: en-us
app_type: mobile apps
platform-version: o11
---

# OS-MABS-PREF-40001

## Error message

`Preference key <key> in <context> wasn't found.`

## Cause

This error occurs when the application's extensibility configuration is missing a mandatory key named **&lt;key&gt;** in the context **&lt;context&gt;**.

## Impact

Users can't generate the application package.

## Recommended action

Fix the application extensibility configuration, adding the key to the context and try rebuilding your application. You can find more information about the Property Schema [in our public documentation](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema#property-schema).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PREF-40001).
