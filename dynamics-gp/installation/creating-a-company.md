---
title: "Company setup"
description: "Create a company in Dynamics GP manually."
keywords: ""
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: ee700f07-5dd2-44a6-af03-3d2c9647744d
ms.reviewer: edupont
---
<span id="_Toc499731577" class="anchor"></span>

# Creating a company

Use the instructions in this chapter to create a company if you didn’t create one when you first used [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities. You must set up at least one company before you can start [!INCLUDE[prodshort](../includes/prodshort.md)]. See your System Setup instructions (Help &gt;&gt; Contents &gt;&gt; select Setting up the system) for information about setting up users and companies in [!INCLUDE[prodshort](../includes/prodshort.md)].

This chapter contains the following sections:

-   [Chart of accounts overview](#chart-of-accounts-overview)  

-   [Adding a company using [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities](#adding-a-company-using-microsoft-dynamics-gp-utilities)  

## Chart of accounts overview

Several default charts of accounts are included with your [!INCLUDE[prodshort](../includes/prodshort.md)]

system. You may want to use a default chart of accounts for the following reasons:

-   The charts of accounts we’ve provided reflect sound accounting practices.

-   Extensive research was done to determine the most commonly used account types for the industries we’ve included.

-   Even if changes need to be made after a default chart of accounts is copied for the company, setup time will be greatly reduced by using a default chart.

Based on the business and industry types you choose for your company, you can install the chart of accounts best tailored for your company’s business needs. For instance, if your company is a retail corporation, select Corporation from the Business Type list, as shown in the previous illustration, then select Retail from the Industry Type list. Accounts specific to corporations, such as stock accounts, will then be added to the chart of accounts specifically designed for retail industries.

If you use a default chart of accounts, you won’t be able to shorten the account format. However, it can be lengthened to the maximum length you established in the Account Definition Setup window of [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, earlier in the installation process. Refer to the System Setup instructions (Help &gt;&gt; Contents &gt;&gt; select Setting up the system) for more information about lengthening account formats.

To preview the default chart of accounts for various business and industry types, review the Default Charts of Accounts for [!INCLUDE[prodshort](../includes/prodshort.md)] article (http:// go.microsoft.com/fwlink/?LinkId=89042).

The default chart of accounts you choose for your company in this procedure is designed to be an accurate estimate of your company’s business practices. However, we recommend that you review the accounts and make any necessary additions or changes. You’ll be directed to the General Ledger documentation later in the setup process, if you need to modify the accounts.

## Adding a company using [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities

Use [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities to create companies for [!INCLUDE[prodshort](../includes/prodshort.md)]. You must have at least one company set up before you can start [!INCLUDE[prodshort](../includes/prodshort.md)].

When adding a company, you can select how to configure your company. You can use wizards to migrate data from QuickBooks or Peachtree and enter basic configuration options, or you can configure the company later using the Setup Checklist window in [!INCLUDE[prodshort](../includes/prodshort.md)]. To use a tool to migrate or configure data, you must download and install the Rapid Implementation Tools for [!INCLUDE[prodshort](../includes/prodshort.md)]. If you haven’t installed the Rapid Implementation Tools, click the Download and install the wizards link in the Company Setup Options window.

Before you begin, be sure you have adequate space to add companies (including the sample company) to your SQL database. Each company requires about 300MB of free space.

When you create a company, you can deploy SQL Server Reporting Services reports and Excel reports using [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities. If you have deployed reports for your system database, you can use the default report locations for the company.

To start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system’s documentation for more information.

To add a company using [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities:

1. Start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities.
(Start &gt;&gt; Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities)

2. In the Welcome to [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities window, verify your server name, and enter a system administrator user ID and Password; then click Next.

![login screen to dynamics gp utilities](media/gp-utilities-2.png "Login screen")  

3. In the Welcome to [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities window, review the information and click Next.

4. The Upgrade [!INCLUDE[prodshort](../includes/prodshort.md)] window opens, indicating that [!INCLUDE[prodshort](../includes/prodshort.md)] is at the current version. Click Next to verify version information for companies.

5. After companies are verified, the Additional Tasks window opens. Select Create a company and then click Process.

6. The Create Company window opens, where you can enter a database/company ID, and a company name. You also can select the following options.

   -   Mark to load shipping methods and payment terms.

    -   Mark the Load Default Chart of Accounts option and click a business and industry type. For more information about charts of accounts, see Chart of accounts overview on page 63.

    -   Copy access from another company, except from the sample company, Fabrikam, Inc.

![screen for setting up a company](media/create-company-01.png "Company Setup")  

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you choose to use wizards to migrate QuickBooks or Peachtree data and enter basic configuration information in step 10, the shipping methods and payment terms and the chart of accounts information you have loaded may change.  

7. Click Next after entering and selecting company information.

8. The Database Setup window appears. Enter the location where the data and log devices should be created. Click Next.

![database setup screen](media/create-company-02.png "Database setup screen")  

9. The Very SQL Server window appears. Confirm your selections. If the selections are correct, click Finish.

    The Server Installation Progress window appears, showing progress as tables loaded.

10. In the Business Intelligence Reports Setup window, select the business intelligence components to deploy. Click Next. The window that opens depends on the components you selected.

    If you don’t want to deploy business intelligence components, leave the components unmarked and click Next. The Company Setup Options window appears. Skip to step 18.

11. The SQL Server Reporting Services Reports Setup window appears if you marked to deploy Reporting Services reports. After selecting your report server mode, enter the locations to deploy the reports to. Be sure that the location you enter does not end with a slash.

Native mode location example:

| Location           | Example                                |
|--------------------|----------------------------------------|
| Report Server URL  | http://&lt;servername&gt;/ReportServer |
| Report Manager URL | http://&lt;servername&gt;/Reports      |

SharePoint Integrated mode location example.

| Location |         Example      |
|-----------------------|----------------|
| SharePoint Site       |                |
| Report Library        | ReportsLibrary |

12. If you have selected Native as the report server mode, you can enter the name of the folder to deploy the reports to. By using a folder, you can deploy Reporting Services reports for multiple [!INCLUDE[prodshort](../includes/prodshort.md)] instances to a single Microsoft SQL Server Reporting Server. The default folder name is the name of the system database. If DYNAMICS is the system database name, the Folder Name field is blank. After deploying reports to the folder, you must provide access to the folder.

13. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

16. The Excel Reports Setup window appears if you marked to deploy Excel reports. Select the location to deploy the reports to.

If you have selected SharePoint as the location to deploy reports to, you can mark the Using SharePoint Online option if you are using Microsoft Office 365 and want to deploy Excel reports to a reports library in SharePoint Online 2010. Mark the Using SharePoint Online option to deploy reports only in the [!INCLUDE[prodshort](../includes/prodshort.md)] desktop client. Reports will not be deployed for the [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client.

Be sure to use back slashes when you are entering the location for reports even if you are using a UNC path. You should also be sure that the location doesn’t end in a slash.

Network share location example:

|               |                           |
|---------------|---------------------------|
| Network share | \\\\Servername\\sharename |

SharePoint location example.

| SharePoint Site          | Server          |
|--------------------------|-----------------|
| Data Connections Library | DataConnections |
| Report Library           | ReportsLibrary  |

17. Click Next.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")If you don’t have the appropriate permissions to deploy reports, a window opens where you can enter a domain\\user name and the password you use to log in to Microsoft Windows.  

18. The Verify SQL Server window appears. Confirm your selections. If the selections are correct, click Finish.

    The Business Intelligence Deployment Progress window appears. This window displays the report deployment progress.

19. The Company Setup Options window appears, where you can select one of the following options to configure your company.

    -   Mark the Set up the company later option to set up your company at another time. When you are ready to set up data for your company, you can use wizards to migrate data from QuickBooks or Peachtree and enter basic configuration options, or you can configure the company using the Setup Checklist window in [!INCLUDE[prodshort](../includes/prodshort.md)].

    -   Mark the Set up the company using the configuration wizard option to use the Rapid Configuration Tool for [!INCLUDE[prodshort](../includes/prodshort.md)]. The Rapid Configuration Tool helps you enter the basic setup information required for [!INCLUDE[prodshort](../includes/prodshort.md)]. With the Rapid Configuration Tool, you can start with a standard industry configuration, modify the configuration data, and then import the data into [!INCLUDE[prodshort](../includes/prodshort.md)]. Or, you can import a configuration from a Microsoft Office Excel workbook prepared by a [!INCLUDE[prodshort](../includes/prodshort.md)] partner or business consultant.

    -   Mark the Migrate existing data using the migration wizard option to use the Rapid Migration Tool for [!INCLUDE[prodshort](../includes/prodshort.md)]. The Rapid Migration Tool migrates QuickBooks data or Peachtree to [!INCLUDE[prodshort](../includes/prodshort.md)]. You can migrate master records, transactions, and configuration settings such as payment terms and shipping methods. Master records include customer records, vendor records, item records, and account records. Transactions include open payables transactions, open receivables transactions, open invoices transactions, and purchase orders. You also can review and edit information before you complete the migration.

To use a tool to migrate or configure data, you must download and install the Rapid Implementation Tools for [!INCLUDE[prodshort](../includes/prodshort.md)]. If you haven’t installed the Rapid Implementation Tools, click the Download and install the wizards link.

![screen to specify when to set up the company with data](media/create-company-03.png "Company Setup Options")  

20. Click Next. If you decided to configure your company later, the Additional Tasks window reappears. You can click Create a company to set up a second company, start [!INCLUDE[prodshort](../includes/prodshort.md)], or Exit.

    If you decided to migrate or configure your company data, the Rapid Migration Tool or the Rapid Configuration Tool starts.
