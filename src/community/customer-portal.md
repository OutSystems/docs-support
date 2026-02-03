---
summary: Learn how to manage your team's access to OutSystems online tools such as Customer Portal, Support Portal, and Licensing.
tags:
locale: en-us
guid: 5bd7f106-3784-4821-a603-0ad0c0fd8f82
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma:
---

# Manage your company permissions in OutSystems Customer Portal

As an admin, you can manage your team members and their permissions in the [OutSystems Customer Portal](https://www.outsystems.com/csportal/Team). This gives them access to a restricted digital platform where they can find information about your subscription, platform details, training, and support cases.

As a team member, if you don't have access, contact your company's OutSystems administrators. They can invite you to join the team.

## Access the Customer Portal

Sign in to [OutSystems Community](https://www.outsystems.com/community) and click **My Platform > Customer Portal**.

For security reasons, the credentials you use for your Community profile aren't synced with the credentials for OutSystems consoles, ODC Portal for ODC, and LifeTime for O11.

## Manage members

In OutSystems Customer Portal, go to the **Team** tab.

This screen shows everyone currently associated with your company, including those invited to join your Customer Portal (but haven't yet) and contacts with partial access:

* **Active members**:

    * Have an OutSystems Community user account.
    * Are linked to the company and have permission to access digital properties such as the Customer Portal and Support Portal.

* **Pending members**:

    * Don't have an OutSystems Community account yet, but may have been invited to create one and join your team.
    * Can access the Customer Portal and become effective members after they create an OutSystems Community account.

* **Support contacts**:

    * Are part of one or more of your support cases, whether or not they have an OutSystems Community account. For example, they may have been added in CC of a support case.
    * Have access only to the support cases where they were added.

As an administrator, you have full visibility and control over who has access to your company's area in the Customer Portal. Ensure your team members have the appropriate access at all times.

### OutSystems Customer Portal permissions

The rules for managing members differ depending on whether the infrastructure is O11 or ODC. For ODC, members are managed in the ODC Portal and then synchronized to the Customer Portal.

To manage permissions across growing teams, there are three levels of access:

#### Company admin

Company admins can oversee all the permissions and members of all your OutSystems subscriptions. Company admins can:

* Access OutSystems Customer Portal.
* Manage users and permissions for all your OutSystems subscriptions.
* Assign or remove other company administrators.
* Register support cases in infrastructures the user is associated with.
* Remove contacts.
* [Register environments](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/03_Get_a_license_file_for_an_environment#Registering_your_environment_(using_the_serial_number)).
* [Release environment slots](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/05_How_to_free_up_an_existing_environment_in_licensing)
* Download licenses (O11 self-managed only).
* Receive notifications about disruptive events.
* Receive license expiration email notifications.

OutSystems sets the first **Company admin** as the person identified as such in your initial purchase order. You can change this later.

The company admin can also have an infrastructure-specific role.

#### Infrastructure admin

Infrastructure admins can:

* Access OutSystems Customer Portal.
* Manage users and permissions for the infrastructures where they are set as administrator.
* Register support cases, [approve unauthorized cases](https://success.outsystems.com/Support/Account_and_Members_Management/Enhanced_security_for_OutSystems_support_cases), and view all cases for that infrastructure.
* [Register](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/03_Get_a_license_file_for_an_environment#Registering_your_environment_(using_the_serial_number)), [release](https://success.outsystems.com/Support/Enterprise_Customers/Licensing/Manage_and_Upgrade/05_How_to_free_up_an_existing_environment_in_licensing) environment slots, and download licenses (O11 self-managed only).
* Receive notifications about maintenance and disruptive events.
* Receive license expiration email notifications.

By default, OutSystems sets the first infrastructure administrator as the person identified as such in your initial purchase order. You can change this later.

#### Member

A regular user who is linked to your company and has granular access to your tools:

* Access OutSystems Customer Portal (read-only):
    * Home
    * Subscription
    * Analytics
    * My Training
* Register support cases, but can only view cases they created.

### Add a new member

#### For O11 infrastructures

In your Customer Portal:

1. Click **Team** in the left-side menu.
1. Click **Add Team Member**.

Complete the following:

* Enter the email address to receive the invite.
* Select their role within the team.
* Specify what type of **Company permissions** (Member or Admin) this person has.
* Select the individual permissions they should have for each of your OutSystems infrastructures, for example, Infrastructure admin (optional).
* Invite this person to configure their initial developer account in LifeTime:
    * This option only applies to OutSystems Cloud and hybrid infrastructures. This option isn't available for Sentry subscriptions.
    * The username is the same as their email.
    * The new member selects the password when following the invitation link in their email.

<div class="info" markdown="1">

The option to grant **Development Permissions** is only available when adding new users.

Your administrators can manage [IT users' permissions](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Users) in your infrastructure's management console, LifeTime.

Granting developer permissions through the Customer Portal is [audited in LifeTime](https://www.outsystems.com/tk/redirect?g=ff41a92e-5717-4a6c-9016-12acdb4de71f) as actions performed by the `Administrator` user. This `Administrator` user is separate from your LifeTime or Customer Portal administrators; it's a service user designated for integrations with OutSystems 11 Cloud, including the Customer Portal.

</div>

#### For ODC infrastructures

Users created in the ODC Portal are automatically added to your account in the Customer Portal, based on their ODC organization roles. If they have a [Community account](intro.md), no other action is required. If a Community account doesn't exist, members marked as Pending need to [create an OutSystems Community account](https://www.outsystems.com/community/) with the same email to complete their onboarding and access the [ODC Training Catalog](https://learn.outsystems.com/training/catalog/odc).

* ODC Administrator (built-in role) becomes an infrastructure admin.
* ODC Developer (built-in role) becomes a member.
* ODC custom roles are based on the Support permissions:
    * Permission to "View all support cases" becomes an infrastructure admin.
    * Permission to "Open support cases" only becomes a member.
    * Otherwise, the user isn't created in the Customer Portal.

### Edit permissions for existing members

#### For O11 infrastructures

To change a user's permissions, click **Edit** under the **Action** column. To remove a user, click **Delete**.

#### For ODC infrastructures

To change a user's permissions or remove them, use the ODC Portal. Users updated in the ODC Portal are automatically updated in the Customer Portal, based on their deletion, deactivation, or changes in their ODC organization roles.

### Define the security contact

The security contact receives all security-related communications and notifications. This contact may have other permissions.

Security contacts are members that have the **Role** set to **Security**.

In the **Security Contact** field, enter the phone number.
Only users with **Company admin** or **Infrastructure admin** permissions can manage the security contact.

If you need assistance managing your permissions, [contact OutSystems Support](https://www.outsystems.com/goto/contact-outsystems-support).
