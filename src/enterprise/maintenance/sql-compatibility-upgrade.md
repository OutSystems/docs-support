---
summary: Explore SQL Server 2019 compatibility upgrade options for OutSystems 11 (O11) to ensure optimal database performance and compliance.
locale: en-us
guid: 394c269a-4655-41ff-8543-957c705d97fd
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: database upgrade, sql server 2019, database compatibility, outsystems platform server, database maintenance
audience:
  - platform administrators
  - infrastructure managers
  - backend developers
  - full stack developers
outsystems-tools:
  - platform server
coverage-type:
  - apply
---

# Upgrading SQL Server to a new compatibility level

Platform Server 11.12.0 supports Microsoft SQL Server 2019  (15.x).  Customers with self-managed installations may choose to upgrade to this database engine, either to remain up-to-date or because of company compliance requirements.

By following the upgrade process described in this article, you can also safeguard correct application behavior for databases created with lower SQL Server compatibility levels.

This article discusses two possible paths for your operations/infrastructure team and your database administrators to upgrade the database to a higher compatibility level:

* Upgrade in place
* Fresh install

## Upgrade in place

Follow the procedure below to perform an upgrade in place.

1. Stop [OutSystems Services](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Manually_starting_services_of_the_OutSystems_Platform_-_how-to_and_caveats#Starting_services) and [IIS](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj635851(v=ws.11)) to prevent database changes during the SQL Server engine upgrade.
1. Create a backup of the platform, log, and session databases. Verify that this backup can be restored if needed.
1. [Upgrade the SQL Server engine version](https://docs.microsoft.com/en-us/sql/database-engine/install-windows/supported-version-and-edition-upgrades-version-15?view=sql-server-ver15).
1. Change the compatibility level of the platform, log, and session databases.
1. Rebuild all indexes of the platform, log, and session databases.
1. Start [OutSystems Services](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Manually_starting_services_of_the_OutSystems_Platform_-_how-to_and_caveats#Starting_services) and [IIS](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj635851(v=ws.11)).

## Fresh install

Follow the procedure below to perform a fresh install.

<div class="info" markdown="1">

To minimize downtime, especially for large databases, this procedure can be done twice: first with a full backup and restore with no-recovery option, and then with a differential backup and restore with recovery.

</div>

1. [Install a new SQL Server engine](https://docs.microsoft.com/en-us/sql/database-engine/install-windows/install-sql-server?view=sql-server-ver15) that supports the desired compatibility level.
1. Stop [OutSystems Services](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Manually_starting_services_of_the_OutSystems_Platform_-_how-to_and_caveats#Starting_services) and [IIS](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj635851(v=ws.11)) to prevent database changes during SQL Server engine installation.
1. Ensure that all platform, logs, and session databases are read-only.
1. Create a full backup of the platform, log, and session databases. Verify that this backup can be restored if needed.
1. Ensure that all platform, logs, and session databases are offline.
1. Restore platform, log, and session databases in the new SQL Server engine.
1. Ensure that all platform, logs, and session databases are read-write in the new server.
1. [Transfer SQL user logins](https://docs.microsoft.com/en-us/troubleshoot/sql/security/transfer-logins-passwords-between-instances) from the old database server to the new database server.
1. Change the compatibility level of each of the platform and log databases.
1. Rebuild all indexes.
1. Run the OutSystems [Configuration Tool](https://success.outsystems.com/Documentation/11/Reference/Configuration_Tool) to point the platform, logs, and session database at the new database engine.
1. Start [IIS](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj635851(v=ws.11)).
1. Apply settings to the whole factory.
1. If needed, manually reconfigure external connections that may point at the old database.

## Additional considerations

Because of changes introduced in the [cardinality estimator](https://docs.microsoft.com/en-us/sql/relational-databases/performance/cardinality-estimation-sql-server?view=sql-server-ver15) in SQL Server 2014, upgrading the compatibility level of previous database versions may have a negative impact on the speed of some queries in the platform/apps database.

In this case, you can rewrite affected application code to improve query performance. Where this is not feasible, you may need to turn on the [Legacy Cardinality Estimator](https://docs.microsoft.com/en-us/sql/relational-databases/performance/cardinality-estimation-sql-server?view=sql-server-ver15).
