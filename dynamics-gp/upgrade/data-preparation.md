---
title: "Data preparation"
description: "Prepare your data before you upgrade your database to the latest version of Dynamics GP."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 09/21/2021
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 4af5a255-4233-4158-b7d7-660a67e226d0
ms.reviewer: 
---
# Data preparation

We recommend that you complete the steps in this section to prepare your data before you upgrade your system. After you've completed these steps, see [System preparation](system-preparation.md), for instructions to prepare your system before upgrading to the latest version of Dynamics GP. Be sure to review the known issues before upgrade.  

## Payroll

If you're upgrading to Dynamics GP or Dynamics GP 2018 R2, you need to determine whether the payroll tax update tables are current. To do so, check the Last Tax Update field in the Payroll Tax Setup window (Tools &gt;&gt; Setup &gt;&gt; System &gt;&gt; Payroll Tax). If your tax tables are not current, update them after you upgrade to Dynamics GP. Review the latest tax update documentation for the date of the last tax update.

Tax tables are not included on the Dynamics GP media; to update tax tables, you must download them from the following locations:

- [US Payroll](/dynamics/s-e/gp/tugp2018_391)  
- [Canadian Payroll](/dynamics/s-e/gp/cagptuye2018_285)  

Choose Tax and Regulatory Updates. Follow instructions for installing the tax update to ensure that clients and servers are updated properly.

## 1099 amounts in Payables Management

After you upgrade, the 1099 amounts might be transferred to a different month if you have transactions that are posted in one month and applied in another month after you upgrade. You might have to make adjustments to your 1099 amounts so that the 1099 amounts aren't overstated or understated.

For example, you enter and post the following transaction in December.

- An invoice for $100.00 that has a 1099 amount of $100.00.

- A credit memo for $75.00 that has a 1099 amount of $75.00.

- A payment for $25.00.

You apply all three documents together in January. The 1099 amount is $25.00 for December.

You upgrade to Dynamics GP in February and reconcile your data. The 1099 amount of $25.00 is moved from December because the later of the apply date or posting date is used to update the 1099 amount.

## Direct Debits and Refunds

You must process or delete existing Direct Debits and Refunds batches before upgrading from an earlier release of Direct Debits and Refunds (DDR).

## Field Service Series

You must ship and post all inventory transfers that have a partially shipped, shipped, or partially received status before you upgrade.

## Workflow for SharePoint

Workflow for SharePoint is no longer available for GP. There is no upgrade from Workflow for SharePoint to the new Workflow feature in Dynamics GP. Workflow types that were created in SharePoint-based workflow feature do not upgrade. Any workflows that you created in the SharePoint-based workflow feature will need to be re-created in the new workflow feature after the upgrade is complete. Note that some workflow types that were available in the SharePoint workflow feature are not yet available in the new workflow feature.

## Posting open transactions

Before you upgrade, you should post all single-use batches. We recommend that you post all transactions that can affect your purchase receipts and sales transactions. For some integrating products, the upgrade process removes and re- creates work tables, which will cause open transactions to become corrupted. In addition, if errors are encountered during the upgrade, troubleshooting is easier if there are no unposted transactions.

If you are using Analytical Accounting, be sure to post all saved batches that you created using the Collection and Payment Methods – Withholds, Perceptions, Tax Administration Purchasing, or Tax Administration Sales modules. You can then use the Analytical Adjustment Entry window to enter analysis information for the posted transactions.

## Reconciling

You may want to reconcile your accounting records before upgrading to Dynamics GP to verify that your accounting records are accurate. Refer to the documentation of the modules you are using for specific information.

Before reconciling, back up your company's accounting data.  

## Backups

You should make at least one complete backup of all your databases before upgrading. It's a good idea to make a backup before completing table maintenance procedures, in case you encounter any problems in that process. You also should make a backup of your modified forms and reports, eConnect pre and post procedures and your existing Integration Manager database.

If you are upgrading a company that has previously deployed SQL Server Reporting Services reports and Microsoft Excel reports, the deployed reports are automatically upgraded. If you have modified reports, those reports will be overwritten during the upgrade. Be sure to make a backup of your reports.

## Reports you should print

Before you upgrade, it's a good idea to print the following reports to a printer or to a file. You can use them to verify that your system was upgraded properly or to re- create modifications.

| Module                  | Reports                            |
|----------------         |---------------------------         |
| System                  | Process Server Setup List          |
| General Ledger          | Detailed Trial Balance             |
| Receivables Management  | Aged Trial Balance with Options    |
| Payables Management     | Aged Trial Balance with Options    |
| Inventory Control       | Pricing Reports                    |
                          | Extended Pricing Error Reprots     |
                          | Purchase Receipts                  |
| Purchase Order Proc.    | Purchase order                     |
                          | Purchase Order Status Report       |
| Payroll                 | Benefit & Deduction Summary        |
                          | FUTA,SUTA & Workers Comp Period End|
                          | Check and Transaction History      |
                          | Employee Pay History               |                          
                          | 941 and 941 Schedule B             |    
| Manufacturing           | WIP Report                         |  
                          | Manufacturing Order Summary        |  
                          | Standard Cost Pending              |  
