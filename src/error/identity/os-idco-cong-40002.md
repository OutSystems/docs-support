---
summary: OS-IDCO-CONF-40002 in OutSystems Developer Cloud (ODC) fails when an external IdP email is a duplicate; remove the conflicting profile to unblock.
tags:
  - Authentication
  - End-user Authentication
  - External Authentication
  - IdP
  - Troubleshooting
guid: b8c9d0e1-f2a3-4b5c-6d7e-8f9a0b1c2d3e
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

# OS-IDCO-CONF-40002

## Error message

`There was an unexpected error authenticating you. Try again. If the problem continues, contact your administrator. Displayed alongside the error code "OS-IDCO-CONF-40002."`

## Cause

This error occurs when an end user attempts to log in via an external IdP, but the system encounters a data conflict. Specifically, the system tries to update a profile with an email address that is already associated with a different existing user profile from another IdP.

## Impact

The user is blocked from logging in and cannot access the app.

## Recommended Action

To resolve this error, you should:

* **Remove Conflicts**: Identify and delete the redundant or conflicting user profile in the database (e.g., the duplicate profile created by an initial SAML login attempt).

* **Retry Login**: Once the duplicate is removed, the user should retry the login process; the system should then correctly update the intended profile.

* **Audit IdP Configuration**: Review the Idp configurations to determine how account linking is managed when duplicate emails are encountered across different IdPs.
