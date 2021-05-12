
---
summary: How to solve the problem of timeouts when deploying an application that contains new entity attributes.
---

# Slow publishes and timeout issues when adding a new column to existing tables that have a large number of records

## Symptoms

When publishing new versions of an application, the deploy stage (namely, the update DB phase) for some modules, takes a long time or times out. The latter aborts the upgrade and may leave the metamodel in an inconsistent state.

## Cause

These issues typically occur when adding a new column to an existing table that has a large number of records (for example, several millions of records).

Until Platform Server 11.11.1, the platform performed the creation of the new column in two separate steps:

    DDL statement to add the new column
    DML statement to set the default value of the column

The second step should be the one causing the big execution times in these cases since it will perform the query over the full table, potentially performing constraint validation steps along the way.

Timeouts have been seen to occur mainly in 3 scenarios that involve publishes and tables with a large number of records:

    Adding a new column to an existing table
    Converting an entity to multitenant (which technically is adding a new column)
    Adding a unique constraint over an existing column

## Solution

Upgrade to Platform Server 11.11.1, where the addition of default values is much faster in SQL Server Enterprise and in any edition of Oracle.

This is because there is no longer a DML statement to add default values. 
The DDL statement that adds the new columns also adds the default values in a very efficient way. However, while the addition is very quick for any edition of Oracle starting in Oracle 11g, the optimization is only enabled in SQL Server Enterprise and not in SQL Server Standard. This means that if the database is SQL Server Standard, the operation will still take some considerable time.
