---
title: "Glossary"
description: "Terminology used in the Financials area in Dynamics GP."
keywords: "banking, bank reconciliation"
author: theley502
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 01/14/2019
---

# Glossary of Terms in the Financials Area in Dynamics GP

The following table explains the terminology used in the Financials area in Dynamics GP.

|Term  |Definition |
|---------|---------|
|Alternate currency |Any currency that is not a functional currency. |
|Audit trail| A series of permanent records used to track a transaction to the point where it was originally entered in the accounting system. The audit trail can be used to verify the accuracy of financial statements by outside accountants or auditors.|
|Audit trail code|A series of alphanumeric characters providing a precise record of each transaction and where it has been posted within Dynamics GP.|
|Background processing|Background processing enables users to continue working while transactions are being posted or reports are being printed.|
|Bank card|A card for which payments might be treated as cash by the business receiving the payment. |
|Bank reconciliation |The process of making the cash balance shown on the bank statement and the cash balance entered in Bank Reconciliation match as of a certain date.|
|Bank statement|A statement issued by a bank describing the activities in checking accounts and other bank accounts over a period of time.|
|Batch|A group of transactions identified by a unique name or number. Batches are used in computerized accounting to conveniently group transactions, both for identification purposes and to speed up the posting process.|
|Batch-level posting| A posting method that enables transactions to be saved in batches that can be posted whenever convenient. There are three types of batch-level posting: batch posting, series posting, and master posting.|
|Breakout of due to/due from accounts|Detail created by Dynamics GP showing the distribution account you enter and the offset due to account or due from account for each intercompany distribution. This breakout prints only on edit lists (in Payables Management) and posting journals (in General Ledger and Payables Management).|
|Check |A written order on a bank to pay a sum of money from funds in an account. Checks show the name of the company or individual receiving payment, the signature and account number of the person issuing the check, the payment amount, and the current date. Checks usually are numbered in sequence.|
|Check card|A type of credit card. When purchases are made with a check card, the amount of purchase will immediately be withdrawn from the user’s bank account. Check cards also are known as debit cards.|
|Checkbook|An account that keeps a currency balance and tracks the receiving and disbursing of cash. |
|Cleared amount|The amount a bank statement shows a transaction cleared for.|
|Cleared difference|The difference between what you entered for a transaction in your checkbook and the amount the transaction cleared for on the bank statement.|
|Decrease adjustment |An entry that decreases the checkbook amount.|
|Deposit|Money added to an account.|
|Deposit slip|A form that shows the date and the items that make up a deposit, including receipt and payment information, the currency, check, and coin totals, and the amount of cash received.|
|Destination company|A company that will be the recipient of an intercompany transaction.|
|Deposit in transit|Deposit that has been entered but hasn’t cleared the bank.|
|Due to/due from accounts| General Ledger accounts used by Dynamics GP to track amounts to be paid or to be collected among companies. The due to/due from accounts are often called Intercompany Payable and Intercompany Receivable in the Chart of Accounts.|
|Euro|A trading currency for participating countries/regions in the European Union.|
|Exchange rate|The rate of exchange between two currencies on a particular date and time.|
|Expansion button| A button used to open a window where information for the field next to the button can be added, changed, or viewed.|
|Functional amount|The equivalent transaction amount in the functional currency for a  multicurrency transaction amount that was entered using an originating currency. This amount sometimes is referred to as the functional equivalent of the originating amount.|
|Functional currency|The primary currency a company keeps its financial records in. Typically, the functional currency is the currency for the country/ region where the company is located.|
|Functional equivalent|See *Functional amount*.|
|Group printing|Creating and printing report options in groups. For example, you could use a report group to print the Checkbook Register Report and the Undeposited Receipts Report.|
|History|Transaction activity from a previous year. Maintaining history files enables users to print detailed reports, comparing currentyear activity to activity in a previous year.|
|Increase adjustment|An entry that increases the checkbook amount.|
|Inquiry|A feature that enables users to view openyear and historical information.|
|Intercompany transaction|Any transaction that contains distributions to another company.|
|Intercompany-generated transaction|Any transaction that originated in another company.|
|Journal|A chronological list of transactions, in the form of debits and credits, for a particular account or group of accounts, such as sales or cash disbursements.|
|Journal entry|A transaction recorded in a formalized manner by entering an account and the amounts to be debited and credited.|
|Last reconciled balance|The balance of a checkbook on the bank statement. This is the amount to reconcile to.|
|Master posting|A posting process in which marked batches from different series can be posted simultaneously.|
|Origin|A transaction entry window within a specific Dynamics GP module. Certain options, such as verifying batch controls and closing fiscal periods can be selected for each transaction origin. Also, the transaction origin will appear as part of the audit trail code on all posting reports in Dynamics GP.|
|Originating amount|The transaction amount in the originating currency for a multicurrency transaction. Originating amounts are posted using their corresponding functional amounts, sometimes referred to as functional equivalents.|
|Originating company|The company in which you initiate (or originate) an intercompany transaction.|
|Outstanding check|Check that has been written, entered, and sent to payees but hasn’t yet been received, paid, and canceled by the bank.|
|Posting|A procedure to make temporary transactions a part of a business’s permanent records; to update the checkbook and the General Ledger accounts.|
|Posting account|A financial account that tracks assets, liabilities, revenue, or expenses. These accounts will appear on financial statements and on other reports created in the financial series.|
|Posting journal|A report printed following the posting process that shows the detail for each transaction that’s been posted. Posting journals also include the audit trail code, which is a precise record of where each transaction has been posted.|
|Real-time posting|See *Transaction-level posting*.|
|Realized gain|Gain realized due to the difference in exchange rates between when the receipt was posted and when the receipt was deposited.|
|Realized loss|Loss realized due to the difference in exchange rates between when the receipt was posted and when the receipt was deposited.|
|Receipt|Any type of payment a business might receive.|
|Reconciling|A procedure that compares a checkbook to a bank statement.|
|Recurring batch| A batch that will be posted repeatedly, according to the selected frequency. An example of a recurring batch would be one to record monthly rent expense. In Australia and New Zealand, transactions entered in a recurring batch are referred to as standing transactions.|
|Report option|A collection of entries that specify the amount or type of information that  will appear on a report. You can create multiple report options.|
|Removing history|A procedure that erases ranges of account or transaction history. Removing history will remove ranges of history that are no longer useful, making additional hard disk space available.|
|Report Writer|A Microsoft application that can be used to create customized reports.|
|Rounding difference account|A multicurrency posting account that recognizes a difference between debit and credit amounts for originating transaction amounts. The difference might be because of how accounts are split to update posting accounts using the exchange rate for the transaction.|
|Series posting|A posting process in which marked batches from the same series can be posted simultaneously.|
|Source document code|A code that identifies the type of journal or entry that you can examine for more information about a specific transaction. For example, you could use the source document code BRDEP for Bank Reconciliation deposits.|
|Tab-delimited format|A tab-separated ASCII character file format used when exporting a report so that it can be read by programs that use this format.|
|Text-only format|A file format that saves reports as text without formatting. This format is used when exporting reports to applications that are unable to read other formats available in Dynamics GP.|
|Transaction|An event or condition that is entered in asset, liability, expense, revenue, or equity accounts. Checks and withdrawals are two types of transactions.|
|Transaction history|Transactions that have been reconciled or voided.|
|Transaction-level posting|A posting method in which you can enter and post transactions without having to create a batch. Also known as real-time posting.|
|Transfer|A transaction used to enter a transfer of funds from one checkbook to another.|
|Typical balance|Yhe type of balance, either debit or credit, an account has under ordinary circumstances. Asset and expense accounts normally have debit balances, while liability, revenue, and equity accounts normally have credit balances.|
|Withdrawal|A removal of cash from a checkbook for business or personal use.|
