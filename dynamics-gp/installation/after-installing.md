---
title: "Start using Dynamics GP"
description: "Get up and running with Dynamics GP."
keywords: "install"
author: jswymer
ms.author: jswymer
manager: annbe
applies_to: 
ms.date: 08/23/2018
ms.topic: how-to
ms.assetid: ec79456b-f8e6-402c-acfa-daaca48c059b
ms.reviewer: jswymer
ms.custom: sfi-image-nochange
---

# After installing Dynamics GP

Use the information in this chapter to log in to Dynamics GP for the first time and register Dynamics GP. You also may have to grant user access to alternate Dynamics GP windows and reports.

## Logging in to and quitting Dynamics GP

If you have trouble starting Dynamics GP, contact your network administrator.

To log in to Dynamics GP:

1. Choose Start &gt; Programs &gt; Microsoft Dynamics &gt; GP
The Welcome to Dynamics GP window opens.

![login screen using the sa user](media/install-dynamics-gp-setup-01.png "Login screen")  

2. Enter your user ID and password. Passwords are case-sensitive.

3. Click OK. The Company Login window appears.

![screen to choose the company to log into](media/install-dynamics-gp-setup-02.png "Login screen")  

4. Select a company and click OK. The Dynamics GP main menu appears.

    To switch to a different company while you are working in Dynamics GP, choose Dynamics GP menu &gt;&gt; User and Company.

To quit Dynamics GP:

1. Save your work in the window you are working in.

2. Choose Dynamics GP menu &gt;&gt; Exit.

## Registering Dynamics GP

By registering your software, we can provide you with better service. We can gather information about additional needs you have and how Dynamics GP can be improved. Software registration also eliminates unauthorized use of the software without imposing restrictive copy protection.

You can enter your site name and registration keys for Dynamics GP in the Registration window (Administration&gt;&gt; Setup &gt;&gt; System &gt;&gt; Registration).

You must register Dynamics GP before you can use it. Enter your site name and registration keys exactly as they appear on your registration document. If you don’t register a module before you begin to use it, you won’t be able to open any transaction entry window. Modules in the sample company, Fabrikam, Inc., are registered and you can use the sample company to practice procedures.

After you’ve registered Dynamics GP, you won’t need to register additional companies that you add. To verify that a module has been registered, open the Dynamics GP Options window (Help &gt;&gt; About Dynamics GP &gt;&gt; Options). Registered modules have a check mark in the Registered column.

## Security for Dynamics GP

The default security settings in Dynamics GP allow all users access to only the windows and forms in Dynamics GP that are needed to log in to the application. After setting up new user records, you should set access to companies and set up security for new users. To learn more about setting up security, refer to the System Setup Guide (Help &gt;&gt; Contents &gt;&gt; select Setting up the System).

Each time you install a new feature or component in Dynamics GP, such as Human Resources, you must set up security for that feature or component. For example, if you have been using Dynamics GP for a year and you just installed Human Resources, you will need to set up access to Human Resources before anyone can use it.

Refer to the Planning For Security document (C:\\Program Files\\Microsoft Dynamics\\GP\\Documentation\\SecurityPlanning.pdf) or to the System Setup Guide (Help &gt;&gt; Contents &gt;&gt; select Setting up the System) for more information about security.

## Tasks for SQL Server Reporting Services reports

Review the following tasks.

### Security

After deploying the Dynamics GP SQL Server Reporting Services reports, the only individuals who will be able to access or view the reports within the Report Manager are those users who are members of the web server ’s local administrator group and local administrators on SQL Server. The web site administrator has to implement and grant access to the Reporting Services Web site and database objects required to print reports.

If you have deployed reports using the SharePoint integrated mode and have already assigned permissions to users, those same users will have access to report server items and operations immediately after you configure the integration settings between Microsoft SharePoint and a report server. You can use existing permissions to upload report definitions and other documents, view reports, create subscriptions, and manage items.

If you have not assigned permissions, assign user and group accounts to predefined SharePoint groups. You also can create new permission levels and groups, or modify existing ones to vary server access permissions as specific needs arise.

You can deploy SQL Server Reporting Services reports for multiple Dynamics GP instances to a single Microsoft SQL Server Reporting Server. If you have deployed reports to a folder on a Microsoft SQL Server Reporting Server using the Native mode, you must to provide access to the folder.

### Microsoft Dynamics CRM

Before you render a SQL Server Reporting Services report with CRM data, be sure to start the Microsoft Dynamics CRM application to initialize data
