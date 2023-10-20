---
summary:
locale: en-us
guid: e8b5cd23-b031-4fca-b2ee-071f8a074def
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Reset Users authentication preferences

## Symptoms

You've been locked out of your [Users app](https://www.outsystems.com/tk/redirect?g=2cbb2e7d-9936-4bb4-8791-240ade1d1ad6) and can't login.

## Cause

Usually, this happens when you activate Active Directory (with Windows Integrated) authentication with incorrect configurations, thus failing all logins.

## Resolution

To resolve this issue, please follow these instructions

1. Go to Service Center > Factory > Modules

1. Search for the Users module

1. On the tab Tenants click on the default tenant

1. Change the following site properties to false:

    * UseActiveDirectoryLogin (Users)

    * UseIntegratedAuthenticationLogin (Users)

    * UseLDAPLogin (Users)

    * UseSAMLLogin (Users) (when present)

After that, you will be able to log into Users with your previous credentials.

