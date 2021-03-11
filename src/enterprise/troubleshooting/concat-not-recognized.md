---
summary: 
---

# CONCAT is not a recognized built-in function name

## Problem

After upgrading to OutSystems 10, when creating/upgrading the database in the Configuration Tool, sometimes the following error shows up:

`"Database Error: Database error - 'CONCAT' is not a recognized built-in function name"`

This happens when using SQL Server 2008 or SQL Server 2008 R2 as database management system, because one of the Configuration Tool database creation scripts (runtimemodel_sqlserver.sql) has a `CONCAT` function, but the `CONCAT` function only exists since SQL Server 2012.

## Resolution

This problem has been fixed in 10.0.405.0 - If you're experiencing this issue we recommend you download and install the latest OutSystems 10 revision available.

