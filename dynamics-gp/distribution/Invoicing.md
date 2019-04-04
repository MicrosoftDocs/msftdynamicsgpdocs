**Invoicing in Microsoft Dynamics GP**

**Introduction**

You can use Invoicing to enter and edit invoices and returns and print an
invoice or return. You also can manage your invoicing documents once they’re
entered and print reports to analyze your invoicing activity.

>   You also can use Invoicing to complete the following tasks:

-   Correct, delete, and void invoicing documents

-   Print a quote, order, invoice, back order, or return for a customer

-   Allocate and fulfill items.

-   This introduction is divided into the following sections:

-   *What’s in this manual*

-   *Symbols and conventions*

-   *Resources available from the Help menu*

-   *Send us your documentation comments*

>   **What’s in this manual**

>   This manual is designed to give you an understanding of how to use the
>   features of Invoicing, and how it integrates with the Microsoft Dynamics® GP
>   system.

>   To make best use of Invoicing, you should be familiar with systemwide
>   features described in the System User’s Guide, the System Setup Guide, and
>   the System Administrator’s Guide.

>   Some features described in the documentation are optional and can be
>   purchased through your Microsoft Dynamics GP partner.

>   To view information about the release of Microsoft Dynamics GP that you’re
>   using and which modules or features you are registered to use, choose Help
>   \>\> About Microsoft Dynamics GP.

>   The manual is divided into the following parts:

-   *Part 1, Setup*, introduces Invoicing and gives detailed instructions on how
    to set it up.

-   *Part 2, Transaction entry*, explains how to enter and edit invoices and
    returns and how to print an invoice or return. It also explains how to post
    Invoicing transactions.

-   *Part 3, Transaction activity*, includes information that will help manage
    your invoicing documents once they are entered.

-   *Part 4, Inquiries, reports, and utilities*, describes how to use inquiries
    and reports to analyze your invoicing activity and explains procedures you
    can use to clear historical data.

>   **Resources available from the Help menu**

>   The Microsoft Dynamics GP Help menu gives you access to user assistance
>   resources on your computer, as well as on the Web.

>   **Contents**

>   Opens the Help file for the active Microsoft Dynamics GP component, and
>   displays the main “contents” topic. To browse a more detailed table of
>   contents, click the Contents tab above the Help navigation pane. Items in
>   the contents topic and tab are arranged by module. If the contents for the
>   active component includes an “Additional Help files” topic, click the links
>   to view separate Help files that describe additional components.

>   To find information in Help by using the index or full-text search, click
>   the appropriate tab above the navigation pane, and type the keyword to find.

>   To save the link to a topic in the Help, select a topic and then select the
>   Favorites tab. Click Add.

>   **Index**

>   Opens the Help file for the active Microsoft Dynamics GP component, with the
>   Index tab active. To find information about a window that’s not currently
>   displayed, type the name of the window, and click Display.

>   **About this window**

>   Displays overview information about the current window. To view related
>   topics and descriptions of the fields, buttons, and menus for the window,
>   choose the appropriate link in the topic. You also can press F1 to display
>   Help about the current window.

**Lookup**

Opens a lookup window, if a window that you are viewing has a lookup window. For
example, if the Checkbook Maintenance window is open, you can choose this item
to open the Checkbooks lookup window.

**Show Required Fields**

Highlights fields that are required to have entries. Required fields must
contain information before you can save the record and close the window. You can
change the font color and style used to highlight required fields. On the
Microsoft Dynamics GP menu, choose User Preferences, and then choose Display.

**What’s New**

Provides information about enhancements that were added to Microsoft Dynamics GP
since the last major release.

>   **Microsoft Dynamics GP Online**

Opens a Web page that provides links to a variety of Web-based user assistance
resources. Access to some items requires registration for a paid support plan.

>   **Current implementation and upgrade information** The most recent revisions
>   of upgrade and implementation documentation, plus documentation for service
>   packs and payroll tax updates.

>   **User documentation and resources** The most recent user guides, howto
>   articles, and white papers for users.

>   **Developer documentation and resources** The most recent documentation and
>   updated information for developers.

>   **Product support information** Information about the Microsoft Dynamics GP
>   product support plans and options that are available, along with information
>   about peer support and self-support resources.

>   **Services information** Information about Microsoft Dynamics GP support,
>   training, and consulting services.

>   **Microsoft Dynamics GP Community** Access to newsgroups, where you can ask
>   questions or share your expertise with other Microsoft Dynamics GP users.

>   **CustomerSource home page** A wide range of resources available to
>   customers who are registered for a paid support plan. Includes access to
>   Knowledge Base articles, software downloads, self-support, and much more.

>   **Part 1: Setup**

This part of the documentation includes information that will help you set up
Invoicing. The setup procedures generally need to be completed once, but you can
refer to this information at other times for instructions on modifying or
viewing existing entries.

>   The following information is discussed:

-   *Chapter 1, “Setup overview,”* lists the setup tasks you need to complete in
    other modules and explains the setup process.

-   *Chapter 2, “Module setup,”* provides instructions for setting up the
    Invoicing module.

**Chapter 1: Setup overview**

>   Use this information to learn about and set up Invoicing. The setup
>   procedures are organized in an order that will ensure Invoicing is set up
>   properly.

>   Setup information is divided into the following sections:

-   *Before you set up Invoicing*

-   *Invoicing setup*

#### Before you set up Invoicing

>   Before you begin setting up Invoicing, be sure you’ve completed the System

>   Manager and General Ledger setup procedures. If you’re using Receivables
>   Management and Inventory, you also should set up these modules before you
>   set up Invoicing. For more information about setting up your system, refer
>   to the System Setup documentation (Help \>\> Contents \>\> select Setting up
>   the System). For more information about setting up General Ledger,
>   Receivables Management, and Inventory, refer to the documentation for those
>   modules.

#### Invoicing setup

>   When you set up Invoicing, you can open each setup window and enter
>   information, or you can use the Setup Checklist window (Microsoft Dynamics
>   GP \>\> Tools \>\> Setup \>\> Setup Checklist) to guide you through the
>   setup process. See your System Setup Guide (Help \>\> Contents \>\> select
>   Setting up the System) for more information about the Setup Checklist
>   window.

**Chapter 2: Module setup**

>   During the Invoicing setup process, you’ll set up your Invoicing preferences
>   such as default entries, tax calculation options, starting document numbers,
>   and whether to maintain document history.

>   You can open the Invoicing setup windows using menu options, or you can
>   follow the setup routine, which will guide you through the setup process.
>   For more information about the setup routine, see *Invoicing setup* .

>   Setup information is divided into the following sections:

-   *Setting Invoicing general options and defaults*

-   *Advanced tax options for Invoicing*

-   *Setting up taxes and options*

#### Setting Invoicing general options and defaults

>   Use the Invoicing Setup window to set general default entries that will
>   appear throughout the Invoicing module. You can also indicate what kind of
>   history records you want to maintain, which posting accounts to use, and
>   what document numbering options you want to use.

>   **To set Invoicing general options and defaults:**

1.  Open the Invoicing Setup window. (Microsoft Dynamics GP menu \>\> Tools \>\>
    Setup \>\> Sales \>\> Invoicing) Mark Preferences settings:

>   Image(INVSET)

![](media/32767b32f88a51062a725da2326fbe71.jpg)

>   A screenshot of a cell phone Description automatically generated

>   **Display Item Unit Cost** Mark to view the cost of each item as you’re
>   entering it on an invoice. The unit cost displayed will depend on the
>   inventory valuation method assigned to each item, which can have its own
>   valuation method.

>   The following table displays the cost displayed with each valuation method:

| **Valuation method** | **Cost displayed** |
|----------------------|--------------------|
| FIFO Perpetual       | Current Cost       |
| LIFO Perpetual       | Current Cost       |
| Average Perpetual    | Current Cost       |
| FIFO Periodic        | Standard Cost      |
| LIFO Periodic        | Standard Cost      |

>   **Track Voided Transactions in History** Mark to keep track of voided
>   transactions. If you don’t track voided documents, they will be removed
>   during posting, and the document number will become available for recording
>   documents again.

1.  Choose Item or Customer to use the set of posting accounts as default
    accounts.

>   Many of the posting accounts you assign to customer records in Receivables
>   Management and to items in Inventory Control are used to track similar
>   revenue or expense accounts. For example, you can assign different posting
>   accounts to track Cost of Goods Sold amounts for individual items and for
>   customers. Choose the posting accounts assigned to items, or those assigned
>   to customers, to be suggested as default entries if the items and customers
>   aren’t assigned matching posting accounts.

1.  Choose the types of history to keep for your company.

>   **Transaction Detail** Mark to keep detailed history for the transactions
>   you enter. If you keep transaction detail history, you’ll be able to view
>   posted transactions in the inquiry windows and print reports for posted
>   transactions.

>   **Account Distributions** Mark to keep history that includes the debit and
>   credit amounts for each document, along with the posting accounts they were
>   distributed to; you may find this information useful for auditing purposes.

>   *Keeping transaction and distribution history will use a considerable amount
>   of disk space. Please plan accordingly if you keep history. Historical
>   information can be removed when it’s no longer useful. For more information,
>   see Removing invoicing history.*

1.  Enter labels for user-defined fields, which can be used to track special
    information in Invoicing. For example, to track shipping numbers for special
    courier labels, enter Shipping Number as the name of one of the user-defined
    fields. In the Invoice Customer Detail Entry window, Shipping Number will
    appear as a field name and you can enter the shipping number for each
    invoice.

2.  Enter default site, checkbook, and comment ID values.

>   **Site ID** Enter or select a site ID. A site is a store, warehouse, or
>   other building at which you do business or store items. The site ID you
>   enter here will appear as a default entry in the Invoice Entry window. If
>   you have multiple sites, enter the site you’ll use most often.

>   **Checkbook ID** Enter or select a checkbook ID. The checkbook ID identifies
>   a particular checking account to which amounts received will be deposited.
>   The checkbook ID you enter here will appear as a default entry in the
>   Invoice Batch Entry window.

>   **Comment ID** Enter or select a comment ID. Comment IDs identify standard
>   comments you print on invoices. The comment ID you enter here will appear as
>   a default in the Invoice Entry window.

1.  Select default document formats for printing invoices, returns, and packing
    slips. You can print on blank paper, a long form, or a short form. You’ll be
    able to change these defaults for individual documents.

2.  Select the number of decimal places to use for non-inventoried item
    quantities and currency amounts. The decimal places you enter here will
    appear as default entries in the Invoice Entry window when you enter a
    non-inventoried item.

>   If you’re selling inventoried items, the decimal place settings you made in
>   the Item Maintenance window will appear as default entries for those items
>   when you enter invoices in the Invoice Entry window.

1.  Enter the document description, code, and number for each document type used
    in Invoicing or accept the default entries.

>   **Description** The description entered here will appear in the document
>   list in the Invoice Entry window. You can change the default description if
>   you prefer to call your invoices, returns, and packing slips by another
>   name. For example, if you refer to your invoices as bills of sale, enter
>   Bill of Sale in the Description field.

>   **Code** The document code will be used on reports to indicate the document
>   type for each document.

>   **Number** The starting number for this document type will increment by one
>   to the next available number each time you enter a transaction. We recommend
>   that you use an alphanumeric code for document numbers with the document
>   type included, such as IVC000001, to make transactions easier to identify on
>   reports and in lookup windows.

>   By defining the next document number, you also are determining the number of
>   unique document numbers that will be available. For example, if you enter
>   IVC001 as the next invoice number, you'll be able to enter up to 999 unique
>   invoice documents. You can change the next document number when you enter
>   transactions; however, the same number can’t be posted twice. If you don’t
>   choose to keep historical records of voided transactions, the document
>   number will become available when an invoice is deleted.

>   *If you use Invoicing on a network where more than one person is entering
>   transactions at the same time, the number may appear to increment by two or
>   more.*

1.  If you’re using generic—non-numbered—forms and aren’t using alphanumeric
    document numbers, you can set additional options that control document
    numbering sequences for returns and packing slips.

>   **Return** Mark to use the invoice numbering sequence for both invoices and
>   returns. For example, if you’re entering a return in the Invoice Entry
>   window, and the next available invoice number is 98, the document number
>   that appears for your return will be 98.

>   **Packing Slip** Mark for the document number that appears on the packing
>   slip to match the number of the invoice associated with it.

1.  Choose File \>\> Print to review the setup options you’ve entered.

2.  Choose OK to save changes and close the Invoicing Setup window.

#### Advanced tax options for Invoicing

>   If Advanced is marked in the Invoicing Setup Options window, the tax details
>   in the tax schedules are compared when tax is calculated on an invoice. Tax
>   is calculated only for the details that match the customer, item, site,
>   freight, and miscellaneous charges, depending on the shipping method
>   selected on the invoice.

>   The shipping method determines where the exchange of goods takes place and
>   which tax schedule appears as a default for the transaction.

>   **Delivery** The tax schedule designated for the shipping address of the
>   customer will appear as the default.

>   **Pickup** The tax schedule designated for the site you’re selling from will
>   appear as the default schedule.

>   The following diagrams show how tax details are compared to determine the
>   amount of tax that will be calculated.

>   **For a delivery shipping method**

Image INVDSM.jpg

![](media/451fe8a08df1b60778b8fa95cc7df3f3.jpg)

>   A picture containing screenshot Description automatically generated

>   The tax calculated on the line item would be the amount or percentage
>   assigned to tax detail TAX001, the tax calculated on the freight charge will
>   be the amount or percentage assigned to tax detail TAX003, and the tax on
>   the miscellaneous charge will be the amount or percentage assigned to tax
>   details TAX001 and TAX004. These details are used because they appear in
>   both the customer schedule and in the item, freight, or miscellaneous
>   schedule.

>   **For a pickup shipping method**

Image INVSM.jpg

![](media/16436353e4fc80931c711c555f609205.jpg)

>   A screenshot of a cell phone Description automatically generated

>   The tax calculated on the line item would be the amount or percentage
>   assigned to tax detail TAX002, the tax calculated on the freight charge will
>   be the amount or percentage assigned to tax detail TAX002, and the tax on
>   the miscellaneous charge will be the amount or percentage assigned to tax
>   detail TAX004. These details are used because they appear in both the site
>   schedule and in the item, freight, or miscellaneous schedule.

>   *Each time the shipping method, site ID, or shipping address for the
>   customer is changed, the tax schedule may be changed and taxes may be
>   recalculated.*

#### Setting up taxes and options

>   Use the Invoicing Setup Options window to specify a method for calculating
>   taxes and to set up other options. You can further restrict each option by
>   assigning a password to it. If the option is marked but no password is
>   entered, anyone who has access to the related windows can use the option.

>   **To set up taxes and options:**

1.  Open the Invoicing Setup Options window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Sales \>\> Invoicing \>\> Options button)

Image INVISO.jpg

![A screenshot of a cell phone Description automatically generated](media/4e459f1310fc6a7a2d447aab5841022f.jpg)

1.  Choose advanced tax calculations or a single schedule for use for all sales.

>   **Advanced** Mark to specify a tax schedule to use for non-inventoried items
>   and freight and miscellaneous charges.

>   **Single Schedule** Mark to specify one tax schedule for all items on all
>   documents. Items on each sales document will be taxed using the tax details
>   in the schedule you specify here. Tax-exempt and non-tax items are not
>   available when you select single schedule. Taxes won’t be calculated on
>   freight or miscellaneous charges.

>   Inventoried items will use the tax schedule assigned to each item in the
>   Item Maintenance window. You can change tax details for an individual
>   invoice using the Invoice Tax Summary Entry window (Transactions \>\> Sales
>   \>\> Invoice Entry \>\> Tax expansion button).

1.  If you use advanced tax calculations, select the taxes options for
    noninventoried items, freight, and miscellaneous charges.

>   **Taxable** Tax details will be assigned to the customer, item, freight, and
>   miscellaneous charges.

>   **Nontaxable** No taxes will be calculated.

>   **Base on customers** The shipping method determines the tax schedule. If
>   the shipping method is delivery, the tax details from the customer tax
>   schedule will be used. If the shipping method is pickup, the tax details
>   from the site tax schedule will be used.

>   *You can change the tax schedules for individual invoices in the Invoice Tax
>   Schedule Entry window.*

>   For more information on how taxes are calculated for an invoice, see
>   *Advanced tax options for Invoicing*.

>   Mark Invoicing options. You can further restrict each option by assigning a
>   password to it.

**Override Document Number** Mark to change the default document number that
appears in the Invoice Entry window—this is the number displayed in the
Invoicing Setup window. If you don’t mark this option, the Document Number field
in the

>   Invoice Entry window will display the next number available from the
>   Invoicing Setup window, and you won’t be able to change it.

>   **Override Item Quantity** Mark to sell inventoried items that aren’t
>   currently in stock. If you mark this option and a quantity entered in the
>   Invoice Entry window is greater than the amount available, the Invoice
>   Quantity Shortage Options window will open and you can choose to override
>   the quantity available. If you don’t mark this option, only the quantity
>   available can be sold.

>   **Override Price** Mark to override the unit price that appears as a default
>   and the extended price that is automatically calculated for invoices and
>   returns in the Invoice Entry window. If you don’t mark this option, changes
>   won’t be allowed to the amounts displayed in the Unit Price and Extended
>   Price fields.

>   **Enter Price Below Cost** Mark to enter a price that’s lower than the
>   current cost of an item. This option is available only if you also marked
>   the Override Price option. If you don’t mark this option, prices below the
>   current cost won’t be allowed in the Invoice Entry window.

>   **Override Item Unit Cost for Returns** Mark to override the unit cost of an
>   item when you enter a return.

>   **Enter Non-Inventory Items** Mark to enter non-inventoried items in the
>   Invoice Entry window for a sale or return without creating records for those
>   items. If you mark this option, any item numbers entered in the Invoice
>   Entry window that don’t exist can be recognized as non-inventoried items. If
>   you don’t allow non-inventory items, only items that exist in your inventory
>   can be entered.

>   **Auto-Assign Serial Numbers** Mark to automatically assign serial numbers
>   to sales according to the valuation method selected for serialnumbered items
>   being sold. For example, invoices for an item with a FIFO valuation method
>   will be assigned items with the oldest serial numbers first.

>   **Auto-Assign Lot Numbers** Mark to automatically assign lot numbers to
>   sales. Lot numbers can be assigned automatically by receipt date or by
>   expiration date, depending on how you select to automatically assign lot
>   numbers in the Inventory Control Setup window.

>   Lot number assignment will be based on the valuation method selected for
>   lotnumbered items being sold if you selected to assign lot numbers by
>   receipt date. For example, invoices for an item with a FIFO valuation method
>   will be assigned items with the oldest lot numbers first. If you selected to
>   assign lot numbers by expiration date, the lot numbers nearing expiration
>   dates will be used first. Lot numbers without an expiration date will not be
>   assigned.

>   When automatically assigning lot numbers by receipt date or expiration date,
>   expired lots won’t be used even if you marked the Other Transactions option
>   in the Inventory Control Setup window.

>   **Remove Transaction Holds** Mark to remove a hold status on a transaction
>   during data entry. We recommend that you enter a password to limit the
>   number of employees who are able to remove transaction holds.

>   **Edit Printed Documents** Mark to edit documents after they’ve been
>   printed. If you don’t specify a password, this option also allows you to
>   print invoices, returns, and packing slips without entering the transactions
>   in a batch.

>   If you don’t mark this option, printed documents won’t be available for
>   editing, and you’ll be able to view the document only by using the inquiry
>   feature. In addition, you’ll be able to print invoices and returns for
>   transactions only if they’ve been entered in a batch.

>   *We recommend that you use a password to limit the number of employees who
>   are able to edit printed documents. If you require a password, however, you
>   must enter transactions in a batch to print invoices, returns, and packing
>   slips.*

>   **Void Documents** Mark to void saved invoices and returns in the Invoice
>   Entry window. We recommend that you require a password to limit the number
>   of employees who are able to void documents. If you don’t allow documents to
>   be voided, the Delete button in the Invoice Entry window will be
>   unavailable.

1.  Choose File \>\> Print to review the setup options you’ve entered.

2.  Choose OK to save the changes you’ve made. The Invoicing Setup window will
    be displayed.

3.  Choose OK to save changes and close the Invoicing Setup window.

>   **Part 2: Transaction entry**

This part of the documentation explains how to enter invoices and returns. You
can enter Invoicing documents individually or in batches. It also describes how
items are tracked, priced, allocated, and fulfilled, and how taxes are handled.

The following information is discussed:

-   *Chapter 3, “Item information,”* describes item tracking and pricing related
    to Invoicing.

-   *Chapter 4, “Batches,”* explains how to create, modify, and delete batches.

-   *Chapter 5, “Invoices and returns,”* describes how to enter, edit, and post
    transactions and also includes information needed to create transactions.

-   *Chapter 6, “Invoicing taxes,”* explains how sales tax is calculated,
    modified, and distributed in Invoicing.

-   *Chapter 7, “Allocating item quantities,”* describes how items are allocated
    and fulfilled on invoices

**Chapter 3: Item information**

>   Use this information to learn more about handling items in Invoicing. Item
>   information is divided into the following sections:

-   *Item pricing*

-   *Unit cost of items*

-   *Non-inventoried items*

-   *Adding items*

-   *Serial- or lot-numbered items*

#### Item pricing

>   If you’re entering an inventoried item, the unit price*—*the price at which
>   each item is being sold—will be calculated using the information entered for
>   the item in the Item Price List Maintenance window. For more information,
>   refer to the Inventory Control documentation.

| **Valuation method** | **Unit cost displayed** |
|----------------------|-------------------------|
| FIFO perpetual       | Current cost            |
| LIFO perpetual       | Current cost            |
| Average perpetual    | Current cost            |
| FIFO periodic        | Standard cost           |
| LIFO periodic        | Standard cost           |

>   The price for an item is determined by price levels on the customer card. If
>   a price level hasn’t been assigned to the customer, the price level from the
>   Receivables Management Setup window is used. If there isn’t a price level
>   set up for the customer or for Receivables Management, the default price
>   level for the item is used.

>   When you enter an item, the price from the item price list is determined by
>   the price level and the unit of measure selected on the invoicing document
>   for the item. If a price hasn’t been set up for the price level, the default
>   price level for the item will be used to determine the price. You can view
>   the price level used for the item in the Invoice Item Detail Entry window.

>   You can change the unit price on the document if Override Prices is marked
>   in the

>   Invoicing Setup Options window. If you’re entering a unit price that is
>   below cost, Enter Price Below Cost also must be marked in the Invoicing
>   Setup Options window. Depending on how these options were set up, you might
>   need to enter a password.

#### Unit cost of items

>   If Display Unit Cost is marked in the Invoicing Setup window, the unit cost
>   will be displayed in the Invoice Entry window for each sales inventory type
>   item. The unit cost will not be displayed for items that are assigned the
>   type of service, flat fee, or miscellaneous charge.

>   The unit cost is the current cost or the standard cost of the item,
>   depending on the inventory valuation method. The following table shows the
>   default cost that appears as the Unit Cost for each valuation method.

The cost displayed might not be the cost used to adjust inventory and cost of
goods sold when the document is posted; this will depend on the valuation method
used.

-   For FIFO Perpetual and LIFO Perpetual, the valuation method is used to
    determine the actual cost of the item sold.

-   For FIFO Periodic and LIFO Periodic, the standard cost is used.

-   For Average Perpetual, the current cost is used. For this valuation method,
    the current cost represents the average cost of the item and is updated
    whenever the item quantity is increased.

If you enter a return, the default entry for the unit cost of a line item is the
current cost for the item from the Item Maintenance window. If Override Item
Unit Cost for Returns is marked in the Invoicing Setup Options window, you can
change the unit cost of the item, which is the cost used to return the item to
inventory. If Override Item Unit Cost for Returns isn’t marked, the current cost
of the line item will be displayed and can’t be changed.

#### Non-inventoried items

You can enter non-inventoried items—items that don’t exist in your inventory
records—if Enter Non-Inventoried Items is marked in the Invoicing Setup Options
window.

When you enter a non-inventoried item you must enter the item description, unit
price and unit cost. The item won’t be tracked in inventory, but it will appear
on Invoicing analysis and history reports.

The following default accounts are used for non-inventoried items:

| **Account**          | **Source**                                                                                                                                                                                                         |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inventory            | The account assigned to non-inventoried items for the Sales series in the Posting Accounts Setup window.                                                                                                           |
| Returned, In Use, In | The account assigned to non-inventoried items for the Sales series in the Posting Accounts Setup window.                                                                                                           |
| Cost of Goods Sold   | If you have marked to use posting accounts from the customer, the system uses the account assigned to the customer. Otherwise, the account from the Inventory series in the Posting Accounts Setup window is used. |
| Sales                | If you have marked to use posting accounts from the customer, the system uses the account assigned to the customer. Otherwise, the account from the Inventory series in the Posting Accounts Setup window is used. |
| Accounts Receivable  | The customer card. If no account is assigned to the customer, the system uses the account from the Sales series in the Posting Accounts Setup window.                                                              |
| Markdown             | The Inventory series in the Posting Accounts Setup window.                                                                                                                                                         |

#### Adding items

>   If Enter Non-Inventoried Items is marked in the Invoicing Setup Options
>   window and you enter an item number that doesn’t exist in inventory, you can
>   select Add Item from the Options menu in the Invoice Entry window and either
>   add the item to your inventory or choose a different item. Selecting Add
>   Item can help prevent data entry errors that inadvertently create
>   non-inventoried items.

>   If you select Add Item and enter an item that isn’t in your inventory,
>   you’ll have the option to add the item. Add Item will remain marked as long
>   as the Invoice Entry window is open. If you close the window and open it
>   again, you must select Add Item again.

#### Serial- or lot-numbered items

>   If an item is tracked by serial or lot numbers, you must identify the
>   specific item or items being sold, and you must assign the serial or lot
>   number before you ship the item.

>   Serial and lot numbers will be assigned automatically to items if you have
>   marked the Auto-Assign Serial Numbers and Auto-Assign Lot Numbers options in
>   the Invoicing Setup Options window. The serial number will be assigned
>   according to your valuation method. Lot numbers will be assigned
>   automatically by receipt date or by expiration date, depending on how you
>   select to automatically assign lot numbers in the Inventory Control Setup
>   window.

>   Lot numbers with expiration dates that haven’t expired will be used when
>   assigning lot numbers by expiration date. Lot numbers without an expiration
>   date will not be assigned. When assigning lots by receipt date, lot numbers
>   with expiration dates that haven’t expired and lot numbers without an
>   expiration date will used and the assignment will be based on the valuation
>   method. When automatically assigning lot numbers, expired lots will not be
>   used even if you’ve marked the Other Transactions option in the Inventory
>   Control Setup window. You can view or change the serial or lot numbers that
>   are assigned to an item. For more information, see *Changing a serial or lot
>   number*.

>   If the auto-assign options aren’t marked in the Invoicing Setup Options
>   window, you can enter or select a serial or lot number. When the item is
>   fulfilled, the Invoice Serial Number Entry window or the Invoice Lot Number
>   Entry window will open and you can assign the serial or lot number to the
>   item.

>   If you add a serial- or lot-numbered item to a return document, the Invoice
>   Serial Number Entry or Invoice Lot Number Entry window will open and you can
>   enter the serial or lot number for the item.

>   *Don’t override shortages on serial- and lot-numbered items. Your inventory
>   will be overstated when the quantity is replenished.*

**Chapter 4: Batches**

>   Batches are groups of transactions with something in common and identified
>   by a unique name or a number. Batches can be identified as a group of
>   transactions entered by a specific employee, or a group of transactions
>   entered on a particular date.

>   You can enter Invoicing documents individually or in batches. Individual
>   transactions are entered in the Invoice Entry window and posted immediately,
>   so your records are always up to date.

>   You can post batches of transactions using the batch, series, or master
>   posting procedures. For more information posting methods, refer to the
>   System User’s Guide (Help \>\> Contents \>\> select Using the System).

>   Batch information is divided into the following sections:

-   *Creating a batch*

-   *Modifying a batch* • *Deleting a batch*

#### Creating a batch

>   Use the Invoice Batch Entry window to create a batch. Batches can be used to
>   group and save transactions so you can review the transactions and make
>   corrections before they’re posted.

>   **To create a batch:**

1.  Open the Invoice Batch Entry window. (Transactions \>\> Sales \>\> Invoicing
    Batches)  
    

    ![A screenshot of a cell phone Description automatically generated](media/873d155296f235a43b3de1db75a2dfc6.jpg)

2.  Enter a batch ID to identify the batch.

3.  Select the batch origin and enter a batch comment.

*The Frequency field is unavailable. You must use single-use batches in
Invoicing.*

1.  Enter or accept the posting date. The user date will be the default entry
    but you can change it. This field will be available only if you marked Batch
    in the Posting Date From field in the Posting Setup window. If this field is
    unavailable, the posting date from the Invoice Date Entry window for each
    transaction will be the posting date for each transaction.

>   The date you enter is the date the General Ledger records will use.
>   Invoicing records will be updated according to the document date entered in
>   the Invoice Entry window.

>   *The General Ledger posting date applies to invoices and returns because
>   those are the only document types that are posted.*

1.  Select the Checkbook ID that will be affected by the transactions in this
    batch.

2.  You can enter the required number of transactions that must be entered
    before this batch can be posted.

3.  Enter the required currency amount for all transactions you’ll enter in this
    batch.

4.  Choose Transactions to open the Invoice Entry window.

5.  Choose Save.

6.  When you have entered all your transactions in a batch, you can choose File
    \>\> Print or the printer icon button to print an edit list.

#### Modifying a batch

Use the Invoice Batch Entry window to make changes to an unposted batch. If
you’ve approved a batch for posting, you must unmark Approved before making
changes.

**To modify a batch:**

1.  Open the Invoice Batch Entry window. (Transactions \>\> Sales \>\> Invoicing
    Batches)

2.  Enter or select a batch ID. If you enter a batch ID, you also must select
    the origin.

Make your changes and choose

#### Deleting a batch

>   Use the Invoice Batch Entry window to delete an unposted batch of documents,
>   including all transactions in the batch. If you’ve approved a batch for
>   posting, you must unmark Approved before making changes.

>   **To delete a batch:**

1.  Open the Invoice Batch Entry window. (Transactions \>\> Sales \>\> Invoicing
    Batches)

2.  Enter or select the batch ID to delete. If you enter the batch ID, you also
    must select the origin.

3.  Choose Delete.

**Chapter 5: Invoices and returns**

>   Entering and posting transactions are two of the most common routines in
>   accounting. Transactions can be saved, edited if necessary, and then posted
>   so that they become part of your permanent accounting record.

>   During posting, the balances of your customer and item accounts will be
>   updated by the amounts entered on the invoices. If your Microsoft Dynamics
>   GP system includes General Ledger, the balances of your posting accounts
>   will be updated, as well.

>   Invoice and return information is divided into the following sections:

-   *Entering an invoice*

-   *Entering a return*

-   *Adding a markdown for an item*

#### Entering an invoice

>   The Invoice Entry window contains customer, line item, and totals
>   information, much like an actual invoice. You can enter and post invoices
>   and returns using the Invoice Entry window. You also can print invoices,
>   returns, and packing slips using this window.

>   You can enter additional information about the customer, a line item, the
>   markdown, the amount received, and the terms discount taken by choosing the
>   expansion buttons next to the appropriate fields. You also can enter
>   additional information about the comment ID, the date, the batch ID, and the
>   freight, miscellaneous, and tax amounts. The following table shows the
>   windows that open with each expansion button:

| **Field**            | **Window that opens**                |
|----------------------|--------------------------------------|
| Date                 | Invoice Date Entry window            |
| Batch ID             | Invoice Batch Entry window           |
| Customer ID          | Invoice Customer Detail Entry window |
| Item Number          | Invoice Item Entry Detail window     |
| Markdown             | Invoice Markdown Entry window        |
| Amount Received      | Invoice Payment Entry window         |
| Terms Discount Taken | Invoice Payment Terms Entry window   |
| Comment ID           | Invoice Comment Entry window         |
| Freight              | Invoice Tax Schedule Entry window    |
| Miscellaneous        | Invoice Tax Schedule Entry window    |
| Tax                  | Invoice Tax Summary Entry window     |

>   **To enter an invoice:**

1.  In the navigation pane, choose the Sales button, and then choose the
    Invoicing Transactions list.

2.  Choose Invoice to open the Invoice Entry window.

3.  Select Invoice as the document type and enter a document number. The next
    document number specified in the Invoicing Setup window will be displayed.

4.  You can put a transaction on hold by marking Hold. Unmark Hold to remove a
    hold from the document if Remove Transaction Holds is marked in the
    Invoicing Setup Options window.

*If you mark Hold, the items you’ve selected will remain allocated in
inventory.*

1.  Enter the document date. This date will be used to update your invoicing
    records. To change the posting date or enter a quote or order date, choose
    the Date expansion button to open the Invoice Date Entry window.

2.  Enter or select the site ID from which the items will be sold. The site ID
    specified in the Invoicing Setup window will appear as a default site. The
    site ID will be used to allocate items from inventory and might be used to
    calculate taxes.

3.  You can create or select a batch ID to assign to the invoice.

4.  Enter or select a customer ID and enter the customer’s purchase order
    number, if there is one for this invoice. The purchase order number will be
    printed on the invoice, and will be displayed in the Invoice Inquiry window.

5.  Enter or select item numbers and enter or select a unit of measure and the
    quantity of the line item you’re selling. When you enter a quantity for an
    item, it is allocated in inventory. If you’re selling a non-inventoried
    item, enter the unit price.

6.  Enter the trade discount, freight, miscellaneous, and tax amounts for this
    invoice. The trade discount is calculated automatically if you assigned a
    trade discount to this customer when setting up the customer record. Taxes
    will be calculated automatically as you enter items.

7.  If you receive a payment from the customer, enter the amount in the Amount
    Received field. The Invoice Payment Entry window will open and you can enter
    further information about the payment, such as the payment method.

8.  To print a comment on the invoice, enter the comment ID for the comment to
    print. The comment ID you enter here will appear as the reference in the
    General Ledger Transaction Entry window. For more information, refer to
    *Adding comments to invoices and returns* .

9.  Choose Distributions to open the Invoice Distribution Entry window and
    verify or change distribution amounts.

10. Choose Commissions to open the Invoice Commissions Entry window and verify
    or change commission amounts. For more information about commissions, see
    *Modifying commission information* and *Splitting commissions*.

11. Choose Print to print the invoice. For more information about printing
    documents, see *Chapter 9, “Printing documents.”*

12. Save or post the invoice.

#### Entering a return

>   Return documents record the return of items you previously sold. Returns
>   decrease the customer’s balance on account and may increase inventory
>   quantities. Because returns record an increase to inventory and a refund of
>   sales, they should be posted. Use the Invoice Entry window to enter and post
>   returns.

>   **To enter a return:**

1.  In the navigation pane, choose the Sales button, and then choose the
    Invoicing Transactions list.

2.  Choose Return to open the Invoice Entry window.

3.  Select Return as the document type and enter a document number. The next
    document number specified in the Invoicing Setup window will be displayed.

4.  Enter the document date. This date will be used to update your invoicing
    records. To change the posting date or enter a quote or order date, choose
    the Date expansion button to open the Invoice Date Entry window.

5.  Enter or select the site ID to which the items will be returned.

6.  You can create or select a batch ID to assign to the return.

7.  Enter or select a customer ID and enter the customer’s purchase order
    number, if there is one for this return. The purchase order number will be
    printed on the return, and will be displayed in the Invoice Inquiry window.

8.  Enter or select item numbers, and enter or select a unit of measure and the
    quantity of the line item being returned. If you’re selling a
    non-inventoried item, enter the unit price.

>   If Override Price is marked in the Invoicing Setup Options window, you can
>   change the unit price and extended price. If you’re decreasing the unit
>   price below the unit cost, you also must have the Enter Price Below Cost
>   option marked.

1.  When you enter a quantity, the Invoice Returned Quantities Entry window will
    open and you can specify which site the items will be returned to. You also
    can specify the quantity type for the returned items—on hand, returned, in
    use, in service, or damaged.

>   IMAGE: INVRQE.jpg

![A screenshot of a cell phone Description automatically generated](media/a583ab85a5fd23a26953e229a8e6af98.jpg)

>   The item will be returned automatically at the current cost. If the Override
>   Item Unit Cost for Returns option is marked in the Invoicing Setup Options
>   window, you’ll be able to change the cost.

>   *If you return an item to a return quantity type other than On Hand, you
>   can’t resell the item. You must transfer the item to On Hand before it can
>   be sold again. If the item was returned to the Damaged quantity type, to
>   return the item to the vendor, you must transfer the item to On Hand and
>   then enter a decrease adjustment for the item. For more information, refer
>   to the Inventory Control documentation.*

1.  If applicable, enter the trade discount, freight, miscellaneous, and tax
    amounts for this return. Taxes will be calculated automatically as you enter
    items.

2.  If you’ve entered payment terms for this customer that allow a discount for
    the sale, and if a payment was made at the time of the sale, enter the
    discount returned amount in the Discount Returned field.

3.  To print a comment on the invoice, enter the comment ID for the comment to
    print. The comment ID you enter here will appear as the reference in the
    General Ledger Transaction Entry window.

4.  Choose Distributions to open the Invoice Distribution Entry window and
    verify or change distribution amounts.

5.  Choose Commissions to open the Invoice Commissions Entry window and verify
    or change commission amounts. For more information about commissions, see
    *Modifying commission information* and *Splitting commissions*.

6.  Choose Print to print the invoice. For more information about printing
    documents, see *Chapter 9, “Printing documents.”* 16. Save or post the
    return.

#### Adding a markdown for an item

>   Use the Invoice Markdown Entry window to enter a markdown for an individual
>   line item. A markdown is a price reduction and can be a set amount or a
>   percentage of the item price.

>   **To add a markdown for an item:**

1.  Open the Invoice Markdown Entry window. (Transactions \>\> Sales \>\>
    Invoice Entry \>\> Markdown expansion button)

>   IMAGE - INVME.jpg

![](media/e8b31efbbf5a1cb8bd7b002f0abe02d3.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Mark the markdown type—percentage or amount—and enter the percentage or
    amount. The unit price, markdown amount, adjusted unit price and the revised
    extended price are displayed.

2.  Choose OK. The markdown amount and the revised extended price are displayed
    in the Invoice Entry window.

3.  Choose Save.

**Chapter 6: Invoicing taxes**

>   Sales tax can be calculated, modified, and distributed in Invoicing. Use the
>   Invoice Tax Summary Entry window to view tax distributions and to change
>   distribution accounts, if your system is set up to allow editing
>   summary-level taxes. To change tax details or the amounts distributed to tax
>   details for individual line items, use the Invoice Line Item Tax Detail
>   Entry window.

>   Tax information is divided into the following sections:

-   *Invoicing tax calculations*

-   *Calculating and distributing tax amounts*

-   *Goods value and net purchase amount*

#### Invoicing tax calculations

>   Taxes are automatically calculated for a document. When you set up
>   Invoicing, you can choose to use a single tax schedule for all items on all
>   documents or you can mark the advanced option to determine the tax for
>   inventory items, noninventoried items, freight, and miscellaneous charges
>   individually.

>   If you mark the advanced option, the tax is calculated for each item on the
>   document. Here are the components of the calculation if you use an advanced
>   tax schedule in Invoicing:

>   **Item** The tax option for each item on the invoice is used. To view the
>   tax option for an item, choose the Item Number expansion button in the
>   Invoice Entry window to open the Invoice Item Detail Entry window.

-   If the tax option for the item is Nontaxable, no tax is calculated for that
    item.

-   If the tax option for the item is Taxable, the tax schedule for the line
    item is taken from the Item Maintenance window and compared to the shipping
    method tax schedule ID to calculate taxes.

-   If the tax option for the item is Base on customers, the line item’s tax
    schedule from the Customer Maintenance window is used.

>   **Shipping method** The shipping method specified in the Ship To Address
>   field in the Invoice Customer Detail Entry window for the customer will be
>   used, if your system is set up to use the shipping method in tax
>   calculations. For more information on this option, see the System Setup
>   Guide (Help \>\> Contents \>\> select Setting up the System).

>   To view the shipping method used for a document, choose the customer ID
>   expansion button in the Invoice Entry window to open the Invoice Customer
>   Detail Entry window.

-   If the shipping method is Pickup, the tax schedule from the Site ID on the
    document is used.

-   If the shipping method is Delivery, the tax schedule from the Ship To
    Address for the customer is used.

Any common details between the two tax schedules—the tax schedule for the item
and either the tax schedule for the ship-to address or the schedule for the
site—will be the tax details used to calculate the tax for the item.

To view the tax calculation for an item, choose the Item Number expansion button
to open the Invoice Item Detail Entry window. Then choose the Calculated Tax
expansion button to open the Invoice Line Item Tax Detail Entry window.

#### Calculating and distributing tax amounts

Sales tax can be calculated, modified, and distributed in Invoicing. Use the
Invoice Tax Summary window to view tax distributions and to change distribution
accounts.

Sales Order Processing and Invoicing are not integrated and do not share sales
information. If you use Invoicing to enter transactions, you won’t be able to
view those transactions in the Sales Order Processing inquiry windows or on
Sales Order Processing analysis reports.

If you’re using VAT (Value-Added Tax), you also can use the Invoice Line Item
Tax Detail Entry window to calculate, modify, and distribute input tax amounts
for shipment/invoice receipts.

>   **To calculate and distribute tax amounts:**

1.  Open the Invoice Entry window. (Transactions \>\> Sales \>\> Invoice Entry)

2.  Enter document information, including the document number, the document
    date, and the site ID.

>   Choose the Date expansion button to open the Invoice Date Entry window where
>   you can enter a tax date and posting date that differ from the document
>   date. The tax date you enter is the date your tax records will be updated.

1.  Enter or select a customer ID.

>   *Mark the EU Transaction option in the Invoice Customer Detail Entry window
>   to record statistics for a customer.*

1.  Enter line item information. To change either the price of a line item or
    the tax amount, choose the Item Number expansion button to open the Invoice
    Item Detail Entry window.

2.  Enter total information. The output tax is calculated on the net sale
    amount, which includes freight and miscellaneous charges, if taxable, and
    any trade discount.

3.  Choose the Calculated Tax expansion button in the Invoice Item Detail Entry
    window to open the Invoice Line Item Tax Detail Entry window and enter or
    select other tax details.

>   The tax amount is based on the output tax detail on each item’s assigned tax
>   schedule. You can change the percentage assigned to an existing tax detail
>   using the Tax Detail Setup window.

>   Choose the Tax expansion button in the Invoice Entry window to open the
>   Invoice Tax Summary Entry window and view the amount of output tax that is
>   distributed to each tax detail.

>   If Allow Summary-Level Tax Edits is marked in the Company Setup window, you
>   can use this window to change the Tax Detail ID, Total Sale, Tax Amount, and
>   Account fields. If Allow Summary-Level Tax Edits is not marked, use the you
>   can use Invoice Line Item Tax Detail Entry window to change the distribution
>   amounts.

#### Goods value and net purchase amount

>   The goods value is the same as the net purchase amount, which includes
>   freight and miscellaneous charges if taxable and any trade discount. If
>   several different tax details are used for a transaction, you must
>   distribute the total goods value amount to all appropriate tax details and
>   enter the tax in the Tax Amount field in the Invoice Tax Summary Entry
>   window. This requirement applies even if no tax will be paid on the entire
>   transaction or on individual items included on the transaction.

>   For example, you’re entering a purchase amount of £500. However, £250 of
>   this purchase is exempt from tax. To distribute the exempt portion of the
>   transaction, enter or select the appropriate tax-exempt detail. Then, enter
>   a goods value of £250 for the tax-exempt detail and the remaining taxable
>   goods value of £250 for the input tax detail. The tax amount automatically
>   will be adjusted to reflect the reduction in the taxable goods value.

**Chapter 7: Allocating item quantities**

>   When you allocate an item, it is reserved in inventory and the quantity
>   available for the item and for the site is reduced in inventory. You must
>   allocate items before you can fulfill them.

>   Allocation information is divided into the following sections:

-   *Quantity shortage options*

-   *Selling an item from another site*

-   *Substituting an item*

#### Quantity shortage options

>   A quantity shortage occurs when the quantity on an invoice is greater than
>   the quantity available in inventory. If there is a quantity shortage, the
>   Invoice Quantity Shortage Options window will open and you can choose how to
>   treat the quantity shortage—sell balance, override, or other options.

>   **Sell Balance** Mark to allocate the quantity available in inventory for
>   the site to the document. For example, if you entered 5 for the quantity on
>   an invoice but have 3 available in inventory, the quantity is set to 3. The
>   quantity available in inventory for the item is now zero.

>   **Override** Mark to ignore the shortage and sell the entire quantity. The
>   quantity available in inventory will be negative.

>   *Do not override a shortage on an item that is tracked by serial or lot
>   numbers. Your inventory will be overstated when the quantity is
>   replenished.*

>   **Other options** Mark and choose Options to open the Invoice Quantity

>   Distribution Entry window, where you can sell items from another site or
>   substitute items. For more information, see *Selling an item from another
>   site* or *Substituting an item*.

#### Selling an item from another site

Use the Invoice Quantity Distribution Entry window to check the quantity
available at other sites and allocate the item from other sites if there is a
quantity shortage for the item at the default site.

>   **To sell an item from another site:**

1.  Open the Invoice Quantity Distribution Entry window. (Transactions \>\>
    Sales \>\> Invoice Entry \>\> enter a quantity greater than the available
    inventory quantity \>\> mark Other Options \>\> Options button)

IMAGE - INVQDE.jpg

![](media/66dd8e2d7a25c58f2c1efbeb54c24f1b.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Change the Site ID.

2.  If there is a quantity available for a site in the Available Quantities
    window, enter the quantity needed for the document in the Quantity Selected
    field.

3.  Choose Insert. An entry will appear in the Selected Quantities section of
    the window.

4.  Repeat steps 2 through 4 to fill the quantity needed. The Extended Quantity
    Selected must equal the Original Item Extended Quantity.

5.  Choose OK to close the window and save your entries.

#### Substituting an item

>   Use the Substitute Items window to choose a substitute item if there is a
>   quantity shortage for an item and the default site. Substitute items must be
>   set up in inventory and you can set up two substitute items for an inventory
>   item. For more information about substitute items, see the Inventory Control
>   documentation.

>   **To substitute an item:**

1.  Open the Invoice Quantity Distribution Entry window. (Transactions \>\>
    Sales \>\> Invoice Entry \>\> enter a quantity greater than the inventory
    quantity available \>\> select Other Options \>\> Options button)

2.  Choose the Item Number expansion button to open the Substitute Items window.
    Select a substitute item and choose OK.

3.  In the Invoice Quantity Distribution Entry window, verify the quantity
    available for the substitute item. Enter the quantity needed for the
    document in the Quantity Selected field.

4.  Choose Insert. The item number will appear in the Selected Quantities
    window.

5.  Repeat steps 2 through 4 to choose an additional substitute item or site to
    fill the quantity needed. The Extended Quantity Selected must equal the
    Original Item Extended Quantity.

6.  Choose OK to close the window and save your entries.

Part 3: Transaction activity
============================

>   This part of the documentation includes information that will help manage
>   your invoicing documents once they are entered. You can transfer, modify,
>   delete, post, and print invoicing documents.

>   The following information is discussed:

-   *Chapter 8, “Invoicing document maintenance,”* explains how to correct,
    delete, and void invoicing documents.

-   *Chapter 9, “Printing documents,”* explains how to print a quote, order,
    invoice, back order, or return, and send it to a customer. You also can
    print packing slips, picking tickets, shipping labels and cash on delivery
    (COD) tags.

-   *Chapter 10, “Posting,”* describes how to transfer transactions to permanent
    records and how to transfer the original transaction information to history.

Chapter 8: Invoicing document maintenance
-----------------------------------------

>   Before you transfer or post an invoice, you can modify the item, commission,
>   and total information. For example, you can change quantities, add items,
>   correct addresses, split commissions, or add freight charges. If the invoice
>   was entered in error, you can delete the invoice.

>   Invoicing document maintenance information is divided into the following
>   sections:

### • *Adding comments to invoices and returns*

-   *Changing a serial or lot number*

-   *Modifying commission information*

-   *Splitting commissions*

-   *Correcting an invoicing document*

-   *Deleting an invoicing document*

-   *Entering Intrastat statistics*

**Adding comments to invoices and returns**

>   You can add comments to invoices, returns, or to individual line items on
>   these documents. You also can define standard comments on a company-wide
>   basis, and those used on Sales Order Processing, Invoicing, or Purchase
>   Order Processing documents.

>   *Only the first 200 characters of a line item comment will appear on an
>   invoice or return. For longer comments to appear, use Report Writer to
>   modify the default document layouts.*

>   You can enter or select the ID of a predefined comment in the Invoice Entry
>   window or Invoice Item Detail Entry window and can create new comments while
>   you are entering transactions. You also can create custom comments for a
>   particular document or line item, or modify existing comments. One-time
>   comments or modified comments won’t be available for other documents or line
>   items.

>   **To create a new comment:**

1.  Open the Comment Setup window.

>   (Transactions \>\> Sales \>\> Invoice Entry \>\> enter a new Comment ID
>   value \>\> press TAB or ENTER \>\> Add button)

1.  Select the Sales series.

2.  Enter the comment text.

3.  Choose Save, then close the Comment Setup window.

>   **To create a one-time comment:**

1.  Open the Invoice Comment Entry window.

>   (Transactions \>\> Sales \>\> Invoice Entry \>\> Comment ID expansion
>   button)

1.  If the Comment ID field contained a value, you’ll be able to modify the
    existing comment. If the Comment ID field was blank, you’ll be able to
    create a new, one-time comment.

2.  Enter or change the comment text.

3.  Choose OK.

### Changing a serial or lot number

>   You can verify or change the serial or lot number assigned to an item before
>   the sale is posted.

>   **To change a serial or lot number:**

1.  Open the Invoice Entry window.

>   (Transactions \>\> Sales \>\> Invoice Entry)

1.  Enter or select a serial- or lot-numbered item, then choose the Item Number
    expansion button.

2.  In the Invoice Item Detail Entry window, choose Serial/Lot.

3.  Select the serial or lot number in the Selected list to change and choose
    Remove.

4.  From the list of available serial or lot numbers, select one to use. If you
    selected a lot number, also enter a quantity. Choose Insert.

>   You can also enter a serial or lot number that hasn't been entered. To do
>   so, enter the number in the Serial Number or Lot Number field and choose
>   Insert.

>   *A warning icon appears in the Lot Number field if you select a lot number
>   that has expired.*

1.  Choose OK to save your changes and close the window.

2.  Save your changes and close the Invoice Item Detail Entry window.

### Modifying commission information

>   Use the Invoice Commission Entry window to modify commission amounts,
>   percentages and commission sales amounts on invoices and returns. The
>   commission amounts will be posted when the transaction is posted.

>   Commission amounts on invoicing documents are calculated using the
>   commission information from the Salesperson Maintenance window. Commission
>   amounts on return documents will decrease the commissions payable to a
>   salesperson. For more information about the Salesperson Maintenance window,
>   refer to the Receivables Management documentation.

>   **To modify commission information:**

1.  Open the Invoice Commission Entry window. (Transactions \>\> Sales \>\>
    Invoice Entry \>\> enter or select an item number \>\> Commissions button)

>   IMAGE - INVCOME.jpg

![](media/889aa564c305239ce95705b11812c921.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Choose the hide and show button to expand the scrolling window.

2.  Make your changes to the commission information. You also can enter or
    select a different salesperson ID.

*To remove a commission distribution, select the line and choose Edit \>\>
Delete Row.*

1.  Choose OK to save changes and close the window.

### Splitting commissions

>   You can split the commission on invoices and returns among multiple
>   salespeople. Use the Invoice Commission Entry window to split commissions.
>   Commission amounts on return documents will decrease the commissions payable
>   to a salesperson.

>   **To split commissions:**

1.  Open the Invoice Commission Entry window. (Transactions \>\> Sales \>\>
    Invoice Entry \>\> enter or select an item number \>\> Commissions button)

2.  Choose the hide and show button to expand the scrolling window.

3.  Change the Percent of Sale amount to the appropriate percentage for the
    first salesperson listed.

4.  In the next available line, enter or select an additional salesperson. Enter
    an amount in the Percent of Sale and Commission Sale Amount fields for the
    additional salesperson. The Commission amount will be calculated
    automatically.

5.  Choose OK to save the changes and close the window.

### Correcting an invoicing document

>   You can correct mistakes in Invoicing transactions before posting. As you
>   enter transactions, you can print a variety of reports that allow you to
>   double-check the information you’ve entered. When you identify errors on
>   these reports, the errors must be corrected to ensure accurate reporting of
>   your sales activity.

>   *You can change invoices that have been printed only if Edit Printed
>   Documents is marked in the Invoicing Setup Options window.*

>   You can’t correct a transaction that has been posted. If the transaction has
>   been posted, you must enter a transaction to reverse the
>   original—incorrect—transaction. Then you can enter the transaction
>   correctly.

>   **To correct an invoicing document:**

1.  Open the Invoice Entry window. (Transactions \>\> Sales \>\> Invoice Entry)

2.  Select the transaction.

3.  Highlight the field to change and enter the correct information.

4.  Choose Save.

### Deleting an invoicing document

>   When you delete an invoice, all the items on that invoice will be
>   unallocated in inventory, if Inventory Control is part of your Microsoft
>   Dynamics GP system. If Track Voided Transactions in History is marked in the
>   Invoicing Setup window, a voided document will be transferred to your
>   company’s historical records.

>   You can’t delete an invoice or return if:

-   The invoice has been posted.

-   The document is in a batch that is being processed.

-   Void Documents isn’t marked in the Invoicing Setup Options window.

-   The document is on hold.

>   **To delete an invoicing document:**

1.  In the navigation pane, choose the Sales button, and then choose the
    Invoicing Transactions list.

2.  Mark the invoice or return.

3.  Choose Delete.

### Entering Intrastat statistics

>   Intrastat is the system for collecting statistics on the trade of goods
>   between European Union (EU) countries. Intrastat data is required for all
>   items either bought from EU vendors or sold to EU customers, and must be
>   provided on a monthly basis. Requirements for Intrastat are similar in all
>   EU countries. The government uses these statistics as an economic indicator.

>   For information on setting up Intrastat codes, see the System Setup Guide
>   (Help \>\> Contents \>\> select Setting up the System).

>   Use the Invoice Intrastat Entry window to enter the information required to
>   create the Intrastat Trade Report you submit to your government, and the EC
>   Sales List, which displays cumulative goods value totals by each vendor or
>   customer Tax Registration number. You can enter Intrastat statistics for
>   each line item.

>   If Intrastat information was entered for the customer’s ship to address ID,
>   that information appears in this window. You can use the Invoice Intrastat
>   Entry window to change Intrastat information for an individual transaction,
>   or to enter Intrastat information if none was entered for the customer.

>   *You can enter Intrastat statistics only if Enable Intrastat Tracking is
>   marked in the Company Setup Options window.*

>   **To enter Intrastat statistics:**

1.  Open the Invoice Entry window. (Transactions \>\> Sales \>\> Invoice Entry)

2.  Enter the EU transaction, including the customer ID and the goods value.

3.  Choose the Item EU expansion button to open the Invoice Intrastat Entry
    window. If this button is unavailable, choose the Customer ID expansion
    button to open the Invoice Customer Detail Entry window and mark EU
    Transaction.

>   If the country/region code assigned to the customer’s shipping address is
>   designated an EU country, this is marked automatically.

IMAGE - INVINE.jpg

![A screenshot of a cell phone Description automatically generated](media/56c495143606260b358edb18bdab928f.jpg)

1.  Enter Intrastat information, or change the default entries, if necessary.

2.  In the Net Unit Mass field, enter the weight of the goods in kilograms.

>   The item’s shipping weight from the Item Maintenance window is the default
>   weight. You can change this information.

1.  The line mass displays the total mass per item and is calculated by
    multiplying the amount entered in the Net Unit Mass field by the amount
    displayed in the Quantity field.

2.  Enter a supplementary units amount, if applicable. The supplementary units
    amount is simply a second quantity. Supplementary units amounts are required
    by the EU Combined Nomenclature for certain goods.

3.  In the Traders Reference field, enter a reference code, such as an invoice
    or dispatch number, or any other information that will identify the
    transaction.

4.  Choose OK to save the record.

Chapter 9: Printing documents
-----------------------------

>   After you enter a quote, order, invoice, back order, or return, you can
>   print the document and send it to a customer. You also can print packing
>   slips, picking tickets, shipping labels and cash on delivery (COD) tags.

>   Information about printing documents is divided into the following sections:

-   *Printing options*

-   *Printing an individual document*

-   *Printing all documents in a batch*

-   *Printing a posted document*

-   *Printing invoice labels*

### Printing options

>   When you print an invoice or return, you can choose the Options menu in the
>   Invoice Entry window or the Invoice Batch Entry window to select several
>   printing options.

>   **Document Format** Opens the Invoice Document Formats window where you can
>   change the document format used to print invoices, returns and packing
>   slips.

>   **Print Invoice or Return** Prints invoice or return documents in the
>   Invoice Entry window and prints a batch of invoice or return documents in
>   the Invoice Batch Entry window.

>   **Print Packing Slip** Prints a packing slip for each invoicing document.

>   **Include Tax Details on Doc.** Prints the tax details and tax amount for
>   each item and prints the total tax amount for each detail after the last
>   item.

>   **Print Alignment Form** Prints an alignment form before you print
>   documents, to ensure that the information is printed in the correct fields
>   on the document.

### Printing an individual document

>   You can print a single invoice or return when you enter the document in the
>   Invoice Entry window. Before you print documents, you can print an alignment
>   form to ensure that the information is printed in the correct fields on the
>   document. You can use four predefined document formats to print
>   documents—blank paper, short form, long form, or other form.

>   You also can print a packing slip at the same time as you print the
>   invoicing document.

*Choose Options \>\> Document Format to change the document format used to print
the invoice, return, or packing slip.*

>   **To print an individual document:**

1.  Open the Invoice Entry window.

>   (Transactions \>\> Sales \>\> Invoice Entry)

1.  Enter or select a document.

2.  Choose Options \>\> Print Packing Slip to print a packing slip when the
    invoice or return is printed.

3.  Choose Options \>\> Include Tax Details on Doc. to include tax details on
    the invoice or return.

4.  Choose Options \>\> Print Alignment Form to print an alignment form.

>   *If a tax detail doesn’t appear on a document, check the Tax Detail
>   Maintenance window. The Print on Documents option must be marked.*

1.  Choose Print.

### Printing all documents in a batch

>   You can print all of the documents in a batch using four predefined document
>   formats to print documents—blank paper, short form, long form, or other
>   form. You also can print packing slips at the same time as you print the
>   documents.

>   You can print an alignment form to ensure that the information is printed in
>   the correct fields on the document.

>   **To print all documents in a batch:**

1.  Open the Invoice Batch Entry window.

>   (Transactions \>\> Sales \>\> Invoicing Batches)

1.  Select a batch.

2.  Choose Options \>\> Document Format to change the document format used to
    print the invoice, return, or packing slip.

3.  Choose Options \>\> Print Packing Slip to print a packing slip when the
    invoice or return is printed.

4.  Choose Options \>\> Include Tax Details on Doc. to include tax details on
    the invoice or return.

5.  Choose Options \>\> Print Alignment Form to print an alignment form.

>   *If a tax detail doesn’t appear on a document, be sure Print on Documents is
>   marked in the Tax Detail Maintenance window.*

1.  Choose a sorting option.

2.  Choose Print.

### Printing a posted document

>   You can reprint individual invoicing documents from historical records.
>   Documents are moved to history when they are posted or voided. You can’t
>   reprint packing slips for documents that have been moved to history.

>   You can print an alignment form to ensure that the information is printed in
>   the correct fields on the document. To print an alignment form, choose
>   Options and mark the Alignment Form option. You can use four predefined
>   document formats to print documents—blank paper, short form, long form, or
>   other form.

>   *If you modified the invoicing document in Report Writer, your changes will
>   not appear when you print a posted document because a different report is
>   used to print posted documents.*

>   **To print a posted document:**

1.  Open the Invoicing Document Inquiry window. (Inquiry \>\> Sales \>\>
    Invoice)

2.  Select a sorting option or a range of documents.

3.  Mark to include History and choose Redisplay.

4.  Highlight a document and click the Document Number link to open the Invoice
    Inquiry window.

5.  Choose Print.

### Printing invoice labels

>   Use the Mailing Labels window to print invoice labels for a range of
>   unposted transactions in Invoicing. You can print labels for invoices and
>   can select a range by batch, document ID, state, ZIP or postal code,
>   customer, or date.

>   **To print invoice labels:**

1.  Open the Mailing Labels window.

>   (Reports \>\> Company \>\> Mailing Labels)

1.  Select Invoice Labels from the Reports list and choose New to open the
    Mailing Label Report Options window.

2.  Enter or select an option name.

3.  Mark a format to use, select the number across and number of copies to be
    printed.

*If you mark Laser, the labels will be printed two across.*

1.  Mark the address to be used, select sorting options and enter restrictions.

2.  Choose Destination to select a printing destination.

3.  Choose Print. You can save the report option and print it later from either
    the Mailing Labels window or the Mailing Label Report Options window.

Chapter 10: Posting
-------------------

>   Posting is the process of transferring transactions to permanent records. If
>   you need to change or delete a transaction, you must do so before posting
>   the transaction.

>   When you post Invoicing transactions, transaction information is transferred
>   to other parts of your financial records. Quantity information for items,
>   the balances of customer accounts, and the balances of the posting accounts
>   in your chart of accounts are updated. Transaction information becomes part
>   of an open fiscal year’s permanent records.

>   Posting also transfers the original transaction information to history, so
>   you can later review individual transactions and print reports of historical
>   activity.

>   Posting reports will be printed when you post transactions, either
>   individually or in batches. For more information about posting reports for
>   Invoicing, refer to *Invoicing report summary*.

>   For more information about setting up posting, see the System Setup Guide
>   (Help \>\> Contents \>\> select Setting up the System).

>   *Some Invoicing setup options affect posting and history. For more
>   information, see Setting Invoicing general options and defaults .*

>   Posting information is divided into the following sections:

-   *Posting an individual transaction*

-   *Posting transactions for the Sales series*

-   *Posting transactions in all modules*

### Posting an individual transaction

>   Transaction-level posting allows you to enter and post transactions without
>   ever having to create a batch. Sales and inventory information will be up to
>   date when you post using this method, because transactions are posted or
>   deleted immediately. They can’t be saved and posted later. Also, you can’t
>   post to a year that hasn’t been set up in the Fiscal Periods Setup window.

>   Transaction-level posting is optional and can be selected in the Posting
>   Setup window when you set up Microsoft Dynamics GP. If your system has been
>   set up to allow transaction-level posting, you’ll be able to enter and post
>   transactions directly from the Invoice Entry window. If your system doesn’t
>   allow individual transaction entry, you’ll need to create a batch before you
>   save transactions.

>   When you post transactions individually, the posting date will be the same
>   as the transaction date used to make the entry, but can be changed in the
>   Invoice Date Entry window. If you’re posting using the transaction date and
>   transaction-level posting isn’t allowed, the document date will be used as
>   the posting date. All transactions posted individually in a single data
>   entry session will have the same audit trail code.

>   **To post an individual transaction:**

1.  Open the Invoice Entry window.

>   (Transactions \>\> Sales \>\> Invoice Entry)

1.  Enter or select a transaction. For new transactions, leave the Batch ID
    field blank. For existing transactions that were previously entered in a
    batch, clear the Batch ID field.

2.  Choose Post to post the transaction.

3.  Close the window. The Invoicing Posting Journal will be printed if you chose
    to print this audit trail report when you set up Microsoft Dynamics GP.

>   *When you post transactions individually, your user ID will appear on
>   reports as a batch ID.*

### Posting transactions for the Sales series

>   Use the Sales Series Posting window to post transactions for the Sales
>   series.

>   You can require that a password be entered before batches can be posted. The
>   options to approve batches for posting and to require passwords before
>   posting will be available only if you’ve marked the Require Batch Approval
>   option and entered a batch approval password using the Posting Setup window.

>   Depending on the selections that you made in the Invoice Batch Entry window
>   and Posting Setup window, you may not be able to post a batch until you’ve
>   entered a specific number of transactions or transactions that total a
>   certain amount. For more information about batch status and setting batch
>   requirements, see *Creating a batch*.

>   **To post transactions for the Sales series:**

1.  Open the Sales Series Posting window. (Transactions \>\> Sales \>\> Series
    Post)

>   IMAGE – INVSALP.jpg

![](media/5707e44a41ccfca2721eb419bc1db795.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Set display options. You can display all Sales series batches or only those
    that have been marked. Choose the show button to display information about
    the user who created or last marked a batch for posting, comments entered
    for each batch, and additional information.

>   *If you’re using* Microsoft Dynamics GP *on a network, choose Redisplay to
>   show any batches that have been added or changed by your coworkers since you
>   opened the window. If a batch was marked previously, the User column
>   identifies the person who marked it. To post that batch, unmark it and mark
>   it again so the batch is assigned to you. The series posting method allows
>   you to post only those batches that you’ve marked.*

1.  To mark a batch for posting, mark the box in the Batch ID column. The batch
    status column displays the current status of each batch. For more
    information about batch requirements and approval options, refer to the
    System User’s Guide (Help \>\> Contents \>\> select Using the System).

>   *You might not have posting privileges for all batch types in Invoicing,
>   depending on how security has been set up for your Microsoft Dynamics GP
>   system.*

1.  Choose Post to post the selected batches.

>   If you’ve entered batch total requirements or batch approval requirements in
>   Invoicing and posted a batch through General Ledger, the batch will be
>   posted through regardless of the batch requirement or approval requirements
>   that you’ve selected in General Ledger. For more information about posting
>   to or through General Ledger, see the System Setup Guide (Help \>\> Contents
>   \>\> select Setting up the System).

1.  Print the posting journals. Depending on the settings you made in the
    Posting Setup window, posting journals and distribution breakdown registers
    may be printed when the series posting process is complete.

### Posting transactions in all modules

>   You can post batches from any Microsoft Dynamics GP modules you have in
>   addition to Invoicing using master posting. When you use the master posting
>   process, all batches marked for posting, in all modules, will be posted
>   regardless of who marked them. Master posting is an excellent way to update
>   all the records in the Microsoft Dynamics GP system at the same time.

>   You can require that a password be entered before batches can be posted. The
>   options to approve batches for posting and to require passwords before
>   posting will be available only if you’ve marked the Require Batch Approval
>   option and entered a batch approval password using the Posting Setup window.

>   **To post transactions in all modules:**

1.  Open the Master Posting window. (Microsoft Dynamics GP menu \>\> Tools \>\>
    Routines \>\> Master Posting)

>   IMAGE – INVMP.jpg

![](media/496f5b7262fb001a23d01d1c21a3fa4d.jpg)

>   A screenshot of a cell phone Description automatically generated

1.  Set display options. You can list batches by batch ID, origin, or frequency.
    You also can display all batches, those that have been marked, or those for
    a specific series.

2.  To mark a batch for posting, mark the box in the Batch ID column. The batch
    status column displays the current status of each batch. For more
    information about batch requirements and approval options, refer to the
    System User’s Guide (Help \>\> Contents \>\> select Using the System).

3.  Choose Post to post the selected batches.

4.  Print the posting journals. Depending on the settings you made in the
    Posting Setup window, posting journals and distribution breakdown registers
    may be printed when the series posting process is complete.

Part 4: Inquiries, reports, and utilities
=========================================

>   This part of the documentation explains how to use inquiries and reports to
>   analyze your invoicing activity. You can analyze transaction and item
>   information, and display the information either on the screen or on a
>   printed report.

>   This part of the documentation also explains how to remove historical
>   information when it’s no longer useful and print reports to create a
>   permanent record of the information stored in history.

>   The following information is discussed:

-   *Chapter 11, “Inquiries,”* explains how to use Invoicing inquiry windows to
    view document and item information.

-   *Chapter 12, “Reports,”* describes how to use reports to analyze invoicing
    activity.

-   *Chapter 13, “History removal,”* explains how to remove Invoicing and
    Intrastat statistics information when it’s no longer useful.

Chapter 11: Inquiries
---------------------

>   Use the Invoice inquiry windows to view detailed or summarized Invoicing
>   information. You can view invoice, item, and salesperson activity, as well
>   as unposted transactions or historical records that have been maintained.

>   *You can’t make changes to transactions in inquiry windows. To change
>   unposted transactions, use the Invoice Entry window. For more information,
>   see Correcting an invoicing document.*

>   You can open other windows from the Invoicing inquiry windows and view
>   information as it was entered originally. For example, you can select a
>   document number in the Invoicing Document Inquiry window and open the
>   Invoice Inquiry window to view the transaction as it was entered, including
>   distribution and commission information.

>   Inquiry information is divided into the following sections:

-   *Viewing invoicing documents*

-   *Viewing invoicing items*

-   *Viewing salesperson commissions*

-   *Viewing invoices*

### Viewing invoicing documents

>   Use the Invoicing Document Inquiry window to view unposted or historical
>   documents. You can use the information to answer customers’ questions about
>   invoices they’ve received, for example.

>   You can limit the number of documents to view by selecting a range of
>   documents. For each document selected, you can view the document
>   type—invoice or return— document number, document date, customer ID,
>   document subtotal, other charges, and the document total.

>   **To view invoicing documents:**

>   Open the Invoicing Document Inquiry window. (Inquiry \>\> Sales \>\>
>   Invoice)

1.  Select a sorting option for the information in the Documents field.

2.  To display a range of information, mark From and specify the start and end
    of the range. The type of range varies depending on the sorting option you
    select.

3.  Mark Unposted to display unposted transactions or mark History to display
    transactions in history.

4.  Choose Redisplay to update the window with your selections.

5.  To find documents associated with a particular document number, customer ID,
    or date, choose Find.

6.  To open a window where you can view more detailed information about a
    particular invoice or customer, highlight a document, then click the
    Document Number or Customer ID link.

### Viewing invoicing items

Use the Invoicing Item Inquiry window to view all the documents on which a
particular item is found. This can be helpful to target sales promotions to
customers who have bought a particular item, for example.

You can limit the number of items displayed by specifying a range of items. For
each item, you can view the type and number for each document that each item
appears on, the customer IDs for the customer that each item has been sold to,
and the item number, units of measure, quantity, and extended price for each
document.

**To view invoicing items:**

1.  Open the Invoicing Item Inquiry window. (Inquiry \>\> Sales \>\> Invoiced
    Items)

2.  Select a sorting option for the information in the Items field.

3.  To display a range of information, mark From and specify the start and end
    of the range. The type of range varies depending on the sorting option you
    select.

4.  Mark Unposted to display unposted transactions or mark History to display
    transactions in history.

5.  Choose Redisplay to update the window with your selections.

6.  To find documents associated with a particular document type, document
    number, or item number, choose Find.

7.  To open a window where you can view more detailed information about a
    particular invoice, customer, or item, select an item, then click the
    Document Number, Customer ID, or Item Number link.

### Viewing invoicing items

Use the Invoicing Item Inquiry window to view all the documents on which a
particular item is found. This can be helpful to target sales promotions to
customers who have bought a particular item, for example.

You can limit the number of items displayed by specifying a range of items. For
each item, you can view the type and number for each document that each item
appears on, the customer IDs for the customer that each item has been sold to,
and the item number, units of measure, quantity, and extended price for each
document.

**To view invoicing items:**

1.  Open the Invoicing Item Inquiry window. (Inquiry \>\> Sales \>\> Invoiced
    Items)

2.  Select a sorting option for the information in the Items field.

3.  To display a range of information, mark From and specify the start and end
    of the range. The type of range varies depending on the sorting option you
    select.

4.  Mark Unposted to display unposted transactions or mark History to display
    transactions in history.

5.  Choose Redisplay to update the window with your selections.

6.  To find documents associated with a particular document type, document
    number, or item number, choose Find.

7.  To open a window where you can view more detailed information about a
    particular invoice, customer, or item, select an item, then click the
    Document Number, Customer ID, or Item Number link.

### Viewing salesperson commissions

>   Use the Salesperson Inquiry window to view information about commissions and
>   sales for salespeople. This can be helpful for evaluating the performance of
>   your sales force.

>   You can limit the records displayed by specifying a range of salesperson
>   IDs. The following information is available for each salesperson: sales
>   territory, document numbers for invoices associated with the salesperson,
>   audit trail codes for the documents, sales amounts, non-commission amounts,
>   commission percentages, and commission amounts.

>   **To view salesperson commissions:**

1.  Open the Salesperson Inquiry window. (Inquiry \>\> Sales \>\> Salesperson)

2.  Select Invoicing in the Module field.

3.  Select a sorting option for the information in the Salespeople field.

4.  To display a range of information, mark From and specify the start and end
    of the range. The type of range varies depending on the sorting option you
    select.

5.  Choose Redisplay to update the window with your selections.

6.  To find salespeople associated with a particular salesperson ID, sales
    territory ID, document number, or audit trail code, choose Find.

>   To view more information about the salesperson, territory, or invoice in the
>   list, highlight a record and click a link to open a window displaying the
>   original record.

The following table lists the link fields in the Salesperson Inquiry window.

| **Link field**     | **Window that opens**       |
|--------------------|-----------------------------|
| Salesperson ID     | Salesperson Maintenance     |
| Sales Territory ID | Sales Territory Maintenance |
| Document Number    | Invoice Inquiry             |

### Viewing invoices

Use the Invoice Inquiry window to view each invoice as it was originally
entered, reprint individual documents, and open additional inquiry windows to
gain more detailed information about individual fields on the invoice.

**To view invoices:**

1.  Open the Invoice Inquiry window.

>   (Inquiry \>\> Sales \>\> Invoice \>\> click Document Number link)

>   (Inquiry \>\> Sales \>\> Invoiced Items \>\> click Document Number link)
>   (Inquiry \>\> Sales \>\> Salesperson \>\> click Document Number link)

IMAGE - INVINQ.jpg

![A screenshot of a cell phone Description automatically generated](media/bb3b2302a95a7f4a0903252d1d018f69.jpg)

1.  Choose expansion buttons to view additional inquiry windows.

>   The following inquiry windows are available:

| **Expansion button** | **Inquiry window displayed**    |
|----------------------|---------------------------------|
| Date                 | Invoice Date Inquiry            |
| Customer ID          | Invoice Customer Detail Inquiry |
| Item Number          | Invoice Item Detail Inquiry     |
| Freight              | Invoice Tax Schedule Inquiry    |
| Miscellaneous        | Invoice Tax Schedule Inquiry    |
| Tax                  | Invoice Tax Summary Inquiry     |
| Amount Received      | Invoice Payment Inquiry         |
| Terms Discount Taken | Invoice Payment Terms Inquiry   |
|                      |                                 |
| Comment ID           | Invoice Comment Inquiry         |

1.  Choose Distributions to view distributions information. The Invoice
    Distribution Inquiry window will open, displaying the accounts to which
    transaction amounts were distributed.

2.  Choose Commissions to view commissions information. The Invoice Commissions
    Inquiry window opens, displaying sales commission information related to the
    invoice.

3.  To reprint an invoice or return, choose Print. To change the invoice format,
    print tax details on an invoice, or print an alignment form, choose the
    Options menu and select the appropriate item when the Invoice Inquiry window
    is open.

Chapter 12: Reports
-------------------

>   You can use Invoicing reports to analyze receivables activity and identify
>   errors in transaction entry. Use the information in this chapter to guide
>   you through printing reports and working with report options.

>   For more information about creating and printing reports, and the various
>   reporting tools that you can use with Microsoft Dynamics GP, refer to your
>   System User’s Guide (Help \>\> Contents \>\> select Using The System).

>   Reports information is divided into the following sections:

-   *Invoicing report summary*

-   *Specifying an Invoicing report option*

### Invoicing report summary

>   Some Invoicing reports are printed automatically when you complete certain
>   procedures; for example, posting journals can be printed automatically when
>   you post transactions. You can choose to print some reports during
>   procedures; for example, you can print an edit list when entering
>   transactions. In order to print some reports, such as analysis or history
>   reports, you must set up report options to specify sorting options and
>   ranges of information to include on the report.

>   The following table lists the report types available in Invoicing and the
>   reports that fall into those categories.

IMAGE – INVRPTS.jpg

![A screenshot of a cell phone Description automatically generated](media/9e22f7a16c489ea2fec8b5b57f133815.jpg)

### Specifying an Invoicing report option

>   Report options include specifications of sorting options and range
>   restrictions for a particular report. In order to print some of the
>   Invoicing reports, you must first create report options. Each report can
>   have several different options so that you can easily print the information
>   you need. For example, you can create one report option to show summary
>   information, and another option to show detailed information.

>   *A single report option can’t be used by multiple reports. For identical
>   options for several reports, you must create them separately.*

>   Use the Sales report options windows to create sorting, restriction and
>   printing options for the reports that have been included with Invoicing.

>   **To specify an Invoicing report option:**

1.  Open a Sales reports window. There are separate windows for each report
    type.

>   (Reports \>\> Sales \>\> Setup)

>   (Reports \>\> Sales \>\> Posting)

>   (Reports \>\> Sales \>\> History) (Reports \>\> Sales \>\> Analysis)

1.  Select a report from the Reports List.

2.  Choose New to open the report options window. Your selection in step 2
    determines which report options window appears.

>   For report options window information choose Help \>\> Index; then enter the
>   name of the specific report options window.

1.  Name the option and enter information to define the option. The name you
    choose for the option won’t appear on the report. The selections available
    for defining report options vary, depending on the report type you’ve
    selected.

2.  Enter range restrictions. The Ranges list shows the ranges available for
    each report. The available ranges vary, depending on the type of report.

>   *You can enter only one restriction for each restriction type. For instance,
>   you can insert one customer ID restriction or one document number
>   restriction.*

1.  Choose Insert to add the range to the Restrictions List. To remove an
    existing range from the list, select the range and choose Remove.

2.  Choose Destination to select a printing destination. Reports can be printed
    to the screen, to the printer, to a file, or to any combination of these
    options. If you select Ask Each Time, you’ll be able to select printing
    options each time you print this report option.

3.  To print the report option from the report options window, choose Print
    before saving it. If you don’t want to print the option now, choose Save and
    close the window. The report window will be redisplayed.

Chapter 13: History removal
---------------------------

>   History records provide useful information for auditing purposes. If you’re
>   keeping one of the types of history available in Invoicing, those records
>   can be maintained for an unlimited number of years.

>   You can remove the historical information when it’s no longer useful. You
>   also can print reports to create a permanent record of the information
>   stored in history.

>   The amount of information stored in history can occupy a considerable amount
>   of disk space. If you need to change the type of historical information
>   being saved, see *Setting Invoicing general options and defaults*.

>   Information about maintaining history is divided into the following
>   sections:

-   *Removing invoicing history*

-   *Printing history reports without removing history*

-   *Removing Intrastat statistics history*

### Removing invoicing history

>   In Invoicing, you can maintain three types of history—transaction, account
>   distribution, and journal history. Use the Remove Invoicing History window
>   to remove all three types of history.

>   **Transaction history** Detailed information for all transactions that were
>   transferred to history during the posting process. When you remove
>   transaction history, you’ll remove sales tax history and salesperson
>   commission history, as well.

>   **Distribution history** Detailed record of how Invoicing transactions have
>   affected the balances of distribution accounts.

>   **Journal history** Batch and audit trail information. If you remove journal
>   history, you won’t be able to reprint posting journals for the range of
>   information you’ve removed.

>   *Before removing history, back up your company’s accounting data. For more
>   information about making backups in Microsoft Dynamics GP, refer to the
>   System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration), or search for the keyword “backups” in the online help.*

>   **To remove invoicing history:**

1.  Make a backup of your accounting data. Making a backup protects your data in
    case of a power fluctuation or other problem.

2.  Open the Remove Invoicing History window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Utilities \>\> Sales \>\> Remove Invoice History)

3.  Select the history type to remove.

4.  Select a range of history to remove and specify the start and end of the
    range.

5.  Choose Insert. The range you’ve entered will be displayed in the
    Restrictions box.

6.  Select additional ranges and restrictions, if desired. You can enter only
    one restriction for each restriction type. For example, if you enter a
    restriction specifying that only document numbers IVC100 through IVC300
    should be removed, you can’t enter another restriction for document numbers
    IVC500 through IVC800. However, you could enter a range of dates in addition
    to the document numbers. To clear multiple ranges of history, you must clear
    each range separately.

>   *If you’ve made an error in selecting a range, highlight the range and
>   choose Remove. The range will be removed from the Restrictions box.*

1.  Mark the type of history to remove—Transaction, Distributions, or Journal.

2.  Mark Report to print a report listing the information that was removed from
    history. Depending on which type of history you remove, a Journal Removal
    Report, Transaction Removal Report, or Account Distribution Removal Report
    will be printed.

3.  Choose Process to remove the history and print the selected reports.

### Printing history reports without removing history

>   Use the Remove Invoicing History window to print history reports at any
>   time, so you can review the information stored in history before you remove
>   it.

>   **To print history reports without removing history:**

1.  Open the Remove Invoicing History window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Utilities \>\> Sales \>\> Remove
>   Invoice History)

1.  Select the history type.

2.  Select a range of history to remove and specify the start and end of the
    range.

3.  Choose Insert. The range you’ve entered will be displayed in the
    Restrictions box.

4.  Mark Report, and be sure Transaction, Distributions, and Journal are
    unmarked.

5.  Choose Process to print the report or reports selected. Depending on which
    type of history you selected, a Journal Removal Report, Transaction Removal
    Report, or Account Distribution Removal Report will be printed.

### Removing Intrastat statistics history

>   Use the Remove Intrastat History window to remove Intrastat statistics
>   history records that are no longer necessary. Only the Intrastat statistics
>   records for the range you specify will be removed.

>   *Before removing history, back up your company's accounting data. For more
>   information on making backups, refer to the System Administrator’s Guide
>   (Help \>\> Contents \>\> select System Administration).*

>   Once history has been removed, you won’t be able to print the Intrastat
>   statistics removal reports for the ranges of information you’ve removed.

>   **To remove Intrastat statistics history:**

1.  Open the Remove Intrastat History window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Utilities \>\> Company \>\>
>   Remove Intrastat History)

1.  Select a range type and specify the start and end of the range.

2.  Choose Insert to display the range. Select additional ranges and
    restrictions, if desired. You can enter only one restriction for each
    restriction type. For

>   example, if you enter a restriction specifying that history should be
>   deleted for customer records COMPUTER0003 through GRAHAMAR0001, you can’t
>   enter another restriction for customer IDs CONTINEN0001 through
>   EXECUTIV0001.

1.  Mark Transactions, then mark Print Report to print the Intrastat removal
    reports for the range of customer records or vendor records you’ve
    specified. Print these reports to retain a permanent record of your past
    Intrastat records after you’ve cleared history.

>   *You can print the Intrastat removal reports without removing history. To do
>   so, mark only Print Report and choose OK.*

Glossary
========

**Account**

>   The type of record—asset, liability, revenue, expense, or owner’s
>   equity—traditionally used for recording individual transactions in an
>   accounting system. Also, the identifying alphanumeric characters that have
>   been assigned to the record. *See also Posting account*.

**Account alias**

>   A “short name” for a posting account in the chart of accounts. If the
>   account format has a large number of segments, using aliases can speed data
>   entry.

**Accounting period**

>   A subdivision of the fiscal year. Common periods are months or quarters.

**Active customer**

>   A user with whom business is conducted on a regular basis.

**Alert message**

>   A message that appears when inappropriate, inadequate, or unclear data or
>   instructions are issued, when data is not accessible or when a confirmation
>   is sought. Additional information about some alert messages and their causes
>   can be viewed by choosing the Help button in the alert message dialog box.

**Alignment form**

>   A document that ensures text will be properly aligned when statements are
>   printed.

**Application**

>   A software program designed to perform particular tasks through the use of
>   one or more windows. *See also Module*.

**Audit trail**

>   A series of permanent records used to track a transaction to the point where
>   it was originally entered in Microsoft Dynamics GP. The audit trail can be
>   used to verify the accuracy of financial statements by outside accountants
>   or auditors.

**Audit trail code**

>   A series of alphanumeric characters providing a precise record of each
>   transaction and where it has been posted within Microsoft Dynamics GP.

**Bank card**

>   A card, such as VISA or Master Card. Bank cards differ from charge cards,
>   such as American Express, because payments can be treated as cash by the
>   business that receives the payment.

**Batch**

>   A group of transactions identified by a unique name or number. Batches are
>   used in computerized accounting to conveniently group transactions, both for
>   identification purposes and to speed the posting process.

**Batch approval**

>   Allows users to choose whether to approve batches of transactions before
>   posting. If the batch approval option is being used, the ID of the user who
>   approved the batch and the approval date will appear on posting reports.

**Batch controls**

>   Values for both the number of transactions in a batch and the total currency
>   amount of the batch. As transactions are entered, the actual totals will be
>   displayed. These totals can be verified periodically as transactions are
>   entered to ensure that the required number and amount of transactions match
>   the actual number and amount that was entered.

**Batch frequency**

>   A selection in many batch entry windows that determines how often a
>   recurring batch will be posted, such as weekly, monthly, or quarterly.
>   Invoicing batches must be singleuse.

**Batch posting**

>   An option used to post a group of transactions identified by a unique name
>   or number in the Invoice Batch Entry window.

**Batch-level posting**

>   A posting method you can use to save transactions in batches and post the
>   batches whenever it’s convenient. There are three types of batch-level
>   posting: batch posting, series posting, and master posting. *See also Series
>   posting*.

**Calendar year**

>   An accounting period running from January 1 to December 31.

**Calendar-year history**

>   A record of transactions by calendar months.

**Cash**

>   Ready money or its equivalent that a bank will accept at face value. Cash
>   includes coins; paper money; certain deposited negotiable instruments such
>   as checks, bank drafts, and money orders; amounts in checking and savings
>   accounts; and demand certificates of deposit.

**Cash receipt**

>   A document used to record payments and deposits received from users.

**Charge card**

>   A type of credit card. Charge cards are issued by banks and authorize the
>   holder to buy goods or services on credit. Payments received from charge
>   cards are treated as accounts receivable amounts, because you must submit
>   them to the card companies for reimbursement. You must receive reimbursement
>   to consider the charged amounts paid.

**Check card**

>   A type of credit card. When purchases are made with a check card, the amount
>   of purchase will be immediately withdrawn from the user’s bank account.

**Checkbook**

>   An account used to maintain a currency balance and track the receiving and
>   disbursing of cash.

**Class**

>   A feature that allows users, vendors, or items to be grouped according to
>   common characteristics. For example, a user class could be created to group
>   users according to credit limit or location.

**Comma-delimited field**

>   The standard comma-separated ASCII character format used when exporting a
>   report so that it can be read by database programs, such as dBASE and 4th
>   Dimension.

**Commission**

>   The amount, usually a percentage of the sale amount, paid to the salesperson
>   making the sale.

**Credit card**

>   Cards used to pay for items instead of a check, cash, or other method. The
>   amount due is then billed by the credit card company. You can use the Credit
>   Card Setup window to classify cards used to make payments as credit cards or
>   check cards. Cards accepted as payment by a company can be classified as
>   bank cards or charge cards.

**Credit limit**

>   A limit placed by the vendor on the monetary amount that a business can
>   charge.

**Credit term**

>   A condition agreed on when credit is granted.

**Creditor**

>   A business or person that lends money or extends credit to another business
>   or person.

**Customer**

>   A person or company provided with goods or services with an obligation to
>   pay for these goods and services.

**Customer ID**

>   An alphanumeric identification assigned to users in the Customer Maintenance
>   window. The customer ID can be used to sort information for reports.

**Debtor**

>   A person or business that has borrowed money or has received credit from
>   another person or business.

**Default**

>   A value that is displayed in a window automatically, and that will be used
>   unless a different value is entered.

**Deleting**

>   The process of removing stored information that has been selected.

**Discount available**

>   A reduction in the amount payable, typically offered if the payment is made
>   by a certain date. *See also Discount taken*.

**Discount date**

>   The date an invoice must be paid for a discount to be valid.

**Discount taken**

>   The discount amount users take from their available payment terms discount.
>   *See also Discount available*.

**Distributing**

>   The process of allocating to separate accounts a percentage or part of
>   transaction amounts.

**Distribution account**

>   An account designated to receive a percentage of transaction amounts posted
>   to a fixed or variable allocation account or accounts designated to receive
>   a percentage or part of posted transactions.

**Distribution history**

>   A record of the debits and credits for each document that was distributed to
>   individual posting accounts.

**Document**

>   All the information entered for a single, complete transaction, including
>   distribution amounts.

**Document number**

>   The number assigned to any invoice, return, or packing slip document
>   recorded in Invoicing.

**Document type**

>   A selection that identifies a document’s purpose and how document amounts
>   will be posted. In Invoicing, the document types include invoices, returns,
>   and packing slips.

**Drill down**

>   *See Link*.

**Edit list**

>   A list of transactions in an unposted batch that can be printed to verify
>   the accuracy of transactions before posting. Edit lists can be printed from
>   the Invoice Batch Entry window or any transaction entry window as long as a
>   batch ID has been entered.

**Error message**

>   *See Alert message*.

**Extended price**

>   The total price for each line item on an invoice calculated using the
>   following formula: (Unit Price – Markdown) x Quantity = Extended Price.

**Group printing**

>   Creating and printing report options in groups. For example, a report group
>   could be used to print all the financial statements and the Trial Balance
>   before closing a month, quarter, or fiscal year.

**History**

>   A record of transactions or account balances for previous years.

**Hold**

>   A restriction that prevents a document from being posted. Items that have
>   been assigned to a transaction on hold will be allocated in inventory for
>   that transaction, if you’re using the Inventory Control module.

**HTML file**

>   A file format that allows you to put information onto a web page and access
>   it from the Internet or from your company’s intranet using a web browser.

**Inactive customer record**

>   A user with whom business isn’t being conducted any longer. Typically,
>   records for these users can’t be deleted because historical records are
>   being maintained.

**Inquiry**

>   A feature that allows users to view openyear and historical information.

**Integrate**

>   To join two or more accounting modules to form a system in which data is
>   shared among modules. All Microsoft Dynamics GP modules are automatically
>   integrated.

**Intrastat**

>   The system for collecting statistics on the trade of goods between European
>   Union (EU) countries. Intrastat data is required for all items either bought
>   from EU vendors or sold to EU customers, and must be provided on a monthly
>   basis. Requirements for Intrastat are similar in all EU countries. The
>   government uses these statistics as an economic indicator.

**Invoice**

>   A document that records the prices and other details of goods and services
>   sold or supplied.

**Link**

>   A feature in some windows that displays information as it was originally
>   entered.

**Lookup window**

>   A window that displays a list of accounts, users, jobs, or other items in
>   the Microsoft Dynamics GP system. Lookup windows for a specific field are
>   displayed by choosing the lookup button next to the field.

**Lot number**

>   A number that describes items that were created at the same time and have
>   characteristics in common, such as the dye used in fabrics and carpet.

**Markdown**

>   The amount or percentage subtracted from the unit price of an item to
>   determine the price at which the item is sold.

**Master posting**

>   A posting process in which marked batches from different series can be
>   posted simultaneously.

**Miscellaneous charge**

>   A charge that isn’t part of a normal purchasing process. A miscellaneous
>   charge may be a service charge such as installation or repair of
>   merchandise.

**Module**

>   A Microsoft Dynamics GP application that can be used to perform a specific
>   set of tasks. Modules are combined to form a series. For example, the
>   Receivables Management and Invoicing modules are part of the Sales series.
>   *See also Series*.

**Multiple addresses**

>   Locations in addition to a company’s main location. For example, a business
>   with several stores can specify an address for each location.

**Notes**

>   A feature that is used to attach messages to windows and records throughout
>   the Microsoft Dynamics GP system. The Notes button shows whether a note is
>   attached to a window. Notes can be edited and reattached, deleted, or
>   printed.

**Origin**

>   A transaction entry window within a specific Microsoft Dynamics GP module.
>   Certain options, such as closing fiscal periods, can be selected for each
>   transaction origin. Also, the transaction origin will appear as part of the
>   audit trail code on all posting reports in Microsoft Dynamics GP.

**Packing slip**

>   A document you can print that displays the items and quantities that are
>   included when you ship an order.

**Payment terms**

>   Conditions for payment agreed on when a sales transaction takes place.
>   Payment terms might include a discount to the selling price if the payment
>   is received within a certain time period.

**Posting**

>   A procedure to make temporary transactions a part of permanent records or to
>   update accounts with specific transaction amounts. In manual accounting,
>   posting transfers journal entries to the appropriate accounts in a general
>   ledger.

**Posting account**

>   A financial account that tracks assets, liabilities, revenue, or expenses.
>   These accounts will appear on the financial statements and other reports
>   created in the financial series. *See also Account*.

**Posting journal**

>   A report printed following the posting process that shows the detail for
>   each transaction that has been posted. Posting journals also include the
>   audit trail code, which provides a precise record of where each transaction
>   has been posted within Microsoft Dynamics GP.

**Price level**

>   A feature that allows you to specify different prices for an item or group
>   of items, depending on who it’s being sold to. For example, you might charge
>   one price if you are selling to a retail customer and another price if you
>   are selling to a wholesale customer. You don’t need to assign all price
>   levels to all U of Ms, but you need to verify that each U of M can be used
>   with every price level at which you might want to sell the item.

**Range**

>   A selection used to narrow the amount of records that will be printed on a
>   report. For example, a selected range of customer IDs could be those between
>   5,000 and 6,000.

**Real-time posting**

>   *See Transaction-level posting*.

**Record**

>   A collection of related fields within a file.

>   Records typically comprise most or all of the data entered in the fields in
>   a given window. The entries in a single transaction entry window constitute
>   a record.

**Removing history**

>   A procedure used to erase ranges of historical information. Additional hard
>   disk space will become available when history has been removed and files
>   have been shrunk.

**Report option**

>   A collection of entries that specify the amount of information or the type
>   of information that will appear on a report. Multiple report options can be
>   created for each Microsoft Dynamics GP report.

**Return**

>   A transaction that records the return of merchandise after the invoice for
>   the sale has been posted. Returns are applied to the original invoice (for
>   open item customers) or to the customer’s balance (for balance forward
>   customers).

**Sales tax detail**

>   *See Tax detail*.

**Sales tax schedule**

>   *See Tax schedule*.

**Sales territory**

>   A division of the regions in which a company’s products are sold, based on
>   geographic location. In Microsoft Dynamics GP, sales and commissions can be
>   tracked for each sales territory.

**Salesperson**

>   A person who sells a company’s goods or services.

**Sample data**

>   Data that can be used to practice procedures by entering the information
>   listed in the online lessons. Sample data can be accessed using the lesson
>   company, Fabrikam, Inc.

**Serial number**

>   A number assigned to a specific inventoried item to identify it and
>   differentiate it from similar items with the same item number.

**Series**

>   A group of Microsoft Dynamics GP modules that form an interrelated set of
>   applications. Receivables Management is part of the Sales series, for
>   example.

**Series posting**

>   A posting process in which marked batches from the same series can be posted
>   simultaneously.

**Setup routine**

>   A series of procedures that can be used to open the windows where options
>   and defaults for a specific module are modified or set up.

**Single-use batch**

>   A batch that is created, posted once and then deleted from the system
>   automatically.

**Sorting**

>   A method of arranging data based on the order of specified information. For
>   example, records sorted by document would list all items on a document
>   before listing the items on the next document.

**Sorting segment**

>   Segments of posting accounts that can be used for sorting Microsoft Dynamics
>   GP reports. Sixteen sorting segments can be used; seven are predefined and
>   the remaining nine can be selected by the user.

**Tab-delimited fields**

>   The tab-separated ASCII character format used when exporting a report so
>   that it can be read by worksheet programs, such as Microsoft Excel®.

**Tax detail**

>   A definition of a tax that may apply to users.

>   Tax details are grouped into tax schedules.

>   *See also Tax schedule*.

**Tax schedule**

>   Groups of tax details that define each tax that may apply to users, items,
>   or other taxable costs. Tax schedules are used to determine which taxes
>   apply to individual sales.

**Text-only format**

>   A file format that saves reports as text without formatting. This format is
>   used when exporting reports to applications that are unable to read other
>   formats available in Microsoft Dynamics GP.

**Trade discount**

>   A discount a user always receives. The rate is calculated at the time of a
>   sale and is given in addition to any payment terms discounts that also may
>   be offered.

**Transaction**

>   An event or condition that is recorded in asset, liability, expense,
>   revenue, and/or equity accounts. Sales to users or purchases from vendors
>   are examples of transactions.

**Transaction date**

>   The date a transaction occurred; not necessarily the date it was entered in
>   the system.

**Transaction history**

>   A record of the transactions that have been entered and posted in Invoicing.

**Transaction-level posting**

>   A posting method in which transactions can be entered and posted without
>   having to create a batch. Also know as real-time posting. *See also
>   Batch-level posting*.

**Unit account**

>   An account that tracks statistical or nonfinancial quantities, like the
>   number of users with past-due balances or the number of invoices generated
>   over a specific time period.

**Unit cost**

>   The amount per unit that you paid for an item you’re planning to sell or
>   consume.

**Unit of measure**

>   A user-defined unit in which an item can be bought or sold. Items can be
>   sold in multiple units of measure. For example, a “pair” might be your unit
>   of measure for shoes.

**Unit price**

>   The amount per unit that you sell an item for.

**VAT (Value-Added Tax)**

>   A sales tax used in Europe and elsewhere in the world.

**ZIP code**

>   In the United States, the postal code assigned to business and residential
>   addresses. In other countries/regions, it may be referred to as postcode or
>   postal code.
