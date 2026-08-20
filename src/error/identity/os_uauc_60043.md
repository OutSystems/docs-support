---
summary: OS-UAUC-60043 ODC error occurs when the profile target for an invitation becomes invalid due to authentication configuration changes, blocking onboarding.
tags:
  - Authentication
  - End-user Authentication
  - External Authentication
  - IdP
  - Troubleshooting
guid: 94c36ff0-fa48-46cd-8a7d-012e28c6b047
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

# OS-UAUC-60043

## Error message

`Couldn't complete onboarding because the authentication configuration changed. Contact your administrator.`

## Cause

The profile target associated with the invitation is no longer valid, as it changed after the invitation was sent.

## Impact

The user cannot complete onboarding.

## Recommended action

To resolve this error, you should:

* Contact your administrator and verify the identity provider configurations.

* Ask the administrator to resend the invitation.
