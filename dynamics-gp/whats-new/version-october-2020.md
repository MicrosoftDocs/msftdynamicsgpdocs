---
title: "What's new in Dynamics GP in October 2020"
description: "Learn about enhancements that were added to the product in this release of Dynamics GP."
author: edupont04

ms.author: edupont
ms.reviewer: edupont
manager: annbe
ms.prod: dynamics-gp
ms.topic: article
ms.date: 10/01/2020
---

# What's New in Dynamics GP in October 2020

This page lists enhancements to Dynamics GP in the October 2020 release. The Dynamics GP October 2020 release enhances specific areas of the product.

## Financial enhancements

A number of updates have been made to the Finance area in Dynamics GP.

### Additional user-defined fields in General Ledger Transaction Entry​

Two new fields are added to the **General Ledger Transaction Entry​** window and included in the **Edit list** and **Posting journal** so that users can describe transactions​.

You must configure labels in **General Ledger Setup​**. users can then add information or comments regarding transactions​.

> [!TIP]
> Add the fields to SmartList & other reports​ if your organization finds them useful.

For more information, see [Additional User-Defined Fields in General Ledger Transaction Entry](additional-user-defined-fields-in-general-ledger-transaction-entry.md).  

### Import credit card transactions​

Import credit card transactions as payable invoices or manual payments​. This helps reduce risk of entry errors​ because you can bring in invoices for a vendor as a batch​.  

After import, a report prints a list of transactions and their status​.  For more information, see [Import Credit Card Transactions](import-credit-card-transactions.md).  

### Automate financial full reconcile​

Reconcile all years from oldest to newest year​. Each year is completed before the next year is reconciled​.  

> [!NOTE]
> Users cannot choose another year until the first reconciliation is complete​.

For more information, see [Automate Financial Full Reconcile](automate-financial-full-reconcile.md).  

### Match Excel copy and paste decimal places to Currency Setup​

Configure your preference of decimal and thousands separators​ in the **Currency Setup** window so that you can copy/paste amounts from Excel without running into problems with different currencies using different separators.  

For example, specify period as the decimal separator for the USD currency and comma as the decimal separator for the DKK currency.  

For more information, see [Match Excel Copy and Paste Decimal Places to Currency Setup](match-excel-copy-and-paste-decimal-places-currency-setup.md).  

### Form 1099 Non-Employee Compensation​

The IRS releases a new 1099 NEC form for the 2020 tax year​ where *Non-Employee Compensation* (NEC) is moved from 1099 MISC to its own form​. This update of Dynamics GP adds **Nonemployee Compensation** as a 1099 tax type in the following windows:​

* Vendor Card​
* Update 1099 Information utility​

For more information, see [Form 1099 NEC](form-1099-nec-now-supported.md).  

### 1099 MISC form updates​

The 1099-MISC form has been revised to meet the IRS regulatory changes for the 2020 tax year​

* Non-Employee Compensation (NEC) moved to its own form​

* Box 9: Crop insurance proceeds are reported​

* Box 10: Gross proceeds to an attorney​

* Box 12: Section 409A deferrals​

* Box 14: Non-qualified deferred compensation income​

* Boxes 15 and 17: State taxes withheld, and amount of income earned in the state, respectively​

* Box 7: Replaced by the 1099 NEC form​

* Box 16: State number is not a currency field and it is available at the header level of the 1099 details window​

For more information, see [1099 MISC Form Updates](1099-misc-form-updates.md).  

### DBA field for vendors

Vendors that have a "Doing Business As" (DBA) name in addition to the legal company name, and that want to have the DBA name appear on the 1099, can now do so​. It is common for companies to have a legal name registered but do business under another name, the name that they want customers to see. ​

The feature enables the user of both the legal name of a company and DBA.​  For more information, see [DBA for Vendor](dba-for-vendor.md).  

### Removed fully applied Multicurrency documents from PM HATB​

You can choose to exclude fully applied multi-currency documents from the **PM Historical Aged Trial Balance** report​.  

In previous releases of Dynamics GP, if an invoice went through a revalue before it was paid, the documents would print on the report even though they were fully applied. They would show with an aged total of $0.00 which made the report longer due to unnecessary data listed.​ For more information, see [Removed Fully Applied Multicurrency Documents from PM HATB](removed-fully-applied-multicurrency-documents-from-pm-hatb.md).  

## Distribution functionality​

A number of updates have been made to the Distribution area in Dynamics GP.

### Export/Import stock counts to Excel​

Export and import data with Excel from the **Stock Count** and **Stock Count Schedule** windows, giving you more flexibility with this process​.  

For more information, see [Export/Import Stock Counts to Excel](exportimport-stock-counts-excel.md).  

## Human resources and payroll functionality​

A number of updates have been made to the HR and Payroll areas in Dynamics GP.

### Mask the Social Security in Human Resources reports

The Social Security Number (SSN) mask is now also available on the **Human Resources** reports. By default, SSN will be marked as masked​, but to see the SSN on the reports, unmark it from the settings in the **Human Resources Preferences** window​. For more information, see [Human Resources Social Security Number Mask](human-resource-social-security-number-mask.md).  

## System enhancements

A number of updates have been made to Dynamics GP across the product areas.

### Schedule Check Links​

Set up a schedule to run **Check Links** outside of normal business hours​. For more information, see [Schedule Check Links](schedule-check-links.md).  

### Multi-Factor Authentication​

Use Multi-Factor Authentication for e-mail​ authentication. This new feature relies on an Azure Active Director App registration​ - register an app in the[Azure portal](https://portal.azure.com/) & copy the value of Application (client) ID​. For more information, see [Azure portal app registration experience](/azure/active-directory/develop/app-registration-portal-training-guide).  

In Dynamics GP, you must then add this Application (client) ID​ to the **Company E-mail Setup** window​. For more information, see [Multi-Factor Authentication](multi-factor-authentication.md).  

> [!NOTE]
> For now, Multi-Factor Authentication is not supported in the Web Client​.

### TLS 1.2

TLS 1.0 and 1.1 protocols are being deprecated in general. This release of Dynamics GP adds support for TLS 1.2. For more information, see [Support for TLS 1.2](tls-1.2.md).  

### Save per-user column layouts on Home Page​

Users can now customize and save the layout of their Home Page. Simply choose the **Customize this page** control in the upper-right corner of the Home Page​, and then, choose the column layout and how to stack columns when you maximize a specific section​. For more information, see [Save Per-User Column Layouts of Home Page](save-per-user-column-layouts-on-home-page.md).  

### Disable print dialog when printing to Word​

You can now use Named Printers with Word Templates. ​This lets users access full one-click printing when using Word Templates. No more print dialog when using Templates! ​

Set up named printers, then assign named printers to users​. For more information, see [Disable Print Dialog when Printing to Word](disable-print-dialog-when-printing-word.md).  

### Enable Self Service user type access to User Preference​

Manage User Preference and Workflow Delegation settings by adding a self-service user & then set up workflow delegation​. For more information, see [Enable Self-Service User Type Access to User Preference](enable-self-service-user-type-access-user-preference.md).  

### Bulk-edit SmartList Columns​

You can now edit the columns on a SmartList​. For more information, see [Bulk-edit SmartList Columns](bulk-edit-smartlist-columns.md).  

## Top feature requests

The following features were chosen to be added in this release because they have been voted the most popular feature asks on the Ideas site.

### Maximum print output screen​

Users no longer have to manually maximize the print output screen each time they print a report to the screen - the report will automatically pop out to full screen mode for you!​ For more information, see [Maximum Print Output Screen](maximum-print-output-screen.md).  

### Copy/Paste Purchasing transactions from Excel​

The same copy/paste functionality that you know from General Ledger is now available for Purchasing!. Use the **Transaction Entry** window to copy/paste PM Transactions and PM Distributions​. You can include distributions or not​.  

> [!TIP]
> The Excel Spreadsheet must have the required fields in this order to copy paste correctly​.

For more information, see [Copy/Paste Purchasing transactions from Excel](copypaste-purchasing-transactions-from-excel.md).  

## See also

[System requirements](../installation/system-requirements.md)  
[Upgrade introduction](../upgrade/introduction.md)  
[Dynamics GP community on https://community.dynamics.com](https://community.dynamics.com/gp)  
[Dynamics GP User Group](https://www.gpug.com/home)  
[Additional User Defined fields in General Ledger Transaction Entry](additional-user-defined-fields-in-general-ledger-transaction-entry.md)  
[Import Credit Card Transactions](import-credit-card-transactions.md)  
[Automate Financial Full Reconcile](automate-financial-full-reconcile.md)  
[Match Excel copy and paste decimal places to Currency Setup](match-excel-copy-and-paste-decimal-places-currency-setup.md)  
[Form 1099 NEC now supported](form-1099-nec-now-supported.md)  
[1099 MISC Form Updates](1099-misc-form-updates.md)  
[DBA for Vendor](dba-for-vendor.md)  
[Removed fully applied Multicurrency documents from PM HATB](removed-fully-applied-multicurrency-documents-from-pm-hatb.md)  
[Copy/Paste Purchasing transactions from Excel](copypaste-purchasing-transactions-from-excel.md)  
[Export/Import stock counts to Excel](exportimport-stock-counts-excel.md)  
[Print all Sales Documents](print-all-sales-documents.md)  
[Human Resource Social Security Number mask](human-resource-social-security-number-mask.md)  
[Schedule Check Links](schedule-check-links.md)  
[Multi-Factor Authentication](multi-factor-authentication.md)  
[TLS 1.2](tls-1.2.md)  
[Save per user column layouts on Home Page](save-per-user-column-layouts-on-home-page.md)  
[Disable print dialog when printing to word](disable-print-dialog-when-printing-word.md)  
[Enable Self Service user type access to User Preference](enable-self-service-user-type-access-user-preference.md)  
[Maximum print output screen](maximum-print-output-screen.md)  
[Bulk edit SmartList Columns](bulk-edit-smartlist-columns.md)  
