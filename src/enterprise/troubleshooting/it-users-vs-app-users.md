---
summary: 
locale: en-us
guid: de98a7b8-ecf1-4b7e-adbf-5cfdcb6f9894
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Understanding the difference between Service Center logins and Users login - IT Users vs Application Users

## Overview

OutSystems allows configuring multiple "User Providers". This means that, in an environment, multiple user spaces exist, and users with the same information (login name, user name, etc) may exist. You may refer to [this article](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_User_Management/End_Users_Authentication/Single_Sign-On) for more information on the topic.

## Default user providers

In a standard setup, you will find two distinct user spaces in an OutSystems environment:

- Application Users (managed under the Users "User Provider"). [More on application users](https://success.outsystems.com/Documentation/11/Developing_an_Application/Secure_the_Application/End_User_Management).

- IT Users (managed under the Service Center "User Provider"). These are the credentials used in Service Studio, Service Center and LifeTime. [More on IT Users](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Users).

There is also multi-tenancy: for a given User Provider, multiple "tenants" can exist (this is useful, for example, in SaaS applications). If you have multiple tenants for a given User Provider, each tenant has its own "user space". [More on multi-tenancy](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/How_to_Build_a_Multi-tenant_Application).

## My login works in Service Center but does not work in Users...

If you are having trouble logging in with a given username under Users, but are able to log in just fine in Service Center, your problem can be:

- your user in the Users provider is inactive

- your user in Users has a different password

- the entry for your Users object in the database has a different password, and you are not resetting it well

- Users application is configured for [external authentication](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Use_an_External_Authentication_Provider) and the user does not exist in the external authentication system - so login is not possible

- an issue of multi-tenancy (somehow your user from Users got moved to a different tenant)

In the opposite situation (you can login in Users but not in Service Center) you were probably never created as an IT user. In that situation, request that a user is created for you under Service Center / LifeTime.

