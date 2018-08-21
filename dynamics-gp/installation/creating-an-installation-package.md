### 

# Creating an installation package

Instead of physically going to each client computer to install Microsoft Dynamics GP, you can use an installation package to install Microsoft Dynamics GP on multiple client computers. An installation package stores the files required to install a custom configured installation in a shared network location you set up. How Microsoft Dynamics GP is installed on the client computer using the installation package depends on the tools and applications you use.

This chapter contains the following sections:

-   [Installation package overview](#installation-package-overview)  

-   [Creating an installation package](#creating-an-installation-package-1)  

## Installation package overview

You can use a client installation package to install Microsoft Dynamics GP on additional client computers without having to physically go to each client computer and use the Microsoft Dynamics GP installation wizard. When you create an installation package, the installation package stores the files required to install a custom configured Microsoft Dynamics GP installation.

We recommend that you install the following components on each client computer. You can install these components from the Microsoft Dynamics GP 2018 media.

-   Microsoft Windows Installer 4.5

-   Microsoft .NET Framework 3.5

-   Microsoft .NET Framework 4.6

-   Microsoft SQL Server Native Client 11.0

-   Microsoft Dexterity Shared Components 18.0

-   Microsoft Application Error Reporting 11.0

-   Microsoft Lync 2010 SDK Runtime

-   Open XML SDK 2.0 for Microsoft Office

-   Visual C++ 2015 Runtime Libraries

-   Visual Basic for Applications Core

These components aren’t installed for you if you set up your installation package to install Microsoft Dynamics GP using the GreatPlains.msi file. If these components are not installed on the client computer, Microsoft Dynamics GP won’t be installed. These components are installed for you if you set up your installation package to install Microsoft Dynamics GP using the Setup.exe file.

When creating the installation package, you’ll select the shared network location where the installation package will be created, select Microsoft Dynamics GP features, and enter a location where Microsoft Dynamics GP will be installed on each client computer.

The installation package must be created in a shared network location that each client computer has access to. The location where Microsoft Dynamics GP will be installed must be a valid location for each client computer.

After Microsoft Dynamics GP is installed and the user on the client has started Microsoft Dynamics GP, the user may have to include new code and use Microsoft Dynamics GP Utilities to synchronize the account framework.

After the installation package is created, it can be run from the shared network location to install the Microsoft Dynamics GP client without the user having to make install decisions. A progress window shows how the process is progressing.

How Microsoft Dynamics GP is installed on the client computer using the installation package depends on the tools and applications you use. You can send an email with a link to the installation package. The user can click the link to install Microsoft Dynamics GP. Or, you can create a deployment package using a software distribution tool such as Systems Management Server so that Microsoft Dynamics GP is automatically installed after the user logs into his or her computer.

## Creating an installation package

You can use an installation package to install Microsoft Dynamics GP on your client computers. An installation package contains all the information required to install Microsoft Dynamics GP.

To create an installation package:

1. Create a shared network location or verify that the client computers have access to a shared network location.

2. From the Microsoft Dynamics GP 2018 installation media, double-click the Setup.exe file.

3. Click Create Installation Package.

4. In the Installation Location window, enter or select the folder where the installation package will be created. It is recommended that you use an Universal Naming Convention (UNC) path or a mapped drive letter that is common across all targeted machines. The network location must be accessible from any computer that will have Microsoft Dynamics GP 2018 installed on it using the installation package.

Click Next.

5. In the Country/Region Selection window, select the primary country or region where you do business. Click Next.

6. In the Select Features window, select the features to install.

When you click a button for a feature, a pop-up menu of options appears. Refer to the table for more information about each option.

| Option                                                                         | What happens                                                                                                             |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ![Chapter 11 Creating an installation package image1](media/Chapter-11-Creating-an-installation-package-image1.PNG) Run from My computer     | The selected feature will be installed on the local hard disk. (This option installs the feature, but not sub–features.) |  
| ![Chapter 11 Creating an installation package image1](media/Chapter-11-Creating-an-installation-package-image1.PNG) Run all from My computer | Will install the feature and all of its sub–features.                                                                    |  
| ![Chapter 11 Creating an installation package image2](media/Chapter-11-Creating-an-installation-package-image2.png) Not available            | Will not install the selected feature or sub–features.                                                                   |  

We recommend that you install each Microsoft Dynamics GP feature and additional component that you are going to register on all client computers.

7. Specify the location on the client computer where you want the Microsoft Dynamics GP files installed. If you don’t enter the location, the default location is \\Program Files\\Microsoft Dynamics\\GP on the hard disk that has the operating system installed.

Be sure that the location is a valid location for every computer on which the installation package is used to install Microsoft Dynamics GP 2018.

After you have specified the installation folder, click Next.

8. To set up an ODBC data source, enter the name you assigned to the SQL Server when you installed Microsoft SQL Server. A data source name called Dynamics GP also is created using SQL Native Client. If you don’t want to set up an ODBC data source, mark the Do not create a data source option.

9. Select the system database name.

Click Next.

10. Specify the location of the Reports dictionary and the Forms dictionary. The location where dictionaries are must be a valid location for each client computer. The locations are written to the Dex.ini file. Click Next.

11. Specify the location of the OLE Notes files and Letter Wizard files. Click Next.

![Chapter 11 Creating an installation package image3](media/Chapter-11-Creating-an-installation-package-image3.png)Microsoft Dynamics GP uses the Document Attachment Management functionality instead of OLE objects.  

12. In the Install Program window, click Install.

13. The Installation Progress window appears, where you can view the status of the installation.

14. In the Create Installation Package Complete window, click Finish.

The installation package is installed in the shared network location you specified. The installation package stores the files, such as Great Plains.msi and Setup.exe, required to install a custom configured Microsoft Dynamics GP installation.

15. How Microsoft Dynamics GP is installed on the client computer using the installation package depends on the tools and applications you use. You can send an email with a link to the installation package. Or, you can create a deployment package using a software distribution tool such as Systems Management Server so that Microsoft Dynamics GP is automatically installed after the user logs into their computer.

For more information about deployment, see the Documentation and resources for Microsoft Dynamics GP 2018 Web site (<http://go.microsoft.com/fwlink/?LinkId=249465>).
