---
title: Encumbrance management
description: Learn about the Encumbrance Management capabilities in Dynamics GP.
keywords: 
author: theley502
ms.reviewer: jswymer
ms.topic: article
ms.author: theley
ms.date: 07/23/2024
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

## Transactions
This part of the documentation describes how to work with encumbrances, including how to create them and how they’re affected by purchase order changes. 
This information also explains how to authorize groups of pre-encumbrances, which are encumbrances that exceed the budget limits and haven’t been authorized.

When you create purchase orders using the Purchase Order Entry window, encumbrances automatically are created. They’re authorized automatically if the 
purchase order line items fit the budget requirements, and can be authorized manually if they’re outside budget requirements. To meet the budget requirements, 
the result of the following formula must be positive:

Budget Amount - Actual Amount - Encumbrance Amount

Purchases are associated with a budget based on the posting account on the purchase order line item, and the fiscal period that the required date on the 
purchase order falls within.

For example, if an annual budget is set at $10,000 and a purchase order line item is created for $2,000, the available budget amount would be reduced to $8,000. 
A new purchase order line item for $8,500 would exceed the budget and require authorization. (This assumes that no budget tolerances have been set up.)

The amount that is encumbered is calculated using the following formula:
(Quantity Ordered - Quantity Canceled - Quantity Shipped) * Unit Cost in the Functional Currency

When you receive a shipment, the encumbrance amount is reduced, or liquidated. However, the Actual amount is increased at the same time so that the available 
budget amount remains the same. If the quantity received is the same as or more than the quantity encumbered, the encumbered amount is liquidated to zero. 
Encumbrances are liquidated in the period of the posting date of the receipt.

Encumbrance amounts also are liquidated if you cancel a purchase order line item or close a purchase order. 

## Calculating available budget amounts for dimension codes using budget trees
Budget trees are used in Analytical Accounting; the calculations for available budget amounts described in this section do not apply if you’re tracking 
encumbrance amounts against General Ledger budgets. 

When a purchase order is posted, budget amounts are verified for each branch in the budget tree structure, for each purchase order line. If there are multiple branches 
on a purchase order line and one of the branches is over budget, the status for all the branches for that line will be set to Pre-encumbered. You must either approve the 
over-budget amount or adjust the budget. Items cannot be received against a purchase order unless it is encumbered.

Budget amounts for the top level of the budget tree are not validated because no dimension codes are associated with this level of the tree. 

Purchase order line items are not validated against the budget and are instead given the special Encumbrance status Limbo. For the Analytical Account entry for the 
purchase order: 
• You do not enter dimension codes.
• When using Grant budget validation, the dimension code that you enter is not linked to a grant

## Purchase order types and liquidation

In addition to creating encumbrances for standard purchase orders, you also can create encumbrances for drop-ship, blanket, and drop-ship blanket purchase orders. 
The following briefly describes each purchase order type and explains when the purchase orders are liquidated.

| Type      | Description                                        | When liquidated                                                    |
|--------------------------------------------------------------- |--------------------------------------------------------------------|
| Standard  | Lists items that will be shipped to your business  |The purchase is liquidated when a shipment/invoice receipt is posted|
|              to be received into your inventory                |                                                                    |
| Drop-Ship | Used for items you purchase on behalf of a customer|The purchase is liquidated when an invoice is posted                |
|              The items are shipped to the customer without     |                                                                    |   
|              being physically received into your inventory     |                                                                    |
| Blanket   | Lists a single item and its quantities that will   |The control blanket line itemm is liquidated by creating blanket    |
|              be delivered in a series of shipments. The item   |Line items.  These items are liquidated when a shipment/invoice     |
|              will be received into your inventory              |receipt is posted.                                                  |   
| Drop-Ship | Is a combination of drop-ship & blanket purchase   |The cotrol blanket line item is liequidated by creating blanket line|
|  Blanket     orders; lists a single item & the quantities      |items. The blanket line items are liquidated when an invoice receipt|
|               that will be delivered to the customer in series |is posted.                                                          |

## Control blanket line items and encumbrances

The first line item entered for a blanket or drop-ship blanket purchase order is called the control blanket line item. This line item has a line number of 0 (zero) and 
is the line item that the blanket line items are based on. The control blanket line item is not affected by creating or posting receipts.

For example, you might enter a quantity of 5,000 for the control blanket line item and then enter five blanket line items with a quantity of 1,000 each. The control 
blanket line item isn’t included in tax amounts or the purchase order’s subtotal, nor is it printed on purchase orders. 

When you use Encumbrance Management with blanket and drop-ship blanket purchase orders, the control blanket line item is always pre-encumbered, even if it 
doesn’t exceed the budgeted amount. A message is displayed if this line item amount exceeds the budgeted amount. The line item amount is included in the 
budget validation calculations, and the funds for this line item are reserved in the budget.

The control blanket line item amount is reduced only when blanket line items are created. Blanket purchase orders can be controlled by either the quantity or the
value of the control blanket line item. The calculation of the reduction of the control blanket line item depends on this setting.

Quantity - The reduction is for the quantity of the blanket line item, using the unit cost of the control blanket line item.
Value  - The reduction is for the value of the blanket line item.

## Creating an encumbrance for a standard or drop-ship purchase order

Use the Purchase Order Entry window to create and authorize encumbrances for standard and drop-ship purchase orders. A standard purchase order lists items that 
will be shipped to your business to be received into your inventory. A drop-ship purchase order lists items that will be shipped directly to the customer.

1. Open the Purchase Order Entry window. (Transactions >> Purchasing >> Purchase Order Entry)
2. Select Standard or Drop-Ship as the purchase order type.
3. Enter the purchase order. See the Purchase Order Processing documentation for more information. 
If any line items exceed the available budgeted amount, a message will be displayed asking if you want to encumber the purchase. You must enter a 
password, if one was set up.

If you change the information in the Quantity Ordered, Quantity Canceled, or Unit Cost fields for a line item, the line is validated again. 

5. Choose Save and close the window. You will have the option to print an edit list. 
You can choose File >> Print or the Print icon, or use the Print Purchasing Documents window, to print the purchase order if all lines have a status of 
Encumbered.

## Creating an encumbrance for a blanket or drop-ship blanket purchase order
Use the Purchase Order Entry window to create and authorize encumbrances for blanket and drop-ship blanket purchase orders. A blanket purchase order lists a 
single item and the quantities that will be delivered in a series of shipments, usually on a specific date. A drop-ship blanket purchase order lists a single item and the 
quantities that will be delivered directly to the customer in a series of shipments, usually on multiple dates that are specified in advance.

1. Open the Purchase Order Entry window. (Transactions >> Purchasing >> Purchase Order Entry)
2. Select Blanket or Drop-Ship Blanket as the purchase order type.
3. Enter the purchase order. See the Purchase Order Processing documentation for more information.
If any line items exceed the available budgeted amount, a message will be displayed asking if you want to encumber the purchase. 
You must enter a password, if one was set up.

If you change the information in the Quantity Ordered, Quantity Canceled, or Unit Cost fields for a line item, the line is validated. You can’t add item 
information to a purchase order if the control blanket line item has a status of Invalid. 

You can’t change the unit of measure for the control blanket line item if you’ve already entered a blanket line item in the scrolling window. You must delete the line item before 
changing the unit of measure. However, you can change the unit of measure on the blanket line items.

4. You can choose Blanket to open the Purchasing Blanket Detail Entry window, where you can enter several blanket line items at once.
5. Mark a Control Blanket By option. This option affects how the control blanket line item is liquidated.
   
You can’t change the Control Blanket By option if you’ve already entered a blanket line item in the scrolling window. You must delete the line item before changing the option.

7. Enter the blanket line item information.
8. Choose OK to return to the Purchase Order Entry window.
9. Choose Save and close the window. You will have the option to print an edit list. 
You can choose File >> Print or the Print icon, or use the Print Purchasing Documents window, to print the purchase order for all lines that have been 
released using the Purchasing Blanket Detail Entry window and have a status of Encumbered.

## How purchase order changes affect encumbrance amounts
The following describes how encumbrance amounts are affected when you modify, delete, or void purchase orders, or change the status of a purchase order.

*Modify a purchase order*
The encumbrance amount is recalculated and re-evaluated against the budget.

*Delete a line item/ blanket line item*
The current encumbrance information for that line item is removed.
For the control blanket line item in blanket and drop ship blanket purchase orders, the encumbrance amount for the control blanket line item is increased.

*Delete a purchase order*
The current encumbrance amount for all items is removed.

*Void a purchase order*
The current encumbrance amount for all items is removed.

*Change the purchase order status to Closed, Received, or Canceled*
Any pre-encumbered or encumbered amounts are removed.

*Change the purchase order status from Canceled to Change Order, New or Released*
The encumbrance amount is recalculated and re-evaluated against the budget.

*Change the purchase order status from New to Released*
The encumbrance amount does not change.

## Encumbrance liquidations

Some actions reduce, or liquidate, encumbrances. A liquidation is a reduction in the encumbered amount due to posting a receipt, closing or canceling a purchase order 
or line item, or reducing the quantity ordered or unit cost of the purchase order line item.

*Closed or canceled purchase orders*
When you close or cancel a purchase order, encumbrance amounts for that purchase order also are updated:
• If you close a purchase order, the remaining encumbrance amount for all line items in the purchase order will be reduced to zero.
• If you cancel a purchase order line item, the encumbrance amount will be reduced by the amount canceled.

*Receivings transactions*
For standard and blanket purchase orders, when you post a shipment receipt or shipment/invoice receipt, the encumbered amount for the received goods is 
reduced by the quantity received using the posting date of the receipt. The posting date must be within a period of a budget selected in the Encumbrance Setup 
window. The liquidation uses the unit cost of the purchase order line item.

For drop-ship and drop-ship blanket purchase orders, when you post an invoice receipt, the encumbered amount for the invoiced goods is reduced by the quantity 
invoiced using the posting date of the invoice. The liquidation uses the unit cost of the purchase order line item

When a shipment is posted, the actual amount is increased for the purchase orders for the general ledger account, the dimension code, or both. For this reason, the encumbrance on the 
general ledger account is liquidated when the goods are shipped, and not when the payment is made to the vendor.

If the quantity received is equal to or greater than the quantity encumbered for that line item, the encumbered amount will be reduced to zero.
If you’re using blanket or drop-ship blanket purchase orders, the liquidation works the same except for the control blanket line item, which is reduced by entering 
blanket line items.

When you save a receivings transaction to a batch, encumbrances are not liquidated until the batch is posted.

*Authorizing pre-encumbrances for multiple purchase orders*
Use the Mass Encumbrance window to authorize pre-encumbrances for multiple purchases at one time. For example, suppose you supervise a user who doesn’t have 
the authority to approve purchases that exceed the budget. You might use this window to review those pre-encumbrances and authorize them.

If you’re using blanket or drop-ship blanket purchase orders, the control blanket line item won’t be displayed with the pre-encumbered purchase orders because you 
can’t encumber the control blanket line item. 

You also can use the Mass Encumbrance window to view invalid purchase order line items, which must be modified before they can become encumbered.

To authorize pre-encumbrances for multiple purchase orders:
1. Open the Mass Encumbrance window. (Transactions >> Purchasing >> Encumbrance Management >> Mass Encumbrance)
2. Select Pre-Encumbered as the encumber status.
3. Select a range of pre-encumbrances.

• To encumber all available pre-encumbrances, set the range to All Available.
• To restrict the range of pre-encumbrances, select a range restriction based on PO Number, Vendor ID, or Created By, and enter a range of purchase 
order numbers, vendors, or users in the From and To fields. Choose Redisplay. The applicable purchase order line items will be displayed in the 
scrolling window.

4. In the Encumber column, mark the purchase order line items to authorize. You can mark individual lines, or choose Mark All to mark all the lines displayed in 
the window.

If you change the Ranges field in this window after marking any purchase order line items, those lines will remain marked even though they are no longer visible in the 
window. You must redisplay your previous range to view those lines.

5. You can print an edit list by choosing File >> Print or the Print icon. An edit list itemizes the purchase order line items that will be encumbered.
6. Choose Encumber. A message is displayed asking if you want to continue. Choose Yes. You’ll need to enter a password if one was set up.
7. Close the window. You will have the option to print the Encumbrance Audit Report showing the purchase order line items that have been encumbered

*Transferring encumbrance amounts at year end*
Use the Year End Encumbrance Transfer window to transfer encumbrance amounts from a fiscal year that’s ending to the next fiscal year. 

1. Open the Year End Encumbrance Transfer window: (Microsoft Dynamics GP menu >> Tools >> Routines >> Purchasing >> Year End Encumbrance Transfer)
2. Enter or select the year that you’re transferring encumbrance amounts from. 
3. Enter a range of purchase order numbers to transfer encumbrance information for.
4. Select to increase budget amounts for the encumbrances that you’re transferring. If the budget for the fiscal year that you’re transferring 
encumbrance information to doesn’t include the funding for items that were ordered and encumbered in the previous year, you can increase those budgets 
by the amount being transferred. If you choose to increase budget amounts, you also can increase budget amounts for pre-encumbered items. 

When the budget ID is the same for both years (the year that you’re transferring amounts from and the year that you’re transferring amounts to) and the 
Increase corresponding budget amounts option is marked, increasing an amount for the new fiscal year results in an equal decrease for the year you’re 
transferring from.

5. Choose Preview to view a report that shows transfer information without actually changing budgets or account balances. 
The encumbrance transfer updates the required date on each purchase order line item to the first day of the new fiscal year. 
6. Choose Transfer to transfer encumbrance information to a new fiscal year.

## Encumbrance Management maintenance
This part of the documentation describes the data tables that are included with Encumbrance Management and explains how to verify and repair Encumbrance 
Management data inconsistencies.

You can use the Encumbrance Routine Maintenance window to verify and repair Encumbrance Management data inconsistencies.
1. Open the Encumbrance Routine Maintenance window. (Microsoft Dynamics GP menu >> Maintenance >> Encumbrance Management >> Routine Maintenance)
2. Select an operation to complete.

Verify: Detail versus purchase order
Compares the encumbrance totals in the Encumbrance Purchase Order Line and Encumbrance Purchase Order 
Line Changes tables to the encumbrance totals calculated using the purchase order table and posted receipts.

Verify: Summary versus Detail 
Compares the encumbrance totals in the Encumbrance Purchase Order Line Changes table to the encumbrances totals in 
the budget table (GL002001).

Repair: Detail based on Purchase Order 
If purchase orders in the Encumbrance Purchase Order Line and Encumbrance Purchase Order Line Changes tables do not equal the encumbrance totals calculated using the 
purchase order table and posting receipts, any existing records are deleted and recreated using the required date on the purchase order line and the posting 
date on the receipts.

Repair: 
Summary based on Detail If the encumbrance budget totals for an account where the encumbrance totals in the Encumbrance Purchase Order 
Line Changes encumbrance table does not match the encumbrances totals in the budget table (GL002001), the encumbrance budget record for that account is 
deleted and recalculated using the total for that account in the Encumbrance Purchase Order Line Changes table.
3. Choose Process. A message will be displayed when the verification or repair has been completed.
4. Choose OK to close the message window.
5. Choose OK to close the Encumbrance Routine Maintenance window

**Data Tables**

ENC_POLine  / ENC10110 -Encumbrance Purchase Order Line
Holds current purchase order line information, including encumbrance status, amount, and purchase order line status.

ENC_POLineChg / ENC10111 -Encumbrance Purchase Order Line Changes
Holds any changes made to current purchase order line items, such as quantity, unit cost, and inventory amount.

ENC_POLineEntry / ENC10115 -Encumbrance Management PO Line Entry
Activity tables hold information about encumbered purchase order line items for each user; used primarily for printing the Audit Report 
upon closing of the Purchase Order Entry window.

ENC_PORcptApply / ENC10500 -Encumbrance Received Transactions
Tracks posted receipts (liquidations).

ENC_Setup / ENC40000 -Encumbrance Setup Holds encumbrance activation status, variance amount, type of validation (Annual, Period, Year-To-Date), and password.

ENC_SetupLine / ENC40100 -Encumbrance Budget Setup
Holds budgets that have been set up in Encumbrance Management

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

Batch ID 
This is the default batch ID for all your Control Account Management transactions.
You can save only one Control Account Management batch at a time. That batch must be posted using the batch entry or series posting windows before you can enter another 
Control Account Management batch.

Batch Comment 
This comment is included on the Control Account Management batch.

Reference 
The reference is included in the Control Account Management transactions.

8. Choose Save to save your changes. Close the Control Account Management Account Types window.

## Transactions and reports

After you’ve set up Control Account Management by specifying your main account segment and the control account to be used for each account within that segment, 
you must create reports and generate reversing transactions to create your control account distributions for both receivables and payables.

Before you run your month-end reports, you must create your report using the Generate Control Account Management Transactions window and then generate 
the reversing journal entry to redistribute the total amount to the control accounts specified in the setup window. You have full control of the dates of both the journal 
entry and the reversing journal entry. This process generates a batch that you will need to post, just as other Microsoft Dynamics GP journal entries are posted

**Printing a Control Account Management report**

Use the Generate Control Account Management Transactions window to print summary or detail reports.
You also can use the window to generate reversing journal entries.  

To a print a Control Account Management report:
1. Open the Generate Control Account Management Transactions window.
(Transactions >> Financial >> Control Account Management)
2. Choose Payables or Receivables.
3. Choose Report to generate a Control Account Management report.
4. To see more information that is included on the report, choose the Show Details button.
5. To print the report, choose Save, and then choose the Print icon. (You can’t print reports that haven’t been saved.)
6. When you’ve finished, close the window

**Batches for Control Account Management**

Batches that are generated when you use Control Account Management must be posted, just as other Microsoft Dynamics GP journal entries are posted.

When you set up Control Account Management, you specify a batch ID for Control Account Management. You can use that default batch ID each time you generate a 
Control Account Management journal entry, or you can use the Batch tab in the Generate Control Account Management Transactions window to modify the default 
information. Any information that you enter in the Batch tab will override the default batch information you entered during the setup procedure.

After a batch of transactions has been created, you can post it using batch entry or series posting windows.

> [!NOTE]
> We recommend that you use the default batch ID each time you post, so only one Control Account Management batch is in use at any time. If you prefer, you can enter a new batch 
> ID in the Batch tab for each report, and Control Account Management will create an additional batch for each report. However, if you enter multiple batch IDs, you must keep 
> track of your Control Account Management batches to ensure that you do not post a batch containing the same information twice.
> 

**Generating reversing journal entries**

The Generate Control Account Management Transactions window generates  reversing journal entries for your transactions. You have full control of the dates of 
both the journal entry and the reversing journal entry. This process generates a batch that you will need to post.

1. Open the Generate Control Account Management Transactions window. (Transactions >> Financial >> Control Account Management)
2. Choose Payables or Receivables.
3. Choose Report to generate a Control Account Management report.
4. Choose the Show Details button. Supporting information for the report is displayed in each of the three tabs in the window. 
5. Before you generate the journal entry, be sure to verify or change the transaction date and revision date, and other journal entry information.
6. Choose Generate to create a journal entry that redistributes the total default control account balance to the predetermined segments.

A reversing journal entry automatically will be created using the default batch ID from the Control Account Management Setup window, or from the Batch tab 
if you made modifications to the default information.

When you generate a journal entry, the report is saved automatically.

7. After the reversing journal entry is created, you must post it using the batch entry or series posting windows before you can save another Control Account 
Management batch.  When you’ve finished, close the window


<!--## See also-->
