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


## More terms

#### Accounting period

>   A subdivision of the fiscal year. Common periods are months or quarters.

#### Active customer

>   A customer with whom you’re currently doing business on a regular basis.

#### ADTP (Average days to pay)

>   An average based on the number of invoices a customer has and the time taken
>   to pay each invoice. The formula for calculating the average days to pay is:
>   ADTP = (Current ADTP) x (Number of Invoices) + (Number of Days Taken to Pay
>   Most Recent Invoice) / (Number of Invoices + 1).

#### Aged Trial Balance

>   The Aged Trial Balance shows the balances for each aging period as of the
>   last aging date. You can print the Aged Trial Balance to view the current
>   aging status of accounts.

#### Aging

>   The process that determines the maturity of an account from the transaction
>   date or due date, indicating how many days each account has been
>   outstanding. Aging places each posted transaction in the appropriate
>   current, past-due, or days old aging period.

#### Aging period

>   A specified number of days to age your accounts by. For example, your aging
>   periods might be from 0 to 30 days, 31 to 60 days, and so on. Up to seven
>   aging periods can be used for open item accounts and two periods (current
>   and non-current) for balance forward accounts.

#### Alignment form

>   A document printed to ensure text is properly aligned before you print
>   actual statements.

#### Apply

>   The process of linking a payment amount to one or more documents being paid.

#### Audit trail

>   A series of permanent records that you can use to track a transaction to the
>   point it was originally entered in Microsoft Dynamics GP. You can use the
>   audit trail to verify the accuracy of sales records by outside accountants
>   or auditors.

#### Audit trail code

>   A code providing a precise record of each transaction and its origin within
>   the Microsoft Dynamics GP system.

#### Auto apply

>   Applies selected cash receipts, credit memos, and returns to a customer’s
>   oldest documents. During setup you can select whether to apply the amounts
>   to documents with the oldest due dates or those with the oldest document
>   dates. *See also Apply*.

#### Background processing

>   A processing system you can use to continue working while transactions are
>   being posted or reports are being printed.

#### Backing up

>   The process of storing data on a secondary medium, usually diskettes or
>   magnetic tape, to minimize the difficulty of recovering from data loss.
>   Backups should be performed routinely.

#### Balance

>   The difference between the debit amount and the credit amount of a
>   particular account.

#### Balance brought forward

>   Balance for each account that is carried forward to the next period.

#### Balance forward account

>   An account type that records all documents entered during the current period
>   and the balance brought forward amount for prior periods. Cash receipts are
>   applied to the oldest balance, not to specific transactions.

#### Batch

>   A group of transactions identified by a unique name or number. Batches are
>   used in computerized accounting to conveniently group transactions, both for
>   identification purposes and to make posting the transactions easier.

#### Batch frequency

>   An option that determines how often a recurring batch will be posted, such
>   as weekly, monthly, or quarterly.

#### Batch inquiry

>   A window that shows the users that are currently working with batches and
>   the statuses of those batches.

#### Batch posting

>   An option used to post batches—groups of transactions identified by a unique
>   name or number—within a module one at a time.

#### Batch-level posting

>   A posting method that enables transactions to be saved in batches; the batch
>   is posted whenever convenient. There are three types of batch-level posting:
>   batch, series, and master.

#### Beginning balance

>   Those balances either entered during the setup of your Microsoft Dynamics GP
>   system or carried forward from the preceding fiscal year.

#### Calendar year

>   An accounting cycle beginning on January 1 and ending on December 31.

**Calendar-year history**

>   A record of transactions by calendar months.

#### Cash receipt

>   A document used to record payments and deposits received from customers.

#### Child customer ID

>   Customers assigned to a national account parent. Typically, invoices
>   originate with the child customers of the national account.

#### Class

>   Enables customers, vendors, users, or items to be grouped according to
>   common characteristics. For example, a customer class could be created to
>   group customers according to credit limit or location.

#### Comma-delimited field

>   The standard comma-separated ASCII character format used when exporting a
>   report so database programs can read it.

#### Commission

>   The amount, usually a percentage of the sale amount, paid to the salesperson
>   who made the sale.

#### Consolidating

>   A period-end procedure that draws together individual transaction amounts
>   into a single summary transaction balance. Typically, this procedure is used
>   for balance forward account types before a balance is brought forward to the
>   next period.

**Credit limit** A limit on the amount a customer can purchase on account.

#### Credit memo

>   A document that credits a customer’s account and explains the reason for the
>   credit.

**Credit receipt** *See Credit memo*.

#### Credit terms

>   Conditions agreed upon when credit is granted.

#### Customer ID

>   An alphanumeric identification assigned to customers using the Customer
>   Maintenance window. You can use the customer ID to sort information on
>   reports.

#### Debit memo

>   A document that debits a customer’s account and explains the reason for the
>   debit.

#### Default class

>   A class whose values are used for the creation of new classes.

#### Default entry

>   A value displayed in a window automatically; used unless a different value
>   is entered.

#### Discount available

>   A reduction in the amount receivable, offered if the payment is made by a
>   certain date.

#### Discount date

>   The date an invoice must be paid in order for a discount to be valid.

#### Discount taken

>   The discount amount customers take from their available payment terms
>   discount. *See also Discount available*.

#### Distributing

>   The process of allocating to separate accounts a percentage or part of
>   transaction amounts.

#### Distribution account

>   An account designated to receive a percentage or part of a posted
>   transaction.

#### Distribution history

>   A record of the debits and credits for each document distributed to
>   individual posting accounts.

#### Document

>   All the information entered for a single, complete transaction, including
>   distribution amounts.

#### Document number

>   The number assigned to any document recorded in Receivables Management, such
>   as sales, credit memos, and payments.

#### Document type

>   An option that identifies a document’s purpose and how document amounts will
>   be posted. In Receivables Management, the document types include
>   sales/invoices, debit memos, finance charges, services/ repairs, warranties,
>   credit memos, returns, and cash receipts.

#### EFT (Electronic Funds Transfer)

>   A service provided by banks in conjunction with businesses to have money
>   moved in and out of an account.

#### Exchange rate

>   The rate of exchange between two currencies on a particular date and time.

#### Exchange rate source

>   The service, publication, or institution exchange rates are obtained from.
>   For example, you can use rates from a local bank, a financial journal, or an
>   electronic service such as CompuServe.

#### Exchange rate table

>   A table used to store exchange rates for a unique combination of currencies
>   and rate types. These tables also are used to define selections for
>   determining the exchange rate that will be used when the currency for a
>   table is entered on a multicurrency transaction.

#### Finance charge

>   The cost of borrowing money; usually a charge assessed to overdue accounts.
>   Also a document type used to record a finance charge.

**Financial year**

>   *See Fiscal year*.

#### Fiscal year

>   An accounting cycle composed of up to 54 consecutive periods. In Australia
>   and New

>   Zealand, this is referred to as a financial year.

#### Fiscal-year history

>   A record of sales, commission amounts, and other transactions organized by
>   fiscal periods.

#### Functional amount

>   The equivalent transaction amount in the functional currency for a
>   transaction amount that was entered using an originating currency. This
>   amount sometimes is referred to as the functional equivalent of the
>   originating amount.

#### Functional currency

>   The primary currency a company keeps its financial records in. Typically,
>   the functional currency is the currency for the country/ region where the
>   company is located.

**Functional equivalent**

>   *See Functional amount*.

#### Grace period

>   A period of days added to end-of-month (EOM) terms to prolong the payment
>   due date for purchases made during the last few days of the month. For
>   example, with a grace period of five days, a purchase made on December 28 or
>   later would not be due until the end of January.

#### Group printing

>   Saving and printing reports in groups. For example, you can create a report
>   group used to print the Salesperson Commission Summary and Sales Territory
>   Commission Summary before closing a fiscal year. You can create groups of
>   reports within the same series and groups of series report groups.

#### GST (Goods and Services Tax)

>   A tax on the consumption of goods and services used in Canada, New Zealand,
>   and other countries/regions.

#### Historical Aged Trial Balance

>   A Receivables Management report that projects the balances in each aging
>   period by aging the accounts; for reporting purposes only. *See also ADTP
>   (Average days to pay)*.

#### History

>   A record of paid transactions or account balances.

#### Hold

>   A restriction that prevents certain types of transactions from being entered
>   for a specified record. For example, you can place a customer with a past
>   due balance on hold.

#### HTML (Hypertext Markup Language)

>   A format that you can view using a web browser. Use this format for reports
>   placed on your company’s intranet.

#### Inactivate

>   The process of making customer cards inactive. If you inactivate customer
>   cards, you won’t be able to post any of their transactions—sales or
>   payments.

#### Inactive customer

>   A customer with whom business isn’t being conducted any longer. Typically,
>   records for these customers can’t be deleted because historical records are
>   being kept.

#### Inquiry

>   Enables you to view open-year and historical information.

#### Intrastat statistics

>   The system for collecting statistics on the trade of goods between European
>   Union countries/regions.

#### Invoice

>   A document that records the prices and other details of goods and services
>   sold or supplied.

#### Lockbox

>   A place where bills that are paid every month are stored at a bank. The bank
>   locks this money away to pay certain bills.

#### Lookup window

>   A window that displays a list of accounts, customers, documents, or other
>   items in the Microsoft Dynamics GP system. Lookup windows for a specific
>   field are displayed by choosing the magnifying glass button next to the
>   field.

#### Master posting

>   A posting process where all batches marked to post, in all modules, are
>   posted regardless of who marked them.

#### Miscellaneous charge

>   A charge that isn’t part of a normal purchasing process. A miscellaneous
>   charge might be a service charge such as installation or repair of
>   merchandise, or a shipping and handling fee on a credit card purchase.

#### Multiple addresses

>   Locations in addition to a company’s main location. For example, a business
>   with several stores can specify an address for each location.

#### Multiple companies

>   Companies separate data folders have been established for. Enables you to
>   keep a separate set of financial information for each company you operate.

#### National account

>   A combination of related customers that make up a single organization. The
>   parent customer is the controlling customer of the national account. This
>   parent customer has child customers, and is usually the customer who
>   distributes payments on behalf of the child accounts.

#### NSF (Non-sufficient funds)

>   The process of assessing a charge to payments, such as checks, with
>   insufficient funds. If you mark a payment as NSF, the system unapplies the
>   payment, backs out the distributions, and increases the amount in the
>   Receivables account while decreasing the amount in the Cash account.

#### Open item account

>   An account type that shows details of all transactions not fully applied.
>   Open item accounts enable cash receipts to be applied to specific invoices.

#### Open transaction

>   A posted transaction. You can apply or unapply this transaction.

#### Origin

>   A transaction entry window within a specific Microsoft Dynamics GP module.
>   You can select certain options, such as closing fiscal periods, for each
>   transaction origin. The transaction origin appears as part of the audit
>   trail code on all posting reports in Microsoft Dynamics GP.

#### Originating amount

>   The transaction amount in the currency the transaction was entered in.
>   Originating amounts are posted along with their corresponding functional
>   amounts, also referred to as functional equivalents.

#### Originating currency

>   The currency a multicurrency transaction was conducted in.

#### Paid transaction removal

>   A procedure used to transfer paid transactions to history and to consolidate
>   balance forward account balances. If you’re not keeping history, this
>   procedure deletes paid transactions from your records.

#### Parent customer ID

>   The controlling customer of a national account; has child customers. The
>   parent customer usually distributes payments on behalf of the child
>   customers.

#### Payment terms

>   Conditions for payment agreed upon when a sales transaction takes place.
>   Payment terms might include a discount to the selling price if the payment
>   is received within a certain time period.

**Postal code**

>   *See ZIP code*.

#### Posting

>   A procedure that makes temporary transactions a part of your business
>   records; permanent records are updated with the amount of these
>   transactions. In manual accounting, to transfer journal totals to the
>   appropriate accounts in a ledger.

#### Posting account

>   A financial account that tracks assets, liabilities, revenue, or expenses.
>   Amounts posted to these accounts appear on the Profit and Loss Statement,
>   the Balance Sheet, and other financial reports if you use General Ledger.

#### Posting date

>   The date a specific transaction was posted to your company’s posting
>   accounts.

#### Posting journal

>   A report printed following the posting process that shows the detail for
>   each transaction that’s been posted. Posting journals include the audit
>   trail code, which provides a precise record of where each transaction has
>   been posted within Microsoft Dynamics GP.

**PST (Provincial Sales Tax)**

>   A tax set by each Canadian province.

#### QST (Québec Sales Tax)

>   The Provincial Sales Tax for the province of Québec. *See also PST
>   (Provincial Sales Tax)*.

#### Range

>   An option used to narrow the amount of records printed on a report. For
>   example, a selected range of customer IDs could be those between Acme
>   Company and Limited, Inc.

#### Rate calculation method

>   A mathematical operation (multiply or divide) specified for calculating
>   functional and originating equivalents on a transaction, or for displaying
>   amounts in summary or inquiry windows. The exchange rate on the exchange
>   rate table is used in the calculation. The operation is used to calculate a
>   functional currency amount from the originating currency amount using a
>   specified exchange rate.

#### Rate frequency

>   The frequency you should enter new exchange rates for an exchange rate
>   table. The rate frequency is used to determine the length of time an
>   exchange rate is valid. For example, you can mark a rate as valid for a
>   single day, week, month, quarter, or year. The rate frequency determines the
>   expiration date for each rate, based on the day the rate is entered.

#### Rate type

>   An option used to identify different exchange rate tables for one currency
>   that are used for different purposes. For example, you might set up exchange
>   rate tables with a Buy rate type for sales transactions and a Sell rate type
>   for purchasing transactions. You also can use rate types to distinguish the
>   posting accounts that are used for realized gains and losses and rounding
>   differences.

#### Rate variance

>   A range you can specify to limit the amount the exchange rate can fluctuate
>   when you enter a new exchange rate in an exchange rate table or during the
>   transaction entry. For example, if the default exchange rate is 0.68450 and
>   the rate variance is 0.01000, you could enter an exchange rate between
>   0.67450 and 0.69450.

**Real-time posting**

>   *See Transaction-level posting*.

#### Realized gain

>   Gain realized in the functional currency because of the difference in
>   exchange rates between the transaction date and the settlement date for a
>   multicurrency transaction.

#### Realized loss

>   Loss realized in the functional currency because of the difference in
>   exchange rates between the transaction date and the settlement date for a
>   multicurrency transaction.

#### Reconciling

>   A procedure used to verify that Receivables Management data is accurate. The
>   reconcile process verifies, and recalculates if necessary, the accuracy of
>   the account balances and document ages in each aging period.

#### Recurring batch

>   A batch that you can post repeatedly.

#### Recurring transaction

>   Transactions, such as membership dues, that occur repeatedly over time. In
>   Australia and New Zealand these transactions are referred to as standing
>   transactions.

#### Refund check

>   A transaction used to transfer receivables balances to Payables Management.
>   Receivables debit documents and payables miscellaneous charge documents are
>   created for each customer that refund checks are created for.

#### Removing history

>   A procedure used to erase ranges of account or transaction history that are
>   no longer useful.

#### Report option

>   A collection of entries that specifies the amount or type of information
>   that appears on a report. You can create multiple report options.

#### Reporting currency

>   The currency used to convert functional currency amounts to another currency
>   on inquiries and reports.

#### Return

>   A transaction that records the return of merchandise after the invoice for
>   the sale has been posted. Returns are applied to the original invoice (for
>   open item customers) or to the customer’s balance (for balance forward
>   customers).

#### Roll down

>   Applies changes you’ve made to a class record to all customer records within
>   the class. For example, if you change the payment terms for the class from
>   Net 30 to 2%-10/Net 30, you can roll down the change to all records in the
>   customer class.

**Sales tax detail**

>   *See Tax detail*.

**Sales tax schedule**

>   *See Tax schedule*.

#### Sales territory

>   A division of the regions a company’s products are sold in, separated from
>   other divisions oftentimes by geographical location. In Microsoft Dynamics
>   GP, you can track sales and commissions for each sales territory.

#### Salesperson

>   A person who sells a company’s goods or services.

#### Sample data

>   Data that you can use to practice Microsoft Dynamics GP procedures by
>   entering the information listed in the online lessons. You can use sample
>   data using the lesson company.

#### Series

>   A group of Microsoft Dynamics GP modules that form an interrelated set of
>   applications.

#### Series posting

>   A posting process where you can post batches for a series marked by a
>   particular user.

#### Service/Repair

>   A document that records the charges for services or repairs provided.

#### Short name

>   A shortened version of a customer name that you can print on reports when
>   full names are too long.

**Single-use batch**

>   A batch posted only once, then deleted.

#### Splitting commissions

>   A method of dividing commission amounts or percentages among two or more
>   salespeople.

**Spot rate**

>   The exchange rate used for the day.

**Standing transaction**

>   *See Recurring transaction*.

#### Statement

>   A record of customer activity including aging period information, the total
>   amount due, and payments received.

#### Statement name

>   A name printed on statements that replaces the customer’s name as it appears
>   in the Customer Name field. Statement names often are used to print the
>   customer’s first name first on the statements. For example, the customer
>   name Goodwin, Gayle could be printed as Gayle Goodwin on statements.

#### Tab-delimited field

>   The tab-separated ASCII character format used when exporting a report.

#### Table

>   A collection of related records, such as transactions or accounts. All the
>   accounting information you enter in Microsoft Dynamics GP is stored in
>   tables. Formerly referred to as file or data file.

#### Tax detail

>   A definition of each tax that might apply to customers. Tax details are
>   grouped into tax schedules. *See also Tax schedule*.

#### Tax schedule

>   Groups of tax details. When you assign tax schedules to customers, Microsoft
>   Dynamics GP calculates the applicable taxes during transaction entry. *See
>   also Tax detail*.

#### Text file (text only)

>   A file format that saves reports as text without formatting. This option
>   should be used when the application you’re converting the document to is
>   unable to read any of the other file formats.

#### Trade discount

>   A discount a customer always receives. The rate is calculated at the time of
>   a sale and is given in addition to any payment terms discounts that also
>   might be offered.

#### Transaction history

>   A record of the transactions that have been entered and fully paid in
>   Receivables Management. If you’re not keeping history, the paid transaction
>   removal deletes paid transactions from your records.

#### Transaction-level posting

>   A posting method that enables you to enter and post transactions
>   individually without having to create a batch.

#### Trial Balance

>   A Receivables Management report that illustrates the outstanding balances
>   and the aging periods for each customer account.

#### Unapply

>   A procedure that reverses the entries that applied amounts to documents.

#### Unrealized gain

>   Gain because of the difference in exchange rates between the transaction
>   date and the revaluation date for an account with multicurrency activity.

#### Unrealized loss

>   Loss because of the difference between the transaction date and the
>   revaluation date for an account with multicurrency activity.

#### User-defined field

>   Two fields in the Customer Maintenance window that you can define to track
>   information specific to your business.

#### VAT (Value-added Tax)

>   A tax on goods and services used throughout Europe and elsewhere in the
>   world.

#### Voiding

>   The process of recording an equal and opposite transaction to undo the
>   effects of a posted transaction.

#### Waiving

>   To remove a finance charge that already was assessed.

#### Warranty

>   A document that records a service or repair charge covered by a warranty.

#### Writeoff

>   A process used to adjust small differences between an invoice amount and a
>   payment.

#### Year-end closing

>   The process used to transfer current-year amounts to last-year amounts.

#### ZIP code

In the United States, the postal code assigned to business and residential
addresses. In other countries/regions, it might be referred to as post code or
postal code.