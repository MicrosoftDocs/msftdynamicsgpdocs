# Data preparation

<span id="_Toc498615770" class="anchor"></span>

We recommend that you complete the steps in this chapter to prepare your data before you upgrade your system. After you’ve completed these steps, see [Chapter 4, System preparation](#_System_Preparation), for instructions to prepare your system before upgrading to Microsoft Dynamics GP 2018. Be sure to review the [Known issues](#_Known_issues) on page 23 before upgrading to Microsoft Dynamics GP 2018.  

This chapter contains the following sections:

-   [Payroll](#payroll)  

-   [1099 amounts in Payables Management](#amounts-in-payables-management)  

-   [Direct Debits and Refunds](#direct-debits-and-refunds)  

-   [Field Service Series](#field-service-series)  

-   [Workflow for SharePoint](#workflow-for-sharepoint)  

-   [Posting open transactions](#posting-open-transactions)  

-   [Reconciling](#reconciling)  

-   [Backups](#backups)  

-   [Reports you should print](#reports-you-should-print)  

## Payroll

If you’re upgrading to Microsoft Dynamics GP 2018, you need to determine whether the payroll tax update tables are current. To do so, check the Last Tax Update field in the Payroll Tax Setup window (Tools &gt;&gt; Setup &gt;&gt; System &gt;&gt; Payroll Tax). If your tax tables are not current, update them after you upgrade to Microsoft Dynamics GP 2018. Review the latest tax update documentation for the date of the last tax update.

Tax tables are not included on the Microsoft Dynamics GP media; to update tax tables, you must download them from CustomerSource (US Payroll <https://mbs.microsoft.com/customersource/northamerica/GP/downloads/taxregulatory-updates/TUGP2018>; Canadian Payroll: <https://mbs.microsoft.com/customersource/northamerica/GP/downloads/tax-regulatory-updates/cagptuye2018>). Choose Tax and Regulatory Updates. Follow instructions for installing the tax update to ensure that clients and servers are updated properly.

## 1099 amounts in Payables Management

After you upgrade, the 1099 amounts might be transferred to a different month if you have transactions that are posted in one month and applied in another month after you upgrade. You might have to make adjustments to your 1099 amounts so that the 1099 amounts aren’t overstated or understated.

For example, you enter and post the following transaction in December.

-   An invoice for $100.00 that has a 1099 amount of $100.00.

-   A credit memo for $75.00 that has a 1099 amount of $75.00.

-   A payment for $25.00.

You apply all three documents together in January. The 1099 amount is $25.00 for December.

You upgrade to Microsoft Dynamics GP 2018 in February and reconcile your data. The 1099 amount of $25.00 is moved from December because the later of the apply date or posting date is used to update the 1099 amount.

## Direct Debits and Refunds

You must process or delete existing Direct Debits and Refunds batches before upgrading from an earlier release of Direct Debits and Refunds (DDR).

## Field Service Series

You must ship and post all inventory transfers that have a partially shipped, shipped, or partially received status before you upgrade.

## Workflow for SharePoint

Workflow for SharePoint is no longer available for GP. There is no upgrade from Workflow for SharePoint to the new Workflow feature in Microsoft Dynamics GP. Workflow types that were created in SharePoint-based workflow feature do not upgrade. Any workflows that you created in the SharePoint-based workflow feature will need to be re-created in the new workflow feature after the upgrade is complete. Note that some workflow types that were available in the SharePoint workflow feature are not yet available in the new workflow feature.

## Posting open transactions

Before you upgrade, you should post all single-use batches. We recommend that you post all transactions that can affect your purchase receipts and sales transactions. For some integrating products, the upgrade process removes and re- creates work tables, which will cause open transactions to become corrupted. In addition, if errors are encountered during the upgrade, troubleshooting is easier if there are no unposted transactions.

If you are using Analytical Accounting, be sure to post all saved batches that you created using the Collection and Payment Methods – Withholds, Perceptions, Tax Administration Purchasing, or Tax Administration Sales modules. You can then use the Analytical Adjustment Entry window to enter analysis information for the posted transactions.

## Reconciling

You may want to reconcile your accounting records before upgrading to Microsoft Dynamics GP 2018 to verify that your accounting records are accurate. Refer to the documentation of the modules you are using for specific information.

Before reconciling, back up your company’s accounting data. For more information about making backups, refer to your System Administrator’s Guide (Help &gt;&gt; Contents &gt;&gt; select System administration)![Chapter 3 Data Preparation image1](media/Chapter-3-Data-Preparation-image1.png).  

## Backups

You should make at least one complete backup of all your databases before upgrading. It’s a good idea to make a backup before completing table maintenance procedures, in case you encounter any problems in that process. You also should make a backup of your modified forms and reports, eConnect pre and post procedures and your existing Integration Manager database.

If you are upgrading a company that has previously deployed SQL Server Reporting Services reports and Microsoft Excel reports, the deployed reports are automatically upgraded. If you have modified reports, those reports will be overwritten during the upgrade. Be sure to make a backup of your reports.

## Reports you should print

Before you upgrade, it’s a good idea to print the following reports to a printer or to a file. You can use them to verify that your system was upgraded properly or to re- create modifications.

| Module         | Reports                   |
|----------------|---------------------------|
| System         | Process Server Setup List |
| General Ledger | Detailed Trial Balance    |
|                |                           |


