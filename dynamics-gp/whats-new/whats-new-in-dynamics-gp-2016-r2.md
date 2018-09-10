---
title: "What's new in Dynamics GP 2016 R2"
description: "Learn about enhancements that were added to the product since the release of [!INCLUDE[prodshort](../includes/prodshort.md)] 2016 R2. "
keywords: ""
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.service: dynamicsgp
ms.topic: article
ms.reviewer: 
ms.date: 09/05/2018
---

# What’s new in Dynamics GP 2016 R2

The following sections describe enhancements included in [!INCLUDE[prodshort](../includes/prodshort.md)] 2016 R2.

## Business Intelligence changes 

### SmartList favorite protection

Greater control over changes to SmartList favorites is now available by requiring a password to modify a favorite. When users try to modify a SmartList favorite they will be prompted to enter a password.

### SmartList Designer SmartLists available in Advanced Lookups

Users can now assign SmartList Designer List favorites to Advanced Lookup windows. Favorites now can be assigned to all lookup windows.

### Support secure connection to Management Reporter service

Enable users to connect to Management Reporter (MR) service using a more secure `https://` connection. Currently, the MR Services only supports `http://` This enhancement was added in response to feedback from customers who requested a more secure connection when rendering their financial data. This functionality became available with Management Reporter cumulative update 16.

### Power BI on Web Client Home page

Power BI reports are now available on the web client home page if Dynamics GP must be registered with Power BI App Registration Tool or with Azure Management Portal. With this enhancement, you can make critical business information more readily available than it was previously.

## System-wide enhancements

Indicate the name of person editing a batch in the message "Batch is being edited by another user"

There is now greater visibility for showing which specific users are editing batches. If you try to edit a batch that another user is already working with, that user’s ID appears in the message appears. Previously, the message only indicated that ‘another user’ was editing the batch.

## Financial enhancements

### Distribution Line Display opens expanded

The General Ledger Transaction Entry and Journal Entry Inquiry windows will default the scrolling window expanded or collapsed based on the previous display state. This allows users to display distribution information in more detail by default. The same functionality has been added to the Payables Transaction Entry Distribution and Sales Transaction Distribution Entry windows and the corresponding inquiry windows. The distribution scrolling window will open expanded or collapsed based on the previous display state. This is a per user, per form automatic setting.

### Credit Limit Warning Calculation for unposted Credit Documents

The credit limit warning calculation now considers when a cash receipt is entered and is applied against an outstanding invoice. In the credit limit calculation, we track a customer’s remaining credit limit by looking at invoices that are already posted. We also look at any unposted transactions that would increase or decrease that customer’s balance. The unposted cash receipt is kind of a special case, when it is applied, it automatically adjusts the customer’s remaining balance by the applied amount. Our calculation now considers whether the unposted cash receipt is applied.

### POP to FA Link to Include Taxes

The option is added to include the tax amount in the cost basis of an asset when posting POP through to FA. When using the “by Receipt Line” option for posting, the tax amount calculated for the receipt line is capitalized with the extended cost. When using the “by Account” option, the amount posted to the tax account for the receipt is capitalized with the amounts posted to other accounts set up as Fixed Assets purchasing posting accounts.

### Link credit card invoices to original invoices

When a credit card payment is entered for an invoice the transaction description is now updated with a vendor ID and document number on the credit card vendor invoice to easily trace back to the originating voucher. The GL for Payables reconcile process has been modified to link the credit card payment and credit card vendor invoice to GL entries with Matched Transactions.

### Add Bank Rec history table and do transaction history removal.

A new process for Reconciled Transaction maintenance in Routines has been added that moves reconciled transactions to Bank Reconciliation history tables. With the transactions moved to history, the bank reconciliation process performance will improve. When removing history, the process also removes any moved or reconciled transactions.

### Save Fixed Asset ID with suffix

When setting up a fixed asset, a suffix for the fixed asset, other than 1, can be entered and saved. This enhancement can help you group assets and components.

### SafePay file displays Check Name from the Check

The SafePay file uses the vendor’s name that’s printed on the check when the payment was made, rather than using the default name from the Vendor Maintenance window. While checks can be printed that include vendor names that are different name from the vendor name in Vendor Maintenance. It is important to use the name that was printed on the check as part of the SafePay file because that is the name that the bank uses when the check is presented for payment.

## Distribution enhancements

### Display Tax Percent for Historical Transactions

When drilling into the sales transaction tax details, the tax percent used at time of transaction displays instead of the percent that is set up on the tax detail maintenance window.

### Cancel PO when linked to a Requisition

You can now cancel a purchase order line quantity when it is linked to a purchase requisition. This functionality is available in Purchase Order Entry and in Edit Purchase Orders window. After entering the quantity canceled a warning message is given but you can continue with transaction. The linked icon has also been updated to reflect quantities that cannot be fulfilled if a purchase order has been updated, such as cancelling quantities.

## Human Resources and Payroll enhancements

### Track history on Termination / Rehire Dates

A new Employment History option will now track the date that an employee was hired and the date when their employment concluded. The dates are Hire Date, Adjusted Hire Date, Date Inactivated, Last Day Worked and Termination Date. This information is saved each time one of these date fields is updated.

### Allow payroll user to print using self-service W2 report 

Now the payroll administrator, can print W2 information for employees using the same self-service report that employees use. This eliminates the need for preprinted forms because there is a new form type option available for printing W-2s that prints W-2 information in the correct format with current labels.

## Project Accounting enhancements 

### PA Timesheet Status Report

A new report is available for Project Time Entry (PTE) timesheet approvers that will print the status of all timesheets. The report includes the option to sort the report by the approval status, or by the approver. This report provides visibility into all timesheets, including timesheets that are missing but that were expected to have been entered.

### PA Line Item Distributions added for all transaction entry windows in Project Accounting 

All Project Accounting transaction entry windows have a new window for Line Distributions. This allows you to enter distributions on a per line item basis. Distributions for projects are no longer allowed at the summary level. This will enable the PA Trial Balance report to print the correct distributions for any accounts that were changed during transaction entry.

## See Also

[What's New](introduction.md)  
