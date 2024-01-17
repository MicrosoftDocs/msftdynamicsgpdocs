---
title: "Payroll Connect for Dynamics GP"
description: "Payroll Connect for Dynamics GP"
keywords: "payroll"
author: tnistler
manager: jswymer

ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 01/07/2019

---
# Payroll Connect

Payroll Connect lets you import Automated Data Processing (ADP) account transactions from an ADP file into Microsoft Dynamics GP General Ledger. In addition to using ADP PC/Payroll for Windows®, you also must be using ADP’s GL Interface and Super Data Access.

## Installation and setup

Payroll Connect is installed when you install Microsoft Dynamics GP, and does not require a separate installation process. It will become available once you enter the appropriate registration keys.

To use the ADP General Ledger Interface, you’ll need to work with ADP to set up the same account framework in their product as in General Ledger. You must set up the General Ledger account framework first.

You’ll also need to work with an ADP representative to generate a .GLI output file that has the correct format, which is described in *Payroll Connect overview*.

### Payroll Connect overview

When you use Payroll Connect, Microsoft Dynamics GP expects a comma-delimited ASCII text file in comma-separated values (CSV) format, as follows:

| **Column**                                                       | **Maximum size** |
|------------------------------------------------------------------|------------------|
| Client Code                                                      | 5                |
| General Ledger Account Number                                    | 24               |
| Journal Source Code                                              | 2                |
| Date (format is MMDDYYYY)                                        | 8                |
| Amount (Negative numbers (credit amounts) are preceded by a ‘-’. | 13               |
| Contains an explicit decimal point.)
| Reference number 1                                               | 6                |
| Description                                                      | 20               |
| Reference number 2                                               | 6                |
| Reference number 3                                               | 6                |
| Record Code                                                      | 2                |

The following is a sample ADP file showing the correct format:

```
"QC911","208015","PR","04302007","33222.11","","GROSS","","","02"
"QC911","208003","PR","04302007","-2696.34","","ER SOCIAL SECURITY","","","02" 
"QC911","208004","PR","04302007","-630.59","","ER MEDICARE","","","02"
"QC911","208005","PR","04302007","-2696.34","","EE SOCIAL SECURITY","","","02"
"QC911","208006","PR","04302007","-630.59","","EE MEDICARE","","","02"
"QC911","208010","PR","04302007","-29051.95","","NET PAY","","","02"
"QC911","208011","PR","04302007","-8590.10","","EE FEDERAL TAX","","","02"
"QC911","208012","PR","04302007","-348.07","","FUTA TAX","","","02"
"QC911","208013","PR","04302007","-59.63","","EE SUI TAX","","","02"
"QC911","208106","PR","04302007","-398.49","","MEALS","","","02"
"QC911","","PR","04302007","1612.60","","","","","02"
"QC911","ABCDEFGHIJKL","PR","04302007","-999999999.99","","TEST LINE","","","02"
```

Once the batch is imported and you select the imported Journal Entry in General Ledger Transaction Entry, the source document and reference depend on how you imported the transactions. If you create a batch for the import, the source document will be GJ and the reference will be Payroll Connect. If you add the ADP transactions to an existing batch, the source document will be whatever was originally assigned to the batch. In either case, the currency ID will be the functional currency from the 
**Multicurrency Setup** window.

Account, debit, and credit fields are imported. If the number of characters in the imported data is greater than the General Ledger field allows, the information will be truncated. For example, if your General Ledger account numbers have 15 digits, and ADP account numbers have 24 digits, the additional numbers from the ADP file are truncated as shown in the following table.

| **General Ledger account number** | **Value**                  |
|-----------------------------------|----------------------------|
| ADP                               | “255354249990001249786758” |
| General Ledger                    | “255354249990001”          |

The debit and credit decimal settings will be set by the currency ID. If the ADP file contains more decimal places than the currency ID, the amounts will be rounded.

The distribution reference will be the description from the ADP file.

### Importing ADP transactions into General Ledger

Use the Import From ADP window to import ADP account transactions from an ADP file into Microsoft Dynamics GP General Ledger.

**To import ADP transactions into General Ledger:**

1. Open the Import From ADP window. (Tools \>\> Integrate \>\> Import From ADP)

2. Enter or select a batch.

3. Enter the date that you want for the General Ledger transaction.

4. Select the location and file name you want to import.

5. Choose Process. The ADP transactions will be added to the specified batch or a new batch will be created and a unique Journal Entry created to associate transactions with the batch.

    If you receive the message, “Selected import file is not a valid ADP export file,” first verify the pathname to the import file. If the pathname is correct, there may be damage to the ADP file. Contact your ADP representative.

6. In the General Ledger Transaction Entry window, select the Journal Entry for the imported batch, verify the transactions and post the batch.
