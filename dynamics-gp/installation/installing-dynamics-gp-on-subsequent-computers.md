---
title: "Client installation"
description: "Get Dynamics GP on each user's computer and synchronize data with the server."
keywords: "install"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 7b191c03-4d6c-490e-8257-33888b08f16d
ms.reviewer: edupont
---
# Installing Dynamics GP on subsequent computers

Use the information in this chapter to install [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 on each client computer. You also use [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities to synchronize the [!INCLUDE[prodshort](../includes/prodshort.md)] dictionary on each additional client with your account framework on the server.

This chapter contains the following sections:

-   [Installation overview](#installation-overview)  

-   [Installing [!INCLUDE[prodshort](../includes/prodshort.md)] on an additional computer](#installing-microsoft-dynamics-gp-on-an-additional-computer)  

-   [Synchronizing a client’s account framework](#synchronizing-a-clients-account-framework)  

-   [Multiple instances of [!INCLUDE[prodshort](../includes/prodshort.md)]](#_Multiple_instances_of)  

## Installation overview

In a multiuser local area network environment, [!INCLUDE[prodshort](../includes/prodshort.md)] applications are typically installed on a server, and then on each client. However, [!INCLUDE[prodshort](../includes/prodshort.md)] is not required to be installed on the server. Each client will have access to data stored on the server. You can install clients using the [!INCLUDE[prodshort](../includes/prodshort.md)] media or using a client installation package. For more about creating an installation package for your clients, see Chapter 11, “Creating an installation package.”

When you install [!INCLUDE[prodshort](../includes/prodshort.md)], the Distributed Process Server (DPS) and the Distributed Process Manager (DPM) are installed automatically. You can specify which computers in your system are process servers, and which tasks will be completed on those process servers. A process server is an application that allows users to direct the processing such as posting or printing checks and maintenance procedures to another computer on the network. The Distributed Process Manager is the application that tracks activity on all clients and process servers. See your System Administrator ’s Guide (Help &gt;&gt; Contents &gt;&gt; select System administration) for more information.

## Installing [!INCLUDE[prodshort](../includes/prodshort.md)] on an additional computer

Use the information in this section to install a client in a multiuser system after you’ve installed [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 on the server or the first computer and created your first company.

To install [!INCLUDE[prodshort](../includes/prodshort.md)] on an additional computer:

1. From the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 installation media, double-click the Setup.exe file to open the [!INCLUDE[prodshort](../includes/prodshort.md)] installation window.

2. Click [!INCLUDE[prodshort](../includes/prodshort.md)].

The installation program verifies that your system has the minimum operating system required to run [!INCLUDE[prodshort](../includes/prodshort.md)]. If your system does not meet requirements, the installation will not continue.

3. Select a new [!INCLUDE[prodshort](../includes/prodshort.md)] instance and click Next

### 

If you are installing [!INCLUDE[prodshort](../includes/prodshort.md)] on a computer with an existing instance of [!INCLUDE[prodshort](../includes/prodshort.md)], select Create a new instance and enter a name for the new instance. See Multiple instances of [!INCLUDE[prodshort](../includes/prodshort.md)] on page 82 for more information.

4. In the Select a Country/Region window, select the primary country or region where you do business. Click Next.

5. Follow the instructions in the window to accept the software license agreement.

To install [!INCLUDE[prodshort](../includes/prodshort.md)], you must accept this agreement.

6. In the Select Features window, select the features to install.

| **Option**                                                                     | **What happens**                                                                                                         |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ![component icon](media/installed-component.png "Component icon") Run from My computer     | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |  
| ![component icon](media/installed-component.png "Component icon") Run all from My computer | Will install the feature and all of its sub–features.                                                                    |  
| ![component icon](media/not-installed-component.png "Component icon") Not available            | Will not install the selected feature or sub–features.                                                                   |  

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

7. Specify the folder where you want the [!INCLUDE[prodshort](../includes/prodshort.md)] files installed. The default folder is C:\\Program Files\\Microsoft Dynamics\\GP. To select a different folder, click Browse.

After you have specified the installation folder, click Next.

8. To set up an ODBC data source, enter the name you assigned to the SQL Server when you installed Microsoft SQL Server. A data source name called Dynamics GP also is created using SQL Native Client. If you don’t want to set up an ODBC data source, mark the Do not create a data source option.

9. Select the system database name. If you selected Enter custom name, enter the system database name.

Click Next.

10. If you have selected to install the Service Based Architecture feature, provide the Windows account that will be used as the service account for the Service Based Architecture service.

The Service Based Architecture feature will create a Windows service on the computer. The Windows account provided will be the identity used for this service.

11. In the Install Program window, click Install.

12. The Installation Progress window appears, where you can view the status of the installation.

13. In the Installation Complete window, click Finish.

14. Before you start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, check for and install current update for [!INCLUDE[prodshort](../includes/prodshort.md)] 2018. See CustomerSource (<http://go.microsoft.com/fwlink/?LinkId=249465>) for the latest update information.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")To start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system’s documentation for more information.  

15. Start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities. Choose Start &gt;&gt; All Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities.

16. Follow the instructions in the [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities windows to synchronize your account framework. See Synchronizing a client’s account framework on page 81 for more information.

17. After using [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you can install additional component applications. See Chapter 8, “Installing additional components,” for more information.

## Synchronizing a client’s account framework

Synchronize the account framework of each client where you install [!INCLUDE[prodshort](../includes/prodshort.md)].

[!INCLUDE[prodshort](../includes/prodshort.md)] Utilities uses the scripts and files installed previously to complete the client setup. In addition, you can use [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities to complete various maintenance procedures, now and on an ongoing basis.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")To start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system’s documentation for more information.  

To synchronize a client’s account framework:

1. Start [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities.
(Start &gt;&gt; Programs &gt;&gt; Microsoft Dynamics &gt;&gt; GP 2018 &gt;&gt; GP Utilities)

2. In the Welcome to [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities window, verify your server name, and enter a user ID and password. Click Next.

![login screen to dynamics gp utilities](media/gp-utilities-2.png "Login screen")  

3. In the Welcome To [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities window, click Next.

The [!INCLUDE[prodshort](../includes/prodshort.md)] dictionary is synchronized automatically with your account framework.

4. In the Additional Tasks window, you can choose to complete additional tasks, launch [!INCLUDE[prodshort](../includes/prodshort.md)], or end the installation. If you select any task, choose Process; otherwise, click Exit.

![screen with list of tasks that open setup wizards](media/gp-utilities-15.png "Task selector")  

5. Repeat the client installation process for each computer you’ll use as a client or process server for [!INCLUDE[prodshort](../includes/prodshort.md)].

<span id="_Multiple_instances_of" class="anchor"></span>

## Multiple instances of [!INCLUDE[prodshort](../includes/prodshort.md)]

You can have multiple instances—installations—of [!INCLUDE[prodshort](../includes/prodshort.md)] on the same computer. Multiple instances are typically installed on client computers. You may want to use an additional instance of [!INCLUDE[prodshort](../includes/prodshort.md)] for testing purposes.

When you install [!INCLUDE[prodshort](../includes/prodshort.md)] on a computer with an existing instance of [!INCLUDE[prodshort](../includes/prodshort.md)], you’ll enter a name for the new instance during the installation process. Each instance will be displayed in the Add or Remove Programs control panel. For example, if you entered TEST as an instance name, [!INCLUDE[prodshort](../includes/prodshort.md)] (TEST) will be displayed in the Add or Remove Programs control panel. The instance also will appear in the program group for Microsoft Dynamics and in the folder where Microsoft Dynamics is installed. The default folder location is C:\\Program Files\\Microsoft Dynamics\\GP$TEST. The first instance of [!INCLUDE[prodshort](../includes/prodshort.md)] on a computer is considered the default instance. The default instance of [!INCLUDE[prodshort](../includes/prodshort.md)] isn’t assigned an instance name.
