---
title: "Accounts used in Manufacturing"
description: "Get an overview of the accounts that are used in the Manufacturing module in Dynamics GP."
keywords: "manufaturing"
author: theley502
manager: jswymer
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 06/19/2020
---

# Accounts Used for Manufacturing in Dynamics GP

This article describes the accounts that are used in the Manufacturing module in Dynamics GP. For information about setting up the module, see [Manufacturing Setup - Part 1: Manufacturing setup](manufacturing-setup-part-1.md) and [Manufacturing Setup - Part 2: User setup](manufacturing-setup-part-2.md).  

## Manufacturing Inventory and General Ledger Transactions General

### Where to set up Manufacturing Accounts

Account numbers for both actual and standard cost items and are set in the Item Account Maintenance window. To open the Item Account Maintenance window go to Cards> Inventory > Item and then click the Account button.  Two windows will open:  

- Item Account Maintenance  
- Item Account Maintenance – Costing  

The top window is the core accounts for Great Plains for Items. The 2nd window below the Item Account Maintenance window is for Manufacturing.  This is the Item Account Maintenance – Costing window.

### What Accounts need to be setup for Manufacturing

This is dependent on the type of costing used.

- Actual Costing Accounts

    Accounts that are used for actual cost item transactions in manufacturing are:
        - Inventory (for most transaction)
        - Inventory Offset (for inventory adjustments, receiving)  
        - Cost Of Goods Sold (for sales invoices)
        - Sales Returns (for sales returns)
        - WIP (for MO close of issued/back flushed components of made items)
        - Variance Material (for potential labor, machine and material variances)

- Standard Costing Accounts

  Account Numbers for standard cost items are set in the Item Account Maintenance Costing window. Accounts that are used for standard cost item transaction in manufacturing are:

  - Standard Cost Revaluation Account (for standard cost revaluation function)
  - Applied – Material overhead Accounts (for receiving – BUY items)
  - Variance Accounts (for variances during MO Close – MAKE items)
  - WIP Accounts (for issue/backflush of materials- MAKE items)
  - COGS Accounts (for sales invoices – sold items)
  - Inventory Accounts (for inventory adjustments, transfers, issue of materials, MO close – all items)
  - Accounts Required for both Actual and Standard Costing Items

Additional accounts necessary for both actual and standard costing are the labor and machine setup accounts, the rounding difference account, and the accrued purchases account.

- Labor applied accounts can be set in the Labor Code Definition window.  
     To open the window go to Cards > Manufacturing > Labor Codes.
- Machine applied accounts can be set in the Machine Definition window. 
     To open the window go to Cards > Manufacturing > Machines.
- The Rounding Difference account can be set in the Costing Preference Defaults window.  
    To open the window go to Tool > Setup > Manufacturing > System Defaults > Costing.
- Accrued Purchases account can be set under the Vendor Account Maintenance window. 
    To open the window go to Cards > Purchasing > Vendor > Account.

### How will the Cost be Determined

- Actual items cost used

    Actual cost items have a perpetual valuation method.  The last cost received for an item can be found in the Current Cost field on the Item Maintenance window. To open the Item Maintenance window go to Cards > Inventory > Item.  The actual costs will be used when items are removed from inventory. The actual costs for each item are located in the Purchase receipts table (IV10200).  You can view these costs by printing the Purchase Receipts report under Report > Inventory > Activity > Purchase Receipts.  The costs that the system will use are based on the Perpetual valuation method selected (FIFO vs. LIFO) and will it will pull out the cost of the IV Purchase receipts table when posted.

- Standard cost items cost used

  Standard Cost items have a periodic valuation method.  The “total” cost for these types of items can be found in the Standard Cost field in the Item Maintenance window.  The “broken out” costs for these types of items can be found on the Standard Cost changes window located under Cards > Manufacturing > Inventory > Standard Cost Changes. The “broken out” costs are used for the GL transactions of standard cost items.

  The “broken out’ costs are:

  - Material
  - Material Fixed Overhead
  - Material Variable Overhead
  - Labor
  - Labor Fixed Overhead
  - Labor Variable Overhead
  - Machine
  - Machine Fixed Overhead
  - Machine Variable Overhead  

## General Ledger Transactions

General Ledger transactions are created in many areas of manufacturing and also from inventory transaction in Dynamics GP. Listed below are the areas where the transactions originated and also detailed information about the transaction.  This information includes what accounts are used, where the accounts are pulled from and what costs are used for the transaction.

Inventory Adjustment

Transactions > Inventory > Transaction Entry
Audit Trail Code example: IVADJ0000000000123

Actual Cost Items

Actual Cost Item Accounts and Costs during Inventory Adjustments

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory (Item Account Maintenance)       | Current Cost       |
| CR        | Inventory Offset(Item Account Maintenance) | Current Cost       |

Example of Accounts and Costs used during an Inventory Adjustment for an actual BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.00              |
| CR        | Inventory Offset                           | $4.00              |

Example of Accounts and Costs used during an Inventory Adjustment for an actual MAKE item	

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $5.56              |
| CR        | Inventory Offset                           | $5.56              |

Standard Cost Items
Standard Cost Item Accounts and Costs during an Inventory Adjustment  

| **DR/CR** | **Account**                                | **Cost Used**                  |
|-----------|--------------------------------------------|------------------------------  |
| DR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| DR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| DR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| DR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| DR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| DR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| DR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| CR        | Inventory Offset(Item Acct Maintenance)    | Total Standard Cost            |
| DR/CR     | Rounding Account(Cost Preferences Default) | Rounding Difference            |

Example of Accounts and Costs used during an Inventory Adjustment for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $3.35              |
| DR        | Inventory – Material Fixed Overhead        | $ .50              |
| DR        | Inventory – Material Variable Overhead     | $ .15              |
| CR        | Inventory Offset                           | $4.00              |

Example of Accounts and Costs used for an Inventory Adjustment for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.10              |
| DR        | Inventory – Material Fixed Overhead        | $ .55              |
| DR        | Inventory – Material Variable Overhead     | $ .35              |
| DR        | Inventory – Labor                          | $ .27              |
| DR        | Inventory – Labor Fixed Overhead           | $ .02              |
| DR        | Inventory – Labor Variable Overhead        | $ .01              |
| DR        | Inventory – Machine                        | $ .43              |
| DR        | Inventory – Machine Fixed Overhead         | $ .10              |
| DR        | Inventory – Machine Variable Overhead      | $ .12              |
| CR        | Inventory Offset                           | $5.95              |

Inventory Transfer

Transactions -> Inventory -> Transfer Entry
Audit Trail Code example: IVFR000000123

Actual Cost Items

Actual Cost item Accounts and Costs used during an Inventory Transfer 

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory (Item Account Maintenance)       | Current Cost       |
| CR        | Inventory (Item Account Maintenance)       | Current Cost       |

Example of Accounts and Costs used during an Inventory Transfer for an actual cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.00              |
| CR        | Inventory                                  | $4.00              |

Example of Accounts and Costs used during an Inventory Transfer for an actual cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $5.95              |
| CR        | Inventory                                  | $5.95              |

Standard Cost Items
Standard Cost Item Accounts and Costs used for Standard Cost items during an Item Transfer 

| **DR/CR** | **Account**                                | **Cost Used**                  |
|-----------|--------------------------------------------|------------------------------  |
| DR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| DR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| DR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| DR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| DR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| DR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| DR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| CR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| CR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| CR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| CR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| CR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| CR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| CR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| CR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| CR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| DR/CR     | Rounding Diff   (Cost Preferences Default) | Rounding Difference            |

Example of Accounts and Costs used during Item Transfer for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $3.35              |
| DR        | Inventory – Material Fixed Overhead        | $ .50              |
| DR        | Inventory – Material Variable Overhead     | $ .15              |
| CR        | Inventory                                  | $3.35              |
| CR        | Inventory – Material Fixed Overhead        | $ .50              |
| CR        | Inventory – Material Variable Overhead     | $ .15              |

Example of Accounts and Costs used during Item Transfer for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.10              |
| DR        | Inventory – Material Fixed Overhead        | $ .55              |
| DR        | Inventory – Material Variable Overhead     | $ .35              |
| DR        | Inventory – Labor                          | $ .27              |
| DR        | Inventory – Labor Fixed Overhead           | $ .02              |
| DR        | Inventory – Labor Variable Overhead        | $ .01              |
| DR        | Inventory – Machine                        | $ .43              |
| DR        | Inventory – Machine Fixed Overhead         | $ .10              |
| DR        | Inventory – Machine Variable Overhead      | $ .12              |
| CR        | Inventory                                  | $4.10              |
| CR        | Inventory – Material Fixed Overhead        | $ .55              |
| CR        | Inventory – Material Variable Overhead     | $ .35              |
| CR        | Inventory – Labor                          | $ .27              |
| CR        | Inventory – Labor Fixed Overhead           | $ .02              |
| CR        | Inventory – Labor Variable Overhead        | $ .01              |
| CR        | Inventory – Machine                        | $ .43              |
| CR        | Inventory – Machine Fixed Overhead         | $ .10              |
| CR        | Inventory – Machine Variable Overhead      | $ .12              |

Receiving Material Only in Purchase Order Processing
Transactions > Purchasing > Receivings Transaction Entry
Audit Trail Code example: RECVG000000123

Actual Cost items
Actual Cost Item Accounts and Costs used for during Receivings Transaction 

| **DR/CR** | **Account**                                | **Cost Used**                         |
|-----------|--------------------------------------------|---------------------------------------|
| DR        | Inventory (Item Account Maintenance)       | Receiving Cost (Item Vendor Maint.)   |
| CR        | Accrued Purchases(Vendor Acct Maint)       | Receiving Cost                        |


Example of Accounts and Costs used during a Receivings Transaction for an actual cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**   |
|-----------|--------------------------------------------|-----------------|
| DR        | Inventory (Item Account Maintenance)       | $4.32           |
| CR        | Accrued Purchases(Vendor Acct Maint)       | $4.32           |

Example of Accounts and Cost used during a Receivings Transaction for an actual cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**   |
|-----------|--------------------------------------------|-----------------|
| DR        | Inventory (Item Account Maintenance)       | $6.43           |
| CR        | Accrued Purchases(Vendor Acct Maint)       | $6.43           |

Standard Cost Items
Accounts and Cost used for Standard Cost item during Receivings Transaction 

| **DR/CR** | **Account**                                | **Cost Used**                  |
|-----------|--------------------------------------------|------------------------------  |
| DR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| DR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| DR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| DR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| DR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| DR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| DR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| DR/CR     | Unrealized PPV (Item Account Maintenance)  | Receiving Cost –Material Cost  |
| CR        | Accrued Purchases (Vendor Account Maint)   | Receiving Cost                 |
| CR        | Applied – Material Fixed Overhead          | Material Fixed Overhead Cost   |
| CR        | Applied – Material Variable Overhead       | Material Variable Overhead Cost|
| CR        | Applied – Labor (Labor Code Definitions )  | Labor Cost                     |
| CR        | Applied – Labor Fixed Overhead             | Labor Fixed Overhead Cost      |
| CR        | Applied – Labor Variable Overhead          | Labor Variable Overhead Cost   |
| CR        | Applied – Machine (Machine Definitions)    | Machine Cost                   |
| CR        | Applied – Machine Fixed Overhead           | Machine Fixed Overhead Cost    |
| CR        | Applied – Machine Variable Overhead        | Machine Variable Overhead Cost |

Example of Item Accounts and Costs used during a Receivings Transaction for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**       |
|-----------|--------------------------------------------|-------------------- |
| DR        | Inventory                                  | $3.35               |
| DR        | Inventory – Material Fixed Overhead        | $ .50               |
| DR        | Inventory – Material Variable Overhead     | $ .15               |
| DR/CR     | Unrealized PPV                             | $4.32 – $3.35 = $.97|
| CR        | Accrued Purchase                           | $4.32               |
| CR        | Applied – Material Fixed Overhead          | $ .50               |
| DR        | Applied – Material Variable Overhead       | $ .15               |

Example of Accounts and Costs used during a Receivings Transaction for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**       |
|-----------|--------------------------------------------|-------------------- |
| DR        | Inventory                                  | $5.05               |
| DR        | Inventory – Material Fixed Overhead        | $ .55               |
| DR        | Inventory – Material Variable Overhead     | $ .35               |
| DR        | Inventory – Labor                          | $ 5.00              |
| DR/CR     | Unrealized PPV                             | $6.43 –$5.05= $1.38 |
| CR        | Accrued Purchase                           | $6.43               |
| CR        | Applied – Labor                            | $ 5.00              |
| CR        | Applied – Material Fixed Overhead          | $ .55               |
| DR        | Applied – Material Variable Overhead       | $ .35               |


Enter/Match Invoice for Purchase Order
Transactions > Purchasing > Enter/Match Invoice
Audit Trail Code example: POINV000000123

Actual Cost Items
Actual Cost Item Accounts and Cost during Enter/Match Invoice (Invoicing)

| **DR/CR** | **Account**                                | **Cost Used**               |
|-----------|--------------------------------------------|-----------------------------|
| DR        | Accrued Purchases(Match Receiving Receipt) | Current Cost (Receipt cost) |
| DR/CR     | Purchase Price Variance(Item Acct Maint)   | Invoice Cost – Current Cost |
| CR        | Accounts Payable(Vendor Acct Maintenance)  | Invoice Cost                |

Example of Accounts and Costs used during an Invoicing Transaction for an actual cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**       |
|-----------|--------------------------------------------|-------------------- |
| DR        | Accrued Purchase                           | $4.32               |
| CR        | Purchase Price Variance                    | $4.22 –$ 4.32 =$ .10|
| CR        | Accounts Payable                           | $4.22               |

Example of Accounts and Costs used during an Invoicing Transaction for an actual cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**       |
|-----------|--------------------------------------------|-------------------- |
| DR        | Accrued Purchase                           | $6.43               |
| DR        | Purchase Price Variance                    | $6.52 –$ 6.43 =$ .09|
| CR        | Accounts Payable                           | $6.52               |

Standard Cost Items
Standard Cost Item Accounts and Costs used during Enter/Match Invoice (Invoicing)

| **DR/CR** | **Account**                             |**Cost Used**                                                                  |
|-----------|-----------------------------------------|-------------------------------------------------------------------------------|
| DR        | Accrued Purchases(Item Acct Maint)      |Receiving  Cost                                                                |
| DR/CR     | Purchase Price Variance(Item Acct Maint)|Invoice Cost – Standard Material Cost                                          |
| DR/CR     | Unrealized Purchase Price Variance      |Receiving Cost–(Total Strd Cost–(Material Fixed Ovrhd+Material Variable Ovrhd))|
| CR        | Accounts Payable(Vendor Acct Maint)     | Invoice Cost                                                                  |


Example of Accounts and Costs used during an PO Invoicing Transaction for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**                       |
|-----------|--------------------------------------------|------------------------------------ |
| DR        | Accrued Purchase                           |$4.32                                |
| DR        | Purchase Price Variance                    |$4.22 –$ 3.35 =$ .87                 |
| CR        | Unrealized Purchase Price Variance         |$4.32 ($4.00 – ($.50 + $.15)) = $.97 |
| CR        | Accounts Payable                           |$4.22                                |
 
Example of Accounts and Costs used during an PO Invoicing Transaction for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**                        |
|-----------|--------------------------------------------|------------------------------------  |
| DR        | Accrued Purchase                           | $6.43                                |
| DR        | Purchase Price Variance                    | $6.52 –$5.05 =$ 1.47                 |
| CR        | Unrealized Purchase Price Variance         | $6.43 ($5.95 – ($.55 + $.35)) = $1.38|
| CR        | Accounts Payable                           | $6.52                                |

Sales Order Invoicing
Transactions > Sales > Sales Transaction Entry
Audit Trail Code example SLSTE00000123

Actual Cost Items
Actual Cost Item Accounts and Costs used in Invoicing 

| **DR/CR** | **Account**                                | **Cost Used**            |
|-----------|--------------------------------------------|--------------------    |
| DR        | COGS - Material (Item Account Maintenance) | Current Cost * Quantity  |
| CR        | FG  Inventory (Item Account Maintenance)   | Current Cost * Quantity  |

Example of Accounts and Costs used during Invoicing for an actual cost finished good entry

| **DR/CR** | **Account**                                | **Cost Used**        |
|-----------|--------------------------------------------|--------------------  |
| DR        | COGS - Material (Item Account Maintenance) | $5.95 * 1 = $5.95    |
| CR        | FG  Inventory (Item Account Maintenance)   | $5.95 * 1 = $5.95    |

Regardless if you print the report or not, the system will split the costs into the 9 COGS buckets using the accounts on the item card.  

- If the COGS accounts are set up to pull from Item (Tools >Setup > Sales > Sales Order Processing) the system looks at the Item card's 9 buckets and pulls the appropriate COGS account.  

- If the COGS accounts are set up to pull from the customer (Tools > Setup > Sales >Sales Order Processing) there is only 1 COGS account on the Customer Card and not 9 buckets.  The material costs will be pulled into the COGS account on the customer card and the rest of the costs (labor and machine) are put into the remaining 8 buckets from the Item card’s COGS accounts.  

Standard Cost Item Accounts and Costs used during an Invoicing Transaction

| **DR/CR** | **Account**                                | **Cost Used**                             |
|-----------|--------------------------------------------|---------------------------------        |
| DR        | COGS - Material (Item Account Maintenance) | Material Cost * Quantity                  |
| DR        | COGS - Material Fixed Overhead             | Material Fixed Overhead Cost * Quantity   |
| DR        | COGS - Material Variable Overhead          | Material Variable Overhead Cost* Quantity |
| CR        | COGS - Labor (Item Account Maintenance)    | Labor Cost * Quantity                     |
| CR        | COGS - Labor Fixed Overhead                | Labor Fixed Overhead Cost * Quantity      |
| CR        | COGS - Labor Variable Overhead             | Labor Variable Overhead Cost* Quantity    |
| DR        | COGS - Machine (Item Account Maintenance)  | Machine Cost * Quantity                   |
| DR        | COGS - Machine Fixed Overhead              | Machine Fixed Overhead Cost * Quantity    |
| DR        | COGS - Machine Variable Overhead           | Machine Variable Overhead Cost* Quantity  |
| CR        | Inventory Material (Item Account Maint)    | Material Cost * Quantity                  |
| CR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost * Quantity   |
| CR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost* Quantity |
| DR        | Inventory - Labor (Item Account Maint)     | Labor Cost * Quantity                     |
| DR        | Inventory - Labor Fixed Overhead           | Labor Fixed Overhead Cost * Quantity      |
| DR        | Inventory - Labor Variable Overhead        | Labor Variable Overhead Cost* Quantity    |
| CR        | Inventory - Machine (Item Account Maint)   | Machine Cost * Quantity                   |
| CR        | Inventory - Machine Fixed Overhead         | Machine Fixed Overhead Cost * Quantity    |
| CR        | Inventory - Machine Variable Overhead      | Machine Variable Overhead Cost* Quantity  |

Example of Accounts and Costs used during Invoicing for a standard cost item where the quantity is 1

| **DR/CR** | **Account**                                | **Cost Used**                     |
|-----------|--------------------------------------------|---------------------------------  |
| DR        | COGS - Material (Item Account Maintenance) | $4.10 * 1 = $4.10                 |
| DR        | COGS - Material Fixed Overhead             | $.55 * 1 = $.55                   |
| DR        | COGS - Material Variable Overhead          | $.35 * 1 = $.35                   |
| CR        | COGS - Labor (Item Account Maintenance)    | $.27 * 1 = $.27                   |
| CR        | COGS - Labor Fixed Overhead                | $.02 * 1 = $.02                   |
| CR        | COGS - Labor Variable Overhead             | $.01 * 1 = $.01                   |
| DR        | COGS - Machine (Item Account Maintenance)  | $.43 * 1 = $.43                   |
| DR        | COGS - Machine Fixed Overhead              | $.10 * 1 = $.10                   |
| DR        | COGS - Machine Variable Overhead           | $.12 * 1 = $.12                   |
| CR        | Inventory Material (Item Account Maint)    | $4.10 * 1 = $4.10                 |
| CR        | Inventory – Material Fixed Overhead        | $.55 * 1 = $.55                   |
| CR        | Inventory – Material Variable Overhead     | $.35 * 1 = $.35                   |
| DR        | Inventory - Labor (Item Account Maint)     | $.27 * 1 = $.27                   |
| DR        | Inventory - Labor Fixed Overhead           | $.02 * 1 = $.02                   |
| DR        | Inventory - Labor Variable Overhead        | $.01 * 1 = $.01                   |
| CR        | Inventory - Machine (Item Account Maint)   | $.43 * 1 = $.43                   |
| CR        | Inventory - Machine Fixed Overhead         | $.10 * 1 = $.10                   |
| CR        | Inventory - Machine Variable Overhead      | $.12 * 1 = $.12                   |

Returns in Sales order Processing Transactions > Sales > Sales Transaction Entry
Audit Trail Code Example:  SLSTE00000123

Actual Cost Item Accounts and Costs used during a SOP Return 

| **DR/CR** | **Account**                                | **Cost Used**                      |
|-----------|--------------------------------------------|--------------------              |
| DR        | Inventory (Item Account Maintenance)       | Current Cost * Quantity            |
| CR        | COGS (Item Account Maintenance)            | Current Cost * Quantity (Material  |

Example of Accounts and Cost used during a SOP Return for an actual cost finished good item

| **DR/CR** | **Account**                                | **Cost Used**        |
|-----------|--------------------------------------------|--------------------  |
| DR        | Inventory                                  | $5.95 * 1 = $5.95    |
| CR        | COGS                                       | $5.95 * 1 = $5.95    |

Standard Cost Item Accounts and Costs used during a SOP Return for a finished good item

| **DR/CR** | **Account**                                | **Cost Used**                             |
|-----------|--------------------------------------------|---------------------------              |
| DR        | Inventory Item     (Item Account Maint)    | Material Cost * Quantity                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost * Quantity   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost* Quantity |
| CR        | Inventory - Labor (Item Account Maint)     | Labor Cost * Quantity                     |
| CR        | Inventory - Labor Fixed Overhead           | Labor Fixed Overhead Cost * Quantity      |
| CR        | Inventory - Labor Variable Overhead        | Labor Variable Overhead Cost* Quantity    |
| DR        | Inventory - Machine (Item Account Maint)   | Machine Cost * Quantity                   |
| DR        | Inventory - Machine Fixed Overhead         | Machine Fixed Overhead Cost * Quantity    |
| DR        | Inventory - Machine Variable Overhead      | Machine Variable Overhead Cost* Quantity  |
| CR        | COGS - Material (Item Account Maintenance) | Material Cost * Quantity                  |
| CR        | COGS - Material Fixed Overhead             | Material Fixed Overhead Cost * Quantity   |
| CR        | COGS - Material Variable Overhead          | Material Variable Overhead Cost* Quantity |
| DR        | COGS - Labor (Item Account Maintenance)    | Labor Cost * Quantity                     |
| DR        | COGS - Labor Fixed Overhead                | Labor Fixed Overhead Cost * Quantity      |
| DR        | COGS - Labor Variable Overhead             | Labor Variable Overhead Cost* Quantity    |
| CR        | COGS - Machine (Item Account Maintenance)  | Machine Cost * Quantity                   |
| CR        | COGS - Machine Fixed Overhead              | Machine Fixed Overhead Cost * Quantity    |
| CR        | COGS - Machine Variable Overhead           | Machine Variable Overhead Cost* Quantity  |

Example of Accounts and Costs used during a SOP Return for a finished good item

| **DR/CR** | **Account**                           | **Cost Used**                     |
|-----------|---------------------------------------|--------------------             |
| DR        | FG - Material                         | $4.10 * 1 = $4.10                 |
| DR        | FG - Material Fixed Overhead          | $.55 * 1 = $.55                   |
| DR        | FG - Material Variable Overhead       | $.35 * 1 = $.35                   |
| CR        | FG -  Labor                           | $.27 * 1 = $.27                   |
| CR        | FG -  Labor Fixed Overhead            | $.02 * 1 = $.02                   |
| CR        | FG -  Labor Variable Overhead         | $.01 * 1 = $.01                   |
| DR        | FG -  Machine                         | $.43 * 1 = $.43                   |
| DR        | FG -  Machine Fixed Overhead          | $.10 * 1 = $.10                   |
| DR        | FG -  Machine Variable Overhead       | $.12 * 1 = $.12                   |
| CR        | COGS - Material                       | $4.10 * 1 = $4.10                 |
| CR        | COGS - Material Fixed Overhead        | $.55 * 1 = $.55                   |
| CR        | COGS - Material Variable Overhead     | $.35 * 1 = $.35                   |
| DR        | COGS - Labor                          | $.27 * 1 = $.27                   |
| DR        | COGS - Labor Fixed Overhead           | $.02 * 1 = $.02                   |
| DR        | COGS - Labor Variable Overhead        | $.01 * 1 = $.01                   |
| CR        | COGS - Machine                        | $.43 * 1 = $.43                   |
| CR        | COGS - Machine Fixed Overhead         | $.10 * 1 = $.10                   |
| CR        | COGS - Machine Variable Overhead      | $.12 * 1 = $.12                   |

Manufacturing Order Processing Transactions
Component Transaction Entry Window
Transactions -> Manufacturing -> Manufacturing Orders -> Component Transaction Entry

Allocate transaction
There is no inventory movement or inventory transaction which occurs. When the allocation document is saved with items on the pick doc tab, those items will be allocated.

Reverse Allocation transaction
There is no inventory movement or inventory transaction which occurs. When the reverse allocation document is saved with items on the pick doc tab, those items will no longer be allocated.

Scrap transaction
There is no inventory movement or inventory transaction which occurs. When the scrap pick doc is posted with items on the pick doc tab, those items will be ‘flagged’ as being scrapped during the MO process.

Reverse Scrap transaction
There is no inventory movement or inventory transaction which occurs. When the reverse scrap pick doc is posted with items on the pick doc tab, those items will no longer be ‘flagged’ as being scrapped during the MO process.

Issue Material from Component Transaction Entry
Issue items from inventory Issue from site to WIP
Audit Trail Code example: IVADJ00000123

Actual Cost Item
Issued items are removed from the issue from site and placed into WIP.

## See also

[Manufacturing Setup - Part 1: Manufacturing setup](manufacturing-setup-part-1.md)  
[Manufacturing Setup - Part 2: User setup](manufacturing-setup-part-2.md)  
[Glossary of Terms in Manufacturing](glossary-manufacturing.md)  
