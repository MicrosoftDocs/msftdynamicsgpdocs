---
title: "Checklist for installation process"
description: "Quick run-through of the installation process."
keywords: "install"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 46580577-d8e4-4b25-ab9f-8538bcbb84f7
ms.reviewer: edupont
---
# Installation checklist

This section provides an overview of information you’ll need during the installation process. It contains tips on gathering information and a checklist to guide you through installing Dynamics GP. Next to each step is a reference to where you can find more detailed information.

## Dynamics GP checklist

Use this checklist as your guide to installing and setting up Dynamics GP

| Step | For more information,see |
|------|--------------------------|
| 1. Plan the security of your system.  | Download the SecurityPlanning.pdf, titled Planning for Security, from the following location: <https://www.microsoft.com/en-us/download/details.aspx?id=45025> by expanding the Details option.                     |
| 2. Refer to the Documentation and resources web site for new or updated information relating to the installation. You also can use CustomerSource for additional information. | <https://go.microsoft.com/fwlink/?LinkId=249465> |
| 3. View the Readme file and make a note of the items that pertain to you. | \\Media\\GreatPlains\\Documentation\\GPReadme.chm |
| 4. Obtain your need registration keys for Dynamics GP2018.   | Contact your Dynamics GP partner before going to CustomerSource/My Account for registration keys for Dynamics GP2018. <https://mbs.microsoft.com/customersource>  My Account  |
| 5. Verify system requirements. | [System Requirements](system-requirements.md)   |
| 6. Install a networking protocol.    | TCP/IP on page 15   |
| 7. Install and set up Microsoft SQL Server.    | Note: Make sure that you install Microsoft SharePoint if you want to use SharePoint Integrated Mode when deploying SQL Server Reporting Services reports. |
| 8. Configure SQL Server Reporting Services.  | This step is required if you didn’t configure SQL Server Reporting Services 2012 in Native mode when installing SQL Server and you want to deploy SQL Server Reporting Services reports for Dynamics GP. If you installed SQL Server Reporting Services 2012 in SharePoint Integrated mode, use the SharePoint Central Administration to complete the configuration.     |
| 9. Design the account framework.  | [Account framework](account-framework.md) |
| 10. Install Dynamics GP Tenant Services. | This step is required if you want to host Dynamics GP for multiple, unrelated organizations. Tenant Services Installation and Administration Guide  |
| 11. Install the data server and initial client.  | [Install Dynamics GP on the first computer](install-microsoft-dynamics-gp-on-the-first-computer.md)
|
| 12. Be sure to download and install the latest Dynamics GP2018 update.     | <https://mbs.microsoft.com/customersource/northamerica/gp/downloads>    |
| 13. Set up the account framework and Dynamics GP system data tables.  | Preparing Dynamics GP for use with custom settings on page 41 |
| 14. Create your first company. | Adding a company using Dynamics GP Utilities on page 63      |
| 15. Install additional components.  | Installing an additional component on page 61  |
| 16. Set up your company. | System Setup instructions (Help &gt;&gt; Contents &gt;&gt; select Setting up the system)  |
| 17. Install Dynamics GP applications on clients.    | Creating an installation package on page 76  Installing [!INCLUDE[prodshort]/includes/prodshort.md)] on an additional computer on page 79  Synchronizing a client’s account framework on page 81  Installing an additional component on page 61       |
| 18. Identify the sources of any errors. | Knowledge Base on CustomerSource  |

## Reviewing the Readme file

To view additional information that was not available when this manual was written, use the Readme file on the Dynamics GP media. Be sure to review the Readme file (GPReadme.chm) before installing Dynamics GP. You can view the Readme by double-clicking the file in \\Media\\GreatPlains

\\Documentation\\GPReadme.chm.

## Troubleshooting resources

To obtain access to information when you encounter a problem, you can use the following troubleshooting resources.

### Documentation and resources on the web

Opens a Web page that provides links to a variety of Web-based user assistance resources. Access to some items requires registration for a paid support plan.

### Dynamics GP documentation

If you’ve installed Dynamics GP, you can use help to access context- sensitive assistance about windows. You can choose Help &gt;&gt; About This Window or press F1 to access help for the window you’re currently viewing. Use the Search tab to find more information about alert messages and procedures.

You can choose Help &gt;&gt; Printable Manuals to find a printable version of procedural or overview information for specific modules.

To view and download documentation, visit the Documentation Resources for Dynamics GP2018 Web site (<https://go.microsoft.com/fwlink/?LinkId=249465> .)

### CustomerSource

CustomerSource is a Web site for registered Dynamics GP customers. CustomerSource is available 24 hours a day. You must have a user name and password to enter the site. You can access CustomerSource by navigating to <https://mbs.microsoft.com/customersource> with your Internet browser.

From the CustomerSource start page, select the Support option. From the Support page, you can look for information on your own or you can use e-mail to send a question to the Dynamics GP Technical Support team.

You’ll find links to Support Hot Topics and Knowledge Base—the best source of information for error messages, troubleshooting guides, work-arounds, and answers to common Report Writer questions. You’ll also find links for automated fixes, hardware compatibility, and downloads. Use the New Support Request link to contact Dynamics GP Technical Support electronically. You also can view recent support requests for yourself and your company.

### Microsoft SQL Server troubleshooting resources

SQL Server Books Online is a documentation resource installed with Microsoft SQL Server. Use Books Online to troubleshoot SQL error messages and other issues related to SQL. Microsoft’s web site, www.microsoft.com, is also a good source of information for issues related to SQL or your operating system. You also can download Microsoft SQL Server Management Studio and SQL Server Books Online for Microsoft SQL Server Express Edition.

![displays a lightbulb to indication tips and tricks](media/lightbulb.png "Lightbulb symbol")SQL-related error messages appear as DBMS errors in Dynamics GP. Always use the SQL Server Books Online to troubleshoot DBMS errors. Choose the Search tab and enter the error number, then choose List Topics.  

## Before you call support

If you are experiencing a problem when installing Dynamics GP, have the answers ready to the following questions to help your support specialist narrow down the source of the problem you’ve experiencing.

-   What is the exact error message?

-   When did the error first occur?

-   What task were you attempting to perform at the time the error message was displayed?

-   Has the task been completed successfully in the past?

-   What is the name of the window you are you working in?

-   What have you done so far to attempt to fix the problem?

-   If you are using more than one company, does the problem occur in another company?

-   Does the problem occur on another workstation?

-   What versions of software are you using?

Verify the version numbers for Dynamics GP, your Microsoft SQL Server, and Microsoft Windows. Also note updates applied to each product.

-   Are you using an integrating product with Dynamics GP?

-   Does the problem occur for the sa or system administrator user?

-   Does the problem occur at the database server?

-   If you use Windows Server 2008 Terminal Server, or Remote Desktop Services, does the same issue happen at the Terminal Server?


