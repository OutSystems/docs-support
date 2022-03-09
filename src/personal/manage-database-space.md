---
summary: Personal Environments can store up to 2GB on the database. This includes system and application data. Learn what you can do to take the most of it.
---

# Manage the database space of your personal environment

Personal Environments have a database limit of 2GB. The database stores the following: 

* **System data**: The metadata used by the OutSystems Platform. This includes, for example, the apps definition, data model, module configurations, logs, and app versions. The system data usually increases as you develop and deploy your app.

* **Application data**: The data your apps generate and manipulate. The application data usually increases as your users access your apps.

## Check how much database space you have

Go to your Personal Environment at `https://<yourpersonal>.outsystemscloud.com` and navigate to the **Environments** tab.

![Environments page, showing information about Development, Servers and Database.](images/manage-database-space_0.png)

In this example only 13% of the available database storage space is being used.

To check how much space is being used for system data and application data, click the **View details** link.

![Details about Database Usage, with metrics for System Data and Application Data.](images/manage-database-space_1.png)

<div class="info" markdown="1">

Note that these metrics are updated every hour, so they might not represent the actual space you're using at the moment.

</div>

To clear database space in your Personal Environment, see [Best practices for a tidy and clean environment](https://success.outsystems.com/Documentation/Best_Practices/Lifecycle/Best_practices_for_a_tidy_and_clean_environment).
