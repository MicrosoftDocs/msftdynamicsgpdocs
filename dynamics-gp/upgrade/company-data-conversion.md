---
title: "Company data conversion"
description: "Learn about the additional procedures to upgrade your tables before you can use Dynamics GP."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 08/24/2018
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: d6f63af5-9c23-46f9-8f22-4bcee28287be
ms.reviewer: 
---
# Company data conversion

After you’ve upgraded your software, you need to complete a number of additional procedures to upgrade your tables before you can use Dynamics GP. To do this, you’ll use an application called Dynamics GP Utilities. Follow the instructions in this chapter to use Dynamics GP Utilities to upgrade tables on your server and client computers.

Before using Dynamics GP Utilities, be sure that you have installed the most current update for your Dynamics GP system. You also should make a backup of your databases.

> [!NOTE]
> To start Dynamics GP Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system’s documentation for more information.  

## Enabling a DexSQL.log

If an error occurs during the upgrade process, you should change several settings in the Dex.ini file so that a DexSQL.log file will record some SQL operations for one user from one client computer. The DexSQL.log file is a helpful tool that can capture SQL operations and provide information if there are issues during the upgrade.

To enable a DexSQL.log:

You’ll have to restart Dynamics GP Utilities after you made the changes.

1.  Open the Dex.ini file in the Data folder of the current Dynamics GP folder.

2.  Change the following statements to TRUE.

    SQLLogSQLStmt=FALSE

    SQLLogODBCMessages=FALSE

    SQLLogAllODBCMessages=FALSE

3.  Save your changes.

## Upgrading Dynamics GP tables

Use this procedure to upgrade Dynamics GP tables on your server computer using Dynamics GP Utilities. You will not need to complete all of these procedures on subsequent computers. When you start Dynamics GP Utilities for subsequent computers, the Additional Tasks window will immediately open, where you can complete additional tasks, such as upgrading your modified forms and reports. The process of upgrading tables may take some time.

Detailed lists of the changes to all tables are available on the Dynamics GP media. To access the table changes lists, install the Software Developers’ Kit from the Dynamics GP media.

> [!WARNING]
> If you are using Connector for Microsoft Dynamics, you must stop the Microsoft Dynamics Adapter Service on the server before starting Dynamics GP Utilities. The company database upgrade will fail if the Microsoft Dynamics Adapter Service is not stopped. Connector is not supported for Dynamics GP, so it’s not necessary to restart the service after the service after the upgrade is complete.  

To upgrade Dynamics GP tables:

1 Back up your system database and all company databases.

2. Start Dynamics GP Utilities.
(Start &gt;&gt; All Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities)

3. In the Welcome to Dynamics GP Utilities window, verify your server name, enter the system administrator user ID and password, and click OK.

![login screen to dynamics gp utilities.](media/gp-utilities-2.png "Login screen")  

> [!NOTE]
> You must be logged in as a system administrator to complete database and system functions within Dynamics GP Utilities.  

4. The Welcome To Dynamics GP Utilities window opens when you are logged into the server that you selected. Read the message and click Next.

5. In the Upgrade Dynamics GP window, click Next to upgrade your system database.

> [!NOTE]
> The Company Detail window opens if errors occurred while upgrading your system tables. You can use this window to view the errors.  

6. In the Upgrade these companies window, click Next. All companies are selected to be upgraded.

> [!NOTE]
> The process of upgrading tables might take some time.  

![shows screen to specify which companies your want to upgrade.](media/upgrade-company-1.png "Upgrade these companies?")  

7. In the Confirmation window, click Finish.

    Dynamics GP Utilities upgrades your company databases. This process may take several minutes to complete. The Server Installation Progress window describes the process as it progresses.

8. After the upgrade process is finished and is successful, the Additional Tasks window will open, where you can upgrade your forms and reports dictionaries, start Dynamics GP, or exit the installation. To upgrade your forms and reports dictionaries, see [Upgrading modified forms and reports](#upgrading-modified-forms-and-reports) for more information. See the following sections for more detailed information about each task.

![screen with list of tasks that open setup wizards.](media/gp-utilities-15.png "Task selector")  

If the upgrade process wasn’t successful, the Update Company Tables window opens. See [Understanding upgrade warnings](#understanding-upgrade-warnings) for more information.  

## Additional upgrade tasks

You’ll use the following selections from the Additional Tasks window to upgrade your Dynamics GP files.

- Re-add or Add sample company data

- • Update modified forms and reports

For more information about upgrading forms and reports, see [Upgrading modified forms and reports](#upgrading-modified-forms-and-reports).  

Start Dynamics GP Utilities if you haven’t already and follow the instructions in the Dynamics GP Utilities windows until you open the Additional Tasks window. The following procedures assume that the Additional Tasks window is open.

## Re-adding sample company data

If you’ve upgraded the sample company from a previous release, you can add the sample data again. If you’ve used the sample data in a previous release, you may want to re-add the data to practice procedures in Dynamics GP. If a Dynamics GP feature is installed, the sample data for that feature will be included when adding or re-adding sample data. The process of reinstalling sample company data may take some time.

If you are adding sample data again and haven’t previously deployed business components for the sample company, you can deploy business intelligence components, such as SQL Server Reporting Services reports.

To re-add sample company data:

1. Select the Re-add sample company data option in the Additional Tasks window and click Process.

2. A message will be displayed indicating that the lesson company (sample company) is installed. Choose to reinstall the lesson company.

3. In the Confirmation window, click Finish.

    The Server Installation Progress window appears, showing the progress as the tables are loaded.

4. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

    If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Additional Tasks window will reappear.

5. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports. After selecting your report server mode, enter the locations to deploy the reports to.

Native mode location example:

| Location             | Example                                  |
|----------------------|------------------------------------------|
| Report Server URL    | http://&lt;servername&gt;/ReportServer   |
| Report Manager URL   | http://&lt;servername&gt;/Reports        |

SharePoint Integrated mode location example:


| Location             | Example                                  |
|-------------------------------------|-----------------------------------------------------|
| SharePoint Site       | http://&lt;servername&gt;/Reports |

> [!NOTE]
> Be sure that your URL locations don’t end with a slash. You can use the Reporting Services Configuration manager to verify the Report Server Mode being and the URL locations.  

If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple Dynamics GP instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must provide access to the folder.

6. Click Next.

> [!NOTE]
> If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

7. The CRM Reports Setup window appears, if you marked to deploy SQL Server Reporting Services reports with CRM data. Enter the CRM connection information. Microsoft Dynamics CRM supports only the native mode of deployment of SQL Server Reporting Services.

    We recommend that you use Windows Authentication (Integrated Security). If you select to be prompted for credentials, you must mark the Use as Windows credentials when connecting to the data source option on the data source deployed.

8. The Excel Reports Setup window appears if you marked to deploy Excel reports. Select the location to deploy the reports to.

    If you have selected SharePoint as the location to deploy reports to, you can mark the Using SharePoint Online option if you are using Microsoft Office 365 and want to deploy Excel reports to a reports library in SharePoint Online 2010. Mark the Using SharePoint Online option to deploy reports only in the Dynamics GP desktop client. Reports will not be deployed for the Dynamics GP Web Client.

    Be sure to use back slashes when you are entering the location for reports even if you are using a UNC path. You should also be sure that the location doesn’t end in a slash.

Network share location example:

| Network share              | [\\\\Servername\\sharename](file:///\\Servername\sharename) |  
|----------------------------|-------------------------------------------------------------|
| SharePoint Site            | http://&lt;servername&gt;/Reports                           |
| Data Connections Library   | DataConnections                                             |
| Report Library             | ReportsLibrary                                              |

9. Click Next.

> [!NOTE]
> If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

10. The Verify SQL Server window appears. Confirm your selections. If the selections are correct, click Finish.

    The Business Intelligence Deployment Progress window appears. This window displays the report deployment progress.

    After the reports deployed, the Additional Tasks window will reappear.

## Adding sample company data

If the sample company has never been installed before, you can add data for the sample company to your Dynamics GP system to practice procedures. If a Dynamics GP feature is installed, the sample data for that feature will be included when adding or re-adding sample data. The name of the sample company is Fabrikam, Inc. When you are adding the sample company, you can create LessonUser1 and LessonUser2 as sample users. These users will have access only to Fabrikam, Inc. The process of adding sample company data may take some time.

When you create the sample company, you can deploy business intelligence components, such as SQL Server Reporting Services reports. If you deployed reports for your system database, you can use the default report locations for the sample company.

To add sample company data:

1. Select the Add sample company data option in the Additional Tasks window and click Process.

2. In the Database Setup window, enter or accept the sample company database name and then select a default location for new files that will be created for the sample company.

    TWO is the default sample company database name if the TWO database doesn’t exist. You can only create LessonUser1 and LessonUser2 as sample users for the TWO sample company database using the Dynamics GP Utilities.

    If the sample company database has a different name than TWO, you must use the User Setup window to create lesson users for the sample company and then use the User Access Setup window to set up user access to the sample company.

3. In the Create Sample Users window, enter a password that will be used by the sample users, LessonUser1 and LessonUser2, to access the sample company. Reenter your password exactly as you previously entered it. Click Next.

    The Create Sample Users window appears if you are creating sample users for the TWO sample company database. If the sample company database is not the TWO database, you will not be able to create sample users using Dynamics GP Utilities.

4. In the Confirmation window, click Finish.

    The Server Installation Progress window appears, showing the progress as the tables are loaded.

5. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

    If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Additional Tasks window will reappear.

6. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports. After selecting your report server mode, enter the locations to deploy the reports to.

Native mode location example:

| Location             | Example                                  |
|----------------------|------------------------------------------|
| Report Server URL    | http://&lt;servername&gt;/ReportServer   |
| Report Manager URL   | http://&lt;servername&gt;/Reports        |

SharePoint Integrated mode location example:



| Location              | Example                           |
|-----------------------|-----------------------------------|
| SharePoint Site       | http://&lt;servername&gt;/Reports |

> [!NOTE]
> Be sure that your URL locations don’t end with a slash. You can use the Reporting Services Configuration Manager to verify the Report Server Mode being used and the URL locations.  

If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple Dynamics GP instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must provide access to the folder.

7. Click Next.

> [!NOTE]
> If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

8. The CRM Reports Setup window appears, if you marked to deploy SQL Server Reporting Services reports with CRM data. Enter the CRM connection information. Microsoft Dynamics CRM supports only the native mode of deployment of SQL Server Reporting Services.

    We recommend that you use Windows Authentication (Integrated Security). If you select to be prompted for credentials, you must mark the Use as Windows credentials when connecting to the data source option on the data source deployed.

9. The Excel Reports Setup window appears if you marked to deploy Excel reports. Select the location to deploy the reports to.

    If you have selected SharePoint as the location to deploy reports to, you can mark the Using SharePoint Online option if you are using Microsoft Office 365 and want to deploy Excel reports to a reports library in SharePoint Online 2010. Mark the Using SharePoint Online option to deploy reports only in the Dynamics GP desktop client. Reports will not be deployed for the Dynamics GP Web Client.

    Be sure to use back slashes when you are entering the location for reports even if you are using a UNC path. You should also be sure that the location doesn’t end in a slash.

Network share location example:

|               |                                                             |
|---------------|-------------------------------------------------------------|
| Network share | [\\\\Servername\\sharename](file:///\\Servername\sharename) |  

SharePoint location example

| SharePoint Site          | http://&lt;servername&gt;/Reports   |
|--------------------------|-------------------------------------|
| Data Connections Library | DataConnections                     |
| Report Library           | ReportsLibrary                      |

10. Click Next.

> [!NOTE]
> If you don’t have the appropriate permissions to deploy the reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

11. The Verify SQL Server window appears. Confirm your selections. If the selections are correct, click Finish.

    The Business Intelligence Deployment Progress window appears. This window displays the report deployment progress.

12. After the reports deployed, the Additional Tasks window will reappear.

## Upgrading modified forms and reports

You can use Dynamics GP to upgrade the following types of information for modified forms and reports:

- Fields where the data type has been changed are upgraded automatically on modified forms and reports.

- Fields that have been moved from one table to another are upgraded automatically on forms and reports that use those fields.

- Fields that have been removed from tables are removed from corresponding forms and reports.

In addition, similar changes are made to modified forms and reports for integrating applications. Consult the documentation for the integrating application for information about whether that application supports automatic form and report upgrades. If you are using Personal Data Keeper, see the Dynamics GP technical support for information about synchronizing forms and reports.

> [!NOTE]
> If your forms and reports dictionaries are in a shared location, you need only to perform this procedure once.  

To upgrade modified forms and reports:

1. Make a backup of each reports dictionary or forms dictionary to upgrade. The name of the reports dictionary for Dynamics GP is Reports.dic and the name of the forms dictionary for Dynamics GP is Forms.dic.

2. Open the Dynamics GP launch file (Dynamics.set) and verify that the paths to the modified reports and forms are correct. The paths must be the location of the reports dictionary and forms dictionary from the previous release.

3. In the Additional Tasks window, select Update modified forms and reports and click Process. The Locate Launch File window appears.

4. Select the Dynamics GP launch file (Dynamics.set) that you use to start Dynamics GP on this client, then click Next. The Update Modified Forms and Reports window appears.

5. Select Dynamics GP and any additional components whose modified forms and reports dictionaries you’re upgrading.

6. For each component, choose the Details button, if necessary, to open the Product Details window, where you can select the location of the original dictionary, such as Dynamics.dic or HR.dic. Click OK in the Product Details window.

The original dictionary is the application dictionary from the previous release of Dynamics GP. After all forms and reports dictionaries have been upgraded, you can delete the original dictionary.

7. In the Update Modified Forms and Reports window, click Update.

    Your modified forms and reports dictionaries are upgraded, and a report named Update2013.txt is generated, which contains information about upgraded modified forms. Be sure to review the report, located in the \\Data folder, to verify that your modified forms have been upgraded correctly.

8. Click Next. The Additional Tasks window reappears.

    Be sure to review the Update2013.txt and Update2013.log, for more information about the modified forms and reports upgrade.

## Managing the Web Client SQL Server login

Use the Manage Web Client SQL Server Login window to create or modify a SQL Server login for Dynamics GP Web Client. By using the single Web Client SQL Server login, each web client user can access the web client by providing their standard Windows login credentials instead of using their own SQL Server login.

During the initial Dynamics GP installation, you can create the SQL Server login. Each web client session can use the login to access SQL Server.

To manage the Web Client SQL Server login:

1. Select the Manage Web Client SQL Server Login option in the Additional Tasks window and click Process.

2. In the Manage Web Client SQL Server Login window, specify the SQL Server Login and password for the Web Client SQL Server login.

3. If the login has an existing password, you can mark the Change password option to enter a different password.

Click Save. The Additional Tasks window reappears.

## Understanding upgrade warnings

After the upgrade or if the upgrade fails, the Update Company Tables window will be displayed. This window indicates the status of a company by the icon displayed between the check box and the name of the company, as shown in the following illustration.

| Icon                                                    | Status                                                                                 |
|---------------------------------------------------------|----------------------------------------------------------------------------------------|
| ![shows green checkmark.](media/upgrade-conversion-success.png "Success")   | Company tables were upgraded successfully.                                             |  
| ![shows read x](media/upgrade-conversion-notsuccess.png "Failure")   | Some company tables were not upgraded successfully. Contact Microsoft                    
                                                                                          
  Dynamics GP Technical Support for further assistance.                                   |
| ![shows read yellow exclamation point.](media/upgrade-conversion-warnings.png "Warning")   | Some company tables have warnings associated with them.                                |  
| ![shows padlock.](media/upgrade-conversion-locked.png "Locked")              | Not converted; someone at another client computer is currently upgrading this company. |  

If no icon appears between the check box and the name of the company, the company needs to be upgraded.

If errors do occur, download the Failed\_Tables\_List.txt script from <https://mbs.microsoft.com/customersource/northamerica/GP/support/hot-topics/HOT_TOPIC_MDGP2018Upgrade>, and save it to your hard disk. Copy all of the contents of the script and paste the contents them into Microsoft SQL Server Management Studio. Run the script and save the results to a file before you contact Dynamics GP for further assistance.

You also should have the results of the DexSQL.log file ready, as well, if you decided to use the DexSQL.log file. (The DexSQL.log file is located in the same folder as the Dex.ini file.)

If warnings appear for temporary files or for modules that the company does not currently use, the warnings can be ignored. If warnings appear for modules that the company currently uses, note the warnings. You can attempt the upgrade again or contact Dynamics GP Technical Support for further assistance.
