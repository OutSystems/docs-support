---
summary:
locale: en-us
guid: e8b5cd23-b031-4fca-b2ee-071f8a074def
app_type: traditional web apps, mobile apps, reactive web apps
---

# Reset Users authentication preferences

## Symptoms

You've been locked out of your Users eSpace and cannot login.

## Cause

Usually this happens when you activate Active Directory (with Windows Integrated) authentication with incorrect configurations, thus failing all logins.

## Resolution

To resolve this issue, please follow these instructions

1. Go to Service Center

2. Search for the Users eSpace

3. On the tab Tenants click on the default tenant

4. Change the following site properties to false:

    * UseActiveDirectoryLogin (Users)

    * UseIntegratedAuthenticationLogin (Users)

    * UseLDAPLogin (Users)

    * UseSAMLLogin (Users) (when present)

After that, you will be able to login on the Users eSpace with your previous credentials.

