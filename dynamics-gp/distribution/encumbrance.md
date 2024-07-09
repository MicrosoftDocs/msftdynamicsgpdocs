---
title: Encumbrance management
description:
keywords: 
author: theley502
manager: jswymer
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 07/09/2024
---

# Encumbrance Management
Encumbrance Management enables you to reserve funds from a budget when purchase orders are created. You can create encumbrances for standard, drop-ship, blanket, and drop-ship blanket orders. You can authorize multiple encumbrances at one time, and set up passwords that verify authorization to exceed budget amounts. In addition, you view inquiries and reports that show encumbrances against budget amounts as well as displaying information in detail or summary formats for actual versus budgeted amounts.

## Recent updates with Encumbrance Management

[Encumbrance Year-End Transfer or the Encumbrance reconcile routine data issues](https://community.dynamics.com/blogs/post/?postid=70bb2e70-82e6-4049-a3aa-b5a1b8a9afc0)
[Encumbrance Management and Blanket Purchase Orders](https://community.dynamics.com/blogs/post/?postid=3b463b0a-ce74-4663-9fdd-ab8956d69c7f)
[Error: You can’t transfer encumbrances for XXXX when there are outstanding encumbrance amounts for a prior fiscal year.](https://community.dynamics.com/blogs/post/?postid=a59bf1e9-7e94-4fbe-8b96-4e4508fcc715
[Error: You can’t transfer encumbrances for XXXX when there are outstanding encumbrance amounts for a prior fiscal year.](https://github.com/theley502/msftdynamicsgpdocs/assets/43243051/59b7022d-e846-4144-8f34-72d9bb2ae8fd)
[Encumbrance Summary Inquiry Amounts Do Not Match Detail in Microsoft Dynamics GP](https://community.dynamics.com/blogs/post/?postid=ee1f1afc-6c4b-48eb-b242-24ba8577698f)
[How to use Encumbrance and Approvals together successfully](https://community.dynamics.com/blogs/post/?postid=a5e474e8-bc64-4316-924f-b3f98dad023a)
[Microsoft Dynamics- Purchase Order Processing/Encumbrance](https://community.dynamics.com/blogs/post/?postid=faefd3c7-0068-4e5e-a5d6-4a168221ee51)
[Information regarding Encumbrance and Blanket Purchase orders]https://community.dynamics.com/blogs/post/?postid=85ee2dfc-bd4c-4c06-8798-00cb58160210)
[Microsoft Dynamics GP Encumbrance Year End Transfer Error](https://community.dynamics.com/blogs/post/?postid=3e311f09-b974-4b1a-8e9e-ec03ced203a8)
[Errors seen in Purchase Order Processing when Encumbrance Management and Requisition Management are installed](https://community.dynamics.com/blogs/post/?postid=e16c0e9d-cd66-4ccb-8b31-985b3c83f7b2)

## Encumbrance Setup

An encumbrance is a purchase that affects budgets because it is an obligation for goods, materials, and services that have been ordered but not received. 
When you set up Encumbrance Management, any existing purchase order line items in Microsoft Dynamics GP are evaluated. Each valid purchase order line item 
is assigned a status of Encumbered. Subsequent purchase order line items will be evaluated when you enter them. The budget that’s encumbered is the budget that 
includes the period of the required date for a purchase line item.

When you set up Encumbrance Management, you select the budget that will be encumbered for the amount of purchases. Any type of budget can be selected: 
General Ledger, Analytical Accounting, or Grant budgets.
You can enter a budget tolerance to limit the acceptable variance when a purchase transaction exceeds the available budget. You can set up a password to require 
authorization before the purchase order is sent to the vendor. Also, you can select what actions occur when a purchase order is approved.

**Prerequisites for using General Ledger budgets**
To use General Ledger budgets with Encumbrance Management, you must set up budgets in General Ledger for each period of each open year.
Prerequisites for using Analytical Accounting budgets
To use Analytical Accounting budgets with Encumbrance Management, you must 
complete the following steps to cover each period of each open year with a budget. 
• Create one or more budget trees.
• Set up dimension codes and assign a dimension code tree to a budget tree.
• Create a budget and assign a budget tree to that budget (you can assign the same budget tree to multiple budgets)

**Prerequisites for using Grant budgets**
Grant Budgets are actually Analytical Accounting budgets that are linked to a grant. 
The steps for using Grant budgets for Encumbrance Management are similar to the steps for using Analytical Accounting budgets, with the following exception. You 
must use Grant Management to associate a grant with a dimension code in an Analytical Accounting budget.

After you save your changes in the Encumbrance Setup window, all existing purchase order line items are evaluated. An encumbrance amount is created using 
the required date on the purchase order line item, and receipts posted against that purchase order line item will have a liquidation that’s created using the posting 
date of the receipt. 

**To set up Encumbrance Management:**
1. Open the Encumbrance Setup window.
(Microsoft Dynamics GP menu >> Tools >> Setup >> Purchasing >>Encumbrance Management)

2. Mark Enable Encumbrance Management. This option must be marked to use 
Encumbrance Management, and to make the other fields in the window available.

3. Select a budget type. Available budget types include General Ledger, Analytical Accounting, or Grant budgets. 
You can specify a budget tree when Analytical Accounting Budgets is the selected budget type. 

If you’re using Fiscal Year as 
the tracking method, you must specify a budget tree.

If the selected budget type is Grant Budgets, purchase order line items will be 
encumbered when you enter transactions for the grant that’s assigned to the corresponding budget in Grant Management. 

4. Mark a tracking method for your encumbrances. 
The tracking method determines how the budget amounts and the purchase order amounts (plus 
actual amounts) are compared to each other.

*Total Budget*
Purchases are compared to the total budget and total actual amounts for that budget.

*Period*
Purchases are compared to the budget and actual amounts for the period of the purchase.

*Budget-To-Date*
Purchases are compared to the budget and actual amounts in the range from the starting date for the budget to the end of the period of the 
required date on the purchase order. 

*Fiscal Year*
Purchases are compared to the total budget and total actual amounts for the fiscal year specified in the required date on the purchase order. 

If you are using Analytical Budgets and you select Fiscal Year as the tracking method, you must specify a budget tree to use in validating purchases. 

If you use blanket purchase orders, we recommend that you use the Total Budget tracking method to help ensure that budgets are not unexpectedly exceeded.

5. To set up a password for authorizations of purchase order amounts that exceed the budget limits, choose Enter/Change Password to open the Encumbrance 
Password Setup window. 

6. Select a tolerance level type and enter an acceptable amount or percentage that a purchase may vary from the available budget before authorization is required.
You can enter either a positive or negative budget tolerance level—an amount or percentage that a purchase is allowed to deviate from a budget without 
requiring authorization. 

7. If you’re using General Ledger or Analytical Accounting budgets, in the 
scrolling window, enter or select the budget IDs that purchases should be 
compared to.

None of the periods within any of the budgets that you select may overlap. For 
example, if Budget A spans June 2016 through May 2017 and Budget B spans 
May 2017 through May 2018, you won’t be able to select both budget A and B 
because they contain overlapping periods. 

8. If you’re using Analytical Accounting budgets, choose to validate budgets by 
account or node in a budget tree. Choosing Node causes the budgets to be 
validated by a combination of dimension codes from Analytical Accounting. 
Choosing Account causes the budgets to be validated by a combination of 
accounts and dimension codes. 

9. If you are using Workflow or purchase order approvals in Purchase Order 
Enhancements, select an option for how approved purchase orders are 
encumbered.

*Ask when over budget*
Encumbers any purchase order lines that are under budget. Displays a message for lines that are over budget with the option to 
encumber those lines or leave them pre-encumbered. Choose this option when If you enter a positive value If you enter a negative value
Amount Purchases can exceed the budget amount by the currency amount you specify.

*Always pre-encumber*
Pre-encumbers all purchase order lines, regardless of their budget status. With this option, the Mass Encumbrance window is used 
to do all validations against the budget.

*Pre-encumber*
When over budget Encumbers any purchase order lines that are under budget and pre-encumbers lines that are over budget. Choose 
this option when different people have authority to approve the purchase order 
and over-expenditures to the budget. In this scenario, the Mass Encumbrance 
window is used to approve the over-expenditures to the budget.

10. Choose OK to save your changes and close the Encumbrance Setup window.
If you have existing purchase orders or receipts in your system, all purchase 
order line items and receipts are verified. If the purchase order or receipt is 
valid, the purchase order is encumbered, even if it exceeds the budget amount. 


## See also
