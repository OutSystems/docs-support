---
summary: Learn how to manage your team access to the OutSystems online tools like Customer Portal, Support Portal and Licensing.
tags:
locale: en-us
guid: 5bd7f106-3784-4821-a603-0ad0c0fd8f82
app_type: traditional web apps, mobile apps, reactive web apps
---

# Managing your company permissions on OutSystems Customer Portal

Manage your team permissions without jumping in and out of different applications (Support Portal and Licensing Portal).

Permissions are managed in the [OutSystems Customer Portal](https://www.outsystems.com/cs-home/team/), an area accessible to users who:

* Have an OutSystems user account and are linked with your company.
* Were invited to join your company.

Not all company members are able to manage permissions but all have access so they may: 

* See the account information.
* Browse to discover their team members (and their permissions) in the OutSystems world.

<div class="info" markdown="1">

If you don’t have access, reach out to your company’s OutSystems administrators. They’ll be able to [invite you to join the team](#add-member).

</div>

## Reaching the Customer Portal

Login into [OutSystems Community](https://www.outsystems.com/community) and click **My Platform > Customer Portal**.


## Managing members

In OutSystems Customer Portal, navigate to the Team pane:

On this screen, you can see everyone who is currently associated with your company, including those invited to join your Customer Portal (but haven’t yet) and the contacts OutSystems with partial access:

* **Active members** are:

    * Those that have an outsystems.com user account.
    * Linked to your company and have permission to access outsystems.com online tools such as the Customer Portal, Support Portal, and Licensing Portal.

* **Pending members**:

    * Don’t yet have an outsystems.com user account (but were invited to create one and join your Customer Portal).
    * Will be able to access your Customer Portal and become effective Members when they create an outsystems.com account.

* **Support Contacts**:

    * Are those (with or without an outsystems.com user account) linked to one or more of your support cases. Such as, for example when added in cc.
    * Have access only to the support cases where they were added.

You have full visibility and control over who has access to your OutSystems account.

### OutSystems Customer Portal permissions 

As teams grow significantly, permission management can get out of control. To help you manage that, there are 3 levels of access:

#### Company Admin

This represents a role that can oversee all the permissions and members of all your OutSystems subscriptions. Company Admins are able to:


* Access to OutSystems Customer Portal
* Manage your users and permissions for each and every one of your OutSystems subscriptions.
* Assign or remove other company administrators.
* Register support cases in infrastructures the user is associated with.
* Remove contacts.
* [Register](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/03_Get_a_license_file_for_an_environment#Registering_your_environment_(using_the_serial_number)), [release](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/05_How_to_free_up_an_existing_environment_in_licensing) environment slots, and download licenses.
* Receive notifications regarding disruptive events.
* Receive license expiration email notifications.


OutSystems will set as the first **Company Admin**, the person that was identified as such in your initial purchase order. It can, however, be changed to your preference at a later stage.

The Company Admin can also have a role infrastructure-wise that can be set as suitable.

#### Infra Admin

This person will be able to:

* Access to OutSystems Customer Portal
* Manage your users and permissions for the infrastructures where he is set as administrator.
* Register support cases, [approve unauthorized cases](https://success.outsystems.com/Support/Account_and_Members_Management/Enhanced_security_for_OutSystems_support_cases), and view all cases of that infrastructure.
* [Register](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/03_Get_a_license_file_for_an_environment#Registering_your_environment_(using_the_serial_number)), [release](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/05_How_to_free_up_an_existing_environment_in_licensing) environment slots, and download licenses.
* Receive notifications regarding maintenance and disruptive events.
* Receive license expiration email notifications.

OutSystems will set by default as the first Infrastructure administrator, the person that was identified as such in your initial purchase order. It can, however, be changed to your preference at a later stage.


#### Member

A regular user who is linked to your company and will have granular access to your tools:

* Access to OutSystems Customer Portal
* Can register support cases but will only be able to view the cases they have created.

### How to add a new member

At your Customer Portal: 

1. click **Team** on the left-side menu
1. and then the **Add Team Member** button.


Here you can:

* Specify if that person should have **Company permissions** (this means that the Company Admin permission will be granted).
* Select the individual permissions he or she should have for each of your OutSystems infrastructures, for example, be an Infra Admin.
* Invite this person to configure their initial developer account in LifeTime:
    * This option only applies to OutSystems Cloud and hybrid infrastructures. Aditionally, in Sentry subscriptions this option isn't available.
    * The username will be the same as their email.
    * The password will be selected by the new member when following the invitation link in their email.


The option to grant Development Permissions is only available while adding new users.


<div class="info" markdown="1">

The option to grant **Development Permissions** is only available while adding new users. 

[IT users' permissions](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Users) can be managed by your Administrators in your infrastructure's management console, LifeTime.

</div>


### Editing permissions for existing members

To change a user’s permissions click **Edit** under the **ACTION** column. You can also remove a user by clicking **Delete**.


### Defining the security contact

The security contact will receive all communications and notifications that are security-related. This contact may have other permissions.

The security contacts are those members that are added and have the **Role** set as **Security**.


On the **Security Contact** field, fill in the phone number.
This security contact can only be managed by users with **Company Admin** or **Infra Admin** permissions.

If you need assistance while managing your permissions [reach out to OutSystems Support](https://www.outsystems.com/goto/contact-outsystems-support).
