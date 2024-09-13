---
title: What's new in Dynamics GP in October 2024
description: Learn about enhancements that were added to the product in the October 2024 release of Dynamics GP.
author: theley502
ms.author: theley
ms.reviewer: jswymer
ms.topic: article
ms.date: 07/22/2024
---
# What's New in Dynamics GP in October 2024

This page lists enhancements to Dynamics GP in the October 2024 release. The Dynamics GP October 2024 release enhances different areas of the product.

For an overview and additional details for key enhancements, see the [Dynamics GP Blog](https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-october-2024---feature-blog-series-schedule).

## Core Features

Functionality has been added across the core modules of Microsoft Dynamics GP.

### Email RM Statement with Multicurrency Blank Form

In the October 2024 release, we have updated the Print RM Statement functionality to enable emails with forms other than the Blank Form.  Now if you select any form type, the Email Optionsand the Email ribbon action will both be enabled. Two additional statement templates are added as well; RM Statement Long form and MC Statement Long Form.

![image](https://github.com/user-attachments/assets/bdb63dae-d4e7-4e11-988e-d806e2b74d41)

### Mask ID on Payables 1099’s

There is now an option available on the Print 1099 window to mask the vendor's Tax identification number.  When you mark the checkbox and print a 1099, the Tax ID number will print with the first 5 numbers as an X.

![image](https://github.com/user-attachments/assets/7ba94724-7bde-4a09-9ce9-18f5c252d259)

![image](https://github.com/user-attachments/assets/0a46f5ba-80eb-44aa-8e50-bf74e5f480b7)

### Reprint EFT payment Register

In the Purchasing Posting Journal Options Report selection, the EFT Payment Register has been added in order to reprint the report after posting a Payables batch.  

![image](https://github.com/user-attachments/assets/f54f1bc5-ad8f-4daf-8201-615fbf5c7709)

### Print Historical Aged Trial Balance when voucher number has special characters

The Print Historical Aged Trial Balance report will show the posted information when a voucher number or a payment number is posted with special characters.

![image](https://github.com/user-attachments/assets/c8d81427-5858-44c7-9bc5-318609672bba)

### Default Vendor Class Update Option to No

If you edit a vendor record and modify the vendor class ID, now the default option when changing the vendor class ID on a vendor will be to not roll down changes.

![image](https://github.com/user-attachments/assets/1a0565b8-25ce-43db-8111-ba207e438dba)

### Restrict Edit 1099 Transaction Information by Calendar Year

With this October release, we have added changes for the edit 1099 information.  Now, there is an option in the Documents drop down for Calendar Year Paid.  When selected, there is a Year ddl to select. This will show you a filtered list of 1099 transactions that were paid in the calendar year selected.

There is a new zoom on the 1099 Details window or the 1099 Inquiry window to open the Edit 1099 transactions restricted by year.  This will allow you to find the details more quickly for transactions that were paid in a specified calendar year. In addition, there is a new reporton the Edit 1099 Transactions window to print the information you have filtered to.

![image](https://github.com/user-attachments/assets/14e383b2-63df-4b1e-b10b-151ab61816c9)

![image](https://github.com/user-attachments/assets/41ea035b-8d77-43e4-886d-daac789825c4)

### Payables Transaction Remit to Address Display

There is now an expansion selection in Payables Transaction Entry to view the Remit to Address details for the selected address ID.

![image](https://github.com/user-attachments/assets/b8dbbc52-f7cf-4f46-93be-388ee88a17f7)

### Save Remit to Address Details to History

Payables transaction Remit to Address Transaction Details will be saved when a payables transaction is posted. These details will be saved in a new table PM80810.  You can now view the saved Remit to Address on PM Transaction once posted from PM Transaction Entry Zoom. In addition, Payment processing will verify actual remit to address details when combining transactions to a single payment.

![image](https://github.com/user-attachments/assets/d47f639e-9606-4e87-bfbb-8cf8e0dee3a8)

### Credit Card Payments setup as Check Cards in PM Missing Originating information in Bank Rec

When you setup a credit card from a checkbook in a non functional currency, now the originating amounts will be displayed correctly on the Checkbook Register.

![image](https://github.com/user-attachments/assets/b788a360-073a-4d87-a15d-62ce3d646131)

### Email address on Doc Type display emails from cust/vend when open email detail

A vendor or customer transaction will display the email address information on the transaction as to how they are assigned im the customer or vendor email setup. 

For example:
* a customer or a vendor is setup to email by document type
* you enter a Purchase Order and you view the email information to verify or edit
* the system will display email address how they are assigned in the email setup

![image](https://github.com/user-attachments/assets/18c1f3b7-7f04-408d-a57a-e8b9959cdd9a)

![image](https://github.com/user-attachments/assets/d0babf1c-d988-499b-9b80-d5edd71b0261)
 
### Sales Document Inquiry Changes

There is now a drill down to Sales Document Detail Inquiry Zoom on Document Number and Orig Number fields on the Sales Document Inquiry window. When you drill down, it will display that selected document in the Sales Transaction Inquiry window.

![image](https://github.com/user-attachments/assets/96c26026-8bf9-4155-9bd4-45647c787b2c)

![image](https://github.com/user-attachments/assets/c0ac82ee-238d-41ff-9676-4d9677f5628e)

### Link SOP Print Options to SOP Document Type

When you are entering a certain transaction type in Sales Transaction Entry, and then you select to print, the system will default the SOP Print options based on the document type. If you are entering a SOP Quote and choose print, the settings for Quote will automatically be marked in the Print Options window. The format will be defaulted from the Document ID Setup.

![image](https://github.com/user-attachments/assets/77c1bde9-4a6a-4d57-8a9d-f159812d7a57)

### Mass email reports from Report Navigation lists

Now when you are working on a Reports Navigation list, you will be able to mark multiple reports that are set to email and using the Send action on the ribbon, email more than one report at a time.

![image](https://github.com/user-attachments/assets/381648dd-f8f7-4181-932e-91e9a839a30e)

### PO Delete Lines action available in PO Entry drop down
On Purchase Order Entry, there are different ways to delete a line that is on the PO.  Now, the PO Delete Line action is also available in the PO entry drop down.

![image](https://github.com/user-attachments/assets/2cd2b5fb-be21-477a-a540-1153a998ed8a)

### Payroll Monthly Deduction Maximum

With the October 2024 release, there is another deduction maximum limit available in U.S. Payroll.  You can now add a Monthly maximum field for Payroll deduction Setup. Or add a Monthly maximum for Payroll deduction entry at the employee level. When you are processing payroll, the limit hierachy will be followed: 1 - Pay Period 2 - Monthly 3 - Shared Deduction 4 - Calendar 5 - Fiscal 6 - Lifetime.

The maximum will be considered during Computer check calculation using user date. If you are entering a manual payment,and the amount is over the deduction maximum a warning will be given. 

![image](https://github.com/user-attachments/assets/b993db8f-ada4-46b4-a349-58bceaf840ff)

### Payroll Monthly Benefit Maximum

There is also another benefit maximum limit available in U.S. Payroll.  You can now add a Monthly maximum field for Payroll benefit Setup. Or add a Monthly maximum for Payroll benefit entry at the employee level. When you are processing payroll, the limit hierachy will be followed: 1 - Pay Period 2 - Monthly 3 - Shared Benefit 4 - Calendar 5 - Fiscal 6 - Lifetime.

The maximum will be considered during Computer check calculation using user date. If you are entering a manual payment,and the amount is over the benefit maximum a warning will be given.

![image](https://github.com/user-attachments/assets/6d91ac93-22c6-4486-83e3-e8e9d3866027)

### Mask ID on Payroll 1099-R

Similar to the Payables 1099 change, there is now an option available on Print 1099-R window to mask the employee's Social Security number. When you mark the checkbox and print a 1099, the Social Security number will print with the first 5 numbers as an X

![image](https://github.com/user-attachments/assets/6c055240-daaf-4520-8e75-652a5f7b60ac)

![image](https://github.com/user-attachments/assets/01b55710-254b-4f98-8412-002d26e94233)

### Workflow emails trim trailing zeroes

With the October 2024 release, we're continuing to improve the workflow emails. Now, in addition to using the item detail decimals for formatting,  the workflow emails will trim trailing zeroes.

![image](https://github.com/user-attachments/assets/e692280b-d887-4251-bda0-ed990dc993cb)

