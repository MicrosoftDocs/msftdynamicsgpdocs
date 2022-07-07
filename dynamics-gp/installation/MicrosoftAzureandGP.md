---
title: Microsoft Dynamics GP on Microsoft Azure 
description: A guide to planning, deploying and managing Microsoft Dynamics GP on Microsoft Azure.  
keywords: "Azure"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 7/6/2022
---

# Microsoft Dynamics GP on Microsoft Azure 

This guide provides information for deploying Microsoft Dynamics GP on Microsoft Azure. Microsoft Azure provides the infrastructure you need to run 
Microsoft Dynamics GP on a dependable, secure, and scalable cloud platform.   
  
Flexibility and familiarity make the infrastructure services in Microsoft Azure an ideal platform for Microsoft Dynamics GP. 

The Microsoft Dynamics GP you deploy in Microsoft Azure is the same one that you would deploy in your own office or data center. Since Microsoft Azure 
infrastructure services (MAIS) is a virtual machine environment, the process of deploying and managing Microsoft Dynamics GP on MAIS should be very 
familiar to you already. Your knowledge and previous experience deploying Microsoft Dynamics GP on premise or as a hosted service will be beneficial 
when deploying on MAIS. You have flexibility with respect to the license model you choose to use when deploying Microsoft Dynamics GP on Microsoft Azure. 
And because the product is constant, you can be reassured that you can move your deployment into or out of Microsoft Azure seamlessly.  
  
The following Microsoft Azure infrastructure services features are used as building blocks when you create a Microsoft Dynamics GP environment.   
  
1.	Virtual Machines – The virtual machines are the Windows Servers that host the Microsoft Dynamics GP components and other pre-requisite software.  
2.	Virtual Network – A virtual network provides a network in the cloud for cross-machine communication.  
3.	Storage Account – A storage account stores the data disks and the virtual machine VHD files.  
    
How you configure the infrastructure services features will be depend on the needs of your Microsoft Dynamics GP deployment. 
For example, how many virtual machines are required, the network configuration for cross-machine communication, and disk configuration for storing data 
must be configured in Microsoft Azure to support the Microsoft Dynamics GP installation. After the Microsoft Azure environment is set up and configured, 
the Microsoft Dynamics GP components and required prerequisite software can be installed on the virtual machines in much the same way as they would be on 
virtual machines in an on premise or hosted environment.  

This document provides guidelines for deploying Microsoft Dynamics GP on Microsoft Azure.  The information contained in this guide is intended to be used 
along with the main product documentation for Microsoft Dynamics GP. 

## Checklist

The following checklist provides an overview of the steps for deploying Microsoft Dynamics GP on Microsoft Azure.  
 
 1. [Sign up for a Microsoft Azure account](https://azure.microsoft.com/free/search/?OCID=AID2200277_SEM_ae067f8b5cdd14162ab71d3f9d0ecdcf:G:s&ef_id=ae067f8b5cdd14162ab71d3f9d0ecdcf:G:s&msclkid=ae067f8b5cdd14162ab71d3f9d0ecdcf)
 2. Create subscription 
 3. Determine deployment configuration
 4. Create Virtual Network
 5. Create Virtual Machines
 6. Deploy Microsoft Dynamics GP
 7. Create back up and scheduled maintenance procedures
 8. Maintain virtual machines
 9. Update Microsoft Dynamics GP
 
 ## Microsoft Azure Account
 
 This part contains information about signing up for a Microsoft Azure Account and creating a subscription.
 
 ### Sign up for a Microsoft Azure Account
 
 You will need to sign up for a Microsoft Azure Account before creating any of the service components. Use these steps to create a Microsoft Azure Account.  

1. [Sign up for a Microsoft Azure account](https://azure.microsoft.com/free/search/?OCID=AID2200277_SEM_ae067f8b5cdd14162ab71d3f9d0ecdcf:G:s&ef_id=ae067f8b5cdd14162ab71d3f9d0ecdcf:G:s&msclkid=ae067f8b5cdd14162ab71d3f9d0ecdcf)

2.	Choose to create a new account using either the free trial or purchase option.  

  If you are deploying Microsoft Dynamics GP for development or testing purposes, you can sign up as an MSDN subscriber. 
  If you select the purchase option, you will have the option of buying the Azure services using Pay-as-You-Go, Microsoft Reseller or Enterprise agreement.  

3.	Log in using the Microsoft Account that will be the owner of the Microsoft Azure account. Sign up for a Microsoft Account if needed.  
4.	Assuming that the Microsoft Account is not already the owner of a Microsoft Azure account, a wizard window will open and walk you through the 
process of setting up a new account.   

### Creating a Subscription

You will create one or more subscriptions for the Microsoft Azure account. A subscription is a grouping of Microsoft Azure services and applications, including 
the virtual machines discussed earlier. The subscription provides a way to control the access to and the use of the Microsoft Azure subscribed service. 
On the account billing, the resource usage of Microsoft Azure services for each subscription is reported separately. In a situation where you will 
have multiple Microsoft Dynamics GP deployments, you may decide to use a separate subscription for each deployment in order to track expenses 
related to each deployment. All of the Microsoft Dynamics GP components for a single deployment need to be deployed to the same subscription, however.  
You can set up different administrators for each subscription as required. 

For more information, see [Overview of Subscription Management](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions) in the Azure content.  

## See also

[Installation Checklist](installation-checklist.md)  
[Overview of Subscription Management](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions)  
[Sign up for Azure account](https://azure.microsoft.com/free/)  
