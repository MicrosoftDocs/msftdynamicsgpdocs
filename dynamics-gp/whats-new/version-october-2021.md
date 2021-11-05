---
title: "What's new in Dynamics GP in October 2021"
description: "Learn about enhancements that were added to the product in this release of Dynamics GP."
author: edupont04

ms.author: edupont
ms.reviewer: edupont
manager: annbe
ms.prod: dynamics-gp
ms.topic: article
ms.date: 10/12/2021
---

# What's New in Dynamics GP in October 2021

This page lists enhancements to Dynamics GP in the October 2021 release. The Dynamics GP October 2021 release enhances different areas of the product. 
To view additional detail for these enhancements go to the Dynamics GP Blog - https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-2021-new-feature-blog-series-schedule.

## Ease of Use

A number of updates have been made throughout the system to make it easier to use Dynamics GP.

### Scroll through Account Segments

You can now scroll through the account segments in Account Segment setup to make it easier to navigate, edit or review the segments and descriptions that are setup.  This allows you to spend less time and clicks navigating through the account segments and complete your tasks faster in this setup window.

Adding the forward and back buttons next to the number field will move between the segments within the Segment ID quickly and easily.

### Save Inquiry Sort Options

Many times a user has a specific way they like to view inquiry information.  Now you can save your choices for the inquiry windows so you don’t have to make those same changes every time you look at Inquiry. This will save the Sort By selection, descending/ascending option and the include data selections on the window.

Under the View option on the Ribbon, there is a Save Window Preferences action.  This will store the settings for the inquiry window by user so the next time you enter this same window, it will default the display the way you like it.

This save window preferences option is available in Receivables – Transaction by Customer, Transaction by Document, Sales Item.         
Payables – Transaction by Vendor, Transaction by Document.  
Bank Reconciliation – Checkbook Register, Checkbook Balance.

![image](https://user-images.githubusercontent.com/28811495/140556185-d6a33c38-eb72-4054-87f0-733cf3cdfcca.png)


### Default 1099 to Single Feed Form Type

For ease of use, often the option that defaults is the one that people use most often.  We changed the default form type to Single Feed instead of continuous.  

The goal is to reduce the number of clicks and make it easier to navigate the windows.   

### Default Email on form 1096

We have adjusted the functionality for the Payables Form 1096.  Now, the email address on the Print 1099 window will default from the Internet address information setup on the company address ID.  This email address on the window will also print on the 1096 form that is generated.          

### Sales Inquiry GoTo

In Sales Inquiry, today, the default action on the zoom for the transaction is to navigate the user to the associated Inquiry window for the document that is selected in the window.  In Dynamics GP October 2021, we have added a GoTo drop down to the Sales Documents and Sales Document Range Inquiry to allow the user to choose where to navigate to.  

This allows the user to use the Inquiry window to search and find a work transaction and then navigate to Sales Transaction Entry to continue editing or complete the transaction.  The Sales Transaction Entry window will honor the users security settings; in order to navigate to it, that user must have permissions to the window itself. 

![image](https://user-images.githubusercontent.com/28811495/140558331-4577ca6d-8681-46ec-9979-7b7f46967931.png)


## Customer Requests

Some of the enhancements added for Dynamics GP October 2021 are taken directly from customer suggestions.  These are highly voted on and discussed feature asks.

### Update Account Description from Mass Modify

A common customer request is the ability to recreate the account descriptions using the Mass Modify Chart of Accounts window.  We have added an option to the modify drop down – Update Account Description.

This option will recreate the account description for the accounts included in the update display.  It will use the associated segment descriptions and separate each segment description with a dash.   

### Save All in One viewer settings

We’ve added the functionality to save the filter and preference settings for the user when they log out of Dynamics GP and log back in.  Previously, if they logged out, those settings were discarded and the user had to set the parameters again when they enter the All In One View window.  The settings are automatically saved when the user closes Dynamics GP.   
         
 We will save the Options selections and the filter settings all at the same time. These are settings stored per user.
  
### Save US Payroll Transaction Entry Defaults

In US Payroll Transaction entry, there are transaction defaults at the header that will then default when adding additional lines in the scrolling window.  Previously, those settings weren’t saved once you closed Payroll Transaction Entry.  

In Dynamics GP October 2021 the Transaction Defaults will be saved with the batch and display the next time you enter Payroll Transaction Entry and select a batch.  This should help with entering payroll transactions and reduce the mistakes with the defaults being consistently used. 
  
### Copy/Paste US Payroll Transactions from Excel

Many people use alternate methods to track hours for employees.  Because of this, we have added the ability to paste US Payroll transactions from Microsoft Excel directly into Payroll Transaction Entry.  

A paste action item has been added to the ribbon in Payroll Transaction Entry. When you are entering a new batch you copy the transactions in Excel, then select the Paste action in Transaction Entry.  This will create the transactions in the batch.  The paste action is only available with an empty batch.  

During the paste, the system will create each line and default existing information from Payroll for fields that are not included in Excel.  A validation report will print and display any errors found prior to pasting the transactions.  If there are any validation errors, the paste process will not complete and no transactions will be added to the payroll batch.  

This will help you add transactions more quickly and accurately into Payroll Transaction Entry to complete the payroll processes.

![image](https://user-images.githubusercontent.com/28811495/140557647-cbc1fe04-d8c5-47d4-8405-2f29d98e374a.png)

  
### Mask Social Security Number on US W-2

You can optionally mask the Social Security Numbers for the employees when printing W-2’s.  This is a new checkbox on the Print W-2 Forms window that is available when you choose to print W-2 forms in the print selection box.   

When marked, the first 5 characters of the social security number will print with an X and only the last four characters will display on the W-2 
  
### SafePay - Display Employee Name from Check

SafePay is the process that creates a file that can be sent to the bank to indicate what checks were written, when they were written and who they were written to.  This enables the bank to verify any checks that are presented for payment against the business records.  

Now we include the name of the employee from the payroll check as it is stored in check history instead of Employee maintenance.
 
### Project Code Modifier

You now can update the following Project fields:  Contract Number, Contract ID, Project Number, Project ID and Cost Category ID.  

Once you select the code type, you can enter or select from the lookup an existing Old Code and then type in the New Code you want to replace it with.  This update will require you to enter a completely New Code, you cannot enter an existing code to combine two codes. 

A Code Modification report will be printed which tells you what was changed and where it was changed once you select the Update action button.

![image](https://user-images.githubusercontent.com/28811495/140557995-5193cd82-337f-4748-9b5b-810fd564d822.png)


## Extend Functionality

These features are adding functionality to existing features within Dynamics GP.  

### Summary post Accounts Receivable Cash Receipt

Previously, we added the ability to Summary Post AR Cash Receipts as an option in Company Setup. This has been well received as it takes the customer cash received and posts a summary deposit for the transactions through Bank Reconciliation to update the checkbook.  However, we’ve received requests that users want greater control over this process.  Not all batches should automatically post in summary through Bank Reconciliation.  

Now we have added an option with a drop down selection when Automatically post cash receipt deposits is marked.  This drop down will display an option for the entire batch to post in Summary or to post each individual transaction through Bank Reconciliation. The system will still automatically post the deposit in Bank Reconciliation, however by this selection, you can determine if the batch posts as a combined deposit, or if each receipt in the batch will post as a deposit in Bank Reconciliation. 

### Add Autopost for Workflow Batch Approvals

You can now automatically post Workflow Approval batches when the workflow approval is complete.  This is an option in Workflow Maintenance for the specific workflow and can be marked for General Ledger Batch Workflow, Receivables Batch Workflow and Payables Batch Workflow.  

When this is selected and the final step of the workflow is completed setting the workflow to complete status, the batch will automatically be sent to post.  Workflow history will be updated with the posting step.  
   
### Workflow Approvers Count

In Dynamics GP October 2021 we have added an option to the workflow completion policy. Now, you can set a Number of Approvers with a count instead of the existing options for only one response, majority or all must approve.  

For this completion option, when the number of approvals replied has reached this count, then the workflow step will be marked as complete and will be sent to the next step in the workflow.

![image](https://user-images.githubusercontent.com/28811495/140558166-ad711c33-7970-4a6e-9131-eae3f4dd1ca7.png)

  
### Remove Carbon Copy email in Workflow Maintenance

In workflow notifications, you can setup carbon copy emails for each of the notifications.  The difficulty was previously, you couldn’t edit those carbon copy emails.  

Now, you can delete the carbon copy emails with the delete option added to the line.  This will delete all the carbon copy emails, so you can ensure the right individuals are receiving notifications.




## See also

[System requirements](../upgrade/system-requirements.md)  
[Upgrade introduction](../upgrade/introduction.md)  
[Dynamics GP community on https://community.dynamics.com](https://community.dynamics.com/gp)  
[Dynamics GP User Group](https://www.gpug.com/home)  
