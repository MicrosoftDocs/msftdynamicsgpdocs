---
title: "Configure SQL Server"
description: "Set up SQL Server so that you can install Dynamics GP."
keywords: ""
author: jswymer
ms.author: jswymer
manager: annbe
applies_to: 
ms.date: 10/12/2021
ms.topic: how-to
ms.assetid: a292895a-a538-4ae6-a3d2-cd8bb93de39a
ms.reviewer: jswymer
---
# Microsoft SQL Server configuration

### Microsoft SQL Server Installation for Dynamics GP

This chapter guides you through the Microsoft SQL Server 2012 and the Microsoft SQL Server 2012 Express Installation and setup process for Dynamics GP. It's important that you install and set up Microsoft SQL Server according to these instructions.

If you've already installed and set up SQL Server using different options, you may have to change those options. Changing options after they've been set sometimes involves reinstalling SQL Server.

This chapter contains the following sections:

- [SAN and NAS disk support](#san-and-nas-disk-support)  

- [Selecting a SQL Server collation](#selecting-a-sql-server-collation)  

- [Understanding sorting options](#understanding-sorting-options)  

- [Installing Microsoft SQL Server 2012](#installing-microsoft-sql-server-2012)  

- [Installing Microsoft SQL Server 2012 Express Edition](#installing-microsoft-sql-server-2012-express-edition)  

- [Setting up an ODBC data source using the SQL Native Client driver](#setting-up-an-odbc-data-source-using-the-sql-native-client-driver)  

- [SQL Server Agent](#sql-server-agent)  

- [Enabling Delete PJournal job](#enabling-delete-pjournal-job)  

## SAN and NAS disk support

Because Dynamics GP relies on SQL Server to maintain databases and make databases available, there are guidelines you must follow when configuring SQL Server disk support.

We recommend that you use a Storage Area Network (SAN) or locally attached disk to store your Microsoft SQL Server database files because this configuration optimizes SQL Server performance. By default, use of network database files stored on a networked server or Network Attached Storage (NAS) is not enabled for SQL Server. However, you can configure SQL Server to store a database on a networked server or NAS storage server. Servers used for this purpose must meet SQL Server requirements for data write ordering and write-through guarantees.

If you are using Microsoft SQL Server Express Edition, SAN and NAS disk support isn't typically used.

For more information, see Microsoft Knowledge Base article, "Description of support for network database files in SQL Server," (go to <https://support.microsoft.com> and search for the article) or contact the SQL Server Support Team.

## Selecting a SQL Server collation

A SQL Server collation—a set of rules that determines how character data is sorted and compared—includes character set, sort order, and locale-specific settings. See your SQL Server 2012 documentation for more information about collation settings.

The SQL Server collation you select determines how information is presented in response to SQL queries and affects the performance of the system.

The code page for character data is defined by the Windows locale selected when the operating system was installed. The code page contains the valid set of characters in your SQL Server database. A character set consists of 256 uppercase and lowercase letters, numbers, and symbols. The first 128 characters are the same for all character sets. The supported character set in the United States is the 1252/ ISO character set.

It is important to select the correct collation for Dynamics GP when you're installing SQL Server. Using SQL Server collations that include Binary (sort order 50) or Dictionary Order, Case-Insensitive (sort order 52) sorting is required for Dynamics GP. To change these settings later, you must reinstall SQL Server and Dynamics GP.

> [!NOTE]
> You should check the compatibility of all the products you have that will use SQL Server before deciding on the collation option.  

## Understanding sorting options

Using SQL Server collations that include Binary (sort order 50) or Dictionary Order, Case-Insensitive (sort order 52) sorting is required.

Binary sort order assigns characters numeric values of 0 through 255. Dictionary Order, Case-Insensitive (DOCI) sort order makes no distinction between uppercase and lowercase characters. DOCI is the most common sort order.

The following table shows the differences between Dictionary Order, Case- Insensitive and Binary.

| Sort order                          | Technical name                    | Sorting result               |
|-------------------------------------|-----------------------------------|------------------------------|
| Dictionary Order, Case- Insensitive | SQL\_Latin1\_General\_CP1\_CI\_AS | McMaster MMCompanyName Zebra |
| Binary                              | Latin1\_General                   | MMCompanyName   Zebra                         |

## Installing Microsoft SQL Server 2012

We recommend that you follow the instructions in this section if you have not yet installed Microsoft SQL Server 2012. For information about upgrading SQL Server, see the SQL Server installation documentation. (In the window that appears when you insert the SQL Server DVD, select Browse Setup/Upgrade Help.)

> [!NOTE]
> With SQL Server 2012, you can have multiple instances of SQL Server on the same physical server. We recommend that you have a dedicated a server. See your SQL Server 2012 documentation for more information about multiple instances.  

To install Microsoft SQL Server 2012:

1. Insert the SQL Server 2012 installation media. The main SQL Server installation screen should appear. If you do not see this screen, browse the media and double-click the Setup.exe file.

2. After the SQL Server Installation Center appears, click Installation in the left pane. Then, click New SQL Server stand-alone installation or add features to an existing installation.

3. Your computer is scanned for conditions that may stop installation. To proceed with the installation, click OK in the Setup Support Rules window.

4. In the Product Key window, enter the product key. Click Next.

5. Mark the option to accept the terms of the license terms and then click Next.

6. SQL Server setup files are installed on your computer. To proceed with the installation, click Next in the Setup Support Rules window.

7. In the Setup Role window, select SQL Server Feature Installation, and click Next.

8. In the Feature Selection window, select the features you want to use and specify the location to install SQL Server 2012. You should install at least the following features to use Dynamics GP.

    - Database Engine Services

    - Client Tools Connectivity

    - Client Tools Backwards Compatibility

    - Documentation Components

    - Management Tools – Basic

> [!NOTE]
> Select Reporting Services – Native or Reporting Services – SharePoint to use SQL Server Reporting Services reports, display SQL Server Reporting Services metrics on your home page in Dynamics GP, and display SQL Server Reporting Services reports in Microsoft Dynamics Business Analyzer. If you have marked Reporting Services – SharePoint, be sure to mark Reporting Services Add-in for SharePoint Products as well. For more information about installing and setting up SQL Server Reporting Services for use with Dynamics GP see the [Documentation and resources for Dynamics GP](https://go.microsoft.com/fwlink/?LinkId=249465) site for the most current documentation.  

Click Next.

9. Your computer is scanned again for conditions that may stop installation. To proceed with the installation, click Next in the Installation Rules window.

10. In the Instance Configuration window, select a default or named instance for your installation.

    - To install a new default instance (the primary instance on the computer), select Default instance and click Next. There can be only one default instance.

    - To install a named instance, select Named instance and then enter a unique instance name. Click Next.

    - If a default or named instance is already installed, select the existing instance for your installation and click Next. The instance upgrades and you will have the option to install additional components.

    For information about using instances of SQL Server, see your SQL Server documentation. We recommend that you have a dedicated server.

11. The required disk space is calculated. Click Next.

12. In the Services Accounts tab, we recommend that you use the same account for each service and automatically start services.

13. In the Collation tab, click the Customize button for the Database Engine.

14. In the Customize the SQL Server 2012 Database Engine Collation window, you can select Binary or Dictionary Order, Case-Insensitive as the sorting option. For more information, see [Selecting a SQL Server collation](#selecting-a-sql-server-collation).

> [!WARNING]
> Check the compatibility of all the products, such as Business Portal for Dynamics GP and Workflow, you have that will use SQL Server before deciding on the collation option.  

**Binary**   To use Binary sorting, use the Windows Collation designator and sort order option and make the following selections in the window.

![screenshot of configuration of sql server database collation window with windows collation selected](media/sql-server-collation_01.png "SQL Server collation")  

**Dictionary Order, Case-Insensitive**   To use Dictionary Order, Case- Insensitive sorting, choose SQL collation, used for backwards compatibility option and make the following selections in the window.

![screenshot of configuration of sql server database collation window with sql collation selected](media/sql-server-collation_02.png "SQL Server collation")  

Click OK after you make your selections, and then click Next.

15. In the Database Engine Configuration window, select Mixed Mode as the authentication mode in the Server Configuration tab. Mixed Mode is required by Dynamics GP.

    With Mixed Mode, users can connect using Windows Authentication or SQL Server Authentication. You must enter and confirm the system administrator password when you select Mixed Mode. You'll use this is the password to log in to Dynamics GP Utilities as the system administrator.

    You must specify at least one system administrator. To add the account, click Add Current User to add accounts to the list of system administrators.

    Click Next.

16. If you selected to install Reporting Services, use the Reporting Services Configuration page to specify the type of Reporting Services installation to create. Click Next.

17. In the Error Reporting window, select to allow error reporting. Click Next.

18. Your computer is scanned again for conditions that may stop installation. To proceed with the installation, click Next in the Installation Configuration Rules window.

19. In the Ready to Install window, review the list of components that will be installed and click Install.

20. The Installation Progress window appears, allowing you to view the status of the installation. Click Next after the installation is completed.

21. In the Complete window, click Close to exit the installation wizard.

22. Restart the computer if you are instructed to do so.

23. Install the current SQL Server 2012 service pack. See the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx) for the latest service pack information.

## Installing Microsoft SQL Server 2012 Express Edition

Microsoft SQL Server 2012 Express Edition has a maximum database size of 10 GB. You can download Microsoft SQL Server 2012 Express from [www.microsoft.com](https://www.microsoft.com). Be sure to download SQL Server 2012 Express with data management tools. You can download SQL Server 2012 Books Online for SQL Server Express from [www.microsoft.com](https://www.microsoft.com).

Use the information in this section to install Microsoft SQL Server 2012 Express on your computer.

To install Microsoft SQL Server 2012 Express Edition:

1. Download SQL Server 2012 Express with data management tools.

2. A dialog window appears, showing the progress of the files being extracted.

3. After the files have been extracted, the SQL Server Installation Center appears.

4. Click New installation or add features to an existing installation.

5. Mark the option to accept the terms of the License Agreement and then click Next.

6. The Setup Support Rules window appears while your computer is scanned again for conditions that may stop installation.

7. In the Feature Selection window, select the features you want to use and specify the location to install SQL Server 2012 Express. Click Next.

8. In the Instance Configuration window, select a default or named instance for your installation.

    - To install a new default instance (the primary instance on the computer), select Default instance and click Next. There can be only one default instance.

    - To install a named instance, select Named instance and then enter a unique instance name. Click Next.

    - If a default or named instance is already installed, select the existing instance for your installation and click Next. The instance upgrades and you will have the option to install additional components.

    For information about using instances of SQL Server, see your SQL Server documentation. We recommend that you have a dedicated server.

9. In the Services Accounts tab, we recommend that you use the same account for each service and automatically start services. Click Use the same account for all SQL Service services to open a window where you can enter a user name and password. Click OK to return to the Server Configuration window.

10. In the Account Provisioning tab, select Mixed Mode as the authentication mode. Mixed Mode is required by Dynamics GP.

    With Mixed Mode, users can connect using Windows Authentication or SQL Server Authentication. You must enter and confirm the system administrator password when you select Mixed Mode. You'll use this is the password to log in to Dynamics GP Utilities as the system administrator.

    You must specify at least one system administrator. To add the account, click Add Current User to add accounts to the list of system administrators.

    Click Next.

11. In the Error Reporting window, select to allow error reporting. Click Next.

12. The Installation Progress page appears, allowing you to view the status of the installation.

13. In the Complete window, click Close to exit the installation wizard.

14. Restart the computer if you are instructed to do so.

15. Install the current SQL Server 2012 Express service pack. See the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx) for the latest service pack information.

## Setting up an ODBC data source using the SQL Native Client driver

You must set up a 32-bit Open Database Connectivity (ODBC) data source using SQL Native Client or SQL Native Client 10 on your computer. If you are using SQL Server 2012, you must set up a 32-bit Open Database Connectivity (ODBC) data source using SQL Native Client or SQL Native Client 11 on your computer. Use these instructions to enter the appropriate setup information for ODBC for SQL Server.

If you are using a 64-bit operating system, you must set up a 32-bit ODBC data source. For instructions on how to set up a data source for a 64-bit operating system, see the Microsoft Knowledge Base article [How to set up an ODBC Data Source on SQL Server for Dynamics GP](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb;en-us;870416).

To set up an ODBC data source using the SQL Native Client driver:

1. Open the ODBC Data Source Administrator window.

2. Select the System DSN tab and choose Add.

3. In the Create New Data Source window, select SQL Native Client, SQL Native Client 10.0, or SQL Native Client 11.0 from the list and choose Finish.

    The options in the list depend on the version of SQL Server you are using.

4. In the first Create a New Data Source to SQL Server window, enter the following information.

| Field       | Value                                                                                     |
|-------------|-------------------------------------------------------------------------------------------|
| Name        | Enter the name to use for the data source. This name will be stored in the Odbc.ini file. |
| Description | Enter a description of the data source.                                                   |
| Server      | Enter the name you assigned to the SQL Server when you installed Microsoft SQL Server.    |

Choose Next.

In the second Create a New Data Source to SQL Server window, select With SQL Server authentication using a login ID and password entered by the user option as how to verify the login ID.

6. Enter sa as the login ID and enter a password. Choose Next.

7. In the third Create a New Data Source to SQL Server window, be sure that all the options are unmarked and choose Next.

8. In the fourth Create a New Data Source to SQL Server window, be sure that all the options are unmarked. Choose Finish.

9. In the ODBC Microsoft SQL Server Setup window, verify your settings and choose OK. You can also choose the Test Data Source button to test it before choosing OK.

## SQL Server Agent

When you install Dynamics GP on the server, an automated database maintenance job is created. SQL Server Agent is used to run automated jobs.

Be sure that the SQL Server Agent service is set up to start automatically with the operating system if you are using Microsoft SQL Server. In SQL Server Service Manager, select SQL Server Agent from the list of services and mark the Auto-start service when OS starts option.

Jobs are customizable, and you can select how frequently they should be completed. You may want certain jobs to run every half hour, while others should run once at night. For more information on scheduling jobs, refer to Microsoft SQL Server Books Online.

SQL Server Agent is not available for SQL Server Express. For information about how to schedule backups for SQL Server Express, see the Microsoft Knowledge Base article [How to schedule and automate backups of SQL Server databases in SQL Server Express](https://support.microsoft.com/kb/2019698/).

<!--Microsoft SQL Server 2008 Express doesn't include SQL Server Agent. Refer to [Support Hot Topic on CustomerSource](https://learn.microsoft.com/dynamics/s-e/) for more information about scheduling a backup.-->

## Enabling Delete PJournal job

The Delete PJournal job is created during the installation of Dynamics GP. By enabling the Delete PJournal job, the speed of the posting process is increased.

To enable Delete PJournal job using SQL Server

Management Studio:

1. Open SQL Server Management Studio by choosing Start &gt;&gt; Programs &gt;&gt; Microsoft SQL Server &gt;&gt; SQL Server Management Studio.

2. Log in to Microsoft SQL Server.

3. Expand SQL Server Agent, and click Jobs.

    If you are using SQL Server 2012, expand Jobs.

4. Right-click on Remove Posted PJournals for your company database and click Properties to open the Properties window.

5. Unmark and mark the Enable option.

6. Click Apply and then click OK.


## Guidance for running Microsoft Dynamics GP with Microsoft SQL Server AlwaysOn Availability Groups

Describes the requirements to run Microsoft Dynamics GP with Microsoft SQL Server AlwaysOn Availability Groups.

SQL Server AlwaysOn Availability Groups is a high-availability and disaster-recovery solution introduced in SQL Server 2012. The solution creates a failover environment for a set of application databases. Refer to the [AlwaysOn Availability Group documentation for additional information](/sql/database-engine/availability-groups/windows/always-on-availability-groups-sql-server?redirectedfrom=MSDN&view=sql-server-ver15&preserve-view=true)

Deploying Microsoft Dynamics GP with SQL Server AlwaysOn Availability Groups to provide a high-availability configuration will include.

1.	Configuring SQL Server AlwaysOn Availability Groups using the synchronous-commit availability mode and automatic failover.
a.	Adding the GP system and company databases to the availability group.
2.	Creating an availability group listener that GP will use to connect to the SQL Server databases.
3.	Implementing a solution to synchronize SQL Logins across the availability group.



### Configuring SQL Server AlwaysOn Availability Groups

Use the [Creation and Configuration of Availability Groups documentation](/sql/database-engine/availability-groups/windows/creation-and-configuration-of-availability-groups-sql-server?redirectedfrom=MSDN&view=sql-server-ver15&preserve-view=true) to set up the availability group. Note that in order to complete the setup of the availability group, you will need to have the Microsoft Dynamics GP databases created. You will use Dynamics Utilities to connect to the target primary replica SQL Server instance to create the databases. Make sure when configuring the SQL Server replicas that you select Automatic Failover and Synchronous Commit. Using these options along with an availability group listener will provide you with a single virtual address to the availability group. The availability group listener’s virtual address will then be used as the name of the SQL Server for the Microsoft Dynamics GP components, like the GP runtime ODBC data source. The result is automatic application failover after an availability group fails over. 

You will need to put all of the GP system and company databases in a single availability group so they all fail over together. Verify the [Prerequisites, Restrictions, and Recommendations for AlwaysOn Availability Groups](/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?redirectedfrom=MSDN&view=sql-server-ver15&preserve-view=true) and specifically that the GP databases are using full recovery mode.

According to the documentation, the synchronous-commit availability mode emphasizes high availability and data protection over performance, resulting in increased transaction latency. Testing has shown a performance impact running Microsoft Dynamics GP in this mode, with certain processes showing a 5-15% degradation. 

### Creating an availability group listener

Use the [Create or Configure an Availability Group Listener documentation](/sql/database-engine/availability-groups/windows/creation-and-configuration-of-availability-groups-sql-server?redirectedfrom=MSDN&view=sql-server-ver15&preserve-view=true) to set up the availability group listener. The listener requires a DNS host name that is unique in your domain and the NetBIOS. The DNS host name is the value you will enter for the SQL Server name when setting up the Microsoft Dynamics GP components. 

### Synchronize SQL logins

Since you are not able to configure the SQL Server system databases as part of an availability group, you will need to implement a separate solution in order to synchronize the SQL logins across the replicas of the availability group. It is very important when using SQL identities for Microsoft Dynamics GP that you implement a solution that synchronizes logins in a continuous fashion since SQL logins may be added, removed or changed continually from within Microsoft Dynamics GP. The solution will need to synchronize users from the primary replica to the secondary replicas, but remember that after a fail over the primary replica may be a SQL instance that was previously a secondary replica. The result is that the solution will need to be able to synchronize logins from any replica in the group if it becomes the primary replica after a fail over. The solution will need to synchronize the passwords of the SQL logins so after a failover the GP user is able to log in using their most current user name and password.

There are various tools and processes available for synchronizing logins in an AlwaysOn Availability Group. Review the SQL Server documentation or reach out to the SQL Server team via a support case or their community forums if you need assistance with setting this up and running.
