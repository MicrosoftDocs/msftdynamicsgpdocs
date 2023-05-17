---
title: "After the upgrade"
description: "Complete the upgrade to Dynamics GP by taking a backup, reconciling financial data, applying security roles, and other important steps."
keywords: "upgrade"
author: jswymer
ms.author: jswymer
manager: jswymer
applies_to: 
ms.date: 08/24/2018
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 15929702-4de8-48c9-9c72-d280553a4676
ms.reviewer: 
---

# After you upgrade

We recommend that you complete the steps in this chapter after you upgrade all Dynamics GP databases. After you’ve completed these steps, see [Module upgrades from Dynamics GP 2013](module-upgrades-from-microsoft-dynamics-gp-2013.md) to complete additional procedures that are necessary after you’ve upgraded Dynamics GP and your company data to the latest version of Dynamics GP.

## Backups

You should make at least one complete backup of your system database and each company database after upgrading to Dynamics GP.

## Reconciling financial data

Use the Reconcile Financial Information window to reset the summary amounts for each year.

To reconcile financial data:

1. Open the Reconcile Financial Information window. (Financial &gt;&gt; Utilities &gt;&gt; Financial &gt;&gt; Reconcile)

2. Select a year to reconcile.

3. Choose Reconcile.

4. Repeat steps 2 and 3 until all the years in General Ledger have been reconciled.

## Checking links for currency tables

Use the Check Links window to check relationships among tables to find information that may be missing from one table within the relationship. You must check links for the Multicurrency Setup table even if you are not registered for Multicurrency Management.

To check links for currency tables:

1. Open the Check Links window.
(Dynamics GP menu &gt;&gt; Maintenance &gt;&gt; Check Links)

2. In the Series list, be sure that Financial is displayed.

3. In the Logical Tables list, select Multicurrency Setup and choose Insert to insert it into the Selected Tables list.

4. Choose OK to check links.

## Discontinuing the DexSQL.log

You should discontinue using the DexSQL.log file after the upgrade process. The DexSQL.log is a helpful tool that captures SQL operations and can provide information if there are issues during the upgrade process.

To discontinue the DexSQL.log:

1. Open the Dex.ini file in the Data folder of the Dynamics GP folder.

2. Change the following statements to FALSE.

    SQLLogSQLStmt=TRUE

    SQLLogODBCMessages=TRUE

    SQLLogAllODBCMessages=TRUE

3. Save your changes.

## Reports you should print after upgrading

After you upgrade, we recommend printing the following reports to a printer or to a file. You can use them to verify that your system was upgraded properly, or to re-create modifications.

| Module                    | Reports                                                                                                         |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| System                    | Shortcut Bar                                                                                                    |
| General Ledger            | Detailed Trial Balance                                                                                          |
| Receivables Management    | Aged Trial Balance with Option                                                                                  |
| Payables Management       | Aged Trial Balance with Option                                                                                  |
| Inventory Control         | Pricing Reports                                           |
|          |Error Reports|
|          |Purchase Receipts|
| Purchase Order Processing | Purchase orders|
 |          | Purchase Order Status Report                                                                                     |
| Payroll                   | Manual Check Edit|
|          |List Benefit Summary Deduction Summary|
 |          | Department Wage Summary|
|          |  FUTA Summary |
|          |Local Tax Summary |
|          |Payroll Summary |
|          |Pay Code Summary |
|          |Position Summary |
|          |State Tax Summary|
|          | SUTA Summary  |
|          | Workers’ Compensation Summary|
 |          | Form 941|  
 |          |  Form 941 Schedule B |
|          | Employee Pay History\* | 
|          | Transaction History Report\*|
|          |  Check History\*                       |
| Manufacturing             | WIP Report |
  |          | Manufacturing Order Summary|
 |          | Standard Cost Pending                                                                                           |

Print this report only if you’re keeping history.

## Removing the previous release

You should remove the previous release from your computer by using your operating system’s Add/Remove Programs utility. This includes the reports dictionary and program files for integrating products from the previous release. After removing the release, use Windows Explorer to find and delete the folder where the release was installed.

To remove Dynamics GP, use your operating system’s Add/Remove Programs utility, and select Dynamics GP.

## Security for Dynamics GP

Refer to the Planning for Security document (Help &gt;&gt; Printable Manuals &gt;&gt; select Planning for Security) or to the System Setup Guide (Help &gt;&gt; Contents &gt;&gt; select Setting up the System) for more information about security.

New users, by default, will not have access to any Dynamics GP data. You can use the default security roles and tasks that are available, or you can create your own security roles and tasks to fit your company.

### Create security tasks

For new users, you must create security tasks for Workflow, purchase requisitions, Payroll timecards, and Project timesheets. You can use the Security Task Setup window to create those tasks. As a guide for the new tasks, review the following tasks that are created for new Dynamics GP installations.

| Field                          | Entry                                                                                                                                     |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Task ID                        | ADMIN\_COMPANY\_013\*                                                                                                                     |
| Task Name                      | Set up and maintain Workflow                                                                                                              |
| Description                    | Set up Workflow access, calendars, and workflow definitions.                                                                              |
| Category                       | Company                                                                                                                                   |
| Product                        | Dynamics GP                                                                                                                     |
| Type                           | Windows                                                                                                                                   |
| Series                         | Company                                                                                                                                   |
| Select the following resources | Copy workflow                                                                                                                             |
|                                | Workflow Email Notification Maintenance                                                                                                   |
|                                | Workflow Maintenance                                                                                                                      |
|                                | Workflow User Selection                                                                                                                   |
|                                | Workflow Calendar                                                                                                                         |
|                                | Workflow Condition Editor                                                                                                                 |
| Description                    | View purchase requisition documents and purchase requisition items. Also includes the Purchase Requisition Transactions list and preview. |
| Category                       | Purchasing                                                                                                                                |
| Product                        | Dynamics GP                                                                                                                     |
| Type                           | Windows                                                                                                                                   |
| Series                         | Financial                                                                                                                                 |
| Select the following resource  | PO Commitment for Document Inquiry Zoom                                                                                                   |
| Type                           | Windows                                                                                                                                   |
| Series                         | Purchasing                                                                                                                                |
| Select the following resources | Purchase Requisition Inquiry                                                                                                              |
|                                | Purchase Requisition Inquiry Zoom                                                                                                         |
|                                | Purchase Comment Inquiry Zoom                                                                                                             |
|                                | Purchase Requisitions                                                                                                                     |
|                                | Purchasing Ship To Address Inquiry                                                                                                        |
| Type                           | Windows                                                                                                                                   |
| Series                         | Company                                                                                                                                   |
| Select the following resources | Attachment Properties                                                                                                                     |
|                                | Document Attachment Inquiry                                                                                                               |
|                                | Document Attachment Status Inquiry                                                                                                        |
| Type                           | Navigation Lists                                                                                                                          |
| Series                         | Navigation Lists                                                                                                                          |
| Select the following resource  | Purchasing Requisition Transactions                                                                                                       |
| Type                           | Navigation Lists                                                                                                                          |
| Series                         | Information Pane                                                                                                                          |
| Select the following resource  | Purchasing Requisition Transactions                                                                                                       |

| Field                         | Entry                                                        |
|-------------------------------|--------------------------------------------------------------|
| Task ID                       | RPT\_PURREQ\_006\*                                           |
| Task Name                     | Approve Timecards                                            |
| Description                   | View and approve submitted timecard data. Delegate approval. |
| Category                      | Payroll                                                      |
| Product                       | Dynamics GP                                        |
| Type                          | Windows                                                      |
| Series                        | Payroll                                                      |
| Select the following resource | Timecard Entry                                               |
| Type                          | Navigation Lists                                             |
| Series                        | Navigation Lists                                             |
| Select the following resource | Timecards Pending Approval                                   |
| Type                          | Navigation Lists                                             |
| Series                        | Information Pane                                             |
| Select the following resource | Timecards Pending Approval                                   |
| Type                          | Navigation Lists                                             |
| Series                        | Customize Lists                                              |
| Select the following resource | Timecards Pending Approval                                   |

| Field                         | Entry                                             |
|-------------------------------|---------------------------------------------------|
| Task ID                       | PTE\_TIME\_ENTRY\_001\*                           |
| Task Name                     | Self-service employee project time entry          |
| Description                   | Ability to enter project time entry transactions. |
| Category                      | Project                                           |
| Product                       | Project Accounting                                |
| Type                          | Windows                                           |
| Series                        | Project                                           |
| Select the following resource | PTE Timesheet Entry                               |
|                               | PTE Inquiry Zoom Timesheet                        |
| Type                          | Navigation Lists                                  |
| Series                        | Navigation Lists                                  |
| Select the following resource | PTE Timesheets                                    |
| Type                          | Navigation Lists                                  |
| Series                        | Customize Lists                                   |
| Select the following resource | PTE Timesheets                                    |

## Create security roles

For new users, you must create the following security roles for Workflow, purchase requisitions, Payroll timecards, and Project timesheets. As a guide for the new security roles, review the following tasks that are created for new Dynamics GP installations

To create security roles:

1. Open the Security Role Setup window.
(Administration &gt;&gt; Setup &gt;&gt; System &gt;&gt; Security Roles)

2. Create the following new roles.

| Field                      | Entry                                                      |
|----------------------------|------------------------------------------------------------|
| Role ID                    | ESS PURCHASE REQUESTER\*                                   |
| Role Name                  | Purchase Requisitions PO Preview                           |
| Role Description           | Tasks include entering and reviewing purchase requisitions |
| Select the following tasks | DEFAULTUSER                                                |
|                            | ADMIN\_PURREQ\_021\*                                       |
|                            | INQ\_PURREQ\_005                                           |

| Field                      | Entry                                                    |
|----------------------------|----------------------------------------------------------|
| Role ID                    | ESS EMPLOYEE\*                                           |
| Role Name                  | Employee Self Service Employee                           |
| Role Description           | Tasks include entering payroll time and viewing reports. |
| Select the following tasks | DEFAULTUSER                                              |
|                            | EMP\_TIME\_EMPLOYEE\_001\*                               |

| Field                      | Entry                                                                           |
|----------------------------|---------------------------------------------------------------------------------|
| Role ID                    | ESS EMPLOYEE MANAGER\*                                                          |
| Role Name                  | Employee Self Service Manager                                                   |
| Role Description           | Tasks include View and approve submitted timecard data and delegating approval. |
| Select the following tasks | DEFAULTUSER                                                                     |
|                            | EMP\_TIME\_MANAGER\_001\*                                                       |

| Heading                    | Information                                     |
|----------------------------|-------------------------------------------------|
| Role ID                    | ESS PTE EMPLOYEE\*                              |
| Role Name                  | Project Time and Expense Self Service Employee  |
| Role Description           | Can enter project time and expense transactions |
| Select the following tasks | DEFAULTUSER                                     |
|                            | PADEFAULTUSER\*                                 |
|                            | PTE\_TIME\_Entry\_001\*                         |

## Security for SQL Server Reporting Services reports

After the upgrade, use Report Manager to grant access to additional reports deployed during the upgrade. You should also use the SQL Server Management Studio to assign user groups to the SQL Server database roles that correspond to the additional data connections and reports deployed during the upgrade. The user permissions assigned to the previous versions connections and reports are maintained during the upgrade process.

If you have deployed reports using the SharePoint integrated mode and have already assigned permissions to users, those same users will have access to report server items and operations immediately after you configure the integration settings between Microsoft SharePoint and a report server. You can use existing permissions to upload report definitions and other documents, view reports, create subscriptions, and manage items.

If you have not assigned permissions, assign user and group accounts to predefined SharePoint groups. You also can create new permission levels and groups or modify existing ones to vary server access permissions as specific needs arise.

You can deploy SQL Server Reporting Services reports for multiple Dynamics GP instances to a single Microsoft SQL Server Reporting Server. If you have deployed reports to a folder on a Microsoft SQL Server Reporting Server using the Native mode, you must to provide access to the folder.
