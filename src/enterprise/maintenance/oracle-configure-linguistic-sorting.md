---
summary: OutSystems 11 (O11) supports configurable linguistic sorting for Oracle databases in on-premises installations.
locale: en-us
guid: 97a691c3-79e8-4016-9437-045cb9725cc0
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise%20Customers?node-id=619:15
tags: database configuration, oracle database, linguistic sorting, character data configuration, database administration
audience:
  - platform administrators
  - full stack developers
  - backend developers
  - tech leads
outsystems-tools:
  - platform server
  - service center
coverage-type:
  - understand
  - apply
---

# Configuring linguistic sorting in an OutSystems environment using an Oracle database

<div class="info">

Only available in OutSystems on-premises installations.

</div>

This document explains how you can configure linguistic sorting for character data in an OutSystems environment using an Oracle database. 

Different countries have different ways of sorting characters, and Oracle provides mechanisms for the Database Administrator to configure and control the database string sorting behavior. Check [Oracle's documentation](https://docs.oracle.com/cd/B28359_01/server.111/b28298/ch5lingsort.htm#i1009059) for more information on Oracle linguistic sorting settings.

In OutSystems, in Platform Server versions before 11.7.0, all Oracle databases must have the following configuration:

* NLS_LANGUAGE: **AMERICAN**
* NLS_TERRITORY: **AMERICA**
* NLS_CHARACTERSET: **AL32UTF8** (Unicode support) or **WE8MSWIN1252** (no Unicode support)
* NLS_DATE_FORMAT: **DD-MON-RR**

However, with this configuration, there might be a few unexpected query results. One of the issues has to do with accented characters in languages like Japanese. 

For example, if you have the word "セト" (romanization: Seto) stored in the database and search for the word "ゼト" (romanization: Zeto), the query results will include the record containing "セト" (romanization: Seto) when using the configuration stated above. This record is included in the query results because the default string sorting algorithm for Oracle used by the platform is `BINARY_AI`, which is accent insensitive.

Starting with Platform Server 11.7.0, OutSystems system administrators can change the linguistic sorting configuration (the value of the `NLS_SORT` parameter) of the Oracle database from `BINARY_AI` (the default value) to `BINARY_CI` on the OutSystems platform database. Changing this configuration requires you to republish applications for the setting to become active. 

Check the next section for instructions on changing the linguistic sorting for the platform database.

## Configure linguistic sorting 

To change the linguistic sorting **for the platform database**, do the following:

1. Start the Configuration Tool, available at Start > Programs > OutSystems > Administration Tools.

1. In the **Platform** tab, click the "Advanced Settings" link in the "Database" section.

    ![Screenshot highlighting the 'Advanced Settings' link in the OutSystems Configuration Tool for Oracle database settings.](images/oracle-ct-advanced-settings-link.png "Advanced Settings Link in Configuration Tool")

1. Select the desired linguistic sorting. The available options are:

    **BINARY_AI** – Collation-sensitive SQL operations use a binary sort that is accent-insensitive and case-insensitive.  
    **BINARY_CI** – Collation-sensitive SQL operations use a binary sort that is case-insensitive, but accent-sensitive.

    ![Dialog box showing the Advanced Platform Database Connection Settings with options for linguistic sorting in the OutSystems Configuration Tool.](images/oracle-ct-advanced-settings.png "Advanced Platform Database Connection Settings")

1. Press **OK** to close the "Advanced Settings" dialog box, and then press **Apply and Exit**.

1. Republish all modules in your environment.
