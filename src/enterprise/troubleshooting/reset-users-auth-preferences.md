---
summary: Explore how to regain access to the Users app in OutSystems 11 (O11) when locked out due to incorrect external authentication configurations.
locale: en-us
guid: e8b5cd23-b031-4fca-b2ee-071f8a074def
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: authentication, user management, security, troubleshooting, configuration
audience:
  - platform administrators
  - full stack developers
outsystems-tools:
  - service studio
  - users application
coverage-type:
  - unblock
---

# Unblock access to Users app

## Symptoms

You've been locked out of your [Users app](https://www.outsystems.com/tk/redirect?g=2cbb2e7d-9936-4bb4-8791-240ade1d1ad6) and can't login.


## Cause

Usually, this happens when you activate **External Authentication** with incorrect configurations, thus failing all logins.

For more infomation about external authentication configurations, refer to [Use an External Authentication Provider](https://success.outsystems.com/documentation/11/managing_the_applications_lifecycle/manage_it_users/use_an_external_authentication_provider/)

## Resolution

If your authentication configuration is incorrect and prevents you from logging in using external authentication, you can still log in with an administrator account (it must be a user with the **UserManager** role) by navigating to the default Users app login page. This bypasses the configured authentication method, allowing you to log in and fix the incorrect settings.

The default Users app login page is available at: `https://<your_server_name>/Users/Login`.aspx

For more information on how to create an admin user, refer to [Configure the Administrator user of the Users app](https://success.outsystems.com/documentation/11/developing_an_application/secure_the_application/end_users/configure_the_administrator_user_of_the_users_app/).



