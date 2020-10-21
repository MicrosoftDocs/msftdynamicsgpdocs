---
title: "Workflow Administrator's Guide"
description: "Learn about setting up workflows in Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 08/10/2020
---

# Workflow Administrator's Guide

The following information provides a basic overview of the Workflow system and describes the benefits it provides.

- What is workflow?
-    Benefits of using the Workflow system
- How users will interact with the Workflow system

## What is workflow?
This documentation defines the term workflow in two ways:

1. Workflow is a system

  Workflow is the system that you installed with Microsoft Dynamics GP. The Workflow system provides functionality you can use to create individual workflows, or approval processes.

2. Workflow is an approval process

  A workflow is the approval process for a document, master record, or batch. A workflow defines how a document, master record, or batch "flows" through the system by showing who must approve it, and the conditions under which they must approve it.  

For example, consider the following illustration of a purchase order approval workflow. <!--missing image-->This workflow shows who must approve purchase orders, and the conditions under which their approval is required. For example, suppose Sam submits a purchase order for $2,000. In this scenario, the purchase order must be approved by Frank. If Sam submits a purchase order for $8,000, it must be approved by both Frank and Sue.

## Benefits of using the Workflow system

There are several benefits of using the Workflow system in your organization. 

Here are a few key benefits.

- Consistent processes

  The Workflow system enables you to define the approval process for specific documents, master records, and batches, such as purchase order documents and Receivables Management batches. By using the Workflow system, you ensure that documents, master records, and batches are reviewed and approved in a consistent and efficient manner.

- Automatic notification

  Users can be automatically notified when a document, master record, or batch is assigned to them for approval, or when a document, master record, or batch they submitted is approved. Users can be notified via desktop alerts or e-mail alerts. For more information about alerts, see Indicate if you want to send alert messages on page 66.

- Access through Outlook

  Users don't have to log on to Microsoft Dynamics GP to approve documents, master records, and batches. Users can approve documents, master records, and batches by accessing the Workflow by responding to e-mail messages in Outlook.

- Reports

  There are several Workflow reports you can generate. These reports help you monitor the Workflow system and identify specific workflow steps or approvers who may be slowing down an approval process. 

## How users will interact with the Workflow system

Users can interact with the Workflow system through Microsoft Dynamics GP and Outlook.

### Microsoft Dynamics GP

Workflow functionality is available in many areas of Microsoft Dynamics GP. For example, the Purchase Order Entry window enables a user to submit purchase orders for approval. This window has a message bar and history pane. The message bar displays the document's status and has buttons for approving and rejecting the document. The history pane displays previous actions made to the document.

### Outlook

When a document, master record, or batch is assigned to a user for approval, an e-mail message can be sent to the user. The e-mail message displays information about the document, master record, or batch and has an Edit this Task link. When the user clicks this link, a window appears where the user can approve or reject the document, master record, or batch.

## Workflow architecture

The Workflow system is made up of several software components. The following information describes these components and shows where they may be installed on your network.
*    Architecture overview
*    Deployment configurations

### Architecture overview

The Microsoft Dynamics GP Workflow system accesses two different types of data. It accesses accounting data from your Microsoft Dynamics GP databases, such as purchase orders, sales quotes, master records, and batch information. It also accesses workflow setup information from your SharePoint databases, such as the names of approvers and the conditions under which they must approve a document, master record, or batch.  

The following diagram illustrates the Workflow architecture and shows the software components that are used to access data.
As the diagram shows, the Microsoft Dynamics Workflow system consists of three main pieces: a web service, a web site, and server components. The Workflow web service enables employees using Microsoft Dynamics GP clients to interact with the Workflow server components. The Workflow web site enables employees using Outlook and Internet Explorer to interact with the Workflow server components.
The Workflow server components contain business logic and communicate with the SharePoint and Microsoft Dynamics GP databases. These components are installed on a server running SharePoint and can communicate directly with the SharePoint databases. The components must use Web Services for Microsoft Dynamics GP to communicate with the back office databases.

## Deployment configurations

There are several ways the Workflow system can be deployed. The following information describes the supported deployment configurations and shows where each software component is installed.

It's important that you know and understand how the Workflow system is deployed in your organization so that you can perform maintenance procedures and help troubleshoot any issues that may arise.

### Single-server configuration

In a single-server configuration, all the server-side components (such as Microsoft Dynamics GP, Web Services for Microsoft Dynamics GP, SharePoint, and Workflow) are installed on one server.
This configuration is recommended for testing and demonstration purposes only. This configuration does not provide the best security or performance.

