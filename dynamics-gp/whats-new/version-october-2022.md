---
title: What's new in Dynamics GP in October 2022
description: "Learn about enhancements that were added to the product in the October 2022 release of Dynamics GP."
author: theley502

ms.author: theley
ms.reviewer: edupont
manager: tfehr
ms.prod: dynamics-gp
ms.topic: article
ms.date: 5/18/2023
---

# What's New in Dynamics GP in October 2022

This page lists enhancements to Dynamics GP in the October 2022 release. The Dynamics GP October 2022 release enhances different areas of the product. 
For an overview and additional details for key enhancements, see the [Dynamics GP Blog](https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-october-2022---feature-blog-series-schedule).

## Core Features

Functionality has been added across the core modules of Microsoft Dynamics GP.

### Print Cash Receipts

A highly requested item for Dynamics GP October, we have added the ability to print a Cash Receipt document. 

This is setup as both a Report Writer report and as a Word form, so the Cash Receipt can be assigned specifically to a customer.  Then, when you enter a cash receipt transaction, you can print the form or email it directly to the customer.  

The Cash Receipt can be printed from Cash Receipts Entry or the Receivables Transaction Navigation List.

![image 1](https://user-images.githubusercontent.com/28811495/197573350-927bf6ad-9c34-4b42-98ad-c9b1a7a12b1b.png)

### Inactivate Vendor Address ID

Previously, there was no way to mark a vendor address record as not needed or do not use.  Now you can set the status of a vendor address record as Inactive.  

In Vendor Address Maintenance a report can be printed which will list all the transactions that the Vendor Address ID is used in Dynamics GP.  Once the address ID is marked inactive, a warning will be given on selection, on edit lists, on posting reports that the inactive address ID is being used.  You can continue to use the vendor address ID, but will be warned.  This will allow you to continue to pay or process any existing transactions with the vendor address ID or change them prior to posting.

![image 2](https://user-images.githubusercontent.com/28811495/197573885-2868d71c-5667-4bd9-945b-00a60cf5bc3d.png)

### 1099-NEC Form with Lines

A core feature of Microsoft Dynamics GP is the ability to print Payables 1099 statements for vendors.  Continuing that functionality, we have added a built in format with boxes and lines for the 1099-NEC form.  
Now, when you select to print the 1099-NEC form, you have the option of printing the form type one-wide with boxes. When this option is selected, the form will print on blank paper.

![image 3](https://user-images.githubusercontent.com/28811495/197574361-7c1be975-6a7a-451b-aff4-4664a64c619b.png)

###Summary Display Bank Reconciliation for Payables EFT

Now you can choose to have the system post an EFT batch in summary to Bank Reconciliation.  Once, the option is set in Payables Setup, the drop down will display for the batch in Payables Batch Entry for an EFT computer check payment.  

This will then post all the payments in the batch as one record to Bank Reconciliation.  You can zoom from the summary record to see the individual payments included.

On the upgrade, the option in Payables Setup is not marked and all batches are set to post as they do prior to the October 2022 release.  

![image 4](https://user-images.githubusercontent.com/28811495/197575872-34b63b8a-cd01-4223-a544-b9aa9679e38f.png)
 
### Summary Display Bank Reconciliation for Payables Credit Card Payment

Now you can choose to have the system post a Credit Card batch in summary to Bank Reconciliation.  Once, the option is set in Payables Setup, the drop down will display for the batch in Payables Batch Entry for a Credit Card payment.  

This will then post all the payments in the batch as one record to Bank Reconciliation.  You can zoom from the summary record to see the individual payments included. 

On the upgrade, the option in Payables Setup is not marked and all batches are set to post as they do prior to the October 2022 release.  For a Credit Card batch to enable the option, the credit card must be setup to be Used by the Company in Credit Card Setup and associated with a Checkbook ID.

![image 5](https://user-images.githubusercontent.com/28811495/197575396-326583fe-b5ac-42e7-a71b-a2f7194539c1.png)

## Customer Requests

We consistently review customer suggestions.  These are highly voted on and discussed feature asks that are included in the October 2022 Dynamics GP release.

### Checkbook Balance Inquiry Enhancements

We have enhanced the usability of the Checkbook Balance Inquiry window in Bank Reconciliation.  Previously, you selected the checkbook and the window filled in.  

Now, you complete all the heading type information on the window and then select to redisplay to filter the checkbook information.  Enter checkbook, date range, sort by options and then click redisplay. This will allow you to filter the data immediately and make it easier to find the information you are looking for.

![image 6](https://user-images.githubusercontent.com/28811495/197577077-dfb41d28-2ca1-4fd2-95af-8a112504f851.png)

### Checkbook Register Inquiry Enhancements

Similar changes have been made to the Checkbook Register Inquiry window to enhance the usability of the window.    

Now, you complete all the heading type information on the window and then select to redisplay to filter the checkbook register information.  Enter checkbook, included information, sort by options and then click redisplay. This will allow you to filter the data immediately and make it easier to find the information you are looking for.

![image 7](https://user-images.githubusercontent.com/28811495/197577524-c14836e1-ef0a-4127-8651-41a9f587106d.png)

### Account Category Lookup Enhancement

You now can change the sort for the Account Category Lookup. And you can search within the lookup itself to more quickly and easily find the Account Category you want to use. 

![image 8](https://user-images.githubusercontent.com/28811495/197577911-c4bf14fa-deef-433e-a49d-61624e5b1a71.png)

### Account Segment Lookup

Similar to the Account Category lookup, there is additional functionality for the Account Segment Lookup. You can change the sort to description for the Account Segment Number Lookup. And you can search within the lookup itself to more quickly and easily find the Account Segment number you want to use. 

![image 9](https://user-images.githubusercontent.com/28811495/197578086-ca8bf66c-a512-450b-8bc8-822e8631d27c.png)

### Journal Entry Inquiry View Workflow History

We have added the ability to view workflow history in Journal Entry Inquiry when the transaction type is a Reversing Journal Entry.  Previously if the user selected a reversing journal entry, the workflow history button was disabled.  

It will now be enabled if Workflow is being used and a reversing journal entry is selected letting the user see all the information related to the reversing entry.

![image 10 11](https://user-images.githubusercontent.com/28811495/197578348-bb9a7563-7cd6-444a-bc0e-f9699dc7938a.png)

### Transaction Level Post through GL without Printing GL Posting Journal

Previously, there was the ability to setup Payables Transaction Entry posting to Post Through GL, this required the GL Posting Journal to be marked in the Posting Setup for General Journal Entry.  With the October 2022 release of Microsoft Dynamics GP, we have removed this requirement. 

Now for both Payables Transaction Entry and Payables Manual Payment Entry, you can successfully transaction level post through General Ledger without marking the General Posting Journal.

![image](https://user-images.githubusercontent.com/28811495/197579230-965334dc-aea2-4073-9b6b-98ab4f605c5f.png)

### Reprint Bank Journals

There are now additional options available when reprinting the Bank Journals.  For the Bank Deposit Journal, Multicurrency Bank Deposit Journal, Cleared Transactions Journal and Outstanding Transactions Report you can now restrict by a range of Audit Trail to more easily identify data you want to include on the reprint report.

For the Bank Adjustments Journal and Multicurrency Bank Adjustments Journal, you can filter by both the Audit Trail Code and a Date range for the reprint journals.

![image 12](https://user-images.githubusercontent.com/28811495/197579512-4ebf4c0e-2cd6-44b5-bcfe-c61a3821dfd4.png)

### Print Bank History Reports

Now, when setting up the report options for the Bank History reports, you can use a date range restriction to further filter your reports.  This will give you the ability to find the information you are looking for quickly and easily.  The date range will print on the header of the report so you can see how you restricted the report information.  

The report option range is available for the Bank Adjustments Reprint Journal, Bank Deposit Reprint Journal, Bank Transaction History Report, Multicurrency Bank Adjustments Reprint Journal, Multicurrency Bank Deposit Reprint Journal and the Outstanding Transactions Report - Reprint.

![image 13](https://user-images.githubusercontent.com/28811495/197579777-b9feb4bf-5732-47c9-b41e-2822622b9c10.png)

### Print and Email POP and SOP Documents at the same time

The ability to e-mail a Sales or Purchasing document such as a Purchase Order and to print a copy of it at the same time has been made consistent across the system.  The Purchasing Navigation List, Sales Navigation List, Purchase Order Entry.

Now, when you select to Send in E-mail, you can mark either Print a Copy or Print Remaining for the Print Options.  Not marking either selection will only e-mail those documents that can be e-mailed.  

Marking Print a Copy will print all the documents selected for the process but will only e-mail those documents that are setup to be e-mailed.  Marking Print Remaining will e-mail the documents setup to be e-mailed and print any documents that are selected for the process but weren't setup to be e-mailed.

![image 14](https://user-images.githubusercontent.com/28811495/197580359-60eeb414-9f8d-42b8-bca9-928f33bfa17c.png)

### Workflow History Option for No Approval Needed Steps

You can choose whether to save history when a Workflow Step has no approval needed.  

This is a per workflow setting where you can mark to save or not save the no approval needed steps to Workflow History.   This option will reduce the amount of data that is saved in workflow history.  

![image 15](https://user-images.githubusercontent.com/28811495/197580542-ed35caa4-d8a3-4726-946e-7b7e6b36bff9.png)

## Extend Functionality

We also welcome feedback on existent features in Dynamics GP that we can improve. These features are adding functionality to existing features within Dynamics GP. 

### Filter Navigation Lists by Batch ID or Batch Source

Now you can choose to filter selected Navigation Lists by Batch ID or Batch Source as well as add the display to the navigation list information.  

This is available for the Account Transactions list, All Sales Transactions, Receivables Transactions, Sales Order Transactions, Invoicing Transactions, All  Purchasing Transactions, Payables Transactions, Purchase Order Transactions and Item Transactions lists.

To add the column to the navigation list, you will be able to create a saved list and add the batch ID or batch source columns when you choose to customize the saved list.

![image 16](https://user-images.githubusercontent.com/28811495/197581233-662a6d55-04f9-48c6-b682-ac13ac5be3ec.png)

### Add Time option to Report Scheduler

In the Report Scheduler functionality, you have the option to print report or to schedule checklinks.  Previously, this would run automatically on the date that was selected.  

We have extended the functionality to allow the user to set a time for the report or checklinks process to run.  This allows you to run these processes during off-peak times or overnight.  A user is logged in who has the ability to the report schedule process and the system will query every so often for a scheduled task to run.  Once the time is reached or is passed, the task will be run.

![image 17](https://user-images.githubusercontent.com/28811495/197581666-bbb7a63f-7379-417b-88a7-eff7a68d45e0.png)

### E-mail Approve Automatically Post Workflow Batches

In October 2021, we released functionality to allow the user to mark to Auto Post a batch that was approved when the Workflow for the batch was completed.  One of the requests after this release came out was that we extend the capability for the Auto Post when a Workflow task is approved from an e-mail.  

With the October 2022 Dynamics GP release, we have addressed that functionality and extended the capability to include all workflow tasks.

Now, when the Workflow task is approved from an e-mail and it completes the Workflow process, the system will create a Scheduled Task in the Report Scheduler window to automatically post the batch.  This will work for General Ledger, Accounts Receivable and Accounts Payable batches that have Workflow assigned to them.

![image 18](https://user-images.githubusercontent.com/28811495/197581878-b8dd2678-b73e-4d75-a5d6-1c530fa9daa5.png)

### MultiFactor Authentication in Dynamics GP Web Client

We have enabled Multifactor authentication in Dynamics GP Web Client. Included with this is the capability of using the reply to e-mail address when setup with MFA.
[Detailed setup for MFA in Web Client](https://community.dynamics.com/gp/b/dynamicsgp/posts/modern-authentication-in-web-client)
[Email Troublesheeting Guide](https://learn.microsoft.com/en-us/dynamics-gp/installation/email-troubleshooting-guide#mfa---multi-factor-authentication-modern-authentication)


