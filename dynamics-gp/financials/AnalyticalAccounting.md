---
title: "Analytical Accounting in Microsoft Dynamics GP"
description: "Examine how analytical accounting works in Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 05/13/2019
---

# Microsoft Dynamics GP Analytical Accounting

Analytical Accounting is a tool that helps you to analyze, interpret, and create
reports based on your company’s chart of accounts.

Using Analytical Accounting, you can better assess your company’s accounts. You
can also store information which cannot be computed in monetary terms such as
labour hours. You can enter detailed analysis information without resorting to
segmental accounting. You can create budgets using analysis dimensions and
compare your actual figures with budgeted figures.

With Analytical Accounting, you can:

-   Set up unlimited analysis dimensions.

-   Enter analysis information for a group of analysis dimensions.

-   Create budgets using the analysis dimensions you’ve set up.

-   Perform comprehensive reporting by exporting analysis queries to Microsoft
    Excel®.

*You must be using Excel 2000 or higher to export Analytical Accounting queries
to Excel.*

This manual is designed to give you an understanding of how to use the features
of Analytical Accounting, and how it integrates with the Microsoft Dynamics GP
system.

To make best use of Analytical Accounting, you should be familiar with
systemwide features described in the System User’s Guide, the System Setup
Guide, and the System Administrator’s Guide.

Some features described in the documentation are optional and can be purchased
through your Microsoft Dynamics GP partner.

To view information about the release of Microsoft Dynamics GP that you’re using
and which modules or features you are registered to use, choose Help \>\> About
Microsoft Dynamics GP.

>   The manual is divided into the following parts:

• *Part 1, Setup*, describes the set up tasks you need to complete to start
using

>   Analytical Accounting. It explains how to set up analysis codes and account

>   classes in order to enter analysis information. It also describes how you
>   can set up budgets for a group of analysis dimensions.

-   *Part 2, Transactions*, provides detailed information about entering and
    viewing analysis information for your transactions.

-   *Part 3, Routines, Inquiries and Reports*, describes how to perform queries
    for the analysis information you have entered and generate reports.

## Part 1: Setup

>   Use this part of the documentation to understand how you can start using
>   Analytical Accounting. The following information is discussed:

-   *Chapter 1, “Setup”* introduces you to Analytical Accounting and explains
    how to set it up for your company.

-   *Chapter 2, “Cards”* provides information about setting up analysis codes
    for Analytical Accounting.

-   *Chapter 3, “Budgets”* explains how to set up budget trees and assign
    budgets to nodes and account combinations. It also explains how you can
    export and import budgeted information to Excel.

### Chapter 1: Setup

>   The Analytical Accounting Setup wizard helps you complete the tasks required
>   to begin using Analytical Accounting. You can use the information here to
>   then specify Analytical Accounting options. You can set up posting options,
>   modify column headers, define fiscal years and set up the SmartList for
>   Analytical Accounting. You can also set default labels for the user-defined
>   fields to be used in analysis dimensions. You can specify whether
>   transactions can be posted with partial analysis information.

>   When you set up Analytical Accounting, you can open each setup window and
>   enter information, or you can use the Setup Checklist window (Administration
>   \>\> Setup \>\> Setup Checklist) to guide you through the setup process. See
>   your System Setup Guide (Help \>\> Contents \>\> select Setting up the
>   System) for more information about the Setup Checklist window.

*Analytical Accounting is not compatible with SQL Server® 7.0.*

>   This information is divided into the following sections:

-   *Analytical Accounting overview*

-   *Creating default records*

-   *Setting up posting options for Analytical Accounting*

-   *Activating Analytical Accounting*

-   *Assigning security roles and tasks to users*

-   *Setting up Analytical Accounting options*

-   *Modifying column headings for inquiries and reports*

-   *Defining fiscal years*

-   *Setting up SmartList integration*

-   *Setting up default user-defined fields for transaction dimensions*

-   *Setting up assignment options*

-   *Setting up user access to codes*

#### Analytical Accounting overview

>   The following flowchart shows you the sequence in which you will set up
>   Analytical Accounting, enter analysis information, and generate queries and
>   reports.

IMAGE – AAFLOW.jpg

![A close up of text on a white background Description automatically generated](media/2dbab2e22369c17bfba4f465a12f0249.jpg)

A close up of text on a white background Description automatically generated

#### Creating default records

>   After installing Analytical Accounting, you must run the Create Default
>   Record routine using the Analytical Accounting Setup wizard. You must run
>   this routine once, for each company registered in your Microsoft Dynamics GP
>   system.

*You must be logged in as SA or DYNSA to set up Analytical Accounting.*

>   **To create default records:**

1.  Open the Analytical Accounting Setup wizard window. (Administration \>\>
    Setup \>\> Company \>\> Analytical Accounting \>\> Setup)

>   The option Create Default Record is marked by default. This option is only
>   available if it has not already been completed.

1.  Choose Next to go to the Selected Option window, or choose Cancel to exit
    the setup process.

>   The tasks that will be performed are displayed in the Selected Option
>   window.

1.  Choose Finish to perform the tasks displayed. An arrow next to a task in the
    scrolling window indicates the progress of the tasks that are running. As
    each task is completed, a check mark appears next to it. If any error
    occurs, an error sign is displayed.

2.  Choose OK to close the window when all the tasks are completed.

#### Setting up posting options for Analytical Accounting

>   Once you’ve installed Analytical Accounting for your company, you must set
>   up the appropriate posting options for Analytical Accounting in the
>   Microsoft Dynamics GP Posting Setup window. Be sure that you’ve completed
>   this task before you activate Analytical Accounting,

>   In order to collect analytical information for an account, the account must
>   be linked to an account class. Analytical Accounting does not support
>   posting in summary. Therefore, you must ensure that each account in the
>   Account Maintenance window that you want to link to an account class has its
>   level of posting set to detail. Refer to *Linking accounts to an account
>   class* for information about linking accounts to an account class.

>   **To set up posting options for Analytical Accounting:**

1.  Open the Posting Setup window. (Administration \>\> Setup \>\> Posting \>\>
    Posting)

2.  Refer to the Microsoft Dynamics GP posting setup procedures (Help \>\>
    Contents \>\> Setting up the System) and (Help \>\> Contents \>\> Using the
    System) for information about setting up posting in Microsoft Dynamics GP.

3.  In the Posting Setup window, select the option Create a Journal Entry per
    Transaction or Batch. If you select Batch, mark the Use Account Settings
    option.

4.  Select Payroll in the Series field and All in the Origin field, and mark the
    Post in Detail option to post U.S. Payroll transactions in detail for all
    origins, except Period End Reports.

>   *You must mark this option to enter and view analysis information for U.S.
>   payroll transactions.*

>   Once Analytical Accounting is activated, you cannot select Create a Journal
>   Entry Per Batch without marking Use Account Settings. You also cannot unmark
>   the Use Account Settings option after Analytical Accounting has been
>   activated. However, you can change the posting option to Create a Journal
>   Entry per Transaction, or per Batch with Use Account Settings marked after
>   Analytical Accounting has been activated.

>   After Analytical Accounting has been activated, any account that has a level
>   of posting set to summary in the Account Maintenance window cannot be linked
>   to an account class. After you have linked an account to an account class,
>   you cannot change the level of posting from detail to summary in the Account
>   Maintenance window.

IMAGE – AAPOST.jpg

![A screenshot of a cell phone Description automatically generated](media/958244b7def8cb9a998113d0d029b72a.jpg)

A screenshot of a cell phone Description automatically generated

1.  Complete the setup procedures and choose OK or Save to save the posting
    setup.

#### Activating Analytical Accounting

>   You must activate Analytical Accounting in all the companies where it will
>   be used. The Activate Analytical Accounting routine can be accessed through
>   the Analytical Accounting Setup wizard.

>   You cannot enter or view analysis information for your transactions before
>   you activate Analytical Accounting. Also, the Smartlist folders that are
>   created for Analytical Accounting will not display any data until you have
>   activated Analytical Accounting.

>   You can, however, access Analytical Accounting Setup and Cards windows and
>   create necessary setup information such as transaction dimensions,
>   relations, and codes before activating Analytical Accounting.

>   *Before activating Analytical Accounting, you must have marked the
>   appropriate options in the Posting Setup window. Refer to Setting up posting
>   options for Analytical Accounting for more information.*

>   The process of activation will also ensure that the last updated balances in
>   your Microsoft Dynamics GP accounts are transferred to the Analytical
>   Accounting system tables.

>   **To activate Analytical Accounting:**

1.  Open the Analytical Accounting Setup wizard window. (Administration \>\>
    Setup \>\> Company \>\> Analytical Accounting \>\> Setup)

>   IMAGE – AAWIZ.jpg

![](media/a9c853b5106dbf1f470594504be1dca5.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Mark the Activate Analytical Accounting option to activate the product for
    the company you are logged into. If you have not registered Analytical
    Accounting, a message appears when you mark the option Activate Analytical
    Accounting prompting you to do so. Contact your Microsoft Dynamics GP
    representative for more information about registration.

>   The Activate Analytical Accounting option is available only if you’ve
>   created the default records for the company you are logged into. Refer to
>   *Creating default records* for more information.

1.  Choose Next to go to the next setup window which displays the tasks that are
    performed.

2.  Choose Finish to perform the tasks. An arrow next to a task in the scrolling
    window indicates the progress of the tasks that are running. As each task is
    completed, a check mark appears next to it. If any error occurs, an error
    sign is displayed.

3.  When all the tasks are completed, choose OK to close the window.

#### Assigning security roles and tasks to users

>   Individual security is role-based in Microsoft Dynamics GP. Each user must
>   be assigned to a security role before they can access any forms, reports, or
>   other data within Microsoft Dynamics GP. After installing Analytical
>   Accounting, the user must add the AA roles to each user, and add the AA
>   security tasks to the appropriate roles. If this is not done, the user will
>   not have access to any Analytical Accounting information.

>   To begin assigning user security, identify the daily tasks that a user
>   completes within Microsoft Dynamics GP. Then either select from the default
>   security roles or create new security roles that only grant access to the
>   tasks that the user needs.

>   For example, user ABC is an analysis manager for Fabrikam, Inc., and needs
>   access to set up and administer Analytical Accounting, enter or edit
>   transaction dimensions or perform other analysis tasks. Review the default
>   security roles in Microsoft Dynamics GP to find one that grants access to
>   the appropriate analysis functionality for user ABC. For our example, the AA
>   MANAGER\* security role is appropriate for user ABC. Use the User Security
>   Setup Window to assign the AA MANAGER\* security role to user ABC in the
>   Fabrikam, Inc. company.

>   The default security roles for Analytical Accounting are AA MANAGER and AA
>   CLERK. You can assign the following default security tasks to these roles.
>   You can also create new roles and tasks based on your requirement.

-   ADMIN_AA_001\*

-   CARD_AA_001\*

-   TRX_AA_001\*

-   INQ_AA_001\*

-   INQ_AA_002\*

-   RPT_AA_001\*

-   AADEFAULTUSER\*

-   ADMIN_AA_002\*

>   To specify security settings for specific tasks in Analytical Accounting,
>   use the

>   Security Task Setup window. (Administration \>\> Setup \>\> System \>\>
>   Security Tasks) To assign security tasks to the security roles, use the
>   Security Role Setup window (Administration \>\> Setup \>\> System \>\>
>   Security Roles) and grant access to the required windows, reports or files.
>   Refer to the System Setup documentation for more information on security in
>   Microsoft Dynamics GP.

#### Setting up Analytical Accounting options

>   You can set up posting, viewing, and deletion options in the Analytical
>   Accounting Options window.

>   **To set up Analytical Accounting options:**

1.  Open the Analytical Accounting Options window. (Administration \>\> Setup
    \>\> Company \>\> Analytical Accounting \>\> Options)

>   IMAGE – AAOPT.jpg

![](media/23357e8ca8d04ef1c6e196260e5d731b.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Mark the Post Cash Receipt deposits automatically in Bank Reconciliation
    option so that cash receipts entered in Receivables Management directly
    update the checkbook balance when posted. You will not be required to post
    the cash receipt again from the Bank Deposit Entry window (Transactions \>\>
    Financial \>\> Bank Deposits) in Bank Reconciliation if you mark this
    option.

2.  Mark the Post through to General Ledger for Transaction Posting option to
    directly update posting accounts when individually entered transactions are
    posted from the subsidiary modules. Batches are created during transaction
    posting in the subsidiary modules and automatically update the posting
    accounts after the individual transactions have been posted from these
    modules.

3.  Mark the Allow Deletion of Transaction Dimensions option to delete
    transaction dimensions that exist in posted transactions from the
    Transaction Dimension Maintenance window. Refer to *Defining transaction
    dimensions* for more information about deleting a transaction dimension.

>   *You can restrict users’ ability to delete a transaction dimension. To do
>   this, open the Security Setup window (Administration \>\>Setup \>\> System
>   \>\> Security) and deny access as necessary, to the Transaction Dimension
>   Maintenance window.*

1.  Mark the Show Inactive Trx Dim in Acct Class Maint window option to view the
    transaction dimensions that have been set to inactive in the Accounting
    Class Maintenance window. Refer to *Defining transaction dimensions* for
    more information about making a transaction dimension inactive.

2.  Mark the Show Inactive Trx Dim in Dim Relations window option to view the
    transaction dimensions which have been set to inactive in the Transaction
    Dimension Relations window. Refer to *Defining transaction dimensions* for
    more information about viewing inactive transaction dimensions.

3.  Mark the Enable Transaction Dimensions in Payroll (United States) option to
    enable transaction dimensions for transactions entered through the Payroll
    (United States) series. This option is available only if you have registered
    the Payroll module in the Registration window (Administration \>\> Setup
    \>\> System \>\> Registration). Refer to the Microsoft Dynamics GP
    documentation for more information.

>   *You must mark the Post in Detail option for the Payroll series in the
>   Posting Setup window before you can enable transaction dimensions in U.S.
>   Payroll.*

1.  Unmark the Allow special characters in Trx Dim./Codes option if you are
    using FRx® with Analytical Accounting. FRx does not support transaction
    dimension IDs or code IDs that contain special characters.

2.  Mark the Show valid code combinations in trns and budgets option if
    required. Selecting this option will display in the Code lookup window only
    those codes that have a valid combination with the codes that you have
    already selected for an analytical transaction or for a budget tree.

3.  Mark the Include dimensions in the year end close option to move analysis
    information to history in the year end close process. Refer to *Including
    Analytical Accounting in the year-end close process*.

4.  Mark the Enable Trx. Dimensions in Fixed Assets option to enable transaction
    dimensions for transactions entered through the Fixed Asset GL posting. This
    option is available only if you have registered for Fixed asset module in
    the Registration window (Administration \>\> Setup \>\> System \>\>
    Registration). Refer to the Microsoft Dynamics GP documentation for more
    information.

5.  Choose User-Defined to open the Analytical Default User-Defined Fields Setup
    window. Refer to *Setting up default user-defined fields for transaction
    dimensions* for more information.

6.  Choose Column Heading to open the Column Maintenance window. Refer to
    *Modifying column headings for inquiries and reports* for more information.

7.  Choose Reporting Periods to open the Reporting Periods window. Refer to
    *Defining fiscal years* for more information.

8.  Choose Smart List Integration to open the Smart List Integration window.
    Refer to *Setting up SmartList integration* for more information.

9.  Click the printer icon button to print the Company Options report.

10. Choose Redisplay to revert to the last saved information in the scrolling
    window.

11. Choose OK to save the changes made to the window and close the window.

12. Choose Cancel to close the window without saving the changes.

#### Modifying column headings for inquiries and reports

>   Analytical Accounting uses pre-defined columns to classify information in
>   the Multilevel Query wizard. You can modify the column header and column
>   description information for each column. Columns are created for actual
>   figures, budgeted figures and variances. Refer to *Creating and running a
>   multilevel query* for more information about multilevel queries.

>   You cannot create or delete any column in this window.

>   **To modify column headings for inquiries and reports:**

1.  Open the Column Maintenance window. (Administration \>\> Setup \>\> Company
    \>\> Analytical Accounting \>\> Options \>\> Column Heading button)

2.  The Column Description field displays the description of the column. Select
    the description and enter a unique column description, if needed.

3.  The Column Header field displays the standard header as a brief description
    for the column. Enter a unique column header, if needed.

4.  The column type and column data type will be displayed when you click the
    show button. You cannot modify this information. The columns types are
    Standard-Debit, Standard-Credit, Standard-Budget, and Standard-Variance

5.  Choose Load Defaults to insert the default column description and header
    information.

6.  Choose the printer icon button to print all the column definitions.

7.  Choose Redisplay to update the window by displaying any new information
    since you last modified the column headings.

8.  Choose OK to close the window.

![A screenshot of a cell phone Description automatically generated](media/b5a63aac5022ab48480513880201f344.jpg)

A screenshot of a cell phone Description automatically generated

#### Defining fiscal years

>   The Reporting Periods window displays the calendar and fiscal definition for
>   the fiscal years that are set up in Microsoft Dynamics GP. While doing an
>   analysis or preparing a report, you can switch between the Calendar and
>   Fiscal view. The fiscal year can be viewed by date, week, period, quarter,
>   or half year.

>   **To define fiscal years:**

1.  Open the Reporting Periods window. (Administration \>\> Setup \>\> Company
    \>\> Analytical Accounting \>\> Options \>\> Reporting Periods button)

>   IMAGE – AARP.jpg

![](media/46c00ccd131fa40c67a4829d50636dbf.jpg)

>   A screenshot of a social media post Description automatically generated

1.  The Year field displays the current open year. Select a year from the fiscal
    years set up in Microsoft Dynamics GP. The Fiscal View and the Calendar view
    columns display information for the selected year.

2.  Choose the printer icon button to print the settings for the selected year.

3.  Choose OK to close the window.

#### Setting up SmartList integration

>   You can add Analytical Accounting records to the SmartList using the
>   SmartList Integration window. All the records that you add to the SmartList
>   will also become available in the Report List (Reports \>\> Report List). In
>   the Report List window, choose Actions \>\> Add to My Reports, to open the
>   Add to My Reports window, where you can add a report to the My Reports list.
>   Refer to the Microsoft Dynamics GP documentation for more information on My
>   Reports.

>   Folders will be created at the root level in the SmartList for the following
>   type of records:

-   AA Accounting Classes

-   AA Distribution Queries

-   AA Multilevel Queries

-   AA Trees

-   AA Trx Dimension Codes

-   AA Trx Dimensions

-   AA Dimension Balances

-   Analytical Accounting Transactions

-   Asset ID

-   Book ID

>   If you choose to process a folder that already exists in the SmartList
>   Integration window, the Analytical Accounting records related to that folder
>   will be added to the relevant folder in the SmartList.

>   **To set up SmartList integration:**

1.  Open the SmartList Integration window.

>   (Administration \>\> Setup \>\> Company \>\> Analytical Accounting \>\>
>   Options \>\> SmartList Integration)

1.  Mark the options you want to create in the Install field. The Smart List
    Folder lists all the folders that you can install into a SmartList.

2.  If you mark a checkbox and choose Process, a folder will be created. For
    example, if you mark AA Trx Dimension and choose Process, a folder is
    created for transaction dimension in the SmartList that will display all the
    existing transaction dimensions.

>   If you unmark a checkbox that had been marked earlier, the folder will be
>   removed from the SmartList after you click Process.

1.  Choose Mark All to select all the folders in the scrolling window.

2.  Choose Unmark All to unmark all the folders in the scrolling window.

3.  Choose Process to add or remove the SmartList folders that you’ve selected.
    Choose OK when a message appears after the SmartList folders have been
    created.

4.  Choose Cancel to close the window without saving the changes made to the
    scrolling window.

#### Setting up default user-defined fields for transaction dimensions

>   Analytical Accounting allows you to enter labels for up to twenty
>   user-defined fields for each alphanumeric transaction dimension.
>   User-defined fields are of four types: Text, Numeric, Date and Checkbox. You
>   can define up to five fields of each type. You can use these fields to enter
>   additional information for each transaction dimension code that you’ve set
>   up. This information can be printed on the multilevel query report that you
>   generate for the transaction dimension code.

>   **To set up default user-defined fields for transaction dimensions:**

1.  Open the Analytical Default User-Defined Fields Setup window.
    (Administration \>\> Setup \>\> Company \>\> Analytical Accounting \>\>
    Options \>\> User-Defined button)

2.  Modify the label for each user-defined field if required. The system
    generated label for each user-defined field is the same as the field name.
    For example, the system generated label for Text Field 1 is Text Field 1.
    You cannot enter the same label in two fields. The label entered for each
    field is saved as soon as you move to another field in the window.

>   The labels you enter in this window will be the default labels for all
>   alphanumeric transaction dimensions that you’ve set up. You can change these
>   labels for each alphanumeric transaction dimension. Refer to *Setting up
>   userdefined fields per transaction dimension* for more information.

1.  Choose Load Defaults to clear all the values you’ve entered and revert to
    the system generated values.

2.  Choose the printer icon to print the Analytical Default User-Defined Fields
    Setup Report.

3.  Choose OK to close the window.

#### Setting up assignment options

>   You can specify if the distribution amount of an analytical account is to be
>   assigned fully or partially. You can post partially assigned transactions in
>   those modules where you allow partial assignments. By default Fixed Assets
>   will be unmarked during the upgrade. When Analytical accounting is activated
>   Fixed Asset will be marked by default on a new install or a new company.

>   **To set up assignment options:**

1.  Open the Assignment Setup window. (Administration \>\> Setup \>\> Company
    \>\> Analytical Accounting \>\> Assignment)

>   IMAGE – AAAS.jpg

![](media/c5e05edee133ee678d89245f744a14e1.jpg)

>   A screenshot of a cell phone Description automatically generated

>   All the Microsoft Dynamics GP modules that integrate with Analytical
>   Accounting are listed in the scrolling window. The Full option is marked for
>   all by default. This indicates that the distributions must be fully assigned
>   before you can post the transactions.

>   *In the case of Bank Management transactions, you can post a transaction
>   with partial assignments, if you’ve allowed partial assignments for the
>   module that you’re posting the Bank Management transaction to. The Inventory
>   module is not included since assignments are not allowed in this module.*

1.  Unmark the Full option for the modules where you want to allow partial
    assignments. If you allow partial assignments for a module, you can post a
    transaction even if the sum of assignments entered for an analytical account
    is not equal to the distribution amount of the analytical account.

>   You can mark and unmark this option at any time for each module. The options
>   that you have saved will apply to all un-posted and future transactions.

1.  Mark the option “No Warning When Partial Assignments Are Allowed” if you do
    not want to be warned while saving or posting partially assigned
    transactions. When this option is unmarked, you will be warned each time you
    save or post a partially assigned transaction. You can choose Yes on the
    message to continue saving or posting with partial assignments.

>   You can mark this option even when the Full option has been marked for all
>   modules. You can mark or unmark this option at any time.

1.  Choose the Redisplay button to revert to the last saved changes on the
    window.

2.  Choose OK to save your changes and close the window.

3.  Choose Cancel to close the window without saving any changes.

4.  Choose Print to print the Assignment Options report for the assignment
    options that you’ve saved for each module.

#### Setting up user access to codes

>   Use the User Access to Trx Dimension Codes window to specify which users
>   have permission to use transaction dimension codes in distributions and
>   adjustments. This will ensure that the analysis information at the time of
>   posting transactions or adjustments is entered only by users with the access
>   to use the required codes.

>   If you’re already using Analytical Accounting, then all existing users in
>   the company will have access to distribute and adjust all the existing
>   transaction dimension codes by default. However, when you create a new code,
>   you must specify the users who have permission to use that code in
>   transactions. Also, any new users that you create in the company must be
>   given access to the existing transaction dimension codes that they are
>   required to use.

>   *Security access to use a transaction dimension code is granted
>   automatically to the user who created the code during transaction entry.*

>   The user access that you set up is valid only for the company that you’re
>   logged into. To give users access to codes for another company, you must
>   login to that company and grant the required access.

>   You can specify user access only for codes belonging to alphanumeric
>   transaction dimensions. You can give access to users per transaction
>   dimension code, per user or per employee. If you are using Analytical
>   Accounting with Payroll (United States), the user provided with access to
>   employees can view, sort and filter analysis information in multilevel query
>   and distribution query reports.

>   *Users can still view the transaction dimension codes though they may not
>   have permission to distribute or adjust those codes.*

>   **To set up user access per transaction dimension code:**

1.  Open the User Access to Trx Dimension Codes window. (Administration \>\>
    Setup \>\> Company \>\> Analytical Accounting \>\> User Access)

>   The Type field displays Transaction Dimension as the default selection.  
>   IMAGE – AAUA.jpg

![A screenshot of a cell phone Description automatically generated](media/8d2566f79fcac71b9607c70cd9266f58.jpg)

A screenshot of a cell phone Description automatically generated

1.  Select an alphanumeric transaction dimension in the Transaction Dimension
    field. You can select an active or an inactive transaction dimension.

2.  Select the Transaction Dimension Code for which you want to set user access.

>   The scrolling window displays all the user IDs you’ve set up for the
>   company. You can add or remove users from the scrolling window.

1.  Mark the Distribute and Adjust options for the users to whom you want to
    give access to the selected code. Unmark these options for the users to whom
    you do not want to give access.

>   If you are already using Analytical Accounting, the Distribute and Adjust
>   options are marked by default for all existing users.

1.  In the Default Values for User ID field, mark the Distribute and Adjust
    options to give access to all the users displayed in the scrolling window.
    Unmark these options to remove access for all users displayed in the
    scrolling window.

2.  Choose Save to save your access settings and clear the window.

3.  Choose Clear to clear the window without saving changes.

4.  Choose Redisplay to revert to the last saved changes. The scrolling window
    will also display any new users that have been set up in the company since
    you opened this window.

>   **To set up user access per user:**

1.  Open the User Access to Trx Dimension Codes window. (Administration \>\>
    Setup \>\> Company \>\> Analytical Accounting \>\> User Access)

2.  Select User ID in the Type field.

3.  Select the user ID in the User ID field.

4.  Select an alphanumeric transaction dimension. You can select an active or
    inactive transaction dimension. The scrolling window displays all the
    transaction dimension codes belonging to the selected transaction dimension.
    You can add or remove codes from the scrolling window.

5.  Mark the Distribute and Adjust options for the codes to which you want to
    give access to the selected user. Unmark these options for the codes to
    which you do not want to give access.

>   If you are already using Analytical Accounting, the Distribute and Adjust
>   options are marked by default for all existing transaction dimension codes.

1.  In the Default Values for Trx Dimension Codes field, mark the Distribute and
    Adjust options to give access to all the codes displayed in the scrolling
    window. Unmark these options to remove access for all codes displayed in the
    scrolling window for the selected user.

2.  Choose Save to save your access settings and clear the window.

3.  Choose Clear to clear the window without saving changes.

4.  Choose Redisplay to revert to the last saved changes. The scrolling window
    will also display any new transaction dimension codes that have been set up
    in the company since you opened this window.

>   **To set up user access per employee:**

1.  Open the User Access to Trx Dimension Codes window. (Administration \>\>
    Setup \>\> Company \>\> Analytical Accounting \>\> User Access)

2.  Select Employee in the Type field.

3.  In the scrolling window, mark the View column for each corresponding User ID
    to which you want to grant permission to view, sort, and filter by employee
    ID on distribution and multilevel query reports.

4.  Choose Save to save your access settings and clear the window.

5.  Choose Clear to clear the window without saving changes.

6.  Choose Redisplay to revert to the last saved changes.

**Chapter 2: Cards**

>   You can set up various transaction dimensions, relationships between
>   alphanumeric transaction dimensions, transaction dimension codes, and valid
>   code combinations in order to enter analysis information. The process of
>   creating account classes and linking accounts to an account class in
>   Analytical Accounting also is explained. Information about trees and tree
>   structures, which are used in reporting, is also explained.

>   This information is divided into the following sections:

-   *Defining transaction dimensions*

-   *Setting up user-defined fields per transaction dimension*

-   *Setting transaction dimension relationships*

-   *Changing the order of transaction dimensions*

-   *Defining transaction dimension codes*

-   *Entering details for user-defined fields per code*

-   *Defining combinations between transaction dimension codes*

-   *Copying a transaction dimension code combination*

-   *Creating an alias*

-   *Copying an alias*

-   *Importing an alias*

-   *Format to import aliases*

-   *Setting up an account class*

-   *Linking accounts to an account class*

-   *Linking accounts to classes and nodes*

-   *Setting up account access to codes*

-   *Entering analysis information for fixed assets transactions*

-   *Setting up trees*

-   *Defining a tree structure*

-   *Copying a tree structure*

-   *Linking master records to an existing tree structure*

-   *Adding master records to an existing tree*

#### Defining transaction dimensions

>   Use the following information to set up various types of transaction
>   dimensions. A transaction dimension is any transaction criterion that you
>   can classify, report and analyze for a period. A transaction dimension can
>   be Alphanumeric, Numeric, Yes/ No (Boolean) or Date Type. For example, you
>   can set up Cost Centre, Profit Centre, Country/Region, Billable or Hours as
>   transaction dimensions. You can define any number of transaction dimensions
>   according to your analysis or reporting requirements.

>   *If you are integrating Analytical Accounting with FRx, be sure that
>   transaction dimensions do not contain any special characters in them. Refer
>   to Setting up Analytical Accounting options for information on avoiding use
>   of special characters.*

>   **To define transaction dimensions:**

1.  Open the Transaction Dimension Maintenance window. (Cards \>\> Financial
    \>\> Analytical Accounting \>\> Transaction Dimension)

-   IMAGE – AATDM.jpg

![](media/b77da2c964d58d499e229a18e3091a31.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Enter the name of a transaction dimension.

>   *Note: Use a different name for the transation dimension other than the six
>   AA dimensions that already exist.*

1.  Mark Inactive if you do not want to enter analysis information for the
    transaction dimension during transaction entry. An inactivated transaction
    dimension cannot be used to create analysis information. Unmark the Inactive
    check box to activate a transaction dimension.

2.  Select the analysis type of the transaction dimension from the Data Type
    list. For example, an alphanumeric data type could be a profit centre of the
    company, numeric could be the quantity of units sold, boolean could be a
    billable or saleable item, and date type could be the date on which goods
    are dispatched.

>   The data type you select is used to determine the additional setup
>   information that you can or cannot create for a transaction dimension. It
>   also determines the type of analysis information that you can enter for the
>   transaction dimension. For example, if you select a data type of Numeric,
>   you can enter only numbers as analysis information.

1.  Enter the description for the transaction dimension in the Description 1
    field.

2.  Enter any additional descriptions for the transaction dimension in the
    Description 2 field.

3.  Keep the Create New Codes on the Fly option marked to create alphanumeric
    transaction dimension codes during transaction entry. This will allow you to
    open the Transaction Dimension Code Maintenance window (Cards \>\> Financial
    \>\> Analytical Accounting \>\> Transaction Dimension Code) to add a new
    alphanumeric transaction dimension code during transaction entry. Unmark the
    option if it is not required.

4.  Mark the Create New Codes in Background option to create new alphanumeric
    transaction dimension codes in the background during transaction entry.
    Selecting this option will automatically add the new code during transaction
    entry to the existing codes of the alphanumeric transaction dimension. This
    option is available only if you selected the Create New Codes on the Fly
    option.

>   *In the case of non-alphanumeric transaction dimensions, transaction
>   dimension codes are always created in the background.*

1.  Select the number of decimal places from the Decimal Places list to
    determine the number of decimal places that can be used for a numeric
    transaction dimension code. This field is available only if the data type of
    the transaction dimension is Numeric.

2.  Select the U of M Schedule ID to link a Unit of Measure ID to a Numeric
    transaction dimension. The base unit is displayed beside the numeric
    transaction dimension code during transaction entry. This field is available
    only if the data type of the transaction dimension is Numeric.

3.  Mark the Allow Adjustments option to allow the selected transaction
    dimension to be adjusted in the Analytical Adjustment Entry window. You can
    make adjustments only for transaction dimensions that have this option
    marked. You can mark or unmark this option at any time. Refer to *Adjusting
    analysis information in posted transactions* for more information on
    adjustments.

4.  Mark the Code Required During Adjustment option to make entering a code a
    required criteria during adjustment entry. You cannot post an adjustment
    until you enter a Transaction Dimension Code against the Transaction
    Dimension. This option is unmarked and not available if you’ve not marked
    Allow Adjustments.

5.  Mark the Include In Year End Close option to include the analysis
    information for alphanumeric transaction dimensions during the year end
    closing process. You must have also marked the Include In Year End Close
    option for the transaction dimension in the Analytical Accounting Options
    window.

6.  Choose User-Defined to open the Transaction Dimension User-Defined Fields
    Setup window. You can enter unique labels for each transaction dimension
    that you have set up.

7.  Choose Relations to open the Transaction Dimension Relations window. The
    Relations button is only available for alphanumeric transaction dimensions.
    Refer to *Setting transaction dimension relationships* for more information.

8.  Choose Order to open the Transaction Dimension Order window to change the
    order of the transaction dimensions that you’ve created. Refer to *Changing
    the order of transaction dimensions* for more information.

9.  Choose Codes to open the Transaction Dimension Code Maintenance window if
    the transaction dimension is alphanumeric. Refer to *Defining transaction
    dimension codes* for more information.

10. Choose the Print drop-down list to print setup details of the transaction
    dimension currently displayed or all the transaction dimensions that you
    have created.

11. Choose Save to save the details that you have entered for the transaction
    dimension.

12. Choose Clear to clear the window.

13. Choose Delete to delete a transaction dimension with all its codes and
    relations, if applicable. You cannot carry out any inquiries for transaction
    dimensions that have been deleted.

>   If you have created a query or queries using the Distribution Query wizard
>   or Multilevel Query wizard, you cannot delete a transaction dimension that
>   has been saved in such query or queries. Refer to *Chapter 17,
>   “Inquiries”*for more information about queries. You also cannot delete a
>   transaction dimension that is used in a budget tree ID.

>   You can delete a transaction dimension that exists in posted transactions
>   only if you have selected the Allow Deletion of Transaction Dimensions
>   option in the Analytical Accounting Setup window (Administration \>\> Setup
>   \>\> Company \>\> Analytical Accounting \>\> Setup).

#### Setting up user-defined fields per transaction dimension

>   You can change the default labels you’ve set up in the Analytical
>   User-Defined Setup window, and assign unique labels for each alphanumeric
>   transaction dimension.

>   **To set up user-defined fields per transaction dimension:**

1.  Open the Transaction Dimension User-Defined Fields Setup window. (Cards \>\>
    Financial \>\> Analytical Accounting \>\> Transaction Dimension
    \>\>User-Defined button)

>   The transaction dimension and description are displayed in the Transaction
>   Dimension and Description fields.

1.  Modify the label for each user-defined field if required. You cannot enter
    the same label in two fields. The label entered for each field is saved as
    soon as you move to another field in the window.

>   The values you enter in this window will be the user-defined field names for
>   all transaction dimensions codes belonging to the selected transaction
>   dimension. You can enter details for each field code in the Transaction
>   Dimension Code User-Defined Fields Maintenance window. Refer to *Entering
>   details for userdefined fields per code* for more information.

1.  Choose Load Defaults to clear all the values you’ve entered and revert to
    the values entered in the Analytical Default User-Defined Fields Setup
    window.

2.  Choose the printer icon to print the Transaction Dimension User-Defined
    Fields Setup Report.

3.  Choose OK to close the window.

#### Setting transaction dimension relationships

>   The following information explains the various kinds of relationships that
>   you can set up between alphanumeric transaction dimensions. You can create a
>   relationship of ownership between alphanumeric transaction dimensions where
>   a transaction dimension is owned or owns another transaction dimension. For
>   example, you can set the relationship between profit centre P1 and cost
>   centre C1 as: P1 owns C1. You can create other combinations as well in the
>   Transaction Dimension Relations window. Setting up relationships will also
>   ease data entry.

>   **To set transaction dimension relationships:**

1.  Open the Transaction Dimension Relations window.

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
>   Relation)

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
>   \>\> Relations button)

1.  Enter or select an alphanumeric transaction dimension. The scrolling window
    displays all the other alphanumeric transaction dimensions that you have
    created except the transaction dimension that you have selected.

>   Inactive alphanumeric transaction dimensions will be displayed in the

>   Transaction Dimension Relations window if you have marked the Show Inactive
>   Trx Dim in Dim Relations window option in the Analytical Accounting Setup
>   window.

1.  Select the type of relationship to establish between the selected
    transaction dimension and the other transaction dimensions displayed from
    the Relation List. You can set the relationship between transaction
    dimensions to one of the following options in the Relation list:

>   **All combinations allowed** All code combinations between two transaction
>   dimensions are permitted. For example, if the transaction dimensions profit
>   centre and cost centre are set to a relationship of All Combinations Allowed
>   then any profit centre code can be used with any cost centre code.

>   **Combination not allowed** Code combinations between two transaction
>   dimensions are not permitted. For example, transaction dimension profit
>   centre and cost centre set to a Combination relationship is not allowed;
>   then code combination between these transaction dimensions is not allowed.

>   If you set the relationship between two alphanumeric transaction dimensions
>   to Combination not allowed, you cannot use both the transaction dimensions
>   at the same time for analysis during transaction entry.

>   **Is owned by** Where the selected alphanumeric transaction dimension is
>   owned by another alphanumeric transaction dimension. For example, cost
>   centre C1 is owned by profit centre P1.

>   **Owns Trx Dimension** where the selected alphanumeric transaction dimension
>   owns another alphanumeric transaction dimension.

>   **Example**

>   Suppose that factory X (which is a cost centre) manufactures only Product Y
>   (which is a profit centre). You can create a relationship where the cost
>   centre owns the profit centre. This will ensure that all analysis
>   information entered for the expenses incurred by the cost centre
>   automatically will be picked up for the profit centre.

>   An alphanumeric transaction dimension can own only one alphanumeric
>   transaction dimension. Additionally, an alphanumeric transaction dimension
>   cannot be owned by more than one alphanumeric transaction dimension at a
>   time.

>   The relationships Is owned by and Owns Trx Dimension require combinations to
>   be set between the codes of the owning and owned alphanumeric transaction
>   dimensions. For example, factory X (cost centre) manufactures only Product Y
>   (profit centre). You would have to create a combination where a code of the
>   cost centre, factory X, owns a code of the profit centre, Product Y.

>   While creating analysis information, the code of the owned transaction
>   dimension will derive the relevant code of the owning transaction dimension.
>   For example, if you enter Product Y while entering analysis information, it
>   will derive the code Factory X, as you have created a combination between
>   the codes Factory X and Product Y.

>   The code of an owning transaction dimension can own any number of codes of
>   the owned transaction dimension. However, a code of the owned transaction
>   dimension can be assigned to only one code of the owning transaction
>   dimension at a time.

>   You can set the code combination while creating codes in the Trx Dimension
>   Code Maintenance window or in the Transaction Dimension Code Validation
>   window.

>   If you delete a transaction dimension that owns another transaction
>   dimension, the codes of the owning transaction dimension also will be
>   deleted. The relevant codes of the owned transaction dimension will now not
>   be owned by any code.

>   An alphanumeric transaction dimension that has been set to Inactive, cannot
>   own any other alphanumeric transaction dimension. However, the owned
>   alphanumeric transaction dimension can be inactive.

>   The code or codes of an owning transaction dimension must be active before
>   you create a combination with code or codes of the owned transaction
>   dimension.

>   **Valid subset** Certain code combinations between two transaction
>   dimensions are permitted. This relation allows you to restrict the code
>   combinations.

>   **Example**

>   Sales Zone A is a Revenue Centre. There are products X, Y and Z. Revenue
>   Centre A sells only Products X and Y, which are set as a Profit Centre. You
>   can specify that Revenue Centre is a valid subset of Profit Centre and
>   create a valid code combination of A with X and Y. This will ensure that
>   where Revenue Centre and Profit Centre are used together while entering
>   analysis information, A can be used only with X and Y or vice versa.

>   You can set the code combinations between the transaction dimensions in the
>   Transaction Dimension Code Validation window.

1.  Choose the Show as Tree button to open the Transaction Dimension Dependency
    (Relation) Inquiry window where the transaction dimensions are displayed in
    the form of a tree. Refer to *Chapter 17, “Inquiries”*for more information.

2.  Choose Save to save the changes you’ve made.

3.  Choose Clear to clear the window.

4.  Choose Redisplay to revert to the information last displayed in the window.
    The window also will display any other alphanumeric transaction dimensions
    that have been created by other users while you were setting up
    relationships.

#### Changing the order of transaction dimensions

>   You can change the order in which the transaction dimensions will appear
>   during transaction entry and inquiry windows using the Transaction Dimension
>   Order window. The relevant transaction entry or inquiry window displays the
>   transaction dimensions in the order that is specified in the Transaction
>   Dimension Order window.

>   **To change the order of transaction dimensions:**

1.  Open the Transaction Dimension Order window.

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
>   Order)

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
>   \>\> Order Button

IMAGE – AATDO.jpg

![A screenshot of a cell phone Description automatically generated](media/91397a73c7152b7226d90a03cfe0fcc5.jpg)

A screenshot of a cell phone Description automatically generated

1.  The transaction dimensions and their descriptions are displayed in the
    scrolling window in the order they were created.

    -   Choose the Move to Top button to shift a selected item to the top of the
        list.

    -   Choose the Move Up button to shift a selected item one line up in the
        list window.

    -   Choose the Move Down button to shift a selected item one line down in
        the list window.

    -   Choose the Move to Bottom button to shift a selected item to the bottom
        of the list window.

2.  Choose Save to save changes you’ve made.

3.  Choose Cancel to close the window without saving the changes.

#### Defining transaction dimension codes

>   Use the following information to define alphanumeric transaction dimension
>   codes. Transaction dimension codes are the defined values of transaction
>   dimensions that you enter during transaction entry and for which analysis
>   information is collected.

>   *If you are integrating Analytical Accounting with FRx, be sure that
>   transaction dimension codes do not contain any special characters in them.
>   Refer to Setting up Analytical*

>   *Accounting options for information on avoiding use of special characters.*

>   **To define transaction dimension codes:**

1.  Open the Transaction Dimension Code Maintenance window.

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
>   Code)

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
>   \>\> Codes button)

IMAGE – AATDC.jpg

![A screenshot of a cell phone Description automatically generated](media/b004c60791e288c4dc797dd20196af0c.jpg)

A screenshot of a cell phone Description automatically generated

1.  Enter or select an alphanumeric transaction dimension in the Trx Dimension
    field.

2.  Enter a code in the Trx Dimension Code field. For example, if your
    manufacturing units are Cost Centres, you can enter the location of a
    manufacturing unit, say Fargo, as a Cost Centre code.

>   If a transaction dimension owns another transaction dimension, you first
>   need to create the codes for the owning transaction dimension. For example,
>   if a Profit Centre owns a Cost Centre, then you have to first create codes
>   for the Profit Centre.

>   At least one active code must exist for an owning transaction dimension
>   before you begin to create combinations with the codes of the owned
>   transaction dimension. You cannot delete the last remaining code of the
>   owning transaction dimension if codes exist for the owned transaction
>   dimension.

>   *You must grant access to users to use this code in the User Access to Trx
>   Dimension Codes window. However, security access to use a transaction
>   dimension code is granted automatically to the user who created the code
>   during transaction entry.*

1.  Enter the description for the transaction dimension code in the Description
    1 field.

*Two transaction dimension codes cannot have the same description.*

1.  Enter any additional description for the transaction dimension code in the
    Description 2 field.

2.  Mark Inactive if you do not want to use the transaction dimension code to
    create analysis information. To use the transaction dimension code during
    transaction entry, you must unmark the Inactive check box.

>   You cannot inactivate the following codes:

-   An alphanumeric transaction dimension code that owns another alphanumeric
    transaction dimension code. This will be applicable even if the owned
    alphanumeric transaction dimension code is inactive.

-   A transaction dimension code that has been set as a default for a Fixed or
    Hidden Alphanumeric transaction dimension. The code must be removed as a
    default before it is inactivated. Refer to *Setting up an account class* for
    more information about default codes and Fixed and Hidden transaction
    dimensions.

>   You can inactivate the following codes:

-   The default codes of the Required or Optional Alphanumeric transaction
    dimensions. When you inactivate transaction dimension codes, they will be
    removed from the relevant account class in the Accounting Class Maintenance
    window. Refer to *Setting up an account class* for more information about
    account classes.

>   You can create codes for inactive alphanumeric transaction dimensions, but
>   you can use these codes only if the transaction dimension is activated.

1.  In the Linked to Node field, select a node for the specific transaction
    dimension code as each code has to be linked to a valid node of the Main
    Tree.

2.  A Main Tree is created by default for each Alphanumeric Transaction
    Dimension that you create. You can create an unlimited number of additional
    trees. You can also create a new node from the Linked to Node field. Refer
    to *Setting up trees* for more information.

3.  In the Owned By field, select a code of the transaction dimension that will
    own the transaction dimension code you are creating. This field is available
    only if a transaction dimension is owned by another transaction dimension.

4.  Choose Code Validation to open the Trx Dimension Code Validation window
    where you can set valid combinations between transaction dimension codes of
    the selected alphanumeric transaction dimension and the other existing
    alphanumeric transaction dimensions. Refer to *Defining combinations between
    transaction dimension codes* for more information.

>   Where transaction dimensions are valid subsets, you can create valid code
>   combinations between inactive transaction dimension codes. However, these
>   codes cannot be used till they have been activated. Refer *Setting
>   transaction dimension relationships* for more information about valid
>   subsets.

1.  Choose User-Defined to open the Transaction Dimension Code User-Defined
    Fields Maintenance window, where you can enter values for the user-defined
    fields you have set up.

2.  Choose the printer icon button to print a report for the details you have
    set up for the codes of the transaction dimension currently displayed or for
    all alphanumeric transaction dimensions.

3.  Choose Save to save the changes you’ve made.

4.  Choose Clear to clear the entries you’ve made.

5.  Choose Delete to remove the transaction dimension code displayed. You cannot
    delete a transaction dimension code if you have used it in any posted
    transaction. To delete such a transaction dimension code, you will have to
    delete the transaction dimension that the code belongs to.

>   You cannot delete a transaction dimension code if it is used as a default
>   code of a fixed alphanumeric transaction dimension in the Accounting Class
>   Maintenance window. You also cannot delete a transaction dimension code that
>   is used in a budget tree ID.

>   If you delete a code that owns another code, the code that is owned will be
>   automatically assigned to the next available code of the owning alphanumeric
>   transaction dimension.

#### Entering details for user-defined fields per code

>   Once you’ve entered labels for the user-defined fields that you want to use,
>   you can enter details for each field in the Transaction Dimension Code
>   User-Defined Fields Maintenance window. You can enter different details for
>   each code that you have set up.

>   **To enter details for user-defined fields per code:**

1.  Open the Transaction Dimension Code User-Defined Fields Maintenance window.
    (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
    Code \>\> User-Defined button)

>   The Transaction Dimension, and Transaction Dimension Code fields display the
>   selected code for which you’re entering user-defined information.

1.  Enter the necessary values in the user-defined text, numeric, and date
    fields.

2.  Mark the required checkbox fields.

3.  Choose OK to close the window. You must choose Save on the Transaction
    Dimension Code Maintenance window in order to save the values you’ve
    entered.

4.  Choose the print icon on the Transaction Dimension Code Maintenance window
    to print the Transaction Dimension Code Maintenance report along with the
    details for user-defined fields.

#### Defining combinations between transaction dimension codes

>   You can set combinations between the transaction dimension codes of

>   alphanumeric transaction dimensions that you have created, using the
>   Transaction Dimension Code Validation window. These combinations are
>   verified during transaction entry while entering analysis information and
>   therefore, you can’t enter code combinations that aren’t valid. In addition,
>   if the combination between two transaction dimension codes isn’t valid, it
>   will not pass the validation routine in Analytical Accounting.

>   The combination between the transaction dimension codes only can be set if
>   transaction dimensions are alphanumeric. You cannot define a code
>   combination if the relationship between the two transaction dimensions is
>   set to Combination not Allowed or All combinations allowed.

>   You can change the ownership between the transaction dimension codes in this
>   window.

>   **To define combinations between transaction dimension codes:**

1.  Open the Transaction Dimension Code Validation window. (Cards \>\> Financial
    \>\> Analytical Accounting \>\> Transaction Dimension Code Validation)

>   IMAGE – AATDCV.jpg

![](media/f2d7f8bae3aa9d51e6eb1ab5a56b1a94.jpg)

>   A screenshot of a social media post Description automatically generated

1.  In the Trx Dimension field, select a transaction dimension. All the
    transaction dimension codes that you’ve created for the selected transaction
    dimension are displayed in the left scrolling window. The Trx Dimension Code
    column displays the name that you have assigned to the transaction dimension
    code in the Transaction Dimension Code Maintenance window. The Description
    column displays the description of the transaction dimension code created in
    the Transaction Dimension Code Maintenance window.

2.  In the Related Trx Dimension field, select the transaction dimension that
    you will use to create a code combination. A related transaction dimension
    is one that is owned by or is a valid subset of the transaction dimension
    selected in the Trx Dimension field.

>   All the codes of the related transaction dimension will be displayed in the
>   right scrolling window. If the relationship between the transaction
>   dimensions is that of ownership, the combination between the codes of the
>   owned and owning transaction dimensions that you have entered in the
>   Transaction Dimension Code Maintenance window will be displayed.

1.  To create a valid code combination between transaction dimensions that are
    valid subsets or in the case of ownership, select and mark a code for both
    the transaction dimensions and the related transaction dimension. You can
    select only one code at a time from the transaction dimension and related
    transaction dimension. The codes you have marked will constitute a valid
    combination.

>   For example, if you have selected Cost Centre in the Transaction Dimension
>   field and Profit Centre in the Related Transaction Dimension field (which
>   are valid subsets), you can create a valid code combination between the code
>   C1 of Cost Centre and P1 of Profit Centre. Mark C1 and P1 in the scrolling
>   window to create the combination. You also can mark C1 and P2 or C2 and P1,
>   thereby creating unlimited valid code combinations.

1.  In the Related Transaction Dimension field, you also can select a
    transaction dimension where the relationship that exists is Combination Not
    Allowed or All Combination Allowed. However, you can’t select any codes of
    these transaction dimensions.

2.  The Inactive field displays the alphanumeric transaction dimensions that
    have been inactivated.You can create combinations between the codes of
    inactive alphanumeric transaction dimensions that are valid subsets.

3.  Choose Save to save a code combination.

4.  Choose the printer icon button to print a report displaying the code
    combinations of the transaction dimension code that is highlighted in the
    left scrolling window with the codes of the related transaction dimension.
    You can also print a report displaying the code combinations between all
    codes of the transaction dimension with the codes of the related transaction
    dimension.

5.  To interchange the transaction dimensions between the left and right
    scrolling windows, choose Switch.

6.  Choose Clear to clear the information from the window.

7.  Choose Redisplay to revert to the information last displayed and to display
    any other transaction dimension codes that have been created while you were
    setting code relationships.

8.  Choose Copy to open the Copy Transaction Dimension Code Validation Copy
    window. Refer *Copying a transaction dimension code combination* 40 for more
    information.

9.  Choose Mark to mark the code that has been selected from the right scrolling
    window.

10. Choose Unmark to unmark the code selected from the right list window.

#### Copying a transaction dimension code combination

>   You can copy one, all, or a subset of the related transaction dimension code
>   combinations in the Transaction Dimension Code Validation window to the
>   transaction dimension codes of another transaction dimension using the Copy
>   Transaction Dimension Code Combinations window. Copying is only possible if
>   the relation between the two transaction dimensions is set to Valid Subset
>   in the Transaction Dimension Relations window. Refer *Setting transaction
>   dimension relationships* for more information.

>   **Example**

>   Sales Zone A is a Revenue Centre. Sales Zone A sells only two products, X
>   and Y.

>   You’ve defined Products as Profit Centres. In the Transaction Dimension Code

>   Validation window, you have created a combination between Sales Zone A and
>   Products X and Y. Using the Copy button, you can create the same combination
>   with any other sales zone, say Sales Zone B.

>   You must select a code of the related transaction dimension in the
>   Transaction Dimension Code Validation window before opening the Copy
>   Transaction Dimension Code Combination window. A transaction dimension code
>   will be selected automatically when you select a code for the related
>   transaction dimension.

>   **To copy a transaction dimension code combination:**

1.  Open the Copy Transaction Dimension Code Combinations window. (Cards \>\>
    Financial \>\> Analytical Accounting \>\> Transaction Dimension Code
    Validation \>\> Copy button)

>   The Copy from Trx Dimension field displays the source that the code
>   combination will be copied from. The source always will be the related
>   transaction dimension that is displayed in the Transaction Dimension Code
>   Validation window.

>   The Copy to Trx Dimension field displays the destination to which the code
>   combination must be copied. The destination always will be the transaction
>   dimension displayed in the Transaction Dimension Code Validation window.

1.  All the transaction dimension codes of the Copy to Trx Dimension, except for
    the code selected in the Transaction Dimension Code Validation window, will
    be displayed. All codes displayed in the scrolling window will be
    automatically selected.

>   You can select one, all or a subset of transaction dimension codes to copy
>   to the code combination. Press SHIFT+CTRL to select more than one
>   transaction dimension code from the list window.

1.  Choose Copy to start the process of copying the transaction dimension code
    combinations to the codes you have selected. The window will close as soon
    as the copying process is complete.

2.  After the process has been completed, a combination is created between Sales
    Zone B and Products X and Y.

3.  Choose Cancel to close the window. The code combination will not be copied
    to the codes you have selected in the window.

#### Creating an alias

>   You can create aliases to group the transaction dimension code combinations
>   that you use while entering analysis information for transactions. Aliases
>   allow you to enter large amounts of analysis information quickly and
>   accurately during transaction entry. When you use an alias, the codes
>   associated with the alias default for the account. You can also change the
>   default transaction dimension codes for the alias during transaction entry.
>   You can create multiple aliases with different combinations of transaction
>   dimension codes. Refer to *Entering analysis information for General Ledger
>   transactions* for more information.

>   **To create an alias:**

1.  Open the Alias Maintenance window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Alias)

2.  Enter a name, description, and a short description for the alias that you
    are setting up.

>   The scrolling window displays all the alphanumeric transaction dimension
>   codes that you have set up.

1.  Mark the Inactive checkbox to inactivate the alias displayed in the window.
    You cannot use an inactive alias during transaction entry.

2.  Select a transaction dimension code for each transaction dimension to
    include in the alias.

3.  Choose Save to save the alias you have set up.

4.  Choose Clear to clear the values, or Delete to delete the alias displayed in
    the window.

5.  Choose Copy to copy the transaction dimension codes from an existing alias
    to set up another alias. Refer to *Copying an alias* for more information.

6.  Choose Import to import the transaction dimension codes from an Excel
    application to the alias. Refer to *Importing an alias* for more
    information.

#### Copying an alias

>   You can copy an existing alias to set up another alias and modify it as
>   required. The transaction dimension codes from the existing alias are copied
>   to the new alias. You can add or delete transaction dimension codes in the
>   new alias.

>   **To copy an alias:**

1.  Open the Copy Alias window. (Cards \>\> Financial \>\> Analytical Accounting
    \>\> Alias \>\> Select an alias \>\> Copy button)

>   The Copy from Alias field displays the alias you selected in the Alias
>   Maintenance window.

1.  Enter an alias name to copy to in the Copy to Alias field.

2.  Enter a description and a short description for the new alias.

3.  Choose Copy to copy the transaction dimension codes to the new alias.

4.  Choose Cancel to cancel the process and close the window.

#### Importing an alias

>   You can import alias information from an Excel spreadsheet that has been set
>   up in the required format. Refer to *Format to import aliases* for more
>   information.

>   **To import an alias:**

1.  Open the Import Alias window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Alias \>\> Import button)

2.  Select the path for the Excel file to import the alias information from.

3.  The Select the Worksheet field displays all the worksheets in the selected
    Excel file. Highlight the worksheet that you want to import.

4.  Select a destination for the log file.

5.  Choose OK to import the alias information from the selected worksheet.

#### Format to import aliases

>   You can import aliases only if they are in the required format. The first
>   line in the

>   Excel sheet from which you are importing the alias information must be
>   blank. The Excel sheet must have the columns Alias, Description,
>   SDescription, Trx Dim, and Trx Dim Code.

>   Refer to *Importing an alias* for more information on importing aliases.

#### Setting up an account class

>   An account class is a category of accounts. During transaction entry, it
>   determines the Microsoft Dynamics GP accounts that you can enter analysis
>   information for. The Analytical Transaction Entry window, where you will
>   enter analysis information, can be opened in relation to a specific
>   Microsoft Dynamics GP account only if such account is linked to an account
>   class.

>   In the Accounting Class Maintenance window, you can define transaction
>   dimensions for each account that can be used during transaction entry, if
>   linked to an account class, to enter analysis information. You can select
>   default transaction dimension codes for each of the transaction dimensions,
>   determine if default codes can be overwritten during transaction entry, and
>   allow or restrict the ability to report on customers, vendors, item numbers,
>   and site IDs.

>   **To set up an account class:**

1.  Open the Accounting Class Maintenance window. (Cards \>\> Financial \>\>
    Analytical Accounting \>\> Accounting Class)

>   IMAGE – AAACM.jpg

![](media/4b5ff99c745bd2aad5c15e4489904041.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Enter or select an account class in the Class ID field. The existing
    alphanumeric transaction dimensions will be displayed in the scrolling
    window.

2.  Enter a description for the account class in the Description 1 field. Enter
    an additional description, if required, in the Description 2 field.

3.  In the Enable Reporting On field, mark the following options to view
    analysis information about:

>   **Customers** This will allow customer numbers to be stored during
>   transaction entry for reporting purposes. You can view analysis information
>   entered in relation to a customer against the transaction dimensions set up
>   in the account class or the accounts linked to the class. If you unmark this
>   option, you cannot view analysis information for customers.

>   **Vendors** This will allow vendor numbers to be stored during transaction
>   entry for reporting purposes. You can view analysis information entered in
>   relation to a vendor against the transaction dimensions set up in the
>   account class or the accounts linked to the class. If you unmark this
>   option, you cannot view analysis information for vendors.

>   **Employees** This will allow employee IDs to be stored during transaction
>   entry for reporting purposes. You can view analysis information entered in
>   relation to an employee against the transaction dimensions set up in the
>   account class or the accounts linked to the class. If you unmark this
>   option, you cannot view analysis information for employees.

>   **Item Numbers** This will allow item numbers to be stored during
>   transaction entry for reporting purposes. You can view analysis information
>   entered in relation to an item number against the transaction dimensions set
>   up in the account class or the accounts linked to the class. If you unmark
>   this option, you cannot view analysis information for item numbers.

>   **Site IDs** This will allow site IDs to be stored during transaction entry
>   for reporting purposes. You can view analysis information entered in
>   relation to a site ID against the transaction dimensions set up in the
>   account class or the accounts linked to the class. If you unmark this
>   option, you cannot view analysis information for site IDs.

>   **Asset IDs** This will allow asset IDs to be stored during transaction
>   entry for reporting purposes. You can view analysis information entered in
>   relation to a assets ID against the transaction dimensions set up in the
>   account class or the accounts linked to the class. If you unmark this
>   option, you cannot view analysis information for assets IDs.

>   **Book IDs** This will allow book IDs to be stored during transaction entry
>   for reporting purposes. You can view analysis information entered in
>   relation to a book ID against the transaction dimensions set up in the
>   account class or the accounts linked to the class. If you unmark this
>   option, you cannot view analysis information for book IDs.

1.  In the scrolling window, you can select the analysis type for each
    transaction dimension. The following analysis types are available in the
    Data Type field:

>   **Not allowed** Transaction dimension will not be available to create
>   analysis information for accounts linked to the account class. Transaction
>   dimension codes cannot be entered for this transaction dimension during
>   transaction entry. The transaction dimensions with an analysis type of Not
>   allowed will not be displayed in the Analytical Transaction Entry windows.

>   By default, any new transaction dimension that is added will have an
>   analysis type of Not Allowed.

>   **Required** Transaction dimension codes must be entered for the transaction
>   dimension for each account that is linked to the account class.

>   **Optional** The entry of a transaction dimension code for such transaction
>   dimensions optional. For each account linked to the account class, analysis
>   information may or may not be entered.

>   **Fixed** A default transaction dimension code must be entered against this
>   transaction dimension and it cannot be overwritten during transaction entry.
>   The code will be used for all accounts linked to the account class. The
>   default transaction dimension code must be entered and can be overwritten
>   only in the Accounting Class Maintenance window.

>   If the relationship between alphanumeric transaction dimensions is
>   Combination Not Allowed, the analysis type of one of the transaction
>   dimensions must always be Not Allowed. You cannot change the analysis type
>   from Combinations Not allowed to Required or Optional or Fixed.

1.  You can enter a default transaction dimension code for the transaction
    dimension if the analysis type of the transaction dimension is Required,
    Fixed or Optional. This default dimension code will be displayed during
    transaction entry and only can be overwritten if the analysis type of the
    transaction dimension is not Fixed.

>   If you’ve marked the Show valid code combinations in trns and budgets option
>   in the Analytical Accounting Options window, then the lookup window will
>   display only those codes that have a valid combination with the codes you
>   have already selected for the transaction.

>   *You are required to enter a default transaction dimension code if the
>   analysis type of the transaction dimension is Fixed.*

1.  If the distribution accounts of a fixed or variable allocation account are
    linked to an account class, you must ensure that during transaction entry
    default transaction dimension codes are entered for all transaction
    dimensions set to Required in the class. These codes will be considered when
    you post transactions comprising fixed or variable allocation accounts.

>   For an alphanumeric transaction dimension, you can select a default
>   transaction dimension code from the transaction dimension code Lookup
>   window. You also can view information for a code or create a new code by
>   opening the Transaction Dimension Code Maintenance window from the Trx
>   Dimension Code Default Link.

>   For Numeric transaction dimensions, the field to the right of the Trx
>   Dimension Code Default field will display the Base U of M and the decimal
>   places, if it has been set in the Transaction Dimension Maintenance window.

1.  Choose the Show button to display the description of the Trx Dimension Codes
    of alphanumeric transaction dimensions.

2.  Mark the Show check box to view transaction dimensions while entering
    analysis information for transactions. This check box will be marked by
    default if the transaction dimension is Required, Fixed or Optional. Unmark
    the check box if you don’t want to view the transaction dimension during
    transaction entry.

>   You cannot hide a transaction dimension unless a default transaction
>   dimension code has been entered. If the default code of a Required or
>   Optional transaction dimension that is hidden is removed from the Accounting
>   Class Maintenance window, the transaction dimension automatically will be
>   set to Show. However, transaction dimensions will be displayed in Inquiry
>   windows, regardless of the status marked here.

1.  Inactive transaction dimensions will be displayed in the Accounting Class
    Maintenance window if you have selected the Show Inactive Trx Dim in Acct.
    Class Maint window option in the Analytical Accounting Setup window. The
    check box under the Inactive column will be marked automatically if the
    transaction dimension is inactive. This column is non-editable.

>   The analysis type of an inactive transaction dimension always will be Not
>   Allowed. It cannot be changed to any other analysis type unless the
>   transaction dimension is activated.

1.  Choose Accounts to open the Account Class Link window. Refer *Linking
    accounts to an account class* for more information.

2.  Choose Save to save the changes you’ve made. When you choose Save, the
    following checks take place:

-   If transaction dimensions have been deleted or inactivated, a message is
    displayed indicating that the relevant transaction dimension is deleted or
    inactivated. The Accounting Class Maintenance window will be cleared after
    you close the message.

-   If a transaction dimension code is deleted or inactivated a message is
    displayed indicating that the relevant code is deleted or inactivated. You
    can save the account class only if you replace or remove the relevant code.

-   If the relationship between the default codes you’ve set up in the Account
    Class Maintenance window is still valid.

-   If the relation between the default codes of such dimensions is no longer
    valid, a message appears. You cannot save changes to the account class if
    the combination between codes is not valid.

1.  Choose Clear to clear the window.

2.  Choose Delete to delete an account class. When you delete a class, all
    information related to such class will be removed from all unposted
    transactions, where accounts linked to such class have been used.

>   The Accounting Class Maintenance window will be updated when opened after
>   the following changes are made:

-   If you change the relationship between transaction dimensions in the
    Transaction Relations window, the analysis type of the transaction
    dimensions will be set to Not Allowed in the Accounting Class Maintenance
    window. The default codes you’ve entered for the dimensions also will be
    removed.

-   If you change the ownership between codes and the codes have been used as
    default codes in the Accounting Class Maintenance window, the codes will be
    removed from the account class.

>   **Example**

>   Profit Centre owns Cost Centre. Code P1 owns C1. Both codes are default
>   codes in the Accounting Class Maintenance window. This relationship is
>   changed so that C1 is now owned by P2. In the Accounting Class Maintenance
>   window, P1 and C1 will be deleted. However, you cannot change this
>   relationship if C1 is used as a default code for a fixed transaction
>   dimension. The analysis type of the transaction dimension has to be changed
>   prior to changing the ownership.

>   If transaction dimensions are valid subsets and you change the combination
>   between codes used as default codes in the Transaction Dimension Code
>   Validation window, the codes will be removed from the Accounting Class
>   Maintenance window.

>   **Example**

>   Profit Centre and Cost Centre are valid subsets. Code P1 and C1 are set as a
>   valid combination and are used as defaults in the Accounting Class
>   Maintenance window. Subsequently, P1 is set as a valid combination only with
>   C2. In the Accounting Class Maintenance window, C1 and P1 will be removed.

>   However, you cannot change the combination between C1 and P1 if Profit

>   Centre and Cost Centre are Fixed types and have been used as default codes.
>   To

>   do this, you must change the analysis type of Profit Centre and Cost Centre
>   from Fixed to any of the other available analysis types.

>   Transaction Dimensions or Transaction Dimension codes that have been deleted
>   or inactivated will be removed from the Accounting Class Maintenance window.
>   To delete or inactivate default transaction dimension codes for a fixed or
>   hidden transaction dimension, you must change the analysis type set for the
>   transaction dimension to show.

#### Linking accounts to an account class

>   Use the Account Class Link window to link accounts to an account class.

>   You can link any Microsoft Dynamics GP account to an account class, except
>   for the fixed and variable allocation accounts. However, distribution
>   accounts for fixed and variable accounts can be linked to an account class.

*An account can be linked only to one account class.*

>   **To link accounts to an account class:**

1.  Open the Account Class Link window.  
    (Cards \>\> Financial \>\> Analytical Accounting \>\> Accounting Class
    Maintenance \>\> Accounts button)  
    (Cards \>\> Financial \>\> Analytical Accounting \>\>Accounting Class Link)

-   IMAGE - AAACL.jpg

![](media/4a39c9de410d1bbdb9a2832dcbb0445d.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Enter or select an account class to that the accounts will be linked to. The
    scrolling window will display all the accounts in the Microsoft Dynamics GP
    Chart of Accounts except fixed and variable allocation accounts.

2.  From the Show Accounts options, select one of the following:

>   **All** Displays all posting, and unit accounts

**Balance Sheet** Displays only Balance Sheet accounts

>   **Profit/Loss** Displays only Profit/Loss accounts

**Unit** Displays only Unit accounts

1.  From the Link Status options, select one of the following:

**All** Displays all accounts, whether linked or not.

>   **Linked** Displays accounts which are linked to an account class.

**Not Linked** Displays accounts which are not linked to any account class.

1.  Use the Search by field to search for a specific account in the scrolling
    window. The method you use depends on the option selected from the View Menu
    drop- down list. For example, if you have selected the Show Accounts by
    account option, the Search by field will allow you to find an account based
    on the account.

2.  The scrolling window displays the accounts based on the option you select
    from the View menu. To link an account to the account class displayed, mark
    the Link check box for the account to link.

3.  The Linked to Class ID field displays the account class that the account has
    been linked to. If the account is not linked to an account class, you can
    select an account class to link it to from the Accounting Class lookup
    window. The account class you select can be different from the class that is
    displayed in the Account Class Link window.

4.  If you select a posting account that’s used as a distribution account of a
    fixed or variable allocation account to link to an account class, a message
    will appear reminding you to specify default transaction dimension codes for
    transaction dimensions set to Required or Optional in the Accounting Class
    window. Refer *Setting up an account class* for more information about
    default transaction dimension codes.

>   The Account No field displays the account.

>   The Account Description field displays the description for the account.

1.  Choose Mark All to mark all displayed accounts to link the accounts to the
    account class you have selected in the Class ID field. If the posting option
    you have selected in the Posting Setup window (Administration \>\> Setup
    \>\>Posting \>\> Posting) is Create a Journal Entry Per Batch, a message
    appears when you choose Mark All indicating that accounts set to Post in
    Summary will not be marked.

>   This is to ensure that if the Use Account Settings option is not marked,
>   accounts that post in summary are not linked to an account class. Before you
>   activate Analytical Accounting, you can ensure that the level of posting of
>   such accounts is set to detail to link it to an account class.

>   *You must mark the Create a Journal Entry per Batch and Use Account Settings
>   options in the Posting Setup window to activate Analytical Accounting.
>   However, you can link accounts to an account class before Analytical
>   Accounting has been activated.*

1.  Choose Unmark All to unmark all the accounts that were previously marked. If
    you unmark an account from an account class and if the account exists in an
    unposted transaction, analysis information for the account will be deleted
    from the transaction. In addition, any account that is removed from an
    Accounting Class cannot be adjusted on the Analytical Adjustment Entry. If
    the account exists in an un-posted adjustment, any adjustment made for that
    account will be deleted once the account is unmarked from the accounting
    class.

2.  Choose Save to save the links you have made.

3.  Choose Clear to clear the window.

#### Linking accounts to classes and nodes

>   Use the Analytical Accounting Account Maintenance window to link accounts to
>   both an account class and a node on the main tree.

>   You can link any Microsoft Dynamics GP account to an account class, except
>   for the fixed and variable allocation accounts.However, distribution
>   accounts of fixed and variable accounts can be linked to an account class.

*An account can be linked only to one account class.*

>   **To link an account to classes and nodes:**

1.  Open the Analytical Accounting Account Maintenance window. (Cards \>\>
    Financial \>\> Analytical Accounting \>\> Account)

2.  Enter or select an existing account. If you select a posting account that is
    used as a distribution account of a fixed or variable allocation account, a
    message will appear indicating that you must be sure that default
    transaction dimension codes have been entered for Required or Optional
    transaction dimensions in the Accounting Class that the account is or will
    be linked to. Refer to *Setting up an account class* for more information.

>   The Description field displays the description of the account.

1.  In the Linked to Node field, select the node of the main tree that the
    account must be attached to. Each account must be linked to a valid node of
    the main tree. Refer to *Setting up trees* for more information.

2.  Select the account class in the Class ID field to enter analysis information
    for this account during transaction entry. The name or description of the
    selected account class is displayed in the field below Class ID.

>   If the level of posting of an account is set to summary, you cannot link the
>   account to an account class if the posting setup in the Posting Setup window
>   is Create a Journal Per Batch.

1.  Choose Save to save the details.

2.  Choose Clear to clear the information in the window.

#### Setting up account access to codes

>   Use the Account Access to Transaction Dimension Codes window to specify the
>   accounts that have access to a selected transaction dimension code. This
>   will determine which codes can be used for a distribution while entering an
>   analytical transaction. By default, all the codes have access to all the
>   accounts linked to an accounting class. You can assign multiple ranges of
>   accounts to a dimension code; you can also assign an account to multiple
>   dimension codes.

>   *The codes belonging to a transaction dimension that is set to Not Allowed
>   for an accounting class do not have access to that accounting class.*

>   The following conditions must be met before you can specify account access
>   for codes:

-   You must have set up at least one accounting class.

-   The selected transaction dimension must have a valid relationship with at
    least one accounting class. You cannot select a dimension if it’s analysis
    type is set to Not Allowed for all accounting classes.

>   **To set up account access to codes:**

1.  Open the Account Access to Trx Dimension Codes window. (Cards \>\> Financial
    \>\> Analytical Accounting \>\> Account Access)

2.  Enter or select a transaction dimension. The description for the selected
    dimension is displayed in the Description field.

3.  Enter or select the transaction dimension code for which to specify account
    access. The description for the selected dimension code is displayed in the
    Description field.

4.  Select the access option for the selected transaction dimension code.

>   **All Accounts** is the default selection, giving access to all accounts
>   linked to an accounting class.

>   **Select Accounts** Select this option to specify the accounts to which the
>   selected code will have access. The rest of the window will become available
>   for you to select the accounts.

>   *You must insert at least one account in the scrolling window if you choose
>   the option Select Accounts. If you choose Save or close the window when
>   there are no accounts in the scrolling window, the account access setting
>   for the selected code will automatically revert to All Accounts.*

1.  In the Account Type field, select the type of accounts to include in the
    range.

>   **All** All the accounts in the selected range will be available for
>   selection in the From and To Look up. This includes Balance Sheet, Profit
>   and Loss and Unit accounts.

>   **Balance Sheet** Only balance sheet accounts from the selected range will
>   be available for selection in the From and To Look up.

>   **Profit and Loss** Only profit and loss accounts from the selected range
>   will be available for selection in the From and To Look up.

>   **Unit** Only unit accounts from the selected range will be available for
>   selection in the From and To Look up.

1.  In the Ranges field, select whether to assign a range based on Account,
    Segment ID or Account Class. If you select Segment, the Segment ID field
    becomes available. Enter the Segment ID.

2.  Enter the range in the From and To fields. The lookup displays the range of
    accounts, account classes, or segment ID, depending on your selection in the
    Ranges field.

3.  Choose Insert to insert the accounts within the selected range into the
    scrolling window. The scrolling window displays the account and description
    for each account. If you’ve chosen Account Class, all the accounts of the
    selected type assigned to those classes will be inserted. For example, if
    you’ve selected Balance Sheet as the Account Type, then only Balance Sheet
    accounts that are part of the selected range will be inserted into the
    scrolling window.

>   Once you’ve inserted a range in the scrolling window, you can select another
>   range to insert. The new range will be added below the existing range in the
>   scrolling window. An account will be inserted into the scrolling window only
>   once, even if it is part of more than one range.

1.  Select an account in the scrolling window and choose Remove to remove that
    account. Choose Remove All to remove all the accounts from the scrolling
    window. The Remove and Remove All fields become available only when accounts
    exist in the scrolling window.

2.  Choose Save to save the account access settings for the selected transaction
    dimension code and clear the window. The settings you’ve saved will be
    displayed when you open this window and select the same dimension code.

3.  Choose Clear to clear all the values you’ve entered in the window without
    saving.

#### Entering analysis information for fixed assets transactions

>   Use the Analytical Fixed Asset Setup window to module enter or view the
>   analysis information for the distribution accounts that are linked to an
>   account class. The window name depends upon the path from where you open
>   this window.

>   You can view the transaction dimension codes and description for the
>   transaction dimension codes for fixed asset transactions. You can view the
>   Asset ID, Book ID and Alias details in the Analytical Fixed Asset Setup
>   window.

>   **To enter or view analysis information for fixed assets transactions**

1.  Open the Analytical Fixed Asset Setup window  
    (Cards \>\> Fixed Asset \>\> Book \>\> enter or select an asset ID and book
    ID \>\>Additional \>\> Analytical Transaction or CTRL+T)  
    (Cards \>\> Fixed Asset \>\> Book \>\> enter or select an asset ID and book
    ID \>\>Analytical Accounting Button)  
    (Cards \>\> Fixed Assets \>\> Book\>\>\> Go to button \>\> Account\>\> enter
    or select an asset ID and book ID \>\> Additional \>\> Analytical
    Transaction or CTRL+T) (Cards \>\> Fixed Assets \>\> Book\>\>\> Go to button
    \>\> Account\>\> enter or select an asset ID and book ID \>\> Analytical
    Accounting Button)  
    (Cards \>\> General \>\> select an asset ID \>\> Go to button\>\> Book \>\>
    select a book ID \>\> Additional \>\> Analytical Transaction or CTRL+T)  
    (Cards \>\> General \>\> select an asset ID \>\> Goto button\>\> Book \>\>
    select a book ID \>\>Analytical Accounting Button)  
    (Cards \>\> Fixed Assets \>\> Account\>\> enter or select an asset ID \>\>
    Analytical Accounting Button)  
    (Cards \>\> Fixed Assets \>\> Account\>\> enter or select an asset ID \>\>
    Additional\>\> Analytical Transaction or CTRL+T)

2.  The Distribution field displays the distribution account selected in the
    Asset Account window.To view other distributions, enter or select a
    distribution number.

>   The sequence of distributions in the Analytical Transfer Maintenance window
>   may not correspond to the sequence in the Payroll Transaction Entry window
>   because only accounts linked to an account class are displayed in the
>   Analytical Payroll Transaction Entry window.

>   The Company ID field will display the company in which the transaction is
>   taking place.

1.  The Account field will display the distribution account for which analytical
    information is being entered. The description of the account, as set up in
    the Account Maintenance window, will appear in the next line. Click the
    Account expansion button to open the Microsoft Dynamics GP Account Entry
    window.

>   The balance type of the account, whether debit or credit, will be displayed
>   next to the account.

1.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes,
    if required. Refer to *Creating an alias* for more information.

>   The Trx Dimension field displays Transaction Dimensions of the account class
>   to which the distribution account is linked. Only Transaction Dimensions
>   which have been set as Fixed, Required, or Optional will be displayed.
>   Transaction dimensions which are set to Hide in the Accounting Class
>   Maintenance window will not be displayed. Refer to *Setting up an account
>   class* for more information.

>   The Trx Dimension Description field displays the description of the
>   transaction dimension.

1.  Enter or select an alphanumeric transaction dimension code in the
    Alphanumeric column. You can add a new alphanumeric transaction dimension
    code if you have selected the Create New Codes On The Fly option in the
    Transaction Dimension Maintenance window.

>   *The Alphanumeric column is available only for an alphanumeric transaction
>   dimension.*

1.  Choose Save to save the analysis information you have entered and clear the
    window.

>   You can save analysis information with errors, but you cannot post them.

1.  Choose Validate to validate the distribution displayed in the window. If
    changes are made to the account class in setup or errors are found during
    the validation process, the Analytical Accounting Validation Log window will
    open displaying the errors or changes identified. You can view the changes
    to the account class by selecting the Default button in the Analytical Item
    Transaction Entry window.

>   *Analysis information will also be validated if you select OK or Save in the
>   Analytical Fixed Asset Setup window.*

>   You can choose to save analysis information with errors or without updating
>   changes made to the account class.

>   You can validate a document in the Item Transaction Entry window by using
>   the options CTRL+R or Additional \>\> Run Validation.

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

1.  Choose the Print drop-down to print the Analytical Accounting Edit list for
    the distribution currently displayed in the window or for all distributions
    of the transaction linked to an account class. If errors are detected, the
    Analytical Validation Log is also printed.

#### Setting up trees

>   You can set up an unlimited number of trees to group master data in
>   Analytical Accounting. Use the trees to select master records and also to
>   display selected nodes, or single records, or to build groups to show totals
>   and subtotals on reports.

>   Trees are also used for reporting and analyzing purposes in the Multilevel
>   Query wizard. Refer to *Chapter 17, “Inquiries”*for more information.

>   There are two types of trees:

>   **Main Tree** These are created automatically for each type of master record
>   and cannot be deleted. By default, the master records will be linked to the
>   root node of the main tree but can be attached to other nodes within the
>   same tree. New master records always will be linked to the root node of the
>   tree but can be changed.

>   **Additional Trees** You can create unlimited trees for each type of master
>   record. You can choose whether the tree should include all master records or
>   just a subset of master records. If you link all the records to the tree,
>   any new master record created automatically will be linked to the tree.

>   **To set up trees:**

1.  Open the Tree Maintenance window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Tree)

2.  Select the type of the master record from the Tree Type field. The options
    available are:

    -   Account

    -   Customer

    -   Employee

    -   Vendor

    -   Item

    -   Site

    -   Trx Dimension

>   You can create trees only for alphanumeric transaction dimensions.

1.  Enter or select a tree definition. A main tree will always be available in
    the Tree lookup window. If the tree is a main tree, the Main Tree check box
    will be marked by default. You cannot unmark this check box. If you’ve
    defined the tree, the Main Tree check box is unmarked and cannot be marked.

>   The Dimension field will be available only if you select Transaction
>   Dimension in the Tree Type field. The description of the alphanumeric
>   transaction dimension that the tree has been created for is displayed in
>   this field. You can’t modify the description. The default description will
>   be displayed when you select an alphanumeric transaction dimension in the
>   Dimension field.

1.  Mark the Tree includes all records option to link all the master records to
    the tree. This field is available only if you are creating a new tree. The
    master records will be attached to the root node of the tree. If a new
    master record is created, it will be linked to the root node of the main
    tree and to all the other trees that have this field marked.

2.  Enter a description for the tree in the Description field.

3.  Choose Structure to open the Tree Structure window where you can define the
    structure of the tree. Refer *Defining a tree structure* for more
    information.

4.  Choose Save to save the tree definition.

5.  Choose Clear to clear the window.

6.  Choose Delete to delete the tree. You cannot delete a tree if it has been
    used in a query created in the Multilevel Query wizard. You cannot delete a
    main tree.

#### Defining a tree structure

>   You can define the structure of an existing tree in the Tree Structure
>   window.

>   **To define a tree structure:**

1.  Open the Tree Structure window.

>   (Cards \>\>Financial \>\> Analytical Accounting \>\>Tree Structure)

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Tree \>\> Structure
>   button)

1.  Select a master record type in the Tree Type field. The master record types
    are:

    -   Account

    -   Customer

    -   Employee

    -   Vendor

    -   Item Number

    -   Site

    -   Trx Dimension

2.  Enter or select a tree in the Tree field. If the tree is a main tree, the
    Main Tree check box will be marked by default. This check box cannot be
    unmarked. If the tree is user-defined, the Main Tree check box is unmarked
    and cannot be marked.

>   If you’ve opened the Tree Structure window from the Tree Maintenance window,
>   the tree type and tree entered is displayed.

>   The Tree View window shows the tree structure of the selected tree. You can
>   double-click a node and open the Edit Tree Node window where you can change
>   the description of the node.

1.  Enter the new description for the node.

2.  Choose Save to save the description or Cancel to cancel the description you
    have entered and return to the Tree Structure window.

3.  In the Tree Structure window, to create a new node, select an existing node
    and choose New Node. This will open the Add Tree Nodes window.

4.  Enter a description for the new node and choose Add. The new node will be
    created one level below the selected node. To create a new node at the first
    level, select the Root Node, which is the first entry in the tree view.

5.  In the Tree Structure window, choose the Left arrow to move the selected
    node and its sub nodes one level higher in the tree if the selected node is
    not at the first level.

6.  Choose the Right arrow to move the selected node and its sub nodes one level
    lower in the tree if the selected node is not at the last level. The new
    main node will be one line up on the same level.

7.  Choose the Up arrow to move the selected node and its sub nodes one line up
    on the same level in the structure.

8.  Choose the Down arrow to move the selected node and its sub nodes one line
    down on the same level in the structure.

9.  Choose Delete Node to remove a selected node and its sub nodes. If there are
    master records linked to the deleted node, they will be linked to the root
    node when you choose Save.

10. Choose the printer icon button to print the edit list. The structure of the
    tree selected in the tree structure window will be printed.

#### Copying a tree structure

>   You can copy an existing tree structure to set up another tree. You also can
>   copy the records linked in an existing tree to another tree.

>   **To copy a tree structure:**

1.  Open the Copy Tree Structure window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Tree Structure \>\> Copy button)

2.  Select the tree to copy from in the Copy from Tree field. Be sure that the
    Tree that the data is being copied from is the same Tree Type (Dimension,
    account) as the tree where the data will be copied to. The description of
    the selected tree appears in the field below.

3.  Select the tree to copy to. The tree types that are similar to the tree type
    you are copying from are displayed in the lookup window.

4.  Select to copy only the tree structure, or both the tree structure and the
    link records.

    -   If you select the Copy tree structure option, then only the tree
        structure will be copied. Before the copying process begins, the
        existing structure of the destination structure will be deleted and all
        the linked records will be linked to the root node.

    -   If you select the Copy tree structure and link records option, the
        existing structure and all links to master records are removed and will
        be replaced by the new structure and link records from tree you’re
        copying from.

>   *This option is only available if both the Copy Source and Destination have
>   the Tree includes all records available or unavailable option selected in
>   the Tree Maintenance window.*

1.  Choose Copy to copy the tree structure and close the window.

2.  Choose Cancel to close the window.

#### Linking master records to an existing tree structure

>   The Tree Record Link window allows you to link master records to an existing
>   tree structure. You also can add new master records to the tree, remove
>   master records from the tree and print the structure with its linked master
>   records.

>   **To link master records to an existing tree structure:**

1.  Open the Tree Record Link window.

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Tree Record Node Link)

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Tree \>\> Structure
>   \>\> Link Records)

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Tree Structure \>\>
>   Link Records)

>   IMAGE – AATRL.jpg

![A screenshot of a cell phone Description automatically generated](media/9bc89c12908147acc8f143a8e7afbd67.jpg)

A screenshot of a cell phone Description automatically generated

1.  Select the tree type.

2.  Select the Tree ID to modify the Record Links in. If you select a main tree,
    the Main Tree checkbox will be marked. If opened from the Tree Structure
    window, the tree type and tree entered in that window are displayed in the
    Tree Type and Tree fields.

3.  If the tree has an associated transaction dimension, the dimension is
    displayed.

4.  The tree structure of the selected tree appears in the Tree View window on
    the left. Select an item in the tree view to display the master records
    linked to that node in the list window on the right side.

5.  Click the Attach to button to open the Move Master Records window where all
    nodes, except the node to which the record is currently linked to, are
    displayed.

6.  Highlight the node that the record selected is to be attached to and choose
    Select to attach the master record to the node. The Attach to button is only
    available if at least one master record is selected in the list window.

7.  After the records are linked to the new node, the linked master records of
    this node will appear in the list window.

8.  Choose Add to open the Add Master Records To Tree window. This button is
    only available if the selected tree is not a main Tree and the Tree includes
    all records option is not marked in the Tree Maintenance window.

9.  Choose Remove to remove the selected master record from the tree. This
    button is only available if at least one master record has been selected in
    the list window, the tree is not a main Tree and the Tree includes all
    Records option is not marked in the Tree Maintenance window.

10. Choose Save to save the Record Node link to the table.

11. Choose Clear to clear the window.

### Adding master records to an existing tree

>   You can add master records to an existing tree using the Add Master Records
>   to Tree window. This can be done only if the tree is not the main tree and
>   the Tree includes all records option is not marked in the Tree Maintenance
>   window.

>   **To add master records to an existing tree:**

1.  Open the Add Master Records to a Tree window. (Cards \>\> Financial \>\>
    Analytical Accounting \>\> Tree Record Node Link \>\> Add button)

2.  The Search By field displays the search method that was selected in the View
    menu. To search for a master record, enter the description for the record in
    this field and press the TAB key.

>   Master records that are not linked to the tree and their descriptions are
>   displayed in the scrolling window.

1.  Mark the records you want to add to the tree and choose OK.

2.  Click Add in the scrolling window to display the records by their add
    status.

3.  Click the Column Header ID to sort the records in the scrolling window for
    the selected tree. This field is determined depending on the tree type and
    the dimension if Trx Dimension is used as tree type.

4.  Choose Mark All to select all the records.

5.  Choose Unmark All to unmark all the selected records.

6.  Choose the Add button to add the selected records to the tree and close the
    window.

Chapter 3: Budgets
------------------

>   Analytical Accounting Budgets allows you to set up a budget tree using the
>   transaction dimensions and codes that you have created. You can record
>   amounts against each node of the budget tree and allocate the amounts to
>   various accounts for each node. You can export the budget to Excel where you
>   can modify it if required, before importing it back into Microsoft Dynamics
>   GP. The Multilevel Query wizard allows you to compare actual versus budgeted
>   amounts and find the variance, as well as compare budget amounts for
>   different years.

>   This information is divided into the following sections:

-   *Setting up a budget tree*

-   *Assigning budget tree codes*

-   *Using the dimension code tree view*

-   *Adding and removing transaction dimension codes*

-   *Creating a budget*

-   *Copying budgets*

-   *Selecting calculation methods for budgets*

-   *Understanding node budget roll down*

-   *Rolling down node budget amounts*

-   *Understanding account budget roll down*

-   *Understanding node budget roll up*

-   *Assigning a range of accounts* • *Exporting budget details*

-   *Understanding budget import*

-   *Importing a budget*

### Setting up a budget tree

>   A budget tree consists of only alphanumeric transaction dimensions and the
>   codes attached to those dimensions. You can choose the transaction
>   dimensions that make up a budget tree, and specify the order in which they
>   appear in the tree. All the selected dimensions must share a valid
>   relationship with one another, and must belong to at least one common
>   accounting class. Refer to *Setting transaction dimension relationships* and
>   to *Setting up an account class* for more information.

>   **To set up a budget tree:**

1.  Open the Budget Tree Maintenance window. (Cards \>\> Financial \>\>
    Analytical Accounting \>\> Budget Tree)

2.  Enter or select a Budget Tree ID. This field becomes unavailable once you
    press TAB after entering a value here. Enter a description for the budget
    tree ID in the Description field.

>   The Available Dimensions list displays the description for all the
>   alphanumeric dimensions, entered in the Description 1 field on the
>   Transaction Dimension Maintenance window. The descriptions are listed in the
>   order that you have assigned to the dimensions on the Transaction Dimension
>   Order window. Refer to *Defining transaction dimensions* , and *Changing the
>   order of transaction dimensions* for more information. The first dimension
>   in this list is highlighted by default.

1.  Select a dimension from the Available Dimensions list and choose Insert to
    insert it into the Selected Dimensions list to the right of the window. Once
    you have selected a dimension, it is removed from the Available Dimensions
    list. All the selected dimensions must belong to at least one common
    accounting class.

>   *A dimension belongs to an accounting class if its analysis type is either
>   Required, Fixed or Optional for that accounting class.*

>   Once you have inserted at least one dimension in the Selected Dimensions
>   list, then every subsequent dimension that you select must have a valid
>   relationship with the dimensions already selected. If a dimension shares a
>   relationship of No Combination Allowed with any of the previously selected
>   dimensions, you will not be able to insert that dimension.

1.  Choose Insert All to insert all the dimensions into the Selected Dimensions
    list. If any of the dimensions does not have a valid relationship with any
    other dimension, you will get a message and none of the dimensions will be
    inserted.

2.  Select a dimension in the Selected Dimensions list and choose Remove to
    remove it. Once you have removed a dimension, you can view it in the
    Available Dimensions list. The Remove button becomes available only when you
    select a dimension in the Selected Dimensions list. You can only highlight
    one dimension at a time in the Selected Dimensions list.

3.  Choose Remove All to remove all dimensions from the Selected Dimensions
    list. The Remove All button will be unavailable if no dimension is listed in
    the Selected Dimensions list.

4.  Use the up, down, top and bottom arrow buttons to change the order of the
    selected dimensions if required. All the dimensions will first appear in the
    Selected Dimensions list in the order in which you select them. The order of
    dimensions in the Selected Dimensions list determines the order in which
    they appear on the budget tree.

>   You cannot insert or remove dimensions, or change the order of dimensions if
>   the budget tree ID is attached to a budget ID. To do this, you must first
>   delete all the budget IDs to which the budget tree ID has been attached.

>   You cannot insert or remove dimensions, or change the order of dimensions if
>   the budget tree ID has codes assigned to it. A message appears warning you
>   that on doing so, all the codes attached to the budget tree ID will also be
>   removed. If you choose to continue, you must then re-assign the codes in the
>   Assign Budget Tree Codes window.

1.  Choose Codes to open the Assign Budget Tree Codes window, where you can
    assign codes for each dimension in the budget tree. Refer to *Assigning
    budget tree codes* for more information.

2.  Choose Save to save the budget tree ID you have created.

3.  Choose Delete to delete the budget tree ID that is displayed in this window.

>   You cannot delete a budget tree ID that is attached to a budget ID. To do
>   this, you must first delete all the budget IDs to which the budget tree ID
>   has been attached.

>   If a budget tree is not attached to a budget ID, but has codes assigned to
>   it, all the codes will be lost when you delete the budget tree ID.

1.  Choose Print to print the Budget Tree Maintenance Report for all budget tree
    IDs or for the budget tree ID displayed in the window.

### Assigning budget tree codes

>   Once you have set the order of transaction dimensions, you must assign
>   dimension codes to the budget tree ID that you have created. You can only
>   set budget amounts for the codes that you assign to the budget tree ID. You
>   can assign a range of codes, or individual codes to a dimension. If you make
>   changes to the budget tree ID on the Budget Tree Maintenance window after
>   assigning codes, all the assigned codes will be deleted. You will have to
>   re-assign the codes.

>   **To assign budget tree codes:**

1.  Open the Assign Budget Tree codes window. (Cards \>\> Financial \>\>
    Analytical Accounting \>\> Assign Budget Tree Codes)

-   IMAGE – AABT.jpg

    ![A screenshot of a social media post Description automatically generated](media/69124bee71206a3c37be4b2b773e19f2.jpg)

    A screenshot of a social media post Description automatically generated

1.  Enter or select the budget tree ID for which you are assigning codes. The
    Description field displays the description for the selected budget tree ID.

2.  Assign a range of codes in the From and To columns for each dimension
    displayed in the Dimensions column of the scrolling window. Dimensions are
    listed in the order defined in the Budget Tree Maintenance window. The
    default values in the From and To columns are the text \<FIRST\> and
    \<LAST\> respectively. \<FIRST\> denotes the first code of the dimension,
    and \<LAST\> denotes the last code, in numeric-alpha order.

>   To select a different range, enter or select the range of codes for each
>   dimension in the From and To columns, in numeric-alpha order. You can also
>   keep \<FIRST\> as it is in the From column and select a code in the To
>   column. Alternatively, you can select a code in the From column and keep
>   \<LAST\> as it is in the To column. Both the From and To fields must have
>   values; you cannot enter a value in one field and leave the other blank.

>   *If you’ve marked the Show valid code combinations in trns and budgets
>   option in the Analytical Accounting Options window, then the lookup window
>   will display only those codes that have a valid combination with the codes
>   you have already selected for the budget tree.*

1.  Clear the default values in the From and To fields if you do not want to
    assign codes to a dimension. If you do not assign codes for a particular
    dimension, you will not be able to assign codes for any dimension below that
    dimension. The From and To fields for the lower dimensions will be blank and
    unavailable.

>   *In order to assign a range to a dimension, ranges should have been assigned
>   to all the dimensions that appear above that dimension.*

1.  Choose Assign to assign the selected codes to the budget tree ID. The values
    in the From and To columns of the scrolling window return to the \<FIRST\>
    and \<LAST\> code values.

>   The tree you’ve created can be viewed in the Dimension Code Tree view. Codes
>   will only be inserted below nodes with which they share a valid
>   relationship. Refer to *Using the dimension code tree view* for a better
>   understanding of the structure of the dimension code tree.

>   *After you’ve assigned codes for the first time, if you subsequently assign
>   a different range of codes to the budget tree ID, the existing dimension
>   code tree will be over written.*

1.  Highlight a node in the dimension code tree view. The Selected Node field
    displays the combination of codes to which the highlighted node belongs. The
    budget tree ID is highlighted by default.

2.  Select a code from the Add to Node drop down list and choose Add to add the
    code to the selected node. You can add a code only if it shares a valid
    relationship with the selected node. You cannot add a code that already
    exists under the selected node.

>   The Add to Node field displays the description of the dimension that is
>   directly below the selected node. The drop-down menu lists all the codes
>   you’ve assigned to the dimension below the selected node.

1.  Highlight a code and choose Remove in the Remove Dimension Code field to
    remove the code from the selected node or from the entire tree.

>   **Select Node** to remove the selected code from the node it belongs to.
>   This will remove the selected code and all codes below it from the node
>   displayed in the Selected Node field.

>   **Select Tree** to remove the code from the entire tree. This will remove
>   the selected code and all the codes below it from all nodes of the tree.

1.  Choose the Budget button to open the Analytical Accounting Budget
    Maintenance window, where you can assign budget amounts to the budget tree.
    Refer to *Adding and removing transaction dimension codes* for more
    information.

2.  Choose Save to save the codes assigned to the budget tree ID.

3.  Choose Delete to delete all the codes assigned to the budget tree ID.

4.  Choose Print to print the Assign Budget Tree Codes Report for the budget
    tree displayed in the window.

### Using the dimension code tree view

>   Analytical Accounting Budgets uses a tree view called the Dimension Code
>   Tree to display the codes that you’ve assigned to the budget tree ID. You
>   can create and modify the dimension code tree for each budget tree ID in the
>   Assign Budget Tree Codes window (Cards \>\> Financial \>\> Analytical
>   Accounting \>\> Assign Budget

>   Tree Codes). You can view the dimension code tree for the selected budget
>   tree ID in

>   the Analytical Accounting Budget Maintenance window (Cards \>\> Financial
>   \>\> Analytical Accounting \>\> Budget).

>   Each line in the tree is a node and the nodes are organized in the order
>   that you’ve set the transaction dimensions in the Budget Tree Maintenance
>   window.

>   Use the following example to understand the dimension code tree. You have
>   set up a budget tree ID AA, and the following dimensions and codes are
>   assigned to it:

| **Dimensions** | **Range of codes attached to dimensions** |
|----------------|-------------------------------------------|
| Profit Centre  | PCTR1 to PCTR2                            |
| Project        | PRJ1 to PRJ1                              |
| Product        | PDT1 to PDT2                              |
| Location       | LOC1 to LOC1                              |

>   Based on the valid relationships that the codes have with one another, the
>   tree will look as follows:

>   IMAGE – AABTR.jpg

![A screenshot of a cell phone Description automatically generated](media/77cfbf2c0c1a346f47d831e9f2e9c5ad.jpg)

A screenshot of a cell phone Description automatically generated

-   The budget tree ID is the highest level of the dimension code tree, and is
    also called the root node of the tree.

-   The level of codes directly below the root node is called the first level of
    the tree.

-   Highlight a node in the dimension code tree, to enter or view the
    information relevant to that node in the scrolling window (in the Analytical
    Accounting Budget Maintenance window, or the Analytical Accounting Budget
    vs. Actual Inquiry window). When you move the focus to another node, and
    then navigate to another field in the window, the node that you last
    selected remains highlighted. Therefore, a node is always highlighted in the
    dimension code tree view.

-   The Selected Node field displays the combination of codes to which the node
    you’ve highlighted belongs. Any changes you make to the scrolling window are
    valid only for the selected node.

-   A node that does not have any nodes below it is called a bottom node. A tree
    can have several bottom nodes.

>   *If a code (e.g. PDT 2), does not have a relationship with any code above it
>   (e.g. PCTR 2), then it will not appear under that node (PCTR 2 \>\> PRJ 1).
>   It will, however, continue to appear under those nodes with which it shares
>   a valid relationship (e.g. PCTR 1 \>\> PRJ 1 \>\> PDT 2).*

### Adding and removing transaction dimension codes

>   You can add or remove transaction dimension codes from a budget tree ID that
>   is attached to a budget ID. Use the following information to understand how
>   codes are added to and removed from a budget tree that is attached to a
>   budget ID.

-   When you add codes to a budget tree ID, the new codes will have no amounts
    and/ or accounts assigned to them in the Analytical Accounting Budget
    Maintenance window.

-   When you remove codes from a budget tree ID, the amounts and the accounts
    that were assigned to those codes in the Analytical Accounting Budget
    Maintenance window will also be removed.

-   Removing a node from the budget tree will also remove all sub-nodes, and the
    amounts and accounts assigned to those sub-nodes in the Analytical
    Accounting Budget Maintenance window.

-   If you remove a code from the budget tree after assigning the budget
    amounts, you must reassign the root node amount to the remaining codes so
    that the root node amount is rolled down 100%.

### Creating a budget

>   You can create an unlimited number of budgets for both open and historic
>   years in Analytical Accounting. You also can change or delete existing
>   budgets. A budget that you enter here is not removed until you delete it
>   from the system. Use the Analytical Accounting Budget Maintenance window to
>   assign amounts and accounts to the budget tree that you have created.

>   **To create a budget:**

1.  Open the Analytical Accounting Budget Maintenance window. (Cards \>\>
    Financial \>\> Analytical Accounting \>\> Budget)

-   IMAGE – AABM.jpg

![](media/d00cebec54be3bd8c1a107a73f46e8b8.jpg)

>   A screenshot of a computer Description automatically generated

1.  Enter or select a budget ID and enter a description for the budget ID in the
    Description field.

2.  Select to base the budget on a fiscal year or a date range. If you select to
    base the budget on a date range, specify a range that crosses one or more
    fiscal years.

3.  To restrict access to the budget, choose the Password Padlock button to open
    the Microsoft Dynamics GP User Password Setup window and enter a password.
    If you don’t need to restrict access to the budget, skip to the next step.

4.  Select a year for which you are assigning budget amounts. Budget amounts are
    saved against the Budget ID - Year combination, which is a unique
    combination. The value in the Year field cannot be changed once you enter a
    year and TAB off the field.

>   If you enter a Budget ID - Year combination for the first time, and the
>   budget ID already exists in the previous year, a message appears asking if
>   you want to copy the existing budget. Choose Yes to open the Copy window,
>   where you can copy the budget. Refer to *Copying budgets* for more
>   information.

1.  Select whether to mark the budget as Preliminary or Actual.

>   Choose Actual if you know that the budget will be calculated correctly and
>   that you will not be making changes to the budget.

>   Choose Preliminary to experiment with budgets. You can change preliminary
>   budgets and then revert to the original version of the budget, but when you
>   change actual budgets, the change is permanent.

>   *If you’re calculating a preliminary budget and you’d like to save it, make
>   the changes permanent by choosing Actual and save the budget. The budget
>   will also be saved as Actual if you choose the Save button to save changes
>   to a preliminary budget.*

1.  Enter or select a budget tree ID. The dimension code tree that was set up
    for the selected budget tree ID is displayed in the tree view. You can
    assign a same budget tree ID to multiple budget IDs.

>   The budget ID - budget tree combination is unique across all years. When you
>   enter a budget ID that exists in a different year, and enter a new year, the
>   budget tree ID will automatically default from the budget ID- year that
>   already exists. You cannot change this budget tree ID.

1.  When you select the budget tree ID, the dimension code tree view is
    populated with all the dimension codes in fully expanded form. The root node
    is highlighted by default. Refer to *Using the dimension code tree view* for
    more information.

>   **Node Budget Amounts scrolling window** displays the amount entered for
>   each period for the node that you’ve highlighted in the dimension code tree
>   view. When the budget level is Account, this window displays the values
>   allocated to the account that you’ve selected in the Account field.

>   **Node Period Total** displays the total amount for the selected node for
>   the selected period. If you’ve selected an account for which you are
>   entering period amounts for a node, you can still view the total amount for
>   the period in the Node Period Total field.

>   **Total** displays the total amount or quantity that you’ve entered for the
>   selected node or for a selected account on the selected node.

1.  Select the Budget Level at which to create the budget, whether Tree or
    Account You can enter a budget for a budget tree or for a budget tree -
    account combination.

>   **Tree** is the default selection. You must first enter budget amounts for
>   the budget tree, before you can allocate budgets for accounts.

>   **Account** select to assign a single posting or unit account to a selected
>   node of the budget tree. You can assign an account to any node as long as
>   you’ve assigned that account to the node directly above it. You cannot
>   assign fixed or variable allocation accounts. You cannot assign accounts to
>   the root node.

1.  In the Budget Roll Total field, select whether to roll down the budget from
    the root node to lowest nodes or roll up the budget from lowest nodes to the
    root node.

>   **Down** Rolls down the budget amount specified in the root node to lower
>   nodes till the lowest node. This option is selected by default. Refer to
>   *Understanding node budget roll down* for more information.

>   **Up** You can enter amounts in the lowest nodes. These amounts are added up
>   and rolled up to the parent node. This process repeats itself until the
>   amount is rolled up to the root node. Refer to *Understanding node budget
>   roll up* for more information.

>   *If you select the option as Up for a budget which is not rolled down
>   completely, the amount or quantity that you have entered for each node of
>   the budget will be reset to zero.*

1.  In the Enter field, choose whether to enter an amount for the budget, which
    would be used in posting accounts, or a quantity, which would be used in
    unit accounts.

>   **Amount** the Amount field in the Node Budget Amounts scrolling window
>   displays a currency format.

>   **Quantity** the Amount field in the Node Budget Amounts scrolling window
>   displays a quantity format with two decimal places.

1.  Select whether to view Net Change or Period Balances on the Node Budget
    Amounts scrolling window.

>   **Net Change** the Amount field for a period displays the actual amount
>   assigned to that period.

>   **Period Balances** the Amount field for a period displays the sum of all
>   preceding periods plus the amount assigned to the selected period.

1.  Select the root node in the dimension code tree view to assign the overall
    budget amount. Enter amounts for the root node for each period in the Node
    Budget Amounts scrolling window. Alternatively, you may also enter the
    amounts using the Budget Calculation Methods window. Refer to *Selecting
    calculation methods for budgets* for more information.

>   Once you’ve entered all the period amounts for the root node, you must roll
>   down 100% of each period amount to the first level below the root node.
>   Refer to *Understanding node budget roll down* for more information on how
>   node budget amounts are rolled down.

1.  Enter or select an account in the Account field, if you’ve chosen Account in
    the Budget Level field. You can only select an account that is attached to
    the accounting class to which all the dimensions of the budget tree belong.
    The Enter radio group defaults to Amount if you select a posting account,
    and to Quantity if you select a unit account.

2.  Choose the arrow buttons next to the account field to select the next
    account that you want to assign.

3.  Click the Delete icon next to the account field to delete the displayed
    account from the selected node.

>   *You can assign as many accounts to a node as you like, but the total of all
>   assigned accounts for a period cannot exceed the period amount for the
>   selected node.*

1.  Enter the period amounts to be assigned to the displayed account for the
    selected node in the Node Budget Amounts scrolling window.

2.  Highlight a node on the dimension code tree and choose the Methods button to
    assign period amounts to the node using a calculation method. Refer to
    *Selecting calculation methods for budgets* for more information.

3.  If you have selected Down as the Budget Roll Total option, highlight a node
    on the dimension code tree and choose the Node button to roll down budget
    amounts to the next nodes. You can roll down amounts only if you have
    entered a period amount for the selected node. Refer to *Rolling down node
    budget amounts* for more information. This button is not available if you
    have selected a bottom node on the dimension code tree, or if the selected
    budget level is Account.

4.  Highlight a node on the dimension code tree and choose the Accounts button
    to assign a range of accounts to the node. Refer to *Assigning a range of
    accounts* for more information. This button is not available if the selected
    budget level is Account.

5.  Choose the Copy button to open the Copy Budgets window, where you can copy
    an existing budget with amounts and accounts. Refer to *Copying budgets* for
    more information.

6.  Choose the Export button to export an actual budget to an Excel spreadsheet.
    Refer to *Exporting budget details* for more information.

>   *You cannot export a preliminary budget. Save it to make it an actual budget
>   before exporting.*

1.  Choose the Import button to import a budget from an Excel spreadsheet. Refer
    to *Importing a budget* for more information.

2.  Choose Print to print the Analytical Accounting Budget Maintenance report.
    You can print the report in one of the following formats:

    -   Budget tree with amounts

    -   Budget tree with accounts summary

    -   Budget tree with accounts detail

3.  Choose Delete to delete the budget ID that you have created.

4.  Choose Clear to clear all the information that is displayed on the window.

5.  Choose Save to save the budget ID that you have created.

>   If the root node amount has not been rolled down 100% to the lower nodes for
>   any period, a validation log will print listing all the periods where the
>   budget amount must be rolled down 100%. You cannot save until you’ve
>   completely rolled down the root node amount to the nodes below.

### Copying budgets

>   You can copy a budget that you have previously set up, and modify it for the
>   current year to suit your requirements. You can include opening balances,
>   copy the accounts that were assigned to the previous budget, and increase or
>   decrease the amounts in the budget. The ability to copy budgets is not
>   available for budgets based on a date range.

>   **To copy budgets:**

1.  Open the Copy Budgets window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Budget \>\> Copy button)

2.  The Budget ID, Budget Year and Description fields display the values entered
    in the Analytical Accounting Budget Maintenance window.

>   If this window has opened after you chose Yes on a message asking whether
>   you wanted to copy the previous year’s budget, the Source Budget ID, and
>   Budget Tree ID fields display the values entered in the Analytical
>   Accounting Budget Maintenance window, while the Year field displays the year
>   previous to the year chosen in the Analytical Accounting Budget Maintenance
>   window.

1.  If this window has opened when you chose the Copy button on the Analytical
    Accounting Budget Maintenance window, enter or select the Source Budget ID
    that you want to copy. The Budget Tree ID field displays the corresponding
    values for the selected Source Budget ID.

    -   If the destination budget ID has a budget tree ID attached to it for
        another year, then the source budget ID that you choose must have the
        same budget tree ID attached. If the source budget ID has a different
        budget tree ID, then a message appears asking you to select a budget ID
        with the same budget tree ID.

    -   If the destination budget ID does not have a budget tree attached for
        any other year, then the budget tree ID attached to the source budget ID
        will over write any budget tree ID that you may have assigned to the
        budget ID.

2.  The Year field drop down displays all historic and open years. You can only
    select a year in which the selected Source budget ID has been set up.

3.  Choose the Calculation Option to be used while calculating the budget
    amounts. The options are:

>   **No Amounts** The budget tree will be copied. No amounts will be copied,
>   and the amounts fields will be blank in the Analytical Accounting Budget
>   Maintenance window.

>   **Exact Amounts** The budget tree and the exact amounts will be copied to
>   the Analytical Accounting Budget Maintenance window.

>   **Percentage Change** You can increase or decrease the amounts for the
>   destination budget.

>   *If you choose a calculation option other than No Amounts the amounts will
>   over write any existing amounts in the destination budget ID when you choose
>   Copy.*

1.  If you choose Percentage Change, the Percentage field becomes available, and
    you can enter a percentage value. Choose the Increase or Decrease radio
    options to increase or decrease the source budget ID amounts by the
    percentage you have entered.

2.  Mark the Include Opening Balance option to copy the opening balance from the
    source budget ID. If this option is unmarked, the opening balance will not
    be copied over. If this option is marked, the opening balance will be copied
    over, even if it is zero. The opening balance will be treated as another
    period, and will be affected by the Calculation Method you choose in this
    window.

3.  Mark the Copy Accounts option to copy all the accounts attached to the
    source budget ID to the destination budget ID. This option is not available
    if the source budget ID has no accounts attached to it.

>   *The copied accounts will over write any existing accounts assigned to the
>   destination budget ID when you choose Copy. If you’ve selected No Amounts,
>   then no accounts will be copied over, even if you’ve marked this option.*

1.  Choose Copy to copy all the selected details on the source budget ID to the
    destination budget ID, and close the window. The Analytical Accounting
    Budget Maintenance window displays all the details that have been copied
    over. Nothing will be copied over if you close the window without choosing
    Copy.

2.  Choose Clear to revert all fields to their default values.

### Selecting calculation methods for budgets

>   You can specify one of two methods by which to calculate the budget amounts
>   for each period for a selected node or node/account combination of the
>   budget tree.

>   **To select calculation methods for budgets:**

1.  Open the Budget Calculation Methods window:

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Budget \>\> Methods
>   button)

>   The Budget ID, Description, Budget Year, Budget Tree ID and Selected Node
>   fields display the default values from the Analytical Accounting Budget
>   Maintenance window.

>   If you’re calculating amounts for an account on the selected node, then the
>   selected account and the account description is displayed in the Account and
>   Description fields.

1.  Choose the Calculation Method to be used while calculating the period budget
    amounts. The options are:

>   **Set Amount** The amount you enter in the Amount field will be assigned to
>   each period of the budget for the selected node/ account, including the
>   opening balance if it’s marked.

>   **Yearly Budget Amount** The amount you enter in the Amount field will be
>   split equally over all the periods of the year for the selected
>   node/account, including the opening balance if it’s marked.

1.  Enter the amount in the Amount field. This amount will be distributed among
    all the periods using the method you’ve specified. This field will display
    as Quantity if you’ve selected Quantity in the Enter field, or selected a
    Unit account in the Analytical Accounting Budget Maintenance window.

2.  Mark the Include Opening Balances option to include the opening balance in
    the calculation.

>   *Profit and Loss accounts will not have the opening balance included as a
>   period in their calculations.*

1.  Choose Calculate to calculate the amounts and close the Node Budget
    Calculation Method window. The Analytical Accounting Budget Maintenance
    window displays the calculated amounts for all periods.

2.  Choose Clear to clear all values displayed in this window, and restore the
    default values.

3.  Choose Close to close the window without performing any calculations.

### Understanding node budget roll down

>   You can roll down budget amounts from one node to the codes on the node
>   immediately below it. The amount to be rolled down for the codes is
>   calculated for each period. If a period for a selected node has a zero
>   amount, then no amounts will be rolled down for that period to the lower
>   nodes.

>   Use the following table and information below it to understand how budget
>   amounts on one node are rolled down to the nodes below it.

| **Root Node** | **Nodes Level 1** | **Nodes Level 2** | **Root Node Amount** | **Node Level 1 Amounts** | **Node Level 2 Amounts** |
|---------------|-------------------|-------------------|----------------------|--------------------------|--------------------------|
| Root node     |                   |                   | \$10000.00           |                          |                          |
|               | Node 1Level 1     |                   |                      | \$7000.00                |                          |
|               |                   | Node A Level2     |                      |                          | \$2000.00                |
|               |                   | Node B Level2     |                      |                          | \$1500.00                |
|               | Node 2 Level1     |                   |                      | \$3000.00                |                          |
|               |                   | Node A Level2     |                      |                          | \$1000.00                |
|               |                   | Node B Level2     |                      |                          | \$1000.00                |
|               |                   | Node C Level 2    |                      |                          | \$1000.00                |

>   **Root Node** The amount entered on the root node must be rolled down 100%
>   to the next level nodes, in order to save the budget. You can roll down the
>   amounts manually, or use the Node Budget Roll Down window to roll down the
>   root node amounts. Refer to *Rolling down node budget amounts* for more
>   information.

>   If you increase a period amount on the root node, you must roll down 100% of
>   the new total amount, before you can save the budget.

>   You cannot decrease the period amount on the root node until you reduce the
>   amounts on the lower nodes so that they do not exceed the amount that you
>   have decided to enter on the root node.

>   **Other Nodes** The amount entered on any node other than the root node need
>   not be rolled down 100% to the subsequent nodes. You can use the Node Budget
>   Roll Down window to roll down amounts from any node to the subsequent nodes.
>   Refer to *Rolling down node budget amounts* for more information.

>   You can enter period amounts for any node as long as you’ve assigned amounts
>   for those periods to the nodes on the level above. The following validation
>   takes place when you change period amounts on a node, and the upper and
>   lower nodes have values entered:

-   You can increase the period amount on any node, as long as the period total
    of all the nodes on that level does not exceed the period total of the node
    above.

-   You can decrease the period amount on any node, as long as the period total
    of all the nodes on the level below does not exceed the node total you are
    decreasing.

### Rolling down node budget amounts

>   Use the Node Budget Roll Down window to roll down budget amounts from one
>   node to the codes on the node immediately below it. The amount to be rolled
>   down for the codes is calculated for each period, based on the calculation
>   method you have specified. This window is available only if you have
>   selected Down as the Budget Roll Total option in the Analytical Accounting
>   Budget Maintenance window (Cards \>\> Financial \>\> Analytical Accounting
>   \>\> Budget).

>   **To roll down node budget amounts:**

1.  Open the Node Budget Roll Down window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Budget \>\> Node button)

>   The Budget ID, Description, Budget Year, Budget Tree ID and Selected Node
>   fields display the default values from the Analytical Accounting Budget
>   Maintenance window. The Total field displays the budget total for the
>   selected node.

1.  Choose the Calculation Method you want to use for the roll down, whether
    Percentage Split or Equal Split. The default method is percentage split.

>   You can choose Equal Split only if the amount for each period in the
>   Analytical Accounting Budget Maintenance window is large enough to be
>   divided between the codes listed. If even one period amount is too small, a
>   message appears that you cannot select Equal Split.

1.  The scrolling window displays all the codes for the node immediately below
    the selected node. The percent field displays a zero value by default, with
    two decimal places.

>   **Percentage Split** Enter the percentage to be allocated to each code. If
>   the root node is the Selected Node, then the percentage total must equal
>   100. If any other node is the selected node, the percentage total can be
>   less than or equal to 100, but must not exceed 100. Refer to *Understanding
>   node budget roll down* for more information.

>   **Equal Split** The percent field displays the value obtained by dividing
>   100 by the number of codes. If it is not possible to do an exact equal
>   split, the last dimension code displays the larger amount.

>   *The period amounts on the relevant node in the Analytical Accounting Budget
>   Maintenance window should be large enough to be split by the percentage
>   you’ve entered. If one of the period balances is too small to be divided
>   among all the codes the last code will be allocated 100% of that small
>   amount for the relevant period*.

1.  Choose Assign to calculate the roll down and close the window. The period
    amounts for the codes below the selected node will be updated with the
    amounts calculated as per the method selected. The amounts that are being
    rolled down will overwrite any amounts already entered. In the Analytical
    Accounting Budget Maintenance window, the focus will be on the node that you
    had highlighted.

>   *If the nodes below the nodes that are being rolled down to have amounts
>   assigned, those amounts should not exceed the new amounts being rolled down.
>   If they do, the roll down will not take place. The window will close and
>   focus will return to the node in Analytical Accounting Budget Maintenance
>   window that was originally changed, and the original root node amounts will
>   populate the window.*

### Understanding account budget roll down

>   You can assign a range of posting and/or unit accounts to a selected node,
>   and distribute the amount assigned to that node among these accounts. The
>   amounts can be distributed by an equal split, or by assigning a specific
>   percentage to each account. You can further roll down the assigned accounts
>   and amounts to lower nodes.

>   Use the following examples to understand how amounts are rolled down to
>   accounts.

>   **Rolling down node period amounts to accounts**

>   The period amounts assigned to the selected node in the Analytical
>   Accounting Budget Maintenance window will be distributed among all the
>   selected accounts in the percentage specified on the Account Budget Roll
>   Down window.

>   **Percentage Split** The period amounts on the relevant node should be large
>   enough to be split by the percentage you’ve entered. If one of the period
>   balances is too small to be divided among all the accounts, the last account
>   will be allocated 100% of that small amount for the relevant period.

>   **Equal Split** Each period amount for the selected node will also be
>   divided equally by the number of accounts in the list. If it is not possible
>   to do an exact equal split, the last account will display the larger amount.

>   **Rolling down accounts to lower nodes**

>   You have selected the node PCTR \>\> PROJ in the Budget Tree A \>\> PCTR
>   \>\> PROJ \>\> PROD. The following amounts have been assigned to the nodes
>   for Period 1.

| **Node**                   | **Period 1** |
|----------------------------|--------------|
| PCTR                       | \$10000      |
| PCTR \>\> PROJ             | \$5000       |
| **Node**                   | **Period 1** |
| PCTR \>\> PROJ \>\> PROD A | \$3000       |
| PCTR \>\> PROJ \>\> PROD B | \$2000       |

>   25% of the amount of the node PCTR \>\> PROJ is assigned to Account A
>   -Travel Expenses.:

| **Node**       | **Account No** | **Account Type** | **Period 1** |
|----------------|----------------|------------------|--------------|
| PCTR \>\> PROJ | Account A      | Travel Expenses  | \$1250       |

>   When Include Lower Nodes is marked, the budget for Account A - Travel
>   Expense will be assigned to the lower nodes as follows:

| **Node** | **Account** |
|----------|-------------|


>   **No**

**Account**

>   **Description**

**Period 1**

| PCTR \>\> PROJ             | Account A | Travel Expenses | \$1250 |   |   |
|----------------------------|-----------|-----------------|--------|---|---|
| PCTR \>\> PROJ \>\> PROD A | Account A | Travel Expenses | \$750  |   |   |
| PCTR \>\> PROJ \>\> PROD B | Account A | Travel Expenses | \$500  |   |   |

>   **Rolling down opening balances for posting accounts**

>   In the case of posting accounts, the opening balance amount assigned to the
>   selected node is rolled down only to the balance sheet accounts included in
>   the selected range. This is because Profit and Loss accounts do not have an
>   opening balance. However, you can manually enter an opening balance for
>   Profit and Loss accounts in the Analytical Accounting Budget Maintenance
>   window. Use the following table and examples to understand how the opening
>   balance is divided for different calculation methods.

| **Account type** | **Calculation** |
|------------------|-----------------|


>   **Method**

**How the Opening Balance is divided among balance sheet accounts**

| Posting | Equal Split      | Equally split by the number of balance sheet accounts. Refer to *Example 1*                                                                                               |   |
|---------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| Posting | Percentage Split | Split by calculating the ratio of the percentage assigned to a balance sheet account to the total percentage assigned to all Balance Sheet accounts. Refer to *Example 2* |   |

>   The Budget Tree A has the following nodes under it: PCTR \>\> PROJ \>\> PROD

| **Node**                                    | **Opening Balance** | **Period 1** |
|---------------------------------------------|---------------------|--------------|
| Budget Tree A \>\> PCTR                     | \$10000             | \$50000      |
| Budget Tree A \>\> PCTR \>\> PROJ           | \$5000              | \$3000       |
| Budget Tree A \>\> PCTR \>\> PROJ \>\> PROD | \$3000              | \$2000       |

>   The following accounts are assigned to the node Budget Tree A \>\> PCTR \>\>
>   PROJ:

| **Node: Budget Tree A \>\> PCTR \>\> PROJ** |                  |
|---------------------------------------------|------------------|
| **Account No**                              | **Account Type** |
| Account A                                   | Profit and Loss  |
| Account B                                   | Balance Sheet    |
| Account C                                   | Balance Sheet    |
| Account D                                   | Profit and Loss  |

>   **Example 1**

>   Dividing the opening balance among balance sheet accounts when the
>   calculation method is equal split.

| **Node: Budget Tree A \>\> PCTR** |
|-----------------------------------|


>   **\>\> PROJ**

**Amount assigned per account**

| **Account** | **Account Type** | **Opening Balance** | **Period 1** |
|-------------|------------------|---------------------|--------------|
| Account A   | Profit and Loss  |                     | \$750        |
| Account B   | Balance Sheet    | \$2500              | \$750        |
| Account C   | Balance Sheet    | \$2500              | \$750        |
| Account D   | Profit and Loss  |                     | \$750        |

>   **No**

>   **Example 2**

>   Dividing the opening balance among balance sheet accounts when the
>   calculation method is percentage split.

| **Node: Budget Tree A \>\> PCTR \>\>** |
|----------------------------------------|


>   **PROJ**

**Amount assigned per account**

| **Account** | **Account Type** | **Percentage assigned** | **Opening** | **Period 1** |
|-------------|------------------|-------------------------|-------------|--------------|
| Account A   | Profit and Loss  | 15%                     |             | \$450        |
| Account B   | Balance Sheet    | 20%                     | \$1818.19   | \$600        |
| Account C   | Balance Sheet    | 35%                     | \$3181.19   | \$1050       |
| Account D   | Profit and Loss  | 30%                     |             | \$900        |

>   **No**

>   **Balance**

>   The opening balance for Account B, which is a balance sheet account, is
>   calculated as (20/55)\*5000=1818.19.

>   The opening balance for Account C, which is a balance sheet account, is
>   calculated as (35/55)\*5000=3181.19.

>   No opening balances are calculated for Accounts A and D, which are Profit
>   and Loss accounts.

### Understanding node budget roll up

>   You can roll up budget amounts from the lowest node to the higher nodes till
>   the root node.

>   Use the following table and information below to understand how budget
>   amounts on one node are rolled up to the parent node.

| **Root Node** | **Nodes Level 1** | **Nodes Level 2** | **Root Node Amount** | **Node Level 1 Amounts** | **Node Level 2 Amounts** |
|---------------|-------------------|-------------------|----------------------|--------------------------|--------------------------|
| Root node     |                   |                   | \$10000.00           |                          |                          |
|               | Node 1Level 1     |                   |                      | \$7000.00                |                          |
|               |                   | Node A Level2     |                      |                          | \$2000.00                |
|               |                   | Node B Level2     |                      |                          | \$5000.00                |
|               | Node 2 Level1     |                   |                      | \$3000.00                |                          |
|               |                   | Node A Level2     |                      |                          | \$1000.00                |
|               |                   | Node B Level2     |                      |                          | \$1000.00                |
|               |                   | Node C Level 2    |                      |                          | \$1000.00                |

>   In the above example, the user enters values in Node Level 2 which is the
>   lowest node. These amounts are added up and rolled up to the parent node.
>   This process is repeated until the amount is finally rolled up to the root
>   node.

### Assigning a range of accounts

>   Use the Account Budget Roll Down window to assign a range of accounts to a
>   selected node. The ranges may be based on Accounts, Segment IDs or Account
>   Classes. You can enter more than one range of each type. If an account
>   already exists in the scrolling window, it will not be inserted again even
>   if it is a part of the next chosen range.

*You cannot assign accounts to the root node of the budget tree ID.*

>   **To assign a range of accounts:**

1.  Open the Account Budget Roll Down window.

>   (Cards \>\> Financial \>\> Analytical Accounting \>\> Budget \>\> Accounts
>   button)

>   The Budget ID, Description, Year, Budget Tree ID, Selected Node and Total
>   fields display the default values from the Analytical Accounting Budget
>   Maintenance window.

>   If you have already assigned any accounts manually or in a range to the
>   selected node, then those accounts and the amounts assigned to them are
>   displayed in the scrolling window. The Calculation Method field is blank,
>   and you cannot make any changes to the amounts displayed in the scrolling
>   window.

1.  Choose the Calculation Method you want to use for the account roll down,
    whether Percentage Split or Equal Split.

>   *You can choose Equal Split only if the amount for each period in the
>   Analytical Accounting Budget Maintenance window is large enough to be
>   divided between the accounts listed. If even one period amount is too small,
>   a message appears that you cannot select Equal Split.*

>   If accounts and amounts already exist in the scrolling window, and you
>   select a method, a message appears that the existing amounts will be over
>   written, and whether you want to continue. Choose Yes to continue with the
>   selected method.

1.  Mark the Include Lower Nodes option to assign the range of accounts to all
    nodes below the selected node. The amounts will also be distributed to the
    lower nodes for each period in the same percentage as the selected node.
    Refer to *Rolling down accounts to lower nodes* for more information.

>   *If a lower node does not have an amount assigned to it in the Analytical
>   Accounting Budget Maintenance window, no amounts will be rolled down to that
>   node.*

1.  In the Ranges field, select whether to assign a range based on Account,
    Segment ID or Account Class. If you select Segment, enter the Segment ID.

2.  Enter the range in the From and To fields. The lookup lists only those
    accounts that have already been assigned to the node directly above the
    selected node.

>   If you’ve chosen Amount in the Enter field of the Analytical Accounting
>   Budget Maintenance window, you can only enter a range of posting accounts.
>   If you’ve chosen Quantity, you can only enter a range of unit accounts.

1.  Choose Insert to insert the accounts within the selected range into the
    scrolling window. The scrolling window displays the account and description
    for each account. If you’ve chosen Account Class, all the accounts assigned
    to those classes will be inserted.

>   Once you’ve inserted a range in the scrolling window, you can select another
>   range to insert. The new range will be added below the existing range in the
>   scrolling window.

1.  Enter the percentage to be assigned to each account, if you’ve chosen
    Percentage Split as the calculation method. The percentage total must not
    exceed 100%.

>   If you’ve chosen Equal split, no amounts are displayed in the scrolling
>   window. The total amount will be divided by the number of accounts in the
>   scrolling window when you choose Assign.

>   The node period amounts will be distributed among all selected accounts in
>   the percentage specified here. Refer to *Assigning a range of accounts* for
>   more information.

1.  The Remove and Remove All fields become available only when accounts exist
    in the scrolling window. Select an account in the scrolling window and
    choose Remove to remove that account. Choose Remove All to remove all the
    accounts from the scrolling window.

>   If you insert accounts after assigning percentages, the percentages already
>   assigned will remain, and any new accounts added will have zero percentage
>   assigned to them. If you remove accounts after assigning percentages, the
>   remaining accounts will still have the percentages assigned to them, and the
>   percentage total of the deleted accounts will remain unassigned.

1.  Mark the Include Opening Balance option to roll down opening balances to the
    range of accounts.

>   **Unit accounts** The opening balance is treated as a period and it will be
>   rolled down to all the accounts in the range.

>   **Posting accounts** The opening balances are only rolled down to the

>   Balance Sheet accounts within the selected range. Refer to *Rolling down
>   opening balances for posting accounts* for more information on rolling down
>   opening balances.

1.  Choose Assign to assign the account range to the selected node. The amount
    for each account will be rolled down to each period of the selected node
    that has an amount entered against it. If the selected node has a zero
    amount for a period, the accounts assigned to the node will also have zero
    amounts for that period.

>   If you’ve marked Include Lower Nodes, then the accounts and amounts will be
>   assigned to all nodes below the selected node following the same validations
>   as for the selected node.

>   Once you have chosen a range it is displayed every time you open this window
>   from the selected node, along with the amounts assigned to it. You can add
>   to or remove accounts from the scrolling window or change the calculation
>   method. The changes you make will be effected only when you choose the
>   Assign button.

>   *If any period on a node has an amount or quantity that is too small to be
>   rolled down any further, then it will not be rolled down to nodes below that
>   node.*

1.  Choose the Clear button to clear the values entered in the window, and
    restore the original defaults that were displayed when you opened this
    window.

2.  If you close the window without choosing Assign, all changes you’ve made in
    the window will be lost and no calculation will take place.

### Exporting budget details

>   You can export the details of a budget you’ve set up to a workbook in Excel.

>   **To export budget details:**

1.  Open the Export Budget window. (Cards \>\> Financial \>\>Analytical
    Accounting \>\> Budget \>\> Export button)

>   The Budget ID, Description, Budget Year and Budget Tree ID fields display
>   the default values from the Analytical Accounting Budget Maintenance window.

1.  Mark the Export Accounts option to export the accounts that are attached to
    the budget ID. All the accounts attached to the budget ID will be exported,
    and the Accounts will be displayed at the end of each node of the tree to
    which they have been attached. This field is not available if no accounts
    are attached to the budget ID.

2.  Choose whether you want to export the budget to a new workbook or an
    existing workbook. If you select Existing Workbook, then enter the path name
    and file name of the exiting file. The default path name will be My
    Documents.

>   If you select New Workbook, the path name and file name fields will be
>   unavailable.

1.  Choose OK to export the selected budget to Excel.

2.  Choose Cancel to return to the Analytical Accounting Budget Maintenance
    window without exporting the budget. If you are exporting to a new workbook,
    a new Excel Workbook will open and you will be prompted to save the file.

### Understanding budget import

>   When you select an Excel worksheet to import a budget into Microsoft
>   Dynamics GP, it is successfully imported only if the following conditions
>   are fulfilled:

-   The worksheet should be in one of the following formats:

>   **Template 1** Budget tree with accounts. All the account fields must be
>   filled in. All the accounts in the spreadsheet should belong to an Account
>   Class that is attached to all the dimensions within the budget tree ID. The
>   total amounts entered against the accounts being imported should not exceed
>   the budget total of the relevant nodes.

>   IMAGE – AABIT.jpg

![A screenshot of a computer Description automatically generated](media/6e66a95340ee9afe3d711b9941c545d3.jpg)

A screenshot of a computer Description automatically generated

>   **Template 2** Budget tree without accounts.

IMAGE – AABIT2.jpg

![A close up of a piece of paper Description automatically generated](media/c28cd897162dcd58e59d73992e34fb59.jpg)

A close up of a piece of paper Description automatically generated

-   The budget tree ID in the Budget Tree column of the Excel spreadsheet should
    match the budget tree ID entered against the budget ID in the Analytical
    Accounting Budget Maintenance window.

-   The budget totals entered on each level of the tree within the spreadsheet
    should be less than or equal to the budget totals on the level above. They
    should not exceed the totals on the level above.

-   The amounts in the opening balance and period columns for the root node of
    the spreadsheet, that is the budget tree ID, should be exactly equal to the
    totals of all the budget amounts entered against the next level nodes.

>   If any one of the above conditions is not fulfilled, the worksheet will not
>   be imported, and an Import Error report will be printed listing all the
>   errors.

>   Once the file has been imported into Microsoft Dynamics GP, the following
>   validations will take place:

-   If the imported file is the budget tree format without accounts, but
    accounts have been assigned to the budget ID in Microsoft Dynamics GP, such
    accounts will have their balances reverted to zero. The amounts will be
    imported only against the budget tree.

-   If the imported file is the account- budget tree format, the amounts will be
    imported against the accounts and the tree. If there are accounts attached
    to the budget ID in Microsoft Dynamics GP, any account that does not exist
    in the import file will have its balance reverted to zero. If there are
    accounts within the imported spreadsheet that have not been assigned to the
    budget ID, they will be assigned when the file is imported. Accounts that
    are common to the import file as well as to the budget ID in Microsoft
    Dynamics GP will be assigned the amounts from the import file.

### Importing a budget

>   You can import budget figures from an Excel spreadsheet that has been set up
>   in the correct format. Refer to *Understanding budget import* for an
>   overview of the conditions that must be fulfilled to successfully import a
>   budget.

>   *Be sure not to close the Excel sheet if it appears while importing the
>   budgets. If you do so, an error message appears and the system will stop
>   importing the budgets.*

>   **To import a budget:**

1.  Open the Import Budget window. (Cards \>\> Financial \>\> Analytical
    Accounting \>\> Budget \>\> Import button)

>   The Budget ID, Description, Budget Year and Budget Tree ID fields display
>   the default values from the Analytical Accounting Budget Maintenance window.

1.  Select the path for the Excel file from where you want to import the budget.
    The default path name to select the file is My Documents. If you select a
    document type other than an Excel spreadsheet, a warning message appears and
    you will not be able to select the file.

2.  The Select the Worksheet window lists all the worksheets in the selected
    Excel file. Highlight the worksheet that you want to import and choose OK.

*Be sure not to edit any open Excel file during the import process.*

1.  Choose OK to import the Excel worksheet. If the import is successful, the
    Analytical Accounting Budget Maintenance window will display the fully
    expanded tree, and the root node will be highlighted.

2.  Choose Cancel to return to the Analytical Accounting Budget Maintenance
    window without importing the budget.

Part 2: Transactions
====================

>   This part of the documentation contains information about entering analysis
>   information for transactions in Microsoft Dynamics GP. This information
>   includes the following topics:

-   *Chapter 4, “General Ledger Transactions”* describes how to enter analysis
    information for General Ledger transactions. It also explains how you can
    adjust analysis information for posted journal entries.

-   *Chapter 5, “Payables Management Transactions”* explains how to enter
    analysis information for Payables Management transactions.

-   *Chapter 6, “Purchase Order Processing Transactions”* explains how to enter
    analysis information for Purchase Order Processing transactions.

-   *Chapter 7, “Receivables Management Transactions”* describes how to enter
    analysis information for Receivables Management transactions.

-   *Chapter 8, “Sales Order Processing Transactions”* explains how to enter
    analysis information for transactions in Sales Order Processing.

-   *Chapter 9, “Inventory Transactions”* explains how to enter analysis
    information for Inventory transactions.

-   *Chapter 10, “Fixed Asset Transaction”* explains how to enter analysis
    information for Fixed Asset Transactions

-   *Chapter 11, “Bank Reconciliation Transactions”*explains how to enter
    analysis information for Bank Reconciliation transactions.

-   *Chapter 12, “Cashbook Bank Management Transactions”*describes how to enter
    analysis information for Cashbook Bank Management transactions.

-   *Chapter 13, “Electronic Bank Management.”*describes how to enter analysis
    information for Electronic Bank Management transactions.

-   *Chapter 14, “Direct Debits And Refunds Transactions”*describes the analysis
    information that is created for Direct Debits and Refunds transactions.

-   *Chapter 15, “Analysis information for U.S. Payroll transactions”* describes
    the analysis information that is created for U.S. Payroll transactions.

Chapter 4: General Ledger Transactions
--------------------------------------

>   The various procedures involved in entering analysis information for General
>   Ledger transactions are explained here. You can enter analysis information
>   for distribution accounts that are linked to an account class. You can also
>   adjust analysis information for posted journal entries. Also, you can view
>   the analysis information for a selected account or journal entry.

>   The reports generated using the Distribution and Multilevel queries display
>   analysis information entered in General Ledger.

>   You can open the Analytical Transaction Entry window only if Analytical

>   Accounting has been activated. Refer to *Activating Analytical Accounting*
>   for more information.

>   This information is divided into the following sections:

-   *Entering analysis information for General Ledger transactions*

-   *Validating transactions and correcting errors*

-   *Entering analysis information for Quick Journals*

-   *Entering analysis information for Miscellaneous Checks*

-   *Analysis information in batches*

-   *Voiding an unposted transaction*

-   *Backing out a posted transaction*

-   *Backing out and correcting a posted transaction*

-   *Copying a posted transaction*

-   *Voiding a Quick Journal entry*

-   *Analysis information for writeoffs*

-   *Series posting and master posting*

-   *Adjusting analysis information in posted transactions*

-   *Validating adjustments and correcting errors*

-   *Viewing detail journal entries with analysis information*

-   *Viewing journal entries with analysis information*

-   *Analytical Accounting check links*

-   *Copying Analytical Accounting Information for General Journal*

### Entering analysis information for General Ledger transactions

>   Use the following information to enter analysis information for distribution
>   accounts that are linked to an account class. You can save transactions
>   individually or in a batch with or without analysis information.

IMAGE – AAGL.jpg

![A screenshot of a computer Description automatically generated](media/97b4689fdbffcca4429782637cfff5d8.jpg)

>   The Analytical General Transaction Entry window opens automatically when you
>   press TAB from a field in the Transaction Entry window (Transactions \>\>
>   Financial \>\> General) in the following instances:

-   If an account is linked to an account class and no analysis information has
    been entered for the account earlier.

-   If changes are made to a distribution line that affects analysis information
    entered previously for the line. These include changing the account, amount
    or debit to credit or vice versa, as this will delete the previously entered
    analysis information and create a single assignment of 100 percent.

-   If the option Calculate Taxes in General Ledger is marked in the Company

>   Setup Options window (Administration \>\> Setup \>\> Company \>\> Company
>   \>\> Options), you may need to enter analysis information for distribution
>   accounts that are created from the Tax Entry window. If any of the new
>   distribution accounts are linked to an account class, after the tax
>   transactions are created from the Tax Entry window, the Analytical General
>   Transaction Entry will open automatically from the general Transaction Entry
>   window. If the Analytical General Transaction Entry window has been opened
>   earlier for the distribution accounts, it displays the first of the new
>   distribution accounts that are linked to an account class (as per the
>   distribution sequence). If not, the first of the previous distribution
>   accounts linked to an account class will be displayed.

>   If you delete a transaction in the General Ledger Transaction Entry window,
>   any analysis information entered for the transaction is also deleted.

>   For multicurrency transactions, a change in the transaction date re-creates
>   distribution amounts due to a change in the exchange rate. If the
>   transaction date is modified, analysis information created previously is
>   deleted when the distribution amounts are re-created.

>   **To enter analysis information for General Ledger transactions:**

1.  Open the Analytical General Transaction Entry window.  
    (Transactions \>\>Financial \>\> General \>\> Enter account/amount \>\>
    Choose the Analytical Accounting button)  
    (Transactions \>\>Financial \>\> General \>\> Enter account/amount \>\>
    Additional \>\> Analytical Transaction or CTRL+T)

2.  The Analytical General Transaction Entry window displays the distribution
    account selected in the General Transaction Entry window. To view the other
    distributions for the transaction, enter or select a distribution number.

>   The sequence of distributions in the Analytical General Transaction Entry
>   window may not correspond to the sequence in the General Transaction Entry
>   window because only accounts linked to an account class are displayed in the
>   Analytical General Transaction Entry window.

>   **The Originating or Functional Amount field** displays the distribution
>   amount in the originating or functional currency based on the option
>   selected in the currency view.

>   *You can choose the expansion button to view multicurrency information if
>   the originating currency differs from the functional currency. The currency
>   icon is not displayed if the displayed distribution account is a unit
>   account.*

**The Company ID field** displays the ID for the current company.

>   **The Account field** displays the account related to the distribution. The
>   expansion button will open the Microsoft Dynamics GP Account Entry window.
>   The balance type, whether debit or credit, is also displayed.

>   **The Assigned field** displays the total distribution amount in value and
>   percentage that has been assigned.

>   **The Unassigned field** displays the remaining distribution amount that is
>   to be assigned in value and percentage.

>   In the assignment list view, an arrow before the Number field indicates that
>   the analysis information displayed is for the selected assignment. Each
>   assignment created for the distribution is displayed separately.

1.  In the list window, enter the transaction distribution amount in functional
    or originating currency, by value or on a percentage basis.

**The Number field** displays the number of the assignment.

>   **The Originating or Functional Amount field** in the assignment list view,
>   displays the assignment in the originating or the functional currency based
>   on the option you selected in the Currency View. Enter the amount to assign
>   in the Originating/Functional Amount field. Assignments can be entered in
>   the functional or originating currency.

*You can enter the assignment either in value or percentage terms.*

1.  Enter the assignment in percentage value in the Assign% field. Initially, a
    single assignment is created by default. You can overwrite the assignment
    with more than one assignment.

>   You can save analysis information for a distribution even if the assignment
>   is not 100%. However, you can post a transaction with partial assignments
>   only if you have opted to allow partial assignments during posting for the
>   module you’re working in. Refer to *Setting up assignment options* for more
>   information.

1.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes
    if required. Refer to *Creating an alias* for more information.

2.  Enter reference information for the assignment in the Reference field.

3.  Choose Delete Row to delete a single row in the assignment List View. You
    cannot choose this option if only a single assignment has been entered.

4.  Choose Remaining to add one assignment for the remaining unassigned amount.
    The new assignment will ensure that the total assigned amount equals the
    distribution amount. For example, the distribution amount is \$100 and
    you’ve entered four assignments that total \$75. When you choose Remaining,
    a fifth assignment for the remaining value, \$25 is created. This button is
    not available if the distribution field is blank or has a zero value.

5.  Choose Default to load the current setup information specified for the
    account class in the Accounting Class Maintenance window and create a single
    assignment. The following processes will occur:

    -   Fixed, Required, and Optional Transaction Dimensions (including hidden
        transaction dimensions) will be installed.

    -   All the assignments that you have created for the current distribution
        will be removed and create a single assignment that is equal to the
        distribution amount will be created.

    -   If the analysis type is changed to or from Not Allowed, transaction
        dimensions will be added or removed.

    -   Transaction dimensions that have been deleted will be removed.

6.  The Trx Dimension field displays transaction dimensions for the account
    class that the distribution account is linked to. Only transaction
    dimensions that have been set as Required, Fixed, or Optional are displayed.

7.  The Transaction Dimension Description field displays the description of the
    Transaction Dimension that you’ve entered in the Transaction Dimension
    Maintenance window.

8.  Enter or select the code for each Alphanumeric transaction dimension in the
    Alphanumeric column. If you’ve marked the Show valid code combinations in
    trns and budgets option in the Analytical Accounting Options window, then
    the lookup window will display only those codes that have a valid
    combination with the codes you have already selected for the transaction.

>   *Security access to use a transaction dimension code is granted
>   automatically to the user who created the code during transaction entry.*

1.  Enter a transaction dimension code in the Numeric, Yes/No or Date field for
    a Numeric, Boolean or Date type Transaction Dimension.

2.  Choose OK to save your changes and close the window. The analysis
    information that you have entered is validated when you choose OK. Refer to
    *Validating transactions and correcting errors* for more information.

3.  Choose Save to save the analysis information you have entered and clear the
    window. A validation takes place when you choose Save in the Analytical
    General Transaction Entry window. Refer to *Validating transactions and
    correcting errors* for more information. You can save the analysis
    information with errors or without updating changes made to the account
    class.

4.  Choose Clear to clear the information from the Analytical General
    Transaction Entry window.

5.  Choose Validate to validate the analysis information of the distribution
    displayed in the window. If changes are made to the account class in the
    Analytical Accounting setup or errors are found during the validation
    process, the Analytical Accounting Validation Log window will open where you
    can view the errors or changes. Refer to *Validating transactions and
    correcting errors* for more information about validation.

>   Choose Print to print the error report. Choose OK to close the window and
>   return to the Analytical General Transaction Entry window.

1.  To view the changes to the account class choose the Default button in the
    Analytical General Transaction Entry window. Double click on an Analytical
    Accounting error to open the Analytical Accounting General Transaction Entry
    window where the specific error will be highlighted

2.  Choose the printer icon button to print the Analytical Accounting edit list
    for the current distribution displayed or for all distributions of the
    transaction linked to an account class. The Analytical Accounting Validation
    Log report which describes the Analytical Accounting errors also is printed.

>   If you post a reversing transaction or reverse an existing transaction, the
>   analysis information is copied from the transaction to the reversed
>   transaction with the change in balance type, whether debit or credit.

>   If you void a transaction that has been posted to General Ledger, a
>   reversing transaction is created along with any analysis information
>   assigned to the original transaction.

>   On posting Clearing Journals, analysis information that has been entered for
>   the transactions will not be posted. Also, no validation will take place for
>   the distribution accounts, even if the accounts are linked to an account
>   class. To post analysis information, use the general Transaction Entry
>   window (Transactions \>\> Financial \>\> General).

### Validating transactions and correcting errors

>   You can validate a transaction document by selecting the transaction in the
>   relevant

>   Analytical Accounting Transaction Entry window and choosing Additional \>\>
>   Run Validation or by pressing CTRL+R. You can validate a transaction
>   distribution by choosing OK, Save or Validate, only if it has an amount.

>   The validation process verifies the following information:

-   The assignments that you’ve created conform to the assignment options you
    have set up for the module.

-   Codes are specified for all transaction dimensions that have a required
    status.

-   The code combinations are valid.

-   All the alphanumeric codes have access to the relevant user ID and
    distribution account.

-   That accounts associated with the transaction are still linked to an account
    class.

-   The transaction dimensions and codes have not been deleted from the setup.

-   The multicurrency information for Analytical Accounting and Microsoft
    Dynamics GP is the same.

-   There is a distribution record and at least one assignment record for all
    the Microsoft Dynamics GP distributions.

-   All distributions, assignments and codes link to existing Microsoft Dynamics
    GP distribution.

-   Changes that were made to the analysis type of the transaction dimension are
    invalid.

>   The validation routine takes place in the following stages:

>   **Stage one** At the first stage, changes in setup are verified. If any
>   changes have been made, then you must click the Default button in the
>   Analytical Transaction Entry window to update the window with changes.

>   **Stage two** At the second stage, the validation routine checks whether
>   code combinations are valid and selected codes exist and have the required
>   access to user ID and account; if codes have been entered for required
>   transaction dimensions and if assignments equal the transaction distribution
>   amount. This part of validation takes place only after all errors that are
>   indicated at the first stage have been corrected.

>   When you post a general transaction, a validation takes place for the entire
>   document. The document is posted if no errors are found in the transaction.

>   If errors are found while posting a general entry transaction, the
>   transaction will not be posted. The Analytical Accounting Validation Log
>   window will open. The Microsoft Dynamics GP errors will be listed first in
>   the window and then the Analytical Accounting errors.

>   We recommend that you resolve the Microsoft Dynamics GP errors before you
>   correct the Analytical Accounting errors.

>   To correct an Analytical Accounting error, double-click on the relevant
>   error to open the Analytical General Transaction Entry window. The specific
>   distribution where the error exists is displayed.

### Entering analysis information for Quick Journals

>   Use the following information to enter analysis information for distribution
>   accounts in the Analytical Quick Journal Entry window. The Analytical Quick
>   Journal window is similar to the Analytical General Transaction Entry
>   window. Refer to *Entering analysis information for General Ledger
>   transactions* for more information.

>   **To enter analysis information for Quick Journals**

1.  Open the Analytical Quick Journal Entry window.  
    (Transactions \>\> Financial \>\> Quick Journal \>\> Choose the Analytical
    Accounting button)  
    (Transactions \>\> Financial \>\> Quick Journal \>\> Additional \>\>
    Analytical Transaction or CTRL+T)

IMAGE – AAQJ.jpg

![A screenshot of a computer Description automatically generated](media/ef36732ec761feef512536666e7f26fb.jpg)

>   The Analytical Quick Journal Entry window will open only if you have entered
>   an account and amount in the scrolling window of the Quick Journal Entry
>   window.

>   The Analytical Quick Journal Entry window displays the first account linked
>   to a class ID in the accounts scrolling window.

1.  Enter or select a distribution number. If you click Offset to open the
    Analytical Transaction Entry window and lookup, only one distribution is
    displayed. If the window and lookup window are opened from the main
    distribution account, then only the main distribution accounts are
    displayed.

2.  Choose Browse to view the remaining distributions. If you browse when the
    main account is displayed, you cannot view the control account distribution.
    Similarly, if you choose to browse when the control account is displayed,
    you cannot view the main account distribution.

>   The total number of distributions, including all accounts of the document
>   linked to an account class is displayed in the Distribution of field.

1.  Enter the percentage to assign in the Assign% field. You can view the total
    of the assignments in percentage. Assignment can be given in amount or
    percentage.

2.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes
    if required. Refer to *Creating an alias* for more information.

3.  Enter a reference for the assignment in the Reference field.

4.  Choose Remaining to add one assignment for the unassigned balance amount.
    You can assign an amount in a new assignment line and you can modify the
    assignment line.

5.  Choose Default to remove all the assignments for a given distribution line
    and to create a new assignment amount of 100%. Refer to *Entering analysis
    information for General Ledger transactions* for more information about the
    Default button.

6.  The Trx Dimension field will display transaction dimensions for the account
    class to which the distribution account is linked. Transaction dimensions
    that have been set as Required, Fixed, or Optional will be displayed.

>   The default transaction dimensions are displayed in the Trx Dimension Code
>   field.

1.  Enter the transaction dimension code for an alphanumeric transaction
    dimension in the Alphanumeric field. You can click the alphanumeric link to
    open the Transaction Dimension Code window to view information about an
    existing code. The Alphanumeric column is available only for an alphanumeric
    transaction dimension

>   Security access to use a transaction dimension code is granted automatically
>   to the user who created the code during transaction entry.

1.  Enter a transaction dimension code in the Numeric, Yes/No or Date field for
    a Numeric, Boolean or Date type Transaction Dimension.

2.  Choose the Show button to view the description of the transaction dimensions
    in the Trx Dimension field. You can view the description of a transaction
    dimension code in the Trx Dimension Code Description field.

3.  When you open the Analytical Quick Journal Entry window from any
    distribution line, you can use the Offset Acct. button to assign an
    Analytical Accounting assignment to an offset account. The Offset Acct.
    button is not available if the control total is zero. Control total is the
    net total of debits and credits.

4.  When you click Offset Acct., the Main button becomes available. You can
    switch between the main and offset accounts and enter Analytical Accounting
    assignment by clicking this button.

5.  If the offset account is linked to an account class, and the control total
    is not entered, the control total amount is calculated when you choose Post
    or Save and the Analytical Transaction Entry window opens.

6.  Choose the printer icon button in the Quick Journal Entry window to print
    the Quick Journal Entry edit list and the Analytical Accounting edit list. A
    validation takes place for the entire document before the Analytical
    Accounting assignment in the distribution accounts is printed. Assignments
    with errors as well as the ones without errors will be printed.

7.  Choose OK to save the changes and to close the window. Choose Continue to
    close the window or No to keep the window open.

8.  Choose Clear to clear the entries you’ve made in the window.

>   When you post a quick journal, a validation takes place for the entire
>   document. The document would be posted if no errors occur in the Microsoft
>   Dynamics GP transaction and in the Analytical Accounting assignments. You
>   can print the Quick Posting Journal and the Analytical Accounting posting
>   journal reports if you close the Quick Journal Entry window after posting.
>   Refer to *Validating transactions and correcting errors* for more
>   information.

### Entering analysis information for Miscellaneous Checks

>   Use the Analytical Miscellaneous Check Entry window to enter analysis
>   information for the distribution accounts used in miscellaneous checks. You
>   can create assignments, enter transaction dimension codes and references for
>   accounts that are linked to an account class. The Analytical Miscellaneous
>   Check Entry window does not support multicurrency since miscellaneous checks
>   do not support multicurrency.

>   The Analytical Miscellaneous Check Entry window opens automatically when you
>   press TAB in the Miscellaneous Checks (Transactions \>\> Financial \>\>
>   Miscellaneous Checks) window in the following instances:

-   If an account is linked to an account class and no analysis information has
    been entered for the account earlier.

-   If changes are made to a distribution line that affects analysis information
    such as account or amount or type of amount created previously for such
    line.

>   The analysis information is deleted if the distribution line is deleted, and
>   you do not post the document. The analysis information you’ve entered is
>   validated before you post the transaction. Refer to *Validating transactions
>   and correcting errors* for more information.

>   *The analytical information for miscellaneous checks cannot be voided since
>   you cannot void miscellaneous checks.*

>   **To enter analysis information for Miscellaneous Checks:**

1.  Open the Analytical Miscellaneous Check Entry window.  
    (Transactions \>\> Financial \>\> Miscellaneous Check \>\> CTRL+T or
    Additional \>\>Analytical Transaction)  
    Refer to *Entering analysis information for General Ledger transactions* for
    more information.  
      
    IMAGE – AAMC.jpg

![](media/4f0bb1113c8457c9f1e66ad5e9742a04.jpg)

>   A screenshot of a computer Description automatically generated

1.  You can also edit the analysis information you’ve entered in the Analytical
    Miscellaneous Check Entry window before you post the transaction.

### Analysis information in batches

>   The following section deals with information specific to batches. To enter
>   analysis information for individual transactions, refer to *Entering
>   analysis information for General Ledger transactions* .

>   To print the Analytical Accounting Edit List and Analytical Accounting error
>   list along with the Microsoft Dynamics GP edit list for a selected batch,
>   choose the printer icon button in the Analytical Transaction Entry window.
>   You can correct the Analytical Accounting errors by selecting the batch and
>   then correcting each of the transactions that have errors.

>   When you post a batch from the Batch Entry window (Transactions \>\>
>   Financial \>\> Batches), a validation will take place for all the
>   transactions saved in the batch. Microsoft Dynamics GP and Analytical
>   Accounting transactions without errors will be posted and the Analytical
>   Accounting General Posting report will be printed along with the Microsoft
>   Dynamics GP reports. If errors are found during the validation process, an
>   error list report is printed listing analysis errors for the transaction
>   distributions in the batch being posted. You can correct the errors by
>   modifying the transactions in the window where the transaction originated
>   from.

>   If you delete a single or recurring use batch or a transaction within such
>   batches, the analysis information entered for the transaction distributions
>   in the batch or for the transaction also will be deleted.

>   You can save a transaction in a batch with Analytical Accounting errors but
>   cannot post the transaction.

>   For a recurring batch, the analysis information of the batch last posted
>   will be retained and will update each subsequent batch that is posted,
>   unless changes are made to the analysis information in the batch.

>   Analysis information that originated in the subsidiary modules can be viewed
>   in the General Ledger. Such information can be modified prior to updating
>   General Ledger.

### Voiding an unposted transaction

>   You can void a transaction saved in General Ledger using the Transaction
>   Entry window. You also can void transactions that originated in other
>   modules in this window, if you’ve marked the Void/Correcting of Subsidiary
>   Transactions option in the General Ledger Setup window (Administration \>\>
>   Setup \>\> Financial \>\> General Ledger). The analysis information for the
>   transaction voided in the General Ledger will not be updated in the
>   subsidiary module.

>   When you void a transaction with analysis information and close the
>   Transaction Entry window, the Analytical Accounting Posting Journal will be
>   printed along with the Microsoft Dynamics GP Posting Journal. The Analytical
>   Accounting Posting Journal will only display the journal number and the
>   account for the transaction. When you void a transaction in a batch, the
>   analysis information for the voided transaction will be deleted.

### Backing out a posted transaction

>   You can back out a transaction posted in General Ledger using the General
>   Ledger Transaction Entry window. You also can back out a posted transaction
>   that originated in a subsidiary module using the Transaction Entry window,
>   if you’ve marked the Void/Correcting of Subsidiary Transactions option in
>   the General Ledger Setup window (Administration \>\> Setup \>\> Financial
>   \>\> General Ledger).

>   When you back out a posted transaction with analysis information, the
>   transaction dimension codes in the posted transaction will be copied from
>   the backed out transaction to the new transaction that is created. You
>   cannot open the Analytical General Transaction Entry window for the backed
>   out transaction. The analysis information will not be validated when you
>   post the backed out transaction.

### Backing out and correcting a posted transaction

>   You can back out and correct a transaction posted in General Ledger using
>   the General Ledger Transaction Entry window. You can also back out and
>   correct a posted transaction that originated in a subsidiary module in this
>   window, if you’ve marked the Void/Correcting of Subsidiary Transactions
>   option in the General Ledger Setup window (Administration \>\> Setup \>\>
>   Financial \>\> General Ledger).

>   When you back out and correct a posted transaction with analysis
>   information, the transaction dimension codes in the posted transaction will
>   be copied to the reversing transaction that is created. You cannot open the
>   Analytical General Transaction Entry window for the backed out transaction.
>   The analysis information will not be validated when you post the backed out
>   transaction.

>   Also, a new correcting transaction is created using the debits and credits
>   of the original transaction. However, the analysis information will not be
>   copied to the correcting transaction, which will be treated as a new
>   transaction. You need to enter analysis information for the new transaction
>   in General Ledger. Refer to *Entering analysis information for General
>   Ledger transactions* for more information.

### Copying a posted transaction

>   When you copy a saved or posted transaction, the analysis information for
>   the source transaction will not be copied to the new transaction. You need
>   to enter analysis information for the new transaction in the General Ledger.
>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information.

### Voiding a Quick Journal entry

>   You can void a saved Quick Journal entry using the Quick Journal Entry
>   window.

>   When you void a transaction with analysis information and close the Quick
>   Journal Entry window, the Analytical Accounting Posting Journal will be
>   printed along with the Microsoft Dynamics GP Posting Journal. The Analytical
>   Accounting Posting Journal will display only the journal number and the
>   account for the transaction. When you void a transaction in a batch, the
>   analysis information for the voided transaction will be deleted.

### Analysis information for writeoffs

>   When you process writeoffs for underpayments or overpayments, the Analytical
>   Accounting validation process will take place. If the distribution accounts
>   for the writeoffs are linked to an account class ID, the default analysis
>   codes for the account class will be loaded for the distribution accounts.
>   The Analytical Accounting validation will not run if the distributions are
>   linked to an account class ID, but the default codes for the account class
>   ID to which the distributions are linked are not specified.

>   The Analytical Transaction Entry window will not open when you process
>   writeoffs from the Write Off Documents window. A single assignment of 100
>   percent will be created for every distribution account that is linked to an
>   account class.

>   When you process writeoffs, the Analytical Accounting Posting Journal is
>   printed, along with the Microsoft Dynamics GP Posting Journal, if you have
>   marked the option to print the report in the Posting Setup window
>   (Administration \>\> Setup \>\> Posting \>\> Posting).

>   If you have marked the Post Through GL option for Receivables Apply Docs in
>   the

>   Posting Setup window, the Analytical Accounting validation takes place and
>   the

>   Analytical Accounting Posting Journal is printed along with the Microsoft
>   Dynamics GP Posting Journal when you process a writeoff. If the default
>   codes for the distribution accounts linked to an account class are not
>   entered, the Analytical Validation log will be printed displaying the
>   errors, and the transaction will not be posted to the General Ledger.

### Series posting and master posting

>   When you select multiple batches to post from the Series Posting or Master
>   Posting window, batches with analysis information are validated. If errors
>   are found in the batch, the status of the batch automatically changes to
>   available.

>   When you choose the Mark All button, only General Ledger batches without
>   Analytical Accounting errors are selected. You can print the Analytical
>   Error Log to view and correct the Analytical Accounting errors in the other
>   General Ledger batches, before you can select them for posting.

>   The Analytical Accounting Posting Journal is printed for all transactions
>   that have been successfully posted in each batch.

### Adjusting analysis information in posted transactions

>   You can enter or edit analysis information for all journal entries posted
>   from General Ledger, irrespective of their originating module.

>   *In the case of Balance Brought forward journal entries, you can enter the
>   analysis values only for transaction dimensions other than alphanumeric. The
>   analysis data for alphanumeric transaction dimensions is consolidated and
>   brought forward when you perform the year-end close. Refer to Year-end close
>   for Analytical Accounting for more information.*

>   You can also change the number of assignments and the value of each
>   assignment for entries that have existing analysis information. Thus, any
>   analysis information that you have entered for a posted transaction in a
>   module, say, Receivables Management or Payables Management, can be adjusted
>   after you’ve posted the transaction from General Ledger. You can add or
>   remove transaction dimensions, and also change the transaction dimension
>   codes for those dimensions that have the Allow Adjustments option marked on
>   the Transaction Dimension Maintenance window. Refer to *Defining transaction
>   dimensions* for more information.

>   You can modify the analysis information for a journal entry as often as
>   required. Once you post an adjustment, the analysis information that you’ve
>   entered will override the previous analysis information.

>   *Analytical information can be adjusted only for those distribution accounts
>   of a journal entry that are linked to an accounting class at the time of
>   adjustment.*

>   **To adjust analysis information in posted transactions:**

1.  Open the Analytical Adjustment Entry window.  
    (Transactions \>\> Financial \>\> Analytical Accounting \>\> Edit Analysis)

>   IMAGE – AAAE.jpg

![](media/2d16bd10e7ba09c1c015aa0fd81672c7.jpg)

>   A screenshot of a computer Description automatically generated

>   Enter the open year for which to view transactions. All open years for the
>   company are listed in the drop down.

1.  Enter or select the journal entry number for which to enter or edit the
    analysis information. The following values default on selecting a journal
    entry:

>   **The Transaction Date field** displays the transaction date of the journal
>   entry. Any adjustments to the analysis information will also have the
>   transaction date.

>   **The Audit Trail Code field** displays the Analytical Accounting audit
>   trail code if the selected journal entry has existing analysis information.
>   This field is blank if no analysis information exists for the selected
>   journal entry.

>   **The Distribution field** displays the first distribution account of the
>   selected journal entry. You can view all distributions for a journal entry,
>   however, you can adjust analysis information only for those distributions
>   that are linked to an accounting class.

>   **The Originating or Functional Amount field** displays the distribution
>   amount in the originating or functional currency based on the option
>   selected in the currency view. You cannot edit this amount.

>   *Choose the expansion button to view multicurrency information if the
>   originating currency differs from the functional currency. If the Analytical
>   Adjustment Entry window is opened for a unit account, the currency icon is
>   not displayed. You cannot edit the multicurrency information, and
>   conversions for adjusted assignments will take place using the same rate.*

>   **The Company ID field** displays the ID for the current company.

>   **The Account field** displays the account related to the distribution. The
>   expansion button will open the Microsoft Dynamics GP Account Entry window.
>   The balance type, whether debit or credit, is also displayed.

>   **The Assigned field** displays the total distribution amount in value and
>   percentage that has been assigned. This field is blank if no analysis
>   information exists for the selected journal entry.

>   **The Unassigned field** displays the distribution amount that is not
>   assigned in value and percentage.

1.  In the assignment list view, enter the transaction distribution amount for
    an assignment in functional or originating currency, by value or on a
    percentage basis. Each assignment created for the distribution is displayed
    separately.

>   **The Number field** displays the number of the assignment. When you enter a
>   new assignment for an account that already has one assignment, the
>   analytical information from the first assignment automatically defaults on
>   to the new assignment. You can edit this information.

>   An arrow before the Number field indicates that the analysis information
>   displayed is for the selected assignment.

>   **The Originating or Functional Amount field** displays the assignments
>   originally posted for the selected account. Enter or edit the amount
>   assigned in the Originating/Functional Amount field. You can enter
>   assignments in the functional or originating currency based on the option
>   you selected in the Currency View.

>   **The Assign% field** displays the assignments originally posted for the
>   selected account. You can overwrite these assignments.

>   You can enter the assignment either in value or percentage terms.

>   **Alias field** Displays the alias. The Alphanumeric field in the scrolling
>   window displays the transaction dimension codes that are associated with the
>   alias for the transaction dimensions displayed. You can change these codes
>   if required. Refer to *Creating an alias* for more information.

>   **The Reference field** displays the information entered for the existing
>   assignments. You can change this information for existing assignments, and
>   add new reference information for any new assignments that you create.

>   The assignment option you’ve saved for General Ledger determines whether the
>   distribution amount must be assigned fully, or can be assigned partially.
>   Refer to *Setting up assignment options* for more information.

1.  Choose Delete Row to delete a selected row in the assignment list view. You
    cannot choose this option if only a single assignment has been entered.

2.  Choose Remaining to add one assignment for the remaining unassigned amount.
    The new assignment will ensure that the total assigned amount equals the
    distribution amount. For example, the distribution amount is \$100 and
    you’ve entered four assignments that total \$75. When you choose Remaining,
    a fifth assignment for the remaining value, \$25 is created. This button is
    not available if the distribution field is blank or has a zero value.

3.  Choose Default to load the current setup information specified for the
    account class in the Accounting Class Maintenance window and create a single
    assignment. The following processes will occur:

    -   Fixed, Required, and Optional Transaction Dimensions (including hidden
        transaction dimensions) will be installed.

    -   All the assignments that you have created for the current distribution
        will be removed and a single assignment that is equal to the
        distribution amount will be created.

    -   If the analysis type is changed to or from Not Allowed, transaction
        dimensions will be added or removed.

    -   Transaction dimensions that have been deleted will be removed.

4.  Enter or select an existing transaction dimension in the Trx. Dimension
    field to add it to the analytical account if required. You can only select
    transaction dimensions whose analysis type is set as Required, Fixed, or
    Optional for the account class that the distribution account is linked to.

>   You can also remove a transaction dimension from the scrolling window if it
>   is no longer needed.

>   The Transaction Dimension Description field displays the description of each
>   Transaction Dimension that is listed.

1.  Enter or edit the transaction dimension code for each transaction dimension
    listed in the Trx Dimension field if required. Entering a code is optional,
    except for those transaction dimensions that have the analysis type set to
    Required.

>   You can add new alphanumeric codes on the fly if you’ve selected that option
>   in the Transaction Dimension Maintenance window. You can only edit an
>   alphanumeric code that the user ID you’re logged in as and the selected
>   distribution account, both have access to. Refer to *Setting up user access
>   to codes* , and *Setting up account access to codes* for more information.

1.  Choose Validate to validate the analysis information of the analytical
    account displayed in the window. The Analytical Accounting Validation Log
    Report is displayed if errors are found in the analysis information entered.
    Refer to *Validating adjustments and correcting errors* for more
    information.

2.  Choose the printer icon to print the Analytical Adjustment Entry edit list
    for the current distribution displayed or for all distributions of the
    journal entry that can be adjusted. The Analytical Accounting Validation Log
    report which describes the Analytical Accounting errors also is printed if
    errors exist.

3.  Choose Clear to clear all the values entered that you’ve not saved. If
    you’ve saved any changes to a selected journal entry, you cannot clear this
    window until you’ve posted or deleted such saved changes.

4.  Choose Save to save the changes you’ve made to the analysis information of
    all the analytical accounts of the journal entry. You can only save changes
    for one journal entry at a time. You must post or delete these changes
    before you can make changes to another journal entry.

>   The analysis information that you have entered is validated when you choose
>   Save. You can save with errors, but you cannot post until all the errors
>   have been corrected.

1.  Choose Post to post your changes and close the window. The analysis
    information that you have entered is validated when you choose Post. You can
    post a partial assignment if you have allowed partial assignments in General
    Ledger on the Assignment Setup window.

>   *Until you post an adjustment, the analysis information last posted with the
>   journal entry will be available for inquiry and reporting.*

1.  Choose Delete to delete any adjusted analytical information for the journal
    entry. Any analytical information entered for the journal entry when it was
    last posted will be retained.

### Validating adjustments and correcting errors

>   You can validate an adjustment by choosing the Additional \>\> Run
>   Validation or by pressing CTRL+R. You can also validate an adjustment by
>   choosing the OK, Save or Validate buttons.

>   If errors are found while posting, the adjustment will not be posted. The
>   Analytical Accounting Validation Log window will open, listing all the
>   errors found.

>   To correct an Analytical Accounting error, double-click on the relevant
>   error to open the Analytical Adjustment Entry window. The specific
>   distribution where the error exists is displayed. You can post the
>   adjustment only after all the errors have been resolved.

>   The validation process verifies the following information for each
>   analytical account that has been adjusted:

-   The transaction dimensions of the analytical account are active or have not
    been deleted.

-   Transaction dimension codes have been entered for all those transaction
    dimensions where Code Required During Adjustment has been marked on the
    Transaction Dimension Maintenance window.

-   The transaction dimension codes used are active.

-   The analytical account has access to the transaction dimension codes that
    have been entered.

-   The user making the adjustments has access to the transaction dimension
    codes that have been entered.

-   The combination between the transaction dimension codes of the alphanumeric
    transaction dimensions is valid.

-   If Full Assignment is opted for in General Ledger, then the total of all
    assignments entered for the analytical account equals the distribution
    amount of the account.

### Viewing detail journal entries with analysis information

>   Use the Analytical Accounting Detail Journal Entry Inquiry window to view
>   analysis information of an account for the current year or for a closed year
>   from the Transaction Entry Zoom window. Refer to *Transferring analysis
>   information for closed years to history* for more information on year end
>   closing process.

>   This window only will display those distribution accounts of a Journal Entry
>   that comprise analysis information.

>   **To view detail journal entries with analysis information:**

1.  Open the Analytical Accounting – Detail Journal Entry Inquiry window.  
    (Inquiry \>\> Financial \>\> Detail \>\> Select an account and Year \>\>
    Click the Journal Entry link \>\> Select account \>\> CTRL+T)  
    (Inquiry \>\> Financial \>\> History Detail \>\> Select an account and Year
    \>\> Click the Journal Entry link \>\> Select account \>\> CTRL+T)

>   The Analytical Detail Inquiry window displays all analysis information that
>   has been entered for the distribution account. The Journal Entry field
>   displays the Journal Number.

1.  The Reporting Ledger field displays the reporting ledger assigned to the
    General Ledger transaction in the General Ledger transaction entry window
    (Transactions \>\> Financial \>\> General). Refer to the General Ledger
    documentation for more information.

>   This field is available only if you have marked the Allow check box for the
>   Reporting Ledger option in the General Ledger Setup window (Administration
>   \>\> Setup \>\> Financial \>\> General Ledger).

1.  Enter or select a distribution for the Journal Entry.

2.  The Account field displays the account related to the distribution. Choose
    the expansion button to open the Microsoft Dynamics GP Account Entry window.

>   The Audit Trail Code field displays the Analytical Accounting Audit Trail
>   Code.

>   *An Audit Trail Code is created for each Journal Entry made in Analytical
>   Accounting. This Audit Trail is separate from the one created by Microsoft
>   Dynamics GP.*

1.  The Transaction Date field displays the transaction date of the selected
    Journal Entry

2.  The Company ID field displays the ID for the current company.

3.  The Originating or Functional Amount field displays the distribution amount
    in the originating or functional currency based on the option selected in
    the Currency View. Choose the expansion button to view multicurrency
    information if the originating currency differs from the functional
    currency. When the Analytical Accounting-Journal Entry Inquiry window is
    opened for Unit Accounts, the currency information will not be available.

4.  Choose Expand to display all analysis information entered for the
    distribution account in the list window which includes assignments,
    reference information entered per assignment, transaction dimensions and
    their codes.

5.  Choose Collapse to display analysis information entered per assignment.

6.  You also can view all information entered for each assignment or just
    reference information that may exist. Choose the plus button (+) available
    next to each assignment to view all analysis information entered for an
    assignment or choose the minus button (-) to view only reference
    information.

### Viewing journal entries with analysis information

>   You can view analysis information for posted transactions in the Analytical
>   Accounting Journal Entry Inquiry window.

>   **To view journal entries with analysis information:**

1.  Open the Analytical Accounting-Journal Entry Inquiry window.  
    (Inquiry \>\> Financial \>\> Journal Entry Inquiry \>\> CTRL+T)  
    (Inquiry \>\> Financial \>\> Analytical Accounting \>\> Journal Entry)

2.  The Journal Entry field displays the Journal Number selected. Enter or
    select a Journal Entry Number of an open Year.

3.  The Reporting Ledger field displays the reporting ledger assigned to the
    General Ledger transaction in the General Ledger transaction entry window
    (Transactions \>\> Financial \>\> General). Refer to the General Ledger
    documentation for more information.

>   This field is available only if you have marked the Allow check box for the
>   Reporting Ledger option in the General Ledger Setup window (Administration
>   \>\> Setup \>\> Financial \>\> General Ledger).

1.  You can browse and sort by the following options:

>   **Journal Entry** You can browse analysis information entered for each
>   Journal Entry.

>   **Audit Trail Code** You can browse analysis information based on the Audit
>   Trail Code of a Journal Entry.

>   **Posting Date** You can browse analysis information by Posting Date.

1.  Choose OK to close the window.

### Analytical Accounting check links

>   Checking links examines tables, checking corresponding information in
>   related tables in Analytical Accounting and Microsoft Dynamics GP and, if
>   possible, changing the data to match the corresponding data in a table.

>   **To check links:**

1.  Ensure that all users are logged out of Microsoft Dynamics GP. To view which
    users are in the Microsoft Dynamics GP system and where, choose
    Administration \>\> Setup \>\> System \>\> User Activity.

2.  Take a backup of all your databases.

>   Always take a backup before checking links.

1.  Open the Analytical Accounting Check Links window  
    (Administration \>\> Maintenance \>\> Analytical Accounting Check Links).

2.  Select the table groups to check links for, whether AA Open and History
    Transactions, AA Work Transactions, or both.

3.  Choose Insert to insert the highlighted logical tables in the Selected
    Tables list.

4.  Choose All to Insert all files from the Logical Tables list into the
    Selected Tables list so you can check links for all files.

5.  Choose Remove to remove any table from the Selected Tables list, highlight
    the table name and choose Remove.

6.  Choose Preview to print the AA File Maintenance Error Log Report - Preview.

7.  Choose Cancel to Close the window. If you inserted table group names into
    the Selected Tables list.

>   Total Number of records field displays the total number of records within
>   the tables in the Selected Tables list.

1.  Choose Process to check links for the selected tables and print the Check
    Links Report.

    -   The Report Destination window will appear, and you can specify where the
        Check Links Report should be printed. If you mark File, select the
        appropriate table format and enter the report file name.

    -   The Check Links Report will display any information that was re-created.
        *We recommend that you send the Check Links Report to the screen, and
        then print it if necessary, because it may be very large. Each report
        can only be printed once each time you check links, so its a good idea
        to send the report to a file as well.*

2.  To determine what information to re-enter, use the Table Descriptions window
    (Administration \>\> Resource Descriptions \>\> Tables) to view information
    for the table you checked links for, then use a window that accesses the
    table to reenter information.

>   *You may want to create a report using Report Writer that lists all fields
>   included in the table that you checked links for. This report can serve as a
>   valuable reference tool. For more information, refer to the Report Writer
>   manual.*

### Copying Analytical Accounting Information for General Journal

>   Use the Copy Journal Entry window to copy analytical accounting information
>   for posted transaction.

>   **To copy analytical accounting information for general journal:**

1.  Open copy the Transaction Entry window.

>   (Transactions \>\>Financial \>\> General)

1.  Choose Copy. The Copy Journal Entry window will open.

2.  In the Copy Journal Entry window, select the year that the transaction
    you’re copying was posted.

3.  Select the journal entry number for the transaction that you’re copying.

4.  Mark the Copy Analytical Accounting information option.

5.  Choose OK. The Copy Journal Entry window will close. The new transaction
    will appear in the Transaction entry window along with the analytical
    accounting information. Modify the analytical accounting information as
    necessary.

Chapter 5: Payables Management Transactions
-------------------------------------------

>   You can enter and view analysis information for transactions in Payables
>   Management. You can create assignments, enter transaction dimension codes,
>   and also view analysis information created for a document. You also can save
>   transactions with analysis information to a single or recurring batch before
>   posting the batch. Analysis information created for transactions can be
>   validated at any time before they are posted.

>   You can open the Analytical Transaction Entry window only if Analytical

>   Accounting has been activated. Refer to *Activating Analytical Accounting*
>   for more information about activating Analytical Accounting.

>   This information is divided into the following sections:

-   *Entering analysis information for payables transactions*

-   *Entering analysis information for manual payments*

-   *Processing batches of computer checks with analysis information*

-   *Entering analysis information while applying documents*

-   *Unapplying a document*

-   *Applying unposted credit memos, returns and payments*

-   *Unapplying unposted credit memos, returns and payments*

-   *Voiding documents with analysis information*

-   *Viewing analysis information for payables transactions*

### Entering analysis information for payables transactions

>   You can create assignments and enter transaction dimension codes for
>   accounts that are linked to an account class from the Payables Transaction
>   Entry window. This information can be entered in the Analytical Payables
>   Transaction Entry window.

>   The Analytical Payables Transaction Entry window opens automatically from
>   the Payables Transaction Entry Distribution window in the following
>   instances:

-   If the account is linked to an account class and the Analytical Payables
    Transaction Entry window has not been opened even once for the account.

-   If changes are made to a distribution line that affects analysis information
    such as account or amount or type of amount created previously for such
    line.

>   If you delete a document from the Payables Transaction Entry window, the
>   analysis information that exists for the document will also be deleted.

>   In case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. Analysis
>   information entered previously is deleted when the distributions are
>   re-created.

>   If you select Default in the Payables Transaction Entry Distribution window,
>   all analysis information created for the document will be deleted.

>   **To enter analysis information for payables transactions:**

1.  Open the Analytical Payables Transaction Entry window.  
    (Transactions \>\> Purchasing \>\> Transaction Entry \>\> Choose the
    Analytical Accounting button)  
    (Transactions \>\> Purchasing \>\> Transaction Entry \>\> CTRL+T or
    Additional \>\>Analytical Transaction)  
    (Transactions \>\> Purchasing \>\> Transaction Entry \>\> Tax expansion
    button \>\>CTRL+T or Additional \>\> Analytical Transaction)  
    (Transactions \>\> Purchasing \>\> Transaction Entry \>\> Distributions
    button \>\> CTRL+T or Additional \>\> Analytical Transaction)

IMAGE – AAPT.jpg

![A screenshot of a computer Description automatically generated](media/b36decfcaa4e5996c8bbf5270c52a410.jpg)

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information about entering the analysis information.

### Entering analysis information for manual payments

>   You can also enter analysis information for manual payments using the
>   Analytical Payables Manual Payment Entry window.

>   If you delete a document from the Payables Manual Payment Entry window, the
>   analysis information that exists for the document also will be deleted.

>   In case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. Analysis
>   information entered earlier is deleted when the distributions are
>   re-created.

>   If you select Default on Payables Transaction Entry Distribution window, all
>   analysis information created for the document will be deleted.

>   The Analytical Payables Manual Payment Entry window will open automatically
>   from the Payables Transaction Entry Distribution window, when you press TAB
>   from a row in the following instances:

>   • If the account is linked to an account class and the Analytical Payables
>   Manual Payment Entry window has never been opened for the account.

>   • If changes are made to a distribution line that affects analysis
>   information entered previously for the line. These include changing the
>   account, amount or debit to credit or vice versa, as this will delete the
>   previously entered analysis information and create a single assignment of
>   100 percent.

>   **To enter analysis information for manual payments:**

1.  Open the Analytical Payables Manual Payment Entry window.  
    (Transactions \>\> Purchasing \>\> Manual Payments \>\> Choose the
    Analytical Accounting button)  
    (Transactions \>\> Purchasing \>\> Manual Payments \>\> CTRL+T or
    Additional\>\>Analytical Transaction)  
    (Transactions \>\> Purchasing \>\> Manual Payments \>\> Distributions \>\>
    CTRL+T or Additional \>\> Analytical Transaction)

IMAGE – AAPMT.jpg

![A screenshot of a computer Description automatically generated](media/d65c6f939de93ef703fa4f561765aa0b.jpg)

>   The Analytical Payables Transaction Entry window displays the distribution
>   account selected. To view other distributions, enter or select a
>   distribution number.

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information about the entering analysis information.

### Processing batches of computer checks with analysis information

>   You can enter analysis information for distributions that are created after
>   a computer check run only in the General Ledger. The Analytical Transaction
>   Entry window cannot be opened from any of the Microsoft Dynamics GP windows
>   where computer checks are posted.

>   For computer checks, the option Post Through General Ledger files under
>   Posting Setup will not be available. This is to ensure that analysis
>   information for distribution accounts linked to an account class is created
>   before updating General Ledger History.

>   A verification takes place to check if any of the distribution accounts are
>   linked to an account class in the following instances:

-   When you print checks from the Print Payables Checks window

>   (Transactions \>\> Purchasing \>\> Print Checks)

-   When you post a batch from the Post Payables Checks window

>   (Transactions \>\> Purchasing \>\> Post Checks)

-   When you post a batch from the Process Payables Checks window

>   (Transactions \>\> Purchasing \>\> Process Remittance)

>   If the distribution accounts are linked to an account class, then the
>   default codes that are set for the account class will be assigned to these
>   distribution accounts. A single assignment will be created for each
>   distribution account that is linked to an account class.

>   There will be no Analytical Accounting validation during a computer check
>   run or while printing a cheque.

>   If you void checks in the Post Payables Check window, all the distributions
>   for the payment will be deleted in Microsoft Dynamics GP and the payment
>   will move to history. Any analysis information that exists for the payment
>   will also be deleted.

### Entering analysis information while applying documents

>   You can enter analysis information for distributions, if any, created after
>   posted payments, credit memos and returns documents are applied in the Apply
>   Payables Documents window (Transactions \>\> Purchasing \>\> Apply To). You
>   can enter analysis information in the Analytical Apply Payables Documents
>   window.

>   Analysis information can be entered for distributions created for terms
>   taken, writeoffs, realized gain or realized loss when posted credit
>   documents, returns and payments are applied against invoices, if the
>   distribution accounts are linked to an account class in the Analytical Apply
>   Payables Documents window. The Analytical Apply Payables Documents window
>   will open when you choose OK in the Apply Payables Documents window. This
>   would be applicable even if distributions are created after transactions are
>   auto applied.

>   The Analytical Apply Payables Document window will also open if you change
>   the Customer ID or Document No. in the Apply Payables Documents window.

>   If the Analytical Apply Payables Documents window has been opened at least
>   once, you can open it any time thereafter by pressing CTRL+T or choosing
>   Additional \>\> Analytical Transaction before the distributions are posted.

>   The Analytical Apply Payables Documents window will open displaying the
>   first of the distribution accounts created during the process of apply that
>   have been linked to an account class.

>   If you’ve marked the Show valid code combinations in trns and budgets option
>   in the Analytical Accounting Options window, then the lookup window will
>   display only those codes that have a valid combination with the codes you
>   have already selected for the transaction.

>   Refer to *Entering analysis information for payables transactions* for more
>   information about entering analysis information.

### Unapplying a document

>   When you unapply posted credit memos, returns or payments, the entries
>   relating to terms taken, write offs, realized gain or loss are reversed.
>   Analysis information must be entered for these distribution accounts if they
>   are linked to an account class. You can enter analysis information in the
>   Analytical Apply Payables Documents window. The window opens when you choose
>   OK in the Apply Payables Documents window.

>   The analysis information entered for distribution accounts relating to terms
>   taken, write offs, realized gain or loss will be validated before these
>   entries are posted. Errors detected will be displayed in the Analytical
>   Accounting Validation Log.

>   You will not be able to close the Apply Payables Document window without
>   entering all required analysis information for the distribution accounts
>   linked to an account class.

#### Applying unposted credit memos, returns and payments

>   You can enter analysis information for credit memos, returns and payments
>   applied in the Payables Transaction Entry and Payables Manual Payment Entry
>   windows using the Analytical Payables Transaction Entry or Analytical
>   Payables Manual Payment Entry windows. The Analytical Payables Transaction
>   Entry or Analytical Payables Manual Payment Entry windows will open when you
>   select OK in the Apply Payables Documents window.

>   Analysis information entered for the Accounts Payable account in the
>   Payables Transaction Entry or Manual Payments Entry windows before the
>   credit memo, return or payment is applied, will be deleted if distributions
>   are created for terms taken, write offs, and realized gain or loss.

#### Unapplying unposted credit memos, returns and payments

>   If you unapply unposted credit memos, returns and payments that were
>   applied, prior to posting, analysis information entered for the distribution
>   accounts relating to terms taken, write offs and realized gain or loss
>   accounts will be deleted.

#### Voiding documents with analysis information

>   When you void documents in the Void Historical Payables Transaction window

>   (Transactions \>\> Purchasing \>\> Void Historical Transaction) or the Void
>   Open Payables Transaction window (Transactions \>\> Purchasing \>\> Void
>   Open Transaction), all analysis information entered for the document during
>   transaction entry will be copied with the exception of the balance type of
>   each distribution account linked to an account class. The balance type of
>   each distribution account will be reversed.

>   The Analytical Transaction Entry window cannot be opened prior to voiding a
>   document in the Void Historical Payables Transaction or Void Open Payables
>   Transaction windows.

>   The Analytical Accounting Posting Journal will print after the Microsoft
>   Dynamics GP reports, if you’ve selected the option under Posting Setup. This
>   report will display all analysis information for the voided transaction.

#### Viewing analysis information for payables transactions

>   You can view analysis information for payables transactions in the
>   Analytical Payables Transaction Entry zoom window. The Analytical inquiry
>   window will only display distribution accounts of a document that are linked
>   to an account class.

>   **To view analysis information for payables transactions:**

1.  Open the Analytical Payables Transaction Entry zoom window.  
    (Inquiry \>\> Purchasing \>\> Transaction by Vendor/Document \>\> Select a
    document and zoom on the Document Number \>\> Additional \>\> Analytical
    Transaction)  
    (Inquiry \>\> Purchasing \>\> Transaction by Vendor/Document \>\> Select
    document and zoom to Document Number \>\> Distributions button \>\>
    Additional \>\> Analytical Transaction)

2.  The Analytical Payables Transaction Entry zoom window displays all analysis
    information created for a distribution account.

3.  Refer to *Viewing analysis information for Purchase Order Processing
    documents* for more information about viewing analysis information for
    transactions.

**Chapter 6: Purchase Order Processing Transactions**

>   You can enter analysis information for transactions in Purchase Order
>   Processing and save analysis information for a batch.

>   This information is divided into the following sections:

-   *Entering analysis information for purchase orders and receipts*

-   *Entering analysis information for purchase orders*

-   *Analysis information for adjusting entries*

-   *Posting transactions with analysis information*

-   *Posting a batch with analysis information*

-   *Posting through to General Ledger for transaction posting*

-   *Viewing analysis information for Purchase Order Processing documents*

-   *Viewing analysis information for purchase orders*

-   *Copying Analytical Accounting Information for Purchase Order or Purchase
    Order Line Items*

#### Entering analysis information for purchase orders and receipts

>   The Analytical Receivings Transaction Entry and the Analytical Purchasing
>   Invoice Entry windows will open automatically when you press TAB from a row
>   in the Payables Transaction Distribution Entry window in the following
>   instances:

-   If the account is linked to an account class and the Analytical Transaction
    Entry window has not been opened even once for the account.

-   If changes are made to a distribution line that affects analysis information
    entered previously for such line. These include changing the account or
    amount or debit to credit or credit to debit, as this will delete the
    previously entered analysis information and create a single assignment of
    100 percent.

>   If you delete a document in the Receivings Transaction Entry window or the
>   Purchasing Invoice Entry window, the analysis information entered for the
>   document also will be deleted.

>   If you void an unposted document in the Receivings Transaction Entry or
>   Purchasing Invoice Entry windows, analysis information created for the
>   document will be deleted.

>   In case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. If the
>   transaction date is altered, analysis information created previously is
>   deleted when the distributions are recreated.

>   **To enter analysis information for purchase orders and receipts:**

1.  Open the Analytical Receivings Transaction Entry or Analytical Purchasing
    Invoice Entry windows.  
    (Transactions \>\> Purchasing \>\> Receivings Transaction Entry \>\> Choose
    the Analytical Accounting button)  
    (Transactions \>\> Purchasing \>\> Receivings Transaction Entry \>\> Enter
    vendor item \>\> CTRL+T or Additional \>\> Analytical Transaction)  
    (Transactions \>\> Purchasing \>\> Enter/Match Invoice \>\> Choose the
    Analytical Accounting button)  
    (Transactions \>\> Purchasing \>\> Enter/Match Invoice \>\> Enter quantity
    invoiced \>\> CTRL+T or Additional \>\> Analytical Transaction)

IMAGE – AART.jpg

![A screenshot of a computer Description automatically generated](media/2fa8ff57d57bb2bec022a56619308942.jpg)

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information on entering analysis information for transactions.

>   You can validate a transaction by pressing CTRL+T or by choosing Additional
>   \>\> Run Validation in the following windows:

-   Payables Transaction Entry

-   Payables Manual Payments Entry

-   Apply Payables Documents

-   Receivings Transaction Entry

-   Purchasing Invoice Entry

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

>   If errors are detected in the transaction, the Analytical Accounting
>   Validation Log window will open displaying all errors detected by the
>   validation routine.

>   *You can select View \>\> Incomplete or Erroneous Distributions, to browse
>   through the distribution accounts in the Analytical Transaction Entry window
>   which are incomplete or have erroneous information.*

#### Entering analysis information for purchase orders

>   You can enter analysis information for inventory, purchases or drop ship
>   accounts linked to a line item while entering a purchase order. The
>   information will default when you receive these line items in the Receivings
>   Transaction Entry window.

>   You can open the Analytical Purchase Order Entry window from the Purchasing
>   Item Detail Entry window in the following instance if the account is linked
>   to an account class:

>   • If changes are made to a distribution line that affects analysis
>   information such as account or amount entered previously for such line. This
>   will delete and refresh the previously entered analysis information and
>   create a single assignment of 100 percent.

>   If you delete a document or a distribution line in the Purchase Order Entry
>   or the Purchasing Item Detail Entry window, the analysis information entered
>   for the same will also be deleted.

>   You cannot edit the Purchase Order Entry or the Purchasing Item Detail Entry
>   window while the Analytical Purchase Order Entry window is open.

>   In the case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. If the
>   transaction date is altered, analysis information created previously is
>   deleted when the distributions are recreated.

>   *Analysis information is not copied when you choose to copy PO lines from
>   another PO to the current PO. You must enter fresh analytical information
>   for the new purchase order.*

>   **To enter analysis information for purchase orders:**

1.  Open the Analytical Purchase Order Entry window.  
    (Transactions \>\> Purchasing \>\> Purchase Order Entry \>\> Enter or select
    a purchase order \>\> Choose the Analytical Accounting button)  
    (Transactions \>\> Purchasing \>\> Purchase Order Entry \>\> Enter or select
    a purchase order \>\> CTRL+T or Additional \>\> Analytical Transaction)
    (Transactions \>\> Purchasing \>\> Purchase Order Entry \>\> Enter or select
    a purchase order \>\> Item or Vendor Item expansion button \>\> Choose the
    Analytical Accounting button)  
    (Transactions \>\> Purchasing \>\> Purchase Order Entry \>\> Enter or select
    a purchase order \>\> Item or Vendor Item expansion button \>\> CTRL+T or
    Additional \>\> Analytical Transaction)

IMAGE – AAPO.jpg  


![A screenshot of a computer Description automatically generated](media/aa259ae274731113d94ade624c55fac5.jpg)

>   When you open the Analytical Purchase Order Entry window from the Purchasing
>   Item Detail Entry window, it displays only the account for the selected
>   item.

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information on entering analysis information for transactions.

2.  You can validate the analysis information by pressing CTRL+R or by choosing
    Additional \>\> Run Validation in the Purchase Order Entry or the Purchasing
    Item Detail Entry windows. Refer to *Validating transactions and correcting
    errors* for more information about validation.

#### Analysis information for adjusting entries

>   Adjusting entries are posted to General Ledger for each item that has its
>   current cost changed and uses the Average Perpetual valuation method.
>   Adjusting entries are also posted for quantity sold transactions relating to
>   the purchase receipt of items that use the Average Perpetual, LIFO
>   Perpetual, or FIFO Perpetual valuation method. Such entries are created in
>   the following instances:

-   The user selects to revalue inventory when posting a purchasing invoice
    where the invoice cost differs from the shipment cost.

-   The Adjust Costs utility is used to edit a purchase receipt record’s cost.

-   A Purchase Order line item is changed to a status of Closed when its
    Quantity Shipped is greater than the Quantity Invoiced, when Quantity
    Invoiced is not zero.

-   A purchase receipt is inserted into an existing purchase receipt stack.

>   When such adjusting entries are generated in General Ledger, default
>   transaction dimension codes are loaded and a single assignment is created
>   for distribution accounts that are linked to an account class. You can
>   modify the default analysis information, before posting through General
>   Ledger. Refer to *Entering analysis information for General Ledger
>   transactions* for more information.

>   If you have marked the option Post Through General ledger Files in the
>   Posting Setup window (Administration \>\> Setup \>\> Posting \>\> Posting),
>   or you have marked the option Post through to General Ledger for Trx Posting
>   in the Analytical Accounting Options window (Administration \>\> Setup \>\>
>   Company \>\> Analytical

>   Accounting \>\> Options), the transaction or batch is posted directly
>   through General Ledger with default analysis information for the additional
>   distributions. You can modify this information in the Analytical Adjustment
>   Entry window if required. Refer to *Adjusting analysis information in posted
>   transactions* for more information.

#### Posting transactions with analysis information

>   When you post a transaction with analysis information from the following
>   windows, a validation will take place:

-   Payables Transaction Entry

-   Payables Manual Payments Entry

-   Receivings Transaction Entry

-   Purchasing Invoice Entry

>   When you close the Apply Payables Documents window, analysis information
>   created for the document in the window will be validated.

>   Refer to *Validating transactions and correcting errors* for more
>   information. In addition to Analytical Accounting information, Microsoft
>   Dynamics GP information will also be validated before the transaction is
>   posted.

>   The Analytical Posting Journal will be printed after a transaction is posted
>   or after closing the Apply Payables Documents window if specified under
>   Posting Setup.

#### Posting a batch with analysis information

>   You can enter analysis information for transactions within a Payables or
>   Purchasing Batch. Refer to *Entering analysis information for purchase
>   orders and receipts* for more information about entering analysis
>   information.

>   You can print the Analytical Accounting Edit List and Analytical Accounting

>   Validation Log to check if errors exist in the analysis information along
>   with the Microsoft Dynamics GP Edit List for a selected batch by choosing
>   the printer icon button.

-   When you post a batch from the Payables Management window or the Purchase
    Order Processing window, a validation takes place for all the transactions
    saved in the batch. Refer to *Validating transactions and correcting errors*
    for more information about the validation process. Microsoft Dynamics GP and
    Analytical Accounting transactions without errors are posted. The Analytical
    Posting Journal is printed, if specified under Posting Setup, along with the
    Microsoft Dynamics GP reports. If errors are found during the validation
    process, the Analytical Accounting Validation Log report is printed listing
    the analysis errors for the transactions in the batch being posted. You can
    correct the errors by editing the transactions in the window where the
    transaction originated from.

-   If you delete a single or recurring use batch or a transaction within such
    batches, the analysis information entered for the transactions in the batch
    or for the transaction will also be deleted.

-   You can save a transaction in a batch with Analytical Accounting errors but
    you cannot post the transaction.

-   For a recurring batch, the analysis information of the batch last posted
    will be retained and will update each subsequent batch that is posted,
    unless changes are made to the analysis information in the batch.

>   When you print the Analytical Posting Journal, detailed analysis information
>   of all accounts will be printed. This would also include accounts with
>   errors. The Analytical Validation Log report detailing all Analytical
>   Accounting errors will also be printed. You can correct Analytical
>   Accounting errors by opening the batch and then correcting the transactions
>   that have errors.

#### Posting through to General Ledger for transaction posting

>   Individual transactions and batches posted from Payables Management will
>   automatically update the appropriate posting accounts in General Ledger if
>   you have marked the following options, and if there are no Analytical
>   Accounting and Microsoft Dynamics GP errors:

-   Post through General Ledger files under Posting Setup (Administration \>\>
    Setup \>\> Posting \>\> Posting); and

-   Post through to General Ledger for Trx Posting (Administration \>\> Setup
    \>\> Company \>\> Analytical Accounting \>\> Setup)

>   Refer to *Setting up posting options for Analytical Accounting* for more
>   information about Analytical Accounting posting setup.

>   While posting individual and batch transactions, Analytical Accounting or
>   Microsoft Dynamics GP errors may exist which would prevent the transaction
>   or batch from updating the appropriate posting accounts in General Ledger.
>   For example, default codes may not be assigned for Required transaction
>   dimensions in the account class that the distribution accounts of Fixed or
>   Variable accounts are linked to. The transaction or batch will update the
>   General Ledger. You must correct the errors in the transaction or batch in
>   the General Ledger from the Transaction Entry window (Transactions \>\>
>   Financial \>\> General) before the posting accounts can be updated.

>   The Analytical Accounting and Microsoft Dynamics GP errors will be displayed
>   in the Analytical Accounting Validation Log Report which will print after
>   the transaction or batch updates Payables Management.

>   The transaction and batch will update the Payables Management. You will be
>   able to view analysis information that originated for the transaction or
>   batch in Payables Management from the relevant Inquiry windows.

#### Viewing analysis information for Purchase Order Processing documents

>   You can view analysis information created for transactions in Purchase Order
>   Processing in the Analytical Purchasing Invoice Inquiry Zoom window.

>   You can view the assignments, transaction dimension codes and reference
>   notes that have been created for individual transaction distributions in
>   this window.

>   **To view analysis information for Purchase Order Processing documents:**

1.  Open the Analytical Purchasing Invoice Inquiry Zoom window.  
    (Inquiry \>\> Purchasing \>\> Purchase Order Docs \>\> Purchasing Invoice
    Inquiry Zoom \>\> CTRL+ T or Additional \>\> Analytical Transaction)  
    (Inquiry \>\> Purchasing \>\> Purchase Order Docs \>\> Receivings
    Transaction Inquiry Zoom \>\> CTRL+T or Additional \>\> Analytical
    Transaction)

2.  The Analytical Posting Inquiry window displays all analysis information
    created for a distribution account. The first distribution account of the
    document linked to an account class is displayed. Enter or select a
    distribution number to view analysis information for other distribution
    accounts.

3.  If you select a specific account in the Purchasing Distribution Inquiry
    Zoom, the Analytical Posting Inquiry window will display analysis
    information relating to the selected account.

4.  The Document Type and Number fields display the values from the Receivings
    Transaction Inquiry window or the Purchasing Invoice Inquiry zoom.

5.  The Originating or Functional Amount field displays the distribution amount
    in the originating or functional currency based on the option you selected
    in the Currency View. Click the expansion button to view multicurrency
    information if the originating currency differs from the functional
    currency.

6.  The Document Date displays the date of the document and will default from
    the Receivings Transaction Inquiry or Purchasing Invoice Inquiry Zoom.

7.  The Company ID field displays the ID of the current company.

8.  Click Expand to display all analysis information entered for the
    distribution account in the assignment list window. This includes
    assignments, reference information entered per assignment, transaction
    dimensions and their codes.

9.  Click Collapse to display only assignments and reference information entered
    per assignment for the distribution account.

10. You also can view all information entered for each assignment or just
    reference information that may exist. Choose the plus button (+) available
    next to each assignment to view all analysis information entered for an
    assignment or choose the minus button (-) to view only reference information
    that may exist.

11. Choose OK to close the window.

#### Viewing analysis information for purchase orders

>   You can view the analysis information you’ve entered for a purchase order in
>   the Analytical Purchase Order Inquiry window.

>   **To view analysis information for purchase orders:**

1.  Open the Analytical Purchase Order Inquiry Zoom window.  
    (Inquiry \>\> Purchasing \>\> Purchase Order Documents/Purchase Order Items
    \>\> Choose the PO Number link \>\> CTRL+T or Additional \>\> Analytical
    Transaction)  
    Transactions \>\> Purchasing \>\> Receivings Transaction Entry \>\> Select a
    purchase order in the scrolling window \>\> Choose the PO Number link \>\>
    CTRL+T or Additional \>\> Analytical Transaction)  
    (Transactions \>\> Purchasing \>\> Receivings Transaction Entry \>\> Select
    a purchase order in the scrolling window \>\> Choose the PO Number link \>\>
    Vendor Item Expansion button \>\> CTRL+T or Additional \>\> Analytical
    Transaction)

2.  Refer to *Viewing analysis information for payables transactions* for more
    information on viewing analysis information for transactions.

#### Copying Analytical Accounting Information for Purchase Order or Purchase Order Line Items

>   Use the Copy a Purchase Order window to copy analytical accounting
>   information from an existing purchase order.

>   **To copy analytical accounting information for purchase order or Purchase
>   Order Line Items:**

1.  Open Purchase Order Entry window.  
    (Transactions \>\> Purchasing \>\> Purchase Order Entry \>\> Actions \>\>
    Create and Copy New PO)  
    (Transactions \>\> Purchasing \>\> Purchase Order Entry \>\> enter a
    purchase order \>\> Actions \>\> Copy PO Lines to Current PO)  
      
    IMAGE – AACP.jpg

![](media/6593ad6049c79a4053c364b47d7fe479.jpg)

>   A screenshot of a computer Description automatically generated

1.  Choose Actions and select Create and Copy New PO or Copy PO lines to Current
    PO to open the Copy Purchase Order window.

2.  Enter or select a purchase order with a status of New, Released, or Change
    Order to copy.

3.  Mark the Copy Analytical Accounting information option.

4.  Choose copy.The analytical accounting information is copied from the
    originating document to new document.

**Chapter 7: Receivables Management Transactions**

>   For transactions in Receivables Management, you can create assignments and
>   enter transaction dimension codes for the distribution accounts that are
>   linked to an account class. You can save transactions with analysis
>   information to a single or recurring batch prior to posting the batch. Also,
>   you can view analysis information created for transactions in the Analytical
>   Inquiry windows. The process of validating transactions with analysis
>   information is also explained.

>   You can open the Analytical Transaction Entry window only if Analytical

>   Accounting has been activated. Refer to *Activating Analytical Accounting*
>   for more information about activating Analytical Accounting.

>   This information is divided into the following sections:

-   *Entering analysis information for receivables documents*

-   *Entering analysis information for cash receipts*

-   *Entering analysis information for applied documents*

-   *Unapplying a document*

-   *Applying unposted credit memos, returns and payments*

-   *Unapplying unposted credit memos, returns and payments*

-   *Voiding or waiving documents with analysis information*

-   *Entering analysis information for NSF charges*

-   *Validating transactions and correcting errors*

-   *Posting transactions with analysis information*

-   *Posting a batch with analysis information*

-   *Posting through or to General Ledger*

-   *Viewing analysis information in Receivables Management*

#### Entering analysis information for receivables documents

>   You can enter assignments and transaction dimension codes for receivables
>   documents using the Analytical Receivables Transaction Entry window.

>   When you press TAB from a field in the Sales Transaction Distribution Entry
>   window (Transaction \>\> Sales \>\> Transaction Entry), under the following
>   instances, the Analytical Receivables Transaction Entry window will open:

-   If an account is linked to an account class and no analysis information has
    been entered for the account earlier.

-   If changes are made to a distribution line that affects analysis information
    entered previously for the line. These include changing the account, amount
    or debit to credit or vice versa, as this will delete the previously entered
    analysis information and create a single assignment of 100 percent.

>   If you delete a document from the Receivables Transaction Entry window, the
>   analysis information that exists for the document will also be removed.

>   In case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. If the
>   transaction date is modified, analysis information created previously is
>   deleted when the distributions are re-created.

>   If you select Default in the Sales Transaction Entry Distribution, all
>   analysis information created for the document will be deleted.

>   **To enter analysis information for receivables documents:**

1.  Open the Analytical Receivables Transaction Entry window.  
    (Transaction \>\> Sales \>\> Transaction Entry \>\> Analytical Accounting
    button)  
    (Transaction \>\> Sales \>\> Transaction Entry \>\> Additional \>\>
    Analytical Transaction)  
    (Transaction \>\> Sales \>\> Transaction Entry \>\> Distributions \>\>
    Analytical Accounting button)  
    (Transactions \>\> Sales \>\> Transaction Entry \>\> Distributions \>\>
    Additional \>\>Analytical Transaction)  
    (Transactions \>\> Sales \>\> Transaction Entry \>\> Tax expansion button
    \>\> Additional \>\> Analytical Transaction)  
      
    IMAGE – AARTE.jpg

![](media/e7030d940008b7c4f45bf9d701a13a9c.jpg)

>   A screenshot of a computer Description automatically generated

1.  To enter analysis information for receivables transactions, refer to
    *Entering analysis information for General Ledger transactions* .

#### Entering analysis information for cash receipts

>   You can enter analysis information for cash receipts using the Analytical
>   Cash Receipts Entry window.

>   If you delete a document from the Cash Receipts Entry window, the analysis
>   information that exists for the document also will be removed.

>   For multicurrency transactions, a change in the transaction date re-creates
>   distributions due to a change in the exchange rate. If the transaction date
>   is modified, analysis information created previously is deleted when the
>   distributions are re-created.

>   If you choose Default in the Cash Receipts Distribution Entry window, all
>   analysis information created for the document will be deleted.

>   In the Cash Receipts Distribution Entry window, the Analytical Cash Receipts
>   Entry window will open automatically when you press TAB from a row in the
>   following instances:

-   If an account is linked to an account class and no analysis information has
    been entered for the account earlier.

-   If changes are made to a distribution line that affects analysis information
    entered previously for the line. These include changing the account, amount
    or debit to credit or vice versa, as this will delete the previously entered
    analysis information and create a single assignment of 100 percent.

>   Refer to *Entering analysis information for receivables documents* for more
>   information about creating analysis information.

#### Entering analysis information for applied documents

>   You can enter analysis information for distributions created, if any, after
>   a posted credit memo, return or payment is applied in the Apply Sales
>   Documents window (Transactions \>\> Sales \>\> Apply) using the Analytical
>   Apply Sales Documents window.

>   When posted credit memos, returns or payments are applied to sales documents
>   or other debit documents, distributions will be created for terms taken,
>   writeoffs, tax rebate, and realized gain or realized loss. If these
>   distribution accounts are linked to an account class, you must enter
>   analysis information for the accounts.

>   The Analytical Apply Sales Documents window will open when you select OK in
>   the Apply Sales Documents window, or if distributions are created when you
>   automatically apply sales documents.

>   The Analytical Apply Sales Document window also will open if you change the
>   customer ID or document no. in the Apply Sales Documents window.

>   In Analytical Accounting, voided and applied documents will update General
>   Ledger, if you marked the Post Through General Ledger option in the Posting
>   Setup window (Administration \>\> Setup \>\> Posting \>\> Posting).

>   If the Analytical Apply Sales Documents window has been opened at least
>   once, you can open it later from the Additional menu. Choose Additional \>\>
>   Analytical Transaction or CTRL+T before the distributions are posted.

>   The Analytical Apply Sales Documents window will display the first of the
>   distribution accounts created during the apply process that have been linked
>   to an account class.

>   If you’ve marked the Show valid code combinations in trns and budgets option
>   in the Analytical Accounting Options window, then the lookup window will
>   display only those codes that have a valid combination with the codes you
>   have already selected for the transaction.

>   Refer to *Entering analysis information for receivables documents* for more
>   information about entering analysis information.

#### Unapplying a document

>   When you unapply posted credit documents, returns and payments, entries
>   relating to terms taken, write offs, realized gain or loss are reversed. You
>   must enter analysis information for these distribution accounts if such
>   accounts are linked to an account class. You can enter analysis information
>   in the Analytical Apply Sales Documents window which will open when you
>   choose OK in the Apply Sales Documents window.

>   The analysis information entered for distribution accounts relating to terms
>   taken, write offs, realized gain or loss will be validated before these
>   entries are posted. Errors detected will be displayed in the Analytical
>   Accounting Validation Log.

>   Refer to *Posting transactions with analysis information* for more
>   information.

>   You can close the Apply Sales Document window only after entering all
>   required analysis information for the distribution accounts linked to an
>   account class.

#### Applying unposted credit memos, returns and payments

>   You can enter analysis information for credit memos, returns, and payments
>   applied in the Receivables Transaction Entry and Cash Receipts Entry windows
>   in the Analytical Receivables Transaction Entry or Analytical Cash Receipts
>   Entry windows respectively. The Analytical Receivables Transaction Entry or
>   Analytical Cash Receipts Entry windows will open when you select OK in the
>   Apply Sales Documents window.

>   If you have created analysis information for the Accounts Receivable account
>   in the Receivables Transaction Entry or Cash Receipts Entry windows prior to
>   applying the credit memo, return or payment, such information will be
>   deleted if distributions are created for terms taken, write offs, realized
>   gain or loss. You will have to re-enter analysis information for the
>   Accounts Receivable account.

#### Unapplying unposted credit memos, returns and payments

>   Before posting, if you unapply unposted credit memos, returns and payments,
>   in the Apply Sales Documents window (Transaction \>\> Sales \>\> Transaction
>   Entry \>\> Apply or Transactions \>\> Sales \>\> Cash Receipts \>\> Apply),
>   the analysis information entered for the distribution accounts relating to
>   terms taken, write offs and realized gain or loss accounts will be deleted.

#### Voiding or waiving documents with analysis information

>   If you make changes to the terms taken or writeoff amount before voiding a
>   credit document in the Apply Sales Documents window (Transactions \>\> Sales
>   \>\> Apply), extra distributions may be created. After voiding, default
>   codes will be loaded for the distributions that have been created.

>   The Analytical Transaction Entry window cannot be opened prior to voiding a
>   document in the Receivables Posted Transaction Maintenance window.

>   The Analytical Accounting Posting Journals will be printed along with the
>   Microsoft Dynamics GP reports, if you’ve selected the option under Posting
>   Setup.

>   This report will display all analysis information relating to the voided
>   transaction.

#### Entering analysis information for NSF charges

>   When you mark a check as Non Sufficient Funds (NSF) in the Receivables
>   Posted Transaction Maintenance window (Transactions \>\> Sales \>\> Posted
>   Transactions), analysis information may have to be entered for distribution
>   accounts relating to the NSF Charge, if such accounts are linked to an
>   account class.

>   When you choose OK in the Auto Post NSF Debit Charge window, the Analytical
>   Auto Post NSF Debit Charge window will open displaying the first of the
>   distribution accounts relating to the NSF Charge that is linked to an
>   account class (as per the distribution sequence).

>   Refer to *Entering analysis information for receivables documents* for more
>   information about entering analysis information.

>   If the Analytical Auto Post NSF Debit Charge window has been opened at least
>   once, you can open it any time thereafter from the Additional menu. Choose
>   Additional \>\> Analytical Transaction or CTRL+T before the distributions
>   are posted.

>   The analysis information entered for distribution accounts relating to NSF
>   charges will be validated before these entries are posted. Errors detected
>   will be displayed in the Analytical Accounting Validation Log.

>   Refer to *Posting transactions with analysis information* for more
>   information.

>   You can close the Auto Post NSF Debit Charges window only after entering all
>   required analysis information for the distribution accounts linked to an
>   account class.

>   Analysis information that exists for the cash receipt will be copied, except
>   for the balance type which will be reversed.

>   Refer to *Voiding or waiving documents with analysis information* for more
>   information about voiding documents.

#### Validating transactions and correcting errors

>   You can use the following windows to validate a transaction. From the
>   Additional menu, choose Additional \>\> Run Validation or CTRL+T:

-   Receivables Transaction Entry

-   Cash Receipts Entry

-   Apply Sales Documents

-   Auto Post NSF Debit Charge

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

>   If errors are detected in the transaction, the Analytical Accounting
>   Validation Log window will open, displaying all errors detected by the
>   validation routine.

>   You can select View \>\> Incomplete or Erroneous Distributions, to browse
>   the distribution accounts in the Analytical Transaction Entry window that
>   are incomplete or have errors.

>   To correct an Analytical Accounting error, double-click on the error to open
>   the relevant Analytical Transaction Entry window. The specific distribution
>   in which the error exists is displayed.

#### Posting transactions with analysis information

>   When you post a transaction from the Receivables Transaction Entry or the
>   Cash Receipts Entry window, a validation will take place.

>   Also, when you close the Apply Sales Documents or Auto Post NSF Debit Charge
>   window, analysis information created for the transaction/document will be
>   validated.

>   In addition to analysis information, Microsoft Dynamics GP data also will be
>   validated before the transaction is posted.

>   If errors are found while posting a transaction, the transaction will not be
>   posted. The Analytical Accounting Validation Log window will open, listing
>   the Microsoft Dynamics GP errors first and then the Analytical Accounting
>   errors.

>   We recommend that you resolve the Microsoft Dynamics GP errors first, and
>   then the Analytical Accounting errors.

>   To correct an Analytical Accounting error, double-click on the error to open
>   the relevant Analytical Transaction Entry window. The specific distribution
>   in which the error exists is displayed which you can then correct.

>   The Analytical Posting Journal will be printed, along with the Microsoft
>   Dynamics GP Posting reports if specified under Posting Setup.

#### Posting a batch with analysis information

>   When you post a batch from Receivables Management, a validation will take
>   place for all the transactions saved in the batch. Microsoft Dynamics GP and
>   Analytical Accounting transactions without errors will be posted and the
>   Analytical Posting Journal will be printed, along with the Microsoft
>   Dynamics GP reports if specified in the Posting Setup window. If errors are
>   found during the validation process, the Analytical Accounting Validation
>   Log report will be printed listing analysis errors for the transactions in
>   the batch being posted. You can correct the errors by modifying the
>   transactions in the window where the transaction originated from.

>   If you delete a single or recurring use batch or a transaction within such
>   batches, the analysis information entered for the transactions in the batch
>   or for the transaction also will be deleted.

>   You can save a transaction in a batch with Analytical Accounting errors but
>   cannot post the transaction.

>   For a recurring batch, the analysis information of the batch last posted
>   will be retained and will update each subsequent batch that is posted,
>   unless changes are made to the analysis information in the batch.

>   You can print the Analytical Accounting Edit List and Analytical Accounting
>   Validation Log Report along with the Microsoft Dynamics GP Edit List for a
>   selected batch by choosing the printer icon button.

>   When you print the Analytical Posting Journal, detailed analysis information
>   of all accounts will be printed including accounts with errors. The
>   Analytical Validation Log report detailing all Analytical Accounting errors
>   also will be printed. You can correct Analytical Accounting errors by
>   opening the batch and then correcting each of the transactions that have
>   errors.

#### Posting through or to General Ledger

>   If you’ve marked the following options, individual transactions and batches
>   posted from Receivables Management will automatically update the appropriate
>   posting accounts in General Ledger, if there are no Analytical Accounting
>   and Microsoft Dynamics GP errors.

-   Post through General Ledger files under Posting Setup (Administration \>\>
    Setup \>\> Posting \>\> Posting)

-   Post through to General Ledger for Trx Posting (Administration \>\> Setup
    \>\> Company \>\> Analytical Accounting \>\> Setup)

>   While posting individual and batch transactions, errors might exist in
>   Analytical Accounting or Microsoft Dynamics GP information that prevent the
>   transaction or batch from updating the appropriate posting accounts in
>   General Ledger. For example, default codes may not have been assigned for
>   required transaction dimensions in the account class to which the
>   distribution accounts of Fixed or Variable accounts are linked. The
>   transaction or batch will update General Ledger.

>   You must correct the errors in the transaction or batch in General Ledger
>   from the Transaction Entry window (Transactions \>\> Financial \>\> General)
>   before the posting accounts can be updated.

>   The transaction and batch will update Receivables Management. You can view
>   analysis information that originated for the transaction or batch in
>   Receivables Management from the relevant Inquiry windows.

>   The Analytical Accounting and Microsoft Dynamics GP errors will be displayed
>   in the Analytical Accounting Validation Log Report which will print after
>   the transaction or batch updates Receivables Management.

#### Viewing analysis information in Receivables Management

>   You can view analysis information entered for transactions in Receivables

>   Management in the Analytical Receivables Transaction Inquiry Zoom window.
>   The Analytical Inquiry window will display only distribution accounts of a
>   document that are linked to an account class.

>   **To view analysis information in Receivables Management:**

1.  Open the Analytical Receivables Transaction Inquiry Zoom window.  
    (Inquiry \>\> Sales \>\> Transaction by Customer/Transaction by Document
    \>\>Additional \>\> Analytical Transaction)

>   When the Analytical Transaction Inquiry window opens, all analysis
>   information created for a distribution account will be displayed.

1.  The first distribution account of the document linked to an account class is
    displayed. Enter or select a distribution number to view analysis
    information of other distribution accounts.

>   *If you select a specific account in the Receivables Distribution Inquiry
>   Zoom, the Analytical Posting Inquiry window will display analysis
>   information relating to such account.*

>   The Document Type and Number fields display values from the Receivables
>   Transaction Inquiry zoom or Cash Receipts Inquiry zoom.

1.  The Originating or Functional Amount field displays the distribution amount
    in the originating or functional currency based on the option you have
    chosen in the Currency View. Click the expansion button to view
    multicurrency information if the originating currency differs from the
    functional currency.

2.  The Document Date field displays the date of the document from the
    Receivables Transaction Inquiry zoom or Cash Receipts Inquiry Zoom.

3.  The Company ID field displays the ID of the current company.

4.  Choose Expand to display all analysis information entered for the
    distribution account in the list window. This includes assignments,
    reference information entered per assignment, transaction dimensions and
    their codes.

5.  Click Collapse to display only assignments and reference information entered
    per assignment for the distribution account.

6.  You also can view all information entered for each assignment or just
    reference information that may exist. Choose the plus button (+) available
    next to each assignment to view all analysis information entered for an
    assignment or choose the minus button (-) to view only reference information
    that may exist.

**Chapter 8: Sales Order Processing Transactions**

>   You can enter and view analysis information such as assignments, transaction
>   dimension codes and reference information for transactions entered in Sales
>   Order Processing. You can save transactions with analysis information in a
>   Sales Batch before posting. The analysis information you have entered will
>   be validated before posting.

>   You can enter analysis information in Sales Order Processing only from the
>   Sales Transaction Entry window (Transactions \>\> Sales \>\> Sales
>   Transaction Entry) and for Sales Invoices and Sales Returns.

>   You can open the Analytical Transaction Entry window only if Analytical

>   Accounting has been activated. Refer to *Activating Analytical Accounting*
>   for more information.

>   This information is divided into the following sections:

-   *Entering analysis information for an invoice or return*

-   *Analysis information in re-created distributions*

-   *Analysis information for deposits received against an order*

-   *Deletion of analysis information on invoice transfer to back order*

-   *Validating transactions and correcting errors*

-   *Posting an invoice or return with analysis information*

-   *Posting a batch with analysis information*

-   *Posting through to General Ledger for transaction posting*

-   *Voiding transactions with analysis information*

-   *Viewing analysis information for sales documents*

-   *Copying Analytical Accounting Information for Sales Order*

#### Entering analysis information for an invoice or return

>   You can enter analysis information for an invoice or return in the Sales
>   Transaction Entry window (Transactions \>\> Sales \>\> Sales Transaction
>   Entry) using the Analytical Sales Transaction Entry window.

>   If you delete an invoice or return from the Sales Transaction Entry window,
>   the analysis information that exists for the document will also be removed.

>   If you delete an item number from an invoice or return, analysis information
>   that exists for distribution accounts relating to the item number deleted
>   will also be removed.

>   In case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. If the
>   transaction date is altered, analysis information created previously is
>   deleted when the distributions are recreated.

>   If you select Default in the Sales Distribution Entry window, all analysis
>   information created for the invoice or return will be deleted.

>   The Analytical Sales Transaction Entry window will open automatically when
>   you press TAB from a field in the Sales Distribution Entry window, in the
>   following instances:

-   If the account is linked to an account class and the Analytical Sales
    Transaction Entry window has not been opened even once for the account.

-   If changes are made to a distribution line that affects analysis information
    entered previously for such line. These include changing the account or
    amount or debit to credit or vice versa, as this will delete the previously
    entered analysis information and create a single assignment of 100 percent.

>   In an invoice, you can enter analysis information for the Cost of Goods Sold
>   (COGS) and Inventory accounts of the relevant item numbers entered in the
>   invoice, if such accounts are linked to an account class even though these
>   accounts are not displayed in the Sales Distribution Entry window. However,
>   you cannot create assignments for such accounts as the amount that updates
>   these accounts can be determined only after the invoice is posted.

>   **To enter analysis information for an invoice or return:**

1.  Open the Analytical Sales Transaction Entry window.  
    (Transactions \>\> Sales \>\> Sales Transaction Entry \>\> Analytical
    Accounting button)  
    (Transactions \>\> Sales \>\> Sales Transaction Entry \>\> Additional \>\>
    Analytical Transaction or CTRL+T)  
    (Transactions \>\> Sales \>\> Sales Transaction Entry \>\> Distributions
    \>\>Analytical Accounting button)  
    (Transactions \>\> Sales \>\> Sales Transaction Entry \>\> Distributions
    \>\>Additional \>\> Analytical Transaction or CTRL+T)

IMAGE – AAST.jpg

![A screenshot of a computer Description automatically generated](media/be24d97b079718b840e31a6b32831e2c.jpg)

>   The distribution accounts of each item number linked to an account class
>   that you enter on an invoice or return, will be added to the total
>   distributions in the Analytical Sales Transaction Entry window only after
>   you tab off the Line Item in the Sales Transaction Entry window.

>   The Analytical Sales Transaction Entry window will open only if you have
>   specified at least one item number with a unit cost more than zero for the
>   invoice or return.

1.  The first of the distribution accounts in the Sales Distribution Entry
    window that is linked to an account class is displayed in the Analytical
    Sales Transaction Entry window. To view other distributions (other than the
    COGS and Inventory Accounts in case of an invoice) enter or select a
    distribution number or use the browse buttons.

>   You view a specific distribution account linked to an account class by
>   selecting that account prior to opening the Analytical Sales Transaction
>   Entry window.

>   The sequence of distributions in the Analytical Sales Transaction Entry
>   window may not correspond to the sequence in the Sales Distribution Entry
>   window as only accounts linked to an account class are displayed here.

>   If only the COGS and Inventory Accounts of an Invoice are linked to an
>   account class, the Analytical Sales Transaction Entry window will open
>   displaying the first of such accounts linked to an account class.

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information about entering analysis information for transactions.

2.  Choose Cogs/Inv to view the Cost of Goods Sold and Inventory accounts of an
    Invoice, linked to an account class. The first of these accounts linked to
    an account class will be displayed when you select this button. The sequence
    in which the Cost of Goods Sold and Inventory Accounts will be displayed
    will be based on the order in which item numbers are displayed on the
    invoice. To view the other COGS and Inventory Accounts linked to an account
    class, you can use the browse button or enter or select the distribution
    number in the Distribution field. Choose MAIN to view the distribution
    accounts displayed in the Sales Distribution Entry window that are linked to
    an account class.

>   For an invoice, since the amount that updates the COGS and Inventory
>   accounts can be determined only after the invoice is posted, the fields and
>   scrolling windows relating to amount and assignment will not be available in
>   relation to these accounts.

>   The Cogs/Inv button will not be available in the following instances:

-   If the COGS and Inventory accounts are not available under the relevant
    setup, such as Item or Customer or Posting or if these accounts are not
    linked to an account class.

-   If non-inventory items are entered on an invoice.

-   If the unit cost for drop-ship items in the Sales Transaction Entry window
    is zero.

-   If the item number selected in the Sales Transaction Entry window is marked
    as is marked as Misc Charges/Services/Flat Fee on Item Maintenance window

-   If the Document Type of the transaction is Return. In the case of Sales
    Returns, the COGS and Inventory accounts will form part of the distribution
    accounts displayed in the Sales Distribution Entry window. You can enter
    analysis information including assignments for these accounts if required,
    in the same manner as the other distribution accounts displayed in the Sales
    Distribution Entry window that are linked to an account class.

>   If you have entered Kit Items on an invoice, addition or deletion of a
>   component item from the Sales Kit Options window (Transactions \>\> Sales
>   \>\> Sales Transaction Entry \>\> Item Number expansion button \>\> Kits)
>   may increase or decrease the COGS and Inventory Accounts displayed in the
>   Analytical Sales Transaction Entry window, if the accounts concerned are
>   linked to an account class.

>   If you have entered Kit Items on a return, addition of a component item in
>   the Sales Kit Options window may increase the COGS and Inventory Accounts
>   displayed in the Analytical Sales Transaction Entry window, if the relevant
>   accounts are not already displayed and are linked to an account class.

1.  Choose OK to close the window. A validation will take place when you choose
    OK. Refer to *Validating transactions and correcting errors* for more
    information about validation.

2.  Choose Save to save the analysis information you’ve entered and clear the
    window. A validation takes place when you choose Save in the Analytical
    Sales Transaction Entry window. Refer to *Validating transactions and
    correcting errors* for more information about validation.

>   You can save the analysis information with errors or without updating
>   changes made to the account class.

1.  Choose Clear to clear the information you have entered but not saved.

2.  Choose Validate to validate the analysis information of the distribution
    account displayed in the window. If changes are made to the account class or
    errors are found during the validation process, the Analytical Accounting
    Validation Log window will open displaying the changes and errors. Double
    click an Analytical Accounting error to open the Analytical Sales
    Transaction Entry window where the distribution account comprising the error
    is displayed.

>   You can select View \>\> Incomplete or Erroneous Distributions, to browse
>   through the distribution accounts which are incomplete or have erroneous
>   information.

1.  Click the printer icon button to print the Analytical Accounting Edit List
    which will display analysis information of the distribution account
    currently displayed or for all distribution accounts of the Invoice or
    Return that are linked to an account class. The Analytical Accounting
    Validation Log report describing the Analytical Accounting errors, if any,
    in brief is also printed.

#### Analysis information in re-created distributions

>   Before posting a sales invoice/return, if changes listed below are made to
>   the existing information for these documents, distributions will be
>   re-created. This will automatically delete the existing analysis information
>   for distribution accounts linked to an account class. Analysis information
>   entered for COGS and Inventory accounts of an invoice is not affected by
>   these changes.

| **Window name**                                                    | **Changes made**                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sales Tax Summary Entry or Sales Line Item Tax Detail Entry window | Change in or deletion of a Tax Detail ID, Total Sales and Tax Amount; Selecting Default or Delete in the Sales Tax Summary Entry window.                                                                                                                                                                                                                                           |
| Sales Item Detail Entry window                                     | Changes to the Shipping address or the tax schedule assigned to this address; Change to the Item Tax Schedule ID; Change in Salesperson ID; Distributions will also be re-created if the Total Invoice or Sales Amount is altered.                                                                                                                                                 |
| Sales Payment Terms Entry window                                   | Change in Discount Percent; Change in Terms Discount Available or Payment Terms Amount (this will re-create distributions if Default is selected in the Sales Distribution Entry window after changes); Deletion of Terms Discount or Payment Terms Percent or Amount; (would re-create distributions if Default is selected in the Sales Distribution Entry window after changes) |
| Sales Customer Detail Entry window                                 | Changes to the payment terms.                                                                                                                                                                                                                                                                                                                                                      |
| Sales Tax Schedule Entry window                                    | Change in tax schedules; Change in tax status. For example, from taxable to non taxable; Price level in the Sales Item Detail Entry window; Change in Unit Price, Extended Price, and Invoice Quantity in the Sales Item Detail Entry window or Sales Transaction Entry window.                                                                                                    |
| Sales Commission Entry window                                      | Change in Salesperson ID, Percent of Sale (provided the Territory ID remains unchanged), Commission Percent and Commission Amount; Addition or deletion of a Salesperson ID; Deletion of commission distributions; Amending or deleting Commission Sale Amount.                                                                                                                    |
| Sales Payment Entry window                                         | Change in Cash Account in the Checkbook Setup window. The distributions will be re-created only if you select Default in the Sales Distribution Entry window; Deletion of line item in the Sales Transaction Entry window.                                                                                                                                                         |
| Sales Trade Discount Entry window                                  | Change in Trade Discount.                                                                                                                                                                                                                                                                                                                                                          |
| Sales Transaction Entry window                                     | Amending the Trade Discount percent or amount; Inclusion or deletion of freight and miscellaneous charges; Change or deletion of Amount Received; Entering or deleting an amount on the Terms Discount Taken field.                                                                                                                                                                |
| Sales Transaction Entry window (Selecting the Show Detail option)  | Changes to the following could re-create distributions: Invoice Quantity, Unit Price, Extended Price, Entering a Mark Down in the Sales Markdown Entry window, Price Level, Ship To Address ID (affects tax calculations), Site ID (affects tax calculations if method of shipping is Pickup).                                                                                     |

>   In the case of analysis information entered for the COGS and Inventory
>   Accounts of a Return, the following changes prior to posting would result in
>   a re-creation of such information:

| **Window name**                                                 | **Changes made**                                                                                                                                                  |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sales Item Detail Entry or Line Item Detail Entry windows       | Change in Unit Cost                                                                                                                                               |
| Sales Returned Quantities Entry window                          | Changes to Return Quantity Type. For example, splitting the quantity returned between Returned and Damaged, after the entire quantity was assigned to Returned.   |
| Sales Kit Options window If Kit Items are entered on the Return | Deletion of a component item from the Sales Kit Options window. This could result either in a change in distribution amount or removal of a distribution account. |

#### Analysis information for deposits received against an order

>   For a deposit received against an order in the Sales Transaction Entry
>   window, distributions relating to the deposit will be created in General
>   Ledger after the order is saved.

>   If the distribution accounts relating to the deposit are linked to an
>   account class, you can enter analysis information for such accounts only in
>   the General Ledger. Refer to *Entering analysis information for General
>   Ledger transactions* for more information.

>   You cannot open the Analytical Sales Transaction Entry window from the Sales
>   Transaction Entry or Sales Payment Entry windows. Also, no validation will
>   take place when you save the order.

#### Deletion of analysis information on invoice transfer to back order

>   If you transfer an invoice quantity fully or partly to a back order, the
>   analysis information entered for the document, including the COGS and
>   Inventory accounts, will be deleted.

>   You will have to re-create analysis information when the back order is
>   subsequently converted to an invoice.

>   Refer to *Entering analysis information for an invoice or return* for more
>   information about entering analysis information.

#### Validating transactions and correcting errors

>   You can validate analysis information entered for an invoice or return in
>   the Sales Transaction Entry window, before posting by choosing CTRL+T or
>   Additional \>\> Run Validation.

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

>   If errors are detected in the document, the Analytical Accounting Validation
>   Log window will open displaying all errors detected by the validation
>   routine.

>   You can select View \>\> Incomplete or Erroneous Distributions, to browse
>   through the distribution accounts in the Analytical Sales Transaction Entry
>   window which are incomplete or have erroneous information.

>   To correct an Analytical Accounting error, double-click in the relevant
>   error to open the Analytical Sales Transaction Entry window. The specific
>   distribution in which the error exists is displayed which you can then
>   correct.

#### Posting an invoice or return with analysis information

>   When you post an invoice or return from the Sales Transaction Entry window,
>   analysis information created for the document will be validated.

>   In addition to Analytical Accounting information, Microsoft Dynamics GP data
>   will also be validated before the transaction is posted.

>   If errors are found while posting the invoice or return, the transaction
>   will not be posted. The Analytical Accounting Validation Log window will
>   open listing the Microsoft Dynamics GP errors first and then the Analytical
>   Accounting errors.

>   We recommend that you resolve the Microsoft Dynamics GP errors first and
>   then the Analytical Accounting errors.

>   To correct an Analytical Accounting error, double-click on the relevant
>   error to open the Analytical Sales Transaction Entry window. The specific
>   distribution in which the error exists is displayed which you can then
>   correct.

>   The Analytical Posting Journal will be printed along with the Microsoft
>   Dynamics GP Posting reports if specified under Posting Setup.

#### Posting a batch with analysis information

>   You can enter analysis information for transactions within a Sales Batch

>   (Transactions \>\> Sales \>\> Sales Batches). Refer to *Entering analysis
>   information for an invoice or return* for more information.

>   You can print the Analytical Accounting Edit List and Analytical Accounting

>   Validation Log Report (if errors exist in analysis information) along with
>   the Microsoft Dynamics GP Edit List for a selected batch by choosing the
>   printer icon button.

>   When you post a batch from Sales Order Processing, a validation will take
>   place for all the transactions saved in the batch. Refer to *Validating
>   transactions and correcting errors* for more information about the
>   validation process. Microsoft Dynamics GP and Analytical Accounting
>   transactions without errors will be posted and the Analytical Posting
>   Journal will be printed, if specified under Posting Setup along with the
>   Microsoft Dynamics GP reports. If errors are found during the validation
>   process, the Analytical Accounting Validation Log report will be printed
>   listing analysis errors for the transactions in the batch being posted. You
>   can correct the errors by correcting the transactions in the window where
>   the transaction originated.

>   If you delete a batch or a transaction within a batch, the analysis
>   information entered for the transactions in the batch or for the transaction
>   will also be deleted.

>   You can save a transaction in a batch with Analytical Accounting errors but
>   cannot post the transaction.

>   When you print the Analytical Posting Journal, detailed analysis information
>   of all accounts will be printed. This would include even accounts with
>   errors. The Analytical Validation Log report detailing all Analytical
>   Accounting errors will also be printed. You can correct Analytical
>   Accounting errors by opening the batch and then correcting each of the
>   transactions that have errors.

#### Posting through to General Ledger for transaction posting

>   If you have marked the following options, individual transactions and
>   batches posted from Sales Order Processing will automatically update the
>   appropriate posting accounts in General Ledger if there are no Analytical
>   Accounting and Microsoft Dynamics GP errors.

-   Post through General Ledger files under Posting Setup (Administration \>\>
    Setup \>\> Posting \>\> Posting); and

-   Post through to General Ledger for Trx Posting (Administration \>\> Setup
    \>\> Company \>\> Analytical Accounting \>\> Setup)

>   While posting individual and batch transactions, Analytical Accounting or
>   Microsoft Dynamics GP errors may exist which would prevent the transaction
>   or batch from updating the appropriate posting accounts in General Ledger.
>   For example, default codes may not be assigned for Required Transaction
>   Dimensions in the account class to which the distribution accounts of Fixed
>   or Variable accounts are linked. The transaction or batch will update the
>   General Ledger. You must correct the errors in the transaction or batch in
>   General Ledger from the Transaction Entry window (Transactions \>\>
>   Financial \>\> General) before the posting accounts can be updated.

>   The Analytical Accounting and Microsoft Dynamics GP errors will be displayed
>   in the Analytical Accounting Validation Log Report which will print after
>   the transaction or batch updates Sales Order Processing.

>   The transaction and batch will update Sales Order Processing. You can view
>   analysis information that originated for the transaction or batch in Sales
>   Order Processing from the relevant Inquiry windows.

#### Voiding transactions with analysis information

>   If you void an unposted invoice or return in the Sales Transaction Entry
>   window, the analysis information entered for the document will be deleted.

>   If you void an invoice or return posted from Sales Order Processing from

>   Receivables Posted Transaction Maintenance window (Transactions \>\> Sales
>   \>\> Posted Transactions), analysis information created for the invoice or
>   return will be copied for each distribution account linked to an account
>   class with the exception of the balance type. The Balance type of each
>   distribution account will be reversed.

>   You can view the analysis information for a voided invoice or return in
>   General Ledger (Transactions \>\> Financial \>\> General).

>   If posted from the General Ledger, the analysis information of the voided
>   document can be viewed by zooming to the source document in the Financial
>   Inquiry windows. You can open the Analytical Accounting Inquiry window from
>   the Receivables Transaction Inquiry Zoom choosing Additional \>\> Analytical
>   Transaction or CTRL+T).

#### Viewing analysis information for sales documents

>   You can use the Analytical Sales Transaction Inquiry Zoom window to view
>   analysis information that you have entered for invoices or returns in Sales
>   Order Processing.

>   **To view analysis information for sales documents:**

1.  Open the Analytical Sales Transaction Inquiry Zoom window.  
    (Inquiry \>\> Sales \>\> Sales Documents \>\> Click Document Number link
    \>\>Additional \>\> Analytical Transaction)  
    (Inquiry \>\> Sales \>\> Sales Documents \>\> Click Document Number link
    \>\>Distributions \>\> Additional \>\> Analytical Transaction)

>   The Analytical Sales Transaction Inquiry Zoom window displays all the
>   analysis information you’ve created for a distribution account.

1.  The first distribution account of the document linked to an account class is
    displayed. To view analysis information of other distribution accounts,
    enter or select a distribution number.

>   If you select a specific account in the Sales Distribution Inquiry Zoom, the
>   Analytical Sales Inquiry window will display analysis information relating
>   to such account.

>   The information in the Document Type and Number field will correspond to
>   that in the Sales Transaction Inquiry zoom.

1.  The Originating or Functional Amount field displays the distribution amount
    in the originating or functional currency based on the option you have
    chosen in the Currency View. Click the expansion button to view
    multicurrency information if the originating currency differs from the
    functional currency.

>   The Document Date displays the date of the document and will default from
>   the Sales Transaction Inquiry zoom.

>   The Company ID field displays the ID of the current company.

1.  Click Expand to display all analysis information entered for the
    distribution account in the list window. This would comprise assignments,
    reference information entered per assignment, transaction dimensions and
    their codes.

2.  Click Collapse to display only assignments and reference information entered
    per assignment for the distribution account.

3.  You also can view all information entered for each assignment or just
    reference information that may exist. Choose the plus button (+) available
    next to each assignment to view all analysis information entered for an
    assignment or choose the minus button (-) to view only reference
    information.

4.  Choose OK to close the window.

#### Copying Analytical Accounting Information for Sales Order

>   Use the Copy a Sales Order window to copy analytical accounting information
>   from one sales order document to another.

>   **To copy analytical accounting information for sales order:**

1.  Open copy a Sales Order window  
    (Transaction\>\> Sales \>\> Sales Transaction Entry \>\>enter a sales order
    number \>\> Actions \>\> Copy)

>   IMAGE – AACSO.jpg

![](media/2de46d8fe2a52c2cd480699da271aef8.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Choose Actions and select copy to open the Copy a Sales Order window.

2.  Enter or select the document number for the document that contains the
    information to copy.

3.  Mark the Copy Analytical Accounting information option.

4.  Choose copy. The analytical accounting information is copied from the
    originating document to the new document.

>   *Analytical Accounting information is copied only for invoice and Return
>   type of documents in the Sales Transaction Entry window.*

**Chapter 9: Inventory Transactions**

>   Use the following information to create analysis information for Inventory
>   transactions.

>   This information is divided into the following sections:

-   *Entering analysis information for inventory transactions*

-   *Entering analysis information during transfer entry*

-   *Entering analysis information for variance accounts*

-   *Posting inventory transactions*

-   *Batch posting*

-   *Series posting*

-   *Post through General Ledger for transaction posting*

-   *Viewing analysis information for inventory transactions*

#### Entering analysis information for inventory transactions

>   You can enter analysis information such as transaction dimension codes and
>   reference information for inventory transactions. You cannot create
>   assignments as the Extended Cost of a document can be determined only after
>   the transaction is posted.

>   You can enter analysis information for adjustment, variance and transfer
>   transactions and view the Item Number, Site ID, Balance Type, and the
>   Inventory and/or Offset accounts. This is possible only if such accounts are
>   linked to an account class in the Analytical Item Transaction Entry,
>   Analytical Item Transfer Entry or Analytical Stock Count Entry window.

>   The Analytical Item Transaction/Transfer/Stock Count Entry window will only
>   display those distribution accounts attached to an item number that are
>   linked to an account class.

>   For Inventory transactions, the Analytical Transaction Entry windows will
>   open when you TAB off the Item line in the Item Transaction, Item Transfer
>   or Stock Count Entry windows. This will only happen if one or both of the
>   distribution accounts associated with the item number are linked to an
>   account class, and if the window has not been previously opened for such
>   accounts.

>   If you are tracking inventory items by serial or lot numbers, the Analytical
>   Transaction Entry window will open automatically when you press TAB only
>   after you close the Item Serial/Lot Number Entry window.

>   *In the Inventory Batch Entry window, if the option Post to General Ledger
>   is not marked in the Posting Setup window (Administration \>\> Setup \>\>
>   Posting \>\> Posting), the Analytical Transaction Entry window will not open
>   when you TAB off an item line in the Item Transaction or Item Transfer Entry
>   window.*

>   The Analytical Transaction Entry window will open automatically only once
>   except in the following instances.

-   The Site ID is changed in the scrolling window of the Item Transaction Entry
    window.

-   The From and/or To Site ID are changed in the scrolling window in the Item
    Transfer Entry window.

-   The quantity is changed from positive to negative or from negative to
    positive in the Item Transaction Entry window.

-   The variance quantity is changed from positive to negative or from negative
    to positive in the Stock Count Entry window.

-   The distribution account is changed in the Distribution window. In this case
    the analysis information that you entered will be deleted.

-   Change in quantity type in the Item Transfer Entry window.

>   You can also open the Analytical Transaction Entry window from the Item
>   Transaction or Item Transfer or Stock Count Entry windows and the
>   Distribution windows from Additional \>\> Analytical Transaction Entry or by
>   using CTRL+T.

>   If the quantity of an item number in the Item Transaction or Item Transfer
>   windows has not been specified, the Analytical Transaction Entry window will
>   not open automatically from Additional \>\> Analytical Transaction Entry or
>   using CTRL+T.

>   In the Stock Count Entry window, if the variance quantity is zero, the
>   Analytical Transaction Entry window will not open automatically from
>   Additional \>\> Analytical Transaction Entry or by using CTRL+T.

>   If you delete the quantity specified for an item number in the Item
>   Transaction, Item Transfer or Stock Count Entry windows, the analysis
>   information created for such item number also will be deleted.

>   **To enter analysis information during transaction entry:**

1.  Open the Analytical Item Transaction Entry window.  
    (Transactions \>\> Inventory \>\> Transaction Entry \>\> Analytical
    Accounting button)  
    (Transactions \>\> Inventory \>\> Transaction Entry \>\> CTRL+T or
    Additional menu\>\> Additional \>\> Analytical Transaction Entry)  
    (Transactions \>\> Inventory \>\> Stock Count Entry \>\> Analytical
    Accounting button)  
    (Transactions \>\> Inventory \>\> Stock Count Entry \>\> CTRL+T \>\>
    Additional \>\>Analytical Transaction Entry)

IMAGE – AAIE.jpg

![A screenshot of a cell phone Description automatically generated](media/459376694b78cc322336cc0b6848f7c6.jpg)

>   The Analytical Item Transaction Entry window displays the first distribution
>   account of the Item Number selected that is linked to an account class. To
>   view other distributions enter or select a distribution number. The
>   distribution lookup displays all distribution accounts of the transaction
>   linked to an account class.

>   The Account field will display the distribution account for which analytical
>   information is being entered. The description of the account, as set up in
>   the Account Maintenance window, will appear in the next line. Click the
>   Account expansion button to open the Microsoft Dynamics GP Account Entry
>   window.

>   The balance type of the account, whether debit or credit, will be displayed
>   next to the account.

1.  In the Reference field, enter reference information for the account.

>   The Item field will display the item number of the distribution account for
>   which you are entering analysis information. This will appear as a default
>   value from the Item Transaction Entry window.

>   The Site ID of the item number as displayed in the Item Transaction Entry
>   window will be displayed.

1.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes,
    if required. Refer to *Creating an alias* for more information.

2.  Choose Default to load the current setup information specified for the
    account class in the Accounting Class Maintenance window and create a single
    assignment.

>   The Trx Dimension field displays Transaction Dimensions of the account class
>   to which the distribution account is linked. Only Transaction Dimensions
>   which have been set as Fixed, Required, or Optional will be displayed.

>   Transaction dimensions which are set to Hide in the Accounting Class
>   Maintenance window will not be displayed. Refer to *Setting up an account
>   class* for more information.

>   The Trx Dimension Description field displays the description of the
>   transaction dimension.

1.  Enter or select an alphanumeric transaction dimension code in the
    Alphanumeric column. You can add a new alphanumeric transaction dimension
    code if you have selected the Create New Codes On The Fly option in the
    Transaction Dimension Maintenance window.

>   *The Alphanumeric column is available only for an alphanumeric transaction
>   dimension.*

>   The description of the Alphanumeric Transaction Dimension Code is displayed
>   in the Transaction Dimension Code Description field.

1.  Enter a Transaction Dimension Code in the Numeric, Yes/No or Date field if
    the Transaction Dimension is Numeric, Boolean or Date.

2.  Select the type of account that you want to browse through for each item
    number entered in the Item Transaction Entry window, from the following:

>   **All** to browse through the Inventory and Offset accounts for each item
>   number if it is linked to an account class.

>   **Inventory** to browse through the Inventory account of each Item Number if
>   it is linked to an account class.

>   **Offset** to browse through the Offset account of each item number if it is
>   linked to an account class.

>   *The Radio Group will further filter accounts if you select View \>\>
>   Incomplete or Erroneous Dist.*

1.  Choose OK to save and close the window.

2.  Choose Save to save the analysis information you have entered and clear the
    window.

>   You can save analysis information with errors, but you cannot post them.

1.  Choose Contra to switch between the inventory account and the offset account
    of the item number that is currently displayed in the Analytical Item
    Transaction Entry window. This is possible only if both the Inventory and
    Offset accounts of an item number are linked to an account class.

>   If only one account of an item number is linked to an account class, a
>   message appears when you select the Contra button.

1.  Choose Validate to validate the distribution displayed in the window. If
    changes are made to the account class in setup or errors are found during
    the validation process, the Analytical Accounting Validation Log window will
    open displaying the errors or changes identified. You can view the changes
    to the account class by selecting the Default button in the Analytical Item
    Transaction Entry window.

>   *Analysis information will also be validated if you select OK or Save in the
>   Analytical Item Transaction Entry window.*

>   You can choose to save analysis information with errors or without updating
>   changes made to the account class.

>   You can validate a document in the Item Transaction Entry window by using
>   the options CTRL+R or Additional \>\> Run Validation.

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

1.  Choose the Print drop-down to print the Analytical Accounting Edit list for
    the distribution currently displayed in the window or for all distributions
    of the transaction linked to an account class. If errors are detected, the
    Analytical Validation Log is also printed.

2.  If you delete a transaction in the Item Transaction window, the analysis
    information you entered for the transaction will be deleted.

3.  You cannot insert or delete a row, or change the Site ID or distribution
    accounts in the Item Transaction Entry window if the Analytical Item
    Transaction Entry window is open.

#### Entering analysis information during transfer entry

>   You can enter analysis information for inventory transfers in the Analytical
>   Item Transfer Entry window.

>   **To enter analysis information during transfer entry:**

1.  Open the Analytical Item Transfer Entry window.  
    (Transactions \>\> Inventory \>\> Transfer Entry \>\> Analytical Accounting
    button)  
    (Transactions \>\> Inventory \>\> Transfer Entry \>\> CTRL+T or Additional
    \>\> Analytical Transfer Entry)

2.  Enter or select the distribution number for the distribution account.

>   The Company ID field will display the company in which the transaction is
>   taking place.

1.  The Account field will display the distribution account for which the
    Analytical information is being entered and the balance type of the account,
    whether debit or credit. The description of the account, as set up in the
    Account Maintenance window, will appear in the next line. Click the Account
    expansion button to open the Microsoft Dynamics GP Account Entry window.

2.  In the Reference field, enter reference information up to 30 characters for
    the account or distribution.

>   The balance type of the account, whether debit or credit, will be displayed
>   next to the account.

>   The Item field will display the item number for the distribution account for
>   which you are entering analysis information. This will appear as a default
>   value from the Transfer Entry window.

>   The From Site ID and To Site ID of the Item Number in the Inventory Transfer
>   Entry window are displayed.

1.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes
    if required. Refer to *Creating an alias* for more information.

2.  Choose Default to load the default transaction dimension codes if you
    overwrite the codes of Required or Optional Alphanumeric Transaction
    Dimensions while creating analysis information.

3.  The transaction dimensions for the account class to which the distribution
    account is linked are displayed in the scrolling window. Only transaction
    dimensions which have been set as Fixed, Required, or Optional will be
    displayed. Transaction dimensions which are set to Hide in the Accounting
    Class Maintenance window will not be displayed. Refer to *Setting up an
    account class* for more information.

4.  Enter or select a transaction dimension code in the Alphanumeric column.

5.  Enter a numeric transaction dimension code in the Numeric field.

6.  Mark or unmark the Yes/No checkbox in the Yes/No column.

7.  Enter a date type transaction dimensions in the Date field.

>   The description of the transaction dimension is displayed in the Transaction
>   Dimension Description field.

>   The description of the alphanumeric transaction dimension code will be
>   displayed in the Transaction Dimension Code Description field.

1.  Select the type of account that you want to browse through from the
    following:

>   **All** to browse through the inventory and offset accounts for each item
>   number if it is linked to an account class.

>   **Inventory** to browse through the inventory account of each item number if
>   it is linked to an account class.

>   **Offset** to browse through the offset account of each item number if it is
>   linked to an account class.

1.  Choose Contra to switch between the offset account and the inventory account
    of the item number that is currently displayed in the Analytical Transaction
    Entry window. This button is available only if both the inventory and the
    offset accounts for an item number are linked to an account class.

2.  Choose Save to save the analysis information for the distribution.

3.  Choose Clear to clear the information you have entered.

4.  Choose Validate to validate the distribution displayed in the window. You
    can also validate transactions by choosing CTRL+R or from Additional \>\>Run
    validation. Refer to *Validating transactions and correcting errors* for
    more information about the validation process.

5.  Choose the Print drop-down list to print information for the distribution
    displayed in the window or for all distributions.

6.  If you delete a transaction in the Inventory Transfer window the analysis
    information you entered for the transaction will also be deleted.

7.  You cannot insert or delete a row, or change the Site ID or distribution
    accounts in the Item Transfer Entry window if the Analytical Item Transfer
    Entry window is open.

#### Entering analysis information for variance accounts

>   You can create analysis information for variance transactions in the
>   Analytical Stock Count Entry window. The window can be opened from the Stock
>   Count Entry window by choosing Additional \>\> Analytical Transaction Entry
>   or CTRL+T.

>   You can enter analysis information such as transaction dimension codes and
>   reference information for the transactions in this window. Refer to
>   *Entering analysis information for inventory transactions* for more
>   information about entering analysis information for inventory transactions.

>   If you choose Clear Count in the Stock Count Entry window, the analysis
>   information you’ve entered for the transaction also will be deleted.

>   You cannot change the quantity or distribution accounts in the Stock Count
>   Entry window or the Unit of Measure in the Stock Count Unit of Measure
>   window or make changes in the Stock Count Serial/Lot Number Entry window if
>   the Analytical Stock Count Entry window is open.

#### Posting inventory transactions

>   When you post a transaction with analysis information from the Item
>   Transaction or Item Transfer window or process a Stock Count Schedule in the
>   Stock Count Entry window, a validation takes place for the document.

>   If selected in Posting setup, the Analytical Posting Journals will be
>   printed along with the Microsoft Dynamics GP Journal. If no errors are found
>   during the validation process, the document will be posted.

>   If errors are detected in the Microsoft Dynamics GP or Analytical Accounting
>   transactions, the Analytical Validation Log window will open displaying all
>   the errors. You can double click on an Analytical Accounting error to go to
>   the relevant distribution in the Analytical Transaction Entry window. You
>   cannot zoom to a Microsoft Dynamics GP window from the Analytical Validation
>   Log.

>   We recommend that you correct the Microsoft Dynamics GP errors first before
>   correcting the Analytical Accounting errors.

>   In the Stock Count Entry window, if Autopost Stock Count Variances is not
>   marked, the analysis information created will update the Item Transaction
>   Entry window when you process the Stock Count Schedule.

#### Batch posting

>   You can print the Analytical Accounting Edit List along with the Microsoft

>   Dynamics GP Edit List from the Inventory Batch Entry window. The Analytical
>   Validation Log is also printed if there are any Analytical Accounting errors
>   in the transactions in the batch.

>   You can also print the Analytical Accounting Edit List from the Item
>   Transaction or Item Transfer Entry window.

>   Analysis information that has been created for transactions in an inventory
>   batch will not be posted if the Post to General Ledger option is not marked
>   in the Inventory Batch Entry window.

>   If the option Post to General Ledger is marked, the analysis information
>   entered for transactions in a batch will be validated when you choose Post.
>   Transactions that do not have any Microsoft Dynamics GP or Analytical
>   Accounting errors will be posted. The Analytical Posting Journal will be
>   printed with the Microsoft Dynamics GP Posting Journals if specified in
>   Posting setup. If errors are found during the validation process, the
>   Analytical Validation Log report will be printed. Refer to *Validating
>   transactions and correcting errors* for more information.

>   When you delete a single or recurring use batch or a transaction within such
>   batches, the analysis information you’ve entered for the transaction
>   distributions in the batch or for the transaction will also be deleted.

>   For recurring batches, you must enter analysis information each time the
>   batch is posted.

#### Series posting

>   When you post multiple batches from the Series Posting window, batches with
>   analysis information are validated. You can modify the analysis information
>   created for transactions in a batch before posting.

>   When you post batches, transactions without any errors will be posted.
>   Transactions with errors will not be posted and the errors will be listed in
>   the Analytical Validation Log. The errors must be corrected before you post
>   the transactions again.

>   The Analytical Posting Journal is printed for all transactions that are
>   successfully posted in each batch.

#### Post through General Ledger for transaction posting

>   If you have marked the following options, online transactions and batches
>   posted from Inventory will automatically update the appropriate posting
>   accounts in General Ledger if there are no Analytical Accounting and
>   Microsoft Dynamics GP errors.

-   Post through General Ledger files under Posting Setup (Administration \>\>
    Setup \>\> Posting \>\> Posting); and

-   Post through to General Ledger for Trx Posting (Administration \>\> Setup
    \>\> Company \>\> Analytical Accounting \>\> Setup)

>   While posting online and batch transactions, Analytical Accounting or
>   Microsoft Dynamics GP errors may exist which would prevent the transaction
>   or batch from updating the appropriate posting accounts in General Ledger.
>   For example, default codes may not be assigned for Required Transaction
>   Dimensions in the account class to which the distribution accounts of Fixed
>   or Variable accounts are linked. The transaction or batch will update the
>   General Ledger. You must correct the errors in the transaction or batch in
>   General Ledger from the Transaction Entry window (Transactions \>\>
>   Financial \>\> General) before the posting accounts can be updated.

>   The Analytical Accounting and Microsoft Dynamics GP errors will be displayed
>   in the Analytical Accounting Validation Log Report which will print after
>   the transaction or batch updates Sales Order Processing.

>   The transaction and batch will update Sales Order Processing. You can view
>   analysis information that originated for the transaction or batch in Sales
>   Order Processing from the relevant Inquiry windows.

#### Viewing analysis information for inventory transactions

>   Use the Analytical Inventory Transaction Inquiry window to view the analysis
>   information that has been created for accounts associated with an Item
>   Number in the Item Transaction or Item Transfer or Stock Count Entry
>   windows.

>   You can view transaction dimension codes and other related information such
>   as reference notes created for the accounts.

>   A single assignment equal to the transaction distribution amount will be
>   displayed for each distribution account linked to an account class, which
>   can be viewed in the Analytical Inventory Transaction Inquiry window.

>   **To view analysis information for inventory transactions:**

1.  Open the Analytical Inventory Transaction Inquiry window.  
    (Inquiry \>\> Inventory \>\> Item Transaction \>\> Select an Item Number
    \>\>Additional \>\> Analytical Transaction)

>   The Analytical Inventory Inquiry window displays the first distribution of
>   the Item Number selected that is linked to an account class.

>   **The Document Type field** Displays the type of transaction.

**The Number field** Displays the document number.

>   **The Item field** Displays the item number relevant to the account
>   displayed. **The Site ID field** Displays the site ID of the item number.

1.  Enter or select the distribution in the Distribution field. The Distribution
    lookup will only display those distributions that are linked to an account
    class.

2.  The Account field will display the account for which you are viewing
    analysis information. The description for the account is displayed in the
    next line. The expansion button will open the Microsoft Dynamics GP Account
    Entry window.

3.  The distribution amount is displayed in the functional amount field. The
    type of balance, whether credit or debit, is displayed next to the
    Functional Amount field.

4.  The transaction date of the document selected is displayed in the
    Transaction Date field.

5.  The Company ID field displays the ID for the current company.

6.  Select the Expand button to view all analysis information created for the
    distribution account in the list window. This would comprise assignments
    (always single), reference information, transaction dimensions and their
    codes.

7.  Select the Collapse button to view only assignments and reference
    information.

8.  You can also view all information created for each account or just reference
    information that may exist. Select the +/- buttons available next to the
    assignment to view all analysis information created for the account or only
    reference information that may exist.

9.  Select the type of account that you want to browse through from the
    following:

>   **All** You can browse through the inventory and offset accounts for each
>   item number if it is linked to an account class.

>   **Inventory** You can browse through the Inventory account of each item
>   number if it is linked to an account class.

>   **Offset** You can browse through the Offset account of each item number if
>   it is linked to an account class.

1.  Choose Contra to switch between the Inventory account and the Offset account
    of the Item Number that is currently displayed in the Analytical Inventory
    Inquiry window. This is possible only if both the Inventory and Offset
    accounts of an Item Number are linked to an account class.

2.  If only one account of an Item Number is linked to an account class, a
    message appears when you click the Contra button.

3.  Click the printer icon button to print information for the distribution
    displayed in the Inquiry window or for all distributions of the document
    that are linked to an account class.

4.  Choose OK to close the window.

**Chapter 10: Fixed Asset Transaction**

>   Analytical Transfer Maintenance window is used to maintain information on
>   the asset transfer for Fixed Asset module. You can view the transaction
>   dimension codes and description for the transaction dimension codes for
>   fixed asset transactions. You can enter or select the Alias details in the
>   Analytical Transfer Maintenance window.

>   For transactions in Fixed Asset, you can create assignments and enter
>   transaction dimension codes for the distribution accounts that are linked to
>   an account class. You can save transactions with analysis information to a
>   single or recurring batch prior to posting the batch. The process of
>   validating transactions with analysis information is also explained in the
>   Analytical fixed Asset Transaction Entry window.

>   This information is divided into the following sections:

-   *Entering Analysis information for Asset Transfer*

-   *Entering analysis information for Fixed Asset Transaction*

-   *Viewing analysis information for Financial Detail*

-   *Viewing analysis information for Asset Account*

-   *Viewing analysis information for Transfer*

#### Entering Analysis information for Asset Transfer

>   Use the Analytical Transfer Maintenance window to enter the analytical
>   information for assets transferred from one location, structure ID, account
>   number, or master asset ID to another.

>   **To enter analysis information on asset transfer**

1.  Open the Analytical Transfer Maintenance window  
    (Transactions \>\> Fixed Asset \>\> Transfer \>\> enter or select an asset
    ID\>\>Additional \>\> Analytical Transaction or CTRL+T)  
    (Transactions \>\> Fixed Assets \>\> Transfer \>\> enter or select an asset
    ID \>\> G/L Accounts expansion button\>\> Expand Transfer\>\> Analytical
    Accounting Button)

>   IMAGE – AATM.jpg

![](media/2e1b0bce0f68b61920a1d3a969bf0993.jpg)

>   A screenshot of a social media post Description automatically generated

1.  The Distribution field displays the first distribution account of the Item
    Number selected one of the account associated to Asset ID.To view other
    distributions, enter or select a distribution number. Select the
    distribution lookup button to view all the distribution accounts of the
    transaction linked to an account class in the Analytical Asset Account
    Lookup window.

>   The Company ID field will display the company in which the transaction is
>   taking place.

1.  The Account field will display the distribution account for which analytical
    information is being entered. The description of the account, as set up in
    the Account Maintenance window, will appear in the next line. Click the
    Account expansion button to open the Microsoft Dynamics GP Account Entry
    window.

>   The balance type of the account, whether debit or credit, will be displayed
>   next to the account.

1.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes,
    if required. Refer to *Creating an alias* or more information.

2.  The Trx Dimension field displays Transaction Dimensions of the account class
    to which the distribution account is linked. Only Transaction Dimensions
    which have been set as Fixed, Required, or Optional will be displayed.
    Transaction dimensions which are set to Hide in the Accounting Class
    Maintenance window will not be displayed. Refer to *Setting up an account
    class* for more information.

>   The Trx Dimension Description field displays the description of the
>   transaction dimension.

1.  Enter or select an alphanumeric transaction dimension code in the
    Alphanumeric column. You can add a new alphanumeric transaction dimension
    code if you have selected the Create New Codes On The Fly option in the
    Transaction Dimension Maintenance window.

>   *The Alphanumeric column is available only for an alphanumeric transaction
>   dimension.*

>   The description of the Alphanumeric Transaction Dimension Code is displayed
>   in the Transaction Dimension Code Description field.

1.  Enter a Transaction Dimension Code in the Numeric, Yes/No or Date field if
    the Transaction Dimension is Numeric, Boolean or Date.

2.  Choose OK to save and close the window.

3.  Choose Save to save the analysis information you have entered and clear the
    window.

4.  Choose Validate to validate the distribution displayed in the window. If
    changes are made to the account class in setup or errors are found during
    the validation process, the Analytical Accounting Validation Log window will
    open displaying the errors or changes identified. You can view the changes
    to the account class by selecting the Default button in the Analytical Item
    Transaction Entry window.

>   *Analysis information will also be validated if you select OK or Save in the
>   Analytical Fixed Asset Setup window.*

>   You can choose to save analysis information with errors or without updating
>   changes made to the account class.

>   You can validate a document in the Item Transaction Entry window by using
>   the options CTRL+R or Additional \>\> Run Validation.

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

1.  Choose the Print drop-down to print the Analytical Accounting Edit list for
    the distribution currently displayed in the window or for all distributions
    of the transaction linked to an account class. If errors are detected, the
    Analytical Validation Log is also printed.

#### Entering analysis information for Fixed Asset Transaction

>   Use the Analytical Fixed Asset Transaction Entry windows to enter analysis
>   information for transactions for Fixed Asset module. The window name depends
>   upon the path where you open this window.

>   You can enter assignments and transaction dimension codes for fixed asset
>   documents using the Analytical Fixed Asset Transaction Entry window.Also,
>   you can view analysis information created for transactions in the Analytical
>   Inquiry windows.

>   You can open the Analytical Transaction Entry window only if Analytical
>   Accounting has been activated. Refer to *Activating Analytical Accounting*
>   for more information about activating Analytical Accounting.

>   In case of multicurrency transactions, a change in the transaction date
>   re-creates distributions due to a change in the exchange rate. If the
>   transaction date is modified, analysis information created previously is
>   deleted when the distributions are re-created.

>   **To enter Analytical Fixed Asset Transaction Entry**

1.  Open the Analytical Fixed Asset Transaction Entry window.  
    (Cards\>\> Fixed Asset\>\> Book\>\> select Book ID and enter Asset
    ID\>\>Analytical Accounting Icon.)  
    (Cards\>\> Fixed Asset\>\> Book\>\> select Book ID and enter Asset
    ID\>\>Additional \>\> Analytical Transaction or CTRL+T)  
    (Cards\>\> Fixed Asset\>\> Book\>\> select Book ID and enter
    AssetID\>\>Distributions\>\> Financial Detail Maintenance\>\> Analytical
    Accounting Icon) (Cards\>\> Fixed Asset\>\> Book\>\> select Book ID and
    enter Asset ID\>\>Distributions\>\> Financial Detail Maintenance\>\>
    Additional\>\> Analytical Transaction or CTRL+T)  
    (Administration \>\> Routines\>\> Fixed Assets\>\> GL Posting\>\> Analytical
    Accounting Icon)  
    (Administration \>\> Routines\>\> Fixed Assets\>\> GL Posting\>\>
    Additional\>\> Analytical Transaction or CTRL+T)

>   IMAGE – AAFAT.jgp

![](media/95d3b57608389dbfe5fe9be1c8f20e8b.jpg)

>   A screenshot of a computer Description automatically generated

1.  The Distribution field displays the first distribution account of the one of
    the account associated to Asset ID. To view other distributions for the
    transaction, enter or select a distribution number.

>   The sequence of distributions in the Analytical Fixed Asset Transaction
>   Entry window may not correspond to the sequence in the Fixed Asset Entry
>   window because only accounts linked to an account class are displayed in the
>   Analytical Payroll Transaction Entry window.

1.  In the list window, enter the transaction distribution amount in functional
    or originating currency, by value or on a percentage basis.

2.  Enter the assignment in percentage value in the Assign% field. Initially, a
    single assignment is created by default. You can overwrite the assignment
    with more than one assignment.

>   You can save analysis information for a distribution even if the assignment
>   is not 100%. However, you can post a transaction with partial assignments
>   only if you have opted to allow partial assignments during posting for the
>   module you’re working in. Refer to *Setting up assignment options* for more
>   information.

1.  Select an alias in the Alias field. The Alphanumeric field in the scrolling
    window displays the transaction dimension codes that are associated with the
    alias for the transaction dimensions displayed. You can change these codes
    if required. Refer to Creating an alias for more information.

2.  Enter reference information for the assignment in the Reference field.

3.  Choose Delete Row to delete a single row in the assignment List View. You
    cannot choose this option if only a single assignment has been entered.

4.  Choose Remaining to add one assignment for the remaining unassigned amount.
    The new assignment will ensure that the total assigned amount equals the
    distribution amount. For example, the distribution amount is \$100 and
    you’ve entered four assignments that total \$75. When you choose Remaining,
    a fifth assignment for the remaining value, \$25 is created. This button is
    not available if the distribution field is blank or has a zero value.

5.  Choose Default to load the current setup information specified for the
    account class in the Accounting Class Maintenance window and create a single
    assignment. The following processes will occur:

    -   Fixed, Required, and Optional Transaction Dimensions (including hidden
        transaction dimensions) will be installed.

    -   All the assignments that you have created for the current distribution
        will be removed and create a single assignment that is equal to the
        distribution amount will be created.

    -   If the analysis type is changed to or from Not Allowed, transaction
        dimensions will be added or removed.

    -   Transaction dimensions that have been deleted will be removed.

6.  Enter or select the code for each alphanumeric transaction dimension in the
    alphanumeric column. If you’ve marked the Show valid code combinations in
    trns and budgets option in the Analytical Accounting Options window, then
    the lookup window will display only those codes that have a valid
    combination with the codes you have already selected for the transaction.

7.  Enter a transaction dimension code in the Numeric, Yes/No or Date field for
    a Numeric, Boolean or Date type Transaction Dimension.

8.  Choose OK to save your changes and close the window. The analysis
    information that you have entered is validated when you choose OK. Refer to
    Validating transactions and correcting errors for more information.

9.  Choose Save to save the analysis information you have entered and clear the
    window. A validation takes place when you choose Save in the Analytical
    General Transaction Entry window. Refer to Validating transactions and
    correcting errors for more information. You can save the analysis
    information with errors or without updating changes made to the account
    class.

10. Choose Clear to clear the information from the Analytical General
    Transaction Entry window.

11. Choose Validate to validate the analysis information of the distribution
    displayed in the window. If changes are made to the account class in the
    Analytical Accounting setup or errors are found during the validation
    process, the Analytical Accounting Validation Log window will open where you
    can view the errors or changes. Refer to Validating transactions and
    correcting errors for more information about validation.

12. To view the changes to the account class choose the Default button in the
    Analytical General Transaction Entry window. Double click on an Analytical
    Accounting error to open the Analytical Accounting General Transaction Entry
    window where the specific error will be highlighted.

13. Choose the printer icon button to print the Analytical Accounting edit list
    for the current distribution displayed or for all distributions of the
    transaction linked to an account class. The Analytical Accounting Validation
    Log report which describes the Analytical Accounting errors also is printed.

#### Viewing analysis information for Financial Detail

>   You can view analysis information for financial detail in the Analytical
>   Financial Detail Inquiry window.

>   **To view analysis information for financial detail**

1.  Open the Analytical Financial Detail Inquiry window  
    (Inquiry \>\> Fixed Assets \>\> Financial Detail \>\> enter or select an
    asset ID \>\> select a book ID \>\> select a line \>\> Additional \>\>
    Analytical Transaction or CTRL+T)

2.  Enter or select an asset ID and select a book ID.

3.  Select a transaction and select Additional and choose Additional \>\>
    Analytical Transaction or CTRL+T to open the Analytical Financial Detail
    Inquiry window.

4.  In the Analytical Financial Detail Inquiry window, click the account
    expansion button to open the Account Entry window to enter or select an
    alias for an account.

5.  Choose OK to close the Analytical Financial Detail Inquiry window.

#### Viewing analysis information for Asset Account

>   You can view analysis information for asset account in the Analytical Asset
>   Account Inquiry window.

>   **To view analysis information for asset account**

1.  Open the Analytical Asset Account Inquiry window  
    (Inquiry \>\> Fixed Assets \>\> General\>\> enter or select an asset ID \>\>
    Goto button \>\> Account \>\>Additional \>\> Analytical Transaction or
    CTRL+T)

2.  Enter or select an Asset ID in the Asset Inquiry window.

3.  Choose the Goto button to select the Account option.

4.  Select Additional and choose Additional \>\> Analytical Transaction or
    CTRL+T to open the Analytical Asset Account Inquiry window.

5.  In the Analytical Asset Account Inquiry window, click the account expansion
    button to open the Account Entry window to enter or select an alias for an
    account.

6.  Choose OK to close the Analytical Asset Account Inquiry window.

#### Viewing analysis information for Transfer

>   You can view analysis information for Transfer Assets in the Analytical
>   Transfer Inquiry window.

>   **To view the transfer analysis information**

1.  Open Analytical Transfer Inquiry window  
    (Inquiry \>\> Fixed Assets \>\> Transfer\>\> enter or select asset ID \>\>
    Additional\>\> Analytical Transaction or CTRL+T)

2.  Enter or select an Asset ID in the Asset Inquiry window.

3.  Select Additional and choose Additional \>\> Analytical Transaction or
    CTRL+T to open the Analytical Transfer Inquiry window.

4.  In the Analytical Transfer Inquiry window, click the account expansion
    button to open the Account Entry window to enter or select an alias for an
    account.

5.  Choose OK to close the Analytical Transfer Inquiry window.

**Chapter 11: Bank Reconciliation Transactions**

>   You can enter and view analysis information for transactions in Bank

>   Reconciliation. This would comprise creating assignments and entering
>   transaction dimension codes for accounts that are linked to an account
>   class.

>   This information is divided into the following sections:

-   *Entering analysis information for bank transactions and receipts*

-   *Voiding transactions or receipts*

-   *Entering analysis information for bank transfers*

-   *Voiding bank transfers*

-   *Entering analysis information for reconcile adjustments*

-   *Validating transactions and correcting errors*

-   *Posting transactions with analysis information*

-   *Entering analysis information for deposits*

-   *Viewing analysis information in Bank Reconciliation*

#### Entering analysis information for bank transactions and receipts

>   You can create assignments, enter transaction dimension codes, and reference
>   information for accounts that are linked to an account class in the
>   Analytical Bank Transaction Entry window. You can modify the analysis
>   information that you have entered at any time before posting the document.

>   The Analytical Bank Transaction Entry window opens automatically when you
>   press TAB from a row in the Bank Transaction Entry window in the following
>   instances:

-   If the distribution account is linked to an account class and the Analytical
    Bank Transaction Entry window has not been opened even once for the account
    and if all required fields have been entered in the Bank Transaction Entry
    window.

>   The Analytical Bank Transaction Entry window also opens automatically If the
>   following changes are made:

-   Change in distribution account other than the checkbook account.

-   Change in checkbook amount.

-   Change in amount of other distribution accounts.

-   Change from debit to credit or vice versa.

-   Change in amount from positive to negative or vice versa.

>   These changes would result in a deletion of the analysis information created
>   previously for the relevant account.

>   If you clear an unposted transaction or receipt from the Bank Transaction
>   Entry window, the analysis information that exists for the transaction or
>   receipt will be deleted.

>   If you choose to clear previous entries after you change the Option or Type
>   in the Bank Transaction Entry window the analysis information that exists
>   for the checkbook account and all other distribution accounts that are
>   linked to an account class will be deleted.

>   If you choose to continue using entries in a new transaction after changing
>   the

>   Option in the Bank Transaction Entry window (except for a change from Enter
>   Transaction to Enter Receipt or vice versa), analysis information entered
>   for the checkbook account and all other distribution accounts that are
>   linked to an account class will be deleted.

>   If you change the credit card assigned to a receipt, for which the checkbook
>   is different from the one originally assigned to the receipt, analysis
>   information that exists for the checkbook account will be deleted.

>   In the case of multicurrency transactions, the following changes will delete
>   the existing analysis information for a transaction or receipt:

-   Change from originating to functional currency (if entering receipt).

-   Change in currency ID due to a change in the checkbook ID.

-   Change in exchange rate in the Exchange Rate Entry window.

-   Change in the rate type ID in the Exchange Rate Entry window. In this case,
    distributions are re-created if the rate type ID selected is from a
    different exchange rate table ID than the one originally assigned to the
    transaction.

-   Change in transaction date.

>   **To enter analysis information for bank transactions and receipts:**

1.  Open the Analytical Bank Transaction Entry window.  
    (Transactions \>\> Financial \>\> Bank Transactions \>\> Analytical
    Accounting button)  
    (Transactions \>\> Financial \>\> Bank Transactions \>\> Additional \>\>
    Analytical Transaction or CTRL+T)

>   IMAGE – AABTE.jpg

![](media/a129760d67ac1b1acd0f2935fd4c162c.jpg)

>   A screenshot of a computer Description automatically generated

>   The Analytical Bank Transaction Entry window will only display distribution
>   accounts of a transaction or receipt that are linked to an account class.

>   For example, if a check transaction has two distribution accounts of which
>   only one is linked to an account class, then the distribution account linked
>   to the account class will be displayed in the Analytical Bank Transaction
>   Entry window. If there is more than one distribution account linked to an
>   account class, they will be displayed in the Analytical Bank Transaction
>   Entry window as per the distribution sequence. You can enter or select the
>   distribution account you want to view.

>   You can also view a specific distribution account in the Bank Transaction
>   Entry window linked to an account class, by selecting the account prior to
>   opening the Analytical Bank Transaction Entry window.

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Voiding transactions or receipts

>   When you void a transaction or receipt in the Bank Transaction Entry window,
>   the analysis information entered for the document during transaction entry
>   will be copied with the exception of the balance type. The balance type of
>   each distribution account linked to an account class will be reversed.

>   You cannot modify the analysis information of the checkbook account and
>   other distribution accounts prior to voiding. However, if you have made
>   changes to distribution accounts other than the checkbook account prior to
>   voiding that affects the analysis information entered previously for such
>   accounts during transaction entry, such information will be deleted. You
>   must re-enter analysis information for these accounts prior to voiding the
>   transaction or receipt.

>   The changes made to a distribution line that would result in a deletion of
>   analysis information include changing the account or amount or debit to
>   credit or vice versa or positive amounts to negative or vice versa.

>   When you void a transaction or receipt, the analysis information entered
>   prior to voiding will be validated. Refer *Posting transactions with
>   analysis information* for more information about validation.

#### Entering analysis information for bank transfers

>   You can enter assignments, transaction dimension codes and reference
>   information for bank transfers in the Analytical Bank Transfer Entry window.

>   *Be sure to follow the tab sequence while entering transactions in the Bank
>   Transfer Entry window, to create analysis information. You may lose data if
>   the tab sequence is not followed.*

>   The Analytical Bank Transfer Entry window will only display checkbook
>   accounts that are linked to an account class.

>   The Analytical Bank Transfer Entry window opens automatically when you press
>   TAB from a field in the following instances:

-   The Transfer To Checkbook ID field if either or both the Transfer From or
    Transfer To Checkbooks are linked to an account class and the Analytical
    Bank

>   Transfer Entry window has not been opened previously for such account. The
>   Analytical Bank Transfer Entry window will open automatically in this
>   instance only if both Checkbook IDs and the amount have been specified in
>   the Bank Transfer Entry window.

-   The Transfer From or Transfer to Checkbook ID fields, if there is a change
    in the checkbook ID that results in a change in the distribution account.

-   The amount field, if there is a change in the bank transfer amount.

>   If you clear an unposted transfer from the Bank Transfer Entry window, the
>   analysis information that exists for the transfer will be deleted.

>   In the case of multicurrency transactions, the following changes will delete
>   the existing analysis information of a transfer:

-   The Transfer From Checkbook is changed to a functional currency checkbook.

-   Change in exchange rate in the Exchange Rate Entry window.

-   Change in the Rate Type ID in the Exchange Rate Entry window. In this case,
    distributions are re-created if the Rate Type ID selected is from a
    different exchange rate table ID than the one originally assigned to the
    transaction.

-   Change in transfer date.

>   **To enter analysis information for bank transfers**

1.  Open the Analytical Bank Transfer Entry window.  
    (Transactions \>\> Financial \>\>Bank Transfers \>\> Analytical Accounting
    button)  
    (Transactions \>\> Financial \>\>Bank Transfers \>\> CTRL+T or Additional
    \>\> Analytical Transaction)

2.  Refer *Entering analysis information for General Ledger transactions* for
    more information about entering analysis information.

#### Voiding bank transfers

>   When you void a bank transfer, the analysis information that was entered for
>   the transfer will be copied, along with a change in the balance type. The
>   balance type will be reversed. You cannot modify the analysis information
>   for the transfer prior to voiding.

#### Entering analysis information for reconcile adjustments

>   You can enter analysis information for an adjustment in the Reconcile Bank

>   Adjustments window (Transactions \>\> Financial \>\> Reconcile \>\>
>   Transactions \>\>

>   Adjustments \>\> Select an adjustment \>\> CTRL+T or Additional \>\>
>   Analytical Transaction), if the checkbook account and/or adjustment account
>   are linked to an account class. The Analytical Reconcile Entry window will
>   only display accounts of an adjustment linked to an account class.

>   You can enter analysis information for one adjustment at a time. To create
>   analysis information for a specific adjustment, select the adjustment prior
>   to opening the Analytical Reconcile Entry window.

>   The Analytical Reconcile Entry window opens automatically when you press TAB
>   from a field in the Reconcile Bank Adjustments window, in the following
>   instances:

-   Either or both the distribution accounts of the adjustment are linked to an
    account class and the Analytical Reconcile Entry window has not been opened
    previously for such adjustment.

-   Change in distribution account of an adjustment

-   Change in adjustment amount

>   Analysis information entered for adjustments will be deleted if
>   reconciliation information of the Checkbook is deleted from the Reconcile
>   Bank Statements window. Also, if you delete a row in the Reconcile Bank
>   Adjustments window, analysis information that you’ve entered for
>   distribution accounts of that row will be deleted.

>   In the case of multicurrency transactions, the following changes will delete
>   the analysis information entered for an adjustment:

-   Change in the Rate Type ID in the Exchange Rate Entry window. In this case,
    distributions are re-created if the Rate Type ID selected is from a
    different exchange rate table ID than the one originally assigned to the
    transaction.

-   Change in Exchange Rate in the Exchange Rate Entry window.

-   Change in Date.

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Validating transactions and correcting errors

>   You can validate a transaction from the following windows by choosing
>   Additional \>\> Run Validation or CTRL+R.

-   Bank Transaction Entry

-   Bank Transfer Entry

-   Reconcile Bank Adjustments

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

>   In the Reconcile Bank Adjustments window, you can validate the analysis
>   information entered only for individual adjustments. To validate an
>   adjustment, select the adjustment and choose CTRL+T or Additional \>\> Run
>   Validation.

>   You can validate any analysis information entered before voiding. If errors
>   are detected during validation, the Analytical Accounting Validation Log
>   window will open displaying the errors.

>   *You can select View \>\> Incomplete or Erroneous Distributions, to browse
>   through the distribution accounts in the Analytical Transaction Entry window
>   which are incomplete or have erroneous information.*

>   To correct an Analytical Accounting error, double-click on the relevant
>   error to open the relevant Analytical Transaction Entry window. The specific
>   distribution in which the error exists is displayed which you can then
>   correct.

>   If errors are detected in the analysis information you have entered for
>   adjustments, you can save such information with errors. However, the
>   checkbook cannot be reconciled till you have rectified these errors.

#### Posting transactions with analysis information

>   When you post a transaction or transfer or reconcile a checkbook, the
>   analysis information you have entered will be validated.

>   Refer to *Validating transactions and correcting errors* for more
>   information. In addition to Analytical Accounting information, Microsoft
>   Dynamics GP data will also be validated before the transaction or transfer
>   is posted or the checkbook is reconciled.

>   If errors are found while posting a transaction or transfer, the transaction
>   or transfer will not be posted. The Analytical Accounting Validation Log
>   window will open listing the Microsoft Dynamics GP errors first and then the
>   Analytical Accounting errors.

>   To correct an Analytical Accounting error, double-click on the relevant
>   error to open the relevant Analytical Transaction Entry window. The specific
>   distribution in which the error exists is displayed which you can then
>   correct.

>   If errors are detected while reconciling a checkbook, they will be listed in
>   the Analytical Accounting Validation Log Report. You will have to select the
>   appropriate adjustment in the Reconcile Bank Adjustments window and correct
>   the errors before the checkbook can be reconciled.

>   We recommend that you resolve the Microsoft Dynamics GP errors first and
>   then the Analytical Accounting errors.

>   The Analytical Posting Journal will be printed along with the Microsoft
>   Dynamics GP Posting reports if specified under Posting Setup.

#### Entering analysis information for deposits

>   If distributions are created for realized gain or loss accounts when you
>   post deposits from the Bank Deposit Entry window (Transactions \>\>
>   Financial \>\> Bank Deposits), the Analytical Bank Deposit window will open
>   automatically if any of these accounts are linked to an account class. Refer
>   to *Entering analysis information for bank transactions and receipts* for
>   more information about entering analysis information.

>   The Analytical Bank Deposit Entry window will only display distribution
>   accounts that are linked to an account class.

>   After you have entered analysis information for the relevant accounts, a
>   validation will take place when you choose Post. If there are errors in the
>   analysis information, the Analytical Validation Log will open displaying the
>   Analytical Accounting errors. Refer to *Posting transactions with analysis
>   information* for more information.

>   The Analytical Posting Journal will print after you post the deposits, if
>   you have selected the option in the Posting Setup.

#### Viewing analysis information in Bank Reconciliation

>   You can view analysis information you’ve entered for transactions in the
>   Bank Transaction Entry, Bank Transfer Entry and Reconcile Bank Adjustments
>   windows in the Analytical inquiry window.

>   You can open the Analytical inquiry window from the Bank Transaction Entry
>   zoom or the Bank Transfer Entry zoom in the Checkbook Register Inquiry
>   window.

>   **To view analysis information in Bank Reconciliation:**

1.  Open the Analytical Bank Transaction Entry Zoom or Bank Transfer Entry zoom
    window.  
    (Inquiry \>\> Financial \>\> Checkbook Register \>\>Bank Transaction Entry
    Zoom or Bank Transfer Entry Zoom \>\> Additional \>\> Analytical Transaction
    or CTRL+T)

>   The Analytical Bank Recon Inquiry window displays all analysis information
>   created for a distribution account.

1.  The first distribution account of the document linked to an account class is
    displayed. Enter or select a distribution number to view analysis
    information of other distribution accounts.

>   If you select a specific account in the Bank Transaction Entry Zoom, the
>   Analytical Bank Recon Inquiry window will display analysis information
>   relating to such account.

>   The Document Type and Number field will default from the Bank Transaction
>   Entry or Bank Transfer Entry Zoom.

1.  The Originating or Functional Amount field displays the distribution amount
    in the originating or functional currency based on the option you have
    chosen in the Currency View. Click the expansion button to view
    multicurrency information if the originating currency differs from the
    functional currency.

2.  The Document Date field displays the transaction/ transfer date of the
    document from the Bank Transaction Entry or Bank Transfer Entry zoom.

3.  The Company ID field displays the ID of the current company.

4.  Click Expand to display all analysis information entered for the
    distribution account in the list window. This includes assignments,
    reference information entered per assignment, Transaction Dimensions and
    their codes.

5.  Click Collapse to display only assignments and reference information entered
    per assignment for the distribution account.

6.  You also can view all information entered for each assignment or just
    reference information that may exist. The plus or minus buttons available
    next to each assignment allow you to view all analysis information entered
    for an assignment or only reference information that may exist.

**Chapter 12: Cashbook Bank Management Transactions**

>   You can enter and view analysis information for payments, deposits, bank
>   transfers, and cash receipts entered in Cashbook Bank Management. You can
>   create assignments and enter transaction dimension codes for accounts that
>   are linked to an account class.

>   This information is divided into the following sections:

-   *Entering analysis information for payments and deposits*

-   *Entering analysis information for bank transfers*

-   *Entering analysis information for bank transfer charges*

-   *Entering analysis information for cash receipts*

-   *Entering analysis information for writeoffs, terms taken, and realized
    gain/loss*

-   *Entering analysis information for distributions*

-   *Posting transactions*

-   *Validating transactions and correcting errors*

-   *Voiding transactions*

-   *Viewing analysis information in Cashbook Bank Management*

#### Entering analysis information for payments and deposits

>   You can enter analysis information for payments and deposits that are in a
>   batch in Cashbook Bank Management. The Analytical Transaction Entry window
>   will open automatically when you TAB out from the amount field in the
>   Payments or Deposits window, if any of the accounts used in the transaction
>   distributions are linked to an account class and if analysis information has
>   not been entered for the transaction. You can also open the Analytical
>   Transaction Entry window from the Distributions window for payments and
>   deposits.

>   The Analytical Payment/Deposit Transaction Entry window will open
>   automatically if you make the following changes in the Payments or Deposits
>   window:

>   **Amount** If you change the amount, and the cheque or deposit contains only
>   one transaction, the analysis information created earlier for the payment or
>   receipt will be deleted. When you open the Analytical Payment/Deposit window
>   after saving the changes, it will display the first distribution created for
>   the transaction with the amount field displaying the new amount. If the
>   cheque or deposit is made up of multiple lines of receipts that have been
>   changed, the analysis information created for the line of receipt will be
>   deleted. This would include the account to which the amount is debited or
>   credited, the tax account, and the checkbook account. A single assignment
>   equal to the new debit or credit amount will be created. Transaction
>   dimensions and default transaction dimension codes specified for the account
>   class to which the checkbook account is linked, will be loaded in the
>   Analytical Payment/Deposit Transaction Entry window.

>   **Distribution account** The analysis information created for the
>   distribution account will be deleted if there is any change in the
>   distribution account.

>   **Creditor or Debtor ID** The analysis information created for the debtor or
>   creditor control account will be deleted, even if the control account has
>   not been changed. The Analytical Deposit window will display information
>   relating to the new debtor or creditor control account.

##### Changing positive amount to negative amount or negative amount

>   **to positive amount** The analysis information created for the line or
>   receipt affected by the change will be deleted. This would include the
>   account to which the amount is debited or credited, the tax account, and the
>   checkbook account. A single assignment equal to the new debit or credit
>   amount will be created. Transaction dimensions and default transaction
>   dimension codes specified for the account class to which the checkbook
>   account is linked will be displayed in the Analytical Payment/Deposit
>   Transaction Entry window.

>   **Tax amount** Analysis information entered for the tax amount will be
>   deleted if any changes are made.

>   **Tax schedule** Analysis information entered for the tax schedule will be
>   deleted if any changes are made.

>   **To enter analysis information for payments and deposits:**

1.  Open the Analytical Transaction Entry window.

>   (Transactions \>\> Financial \>\> Bank Management \>\> Batches \>\> Payments
>   button \>\> CTRL+T or Additional \>\> Analytical Transaction)

>   (Transaction \>\> Financial \>\> Bank Management \>\> Batches \>\> Deposits
>   button \>\> CTRL+T or Additional \>\> Analytical Transaction)

>   (Transaction \>\> Financial \>\> Bank Management \>\> Batches \>\>
>   Payments/Deposits button \>\> Distribution button \>\> CTRL+T or Additional
>   \>\> Analytical Transaction)

>   The information for the first distribution account that has been linked to
>   an account class is displayed when you open the window. Information relevant
>   to the account associated with the creditor, debtor or GL transaction
>   selected in the scrolling window of the Payments/Deposits window will appear
>   if the cheque comprises a single line or the deposit contains only a single
>   receipt.

>   For multiple lines or receipts, you can create analysis information for a
>   specific line or receipt displayed in the scrolling window.

1.  You can enter analysis information for the remaining accounts by selecting
    the appropriate distribution in the Distribution lookup or by entering a
    distribution number in the Distribution field.

2.  You can delete the analysis information that you have entered for a batch,
    cheque, or deposit before posting it. This will delete all data such as
    assignments, transaction dimension codes, and reference information that you
    entered for the transaction.

>   If you delete a specific row in the scrolling window of the Payment/Deposit
>   window, all analysis information entered for the transaction will be
>   deleted. In the Payment window, if you have not entered a cheque amount,
>   then a single assignment equal to the revised amount will be created. The
>   transaction dimensions and default transaction dimension codes specified for
>   the account class that the checkbook account is linked to will be displayed
>   in the Analytical Payment/Deposit Entry window.

>   If a tax schedule is deleted from an existing General Ledger payment or
>   deposit, the analysis information created for the tax account will be
>   deleted. If you delete the tax amount in the Tax Lookup window, the analysis
>   information entered will also be deleted.

1.  You can print the Analytical Accounting Edit List from the Analytical
    Transaction Entry window by choosing the printer icon button.

>   You also can print the Analytical Accounting Edit List before you post a
>   batch in the Batch Entry window by choosing the printer icon button. A
>   validation will take place when you print the edit list. If there are any
>   errors, the Analytical Error Report will be printed after the Analytical
>   Accounting Edit list. The Analytical Accounting Edit list will print the
>   payments and deposits along with the distributions, assignments, and codes.

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Entering analysis information for bank transfers

>   You can enter analysis information for bank transfers in the Analytical Bank
>   Transfer Entry window.

>   **To enter analysis information for bank transfers:**

1.  Open the Analytical Bank Transfer Entry window.  
    (Transactions \>\> Financial \>\> Bank Management \>\> Bank Transfers \>\>
    CTRL+T or Additional \>\> Analytical Transaction Entry window)  
    (Transactions \>\> Financial \>\> Bank Management \>\> Bank Transfers
    \>\>Distribution button \>\> CTRL+T or Additional \>\> Analytical
    Transaction)

>   The Analytical Bank Transfer Entry window will display information relevant
>   to the first distribution created for the transfer. If you selected a row in
>   either of the scrolling windows, or placed the cursor on any field in the
>   Bank Transfer Entry window, the Analytical Bank Transfer Entry window will
>   display the information for the first distribution created for the transfer.

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information about entering analysis information.

>   In the Bank Transfer Entry window, if a change is made to the amount, the
>   analysis information created for the account which has been affected by the
>   change will be deleted. For example, if the Transfer From amount is changed,
>   the analysis information you entered for the From Checkbook will be deleted.

>   If you delete a bank transfer, the analysis information created for the From
>   and To Checkbook Accounts and the Bank Charges Account will be deleted.

>   If you delete a row in the scrolling window, the analysis information
>   created for the transaction will also be deleted.

>   If you delete data related to bank charges in the Bank Transfer Charges
>   window, the analysis information created for the bank charges account will
>   also be deleted.

#### Entering analysis information for bank transfer charges

>   The Analytical Bank Transfer Charges window will open automatically when you
>   press TAB from the Amount field in the Bank Transfer Charges window for the
>   first time, if all the required information is entered. This will happen
>   only if any of the accounts used in the transaction are linked to an account
>   class and if analysis information has not been entered for the accounts.

>   You can open the Analytical Bank Transfer Charges window by choosing CTRL+T
>   in the Bank Transfer Charges window (Transactions \>\> Financial \>\> Bank
>   Management \>\> Bank Transfer \>\> Bank Transfers charges) to enter analysis
>   information.

>   The Analytical Bank Transfer Charges window will open automatically if a
>   change is made in the bank charges amount or bank charges account in the
>   Bank Transfer Charges window.

>   Analysis information created for a bank charges account will be deleted if
>   the amount of charges is altered in the Bank Transfer Charges window.

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Entering analysis information for cash receipts

>   You can enter analysis information for cash receipts in the Analytical Cash
>   Receipts

>   Entry window. This window will open automatically when you press TAB from
>   the Amount field in the Cash Receipts window for the first time. This will
>   happen only if any of the accounts in the transaction are linked to an
>   account class and if analysis information has not been entered for the
>   accounts.

>   You can open the Analytical Cash Receipts Entry window by choosing
>   Transactions \>\> Financial \>\> Bank Management \>\> Cash Receipts \>\>
>   CTRL+T or Additional \>\>Analytical Transaction.

>   You can also open the Analytical Cash Receipts Entry window from the

>   Distributions window for cash receipts (Transactions \>\> Financial \>\>
>   Bank Management \>\> Cash Receipts \>\> Distributions \>\> Additional \>\>
>   Analytical Transaction or CTRL+T).

>   You can use the browse button to view the other distributions and enter
>   analysis information. You also can select a distribution in the Distribution
>   Lookup or enter the distribution number in the Distribution field to view it
>   in the scrolling window.

>   The Analytical Cash Receipts Entry window will display information for the
>   account that has been linked to an account class. If more than one account
>   in the transaction has been linked to an account class, then this window
>   will display information for the first of such accounts.

>   Choose Save to save the transactions you have entered in the Analytical Cash
>   Receipts Entry window.

>   If you clear a transaction in the Cash Receipts window, the analysis
>   information entered for the transaction will be deleted.

>   If you close the Cash Receipts window without posting the transaction, the
>   analysis information entered for the transaction will also be deleted.

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Entering analysis information for writeoffs, terms taken, and realized gain/loss

>   You can enter analysis information for writeoffs, terms taken and realized
>   gain/loss if the payment or receipt has been applied. You can open the
>   Analytical Transaction Entry window from the Payment/Deposits window and
>   Cash Receipts window by choosing CTRL+T or Additional \>\> Analytical
>   Payment/Deposit Transaction Entry.

>   When a payment or receipt is applied in the Payment/Deposit window or the
>   Cash Receipts window, analysis information can be entered for accounts
>   relating to writeoffs, terms taken, and realized gain/loss if they are
>   linked to an account class.

>   When you return to the Payment window after applying a payment, a
>   verification will take place to check if any amount exists for writeoffs,
>   terms taken, or realized gain/loss or tax distributions. If it does exist,
>   and if the account to which the amount is to be debited or credited is
>   linked to an account class, the Analytical Payment Transaction Entry window
>   will open. This window will display information relating to the first of
>   such accounts in case there is more than one account.

>   Analysis information that has been entered for the creditor’s control
>   account before the terms taken, writeoffs or realized gain/loss is entered
>   will be deleted. A single assignment for the revised distribution amount
>   will be created. The transaction dimensions and default transaction
>   dimension code for the account class that the creditor control account is
>   linked to will be displayed in the Analytical Payment Transaction Entry
>   window.

>   When you return to the Deposit window after applying a receipt, a
>   verification will take place similar to payments. You can enter analysis
>   information for terms taken, writeoffs, or realized gain/loss before saving
>   the receipt.

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Entering analysis information for distributions

>   You can enter analysis information for the distributions created for
>   transactions in Cashbook Bank Management. The Analytical Accounting window
>   can be opened from the Distributions windows that open from the following
>   windows:

-   Payments Entry

-   Deposits Entry

-   Bank Transfer Entry

-   Bank Transfer Charges

-   Cash Receipts Entry

>   Refer to *Entering analysis information for General Ledger transactions* for
>   more information about entering analysis information.

#### Posting transactions

>   A validation will take place when you post transactions in the following
>   windows:

-   CBM Batch Entry

-   Bank Transfer Entry

-   Cash Receipts Entry

>   A transaction can be posted only after you close the Analytical Transaction
>   Entry window.

>   After posting transactions, the Analytical Accounting posting journal is
>   printed. If there are errors in the transactions, the Analytical Accounting
>   error list is printed.

>   If you selected to print cash receipts in the Checkbook Setup window (Cards
>   \>\> Financial \>\> Bank Management \>\> Setup \>\> Checkbooks), a
>   validation will take place when you choose Post. If you have not selected to
>   print cash receipts, a validation takes place when you choose Post. If
>   errors are found, the Analytical Accounting Validation Log window will open
>   listing the Microsoft Dynamics GP errors first and then the Analytical
>   Accounting errors.

>   When you post a bank transfer, the bank charge distributions are validated
>   first and if any errors are found, then the Analytical Accounting Validation
>   Log window will open.

#### Validating transactions and correcting errors

>   You can validate analysis information for payments in the Payments window by
>   choosing Additional \>\> Run Validation or by pressing CTRL+R. Validation
>   can only be done for a single transaction at a time.

>   You can validate analysis information for deposits by selecting a receipt
>   and choosing CTRL+R or Additional \>\> Run Validation.

>   Analysis information for bank charges can be validated when the Bank Charges
>   window is open, by choosing CTRL+R.

>   You can validate analysis information for transactions in the Cash Receipts
>   window by choosing Additional \>\> Run Validation or CTRL+R

>   Refer to *Validating transactions and correcting errors* for more
>   information about validation.

#### Voiding transactions

>   When you void a transaction in the Transaction Reconcile or Transaction
>   Inquiry windows, the analysis information entered for that transaction will
>   be reversed. For example, you void a transaction CBPay001 in the Transaction
>   Reconcile (Transactions \>\> Financial \>\> Bank Management \>\> Reconcile
>   \>\> OK) or

>   Transaction Inquiry (Inquiry \>\> Financial \>\> Bank Management \>\>
>   Transaction Inquiry) windows. This transaction will have assignments in the
>   Analytical Transaction Entry window. When you void the transaction, a
>   reverse entry will be created in Microsoft Dynamics GP and also reverse
>   assignments will be created in Analytical Accounting. The Analytical Voiding
>   posting journal will also be printed when you close the Bank Transaction
>   Inquiry window.

>   This will happen only for transactions voided in the Payment Inquiry/Void or
>   Deposit Inquiry/Void window.

#### Viewing analysis information in Cashbook Bank Management

>   You can view the analysis information that you have entered for transactions
>   in Cashbook Bank Management in the Analytical Inquiry window.

>   The Analytical Inquiry window can be opened by choosing CTRL+T or Additional
>   \>\> Analytical Transaction after zooming to a document or choosing void in
>   the Transaction Inquiry or Transaction Reconcile window.

>   You can also open the Analytical Inquiry window for cash receipts by zooming
>   on a cash receipt in the Deposit Inquiry window and choosing Additional \>\>
>   Analytical Transaction.

>   **To view analysis information in Cashbook Bank Management:**

1.  Open the Analytical Inquiry window.

>   (Inquiry \>\> Financial \>\> Bank Management \>\> Transaction Inquiry \>\>
>   Void \>\> CTRL+T)

1.  The Analytical Inquiry window will display analysis information for the
    first distribution created for the transaction. Choose the browse button to
    view the remaining distributions or click the Distribution lookup. You can
    also view the other distributions by entering the number in the Distribution
    field. To view the analysis information for a particular receipt, you can
    select the receipt in the Deposit window and then open the Analytical
    Inquiry window.

2.  If you are viewing a bank transfer, the Transfer From and Transfer to
    Checkbooks will be displayed. The bank transfer number relevant to the
    transaction that you are viewing will also be displayed. If you are viewing
    bank transfer charges, the bank transfer number, checkbook ID and charge
    number will be displayed.

3.  If you are viewing a cash receipt, the receipt number will be displayed.

4.  If a deposit contains multiple lines of receipts, you can view analysis
    information for a specific line of receipt. If the cursor is on a specific
    transaction in the Deposit Inquiry window, then information for the account
    associated with the debtor or creditor or the General Ledger transaction
    will be displayed.

5.  The Analytical Inquiry window will display the analysis information for a
    distribution account in detail, when opened initially. The amount assigned
    in value and percentage terms, the transaction dimensions, transaction
    dimension codes and reference information will also be displayed.

**Chapter 13: Electronic Bank Management.**

>   You can enter and view analysis information for bank transactions, bank
>   transfers, writeoffs, and terms taken transactions entered in Electronic
>   Bank Management.

>   This information is divided into the following sections:

-   *Entering analysis information for bank transactions*

-   *Entering analysis information for matched transactions*

-   *Entering analysis information for writeoffs and terms taken*

-   *Entering analysis information for distributions*

-   *Entering analysis information for bank transfers*

-   *Posting transactions*

-   *Viewing analysis information in Electronic Bank Management*

#### Entering analysis information for bank transactions

>   You can create assignments, enter transaction dimension codes, and reference
>   information for bank transactions, if any of the accounts used in the
>   transaction are linked to an account class, in the Analytical Bank
>   Transaction Entry window.

>   The Analytical Bank Transaction Entry window will open automatically the
>   first time when you save the transaction amount in the Bank Transaction
>   Entry window and also in the following instances:

-   A new transaction is being created.

-   The account/s associated with the transaction are linked to an account
    class.

-   Analysis information has not been created for such accounts.

-   All required fields have been filled in the Bank Transaction Entry window.

>   The Analytical Bank Transaction Entry window will open automatically if you
>   make the following changes in the Bank Transaction Entry window:

-   Change in the amount (in case of unmatched transactions).

-   Change in distribution account (in case of General Ledger payments and
    receipts).

-   Selecting a General Ledger distribution account after a matched General
    Ledger transaction is unmatched.

-   Change in Debtor or Creditor ID (in case of unmatched Payables Management
    and Receivables Management payments/receipts).

-   Change in tax schedule (in case of unmatched General Ledger payments and
    receipts).

-   Change in tax amount in the Tax Lookup window (in case of unmatched General
    Ledger payments and receipts).

>   In all these instances, the analysis information created for the original
>   entry will be deleted.

>   The Analytical Accounting Transaction window will not open if the
>   transaction amount is zero in the Bank Transaction Entry window, even if the
>   accounts associated with the transaction are linked to an account class, as
>   no distributions would be created.

If you delete a transaction with analysis information in the Bank Transaction
Entry window, all the analysis information for the relevant transaction will
also be deleted.

If you delete a tax schedule or alter the tax amount for a transaction with
analysis information in the Bank Transaction Entry window, the analysis
information for the tax accounts and the checkbook account will be deleted and a
single assignment equal to the revised amount will be created.

**To enter analysis information for bank transactions:**

1.  Open the Analytical Bank Transaction Entry window.  
    (Transactions \>\> Financial \>\> Bank Management \>\> Reconciliation \>\>
    Select Statement \>\> Transactions \>\> CTRL+T or Additional \>\> Analytical
    Transaction)

>   The Analytical Bank Transaction Entry window displays information for the
>   first distribution account that has been linked to an account class. To view
>   other distributions, enter or select a distribution number. You can also use
>   the browse buttons to view the required distribution.

>   In the case of multicurrency transactions, the window will display the
>   transaction amount of the account displayed, and the assignments created for
>   the account in the originating currency.

1.  Refer to *Entering analysis information for General Ledger transactions* for
    more information about entering analysis information.

2.  Choose Save to save the information you have entered.

>   You can validate individual transactions with analysis information in the
>   Bank Transaction Entry window by selecting a transaction and choosing
>   CTRL+R. You can validate all the transactions with analysis information by
>   choosing CTRL+R or Additional \>\> Run Validation. If no errors are detected
>   during the validation process, the reconciliation is posted and the
>   Analytical Accounting Posting Journal is printed. If errors are detected,
>   the Analytical Validation Log is printed. Refer to *Validating transactions
>   and correcting errors* for more information.

#### Entering analysis information for matched transactions

>   When you match transactions in the Match Transactions window (Transactions
>   \>\> Financial \>\> Bank Management \>\> Reconciliation \>\> Transactions
>   \>\> Match Trans), and choose OK, the Analytical Bank Transaction Entry
>   window will open. The window will open only if the holding account is linked
>   to an account class, and if the transaction has been fully matched.

>   The transaction dimensions and any existing default transaction dimension
>   codes relevant to the holding account will be displayed.

>   Analysis information created for any account other than the checkbook
>   account in the Bank Transactions window, that is not related to
>   distributions created after matching transactions, is deleted when you close
>   the Match Transactions window. Analysis information created for tax accounts
>   in the Tax Lookup window will also be deleted.

>   You can view the analysis information created for a matched transaction
>   before it is posted, in the Analytical Bank Transaction Entry window.

>   When you unmatch a matched transaction before posting the reconciliation,
>   analysis information for the transaction apart from the analysis information
>   for the checkbook account will be deleted on closing the Match Transaction
>   window.

>   Analysis information for transactions that have been partially matched will
>   be deleted. The information will only be deleted if the transaction is fully
>   matched, or the transaction or tax amount is deleted or if the distribution
>   or tax account is no longer linked to an account class.

>   If the holding account of the matched transactions is linked to an account
>   class, and Auto Match is completed successfully, a message will appear that
>   analysis information needs to be entered for the matched transactions. Refer
>   to *Entering analysis information for bank transactions* for more
>   information about entering analysis information. Analysis information that
>   was created for transactions before Auto Match was run will be deleted after
>   Auto Match is completed.

#### Entering analysis information for writeoffs and terms taken

>   If you apply a payment or receipt in the Bank Transaction Entry window, then
>   analysis information must be created for accounts linked to an account
>   class, for writeoffs and terms taken.

**P A R T 2** T R A N S A C T I O N S

Analysis information will be created for writeoffs and terms taken when you
close the Apply Payables/Sales documents window if any amount is entered, and if
the accounts are linked to an account class.

Analysis information that exists for debtor/creditor control account before
entering terms taken or writeoffs, will be deleted. A single assignment equal to
the new distribution amount is created. The window will display the transaction
dimensions and default transaction dimension codes for the account class that
the creditor/ debtor control account is linked to.

#### Entering analysis information for distributions

You can enter analysis information for distributions in Electronic Bank
Management. The Analytical Transaction Entry window will open from the
Distributions windows that open from the following windows:

-   Bank Transactions Entry

-   Bank Transfers

You can press CTRL+T or choose Additional \>\> Analytical Transaction to open
the Analytical Transaction Entry window. The window will only open if the
account selected in the Distributions window is linked to an account class.

Refer to *Entering analysis information for bank transactions* for more
information about entering analysis information.

#### Entering analysis information for bank transfers

You can enter analysis information for bank transfers if the accounts are linked
to an account class, using the Analytical Bank Transfer Entry window. You can
open the Analytical Bank Transfer Entry window by selecting an account in the
scrolling window or placing the cursor on any field in the Bank Transfer Entry
window (Transactions \>\> Financial \>\> Bank Management \>\> Bank Transfers)
and pressing

CTRL+T or by choosing Additional \>\> Analytical Transaction. The Analytical
Bank Transfer Entry window will display the first distribution account of the
transaction that is linked to an account class.

>   In the case of multicurrency transactions, the window will display the
>   transaction amount of the account displayed, and the assignments created for
>   the account in the originating currency.

Refer to *Entering analysis information for bank transactions* for more
information.

If there is a change in the amount of the bank transfer, the analysis
information that exists for the account related to the transfer will be deleted.
You must enter analysis information again for the transfer before it is posted.

You can the validate analysis information that you have created for bank
transfers choosing CTRL+R or Additional \>\> Run Validation. If errors are found
during the validation process, the Analytical Error window opens, displaying the
error. Refer to *Validating transactions and correcting errors* for more
information about validation.

#### Posting transactions

>   When you post a reconciliation from the Select Statement window
>   (Transactions \>\> Financial \>\> Bank Management \>\> Reconciliation),
>   analysis information created for transactions in the Bank Transaction Entry
>   window is validated. If no errors are detected during the validation
>   process, the reconciliation is posted and the Analytical Accounting Posting
>   Journal is printed. If errors are detected, the Analytical Error Report is
>   printed after the Analytical Accounting Edit List. The reconciliation can be
>   posted only if no errors are found during the validation process.

#### Viewing analysis information in Electronic Bank Management

>   You can view analysis information created for bank transactions and bank
>   transfers in the Analytical Inquiry window. The window can be opened from
>   the Transaction Inquiry window only if you have selected a specific
>   transaction.

>   **To view analysis information for bank transactions and bank transfers:**

1.  Open the Analytical Bank Transfer Enquiry window.  
    (Inquiry \>\> Financial \>\> Bank Management \>\> Reconcile Inquiry \>\>
    Transaction Inquiry \>\> CTRL+ T or Additional \>\> Analytical Transaction)  
    (Inquiry \>\> Financial \>\> Bank Management \>\> Bank Transfers \>\> CTRL+
    T or Additional \>\> Analytical Transaction)

2.  The Analytical Inquiry window displays the analysis information related to
    the first distribution account of the transaction that has been linked to an
    account class. If you selected a matched transaction in the Transaction
    Inquiry window, the analysis information would related to the holding
    account and/or checkbook account if it is linked to an account class.

3.  The analysis information for a distribution account is displayed in detail.
    This includes the amount assigned in value and percentage terms, transaction
    dimensions, transaction dimension codes and reference information.

198 A N A L Y T I C A L A C C O U N T I N G

**Chapter 14: Direct Debits And Refunds Transactions**

>   You can create analysis information for direct debits and direct debit
>   refunds, when you process Direct Debits and Refunds transactions. This
>   information is only for default transaction dimension codes that are
>   assigned to Required, Fixed and Optional Transaction Dimensions of the
>   account class that the transaction distribution accounts used in processing
>   are linked to. For the transaction distributions that are created on
>   processing, a single assignment equal to the distribution amount is created
>   by default. The analysis information will be created during processing and
>   you can modify default information in General Ledger.

>   In Direct Debits and Refunds, there will be no validation of analysis
>   information. However, you will not be able to post a batch that originates
>   from Direct Debit and Refunds from General Ledger if there are errors in the
>   default analysis information, such as a transaction dimension code has not
>   been specified for a Required transaction dimension. This batch will not
>   update posting accounts from General Ledger until you enter a code for the
>   transaction dimension.

>   This information is divided into the following sections:

-   *Analysis information for direct debits and refunds*

-   *Posting through to General Ledger for transaction posting*

-   *Viewing analysis information for direct debits and refunds*

#### Analysis information for direct debits and refunds

>   In the Select Direct Debits window (Transactions \>\> Sales \>\> Select
>   Direct Debits), when you select a batch for direct debit and refunds and
>   choose Process, the payments and debit memos are created and default
>   transaction dimension codes loaded and assignments created for distribution
>   accounts that are linked to an account class.

>   You can create multiple assignments or modify/enter transaction dimension
>   codes for the distribution accounts linked to an account class in General
>   Ledger after processing. Refer *Entering analysis information for General
>   Ledger transactions* for more information.

#### Posting through to General Ledger for transaction posting

>   For Direct Debits and Refunds, the option Post through General Ledger files
>   under Posting Setup (Administration \>\> Setup \>\> Posting \>\> Posting) is
>   unavailable. Transactions posted from Direct Debits and Refunds must be
>   posted from General Ledger.

#### Viewing analysis information for direct debits and refunds

You can view default Transaction Dimension codes and assignments of transaction
distribution accounts created after processing direct debits and refunds from
the Sales Distribution Inquiry Zoom window.

(Inquiry \>\> Sales \>\> Transaction by Customer or Transaction by Document \>\>
Select a receivables document \>\> Document Number link)

Refer *Viewing analysis information in Receivables Management* for more
information about viewing analysis information.

**Chapter 15: Analysis information for U.S. Payroll transactions**

>   You can enter and view analysis information for transactions entered in the
>   U.S. Payroll series. You can create assignments and enter transaction
>   dimensions and codes by assigning a default alias to each employee. The
>   default transaction dimension codes associated with the alias is displayed
>   for U.S. Payroll transactions. You also can assign a default alias to
>   display transaction dimension information associated with the alias for a
>   batch of U.S. Payroll transactions in the Mass Payroll Transactions Entry
>   window. You can modify the analysis information before posting the
>   transactions. Multilevel query and distribution queries can be used to view
>   analysis information for the employees.

>   This information is divided into the following sections:

-   *Understanding analysis information for payroll transactions*

-   *Defining default dimensions for payroll transactions*

-   *Entering analysis information for payroll transactions*

-   *Viewing analysis information for payroll transactions*

#### Understanding analysis information for payroll transactions

>   You can enter and view analysis information for payroll transactions if you
>   have registered Payroll in the Registration window (Administration \>\>
>   Setup \>\> System

>   \>\> Registration), and enabled transaction dimensions for payroll in the
>   Analytical Accounting Options window. Be sure to mark the Post in Detail
>   option for the Payroll series in the Posting Setup window. Refer to *Setting
>   up posting options for Analytical Accounting* for more information.

>   With Analytical Accounting for Payroll, you can:

-   Assign an alias to a combination of posting type, employee, department,
    position, and code in the Analytical Payroll Default Dimensions window.

-   View and modify the default analysis information for a payroll transaction
    before posting.

-   View the assignments in percentage or hours for transactions other than
    overhead transactions. In the case of overhead transactions, you can view
    this information in General Ledger.

-   Create and run queries using the Distribution Query wizard and the
    Multilevel Query wizard to view analysis information for selected employees.

#### Defining default dimensions for payroll transactions

>   You can assign an Analytical Accounting alias to a combination of posting
>   type, employee, department, position and code for the default dimension in
>   the Analytical Payroll Default Dimensions window. The default transaction
>   dimension codes associated with the alias is displayed when you enter a
>   transaction for the specific combination.

>   **To define default dimensions for payroll transactions:**

1.  Open the Analytical Payroll Default Dimensions window.  
    (Administration \>\> Setup \>\> Posting \>\> Payroll Accounts \>\>
    Analytical Accounting button)  
    (Administration \>\> Setup \>\> Posting \>\> Payroll Accounts \>\>
    Additional \>\>Payroll Defaults)  
    (Administration \>\> Setup \>\> Posting \>\> Analytical Accounting Default
    Dimensions button)  
      
    IMAGE – AAPR.jpg

![](media/8ddcef4c4dc549199c07d8e7c1112a2f.jpg)

>   A screenshot of a computer Description automatically generated

1.  Select a payroll posting account type in the Payroll Posting Type field. The
    posting types available in the U.S. Payroll module are available for
    selection. Refer to U.S. Payroll documentation for more information.

2.  Select the employee ID.

3.  Select the department code in the Department field.

4.  Select the position code in the Position field.

5.  Select the pay code in the Code field.

6.  Select an alias in the Alias field as the default alias for the employee ID
    and payroll combination defined in this window.

7.  Enter a percentage for the alias in the Percentage field. You can enter a
    percentage value between 0 to 100%.

8.  Choose OK to save the information and close the window.

#### Entering analysis information for payroll transactions

>   You can enter or modify analysis information assigned to U.S. payroll
>   transactions.

-   For manual checks, as well as for Pay Code type of computer checks, you can
    view and change the default analysis information during transaction entry.

-   For Deduction and Benefit type of computer checks, you can edit the default
    analysis information only after you have performed the Calculate Checks
    process.

-   In the Payroll Mass Transaction Entry window, you can enter an alias to
    assign default analytical information to a selected range within a payroll
    batch.

>   **To enter analysis information for payroll transactions:**

1.  Open the Analytical Payroll Transaction Entry window.  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Analytical Accounting
    button)  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Additional \>\>
    Analytical Transaction)  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Ctrl + T)  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Select a transaction
    in the scrolling window \>\> Analytical Accounting button)  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Select a transaction
    in the scrolling window \>\> Dimensions Button)  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Select a transaction
    in the scrolling window \>\> Additional \>\> Analytical Transaction)  
    (Transactions \>\> Payroll \>\> Transaction Entry \>\> Select a transaction
    in the scrolling window \>\> Ctrl + T)  
    (Transactions \>\> Payroll \>\> Manual Check \>\> Distributions Button
    \>\>Analytical Accounting Button)  
    (Transactions \>\> Payroll \>\> Payroll Posting Edits \>\> Analytical
    Accounting Button)

>   IMAGE – AAPRT.jpg

![](media/aaaa96c29f019c4bec396ab702f5c947.jpg)

>   A screenshot of a computer Description automatically generated

1.  The Distribution field displays the distribution account selected in the
    Payroll Transaction Entry window. To view other distributions for the
    transaction, enter or select a distribution number. The field name depends
    upon the path from which you open this window.

>   The sequence of distributions in the Analytical Payroll Transaction Entry
>   window may not correspond to the sequence in the Payroll Transaction Entry
>   window because only accounts linked to an account class are displayed in the
>   Analytical Payroll Transaction Entry window.

>   **Functional Amount** Displays the distribution amount in the functional
>   currency.

>   **Assigned** Displays distribution amount, hours or units based on the pay
>   type associated with the code.

>   **Unassigned** Displays the remaining distribution amount that is to be
>   assigned in value and percentage.

>   **Account** The Account field displays the account related to the
>   distribution. The expansion button will open the Microsoft Dynamics GP
>   Account Entry window. The account description is also displayed.

>   The Employee, Department, Position, Code and Posting Type fields display the
>   employee ID, department, position, pay code and the payroll posting type for
>   the distribution.

1.  Select Hours/Units or the Percentage as the assignment type to assign values
    to the distribution amount.

>   **Hours/Units** This option is automatically selected and available for pay
>   types that are calculated on hourly or unit basis. If this option is marked,
>   you can enter the Analytical Accounting distributions based on hours/units.

>   **Percentage** Select this option to enter the Analytical Accounting
>   distributions based on percentages. This option is automatically selected
>   for pay types other than hours or units.

>   *If the option hours/units is selected automatically for a distribution and
>   you change the default assignment type to percentage, an assignment of 100%
>   is created based on your setups in the linked accounts class.*

>   In the assignment list view, an arrow in the Number field indicates that the
>   analysis information displayed is for the selected assignment. Each
>   assignment created for the distribution is displayed separately.

1.  In the list window, enter the hours or units by value or by percentage
    depending on the assignment type selected.

>   **Number** Displays the assignment number.

>   **Hours/Units** Displays the hours or units for the selected assignment
>   based on the default percentage set up in the Analytical Payroll Default
>   Dimensions window. You can modify this information if required.

>   **Assign%** Displays the percentage based on your selections in the
>   Analytical Payroll Default Dimensions window. You can modify the assignment
>   percentage if required.

>   You can save analysis information for a distribution even if the assignment
>   is not 100%. However, you can post a transaction with partial assignments
>   only if you have opted to allow partial assignments during posting for the
>   Payroll module. Refer to *Setting up assignment options* for more
>   information.

>   **Alias** Displays the alias for each assignment based on the default alias
>   defined in the Analytical Payroll Default Dimensions window. You can select
>   a different alias if required.

1.  Enter the reference information for the assignment in the Reference field.

>   The Trx Dimension column displays transaction dimensions of the account
>   class that the distribution account is linked to. Only transaction
>   dimensions that have been set as Required, Fixed, or Optional are displayed.

>   The Alphanumeric column displays the dimension codes assigned to the
>   corresponding transaction dimension in the Alias Maintenance window and to
>   the transaction dimensions of the account class of the distribution account
>   in the Accounting Class Maintenance window.

1.  Enter a transaction dimension code in the Numeric, Yes/No or Date field for
    a Numeric, Boolean or Date type Transaction Dimension.

2.  Choose Delete Row to delete a single row in the assignment List View. You
    cannot choose this option if only a single assignment has been entered.

3.  Choose Remaining to add one assignment for the remaining unassigned amount.
    The new assignment will ensure that the total assigned amount equals the
    distribution amount. For example, if the distribution amount is \$100 and
    you have entered four assignments that total \$75. When you choose
    Remaining, a fifth assignment for the remaining value, \$25 is created. This
    button is not available if the distribution field is blank or has a zero
    value or if the distribution amount is fully assigned.

4.  Choose Default to load the current setup information specified for the
    account class in the Accounting Class Maintenance window and create a single
    assignment. The following processes will occur:

    -   Fixed, Required, and Optional Transaction Dimensions (including hidden
        transaction dimensions) will be installed.

    -   All the assignments that you have created for the current distribution
        will be removed and create a single assignment that is equal to the
        distribution amount will be created.

    -   If the analysis type is changed to or from Not Allowed, transaction
        dimensions will be added or removed.

    -   Transaction dimensions that have been deleted will be removed.

5.  Choose OK to save your changes and close the window. The analysis
    information that you have entered is validated when you choose OK.

6.  Choose Validate to validate the analysis information of the distribution
    displayed in the window. If changes are made to the account class in the
    Analytical Accounting setup or errors are found during the validation
    process, the Analytical Accounting Validation Log window will open where you
    can view the errors or changes. Refer to *Validating transactions and
    correcting errors* for more information about validation.

>   Choose Print to print the error report. Choose OK to close the window and
>   return to the Analytical Payroll Transaction Entry window.

1.  Choose Clear to clear the values displayed in the Analytical Payroll
    Transaction Entry window.

2.  Choose Validate to validate the analysis information of the distribution
    displayed in the window. If changes are made to the account class in the
    Analytical Accounting setup or errors are found during the validation
    process, the Analytical Accounting Validation Log window will open where you
    can view the errors or changes. Refer to *Validating transactions and
    correcting errors* for more information about validation.

3.  Choose Save to save the default or modified analysis information you have
    entered.

4.  Choose the printer icon button to print the Analytical Accounting edit list
    for the current distribution displayed or for all distributions of the
    transaction linked to an account class. The Analytical Accounting Validation
    Log report which describes the Analytical Accounting errors also is printed.

#### Viewing analysis information for payroll transactions

>   You can use the Analytical Payroll Transaction Entry Zoom window to view
>   analysis information for payroll transactions generated from the U.S.
>   Payroll module.

>   **To view analysis information for payroll transactions:**

1.  Open the Analytical Payroll Transaction Entry Zoom window.  
    (Inquiry \>\> Payroll \>\> Check History \>\> Distributions button \>\>
    Select a distribution account \>\> Analytical Accounting button)  
    (Inquiry \>\> Payroll \>\> Check History \>\> Select a transaction \>\>
    Additional \>\>Analytical Transaction)  
      
    IMAGE – AAPRI.jpg

![](media/1ba894bb2b5e18ed65172a6533e7bf7e.jpg)

>   A screenshot of a computer Description automatically generated

>   The Analytical Payroll Transaction Entry Zoom window displays all analysis
>   information created for a distribution account. The first distribution
>   account of the document linked to an account class is displayed. Enter or
>   select a distribution number to view analysis information for other
>   distribution accounts.

1.  Choose the plus button (+) available next to each assignment to view all
    analysis information entered for an assignment or choose the minus button
    (-) to view only reference information that may exist.

2.  Choose OK to close the window after viewing the information required.

**Part 3: Routines, Inquiries and Reports**

>   You can make queries and generate reports within Analytical Accounting that
>   will help you analyze your company’s chart of accounts in detail. Use the
>   Analytical Accounting query wizard windows to create and run queries that
>   are based on your analysis requirements.

>   You can also compare the allocated amounts with the actual figures to
>   analyze how the budgeted amounts are being used. The Multilevel Query wizard
>   allows you to generate reports on the budgets.

>   The following information is discussed:

-   *Chapter 16, “Year-end close for Analytical Accounting”*explains how
    analytical information is transferred to history and how balances are
    consolidated and brought forward during the year-end close process.

-   *Chapter 17, “Inquiries”*explains how to create, modify, and print
    Analytical Accounting queries.

-   *Chapter 18, “Reports”*shows you how to use Analytical Accounting reports to
    view your analysis information.

**Chapter 16: Year-end close for Analytical Accounting**

>   This information is divided into the following sections:

-   *Including Analytical Accounting in the year-end close process*

-   *Closing a year with analysis information*

-   *Consolidating analysis information and carrying balances forward*

-   *Transferring analysis information for closed years to history*

#### Including Analytical Accounting in the year-end close process

>   If you’ve included Analytical Accounting in the year-end close process,
>   closing the year transfers the current year analytical data for each account
>   to account and transaction history (if you’re keeping history records).
>   Analytical data for alphanumeric transaction dimensions is consolidated and
>   the balance is carried forward to the next year.

>   To include Analytical Accounting information in the year-end closing
>   process, you must:

-   Mark the Include in Year End Close option in the Analytical Accounting
    Options window. Refer to *Setting up Analytical Accounting options*. Mark
    the Include in Year End Close checkbox in the Transaction Dimension
    Maintenance window for the alphanumeric transaction dimensions that you want
    to consolidate balances for in the year-end close process. Refer to
    *Defining transaction dimensions*. Balances are brought forward only for the
    selected transaction dimensions.

-   If you have previously closed years in Microsoft Dynamics GP, transfer the
    analytical data for those years to history and carry forward the
    consolidated balances before you close the current year. Not doing so will
    lead to incorrect brought forward balances. Refer to *Transferring analysis
    information for closed years to history*.

>   *Do not post adjustments to a closed year after you have marked to include
>   analysis data in the year-end close process, and before you have run the
>   Transfer transaction Data to History utility. Doing so will result in
>   incorrect brought forward balances.*

**Closing a year with analysis information**

>   When you close a year with analytical information, the year-end closing
>   process:

-   Transfers all current year analytical data for each account to account and
    transaction history (if you’re keeping history records). The analytical data
    is transferred to history for all transaction dimensions, whether or not
    you’ve marked to consolidate them during the year-end close.

-   Consolidates analytical information related to the marked alphanumeric
    transaction dimensions for open year profit and loss accounts and transfers
    it to the Retained Earnings account.

>   *Balance brought forward transactions are created for the retained earnings
>   account even if no profit and loss distributions exist in the fiscal year
>   that the year-end close is being run for. This ensures that your analytical
>   data is accurate if you have directly entered the net value to the retained
>   earnings account as part of a single balanced beginning balance transaction
>   when installing Microsoft Dynamics GP.*

-   Consolidates analytical information related to the marked alphanumeric
    transaction dimensions for balance sheet accounts, bringing the balances
    forward as the accounts’ beginning balances in the new fiscal year.

>   Refer to *Consolidating analysis information and carrying balances forward*
>   for more information.

-   Zeroes the analytical balance for all profit and loss accounts after they’ve
    been closed to the Retained Earnings account.

>   *If you enter adjustments to a profit and loss account after closing a year,
>   the analytical information for the adjustment is automatically updated to
>   the corresponding retained earnings account. You won’t need to do anything
>   following the adjustments.*

-   Brings the balances of unit account forward to the new fiscal year.

-   Prints the Analytical Accounting Year-End Closing Report.

>   Refer to the Microsoft Dynamics GP documentation for more information on the
>   year-end closing process.

#### Consolidating analysis information and carrying balances forward

>   When you run the year-end close process, the analytical data for
>   alphanumeric transaction dimensions is consolidated and carried forward to
>   the next year. The consolidation is performed only for those transaction
>   dimensions that you’ve marked to include in the year-end process. Refer to
>   *Including Analytical Accounting in the year-end close process*.

>   In the balance brought forward journal:

-   One assignment is created for each unique combination of account,
    alphanumeric transaction dimensions, and codes in the case of balance sheet
    accounts.

-   One assignment is created for each unique combination of alphanumeric
    transaction dimensions and codes across all profit and loss accounts.

-   If amounts without any analytical information exist, then a single
    assignment is created for the total unassigned amount with no alphanumeric
    transaction dimension codes assigned to it.

-   The total of all assignments for a balance sheet account represents the
    General Ledger distribution amount or the brought forward balance for the
    account.

>   • The total of all assignments for the profit and loss accounts is carried
>   forward to the Retained Earnings account.

>   **Example**

>   Account 1011 which is a balance sheet account for customer A is assigned to
>   an accounting class. The following alphanumeric transaction dimensions and
>   codes are created with a valid relationship to one another.

| **Dimensions** | **Codes**  |
|----------------|------------|
| Project        | PRJ1, PRJ2 |
| Product        | PDT1, PDT2 |
| Location       | LOC1, LOC2 |

>   **Scenario 1**

>   Partial assignments are not allowed. Transaction dimension codes are
>   optional and the following transactions are posted for the account 1011
>   during the year.

| **Dr.** | **Cr.** | **Location Code** | **Product Code** | **Project Code** |
|---------|---------|-------------------|------------------|------------------|
| 250000  | \-      | LOC 1             | PDT 1            | PRJ 1            |
| 150000  | \-      | LOC 2             | \----            | PRJ 1            |
| 100000  | \-      | LOC 1             | PDT 2            | PRJ 1            |
| \-      | 10000   | LOC 1             | PDT 2            | PRJ 1            |

>   On performing the year-end close, one assignment is created with the
>   consolidated amount for each unique combination of transaction dimension
>   codes.

|                   | **Account**            | **Dr.** | **Cr.** |
|-------------------|------------------------|---------|---------|
| **Journal Entry** | **Account 1011**       | 490000  | \-      |
| Assignment 1      | LOC 1 - PDT 1 - PRJ 1  | 250000  | \-      |
| Assignment 2      | LOC 2 - ------ - PRJ 1 | 150000  | \-      |
| Assignment 3      | LOC 1 - PDT 2 - PRJ 1  | 90000   | \-      |

>   **Scenario 2**

>   Partial assignments also are allowed. Transaction dimension codes are
>   optional and the following transactions are posted for the account 1011
>   during the year.

| **Dr.**  | **Cr.** | **Assignment%** | **Assignment Amount** | **Location Code**                                     | **Product Code** | **Project Code** |
|----------|---------|-----------------|-----------------------|-------------------------------------------------------|------------------|------------------|
| 250000 - |         | 40%             | 100000                | LOC 1                                                 | PDT 1            | PRJ 1            |
|          |         | 60%             | 150000                | Partially unassigned, no codes entered for 60% amount |                  |                  |
| 150000 - |         | 75%             | 112500                | LOC 2                                                 | \---             | PRJ 1            |
|          |         | 25%             | 37500                 | Partially unassigned, no codes entered for 25% amount |                  |                  |
| 100000   |         | 100%            | 100000                | LOC 1                                                 | PDT 1            | PRJ 1            |
| \-       | 10000   | 100%            | 10000                 | Default 100% assignment, no codes entered             |                  |                  |

>   On performing the year-end close, one assignment is created with the
>   consolidated amount for each unique combination of transaction dimension
>   codes. One assignment also is created for the amount to which no codes are
>   assigned.

|                   | **Account**           | **Dr.** | **Cr.** |
|-------------------|-----------------------|---------|---------|
| **Journal Entry** | **Account 1011**      | 490000  | \-      |
|                   | **Account**           | **Dr.** | **Cr.** |
| Assignment 1      | LOC 1 - PDT 1 - PRJ 1 | 200000  | \-      |
| Assignment 2      | LOC 2 - ----- - PRJ 1 | 112500  | \-      |
| Assignment 3      | \--- - --- - ---      | 177500  |         |

#### Transferring analysis information for closed years to history

>   If you have previously closed years in Microsoft Dynamics GP, you must
>   transfer the analytical data for those years to history before you close the
>   current year. You also can consolidate and bring forward the closing balance
>   as the next year’s opening balance. This also will transfer the balances for
>   any adjustments you posted to a closed year. You must run this process
>   sequentially starting from the first closed year up to the most recently
>   closed year.

>   *You must perform this process before you close an open year or post an
>   adjustment to a closed year. Not doing so will result in incorrect balances
>   being brought forward.*

>   **To transfer analysis information for closed years to history:**

1.  Open the Transfer Transaction Data to History window.  
    (Administration \>\> Utilities \>\> Financial \>\> Analytical Accounting
    \>\> Move Data to History)

2.  The Year field displays the earliest closed year for the company in
    Microsoft Dynamics GP.

3.  Select an action to perform.

>   **Transfer transaction detail to history** Select this option to transfer
>   all the analysis information for the selected closed year to history.

>   **Consolidate transactions and transfer detail to history** Select this
>   option to consolidate transactions in the closed year based on the
>   combination of alphanumeric transaction dimensions that are marked to
>   include in the yearend close process. The analysis information for the
>   selected year is moved to history and the closing balances are brought
>   forward to the next year. Refer to *Consolidating analysis information and
>   carrying balances forward*.

>   **Print transfer preview report only** Select this option to print a preview
>   report before performing the transfer and consolidation.

1.  Choose OK to process the selected option.

2.  Choose Cancel to cancel the process and close the window.

**Chapter 17: Inquiries**

>   The inquiries available in Analytical Accounting Inquiry allow you to view
>   transaction dimension relationships and budgeted vs. actual figures. You can
>   create distribution queries to view analysis codes for every assignment, and
>   create multilevel queries to view analysis code information in the form of
>   trees and levels. You can define queries and save them or print the queries
>   without saving. The queries export data to an Excel worksheet.

*You must be using Excel 2000 or higher to export Analytical Accounting queries
to Excel.*

>   Before you start generating a query, be sure that the functional currency
>   you’re using has a negative sign before the amount. You can select this
>   option in the Currency Setup window (Administration \>\> Setup \>\> System
>   \>\> Currency).

>   The query output to Excel must be limited to 256 columns.

*You cannot run more than one query at a time on the same system.*

>   This information is divided into the following sections:

-   *Viewing transaction dimension relationships*

-   *Viewing budgeted versus actual values*

-   *Creating and running a distribution query*

-   *Defining a distribution query*

-   *Selecting columns for a distribution query*

-   *Setting filter options for a distribution query*

-   *Setting the order of data for a distribution query*

-   *Completing distribution query options*

-   *Creating and running a multilevel query*

-   *Including brought forward balances in a multilevel query*

-   *Defining a multilevel query*

-   *Selecting rows for a multilevel query*

-   *Selecting column spreads for a multilevel query*

-   *Selecting trees for a multilevel query*

-   *Setting filter options for a multilevel query*

-   *Selecting columns for a multilevel query* • *Completing the multilevel
    query options*

#### Viewing transaction dimension relationships

>   You can view all the existing transaction dimensions and their relationship
>   to other transaction dimensions in the Transaction Dimension Dependency
>   (Relation) Inquiry window.

>   **To view a transaction dimension relationship:**

1.  Open the Transaction Dimension Dependency (Relation) Inquiry window.  
    (Inquiry \>\> Financial \>\> Analytical Accounting \>\> Transaction
    Dimension Relation)  
    (Cards \>\> Financial \>\> Analytical Accounting \>\> Transaction Dimension
    Relation \>\> Show as Tree button)  
      
    The tree structure displays the relationship of ownership between
    alphanumeric transaction dimensions. For example, Cost Centre is owned by
    Profit Centre, as indicated in the tree structure.

2.  Choose Redisplay to update the tree if any changes have been made to the
    transaction dimension relationships and display transaction dimensions that
    may have been created by other users while you were setting relationships.

3.  Choose OK to close the window and return to the Transaction Dimension
    Relations window.

#### Viewing budgeted versus actual values

>   Use the Analytical Accounting Budget vs. Actual Inquiry window to compare
>   budgeted and actual values. You can also view the variance and variance
>   percentage, so you can analyze how closely your actual amounts match the
>   budgeted amounts for the selected account and/or dimension code tree.

>   **To view budgeted versus actual values:**

1.  Open the Analytical Accounting Budget vs. Actual Inquiry window.  
    (Inquiry \>\> Financial \>\> Analytical Accounting \>\> Budget vs. Actual)

2.  Enter or select a budget ID. The Budget Year, Description, Budget Tree,
    Dimension Code Tree window and Period Column fields display the default
    values for the selected budget ID.

>   The root node is automatically highlighted, and the columns in the scrolling
>   window display the figures for the root node. The scrolling window displays
>   the Actual and Budgeted values, Variance and Variance Percent for each
>   period.

1.  Select whether to view information for the tree or for accounts. If you
    select Tree, you can view period amounts for the selected node. If you
    select Account, go to step 4.

2.  Mark All in the Account radio group field to view the period amounts
    assigned to all accounts on the selected node in the scrolling window.

>   Mark Select and select an account to view the period amounts for the
>   selected account for the selected node.

1.  Highlight a node in the Dimension Code Tree to view the period amounts for
    that node or node/account combination in the scrolling window. The selected
    node is displayed at the bottom of the Dimension Code Tree.

2.  Choose whether to view the amounts for the Node or the Dimension Code. If
    you select Node, you can view the period amounts for the code that you’ve
    selected under a specific node. If you select Dimension Code, you can view
    the period amounts for the selected dimension code under all nodes of the
    budget tree. Refer to Budget Tree overview for more information on nodes and
    codes.

3.  Choose how to display the budget information, Net Change or Period Balances.

4.  Select the reporting ledgers for which to view the information for and click
    the redisplay button.

>   This field is available only if you have marked the Allow check box for the

>   Reporting Ledger option in the General Ledger Setup window (Administration
>   \>\> Setup \>\> Financial \>\> General Ledger). Refer to the General Ledger
>   documentation for more information.

1.  You can print a Budget vs. Actual Inquiry Report by choosing File \>\> Print
    or clicking the printer icon button while the information you'd like to
    print is displayed.

2.  Choose Redisplay to refresh the information in the window.

3.  Close the window when you’ve finished viewing information.

#### Creating and running a distribution query

>   Use the Distribution Query wizard to create and run queries and export data
>   to Excel. You can view selected assignments and the transaction codes they
>   are attached to using the Distribution Query wizard. You can create the
>   queries, view them, and delete them, or you can save them to use again. You
>   can create and run the queries for both active and inactive transaction
>   dimension codes. You can view the posted analysis information for
>   transaction dimension codes that are subsequently set to inactive status.
>   You can select the columns to be displayed in the Excel report and select
>   the subset of assignments that have been entered.

>   You can view data for history and open years and restrict the data to half
>   year, quarter, month, week, period or a specific date range. You can also
>   view the consolidated balances that are brought forward when you close a
>   fiscal year. Refer to *Completing distribution query options* for more
>   information.

>   **To create and run a distribution query:**

1.  Open the Distribution Query wizard Welcome window.  
    (Inquiry \>\> Financial \>\> Analytical Accounting \>\> Distribution Query)

2.  Select the type of query to run.

>   **Execute Existing Query** To execute a query that has been saved earlier.
>   You also can change the definition of an existing query and save or run the
>   query.

>   Choose Next to open the Distribution Query wizard- Query Selection window,
>   where you can select an existing query and then complete the query in the
>   Distribution Query wizard-Finish window. Refer to *Completing distribution
>   query options* for more information.

**Execute Ad hoc Query** To run a query that will not be saved.

>   Choose Next to open the Distribution Query wizard-Column Selection window
>   where you can select the levels to display in the query. Refer to *Selecting
>   columns for a distribution query* for more information.

>   **Query Maintenance** To define a new query that can be saved or run. You
>   also can delete or change existing query definitions and save these changes
>   to use later.

|   |
|---|


#### Defining a distribution query

>   You can enter the name and description for a query in the Distribution Query
>   wizard - Query Maintenance window.

>   **To define a distribution query:**

1.  Refer to *Creating and running a distribution query* and select a query
    option. Choose Next and open the Distribution Query wizard- Query
    Maintenance window.

2.  Enter or select the name of the query in the Query ID field.

3.  Enter a description for the query.

4.  Choose the GoTo button to display other windows in the wizard. You can
    select a window from the list instead of choosing the Next or Back buttons
    in the wizard windows. The windows available in the list will depend on the
    current window. For example, from the Query Maintenance window, the
    following windows will be available in the drop-down list:

    -   Option selection

    -   Column selection

    -   Filter Options

    -   Order by Options

    -   Completing the options

5.  Choose Delete to delete an existing Query ID.

6.  Choose Back to return to the previous window.

7.  Choose Cancel to close the wizard without saving any information.

8.  Choose the Print drop-down list to print a Query ID that is saved. Select
    Print Current Record to print the definition for a selected query. Select
    Print All to print all the saved query definitions.

9.  Choose Next to open the Distribution Query wizard-Column Selection window
    where you can select the columns to display in the Excel report.

#### Selecting columns for a distribution query

>   You can select the columns to be displayed in the query using the
>   Distribution Query wizard- Column Selection window. You can select from the
>   33 pre-defined columns and an additional column for every dimension that you
>   create, in this window. Refer to *Modifying column headings for inquiries
>   and reports* for more information on pre-defined columns.

>   **To select columns for a distribution query**

1.  Refer to *Creating and running a distribution query*, and select a query
    option. Choose Next and open the Distribution Query wizard - Query
    Maintenance window. Select a name and description for the query and choose
    Next to open the Distribution Query wizard- Column Selection window.

2.  The Available Columns scrolling window shows the columns that can be
    displayed in the Excel Report when a query is run. Select a column and
    choose Insert to display the column in the Selected Columns list window.

3.  Choose Insert All to insert all Available Columns in the Selected Columns
    window. If you select all the available columns for your query, printing
    speed will be reduced.

4.  Choose Remove to remove a selected item from the Selected Column list.

5.  Choose Remove All to remove all the items from the Selected Columns list.

6.  Choose the Move to Top button to move a selected item to the top of the
    Selected Columns list. This column will appear first in the Excel output.

7.  Choose the Move Up button to move a selected item one line up in the
    Selected Columns list.

8.  Choose the Move Down button to move a selected item one line down in the
    Selected Columns list.

>   The order in which the columns are selected will be the order they are
>   displayed in the Excel report. For example, you’ve inserted columns in the
>   following order:

-   Header ID

-   Journal Entry

-   GL Posting Date

-   Profit Centre

>   In the Excel report, the first column displayed will be Header ID, the
>   second column will be Journal Entry and so on.

1.  Choose the Move to the Bottom button to move a selected item to the bottom
    of the Selected Columns list.

2.  Choose Back to return to the previous window.

3.  Choose Cancel to exit the wizard.

4.  Choose Next to open the Distribution Query wizard-Filter Options window
    where you can select the filter option for your query.

#### Setting filter options for a distribution query

>   You can use the Distribution Query wizard-Filter Options window to sort the
>   query and specify the information to display in the report that is
>   generated. If you do not choose filter options, all the transactions that
>   have taken place in the defined period will be selected for the query.

>   **To set filter options for a distribution query:**

1.  Refer to *Selecting columns for a distribution query*, select the column
    headings and choose Next to open the Distribution Query wizard-Filter
    Options window.

2.  The scrolling window in the Distribution Query wizard –Filter Options window
    displays all available columns.

3.  Select a column, one at a time, in the scrolling window and from the Select
    Type list, select a filter option for the column from the following:

**Any** To select all the records.

**Contains** To select only records that match the specified criteria.

**Equal To** To select records that are equal to the specified criteria.

>   **Not Equal to** Only records that do not match the specified criteria are
>   selected.

**Begins with** To select only records that begin with a specified criterion.

**Is Between** To select only records that are between a specified value.

>   **Greater than** To select only records with values that are greater than
>   the specified value.

>   **Less than** To select only records with values that are lesser than the
>   specified value.

1.  The “…” field is available for all the filter options, except for Any. You
    can enter a value in this field to further restrict your query range. For
    example, if you selected Journal Entry, you can restrict whether to display
    a range of journal entries.

2.  The And field will be available if the search type of the selected column is
    ‘Is Between’. Enter a closing range for your query. The lookup is available
    for the following columns:

    -   Currency ID

    -   Customer ID

    -   Vendor ID

    -   account

    -   Account Alias

    -   Item Number

    -   Site ID

    -   Trx Dimensions

    -   Asset Id

    -   Book ID

3.  Mark the account types to include in the query. You can mark Balance Sheet,
    Profit and Loss and/or Unit Accounts in the query. You must mark at least
    one account Type. Profit/Loss is marked by default.

>   In the Search Type list, select whether all or some of the filter options
>   must match the query criteria before a record can be displayed. If the
>   filter option for each column must match before a record is displayed,
>   select Match All. If a record can be displayed if it matches at least one of
>   your filter options, select Match 1 or More.

1.  Choose Next to open the Distribution Query wizard –Order By window where you
    can select the order to display the data when you print the query to Excel.

#### Setting the order of data for a distribution query

>   You can select the order to display data in the report you generate in the
>   Distribution Query wizard- Order by window.

>   **To set the order of data for a distribution query:**

1.  Refer *Setting filter options for a distribution query*, select the filter
    options, and choose Next to open the Distribution Query wizard-Order by
    window.

2.  The Available columns list window displays all the columns available except
    those for transaction dimensions. Select a column and choose Insert to
    insert the selection in the Order by scrolling window.

3.  The Order by column displays the order in which the columns will be
    displayed in Excel. By default, the columns are displayed in ascending
    order. You can change this to descending order by choosing the A/Z icon.

4.  Choose Remove to remove a selected item from the Order by column.

5.  Choose Remove All to remove all the items from the Order by column.

6.  Choose the Move to top button to move a selected item to the top of the
    Order by column.

7.  Choose the Move Up button to move a selected item one line up in the Order
    by column.

8.  Choose the Move Down button to move a selected item one line down in the
    Order by column.

9.  Choose the Move to Bottom button to move a selected item to the bottom of
    the list window.

10. Choose Next to open the Distribution Query wizard-Finish window where you
    can complete the distribution queries.

#### Completing distribution query options

>   You can complete the query options in the Distribution Query wizard- Finish
>   window. The settings you choose in this window are run time options and must
>   be entered each time you run a query.

>   **To complete distribution query options:**

1.  Refer to *Setting the order of data for a distribution query*, select the
    order of data, and choose Next to open the Distribution Query wizard-Finish
    window.

2.  In the Year field under the Period options, select the fiscal year for the
    query. All the fiscal years set up in Microsoft Dynamics GP are available in
    the drop-down list. The current year is the default year when you first open
    the window.

3.  Select whether to view the financial or calendar year.

4.  Select the Period for the query.

>   If you selected Fiscal view, the following options are available:

-   Date

-   Week

-   Period

-   Quarter

-   Half-year

>   If you selected Calendar view, the following options are available:

-   Date

-   Week

-   Month

-   Quarter

-   Half-year

1.  In the From and To fields, enter a period range, or date range if you
    selected Date. To view the consolidated balances that are brought forward
    when you close the fiscal year, enter 0(zero) in the From field. You must
    also select to view the report for the fiscal year.

2.  Select the reporting ledger options in the Reporting Ledger field for the
    query, whether BASE, IFRS or LOCAL. You can select multiple reporting
    options for your query if required.

>   This field is available only if you have marked the Allow check box for the

>   Reporting Ledger option in the General Ledger Setup window
>   (Administration\>\> Setup \>\> Financial \>\> General Ledger). Refer to the
>   General Ledger documentation for more information.

1.  Enter a comment in the Comment field. This comment will be displayed in the
    Title page worksheet in the Excel report.

2.  Under the Task to be performed section, mark whether to Save the Query
    Definition or Execute Query. The Save the Query Definition option is not
    available if you marked the Execute Ad Hoc Query option in the Welcome
    window. You can mark both the options to save the query before running it.
    The Distribution Query wizard window closes when you choose Finish if you
    have not marked either of these options.

3.  Mark the Generate Title Page option to create a separate worksheet in Excel
    that will display information about the query options. This option is only
    available if you have marked the Execute Query option.

4.  Mark the Create Column Header option if you want to display the column name
    of each selected column in a column header in Excel. This option is only
    available if you have marked the Execute Query option.

5.  Mark the Autofilter Columns option to auto filter all columns in Excel This
    option is only available if you have marked the Execute Query and Create
    Column Header options.

6.  Mark the Save Query Definition option to save the query definition. This
    option is only available if you have chosen to Execute Existing query or
    built a new query using the Query Maintenance option in the Distribution
    Query Welcome window.

7.  Mark the Execute Query check box to run the query. If you marked the Save
    Query Definition option, the query definition is also saved before it is
    run.

8.  Choose Finish to complete the process of saving or running the query
    definition. If you choose to Execute Query, the window will close when you
    choose Finish and the export to Excel will begin. You can cancel the export
    process at any time by choosing Stop in the Progress window.

>   The distribution query will display all the transactions posted from General
>   Ledger, whether or not the transaction accounts are linked to an account
>   class. For transactions that are not linked to an account class, a single
>   assignment will be displayed, without any analysis information.

#### Creating and running a multilevel query

>   You can use Analytical Accounting to generate multilevel queries based on
>   your specific requirements and transaction dimensions. You also can create
>   queries based on columns that you choose to display in the query. The
>   analysis information that is generated when you create a query, is exported
>   to Excel. You can generate a query to view budgeted and actual information
>   for budget IDs, and view the variance and variance percentage between
>   budgeted and actual figures. You can view the posted analysis information
>   for transaction dimension codes that you subsequently set to inactive
>   status.

>   You can create reports with as many levels or rows as you require. A level
>   may be accounts, a dimension, a transaction, a customer, a vendor, an item
>   or site, a tree within a dimension, or a time-period: for example, a week, a
>   month, a fiscal period, or a half-year. You also can create a report for a
>   tree, which will display all the levels of the tree.

>   The level of a report can include some or all codes, accounts, or nodes
>   within a tree. You can create and save your report options or print the
>   report without saving it. Rows with zero values can be hidden at any level
>   within the report. You also can include transactions for which no code has
>   been entered in a report. This is useful for tracking errors.

>   You can view or hide sub-totals at each level. Also, you can select to
>   display details, and also whether to display the detail at the same level
>   throughout the report, or within sections.

>   Queries also can be based on time periods: for example you can select
>   Year-to-Date, This Period, Last Period including Last Year data and also
>   comparisons between this year and last year.

>   **To create and run a multilevel query:**

1.  Open the Multilevel Query wizard-Welcome window.  
    (Inquiry \>\> Financial \>\> Analytical Accounting \>\> Multilevel Query)

2.  Select the type of query to run from the following options:

>   **Execute Existing Query** To run a query that has been saved earlier. You
>   also can change the definition of an existing query and save or run the
>   query.

>   Choose Next to open the Multilevel Query wizard-Query Selection window where
>   you can select an existing query and then complete the query options in the
>   Multilevel Query wizard-Finish window. Refer to *Completing the multilevel
>   query options* for more information.

>   **Execute Ad hoc Query** To run temporary queries. You cannot save ad hoc
>   queries.

>   Choose Next to open the Multilevel Query wizard-Level Selection window where
>   you can select the rows to display in your query. Refer to *Selecting rows
>   for a multilevel query* for more information.

>   **Query Maintenance** To define a new query that can be saved or run. You
>   also can change existing query definitions and save these changes. Saved
>   Query definitions can be used again later.

>   Choose Next to open the Multilevel Query wizard-Query Maintenance window,
>   where you can define the query.

#### Including brought forward balances in a multilevel query

>   You must select the appropriate options in order to view brought forward
>   balances in a multilevel query. The balances are consolidated based on the
>   combination of alphanumeric transaction dimension codes used during
>   transaction entry. Refer to *Consolidating analysis information and carrying
>   balances forward*. Use the following information to understand the options
>   to select to view brought forward balances.

-   Select account numbers as the first level and transaction dimensions as the
    second level in the Multilevel Query wizard-Level Selection window.

-   For Balance Brought Forward transactions, select Not Used as the Code Spread
    to view the consolidated balance in the retained earnings account.

#### Defining a multilevel query

>   You can enter the name and description for a query in the Multilevel Query
>   wizardQuery Maintenance window.

>   **To define a multilevel query:**

1.  Refer to *Creating and running a multilevel query* and select a query
    option. Select Next and open the Multilevel Query wizard-Query Maintenance
    window.

2.  Enter an ID for the query.

3.  Enter a description for the query. This is a required field.

4.  Choose Delete to delete a selected query.

5.  Choose Back to return to the Welcome window.

6.  Choose Cancel to exit the Multilevel Query wizard.

7.  Choose the GoTo button to display the other windows in the wizard. You can
    select a window from the list instead of choosing the Next or Back button
    within the wizard windows. The windows available in the list will depend on
    the current window. For example, from the Query Maintenance window, the
    following windows will be available in the drop-down list:

    -   Option Selection

    -   Level Selection

    -   Tree Selection

    -   Level Filtering

    -   Data Filtering

    -   Column Spreads

    -   Column Selection

    -   Completing the Options

8.  Choose Next to open the Multilevel Query wizard-Level Selection window where
    you can select the rows for the query.

#### Selecting rows for a multilevel query

>   You can select the rows to display in the query using the Multilevel Query
>   wizardLevel Selection window. You must select at least one level for the
>   query. Be sure to select the appropriate levels if you’re creating a query
>   to view budgeted values, or to view brought forward balances.

>   **Budgets** To create a budget query, you must have created at least one
>   budget ID. Choose alphanumeric transaction dimensions along with time and/or
>   accounts as levels. You cannot select any other levels if you want to view
>   any budget information. Once you’ve chosen the required levels, you must
>   specify budget columns in the Column Selection window. Refer to *Selecting
>   columns for a multilevel query* for more information.

>   **Brought forward balances** To view the consolidated balance in the
>   retained earnings account, select Account Numbers as the first level and
>   transaction dimensions as the subsequent levels.

>   **To select rows for a multilevel query:**

1.  Refer to *Creating and running a multilevel query*, and select the query
    option to run. Choose Next and open the Multilevel Query wizard-Query
    Maintenance window. Select a name and description for the query and choose
    Next to open the Multilevel Query wizard-Level Selection window.

2.  From the Available Items list, select the level to include and choose Insert
    to insert the item in the list window level. You can select as many levels
    as required. The levels are organized in a hierarchical manner so that the
    items of level one will appear as the main level of the query. The items of
    level 2 will be combined with the items of level 1.

>   For example, you’ve selected Profit Center as Level 1, and Cost Center as
>   Level 2. When you generate the query, all the Profit Centers will appear at
>   level 1 and the Cost Centers will be combined with each item of level 1.

1.  The Level field displays the name of the level.

2.  Mark the Add Totals Row check box to create a totals row for each item of
    the level.

3.  Mark the Add Page Break check box to add a horizontal page break for each
    item of the level.

4.  Mark the User-Defined Field checkbox to open the Select User-Defined Fields
    window. You can mark this box only when the selected level is an
    alphanumeric transaction dimension. You can also open the Select
    User-Defined Fields window by clicking the expansion arrow button.

5.  Mark the user-defined fields to be displayed on the report you are
    generating.

6.  Choose Select to include the marked user-defined fields on your report.

7.  Choose Cancel to close the window without making a selection and return to
    the Multilevel Query wizard-Level Selection window. No user-defined fields
    will be printed on your report.

8.  In the Multilevel Query wizard-Level Selection window, choose Remove to
    remove a selected item in the list window level.

9.  Choose Remove All to remove all the items in the list window level.

10. Choose the Go To button to select other windows to open in the Multilevel
    Query wizard.

11. Choose Next to open the Multilevel Query wizard-Column Spreads window.

#### Selecting column spreads for a multilevel query

>   You can select the columns to display in the query using the Multilevel
>   Query wizard-Column Spreads window. There are three options for the column
>   output in the Multilevel Query wizard. Of these, you can select two in the
>   Column Spreads window, each of which is optional. The third option is
>   system-defined, and includes debit columns, credit columns, and balance
>   columns, that you can select in the Multilevel Query wizard-Column Selection
>   window.

>   **To select column spreads for a multilevel query:**

1.  Refer to *Selecting rows for a multilevel query*, and select the levels to
    display in the query. Choose Next and open the Multilevel Query wizardColumn
    Spreads window.

2.  Select the level for the Time Spread from the following options:

    -   Not used

    -   As first level

    -   As second level

>   *If Time was chosen as a level in the Level Selection window, this option
>   will be unavailable. To view the consolidated balances in the retained
>   earnings account, select Not Used as the Code Spread.*

1.  If you selected Time Spread at first level or second level, you must choose
    the time frame in the Multilevel Query wizard Finish window. The data in the
    query you generate will be displayed for the time period you select.

>   For example, if you select Use Time Spread as first Level and if you select
>   to view data for a period from 2 to 5, then the report in Excel will display
>   four columns as time spread for each column selected.

1.  The Code Spread option allows you to display codes at the row and column
    levels. Select the level for the code spread from the following options:

    -   Not used

    -   As first level

    -   As second level. The Item field is available for all the options, except
        Not used.

>   *If you select only one of the options, either Time Spread or Code Spread,
>   the value must be at first level. For Balance Brought Forward transactions,
>   select Not Used as the Code Spread to view the consolidated balance in the
>   retained earnings account.*

1.  Select the item to use as code spread. The Item field is available only if
    you’ve selected a code spread and is a required field. Only items that have
    not been selected as levels are available in the Item list.

2.  Choose Exchange Levels to switch the levels of the Time Spread and Code
    Spread fields.

3.  Choose the GoTo button to select other windows to open in the Multilevel
    Query wizard.

4.  Choose Next to open the Multilevel Query wizard-Tree Selection window where
    you can select the trees and Code Spread. If you only selected Time Spread
    as a level, and not Code Spread, the next window in the wizard will be the
    Filter Options window.

#### Selecting trees for a multilevel query

>   Use the Multilevel Query wizard-Tree Selection window to select the trees
>   and code spread to display in your query.

>   **To select trees for a multilevel query:**

1.  Refer to *Selecting column spreads for a multilevel query*, and select
    columns to display in the query. Choose Next and open the Multilevel Query
    wizard-Tree Selection window.

>   The scrolling window displays all selected levels, except time levels. The
>   icon next to a record in the Level column indicates whether it is a level or
>   a code spread. A level is indicated by a vertical blue block. A code spread
>   is indicated by a horizontal blue block.

1.  Mark the Use Tree check box to display the level items in the form of a
    tree.

2.  The Tree field will be available if you selected Use Tree. Select a
    corresponding tree type that matches the level.

3.  Mark the Show Codes check box to display the tree structure and the selected
    level items. If unmarked, only the tree structure of the level item will be
    displayed.

>   If you’ve selected user-defined fields in the Level selection window for a
>   dimension, and you select a tree here for that dimension, the Show Codes
>   option is automatically marked. You cannot unmark this option.

1.  In the Restrict to Tree Level field, you can select the level to be
    displayed for the tree. By default, all levels of a tree will be displayed.
    For Code Spread options, this is a required field.

>   Only the level that you have specified for each tree will be included in the
>   query. For example, if you specify level 3 for a tree, then the query will
>   only print the values existing on level 3.

1.  Choose Back to return to the Multilevel Query wizard- Column Spreads window.

2.  Choose Cancel to exit the Multilevel Query wizard.

3.  Click the GoTo button and select any other window you want to open in the
    Multilevel Query wizard.

4.  Choose Next to open the Multilevel Query wizard-Filter Options window. In
    this window, you can restrict the information you want to display in the
    query.

#### Setting filter options for a multilevel query

>   You can select the row output of each level, the column output, and the Code
>   Spread columns in the Multilevel Query wizard-Filter Options window. These
>   filters will help you generate queries specific to your requirements.

>   **To set filter options for a multilevel query:**

1.  Refer to *Selecting trees for a multilevel query*, and select a tree for the
    query. Choose Next to open the Multilevel Query wizard-Filter Options
    window.

>   This window displays all levels except the following levels:

-   Time level, that is set in the Completing the Options window.

-   All levels if no tree is defined

-   The Code spread, if no tree output is defined for it.

>   The image on the left of a level indicates if a filter already exists, or if
>   an item is used as a level, or as a Code Spread.

>   The Level column displays the name of the level.

>   The Empty, Select type, …, and And columns will display the options that you
>   select in the Selected fields section below.

>   The Selected fields are available only if you have selected an item in the
>   list window.

1.  Select a level in the list window. The Item field will display the name of
    the selected level.

2.  Mark the Empty checkbox to include empty fields for the selected item in the
    query. The Empty checkbox is available only if you’ve selected one of the
    following in the Item field:

-   Customer ID

-   Vendor ID

-   Item Number

-   Site ID and all Transaction dimensions.

1.  From the Select Type list, select the restrictions for the query from the
    following options:

**Any** To select all the records.

**Contains** To select only records that match the specified criteria.

**Equal To** In order to select records that are equal to the specified
criteria.

>   **Not Equal to** Only records that do not match the specified criteria are
>   selected.

>   **Begins with** To select only records that begin with a specified
>   criterion.

**Is Between** To select only records that are between a specified value.

>   **Greater than** To select only records with values that are greater than
>   the specified value.

>   **Less than** To select only records with values that are lesser than the
>   specified value.

1.  The ‘**…**’ field is available for all Select Types, except Any. Enter a
    value to restrict the query.

2.  The ‘And’ field is available if the Select Type is set to Is Between. Enter
    a value to restrict the query.

3.  In the Accounts field, mark to include the Balance Sheet, Profit and Loss
    and/or Unit Accounts in the query. By default, Balance Sheet and Unit
    accounts are not marked and Profit and Loss is marked.

4.  Use the Search Type selections to specify whether all or some of the filter
    options must be matched before a record can be displayed. If the filter
    option for each column should match before displaying a record, select Match
    All. To see a record displayed as long as it matches at least one of your
    filter options, select Match 1 or More.

5.  Choose the GoTo button to select other windows to open in the Multilevel
    Query wizard.

6.  Choose Next to open the Multilevel Query wizard-Column Selection window.

>   You can select the columns to be displayed in the query in this window.

#### Selecting columns for a multilevel query

>   You can select the columns to display in your query using the Multilevel
>   Query wizard-Column Selection window. These columns are system defined and
>   consist of Debit, Credit, and Balance columns for actual, budgets, the
>   variance and the variance percentage. Refer to *Modifying column headings
>   for inquiries and reports* for more information.

>   **Budget columns** You can select budget columns in this window if you’ve
>   selected alphanumeric dimensions with or without account and/or time as
>   levels in the Level Selection window. You can choose the actual, budget,
>   variance, and variance percentage columns to view the variance between
>   actual and budgeted figures.

-   You must select a budget ID for every budget column that you select. Once
    you select a budget ID against a budget column, it will default for all
    budget columns that you insert directly below it until you use the same
    budget column that is already inserted. However, if you insert a non- budget
    column after a budget column, and then insert another budget column, you
    will have to select a budget ID manually.

-   You cannot select a budget column if you have selected Customer ID, Vendor
    ID, Site, or Item in the Level Selection window.

-   You can select a budget column more than once, if you assign a different
    budget ID for every selection. All the budget IDs you select must have the
    same budget tree ID attached to them.

>   **To select columns for a multilevel query:**

1.  Refer to *Setting filter options for a multilevel query*, and set the filter
    options for the query. Choose Next to open the Multilevel Query wizardColumn
    Selection window.

2.  Click the Available Columns button to switch the column display between
    description and header.

3.  Select a column from the Available Columns list and choose Insert to insert
    it into the Column field. The columns will be created in the query based on
    the order displayed here.

*If you select all the columns available, the reports will take longer to
generate.*

1.  Mark the Add Subtotal Column option to create a Subtotal column at the end
    of each second level range. This option is available only if time spread and
    code spread have been defined. Also, this option only can be used for amount
    columns and not percentage columns.

2.  Mark the Add Totals Column to create a totals column, that will be added at
    the end of all the other columns in the query. This option is available only
    if time or code spread have been defined. Also, this option can only be used
    for amount columns and not percentage columns.

3.  Choose Next to open the Multilevel Query wizard-Finish window where you can
    complete the query definitions before generating the query.

#### Completing the multilevel query options

>   Use the Multilevel Query wizard-Finish window to complete your query
>   options. The options you select in this window are run time options and must
>   be set up each time you run a query.

>   **To complete the multilevel query options:**

1.  Refer to *Selecting columns for a multilevel query*, and select the columns
    to include in your query. Choose Next to open the Multilevel Query
    wizard-Finish window.

2.  In the Year field, select the year for the query. The current open year is
    selected by default.

3.  Select whether to view the fiscal or calendar year and select the period for
    the fiscal or calendar year.

4.  If you selected Fiscal view, select one of the following options:

-   Week

-   Period

-   Quarter

-   Half-year

>   If you selected Calendar view, select one of the following options:

-   Week

-   Month

-   Quarter

-   Half-year

>   *You cannot select Week as a period if you have selected budget columns.
>   Also, you can view the consolidated balances that are brought forward only
>   if you select Fiscal view.*

1.  Enter a period range in the From and To fields.

2.  Enter a base period for the query. The Base Period field only will be
    available if time spread or code spread are not used. This is a required
    field that generates the period reference for all columns.

3.  Select the reporting ledger options in the Reporting Ledger field for the
    query, whether BASE, IFRS or LOCAL. You can select multiple reporting
    options for your query if required.

>   This field is available only if you have marked the Allow check box for the

>   Reporting Ledger option in the General Ledger Setup window (Administration
>   \>\> Setup \>\> Financial \>\> General Ledger). Refer to the General Ledger
>   documentation for more information.

1.  Enter a comment for the query. This comment will be displayed in the Title
    page worksheet in the Excel Report.

2.  In the Show Amounts in field, select how to round off cell values.

3.  The Save Query Definition check box is only available if you have selected
    Execute Existing query or created a new query using the Query Maintenance
    option in the Multilevel Query wizard-Welcome window. Mark this option to
    save the query definition.

4.  Mark the Execute Query option to run the query.

5.  Select the Generate Title Page option to create a separate worksheet in
    Excel that will display information about the query options. This option
    only will be available if you selected the Execute Query option

6.  Select the Group Columns option to group columns by first and second column
    level. This option will be only available if you selected the Execute Query
    option and have used the Time Spread or Code Spread.

7.  Mark the Clear Empty Cells option to clear column cells with no values. This
    option will only be available if you have selected the Execute Query option

8.  Mark the Group Rows option to group the rows by display level in Excel. This
    option will only be available if you have selected the Execute Query option

9.  Mark the Include BBF option to view the consolidated brought forward
    balances in the YTD columns in the report. You must select Fiscal Year as
    the option in step 3 to view brought forward balances.

10. Click the GoTo button to select other windows you want to open in the
    Multilevel Query wizard.

11. Choose Finish to save or run the query. If you’ve chosen to run a query, a
    progress window will appear and when processing is complete, an Excel
    worksheet will open, displaying the query.

**Chapter 18: Reports**

>   You can print the queries that you generate using the Analytical Accounting

>   Distribution Query wizard or the Multilevel Query wizard to an Excel
>   spreadsheet.

>   Refer to *Chapter 17, “Inquiries”*for more information about generating
>   queries in Analytical Accounting.

>   Use the following information to understand the reports generated using the
>   Analytical Accounting query wizards.

>   This information is divided into the following sections:

-   *Distribution query report*

-   *Multilevel query report*

#### Distribution query report

>   After you process a query, it will be displayed in an Excel Spreadsheet. If
>   you double-click a specific journal entry in the spreadsheet, the Analytical
>   Accounting Journal Inquiry window will open, where you can view the entry in
>   detail.

>   You can view the descriptions of Vendor ID, Customer ID, Item Number, Site
>   ID, Asset ID, Book ID, and all transaction dimensions by clicking the
>   comment of the relevant row.

>   In a Distribution Query, all posted transactions, regardless of the account
>   class they are linked to, are displayed.

>   For transactions that are not linked to an account class, a single
>   assignment will be displayed with no analysis information.

>   The audit trail column displayed is generated by Analytical Accounting.
>   Refer to*Creating and running a distribution query* for more information on
>   generating a distribution query.

**Distribution Query displaying distributions:**  
  
**IMAGE – AADQ.jpg**

![A screenshot of a social media post Description automatically generated](media/39b52737a49177f60d86955bb17e0d65.jpg)

**Distribution Query without column header:**

**IMAGE – AADQC.jpg**

![A screenshot of a cell phone Description automatically generated](media/c001a8fd37eb88520f4330264168c26d.jpg)

>   **Distribution Query displaying column header:**

IMAGE – AADQH.jpg

![A screenshot of a cell phone Description automatically generated](media/94a06be68a7e49b7c789d931baec04e4.jpg)

#### Multilevel query report

>   The multilevel query will display the system-defined columns and the columns
>   you've selected. Refer to *Creating and running a multilevel query* for more
>   information about generating a multilevel query.

>   The report also will display as many levels as you've selected, along with
>   other options you've specified while generating the query.

**Glossary**

#### Account class

>   A set of accounts grouped together. An account class is linked to one or
>   more transaction dimensions. Analytical Accounting assignments can be
>   carried out only for those distribution accounts that are linked to an
>   account class.

#### Activate

>   The process of integrating Microsoft Dynamics GP data into Analytical
>   Accounting.

#### Alias

>   A group of transaction dimension codes that can be used to enter the
>   analysis information quickly during transaction entry.

#### Alphanumeric transaction dimension

>   A transaction dimension that consists of letters and numbers or special
>   characters.

#### Analysis information

>   Information entered using Analytical Accounting that helps you analyze the
>   transactions of your company. This information would include assignments and
>   transaction dimension codes.

#### Analysis type

>   The status assigned to a transaction dimension in an account class. Statuses
>   are:

>   Not Allowed, Fixed, Required or Optional.

#### Assignment

>   Allocation of transaction distribution amount by value or percentage basis
>   among valid code combinations.

#### Boolean transaction dimension

>   A transaction dimension defined by a Yes/ No condition.

#### Budget Tree

>   A hierarchal combination of transaction dimension codes. The hierarchy is
>   based on the order in which transaction dimensions are selected.

#### Code combination

>   The relationship between the transaction dimension codes of two alphanumeric
>   transaction dimensions.

#### Data type

>   The nature of a transaction dimension, whether alphanumeric, numeric, date
>   or Boolean.

#### Date transaction dimension

>   A transaction dimension that allows you to enter information in date format.

**Dimension Code Tree**

>   Budget tree created after assigning codes.

#### Inactive transaction dimension Valid subset

A transaction dimension that cannot be used A relationship between alphanumeric

>   to enter analysis information during transaction dimensions that allows
>   specific transaction entry. code combinations to be used.

#### Incomplete distribution

>   A distribution where transaction distribution amounts are not assigned fully
>   or where required codes have not been entered.

#### Leaf Node

>   The last node on a tree. This node has no sub nodes.

#### Master records

>   Permanent records of your business such as accounts, vendors, customers etc.

#### Main tree

>   System-generated tree that cannot be deleted.

#### Node

>   A subsidiary of a tree. For budget trees, a node is a combination of codes
>   to which a code belongs.

#### Numeric transaction dimension

>   A transaction dimension that collates numeric information.

#### Related transaction dimension

>   An alphanumeric transaction dimension that is linked to another by way of
>   ownership, or as a valid subset.

#### Transaction dimension

>   A criterion for collating analysis information. These are linked to the
>   company’s chart of accounts using an account class.

#### Transaction dimension code

>   The defined subset of a transaction dimension. Analysis information is
>   entered using codes; this information is compiled to display the analytical
>   information for transaction dimensions.

#### Transaction dimension relation

>   The relationship between transaction dimensions. Determines if transaction
>   dimensions can be used together or not during transaction entry.

**Trees**

>   Display of data in hierarchal form.

#### Tree structure

>   The relationship of ownership between alphanumeric transaction dimensions

#### Unassigned

>   Transaction distribution amount that remains to be assigned.

**User-defined tree**

>   Tree structure set up by the user.

#### Validation

>   The process of verifying the analysis information you’ve entered.
