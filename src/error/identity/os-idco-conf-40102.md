---
summary: "OS-IDCO-CONF-40102 error in ODC occurs when automatic user creation is disabled for an external IdP, blocking end-user login."
tags:
  - Authentication
  - End-user Authentication
  - External Authentication
  - IdP
  - Troubleshooting
guid: a0fad8df-d275-460c-9b41-66ce4ed56230
locale: en-us
app_type: mobile apps, reactive web apps
platform-version: odc
figma:
outsystems-tools:
coverage-type:
  - unblock
audience:
  - Platform administrator
topic:
isautopublish: true
---

# OS-IDCO-CONF-40102

## Error message

`There was an unexpected error authenticating you. Try again. If the problem continues, contact your administrator. Displayed alongside the error code “OS-IDCO-CONF-40102.”`

## Cause

An end user attempted to log in with an external Identity Provider (IdP), but their account could not be created because the **_automatic user creation_** setting is disabled for this IdP configuration.

## Impact

The user cannot log in or access the app.

## Recommended Action

Depending on your organization's security policies, this error can be resolved in one of the following ways:

* **Enable automatic creation**: If users from this IdP should have accounts generated automatically upon their first successful authentication, navigate to your external IdP settings in ODC and toggle **_Automatic user creation_** to True.

* **Manual provisioning**: If automatic user creation is intentionally turned off for security reasons, the IT administrator must manually provision the user's profile in the system before the user attempts to log in again.
