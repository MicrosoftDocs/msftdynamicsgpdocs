---
title: Additional User-Defined Fields
description: New in october 2020 - Additional User Defined Fields
ms.date: 10/01/2020
ms.topic: article
ms.prod: dynamics-gp
author: theley502
ms.author: theley
manager: edupont
---

# Additional User-Defined Fields in General Ledger Transaction Entry

In the General Ledger Transaction Entry window there are now two new user defined fields. When users enter transactions into the General Ledger, they like to add information/comments regarding the transactions.

User Define labels for the user defined fields are at the bottom of the General Ledger Setup Window.

Go to Financial Home Page, under Setup, click Financial and choose General Ledger.

The field length for the User defined label is the same as the other user defined label fields which is 15. The size of the user defined fields is 30 characters in the transaction entry window.

The User Defined fields are added to the following reports:

* Edit list
* Posting journal

The fields are available in Report Writer to be added to other reports as needed.

The size of the user defined fields is 30 characters in the transaction entry window.

## Table Changes

| **Table Physical Names**   | **Table Technical Name** | **New field**        |
|-----------------------------|---------------------------|-----------------------|
| GL20000                     | GL\_YTD\_TRX\_OPEN        | User\_Defined\_Text01 |
| GL20000                     | GL\_YTD\_TRX\_OPEN        | User\_Defined\_Text02 |
| GL30000                     | GL\_YTD\_TRX\_HIST        | User\_Defined\_Text01 |
| GL30000                     | GL\_YTD\_TRX\_HIST        | User\_Defined\_Text02 |

Go to the Financial Home Page, under Setup, click Financial and choose General Ledger.

<img src="media/image1.png" alt="General Ledger Setup" width="343" height="402" />

To see the User Defined fields you setup above you can go to Transaction choose Financial and General

<img src="media/image2.png" alt="Transaction Entry" width="375" height="354" />

Example report for the General Posting Journal

<img src="media/image3.png" alt="General Posting Journal" width="495" height="315" />

Once a transaction has been posted with user defined information populated you will be able to see this in the inquiry windows. Located under the Financial Home page, choose Inquiry, then Financial and Journal Entry Inquiry

<img src="media/image4.png" alt="Journal Entry Inquiry" width="444" height="395" />

You can also add the new Extra fields to a SmartList. We can also use the new feature to quickly add multiple fields at once to a SmartList!

<img src="media/image5.png" alt="Dialog showing Change Column Display" width="519" height="334" />

<img src="media/image6.png" alt="Dialog showing columns" width="393" height="338" />


