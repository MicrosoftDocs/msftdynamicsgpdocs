---
title: "System requirements"
description: "See some of the prerequisites and system requirement changes for when you are installing or upgrading Dynamics GP."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 03/1/2023
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 3509e92e-d825-4947-8ea2-7e57b7c2a9e0
ms.reviewer: 
---
# Prerequisites and System Requirements for Upgrade/Installation

This chapter contains a list of prerequisites and system requirement changes for Dynamics GP, as well as disk space requirements for SQL Server computers.

> [!NOTE]
> Recommended system requirements depend on the number of users and transactions. If there will be many users performing concurrent tasks, such as depreciation, posting, or heavy reporting, enhancing your hardware and system software will improve performance.  

## Releases supported by the upgrade

You can upgrade to Dynamics GP from selected previous releases. To review whether or not you can upgrade your release, see [Upgrade Hot Topic](/dynamics/s-e/gp/hot_topic_mdgpupgrade_415).

If you are upgrading to Dynamics GP, you must install the latest update or hotfix for Dynamics GP before starting Dynamics GP Utilities. See the [Microsoft Dynamics GP Resource Directory](../resources.md) article for the latest update information.

## System requirement changes

[System Requirements for Microsoft Dynamics GP](/dynamics/s-e/gp/mdgp2018_system_requirements).

## Home page prerequisites

To display metrics and reports in the Business Analyzer area on your home page, install and set up Microsoft SQL Server Reporting Services to use with Dynamics GP. The reports and metrics you want to display must be created in SQL Server Reporting Services. For more information about installing and setting up Reporting Services for use with Dynamics GP, go to the [Dynamics GP documentation resource Web site](/dynamics/s-e/) for the most current documentation.

## Word templates prerequisites

The following components must be installed before you can use Word Templates for Dynamics GP.

- Microsoft Word 2013 or later to make layout changes such changing the font size

- Open XML SDK 2.0 for Microsoft Office (installed as a Dynamics GP prerequisite)

If a component isn't installed, you can download the component from [microsoft.com](https://www.microsoft.com).

Additional components are required to modify templates.

- Dynamics GP Add-in for Microsoft Word

- Visual Studio Tools for Office Runtime 2.0 or later (Visual Studio Tools for Office Runtime 3.0 is installed with Dynamics GP Add-in for Microsoft Word.)

You can install Dynamics GP Add-in for Microsoft Word from the Dynamics GP installation media. Double-click the Setup.exe file and then click Dynamics GP Add-in for Microsoft Word.

## Email requirements

By using the email functionality in Dynamics GP, you can embed documents into the body of the email or send documents as attachments. You can send a single document, batches of documents, or send multiple documents from sales and purchasing transaction lists. When setting up the email functionality, you can select which documents you can send and which customers and vendors should receive their documents in email. If you are using Word templates for Dynamics GP, you can send predefined or customized forms.

Review the following requirements:

- The email functionality in Dynamics GP supports the following document types. Depending on the document type and the email service, Microsoft Word 2010 or later and Word templates for Dynamics GP are required.

    | File format | Word 2013 | Word templates | Web Client |
    |--|--|--|--|
    | XPS | Required for MAPI | Enabled | Not available |
    | PDF | Required for MAPI | Enabled | Not available |
    | DOCX | Not required | Enabled | Available\* |
    | HTML | Not required | Not required | Available\* |

    \*Email for Dynamics GP Web Client will only be available if Exchange is your server type in the System Preferences window.  

- Before you can send documents as DOCX, PDF, or XPS attachments, the Word template for the document must be enabled in the Template Configuration Manager window.

- Depending on the file format you choose to send your documents in e-mail, your customers and vendors must be using the following components to view their documents.

    | File format | Component |
    |--|--|
    | XPS | Microsoft XPS Viewer |
    | PDF | Adobe Reader |
    | DOCS | Microsoft Word Viewer |
    | HTML\* | Internet Explorer 11 and Edge |

    \*If you are using Dynamics GP Web Client only for your customers and vendors must be using HTML to view their documents.  

For all email documentation on workflow, Modern Authentication and Exchange reiew the [Email Troubleshooting Guide](https://learn.microsoft.com/en-us/dynamics-gp/installation/email-troubleshooting-guide).

## SQL Server Reporting Services requirements

Before you deploy Dynamics GP Reporting Services reports, you must install and configure SQL Server Reporting Services, and then set up security for SQL Server Reporting Services reports. Review the following table for the version of SQL Server Reporting Services and the report type available for that version.

| SQL Server Reporting Services version | Report type available |
|--|--|
| Reporting Services 2012 Standard or Enterprise Reporting Services 2014 Standard or Enterprise Reporting Services 2016 Standard or Enterprise | SQL Server Reporting Services reports |
|  |
| Charts and key performance indicators (KPIs) Map charts |

## Modify the Report Server web.config file

To deploy the SQL Server Reporting Services reports, you must modify the Report Server web.config file for the timeout execution and the maximum request length. If you don't update the Report Server web.config file for the timeout execution, you might receive an error that states that the operation has timed out. If you don't update the Report Server web.config file for the maximum request length, you will receive an error that the deployment has exceeded the maximum request length allowed by the target server.

> [!NOTE]
> You must be an administrator to modify the Report Server web config file.  

To modify the Report Server Web config file:

1. Create a backup copy of the web.config file located in the ReportServer folder. (The ReportServer folder is located in C:\\Program Files\\Microsoft SQL Server\\MSSQLSERVER\\Reporting Services\\ReportServer where Reporting Services is installed.)

2. Open the Report Server web.config file using a text editor, such as Notebad.

3. Search for &lt;httpRuntime executionTimeout="9000" /&gt;.

4. In that line, change executionTimeout="9000" to executionTimeout="19000" and add the value maxRequestLength="20960".

    ```
    &lt;httpRuntime executionTimeout="19000" maxRequestLength="20960"/&gt;
    ```
5. Save and close the Report Server web.config file.


## About remote access

You can use Windows Server 2012 Remote Desktop Services, Windows Server 2012 R2 Remote Desktop Services, and Windows Server 2016 Remote Desktop Services. Citrix Xenapps can also be used with most database configurations to provide remote access to Dynamics GP in a Wide Area Network (WAN) environment.

A Windows Server 2008 Terminal Server is supported only as a client. You also can use Remote Desktop Services.

You also should refer to the documentation provided by Citrix for more information.

## Determine disk space for the upgrade process

For the upgrade process, be sure that you have enough disk space before you begin. To determine the disk space required for the upgrade, you need to find the size of the largest table for all Dynamics GP databases. To determine disk space, use Microsoft SQL Server Management Studio for Microsoft SQL Server.

> [!NOTE]
> You can download an upgrade preparation script that will help you determine the disk space requirements from [dynamics-product-downloads](/dynamics/s-e/).

To determine disk space for the upgrade process using Microsoft SQL Server Management Studio:

1. Download and open the Table\_Size.txt script.

2. Copy all of the contents of the script.

3. In Microsoft SQL Server Management Studio, select a Dynamics GP database, click New Query and paste the contents. Then, execute the query.

4. Run the script for each Dynamics GP database.

5. The largest table will be the first record in the result set. You will need to convert the table size from kilobytes to megabytes by using the following calculation. This will determine the amount of space that will be allocated to the data file (MDF) and the transaction log file (LDF) for each database.

    (table size in KB/1024) = table size in MB

    The table size in megabytes of the largest table from all the databases is the amount of disk space you will need to allocate to the data file of the TEMPDB.

    In the following example, the largest table is the SOP30300 in the company database. The TEMPDB will need 176 MB allocated for the data file.

    | Database | Total size KB | Rows   | Name     | MB  |
    |----------|---------------|--------|----------|-----|
    | DYNAMICS | 33913.171873  | 180872 | 98075    | 33  |
    | TEST     | 180608.280270 | 98075  | SOP30300 | 176 |

6. Calculate the total amount of hard disk space that is needed by adding the space needed for the data file and transaction log file of all databases.

    For the company databases and the DYNAMICS database, both the data file and transaction log file will be increased to the size of the largest table. For the TEMPDB, only the data file will be increased to the size of the largest table out of all databases.

    In following example, TEST, DYNAMICS and TEMPDB are the databases and both the data file (MDF) and transaction log (LDF) file are located on the same hard disk.

    | File                         | MF  |
    |------------------------------|-----|
    | TEST data file               | 176 |
    | TEST log file                | 176 |
    | DYNAMICS data file           | 33  |
    | DYNAMICS log file            | 33  |
    | TEMDB data file              | 176 |
    | Total hard disk space needed | 594 |

    If the data files (MDF) are located on a different hard disk than the transaction log (LDF) files, the total space needed would be calculated for each hard disk. For example, assume that the data files are on the E drive and the transaction log files are on the D drive. The following hard disk space would be needed for each drive.

    | File                         | Drive E: MB | File              | Drive D: MB |
    |------------------------------|-------------|-------------------|-------------|
    | TEST data file               | 176         | TEST log file     | 176         |
    | DYNAMICS data file           | 33          | DYNAMICS log file | 33          |
    | TEMPDB data file             | 176         |                   |             |
    | Total hard disk space needed | 385         |                   | 209         |

7. Verify that the space is available for each drive by using File Explorer. In Windows Explorer, right-click each drive and select Properties to view free space available. By using the information in the previous table, drive E would need at least 385 MB available and drive D would need at least 209 MB available.

8. Use Microsoft SQL Server Management Studio to manually increase the space allocated for the data file and the transaction log file for the DYNAMICS database and each company database.

    - Right-click each database in Microsoft SQL Server Management Studio and select Properties.

    - In the properties window for each database, choose Files and add the additional space needed for the size of the largest table for that database to the Initial Size column. When adding additional space, you are increasing the space for the data file (MDF) and the transaction log file (LDF) as well.

    - Repeat for the remaining Dynamics GP databases.

    - Right-click the TEMPDB database and select Properties. Choose Files and add the additional space needed for the size of the largest table of all Dynamics GP databases to the Space Allocated (MB) column. When adding additional space, you are increasing the space for the data file (MDF) and the transaction log file (LDF) as well.

> [!NOTE]
> If the database size is not manual configured, the time needed to upgrade the databases will increase because the database data, transaction log and TEMPDB files will all have to increase.  

## See also

[Upgrade checklist](upgrade-checklist.md)  
