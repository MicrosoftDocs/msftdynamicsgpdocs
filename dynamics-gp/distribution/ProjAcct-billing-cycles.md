---
title: "Project Accounting Billing Guide"
description: "Examine how billing cycles work in Dynamics GP's project accounting module."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 03/04/2021
---

# Project Accounting Billing Guide

This part of the documentation includes information for an accounts receivable administrator about how to set up billing cycles for generating billing invoices based on billing frequencies.

## Billing cycles and billing customers for projects

We recommend that you use billing cycles to bill customers for projects. When you use a billing cycle, a batch of billing invoices will be generated using the billing frequency that you specified for the billing cycle. After the batch has been generated, you can modify the billing invoices, as necessary

You can assign billing cycles to customers, contracts, and projects

When you use a billing cycle, you must specify whether to limit billing to the customers, contracts, or projects assigned to the billing cycle. 

You also can enter a batch of billing invoices manually, if necessary. 

## Creating a billing cycle

You can create billing cycles that you can use to generate billing invoices. 

1. Open the Billing Cycle Maintenance window.  Cards > Project > Billing Cycle
2. Enter a billing cycle ID and description.
3. Select the billing frequency and billing date. Enter the cut off date.
4. Select the fees to include when billing customers. 
5. Select the cost transaction types to bill customers for. 
6. Click Save and close the window.

## Invoice and billing formats

This part of the documentation includes information for an accounts receivable administrator about invoice formats and how to specify the information to include on them for printing billing invoices. It also includes information about grouping invoice formats into billing formats so that when you print billing invoices, all invoice formats in the billing format will be included.

## Invoice formats

An invoice format is the framework that contains information for the layout and content of a printed billing invoice. There are 55 predefined invoice formats. The invoice formats that you can choose from are listed in the Standard Billing Reports Lookup window (Tools > Setup > Project > Billing > Billing Report button > Billing Report Key lookup button).

There are several types of predefined invoice formats, including formats specifically for Cost Plus, Fixed Price, or Time and Materials projects. Some invoice formats will display itemized information about the amounts due, while others will display only the total amount due and the current balance. Depending on the invoice format, information might be grouped by contract, project, or cost transaction type. Some invoice formats are specifically for fees.

You can group invoice formats into a billing format so that you can print more than one type of billing invoice at the same time. 

You can specify the content to be included on an invoice format.

You also can use Report Writer to modify the layout of invoice formats, including five blank invoice formats. 

## Specify information to include on an invoice format

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

## Specify information to include for cost transactions on an invoice format

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

## Options for summarizing cost transaction information on invoice formats

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

## Group invoice formats into a billing format

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

## Configure general settings for billing customers

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

## Grant billing invoice and return data entry permissions

You can grant all users permission to various data entry options for billing invoices and billing returns. You also can require a password for each data entry option to limit user access.

1. Open the Billing Setup Options window.  Tools > Setup > Project > Billing > Billing Options button
2. Select the data entry tasks to grant permission for.

    * Override Document Number 

        Allow users to modify the default document number for a billing invoice or billing return.

    * Allow Actual Billings to Exceed Projected Billings  

        Allow users to enter a billing amount that exceeds the calculated billing amount for a billing invoice line item for a Time and Materials project.

3. Click OK.

## Set up a customer class for billing

You can use the PA Customer Class Options window (Tools > Setup > Sales > Customer Class > Project button) to set up a customer class for billing. If you assign a customer to the class, the customer record will inherit information from the class.

The window is similar to the PA Customer Options window. 
 
## Set up a customer record for billing

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

## Default billing formats for customers, contracts, and projects
The billing format that will be used when you print billing invoices depends on the billing formats that you've selected for customers, contracts, and projects. 

You can select the overall default billing format in the Biller Setup window. The default billing format will be used when you print billing invoices if no billing format has been specified for a customer, contract, or project. 

The billing format that you specify for a customer will be the default billing format for contracts for that customer. 

## Use a billing cycle to generate billing invoices
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

## Enter or modify a billing invoice
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

## See also

[Project Accounting Cost Management](ProjAcctCostManagement.md)  
[Project Accounting Administrator's Guide](ProjAcctAdministration.md)  
