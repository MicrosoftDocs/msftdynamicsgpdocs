<span id="_Toc498615810" class="anchor"></span>

# Insatall Microsoft Dynamics GP on subsequent computers

Use the information in this chapter to install to Microsoft Dynamics GP 2018 on each client computer. You also can use Microsoft Dynamics GP Utilities to synchronize the Microsoft Dynamics GP dictionary on each additional client with your account framework.

This chapter contains the following sections:

-   [Installing Microsoft Dynamics GP (additional computers)](#_Installing_Microsoft_Dynamics)  

-   [Synchronizing a client’s account framework](#synchronizing-a-clients-account-framework)  

## Installing Microsoft Dynamics GP (additional computers)

Use the information in this section to install a client in a multiuser system after you’ve installed Microsoft Dynamics GP 2018 on the first computer, and created company data using Microsoft Dynamics GP Utilities.

To install Microsoft Dynamics GP (additional computers):

1. From the Microsoft Dynamics GP 2018 media, double-click the Setup.exe file.

2. If one or more of the following components isn’t installed on your computer, the Microsoft Dynamics GP Bootstrapper Setup window opens and you can choose to install the missing component or components.

-   • Dexterity Shared Components 18.0

-   • Microsoft Application Error Reporting 11.0

-   • Microsoft Lync 2010 SDK Runtime

-   • Microsoft SQL Server Native Client 11.0

-   • Microsoft Windows Installer 4.5

-   • Microsoft .NET Framework 4.6

-   • Microsoft .NET Framework 3.5

-   • Open XML SDK 2.0 for Microsoft Office

-   • Visual C++ 2015 Runtime Libraries

-   • Visual Basic for Applications Core

After all the components are installed, you may need to restart your computer before continuing the installation of Microsoft Dynamics GP.

3. Click Microsoft Dynamics GP.

The installation program verifies that your system has the minimum operating system required to run Microsoft Dynamics GP. If your system does not meet requirements, the installation won’t continue.

4. Select the primary country or region where you do business in the Country/ Region Selection window. Click Next.

5. Follow the instructions in the windows to accept the software license agreement. To install Microsoft Dynamics GP, you must accept this agreement.

6. In the Select Features window, select the features to install. We recommend that you install all the features that you are registered to use on all client computers.

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

| Option                                                                         | What happens                                                                                                             |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ![component icon](media/installed-component.png "Component icon") Run from My computer     | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |  
| ![component icon](media/installed-component.png "Component icon") Run all from My computer | Will install the feature and all of its sub–features.                                                                    |  
| ![component icon](media/not-installed-component.png "Component icon") Not available            | Will not install the selected feature or sub–features.                                                                   |  

If you’ve installed a feature in a previous release, use the Select Features window to install that component. See Microsoft Dynamics GP features on page 47 for a list of Microsoft Dynamics GP features.

7. Specify the folder where the Microsoft Dynamics GP files should be installed. To select a different folder, click Browse.

After you have specified the installation folder, click Next.

8. To set up an ODBC data source, enter the name you assigned to the SQL Server when you installed Microsoft SQL Server. Click Next.

If you don’t want to set up an ODBC data source, mark the Do not create a data source option.

9. Select the system database name you are upgrading.

Click Next.

10. If you have selected to install the Service Based Architecture feature, provide the Windows account that will be used as the service account for the Service Based Architecture service.

![login screen for service based architecture service.](media/service-based-architecture-login.png "Login screen")  

The Service Based Architecture feature will create a Windows service on the computer. The Windows account provided will be the identity used for this service.

11. In the Install Program window, click Install.

The Installation Progress window appears, where you can view the status of the installation.

12. In the Installation Complete window, click Exit.

13. Before you start Microsoft Dynamics GP Utilities, check for and install the most current Microsoft Dynamics GP update for Microsoft Dynamics GP 2018. See CustomerSource ([*https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource\#GP2018*](https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource#GP2018)) for the latest update information.

14. After installing Microsoft Dynamics GP and the most recent update, you can perform the following steps.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")To start Microsoft Dynamics GP Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system's documentation for more information.  

-   Start Microsoft Dynamics GP Utilities.

-   Follow the instructions in the Microsoft Dynamics GP Utilities windows to synchronize your account framework. See Synchronizing a client’s account framework for more information about synchronizing your account framework.

-   After using Microsoft Dynamics GP Utilities, you can install additional component applications on the server computer. See Installing an additional component on page 51 for more information.

## Synchronizing a client’s account framework

Synchronize the account framework of each client where you install Microsoft Dynamics GP. Scripts and files installed previously on the server are used by Microsoft Dynamics GP Utilities to complete the client setup.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")To start Microsoft Dynamics GP Utilities, you must have appropriate user privileges. Typically, this means being part of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system's documentation for more information.  

To synchronize a client’s account framework:

1. Start Microsoft Dynamics GP Utilities.

2. In the Welcome to Microsoft Dynamics GP Utilities window, verify your server name, and enter your User ID and Password. Click OK.

![login screen to dynamics gp utilities.](media/gp-utilities-2.png "Login screen")  

3. In the Welcome to Microsoft Dynamics GP Utilities window, click Next.

The Microsoft Dynamics GP dictionary is synchronized automatically with your account framework.

4. After the account framework is synchronized, the Additional Tasks window opens. In the Additional Tasks window, you can choose to complete additional tasks, launch Microsoft Dynamics GP, or end the installation. If you select any task, choose Process; otherwise, choose Exit.

![screen with list of tasks that open setup wizards.](media/gp-utilities-15.png "Task selector")  

Repeat the client installation process for each computer you’ll use as a client or process server for Microsoft Dynamics GP.

See Chapter 6, “Company data conversion,” for more information about additional tasks using Microsoft Dynamics GP Utilities.
