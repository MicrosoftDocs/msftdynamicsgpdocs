---
title: Welcome to Microsoft Dynamics GP | Microsoft Docs
description: Microsoft Dynamics GP is a business management solution for small and mid-sized organizations that automates and streamlines business processes and helps you manage your business.
documentationcenter: ''
author: edupont04

ms.product: dynamicsgp
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: install
ms.date: 07/13/2018
ms.author: edupont

---
# Installation Checklist for Microsoft Dynamics GP
This chapter provides an overview of information you’ll need during the
installation process. It contains tips on gathering information and a checklist
to guide you through installing Microsoft Dynamics GP. Next to each step is a
reference to where you can find more detailed information.

This chapter contains the following sections:

-   [Microsoft Dynamics GP Checklist](#_Microsoft_Dynamics_GP_1)
-   [Reviewing the Readme file](#_Reviewing_the_Readme)
-   [Troubleshooting resources](#_Troubleshooting_resources)
-   [Before you call support](#_Before_you_call)

### Microsoft Dynamics GP checklist

Use this checklist as your guide to installing and setting up Microsoft Dynamics
GP.
|Step | For more information|
|-----|---------------------|
| 1. Plan the security of your system.| Download the SecurityPlanning.pdf, titled Planning for Security, from the following location: <http://www.microsoft.com/en-us/download/details.aspx?id=45025> by expanding the Details option.  |
| 2. Refer to the Documentation and resources web site for new or updated information relating to the installation. You also can use CustomerSource for additional information. | <http://go.microsoft.com/fwlink/?LinkId=249465> For the most current documentation <https://mbs.microsoft.com/customersource> Support Hot Topics or Knowledge Base|
| 3. View the Readme file and make a note of the items that pertain to you.| \\Media\\GreatPlains\\Documentation\\GPReadme.chm|
| 4. Obtain your need registration keys for Microsoft Dynamics GP2018. | Contact your Microsoft Dynamics GP partner before going to CustomerSource/My Account for registration keys for Microsoft Dynamics GP2018. <https://mbs.microsoft.com/customersource> My Account|
| 5. Verify system requirements. | <https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/MDGP2018_System_Requirements>   |
| 6. Install a networking protocol.| TCP/IP on page 15|
| 7. Install and set up Microsoft SQL Server.| Installing Microsoft SQL Server 2012 on page 18 Note: Be sure to install Microsoft SharePoint® if you want to use SharePoint Integrated Mode when deploying SQL Server Reporting Services reports.|
| 8. Configure SQL Server Reporting Services. | This step is required if you didn’t configure SQL Server Reporting Services 2012 in Native mode when installing SQL Server and you want to deploy SQL Server Reporting Services reports for Microsoft Dynamics GP. If you installed SQL Server Reporting Services 2012 in SharePoint Integrated mode, use the SharePoint Central Administration to complete the configuration. |
| 9. Design the account framework. | Chapter 5, “Account framework”|
| 10. Install Microsoft Dynamics GP Tenant Services. | This step is required if you want to host Microsoft Dynamics GP for multiple, unrelated organizations. Tenant Services Installation and Administration Guide|
| 11. Install the data server and initial client.| Installing Microsoft Dynamics GP (first computer) on page 31|
| 12. Be sure to download and install the latest Microsoft Dynamics GP2018 update.| <https://mbs.microsoft.com/customersource/northamerica/gp/downloads>              |
| 13. Set up the account framework and Microsoft Dynamics GP system data tables.| Preparing Microsoft Dynamics GP for use with custom settings on page 41|
| 14. Create your first company.| Adding a company using Microsoft Dynamics GP Utilities on page 63|
| 15. Install additional components.| Installing an additional component on page 61|
| 16. Set up your company.| System Setup instructions (Help \>\> Contents \>\> select Setting up the system)|
| 17. Install Microsoft Dynamics GP applications on clients.| Creating an installation package on page 76 Installing Microsoft Dynamics GP on an additional computer on page 79 Synchronizing a client’s account framework on page 81 Installing an additional component on page 61|
| 18. Identify the sources of any errors.| Knowledge Base on CustomerSource |

### Reviewing the Readme file

To view additional information that was not available when this manual was written, use the Readme file on the Microsoft Dynamics GP media. Be sure to review the Readme file (GPReadme.chm) before installing Microsoft Dynamics GP. You can view the Readme by double-clicking the file in \\Media\\GreatPlains\\Documentation\\GPReadme.chm.

### Troubleshooting resources

To obtain access to information when you encounter a problem, you can use the following troubleshooting resources.

#### Documentation and resources on the web

Opens a Web page that provides links to a variety of Web-based user assistance resources. Access to some items requires registration for a paid support plan.

#### Microsoft Dynamics GP documentation

If you’ve installed Microsoft Dynamics GP, you can use help to access context-sensitive assistance about windows. You can choose Help \>\> About This Window or press F1 to access help for the window you’re currently viewing. Use the
Search tab to find more information about alert messages and procedures.

You can choose Help \>\> Printable Manuals to find a printable version of procedural or overview information for specific modules.

To view and download documentation, visit the Documentation Resources for Microsoft Dynamics GP2018 Web site
(<http://go.microsoft.com/fwlink/?LinkId=249465> .)

#### CustomerSource

CustomerSource is a Web site for registered Microsoft Dynamics GP customers. CustomerSource is available 24 hours a day. You must have a user name and password to enter the site. You can access CustomerSource by navigating to <https://mbs.microsoft.com/customersource> with your Internet browser.

From the CustomerSource start page, select the Support option. From the Support page, you can look for information on your own or you can use e-mail to send a question to the Microsoft Dynamics GP Technical Support team.

You’ll find links to Support Hot Topics and Knowledge Base—the best source of information for error messages, troubleshooting guides, work-arounds, and answers to common Report Writer questions. You’ll also find links for automated fixes, hardware compatibility, and downloads. Use the New Support Request link to contact Microsoft Dynamics GP Technical Support electronically. You also can view recent support requests for yourself and your company.

#### Microsoft SQL Server troubleshooting resources

SQL Server Books Online is a documentation resource installed with Microsoft SQL Server. Use Books Online to troubleshoot SQL error messages and other issues related to SQL. Microsoft’s web site, www.microsoft.com, is also a good source of information for issues related to SQL or your operating system. You also can download Microsoft SQL Server Management Studio and SQL Server Books Online for Microsoft SQL Server Express Edition.

SQL-related error messages appear as DBMS errors in Microsoft Dynamics GP. Always use the SQL Server Books Online to troubleshoot DBMS errors. Choose the Search tab and enter the error number, then choose List Topics.

### Before you call support

If you are experiencing a problem when installing Microsoft Dynamics GP, have the answers ready to the following questions to help your support specialist narrow down the source of the problem you’ve experiencing.

-   What is the exact error message?

-   When did the error first occur?

-   What task were you attempting to perform at the time the error message was displayed?

-   Has the task been completed successfully in the past?

-   What is the name of the window you are you working in?

-   What have you done so far to attempt to fix the problem?

-   If you are using more than one company, does the problem occur in another company?

-   Does the problem occur on another workstation?

-   What versions of software are you using?

Verify the version numbers for Microsoft Dynamics GP, your Microsoft SQL Server, and Microsoft Windows. Also note updates applied to each product.

-   Are you using an integrating product with Microsoft Dynamics GP?

-   Does the problem occur for the sa or system administrator user?

-   Does the problem occur at the database server?

If you use Windows Server 2008 Terminal Server, or Remote Desktop Services, does the same issue happen at the Terminal Server?
