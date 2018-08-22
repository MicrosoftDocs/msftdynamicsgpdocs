<span id="_Toc498615790" class="anchor"></span>

# Install Microsoft Dynamics GP on the first computer

Use the information in this chapter to install Microsoft Dynamics GP 2018. This chapter contains the following sections:

-   [Installation overview](#installation-overview)  

-   [Installing Microsoft Dynamics GP (first computer)](#installing-microsoft-dynamics-gp-first-computer)  

## Installation overview

In a multiuser local area network environment, Microsoft Dynamics GP applications are typically installed on a server, and then on each client. However, Microsoft Dynamics GP is not required to be installed on the server. You must install the Microsoft Dynamics GP databases on one computer first. After the Microsoft Dynamics GP databases are installed on that computer, you’ll be using the Microsoft Dynamics GP installation media or using an installation package to install on all remaining clients. For more about creating an installation package for your clients, see Chapter 8, “Installation package.”

The program files of the previous release aren’t removed by the Microsoft Dynamics GP 2018 upgrade process.

## Installing Microsoft Dynamics GP (first computer)

Before you begin, be sure you’ve completed the preparation steps listed in Chapter 3, “Data preparation,” and Chapter 4, “System preparation.” You must be logged in to Windows as a user with system administrator privileges.

To install Microsoft Dynamics GP (first computer):

1. From the Microsoft Dynamics GP installation media, double-click the Setup.exe file to open the Microsoft Dynamics GP installation window.

2. If one or more of the following components isn’t installed on your computer, the Microsoft Dynamics GP 2018 Bootstrapper Setup window opens and you can choose to install the missing component or components.

-   Dexterity Shared Components 18.0

-   Microsoft Application Error Reporting 11.0

-   Microsoft Lync 2010 SDK Runtime

-   Microsoft SQL Server Native Client 10.0

-   Microsoft Windows Installer 4.5

-   Microsoft .NET Framework 3.5

-   Microsoft .NET Framework 4.6

-   Open XML SDK 2.0 for Microsoft Office

-   Visual C++ 2015 Runtime Libraries

<!-- -->

-   Visual Basic for Applications Core

After all the components are installed, you may need to restart your computer before continuing the installation of Microsoft Dynamics GP.

3. Click Microsoft Dynamics GP.

The installation program verifies that your system has the minimum operating system required to run Microsoft Dynamics GP. If your system does not meet requirements, the installation will not continue.

4. Select the primary country or region where you do business in the Country/ Region Selection window. Click Next.

5. Follow the instructions in the screen to accept the software license agreement. To install Microsoft Dynamics GP, you must accept this agreement and click Next.

6. In the Select Features window, select the features to install.

![Chapter 5 Install Microsoft Dynamics GP on the first computer image1](media/Chapter-5-Install-Microsoft-Dynamics-GP-on-the-first-computer-image1.png)  

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

| Option                                                              | What happens                                                                                                             |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ![](media/Chapter-5-Install-Microsoft-Dynamics-GP-on-the-first-computer-image2.png) Run from My Computer                          | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |
| ![](media/Chapter-5-Install-Microsoft-Dynamics-GP-on-the-first-computer-image2.png) Run all from My Computer                      | Will install the feature and all of its sub–features.                                                                    |
| ![Chapter 5 Install Microsoft Dynamics GP on the first computer image3](media/Chapter-5-Install-Microsoft-Dynamics-GP-on-the-first-computer-image3.png) Not Available | Will not install the selected feature or sub–                                                                            |  

If you’ve installed a feature in a previous release, be sure that you’ve selected to install that feature in the Select Feature window. See [Microsoft Dynamics GP features](#_Microsoft_Dynamics_GP_1) on page 47 for a list of Microsoft Dynamics GP features. You also can install additional features. You can review the DYNAMICS.SET file for a list of features you have installed.  

7. Specify a new folder where the Microsoft Dynamics GP files should be installed. To select a different folder, click Browse.

After you have specified the installation location, click Next.

8. In the SQL Server window, you can set up an ODBC data source in the SQL Server window by entering the name you assigned to the SQL Server when you installed Microsoft SQL Server.

If you don’t want to set up an ODBC data source, mark the Do not create a data source option.

9. Select the system database name that you are upgrading.

Click Next.

10. If you have selected to install the Service Based Architecture feature, provide the Windows account that will be used as the service account for the Service Based Architecture service.

![Chapter 5 Install Microsoft Dynamics GP on the first computer image4](media/Chapter-5-Install-Microsoft-Dynamics-GP-on-the-first-computer-image4.png)  

The Service Based Architecture feature will create a Windows service on the computer. The Windows account provided will be the identity used for this service.

11. In the Install Program window, click Install.

12. The Installation Progress window appears, where you can view the status of the installation.

13. In the Installation Complete window, click Exit.

14. Before you start Microsoft Dynamics GP Utilities, check for and install the most current Microsoft Dynamics GP update for Microsoft Dynamics GP 2018. See CustomerSource (<https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource#GP2018>) for the latest update information.

![Chapter 5 Install Microsoft Dynamics GP on the first computer image5](media/Chapter-5-Install-Microsoft-Dynamics-GP-on-the-first-computer-image5.png)To start Microsoft Dynamics GP Utilities, you must have appropriate privileges. Typically this means being prat of the Administrators group or the Power Users group. If you are using an operating system that has User Account Control, (UAC) enabled, you will be prompted to run the program as a user with administrative privileges. Refer to your operating system documentation for more information.  

15. After installing Microsoft Dynamics GP and the most recent update, you can perform the following steps.

-   Start Microsoft Dynamics GP Utilities.

-   Follow the instructions in the Microsoft Dynamics GP Utilities windows to upgrade tables on your server, upgrade your companies, and upgrade modified forms and reports. See Chapter 6, “Company data conversion,” for more information.

-   After using Microsoft Dynamics GP Utilities, you can install additional component applications on the server computer. See [Chapter 8, “Installation package,”](#_Installation_package) or [Installing an additional component](#_Installing_an_additional) on page 50 for more information.  


