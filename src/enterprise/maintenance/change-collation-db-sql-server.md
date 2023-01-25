---
summary:
locale: en-us
guid: e7538434-44da-476c-b203-0df42ed1ce0e
app_type: traditional web apps, mobile apps, reactive web apps
---

# Change the collation of an OutSystems database running on SQL Server

## Introduction

When a customer installs the OutSystems Platform on-premises using SQL Server as a database backend, a choice is made regarding the database collation to be used. 

Collations come at several levels: at database instance level, at the database level, and at the individual column level. OutSystems Platform is only certified to be installed or to integrate with SQL Server databases if they are installed as case-insensitive. This means:

* The database [instance collation](https://msdn.microsoft.com/en-us/library/ms179254.aspx) must be case-insensitive (e.g. Latin1_General_**CI**_AS)

* The [database collation](https://msdn.microsoft.com/en-us/library/ms175835.aspx) must also be case-insensitive (e.g. Latin1_General_**CI**_AI).

* The [column collation](https://msdn.microsoft.com/en-us/library/ms190920.aspx) is inherited from the database collation.

The collations for the instance and the database can be different, as in the example above; but both must be Case Insensitive (CI).

Collations should be consistent between all environments in an OutSystems infrastructure: Development, Quality, Pre-Production, Production, etc. should all be in the same collation. It's rare, but applications may behave differently in regards of international support if collations are not the same in all environments.

## Collation conflicts and needs for changes

In addition to the case and accent sensitiveness, other properties define a collation: languages, versions, etc. [Learn more about collations](https://msdn.microsoft.com/en-us/library/ms143726.aspx) from Microsoft's documentation.

There are many collations in SQL Server, and if collations mismatch SQL Server cannot deal with it properly. Particularly, if you try to do the below, you will get errors:

* Create join conditions in queries using columns with different collations;

* Create foreign keys between columns using different collations.

This may lead to issues when building your applications. For the first example, you are able to overcome that by using a special SQL Server clause ([COLLATE](https://msdn.microsoft.com/en-us/library/ms184391.aspx)), but it requires that you use Advanced Queries / SQL Nodes, not Aggregates / Simples Queries. For the second example, there is no workaround.

This means that the choice of a collation should be very well thought considering future integration needs - particularly, if you will need to join data models external to the Platform.

## Changing the collation

If you have just installed the platform and detected that you did it with the wrong collation, the easiest approach is to "start over": recreate the database from zero, setup the platform on top of it, and start developing.

However, if you have been using your environment for a while and find that out at that time, things get a little trickier. 

There is no easy way to fix the collation of an existent database.

### Just changing the database collation does not solve the problem; instead, it creates additional ones!

Although is possible with a simple click to change the collation of the database (catalog), this change does not alter the existing columns: they got the collation at the time they were created and will retain it after you change the database collation.

On top of that, just changing the database collation will expose you to problems:  since pre-existent objects use the previous collation and new objects you create in the future will use the new one, you are exposing yourself to conflicts in later developments in your application.

### Can it be done?

It is possible to perform a collation change in a SQL Server database; however, it is somehow complex, risky, and involves stopping your environment for a given time period.

**Assistance with a database collation change is outside the scope of OutSystems Support**: it is a task at database level that should be done resorting to the appropriate professionals and with the required testing procedures of any significant infrastructure change.

You should not expect assistance from OutSystems Support in the execution of such task.

Usual approaches to this change include scripts that perform the collation changes of the objects like columns, default constraints and indexes.

The below links may be useful on how to consider such an approach:

* [http://www.db-staff.com/index.php/mi...ange-collation](http://www.db-staff.com/index.php/microsoft-sql-server/69-change-collation)

* [https://www.outsystems.com/forums/di...-to-operation/](https://www.outsystems.com/forums/discussion/2766/mssql-error-cannot-resolve-collation-conflict-for-equal-to-operation/)

* [https://msdn.microsoft.com/en-us/lib.../ms143726.aspx](https://msdn.microsoft.com/en-us/library/ms143726.aspx)

Bear in mind that, as with any operation involving databases, the appropriate caution must be taken: performing backups, thorough testing of the procedure, application testing, and rollback plans.

If such change is incorrectly performed, errors may show up in runtime or when performing application deployments. Errors will have messages including something similar to:

```Cannot resolve the collation conflict between "SQL_Latin1_General_CP1_CI_AI*" and "*Latin1_General_CI_AI"```
