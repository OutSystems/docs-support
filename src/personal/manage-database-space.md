---
summary: Personal environments can store up to 2GB on the database. This includes system and application data. Learn what you can do to take the most of it.
---

# Manage the database space of your personal environment

**Personal environments have a database limited to 2GB**. The database stores : 

* System data: the meta data used by OutSystems Platform. This includes the applications definition, data model, module configurations, logs, application versions, and other information. The system data usually grows as you develop and deploy your applications;

* Application data: the data your applications generate and manipulate. The application data usually grows as your users access your applications.

## Check how much database space you have

Access your personal environment on `https://<yourpersonal>.outsystemscloud.com`, and navigate to the **Environments** tab.

![](images/manage-database-space_0.png)

In this example, we are only using 13% of the available database storage space.

You can also check how much is being used for system data, and application data. Click the **View details** link.

![](images/manage-database-space_1.png)

Note that these metrics are updated every hour, so they might not represent the real space you are using at the moment.

To clear database space of your Personal Environment, check [Best practices for a tidy and clean environment](https://success.outsystems.com/Documentation/Best_Practices/Lifecycle/Best_practices_for_a_tidy_and_clean_environment).
