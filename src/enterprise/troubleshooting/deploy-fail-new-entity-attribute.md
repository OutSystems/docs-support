---
summary: Identify and solve a timeout issue when deploying an application after adding a new Entity Attribute.
tags:
---

# Application deployment takes too long after adding a new Entity Attribute

## Symptoms

After adding a new [Entity Attribute](https://success.outsystems.com/Documentation/11/Reference/OutSystems_Language/Data/Modeling_Data/Entity_Attribute) to an existing [Entity](https://success.outsystems.com/Documentation/11/Reference/OutSystems_Language/Data/Modeling_Data/Entity), the new application version takes a long time to deploy or the deployment times out during the update database phase.

This scenario occurs when the Entity with the new Attribute already has millions of records.

The following use cases can also lead to this scenario:

* Converting an Entity to multi-tenant (which results in adding a new Attribute to the Entity)
* Adding a unique constraint over an existing Entity Attribute

## Cause

In environments with Platform Server 11.11.0 or earlier, the step to update the database model during the deployment runs a DML (Data Manipulation Language) statement to set the default value of the new database column. As this statement performs over the full table, it causes a timeout at the database side for tables having millions of records.

## Solution

For SQL Server Enterprise and Oracle databases, upgrade the environment to [Platform Server 11.11.1](https://success.outsystems.com/Support/Release_Notes/11/Platform_Server#Platform_Server_11.11.1), as this version provides the fix for this issue.

As workaround, increase the query timeout by running the Configuration Tool and changing the **Default Query Timeout** under the Platform Tab (applies only to self managed environments).
