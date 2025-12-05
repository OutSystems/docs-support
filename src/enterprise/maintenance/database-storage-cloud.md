---
summary: OutSystems 11 (O11) supports SQL Server or Oracle RDS databases with autogrow features on OutSystems Cloud.
locale: en-us
guid: e0ed7b1b-f7cc-42cb-9b6d-d36c808e7f0e
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise%20Customers?node-id=618:298
tags: database management, cloud infrastructure, data storage, performance optimization, best practices
audience:
  - platform administrators
  - full stack developers
  - backend developers
  - tech leads
  - infrastructure managers
outsystems-tools:
  - lifetime
  - service studio
coverage-type:
  - unblock
  - understand
---

# Database storage on OutSystems Cloud

OutSystems Cloud can run with either SQL Server or Oracle RDS databases. Upon purchase, an initial database storage is provisioned. Storage autogrows as needed.

## What does the value I see in LifeTime mean?

In the **Environments** screen in LifeTime, you can click on an environment card to see the occupied space of each database as well as the total available space.

<div class="info" markdown="1">

Starting with LifeTime Management Console 11.25.0, the panel that shows free database space is no longer available for Enterprise PaaS infrastructures. Personal Environments still display this section so that you can check the storage available in the free offer. For Enterprise PaaS environments, rely on your database monitoring tooling or contact OutSystems Support if you need assistance understanding the current allocation.

</div>

![Screenshot of the OutSystems LifeTime platform showing an overview of database storage for Development, Testing, and Production environments.](images/database-storage-cloud_LT.png "OutSystems LifeTime Environments Overview")

By clicking on **View details** you can see the breakdown between System and Application data.

**System data** represents the space occupied by OutSystems system tables. This includes:

* Module and solution versions
* Processes
* Emails
* Logs

**Application data** refers to all the information stored in the database Entities of your applications. This includes deleted Entities and Attributes of the data model.

![Detailed view in OutSystems LifeTime platform displaying the database usage breakdown into System Data and Application Data.](images/database-storage-cloud-detail_LT.png "OutSystems LifeTime Database Usage Details")

## Should I still clean up space?

It's a best practice that you can execute as you see fit. Regardless, your OutSystems Cloud database space will autogrow if necessary.

For more details on cleaning up space, refer to [Best Practices for a Tidy and Clean Environment](https://success.outsystems.com/Documentation/Best_Practices/Lifecycle/Best_practices_for_a_tidy_and_clean_environment).

## Will my environment ever stop due to lack of database space?

Our health monitoring mechanisms will enable OutSystems to act promptly, safeguarding the robustness of your platform. However, if the consumed storage increases both suddenly and by a large amount, we may not have enough time to react before it starts affecting your platform.

## Can I know how the database space is distributed?

You can do this by querying the database model directly, utilizing the [direct database access](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Access_the_database_of_your_PaaS) provided by OutSystems.
