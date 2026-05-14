---
summary: OS-IDCO-CONF-40001 error in OutSystems Developer Cloud (ODC) means the username claim mapping is missing or misconfigured in the external IdP.
tags:
  - Authentication
  - End-user Authentication
  - External Authentication
  - IdP
  - Troubleshooting
guid: d6096c18-41ad-41b7-a939-beed1039956c
locale: en-us
app_type: mobile apps, reactive web apps
platform-version: odc
figma:
outsystems-tools:
coverage-type:
  - understand
  - apply
  - unblock
audience:
  - Platform administrator
topic:
isautopublish: true
---

# OS-IDCO-CONF-40001

## Error message

`There was an unexpected error authenticating you. Try again. If the problem continues, contact your administrator. Displayed alongside the error code "OS-IDCO-CONF-40001."`

## Cause

The system cannot find a user profile matching the field data from the external IdP. This occurs because the username claim mapping is either missing or incorrectly configured on the external IdP side.

## Impact

The user cannot authenticate or log in to the app.

## Recommended action

To resolve this error:

* **Verify IdP configuration**: Check the external IdP settings to ensure the username claim mapping is present and is sending the correct data.

* **Verify ODC mapping**: Confirm that the mapping configured within the ODC external IdP settings exactly matches the claims sent by the external IdP.
