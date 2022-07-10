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
ms.date: 7/9/2022
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
 

**Microsoft Dynamics GP**
Use the Microsoft Dynamics GP Pricing and Licensing to learn more about the Perpetual Licensing and Service Provider License agreement (SPLA) licensing programs – both of which are supported for on-Azure deployments.  
  
Consult the [Licensing Guide](https://download.microsoft.com/download/E/6/8/E685081D-647F-432A-AFF3-20AA95353798/GP - English.pdf) to improve your understanding of how to license Microsoft Dynamics GP .  


**Remote Desktop Services (RDS)**
There are two ways to license Remote Desktop Services (RDS), formerly known as Terminal Services in Microsoft Azure Virtual Machines.   

1.	Remote Desktop Services (RDS) Subscriber Access Licenses (SALs) purchased through the Microsoft Service Provider Licensing Agreement (SPLA) may be used to deliver graphical user interface functionality for applications on Microsoft Azure virtual machines.  

2.	Volume Licensing customers who have active Software Assurance on their RDS User CALs are entitled to RDS CAL Extended Rights, which allow use of their RDS User CAL with Software Assurance against a Windows Server running on Microsoft Azure or other service providers’ shared server environments.   
  
To read more about [licensing RDS with Microsoft Azure Virtual Machines](http://www.windowsazure.com/en-us/pricing/licensing-faq/) & 
[Product Use Rights(PUR) document](http://www.microsoft.com/licensing/about-licensing/product-licensing.aspx)    

**Microsoft SQL Server**   
There are three ways to license Microsoft SQL Server in Microsoft Azure Virtual Machines:   
1.	Install or upload your own SQL Server image using the license mobility benefits under Software Assurance.   
2.	Obtain the SQL Server image from the image gallery and pay the per-minute rate of SQL Server in Microsoft Azure Virtual Machines.   
3.	If you are a Service Provider with a signed Services Provider License Agreement (SPLA), install or upload your SQL Server Standard image with Subscriber Access License (SAL) reported via your SPLA.   
  
You will want to carefully evaluate each of these options for Microsoft SQL Server as the cost models can be very different. The deployment model you choose to employ and the number of users that will be supported are key factors in this decision.   

**Other Licensing Considerations – Microsoft Azure Billing / Cost Allocation**
For many Service Providers offering a hosted solution, determining how to bill Customers for monthly, consumption-based charges from Microsoft Azure will represent a new challenge.   
  
To learn what billing information is available, you should review the [Understand Your Bill for Microsoft Azure](http://www.windowsazure.com/en-us/support/understand-your-bill/) on the Microsoft Azure Portal. These pages provide an overview of the Microsoft Azure billing process, links to sample invoices and a description of the daily usage data file that can be exported and analyzed.   
  
Microsoft Azure billing is done monthly at the Account level. Charges for various services are grouped and reported at the Subscription level. To simplify the cost allocation exercised, Partners supporting multiple Customer deployments may wish to segregate each Customer’s services to individual subscriptions.  
    
Note:  
Please note that this whitepaper does not supersede or replace any of the legal documentation covering use rights for Microsoft products and does not constitute a commitment of licensing program availability.  For current product use rights and licensing program availability for products licensed through [Volume Licensing including SPLA](http://www.microsoft.com/licensing/)

### Legal

Legal provides information on protecting customers data deployed on Microsoft Azure. 

Together with Microsoft, Partners must work together to protect Customer data and provide guidance to Customers when it comes to security, privacy, and compliance practices.  
  
Microsoft runs Microsoft Azure services with common operational practices and features across multiple geographies and jurisdictions. However, it is ultimately up to Partners and Customers to determine if Microsoft services satisfy their regulatory needs.     
  
To help provide Partners and Customers with up to date information the [Microsoft Azure Trust Center](http://www.windowsazure.com/en-us/support/trust-center/) provides detailed information on security, privacy, and compliance topics for Microsoft Azure customers.  

**Security**
This topic provides an overview of the provisions Microsoft is taking to provide a secure environment within geographically dispersed datacenters. Among the extensive list of Security-related resources, the [Standard Response to Request for Information:Security and Privacy](http://go.microsoft.com/fwlink/?linkid=293448&clcid=0x409) outlines how Microsoft Azure meets the suggested principals and mapped them to the [International Standards Organization](https://azure.microsoft.com/en-us/blog/microsoft-azure-leads-the-industry-in-iso-certifications/#:~:text=We%20are%20happy%20to%20announce%20that%20Microsoft%20Azure,to%20meet%20a%20wide%20range%20of%20regulatory%20obligations). This standardized response empowers Partners and Customers with in-depth information to evaluate different offerings in the market place today.  

**Privacy**
Includes links to multiple resources that describe Privacy practices of the Microsoft Azure environment. It includes a link to the [Microsoft Azure Privacy Statement](http://go.microsoft.com/fwlink/p/?linkid=131004&clcid=0x409) an overview of privacy terms and a discussion of the location of Customer data, E.U. Data Protection Directive 

**Compliance**
This topic provides resources to help Partners and Customers comply with the specific laws and regulations applicable to their unique industry and use scenario.  


### Microsoft Dynamics GP Components

Microsoft Dynamics GP Components provides information about the Microsoft Dynamics GP components that can be deployed on Microsoft Azure.

This section provides information about the Microsoft Dynamics GP components that can be deployed on Microsoft Azure. How you license Windows Server will determine how you deploy some of the Microsoft Dynamics GP components on Microsoft Azure. The Microsoft Dynamics GP components that require Remote Desktop Services (RDS) for end-user access over the Internet can be deployed on Microsoft Azure only if you are able to license RDS using the methods provided in the Remote Desktop Services licensing section. You can also use Remote Desktop for Administration to run these components for administrative purposes. User access to applications using remote desktop, will be limited to a maximum of 2 concurrent administrator users using Remote Desktop for Administration. Refer to the following list for component availability.  


| Component                            |   Availability   |
|-----------------------------------   | --------------   |
| Microsoft Dynamics GP Databases      |     Yes          |
| Microsoft Dynamics GP Client         |     Yes          |
| Microsoft Dynamics GP Web Client     |     Yes          |
| Service Based Architecture           |     Yes          |
| Companion Application Service        |     Yes          |
| eConnect                             |     Yes          |
| SQL Server Reporting Services Reports|     Yes          |
| Excel Reports                        |     Limited      |
| Integration Manager                  |     Yes          |
| Analysis Cubes                       |     Limited      |
| Management Reporter                  |     Yes          |
| FRx                                  |     No           |
| ISV Solutions                        |     Limited      |

The Microsoft Dynamics GP desktop client can be used for end-user access through Remote Desktop Services. 
The Microsoft Dynamics GP desktop client can be used for administrative purposes with Remote Desktop for Administration.  

If the application that is using eConnect requires Remote Desktop Services for end-user access, then you will need to properly license RDS. 
If access is for administrators only, then Remote Desktop for Administration can be used.   

Excel reports connect directly to the Microsoft Dynamics GP databases. 
-Because the SQL Server is not exposed to the Internet, the Excel reports must be run from a computer connected to the Microsoft Azure Virtual Network. 
-This means that Microsoft Excel to be run on a Remote Desktop Services server or from a computer on the network connected to the Microsoft Azure Virtual Network.  

Integration Manager can be used for end-user access through Remote Desktop Services. 
-Integration Manager can be used for administrative purposes with Remote Desktop for Administration.  

Analysis Cubes reports connect directly to the Microsoft Dynamics GP databases. Because the SQL Server is not exposed to the Internet, the Analysis Cubes reports must be run from a computer connected to the Microsoft Azure Virtual Network.   

The Management Reporter report designer and desktop viewer can be used for end-user access through Remote Desktop Services. The Management Reporter report designer and desktop viewer can be used for administrative purposes with Remote Desktop for Administration. The Web Viewer can be used by all end-users to view reports. 18 ISV products must be evaluated on a product-by-product basis.  


### Deployment Model

Deployment Models describes the two common configurations that are used when deploying Microsoft Dynamics GP on Microsoft Azure.

The deployment models for Microsoft Dynamics GP on Microsoft Azure are the same models available for on premise and hosted environments. The models range from a single-machine deployment joined to your corporate network, to a scale out multitenant public cloud deployment using a private virtual network in Microsoft Azure. The difference in these models on Microsoft Azure when comparing with an on premise installation is the setup of the environment, (machines, network configuration, etc.). 
The machine configurations, like single-machine and scale-out, available for deploying Microsoft Dynamics GP on premise are also available for deploying in Microsoft Azure. The network configuration model for all of the Microsoft Dynamics GP components, with the exception of some ISV products that integrate using Web Services for Microsoft Dynamics GP, are installed to one or more virtual machines in Microsoft Azure. For performance reasons you will want to avoid installing some of the Microsoft Dynamics GP components to your on premise network and some to virtual machines in Microsoft Azure.    

**Dedicated Private Virtual Network**

This is the only model tested with Dynamics GP.  A Microsoft Azure Virtual Network is created that is fully contained within Microsoft Azure. It is not connected to an on premise network. All of the Microsoft Dynamics GP and required infrastructure components are installed on virtual machines on the virtual network. Unless a single machine configuration is being used, you will need to add an Active Directory domain controller with DNS to the virtual network. The virtual network will be configured to use the domain’s DNS system for name resolution of machines on the virtual network. The quantity and configuration of the virtual machines is based on your deployment needs, much like deploying to computers on your corporate network. The following diagram shows a simple Microsoft Dynamics GP Web Client deployment on a dedicated private Microsoft Azure Virtual Network.  


![Azure sub image 1](media/azuregp003.png)


In this diagram the Microsoft Azure Virtual Network contains an Active Directory domain controller with DNS. The virtual network is configured to use the DNS services on the domain controller for name resolution of the Microsoft Azure Virtual Machines. The Web Server and SQL Server virtual machines are joined to the domain in Microsoft Azure for directory services, including the 
authentication of Microsoft Dynamics GP users. If additional server roles are required for the Microsoft Dynamics GP deployment, additional virtual machines would be added to the virtual network in Microsoft Azure and joined to the domain in Microsoft Azure.  


### System Requirements

System Requirements provides sizing recommendations for the virtual machine instance sizes that are available in Microsoft Azure.  

The system requirements for deploying Microsoft Azure are the same as deploying Microsoft Dynamics GP on premise or in other data centers. The virtual machines in Microsoft Azure have standard processor and memory configurations that are based on the instance size. The instance sizes range from VMs with 1 core and .75 GB RAM to 16 cores with 112 GB RAM. You can scale the instance size up or down as usage patterns change. You can also add additional instances to scale out as demand increases. Refer to the [Pricing Details](http://azure.microsoft.com/en-us/pricing/details/virtual-machines/) for the latest instance sizes and pricing.   
  
Use the [Dynamics GP System Requirements](https://docs.microsoft.com/en-us/dynamics/s-e/gp/MDGP2018_System_Requirements) when determining the compute instance size required for each of the virtual machine instances in your configuration.  


### High Availability and Disaster Recovery (HADR)

High Availability and Disaster Recovery (HADR) provides information on setting up the Azure environment for high availability and disaster recovery.

While the Microsoft Azure Infrastructure Services are designed to provide a high availability and fault tolerant platform for applications, there are considerations you as the administrator need to plan for in order to best utilize these capabilities.  The Microsoft Azure high availability mechanisms protect the high availability of the Virtual Machines (VMs), not specifically the applications which run on these VMs. It is up to you as the administrator to use these mechanisms when implementing the application in order to meet the HADR capabilities you require. The following sections contain information on the high availability mechanisms available in Microsoft Azure to use with your Microsoft Dynamics GP deployment.  

**Availability Set**
An availability set in Microsoft Azure is a configuration option available when load balancing multiple VMs that places the VMs in different fault and update domains. The result is that the application is still available even if there is a failure or planned update to a VM instance that takes it off-line for a period of time. The fault domain protects against unplanned failures by creating the VMs in a different “rack” of servers, resulting in them being on different physical hardware and serviced by different networking components. The update domain protects against downtime from planned updates to the host operating system by placing the VMs on host machines configured with different maintenance schedules.   
  
An availability set requires that the application is installed on multiple VMs that have been configured as a load balanced cloud service. Not all of the Dynamics GP components can be deployed in this configuration however, the following Dynamics GP application components support being deployed on a load balanced cloud service.     
  
1.	SQL Server (when utilizing SQL Server HADR)  
2.	Web Client/Service Based Architecture web server 
(Only possible if using a scale out deployment with separate Session Host servers or if each of the servers runtime service is configured for a unique port.)   
3.	Web Services for Microsoft Dynamics GP  
4.	SQL Server Reporting Services   
5.	Tenant Services   
6.	RDS Servers (GP client, Management Reporter, Integration Manager, eConnect, ISV solutions)  

Refer to the [Manage the High Availability of Virtual Machines](https://docs.microsoft.com/en-us/azure/virtual-machines/availability) for additional information.  

**SQL Server HADR**
There are several different HADR technologies in the SQL Server product that are supported in Microsoft Azure. These include the following.  
•	AlwaysOn Availability Groups  
•	Database Mirroring  
•	Log Shipping  
•	Backup and Restore with Microsoft Azure Blob Storage Service  
These technologies can be used independently or together to provide the high availability and disaster recovery required. When used with Microsoft Dynamics GP, the AlwaysOn and Database Mirroring technologies provide failover capabilities for the Dynamics GP databases. The Log Shipping and Backup and Restore with Microsoft Azure Blob Storage Service provides recovery capabilities for the Dynamics GP databases. Refer to the article [Business continuity and HADR for SQL server on Azure Virtual Machines](https://docs.microsoft.com/en-us/azure/azure-sql/virtual-machines/windows/business-continuity-high-availability-disaster-recovery-hadr-overview?view=azuresql) for additional information.   

**Redundant Storage**
The redundant storage mechanism of Microsoft Azure provides for multiple copies of the VM’s VHD files and the data disks that store data such as the Dynamics GP databases. The first redundant storage mechanism is locally redundant storage (LRS), which maintains three copies of the account data within the primary data center. The second mechanism is geo redundant storage (GRS, also known as geo-replication), which replicates the account data to a secondary data center. These redundant copies are done automatically by the platform. You do need to be aware that for the Microsoft Azure data disks used to store the Dynamics GP databases, if GRS is enabled the data and log files for a database need to be placed on the same disk.   

**Host O/S Maintenance**
Refer to the following article about VM Maintenance 
[Maintenance for virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/maintenance-and-updates)


## Deploy Microsoft Dynamics GP 

The deployment of Microsoft Dynamics GP on Microsoft Azure is very similar to an on-premise deployment. The setup of the network and virtual machines in Microsoft Azure is where the deployment of Microsoft Dynamics GP on Microsoft Azure is the most different from on premise deployments. You will use the Microsoft Azure Management Portal or PowerShell for most of the setup actions. These include setting up a virtual network, creating virtual machines, and configuring the virtual machines through Remote Desktop for Administration. After setting up the environment, you will install the Microsoft Dynamics GP components on the virtual machines that are acting as the SQL Server, Web Server, Session Host machines, and so on. This part contains the following sections.  

### Creating a Virtual Network
Creating a Virtual Network provides directions for setting up a virtual network in Microsoft Azure.  

A Microsoft Azure Virtual Network must be created in your subscription so that you can create and run the Microsoft Azure Virtual Machine instances. The Microsoft Azure Virtual Network may be connected to a physical network for site-to-site connectivity, it could also be set up as a dedicated private network in the cloud. The virtual machines serve as the Windows Server hosts for the Microsoft Dynamics GP components deployed on the virtual network you create.   
   
Before setting up your virtual network, you will need to determine the design that will best meet your deployment scenario. Things to consider include whether you will be joining this network to another network, the address ranges for the network and how domain name resolution (DNS) will be handled. In the current Microsoft Azure release, it may be difficult to make changes to the virtual network after virtual machines have been deployed. Refer to the [Azure Virtual Network concepts and best practices](https://docs.microsoft.com/en-us/azure/virtual-network/concepts-and-best-practices)
  
When deploying Microsoft Dynamics GP on Microsoft Azure, you have two options. You can create a private virtual network that is fully contained within Microsoft Azure, or you can create a virtual network in Microsoft Azure that is connected to your existing physical network. In either case, all of the Microsoft Dynamics GP components will be deployed to virtual machine instances on the Microsoft Azure Virtual Network. You may want to connect to an existing network to leverage on-premise resources. When creating a private virtual network with multiple virtual machines, you will need to create a domain controller for authentication and name resolution (DNS). The virtual network will need to be configured to use the domain controller’s IP address for DNS. This means that you must modify the DNS setting for the virtual network after creating the domain controller virtual machine on the virtual network.   
 

You create a virtual network by using the Microsoft Azure Management Portal or using the Azure CLI. 
Refer to the article [Quickstart: Create a virtual network using the Azure portal](https://docs.microsoft.com/en-us/azure/virtual-network/quick-create-portal) for information about creating a virtual network using the Microsoft Azure Management Portal. Refer to the article 
[Quickstart: Create a virtual network using the Azure CLI](https://docs.microsoft.com/en-us/azure/virtual-network/quick-create-cli) for information about using the Azure CLI. 

### Creating Virtual Machiens
Creating Virtual Machines provides directions for creating a virtual machine instance in Microsoft Azure.    



### Configuring Active Directory

### Configuring Microsoft SQL SErver

### Configuring Microsoft SQL SErver REporting Services 

### 


## See also

[Installation Checklist](installation-checklist.md)  
[Overview of Subscription Management](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions)  
[Sign up for Azure account](https://azure.microsoft.com/free/)  
