---
title: "System preparation"
description: "Prepare your system, including client computers before you upgrade to the latest version of Dynamics GP."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 08/24/2018
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 288c5bf3-9273-4a2d-804f-a33f87de69f7
ms.reviewer: 
---
# System Preparation

<span id="_Toc498615780" class="anchor"></span>

We recommend that you complete the steps in this chapter before you upgrade your system. Be sure to follow the instructions on how to prepare your data in [Data preparation](data-preparation.md) before preparing your system. After you've completed the steps in this chapter, see [Installing Dynamics GP on the first computer](installing-on-first-computer.md) for instructions to upgrade Dynamics GP.  

## Updates

We recommend that you check for and install the most current Dynamics GP update for the release you are upgrading to. For the latest update information, see [Dynamics GP Downloads](/dynamics/s-e/gp/mdgp2018_release_download_378).

Be sure that you have installed the most current updates for your Dynamics GP system before using Dynamics GP Utilities to upgrade your databases. If you don't install the update before using Dynamics GP Utilities, the fixes will not take effect. After upgrading your database, install the update on your client computers.

You can't log in to Dynamics GP on a client computer if a Dynamics GP feature or additional component installed on the client has different version information than the server. For more information about upgrading Dynamics GP features and additional components, see [Additional features and components upgrade]additional-features-and-components-upgrade.md).  

## Reviewing the Readme file

To view additional information, use the Readme file on the Dynamics GP media. Be sure to review the Readme file (GPReadme.chm) before installing Dynamics GP.

## Installing components on all client computers

We recommend that you install each registered Dynamics GP feature and additional components on all client computers. If you're using Project Accounting, you should install Project Accounting on every computer that you have installed Dynamics GP on. You must install Bank Management on all clients for Direct Debits and Refunds to work properly.

## Upgrading Integration Manager

Before you install Integration Manager 2018, we recommend that you make a backup copy your existing Integration Manager database (usually called IM.mdb) and then remove any previous versions of Integration Manager. You can remove earlier versions of Integration Manager, but it's not required.

To remove Integration Manager, use your system's Add/Remove Programs utility, and select Integration Manager.

After you install Integration Manager 2018, you must convert the database you backed up. After you convert your SQL Optimized data to Integration Manager

2018 for the eConnect adapter, review your destination settings and verify that they are correct. For more information about installing Integration Manager and converting a database, refer to the Integration Manager User 's Guide.

## Upgrading in a test environment

It is recommended that you use a test environment to practice the process of upgrading Dynamics GP, additional components, modified forms and reports, and customizations. By using a test environment, you can resolve any potential issues that may occur before you upgrade your current release of Dynamics GP. You also can estimate the time it will take to upgrade your current release to Dynamics GP. A test environment also allows users to test their day-to-day tasks to ensure that processes are working properly, and to learn the new features and modules in Dynamics GP.

A test environment can be a single server or a server with one or more client computers where an upgrade takes place. The client computers can be used for testing and training purposes. There isn't a required number of computers that need to be involved in a test environment.

## Backups

You should make at least one complete backup of all your databases before upgrading. You also should make a backup of all your modified dictionaries as well. It's a good idea to make a backup before completing table maintenance procedures, in case you encounter any problems in that process. You also should make a backup of eConnect pre and post procedures and your existing Integration Manager database.

If you are upgrading a company that has previously deployed SQL Server Reporting Services reports and Microsoft Excel reports, the deployed reports are automatically upgraded. If you have modified reports, those reports will be overwritten during the upgrade. Be sure to make a backup of your reports.

## Database maintenance

For your SQL database, you should run the following database maintenance routine against the DYNAMICS database and all company databases in or Microsoft SQL Server Management Studio. The database maintenance routine will help to ensure that your table structure is ready to be upgraded if there are no errors indicated. Be sure that there are no allocation or consistency errors in the results.

If you prefer to perform table maintenance only on the tables that have changed, lists of tables that have changed from previous releases are available on the Dynamics GP media as part of the Software Developers' Kit (SDK).

> [!NOTE]
> It's a good idea to make a second backup after performing table maintenance, but before upgrading to a new version. If you have this backup and an expected problem occurs while upgrading, you won't have to repeat the table maintenance step.  

## Known issues

Review the following known issues before upgrading to Dynamics GP.

### Records that aren't valid in purchase order tables

If records that aren't valid exist in the Purchase Order Line table (POP10110), or in the Purchase Order Line History table (POP30110), or in both tables, the upgrade can fail.

You can download an upgrade preparation script that will help you determine the disk space requirements from [CustomerSource](/dynamics/s-e/).

To verify purchase order tables:

1.  Download and open the Invalid\_Records\_POTables.txt script.

2.  Copy all of the contents of the script and paste the contents of the script into Microsoft SQL Server Management Studio.

3.  Run the script against all company databases.

4.  If results aren't returned after running the script, invalid records don't exist. You can upgrade to Dynamics GP.

If results are returned after running the script, invalid records exist and you can use Microsoft SQL Server Management Studio to remove these records. You also can check links in the Purchasing series before upgrading to Dynamics GP to remove invalid records.

### Microsoft SQL Server 2012 database compatibility level

If you have upgraded to Microsoft SQL Server 2012 before upgrading to Dynamics GP, be sure to change your database compatibility level to SQL Server 2012 (110) for all your databases.

To change the database compatibility level:

1. Open the SQL Server Management Studio. Log in to the server.

2. In the Object Explorer, expand the databases.

3. Right-click on a database and click Properties to open the database properties window.

4. Select Options in the Select a Page pane.

5. In the Compatibility level field, select SQL Server 2012 (110) as the level.

6. Repeat steps 4 through 6 until all the databases have been changed.

### Microsoft SQL Server 2014 database compatibility level

If you have upgraded to Microsoft SQL Server 2014 before upgrading to Dynamics GP, be sure to change your database compatibility level to SQL Server 2014 (120) for all your databases.

To change the database compatibility level:

1. Open the SQL Server Management Studio. Log in to the server.

2. In the Object Explorer, expand the databases.

3. Right-click on a database and click Properties to open the database properties window.

4. Select Options in the Select a Page pane.

5. In the Compatibility level field, select SQL Server 2014 (120) as the level.

6. Repeat steps 4 through 6 until all the databases have been changed.

### Microsoft SQL Server 2016 database compatibility level

If you have upgraded to Microsoft SQL Server 2016 before upgrading to Dynamics GP, be sure to change your database compatibility level to SQL Server 2016 (120) for all your databases.

To change the database compatibility level:

1. Open the SQL Server Management Studio. Log in to the server.

2. In the Object Explorer, expand the databases.

3. Right-click on a database and click Properties to open the database properties window.

4. Select Options in the Select a Page pane.

5. In the Compatibility level field, select SQL Server 2016 (120) as the level.

6. Repeat steps 4 through 6 until all the databases have been changed.

### The Server drop-down list is blank in Welcome to Dynamics GP window

If the Server drop-down list is blank in the Welcome to Dynamics GP window after you upgrade, you must set up an Open Database Connectivity (ODBC) data source using SQL Native Client 10 or SQL Native Client 11 on your computer.

If you are using a 64-bit operating system, you must set up a 32-bit ODBC data source. For instructions on how to set up a data source for a 64-bit operating system, see Microsoft Knowledge Base article, [How to set up an ODBC Data Source on SQL Server for Dynamics GP](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb;en-us;870416).

To set up an ODBC data source using the SQL Native Client 10 driver:

1. Open the ODBC Data Source Administrator window.

2. Select the System DSN tab and choose Add.

3. In the Create New Data Source window, select SQL Native Client 10 from the list and choose Finish.

4. In the first Create a New Data Source to SQL Server window, enter the following information.

| Field       | Value                                                                                     |
|-------------|-------------------------------------------------------------------------------------------|
| Name        | Enter the name to use for the data source. This name will be stored in the Odbc.ini file. |
| Description | Enter a description of the data source.                                                   |
| Server      | Enter the name you assigned to the SQL Server when you installed Microsoft SQL Server.    |

Choose Next.

5. In the second Create a New Data Source to SQL Server window, select With SQL Server authentication using a login ID and password entered by the user option as how to verify the login ID.

6. Enter sa as the login ID and enter a password. Choose Next.

7. In the third Create a New Data Source to SQL Server window, be sure that all the options are unmarked and choose Next.

8. In the fourth Create a New Data Source to SQL Server window, be sure that all the options are unmarked. Choose Finish.

9. In the ODBC Microsoft SQL Server Setup window, verify your settings and choose OK. You can also choose the Test Data Source button to test it before choosing OK.

To set up an ODBC data source using the SQL Native Client 11 driver:

1. Open the ODBC Data Source Administrator window.

2. Select the System DSN tab and choose Add.

3. In the Create New Data Source window, select SQL Native Client 11 from the list and choose Finish.

4. In the first Create a New Data Source to SQL Server window, enter the following information.

| Field       | Value                                                                                     |
|-------------|-------------------------------------------------------------------------------------------|
| Name        | Enter the name to use for the data source. This name will be stored in the Odbc.ini file. |
| Description | Enter a description of the data source.                                                   |
| Server      | Enter the name you assigned to the SQL Server when you installed Microsoft SQL Server.    |

Choose Next.

5. In the second Create a New Data Source to SQL Server window, select With SQL Server authentication using a login ID and password entered by the user option as how to verify the login ID.

6. Enter sa as the login ID and enter a password. Choose Next.

7. In the third Create a New Data Source to SQL Server window, be sure that all the options are unmarked and choose Next.

8. In the fourth Create a New Data Source to SQL Server window, be sure that all the options are unmarked. Choose Finish.

9. In the ODBC Microsoft SQL Server Setup window, verify your settings and choose OK. You can also choose the Test Data Source button to test it before choosing OK.

### Tables contain incorrect account framework information

If the following tables contain incorrect account framework information, the upgrade will fail. You must run the following script in each company to correct the issue.

| Table physical name   | Table display name                      |
|-----------------------|-----------------------------------------|
| GL10110               | Account Current Summary Master          |
| GL10111               | Account Summary History                 |
| GL70500               | General Ledger Report Options           |
| GL70501               | General Ledger Report Options Temporary |
| GL00200               | Budget Master                           |
| GL00201               | Budget Summary Master                   |

> [!NOTE]
> You can download an upgrade preparation script that will help you determine incorrect account framework information from <https://docs.microsoft.com/dynamics/s-e/>.  

### To verify account framework information in tables:

1. Download and open the Account\_Framework\_Validation.txt script.

2. Copy all of the contents of the script and paste the contents of the script into

Microsoft SQL Server Management Studio.

3. Run the script against any database.

4. If results aren't returned after running the script, the tables are in the correct format.

If results are returned after running the script, the tables do not match the account framework information. Contact the Dynamics GP Update Technical Support Team for instructions before upgrading. You can contact Dynamics GP Technical Support using one of the following methods.

- Create a [Support request](https://mbs.microsoft.com/support/newstart.aspx).

- Contact by telephone at 1-888-477-7877.

### Dynamics GP Utilities not responding

During the upgrade process, the Dynamics GP Utilities might appear as not responding and a Dynamics GP Utilities window might appear as white. Do not cancel Dynamics GP Utilities. Dynamics GP Utilities is still processing.

### Budget date records in Analytical Accounting

The AA Budget Tree Balance (AAG00904) table contains the records for each budget in Analytical Accounting. If there are budget date records in the AAG00904 table that do not exist in the aaDateSetup (AAG00500) table, the upgrade will fail and the following error occurs.

AAG00904 135 \[Microsoft\]\[SQL Server Native Client 10.0\]\[SQL Server\]Cannot insert the value NULL into column'YEAR1', table 'XXXX.dbo.AAG00904'; column does not allow nulls.UPDATE fails.

To validate budget date records in the Analytical Accounting:

1. Copy the following script and paste it into Microsoft SQL Server Management Studio.

    select distinct(a.PERIODDT) from AAG00904 a, AAG00500 b where a.PERIODDT not in (select b.date1 from AAG00500 b)

2. Run the script against the company database.

3. If results aren't returned after running the script, you can upgrade to Dynamics GP.

    If results show that there are budget date records that do not exist in the AAG00500 table, continue with the next step.

4. Run the following script to see if there is a fiscal or calendar year set up in the SY40101 (Period Header) table for the budget dates.

    select \* from SY40101

5. If there a fiscal or calendar year isn't set up for the date, you must set up the fiscal or calendar year for those budget record dates before you can upgrade.

    If there is a fiscal or calendar year set up for the date, the records are missing from the AAG00500 table. Complete the following steps.

6. Run the following script to back up the AAG00500 table.
