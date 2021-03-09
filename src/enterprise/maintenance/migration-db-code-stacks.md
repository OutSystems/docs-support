---
summary:
---

# Migration between database stacks (SQL Server; Oracle; MySQL) and code stacks (.NET; Java)

## Overview

OutSystems Platform runs on multiple code stacks and database stacks. This is a choice that customers take when they initially start using the platform.

At some point in time, the need or will may come to move an application, created in one of the stack combinations, into a different one. Although the architecture of the OutSystems Platform is essentially the same in all stacks, these lower-level differences means that one must take some actions to ensure the move is done properly.

The two things below are the topmost concerns when performing such an operation:

* Using an app developed for a SQL Server database in a Oracle database

* Moving data from a SQL Server database to an Oracle database.

This article gives an overview on how to deal with these topics, with pointers to other references for more information.

## Using an app developed for a SQL Server database in a Oracle database

To move an application from an environment to the other, it suffices to download the app from the source and publish it in the new environment. 

When you move an app between different stacks (be it the code - Java or .NET - or the database - SQL Server, Oracle or MySQL), most of the application behavior will remain the same.

The things to worry about are (top of mind):

* Advanced queries / SQL nodes: the SQL syntax between the 3 database engines differs, so your queries may need to be altered. A classic example is the difference between SELECT TOP N .... [SQL Server] and SELECT * FROM (SELECT ....) WHERE ROWNUM < N [Oracle];

* [Transactional behavior](https://success.outsystems.com/Documentation/10/Reference/OutSystems_Language/Data/Database_Reference/Handling_Transactions) may not be the same: some engines use READ UNCOMMITTED, others use READ COMMITTED. This is probably where you want to pay more attention in such migration;

* Query performance: in a typical scenario, most queries will not experience significant performance improvement or degradation, since the underlying principles of a data model are the same (tables with columns, indexes, statistics, etc).
However, given that each database engine has its own independent implementation, behaviors are not guaranteed to be the same. This means you may observe degradation in individual queries which may require localized tuning to restore adequate performance;
 
* Integration using Extensions: if moving between Java and .NET or vice-versa, extension code will need to be re-written / added. Extensions provided by OutSystems have code in both stacks, but it was explicitly written by us - if you coded your own (or used Extensions from the Forge), this is something you will need to worry about. 

## Moving data from a SQL Server database to an Oracle database

This is the part that is not trivial. The models OutSystems creates in SQL Server, Oracle and MySQL are very similar, but not equal. A blind migration between one and another will not work correctly. Simple examples are [the](http://www.outsystems.com/help/servicestudio/9.1/#t=Using_Data%2FDefault_Values_on_database.htm)[ way an empty string is stored in the database](https://success.outsystems.com/Documentation/10/Reference/OutSystems_Language/Data/Database_Reference/Default_Values_on_Database) and the maximum length of object names in Oracle.

As such, OutSystems does not document the process and advises customers against performing the said operation on their own - the operation is not supported, we will not be able to assist and customer may run into issues in which OutSystems may not be able to help. 

If data move is needed, using the platform, it is possible to implement logic to move the data (e.g. via web services) from one to the other; but it should include doing all the data writing using platform primitives. Any other approach is not feasible.

