---
summary: Know the difference between Service Center and LifeTime Roles and what happens when a new environment is registered in LifeTime.
tags: lifetime; support-Application_Lifecycle;
---

# Service Center and LifeTime Roles

Service Center and LifeTime Roles have different scope and granularity. While a Role in Service Center applies only to that specific environment, a Role in LifeTime applies across all environments.

An IT User in LifeTime can only have one Role which specifies the IT user permissions in each environment of the infrastructure. IT user permissions can be further configured by granting specific permissions per application in each of the environments.

## Creating new LifeTime roles

By default, LifeTime has two built-in roles - Administrator and Developer - to address the simplest infrastructure security configuration: a single team developing all applications and an IT administrator responsible for managing the infrastructure.

If you need to enforce more complex security policies across the infrastructure, you need to create new and specific Roles for IT users in LifeTime. Check the [product documentation](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Teams/Create_an_IT_Role) to learn how to create new Roles.

## What happens when a new environment is registered in LifeTime

When a new environment is registered in LifeTime, the existing Service Center Roles are not imported to LifeTime.

If you were previously managing the users and roles of your OutSystems environments in Service Center, when you register those environments in LifeTime you must rethink the security policy of the infrastructure.

If you already know which roles the IT users will have, it is much easier to create those Roles in LifeTime beforehand. Then, in the process of registering a new environment, LifeTime asks you to choose the role for the imported users, and having them already created allows you to set them right on that moment and in a single place. If you choose not to create your roles beforehand, you’ll have to select one of the default roles, and later on create the roles and edit each imported IT user and set the right role for him.

Since in LifeTime the scope of roles is across environments, it is recommended that you review the users which should remain with Administrator role after importing environments. For example, a user with Administrator role in Development is also an administrator in Production.

## Examples

The following examples illustrate how to achieve in LifeTime the same permissions model you previously had in Service Center.

**Example 1**

John Penn is an external developer and only needs permissions to publish the Mobile Sales in the Development Environment.

Permissions in Service Center
:   There is **Mobile Sales Developer** role in the Development Environment. John Penn is assigned with that role.

Permissions in LifeTime
:   Create an **External Developer** role that does not have permissions in any environment, and assign John Penn with that role. Then increase John's permissions for the Mobile Sales application, letting him change and deploy that application in Development.

**Example 2**

Lisa Carlson also works in the Mobile Sales team. She is able to deploy to Development and Quality Assurance.

Permissions in Service Center
:   There is a **Mobile Sales Developer** role in the Quality Assurance environment, having the same permissions as in the Development environment. Lisa Carlson is assigned to that role in both environments.

Permissions in LifeTime
:   Assign Lisa the **External Developer** role and increase her permissions for the Mobile Sales application, letting her deploy in both Development and Quality Assurance.

**Example 3**

The architecture team decides to add one more module to the Mobile Sales application. The permissions must be updated to let the developers change that module.

Permissions in Service Center
:   In Development and Quality Assurance, the **Mobile Sales Developer** role include permissions for the new module.

Permissions in LifeTime
:   Since the permissions are managed by application, nothing needs to be changed.
