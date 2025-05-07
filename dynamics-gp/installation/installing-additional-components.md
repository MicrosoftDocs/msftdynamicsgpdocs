---
title: "Add or remove features"
description: "Customize Dynamics GP by adding or removing functionality."
keywords: "install"
author: jswymer
ms.author: jswymer
manager: annbe
applies_to: 
ms.date: 03/21/2024
ms.topic: how-to
ms.assetid: 3f1d0bb8-4967-4a30-814b-b07c5ea58959
ms.reviewer: jswymer
---

# Installing additional components

Depending on your organization's needs, you may have purchased additional features that add specialized functionality to your Dynamics GP system. A Dynamics GP feature can be a single function or a complete a range of related business and accounting tasks that use one or more modules. Several products that integrate with Dynamics GP are included on the Dynamics GP media.

## Dynamics GP features

After you've installed Dynamics GP, you may decide to purchase an additional feature or remove a feature. Some features add a single function to your Dynamics GP system while some, such as Manufacturing, allow you to complete a range of related business and accounting tasks that use one or more modules. You can use the Select Features window to install or uninstall a feature. For more information about accessing this window, see Adding or removing additional features.

You can register Dynamics GP using the Registration window (Administration &gt;&gt; Setup &gt;&gt; System &gt;&gt; Registration) after you install. For more information about registration, see [Registering Dynamics GP](/dynamics-gp/installation/after-installing#registering-dynamics-gp). All features are registered for the sample company, Fabrikam, Inc. For more information about the sample company, see [Adding sample company data](/dynamics-gp/installation/using-microsoft-dynamics-utilities#adding-sample-company-data).

The following lists shows the Dynamics GP features. The features available depends on the country or region you selected when installing Dynamics GP.

For all countries and regions:

- A4  
- Analysis Cubes Client  
- Analytical Accounting 
- Date Effective Tax Rates  
- Electronic Bank Reconcile  
- Encumbrance Management  
- Enhanced Intrastat  
- Fixed Asset Management  
- Grant Management  
- Manufacturing  
- Multilingual Checks  
- Payment Document Management  
- Professional Services Tools Library  
- Project Accounting  
- Revenue/Expense Deferrals  
- Safe Pay  
- Service Based Architecture  
- VAT Daybook  
- Web Client Runtime  

For all countries and regions except Canada and the United States:

- Bank Management  
- Direct Debit Refunds  
- Scheduled Installments  

For the United States:
- Human Resources and Payroll suite  

For Belgium and France:
- Export Financial Data  

> [!NOTE]
> We recommend that you install each Dynamics GP feature and additional component that you are going to register on all client computers.

## Adding or removing additional features

Use the installation wizard to add or remove features from your Dynamics GP installation. You also can use the Program Maintenance window, opened from the Add or Remove Programs control panel, to add or remove features. You should make a complete backup of your data before adding or removing features. Removing a feature does not remove tables from the database.

Be sure to follow the instructions in the Dynamics GP Utilities windows after installing a feature. Depending on the feature that you're installing, you may have to update tables and update your companies.

After you install a feature, be sure that the feature is at the current version. You can't log in to Dynamics GP on a client computer if a product installed on the client has different version information than the server. You can use the GP\_LoginErrors. file in your temporary directory to help resolve the version information issue. The log file will contain the product name, along with the dictionary version and the database version.

To add or remove additional features:

1. Start the installation wizard. You can use either of the following methods.

- From the Dynamics GP installation media, double-click the Setup.exe file to open the Dynamics GP installation window. Select the existing instance of Dynamics GP in the Instance Selection window and click Next.

—or—

- Open the Control Panel &gt; Programs and Features or Uninstall a program Select Dynamics GP. Click Change to open the Program Maintenance window.

![login screen for service based architecture service](media/service-based-architecture-login.png "Login screen")  

2. Click Add/Remove Features.

3. In the Select Features window, select the features to install or uninstall. When you install a new feature, you won't reinstall features that have been installed previously.

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

| Option   | What happens |
|----------|-------------|
| :::image type="icon" source="media/installed-component.png"::: Run from My computer | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |  
| :::image type="icon" source="media/installed-component.png"::: Run all from My computer | Will install the feature and all of its sub–features. |  
| :::image type="icon" source="media/not-installed-component.png"::: Not available | Will not install the selected feature or sub–features. |  

After you have specified the feature or features, click Next.

4. In the Install Program window, click Install.

5. The Installation Progress window appears, where you can view the status of the installation.

6. In the Installation Complete window, click Exit.

7. Start Dynamics GP Utilities. Choose Start &gt;&gt; All Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP&gt;&gt; GP Utilities.

> [!NOTE]
> To start Dynamics GP Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system's documentation for more information.  

8. The Welcome To Dynamics GP Utilities window opens when you are logged into the server you selected. Read the message and click Next.

9. Follow the instructions in the Dynamics GP Utilities windows. Depending on the feature that you're installing, you may have to update tables and update your companies.

10. After the processing is finished, the Additional Tasks window will open, where you can perform additional tasks, start Dynamics GP, or exit the installation.

## Additional components

A smaller set of additional components are separate installations available on the Dynamics GP media. These additional components are listed on the main Dynamics GP installation window for media. For more information about accessing this window, see [Installing an additional component](#installing-an-additional-component).

| Additional components    | Description    |
|------------------------|---------------------------|
| Analysis Cubes Server         | Installs Analysis Cube Server configuration wizards for SQL Server 2012, SQL Server 2014, and SQL Server 2016. |
| Dynamics GP Add-in for Microsoft Word | Installs the code necessary to enable template mapping so you can create and modify Word templates for Dynamics GP.   |
| eConnect    | A document integration tool that enables high volume, high speed programmatic integration to and from applications and the Dynamics GP back office solution.  |
| Integration Manager       | Allows you to perform a one-time data conversion from your existing system to Dynamics GP products, or to perform ongoing integrations from other applications.   |
| Tenant Service     | A service that will provide tenant and user configuration information to applications. This service is required if you are setting up Dynamics GP Web Client for multiple tenants.  |
| Web Client   | The web server components that will provide browser access to Dynamics GP.   |
| GP Web Resource Cache   | Install on each session server to improve performance by enabling web client caching. |
| Web Services Runtime     | The runtime engine that adds a Web Services interface to Dynamics GP. Install this component if you want to run integrations that access Dynamics GP data through Web Services. Several prerequisites must be met before you can install this component. Refer to the Web Services Installation and Administration Guide for more details. |
| Web Services Management Tools | Installs the Security Console and Exceptions Management Console, which you can use to administer security and exception information for Web Services for Dynamics GP. Install this component if you want to manage Web Services from a workstation separate from where the Web Services Runtime is installed.  |
| Companion Application Services   | A tool that enables you to connect your Dynamics GP application to a data source.   |
| GP PowerShell     | PowerShell cmdlets that perform various configuration tasks for a Dynamics GP web client installation.  |
| OData Services    |   |

There are some additional components that are released only on [CustomerSource](/dynamics/s-e/howto).

## Installing an additional component

Use this procedure to install an additional component after you've installed Dynamics GP. Before installing additional components, you should make a complete backup of your data.

Each additional component has its own installation instructions and documentation that you can access before you install the component. After you review the documentation you can install the component.

To install an additional component:

1. From the Dynamics GP installation media, double-click the Setup.exe file to open the Dynamics GP installation window.

2. Click the additional component you want to install and then click View Documentation.

3. After you review the documentation, install the component by clicking the additional component you want to install and then clicking Install.

4. Depending on the component you installed, you may be instructed to restart your computer.

5. When installation of the additional component is complete, you can either install another component or close the main Dynamics GP installation window.

## OData Installation and Troubleshooting Guide

1. Deploying Dynamics GP OData Service:

    - [Install Dynamics GP OData Service from the Dynamics GP Installation Media](/dynamics/s-e/gp/MDGP2018_Release_Download_378).
    - When launching the Installation Media, you see an option for ‘GP OData Service’.
    - This service creates a URL endpoint for building reports and authenticating users with the correct permissions.

1. Configuring GP Logins and Security Roles:

    - In Dynamics GP, verify that GP logins are tied to Windows AActive Directory (AD) accounts in the User Setup window.
    - Assign users to security roles beginning with OD.
    - To create custom security tasks and roles, use the SQL Objects for OData reporting purposes in the Microsoft Dynamics GP database.
    - You will see security roles that begin with OD_ for OData, which then give access to RPT security tasks that allow OData to pull the data from the GP databases.

    [If you recently upgraded and don't see those roles, you must run the scripts to add the new security objects into Dynamics GP.](https://community.dynamics.com/blogs/post/?postid=7539b330-654e-ee11-a81c-6045bd86143b)

1. Setting up OData Service and Data Sources:

    - Go to Tools > Setup > System > OData.
    - In the Reporting Tools Setup window, go to the OData tab and enter the endpoint URL in the format `https://machineName.domain.com/` (trailing slash is required).
    - In the Data Sources section, select which SQL objects you want to make available for OData reporting.
    - Use the Add Objects button to add custom tables and views. Make sure the user has security access to the objects.
    - In the Publish OData section, check the Publish button for the objects you want to publish for OData reporting.
    - Each object has its own URL, but you only need to specify the URL up to the company level. The URL pulls all objects for the company.

1. Using OData Data Feed in Excel:

    - In Excel, go to the Data tab and select Data from Other Sources > OData Data Feed.
    - In the Data Connection Wizard, enter the OData URL up to the company name.
    - Provide credentials to access the data.
    - The wizard brings up all objects tied to the URL that you can use for reporting.
    - Select the desired object(s) and use them for reporting purposes.

1. Using OData Data Feed in Power BI:

    - In the Power BI desktop app, select on Get Data > OData Feed.
    - Enter the OData URL up to the company name and provide credentials to access the data.
    - Select the desired object(s) and use them for reporting purposes.

1. Troubleshooting OData Access Issues:

    - Make sure the user's Windows account is added to the GP login and has access to OData security roles. Otherwise, they'll receive an unauthorized/forbidden message in Excel.

## See Also

[Using Microsoft Dynamics Utilities](using-microsoft-dynamics-utilities.md)
