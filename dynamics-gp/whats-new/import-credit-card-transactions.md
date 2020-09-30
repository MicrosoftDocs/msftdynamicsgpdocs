---
title: Import Credit Card Transactions 
description: New in October 2020 - Import Credit Card Transactions
ms.date: 09-30-2020
ms.topic: article
ms.prod: dynamics-gp
author: theley502
ms.author: theley
manager: edupont
---

# Import Credit Card Transactions

Importing a credit card statement to a vendor account in Dynamics GP makes it fast and easy to enter invoice transactions. Users can import the credit card transactions as payable invoices or manual payments. Using the import functionality helps reduce the chances of data entry errors and brings invoices for a vendor into a batch.

The imported transactions must be saved as a batch and appropriate distributions must be created for each transaction.

Once the transactions import process is completed, a report will print with a list of transactions and status of the transactions.

An example of how this will work is a company gets their credit statement electronically or they can download the transactions to a qbo/qfo/qfx file locally. This allows the user to bring that data into Microsoft Dynamics GP and generate invoices for the credit card that is setup as a vendor within the Dynamics GP system.

Vendor Mapping and Transaction Type mapping setup needs to be completed before the functionality will work.

> [!NOTE]
> ONLY debit type transactions will be brought in with the import. Credit type transactions will still need to be manually entered.

## Table Changes

There are two new tables.

* PMVendorMapCreditCardSetup - PM40107
  * New field: OriginText
  * New field: VENDORID

* PMCreditCardAccountSetup - PM40108
  * New field: CreditCardTrxType
  * New field: ACTINDX
  * New field: ACTNUMBR

In the Payable Management Setup page, under the Purchasing Home page, choose Setup, click Payables. Two buttons have been added: Vendor Map and Trx Type Map.

<img src="media/image7.jpg" alt="Payables Management Setup" width="458" height="392" />

The Vendor Mapping window is used to map the Credit Card (Org) field in the file format .qbo, .qfo, .qfx, to the corresponding Vendor ID you have setup in Dynamics GP.

This mapping will determine which Vendor ID is used when the invoices are created from the import. Without this information populated in Dynamics GP the system will not know what Vendor ID should be used to create the invoices for the credit card statement being imported. This setup is required.

To find the Credit Card Org, open the qbo/qfo/qfx file using a text file program and search for &lt;ORG&gt;AMEX&lt;/ORG&gt;. This will be the Credit Card (Org) field. Map that name to the Vendor ID being used for the Credit Card in Dynamics GP. In the example below you will see AMEX as the Credit Card Org, as an American Express Credit Card QBO file. It has been mapped to Vendor ID AMEX0001 which is the vendor that has been created to track invoices and payments for the American Express Credit Card the Fabrikam, Inc. company uses. The 'Credit Card (Org) field is freeform and is 10 characters in length.

<img src="media/image8.jpg" alt="Vendor Mapping" width="261" height="245" />

> [!NOTE]
> If there isn't a vendor setup in the vendor mapping for the file when the user chooses process, they will get an error This vendor hasn't been mapped.

Transaction Type Account Mapping will give the user the ability to map the transaction type from the qbo file to the Account Number in Dynamics GP. This information isn't required but will allow a different purchases account to be posted other than the default "purchases account" on the vendor card. To pull the account number from this window, the transaction type string will need to match. If there are multiple "matches" the GP will not pull the account number into the invoice.

The "transaction type" field in the window will be a freeform field. This field will have a max length of 50.

The Account field will be a lookup field that will give the user the ability to look up the Account Numbers and select an existing Account to be used when the invoices are created during the import.

<img src="media/image9.jpg" alt="Transaction Type Account Mapping" width="356" height="257" />

> [!NOTE]
> The name of transaction type can be mapped to an Account. That account will then be used for the Purchases Account type on the Invoice transaction distributions. The Transaction Type will be compared to the &lt;NAME&gt;DELTA AIR LINES&lt;/NAME&gt; within the import file. The entire name in the .qbo file needs to be entered into the Transaction Type field to match and use the account setup. If this is not setup with any account mappings or there are no matches between the import file and the transaction type account mapping the Purchases account on the vendor card is used by default.

To import the credit card transactions from the Payables Home page click Transactions choose Payables and Import Payables Invoices.

Use the yellow folder icon to map to your saved import file.

<img src="media/image10.jpg" alt="Import Payables Invoices" width="469" height="206" />

The process button will give the user the ability to import from the file location.

If the user wants to modify the information on the transactions, they will need to do that after the import when the transactions are in the batch.

Once the import is completed you will get a message below:

<img src="media/image11.jpg" alt="Confirmation dialog" width="471" height="183" />

> [!NOTE]
> Transactions will be entered into the system using the functional currency.

Once the import process has run, a batch is created and needs to be posted by the user. Creating the batch and not posting gives the user the ability to verify the batch before it posts. This would also allow the user to change the distributions if needed before they post the batch.

If you click Transactions and then choose Purchasing, click Batches. You should see your imported batch.

<img src="media/image12.jpg" alt="Payables Batches" width="464" height="330" />

<img src="media/image13.jpg" alt="Payables Transaction Entry" width="624" height="841" />


