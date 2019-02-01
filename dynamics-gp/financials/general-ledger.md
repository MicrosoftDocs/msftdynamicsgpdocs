---
title: "General Ledger"
description: "The general ledger in Dynamics GP"
keywords: "purchase order"
author: tnistler
manager: edupont

ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: tnistler
ms.date: 01/30/2019

---
# Dynamics GP General Ledger

You can use General Ledger to enter a chart of accounts and post beginning balances. You can set up budgets in Microsoft Dynamics® GP or use Microsoft® Excel® to set them up. You can export budgets from Microsoft Dynamics GP to Excel, modify them, or distribute worksheets to budget managers for review and input, then import the modified budgets back into Microsoft Dynamics GP. If you use a predefined chart of accounts, you can quickly print financial statements or modify them using Advanced Financial Analysis or Management Reporter for Microsoft Dynamics ERP.

You also can use General Ledger to complete the following tasks:

-   Enter and post standard or correcting transactions

-   Enter unit accounts that capture non-financial data, and fixed or variable allocation accounts that allow you to efficiently distribute amounts among multiple accounts

-   Set posting options that allow you to post transactions from subsidiary ledgers to General Ledger, where can review and them and make correcting entries, if necessary, or post them through General Ledger in a single step

-   Void or delete unposted transactions easily, back out or reverse posted transactions, and post corrected entries—all with a complete, clear audit trail

-   Bring greater efficiency to recurring transactions by defining quick journal transactions that can be posted repeatedly with minimal changes

-   Filter account views based on access granted for accounts, increasing security and eliminating errors caused when entries are made to inappropriate accounts

If you’re using Intercompany Processing, you post transactions across companies and print consolidated financial statements. For more information, see the Intercompany Processing documentation.

If you are using Analytical Accounting, you can set up dimension codes and account classes that provide greater flexibility in analyzing transaction data. For more information, see the Analytical Accounting documentation.

>   **What’s in this manual**

This manual is designed to give you an understanding of how to use the features of General Ledger, and how it integrates with the Microsoft Dynamics GP system.

To make best use of General Ledger, you should be familiar with systemwide features described in the System User’s Guide, the System Setup Guide, and the System Administrator’s Guide.

>   Some features described in the documentation are optional and can be purchased through your Microsoft partner.

>   To view information about the release of Microsoft Dynamics GP that you’re using and which modules or features you are registered to use, choose Help \>\> About Microsoft Dynamics GP.

>   The manual is divided into the following parts:

-   *Part 1, Setup*, describes how to set up General Ledger so that it meets the needs of your business and works with other modules that you use.

-   *Part 2, Budgets*, describes how to create a new budget in Microsoft Dynamics GP or in Microsoft Excel.

-   *Part 3, Transactions*, provides procedures for completing General Ledger accounting tasks.

-   *Part 4, Inquiries*, shows how to view both current and historical account, budget, and transaction information.

-   *Part 5, Reports*, describes how to use reports to analyze transaction and account information, and how to display the information on a computer screen or on a printed report, or to save it to a file.

-   *Part 6, Utilities and routines*, provides the procedures that you need to maintain your data in General Ledger. Information about creating and modifying checklists for General Ledger routines for the end of a month, quarter, or year also are included.

**Part 1: Setup**

>   Use the following information to set up General Ledger. Setup procedures generally need to be completed once, but you can refer to the information at other times for instructions on modifying or viewing existing entries.

>   The following information is discussed:

-   *Chapter 1, “General Ledger setup,”* describes how to use the setup routine to correctly set up General Ledger.

-   *Chapter 2, “Understanding accounts,”* describes the types of accounts that make up your chart of accounts.

-   *Chapter 3, “Posting accounts,”* describes how to set up posting accounts to track your assets, liabilities, revenue, expenses, and equity.

-   *Chapter 4, “Unit accounts,”* describes setting up accounts to track nonfinancial quantities.

-   *Chapter 5, “Fixed allocation accounts,”* describes setting up accounts to distribute fixed amounts among several accounts.

-   *Chapter 6, “Variable allocation accounts,”* describes setting up accounts to distribute variable amounts among several accounts.

-   *Chapter 7, “Retained earnings accounts,”* describes how to set up retained earnings accounts to use during the year-end closing process.

-   *Chapter 8, “Chart of accounts,”* contains information about setting up a chart of accounts.

-   *Chapter 9, “Beginning balances and history,”* describes how to enter beginning balances and history.

-   *Chapter 10, “Quick journal transactions setup,”* describes how to set up quick journals for time-saving journal entry.

-   *Chapter 11, “Revenue/Expense Deferrals setup,”* provides instructions for setting up Revenue/Expense Deferrals.

**Chapter 1: General Ledger setup**

>   One way to set up General Ledger is to follow the setup routine provided. It guides you through the procedures you need to complete, in the order you need to complete them.

>   This information is divided into the following sections:

-   *Before you begin setting up General Ledger*

-   *Setting up default entries and preferences*

-   *Understanding net change and period balance*

-   *Setting up transaction matching*

#### Before you begin setting up General Ledger

>   Before setting up General Ledger, be sure you’ve set up all of the following for the company:

-   Account format

-   Fiscal periods

-   Posting

-   Source documents

-   Audit trail codes

>   For more information about setting up your system and company, refer to the

>   System Setup instructions (Help \>\> Contents \>\> select Setting Up the System).

#### Setting up default entries and preferences

>   Use the General Ledger Setup window to specify the next journal entry number, indicate how account balances will appear in the General Ledger Account Maintenance and Transaction Entry windows, as well as other Microsoft Dynamics GP windows, and select the type of historical information to save. You also can restrict or allow specific actions, such as posting to historical years, deleting saved transactions.

>   The General Ledger Setup window also allows you to enable base, local, and International Financial Reporting Standards (IFRS) ledgers. After this process, users who are entering General Ledger transactions can assign the transactions to these specific reporting ledgers.

>   **To set up default entries and preferences:**

1.  Open the General Ledger Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> General Ledger)

![](media/591eb60045c794b3d94704814b39f488.jpg)

2.  Enter the next journal entry and budget journal entry numbers. A new journal entry number is assigned each time you save an entry in the Transaction Entry, Clearing Entry or Quick Journal Entry windows. A new budget journal entry is assigned each time you save an entry in the Budget Transaction Entry window.

>   The journal entry and budget journal entry number appears on reports as part of your audit trail. You can use these numbers to trace transactions to their original point of entry.

3.  Choose whether to display account balances as net change or period balance amounts.

>   The display method you select will appear throughout Microsoft Dynamics GP. You can change the method in each window where the account balances are displayed. Refer to *Understanding net change and period balance* for more information.

4.  Skip the retained earnings entries.

>   You need to enter the chart of accounts before specifying a retained earnings account. Later, after you’ve set up posting and fixed allocation accounts, you can refer to *Chapter 7, “Retained earnings accounts,”* for more information about this entry.

5.  Choose whether to keep account history, transaction history, budget transaction history, or all three.

>   Account history provides account summary balances only. Transaction history includes all transactions posted to an account. Budget transaction history retains the history of budget adjustments. When budget transactions are posted, they move directly to the history table because there is no open table for these transactions. Thus, you must choose an option here if you want to do inquiries on budget transactions after they have been posted.

>   You can keep history for an unlimited number of years. This information is updated during the year-end closing process when current-year balances become previous-year balances.

>   If you choose to keep history, you can print historical information on financial statements, comparing previous-year amounts to current-year amounts. You also can calculate budgets based on information from a previous year.

6.  Mark whether to enable users to post to history. If this checkbox is marked, you can post transactions to the most recent history year. For example, you can post audit adjustments after you have closed the year.

7.  Mark the Deletion of Saved Transactions option to enable users to delete transactions that are saved, but not posted. If you unmark this option, saved transactions must be voided instead of deleted.

8.  Mark the Voiding/Correcting of Subsidiary Transactions option to enable saved transactions originating in other modules to be voided or posted transactions originating in other modules to be backed out or backed out and corrected. Voiding saved transactions originating in other modules will not update the transactions in those modules. You must void or delete the originating transactions using the originating modules.

9.  Mark the Back Out of Intercompany Transactions option to enable intercompany transactions to be backed out.

10.  Mark whether to update the accelerator information.

>   Mark the Update Accelerator Information option if you want to update row and column information on financial statements each time you modify the layout of an existing financial report using Advanced Financial Analysis.

>   *If you don’t use account ranges and wildcard characters in your financial statements, you don’t need to mark this option. For more information about financial statements, refer to Chapter 30, “Financial statement reports.”*

11.  Mark whether to allow reporting ledgers.

>   *Allowing reporting ledgers is a permanent selection after you save your changes by clicking OK. You cannot unmark Allow Reporting Ledgers later.*

>   When you mark this option:

-   The reporting ledger types Base, IFRS, and Local become available for the selected account. Later, transactions for this account can be assigned to one of these reporting ledger types. For more information on assigning a transaction to a reporting ledger type, see *Chapter 18, “Standard and reversing transactions.”*

-   You can change the description for each reporting ledger type.

-   When you mark this option, the Account Balance for Subsidiary Windows list becomes active. This list lets you decide which reporting ledger types are used to calculate account balances that appear in Microsoft Dynamics GP modules other than General Ledger.

>   If you do not mark this option, all transactions for the selected account are assigned to the Base ledger.

>   Definitions of the reporting ledger types:

-   Base represents the base ledger, where the transactions can be applied for both local and IFRS accounting. All transactions originating sub-ledger modules are applied to the base ledger by default.

-   IFRS represents the IFRS ledger, where the transactions can be applied for IFRS accounting.

-   Local represents the local ledger, where the transactions can be applied for local accounting.

>   The local and IFRS ledger types allow you to enter similar transactions and assign them to a specific reporting ledger, which can vary because the accounts or amounts might differ on the accounting rules that are applied when determining the accounting transaction.

12.  In the Account Balance for Subsidiary Windows list, choose the reporting ledger types that you want to use to calculate balances for accounts that appear outside of General Ledger.

>   Review the setup options you’ve entered on the Setup List report. To print the list, choose File \>\> Print or the printer icon button while the General Ledger Setup window is displayed.

#### Understanding net change and period balance

>   You can view the status of your accounts by net change or in a period-by-period format. Some windows display both net change and period balances.

>   If you choose net change, the amount displayed is the difference between each period and the preceding period, whether positive or negative.

>   If you choose period balances, the actual balance for each period is displayed. Refer to the table for an example of how the same information is displayed, depending on the display setting you choose.

| **Period** | **Net change** | **Period balance** |
|------------|----------------|--------------------|
| Period 1   | \$100.00       | \$100.00           |
| Period 2   | \$100.00       | \$200.00           |
| Period 3   | \$0.00         | \$200.00           |
| Period 4   | \$50.00        | \$250.00           |

>   The display method you choose in the General Ledger Setup window will be used as the default throughout Microsoft Dynamics GP; however, you can change the method in each window where account balances are displayed.

#### Setting up transaction matching

>   Transaction matching is the process of linking related transaction distributions from different journal entries. For example, you can link period-end adjusting entries to the original transactions, or link a set of transactions associated with a project. You can also create groups of linked transaction distributions. For example, you could create a group of the links for period-end adjustments to aid in the audit process.

>   Use the Transaction Matching Setup window to set the options you want to use for linking transactions, including whether you want to require the transactions you link to balance, the next number to use for links, and whether you want to enable links to be deleted.

>   **To set up transaction matching:**

1.  Open the Transaction Matching Setup window.
>   (Financial \>\> Setup \>\> Financial \>\> Transaction Matching)

![](media/98fc3851d8517db0b0ffe6e6aeee257b.jpg)

2.  Enter the default next link number.

3.  Indicate whether you want to require linked distributions to balance.

>   When you link transaction distributions in the General Ledger Transaction Link Maintenance window, the credits and debits are totaled and the balance  is displayed. If you mark this option, linked distributions must balance (that is, total debits must equal total credits) before the link can be saved.

4.  Indicate whether you want to require linked distributions to be for a single account only.

>   For example, assume you want to be able to link distributions to the accounts for Finance Charge Income and Interest Income. If you mark this option, you won’t be able to establish this link. If you don’t mark this option, you can establish this link.

5.  Indicate whether you want to enable saved links to be deleted. If you mark this option, you can choose Deletion Password to enter a password that must be entered before a link can be deleted.

6.  Choose OK to save your entries and close the window.

**Chapter 2: Understanding accounts**

>   Your chart of accounts will include several types of accounts. This part of the documentation describes the different types of accounts and how account categories are used to group accounts on financial statements.

>   This information is divided into the following sections:

-   *Posting, unit, and allocation accounts*

-   *Understanding account categories*

-   *Maintaining account categories*

-   *Understanding account aliases*

-   *Using an account alias during data entry*

-   *User-defined fields for accounts*

#### Posting, unit, and allocation accounts

>   A chart of accounts can include three types of accounts: posting, unit, and allocation accounts. Each type can be used to meet different business needs.

>   **Posting accounts** Posting accounts are the financial accounts that track assets, liabilities, revenue, expenses, and equity. Transactions posted to these accounts appear on financial reports. Examples of posting accounts include Cash, Cost of Goods Sold, and Accounts Receivable. For more information, see *Chapter 3, “Posting accounts.”*

>   **Unit accounts** Unit accounts are similar to posting accounts. Like posting accounts, unit accounts are used in transaction entry. Historical information and budgets can be maintained for both types of accounts. However, quantities—rather than amounts—are posted to unit accounts, and unit accounts don’t appear on financial statements. For more information, see *Chapter 4, “Unit accounts.”*

>   **Allocation accounts** Allocation accounts are used to distribute percentages of a single transaction among several accounts. Two different types of allocation accounts are available: fixed and variable. For more information, see *Chapter 5,* *“Fixed allocation accounts,”* and *Chapter 6, “Variable allocation accounts.”*

#### Understanding account categories

>   All posting accounts are assigned to account categories, which are used to group accounts on financial statements. For example, all accounts assigned to the Cash category—Petty Cash, Cash-Operating, Cash Payroll—will appear under the Cash category when financial statements are printed. You also can choose whether to print descriptions for the first account in the category or print the category description.

>   General Ledger includes 48 predefined account categories. The account categories can be displayed in the Account Category Setup window. The account categories provided with General Ledger, their type (balance sheet, profit and loss, or statement of changes) and the financial statements that include each account category are listed in the following table:

| **Category**                          | **Type**                  | **Appears on:**                                                 |
|---------------------------------------|---------------------------|-----------------------------------------------------------------|
| Cash                                  | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| **Category**                          | **Type**                  | **Appears on:**                                                 |
| Short-Term Investments                | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| Accounts Receivable                   | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| Inventory                             | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| Notes Receivable                      | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| Work in Process                       | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| Prepaid Expenses                      | Balance Sheet             | Balance Sheet Statement of Cash Flows                           |
| Long-Term Investments                 | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Property, Plant, and Equipment        | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Accumulated Depreciation              | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Intangible Assets                     | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Other Assets                          | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Accounts Payable                      | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Notes Payable                         | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Current Maturities of Long- Term Debt | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Taxes Payable                         | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Interest Payable                      | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Dividends Payable                     | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Leases Payable (Current)              | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Sinking Fund Payable (Current)        | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Other Current Liabilities             | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Long-Term Debt                        | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Common Stock                          | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Preferred Stock                       | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Additional Paid-in Capital– Common    | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| Additional Paid-in Capital– Preferred | Balance Sheet             | Balance Sheet Statement of Cash Flows                                        |
| **Category**                          | **Type**                  | **Appears on:**                                                              |
| Retained Earnings                     | Balance Sheet             | Balance Sheet                                                                |
| Treasury Stock                        | Balance Sheet             | Balance Sheet                                                                |
| Common Dividends                      | Balance Sheet             | Balance Sheet                                                                |
| Preferred Dividends                   | Balance Sheet             | Balance Sheet                                                                |
| Sales                                 | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Sales Returns and Discounts           | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Cost of Goods Sold                    | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Selling Expense                       | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Administrative Expense                | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Salaries Expense                      | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Other Employee Expenses               | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Interest Expense                      | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Tax Expense                           | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Depreciation Expense                  | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Income Tax Expense                    | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Other Expenses                        | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Other Income                          | Profit and Loss Statement | Profit and Loss Statement                                                    |
| Charges Not Using Working             | Statement of changes      | Statement of Cash Flows                                                      |
| Revenues Not Producing                | Statement of changes      | Statement of Cash Flows                                                      |
| Gain/Loss on Asset Disposal           | Statement of changes      | Statement of Cash Flows                                                      |
| Amortization of Intangible            | Statement of changes      | Statement of Cash Flows                                                      |
| Nonfinancial Accounts                 | Not applicable            | Nonfinancial accounts (unit accounts) do not appear on financial statements. |

>   Statement of Cash Flows

>   Statement of Retained

>   Earnings

>   Statement of Cash Flows

>   Statement of Cash Flows

>   Statement of Retained

>   Earnings

>   Statement of Cash Flows

>   Statement of Retained

>   Earnings

>   Statement of Cash Flows

>   Capital

>   Working Capital

>   Assets

#### Maintaining account categories

>   Account categories are used to group the posting accounts on financial statements. For example, all accounts in the Cash category—will appear under the Cash category. The default list includes categories such as Cash, Short-Term Investments and Notes Receivable.

>   Use the Account Category Setup window to view and make changes to the descriptions of the account categories. You can customize any account category by changing its description, but the financial statement it appears on will not be changed. In addition, predefined category descriptions cannot  be removed.

>   You can add unlimited account categories if your business has specialized reporting needs. Additional user-defined categories appear after the predefined categories in the scrolling window and are preceded by an asterisk in the Number column. You can remove a user-defined category, only if it has no accounts assigned to it.

>   To revert to the original set of account categories once you've changed them, clear data from the Account Category Table.

>   **To maintain account categories:**

1.  Open the Account Category Setup window.
>   (Financial \>\> Setup \>\> Financial \>\> Category)

![](media/0544c4e6f26f41b4796bed93f5ab725d.jpg)

2.  Rename any predefined categories, if needed.

3.  If your business has specialized reporting needs, you can add user-defined categories by scrolling to the bottom of the list and entering a category description.

4.  You can verify your changes with an Account Category List.

>   To print an Account Category List, choose File \>\> Print or the printer icon button while the Account Category Setup window is displayed.

#### Understanding account aliases

>   An account alias is a 20-character “short name” assigned to an account. You can use an account alias instead of the entire account in any window where you enter or select accounts. If you’re using a large account structure, aliases provide a quick method of data entry.

>   For example, if you’ve set up the Cash Operating account for your main branch as account 1200-0000-2100-0000-0000, you could assign an alias such as \$-CO.

>   You can set up account aliases in the Account Maintenance, Unit Account Maintenance, Variable Allocation Maintenance, and Fixed Allocation Maintenance windows. Using account aliases is optional. You can modify an account alias at any time using the appropriate account maintenance window.

#### Using an account alias during data entry

>   Use the Account Entry window to enter account aliases during transaction entry.

>   **To use an account alias during data entry:**

1.  Open the Account Entry window using any of these methods in a transaction entry window:

    -   Choose the Account expansion button.

    -   Press CTRL+A.

    -   Choose Account Alias from the View menu in any window where you can enter an account.

>   *The View menu and keyboard shortcut are available only when you’re entering account aliases in transaction entry windows.*

![](media/4580237476881bdcbe0f98a2856aadc2.jpg)

2.  Enter or select an alias. As soon as you enter or select an alias, the Account Entry window closes and the transaction entry window is displayed.

>   *You also can choose an alias using the Accounts lookup window. Account aliases are displayed below the account they represent in the Accounts window. When you select an account and then press TAB, the lookup window closes and the account is displayed in the main window.*

3.  Continue entering transaction information.

#### User-defined fields for accounts

>   General Ledger includes four user-defined fields for tracking additional information about each account.

>   For example, to be able to sort groups of accounts, such as Expense-Retail, you can enter Account Group as the label in the User-Defined 1 field. In the Account Maintenance window, you’ll see Account Group as the label for the field that was User-Defined 1, and you can enter Expenses-Retail for the accounts that are in that group. You also will see Account Group as a sorting method on General Ledger account lists. You can use the four user-defined fields to enter and track information for each account.

**Chapter 3: Posting accounts**

>   Posting accounts are the financial accounts used to track assets, liabilities, revenue, expenses, and equity. Transactions posted to these accounts appear on financial reports. Examples of posting accounts include Cash, Cost of Goods Sold, and Accounts Receivable.

>   *If you didn’t install the default chart of accounts when you created the company but you want to use the default chart of accounts now, you must delete the company and recreate it. See the System Administrator’s Guide (Help \>\> Contents \>\> select System Administration) for more information about creating companies.*

>   This information is divided into the following sections:

-   *Setting up a posting account*

-   *Deleting or inactivating a posting account*

#### Setting up a posting account

>   Use the Account Maintenance window to set up a posting account. Before you add accounts to an existing chart of accounts, print a Posting Accounts List (Financial \>\> Reports \>\> Financial \>\> Account) to determine whether accounts should be added to fit the current needs of your business.

>   *As you set up accounts, keep in mind that you can create a basic set of accounts for a department and use the Mass Modify Chart of Accounts window to copy the basic set of accounts to other departments. Refer to Chart of accounts modifications for more information.*

>   **To set up a posting account:**

1.  Open the Account Maintenance window.
>   (Financial \>\> Cards \>\> Financial \>\> Account)

![](media/7a2d24a25334f30e7c82113655828e9e.jpg)

2.  Enter an account identifier using any combination of letters or numbers. You also can enter a description and an alias. Refer to *Understanding account aliases* for more information.

>   If you’ve set up account segments already and you leave the description field blank, The account description will be created automatically by combining the account segment descriptions.

>   To make changes to an existing posting account, enter or select the account.

3.  Indicate whether you want users to be able to manually enter or select this account in transaction or distribution entry windows. If you unmark this option, you will not be able to manually enter this account in a transaction or distribution entry window.

4.  Enter or select the account category.

5.  Specify whether the account typically appears on the Balance Sheet or the Profit and Loss Statement. This selection determines which accounts will be closed at year-end.

>   *If you are unsure of an account’s posting type, refer to Understanding account categories for information about the posting type and financial statements used with each of the account categories. If you’re unsure of the account type or balance, you should contact a certified public accountant.*

6.  Specify the typical balance—debit or credit. Asset and expense accounts normally have debit balances, while liability, revenue, and equity accounts normally have credit balances. For example, your Cash account is an asset account, and it typically should have a debit balance.

2.  If the transaction origin in the Posting Setup window is set up to use
    account settings, decide how much detail to post to this account from each
    series.

    -   Select Detail to post a separate distribution amount to this account for
        each transaction in a batch.

    -   Select Summary to post a summarized total for an entire group of
        transactions to this account.

>   For more information about posting setup, refer to the System Setup
>   instructions (Help \>\> Contents \>\> select Setting Up the System).

1.  Select the series where you expect to use this posting account; the account
    will appear in all lookup windows in the selected series. Use the SHIFT and
    CTRL keys to select more than one series.

2.  Enter additional information in the user-defined fields about the posting
    account that you're setting up. The information will appear on the Posting
    Accounts List and the Accounts List beneath the headings that were entered
    for user-defined fields in the General Ledger Setup window.

3.  Choose Summary to view open-year summary information for the account. Choose
    History to view and enter historical year summary information. For more
    information on entering account balances and history, see *Chapter 9,
    “Beginning balances and history.”*

4.  Choose Budget to enter a budget for the account. You can set up a budget for
    the account now or wait until all accounts have been entered.

5.  Choose Analysis to enter default Multidimensional Analysis information. For
    more information, refer to the Multidimensional Analysis documentation.

6.  If you’re using Multicurrency Management, choose Currency to assign
    currencies to the account.

>   You can mark Revalue Account to revalue the account when the revaluation
>   procedure is performed. Typically, cash accounts for another currency are
>   revalued to calculate the unrealized gain or loss based on fluctuating
>   exchange rates. You can revalue based on the net change amount for the
>   revaluation period or based on the period balance.

1.  Choose Save to save the account. Redisplay the account and choose File \>\>
    Print or the printer icon button to verify your entries with a Posting
    Accounts List.

#### Deleting or inactivating a posting account

>   Use the Account Maintenance window to delete or inactivate an account. If an
>   account has become obsolete and you’re not planning to use it again, you can
>   delete it from the chart of accounts. In other situations, you can
>   inactivate an account because it has year-to-date activity and can’t be
>   deleted from the chart of accounts. If you inactivate an account, you won’t
>   be able to post to that account.

>   To delete an account from the chart of accounts, it must first meet several
>   conditions:

-   No balance

-   No activity for an open period

-   No account history amounts

-   Not part of an allocation account

-   Not part of an unposted transaction

-   No multicurrency data

-   No transaction history records

>   If the account has any activity for an open year, the account can’t be
>   deleted. However, once the year is closed and the above conditions are met,
>   you can remove transaction history for the account and delete it. For more
>   information, see *Removing or printing history*. When you remove transaction
>   history, you won’t be able to view the transaction detail in inquiry or on
>   reports. When you choose to delete an account, all budget information for
>   the account also is deleted.

>   You can inactivate a posting account at any time. Inactive accounts continue
>   to appear on the financial statements if they have year-to-date activity.
>   When you print other reports in General Ledger, such as account lists, you
>   can include inactive accounts.

>   **To delete or inactivate a posting account:**

1.  Open the Account Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Account)

1.  Enter or select the account to delete or inactivate.

**Chapter 4: Unit accounts**

>   Unit accounts track nonfinancial quantities such as employee headcount,
>   square footage or the number of customers with past due accounts.

>   This information is divided into the following sections:

-   *About unit accounts*

-   *Setting up a unit account*

-   *Posting to a unit account*

-   *Deleting or inactivating a unit account*

#### About unit accounts

>   Unit accounts are similar to posting accounts. Both are used in transaction
>   entry, and historical information and budgets can be kept for both types of
>   accounts.

>   When you post to unit accounts, however, you post quantities rather than
>   amounts. Unit accounts don’t appear on financial statements.

>   You can use unit accounts to compare financial and nonfinancial information.
>   You can also use them with posting accounts to calculate information such as
>   sales per employee. Use unit accounts with variable allocation accounts to
>   allocate amounts such as rent expense to each department based on its square
>   footage. For more information on variable allocation accounts, see *Chapter
>   6, “Variable allocation accounts.”*

#### Setting up a unit account

>   Use the Unit Account Maintenance window to set up or add a unit account.
>   Before you add accounts to an existing chart of accounts, choose File \>\>
>   Print or the printer icon button to print a Unit Accounts List to determine
>   whether accounts should be added to fit the current needs of your business.
>   You also can use this window to view period balances and net change balances
>   for the selected account.

>   **To set up a unit account:**

1.  Open the Unit Account Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Unit Account)

1.  Enter an account identifier using any combination of letters or numbers. You
    also can enter a description and an alias. Refer to *Understanding account
    aliases* for more information.

>   If you’ve set up account segments already and you leave the description
>   field blank. The account description will be created automatically by
>   combining the account segment descriptions.

>   To make changes to an existing unit account, enter or select the account.

1.  Select the number or decimal places for the account’s amounts.

2.  Choose the product series that will use this account.

3.  Choose History to view and enter historical year summary information. For
    more information on entering account history, see *Chapter 9, “Beginning
    balances and history.”*

4.  You can choose Budget to enter a budget for the unit account.

5.  Choose Save to save the account. Redisplay the account and choose File \>\>
    Print or the printer icon button to verify your entries with a Unit Accounts
    List.

#### Posting to a unit account

You can post adjustments to unit accounts in the transaction entry window. The
amount posted to a unit account will not affect the transaction totals or
financial statements. Unit accounts have a debit balance and are assigned to the
non-financial account category. You can enter a one-sided transaction to adjust
a unit account balance.

For example, assume you have set up a unit account to track square footage in a
building. In January, you sign a lease to rent an additional 10,000 square feet
in the building. You can enter a one-sided transaction in the Transaction Entry
window or add a line to an existing transaction to increase the unit account
balance.

#### Deleting or inactivating a unit account

Use the Unit Account Maintenance window to delete or inactivate a unit account.
If an account has become obsolete and you’re not planning to use it again, you
may want to delete it from the chart of accounts. In other situations, you may
want to inactivate an account because it has year-to-date activity and can’t be
deleted from the chart of accounts.

To delete an account from the chart of accounts, it must first meet several
conditions:

-   No balance

-   No activity for an open period

-   No account history amounts

-   Not part of an allocation account

-   Not part of an unposted transaction

-   No multicurrency data

-   No transaction history records

If the account has any activity for an open year, the account can’t be deleted.
However, once the year is closed and the above conditions are met, you can
remove transaction history for the account and delete it. For more information,
see *Removing or printing history*. When you remove transaction history, you
won’t be able to view the transaction detail in inquiry or on reports. When you
choose to delete an account, all budget information for the account also is
deleted.

>   You can inactivate a unit account at any time. Inactive accounts continue to
>   appear on the financial statements if they have year-to-date activity. When
>   you print other reports in General Ledger, such as account lists, you can
>   include inactive accounts.

>   **To delete or inactivate a unit account:**

1. Open the Unit Account Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Unit Account) 2. Enter or select
>   the account to delete or inactivate.

1.  Choose Delete to delete the account. Mark the Inactive box to inactivate the
    account.

2.  Choose Save to save the changes.

3.  Print a Unit Accounts List to review the changes you’ve made to the chart of
    accounts. For more information on printing lists and reports, see *Chapter
    31, “General Ledger reports.”*

**Chapter 5: Fixed allocation accounts**

>   Fixed allocation accounts are used to distribute fixed percentages of a
>   single transaction among several accounts. For example, a fixed allocation
>   account might be used to divide utility expenses among the departments
>   within a company. When

>   you post transactions to allocation accounts, the amounts are allocated to
>   distribution accounts based on percentages you define.

>   Allocation accounts don’t appear on the financial statements—only the
>   corresponding distribution accounts are shown. Once you’ve posted the
>   transaction, the balances of the distribution accounts assigned to the
>   allocation account reflect the changes you’ve made during transaction entry.

>   This information is divided into the following sections:

-   *Setting up a fixed allocation account*

-   *Deleting or inactivating a fixed allocation account*

#### Setting up a fixed allocation account

>   Use the Fixed Allocation Maintenance window to set up a fixed allocation
>   account to distribute fixed percentages of a transaction among several
>   distribution accounts. Distribution accounts can be either posting or unit
>   accounts; however, all distribution accounts assigned to a single allocation
>   account must be the same account type, either posting or unit accounts.
>   Also, an allocation account can’t be assigned as a distribution account for
>   another allocation account.

>   **To set up a fixed allocation account:**

1.  Open the Fixed Allocation Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Fixed Allocation)

![](media/e6c8257b40dc4469ebc56fb0952ebc66.jpg)

1.  Enter an account identifier using any combination of letters or numbers. You
    also can enter a description and an alias. Refer to *Understanding account
    aliases* for more information.

>   If you’ve set up account segments already and you leave the description
>   field blank. The account description will be created automatically by
>   combining the account segment descriptions.

>   To make changes to an existing fixed allocation account, enter or select the
>   account.

1.  If a transaction origin in the Posting Setup window is set up to use account
    settings, select how much detail to post to this account from each series.

    -   Select Detail to post a separate distribution amount to this account for
        each transaction in a batch.

    -   Select Summary to post a summarized total for an entire group of
        transactions to this account.

2.  Select the series where you expect to use this allocation account. The
    account will appear in all lookup windows in the selected series.

3.  Enter or select distribution accounts and percentages.

>   You can save a fixed allocation account even if the percentages for
>   distribution don’t equal 100%. However, you won’t be able to post
>   transactions to the account until they do.

1.  Save the account. Redisplay the account and choose File \>\> Print or the
    printer icon button to verify your entries with a Fixed Allocation Accounts
    List.

#### Deleting or inactivating a fixed allocation account

Use the Fixed Allocation Maintenance window to delete or inactivate a fixed
allocation account. Allocation accounts often are set up to accommodate a
specific situation, such as a sales promotion where a specified amount of cash
is distributed among locations, then broken down by department. Once the sales
promotion is over, the account might no longer be of value and can be deleted
from the chart of accounts.

In other situations, you might want to inactivate an account, rather than delete
it from the chart of accounts. Inactivating an account prevents posting to the
account, but keeps information about the account.

Fixed allocation accounts can be deleted at any time, unless the account is used
on any unposted transactions. When you delete a fixed allocation account, you’ll
also delete associated records for distributions. The posting or unit accounts
you’ve assigned as distributions and posted transactions that used the fixed
allocation account won’t be affected.

The Fixed Allocation Accounts List displays all the fixed allocation accounts
you’ve created, including distribution accounts. You should print this list
periodically to ensure that your chart of accounts accurately reflects the
current needs of your business. For more information on printing lists and
reports, see *Chapter 31, “General Ledger reports.”*

**To delete or inactivate a fixed allocation account:**

1.  Open the Fixed Allocation Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Fixed Allocation)

1.  Enter or select the allocation account you want to delete or inactivate.

2.  Choose Delete to delete the account or mark the Inactive option to
    inactivate the account.

3.  Choose Save to save the changes.

4.  Choose File \>\> Print or the printer icon button to print a Fixed
    Allocation

>   Accounts List to review the changes you’ve made to the chart of accounts.

**Chapter 6: Variable allocation accounts**

>   Variable allocation accounts are used to distribute percentages of a single
>   transaction to several different accounts, much like fixed allocation
>   accounts. You might use variable allocation accounts instead of fixed
>   allocation accounts when you need to break down expenses precisely. For
>   example, you could set up an account, Insurance Expense, and distribute the
>   expense among the distribution accounts set up for each department. The
>   expense could be further broken down by the number of employees in each
>   department, if you set up unit accounts that track each department’s head
>   count.

>   This information is divided into the following sections:

-   *Understanding variable allocation accounts*

-   *Setting up a variable allocation account*

-   *Deleting or inactivating a variable allocation account*

#### Understanding variable allocation accounts

>   Although variable allocation accounts are similar to fixed allocation
>   accounts, variable allocation accounts don’t use fixed percentages to
>   calculate amounts that will be posted to the distribution accounts.

>   Instead, you can use variable allocation accounts to distribute transactions
>   based on additional factors that might change over time, such as the number
>   of employees or the physical size of the departments in your business. These
>   additional factors are tracked by breakdown accounts. Breakdown accounts can
>   be posting accounts, like sales and expenses, or they can be unit accounts,
>   like the number of employees per department.

>   When transactions are posted to a variable allocation account, the total is
>   divided among its distribution accounts, based on the percentages determined
>   by the breakdown accounts. You don’t need to enter these percentages,
>   because they are calculated based on the varying balance of each breakdown
>   account. Each time you post to a variable allocation account, the
>   percentages might vary because the balances of the breakdown accounts might
>   have changed.

>   For example, assume you need to distribute the rent expense for a building
>   between several departments and use unit accounts to track the square
>   footage used by each department. You can set up a variable allocation
>   account and use the rent expense for each department as the distribution
>   accounts and the square footage unit accounts for the breakdown accounts.
>   When you post an amount to the variable allocation account, the balances of
>   the unit accounts are used to determine the rent expense amount to post to
>   each department.

>   Variable allocation accounts don’t appear on financial statements because
>   they don’t have balances. The amounts posted to variable allocation accounts
>   are reflected in the balances of the distribution accounts. The distribution
>   accounts appear on financial statements if they’re posting accounts.

#### Setting up a variable allocation account

>   Use the Variable Allocation Maintenance window to set up a variable
>   allocation account.

Distribution and breakdown accounts can be posting accounts or unit accounts.
All distribution accounts assigned to a single allocation account must be the
same account type. All breakdown accounts assigned to all distribution accounts,
for that variable allocation account, also must be the same account type.
However, your breakdown accounts don’t have to be the same account type as your
distribution accounts. For example, you can enter posting accounts for the
distribution accounts and unit accounts for the breakdown accounts. Other
allocation accounts can’t be used as distribution or breakdown accounts.

>   **To set up a variable allocation account:**

1.  Open the Variable Allocation Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Variable Allocation)

![](media/da43a9938115e9d6b0f3e7556627d56f.jpg)

1.  Enter an account identifier using any combination of letters or numbers. You
    also can enter a description and an alias. Refer to *Understanding account
    aliases* for more information. If you’ve set up account segments already and
    you leave the description field blank, Microsoft Dynamics GP will create the
    account description automatically by combining the account segment
    descriptions.

>   To make changes to an existing variable allocation account, enter or select
>   the account.

1.  Indicate whether you want to calculate the percentages based on the year-to
    date balance or on the transaction period balance of each breakdown account.

>   The transaction period balance is the net amount posted to the breakdown
>   account in a period. The user date determines which period is used.

1.  If the transaction origin in the Posting Setup window is set up to use
    account settings, select how much detail to post to General Ledger from each
    series.

    -   Select Detail to post a separate distribution amount to this account for
        each transaction in a batch.

    -   Select Summary to post a summarized total for an entire group of
        transactions to this account.

2.  Select the series where you expect to use this allocation account; the
    account will appear in all lookup windows in the selected series.

3.  Enter or select distribution accounts.

4.  Enter or select breakdown accounts for each distribution account. The
    balances of the breakdown accounts determine the percentage that will be
    posted to each distribution account.

5.  Choose Save to save the account. Redisplay the account and choose File \>\>
    Print or the printer icon button to verify your entries with a Variable
    Allocation Accounts List.

#### Deleting or inactivating a variable allocation account

>   Use the Variable Allocation Maintenance window to delete or inactivate a
>   variable allocation account.

>   Variable allocation accounts can be deleted at any time unless the account
>   is used on any unposted transactions. When you delete a variable allocation
>   account, you also delete associated records for breakdowns and
>   distributions. The posting or unit accounts you’ve assigned as distributions
>   and breakdowns and posted transactions that used the variable allocation
>   account won’t be affected.

>   The Variable Allocation Accounts List contains all the variable allocation
>   accounts you’ve created, including breakdown and distribution accounts. You
>   should print this list periodically to ensure that your chart of accounts
>   accurately reflects the current needs of your business.

>   **To delete or inactivate a variable allocation account:**

1.  Open the Variable Allocation Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Variable Allocation)

1.  Enter or select the account to delete or inactivate.

2.  Choose Delete to delete the account or mark the Inactive option to
    inactivate the account.

3.  Print a Variable Allocation Accounts List to review the changes you’ve made
    to the chart of accounts.

4.  Choose Save to save the changes.

**Chapter 7: Retained earnings accounts**

>   Retained earnings accounts are used for transferring the balances of
>   current-year profit and loss accounts during the year-end closing process.
>   The profit and loss accounts can be closed to two types of retained earnings
>   accounts: a single retained earnings account or divisional retained earnings
>   account. A net income or net loss amount is transferred to the retained
>   earnings account that you choose in the General Ledger Setup window.

>   This information is divided into the following sections:

-   *Understanding single retained earnings accounts*

-   *Setting up a single retained earnings account*

-   *Understanding divisional retained earnings accounts*

-   *Setting up divisional retained earnings accounts*

#### Understanding single retained earnings accounts

>   A single retained earnings account can be a posting account or a fixed
>   allocation account. In a single retained earnings account, the net income or
>   net loss amount is closed to a single posting account.

>   You can distribute the retained earnings to a fixed allocation retained
>   earnings account. You can use a fixed allocation account to post amounts to
>   distribution accounts based on the fixed percentage that you defined when
>   you set up the fixed allocation account.

#### Setting up a single retained earnings account

>   Use the General Ledger Setup window to set up a retained earnings account.
>   If you decide to close the profit and loss accounts to one retained earnings
>   account, the net income or net loss amount are closed to a single posting
>   account or fixed allocation account.

*Select your retained earnings account before posting your beginning balances.*

>   **To set up a single retained earnings account:**

1. Open the General Ledger Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> General Ledger)

![](media/c677af1b6541a096eb006362eec181d1.jpg)

1.  Enter or select a posting account or fixed allocation account to use as your
    retained earnings account.

2.  Save the account.

#### Understanding divisional retained earnings accounts

You can close your profit and loss accounts to divisional retained earnings
accounts. If you use divisional retained earnings accounts, you can close the
profit and loss accounts for each division to the retained earnings accounts
that corresponds to the department. Divisional retained earnings accounts also
can be fixed allocation accounts.

Account segments are used to determine how the retained earnings will be divided
when using a divisional retained earnings account. You can use divisional
retained earnings accounts if the following conditions apply:

-   Your company uses an account segment to represent individual departments
    within your company.

-   A retained earnings account is set up for each department.

-   The account number used for retained earnings for each department is
    identical, except for the account segment used to represent departments.

For example, a company has three departments and three segments in the account
format. The first account segment represents the department, the second segment
is the account number and the third segment is a sub-account. A retained
earnings account must be set up for each department as follows:

| **Department** | **Retained earnings account** |
|----------------|-------------------------------|
| Administration | 100-3100-00                   |
| Sales          | 200-3100-00                   |
| Training       | 300-3100-00                   |

If a retained earnings account was not set up for the training department, you
won’t be able to complete a year end close for the company.

#### Setting up divisional retained earnings accounts

Use the Account Maintenance window to set up a divisional retained earnings
account.

>   **To set up divisional retained earnings accounts:**

1.  Open the Account Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Account)

1.  Set up a separate retained earnings account for each division. Each account
    must be identical, except for the segment your division will be based on.

>   *You must set up a retained earnings account for each division in the
>   company, otherwise the year-end close will not take place.*

1.  Save your changes in the Account Maintenance window.

2.  Open the General Ledger Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> General Ledger)

1.  Mark Close to Divisional Account Segments and enter or select the account
    segment you’ll use as the divisional segment. For example, you might enter
    the first segment, Department.

2.  Enter or select one of the retained earnings accounts set up earlier. This
    account will be used as a template to find the retained earnings accounts
    for the remaining divisions.

 Chapter 8: Chart of accounts
-----------------------------

>   A chart of accounts is a list of all accounts in General Ledger. You can
>   modify an existing chart of accounts or define segments to identify specific
>   business units.

>   This information is divided into the following sections:

-   *Setting up an account segment definition*

-   *Chart of accounts modifications*

-   *Modifying ranges of accounts*

### Setting up an account segment definition

>   Use the Account Segment Setup window to enter or change account segment
>   definitions for each account segment number.

>   **To set up an account segment definition:**

1.  Open the Account Segment Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> Segment)

![](media/a1e446c1babf1942a455107081983e6f.jpg)

1.  Enter or select the segment ID to further identify.

2.  Enter or select a segment number. For example, if all the accounts for Store
    1 begin with 100, enter 100.

3.  Enter the description for the segment. For example, if you selected segment
    number 100 and that segment number is for accounts at the North Store, you’d
    enter North Store.

4.  Choose Save.

5.  Repeat steps 2 through 5 for each account segment definition.

6.  Choose File \>\> Print or the printer icon button to print the Account
    Segment List.

### Chart of accounts modifications

>   You can use General Ledger to change or copy ranges of accounts in your
>   chart of accounts. For example, you can copy a range of accounts created for
>   one department for use in another department. You can use the Mass Modify
>   Chart of Accounts window to copy, move, inactivate, delete, and update
>   accounts in a chart of accounts. To modify the chart of accounts, see
>   *Modifying ranges of accounts*.

>   **Copy** Use this method to duplicate a range of accounts. For example, if
>   the first segment of an account number identifies the department and you’ve
>   created a range of accounts with 100 as the first segment number, you could
>   copy all those accounts and assign a new first segment number 200. This
>   copies the account, typical balance, account type, series, and
>   active/inactive information. Account descriptions for the copied accounts
>   will be formed by combining the descriptions of the account segments. Spaces
>   will be left in the account description for any segments that have a blank
>   description. Actual account balances aren’t copied.

>   **Move** Use this method to move accounts within your company. You might
>   want to do this if a different department is now performing tasks associated
>   with a range of accounts. Account descriptions for the new accounts will be
>   formed by combining the descriptions of the account segments. Spaces will be
>   left in the account description for any segments that have a blank
>   description.

>   You can move accounts only if they meet the following conditions:

-   No balance

-   No activity for an open period

-   No account history amounts

-   Not part of an allocation or unposted transaction

-   Not part of an unposted transaction

-   No multicurrency data

-   No transaction history records

>   **Inactivate** Use this method to inactivate a range of active accounts with
>   zero balances or to inactivate all accounts in the range. For example, if
>   your company purchased a building and needed to inactivate all the rent
>   expense accounts you’ve used previously, you could inactivate the range of
>   accounts at once, rather than doing them one at a time.

>   **Delete** Use this method to delete a range of accounts from the chart of
>   accounts. All account information will be removed. For example, you might
>   delete a range of accounts if you’re closing out a product line and no
>   longer need the accounts or information associated with it. Deleting
>   accounts permanently removes them from the chart of accounts.

>   You can delete accounts only if they meet the following conditions:

-   No balance

-   No activity for an open period

-   No account history amounts

-   Not part of an allocation or unposted transaction

-   Not part of an unposted transaction

-   No multicurrency data

-   No transaction history records

>   **Update** Use this method to update the level of posting for a range of
>   accounts from the chart of accounts. For example, you might want to change
>   the level of posting from summary to detail so that you can track additional
>   information for that range of accounts.

### Modifying ranges of accounts

>   Use the Mass Modify Chart of Accounts window to copy, move, delete,
>   inactivate, or update ranges of accounts that you’ve already entered in your
>   chart of accounts.

>   All four account types—posting, unit, fixed allocation, and variable
>   allocation—are included in the chart of accounts and can be modified using
>   this window.

>   *The changes made in this window permanently affect the chart of accounts,
>   so you might want to experiment with the sample company before modifying
>   your accounting data. Back up your company’s data directory before making
>   changes to your company’s accounts, so you can restore the chart of accounts
>   and related information if necessary. For more information about making
>   backups, see the System Administrator’s Guide (Help \>\> Contents \>\>
>   select System Administration).*

>   **To modify a range of accounts:**

1.  Open the Mass Modify Chart of Accounts window.

>   (Financial \>\> Cards \>\> Financial \>\> Mass Modify)

![](media/43484c4a8f8d5df52a0b5e9d3a09a99f.jpg)

1.  Choose a Modify option. Refer to *Chart of accounts modifications* for more
    information.

2.  Select a range of accounts.

3.  If you’re updating accounts, select the level of posting for each series.

    -   Select Detail to post a separate distribution to each account in the
        range for each transaction in a batch.

    -   Select Summary to post a summarized total for an entire group of
        transactions to each account in the range.

4.  If you’re copying or moving accounts, enter an account mask.

>   For example, suppose you have a range of accounts set up for an existing
>   department, and you want to create a similar set of accounts for a new
>   department. If the first segment is used to identify departments, and the
>   existing department is identified by 100, you could enter 200 in the first
>   segment of the new account mask. The range of accounts you selected would be
>   copied but 200 would be substituted for the first segment.

1.  Choose Modify.

>   If you’ve selected to display all the accounts, your entire chart of
>   accounts appears, and you can scroll through the account list to find your
>   changes.

>   You also can display the modified range only by marking Selected Range. Only
>   the modified accounts will appear in the scrolling window.

Chapter 9: Beginning balances and history
-----------------------------------------

>   Unless your business is new, you must enter existing accounting data if you
>   want it to be available for comparative analysis. You can enter beginning
>   balances for a new fiscal year or in the middle of a fiscal year. You also
>   can enter account history.

>   This information is divided into the following sections:

-   *Understanding beginning balances and history*

-   *Entering beginning balances for a new fiscal year*

-   *Entering beginning balances in the middle of a fiscal year*

-   *Entering account history*

### Understanding beginning balances and history

>   You can keep unlimited years of account and transaction history in General
>   Ledger. If you choose to keep history in General Ledger, you can print
>   historical information on financial statements and compare historical-year
>   amounts to open-year amounts. You also can calculate budgets based on
>   information from a historical year.

>   When you’re setting up General Ledger for the first time, you can enter
>   three types of information:

>   **Beginning balances** The beginning balances for all posting accounts and
>   unit accounts in your chart of accounts.

>   **Account history** A record of account summary balances for previous
>   periods.

>   **Transaction history** A detailed record of all transactions that have been
>   posted to each account.

### Entering beginning balances for a new fiscal year

>   Use the Batch Entry window and the Transaction Entry window to enter
>   beginning balances and history at the beginning of a fiscal year. The
>   balance brought forward into the fiscal year serves as the beginning balance
>   for the accounts.

>   Be sure to mark the appropriate options in the General Ledger Setup window
>   for maintaining account and transaction history if you plan to keep either
>   type of historical information. You also must mark Allow Posting to History.
>   For more information about setup options, see *Setting up default entries
>   and preferences*.

>   *Be sure that you’ve set up the previous year in the Fiscal Periods Setup
>   window*

>   *(Administration \>\> Setup \>\> Company \>\> Fiscal Periods) and marked it
>   as a history year.*

>   **To enter beginning balances for a new fiscal year:**

1.  Open the Batch Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Batches)

![](media/f2bcd17f9cef386fe894a14ac15a74ba.jpg)

1.  Enter a batch ID—such as BBAL, for beginning balances—and select General
    Entry as the origin.

2.  Enter a batch comment, such as “Beginning balance for FY02.”

3.  Select Single Use as the frequency because you’ll post beginning balances
    and historical information only once.

>   *You can enter batch control totals in the Batch Entry window to verify the
>   number of beginning balance transactions entered or the total amount of the
>   batch. For more information on batch controls, refer to the System User’s
>   Guide (Help \>\> Contents \>\> Using the system)*.

1.  Choose Transactions to open the Transaction Entry window, where you can
    enter beginning balance transactions.

![](media/0f4580487787a08753d391102fd8d9d3.jpg)

1.  Enter a journal entry number and select Standard as the transaction type.

2.  Enter a transaction date that falls within the historical year.

>   With General Ledger you can post to the most recent historical year. The
>   transaction date determines which period in the historical year the
>   transaction will be posted to. When the transaction is posted, the amounts
>   will also be brought forward to the open fiscal year to adjust the beginning
>   balance for each account.

1.  Enter or select a source document ID and reference.

2.  Enter beginning balances and historical information.

>   Refer to the table for more information about the information you must
>   enter, depending on the amount of history you’re keeping.

| **If you plan to keep:**                                                       | **Enter:**                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Account and transaction history (Detailed transaction history for each period) | Enter the historical year’s first period balance for each account in the debit or credit column, depending on the account’s typical balance using the first day of the historical year as the date. Enter each transaction from the historical year as a separate entry using the exact date of the transaction in the historical year. Choose Save after each transaction entry. |
| Account history only (Account summary balances for each period)                | Enter the historical year’s first period balance for each account in the debit or credit column, depending on the account’s typical balance. Enter a summary transaction for each period of the historical year for each account you want summary account information posted to using the last day of the period as the date.                                                     |
| Beginning balances only                                                        | Enter the beginning balances for each balance sheet account in the debit or credit column, depending on the account’s typical balance, using the last day of the historical year as the date. Each balance sheet account should be listed as one line in the scrolling window of the Transaction Entry window.                                                                    |

>   As transactions used to enter historical information are posted to the most
>   recent historical year, beginning balances for each account will be
>   calculated automatically.

>   *If you enter a debit and credit amount on the same line, the debit entry
>   will be deleted automatically when you move to the following line.*

1.  Choose File \>\> Print or the printer icon button to verify your entries
    with a General Transaction Edit List before posting.

2.  Choose the Batch ID expansion button to open the Batch Entry window.

3.  Choose Post.

>   Audit trail codes are automatically assigned to these transactions as
>   they’re posted. You can use audit trail codes to trace the posting sequence
>   of a transaction back to its origin. The audit trail code for transactions
>   posted to history will have the prefix GLTHS and transactions posted to the
>   current year will have the prefix GLTRX.

### Entering beginning balances in the middle of a fiscal year

>   Use the Batch Entry window and the Transaction Entry window if you’re
>   entering beginning balances and history during an on-going fiscal year. You
>   must enter both historical information and current information.

>   Be sure to mark the appropriate options in the General Ledger Setup window
>   for maintaining account and transaction history if you plan to keep either
>   type of historical information. You also must mark Allow Posting to History.

>   *Be sure that you’ve set up the prior year in the Fiscal Periods Setup
>   window*

>   *(Administration \>\> Setup \>\> Company \>\> Fiscal Periods) and marked it
>   as a historical year.*

>   **To enter beginning balances in the middle of a fiscal year:**

1.  Open the Batch Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Batches)

1.  Enter a batch ID—such as BBAL—for beginning balances.

2.  Select General Entry as the origin.

3.  Enter a batch comment, such as “Beginning balance for FY08.”

4.  Select Single Use as the frequency because you’ll post beginning balances
    and historical information once only.

>   *You can enter batch control totals in the Batch Entry window to verify the
>   number of beginning balance transactions entered or the total currency
>   amount of the batch. For more information on batch controls, refer to the
>   System User’s Guide (Help \>\> Contents \>\> Using the system)*.

1.  Choose Transactions to open the Transaction Entry window, where you will
    enter beginning balance transactions.

2.  Enter a journal entry number.

3.  Select Standard as the transaction type since you’re entering standard
    transactions to record your beginning balances.

4.  Enter a transaction date that falls within the historical year. The
    transaction date determines which period in the historical year the
    transaction will be posted to. When the transaction is posted, the amounts
    will also be brought forward to the open fiscal year to adjust the beginning
    balance for each account.

5.  Enter or select a source document ID and reference.

6.  Enter beginning balances and historical information and save the
    transactions.

>   Refer to the following table for more information about the information you
>   must enter, depending on the amount of history you’re keeping.

| **If you plan to keep:**                                                       | **Enter:**                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Account and transaction history (Detailed transaction history for each period) | Enter the historical year’s first period balance for each account in the debit or credit column, depending on the account’s typical balance using the first day of the historical year as the date. Enter each transaction from the historical year as a separate entry using the exact date of the transaction in the historical year. Choose Save after each transaction entry. |
| Account history only (Account summary balances for each period)                | Enter the historical year’s first period balance for each account in the debit or credit column, depending on the account’s typical balance. Enter a summary transaction for each period of the historical year for each account you want summary account information posted to using the last day of the period as the date.                                                     |
| **If you plan to keep:**                                                       | **Enter:**                                                                                                                                                                                                                                                                                                                                                                        |
| Beginning balances only                                                        | Enter the beginning balances for each balance sheet account in the debit or credit column, depending on the account’s typical balance, using the last day of the historical year as the date.                                                                                                                                                                                     |

>   Each balance sheet account should be listed as one line in the scrolling
>   window of the Transaction Entry window.

>   As transactions used to enter historical information are posted to the most
>   recent historical year, beginning balances for each account will be
>   calculated automatically.

>   *If you enter a debit and credit on the same line, the debit entry will be
>   deleted automatically when you move to the following line.*

1.  Choose Save to save the transaction.

2.  Enter another journal entry number, select Standard as the transaction type
    and enter a transaction date to begin entering accounts and amounts for
    current year activity.

    -   If you plan to keep account and transaction history, enter each
        transaction from the current year as a separate transaction, using the
        exact date of the transaction.

    -   If you plan to keep only account history, enter a summary transaction
        for the activity in each previous period in the current year, using the
        last day of the period as the transaction date.

3.  Choose File \>\> Print or the printer icon button to verify your entries
    with a General Transaction Edit List.

4.  Choose the Batch ID expansion button to open the Batch Entry window. Choose
    Post. The posted amounts for the historical year are brought forward to the
    open year as each account’s beginning balance, and the correct historical
    information will be added.

>   Audit trail codes automatically will be assigned to these transactions as
>   they’re posted. Audit trail codes enable you to trace the posting sequence
>   of a given transaction back to the point it was originally entered in
>   Microsoft Dynamics

>   GP. The audit trail code for transactions posted to history will have the
>   prefix GLTHS and transactions posted to the current year will have the
>   prefix GLTRX.

### Entering account history

>   Use the Account History window to enter summary amounts for each account.

>   Even if you have historical information for each account for several
>   historical years, you can only post information to the most recent
>   historical year. To enter history for earlier years, you must enter summary
>   account information in this window. You also can use the Account History
>   window to change or delete existing account history information for posting
>   and unit accounts.

>   *Before entering account history for a particular year, you must set up the
>   year and mark it as a historical year in the Fiscal Periods Setup window.
>   For more information about fiscal period setup, refer to the System Setup
>   instructions (Help \>\> Contents \>\> select Setting Up the System).*

>   **To enter account history:**

1.  Open the Account History window.

>   (Financial \>\> Cards \>\> Financial \>\> Account History)

![](media/adee4e46eb9f606d343eb2aae96fd908.jpg)

1.  Enter or select an account.

2.  Select the year for which you want to enter or update historical
    information.

3.  Enter the net change, either debit or credit, for each period in the
    selected year. The net change and period balance fields will be updated
    automatically.

4.  If you’re using Multicurrency Management, you can choose Currency to open
    the Multicurrency Account History window, where you can enter historical
    multicurrency information for this account.

>   If you aren’t using Multicurrency Management, skip to step 7.

>   You can add, modify, or delete balances for an account for the selected
>   period and currency. You also can use the window to calculate a functional
>   currency amount for transaction activity for the selected account in a
>   historical period by entering amounts and exchange rates in the originating
>   currency.

1.  Choose Save and close the Multicurrency Account History window when you’ve
    finished.

2.  Choose Save in the Account History window.

>   *If you enter account history balances in the Account History window, you
>   shouldn’t reconcile the historical year. The reconcile process would look
>   for detail transactions but would not find any. The summary balances would
>   then be set to zero.*

 Chapter 10: Quick journal transactions setup
---------------------------------------------

>   You can use quick journals to quickly enter journal entries that aren’t part
>   of a batch. This document defines quick journals and explains how to use
>   them.

>   This information is divided into the following sections:

-   *Understanding quick journal transactions*

-   *Setting up a quick journal*

-   *Deleting a quick journal*

### Understanding quick journal transactions

>   You can use the Quick Journal Setup window to set up a template for entering
>   many different types of transactions. Quick journals are most effective for
>   transaction entry when the accounts used in the transaction remain constant,
>   but the amounts vary. You can make entries more quickly than in the
>   Transaction Entry window because all the necessary accounts are already set
>   up in the quick journal and you’ll enter only the transaction amounts for
>   each account.

>   For example, your company might make monthly cash disbursements for rent,
>   utilities, telephone, and insurance expenses. In the Quick Journal Setup
>   window, you could set up a quick journal entry that includes all the
>   accounts required to enter these disbursements. Instead of having to reenter
>   the accounts every pay period in the Transaction Entry window, you enter
>   only the amounts for the selected accounts. For more information about using
>   quick journals, see *Chapter 20, “Quick journal transactions.”*

>   *If you’re using Multicurrency Management, you can enter quick journals only
>   in your company’s functional currency.*

### Setting up a quick journal

>   Use the Quick Journal Setup window to create a quick journal, to make
>   changes and add accounts to an existing journal or to delete a journal
>   altogether.

**To set up a quick journal:**

1.  Open the Quick Journal Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> Quick Journal)

![](media/a36576a0b5c315fc55fa327e3c7477c0.jpg)

1.  Enter or select a journal ID and enter a description.

2.  Enter or select a source document and enter a reference. For more
    information about setting up source documents, refer to the System Setup
    instructions (Help \>\> Contents \>\> select Setting Up the System).

3.  Enter or select the offset account. The entire offsetting portion of each
    transaction entered in this quick journal will be posted to this account.

>   Mark the Allow Override option to enable users to override the default
>   offset account when entering transactions. Don’t mark the option if you want
>   to use the default offset account every time you enter quick journal
>   transactions.

>   *Only posting accounts, fixed allocation accounts, or variable allocation
>   accounts can be offset accounts. Unit accounts can’t be entered as the
>   offsetting account in a quick journal entry since they track nonfinancial
>   quantities.*

1.  To have breakdown allocations printed on the Quick Journal Edit List and
    Quick Journal Posting Journal, mark the Break Down Allocation option.

2.  Enter or select the accounts to which transactions entered in this quick
    journal will be posted.

3.  Choose Save.

4.  Choose File \>\> Print or the printer icon button while the Quick Journal
    Setup window is displayed to review the options you’ve selected with the
    Quick Journal Setup List.

### Deleting a quick journal

Use the Quick Journal Setup window to delete quick journals. When you delete a
quick journal, any unposted quick journal transactions using this quick journal
also will be deleted. An alert message will appear if there are unposted quick
journal transactions.

>   **To delete a quick journal:**

1.  Open the Quick Journal Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> Quick Journal)

1.  Enter or select the journal ID.

2.  Choose Delete.

 Chapter 11: Revenue/Expense Deferrals setup
--------------------------------------------

>   Before you begin using Revenue/Expense Deferrals, you need to set the
>   options you want to use for creating deferral transactions, such as the
>   posting method used, and user access options.

>   This information includes the following sections:

-   *Revenue/Expense Deferrals overview*

-   *Deferral posting methods*

-   *Balance Sheet posting example*

-   *Profit and Loss posting example*

-   *Setting up revenue/expense deferrals*

-   *Selecting deferral warning options*

-   *Setting up a deferral profile*

-   *Setting access to a deferral profile*

### Revenue/Expense Deferrals overview

>   Revenue/Expense Deferrals simplifies deferring revenues or distributing
>   expenses over a specified period. Revenue or expense entries can be made to
>   future periods automatically from General Ledger, Receivables Management,
>   Payables Management, Sales Order Processing, Purchase Order Processing, and
>   Invoicing.

>   If you use deferral transactions frequently, you can set up deferral
>   profiles, which are templates of commonly deferred transactions. Using
>   deferral profiles helps ensure that similar transactions are entered with
>   the correct information. For example, if you routinely enter transactions
>   for service contracts your company offers, and the revenue is recognized
>   over a 12-month period, you could set up a deferral profile for these
>   service contracts, specifying the accounts to be used, and the method for
>   calculating how the deferred revenue is recognized.

### Deferral posting methods

>   You can use two methods for posting the initial transactions and the
>   deferral transactions: the Balance Sheet method, and the Profit and Loss
>   method.

>   **Balance Sheet** Using the Balance Sheet method, you’ll identify two
>   posting accounts: a Balance Sheet deferral account to be used with the
>   initial transaction for the deferred revenue or expense, and a Profit and
>   Loss recognition account to be used with each period’s deferral transaction
>   that recognizes the expense or revenue. For an illustration of this method,
>   see *Balance Sheet posting example*.

>   **Profit and Loss** Using the Profit and Loss method, you can identify up to
>   five accounts, which allows greater detail in financial reporting than the
>   Balance Sheet method. These accounts are three Profit and Loss accounts, and
>   two Balance Sheet accounts.

>   Profit and Loss accounts:

-   An account for the initial posting of the full amount of the original
    revenue or expense

-   An account used for reversing the deferred revenue or expense (this can be
    the same as the original account)

-   An account used for recognizing the deferred revenue or expense (again, this
    can be the same as the original account)

>   Balance Sheet accounts:

-   A deferrals account to record the full deferred balance (transferred from
    the original revenue or expense account)

-   A deferrals transfers account (this can be the same as the deferrals
    account)

>   For an illustration of this method, see *Profit and Loss posting example*.

>   *Once you have selected a deferral posting method for a series and posted
>   deferral transactions, we recommend that you not change the deferral posting
>   method.*

### Balance Sheet posting example

>   Assume you have a transaction for \$12,000 of revenue, to be deferred over
>   one year, from January to December. When you defer this transaction using
>   the Balance Sheet posting method, the full sales amount is posted to the
>   deferrals account, rather than the sales account that would be used for
>   non-deferred revenue. The initial transaction is posted as follows:

| **Account**       | **Debit** | **Credit** |
|-------------------|-----------|------------|
| Cash              | \$12,000  |            |
| Deferrals Account |           | \$12,000   |

>   The deferral transactions for each month created for this deferred revenue
>   would appear as follows:

| **Account**               | **Debit** | **Credit** |
|---------------------------|-----------|------------|
| Deferrals Account         | \$1,000   |            |
| Sales Recognition Account |           | \$1,000    |

>   The full revenue amount of \$12,000 will be posted to the Profit and Loss
>   sales recognition account in \$1,000 increments each month for a year, and
>   the Balance Sheet deferrals account is reduced by the same amount.

### Profit and Loss posting example

>   Assume you have a transaction for \$12,000 of revenue, to be deferred over
>   one year, from January to December. Three Profit and Loss accounts, and two
>   Balance Sheet accounts are being used for the deferral. The full sales
>   amount is posted to the usual sales account, as follows:

| **Account**            | **Debit** | **Credit** |
|------------------------|-----------|------------|
| Cash                   | \$12,000  |            |
| Original Sales Account |           | \$12,000   |

>   However, when you defer this transaction using the Profit and Loss posting
>   method, a second entry is also created that reverses the Sales account entry
>   and transfers the full balance to the deferrals account.

| **Account**            | **Debit** | **Credit** |
|------------------------|-----------|------------|
| Deferred Sales Account | \$12,000  |            |
| Deferrals Account      |           | \$12,000   |

>   The deferral transactions for each month created for this deferred revenue
>   would appear as follows:

| **Account**                | **Debit** | **Credit** |
|----------------------------|-----------|------------|
| Deferrals Transfer Account | \$1,000   |            |
| Sales Recognition Account  |           | \$1,000    |

>   The balances for the Profit and Loss accounts at the end of the deferral
>   period will appear as follows:

| **Account**               | **Debit** | **Credit** |
|---------------------------|-----------|------------|
| Original Sales Account    |           | \$12,000   |
| Deferred Sales Account    | \$12,000  |            |
| Sales Recognition Account |           | \$12,000   |

>   The balances for the Balance Sheet accounts at the end of the deferral
>   period will appear as follows:

| **Account**                | **Debit** | **Credit** |
|----------------------------|-----------|------------|
| Deferrals Account          |           | \$12,000   |
| Deferrals Transfer Account | \$12,000  |            |

>   The overall result will be a credit balance of \$12,000 for the Profit and
>   Loss sales accounts, and a \$0 balance for the Balance Sheet deferrals
>   accounts.

>   *You can use the same account for the original sales, deferred sales, and
>   sales recognition accounts, and for the deferrals and deferrals transfer
>   accounts. However, if you use a different account for each, you can identify
>   the amounts for reporting purposes.*

### Setting up revenue/expense deferrals

>   Use the Deferral Setup window to enter the options you want to use with
>   Revenue/ Expense Deferrals.

>   **To set up revenue/expense deferrals:**

1.  Open the Deferral Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> Deferral)

![](media/e6a68e7ed88b39ac144e9d6c53fa3f59.jpg)

1.  Enter the next batch number you want to use for deferral transactions, the
    source document code, and the next transaction number.

2.  Select the default method you want to use to calculate the allocations for
    deferral transaction amounts.

    -   The Days In Period method apportions the amount based on the number of
        days in a fiscal period.

    -   The Equal Per Period method allocates an equal amount per fiscal period.

    -   The Miscellaneous method allows you to specify the length of the periods
        and allocates an equal amount per period.

3.  Indicate whether you want to automatically post deferral transactions
    through General Ledger, and to closed future or previous fiscal periods.

4.  Indicate whether you want deferral transactions for the Sales and Purchasing
    series to use the Balance Sheet or Profit and Loss method for posting the
    initial and deferral transactions. For more information, see *Deferral
    posting methods*.

>   *Once you have selected a deferral posting method for a series and posted
>   deferral transactions, we recommend that you don’t change the deferral
>   posting method.*

1.  Specify whether you want to void the associated original transaction when
    any deferral transaction is voided.

2.  Indicate whether you want all users to have access to deferral profiles, or
    if you want to limit access based on user or user class. If you restrict
    access, you’ll specify the users or user classes that have access to a
    profile when you set up the profile. For more information, see *Setting up a
    deferral profile*.

3.  Select an option for overriding distribution accounts.

4.  Indicate whether you want the deferral posting reports to be printed and
    specify whether you want them sent to the printer, displayed on screen, or
    both.

5.  Choose Warning Options to set up options for warning users about assigning
    deferrals to specific distribution types. For more information, see
    *Selecting deferral warning options*.

6.  Choose OK to save your changes and close the window.

### Selecting deferral warning options

>   Use the Deferral Warning Options window to select the warning options you
>   want to use to help prevent users from attaching deferrals to incorrect
>   distribution types. For example, you could set up the warning options for
>   Sales Order Processing so if a user attempted to defer the CASH
>   distribution, a warning would appear.

>   *Selecting these options does not block a user from attaching a deferral
>   transaction to an incorrect distribution type. A message will appear in this
>   situation, but the user can post the transaction.*

>   **To select deferral warning options:**

1.  Open the Deferral Setup window.

>   (Financial \>\> Setup \>\> Financial \>\> Deferral)

1.  Choose Warning Options to open the Deferral Warning Options window.

![](media/48ee3f63c4dbd292076b115799341c8b.jpg)

1.  Select the module you want to select warning options for from the list.

2.  Mark the checkbox for the distribution types you want to avoid using for
    deferrals.

3.  Select another module and continue selecting warning options.

4.  Choose OK to save your entries and close the window.

### Setting up a deferral profile 

>   Use the Deferral Profile Maintenance window to set up templates of commonly
>   deferred transactions. Using deferral profiles helps ensure that similar
>   transactions are entered with the correct information. For example, if you
>   routinely enter transactions for service contracts your company offers, and
>   the revenue is recognized over a 12-month period, you could set up a
>   deferral profile for these service contracts, specifying the accounts to be
>   used, and the method for calculating how the deferred revenue is recognized.

>   You can set up profiles for transactions originating in General Ledger,
>   Receivables Management, Sales Order Processing, Payables Management, and
>   Purchase Order Processing.

>   **To set up a deferral profile:**

1.  Open the Deferral Profile Maintenance window.

>   (Financial \>\> Setup \>\> Financial \>\> Deferral Profiles)

![](media/b25481b18d390291af8e08f483ba9263.jpg)

1.  Enter a name for this profile. For example, you could create a profile
    called SERVICE CONTRACT.

2.  Select the modules the profile is to be used with from the list. For
    example, you might want to use a service contracts profile with Receivables
    Management and Sales Order Processing.

>   To select multiple modules, hold down the CTRL key while clicking the
>   modules.

1.  Select the types of distribution you want this profile used with. For
    example, you might select the SALES, MISC, and SERVICE distribution types.

>   To select multiple distributions, hold down the CTRL key while clicking the
>   distributions.

1.  Select the accounts you want to use to defer and recognize the revenues or
    expenses. Depending on the option you selected for overwriting distribution
    accounts in the Deferral Setup window, you may be able to mark the option to
    enable an account to be changed.

2.  Select the method to calculate the deferral amounts across each period, the
    date of the first allocation, and the number of fiscal periods to allocate
    the transaction over. If you leave the start date or number of periods
    blank, you’ll need to enter a start date and number of periods when you use
    the profile to defer a transaction distribution.

3.  If you chose to limit access to profiles to specific users or user classes
    in the Deferral Setup window, choose User Access to select the users or user
    classes who can use this profile. You can also select the information on a
    profile you want users to be able to change. For more information, see
    *Setting access to a deferral profile*.

4.  Choose Save to save this profile.

### Setting access to a deferral profile

>   Use the Profile User Access window to limit access to a profile to specific
>   users or user classes. You can also specify which information on a profile
>   you want users to be able to change. For example, you can enable some users
>   to change the start date and number of periods for a deferral transaction,
>   but not the deferral or recognition accounts, and you can enable other users
>   to change the deferral and recognition accounts.

>   **To set access to a deferral profile:**

1.  In the Deferral Profile Maintenance window, enter or select the profile you
    want to set access for, and choose User Access to open the Profile User
    Access window.

![](media/96113783d75a0c7e85629e6aa3a5cf09.jpg)

1.  Indicate whether you want to grant access to the profile to the users you
    specify, or to the user classes you specify.

2.  Enter or select the user or user class you want to have access to the
    profile and mark the option to enable access.

>   If you’re setting access for a user, you can also indicate whether this
>   profile is the default profile for this user. If you mark this option, this
>   profile will appear automatically when the user uses deferral profiles
>   during transaction entry.

1.  Mark the types of information you want the user or members of the user class
    to be able to edit during deferral transaction entry.

2.  Choose Save to save the access information for this user or user class.

3.  To set access to this profile for another user or user class, repeat steps 2
    through 5.

Part 2: Budgets
===============

>   You can create a budget in Microsoft Dynamics GP.

>   The following information is discussed:

-   *Chapter 12, “Budget overview,”* outlines the features in Microsoft Dynamics
    GP you can use to create and maintain budgets.

-   *Chapter 14, “Setting up budgets in Microsoft Dynamics GP,”* describes how
    to create a budget in Microsoft Dynamics GP using the Budget Maintenance
    window or the Single-Account Budget Maintenance window.

Chapter 12: Budget overview
---------------------------

>   You can use General Ledger to use the features of both Microsoft Dynamics GP
>   and Microsoft Excel to create and maintain budgets. You can create and
>   modify budgets, export them to Excel, or import them to Microsoft Dynamics
>   GP.

>   For example, you can start building your budget in Microsoft Dynamics GP
>   based on your account framework, then export the budget to Excel to add
>   formulas and explore forecasting scenarios. Finally, you can import the
>   budget into Microsoft Dynamics GP to be used in the accounting system.

>   This information is divided into the following sections:

-   *Viewing a list of existing budgets*

-   *Creating a new budget*

-   *Opening an existing budget*

-   *Deleting a budget*

### Viewing a list of existing budgets

>   You can use the Budget Selection window (Financial \>\> Cards \>\> Financial
>   \>\> Budgets) to view all budgets in the system, including budgets created
>   in Excel and imported into Microsoft Dynamics GP.

>   To change the order budgets are listed in the Budget Selection window, click
>   the arrow in the scrolling window title bar, then select to sort items by
>   Budget ID or by Description.

### Creating a new budget

>   Use the Budget Selection window to select whether to create new budgets in
>   Microsoft Dynamics GP or in Microsoft Excel.

>   **To create a new budget:**

1.  Open the Budget Selection window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets)

1.  Decide if the budget will be created in Microsoft Dynamics GP or in Excel.

-   To create a budget in Microsoft Dynamics GP, choose New and select using

>   Microsoft Dynamics GP to open the Budget Maintenance window. Refer to
>   *Chapter 14, “Setting up budgets in Microsoft Dynamics GP,”* for more
>   information.

-   To create a budget in Excel, choose New and select using Budget Wizard for
    Excel. Refer to *Chapter 13, “Setting up budgets in Microsoft Excel,”* for
    more information.

>   3. Choose New to open the Budget Maintenance window. Refer to *Chapter 14,
>   “Setting up budgets in Microsoft Dynamics GP,”* for more information.

>   *You’ll use a different method to set up a single-account budget in
>   Microsoft Dynamics GP. Refer to Creating a single-account budget for more
>   information.*

### Opening an existing budget

>   You can open existing budgets in either Microsoft Dynamics GP or Microsoft
>   Excel.

>   **To open an existing budget:**

1.  Open the Budget Selection window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets)

1.  Select a budget in the scrolling window.

    -   To open a budget with Excel, choose Open and select using Excel. The
        Microsoft Dynamics GP budget must have an Excel file associated with it.

    -   To open a budget with Microsoft Dynamics GP, choose Open and select
        using Microsoft Dynamics GP.

2.  Choose Open.

### Deleting a budget

>   You also can use the Budget Selection window to delete a budget. When you
>   delete a budget, accounts are removed from the specified budget ID and
>   you’ll then have an option to deleting the budget ID itself.

>   **To delete a budget:**

1.  Open the Budget Selection window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets)

1.  Highlight the budget in the scrolling window.

2.  Choose Delete. An alert message appears, asking if you’re sure you want to
    delete the budget. Choose Yes to delete the budget or choose No to cancel
    the process.

Chapter 13: Setting up budgets in Microsoft Excel
-------------------------------------------------

>   You can use pre-existing budgets you’ve created in Microsoft Excel, or you
>   can create new budgets in Microsoft Excel using the Budget Wizard for Excel.

>   The wizard helps you choose the framework for the budget, the calculation
>   method for amounts, and the account types and ranges to include in the
>   budget.

>   Later, you can import the budget into Microsoft Dynamics GP. For more
>   information about importing budgets from Microsoft Excel, see *Chapter 15,
>   “Exporting and importing budgets.”*

>   This information is divided into the following sections:

-   *Budget calculation methods*

-   *Account types for budgets*

-   *Creating a budget with the budget wizard*

-   *Format requirements for budgets in Microsoft Excel*

### Budget calculation methods

>   After you’ve identified the budget, you can choose a calculation method for
>   the budget. The Budget Calculation Method window includes four calculation
>   methods. Although each budget calculation method is different, the steps for
>   using the wizard will be roughly the same for each one.

>   **Open Year Percent** This budget method calculates budget amounts based on
>   a percentage of actual amounts in an open year. For example, you can build a
>   2006 budget by selecting an open year, such as 2004, and entering a
>   percentage by which to increase or decrease the amounts for the new budget.

>   **Other Budget Percent** This budget method calculates budget amounts based
>   on a percentage of amounts in another budget. To use this method, select an
>   existing budget, indicate whether the amounts will be increased or
>   decreased, and enter the percentage by which to increase or decrease the
>   amounts.

>   **Historical Year Percent** This budget method calculates budget amounts
>   based on actual account balances of a previous, historical year. The amounts
>   can be increased or decreased by a percentage you specify.

>   **Blank Budget** This budget method calculates no budget amounts but
>   provides you with a blank Microsoft Excel budget spreadsheet. You can choose
>   fiscal years from which to pull actual amounts.

### Account types for budgets

>   Three types of accounts are available for use in Microsoft Excel budgets:
>   balance sheet accounts, profit and loss accounts, and unit accounts.

>   **Balance sheet accounts** Balance sheet accounts are assets, liabilities,
>   and owner’s equity accounts. The amounts in these accounts would typically
>   appear on a company’s balance sheet.

>   **Profit and loss accounts** Profit and loss accounts are for revenues and
>   expenses. These accounts represent the cash and assets going into and out of
>   a company’s general ledger.

>   **Unit accounts** Unit accounts do not track dollar amounts but track other
>   amounts such as the number of employees. Unit accounts are used to
>   accurately distribute the revenue or expense from another account, set up to
>   cover all the employees, departments, or other units, in the unit account.

>   You can choose to include any or all of these account types. Depending on
>   the budget you want to create, you might not want to include all of the
>   information. For example, if you’re creating a budget to determine the total
>   value of a business, you’d want to include both balance sheet accounts and
>   profit and loss accounts. If you want to create a budget for a specific
>   department, you’ll probably include profit and loss accounts and unit
>   accounts, but not balance sheet accounts.

>   As you use the wizard, you’ll choose specific accounts to include in your
>   budget.

### Creating a budget with the budget wizard

>   You can use Microsoft Dynamics GP to create a new budget in Microsoft Excel.
>   The new budget will be a new worksheet that can be part of an existing
>   workbook, or a new workbook. You can add budget amounts in this worksheet
>   and import the budget into Microsoft Dynamics GP.

>   *This procedure uses the Open Year budget calculation method. Creating
>   budgets using other budget calculation methods is similar, but differences
>   are noted.*

>   **To create a budget with the budget wizard:**

1.  Open the Budget Selection window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets)

![](media/6814a53b87625f1ee211947dc4df5c4c.jpg)

1.  Choose New and select using Budget Wizard for Excel to open the welcome
    window.

2.  Choose Next to open the New Budget Information window.

![](media/3756a032c3996e477bc8b51687e00ba8.jpg)

1.  Enter basic identifying information about the budget you are creating.

2.  Select whether to base the budget on a fiscal year or a date range. If you
    base the budget on a date range, specify a range that crosses one or more
    fiscal years. See *Calculating budgets that overlap fiscal years* for more
    information.

3.  If you want to restrict access to the budget with a password, choose the
    padlock icon button to open the User Password Setup window. If you don’t
    want to restrict access to the budget, skip to step 7.

![](media/29d632a6cc68667049d73a61aa3f909f.jpg)

1.  Enter a password and choose OK.

2.  Choose Next to open the Budget Calculation Method window.

![](media/4fcd4380a5679d423093382a34d1aa1f.jpg)

1.  Highlight a budget calculation method to view its description. When you have
    selected the method you want to use, choose Next to open the Open Year
    Percent window.

![](media/288d9d6ee9f9a4b3515a07f09e6cd322.jpg)

>   The following steps assume you selected the Open Year Percent budget
>   calculation method. All of the steps are essentially the same for each
>   method, except Blank Budget. Differences are noted in the following steps.

>   If you selected a budget method other than Open Year Percent, the name of
>   the window will be different. If you’re using the Other Budget Percent
>   method, the Other Budget Percent window opens. If you’re using the
>   Historical Budget Percent method, the Historical Year Percent window opens.
>   Information in the windows will be the same, except you will select a
>   specific budget or a historical year instead of an open year. You won’t see
>   this window if you chose Blank Budget, but will instead go to the next
>   window, Actual Amounts Selection.

1.  Select the open year you want to use as the basis for your new budget. If
    you’re using another calculation method, choose an actual budget or
    historical year for the other calculation methods.

2.  Select the type of change to be made and enter a percentage of increase or
    decrease. Press TAB to exit this field and enable the Next button. Choose
    Next to open the Actual Amounts Selection window.

![](media/bebd995f74958b99d16866df9b51e1a1.jpg)

1.  Select the years with the amount information to use. A separate Microsoft
    Excel worksheet will be created for each year you select

>   *Worksheets will be in the same order you select them in the Actual Amounts
>   Selection window, so if you want them to appear in the workbook in a
>   specific order, be sure to select them in order.*

>   When you have made your selections, choose Next to open the Account Types
>   window.

![](media/e3a4de5fcba7e9833dc2497022b46eb9.jpg)

1.  Select the account types to include in your budget. Choose Next to open the
    Accounts window.

![](media/64145d8b286ca4549e4e37f8b8bab88d.jpg)

1.  Select the accounts for the budget. You can add all accounts of the account
    type you selected, or you can restrict the range of accounts.

>   Select a segment for sorting the accounts. Enter or select the starting and
>   ending segment numbers in the range, then choose Insert to add them to the
>   scrolling window.

>   Choose Next to open the Account Verification window.

![](media/4d630da438800d4f17c7476be3688554.jpg)

1.  Mark the accounts to include in the budget. All accounts will be marked, but
    you can clear the option for any account to exclude it from the budget.

>   To add an account that isn’t displayed, choose Add Account. The Accounts
>   Lookup window will open. Select the account to add.

>   Choose Next to open the Workbook Selection window.

![](media/657286ca47cb52c4709b67c8ab2bc55e.jpg)

1.  Select the workbook for your new budget worksheet. You can create a new
    workbook or add to an existing one. Choose Next to open the Completing the
    Budget Wizard for Excel window.

2.  Review your selections, then choose Finish to complete the budget. The
    wizard will build a new budget worksheet and fill the columns with budget
    amounts from the accounts you selected, adjusted by the percentage you
    specified.

### Format requirements for budgets in Microsoft Excel

>   When a worksheet is created using the budget wizard or when an existing
>   budget is exported to Microsoft Excel, the worksheet must have the following
>   standard layout:

-   Column A lists the accounts included in the budget, in view-only format.

-   Column B lists the descriptions for the accounts, in view-only format.

-   Column C lists the beginning balance budget amounts.

-   Columns D and columns beyond list the period budget amounts. The amounts and
    formulas in these columns can be changed**.**

-   The first column after all the period amounts will total all of the period
    budget amounts, in view-only format.

-   The last row will display the totals for each period column in view-only
    format.

-   The maximum number of fiscal periods (columns) you can use is 252, because
    the first four columns are required for the account information and balance
    amounts. (Excel allows a maximum of 256 columns in a spreadsheet.)

Chapter 14: Setting up budgets in Microsoft Dynamics GP
-------------------------------------------------------

>   You can maintain an unlimited number of budgets in Microsoft Dynamics GP and
>   calculate the budgets using one of several different calculation methods.
>   You can create budgets for ranges of posting and unit accounts, or for
>   single accounts. You also can change or delete existing budgets and
>   recalculate budget amounts.

>   This information is divided into the following sections:

-   *Budget calculation methods*

-   *Calculating budgets that overlap fiscal years*

-   *Creating a budget for a range of accounts*

-   *Deleting a budget*

-   *Creating a single-account budget*

-   *Entering budget transactions*

-   *Combining budgets in Microsoft Dynamics GP*

### Budget calculation methods

>   You can use one of seven calculation methods for budgets you create in
>   Microsoft Dynamics GP, and apply these methods to posting or unit accounts.
>   You also can choose whether your budget will include beginning balances.
>   Each method’s description includes information about the entries needed. The
>   same calculation methods are available whether you’re calculating a budget
>   for a fiscal year or for a range of dates; however, there are some
>   differences to be aware of. See *Calculating budgets that overlap fiscal
>   years* for more information.

>   **Open Year Percent** This budget method calculates budget amounts based on
>   the actual balances of any year that hasn’t been closed, increasing or
>   decreasing them by a specified percentage. Actual account balances won’t be
>   affected.

>   To use this method, you must select the year to base the calculations on.
>   Enter the percentage to increase or decrease the amounts or enter 0% to use
>   the existing account balances.

>   **Other Budget Percent** This budget method calculates budget amounts based
>   on another budget. You can copy amounts from another budget and then
>   increase or decrease them by a percentage you specify.

>   To use this method, you must enter the ID for the source budget and the
>   percentage to increase or decrease the amounts. You can enter 0% to use the
>   existing budget amounts.

>   **Percent Change** This budget method calculates budget amounts based on
>   amounts in a current budget. You can increase or decrease the amounts by a
>   percentage you specify.

>   For example, suppose your budget for an account includes \$100 for the
>   beginning balance and \$200 for each budget period. To decrease the budget
>   by 20 percent, you can choose Percent Change, enter the percentage and
>   indicate that you want the amounts decreased. The new budget amounts will
>   include a beginning balance of \$80 and period amounts of \$160.

>   **Amount Change** This budget method calculates budget amounts based on
>   amounts in a current budget. You can increase or decrease the amounts by a
>   dollar amount (for posting accounts) or quantity (for unit accounts) you
>   specify.

>   To use this budget calculation method, enter the specified amount and
>   indicate whether the current budget amounts should be increased or
>   decreased.

>   **Set Amount** This budget method calculates budget amounts based on a fixed
>   amount for each period included in the budget.

>   Enter the amount and indicate which periods you want to include. To include
>   beginning balance amounts in the budget calculation, mark the option to
>   include the beginning balances. If you mark this option, beginning balances
>   for all balance sheet accounts will be included.

>   **Yearly Budget Amount** This budget method calculates budget amounts and
>   divides them equally among all periods in the budget.

>   To use this method, enter the amount and specify the periods to be included
>   in the calculation. To include beginning balance amounts in the budget
>   calculation, mark the option to include the beginning balances. If you mark
>   this option, beginning balances for all balance sheet accounts will be
>   included.

>   **Historical Year Percent** This budget method calculates budget amounts
>   based on a historical year’s actual balances, which can be increased or
>   decreased by a percentage you specify. Actual account balances aren’t
>   affected. You can use this method only if you are keeping account history.

>   To use this method, choose a year and enter the percentage increase or
>   decrease.

>   Enter 0% if you want to use the existing account balances.

### Calculating budgets that overlap fiscal years

>   You can create budgets for a range of dates that don’t match your fiscal
>   year. This can be useful if your organization receives grants that span
>   multiple years, or that cover a period of time that’s different from your
>   fiscal year. Budgets based on a range of dates can be created for either a
>   single account or a range of accounts.

>   To base a budget on a range of dates, fiscal periods must be set up for the
>   full period that’s covered by the date range of the budget. For example, if
>   you create a budget for March 1, 2007 to August 31, 2009, you can’t save the
>   budget if you haven’t created fiscal periods through August 31, 2009.

>   After you’ve saved a budget, you can’t change the time period that it’s
>   based on, nor can you change the starting and ending dates when you’re
>   basing the budget on a date range.

>   The calculation methods that are available for budgets based on fiscal years
>   also are available for budgets based a date range. Some calculation methods
>   involve

>   copying budget amounts from one budget to another. The following table
>   describes how this process works when you’re basing a budget on a range of
>   dates.

| **Calculation method** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Open year percent      | These calculation methods copy amounts from an existing budget to the budget you’re setting up, and then calculate a specified increase or decrease. The first period of the existing budget is copied to the first period of the budget you’re setting up. The second period of the existing budget is copied to the second period of the new budget, and so on. If there are more periods in the budget you’re setting up than in the existing budget being copied from, the additional periods in the new budget will have a balance of \$0. |
| Yearly budget amount   | This calculation method allocates amounts evenly over all the budget periods. If you’re basing a budget on a date range, the number of periods might be more or less than the number of periods in your fiscal year. The yearly budget amount is allocated evenly among the periods in the date range regardless of the number of periods in your fiscal year.                                                                                                                                                                                  |

>   Other budget percent

>   Historical year percent

### Creating a budget for a range of accounts

>   Use the Budget Maintenance window to create a budget for a range of posting
>   and unit accounts. You can view how the calculation has affected the
>   accounts included in the range, one account at a time. You can display the
>   calculated amounts for each account if you want to view the budget
>   calculation for a single account.

>   **To create a budget for a range of accounts:**

1.  Open the Budget Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets \>\> New \>\> using
>   Microsoft Dynamics GP)

![](media/3a4009db3e073ac8ef0ec1cb65a869a3.jpg)

1.  Enter or select a budget ID.

*Use only alphanumeric characters in the budget ID.*

1.  Select whether to base the budget on a fiscal year or a date range. If you
    base the budget on a date range, specify a range that crosses one or more
    fiscal years. See *Calculating budgets that overlap fiscal years* for more
    information.

2.  Choose the budget type: actual or preliminary.

>   Choose Actual if you know that the budget will be calculated correctly and
>   that you will not be making changes to the budget.

>   Choose Preliminary to experiment with budgets. You can change preliminary
>   budgets and then revert to the original version of the budget, but when you
>   change an actual budget, the change is permanent.

>   *If you’re calculating a preliminary budget and you’ve decided that you’d
>   like to save it, make the changes permanent by choosing Actual and save the
>   budget.*

1.  To restrict access to the budget, choose the password padlock icon button to
    open the User Password Setup window. If you don’t need to restrict access to
    the budget, skip to step 6.

2.  Enter a password and choose OK.

3.  Choose a budget year. If you’ve selected an existing budget and you change
    budget years, some periods may not appear in the scrolling window.
    Recalculate the budget before continuing.

4.  Choose Ranges to open the Account Segment Ranges window.

>   *If you don’t define a range, all your company's accounts will be included
>   in the budget calculation.*

![](media/aabb7c3e9731455a82576722dbc56fd0.jpg)

1.  Enter or select the segment ID the range will be based on. Enter or select
    beginning and ending account segments.

2.  Choose Insert to insert the range into the Restrictions box. All accounts
    that meet all restrictions you’ve entered will be included in the budget.

>   *To calculate actual budgets for single accounts, you might find it easier
>   to use the Single-Account Budget Maintenance window. (Preliminary budgets
>   can’t be calculated using the Single-Account Budget Maintenance window.) For
>   more information, see Creating a single-account budget.*

1.  Choose OK to return to the Budget Maintenance window.

2.  Choose the Methods button to display the Budget Calculation Methods window.

![](media/9ff193c02621e227990798fd211b1462.jpg)

1.  Select a calculation method, enter the necessary information and indicate if
    the budget should include the beginning balance amounts. For more
    information about calculation methods, see *Budget calculation methods*.

2.  Choose Calculate to begin the calculation process. If a range hasn’t been
    defined, all your company’s accounts will be included in the calculation.

>   *To modify the amounts for an individual account, simply type over the
>   calculated amounts for each period.*

1.  If you want to save the budget information, choose Save.

>   If you’re calculating a preliminary budget and you’ve decided that you’d
>   like to save it, choose Actual before saving the budget information.

1.  If you want to combine this budget with another, open the Combine Budgets
    window by choosing the Combine Budgets button. For more information, see
    *Combining budgets in Microsoft Dynamics GP.*

2.  If needed, choose File \>\> Print or the printer icon button to view a
    Budget List.

### Deleting a budget

>   You can use the Budget Maintenance window to delete a budget.

>   **To delete a budget:**

1.  Open the Budget Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets \>\> New \>\> using
>   Microsoft Dynamics GP)

![](media/3a4009db3e073ac8ef0ec1cb65a869a3.jpg)

1.  Enter or select a budget ID.

2.  Choose Delete.

### Creating a single-account budget

>   Use the Single-Account Budget Maintenance window to calculate, modify or
>   delete budgets for individual accounts, one account at a time. You can’t
>   calculate preliminary budgets using this window.

>   *Only posting and unit accounts can be used when calculating budgets. You
>   can’t create budgets for variable and fixed allocation accounts.*

>   **To create a single-account budget:**

1.  Open the Single-Account Budget Maintenance window.

>   (Financial \>\> Cards \>\> Financial \>\> Account \>\> Budget button)
>   (Financial \>\> Cards \>\> Financial \>\> Unit Account \>\> Budget button)

![](media/83b6658ffd167b4a3f69fd99f194126d.jpg)

1.  Enter or select the account and budget ID.

2.  Select whether to base the budget on a fiscal year or a date range. If you
    base the budget on a date range, specify a range that crosses one or more
    fiscal years. See *Calculating budgets that overlap fiscal years* for more
    information.

>   *If you’ve selected an existing budget and you change budget years, some
>   periods might not appear in the scrolling window. Recalculate the budget
>   before continuing.*

1.  To restrict access to the budget, choose the password padlock icon button to
    open the User Password Setup window. If you don’t need to restrict access to
    the budget, skip to step 6.

2.  Enter a password and choose OK.

3.  Select a calculation method and indicate if the budget should include the
    account’s beginning balance. For more information about calculation methods,
    see *Budget calculation methods*.

4.  Choose Calculate to begin the calculation process. When the budget has been
    calculated, the amounts will be displayed.

5.  To make changes to the budget amounts without recalculating, type over the
    existing amounts.

6.  To save the budget, choose Save.

7.  To remove the selected account from the budget, choose Delete.

8.  Choose File \>\> Print or the printer icon button to view a Detailed Budget
    report.

### Entering budget transactions

>   Use the Budget Transaction Entry window to create transactions that, when
>   posted, increase or decrease the budget for one or more accounts for
>   specific periods. Amounts are displayed on a period-by-period basis. You can
>   also choose to view period balance amounts, which displays the cumulative
>   budget and budget transaction for each period and all previous periods. A
>   single journal entry can contain adjustments to multiple accounts.

>   **To enter a single budget transaction:**

1.  Open the Budget Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Budget Transactions)

![](media/bf88a7cdb4b5587c466c2afd7806aa85.jpg)

1.  Enter or select a budget journal entry.

2.  Enter or select a batch ID for the journal entry.

3.  Enter or select a transaction date for the journal entry.

4.  Enter or select a budget ID.

5.  Enter a reference for the journal entry. References can be any combination
    of alphanumeric symbols to help you identify the journal entry.

6.  Enter or select an account for which you want to adjust the budget.

7.  Enter the adjustment amount for each period.

8.  Choose File \>\> Print or the printer icon button to view a Budget
    Transaction Edit List report.

>   **To enter multiple budget transactions:**

1.  Perform the steps in *To enter multiple budget transactions:*.

2.  Choose Ranges to open the Account Segment Ranges window.

>   *If you don’t define a range, only the single account that is displayed will
>   be included in the budget calculation. For information on the Account
>   Segment Ranges window, choose the Help button in that window, or see
>   Creating a budget for a range of accounts.*

1.  Select a method for calculating adjustments and indicate if the budget
    should include the beginning balance amounts. For more information on
    calculation methods, see *Budget calculation methods*.

2.  Choose Calculate to begin the calculation process.

### Combining budgets in Microsoft Dynamics GP

>   Use the Combine Budgets window to simplify the process of combining General
>   Ledger budgets. This is useful when multiple departments in your
>   organization create their own budgets, which are then consolidated into a
>   single budget. You can combine only two budgets at a time with this window,
>   but you can repeat the process so that many budgets are combined into one.

>   To combine multiple budgets, first combine two budgets, and then merge
>   others into the new, consolidated budget.

>   Any budget that is added to the new, consolidated budget must have a date
>   range that matches the consolidated budget.

>   **To combine two budgets:**

1.  Open the Combine Budgets window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets \>\> Combine Budgets
>   button)

![](media/3a4009db3e073ac8ef0ec1cb65a869a3.jpg)

1.  Enter or select a master budget ID. This is the ID for the consolidated
    budget that will receive other budgets.

>   If the budget ID doesn’t exist, you must create it in the Budget Maintenance
>   window. You cannot create a budget in the Combine Budgets window.

1.  Enter or select a budget ID to combine with the master budget.

2.  If you want to delete the budget you are merging into the master budget,
    mark the Delete Budget after it is combined check box.

3.  To combine the two budgets, choose Process.

**Chapter 15: Exporting and importing budgets**

>   If you already have created a budget in Microsoft Dynamics GP, you can
>   export it to Microsoft Excel to take advantage of the calculations and
>   formulas available in that application. You can then import the budget into
>   Microsoft Dynamics GP when you’ve finished making changes. With Microsoft
>   Dynamics GP, you can import a budget you’ve created from scratch in
>   Microsoft Excel, provided the budget’s columns are formatted correctly.
>   Refer to *Format requirements for budgets in Microsoft Excel* for more
>   information.

>   This information is divided into the following sections:

-   *Exporting a budget to Microsoft Excel*

-   *Preparing a budget for import from Microsoft Excel*

-   *Importing a budget from Microsoft Excel*

#### Exporting a budget to Microsoft Excel

>   Exporting budgets to Microsoft Excel transfers data from the following
>   Microsoft Dynamics GP budget fields to an Excel worksheet:

-   Budget ID

-   Budget description

-   Account numbers

-   Account descriptions

-   Periods

-   Budget amount for each period for each account

>   The information will be arranged in a worksheet. The name of the worksheet
>   will be the budget description.

>   When you export the budget to an existing workbook, the name of the
>   worksheet tab will be budget ID. When you export to a new workbook, the
>   default file name will be the budget ID. The column headers will be
>   automatically created and based on the number of periods created during
>   Fiscal Period Setup. All of the period amounts will be filled into the
>   columns, as well.

>   Once the budget is exported, you can adjust the layout of the worksheet, as
>   well as the budget amounts.

>   **To export a budget to Microsoft Excel:**

1.  Open the Budget Selection window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets)

![](media/6814a53b87625f1ee211947dc4df5c4c.jpg)

1.  Highlight a budget. Choose Excel and select Export to Excel to open the
    Export Budget to Excel window.

2.  Select a destination for the budget. The destination can be a new workbook
    or an existing one. If you select an existing workbook, the budget will be
    added on a new worksheet in the workbook.

>   *If your worksheet has the same name—the same Budget ID—as an existing
>   worksheet in the workbook you’re exporting to, the existing worksheet will
>   be overwritten. You won’t be able to cancel the export process.*

![](media/dddd7ca4a998f17f6f986b2b1efc7511.jpg)

1.  Choose OK to complete the export process.

>   If you export the budget to a new workbook, you’ll be prompted to enter a
>   name and location for the workbook. When the process is complete, the budget
>   will be displayed in Microsoft Excel.

#### Preparing a budget for import from Microsoft Excel

>   Before you can import a Microsoft Excel budget into Microsoft Dynamics GP,
>   it must be properly formatted. Refer to *Format requirements for budgets in
>   Microsoft Excel* for more information.

>   *To create a Microsoft Excel worksheet with the correct format, you can use
>   the budget wizard to create a blank worksheet with the accounts you
>   specify.*

>   The import process creates a budget with periods corresponding to the period
>   columns in the Microsoft Excel budget. If the number of periods in the
>   Microsoft Dynamics GP budget doesn’t match the number of periods in the
>   Microsoft Excel budget, you’ll be prompted to add periods to the Microsoft
>   Excel budget before completing the import. The amount from each period cell
>   in Microsoft Excel will be transferred to Microsoft Dynamics GP. Once the
>   budget is imported, you can adjust the amounts as needed.

#### Importing a budget from Microsoft Excel

>   You can import Microsoft Excel budget information into an existing Microsoft
>   Dynamics GP budget, or into a newly created Microsoft Dynamics GP budget.

>   *If you choose to import the Microsoft Excel budget worksheet into an
>   existing* Microsoft Dynamics GP *budget, all of the amounts in the*
>   Microsoft Dynamics GP *budget will be overwritten with the amounts from the
>   worksheet.*

>   When you start the budget import process, a series of windows will open in
>   which you can specify information about the budget before it is created. The
>   windows are basically the same whether you choose to import into a new or
>   existing budget.

>   However, if you choose to import into a new budget, you’ll see one
>   additional window, the New Budget Information window. Use that window to
>   enter the budget ID, description, and fiscal year information.

>   The following procedure assumes you’re importing to create a new budget. The
>   steps will remain the same when you choose to import to an existing budget,
>   except that you will skip step 5.

>   **To import a budget from Microsoft Excel:**

1.  Open the Budget Selection window.

>   (Financial \>\> Cards \>\> Financial \>\> Budgets)

![](media/6814a53b87625f1ee211947dc4df5c4c.jpg)

1.  Choose Excel and select Import from Excel to open the Welcome to the Budget
    Wizard for Excel window.

2.  Choose Next to open the Import Budget window.

![](media/394bf7d061c86dafd7b975f488b738ac.jpg)

1.  Decide if the imported budget should be a new budget or if it should
    overwrite an existing budget.

-   To import the Microsoft Excel budget worksheet to a new budget, select A new
    Microsoft Dynamics GP budget and choose Next.

-   To overwrite an existing budget, mark An existing Microsoft Dynamics GP
    budget and enter or select the budget. Choose Next and continue with step 8.

1.  If you’re creating a new budget, the New Budget Information window opens.
    Enter basic identifying information about the budget you’re creating.

![](media/3756a032c3996e477bc8b51687e00ba8.jpg)

1.  To restrict access to the budget with a password, choose the padlock icon
    button to open the User Password Setup window. If you don’t want to restrict
    access to the budget, skip to step 8.

2.  Enter a password and choose OK.

3.  Choose Next to open the Excel File Selection window.

![](media/2d3c2468045c8e684ed27b425662c3c1.jpg)

1.  Enter or select the name of the Excel file to import, then select the
    specific worksheet to import. Choose Next to open the Completing the Budget
    Wizard for Excel window.

2.  Choose Finish to complete the import process.

**Part 3: Transactions**

>   Transaction procedures provide step-by-step instructions for completing
>   General Ledger accounting tasks with Microsoft Dynamics GP.

>   The following information is discussed:

-   *Chapter 16, “Multicurrency transactions,”* explains how to choose the
    currency for entering transactions.

-   *Chapter 17, “Batches,”* explains how to group transactions into batches.

-   *Chapter 18, “Standard and reversing transactions,”* explains standard and
    reversing transactions, the most common transactions in your system.

-   *Chapter 19, “Clearing transactions,”* defines and explains how to use
    clearing transactions.

-   *Chapter 20, “Quick journal transactions,”* explains quick journals, a
    time-saving journal entry that doesn’t require batches.

-   *Chapter 21, “Transaction deferrals,”* describes the methods available for
    deferring revenues or distributing expenses over a specified period.

-   *Chapter 22, “Posting,”* describes posting, the process of transferring your
    temporary transactions to the company’s permanent records.

-   *Chapter 23, “Correcting transactions,”* explains how to correct
    transactions, whether or not the transaction has been posted.

-   *Chapter 24, “Matching transactions,”* describes the process of linking
    related transaction distributions from different journal entries.

**Chapter 16: Multicurrency transactions**

>   If you’re using Multicurrency Management with General Ledger, you can choose
>   the currency you want to use when entering transactions.

>   For information about setting up your financial system to use multiple
>   currencies, including the euro, refer to the Multicurrency Management
>   documentation.

>   This information is divided into the following sections:

-   *Viewing multiple currencies*

-   *Exchange rate and document date*

-   *Multicurrency account distributions*

#### Viewing multiple currencies

>   You can choose to view multicurrency transactions in the originating or the
>   functional currency. Choose View \>\> Currency \>\> Functional or
>   Originating while entering a transaction. The option will be saved on a per
>   user, per window basis.

>   You also can use the Currency list button in the windows that support
>   changing the currency view.

>   The View menu and currency list button are available in the following
>   windows:

-   Transaction Entry

-   Summary Inquiry

-   Detail Inquiry

-   Journal Entry Inquiry

-   History Summary Inquiry

-   History Detail Summary

>   The first time you open these windows after registering Multicurrency

>   Management, all the transactions will be displayed in the originating
>   currency. If you change the currency view, that option will be the default
>   view the next time you open that window.

#### Exchange rate and document date

>   If a transaction’s currency ID is not in the functional currency, a rate
>   type and associated exchange rate table are assigned to the transaction. The
>   rate type is the default rate type for the Financial series specified in the
>   Multicurrency Setup window. You also can choose the currency expansion
>   button to open the Exchange Rate Entry window to view or modify the default
>   exchange rate.

>   The document date assigned to a transaction determines which exchange rate
>   is used, based on the currency ID and associated rate type that’s entered
>   for the transaction. Each time you change the document date on a
>   multicurrency transaction, the system searches for a valid exchange rate. If
>   a valid rate doesn’t exist, you can enter an exchange rate using the
>   Exchange Rate Entry window. If you’ve entered a General Ledger posting date
>   that’s different from the document date, the exchange rate expiration date
>   must be after the posting date.

#### Multicurrency account distributions

For multicurrency transactions, distribution amounts are displayed in both the
functional and originating currencies. However, you can change only the
originating amounts.

When you’re entering a multicurrency transaction, the originating debit and
credit amounts must balance. If the functional equivalents don’t balance, the
difference is posted automatically to a Rounding Difference account and a
distribution type of Round identifies the distribution amount.

For example, assume you’ve entered a transaction in the euro currency, with a
purchase amount of 28,755.42 EUR, a trade discount of 586.84 EUR, a discount
available of 1544.33 EUR and the exchange rate is 1.0922. The distributions
would be calculated as follows:

| **Account**      | **Euro debit** | **Euro credit** | **US Dollars debit** | **US Dollars credit** |
|------------------|----------------|-----------------|----------------------|-----------------------|
| Accounts Payable | 28,755.42 EUR  |                 | \$31,406.67          |                       |
| Trade Discount   | 586.84 EUR     |                 | \$640.95             |                       |
| Discount         | 1544.33 EUR    |                 | \$1686.72            |                       |
| Accrued          |                | 30,886.59 EUR   |                      | \$33,734.33           |
| Totals           | 30,886.59 EUR  | 30,886.59 EUR   | \$33,734.34          | \$33,734.33           |
| Rounding         |                |                 |                      | \$0.01                |
| Totals           | 30,886.59 EUR  | 30,886.59 EUR   | \$33,734.34          | \$33,734.34           |

>   Available

>   Purchases

>   Difference

**Chapter 17: Batches**

>   General Ledger transactions can be entered individually or in batches. A
>   batch is a group of transactions identified by a unique name or number. By
>   entering and posting transactions in batches, you can group similar
>   transactions during data entry and review them before posting. More than one
>   person can enter transactions in the same batch, but not at the same time.
>   Also, a batch can’t be posted if anyone is making changes to it.

>   This information is divided into the following sections:

-   *Creating a batch*

-   *General Ledger batch approval workflow*

-   *Modifying or deleting a batch*

#### Creating a batch

>   Use the Batch Entry window to create batches. A batch is a group of
>   transactions identified by a unique name or number. If you’ve decided to
>   enter transactions in batches, they can be posted using the batch, series,
>   or master posting procedures.

>   For more information about batch posting, see *Chapter 22, “Posting.”*

>   **To create a batch:**

1.  Open the Batch Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Batches)

![](media/f2bcd17f9cef386fe894a14ac15a74ba.jpg)

1.  Enter or select a batch ID to identify the batch. Batches entered in
    different transaction entry windows might have the same ID. If you aren’t
    sure which batch to select, you can use the Batch ID lookup window to view
    the origins of transactions within each batch.

2.  Select a batch origin. You can select General Entry, Clearing Entry, or
    Budget Transactions. Once you’ve saved the batch, you can’t change the
    origin.

3.  Enter a batch comment, such as a brief description of the transactions that
    will be entered in the batch.

4.  Select a frequency. If you chose a frequency other than Single Use, enter
    the number of recurring postings. If you want the batch to remain in the
    system indefinitely, enter zero in the Remaining Posting field.

>   If you choose a frequency of miscellaneous, enter the number of recurring
>   postings and the days to increment.

1.  To print the breakdown allocation accounts on the edit lists, mark the Break
    Down Allocation option.

2.  To clear the distribution amounts for recurring batches after posting, mark
    the Clear Recurring Amounts After Posting option.

3.  You can define batch entry requirements. Refer to the System User’s Guide
    for information about batch requirements and approvals.

>   *If the Allow Negative Debits and Credits in General Ledger option is marked
>   in the Company Setup Options window, you can enter negative amounts in the
>   batch control total field.*

1.  Choose Save to save the batch or choose Transactions to open the Transaction
    Entry window, where you can enter transactions in the batch.

2.  You can choose File \>\> Print or the printer icon button to verify the
    accuracy of the transactions you’ve entered before posting.

3.  If you’re using Workflow, submit the batch for approval if needed. See
    *General Ledger batch approval workflow* for more information.

#### General Ledger batch approval workflow

If your company uses the Workflow feature among its business controls, batches
might have to be approved before posting. The rules for approving batches can
defined to fit your organization’s needs. Multiple approvers might be required,
or approval might not be required for batches with few transactions or small
currency amounts. When a batch is ready to be approved, approvers can be
notified and the batches can be approved, using Outlook®, Microsoft Dynamics GP,
or Internet Explorer®. After a batch is approved, it can be posted. For more
information about

Workflow, see the System Setup Guide (Help \>\> Printable Manuals \>\> select

System \>\> select System Setup Guide) or the Workflow Administrator’s Guide
(Help \>\> Printable Manuals \>\> select System \>\> select Workflow
Administrator’s Guide).

Before you can use the batch approval workflow for General Ledger, you must turn
off the Require Batch Approval feature in Microsoft Dynamics GP. To do so, open
the Posting Setup window (Administration \>\> Setup \>\> Posting \>\> Posting)
and select the Financial series. Unmark the Require Batch Approval option for
the General Ledger and Clearing Entry origins.

#### Modifying or deleting a batch

Use the Batch Entry window to modify or delete a batch. You can change or delete
unposted batches at any time. Recurring batches are deleted after the batch has
been posted the number of times you specify in the Recurring Posting field.

>   If you are using Workflow you must resubmit the batch if you modify or
>   delete any transactions in an approved batch.

>   See *Correcting an unposted transaction* for information about changing the
>   transactions in a batch.

>   **To modify or delete a batch:**

1.  Open the Batch Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Batches)

1.  To modify the batch, replace the incorrect information with correct
    information. Choose Save to save the changes or resubmit the batch for
    approval, if you are using Workflow. .

2.  To delete the batch, choose Delete and close the window.

>   **To modify a batch using the action pane:**

1.  In the navigation pane, choose the Financial button, then choose the General
    Ledger Batches list.

2.  Mark a batch to modify.

3.  In the new group, choose Edit to open the Batch Entry window.

4.  To delete a batch, choose Delete.

5.  To correct the batch, replace the incorrect information with the correct
    information. Choose save to save the changes or resubmit the batch for
    approval, if you are using Workflow.

**Chapter 18: Standard and reversing transactions**

>   Standard transactions are entered and posted once. If they are assigned to a
>   recurring batch, standard transactions can be posted periodically, such as
>   weekly or monthly, or on a specific date, and then automatically or manually
>   deleted from Microsoft Dynamics GP.

>   A reversing transaction reverses the distributions—debit and credit
>   entries—of a previous transaction. Generally speaking, entries that involve
>   the accrual of assets (such as unbilled revenues) or the accrual of
>   liabilities (such as salaries) might be reversed because they result in a
>   future cash receipt or payment. Examples of such accruals include salaries
>   that haven’t been paid or revenues that haven’t been billed.

>   When entering transactions, transaction information is collectively referred
>   to as audit trail information. For example, the journal entry number,
>   transaction date, source document code, and reference appear on
>   cross-reference reports. This information helps to trace the history of a
>   specific transaction and might be used by external auditors to verify the
>   accuracy of your records and record-keeping processes.

>   This information is divided into the following sections:

-   *Entering a standard or reversing transaction*

-   *Voiding or deleting a saved standard or reversing transaction*

-   *Understanding Value-Added Taxes*

-   *Calculating and distributing tax*

#### Entering a standard or reversing transaction

>   Use the Transaction Entry window to enter standard and reversing
>   transactions. For more information about posting, see *Chapter 22,
>   “Posting.”*

>   **To enter a standard or reversing transaction:**

1. Open the Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> General)

![](media/042841c3e8c3855721198c6c617f5bc5.jpg)

1.  Enter a journal entry number or accept the default number.

2.  If you’re using batches, enter or select a batch. If you are using Workflow
    and are not allowed to approve batches, don't assign the cash receipt to a
    batch that is pending approval. If you do, you won't be able to enter cash
    receipt information.

3.  Enter a transaction type: standard or reversing.

4.  Enter the transaction date, source document code, reference, and currency
    ID. If the transaction is reversing, also enter a reversing date.

5.  Select the reporting ledger type to which the transaction should apply:
    Base, IFRS, or Local. Note that the reporting ledger type is available only
    when you choose to allow reporting ledgers in the General Ledger Setup
    window.

6.  Enter accounts and transaction amounts.

>   Transactions can contain either posting or unit accounts. If you enter a
>   unit account—which tracks nonfinancial amounts such as head count or square
>   footage—on a transaction, a debit entry will increase the balance of the
>   selected unit account and a credit entry will decrease the balance. Amounts
>   posted to unit accounts won’t have any effect on the transaction total.

>   *If the Allow Negative Debits and Credits in General Ledger option is marked
>   in the Company Setup Options window, you can enter negative transaction
>   amounts.*

>   If your transactions include tax, refer to *Understanding Value-Added Taxes*
>   and *Calculating and distributing tax* for more information.

1.  If you’re entering transactions individually—without a batch—choose Post.

>   *We recommend that you back up company data before posting. If power
>   fluctuates or some other problem occurs, you can restore your data and begin
>   the posting process again. For more information about making backups, refer
>   to the System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

>   When you close the Transaction Entry window, the General Posting Journal
>   might be printed for all transactions posted using the transaction-level
>   method, depending on how you set up your system.

1.  If you’re entering transactions in a batch, choose Save.

#### Voiding or deleting a saved standard or reversing transaction

You can use the Transaction Entry window to void or delete transactions that
have been saved, but not posted.

By default, you can delete saved transactions. However, you can change default
settings so that you must void saved transactions instead of deleting them. See
*Setting up default entries and preferences* for more information.

You can void transactions originating in other modules if you marked the
Voiding/ Correcting of Subsidiary Transactions option in the General Ledger
Setup window. See *Setting up default entries and preferences* for more
information.

>   **To void or delete a saved standard or reversing transaction:**

1.  Open the Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> General)

1.  Enter or select the journal entry number for the transaction you’re voiding
    or deleting.

2.  Choose Void to void the transaction or Delete to delete the transaction.

3.  Close the window.

#### Understanding Value-Added Taxes

>   General Ledger accommodates the different tax rates on goods and services
>   sold in different cities, states, provinces, and countries/regions. These
>   taxation methods include Value-added Taxes (VAT). VAT is a system of input
>   taxes due on purchases and output taxes due on sales.

>   Each country/region that uses VAT has its own rate of taxation and often has
>   different rates for different goods or zones. VAT is collected on sales. Any
>   credit for tax paid on purchases also is tracked. The difference is remitted
>   to the taxation authority.

>   VAT entries in General Ledger transactions are used to compile the Detail
>   Tax Report, which displays the total sale or purchase amount, the total tax
>   amount, the total EU sale or purchase amount, and the total EU tax.

>   The goods value is the same as the net purchase amount, which includes
>   freight and miscellaneous charges, if taxable, and any trade discount. If
>   several different tax details are used for a transaction, you must
>   distribute the total goods value amount to all appropriate tax details and
>   enter the tax in the Tax Amount field. This requirement applies even if no
>   tax will be paid on the entire transaction or on individual items included
>   on the transaction.

>   For example, you’re entering a purchase amount of £500. However, £250 of
>   this purchase is exempt from tax. To distribute the exempt portion of the
>   transaction, enter or select the appropriate tax-exempt detail. Then, enter
>   a goods value of £250 for the tax-exempt detail and the remaining taxable
>   goods value of £250 for the input tax detail. The tax amount automatically
>   will be adjusted to reflect the reduction in the taxable goods value.

>   For information about setting up your system to calculate VAT, see the
>   System Setup instructions (Help \>\> Contents \>\> select Setting Up the
>   System).

#### Calculating and distributing tax

>   Use the Tax Entry window to enter tax information for a standard General
>   Ledger transaction if you’ve marked the Calculate Taxes in General Ledger
>   option in the Company Setup Options window.

>   Use General Ledger to enter taxable transactions that can’t be entered in
>   the Payables Management, Receivables Management, Purchase Order Processing,
>   Invoicing, or Sales Order Processing modules.

For example, a taxable expense reimbursement to an employee should be entered in
General Ledger. You could enter this transaction in Payables Management, but it
would require that the employee be set up as a vendor. General Ledger also can
be used to make corrections to tax transactions from other modules.

>   If you’ve registered Multicurrency Management, use the View menu or Currency
>   list button in the Transaction Entry window to choose to view transactions
>   in the originating or the functional currency.

>   **To calculate and distribute tax:**

1.  Open the Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> General)

1.  Enter the transaction.

>   *Be sure to select a transaction type of Standard. You cannot enter tax
>   information for Intercompany, Reversing, Clearing, or Quick Journal
>   entries.*

>   A journal entry that contains tax records can be saved in a single-use or
>   recurring batch.

>   When a journal entry that contains tax records is deleted, all tax
>   information associated with the transaction is removed.

1.  Choose Tax Entry to open the Tax Entry window.

![](media/d90ddd355a1435d9daac150aa463dc46.jpg)

1.  Decide if the transaction is a debit or a credit.

2.  Enter or select the account number of the account.

3.  Enter an amount for the transaction. This is the sales or purchase amount
    that tax calculations are based on. Each time the amount is changed, the
    taxable sales/purchases amount and tax amount are recalculated.

4.  Enter or select a tax detail. A taxable sales/purchases amount and tax
    amount are automatically calculated when the tax detail is selected, based
    on the amount entered, the tax type, and tax percent for the tax detail.
    Each time the tax detail is changed, the taxable sales/purchases amount and
    tax amount are recalculated.

>   Any of the six types of tax details can be selected, but only percent of
>   sale/ purchase, percent of sale/purchase with taxable tax, and tax included
>   with item price tax details calculate a tax amount. Tax details that use the
>   percent of cost,

>   flat amount, or percent of another tax detail can be selected, but will
>   calculate a tax of \$0.00. The taxable sales/purchases amount is set to the
>   amount if one of these tax details is selected.

1.  In the Distribution Reference field, you can enter a description for the new
    General Ledger distributions. The Reference entry from the Transaction Entry
    window is the default Distribution Reference.

2.  Choose Create to create tax distributions. The Tax Entry window closes, and
    the Transaction Entry window is updated.

>   Two distributions are created in Transaction Entry. The first distribution
>   is the taxable sales/purchases amount portion of the tax record, and the
>   second is the tax amount portion. Only the account numbers and distribution
>   references can be edited for the distributions; you can't edit the debit or
>   credit amounts.

>   *The debit or credit amounts for the taxable sales/purchases amount and tax
>   amount distributions can be negative. If negative amounts are entered in the
>   Tax Entry window, the taxable sales/purchases amount and tax amount
>   distributions also will be negative.*

**Chapter 19: Clearing transactions**

>   Clearing transactions are useful when accounts are obsolete but can’t be
>   deleted because they have activity for open periods.

>   This information is divided into the following sections:

-   *Understanding clearing transactions*

-   *Entering a clearing transaction*

-   *Voiding or deleting a saved clearing transaction*

#### Understanding clearing transactions

>   When you’re no longer using an account and want to transfer its balance to
>   another account, you need to make a clearing transaction. With a clearing
>   entry, the account balance will be transferred, the transaction activity
>   will remain with the original account and the account remains active.

*If you’re using Multicurrency Management, you cannot use clearing
transactions.*

>   You also can use clearing transactions for accounts with balances that
>   periodically are cleared to other accounts, such as departmental sales
>   accounts, which are cleared to controlling sales accounts at the end of each
>   accounting period. You’ll still have a record of the account’s activity, and
>   you can reuse the account later for the next period.

>   When entering clearing transactions, if you select the year-to-date balance,
>   the system transfers the year-to-date balance through the period in which
>   the transaction date occurs. For example, if the transaction date is January
>   15, 2004, all of the January transactions are cleared, even if there are
>   transactions after January 15, 2004, in that period. If you select the
>   period balance, the system transfers the entire balance for the period in
>   which the transaction date falls. You can post clearing transactions only to
>   open years. You can’t post clearing transactions that fall within a
>   historical year.

>   If the account you enter is a posting account, the offsetting account also
>   must be a posting account or a posting allocation account. The same
>   principle applies to unit accounts: if the account to be cleared is a unit
>   account, the offsetting account must be a unit account or unit allocation
>   account.

#### Entering a clearing transaction

>   Use the Clearing Entry window to enter clearing transactions. You can post
>   clearing transactions only to open years. You can’t enter clearing
>   transactions for a historical year.

>   **To enter a clearing transaction:**

1.  Open the Clearing Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Clearing)

![](media/12ee012b01734f7b73d016b3bc534889.jpg)

1.  Enter a journal entry number or accept the default number.

2.  If you’re using batches, enter or select a batch.

3.  Enter the transaction date, source document code, and reference.

4.  Mark Year-to-Date or Trx Period to indicate which periods’ account balances
    will be cleared during posting.

5.  Enter or select an account to clear and an offset account that will receive
    the cleared account’s balance.

6.  If you’re entering transactions individually, choose Post.

>   *We recommend that you back up company data before posting. If power
>   fluctuates or some other problem occurs, you can restore your data and begin
>   the posting process again. For more information about making backups, refer
>   to the System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

>   When you close the Clearing Entry window, the Clearing Posting Journal will
>   be printed for all transactions posted using the transaction-level method.

>   See *Chapter 22, “Posting,”* for information about posting transactions in a
>   batch.

1.  If you’re entering transactions in a batch, choose Save.

#### Voiding or deleting a saved clearing transaction

You can use the Clearing Entry window to void or delete transactions that have
been saved, but not posted.

By default, you can delete saved transactions. However, you can change default
settings so that you must void saved transactions instead of deleting them. See
*Setting up default entries and preferences* for more information.

>   **To void or delete a saved clearing transaction:**

1.  Open the Clearing Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Clearing)

1.  Enter or select the journal entry number for the transaction you’re voiding
    or deleting.

2.  Choose Void to void the transaction or Delete to delete the transaction.

3.  Close the window.

**Chapter 20: Quick journal transactions**

>   Quick journals provide a method of time-saving journal entry that doesn’t
>   require batches.

>   This information is divided into the following sections:

-   *Understanding quick journal transactions*

-   *Entering a quick journal transaction*

-   *Voiding or deleting a saved quick journal transaction*

#### Understanding quick journal transactions

>   Transactions that require many different entries can be simplified using the
>   quick journal method. For example, payroll transactions often require many
>   entries, such as debits to employer’s tax expense and wages expense, broken
>   down by department. Instead of entering nearly a dozen accounts, you can set
>   up a quick journal and enter only the transaction amounts. The total of the
>   amounts you enter will be offset to the Cash account. For transactions that
>   recur and affect many accounts but are offset to a single account, Quick
>   Journal Entry can save data entry time.

>   Quick journals are set up in the Quick Journal Setup window. See *Chapter
>   10, “Quick journal transactions setup,”* for more information.

>   If you’re using Multicurrency Management, you can enter quick journals only
>   in your company’s functional currency.

>   The amounts entered in a quick journal can be both debits and credits. The
>   difference between total debits and credits is the amount applied to the
>   offset account. Unlike standard transactions entered individually without a
>   batch, quick journal transactions can be saved and posted at a later date.

>   You also can enter a control balance at any point during the data entry
>   process to double-check totals. The control balance you enter will be
>   compared with the total of all debit and credit amounts entered for the
>   distribution accounts. If the two balances don’t match, you won’t be able to
>   post the quick journal transaction.

>   Quick journal entries can be posted individually, or by using the Series
>   Posting or Master Posting window. If you select series or master posting,
>   the quick journal ID will be used as an identifier, similar to batch ID; all
>   journal entries for a single quick journal are posted when you select the
>   quick journal and choose Post.

#### Entering a quick journal transaction

>   Use the Quick Journal Entry window to enter transactions you've identified
>   as good candidates for quick journal entry. Quick journal transactions
>   always are assigned to the Base reporting ledger. For more information on
>   reporting ledgers, see *Setting up default entries and preferences*.

>   **To enter a quick journal transaction:**

1.  Open the Quick Journal Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Quick Journal)

![](media/ee638add91e8d28dd8bab958d94cf33d.jpg)

1.  Enter a journal entry number or accept the default.

2.  Enter or select a quick journal ID.

>   Once you’ve chosen a quick journal, the description, reference, offset
>   account, source document code, breakdown allocations, and accounts you
>   entered during the setup process appear as defaults.

>   *If you enter only unit accounts in the scrolling window, the offset
>   account’s balance isn't updated when you post the transaction.*

>   You can add or delete accounts that appear as default accounts, but to
>   permanently change the quick journal setup, you must use the Quick Journal
>   Setup window.

>   A default offset account is displayed, but you can select another offset
>   account if you marked the Allow Override option during the setup process.
>   Refer to *Setting up a quick journal* for more information.

1.  Enter or accept the default transaction date, source document code,
    reference, and offset account.

2.  If you want to confirm your entries, enter a control balance. The control
    balance will be compared with the total of all debit and credit amounts
    entered for the distribution accounts. If the two balances don’t match, you
    won’t be able to post.

3.  Enter debits and credits and double-check the balance.

>   *You don’t have to enter amounts for all accounts listed in the Quick
>   Journal Entry window. Accounts can have zero balances and the transaction
>   will still be posted. However, the actual amounts must equal the control
>   total you’ve entered before you can post the transaction.*

1.  Choose File \>\> Print or the printer icon button to verify your entries
    with a Quick Entry Edit List, before posting.

>   *We recommend that you back up company data before posting. If power
>   fluctuates or another problem occurs, you can restore your data and begin
>   the posting process again. For more information about making backups, refer
>   to the System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

1.  Save or post the entry.

2.  Depending on the way your system has been set up, the Quick Journal Posting
    Journal might be printed automatically when you post.

>   See *Chapter 22, “Posting,”* for information about posting transactions.

#### Voiding or deleting a saved quick journal transaction

>   You can use the Quick Journal Entry window to void or delete transactions
>   that have been saved, but not posted.

>   By default, you can delete saved transactions. However, you can change
>   default settings so that you must void saved transactions instead of
>   deleting them. See *Setting up default entries and preferences* for more
>   information.

>   **To void or delete a saved quick journal transaction:**

1.  Open the Quick Journal Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Quick Journal)

1.  Enter or select the journal entry number for the transaction you’re voiding
    or deleting.

2.  Choose Void to void the transaction or Delete to delete the transaction.

3.  Close the window.

**Chapter 21: Transaction deferrals**

>   You can defer transaction distributions for transactions originating from
>   General Ledger, Receivables Management, Sales Order Processing, Payables
>   Management, or Purchase Order Processing. You can enter the information for
>   each deferral transaction individually, or you can use deferral profiles to
>   speed data entry by applying the same default settings to similar deferral
>   transactions.

>   This information includes the following sections:

-   *Deferring a transaction distribution*

-   *Deferring a transaction distribution using a profile*

-   *Entering a General Ledger deferral transaction*

-   *Entering a General Ledger deferral transaction using a profile*

-   *Creating a retroactive deferral transaction*

-   *Posting deferral transactions*

-   *Voiding a deferral transaction*

#### Deferring a transaction distribution

>   Use the Deferral Entry window to defer a transaction distribution for
>   transactions originating from Receivables Management, Payables Management,
>   Sales Order Processing, Invoicing, or Purchase Order Processing. For
>   information about deferring General Ledger transactions, see *Entering a
>   General Ledger deferral transaction* and *Entering a General Ledger deferral
>   transaction using a profile*.

>   When you use the Deferral Entry window, you will specify the deferral and
>   recognition accounts to use, the beginning and end dates for the deferral,
>   and the method for calculating the deferred amounts. If you want to ensure
>   that similar transactions are entered with consistent information, you can
>   use a deferral profile. For more information, see *Deferring a transaction
>   distribution using a profile*.

>   You can open the Deferral Entry window from the following distribution entry
>   windows.

| **Module**                | **Distribution entry window**           | **Navigation**                                                                                                                 |
|---------------------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Receivables Management    | Sales Transaction Distribution Entry    | Sales \>\> Transactions \>\> Transaction Entry \>\> Enter or select a customer ID \>\> Distribution button                     |
| Sales Order Processing    | Sales Distribution Entry                | Sales \>\> Transactions \>\> Sales Transaction Entry \>\> Enter or select a document number for an invoice or return \>\>      |
| Invoicing                 | Invoice Distribution Entry window       | Sales \>\>Transactions \>\> Invoice Entry \>\> Enter or select a document number \>\> Distributions button                     |
| Payables Management       | Payables Transaction Entry Distribution | Purchasing \>\> Transactions \>\> Transaction Entry \>\> Enter or select a voucher number \>\> Distributions button            |
| Purchase Order Processing | Purchasing Distribution Entry           | Purchasing \>\> Transactions \>\> Receivings Transaction Entry \>\> Enter or select a receipt number \>\> Distributions button |

>   Distributions button

>   **To defer a transaction distribution:**

1.  Enter or select a transaction and open the appropriate distribution window.
    For example, if you wanted to defer the revenue from a transaction entered
    in the Receivables Transaction Entry window, you would enter the transaction
    amounts, and choose Distribution to open the Sales Transaction Distribution
    Entry window.

2.  In the distribution entry window, select the distribution you want to defer.

![](media/4cc6292e026e5880cc5deb14a59da3df.jpg)

>   Depending on how your default posting accounts are set up, you may need to
>   change the account to a deferral account. For example, if you’re deferring
>   the revenue for a prepaid maintenance contract, you could change the SALES
>   posting account to the account you use for deferred revenue.

1.  From the Additional menu, choose Deferral to open the Deferral Entry window.

![](media/d6fe788dd0e6c713090d9855766da1a2.jpg)

>   Enter the beginning and end of the period and select the method to use for
>   apportioning the deferred amounts over that period.

-   The Days In Period method apportions the amount based on the number of days
    in a fiscal period.

-   The Equal Per Period method allocates an equal amount per fiscal period.

-   The Miscellaneous method allows you to specify the length of the periods and
    allocates an equal amount per period.

1.  If you’re using the Balance Sheet deferral posting method, enter or select
    the recognition account for the deferral. If you’re using the Profit and
    Loss deferral posting method, enter or select the additional deferral and
    recognition accounts.

2.  When you’ve entered this information, the individual deferral transactions
    will be calculated and appear in the lower scrolling window. If necessary,
    you can edit the date, description, and amount for each deferral
    transaction.

3.  Choose Save Account when the information is correct, then choose OK to close
    the window.

4.  If you need to defer another distribution for this transaction, repeat steps
    2 through 6.

5.  Close the distribution entry window and save or post the transaction. If you
    print an edit list for a batch that includes deferred transactions, the
    Deferral Edit List will also be printed, showing how the deferrals will be
    posted.

#### Deferring a transaction distribution using a profile

>   Use the Deferral Profile Selection window to defer a transaction
>   distribution using a deferral profile. A deferral profile provides default
>   entries to help ensure that similar transactions are entered with consistent
>   information. For example, if you routinely enter transactions for service
>   contracts your company offers, and the revenue is recognized over a 12-month
>   period, you could use a deferral profile for these service contract
>   transactions.

>   The profile specifies the accounts to be used, and the method for
>   calculating how the deferred revenue is recognized. For information on
>   setting up profiles, see *Setting up a deferral profile*.

>   You can open the Deferral Profile Selection window from the following
>   distribution entry windows.

| **Module**                | **Distribution entry window**           | **Navigation**                                                                                                            |
|---------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Receivables Management    | Sales Transaction Distribution Entry    | Sales \>\> Transactions \>\> Transaction Entry \>\> Enter or select a customer ID \>\> Distribution button                |
| Sales Order Processing    | Sales Distribution Entry                | Sales \>\> Transactions \>\> Sales Transaction Entry \>\> Enter or select a document number for an invoice or return \>\> |
| Invoicing                 | Invoice Distribution Entry window       | Sales \>\> Transactions \>\> Invoice Entry \>\> Enter or select a document number \>\> Distributions button               |
| Payables Management       | Payables Transaction Entry Distribution | Purchasing \>\> Transactions \>\> Transaction Entry \>\> Enter or select a voucher number \>\> Distributions button       |
| Purchase Order Processing | Purchasing Distribution Entry           | Purchasing \>\> Transactions \>\> Receivings Transaction Entry                                                            |

>   Distributions button

>   \>\> Enter or select a receipt number \>\> Distributions button

>   **To defer a transaction distribution using a profile:**

1.  Enter or select a transaction and open the appropriate distribution window.
    For example, if you wanted to defer the revenue from a transaction entered
    in the Receivables Transaction Entry window, you would enter the transaction
    amounts, and choose Distribution to open the Sales Transaction Distribution
    Entry window.

2.  In the distribution entry window, select the distribution you want to defer.

>   Depending on how your default posting accounts are set up, you may need to
>   change the account to a deferral account. For example, if you’re deferring
>   the revenue for a prepaid maintenance contract, you could change the SALES
>   posting account to the account you use for deferred revenue.

1.  From the Additional menu, choose Deferral Profile to open the Deferral
    Profile Selection window.

![](media/f8ae53898e7e0a6abd48de82ca9350a6.jpg)

>   Enter or select the profile you want to use to defer this distribution.

1.  Depending on how you have set up the deferrals feature and the options for
    access to this profile, you may be able to change the deferral and
    recognition accounts, the calculation method and period information, and
    each period’s transaction information.

2.  Choose Allocate to save this distribution deferral and close the window.

3.  If you need to defer another distribution for this transaction, repeat steps
    2 through 5.

4.  Close the distribution entry window and save or post the transaction. If you
    print an edit list for a batch that includes deferred transactions, the
    Deferral Edit List will also be printed, showing how the deferrals will be
    posted.

#### Entering a General Ledger deferral transaction

>   Use the Deferral Document Entry window to enter a deferral transaction
>   directly in General Ledger. For example, you can use this window to create
>   the deferral transactions for an amount that has been posted to a deferral
>   account.

>   When you use the Deferral Document Entry window, you will specify the
>   deferral and recognition accounts to use, the beginning and end dates for
>   the deferral, and the method for calculating the deferred amounts. If you
>   want to ensure that similar transactions are entered with consistent
>   information, you can use a deferral profile. For more information, see
>   *Entering a General Ledger deferral transaction using a profile*.

>   **To enter a General Ledger deferral transaction:**

1.  Open the Deferral Document Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Financial Deferral \>\>
>   Deferral Document Entry)

![](media/4b13071e03833ef29d6d52f0c1f4dfa7.jpg)

1.  Enter the beginning and end of the period and select the method to use for
    apportioning the deferred amounts over that period.

2.  Enter a GL Reference and enter or select a batch.

3.  Enter the amount to be deferred, and the recognition and deferral accounts.
    If necessary, you can change which account will be debited or credited by
    clicking the Dr/Cr buttons next to the account field.

4.  The individual deferral transactions will be calculated and appear in the
    lower scrolling window. If necessary, you can edit the date, description,
    and amount for each deferral transaction.

5.  Choose Save to save the transaction.

#### Entering a General Ledger deferral transaction using a profile

>   Use the Deferral Profile Document Entry window to enter a deferral
>   transaction directly in General Ledger using a profile. A deferral profile
>   provides default entries that can help ensure that similar transactions are
>   entered with consistent information. For example, if you routinely enter
>   transactions for asset depreciation, you could use a deferral profile for
>   these depreciation transactions. The profile specifies the accounts to be
>   used, and the method for calculating how the deferred revenue is recognized.
>   For information on setting up profiles, see *Setting up a deferral profile*.

>   **To enter a General Ledger deferral transaction using a profile:**

1.  Open the Deferral Profile Document Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Financial Deferral \>\>
>   Deferral Profiles)

![](media/9c9767e8fb93e4e17602667f51a4ec78.jpg)

1.  Enter or select the profile you want to use for this deferral transaction.

2.  Enter the amount to be deferred, the batch for this transaction, and a
    reference.

3.  Depending on how you have set up the deferrals feature and the options for
    access to this profile, you may be able to change the deferral and
    recognition accounts, the calculation method and period information, and
    each period’s transaction information for this distribution deferral.

4.  Choose Save to save the transaction.

#### Creating a retroactive deferral transaction

>   Use the Retroactive Deferral Transaction Entry window to create distribution
>   deferrals to apply to previously posted transactions originating from the
>   Sales or Purchasing series.

>   *Retroactive deferral transactions should use the Profit and Loss deferral
>   posting method. This allows the posted amount to be reversed from the Profit
>   and Loss account it was originally posted to and transferred to a deferrals
>   account. If you need to change the deferral posting method for a series, you
>   must first post all unposted deferral transactions. For more information on
>   changing the deferral posting method, see Setting up revenue/expense
>   deferrals.*

>   **To create a retroactive deferral transaction:**

1.  Open the Retroactive Deferral Transaction Entry window.

>   (For sales transactions: Financial \>\> Transactions \>\> Financial \>\>
>   Sales

>   Retroactive \>\> Retroactive Deferral)

>   (For purchase transactions: Financial \>\> Transactions \>\> Financial \>\>
>   Purchasing Retroactive \>\> Retroactive Deferral)

![](media/354c788f37ddaa8a6dc6e7f6b3b95c32.jpg)

1.  Enter or select the customer ID or vendor ID for the transaction you want to
    defer.

2.  Enter or select a batch for the deferral transactions.

3.  If necessary, you can restrict the number of transactions that appear in the
    scrolling window by entering a range restriction or by displaying only open
    or historical transactions. Choose Redisplay to update the list of
    transactions.

4.  Select the transaction you want to enter deferrals against and click the
    Document Number link to open the Distribution Deferral Information window.

![](media/d674e9f3cd36b62aed897d83e962613e.jpg)

1.  Select the distribution you want to defer and choose Extras \>\> Additional
    \>\> Deferral to open the Deferral Entry window or choose Extras \>\>
    Additional \>\> Deferral Profile to open the Deferral Profile Selection
    window.

2.  Enter and save the necessary deferral information. For more information, see
    *Deferring a transaction distribution* and *Deferring a transaction
    distribution using a profile*.

3.  If you need to defer another distribution for this transaction, repeat steps
    6 through 7. Otherwise, choose OK to close the Distribution Deferral
    Information window.

4.  If you need to defer another transaction for this customer or vendor, repeat
    steps 5 through 8. Otherwise, choose Save to save the deferral transactions.

5.  Post the batch. For more information, see *Posting deferral transactions*.

#### Posting deferral transactions

>   You can post deferral transaction batches individually, or several at a
>   time. You’ll use different windows to post deferral transactions, depending
>   on whether they are General Ledger deferral transactions, or retroactive
>   deferral transactions for the Sales or Purchasing series.

>   **To post individual deferral transaction batches:**

1.  Open the Deferral Batch Entry window.

>   (For General Ledger deferrals: Financial \>\> Transactions \>\> Financial
>   \>\> Financial Deferral \>\> Deferral Batches)

>   (For retroactive Sales deferrals: Financial \>\> Transactions \>\> Financial
>   \>\> Sales Retroactive \>\> Retroactive Batches)

>   (For retroactive Purchasing deferrals: Financial \>\> Transactions \>\>
>   Financial \>\> Purchasing Retroactive \>\> Retroactive Batches)

![](media/e0428d6eb1f63c855c1e193d7f84ee3b.jpg)

1.  Enter or select the batch you want to post.

2.  Choose Post.

>   **To post multiple deferral transaction batches:**

1.  Open the Deferral Posting window.

>   (For General Ledger deferrals: Financial \>\> Transactions \>\> Financial
>   \>\>

>   Financial Deferral \>\> Deferral Posting)

>   (For retroactive Sales deferrals: Financial \>\> Transactions \>\> Financial
>   \>\> Sales

>   Retroactive \>\> Deferral Posting)

>   (For retroactive Purchasing deferrals: Financial \>\> Transactions \>\>
>   Financial \>\> Purchasing Retroactive \>\> Deferral Posting)

![](media/6c6e2553e60d6256a9e98c1a835accf7.jpg)

1.  Mark the available batches that you want to post.

2.  Choose Post.

#### Voiding a deferral transaction

>   Use the Void Deferral Transactions window to void a posted deferral
>   transaction. Voiding a deferral transaction will post journal entries
>   reversing the original deferral journal entries. Depending on how you set up
>   the option for voiding deferrals, the original transaction associated with
>   the deferrals may also be voided. For more information, see *Setting up
>   revenue/expense deferrals*.

>   **To void a deferral transaction:**

1.  Open the Void Deferral Transactions window.

>   (Financial \>\> Transactions \>\> Financial \>\> Financial Deferral \>\>
>   Void Deferral Transactions)

![](media/115a625698c2026d5da814676536d492.jpg)

1.  Select the series of the transaction you want to void.

2.  Enter or select the customer or vendor for the transaction, and if
    necessary, restrict the number of transactions that appear in the scrolling
    window by entering a range restriction. Choose Redisplay to update the list
    of transactions.

3.  Select the document you want to void and choose Void.

**Chapter 22: Posting**

>   Posting is the process of transferring transactions to the company’s
>   permanent records.

>   This information is divided into the following sections:

-   *Posting overview*

-   *Transaction-level posting*

-   *Posting an individual batch*

-   *Posting batches using the action pane*

-   *Posting to a historical year*

#### Posting overview

>   Posting makes transactions part of your company’s permanent records. Until
>   they’re posted, transactions can be modified, voided, or deleted. Once
>   they’ve been posted, they can’t be altered, though you can enter correcting
>   transactions.

>   You’ll notice the effects of posting on most reports, which display updated
>   amounts every time transactions related to the reports are posted.

>   You can post to the most recent historical year or to any open year in
>   General Ledger. Historical years include years that have been closed using
>   the fiscal yearend closing routine, and also years for which the Historical
>   Year option has been marked in the Fiscal Periods Setup window. See the
>   System Setup instructions (Help \>\> Contents \>\> select Setting Up the
>   System) for more information about using the Fiscal Periods Setup window.

>   Posting to history is valuable if, for example, an audit shows discrepancies
>   in the previous year’s account balance and you must make an adjusting entry.
>   When you post to a historical year, the system updates the account balances
>   in history and adds a record for each line item in each transaction. The
>   beginning balance of the retained earnings account or the beginning balance
>   brought forward account also is adjusted, depending on the type of accounts
>   (profit and loss, or balance sheet) affected. See *Posting to a historical
>   year* for more information.

>   Posting journals are printed when you post a transaction or a batch and
>   provide a record and an audit trail for the transactions. When you close the
>   transaction entry window after posting transactions individually, the
>   posting journal is printed for all transactions that have been posted.
>   Depending on the setup, the posting journal might be printed automatically
>   when you post batches. For more information about posting setup, see the
>   System Setup instructions (Help \>\> Contents \>\> select Setting Up the
>   System).

>   You can use two types of posting: transaction-level posting and batch
>   posting.

#### Transaction-level posting

>   If you use transaction-level posting, you must post each transaction as it
>   is entered. You also can use transaction-level posting for a transaction
>   that is part of a batch in the Transaction Entry window (Transaction \>\>
>   Financial \>\> General) by clearing the Batch ID and choosing Post.

>   Transactions can be posted individually in the Transaction Entry or Clearing
>   Entry windows. Quick journal entries can be posted directly from the Quick
>   Journal Entry window. In either case, the posting date is the same as the
>   transaction date. All transactions posted individually in a single data
>   entry session have the same audit trail code.

>   The individual transaction posting method is useful if a transaction won’t
>   be repeated. For example, you might need to enter an adjusting entry at
>   month’s end to assign revenues or expenses to the period in which they were
>   either earned or incurred. Also, individual transaction entry would be
>   useful if you need to make an adjusting entry to correct a previous error
>   made in recording a transaction.

#### Posting an individual batch

>   Use batch posting to post one batch at a time from the Batch Entry window.
>   With batch posting, you can post batches individually or in groups. You can
>   use these methods in any combination to update your records in a timely and
>   efficient manner. If you are using Workflow, the batch must be approved
>   before you can post the batch. You also can post batches that don’t need
>   approval.

>   *We recommend that you back up company data before posting. If power
>   fluctuates or another problem occurs, you can restore your data and begin
>   the posting process again. For more information about making backups, refer
>   to the System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

>   **To post an individual batch:**

1.  Open the Batch Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> Batches)

![](media/f2bcd17f9cef386fe894a14ac15a74ba.jpg)

1.  Enter or select a batch to be posted.

2.  Choose File \>\> Print or the printer icon button to verify the transactions
    included in the batch with an edit list.

>   *If the Allow Negative Debits and Credits in General Ledger option is marked
>   in the Company Setup Options window, negative transaction amounts or batch
>   totals might be included.*

1.  Check your selections in the Batch Entry window for accuracy, including
    batch requirements and approval options.

2.  Choose Post to post the batch.

#### Posting batches using the action pane

>   You can view, print an edit list, mark, and post one or more batches using
>   the

>   General Ledger Batches list view and the buttons in the action pane. If you
>   are using Workflow, the batch must be approved before you can post the
>   batch. You also can post batches that don’t need approval.

>   **To post batches using the action pane:**

1.  Open the General Ledger Batches list view. From the navigation pane, choose
    the Financial button \>\> General Ledger Batches.

2.  Print an edit list for each batch to post and review the transactions in
    that batch. To print the edit list, in the Reports group, choose \>\> Print
    Edit List.

3.  Review the transactions, make any changes that are necessary and print the
    edit list again to verify them. For more information, see *Chapter 23,
    “Correcting transactions.”*

4.  Save your changes and close the Transaction Entry and Batch Entry windows.

5.  Make a backup of your company’s data. See the System Administrator’s Guide
    (Help \>\> Contents \>\> select System Administration) for information about
    making backups.

6.  In the General Ledger Batches list, mark the batches to post.

7.  Choose to post the selected batches.

8.  Print posting journals and distribution breakdown registers. Using the
    Posting Setup window, you can select posting journals to print according to
    your preferences.

#### Posting to a historical year

>   You can post transactions to the most recent historical year. Historical
>   years include years that have been closed using the fiscal year-end closing
>   routine, and also years for which the Historical Year option has been marked
>   in the Fiscal Periods Setup window. See the System Setup instructions (Help
>   \>\> Contents \>\> select Setting Up the System) for more information about
>   using the Fiscal Periods Setup window.

>   Posting to an historical year is useful if you have to enter audit
>   adjustments after you have closed the year. When you post an adjustment to a
>   closed year, the beginning balances of the affected accounts for the next
>   year are adjusted automatically and you will see both entries on the posting
>   journal.

>   You must have Allow Posting to History marked in the General Ledger Setup
>   window if you want to post to a history year. Also, the period can’t be
>   marked as closed in the Fiscal Period Setup window.

>   For example, assume you have closed fiscal year 2003. In fiscal year 2004,
>   you determine that an adjustment needs to be made to fiscal year 2003. When
>   you post the adjustment with a posting date that falls in fiscal year 2003,
>   you will see two transactions on the posting journal, one to adjust the
>   account activity for the historical year and the other to adjust the
>   beginning balances for the open year. For example, if the transaction
>   affected two balance sheet accounts, the posting journal would look like
>   this:

| **Account**      | **Date** | **Debit** | **Credit** |
|------------------|----------|-----------|------------|
| Accounts Payable | 12/15/03 | 100       |            |
| Cash             | 12/15/03 |           | 100        |
| Accounts Payable | 12/31/03 | 100       |            |
| Cash             | 12/31/03 |           | 100        |

>   If the adjustment affected a balance sheet account and an income statement
>   account, the posting journal would look like this:

| **Account**       | **Date** | **Debit** | **Credit** |
|-------------------|----------|-----------|------------|
| Travel Expense    | 12/15/03 | 100       |            |
| Accounts Payable  | 12/15/03 |           | 100        |
| Retained Earnings | 12/31/03 | 100       |            |
| Accounts Payable  | 12/31/03 |           | 100        |

>   The first transaction adjusts the account balances for the fiscal year 2003.
>   The second transaction adjusts the beginning balance that was set up for
>   fiscal year 2004 when fiscal year 2003 was closed. Thus, you don’t need to
>   close fiscal year 2003 again to roll forward the changes; the beginning
>   balances are updated automatically.

**Chapter 23: Correcting transactions**

>   Transaction errors can and should be corrected to keep your accounting data
>   accurate. The way you correct the error depends on whether or not the
>   transaction has been posted.

>   This information is divided into the following sections:

-   *Correcting an unposted transaction*

-   *Backing out a posted transaction*

-   *Backing out and correcting a posted transaction*

-   *Copying a posted transaction*

#### Correcting an unposted transaction

>   If you’ve entered but haven’t posted an incorrect transaction, the error
>   should appear on the transaction edit list. If the error involves an
>   unbalanced transaction, you’ll receive an alert message that the transaction
>   can’t be posted because it contains unequal debit and credit entries.

>   **To correct an unposted transaction:**

1.  Open the window in which the transaction was originally entered.

>   (Transaction Entry, Clearing Entry, or Quick Journal Entry)

1.  Enter or select the journal entry number assigned to the erroneous
    transaction. This number should be listed on the transaction edit list, next
    to or above (depending on the report layout) the erroneous transaction.

2.  Edit the incorrect information.

3.  To insert a new distribution row, choose Edit \>\> Insert Row. To delete a
    row, select the row to delete and choose Edit \>\> Delete Row.

4.  Choose File \>\> Print or the printer icon button to print a transaction
    edit list to check your work.

5.  Save and post the corrected transaction.

#### Backing out a posted transaction

>   You can use the Transaction Entry window to back out a posted transaction.
>   When you back out a transaction, a new transaction is created, and the
>   debits and credits of the original transaction are reversed when you post
>   the new transaction. Any tax distributions and multidimensional analysis
>   information also will be reversed. The source document code, currency ID,
>   and transaction date are copied from the original transaction.

>   You can back out the following types of posted transactions.

-   Standard

-   Reversing

-   Clearing

-   Quick journal

>   You can back out transactions that were posted during an open year or the
>   most recent historical year.

>   You can’t back out the following types of transactions.

-   Voided transactions

-   Consolidated transactions

-   Transactions that were created during the year-end closing process

-   Transactions that were posted to a historical year

-   Clearing entries that use multiple currencies

-   Clearing entries that use a single currency other than the functional
    currency

-   Transactions that already have been backed out

-   Transactions that were entered to back out a previous transaction

>   When you back out a transaction, you also have the option to create a new,
>   correcting transaction using the debits and credits of the original
>   transaction. See *Backing out and correcting a posted transaction* for more
>   information.

>   You can back out transactions originating in other modules if you marked the
>   Voiding/Correcting of Subsidiary Transactions option in the General Ledger
>   Setup window. You also can back out intercompany transactions if you marked
>   the Back Out of Intercompany Transactions option in the window. See *Setting
>   up default entries and preferences* for more information.

>   **To back out a posted transaction:**

1.  Open the Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> General)

1.  Choose Correct. The Correct Journal Entry window will open.

![](media/4ea1da78bf2addb732cb062f0cd76db5.jpg)

1.  In the Correct Journal Entry window, select the Back Out a Journal Entry
    option.

2.  Select the year that the transaction you’re backing out was posted. Select
    the journal entry number for the transaction.

3.  Choose OK. The Correct Journal Entry window will close and the new
    transaction will appear in the Transaction Entry window. The debits and
    credits from the original transaction will be reversed when you post the new
    transaction.

4.  Choose Post to post the transaction or enter or select a batch ID number and
    choose Save to save the transaction in a batch.

5.  Close the window.

#### Backing out and correcting a posted transaction

>   You can use the Transaction Entry window to back out and correct a posted
>   transaction. When you back out and correct a transaction, a new transaction
>   is created, and the debits and credits of the original transaction are
>   reversed when you post the new transaction. Any tax distributions and
>   multidimensional analysis information also will be reversed. The source
>   document code, currency ID, and transaction date are copied from the
>   original transaction.

>   You also create a new, correcting transaction using the debits and credits
>   of the original transaction. The source document code, tax information,
>   currency ID, transaction date, and multidimensional analysis information
>   also are copied from the original transaction.

>   You can back out the following types of posted transactions.

-   Standard

-   Reversing

-   Clearing

-   Quick journal

>   You can back out transactions that were posted during an open year or the
>   most recent historical year.

>   You can’t back out the following types of transactions.

-   Voided transactions

-   Consolidated transactions

-   Transactions that were created during the year-end closing process

-   Transactions that were posted to a historical year

-   Clearing entries that use multiple currencies

-   Clearing entries that use a single currency other than the functional
    currency

-   Transactions that already have been backed out

-   Transactions that were entered to back out a previous transaction

>   You can back out a transaction without creating a new, correcting
>   transaction. See *Backing out a posted transaction* for more information.

>   You can back out and correct transactions originating in other modules if
>   you marked the Voiding/Correcting of Subsidiary Transactions option in the
>   General Ledger Setup window. You also can back out intercompany transactions
>   if you marked the Back Out of Intercompany Transactions option in the
>   window. See *Setting up default entries and preferences* for more
>   information.

>   **To back out and correct a posted transaction:**

1.  Open the Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> General)

1.  Choose Correct. The Correct Journal Entry window will open.

![](media/68630c4acd8d8359222fca7015731c9b.jpg)

1.  In the Correct Journal Entry window, select the Back Out a Journal Entry and
    Create a Correcting Entry option.

2.  Select the year that the transaction you’re backing out and correcting was
    posted. Select the journal entry number for the transaction.

3.  Choose OK. The Correct Journal Entry window will close, and the new
    transaction will appear in the Transaction Entry window. The debits and
    credits from the original transaction will be reversed when you post the new
    transaction.

4.  Choose Post to post the transaction or enter or select a batch ID number and
    choose Save to save the transaction in a batch.

5.  The correcting transaction will appear in the Transaction Entry window. The
    transaction will include the debits and credits of the original transaction.
    Modify the transaction, as necessary.

6.  Choose Post to post the correcting transaction or enter or select a batch ID
    number and choose Save to save the transaction in a batch.

7.  Close the window.

#### Copying a posted transaction

>   You can use the Transaction Entry window to copy a posted transaction. When
>   you copy a transaction, you use the debits and credits of the original
>   transaction to create a new transaction. The source document code, tax
>   information, currency ID, transaction date, and multidimensional analysis
>   information also are copied from the original transaction.

>   You can copy the following types of posted transactions.

-   Standard

-   Reversing

-   Clearing

-   Quick journal

>   You can copy transactions that were posted during an open year or the most
>   recent historical year.

>   You can’t copy the following types of transactions.

-   Voided transactions

-   Consolidated transactions

-   Transactions that were created during the year-end closing process

-   Transactions that were posted to a historical year

-   Clearing entries that use multiple currencies

-   Clearing entries that use a single currency other than the functional
    currency

>   **To copy a posted transaction:**

1.  Open the Transaction Entry window.

>   (Financial \>\> Transactions \>\> Financial \>\> General)

1.  Choose Copy. The Copy Journal Entry window will open.

![](media/a6ad2e6edd3916467aa7a2108df12235.jpg)

1.  In the Copy Journal Entry window, select the year that the transaction
    you’re copying was posted.

2.  Select the journal entry number for the transaction that you’re copying.

3.  Choose OK. The Copy Journal Entry window will close. The new transaction
    will appear in the Transaction Entry window. The transaction will include
    the debits and credits of the original transaction. Modify the transaction,
    as necessary.

4.  Choose Post to post the transaction or enter or select a batch ID number and
    choose Save to save the transaction in a batch.

5.  Close the window.

**Chapter 24: Matching transactions**

>   Transaction matching is the process of linking related transaction
>   distributions from different journal entries. For example, you can link
>   period-end adjusting entries to the original transactions or link a set of
>   transactions associated with a project.

>   After you have created links, you can also create groups of linked
>   transaction distributions. For example, you could create a group of the
>   links for period-end adjustments to aid in the audit process.

>   This information includes the following sections:

-   *Linking transaction distributions*

-   *Modifying transaction distribution links*

-   *Creating a matched transaction group*

#### Linking transaction distributions

>   Use the General Ledger Transaction Link Maintenance window to link
>   distributions from multiple posted transactions. Depending on how you set up
>   transaction matching, you can link distributions to a single account or
>   multiple accounts. Also, linked distributions may be required to balance
>   (that is, total debits must equal total credits) before the link can be
>   saved. For more information about transaction matching setup options, see
>   *Setting up transaction matching*.

>   **To link transaction distributions:**

1.  Open the General Ledger Transaction Link Maintenance window.

>   (Financial \>\> Transactions \>\> Financial \>\> Transaction Matching)

![](media/657a8a2eeab7ffe1a7f8b663f621d6ea.jpg)

1.  Enter a description for the distributions you want to link. For example, if
    you’re linking some month-end adjusting entries to the original
    transactions, you could enter “January adjusting entries.”

2.  Accept the default link date or enter the date you want to use for this
    link. The date you enter will be used to determine whether to archive a
    link. For more information, see *Archiving matched transactions*.

3.  Enter or select an account that has distributions you want to include in
    this link, then select the year for the transactions you want to include.
    All transactions posted to this account and year will appear in the
    scrolling window.

4.  If necessary, enter range restrictions to reduce the number of transactions
    displayed and choose Redisplay.

>   You can also choose whether to display debit or credit distributions or
>   both, and whether to display only those distributions that have not
>   previously been included in other links.

1.  Mark the link option for each distribution you want to include. As you mark
    distributions, the difference (that is, the debit or credit balance) and the
    number of distributions included will be updated.

>   If you want to include distributions to a different account, enter that
>   account and any range restrictions. The transactions posted to that account
>   will appear, and you can mark the distributions.

1.  Choose Save to save the link.

#### Modifying transaction distribution links

Use the General Ledger Transaction Link Maintenance window to modify transaction
distribution links. You can link additional distributions or remove distribution
links. Depending on how you set up transaction matching you can add links to
distributions to additional accounts.

>   **To modify transaction distribution links:**

1.  Open the General Ledger Transaction Link Maintenance window.

>   (Financial \>\> Transactions \>\> Financial \>\> Transaction Matching)

1.  Enter or select the link number you want to modify.

2.  Make the necessary changes and choose Save.

#### Creating a matched transaction group

Use the Transaction Matching Group Maintenance window to create and modify
groups of transaction distribution links. For example, you could create a group
of the links of month-end adjusting entries.

>   **To create a matched transaction group:**

1.  Open the Transaction Matching Group Maintenance window.

>   (Financial \>\> Transactions \>\> Financial \>\> Transaction Matching
>   Groups)

![](media/2a6c6902927f3b60dd99e9d7302a69c1.jpg)

1.  Enter a name for the group. A message will appear asking if you want to
    create this group. Choose Yes.

2.  Mark the links you want to include in this group. You can include links that
    have been included in other groups, as well as archived links.

3.  Choose Save.

**Part 4: Inquiries**

>   You can use inquiries to display and analyze account and transaction
>   information.

>   In General Ledger, you can use inquiries to quickly view both current and
>   historical account, budget, and transaction information. You can review
>   information in summary or detailed form, with the option of printing the
>   information in the window by choosing File \>\> Print.

>   The following information is discussed:

-   *Chapter 25, “Account inquiries,”* describes how to view account activity
    for open or historical years.

-   *Chapter 26, “Transaction inquiries,”* describes how to view posted
    transactions for open periods or historical years.

-   *Chapter 27, “Transaction matching inquiries,”* describes how to view
    information about linked transaction distributions.

-   *Chapter 28, “Budget inquiries,”* describes how to view budget summary
    information so you can compare budget amounts to actual amounts for a
    selected account and budget.

-   *Chapter 29, “Account rollup inquiries,”* describes how to use account
    rollup inquiries to create segment-based inquiries for any range of account
    segments.

**Chapter 25: Account inquiries**

>   You can view account activity for open or historical years. In addition, you
>   can analyze net changes to accounts for open periods.

>   This information is divided into the following sections:

-   *Viewing multiple currencies*

-   *About reporting currency*

-   *Viewing a summarized account balance for an open fiscal year*

-   *Viewing a summarized account balance for a historical year*

-   *Viewing changes to an account balance*

#### Viewing multiple currencies

>   If you are using Multicurrency Management, you can choose whether to view
>   multicurrency amounts in the originating, functional, or reporting currency.
>   Choose View \>\> Currency \>\> Functional, Originating, or Reporting in an
>   inquiry window. The option will be saved on a per user, per window basis.

>   You also can use the currency list button in windows that support changing
>   the currency view. The View menu and currency list button are available in
>   the following inquiry windows:

-   Summary Inquiry

-   Detail Inquiry

-   Journal Entry Inquiry

-   History Summary Inquiry

-   History Detail Inquiry

>   *The originating currency view isn’t available in the Summary Inquiry window
>   or History Summary Inquiry window because the amounts might be for multiple
>   currencies.*

>   The first time you open each of these windows after registering
>   Multicurrency Management, all the transactions will be displayed in the
>   originating currency. If you change the currency view, it will be the
>   default view the next time you open that window.

#### About reporting currency

>   A reporting currency is used to convert functional or originating currency
>   amounts to another currency on inquiries and reports. For example, if the
>   U.S. dollar is the functional currency for a company, you can set up the
>   euro as your reporting currency to view an inquiry window with currency
>   amounts displayed in the euro currency.

>   When you set up the reporting currency in Multicurrency Management, you
>   enter a default exchange rate and rate calculation method. Depending on how
>   your system is set up, you might be able to override the default reporting
>   currency exchange rate or rate calculation method on inquiries and reports.
>   To change the default reporting currency exchange rate, choose View \>\>
>   Currency \>\> Modify Reporting Rate to open the Modify Reporting Rate
>   window.

>   For more information about the reporting currency, see the Multicurrency
>   Management documentation.

#### Viewing a summarized account balance for an open fiscal year

>   Use the Summary Inquiry window to view account balances in a net change and
>   period balance format. The window also displays the account total (the sum
>   of the beginning balance and all period balances).

>   The Summary Inquiry window can be helpful if you want to verify the amounts
>   for an open year. To do so, print a detailed trial balance and compare the
>   detail on the report with the summary amount displayed in this window. If
>   the amounts differ, you should reconcile the year. During the reconcile
>   process, the summary balance will be adjusted to match the transaction
>   detail. For more information about reconciling, see *Reconciling financial
>   data*.

>   **To view a summarized account balance for an open fiscal year:**

1.  Open the Summary Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Summary)

![](media/aa37f8aeec90cb59eb7f306e43d2ae5b.jpg)

1.  Enter or select an account.

2.  Enter or select a year.

>   *You can click the Account field link to open the Account Maintenance
>   window, where you can view account details. You can click the Debit, Credit,
>   Net Change, or Period Balance field links to open the Detail Inquiry window
>   to view transactions posted to specific accounts in open fiscal years.*

1.  You can choose Currency to open the Multicurrency Summary Inquiry window,
    where you can view summarized account balances and multicurrency
    information.

2.  You can print a Summary Inquiry Report by choosing File \>\> Print or the
    printer icon button while the information you'd like to print is displayed.

#### Viewing a summarized account balance for a historical year

>   Use the History Summary Inquiry window to view summarized account balances
>   in a net change and period-by-period format for a historical fiscal year.
>   This window is similar to the Summary Inquiry window, except that it shows
>   historical amounts.

>   To verify the amounts for a historical year, print a detailed historical
>   trial balance and compare the detail on the report with the summary amount
>   displayed in this window. If the amounts differ, you should reconcile the
>   year. During the reconcile process, the summary balance will be adjusted to
>   match the transaction detail. For more information about reconciling, see
>   *Reconciling financial data*.

>   **To view a summarized account balance for a historical year:**

1.  Open the History Summary Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> History Summary)

![](media/f07fa33b87a11bd953d103ba78e917ff.jpg)

1.  Enter or select an account, then select a year.

>   Period-by-period balances for the specified year will be displayed, along
>   with the beginning balance of the account, debits, credits, net change, and
>   the totals of each category for each period.

>   *You can click the Account link to open the Account Maintenance window,
>   where you can view account details. You can highlight a period and click the
>   Debit, Credit, Net Change, or Period Balance link to open the History Detail
>   Inquiry window, where you can view transactions posted to specific accounts
>   in historical years. You also can choose the Currency button to open the
>   Multicurrency Summary Inquiry window, where you can view summarized account
>   balances and multicurrency information.*

1.  You can print a Summary Inquiry Report from this window by choosing File
    \>\> Print or the printer icon button while the information you'd like to
    print is displayed.

#### Viewing changes to an account balance

>   Use the Net Change Inquiry window to view changes for a selected year—the
>   debit and credit amounts and overall net change—to the balance of a selected
>   account. This window displays the description, beginning balance, total
>   debits and credits, net change, and ending balance for the selected account.

>   **To view changes to an account balance:**

1.  Open the Net Change Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Net Change)

![](media/c366750849fea73a40ad7a365fc196f0.jpg)

1.  Enter or select an account.

2.  Enter or select a year.

3.  When you’ve finished viewing information, close the window.

**Chapter 26: Transaction inquiries**

>   You can view posted transactions for open periods or historical years using
>   transaction inquiries. You can also view information about deferral
>   transactions.

>   This information is divided into the following sections:

-   *Viewing budget transaction and history summary information*

-   *Viewing transactions posted to an open year*

-   *Viewing transactions posted to a specific account in a historical year*

-   *Viewing posted transactions during an open fiscal year*

-   *Viewing deferral transactions*

#### Viewing budget transaction and history summary information

>   Use the Budget Transaction Inquiry window to view balances and budget
>   amounts or net change for open or historical periods. This information can
>   be used to compare actual account activity with budgeted amounts.

>   The Budget Transaction Inquiry window is useful if you’re interested in
>   viewing budget figures, but don’t want to change any calculations.

>   Use the Budget Summary History window to view period balances, net change,
>   and total amounts for an account and budget ID. This information can be used
>   to view the history of budget transactions for a particular account over
>   multiple periods.

>   **To view budget transaction summary information:**

1.  Open the Budget Transaction Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Budget Journal Entry Inquiry)

![](media/ecfaa65ab995631a4457919d34ce9c0b.jpg)

1.  Select budget journal entry.

2.  Enter or select an account.

3.  Choose how you want to display the budget information: Net Change or Period
    Balances.

4.  When you’ve finished viewing information, click OK to close the window.

>   **To view budget history summary information:**

1.  Open the Budget Summary Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Budget Summary)

![](media/3d774405caeb0b32d3f17adbc0620028.jpg)

1.  Enter or select an account.

2.  Enter or select a budget ID.

3.  Choose how you want to display the budget history information: Net Change or
    Period Balances.

4.  Choose how you want to sort the results: by alias, description, account
    type, category, account, or main segment.

5.  To return all fields to their default values and remain working in the
    window, click Clear.

#### Viewing transactions posted to an open year

>   Use the Journal Entry Inquiry window to view transaction detail for General
>   Ledger posted journal entries in an open fiscal year.

>   Multiple journal entries with the same number might exist if a recurring
>   transaction is posted or a reversing transaction is posted. If you enter a
>   journal entry for which multiple entries exist, the journal entry with the
>   oldest posting date in the open year is displayed. If you use the Journal
>   Entry lookup button, all unique journal entries are displayed, and you can
>   select the journal entry you’d like to view.

>   *The Intercompany button is enabled only if the currently displayed journal
>   entry originated from an intercompany transaction.*

>   The Journal Entry Inquiry window displays posted journal entries in any open
>   year in General Ledger, so you don’t need to keep transaction history to be
>   able to view journal entries in this window.

>   **To view transactions posted to an open year:**

1.  Open the Journal Entry Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Journal Entry Inquiry)

![](media/bb94d8422687c596ebadb0644f2077c9.jpg)

1.  Enter or select the journal entry number. You can view any posted journal
    entry number, as long as the journal entry has not been moved to history.
    Audit trail code, transaction date, source document, batch ID, reference,
    currency ID, account, debit, credit, distribution reference, and difference
    information are displayed.

>   You also can click the Source Document link to open a window containing
>   detailed information about the journal entry if it originated in a module
>   other than General Ledger.

1.  You can print a Journal Inquiry Report by choosing File \>\> Print or the
    printer icon button while the information you’d like to print is displayed.

2.  When you’ve finished viewing the information, close the window.

#### Viewing transactions posted to a specific account in a historical year

>   Use the History Detail Inquiry window to view the transactions posted to
>   specific accounts in historical years. You also can limit the detail that is
>   displayed, by setting a range of dates, source documents, or currency IDs.
>   Each transaction’s date, journal entry number, audit trail code, source
>   document, reference, currency ID, and debit or credit is displayed.

>   **To view transactions posted to a specific account in a historical year:**

1.  Open the History Detail Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> History Detail)

![](media/d707a058d243b408dca055db1638df48.jpg)

1.  Enter or select an account.

2.  Select a year.

3.  Enter ranges of dates, source documents, and currency IDs that will appear
    in the window, and choose Redisplay.

>   *You can highlight a journal entry and click the Journal Entry link to open
>   the Transaction Entry Zoom window, where you can view information about a
>   posted or historical transaction. You also can click the Currency ID link
>   for a journal entry not entered in the functional currency, to open the
>   Financial Exchange Rate Entry Zoom window, where you can view currencies,
>   exchange rates, and originating and functional currency amounts for posted
>   multicurrency transactions.*

1.  You can print a History Detail Inquiry Report by choosing File \>\> Print or
    the printer icon button while the information you’d like to print is
    displayed.

2.  When you’ve finished viewing information, close the window.

#### Viewing posted transactions during an open fiscal year

>   Use the Detail Inquiry window to display detailed information about
>   transactions posted during an open fiscal year. When you select an account,
>   transactions for the account are displayed. You also can limit the detail by
>   setting a range of dates, source documents, or currency IDs. Each
>   transaction’s date, journal entry number, audit trail code, source document,
>   reference, and debit or credit is displayed.

>   For example, you might use the Detail Inquiry window if you suspect an error
>   on the summary trial balance. If the account in question, the Cash account,
>   shows a \$5,000 balance, display the Cash account in this window. The
>   amounts displayed here for an open period should match the total on the
>   summary trial balance.

>   **To view posted transactions during an open fiscal year:**

1.  Open the Detail Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Detail)

![](media/546c00dc22f88e302a84672457cedff4.jpg)

1.  Enter or select an account.

2.  Select a year.

3.  Enter ranges of dates, source documents, and currency IDs that will appear
    in the window, and choose Redisplay.

>   *You can select a journal entry and click the Journal Entry link to open the
>   Transaction Entry Zoom window, where you can view information about a posted
>   or historical transaction. You also can click the Currency ID link for a
>   journal entry not entered in the functional currency to open the Financial
>   Exchange Rate Entry Zoom window, where you can view currencies, exchange
>   rates, and originating and functional currency amounts for posted
>   multicurrency transactions.*

1.  You can print a Detail Inquiry Report by choosing File \>\> Print or the
    printer icon button while the information you’d like to print is displayed.

2.  When you’ve finished viewing information, close the window.

#### Viewing deferral transactions

>   Use the Deferral Inquiry window to view the deferral transactions for a
>   selected module.

>   **To view deferral transactions:**

1.  Open the Deferral Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Deferral)

![](media/b818e5625c70668443f1fa946161b783.jpg)

1.  Using the list at the bottom of the window, select the module you want to
    view deferral transactions for.

2.  If necessary, enter a range to restrict the number of transactions that
    appear in the window, then choose Redisplay.

3.  To view more information about a specific deferral, select the transaction
    and click on the Document Number link to open the Deferral Inquiry Zoom
    window.

**Chapter 27: Transaction matching inquiries**

>   You can view and print information about linked transactions, including
>   specific links, all the links for a specific account, or the links in a
>   transaction matching group.

>   This information includes the following sections:

-   *Viewing transaction distribution links by number*

-   *Viewing transaction distribution links by account*

-   *Viewing matched transactions by group*

#### Viewing transaction distribution links by number

>   Use the Transaction Matching by Link Number Inquiry window to view detailed
>   information about an individual transaction distribution link record.

>   **To view transaction distribution links by number:**

1.  Open the Transaction Matching by Link Number Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Transaction Match by Link
>   Number)

![](media/e280f825e3f413e68c79f85d68f57d8c.jpg)

1.  Enter or select the link number you want to view.

2.  To view more information about a specific distribution, highlight the record
    and click on the Jrnl No. link to open the Transaction Entry Zoom window.

>   If the link is a member of one or more matched transaction groups, you can
>   view more information about the group by selecting the group and clicking on
>   the Group link to open the Transaction Matching Group Inquiry window.

1.  You can choose the Print button to print the Transaction Matching by Link
    Number report for the information displayed in the inquiry window.

#### Viewing transaction distribution links by account

>   Use the Transaction Matching by Account Inquiry window to view the
>   transaction distributions for an account that have been linked with other
>   distributions.

>   **To view transaction distribution links by account:**

1.  Open the Transaction Matching by Account Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Transaction Match by Account)

![](media/3350a2e79ff89c8343cd91422bb34d5a.jpg)

1.  Enter or select the account you want to view link information for, then
    choose the year for the transaction distributions you want to view.

2.  Indicate whether you want to view only linked or unlinked distributions, or
    all distributions.

3.  Indicate whether you want to view saved links or archived links.

4.  Indicate whether you want to view all links, or links in a particular
    transaction matching group.

5.  To view more information about the journal entry, link, or currency for a
    distribution, highlight the record and click the link for the information
    you want to view.

>   You can use the following windows to view additional information:

| **Link**    | **Window that opens**              |
|-------------|------------------------------------|
| Journal No. | Transaction Entry Zoom             |
| Link        | Distribution Links Inquiry Zoom    |
| Currency ID | Financial Exchange Rate Entry Zoom |

1.  You can choose the Print button to print the Transaction Matching by Account
    Number report for the information displayed in the inquiry window.

#### Viewing matched transactions by group

>   Use the Transaction Matching Group Inquiry window to view the transaction
>   distribution links that have been assigned to a group.

>   **To view matched transactions by group:**

1.  Open the Transaction Matching Group Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Transaction Matching Groups)

![](media/eae1ff9e4a568d0c2bcd0c141e334729.jpg)

1.  Enter or select the group you want to view.

2.  To view more information about a particular link, highlight the link in the
    scrolling window and click the Link Number link to open the Transaction
    Matching by Link Number Inquiry window.

**Chapter 28: Budget inquiries**

>   You can use budget inquiries to view budget summary information and to
>   compare budget amounts to actual amounts for a selected account and budget.

>   This information is divided into the following sections:

-   *Viewing budget summary information*

-   *Viewing budgeted versus actual expenditures*

#### Viewing budget summary information

>   Use the Budget Summary Inquiry window to view balances and budget amounts or
>   net change for open or historical periods. This information can be used to
>   compare actual account activity with budgeted amounts.

>   The Budget Summary Inquiry window is useful if you’re interested in viewing
>   budget figures, but don’t want to change any calculations.

>   **To view budget summary information:**

1.  Open the Budget Summary Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Budget Summary)

![](media/44b5cbf100972db5e73c69a7a22bc3b2.jpg)

1.  Enter or select an account.

2.  Enter or select a budget ID.

3.  Choose how you want to display the budget information: Net Change or Period
    Balances.

>   *You can select a period and click the Account link to open the Account
>   Maintenance window, where you can view detailed account information.*

1.  When you’ve finished viewing information, close the window.

#### Viewing budgeted versus actual expenditures

>   Use the Budget vs Actual Inquiry window to view budget and actual amounts or
>   net change for a particular account and budget ID by period. You can also
>   view the variance and variance percentage, so you can analyze how closely
>   your actual amounts match the budgeted amounts for the selected account.

>   **To view budgeted versus actual expenditures:**

1.  Open the Budget vs Actual Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Budget vs. Actual)

![](media/57879175e9656f99164d4c340be1c590.jpg)

1.  Enter or select an account.

2.  Enter or select a budget ID.

3.  Choose how to display the budget information: Net Change or Period Balances.

>   *You can highlight a period and click the Actual link to open the Detail
>   Inquiry window, where you can see all transactions in the period.*

1.  You can print a Budget vs Actual Inquiry Report by choosing File \>\> Print
    or the printer icon button while the information you'd like to print is
    displayed.

2.  When you’ve finished viewing information, close the window.

**Chapter 29: Account rollup inquiries**

>   You can create segment-based inquiries for any range of account segments
>   within General Ledger.

>   This information includes the following sections:

-   *Account rollup inquiry overview*

-   *Creating an account rollup inquiry option*

-   *Setting up a calculated column*

-   *Modifying an account rollup inquiry option*

-   *Viewing an account rollup inquiry*

#### Account rollup inquiry overview

>   The Account Rollup Inquiry window displays summarized period balances for
>   ranges of accounts. You create account rollup inquiry options to define
>   these account ranges by selecting segment ranges that include the
>   information you want to summarize. For example, assume your chart of
>   accounts is set up with four segments: Division, Department, Account, and
>   Sub-Account. You could create an account rollup inquiry option to summarize
>   travel expenses for a group of departments across several divisions. Or you
>   could summarize the cost of goods sold accounts for the sales department of
>   a single division, or of all divisions.

>   You can set up an account rollup inquiry option that includes multiple
>   ranges for each segment. For example, you could create an option that
>   included information for departments 100, 200, 400, and 700, and accounts
>   1000 through 1400, and 2700 through 2900.

>   The Account Rollup Inquiry window can display up to four columns of
>   information. You can set up an option to display actual amounts (in the
>   reporting currency), previous year balances, other currency balances, and
>   budget amounts. You can also display columns that show the results of simple
>   calculations; for example, the difference between actual amounts and
>   budgeted amounts.

>   For information about setting up inquiry options, see *Creating an account
>   rollup inquiry option*. For information about calculated columns, see
>   *Setting up a calculated column*.

#### Creating an account rollup inquiry option

>   Use the Account Rollup Inquiry Options window to define the segment ranges
>   and types of information you want to view in the Account Rollup Inquiry
>   window.

>   **To create an account rollup inquiry option:**

1.  Open the Account Rollup Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Account Rollup)

1.  Choose Modify to open the Account Rollup Inquiry Options window.

![](media/2065f5b31d477da34fe31c2624738918.jpg)

1.  Enter a name for the option you are creating.

2.  Select the segment you want to use to sort the information. The selection
    you make here will control how the information is sorted in the Account
    Rollup Detail Inquiry Zoom window.

3.  Select the number of columns of information you want to display.

4.  For each column of information, enter the column heading you want to use,
    and the type of information you want to display. If you selected Budget or
    Other Currency for the type, enter or select the budget or currency you want
    to display. If you selected the type Calculated, choose the Selection lookup
    button to open the Account Rollup Inquiry Calculated Column window. For more
    information, see *Setting up a calculated column*.

>   *A calculated column must follow the columns it is performing its operations
>   on. For example, assume you set up an inquiry option with column 1 as
>   Actual, column 2 as Budget, column 3 as Calculated, and column 4 as Previous
>   Year. In this case, the calculated column could not include the previous
>   year amounts in its calculations because it is listed after the calculated
>   column.*

1.  Enter restrictions to define the segment ranges you want to create this
    inquiry option for. You can set up multiple ranges for a single segment.

2.  Choose Save to save the account rollup inquiry option.

#### Setting up a calculated column

>   Use the Account Rollup Inquiry Calculated Column window to create a
>   mathematical formula for an account rollup inquiry option that displays the
>   results of simple calculations. For example, if you create an inquiry option
>   that displays the actual expenses of a department and the budgeted expenses,
>   you can create a formula to calculate the difference between the actual
>   amounts and the budget.

>   *A calculated column must follow the columns it is performing its operations
>   on. For example, assume you set up an inquiry option with column 1 as
>   Actual, column 2 as Budget, column 3 as Calculated, and column 4 as Previous
>   Year. In this case, the calculated column could not include the previous
>   year amounts in its calculations because it is listed after the calculated
>   column.*

>   **To set up a calculated column:**

1.  In the Account Rollup Inquiry Options window, select the type Calculated for
    one of the columns, and click the Selection lookup button. The Account
    Rollup Inquiry Calculated Column window appears.

![](media/dd27faf5600a9d28fe34d22b811c7aee.jpg)

1.  Enter the columns, constants, and operators for the calculation you want to
    create.

>   For example, to calculate the difference between column 1, Actuals, and
>   column 2, Previous Year, select the Actuals column from the list and click
>   the Column button. Then click the - operator button. Then choose Previous
>   from the list and click the Column button again. As you create the
>   calculation, the expression is displayed in the window: in this case, C1 -
>   C2.

>   You can create more complex expressions, such as the difference between two
>   columns as a percentage. This would be ((C1 - C2)/C1)\*100.

1.  Choose OK to save the expression and close the window.

#### Modifying an account rollup inquiry option

>   Use the Account Rollup Inquiry Options window to modify a saved account
>   rollup inquiry option. You can change the sorting order, add or remove
>   columns of information, change the formula for a calculated column, and add
>   or remove segment restrictions.

>   **To modify an account rollup inquiry option:**

1.  Open the Account Rollup Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Account Rollup)

1.  Choose Modify to open the Account Rollup Inquiry Options window.

2.  Enter or select the option you want to change.

3.  Make the necessary changes to the option.

>   To change the formula for a calculated column, click in the row for that
>   column and click the Selection lookup button.

1.  Choose Save to save the account rollup inquiry option.

#### Viewing an account rollup inquiry

>   Use the Account Rollup Inquiry window to view segment-based inquiries using
>   options you created in the Account Rollup Inquiry Options window. You can
>   view for open or historical years.

>   **To view an account rollup inquiry:**

1.  Open the Account Rollup Inquiry window.

>   (Financial \>\> Inquiry \>\> Financial \>\> Account Rollup)

![](media/0f027d9b43a1e2a911bbddbb8b7abdfa.jpg)

1.  Enter or select an option. (For information on creating options, see
    *Creating an account rollup inquiry option*.)

2.  Select the year you want to view and indicate whether you want to view the
    net change for each period, or period balances.

3.  Choose Redisplay to display the information. To print a report of the
    information displayed in the Account Rollup Inquiry window, choose File \>\>
    Print.

4.  To view detailed information about the amounts shown for each period, select
    a period and click on one of the column heading links to open the Account
    Rollup Detail Inquiry Zoom window.

**Part 5: Reports**

>   You can analyze transaction and account information and display the
>   information on the computer screen or on a printed report. You also can save
>   it to a file.

>   The following information is discussed:

-   *Chapter 30, “Financial statement reports,”* describes financial statements,
    the summarized outcome of all the steps in the accounting cycle.

-   *Chapter 31, “General Ledger reports,”* shows how to use reports to analyze
    account activity and identify errors in transaction entry.

**Chapter 30: Financial statement reports**

>   General Ledger financial statements help you analyze your business activity.
>   Financial statements are the summarized outcome of all the steps in the
>   accounting cycle. You can use financial statements to gain a better
>   understanding of your company's financial position.

>   This information is divided into the following sections:

-   *Understanding financial statements*

-   *Types of financial statements*

-   *Setting up a quick financial statement*

-   *Printing financial statements*

#### Understanding financial statements 

>   In any business, the accounting cycle consists of processes for recording,
>   summarizing, reporting, and analyzing financial information. However, the
>   ultimate purpose of all these activities is to generate the financial
>   statements. You can think of the financial statements printed in General
>   Ledger as the summarized outcome of all the steps in the accounting cycle
>   and use the information to gain a better understanding of your company’s
>   financial position.

>   There are several ways to print financial statements:

-   You can set up financial statements in the Quick Financial Setup window. In
    this window, you can quickly set up a basic financial statement and choose
    which columns to include in the financial statement. After you save the
    statement, you can print it using the Financial Statement Report Options
    window.

-   You can create an unlimited number of financial statement layouts using
    Advanced Financial Analysis. For information on creating and modifying
    financial statements using Advanced Financial Analysis, refer to the
    Advanced Financial Analysis documentation.

-   You can use Management Reporter for Microsoft Dynamics ERP to print
    financial statements. For more information about printing financial
    statements using Management Reporter, refer to the Management Reporter
    documentation.

If you’re keeping history, you can use Microsoft Dynamics GP reporting
capabilities to compare open- and historical-year figures. You also can print
financial statements for any open-year period or historical-year period.

>   *Until the year-end close is completed for General Ledger, you won’t get
>   accurate financial statements for the new year. Beginning balances for the
>   new year are not created until the year-end close process is completed.
>   Therefore, the financial statements for the new year will reflect only
>   current year activity until the year-end closing process is completed. This
>   applies to both Advanced Financial Analysis and Management Reporter.*

#### Types of financial statements

>   You can define and print four types of financial statements:

**Balance Sheet** The Balance Sheet reflects the solvency and financial position
of your company at a specific point in time, listing the assets, and liabilities
of your company. This statement shows your company’s ability to pay its debts as
they become due.

**Profit and Loss Statement** A Profit and Loss Statement includes your
company’s revenues and expenses, reflecting the profitability of your company
for a specific time period, such as a month or a year.

**Statement of Cash Flows** The Statement of Cash Flows provides information
about your company’s cash receipts and cash payments over a specified period of
time. You also can determine the amount of cash your company has available at
any given time.

>   *The indirect method is used for calculating and printing the Statement of
>   Cash Flows. This method calculates the amount of net cash flow from
>   operating activities by reconciling net income to net cash flow.*

**Statement of Retained Earnings** The Statement of Retained Earnings shows the
items causing changes to your retained earnings, including net income and
declared dividends, for a stated period of time.

Each financial statement includes a number of required columns, which will
appear in the Selected Columns list. In addition to these required columns, you
can insert optional columns for each financial statement. On the Profit and Loss
Statement, Statement of Retained Earnings, and Statement of Cash Flows, you can
use a total of six required and optional columns. On the Balance Sheet, you can
use a total of five columns.

The rows in the financial statement are defined automatically, using General
Ledger’s account categories to group the accounts on the statements.
*Understanding account categories* shows the account categories provided with
General Ledger, their account type, and which financial statements will contain
each of the account categories.

#### Setting up a quick financial statement

Use the Quick Financial Setup window to define the layout for financial
statements. Unlike other Microsoft Dynamics GP reports, financial statements
must be set up before you can print them.

>   Each financial statement includes a number of required columns, which will
>   appear in the Selected Columns list. In addition to these required columns,
>   you can insert optional columns for each financial statement. On the Profit
>   and Loss Statement, Statement of Retained Earnings, and Statement of Cash
>   Flows, you can use a total of six required and optional columns. On the
>   Balance Sheet, you can use a total of five columns.

>   The rows in the financial statement are defined automatically, using General
>   Ledger’s account categories to group the accounts on the statements.
>   *Understanding account categories* shows the account categories provided
>   with General Ledger, their account type, and which financial statements will
>   contain each of the account categories.

>   *If you create a new financial statement using Advanced Financial Analysis,
>   you can’t use the new financial statement with Quick Financials.*

>   You can use the Advanced Financial Report Layout window to customize the
>   financial statements provided with Microsoft Dynamics GP. For example, you
>   can add report columns, rows, and headers to these statements for reporting
>   detailed financial information specific to your business.

>   *If you modify an existing quick financial statement and close the window,
>   an alert message will appear and ask if you want to save your changes. If
>   you choose Delete, the entire financial statement will be deleted.*

>   **To set up a quick financial statement:**

1.  Open the Quick Financial Setup window.

>   (Financial \>\> Reports \>\> Financial \>\> Quick Financial)

![](media/a2bea8634cc8708bc9ddc9b2cb31e81b.jpg)

1.  Enter or select a financial statement name and select a statement type.

>   If you’re defining the layout for a Balance Sheet, Statement of Cash Flows,
>   or Statement of Retained Earnings, identify the Profit and Loss account that
>   will provide the net income or net loss source amount for the statement.

1.  You can select additional columns from the Optional Columns list to include
    on the financial statement. Select an additional column and choose Insert to
    add it to the Selected Columns list. You can have up to six columns for a
    profit and loss statement, and up to five columns for a balance sheet.

2.  Choose Insert to insert the additional columns into the Selected Columns
    list.

>   *You can add optional columns only below a required column; you can’t insert
>   an optional column between two other optional columns or at the top of the
>   list. However, if you’re using Advanced Financial Analysis, you can add
>   report columns later or move columns to new locations.*

>   To remove a column from the layout, highlight it and choose Remove. You can
>   remove only optional columns from the layout.

1.  Enter a budget ID if you've included either a year-to-date budget column or
    current budget column on the financial statement.

2.  Enter or select an open year and a historical year if you’ve included a
    column for History YTD or History Currency on the financial statement.

>   *To use more than one budget on a report or more than one year on a history
>   column, use the Advanced Financial Report Layout window to add more
>   information for reporting detailed financial information specific to your
>   business.*

1.  Choose Save.

#### Printing financial statements

Use the Financial Statement Report window to print financial statements. Before
printing a financial statement, you must create a report option.

>   *If you’re printing a Statement of Retained Earnings and want to enter a
>   prior period adjustment, enter a description and amount for the adjustment
>   using the Prior Period Adjustments window (Financial \>\> Reports \>\>
>   Financial \>\> Prior Period Adjustments). The description and amount of the
>   adjustment that you enter will appear as an adjustment to the beginning
>   balance of the Retained Earnings account when you print the statement.*

>   **To print a financial statement:**

1.  Open the Financial Statement Report window.

>   (Financial \>\> Reports \>\> Financial \>\> Financial Statements)

1.  Choose the report you want to print and choose New to open the Financial
    Statement Report Options window and to create a new report option.

![](media/f6b501e9a5488093d0529ed9981c3992.jpg)

1.  Enter a name for the report option.

2.  Choose the level of detail to print for the amounts. If you choose Detail
    with Rollups, Summary, or Summary with Rollups, select whether you want the
    first account description or the account category description to print for
    the rows.

3.  Mark to include unit accounts and accounts with zero balances.

>   If you are updating the accelerator file and want to use this updated
>   information when printing this financial statement, mark the Use Accelerator
>   option.

1.  Select or enter a segment ID to print a financial statement for a range of
    account segments. For example, you can print a financial statement for
    departments 100 to 400 by entering a restriction on the segment that
    represents the department.

>   If you select a segment ID, you can choose to print an individual report for
>   each segment within the range you define. If this box is not marked, a
>   single report will be printed that includes all accounts in the selected
>   range.

>   If you have columns in the financial statement that contain user-defined
>   calculations, you can choose to base the calculation on all accounts in the
>   defined range or on the amounts on the individual reports. For more
>   information, see the Advanced Financial Analysis documentation.

1.  If you want to modify a column on the financial statement, choose Adjust to
    open the Temporary Financial Column Adjustment window. Changes made in this
    window will be removed when you close the Financial Statement Report window.
    If you want to make a permanent change to the financial statement, use the
    Advanced Financial Report Layout window. For more information, see the
    Advanced Financial Analysis documentation.

>   Choose Revert if you made a temporary column adjustment and want to remove
>   it before printing.

1.  Choose Destination to select a printing destination. Reports can be printed
    to the screen, to the printer, to a file, or to any combination of these
    options. If you select Ask Each Time, you can select printing options each
    time you print this report option.

2.  To print the report option from the report options window, choose Print
    before saving it. If you don’t want to print the option now, choose Save and
    close the window. The report window will be redisplayed.

**Chapter 31: General Ledger reports**

>   You can use General Ledger reports to analyze account activity and identify
>   errors in transaction entry. Use this information to guide you through
>   printing reports and working with report options. For more information about
>   creating and printing reports, and the various reporting tools that you can
>   use with Microsoft Dynamics GP, refer to your System User's Guide (Help \>\>
>   Contents \>\> select Using The System).

>   This information is divided into the following sections:

-   *General Ledger report summary*

-   *Specifying a General Ledger report option*

-   *General Ledger Microsoft SQL Server® Reporting Services reports*

#### General Ledger report summary

>   You can print several types of reports using General Ledger. Some reports
>   automatically are printed when you complete certain procedures; for example,
>   posting journals can automatically be printed when you post transactions,
>   depending on how your posting options are set up. You can choose to print
>   some reports during procedures; for example, you can print an edit list when
>   entering transactions by choosing the Print button in the batch entry
>   window.

>   In order to print some reports, such as analysis or history reports, you
>   must set up report options to specify sorting options and ranges of
>   information to include on the report. For more information, refer to
>   *Specifying a General Ledger report option*.

>   The following table lists the report types available in General Ledger and
>   the reports that fall into those categories. (Reports printed using Bank
>   Reconciliation are printed using many of the same windows. Refer to the Bank
>   Reconciliation documentation for information about reports printed in that
>   module.)

| **Report type**                                                                                                                                                                                                                                                  | **Report**                                                                                                                           | **Printing method**                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Setup reports                                                                                                                                                                                                                                                    | Setup List\* Account Category List Account Segment List Quick Journal Setup List Deferral Setup List Deferral Profile Setup          | Choose File \>\> Print in the setup windows **or** create report options in the Setup Reports or Deferral Reports window.                          |
| Chart of Account lists                                                                                                                                                                                                                                           | Accounts List Posting Accounts List Unit Account List Fixed Allocation Accounts List Variable Allocation Accounts List Category List | Create report options in the Chart of Accounts Report window.                                                                                      |
| Posting reports                                                                                                                                                                                                                                                  | General Posting Journal\*† Clearing Entry Posting Journal† Quick Journal Posting Journal†                                            | Choose File \>\> Print in the window you use to complete the procedure, **or** some will be printed automatically when you complete the procedure. |
| \* Indicates reports that can be printed with multicurrency information displayed. † Indicates reports that can be assigned to named printers. See the System Administrator’s Guide (Help \>\> Contents \>\> select System Administration) for more information. |                                                                                                                                      |                                                                                                                                                    |
| **Report type**                                                                                                                                                                                                                                                  | **Report**                                                                                                                           | **Printing method**                                                                                                                                |
| Edit lists                                                                                                                                                                                                                                                       | General Transaction Edit List\*                                                                                                      | Choose File \>\> Print in the window you used to complete the procedure.                                                                           |
| Revenue/Expense                                                                                                                                                                                                                                                  | Deferral Profile Report                                                                                                              | Create report options in the Deferral Reports window.                                                                                              |
| Transaction matching reports                                                                                                                                                                                                                                     | Transaction Matching by Account                                                                                                      | Create report options in the Transaction Matching Report Options window.                                                                           |
| History reports                                                                                                                                                                                                                                                  | Transaction History                                                                                                                  | Choose Financial \>\>Utilities \>\> Financial \>\> Remove History and mark the print option before removing history.                               |
| Utility report                                                                                                                                                                                                                                                   | Reconcile Report                                                                                                                     | This report will be printed when you complete the corresponding procedure.                                                                         |
| Cross-Reference reports                                                                                                                                                                                                                                          | Cross-Reference Report by Journal                                                                                                    | Create report options in the                                                                                                                       |
| Budget reports                                                                                                                                                                                                                                                   | Budget List                                                                                                                          | Create report options in the Budget Report window.                                                                                                 |
| Inquiry reports                                                                                                                                                                                                                                                  | Summary Inquiry Report                                                                                                               | Choose File \>\> Print in the corresponding Inquiry window.                                                                                        |
| Trial Balance reports                                                                                                                                                                                                                                            | Detailed Trial Balance\*†                                                                                                            | Create report options in the Trial Balance Report window.                                                                                          |
| \* Indicates reports that can be printed with multicurrency information displayed.                                                                                                                                                                               |                                                                                                                                      |                                                                                                                                                    |

>   Clearing Entry Edit List

>   Quick Journal Edit List

>   Deferral General Ledger Edit List\*

>   Deferral Edit List\*

>   Deferrals reports

>   Deferral Report

>   Number\*

>   Transaction Matching by Link Date\*

>   Transaction Matching by Link

>   Number\*

>   Transaction Matching by User ID\*

>   Account History

>   Entry†

>   Cross-Reference Report by Source

>   Document†

>   Cross-Reference Report by Audit

>   Trail Code†

>   Cross-Reference Report window.

>   Detail Inquiry Report

>   Journal Inquiry Report

>   History Detail Inquiry Report

>   Budget vs Actual Inquiry Report

>   Transaction Matching by Account

>   Inquiry

>   Transaction Matching by Link

>   Number Inquiry

>   Trial Balance Summary\*†

>   Trial Balance Worksheet\*†

>   Quick Detailed Trial Balance\*†

>   Quick Trial Balance Summary\*†

>   † Indicates reports that can be assigned to named printers. See the System
>   Administrator’s Guide (Help \>\> Contents \>\> select System Administration)
>   for more information.

| **Report type**                                                                                                                                                                                                                                                  | **Report**                                                                                         | **Printing method**                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Period and Year-end reports                                                                                                                                                                                                                                      | Period Consolidation Report Year-End Closing Report                                                | These reports will be printed when you complete the corresponding procedure.                                                                                                   |
| Financial Statements                                                                                                                                                                                                                                             | Balance Sheet† Profit and Loss Statement† Statement of Retained Earnings† Statement of Cash Flows† | Create a layout for the report in the Quick Financial Setup window. For more information about printing financial statements, see *Chapter 30, “Financial statement reports.”* |
| \* Indicates reports that can be printed with multicurrency information displayed. † Indicates reports that can be assigned to named printers. See the System Administrator’s Guide (Help \>\> Contents \>\> select System Administration) for more information. |                                                                                                    |                                                                                                                                                                                |

#### Specifying a General Ledger report option

>   Report options include specifications for sorting options and range
>   restrictions for a particular report. In order to print several General
>   Ledger reports, you must first create a report option. Each report can have
>   several different options so that you can easily print the information you
>   need. For example, you can create report options for the Trial Balance
>   Report that show either detailed or summary information.

>   *A single report option can’t be used by multiple reports. If you want
>   identical options for several reports, you must create them separately.*

>   Use the Financial report options windows to create sorting, restriction, and
>   printing options for the reports that have been included with General
>   Ledger.

>   **To specify a General Ledger report option:**

1.  Open a Financial reports window. There are separate windows for each report
    type.

>   (Financial \>\> Reports \>\> Financial \>\> Account)

>   (Financial \>\> Reports \>\> Financial \>\> Setup)

>   (Financial \>\> Reports \>\> Financial \>\> Financial Statements)

>   (Financial \>\> Reports \>\> Financial \>\> Budget)

>   (Financial \>\> Reports \>\> Financial \>\> Cross-Reference)

>   (Financial \>\> Reports \>\> Financial \>\> Trial Balance)

>   (Financial \>\> Reports \>\> Financial \>\> Deferral)

1.  Select a report from the Reports list.

2.  Choose New to open the report options window. Your selection in step 2
    determines which report options window appears.

3.  Name the option and enter information to define the option. The name you
    choose for the option won’t appear on the report. The selections available
    for defining report options vary, depending on the report type you’ve
    selected.

4.  Enter range restrictions. The Ranges list shows the available options for
    each report. The available ranges vary, depending on the type of report.

>   *You can enter only one restriction for each restriction type. For instance,
>   you can insert one account segment ID restriction (1100 to 1104) and one
>   account description restriction (Cash - Operating Account to Cash in Bank -
>   South Africa).*

1.  Choose Insert to insert the range in the Restrictions List. To remove an
    existing range from the list, select the range and choose Remove.

2.  Choose Destination to select a printing destination. Reports can be printed
    to the screen, to the printer, to a file, or to any combination of these
    options. If you select Ask Each Time, you can select printing options each
    time you print this report option.

3.  To print the report option from the report options window, choose Print
    before saving it. If you don’t want to print the option now, choose Save and
    close the window. The report window will be redisplayed.

#### General Ledger Microsoft SQL Server® Reporting Services reports

You can view General Ledger Reporting Services reports from the Reporting
Services Reports list. If you are using Reporting Services 2008, financial
metrics for your home page also appear in the Reporting Services Reports list.
You can access the Reporting Services Reports list from the navigation pane or
from an area page in the Microsoft Dynamics GP application window. This report
list appears if you specified the location of your Reporting Services reports
using the Reporting Tools Setup window. See your System Setup Guide (Help \>\>
Contents \>\> select Setting up the System) for more information.

The following Reporting Services reports are available for General Ledger.

Journal Entry Report Source Cross Reference

Trial Balance Detail Trial Balance Summary

**To print a General Ledger Reporting Services report:**

1.  In the navigation pane, choose the Financial button, and then choose the
    Reporting Services Reports list.

2.  Mark the General Ledger report that you want to print.

3.  In the Actions group, choose View to open the Report Viewer.

4.  In the Report Viewer, select the specifications for the report and choose
    View Report.

5.  After viewing the report, select a format and print the report.

**Part 6: Utilities and routines**

>   Utilities are the procedures you need to maintain your data in General
>   Ledger.

>   Routines are the sets of procedures you need to complete periodically. You
>   can use the checklists provided with General Ledger, you can customize those
>   checklists to suit your needs, or you can create your own checklists.

>   The following information is discussed:

-   *Chapter 32, “Checklists,”* describes how you can create customized
    checklists of General Ledger routines or modify existing checklists.

-   *Chapter 33, “Period and year-end routines,”* provides procedures to
    consolidate and close a period, as well as close a year.

-   *Chapter 34, “Account utilities,”* shows how to maintain your data in
    General Ledger.

**Chapter 32: Checklists**

>   You can create customized checklists of General Ledger routines or modify
>   existing checklists. For example, you can set up a checklist to ensure that
>   your month-end reports are printed consistently each month.

>   Checklist information is contained in the following sections:

-   *Using a General Ledger checklist*

-   *Adding or modifying a checklist item*

#### Using a General Ledger checklist

>   Use the Financial Checklists window to complete a General Ledger checklist.
>   As you select each step in the routine list, the appropriate window used to
>   complete that procedure appears. You can enter the necessary information in
>   the window, referring to the procedures in the printed manual or to the
>   online documentation whenever necessary.

>   **To use a General Ledger checklist:**

1.  Open the Financial Checklists window.

>   (Financial \>\> Routines \>\> Financial \>\> Checklists)

![](media/286463460ab461fd729920b1bad802ff.jpg)

1.  Select a frequency from the Frequency list. The list of tasks appears.

2.  Select a task in the checklist.

3.  Choose Open. The appropriate window opens for the selected task.

4.  Perform the required task, then close the window.

5.  In the Financial Checklists window, select the next task.

>   When you save the information, the window closes, and the Financial
>   Checklists window becomes active, displaying the date the procedure was
>   completed and the ID of the user who completed it.

#### Adding or modifying a checklist item

>   Use the Financial Checklists window to add or modify checklists of financial
>   routines. You can select the frequency with which each set of routines
>   should be completed. The following frequencies are available:

-   Daily

-   On payday

-   At the end of a period, month, quarter, fiscal year, or calendar year

-   During setup

-   User defined

>   **To add or modify a checklist item:**

1.  Open the Financial Checklists window.

>   (Financial \>\> Routines \>\> Financial \>\> Checklists)

1.  Select a frequency.

2.  Choose Add to add an item or select an item and choose Modify to modify an
    item. The Add-Modify Financial Routines window will open.

3.  Enter the item information.

4.  Choose OK to save the information. The Financial Checklists window is
    redisplayed, where you can adjust the position of the item in the checklist.

**Chapter 33: Period and year-end routines**

>   This part of the documentation describes routines you may complete at the
>   end of a period and at the end of a year. This chapter describes a
>   spreadsheet that you can generate to help you match transactions in General
>   Ledger with the corresponding transactions in the original module. You can
>   also find information to help you prepare and close a period and to prepare
>   and close a year. A procedure for printing a VAT return is also included.

>   This information is divided into the following sections:

-   *Reconciling to General Ledger*

-   *Understanding the reconciliation spreadsheet*

-   *Consolidating a period*

-   *Closing a period*

-   *Understanding closing a year*

-   *Preparing to close a year*

-   *Closing a fiscal year*

-   *Printing a VAT Return*

#### Reconciling to General Ledger

>   During normal business operations, thousands of transactions can be
>   processed. When working with this volume of transactions, standard processes
>   might be inadvertently changed, or unintended entries made and posted. As a
>   result, the balances on a General Ledger trial balance report might not
>   match the corresponding balance on trial balance reports printed in the
>   original module. Some specific examples might include the following.

-   A transaction is posted to—but not through—General Ledger and is deleted
    before it’s posted in General Ledger.

-   A transaction is posted to General Ledger, but the amounts are changed
    before it’s posted in General Ledger.

>   Use the Reconcile to GL window to set the restrictions for generating a
>   Microsoft Excel spreadsheet that can help you match transactions in General
>   Ledger with the original transaction. This spreadsheet provides information
>   that helps you enter adjusting transactions that reconcile any
>   discrepancies. For information about how transactions are matched, refer to
>   *Understanding the reconciliation spreadsheet*.

>   Transactions are displayed on the spreadsheet using the functional currency.
>   To be included in the spreadsheet, transactions must be posted and exist in
>   either an Open or History table.

>   *The reconcile routine can help you analyze transactions in General Ledger,
>   but it doesn’t change data automatically, even if unmatched transactions are
>   identified. Adjustments are not automatically created or posted, nor are
>   transactions marked or identified as being reconciled within General Ledger.
>   For information about entering reversing or correcting transactions in
>   General Ledger, refer to Chapter 23, “Correcting transactions.”*

>   Use the following procedures to help you reconcile the following modules:

-   *To reconcile Payables Management to General Ledger*

-   *To reconcile Receivables Management to General Ledger:*

-   *To reconcile Inventory Control to General Ledger*

-   *To reconcile Bank Reconciliation to General Ledger*

>   **To reconcile Payables Management to General Ledger**

1.  Open the Reconcile to GL window.

>   (Financial \>\> Routines \>\> Financial \>\> Reconcile to GL)

1.  Enter or select the Reconciliation number. This number is used as part of
    the default file name for the Excel spreadsheet. You can enter and save the
    information for the reconciliation and process later.

2.  Enter the date for this reconciliation. The user date is the default date.

3.  Enter the date range for the transactions to include in this reconciliation.
    Typically, reconciling to General Ledger is processed once a month, but
    transactions can be reconciled more or less often depending on the number of
    transactions in the module. The Payables Management transactions with a
    transaction date that is on or between the date range will be included in
    the reconcile.

4.  Select Payables Management to reconcile with General Ledger.

5.  Select a file location for the Excel spreadsheet that will be created. The
    output file and location is module-specific. After the first time you
    reconcile, the most recently used location for Payables Management
    reconciliations will be the default location.

>   The default file name is created for the Excel spreadsheet by using the
>   module abbreviation, reconciliation number, and date. This name can be
>   changed, however, we recommend that you use a consistent naming convention
>   and folder for all reconcile to General Ledger spreadsheets.

1.  Enter the accounts to use to match Payables Management transactions to
    General Ledger distributions. This would most often be the Accounts Payable
    or Discount Available accounts. The accounts that were on the previous
    reconciliation for Payables Management are displayed, if this is not the
    first reconciliation for this module.

2.  Choose Process. The matching process begins and the following occurs:

    -   Transactions from Payables Management are matched with General Ledger
        distributions using the transaction source code, voucher number, posting
        date, and transaction amount. This process may take some time, depending
        on the number of transactions being processed.

    -   Transactions are potentially matched if some, but not all, of the
        information matches. For example, if the source code and date for the
        transaction matches the code and date in General Ledger, but the
        transaction amounts don’t match, the transactions are considered
        potentially matched and will appear in that section of the spreadsheet.

    -   If the transaction exists in Payables Management but not in General
        Ledger or vice versa, the transaction is unmatched and will appear in
        the Unmatched section of the spreadsheet.

    -   The subledger and General Ledger balances are calculated and displayed
        in the window.

    -   The Excel spreadsheet is created and saved in the output file location
        that you specified in step 6. After the processing is complete, the
        spreadsheet will open.

>   You can use the spreadsheet to determine which, if any, next steps you need
>   to make.

>   **To reconcile Receivables Management to General Ledger:**

1.  Open the Reconcile to GL window.

>   (Financial \>\> Routines \>\> Financial \>\> Reconcile to GL)

1.  Enter or select the Reconciliation number. The number is used as part of the
    default file name for the Excel spreadsheet. You can enter and save the
    information for the reconciliation and process later.

2.  Enter the date for this reconciliation. The user date is the default date.

3.  Enter the date range for the transactions to include in this reconciliation.
    Typically, reconciling to General Ledger is processed once a month, but
    transactions can be reconciled more or less often depending on the number of
    transactions in the module. The Receivables Management transactions with a
    transaction date that is on or between the date range will be included in
    the reconcile.

4.  Select Receivables Management to reconcile with General Ledger.

5.  Select a file location for the Excel spreadsheet that will be created. The
    output file and location is module-specific. After the first time you
    reconcile, the most recently used location for Receivables Management
    reconciliations will be the default location.

>   The default file name is created for the Excel spreadsheet using the module
>   abbreviation, reconciliation number, and date. This name can be changed,
>   however, we recommend that you use a consistent naming convention and folder
>   for all reconcile to General Ledger spreadsheets.

1.  Enter the accounts to use to match Receivables Management transactions to
    General Ledger distributions. This would most often be the Accounts
    Receivable or Discount Available accounts. The accounts that were on the
    previous reconciliation for Receivables Management are displayed, if this is
    not the first reconciliation for this module.

2.  Choose Process. The matching process begins and the following occurs:

    -   Transactions from Receivables Management are matched with General Ledger
        distributions using the transaction source code, document number,
        posting date, and transaction amount. This process may take some time,
        depending on the number of transactions being processed.

    -   Transactions are potentially matched if some, but not all, of the
        information matches. For example, if the source code and date for the
        transaction matches the code and date in General Ledger, but the
        transaction amounts don’t match, the transactions are considered
        potentially matched and will appear in that section of the spreadsheet.

    -   If the transaction exists in Receivables Management but not in General
        Ledger or vice versa, the transaction is unmatched and will appear in
        the Unmatched section of the spreadsheet.

    -   The subledger and General Ledger balances are calculated and displayed
        in the window.

    -   The Excel spreadsheet is created and saved in the output file location
        that you specified in step 6. After the processing is complete, the
        spreadsheet will open.

>   You can use the spreadsheet to determine which, if any, next steps you need
>   to make.

>   **To reconcile Inventory Control to General Ledger**

>   *The Historical Inventory Trial Balance (HITB) table is used to reconcile
>   Inventory to General Ledger. Depending on the version of Microsoft Dynamics
>   GP you’re using, this table may not be included in your system. You must
>   contact Microsoft Dynamics GP Technical Support to see if the Historical
>   Inventory Trial Balance report and the HITB Inventory Reset Tool fits your
>   current business process.*

1.  Open the Reconcile to GL window.

>   (Financial \>\> Routines \>\> Financial \>\> Reconcile to GL)

1.  Enter or select the Reconciliation number. This number is used as part of
    the default file name for the Excel spreadsheet. You can enter and save the
    information for the reconciliation and process later.

2.  Enter the date for this reconciliation. The user date is the default date.

3.  Enter the date range for the transactions to include in this reconciliation.
    Typically, reconciling to General Ledger is processed once a month, but
    transactions can be reconciled more or less often depending on the number of
    transactions in the module. The Inventory transactions with a transaction
    date that is on or between the date range will be included in the reconcile.

>   *If any dates in the range are prior to the date you installed a version of
>   Microsoft Dynamics GP that includes HITB or updated your system using the
>   Inventory Reset Tool, you won’t be able to reconcile Inventory to General
>   Ledger.*

1.  Select Inventory to reconcile with General Ledger.

2.  Select a file location for the Excel spreadsheet that will be created. The
    output file and location is module-specific. After the first time you
    reconcile, the most recently used location for Inventory reconciliations
    will be the default location.

>   The default file name is created for the Excel spreadsheet using the module
>   abbreviation, reconciliation number and date. This name can be changed,
>   however, we recommend that you use a consistent naming convention and folder
>   for all reconcile to General Ledger spreadsheets.

1.  Enter the accounts to use to match Inventory transactions to General Ledger
    distributions. This would most often be the Inventory accounts. The accounts
    that were on the previous reconciliation for Inventory Control are
    displayed, if this is not the first reconciliation for this module.

2.  Choose Process. The matching process begins and the following occurs:

    -   Transactions from Inventory are matched with General Ledger
        distributions using the journal entry, transaction source code, document
        number, posting date, and extended cost amount. This process may take
        some time, depending on the number of transactions being processed.

    -   Transactions are potentially matched if some, but not all, of the
        information matches. For example, if the source code and date for the
        transaction matches the code and date in General Ledger, but the
        transaction amounts don’t match, the transactions are considered
        potentially matched and will appear in that section of the spreadsheet.

    -   If the transaction exists in Inventory but not in General Ledger or vice
        versa, the transaction is unmatched and will appear in the Unmatched
        section of the spreadsheet.

    -   The subledger and General Ledger balances are calculated and displayed
        in the window.

    -   The Excel spreadsheet is created and saved in the output file location
        that you specified in step 6. After the processing is complete, the
        spreadsheet will open.

>   You can use the spreadsheet to determine which, if any, next steps you need
>   to make.

>   **To reconcile Bank Reconciliation to General Ledger**

1.  Open the Reconcile to GL window.

>   (Financial \>\> Routines \>\> Financial \>\> Reconcile to GL)

1.  Enter or select the Reconciliation number. This number is used as part of
    the default file name for the Excel spreadsheet. You can enter and save the
    information for the reconciliation and process later.

2.  Enter the date for this reconciliation. The user date is the default date.

3.  Enter the date range for the transactions to include in this reconciliation.
    Typically, reconciling to General Ledger is processed once a month, but
    transactions can be reconciled more or less often depending on the number of
    transactions in the module. The Bank Reconciliation transactions with a
    transaction date that is on or between the date range will be included in
    the reconcile.

4.  Select Bank Reconciliation to reconcile with General Ledger

5.  Select the checkbook that contains the transactions to reconcile.
    Reconciliation information for Bank Reconciliation is saved and processed on
    a checkbook-by checkbook basis.

6.  Select a file location for the Excel spreadsheet that will be created. The
    output file and location is module specific. After the first time you
    reconcile, the most recently used location for Bank Reconciliation
    reconciliations will be the default location.

>   A default file name is created for the Excel spreadsheet using the
>   checkbook, reconciliation number and date. This name can be changed,
>   however, we recommend that you use a consistent naming convention and folder
>   for all reconcile to General Ledger spreadsheets.

1.  The cash account for the checkbook that you’re reconciling with General
    Ledger appears as a default account in the Account list. In Bank
    Reconciliation, each checkbook is assigned only one account, therefore, only
    one account should be entered in this window.

2.  Choose Process. The matching process begins and the following occurs:

    -   Transactions from Bank Reconciliation are matched with General Ledger
        distributions using the transaction source code, document number,
        transaction date, and payment or deposit amount. This process may take
        some time, depending on the number of transactions being processed.

    -   Transactions are potentially matched if some, but not all, of the
        information matches. For example, if the source code for the transaction
        matches the code in General Ledger, but the transaction amounts don’t
        match, the transactions are considered potentially matched and will
        appear in that section of the spreadsheet.

    -   If the transaction exists in Bank Reconciliation but not in General
        Ledger or vice versa, the transaction is unmatched and will appear in
        the Unmatched section of the spreadsheet.

    -   The subledger and General Ledger balances are calculated and displayed
        in the window.

    -   The Excel spreadsheet is created and saved in the output file location
        that you specified in step 7. After the processing is complete, the
        spreadsheet will open.

>   You can use the spreadsheet to determine which, if any, next steps you need
>   to make.

#### Understanding the reconciliation spreadsheet

>   The Excel spreadsheet that is created through the reconciliation process can
>   be used to identify the unmatched or potentially matched transactions to
>   help you find the transactions that you may need to correct. Matched
>   transactions will also be printed on the spreadsheets as a reference.

>   There are links from several cells on the spreadsheet to the entry or
>   inquiry windows in the original module, so you can see details that aren’t
>   available on the spreadsheet.

>   The information used to match transactions with General Ledger differs
>   depending on which module you’re reconciling. In addition, some modules
>   display additional information on the spreadsheet to help you identify the
>   transaction in the original module. The following table shows which fields
>   are used to match the corresponding General Ledger field in each module.

| **General Ledger** | **Inventory**  | **Receivables**  |
|--------------------|----------------|------------------|


>   **Management**

**Payables**

>   **Management**

**Bank Reconciliation**

| **Transaction Date**   | GL Post Date       | Posted Date        | Posting Date       | Date               |   |   |
|------------------------|--------------------|--------------------|--------------------|--------------------|---|---|
| **Journal Entry**      | Journal Entry      |                    |                    |                    |   |   |
| **Orig. Transaction**  | Transaction Source | Transaction Source | Transaction Source | Transaction Source |   |   |
| **Orig. Control**      | Document Number    | Document Number    | Voucher Number     | Document Number    |   |   |
| **DR/CR**              | Extended Cost      | On Account Amount  | On Account Amount  | Payment/Deposit    |   |   |
|                        |                    | Customer Number    | Vendor ID          | Transaction Number |   |   |
|                        |                    |                    | Document Number    | Type               |   |   |

>   **Source**

>   **Number**

>   After the information is processed, you will see three sections on the Excel
>   spreadsheet that opens.

>   **Unmatched**

>   This section of the spreadsheet lists the transactions in which no fields in
>   the subledger and General Ledger match. This may occur, for example, if
>   transactions are not posted in General Ledger, or if subledger history has
>   been removed.

>   **Potentially Matched**

-   If some subledger fields, but not all, match the corresponding fields in
    General Ledger, the transactions are considered Potentially Matched and are
    listed in that section of the spreadsheet.

-   Potentially matched transactions may occur if, for example, a Receivables

>   Management transaction is entered and posted but the corresponding General
>   Ledger transaction is deleted. If the General Ledger transaction is
>   re-entered and posted because the correction has been made, the transaction
>   amounts and posting dates are the same, but the audit trail and document
>   number entries will be different.

>   **Matched**

-   When all fields in the subledger match the corresponding fields in General
    Ledger, the transactions are considered Matched and are listed in that
    section of the spreadsheet.

-   If there are transactions that are matched that do not have an entry in the
    General Ledger Originating Control Number column on the spreadsheet, verify
    whether they were posted in summary to General Ledger. Control number
    information is not used when posting in summary.

-   You may have multiple subledger transactions matched to one General Ledger
    transaction and vice versa. For example, two receipts are entered in
    Purchase Order Processing and are posted in summary to General Ledger. One
    distribution line is used to record the extended cost of the two receipts in
    the Inventory account in General Ledger. Or, if one receipt is entered in
    Purchase Order Processing containing two items, each using a different
    Inventory account. Two entries would be posted in General Ledger and you’ll
    see two entries if both accounts were selected to reconcile in the Reconcile
    to GL window.

>   **Additional information**

>   **Voided transactions** When the original transaction and the voided
>   transaction are both within the date range you selected, both the original
>   and voided transaction will appear on the spreadsheet. The voided
>   transaction will be indicated as such with an asterisk. However, if the
>   reversing entry occurs outside of the date range, the original transaction
>   will appear as it did originally, and it will not be indicated as a voided
>   transaction.

>   **Bank Reconciliation deposit group matching** A deposit group is made up of
>   the receipts associated with a deposit record. All receipts found in the
>   group are displayed together on the spreadsheet, whether matched,
>   potentially matched or unmatched. For example, if the General Ledger date of
>   one of the receipts in the deposit group doesn’t match the receipt date in
>   Bank Reconciliation, all receipts in the group are potentially matched.
>   Additionally, if the sum of the receipts in the deposit group does not match
>   the deposit amount (and all other fields are matched) the group is
>   considered potentially matched and appears in that section of the
>   spreadsheet.

>   **Links to inquiry windows from Excel** Click any field data indicated with
>   colored text to open the entry or inquiry window displaying the information
>   as it was originally entered.

>   *Use the procedures in the subledger module documentation to help you make
>   corrections to existing transactions.*

#### Consolidating a period

>   Consolidating a period combines the transaction detail into a single summary
>   transaction balance for each account carried forward to the next period.
>   Consolidating is optional and can be used if you no longer need detailed
>   information for the period in question.

>   *Once the consolidation is complete, the detailed transactions will no
>   longer be available for reporting or inquiry purposes. You can no longer
>   post transactions to the period and a single total will appear on the
>   Detailed Trial Balance for each consolidated account.*

>   If you are using multiple ledgers, when you consolidate a period,
>   information is consolidated by reporting ledger. This means that a period
>   transaction is created for each reporting ledger for each account that has
>   one or more transactions assigned to a reporting ledger. Note that a
>   transaction can have only one reporting ledger, but an account can have
>   multiple transactions, each with a different reporting ledger.

>   For example, in June, Account 1100 has six transactions in the base
>   reporting ledger and four in the local reporting ledger. When the June
>   period is consolidated, Account 1100 will have one transaction for base and
>   one for local.

>   When a period has been consolidated, you can mark it as closed to prevent
>   transactions from being posted to it. You also can close fiscal periods
>   without consolidating them first. For more information about closing fiscal
>   periods, see *Closing a period*.

>   Before consolidating a period, enter and post all adjusting entries to
>   correct transaction detail for the period you want to consolidate. Adjusting
>   entries include all entries that correct errors made in recording
>   transactions, and journal entries that assign revenues or expenses to the
>   period in which they were earned or incurred. After you’ve entered adjusting
>   entries, print an edit list to verify the accuracy of the data you’ve
>   entered and post the transactions.

>   You also should print financial statements and a trial balance before and
>   immediately after consolidating a period. Then, you can compare the detailed
>   information printed before the consolidation with the summary information
>   printed immediately after consolidating a period. You can set up a group of
>   period end reports in the Financial Groups window that can be used to print
>   all the financial statements and the Trial Balance each time you consolidate
>   a period.

>   *Before consolidating the period, make a complete backup of your company’s
>   accounting data. If you have a current backup, information can be restored,
>   if necessary.*

>   **To consolidate a period:**

1.  Open the Period Consolidation window.

>   (Financial \>\> Routines \>\> Financial \>\> Period Consolidation)

![](media/a38ccbd964c40258a1b009f2ad7d1565.jpg)

1.  Choose whether you want to consolidate a period from an open year or a
    historical year.

2.  Enter or select the year that contains the period you want to consolidate.
    You can only select a year that contains transactions.

3.  Enter or select a period.

4.  Choose Ranges to display the Account Segment Ranges window. You can
    restrict—by account segment—the accounts that will be consolidated. When
    you’ve finished, close the Account Segment Ranges window.

>   *If you restrict the consolidation process by account segments, your reports
>   might not balance. For example, if you post a credit of \$100 to the Cash
>   account and a debit of \$100 to the Accounts Payable account in Period 1 and
>   then consolidate the Cash account for Period 1 only, the Cross-Reference
>   Report by Journal Entry will be out of balance by \$100.*

1.  Choose OK to consolidate the selected period.

#### Closing a period

>   Use the Fiscal Periods Setup window to mark the period as being closed for
>   the Financial series. When you close a period, you can’t post transactions
>   to the period. This is useful if you want to prevent a user from accidently
>   posting a transaction to a period. The period may be reopened at any time
>   and the transaction details will print on the Detailed Trial Balance.

>   Before closing a period, enter and post all adjusting entries to correct
>   transaction details for the period you want to close. Adjusting entries
>   include all entries that correct errors made in recording transactions, and
>   journal entries that assign revenues or expenses to the period in which they
>   were earned or incurred. After you’ve entered adjusting entries, print an
>   edit list to verify the accuracy of the data you’ve entered.

>   **To close a period:**

1.  Open the Fiscal Periods Setup window.

>   (Administration \>\> Setup \>\> Company \>\> Fiscal Periods)

![](media/6a72e86aedfcac2700d38fa03d7f758b.jpg)

1.  Enter or select a year.

2.  Mark the period you want to close.

>   *Within the open and historical years, you can close periods for a Microsoft
>   Dynamics GP series. For example, if you close the Sales series for the first
>   period of an open fiscal year, you won’t be able to post from any
>   transaction entry window in Receivables Management, Invoicing, or Sales
>   Order Processing to that closed period.*

1.  If you want to close individual transaction origins within each Microsoft
    Dynamics GP series, choose Mass Close to open the Mass Close Fiscal Periods
    window. For example, if you’ve decided you no longer want to post
    transactions for the sale of merchandise to the period you’ve consolidated,
    you can close the Receivables Transaction Entry window.

2.  Choose OK to close the window and save your entries.

#### Understanding closing a year 

>   Closing the year transfers all current-year information for each account in
>   the chart of accounts to account and transaction history (if you’re keeping
>   history records) and prepares the accounting system for a new fiscal year.

>   You can enter General Ledger transactions for the next fiscal year without
>   closing the current year, leaving fiscal years open until all adjusting
>   entries have been entered and posted to the correct periods. You can set up
>   and post to unlimited open years.

>   In addition to transferring open-year amounts to transaction and account
>   history, the year-end closing process:

-   Reconciles and summarizes the General Ledger balances that have accumulated
    throughout the year.

-   Transfers open-year profit and loss amounts to the Retained Earnings
    account.

-   Zeros all profit and loss account balances after they’ve been closed to the
    Retained Earnings account.

>   *If you find you need to enter adjustments to a profit and loss account
>   after you’ve closed the year, the system will automatically update the
>   corresponding retained earnings account. You won't need to do anything
>   following the adjustments.*

-   Summarizes balance sheet accounts, bringing the balances forward as the
    accounts’ beginning balances in the new fiscal year.

>   Until the year-end close is completed for General Ledger, you won’t get
>   accurate financial statements for the new year. Beginning balances for the
>   new year are not created until the year-end close process is completed.
>   Therefore, the financial statements for the new year will reflect only
>   current year activity until the year-end closing process is completed. This
>   happens whether the financial statements are printed from Advanced Financial
>   Analysis or Management Reporter.

-   Consolidates information by reporting ledger. This means that a transaction
    is created as of the last day of the previous fiscal year for each account
    that has one or more transactions assigned to a reporting ledger. A retained
    earnings transaction is created for each reporting ledger based on the
    consolidation of the profit and loss accounts. Note that a transaction can
    have only one reporting ledger, but an account can have multiple
    transactions, each with a different reporting ledger.

-   Prints the Year-End Closing Report.

#### Preparing to close a year

>   Before you close a year, you must complete the following tasks:

-   Complete month-end and period-end procedures for all modules, except General
    Ledger.

-   Use normal posting procedures to post final transactions in all modules,
    except General Ledger.

-   After all transactions have been posted successfully, complete year-end
    procedures for all modules, in the following order: Inventory, Receivables
    Management, and Payables Management.

>   Payroll year-end procedures are independent of those in other modules and
>   are always performed at the calendar year-end.

-   Post final adjusting entries in General Ledger.

>   If you need to make any adjusting entries to allocate revenue, expenses, or
>   depreciation to the year you’re going to close, use the Transaction Entry
>   window or the Quick Journal Entry window to enter adjusting entries in
>   General Ledger.

>   Many of these adjusting entries were made automatically if you marked them
>   as reversing in the Transaction Entry window. Entries that increased assets
>   or liabilities could be entered as automatically reversing since they would
>   result in a future cash receipt or payment.

-   You can close the last period of the current fiscal year.

>   Use the Fiscal Periods Setup window to close any fiscal periods that are
>   still open for the current fiscal year. This keeps transactions from
>   accidentally being posted to the wrong period or year.

>   *Be sure you've posted all transactions for the period and year for all
>   modules before closing fiscal periods. If you later need to post
>   transactions to a fiscal period you've already closed, you'll need to return
>   to the Fiscal Periods Setup window to reopen the period before you can post
>   the transaction.*

-   You can print an Account List to verify the posting type for the posting
    accounts. To print an Account List, choose Financial \>\> Reports \>\>
    Financial \>\> Accounts to open the Chart of Accounts Report window and
    select All Accounts in the Reports list. Use this report to verify that all
    balance sheet and profit and loss accounts have the correct posting type.
    The posting type is used to determine which posting accounts should be
    closed to retained earnings and which accounts should have the balance
    brought forward to the next year.

>   If the posting type is incorrect for an account, you can change it in the
>   Account Maintenance window (Financial \>\> Cards \>\> Financial \>\>
>   Account) before closing the year.

-   If you want to keep historical records, verify that Maintain History for
    Accounts and for Transactions are marked in the General Ledger Setup window
    (Financial \>\> Setup \>\> Financial \>\> General Ledger). If you maintain
    account history, you can print financial statements and calculate budgets
    from historical years. If you maintain transaction history, you can drill
    down to transaction detail and print historical detail trial balances.

>   If these boxes aren’t marked, the transaction or account information for the
>   year will be deleted once the year end close process is completed.

-   Check links for all Financial tables.

-   Back up your company data.

-   Use the Trial Balance Report window to print a year-end detailed trial
    balance.

>   *Be sure you've posted all transactions for the period and year for all
>   modules before printing the Detailed Trial Balance. If you later need to
>   post transactions, you should print a new Detailed Trial Balance.*

-   Print any year-end financial statements required.

-   Set up a new fiscal year.

>   Before you can perform a year-end closing, a new fiscal year must be set up
>   using the Fiscal Periods Setup window. For example, if you’re closing 2004,
>   be sure that 2005 has been created.

#### Closing a fiscal year

>   Use the Year-End Closing window to close a year and prepare the accounting
>   system for a new fiscal year.

>   After you close a year, you can continue to post transactions within the
>   year as long as the year remains the most recent historical year and as long
>   as the period you’re posting transactions within hasn’t been marked closed
>   in the Fiscal Periods Setup window (Administration \>\> Setup \>\> Company
>   \>\> Fiscal Periods). Historical years include years that have been closed
>   using the fiscal year-end closing routine, and also years for which the
>   Historical Year option has been marked in the Fiscal Periods Setup window.
>   See the System Setup instructions (Help \>\> Contents \>\> select Setting Up
>   the System) for more information about using the Fiscal Periods Setup
>   window.

>   Posting to an historical year is useful if you have to enter audit
>   adjustments after you have closed the year. See *Posting to a historical
>   year* for more information.

>   **To close a fiscal year:**

1.  Open the Year-End Closing window.

>   (Financial \>\> Routines \>\> Financial \>\> Year End Closing)

1.  Enter or select a retained earnings account to which the year’s profit or
    loss will be closed. If you are closing to divisional retained earnings,
    enter or select one of the divisional retained earnings accounts.

2.  Enter a starting journal entry that will be used as the first journal entry
    number in the next fiscal year.

3.  Mark the Remove Unused Segment Numbers option to automatically remove
    account segment numbers that are not used in any account.

4.  Specify how to handle inactive accounts with zero balances during the
    year-end close.

    -   To keep inactive accounts with zero balances that have budget amounts,
        mark Maintain Inactive Accounts, and then select With Budget Amounts.
        Inactive accounts with zero balances and no budget amounts will be
        deleted during the year-end close.

    -   To keep all inactive accounts with zero balances, mark Maintain Inactive
        Accounts, and then select All Inactive Accounts.

    -   To delete all inactive accounts with zero balances, unmark Maintain
        Inactive Accounts.

5.  Choose Close Year to begin the closing process.

>   A status bar in the Year-End Closing window appears, displaying the steps
>   that are completed.

| **Step** | **Description**                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------|
| Step 1   | Transactions and the retained earnings account are verified.                                                  |
| Step 2   | Account balances are verified.                                                                                |
| **Step** | **Description**                                                                                               |
| Step 3   | Fiscal year information is verified. Posting numbers and transactions are reconciled.                         |
| Step 4   | Beginning balances brought forward and retaining earnings are created and distributions are moved to history. |
| Step 5   | Divisional retained earnings account is closed.                                                               |
| Step 6   | Posting numbers used during the year-end close are updated.                                                   |
| Step 7   | The previous year is removed from the account summary.                                                        |

>   *Step 3 and step 4 may take a long time to complete. Don’t try to close
>   Microsoft Dynamics GP or restart the computer. Let the process continue.*

>   When closing is complete, the Year-End Closing Report is printed. This
>   report lists the accounts that have been closed and the transactions created
>   to close them. The Year-End Closing Report is part of the audit trail and
>   should be saved with your company’s permanent records.

>   *You should not complete step 6 until you're sure that adjusting
>   transactions won’t be needed for the year.*

1.  You can close all fiscal periods for all series using the Fiscal Periods
    Setup window.

>   This step will prevent transactions from being posted from any module to any
>   period in the year you closed. Once a period has been marked as closed, you
>   can’t post transactions to it, unless it is reopened in the Fiscal Periods
>   Setup window.

1.  Adjust budget figures for the new year using the Budget Maintenance or
    Single Account Budget Maintenance windows and print financial statements.

>   After closing the year, update all Trial Balance and Cross-Reference report
>   options if you want to print them for another open year.

>   *After you finish closing a year, make a complete backup of your company’s
>   accounting data.*

#### Printing a VAT Return

>   Use the VAT Return window to print VAT reports you must submit to the
>   government. You can print summary and detailed VAT information for a
>   specified period. You can save VAT report IDs and reprint reports at a later
>   time.

>   **To print a VAT Return:**

1.  Open the VAT Return window.

>   (Administration \>\> Routines \>\> Company \>\> VAT Return)

![](media/21319f76bab86ce5c494a6acf71d3d56.jpg)

1.  Enter or select a VAT report ID and description.

2.  Enter starting and ending dates for the report.

>   Each VAT Report ID you create must have a unique starting date. You can’t
>   use the same starting date on more than one report ID.

1.  Choose Calculate. VAT Return information is displayed in the VAT Return
    window.

2.  To save the report, choose Save. You must calculate VAT information before
    you can save the report ID.

3.  To print the report, choose Print. The VAT Return Print Options window will
    open. Mark the reports you want to print. You can print summary, detail, tax
    detail, or exception reports.

>   Choose Print. A Report Destination window will appear, where you can select
>   to print to a file, to the screen, or to a printer.

**Chapter 34: Account utilities**

>   The following procedures remove historical data from your system, so be sure
>   to back up your accounting data before performing any of these procedures.

>   This information is divided into the following sections:

-   *Reconciling financial data*

-   *Removing or printing history*

-   *Archiving matched transactions*

-   *Checking links for deferral records*

#### Reconciling financial data

>   Use the Reconcile Financial Information window to reset account totals in
>   the chart of accounts so they match the posted transaction amounts.
>   Reconciling an open year ensures that amounts on the financial statements
>   are the same as the totals printed on the Detailed Trial Balance.
>   Reconciling recalculates account summary amounts for the open periods.

>   You also can reconcile account balances for a historical year, if you’re
>   keeping both account and transaction history. This can be useful for
>   comparing historical-year amounts to open-year totals and budget amounts.
>   For example, reconciling a historical year is valuable if your accounting
>   periods for a historical year and an open year are set up differently. By
>   reconciling accounts, you can redistribute historical-year transactions to
>   periods that parallel the open year; transactions are distributed according
>   to their posting dates. Then, you could compare historical year and
>   open-year amounts.

>   *Before reconciling accounts, back up all your company’s accounting data.
>   For more information about making backups, refer to the System
>   Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

>   **To reconcile financial data:**

1.  Open the Reconcile Financial Information window.

>   (Financial \>\> Utilities \>\> Financial \>\> Reconcile)

![](media/f75f1ac5808bc07ef8ec098d89524e1c.jpg)

1.  You can indicate if all allocation accounts should be reconciled.

>   If you reconcile allocation accounts, the system verifies the validity of
>   all allocation accounts, distribution and breakdown accounts, and account
>   types. If the allocation accounts contain errors, the Reconcile Report is
>   printed. The reconciliation process doesn't correct allocation account
>   errors, you must enter those corrections manually.

1.  Select a year to reconcile.

>   You can reconcile either an open year or a historical year that contains
>   transactions. You must be maintaining both account history and transaction
>   history to reconcile records for a historical year.

1.  Indicate whether you want to reconcile batches.

>   If you reconcile batches, the system verifies that all the identifying
>   information for the unposted batches is correct. If you reconcile batches
>   and identifying records are added, the Reconcile Report is printed.

1.  Choose Posting Numbers to open the Reconcile Posting Numbers window, where
    you can reconcile posting numbers so that no gaps in the posting number
    sequence exist.

>   The Posting Numbers buttons appears only if you have marked the Enable
>   Posting Numbers in General Ledger option in the Company Setup Options
>   window. Sequential posting numbers are a legal requirement in some European
>   countries.

1.  Choose Reconcile to reconcile account totals, batch information, or both.

#### Removing or printing history

Use the Remove History window to remove ranges of account or transaction history
that are no longer useful. If you’re keeping account and transaction history,
those records can be maintained for historical years. When you close the year,
the system transfers the records for the year being closed, then creates new
history records.

Transaction history is a record of all General Ledger transactions transferred
from an open year to history during the year-end closing process. Account
history is a record of the beginning and period balances for the historical year
for all accounts in the chart of accounts.

After removing history, you won’t be able to print the Transaction and Account
History reports or reprint source document reports for the dates or account
ranges that you’ve removed.

>   *Before removing history, back up your company’s accounting data. For more
>   information about making backups in Microsoft Dynamics GP, see the System
>   Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

>   **To remove or print history:**

1.  Open the Remove History window.

>   (Financial \>\> Utilities \>\> Financial \>\> Remove History)

![](media/313b3653a5ee700d049803a3920b8803.jpg)

2.  Indicate whether to remove or print transaction and account histories.

>   If you’ve decided to remove transaction history, mark the Remove option. If you mark Print, the Transaction History Report is printed for the range of accounts you’ll specify later in this procedure.

>   To remove account history, mark the appropriate option and choose to print this information on the Account History Report. The reports you’ve selected will be printed when the procedure is completed.

>   *You can print the Account History Report or Transaction History Report without removing history. To do so, mark only the Print options and choose Process.*

3.  Select a year for which you want to remove history and select a range of information to remove. You will be able to select only a year that contains transactions.

>   You can remove all transactions and account balances from the selected year  by marking All. If you don’t want to remove all records, you can remove a range of transactions by period or date. If you’re removing account history, select period range since account history is kept period-by-period.

>   If you select to remove both account and transaction history and enter a period or date range, account history for the entire year will be removed. However, transaction history will be removed only for the date range you’ve entered. To remove both account and transaction history for a range of dates, we recommend you complete the procedure for each type of history separately.

4.  Enter a beginning and an ending period, or a beginning and an ending date, if you’ve selected to remove history for a period or date range.

5.  Choose Ranges to open the Account Segment Ranges window to enter the account segments for which history will be removed. When you’ve entered the appropriate restrictions in the Restrictions list, choose OK to close the Account Segment Ranges window.

6.  Choose Process in the Remove History window to remove history.

#### Archiving matched transactions

Use the Archive Matched Transactions window to move transaction distribution links to history. You can still view the historical links in inquiries and reports, but you won’t be able to modify them.

>   **To archive matched transactions:**

1.  Open the Archive Matched Transactions window.

>   (Financial \>\> Utilities \>\> Financial \>\> Archive Matched Transactions)

![](media/3b0629e876585bdddccca2b960ad51b9.jpg)

2.  Mark the option to archive links and enter the archive date. Transaction distribution links with a date prior to this date will be moved to history.

3.  Indicate whether you want to move links with a zero balance to history.

4.  Choose OK.

#### Checking links for deferral records

Use the Deferral Check Links window to verify that your transaction distribution deferral data is accurate. Checking links examines a set of records and compares them to related information.

>   **To check links for deferral records:**

1.  Open the Deferral Check Links window.

>   (Microsoft Dynamics GP menu \>\> Maintenance \>\> Deferral Check Links)

![](media/f1cedffc055877a4a0bd669756349f66.jpg)

2.  Select each table you want to check links for and choose Insert.

3.  Choose OK.

**Glossary**

#### Account categories

>   General Ledger provides account categories that are used for grouping accounts on financial statements. Account categories also can be used as a sorting method for viewing the chart of accounts. Examples of account categories include Cash, Short Term Investments, and Notes Receivable.

#### Account history

>   A record of summarized account balances for historical years.

#### Account segment

>   A portion of the account format that can be used to represent a specific aspect of a business. For example, accounts can be divided into segments that represent business locations, divisions, or profit centers.

#### Account segment number

>   A number that represents a particular area of a business or an account category. Using account 01-200-1100, for example, account segment number 01 might represent a particular site, 200 might represent a department located at that site, and 1100 might represent the Cash account for that site and that department. Descriptions can be entered for each account segment number and appear on General Ledger reports.

#### Accrual basis accounting

>   The reporting of all accounting activity in the period in which it occurs, regardless of whether cash has been paid or received.

#### Accrued expense 

>   An expense that increases from day to day, but is recorded only when cash is paid. Salary Expense is an example of an accrued expense, because the amount a company owes increases daily but cash payments commonly are made on a biweekly or monthly basis. *See also Accrued liability*.

#### Accrued liability

>   An accrued expense that remains unpaid at the end of an accounting period. *See also Accrued expense*.

#### Accrued revenue

>   Revenue received during an accounting period that hasn't been recorded at the end of an accounting period. In such cases, the revenue should be recorded by debiting an asset account and crediting a revenue account.

#### Accumulated depreciation account

>   An asset account used to record an asset's total depreciation to date.

#### Adjusting entries

>   End-of-period journal entries that assign revenues and expenses to the period in which they were earned and incurred. Adjusting entries also can be used to correct errors in recording transactions.## Alert message

>   A message that appears when inappropriate, inadequate, or unclear data or instructions are issued, when data is not accessible, or when a confirmation is sought. Additional information about some alert messages and their causes can be viewed by choosing the Help button in the alert message dialog box.

#### Allocation account

>   An account that is used to distribute percentages of a single transaction to several other accounts. For example, an allocation account can be used to distribute rent expense to each of the sites affected by the expense.

#### Audit trail 

>   A series of permanent records used to track a transaction to the point where it was originally entered in the accounting system. The audit trail can be used to verify the accuracy of financial statements by outside accountants or auditors.

#### Audit trail code

>   A series of alphanumeric characters providing a precise record of each transaction and where it has been posted within Microsoft Dynamics GP.

#### Background processing

>   A processing system that allows users to continue working while transactions are posting or reports are printing.

#### Batch

>   A group of transactions identified by a unique name or number. Batches are used in computerized accounting to conveniently group transactions, both for identification purposes and to speed up the posting process.

#### Batch controls

>   Values for both the number of transactions in a batch and the total currency amount of the batch. As transactions are entered, the actual totals are displayed. These totals can be verified periodically as transactions are entered to ensure the required number and amount of transactions match the actual number and amount that was entered.

#### Batch frequency

>   A selection in the Batch Entry window that determines how often a recurring batch will be posted, such as weekly, monthly, or quarterly. *See also Recurring batch*.

#### Batch posting

>   A posting method that allows transactions to be saved in batches and post the batch whenever convenient. There are three types of batch-level posting: batch posting, series posting, and master posting.

#### Breakdown accounts

>   Accounts whose balances are used to determine the percentages that will be posted to the distribution accounts assigned to a variable allocation account.

#### Chart of accounts

>   A list of all accounts that a business maintains in its general ledger.

#### Chart of accounts reports

>   A General Ledger report type from which report options can be created for an Accounts List, Posting Accounts List, Unit Accounts List, Fixed Allocation Accounts List, Variable Allocation Accounts List, and Category List.

#### Clearing transaction

>   Transaction used to transfer the balance of an account to another account without deleting the account. Clearing transactions are also useful when accounts are obsolete, but can’t be deleted because they have current-year activity that should appear on the financial statements.

#### Closing entries

>   Entries made to close and clear temporary accounts, such as an Income Summary account. The effect of a closing entry is a net increase or a net decrease to the Retained Earnings account.

#### Comma-delimited fields

>   A standard ASCII, or character, file format used when exporting a report so that it can be read by programs that use this format.

#### Cross-reference reports

>   A General Ledger report type from which report options can be created for cross reference reports by source document, audit trail code, or journal entry number. The cross-reference reports are used to trace the audit trail of a company's transaction activity.

#### Currency symbol

>   The symbol that has been selected to designate currency amounts on reports. Most information about how currency amounts are displayed can be specified in the operating system documentation.

#### Default value

>   A value that is displayed in a window automatically, and that will be used unless a different value is entered.

#### Deferral

>   Delaying the recognition of revenue or expense. Usually, deferred revenue or expense is recognized at specific intervals over a period of time. For example, a customer may make a single payment for a yearly service contract, and a portion of the revenue is recognized each month.

#### Department

>   A business division that incurs costs and/or generates revenue. In General Ledger, an account segment can be used to identify a department or division of a business.

#### Detailed report

>   A report that displays detailed transaction information for each account.

#### Distribution accounting

>   The practice of allocating transactions to their departments of origin.

#### Distribution accounts

>   Accounts assigned to a fixed or variable allocation account that will receive a percentage of transaction amounts when the journal entry is posted.

#### Divisional retained earnings accounts

>   Two or more accounts among which the net income or net loss amount has been divided.

#### Double-entry accounting

>   An accounting process whereby equal credit and debit amounts are entered for each transaction.

#### Edit list

>   A list of transactions in an unposted batch that can be printed to verify the accuracy of transactions before posting. Edit lists can be printed from the Batch Entry window or any transaction entry window as long as a batch ID has been entered.

**Error message**

>   *See Alert message*.

#### Financial series

>   A group of Microsoft Dynamics GP modules including General Ledger with Advanced Financial Analysis and other modules in which transaction information from other modules is collected and maintained.

#### Financial statements

>   In General Ledger, a term that refers collectively to the Balance Sheet, Profit and Loss Statement, Statement of Cash Flows, and Statement of Retained Earnings.

**Financial year**

>   *See Fiscal year*.

#### Financing section

>   The section of a Statement of Cash Flows that includes transaction amounts for obtaining resources for owners and providing them with a return on their investments, along with obtaining resources from creditors and repaying the amounts borrowed.

#### Fiscal period

>   Division of the fiscal year, usually monthly, quarterly, or semiannually, when transaction information is summarized and financial statements are prepared.

#### Fiscal year

>   An accounting cycle composed of up to 54 consecutive periods, spanning the number of days in a year. The fiscal year may also be referred to as a *financial year*.

#### Fixed allocation account

>   Accounts used to distribute specified percentages of a single transaction among several distribution accounts.

#### Fixed allocation retained earnings account

>   Accounts used to distribute specified percentages of retained earnings among several distribution accounts.

#### Group printing

>   Creating and printing report options in groups. For example, a report group could be used to print all the financial statements and the Trial Balance before closing a month, quarter, or fiscal year.

#### HTML file

>   A file format that allows you to place financial information on your company’s intranet or web site.

#### Inquiry

>   A feature that allows users to view information for open and historical years.

#### Investing section

>   The section of a Statement of Cash Flows that includes amounts for transactions involving lending money and collecting on the loans, acquiring and selling investments, and acquiring and selling property and equipment.

#### Journal entry

>   A transaction recorded in a formalized manner by entering an account and debit and credit amounts.

#### Lookup window

>   A window that displays a list of accounts, customers, jobs, or other items in the Microsoft Dynamics GP system. Lookup windows for a specific field are displayed by choosing the lookup button next to the field.

#### Macro

>   A series of actions performed within an application that have been recorded for playback at another time. Macros can be used to automate repeated tasks, such as month-end procedures or printing reports.

#### Main segment

>   The segment of posting accounts that has been designated as the sorting option for accounts on financial statements. Typically, the main segment is used to indicate whether the account is an asset, liability, owners’ equity, revenue, or expense account.

#### Mass modify

>   A process in which ranges of accounts are copied, moved, deleted, or inactivated.

#### Master posting

>   A posting process in which marked batches from different series can be posted simultaneously.

#### Module

>   A group of Microsoft Dynamics GP applications that can be used to perform a specific set of tasks. Modules are combined to form a *series*. For example, the General Ledger with Advanced Financial Analysis is a member of the Financial series. *See also Series*.

#### Net income/loss source

>   The Profit and Loss Statement used to calculate the net income/loss on another financial statement.

#### Offset account

>   In double-entry accounting, the second account used to balance a transaction, making debits equal credits.

#### Operating section

>   The section of a Statement of Cash Flows that includes transaction amounts for acquiring, selling, and delivering goods for sale, along with providing services.

#### Origin

>   A transaction window within a specific Microsoft Dynamics GP module. Certain options, such as verifying batch controls and closing fiscal periods, can be selected for each transaction origin. Also, the transaction origin will appear as part of the audit trail code on all posting reports in Microsoft Dynamics GP.

#### Password

>   A combination of distinct, user-defined characters used to gain access to the Microsoft Dynamics GP system or to a selected application within Microsoft Dynamics GP.

#### Period consolidation

>   A procedure that will total transaction detail into a single summary amount to be carried forward to the next period. This procedure is optional, and can be used if detailed information is no longer needed for a specific period.

#### Posting

>   A procedure to make temporary transactions a part of a business’s permanent records; to update accounts by transaction amounts. In manual accounting, posting transfers journal entries to the proper accounts in a general ledger.

#### Posting account

>   A financial account that tracks assets, liabilities, revenue, or expenses. These accounts will appear on the financial statements and other reports created in the financial series.

#### Posting journal

>   A report printed following the posting process that shows the detail for each transaction that has been posted. Posting journals also include the audit trail code, which is a precise record of where each transaction has been posted within Microsoft Dynamics GP.

#### Prior period adjustment

>   An adjustment for an error that was not discovered during the fiscal period in which it occurred.

>   Prior period adjustments should be reported as an adjustment to the retained earnings balance at the beginning of the period in which the correction was made.

#### Profit and loss account

>   Revenue or expense accounts whose balances – which determine the net income or net loss for the year – will be transferred to a retained earnings account at the end of a fiscal year.

#### Profit and Loss Statement

>   A financial statement showing revenue earned by a business, the expenses incurred in earning that revenue, and the resulting net income or net loss.

#### Quick financial setup

>   A method of creating financial statement layouts. Once the layouts have been created, they can be used to create report options.

#### Quick journal

>   A General Ledger journal that can be used to speed data entry for routinely recorded transactions. All the accounts typically used in a particular quick journal are selected when the quick journal is set up; as a result, only amounts must be entered when transactions are recorded.

#### Ratio

>   The quotient when one amount is divided by another, such as when the balance in a column is divided by the balance of a unit account.

**Real-time posting**

>   *See Transaction-level posting*.

#### Reconciling

>   A procedure used to recalculate account totals in the Chart of Accounts so they'll match transaction amounts that have been posted.

#### Record

>   A collection of related fields within a table. Records typically comprise most or all of the data entered in the fields in a given window. For instance, all the information entered about a specific account in the Account Maintenance window makes up a single record. A single transaction entered in the Transaction Entry window also constitutes a record.

#### Recurring batch

>   A batch that will be posted repeatedly, according to the selected frequency. An example of a recurring batch would be one to record monthly rent expense.  In Australia and New Zealand, transactions entered in a recurring batch are referred to as *standing transactions*.

#### Removing history

>   A procedure used to erase ranges of account or transaction history. Removing history will remove ranges of history that are no longer useful, making additional hard disk space available.

#### Report option

>   A collection of entries that specify the amount of information or the type of information that will appear on a report. Multiple report options can be created.

#### Retained earnings

>   The balance of the owners’ equity that is being retained in the business or corporation.

#### Retained earnings account(s)

>   Account(s) to which the balances of currentyear profit and loss accounts will be transferred during the year-end closing.

#### Reversing entry

>   A transaction that reverses the debit and credit entries of a previously posted adjusting entry. Reversing entries also can be used to correct an erroneous transaction that already has been posted.

#### Sample data

>   Data that can be used to practice Microsoft Dynamics GP procedures by entering the information listed in the online lessons. Sample data can be accessed using the lesson company.

**Segment number**

>   *See Account segment number*.

#### Series

>   A group of Microsoft Dynamics GP modules that form an interrelated set of applications. The Financial series, for example, contains  General Ledger, Advanced Financial Analysis, and other modules that collect and analyze transaction information from other modules.

#### Series posting

>   A posting process in which marked batches from the same series can be posted simultaneously.

#### Setup reports

>   A General Ledger report type that can be used to create report options for an Account Category List, Account Segment List, Setup List, and Quick Journal Setup List. The information on these reports is entered when the General Ledger module is set up initially.

#### Setup routine

>   A series of procedures that can be used to open the windows where options and defaults for a specific module are modified or set up.

#### Single-use batch

>   A batch that is created, posted once and then deleted from the system automatically.

#### Sorting

>   A method of arranging data based on the order of specified information. For example, records sorted by class would list all records within a class before moving to records in the next class.

#### Sorting segment

>   Segments of posting accounts that can be used for Microsoft Dynamics GP reports. Sixteen sorting segments can be used: seven are predefined and the remaining nine can be selected by the user.

#### Source document code

>   A code that identifies the type of journal or entry that can be examined for more information about a specific transaction. For example, the source document code, GJ, could be used for general journal entries, while BBAL could be used for beginning balance entries.

#### Standing transactions

>   *See Recurring batch*.

#### Statement of Cash Flows

>   A financial statement that provides information about the cash receipts and cash payments of a business over a specified period of time. The system uses the indirect method for calculating and printing the Statement of Cash Flows. This method indirectly reports the amount of net cash flow from operating activities by reconciling net income to net cash flow.

#### Statement of Retained Earnings

>   A financial statement that provides an analysis of retained earnings, including net income, declared dividends, and the ending balance of the retained earnings account for the period being reported.

#### Subsidiary ledger

>   A group of accounts other than General Ledger accounts that show the details underlying the balance of a controlling account in the General Ledger. Examples of subsidiary ledgers are customer accounts and vendor accounts.

#### Summarized report

>   A report where the amounts from an account range or category are printed in a single line.*See also Detailed report*.

#### Tab-delimited fields

>   A tab-separated ASCII character file format used when exporting a report so that it can be read by programs that use this format.

#### Text-only format

>   A file format that saves reports as text without formatting. This format is used when exporting reports to applications that are unable to read other formats available in Microsoft Dynamics GP.

#### Transaction

>   An event or condition that is recorded in asset, liability, expense, revenue, and/or equity accounts. Sales to customers or purchases from vendors are examples of transactions.

**Transaction history**

>   A record of transactions for a historical year.

#### Transaction matching

>   The process of linking related transaction distributions from different journal entries. For example, you can link period-end adjusting entries to the original transactions, or link a set of transactions associated with a project.

#### Transaction-level posting

>   A posting method in which transactions can be entered and posted without having to create a batch. Also known as *real-time posting*. *See also Batch posting*.

#### Trial balance reports

>   A General Ledger report type from which report options for a detailed trial balance, summary trial balance, or trial balance worksheet can be created. Trial balances are used to illustrate that debits equal credits for a range of accounts.

#### Typical balance

>   The type of balance, either debit or credit, that an account has under ordinary circumstances. Asset and expense accounts normally have debit balances, while liability, revenue, and equity accounts normally have credit balances.

#### Unit account

>   An account that tracks statistical or nonfinancial quantities, such as the number of customers with past-due balances or the number of invoices generated over a specific time period.

#### Variable allocation account

>   An account used to distribute fluctuating percentages of a single transaction to several different accounts.

#### Variance

>   The difference between two amounts, such as balances in two columns, when one is subtracted from the other. A common variance compares budgeted amounts to actual balances.

#### Year-end closing

>   A process used to calculate retained earnings for the year, transfer all current-year information for each account in the chart of accounts to account and transaction history and to prepare the accounting system for a new fiscal year.
