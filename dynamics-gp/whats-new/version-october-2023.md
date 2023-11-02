---
title: What's new in Dynamics GP in October 2023
description: Learn about enhancements that were added to the product in the October 2023 release of Dynamics GP.
author: theley502
ms.author: theley
ms.reviewer: jswymer
manager: tfehr
ms.prod: dynamics-gp
ms.topic: article

ms.date: 10/30/2023

# What's New in Dynamics GP in October 2023

This page lists enhancements to Dynamics GP in the October 2023 release. The Dynamics GP October 2023 release enhances different areas of the product.

For an overview and additional details for key enhancements, see the [Dynamics GP Blog](https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-october-2023---feature-blog-series-schedule).

## Core Features

Functionality has been added across the core modules of Microsoft Dynamics GP.

### [Add Display action for Financial Summary Inquiry](https://community.dynamics.com/blogs/post/?postid=102180cc-5c62-ee11-a81c-00224852432e)

There is a redisplay action added to the ribbon on the Financial Summary Inquiry window. This action allows you to refresh the information displayed without needing to close Summary Inquiry and reopen it. 


![Shows the summary inquiry window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/8e9943a8-dc2b-40b6-9382-05604a8636ba)

### [Reverse Fiscal Year End Close by Company](https://community.dynamics.com/blogs/post/?postid=18ada931-ee62-ee11-a81c-00224852432e)

Previously, to run the Reverse Fiscal Year End Close process, all users had to be out of all companies.  Now, we only require all users to be out of the company you want to process the Reverse Fiscal Year End Close.

### [Display Open Transactions only for Customer Statements](https://community.dynamics.com/blogs/post/?postid=6f8bdf93-c963-ee11-a81c-00224852432e)

There is an option added to the Print For selection in Print Receivables Statement.  This option allows you to remove any payments, credits, debits, or invoices that have been fully applied from the statement.  Now, you can restrict the amount of detail displayed on the statement by this new selection.

![Shows a print receivables statement in the user interface](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/23090475-7e2e-4a2e-bd33-a10f01e0ec43)

![Shows a printed receivables statement](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/65fd92b2-3b99-4f43-a274-fe6622f8c368)

### [Print/Email Cash Receipts Enhancements](https://community.dynamics.com/blogs/post/?postid=0705bcf3-1469-ee11-a81c-000d3adadbcd)

More features have been added the Email Cash receipts functionality. The email detail icon displays on Cash Receipts Entry and on Cash Receipts Inquiry.  When selected, the Email Detail Entry will display.  This form shows the default email address selected from the customer’s bill-to address and the default message ID. By displaying on this form, the user can edit the email address to be used or the message that will be included on the email. 
With this release you can mass update the customer email settings from the Customers navigation list, as well as mass assign the cash receipt email to customers in Report Template Maintenance.

![Shows the cash receipts entry window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/99630f32-0d2e-47d3-a8f4-f61cae119c2e)

![Shows the receivables ee-mail entry detail entry window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/b8ffa9dc-b3e0-42a3-acb1-3daa68a907d9)

### Email/Reprint Vendor Remittance with Message Fields

When you choose to email or reprint the vendor remittance, we've extended the functionality to include any customized message fields.  Now, when you edit the Vendor email message, this same message will be used prior to posting the Vendor remittance as well as when you reprint it.

![Shows the vendor remittance window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/ebf5b587-328a-4ad6-a9a3-8c888506fb65)

### Print 1099-DIV with Lines and Boxes

In the October 2023 Microsoft Dynamics GP release, we have added the capability to print the 1099-DIV with lines and boxes, similarly to the 1099-NEC. When you select 1099-DIV, the Form Type DDL displays an option for One Wide with Box. When printed, this option will display the 1099-DIV with the lines, boxes, and text to visually represent the 1099-DIV.

![Shows the print 1099 window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/96c43bd6-53a4-4ed2-a408-914a0a5138e0)

![Shows a printed 1099](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/173fae10-086e-4a14-a0ad-d9c231c24980)

### Print 1099-INT with Lines and Boxes

Now, you can print the 1099-INT with lines and boxes similarly to the 1099-NEC. The Form Type DDL displays an option for One Wide with Box. When printed, this option displays the 1099-INT with the lines, boxes, and text.

![image](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/00bfb027-bd95-492c-814d-6de83621ef3b)

### Print 1099-Misc with Lines and Boxes

In this release of Microsoft Dynamics GP, we have added the capability to print the 1099-MISC with lines and boxes. When you select 1099-MISC, the Form Type DDL will display an option for One Wide with Box. The printed form will display the 1099-MISC with the lines, boxes and text. 

![Shows the print 1099 INT](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/5bfd39e7-e3dc-4778-ae06-6127d4058367)

### SOP Blank Picking Ticket/Packing Slip Bin Sequence Template

When either the Print Separate Picking Ticket per site or Print Separate Packing Slip is marked, you can now print the Template form directly to the printer. This functionality will be consistent for both the Picking Ticket and Packing Slip. The system prints a document for each site and an additional document that includes all sites combined.

![Shows the sales document print options window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/f1ae2cb6-c5ba-4d7a-b33b-383a30594004)

![Shows the report destinations window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/10dd006d-d27a-4674-abf7-40483c250147)

### Allow U of M from Requisition to default on Purchase Order

A setup option has been added for Purchase Order Requisition U of M functionality. This option allows you to use the U of M from the PO Requisition line item when generating the Purchase Order. This will default to the Item’s Default Purchasing U of M during the upgrade.

![Shows the requisition setup window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/311ca5c2-0a05-499f-91c7-b96bdfdce936)

![Shows the purchase orders preview window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/6d24b6ce-09ce-46d1-a71f-5eef18f3a4b6)
 
### Format Numbers on Payroll Year End Wage Report

There is additional formatting of numbers and amounts on the Payroll Year End Wage Report.

![Shows the printed payroll year end wage report](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/b933ebb1-695c-49e0-aaac-5d78200adfd6)

### Display Item Decimals on Workflow Email messages

With the new release, workflow email messages now format item detail fields to use the decimals assigned to the items.

![Shows the email message with new format](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/4dee6599-0176-4953-92a2-a75a48c0637a)

### Project Time and Expense My Expenses Navigation List

We've added a My Expenses navigation list for Project Time and Expense. This list will display for the user who is logged in, and it displays any expenses they've entered as well as any expenses entered on their behalf.

![Shows the expenses window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/94da5db5-dc61-48bd-99ff-7b8211ec5cc8)

### Project Time and Expense My Team Expenses Navigation List

Now, there is a My Team Expenses navigation list for Project Time and Expense. This list displays expenses for the user who is logged in and any users this user is a delegate for.

![Shows the teams expenses window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/68713ca5-947a-42e6-9df1-0d4207b290bf)

### Project Time and Expense My Timesheets Navigation List

We've added a My Timesheets navigation list for Project Time and Expense. This list will display for the user who is logged in, and it displays any timesheets they've entered as well as any entered on their behalf.

![Shows the timesheets window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/cc08598d-eb7a-4235-a083-a14cdcd74f34)

### Navigations Lists Filter by Batch Source display Drop Down List selection

On any batch navigation list, there is a filter for the Batch Source field.  Now, there is a drop down list that will display the available batch sources based on the navigation lis type. 

![Shows the receivables transactions window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/18623b6b-b038-4b87-9ec7-1c67f068e4f6)

![Shows the purchasing transactions window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/677597e1-647c-4ddf-8707-feba530bbb5f)

### Shared Mailbox with MultiFactor Authentication

Now, you can select to use a Shared Mailbox when using MultiFactor Authentication. This option is available for both Sales and Purchasing Email setup. It allows you to use a different mailbox for each. When using a shared mailbox, only a single mailbox can be entered. The Shared mailbox will be used as the Send from Address as well as when replies are sent for any email documents in the series.

![Shows the sales e-mail setup window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/8aebfd44-d096-400b-a178-93f8e708d95e)

![Shows the purchasing e-mail setup window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/7d5b11cf-f6e5-45c0-9219-07a90cd92487)

### Fully Delete Document Attachment

We've added the ability to fully delete document attachment. This process will remove the attachment completely from the document attachment blob file storage. This is available for all document attachment management windows and appears as a new ribbon action on the Document Attachment Management window.

![Shows the document attachment management window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/cde2e04e-b852-4146-97b5-6f668c680c8d)

![Shows the document attachment management card](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/38ac0cf0-c01f-40e8-8cda-f936871137c5)

### Letter Writing Assistant Human Resources Letters

We've added new letter templates for Human Resources: All Skills and Tests, Expiring Skills and Tests, Expiring Skills and Expiring Tests. Each of these letter options will display the tests or skills in a table format.

![Shows the letter writing assistant window](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/59f4f0e6-daa4-4d95-a598-f54807ee07a2)

![Shows the printed letter](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/9c375e5a-5209-46b8-9459-c4ec4644cb1e)

### Letter Writing Assistant Collection Final Notice Letter

The Final Notice letter template for Letter Writing Assistant will display the invoice information in a table format.

![Shows the letter writing assistant window for final notice letter](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/b3f0f808-84c1-45f5-98ae-d77408935cd1)

![Shows the printed final notice letter](https://github.com/MicrosoftDocs/msftdynamicsgpdocs/assets/28811495/a4c900b0-681d-4744-86d5-a10f8c8ec844)

