---
title: "Glossary"
description: "Terminology used in the Distribution area in Dynamics GP."
keywords: "banking, bank reconciliation"
author: theley502
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 01/25/2019
---
# Glossary of Terms in the Distribution Area in Dynamics GP

The following table explains the terminology used in the Distribution area in Dynamics GP.

|Term          |Definition                                                         |
|--------------|-------------------------------------------------------------------|
|1099 statement|A report required by the US Internal Revenue Service for each vendor from whom goods and services worth \$600 or more have been purchased within a calendar year. There are three possible formats for a 1099: miscellaneous (1099-MISC), interest (1099-INT) and dividend (1099-DIV).|
|1099 vendor|A vendor from whom goods and services worth \$600 or more have been purchased within a calendar year.|
|Account alias|A “short name” for a posting account in the chart of accounts. If the account format has a large number of segments, using aliases can speed data entry.|
|Active customer| A customer with whom business is conducted on a regular basis.|
|Active vendor|A vendor with whom business is being conducted on a regular basis.|
|Advanced picking| Allows you to group picking tickets by specific criteria, print bulk picking tickets, print the customer item on the packing slip and invoice, and define customer specific picking instructions that are printed on the picking ticket.
|Alert message| A message that appears when inappropriate, inadequate or unclear data or instructions are issued, when data is not accessible or when a confirmation is sought.
|Alignment form| A document that ensures text will be properly aligned when documents are printed.|
|Allocating| The process of reserving the item in inventory. The item remains in inventory until fulfillment but isn’t available for sale.|
|Audit trail| A series of permanent records used to track a transaction to the point where it was originally entered. The audit trail can be used to verify the accuracy of financial statements by outside accountants or auditors.|
|Audit trail code| A series of alphanumeric characters providing a precise record of each transaction and where it has been posted.|
|Available to promise| The quantity available for a customer on a specific day by calculating on-hand inventory and transactions that increase or decrease inventory, such as sales orders, inventory adjustments, and purchase orders.|
|Back order| Orders that you place without adequate quantities on hand. For example, if you want to allocate five items from your inventory, but have only three on hand, you can back order the remaining two.|
|Backing up| The process of storing data on a secondary medium, usually on diskettes or magnetic tape, in order to minimize the difficulty of recovering from data loss. Backups should be performed routinely.|
|Bank card| A type of credit card. Bank cards include ATM cards that when used by a customer, funds are transferred directly into your bank account. Bank cards also include cards issued by a bank based on a credit rating and typically do not carry a credit limit. The bank that issued the card will see to it that the seller receives payment. Payments received from these cards are treated as check or cash payments.|
|Base unit of measure| The unit of measure that is common to all units of measure on a unit of measure schedule. The base is the smallest unit of measure on the schedule. For example, if a unit of measure schedule includes the following units of measure: each, pair and dozen, each would be the base unit of measure.|
|Batch| A group of transactions identified by a unique name or number. Batches are used to conveniently group transactions, both for identification purposes and to speed the posting process.|
|Batch approval| Allows users to choose whether to approve batches of transactions before posting. If the batch approval option is being used, the ID of the user who approved the batch and the approval date will appear on posting reports.|
|Batch controls| Values for both the number of transactions in a batch and the total currency amount of the batch. As transactions are entered, the actual totals will be displayed. These totals can be verified periodically as transactions are entered to ensure that the required number and amount of transactions match the actual number and amount that was entered.|
|Batch inquiry|A window that shows which users are currently working with batches and the status of those batches.|
|Batch-level posting|A posting method that allows transactions to be saved in batches so you can post a batch whenever convenient. There are three types of batch-level posting: batch posting, series posting, and master posting.|
|Batch list| A list of all the transactions—quotes, orders, invoices, back orders and returns—in an unposted batch. This report can be printed to verify the accuracy of transactions.|
|Bin| A location within a site where you store items, or a storage device to hold discrete items.|
|Blanket purchase order|A document that lists a single item and the quantities that will be delivered in a series of shipments, usually on specific dates. The item quantities will be shipped to your business to be received into your inventory.|
|BOL (Bill of Lading)|Identification number assigned to a shipment by the carrier.|
|Bulk picking ticket| A picking ticket that displays the items and quantities needed to fulfill more than one fulfillment order or invoice and the location of each item for a batch of items. You can print bulk picking tickets for fulfillment orders and invoices only.|
|Buyer|A person whose job includes vendor selection, negotiation, and purchase order placement and follow-up.|
|Calendar year|An accounting period running from January 1 to December 31.|
|Calendar year history|Transaction history records maintained in a calendar-year format.|
|Canceled status|A purchase order is assigned Canceled status when all of the line items have been canceled and haven’t been received against. If you change the purchase order status to Canceled, then all of the line items will be canceled.</br>A line item with this status doesn’t have shipped or invoiced quantities. A line item with a Canceled status can be changed to New or Change Order, but not Closed.|
|Change Order status|This status occurs when a purchase order with a Released status has been edited. A purchase order’s revision number increases every time its status becomes Change Order. A Change Order status purchase order can’t be deleted or voided, but it can be received against in the Receivings Transaction Entry window. To remove a purchase order with a Change Order status, close or cancel the purchase order and then transfer it to history. </br>A line item with this status has also been changed since it was released. Change Order line items become Released when the purchase order is printed again.|
|Charge card| A type of credit card. Charge cards are issued by banks and authorize the holder to buy goods or services on credit. Payments received from charge cards are treated as accounts receivable amounts because you must submit them to the card companies for reimbursement. You must receive reimbursement to consider the charged amounts paid.|
|Check card| A type of credit card. When purchases are made with a check card, the amount of purchase will be immediately withdrawn from the user’s bank account.|
|Checkbook| An account used to maintain a currency balance and track the receiving and disbursing of cash.|
|Class| A feature that allows customers, vendors, users or items to be grouped according to common characteristics. For example, a customer class could be created to group customers according to credit limit or location.|
|Closed status|A purchase order is assigned this status when all of the line items for the purchase order have been closed or canceled.</br>A line item with a Closed status can’t be reopened or change its status to Canceled.|
|Control blanket line item|The first line item entered for a blanket or drop-ship blanket purchase order is and has the line number 0. Blanket line items are based on this is the line item. It can’t be received or invoiced against.|
|Comma-delimited fields| The standard comma-separated ASCII character format used when exporting a report so that it can be read by database programs.|
|Comment ID| Identifies a particular comment that will be printed on a sales document. Comments for each line item can be entered also.|
|Credit card| Cards used to pay for items instead of a check, cash or other method. The amount due is then billed by the credit card company. Using the Credit Card Setup window, cards used to make payments can be classified as credit cards or check cards. Cards accepted as payment by a company can be classified as bank cards or charge cards.|
|Credit terms| Conditions agreed upon when credit is granted.|
|Customer item| The name that the customer uses for an item. For example, suppose the customer calls an item a White Board, but the item in your inventory is a Dry-Erase Board. White Board would be the customer item.|
|Default entry| A value that is displayed in a window automatically, and that will be used unless a different value is entered.|
|Default site| A site ID selected in Sales Order Processing Setup that identifies the location from which the most items are sold.|
|Deposit| An amount received when the customer places an order. Deposits are posted when they are entered on the order or back order and can be transferred to an invoice.|
|Discount available| A reduction in the amount receivable, typically offered to a customer if the payment is made by a certain date.|
|Discount date| The date an invoice must be paid for a discount to be valid.|
|Distributing| The process of allocating to separate accounts a percentage or part of transaction amounts.|
|Distribution accounts| Accounts designated to receive a percentage of transaction amounts posted to a fixed or variable allocation account or accounts designated to receive a percentage or part of posted transactions.|
|Distribution history| A record of the debits and credits for each document that was distributed to individual posting accounts.|
|Document status| Describes the step in the sales fulfillment workflow process that fulfillment orders and orders are at. Fulfillment order document statuses include:</br>1.  Ready to Print Picking Ticket</br>2.  Unconfirmed Pick</br>3.  Confirm Pick/Ready to Pack</br>4.  Unconfirmed Pack</br>5.  Shipped</br>6.  Ready to Print/Post</br>You can change the fulfillment order status descriptions, and activate or inactivate them. Order document statuses include New, In Process, and Complete.|
|Document type| A selection that identifies a document’s purpose and how document amounts will be posted. In Sales Order Processing, the document types include quotes, orders, invoices, back orders, and returns.|
|Drop-ship| A sale where the items are sent directly to the customer from your supplier. Drop-ship transactions have no effect on your inventory because the inventory is never adjusted to reflect increases or decreases in quantities.|
|Drop-ship blanket purchase order|A document that lists a single item and the quantities that will be delivered to the customer in a series of shipments, usually on specific dates. The vendor sends you an invoice and you, in turn, send an invoice to the customer.|
|Drop-ship purchase order|A document whose items will be shipped directly to the customer. The vendor will invoice your business and you, in turn, will invoice the customer.|
|Edit list| A list of transactions—invoices and returns—in an unposted batch that can be printed to verify the accuracy of transactions before posting.|
|EOM (End of Month)|A payment term requiring payment at month-end for all purchases made during that month.|
|Error message| See *Alert message*.|
|Expansion button| A button next to certain fields that opens another window. This window shows additional information related to the field. For example, the customer expansion button opens a window that contains additional information about the customer.|
|Extended price| The total price for each line item on a document calculated using the following formula for quotes, orders, returns and back orders: (Unit Price – Markdown) x Document Quantity = Extended Price and the following formula for invoices: (Unit Price - Markdown) x Billed Quantity = Extended Price.|
|Extended quantity| The quantity for the unit of measure restated in the base unit of measure. For example, if the base U of M is each, the U of M on the transaction is pair and the quantity is 3, the extended quantity will be 6.|
|Financial year|See *Fiscal year*.|
|Fiscal period|Division of the fiscal year, usually monthly, quarterly, or semiannually, when transaction information can be summarized and financial statements are prepared.|
|Fiscal year|An annual accounting cycle of up to 54 consecutive periods, ordinarily beginning with the first day of a month and ending on the last day of the twelfth month. In Australia and New Zealand, this is referred to as a financial year.|
|Fiscal year history|A record of purchases, payments and other transactions for a historical year.|
|Flat fee| An item type assigned to items with current costs but no quantities. For example, the fee for an extended warranty might be assigned a flat fee item type.|
|FOB (Free on Board)|Terms of sale that identify when ownership passes to the buyer. An FOB of Origin means that ownership transfers to the buyer when the vendor delivers the goods to the carrier. An FOB of Destination means that ownership transfers to the buyer when the goods are received from the carrier. The FOB is especially important when in-transit damages occur.|
|Free-forward| The total of available and pending quantities of an item, plus any additional quantities from purchase orders, assembly receipts, manufacturing orders, and sales returns that are displayed in the Inventory Available to Promise Inquiry window. The total sum is reduced by the item quantities from unallocated sales orders, sales back orders, and unallocated manufacturing components displayed in the Inventory Available to Promise Inquiry window.|
|Freight| An additional charge for shipping the item to the customer. You must manually enter freight amounts on a sales document.|
|Fulfill| Updates bin, serial-number, and lot-number information, but not item quantities.|
|Fulfillment| The process of identifying and verifying the items to satisfy an order or invoice. When you fulfill serial or lot numbers items, you must select the serial or lot number for the item. Items on an invoice must be fulfilled before the invoice can be posted.|
|Fulfillment order| A type of sales document that uses document statuses to provide additional structure and control over typical sales processes, such as printing the picking ticket, picking the goods, printing the packing slip, packing and shipping the goods, and sending the invoice to the customer. You can create a fulfillment order from a quote, a back order, or an order. You can create an invoice from a fulfillment order.|
|Functional currency| The primary currency in which a company maintains its financial records. Typically, the functional currency is the currency for the country or region where the company is located.|
|Group printing| Creating and printing report options in groups. For example, a report group could be used to print all the financial statements and the Trial Balance before closing a month, quarter or fiscal year.|
|GST (Goods and Services Tax)|A federal tax on the consumption of goods and services used in Canada, New Zealand and other countries.|
|History| A record of completed transactions or account balances. In Sales Order Processing, once a document has been transferred, voided or posted, it is automatically moved to history.|
|Hold|See *Process hold*.|
|Inactive customer|A customer with whom you no longer conduct business. Typically, records for these customers can’t be deleted because historical records are being maintained.|
|Inactive vendor|A vendor with whom business isn’t being conducted. Typically, these vendors can’t be deleted because historical records are being maintained.|
|In-transit inventory receipt|A document used to record the receipt of the material into the final destination site.|
|Intrastat| The system for collecting statistics on the trade of goods between European Union countries.|
|Intrastat statistics|The system for collecting statistics on the trade of goods between European Union countries.|
|Invoice| A document that records the prices and other details of goods and services sold or supplied. Invoices also are used to serve as part of the audit trail.|
|Item print option| Determines which items that are printed on bulk picking tickets, individual picking tickets, or both.|
|Kit| An item type that is assigned to items made up of components (other inventory items). Kits are not tracked in inventory. They are assembled at the time of sales and are sold as an individual item.|
|Landed cost|The cost of an item that includes the cost from the vendor plus any additional costs, such as duty, freight, import taxes, handling fees, and so on, to get the item into inventory.|
|Linking| The process of associating a sales line item with a line item on a purchase order. If you generate a purchase order from Sales Order Processing, the items are linked automatically. You also can link sales line items to existing purchase orders.|
|Lookup window| A window that displays a list of accounts, customers, jobs or other items. Lookup windows for a specific field are displayed by choosing the lookup button next to the field.|
|Lot number| A number that identifies items that were created at the same time and have the same characteristics, such as the dye used when manufacturing fabrics and carpet.|
|Markdown| The currency amount or percentage that is subtracted from the unit price of an item to determine a discounted selling price.|
|Master number| A single number assigned to a series of documents that is used to track related documents. For example, when a customer requests a quote, then places an order and receives an invoice for the items on the quote, each document will be assigned the same master number. (However, each document also maintains its own document number.)|
|Master posting| A posting process in which marked batches from different series can be posted simultaneously.|
|Miscellaneous charge| A charge that isn’t part of a normal purchasing process. A miscellaneous charge may be a service charge such as installation or repair of merchandise. You must manually enter miscellaneous charges on sales documents.|
|Miscellaneous charge item| An item type assigned to items that aren’t being tracked by quantity or current cost, such as shipping costs, customizing costs, or other costs that occur infrequently.|
|New status|A purchase order or line item is assigned to this status when it is saved for the first time. A purchase order or line item that has a New status can be deleted or voided. A New purchase order or line item will automatically change from New to Released when the purchase order is printed. When a shipment, shipment/invoice or invoice is posted against a line item, the purchase order status and line item status will change from New to Released.|
|Non-inventoried item| An item that is not set up and is not tracked in Inventory Control. If you enter a non-inventoried item on a sales document, the item will appear on sales reports but not inventory reports.|
|Note| A feature used to attach messages to windows and records. The note button shows whether a note is attached to a window. Notes can be edited and reattached, deleted or printed.|
|Object| An element of the tree view in the Purchase Orders Preview window. Each line in the tree is an object—and the objects are organized first by vendor, then by purchase order, then item, and finally sales document.|
|Order| A document that expresses a commitment by a customer to purchase items from you. Orders also are used as part of the audit trail.|
|Origin| A transaction entry window within a specific module. Certain options, such as closing fiscal periods can be selected for each transaction origin. Also, the transaction origin will appear as part of the audit trail code on all posting reports.|
|Originating currency| The currency that a multicurrency transaction is conducted in.|
|Packing slip| A document that displays the items and quantities that have been included in a shipment. Packing slips are often attached directly to the shipment when it is sent to the customer and can be used to verify that all invoiced items were included in the shipment.|
|Payment| An amount received that can’t be realized until after the order is shipped to the customer. Payment amounts are posted when the invoice or return is posted.|
|Payment terms| Conditions for payment agreed upon when a sales or purchase transaction takes place. Payment terms might include a discount to the selling price if the payment is received within a certain time period.|
|Pending purchase order| A purchase order that would be created from a sales order or back order but hasn’t been generated yet. You can view pending purchase orders in the Purchase Order Preview window.|
|Periodic valuation method|Detailed information for the cost of all items is maintained. The current cost for an item is the cost the last time it was received. Items are valued at standard cost.|
|Perpetual valuation method|Detailed information for the cost of all items is maintained. The current cost for an item is the cost the last time it was received. Items are valued at actual cost.|
|Picking instruction| Information that you can assign to a customer record or item record that might include information such as the sequence that items should be picked or that a forklift is required to pick an item.|
|Picking ticket| A document that displays the items and quantities on an order as well as the site and bin number. Picking tickets typically aren’t sent with the order, but are used by warehouse personnel when assembling the items on an order.|
|Posting| A procedure to make temporary transactions a part of permanent records or to update accounts with specific transaction amounts. In manual accounting, posting transfers journal entries to the appropriate accounts in a general ledger.|
|Posting account| A financial account that tracks assets, liabilities, revenue or expenses. These accounts will appear on the financial statements and other reports created in the financial series.|
|Posting journal| A report printed after the posting process that shows the detail for each transaction posted. Posting journals also include the audit trail code, which provides a precise record of where each transaction has been posted.|
|Primary vendor| The vendor you order the selected item from most often. The primary vendor is the default vendor when you generate purchase orders from Sales Order Processing.|
|Process hold| A user-defined restriction that prevents a document from further processing. In Sales Order Processing, you can set up an unlimited number of holds and assign them to various processes. For example, you can set up a hold that restricts posting until a manager has approved the documents.|
|Prospect customer| A customer that may become part of your customer base sometime in the future; a potential customer. Prospect customer records can be entered on quote documents only.|
|Pro No. (Progressive Number)|Identification number assigned to a shipment by the carrier.|
|Promised date|Date the vendor promised that you would receive merchandise or services.|
|Promised ship date|Date the vendor promised to ship the merchandise or services you’ve ordered.|
|PST (Provincial Sales Tax)|A tax for the Canadian provinces that is set by each province.|
|Purchase order|A document authorizing a seller to deliver goods with payment to be made later.|
|Purchase order status|The status of a purchase order indicates whether all line items on a purchase order have been received. You can change the status of the purchase order in the Edit Purchase Order Status window. Refer to the definitions of individual statuses.|
|Quote| A document that lists prices for items that a customer is interested in purchasing. Items on quotes are not allocated in inventory.</br> Quotes also are a part of the audit trail.|
|QST (Québec Sales Tax)|The Provincial Sales Tax for the province of Québec. See also *PST (Provincial Sales Tax)*.|
|Range|A selection used to narrow the amount of records that will be printed on a report. For example, a selected range of vendor IDs could be those between 5000 and 6000.|
|Real-time posting| See *Transaction-level posting*.|
|Receipt|A document recording the shipment of items that have been ordered from a vendor via a purchase order. Also refers to a document for invoicing the items received.|
|Receiving|Recording the receipt (shipment) of items that have been ordered from a vendor via a purchase order. Receiving also can refer to recording the invoice for the items received.|
|Received status|When items for a purchase order have been fully received, but not invoiced, the purchase order is assigned this status. A Received purchase order can’t be deleted or voided, but it can be received against in the Purchasing Invoice Entry window. To remove a purchase order with a Received status, close the purchase order and then transfer it to history.</br>A line item with this status has fully received shipments, but no invoice receipts.|
|Reconciling| A procedure used to verify that sales or purchase order processing data is accurate. Reconciling only involves unposted documents and verifies the quantity amounts and totals on the documents. Reconciling is often performed after rebuilding a file, and is necessary after changing fiscal periods.|
|Release by date|Date a purchase order line item should be released to the vendor.|
|Released status|When a purchase order is printed or received against, it’s assigned this status. A Released purchase order can’t be deleted or voided, but it can be received against in the Receivings Transaction Entry window. To remove a purchase order with a Released status, close or cancel the purchase order and then transfer it to history.</br>A line item with this status either doesn’t have quantities shipped or invoiced or has partially shipped or invoiced quantities.|
|Removing history| A procedure used to erase ranges of historical information. Additional hard disk space will become available when history has been removed and files have been shrunk.|
|Report option| A collection of entries that specify the amount of information or the type of information that will appear on a report. Multiple report options can be created for each report.|
|Return| A transaction that records the return of merchandise after the invoice has been posted. Return amounts are applied to the original invoice (for open item customers) or to the customer’s balance (for balance forward customers).|
|Return quantity type| A general category that returned items are assigned to. The categories are On Hand, In Use, In Service, Damaged or Returned. You can return items to any quantity type, but you can sell items only from the on hand quantity type.|
|Sales tax detail| See *Tax detail*.|
|Sales tax schedule| See *Tax schedule*.|
|Serial number|A number that is one of a series and is assigned to a specific inventory item to identify it and differentiate it from similar items with the same item number.|
|Serial number mask|A pre-defined format for serial numbers of Inventory items. If an item has been identified as being tracked by serial numbers, the mask is used to generate the starting serial number used when you automatically generate serial numbers.|
|Series|A group of modules that form an interrelated set of applications. For example, Purchase Order Processing is part of the Purchasing series.|
|Series posting|A posting process in which marked batches from the same series can be posted simultaneously.|
|Shipment receipt|The document used to record merchandise received from a vendor.|
|Shipping method|The means used to send goods from a vendor. Also, the expected arrival time of a shipment.|
|Site|A store, warehouse or other building from which you do business or store items.|
|Standard cost|A predetermined cost associated with an item that has a periodic valuation method. Standard costs are compared to actual costs to compute price variances.|
|Standard purchase order|A document whose items will be shipped to your business to be received into your inventory.|
|Substitute item| An inventoried item that can be sold in place of another inventoried item.|
|Summary report|A report summarizing the transactions made to a particular record.|
|Tab-delimited field| The tab-separated ASCII character format used when exporting a report.|
|Tax detail| A definition of a tax that may apply to customers. Tax details are grouped into tax schedules. See also *Tax schedule*.|
|Tax schedule| Groups of tax details that define each tax that may apply to customers, items or other taxable costs. Tax schedules are used to determine which taxes apply to individual sales.|
|Temporary vendor|A vendor used on a one-time or occasional basis. An example might be a caterer for a company party.|
|Terms discount taken| The discount amount customers take from their available payment terms discount.|
|Text-only format| A file format that saves reports as text without formatting. This format is used when exporting reports to applications that are unable to read other formats available.|
|Trade discount| A discount a customer always receives. The rate is calculated at the time of a sale and is given in addition to any payment term discounts that also may be offered. Trade discounts are set up for a customer in the Customer Maintenance window.|
|Transaction date|The date a transaction occurred; not necessarily the date it was entered in the system.|
|Transaction history|A record of a fully applied transaction.|
|Transaction-level posting| A posting method in which transactions can be entered and posted without having to create a batch. Also known as *real-time posting*. See also *Batch-level posting*.|
|Transferring| The process of transferring customer and item information from an existing document to a new document of a another type.|
|Tree view| The Purchase Orders Preview window uses a tree view to show pending or existing purchase orders. The tree view appears on the left side of the window. Each line in the tree is an object. Items selected in the tree view determine what is displayed in the other portion of the window.|
|Unit account| An account that tracks statistical or non financial quantities, like the number of customers with past-due balances or the number of invoices generated over a specific time period.|
|Unit cost| The amount per unit that you paid for an item you’re planning to sell or consume.|
|Unit of measure (U of M)| A user-defined unit in which you purchase or sell an item, such as each, pair or case. You can sell an item in multiple units of measure.|
|Unit price| The amount per unit you sell an item for. For example, if you sell a case of oil, the unit price is the price per can of oil.|
|VAT (Value-Added Tax)| A sales tax used in Europe and elsewhere in the world.|
|Workflow| The defining and tracking of a business process, during which tasks are completed and documents are passed from one individual or department to another to complete the next task in the process.|
|ZIP code| In the United States, the postal code assigned to business and residential addresses. In other countries/regions, it may be referred to as *post code* or *postal code.*|

## See Also

[Purchase Order Processing](purchase-order-processing.md)  
[Purchase Order Enhancements](purchase-order-enhancements.md)  
[Sales Order Processing](sales-order-processing.md)  
