---
summary:
tags: external identity provider, profile matching
guid: d1b7f555-e0ae-4e21-b6f1-566878c9a86d
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

# OS-IDCO-AUTH-40101

## Error message

`The login attempt with the external identity provider failed because your account has been deactivated. Displayed with error code "OS-IDCO-CONF-40xxx."`

## Cause

The user's account status in ODC is set to inactive.

## Impact

The user is unable to authenticate and log in to the app.

## Recommended action

This error can be resolved in the following ways:

* **In ODC Portal**: Navigate to **Management > Users**, search for the specific user, click the three dots, and select **Activate User** from the drop-down menu to restore the user’s authentication capabilities.

* **Using APIs**: Use the [ODC user management APIs](https://success.outsystems.com/documentation/outsystems_developer_cloud/odc_rest_apis/api_references/user_and_access_management_api/) to programmatically update the user's status to active.
