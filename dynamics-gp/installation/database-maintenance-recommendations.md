---
title: Recommended Maintenance of Your Databases
description: 
ms.date: 10-23-2020
ms.topic: article
ms.service: dynamics-gp
author: edupont04
ms.author: edupont
---

# Recommended Maintenance of Your Databases

Database maintenance helps keep the inner workings of Microsoft SQL Server and the Microsoft Dynamics GP databases running at their peak level. ​​We recommend that you use the following SQL Server maintenance procedures:

- Use database consistency check commands

- Update statistics

- Recompile stored procedures

We recommend that you perform these maintenance procedures weekly for the DYNAMICS database and all company databases. However, you can vary this frequency based on your environment and the activity each database receives. We also recommend that you stagger these maintenance procedures throughout the week to handle lots of data.

> [!NOTE]
> Before you follow the instructions in this article, make sure that you have a complete backup copy of the database that you can restore if a problem occurs.

## Database consistency check commands

You can run database consistency check (DBCC) commands manually with SQL Server through SQL Query Analyzer or SQL Server Management Studio. To do this, follow these steps:

1. Open **SQL Server Management Studio**.

2. In SQL Query Analyzer or SQL Server Management Studio, run one or more of the following DBCC commands:

    - DBCC CHECKCATALOG (DBNAME)

      When you use this statement, replace *DBNAME* with the name of your database, such as DYNAMICS.
      > [!NOTE]
      > DBCC CHECKCATALOG is included in DBCC CHECKDB for Microsoft SQL Server 2005 or later.

    - DBCC CHECKDB (DBNAME)
        > When you use this statement, replace *DBNAME* with the name of your database, such as DYNAMICS.
        > You can schedule this command within SQL Server Enterprise Manager or SQL Server Management Studio so that the maintenance process runs automatically.

    -   DBCC DBREINDEX (TableName)
      When you use this statement, replace *TableName* with the name of the table, such as GL00100.

      The DBCC DBREINDEX command can also be executed manually against all tables at the same time by using the Reindex.sql script. You can find the Reindex.sql script in the default path for Microsoft Dynamics GP as C:\\Program Files\\Microsoft Dynamics\\GP\\SQL\\Utility\\0 folder.

      You can also schedule this command within SQL Server Enterprise Manager or SQL Server Management Studio so that the maintenance process runs automatically.

## Update Statistics

There are several ways for you to run the update statistics procedure.

- You can update statistics by running the UpdatSta.sql script with Microsoft SQL Server by using SQL Query Analyzer or SQL Server Management Studio. You can find the UpdatSta.sql script in the default path for Microsoft Dynamics GP as C:\\Program Files\\Microsoft Dynamics\\GP\\SQL\\Utility\\0 folder.

- You can run the update statistics process within Microsoft Dynamics GP. To do this, follow these steps:

    1. On the **File** menu, point to **Maintenance**, and then choose **SQL**.

    2. Select a database from the **Database** box and product for **Product** box.

    3. Select all the tables for that database by pressing **CTRL+A** within the table listing.

    4. Choose **Update Statistics**, and then choose **Process**.

- You can configure SQL Server to run the update statistics process automatically within SQL Server Enterprise Manager or SQL Server Management Studio. To do this, right-choose your database, choose **Properties**, choose **Options**, and then choose to select **Auto Create Statistics** and **Auto Update Statistics**.

- You can schedule the update statistics process on a recurring basis within Database Maintenance Plans.

## Recompile Stored Procedures

There are several ways for you to recompile stored procedures.

- You can recompile stored procedures by running the Recomp.sql script with Microsoft SQL Server by using SQL Query Analyzer or SQL Server Management Studio. You can find the Recomp.sql script in the default path for Microsoft Dynamics GP as C:\\Program Files\\Microsoft Dynamics\\GP\\SQL\\Utility\\0 folder.

- You can also recompile stored procedures within Microsoft Dynamics GP. To do this, follow these steps:

    1. On the **File** menu, point to **Maintenance**, and then choose **SQL**.

    2. Select a database from the **Database** box and product for **Product** box.

    3. Select all the tables for that database by pressing **CTRL+A** within the table listing.

    4. Choose **Recompile**, and then choose **Process**.

- You can recompile stored procedures by scheduling the sp\_recompile procedure by using SQL Server Agent Jobs. For more information about steps to create a job within SQL Server Enterprise Manager or SQL Server Management Studio, see the [SQL Server documentation](/sql/).

If you receive any consistency or allocation errors when you are running these SQL maintenance procedures, you must contact Microsoft SQL Server support. This is not included in the support plan for Microsoft Dynamics GP and it would be an additional cost. Microsoft SQL Server support can be contacted at 1-800-936-5800.

## Database Maintenance Procedure Definitions

The following is a list of definitions of database maintenance procedures. For more information, see the [SQL Server documentation](/sql/).

- **DBCC CHECKCATALOG**: Examines the consistency in system tables and between system tables. This command checks data pages and tables in the specified database for errors.

    > [!NOTE]
    > DBCC CHECKCATALOG is included in DBCC CHECKDB for Microsoft SQL Server 2005 or later.

- **DBCC CHECKDB**: Examines the allocation and structural integrity of all the objects in the specified database.

- **DBCC DBREINDEX**: Rebuilds all indexes. This command will help reduce page splitting and will improve data modification performance.

- **Update statistics**: Updates the query optimizer with distribution information about key values of indexes. This enables the query optimizer to make efficient decisions.

- **Recompile stored procedures**: Recompiles the queries and optimizes the triggers used by stored procedures. This recompile procedure updates database statistics and optimization information that can become outdated with changes to the database.

## See also

[Uninstall or Reinstall the Sample Company](uninstall-or-reinstall-sample-company.md)  
[System Administration Guide](systemadminguide.md)  
