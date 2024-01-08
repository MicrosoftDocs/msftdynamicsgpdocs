---
title: "Developer Tools"
description: "Information around eConnect, Integration Manager and Web Services in Microsoft Dynamics GP."
keywords: "import"
author: theley502
manager: jswymer
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 1/8/2024
---

# Developer Tools

This documentation supports developers who work with Microsoft Dynamics GP.

## eConnect 

This documentation contains detailed information about the operations, classes, XML schemas and nodes available in Microsoft [Dynamics GP eConnect](/previous-versions/dynamicsgp/developer/bb219081(v=msdn.10)). 

The Microsoft eConnect procedures are encrypted to preserve the Microsoft intellectual property.

Business Logic Modification: eConnect provides both Pre and Post procedures for modifying business logic before passing a transaction through eConnect to Microsoft Dynamics GP. If these procedures were not encrypted, unauthorized modifications could be made, potentially leading to incorrect business logic application and data corruption.

Therefore, keeping Dynamics eConnect procedures encrypted is essential for data security, compliance with standards, and maintaining the integrity of business logic. It’s advised against modifying any Dynamics GP stored procedures as it may cause problems with your Microsoft Dynamics GP data.

However, over the years, we have found some issues with a few of the eConnect procedures based on business practices for a specific company. Microsoft is not actively fixing these issues in the eConnect shipping product, due to the life cycle of the product. The below published procedures are modified eConnect procedures with fixes around areas a large majority of customers have run into.

These modified procedures are use at your own risk and should be tested by your company before using in your production system.  When you upgrade Microsoft Dynamics GP, these modified procedures may be lost.

- [taPOPCreateDistributions](https://mbs2.microsoft.com/fileexchange/?fileID=e004756e-9413-4fed-9b4a-82306d2763b2) - December 2023
- [taCalcDueDatePM](https://mbs2.microsoft.com/fileexchange/?fileID=400b0ad2-3452-470f-bc99-e690c12dab60) - December 2023
- [taCalcDueDateRM](https://mbs2.microsoft.com/fileexchange/?fileID=6f1f21fb-8eec-4527-b163-578e4e55b06f) - December 2023
- taSOPLot - May 2021

## Web Services

This documentation describes [Web Services for Microsoft Dynamics GP](/previous-versions/dynamicsgp/developer/cc534132(v=msdn.10)). 
The programmer's guide contains information about how to use the services. 
The web service reference contains detailed information about the operations, classes, enumerations, and policies available in the Dynamics GP service. 

## Visual Studio Tools

This documentation contains detailed information about using [Visual Studio Tools for Microsoft Dynamics GP](/previous-versions/dynamicsgp/developer/cc543538(v=msdn.10)) to develop integrating applications. 
