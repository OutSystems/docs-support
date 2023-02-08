---
summary:
locale: en-us
guid: 77573d1b-9ee1-4e99-87a9-27af4a994376
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Resetting the admin password for IT users and end users

On occasion, you may need to reset the admin password for either IT Users or End users.

To achieve this, you may need to have access to the database to execute a direct update to the OSSYS_USER table. Please remember to be careful, running the database statement incorrectly can destroy other passwords in your system.

## Resetting the admin password for IT users

### Cloud

1. Ask another administrator to reset your password.

1. If there are no other administrator with access, please request a password reset by opening a new case at OutSystems Support Portal.

<div class="info" markdown="1">

OutSystems only accepts requests to reset the password of users with the administrator role in LifeTime. To reset the password of users with other roles (for example, Developer) should request an administrator to reset their password.

</div>

### On-premises

Run the following query on the Platform Server database:

```sql
UPDATE ossys_user
SET password = '<hash>'
WHERE username = 'admin'
and tenant_id in (SELECT id FROM ossys_tenant WHERE name = 'ServiceCenter');
```

<div class="info" markdown="1">

Obtain [here](https://globalsupport.outsystemsenterprise.com/HashPassword/) the hash for the password you want to use.

</div>

## Resetting the admin password for the Users application

### Cloud

**For OutSystems 11 Platform Server Release Jul.2019 or later** and **OutSystems 10 Platform Server 10.0.1014.0 or later**

Reset the admin password for the users application using Service Center. Check [here](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_Users/Access_the_Users_application#configure-users-administrator) the instructions to configure the administrator user.

**For other versions of OutSystems 11 or OutSystems 10 Platform Server**

Request the password reset by opening a [new case at OutSystems Support Portal](https://www.outsystems.com/goto/submit-support-case) .

### On-premises

**For OutSystems 11 Platform Server Release Jul.2019 or later** and **OutSystems 10 Platform Server 10.0.1014.0 or later**

Check [here](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_Users/Access_the_Users_application#configure-users-administrator) the instructions to configure the administrator user.

**For other versions of OutSystems 11 or OutSystems 10 Platform Server**

Run the following query on the Platform Server database:

```sql
UPDATE ossys_user
SET password = '<hash>'
WHERE username = 'admin'
and tenant_id in (SELECT id FROM ossys_tenant WHERE name = 'users');
```

<div class="info" markdown="1">

Obtain [here](https://globalsupport.outsystemsenterprise.com/HashPassword/) the hash for the password you want to use.

</div>
