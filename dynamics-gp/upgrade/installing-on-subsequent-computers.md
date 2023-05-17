---
title: "CInstall the Dynamics GP client on subsequent computers"
description: "Get the Dynamics GP client on each user's computer and synchronize data with the server."
keywords: "upgrade"
author: jswymer
ms.author: jswymer
manager: jswymer
applies_to: 
ms.date: 08/24/2018
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 6f2f7511-6871-4d78-a9b9-824e479348e5
ms.reviewer: 
---

# Install the Dynamics GP client on subsequent computers

Use the information in this chapter to install to Dynamics GP on each client computer. You also can use Dynamics GP Utilities to synchronize the Dynamics GP dictionary on each additional client with your account framework.

## Installing Dynamics GP (additional computers)

Use the information in this section to install a client in a multiuser system after you've installed Dynamics GP on the first computer, and created company data using Dynamics GP Utilities.

To install Dynamics GP (additional computers):

1. From the Dynamics GP media, double-click the Setup.exe file.

2. If one or more of the following components isn't installed on your computer, the Dynamics GP Bootstrapper Setup window opens and you can choose to install the missing component or components.

    - Dexterity Shared Components 18.0

    - Microsoft Application Error Reporting 11.0

    - Microsoft Lync 2010 SDK Runtime

    - Microsoft SQL Server Native Client 11.0

    - Microsoft Windows Installer 4.5

    - Microsoft .NET Framework 4.6

    - Microsoft .NET Framework 3.5

    - Open XML SDK 2.0 for Microsoft Office

    - Visual C++ 2015 Runtime Libraries

    - Visual Basic for Applications Core

    After all the components are installed, you may need to restart your computer before continuing the installation of Dynamics GP.

3. Click Dynamics GP.

    The installation program verifies that your system has the minimum operating system required to run Dynamics GP. If your system does not meet requirements, the installation won't continue.

4. Select the primary country or region where you do business in the Country/ Region Selection window. Click Next.

5. Follow the instructions in the windows to accept the software license agreement. To install Dynamics GP, you must accept this agreement.

6. In the Select Features window, select the features to install. We recommend that you install all the features that you are registered to use on all client computers.

    When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

    | Option | What happens |
    |--|--|
    | ![component icon1](media/installed-component.png "Component icon") Run from My computer | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.)  |
    | ![component icon2](media/installed-component.png "Component icon") Run all from My computer | Will install the feature and all of its sub–features.  |
    | ![component icon3](media/not-installed-component.png "Component icon") Not available | Will not install the selected feature or sub–features.  |

    If you've installed a feature in a previous release, use the Select Features window to install that component. See [Dynamics GP features](/dynamics-gp/installation/installing-additional-components#dynamics-gp-features) for a list of Dynamics GP features.

7. Specify the folder where the Dynamics GP files should be installed. To select a different folder, click Browse.

    After you have specified the installation folder, click Next.

8. To set up an ODBC data source, enter the name you assigned to the SQL Server when you installed Microsoft SQL Server. Click Next.

    If you don't want to set up an ODBC data source, mark the Do not create a data source option.

9. Select the system database name you are upgrading.

    Click Next.

10. If you have selected to install the Service Based Architecture feature, provide the Windows account that will be used as the service account for the Service Based Architecture service.

    ![login screen for service based architecture service.](media/service-based-architecture-login.png "Login screen")  

    The Service Based Architecture feature will create a Windows service on the computer. The Windows account provided will be the identity used for this service.

11. In the Install Program window, click Install.

    The Installation Progress window appears, where you can view the status of the installation.

12. In the Installation Complete window, click Exit.

13. Before you start Dynamics GP Utilities, check for and install the most current Dynamics GP update for Dynamics GP. See [Microsoft Dynamics GP Resource Directory](../resources.md)) for the latest update information.

14. After installing Dynamics GP and the most recent update, you can perform the following steps.

> [!NOTE]
> To start Dynamics GP Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system's documentation for more information.  

- Start Dynamics GP Utilities.

- Follow the instructions in the Dynamics GP Utilities windows to synchronize your account framework. See Synchronizing a client's account framework for more information about synchronizing your account framework.

- After using Dynamics GP Utilities, you can install additional component applications on the server computer. See the **Installing an additional component** section for more information.

## Synchronizing a client's account framework

Synchronize the account framework of each client where you install Dynamics GP. Scripts and files installed previously on the server are used by Dynamics GP Utilities to complete the client setup.

> [!NOTE]
> To start Dynamics GP Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system's documentation for more information.  

To synchronize a client's account framework:

1. Start Dynamics GP Utilities.

2. In the Welcome to Dynamics GP Utilities window, verify your server name, and enter your User ID and Password. Click OK.

![login screen to dynamics gp utilities.](media/gp-utilities-2.png "Login screen")  

3. In the Welcome to Dynamics GP Utilities window, click Next.

    The Dynamics GP dictionary is synchronized automatically with your account framework.

4. After the account framework is synchronized, the Additional Tasks window opens. In the Additional Tasks window, you can choose to complete additional tasks, launch Dynamics GP, or end the installation. If you select any task, choose Process; otherwise, choose Exit.

![screen with list of tasks that open setup wizards.](media/gp-utilities-15.png "Task selector")  

Repeat the client installation process for each computer you'll use as a client or process server for Dynamics GP.

See Chapter 6, "Company data conversion," for more information about additional tasks using Dynamics GP Utilities.
