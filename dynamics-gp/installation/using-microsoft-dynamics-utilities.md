---
title: "Utilities for Dynamics GP"
description: "Set up the synchronization with the Dynamics GP data, create companies, and apply default settings using the Dynamics GP Utilities."
keywords: ""
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: ecc84869-2580-466e-a9eb-4c309b748b14
ms.reviewer: edupont
---
# Using Microsoft Dynamics Utilities

After you’ve installed Microsoft Dynamics GP, you need to complete a number of additional configuration procedures. To do this, you’ll use an application called Microsoft Dynamics GP Utilities.

### 

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")After you’ve installed Microsoft Dynamics GP, you need to complete a number of additional configuration procedures. To do this, you’ll use an application called Microsoft Dynamics GP Utilities.  

One of the most important—and difficult to change later—configuration tasks is setting up an account framework. Be sure to review Chapter 5, “Account framework,” before using the Microsoft Dynamics GP Utilities.

This chapter contains the following sections:

-   [Microsoft Dynamics GP Utilities overview](#microsoft-dynamics-gp-utilities-overview)  

-   [Installation options in Microsoft Dynamics GP Utilities](#installation-options-in-microsoft-dynamics-gp-utilities)  

-   [Preparing Microsoft Dynamics GP for use with default settings](#preparing-microsoft-dynamics-gp-for-use-with-default-settings)  

-   [Preparing Microsoft Dynamics GP for use with custom settings](#preparing-microsoft-dynamics-gp-for-use-with-custom-settings)  

-   [Additional installation tasks](#additional-installation-tasks)  

-   [Adding sample company data](#adding-sample-company-data)  

-   [Creating a company](#creating-a-company)  

-   [Removing SOP and Invoicing message](#removing-sop-and-invoicing-message)  

-   [Managing the Web Client SQL Server login](#managing-the-web-client-sql-server-login)  

-   [Managing user authentication](#managing-user-authentication)  

## Microsoft Dynamics GP Utilities overview

You’ll use Microsoft Dynamics GP Utilities to complete the following tasks after you’ve installed software and data on a server computer.

-   Select whether to use default or custom settings to configure the system database.

-   Create SQL Server databases for Microsoft Dynamics GP.

-   Deploy predefined SQL Server Reporting Services reports that are included in

-   Microsoft Dynamics GP.

-   Deploy predefined Microsoft Excel® reports that are included in Microsoft

-   Dynamics GP.

-   Create your account framework and synchronize the Microsoft Dynamics GP dictionary, if you are providing custom settings.

-   Select a default account framework and synchronize the Microsoft Dynamics

-   GP dictionary, if you decide to use default settings.

-   Define account sorting options, if you are providing custom settings.

-   Enter the password for the DYNSA user.

-   Set up the system password, which controls access to system management functions in Microsoft Dynamics GP, if you are providing custom settings.

-   Synchronize sample data with your account framework, if you installed the sample company.

-   Remove SOP and Invoicing message. This lets you removes a message that appears every time you enter a transaction in Sales Order Processing or Invoicing, if both modules are registered.

-   Create a SQLServer login for Microsoft Dynamics GP Web Client

-   Select the authentication type for the Microsoft Dynamics GP Web Client.

-   Create additional companies, as needed.

## Installation options in Microsoft Dynamics GP Utilities

When using Microsoft Dynamics GP Utilities, you can select an installation option to use default settings or to provide your own custom settings. If you select the Basic option, the default settings for the system database, the account framework, and system password are provided. If you select the Advanced option, you’ll provide the settings to create the database, the account framework, and system password.

The following table compares the default settings of the Basic option with the custom settings of the Advanced option.

| Setting           | Basic installation                                                                                                                                              | Advanced installation                                                                                                                                                                                                                                                                     |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System database   | The system database files are created at the default locations defined in the SQL Server.                                                                       
                                                                                                                                                                   
  A typical default location is \\Program Files\\Microsoft SQL Server\\MSSQL\\dat .                                                                                | You can specify the locations where the system database files are created in the SQL Server.                                                                                                                                                                                              |
| Account framework | The following account framework is created for you. Maximum number of segments: 5                                                                               
                                                                                                                                                                   
  Maximum Account Length: 45                                                                                                                                       
                                                                                                                                                                   
  Length of each segment: 9                                                                                                                                        
                                                                                                                                                                   
  Sorting Options: No sorting options by segment                                                                                                                   
                                                                                                                                                                   
  Account preview:                                                                                                                                                 
                                                                                                                                                                   
  xxxxxxxxx-xxxxxxxxx-xxxxxxxxx-xxxxxxxxx-xxxxxxxxx                                                                                                                | You can design your account framework by entering the maximum for the account length, the number of account segments, and the length of each segment. You also can select sorting options. For more information about designing an account framework, see Chapter 5, “Account framework.” |
| System password   | The system password is blank. This means that all users will have access to systemwide setup information. You can enter this password in Microsoft Dynamics GP. | You can enter a password for systemwide setup information.                                                                                                                                                                                                                                |

## Preparing Microsoft Dynamics GP for use with default settings

Use Microsoft Dynamics GP Utilities to prepare Microsoft Dynamics GP for use. Complete this procedure when you install Microsoft Dynamics GP for the first time. You need to do this only once.

With this procedure, you’ll select the Basic option in the Installation Options window to use default settings for the system database, account framework, and system password. For more information about the Basic option, see Installation options in Microsoft Dynamics GP Utilities on page 36.

Before you use Microsoft Dynamics GP Utilities, check for and install the most current update for Microsoft Dynamics GP 2018. See CustomerSource (<https://mbs.microsoft.com/customersource>) for the latest update information. After installing the update, start Microsoft Dynamics GP Utilities.

To prepare Microsoft Dynamics GP for use with default settings:

1. Start Microsoft Dynamics GP Utilities.
(Start &gt;&gt; All Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities)

![login screen to dynamics gp utilities](media/gp-utilities-2.png "Login screen")  

2. In the Welcome to Microsoft Dynamics GP Utilities window, verify your server name, and enter a system administrator user ID and password; then click OK.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")You must be logged in as a system administrator to complete database and system functions within Microsoft Dynamics GP Utilities.  

3. The Welcome To Microsoft Dynamics GP Utilities window opens when you are logged into the server you selected. Read the message and click Next.

4. The Installation Options window appears. Mark Basic and then click Next.

5. If the DYNSA user doesn’t have a password, the Enter DYNSA User Password window opens. Use this window to enter the password for the DYNSA user. The DYNSA user is the database owner and can perform tasks, such as table maintenance procedures. If you have multiple Microsoft Dynamics GP system databases on the same SQL Server instance, the DYNSA user is the database owner for all of the system databases. This password is case-sensitive.

![screen to enter dynsa user password](media/gp-utilities-3.png "SA user setup")  

Click Next.

6. In the Web Client SQL Server Login window, you can create a SQL Server login for Microsoft Dynamics GP Web Client. The Web Client SQL Server login is used for the connection to the SQL Server when a Microsoft Dynamics GP user has been configured with a Windows login.

![screen to set up sql server login](media/gp-utilities-4.png "SQL Server login setup")  

Mark the Using web client option if you are creating a SQL Server login for the Microsoft Dynamics GP Web Client. Enter an existing SQL Server login or enter a new login. Then, enter a password and confirm your password. Click Next.

Unmark the Using web client option if you are not creating a login for the Microsoft Dynamics GP Web Client. Click Next.

7. Select the authentication type for the Microsoft Dynamics GP web client. Accept the default Windows Account setting if GP users will be logging into the web client using their Windows domain credentials. Select Organizational Account if GP users will be logging into the web client using their organizational account credentials.

![screen to specify authentication type for gp users](media/gp-utilities-5.png "Authentication setup")  

When selecting Organizational Account, additional settings will be required complete the setup. Provide the Azure AD domain name for the user accounts. An example is contoso.onmicrosoft.com. Provide the name of the SQL Server where the web components database is stored and the name of the web components database.

8. In the Confirmation window, click Finish.

Microsoft Dynamics GP Utilities installs databases, installs initial module setup information, and sets up Microsoft Dynamics GP menus. These procedures may take several minutes to complete. The Server Installation Progress window describes the processes as they are completed.

9. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

![screen to set up business intelligence](media/gp-utilities-6.png "BI report setup")  

If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Additional Tasks window will reappear. Skip to step 11.

10. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports.

![screen to specify where to save excel reports](media/gp-utilities-7.png "Excel Report Setup")  

After selecting your report server mode, enter the locations to deploy the reports to.

Native mode location example.

| Location           | Example                                |
|--------------------|----------------------------------------|
| Report Server URL  | http://&lt;servername&gt;/ReportServer |
| Report Manager URL | http://&lt;servername&gt;/Reports      |

SharePoint Integrated mode location example.

| SharePoint Integrated |
|-----------------------|----------------|
| Location              | Example        |
| SharePoint Site       |                |
| Report Library        | ReportsLibrary |

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")Be sure that your locations don’t end with a slash. You can use the Reporting Services Configuration Manager to verify the Report Server Mode being used and the URL locations.  

11. If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple Microsoft Dynamics GP instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must to provide access to the folder.

12. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

The Excel Reports Setup window appears if you marked to deploy Microsoft Excel reports.

![screen to specify where to save excel reports](media/gp-utilities-7.png "Excel Report Setup")  

Select the location to deploy the reports to. Network share location example:

|               |                           |
|---------------|---------------------------|
| Network share | \\\\Servername\\sharename |

If you have selected SharePoint as the location to deploy reports to, you can mark the Using SharePoint Online option if you are using Microsoft Office 365 and want to deploy Excel reports to a reports library in SharePoint Online 2010. Mark the Using SharePoint Online option to deploy reports only in the Microsoft Dynamics GP desktop client. Reports will not be deployed for the Microsoft Dynamics GP Web Client.

SharePoint location example:

| SharePoint Site          |                |
|--------------------------|----------------|
| Data Connections Library |                |
| Report Library           | ReportsLibrary |

Be sure to use back slashes when you are entering the location for reports even if you are using a UNC path. You should also be sure that the location doesn’t end in a slash.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

13. In the Additional Tasks window, you can choose to perform additional procedures, start Microsoft Dynamics GP, or end the installation. If you select any task, click Process; otherwise, click Exit.

See Additional installation tasks for more information about additional installation tasks.

## Preparing Microsoft Dynamics GP for use with custom settings

Use Microsoft Dynamics GP Utilities to prepare Microsoft Dynamics GP for use. Complete this procedure when you install Microsoft Dynamics GP for the first time. You need to do this only once.

With this procedure, you’ll select the Advanced option in the Installation Options window to use custom settings for the system database, account framework, and system password. For more information about the Advanced option, see Installation options in Microsoft Dynamics GP Utilities on page 36.

Before you use Microsoft Dynamics GP Utilities, check for and install the most current update for Microsoft Dynamics GP 2018. See CustomerSource (<https://mbs.microsoft.com/customersource>) for the latest update information. After installing the update, start Microsoft Dynamics GP Utilities.

To prepare Microsoft Dynamics GP for use with custom settings:

1. Start Microsoft Dynamics GP Utilities.
(Start &gt;&gt; Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities)

2. In the Welcome to Microsoft Dynamics GP Utilities window, verify your server name, and enter a system administrator user ID and password; then click OK.

![login screen to dynamics gp utilities](media/gp-utilities-2.png "Login screen")  

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")You must be logged in as a system administrator to complete database and system functions within Microsoft Dynamics GP Utilities.  

3. The Welcome To Microsoft Dynamics GP Utilities window opens when you are logged into the server you selected. Read the message and click Next.

4. The Installation Options window appears. Mark Advanced and then click Next.

5. In the Database Setup window, enter the location to create the data and log devices (files). For more information about disk and RAID configuration, see <http://go.microsoft.com/fwlink/?LinkId=263763>. Click Next.

![database setup screen](media/gp-utilities-8.png "Database setup screen")  

6. In the Set Up Account Framework window, enter a framework for the accounts for all Microsoft Dynamics GP companies, as well as all companies you may set up in the future.

![screen to specify maximum values for accounts](media/gp-utilities-9.png "Account framework")  

Enter the maximum account length (up to 66 characters) and the maximum number of segments (up to 10) that you’ll need for the charts of accounts in companies you set up now or in the future. Maximums you enter now will apply to all companies you plan to set up.

See Planning your account framework on page 26 for more information.

7. In the Set Up Account Segment Lengths window, enter a name for each segment of the account, as well as the maximum length you’ll use for each segment in the charts of accounts for your companies.

![screen to specify account segment length](media/gp-utilities-10.png "Account framework")  

You should use descriptive names that clearly indicate how each segment will be used. These segment names will appear as the default segment names when you set up the account format for each company; you can change the names later, if necessary.

The length of each segment can be no longer than 66 characters. Maximums you enter now will apply to companies you set up later.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you have more than one company, you may need to enter maximum segment lengths that exceed the 66-character account length maximum when the segment lengths are added together. The total size must be 82 or less. See Choosing account framework storage size on page 27 for more information.  

8. Select sorting options in the Define Additional Sorting Options window. This window displays the predefined sorting options available in Microsoft Dynamics GP to sort account information in windows and on reports.

![set up sorting](media/gp-utilities-11.png "Account framework")  

-   If the displayed sorting options include the ways you’ll need to sort account information, leave the No option marked and click Next, then continue to step 10.

-   To select segments of your account framework to sort by, as well, mark Yes, then click Next. The Set Up Additional Sorting Options window appears. Continue to step 9.

![set up sorting for segments](media/gp-utilities-12.png "Account framework")  

9. If you selected Yes in step 8, select each account segment you want to use as a sorting option and click Add. You can define up to nine additional sorting options.

If you select more than one segment, use the Up and Down buttons to specify in what order the segments will be used to sort account information. Sorting options are used to control the way accounts are displayed in Microsoft Dynamics GP windows, in all your companies.

10. When you’ve finished selecting segments, click Next to verify your account framework in the Verify Account Framework window.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")To make corrections if necessary, click Back until the appropriate window is displayed, then click Next in each window until the Verify Account Framework window is displayed again.  

A report file called Acctfram.txt is created in the Data folder inside of the GP folder, which contains the same account framework information. This file, which is created only on the first client, stores account framework information for your reference. Be sure to make a backup of the Acctfram.txt file.

11. If the DYNSA user doesn’t have a password, the Enter DYNSA User Password window opens. Use this window to enter the password for the DYNSA user. The DYNSA user is the database owner and can perform tasks, such as table maintenance procedures. If you have multiple Microsoft Dynamics GP system databases on the same SQL Server instance, the DYNSA user is the database owner for all of the system databases. This password is case-sensitive.

![screen to enter dynsa user password](media/gp-utilities-3.png "SA user setup")  

12. In the Web Client SQL Server Login window, you can create a SQL Server login for Microsoft Dynamics GP Web Client. The Web Client SQL Server login is used for the connection to the SQL Server when a Microsoft Dynamics GP user has been configured with a Windows login.

![screen to set up sql server login](media/gp-utilities-4.png "SQL Server login setup")  

Mark the Using web client option if you are creating a SQL Server login for the Microsoft Dynamics GP Web Client. Enter an existing SQL Server login or enter a new login. Then, enter a password and confirm your password. Click Next.

Unmark the Using web client option if you are not creating a login for the Microsoft Dynamics GP Web Client. Click Next.

13. Select the authentication type for the Microsoft Dynamics GP web client. Accept the default Windows Account setting if GP users will be logging into the web client using their Windows domain credentials. Select Organizational Account if GP users will be logging into the web client using their organizational account credentials.

![screen to specify authentication type for gp users](media/gp-utilities-5.png "Authentication setup")  

When selecting Organizational Account, additional settings will be required complete the setup. Provide the Azure AD domain name for the user accounts. An example is contoso.onmicrosoft.com. Provide the name of the SQL Server where the web components database is stored and the name of the web components database.

14. In the Enter System Password window, enter the password to use to access Microsoft Dynamics GP system windows, reports, and utilities. This password is case-sensitive and will be used for control functions, such as user security.

![screen to specify system password](media/gp-utilities-13.png "System password setup")  

15. In the Confirmation window, click Next.

Microsoft Dynamics GP Utilities installs databases, installs initial module setup information, and sets up Microsoft Dynamics GP menus. These procedures may take several minutes to complete. The Server Installation Progress window describes the processes as they are completed.

16. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

![screen to set up business intelligence](media/gp-utilities-6.png "BI report setup")  

If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Additional Tasks window will reappear. Skip to step 19.

17. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports.

![screen to specify where to save sql server reporting services reports](media/gp-utilities-14.png "SSRS Report Setup")  

After selecting your report server mode, enter the locations to deploy the reports to.

Native mode location example:

| Location           | Example                                |
|--------------------|----------------------------------------|
| Report Server URL  | http://&lt;servername&gt;/ReportServer |
| Report Manager URL | http://&lt;servername&gt;/Reports      |

SharePoint Integrated mode location example.

| SharePoint Integrated |
|-----------------------|----------------|
| Location              | Example        |
| SharePoint Site       |                |
| Report Library        | ReportsLibrary |

18. If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple Microsoft Dynamics GP instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must to provide access to the folder.

19. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

20. The Excel Reports Setup window appears if you marked to deploy Excel reports.

![screen to specify where to save excel reports](media/gp-utilities-7.png "Excel Report Setup")  

21. Select the location to deploy the reports to.

Network share location example:

|               |                           |
|---------------|---------------------------|
| Network share | \\\\Servername\\sharename |

SharePoint location example:

| SharePoint Site          |                |
|--------------------------|----------------|
| Data Connections Library |                |
| Report Library           | ReportsLibrary |

Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

22. In the Additional Tasks window, you can choose to perform additional procedures, start Microsoft Dynamics GP, or end the installation. If you select any task, click Process; otherwise, click Exit.

See Additional installation tasks for more information about additional installation tasks.

## Additional installation tasks

The Additional Tasks window in Microsoft Dynamics GP Utilities contains the following selections:

-   Add sample company data

-   Create a company

-   Remove SOP and Invoicing message

-   Update modified forms and reports

-   Synchronize forms and reports dictionaries

-   Manage Web Client SQL Server login

-   Manage user authentication

The Update modified forms and reports option is used when upgrading from a previous release; it isn’t used when you initially install Microsoft Dynamics GP. The Synchronize forms and report dictionaries option can be used at anytime when you want to synchronize your forms and reports to your account framework.

Start Microsoft Dynamics GP Utilities if you haven’t already and follow the instructions in the Microsoft Dynamics GP Utilities windows until you open the Additional Tasks window. The following procedures assume that the Additional Tasks window is open.

## Adding sample company data

You can add data for the sample company, Fabrikam, Inc., to your Microsoft Dynamics GP system to practice procedures. If a Microsoft Dynamics GP feature is installed, the sample data for that feature will be included when adding sample data. When you are adding the sample company, you can create LessonUser1 and LessonUser2 as sample users. These users will have access only to Fabrikam, Inc. The process of adding sample company data may take some time.

When you create the sample company, you can deploy business intelligence components, such as SQL Server Reporting Services reports. If you deployed reports for your system database, you can use the default report locations for the sample company.

To add sample company data:

1. Select the Add sample company data option in the Additional Tasks window and click Process.

2. In the Database Setup window, enter or accept the sample company database name and then select a default location for new files that will be created for the sample company.

TWO is the default sample company database name if the TWO database doesn’t exist. You can only create LessonUser1 and LessonUser2 as sample users for the TWO sample company database using the Microsoft Dynamics GP Utilities.

If the sample company database has a different name than TWO, you must use the User Setup window to create lesson users for the sample company and then use the User Access Setup window to set up user access to the sample company.

3. In the Create Sample Users window, enter a password that will be used by the sample users, LessonUser1 and LessonUser2, to access the sample company. Reenter your password exactly as you previously entered it.

The Create Sample Users window appears if you are creating sample users for the TWO sample company database. If the sample company database is not the TWO database, you will not be able to create sample users using Microsoft Dynamics GP Utilities.

4. Click Next.

5. In the Confirmation window, click Finish.

The Server Installation Progress window appears, showing the progress as the tables are loaded.

6. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Additional Tasks window will reappear.

7. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports. After selecting your report server mode, enter the locations to deploy the reports to.

Native mode location example:

| Location           | Example                                |
|--------------------|----------------------------------------|
| Report Server URL  | http://&lt;servername&gt;/ReportServer |
| Report Manager URL | http://&lt;servername&gt;/Reports      |

SharePoint Integrated mode location example.

| SharePoint Integrated |
|-----------------------|----------------|
| Location              | Example        |
| SharePoint Site       |                |
| Report Library        | ReportsLibrary |

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")Be sure that your URL locations don’t end with a slash. You can use the Reporting Services Configuration Manager to verify the Report Server Mode being used and the URL locations.  

8. If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple Microsoft Dynamics GP instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must provide access to the folder.

9. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

10. The CRM Reports Setup window appears, if you marked to deploy SQL Server Reporting Services reports with CRM data. Enter the CRM connection information. Microsoft Dynamics CRM supports only the native mode of deployment of SQL Server Reporting Services.

We recommend that you use Windows Authentication (Integrated Security). If you select to be prompted for credentials, you must mark the Use as Windows credentials when connecting to the data source option on the data source deployed.

11. The Excel Reports Setup window appears if you marked to deploy Excel reports. Select the location to deploy the reports to.

If you have selected SharePoint as the location to deploy reports to, you can mark the Using SharePoint Online option if you are using Microsoft Office 365 and want to deploy Excel reports to a reports library in SharePoint Online 2010. Mark the Using SharePoint Online option to deploy reports only in the Microsoft Dynamics GP desktop client. Reports will not be deployed for the Microsoft Dynamics GP Web Client.

Be sure to use back slashes when you are entering the location for reports even if you are using a UNC path. You should also be sure that the location doesn’t end in a slash.

Network share location example:

|               |                           |
|---------------|---------------------------|
| Network share | \\\\Servername\\sharename |

SharePoint location example.

| SharePoint Site          |                 |
|--------------------------|-----------------|
| Data Connections Library | DataConnections |
| Report Library           | ReportsLibrary  |

12. Click Next.

If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\username and the password you use to log in to Microsoft Windows.

13. The Verify SQL Server window appears. Confirm your selections. If the selections are correct, click Finish.

The Business Intelligence Deployment Progress window appears. This window displays the report deployment progress.

14. After the reports deployed, the Additional Tasks window will reappear.

## Creating a company

This option will create SQL tables that are needed for your company data. You must have at least one company set up before you can start Microsoft Dynamics GP.

When you create a new company, you can deploy business intelligence components, such as SQL Server Reporting Services reports. If you deployed reports for your system database, you can use the default report locations for the company.

When adding a company, you can select how to configure your company. You can use wizards to migrate data from Intuit QuickBooks or Peachtree and enter basic configuration options, or you can configure the company later using the Setup Checklist window in Microsoft Dynamics GP. To use a wizard to migrate or configure data, you must download and install the Rapid Implementation Tools for Microsoft Dynamics GP. If you haven’t installed the Rapid Implementation Tools, click the Download and install the wizards link in the Company Setup Options window.

For each company you create, be sure the folder you specify must exist on the hard disk.

To create a company:

1. Select the Create a company option in the Additional Tasks window and click Process.

2. In the Create Company window, enter a company ID and name and select additional options.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")The additional options, such as shipping methods and payment terns, may be overwritten if you choose to use the wizards to migrate QuickBooks or Peachtree data and enter basic configuration information in step 6.  

3. Click Next.

4. In the Database Setup window, select a default location for new files that will be created.

5. The Confirmation window appears. Confirm your selections. If the selections are correct, click Finish.

The Server Installation Progress window appears, showing progress as tables loaded.

6. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Company Setup Options window appears. Skip to step 13.

7. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports. After selecting your report server mode, enter the locations to deploy the reports to.

Native mode location example:

| Location           | Example                                |
|--------------------|----------------------------------------|
| Report Server URL  | http://&lt;servername&gt;/ReportServer |
| Report Manager URL | http://&lt;servername&gt;/Reports      |

SharePoint Integrated mode location example.

| SharePoint Integrated |
|-----------------------|----------------|
| Location              | Example        |
| SharePoint Site       |                |
| Report Library        | ReportsLibrary |

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")Be sure that your URL locations don’t end with a slash. You can use the Reporting Services Configuration Manager to verify the Report Server Mode being used and the URL locations.  

8. If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple Microsoft Dynamics GP instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must provide access to the folder.

9. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

10. The CRM Reports Setup window appears, if you marked to deploy SQL Server Reporting Services reports with CRM data. Enter the CRM connection information. Microsoft Dynamics CRM supports only the native mode of deployment of SQL Server Reporting Services.

We recommend that you use Windows Authentication (Integrated Security). If you select to be prompted for credentials, you must mark the Use as Windows credentials when connecting to the data source option on the data source deployed.

11. The Excel Reports Setup window appears if you marked to deploy Excel reports. Select the location to deploy the reports to.

If you have selected SharePoint as the location to deploy reports to, you can mark the Using SharePoint Online option if you are using Microsoft Office 365 and want to deploy Excel reports to a reports library in SharePoint Online 2010. Mark the Using SharePoint Online option to deploy reports only in the Microsoft Dynamics GP desktop client. Reports will not be deployed for the Microsoft Dynamics GP Web Client.

Be sure to use back slashes when you are entering the location for reports even if you are using a UNC path. You should also be sure that the location doesn’t end in a slash.

<span id="_Hlk494100347" class="anchor"></span>Network share location example:

|               |                           |
|---------------|---------------------------|
| Network share | \\\\Servername\\sharename |

SharePoint location example.

| SharePoint Site          | Server          |
|--------------------------|-----------------|
| Data Connections Library | DataConnections |
| Report Library           | ReportsLibrary  |

12. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

13. The Verify SQL Server window appears. Confirm your selections. If the selections are correct, click Finish.

The Business Intelligence Deployment Progress window appears. This window displays the report deployment progress.

14. The Company Setup Options window appears, where you can select to use a wizard to migrate data from QuickBooks or Peachtree, use a wizard to enter basic configuration options, or configure the company later using the Setup Checklist window in Microsoft Dynamics GP.

To use a wizard to migrate or configure data, you must download and install the Rapid Implementation Tools for Microsoft Dynamics GP. If you haven’t installed the Rapid Implementation Tools, click the Download and install the wizards link in the Company Setup Options window before you click Next.

15. Click Next. If you decided to configure your company later, the Additional Tasks window reappears. You can click Create a company to set up a second company, start Microsoft Dynamics GP, or Exit.

If you decided to use a wizard to migrate or configure your company data, the Rapid Migration Tool or the Rapid Configuration Tool starts.

## Removing SOP and Invoicing message

Return to Microsoft Dynamics GP Utilities and complete this task after you’ve set up Sales Order Processing. The following message will appear every time you enter a transaction in Sales Order Processing or Invoicing, if both modules are registered: “Sales Order Processing and Invoicing modules are both installed. They do not share information. Transactions should be entered in one module only.” To remove this message, select Remove SOP and Invoicing message in the Additional Tasks window and click Process, then follow the instructions in the window.

## Managing the Web Client SQL Server login

Use the Manage Web Client SQL Server Login window to create or modify a SQL Server login for Microsoft Dynamics GP Web Client. By using the single Web Client SQL Server login, each web client user can access the web client by providing their standard Windows login credentials instead of using their own SQL Server login.

During the initial Microsoft Dynamics GP installation, you can create the SQL Server login. Each web client session can use the login to access SQL Server.

To manage the Web Client SQL Server login:

1. Select the Manage Web Client SQL Server Login option in the Additional Tasks window and click Process.

2. In the Manage Web Client SQL Server Login window, specify the SQL Server

Login and password for the Web Client SQL Server login.

3. If the login has an existing password, you can mark the Change password option to enter a different password.

4. Click Save. The Additional Tasks window reappears.

## Managing user authentication

Use the Manage user authentication process to change the authentication type for this Microsoft Dynamics GP instance. If there are accounts assigned for the current authentication type, the assigned accounts will be removed when the authentication type is changed. You cannot change the authentication type if there is an active workflow or a workflow that is currently pending user action.

During the initial Microsoft Dynamics GP installation, you selected an authentication type. If you upgraded to GP 2018 from a previous release, the authentication type was set to Windows Account automatically.

To manage the user authentication

1. Select the manage user authentication option in the Additional Tasks window and click Process.

2. In the Manage User Authentication window, select the Authentication Type drop down and select the authentication type.

3. If you have selected Organizational Account, provide the required configuration information for using Organizational Accounts.

Provide the Azure AD domain name for the user accounts. An example is contoso.onmicrosoft.com. Provide the name of the SQL Server where the web components database is stored and the name of the web components database.

4. Click OK. The Additional Tasks window reappears.
