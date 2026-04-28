---
summary:
tags: external identity provider, profile matching
guid: d6096c18-41ad-41b7-a939-beed1039956c
locale: en-us
app_type: mobile apps, reactive web apps
platform-version: odc
figma:
outsystems-tools:
coverage-type:
  - unblock
audience:
topic:
isautopublish: true
---

# OS-IDCO-CONF-40001

## Error message

`The login with the external identity provider fails. Try again. If this keeps happening, contact your administrator. Displayed alongside the error code OS-IDCO-CONF-40001.`

## Cause

The system cannot find a user profile matching the field data from the external Identity Provider (IdP). This occurs because the username claim mapping is either missing or incorrectly configured on the external IdP side.

## Impact

The user cannot authenticate or log in to the app.

## Recommended action

To resolve this error:

* **Verify IdP configuration**: Check the external IdP settings to ensure the username claim mapping is present and is sending the correct data.

* **Verify ODC mapping**: Confirm that the mapping configured within the ODC external Idp settings exactly matches the claims sent by the external IdP.
