**Introduction**

You can use Purchase Order Processing to enter standard, drop-ship, and blanket
purchase orders for items. When necessary, you can change the status of a
purchase order or the individual line items on the purchase order. For example,
you might cancel a line item on a purchase order if the item that you’ve ordered
has been discontinued or if you won’t be receiving part of the quantity ordered
for the purchase order.

You also can use Purchase Order Processing to complete the following tasks:

-   Enter and post shipment receipts, in-transit inventory receipts, and invoice
    receipts individually or in batches

-   Enter and post shipment/invoice receipts individually or in batches

-   Match shipments to invoices so that accurate costs are assigned to items
    received into inventory

-   Apply landed costs, such as shipping costs and handling fees, to items

-   Use purchase order generator to automatically create purchase orders to
    replenish inventory quantities

-   Process purchasing returns and offsets the original purchase order
    transaction amount against inventory accounts and applicable general ledger
    accounts. Returned items are matched to the original receipts.

If you are using Project Accounting, you can enter purchase orders and drop-ship
purchase orders for projects.

If you are using Sales Order Processing, you can commit purchase order line
items to Sales Order Processing line items to fill sales orders.

If you are using Purchase Order Enhancements, you can approve and commit
purchase orders and return items that have been received on a shipment or
shipment/invoice receipt. For more information, see the Purchase Order
Enhancements documentation.

>   **What’s in this manual**

This manual is designed to give you an understanding of how to use the features
of Purchase Order Processing, and how it integrates with the Microsoft Dynamics®
GP system.

To make best use of Purchase Order Processing, you should be familiar with
systemwide features described in the System User’s Guide, the System Setup
Guide, and the System Administrator’s Guide.

Some features described in the documentation are optional and can be purchased
through your Microsoft Dynamics GP partner.

>   **I N T R O D U C T I O N**

>   To view information about the release of Microsoft Dynamics GP that you’re
>   using and which modules or features you are registered to use, choose Help
>   \>\> About Microsoft Dynamics GP.

>   The manual is divided into the following parts:

-   *Part 1, Setup and cards*, introduces Purchase Order Processing and gives
    detailed instructions on setting it up.

-   *Part 2, Purchase orders*, explains how to enter, print, issue, and manage
    purchase orders.

-   *Part 3, Receipts*, explains how to enter and manage receipts.

-   *Part 4, Purchase order returns*, includes information about using purchase
    order returns.

-   *Part 5, Inquiries and reports*, explains how to use inquiries and reports
    to analyze your purchasing and receiving activity.

-   *Part 6, Utilities*, describes procedures you can use to reconcile purchase
    order information or remove history.

Part 1: Setup and cards
=======================

Use the following information to set up Purchase Order Processing. Setup
procedures generally need to be completed once, but you can refer to the
information at other times for instructions on modifying or viewing existing
entries.

The following topics are discussed:

-   *Chapter 1, “Module setup,”* provides instructions for setting up the
    Purchase Order Processing module.

-   *Chapter 2, “Buyers,”* describes how to set up and manage buyer IDs.
    Identifying a buyer on a purchase order makes it easier to track orders.

-   *Chapter 3, “Purchase order generator setup,”* provides instructions for
    setting up the purchase order generator.

-   *Chapter 4, “Project setup for Purchase Order Processing,”* provides
    instructions for setting up project information in the Purchase Order
    Processing module.

Chapter 1: Module setup
-----------------------

>   Use this information to learn about and set up Purchase Order Processing.
>   The setup procedures are organized in an order that will ensure Purchase
>   Order Processing is set up properly.

>   When you set up Purchase Order Processing, you can open each setup window
>   and enter information, or you can use the Setup Checklist window
>   (Administration \>\> Setup \>\> Setup Checklist) to guide you through the
>   setup process. See your System Setup Guide (Help \>\> Contents \>\> select
>   Setting up the System) for more information about the Setup Checklist
>   window.

>   This information is divided into the following sections:

-   *Purchase Order Processing document types*

-   *Purchase Order Processing history types*

-   *Before you set up Purchase Order Processing*

-   *Setting up Purchase Order Processing preferences and default entries*

-   *Setting up currency decimal places for non-inventoried items*

-   *Setting up Purchase Order Processing tax options*

-   *Setting up user-defined fields for receivings*

-   *Setting up comments*

### Purchase Order Processing document types

>   Use Purchase Order Processing to track your company’s purchasing activity.
>   You can enter and manage purchase orders, track shipments and invoices
>   received, and match shipments to invoices that were received separately.
>   There are seven types of documents in Purchase Order Processing.

-   Standard purchase orders list items that will be shipped to your business to
    be received into your inventory. For more information, see *Entering a
    standard purchase order*. If you are using Project Accounting, see *Entering
    a standard purchase order for projects* for more information.

-   Drop-ship purchase orders list items that will be shipped directly to the
    customer. The vendor sends you an invoice and you, in turn, send an invoice
    to the customer. For more information, see *Entering a drop-ship purchase
    order*. If you are using Project Accounting, see *Entering a drop-ship
    purchase order for projects* for more information.

-   Blanket purchase orders list a single item and the quantities that will be
    delivered in a series of shipments, usually on specific dates. The items
    will be shipped to your business to be received into your inventory. For
    more information, see *Entering a blanket purchase order*. If you are using
    Project Accounting, you can’t enter blanket purchase orders for projects.

-   Drop-Ship blanket purchase orders list a single item and the quantities that
    will be delivered to the customer in a series of shipments, usually on
    specific dates. The vendor sends you an invoice and you, in turn, send an
    invoice to the customer. For more information, see *Entering a drop-ship
    blanket purchase order*. If you are using Project Accounting, you can’t
    enter drop-ship blanket purchase orders for projects.

-   Shipment/invoice receipts record the receipt of goods and services
    accompanied by an invoice. For more information, see *Receiving a shipment/
    invoice*. If you are using Project Accounting, see *Receiving a
    shipment/invoice for project* for more information.

-   Shipment receipts record the receipt of goods and services without an
    invoice. For more information, see *Receiving a shipment*. If you are using
    Project Accounting, see *Receiving a shipment for projects* for more
    information.

-   Invoice receipts record an invoice received for a shipment you received and
    posted earlier, or an invoice received for a shipment that you have not yet
    received. For more information, see *Entering an invoice receipt*

    1.  If you are using Project Accounting, see *Entering an invoice receipt
        for projects* for more information.

### Purchase Order Processing history types

>   When setting up Purchase Order Processing, you’ll have the option to
>   maintain the following types of history. If you are using Project
>   Accounting, historical information for project line items will be maintained
>   in Project Accounting.

>   **Purchase Order** This option keeps a detailed copy of each purchase order
>   in history. When you transfer a purchase order to history using the Remove
>   Completed Purchase Orders window, or when you void a purchase order using
>   the Purchase Order Entry window, purchase order history will include
>   line-by-line detail of all information entered for each purchase order.

>   **Account Distributions** This option keeps a detailed record of transaction
>   distributions that are posted to General Ledger. Account distribution
>   history will be updated when each receipt is posted. Distribution history
>   includes the audit trail code, account, account description, debit or credit
>   amount, and other information about each transaction.

>   **Receipt** This option keeps a detailed copy of each receipt in history.
>   When you post or void a receipt using the Receivings Transaction Entry
>   window or the Purchasing Invoice Entry window, receipt history will include
>   line-by-line detail of all the information entered for each receipt,
>   including serial numbers, lot numbers, and bin information.

>   *Keeping history will increase the amount of hard disk space needed. You
>   should periodically remove the historical records you no longer need. For
>   more information, see Chapter 27, “Purchase order history removal.”*

### Before you set up Purchase Order Processing

>   You should complete setup procedures in Payables Management and Inventory
>   Control before you set up Purchase Order Processing. If you haven’t
>   completed all of the following tasks, be sure to do so before continuing.

-   Set up Payables Management

-   Create vendor cards

-   Enter beginning inventory quantities

-   Set up item records (be sure to assign price lists and vendor items)

-   Set up item sites

-   Set up inventory and purchasing accounts in the Posting Accounts Setup
    window

>   *To view the Posting Accounts Setup window, choose Administration \>\> Setup
>   \>\> Posting \>\> Posting Accounts and then select to view Inventory or
>   Purchasing accounts.*

>   Be sure you’ve also completed the setup procedures for your company,
>   currency, checkbooks, and posting options. Tax schedules and tax details
>   also should be set up. For more information about completing these
>   procedures, refer your System Setup instructions (Help \>\> Contents \>\>
>   select Setting Up the System).

>   If you’re using landed costs, be sure to set up landed cost records and
>   groups before you set up Purchase Order Processing. For details, see the
>   Inventory Control documentation.

>   If you’re using Multicurrency Management, be sure to set up currencies,
>   exchange rate tables, and rate types before you set up Purchase Order
>   Processing. For details, see the Multicurrency Management documentation.

### Setting up Purchase Order Processing preferences and default entries

>   Use the Purchase Order Processing Setup window to set preferences and
>   default entries that appear throughout Purchase Order Processing.

>   **To set up Purchase Order Processing preferences and default entries:**

1.  Open the Purchase Order Processing Setup window.

>   (Purchasing \>\> Setup \>\> Purchase Order Processing)

1.  Accept or change the default document code and enter the next document
    number you want to use for purchase orders.

>   The document code can be used to identify the documents on reports and
>   inquiries. The next number will be the starting document number when
>   receipts are entered. You can reuse a document number if the document has
>   been deleted or removed from history (if you’re keeping history).

>   By defining the next document number, you also are determining the number of
>   unique document numbers that will be available. For example, if you enter
>   PO001 as the next purchase order number, you’ll be able to enter up to 999
>   purchase orders; if you enter PO0001 as the next purchase order number,
>   you’ll be able to enter up to 9,999 purchase orders. Be sure to enter a next
>   number that will accommodate your business volume.

1.  Select the format you want to use when purchase orders are printed. If you
    are using Project Accounting, the default document format for a purchase
    order with project information will be the document format specified for the
    vendor record in the PA Vendor Options window.

>   *To use purchase order forms other than the suggested forms, you may want to
>   use Report Writer to be sure the information is printed on your forms
>   correctly. For more information, refer to Report Writer help.*

1.  Accept or change the default document code that appears and enter the next
    document number you want to use for receipts.

>   The document code can be used to identify the documents on reports and
>   inquiries. The next number will be the starting document number when
>   receipts are entered. You can reuse a document number if the document has
>   been deleted or removed from history (if you’re keeping history).

1.  Enter the number of decimal places to use when displaying and entering
    quantity and currency amounts for non-inventoried items.

>   If you’re using Multicurrency Management, choose the expansion button to
>   open the Purchasing Non-Inventoried Currency Decimals Setup window. Use this
>   window to define currency decimal places for each currency to which you have
>   access. For more information, see *Setting up currency decimal places for
>   non-inventoried items*.

1.  Mark Shortage and then enter the percentage to use when the quantity
    received is less than the quantity ordered for non-inventoried items when
    receiving against a standard or blanket purchase order. If the difference
    between the quantity received and quantity ordered falls within the quantity
    shortage percentage, the difference between the quantities is canceled and
    the status of a line item is automatically changed to change order,
    received, or closed. The status of the line item depends on whether or not
    the line item has been invoiced.

2.  Mark Overage and then enter the percentage to use when the quantity received
    is more than the quantity ordered for non-inventoried items when receiving
    against a standard or blanket purchase order. If the quantity received is
    over the overage tolerance, you will receive a message that you can't enter
    a quantity greater than the combined total of the Remaining to Receive
    quantity and the overage tolerance set up for the item.

3.  Select which date to use as a default date each time that you open the
    Purchase Order Entry window to work with purchase orders. You can use the
    date from the last document you entered or the user date.

4.  Select a default site ID for purchase order line items. You can select
    either the default site ID set up for the item in Item Quantities
    Maintenance window or the previous purchase order line’s site ID.

5.  Select which item numbers to use during transaction entry—the item numbers
    your company uses or the item numbers used by your vendors.

>   If you are using Project Accounting and select Vendor Items, you can’t enter
>   a project number and a cost category for purchase orders, shipment receipts,
>   shipment/invoice receipts, or invoice receipts.

1.  Indicate whether you want New purchase orders generated in Sales Order
    Processing to be placed on hold when they appear in the Purchase Order Entry
    window. If you mark this option, committing a Sales Order Processing line
    item to an existing purchase order line item will not cause the purchase
    order to be placed on hold.

>   If you mark this option and you’ve assigned a password to the option “Allow
>   Hold/Remove Hold of Purchase Orders,” you will not need to enter the
>   password during the purchase order generation process in Sales Order
>   Processing. However, the password to remove holds will apply when a purchase
>   order is viewed in the Purchase Order Entry window.

>   If you are using Project Accounting, you can’t create purchase orders for
>   projects from Sales Order Processing.

1.  Indicate whether you want the system to search for uncommitted purchase
    order quantities when you attempt to create a link between a sales line and
    a purchase order. If you don’t mark the option, you’ll be able to create a
    new purchase order for the sales document, but you won’t be able to link the
    sales line to an existing purchase order. Refer to the Sales Order
    Processing documentation for information about linking an item to an
    existing purchase order.

>   If you are using Project Accounting, you can’t commit purchase orders for
>   projects to sales documents.

1.  Indicate whether you want to transfer line item comments from sales
    documents to new purchase orders. If you mark this option, existing purchase
    order line comments will not change if linked to sales line items with
    comments.

>   If you are using Project Accounting, you can’t transfer line comments from
>   sales line items to purchase order line items that are assigned to projects.

1.  Indicate whether the release by date for a purchase order line item should
    be calculated by subtracting the vendor’s planning lead time from the
    required date. By marking this option, you can use the PO Line Items to
    Release Report to identify purchase order line items that should be released
    to the vendor. If you don’t mark this option, the release by date isn’t
    calculated automatically.

>   If you are using Project Accounting, the release by date isn’t calculated
>   for purchase order line items that are assigned to projects.

1.  Select the types of historical information you want to maintain for your
    purchase transactions. If you are using Project Accounting, historical
    information for project line items will be maintained in Project Accounting.
    For information about history types, see *Purchase Order Processing history
    types*.

>   *If you’ve selected to reprint Purchase Order Processing posting journals in
>   the Audit Trail Codes Setup window, the system will maintain the history
>   necessary to reprint posting journals whether or not you’ve marked to
>   maintain history in the Purchase Order Processing Setup window.*

1.  Mark Allow Purchase Order Prepayments to enter a prepayment amount for a
    purchase order and generate the prepayment as computer check in Payables
    Management.

>   Payables Management and Purchase Order Processing must be registered for
>   this option to be available, but Project Accounting, Multidimensional
>   Analysis, and Analytical Accounting must not be registered.

1.  To enter manual prepayments for purchase orders, mark the Create manual
    prepayment from Purchase Order Processing option.

>   This option is available when the Allow Purchase Order Prepayments option is
>   marked.

1.  Enter a password to limit the users who can enter prepayments for purchase
    orders.

>   This option is available when the Allow Purchase Order Prepayments option is
>   marked.

1.  Enter or select the account to be used as the default posting account when
    you post prepayments.

>   This option is available when the Allow Purchase Order Prepayments option is
>   marked.

1.  In the Options scrolling window, mark the check boxes next to the options
    you want to enable. You can assign passwords to the options to restrict who
    has access to them. If an option is marked, but no password is entered,
    anyone with access to the affected window can perform the action. You can
    select to allow the following:

>   **Receiving items without a purchase order** Select this option to allow
>   line items not assigned to a purchase order to be entered on a shipment,
>   shipment/invoice or invoice receipt. If the option isn’t selected, you won’t
>   be able to receive or invoice line items not associated with a purchase
>   order.

>   **Changing the site ID in receiving** Select this option to allow receiving
>   line items to different locations than indicated on the original purchase
>   order.

>   **Allowing/removing holds on purchase orders** Select this option to allow
>   users to place and remove holds on New, Released or Change Order purchase
>   orders of either type—standard or drop-ship.

>   When you mark this option, you also can indicate whether you want to allow
>   editing of purchase orders on hold. If you don’t allow editing on-hold
>   purchase orders, you will be able to view purchase orders that have been
>   placed on hold, but you won’t be able to edit, delete or void them.

>   **Editing costs in receiving** Select this option to allow changing an
>   item’s Unit Cost and Extended Cost in the Receivings Transaction Entry
>   window.

>   *When deciding whether to allow the editing of costs in receiving, keep in
>   mind that purchase price variances are calculated by comparing the cost
>   posted from receiving with the standard cost for items with periodic
>   valuation methods. For more information about standard cost and valuation
>   methods, see the Inventory Control documentation.*

>   If you allow receiving without a purchase order, you should allow editing of
>   costs in receiving, or you won’t be able to enter costs for items without
>   purchase orders. To restrict access, you can require a password.

>   **Warning when purchase order line item is not fully Invoiced** Select this
>   option to receive a warning message that a purchase order line item has a
>   remaining quantity to invoice when closing a purchase order or a purchase
>   order line item in the Edit Purchase Order Status window.

1.  If you are using Project Accounting, choose Project to open the PA Purchase
    Order Processing Setup Options window, where you can select preferences and
    default entries for purchase orders, shipment receipts, shipment/invoice
    receipts, and invoice receipts for projects. See *Setting up project
    preferences and default entries in Purchase Order Processing* for more
    information.

2.  Choose Options to open the Purchase Order Processing Setup Options window,
    where you can set up tax calculations in Purchase Order Processing. See
    *Setting up Purchase Order Processing tax options* for more information. If
    you are using purchase order generator, you can use the Purchase Order
    Processing Setup Options window select options for generating purchase
    orders. See *Setting up purchase order generator default entries* for more
    information.

3.  Choose Receivings User-Defined to enter labels for user-defined fields,
    lists, and dates that will be used when entering shipments and
    shipment/invoices. See *Setting up user-defined fields for receivings* for
    more information.

4.  Choose OK to save the entries you’ve made in the Purchase Order Processing
    Setup window.

5.  Print a Purchase Order Processing Setup List (optional).

>   Choose File \>\> Print while the Purchase Order Processing Setup window is
>   displayed to print a Purchase Order Processing Setup List to review the
>   setup options you’ve entered. If you’ve identified errors in the setup list,
>   simply enter or select the correct information.

>   This report also can be printed using the Purchasing Setup Reports window.

### Setting up currency decimal places for non-inventoried items

>   Use the Purchasing Non-Inventoried Currency Decimals Setup window to define
>   currency decimal places for non-inventoried items for each currency to which
>   your company has access. This window is available only if you are using
>   Multicurrency Management. If you aren’t using Multicurrency Management, use
>   the Purchase Order Processing Setup window to define the number of decimal
>   places when displaying currency amounts for non-inventoried items.

>   The default number of decimal places for each currency was determined when
>   the currencies were set up. Use this window to change the number of decimal
>   places used to display currency amounts for non-inventoried items. You can
>   change the non-inventoried currency decimal places for a currency at any
>   time.

>   Changing the decimal place setting for a currency won’t change the decimal
>   place settings of non-inventoried items already entered on existing
>   documents. Only new items added to existing transactions or new transactions
>   will use the new settings.

>   **To set up currency decimal places for non-inventoried items:**

1.  Open the Purchasing Non-Inventoried Currency Decimals Setup window.
    (Purchasing \>\> Setup \>\> Purchase Order Processing \>\> Currency
    expansion button)

![](media/6ba2ec7c1e8272e35d890878b6ba86e9.jpg)

1.  In the Currency Decimals column, change the number of currency decimal
    places to use for non-inventoried items. Amounts will appear in the format
    defined in this window whenever a non-inventoried item is entered for a
    specific currency.

2.  Continue this process until you define the decimal places for all the
    currencies displayed in the window.

3.  Choose File \>\> Print to print the Non-Inventoried Currency Decimals Setup
    List.

4.  Choose OK to close the window.

### Setting up Purchase Order Processing tax options

>   Use the Purchase Order Processing Setup Options window to set up the tax
>   calculations that will be used on documents. Depending on the tax
>   calculation selected, you can enter default tax schedules for
>   non-inventoried items, freight, and miscellaneous items. For information
>   about setting up the purchase order generator, see *Chapter 3, “Purchase
>   order generator setup.”*

>   **To set up Purchase Order Processing tax options:**

1.  Open the Purchase Order Processing Setup Options window.

>   (Purchasing \>\> Setup \>\> Purchase Order Processing \>\> Options button)

![](media/4ee2339a127b86e95966e259c53caf9d.jpg)

1.  Mark the type of tax calculation to use on documents.

>   **Advanced** Mark Advanced to specify a tax schedule to use for
>   noninventoried items, freight, and miscellaneous charges. For inventory
>   items, the tax schedule you chose for each item in the Item Maintenance
>   window will be used.

>   **Single Schedule** Mark Single Schedule to specify one tax schedule for all
>   items on all documents. Items on each document will be taxed using the tax
>   details in the schedule you specify here, even if the item is nontaxable or
>   if the vendor is tax exempt. Taxes won‘t be calculated on freight or
>   miscellaneous charges.

1.  If you marked Advanced in step 2, enter or select tax options for
    non-inventoried items, freight, and miscellaneous charges. You can change
    the tax schedules used for a transaction in a tax schedule entry window
    during transaction entry. The tax options are:

>   **Taxable** The tax details that are assigned to the vendor or site will be
>   compared to the tax details in the tax schedule you specify here.

>   **Nontaxable** No taxes will be calculated.

>   **Base on vendor** The tax schedule assigned to the vendor’s purchase
>   address will be used calculating taxes.

1.  Choose OK.

>   To print the Purchase Order Processing Setup List, choose File \>\> Print in
>   the Purchase Order Processing Setup window.

### Setting up user-defined fields for receivings

>   Use the Receivings User-Defined Fields Setup window to enter labels for up
>   to 35 user-defined fields to further track additional information for
>   shipment and shipment/invoice receipts. Later, when you enter receivings
>   transactions, the labels will appear in the Receivings User-Defined Fields
>   Entry window, where you can enter information that is unique to the
>   transaction. You can set up the following types of user-defined fields.

>   **List** Use list fields to predefine options to track information that is
>   specific to your business. For example, to track the origin of orders, you
>   could name a list Order Origin and enter Fax, Phone, and Mail as values for
>   the list. When you enter transactions, Order Origin will appear as a title
>   in the Receivings User-Defined Fields Entry window and you can select where
>   the order originated from the list you created or include additional values.

>   **Text** Use text fields to record additional information about the
>   transactions you enter in the Receivings Transaction Entry window. For
>   example, to track special ID numbers for shipped equipment, you can enter
>   Shipping ID in a text field.

>   **Dates** Use date fields to record additional dates that affect your
>   documents. For instance, if you want to track the date that an installation
>   was complete, enter Install Date in a date field.

>   **To set up user-defined fields for receivings:**

1.  Open the Receivings User-Defined Fields Setup window.

>   (Purchasing \>\> Setup \>\> Purchase Order Processing \>\> Receivings
>   UserDefined button)

![](media/57f6ffc6591d6ef0f007c40b6030200e.jpg)

1.  Enter as many as five list fields. Choose the expansion button next to each
    list name you‘ve entered; the Receivings User-Defined List Setup window will
    appear. Use this window to enter values for each list.

2.  Enter as many as 10 text fields to track additional information about your
    customers.

3.  Enter as many as 20 date fields to record additional dates that affect your
    documents.

4.  Choose File \>\> Print to print the Receivings User-Defined Fields Setup
    List.

5.  Choose OK to return to the Purchase Order Processing Setup window. Your
    changes are saved when you choose OK in the Purchase Order Processing Setup
    window.

### Setting up comments

>   You can add comments to purchase orders or to individual line items on a
>   purchase order or receipt. Comments are printed automatically on the
>   purchase order and line item comments are printed below the item on the
>   purchase order or receipt.

>   Use the Comment Setup window to define comments for each company. You can
>   use these comments on Sales Order Processing, Invoicing or Purchase Order
>   Processing documents. You also can modify standard comments for a particular
>   document or item, or create one-time comment.

>   **To set up comments:**

1.  Open the Comment Setup window.

>   (Administration \>\> Setup \>\> Company \>\> Comments)

![](media/342a27056685143222eabc944b7f08c3.jpg)

1.  Enter a short identifier for the comment.

2.  Select a series this comment will be associated with.

3.  Enter the comment text.

>   *You can enter up to 200 characters, which will appear on the purchase order
>   or receipt as four lines of 50 characters each. If you want longer comments
>   to appear, use Report Writer to modify the document layout.*

1.  Choose Save.

Chapter 2: Buyers
-----------------

>   Large companies typically have several buyers working in the purchasing
>   department, with each buyer assuming responsibility for certain items. A
>   buyer’s job may include vendor selection, negotiation, and purchase order
>   placement and follow-up.

>   Identifying a buyer on a purchase order makes it easier to track orders. For
>   example, if your company employs ten buyers who enter purchase orders in the
>   same system, the purchase order numbers are not an effective way of locating
>   a particular buyer’s documents. If buyers are assigned to purchase orders,
>   you can print a report sorted by Buyer ID.

>   This information is divided into the following sections:

-   *Adding buyer IDs*

-   *Modifying buyer IDs*

-   *Removing buyer IDs*

### Adding buyer IDs

>   Use the Buyer Maintenance window to add new buyer IDs. For example, a buyer
>   ID can be based on a location, a group of items, or an existing user ID.

>   **To add buyer IDs:**

1.  Open the Buyer Maintenance window. (Purchasing \>\> Cards \>\> Buyers)

![](media/5feaebfba15be5cb2970b747948f5130.jpg)

1.  Enter a buyer ID in the Buyer ID field.

2.  Enter a description.

3.  Choose Insert to insert the buyer ID in the scrolling window and save the
    record.

4.  Choose OK when you’re finished adding buyer IDs.

### Modifying buyer IDs

>   Use the Buyer Maintenance window to modify existing buyer IDs.

**To modify buyer IDs:**

1.  Open the Buyer Maintenance window.

>   (Purchasing \>\> Cards \>\> Buyers)

1.  Select a buyer ID in the scrolling window.

2.  Choose Modify. The buyer you selected will appear in the Buyer ID and
    Description fields.

3.  Edit the existing description.

4.  Choose Insert to insert the buyer ID in the scrolling window and save the
    record.

5.  Choose OK when you’re finished modifying a buyer ID.

### Removing buyer IDs

Use the Buyer Maintenance window to delete buyer IDs you no longer want to use.

If you remove a buyer ID that is linked to an active purchase order (one that
isn’t in history), the buyer ID will remain attached to that purchase order. If
the

Manufacturing Series is registered and you delete a buyer ID that is linked to
items in Item Engineering, the buyer ID will be removed from those items.

**To remove buyer IDs:**

1.  Open the Buyer Maintenance window.

>   (Purchasing \>\> Cards \>\> Buyers)

1.  To remove a single buyer ID, select it in the scrolling window and choose
    Remove. To remove all of your buyer IDs, choose Remove All.

Chapter 3: Purchase order generator setup
-----------------------------------------

>   If you are using the purchase order generator, you can automatically
>   generate purchase orders to replenish inventory based on a reorder point you
>   specify. If you are using Project Accounting, you can’t generate purchase
>   orders for projects.

>   Use the purchase order generator to analyze inventory levels and suggest
>   purchase order line items based on default settings and reorder levels; the
>   suggested purchase orders can be modified before they are created.

>   This information is divided into the following sections:

-   *Sites and purchase order generator*

-   *Setting up purchase order generator default entries*

-   *Mapping inventory sites to addresses*

### Sites and purchase order generator

>   You’ll use master sites, subordinate sites, and independent sites when
>   generating suggested purchase orders. How the demand is purchased, received,
>   and distributed depends on how you use these sites.

>   A **master site** is a central location where its requirements are
>   consolidated with the net demand from subordinate sites. A purchase order is
>   placed from the total net demand at the master site. You can have more than
>   one master site. A **subordinate site** is a location that passes its
>   requirements to a central location, the master site, to be purchased,
>   received, and distributed. An **independent site** is a location that has
>   requirements that must be fulfilled by the items that are to be purchased. A
>   master site is an independent site.

>   The order method you select for an item decides which site will be used when
>   generating purchase orders. If you select Order to Master Site, suggested
>   purchase order quantities will be based on requirements for this site and
>   other sites that have the same master site. When you are ordering to a
>   master site, you’ll need to set up your master site before setting up your
>   subordinate sites in the Purchase Order Generator Item Maintenance window.
>   The master site must have an order method of Order To Independent Site.
>   Assume that your default master site is Warehouse. If you didn’t set up
>   Warehouse as an independent site, any subordinate site that would have used
>   Warehouse as their master site will use order to independent site as their
>   order method.

>   If you select Order to Independent, suggested purchase orders can be
>   generated for the site where the material is required or if the site is a
>   master site for subordinate sites as well as the master site. Requirements
>   from subordinate sites will not be required is the site isn’t a master site.

### Setting up purchase order generator default entries

>   Use the Purchase Order Processing Setup Options window to define default
>   reorder information that will appear in the Purchase Order Generator Item
>   Maintenance window and the Purchase Order Item Mass Update window.

>   You also can select how purchase orders should be created when you generate
>   suggested purchase order line items using the Suggested Purchase Orders
>   Preview window. You can select to create a purchase order for all items that
>   have the same vendor, buyer, and ship-to address or create a purchase order
>   for all items that have the same vendor and buyer.

You should set up general default information before you define preferences for
a specific item-site combination or a group of items and sites. You can change
the entries for individual item-site combinations, if necessary. Use the
Purchase Order Generator Item Maintenance window to set up reorder preferences
for each item at a specific site. Use the Purchase Order Item Mass Update window
to set up or change reorder preferences for a group of items. For more
information, see the Inventory Control documentation.

If you are using Project Accounting, you can’t generate purchase orders for
projects.

**To set up purchase order generator default entries:**

1.  Open the Purchase Order Processing Setup Options window.

>   (Purchasing \>\> Setup \>\> Purchase Order Processing \>\> Options button)

![](media/55bf27ff53db6316fd539f79f8427ce2.jpg)

1.  Select a default order method for automatically generated purchase orders.

>   **Order To Independent Site** Use this option if you want to order to the
>   site where the material is required.

>   **Order To Master Site** Use this option if items are purchased to a central
>   location (a master site) and distributed to other sites (subordinate sites).

1.  If the order method is Order To Master Site, enter or select a master site.
    Demand from all subordinate sites will be combined with demand for the
    master site you select when determining the order quantity.

2.  Select a default replenishment level.

>   **Order Point Quantity** Select this level to order a quantity that will
>   bring available inventory up to the order point defined in the Item Resource
>   Planning Maintenance window.

>   **Order-Up-To-Level** Select this level to order a quantity that will bring
>   available inventory up to the order-up-to level defined in the Item Resource
>   Planning Maintenance window. The Order Point Quantity will be used if the
>   Order-Up-To Level is zero or less than the Order Point Quantity.

>   **Vendor EOQ** Select this level to order a quantity that is equal to the
>   economic order quantity defined in the Item Vendors Maintenance window for
>   the selected vendor. The vendor economic quantity is used when it is greater
>   than the required quantity otherwise, the required quantity is used.You
>   won’t be able to select this option if the order method is Order To Master
>   Site.

>   Refer to *How quantities are calculated for suggested purchase orders* for
>   information about how replenishment levels affect required quantity.

1.  If the order method is Order To Independent Site, indicate which vendor to
    use for purchase orders.

>   **Site Primary Vendor** The primary vendor specified in the Item Quantities
>   Maintenance window for the item-site combination is used.

>   **Vendor with Lowest Cost** The vendor with the lowest cost will be selected
>   based on the functional equivalent of the Last Originating Invoice Cost
>   field in the Item Vendors Maintenance window.

>   **Vendor with Shortest Lead Time** The vendor with the shortest planning
>   lead time will be selected based on the Planning Lead Time field in the Item
>   Vendors Maintenance window.

>   You won’t be able to select a vendor selection if the order method is Order
>   To Master Site. The master site’s vendor selection will be used to determine
>   the vendor.

>   If the order method is Order To Independent Site, indicate which item cost
>   to use for purchase orders.

>   **Vendor Last Originating Invoice Cost** The last originating invoice cost
>   from the Item Vendors Maintenance window for the selected vendor will be
>   used.

>   **Item Current Cost** The current cost from the Item Maintenance window will
>   be used.

>   **Item Standard Cost** The standard cost from the Item Maintenance window
>   will be used.

>   **Specified Cost (In Functional Currency)** The cost specified in the
>   Purchase Order Generator Item Maintenance window will be used regardless of
>   the vendor.

>   You won’t be able to select a cost selection if the order method is Order To
>   Master Site. The master site’s cost selection will be used to determine the
>   cost.

1.  Mark Allocations to subtract the allocated quantity from the current supply
    when the required quantity is calculated.

2.  Mark Back Orders to subtract the back ordered quantity from the current
    supply when the required quantity is calculated.

3.  Mark Requisitions to subtract the requisitioned quantity from the current
    supply when the required quantity is calculated.

4.  Unmark Create One Purchase Order per Ship To Address to generate a purchase
    order for all items that have the same vendor and buyer. If this option is
    marked, you can generate a purchase order for all items that have the same
    vendor, buyer, and ship-to address.

5.  Choose OK to close the window and return to the Purchase Order Processing
    Setup window.

### Mapping inventory sites to addresses

Use the Purchase Order Generator Map Sites window to define the relationship
between inventory site IDs and company addresses. The company address you assign
to an inventory site is used as the ship-to address on suggested purchase orders
for that site. If there is no company address mapped to a site, the company’s
primary address ID is used on purchase orders for that site.

When suggested purchase order line items are generated, all items for the same
vendor, buyer ID, and ship-to address will be grouped together on a single
purchase order. The ship-to address for a purchase order line is determined by
the item’s site ID.

For example, if an item needs to be replenished at three sites and all sites
have the same address ID, three lines for the item will be created on the same
purchase order—one line for each site.

If you are using Project Accounting, you can’t generate purchase orders for
projects.

**To map inventory sites to addresses:**

1.  Open the Purchase Order Generator Map Sites window.

>   (Purchasing \>\> Setup \>\> Purchase Order Generator Map Sites)

![](media/4677bf4ea0b0bfd61f76a748c7999322.jpg)

>   All inventory site IDs defined for the current company will be displayed.

1.  Enter or select an address ID (defined in the Company Addresses Setup
    window) for each site ID.

>   Any site that is left unmapped will use the primary company address.
>   Suggested purchase order line items for these sites will be consolidated as
>   lines on a purchase order.

1.  Choose OK to save changes and to close the window when you’re finished
    mapping sites.

Chapter 4: Project setup for Purchase Order Processing
------------------------------------------------------

>   If you are using Project Accounting, you can enter project information on
>   purchase orders, shipment receipts, shipment/invoice receipts, and invoice
>   receipts. Use the following information to set up project preferences and
>   default entries for Purchase Order Processing.

>   This information is divided into the following sections:

-   *Projects in Purchase Order Processing*

-   *Before you set up Purchase Order Processing for projects*

-   *Setting up project preferences and default entries in Purchase Order
    Processing*

### Projects in Purchase Order Processing

>   You can set up, enter and maintain project records and transactions using
>   Project Accounting. You also can budget resources, manage purchases,
>   schedule tasks, monitor costs, bill customers, and recognize revenue. For
>   more information about Project Accounting, projects, and cost categories,
>   refer to the Project Accounting documentation.

>   You can acquire goods and services to be used in projects or you can buy
>   them on behalf of customers. You can enter standard and drop-ship purchase
>   orders for projects. As you receive the goods and services that you purchase
>   for projects, you can enter the receipt of shipments and invoices. Items
>   received from a standard purchase order are stored in inventory. To transfer
>   these items to a project to make the items billable, you’ll use the
>   Inventory Transfer Entry window in Projecting Accounting. Items from a
>   drop-ship purchase order are automatically invoiced and transferred to a
>   project.

>   You can complete the following tasks if you aren’t entering project
>   information for purchase orders, shipment receipts, shipment/invoice
>   receipts, or invoice receipts.

-   Enter blanket and drop-ship blanket purchase orders

-   Commit purchase orders to sales documents

-   Enter manufacturers’ item numbers for purchase orders

-   Enter manufacturing job links for purchase orders, shipment, shipment/
    invoice, and invoice receipts

-   Open the MRP Item Inquiry window to view Material Requirements Planning
    information for an item if you’re using the Manufacturing Series

-   Automatically generate purchase orders to replenish inventory, based on a
    reorder point that you specify

### Before you set up Purchase Order Processing for projects

You should complete setup procedures in Project Accounting before you set up
Purchase Order Processing for projects. If you haven’t completed all of the
following tasks, be sure to do so before continuing. Refer to the Project
Accounting documentation for more information about setting up Project
Accounting.

| **Task to complete**                                                           | **Window used**                               |
|--------------------------------------------------------------------------------|-----------------------------------------------|
| Set up user options for purchase orders                                        | User Purchase Order Settings window           |
| Set up user options for invoice receipts                                       | User Purchasing Invoice Settings window       |
| Set up user class options for purchase orders                                  | User Class Purchase Order Settings window     |
| Set up user class options for invoice receipts                                 | User Class Purchasing Invoice Settings window |
| Set up project default entries                                                 | Project Setup window                          |
| Set up project and contract status options                                     | Project Setup – Status Options window         |
| Create contract records                                                        | Contract Maintenance window                   |
| Create a cost category record                                                  | Cost Category Maintenance window              |
| Create project records                                                         | Project Maintenance window                    |
| Assign cost categories to a project                                            | Budget Maintenance window                     |
| Create cost category budgets                                                   | Budget Detail Entry window                    |
| Assign inventoried items to cost categories                                    | Budget Detail IV Items window                 |
| Set up vendor default entries for profit, purchase order format, and unit cost | PA Vendor Options window                      |

### Setting up project preferences and default entries in Purchase Order Processing

Use the PA Purchase Order Processing Setup window to set up preferences and
default entries that will be used when entering purchase orders, shipment
receipts, shipment/invoice receipts, and invoice receipts for projects.

>   **To set up project preferences and default entries in Purchase Order
>   Processing:**

1.  Open the PA Purchase Order Processing Setup Options window.

>   (Purchasing\>\> Setup \>\> Purchase Order Processing \>\> Project button)

![](media/ed0fa897dfb934bb208ff66bd97e2724.jpg)

1.  Enter purchase order label descriptions for three purchase order formats
    that are available when you are using Project Accounting. These labels will
    be displayed as options in the Purchase Order Format list in the Purchase
    Order Print Options window and the Print Purchasing Documents window.

2.  Enter and attach a default transaction billing note. This note is used only
    when you select None in the Default Billing Note From field. The note will
    be displayed when you enter an item in the Purchase Order Entry window, in
    the Receivings Transaction Entry window, or in the Purchasing Invoice Entry
    window.

3.  Select the default billing note to be displayed when entering items in the
    Purchase Order Entry window, in the Receivings Transaction Entry window, or
    in the Purchasing Invoice Entry window.

>   **Budget** Select to use the billing note entered for the cost category in
>   the project budget.

>   **Cost Category** Select to use the billing note entered for the cost
>   category record.

>   **None** Select to use the billing note entered as the default transaction
>   billing note.

1.  Enter the cost description that will be assigned to invoice receipts. The
    cost description will be displayed as the collective name of invoice
    receipts in Project Accounting windows such as the Project Billing Settings
    window, Contract Settings window, and Budget Maintenance window.

2.  Select to update periodic budget amounts for actual costs using the document
    date or posting date of invoice receipts.

**P A R T 1** S E T U P A N D C A R D S

1.  Select the unit cost to use for project line items when entering purchase
    orders and receipts.

>   **Budget** Select to use the unit cost entered for the cost category in the
>   project budget.

>   **Cost Category** Select to use the unit cost entered for the cost category
>   record.

>   **None** Select if you don’t want to use a default unit cost.

1.  Enter a percentage of how much the unit cost of an invoice receipt can
    exceed the unit cost of a purchase order that the invoice receipt is matched
    to. To vary the unit cost by an unlimited amount, mark the Exceed PO Unit
    Cost option in the scrolling window.

2.  Select the default profit type when entering invoice receipts.

>   **Budget** Select to use the profit type entered for the cost category in
>   the project budget.

>   **Cost Category** Select to use the profit type entered for the cost
>   category record.

>   **Vendor** Select the profit type entered for the vendor record in the PA
>   Vendor Options window.

1.  Select the default inventory item price level when entering invoice
    receipts.

>   **Budget** Select to use the default price level entered for the item in the
>   cost category in a project budget.

>   **Cost Category** Select to use the default price level entered for the item
>   in the Item Price List Maintenance window.

>   **None** Select if you want to enter the price level when entering invoice
>   receipts.

1.  You can enter user-defined field labels to track information about invoice
    receipts.

2.  In the scrolling window, mark the Allow check boxes next to the options that
    you want to use. You can assign passwords to the options to restrict who has
    access to them. If an option is marked, but no password is entered, anyone
    with access to the affected window can perform the action. You can select to
    allow the following options.

>   **Override Document Number PO** Select this option to change the purchase
>   order number that appears as a default entry in the Purchase Order Entry
>   window. If you don't mark this option, the PO Number field in the Purchase
>   Order Entry window will display the next number available. The number can’t
>   be changed.

>   **Override Document Number PI** Select this option to change the document
>   number that appears as a default entry in the Purchasing Invoice Entry
>   window. If you don't mark this option, the Document Number field in the

32 P U R C H A S E O R D E R P R O C E S S I N G

**C H A P T E R 4** P R O J E C T S E T U P F O R P U R C H A S E O R D E R P R
O C E S S I N G

>   Purchasing Invoice Entry window will display the next number available. The
>   number can’t be changed.

>   **Allow Zero Quantity** Select this option to enter a zero quantity for
>   purchase orders and invoice receipts.

>   **Allow Zero Unit Costs** Select this option to enter a zero unit cost for
>   purchase orders and invoice receipts.

>   **Exceed Total Budget Quantity PO** Select this option to enter a quantity
>   for a purchase order that exceeds the Forecast quantity set in the Budget
>   Detail Entry window.

>   **Exceed Total Budget Costs PO** Select this option to use a total cost for
>   a purchase order that exceeds the Forecast total cost set in the Budget
>   Detail Entry window.

>   **Exceed Total Budget Quantity PI** Select this option to enter a quantity
>   for an invoice receipt that exceeds the Forecast quantity set in the Budget
>   Detail Entry window.

>   **Exceed Total Budget Costs PI** Select this option to use a total cost for
>   an invoice receipt that exceeds the Forecast total cost set in the Budget
>   Detail Entry window.

>   **Exceed Total Budget Revenue/Profit** Select this option to use a total
>   cost that exceeds the Forecast revenue set in the Budget Detail Entry
>   window.

>   **Exceed Total PO Costs** Select this option to enter invoice receipts that
>   exceed the total cost specified in purchase orders.

>   **Exceed PO Unit Cost** Select this option to enter invoice receipts that
>   exceed the unit costs specified in purchase orders.

>   **Allow Receiving of Unprinted PO** Select this option to receive against
>   unprinted purchase orders.

>   Choose OK.

Part 2: Purchase orders
=======================

>   This part of the documentation explains how to enter, print, issue, and
>   manage purchase orders. The data entry windows were designed to resemble
>   actual purchase order documents, with vendor, line item, and totals
>   information.

>   Following is a list of topics that are discussed:

-   *Chapter 5, “Multicurrency transactions,”* describes the effects of using
    Multicurrency Management with Purchase Order Processing.

-   *Chapter 6, “Purchase order entry,”* describes how to enter and print
    purchase order information.

-   *Chapter 7, “Purchase order entry for projects,”* describes how to enter
    purchase order information for projects.

-   *Chapter 8, “Purchase order detail entry,”* describes how to enter detailed
    information about a purchase order, vendor, line item, or other elements of
    a transaction.

-   *Chapter 9, “Purchase order generator,”* explains how to automatically
    generate purchase orders to replenish inventory based on a reorder point you
    specify.

-   *Chapter 10, “Taxes for purchase orders,”* explains how tax is calculated,
    modified, and distributed for purchase orders.

-   *Chapter 11, “Purchase order maintenance,”* explains how to correct, delete,
    and void purchase orders. It also explains purchase order statuses and
    holds.

Chapter 5: Multicurrency transactions
-------------------------------------

>   If you’re using Multicurrency Management with Purchase Order Processing, you
>   can choose the currency you want to enter on purchase orders and receipts.

>   This information is divided into the following sections:

-   *Viewing multiple currencies*

-   *Exchange rate and document date*

-   *Multicurrency account distributions*

### Viewing multiple currencies

>   You can choose whether you want to view multicurrency transactions in the
>   originating or the functional currency. Choose View \>\> Currency \>\>
>   Functional or Originating while entering a purchase order or receipt. The
>   option will be saved on a per user, per window basis.

>   You also can use the currency list button in the windows that support
>   changing the currency view. The View \>\> Currency menu options and currency
>   list button are available in the following windows:

-   Purchase Order Entry

-   Receivings Transaction Entry

-   Purchasing Invoice Entry

>   The first time you open these windows after registering Multicurrency

>   Management, all the transactions will be displayed in the originating
>   currency. If you change the currency view, the option you last used will be
>   the default view the next time you open that window.

### Exchange rate and document date

>   If a transaction’s currency ID is not in the functional currency, a rate
>   type and associated exchange rate table are assigned to the transaction. The
>   rate type is based on the rate type you’ve assigned to the selected vendor.
>   If one isn’t assigned to the vendor, the default rate type for the
>   Purchasing series specified in the Multicurrency Setup window is used. You
>   also can choose the currency expansion button to open the Exchange Rate
>   Entry window to view or modify the default exchange rate.

>   The document date (receipt or invoice date) assigned to a transaction
>   determines which exchange rate is used, based on the currency ID and
>   associated rate type that’s entered for the transaction. Each time you
>   change the document date on a multicurrency transaction, the system searches
>   for a valid exchange rate. If a valid rate doesn’t exist, you can enter an
>   exchange rate using the Exchange Rate Entry window. If you’ve entered a
>   General Ledger posting date that’s different from the document date, the
>   exchange rate expiration date must be after the posting date.

### Multicurrency account distributions

>   For multicurrency transactions, distribution amounts are displayed in both
>   the functional and originating currencies. However, you can change only the
>   originating amounts.

>   When you’re entering a multicurrency transaction, the originating debit and
>   credit amounts must balance. If the functional equivalents don’t balance,
>   the difference is posted automatically to a Rounding Difference account and
>   a distribution type of Round identifies the distribution amount in the
>   Purchasing Distribution Entry window.

>   For example, assume you’ve entered an invoice in the euro currency, with an
>   amount of 28,755.42 EUR, a trade discount of 586.84 EUR, a discount
>   available of 1544.33 EUR and the exchange rate is 1.0922. The distributions
>   would be calculated as follows:

| **Account**      | **Euro debit** | **Euro credit** | **US Dollars debit** | **US Dollars credit** |
|------------------|----------------|-----------------|----------------------|-----------------------|
| Accounts Payable |                | 28,755.42 EUR   |                      | \$31,406.67           |
| Trade Discount   |                | 586.84 EUR      |                      | \$640.95              |
| Discount         |                | 1544.33 EUR     |                      | \$1686.72             |
| Accrued          | 30,886.59 EUR  |                 | \$33,734.33          |                       |
| Totals           | 30,886.59 EUR  | 30,886.59 EUR   | \$33,734.34          | \$33,734.33           |
| Rounding         |                |                 | \$0.01               |                       |
| Totals           | 30,886.59 EUR  | 30,886.59 EUR   | \$33,734.34          | \$33,734.34           |

>   Available

>   Purchases

>   Difference

Chapter 6: Purchase order entry
-------------------------------

>   Entering purchase orders is a common routine in many businesses. You can
>   enter four types of purchase orders. The following table describes the types
>   of purchase orders you can enter.

| **Purchase order type** | **Description**                                                                                                                                                                                                                       |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard                | A document that lists items that will be shipped to your business to be received into your inventory.                                                                                                                                 |
| Drop-ship               | A document that lists items that will be shipped directly to the customer. The vendor sends you an invoice and you, in turn, send an invoice to the customer.                                                                         |
| Blanket                 | A document that lists a single item and the quantities that will be delivered in a series of shipments, usually on specific dates. The item will be shipped to your business to be received into your inventory.                      |
| Blanket drop-ship       | A document that lists a single item and the quantities that will be delivered to the customer in a series of shipments, usually on specific dates. The vendor sends you an invoice and you, in turn, send an invoice to the customer. |

>   If you are using Project Accounting, see *Chapter 7, “Purchase order entry
>   for projects,”* to enter purchase orders for projects. You can’t enter
>   blanket purchase orders or drop-ship blanket purchase orders for projects.

>   This information is divided into the following sections:

-   *Purchase order approval workflow*

-   *Prepayment for purchase orders*

-   *Entering a standard purchase order*

-   *Entering a drop-ship purchase order*

-   *Entering a blanket purchase order*

-   *Entering a drop-ship blanket purchase order*

-   *Entering a prepayment for a purchase order*

-   *Copying a purchase order*

-   *Committing purchase orders to sales documents*

-   *Quantity Tolerances in Purchase Order Processing*

-   *Print options for purchase orders*

-   *Requirements for sending purchase orders in e-mail*

-   *Printing and sending an individual purchase order in e-mail*

-   *Printing and sending multiple purchase orders in e-mail*

-   *Printing an individual blanket purchase order delivery schedule*

-   *Printing multiple blanket purchase order delivery schedules*

### Purchase order approval workflow

>   If your company uses the Workflow feature among its business controls,
>   purchase orders might have to be approved before receiving or invoicing
>   items. The rules for approving purchase orders can be defined to fit your
>   organization’s needs. Multiple approvers might be required, or approval
>   might not be required for purchase orders with certain buyers or small
>   currency amounts. When a purchase order is ready to be approved, approvers
>   can be notified and the purchase orders can be approved, using Microsoft
>   Office Outlook®, Microsoft Dynamics GP, or SharePoint®. After a purchase
>   order is approved, it can be printed, sent in e-mail, received, or invoiced
>   against. For more information about Workflow, see the System Setup Guide
>   (Help \>\> Printable Manuals \>\> select System \>\> select System Setup
>   Guide).

>   Before you can use the purchase order approval workflow for Purchase Order

>   Processing, you must unmark the Activate Approvals option in the PO
>   Enhancements Setup window (Purchasing \>\> Setup \>\> Purchase Order
>   Enhancements).

### Prepayment for purchase orders

>   By marking the Allow Purchase Order Prepayments option in the Purchase Order
>   Processing Setup window, you can enter a prepayment amount for a purchase
>   order and generate the prepayment as computer check in Payables Management.
>   You can enter a prepayment for a New, Released, or Change Order purchase
>   order that hasn't been received or invoiced against. You can only enter one
>   prepayment for each purchase order. To enter a manual prepayment for
>   purchase order, the Create manual prepayment from Purchase Order Processing
>   option must be marked in the Purchase Order Processing Setup window.

>   After entering a prepayment amount, you can choose the Prepayment expansion
>   button to open the Purchasing Prepayment Entry window. If the prepayment is
>   a computer check and you have set up a default prepayment account, you don't
>   have to open the Purchasing Prepayment Entry window unless you want to
>   change the default prepayment account. If the prepayment is a manual
>   payment, you can use the Purchasing Prepayment Entry window to enter
>   information such as the prepayment account, payment type, and payment
>   method.

>   When you save a purchase order that has a computer check prepayment entered
>   for it, the payment information is saved, but not posted. The prepayment is
>   posted when completing a computer check run for the prepayment in Payables
>   Management. If you have entered a manual prepayment for the purchase order,
>   the manual prepayment is posted to Payables Management when saving the
>   purchase order, creating a posted manual payables payment.

>   You can receive or invoice against the purchase order after you post the
>   prepayment for the purchase order. When you receive or invoice against the
>   purchase order with a posted prepayment, the posted prepayment is applied to
>   the shipment/invoice or invoice. If items for a purchase order are fully
>   received or invoiced against when posting a shipment/invoice or invoice, any
>   remaining prepayment amount is an unapplied payment in Payables Management.
>   You can apply the remaining prepayment using the Apply Payables Documents
>   window to other documents for the vendor. A purchase order with a prepayment
>   must be closed or canceled before the unapplied payment can be applied.

### Entering a standard purchase order

>   Use the Purchase Order Entry window to enter purchase orders. You can use
>   this window to modify purchase orders with New, Released, and Change Order
>   statuses. You also can enter detailed information for each purchase order
>   and enter non-inventoried items.

>   *If you are using Project Accounting, see Chapter 7, “Purchase order entry
>   for projects” to enter purchase orders for projects.*

>   From the Actions button, you can select Create and Copy New PO to create a
>   new purchase order record from an existing purchase order. You also can
>   select Copy PO Lines to Current PO from the Actions button to copy line
>   items from one purchase order to another. See *Copying a purchase order* or
>   *Copying purchase order line items* for more information.

>   You also can select options from the Actions button to open additional
>   windows where you can receive items, receive and invoice items, or invoice
>   the items from the purchase order. See *Receiving items from a purchase
>   order* or *Invoicing items from a purchase order* for more information.

>   Use the View \>\> Currency menu option or the currency list button to view
>   amounts in the Purchase Order Entry window in the originating or functional
>   currency.

>   **To enter a standard purchase order:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Standard Purchase Order to
    open the Purchase Order Entry window.

![](media/759bdcaf0910602d2bfaa684ca52794c.jpg)

1.  Enter a purchase order number or accept the default entry.

2.  Enter or select a buyer ID.

3.  Accept the default date or enter a date that will be used to update your
    purchasing records.

>   In multicurrency transactions, the exchange rate used is based on the
>   document date, the currency ID, and associated rate type that’s entered for
>   the transaction.

1.  Choose the Date expansion button to open the Purchasing Date Entry window,
    where you can enter a contract expiration date for the purchase order.
    Choose OK to return to the Purchase Order Entry window.

2.  Mark the Allow Sales Document Commitments option to allow purchase order
    line items to be committed to matching sales order line items.

>   The Link Purchase Order icon will be displayed in the Quantity Ordered field
>   for line items with sales commitments. Select the line item and choose the
>   button next to the Quantity Ordered heading to view, add, or delete
>   commitments in the Sales Commitments for Purchase Order window. For more
>   information, see *Committing purchase orders to sales documents*.

1.  Enter or select the vendor that you’re ordering the item from.

>   *To enter a temporary vendor—a vendor with whom you have a short-term
>   relationship and want to keep minimal information—place the pointer in the
>   Vendor ID field and choose Options \>\> Temporary Vendor. The Vendor
>   Maintenance window will open, where you can enter a vendor name and any
>   other information.*

1.  Choose the Vendor E-mail Detail Entry expansion button to open the
    Purchasing E-mail Detail Entry window to update a vendor's e-mail
    information for a purchase order. See *Updating a vendor’s e-mail
    information for a purchase order* for more information.

>   The document type to send in e-mail must be available for the vendor before
>   you can open the Purchasing E-mail Detail Entry window.

1.  Enter or select a currency ID, or change the default currency ID.

>   If the currency ID is not the company’s functional currency, a rate type and
>   associated exchange rate table is assigned to the transaction.

1.  Enter or select the number of the vendor item or item you’re purchasing. If
    a vendor item or an item hasn’t been set up in your inventory, see *Adding a
    vendor item*, *Adding an item to inventory*, or *Using non-inventoried
    items* for more information.

    -   The item number will be displayed if Options \>\> Display Vendor Item is
        unmarked. If Display Vendor Item is marked, the vendor item will be
        displayed.

    -   To indicate that an item must be a specific manufacturer’s item, choose
        the

>   Manufacturer’s Item Number expansion button to open the Purchasing
>   Manufacturer’s Item Number Entry window. See *Specifying the manufacturer’s
>   item numbers to print on a purchase order* for more information.

-   To view or enter additional information for a vendor item, item, or
    noninventoried item, open the Purchasing Item Detail Entry window by
    choosing Item or Vendor Item expansion button. For more information, see
    *Entering line item detail information*.

-   To add an attachment to the item, select the item and choose the Attachment
    Management icon to open the Document Attachment Management window.

1.  Enter the item quantity.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can modify the default unit cost.

3.  Enter a site ID, or accept the default site.

>   *Sites are required for line items. You must enter a site ID before
>   continuing to the next line.*

1.  Continue to enter all the line items for the purchase order.

2.  Enter a prepayment amount, if applicable. This field is available if you
    have marked Allow Purchase Order Prepayments in the Purchase Order
    Processing Setup window. To enter a manual payment, the Create manual
    prepayment from Purchase Order Processing must be marked as well. You can
    enter a prepayment for a New purchase order, a Released or Change Order
    purchase order that hasn’t been received or invoiced against. You can only
    enter one prepayment for each purchase order.

>   You can choose the Prepayment expansion button to open the Purchasing
>   Prepayment Entry window to enter or view computer check or manual check
>   information. If the prepayment is a computer check and you have set up a
>   default prepayment account, you don’t have to open the Purchasing Prepayment
>   Entry window unless you want to change the default prepayment account.

>   If the prepayment is a manual payment, use the Purchasing Prepayment Entry
>   window to enter information such as the prepayment account, payment type,
>   and payment method. See See “Entering a prepayment for a purchase order”.
>   for more information.

1.  Enter a tax schedule ID or accept the default entry. This tax schedule ID
    will be used to calculate tax on the amount of the document. See *Default
    tax schedules for purchase orders* for more information about default tax
    schedule IDs for purchase orders.

2.  Enter the trade discount, freight, miscellaneous, and tax amounts. The trade
    discount is automatically calculated if you’ve assigned a trade discount
    percentage to the vendor that you’re purchasing the items from.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 10, “Taxes for purchase
>   orders.”* To change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for purchase orders*. To change the tax amounts
>   for a line item, see *Calculating and distributing detail taxes for purchase
>   order items*.

1.  Enter a comment ID (optional). For more information about comments, see
    *Adding comments to purchasing documents*.

2.  Choose the Attachment Management icon to attach documents to the purchase
    order, if applicable.

3.  Choose File \>\> Print to open the Purchase Order Print Options window,
    where you can print the purchase order, send the purchase order in e-mail,
    or both. (optional).

>   You also can print the purchase order by choosing the printer button or send
>   the purchase order in e-mail by choosing the Send in e-mail button in the
>   upper right of the Purchase Order Entry window.

>   *If you are using purchase order approval workflow, the purchase order must
>   be approved before you can print it. You also can print a purchase order
>   that doesn’t need approval. If you are using vendor approval workflow, the
>   vendors assigned to the purchase orders must be approved or have the
>   workflow status of No Approval Needed.*

>   You can select to send a purchase order in e-mail or print purchase orders
>   in the functional or originating currency by using the currency list button.
>   To send a purchase order in e-mail or print a purchase order in your
>   reporting currency, you must use the Purchase Order Inquiry Zoom window. For
>   more information about reporting currency, see the Multicurrency Management
>   documentation.

1.  Save the purchase order or submit the purchase order for approval, if you
    are using Workflow.

>   If you have entered a prepayment for the purchase order, saving the purchase
>   order saves the computer check prepayment or posts the manual prepayment to
>   Payables Management to create a posted manual payables payment. To post the
>   computer check prepayment, complete a computer check run for the prepayment
>   in Payables Management.

### Entering a drop-ship purchase order

>   Use the Purchase Order Entry window to enter a drop-ship purchase order to
>   purchase items on behalf of a customer. A customer also can be a vendor. The
>   items on the purchase order are shipped directly to the customer without
>   ever being physically received in your inventory. The vendor will invoice
>   your business and you, in turn, will invoice the customer. The quantity on
>   hand isn’t updated in Inventory Control, but the current cost for the
>   drop-shipped items and the item vendor information will be updated when the
>   invoice is posted. If the item uses the Average Perpetual valuation method,
>   the current cost for the drop-shipped item won’t be updated.

>   *If you are using Project Accounting, see Chapter 7, “Purchase order entry
>   for projects” to enter purchase orders for projects*

>   From the Actions button, you can select Create and Copy New PO to create a
>   new purchase order record from an existing purchase order. You also can
>   select Copy PO Lines to Current PO from the Actions button to copy line
>   items from one purchase order to another. See *Copying a purchase order* or
>   *Copying purchase order line items* for more information.

>   You can select Invoice the PO Items from the Actions button to open
>   additional windows where you can invoice the items from the purchase order.
>   See *Invoicing items from a purchase order* for more information.

>   **To enter a drop-ship purchase order:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Drop-Ship Purchase Order to
    open the Purchase Order Entry window.

3.  Enter a purchase order number or accept the default entry.

4.  Enter or select a buyer ID.

5.  Accept the default date or enter a date that will be used to update your
    purchasing records.

>   In multicurrency transactions, the exchange rate used is based on the
>   document date, the currency ID and associated rate type that’s entered for
>   the transaction.

1.  Choose the Date expansion button to open the Purchasing Date Entry window,
    where you can enter a contract expiration date for the drop-ship purchase
    order. Choose OK to return to the Purchase Order Entry window.

2.  Mark Allow Sales Document Commitments to allow purchase order line items to
    be committed to matching sales order line items.

>   The Link Purchase Order icon will be displayed in the Quantity Ordered field
>   for line items with sales commitments. Select the line item and choose the
>   button next to the Quantity Ordered heading to view, add, or delete
>   commitments in the Sales Commitments for Purchase Order window. For more
>   information, see *Committing purchase orders to sales documents*.

1.  Enter or select the vendor that you’re ordering the item from.

>   *To enter a temporary vendor—a vendor with whom you have a short-term
>   relationship and want to keep minimal information—place the pointer in the
>   Vendor ID field and choose Options \>\> Temporary Vendor. The Vendor
>   Maintenance window will open, where you can enter a vendor name and any
>   other information.*

1.  Moving from the Vendor ID field opens the Enter Drop-Ship Customer window.

![](media/67bec0dd11b14ca67ac91c0300592630.jpg)

>   In the Enter Drop-Ship Customer window, enter or select the customer ID and
>   ship-to address ID where the vendor is shipping the items. Choose OK to
>   return to the Purchase Order Entry window.

1.  Choose the Vendor E-mail Detail Entry expansion button to open the
    Purchasing E-mail Detail Entry window to update a vendor's e-mail
    information for a purchase order. See *Updating a vendor’s e-mail
    information for a purchase order* for more information.

>   The document type to send in e-mail must be available for the vendor before
>   you can open the Purchasing E-mail Detail Entry window.

1.  Enter or select the number of the vendor item or item you’re purchasing. If
    a vendor item or an item hasn’t been set up in your inventory, see *Adding a
    vendor item*, *Adding an item to inventory*, or *Using non-inventoried
    items* for more information.

-   The item number will be displayed if Options \>\> Display Vendor Item is
    unmarked. If Display Vendor Item is marked, the vendor item will be
    displayed.

-   To indicate that an item must be a specific manufacturer’s item, choose the

>   Manufacturer’s Item Number expansion button to open the Purchasing
>   Manufacturer’s Item Number Entry window. See *Specifying the manufacturer’s
>   item numbers to print on a purchase order* for more information.

-   To add an attachment to the item, select the item and choose the Attachment
    Management icon to open the Document Attachment Management window.

1.  Enter the item quantity.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can modify the default unit cost.

3.  Enter a site ID, or accept the default site.

>   *Sites are required for line items. You must enter a site ID before
>   continuing to the next line.*

1.  Continue to enter all the line items for the purchase order.

2.  Enter a prepayment amount, if applicable. This field is available if you
    have marked Allow Purchase Order Prepayments in the Purchase Order
    Processing Setup window. To enter a manual payment, the Create manual
    prepayment from Purchase Order Processing must be marked as well. You can
    enter a prepayment for a New purchase order, a Released or Change Order
    purchase order that hasn’t been received or invoiced against. You can only
    enter one prepayment for each purchase order.

>   You can choose the Prepayment expansion button to open the Purchasing
>   Prepayment Entry window to enter or view computer check or manual check
>   information. If the prepayment is a computer check and you have set up a
>   default prepayment account, you don’t have to open the Purchasing Prepayment
>   Entry window unless you want to change the default prepayment account.

>   If the prepayment is a manual payment, use the Purchasing Prepayment Entry
>   window to enter information such as the prepayment account, payment type,
>   and payment method. See See “Entering a prepayment for a purchase order”.
>   for more information.

1.  Enter a tax schedule ID or accept the default entry. This tax schedule ID
    will be used to calculate tax on the amount of the document. See *Default
    tax schedules for purchase orders* for more information about default tax
    schedule IDs for purchase orders.

2.  Enter the trade discount, freight, miscellaneous, and tax amounts for this
    purchase order. The trade discount is automatically calculated if you’ve
    assigned a trade discount percentage to the vendor that you’re purchasing
    the items from.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Tax calculations in Purchase Order
>   Processing*. To change the tax amounts for the document, see *Calculating
>   and distributing summary taxes for purchase orders*. To change the tax
>   amounts for a line item, see *Calculating and distributing detail taxes for
>   purchase order items*.

1.  Enter a comment ID (optional). For more information about comments, see
    *Adding comments to purchasing documents*.

2.  Choose the Attachment Management icon to attach documents to the purchase
    order, if applicable.

3.  Choose File \>\> Print to open the Purchase Order Print Options window,
    where you can print the purchase order, send the purchase order in e-mail,
    or both (optional).

>   You also can print the purchase order by choosing the printer button or send
>   the purchase order in e-mail by choosing the Send in e-mail button in the
>   upper right of the Purchase Order Entry window.

>   You can select to send purchase orders in e-mail or print purchase orders in
>   the functional or originating currency by using the currency list button.

>   *If you are using purchase order approval workflow, the purchase order must
>   be approved before you can print it. You also can print a purchase order
>   that doesn’t need approval. If you are using vendor approval workflow, the
>   vendors assigned to the purchase orders must be approved or have the
>   workflow status of No Approval Needed.*

1.  Save the purchase order or submit the purchase order for approval, if you
    are using Workflow.

>   If you have entered a prepayment for the purchase order, saving the purchase
>   order saves the computer check prepayment or posts the manual prepayment to
>   Payables Management to create a posted manual payables payment. To post the
>   computer check prepayment, complete a computer check run for the prepayment
>   in Payables Management.

### Entering a blanket purchase order

>   Use the Purchase Order Entry window to enter blanket purchase orders. A
>   blanket purchase order lists a single item and its quantities that will be
>   delivered in a series of shipments, usually on specific dates. The line
>   items you enter for a blanket purchase order must be the same item number.
>   The item will be shipped to your business to be received into your
>   inventory.

>   Blanket purchase orders allow you to make long-term agreements with vendors
>   to purchase the same item—usually to receive a volume discount or to be sure
>   of obtaining items that are hard to get. The agreement you make with the
>   vendor can be based on the total cost of the item or on the total quantity
>   of the item. You’ll use the Purchasing Blanket Detail Entry window to enter
>   line items for the blanket purchase order.

>   The first line item entered for a blanket purchase order is called the
>   control blanket line item and has the line number 0. This is the line item
>   that the blanket line items are based on. For example, you might enter a
>   quantity of 5,000 for the control blanket line item and then enter five
>   blanket line items with a quantity of 1,000 each. The control blanket line
>   item isn’t included in tax amounts, in the purchase order’s subtotal, or
>   printed on purchase orders. If you delete the control blanket line item, all
>   blanket line items are deleted. A control blanket line item can’t be deleted
>   if a blanket line item has been received against. Unlike blanket line items,
>   the control blanket line item can’t be received or invoiced against.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Cat. ID field will be displayed in the Purchase Order Entry window, but you
>   can’t enter project information.

>   From the Actions button, you can select Create and Copy New PO to create a
>   new purchase order record from an existing purchase order. See *Copying a
>   purchase order* for more information.

>   You also can select options from the Actions button to open additional
>   windows where you can receive items, receive and invoice items, or invoice
>   the items from the purchase order. See *Receiving items from a purchase
>   order* or *Invoicing items from a purchase order* for more information.

>   Use the View \>\> Currency menu option or the currency list button to view
>   amounts in the Purchase Order Entry window in the originating or functional
>   currency.

>   **To enter a blanket purchase order:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Blanket Purchase Order to open
    the Purchase Order Entry window.

3.  Enter a purchase order number or accept the default entry.

4.  Enter or select a buyer ID.

5.  Accept the default date or enter a date that will be used to update your
    purchasing records.

>   In multicurrency transactions, the exchange rate used is based on the
>   document date, the currency ID, and associated rate type that’s entered for
>   the transaction.

1.  Choose the Date expansion button to open the Purchasing Date Entry window,
    where you can enter a contract expiration date for the blanket purchase
    order. Choose OK to return to the Purchase Order Entry window.

>   Enter or select the vendor that you’re purchasing items from.

>   *To enter a temporary vendor—a vendor with whom you have a short-term
>   relationship and want to keep minimal information—place the pointer in the
>   Vendor ID field and choose Options \>\> Temporary Vendor. The Vendor
>   Maintenance window will open, where you can enter a vendor name and any
>   other information.*

1.  Choose the Vendor E-mail Detail Entry expansion button to open the
    Purchasing E-mail Detail Entry window to update a vendor's e-mail
    information for a purchase order. See *Updating a vendor’s e-mail
    information for a purchase order* for more information.

>   The document type to send in e-mail must be available for the vendor before
>   you can open the Purchasing E-mail Detail Entry window.

1.  Enter or select a currency ID, or change the default currency ID.

>   If the currency ID is not the company’s functional currency, a rate type and
>   associated exchange rate table is assigned to the transaction.

1.  Mark the Allow Sales Document Commitments option to allow blanket purchase
    order line items to be committed to matching sales order line items.

>   The Link Purchase Order icon will be displayed in the Quantity Ordered field
>   for blanket line items with sales commitments. Select the blanket line item
>   and choose the button next to the Quantity Ordered heading to view, add, or
>   delete commitments in the Sales Commitments for Purchase Order window. You
>   can’t add commitments to the control blanket line item. For more
>   information, see *Committing purchase orders to sales documents*.

1.  Enter or select the number of the vendor item or item you’re purchasing that
    will be the control blanket line item. If a vendor item or an item hasn’t
    been set up in your inventory, see *Adding a vendor item*, *Adding an item
    to inventory*, or *Using non-inventoried items* for more information.

    -   The item number will be displayed if Options \>\> Display Vendor Item is
        unmarked. If Display Vendor Item is marked, the vendor item will be
        displayed.

    -   To indicate that an item must be a specific manufacturer’s item, choose
        the

>   Manufacturer’s Item Number expansion button to open the Purchasing
>   Manufacturer’s Item Number Entry window. See *Specifying the manufacturer’s
>   item numbers to print on a purchase order* for more information.

-   To add an attachment to the item, select the item and choose the Attachment
    Management icon to open the Document Attachment Management window.

1.  Enter the maximum quantity of the item to order.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can edit the default unit cost.

3.  Enter a site ID, or accept the default.

>   *Sites are required for line items. You must enter a site ID before
>   continuing to the next line.*

1.  If the agreement you made with the vendor is based on the total cost of the
    item, modify the extended cost to match the agreed cost.

2.  Choose Blanket to open the Purchasing Blanket Detail Entry window to enter
    line items for the blanket purchase order and to select which line items
    will be released to the vendor when the blanket purchase order is printed.

![](media/e37bba7dbc99959b8512a2650305090b.jpg)

1.  If the agreement you made with the vendor is based on the total quantity,
    mark Quantity to control the blanket by. If the agreement you made with the
    vendor is based on the total cost of the item, mark Value to control the
    blanket by. If you are managing the blanket by value, you still must enter
    quantities for the blanket purchase order’s delivery schedule.

2.  Enter line items using different required dates and quantities, as
    necessary. You also can mark each line item to be released to the vendor
    when the purchase order is printed.

>   When you’ve finished entering line items, choose OK to return to the
>   Purchase Order Entry window.

1.  Enter a prepayment amount, if applicable. This field is available if you
    have marked Allow Purchase Order Prepayments in the Purchase Order
    Processing Setup window. To enter a manual payment, the Create manual
    prepayment from Purchase Order Processing must be marked as well. You can
    enter a prepayment for a New purchase order, a Released or Change Order
    purchase order that hasn’t been received or invoiced against. You can only
    enter one prepayment for each purchase order.

>   You can choose the Prepayment expansion button to open the Purchasing
>   Prepayment Entry window to enter or view computer check or manual check
>   information. If the prepayment is a computer check and you have set up a
>   default prepayment account, you don’t have to open the Purchasing Prepayment
>   Entry window unless you want to change the default prepayment account.

>   If the prepayment is a manual payment, use the Purchasing Prepayment Entry
>   window to enter information such as the prepayment account, payment type,
>   and payment method. See *Entering a prepayment for a purchase order* for
>   more information.

1.  Enter a tax schedule ID or accept the default entry. This tax schedule ID
    will be used to calculate tax on the amount of the document. See *Default
    tax schedules for purchase orders* for more information about default tax
    schedule IDs for purchase orders.

2.  Enter the trade discount, freight, miscellaneous, and tax amounts. The trade
    discount is automatically calculated if you’ve assigned a trade discount
    percentage to the vendor that you’re purchasing the items from.

>   Taxes will be calculated automatically as you enter items. The control
>   blanket line item isn’t included when calculating taxes. For more
>   information about tax calculations, see *Chapter 10, “Taxes for purchase
>   orders.”* To change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for purchase orders*. To change the tax amounts
>   for a line item, see *Calculating and distributing detail taxes for purchase
>   order items*.

1.  Enter a comment ID (optional). For more information about comments, see
    *Adding comments to purchasing documents*.

2.  Choose the Attachment Management icon to attach documents to the purchase
    order, if applicable.

3.  Choose File \>\> Print to open the Purchase Order Print Options window,
    where you can print the purchase order or a blanket purchase order delivery
    schedule. You also can send the purchase order in e-mail (optional).

>   You also can print the purchase order by choosing the printer button or send
>   the purchase order in e-mail by choosing the Send in e-mail button in the
>   upper right of the Purchase Order Entry window.

>   *If you are using purchase order approval workflow, you can print the
>   purchase order delivery schedule, but the purchase order must be approved
>   before you can print it or send it in e-mail. You also can print a purchase
>   order or send a purchase order in e-mail that doesn’t need approval. If you
>   are using vendor approval workflow, the vendors assigned to the purchase
>   orders must be approved or have the workflow status of No Approval Needed.*

>   You can select to send purchase orders in e-mail or print purchase orders in
>   the functional or originating currency using the currency list button in the
>   Purchase Order Entry window. To send a purchase order in e-mail or print a
>   purchase order in your reporting currency, you must use the Purchase Order
>   Inquiry Zoom window. For more information about reporting currency, see the
>   Multicurrency Management documentation.

>   You also can select to print blanket purchase order delivery schedules in
>   the functional or originating currency using the currency list button. To
>   print blanket purchase order delivery schedule in your reporting currency,
>   you must use the Purchase Order Inquiry Zoom window.

1.  Save the purchase order or submit the purchase order for approval, if you
    are using Workflow.

>   If you have entered a prepayment for the purchase order, saving the purchase
>   order saves the computer check prepayment or posts the manual prepayment to
>   Payables Management to create a posted manual payables payment. To post the
>   computer check prepayment, complete a computer check run for the prepayment
>   in Payables Management.

Entering a drop-ship blanket purchase order
-------------------------------------------

>   Use the Purchase Order Entry window to enter a drop-ship blanket purchase
>   order to purchase items on behalf of a customer. A customer also can be a
>   vendor. A dropship blanket purchase order lists a single item and the
>   quantities that will be delivered to the customer in a series of shipments,
>   usually on specific dates. The items on the drop-ship blanket purchase order
>   are shipped directly to the customer without ever being physically received
>   in your inventory. The vendor will send an invoice to your business and you,
>   in turn, will send an invoice to the customer.

>   Blanket purchase orders allow you to make long-term agreements with vendors
>   to purchase the same item—usually to receive a volume discount or to be sure
>   of obtaining hard to get items. The agreement you make with the vendor can
>   be based on the total cost of the item or for the total quantity of the
>   item.

>   The quantity on hand isn’t updated in Inventory Control, but the current
>   cost for the drop-shipped item and the item vendor information will be
>   updated when the invoice is posted. If the item uses the Average Perpetual
>   valuation method, the current cost for the drop-shipped item won’t be
>   updated.

>   The first line item entered for a drop-ship blanket purchase order is called
>   the control blanket line item and it has the line number of 0. This is the
>   line item that the blanket line items are based on. For example, you might
>   enter a quantity of 5,000 for the control blanket line item and then enter
>   five blanket line items with a quantity of 1,000 each. The control blanket
>   line item isn’t included in tax amounts, in the purchase order’s subtotal,
>   or printed on purchase orders. If you delete the control blanket line item,
>   all blanket line items are deleted. A control blanket line item can’t be
>   deleted if a blanket line item has been received against. Unlike blanket
>   line items, the control blanket line item can’t be received or invoiced
>   against.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Cat. ID field will be displayed in the Purchase Order Entry window, but you
>   can’t enter project information.

>   From the Actions button, you can select Create and Copy New PO to create a
>   new purchase order record from an existing purchase order. See *Copying a
>   purchase order* for more information.

>   You also can select Invoice the PO Items from the Actions button to open
>   additional windows where you can invoice the items from the purchase order.
>   See *Invoicing items from a purchase order* for more information.

>   **To enter a drop-ship blanket purchase order:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Drop-Ship Blanket Purchase
    Order to open the Purchase Order Entry window.

3.  Enter a purchase order number or accept the default entry.

4.  Enter or select a buyer ID.

5.  Accept the default date or enter a date that will be used to update your
    purchasing records.

>   In multicurrency transactions, the exchange rate used is based on the
>   document date, the currency ID, and associated rate type that’s entered for
>   the transaction.

1.  Choose the Date expansion button to open the Purchasing Date Entry window,
    where you can enter a contract expiration date for the drop-ship blanket
    purchase order. Choose OK to return to the Purchase Order Entry window.

2.  Enter or select the vendor that you’re ordering the item from.

>   *To enter a temporary vendor—a vendor with whom you have a short-term
>   relationship and want to keep minimal information—place the pointer in the
>   Vendor ID field and choose Options \>\> Temporary Vendor. The Vendor
>   Maintenance window will open, where you can enter a vendor name and any
>   other information.*

1.  Moving from the Vendor ID field opens the Enter Drop-Ship Customer window.

>   In the Enter Drop-Ship Customer window, enter or select the customer ID and
>   ship-to address ID where the vendor is shipping the items to. Choose OK to
>   return to the Purchase Order Entry window.

1.  Choose the Vendor E-mail Detail Entry expansion button to open the
    Purchasing E-mail Detail Entry window to update a vendor's e-mail
    information for a purchase order. See *Updating a vendor’s e-mail
    information for a purchase order* for more information.

>   The document type to send in e-mail must be available for the vendor before
>   you can open the Purchasing E-mail Detail Entry window.

1.  Mark Allow Sales Document Commitments to allow purchase order line items to
    be committed to matching sales order line items.

>   The Link Purchase Order icon will be displayed in the Quantity Ordered field
>   for blanket line items with sales commitments. Select the blanket line item
>   and choose the button next to the Quantity Ordered heading to view, add, or
>   delete commitments in the Sales Commitments for Purchase Order window. You
>   can’t add a sales commitment to the control blanket line item. For more
>   information, see *Committing purchase orders to sales documents*.

1.  Enter or select the number of the vendor item or item you’re purchasing that
    will be the control blanket line item. If a vendor item or an item that
    hasn’t been set up in your inventory, see *Adding a vendor item*, *Adding an
    item to inventory*, or *Using non-inventoried items* for more information.

-   The item number will be displayed if Options \>\> Display Vendor Item is
    unmarked. If Display Vendor Item is marked, the vendor item will be
    displayed.

-   To indicate that an item must be a specific manufacturer’s item, choose the

>   Manufacturer’s Item Number expansion button to open the Purchasing
>   Manufacturer’s Item Number Entry window. See *Specifying the manufacturer’s
>   item numbers to print on a purchase order* for more information.

-   To add an attachment to the item, select the item and choose the Attachment
    Management icon to open the Document Attachment Management window.

1.  Enter the maximum quantity of the item to order.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can modify the default unit cost.

3.  Enter a site ID, or accept the default site.

>   *Sites are required for line items. You must enter a site ID before
>   continuing to the next line.*

1.  If the agreement you made with the vendor is based on the total cost of the
    item, modify the extended cost to match the agreed cost.

2.  Choose Blanket to open the Purchasing Blanket Detail Entry window to enter
    line items for the drop-ship blanket purchase order and to select which line
    items will be released to the vendor when the drop-ship blanket purchase
    order is printed.

3.  If the agreement you made with the vendor is based on the total quantity,
    mark Quantity to control the blanket by. If the agreement you made with the
    vendor is based on the total cost of the item, mark Value to control the
    blanket by. If you are managing the blanket by value, you still must enter
    quantities for the blanket purchase order’s delivery schedule.

4.  Enter line items using different required dates and quantities, as
    necessary. You also can mark each line item to be released to the vendor
    when the purchase order is printed.

>   When you’ve finished entering line items, choose OK to return to the
>   Purchase Order Entry window.

1.  Enter a prepayment amount, if applicable. This field is available if you
    have marked Allow Purchase Order Prepayments in the Purchase Order
    Processing Setup window. To enter a manual payment, the Create manual
    prepayment from Purchase Order Processing must be marked as well. You can
    enter a prepayment for a New purchase order, a Released or Change Order
    purchase order that hasn’t been received or invoiced against. You can only
    enter one prepayment for each purchase order.

>   You can choose the Prepayment expansion button to open the Purchasing
>   Prepayment Entry window to enter or view computer check or manual check
>   information. If the prepayment is a computer check and you have set up a
>   default prepayment account, you don’t have to open the Purchasing Prepayment
>   Entry window unless you want to change the default prepayment account.

>   If the prepayment is a manual payment, use the Purchasing Prepayment Entry
>   window to enter information such as the prepayment account, payment type,
>   and payment method. See See “Entering a prepayment for a purchase order”.
>   for more information.

1.  Enter a tax schedule ID or accept the default entry. This tax schedule ID
    will be used to calculate tax on the amount of the document. See *Default
    tax schedules for purchase orders* for more information about default tax
    schedule IDs for purchase orders.

2.  Enter the trade discount, freight, miscellaneous, and tax amounts for this
    purchase order. The trade discount is automatically calculated if you’ve
    assigned a trade discount percentage to the vendor that you’re purchasing
    the items from.

>   Taxes will be calculated automatically as you enter items. The control
>   blanket line item isn’t included when calculating taxes. For more
>   information about tax calculations, see *Tax calculations in Purchase Order
>   Processing*. To change the tax amounts for the document, see *Calculating
>   and distributing summary taxes for purchase orders*. To change the tax
>   amounts for a line item, see *Calculating and distributing detail taxes for
>   purchase order items*.

1.  Enter a comment ID (optional). For more information about comments, see
    *Adding comments to purchasing documents*.

2.  Choose the Attachment Management icon to attach documents to the purchase
    order, if applicable.

3.  Choose File \>\> Print to open the Purchase Order Print Options window,
    where you can print the purchase order or a blanket purchase order delivery
    schedule, You also can send the purchase order in e-mail (optional).

>   You also can print the purchase order by choosing the printer button or send
>   the purchase order in e-mail by choosing the Send in e-mail button in the
>   upper right of the Purchase Order Entry window.

>   *If you are using purchase order approval workflow, you can print the
>   purchase order delivery schedule, but the purchase order must be approved
>   before you can print it or send it in e-mail. You also can print a purchase
>   order or send a purchase order in e-mail that doesn’t need approval. If you
>   are using vendor approval workflow, the vendors assigned to the purchase
>   orders must be approved or have the workflow status of No Approval Needed.*

>   You can select to send purchase orders in e-mail or print purchase orders in
>   the functional or originating currency using the currency list button in the
>   Purchase Order Entry window. To send a purchase order in e-mail or print a
>   purchase order in your reporting currency, you must use the Purchase Order
>   Inquiry Zoom window. For more information about reporting currency, see the
>   Multicurrency Management documentation.

>   You also can select to print blanket purchase order delivery schedules in
>   the functional or originating currency using the currency list button. To
>   print blanket purchase order delivery schedule in your reporting currency,
>   you must use the Purchase Order Inquiry Zoom window.

1.  Save the purchase order or submit the purchase order for approval, if you
    are using Workflow.

>   If you have entered a prepayment for the purchase order, saving the purchase
>   order saves the computer check prepayment or posts the manual prepayment to
>   Payables Management to create a posted manual payables payment. To post the
>   computer check prepayment, complete a computer check run for the prepayment
>   in Payables Management.

Entering a prepayment for a purchase order
------------------------------------------

>   Use the Purchasing Prepayment Entry window to enter or view computer check
>   or manual payment information for a purchase order. You can enter a
>   prepayment for a New purchase order, a Released or Change Order purchase
>   order that hasn’t been received or invoiced against. You can only enter one
>   prepayment for each purchase order.

>   This window is available for a computer check if you marked the Allow
>   Purchase Order Prepayments option in the Purchase Order Processing Setup
>   window. To enter or view a manual payment, the Create manual prepayment from
>   Purchase Order Processing must be marked as well.

>   **To enter a computer check prepayment for a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order.

2.  Enter a prepayment amount and choose the Prepayment Expansion button.

3.  In the Purchasing Prepayment Entry window, enter or accept the prepayment
    account.

4.  Choose OK to save your changes.

>   **To enter a manual check prepayment for a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order.

2.  Enter a prepayment amount and choose the Prepayment Expansion button.

3.  In the Purchasing Prepayment Entry window, enter or accept the prepayment
    account.

4.  Select Manual Payment as the payment type.

5.  Select Check as the payment method.

6.  Enter or select the checkbook ID you’re using for this transaction.

7.  Enter the number of the check you used to make the payment. The next check
    number specified for checkbook is the default number.

8.  Enter or accept the date of the prepayment.

9.  Enter or accept the payment number of the payment. The next payment number
    displayed in the Payables Setup Options window appears as the default entry.

10. Enter or select the cash account used when posting the prepayment for the
    purchase order.

11. Choose OK to save your changes.

>   **To enter a manual credit card prepayment for a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order.

2.  Enter a prepayment amount and choose the Prepayment Expansion button.

3.  In the Purchasing Prepayment Entry window, enter or accept the prepayment
    account.

4.  Select Manual Payment as the payment type.

5.  Select Credit Card as the payment method.

6.  Enter or select the name of the credit card you’re using for this
    transaction.

7.  Enter or accept the document number for the payment. The payment number is
    the default document number.

8.  Enter or accept the date of the prepayment.

9.  Enter or accept the payment number of the payment. The next payment number
    displayed in the Payables Setup Options window appears as the default entry.

10. Enter or select the accounts payable account used when posting the
    prepayment for the purchase order.

>   If the credit card is used as a credit card, the default account is the
>   accounts payable account for the vendor assigned to the credit card. If the
>   credit card is used as a check card, the default account is the cash account
>   assigned to the checkbook ID.

1.  Choose OK to save your changes.

Copying a purchase order
------------------------

>   Use the Copy a Purchase Order window to create a new purchase order from an
>   existing purchase order. You can copy a blanket purchase order or drop-ship
>   blanket purchase order to another purchase order of the same type.

>   If the new and existing orders have different currencies and neither is the
>   functional currency, amounts are converted from the currency of the existing
>   order to the functional currency and then to the currency for the new order.

>   If the purchase order that you are copying has a prepayment, you will have
>   to enter the prepayment on the new purchase order. If you are using
>   Analytical Accounting, you can copy analysis information assigned to
>   purchase orders or purchase order line items.

>   You can copy a purchase order if you are using Workflow. The new purchase
>   order is assigned a status of Not Submitted.

>   **To copy a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Choose Actions and select Create and Copy New PO to open the Copy a Purchase
    Order window.

2.  Enter or select a purchase order with a status of New, Released, or Change
    Order to copy. You can’t create a new purchase order from a purchase order
    that has project information.

![](media/f6c4036fe8da78a8f312b67bcd2460cb.jpg)

1.  You can change the vendor, currency, and document date for the new order.

2.  For drop-ship purchase orders, enter or select a customer ID and a ship-to
    address ID.

3.  Select a site option. If you select Use Site, enter or select a site.

4.  Enter the required, promise, and promise ship dates.

5.  Select a cost option.

6.  Mark the desired copy options.

7.  You can choose Preview to open the Preview Line Items window, where you can
    mark and modify line items before you copy them. See *Previewing purchase
    order line items* for more information.

8.  Choose Copy.

Committing purchase orders to sales documents
---------------------------------------------

>   Use the Sales Commitments for Purchase Order window to fill sales orders by
>   committing (linking) purchase order line items to Sales Order Processing
>   line items. You can link Sales Order Processing orders or back orders to
>   existing New, Released, or Change Order purchase orders. For more
>   information about linking sales documents to purchase orders, see the Sales
>   Order Processing documentation.

>   If you are using Project Accounting, you can’t commit purchase order line
>   items for projects to Sales Order Processing line items.

>   If you are using Workflow, you can commit purchase orders to sales
>   documents, except for rejected purchase orders. To commit a purchase order
>   that is pending approval, you must be the current approver of the purchase
>   orders.

>   The purchase order must allow sales document commitments, and sales and
>   purchasing line items must meet the following requirements:

-   The purchase order line item that has an uncommitted quantity isn’t the
    control blanket line item for a blanket purchase order or a drop-ship
    blanket purchase order.

-   The uncommitted quantity on the purchase order is equal to or more than the
    quantity required by the sales document.

-   The item numbers match.

-   For inventoried items, the U of M matches if you selected to use the U of M
    from the sales order line in the Sales Order Processing Setup Options
    window. The U of M doesn’t have to match if you selected to use the item’s
    default purchasing U of M.

-   The site ID on the purchase order matches the site ID in the Sales Order
    Processing Setup Options window, if you selected the option Use a Single
    Site for All POs.

-   The site ID on the purchase order matches the site ID on the sales line, if
    you did not select to use a single site for purchase orders in the Sales
    Order Processing Setup Options window.

-   For non-inventoried line items, the item number and U of M match.

-   For drop-ship line items, the customer ID, shipping method, and ship-to
    address match.

>   If a purchase order line item is committed to more than one sales order line
>   item, you can use the Sales Commitments for Purchase Order window to specify
>   the sequence in which the sales line items will be received. You must commit
>   the full quantity of the sales line item to the purchase order line item.
>   Linking a purchase order line item to a sales document will not change
>   purchase order information.

>   **To commit purchase orders to sales documents:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order. Be sure the Allow Sales Document
    Commitments option is marked.

2.  Select a purchase order line item with an uncommitted quantity. Choose the
    Link Purchase Order button on the Quantity Ordered field to open the Sales
    Commitments for Purchase Order window.

>   The item number, description, available quantity, and other information for
>   the item will be displayed. If you selected a line item with existing
>   commitments, sales item information will be displayed in the scrolling
>   window.

![](media/551fa58f5073d7dddfe3c4b91e733595.jpg)

1.  In the Sales Commitments for Purchase Order window, choose the Add Sales Doc
    button to open the Sales Assignments for Purchase Order window, where you
    can select sales line items.

![](media/6829d9f848a45dade3abd3411babcf8b.jpg)

1.  In the Sales Assignments for Purchase Order window, select a sales line item
    and choose the Select button to create a link between the purchase order and
    the line item. The window will close, and information for the sales line
    item you chose will appear in the Sales Commitments for Purchase Order
    window.

>   *A sales line item can be linked to only one purchase order line item, but a
>   purchase order line item can have multiple sales commitments. A drop-ship
>   purchase order or a dropship blanket purchase order can be committed only to
>   drop-ship sales order line items.*

1.  If a line item has more than one Sales Order Processing commitment, you can
    use the arrow buttons in the Sales Commitments for Purchase Order window to
    specify the order in which committed quantities will be received.

>   *To view document information for a Sales Order Processing line item, click
>   on the Sales Document Number link.*

1.  Choose the OK button to save the commitments and return to the Purchase
    Order Entry window.

Quantity Tolerances in Purchase Order Processing
------------------------------------------------

>   You can specify quantity tolerances for shortages and overages for the
>   quantity ordered when receiving against a standard purchase order or a
>   blanket purchase order. Quantity tolerances are not calculated for purchase
>   orders created from Sales Order Processing documents.

>   For inventoried items with an item type of Sales Inventory or Discontinued,
>   you can set up a quantity tolerance for shortages and overages using the
>   Item Purchasing Options Maintenance window. For non-inventoried items, you
>   can set up a quantity tolerance overage and shortage using the Purchase
>   Order Processing Setup window.

>   **Shortage**

>   If the quantity received is short within a certain percentage of the
>   quantity ordered on a standard purchase order or a blanket purchase order,
>   the line item is automatically changed to change order, received, or closed.
>   The status of the line item depends on whether or not the line item has been
>   invoiced.

>   **Example 1**

>   In the following example, a line item is received against and the quantity
>   remaining to receive is within the tolerance.

| Quantity ordered for a purchase order is 100.                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                             |
| You enter a receivings transaction for a quantity of 91.                                                                  |
| The remaining quantity is canceled and the status for the item is Received or Closed if the item has been fully invoiced. |

>   **Example 2**

>   In the following example, a line item is received against multiple times and
>   the receivings transactions are posted.

| Quantity ordered for a purchase order is 100.                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                                                                                             |
| Received and posted a quantity of 75.                                                                                                                                                     |
| The status of the line item and the purchase order is Released.                                                                                                                           |
| If you receive and post a quantity of 14 or less, the line item status remains as Released.                                                                                               |
| If you receive and post a quantity of 15 or more, the remaining quantity of the line item is canceled. The status for the item is Received or Closed if the item has been fully invoiced. |

>   **Example 3**

>   In the following example, a line item assigned to receivings transaction is
>   saved in a batch. The purchase order and line item status is Released.

| Quantity ordered for a purchase order is 100.                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                                                   |
| Purchase Order and line item status is Released.                                                                                                |
| Receive and save a quantity of 75.                                                                                                              |
| The status of the line item and the purchase order is Released.                                                                                 |
| If you receive and post a quantity of 14 or less, the line item status remains as Released.                                                     |
| If you receive and post a quantity of 15 or more, the remaining quantity of the line item is canceled. The status for the item is Change Order. |

>   **Example 4**

>   In the following example, a line item assigned to receivings transaction is
>   saved in a batch. The purchase order and line item status is New.

| Quantity ordered for a purchase order is 100.                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                                   |
| Purchase Order and line item status is New.                                                                                     |
| Receive and save a quantity of 75.                                                                                              |
| The status of the line item and the purchase order is New.                                                                      |
| If a quantity of 14 or less is received and posted, the purchase order and line item have a status of Released.                 |
| If a quantity of 15 or more is received and posted, the remaining amount will be canceled and the line item status is Released. |

>   **Example 5**

>   In the following examples, the item’s quantity is partially rejected. The
>   rejected quantity is a reduction of the quantity received when calculating
>   the shortage tolerance.

| Quantity ordered for a purchase order is 100.                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                                  |
| Receive a quantity of 75 and reject a quantity of 15.                                                                          |
| The status of the line item and the purchase order is Released.                                                                |
| If a quantity of 4 or less is received and posted, the purchase order and line item have a status of Released.                 |
| If a quantity of 5 or more is received and posted, the remaining amount will be canceled and the line item status is Released. |
|                                                                                                                                |
| Receive a quantity of 100 and reject a quantity of 3.                                                                          |
| The status of the line item and the purchase order is Released.                                                                |
| The remaining amount will be canceled and the line item status is Received or Closed if the line item is fully invoiced.       |

>   **Overage**

>   If you are using an overage quantity tolerance for items, you can limit the
>   total quantity you can receive over the quantity ordered on a standard
>   purchase order or blanket purchase order. When the quantity received is over
>   the overage tolerance, you will receive a message that you can't enter a
>   quantity greater than the combined total of the Remaining to Receive
>   quantity and the overage tolerance set up for the item.

>   **Example 1**

>   In the following example, a line item is received against.

| The net quantity order is the quantity order minus the quantity canceled.        |
|----------------------------------------------------------------------------------|
| Purchase order net quantity is 100.                                              |
| Quantity overage tolerance percentage is 10%.                                    |
| No message displays if the receivings transaction has a quantity of 110 or less. |
| Message displays if the receivings transaction has a quantity of 111 or more.    |

>   **Example 2**

>   In the following example, a line item is received against multiple times.

| The net quantity order is the quantity order minus the quantity canceled.                       |
|-------------------------------------------------------------------------------------------------|
| Purchase order net quantity is 100.                                                             |
| Quantity overage tolerance percentage is 10%                                                    |
| You enter a receivings transaction for a quantity of 50.                                        |
| You enter another receivings transaction.                                                       |
| No message displays if the quantity on the receivings transaction has a quantity of 60 or less. |
| Message displays if the quantity on the receivings transaction has a quantity of 61 or more.    |

>   **Example 3**

>   In the following example, an item's quantity is rejected or partially
>   rejected. The rejected quantity is a reduction of the quantity received when
>   calculating the overage tolerance.

| The net quantity order is the quantity order minus the quantity canceled.             |
|---------------------------------------------------------------------------------------|
| Purchase order net quantity is 100.                                                   |
| Quantity overage tolerance percentage is 10%.                                         |
| You enter a receivings transaction for a quantity of 100 and reject a quantity of 10. |
| You enter another receivings transaction.                                             |
| No message displays if the quantity on the transaction has a quantity of 19 or less.  |
| Message displays if the quantity on the transaction has a quantity of 20 or more.     |

Print options for purchase orders
---------------------------------

>   In the Purchase Order Print Options window and the Print Purchasing
>   Documents window, you can select the type of information you want to print
>   on purchase orders. When you send purchase orders to your vendors in e-mail,
>   you use the same options you use as when you are printing purchase orders.
>   The print options that are available depend on the document you are printing
>   or sending in e-mail.

>   **Print Canceled Items** All line items that exist on each purchase order
>   will be printed including line items with a Canceled status, if they were
>   released to the vendor. Line items that changed from New to Canceled (and
>   were never released) will not be printed or sent. Items with a partially
>   canceled quantity are always printed or sent, regardless of whether you mark
>   this option. If you don’t print canceled items, line items that have a
>   Canceled status won’t be printed on the purchase order and the quantity
>   ordered will be reduced by the canceled quantity.

>   For example, assume that you’ve entered a purchase order that has two line
>   items in the Purchase Order Entry window.

| **Item** | **Quantity Ordered** | **Quantity Canceled** | **Unit Cost** | **Extended Cost** | **Status** |
|----------|----------------------|-----------------------|---------------|-------------------|------------|
| Item 1   | 10                   | 1                     | \$1.00        | \$10.00           | Released   |
| Item 2   | 5                    | 5                     | \$1.00        | \$5.00            | Canceled   |

>   The Subtotal amount is \$15.00. The Remaining PO Subtotal amount is \$9.00.

>   If you marked the Print Canceled Items option, the following information
>   would be printed on the purchase order:

| **Item** | **Quantity Ordered** | **Unit Price** | **Extended Price** |
|----------|----------------------|----------------|--------------------|
| Item 1   | 9                    | \$1.00         | \$9.00             |

>   **Include In Totals** Amounts from canceled items will be included in the
>   purchase order total. If you print both canceled line items and their
>   amounts, the quantity ordered for the purchase order is taken from the
>   Quantity Ordered field in the Purchase Order Entry window.

>   Using the information from the previous example, the following information
>   would be printed on the purchase order if you marked the Print Canceled
>   Items and the Include In Totals options:

| **Item** | **Quantity Ordered** | **Unit Price** | **Extended Price** |
|----------|----------------------|----------------|--------------------|
| Item 1   | 10                   | \$1.00         | \$10.00            |
| Item 2   | 5                    | \$1.00         | \$5.00             |

>   The Subtotal amount is \$15.00.

>   If you print canceled line items but not their amounts, the quantity ordered
>   is reduced by the canceled quantity. The following information would be
>   printed:

| **Item** | **Quantity Ordered** | **Unit Price** | **Extended Price** |
|----------|----------------------|----------------|--------------------|
| Item 1   | 9                    | \$1.00         | \$9.00             |
| Item 2   | 0                    | \$1.00         | \$0.00             |

>   The Subtotal amount is \$9.00.

>   **Include POs On Hold** Mark this option to print purchase orders that are
>   on hold. Printing a purchase order that is on hold will not change its
>   status.

>   **Print Reference Number and FOB** The reference number and Free on Board
>   designation are printed in addition to the vendor item number. (The vendor
>   item number is printed on the purchase order regardless of whether you
>   selected to print the reference number.) The reference number is the item
>   number as it was entered in the Item Maintenance window.

>   **Combine Similar Items** Similar items are combined into a single line item
>   when printing a purchase order.

>   Line items on blanket purchase orders and drop-ship blanket purchase orders
>   will not be combined when this option is marked.

>   Similar inventoried items can be combined when the item number, unit of
>   measure, originating unit cost, required date, shipping method, and address
>   information are the same. Similar non-inventoried items can be combined if
>   the item number, vendor item number, unit of measure, originating unit cost,
>   required date, shipping method, and address information are the same. The
>   address information includes name, contact, address, city, state, ZIP code
>   or postal code, and country/region.

>   For example, assume that two different departments submitted requests for a
>   fax machine. Each request was entered as a separate line item on one
>   standard purchase order.

| **Line** | **Item Number** | **Vendor** |
|----------|-----------------|------------|


>   **Item**

**U of M**

**Site**

**Quantity**

**Unit Cost**

**Extended**

>   **Cost**

**Requested by**

| 1 | FAX001   | FAX       | Each | North | 1 | \$450.75 | \$450.75 | Support |   |   |
|---|----------|-----------|------|-------|---|----------|----------|---------|---|---|
| 2 | PHONE001 | TELEPHONE | Each | North | 1 | \$ 75.87 | \$ 75.87 | Support |   |   |
| 3 | FAX001   | FAX       | Each | North | 1 | \$450.75 | \$450.75 | Admin   |   |   |
| 4 | DESK001  | COMPUTER  | Each | South | 1 | \$750.99 | \$750.99 | Admin   |   |   |

>   DESK

>   If you choose to combine similar items on a purchase order and the shipping
>   method and address information are the same for both line items, the
>   following line items would be printed on the purchase order as.

| **Line** | **Item Number** | **Vendor Item** | **U of M** | **Site** | **Quantity** | **Unit Cost** | **Extended Cost** |
|----------|-----------------|-----------------|------------|----------|--------------|---------------|-------------------|
| 1        | FAX001          | FAX             | Each       | North    | 2            | \$450.75      | \$901.50          |
| 2        | PHONE001        | TELEPHONE       | Each       | North    | 1            | \$ 75.87      | \$ 75.87          |
| 4        | DESK001         | COMPUTER        | Each       | South    | 1            | \$750.99      | \$750.99          |

>   DESK

>   When printing a standard or drop-ship purchase order and similar items are
>   combined into a single line item, the purchase order will display the first
>   line number for the combined line items. In the above example, line 1 and
>   line 3 are combined and line 1 will display the combined items.

>   **Reprint Previously Printed POs** Reprint purchase orders that you’ve
>   already printed. When you print a purchase order with a Change Order status,
>   the status of the purchase order changes to Released. This option is
>   available only in the Print Purchasing Documents window.

>   **Print One Purchase Order per Address** Line items that have the same
>   address and shipping method can be included on the same purchase order. For
>   example, assume that you’ve marked the Print One Purchase Order per Address
>   option and have entered the following line item information for PO001, a
>   standard purchase order.

| **Item** | **Shipping method** | **Address**                        |
|----------|---------------------|------------------------------------|
| Item A   | NEXT DAY            | 1234 Allen Street East Chicago, IL |
| Item B   | PICKUP              | 123 West Boardwalk New York, NY    |
| Item C   | NEXT DAY            | 12345 Market Drive Chicago, IL     |
| Item D   | PICKUP              | 123 West Boardwalk New York, NY    |

>   When you print PO001, three separate purchase orders will be printed.

-   A purchase order PO001 for Item A.

-   A purchase order PO001 for Item B and D.

-   A purchase order PO001 for Item C.

>   However, if the Print One Purchase Order per Address option isn’t marked,
>   only one purchase order for PO0001 will be printed. The address and shipping
>   method for each purchase order item will be printed on the purchase order.

>   If you are using Project Accounting, this option will not apply to the
>   purchase order formats that you entered in the PA Purchase Order Processing
>   Setup Options window.

>   **Include Tax Details** The tax details that were used to calculate the tax
>   will be printed directly beneath the item on the document. Each tax detail
>   must have the Print on Documents option in the Tax Detail Maintenance window
>   marked before the tax detail can be printed on documents. Mark Print Dual
>   Currencies to print summary tax information in both the originating and
>   functional currencies on purchase orders that include tax details. Mark Line
>   Item and Summary if you want to include details for line items as well as
>   summary tax information. Mark Summary Taxes Only if you want to include only
>   the summary of tax detail information for each printed document. Summary
>   taxes are printed at the bottom of the document.

Requirements for sending purchase orders in e-mail
--------------------------------------------------

>   You can send purchase orders, drop-ship purchase orders, blanket purchase
>   orders, drop-ship blanket purchases orders in e-mail if the following
>   conditions are met.

-   The document type to send in e-mail must be available for the vendor to send
    in e-mail.

-   At least one e-mail address, To, Cc, or Bcc, must be assigned to the vendor
    using the Internet Information window or the Purchasing E-mail Detail Entry
    window.

-   You can send documents by email if you're using a MAPI-compliant e-mail
    service or Exchange 2007 Service Pack 1 or greater with Exchange Web
    Services.

-   If you are using Exchange 2007 Service Pack 1 or greater with Exchange Web
    Services, the Autodiscover service must be enabled to connect to the
    Exchange server.

-   Word templates for Microsoft Dynamics GP for the vendor and document type
    must be enabled in the Template Configuration Manager window before you can
    send documents as DOCX, PDF, or XPS attachments.

-   Depending on the document type and email service, Microsoft Word 2010 or
    later and Word templates for Microsoft Dynamics GP are required.

| **File format**                                                                                                               | **Word 2010**     | **Word templates** | **Web Client** |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------|--------------------|----------------|
| XPS                                                                                                                           | Required for MAPI | Enabled            | Not available  |
| PDF                                                                                                                           | Required for MAPI | Enabled            | Not available  |
| DOCX                                                                                                                          | Not required      | Enabled            | Available\*    |
| HTML                                                                                                                          | Not required      | Not required       | Available\*    |
| \*Email for Web Client will only be available if you are using Exchange as your server type in the System Preferences window. |                   |                    |                |

-   The file size of the document must not be greater than the maximum file size
    set in the Vendor E-mail Options window.

-   Depending on the file format you choose to send your documents in e-mail,
    your customers and vendors must be using the following components to view
    their documents.

| **File format**                                                                                                                  | **Component**                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| XPS                                                                                                                              | Microsoft XPS Viewer                    |
| PDF                                                                                                                              | Adobe Reader                            |
| DOCX                                                                                                                             | Microsoft Word Viewer                   |
| HTML\*                                                                                                                           | Internet Explorer 8 Internet Explorer 9 |
| \*If you are using Microsoft Dynamics GP Web Client only, your customers and vendors must be using HTML to view their documents. |                                         |

Printing and sending an individual purchase order in e-mail
-----------------------------------------------------------

>   Use the Purchase Order Print Options window to print an individual purchase
>   order when you’ve finished entering it and are satisfied there are no
>   mistakes on it. You also can send the purchase order in e-mail using the
>   Purchase Order Print Options window or by you choosing the Send in e-mail
>   button in the upper right of the Purchase Order Entry window. See *Printing
>   and sending multiple purchase orders in e-mail* for information about
>   printing and sending several purchase orders at once.

>   *If you are using purchase order approval workflow, the purchase order must
>   be approved before you can print or send it. You can print or send a
>   purchase order that doesn’t need approval. If you are using vendor approval
>   workflow, you can print or send a purchase order only if the vendor assigned
>   to the purchase order has been approved or has a workflow status of No
>   Approval Needed.*

>   You also can print and send a historical purchase order in e-mail, which is
>   a closed or canceled purchase order that has been moved to history. To print
>   or send an historical purchase order, you must use the Purchase Order
>   Inquiry Zoom window to open the Purchase Order Print Options window. See
>   *Viewing purchasing documents* for more information.

>   **To print and send an individual purchase order in e-mail:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order.

2.  Choose File \>\> Print to open the Purchase Order Print Options window.

![](media/9f8137d95ed48ef68f59c797cd84d924.jpg)

>   *If you’re using preprinted purchase order forms, we recommend that you
>   print an alignment form. Xs will be printed in the place of the actual
>   purchase order information. Verify that the purchase order forms are aligned
>   correctly.*

1.  Select to print, send the purchase order in e-mail, or both.

2.  Select a format for the purchase order.

>   To send a purchase order in e-mail, the document format must be Blank Paper.

1.  From the currency list button, select whether to print or send the purchase
    order in the functional or originating currency.

>   *To print or send a purchase order in the reporting currency, you must use
>   the Purchase Order Inquiry Zoom window. For more information, see Viewing
>   purchasing documents.*

1.  Select the print options when printing or sending the purchase order. For
    example, you can print canceled items and the totals from the canceled items
    on the purchase orders.

2.  Select whether to include tax details on the document.

3.  Print the purchase order, send the purchase order in e-mail, or both.

>   The status of New purchase orders will be changed to Released when at least
>   one line item on the purchase order changes from New to Released. A Change
>   Order purchase order also changes to Released when printing it or sending it
>   in e-mail results in at least one Released purchase order line item and no
>   remaining Change Order purchase order line items.

>   If you are printing or sending blanket and drop-ship blanket purchase
>   orders, the status of New line items will be changed to Released, if line
>   items have been marked to release in the Purchasing Blanket Detail Entry
>   window. For more information, see *Entering line items with multiple release
>   dates*. For more information about statuses, see *Status overview*.

>   The control blanket line item isn’t printed on the blanket purchase order or
>   the blanket drop-ship purchase order.

Printing and sending multiple purchase orders in e-mail
-------------------------------------------------------

>   Use the Print Purchasing Documents window to print a range of purchase
>   orders when you’ve finished entering them and are satisfied there are no
>   mistakes on them. You also can send a range of purchase orders in e-mail.
>   See *Printing and sending an individual purchase order in e-mail* for
>   information about printing and sending individual purchase orders in e-mail.

>   *If you are using purchase order approval workflow, the purchase order must
>   be approved before you can print or send it. You also can print or send a
>   purchase order that doesn’t need approval. If you are using vendor approval
>   workflow, the vendors assigned to the purchase orders must be approved or
>   have the workflow status of No Approval Needed.*

>   You also can print or send a range of historical purchase orders. A
>   historical purchase order is a closed or canceled purchase order that has
>   been moved to history.

>   **To print and send multiple purchase orders in e-mail:**

1.  Open the Print Purchasing Documents window.

>   (Purchasing \>\> Transactions \>\> Print Purchasing Documents)

![](media/0398681f700a73d2d9330c0564e89307.jpg)

>   *If you’re using preprinted purchase order forms, we recommend that you
>   print an alignment form. X’s will be printed in the place of the actual
>   purchase order information. Verify that the purchase order forms are aligned
>   correctly.*

1.  Select to print or send purchase orders or historical purchase orders.

2.  Select a format for purchase orders.

>   To send a purchase order in e-mail, the document format must be Blank Paper.

1.  Select whether to sort purchase orders by purchase order number or by vendor
    ID.

2.  From the currency list button, select whether to print the purchase orders
    in functional, originating, or reporting currency.

3.  Select the print options when printing purchase orders, sending purchase
    orders in e-mail, or both. For example, you can print canceled items and the
    totals from the canceled items on the purchase orders.

4.  Select which purchase order statuses you want to include.

>   The status of New purchase orders will be changed to Released when at least
>   one purchase order line item changes from New to Released. A Change Order
>   purchase order also changes to Released when printing it or sending it in
>   e-mail results in at least one Released purchase order line and no remaining
>   Change Order purchase order line items.

>   If you are printing or sending blanket and drop-ship blanket purchase
>   orders, the status of New line items will be changed to Released, if line
>   items have been marked to release in the Purchasing Blanket Detail Entry
>   window.

1.  Select a range type and enter starting and ending values for the range.

2.  Choose Insert to move the range restriction you’ve defined into the
    Restrictions list.

>   You can define additional range restrictions, but you can define only one
>   range restriction per range type. For example, you can specify a range of
>   purchase orders and a range of item numbers, but you can’t specify two
>   purchase order ranges.

1.  Print the purchase orders, send the purchase orders in e-mail, or both.

>   The control blanket line item isn’t printed on a blanket purchase order or a
>   blanket drop-ship purchase order.

Printing an individual blanket purchase order delivery schedule
---------------------------------------------------------------

>   Use the Purchase Order Print Options window to print an individual estimated
>   delivery schedule after you’ve finished entering a blanket purchase order or
>   a dropship blanket purchase order. See *Printing multiple blanket purchase
>   order delivery schedules* for information about printing several delivery
>   schedules at once.

>   Printing the delivery schedule won’t release the items to the vendor. To
>   release items to the vendor, print a purchase order.

>   **To print an individual blanket purchase order delivery schedule:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a blanket purchase order or drop-ship blanket purchase
    order.

2.  Choose File \>\> Print to open the Purchase Order Print Options window.

![](media/9f8137d95ed48ef68f59c797cd84d924.jpg)

1.  Select to print a delivery schedule.

2.  From the currency list button, select whether to print in the functional or
    originating currency.

>   *To print a blanket purchase order delivery schedule in the reporting
>   currency, you must use the Purchase Order Inquiry Zoom window. For more
>   information, see Viewing purchasing documents.*

1.  Choose Print to print the delivery schedule.

Printing multiple blanket purchase order delivery schedules
-----------------------------------------------------------

>   Use the Print Purchasing Documents window to print a range of estimated
>   delivery schedules for blanket and drop-ship blanket purchase orders. See
>   *Printing an individual blanket purchase order delivery schedule* for
>   information about printing individual delivery schedule.

>   Printing the delivery schedule won’t release the items to the vendor. To
>   release items to the vendor, print a purchase order.

>   **To print multiple blanket purchase order delivery schedules:**

1.  Open the Print Purchasing Documents window.

>   (Purchasing \>\> Transactions \>\> Print Purchasing Documents)

1.  Select to print delivery schedules.

![](media/0c56d4d21a56a5e5d6feed6964e3837a.jpg)

1.  From the currency list button, select whether to print the delivery
    schedules in functional, originating, or reporting currency.

2.  Select whether or not to include purchase orders that are on hold.

3.  Select a range type and enter starting and ending values for the range.

4.  Choose Insert to move the range restriction you’ve defined into the
    Restrictions list.

>   You can define additional range restrictions, but you can define only one
>   range restriction per range type. For example, you can specify a range of
>   purchase orders and a range of item numbers, but you can’t specify two
>   purchase order ranges.

1.  Choose Print to print the delivery schedules.

Chapter 7: Purchase order entry for projects
============================================

>   If you are using Project Accounting, you can enter standard and drop-ship
>   purchase orders for projects. You can enter blanket and drop-ship blanket
>   purchase orders, but you can’t enter a project number or a cost category for
>   items assigned to those purchase order types. For more information about
>   blanket purchase orders, see *Entering a blanket purchase order*. For more
>   information about drop-ship blanket purchase orders, see *Entering a
>   drop-ship blanket purchase order*.

>   This information is divided into the following sections:

-   *Project numbers and cost categories in Purchase Order Processing*

-   *Entering a standard purchase order for projects*

-   *Entering a drop-ship purchase order for projects*

Project numbers and cost categories in Purchase Order Processing
----------------------------------------------------------------

>   A project number identifies the project where the item in the purchase
>   order, shipment receipt, shipment/invoice receipt or invoice receipt will be
>   used. Each project has its own budget and is made up of cost categories. If
>   an item isn’t assigned to a project, you can enter \<None\> or leave the
>   project number blank. If an item isn’t assigned to a project, the item isn’t
>   assigned to a budget.

>   A cost category is a name given to a project expense, such as, labor,
>   building rental, and materials. When a cost category is used in a project,
>   it is usually called a budget item. Each cost category that is assigned to a
>   project has its own budget. If an item doesn’t have a project number, you
>   don’t have to enter a cost category. You can leave the cost category blank.
>   You must enter a cost category ID if the item you’re entering is part of a
>   project.

Entering a standard purchase order for projects
-----------------------------------------------

>   Use the Purchase Order Entry window to enter purchase orders. A purchase
>   order can involve various projects, cost categories, and items—all of them
>   to be acquired from a single vendor only. You can use this window to modify
>   purchase orders with New, Released, and Change Order statuses. You also can
>   enter detailed information for each purchase order and enter inventoried and
>   non-inventoried items. See *Inventoried items and non-inventoried items for
>   projects* for more information.

>   From the Actions button, you can select Create and Copy New PO to create a
>   new purchase order record from an existing purchase order. You also can
>   select Copy PO Lines to Current PO from the Actions button to copy line
>   items from one purchase order to another. You won’t be able to copy purchase
>   orders or line items that have project numbers and cost categories assigned
>   to them. See *Copying a purchase order* or *Copying purchase order line
>   items* for more information.

>   You also can select options from the Actions button to open additional
>   windows where you can receive items, receive and invoice items, or invoice
>   the items from the purchase order. See *Receiving items from a purchase
>   order* or *Invoicing items from a purchase order* for more information.

>   Use the View \>\> Currency menu option or the currency list button to view
>   amounts in the Purchase Order Entry window in the originating or functional
>   currency.

>   **To enter a standard purchase order for projects:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

![](media/c81bb9d79edf3deaab9c513c95951488.jpg)

1.  Select Standard as the document type.

2.  Enter a purchase order number or accept the default entry.

3.  Enter or select a buyer ID.

4.  Accept the default date or enter a date that will be used to update your
    purchasing records.

>   In multicurrency transactions, the exchange rate used is based on the
>   document date, the currency ID, and associated rate type that’s entered for
>   the transaction.

1.  Enter or select the vendor that you’re ordering the item from.

>   *To enter a temporary vendor—a vendor with whom you have a short-term
>   relationship and want to keep minimal information—place the pointer in the
>   Vendor ID field and choose Options \>\> Temporary Vendor. The Vendor
>   Maintenance window will open, where you can enter a vendor name and any
>   other information.*

1.  Enter or select a currency ID, or change the default currency ID.

>   If the currency ID is not the company’s functional currency, a rate type and
>   associated exchange rate table is assigned to the transaction.

1.  Enter or select the project where an item will be used. If the item that
    you’re purchasing isn’t assigned to a project, enter \<NONE\> or leave the
    Project No. field blank.

>   You cannot enter a project number that belongs to a contract with a status
>   of On Hold, Closed, or Estimate. In addition, you cannot enter a project
>   number for a project, contract, or customer that doesn’t allow you to enter
>   or post cost transactions.

>   **C H A P T E R 7** P U R C H A S E O R D E R E N T R Y F O R P R O J E C T
>   S

>   You can’t enter a project number and a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter or select the cost category where an item will be used. You must enter
    a cost category ID if the item you’re entering is part of a project. If the
    item isn’t a part of a project, leave the Cost Category field blank.

2.  Enter or select the number of the item you’re purchasing. If an item hasn’t
    been set up in your inventory, see *Adding an item to inventory* or *Using
    noninventoried items* for more information.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget. You cannot add a new
>   inventoried item if the Allow Entry of New Budgets/Materials option is not
>   marked in the User Purchase Order Settings window. See *Inventoried items
>   and non-inventoried items for projects* for more information.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter the item quantity.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can modify the default unit cost.

3.  Enter a site ID, or accept the default site.

>   *Sites are required for line items. You must enter a site ID before
>   continuing to the next line.*

1.  Continue to enter all the line items for the purchase order.

2.  Enter a tax schedule ID or accept the default entry. This tax schedule ID
    will be used to calculate tax on the amount of the document. See *Default
    tax schedules for purchase orders* for more information about default tax
    schedule IDs for purchase orders.

3.  Enter the trade discount, freight, miscellaneous, and tax amounts. The trade
    discount is automatically calculated if you’ve assigned a trade discount
    percentage to the vendor that you’re purchasing the items from.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 10, “Taxes for purchase
>   orders.”* You can’t change the Tax amount in the Purchase Order Entry window
>   even if your system is set up to allow editing summary-level taxes in the
>   Company Setup Options window. To change the tax amounts for a line item, see
>   *Calculating and distributing detail taxes for purchase order items*.

1.  Enter a comment ID (optional). For more information about comments, see
    *Adding comments to purchasing documents*.

2.  Choose the Attachment Management icon to attach documents to the purchase
    order, if applicable.

3.  Choose File \>\> Print to open the Purchase Order Print Options window,
    where you can print the purchase order (optional). See *Printing and sending
    an individual purchase order in e-mail* for more information. For
    information about printing several purchase orders at once, see *Printing
    and sending multiple purchase orders in e-mail*.

>   *If you are using purchase order approval workflow, the purchase order must
>   be approved before you can print it. You also can print a purchase order
>   that doesn’t need approval. If you are using vendor approval workflow, the
>   vendors assigned to the purchase orders must be approved or have the
>   workflow status of No Approval Needed.*

>   You can select to print purchase orders in the functional or originating
>   currency using the currency list button. To print a purchase order in your
>   reporting currency, you must use the Purchase Order Inquiry Zoom window. For
>   more information about reporting currency, see the Multicurrency Management
>   documentation.

1.  Save the purchase order or submit the purchase order for approval, if you
    are using Workflow.

Entering a drop-ship purchase order for projects
------------------------------------------------

>   Use the Purchase Order Entry window to enter a drop-ship purchase order to
>   purchase items on behalf of a customer. A customer also can be a vendor. The
>   items on the purchase order are shipped directly to the customer without
>   ever being physically received in your inventory. The vendor will invoice
>   your business and you, in turn, will invoice the customer. The quantity on
>   hand isn’t updated in Inventory Control, but the current cost for the
>   drop-shipped items and the item vendor information will be updated when the
>   invoice is posted. If the item uses the Average Perpetual valuation method,
>   the current cost for the drop-shipped item won’t be updated.

>   You also can enter detailed information for each purchase order and enter
>   inventoried and non-inventoried items. See *Inventoried items and
>   non-inventoried items for projects* for more information.

>   From the Actions button, you can select Create and Copy New PO to create a
>   new purchase order record from an existing purchase order. You also can
>   select Copy PO Lines to Current PO from the Actions button to copy line
>   items from one purchase order to another. You won’t be able to copy purchase
>   orders or line items that have project numbers and cost categories assigned
>   to them. See *Copying a purchase order* or *Copying purchase order line
>   items* for more information.

>   You can select Invoice the PO Items from the Actions button to open
>   additional windows where you can invoice the items from the purchase order.
>   See *Invoicing items from a purchase order* for more information.

>   **To enter a drop-ship purchase order for projects:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Select Drop-Ship as the document type.

2.  Enter a purchase order number or accept the default entry.

>   **C H A P T E R 7** P U R C H A S E O R D E R E N T R Y F O R P R O J E C T
>   S

1.  Enter or select a buyer ID.

2.  Accept the default date or enter a date that will be used to update your
    purchasing records.

>   In multicurrency transactions, the exchange rate used is based on the
>   document date, the currency ID and associated rate type that’s entered for
>   the transaction.

1.  Enter or select the vendor that you’re ordering the item from.

>   *To enter a temporary vendor—a vendor with whom you have a short-term
>   relationship and want to keep minimal information—place the pointer in the
>   Vendor ID field and choose Options \>\> Temporary Vendor. The Vendor
>   Maintenance window will open, where you can enter a vendor name and any
>   other information.*

1.  Moving from the Vendor ID field opens the Enter Drop-Ship Customer window.

![](media/67bec0dd11b14ca67ac91c0300592630.jpg)

>   In the Enter Drop-Ship Customer window, enter or select the customer ID and
>   ship-to address ID where the vendor is shipping the items. Choose OK to
>   return to the Purchase Order Entry window.

1.  Enter or select the project where an item will be used. If the item that
    you’re purchasing isn’t assigned to a project because the item isn’t
    assigned to a budget, leave the Project No. field blank.

>   You cannot enter a project number that belongs to a contract with a status
>   of On Hold, Closed, or Estimate. In addition, you cannot enter a project
>   number for a project, contract, or customer that doesn’t allow you to enter
>   or post cost transactions.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter or select the cost category. You must enter a cost category ID if the
    item you’re entering is part of a project. If the item isn’t part of a
    project, you can leave the Cost Category ID field blank.

2.  Enter or select the number of the item you’re purchasing. If an item hasn’t
    been set up in your inventory, see *Adding an item to inventory* or *Using
    noninventoried items* for more information.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget. You cannot add a new
>   inventoried item if the Allow Entry of New Budgets/Materials option is not
>   marked in the User Purchase Order Settings window. See *Inventoried items
>   and non-inventoried items for projects* for more information.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter the item quantity.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can modify the default unit cost.

3.  Enter a site ID, or accept the default site.

>   *Sites are required for line items. You must enter a site ID before
>   continuing to the next line.*

1.  Continue to enter all the line items for the purchase order.

2.  Enter a tax schedule ID or accept the default entry. This tax schedule ID
    will be used to calculate tax on the amount of the document. See *Default
    tax schedules for purchase orders* for more information about default tax
    schedule IDs for purchase orders.

3.  Enter the trade discount, freight, miscellaneous, and tax amounts for this
    purchase order. The trade discount is automatically calculated if you’ve
    assigned a trade discount percentage to the vendor that you’re purchasing
    the items from.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Tax calculations in Purchase Order
>   Processing*. You can’t change the Tax amount in the Purchase Order Entry
>   window even if your system is set up to allow editing summary-level taxes in
>   the Company Setup Options window. To change the tax amounts for a line item,
>   see *Calculating and distributing detail taxes for purchase order items*.

1.  Enter a comment ID (optional). For more information about comments, see
    *Adding comments to purchasing documents*.

2.  Choose the Attachment Management icon to attach documents to the purchase
    order, if applicable.

3.  Choose File \>\> Print to open the Purchase Order Print Options window,
    where you can print the purchase order (optional). See *Printing and sending
    an individual purchase order in e-mail* for more information. For
    information about printing several purchase orders at once, see *Printing
    and sending multiple purchase orders in e-mail*.

>   *If you are using purchase order approval workflow, the purchase order must
>   be approved before you can print it. You also can print a purchase order
>   that doesn’t need approval. If you are using vendor approval workflow, the
>   vendors assigned to the purchase orders must be approved or have the
>   workflow status of No Approval Needed.*

>   You can select to print purchase orders in the functional or originating
>   currency using the currency list button.

1.  Save the purchase order or submit the purchase order for approval, if you
    are using Workflow.

Chapter 8: Purchase order detail entry
======================================

>   The Purchase Order Entry window is designed to resemble a physical purchase
>   order document and includes vendor, line item, and total information. Use
>   the expansion buttons in the Purchase Order Entry window to open windows
>   where you can enter detailed information about a document, vendor, line
>   item, or other elements of a purchase order.

>   This information is divided into the following sections:

-   *Entering vendor information*

-   *Updating a vendor’s e-mail information for a purchase order*

-   *Entering line items with multiple release dates*

-   *Entering line item detail information*

-   *Entering project line item detail information*

-   *Specifying the manufacturer’s item numbers to print on a purchase order*

-   *Entering and releasing blanket line items*

-   *Copying purchase order line items*

-   *Previewing purchase order line items*

-   *Adding a vendor item*

-   *Adding an item to inventory*

-   *Using non-inventoried items*

-   *Inventoried items and non-inventoried items for projects*

-   *Adding comments to purchasing documents*

Entering vendor information
---------------------------

>   Use the Purchasing Vendor Detail Entry window to display or enter additional
>   information about a vendor for a purchase order. You can change information
>   such as the name, address, and shipping method. If you select a vendor ID in
>   the Purchase Order Entry window before opening this window, that vendor will
>   be displayed.

>   Any changes you make in the Purchasing Vendor Detail Entry window will be
>   applied to the purchase order you’re working with, but won’t affect the
>   vendor’s permanent record.

>   **To enter vendor information:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order.

2.  Choose the Vendor ID expansion button to open the Purchasing Vendor Detail
    Entry window.

![](media/70742914830db7626a316d4bb3f6f168.jpg)

>   Currency amounts in this window appear in the functional or originating
>   currency, depending on the view selected in the Purchase Order Entry window.

1.  Enter the information or highlight the fields to change, such as vendor
    name, customer ID (if you’re entering a drop-ship purchase order or
    drop-ship blanket purchase order), the address IDs, contract number, payment
    terms, or shipping method. You also can enter the name or initials of the
    person who should approve the order, and a tax registration number if
    applicable.

>   If you change the purchase address ID, ship-to address ID, or shipping
>   method, the line items assigned to the purchase order aren’t updated
>   automatically. You should review address and shipping information for each
>   item.

1.  To make changes to the purchase address information or ship-to address
    information for the document, choose the expansion button next to the
    Purchase Address ID field or the Ship To Address ID field to open the
    Purchasing Ship To Address Entry window.

2.  Choose OK to close the window and continue entering the purchase order.

Updating a vendor’s e-mail information for a purchase order
-----------------------------------------------------------

>   Use the Purchasing E-mail Detail Entry window to update a vendor's e-mail
>   information for a transaction. The changes you enter in this window will
>   affect only the current transaction. To make permanent changes to the vendor
>   record for e-mail settings, make them using the Vendor E-mail Options
>   window.

>   You can change the subject, message ID, and message if the Allow Update of
>   E-mail at Entry option in the Purchasing E-mail Setup window is marked. You
>   can update the reply to address if the Changing ’Reply to' Address option in
>   the Purchasing Email Setup window is marked.

>   **To update vendor’s e-mail information for a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order.

2.  Select a vendor ID.

3.  Choose the E-mail Detail Entry expansion button to open the Purchasing
    E-mail Detail Entry window.

![](media/6c4fbddb48f334c5e21b4fb3855577c4.jpg)

1.  Enter a To, Cc, or Bcc address to send the transaction in e-mail. You must
    enter at least one e-mail address to send transactions in e-mail. The
    default e-mail addresses entered in the Internet Information window are
    displayed for the vendor. You can update the To, Cc, and Bcc e-mail
    addresses, if applicable.

2.  Enter or select a message ID if you want to use a predefined message.

3.  Enter a subject line for the message. If you don't enter a subject for the
    message, the document number of the transaction you are sending is used.

4.  Edit the message that will appear in the e-mail when sending the purchase
    order.

5.  Update the address that a vendor can use to send a reply e-mail. For
    example, assume that you have entered purchasing\@fabrikam.com as the reply
    to address. If you send a document in e-mail to a vendor, the vendor
    receives email from someone\@fabrikam.com. When the vendor replies to the
    e-mail, purchasing\@fabrikam.com is used in the To field.

6.  Choose Save to save your changes.

>   Choose Default to restore the default e-mail settings entered for the vendor
>   in Vendor E-mail Options window.

Entering line items with multiple release dates
-----------------------------------------------

>   Use the Release By Date field in the Purchasing Item Detail Entry window to
>   specify the date you’d like to order an item. You can enter release by dates
>   to create a purchase order with multiple line items that will be released to
>   the vendor at different times.

>   The release by date is calculated if the Calculate Line Item’s Release By
>   Date Based on Vendor Lead Time option in the Purchase Order Processing Setup
>   window is marked. The release by date is calculated by subtracting the
>   number of planning lead time days from the required date entered for the
>   line item. The Release By Date is not recalculated when you modify the
>   Required Date. If the Calculate Line Item’s Release By Date based on Vendor
>   Lead Time option isn’t marked, the release by date isn’t calculated.

>   If you are using Project Accounting, you can’t use the Calculate Line Item’s
>   Release By Date Based on Vendor Lead Time option to calculate the release by
>   date.

>   You can monitor the release by dates of purchase order lines by printing a
>   PO Line Items to Release report.

>   You also can set up a business alert to notify you when a purchase order
>   line’s release by date equals the user date, if you are using business
>   alerts.

>   If a purchase order is generated from Material Requirements Planning (in the
>   Manufacturing Series), the release by date will be calculated and filled
>   based on the required date and the item/vendor’s planning lead time.

>   If you are using Project Accounting, you can’t generate purchase orders for
>   projects from Material Requirements Planning.

Entering line item detail information
-------------------------------------

>   Use the Purchasing Item Detail Entry window to view or enter additional
>   information for a vendor item, item, or non-inventoried item. You can enter
>   more specific information, such as the required and promised shipping dates,
>   and a comment ID. You also can use the Release By Date field to specify the
>   date you’d like to order an item. For more information about release dates,
>   see *Entering line items with multiple release dates*. If you select an item
>   in the Purchase Order Entry window before opening this window, that item
>   will be displayed.

>   If you are using Project Accounting, you can enter blanket purchase order
>   line items. The Project Number field and the Cost Cat. ID field will be
>   displayed in the Purchasing Item Detail Entry window, but you can’t enter
>   project information. To enter additional information for a line item
>   assigned to a project, see *Entering project line item detail information*.

>   **To enter line item detail information:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order number, select a line item, and choose the
    Vendor Item or Item expansion button to open the Purchasing Item Detail
    Entry window.

![](media/d04fe8432977bca3c500d4948e40d305.jpg)

>   Currency amounts in this window appear in the functional or originating
>   currency, depending on the view selected in the Purchase Order Entry window.

1.  Enter the item using either the vendor’s item number or your company’s item
    number. You also can enter a vendor item or an item that hasn’t been set up
    in your inventory.

>   You can display the vendor’s item number by marking Options \>\> Display
>   Vendor Item. If the option is not marked, your company’s item number will be
>   displayed. You can change this at any time.

>   If you are entering line items for a blanket purchase order or a drop-ship
>   blanket purchase order, all line items must have the same item number. The
>   first item entered for a blanket purchase order or a drop-ship blanket
>   purchase order is the control blanket line item and it has the line number
>   of 0.

>   To specify that an item must be a specific manufacturer’s item, choose the

>   Manufacturer’s Item Number expansion button to open the Purchasing
>   Manufacturer’s Item Number Entry window. See *Specifying the manufacturer’s
>   item numbers to print on a purchase order* for more information.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter or modify the quantity ordered. If you are entering the quantity
    ordered for a control blanket line item for a blanket or drop-ship blanket
    purchase order, enter the maximum quantity amount to order.

>   The Link Purchase Order icon will be displayed in the Quantity Ordered field
>   for line items with sales commitments. Choose the Link Purchase Order button
>   next to the Quantity Ordered heading to view, add, or delete commitments in
>   the Sales Commitments for Purchase Order window. The control blanket line
>   item for a blanket purchase order or a drop-ship blanket purchase order
>   can’t be added to a commitment. For more information, see *Committing
>   purchase orders to sales documents*.

1.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can edit the default unit cost.

2.  Enter a site ID, or accept the default.

3.  If the agreement you made with the vendor is based on the total cost of the
    item for a blanket purchase order or a drop-ship blanket purchase order,
    modify the extended cost to match the agreed cost.

4.  Enter or select a default posting account that will be used when receipts
    are posted (optional).

5.  Enter or change in-house dates—required date, release by date—if necessary.

6.  Enter or change vendor dates—current promised date, promised ship date—if
    necessary.

>   Date information is used for reports, such as the Expected Shipments Report
>   and the Purchase Order Analysis Report, and also in the Purchase Order
>   Processing Item Inquiry window.

1.  Enter a landed cost group ID, or accept the default if you’re using landed
    cost. The landed cost IDs that are part of the group will be assigned
    automatically when the shipment is received.

2.  Select an FOB (Free on Board) designation of None, Origin, or Destination,
    or accept the default.

3.  Enter the name of the person who requested the item and a comment ID
    (optional). For more information about comments, see *Adding comments to
    purchasing documents*.

4.  Enter a shipping method and ship-to address or accept the default entries.

>   You can’t modify a ship-to address for an item assigned to a standard
>   purchase order or blanket purchase order that has a Delivery shipping method
>   type.

>   You can’t modify the ship-to address or shipping method if a drop-ship sales
>   order line item is linked to a drop-ship purchase order or drop-ship blanket
>   purchase order.

1.  Select the tax status of the line item that’s displayed. You can define the
    item as taxable or non-taxable, or base the tax on the tax schedule assigned
    to the vendor.

>   This field isn’t available if the Single Schedule tax option is marked in
>   the Purchase Order Processing Setup Options window.

1.  Enter the ID for the tax schedules that will be used to calculate tax on the
    item that’s displayed.

2.  Enter the tax amount. Taxes will be calculated automatically as you enter
    items. Taxes aren’t calculated for the control blanket line item of a
    blanket purchase order or a drop-ship blanket purchase order. For more
    information about tax calculations, see *Tax calculations in Purchase Order
    Processing*. If you want to change the tax distribution that’s calculated
    automatically for the item, see *Calculating and distributing detail taxes
    for purchase order items*.

3.  Choose Save to save the item.

4.  Close the window when you are finished entering item information.

Entering project line item detail information
---------------------------------------------

>   If you are using Project Accounting, you can use the Purchasing Item Detail
>   Entry window to view or enter additional information for an inventoried item
>   or noninventoried item. See *Inventoried items and non-inventoried items for
>   projects* for more information.

>   You can enter more specific information, such as the required and promised
>   shipping dates, and a comment ID. You also can use the Release By Date field
>   to specify the date you’d like to order an item. For more information about
>   release dates, see *Entering line items with multiple release dates*.

>   **To enter project line item detail information:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order number, select a line item, and choose the
    Item expansion button to open the Purchasing Item Detail Entry window.

![](media/07217133fd78b65fee9d270ed7cd673c.jpg)

>   Currency amounts in this window appear in the functional or originating
>   currency, depending on the view selected in the Purchase Order Entry window.

1.  Enter or select the project where an item will be used. If the item that
    you’re purchasing isn’t assigned to a project, leave the Project No. field
    blank.

>   You cannot enter a project number that belongs to a contract with a status
>   of On Hold, Closed, or Estimate. In addition, you cannot enter a project
>   number for a project, contract, or customer that doesn’t allow you to enter
>   or post cost transactions.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter or select the cost category where an item will be used. You must enter
    a cost category ID if the item that you’re entering is part of a project. If
    the item isn’t part of a project, leave the Cost Cat. ID field blank.

>   To view additional project information, choose the Cost Cat. ID expansion
>   button to open the PA Purchasing Item Detail Entry window.

1.  Enter or select the number of the item you’re purchasing. If an item hasn’t
    been set up in your inventory, see *Adding an item to inventory* or *Using
    noninventoried items* for more information.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget. You cannot add a new
>   inventoried item if the Allow Entry of New Budgets/Materials option is not
>   marked in the User Purchase Order Settings window. See *Inventoried items
>   and non-inventoried items for projects* for more information.

>   You can choose the Cost Cat. ID expansion button to open the PA Purchasing
>   Item Detail Entry window, where you can enter a billing note.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter or modify the quantity ordered.

2.  If you’ve entered a non-inventoried item, enter the unit cost. If you’ve
    entered an inventoried item, you can edit the default unit cost.

3.  Enter a site ID, or accept the default.

4.  Enter or select a default posting account that will be used when receipts
    are posted (optional).

5.  Enter or change in-house dates—required date, release by date—if necessary.

6.  Enter or change vendor dates—current promised date, promised ship date—if
    necessary.

>   Date information is used for reports, such as the Expected Shipments Report
>   and the Purchase Order Analysis Report, and also in the Purchase Order
>   Processing Item Inquiry window.

1.  Enter a landed cost group ID, or accept the default if you’re using landed
    cost. The landed cost IDs that are part of the group will be assigned
    automatically when the shipment is received.

2.  Select an FOB (Free on Board) designation of None, Origin, or Destination,
    or accept the default.

3.  Enter the name of the person who requested the item and a comment ID
    (optional). For more information about comments, see *Adding comments to
    purchasing documents*.

4.  Enter a shipping method and ship-to address or accept the default entries.

>   You can’t modify a ship-to address for an item assigned to a standard
>   purchase order that has a Delivery shipping method type.

1.  Select the tax status of the line item that’s displayed. You can define the
    item as taxable or non-taxable, or base the tax on the tax schedule assigned
    to the vendor.

>   This field isn’t available if the Single Schedule tax option is marked in
>   the Purchase Order Processing Setup Options window.

1.  Enter the ID for the tax schedules that will be used to calculate tax on the
    item that’s displayed.

2.  Enter the tax amount. Taxes will be calculated automatically as you enter
    items. Taxes aren’t calculated for the control blanket line item of a
    blanket purchase order or a drop-ship blanket purchase order. For more
    information about tax calculations, see *Tax calculations in Purchase Order
    Processing*. If you want to change the tax distribution that’s calculated
    automatically for the item, see *Calculating and distributing detail taxes
    for purchase order items*.

3.  Choose Save to save the item.

4.  Close the window when you are finished entering item information.

Specifying the manufacturer’s item numbers to print on a purchase order
-----------------------------------------------------------------------

>   Use the Purchasing Manufacturer’s Item Number Entry window to specify that a
>   sales inventory item or a discontinued item must be a specific
>   manufacturer’s item and to have the manufacturer’s item number printed on
>   the purchase order. You can include up to five manufacturer item numbers to
>   be printed on the purchase order for an item. You also can modify
>   manufacturer item number information.

>   If you entered manufacturer item number information for an item using the
>   Manufacturer’s Item Number Maintenance window, that information will appear
>   as default values in the Purchasing Manufacturer’s Item Number Entry window.

>   You also can open the Purchasing Manufacturer’s Item Number Entry window
>   from the Purchasing Item Detail Entry window.

>   *If you are using Project Accounting, you can’t use manufacturers’ item
>   numbers for purchase order line items that have project information.*

>   **To specify the manufacturer’s item numbers to print on a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order number, select a line item, and choose the
    Manufacturer’s Item Number expansion button to open the Purchasing
    Manufacturer’s Item Number Entry window.

![](media/e0174db2e0066f034c65b5af4da41bf9.jpg)

1.  Enter or modify the name of the manufacturer, manufacturer’s item number,
    and description of the item.

2.  Mark Include to have the manufacturer’s item number printed on the purchase
    order.

3.  Choose OK to save your changes.

Entering and releasing blanket line items
-----------------------------------------

>   Use the Purchasing Blanket Detail Entry window to enter all of the blanket
>   line items at once, or to enter additional blanket lines later when you know
>   more about the quantities, required date, and costs of the item. You also
>   can select which blanket line items should be released when the purchase
>   order is printed.

>   You must enter the control blanket line item for a blanket purchase order or
>   a dropship blanket purchase order in the Purchase Order Entry window before
>   you can enter or modify blanket line items in the Purchasing Blanket Detail
>   Entry window.

>   If you are using Project Accounting, you can’t enter blanket purchase orders
>   or drop-ship blanket purchase orders for projects.

>   **To enter and release blanket line items:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a blanket purchase order or a drop-ship blanket purchase
    order.

2.  For a new blanket purchase order or a drop-ship purchase order, enter the
    control blanket line item.

>   If the agreement you made with the vendor is based on the total cost of the
>   item, modify the extended cost to match the agreed cost.

1.  Choose Blanket to open the Purchasing Blanket Detail Entry window.

![](media/e37bba7dbc99959b8512a2650305090b.jpg)

>   Currency amounts in this window appear in the functional or originating
>   currency, depending on the view selected in the Purchase Order Entry window.

1.  Enter the information or highlight the fields to change.

    -   You can change the Control Blanket By option until one of the blanket
        line items has a status other than New or Canceled. If you change the
        Control Blanket By option to Value, be sure that the extended cost
        amount for the control blanket line item in the Purchase Order Entry
        window is correct. You also must enter quantities for the blanket
        purchase order’s delivery schedule if you are managing the blanket by
        value.

    -   You can enter additional blanket line items for the purchase order and
        modify the quantities, required dates, and costs for the existing
        blanket line items.

    -   You can select which line items will be released to the vendor when the
        purchase order is printed.

2.  When you’ve finished entering blanket line items, choose OK to return to the
    Purchase Order Entry window.

Copying purchase order line items
---------------------------------

>   Use the Copy a Purchase Order window to copy line items from one purchase
>   order to another. Copied line items are assigned line numbers based on the
>   number of existing line items in the new purchase order. If you are using
>   Project Accounting, you won’t be able to copy line items that have project
>   information assigned to them. You cannot copy line items to or from an
>   existing blanket purchase order.

>   If the new and existing orders have different currencies and neither is the
>   functional currency, amounts will be converted from the currency of the
>   existing order to the functional currency and then to the currency for the
>   new order.

>   If you are using Workflow and you’ve copied line items to a purchase order
>   that isn’t pending changes or pending approval, you have to resubmit the
>   purchase order.

>   **To copy purchase order line items:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a standard or drop-ship purchase order to add line items to.
    To create a new purchase order, select a type, then enter a new purchase
    order number and vendor ID.

2.  Choose Actions and select Copy PO Lines to Current PO to open the Copy a
    Purchase Order window.

![](media/c9766521cb68d0e3abdaa8997398661c.jpg)

*You also can press ALT + P to copy purchase order line items.*

1.  Enter or select an existing purchase order to copy from.

2.  Select a site option. If you select Use Site, enter or select a site.

3.  Select a cost option.

4.  Mark the desired copy options.

>   You can choose Preview to open the Preview Line Items window, where you can
>   mark and modify line items before you copy them. See *Previewing purchase
>   order line items* for more information.

1.  Choose Copy.

Previewing purchase order line items
------------------------------------

>   Use the Preview Line Items window to mark and modify purchase order line
>   items before you copy them. You also can view warnings and correct error
>   messages. You can’t mark a line item that contains an error (red symbol)
>   until you correct the error. You can mark a line item that contains a
>   warning (yellow symbol).

>   If the line items are assigned to project, the line items will be copied
>   except for the project numbers and cost categories assigned to them. These
>   fields will be blank.

>   **To preview purchase order line items:**

1.  Open the Copy a Purchase Order window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry \>\>Actions \>\>
>   Create And Copy New PO)

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry \>\> select a
>   standard or drop-ship purchase order \>\> Actions \>\> Copy PO Lines to
>   Current PO)

1.  Enter an order number.

2.  Mark the desired copy options.

3.  Choose Preview.

![](media/50198a1c36a597f10a0139949f2ceb8e.jpg)

1.  If you selected the Mark All Line Items for Copy option, all line items will
    be marked. You can unmark any line item that shouldn’t be copied.

2.  If a line item contains an error, select the line item and click the
    expansion button to view the error. Then you can correct the error and mark
    the line item.

3.  You can change the order quantity of any line item. You can change the unit
    cost of any purchase order line item.

4.  Choose OK to save your changes and close the Preview Line Items window.

Adding a vendor item
--------------------

>   You can add vendor items as you enter purchase orders, shipment receipts,
>   shipment/invoice receipts, and invoice receipts. If you mark Options \>\>
>   Add Item, you’ll get a message each time you enter a vendor item number that
>   doesn’t exist in your records. (To enter vendor items, Options \>\> Display
>   Vendor Item also must be marked.) You’ll have the option to add the vendor
>   item to inventory, or enter a noninventoried item.

>   **To add a vendor item:**

1.  Be sure Add Item and Display Vendor Item are marked in the Options menu.

>   (Choose Options \>\> Add Item and Options \>\> Display Vendor Item.)

1.  When entering line items for a purchase order, enter a new vendor item
    number. You’ll get a message asking whether you want to assign an item
    number to the vendor item.

2.  Choose Yes; the Item Vendors Maintenance window will open. The vendor ID and
    vendor item will be default entries in this window.

3.  Enter or select an item. If you select an item, the item description appears
    as the description for the vendor item.

>   If you enter a new item, you’ll get a message asking whether you want to add
>   the item. Choose to add the item; the Item Maintenance window will open and
>   you can enter item information. Be sure that you assign a price list and a
>   site.

1.  Enter the default purchasing U of M.

2.  Choose Save and close the Item Maintenance window. Continue entering the
    purchase order.

Adding an item to inventory
---------------------------

>   You can add inventoried items as you enter transactions. If you mark Options
>   \>\> Add Item, you’ll get a message each time you enter an item number that
>   doesn’t exist in your records. You’ll have the option to add the item to
>   inventory, or enter a non-inventoried item. To add inventoried items,
>   Options \>\> Display Vendor Item must be unmarked.

>   **To add an item to inventory:**

1.  Be sure that Add Item is marked and Display Vendor Item is not marked in the
    Options menu. (Choose Options \>\> Add Item and Options \>\>Display Vendor
    Item.)

2.  When entering line items for a purchase order, enter an item that hasn’t
    been set up in your inventory. You’ll get a message asking whether you want
    to add the item.

3.  Choose Yes; the Item Maintenance window will open. Use this window to enter
    item information.

>   When entering information for a new item, be sure that you assign a price
>   list, vendor item and a site, using the appropriate buttons in the Item
>   Maintenance window. Choose Save and close the Item Maintenance window.

>   *If you are using Project Accounting, you must assign a new inventoried item
>   to be used for a project to a cost category in the Budget Detail IV Items
>   window.*

1.  If you add the item and do not assign a vendor item, another message appears
    asking if you want to assign a vendor item to the item. Choose Yes; the Item
    Vendors Maintenance window will open.

>   The item and vendor ID entered for the purchase order are displayed in the

>   Item Vendors Maintenance window. The item description entered in the Item
>   Maintenance window is a default entry for the vendor item description. You
>   can either accept the item description as the vendor item description or
>   enter a new vendor item description.

1.  Choose Save and close the Item Vendors Maintenance window. Continue entering
    the purchase order.

Using non-inventoried items
---------------------------

>   If you mark Options \>\> Add Item, each time you enter a new vendor item or
>   item you’ll have the option of adding the item or vendor item to your
>   inventory records. If you choose not to add the item to inventory, it will
>   be recorded as a noninventoried item.

>   If you don’t mark Options \>\> Add Item, no message appears when you enter a
>   new item, and all new items you enter will be recorded as non-inventoried
>   items.

>   **To use non-inventoried items:**

1.  When entering line items for a purchase order, enter a vendor item or item
    that hasn’t been set up in your inventory.

2.  If Options \>\> Add Item is marked, a message appears. Choose not to assign
    an item to the vendor item or add the item to your inventory.

>   If Options \>\> Add Item isn’t marked, all new items you enter will be
>   recorded as non-inventoried items.

1.  Enter the unit cost of the non-inventoried item, the item description, and
    the site ID.

>   Transaction information for non-inventoried items is maintained in Purchase
>   Order Processing history, but doesn’t affect Inventory records.

>   When you enter a non-inventoried item, the default vendor item number and
>   vendor description are the same as the item number and description. You can
>   change this information.

Inventoried items and non-inventoried items for projects
--------------------------------------------------------

>   If you are entering a purchase order or a receipt that is part of a project,
>   you can use the inventoried items that have been assigned to cost categories
>   in the Budget Detail IV Items window. In the Budget Detail IV Items window,
>   you can specify the inventory items that comprise a single cost category.
>   You also use the Budget Detail IV Items window to view or modify inventory
>   item budgets.

>   If you are entering a purchase order or a receipt that you’re entering is
>   not part of a project, you can use an inventoried item that has been entered
>   in the Item Maintenance window.

>   You also can enter non-inventoried items for project or non-project purchase
>   orders and receipts. These items aren’t tracked in your inventory.

>   The following table shows the situations where you can use inventoried and
>   noninventoried items for projects and cost categories.

| **Project** | **Cost category** | **Item to use**                                                                        |
|-------------|-------------------|----------------------------------------------------------------------------------------|
| Yes         | Yes               | An inventoried item assigned to the cost category in the Budget Detail IV Items window |
| No          | Yes               | Non-inventoried                                                                        |
| No          | No                | Non-inventoried                                                                        |
| **Project** | **Cost category** | **Item to use**                                                                        |
| Yes         | Yes               | Non-inventoried                                                                        |
| No          | No                | An inventoried item entered in the Item Maintenance window                             |

Adding comments to purchasing documents
---------------------------------------

>   You can add comments to purchase orders or to individual line items on a
>   purchase order or receipt. Comments can be predefined on a company-wide
>   basis, and used on Sales Order Processing, Invoicing or Purchase Order
>   Processing documents. You can enter the ID of a predefined comment in the
>   Purchase Order Entry or Purchasing Item Detail Entry windows.

>   *You can enter up to 200 characters, which will appear on the purchase order
>   or receipt as four lines of 50 characters each. If you want longer comments
>   to appear, use Report Writer to modify the document layout.*

>   You can create new comments while you are entering transactions. You also
>   can create custom comments for a particular document or line item, or modify
>   existing comments. One-time comments or modified comments won’t be available
>   for other documents or line items. To modify a comment for new documents and
>   line items, choose Administration \>\> Setup \>\> Company \>\> Comments to
>   open the Comment Setup window and make your changes. If the modified comment
>   should appear on existing documents or line items, you must reassign the
>   comment ID.

>   **To create a new comment:**

1.  In the Purchase Order Entry window, the Purchasing Item Detail Entry window
    or the Recevings Item Detail Entry window, enter a new value in the Comment
    ID field, then press TAB.

2.  A message will ask if you want to add this comment ID. Choose Add to display
    the Comment Setup window.

3.  Select a series this comment will be associated with.

4.  Enter the comment text.

5.  Choose Save, then close the Comment Setup window.

>   **To create a one-time comment:**

1.  In the Purchase Order Entry window, the Purchasing Item Detail Entry window
    or the Receivings Item Detail Entry window, choose the Comment ID expansion
    button to open the Purchasing Comment Entry window.

![](media/b7d7111701da64daab1d5459b9c95ca5.jpg)

>   If the Comment ID field contained a value, you’ll be able to modify the
>   existing comment. If the Comment ID field was blank, you’ll be able to
>   create a new, one-time comment.

1.  Enter the comment text.

2.  Choose OK.

98 P U R C H A S E O R D E R P R O C E S S I N G

Chapter 9: Purchase order generator
===================================

>   If you are using the purchase order generator, you can automatically
>   generate purchase orders to replenish inventory based on a reorder point you
>   specify. If you are using Project Accounting, you can’t generate purchase
>   orders for projects.

>   Use the purchase order generator to analyze inventory levels and suggest
>   purchase order line items based on default settings and reorder levels. You
>   can modify the suggested purchase order line items before generating them
>   into purchase orders in Purchase Order Processing.

>   This information is divided into the following sections:

-   *Purchase order generator overview*

-   *How the replenishment level is used for suggested purchase orders*

-   *How the vendor is selected for suggested purchase orders*

-   *How the cost is selected for suggested purchase orders*

-   *How quantities are calculated for suggested purchase orders*

-   *Generating suggested purchase orders*

-   *Suggested purchase order errors and warnings*

-   *Generating purchase orders in Purchase Order Processing*

-   *Modifying suggested purchase order detail*

-   *Viewing sources of demand*

Purchase order generator overview
---------------------------------

>   If you’re using the purchase order generator, you need to choose an order
>   policy of Use PO Gen in the Item Resource Planning Maintenance window so
>   suggested purchase orders will be created. To generate suggested purchase
>   orders, you must define default reorder information in the Purchase Order
>   Processing Setup Options window. You can modify the item options for each
>   item at a specific site using the Purchase Order Generator Item Maintenance
>   window or modify item options for a group of items using the Purchase Order
>   Item Mass Update window. These options are as follows:

>   **Order method** This option indicates whether you are ordering to an Order
>   to Independent Site—so that suggested purchase orders can be generated for
>   each item-site combination—or to an Order to Master Site—so that suggested
>   purchase order quantities from subordinate sites will be added to the
>   requirements of the master site. The master site will receive and then
>   disperse the purchased items to the sites that required them.

>   **Replenishment level** This allows you to specify which inventory level to
>   order to. For more information about replenishment level, see *How the
>   replenishment level is used for suggested purchase orders*.

>   **Vendor selection** An option that specifies how you want to select which
>   vendor will be used for suggested purchase orders. For more information
>   about vendor selection, see *How the vendor is selected for suggested
>   purchase orders*.

>   **Cost selection** An option that specifies where the default cost for the
>   suggested purchase order should come from. For more information about cost
>   selection, see *How the cost is selected for suggested purchase orders*.

How the replenishment level is used for suggested purchase orders
-----------------------------------------------------------------

>   The specified replenishment level for the item controls the calculations of
>   the order quantity. Refer to *How quantities are calculated for suggested
>   purchase orders* for information about how replenishment levels affect
>   required quantity.

>   If you selected Order Point Quantity as the replenishment level, the
>   available inventory will be brought up to the order point defined in the
>   Item Resource Planning Maintenance window.

>   If you selected Order-Up-To Level as the replenishment level, the available
>   inventory will be brought up to the order-up-to level defined in the Item
>   Resource Planning Maintenance window. The Order Point Quantity will be used
>   if the OrderUp-To Level is zero or less than the Order Point Quantity.

>   If you selected Vendor EOQ as the replenishment level, the vendor economic
>   quantity is used when it is greater than the required quantity. Otherwise,
>   the required quantity is used. You won’t be able to select this option if
>   the order method is Order To Master Site.

How the vendor is selected for suggested purchase orders
--------------------------------------------------------

>   The vendor selection you selected in the Purchase Order Generator Item
>   Maintenance window allows you to indicate which vendor will be used for
>   suggested purchase order line items. The vendor selection is dependent on
>   the order method you selected. If the order method is Order To Master Site,
>   the master site’s vendor selection will be used to determine the vendor. If
>   the order method is Order To Independent Site, the default vendor can be
>   selected from one of the following options: Site Primary Vendor, Vendor with
>   Lowest Cost, or Vendor with Shortest Lead Time.

>   If you selected Site Primary Vendor as the vendor selection, the primary
>   vendor specified in the Item Quantities Maintenance window for the item-site
>   combination is used.

>   If you selected Vendor with Lowest Cost as the vendor selection, the vendor
>   with the lowest cost will be selected based on the functional equivalent of
>   the Last Originating Invoice Cost field in the Item Vendors Maintenance
>   window. If the last originating invoice cost couldn’t be converted to its
>   functional equivalent, the vendor won’t be selected. If a vendor’s cost is
>   zero, that vendor won’t be selected.

>   If you selected Vendor with Shortest Lead Time as the vendor selection, the
>   vendor with the shortest planning lead time will be selected based on the
>   Planning Lead Time field in the Item Vendors Maintenance window. If a
>   vendor’s lead time is zero, that vendor won’t be selected.

How the cost is selected for suggested purchase orders
------------------------------------------------------

>   The cost selection you selected in the Purchase Order Generator Item
>   Maintenance window allows you to indicate where the default cost for the
>   suggested purchase order should come from. The cost selection is dependent
>   on the order method you selected. If the order method is Order To Master
>   Site, the master site’s cost selection will be used to determine the cost.
>   If the order method is Order To Independent Site, the default cost can be
>   selected from one of the following options: Vendor Last Originating Invoice
>   Cost, Item Current Cost, Item Standard Cost, or Specified Cost (In
>   Functional Currency).

>   If you selected Vendor Last Originating Invoice Cost as the cost selection,
>   the last originating invoice cost from the Item Vendors Maintenance window
>   for the selected vendor will be used.

>   If you selected Item Current Cost as the cost selection, the current cost
>   from the Item Maintenance window will be used.

>   If you selected Item Standard Cost as the cost selection, the standard cost
>   from the Item Maintenance window will be used.

>   If you selected Specified Cost (In Functional Currency) as the cost
>   selection, the cost specified in the Purchase Order Generator Item
>   Maintenance window will be used regardless of the vendor.

How quantities are calculated for suggested purchase orders
-----------------------------------------------------------

>   The suggested quantity for an item on a purchase order is based on the
>   quantity available for the item at a site and on which demands are to be
>   included in the calculation indicated by how you set up items using the
>   Purchase Order Generator Item Maintenance window. In addition, if you are
>   using Use PO Gen as the order policy of an item, the suggested quantity can
>   be calculated as a multiple of the number entered as the order multiple in
>   the Item Vendors Maintenance window. For example, assume that you need 50
>   widgets and the order multiple for widgets is 8. The suggested order
>   quantity for the purchase order would be 56.

>   **Available quantity**

>   The available quantity is the amount of the item that is on hand now—or that
>   is already on order less the demand for the item at that site. The quantity
>   is calculated using the following formula.

>   (Quantity On Hand + Quantity On Order + Quantity On Order from purchase
>   order lines with New status) - (Quantity Allocated + Quantity Requisitioned
>   + Quantity Back Ordered + Quantity required by subordinate sites)

>   The quantity allocated, quantity requisitioned, and quantity back ordered
>   will be included in the available quantity calculation only if you mark
>   those options in the Purchase Order Generator Item Maintenance window. If
>   you are using eRequisition, the quantity requisitioned doesn’t include
>   requisitions from eRequisition.

>   Refer to the table for information about when the quantities are included in
>   the calculation.

| **Quantity:**                                                                    | **Is included:**                                                                   |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Quantity On Hand from Item Quantity Maintenance window                           | Always                                                                             |
| Quantity On Order from Item Quantity Maintenance window                          | Always                                                                             |
| Quantity On Order from “New” purchase order lines, less any cancelled quantities | Always                                                                             |
| Quantity Allocated from Item Quantity Maintenance window                         | If Allocated is marked in the Purchase Order Generator Item Maintenance window     |
| Quantity Requisitioned from the Item Quantity Maintenance window                 | If Requisitioned is marked in the Purchase Order Generator Item Maintenance window |
| Quantity Back Ordered from the Item Quantity Maintenance window                  | If Back Orders is marked in the Purchase Order Generator Item Maintenance window   |
| Required quantities for subordinate sites                                        | If the site is a master site                                                       |

>   **Required quantity**

>   If you’re using master sites with the purchase order generator, quantities
>   for subordinate sites are reflected in quantities for the master site.

>   Basically, the required quantity of an item for each subordinate site is the
>   difference between what’s needed and what’s available. Calculating the
>   required quantity depends on the replenishment level selected for the
>   item-site combination.

>   Refer to the table for information about how required quantities are
>   calculated for each type of replenishment level.

| **Replenishment level** | **Availability**                                   | **Required quantity calculation**              |
|-------------------------|----------------------------------------------------|------------------------------------------------|
| Order Point Quantity    | Available for either order                         | Order Point Quantity (from Item Resource       |
| Order-Up-To Level       |                                                    | Order-Up-To Level (from Item Resource          |
| Vendor EOQ              | Only available for Order To Independent Site order | First, calculate the requirement for the item: |

>   method

>   Planning Maintenance window) - Available

>   Quantity = Required Quantity

>   Planning Maintenance window) - Available

>   Quantity = Required Quantity, *unless* the OrderUp-To Level is zero or less
>   than the Order Point Quantity. If that’s the case, then the calculation is
>   Order Point Quantity (from Item Resource

>   Planning Maintenance window) - Available

>   Quantity = Required Quantity

>   method

>   Order Point Quantity (from Item Resource

>   Planning Maintenance window) - Available Quantity = Required Quantity. Then
>   compare that quantity to the economic order quantity (EOQ) for the vendor.
>   The suggested order quantity will be the greater of the two values.

Generating suggested purchase orders
------------------------------------

>   Use the Generate Suggested Purchase Orders window to generate suggested
>   purchase order line items to replenish inventory levels. If you are using
>   Project Accounting, you can’t generate purchase orders for projects.

>   **To generate suggested purchase orders:**

1.  Open the Generate Suggested Purchase Orders window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Generator)

![](media/f9c8bd465ad26919ae1f1645d08556b3.jpg)

1.  Select all item numbers or enter a range of item numbers for which you want
    to generate suggested purchase order line items.

2.  Select all sites or enter a range of sites for which you want to generate
    suggested purchase orders.

3.  Select all buyers or enter a range of buyers for which you want to generate
    suggested purchase orders. Suggested purchase orders will be generated for
    item/site combinations that are associated with the buyer IDs in the range.
    If you want to specify the buyer ID that should be on the suggested purchase
    order, use the Buyer ID Selection field.

4.  Select all vendors or enter a range of vendors for which you want to
    generate suggested purchase orders.

5.  Select all item classes or enter a range of item classes for which you want
    to generate suggested purchase orders.

6.  Unmark the Include Orders with No Vendor ID if you don’t want to generate
    suggested orders for which a vendor couldn’t be identified.

7.  Unmark the Include Demand from Subordinate Sites if you don’t want to
    include demand at subordinate sites when determing order quantity. Keep this
    option marked if you are using master sites and you want to include demand
    from subordinate sites.

8.  Select whether or not you want to assign a buyer ID to suggested purchase
    orders. If you select to specify a buyer ID, enter a buyer ID.

9.  Enter the purchase order date to appear on purchase orders.

10. Select whether you want the promised date set to the purchase order date,
    the purchase order date plus the vendor planning lead time, or a specified
    date.

>   If you choose to use a specified date, enter a date.

1.  Specify the number of shipping days.

>   The number of shipping days helps determine the promised ship date. For
>   example, if the vendor promise date is 10/08/07 and you specify 3 as the
>   number of shipping days, the promised ship date will be set to 10/05/07.

1.  Choose Suggest Purchase Orders. When processing is complete, the Suggested
    Purchase Orders Preview window will be displayed. For more information about
    on using window to complete the process of creating purchase orders, see
    *Generating purchase orders in Purchase Order Processing*.

Suggested purchase order errors and warnings
--------------------------------------------

>   If a problem is detected on a suggested purchase order line item, an error
>   or warning icon will appear next to the item in the Suggested Purchase
>   Orders Preview scrolling window and in the Suggested Purchase Order Detail
>   window. These icons are listed in the following table.

| **Icon**                                   | **Description**                                                                                                                                                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [./media/image28.jpg](./media/image28.jpg) | Error—A suggested purchase order that contains an error won’t be created. You must correct the error before generating the purchase order for that item-site. Examples of errors include an inactive vendor or no purchasing unit of measure. |
| [./media/image29.jpg](./media/image29.jpg) | Warning— You can create a purchase order even if it contains a warning. Examples of warnings include a vendor is on hold or the unit cost is zero.                                                                                            |

>   Information about the error or warning will appear at the bottom of the
>   Suggested Purchase Order Detail window.

Generating purchase orders in Purchase Order Processing
-------------------------------------------------------

>   Use the Suggested Purchase Orders Preview window to modify or view suggested
>   purchase order line items and then generate them into purchase orders.
>   Before generating purchase orders, you can print the Suggested Purchase
>   Orders Report by choosing File \>\> Print.

>   An icon will appear next to the item in the Suggested Purchase Orders
>   Preview scrolling window if an error or warning is detected. See *Suggested
>   purchase order errors and warnings* for more information.

>   If you are using Project Accounting, you can’t generate purchase orders for
>   projects.

>   **To generate purchase orders in Purchase Order Processing:**

1.  Open the Suggested Purchase Orders Preview window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Generator \>\> Suggest
>   Purchase Orders)

![](media/fc8739d69ae02c854190fe3ab8a69b04.jpg)

1.  In the Display field, select how you want to view the suggested purchase
    orders.

>   *If a long list of purchase order line items is displayed, you can type in
>   the find field, then press TAB to go to the first occurrence of that item.
>   The label of the find field is associated with the view menu and how you
>   select to sort the purchase order line items in the scrolling window.*

1.  Mark the Include option next to lines you want to create, after you have
    resolved any errors. If you don’t want to generate a purchase order line for
    a particular item, unmark the Include option. If a line doesn’t have any
    errors, the Include option will be marked.

>   Choose Unmark All to unmark all lines. The Mark All option will mark only
>   lines with no errors.

1.  Make any necessary changes.

    -   If you change the vendor ID, the quantities, promised dates, FOB, U of
        M, and the unit cost may be recalculated.

    -   If you change the U of M, the quantity ordered will remain the same, but
        the unit cost will be recalculated.

2.  To get more information about an item, select the row and choose the Item
    expansion button to open the Suggested Purchase Order Detail window. When
    you’re finished viewing information and resolving errors, choose Save or
    Cancel to return to the Suggested Purchase Orders Preview window. For more
    information, see *Modifying suggested purchase order detail*.

>   *If you selected to view a suggested purchase order line item in the
>   Suggested Purchase Order Detail window and returned to the Suggested
>   Purchase Orders Preview window, the purchase order line that you viewed
>   information for will be the first item in the scrolling window.*

1.  Choose Generate Purchase Orders to create the purchase orders in Purchase
    Order Processing. When processing is complete, a report will be generated
    listing the purchase orders that were created. Errors will be listed in an
    error log that prints after the Purchase Order Generated report.

>   Unmarked items and items with errors will remain in the scrolling window.

1.  The purchase orders that were created have a status of New; use the Print

>   Purchasing Documents window (Purchasing \>\> Transactions \>\> Print
>   Purchasing Documents) to print and release the orders. See *Printing and
>   sending multiple purchase orders in e-mail* for information about printing
>   purchase orders.

Modifying suggested purchase order detail
-----------------------------------------

>   The Suggested Purchase Order Detail window provides additional information
>   about a suggested order. You can use this window to view and resolve errors
>   or warnings on suggested orders. See *Suggested purchase order errors and
>   warnings* for more information.

>   **To modify suggested purchase order detail:**

1.  Open the Suggested Purchase Order Detail window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Generator \>\> Suggest
>   Purchase Orders \>\> select an item and choose the Item Number expansion
>   button)

![](media/2e09d0a4e997b35357162e0f38db6fed.jpg)

1.  In the Suggested Purchase Order Detail window, make any necessary changes.

    -   If you change the vendor ID, the quantities, promised dates, FOB,
        purchasing unit of measure, and the unit cost may be recalculated.

    -   If you change the purchasing unit of measure, the quantity ordered will
        remain the same, but the unit cost will be recalculated.

    -   If you don’t want to generate a purchase order line for an item, unmark
        the Include option.

    -   If you want to include a suggested purchase order line item that has
        errors, you must fix those errors before you can include the item.

2.  Choose Save. If errors or warnings exist, the window will not close. Use the
    close box if you want to close the window without resolving all errors.

Viewing sources of demand
-------------------------

>   Use the Subordinate Required Quantity Detail window or the Required Quantity
>   Detail window to view sources of demand for an item.

>   The Subordinate Required Quantity Detail window shows the sources of demand
>   from subordinate sites if ordering by master site. In the Suggested Purchase
>   Order Detail window, you can choose the Required Qty in Base U of M
>   expansion button to open the Subordinate Required Quantity Detail window.
>   The Subordinate Required Quantity Detail window will open if a master site
>   is used for the item-site combination.

![](media/119eeac6d55afc964983d55d1f15c508.jpg)

>   The Required Quantity Detail window shows the details of the required
>   quantity calculation for a site. The quantities that are displayed in this
>   window were saved at the time the suggested purchase order line item was
>   generated. In the Suggested Purchase Order Detail window, you can choose the
>   Required Qty in Base U of M expansion button to open the Required Quantity
>   Detail window if a master site isn’t used for the item-site combination.
>   This window also can be opened by choosing the Required Quantity field
>   expansion button for the subordinate site ID in the Subordinate Required
>   Quantity Detail window.

![](media/0349249fe5a5d38ae4aae6f80b502d4f.jpg)

Chapter 10: Taxes for purchase orders
=====================================

>   Purchases tax can be calculated, modified, and distributed for purchase
>   orders. Use the Purchase Order Tax Summary Entry window to view tax
>   distributions and to change tax distributions, if your system is set up to
>   allow editing summary-level taxes. To change tax details or the amounts
>   distributed to tax details for individual line items, use the Purchase Order
>   Line Item Tax Detail Entry window.

>   This information is divided into the following sections:

-   *Tax calculations in Purchase Order Processing*

-   *Default tax schedules for purchase orders*

-   *Tax schedules for purchase order items*

-   *Calculating and distributing summary taxes for purchase orders*

-   *Calculating and distributing detail taxes for purchase order items*

Tax calculations in Purchase Order Processing
---------------------------------------------

>   You can use advanced tax calculations or a single tax schedule for all
>   documents in Purchase Order Processing. If you want to use a single tax
>   schedule for all documents, select Single Schedule and enter the tax
>   schedule you want to use in the Purchase Order Processing Setup window. All
>   items will be taxed using all the details on the schedule that you assign;
>   however, taxes won’t be calculated for freight and miscellaneous charges.

>   *If you decided not to use the shipping method to determine the default tax
>   schedule and decided to use advanced tax calculations method, the tax
>   schedule assigned to the vendor’s purchase address will be the default tax
>   schedule.*

>   When Advanced is selected in the Purchase Order Processing Setup window, you
>   can specify a default tax schedule for non-inventoried items, freight, and
>   miscellaneous charges that will appear on the document. You can select tax
>   options for non-inventoried items, freight, and miscellaneous charges. You
>   can make the item taxable, nontaxable, or base taxes on vendor.

>   When using advanced tax calculations, the tax details included in the tax
>   schedules that are assigned to the vendor, item, site, freight, and
>   miscellaneous charges are compared, depending on the shipping method
>   selected on the document. Tax is calculated only for the details that match
>   between the tax schedules that are being used.

>   Calculations for taxes on freight are based on comparisons between the tax
>   schedule for the document and the freight tax schedule. Calculations for
>   taxes on miscellaneous charges are based on comparisons between the tax
>   schedule for the document and the miscellaneous tax schedule.

>   *Keep in mind that each time the shipping method, payment terms, site ID, or
>   purchase address for the document is changed, the tax schedule may be
>   changed and taxes may be recalculated.*

Default tax schedules for purchase orders
-----------------------------------------

>   The shipping method for a purchase order is used to determine where the
>   exchange of goods takes place. The shipping method will determine which tax
>   schedule appears as a default schedule for the purchase order and the
>   default schedule to

**P A R T 2** P U R C H A S E O R D E R S

compare against the item. Refer to the following table for the default tax
schedule for a purchase order.

| **Tax calculation option** | **Purchase order type** | **Shipping method** | **Default tax schedule**                                                                                       | **Label name**         |
|----------------------------|-------------------------|---------------------|----------------------------------------------------------------------------------------------------------------|------------------------|
| Advanced                   | Drop-ship and Drop-ship | Not applicable      | Blank                                                                                                          | Tax Schedule           |
| Advanced                   | Standard and Blanket    | Pickup              | Tax schedule assigned to the vendor’s purchase address                                                         | Purch Addr Tax Sched   |
| Advanced                   | Standard and Blanket    | No shipping method  | Tax schedule assigned to the vendor’s purchase address                                                         | Purch Addr Tax Sched   |
| Advanced                   | Standard and Blanket    | Delivery            | Purchases tax schedule assigned in the Company                                                                 | Company Tax Sched      |
| Single schedule            | Not applicable          | Not applicable      | Tax schedule that is assigned as the single tax schedule in the Purchase Order Processing Setup Options window | Single Tax Schedule ID |

>   Blanket

>   Setup window

>   *If you decided not to use the shipping method to determine the default tax
>   schedule and decided to use the advanced tax calculations method, the tax
>   schedule assigned to the vendor’s purchase address will be the default tax
>   schedule.*

#### Tax schedules for purchase order items

To calculate tax for an item, the tax schedule for the item is compared with
another tax schedule assigned to the item. Taxes aren’t calculated for the
control blanket line item of a blanket purchase order or a drop-ship blanket
purchase order. The default tax schedule for the item is as follows.

| **Item**             | **Default tax schedule**                                                                             |
|----------------------|------------------------------------------------------------------------------------------------------|
| Inventoried item     | Purchase tax schedule assigned to the item in the Item Maintenance window                            |
| Non-inventoried item | Tax schedule assigned to non-inventoried items in the Purchase Order Processing Setup Options window |

>   The default tax schedule to compare against the item’s tax schedule is as
>   follows.

| **Tax calculation option** | **Document type**    | **Inventory Control** | **Shipping method** | **Default tax schedule**                                                                                       | **Label name**         |
|----------------------------|----------------------|-----------------------|---------------------|----------------------------------------------------------------------------------------------------------------|------------------------|
| Advanced                   | All document types   | Not applicable        | No shipping method  | No tax schedule                                                                                                | Tax Schedule ID        |
| Advanced                   | All document types   | Not applicable        | Pickup              | Tax schedule assigned purchase address in the Purchasing Vendor Detail Entry window                            | Purch Addr Tax Sched   |
| Advanced                   | Standard and Blanket | Registered            | Delivery            | Purchase tax schedule assigned to the site                                                                     | Site Tax Schedule ID   |
| Advanced                   | Standard and Blanket | Not registered        | Delivery            | Purchases tax schedule assigned in the Company Setup window                                                    | Company Tax Sched      |
| Single schedule            | All document types   | Not applicable        | Not applicable      | Tax schedule that is assigned as the single tax schedule in the Purchase Order Processing Setup Options window | Single Tax Schedule ID |

>   **C H A P T E R 1 0** T A X E S F O R P U R C H A S E O R D E R S

#### Calculating and distributing summary taxes for purchase orders

>   Use the Purchase Order Tax Summary Entry window to edit or view summarized
>   tax amounts for a purchase order. Taxes are calculated automatically as you
>   enter each tax detail or edit the Total Purchases amount. Summary tax edits
>   won’t change the taxes calculated for each line item in the Purchase Order
>   Line Item Tax Detail Entry window. You won’t be able to edit tax included in
>   item price tax at the summary level. Tax edits made for each line item will
>   change the summary tax amounts in the Purchase Order Tax Summary Entry
>   window.

>   You can’t change the Tax amount in the Purchase Order Entry window or the
>   tax information in the Purchase Order Tax Summary Entry window if your
>   system isn’t set up to allow editing summary-level taxes. If you want to
>   change tax information, use the Purchase Order Line Item Tax Detail Entry
>   window. For more information about the setup option to make summary edits to
>   taxes, see the System Setup documentation.

>   If you are using Project Accounting, you can’t change the Tax amount in the

>   Purchase Order Entry window or the tax information in the Purchase Order Tax
>   Summary Entry window for standard and drop-ship purchase orders even if your
>   system is set up to allow editing summary-level taxes. If you want to change
>   tax information, use the Purchase Order Line Item Tax Detail Entry window.

>   **To calculate and distribute summary taxes for purchase orders:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter document information, including the document type, purchase order
    number, buyer ID, and the document date.

>   Choose the Date expansion button to open the Purchasing Date Entry window,
>   where you can enter a tax date and posting date that differ from the
>   document date. The tax date you enter is the date your tax records are
>   updated. To enter a tax date, the Enable Tax Date option the Company Setup
>   Options window must be marked.

1.  Enter or select a vendor ID. Choose the Vendor ID expansion button to view
    address, and shipping method information.

2.  Enter line item information. To change the tax status, tax schedules, or tax
    amount for an item, choose the Item or Vendor Item expansion button to open
    the Purchasing Item Detail Entry window.

3.  Enter total information. Taxes will be calculated automatically as you enter
    items. If you change the tax amount, you’ll need to edit the tax
    distribution amounts for your change.

4.  Choose the Tax expansion button in the Purchase Order Entry window to open
    the Purchase Order Tax Summary Entry window, where you can view or edit the
    tax distribution amounts.

![](media/2e3ee5bc4aebb65b6addaa60108ad766.jpg)

>   Currency amounts in this window may be displayed in the functional or
>   originating currency, depending on the view selected in the Purchase Order
>   Entry window.

1.  To edit tax information, enter or select a tax detail ID and enter a tax
    amount. Continue entering tax details until your tax is fully distributed.

2.  To distribute tax to multiple tax details, change the amount in the
    scrolling window and enter or select another tax detail and tax amount in
    the next available line.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row.

1.  Choose OK to save your entries and return to the Purchase Order Entry
    window.

>   Choose Delete to delete all the tax details for the purchase order.

>   Choose Default to restore the default tax information.

#### Calculating and distributing detail taxes for purchase order items

Use the Purchase Order Line Item Tax Detail Entry window to add, change, delete,
or view tax amounts calculated on an individual line item. Taxes are calculated
automatically as you enter each tax detail or edit the Total Purchases amount.

Summary tax edits won’t change the taxes calculated for each line item in the
Purchase Order Line Item Tax Detail Entry window. You will be able to edit tax
included in item price taxes. Tax edits made for each line item will change the
summary tax amounts in the Purchase Order Tax Summary Entry window.

>   **To calculate and distribute detail taxes for purchase order items:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter document information, including the document type, purchase order
    number, buyer ID, document date, and vendor ID.

2.  Enter or select a line item and choose the Vendor Item or Item expansion
    button to open the Purchasing Item Detail Entry window. You can change the
    tax status, tax schedules, or tax amount for an item.

>   Taxes will be calculated automatically as you enter items. If you change the
>   tax amount, you’ll need to edit the tax distribution amounts for your
>   change.

1.  Choose the Calculated Tax expansion button to open the Purchase Order Line
    Item Tax Detail Entry window, where you can view or edit tax distribution
    amounts.

![](media/0dbc915f59a9f4d55ce6106b2ae6e484.jpg)

1.  To edit tax distributions, enter or select a tax detail ID. Continue
    entering tax details until your tax is fully distributed.

2.  To distribute tax to multiple tax details, change the default amount in the
    scrolling window and enter or select another tax detail and tax amount in
    the next available line.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row.

1.  Choose OK to save your entries and return to the Purchasing Item Detail
    Entry window.

>   Choose Delete to delete all the tax details for the line item.

>   Choose Default to restore the default tax information.

114 P U R C H A S E O R D E R P R O C E S S I N G

**Chapter 11: Purchase order maintenance**

>   Throughout the purchasing process, you can print a variety of reports that
>   allow you to double-check the documents you’ve entered. If you identify
>   errors on these reports, the errors must be corrected to ensure accurate
>   reporting of your purchasing activity. You may want to delete and void
>   purchase orders that are no longer valid.

>   You may also want to change the status of your purchase orders or the status
>   of the line items after you’ve entered a purchase order in the Purchase
>   Order Entry window. When your purchase orders are complete, you can remove
>   them from the system or move them to history.

>   This information is divided into the following sections:

-   *Deleting a purchase order*

-   *Voiding a purchase order*

-   *Modifying a purchase order*

-   *Placing or removing a purchase order hold*

-   *Editing a purchase order that’s on hold*

-   *Status overview*

-   *Editing purchase order or line item status*

-   *Removing completed purchase orders*

#### Deleting a purchase order

>   Use the Purchase Order Entry window to delete purchase orders with a New
>   status (purchase orders that have never been printed or sent to the vendor).
>   You can’t delete purchase orders that have a status of Released or Change
>   Order, or when the status is New and there are unposted receipts or
>   invoices. To delete a purchase order when you are using Workflow, the
>   purchase order must have a Workflow status of Not Submitted or Submitted.
>   Deleting removes purchase order information from the system and makes
>   purchase order numbers available for reuse.

>   If you’re using Manufacturing and the job is linked to a job, you must have
>   authority to unlink items from jobs to be able to delete the purchase order.
>   Refer to Manufacturing documentation for more information. If you are using
>   Project Accounting, job links aren’t available for transactions that have
>   project information assigned to them.

>   **To delete a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select the number of the purchase order (with a New status) you
    want to delete.

>   *You cannot delete a purchase order that is linked to a sales line item with
>   a Quantity on*

>   *Purchase Order. You also cannot delete a purchase order that has a posted
>   payment in Payables Management or a prepayment that is included in a
>   payables computer check batch. To delete the purchase order, you must void
>   the posted payment in Payables Management or remove the prepayment from the
>   computer check batch.*

1.  Choose Actions and then select Delete.

>   **To delete a purchase order using the action pane:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  Mark the purchase orders (with a New status) you want to delete.

>   *You cannot delete a purchase order that is linked to a sales line item with
>   a Quantity on Purchase Order. You also cannot delete a purchase order when
>   it has a posted payment in Payables Management or a prepayment that is
>   included in a payables computer check batch. To delete the purchase order,
>   you must void the posted payment in Payables Management or remove the
>   prepayment from the computer check batch.*

1.  Delete the purchase orders.

#### Voiding a purchase order

>   Use the Purchase Order Entry window to void purchase orders with a New
>   status (purchase orders that have never been printed). To void a purchase
>   order when you are using Workflow, the purchase order must not be pending
>   changes or pending approval. Voiding moves purchase order information to
>   history and doesn’t make purchase order numbers available for reuse until
>   history is removed, if you’re keeping history. If you’re not keeping
>   history, voiding removes purchase order information.

>   If you track voided purchase orders, you’ll know why a purchase order number
>   is missing or out of sequence. If you’re tracking purchase order history,
>   you can view information about voided purchase orders using the purchasing
>   inquiry windows or by printing the Purchasing Voided Journal or the Purchase
>   Order History Report.

>   To void purchase orders or lines linked to jobs, you must have authority to
>   unlink line items from a job. Security is set in the Job Costing Preference
>   Defaults window. If you are using Project Accounting, job links aren’t
>   available for transactions that have project information assigned to them.

>   **To void a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select the number of the purchase order (with a New status) you
    want to void.

>   *You cannot void a purchase order that is linked to a sales line item with a
>   Quantity on Purchase Order. You also cannot void a purchase order that has a
>   posted payment in Payables Management or has a prepayment that is included
>   in a payables computer check batch. To void the purchase order, you must
>   void the posted payment in Payables Management or remove the prepayment from
>   the computer check batch.*

1.  Choose Actions and then select Void. Depending on if you’re keeping purchase
    order history, the purchase orders will be removed from the system, or moved
    to history.

>   The Purchasing Voided Journal is printed when you close the Purchase Order
>   Entry window after voiding, if you marked the option to print it in the
>   Posting Setup window.

#### Modifying a purchase order

>   Use the Purchase Order Entry window to add an additional item to a purchase
>   order after it’s been printed, to delete a line item if you haven’t released
>   it to the vendor, or to make other changes.

>   You can edit purchase orders with a Received, Closed, or Canceled status
>   using the

>   Purchase Order Entry window. To edit a closed or canceled purchase order,
>   use the Edit Purchase Order Status window. See *Editing purchase order or
>   line item status* for more information.

>   If you are using Workflow, review the following information about modifying
>   a purchase order.

-   You can modify a purchase order that is pending approval if you are the
    current approver of the purchase order.

-   You must resubmit a purchase order if you modify a standard or drop-ship
    purchase order that is approved or that doesn’t need approval.

-   You can modify the control line item of a blanket or drop-ship blanket
    purchase order, but you must resubmit the purchase order.

-   You can modify blanket line items without having to resubmit the blanket or
    drop-ship blanket purchase order.

>   **To modify a purchase order:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  Mark the purchase order you want to edit. In the Modify group, choose Edit
    to open the Purchase Order Entry window.

>   *If Edit isn’t available in the Modify group, the purchase order you have
>   selected has a Received, Closed, or Canceled status.*

1.  Highlight the fields to change and enter the correct information. If you
    won’t be receiving part of the quantity ordered for the purchase order that
    you are modifying, enter a canceled quantity. You can change line items that
    have quantities received or invoiced against them, but you can’t delete the
    line items. To add an additional item, enter or select an item.

>   You can’t change certain item information if the purchase order already has
>   items received or invoiced against it. (For example, you can’t change the U
>   of M or Site ID fields. You can change the Unit Cost and Extended Cost
>   fields if the line item isn’t Received or Closed.)

>   If you are using Project Accounting and the purchase order was entered for a
>   project, you can enter an inventoried item if the item was previously
>   assigned to a budget. Otherwise, you must add the item to a budget. You
>   cannot add a new inventoried item if the Allow Entry of New
>   Budgets/Materials option is not marked in the User Purchase Order Settings
>   window.

>   You can add or modify the prepayment amount until you receive or invoice
>   against the purchase order. You cannot add or modify the prepayment if there
>   is a posted payables payment for the prepayment or if the prepayment is
>   included in a computer check batch.

>   If you delete all the line items from a purchase order that has a posted
>   prepayment, you can apply the remaining prepayment amount to other documents
>   for the vendor after you cancel or close the purchase order.

1.  Choose File \>\> Print to print or reprint the purchase order (optional).

*If you are using Workflow, the purchase order must be approved before you can
print it.*

1.  Save the purchase order or submit the purchase order, if you are using
    Workflow.

#### Placing or removing a purchase order hold

>   You can place a purchase order on hold by marking the Hold check box in the

>   Purchase Order Entry window, if you have the option set up in the Purchase
>   Order Processing Setup window. See *Setting up Purchase Order Processing
>   preferences and default entries* for more information.

>   Occasionally a situation will arise that requires you to temporarily place a
>   purchase order on hold to stop further processing. For example, a buyer may
>   want to use a hold if he or she has a purchasing amount limit, and needs a
>   supervisor’s approval before sending a purchase order to the vendor. The
>   buyer could enter a purchase order and place it on hold, then print a copy
>   to send to the supervisor for approval. The printed purchase order will
>   clearly indicate that it is on hold. The buyer could later remove the hold
>   with the supervisor’s approval, and then print the purchase order and send
>   it to the vendor. The supervisor could also review the purchase order online
>   and remove the hold. The purchase order note field could be used for
>   entering comments. You can’t place a purchase order on hold if you are using
>   Workflow and the purchase order is pending approval.

>   Placing a hold on a purchase order you’ve already sent will prevent shipment
>   and shipment/invoice receipts from being entered or posted. You may want to
>   do this if problems arise with a vendor, and you don’t want to accept
>   shipments. You will be able to enter and save, but not post, invoice
>   receipts for purchase orders on hold.

>   Once a purchase order is on hold, you cannot edit it, unless you have
>   selected the option to Allow Editing of Purchase Orders on Hold in Purchase
>   Order Processing Setup. Printing a purchase order that is on hold will not
>   change its status.

>   You cannot place a purchase order on hold if the purchase order has a posted
>   or unposted prepayment. To place the purchase order on hold that has a
>   prepayment, you must complete one of the following tasks.

-   Void the posted prepayment in Payables Management.

-   Remove the prepayment from the payables computer check batch.

-   Remove the unposted manual prepayment from the Purchase Order Entry window.

>   **To place or remove a purchase order hold:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Select the purchase order you want to place on or release from hold.

2.  Mark or unmark the Hold check box and choose Save.

>   **To place or remove a purchase order hold using the action pane:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  Mark the purchase order you want to place on or release from hold.

3.  In the Modify group, choose Apply Hold or Remove Hold.

#### Editing a purchase order that’s on hold

>   The option to Allow Editing of Purchase Orders on Hold in the Purchase Order
>   Processing Setup window must be selected before you can edit a purchase
>   order that’s on hold.

>   If a purchase order with a Released status is on hold and you edit the
>   purchase order, the purchase order’s status will be changed to Change Order.

>   If the purchase order is on hold and you are allowed to edit purchase orders
>   on hold, you can enter a computer prepayment but not a manual prepayment.

#### Status overview

>   Purchase order and line item status indicates whether the line items and the
>   purchase order have been released to the vendor, received, changed, or
>   closed. A purchase order or line item can have one of six statuses:

| **Status**   | **How it’s assigned**                                                                                                                                                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| New          | The purchase order or line item is saved for the first time, and has not yet been released to the vendor. You can change a New line item or purchase order without affecting its status.                                                                                                                            |
| Released     | **Line item—**The standard or drop-ship purchase order is printed or sent in e-mail**.** The blanket line item is marked to release in the Purchasing Blanket Detail Entry window and the blanket purchase order or drop-ship blanket purchase order is printed. A New line is partially received against**.**      |
|              | **Purchase order—**At least one purchase order line has a status of Released, and there are no lines with a status of Change Order. Released status indicates that the purchase order has been sent to the vendor, and typically occurs when you send a New purchase order in e-mail or print a New purchase order. |
| Change Order | A purchase order or line item with a Released status has been edited. The purchase order could also have been manually changed from Closed or Received to Change Order.                                                                                                                                             |
| Received     | The entire quantity ordered has been received, but not matched to an invoice. There may be a canceled quantity, as well.                                                                                                                                                                                            |
| Closed       | **Line item—**The entire quantity ordered has been received and invoiced, and the line will not be processed any further.                                                                                                                                                                                           |
|              | **Purchase order—**All of the line items have been received and invoiced, and the purchase order will not be processed any further. There may be canceled lines, as well.                                                                                                                                           |
| Canceled     | **Line item—**The line item has not been received or invoiced against, and it is no longer valid. The line will not be processed any further.                                                                                                                                                                       |
|              | **Purchase order—**All of the line items have been canceled and haven’t been received or invoiced against.                                                                                                                                                                                                          |

>   There may be a canceled quantity, as well.

>   For information about changing purchase order or line item status, see
>   *Editing purchase order or line item status*.

#### Editing purchase order or line item status

>   Use the Edit Purchase Order Status window to change the status of a purchase
>   order or the status of the line items on a purchase order. You may want to
>   cancel a line item on a purchase order, for example, if the item you’ve
>   ordered has been discontinued or if you won’t be receiving part of the
>   quantity ordered for the purchase order. You won’t be able to edit a
>   purchase order in the Edit Purchase Order Status window if you are using
>   Workflow and the purchase order is pending approval.

>   You can change the status of an on-hold purchase order or its line items, if
>   you marked the option to allow editing of on-hold purchase orders in
>   Purchase Order Processing Setup. However, you cannot make changes that make
>   the status of an on-hold purchase order Received, Canceled, or Closed,
>   unless you remove the hold.

>   To remove a purchase order with a Released, Received, or Change Order
>   status, close the purchase order, transfer it to history (if you’re keeping
>   history) using the Remove Completed Purchase Orders window, and then remove
>   it using the Remove Purchasing History window.

>   You can close purchase orders with landed costs that haven’t been matched to
>   an invoice; however, if you close a purchase order line item with landed
>   costs that haven’t been matched to an invoice, the shipments for that line
>   item won’t be available for matching. You may need to manually adjust
>   General Ledger accruals for landed costs.

>   The control blanket line item for a blanket purchase order or a drop-ship
>   blanket purchase order won’t be displayed in the Edit Purchase Order Status
>   window. You can view the status of the control blanket line item in the
>   Purchasing Item Detail Entry window. The status of the control blanket line
>   item is the same as the blanket or drop-ship blanket purchase order’s
>   status.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category field will be displayed by the Description field in the Edit
>   Purchase Order Status scrolling window.

>   For more information about a specific status, see *Status overview*.

>   **To edit purchase order or line item status:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  Mark the purchase order that you want to edit the status of.

>   If a purchase order has a prepayment is included in a computer check batch,
>   you must remove the prepayment from the computer check batch before you can
>   select the purchase order.

1.  In the Modify group, choose Edit Purchase Order Status to open the Edit
    Purchase Order Status window.

![](media/3b9386932c3c2ae4bac92d895e8464a1.jpg)

1.  Change the purchase order status.

    -   Only statuses that are available for the purchase order will be
        displayed in the list.

    -   If a purchase order is on hold, you cannot change its status to
        Received, Closed, or Canceled unless you remove the hold.

    -   If a purchase order has sales commitments, you cannot change its status
        to Received, Closed, or Canceled.

    -   If the status of a blanket purchase order or a drop-ship blanket
        purchase order is changed from New to Released and not all of the
        blanket lines have been marked to be released in the Purchasing Blanket
        Detail Entry window, you’ll have the option to release all of the line
        items or release the line items marked to be released.

    -   If the contract expiration date for the purchase order has passed when
        changing the status from New to Released, you can release the line
        items.

2.  Change the purchase order line item status.

    -   You can change a status of a line item to Closed, if a receipt has been
        posted for the line, but you can’t reopen the item. If a line item has
        sales commitments, you cannot change its status to Received, Closed, or
        Canceled.

    -   You can change the quantity canceled; your changes may affect the status
        of the line item and the status of the purchase order. Use the line item
        information button to open the Purchasing Quantity Status window, where
        you can view quantity information for the line item, including the
        quantity ordered, the quantity remaining to be shipped, and remaining
        posted shipments to be matched.

    -   You can release a blanket line item if it hasn’t been marked to be
        released in the Purchasing Blanket Detail Entry window when you change
        the line item status from New to Released.

    -   You can release line items even if the contract expiration date has
        passed.

3.  Choose Process to process changes you’ve made.

>   The Release option in the Purchasing Blanket Detail Entry window will be
>   marked for those items that were released when changing statuses.

>   If you are using Workflow, you might have to resubmit the purchase order,
>   depending on the changes you’ve made.

>   If a New or Released purchase order that has a posted computer or manual
>   payment is closed or canceled after canceling the remaining quantities, any
>   remaining prepayment amount is an unapplied payment in Payables Management.
>   You can apply the remaining prepayment to other documents for the vendor.

>   Depending on your changes and whether or not the prepayment for a new or
>   printed purchase order is posted, the prepayment amount changes to zero or
>   the remaining prepayment amount is an unapplied payment in Payables
>   Management. You can apply the remaining prepayment to other documents for
>   the vendor after the purchase order is closed or canceled.

>   *Amounts may be posted to General Ledger when you close purchase orders or
>   line items that have an item with a shipped quantity that is greater than
>   the invoiced quantity. Purchase receipts in Inventory Control may be
>   adjusted, as well.*

>   One or more posting journals and distribution breakdown registers may be
>   printed when you close the Edit Purchase Order Status window, depending on
>   the options selected in the Posting Setup window.

#### Removing completed purchase orders

>   Use the Remove Completed Purchase Orders window to remove any closed or
>   canceled documents from the Purchase Order Work table that haven’t yet been
>   removed or moved to history. You should remove your completed purchase
>   orders periodically.

>   If you’re keeping purchase order history and you remove completed purchase
>   orders, the purchase orders will be moved to history. If you aren’t keeping
>   history, completed purchase orders will be deleted from your records. For
>   more information, see *Chapter 27, “Purchase order history removal.”*

>   After you’ve transferred the completed purchase orders to history, you can
>   use the Remove Purchasing History window to delete purchase order history or
>   print the Purchase Order Trx History Removal Report before removing history.

>   *Before removing purchase orders, back up your company’s accounting data.
>   For more information about making backups, refer your System Administrator’s
>   Guide (Help \>\> Contents \>\> select System Administration).*

>   **To remove completed purchase orders:**

1.  Open the Remove Completed Purchase Orders window.

>   (Purchasing \>\> Routines \>\> Remove Completed Purchase Orders)+

![](media/e8993c68de4bf303a2fadd21fb4ee843.jpg)

1.  Select a type of range to remove information for purchase orders, then enter
    the first and last records in the selected range.

2.  Choose Insert to insert the range you’ve chosen to remove in the
    Restrictions List.

>   You can insert only one restriction for each document range. For example,
>   you can insert one purchase order number restriction (PO001 to PO099) and
>   one vendor ID restriction (ADVANCED0001 to BEAUMONT0001).

1.  Choose Restrictions to open the Restrict Purchasing Documents window to
    select documents you want to remove from the range you’ve entered
    (optional).

![](media/c56f1a7b945453b3942f813d3735c33c.jpg)

>   For example, assume that you entered a range restriction to include purchase
>   order numbers PO0990 through PO1010. Purchase order PO1000 was canceled
>   because the vendor was out of stock of the items, but now the vendor can
>   fill the order. You can remove the mark from the Process box for PO1000 so
>   that purchase order won’t be removed, as in the following example.

1.  Choose the Process button to remove purchase orders.

When processing is complete, the Completed PO Removal Report is printed, listing
the purchase orders that were removed from the Purchase Order Work Table.

**Part 3: Receipts**

>   This part of the documentation explains how to enter and manage receipts.
>   The data entry windows were designed to resemble actual receipt documents,
>   with vendor, line item, and totals information. Receipts can be saved,
>   edited if necessary, and then posted so that they become part of your
>   permanent accounting records. Posting receipts also updates inventory
>   quantities. If your system includes General Ledger, you can update the
>   balances of your posting accounts, as well.

>   Following is a list of topics that are discussed:

-   *Chapter 12, “Receipt batches,”* explains how to use batches to group
    purchasing documents for posting.

-   *Chapter 13, “Shipment and in-transit inventory receipt entry,”* describes
    how to enter shipment, shipment/invoice, and in-transit inventory receipts.

-   *Chapter 14, “Shipment receipt entry for projects,”* describes how to enter
    shipment and shipment/invoice receipts for projects.

-   *Chapter 15, “Shipment receipt detail entry,”* describes how to enter
    detailed information about a document, line item, or other elements of a
    transaction.

-   *Chapter 16, “Invoice receipt entry,”* explains how to enter invoice
    receipts and match them to shipment receipts.

-   *Chapter 17, “Invoice receipt entry for projects,”* explains how to enter
    invoice receipts and match them to shipment receipts for projects.

-   *Chapter 18, “Invoice receipt detail entry,”* describes how to enter
    detailed information about a document, or other elements of a transaction.

-   *Chapter 19, “Landed costs for receipts,”* describes how to enter,
    apportion, and match landed costs.

-   *Chapter 20, “Taxes for receipts,”* explains how tax is calculated,
    modified, and distributed for receipts.

-   *Chapter 21, “Receipt posting,”* describes the methods of posting
    transactions in Purchase Order Processing.

-   *Chapter 22, “Receipt maintenance,”* includes procedures for correcting,
    deleting, and voiding shipment, in-transit inventory, and invoice receipts.

**Chapter 12: Receipt batches**

>   All receipt document types can be entered in a batch. Batches are groups of
>   transactions, identified by a name or a number, that are used for
>   identification purposes and to make the posting process easier. You can
>   enter receipts in batches to group similar transactions during data entry
>   and review them before posting at a later time. Batches can be identified as
>   a group of transactions entered by a specific employee, or a group of
>   transactions entered on a particular date.

>   To post invoice receipts in a batch if you are using vendor approval
>   workflow, the vendors assigned to invoice receipts must have the workflow
>   status of Approved or No Approval Needed. If you post a batch and a vendor
>   isn’t approved, invoice receipts for that vendor aren’t posted and remain in
>   the batch. For more information about vendor approval workflow, see *Vendor
>   approval workflow*.

>   This information is divided into the following sections:

-   *Using batches to group receipts*

-   *Creating a receipt batch*

-   *Modifying or deleting a batch*

#### Using batches to group receipts

>   Receipts can be entered individually or in batches. Individual transactions
>   are entered and posted immediately, so your records are always up to date.
>   You can’t print edit lists for transactions that aren’t entered in a batch.
>   Batches can be used to group and save transactions, which allows you to
>   review the transactions and make corrections before they’re posted. More
>   than one person can enter transactions in the same batch; however, a batch
>   can’t be posted if anyone is making changes to it.

>   Purchase Order Processing batches originate in either the Receivings
>   Transaction

>   Entry window or the Purchasing Invoice Entry window. A batch with a
>   Receivings Transaction Entry origin can contain a mix of different receipt
>   document types. A batch with a Purchasing Invoice Entry origin can contain
>   only invoice receipt documents. Since batches can have only one origin, you
>   can have batches with the same name, but different origins.

-   For information about entering transactions with the Receivings Transaction
    Entry origin, see *Chapter 13, “Shipment and in-transit inventory receipt
    entry.”*

-   For information about entering transactions with the Purchasing Invoice
    Entry origin, see *Chapter 16, “Invoice receipt entry.”*

#### Creating a receipt batch

>   Use the Purchasing Batch Entry window to create a receipt batch. Each
>   transaction in the batch must have the same origin.

>   **To create a receipt batch:**

1.  Open the Purchasing Batch Entry window.

>   (Purchasing \>\> Transactions \>\> Purchasing Batches)

![](media/027908d84619078250757fe4699fa39f.jpg)

1.  Enter a batch ID to identify the batch.

2.  Select a batch origin.

3.  Enter a batch comment.

4.  Enter a posting date.

>   *This field is available only if, in the Posting Setup window, Batch is
>   selected in the Posting Date From field.*

>   The posting date you enter here is the date that General Ledger files are
>   updated. Your records in Purchase Order Processing are updated using the
>   receipt date you enter in the Receivings Transaction Entry window or the
>   invoice date you enter in the Purchasing Invoice Entry window.

>   If the batch contains multicurrency transactions whose exchange rates
>   expired before the batch posting date, you will be able to save but not post
>   those transactions.

1.  When you have entered and saved all transactions for a batch, choose File
    \>\> Print to verify your entries with a Receivings Edit List or a
    Purchasing Invoice Edit List.

#### Modifying or deleting a batch

>   Use the Purchasing Batch Entry window to change or delete an unposted batch.
>   See *Chapter 22, “Receipt maintenance,”* for information about changing the
>   transactions in a batch.

>   **To modify or delete a batch:**

1.  Open the Purchasing Batch Entry window.

>   (Purchasing \>\> Transactions \>\> Purchasing Batches)

1.  Enter or select a batch ID. If you enter a batch, you also must enter the
    batch origin before information about the batch will be displayed.

2.  If you select a batch that has been marked for posting, you won’t be able to
    edit it.

3.  To correct the batch, replace the incorrect information with correct
    information. Choose Save to save your changes. To delete the batch, choose
    Delete.

**Chapter 13: Shipment and in-transit inventory receipt entry**

>   A shipment receipt is a document used to record shipments received for
>   purchase orders. You can enter two types of shipment receipts in Purchase
>   Order Processing: shipment/invoice and shipment. Enter a shipment/invoice
>   receipt to record the receipt of goods and services accompanied by an
>   invoice. Enter a shipment receipt to record the receipt of goods and
>   services without an invoice. You can enter receipt transactions in a batch
>   or enter and post them individually. Receipts can’t be saved unless they’re
>   in a batch.

>   If you are transferring material from one site to another and want to use a
>   via site, you can enter in-transit transfers in Inventory Control. A via
>   site is an interim location to prevent the material from being sold while
>   the material is in-transit. After you post the in-transit transfer, you can
>   use the Receivings Transaction Entry window to enter an in-transit inventory
>   receipt. An in-transit inventory receipt is a document used to record the
>   receipt of the material into the final destination site.

>   If you are using Project Accounting and want to enter shipment/invoice
>   receipts or shipment receipts for projects, see *Chapter 14, “Shipment
>   receipt entry for projects.”*

>   This information is divided into the following sections:

-   *Receiving a shipment/invoice*

-   *Receiving a shipment*

-   *Receiving items without a purchase order*

-   *Receiving items using the Select Purchase Order window*

-   *Using the Select Purchase Order Items window*

-   *Receiving items from multiple purchase orders*

-   *Receiving items from a purchase order*

-   *Entering an in-transit inventory receipt*

-   *Using the Select In-Transit Items window*

-   *Receiving items from in-transit transfers*

#### Receiving a shipment/invoice

>   Use the Receivings Transaction Entry window to record a shipment/invoice if
>   you’ve received an invoice and merchandise at the same time. The inventory
>   quantity on hand will be updated for the items received and the vendor’s
>   account will be increased. You can include items from multiple purchase
>   orders (from a single vendor) on a shipment/invoice receipt.

>   You can receive against line items with New, Released, Change Order, or
>   Received statuses; however, only active items can be entered. You can
>   continue processing if the item is inactive, but you can’t change the
>   quantity.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   You can’t enter a shipment/invoice receipt for a purchase order that is on
>   hold. If a purchase order is placed on hold after its shipment/invoice
>   receipt is saved to a batch, the receipt for that purchase order will not be
>   posted and will remain in the batch.

>   If you are using Project Accounting, you can enter a shipment/invoice for
>   blanket purchase orders. The Project Number field and the Cost Category ID
>   field will be displayed in the Receivings Transaction Entry window, but you
>   can’t enter project information. To enter a shipment/invoice for a purchase
>   order with project information, see *Chapter 14, “Shipment receipt entry for
>   projects.”*

>   You can use the View \>\> Currency menu option or the currency list button
>   to view currency amounts in the Receivings Transaction Entry window in the
>   originating or functional currency.

>   **To receive a shipment/invoice:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Shipment and Invoice Receipt
    to open the Receivings Transaction Entry window.

![](media/ba97b49731305a1a6612cf0d7c27bb55.jpg)

1.  Enter a vendor document number.

2.  Enter the receipt date.

>   *To enter a General Ledger posting date that is different from the
>   transaction date, choose the Date expansion button; the Receivings Date
>   Entry window will open, where you can enter date information.*

>   For multicurrency transactions, the document date determines which exchange
>   rate is used, based on the currency ID and the associated rate type entered
>   for the transaction.

1.  Enter or select a batch ID (optional).

>   In multicurrency transactions, if the batch posting date does not fall on or
>   before the exchange rate’s expiration date, you will receive a message.
>   Choose Yes to open the Batch Entry window and change the batch posting date.
>   If you choose No, you will be able to save but not post the receipt.

>   See *Creating a receipt batch* for more information.

1.  Enter or select a vendor ID.

2.  Enter or select a currency ID. If a currency ID is assigned to the vendor
    you select, it will appear in the Currency ID field. The currency ID
    assigned to the shipment/invoice must match the currency ID of the purchase
    orders being received against.

3.  Enter or select the purchase order number for which you’re receiving a
    shipment/invoice. You can receive items from multiple purchase orders by
    entering or selecting a different purchase order number in a new row. See
    *Receiving items from multiple purchase orders* for more information.

>   If the Allow Receiving Without a Purchase Order option is marked in Purchase
>   Order Processing Setup, you can leave the PO Number field blank.

>   Before you can receive against the purchase order that has an unposted
>   prepayment, you must post the prepayment or remove the prepayment from the
>   purchase order.

1.  Enter items using either the vendor’s item number or your company’s item
    number. You also can enter a non-inventoried item.

>   You can display the vendor’s item number by marking Options \>\> Display
>   Vendor Item. If the option is not marked, your company’s item number will be
>   displayed. You can change this selection at any time.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter the quantity shipped.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window will open if an item
>   that isn’t tracked by lot or serial numbers requires that you enter bin
>   information.*

>   An icon will be displayed in the Qty Shipped field for purchase order line
>   items with sales commitments. Select a line item and choose the button next
>   to the Qty Shipped heading to view or prioritize commitments in the Sales
>   Commitments for Purchase Order window. For more information, see *Committing
>   purchase orders to sales documents*.

>   If you’re using multiple bins and you change the quantity shipped or the
>   unit of measure after selecting bins for an item, you might have to modify
>   the bin information.

1.  You can change the site ID to receive line items to a location other than
    the location specified on the purchase order, if the option is marked in
    Purchase Order Processing Setup. Changing the site on the receipt will not
    change the site on the purchase order.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The Purchasing
>   Lot Number Entry window or the Purchasing Serial Number Entry window will
>   open for you to assign lot numbers or serial numbers. You can change the
>   bin.

1.  You can edit the unit cost or extended cost, if the Allow Editing of Costs
    in Receiving option is marked in the Purchase Order Processing Setup window.

2.  Enter the quantity invoiced, which is the number of items on the vendor’s
    invoice.

3.  Enter trade discount, freight, miscellaneous, and tax amounts.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   If you want to change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for shipment/invoice receipts*. If you want to
>   change the tax amounts for a line item, see *Calculating and distributing
>   detail taxes for shipment/invoice line items*.

1.  The Prepayment field displays the total of all posted prepayments consumed
    for the purchase orders you are receiving against. The prepayment amount is
    recalculated if you change the quantity shipped, quantity invoiced, unit
    cost, or extended cost for a line item. The prepayment amount is also
    recalculated if you change the trade discount.

>   If a purchase order has a posted prepayment, you can use the Prepayment
>   expansion button to open the Purchasing Prepayment Summary Inquiry window.
>   You can use this window to view the total amount of the prepayments applied
>   and the prepayment applied amount for each purchase order assigned to the
>   shipment/invoice.

1.  Enter or accept the 1099 amount, if applicable.

2.  Enter or accept the payment terms and tax schedule ID.

3.  If you are using Project Accounting, choose the Amount Received expansion
    button to open the PA Receivings Amount Received Entry window, where you can
    enter an amount received. You can enter the amount you’re paying by cash,
    check, or credit card.

4.  If you are using landed costs, choose Landed Cost to open the Receivings
    Landed Cost Apportionment Entry window, where you can add landed costs to
    all line items on a receipt. See *Entering landed costs for a shipment
    receipt* for more information. If you want to enter landed costs for an
    item, see *Entering landed costs for a shipment item*.

5.  Choose the Attachment Management icon to attach documents to the shipment,
    if applicable.

6.  Choose Distributions to open the Purchasing Distribution Entry window, where
    you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account in the scrolling window, select the row containing
        the account and choose Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions for a landed cost won’t be
>   displayed in the Purchasing Distribution Entry window. To view landed cost
>   distributions, print the Receivings Edit List.

>   See *Distributing transaction amounts for shipment receipts* for more
>   information.

1.  Choose User-Defined to open the Receivings User-Defined Fields Entry window,
    where you can enter user-defined information for this receipt.

2.  Choose Save or Post. If you post the receipt, one or more posting journals
    and distribution breakdown registers may be printed, depending on the
    options selected in the Posting Setup window.

>   If you’ve entered a batch ID, you can’t post the transaction individually;
>   you must use batch posting, series posting, or master posting. For more
>   information, see *Chapter 12, “Receipt batches.”*

#### Receiving a shipment

>   Use the Receivings Transaction Entry window to record a shipment if you’ve
>   received merchandise but haven’t received the invoice for the merchandise. A
>   shipment transaction will increase the quantity on hand for the items
>   received for sales and discontinued item types. You can include items from
>   multiple purchase orders (from a single vendor) on a shipment receipt.

>   You can receive against line items with New, Released, Change Order, or
>   Received statuses.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   You can’t enter a shipment receipt for a purchase order that is on hold. If
>   a purchase order is placed on hold after its shipment receipt is saved to a
>   batch, the receipt for that purchase order will not be posted and will
>   remain in the batch.

>   If you are using Project Accounting, you can enter a shipment for blanket
>   purchase orders. The Project Number field and the Cost Category ID field
>   will be displayed in the Receivings Transaction Entry window, but you can’t
>   enter project information. To enter a shipment for a purchase order with
>   project information, see *Chapter 14, “Shipment receipt entry for
>   projects.”*

>   You can use the View \>\> Currency menu option or the currency list button
>   to view amounts in the Receivings Transaction Entry window in originating or
>   functional currency.

>   **To receive a shipment:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Shipment Receipt to open the
    Receivings Transaction Entry window.

![](media/fee9bc61324d0b6a5af63c18d0817222.jpg)

1.  Enter a vendor document number (optional).

2.  Enter the receipt date.

>   *To enter a General Ledger posting date that is different from the
>   transaction date, choose the Date expansion button; the Receivings Date
>   Entry window will open, where you can enter date information.*

>   For multicurrency transactions, the document date determines which exchange
>   rate is used, based on the currency ID and associated rate type that’s
>   entered for the transaction.

1.  Enter or select a batch ID (optional). See *Creating a receipt batch* for
    more information.

>   In multicurrency transactions, if the batch posting date does not fall on or
>   before the exchange rate’s expiration date, you will receive a message.
>   Choose Yes to open the Batch Entry window and change the batch posting date.
>   If you choose No, you will be able to save but not post the receipt.

1.  Enter or select the vendor ID.

2.  Enter or select a currency ID. If a currency ID is assigned to the vendor
    you select, it will appear in the Currency ID field. The currency ID
    assigned to the invoice must match the currency ID of the purchase order
    being received against.

3.  Enter the purchase order number for which you’re receiving a shipment. You
    can receive items from multiple purchase orders by entering or selecting a
    different purchase order number in a new row. See *Receiving items from
    multiple purchase orders* for more information.

>   If the Allow Receiving Without a Purchase Order option is marked in Purchase
>   Order Processing Setup, you can leave the PO Number field blank.

>   Before you can receive against the purchase order that has an unposted
>   prepayment, you must post the prepayment or remove the prepayment from the
>   purchase order.

1.  Enter items using either the vendor’s item number or your company’s item
    number. You also can enter a non-inventoried item.

>   You can display the vendor’s item number by marking Options \>\> Display
>   Vendor Item. If the option is not marked, your company’s item number will be
>   displayed. You can change this selection at any time.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  You can change the site ID to receive line items to a location other than
    the location specified on the purchase order, if the option is marked in
    Purchase Order Processing Setup. Changing the site on the receipt will not
    change the site on the purchase order.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The Purchasing
>   Lot Number Entry window or the Purchasing Serial Number Entry window will
>   open for you to assign lot numbers or serial numbers. You can change the
>   bin.

1.  Enter the quantity shipped.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window will open if an item
>   that isn’t tracked by lot or serial numbers requires that you enter bin
>   information.*

>   An icon will be displayed in the Qty Shipped field for purchase order line
>   items with sales commitments. Select a line item and choose the button next
>   to the Qty Shipped heading to view or prioritize commitments in the Sales
>   Commitments for Purchase Order window. For more information, see *Committing
>   purchase orders to sales documents*.

>   If you're using multiple bins and you change the quantity shipped or the
>   unit of measure after selecting bins for an item, you might have to modify
>   the bin information.

1.  You can edit the unit cost or extended cost, if the Allow Editing of Costs
    in Receiving option is marked in Purchase Order Processing Setup.

2.  If you are using landed costs, choose Landed Cost to open the Receivings
    Landed Cost Apportionment Entry window, where you can add landed costs to
    all line items on a receipt. See *Entering landed costs for a shipment
    receipt* for more information. If you want to enter landed costs for an
    item, see *Entering landed costs for a shipment item*.

3.  Choose the Attachment Management icon to attach documents to the shipment,
    if applicable.

4.  Choose Distributions to open the Purchasing Distribution Entry window, where
    you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account in the scrolling window, select the row containing
        the account and choose Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions for a landed cost won’t be
>   displayed in the Purchasing Distribution Entry window. To view landed cost
>   distributions, print the Receivings Edit List.

>   See *Distributing transaction amounts for shipment receipts* for more
>   information.

1.  Choose User-Defined to open the Receivings User-Defined Fields Entry window,
    where you can enter user-defined information for this receipt.

2.  Choose Save or Post. If you post the receipt, one or more posting journals
    and distribution breakdown registers may be printed, depending on the
    options selected in the Posting Setup window.

>   If you’ve entered a batch ID, you can’t post the transaction individually;
>   you must use batch posting, series posting, or master posting. For more
>   information, see *Chapter 12, “Receipt batches.”*

#### Receiving items without a purchase order

>   In the Receivings Transaction Entry window, you have the option to receive
>   items that weren’t included on the original purchase order or receive items
>   without a purchase order.

>   To set up this option, you must select to allow receiving items without a
>   purchase order in the Purchase Order Processing Setup window. You may assign
>   a password that must be entered before entering a line item not assigned to
>   a purchase order.

>   If you are using Project Accounting, you can receive items without project
>   information. The Project Number field and the Cost Category ID field will be
>   displayed in the Receivings Transaction Entry window. To enter a shipment/
>   invoice or shipment with project information, see *Chapter 14, “Shipment
>   receipt entry for projects.”*

>   **To receive items without a purchase order:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select the appropriate document type for the transaction.

2.  Enter the receipt number, vendor document number, date, and vendor ID.

3.  To add vendor items or items that weren’t included on the original purchase
    order, simply leave the PO number field blank. You don’t have to enter a
    purchase order if you’ve set up the system to allow receiving items without
    a purchase order.

4.  Continue entering the receipt.

>   You must enter the unit cost of non-inventoried items.

1.  In the Receivings Transaction Entry window, save or post the transaction.

#### Receiving items using the Select Purchase Order window

>   Use the Select Purchase Order window to select a purchase order to quickly
>   enter line items on a shipment or shipment/invoice. See *Receiving a
>   shipment* or *Receiving a shipment/invoice* for more information.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   If you are using Project Accounting, you can receive items for blanket
>   purchase orders. The Project Number field and the Cost Category ID field
>   will be displayed in the Receivings Transaction Entry window, but you can’t
>   enter project information. To receive items for purchase orders with project
>   information, see *Chapter 14, “Shipment receipt entry for projects.”*

>   **To receive items using the Select Purchase Order window:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select the appropriate document type for the transaction.

2.  Enter the receipt number, vendor document number, and date. (A vendor
    document number is required for a shipment/invoice.)

3.  Choose Auto-Rcv to automatically receive items. The Select Purchase Order
    window will open.

>   *If you entered a vendor ID, the Select Purchase Order Items window will
>   open instead of the Select Purchase Order window.*

![](media/52b30e91b168f623ad32138cfd2cc98e.jpg)

1.  Enter or select a purchase order for which you want to receive line items.

2.  Choose Receive All in the Select Purchase Order window to automatically
    receive all items on the selected purchase order.

>   You cannot receive against a purchase order that has an unposted prepayment.
>   You can remove the prepayment from the purchase order using the Purchase
>   Order Entry window or complete a computer check run for the prepayment.

>   The control blanket line item for a blanket purchase order or a drop-ship
>   blanket purchase order isn’t included when you automatically receive items.
>   Blanket line items with a New status won’t be included, either. You can use
>   the Receivings Transaction Entry window to enter blanket line items with a
>   New status.

>   If you choose to view details in the Select Purchase Order window, the
>   Select Purchase Order Items window will open, and the purchase order line
>   items will be marked to receive. Choose Receive to automatically receive
>   items on the selected purchase order.

>   Blanket line items with a New status or line items with a New status for a
>   standard purchase order with an expired contract date won’t be marked. To
>   receive these items, you must mark the items individually.

>   In the Receivings Transaction Entry window, continue entering receipt
>   information, if necessary, and save or post the transaction.

#### Using the Select Purchase Order Items window

>   Use the Select Purchase Order Items window to receive line items on multiple
>   purchase orders. In the Select Purchase Order Items window, the tree view
>   and the Sort By option control the information that is displayed. When you
>   change the focus in the tree view, or when you choose a different sorting
>   option, the information in the window is refreshed.

>   The scrolling window shows detail about the object selected in the tree
>   view. When you highlight a different object in the tree view, such as a
>   purchase order or a site, only the information about that object is
>   displayed in the scrolling window. To display all information for a vendor,
>   you must select the vendor ID in the tree view.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Select Purchase Order Items
>   scrolling window.

>   The sorting option you select determines the order in which objects appear
>   in the tree view and the scrolling window. You can sort objects in four
>   ways:

>   **PO/Items** Objects in the tree view and scrolling window are sorted first
>   by purchase order number, then by the order items were entered on the
>   purchase orders.

![](media/c3c1ab10c8eb3a131da66a4583d8478e.jpg)

>   **Item Number/PO** Objects in the tree view and scrolling window are sorted
>   first by item number, then by purchase order number under each item.

![](media/621adf4ad91c0f1ac093be2f9d7f2ca6.jpg)

>   **Site/PO/Item Number** Objects in the tree view and scrolling window are
>   sorted first by site, then by purchase order number under each site, then by
>   item number under each purchase order.

![](media/92ce5f82b583c1d06a4ccf3c04b9bc9a.jpg)

>   **Site/Item Number/PO** Objects in the tree view and scrolling window are
>   sorted first by site, then by item number under each site, then by purchase
>   order number under each item.

![](media/c4b2ed4154a9a756561b58ebd7eeace4.jpg)

#### Receiving items from multiple purchase orders

>   Use the Select Purchase Order Items window to receive line items on multiple
>   purchase orders. New, Released, or Change Order purchase orders that have
>   one or more items with a quantity remaining to receive will be displayed.
>   See *Receiving a shipment* or *Receiving a shipment/invoice* for more
>   information.

>   If you are using Workflow, purchase orders must be approved before you can
>   receive against them. You can receive against purchase orders that don’t
>   need approval.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Select Purchase Order Items
>   window. To receive items from purchase orders with project information, see
>   *Chapter 14, “Shipment receipt entry for projects.”*

>   **To receive items from multiple purchase orders:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose the appropriate document type
    for the transaction to open the Receivables Transaction Entry window.

3.  Enter the vendor document number, and date. (A vendor document number is
    required for a shipment/invoice.)

4.  Enter or select a vendor ID. The currency ID assigned to the vendor will be
    the default currency ID for the receipt.

5.  Choose the Auto-Rcv button. The Select Purchase Order Items window will
    open.

>   New, Released, or Change Order purchase orders that have one or more items
>   with a quantity remaining to receive will be displayed. The control blanket
>   line item for a blanket purchase order or a drop-ship blanket purchase order
>   isn’t included when you automatically receive items.

>   If only a Vendor ID is displayed, the selected vendor does not have any New,

>   Released, or Change Order purchase orders with items to receive. Only

>   purchase orders with currency IDs that match the receipt will be displayed.
>   Purchase orders with posted prepayments that have currency IDs that match
>   the receipt will be displayed.

>   *If you know the purchase order number but not the vendor ID, you can choose
>   AutoRcv without entering a vendor ID. The Select Purchase Order window will
>   open. The vendor and currency ID for the receipt will come from the purchase
>   order you select.*

![](media/e0ad5b55968e990a88c2585f8e4bd114.jpg)

1.  Select a sorting option.

2.  Mark the check boxes next to the items you want to receive. To select all
    items displayed in the scrolling window, choose Mark All.

>   Blanket line items with a New status or line items with a New status for a
>   standard purchase order with an expired contract date won’t be marked. To
>   receive these items, you must mark the items individually.

>   *When you choose Mark All or Unmark All in the Select Purchase Order Items
>   window, only items displayed in the scrolling window will be marked or
>   unmarked. For example, if a purchase order is selected in the tree view,
>   only items from that purchase order will be displayed in the scrolling
>   window, and only those items will be marked when you choose Mark All. To
>   mark or unmark all items for a vendor, the vendor ID must be selected in the
>   tree view.*

1.  Select whether to display all items or only items marked to receive.

2.  Edit Quantity Shipped, Quantity Invoiced (for shipment/invoice receipts) and
    Unit Cost amounts, if necessary. If you edit an item in the scrolling
    window, it will be marked to receive.

3.  Choose the Receive button to add the items to your receipt. The Select
    Purchase Order Items window will close, and the items will appear in the
    Receivings Transaction Entry window. Taxes are calculated at this time.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Receivings Transaction Entry window, save or post the receipt.

#### Receiving items from a purchase order

>   Use the Select Purchase Order Items window and the Receivings Transaction
>   Entry window to receive items. After you enter or select a standard or
>   blanket purchase order with a New, Released, or Change Order status in the
>   Purchase Order Entry window, you can select to receive items or receive and
>   invoice items. From the Actions button, you can select the Receive the PO
>   Items option to enter a shipment receipt. You can select the Receive and
>   Invoice the PO Items option to enter a shipment/invoice receipt for a
>   purchase order. If you are using Workflow, the purchase order must be
>   approved before you can receive against it. You can receive against a
>   purchase order that doesn’t need approval.

>   For more information about a shipment receipt or a shipment/invoice receipt,
>   see *Receiving a shipment* or *Receiving a shipment/invoice*. For more
>   information about the Select Purchase Order Items window, see *Using the
>   Select Purchase Order Items window*.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category

>   ID field will be displayed in the Select Purchase Order Items window and the
>   Receivings Transaction Entry window. To receive items with project
>   information, see *Chapter 14, “Shipment receipt entry for projects.”*

>   **To receive items from a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a standard or blanket purchase order that has one or more
    items with a quantity to receive.

2.  Choose Actions, and then select one of the following options.

    -   If you are receiving goods and services without an invoice, select
        Receive the PO Items.

    -   If you are receiving goods and services accompanied by an invoice,
        select Receive and Invoice the PO Items.

3.  The Select Purchase Order Items window and the Receivings Transaction Entry
    window will open.

>   In the Select Purchase Order Items window, New, Released, or Change Order
>   purchase orders that have one or more items with a quantity remaining to
>   receive will be displayed. The purchase order that you entered in the
>   Purchase Order Entry window will be selected in the tree view. Each item on
>   the purchase order that is available to be received in the scrolling window
>   is marked, except for blanket line items that have a status of New. The
>   control blanket line item for a blanket purchase order isn’t included when
>   you receive items.

1.  Select a sorting option.

2.  Mark the check boxes next to the items to receive. To select all items
    displayed in the scrolling window, choose Mark All.

>   Blanket line items with a New status or line items with a New status for a
>   standard purchase order with an expired contract date won’t be marked. To
>   receive these items, you must mark the items individually.

>   *When you choose Mark All or Unmark All, only items displayed in the
>   scrolling window will be marked or unmarked. For example, if a purchase
>   order is selected in the tree view, only items from that purchase order will
>   be displayed in the scrolling window, and only those items will be marked
>   when you choose Mark All. To mark or unmark all items for a vendor, the
>   vendor ID must be selected in the tree view.*

1.  Select whether to display all items or only items marked to receive.

2.  Modify the quantity shipped, quantity invoiced (for shipment/invoice
    receipts) and unit cost amounts, if necessary. If you edit an item in the
    scrolling window, it will be marked to receive.

3.  Choose Receive to add the items to your receipt. The Select Purchase Order
    Items window will close, and the items will appear in the Receivings
    Transaction Entry window. Taxes are calculated at this time.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Receivings Transaction Entry window, continue entering receipt
    information, if necessary, and save or post the transaction. For a shipment/
    invoice, you must enter the vendor document number.

#### Entering an in-transit inventory receipt

>   If you’ve entered an in-transit transfer transaction in Inventory Control,
>   you can record the receipt of the material into the final destination site
>   using an in-transit inventory receipt type in the Receivings Transaction
>   Entry window. Any landed costs incurred as a result of the in-transit
>   transfer can be recorded on the in-transit inventory receipt, as well. After
>   you post the in-transit inventory receipt, the goods are removed from the
>   via site and placed in the final destination site. Landed costs from
>   in-transit transfer receipts can be invoiced just like landed costs incurred
>   on shipments or shipment invoices in the Purchasing Invoice Entry window.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field are displayed in the Receivings Transaction Entry window,
>   but you can’t enter project information for an in-transit inventory receipt.

>   **To enter an in-transit inventory receipt:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose In-Transit Inventory to open
    the Receivings Transaction Entry window.

![](media/31ea4dff0bd8d840e414b19b3d2c3a54.jpg)

1.  Enter the receipt date.

>   *To enter a General Ledger posting date that is different from the
>   transaction date, choose the Date expansion button; the Receivings Date
>   Entry window will open, where you can enter date information.*

1.  Enter or select a batch ID (optional).

>   See *Creating a receipt batch* for more information.

1.  Enter or select the transfer number for which you’re entering a receipt. You
    can receive items from multiple transfer numbers by entering or selecting a
    different transfer number in a new row.

2.  Enter items using either the vendor’s item number or your company’s item
    number. You also can enter a non-inventoried item.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter the quantity shipped.

>   *The In-Transit Lot Number Entry window or the In-Transit Serial Number
>   Entry window opens if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window opens if an item
>   that isn’t tracked by lot or serial numbers requires that you enter bin
>   information.*

>   If you’re using multiple bins and you change the quantity shipped or the
>   unit of measure after selecting bins for an item, you might have to modify
>   the bin information.

1.  You can change the site ID to receive line items to a location other than
    the location specified on the in-transit transfer, if the Change Site ID in
    Receiving option is marked in Purchase Order Processing Setup window.
    Changing the site on the receipt will not change the site on the in-transit
    transfer.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The In-Transit
>   Lot Number Entry window or the In-Transit Serial Number Entry window will
>   open for you to assign lot numbers or serial numbers. You can change the
>   bin.

1.  If you are using landed costs, choose Landed Cost to open the Receivings
    Landed Cost Apportionment window, where you can add landed costs to all line
    items on a receipt. See *Entering landed costs for a shipment receipt* for
    more information. If you want to enter landed costs for an item, see
    *Entering landed costs for a shipment item*.

2.  Choose the Attachment Management icon to attach documents to the in-transit
    transfer, if applicable.

3.  Choose User-Defined to open the Receivings User-Defined Fields Entry window,
    where you can enter user-defined information for this receipt.

4.  Choose Save or Post. If you post the receipt, one or more posting journals
    and distribution breakdown registers may be printed, depending on the
    options selected in the Posting Setup window.

>   If you’ve entered a batch ID, you can’t post the transaction individually;
>   you must use batch posting, series posting, or master posting. For more
>   information, see *Chapter 12, “Receipt batches.”*

#### Using the Select In-Transit Items window

>   Use the Select In-Transit Items window to receive line items on in-transit
>   transfer transactions. In the Select In-Transit Items window, the tree view
>   and the Sort By option control the information that is displayed. When you
>   change the focus in the tree view, or when you choose a different sorting
>   option, the information in the window is refreshed.

>   The scrolling window shows detail about the object selected in the tree
>   view. When you highlight a different object in the tree view, such as an
>   in-transit item or a site, only the information about that object is
>   displayed in the scrolling window. To display all information for an
>   in-transit transfer, you must select the in-transit transfer in the tree
>   view.

>   The sorting option you select determines the order in which objects appear
>   in the tree view and the scrolling window. You can sort objects in four
>   ways:

>   **Transfer/Items** Objects in the tree view and scrolling window are sorted
>   first by transfer number, then by the order items were entered on the
>   transfers.

![](media/887e7a0ab890b3c349e50cb6783bfdf3.jpg)

>   **Item Number/Transfer** Objects in the tree view and scrolling window are
>   sorted first by item number, then by transfer number under each item.

![](media/ad7e8b012b19b186a3a720fddee7549a.jpg)

>   **Site/Transfer/Item Number** Objects in the tree view and scrolling window
>   are sorted first by site, then by transfer number under each site, then by
>   item number under each transfer.

![](media/d5e77c9685a928a5626378cdeb2ba9ae.jpg)

>   **Site/Item Number/Transfer** Objects in the tree view and scrolling window
>   are sorted first by site, then by item number under each site, then by
>   transfer number under each item.

![](media/85d141806c59f5e38341248814dae3a6.jpg)

#### Receiving items from in-transit transfers

>   Use the Select In-Transit Items window to receive line items on multiple
>   in-transit transfers. In-transit transfers that have one or more items with
>   a quantity remaining to receive will be displayed. See *Entering an
>   in-transit inventory receipt* for more information.

>   **To receive items from an in-transit transfer:**

1.  In the navigation pane, choose the Inventory button, and then choose the
    InTransit Transfers list.

2.  Mark the in-transit transfers you want to receive against.

3.  In the Actions group, choose Receive Items.

4.  The Select In-Transit Items window and the Receivings Transaction Entry
    window will open.

>   In the Select In-Transit Items window, in-transit transfers that have one or
>   more items with a quantity remaining to receive will be displayed. Each item
>   on the in-transit transfer that is available to be received in the scrolling
>   window is marked.

![](media/fd3ab10b78ae6510b13a39eb467e7294.jpg)

1.  Select a sorting option.

2.  Mark the check boxes next to the items you want to receive. To select all
    items displayed in the scrolling window, choose Mark All.

>   *When you choose Mark All or Unmark All in the Select In-Transit Items
>   window, only items displayed in the scrolling window will be marked or
>   unmarked. For example, if an in-transit transfer is selected in the tree
>   view, only items from that in-transit transfer will be displayed in the
>   scrolling window, and only those items will be marked when you choose Mark
>   All. To mark or unmark all items, the In-Transit Items must be selected in
>   the tree view.*

1.  Select whether to display all items or only items marked to receive.

2.  Edit Quantity Shipped, if necessary. You can’t enter a quantity shipped that
    is greater than the quantity remaining to be received. If you edit an item
    in the scrolling window, it will be marked to receive.

3.  Choose the Receive button to add the items to your receipt. The Select
    In-Transit Items window will close, and the items will appear in the
    Receivings Transaction Entry window.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Receivings Transaction Entry window, save or post the receipt.

**Chapter 14: Shipment receipt entry for projects**

>   If you are using Project Accounting, you can enter a shipment receipt to
>   record shipments received for purchase orders entered for projects. You can
>   enter shipment receipts and shipment/invoice receipts in Purchase Order
>   Processing. Enter a shipment/invoice receipt to record the receipt of goods
>   and services accompanied by an invoice. Enter a shipment receipt to record
>   the receipt of goods and services without an invoice. You can enter receipt
>   transactions in a batch or enter and post them individually. Receipts can’t
>   be saved unless they’re in a batch.

>   To enter a shipment/invoice receipt or a shipment receipt for a blanket
>   purchase order, refer to *Chapter 13, “Shipment and in-transit inventory
>   receipt entry.”*

>   This information is divided into the following sections:

-   *Receiving a shipment/invoice for projects*

-   *Receiving a shipment for projects*

-   *Receiving project items without a purchase order*

-   *Receiving items for projects using the Select Purchase Order window*

-   *Receiving items for projects from multiple purchase orders*

-   *Receiving items for projects from a purchase order*

#### Receiving a shipment/invoice for projects

>   Use the Receivings Transaction Entry window to record a shipment/invoice if
>   you’ve received an invoice and merchandise at the same time. The inventory
>   quantity on hand will be updated for the items received and the vendor’s
>   account will be increased. You can include items from multiple purchase
>   orders (from a single vendor) on a shipment/invoice receipt. To enter a
>   shipment/invoice receipt for a blanket purchase order, refer to *Chapter 13,
>   “Shipment and in-transit inventory receipt entry.”*

>   When you enter a shipment/invoice receipt for a non-inventoried item and
>   then save or post the transaction, the project costs will be updated
>   automatically. For an inventoried item, the actual costs for the item will
>   be updated automatically. You can receive against line items with New,
>   Released, Change Order, or Received statuses.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   You can’t enter a shipment/invoice receipt for a purchase order that is on
>   hold. If a purchase order is placed on hold after its shipment/invoice
>   receipt is saved to a batch, the receipt for that purchase order will not be
>   posted and will remain in the batch.

>   You can use the View \>\> Currency menu option or the currency list button
>   to view currency amounts in the Receivings Transaction Entry window in the
>   originating or functional currency.

>   **To receive a shipment/invoice for projects:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

![](media/70a4793e7ea370612a3c5e8b518201f2.jpg)

1.  Select Shipment/Invoice as the document type for the transaction.

2.  Enter or select the receipt number.

3.  Enter a vendor document number.

4.  Enter the receipt date.

>   *To enter a General Ledger posting date that is different from the
>   transaction date, choose the Date expansion button; the Receivings Date
>   Entry window will open, where you can enter date information.*

>   For multicurrency transactions, the document date determines which exchange
>   rate is used, based on the currency ID and the associated rate type entered
>   for the transaction.

1.  Enter or select a batch ID (optional).

>   In multicurrency transactions, if the batch posting date does not fall on or
>   before the exchange rate’s expiration date, you will receive a message.
>   Choose Yes to open the Batch Entry window and change the batch posting date.
>   If you choose No, you will be able to save but not post the receipt.

>   See *Creating a receipt batch* for more information.

1.  Enter or select a vendor ID.

2.  Enter or select a currency ID. If a currency ID is assigned to the vendor
    you select, it will appear in the Currency ID field. The currency ID
    assigned to the shipment/invoice must match the currency ID of the purchase
    orders being received against.

3.  Enter or select the purchase order number for which you’re receiving a
    shipment/invoice. You can receive items from multiple purchase orders by
    entering or selecting a different purchase order number in a new row. See
    *Receiving items for projects from multiple purchase orders* for more
    information.

>   If the Allow Receiving Without a Purchase Order option is marked in the
>   Purchase Order Processing Setup window, you can leave the PO Number field
>   blank.

>   You can enter a purchase order that hasn’t been printed if the Allow
>   Receiving of Unprinted PO option is marked in the PA Purchase Order
>   Processing Setup Options window.

1.  Enter a project number and cost category ID.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter one or more items using your company’s item number.s You also can
    enter non-inventoried items.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter the quantity shipped.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window will open if an item
>   that isn’t tracked by lot or serial numbers requires you to enter bin
>   information.*

>   If you’re using multiple bins and you change the quantity shipped or the
>   unit of measure after selecting bins for an item, you might have to modify
>   the bin information.

1.  You can edit the unit cost or extended cost, if the Allow Editing of Costs
    in Receiving option is marked in the Purchase Order Processing Setup window.

2.  You can change the site ID to receive line items to a location other than
    the location specified on the purchase order, if the option is marked in
    Purchase Order Processing Setup. Changing the site on the receipt will not
    change the site on the purchase order.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The Purchasing
>   Lot Number Entry window or the Purchasing Serial Number Entry window will
>   open for you to assign lot numbers or serial numbers. You can change the
>   bin.

1.  Enter the quantity invoiced, which is the number of items on the vendor’s
    invoice.

2.  Enter trade discount, freight, miscellaneous, and tax amounts.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   You can't change the Tax amount in the Receivings Transaction Entry window
>   even if your system is set up to allow editing summary-level taxes. If you
>   want to change the tax amounts for a line item, see *Calculating and
>   distributing detail taxes for shipment/ invoice line items*.

1.  Enter or accept the 1099 amount, if applicable.

2.  Enter or accept the payment terms and tax schedule ID.

3.  To enter an amount received, choose the Amount Received expansion button to
    open the PA Receivings Amount Received Entry window. You can enter the
    amount you’re paying by cash, check, or credit card.

4.  Choose the Attachment Management icon to attach documents to the
    shipment/invoice, if applicable.

5.  If you are using landed costs, choose Landed Cost to open the Receivings
    Landed Cost Apportionment Entry window, where you can add landed costs to
    all line items on a receipt. See *Entering landed costs for a shipment
    receipt* for more information. If you want to enter landed costs for an
    item, see *Entering landed costs for a shipment item*.

6.  Choose Distributions to open the Purchasing Distribution Entry window, where
    you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account in the scrolling window, select the row containing
        the account and choose Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions for a landed cost won’t be
>   displayed in the Purchasing Distribution Entry window. To view landed cost
>   distributions, print the Receivings Edit List.

>   See *Distributing transaction amounts for shipment receipts* for more
>   information.

1.  Choose User-Defined to open the Receivings User-Defined Fields Entry window,
    where you can enter user-defined information for this receipt.

2.  Choose Save or Post. If you post the receipt, one or more posting journals
    and distribution breakdown registers may be printed, depending on the
    options selected in the Posting Setup window.

>   If you’ve entered a batch ID, you can’t post the transaction individually;
>   you must use batch posting, series posting, or master posting. For more
>   information, see *Chapter 12, “Receipt batches.”*

#### Receiving a shipment for projects

>   Use the Receivings Transaction Entry window to record a shipment if you’ve
>   received merchandise but haven’t received the invoice for the merchandise. A
>   shipment receipt will increase the quantity on hand for the items received
>   for sales and discontinued item types. You can include items from multiple
>   purchase orders (from a single vendor) on a shipment receipt. To enter a
>   shipment receipt for a blanket purchase order, refer to *Chapter 13,
>   “Shipment and in-transit inventory receipt entry.”*

>   When you enter a shipment receipt for a non-inventoried item and then save
>   or post the transaction, the project costs will be updated automatically.
>   For an inventoried item, the actual costs for the item will be updated
>   automatically.

>   You can receive against line items with New, Released, Change Order, or
>   Received statuses.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   You can’t enter a shipment receipt for a purchase order that is on hold. If
>   a purchase order is placed on hold after its shipment receipt is saved to a
>   batch, the receipt for that purchase order will not be posted and will
>   remain in the batch.

>   You can use the View \>\> Currency menu option or the currency list button
>   to view amounts in the Receivings Transaction Entry window in originating or
>   functional currency.

>   **To receive a shipment for projects:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

![](media/daa2448273f59301b014b6b7f1d38999.jpg)

1.  Select Shipment as the document type for the transaction.

2.  Enter or select the receipt number.

3.  Enter a vendor document number (optional).

4.  Enter the receipt date.

>   *To enter a General Ledger posting date that is different from the
>   transaction date, choose the Date expansion button; the Receivings Date
>   Entry window will open, where you can enter date information.*

>   For multicurrency transactions, the document date determines which exchange
>   rate is used, based on the currency ID and associated rate type that’s
>   entered for the transaction.

1.  Enter or select a batch ID (optional). See *Creating a receipt batch* for
    more information.

>   In multicurrency transactions, if the batch posting date does not fall on or
>   before the exchange rate’s expiration date, you will receive a message.
>   Choose Yes to open the Batch Entry window and change the batch posting date.
>   If you choose No, you will be able to save but not post the receipt.

1.  Enter or select the vendor ID.

2.  Enter or select a currency ID. If a currency ID is assigned to the vendor
    you select, it will appear in the Currency ID field. The currency ID
    assigned to the invoice must match the currency ID of the purchase order
    being received against.

3.  Enter the purchase order number for which you’re receiving a shipment. You
    can receive items from multiple purchase orders by entering or selecting a
    different purchase order number in a new row. See *Receiving items for
    projects from multiple purchase orders* for more information.

>   If the Allow Receiving Without a Purchase Order option is marked in the
>   Purchase Order Processing Setup window, you can leave the PO Number field
>   blank.

>   You can enter a purchase order that hasn’t been printed if the Allow
>   Receiving of Unprinted PO option is marked in the PA Purchase Order
>   Processing Setup Options window.

1.  Enter a project number and cost category ID.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter one or more items using your company’s item numbers. You also can
    enter non-inventoried items.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  You can change the site ID to receive line items to a location other than
    the location specified on the purchase order, if the option is marked in
    Purchase Order Processing Setup. Changing the site on the receipt will not
    change the site on the purchase order.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The Purchasing
>   Lot Number Entry window or the Purchasing Serial Number Entry window will
>   open for you to assign lot numbers or serial numbers. You can change the
>   bin.

1.  Enter the quantity shipped.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window will open if an item
>   that isn’t tracked by lot or serial numbers requires you to enter bin
>   information.*

>   If you're using multiple bins and you change the quantity shipped or the
>   unit of measure after selecting bins for an item, you might have to modify
>   the bin information.

1.  You can edit the unit cost or extended cost, if the Allow Editing of Costs
    in Receiving option is marked in Purchase Order Processing Setup.

2.  Choose the Attachment Management icon to attach documents to the shipment,
    if applicable.

3.  If you are using landed costs, choose Landed Cost to open the Receivings
    Landed Cost Apportionment Entry window, where you can add landed costs to
    all line items on a receipt. See *Entering landed costs for a shipment
    receipt* for more information. If you want to enter landed costs for an
    item, see *Entering landed costs for a shipment item*.

4.  Choose Distributions to open the Purchasing Distribution Entry window, where
    you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account in the scrolling window, select the row containing
        the account and choose Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions for a landed cost won’t be
>   displayed in the Purchasing Distribution Entry window. To view landed cost
>   distributions, print the Receivings Edit List.

>   See *Distributing transaction amounts for shipment receipts* for more
>   information.

1.  Choose User-Defined to open the Receivings User-Defined Fields Entry window,
    where you can enter user-defined information for this receipt.

2.  Choose Save or Post. If you post the receipt, one or more posting journals
    and distribution breakdown registers may be printed, depending on the
    options selected in the Posting Setup window.

>   If you’ve entered a batch ID, you can’t post the transaction individually;
>   you must use batch posting, series posting, or master posting. For more
>   information, see *Chapter 12, “Receipt batches.”*

#### Receiving project items without a purchase order

>   In the Receivings Transaction Entry window, you have the option to receive
>   items that weren’t included on the original purchase order or receive items
>   without a purchase order.

>   To set up this option, you must select to allow receiving items without a
>   purchase order in the Purchase Order Processing Setup window. You may assign
>   a password that must be entered before entering a line item not assigned to
>   a purchase order.

>   **To receive project items without a purchase order:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select the appropriate document type for the transaction.

2.  Enter the receipt number, vendor document number, date, and vendor ID.

3.  Enter a project number and cost category ID. If the item that you’re
    receiving isn’t assigned to a project because the item isn’t assigned to a
    budget, enter \<NONE\> or leave the Project No. field blank. If there isn’t
    a project number, you can leave the Cost Category field blank. If the item
    is assigned to a project, you must enter a cost category.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display vendor items.

1.  To add items that weren’t included on the original purchase order, leave the
    PO number field blank. You don’t have to enter a purchase order if you’ve
    set up the system to allow receiving items without a purchase order.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget. You cannot add a new
>   inventoried item if the Allow Entry of New Budgets/Materials option is not
>   marked in the User Purchase Order Settings window. See *Inventoried items
>   and non-inventoried items for projects* for more information.

1.  Continue entering the receipt.

>   You must enter the unit cost of non-inventoried items.

1.  In the Receivings Transaction Entry window, save or post the transaction.

#### Receiving items for projects using the Select Purchase Order window

>   Use the Select Purchase Order window to select a purchase order to quickly
>   enter line items on a shipment or shipment/invoice. See *Receiving a
>   shipment for projects* or *Receiving a shipment/invoice for projects* for
>   more information. To receive items on a blanket purchase order, refer to
>   *Chapter 13, “Shipment and intransit inventory receipt entry.”*

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   **To receive items for projects using the Select Purchase Order window:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select the appropriate document type for the transaction.

2.  Enter the receipt number, vendor document number, and date. (A vendor
    document number is required for a shipment/invoice.)

3.  Choose Auto-Rcv to automatically receive items. The Select Purchase Order
    window will open.

>   *If you entered a vendor ID, the Select Purchase Order Items window will
>   open instead of the Select Purchase Order window.*

![](media/52b30e91b168f623ad32138cfd2cc98e.jpg)

1.  Enter or select a purchase order for which you want to receive line items.

2.  Choose Receive All in the Select Purchase Order window to automatically
    receive all items on the selected purchase order.

>   If you choose to view details in the Select Purchase Order window, the
>   Select Purchase Order Items window will open, and the purchase order line
>   items will be marked to receive. Choose Receive to automatically receive
>   items on the selected purchase order.

1.  In the Receivings Transaction Entry window, continue entering receipt
    information, if necessary, and save or post the transaction.

#### Receiving items for projects from multiple purchase orders

>   Use the Select Purchase Order Items window to receive line items for
>   projects on multiple purchase orders. New, Released, or Change Order
>   purchase orders that have one or more items with a quantity remaining to
>   receive will be displayed. See *Receiving a shipment for projects* or
>   *Receiving a shipment/invoice for projects* for more information.

>   To receive items from multiple blanket purchase orders, refer to *Chapter
>   13, “Shipment and in-transit inventory receipt entry.”*

>   If you are using Workflow, the purchase orders must be approved before you
>   can receive against them. You can receive against purchase orders that don’t
>   need approval.

>   **To receive items for projects from multiple purchase orders for
>   projects:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select the appropriate document type for the transaction.

2.  Enter the receipt number, vendor document number, and date. (A vendor
    document number is required for a shipment/invoice.)

3.  Enter or select a vendor ID. The currency ID assigned to the vendor will be
    the default currency ID for the receipt.

4.  Choose the Auto-Rcv button. The Select Purchase Order Items window will
    open.

>   New, Released, or Change Order purchase orders that have one or more items
>   with a quantity remaining to receive will be displayed.

>   If only a Vendor ID is displayed, the selected vendor does not have any New,
>   Released, or Change Order purchase orders with items to receive. Only
>   purchase orders with currency IDs that match the receipt will be displayed.

>   *If you know the purchase order number but not the vendor ID, you can choose
>   AutoRcv without entering a vendor ID. The Select Purchase Order window will
>   open. The vendor and currency ID for the receipt will come from the purchase
>   order you select.*

![](media/d2f7c7cf44a319e048493ab022e9cb63.jpg)

1.  Select a sorting option.

2.  Mark the check boxes next to the items you want to receive. To select all
    items displayed in the scrolling window, choose Mark All.

>   *When you choose Mark All or Unmark All in the Select Purchase Order Items
>   window, only items displayed in the scrolling window will be marked or
>   unmarked. For example, if a purchase order is selected in the tree view,
>   only items from that purchase order will be displayed in the scrolling
>   window, and only those items will be marked when you choose Mark All. To
>   mark or unmark all items for a vendor, the vendor ID must be selected in the
>   tree view.*

1.  Select whether to display all items or only items marked to receive.

2.  Modify the quantity shipped, quantity invoiced (for shipment/invoice
    receipts) and unit cost amounts, if necessary. If you edit an item in the
    scrolling window, it will be marked to receive.

3.  Choose the Receive button to add the items to your receipt. The Select
    Purchase Order Items window will close, and the items will appear in the
    Receivings Transaction Entry window. Taxes are calculated at this time.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Receivings Transaction Entry window, save or post the receipt.

#### Receiving items for projects from a purchase order

>   Use the Select Purchase Order Items window and the Receivings Transaction
>   Entry window to receive items. After you enter or select a standard order
>   with New, Released, or Change Order statuses in the Purchase Order Entry
>   window, you can select to receive items or receive and invoice items. From
>   the Actions button, you can select the Receive the PO Items option from the
>   Actions button to enter a shipment receipt. You can select the Receive and
>   Invoice the PO Items option to enter a shipment/invoice receipt for a
>   purchase order.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

>   For more information about a shipment receipt or a shipment/invoice receipt,
>   see *Receiving a shipment for projects* or *Receiving a shipment/invoice for
>   projects*. For more information about the Select Purchase Order Items
>   window, see *Using the Select Purchase Order Items window*.

>   To receive items from a blanket purchase order, refer to *Chapter 13,
>   “Shipment and in-transit inventory receipt entry.”*

>   **To receive items for projects from a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a standard purchase order that has one or more items with a
    quantity to receive.

2.  Choose Actions, and then select one of the following options.

-   If you are receiving goods and services without an invoice, select Receive
    the PO Items.

-   If you are receiving goods and services accompanied by an invoice, select
    Receive and Invoice the PO Items.

1.  The Select Purchase Order Items window and the Receivings Transaction Entry
    window will open.

>   In the Select Purchase Order Items window, New, Released, or Change Order
>   purchase orders that have one or more items with a quantity remaining to
>   receive will be displayed. The purchase order that you entered in the
>   Purchase Order Entry window will be selected in the tree view. Each item on
>   the purchase order that is available to be received in the scrolling window
>   is marked.

1.  Select a sorting option.

2.  Mark the check boxes next to the items to receive. To select all items
    displayed in the scrolling window, choose Mark All.

>   *When you choose Mark All or Unmark All, only items displayed in the
>   scrolling window will be marked or unmarked. For example, if a purchase
>   order is selected in the tree view, only items from that purchase order will
>   be displayed in the scrolling window, and only those items will be marked
>   when you choose Mark All. To mark or unmark all items for a vendor, the
>   vendor ID must be selected in the tree view.*

1.  Select whether to display all items or only items marked to receive.

2.  Modify the quantity shipped, quantity invoiced (for shipment/invoice
    receipts) and unit cost amounts, if necessary. If you modify an item in the
    scrolling window, it will be marked to receive.

3.  Choose Receive to add the items to your receipt. The Select Purchase Order
    Items window will close, and the items will appear in the Receivings
    Transaction Entry window. Taxes are calculated at this time.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Receivings Transaction Entry window, continue entering receipt
    information, if necessary, and save or post the transaction. For a shipment/
    invoice, you must enter the vendor document number.

**Chapter 15: Shipment receipt detail entry**

>   The Receivings Transaction Entry window is designed to resemble a physical
>   shipment document and includes vendor, line item, and total information. Use
>   the expansion buttons in the Receivings Transaction Entry window to open
>   windows where you can enter detailed information about a line item, lot
>   number, serial number mask, or other elements of a transaction.

>   This information is divided into the following sections:

-   *Entering detail information for a purchasing receipt*

-   *Entering detail information for an in-transit inventory receipt*

-   *Entering project item detail information for a purchasing receipt*

-   *Defining a lot number mask*

-   *Generating lot numbers automatically for a shipment or shipment/invoice
    receipt*

-   *Entering lot numbers manually for a shipment or shipment/invoice receipt*

-   *Entering lot numbers for an in-transit inventory receipt*

-   *Removing lot numbers from a shipment or shipment/invoice receipt*

-   *Defining a serial number mask*

-   *Generating serial numbers automatically for a shipment or shipment/invoice
    receipt*

-   *Entering serial numbers manually for shipment or shipment/invoice receipt*

-   *Entering serial numbers for an in-transit inventory receipt*

-   *Removing serial numbers from a shipment or shipment/invoice receipt*

-   *Multiple bins in Purchase Order Processing*

-   *Changing bins for a receipt*

-   *Merging trade discount and purchase distributions*

-   *Distributing transaction amounts for shipment receipts*

-   *Entering Intrastat trade statistics*

#### Entering detail information for a purchasing receipt

>   Use the Receivings Item Detail Entry window to add or modify line item
>   information such as rejected quantities, or to change a line item’s posting
>   accounts. If you select an item in the Receivings Transaction Entry window
>   before opening this window, information for that item will be displayed.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Receivings Item Detail Entry
>   window, but you can’t enter project information for blanket purchase order
>   line items. To enter additional information for a line item assigned to a
>   project, see *Entering project item detail information for a purchasing
>   receipt*.

>   **To enter detail information for a purchasing receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a receipt number and vendor and open the Receivings Item
    Detail Entry window by choosing the Vendor Item or Item expansion button.

![](media/165062f416a158c8029bef9d40b25661.jpg)

>   Currency amounts in this window may be displayed in the functional or
>   originating currency, depending on the view selected in the Receivings
>   Transaction Entry window.

1.  Enter the purchase order number for which you’re receiving a shipment. You
    can receive items from multiple purchase orders by entering or selecting a
    different purchase order number in a new row. See *Receiving items from
    multiple purchase orders* for more information.

>   If the Allow Receiving Without a Purchase Order option is marked in Purchase
>   Order Processing Setup, you can leave the PO Number field blank.

>   If you are using Workflow, the purchase order must be approved before you
>   can receive against the purchase order. You can receive against purchase
>   orders that don’t need approval.

1.  If you are entering an item for a project, assign a project number and cost
    category ID.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter or select the number of the vendor item or item you’re receiving. You
    also can enter a non-inventoried item.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget. See *Inventoried items and
>   non-inventoried items for projects* for more information.

1.  Enter the quantity shipped.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window will open if an item
>   that isn’t tracked by lot or serial numbers requires you to enter bin
>   information. You can't assign serial or lot numbers to a non-inventoried
>   item.*

>   An icon will be displayed in the Qty Shipped field for purchase order line
>   items with sales commitments. Select a line item and choose the button next
>   to the Qty Shipped heading to view or prioritize commitments in the Sales

>   Commitments for Purchase Order window. For more information, see

>   *Committing purchase orders to sales documents*. If you are using Project
>   Accounting, you can’t commit purchase order line items for projects to Sales
>   Order Processing line items.

>   If you're using multiple bins and you change the quantity shipped or the
>   unit of measure after selecting bins for an item, you might have to modify
>   the bin information.

1.  If you want to enter landed costs for an item, choose the Unit Cost
    expansion button to open the Receivings Landed Cost Entry window. See
    *Entering landed costs for a shipment item* for more information.

2.  You can change the site ID to receive line items to a location other than
    the location specified on the purchase order, if the option is marked in
    Purchase Order Processing Setup. Changing the site on the receipt will not
    change the site on the purchase order.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The Purchasing
>   Lot Number Entry window or the Purchasing Serial Number Entry window will
>   open for you to assign lot numbers or serial numbers. You can change the
>   bin.

>   If you’re using landed costs and change the site ID, the landed cost group
>   ID will change to the landed cost group ID assigned to the item at the new
>   site. You can specify a landed cost group for each item-site combination in
>   the Item Quantities Maintenance window.

1.  Enter the quantity invoiced, which is the number of items on the vendor’s
    invoice.

2.  The default accounts for posting the receipt and for posting purchase price
    variances will be displayed. If no accounts are displayed, you can enter
    them.

>   Default accounts come from the purchase order. If you’re receiving without a
>   purchase order, the default accounts will come from the item. If there are
>   no accounts associated with an inventoried item, the accounts will come from
>   Posting Accounts Setup. If there are no accounts associated with a
>   noninventoried item, the accounts will come from the vendor or Posting
>   Accounts Setup.

1.  Enter the quantity rejected, if any, and a rejected comment ID. You also can
    enter a comment explaining the reason for rejecting the goods. For more
    information about comments, see *Adding comments to purchasing documents*.

>   *Rejecting an item assumes that the vendor will be replacing the goods. If
>   the goods won’t be replaced, you should enter a quantity canceled instead.*

1.  In the BOL/Pro No. field, enter the bill of lading or progressive number
    assigned to the shipment by the carrier.

2.  If you are using landed costs, enter a landed cost group ID or accept the
    default ID.

3.  Enter or accept the item tax option and the tax schedule IDs. The tax
    information is available only for shipment/invoices.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   If you want to change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for shipment/invoice receipts*. If you want to
>   change the tax amounts for a line item, see *Calculating and distributing
>   detail taxes for shipment/invoice line items*.

1.  Enter the actual date the vendor shipped the order (optional).

2.  Choose Save to save the item information.

#### Entering detail information for an in-transit inventory receipt

>   Use the Receivings Item Detail Entry window to modify line item information
>   such as rejected quantities, or to change a line item’s posting account. If
>   you select an item in the Receivings Transaction Entry window before opening
>   this window, information for that item will be displayed.

>   **To enter detail information for an in-transit inventory receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a receipt number and open the Receivings Item Detail Entry
    window by choosing the Item expansion button.

2.  Enter the transfer number for which you’re entering a receipt. You can
    receive items from multiple in-transit transfers by entering or selecting a
    different transfer number in a new row.

3.  Enter or select the number of the item.

4.  Enter the quantity shipped.

>   *The In-Transit Lot Number Entry window or the In-Transit Serial Number
>   Entry window opens if the item requires that you assign lot or serial
>   numbers. If you are using multiple bins, you also can enter a bin number for
>   the serial or lot number. The Bin Quantity Entry window opens if an item
>   that isn’t tracked by lot or serial numbers requires you to enter bin
>   information.*

>   If you’re using multiple bins and you change the quantity shipped after
>   selecting bins for an item, you might have to modify the bin information.

1.  If you want to enter landed costs for an item, choose the Unit Cost
    expansion button to open the Receivings Landed Cost Entry window. See
    *Entering landed costs for a shipment item* for more information.

2.  You can change the site ID to receive line items to a location other than
    the location specified on the purchase order, if the Change Site ID in
    Receiving option is marked in Purchase Order Processing Setup window.
    Changing the site on the receipt will not change the site on the in-transit
    transfer.

>   If you are using multiple bins and you change the site ID, the default
>   purchase receipts bin assigned to the new site ID will replace your previous
>   bin selections. If the item is tracked by serial or lot numbers, your
>   previous lot number or serial number selections are removed. The In-Transit
>   Lot Number Entry window or the In-Transit Serial Number Entry window opens
>   for you to assign lot numbers or serial numbers. You can change the bin.

>   If you’re using landed costs and change the site ID, the landed cost group
>   ID changes to the landed cost group ID assigned to the item at the new site.
>   You can specify a landed cost group for each item-site combination in the
>   Item Quantities Maintenance window.

1.  The default account for posting the receipt is displayed. If no account is
    displayed, you can enter it.

>   The inventory account assigned to the item in the Item Account Maintenance
>   window is the default posting account. If you didn’t enter posting accounts
>   in the Item Account Maintenance window, the inventory account entered in the
>   Posting Setup window is used as the default entry.

1.  Enter the quantity rejected, if any, and a rejected comment ID. You also can
    enter a comment explaining the reason for rejecting the goods. For more
    information about comments, see *Adding comments to purchasing documents*.

>   *Rejecting an item assumes that the item will be replaced. If the item won’t
>   be replaced, you should enter a quantity canceled instead.*

1.  In the BOL/Pro No. field, enter the bill of lading or progressive number
    assigned to the shipment by the carrier.

2.  If you are using landed costs, enter a landed cost group ID or accept the
    default ID.

3.  Enter the actual date the vendor shipped the order (optional).

4.  Choose Save to save the item information.

#### Entering project item detail information for a purchasing receipt

>   You can use the PA Receivings Item Detail Entry window to add a billing note
>   or modify the billing type. If the item is for a time and materials project,
>   you can enter a billing rate or a markup percentage and view the accrued
>   revenue.

>   **To enter project item detail information for a purchasing receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a receipt number, vendor ID, project number, cost category,
    and item.

2.  Choose the Cost Category expansion button to open the PA Receivings Item
    Detail Entry window.

![](media/1b161fd2c3aeb51904a759af9f6e66bd.jpg)

1.  Enter or modify a billing note.

2.  Modify the billing type, if applicable. The item must be a non-inventoried
    item to modify the billing type.

3.  If the non-inventoried item is for a time and materials project, you can
    enter a billing rate or markup percentage.

4.  Choose OK to close the window and return to the Receivings Transaction Entry
    window.

#### Defining a lot number mask

>   Use the Item Serial/Lot Number Definition window to set up lot number masks
>   for lot-tracked items. A lot number mask is a pre-defined lot number format
>   used to generate lot numbers automatically. With a lot number mask, you can
>   specify starting and ending lot numbers for an item, create incrementing
>   segments, and control the character type. You must create a lot number mask
>   before you can automatically generate lot numbers in Purchase Order
>   Processing.

>   You also can enter a lot split quantity, which is the breakpoint for
>   creating separate lots for a lot-tracked item. For example, assume that you
>   enter a lot split quantity of 50. If you receive 120 units for a lot
>   -tracked item, two lots of 50 and one lot of 20 are created. If the starting
>   value for the mask is AA-001, the first lot is AA-001, the second lot is
>   AA-002, and the third lot for the remainder is AA-003. If the lot split
>   quantity is zero, the total quantity is treated as a single lot.

>   **To define a lot number mask:**

1.  Open the Item Maintenance window.

>   (Inventory \>\> Cards \>\> Item)

1.  Select an item, then choose Options to open the Item Maintenance Options
    window.

2.  Choose Lot Numbers from the Track drop-down list, then choose the Track
    expansion button to open the Item Serial/Lot Number Definition window.

![](media/34d88e83dca8bbcf180372ebf2d25dd8.jpg)

>   Information for the item you selected, including the last lot number that
>   was generated and any current mask information, will appear.

1.  Enter a lot split quantity, if applicable.

2.  Select a character type for the first segment: Numeric, Alpha, Symbol, User
    Date, or Space. The character type will determine which of the remaining
    fields are editable.

3.  Enter a size, if you selected a character type of Alpha or Numeric.

>   Symbol and Space character types must have a size of 1. The size of a User
>   Date segment depends on the date format you select.

1.  Mark Increment if you want this segment to increase each time a lot number
    is generated. You must have at least one segment marked to increment in
    order to automatically generate lot numbers for an item.

>   You can use the Increment option only if the character type is Alpha or
>   Numeric. Symbol and space characters do not change. User date segments
>   automatically increment when the user date changes.

>   If more than one segment is marked to increment, the segments increment from
>   right to left. For example, assume you have incrementing segments 0001-0001.
>   The next lot number contains the segments 0001-0002. The first segment
>   increments when the second reaches its maximum value (from 0001-9999 to
>   0002-0000). If the mask contains a date segment, other incrementing segments
>   will reset when the date segment increments.

1.  Enter starting and ending values.

>   If you selected a type of User Date or Space, you won’t be able to set
>   starting and ending values. If you selected a type of Symbol, you will be
>   able to enter a single character in the starting value field.

1.  If you selected a character type of User Date, select a date format.

2.  Choose the Insert button to add the segment to the lot number mask. The
    segment’s starting value appears in the Lot Number Mask field.

3.  Define and insert the remaining segments. lot number masks can be a maximum
    of 20 characters long.

4.  To move a segment to a different position in the lot number mask, select the
    segment, then choose Up or Down.

>   Choose Remove to delete the selected segment or choose Modify to change the
>   selected segment’s information.

#### Generating lot numbers automatically for a shipment or shipment/invoice receipt

>   Use the Purchasing Lot Number Entry window to assign lot numbers for
>   lottracked line items. You can assign lot numbers automatically, manually,
>   or a combination of the two. In order to automatically generate lot numbers,
>   you must first set up the item and its lot number mask. For more
>   information, see *Defining a lot number mask*.

>   If you’re using multiple bins and are generating lot numbers automatically,
>   the bin number entered in the Purchasing Lot Number Entry window will be
>   used with each generated lot number.

>   **To generate lot numbers automatically for a shipment or shipment/invoice
>   receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice that includes at least one
    lotnumbered item.

2.  Enter the quantity shipped for the line items that contain a lot number.

3.  Enter a site ID. Press TAB or choose the Quantity Shipped expansion button
    to open the Purchasing Lot Number Entry window. (This window will
    automatically open when you choose the Auto-Rcv button in the Receivings
    Transaction Entry window and lot-numbered items are entered for the
    receipt.)

![](media/167dc441a17647f18e31ffd527bfbab1.jpg)

1.  If you are using multiple bins, enter a bin number or accept the default bin
    number.

>   *To set up a lot number mask for the item, click the Lot Number Mask link in
>   the Purchasing Lot Number Entry window to open the Item Serial/Lot Number
>   Definition window.*

1.  Enter the lot(s) to generate (optional). The default lot(s) to generate is
    the Remaining to Select quantity divided by the Lot Split Quantity rounded
    to the next whole number.

2.  Edit the starting lot number, if necessary.

>   If you modify the starting lot number, it must conform to the lot number
>   mask. If you delete the starting lot number, you will not be able to
>   automatically generate lot numbers for the item.

1.  Choose Auto-Generate. Lot numbers for the items are inserted in the
    scrolling window. Numbers that already exist will be skipped.

>   The Total Quantity Selected must equal the item’s extended quantity before
>   you can move to the next line item in the Receivings Transaction Entry
>   window or the Receivings Item Detail Entry window.

1.  Choose OK to save the lot numbers that were automatically generated.

#### Entering lot numbers manually for a shipment or shipment/invoice receipt

>   Use the Purchasing Lot Number Entry window to assign lot numbers for
>   shipment or shipment/invoice receipt line items.

>   **To enter lot numbers manually for a shipment or shipment/invoice
>   receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice that includes a lot-numbered
    item.

2.  Enter the quantity shipped on the line item containing a lot number.

3.  Enter a site ID. Press TAB or choose the Quantity Shipped expansion button
    to open the Purchasing Lot Number Entry window. (This window will
    automatically open when you choose the Auto-Rcv button in the Receivings
    Transaction Entry window and lot-numbered items are entered for the
    receipt.)

4.  If you are using multiple bins, enter a bin number or accept the default bin
    number.

5.  Enter a lot number and a quantity selected.

6.  Choose Insert to add the lot number to the scrolling window.

7.  To assign values to the lot attributes for the item, choose the Lot
    expansion button to open the Lot Attribute Entry window.

>   If you are using sales workflow and are tracking the minimum shelf life for
>   the lot item, the dates that you enter in this window and the number of days
>   entered in the Item Maintenance Options window are used to determine whether
>   or not the item meets the minimum shelf life when you receive the item. If
>   you are using Project Accounting, you can’t use sales workflow with project
>   items.

1.  Continue entering lot numbers for the item. The Total Quantity Selected must
    equal the item’s extended quantity before you can move to the next line item
    in the Receivings Transaction Entry window or the Receivings Item Detail
    Entry window.

2.  Choose OK to save the lot numbers you’ve added.

#### Entering lot numbers for an in-transit inventory receipt

>   Use the In-Transit Lot Number Entry window to assign lot numbers for
>   in-transit inventory receipt line items.

>   **To enter lot numbers for an in-transit inventory receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select an in-transit inventory receipt that includes a lot-numbered
    item.

2.  Enter the quantity shipped on the line item containing a lot number.

3.  Press TAB or choose the Quantity Shipped expansion button to open the
    InTransit Lot Number Entry window.

![](media/53c017886f8e9641675ca82de99dc8e7.jpg)

1.  If you are using multiple bins, enter a bin number or accept the default bin
    number.

2.  In the Available list, enter a quantity selected for a lot number.

3.  Choose Insert to add the lot number to the Lot Numbers Selected list.

4.  To assign values to the lot attributes for the item, choose the Available
    expansion button or the Lot Numbers Selected expansion button to open the
    Lot Attribute Entry window.

>   If you are using the sales fulfillment workflow and are tracking the minimum
>   shelf life for the lot item, the dates that you enter in this window and the
>   number of days entered in the Item Maintenance Options window are used to
>   determine whether or not the item meets the minimum shelf life when you
>   receive the item.

1.  Continue entering lot numbers for the item. The Quantity Selected must equal
    the item’s extended quantity before you can move to the next line item in
    the Receivings Transaction Entry window or the Receivings Item Detail Entry
    window.

2.  Choose OK to save the lot numbers you’ve added.

#### Removing lot numbers from a shipment or shipment/ invoice receipt

>   Use the Purchasing Lot Number Entry window to remove lot numbers for
>   shipment or shipment/invoice receipt line items.

>   **To remove lot numbers from a shipment or shipment/ invoice receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice that includes a lot-numbered
    item.

2.  Select a line item that contains a lot number.

3.  Choose the Quantity Shipped expansion button to open the Purchasing Lot
    Number Entry window.

4.  Select the lot number from the Lot list and choose Remove. To remove all the
    lot numbers from the Lot list, choose Remove All.

5.  Enter new lot numbers for the item.

6.  Choose OK to save your changes.

#### Defining a serial number mask

>   Use the Item Serial/Lot Number Definition window to set up serial number
>   masks for serial-tracked items. A serial number mask is a pre-defined serial
>   number format used to generate serial numbers automatically. With a serial
>   number mask, you can specify starting and ending serial numbers for an item,
>   create incrementing segments, and control the character type. You must
>   create a serial number mask before you can automatically generate serial
>   numbers in Purchase Order Processing.

>   **To define a serial number mask:**

1.  Open the Item Maintenance window.

>   (Inventory \>\> Cards \>\> Item)

1.  Select an item, then choose Options to open the Item Maintenance Options
    window.

2.  Choose Serial Numbers from the Track drop-down list, then choose the Track
    expansion button to open the Item Serial/Lot Number Definition window.

![](media/aaea078246ebb3e6f908f87e1d9368d5.jpg)

>   Information for the item you selected, including the last serial number that
>   was generated and any current mask information, will appear.

1.  Select a character type for the first segment: Numeric, Alpha, Symbol, User
    Date, or Space. The character type will determine which of the remaining
    fields are editable.

2.  Enter a size, if you selected a character type of Alpha or Numeric.

>   Symbol and Space character types must have a size of 1. The size of a User
>   Date segment depends on the date format you select.

1.  Mark Increment if you want this segment to increase each time a serial
    number is generated. You must have at least one segment marked to increment
    in order to automatically generate serial numbers for an item.

>   You can use the Increment option only if the character type is Alpha or
>   Numeric. Symbol and space characters do not change. User date segments
>   automatically increment when the user date changes.

>   If more than one segment is marked to increment, the segments increment from
>   right to left. For example, assume you have incrementing segments 0001-0001.
>   The next serial number contains the segments 0001-0002. The first segment
>   increments when the second reaches its maximum value (from 0001-9999 to
>   0002-0000). If the mask contains a date segment, other incrementing segments
>   will reset when the date segment increments.

1.  Enter starting and ending values.

>   If you selected a type of User Date or Space, you won’t be able to set
>   starting and ending values. If you selected a type of Symbol, you will be
>   able to enter a single character in the starting value field.

1.  If you selected a character type of User Date, select a date format.

2.  Choose the Insert button to add the segment to the serial number mask. The
    segment’s starting value appears in the Serial Number Mask field.

3.  Define and insert the remaining segments. Serial number masks can be a
    maximum of 20 characters long.

4.  To move a segment to a different position in the serial number mask, select
    the segment, then choose Up or Down.

>   Choose Remove to delete the selected segment or choose Modify to change the
>   selected segment’s information.

#### Generating serial numbers automatically for a shipment or shipment/invoice receipt

>   Use the Purchasing Serial Number Entry window to assign serial numbers for
>   serial-tracked line items. You can assign serial numbers automatically,
>   manually, or a combination of the two. In order to automatically generate
>   serial numbers, you must first set up the item and its serial number mask.
>   For more information, see *Defining a serial number mask*.

>   If you’re using multiple bins and are generating serial numbers
>   automatically, the bin number entered in the Purchasing Serial Number Entry
>   window will be used with each generated serial number.

>   **To generate serial numbers automatically for a shipment or
>   shipment/invoice receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice that includes at least one
    serialnumbered item.

2.  Enter the quantity shipped for the line items that contain a serial number.

3.  Enter a site ID. Press TAB or choose the Qty Shipped expansion button to
    open the Purchasing Serial Number Entry window. (This window automatically
    opens when you choose the Auto-Rcv. button in the Receivings Transaction
    Entry window and serial-numbered items are entered for the receipt.)

![](media/039ce7beb4b0826eb3028a60043c2063.jpg)

1.  If you are using multiple bins, enter a bin number or accept the default bin
    number.

>   *To set up a serial number mask for the item, click the Serial Number Mask
>   link in the Purchasing Serial Number Entry window to open the Item
>   Serial/Lot Number Definition window.*

1.  Enter the Quantity to Generate (optional). The default Quantity to Generate
    is the Remaining to Select quantity.

2.  Edit the starting serial number, if necessary.

>   If you modify the starting serial number, it must conform to the serial
>   number mask. If you delete the starting serial number, you will not be able
>   to automatically generate serial numbers for the item.

1.  Choose Auto-Generate. Serial numbers for the items are inserted in the
    scrolling window. Numbers that already exist will be skipped.

>   The number of serial numbers must equal the item’s extended quantity before
>   you can return to the Receivings Transaction Entry window or the Receivings
>   Item Detail Entry window.

1.  Choose OK to save the serial numbers that were automatically generated.

#### Entering serial numbers manually for shipment or shipment/invoice receipt

>   Use the Purchasing Serial Number Entry window to assign serial numbers
>   manually for shipment or shipment/invoice receipt line items.

>   **To enter serial numbers manually for shipment or shipment/invoice
>   receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice that includes at least one
    serialnumbered item.

2.  Enter the quantity shipped for the line items that contain a serial number.

3.  Enter a site ID. Press TAB or choose the Quantity Shipped expansion button
    to open the Purchasing Serial Number Entry window.

>   (This window automatically opens when you choose the Auto-Rcv. button in the
>   Receivings Transaction Entry window and serial-numbered items are entered
>   for the receipt.)

1.  If you are using multiple bins, enter a default bin number or accept the
    default bin number.

2.  Enter a serial number.

3.  Choose Insert to add the serial number to the scrolling window.

4.  Continue entering serial numbers for the item.

>   The number of serial numbers entered must equal the item’s extended quantity
>   before you can move to the next line item in the Receivings Transaction
>   Entry window or the Receivings Item Detail Entry window.

1.  Choose OK to save the serial numbers you’ve added.

#### Entering serial numbers for an in-transit inventory receipt

>   Use the In-Transit Serial Number Entry window to assign serial numbers for
>   intransit inventory receipt line items.

>   **To enter serial numbers for an in-transit inventory receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select an in-transit inventory receipt that includes at least one
    serialnumbered item.

2.  Enter the quantity shipped for the line items that contain a serial number.

3.  Press TAB or choose the Qty Shipped expansion button to open the In-Transit
    Serial Number Entry window.

![](media/fbae38929c4aba796f115617f4b2bade.jpg)

1.  If you are using multiple bins, enter a default bin number or accept the
    default bin number.

2.  Select an available serial number and choose Insert to add the serial number
    to the Selected scrolling window.

3.  Continue entering serial numbers for the item.

>   The number of serial numbers entered must equal the item’s extended quantity
>   before you can move to the next line item in the Receivings Transaction
>   Entry window or the Receivings Item Detail Entry window.

1.  Choose OK to save the serial numbers you’ve added.

#### Removing serial numbers from a shipment or shipment/invoice receipt

>   Use the Purchasing Serial Number Entry window to remove serial numbers for
>   shipment or shipment/invoice receipt line items. Whether you have
>   auto-generated or manually entered serial numbers, you can always choose to
>   remove an incorrect number from the scrolling window, correct or modify it
>   and reinsert it. You cannot modify serial numbers once they are saved.

>   **To remove serial numbers from a shipment or shipment/ invoice receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice that includes a
    serial-numbered item.

2.  Select a line item that contains a serial number.

3.  From the Quantity Shipped column, choose the Quantity Shipped expansion
    button to open the Purchasing Serial Number Entry window.

4.  Select the serial number from the serial number selected list and choose
    Remove. To remove all the serial numbers from the serial number selected
    list, choose Remove All.

5.  Enter new serial numbers for the item. The number of serial numbers entered
    must equal the item’s extended quantity before you can move to the next line
    item in the Receivings Transaction Entry window or the Receivings Item
    Detail Entry window.

6.  Choose OK to save your changes.

#### Multiple bins in Purchase Order Processing

>   Use multiple bins to add another level of detail to item quantity tracking.
>   Besides tracking items within inventory sites, with multiple bins you can
>   track item quantities in bins that reside within each site. Bin quantities
>   are processed and displayed in the item’s base unit of measure.

>   *You can set up bin information when multiple bins functionality has been
>   installed and registered. However, you must also enable this feature in
>   Inventory Control before you can use bins to track items. For more
>   information about enabling multiple bins, see the Inventory Control
>   documentation.*

>   Default bins for transaction types at each site can be identified for use in
>   transactions. For example, a default bin could be created for purchasing
>   transactions at your warehouse site. Default bins can also be identified for
>   a particular item and transaction type at a site. If you always use Bin A
>   when purchasing a certain item from your main site, for example, you can set
>   up Bin A as the default purchase receipts bin for the item at the main site.
>   Microsoft Dynamics GP automatically creates item-site-bin relationships the
>   first time a bin is used for a transaction.

>   When you enter a transaction, the default bin for the transaction type at
>   the itemsite or the site is used automatically. If there isn’t a default bin
>   at the item-site or at the site, you will be required to enter a bin. If the
>   site’s default bin is used, an itemsite-bin record is created automatically.
>   If you delete the line or document after the item-site-bin record is
>   automatically created, that item-site-bin record is not deleted. The on-hand
>   quantity of the item increases at the bin within the site when you post a
>   shipment or shipment/invoice.

>   For more information about setting up and using multiple bins, see the
>   Inventory Control documentation.

#### Changing bins for a receipt

>   If you’re using multiple bins, use the Bin Quantity Entry window to verify
>   or change bin allocations for items that are not tracked by serial or lot
>   numbers.

>   For items that are tracked by serial or lot numbers, you can verify or
>   change bins in the Purchasing Serial Number Entry window or the Purchasing
>   Lot Number Entry window for shipment receipts and shipment/invoice receipts.
>   You can use the InTransit Serial Number Entry window or the In-Transit Lot
>   Number Entry window to verify or change bins for items that tracked serials
>   or lot numbers for in-transit inventory receipt.

>   You can distribute a line item quantity to multiple bins. For example, if
>   the quantity shipped is 20, you can receive 15 items into Bin 1, and five
>   into Bin 2 at site A. You might need to change bin selections manually if
>   you change quantities, the unit of measure, or the site after you already
>   selected bins.

>   **To change bins for a receipt item that isn’t tracked by serial or lot
>   numbers:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment receipt, a shipment/invoice receipt, or an
    in-transit inventory receipt.

2.  Select an item that isn’t tracked by serial or lot numbers and choose the
    Qty Shipped expansion button to open the Bin Quantity Entry window.

>   You also can select an item that isn’t tracked by serial or lot numbers and
>   choose the item expansion button to open the Receivings Item Detail Entry
>   window. Choose Bins.

1.  Select the bin to change and choose Remove.

2.  Select a bin to use from the list of available bins. You also can enter a
    new bin.

3.  Enter a quantity for the bin.

4.  Choose Insert.

5.  Choose OK to save your changes and close the window.

6.  In the Receivings Item Detail Entry window or the Receivings Transaction
    Entry window and choose Save and close the window.

>   **To change bins for a shipment receipt item that is tracked by serial or
>   lot numbers:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice.

2.  Select an item that is tracked by serial or lot numbers and choose the Qty
    Shipped expansion button to open the Purchasing Serial Number Entry window
    or Purchasing Lot Number Entry window.

>   You also can select an item that is tracked by serial or lot numbers and
>   choose the item expansion button to open the Purchasing Item Detail Entry
>   window. Choose Serial/Lot.

1.  Select the serial number or lot number to change and choose Remove.

2.  For an item that is tracked by serial numbers, select a bin number and
    serial number. You can select a bin to use from the list of available bins.
    You also can enter a new bin.

3.  For an item that is tracked by lot numbers, enter a lot number, a quantity,
    and select a bin number. You can select a bin to use from the list of
    available bins. You also can enter a new bin.

4.  Choose Insert.

5.  Choose OK to save your changes and close the window.

6.  In the Receivings Item Detail Entry window or the Receivings Transaction
    Entry window and choose Save and close the window.

>   **To change bins for an in-transit inventory receipt item that is tracked by
>   serial or lot numbers:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select an in-transit inventory receipt.

2.  Select an item that is tracked by serial or lot numbers and choose the Qty
    Shipped expansion button to open the In-Transit Serial Number Entry window
    or In-Transit Lot Number Entry window.

>   You also can select an item that is tracked by serial or lot numbers and
>   choose the item expansion button to open the Purchasing Item Detail Entry
>   window. Choose Serial/Lot.

1.  Select the serial number or lot number to change and choose Remove.

2.  For an item that is tracked by serial numbers, select a to bin number and
    serial number. You also can enter a new bin.

3.  For an item that is tracked by lot numbers, select a to bin and enter a
    quantity selected. You also can enter a new bin.

4.  Choose Insert.

5.  Choose OK to save your changes and close the In-Transit Serial Number Entry
    window or In-Transit Lot Number Entry window.

6.  Choose Save and close the Receivings Item Detail Entry window or the
    Receivings Transaction Entry window.

#### Merging trade discount and purchase distributions

>   If you’ve marked the Merge Trade Discount Distributions in Purchasing option
>   in the Company Setup Options window, the trade discount distributions will
>   be merged with the purchases distribution for shipment/invoice receipts. If
>   you are using Project Accounting, the trade discount distributions won’t be
>   merged with the purchases distributions for shipment/invoice receipts.

>   For example, assume that you’ve entered a purchase transaction of \$100.00
>   with a trade discount of \$15.00. If you’ve marked the Merge Trade Discount
>   Distributions in Purchasing option, the trade discount distributions will be
>   merged as in the following example.

| **Account**     | **Debit** | **Credit** |
|-----------------|-----------|------------|
| Account A PURCH | \$85      |            |
| Account C PAY   |           | \$85       |

>   If you didn’t mark the Merge Trade Discount Distributions in Purchasing
>   option, the trade discount distributions are separated from the purchase
>   distribution.

| **Account**     | **Debit** | **Credit** |
|-----------------|-----------|------------|
| Account A PURCH | \$100     |            |
| Account B TRADE |           | \$15       |
| Account C PAY   |           | \$85       |

#### Distributing transaction amounts for shipment receipts

>   Use the Purchasing Distribution Entry window to redistribute transaction
>   amounts to posting accounts. Transactions will be distributed automatically
>   to the posting accounts assigned in the Vendor Account Maintenance window or
>   the Item Account Maintenance window. If accounts aren’t assigned to vendor
>   or item records, the accounts assigned in the Posting Accounts Setup window
>   will be used instead.

>   If you are using landed costs, the distributions are calculated for a landed
>   cost but won’t be displayed in the Purchasing Distribution Entry window. To
>   view landed cost distributions, print the Receivings Edit List.

>   Currency amounts in the Purchasing Distribution Entry window are displayed
>   in both the functional and originating currencies.

>   **To distribute transaction amounts for shipment receipts:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment or shipment/invoice.

2.  Choose Distributions to open the Purchasing Distribution Entry window.

![](media/e4a5102c0b56d351a15a39d523f4a617.jpg)

1.  Enter a reference for the receipt, or accept the default. The reference
    entered will be posted to General Ledger.

2.  Change the amounts for the default accounts. To distribute the transaction
    to multiple posting accounts, change the default amount in the scrolling
    window.

3.  In the next available line, enter or select another purchasing distribution
    account, choose the distribution type and enter the next amount.

>   If you want to remove a distribution, select it and choose Edit \>\> Delete
>   Row. If you changed distribution accounts and amounts and decide you want to
>   use the original distributions, choose Default.

1.  Continue entering distribution accounts until your transaction is fully
    distributed.

2.  Enter a distribution reference (optional).

>   This is the reference that will post as the General Ledger distribution
>   reference for the account. If you leave this field blank, the reference
>   information entered in the Reference field will post to General Ledger.

1.  Choose OK to save your entries. Continue entering the transaction. You can
    save the transaction if it’s not fully distributed, but you won’t be able to
    post until the full amount is distributed and debits equal credits.

#### Entering Intrastat trade statistics

>   Use the Purchasing Intrastat Entry window to enter the information required
>   to create the Intrastat Trade Report you submit to your government. You can
>   enter Intrastat statistics for each line item. For information about setting
>   up Intrastat codes, refer to your System Setup instructions (Help \>\>
>   Contents \>\> select Setting Up the System).

>   Intrastat is the system for collecting statistics on the trade of goods
>   between European Union (EU) countries. Intrastat data is required for all
>   items either bought from EU vendors or sold to EU customers, and must be
>   provided on a monthly basis. Requirements for Intrastat are similar in all
>   EU countries. The government uses these statistics as an economic indicator.

>   If Intrastat information was entered for the vendor’s ship from address ID,
>   that information appears in this window. Each time you enter a new line
>   item, the Intrastat statistics from the previous line item will be the
>   default Intrastat entry for the new line item. You can use the Purchasing
>   Intrastat Entry window to change Intrastat information for an individual
>   transaction, or to enter Intrastat information if none was entered for the
>   vendor.

>   *You can enter Intrastat statistics only if you have marked to enable
>   Intrastat tracking in the Company Setup Options window.*

>   **To enter Intrastat trade statistics:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter the shipment/invoice receipt and mark the EU transaction option.

2.  Choose the EU button to open the Purchasing Intrastat Entry window. You can
    also open the Purchasing Intrastat Entry window by choosing the EU button in
    the Receivings Item Detail Entry window.

![](media/6a88ae4220d5eaa9750d2d9c2bf8d2af.jpg)

1.  Enter Intrastat information, or change the default entries, if necessary.

2.  In the Net Unit Mass field, enter the weight of the goods in kilograms or
    accept the default.

3.  Enter the quantity of the goods being purchased.

>   The line mass displays the total mass per item and is calculated
>   automatically when you press TAB on the Quantity field. The line mass total
>   is equal to the amount entered in the Unit Mass field multiplied by the
>   amount entered in the Quantity field.

1.  Enter a supplementary units amount, if applicable. The supplementary units
    amount is simply a second quantity. Supplementary unit amounts are required
    by the EU Combined Nomenclature for certain goods.

2.  In the Traders Reference field, enter a reference code, such as an invoice
    or dispatch number, or any other information that will identify the
    transaction.

3.  Enter a goods value and statistical value, if applicable.

4.  Choose OK to save the record.

184 P U R C H A S E O R D E R P R O C E S S I N G

**Chapter 16: Invoice receipt entry**

>   Enter an invoice receipt to record an invoice received for a shipment
>   receipt entered and posted earlier, or to record an invoice received for a
>   shipment that you have not yet received. You also can enter an invoice for
>   drop-ship purchase order line items and blanket drop-ship purchase order
>   line items. You can enter invoice receipt transactions in a batch or enter
>   and post them individually. Invoice receipts can’t be saved unless they’re
>   in a batch.

>   *If you are using vendor approval workflow, the vendor must have the
>   workflow status of Approved or No Approval Needed before you can post the
>   invoice receipt.*

>   If you are using Project Accounting, see *Chapter 17, “Invoice receipt entry
>   for projects”* to enter invoice receipts for projects.

>   This information is divided into the following sections:

-   *Entering an invoice receipt*

-   *Matching shipments to an invoice receipt*

-   *Invoicing items without a purchase order*

-   *Invoicing items using the Select Purchase Order window*

-   *Using the Select Purchase Order Items window*

-   *Invoicing items from multiple purchase orders*

-   *Invoicing items from a purchase order*

#### Entering an invoice receipt

>   Use the Purchasing Invoice Entry window to enter, save, and post invoice
>   receipts. You can enter detailed information for each invoice. You can
>   include items from multiple purchase orders (from a single vendor) on an
>   invoice receipt. If you are using landed costs, you can enter a landed cost
>   as a line item.

>   If you are using Workflow, a drop-ship purchase order or a drop-ship blanket
>   purchase order must be approved before you can invoice against the purchase
>   order. You can invoice against purchase orders that don’t need approval.

>   You can enter and save, but not post, invoice receipts for purchase orders
>   that are on hold. If an invoice for an on hold purchase order is saved to a
>   batch, the batch can be posted, but the invoice for the on hold purchase
>   order will remain in the batch.

>   If you expect to receive multiple invoices for a single shipment, we
>   recommend that you post the shipment receipt and invoice receipts separately
>   instead of entering a shipment/invoice receipt document. If you enter a
>   single shipment/invoice receipt document (with Quantity Shipped greater than
>   Quantity Invoiced) in the Receivings Transaction Entry window and later
>   enter additional invoice documents, amounts in General Ledger and Inventory
>   won’t match.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Purchasing Invoice Entry window,
>   but you can’t enter project information for blanket purchase orders. To
>   enter an invoice for a purchase order with project information, see *Chapter
>   17, “Invoice receipt entry for projects.”*

>   You can use the View \>\> Currency menu option or the currency list button
>   to view amounts in the Purchasing Invoice Entry window in originating or
>   functional currency.

>   **To enter an invoice receipt:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Purchase Order Transactions list.

2.  In the New group or its overflow menu, choose Invoice Receipt to open the
    Purchasing Invoice Entry window.

![](media/c919bc5fa8e014c9f5f1b117a9e1c9fe.jpg)

1.  Enter a vendor document number.

2.  Enter the invoice date.

>   *To enter a General Ledger posting date that is different from the invoice
>   date, choose the Invoice Date expansion button; the Purchasing Invoice Date
>   Entry window will open, where you can enter date information.*

>   For multicurrency transactions, the document date determines which exchange
>   rate is used, based on the currency ID that’s entered for the transaction
>   and the associated rate type.

1.  Enter or select a batch ID (optional).

>   If you’ve received the invoice, but not the shipment, you’ll need to save
>   the invoice receipt in a batch until you receive and post the shipment. Then
>   you can match the invoice to the shipment and post the invoice.

>   Invoices entered for drop-ship purchase orders and drop-ship blanket
>   purchase orders won’t be matched because you can’t enter a shipment receipt
>   for a dropship purchase order or a drop-ship blanket purchase order.

>   In multicurrency transactions, if the batch posting date does not fall on or
>   before the exchange rate’s expiration date, you will receive a message.
>   Choose

>   Yes to open the Batch Entry window and change the batch posting date. If you
>   choose No, you will be able to save but not post the receipt.

>   See *Creating a receipt batch* for more information.

1.  Enter or select a vendor ID.

2.  Enter or select a currency ID, or change the currency ID that appears as a
    default entry.

>   If the currency ID is not the company’s functional currency, a rate type and
>   associated exchange rate table are assigned to the transaction. The currency
>   ID assigned to the invoice must match the currency ID of the purchase order
>   being received against.

1.  Mark the LC option if you want to enter a landed cost.

2.  Enter the purchase order number.

>   You can leave this field blank if you’re entering an invoice for a shipment
>   received without a purchase order. You can receive invoices for multiple
>   purchase orders by entering or selecting a different purchase order number
>   in a new row.

>   You won’t be able to enter a purchase order number if you are invoicing a
>   landed cost. You will specify the purchase order you are matching to the
>   landed cost in the Match Options window.

>   Before you can invoice against the purchase order that has an unposted
>   prepayment, you must post the prepayment or remove the prepayment from the
>   purchase order.

1.  Enter items using either the vendor’s item number or your company’s item
    number. If you marked the LC option, you can enter a landed cost as an item.

>   After you enter a drop-ship or drop-ship blanket line item, the drop-ship
>   purchase order icon appears in the PO Number field.

>   You can display the vendor’s item number by marking Options \>\> Display
>   Vendor Item. If the option is not marked, your company’s item number will be
>   displayed. You can change this selection at any time.

1.  If a drop-ship or drop-ship blanket line item is tracking serial or lot
    numbers, mark the S/L option.

2.  Enter the quantity invoiced, which is the number of items on the vendor’s
    invoice.

>   If multiple shipments exist for the line item, you’ll get a message asking
>   if you want to match the invoice line items to items on a shipment or
>   shipment/ invoice before you move to the next line item.

-   Choose Yes and the Match Shipments to Invoice window will open, where you
    can choose which line items can be matched.

-   Choose No and the line items automatically will be matched in shipment
    receipt number order.

>   For more information, see *Matching shipments to an invoice receipt*.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the drop-ship or drop-ship blanket line item
>   requires that you assign lot or serial numbers.*

>   An icon will be displayed in the Quantity Invoiced field for drop-ship
>   purchase order line items with sales commitments. Select a line item and
>   choose the button next to the Quantity Invoiced heading to view commitments
>   in the Sales Commitments for Purchase Order window. If the purchase order
>   line item is committed to more than one sales order line item, you can use
>   the Sales Commitments for Purchase Order window to specify the sequence in
>   which the sales line items will be received. For more information, see
>   *Committing purchase orders to sales documents*.

1.  Enter trade discount, freight, miscellaneous, and tax amounts.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   If you want to change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for invoice receipts*. If you want to change the
>   tax amounts for a line item, see *Calculating and distributing detail taxes
>   for invoice line items*.

1.  The Prepayment field displays the total of all posted prepayments consumed
    for the purchase orders you are invoicing against. The prepayment amount is
    recalculated if you change the quantity shipped, quantity invoiced, unit
    cost, or extended cost for a line item. The prepayment amount is also
    recalculated if you change the trade discount.

>   If a purchase order has a posted prepayment, you can use the Prepayment
>   expansion button to open the Purchasing Prepayment Summary Inquiry window.
>   You can use this window to view the total amount of the prepayments applied
>   and the prepayment applied amount for each purchase order assigned to the
>   invoice.

1.  Enter or accept the 1099 amount, if applicable.

2.  If you are using Project Accounting, choose the Amount Received expansion
    button to open the PA Purchasing Invoice Amount Received Entry window, where
    you can enter an amount received. You can enter the amount you’re paying by
    cash, check, or credit card.

3.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window, where you can make changes to account distributions. See
    *Distributing transaction amounts for invoice receipts* for more
    information.

4.  Choose Save or Post. If you post, the invoiced quantities for each item on
    the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you saved the transaction to a batch, you can print an edit list.

#### Matching shipments to an invoice receipt

>   Use the Match Shipments to Invoice window if you’ve entered shipments in the
>   Receivings Transaction Entry window and want to match the line items on the
>   shipments to an invoice you’re entering in the Purchasing Invoice Entry
>   window. Invoices entered for drop-ship purchase orders or drop-ship blanket
>   purchase orders won’t be matched because you can’t enter a shipment receipt
>   for a drop-ship purchase order or a drop-ship blanket purchase order. For
>   information about matching shipment line items to landed costs, see
>   *Matching landed costs to shipment line items*. Landed costs aren’t
>   automatically matched.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Match Shipments to Invoice
>   window. To match shipments to an invoice receipt with project information,
>   see *Chapter 17, “Invoice receipt entry for projects.”*

>   **To match shipments to an invoice receipt:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, invoice date, and vendor
    ID.

2.  Enter the PO number and line items.

>   Before you can invoice against the purchase order that has an unposted
>   prepayment, you must post the prepayment or remove the prepayment from the
>   purchase order.

>   If you are using Workflow, a drop-ship purchase order or a drop-ship blanket
>   purchase order must be approved before you can invoice against the purchase
>   order. You can invoice against purchase orders that don’t need approval.

1.  Enter the quantity invoiced. If multiple shipments exist for the line item,
    you’ll get a message asking whether you want to automatically match the
    invoice line items to items on a shipment or shipment/invoice when you move
    to the next line.

2.  Choose Yes and the Match Shipments to Invoice window will open, where you
    can choose which line items can be matched. (If you choose No, the line
    items will be matched in shipment receipt number order.)

![](media/422535eca60e615aa8e4e02e2f9aadee.jpg)

>   Currency amounts in this window may be displayed in functional or
>   originating currency, depending on the view selected in the Purchasing
>   Invoice Entry window.

1.  Select the shipment line items you want to match to the invoice.

2.  Verify or change the default price variance posting account (optional). The
    difference between the shipment unit cost and the invoice cost, if any, will
    be posted to this account. Any unrealized purchase price variance associated
    with the shipment lines will also be posted to this account.

3.  Choose OK to save your changes and to close the Match Shipments to Invoice
    window.

4.  In the Purchasing Invoice Entry window, enter trade discount, freight,
    miscellaneous, and tax amounts. Also enter a 1099 amount, if applicable.

5.  If you are using Project Accounting, choose the Amount Received expansion
    button to open the PA Purchasing Invoice Amount Received Entry window, where
    you can enter an amount received. You can enter the amount you’re paying by
    cash, check, or credit card.

6.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window, where you can make changes to account distributions.

-   To add additional accounts, select the account and enter an amount.

-   To remove an account, select the row containing the account and choose Edit
    \>\> Delete Row.

-   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions are calculated for a landed
>   cost but won’t be displayed in the Purchasing Invoice Distribution Entry
>   window. To view landed cost distributions, print the Purchasing Invoice Edit
>   List.

>   See *Distributing transaction amounts for invoice receipts* for more
>   information.

>   Save or post the transaction. If you post, the invoiced quantities for each
>   item on the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you saved the transaction to a batch, you can print an edit list.

#### Invoicing items without a purchase order

>   In the Purchasing Invoice Entry window, you can enter invoice receipts for
>   items not included on the original purchase order or items not associated
>   with a purchase order.

>   To set up this option, you must select Allow Receiving Without a Purchase
>   Order in the Purchase Order Processing Setup window. You may assign a
>   password that must be entered before entering a line item not assigned to a
>   purchase order. See *Setting up Purchase Order Processing preferences and
>   default entries* for more information.

>   If receiving items without a purchase order is allowed, you can enter items,
>   noninventoried items or vendor items that don’t exist on the purchase order
>   on an invoice receipt as long as those items or vendor items are on a
>   shipment that has been posted.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Purchasing Invoice Entry window.
>   To invoice items with project information, see *Chapter 17, “Invoice receipt
>   entry for projects.”*

>   **To invoice items without a purchase order:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, invoice date, and vendor
    ID.

2.  To add vendor items or items that weren’t included on the original purchase
    order, simply leave the PO number field blank. You don’t have to enter a
    purchase order if you’ve set up the system to allow receiving items without
    a purchase order.

>   To enter a landed cost, mark the LC option and enter a landed cost as an
>   item.

1.  Continue entering the invoice.

>   If you enter a non-inventoried item that isn’t assigned to a purchase order,
>   you’ll need to enter a unit cost. If you enter a non-inventoried item that’s
>   assigned to a purchase order, the unit cost from the purchase order will be
>   displayed and you can change the cost.

1.  Save or post the transaction. If you post, the invoiced quantities for each
    item on the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you’ve saved the transaction to a batch, you can print an edit list.

#### Invoicing items using the Select Purchase Order window

>   Use the Select Purchase Order window to select a purchase order to quickly
>   enter line items on a invoice receipt.

>   If you are using Workflow, a drop-ship purchase order or a drop-ship blanket
>   purchase order must be approved before you can invoice against the purchase
>   order. You can invoice against purchase orders that don’t need approval.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Purchasing Invoice window, but
>   you can’t enter project information for blanket purchase orders.To receive
>   items for purchase orders with project information, see *Chapter 14,
>   “Shipment receipt entry for projects.”*

>   **To invoice items using the Select Purchase Order window:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, and invoice date.

2.  Choose the Auto-Invoice button. The Select Purchase Order window will open.

>   *If you entered a vendor ID, the Select Purchase Order Items window will
>   open instead of the Select Purchase Order window.*

![](media/0de6015486d587eb9ada7f75c01d7e05.jpg)

1.  Enter or select the purchase order for which you want to invoice all line
    items.

2.  Choose Invoice All in the Select Purchase Order window to automatically
    invoice all items on the selected purchase order. Landed costs aren’t
    included when you automatically invoice items. You must enter the landed
    costs on the invoice.

>   You cannot invoice against a purchase order that has an unposted prepayment.
>   You can remove the prepayment from the purchase order using the Purchase
>   Order Entry window or complete a computer check run for the prepayment.

>   The control blanket line item for a blanket purchase order or a drop-ship
>   blanket purchase order isn’t included when you automatically invoice items.

>   Blanket line items with a New status won’t be included, either. You can use
>   the

>   Purchasing Invoice Entry window to enter blanket line items with a New
>   status.

>   If you choose to view details in the Select Purchase Order window, the
>   Select Purchase Order Items window will open, and the purchase order line
>   items will be marked to receive. Landed costs won’t appear in the Select
>   Purchase Order Items window.

>   Drop-ship blanket line items with a New status and line items with a New
>   status for a drop-ship purchase order with an expired contract date won’t be
>   marked when you choose Mark All. To invoice these items, you must mark the
>   items individually.

1.  Choose OK to save information and to close the Select Purchase Order window.

2.  If the Allow Receiving Without a Purchase Order option is marked in Purchase
    Order Processing Setup, you can enter items or vendor items that don’t exist
    on the purchase order.

3.  You can enter blanket line items with a New status if you are invoicing
    items from a blanket purchase order or a drop-ship blanket purchase order.

4.  To enter a landed cost, mark the LC option and enter a landed cost as an
    item.

5.  If a drop-ship or drop-ship blanket line item is tracking serial or lot
    numbers, mark the S/L option. The Purchasing Serial Number Entry window or
    the Purchasing Lot Number Entry window opens, where you can enter the
    appropriate serial or lot numbers.

6.  Edit trade discount, freight, miscellaneous, and tax amounts. Also enter a
    1099 amount, if applicable.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   If you want to change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for shipment/invoice receipts*. If you want to
>   change the tax amounts for a line item, see *Calculating and distributing
>   detail taxes for shipment/invoice line items*.

1.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window, where you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account in the scrolling window, select the row containing
        the account and choose Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions are calculated for a landed
>   cost but won’t be displayed in the Purchasing Invoice Distribution Entry
>   window. To view landed cost distributions, print the Purchasing Invoice Edit
>   List.

>   See *Distributing transaction amounts for invoice receipts* for more
>   information.

1.  Save or post the transaction. If you post, the invoiced quantities for each
    item on the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you’ve saved the transaction to a batch, you can print an edit list.

#### Using the Select Purchase Order Items window

>   Use the Select Purchase Order Items window to invoice line items that have
>   been received from multiple purchase orders. In the Select Purchase Order
>   Items window, the tree view and the Sort By option control the information
>   that is displayed. When you change the focus in the tree view, or when you
>   choose a different sorting option, the information in the window is
>   refreshed.

>   The scrolling window shows detail about the object selected in the tree
>   view. When you highlight a different object in the tree view, such as a
>   purchase order or a site, only the information about that object is
>   displayed in the scrolling window. To display all information for a vendor,
>   you must select the vendor ID in the tree view.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Select Purchase Order Items
>   scrolling window.

>   The sorting option you select determines the order in which objects appear
>   in the tree view and the scrolling window. You can sort objects in four
>   ways:

>   **PO/Items** Objects in the tree view and scrolling window are sorted first
>   by purchase order number, then by the order items were entered on the
>   purchase orders.

![](media/62146f45260ac6e16877ae10bdf94c2b.jpg)

>   **Item Number/PO** Objects in the tree view and scrolling window are sorted
>   first by item number, then by purchase order number under each item.

![](media/f11494d245b8dd5ae212eff2b073fb79.jpg)

>   **Site/PO/Item Number** Objects in the tree view and scrolling window are
>   sorted first by site, then by purchase order number under each site, then by
>   item number under each purchase order.

![](media/1160002653d9293492354e2a9ce706d2.jpg)

>   **Site/Item Number/PO** Objects in the tree view and scrolling window are
>   sorted first by site, then by item number under each site, then by purchase
>   order number under each item.

![](media/e5b5e2a5f430908f3c64f8e4b06db89d.jpg)

#### Invoicing items from multiple purchase orders

>   Use the Select Purchase Order Items window to invoice line items that have
>   been received from multiple purchase orders. Only items with posted
>   shipments and quantities remaining to be invoiced will be displayed. See
>   *Entering an invoice receipt* for more information. Landed costs won’t
>   appear in the Select Purchase Order Items window.

>   If you are using Workflow, drop-ship purchase orders or a drop-ship blanket
>   purchase orders must be approved before you can invoice against them. You
>   can invoice against purchase orders that don’t need approval.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Select Purchase Order Items
>   window. To receive items from purchase orders with project information, see
>   *Chapter 17, “Invoice receipt entry for projects.”*

>   **To invoice items from multiple purchase orders:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, and invoice date.

2.  Enter or select a vendor ID. The currency ID assigned to the vendor will be
    the default currency ID for the receipt.

3.  Choose the Auto-Invoice button. The Select Purchase Order Items window will
    open.

>   Items with posted shipments and quantities remaining to be invoiced will be
>   displayed. The control blanket line item for a blanket purchase order or a
>   dropship blanket purchase order isn’t included when you automatically
>   invoice items.

>   If only a Vendor ID is displayed, the selected vendor does not have any
>   purchase orders with items that have been received, but not invoiced. Only
>   purchase orders with currency IDs that match the invoice will be displayed.
>   Purchase orders with posted prepayments that have currency IDs that match
>   the invoice will be displayed.

>   *If you know the purchase order number but not the vendor ID, you can choose
>   AutoInvoice without entering a vendor ID. The Select Purchase Order window
>   will open. The vendor and currency ID for the invoice will come from the
>   purchase order you select.*

![](media/41423ec501d8572a1ffca938889e05a0.jpg)

1.  Select a sorting option.

2.  Mark the check boxes next to the items you want to invoice. To select all
    items displayed in the scrolling window, choose Mark All.

>   Drop-ship blanket line items with a New status and line items with a New
>   status for a drop-ship purchase order with an expired contract date won’t be
>   marked when you choose Mark All. To invoice these items, you must mark the
>   items individually.

>   *When you choose Mark All or Unmark All in the Select Purchase Order Items
>   window, only items displayed in the scrolling window will be marked or
>   unmarked. For example, if a purchase order is selected in the tree view,
>   only items from that purchase order will be displayed in the scrolling
>   window, and only those items will be marked when you choose Mark All. To
>   mark or unmark all items for a vendor, the vendor ID must be selected in the
>   tree view.*

1.  Select whether to display all items or only items marked to invoice.

2.  Mark the S/L check box next to the drop-ship or drop-ship blanket items that
    require serial or lot numbers. To mark all items that require serial or lot
    numbers, choose Mark All S/L.

3.  Edit Quantity Invoiced and Unit Cost amounts, if necessary. If you edit an
    item in the scrolling window, it will be marked to invoice.

4.  Choose the Invoice button to add the items to your invoice. The Select
    Purchase Order Items window will close, and the items you marked will appear
    in the Purchasing Invoice Entry window.

>   The Purchasing Lot Number Entry window or the Purchasing Serial Number Entry
>   window will open if a drop-ship or drop-ship blanket item requires that you
>   assign lot or serial numbers.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Purchasing Invoice Entry window, save or post the transaction. If you
    post, the invoiced quantities for each item on the receipt must be fully
    matched to shipment quantities.

#### Invoicing items from a purchase order

>   Use the Select Purchase Order Items window and the Purchasing Invoice Entry
>   window to invoice items. After you select a purchase order that has at least
>   one posted shipment received against it in the Purchase Order Entry window,
>   you can select the Invoice the PO Items option from the Actions button. You
>   also can enter or select a drop-ship purchase order or a blanket drop-ship
>   purchase order and select the Invoice the PO Items option from the Actions
>   button to invoice against those items.

>   For more information about invoice receipts, see *Entering an invoice
>   receipt*. For more information about the Select Purchase Order Items window,
>   see *Using the Select Purchase Order Items window*. Landed costs won’t
>   appear in the Select Purchase Order Items window.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Cat. ID field will be displayed in the Select Purchase Order Items window
>   and the Purchasing Invoice Entry window. If you want to receive items with
>   project information, see *Chapter 17, “Invoice receipt entry for projects.”*

>   **To invoice items from a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order that has one or more items with a quantity
    to invoice.

2.  Select Invoice the PO Items from the Actions button.

3.  The Select Purchase Order Items window and the Purchasing Invoice Entry
    window will open.

>   Items with posted shipments and quantities remaining to be invoiced will be
>   displayed. The purchase order that you entered in the Purchase Order Entry
>   window will be selected in the tree view. Each item on the purchase order
>   that is available to be invoiced in the scrolling window is marked. The
>   control blanket line item for a blanket purchase order or a drop-ship
>   blanket purchase order isn’t included when you automatically invoice items.

1.  Select a sorting option.

2.  Mark the check boxes next to the items to invoice. To select all items
    displayed in the scrolling window, choose Mark All.

>   Drop-ship blanket line items with a New status and line items with a New
>   status for a drop-ship purchase order with an expired contract date won’t be
>   marked when you choose Mark All. To invoice these items, you must mark the
>   items individually.

>   *When you choose Mark All or Unmark All, only items displayed in the
>   scrolling window will be marked or unmarked. For example, if a purchase
>   order is selected in the tree view, only items from that purchase order will
>   be displayed in the scrolling window, and only those items will be marked
>   when you choose Mark All. To mark or unmark all items for a vendor, the
>   vendor ID must be selected in the tree view.*

1.  Select whether to display all items or only items marked to invoice.

2.  Mark the S/L check box next to the drop-ship or drop-ship blanket items that
    require serial or lot numbers. To mark all items that require serial or lot
    numbers, choose Mark All S/L.

3.  Modify the quantity invoiced and unit cost amounts, if necessary. If you
    modify an item in the scrolling window, it will be marked to invoice.

4.  Choose the Invoice button to add the items to your invoice. The Select
    Purchase Order Items window will close, and the items you marked will appear
    in the Purchasing Invoice Entry window.

>   The Purchasing Lot Number Entry window or the Purchasing Serial Number Entry
>   window will open if a drop-ship or drop-ship blanket item requires that you
>   assign lot or serial numbers.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Purchasing Invoice Entry window, continue entering invoice
    information, if necessary, and save or post the transaction. For an invoice,
    you must enter the vendor document number.

>   If you post, the invoiced quantities for each item on the receipt must be
>   fully matched to shipment quantities.

**Chapter 17: Invoice receipt entry for projects**

>   If you are using Project Accounting, you can enter an invoice receipt to
>   record an invoice received for a shipment receipt entered and posted
>   earlier, or to record an invoice received for a shipment that you have not
>   yet received. You also can enter an invoice for drop-ship purchase order
>   line items. You can enter invoice receipt transactions in a batch and save
>   them to post later, or enter and post them individually.

>   *If you are using vendor approval workflow, the vendor must have the
>   workflow status of Approved or No Approval Needed before you can post the
>   invoice receipts.*

>   To enter an invoice receipt for a blanket purchase order or a drop-ship
>   blanket purchase order, refer to *Chapter 16, “Invoice receipt entry.”*

>   This information is divided into the following sections:

-   *Entering an invoice receipt for projects*

-   *Matching shipments to an invoice receipt for projects*

-   *Invoicing items for projects without a purchase order*

-   *Invoicing items for projects using the Select Purchase Order window*

-   *Invoicing items for projects from multiple purchase orders*

-   *Invoicing items for projects from a purchase order*

#### Entering an invoice receipt for projects

>   Use the Purchasing Invoice Entry window to enter, save, and post invoice
>   receipts for projects. You can enter detailed information for each invoice.
>   You can include items from multiple purchase orders (from a single vendor)
>   on an invoice receipt. If you are using landed costs, you can enter a landed
>   cost as a line item.

>   To enter an invoice receipt for a blanket purchase order, refer to *Chapter
>   16, “Invoice receipt entry.”*

>   You can enter and save, but not post, invoice receipts for purchase orders
>   that are on hold. If an invoice for a purchase order that is on hold is
>   saved to a batch, the batch can be posted, but the invoice for the purchase
>   order that is on hold will remain in the batch.

>   If you expect to receive multiple invoices for a single shipment, we
>   recommend that you post the shipment receipt and invoice receipts separately
>   instead of entering a shipment/invoice receipt document. If you enter a
>   single shipment/invoice receipt document (with quantity shipped greater than
>   quantity invoiced) in the Receivings Transaction Entry window and later
>   enter additional invoice documents, amounts in General Ledger and Inventory
>   won’t match.

>   You can use the View \>\> Currency menu option or the currency list button
>   to view amounts in the Purchasing Invoice Entry window in originating or
>   functional currency.

>   **To enter an invoice receipt for projects:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select the receipt number.

2.  Enter a vendor document number.

3.  Enter the invoice date.

>   *To enter a General Ledger posting date that is different from the invoice
>   date, choose the Invoice Date expansion button; the Purchasing Invoice Date
>   Entry window will open, where you can enter date information.*

>   For multicurrency transactions, the document date determines which exchange
>   rate is used, based on the currency ID that’s entered for the transaction
>   and the associated rate type.

1.  Enter or select a batch ID (optional).

>   If you’ve received the invoice, but not the shipment, you’ll need to save
>   the invoice receipt in a batch until you receive and post the shipment. Then
>   you can match the invoice to the shipment and post the invoice.

>   Invoices entered for drop-ship purchase orders won’t be matched because you
>   can’t enter a shipment receipt for a drop-ship purchase order.

>   In multicurrency transactions, if the batch posting date does not fall on or
>   before the exchange rate’s expiration date, you will receive a message.
>   Choose Yes to open the Batch Entry window and change the batch posting date.
>   If you choose No, you will be able to save but not post the receipt.

>   See *Creating a receipt batch* for more information.

1.  Enter or select a vendor ID.

2.  Enter or select a currency ID, or change the currency ID that appears as a
    default entry.

>   If the currency ID is not the company’s functional currency, a rate type and
>   associated exchange rate table are assigned to the transaction. The currency
>   ID assigned to the invoice must match the currency ID of the purchase order
>   being received against.

1.  Mark the LC option if you want to enter a landed cost.

2.  Enter the purchase order number.

>   You can leave this field blank if you’re entering an invoice for a shipment
>   received without a purchase order. You can receive invoices for multiple
>   purchase orders by entering or selecting a different purchase order number
>   in a new row.

>   You can’t enter a purchase order number if you are invoicing a landed cost.
>   You will specify the purchase order you are matching the to the landed cost
>   in the Match Options window.

>   You can enter a purchase order that hasn’t been printed if Allow Receiving
>   of Unprinted PO option is marked in the PA Purchase Order Processing Setup
>   Options window.

1.  Enter a project number and cost category ID.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display the vendor items.

1.  Enter one or more items using your company’s item numbers. You also can
    enter non-inventoried items. If you marked the LC option, you can enter a
    landed cost as an item.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget.

>   After you enter a drop-ship line item, the drop-ship purchase order icon
>   appears in the PO Number field.

1.  If a drop-ship line item is tracking serial or lot numbers, mark the S/L
    option.

2.  Enter the quantity invoiced, which is the number of items on the vendor’s
    invoice.

>   If multiple shipments exist for the line item, you’ll get a message asking
>   if you want to match the invoice line items to items on a shipment or
>   shipment/ invoice before you move to the next line item.

-   Choose Yes and the Match Shipments to Invoice window will open, where you
    can choose which line items can be matched.

-   Choose No and the line items automatically will be matched in shipment
    receipt number order.

>   For more information, see *Matching shipments to an invoice receipt for
>   projects*.

>   *The Purchasing Lot Number Entry window or the Purchasing Serial Number
>   Entry window will open if the drop-ship line item requires that you assign
>   lot or serial numbers.*

1.  Enter trade discount, freight, miscellaneous, and tax amounts.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   You can't change the Tax amount in the Purchasing Invoice Entry window even
>   if your system is set up to allow editing summary-level taxes. If you want
>   to change the tax amounts for a line item, see *Calculating and distributing
>   detail taxes for invoice line items*.

1.  Enter or accept the 1099 amount, if applicable.

2.  To enter an amount received, choose the Amount Received expansion button to
    open the PA Receivings Amount Received Entry window. You can enter the
    amount you’re paying by cash, check, or credit card.

3.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window, where you can make changes to account distributions. See
    *Distributing transaction amounts for invoice receipts* for more
    information.

4.  Choose Save or Post. If you post, the invoiced quantities for each item on
    the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you saved the transaction to a batch, you can print an edit list.

#### Matching shipments to an invoice receipt for projects

>   Use the Match Shipments to Invoice window if you’ve entered shipments in the
>   Receivings Transaction Entry window and want to match the line items on the
>   shipments to an invoice you’re entering in the Purchasing Invoice Entry
>   window. Invoices entered for drop-ship purchase orders won’t be matched
>   because you can’t enter a shipment receipt for a drop-ship purchase order.
>   For information about matching shipment line items to landed costs, see
>   *Matching landed costs to shipment line items*. Landed costs aren’t
>   automatically matched.

>   If you want match shipments for blanket purchase orders to an invoice
>   receipt, see *Chapter 16, “Invoice receipt entry.”*

>   **To match shipments to an invoice receipt for projects:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, invoice date, and vendor
    ID.

2.  Enter the PO number, project number, cost category ID, and line items.

3.  Enter the quantity invoiced. If multiple shipments exist for the line item,
    you’ll get a message asking whether you want to automatically match the
    invoice line items to items on a shipment or shipment/invoice when you move
    to the next line.

4.  Choose Yes and the Match Shipments to Invoice window will open, where you
    can choose which line items can be matched. (If you choose No, the line
    items will be matched in shipment receipt number order.)

![](media/c2163e1a78f3e77833acfb9a54b9b875.jpg)

>   Currency amounts in this window may be displayed in functional or
>   originating currency, depending on the view selected in the Purchasing
>   Invoice Entry window.

1.  Select the shipment line items you want to match to the invoice.

2.  Verify or change the default price variance posting account (optional). The
    difference between the shipment unit cost and the invoice cost, if any, will
    be posted to this account. Any unrealized purchase price variance associated
    with the shipment lines will also be posted to this account.

3.  Choose OK to save your changes and to close the Match Shipments to Invoice
    window.

4.  In the Purchasing Invoice Entry window, enter trade discount, freight,
    miscellaneous, and tax amounts. Also enter a 1099 amount, if applicable.

5.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window, where you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account, select the row containing the account and choose
        Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions are calculated for a landed
>   cost but won’t be displayed in the Purchasing Invoice Distribution Entry
>   window. To view landed cost distributions, print the Purchasing Invoice Edit
>   List.

>   See *Distributing transaction amounts for invoice receipts* for more
>   information.

1.  Save or post the transaction. If you post, the invoiced quantities for each
    item on the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you saved the transaction to a batch, you can print an edit list.

#### Invoicing items for projects without a purchase order

>   In the Purchasing Invoice Entry window, you can enter invoice receipts for
>   items not included on the original purchase order or items not associated
>   with a purchase order.

>   To set up this option, you must select Allow Receiving Without a Purchase
>   Order in the Purchase Order Processing Setup window. You may assign a
>   password that must be entered before entering a line item not assigned to a
>   purchase order. See *Setting up Purchase Order Processing preferences and
>   default entries* for more information.

>   If receiving items without a purchase order is allowed, you can enter items
>   or noninventoried items that don’t exist on the purchase order on an invoice
>   receipt as long as those items are on a shipment that has been posted.

>   **To invoice items for projects without a purchase order:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, invoice date, and vendor
    ID.

2.  Enter a project number and cost category ID. If the item that you’re
    receiving isn’t assigned to a project because the item isn’t assigned to a
    budget, enter \<NONE\> or leave the Project Number field blank. If there
    isn’t a project number, you can leave the Cost Category field blank. If the
    item is assigned to a project, you must enter a cost category.

>   You can’t enter a project number or a cost category if the Options \>\>
>   Display Vendor Item is marked to display vendor items.

1.  To add items that weren’t included on the original purchase order, simply
    leave the PO number field blank. You don’t have to enter a purchase order if
    you’ve set up the system to allow receiving items without a purchase order.

>   Inventoried items entered for a project must be assigned to a cost category
>   in the Budget Detail IV Items window. If the item isn’t assigned to a
>   budget, you must add the item to the budget. You cannot add a new
>   inventoried item if the Allow Entry of New Budgets/Materials option is not
>   marked in the User Purchase Order Settings window. See *Inventoried items
>   and non-inventoried items for projects* for more information.

>   To enter a landed cost, mark the LC option and enter a landed cost as an
>   item.

1.  Continue entering the invoice.

>   If you enter a non-inventoried item that isn’t assigned to a purchase order,
>   you’ll need to enter a unit cost. If you enter a non-inventoried item that’s
>   assigned to a purchase order, the unit cost from the purchase order will be
>   displayed and you can change the cost.

1.  Save or post the transaction. If you post, the invoiced quantities for each
    item on the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you’ve saved the transaction to a batch, you can print an edit list.

#### Invoicing items for projects using the Select Purchase Order window

>   Use the Select Purchase Order window to select a purchase order to quickly
>   enter line items on a invoice receipt.

>   **To invoice items for projects using the Select Purchase Order window:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, and invoice date.

2.  Choose the Auto-Invoice button. The Select Purchase Order window will open.

>   *If you entered a vendor ID, the Select Purchase Order Items window will
>   open instead of the Select Purchase Order window.*

![](media/0de6015486d587eb9ada7f75c01d7e05.jpg)

1.  Enter or select the purchase order for which you want to invoice all line
    items.

2.  Choose Invoice All in the Select Purchase Order window to automatically
    invoice all items on the selected purchase order. Landed costs aren’t
    included when you automatically invoice items. You must enter the landed
    costs on the invoice.

>   If you choose to view details in the Select Purchase Order window, the
>   Select Purchase Order Items window will open, and the purchase order line
>   items will be marked to receive. Landed costs won’t appear in the Select
>   Purchase Order Items window.

1.  Choose OK to save information and to close the Select Purchase Order window.

2.  If the Allow Receiving Without a Purchase Order option is marked in Purchase
    Order Processing Setup, you can enter items or vendor items that don’t exist
    on the purchase order.

3.  To enter a landed cost, mark the LC option and enter a landed cost as an
    item.

4.  If a drop-ship line item requires serial or lot numbers, mark the S/L
    option. The Purchasing Serial Number Entry window or the Purchasing Lot
    Number Entry window opens, where you can enter the appropriate serial or lot
    numbers.

5.  Edit trade discount, freight, miscellaneous, and tax amounts. Also enter a
    1099 amount, if applicable.

>   Taxes will be calculated automatically as you enter items. For more
>   information about tax calculations, see *Chapter 20, “Taxes for receipts.”*
>   If you want to change the tax amounts for the document, see *Calculating and
>   distributing summary taxes for shipment/invoice receipts*. If you want to
>   change the tax amounts for a line item, see *Calculating and distributing
>   detail taxes for shipment/invoice line items*.

1.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window, where you can make changes to account distributions.

    -   To add additional accounts, select the account and enter an amount.

    -   To remove an account in the scrolling window, select the row containing
        the account and choose Edit \>\> Delete Row.

    -   To restore the original distributions, choose Default.

>   If you are using landed costs, the distributions are calculated for a landed
>   cost but won’t be displayed in the Purchasing Invoice Distribution Entry
>   window. To view landed cost distributions, print the Purchasing Invoice Edit
>   List.

>   See *Distributing transaction amounts for invoice receipts* for more
>   information.

1.  Save or post the transaction. If you post, the invoiced quantities for each
    item on the receipt must be fully matched to shipment quantities.

>   One or more posting journals and distribution breakdown registers may be
>   printed, depending on the options selected in the Posting Setup window. If
>   you’ve saved the transaction to a batch, you can print an edit list.

#### Invoicing items for projects from multiple purchase orders

>   Use the Select Purchase Order Items window to invoice line items that have
>   been received from multiple purchase orders. Only items with posted
>   shipments and quantities remaining to be invoiced will be displayed. See
>   *Entering an invoice receipt for projects* for more information. Landed
>   costs won’t appear in the Select Purchase Order Items window.

>   **To invoice items for projects from multiple purchase orders:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, and invoice date.

2.  Enter or select a vendor ID. The currency ID assigned to the vendor will be
    the default currency ID for the receipt.

3.  Choose the Auto-Invoice button. The Select Purchase Order Items window will
    open.

>   Items with posted shipments and quantities remaining to be invoiced will be
>   displayed.

>   If only a Vendor ID is displayed, the selected vendor does not have any
>   purchase orders with items that have been received, but not invoiced. Only
>   purchase orders with currency IDs that match the invoice will be displayed.

>   *If you know the purchase order number but not the vendor ID, you can choose
>   AutoInvoice without entering a vendor ID. The Select Purchase Order window
>   will open. The vendor and currency ID for the invoice will come from the
>   purchase order you select.*

1.  Select a sorting option.

2.  Mark the check boxes next to the items you want to invoice. To select all
    items displayed in the scrolling window, choose Mark All.

>   *When you choose Mark All or Unmark All in the Select Purchase Order Items
>   window, only items displayed in the scrolling window will be marked or
>   unmarked. For example, if a purchase order is selected in the tree view,
>   only items from that purchase order will be displayed in the scrolling
>   window, and only those items will be marked when you choose Mark All. To
>   mark or unmark all items for a vendor, the vendor ID must be selected in the
>   tree view.*

1.  Select whether to display all items or only items marked to invoice.

2.  Mark the S/L option next to the drop-ship items that require serial or lot
    numbers. To mark all items that require serial or lot numbers, choose Mark
    All S/L.

3.  Modify the quantity invoiced and unit cost amounts, if necessary. If you
    edit an item in the scrolling window, it will be marked to invoice.

4.  Choose the Invoice button to add the items to your invoice. The Select
    Purchase

>   Order Items window will close, and the items you marked will appear in the
>   Purchasing Invoice Entry window.

>   The Purchasing Lot Number Entry window or the Purchasing Serial Number

>   Entry window will open if a drop-ship item requires that you assign lot or
>   serial numbers.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Purchasing Invoice Entry window, save or post the transaction. If you
    post, the invoiced quantities for each item on the receipt must be fully
    matched to shipment quantities.

#### Invoicing items for projects from a purchase order

>   Use the Select Purchase Order Items window and the Purchasing Invoice Entry
>   window to invoice items. After you select a purchase order that has at least
>   one posted shipment received against it in the Purchase Order Entry window,
>   you can select the Invoice the PO Items option from the Actions button. You
>   also can enter or select a drop-ship purchase order and select the Invoice
>   the PO Items option from the Actions button to invoice against those items.

>   For more information about invoice receipts, see *Entering an invoice
>   receipt for projects*. For more information about the Select Purchase Order
>   Items window, see *Using the Select Purchase Order Items window*. Landed
>   costs won’t appear in the Select Purchase Order Items window.

>   To receive items from multiple blanket purchase orders, refer to *Chapter
>   16, “Invoice receipt entry.”*

>   **To invoice items for projects from a purchase order:**

1.  Open the Purchase Order Entry window.

>   (Purchasing \>\> Transactions \>\> Purchase Order Entry)

1.  Enter or select a purchase order that has one or more items with a quantity
    to invoice.

2.  Select Invoice the PO Items from the Actions button.

3.  The Select Purchase Order Items window and the Purchasing Invoice Entry
    window will open.

>   Items with posted shipments and quantities remaining to be invoiced will be
>   displayed. The purchase order that you entered in the Purchase Order Entry
>   window will be selected in the tree view. Each item on the purchase order
>   that is available to be invoiced in the scrolling window is marked.

1.  Select a sorting option.

2.  Mark the check boxes next to the items to invoice. To select all items
    displayed in the scrolling window, choose Mark All.

>   *When you choose Mark All or Unmark All, only items displayed in the
>   scrolling window will be marked or unmarked. For example, if a purchase
>   order is selected in the tree view, only items from that purchase order will
>   be displayed in the scrolling window, and only those items will be marked
>   when you choose Mark All. To mark or unmark all items for a vendor, the
>   vendor ID must be selected in the tree view.*

1.  Select whether to display all items or only items marked to invoice.

2.  Mark the S/L option next to the drop-ship items that require serial or lot
    numbers. To mark all items that require serial or lot numbers, choose Mark
    All S/L.

3.  Modify the quantity invoiced and unit cost amounts, if necessary. If you
    modify an item in the scrolling window, it will be marked to invoice.

4.  Choose the Invoice button to add the items to your invoice. The Select
    Purchase Order Items window will close, and the items you marked will appear
    in the Purchasing Invoice Entry window.

>   The Purchasing Lot Number Entry window or the Purchasing Serial Number

>   Entry window will open if a drop-ship item requires that you assign lot or
>   serial numbers.

>   To cancel your selections, choose Cancel. To revert all displayed items to
>   unmarked, choose Unmark All.

1.  In the Purchasing Invoice Entry window, continue entering invoice
    information, if necessary, and save or post the transaction. For an invoice,
    you must enter the vendor document number.

>   If you post, the invoiced quantities for each item on the receipt must be
>   fully matched to shipment quantities.

**Chapter 18: Invoice receipt detail entry**

>   The Purchasing Invoice Entry window is designed to resemble a physical
>   invoice document and includes vendor, line item, and total information. Use
>   the buttons in the Purchasing Invoice Entry window to open windows where you
>   can enter detailed information about lot number, serial number mask,
>   distributions and Intrastat trade statistics.

>   This information is divided into the following sections:

-   *Generating lot numbers automatically for invoice receipts*

-   *Entering lot numbers manually for an invoice receipt*

-   *Removing lot numbers from an invoice receipt*

-   *Generating serial numbers automatically for invoice receipts*

-   *Entering serial numbers manually for invoice receipts*

-   *Removing serial numbers for invoice receipts*

-   *Merging trade discount and purchase distributions*

-   *Distributing transaction amounts for invoice receipts*

-   *Entering project item detail information for an invoice receipt*

-   *Entering Intrastat trade statistics*

#### Generating lot numbers automatically for invoice receipts

>   If you are invoicing a drop-ship or drop-ship blanket purchase order, you
>   can use the Purchasing Lot Number Entry window to assign lot numbers for
>   lot-tracked line items. You can assign lot numbers automatically, manually,
>   or a combination of the two. In order to automatically generate lot numbers,
>   you must first set up the item and its lot number mask. For more
>   information, see *Defining a lot number mask*.

>   **To generate lot numbers automatically for invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select an invoice for a drop-ship or blanket drop-ship purchase
    order that includes at least one lot-numbered item.

2.  Mark the S/L option and enter the quantity invoiced for the line items that
    contain a lot number.

3.  Press TAB or choose the Quantity Invoiced expansion button to open the
    Purchasing Lot Number Entry window.

![](media/167dc441a17647f18e31ffd527bfbab1.jpg)

>   *To set up a lot number mask for the item, click the Lot Number Mask link in
>   the Purchasing Lot Number Entry window to open the Item Serial/Lot Number
>   Definition window.*

1.  Enter the lot(s) to generate (optional). The default lot(s) to generate is
    the Remaining to Select quantity divided by the Lot Split Quantity rounded
    to the next whole number.

2.  Edit the starting lot number, if necessary.

>   If you modify the starting lot number, it must conform to the lot number
>   mask. If you delete the starting lot number, you will not be able to
>   automatically generate lot numbers for the item.

1.  Choose Auto-Generate. Lot numbers for the items are inserted in the
    scrolling window. Numbers that already exist will be skipped.

>   The Total Quantity Selected must equal the item’s extended quantity before
>   you can move to the next line item in the Purchasing Invoice Entry window.

1.  Choose OK to save the lot numbers that were automatically generated.

#### Entering lot numbers manually for an invoice receipt

>   If you are invoicing a drop-ship or drop-ship blanket purchase order, you
>   can use the Purchasing Lot Number Entry window to assign lot numbers for
>   lot-tracked line items.

>   **To enter lot numbers manually for nonofficial receipt:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoice)

1.  Enter or select an invoice for a drop-ship or drop-ship blanket purchase
    order that includes a lot-numbered item.

2.  Mark the S/L option and enter the quantity invoiced for a line item that
    contains a lot number.

3.  Press TAB or choose the Quantity Invoiced expansion button to open the
    Purchasing Lot Number Entry window.

4.  Enter a lot number and a quantity selected.

5.  Choose Insert to add the lot number to the scrolling window.

6.  To assign values to the lot attributes for the item, choose the Lot
    expansion button to open the Lot Attribute Entry window.

>   If you are using sales workflow and are tracking the minimum shelf life for
>   the lot item, the dates that you enter in this window and the number of days
>   entered in the Item Maintenance Options window are used to determine whether
>   or not the item meets the minimum shelf life when you receive the item. If
>   you are using Project Accounting, you can’t use sales workflow with project
>   items.

1.  Continue entering lot numbers for the item. The Total Quantity Selected must
    equal the item’s extended quantity before you can move to the next line item
    in the Purchasing Invoice Entry window.

2.  Choose OK to save the lot numbers you’ve added.

#### Removing lot numbers from an invoice receipt

>   Use the Purchasing Lot Number Entry window to remove lot numbers for invoice
>   receipt line items.

>   **To remove lot numbers from an invoice receipt:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select an invoice for a drop-ship or drop-ship blanket purchase
    order that includes a lot-numbered item.

2.  Select a line item that contains a lot number.

3.  Choose the Quantity Invoiced expansion button to open the Purchasing Lot
    Number Entry window.

4.  Select the lot number from the Lot list and choose Remove. To remove all the
    lot numbers from the Lot list, choose Remove All.

5.  Enter new lot numbers for the item.

6.  Choose OK to save your changes.

#### Generating serial numbers automatically for invoice receipts

>   If you are invoicing a drop-ship or drop-ship blanket purchase order, you
>   can use the Purchasing Serial Number Entry window to assign serial numbers
>   for serialtracked line items. You can assign serial numbers automatically,
>   manually, or a combination of the two. In order to automatically generate
>   serial numbers, you must first set up the item and its serial number mask.
>   For more information, see *Defining a serial number mask*.

>   **To generate serial numbers automatically for invoice receipts:**

1.  Open the Purchasing Invoicing Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select an invoice for a drop-ship or drop-ship blanket purchase
    order that includes at least one serial-numbered item.

2.  Mark the S/L option and enter the quantity invoiced for the line items that
    contain a serial number.

3.  Press TAB or choose the Quantity Invoiced expansion button to open the
    Purchasing Serial Number Entry window.

![](media/039ce7beb4b0826eb3028a60043c2063.jpg)

>   *To set up a serial number mask for the item, click the Serial Number Mask
>   link in the Purchasing Serial Number Entry window to open the Item
>   Serial/Lot Number Definition window.*

1.  Enter the Quantity to Generate (optional). The default Quantity to Generate
    is the Remaining to Select quantity.

2.  Edit the starting serial number, if necessary.

>   If you modify the starting serial number, it must conform to the serial
>   number mask. If you delete the starting serial number, you will not be able
>   to automatically generate serial numbers for the item.

1.  Choose Auto-Generate. Serial numbers for the items are inserted in the
    scrolling window. Numbers that already exist will be skipped.

>   The number of serial numbers must equal the item’s extended quantity before
>   you can return to the Purchasing Invoice Entry window.

1.  Choose OK to save the serial numbers that were automatically generated.

#### Entering serial numbers manually for invoice receipts

>   Use the Purchasing Serial Number Entry window to assign serial numbers
>   manually for invoice receipt line items.

>   **To enter serial numbers manually for invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select an invoice for a drop-ship or drop-ship blanket purchase
    order that includes at least one serial-numbered item.

2.  Mark the S/L option and enter the quantity invoiced for the line items that
    contain a serial number.

3.  Press TAB or choose the Quantity Invoiced expansion button to open the
    Purchasing Serial Number Entry window.

4.  Enter a serial number.

5.  Choose Insert to add the serial number to the scrolling window.

6.  Continue entering serial numbers for the item.

>   The number of serial numbers entered must equal the item’s extended quantity
>   before you can move to the next line item in the Purchasing Invoice Entry
>   window.

1.  Choose OK to save the serial numbers you’ve added.

#### Removing serial numbers for invoice receipts

>   Use the Purchasing Serial Number Entry window to remove serial numbers for
>   invoice receipt line items. Whether you have auto-generated or manually
>   entered serial numbers, you can always choose to remove an incorrect number
>   from the scrolling window, correct or modify it and reinsert it. You cannot
>   modify serial numbers once they are saved.

>   **To remove serial numbers for invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select an invoice for a drop-ship or drop-ship blanket purchase
    order that includes a serial-numbered item.

2.  Select a line item that contains a serial number.

3.  From the Quantity Invoiced column, choose the Quantity Invoiced expansion
    button to open the Purchasing Serial Number Entry window.

4.  Select the serial number from the serial number selected list and choose
    Remove. To remove all the serial numbers from the serial number selected
    list, choose Remove All.

5.  Enter new serial numbers for the item. The number of serial numbers entered
    must equal the item’s extended quantity before you can move to the next line
    item in the Purchasing Invoice Entry window.

6.  Choose OK to save your changes.

#### Merging trade discount and purchase distributions

>   If you’ve marked the Merge Trade Discount Distributions in Purchasing option
>   in the Company Setup Options window, the trade discount distributions will
>   be merged with the purchases distribution for invoice receipts. If you are
>   using Project Accounting, the trade discount distributions won’t be merged
>   with the purchases distributions for invoice receipts.

>   For example, assume that you’ve entered a purchase transaction of \$100.00
>   with a trade discount of \$15.00. If you’ve marked the Merge Trade Discount
>   Distributions in Purchasing option, the trade discount distributions will be
>   merged as in the following example.

| **Account**     | **Debit** | **Credit** |
|-----------------|-----------|------------|
| Account A PURCH | \$85      |            |
| Account C PAY   |           | \$85       |

>   If you didn’t mark the Merge Trade Discount Distributions in Purchasing
>   option, the trade discount distributions are separated from the purchase
>   distribution.

| **Account**     | **Debit** | **Credit** |
|-----------------|-----------|------------|
| Account A PURCH | \$100     |            |
| Account B TRADE |           | \$15       |
| Account C PAY   |           | \$85       |

#### Distributing transaction amounts for invoice receipts

>   Use the Purchasing Invoice Distribution window to distribute transaction
>   amounts for invoices. Transactions will be distributed automatically to
>   posting accounts; however, those distributions can be edited.

>   **To distribute transaction amounts for invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select an invoice.

2.  Choose Distributions to open the Purchasing Invoice Distribution Entry
    window.

![](media/c8d56bdd4414a9f4ff6ca25dc7fb7fea.jpg)

1.  In the Reference field, change the reference displayed (optional). The
    reference entered will post to General Ledger as the reference for the
    receipt.

2.  Change the amounts for the default accounts.

3.  You can distribute a transaction to multiple posting accounts. Change the
    default amount in the scrolling window.

4.  In the next available line, enter or select another purchasing distribution
    account, choose the distribution type and enter the next amount.

>   If you want to delete an account, select the row containing it and choose
>   Edit \>\> Delete Row. If you changed distribution accounts and amounts and
>   want to use the original distributions, choose Default.

1.  Continue entering distribution accounts until your transaction is fully
    distributed.

2.  Enter a reference or accept the default. This is the reference that will be
    posted as the General Ledger distribution reference for the account.

3.  Choose OK to save your entries and continue entering the transaction. You
    can save the transaction if it’s not fully distributed, but you won’t be
    able to post until the full amount is distributed and debits equal credits.

#### Entering project item detail information for an invoice receipt

>   If you are using Project Accounting, you can use the PA Purchasing Invoice
>   Item Detail Entry window to add a billing note or modify the billing type.
>   If the item is for a time and materials project, you can enter a billing
>   rate or markup percentage and view the accrued revenue.

>   **To enter project item detail information for an invoice receipt:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select a receipt number, vendor ID, project number, cost category,
    and item.

2.  Choose the Cost Category expansion button to open the PA Purchasing Invoice
    Item Detail Entry window.

![](media/2fb0446b9d2eff43603f2f22dea89ef4.jpg)

1.  Enter or modify a billing note.

2.  Modify the billing type, if applicable. The item must be a non-inventoried
    item to modify the billing type.

3.  If the non-inventoried item is for a time and materials project, you can
    enter a billing rate or markup percentage.

>   Choose OK to close the window and return to the Purchasing Invoice Entry
>   window.

#### Entering Intrastat trade statistics

>   Use the Purchasing Intrastat Entry window to enter the information required
>   to create the Intrastat Trade Report you submit to your government. You can
>   enter Intrastat statistics for each line item. For information about setting
>   up Intrastat codes, refer to your System Setup instructions (Help \>\>
>   Contents \>\> select Setting Up the System).

>   Intrastat is the system for collecting statistics on the trade of goods
>   between European Union (EU) countries. Intrastat data is required for all
>   items either bought from EU vendors or sold to EU customers, and must be
>   provided on a monthly basis. Requirements for Intrastat are similar in all
>   EU countries. The government uses these statistics as an economic indicator.

>   If Intrastat information was entered for the vendor’s ship from address ID,
>   that information appears in this window. Each time you enter a new line
>   item, the Intrastat statistics from the previous line item will be the
>   default Intrastat entry for the new line item.You can use the Purchasing
>   Intrastat Entry window to change Intrastat information for an individual
>   transaction, or to enter Intrastat information if none was entered for the
>   vendor.

>   *You can enter Intrastat statistics only if you have marked to enable
>   Intrastat tracking in the Company Setup Options window.*

>   **To enter Intrastat trade statistics:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the EU transaction, including the vendor ID and the goods value.

2.  Choose the EU button to open the Purchasing Intrastat Entry window. You can
    also open the Purchasing Intrastat Entry window by choosing the EU button in
    the Receivings Item Detail Entry window.

3.  Enter Intrastat information, or change the default entries, if necessary.

4.  In the Net Unit Mass field, enter the weight of the goods in kilograms.

5.  Enter the quantity of the goods being purchased.

>   The line mass displays the total mass per item and is calculated
>   automatically when you press TAB on the Quantity field. The line mass total
>   is equal to the amount entered in the Unit Mass field multiplied by the
>   amount entered in the Quantity field.

1.  Enter a supplementary units amount, if applicable. The supplementary units
    amount is simply a second quantity. Supplementary unit amounts are required
    by the EU Combined Nomenclature for certain goods.

2.  In the Traders Reference field, enter a reference code, such as an invoice
    or dispatch number, or any other information that will identify the
    transaction.

3.  Enter a goods value and statistical value, if applicable.

4.  Choose OK to save the record.

218 P U R C H A S E O R D E R P R O C E S S I N G

**Chapter 19: Landed costs for receipts**

>   Landed costs are the additional costs that might be associated with
>   purchasing a product. For example, if you purchase items from another
>   country/region, the amount you must pay also might include freight costs, or
>   duties.

>   To assign a landed cost to all the items on a receipt, use the Receivings
>   Landed Cost Apportionment window. To assign a landed cost to an item on a
>   receipt, use the Receivings Landed Cost Entry window.

>   This information is divided into the following sections:

-   *Landed cost overview*

-   *How landed costs are apportioned*

-   *Invoice matching and distributions*

-   *Entering landed costs for a shipment receipt*

-   *Entering landed costs for an in-transit inventory receipt*

-   *Entering landed costs for a shipment item*

-   *Entering landed costs for an in-transit inventory item*

-   *Matching landed costs to shipment line items*

-   *Matching landed costs to in-transit inventory line items*

#### Landed cost overview

>   Landed costs are the additional costs that might be associated with
>   purchasing a product, such as freight costs, insurance, or duties. To use
>   landed costs, you must set up landed cost records and groups in Inventory
>   Control. You can define different landed costs in the Landed Cost
>   Maintenance window, including information such as the vendor the landed cost
>   is for, the cost calculation method used, and whether invoices must be
>   matched. You can create as many landed cost records as you like.

>   Once you’ve created landed cost records, you can create landed cost groups
>   using the Landed Cost Group Maintenance window. A landed cost group is a
>   collection of several landed cost records. Each landed cost record can exist
>   in multiple landed cost groups. Each landed cost group can include as many
>   landed cost records as you like. By creating a landed cost group and
>   assigning it to item-site combinations, you can associate many different
>   landed cost records with an item-site combination. For more information
>   about landed cost records and groups, refer to the Inventory Control
>   documentation.

>   When the item-site combination is entered on a purchase order or in-transit
>   transfer, the landed cost group information automatically is reflected in
>   the transaction. You can enter a landed cost group or accept the default
>   landed cost group ID for the purchase order or in-transit transfer. You can
>   use the Item Quantities Maintenance window to enter information for each
>   item-site combination.

>   As you enter a receipt in Purchase Order Processing, you can assign landed
>   costs. To assign a landed cost to all the items on a receipt, use the
>   Receivings Landed Cost Apportionment window. To assign a landed cost to an
>   item on a receipt, use the Receivings Landed Cost Entry window.

>   You can use the Match Shipments to Invoice window to match the landed costs
>   that you’ve entered in the Purchasing Invoice Entry window to one or more
>   shipment items or in-transit inventory items. Landed costs aren’t
>   automatically matched. To match the landed costs to shipment items or
>   in-transit inventory items, the landed costs must be set up to invoice
>   match. You can mark the landed costs to match when entering landed costs
>   using the Receivings Landed Cost Apportionment window or the Receivings
>   Landed Cost Entry window. More information about landed costs is included in
>   the Inventory Control documentation.

#### How landed costs are apportioned

>   In the Receivings Landed Cost Apportionment window, you can select how to
>   apportion or distribute the landed cost amounts among line items.You can
>   apportion a calculation method of Flat Amount by Value, Quantity, or Weight.
>   If the calculation method is Flat Amount per Unit or Percent of Extended
>   Cost, the landed costs will be created for all line items.

>   During the apportionment calculation, a remaining amount for the flat amount
>   is tracked. The calculated apportionment amount for each line item is
>   subtracted from the remaining amount. If a remaining amount can’t be
>   distributed across items due to rounding, it will be distributed to the last
>   line item.

>   **Quantity apportionment calculation**

>   If you selected to apportion landed costs by quantity, the calculation for
>   apportionment is a line item’s quantity shipped - the quantity rejected /
>   the sum of all line items’ quantity shipped - quantity rejected x the Flat
>   Amount.

>   For example, assume that you have the following receipt line items entered.
>   The calculation amount for the landed cost is Flat Amount and the Flat
>   Amount is \$50.00.

| **Item** | **Qty shipped** | **Qty rejected** | **Unit cost** | **Extended cost** |
|----------|-----------------|------------------|---------------|-------------------|
| Item1    | 10              | 2                | 10.00         | 80.00             |
| Item2    | 2               | 0                | 20.00         | 40.00             |
| Item3    | 6.5467          | 0.000            | 2             | 13.09             |

>   The landed cost would be apportioned as follows:

| **Item**  | **Qty shipped** | **Qty rejected** | **Net qty shipped** | **Landed cost calculation**   | **Remaining amt**    | **Landed cost amt** |
|-----------|-----------------|------------------|---------------------|-------------------------------|----------------------|---------------------|
| Item1     | 10              | 2                | 8                   | (8/16.5467) x 50 = 24.17      | 50.00 - 24.17 =26.83 | 24.17               |
| Item2     | 2               | 0                | 2                   | (2/16.5467) x 50 = 6.04       | 26.83 - 6.04 = 19.79 | 6.04                |
| Item3     | 6.5467          | 0.000            | 6.5467              | (6.5467/16.5467) x 50 = 19.78 | 19.79 - 19.78 =.01   | 19.79               |
| **Total** | 18.5467         | 2                | 16.5467             |                               | 50.00                | 50.00               |

>   Note that the last item received the remaining \$.01.

>   **Value apportionment calculation**

>   If you selected to apportion landed costs by Value, the calculation for
>   apportionment is the percent of the line item’s value to the total of all
>   the line items’ value x the Flat Amount.

>   The percent is calculated as [(Individual Line Item’s Qty Shipped -
>   Individual Line Item’s Qty Rejected) x Originating Unit Cost]/ Sum of all
>   line item’s [Qty Shipped- Qty Rejected) x Originating Unit Cost)].

>   For example, assume that you have the following receipt line items entered.
>   The calculation amount for the landed cost is Flat Amount and the Flat
>   Amount is \$50.00.

| **Item** | **Qty shipped** | **Qty rejected** | **Unit cost** | **Extended cost** |
|----------|-----------------|------------------|---------------|-------------------|
| Item1    | 10              | 2                | 10.00         | 80.00             |
| Item2    | 5               | 0                | 20.00         | 100.00            |
| Item3    | 6.5467          | 0.000            | 2             | 13.09             |

>   The landed cost would be apportioned as follows

| **Item**  | **Landed cost calculation**                                                                       | **Remaining amt**     | **Landed cost amt** |
|-----------|---------------------------------------------------------------------------------------------------|-----------------------|---------------------|
| Item1     | [[(10-2) x 10.00)]/[(10-2) x 10.00]+ [(5-0) x 20.00]+[(6.5467-0.0000) x 2.00]]x 50.00 = 20.72     | 50.00 - 20.72 = 29.28 | 20.72               |
| Item2     | [[(5-0) x 20.00)]/[(10-2) x 10.00]+ [(5-0) x 20.00]+[(6.5467-0.0000) x 2.00]] x 50.00 = 25.89     | 29.28 - 25.89 = 3.39  | 25.89               |
| Item3     | [[(6.5467-0) x 2.00)]/[(10-2) x 10.00]+ [(5-0) x 20.00]+[(6.5467- 0.0000) x 2.00]] x 50.00 = 3.39 | 3.39 - 3.39 = 0.00    | 3.39                |
| **Total** |                                                                                                   | 50.00                 | 50.00               |

>   **Weight apportionment calculation**

>   If you selected to apportion landed costs by Weight, the calculation for
>   apportionment is the (Individual Line Item’s Extended Shipping Weight / Sum
>   of all line items’ Extended Shipping Weight} x the Flat Amount.

>   The Extended Shipping Weight is calculated as the Individual Line Item’s
>   Shipping Weight x (quantity shipped - quantity rejected).

>   For example, assume that you have the following receipt line items entered.
>   The calculation amount for the landed cost is Flat Amount and the Flat
>   Amount is \$50.00.

| **Item**  | **Shipping weight** | **Qty shipped** | **Qty rejected** | **Extended shipping weight**      | **Unit cost** | **Extended cost** |
|-----------|---------------------|-----------------|------------------|-----------------------------------|---------------|-------------------|
| Item1     | 5.00                | 10              | 2                | 5.00 x (10 - 2) = 40              | 10.00         | 80.00             |
| Item2     | 1.23                | 5               | 0                | 1.23 x (5 - 0) = 6.15             | 20.00         | 100.00            |
| Item3     | .99                 | 6.5467          | 0.0000           | 0.99 x (6.5467 - 0.0000) = 6.4812 | 2.00          | 13.09             |
| **Total** |                     |                 |                  | 52.6312                           |               |                   |

>   The landed cost would be apportioned as follows

| **Item**  | **Shipping weight** | **Landed cost calculation**     | **Remaining amt**     | **Landed cost amt** |
|-----------|---------------------|---------------------------------|-----------------------|---------------------|
| Item1     | 5.00                | (40.00/52.6312) x 50.00 = 38.00 | 50.00 - 38.00 = 12.00 | 38.00               |
| Item2     | 1.23                | (6.15/52.6312) x 50.00 = 5.84   | 12.00 - 5.84 = 6.16   | 5.84                |
| Item3     | 0.99                | (6.4812/52.6312) x 50.00 = 6.16 | 6.16 - 6.16 = 0.00    | 6.16                |
| **Total** |                     |                                 | 50.00                 | 50.00               |

#### Invoice matching and distributions

>   Matching items assigned to a shipment or shipment/invoice to the landed
>   costs entered on the invoice will affect account distributions. If you
>   decide not to match, you will be responsible for making entries of the
>   accrual account into an adjusting expense account for cost variances. For
>   example, suppose that a shipment is recorded for 10 items at \$1 each. The
>   landed cost uses the Flat Amount cost calculation method on an amount of
>   \$0.50.

>   The distributions for the shipment would look as follows:

| **Account**                     | **Debit amount** | **Credit amount** |
|---------------------------------|------------------|-------------------|
| Inventory                       | \$10.50          |                   |
| Accrued Purchases - Landed Cost |                  | \$0.50            |
| Accrued Purchases - Inventory   |                  | \$10              |

>   Suppose that when the invoice is received, the cost of the goods is
>   unchanged, but the landed cost has increased to \$0.75. If Match is not
>   marked, the account distributions would be as follows:

| **Account**                     | **Debit amount** | **Credit amount** |
|---------------------------------|------------------|-------------------|
| Accrued Purchases - Landed Cost | \$0.75           |                   |
| Accrued Purchases - Inventory   | \$10             |                   |
| Accounts Payable                |                  | \$10.75           |

>   If Match and Revalue IV is marked, the account distributions would be as
>   follows:

| **Account**                     | **Debit amount** | **Credit amount** |
|---------------------------------|------------------|-------------------|
| Accrued Purchases - Landed Cost | \$0.50           |                   |
| Accrued Purchases - Inventory   | \$10             |                   |
| Inventory                       | \$0.25           |                   |
| Accounts Payable                |                  | \$10.75           |

#### Entering landed costs for a shipment receipt

>   Use the Receivings Landed Cost Apportionment window to distribute landed
>   costs to all receivings line items assigned to a document. The landed cost
>   is distributed based on its calculation method. You also can change or
>   delete landed costs that have been assigned to receivings line items. If you
>   want to remove a landed cost, select the landed cost ID and choose Edit \>\>
>   Delete Row. If you want to remove all the apportioned landed costs from all
>   associated receiving line items, choose Delete.

>   If you want to enter a landed cost for an individual receivings line item,
>   see *Entering landed costs for a shipment item*.

>   **To enter landed costs for a shipment receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select a shipment or shipment/invoice as the receipt type.

2.  Enter document information, including receipt number, vendor document
    number, and receipt date.

3.  Receive items.

    -   Choose Auto-Rcv to open the Select Purchase Order window, where you can
        select a purchase order to receive items from.

    -   Enter or select a vendor ID and choose Auto-Rcv to open the Select
        Purchase Order Items window, where you can receive line items on
        multiple purchase orders.

    -   Enter or select a vendor ID and enter line item information.

>   *If you are using Workflow, purchase orders must be approved before you can
>   receive against them. You can receive against purchase orders that don’t
>   need approval.*

1.  Enter total information in the Receivings Transaction Entry window.

2.  Choose the Landed Cost button to open the Receivings Landed Cost
    Apportionment window.

![](media/c1c5684d5dc8fc1c4302e162228f7268.jpg)

1.  Enter or select a landed cost ID.

2.  Select how to apportion the landed costs for the items.

3.  Mark the Match option if you want the landed cost assigned to the shipment
    item to be matched to an invoice.

4.  Enter the reference that you want to post as the General Ledger distribution
    reference for the accrued purchases account (optional).

5.  Enter a purchase price variance account. A purchase price variance account
    is required if the landed cost is set up to invoice match in the Landed Cost
    Maintenance window.

6.  Choose Apply to apply the apportioned landed costs to the line item.

>   If you are done working in this window, use the close box to return to the
>   Receivings Transaction Entry window.

#### Entering landed costs for an in-transit inventory receipt

>   Use the Receivings Landed Cost Apportionment window to distribute landed
>   costs to all in-transit inventory line items assigned to a receipt. The
>   landed cost is distributed based on its calculation method. You also can
>   change or delete landed costs that have been assigned to in-transit
>   inventory line items. If you want to remove a landed cost, select the landed
>   cost ID and choose Edit \>\> Delete Row. If you want to remove all the
>   apportioned landed costs from all associated in-transit inventory line
>   items, choose Delete.

>   If you want to enter a landed cost for an individual in-transit inventory
>   line item, see *Entering landed costs for a shipment item*.

>   **To enter landed costs for an in-transit inventory receipt:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select In-Transit Inventory as the receipt type.

2.  Enter receipt number and receipt date.

3.  Enter line item information.

4.  Choose the Landed Cost button to open the Receivings Landed Cost
    Apportionment window.

5.  Enter or select a landed cost ID.

6.  Select how to apportion the landed costs for the items.

7.  Mark the Match option if you want the landed cost assigned to the in-transit
    inventory item to be matched to an invoice.

8.  Enter the reference that you want to post as the General Ledger distribution
    reference for the accrued purchases account (optional).

9.  Enter a purchase price variance account. A purchase price variance account
    is required if the landed cost is set up to invoice match in the Landed Cost
    Maintenance window.

10. Choose Apply to apply the apportioned landed costs to the line item.

>   If you are done working in this window, use the close box to return to the
>   Receivings Transaction Entry window.

#### Entering landed costs for a shipment item

>   Use the Receivings Landed Cost Entry window to view, edit, add, or delete
>   landed costs that are assigned to a selected receiving line item. If you
>   assigned a landed cost group ID to a purchase order item, the landed costs
>   assigned to that group will be displayed in this window when you receive
>   against the purchase order item. You also can view the landed costs assigned
>   to the item using the Receivings Landed Cost Apportionment window. For more
>   information about entering landed costs to all receivings line items
>   assigned to a document, see *Entering landed costs for a shipment receipt*.

>   If you want to remove a landed cost, select the landed cost ID and choose
>   Edit \>\> Delete Row. If you want to remove all the landed costs from the
>   item, choose Delete.

>   **To enter landed costs for a shipment item:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select a document type and enter document information, including receipt
    number, vendor document number, receipt date, vendor ID, and currency ID.

2.  Enter the item or vendor item.

3.  Choose the Unit Cost button to open the Receivings Landed Cost Entry window.

![](media/35bf38692e0f23af69414f04fe1c5bfd.jpg)

1.  Enter or select a landed cost ID.

>   If a landed cost group ID was assigned to the item you’re receiving against,
>   the landed costs assigned to that group ID will be displayed.

1.  Mark the Match option if you want the landed cost assigned to the shipment
    item to be matched to an invoice.

2.  Enter the reference that you want to post as the General Ledger distribution
    reference for the accrued purchases account (optional).

3.  Enter a purchase price variance account. A purchase price variance account
    is required if the landed cost is set to invoice match in the Receivings
    Landed Cost Entry window.

4.  Choose OK to save your changes and close the window.

#### Entering landed costs for an in-transit inventory item

>   Use the Receivings Landed Cost Entry window to view, edit, add, or delete
>   landed costs that are assigned to a selected in-transit inventory line item.
>   If you assigned a landed cost group ID to an in-transit transfer item, the
>   landed costs assigned to that group will be displayed in this window when
>   you enter an in-transit inventory receipt for an in-transit transfer. You
>   also can view the landed costs assigned to the item using the Receivings
>   Landed Cost Apportionment window. For more information about entering landed
>   costs to all in-transit inventory line items assigned to a document, see
>   *Entering landed costs for a shipment receipt*.

>   If you want to remove a landed cost, select the landed cost ID and choose
>   Edit \>\> Delete Row. If you want to remove all the landed costs from the
>   item, choose Delete.

>   **To enter landed costs for an in-transit inventory item:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select In-Transit Inventory as the document type.

2.  Enter the receipt number and receipt date.

3.  Enter the transfer number and item.

4.  Choose the Unit Cost expansion button to open the Receivings Landed Cost
    Entry window.

5.  Enter or select a landed cost ID.

>   If a landed cost group ID was assigned to the item you’re entering an
>   in-transit inventory receipt for, the landed costs assigned to that group ID
>   will be displayed.

1.  Mark the Match option if you want the landed cost assigned to the in-transit
    inventory item to be matched to an invoice.

2.  Enter the reference that you want to post as the General Ledger distribution
    reference for the accrued purchases account (optional).

3.  Enter a purchase price variance account. A purchase price variance account
    is required if the landed cost is set to invoice match in the Receivings
    Landed Cost Entry window.

4.  Choose OK to save your changes and close the window.

#### Matching landed costs to shipment line items

>   If you are using landed costs, you can use the Match Shipments to Invoice
>   window to match the landed costs that you’ve entered in the Purchasing
>   Invoice Entry window to one or more shipment items. All the shipment items
>   that are available to match to the landed cost IDs are displayed in the
>   Match Shipments to Invoice window. Landed costs aren’t automatically
>   matched. To match the landed costs to shipment items, the landed costs must
>   be set up to invoice match. You can mark the landed costs to match when
>   entering landed costs using the Receivings Landed Cost Apportionment window
>   or the Receivings Landed Cost Entry window. You must be keeping receipt
>   history to match landed costs.

>   **To match landed costs to shipment line items:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, invoice date, and vendor
    ID assigned to the landed cost ID.

>   *The currency ID of the invoice must be the same as the shipment receipt
>   that the landed cost was entered on.*

1.  Invoice items (optional).

    -   Choose Auto-Invoice to open the Select Purchase Order window, where you
        can automatically invoice all shipment line items available for an
        invoice.

    -   Enter or select a vendor ID and choose Auto-Invoice to open the Select
        Purchase Order Items window, where you can invoice line items that have
        been received from multiple purchase orders.

    -   Enter or select a vendor ID and enter line item information.

>   *If you are using Workflow, drop-ship purchase orders and drop-ship blanket
>   purchase orders must be approved before you can invoice against them. You
>   can invoice against purchase orders that don’t need approval.*

1.  Mark the LC option and enter a landed cost ID.

2.  Choose the Match Shipments to Invoice expansion button to open the Match
    Shipments to Invoice window.

![](media/98e4f47d2e2ce62fb511c168fc84fed1.jpg)

>   Currency amounts in this window may be displayed in functional or
>   originating currency, depending on the view selected in the Purchasing
>   Invoice Entry window.

1.  Mark the Match option for the shipment line items you want to match to the
    landed cost item entered on the invoice.

2.  To quickly match all line items for a shipment or shipment/invoice to the
    landed cost entered on the invoice, choose the Match Options button to open
    the Match Options window. You can match the selected landed cost to the
    items on the shipment or shipment/invoice by either receipt number or PO
    number.

![](media/8823a031357e2f2ece184e085e20cc68.jpg)

1.  Mark Revalue IV if you want to have purchase receipts revalued if the cost
    variance for a matched invoice is greater than the tolerance percentage.

2.  Verify or change the default price variance posting account (optional).

3.  Choose OK to save your changes and to close the Match Shipments to Invoice
    window.

#### Matching landed costs to in-transit inventory line items

>   If you are using landed costs, you can use the Match Shipments to Invoice
>   window to match the landed costs that you’ve entered in the Purchasing
>   Invoice Entry window to one or more in-transit inventory items. All the
>   in-transit inventory items that are available to match to the landed cost
>   IDs are displayed in the Match Shipments to Invoice window. Landed costs
>   aren’t automatically matched. To match the landed costs to in-transit
>   inventory items, the landed costs must be set up to invoice match. You can
>   mark the landed costs to match when entering landed costs using the
>   Receivings Landed Cost Apportionment window or the Receivings Landed Cost
>   Entry window. You must be keeping receipt history to match landed costs.

>   **To match landed costs to in-transit inventory line items:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter the receipt number, vendor document number, invoice date, and vendor
    ID assigned to the landed cost ID.

2.  Mark the LC option and enter a landed cost ID as an item.

3.  Choose the Match Shipments to Invoice expansion button to open the Match
    Shipments to Invoice window.

4.  Mark the Match option for the in-transit inventory line items you want to
    match to the landed cost item entered on the invoice.

5.  To quickly match all line items for an in-transit inventory receipt to the
    landed cost entered on the invoice, choose the Match Options button to open
    the Match Options window. You can match the selected landed cost to the
    items on the intransit inventory receipt by receipt number.

6.  Mark Revalue IV if you want to have purchase receipts revalued if the cost
    variance for a matched invoice is greater than the tolerance percentage.

7.  Verify or change the default price variance posting account (optional).

8.  Choose OK to save your changes and to close the Match Shipments to Invoice
    window.

230 P U R C H A S E O R D E R P R O C E S S I N G

**Chapter 20: Taxes for receipts**

>   Purchases tax can be calculated, modified, and distributed in Purchase Order

>   Processing. Use the Receivings Tax Summary Entry window or the Purchasing
>   Invoice Tax Summary Entry window to change tax distributions for receipts,
>   if your system is set up to allow editing summary-level taxes. To change tax
>   details or the amounts distributed to tax details for individual line items,
>   use the Receivings Line Item Tax Detail Entry window or the Purchasing
>   Invoice Line Item Tax Detail Entry window. For more information about tax
>   calculations, see *Tax calculations in Purchase Order Processing*.

>   This information is divided into the following sections:

-   *Default tax schedules for shipment/invoices*

-   *Tax schedules for shipment/invoice items*

-   *Calculating and distributing summary taxes for shipment/invoice receipts*

-   *Calculating and distributing detail taxes for shipment/invoice line items*

-   *Default tax schedules for invoices*

-   *Tax schedules for invoice items*

-   *Calculating and distributing summary taxes for invoice receipts*

-   *Calculating and distributing detail taxes for invoice line items*

#### Default tax schedules for shipment/invoices

>   Where the exchange of goods takes place is based on the shipping method
>   assigned to the vendor’s purchase address. The default schedule for the
>   shipment/invoice and the default schedule to compare against the item are
>   selected based on the shipping method. Refer to the following table for the
>   default tax schedule for a shipment/invoice.

| **Tax calculation option** | **Shipping method** | **Default tax schedule**                                                                                        | **Label name**      |
|----------------------------|---------------------|-----------------------------------------------------------------------------------------------------------------|---------------------|
| Advanced                   | Pickup              | Tax schedule assigned to the vendor’s purchase address                                                          | Purch Addr Tax      |
| Advanced                   | No shipping method  | Tax schedule assigned to the vendor’s purchase address                                                          | Purch Addr Tax      |
| Advanced                   | Delivery            | Purchases tax schedule assigned in the Company                                                                  | Company Tax Sched   |
| Single schedule            | Not applicable      | Tax schedule assigned as the single schedule tax schedule in the Purchase Order Processing Setup Options window | Single Tax Schedule |

>   Sched

>   Sched

>   Setup window

>   ID

>   *If you decided not to use the shipping method to determine the default tax
>   schedule and decided to use the advanced tax calculations method, the tax
>   schedule assigned to the vendor’s purchase address will be the default tax
>   schedule.*

#### Tax schedules for shipment/invoice items

>   To calculate tax for an item, the tax schedules assigned to the item are
>   compared. The item’s default tax schedule is as follows:

| **Item**                                                     | **Default tax schedule**                                                                             |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Item is assigned to a purchase order                         | Tax schedule assigned to the item on the purchase order                                              |
| Inventoried item that isn’t assigned to a purchase order     | Purchase tax schedule assigned to the item in the Item Maintenance window                            |
| Non-inventoried item that isn’t assigned to a purchase order | Tax schedule assigned to non-inventoried items in the Purchase Order Processing Setup Options window |

>   The default tax schedule to mask against the item’s tax schedule is as
>   follows:

| **Tax calculation option** | **Purchase order assigned** | **Shipping method** | **Inventory** |
|----------------------------|-----------------------------|---------------------|---------------|


>   **Control**

**Default tax schedule**

**Label name**

| Advanced        | Yes            | Not applicable     | Not applicable | Tax schedule from the purchase order                                      | Purch Addr Tax Sched |   |
|-----------------|----------------|--------------------|----------------|---------------------------------------------------------------------------|----------------------|---|
| Advanced        | No             | No shipping method | Not applicable | Tax schedule assigned to the shipment/invoice                             | Purch Addr Tax Sched |   |
| Advanced        | No             | Pickup             | Not applicable | Tax schedule assigned to the shipment/invoice                             | Purch Addr Tax Sched |   |
| Advanced        | No             | Delivery           | Registered     | Purchase tax schedule assigned to the site                                | Site Tax Schedule ID |   |
| Advanced        | No             | Delivery           | Not registered | Purchases tax schedule assigned in the Company                            | Company Tax Sched    |   |
| Single schedule | Not applicable | Not applicable     | Not applicable | Tax schedule assigned as the single schedule tax schedule in the Purchase | Single Tax Schedule  |   |

>   Setup window

>   Order Processing Setup

>   Options window

>   ID

>   *If you decided not to use the shipping method to determine the default tax
>   schedule and decided to use the advanced tax calculations method, the tax
>   schedule assigned to the vendor’s purchase address will be the default tax
>   schedule.*

#### Calculating and distributing summary taxes for shipment/invoice receipts

>   Use the Receivings Tax Summary Entry window to add, change, delete, or view
>   summarized tax amounts for a shipment/invoice, as well as the accounts to
>   which the amounts will be posted. Taxes are calculated automatically as you
>   enter each tax detail or edit the Total Purchases amount. Summary tax edits
>   won’t change the taxes calculated for each line item in the Receivings Line
>   Item Tax Detail Entry window.

>   If your system isn’t set up to allow editing summary-level taxes, you can’t
>   change the Tax amount in the Receivings Transaction Entry window or the tax
>   information in the Receivings Tax Summary Entry window, except for the
>   account. You’ll be able to change the account for tax included in item taxes
>   at the summary level regardless of how your system is set up. If you want to
>   change tax information, use the Receivings Line Item Tax Detail Entry
>   window. For more information about the setup option to make summary edits to
>   taxes, refer to your System Setup instructions (Help \>\> Contents \>\>
>   select Setting Up the System).

>   If you are using Project Accounting, you can't change the Tax amount in the

>   Receivings Transaction Entry window or the tax information in the Receivings
>   Tax Summary Entry window even if your system is set up to allow editing
>   summarylevel taxes. If you want to change tax information, use the
>   Receivings Line Item Tax Detail Entry window.

>   **To calculate and distribute summary taxes for shipment/ invoice
>   receipts:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment/invoice. Tax information cannot be entered for
    shipment receipts.

2.  Enter document information, including receipt number, vendor document
    number, and receipt date.

>   Choose the Date expansion button to open the Receivings Date Entry window,
>   where you can enter a tax date and posting date that differ from the
>   document date. The tax date you enter is the date your tax records are
>   updated.

1.  Receive items.

    -   Choose Auto-Rcv to open the Select Purchase Order window, where you can
        select a purchase order to receive items from.

    -   Enter or select a vendor ID and choose Auto-Rcv to open the Select
        Purchase Order Items window, where you can receive line items on
        multiple purchase orders.

    -   Enter or select a vendor ID and enter line item information.

2.  To change the tax status, tax schedules, or tax amount for an item, choose
    the Item or Vendor Item expansion button to open the Receivings Item Detail
    Entry window.

3.  Enter total information in the Receivings Transaction Entry window.

4.  Choose the Tax expansion button to open the Receivings Tax Summary Entry
    window, where you can view or edit the tax distribution amounts.

![](media/b7f153b632865cbff8e362923ecd4d6b.jpg)

>   Currency amounts in this window may be displayed in the functional or
>   originating currency, depending on the view selected in the Receivings
>   Transaction Entry window.

1.  To edit tax information, enter a tax detail ID, a tax amount, total
    purchases, or select a new account. (The tax amount for the detail will be
    posted to the account.)

2.  To distribute tax to multiple tax details, change the default amount in the
    scrolling window and enter or select another tax detail and tax amount in
    the next available line.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row.

1.  Choose OK to save your entries and return to the Receivings Transaction
    Entry window.

>   If there is a difference between the total tax amount distributed to tax
>   details and the tax amount entered in the Receivings Transaction Entry
>   window, the tax amount will be adjusted to match the total tax amount.

>   Choose Delete to delete the tax information in the Receivings Tax Summary
>   Entry window.

>   Choose Default to restore the default tax information.

#### Calculating and distributing detail taxes for shipment/ invoice line items

>   Use the Receivings Line Item Tax Detail Entry window to add, change, delete,
>   or view tax amounts calculated on an individual line item. Taxes are
>   calculated automatically as you enter each tax detail or edit the Total
>   Purchases amount. Summary tax edits won’t change the taxes calculated for
>   each line item in the

>   Receivings Line Item Tax Detail Entry window. Tax edits made for each line
>   item

>   will change the summary tax amounts in the Receivings Tax Summary Entry
>   window.

>   **To calculate and distribute detail taxes for shipment/ invoice line
>   items:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select a shipment/invoice. Tax information cannot be entered for
    shipment receipts.

2.  Enter document information, including receipt number, vendor document
    number, and receipt date.

3.  Receive items.

    -   Choose Auto-Rcv to open the Select Purchase Order window, where you can
        select a purchase order to receive items from.

    -   Enter or select a vendor ID and choose Auto-Rcv to open the Select
        Purchase Order Items window, where you can receive line items on
        multiple purchase orders.

    -   Enter or select a vendor ID and enter line item information.

4.  Select a line item and choose the Vendor Item or Item expansion button to
    open the Receivings Item Detail Entry window. You can change the tax status,
    tax schedules, or tax amount for an item.

5.  Choose the Calculated Tax expansion button to open the Receivings Line Item
    Tax Detail Entry window, where you can view or edit tax distribution
    amounts.

![](media/9af06e72dcf76ad7dfdb3c461d3ffca7.jpg)

1.  To edit tax information, enter a tax detail ID, total purchases, or tax
    amount.

>   (The tax amount for the detail will be posted to the account.)

1.  To distribute tax to multiple tax details, change the default amount in the
    scrolling window and enter or select another tax detail and tax amount in
    the next available line.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row.

1.  Choose OK to save your entries and return to the Receivings Item Detail
    Entry window.

>   If there is a difference between the total tax amount distributed to tax
>   details and the tax amount entered in the Receivings Transaction Entry
>   window, the tax amount will be adjusted to match the total tax amount.

>   Choose Delete to delete all the tax details.

>   Choose Default to restore the default tax information.

#### Default tax schedules for invoices

>   Where the exchange of goods takes place is based on the shipping method
>   assigned to the vendor’s purchase address. The default schedule for the
>   invoice and the default schedule to compare against the item are selected
>   based on the shipping method. Refer to the following table for the default
>   tax schedule for an invoice.

| **Tax calculation option** | **Shipping method** | **Default tax schedule**                                                        | **Label name**         |
|----------------------------|---------------------|---------------------------------------------------------------------------------|------------------------|
| Advanced                   | Pickup              | Tax schedule assigned to the vendor’s purchase address                          | Purch Addr Tax Sched   |
| Advanced                   | No shipping method  | Tax schedule assigned to the vendor’s purchase address                          | Purch Addr Tax Sched   |
| Advanced                   | Delivery            | Purchases tax schedule assigned in the Company Setup window                     | Company Tax Sched      |
| Single schedule            | Not applicable      | Tax schedule assigned as the single schedule tax schedule in the Purchase Order | Single Tax Schedule ID |

>   Processing Setup

>   Options window

>   *If you decided not to use the shipping method to determine the default tax
>   schedule and decided to use the advanced tax calculations method, the tax
>   schedule assigned to the vendor’s purchase address will be the default tax
>   schedule.*

#### Tax schedules for invoice items

>   To calculate tax for an item, the tax schedules assigned to the item are
>   compared. The item’s default tax schedule is as follows:

| **Item**                                                     | **Default tax schedule**                                                                             |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Item is assigned to a purchase order                         | Tax schedule assigned to the item on the purchase order                                              |
| Inventoried item that isn’t assigned to a purchase order     | Purchase tax schedule assigned to the item in the Item Maintenance window                            |
| Non-inventoried item that isn’t assigned to a purchase order | Tax schedule assigned to non-inventoried items in the Purchase Order Processing Setup Options window |

>   The default tax schedule to mask against the item’s tax schedule is as
>   follows:

| **Tax calculation option** | **Purchase order assigned** | **Shipping method** | **Default tax schedule**                                                                   | **Label name**         |
|----------------------------|-----------------------------|---------------------|--------------------------------------------------------------------------------------------|------------------------|
| Advanced                   | Yes                         | Not applicable      | Tax schedule from the purchase order                                                       |                        |
| Advanced                   | No                          | No shipping method  | Tax schedule assigned to the invoice                                                       | Purch Addr Tax Sched   |
| Advanced                   | No                          | Pickup              | Tax schedule assigned to the invoice                                                       | Purch Addr Tax Sched   |
| Advanced                   | No                          | Delivery            | Purchases tax schedule assigned in the Company                                             | Company Tax Sched      |
| Single schedule            | Not applicable              | Not applicable      | Tax schedule assigned as the single schedule tax schedule in the Purchase Order Processing | Single Tax Schedule ID |

>   Setup window

>   Setup Options window

>   *If you decided not to use the shipping method to determine the default tax
>   schedule and decided to use the advanced tax calculations method, the tax
>   schedule assigned to the vendor’s purchase address will be the default tax
>   schedule.*

#### Calculating and distributing summary taxes for invoice receipts

>   Use the Purchasing Invoice Tax Summary Entry window to add, change, delete,
>   or view summarized tax amounts for an invoice, as well as the accounts to
>   which the amounts will be posted. Taxes are calculated automatically as you
>   enter each tax detail or edit the Total Purchases amount. Summary tax edits
>   won’t change the taxes calculated for each line item in the Purchasing
>   Invoice Line Item Tax Detail Entry window.

>   If your system isn’t set up to allow editing summary-level taxes, you can’t
>   change the Tax amount in the Purchasing Invoice Entry window or the tax
>   information in the Purchasing Invoice Tax Summary Entry window, except for
>   the account. You’ll be able to change the account for tax included in item
>   taxes at the summary level regardless of how your system is set up. If you
>   want to change tax information, use the Purchasing Invoice Line Item Tax
>   Detail Entry window. For more information on the setup option to make
>   summary edits to taxes, refer to your System Setup instructions (Help \>\>
>   Contents \>\> select Setting Up the System).

>   If you are using Project Accounting, you can't change the Tax amount in the

>   Purchasing Invoice Entry window or the tax information in the Purchasing
>   Invoice Tax Summary Entry window even if your system is set up to allow
>   editing summary-level taxes. If you want to change tax information, use the
>   Purchasing Invoice Line Item Tax Detail Entry window.

>   **To calculate and distribute summary taxes for invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter document information, including receipt number, vendor document
    number, and invoice date.

>   Choose the Invoice Date expansion button to open the Purchasing Invoice Date
>   Entry window, where you can enter a tax date and posting date that differ
>   from the document date. The tax date you enter is the date your tax records
>   are updated.

1.  Invoice items.

-   Choose Auto-Invoice to open the Select Purchase Order window, where you can
    automatically invoice all shipment line items available for an invoice.

-   Enter or select a vendor ID and choose Auto-Invoice to open the Select
    Purchase Order Items window, where you can invoice line items that have been
    received from multiple purchase orders.

-   Enter or select a vendor ID and enter line item information.

1.  Select a line item and choose the Vendor Item or Item expansion button to
    open the Purchasing Invoice Item Tax Entry window. You can change the tax
    status, tax schedules, or tax amount for an item.

2.  Enter total information in the Purchasing Invoice Entry window.

3.  Choose the Tax expansion button to open the Purchasing Invoice Tax Summary
    Entry window, where you can view or edit the tax distribution amounts.

![](media/f887252a61374019d436e6d5bf58d613.jpg)

>   Currency amounts in this window may be displayed in the functional or
>   originating currency, depending on the view selected in the Purchasing
>   Invoice Entry window.

1.  To edit tax information, enter a tax detail ID, a tax amount, total
    purchases, or select a new account. (The tax amount for the detail will be
    posted to the account.)

2.  To distribute tax to multiple tax details, change the default amount in the
    scrolling window and enter or select another tax detail and tax amount in
    the next available line.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row.

1.  Choose OK to save your entries and return to the Purchasing Invoice Entry
    window.

>   If there is a difference between the total tax amount distributed to tax
>   details and the tax amount entered in the Purchasing Invoice Entry window,
>   the tax amount will be adjusted to match the total tax amount.

>   Choose Delete to delete the tax information.

>   Choose Default to restore the default tax information.

#### Calculating and distributing detail taxes for invoice line items

>   Use the Purchasing Invoice Line Item Tax Detail Entry window to add, change,
>   delete, or view tax amounts calculated on an individual line item. Taxes are
>   calculated automatically as you enter each tax detail or edit the Total
>   Purchases amount. Summary tax edits won’t change the taxes calculated for
>   each line item in the Purchasing Invoice Line Item Tax Detail Entry window.
>   Tax edits made for each line item will change the summary tax amounts in the
>   Purchasing Invoice Tax Summary Entry window.

>   **To calculate and distribute detail taxes for invoice line items:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter document information, including receipt number, vendor document
    number, and invoice date.

>   Choose the Invoice Date expansion button to open the Purchasing Invoice Date
>   Entry window, where you can enter a tax date and posting date that differ
>   from the document date. The tax date you enter is the date your tax records
>   are updated.

1.  Invoice items.

    -   Choose Auto-Invoice to open the Select Purchase Order window, where you
        can automatically invoice all shipment line items available for an
        invoice.

    -   Enter or select a vendor ID and choose Auto-Invoice to open the Select
        Purchase Order Items window, where you can invoice line items that have
        been received from multiple purchase orders.

    -   Enter or select a vendor ID and enter line item information.

2.  Select a line item and choose the Vendor Item or Item expansion button to
    open the Purchasing Invoice Item Tax Detail Entry window. You can change the
    tax status, tax schedules, or tax amount for an item.

3.  Choose the Calculated Tax expansion button to open the Purchasing Invoice
    Line Item Tax Detail Entry window, where you can view or edit the tax
    amounts.

![](media/441dd82fbc8e175fe2e8dac4e67dba07.jpg)

1.  To edit tax information, enter a tax detail ID, total purchases, or tax
    amount.

>   (The tax amount for the detail will be posted to the account.)

1.  To distribute tax to multiple tax details, change the default amount in the
    scrolling window and enter or select another tax detail and tax amount in
    the next available line.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row.

1.  Choose OK to save your entries and return to the Purchasing Invoice Item Tax
    Detail Entry window.

>   If there is a difference between the total tax amount distributed to tax
>   details and the tax amount entered in the Purchasing Invoice Entry window,
>   the tax amount will be adjusted to match the total tax amount.

>   Choose Delete to delete all the tax details.

>   Choose Default to restore the default tax information.

**Chapter 21: Receipt posting**

>   Posting is the process of transferring transactions to permanent records.
>   Until transactions are posted, they can be changed or deleted. After you
>   post transactions in Purchase Order Processing, they can’t be changed or
>   deleted. To print a posting journal after the transaction was posted, use
>   the Purchasing Posting Journals window or the Purchasing Posting Journal
>   Options window.

>   Posting reports will be printed when you post transactions, either
>   individually or in batches. For more information about posting reports for
>   Purchase Order Processing, refer to *Purchase Order Processing standard
>   reports summary*.

>   *For more information about setting up posting, see the System Setup Guide
>   (Help \>\> Contents \>\> select Setting up the System).*

>   This information is divided into the following sections:

-   *Posting a receipt*

-   *Posting a purchasing batch*

-   *Posting Purchasing series batches*

#### Posting a receipt

>   Transaction-level posting allows you to enter and post transactions
>   individually without ever having to create a batch. Purchasing receipt
>   information always will be up-to-date immediately when you post using this
>   method, because transactions must be posted or deleted immediately. They
>   can’t be saved or posted later.

>   You can perform transaction-level posting in the Receivings Transaction
>   Entry window and in the Purchasing Invoice Entry window. Purchasing and
>   inventory information will be update immediately every time you post using
>   this method. All transactions posted individually in a single data entry
>   session will have the same audit trail code.

>   Transaction-level posting is optional and can be selected in the Posting
>   Setup window when you set up Microsoft Dynamics GP. If you aren’t allowed to
>   post individual transactions, you’ll be asked to create a batch when you
>   attempt to post transactions. Also, you can post an individual transaction
>   that was previously entered in a batch. To do so, select the transaction
>   from the batch, clear the Batch ID field and post the transaction.

>   If you’re posting by transaction date, the posting date and the document
>   date will be the same. If you change the posting date in the date entry
>   window, the document date won’t be affected.

>   You can’t post to a year that hasn’t been set up using the Fiscal Periods
>   Setup window. Also, if the year has been set up but the Purchasing period is
>   closed, posting won’t be allowed. The posting journal will indicate the
>   transactions that were posted, as well as the transactions that weren’t
>   posted. Transactions will be posted to General Ledger, even if a Financial
>   series period has been closed. However, transactions will not post through
>   General Ledger.

>   The reports for individually posted transactions contain information only
>   for the transactions that were entered and posted since the Receivings
>   Transaction Entry window or the Purchasing Invoice Entry window was opened.
>   These reports are printed when you close the window.

#### Posting a purchasing batch

>   Use the Purchasing Batch Entry window to post a single batch. Before you
>   post, be sure quantities for each item on an invoice receipt are fully
>   matched to shipment quantities.

>   **To post a purchasing batch:**

1.  Make a backup of your company’s data. Refer your System Administrator's
    Guide (Help \>\> Contents \>\> select System Administration) for more
    information about making backups.

2.  Open the Purchasing Batch Entry window.

>   (Purchasing \>\> Transactions \>\> Purchasing Batches)

1.  Print an edit list to review the transactions in the batch. An edit list can
    be printed from the Purchasing Batch Entry window by choosing File \>\>
    Print with the appropriate batch ID displayed. If you need to make
    corrections, do so at this time.

2.  Enter or select the batch ID and origin for the batch you want to post.

3.  Choose Post. Your Purchase Order Processing records will be updated to
    reflect the information from the transactions. Your General Ledger accounts
    will be updated depending on your posting setup selections.

>   If you’re set up to post to General Ledger in the Posting Setup window, the
>   batch appears in the Financial Series Posting and Master Posting windows;
>   you can edit the transactions in the General Ledger Transaction Entry window
>   before posting them again. Your accounts are updated when you post the
>   transactions in General Ledger.

>   If you post through General Ledger, your accounts are updated at once and
>   you don’t need to post the batch again in General Ledger.

1.  One or more posting journals may be printed, depending on the options
    selected in the Posting Setup window. A Report Destination window may appear
    for each posting journal that was selected to print, depending on how they
    were set up.

#### Posting Purchasing series batches

>   Use the Purchasing Series Posting window to post multiple batches in the
>   Purchasing series at the same time. Before you post, be sure quantities for
>   each item on an invoice receipt are fully matched to shipment quantities.

>   **To post Purchasing series batches:**

1.  Make a backup of your company’s data. Refer your System Administrator’s
    Guide (Help \>\> Contents \>\> select System Administration) for more
    information about making backups.

2.  Print an edit list to review the transactions in the batch. An edit list can
    be printed from the Purchasing Batch Entry window by choosing File \>\>
    Print with the appropriate batch ID displayed. If you need to make
    corrections, do so at this time.

3.  Open the Purchasing Series Posting window. (Purchasing \>\> Transactions
    \>\> Series Post)

![](media/949b59359284915a3d071faeb8de3821.jpg)

1.  Mark the box next to the batch ID for each batch you want to post. The
    status changes to Marked, which indicates to other users that the batch is
    ready to be posted.

>   *If a batch was marked previously, the User ID column identifies the person
>   who marked it. If you want to post that batch, unmark it and mark it again
>   so the batch is assigned to you. Series posting allows you to post only
>   those batches that you’ve marked; you can’t post batches marked by another
>   user.*

1.  Choose Post. One or more posting journals may be printed, depending on the
    options selected in the Posting Setup window. A Report Destination window
    may appear for each posting journal that was selected to print, depending on
    how they were set up.

244 P U R C H A S E O R D E R P R O C E S S I N G

**Chapter 22: Receipt maintenance**

>   Proper maintenance of your receiving information is essential for preserving
>   the accuracy of your records. This chapter focuses on the tasks that allow
>   you to maintain your records effectively.

>   Throughout the receiving process, you can print a variety of reports you can
>   use to double-check documents you’ve entered. If you identify errors on
>   these reports, the errors must be corrected to ensure accurate reporting of
>   your receiving activity. You also may want to delete or void shipment,
>   shipment/invoice and invoice receipts that are no longer valid.

>   If you are using Purchase Order Enhancements, you can process returns
>   against Purchase Order Processing receipts. Items that have been received on
>   a shipment or shipment/invoice receipt can be returned as a Return or a
>   Return w/Credit document type. For more information, see the Purchase Order
>   Enhancements documentation.

>   This information is divided into the following sections:

-   *Correcting unposted shipment, shipment/invoice, and in-transit inventory
    receipts*

-   *Correcting unposted invoice receipts*

-   *About deleting and voiding receipts*

-   *Deleting shipment, shipment/invoice, or in-transit inventory receipts*

-   *Voiding shipment, shipment/invoice, or in-transit inventory receipts*

-   *Deleting invoice receipts*

-   *Voiding invoice receipts*

#### Correcting unposted shipment, shipment/invoice, and in-transit inventory receipts

>   Use the Receivings Transaction Entry window to correct shipment, shipment/
>   invoice, or in-transit inventory receipts before posting. After you enter
>   receipts, print an edit list to determine if the entries contain errors.
>   (You can print edit lists only for receipts entered in a batch.) If you
>   discover that an unposted receipt was entered incorrectly, you can correct
>   the error using the following procedure.

>   **To correct unposted shipment, shipment/invoice, and intransit inventory
>   receipts:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Select the receipt. (You can find the receipt number on the Receivings Edit
    List you used to pinpoint the error.)

2.  Highlight the fields you want to change and enter the correct information.

>   • If you changed a quantity shipped or quantity rejected for a lot-numbered
>   item or a serial-numbered item, the Purchasing Lot Number Entry window or
>   the Purchasing Serial Number Entry window will open; you can assign lot or
>   serial numbers to the item. The In-Transit Serial Number Entry window or the
>   In-Transit Lot Number Entry window opens for an in-transit inventory
>   receipt, where you can assign lot or serial numbers to an item.

**P A R T 3** R E C E I P T S

-   If receiving items without a purchase order is allowed, you can enter items,
    non-inventoried items or vendor items that don’t exist on the purchase
    order. If you are using Project Accounting, you can’t enter vendor items for
    projects.

-   If you delete an item when you are using landed costs, all line and
    apportioned landed costs assigned to the item also are deleted. Deleting an
    item that has apportioned landed costs will cause the unapportioned amount
    and the document’s landed cost functional total to recalculate.

1.  Choose File \>\> Print to verify the corrections you’ve entered with a
    Receivings Edit List.

2.  Choose Save to save the corrected transaction.

#### Correcting unposted invoice receipts

Use the Purchasing Invoice Entry window to correct invoice receipts before
posting. After you enter receipts, print an edit list to determine if the
entries contain errors. (You can print edit lists only for receipts entered in a
batch.) If you discover that an unposted receipt was entered incorrectly, you
can correct the error using the following procedure.

>   **To correct unposted invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Select the receipt. (You can find the receipt number on the Purchasing
    Invoice Edit List you used to pinpoint the error.)

2.  Highlight the fields you want to change and enter the correct information.

    -   If receiving items without a purchase order is allowed, you can enter
        items, non-inventoried items, or vendor items that don’t exist on the
        purchase order as long as those items or vendor items are on a shipment
        that has been posted. If you are using Project Accounting, you can’t
        enter vendor items for projects.

    -   You can match or unmatch shipment line items to invoices. You also can
        match or unmatch landed cost items.

3.  Choose File \>\> Print to verify the corrections you’ve entered with a
    Purchasing Invoice Edit List.

4.  Choose Save to save the corrected transaction.

#### About deleting and voiding receipts

Deleting and voiding receipts reduces the following quantities in the Purchasing
Quantity Status window:

-   Unposted shipment

-   Unposted invoice

-   Unposted rejected quantities

-   Unposted matched quantities

>   **C H A P T E R 2 2** R E C E I P T M A I N T E N A N C E

>   Deleting and voiding receipts increases the following quantities in the
>   Purchasing Quantity Status window:

-   Remaining to ship quantity. (This quantity will be increased by the quantity
    shipped minus the quantity rejected. The remaining to ship quantity is the
    remaining to receive quantity for in-transit inventory receipts.)

-   Remaining to invoice quantities. (These quantities will be increased by the
    quantity invoiced.)

-   Remaining posted shipments to match quantities. (These quantities will be
    increased by the quantity invoiced when you void or delete an unposted
    invoice receipt.)

#### Deleting shipment, shipment/invoice, or in-transit inventory receipts

>   Use the Receivings Transaction Entry window to delete unposted shipment.
>   shipment/invoice, or in-transit inventory receipts. Deleting removes receipt
>   information from the system and makes receipt numbers available for reuse.

>   To delete receipts or line items linked to jobs, you must have authority to
>   unlink line items from a job. Security is set in the Job Costing Preference
>   Defaults window. You can’t link line item jobs to in-transit inventory
>   receipts. If you are using Project Accounting, you can’t link line items to
>   jobs.

>   **To delete shipment, shipment/invoice, or in-transit inventory receipts:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry) 2. Enter or
>   select the receipt number of the receipt you want to delete.

1.  Choose Delete.

#### Voiding shipment, shipment/invoice, or in-transit inventory receipts

>   Use the Receivings Transaction Entry window to void unposted shipment,
>   shipment/invoice, and in-transit inventory receipts. Voiding moves receipt
>   information to history and does not make receipt numbers available for reuse
>   until history is removed, if you’re keeping history. If you’re not keeping
>   history, voiding removes receipt information from the system.

>   If you track voided receipts, you’ll know why a receipt number is missing or
>   out of sequence. If you’ve selected to track receipts in history, you can
>   view information about voided receipts using the purchasing inquiry windows
>   or by printing the Receivings Voided Journal or the Receivings Transaction
>   History Report.

>   To void receipts or line items linked to jobs, you must have authority to
>   unlink line items from a job. Security is set in the Job Costing Preference
>   Defaults window. You can’t link line item jobs to in-transit inventory
>   receipts. If you are using Project Accounting, you can’t link line items to
>   jobs.

**P A R T 3** R E C E I P T S

**To void shipment, shipment/invoice, or in-transit inventory receipts:**

1.  Open the Receivings Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Receivings Transaction Entry)

1.  Enter or select the receipt number of the receipt you want to void.

2.  Choose Void. The Receivings Voided Journal is printed when you close the
    Receivings Transaction Entry window after voiding, if you’ve marked the
    option to print it in the Posting Setup window.

#### Deleting invoice receipts

Use the Purchasing Invoice Entry window to delete unposted invoice receipts.
Deleting removes receipt information from the system and makes receipt numbers
available for reuse.

To delete invoice receipts or line items linked to jobs, you must have authority
to unlink line items from a job. Security is set in the Job Costing Preference
Defaults window. If you are using Project Accounting, you can’t link line items
to jobs.

>   **To delete invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select the receipt number of the receipt you want to delete.

2.  Choose Delete.

#### Voiding invoice receipts

Use the Purchasing Invoice Entry window to void unposted invoice receipts.

If you track voided receipts, you’ll know why a receipt number is missing or out
of sequence. If you’ve selected to track receipts in history, you can view
information about voided receipts using the purchasing inquiry windows or by
printing the Voided Invoice Journal or the Receivings Transaction History
Report.

To void invoice receipts or line items linked to jobs, you must have authority
to unlink line items from a job. Security is set in the Job Costing Preference
Defaults window. If you are using Project Accounting, you can’t link line items
to jobs.

**To void invoice receipts:**

1.  Open the Purchasing Invoice Entry window.

>   (Purchasing \>\> Transactions \>\> Enter/Match Invoices)

1.  Enter or select the receipt number of the receipt you want to void.

2.  Choose Void. The Voided Invoice Journal is printed when you close the
    Purchasing Invoice Entry window after voiding invoice receipts, if you’ve
    marked the option to print it in the Posting Setup window.

**Part 4: Purchase order returns**

>   This part of the documentation includes information about using purchase
>   order returns. The following topics are discussed:

-   *Chapter 23, “Returns transactions,”* describes how to process returns from
    Purchase Order Processing.

-   *Chapter 24, “Taxes for returns,”* contains information about tax
    calculation in purchase order returns.

**Chapter 23: Returns transactions**

>   Returning goods to vendors is a common event during the purchase order life
>   cycle. Returns can occur anytime—before or after receipt of the vendor’s
>   invoice—and returns may or may not involve credit. purchase order returns
>   makes it possible for you to process purchase order returns quickly and
>   easily, with or without credit to the vendor, based on the specific
>   circumstances of that return.

>   *You will have to make a manual adjustment within Payables Management for
>   restocking fees charged by the vendor. This release of purchase order
>   returns does not include a field for these fees.*

>   You can start to use purchase order returns immediately. No special setup is
>   necessary.

>   Purchase order returns transaction information is divided into the following
>   sections:

-   *About purchase order returns*

-   *Purchase order returns and Project Accounting*

-   *Return transaction document types*

-   *Quantity Tolerances for purchase order returns*

-   *Creating a purchasing returns batch*

| **Module**                | **Receipt types** |
|---------------------------|-------------------|
| Purchase Order Processing | Shipment          |
|                           | Shipment Invoice  |

-   *Processing purchasing return transactions*

-   *Processing project return-from-inventory transactions*

-   *Printing purchasing returns transactions*

-   *Entering detail information for a return*

-   *Entering Intrastat trade statistics for returns*

-   *Multiple bins in purchase order returns*

-   *Changing bins for a return transaction*

-   *Assigning lot numbers to a return*

-   *Assigning serial numbers to a return*

-   *Distributing return transaction amounts*

-   *Return distribution accounts*

-   *Processing manual adjustments for returns when closing purchase order
    lines*

#### About purchase order returns

>   You can process returns against both Purchase Order Processing receipts and
>   Inventory receipts. Items that have been received on a shipment or shipment/
>   invoice receipt are available to be returned as a Return or a Return
>   w/Credit document type. Items that have been transferred to another site,
>   added to inventory through an inventory adjustment or variance, or returned
>   by a customer are available to be returned in Purchase Order Processing as
>   an Inventory or Inventory w/Credit document type.

>   Using purchase order approvals, you can process returns against the
>   following receipt types:

| **Module**        | **Receipt types** |
|-------------------|-------------------|
| Inventory Control | Adjustment        |
|                   | Variance          |
|                   | Transfer          |
|                   | Sales return      |

>   When you post a return, the original transaction amount is offset against
>   quantities in inventory and the applicable General Ledger accounts. If the
>   unit cost of the item has changed, you can return at the new unit cost
>   (applicable to returns with credit only). If you are using Multicurrency
>   Management, you can return items involving alternative currencies.

>   When you process a Return w/Credit return document, a return transaction is
>   created in Payables Management. The return transaction must be manually
>   applied to the invoice from the vendor. See the Payables Management
>   documentation (Help \>\> Printable Manuals) for more information.

#### Purchase order returns and Project Accounting

>   If you are using Project Accounting, you can enter project information on
>   standard purchase orders and drop-ship purchase orders in Purchase Order
>   Processing. Items received from a standard purchase order are stored in
>   inventory. To transfer items to a project, you’ll use the Inventory Transfer
>   Entry window in Projecting Accounting. Items from a drop-ship purchase order
>   are invoiced and transferred to a project automatically.

>   You can use purchase order returns to return an item that is in inventory.
>   This is called a project return-from inventory transaction. If the item has
>   been transferred to a project, you can use Project Accounting to return the
>   item. See the Project Accounting documentation for more information.

#### Return transaction document types

>   You can process purchasing returns using the following return transaction
>   document types:

-   Return

-   Return w/Credit

-   Inventory

-   Inventory w/Credit

>   *You must use the document types Return or Return w/Credit to return
>   non-inventoried items or any items with the item types of Misc Charges, Flat
>   Fee, or Services. Returns against kit items are not allowed.*

>   Each of the return document types is described in detail as follows.

>   **Return**

>   Select Return for shipment receipts or shipment/invoice receipts when the
>   item is not matched to an invoice and vendor credit is not applicable. An
>   example would be when the item is being replaced.

>   Manual adjustments may be necessary for return documents using the Return
>   document type, refer to *Processing manual adjustments for returns when
>   closing purchase order lines* for more information.

>   **Return w/Credit**

>   Select Return w/Credit for shipment receipts that are matched with an
>   invoice, or shipment/invoice receipts when vendor credit is applicable.

>   *To return all of the items on a partially invoiced receipt, you must
>   complete two return transactions: one for the invoiced items using document
>   type Return w/Credit and another for the uninvoiced items using document
>   type Return.*

>   **Inventory**

>   Select Inventory for inventory adjustment receipts, variance receipts,
>   transfer receipts and sales return receipts when the item is not matched to
>   an invoice and vendor credit is not applicable. An example would be when the
>   item is being replaced. If you are using Project Accounting, you can’t enter
>   this return document type for project return-from-inventory transactions.

>   When you process an Inventory return, if the items being returned will be
>   replaced by the vendor, you must make adjusting journal entries to remove
>   the accrual created by the new shipment receipt.

>   **Inventory w/Credit**

>   Select Inventory w/Credit for inventory adjustment receipts, variance
>   receipts, transfer receipts and sales return receipts when vendor credit is
>   applicable. If you are using Project Accounting, you can’t enter this return
>   document type for project return-from-inventory transactions.

>   When you process a Return w/Credit return document or Inventory w/Credit
>   return document type, a return transaction is created in Payables
>   Management. The return transaction must be manually applied to the invoice
>   from the vendor. See the Payables Management documentation (Help \>\>
>   Printable Manuals) for more information.

#### Quantity Tolerances for purchase order returns

>   You set up quantity tolerances for shortages and overages for the quantity
>   ordered on a standard purchase order or a blanket purchase order. Review the
>   following information on how returning and replacing quantities affect the
>   calculation when determining if a quantity is within the tolerance set up
>   for an item.

>   **Shortage**

>   If an item's quantity is returned or partially returned, the option to
>   replace quantities on the transaction is taken into account when determining
>   if the quantity is within the tolerance amount and whether the line item
>   status is Received or Closed. The return quantity is not taken into account
>   when calculating the shortage tolerance.

>   **Example 1**

>   In the following example, the quantity returned is not replaced.

| Quantity ordered for a purchase order is 100.                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                                                                                        |
| You enter a receivings transaction for a quantity of 80.                                                                                                                             |
| The purchase order has a Released status.                                                                                                                                            |
| Return a quantity of 20 and do not replace the quantity.                                                                                                                             |
| The purchase order and the line item has a Released status.                                                                                                                          |
| You enter another receivings transaction.                                                                                                                                            |
| If the quantity for the item has a quantity of 9 or less, the line item status is Released.                                                                                          |
| If the quantity for the item has a quantity of 10 or more, the remaining quantity is canceled and the status for the item is Received or Closed if the item has been fully invoiced. |

>   **Example 2**

>   In the following example, the quantity returned is replaced.

| Quantity ordered for a purchase order is 100.                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quantity overage tolerance percentage is 10%.                                                                                                                                        |
| You enter a receivings transaction for a quantity of 80.                                                                                                                             |
| The purchase order has a Released status.                                                                                                                                            |
| Return a quantity of 20 and replace the quantity.                                                                                                                                    |
| You enter another receivings transaction.                                                                                                                                            |
| If the quantity for the item has a quantity of 29 or less, the line item status is Released.                                                                                         |
| If the quantity for the item has a quantity of 30 or more, the remaining quantity is canceled and the status for the item is Received or Closed if the item has been fully invoiced. |

>   **Overage**

>   If an item's quantity is returned or partially returned and the return has
>   been marked to replace returned items, the return quantity is taken into
>   account when calculating the overage tolerance. If the quantity received is
>   over the overage tolerance, the following message displays.

>   You can't enter a quantity greater than the combined total of the Remaining
>   to Receive quantity and the overage tolerance set up for the item.

>   **Example 1**

>   In the following example, the quantity returned is not replaced

| The net quantity order is the quantity order minus the quantity canceled.            |
|--------------------------------------------------------------------------------------|
| Purchase order net quantity is 100.                                                  |
| Quantity overage tolerance percentage is 10%.                                        |
| You enter a receivings transaction for a quantity of 80.                             |
| The purchase order has a Released status.                                            |
| Return a quantity of 20 and do not replace the quantity.                             |
| You enter another receivings transaction.                                            |
| No message displays if the quantity on the transaction has a quantity of 29 or less. |
| Message displays if the quantity on the transaction has a quantity of 30 or more.    |

>   **Example 2**

>   In the following example, the quantity returned is replaced.

| The net quantity order is the quantity order minus the quantity canceled.            |
|--------------------------------------------------------------------------------------|
| Purchase order net quantity is 100.                                                  |
| Quantity overage tolerance percentage is 10%.                                        |
| You enter a receivings transaction for a quantity of 80.                             |
| The purchase order has a Released status.                                            |
| Return a quantity of 20 and replace the quantity.                                    |
| You enter another receivings transaction.                                            |
| No message displays if the quantity on the transaction has a quantity of 49 or less. |
| Message displays if the quantity on the transaction has a quantity of 50 or more.    |

#### Creating a purchasing returns batch

>   Use the Returns Batch Entry window to create a return batch. All
>   transactions in the batch must originate with Returns Transaction Entry
>   window.

>   **To create a purchasing returns batch:**

1.  Open the Returns Batch Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Batches)

![](media/ae0bf66cec1dcf973ac904f6592fe619.jpg)

1.  Enter a batch ID to identify the batch.

2.  Enter a batch comment (optional).

3.  Enter a posting date.

>   This field is available only if Batch is selected in the Posting Date From
>   field in the Posting Setup window.

>   The posting date you enter here is the date that General Ledger files are
>   updated. Your records in Purchase Order Processing are updated based on the
>   date of the return.

1.  Choose Save to save the batch.

>   To verify the transactions you entered, print a returns Edit List. For more
>   information, see *Printing purchasing returns transactions*.

#### Processing purchasing return transactions

>   Use the Returns Transaction Entry window to process purchasing return
>   transactions.

>   If you’re using multiple bins and a default purchase returns bin exists at
>   either the item-site or the site, the quantity at the default bin will
>   decrease by the extended quantity for an item that is not tracked by serial
>   or lot numbers. You can modify the default bin selections. If a default
>   purchase returns bin doesn’t exist, you will be required to enter one. For
>   serial- and lot-numbered items, the purchase returns bin is the bin
>   associated with the serial or lot number, and you can’t to change the bin.

>   If you are using Project Accounting, the Project Number field and the Cost
>   Category ID field will be displayed in the Returns Transaction Entry window.
>   To enter a return for a project return-from-inventory transaction, see
>   *Processing project return from-inventory transactions*.

>   **To process purchasing return transactions:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    All Purchasing Transactions list.

2.  Select a shipment receipt or a shipment/invoice receipt.

3.  Choose Purchase Returns Transactions and then select a document type to open
    the Returns Transaction Entry window.

![](media/e8d8860f26df2daed44bf45318e162f8.jpg)

1.  Select a document type for the return transaction. For more information
    about return document types, see *Return transaction document types*

2.  Enter a return number or accept the default entry. The default entry will be
    the next available receipt number in the Purchase Order Processing Setup
    window.

3.  Enter a vendor document number. A vendor document number is required for
    returns with credit.

4.  Enter the return date. The user date is the default entry.

>   To enter a General Ledger posting date or a tax date that is different from
>   the return date, choose the Date expansion button; the Returns Date Entry
>   window will open.

>   For multicurrency transactions and for document types Return w/Credit,
>   Inventory, and Inventory w/Credit, the return document date determines the
>   exchange rate that will be used, based on the currency ID that’s entered for
>   the transaction and the associated rate type. For a Return document type,
>   the exchange rate of the original receipt will be assigned to each return
>   line. There is no overall exchange rate for the transaction.

1.  Enter or select a batch ID (optional). See *Creating a purchasing returns
    batch* for more information.

2.  Enter or select a vendor ID.

3.  Enter or accept the currency ID. The default currency ID will be the
    currency ID assigned to the vendor you selected. If no currency ID has been
    assigned for this vendor, the company’s functional currency will be used.

>   The currency ID assigned to the return must match the currency ID of the
>   receipts in the scrolling window.

>   If the selected currency ID is not the company’s functional currency, a rate
>   type and associated exchange rate table will be assigned to the transaction.
>   The rate type is based on the rate type assigned to the selected vendor. If
>   the vendor does not have a rate type assigned, the default rate type for the
>   Purchasing series specified in the Multicurrency Setup window is used.

>   For Return w/Credit, Inventory, and Inventory w/Credit returns, you can view
>   or modify the default exchange rate by choosing the currency ID expansion
>   button to open the Exchange Rate Entry window. For more information about
>   exchange rates, refer to the Multicurrency Management documentation.

1.  To select an option for how returned goods are invoiced, mark a combination
    of the Replace Returned Goods and Invoice Expected for Returned Goods
    fields.

>   The following table shows which options to choose.

| **Options marked**                                             | **When to use**                                                                                                                                                                                                                                                                       | **Results**                                                                                                                                                                                | **Notes**                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Replace Returned Goods and Invoice Expected for Returned Goods | When you want to replace the returned goods, using the original purchase order. When you have yet to process the invoice for the original goods. When you want to process an invoice for all of the original quantity of goods received (even though you have returned some of them). | Returned goods are replaced. The same purchase order is used for the replaced goods. You can process the invoice for all of the original goods, including the goods that will be replaced. | If the original purchase order is no longer available (for example, moved to history), a new one is created automatically. The new purchase order includes only the returned goods and quantity that you want to replace. The Invoice Expected from Vendor option is available only for return types Return or Inventory.                                                                    |
| Replace Returned Goods                                         | When you want to replace the returned goods, using the original purchase order. When you do not expect to receive an invoice for the goods you’re returning, or when you do not expect the invoice to match the original quantity of goods.                                           | Returned items are replaced. The same purchase order is used for the replaced items.                                                                                                       | You can process an invoice for only the goods you kept, not the returned goods. If the original purchase order is no longer available (for example, moved to history), a new one is created automatically. The new purchase order includes only the returned goods and quantity that you want to replace. Invoices that you already have processed are not affected by choosing this option. |
| **Options marked**                                             | **When to use**                                                                                                                                                                                                                                                                       | **Results**                                                                                                                                                                                | **Notes**                                                                                                                                                                                                                                                                                                                                                                                    |
| Invoice Expected for Returned Goods                            | When you do not want to replace the returned goods. For example, when you expect a refund or a credit. When you want to close the purchase order when the invoice is processed.                                                                                                       | The credit or refund occurs separately from the original invoice. When you process the invoice, the purchase order is automatically closed.                                                | You returned some goods, but did not ask to replace them. Thus, the transaction is complete and the purchase order is closed.                                                                                                                                                                                                                                                                |
| Neither option is marked                                       | When you do not want to replace the returned goods. For example, when you expect a refund or a credit. When you have already processed the invoice, or when you do not expect to receive an invoice from the vendor.                                                                  | The credit or refund occurs separately from the original invoice.                                                                                                                          | You can process an invoice for only the goods that you kept, not the returned goods. Invoices that you already have processed are not affected by choosing this option.                                                                                                                                                                                                                      |

1.  If the item being returned was purchased from an EU vendor, mark EU
    Transaction. See *Entering Intrastat trade statistics for returns* for more
    information.

2.  If the item being returned is subject to withholding tax, mark the Subject
    to Withholding option and enter or accept the tax rate. If a withholding
    vendor hasn’t been specified in the Company Setup Options window, these
    fields will not be available.

3.  Use the scrolling window to select the items to be returned and to match the
    items to receipts.

>   For document types Return or Return w/Credit, enter or select the purchase
>   order number applicable to this return. You can leave this field blank if
>   you prefer. All purchase orders that have been received for this vendor will
>   be available in the Purchase Orders lookup window.

>   The PO Number field is not available for document types Inventory and
>   Inventory w/Credit.

>   Only standard purchase orders that have been received can be returned. You
>   cannot process returns for drop-ship, canceled, or on-hold purchase orders.

1.  Enter or select the items you want to return using either the vendor’s item
    number or your company’s item number.

>   *You can display the vendor’s item number by marking Display Vendor Items
>   (Options \>\> Display Vendor Item). If the option is not marked, your
>   company’s item number will be displayed. You can change this selection at
>   any time.*

>   Non-inventoried items cannot be selected from the lookup window, however,
>   you can return these by entering the item number.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter or select the receipt number for this return.

>   You must select an item, or a vendor item, before you can select the receipt
>   number.

>   The currency ID of the receipt you select must match the currency ID of the
>   return document.

>   If the receipt number that you enter is matched to more than one receipt
>   line or inventory receipt line, a lookup window (Purchasing Returns PO
>   Receipt Numbers window or Purchasing Returns Inventory Receipt Numbers
>   window) will open allowing you to select the applicable receipt line. The
>   Purchasing Returns PO Receipt Numbers lookup window displays the unit of
>   measure from the original receipt which may be different from the unit of
>   measure in the Returns Transaction Entry window.

>   If there's more than one invoice receipt attached to the receipt number you
>   select, the Purchasing Returns PO Invoice Receipt Numbers lookup window will
>   open automatically allowing you to select the applicable invoice receipt.

>   If there are no quantities available for the receipt number that you
>   entered, you will have the option to search for another receipt. If you
>   choose yes, a lookup window will open where you can select another receipt
>   with the same item.

>   The only way to change a receipt number after it has been entered is to
>   delete the return line and reenter the information.

1.  Enter or accept the unit of measure.

2.  Enter the quantity to be returned or accept the default entry, that is, the
    total quantity available on the selected receipt.

>   If you’re using multiple bins, the total quantity selected for bins must
>   equal the extended quantity of the line item.

1.  The default entry for unit cost of the item or vendor item is based on the
    document type.

>   The following table lists the default unit cost for each document type.

| **Document type**       | **Default unit cost**                 |
|-------------------------|---------------------------------------|
| Return with/Credit      | The original invoice receipt          |
| Inventory w/Credit      | The posted inventory purchase receipt |
| Return or Inventory AND | The average cost of the item          |

>   —If Item type is Average Perpetual

>   —If Item type is Periodic

>   —If any other item type

>   The standard cost of the item

>   The original shipment receipt

>   If necessary, you can change the unit cost for returns with credit.

>   If you change the default unit cost, a purchase price variance will occur.
>   Also, if landed costs are included in the original shipment receipt, a
>   purchase price variance will occur.

>   If the returned item is tracked by lot or serial number, the Returns Lot or
>   Returns Serial Number Entry window will open when you leave the line. Select
>   the lot or serial numbers to be returned. See *Assigning lot numbers to a
>   return* or *Assigning serial numbers to a return* for more information.

>   If you are using multiple bins, the Bin Quantity Entry window will open if a
>   returned item that isn’t tracked by lot or serial numbers requires you to
>   enter bin information. The total quantity selected for bins must equal the
>   line’s extended quantity.

>   *You also can open the Purchasing Returns Lot Number Entry window or the*

>   *Purchasing Returns Serial Entry window by choosing Show Details on the
>   Returns Transaction Entry window and then choosing Serial/Lot. To open the
>   Bin Quantity Entry window, choose Show Details \>\> Bins.*

1.  Enter or accept the 1099 amount if applicable for a 1099 vendor and returns
    with credit.

2.  If your system is set up to calculate taxes using the Advanced tax
    calculation method and you’re entering a return with credit, enter or accept
    the Tax Schedule ID.

3.  Enter or accept trade discount, freight and miscellaneous amounts for
    returns with credit.

>   If your system is using the Advanced tax calculation method, taxes on
>   freight and miscellaneous will be calculated automatically.

1.  Taxes will be calculated automatically as you enter items.

    -   To change the tax amounts for the document, see *Calculating and
        distributing summary taxes for returns* for more information. If you are
        using Project Accounting, you can’t change the tax amount in the Returns
        Transaction Entry window for return and return with credit transactions
        even if your system is set up to allow editing summary-level taxes.

    -   To change the tax amounts for a line item, use the Returns Line Item Tax
        Detail Entry window. See *Calculating and distributing detail taxes for
        return line items* for more information.

    -   If your system is set up to enable GST for Australia/New Zealand and you
        want to indicate that a tax invoice has been received, see *Returns for
        Australia/New Zealand*.

2.  Choose Distributions to open the Purchasing Returns Distribution Entry
    window where you can view or modify account distributions. See *Distributing
    return transaction amounts* for more information.

3.  Choose the Attachment Management icon to attach documents to the return
    transaction, if applicable.

4.  Choose Save or Post. If you want to post this return later, the return must
    be assigned to a Batch ID. You can post the transaction immediately by
    choosing Post.

>   Manual adjustments may be necessary for return documents with the Return
>   document type, refer to *Processing manual adjustments for returns when
>   closing purchase order lines* for more information.

>   For an Inventory document type, if the items being returned will be replaced
>   by the vendor, you must make adjusting journal entries to remove the accrual
>   created by the new shipment receipt.

>   *Refer to the General Ledger documentation for information about correcting
>   General Ledger entries.*

>   If you’re using multiple bins and posting fails, bin quantities will revert
>   to their previous values.

#### Processing project return-from-inventory transactions

>   If you are using Project Accounting, you can use the Returns Transaction
>   Entry window to process project return-from-inventory transactions.

>   If you’re using multiple bins and a default purchase returns bin exists at
>   either the item-site or the site, the quantity at the default bin will
>   decrease by the extended quantity for an item that is not tracked by serial
>   or lot numbers. You can modify the default bin selections. If a default
>   purchase returns bin doesn’t exist, you will be required to enter one. For
>   serial- and lot-numbered items, the purchase returns bin is the bin
>   associated with the serial or lot number and you won’t be able to change the
>   bin.

>   **To process project return-from-inventory transactions:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

![](media/a0f104c7157c5003dddec19545b6f2cd.jpg)

1.  Select a return type for the return transaction. See *Return transaction
    document types* for more information about return document types.

2.  Enter a return number or accept the default entry. The default entry will be
    the next available receipt number in the Purchasing Invoice Setup window.

3.  You can enter a vendor document number.

4.  Enter the return date. The user date is the default date.

>   To enter a General Ledger posting date or a tax date that is different than
>   the return date, choose the Date expansion button; the Returns Date Entry
>   window will open.

>   For multicurrency transactions and for the document type Return w/Credit,
>   the return document date determines the exchange rate that will be used,
>   based on the currency ID entered for the transaction and the associated rate
>   type. For a Return document type, the exchange rate of the original receipt
>   is assigned to the transaction. See the Multicurrency Management
>   documentation (Help \>\> Printable Manuals) for more information.

1.  Enter or select a batch ID (optional). See *Creating a purchasing returns
    batch* for more information.

2.  Enter or select a vendor ID.

3.  Enter a currency ID or accept the default entry. The default currency ID is
    the currency ID assigned to the vendor you selected. If no currency ID has
    been assigned for this vendor, the functional currency for the company will
    be used.

>   The currency ID assigned to the return must match the currency ID of the
>   receipts in the scrolling window.

>   If the selected currency ID is not the functional currency for the company,
>   a rate type and associated exchange rate table will be assigned to the
>   transaction. The rate type is based on the rate type assigned to the
>   selected vendor; if the vendor does not have a rate type assigned, the
>   default rate type for the Purchasing series specified in the Multicurrency
>   Setup window is used.

>   For a Return w/Credit return, you can view or modify the default exchange
>   rate by choosing the currency ID expansion button to open the Exchange Rate
>   Entry window.

1.  If the item being returned was purchased from an EU vendor, mark EU
    Transaction. See *Entering Intrastat trade statistics for returns* for more
    information.

2.  You can enter or select the purchase order number applicable to this return.
    All purchase orders associated with the receipt number will be available in
    the PA Purchase Orders lookup window.

>   Only standard purchase orders that have been received can be returned. You
>   cannot process returns for drop-ship, canceled, or on-hold purchase orders.

1.  Enter or select a project and cost category.

2.  Enter or select the items to return using the item number from the vendor.
    All items previously received for the specified purchase order will be
    available in the lookup window.

>   Non-inventoried items cannot be selected from the lookup window. However,
>   you can return these by entering the item number.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  Enter or select the receipt number applicable to this return.

>   You must select an item, or a vendor item, before you can select the receipt
>   number.

>   The currency ID of the receipt you select must match the currency ID of the
>   return document.

>   If the receipt number that you enter is matched to more than one receipt
>   line or inventory receipt line, a lookup window (Purchasing Returns PO
>   Receipt Numbers) will open, where you can select the applicable receipt
>   line. The Purchasing Returns PO Receipt Numbers lookup window displays the
>   unit of measure from the original receipt, which may be different than the
>   unit of measure in the Returns Transaction Entry window.

>   If there are multiple invoice receipts attached to the receipt number you
>   select, the Purchasing Returns PO Invoice Receipt Numbers lookup window will
>   open, where you can select the applicable invoice receipt.

>   If there are no quantities available for the receipt number that you
>   entered, you will have the option to search for another receipt. If you
>   choose Yes, a lookup window will open, where you can select another receipt
>   with the same item.

>   The only way to change a receipt number after it has been entered is to
>   delete the return line and reenter the information.

1.  Enter or accept the unit of measure.

2.  Enter the quantity to be returned or accept the default entry.

>   If you’re using multiple bins, the total quantity selected for bins must
>   equal the extended quantity of the line item.

1.  Enter or accept the unit cost.

>   The default entry for the unit cost of the item is based on the document
>   type, as shown in the following table.

| **Document type** | **Default unit cost**        |
|-------------------|------------------------------|
| Return w/Credit   | The original invoice receipt |
| Return AND        | The average cost of the item |

>   —If Item type is Average Perpetual

>   —If Item type is Periodic

>   —If any other item type

>   The standard cost of the item

>   The original shipment receipt

>   You can change the unit cost only for returns with credit.

>   If you change the default unit cost, a purchase price variance will occur.
>   Also, if landed costs are included in the original shipment receipt, a
>   purchase price variance will occur.

>   If the returned item is tracked by lot or serial number, the PA Purchasing

>   Returns Lot Number Entry or PA Purchasing Returns Serial Number Entry window
>   will open when you leave the line. Select the lot or serial numbers to be
>   returned. See *Assigning lot numbers to a return* or *Assigning serial
>   numbers to a return* for more information.

>   If you are using multiple bins, the Bin Quantity Entry window will open if a
>   returned item that isn’t tracked by lot or serial numbers requires you to
>   enter bin information. The total quantity selected at bins must equal the
>   line’s extended quantity.

>   *You also can open the Purchasing Returns Lot Entry window or the
>   Purchasing*

>   *Returns Serial Number Entry window by choosing Show Details on the Returns
>   Transaction Entry window and then choosing Serial/Lot. To open the Bin
>   Quantity Entry window, choose Show Details \>\> Bins.*

1.  To see more details about a line item, select the item and choose the shown
    button to expand the scrolling window. In the detailed view, you can change
    the posting account, extended cost, tax details, or comment. The changes
    will apply only to the current line item.

>   *To delete a row in the Returns Transaction Entry scrolling window, select
>   the row and choose Transactions by Order Entered \>\> Delete Row or choose
>   the delete row button.*

1.  Enter or accept the 1099 amount, if applicable for a 1099 vendor.

2.  Enter or select a tax schedule ID.

3.  Enter or accept trade discount, freight, and miscellaneous amounts for
    returns with credit only. All of these fields are optional.

>   If your system is using the Advanced tax calculation method, taxes on
>   freight and miscellaneous will be calculated automatically.

1.  You can enter a tax amount for Return w/Credit transactions. To change the
    tax amounts for the document, see *Calculating and distributing summary
    taxes for returns* for more information. To change the tax amounts for a
    line item, see *Calculating and distributing detail taxes for return line
    items* for more information.

>   See *Returns for Australia/New Zealand* if your system is set up for GST for
>   Australia/New Zealand and you must indicate that a tax invoice has been
>   received.

1.  Choose the Attachment Management icon to attach documents to the return
    transaction, if applicable.

2.  Choose Save or Post. To post this return later, the return must be assigned
    to a batch ID. You can post the transaction immediately by choosing Post.

>   Manual adjustments may be necessary for return documents with the Return
>   document type. See *Processing manual adjustments for returns when closing
>   purchase order lines* for more information.

>   If you’re using multiple bins and posting fails, bin quantities will revert
>   to their previous values.

#### Printing purchasing returns transactions

>   Use the Purchasing Returns Print Options window to print the Edit List or
>   return documents. You can use the edit list to verify the transaction
>   information you entered. Print the return document if you want to give a
>   copy to vendors or others in your organization.

>   **To print purchasing returns documents:**

1.  Open the Purchasing Returns Print Options window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry \>\> select a
>   return document \>\> Print button)

>   (Purchasing \>\> Transactions \>\> Returns Batches \>\> select a batch \>\>
>   Print button)

>   (From the Returns Transaction Inquiry Zoom window, select a return document
>   \>\> Print button)

![](media/90f130cb87bd1032ed275cfaa3e9053b.jpg)

1.  To print an edit list of the selected document or all the unposted return
    transactions in the selected batch, select Edit List.

2.  To print the selected document, or all the documents in the selected batch,
    select Documents.

>   Options in Return Document Options are available to add more detail to the
>   printed document.

-   To include tax details on the printed document, mark Include Tax Details.
    For the tax details to print on return documents, Print on Documents must be
    marked in the Tax Detail Maintenance window.

>   Selecting Line Item and Summary Taxes prints the tax details for each item.
>   A summary of the tax details of all line items is printed at the bottom.

>   Selecting Summary taxes prints a summary of the tax details of all line
>   items at the bottom.

-   To select the currency that should be used on the printed document, select
    the Currency to Print. This option is available only if Multicurrency
    Management is registered.

>   Selecting Functional prints amounts on the return document in currency your
>   company uses. This may be useful if the document will be used by others in
>   your organization.

>   Selecting Originating prints amounts in the currency your vendor uses. This
>   can help in communicating with the vendor about the document.

1.  To print the documents, select Print.

>   *If you select both Documents and Edit List, the edit list will print first
>   followed by the selected document or batches of documents.*

#### Entering detail information for a return

>   Use the Returns Transaction Entry scrolling detail view to add or modify
>   line item information such as extended cost or to change a line item’s
>   posting accounts.

>   **To enter detail information for a return:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    All Purchasing Transactions list.

2.  Choose Purchase Returns Transactions and then select a document type to open
    the Returns Transaction Entry window.

3.  Enter document information, including return number, vendor document number,
    date, and vendor ID.

4.  Enter or select the item to be returned and enter line item information.

>   To add an attachment to the item, select the item and choose the Attachment
>   Management icon to open the Document Attachment Management window.

1.  If you are entering a project return-from-inventory transaction, you can
    modify the billing rate for Time and Materials Projects and the markup
    percentage for all project types.

2.  The default inventory and purchase price variance accounts for posting the
    return will be displayed. If no accounts are displayed, you can enter them.

3.  Enter a comment ID (optional).

4.  You may change the extended cost for returns with credit, if necessary.

5.  For returns with credit, you may change the item tax option, the item tax
    schedule, the tax schedule, and the calculated tax when the Advanced Tax
    Calculation method has been selected in Purchase Order Processing Setup
    Options window.

>   Refer to the *Default tax schedules for return items* for more information
>   about the tax schedule field.

1.  Choose the Show button to display details about line items. You can then
    modify line item detail information or you can choose the Add Row or Delete
    Row buttons to add or delete line items.

>   *You also can choose the arrow beside Transactions by Order Entered and
>   select an option from the list to add or delete a row or show or hide
>   details.*

#### Entering Intrastat trade statistics for returns

>   Use the Purchasing Intrastat Entry window to enter the information required
>   to create the Intrastat Trade Report that you submit to your government, and
>   the EC Sales List, which displays cumulative goods value totals by each
>   vendor or customer tax registration number. You can enter line items along
>   with trade statistics.

>   If Intrastat information was entered for the ship-from address ID for the
>   vendor, that information will be displayed in this window. Each time that
>   you enter a new line item, the Intrastat statistics entered for the first
>   line item will be applied as the default values for the new line item—except
>   for the Transaction Nature field. The default value of the Transaction
>   Nature field for each individual line will be determined by the setup
>   information in the Intrastat Setup window. You can use the Purchasing
>   Intrastat Entry window to change Intrastat information for an individual
>   transaction, or to enter Intrastat information if none was entered for the
>   vendor.

>   *To use the EU Transaction option, your system must be set up in the Company
>   Setup Options window to track Intrastat statistics.*

>   **To enter Intrastat trade statistics for returns:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter return information, including return type, return number, vendor
    document number, date, and vendor ID.

2.  Mark EU Transaction.

3.  Enter or select the item to be returned and enter the line item information.

4.  Choose the EU expansion button to open the Purchasing Intrastat Entry
    window, where you can enter or change Intrastat information.

5.  In the Net Unit Mass field, enter the weight of the goods in kilograms or
    accept the default entry. The default entry is from the shipping weight of
    the item, the default weight of non-inventoried items is 0.

>   The Quantity field displays the quantity of the goods you are returning.

>   The Line Mass field displays the total mass per item and is calculated
>   automatically. The line mass total is equal to the amount entered in the Net
>   Unit Mass field multiplied by the amount in the Quantity field.

1.  If applicable, enter a supplementary units amount or accept the default
    entry. The supplementary units amount is a second quantity. Supplementary
    unit amounts are required by the EU Combine Nomenclature for certain goods.

>   *If Supplementary Units Required is not marked in the Tax Commodity Code
>   Maintenance window, the Supplementary Units field is unavailable.*

1.  In the Traders Reference field, enter a reference code, such as an invoice
    or dispatch number, or other information that will identify the transaction.

2.  Enter a goods value and statistical value, if applicable.

3.  Choose OK to save the record.

#### Multiple bins in purchase order returns

>   Use multiple bins to add another level of detail to item quantity tracking.
>   Besides tracking items within inventory sites, with multiple bins you can
>   track item quantities in bins that reside within each site. Bin quantities
>   are processed and displayed in the item’s base unit of measure.

>   *You can set up bin information when multiple bins functionality has been
>   installed and registered. However, you must also enable this feature in
>   Inventory Control before you can use bins to track items. For more
>   information about enabling multiple bins, see the Inventory Control
>   documentation.*

>   Default bins for transaction types at each site can be identified for use in
>   transactions. For example, a default bin could be created for return
>   transactions at your warehouse site. Default bins also can be identified for
>   a particular item and transaction type at a site. If you always use Bin A
>   when returning a certain item from your main site, for example, you can set
>   up Bin A as the default purchase purchase returns bin for the item at the
>   main site. Microsoft Dynamics GP automatically creates item-site-bin
>   relationships the first time a bin is used for a transaction.

>   If you’re using multiple bins and a default purchase returns bin exists at
>   either the item-site or the site, the quantity at the default bin will
>   decrease by the extended quantity for an item that is not tracked by serial
>   or lot numbers. You can modify the default bin selections. If a default
>   purchase returns bin doesn’t exist, you will be required to enter one. For
>   serial- and lot-numbered items, the purchase returns bin is the bin
>   associated with the serial or lot number and you won’t be able to change the
>   bin.

>   For more information about setting up and using multiple bins, see the
>   Inventory Control documentation

#### Changing bins for a return transaction

>   If you’re using multiple bins, use the Bin Quantity Entry window to verify
>   or change bin allocations for items that are not tracked by serial or lot
>   numbers. For items that are tracked by serial or lot numbers, you can verify
>   bins in the Purchasing Returns Serial Number Entry window or the Purchasing
>   Returns Lot Number Entry window. For more information, see *Assigning lot
>   numbers to a return* or *Assigning serial numbers to a return*.

>   You can select from more than one bin per site for an item that tracks
>   serial or lot numbers. For example, if the quantity returned is 20, you can
>   select 15 from Site A, Bin 1 and 5 from Site A, Bin 2.

>   **To change bins for a return transaction:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter document information, including return type, return number, vendor
    document number, date, and vendor ID.

2.  Select a sales inventory or discontinued item that isn’t tracked by serial
    or lot numbers and choose the Bins button to open the Bin Quantity Entry
    window.

3.  From the list of available bins, select one to use. You also can enter a bin
    that hasn’t been created yet.

4.  Enter a quantity for the item.

5.  Choose Insert.

6.  Choose OK to save your changes and close the window.

7.  Save your changes and close the Returns Transaction Entry window.

#### Assigning lot numbers to a return

>   Use the Purchasing Returns Lot Number Entry window to assign lot numbers for
>   returned items. This window will open automatically when you leave the line
>   after entering a lot-numbered item in the Returns Transaction Entry window.
>   If the quantity returned matches the quantity available in the lot or lots,
>   the lot numbers are displayed automatically.

>   **To assign lot numbers to a return:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter a document information, including return type, return number, vendor
    document number, date, and vendor ID.

2.  If you are entering a project return-from-inventory transaction, enter or
    select a project and cost category.

3.  Enter or select the lot-numbered item to be returned and enter line item
    information. The Purchasing Returns Lot Number Entry window will open
    automatically when you leave the line in the Returns Transaction Entry
    scrolling window.

![](media/135a59c8c15e4c646fac99241fddd995.jpg)

>   *To open the Purchasing Returns Lot Number Entry window manually, choose the
>   Show Details button on the Returns Transaction Entry window and then choose
>   Serial/Lot.*

1.  Select a lot number from the Available column of the scrolling window. You
    also can enter an available lot number in the Lot Number field.

>   An icon appears in the Lot Number field and the Expiration Date field if the
>   lot has already expired.

1.  Enter the quantity you want to return from the lot number in the Quantity
    Selected column and then choose Insert. The Bin columns display the number
    of the bin containing the available or selected lot-numbered item.

    -   If you entered a lot number using the Lot Number field, enter the
        quantity that you want to return from this lot number in the Quantity
        Selected field and then choose Insert.

    -   To remove a selected lot number, choose Remove. To remove all selected
        lot numbers, choose Remove All.

2.  Repeat steps 4 and 5 until all desired lot numbers have been selected.

3.  Choose OK to save your changes to the window.

#### Assigning serial numbers to a return

>   Use the Purchasing Returns Serial Number Entry window to assign serial
>   numbers for returned items. This window will open automatically when you
>   leave the line after entering a serial-numbered item in the Returns
>   Transaction Entry window. If the quantity returned matches the quantity
>   available in the lot or lots, Microsoft Dynamics GP will select and display
>   the serial numbers automatically.

>   **To assign serial numbers to a return:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter document information, including return type, return number, vendor
    document number, date, and vendor ID.

2.  If you are entering a project return-from-inventory transaction, enter or
    select a project and cost category.

3.  Enter or select the serial-numbered item to be returned and enter line item
    information. The Purchasing Returns Serial Number Entry window will open
    automatically when you leave the line in the Returns Transaction Entry
    scrolling window.

![](media/6054a2757890edaa0057288daacb74f2.jpg)

>   *You can open the Purchasing Returns Serial Number Entry window manually by
>   choosing the Show Details button on the Returns Transaction Entry window and
>   then choosing Serial/Lot.*

1.  Select a serial number from the Available column and choose Insert. You also
    can enter an available serial number in the Serial Number field and choose
    Insert. The Bin columns display the number of the bin containing the
    serialnumbered item.

    -   To remove a selected serial number, choose Remove.

    -   To remove all selected serial numbers, choose Remove All.

2.  Repeat step 4 until all desired serial numbers have been selected.

3.  Choose OK to save your changes to the window.

#### Distributing return transaction amounts

>   Use the Purchasing Returns Distribution Entry window to view or modify the
>   Returns distribution transaction. Return transaction amounts are distributed
>   to posting accounts automatically based on the document type. The
>   distributions can be edited.

>   For more information about the origin of account default entries, see
>   *Return distribution accounts*.

>   **To distribute return transaction amounts:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter document information, including return type, vendor document number,
    date, and vendor ID.

2.  Enter or select the item to be returned and enter line item information.

3.  Choose Distributions to open the Purchasing Returns Distribution Entry
    window.

![](media/222238576f2fa8c25ecb8b0114bbb190.jpg)

>   If you are using Multicurrency Management and if the originating debits and
>   credits balance but the functional equivalents do not balance, the
>   difference will be posted automatically to the Rounding Difference account.
>   This also occurs when Euro currency relationships are enabled and the
>   functional amounts balance, but there are amounts remaining in the
>   originating currency. For more information on multicurrency transactions
>   with Purchase Order Processing, see the Purchase Order Processing
>   documentation.

1.  Enter a reference for the return or accept the default entry. The reference
    entered will post to the General Ledger as the reference for the return.

2.  Enter or accept the default amounts.

>   *See Entering detail information for a return for more information on
>   entering these details.*

>   To distribute a transaction to multiple posting accounts, change the default
>   amount in the scrolling window. In the next available line, enter or select
>   another distribution account, choose the distribution type and enter the
>   amount.

1.  Continue entering distribution amounts until your transaction is fully
    distributed.

2.  Enter a distribution reference (optional). This reference will be posted to
    the General Ledger as the distribution reference for the account.

3.  Choose OK to save your entries and continue entering the return. You can
    save the return if it’s not fully distributed, but you won’t be allowed to
    post until the full amount is distributed and debits equal credits.

#### Return distribution accounts

>   The posting accounts will distribute as shown in the following table:

| **Account**          | **Document type**               | **Default entry**                                                                                                                                                                                                                        |
|----------------------|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PURCH (Inventory)    | Return, Return w/Credit         | Shipment receipt.                                                                                                                                                                                                                        |
|                      | Inventory, Inventory w/         | Accounts set up for the item or vendor item. If accounts haven’t been set up for the item or vendor item, then the accounts assigned in the Posting Setup window will be used.                                                           |
| PURCH (PPV)          | Return, Return w/Credit         | Shipment receipt. If not found then the accounts set up for the item or vendor item will be used. If accounts haven’t been set up for the item or vendor item, then the accounts assigned in the Posting Setup window will be used.      |
|                      | Inventory w/Credit              | Accounts set up for the item/vendor item. If accounts haven’t been set up for the item or vendor item, then the accounts assigned in the Posting Setup window will be used.                                                              |
| PURCH (UPPV)         | Return                          | Shipment receipt. Applicable to item types Sales Inventory and Discontinued using the Periodic valuation method.                                                                                                                         |
| ACCRUED              | Return                          | Shipment receipt. If not found, then the accounts assigned in the Posting Setup window for the Purchasing Series will be used.                                                                                                           |
|                      | Inventory (if Variance)         | Variance account set up for the item or vendor item. If an account hasn’t been set up for the item or vendor item, then the variance account assigned in the Posting Setup window for the Inventory Series will be used.                 |
|                      | Inventory (if                   | Inventory offset account set up for the item or vendor item. If an account hasn’t been set up for the item or vendor item, then the inventory offset account assigned in the Posting Setup window for the Inventory Series will be used. |
| PAY, TRADE, FREIGHT, | Return w/Credit,                | Accounts set up for the vendor. If accounts haven’t been set up for the vendor, then the accounts assigned in the Posting Setup window will be used.                                                                                     |
| ROUND                | All return document types       | Rate type. If the rate type hasn’t been set up, then the rounding account set up in the Currency setup window will be used.                                                                                                              |
| OVHD, APP-OVHD       | Return or Return w/             | Posted shipment receipt.                                                                                                                                                                                                                 |
|                      | Inventory or Inventory w/Credit | Accounts set up for the item or vendor item. If accounts haven’t been set up for the item or vendor item, then the accounts assigned in the Posting Setup window for the Manufacturing Series will be used.                              |

>   Credit

>   (not applicable to Inventory return document type)

>   (not applicable to other return document types)

>   Adjustment, Transfer or

>   Sales Return)

>   MISC, TAX

>   Inventory w/Credit

>   Credit

#### Processing manual adjustments for returns when closing purchase order lines

>   Some manual adjustments are required for Return type return documents based
>   on the particular circumstances of that transaction. Purchase order lines
>   are closed automatically when they are completely invoiced. If the returned
>   item is not going to be replaced or if the replacement item will be received
>   on a new purchase order, you must manually close the purchase order line. If
>   the purchase order has been partially invoiced, the purchase receipt cost
>   will be adjusted incorrectly. To correct this, you will need to manually
>   adjust the inventory unit costs and create an adjusting journal entry.

>   *If the returned item will be replaced, we recommend that you close the
>   purchase order line after the non-returned items have been invoiced.*

>   **To process manual adjustments for returns when closing purchase order
>   lines:**

1.  Open the Edit Purchase Orders window.

>   (Purchasing \>\> Transactions \>\> Edit Purchase Orders)

1.  Enter the purchase order number.

2.  Change the purchase order line item status to Closed.

>   *For more information about editing purchase order status, refer to the
>   Purchase Order Processing documentation.*

1.  Use the posting journal and distribution breakdown registers to check the
    adjustment entries created by Purchase Order Processing when closing the
    purchase order.

2.  If the purchase receipt cost has been adjusted incorrectly—this happens when
    the purchase order has been partially invoiced—adjust the Inventory Unit
    Cost using the Inventory Adjust Costs window (Inventory \>\> Utilities \>\>
    Adjust Costs).

>   *For more information about adjusting the purchase receipt cost of an item,
>   refer to the Inventory Control documentation.*

1.  If necessary, create an adjusting journal entry to correct the accrued and
    the inventory accounts.

>   *Refer to the General Ledger documentation for information about correcting
>   General Ledger entries.*

**Chapter 24: Taxes for returns**

>   Taxes for returns with credit can be calculated, modified, and distributed
>   in purchase order approvals. Taxes are calculated automatically when you
>   leave the line in the Returns Transaction Entry window. Taxes for freight
>   and miscellaneous are calculated automatically when you enter those fields.
>   The total tax amount for the return is displayed in the Tax field.

>   If your system is set up to allow editing summary-level taxes, use the
>   Returns Tax Summary Entry window to change tax distributions for returns. To
>   change tax details or the tax distribution for individual line items, use
>   the Returns Line Item Tax Detail Entry window.

>   If your system is set up to specify tax details for automatic tax
>   calculation, only those tax details that are marked in the Tax Schedule
>   Maintenance window will be used to calculate taxes automatically.

>   This information is divided into the following sections:

-   *Default tax schedules for return documents*

-   *Calculating and distributing summary taxes for returns*

-   *Default item tax schedules*

-   *Default tax schedules for return items*

-   *Calculating and distributing detail taxes for return line items*

-   *Returns for Australia/New Zealand*

#### Default tax schedules for return documents

>   The tax calculation option assigned in the Purchase Order Processing Setup
>   window is used to determine which default tax schedule will be assigned to
>   the return document. The shipping method assigned to the vendor’s purchase
>   address is checked as well to determine where the exchange of goods took
>   place. Together the shipping method and the tax calculation option determine
>   which tax schedule appears as a default tax schedule for the return
>   document.

>   Refer to the following table for the default tax schedules for a return
>   document.

| **Tax Calculation option** | **Shipping method**          | **Default tax schedule for the return**                                            |
|----------------------------|------------------------------|------------------------------------------------------------------------------------|
| Single                     | Not applicable               | Single tax schedule assigned in the Purchase Order Processing Setup Options window |
| Advanced                   | Pickup OR No shipping method | Tax schedule assigned to the vendor’s purchase address                             |
| Advanced                   | Delivery                     | Purchases tax schedule assigned in the Company Setup window                        |

>   *If you decided not to use the shipping method to determine the default tax
>   schedule, the tax schedule assigned to the vendor’s purchase address will be
>   the default tax schedule no matter what tax calculation method you selected
>   to use.*

#### Calculating and distributing summary taxes for returns

>   Use the Returns Tax Summary Entry window to add, change, delete, or view
>   summarized tax amounts and the posting accounts for a return. Taxes are
>   calculated automatically as you enter each tax detail or edit the Total
>   Returns amount. Summary tax edits won’t change the taxes calculated for each
>   line item in the Returns Line Item Tax Detail Entry window.

>   If your system isn’t set up to allow editing summary-level taxes, you can’t
>   change the tax amount in the Returns Transaction Entry window or the tax
>   information in the Returns Tax Summary Entry window, except for the account.

>   If you are using Project Accounting, you can’t change the tax amount in the
>   Returns

>   Transaction Entry window or the tax information in the Returns Tax Summary
>   Entry window for return and return with credit transactions even if your
>   system is set up to allow editing summary-level taxes.

>   Regardless of how your system is set up, you will be able to change the
>   account for tax included in item price taxes at the summary level. For more
>   information on setup options, see the System Setup instructions (Help \>\>
>   Contents \>\> select Setting up the System).

>   **To calculate and distribute summary taxes for returns:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter document information, including return type, return number, vendor
    document number, date, and vendor ID. You cannot enter tax information for
    returns without credit.

2.  Enter or select the item to be returned and enter line item information.

3.  Choose the Tax expansion button to open the Returns Tax Summary Entry window
    where you can view or edit the tax distribution amounts.

![](media/452f8e9ac54bd575b7e687623c6c5a2f.jpg)

>   Currency amounts in this window may be displayed in the functional or
>   originating currency depending on the view selected in the Returns
>   Transaction Entry window.

1.  To edit tax information, enter a tax detail ID, total returns, total taxable
    returns, tax amount, or select a new account. (The tax amount for the detail
    will be posted to the account).

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row. To delete all the tax distributions, choose Delete.

>   To restore the default tax information, choose Default.

1.  Continue entering tax details until the tax is fully distributed. See
    *Entering detail information for a return* for more information on entering
    these details.

*To restore the default tax information, choose Default.*

1.  Choose OK to save your entries and return to the Returns Transaction Entry
    window.

>   If there is a difference between the total tax amount distributed to tax
>   details and the tax amount entered in the Returns Transaction Entry window,
>   the tax amount will be adjusted to match the total tax amount.

#### Default item tax schedules

>   The Item Tax Schedule field on the detail view of the Returns Transaction
>   Entry window displays the default tax schedule assigned to the item that is
>   applicable to this return line. The item tax schedule that will be used
>   depends on the return type and the tax calculation method assigned in
>   Purchase Order Processing Setup Options window. Refer to the following table
>   for the item tax schedule default values:

| **Return type**    | **Tax Calculation Option** | **Default item tax schedule**                             |
|--------------------|----------------------------|-----------------------------------------------------------|
| Return w/Credit OR | Single schedule            | None                                                      |
| Inventory w/Credit | Advanced                   | Purchase tax schedule assigned to the item in the Item    |
| Return w/Credit    | Advanced                   | Tax schedule assigned to the item on the original receipt |

>   Inventory w/Credit

>   Maintenance window

#### Default tax schedules for return items

>   When the Single Tax Calculation method is selected in Purchase Order
>   Processing Setup Options window, tax is calculated for each individual
>   return line based on the tax schedule assigned to the return document.

>   When the Advanced tax calculation method is selected in Purchase Order
>   Processing Setup Options window, taxes are calculated for individual return
>   lines based on the item taxable option as follows:

-   When the item taxable option is Taxable, the item tax schedule IDs are
    masked against the tax schedule IDs assigned to the return line. Masking
    means that only tax details that exist in both schedules will be used.

-   When the item taxable option is Nontaxable, no tax is calculated.

-   When the item taxable option is Base on Vendor, the tax schedule IDs
    assigned to the return line will be used to calculate taxes.

>   Refer to the following table for the default tax schedules for return lines.

| **Return Type**    | **Tax Calculation option** | **Shipping Method** | **Default Tax Schedule**                                            |
|--------------------|----------------------------|---------------------|---------------------------------------------------------------------|
| Return w/Credit or | Single                     | Not applicable      | Single tax schedule assigned in the Purchase Order Processing Setup |
| Return w/Credit    | Advanced                   | Not applicable      | Tax schedule assigned to the original purchase receipt              |
| Inventory w/Credit | Advanced                   | Pickup OR           | Tax schedule assigned to the return                                 |
| Inventory w/Credit | Advanced                   | Delivery            | Purchase tax schedule assigned to the site                          |

>   Inventory w/Credit

>   window

>   No shipping method

#### Calculating and distributing detail taxes for return line items

>   Use the Returns Line Item Tax Detail Entry window to add, change, delete, or
>   view tax amounts calculated on an individual line item. Taxes are calculated
>   automatically as you enter each tax detail or edit the Total Returns amount.
>   Summary tax edits won’t change the taxes calculated for each line item in
>   the Returns Line Item Tax Detail Entry window. However, tax edits made for
>   each return line will change the summary tax amounts in the Returns Tax
>   Summary Entry window.

>   **To calculate and distribute detail taxes for return line items:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter document information, including return type, return number, vendor
    document number, date, and vendor ID. You cannot enter tax information for
    returns without credit.

2.  Enter or select the item to be returned and enter line item information.

3.  Enter a calculated tax amount or choose the Calculated Tax expansion button
    to open the Returns Line Item Tax Detail Entry window, where you can view or
    edit tax distribution amounts.

![](media/15b3b875ad8fcd461b06546a5e6a6d3f.jpg)

>   *If your system is set up to enable GST for Australia/New Zealand, you also
>   can change the account.*

1.  To edit tax information, enter a tax detail ID, total returns or tax amount
    for the line item. (The tax amount for the detail will be posted to the
    account.) See *Entering detail information for a return* for more
    information on entering these details.

>   To delete all the tax details, choose Delete.

>   To delete a single tax detail, select the row containing it and choose Edit
>   \>\> Delete Row. To delete all the tax distributions, choose Delete.

>   To restore the default tax information, choose Default.

1.  Choose OK to save your entries and return to the Returns Transaction Entry
    window.

>   If there is a difference between the total tax amount distributed to tax
>   details and the calculated tax amount entered in the scrolling window of the
>   Returns Transaction Entry window, the calculated tax amount will be adjusted
>   to match the total tax amount distributed to tax details.

#### Returns for Australia/New Zealand

>   If your system is set up to enable GST for Australia/New Zealand, you can
>   indicate whether a tax invoice has been received for the return transaction.
>   You also will be able to print a Recipient Created Adjustment Note from the
>   Returns Batch Entry window or from the Returns Transaction Entry window.

#### Indicating that a tax invoice has been received

>   The Returns Transaction Entry window displays Tax Invoice Received and Tax
>   Invoice Required options for returns with credit when your system is set up
>   to enable GST for Australia/New Zealand. The information from these options
>   will be provided to the Tax Invoice Required and Tax Invoice Received
>   reports available to you from the Tax Invoice Received window.

>   Use the Tax Invoice Received option to indicate whether a tax invoice has
>   been received for this return transaction. For more information about the
>   Tax Invoice Required and Tax Invoice Received reports, refer to the GST and
>   Australian Taxes documentation.

>   **To indicate that a tax invoice has been received:**

1.  Open the Returns Transaction Entry window.

>   (Purchasing \>\> Transactions \>\> Returns Transaction Entry)

1.  Enter document information, including return type, vendor document number,
    date, and vendor ID. You cannot enter tax information for returns without
    credit.

>   If you enter a vendor who has the Tax Invoice Received option marked in the
>   Vendor Maintenance Options window, the Tax Invoice Received option in this
>   window will be marked.

1.  Enter or select the item to be returned and enter line item information.

2.  To indicate that a tax invoice has been received for this return, mark the
    Tax Invoice Received option.

>   If the Tax Invoice Required option in the Tax Detail Maintenance window is
>   marked for any tax detail for this transaction, the Tax Invoice Required
>   option in this window will be marked.

1.  Complete the return transaction as explained in *Processing purchasing
    return transactions* or in *Processing project return-from-inventory
    transactions*.

#### Recipient Created Adjustment Note for Returns

>   An adjustment note shows the corrections made on the Business Activity
>   Statement, which usually means the GST charges or input tax credits
>   attributed to the statement are less or more than they should be. The report
>   shows the same information printed in a tax invoice, with the transaction
>   amount modified.

>   The following table lists the windows from which you can print an adjustment
>   note.

| **Window**                                                                              | **Navigation** |
|-----------------------------------------------------------------------------------------|----------------|
| Returns Transaction Entry (Purchasing \>\> Transactions \>\> Returns Transaction Entry) | Reports button |
| Reports Batch Entry (Purchasing \>\> Transactions \>\> Returns Batches)                 | Reports button |

>   For more information about Recipient Created Adjustment Notes, refer to the
>   GST and Australian Taxes documentation.

**Part 5: Inquiries and reports**

>   This part of the documentation explains how to use inquiries and reports to
>   analyze your purchasing and receiving activity. You can analyze transaction
>   and item information, and display the information either on screen or on a
>   printed report.

>   In Purchase Order Processing, inquiries allow you to quickly view both
>   current and historical purchase order information. You can review
>   information in summary or detailed form, with the option of printing the
>   information in the window by choosing File \>\> Print.

>   Purchase Order Processing reports help you analyze your overall business
>   activity. Some reports are important for the audit trail, to ensure that
>   you’re tracking every transaction that’s been entered.

>   The following topics are discussed:

-   *Chapter 25, “Inquiries,”* explains how to use Purchase Order Processing
    inquiry windows to view document and item information.

-   *Chapter 26, “Reports,”* describes how to use reports to analyze purchasing
    and receiving activity and pinpoint errors in transaction entry.

**Chapter 25: Inquiries**

>   You can view important information about your purchasing and receiving
>   activity on-screen using the Inquiry windows. These windows provide easy
>   access to detailed and summarized Purchase Order Processing information.

>   This information is divided into the following sections:

-   *Viewing multiple currencies*

-   *About reporting currency*

-   *Viewing purchasing documents*

-   *Viewing item information for purchasing documents*

#### Viewing multiple currencies

>   You can choose whether you want to view multicurrency amounts in the
>   originating, functional, or reporting currency. Choose View \>\> Currency
>   \>\> Functional, Originating, or Reporting while viewing an inquiry window.
>   The option will be saved on a per user, per window basis.

>   You also can use the currency list button in the windows that support
>   changing the currency view. The View \>\> Currency menu option and currency
>   list button are available in the following windows:

-   Purchase Order Processing Document Inquiry

-   Purchase Order Inquiry Zoom

-   Receivings Transaction Inquiry Zoom

-   Purchasing Invoice Inquiry Zoom

>   The first time you open these windows after registering Multicurrency

>   Management, all the transactions will be displayed in the originating
>   currency. If you change the currency view, the option you last used will be
>   the default view the next time you open that window.

#### About reporting currency

>   A reporting currency is used to convert functional or originating currency
>   amounts to another currency on inquiries and reports. For example, if the
>   Canadian dollar is the functional currency for a company, you can set up the
>   euro as your reporting currency to view an inquiry window with currency
>   amounts displayed in the euro currency.

>   During the reporting currency setup in Multicurrency Management, you’ll set
>   up a reporting currency and enter a default exchange rate and rate
>   calculation method. Depending on how your system is set up, you may be able
>   to override the default reporting currency exchange rate or rate calculation
>   method on inquiries and reports. To change the default reporting currency
>   exchange rate, choose View \>\> Currency \>\> Modify Reporting Rate to open
>   the Modify Reporting Rate window.

>   For more information about the reporting currency, see the Multicurrency
>   Management documentation.

#### Viewing purchasing documents

Use the Purchase Order Processing Document Inquiry window to view information
about documents you’ve entered in Purchase Order Processing. This window
provides easy access to detailed or summarized information about purchase orders
and receipts.

You can view information as it was originally entered by clicking on link
fields. For example, you can select a purchase order and click on the PO Number
label to the Purchase Order Inquiry Zoom window to view the purchase order as it
was entered.

You can choose File \>\> Print in the Purchase Order Inquiry Zoom window to
print and send the purchase order in e-mail, even if the purchase order is in
history. When you choose to print from this window, the Purchase Order Print
Options window will open, where you can select to print or send the document in
the functional, originating, or reporting currency.

To view a receipt, select it in the Purchase Order Processing Document Inquiry
window and click on the Receipt No. label. To view an in-transit transfer,
select it in the Purchase Order Processing Document Inquiry window and click on
the Transfer Number label.

>   **To view purchasing documents:**

1.  Open the Purchase Order Processing Document Inquiry window.

>   (Purchasing \>\> Inquiry \>\> Purchase Order Documents)

![](media/9581e4c7f370e43d345aa75338b2980d.jpg)

1.  Select all vendors or a range of vendors.

>   *To view in-transit transfer inventory receipts, select to view all vendors
>   or leave the From field blank if you want to view a specific range.
>   In-transit transfer inventory receipts aren’t assigned to vendor IDs.*

1.  In the Documents list, select PO Number, Receipt Number, or Purchase Order
    Date as the sorting order.

2.  Select to view all documents or a range of documents.

3.  To display only purchase orders that are on hold, mark Include POs On Hold
    Only.

4.  Mark which documents you want to include in the inquiry. When you restrict
    by PO Number, Receipt Number, or Purchase Order Date, the options that
    appear next to the Include field will change.

>   The following table shows Documents List selections and their corresponding
>   Include options:

| **Documents list selection** | **Include options**  |
|------------------------------|----------------------|
| PO Number                    | Open Purchase Orders |
| Receipt Number               | Unposted Receipts    |
| Purchase Order Date          | Open documents       |

>   Historical Purchase Orders

>   Receipts Received

>   Historical Receipts

>   Assigned PO

>   Historical documents

1.  Choose Redisplay to display the documents in the scrolling window. To print
    the Purchasing Document Inquiry Report, choose File \>\> Print.

2.  Highlight a record and click a link to open a window to view more detailed
    information (optional).

>   The following table shows the link field and the window that the link opens:

| **Link field**  | **Window that opens**                                                                                                                                                   |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PO Number\*     | Purchase Order Inquiry Zoom window                                                                                                                                      |
| Transfer Number | In-Transit Transfer Inquiry Zoom window                                                                                                                                 |
| Receipt No.     | Receivings Transaction Inquiry Zoom window or Purchasing Invoice Inquiry Zoom window, depending on the type of receipt selected Returns Transaction Inquiry Zoom window |
| Vendor ID       | Vendor Inquiry window                                                                                                                                                   |

>   \*Because one receipt can be associated with multiple purchase orders, you
>   will not be able to use the link on the purchase order field if you select
>   Receipt Number from the Documents list and mark to include Assigned PO.

#### Viewing item information for purchasing documents

>   Use the Purchase Order Processing Item Inquiry window to view items assigned
>   to purchase orders and receipts. Control blanket line items for blanket and
>   drop-ship blanket purchase orders won’t be displayed in the window. If you
>   are restricting by the on-order quantity, line items that don’t have an
>   on-order quantity won’t be displayed. Line items entered on drop-ship
>   purchase orders or drop-ship blanket purchase orders won’t be displayed
>   because the line items don’t update the onorder quantity. Line items entered
>   on a standard or blanket purchase orders with a status of New, Canceled,
>   Closed, or Received also won’t be displayed because they don’t have an
>   on-order quantity.

>   To view items by the vendor’s item number, choose Options \>\> Display
>   Vendor

>   Item. The Vendor Item label will be displayed in the Purchase Order
>   Processing

>   Item Inquiry scrolling window. If Display Vendor Item isn’t selected, the
>   Item label will be displayed in the Purchase Order Item Inquiry scrolling
>   window and you can view items using your item number.

If you are using Project Accounting, the Project Number field and the Cost
Category ID field will be displayed in the Purchase Order Processing Item
Inquiry scrolling window.

You can view information as it was originally entered by clicking on link
fields. For example, you can select an item and click on the Qty Shipped label
to open the Purchasing Item Receipts Zoom window, where you can view the
invoiced and shipped quantities of the item.

![](media/45df5d29b413fca3da9d397578a42431.jpg)

**To view item information for purchasing documents:**

1.  Open the Purchase Order Processing Item Inquiry window.

>   (Purchasing \>\> Inquiry \>\> Purchase Order Items)

![](media/366de2d9b2be07977a5b6129f5904fcf.jpg)

1.  From the Items list, select Item (your item number) or Vendor Item (your
    vendor’s item number).

2.  Select All to view all items or select a range of items.

3.  From the Restrict By list, select an additional range to further restrict
    your inquiry. You can select one of the following options from the list.

>   **Promised Date** To view items from the date the vendor promised that you
>   would receive the merchandise or services.

>   **Required Date** To view items from the date you must receive all the
>   items.

>   **Promised Ship Date** To view items from the date the vendor promised to
>   ship the merchandise or services you’ve ordered.

>   **Requested By** To view the items ordered by a department or person.

>   **Vendor ID** To view items from a particular vendor.

>   **Description or Vendor Description (if you are viewing vendor items**) To
>   restrict items by description.

>   **On Order Qty** To view the items by their on order quantities.

>   **Project Number** To view items assigned to a project. This option is
>   available if you are using Project Accounting.

>   **Cost Category ID** To view items assigned to a cost category ID. This
>   option is available if you are using Project Accounting.

1.  Select All or select a range of items that meet the additional restriction.

2.  Select whether to display items at all sites or a specific site.

3.  Select to sort results by purchase order number or vendor ID.

4.  Select whether to include open purchase orders, historical purchase orders
    or both.

5.  Choose Redisplay to display the items in the scrolling window. To print the
    Purchase Order Processing Item Inquiry Report, choose File \>\> Print.

6.  Highlight a record and click a link to open a window to view more detailed
    information (optional).

>   The following table shows the link field and the window that the link opens.

| **Link field**                                                   | **Window that opens**                    |
|------------------------------------------------------------------|------------------------------------------|
| PO Number                                                        | Purchase Order Inquiry Zoom window       |
| Vendor ID                                                        | Vendor Inquiry window                    |
| Vendor Item                                                      | Item Vendors Maintenance window          |
| Item                                                             | Item Inquiry window                      |
| Qty Shipped and Qty Invoiced                                     | Purchasing Item Receipts Zoom window     |
| Project Number (available if you are using Project Accounting)   | PA Project Inquiry window                |
| Cost Category ID (available if you are using Project Accounting) | Cost Category Maintenance Inquiry window |

**Chapter 26: Reports**

>   Purchase Order Processing reports help you analyze purchasing and receiving
>   activity and pinpoint errors in transaction entry. Use this information to
>   guide you through printing reports, and working with report options.

>   For more information about creating and printing reports, using sample
>   reports and modified reports from the Reports Library, and the various
>   reporting tools that you can use with Microsoft Dynamics GP, refer to your
>   System User's Guide (Help \>\> Contents \>\> select Using The System).

>   Reports information is divided into the following sections:

-   *Purchase Order Processing standard reports summary*

-   *Specifying a Purchase Order Processing report option*

-   *Microsoft SQL Server® Reporting Services reports in Purchase Order
    Processing*

#### Purchase Order Processing standard reports summary

>   You can print several types of reports using Purchase Order Processing. Some
>   reports automatically are printed when you complete certain procedures; for
>   example, posting journals can be printed automatically when you post
>   transactions, depending on how your posting options are set up. You can
>   choose to print some reports during procedures; for example, you can print
>   an edit list when entering transactions by choosing the Print button in the
>   batch entry window. In order to print some reports, such as analysis or
>   history reports, you must set up report options to specify sorting options
>   and ranges of information to include on the report. For more information,
>   refer to *Specifying a Purchase Order Processing report option*.

>   The following table lists the report types available in Purchase Order
>   Processing and the reports that fall into those categories. (Reports printed
>   using Payables Management are printed using many of the same windows. Refer
>   to the Payables

>   Management documentation for information about reports printed in that
>   module.)

| **Report type**                                                                    | **Report**         | **Printing method**                                                                                              |
|------------------------------------------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------|
| Setup reports/Lists                                                                | Buyer ID List      | Choose File \>\> Print in the setup windows **or** create report options in the Purchasing Setup Reports window. |
| Documents                                                                          | Purchase Order \*† | Select a document in the                                                                                         |
| \* Indicates reports that can be printed with multicurrency information displayed. |                    |                                                                                                                  |

>   Purchase Order Generator Site Mapping List

>   Purchase Order Processing Setup

>   List

>   Receivings User-Defined Fields

>   Setup List

>   Blanket Purchase Order Delivery

>   Schedule\*

>   Purchase Order Entry window and choose File \>\> Print to print a single
>   document or choose File \>\> Print in the Purchase Order

>   Inquiry Zoom window. Choose

>   Transactions \>\> Print Purchasing Documents to print a range of documents.

>   † Indicates reports that can be assigned to named printers. For more
>   information, refer to your System Administrator’s Guide (Help \>\> Contents
>   \>\> select System Administration).

**P A R T 5** I N Q U I R I E S A N D R E P O R T S

| **Report type**                                                                    | **Report**                     | **Printing method**                                                                                                                               |
|------------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Posting reports                                                                    | Back Ordered Items Received    | Choose File \>\> Print in the window you use to complete the procedure **or** some will be printed automatically when you complete the procedure. |
| Edit lists                                                                         | Purchasing Invoice Edit List\* | Choose File \>\> Print in the window you used to complete the procedure.                                                                          |
| History reports                                                                    | Distribution History Report    | Create report options in the Purchasing History Reports window.                                                                                   |
| \* Indicates reports that can be printed with multicurrency information displayed. |                                |                                                                                                                                                   |

>   Report

>   Purchasing Voided Journal\*

>   Purchasing Voided Journal

>   Currency Summary\*

>   Cost Variance Journal\*

>   Invoice Cost Variance Journal

>   Edit PO Status Cost Variance

>   Journal

>   Edit PO Status Distribution Detail

>   Purchase Receipts Update Detail

>   Purchasing Invoice Distribution

>   Detail\*

>   Purchasing Invoice Posting

>   Journal\*

>   Purchasing Invoice Posting Journal

>   Currency Summary\*

>   Receivings Distribution Detail\*

>   Receivings Posting Journal\*

>   Receivings Posting Journal Currency Summary\*

>   Receivings Voided Journal\*

>   Receivings Voided Journal

>   Currency Summary\*

>   Returns Posting Journal\*

>   Returns Posting Journal Currency

>   Summary

>   Returns Distribution Detail\*

>   Returns Cost Variance Journal\*

>   Voided Purchase Invoice Journal\*

>   Voided Purchase Invoice Journal

>   Currency Summary\*

>   Purchasing Invoice Edit List

>   Currency Summary\*

>   Receivings Edit List\*

>   Receivings Edit List Currency

>   Summary\*

>   Returns documents\*

>   Returns Edit List\*

>   Returns Edit List Currency

>   Summary\*

>   Suggested Purchase Orders

>   Distribution Detail History

>   (purchase order returns)

>   Purchase Order History Report

>   Receivings Trx History Report

>   Returns Trx History – Summary

>   Returns Trx History – Detail

>   † Indicates reports that can be assigned to named printers. For more
>   information, refer to your System Administrator’s Guide (Help \>\> Contents
>   \>\> select System Administration).

290 P U R C H A S E O R D E R P R O C E S S I N G **C H A P T E R 2 6** R E P O
R T S

| **Report type**                                                                                                                                                                                                                                                         | **Report**                                                                                                                                                                                                        | **Printing method**                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Utility reports                                                                                                                                                                                                                                                         | Account Distribution Removal Report Completed PO Removal Report Journal History Removal Report Purchase Order Trx History Removal Report Receivings Trx Removal Report Reconcile Purchasing Documents Report      | These reports will be printed when you complete the corresponding procedure. |
| Analysis reports                                                                                                                                                                                                                                                        | Back-Ordered Items Received† Expected Shipments† Purchase Order Analysis† Purchase Order Status Report† PO Line Items to Release Report† Received/Not Invoiced Report† Shipment/Invoice Matching Activity Report† | Create report options in the Purchasing Analysis Reports window.             |
| Processing reports                                                                                                                                                                                                                                                      | Print Documents Exception Report Purchase Order Edited Status Journal Purchase Order Generated Purchase Order Generated Error Log Purchasing Voided Journal\* Purchasing Voided Journal Currency Summary\*        | These reports will be printed when you complete the corresponding procedure. |
| Inquiry reports                                                                                                                                                                                                                                                         | Purchase Order Processing Item Inquiry Document Inquiry Report                                                                                                                                                    | Choose File \>\> Print in the corresponding Inquiry window.                  |
| \* Indicates reports that can be printed with multicurrency information displayed. † Indicates reports that can be assigned to named printers. For more information, refer to your System Administrator’s Guide (Help \>\> Contents \>\> select System Administration). |                                                                                                                                                                                                                   |                                                                              |

#### Specifying a Purchase Order Processing report option

>   Report options include specifications for sorting options and range
>   restrictions for a particular report. In order to print several Purchase
>   Order Processing reports, you must first create a report option. Each report
>   can have several different options so that you can easily print the
>   information you need. For example, you can create report options for the
>   Purchase Order Status Report that show either detailed or summary
>   information.

>   *A single report option can’t be used by multiple reports. If you want
>   identical options for several reports, you must create them separately.*

>   Use the Purchasing series report options windows to create sorting,
>   restriction, and printing options for the reports that have been included
>   with Purchase Order Processing.

**P A R T 5** I N Q U I R I E S A N D R E P O R T S

**To specify a Purchase Order Processing report option:**

1.  Open a Purchasing reports window. There are separate windows for each report
    type.

>   (Purchasing \>\> Reports \>\> Setup/Lists)

>   (Purchasing \>\> Reports \>\> Analysis)

>   (Purchasing \>\> Reports \>\> Posting Journals)

>   (Purchasing \>\> Reports \>\> History)

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
>   you can insert one vendor ID restriction (ADVANCED0001 to BEAUMONT0001) or
>   one document number restriction (PO0001 to PO0299).*

1.  Choose Insert to insert the range in the Restrictions List. To remove an
    existing range from the list, select the range and choose Remove.

2.  Choose Destination to select a printing destination. Reports can be printed
    to the screen, to the printer, to a file or to any combination of these
    options. If you select Ask Each Time, you can select printing options each
    time you print this report option.

>   For more information about printing reports, refer to your System User's
>   Guide (Help \>\> Contents \>\> select Using The System).

1.  To print the report option from the report options window, choose Print
    before saving it. If you don’t want to print the option now, choose Save and
    close the window. The report window will be redisplayed.

#### Microsoft SQL Server® Reporting Services reports in Purchase Order Processing

You can view Purchase Order Processing Reporting Services reports from the
Reporting Services Reports list. If you are using Reporting Services 2008,
purchasing metrics for your home page also appear in the Reporting Services
Reports list. You can access the Reporting Services Reports list from the
navigation pane or from an area page in the Microsoft Dynamics GP application
window. This report list appears if you specified the location of your Reporting
Services reports using the Reporting Tools Setup window. See your System Setup
Guide (Help \>\> Contents \>\> select Setting up the System) for more
information.

>   **C H A P T E R 2 6** R E P O R T S

>   The following Reporting Services reports are available for Purchase Order
>   Processing.

| Back-ordered Items Received | Purchase Order Status  |
|-----------------------------|------------------------|
| Expected Shipments          | Received Not Invoiced  |
| Purchase Order History      | Receivings Trx History |

>   **To print a Reporting Services report:**

1.  In the navigation pane, choose the Purchasing button, and then choose the
    Reporting Services Reports list.

2.  Mark the Purchase Order Processing report that you want to print.

3.  In the Actions group, choose View to open the Report Viewer.

4.  In the Report Viewer, select the specifications for the report and choose
    View Report.

After viewing the report, select a format and print the report.

**Part 6: Utilities**

>   This part of the documentation explains how to maintain your Purchase Order
>   Processing data. Once you’ve determined how much historical information is
>   necessary, you can remove the information that’s no longer needed.

>   Be sure to back up your accounting data before performing any of these
>   procedures, because they remove historical data from your system.

>   The following topics are discussed:

-   *Chapter 27, “Purchase order history removal,”* explains the different types
    of historical information you can keep in Purchase Order Processing, and
    describes how remove historical information that is no longer needed.

-   *Chapter 28, “Purchase order reconciliation,”* describes reconciliation, the
    process of verifying that your accounting records are accurate.

**Chapter 27: Purchase order history removal**

>   History records provide useful information for auditing purposes. If you’re
>   keeping history, you can maintain and review records for an unlimited number
>   of years. Because historical records increase the amount of hard disk space
>   needed, you should remove history periodically to ensure that you’re keeping
>   only the information you need.

>   This information is divided into the following sections:

-   *Purchase Order Processing history types*

-   *Removing purchasing history*

-   *Removing tax history*

-   *Removing Intrastat history*

#### Purchase Order Processing history types

>   Purchase Order Processing allows you to maintain four types of history:
>   purchase order, receipt, account distribution, and journal. When you remove
>   purchasing history, select one of the four history types for the date range
>   you want to remove.

>   **Account Distributions** Select Account Distributions to remove account
>   distribution history without also removing receipts. Distribution history
>   includes a detailed list of each account and amount posted to the General
>   Ledger, including the audit trail code, account number, account description,
>   debit or credit amount. Once account distribution history has been removed,
>   the documents in the range you’ve removed won’t be printed on the
>   Distribution History Report.

>   **Purchase Order** Select Purchase Order to remove purchase order history.
>   If you’re keeping purchase order history, line-by-line detail of all the
>   information entered for each purchase order has been kept. When voiding a
>   new purchase order or removing a completed purchase order, the purchase
>   order is transferred to history. Once purchase order history has been
>   removed, the documents in the range you’ve removed won’t be printed on the
>   Purchase Order History Report.

>   When removing purchase order history, you can remove document attachments
>   with the purchase orders or just the attachments assigned to purchase
>   orders. The attachments are not removed from where they are stored. The
>   Attachments Only option is available if you are using document attachments
>   or have attachments assigned to purchase orders or purchase order line
>   items.

>   **Receipt** Select Receipt to remove detailed information about shipment and
>   invoice receipts. If you’re keeping receipt history, line-by-line detail of
>   all the information entered on each receipt has been kept, including landed
>   costs, lot numbers, serial numbers, and bin information. Once receipt
>   history has been removed, the documents in the range you’ve removed won’t be
>   printed on the Receivings Transaction History Report.

>   When removing receipt history, you can remove document attachments with the
>   receipts or just the attachments assigned to receipts. The attachments are
>   not removed from where they are stored. The Attachments Only option is
>   available if you are using document attachments or have attachments assigned
>   to receipts or receipt line items.

By selecting Receipt, you also can remove purchase order returns history.

**P A R T 6** U T I L I T I E S

If you’ve marked Receipt, you can select to remove both the receipts and the
account distribution history for the receipts. Distribution history is a
detailed record of how receipt transactions have affected the balances of
posting accounts in General Ledger. When you remove account distribution
history, the audit trail code, account, account description, debit or credit
amounts and other information about receipts will be removed.

**Journal** Select Journal to remove posting journal history. If you’ve selected
to reprint Purchase Order Processing posting journals in the Audit Trail Codes
Setup window, the system will maintain the history necessary to reprint posting
journals whether you’ve marked to maintain history or not in the Purchase Order
Processing Setup window. Once journal history has been removed, you won’t be
able to reprint posting journals for the range of information you’re removing.

If you haven’t selected to maintain purchase order and receipt history in the
Purchase Order Processing Setup window, purchase orders will be deleted when
they’re removed using the Remove Completed Purchase Orders window. Receipts will
be deleted after they’ve been posted unless you’ve selected to reprint Purchase
Order Processing posting journals in the Audit Trail Codes Setup window. In this
case, the system will maintain the history necessary to reprint posting
journals.

If you are maintaining purchase order history, you may want to use the Remove
Completed Purchase Orders window to transfer closed or canceled purchase orders
to history.

#### Removing purchasing history

Use the Remove Purchasing History window to remove Purchase Order Processing
history. You also can remove Purchase Order Returns history. When you remove
history, any corresponding multicurrency information will be removed, as well.

>   *Before removing history, back up your company’s accounting data. For more
>   information about making backups, refer to your System Administrator’s Guide
>   (Help \>\> Contents \>\> select System Administration).*

>   **To remove purchasing history:**

1.  Open the Remove Purchasing History window.

>   (Purchasing \>\> Utilities \>\> Remove Purchasing History)

![](media/cd9e4e1dbe27979ea6c8c294a41d3324.jpg)

1.  Select a history type to remove.

>   If you remove purchase order history but not receipt history, you may notice
>   that information is missing when you view your receipts. The required date,
>   promised date, promised ship date, and comment ID information for the
>   purchase order will not appear when you view the receipt in the Receivings
>   Item Detail Inquiry Zoom window.

1.  Select whether you want to remove history and print the history removal
    report.

    -   To remove attachments without removing purchase order or receipt
        history, mark Attachments Only. This option is available if you are
        using document attachments or have attachments assigned to purchase
        orders, receipts or line items.

    -   To print a history removal report without removing history, mark Print
        Report Only.

>   Depending on the type of history you’re removing, you can print one of the
>   following reports:

-   Purchase Order Transaction History Removal Report

-   Receivings Transaction Removal Report

-   Account Distribution Removal Report

-   Journal History Removal Report

1.  Using the All, From, and To fields, define a restriction.

>   *If you enter a value in only one of the restriction fields, purchasing
>   history will be removed from the value you enter to either the beginning or
>   end of the records. For example, if you enter a starting value and the
>   ending value is blank, all purchasing history from the starting value to the
>   end of the records will be removed.*

1.  Choose Process to remove history or to print the removal report.

>   *If you aren’t keeping history and select to print the history removal
>   report, the report will be blank. The report also will be blank if no
>   records exist within the range you specified.*

#### Removing tax history

>   Use the Tax History Removal window to remove tax detail transactions. Only
>   the tax history for the range you specify will be removed. Once tax history
>   has been removed, the tax details in the range you’ve removed won’t be
>   printed on tax reports.

>   *Before removing history, back up your company*’*s accounting data. For more
>   information about making backups in Microsoft Dynamics GP, refer to your
>   System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

**To remove tax history:**

1.  Open the Tax History Removal window.

>   (Administration \>\> Utilities \>\> Company \>\> Remove Tax History)

![](media/2eccfb6fc397fb65f67509d1b9815c23.jpg)

1.  Select whether you want to remove tax detail transactions and print the Tax
    History Removal Report, remove the tax detail transactions, or print the Tax
    History Removal Report.

2.  Enter or select a range of tax history to remove or print a report of.

3.  Choose Insert to insert the range.

4.  Choose Process to remove tax history. If Print Tax History Removal Report
    was marked, the Tax History Removal Report will print.

#### Removing Intrastat history

Use the Remove Intrastat History window to remove Intrastat history records that
are no longer necessary. Only the Intrastat records for the range you specify
will be removed.

>   *Before removing history, back up your company*’*s accounting data. For more
>   information about making backups in Microsoft Dynamics GP, refer to your
>   System Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

Once history has been removed, you won’t be able to print the Intrastat removal
reports for the ranges of information you’ve removed.

>   **To remove Intrastat history:**

1.  Open the Remove Intrastat History window.

>   (Administration \>\> Utilities \>\> Company \>\> Remove Intrastat History)

1.  Select a range type for the historical information you want to remove.
    Define the beginning and the end of the range, then choose Insert to display
    the range.

>   *You can enter and insert additional ranges. However, you can enter only one
>   range for each range type. For example, if you enter a restriction
>   specifying that history should be deleted for customer records COMPUTER0003
>   through GRAHAMAR0001, you can*’*t enter another restriction for customer IDs
>   CONTINEN0001 through EXECUTIV0001.*

1.  Mark Remove Transactions, then mark Print Report to print the Intrastat
    removal reports for the range of customer records or vendor records you’ve
    specified. Print these reports to retain a permanent record of your past
    Intrastat records after you’ve cleared history.

>   *You can print the Intrastat removal reports without removing history. To do
>   so, mark only Print Report and choose OK.*

**Chapter 28: Purchase order reconciliation**

>   Reconciling is the process of verifying that your accounting records are
>   accurate. Reconcile Purchase Order Processing before reconciling Payables
>   Management or Inventory Control. It’s important that the purchasing
>   documents are correct since purchasing information may be altered and is
>   used when reconciling inventory quantities and payables accounts.

>   *Before reconciling purchase orders, back up your company’s accounting data.
>   For more information about making backups, refer to your System
>   Administrator’s Guide (Help \>\> Contents \>\> select System
>   Administration).*

>   This information is divided into the following topics:

-   *Printing a reconcile report*

-   *Reconciling purchase orders*

#### Printing a reconcile report

>   Use the Reconcile Purchasing Documents window to print the Reconcile
>   Purchasing Documents Report without reconciling your purchasing records. You
>   can print the report for all documents or a selected range of documents.

>   If you print this report before you reconcile, you can verify which
>   documents in the range will be reconciled before you actually reconcile the
>   records.

>   **To print a reconcile report:**

1.  Open the Reconcile Purchasing Documents window.

>   (Purchasing \>\> Utilities \>\> Reconcile Purchasing Documents)

![](media/e82282da36f58af3d56375493bdb5ff6.jpg)

1.  Using the All, To, and From fields, select a document range.

>   *If you’re creating a range, you must enter at least one value in the
>   restriction fields. If you enter a value in only one of the restriction
>   fields, the report will show purchase orders from the value you enter to
>   either the beginning or end of the records. For example, if you enter a
>   starting value and the ending value is blank, all purchase orders from the
>   starting value to the end of the records will be reconciled.*

1.  Select Print Report Only to print the Reconcile Purchasing Documents Report
    without reconciling.

2.  Choose Process. When processing is complete, the Reconcile Purchasing
    Documents Report will be printed. This report lists the purchasing documents
    that will be reconciled.

>   If the Reconcile Purchasing Documents Report indicates that an amount will
>   be adjusted for a specific purchasing document, review the document to
>   verify the accuracy of the changes that were made.

#### Reconciling purchase orders

Use the Reconcile Purchasing Documents window to reconcile your purchasing
records. You can reconcile all records or a selected range of records.

When you reconcile purchase orders, the following information will be
recalculated and adjusted, if needed:

-   Document quantity canceled

-   Quantities linked to sales line items

-   Line item status

-   Purchase order status

-   Line item extended cost

-   Remaining purchase order subtotals

-   Document subtotals

-   Document extended costs

-   Discount available

-   Trade discount

-   Taxes

-   Quantity ordered for the control blanket line item on blanket purchase
    orders and drop-ship blanket purchase orders

>   **To reconcile purchase orders:**

1.  Open the Reconcile Purchasing Documents window.

>   (Purchasing \>\> Utilities \>\> Reconcile Purchasing Documents)

![](media/90683de1d5ca76302c32a7c0d960cdc3.jpg)

1.  Using the All, To, and From fields, select a document range.

>   *If you’re creating a range, you must enter at least one value in the
>   restriction fields. If you enter a value in only one of the restriction
>   fields, purchase orders will be reconciled from the value you enter to
>   either the beginning or end of the records. For example, if you enter a
>   starting value and the ending value is blank, all purchase orders from the
>   starting value to the end of the records will be reconciled.*

1.  Select to reconcile and print the Reconcile Purchasing Documents Report.

>   Select Print Report Only to print the Reconcile Purchasing Documents Report
>   without reconciling. If you select the Print Report Only option before you
>   reconcile and print, you can verify which documents in the range will be
>   reconciled before you actually reconcile the documents.

1.  Choose Process to reconcile purchasing documents. When processing is
    complete, the Reconcile Purchasing Documents Report will be printed. This
    report lists the purchasing documents that were reconciled.

>   *If the Reconcile Purchasing Documents Report indicates that an amount has
>   been adjusted for a specific purchasing document, review the document to
>   verify the accuracy of the changes that were made.*

**Glossary**

#### 1099 statement

>   A report required by the US Internal Revenue Service for each vendor from
>   whom goods and services worth \$600 or more have been purchased within a
>   calendar year. There are three possible formats for a 1099: miscellaneous
>   (1099-MISC), interest (1099-INT) and dividend (1099-DIV).

#### 1099 vendor

>   A vendor from whom goods and services worth \$600 or more have been
>   purchased within a calendar year.

#### Active vendor

>   A vendor with whom business is being conducted on a regular basis.

#### Alert message

>   A message that appears when inappropriate, inadequate or unclear data or
>   instructions are issued, when data is not accessible or when a confirmation
>   is sought. Additional information about some alert messages and their causes
>   can be viewed by clicking the Help button in the alert message dialog box.
>   You can also choose Help \>\> About this item from the window where you
>   received the message and select the Messages tab.

#### Alignment form

>   A document that ensures text will be properly aligned when documents are
>   printed.

#### Audit trail

>   A series of permanent records used to track a transaction to the point where
>   it was originally entered in the accounting system. The audit trail can be
>   used to verify the accuracy of financial statements by outside accountants
>   or auditors.

#### Audit trail code

>   A series of alphanumeric characters providing a precise record of each
>   transaction and where it has been posted.

#### Backing up

>   The process of storing data on a secondary medium, usually on diskettes or
>   magnetic tape, in order to minimize the difficulty of recovering from data
>   loss. Backups should be performed routinely.

#### Batch

>   A group of transactions identified by a unique name or number. Batches are
>   used in computerized accounting to conveniently group transactions, both for
>   identification purposes and to speed up the posting process.

#### Batch inquiry

>   A window that shows which users are currently working with batches and the
>   status of those batches.

#### Batch-level posting

>   A posting method that allows transactions to be saved in batches so you can
>   post a batch whenever convenient. There are three types of batch-level
>   posting: batch posting, series posting, and master posting.

**Bin**

>   A storage device to hold discrete items.

#### Blanket purchase order

>   A document that lists a single item and the quantities that will be
>   delivered in a series of shipments, usually on specific dates. The item
>   quantities will be shipped to your business to be received into your
>   inventory.

#### BOL (Bill of Lading)

>   Identification number assigned to a shipment by the carrier.

#### Buyer

>   A person whose job includes vendor selection, negotiation, and purchase
>   order placement and follow-up.

#### Calendar year

>   An accounting period running from January 1 to December 31.

#### Calendar year history

>   Transaction history records maintained in a calendar-year format.

#### Canceled status

>   A purchase order is assigned Canceled status when all of the line items have
>   been canceled and haven’t been received against. If you change the purchase
>   order status to Canceled, then all of the line items will be canceled.

>   A line item with this status doesn’t have shipped or invoiced quantities. A
>   line item with a Canceled status can be changed to New or Change Order, but
>   not Closed.

#### Change Order status

>   This status occurs when a purchase order with a Released status has been
>   edited. A purchase order’s revision number increases every time its status
>   becomes Change Order. A Change Order status purchase order can’t be deleted
>   or voided, but it can be received against in the Receivings Transaction
>   Entry window. To remove a purchase order with a Change Order status, close
>   or cancel the purchase order and then transfer it to history.

>   A line item with this status has also been changed since it was released.
>   Change Order line items become Released when the purchase order is printed
>   again.

#### Closed status

>   A purchase order is assigned this status when all of the line items for the
>   purchase order have been closed or canceled.

>   A line item with a Closed status can’t be reopened or change its status to
>   Canceled.

#### Control blanket line item

>   The first line item entered for a blanket or drop-ship blanket purchase
>   order is and has the line number 0. Blanket line items are based on this is
>   the line item. It can’t be received or invoiced against.

#### Comma-delimited field

>   The standard comma-separated ASCII character format used when exporting a
>   report so that it can be read by database programs.

#### Comment ID

>   Identifies a particular comment that will be printed on a purchase order.
>   Comments for each line item can be entered also.

#### Default entry

>   A value that is displayed in a window automatically, and that will be used
>   unless a different value is entered.

#### Default site

>   A site ID selected in the Item Quantities Maintenance window that identifies
>   an item’s primary storage location.

#### Detailed report

>   A report that displays detailed transaction information for each account.

#### Discount available

>   A reduction in the amount payable, typically offered if the payment is made
>   by a certain date.

#### Discount date

>   The date an invoice must be paid for a discount to be valid.

#### Discount taken

>   A valid discount applied to a vendor document. *See also Discount
>   available*.

#### Distributing

>   The process of allocating to separate accounts a percentage or part of
>   transaction amounts.

#### Distribution accounts

>   Accounts designated to receive a percentage or part of a posted transaction.

#### Distribution history

>   A record of the debits and credits for each document that was distributed to
>   individual posting accounts.

#### Document type

>   A selection that identifies a document’s purpose and how document amounts
>   will be posted.

#### Drop-ship blanket purchase order

>   A document that lists a single item and the quantities that will be
>   delivered to the customer in a series of shipments, usually on specific
>   dates. The vendor sends you an invoice and you, in turn, send an invoice to
>   the customer.

#### Drop-ship purchase order

>   A document whose items will be shipped directly to the customer. The vendor
>   will invoice your business and you, in turn, will invoice the customer.

#### Edit list

>   A list of transactions in an unposted batch that can be printed to verify
>   the accuracy of transactions before posting. Edit lists can be printed from
>   the Batch Entry window or any transaction entry window as long as a batch ID
>   has been entered.

#### EOM (End of Month)

>   A payment term requiring payment at month-end for all purchases made during
>   that month.

**Error message**

>   *See Alert message*.

**Financial year**

>   *See Fiscal year*.

#### Fiscal period

>   Division of the fiscal year, usually monthly, quarterly, or semiannually,
>   when transaction information can be summarized and financial statements are
>   prepared.

#### Fiscal year

>   An annual accounting cycle of up to 54 consecutive periods, ordinarily
>   beginning with the first day of a month and ending on the last day of the
>   twelfth month. In Australia and New Zealand, this is referred to as a
>   financial year.

#### Fiscal year history

>   A record of purchases, payments and other transactions for a historical
>   year.

#### FOB (Free on Board)

>   Terms of sale that identify when ownership passes to the buyer. An FOB of
>   Origin means that ownership transfers to the buyer when the vendor delivers
>   the goods to the carrier. An FOB of Destination means that ownership
>   transfers to the buyer when the goods are received from the carrier. The FOB
>   is especially important when in-transit damages occur.

#### Group printing

>   Creating and printing report options in groups. For example, a report group
>   could be used to print all the financial statements and the Trial Balance
>   before closing a month, quarter, or fiscal year.

#### GST (Goods and Services Tax)

>   A federal tax on the consumption of goods and services used in Canada, New
>   Zealand and other countries.

#### Hold

>   A way to temporarily stop further processing on a purchase order.

#### Inactive vendor

>   A vendor with whom business isn’t being conducted. Typically, these vendors
>   can’t be deleted because historical records are being maintained.

#### Inquiry

>   A feature that allows users to view currentyear and historical information.

#### In-transit inventory receipt

>   A document used to record the receipt of the material into the final
>   destination site.

#### Intrastat statistics

>   The system for collecting statistics on the trade of goods between European
>   Union countries.

#### Invoice

>   The bill provided by the seller to the buyer for items that have been
>   purchased.

#### Landed cost

>   The cost of an item that includes the cost from the vendor plus any
>   additional costs, such as duty, freight, import taxes, handling fees, and so
>   on, to get the item into inventory.

#### Lookup window

>   A window that displays a list of accounts, customers, documents, or other
>   items in the system. Lookup windows for a specific field are displayed by
>   clicking the lookup button next to the field.

#### Lot number

>   A number that describes items that were created at the same time and have
>   the same characteristics, such as the dye used when manufacturing fabrics
>   and carpet.

#### Master posting

>   A posting process in which marked batches from different series can be
>   posted simultaneously.

#### Miscellaneous charge

>   A charge that isn’t part of the normal purchasing process. A miscellaneous
>   charge may be a service charge such as installation or repair of
>   merchandise.

#### New status

>   A purchase order or line item is assigned to this status when it is saved
>   for the first time. A purchase order or line item that has a New status can
>   be deleted or voided. A New purchase order or line item will automatically
>   change from New to Released when the purchase order is printed.

>   When a shipment, shipment/invoice or invoice is posted against a line item,
>   the purchase order status and line item status will change from New to
>   Released.

#### Note

>   A feature that is used to attach messages to windows and fields throughout
>   the system. The Note button also shows whether a note is attached to a
>   window. Notes can be edited, reattached, and deleted.

#### Payment terms

>   Conditions for payment agreed upon when a purchase transaction takes place.
>   For example, a vendor might extend a discount if payment is received within
>   a specified time period.

#### Periodic valuation method

>   Detailed information for the cost of all items is maintained. The current
>   cost for an item is the cost the last time it was received. Items are valued
>   at standard cost.

#### Perpetual valuation method

>   Detailed information for the cost of all items is maintained. The current
>   cost for an item is the cost the last time it was received. Items are valued
>   at actual cost.

#### Posting

>   A procedure to make transactions a part of permanent records or to update
>   accounts by transaction amounts. In manual accounting, posting transfers
>   journal entries to the proper accounts in a general ledger.

#### Posting account

>   A financial account that tracks assets, liabilities, revenue, or expenses.
>   These accounts will appear on the financial statements and other reports
>   created in the financial series.

#### Posting journal

>   A report printed following the posting process that shows the detail for
>   each transaction that has been posted. Posting journals also include the
>   audit trail code, which is a precise record of where each transaction has
>   been posted.

#### Pro No. (Progressive Number)

>   Identification number assigned to a shipment by the carrier.

#### Promised date

>   Date the vendor promised that you would receive merchandise or services.

#### Promised ship date

>   Date the vendor promised to ship the merchandise or services you’ve ordered.

#### PST (Provincial Sales Tax)

>   A tax for the Canadian provinces that is set by each province.

#### Purchase order

>   A document authorizing a seller to deliver goods with payment to be made
>   later.

#### Purchase order status

>   The status of a purchase order indicates whether all line items on a
>   purchase order have been received. You can change the status of the purchase
>   order in the Edit Purchase Order Status window. Refer to the definitions of
>   individual statuses.

#### QST (Québec Sales Tax)

>   The Provincial Sales Tax for the province of Québec. *See also PST
>   (Provincial Sales Tax)*.

#### Range

>   A selection used to narrow the amount of records that will be printed on a
>   report. For example, a selected range of vendor IDs could be those between
>   5000 and 6000.

**Real-time posting**

>   *See Transaction-level posting*.

#### Receipt

>   A document recording the shipment of items that have been ordered from a
>   vendor via a purchase order. Also refers to a document for invoicing the
>   items received.

#### Receiving

>   Recording the receipt (shipment) of items that have been ordered from a
>   vendor via a purchase order. Receiving also can refer to recording the
>   invoice for the items received.

#### Received status

>   When items for a purchase order have been fully received, but not invoiced,
>   the purchase order is assigned this status. A Received purchase order can’t
>   be deleted or voided, but it can be received against in the Purchasing
>   Invoice Entry window. To remove a purchase order with a Received status,
>   close the purchase order and then transfer it to history.

>   A line item with this status has fully received shipments, but no invoice
>   receipts.

#### Reconciling

>   A procedure used to verify that Purchase Order Processing data is accurate.
>   Reconciling in Purchase Order Processing involves only purchase order
>   documents. Reconciling is often performed after rebuilding a file, and is
>   necessary after changing fiscal periods.

#### Release by date

>   Date a purchase order line item should be released to the vendor.

#### Released status

>   When a purchase order is printed or received against, it’s assigned this
>   status. A Released purchase order can’t be deleted or voided, but it can be
>   received against in the Receivings Transaction Entry window. To remove a
>   purchase order with a Released status, close or cancel the purchase order
>   and then transfer it to history.

>   A line item with this status either doesn’t have quantities shipped or
>   invoiced or has partially shipped or invoiced quantities.

#### Remove history

>   A procedure used to erase ranges of historical information that are no
>   longer useful.

#### Report option

>   A collection of entries that specify the amount of information or the type
>   of information that will appear on a report.

>   Multiple report options can be created.

**Required date**

>   Date you must receive items.

#### Serial number

>   A number that is one of a series and is assigned to a specific inventory
>   item to identify it and differentiate it from similar items with the same
>   item number. Serial numbers allow you to track an individual item from the
>   time you receive it until you sell it.

#### Serial number mask

>   A pre-defined format for serial numbers of Inventory items. If an item has
>   been identified as being tracked by serial numbers, the mask is used to
>   generate the starting serial number used when you automatically generate
>   serial numbers.

#### Series

>   A group of modules that form an interrelated set of applications. For
>   example, Purchase Order Processing is part of the Purchasing series.

#### Series posting

>   A posting process in which marked batches from the same series can be posted
>   simultaneously.

#### Shipment receipt

>   The document used to record merchandise received from a vendor.

#### Shipping method

>   The means used to send goods from a vendor. Also, the expected arrival time
>   of a shipment.

#### Site

>   A store, warehouse or other building from which you do business or store
>   items.

#### Standard cost

>   A predetermined cost associated with an item that has a periodic valuation
>   method. Standard costs are compared to actual costs to compute price
>   variances.

#### Standard purchase order

>   A document whose items will be shipped to your business to be received into
>   your inventory.

#### Summary report

>   A report summarizing the transactions made to a particular record.

#### Tab-delimited field

>   The tab-separated ASCII character format used for exporting a report.

#### Tax detail

>   A definition of a tax that may apply to customers. Tax details are grouped
>   into tax schedules. *See also Tax schedule*.

#### Tax schedule

>   Groups of tax details that define each tax that may apply to customers,
>   items, or other taxable costs. Tax schedules are used to determine which
>   taxes apply to individual sales.

#### Temporary vendor

>   A vendor used on a one-time or occasional basis. An example might be a
>   caterer for a company party.

#### Text-only format

>   A file format that saves reports as text without formatting. This format is
>   used when exporting reports to applications that are unable to read other
>   formats available in Microsoft Dynamics GP.

#### Trade discount

>   A discount given by a vendor. The rate is calculated at the time of a
>   purchase.

#### Transaction date

>   The date a transaction occurred; not necessarily the date it was entered in
>   the system.

**Transaction history**

>   A record of a fully applied transaction.

#### Transaction-level posting

>   A posting method in which transactions can be entered and posted without
>   having to create a batch. Also know as real-time posting. *See also
>   Batch-level posting*.

**Unit cost**

>   The amount per unit paid for an item.

#### Unit of measure

>   A user-defined unit in which you purchase or sell an item, such as each,
>   pair or case.

#### Valuation method

>   The method by which you track the cost of an item from the time you receive
>   it until you sell it. Different businesses and industries use different
>   valuation methods, which are sometimes specified by law.

#### VAT (Value-Added Tax)

>   A sales tax used in Europe and elsewhere in the world.

#### Vendor

>   A person or company providing goods or services in return for payment.

#### Vendor ID

>   An alphanumeric identification assigned to a vendor in Payables Management
>   setup. The vendor ID can be used to sort information for reports.

#### Voiding

>   The process of recording a transaction to reverse the effect of an original
>   transaction.

#### ZIP code

>   In the United States, the postal code assigned to business and residential
>   addresses. In other countries/regions, it may be referred to as post code or
>   postal code.
