---
tags: 
summary: Check here how to improve the performance of queries that become slower after deleting/updating a significant amount of rows. 
locale: en-us
guid: 9F9D7472-775E-4F53-A6E0-F3C649680216
app_type: traditional web apps, mobile apps, reactive web apps
---

# Queries become slower after deleting or updating rows

## Symptoms

Database queries start to run slower than usual after deleting or updating a significant amount of rows.

## Cause

The database query optimizer uses statistics to create query execution plans that improve query performance.  

Deleting or updating a significant amount of rows can cause data fragmentation and/or outdated statistics that can lead the database engine to create inaccurate access plans, reading unnecessary data and causing slowdowns.

## Troubleshooting

To solve this issue, you need to:  

* Check if the table statistics are outdated.  
* Update the table statistics if needed.  
* Check if the table is fragmented.  
* Defragment the table if needed.  

To perform these tasks, you need to access the database. If your database is in OutSystems Cloud:  

* You need to [ask for a database user](../../enterprise/maintenance/access-database-paas/access-database-paas.md) to be able to execute the steps of checking the last maintenance execution (applicable only for Oracle), checking the table statistics, and checking table fragmentation.  
* You need to [open a support case](../../community/open-support-case.md) asking to execute the steps of updating the table statistics and defragmenting the table.  

You can find below the steps to solve this issue in Oracle and SQL Server. 

<div class="info" markdown="1">
We strongly recommend engaging with your DBA to supervise the execution of the steps.
</div>

### Oracle

By default, Oracle marks statistics as stale when 10% or more rows in the table have changed. Oracle updates statistics in the maintenance window by default. However, if the window is small for all the work that Oracle has to do, some statistics may not be updated.  

Follow these steps:

1. Check if the last maintenance execution was successful and if it occurred after the operation that deleted/updated the records, by executing the following query:  

        select  
            client_name, 
            job_status, 
            job_start_time, 
            job_duration 
        from 
            dba_autotask_job_history 
        where 
            client_name = 'auto optimizer stats collection' 
        order by 
            job_start_time desc
        ;

1. To check if the table statistics are up to date, execute the following queries, changing &lt;owner_name&gt; by the owner of the table and &lt;table_name&gt; by the table in which you deleted/updated the records.

    1. Check the last time Oracle updated the table statistics and how many records it had at that time:  
        
            select 
                to_char(t.last_analyzed,'YYYY/MM/DD HH24:MI:SS') table_last_analyzed, 
                t.num_rows
            from 
                dba_tables t
            where 
                t.owner = '<owner_name>' and 
                t.table_name = '<table_name>'
            ;

    1. Check the current number of rows in the table:  

            select 
                count(1) 
            from 
                <owner_name>.<table_name>
            ;
        
        Compare the number of rows in the table to the number of rows obtained in the previous step.

        Note: A small difference between the number of rows presented by the statistics and the current number of rows in the table is considered normal.  

1. If the statistics are outdated, update them manually.  
Execute the following query, changing &lt;owner_name&gt; by the owner of the table and &lt;table_name&gt; by the table in which you deleted/updated the records.  

        EXEC DBMS_STATS.GATHER_TABLE_STATS( OWNNAME => '<owner_name>', TABNAME => '<table_name>', ESTIMATE_PERCENT => 100);

1. With the statistics updated, check table fragmentation. 

    <div class="info" markdown="1">
    If the statistics are outdated, the table fragmentation may not be accurate.
    </div>
    
    1. Retrieve the database block size:  

            select 
                value 
            from 
                v$parameter 
            where 
                name = 'db_block_size'
            ;
    
    1. Execute the following query, changing &lt;block_size&gt; by the database block size, &lt;owner_name&gt; by the owner of the table and &lt;table_name&gt; by the table in which you deleted/updated the records.  

            select
                owner,
                table_name,
                num_rows,
                blocks,
                avg_row_len,
                round(( blocks * <block_size> ) / 1024, 2) sizeMB,
                round(( num_rows * avg_row_len / 1024 / 1024 ), 2) actualSizeDataMB,
                (round( blocks * <block_size>, 2)/1024 - round(( num_rows * avg_row_len / 1024 / 1024 ), 2)) freeSpaceMB,
                (round(( num_rows * avg_row_len / 1024 / 1024 ), 2) * 100)/ case (round(( blocks * <block_size> ), 2) / 1024) when 0 then 1 else (round(( blocks * <block_size> ), 2) / 1024) end percentage
            from
                dba_tables
            where
                owner = '<table_owner>' and 
                table_name = '<table_name>'
            order by
                freeSpaceMB desc
            ;

1. In case there is table fragmentation, the table needs to be defragmented. There are a few ways to defragment the table and the best way depends on the Oracle license (Enterprise/Standard), table size, data type of the columns and indexes. Contact your DBA, as they should know the best way to defragment the table.


### SQL Server

Up to SQL Server 2014, the number of records in the table is used to determine if the statistics are up to date or not. From the 2016 version onwards, SQL Server calculates whether the table statistic is stale according to the table cardinality. As an example, a statistic for a table with 2 million rows will be considered stale if at least 44.721 rows have been modified. You can find more information on the [official documentation](https://docs.microsoft.com/en-us/sql/relational-databases/statistics/statistics?view=sql-server-ver15). 

SQL Server has no default maintenance plan and no maintenance window. This should be set by a DBA. However, SQL Server can update statistics automatically at any time if the "Auto Update Statistics" parameter is set to "True", which is the default value. 

Follow these steps:

1. To check if the table statistics are up to date, execute the following queries, changing &lt;schema_name&gt; by the schema of the table and &lt;table_name&gt; by the table in which you deleted/updated the records.

    1. Check the last time SQL Server updated the table statistics and how many records it had at that time:  

            select
                name, 
                last_updated, 
                rows
            from
                sys.stats AS stat
                Cross apply sys.dm_db_stats_properties(stat.object_id, stat.stats_id) AS sp
            where
                stat.object_id = OBJECT_ID('<schema_name>.<table_name>')
            ;

    1.  Check the current number of rows in the table:  

            select 
                count(1) 
            from 
                <schema_name>.<table_name>
            ;

        Compare the number of rows in the table to the number of rows obtained in the previous step.
        
        Note: A small difference between the number of rows presented by the statistic and the current number of rows in the table is considered normal.

1. If the statistics are outdated, update them manually.  
Execute the following query, changing &lt;schema_name&gt; by the schema of the table and &lt;table_name&gt; by the table in which you deleted/updated the records.  

        update statistics <schema_name>.<table_name> with fullscan;

1. With the statistics updated, check table fragmentation. 

    <div class="info" markdown="1">
    If the statistics are outdated, the table fragmentation may not be accurate.
    </div>

    Execute the following query, changing &lt;schema_name&gt; by the schema of the table and &lt;table_name&gt; by the table in which you deleted/updated the records.

        select
            object_name(ips.object_id) as object_name,
            si.name as index_name,
            round(ips.avg_fragmentation_in_percent, 2) as fragmentation,
            ips.page_count as pages,
            round(ips.avg_page_space_used_in_percent, 2) as page_density
        from
            sys.dm_db_index_physical_stats (
            DB_ID(),
            NULL,
            NULL,
            NULL,
            'DETAILED') ips
            cross apply sys.indexes si
        where
            si.object_id = ips.object_id and
            si.index_id = ips.index_id and
            ips.index_level = 0 and
            ips.alloc_unit_type_desc = 'IN_ROW_DATA' and
            ips.object_id = object_id('<schema_name>.<table_name>')
        order by
            fragmentation desc,
            page_density desc
        ; 

1. There are some parameters that can be used to defragment the table/index and the best combination depends on the SQL Server license (Enterprise/Standard) and the size of the table. Contact your DBA, as they should know the best way to defragment the objects.
