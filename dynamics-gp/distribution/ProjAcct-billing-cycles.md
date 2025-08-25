---
title: "Project Accounting Billing Guide"
description: "Examine how billing cycles work in Dynamics GP's project accounting module."
keywords: "payroll"
author: theley502
manager: jswymer
ms.topic: how-to
ms.reviewer: jswymer
ms.author: theley
ms.date: 08/19/2025
---

# Project Accounting Billing Guide

This part of the documentation includes information for an accounts receivable administrator about how to set up billing cycles for generating billing invoices based on billing frequencies.

## Billing cycles and billing customers for projects

We recommend that you use billing cycles to bill customers for projects. When you use a billing cycle, a batch of billing invoices will be generated using the billing frequency that you specified for the billing cycle. After the batch has been generated, you can modify the billing invoices, as necessary

You can assign billing cycles to customers, contracts, and projects

When you use a billing cycle, you must specify whether to limit billing to the customers, contracts, or projects assigned to the billing cycle. 

You also can enter a batch of billing invoices manually, if necessary. 

### Creating a billing cycle

You can create billing cycles that you can use to generate billing invoices. 

1. Open the Billing Cycle Maintenance window.  Cards > Project > Billing Cycle
2. Enter a billing cycle ID and description.
3. Select the billing frequency and billing date. Enter the cut off date.
4. Select the fees to include when billing customers. 
5. Select the cost transaction types to bill customers for. 
6. Click Save and close the window.

## Invoice and billing formats

This part of the documentation includes information for an accounts receivable administrator about invoice formats and how to specify the information to include on them for printing billing invoices. It also includes information about grouping invoice formats into billing formats so that when you print billing invoices, all invoice formats in the billing format will be included.

### Invoice formats

An invoice format is the framework that contains information for the layout and content of a printed billing invoice. There are 55 predefined invoice formats. The invoice formats that you can choose from are listed in the Standard Billing Reports Lookup window (Tools > Setup > Project > Billing > Billing Report button > Billing Report Key lookup button).

There are several types of predefined invoice formats, including formats specifically for Cost Plus, Fixed Price, or Time and Materials projects. Some invoice formats will display itemized information about the amounts due, while others will display only the total amount due and the current balance. Depending on the invoice format, information might be grouped by contract, project, or cost transaction type. Some invoice formats are specifically for fees.

You can group invoice formats into a billing format so that you can print more than one type of billing invoice at the same time. 

You can specify the content to be included on an invoice format.

You also can use Report Writer to modify the layout of invoice formats, including five blank invoice formats. 

### Specify information to include on an invoice format

You can specify the information to include on an invoice format

1. Open the Billing Report Setup window.  Tools > Setup > Project > Billing > Billing Report button
2. In the Billing Report Key field, enter the invoice format to modify.
3. In the Billing Report Name field, you can enter the name for the invoice format to be displayed on the printed billing invoice.
4. If the invoice format includes information grouped by contract, select the following options.

    *    Select Contract Notes to include billing notes for the contract record.

    *    Select Contract Transaction Notes to include billing notes entered for the contract record for cost transactions.

    *    Select how to sort contracts on the invoice format.

5. If the invoice format includes information grouped by project, select the following options.

    *    Select Project Notes to include billing notes for the project record.

    *    Select Project Transaction Notes to include billing notes entered for the project record for cost transactions.

    *    Select how to sort projects on the invoice format.
 
6. If the invoice format includes fee information, select the following options.

    *    Select Detailed to display itemized fee amounts or Totals to display summarized fee amounts.

    *    Select Fee Notes to include billing notes for fees for projects. 

7. Click Transactions to specify information to include for cost transactions on the invoice format.
8. Click Fees to enter descriptive names to be displayed on the invoice format for fees. See Enter names for fee types on an invoice format on page 15 for more information.
9. Click Print Setup to specify settings for users and printers for the invoice format. 
10. Click Save and close the window.

### Specify information to include for cost transactions on an invoice format

You can specify information to include for cost transactions on an invoice format.

1. Open the Billing Report Setup window.  Tools > Setup > Project > Billing > Billing Report button

2. In the Billing Report Key field, enter the invoice format to modify.

3. Click Transactions to open the Billing Report Transactions Setup window.

4. For each cost transaction type, specify the following options.

    * **Summary Level**

        How information will be summarized on the invoice format for the cost transaction type. 

    * **User Defined Transaction Name**

        The name to display on the invoice format as the heading for the cost transaction type.

    * **Sort Order**

        The priority for displaying the cost transaction type on the invoice format. If you select 1, the cost transaction type will be displayed first.

    * **Include Notes**

        Display billing notes on the invoice format that are entered for line items for the cost transaction type. See Billing notes for invoices on  page 16 for more information.

5. Click OK.

### Options for summarizing cost transaction information on invoice formats

When you specify information to include for cost transactions on an invoice format, you can select how the information should be summarized, as outlined in the following table.  

| Option | Description |
|--|--|
| Cost Category | Amounts will be summarized by cost category. |
| Cost Category Class | Amounts will be summarized by cost category class. |
| Cost Category + Cost Owner | Amounts will be summarized by cost category, and then by the employee, equipment, miscellaneous, or item record. |
| Cost Owner | Amounts will be summarized by employee, equipment, miscellaneous, or item record. |
| Cost Owner Class | Amounts will be summarized by employee, equipment, miscellaneous, or item class. |
| Cost  Owner  + Cost Category | Amounts will be summarized by employee, equipment, miscellaneous, or item record, and then by cost category. |
| Cost  Owner  +  Cost Category Class | Amounts will be summarized by employee, equipment, miscellaneous, or item record, and then by cost category class. |
| Cost  Owner  + Document No. | Amounts will be summarized by employee, equipment, miscellaneous, or item record, and then by document number. |
| Date + Cost Owner + Cost Category | Amounts will be summarized by date, then by employee, equipment, miscellaneous, or item record, and then by cost category. |
| Position | Amounts will be summarized by position code. |
| Position + Rate | Amounts will be summarized by position code, and then by pay rate. |
| Trx    Detail | Amounts will not be summarized. Information about every line item entered for every cost transaction will be displayed. |
| Trx  Summary | All line items entered for the cost transaction type will be summarized on a single line. |

You can summarize cost transaction information on invoice formats in two ways:

1. Enter names for fee types on an invoice format

    You can specify the names to display for types of fees on an invoice format.

    1. Open the Billing Report Setup window.  Tools > Setup > Project > Billing > Billing Report button
    2. In the Billing Report Key field, enter the invoice format to modify.
    3. Click Fees to open the Billing Report Fees Setup window.
    4. For each type of fee, enter the name to display on the invoice format for the fee.
    5. Click OK.

2. Specify settings for users and printers for an invoice format

    For each user that will print billing invoices, you can specify the printer to use for an invoice format.

    1. Open the Billing Report Setup window.  Tools > Setup > Project > Billing > Billing Report button
    2. In the Billing Report Key field, enter the invoice format to modify.
    3. Click Print Setup to open the Print Setup window.
    4. Select the user that will print billing invoices using the invoice format.
    5. Click the Printer Name expansion button to select the printer that the user will use when printing billing invoices using the invoice format.
    6. Click OK.

## Billing notes for invoices

When you enter a cost transaction, you can include a billing note for each line item on the transaction. You then can select to print the billing notes on billing invoices.  

When you set up cost transactions for tracking project costs billing customers, you can select the default billing note to use for each line item on cost transactions.

* None

    Don't use a default billing note for line items.

* Budget

    Use the billing note entered for a cost category in a project budget.

* Cost Category

    Use the billing note entered for a cost category record.

### Group invoice formats into a billing format

You can create a group of invoice formats, called a billing format. You can assign billing formats to customers, contracts, and projects and to individual billing cycles for those customers, contracts, and projects. When you print billing invoices, all invoice formats in the billing format will be included.

1. Open the Billing Format Setup window.   Tools > Setup > Project > Billing > Billing Format button
2. Enter the billing format ID and description.
3. Select Default to use the billing format as the default grouping of invoice formats for all new billing formats.
4. In the Standard Bill Reports list, select the invoice formats to include in the billing format and click Insert. The invoice formats will be displayed in the Selected Bill Reports List.
5. In the Selected Bill Reports list, select an invoice format and click Top, Up, Down, and Bottom to change the position of the invoice format in the list. When you print billing invoices using the billing format, invoice formats will be used in the order listed.
6. Click Save and close the window.

## General billing setup

This part of the documentation includes information for an accounts receivable administrator about how to set up Project Accounting to bill customers for projects.  
It also includes information about how to grant all users permission to various data entry options for billing invoices and billing returns.

### Configure general settings for billing customers

You can configure general settings for billing customers, such as how to calculate taxes on billing invoices.

1. Open the Billing Setup window.  Tools > Setup > Project > Billing
2. In the Billing field enter the next document number to use for billing invoices and billing returns. In the Revenue Recognition field, enter the next document number to use for revenue recognition transactions.  
3. Select Recalculate Billing Rate during write up in TM to adjust the billing rate or markup percentage for a billing invoice line item if you enter a write up amount or percentage for the line item. You can enter write up amounts and percentages for line items that are for Time and Materials projects. If you don't select this option, the quantity for the line item will be adjusted if you enter a write up amount or percentage.
4. Select Recalculate Billing Rate during write down in TM to adjust the billing rate or markup percentage for a billing invoice line item if you enter a write down amount or percentage for the line item. You can enter write down amounts and percentages for line items that are for Time and Materials projects. If you don't select this option, the quantity for the line item will be adjusted if you enter a write down amount or percentage.
5. In the Cycle Billing and RR Log file field, enter the path name where a log file will be saved after you complete a billing or revenue recognition cycle. The log file will list any errors that were encountered while generating billing invoices or revenue recognition transactions.  
6. In the Discount From field, select whether discounts for billing amounts will be based on discount amounts entered for the customer, contract, or project record.  
7. Select the default cutoff date to use for billing invoices.

    For example, if you enter a billing invoice and the user date is 9/22/2010, which is a Wednesday, then the following dates will be used.

    |Date format  |Description  |
    |---------|---------|
    |Document  Date     |The date 09/22/2021 will be used.         |
    |Beginning of week | The date 09/20/2021, which is the Monday for the week that the user date is in, will be used.|
    |Beginning of month | The date 09/01/2021 will be used.|
    |End of month | The date 09/30/2021 will be used.|

    The cutoff date that you select in this window does not affect the cutoff date that you select to use with billing cycles.  

8. Select Calculate retainer commission to calculate commissions on Retainer fees for salespeople. 
9. Select Retainer fee taxable to calculate taxes on Retainer fees.
10. Select Include fully billed fees to include on billing invoices information about fees that already have been billed.
11. Indicate whether to specify individual tax options for non-inventoried items, freight, and miscellaneous charges on billing invoices and billing returns or to use a single tax schedule for all charges.

    * Advanced  

        Specify whether non-inventoried items, freight, and miscellaneous charges are taxable, non-taxable, or based on the tax schedule for the customer record. If you select Taxable, select a tax schedule.

    * Single Schedule  

        Select a tax schedule.

12. In the Update Periodics Using list, select whether to use the document date or the posting date on billing invoices and billing returns to update information in the Project Periodic Budget window.
13. Select the Apply Project First to option to specify whether customer payments will be applied first to amounts for cost categories in project budgets or to amounts for fees for projects.
14. You can enter names for user-defined fields that you can use in the Billing Entry window. You must use Modifier to display user-defined fields in the Billing Entry window and you must use Report Writer to include information entered in those fields on reports. See the Modifier and Report Writer documentation (Help > Printable Manuals) for more information.
15. Select the Currency to use in Cycle Biller option to specify whether to use the currency ID selected for the customer in the Customer Maintenance Options window (Cards > Sales > Customer > Options button) or the functional currency selected in the Multicurrency Setup window (Tools > Setup > Financial > Multicurrency) when generating invoices using billing cycles.

    > [!NOTE]
    > If you select Functional Currency, all billing invoices generated using billing cycles will use the functional currency even though you've specified billing currency IDs for the contracts and projects that you're generating billing invoices for.

16. Select Post to Receivables Management to post billing invoices and billing returns to Receivables Management.
17. Click Billing Report to specify information to include on invoice formats.  
18. Click Billing Format to group sets of invoice formats into billing formats. See the [Group invoice formats into a billing format](#group-invoice-formats-into-a-billing-format) section for more information.

19. Click Billing Options to grant billing invoice and billing return data entry permissions. 
20. Click RR Options to grant revenue recognition transaction data entry permissions. 
21. Click OK.

### Grant billing invoice and return data entry permissions

You can grant all users permission to various data entry options for billing invoices and billing returns. You also can require a password for each data entry option to limit user access.

1. Open the Billing Setup Options window.  Tools > Setup > Project > Billing > Billing Options button
2. Select the data entry tasks to grant permission for.

    * Override Document Number 

        Allow users to modify the default document number for a billing invoice or billing return.

    * Allow Actual Billings to Exceed Projected Billings  

        Allow users to enter a billing amount that exceeds the calculated billing amount for a billing invoice line item for a Time and Materials project.

3. Click OK.

### Set up a customer class for billing

You can use the PA Customer Class Options window (Tools > Setup > Sales > Customer Class > Project button) to set up a customer class for billing. If you assign a customer to the class, the customer record will inherit information from the class.

The window is similar to the PA Customer Options window. 
 
### Set up a customer record for billing

You can set up a customer record for billing.

1. Open the PA Customer Options window.  Cards > Sales > Customer > select a Customer ID > Project button
2. Enter the customer alias. The alias will be used to create contract numbers for the customer. 
3. Select the default billing format to use for billing invoices for the customer. 
4. You can select Closed to Project Costs or Closed to Billings to prevent the accrual of costs or to prevent billing for projects for the customer.
5. Select billing cycles to use for billing the customer for projects. You can select a billing format to use with each billing cycle. 
You also can assign billing cycles to contracts and projects. 
6. Select a revenue recognition cycle to use for recognizing revenue for projects for the customer. 
7. Click Accounts to specify posting accounts for the customer. 
8. Click Fee Accounts to specify posting accounts for fees for the customer. 
9. Click OK.
 

## Billing processes

This part of the documentation includes information for an accounts receivable administrator about how to bill customers for projects. It also includes information about how to apply customer payments to billing invoices and to project balances, and how to determine the number of days that billing amounts are past due. You also can suspend billing for customers, contracts, and projects.

## Billing invoices

This part of the documentation includes information for an accounts receivable administrator about creating and printing billing invoices to bill customers for project costs.

### Default billing formats for customers, contracts, and projects

The billing format that will be used when you print billing invoices depends on the billing formats that you've selected for customers, contracts, and projects. 

You can select the overall default billing format in the Biller Setup window. The default billing format will be used when you print billing invoices if no billing format has been specified for a customer, contract, or project. 

The billing format that you specify for a customer will be the default billing format for contracts for that customer. 

### Use a billing cycle to generate billing invoices

You can generate a batch of billing invoices using a billing cycle. 

You can generate billing invoices for a customer, even though the customer record is on hold. 

Billing invoices can be generated for Open or Completed contracts and projects.
 
Before you generate billing invoices, you can age customer balances and the Work In Progress (WIP) account to calculate outstanding balances for customers and projects. 

1. Open the Billing Cycle Batch Processing window.  Transactions > Project > Billing > Cycle Biller
2. Enter or select a batch ID. 
3. Select the billing cycle to use to generate billing invoices.
4. You can modify the billing date and cutoff date. 
5. Select Create Empty Invoices to generate invoices for customers, even though the billing amounts are zero.
6. Select Include Empty Projects to include projects with zero billing amounts on billing invoices.
7. Select Print Report to create a log file after you generate billing invoices. You can modify the path to where the log file will be saved. The log file will list any errors that are encountered. 
8. In the One Invoice Per options, specify whether to print one invoice per customer, contract, or project. The option that you select also will limit billing to the customers, contracts, or projects that are assigned to the billing cycle.

    If you specified various billing currency IDs for contracts for a customer, a separate invoice will be printed for each billing currency. Each separate invoice will include only contracts that use the same billing currency ID.

    If you select to print one invoice per contract or project, you can select the billing address to use.

    * Customer 

        The address selected in the Bill To field in the Customer Maintenance window. 

    * Contract 

        The address selected in the Tax Address ID field in the Contract Settings window. 

    * Project 

        The address selected in the Tax Address ID field in the Project Billing Settings window. 

    If you select to print one invoice per customer, the address selected in the Bill To field in the Customer Maintenance window will be used. See the Receivables Management documentation (Help > Printable Manuals) for more information.

9. Click Process.

### Enter or modify a billing invoice
You can enter a billing invoice manually. However, we recommend that you use billing cycles to generate a batch of billing invoices using the billing frequency that you specified for the billing cycle. After the batch of billing invoices has been generated, you can modify the individual billing invoices, as necessary.

The data that you can enter depends on the permissions that you've been granted. 

You can enter billing invoices for Open or Completed contracts and projects. 
Before you enter a billing invoice, you can age customer balances and the Work In Progress (WIP) account to calculate outstanding balances for customers and projects. 

You can use the Billing Inquiry window (Inquiry > Project > PA Transaction Documents > Biller Documents) to view posted or saved billing invoices, or you can use the Billing-Detail Inquiry window (Inquiry > Project > PA Transaction Documents > Billed Projects) to view billing invoice line item details.
 
1. Open the Billing Entry window.  Transactions > Project > Billing > Billing Entry
2. Select the Invoice transaction type.

Select the TM Return transaction type to modify amounts on a billing invoice for a Time and Materials project. In the Reference Document No. field, enter the document number for the billing invoice that you're modifying amounts for.

3. Enter a document number and date.
4. Enter or select a batch ID. 
5. Select the customer that the billing invoice is for. You can enter the purchase order number from the customer.
6. Select the billing address for the billing invoice.
7. You can modify the cutoff date for billing. Cost transaction line items with dates after the cutoff date won't be billed. The cutoff date must be on or before the billing date specified for the billing cycle. 

8. Select the billing currency for the invoice.

    The default currency will be the currency that you specified for the customer that the invoice is for in the Customer Maintenance Options window (Cards > Sales > Customer > Options button). If you haven't specified a currency for the customer, the functional currency will be used. 

    You can click the Currency ID expansion button to enter or select an exchange rate to use.

9. For each line item on the billing invoice, select the projects to bill the customer for.

    You bill only projects that use the same billing currency as the currency ID that you selected in the Currency ID field.

10. Click the Billings expansion button to select the cost categories to bill for the project and to modify billing amounts. 
11. Click the Fees expansion button to select the fees to bill for a project and to modify fee billing amounts. 
12. Click the Trade Discount expansion button to enter a trade discount amount or percentage for a Time and Materials project.
13. You can modify the tax schedule used to calculate taxes for the line item. You also can modify the purchase order number for the line item.
14. Click More Info to enter payments, taxes, and other charges for the billing invoice. 
15. Click Commissions to modify salesperson commissions for the billing invoice. 
16. Click Contract Notes to modify billing notes that you entered for contracts that the billing invoice is for.
17. Click Project Notes to modify billing notes that you entered for projects on the billing invoice.
18. Click Distribution to modify the allocation of transaction amounts to specific posting accounts. 
19. You can click Print to print the billing invoice. The billing format that will be used depends on the billing formats that you've selected for the customer, contract, or project that the billing invoice is for. The printer that will be used depends on the printer that you specified for the user that is printing. 

    Use the Print Billing Range window to print a batch of billing invoices.  

20. If the transaction is in a batch, click Save. Otherwise, click Post.  


### Select line items to bill and modify billing amounts for a Time and Materials project

You can select the line items to bill and modify billing amounts on a billing invoice for a Time and Materials project.

> [!NOTE]
> Use the Time and Materials Billing Inquiry window (Inquiry > Project > PA Transaction Documents > T&M Billing) to view billing invoice line item details for Time and Materials projects.

1.	Open the Time and Materials Billing window.   Transactions > Project > Billing > Billing Entry > select a Time and Materials project > Billings expansion button
2.	Select the cost transactions to display line items for in the scrolling window.

   The amounts and percentages displayed in the Current column are totals for all posted cost transactions for the employee, equipment, miscellaneous, or vendor record that is listed in the Cost Owner column for the project. Click the Cost Owner expansion button to view a list of the cost transaction line items that have been entered for the cost owner.

3.	In the Bill column, select the check box for line items to bill. Click Bill All or Do Not Bill All to select or clear all check boxes.

   If the line item is for a change order, C- will be displayed next to the date in the Date column. You can’t select a change order line item for billing if the status of the corresponding change order is Unapproved. 

4.	In the Write Up/Down $ or Write Up/Down % column, enter a positive write- up amount or percentage or a negative write-down amount or percentage to modify the total amount to be billed.

   If you enter a write-up amount or percentage and you’ve selected Recalculate Billing Rate during write up in TM in the Billing Settings window, the billing rate or markup percentage will be recalculated. If you haven’t selected this option, the quantity for the line item will be adjusted.

   If you enter a write-down amount or percentage and you’ve selected Recalculate Billing Rate during write down in TM in the Billing Settings window, the billing rate or markup percentage will be recalculated. If you haven’t selected this option, the quantity for the line item will be adjusted.


5.	You can modify the quantity and amount to bill.   You can choose Extras > Options > Split or press CTRL + S to bill a partial quantity. 
6.	You can modify the tax schedule used to calculate taxes for the line item.

   You can click the Tax Amount expansion button to modify tax details for the tax schedule for the line item.

7.	You can modify the trade discount amount for the line item.
8.	You can modify the billing type for the line item. 
9.	A visual cue will be displayed in the Billing Rate column if the line item is for a Time and Materials project that uses the Billing Rate profit type. 
10. A visual cue will be displayed in the Markup% column if the line item is for a Time and Materials project that uses the Markup % profit type. You can modify the markup percentage. 
11.	Click OK.

### Bill a partial quantity for a billing invoice line item for  a Time and Materials project

You can bill a partial quantity for a billing invoice line item for a Time and Materials project.

1.	Open the Time and Materials Billing window by choosing Transactions > Project > Billing > Billing Entry > select a Time and Materials project > Billings expansion button
2.	Select the cost transactions to display line items for in the scrolling window.
3.	Select the line item to bill a partial quantity for and choose Extras > Options > Split or press CTRL + S to open the Billing Entry Split window.
4.	In the Move to Split field, enter the quantity to create a new billing invoice line item for. The original line item will be reduced by the quantity that you enter.
5.	Click OK. The line item in the Time and Materials Billing window will be split into two line items. Select the check box in the Bill column for line items to bill.

### Modify billing amounts for cost categories for a Cost Plus or Fixed Price project

You can modify billing amounts for cost categories for a Cost Plus or Fixed Price project. Billing amounts for Cost Plus and Fixed Price projects are determined by a percentage of completion calculation. 

You can use the Progress Billing Inquiry window (Inquiry > Project > PA Transaction Documents > Progress Billing) to view billing invoice line item details for Cost Plus and Fixed Price projects.

1.	Open the Progress Billing Entry window by choosing Transactions > Project > Billing > Billing Entry > select a Cost Plus or Fixed Price project > Billings expansion button
2.	Select the cost transactions to display cost categories for in the scrolling window.

   If the cost category includes amounts from a change order, C- will be displayed next to the cost category ID in the Cost Category ID column. The cost category won’t be billed if the status of the corresponding change order is Unapproved. 

3.	You can modify billing amounts.
4.	You can modify the tax schedule used to calculate taxes for a cost category.

   Choose the Tax expansion button to modify tax details for the tax schedule for the cost category.

5.	If the project includes a Retentions fee and the project status is Completed, you can modify the retention amount for a cost category.

   You can click Recalculate to display the original amounts that were calculated for the cost categories before you made changes.

6.	Click OK.

### Select fees to bill and modify fee billing amounts for a project

You can select the Project, Retainer, and Service fees to bill for a project and modify fee billing amounts on a billing invoice. To modify Retentions fee billing amounts for Cost Plus and Fixed Price projects, use the Progress Billing Entry window. 

You can use the Billable Fees Inquiry window (Inquiry > Project > PA Transaction Documents > Fee Billing) to view fees billed for projects.

1.	Open the Billable Fees window by choosing Transactions > Project > Billing > Billing Entry > Fees field > select a Project Number > Fees expansion button

   The fees to be billed for the project will be displayed.

   If a fee is the result of a change order, C- will be displayed next to the fee ID in the Fee ID column. The fee won’t be billed if the status of the corresponding change order is Unapproved. 

2.	You can modify the billing note for a fee.
3.	You can modify billing amounts.
4.	You can modify the tax schedule used to calculate taxes for a fee.

   You can click the Tax Amount expansion button to modify tax details for the tax schedule for the fee.

5.	If a Project fee includes a retention amount and the status for the project that the fee is assigned to is Completed, you can modify the retention amount for the fee.

   You can click Default to display the original amounts for the fees before you made changes.

6.	Click OK.

### Enter payments, taxes, and other charges for a billing invoice

You can enter payments, taxes, and other charges for a billing invoice.

1.	Open the Billing Entry – More Info window.   Transactions > Project > Billing > Billing Entry > More Info button
2.	Enter freight and miscellaneous charges for the billing invoice. Click the Freight or Miscellaneous expansion button to specify whether an amount is taxable, non-taxable, or based on the tax schedule for the customer record. If you select Taxable, select a tax schedule.
3.	Click the Total Tax expansion button to view information about the tax details that are included in calculating tax for the billing invoice.
4.	Click the Applied Retainer expansion button to enter the Retainer fee amount to be credited to the billing invoice. The On Account Amount in the Retainer Billings window includes Retainer fee amounts that have been paid by the customer. 
5.	Select the payment terms for the billing invoice. You can click the Payment Terms ID expansion button to enter the amount or percentage discount that the customer will receive if payment terms are met.
6.	Select a shipping method.
7.	Enter cash, check, and credit card payments that have been made for the billing invoice. You can click the Cash, Check, or Credit Card expansion button to enter additional information about the payment.
8.	If the customer will be given a discount for the billing invoice, enter the amount in the Terms Disc Taken field.
9.	Click OK.

### Modify salespeople commissions for a billing invoice

You can modify the commission amounts that salespeople will receive for a billing invoice. And while you can assign only one salesperson per contract, you can use the Commission Detail window to divide commissions among multiple salespeople. 

1.	Open the Billing Commissions window by choosing Transactions > Project > Billing > Billing Entry > Commissions button
2.	Select a contract and click the Total Commissions expansion button to open the Commission Detail window.
3.	Select the salespeople to receive commissions for the billing invoice. Select the sales territories to track commissions for.
4.	In the Percent of Billing column, enter the percentage of the total billing amount to calculate commissions on or modify the total billing amount in the Commission Billing Amt column. Enter the percentage commission that a salesperson will receive in the Commission Percent column.

   The Commission Amount column will be updated based on your entries.

5.	Click OK.

### Modify billing amounts for a posted billing invoice for a Time and Materials project

You can use the TM Return billing transaction type to modify billing amounts for a posted billing invoice for a Time and Materials project.

1.	Open the Billing Entry window by choosing Transactions > Project > Billing > Billing Entry
2.	Select the TM Return transaction type.
3.	Enter a document number and date.
4.	Enter or select a batch ID. 
5.	In the Reference Document No. field, enter the document number for the billing invoice that you're modifying amounts for.
6.	Select a project to modify billing amounts for.
7.	Click the Billings expansion button to open the Time and Materials Return window.
8.	Select the cost transactions to display line items for in the scrolling window.

   The amounts and percentages displayed in the Invoiced column are totals for all posted billing invoice line items for the employee, equipment, miscellaneous, or item record that is listed in the Cost Owner column for the project. Click the Cost Owner expansion button to view a list of the billing invoice line items that have been entered.

9.	In the **Rtn** column, select the check box for line items to return. Choose **Return All** or **Do Not Return All** to select or clear all check boxes.

10.	You can modify the quantity for the line item.
11.	You can modify the tax schedule used to calculate taxes for the line item.

   Choose the **Tax Amount** expansion button to modify tax details for the tax schedule for the line item.

12.	You can modify the trade discount amount for the line item.
13.	Click OK.

### Modify payments and charges for a posted invoice for a Time and Materials project

You can use the TM Return billing invoice transaction type to modify payments, taxes, and other charges for a posted billing invoice for a Time and Materials project.

1.	Open the Billing Entry window by choosing Transactions > Project > Billing > Billing Entry
2.	Select the TM Return transaction type.
3.	Enter a document number and date.
4.	Enter or select a batch ID. 
5.	In the Reference Document No. field, enter the document number for the billing invoice that you're modifying amounts for.
6.	Click More Info to open the Billing Entry - More Info window.
7.	Modify freight and miscellaneous charges. Click the Freight or Miscellaneous expansion button to specify whether an amount is taxable, non-taxable, or based on the tax schedule for the customer record. If you select Taxable, select a tax schedule.
8.	Click the Total Tax expansion button to view information about the tax details that are included in calculating tax.
9.	Select a shipping method.
10.	Modify cash, check, and credit card payments that have been made for the billing invoice. You can click the Cash, Check, or Credit Card expansion button to enter additional information about the payment.
11.	In the Discount Returned field you can modify the discount that the customer was given for the billing invoice.
12.	Click OK.

## Print billing invoices

You can print a batch of billing invoices or select a range of document numbers to print billing invoices for.

1.	Open the Print Billing Range window.  Transactions > Project > Billing > Print Biller Documents
2.	Select whether to print Work (saved) or Open (posted) billing invoices, or invoices that have been moved to history. 
3.	Select Document Range to print billing invoices based on a range of document numbers and enter the range. Select Batch to print a batch of billing invoices and select the batch.
4.	Choose the billing format to use.

   - Choose a billing format, and then choose **Override** to use that billing format instead of the billing formats that have been assigned to the customers, contracts, or projects that the billing invoices are for.

   - Select **Use Document Bill Format** to use the billing formats that have been assigned to the customers, contracts, or projects that the billing invoices are for.

   - Select **Multicurrency** to use the version of the billing format that is set up for multiple currencies. You must have Include Multicurrency Info selected in the Posting Setup window (Tools > Setup > Posting > Posting) for the Billing Entry origin for the Project series. See the System Setup documentation (Help > Printable Manuals) for more information.

5.	In the Collate by and then by lists, select the sequence to print the billing invoices in.
6.	Click Print.
 
## Applying and aging

This part of the documentation includes information for an accounts receivable administrator about applying payments from customers to projects. It also includes information about how to use aging to determine the number of days that billing invoice balances are past due and the number of days that work in progress and accrued revenue amounts have remained unbilled.

### Apply payments, credits, and returns to billing invoices and project balances

You can apply customer payments, credit memos, and billing returns to billing invoices and project balances.

You can use the Billings and Payments Inquiry window (Inquiry > Project > PA Transaction Documents > Billings and Payments) to view billing invoices and customer payments for projects.

1.	Open the Apply Sales Documents window by choosing Transactions > Sales > Apply Sales Documents
2.	Select a customer ID.
3.	Select the document type and the document number to apply.
4.	Enter an apply date.
5.	Select the billing invoices to apply amounts to. You can modify the amount to apply in the Apply Amount column. You also can enter amounts in the Terms Taken and Writeoffs columns to increase or decrease the amount remaining to be applied to the billing invoice.
6.	Click the Apply Amount expansion button to select the projects to apply amounts to. The Apply Projects window will open.
7.	In the Default Apply First To list, select whether to apply amounts first to cost categories in project budgets or to fees for projects.
8.	In the scrolling window, select the projects to apply amounts to. You can click Auto Apply to distribute amounts among projects in the scrolling window. Click Unapply to clear applied amounts for all projects in the scrolling window.
9.	You can modify the amounts to be applied to cost categories in project budgets or to fees for projects.
10. You can modify the discounts or writeoff amounts to be applied to each project.
11. Click OK to close the Apply Projects window.
12. Click OK to close the Apply Sales Documents window.

### Age billing invoice balances

You can age billing invoice balances to determine the number of days that the balances are past due. To be sure that calculations are accurate, you must enter and post all billing returns and customer payments before aging balances.

1.	Open the Project Aging Process window.   Tools > Routines > Project > Aging
2.	Enter the date to age balances from. The document date for each billing invoice will be compared to this date to determine the age of each document.

   Use the Receivables Management Setup window (Tools > Setup > Sales > Receivables) to set up aging periods

3.	Select the customers to include billing invoices for.
4.	An aging report will be printed after you age balances. Select Detailed to list billing invoices for each customer or Summary to display only customer totals. Select No Report to age without printing a report.
5.	Click Process.

### Age work in progress amounts for projects that use the When Billed accounting method

You can age work in progress amounts for cost transactions to determine the number of days that the amounts have remained unbilled for Time and Materials projects that use the When Billed accounting method.

To be sure that calculations are accurate, you must post all cost transactions before aging work in progress amounts.

1.	Open the Project Aging WIP Process window.   Tools > Routines > Project > Aging WIP
2.	Enter the date to age work in progress amounts from. The document date for each cost transaction will be compared to this date to determine the age of each document.

   Use the Receivables Management Setup window (Tools > Setup > Sales > Receivables) to set up aging periods. 

3.	Select the customers to include work in progress for.
4.	A report will be printed after you age work in progress amounts. Select whether to summarize work in progress by customer, contract, project, or cost category.
5.	Click Process.
 

### Age unbilled accrued revenue amounts for Time and Materials projects

You can age accrued revenue amounts for cost transactions to determine the number of days that accrued revenue amounts have remained unbilled for Time and Materials projects that use the When Billed or When Performed accounting method.

1.	Open the Project Aging Accrued Revenue window.  Tools > Routines > Project > Aging Accrued Revenues
2.	Enter the date to age accrued revenue amounts from. The document date for each cost transaction will be compared to this date to determine the age of each document.

   Use the Receivables Management Setup window (Tools > Setup > Sales > Receivables) to set up aging periods. 

3.	Select the customers to include accrued revenue for.
4.	A report will be printed after you age accrued revenue amounts. Select whether to summarize accrued revenue by customer, contract, project, or cost category.
5.	Click Process.


## Billing suspension

This part of the documentation includes information for an accounts receivable administrator about how to suspend billing for customers, contracts, and projects.

When you suspend billing, you can’t enter or post billing transactions for the project or projects until you clear the Closed to Billings option for the customer, contract, or project record.

The following topics are discussed:

•	Suspend billing for a customer
•	Suspend billing for a contract
•	Suspend billing for a project

### Suspend billing for a customer

You can suspend billing for a customer. When you close a customer record to billing, billing transactions can’t be entered or posted for projects for the customer.

1.	Open the PA Customer Options window by choosing  Cards > Sales > Customer > select a Customer ID > Project button
2.	Select Closed to Billings.
3.	Click OK.

### Suspend billing for a contract

You can suspend billing for a contract. When you close a contract to billing, billing transactions can’t be entered or posted for projects for the contract.

1.	Open the Contract Maintenance window by choosing Cards > Project > Contract
2.	Select a customer ID and enter a contract ID.
3.	Select Closed to Billings.
4.	Click Save and close the window.

### Suspend billing for a project

You can suspend billing for a project. When you close a project to billing, billing transactions can’t be entered or posted for the project.

1.	Open the Project Maintenance window.  Cards > Project > Project
2.	Select a project number.
3.	Select Closed to Billings.
4.	Click Save and close the window.

## Multicurrency billing feature in Project Accounting

In Project Accounting in Microsoft Dynamics GP, you can enter budget amounts in a currency other than the functional currency. This multicurrency billing feature lets you create a budget and then create a billing invoice by using the customer's originating currency. For example, a customer negotiates a billing rate in the originating currency for a project. In this situation, the billing rate doesn't change even if the exchange rate is different at the time of billing. The functional amount is adjusted to reflect the exchange rate at the time of billing. So the project budget bears the risk of any changes in the exchange rate.

### More information

Consider the following behavior that occurs when you use the multicurrency billing feature:

- You can enter an originating currency in the Billing Currency ID field in the Contract Maintenance window and then create a multicurrency billing project. However, this feature is available only for Time and Materials and for Fixed Price projects that have a fee.
- The currency that's entered on the contract in the Contract Maintenance window is automatically rolled down to the projects. All projects under the contract must be assigned the same currency. This currency cannot be changed.
- The Change Orders button may be disabled in the Contract Maintenance window and in the Project Maintenance window. The button is disabled if an originating currency is entered in the Billing Currency ID field. This behavior occurs because the change order functionality is unavailable on multicurrency billing projects.

#### Profit Types

-Only Billing Rate and None profit types can be used on multicurrency billing projects.
-Purchase/Material - Inventory cost categories cannot be used.

#### Fees

Only fees that use Fee Amount as their calculation method can be added to multicurrency billing projects.

#### Exchange Rate Entry

In the Project Maintenance window:

- The Billing Currency ID field has a lookup button.
- If the project status is Estimate, clicking the button opens the PA Baseline Exchange Rate Entry window.
- If the status is Open, it opens the PA Forecast Exchange Rate Entry window.
- The exchange rate entered here is used only for budgeting, not for actual transactions.

#### Currency Viewing Options

A Change Currency Viewed list is available in:

- Contract Maintenance window
- Project Maintenance window
- Budget Maintenance window

#### Budget Restrictions

If the originating currency is displayed in the Budget Maintenance or Budget Detail Entry window: Unit cost cannot be changed.

If the functional currency is displayed: Billing rate cannot be changed in the Budget Detail Entry window.

#### Profit Source

If the functional currency is not entered in the Billing Currency ID field:

- Profit always comes from the budget.
- The profit type used is the one entered in the Profit Type field.

#### Cost Transactions

When entering a cost transaction:

- The lookup button next to the Date field is enabled.
- Clicking it opens the PA Billing Exchange Rate Entry window.
- The exchange rate entered here is used to calculate total accrued revenues.

#### Billing Currency

Projects can only be billed using the billing currency entered in the Project Maintenance window.

#### Exchange Rate Variations

If the exchange rate changes between cost entry and billing:

- The difference is posted to:
- Adjusted Unbilled Revenue
- Adjusted Unbilled Receivable

These use the same account numbers as:

- Unbilled Project Revenue
- Unbilled Accounts Receivable

#### Rate Tables

You can add an Employee or Position Rate Table via the Project Billing Settings window.

- Only cost information comes from the rate table.
- Profit information always comes from the budget.

## See also

[Project Accounting Cost Management](ProjAcctCostManagement.md)  
[Project Accounting Administrator's Guide](ProjAcctAdministration.md)  
