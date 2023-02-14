*   ---
summary: OutSystems logs information that helps the troubleshooting of problems. Learn how to get the troubleshooting information from the different OutSystems components and other system components.
tags:
locale: en-us
guid: 2ACE4DFE-7CCC-45A5-83B4-499B7104C1AF
app_type: traditional web apps, mobile apps, reactive web apps


# How to get AWR and ADDM reports

This article explains how to get the AWR and ADDM reports.

In the context of a support case, OutSystems Support might require that you provide some of these files so they can troubleshoot the issues you are experiencing. In this situation, you should get the required files as described in this article and attach them to your support case.
    
## Definition

The AWR and ADDM report are database reports detailing important information about the performance of the database
        
## Purpose
    
ADDM automatically detects and reports on performance problems with the database, such as:
 * Adding CPUs or changing the I/O subsystem configuration
 * Changing initialization parameter settings
 * Hash partitioning a table or index, or using automatic segment-space management (ASSM)
 * Using the cache option for sequences or using bind variables
 * Running the SQL Tuning Advisor on high-load SQL statements or running the Segment Advisor on hot objects
 
 AWR has valuable information such as:CPU Statistics
 * Wait Time Statistics
 * Workload Profile
 * Sessions
            
## Structure
    
### ADDM
        
![](images/get-db-AWR-ADDM-logs 1.png)

### AWR
        
![](images/get-db-AWR-ADDM-logs 2.png)

## How to get reports
    
**AWR report**: [https://docs.oracle.com/database/121/TGDBA/compare\_stats.htm#TGDBA272]
        
**ADDM report In command line**:
        
 * cd $ORACLE\_HOME/rdbms/admin
 * SQL> @addmrpt.sql
 * Input begin snap\_id and end snap\_id
