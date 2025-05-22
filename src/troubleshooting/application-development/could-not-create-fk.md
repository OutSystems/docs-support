---
summary: Explore common causes and solutions for "Could not create Foreign Key" errors during deployment in OutSystems 11 (O11).
locale: en-us
guid: fa591ec3-eb33-4ac1-8e49-e2a797934f6f
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3330:2686
tags: database management, error handling, entity relationships, data integrity, deployment issues
audience:
  - mobile developers
  - frontend developers
  - full stack developers
  - backend developers
  - platform administrators
outsystems-tools:
  - service studio
  - service center
coverage-type:
  - unblock
---

# Troubleshoot Could not create Foreign Key errors during deployment

When publishing a module, you may, in certain situations, encounter the following error:

```
Could not create Foreign Key: This may have happened because there are '<EntityAId>' values of entity '<EntityB>' with no corresponding value in entity '<EntityA>', or attribute '<EntityAId>' of entity '<EntityB>' is creating a circular dependency between entities. Check error log for details.
```

You may see it when publishing a module in Service Studio:

![Screenshot of a 'Could not create Foreign Key' error in OutSystems Service Studio during deployment.](images/could-not-create-fk-ss.png "Service Studio Foreign Key Error")

Or also in Service Center when, for example, publishing a solution:

![Error message in OutSystems Service Center indicating a failure to create a Foreign Key while publishing a solution.](images/could-not-create-fk-sc.png "Service Center Foreign Key Error")


## Most common scenarios

In this guide, we’ll list the most common situations that can lead to this publishing error and how to fix them. The most likely causes are listed first, so we suggest troubleshooting in this order.

### No corresponding values

To create a Foreign Key (FK) from one table to another, it's important that the table where the FK is being created (entity ‘A' of the error) contains only values that exist in the parent table (entity 'B' of the error). To give you a practical example, imagine the two tables:

Entity 'A':

| ID | User_ID | Task |
|----|----|----|
| 1 | 10 | Create |
| 2 | 11 | Review |

Entity 'B':

| ID | Username | Email |
|----|----|----|
| 5 | Ruben | ruben@example.com |
| 6 | Capitao | capitao@example.com |

If we create the Foreign Key from Entity 'A' column 'User_ID' to point to Entity 'B' column 'ID', we'll obtain an error. This because the existing data in column 'User_ID' contains values that don't exist in the parent table (entity 'B').

To validate this hypothesis, check the data on the physical tables that the entities are pointing to. 

To resolve the situation, it's necessary to correct the data in the tables such that all values referenced exist in the parent table, by either:

* removing entries that don't exist 
* adding the values to the parent table


### Circular dependencies or multiple cascade paths

This situation primarily affects SQL Server databases, as Oracle provides more flexibility regarding Delete Rules.

In OutSystems, you can set up your tables so that when an entry is deleted from a table, all foreign keys depending on that entry are deleted: this is called cascade deletion. You can do this by going to the properties of the Foreign Key relationship and selecting "Delete" for the [Delete Rule property](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Entity_Relationships/Delete_Rules).

![OutSystems interface showing the Delete Rule property set to 'Delete' for a Foreign Key relationship.](images/could-not-create-fk-delete-rule.png "Delete Rule Property in OutSystems")

In some scenarios, these delete rules run into scenarios that the database engine can't handle and therefore doesn't allow. In the scenarios below, this error is expected, and the delete rules should be reviewed to avoid running into the error.

![Diagram illustrating circular dependencies and multiple cascade paths in an entity relationship model that can cause Foreign Key errors.](images/could-not-create-fk-entity-diagram.png "Entity Relationship Diagram with Circular Dependencies and Multiple Cascade Paths")

#### Circular dependencies

In the entity diagram above, on the left, the Delete Rules loop back to the table being deleted, which would cause the database engine to follow the delete cascade path indefinitely. Since this would result in undesirable behaviors, the topology of the entity model should be reviewed such that either: 

* One of the Foreign Key relationships doesn't exist 
* One of the delete rules isn't "Delete"

#### Multiple cascade paths

In the entity diagram above, on the right, deleting a value from table Z will ultimately cause the deletion of values in table X, however, the database engine can't determine which deletion should be made first: Y and consequently X or directly X. 

This error can also happen with just two entities. If table X had both attributes referencing table Z with delete rules set to "Delete", the problem would still occur even if table Y did not exist.

To avoid this situation, at least one of the Foreign Key relationships causing the multiple paths should be set to "Ignore" or "Protect".

### Database timeout

Considering that the SQL engine validates the data present in the tables, if the tables exist, the larger their size, the more time it requires to create the FK. Validate if the tables have many records and, in that case, update the timeout value in the configuration tool. 

![OutSystems Configuration Tool interface highlighting the Default Update Query Timeout field set to 600 seconds.](images/Conf_tool_DB_timeout.png "Configuration Tool Database Timeout Setting")

Otherwise, if increasing the timeout isn't enough and/or the tables are small, check for database locks.

### Database locks

It is also possible that locks in the tables prevent the foreign key from being created by simply causing a timeout as described above. In Oracle, you might even see the following error in the event of a lock:

`ORA-00054: resource busy and acquire with NOWAIT specified or timeout expired`

To check if this is the case, you should work with your Database Administrator to determine whether there are locks affecting the publish operation and how to resolve them.
