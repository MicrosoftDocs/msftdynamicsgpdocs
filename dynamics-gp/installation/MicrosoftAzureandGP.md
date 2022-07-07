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
ms.date: 7/7/2022
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
 
 1. [Sign up for a Microsoft Azure account](https://azure.microsoft.com/free/)
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

1. [Sign up for a Microsoft Azure account](https://azure.microsoft.com/free/)

2.	Choose to create a new account using either the free trial or purchase option.  

    If you are deploying Microsoft Dynamics GP for development or testing purposes, you can sign up as an MSDN subscriber. 
    If you select the purchase option, you will have the option of buying the Azure services using Pay-as-You-Go, Microsoft Reseller or Enterprise agreement.  

3.	Log in using the Microsoft Account that will be the owner of the Microsoft Azure account. Sign up for a Microsoft Account if needed.  
4.	Assuming that the Microsoft Account is not already the owner of a Microsoft Azure account, a wizard window will open and walk you through the process of setting up a new account.   

### Creating a Subscription

You will create one or more subscriptions for the Microsoft Azure account. A subscription is a grouping of Microsoft Azure services and applications, including the virtual machines discussed earlier. The subscription provides a way to control the access to and the use of the Microsoft Azure subscribed service.  

On the account billing, the resource usage of Microsoft Azure services for each subscription is reported separately. In a situation where you will have multiple Microsoft Dynamics GP deployments, you may decide to use a separate subscription for each deployment in order to track expenses related to each deployment. All of the Microsoft Dynamics GP components for a single deployment need to be deployed to the same subscription, however.  

You can set up different administrators for each subscription as required. 

For more information, see [Overview of Subscription Management](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions) in the Azure content.

1.	Sign in to the [Azure account management portal](https://portal.azure.com/)  
2.	In the top search type in subscriptions.  

![Azure sub image 1](media/azuregp001.png)

3. Click to add a subscription.  

![Azure sub image 2](media/azuregp002.png)

>[!NOTE]
> You can rename the subscription after it has been created.  

### Sign up for a Microsoft Azure Support Plan

Microsoft Azure support plans provide technical and billing support for Microsoft Azure. The Microsoft Azure support plans offer flexible support options that will allow you to select the right level of support for your Microsoft Azure deployment. The support options range from support services included with your Microsoft Azure Account at no charge to Premier support services. Information on the available support plans and purchasing a plan can be found on the [Microsoft Azure Support](http://www.windowsazure.com/support/plans/). Technical and billing support for Microsoft Dynamics GP will continue to be offered using the existing programs. Refer to the Microsoft Dynamics GP support section of this document for additional information.     

## Planning

Planning your Microsoft Azure deployment of Microsoft Dynamics GP includes making decisions about which Microsoft Dynamics GP components to deploy, what configuration to use, and what the system requirements are for those components. These are decisions that must be made in all Microsoft Dynamics GP deployments. This part of the document covers the special considerations that impact these decisions when deploying on Microsoft Azure. This part contains the following sections.  

### Licensing

Licensing provides information on licensing Microsoft Dynamics GP and the required software on Microsoft Azure. 

Licensing the various components of the Microsoft Dynamics GP solution is an important consideration in all deployment types. For deployments on Microsoft Azure, you will want to evaluate the special licensing terms specific to Microsoft Azure and the impact that these decisions have on the overall cost of the solution.   
  
All Microsoft software installed in the Microsoft Azure Virtual Machine environment must be properly licensed. Microsoft Azure Virtual Machines include by default a license for use of Windows Server in the Microsoft Azure environment. Certain Microsoft Azure Virtual Machine offerings may also include additional Microsoft software on a per-hour or evaluation basis. 

[Additional common FAQs regarding licensing on Microsoft Azure Virtual Machines](https://azure.microsoft.com/pricing/licensing-faq/)

**Microsoft License Mobility through Software Assurance**
License Mobility through Software Assurance gives Microsoft Volume Licensing customers the flexibility to deploy eligible server applications with active Software Assurance on Microsoft Azure. With this Software Assurance benefit, there is no need to purchase new licenses and no associated mobility fees, so you can easily deploy existing licenses on the Microsoft Azure cloud platform.   
  
With License Mobility through Software Assurance, you can:   
•	Deploy certain server application licenses purchased under your Volume Licensing agreement in Microsoft Azure data centers.   
•	Extend the value of your server application licenses by deploying them on-premises or in the cloud.   
•	Take advantage of the low-cost computing infrastructure for changing business priorities.  More program benefit details and information can be found [HERE](http://www.windowsazure.com/pricing/license-mobility/).   
  
For information about Microsoft’s License Mobility program see:  
[License Mobility & Software Assurance | Microsoft Volume Licensing](https://www.microsoft.com/licensing/licensing-programs/software-assurance-license-mobility?rtc=1)
 


## See also

[Installation Checklist](installation-checklist.md)  
[Overview of Subscription Management](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions)  
[Sign up for Azure account](https://azure.microsoft.com/free/)  
