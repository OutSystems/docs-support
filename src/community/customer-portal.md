---
summary: Learn how to manage your team access to the OutSystems online tools like Customer Portal, Support Portal and Licensing.
tags:
locale: en-us
guid: 5bd7f106-3784-4821-a603-0ad0c0fd8f82
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma:
---

# Managing your company permissions on OutSystems Customer Portal

As an admin, managing your team members and their permissions in the [OutSystems Customer Portal](https://www.outsystems.com/csportal/Team), you allow them to access a restricted digital platform. Here they can find information about your subscription, platform details, training, and support cases, ensuring the best adoption experience for everyone.

As a team member, if you don’t have access, reach out to your company’s OutSystems administrators. They’ll be able to invite you to join the team.

## Reaching the Customer Portal

Login into [OutSystems Community](https://www.outsystems.com/community) and click **My Platform > Customer Portal**.

Keep in mind that for security reasons, the credentials you use for your Community profile are not synced with the credentials for OutSystems consoles, ODC Portal for ODC, and LifeTime for O11.

## Managing members

In OutSystems Customer Portal, navigate to the Team pane:

On this screen, you can see everyone who is currently associated with your company. This includes those invited to join your Customer Portal (but haven’t yet) and the contacts OutSystems with partial access:

* **Active members**:

    * Have an OutSystems Community user account.
    * Are linked to the company and have permission to access digital properties such as the Customer Portal and Support Portal.

* **Pending members**:

    * Don’t have an OutSystems Community  account yet. However, they may have been invited to create one and join your team.
    * Will be able to access the Customer Portal and become effective members once they create an OutSystems Community account.

* **Support Contacts**:

    * Despite having an OutSystems Community or not, are part of one or more of your support cases. For example, when added in CC of a support case.
    * Have access only to the support cases where they were added to.

As Administrator, you have full visibility and control over who has access to your company’s area in the Customer Portal. Please ensure your team members are effectively allowed to do it, at all times.

### OutSystems Customer Portal permissions 

The rules to manage members differ depending on whether the infrastructure is O11 or ODC. For ODC, members are managed in the ODC Portal and then synchronized to the Customer Portal.

As teams grow significantly, permission management can get out of control. To help you manage that, there are 3 levels of access:

#### Company Admin

This represents a role that can oversee all the permissions and members of all your OutSystems subscriptions. Company Admins are able to:

* Access to OutSystems Customer Portal
* Manage your users and permissions for all your OutSystems subscriptions.
* Assign or remove other company administrators.
* Register support cases in infrastructures the user is associated with.
* Remove contacts.
* [Register](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/03_Get_a_license_file_for_an_environment#Registering_your_environment_(using_the_serial_number)), [release](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/05_How_to_free_up_an_existing_environment_in_licensing) environment slots, and download licenses (O11 self-managed only).
* Receive notifications regarding disruptive events.
* Receive license expiration email notifications.

OutSystems will set as the first **Company Admin**, the person that was identified as such in your initial purchase order. It can, however, be changed to your preference at a later stage.

The Company Admin can also have a role infrastructure-wise that can be set as suitable.

#### Infra Admin

This person will be able to:

* Access to OutSystems Customer Portal
* Manage your users and permissions for the infrastructures where he is set as administrator.
* Register support cases, [approve unauthorized cases](https://success.outsystems.com/Support/Account_and_Members_Management/Enhanced_security_for_OutSystems_support_cases), and view all cases of that infrastructure.
* [Register](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/03_Get_a_license_file_for_an_environment#Registering_your_environment_(using_the_serial_number)), [release](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/05_How_to_free_up_an_existing_environment_in_licensing) environment slots, and download licenses (O11 self-managed only).
* Receive notifications regarding maintenance and disruptive events.
* Receive license expiration email notifications.

OutSystems will set by default as the first Infrastructure administrator, the person that was identified as such in your initial purchase order. It can, however, be changed to your preference at a later stage.


#### Member

A regular user who is linked to your company and will have granular access to your tools:

* Access to OutSystems Customer Portal
* Can register support cases but will only be able to view the cases they have created.

### How to add a new member

#### In O11 infrastructures

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

Granting developer permissions through the Customer Portal is [audited in LifeTime](https://www.outsystems.com/tk/redirect?g=ff41a92e-5717-4a6c-9016-12acdb4de71f) as actions performed by the `Administrator` user. This `Administrator` user is separate from your LifeTime or Customer Portal administrators; it's a service user designated for integrations with OutSystems 11 Cloud, including the Customer Portal.

</div>

#### For ODC infrastructures

Users created in the ODC Portal are automatically added to your account in the Customer Portal, according to the following rules that are based on their ODC organization roles. In case they have a Community, no other action is required. However, if a Community account does not exist, the members marked as Pending will need to [create an OutSystems Community account](https://www.outsystems.com/community/) with the same email to complete their onboarding and benefit from [ODC Training Catalog](https://learn.outsystems.com/training/catalog/odc).

* ODC Administrator (built-in role) becomes an Infrastructure Admin;
* ODC Developer (built-in role) becomes a Member;
* ODC custom roles are based on the Support permissions:
    * Permission to “View all support cases” becomes an Infrastructure Admin;
    * Permission to “Open support cases” only becomes a Member.
    * Otherwise, the user is not created in the Customer Portal.

### Editing permissions for existing members

#### For O11 infrastructures

To change a user’s permissions click **Edit** under the **ACTION** column. You can also remove a user by clicking **Delete**.

#### For ODC infrastructures

To change a user’s permissions or remove them you must use the ODC Portal. Users updated in the ODC Portal are automatically updated in the Customer Portal, based on their deletion, deactivation, or changes in their ODC organization roles. 

### Defining the security contact

The security contact will receive all communications and notifications that are security-related. This contact may have other permissions.

The security contacts are those members that are added and have the **Role** set as **Security**.

On the **Security Contact** field, fill in the phone number.
This security contact can only be managed by users with **Company Admin** or **Infra Admin** permissions.

If you need assistance while managing your permissions [reach out to OutSystems Support](https://www.outsystems.com/goto/contact-outsystems-support).
