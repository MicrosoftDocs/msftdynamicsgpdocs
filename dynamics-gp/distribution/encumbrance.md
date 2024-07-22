---
title: Encumbrance management
description: Learn about the Encumbrance Management capabilities in Dynamics GP.
keywords: 
author: theley502
ms.reviewer: jswymer
ms.topic: article
ms.author: theley
ms.date: 07/22/2024
---

# Encumbrance Management
Encumbrance Management enables you to reserve funds from a budget when purchase orders are created. You can create encumbrances for standard, drop-ship, blanket, and drop-ship blanket orders. You can authorize multiple encumbrances at one time, and set up passwords that verify authorization to exceed budget amounts. In addition, you view inquiries and reports that show encumbrances against budget amounts as well as displaying information in detail or summary formats for actual versus budgeted amounts.

## Recent updates with Encumbrance Management

- [Encumbrance Year-End Transfer or the Encumbrance reconcile routine data issues](https://community.dynamics.com/blogs/post/?postid=70bb2e70-82e6-4049-a3aa-b5a1b8a9afc0)
- [Encumbrance Management and Blanket Purchase Orders](https://community.dynamics.com/blogs/post/?postid=3b463b0a-ce74-4663-9fdd-ab8956d69c7f)
- [Error: You can’t transfer encumbrances for XXXX when there are outstanding encumbrance amounts for a prior fiscal year](https://community.dynamics.com/blogs/post/?postid=a59bf1e9-7e94-4fbe-8b96-4e4508fcc715)
- [Error: You can’t transfer encumbrances for XXXX when there are outstanding encumbrance amounts for a prior fiscal year](https://github.com/theley502/msftdynamicsgpdocs/assets/43243051/59b7022d-e846-4144-8f34-72d9bb2ae8fd)
- [Encumbrance Summary Inquiry Amounts Do Not Match Detail in Microsoft Dynamics GP](https://community.dynamics.com/blogs/post/?postid=ee1f1afc-6c4b-48eb-b242-24ba8577698f)
- [How to use Encumbrance and Approvals together successfully](https://community.dynamics.com/blogs/post/?postid=a5e474e8-bc64-4316-924f-b3f98dad023a)
- [Microsoft Dynamics- Purchase Order Processing/Encumbrance](https://community.dynamics.com/blogs/post/?postid=faefd3c7-0068-4e5e-a5d6-4a168221ee51)
- [Information regarding Encumbrance and Blanket Purchase orders](https://community.dynamics.com/blogs/post/?postid=85ee2dfc-bd4c-4c06-8798-00cb58160210)
- [Microsoft Dynamics GP Encumbrance Year End Transfer Error](https://community.dynamics.com/blogs/post/?postid=3e311f09-b974-4b1a-8e9e-ec03ced203a8)
- [Errors seen in Purchase Order Processing when Encumbrance Management and Requisition Management are installed](https://community.dynamics.com/blogs/post/?postid=e16c0e9d-cd66-4ccb-8b31-985b3c83f7b2)

## Encumbrance Setup

An encumbrance is a purchase that affects budgets because it is an obligation for goods, materials, and services that have been ordered but not received. When you set up Encumbrance Management, any existing purchase order line items in Microsoft Dynamics GP are evaluated. Each valid purchase order line item is assigned a status of Encumbered. Subsequent purchase order line items will be evaluated when you enter them. The budget that’s encumbered is the budget that includes the period of the required date for a purchase line item.

When you set up Encumbrance Management, you select the budget that will be encumbered for the amount of purchases. Any type of budget can be selected: 
General Ledger, Analytical Accounting, or Grant budgets.
You can enter a budget tolerance to limit the acceptable variance when a purchase transaction exceeds the available budget. You can set up a password to require 
authorization before the purchase order is sent to the vendor. Also, you can select what actions occur when a purchase order is approved.

## Prerequisites for using General Ledger budgets

To use General Ledger budgets with Encumbrance Management, you must set up budgets in General Ledger for each period of each open year.
Prerequisites for using Analytical Accounting budgets.

To use Analytical Accounting budgets with Encumbrance Management, you must complete the following steps to cover each period of each open year with a budget.  

- Create one or more budget trees.
- Set up dimension codes and assign a dimension code tree to a budget tree.
- Create a budget and assign a budget tree to that budget (you can assign the same budget tree to multiple budgets)

## Prerequisites for using Grant budgets

Grant Budgets are actually Analytical Accounting budgets that are linked to a grant. The steps for using Grant budgets for Encumbrance Management are similar to the steps for using Analytical Accounting budgets, with the following exception. You must use Grant Management to associate a grant with a dimension code in an Analytical Accounting budget.

After you save your changes in the Encumbrance Setup window, all existing purchase order line items are evaluated. An encumbrance amount is created using the required date on the purchase order line item, and receipts posted against that purchase order line item will have a liquidation that’s created using the posting date of the receipt. 

## To set up Encumbrance Management

1. Open the Encumbrance Setup window.
(Microsoft Dynamics GP menu >> Tools >> Setup >> Purchasing >>Encumbrance Management)

2. Mark Enable Encumbrance Management.

    This option must be marked to use Encumbrance Management, and to make the other fields in the window available.

3. Select a budget type.

    Available budget types include General Ledger, Analytical Accounting, or Grant budgets. You can specify a budget tree when Analytical Accounting Budgets is the selected budget type. 

    If you’re using Fiscal Year as the tracking method, you must specify a budget tree.

    If the selected budget type is Grant Budgets, purchase order line items will be encumbered when you enter transactions for the grant that’s assigned to the corresponding budget in Grant Management. 

4. Mark a tracking method for your encumbrances.

    The tracking method determines how the budget amounts and the purchase order amounts (plus actual amounts) are compared to each other.

    - *Total Budget*

      Purchases are compared to the total budget and total actual amounts for that budget.

    - *Period*

      Purchases are compared to the budget and actual amounts for the period of the purchase.

    - *Budget-To-Date*

      Purchases are compared to the budget and actual amounts in the range from the starting date for the budget to the end of the period of the required date on the purchase order. 

    - *Fiscal Year*

      Purchases are compared to the total budget and total actual amounts for the fiscal year specified in the required date on the purchase order. 

    If you are using Analytical Budgets and you select Fiscal Year as the tracking method, you must specify a budget tree to use in validating purchases. 

    If you use blanket purchase orders, we recommend that you use the Total Budget tracking method to help ensure that budgets are not unexpectedly exceeded.

5. To set up a password for authorizations of purchase order amounts that exceed the budget limits, choose Enter/Change Password to open the Encumbrance 
Password Setup window. 

6. Select a tolerance level type and enter an acceptable amount or percentage that a purchase may vary from the available budget before authorization is required.

    You can enter either a positive or negative budget tolerance level—an amount or percentage that a purchase is allowed to deviate from a budget without requiring authorization. 

7. If you’re using General Ledger or Analytical Accounting budgets, in the scrolling window, enter or select the budget IDs that purchases should be compared to.

    None of the periods within any of the budgets that you select may overlap. For example, if Budget A spans June 2016 through May 2017 and Budget B spans May 2017 through May 2018, you won’t be able to select both budget A and B because they contain overlapping periods. 

8. If you’re using Analytical Accounting budgets, choose to validate budgets by account or node in a budget tree.

    Choosing **Node** causes the budgets to be validated by a combination of dimension codes from Analytical Accounting. Choosing **Account** causes the budgets to be validated by a combination of accounts and dimension codes. 

9. If you are using Workflow or purchase order approvals in Purchase Order Enhancements, select an option for how approved purchase orders are 
encumbered.

  - *Ask when over budget*

    Encumbers any purchase order lines that are under budget. Displays a message for lines that are over budget with the option to encumber those lines or leave them pre-encumbered. Choose this option when If you enter a positive value If you enter a negative value Amount Purchases can exceed the budget amount by the currency amount you specify.

  - *Always pre-encumber*

    Pre-encumbers all purchase order lines, regardless of their budget status. With this option, the Mass Encumbrance window is used to do all validations against the budget.

  - *Pre-encumber*

    When over budget Encumbers any purchase order lines that are under budget and pre-encumbers lines that are over budget. Choose this option when different people have authority to approve the purchase order and over-expenditures to the budget. In this scenario, the Mass Encumbrance window is used to approve the over-expenditures to the budget.

10. Choose OK to save your changes and close the Encumbrance Setup window.

If you have existing purchase orders or receipts in your system, all purchase order line items and receipts are verified. If the purchase order or receipt is valid, the purchase order is encumbered, even if it exceeds the budget amount. 

## Setting up or modifying the encumbrance password

You can use the Encumbrance Password Setup window to set up or modify the password for authorizations of purchase order amounts that exceed the budget 
limits. If you set up a password, and the purchase amount exceeds the specified limits, users will need to enter a password before the purchase can be encumbered.

To set up or modify the encumbrance password:
1. Open the Encumbrance Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Purchasing >> Encumbrance Management)
2. Choose the Enter/Change Password button to open the Encumbrance Password Setup window.
3. If you’re setting up the password for the first time, enter and confirm the password. 
4. If you’re modifying the password, enter the existing password, and then enter and confirm the new password.
5. Choose OK to save your changes and return to the Encumbrance Setup window and chose OK.

## Encumbrance statuses

When you first set up Encumbrance Management, all existing purchase order line items are evaluated. An encumbrance amount will be created using the required 
date on the purchase order line item. Also, receipts posted against that purchase order line item will have a liquidation created using the posting date of the receipt. 
Subsequent purchase order line items are evaluated when you enter them.

The following describes the Encumbrance Management statuses:

**Encumbered**
The purchase order line item is within the budget you set up (plus the tolerable range, if you’ve set up budget tolerances). Also, the status is 
encumbered if the budget has been exceeded, but the purchase has been authorized.

**Pre-Encumbered**
The purchase order line item is not within the budgeted amount (plus the tolerable range, if you’ve set up budget tolerances)

**Pre-Budget**
The purchase order has not been approved. This status allows encumbrance records to be created for the purchase order line item. 
Budgets aren’t affected because the purchase order hasn’t been approved. This status is used only if Workflow or purchase order approvals in 
Purchase Order Enhancements is being used. When the purchase order is approved and is within budget, the status will change from pre-budget to encumbered or pre-encumbered based on the 
settings you chose in the Encumbrance Setup window.

**Invalid**
The purchase order line item is missing information or information is not valid.

**Limbo**
The purchase order line item is not validated against the budget.

A purchase order line item is not considered valid under the following circumstances:
• The account number for the purchase order line item is a fixed or variable allocation account.
• The account number for the purchase order line item doesn’t exist.
• The required date for the purchase order line item is in a fiscal year that has not been set up.
• The required date for the purchase order line item doesn’t exist.
• No budget ID has been set up in Encumbrance Management for the fiscal year period the required date falls in.

If the purchase order line item meets the validation requirements and doesn’t exceed the budgeted amounts, the status will be set to Encumbered. Otherwise, the 
status will be set to pre-encumbered. If you’re using blanket or drop-ship blanket purchase orders, the control blanket line will have a status of Pre-Encumbered, 
regardless of the status amount

> [!NOTE]
> If the control blanket line for a purchase order is not valid, you can’t enter blanket line items for that purchase order.
> 

A receipt for an existing purchase order is not considered valid under the following circumstances:
• A posted receipt exists for a purchase order line item, but a Budget ID has not been setup in Encumbrance Management for the fiscal year of the receipt line 
item required date. 
• The receipt line item does not have an inventory account entered on it.
• The account on the receipt line item is an allocation account. 
• The receipt line item required date is missing.

# Control Account Management
Control Account Management allows you to redistribute payables and receivables control account balances automatically based on the segment ID of each account. 
You can create reports that display the balances for each segment, as well as printing a summary report that shows payables and receivables information for 
respective cost centers. In addition, payables and receivables reports can be more accurate because receiving journals are generated that redistribute the control 
account balances to predetermined segments, thereby reflecting the activity of specific areas of your business

## Control Account Setup
Use the information in this part of the documentation to learn more about installing and setting up Control Account Management. Control Account Management 
automatically is registered if Payables Management or Receivables Management are registered for your company.

**Overview of Control Account Management**

When you use Control Account Management, control accounts are redistributed based on the segment ID of each account. You can print reports and generate 
reversing entries that redistribute the control account balance to predetermined segments. Using Control Account Management makes it possible for you to print 
accurate month-end reports of payables and receivables based on account segments.

After your control accounts are set up, you can use Control Account Management to create reports that display the breakdown of your payables and receivables by fund, 
division, department, program, and so on—whatever cost center you decide to use as your account segment identifier.

Through Control Account Management, you can generate a reversing journal entry that distributes these amounts to your balance sheet using the transaction date that 
is specified in the Batch tab for this report. This journal entry breaks down your control account to give you an accurate snapshot of your company’s payables and 
receivables. At the same time, these distributions are reversed using the reversing date that’s specified in the Batch tab for this report, resetting the control account to 
its original state. 

You can obtain accurate financial statements, including the redistributed control accounts, as often as you like—monthly, quarterly, or annually. You also can 
redistribute amounts from the default control account to the various cost centers in your company, eliminating the need to manually reconcile reporting segments.

*Special accounting situations*

The information in this document is based on using Control Account Management with full payments, where the control account balances are distributed to the 
segments you specify, leaving the original document with a zero balance. However, when you use Control Account Management with partial payments, the payment 
amount will be tracked by Control Account Management in the segment that relates to the Cash account.

We recommend that you verify distributions before entering payments if you’re using manual payments or entering and paying invoices at the same time. 
Accounting anomalies can occur if transactions are recorded without the proper distributions.

## Setting up Control Account Management
You can use the Control Account Management Setup window to set up Control Account Management after you’ve installed it.

To set up Control Account Management:

1. Open the Control Account Management Setup window.(Microsoft Dynamics GP menu >> Tools >> Setup >> Financial >> Control Account Management)
2. In the Control Account Management Setup window, enter or select an account segment—the segment ID to use to analyze payables and receivables 
information.
3. Mark Activate Control Account Management. No Control Account Management transactions can be generated until the option is marked.
You can clear the option even after distributions have been processed, but doing so will 
prevent any further Control Account Management entries from being created.
4. To define the control accounts and settings for payables and receivables, choose Account Types. The Control Account Management Account Types window 
opens.
5. Select an account type: Payables or Receivables.
6. In the scrolling window’s Control Account column, enter or choose a control account to associate with the corresponding segment ID. The detail entered in 
the scrolling window applies to the specific account type that you have selected, either payables or receivables.

The Segment ID column displays the segment ID that corresponds to the  account segment you chose in the Control Account Management Setup 
window. The Account Description column displays that segment’s description.  If no description exists, you can enter one.

7. To generate reversing journal entries, set up default batch information.
8. 
Batch ID This is the default batch ID for all your Control Account Management transactions.
You can save only one Control Account Management batch at a time. That batch must be posted using the batch entry or series posting windows before you can enter another 
Control Account Management batch.

Batch Comment This comment is included on the Control Account Management batch.

Reference The reference is included in the Control Account Management 
transactions.

9. Choose Save to save your changes. Close the Control Account Management Account Types window.
10. Choose Save   


<!--## See also-->
