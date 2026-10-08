---
title: What's new in Dynamics GP in October 2026
description: Learn about enhancements that were added to the product in the October 2026 release of Dynamics GP.
author: aeckman
ms.author: aeckman
ms.reviewer: jswymer
ms.topic: whats-new
ms.date: 10/21/2026
---
# What's New in Dynamics GP in October 2026

This article highlights the improvements introduced in the October 2026 release of Dynamics GP, which includes enhancements across various areas of the product.


**Core features**

## [See who last saved a SmartList](https://community.dynamics.com/blogs/post/?postid=e357fd3a-a692-f111-8076-000d3a54bc5d)

SmartList shows the user and date of the last saved change for built-in lists, SmartList Builder lists, and favorites. Existing records remain blank until saved after upgrading; running a list or making unsaved changes isn't tracked. Optional Activity Tracking can also record create, modify, and delete activity when enabled.

IMAGE HERE


## [Choose a date range before retrieving item history](https://community.dynamics.com/blogs/post/?postid=ac43f140-a892-f111-8076-000d3a54bc5d)

Item Stock Inquiry no longer loads document details as soon as you enter an item. Set your date range and other criteria, then select Redisplay to retrieve the details you need without automatically loading years of history. Inventory, costing, and posting behavior are unchanged.

IMAGE HERE 
Item Stock Inquiry: set the date criteria before selecting Redisplay.


## [Record a reason for voiding payables transactions](https://community.dynamics.com/blogs/post/?postid=4ad73617-bbc1-f111-aaad-3833c5e8605a)

Enable void reason codes in Payables Management Setup to capture why open or historical payables transactions are voided. You can make codes optional or required. Saved reasons appear in Payment Entry Zoom and Payables Transaction Entry Zoom, helping users understand the transaction's history.

IMAGE HERE
Payables setup: enable void reason codes and choose whether a reason is required.

IMAGE HERE
Payables Transaction Entry Zoom displays the reason saved with the voided transaction.

## [Complete workflow when a purchase order is canceled](https://community.dynamics.com/blogs/post/?postid=4a9ebe30-c4c1-f111-aaad-3833c5e8605a)

When all applicable remaining lines of a submitted purchase order are canceled through Edit Purchase Order Status and the header reaches Canceled, workflow automatically becomes Completed. Workflow history records the completion. Canceling only some lines does not complete workflow unless the header becomes Canceled.

IMAGE HERE
Workflow History records completion when the purchase order status changes to Canceled.


## [Identify companies by name and database](https://community.dynamics.com/blogs/post/?postid=f038c714-a492-f111-8076-000d3a54bc5d)

The company database identifier (INTERID) now appears alongside the company name in company selection and in the bottom status bar after login. This makes similarly named companies easier to distinguish and helps you confirm which company is active, without changing security or company setup.

IMAGE HERE
Company selection: confirm the company name and INTERID before signing in.

IMAGE HERE
After login: the bottom status bar identifies the active company and database

## [Manage existing purchase links for kit components](https://community.dynamics.com/blogs/post/?postid=f3c4b79f-e2c1-f111-aaad-3833c5e8605a)

You can now view and break an existing sales order/purchase order link for a kit component even when additional inventory has become available. Previously, sufficient current inventory could block access to that purchase commitment. This change applies to existing links, not to creating new links when stock is sufficient.

IMAGE HERE
Kit component purchase connection: review the accessible purchase order in PO Assignment for Document.

## [Notify approvers when another approver takes action](https://community.dynamics.com/blogs/post/?postid=4727dbd0-6ac2-f111-aaaf-000d3a54b64a)

Configured completed-action emails can notify assigned workflow users when another approver acts, especially when only one approval is required. Enable completed-action notifications in Workflow Maintenance and choose actions and messages in Workflow Assigned User Email Maintenance. These notifications are separate from originator emails and do not change all-approver requirements.

IMAGE HERE 
Workflow Maintenance: enable notifications for completed actions.

IMAGE HERE
Assigned-user email settings: choose the actions and messages that notify approvers.

## [Include or exclude voided transactions in inquiries](https://community.dynamics.com/blogs/post/?postid=4727dbd0-6ac2-f111-aaaf-000d3a54b64a)

The new Void Filter in customer and vendor transaction inquiries offers All Transactions, Not Voided, and Voided options. Use it with Work, Open, and History selections to focus on voided or nonvoided transactions, or compare the two views.

INSERT IMAGE
Customer inquiry: use the Void Filter to include all transactions, exclude voids, or show only voided transactions.


## Related information

[What's New Overview](introduction.md)
