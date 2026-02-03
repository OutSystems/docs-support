---
summary: Explore end user management and classification in OutSystems 11 (O11), including internal, external, and anonymous user distinctions and capacities.
tags: 
locale: en-us
guid: 907b0fd3-bc46-4391-aae2-673296d795d9
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma:
coverage-type:
  - remember
  - understand
topic:
  - user-types
  - users-licensing
---

# End Users

An end user is a unique individual who uses your OutSystems apps. Each non-anonymous end user who interacts with your apps counts toward the end user capacities established on your subscription. People who develop your OutSystems apps but do not use them are not considered end users.

## Internal and external end users

You license internal and external end-user capacities separately on your subscription. Each end user of your OutSystems applications is classified as either internal or external. Internal is intended for employees and contractors of your organization. External is for your customers, partners, or other external parties who use your OutSystems apps.

By default in OutSystems, all end users are classified as internal until you configure the domains that you own. You only need to configure your domains when you license external end-user capacity on your subscription because doing so allows you to track the internal and external end-user counts separately.

* For ODC (OutSystems Developer Cloud) you can [define your domains in the ODC Portal](https://www.outsystems.com/tk/redirect?g=f3211746-db90-4515-8175-888d00e14bd9).
* For OutSystems 11, [domains are configured in Service Center](https://www.outsystems.com/tk/redirect?g=8cb73d92-a60d-4133-9f95-67ef4505932d).

When you do this, all end users with email addresses belonging to these domains are classified as internal, and all end users with email addresses outside these domains are classified as external.

For example, if your organization owns `example.com` and the end user's email is `adam@example.com`, then the end user will be classified as internal. Make sure to configure all the email domains used by employees who use your apps, including domains owned by your parent or affiliate organizations.  

<div class="info" markdown="1">

When an end-user has no email address stored on their profile, such as when you only capture a mobile phone number, this is counted as an internal end-user.  

</div>

Independent Software Vendors (ISVs) and Managed Services Providers (MSPs) delivering apps to their clients should configure the domains of their clients (rather than the domains of their own company) as internal. Internal and external end users are from the perspective of the client that is licensing usage of apps from the ISV or MSP, not from the perspective of the ISV or MSP that is licensing the OutSystems platform.

## Anonymous end users

Anonymous end users don't count toward the end user capacities specified in your subscription. Users who use your apps and who don't log in and also don't share any personally identifiable information (name, email, mobile phone, etc.) are anonymous. For example, people who visit your website (that is an OutSystems app) and just browse the information without logging in or providing personal information are anonymous end users.

## How end users are counted

Each OutSystems subscription has an associated end-user capacity: the maximum number of unique individuals who use the apps. OutSystems consoles provide an estimate of the current usage of this capacity based on the user records in the OutSystems database:

* By default, each user record is assumed to be a unique individual.

* If you use shared email addresses, you may end up with an incorrect user count.

* For **OutSystems Developer Cloud**, users that haven't logged in at least once, don't count towards the user count.

* For **OutSystems 11**:

    * If the same individual uses apps in different production runtimes, it is counted in the estimate presented for each of the production runtimes.

    * For the purpose of counting users, the platform deduplicates records with the same email address or login, as long as they are assigned to different [default tenant](https://success.outsystems.com/documentation/how_to_guides/development/how_to_build_a_multi_tenant_application/#multi-tenancy-in-outsystems-platform). This means that users that exist in the default tenant (different [user providers](intro.md#User-providers)) will count as one unique user. Note that the deduplication does not apply to users assigned to non-default tenants. This means that records with the same email address or login that belong to non-default tenants (same or different User Providers) will still count as distinct users.

    * Users without an email in neither the **Email** nor **Username** fields always count as internal.

    * The values displayed on the **User Distribution Per User Provider** table in Service Center show the total number of users without deduplication.

    * From Platform Server version 11.11.3 and higher, users are counted by deduplicating records with the same email address or login, as long as they are assigned to different [default tenant](https://success.outsystems.com/documentation/how_to_guides/development/how_to_build_a_multi_tenant_application/#multi-tenancy-in-outsystems-platform), across user providers. In earlier versions, all users were counted individually without deduplication.

    * Versions prior to Platform Server 11.7.0 don't support classifying end users as internal or external, so customers should update to the latest version to take advantage of this. Older licensing models licensed "named" users, which didn't require end users to be classified as internal or external.

## End user limits

OutSystems subscriptions typically include rights to run applications serving up to a specific number of internal end users and a specific number of external end users, with options for upgrading these end-user capacities that vary by subscription. When you exceed the internal or external end-user capacities specified on your subscription, you need to upgrade your subscription to remain in compliance with the license terms. Please contact your OutSystems sales representative for assistance.

* In **ODC**, because there's a single production runtime, all your users are licenced individually.

* In **OutSystems 11** infrastructures, customers may have more than one production runtime where their apps are hosted and delivered to end users. When the same individual accesses apps hosted on multiple runtimes, this individual is tracked as an end user in each and contributes to the reported end user count in each.
Nonetheless, the individual will count as a unique user towards the end user limits.

## Managing your end users

You may periodically deactivate end users who you know won't continue to use your applications, and these users, once deactivated, will no longer count toward your licensed end-user capacities. For example, when an employee leaves, you would deactivate this user because they no longer need access to apps you've built for your employees.

* In **ODC** you can manage end users in the [ODC Portal](https://www.outsystems.com/tk/redirect?g=9e0fb9b7-d2b0-419f-a5d8-5b5ed730da5e).
* In **OutSystems 11**, you can manage end users through the [Users](https://www.outsystems.com/tk/redirect?g=2cbb2e7d-9936-4bb4-8791-240ade1d1ad6) console, or manage end users programmatically using the [Users API](https://www.outsystems.com/tk/redirect?g=ce2ac90a-1911-4fcf-8c8d-016110b3f8e2).

## Related resources

* [Classify users in ODC](https://www.outsystems.com/tk/redirect?g=f3211746-db90-4515-8175-888d00e14bd9)
* [Classify users in O11](https://www.outsystems.com/tk/redirect?g=8cb73d92-a60d-4133-9f95-67ef4505932d)
* [O11 Multi-tenant applications](https://www.outsystems.com/tk/redirect?g=6e1bb224-5f33-4233-adc5-57dc98793113): managing different cohorts of users from different tenants.
