---
title: "Upgrade from Dynamcis GP 2013"
description: "See the module upgrade information to verify the upgrade from Dynamics GP Release 2013."
keywords: "upgrade"
author: jswymer
ms.author: jswymer
manager: jswymer
applies_to: 
ms.date: 08/24/2018
ms.topic: article
ms.assetid: 19740bf2-52ba-40c0-af22-a9bc30f03a24
ms.reviewer: 
---

# Module upgrades from Dynamics GP 2013

Use the module upgrade information in this chapter to verify the upgrade from Dynamics GP Release 2013. The information in this chapter also provides information about module upgrades from Dynamics GP 2013 to Dynamics GP.

This chapter contains the following sections:

- [System upgrade](#system-upgrade)  

- [Payables Management upgrade](#payables-management-upgrade)  

- [Purchase Order Processing upgrade](#purchase-order-processing-upgrade)  

- [Fixed Assets upgrade](#fixed-assets-upgrade)  

- [Payment Services for Microsoft Dynamics ERP upgrade](#_Payment_Services_for)  

## System upgrade

The following change has been made in Dynamics GP. For more information, refer to your System User ’s Guide .

### Posting Accounts Setup window

The Prepayment field has been added. This field will appear in the scrolling window if you select All or Purchasing in the Display field. If you are allowing prepayments for purchase orders, you can enter an account that will be used as the default entry for the prepayment if you didn't enter a default prepayment account in the Purchase Order Processing Setup window.

### Audit Trail Codes Setup window

Purchasing Prepayments has been added as a new audit trail code. This audit trail code will appear in the scrolling window if you select Purchasing in the Display field.

### Security Task Setup window

Purchasing Prepayments has been added to the Series Posting Permissions type for the TRX\_PURCH\_022 task ID for the Purchasing series.

### Posting Setup window

Purchasing Prepayments has been added as an origin for the Purchasing series.

The Apply Documents Posting Journal has been added to the Receivings Trx Entry origin and Purchasing Invoice Entry origin in the Purchasing series.

### Setup Checklist window

The name of the existing Workflow node in the Setup Checklist window has changed to Workflow for SharePoint. A new Workflow node has been added for the new Workflow feature in Dynamics GP. (Dynamics GP 2013 R2 and later.)

### Message Setup window

All existing messages will be updated to have Standard as the message type in the Message Setup window. The Standard message type is for messages that you send to customers or vendors when sending documents in e-mail. The new Workflow feature has Workflow Assignment and Workflow Action Completed as message types. (Dynamics GP 2013 R2)

### Note window

You can use the Document Attachment Management window to attach documents to record level notes instead of OLE objects. If there is an existing OLE object is attached to a note record, the Attach button in the Note window is a drop-down list where you can select OLE Object or Document Attach. By selecting OLE Object, you can open the OLE container. If you select Document Attach, the Document Attachment Management window opens. A checkmark displays next to the option that has a file attached to the note.

If there isn't an existing OLE object is attached to the note, the Attach button in the Note window opens the Document Attachment Management window. (Dynamics GP 2013 R2)

You can use the OLE Notes Migration Utility to migrate the documents already attached to notes from OLE objects to the new document attachment functionality. For more information refer to Microsoft Dynamics CustomerSource or PartnerSource.

## Payables Management upgrade

The following changes have been made. For more information, refer to your Payables Management documentation.

### 1099 address ID

The default 1099 address ID for a 1099 vendor is the primary address ID. The vendor address information assigned to the 1099 address ID is used when you print 1099 statements.

### Additional 1099 information

Additional 1099 boxes and fields have been added for the 1099 tax types in the following windows.

#### 1099 Setup window 
| Tax type | 1099 box number | Minimum amount   |
|----------|-----------------|------------------|
| Dividend            | 10 Exempt Interest Dividends                          | 0.01           |
|                     | 11 Specified Private Activity Bond Interest Dividends | 0.01           |
|                     | 14 State Tax Withheld                                 | 0.01           |
| Individual          | 13 State Tax Withheld                                 | 0.01           |
| Miscellaneous       | 18 State Income                                       | 0.01           |

#### 1099 Details window 
| Tax type            | 1099 box number or field                              | Amount         |
|----------|-----------------|------------------|
| Dividend            | 10 Exempt Interest Dividends                          | 0.00           |
|                     | 11 Specified Private Activity Bond Interest Dividends | 0.00           |
|                     | 14 State Tax Withheld                                 | 0.00           |
|                     | Foreign Country/Region or U.S. Possession                    |                |
|                     | State Code                                            |                |
|                     | State Identification No.                              | 0.00           |
| Individual          | 13 State Tax Withheld                                 |                |
|                     | Foreign Country/Region or U.S. Possession                    |                |
|                     | Tax Exempt Bond CUSIP No.                             |                |
|                     | State Code                                            |                |
|                     | State Identification No.                              |                |
| Miscellaneous       | 18 State Income                                       | 0.00           |
|                     | Payer Made Direct Sales of $5,000 or more etc.        |                |
|                     | State/Payer's State No.                               |                |

## Purchase Order Processing upgrade

The following changes have been made. For more information, refer to your Purchase Order Processing documentation.

### Drop-ship or drop-ship blanket line items that track serial or lot numbers

If you have purchasing invoice receipts saved in a batch prior to upgrading to Dynamics GP 2013, drop-ship or drop-ship blanket line items that track serial or lot numbers assigned to the invoices will not be marked to track serial or lot numbers after you upgrade. You can track serial or lot numbers for these items by selecting each invoice in the Purchasing Invoice Entry window and marking the S/L option for each item.

### Posting Accounts Setup window

The Prepayment field has been added. This field will appear in the scrolling window if you select All or Purchasing in the Display field. If you are allowing prepayments for purchase orders, you can enter an account that will be used as the default entry for the prepayment if you didn't enter a default prepayment account in the Purchase Order Processing Setup window.

### Audit Trail Codes Setup window

Purchasing Prepayments has been added as a new audit trail code. This audit trail code will appear in the scrolling window if you select Purchasing in the Display field.

### Security Task Setup window

Purchasing Prepayments has been added to the Series Posting Permissions type for the TRX\_PURCH\_022 task ID for the Purchasing series.

### Posting Setup window

Purchasing Prepayments has been added as an origin for the Purchasing series.

The Apply Documents Posting Journal has been added to the Receivings Trx Entry origin and Purchasing Invoice Entry origin in the Purchasing series.

### Purchase order approval workflow

When you upgrade to Dynamics GP 2013 R2 or later, there will no longer be the option to use the Purchase Order Approval workflow type in Workflow for SharePoint.

If you were using the Purchase Order Approval workflow in Workflow for SharePoint, the workflow status for each purchase order with an Open status is updated to the Workflow Not Activated status in the new Workflow feature. After setting up a new the purchase order approval workflow in Dynamics GP, you can resubmit the purchase orders using the Purchase Order Entry window or the Purchase Order Transactions navigation list.

The workflow status for each historical purchase order is updated to the statuses used in the new Workflow feature. Review the following table for the new statuses.

| Workflow for SharePoint status | New Workflow status    |
|--------------------------------|------------------------|
| Workflow Not Activated         | Workflow Not Activated |
| Not Submitted                  | Not Submitted          |
| Pending Approval               | Pending User Action    |
| Pending Changes                | Recalled               |
| No Approval Needed             | No Approval Needed     |
| Approved                       | Completed              |
| Rejected                       | Rejected               |
| Workflow Deactivated           | Workflow Not Activated |

If you were not using the Purchase Order Approval workflow in Workflow for SharePoint, the workflow status for each purchase order, including those in history, is updated to the Workflow Not Activated status in the new Workflow feature. (Dynamics GP 2013 R2)

## Project Accounting upgrade

The following changes have been made. For more information, refer to your Project Accounting documentation.

The Exceed Total PO Quantity option has been removed from the PA Purchase Order Processing Setup window. An Overage field has been added in the Purchase Order Processing Setup, Item Class Setup window, and the Item Purchasing Options Maintenance window. If the item is a Sales Inventory or Discontinued item, you can allow quantity tolerances for overages for the quantity ordered.

If the Exceed Total PO Quantity option was marked in a previous release, the Overage option is unmarked in the Purchase Order Processing Setup window, Item Class Setup window, and the Item Purchasing Options Maintenance window.

If the Exceed Total PO Quantity option was unmarked, the Overage option is marked. You will have to enter a quantity tolerance percentage for the overage.

## Fixed Assets upgrade

The following changes have been made. For more information, refer to your Fixed Assets documentation.

### Fiscal calendar

If you have created a Fixed Assets fiscal calendar in a previous release, the following updates occur to the calendar.

- The calendar ID of DEFAULT is assigned to the calendar.

- The description of Default FA Calendar is assigned to the calendar.

- The Short/Long Year option is unmarked in the Fixed Assets Calendar Setup window for each year in the calendar.

- The Depreciation Percentage is 100% in the Fixed Assets Calendar Setup window for each year in the calendar.

- The DEFAULT calendar is assigned to the existing asset books.

### Next Asset ID

The Next Asset ID field in the Fixed Assets Company Setup window is set to the highest asset ID value in the Asset General Information Master (FA00100) table plus 1. For example, if the highest value in the table is FA0001234, then the Next Asset ID field is set to FA0001235. If the highest asset ID value ends in alphabetic characters, such as 8050AC, then the Next Asset ID field in the Fixed Assets Company Setup window is blank.

### Transfer records

Each existing transfer record in the Asset Transfer Master (FA00800) table is assigned the company ID of the company database as the originating company and destination company

<span id="_Payment_Services_for" class="anchor"></span>

## Payment Services for Microsoft Dynamics ERP upgrade

The following changes have been made. For more information, refer to your Payment Services for Microsoft Dynamics ERP documentation.

Address verification is implemented in Payment Services providing an authorization process that validates the card holder billing address information with the merchant bank's record for the card holder to ensure the card is in the hands of the rightful owner. If the result of the verification is not accepted, the credit card transaction will be voided.

The numeric ISO code that is used to identify the country, rather than the entry in the Country Code field. Because various entries may have been made to identify a country - such as US or USA to identify the United States, the one standard number assigned by the ISO is used to verify the country. After the upgrade, you will have to associate countries codes with the correct countries.
