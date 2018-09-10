---
title: "Client installation"
description: "Get Dynamics GP on the first computer and synchronize data with the server."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 08/24/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: fa4dc1b1-bff3-453b-b5c0-0761098a23c5
ms.reviewer: 
---
<span id="_Toc498615790" class="anchor"></span>

# Install [!INCLUDE[prodshort](../includes/prodshort.md)] on tzz first computer

Use the information in this chapter to install [!INCLUDE[prodshort](../includes/prodshort.md)] 2018. This chapter contains the following sections:

-   [Installation overview](#installation-overview)  

-   [Installing [!INCLUDE[prodshort](../includes/prodshort.md)] (first computer)](#installing-microsoft-dynamics-gp-first-computer)  

## Installation overview

In a multiuser local area network environment, [!INCLUDE[prodshort](../includes/prodshort.md)] applications are typically installed on a server, and then on each client. However, [!INCLUDE[prodshort](../includes/prodshort.md)] is not required to be installed on the server. You must install the [!INCLUDE[prodshort](../includes/prodshort.md)] databases on one computer first. After the [!INCLUDE[prodshort](../includes/prodshort.md)] databases are installed on that computer, you’ll be using the [!INCLUDE[prodshort](../includes/prodshort.md)] installation media or using an installation package to install on all remaining clients. For more about creating an installation package for your clients, see Chapter 8, “Installation package.”

The program files of the previous release aren’t removed by the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 upgrade process.

## Installing [!INCLUDE[prodshort](../includes/prodshort.md)] (first computer)

Before you begin, be sure you’ve completed the preparation steps listed in Chapter 3, “Data preparation,” and Chapter 4, “System preparation.” You must be logged in to Windows as a user with system administrator privileges.

To install [!INCLUDE[prodshort](../includes/prodshort.md)] (first computer):

1. From the [!INCLUDE[prodshort](../includes/prodshort.md)] installation media, double-click the Setup.exe file to open the [!INCLUDE[prodshort](../includes/prodshort.md)] installation window.

2. If one or more of the following components isn’t installed on your computer, the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 Bootstrapper Setup window opens and you can choose to install the missing component or components.

-   Dexterity Shared Components 18.0

-   Microsoft Application Error Reporting 11.0

-   Microsoft Lync 2010 SDK Runtime

-   Microsoft SQL Server Native Client 10.0

-   Microsoft Windows Installer 4.5

-   Microsoft .NET Framework 3.5

-   Microsoft .NET Framework 4.6

-   Open XML SDK 2.0 for Microsoft Office

-   Visual C++ 2015 Runtime Libraries

-   Visual Basic for Applications Core

After all the components are installed, you may need to restart your computer before continuing the installation of [!INCLUDE[prodshort](../includes/prodshort.md)].

3. Click [!INCLUDE[prodshort](../includes/prodshort.md)].

The installation program verifies that your system has the minimum operating system required to run [!INCLUDE[prodshort](../includes/prodshort.md)]. If your system does not meet requirements, the installation will not continue.

4. Select the primary country or region where you do business in the Country/ Region Selection window. Click Next.

5. Follow the instructions in the screen to accept the software license agreement. To install [!INCLUDE[prodshort](../includes/prodshort.md)], you must accept this agreement and click Next.

6. In the Select Features window, select the features to install.

![choose the features to add or remove.](media/add-remove-features.png "Feature selector")  

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

| Option                                                              | What happens                                                                                                             |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ![component icon](media/installed-component.png "Component icon") Run from My Computer                          | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |
| ![component icon](media/installed-component.png "Component icon") Run all from My Computer                      | Will install the feature and all of its sub–features.                                                                    |
| ![component icon](media/not-installed-component.png "Component icon") Not Available | Will not install the selected feature or sub–                                                                            |  

If you’ve installed a feature in a previous release, be sure that you’ve selected to install that feature in the Select Feature window. See [[!INCLUDE[prodshort](../includes/prodshort.md)] features](#_Microsoft_Dynamics_GP_1) on page 47 for a list of [!INCLUDE[prodshort](../includes/prodshort.md)] features. You also can install additional features. You can review the DYNAMICS.SET file for a list of features you have installed.  

7. Specify a new folder where the [!INCLUDE[prodshort](../includes/prodshort.md)] files should be installed. To select a different folder, click Browse.

After you have specified the installation location, click Next.

8. In the SQL Server window, you can set up an ODBC data source in the SQL Server window by entering the name you assigned to the SQL Server when you installed Microsoft SQL Server.

If you don’t want to set up an ODBC data source, mark the Do not create a data source option.

9. Select the system database name that you are upgrading.

Click Next.

10. If you have selected to install the Service Based Architecture feature, provide the Windows account that will be used as the service account for the Service Based Architecture service.

![login screen for service based architecture service.](media/service-based-architecture-login.png "Login screen")  

The Service Based Architecture feature will create a Windows service on the computer. The Windows account provided will be the identity used for this service.

11. In the Install Program window, click Install.

12. The Installation Progress window appears, where you can view the status of the installation.

13. In the Installation Complete window, click Exit.

14. Before you start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, check for and install the most current [!INCLUDE[prodshort](../includes/prodshort.md)] update for [!INCLUDE[prodshort](../includes/prodshort.md)] 2018. See CustomerSource (<https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource#GP2018>) for the latest update information.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")To start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you must have appropriate privileges. Typically this means being prat of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control, (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system documentation for more information.  

15. After installing [!INCLUDE[prodshort](../includes/prodshort.md)] and the most recent update, you can perform the following steps.

-   Start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities.

-   Follow the instructions in the [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities windows to upgrade tables on your server, upgrade your companies, and upgrade modified forms and reports. See Chapter 6, “Company data conversion,” for more information.

-   After using [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you can install additional component applications on the server computer. See [Chapter 8, “Installation package,”](#_Installation_package) or [Installing an additional component](#_Installing_an_additional) on page 50 for more information.  


