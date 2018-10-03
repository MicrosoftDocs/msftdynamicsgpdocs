---
title: "Add or remove features"
description: "Customize Dynamics GP by adding or removing functionality."
keywords: "install"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 3f1d0bb8-4967-4a30-814b-b07c5ea58959
ms.reviewer: edupont
---
### 

# Installing additional components

Depending on your organization’s needs, you may have purchased additional features that add specialized functionality to your [!INCLUDE[prodshort](../includes/prodshort.md)] system. A [!INCLUDE[prodshort](../includes/prodshort.md)] feature can be a single function or a complete a range of related business and accounting tasks that use one or more modules. Several products that integrate with [!INCLUDE[prodshort](../includes/prodshort.md)] are included on the [!INCLUDE[prodshort](../includes/prodshort.md)] media.

This chapter contains the following sections:

-   [[!INCLUDE[prodshort](../includes/prodshort.md)] features](#_Microsoft_Dynamics_GP)  

-   [Adding or removing additional features](#adding-or-removing-additional-features)  

-   [Additional components](#additional-components)  

-   [Installing an additional component](#installing-an-additional-component)  

## [!INCLUDE[prodshort](../includes/prodshort.md)] features

After you’ve installed [!INCLUDE[prodshort](../includes/prodshort.md)] 2018, you may decide to purchase an additional feature or remove a feature. Some features add a single function to your [!INCLUDE[prodshort](../includes/prodshort.md)] system while some, such as Manufacturing, allow you to complete a range of related business and accounting tasks that use one or more modules. You can use the Select Features window to install or uninstall a feature. For more information about accessing this window, see Adding or removing additional features.

You can register [!INCLUDE[prodshort](../includes/prodshort.md)] using the Registration window (Administration &gt;&gt; Setup &gt;&gt; System &gt;&gt; Registration) after you install. For more information about registration, see Registering [!INCLUDE[prodshort](../includes/prodshort.md)] on page 70. All features are registered for the sample company, Fabrikam, Inc. For more information about the sample company, see Adding sample company data on page 49.

The following table lists the [!INCLUDE[prodshort](../includes/prodshort.md)] features. The features available depends on the country or region you selected when installing [!INCLUDE[prodshort](../includes/prodshort.md)].

The following table lists the [!INCLUDE[prodshort](../includes/prodshort.md)] features. The features available depends on the country or region you selected when installing [!INCLUDE[prodshort](../includes/prodshort.md)].

For all countries and regions:
|                      |                       |
|----------------------|-----------------------|
| A4                        | Manufacturing                       |
| Analysis Cubes Client     | Multilingual Checks                 |
| Analytical Accounting     | Payment Document Management         |
| Date Effective Tax Rates  | Professional Services Tools Library |
| Electronic Bank Reconcile | Project Accounting                  |
| Encumbrance Management    | Revenue/Expense Deferrals           |
| Enhanced Intrastat        | Safe Pay                            |
| Fixed Asset Management    | Service Based Architecture          |
| Grant Management          | VAT Daybook                         |
| Web Client Runtime        |                                     |

For all countries and regions except Canada and the United States:
|                                                                      |                       |
|---------------------------------------------------------------------------------------|-----------------------|

| Bank Management      | Scheduled Installments |

| Direct Debit Refunds |                       |

For the United States:

|                                   |     |
|-----------------------------------|-----|
| Human Resources and Payroll suite |     |

For Belgium and France:

|                       |     |
|-----------------------|-----|
| Export Financial Data |     |

### We recommend that you install each [!INCLUDE[prodshort](../includes/prodshort.md)] feature and additional component that you are going to register on all client computers.

## Adding or removing additional features

Use the installation wizard to add or remove features from your [!INCLUDE[prodshort](../includes/prodshort.md)] installation. You also can use the Program Maintenance window, opened from the Add or Remove Programs control panel, to add or remove features. You should make a complete backup of your data before adding or removing features. Removing a feature does not remove tables from the database.

Be sure to follow the instructions in the [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities windows after installing a feature. Depending on the feature that you’re installing, you may have to update tables and update your companies.

After you install a feature, be sure that the feature is at the current version. You can’t log in to [!INCLUDE[prodshort](../includes/prodshort.md)] on a client computer if a product installed on the client has different version information than the server. You can use the GP\_LoginErrors. file in your temporary directory to help resolve the version information issue. The log file will contain the product name, along with the dictionary version and the database version.

To add or remove additional features:

1. Start the installation wizard. You can use either of the following methods.

-   From the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 installation media, double-click the Setup.exe file to open the [!INCLUDE[prodshort](../includes/prodshort.md)] installation window. Select the existing instance of [!INCLUDE[prodshort](../includes/prodshort.md)] in the Instance Selection window and click Next.

—or—

-   Open the Control Panel &gt; Programs and Features or Uninstall a program Select [!INCLUDE[prodshort](../includes/prodshort.md)] 2018. Click Change to open the Program Maintenance window.

![login screen for service based architecture service](media/service-based-architecture-login.png "Login screen")  

2. Click Add/Remove Features.

3. In the Select Features window, select the features to install or uninstall. When you install a new feature, you won’t reinstall features that have been installed previously.

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

| Option                                                                         | What happens                                                                                                             |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ![component icon](media/installed-component.png "Component icon") Run from My computer     | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |  
| ![component icon](media/installed-component.png "Component icon") Run all from My computer | Will install the feature and all of its sub–features.                                                                    |  
| ![component icon](media/not-installed-component.png "Component icon") Not available            | Will not install the selected feature or sub–features.                                                                   |  

After you have specified the feature or features, click Next.

4. In the Install Program window, click Install.

5. The Installation Progress window appears, where you can view the status of the installation.

6. In the Installation Complete window, click Exit.

7. Start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities. Choose Start &gt;&gt; All Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")To start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system’s documentation for more information.  

8. The Welcome To [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities window opens when you are logged into the server you selected. Read the message and click Next.

9. Follow the instructions in the [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities windows. Depending on the feature that you’re installing, you may have to update tables and update your companies.

10. After the processing is finished, the Additional Tasks window will open, where you can perform additional tasks, start [!INCLUDE[prodshort](../includes/prodshort.md)], or exit the installation.

## Additional components

A smaller set of additional components are separate installations available on the [!INCLUDE[prodshort](../includes/prodshort.md)] media. These additional components are listed on the main [!INCLUDE[prodshort](../includes/prodshort.md)] installation window for media. For more information about accessing this window, see Installing an additional component on page 61.

| Additional components                           | Description                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analysis Cubes Server                           | Installs Analysis Cube Server configuration wizards for SQL Server 2012, SQL Server 2014, and SQL Server 2016.                                                                                                                                                                                                                                                 |
| [!INCLUDE[prodshort](../includes/prodshort.md)] Add-in for Microsoft Word | Installs the code necessary to enable template mapping so you can create and modify Word templates for [!INCLUDE[prodshort](../includes/prodshort.md)].                                                                                                                                                                                                                                  |
| eConnect                                        | A document integration tool that enables high volume, high speed programmatic integration to and from applications and the [!INCLUDE[prodshort](../includes/prodshort.md)] back office solution.                                                                                                                                                                                         |
| Integration Manager                             | Allows you to perform a one-time data conversion from your existing system to [!INCLUDE[prodshort](../includes/prodshort.md)] products, or to perform ongoing integrations from other applications.                                                                                                                                                                                      |
| Tenant Service                                  | A service that will provide tenant and user configuration information to applications. This service is required if you are setting up [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client for multiple tenants.                                                                                                                                                                   |
| Web Client                                      | The web server components that will provide browser access to [!INCLUDE[prodshort](../includes/prodshort.md)].                                                                                                                                                                                                                                                                           |
| GP Web Resource Cache                           | Install on each session server to improve performance by enabling web client caching.                                                                                                                                                                                                                                                                          |
| Web Services Runtime                            | The runtime engine that adds a Web Services interface to [!INCLUDE[prodshort](../includes/prodshort.md)]. Install this component if you want to run integrations that access [!INCLUDE[prodshort](../includes/prodshort.md)] data through Web Services. Several prerequisites must be met before you can install this component. Refer to the Web Services Installation and Administration Guide for more details. |
| Web Services Management Tools                   | Installs the Security Console and Exceptions Management Console, which you can use to administer security and exception information for Web Services for [!INCLUDE[prodshort](../includes/prodshort.md)]. Install this component if you want to manage Web Services from a workstation separate from where the Web Services Runtime is installed.                                        |
| Companion Application Services                  | A tool that enables you to connect your [!INCLUDE[prodshort](../includes/prodshort.md)] application to a data source.                                                                                                                                                                                                                                                                    |
| GP PowerShell                                   | PowerShell cmdlets that perform various configuration tasks for a [!INCLUDE[prodshort](../includes/prodshort.md)] web client installation.                                                                                                                                                                                                                                               |
| OData Services                                  |                                                                                                                                                                                                                                                                                                                                                                |

There are some additional components that are released only on the CustomerSource Web site (<https://mbs.microsoft.com/customersource/support/downloads/servicepacks/>).

## Installing an additional component

Use this procedure to install an additional component after you’ve installed [!INCLUDE[prodshort](../includes/prodshort.md)]. Before installing additional components, you should make a complete backup of your data.

Each additional component has its own installation instructions and documentation that you can access before you install the component. After you review the documentation you can install the component.

To install an additional component:

1. From the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 installation media, double-click the Setup.exe file to open the [!INCLUDE[prodshort](../includes/prodshort.md)] installation window.

2. Click the additional component you want to install and then click View Documentation.

3. After you review the documentation, install the component by clicking the additional component you want to install and then clicking Install.

4. Depending on the component you installed, you may be instructed to restart your computer.

5. When installation of the additional component is complete, you can either install another component or close the main [!INCLUDE[prodshort](../includes/prodshort.md)] installation window.
