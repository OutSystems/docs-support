---
summary:
locale: en-us
guid: 77573d1b-9ee1-4e99-87a9-27af4a994376
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Resetting the admin password for IT users and end users

On occasion, while using the default method of authentication in OutSystems, you may need to reset the admin password for either IT users or end users.

To achieve this, you may need to have access to the database to execute a direct update to the OSSYS_USER table. Please remember to be careful, running the database statement incorrectly can destroy other passwords in your system.

## Resetting the admin password for IT users

### Cloud

1. Ask another administrator to reset your password.

1. If there are no other administrator with access, please request a password reset by opening a new case at OutSystems Support Portal.

<div class="info" markdown="1">

OutSystems only accepts requests to reset the password of users with the administrator role in LifeTime. To reset the password of users with other roles (for example, Developer) should request an administrator to reset their password.

</div>

### On-premises

<div class="warning" markdown="1">

To reset the admin password for the Users application in an on-premises infrastructure, you need access to the database to execute a direct update to the OSSYS_USER table. Running the database statement incorrectly can destroy other passwords in your system.

</div>

1. Create [here](https://globalsupport.outsystemsenterprise.com/HashPassword/) the hash with the new password you want to use.

1. Run the following query on the Platform Server database:

        UPDATE ossys_user
        SET password = '<hash>'
        WHERE username = 'admin'
        and tenant_id in (SELECT id FROM ossys_tenant WHERE name = 'ServiceCenter');

## Resetting the admin password for the Users application (end users)

### Cloud

**For OutSystems 11 Platform Server Release Jul.2019 or later** and **OutSystems 10 Platform Server 10.0.1014.0 or later**

Reset the admin password for the Users application using Service Center. Check [here](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_Users/Access_the_Users_application#configure-users-administrator) the instructions to access the Users application to then [configure the administrator user](https://success.outsystems.com/documentation/11/developing_an_application/secure_the_application/end_users/configure_the_administrator_user_of_the_users_app/).

**For older versions of OutSystems 11 or OutSystems 10 Platform Server**

Request the password reset by opening a [new case at OutSystems Support Portal](https://www.outsystems.com/goto/submit-support-case).

### On-premises

**For OutSystems 11 Platform Server Release Jul.2019 or later** and **OutSystems 10 Platform Server 10.0.1014.0 or later**

Check [here](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_Users/Access_the_Users_application#configure-users-administrator) the instructions to access the Users application to then [configure the administrator user](https://success.outsystems.com/documentation/11/developing_an_application/secure_the_application/end_users/configure_the_administrator_user_of_the_users_app/).

**For any versions of OutSystems 11 or OutSystems 10 Platform Server**

<div class="warning" markdown="1">

To reset the admin password for the Users application in an on-premises infrastructure, you need access to the database to execute a direct update to the OSSYS_USER table. Running the database statement incorrectly can destroy other passwords in your system.

</div>

1. Create [here](https://globalsupport.outsystemsenterprise.com/HashPassword/) the hash with the new password you want to use.

1. Run the following query on the Platform Server database:

        UPDATE ossys_user
        SET password = '<hash>'
        WHERE username = 'admin'
        and tenant_id in (SELECT id FROM ossys_tenant WHERE name = 'users');

