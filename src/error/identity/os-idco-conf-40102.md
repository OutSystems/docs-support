---
summary: "OS-IDCO-CONF-40102 error in ODC occurs when a user logs in with the wrong account or automatic user creation is disabled for the IdP."
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
  - automatic-user-creation
isautopublish: true
---

# OS-IDCO-CONF-40102

## Error message

`There was an unexpected error authenticating you. Try again. If the problem continues, contact your administrator. Displayed alongside the error code “OS-IDCO-CONF-40102.”`

## Cause

An end user attempted to log in with an external Identity Provider (IdP) using the wrong account. Alternatively, the IdP couldn't create the account because **Automatic user creation** is disabled for this IdP configuration.

## Impact

The user cannot log in or access the app.

## Recommended Action

Depending on your organization's security policies, this error can be resolved in one of the following ways:

* **Log in with the correct account**: Verify that the account used to log in is your actual account. If not, log out, log in with the correct account, and try again.

* **Enable automatic user creation**: If users from this IdP need accounts generated automatically on their first successful authentication, go to your external IdP settings in ODC and set **Automatic user creation** to **True**.

* **Provision users manually**: If you turned off automatic user creation intentionally for security reasons, the IT administrator must provision the user's profile in the system. The user then logs in again.
