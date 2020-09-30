---
title: HR Social Security Number Mask
description: New in October 2020 - Social Security Number Mask in Human Resources 
ms.date: 09-30-2020
ms.topic: article
ms.prod: dynamics-gp
author: theley502
ms.author: theley
manager: edupont
---

# Human Resources Social Security Number Mask

A few versions back, we added the Social Security Number (SSN) mask for payroll. That has prompted this request why don't we also do this on the Human Resource reports? Great question!

You can go to Tools, point to Setup, choose System, and click Human Resources Preferences.

Towards the bottom of the window you will see the button SSN Mask that was added.

By default on the install, everything will be marked as masked, if you would like to see the SSN on the report you will need to unmark it from this window.

<img src="media/image36.jpg" alt="Human Resource Preferences showing Report Masking of SSN and other PII" width="619" height="343" />

The reports can be found under Human Resource and Reports.

There are many, many Human Resource reports that have SSN on them, we picked a few of the top report's customers use my default.

You will find them in the sections of:

- Benefit reports

- Training reports

- Orientation reports

- Employee Summary and History reports

Here is an example of a report with SSN masked.

<img src="media/image42.jpg" alt="Report showing masked SSN for employees" width="528" height="172" />

Same report with it not masked in setup.

<img src="media/image43.jpg" alt="Report showing not-masked SSN for employees" width="561" height="156" />

> [!NOTE]
> There is no structure change in the table. Only the records will be added in UPR40203.out file.
>
> There is a row in this table for each report that we added, there is also a column in this table for MARKED. 1 means it is marked to mask SSN and 0 means it is not marked to mask SSN.
