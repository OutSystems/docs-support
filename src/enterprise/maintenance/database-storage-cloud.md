---
summary: OutSystems Cloud databases autogrow as needed, ensuring your platform runs smoothly.
---

# Database storage on OutSystems Cloud

OutSystems Cloud can run with either SQL Server or Oracle RDS databases. Upon purchase an initial database storage is provisioned. Storage autogrows as needed at no additional charge.

## What does the value I see in LifeTime mean?

In the **Environments** screen in LifeTime you can click on an environment card to see the occupied space of each database as well as the total available space.

![Environment database space](images/database-storage-cloud_LT.png)

By clicking on **View details** you can see the breakdown between System and Application data.

**System data** represents the space occupied by OutSystems system tables. This includes:

* Module and solution versions
* Processes
* Emails
* Logs 

**Application data** is all the information that's stored in the database Entities of your applications. This includes deleted Entities and Attributes of the data model.

![Environment database space](images/database-storage-cloud-detail_LT.png)

## Should I still cleanup space?

It's a best practice that you can execute as you see fit. Regardless, your OutSystems Cloud database space will autogrow if necessary.

You can see more details about cleaning up space at [Best practices for a tidy and clean environment](https://success.outsystems.com/Documentation/Best_Practices/Lifecycle/Best_practices_for_a_tidy_and_clean_environment).

## Will my environment ever stop due to lack of database space?

Our health monitoring mechanisms will allow OutSystems to act in time, defending your platform's robustness. However, if the consumed storage increases both suddenly and by a large amount, we may not have enough time to react before it starts affecting your platform.

## Can I know how the database space is distributed?

You can do it by querying the database model directly, resorting to the [direct database access](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Access_the_database_of_your_PaaS) provided by OutSystems.
