---
title: "Word Templates in Microsoft Dynamics GP"
description: "Word Templates in Microsoft Dynamics GP."
keywords: "Word Template"
author: theley502

ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 03/08/2022

---

# Introduction to Word Templates in Dynamics GP

Would you like to update the look and feel of your customer facing documents from the drab report writer formats?

Would you also like to email those documents directly out of Dynamics GP?

The Word Template functionality in Microsoft Dynamics GP is pretty awesome and it will do all of this as well as allow you to have separate document types for different companies and customers.

There are a few tricks to setting up and getting things functioning. It’s important to perform these steps in order.

You also will be working with the Template Configuration and Template Maintenance in Dynamics GP.

## Install and Configure Word Templates

You must have two applications installed before beginning this process:  

* Microsoft Dynamics GP Add-On for Word
* Open XML SDK 2.0 for Microsoft Office

Open XML will be installed when you install Dynamics GP. The Dynamics GP Add-On for Word is located on the Dynamics DVD.

To use Microsoft Word with Dynamics GP, you must add the “Developer” tab to your ribbon bar. In Microsoft Word navigate to Options \| Customize Ribbon and select “Popular Commands.” Add the Developer function to the Ribbon list and then check the box. Click “OK.”

## Create and Assign Word Templates

First, you need to determine what report we’re basing our template on and whether it’s an original report or a modified report.

Why?

Word Templates are based on the standard report writer report. In order to create and assign a template the system needs to know the name of the report and also whether the report is already modified.

Tip: We recommend always basing the template on a modified version of the report for greater flexibility in the future.

Why?

Remember that the template uses Report Writer to access data. If we ever want to add a new calculated field, we need to create it first in Report Writer for it to be available in our template, thus it’s a modified report.

Reports \| Template Configuration

In Dynamics GP, the configuration window allows you to enable a specific form(s) to work as a template. Mark the document(s) for which you want to create a template. At the bottom of the window, be sure to mark the ‘Enable Report Templates’ and, if desired, to ‘Allow use of the Standard form’ even though you’re using the template.
