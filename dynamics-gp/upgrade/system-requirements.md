---
title: "System requirements"
description: "See the prerequisites and system requirement changes for [!INCLUDE[prodshort](../includes/prodshort.md)]."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 08/24/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 3509e92e-d825-4947-8ea2-7e57b7c2a9e0
ms.reviewer: 
---
# System Requirements

This chapter contains a list of prerequisites and system requirement changes for [!INCLUDE[prodshort](../includes/prodshort.md)], as well as disk space requirements for SQL Server computers.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")Recommended system requirements depend on the number of users and transactions. If there will be many users performing concurrent tasks, such as depreciation, posting, or heavy reporting, enhancing your hardware and system software will improve performance.  

<span id="_Toc498615759" class="anchor"></span>

This chapter contains the following sections:

-   [Releases supported by the upgrade](#releases-supported-by-the-upgrade)  

-   [Home page prerequisites](#home-page-prerequisites)  

-   [Word templates prerequisites](#word-templates-prerequisites)  

-   [Email requirements](#email-requirements)  

-   [SQL Server Reporting Services requirements](#sql-server-reporting-services-requirements)  

-   [Modify the Report Server web.config file](#modify-the-report-server-web.config-file)  

-   [[!INCLUDE[prodshort](../includes/prodshort.md)] CRM requirements](#_Microsoft_Dynamics_GP)  

-   [About remote access](#about-remote-access)  

-   [Determine disk space for the upgrade process](#determine-disk-space-for-the-upgrade-process)  

## Releases supported by the upgrade

You can upgrade to [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 from selected previous releases. To review whether or not you can upgrade your release, see <https://mbs.microsoft.com/customersource/northamerica/GP/support/hot-topics/HOT_TOPIC_MDGP2018Upgrade>

If you are upgrading to [!INCLUDE[prodshort](../includes/prodshort.md)] 2018, you must install the latest update or hotfix for [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 before starting [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities. See CustomerSource (<https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource#GP2018>) for the latest update information.

## System requirement changes

The following changes are new with [!INCLUDE[prodshort](../includes/prodshort.md)] 2018. For a complete list of all system requirements, see <http://go.microsoft.com/fwlink/?LinkId=521785>. You may want to consider upgrading your hardware for improved performance.

### Operating system requirement changes

Review the following table for supported client operating system changes.

| Operating systems supported         | Editions     |
|-------------------------------------|--------------|
| Windows 7                           | Pro|
|                           | Ultimate|
|                           |  Enterprise    |
| Windows 8 and 8.1                          | Pro|
|                           | Ultimate|
|                           |  Enterprise    |
| Windows 10                          | Pro|
|                           |  Enterprise    |
| Windows Server 2008 R2              | Enterprise|
|                           |  Standard    |
| Windows Server 2012, Windows Server 2012 R2, Windows Server 2016         | Datacenter   |
| Operating systems not supported     | Editions     |
| Windows XP                          | All editions |
| Windows Vista                       | All editions |
| Windows Server 2003                 | All editions |

### Database configuration changes

Microsoft SQL Server 2012, 2014, and 2016 Express, Standard, and Enterprise Editions are supported.

Previous versions of SQL Server are no longer supported.

### Internet Explorer change

Internet Explorer 11 and Edge are the only supported. IE browsers.

### Microsoft Office change

Microsoft Office 2013 and Microsoft Office 2016 are supported. All previous versions are no longer supported.

## Home page prerequisites

To display metrics and reports in the Business Analyzer area on your home page, install and set up Microsoft SQL Server Reporting Services to use with [!INCLUDE[prodshort](../includes/prodshort.md)]. The reports and metrics you want to display must be created in SQL Server Reporting Services. For more information about installing and setting up Reporting Services for use with [!INCLUDE[prodshort](../includes/prodshort.md)], go to the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 documentation resource Web site (<https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource#GP2018>) for the most current documentation.

The following versions of SQL Server Reporting Services are supported.

-   SQL Server 2012 Reporting Services

-   SQL Server 2014 Reporting Services

-   SQ” Server 2016 Reporting Services

## Word templates prerequisites

The following components must be installed before you can use Word Templates for [!INCLUDE[prodshort](../includes/prodshort.md)].

-   Microsoft Word 2013 or later to make layout changes such changing the font size

-   Open XML SDK 2.0 for Microsoft Office (installed as a [!INCLUDE[prodshort](../includes/prodshort.md)] prerequisite)

If a component isn't installed, you can download the component from <http://www.microsoft.com>.

Additional components are required to modify templates.

-   [!INCLUDE[prodshort](../includes/prodshort.md)] Add-in for Microsoft Word

-   Visual Studio Tools for Office Runtime 2.0 or later (Visual Studio Tools for Office Runtime 3.0 is installed with [!INCLUDE[prodshort](../includes/prodshort.md)] Add-in for Microsoft Word.)

You can install [!INCLUDE[prodshort](../includes/prodshort.md)] Add-in for Microsoft Word from the [!INCLUDE[prodshort](../includes/prodshort.md)] installation media. Double-click the Setup.exe file and then click [!INCLUDE[prodshort](../includes/prodshort.md)] Add-in for Microsoft Word.

## Email requirements

Review the following requirements.

-   You can send documents by email if you’re using a MAPI-compliant e-mail service or Exchange 2007 Service Pack 1 or greater with Exchange Web Services.

-   If you are using Exchange 2007 Service Pack 1 or greater with Exchange Web Services, the Autodiscover service must be enabled to connect to the Exchange server.

-   The email functionality in [!INCLUDE[prodshort](../includes/prodshort.md)] supports the following document types. Depending on the document type and the email service, Microsoft Word 2010 or later and Word templates for [!INCLUDE[prodshort](../includes/prodshort.md)] are required.

| File format                                                                                                                           | Word 2013         | Word templates | Web Client    |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------|----------------|---------------|
| XPS                                                                                                                                   | Required for MAPI | Enabled        | Not available |
| PDF                                                                                                                                   | Required for MAPI | Enabled        | Not available |
| DOCX                                                                                                                                  | Not required      | Enabled        | Available\*   |
| HTML                                                                                                                                  | Not required      | Not required   | Available\*   |
| \*Email for [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client will only be available if Exchange is your server type in the System Preferences window. |

-   Before you can send documents as DOCX, PDF, or XPS attachments, the Word template for the document must be enabled in the Template Configuration Manager window.

-   The email functionality is supported on the 32-bit edition of Microsoft Office2013.

-   The email functionality is supported on the 64-bit edition of Microsoft Office2013 if you are using Exchange 2007 Service Pack 1 or greater with Exchange Web Services and Exchange is your server type in the System Preferences window.

-   Depending on the file format you choose to send your documents in e-mail, your customers and vendors must be using the following components to view their documents.

| File format                                                                                                                         | Component                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| XPS                                                                                                                                 | Microsoft XPS Viewer          |
| PDF                                                                                                                                 | Adobe Reader                  |
| DOCS                                                                                                                                | Microsoft Word Viewer         |
| HTML\*                                                                                                                              | Internet Explorer 11 and Edge |
| \*If you are using [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client only for your customers and vendors must be using HTML to view their documents. |

## SQL Server Reporting Services requirements

Before you deploy [!INCLUDE[prodshort](../includes/prodshort.md)] Reporting Services reports, you must install and configure SQL Server Reporting Services, and then set up security for SQL Server Reporting Services reports. Review the following table for the version of SQL Server Reporting Services and the report type available for that version.

| SQL Server Reporting Services version                                                                                                        | Report type available                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Reporting Services 2012 Standard or Enterprise Reporting Services 2014 Standard or Enterprise Reporting Services 2016 Standard or Enterprise | SQL Server Reporting Services reports                   
                                                           
  Charts and key performance indicators (KPIs) Map charts  |

## Modify the Report Server web.config file

To deploy the SQL Server Reporting Services reports, you must modify the Report Server web.config file for the timeout execution and the maximum request length. If you don’t update the Report Server web.config file for the timeout execution, you might receive an error that states that the operation has timed out. If you don’t update the Report Server web.config file for the maximum request length, you will receive an error that the deployment has exceeded the maximum request length allowed by the target server.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")You must be an administrator to modify the Report Server web config file.  

To modify the Report Server Web config file:

1.  Create a backup copy of the web.config file located in the ReportServer folder. (The ReportServer folder is located in C:\\Program Files\\Microsoft SQL Server\\MSSQLSERVER\\Reporting Services\\ReportServer where Reporting Services is installed.)

2.  Open the Report Server web.config file using a text editor, such as Notebad.

3.  Search for &lt;httpRuntime executionTimeout="9000" /&gt;.

4.  In that line, change executionTimeout=”9000” to executionTimeout=”19000” and add the value maxRequestLength="20960".

(&lt;httpRuntime executionTimeout="19000" maxRequestLength="20960"/&gt;

1.  Save and close the Report Server web.config file.

## [!INCLUDE[prodshort](../includes/prodshort.md)] CRM requirements

You must be using SQL Server 2012 Reporting Services or later and Microsoft Dynamics CRM 2011 or later to deploy SQL Server Reporting Services reports and metrics that includes CRM data. Microsoft Dynamics CRM supports only the native mode of deployment of SQL Server Reporting Services.

If Microsoft Dynamics CRM and [!INCLUDE[prodshort](../includes/prodshort.md)] are using different report servers, you must install the Microsoft Dynamics CRM Reporting Extensions on the [!INCLUDE[prodshort](../includes/prodshort.md)] report server to render reports.

## About remote access

You can use Windows Server 2012 Remote Desktop Services, Windows Server 2012 R2 Remote Desktop Services, and Windows Server 2016 Remote Desktop Services. Citrix Xenapps can also be used with most database configurations to provide remote access to [!INCLUDE[prodshort](../includes/prodshort.md)] in a Wide Area Network (WAN) environment.

A Windows Server 2008 Terminal Server is supported only as a client. You also can use Remote Desktop Services.

For more information about system requirements see <http://go.microsoft.com/fwlink/?LinkId=521785>. You also should refer to the documentation provided by Citrix for more information.

## Determine disk space for the upgrade process

For the upgrade process, be sure that you have enough disk space before you begin. To determine the disk space required for the upgrade, you need to find the size of the largest table for all [!INCLUDE[prodshort](../includes/prodshort.md)] databases. To determine disk space, use Microsoft SQL Server Management Studio for Microsoft SQL Server.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")You can download an upgrade preparation script that will help you determine the disk space requirements from <https://mbs.microsoft.com/customersource/northamerica/GP/support/hot-topics/HOT_TOPIC_MDGP2018Upgrade>.  

To determine disk space for the upgrade process using Microsoft SQL Server Management Studio:

1.  Download and open the Table\_Size.txt script.

<!-- -->

1.  Copy all of the contents of the script.

2.  In Microsoft SQL Server Management Studio, select a [!INCLUDE[prodshort](../includes/prodshort.md)] database, click New Query and paste the contents. Then, execute the query.

3.  Run the script for each [!INCLUDE[prodshort](../includes/prodshort.md)] database.

4.  The largest table will be the first record in the result set. You will need to convert the table size from kilobytes to megabytes by using the following calculation. This will determine the amount of space that will be allocated to the data file (MDF) and the transaction log file (LDF) for each database.

(table size in KB/1024) = table size in MB

The table size in megabytes of the largest table from all the databases is the amount of disk space you will need to allocate to the data file of the TEMPDB.

In the following example, the largest table is the SOP30300 in the company database. The TEMPDB will need 176 MB allocated for the data file.

| Database | Total size KB | Rows   | Name     | MB  |
|----------|---------------|--------|----------|-----|
| DYNAMICS | 33913.171873  | 180872 | 98075    | 33  |
| TEST     | 180608.280270 | 98075  | SOP30300 | 176 |

1.  Calculate the total amount of hard disk space that is needed by adding the space needed for the data file and transaction log file of all databases.

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

1.  Verify that the space is available for each drive by using File Explorer. In Windows Explorer, right-click each drive and select Properties to view free space available. By using the information in the previous table, drive E would need at least 385 MB available and drive D would need at least 209 MB available.

2.  Use Microsoft SQL Server Management Studio to manually increase the space allocated for the data file and the transaction log file for the DYNAMICS database and each company database.

-   Right-click each database in Microsoft SQL Server Management Studio and select Properties.

-   In the properties window for each database, choose Files and add the additional space needed for the size of the largest table for that database to the Initial Size column. When adding additional space, you are increasing the space for the data file (MDF) and the transaction log file (LDF) as well.

-   Repeat for the remaining [!INCLUDE[prodshort](../includes/prodshort.md)] databases.

-   Right-click the TEMPDB database and select Properties. Choose Files and add the additional space needed for the size of the largest table of all [!INCLUDE[prodshort](../includes/prodshort.md)] databases to the Space Allocated (MB) column. When adding additional space, you are increasing the space for the data file (MDF) and the transaction log file (LDF) as well.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")If the database size is not manual configured, the time needed to upgrade the databases will increase because the database data, transaction log and TEMPDB files will all have to increase.  
