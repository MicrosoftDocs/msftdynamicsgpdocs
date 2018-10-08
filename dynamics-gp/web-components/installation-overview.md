---
title: "Installation overview for web components"
description: "Get an introduction to the [!INCLUDE[prodshort](../includes/prodshort.md)] web components and introduces the major parts of the installation."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 2351bb7b-8f14-4b7d-b4ed-8b97f7974617
ms.reviewer: 
---
<span id="_Toc498953269" class="anchor"></span>

# Installation overview

This chapter briefly describes the [!INCLUDE[prodshort](../includes/prodshort.md)] web components and introduces the major parts of the installation. It also provides an installation checklist.

## What are the web components?

The [!INCLUDE[prodshort](../includes/prodshort.md)] web components include the web client, service based architecture and web management console. These components can be installed together on the same server or installed separately on different servers as needed.

## What is the web client?

The [!INCLUDE[prodshort](../includes/prodshort.md)] web client provides access to [!INCLUDE[prodshort](../includes/prodshort.md)] through the Internet Explorer web browser. The user experience and functionality provided by the [!INCLUDE[prodshort](../includes/prodshort.md)] web client closely matches the experience of using the [!INCLUDE[prodshort](../includes/prodshort.md)] desktop client.

No client application software is installed on the user ’s local system. The [!INCLUDE[prodshort](../includes/prodshort.md)] application process for the user is running on a separate server. For the GP 2018 release, Silverlight is no longer needed as the Web Client is now an HTML web client.

The following illustration shows the Sales area page in the [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client.

![shows the sales area homescreen in dynamics gp in a browser.](media/web-client-homescreen-sales.png "Sales homescreen")  

## Parts of the web components

There are several parts of the web components installation that function together to present the web client to the user.

### Web site

An Internet Information Services (IIS) web site is the main entry point for the [!INCLUDE[prodshort](../includes/prodshort.md)] web client. This is the web site that users connect to when they access the web client. It displays the login page where users supply their credentials to access the system. The site must be configured to use Secure Sockets Layer (SSL) to help ensure data security.

### Session Hosts

The server machines that run the sessions of the [!INCLUDE[prodshort](../includes/prodshort.md)] web client are called session hosts. Each session host machine will have an installation of [!INCLUDE[prodshort](../includes/prodshort.md)].

### Session Service

The Session Service is running on each session host machine. It manages the new process that is created each time a user logs into the [!INCLUDE[prodshort](../includes/prodshort.md)] web client.

### Session Central Service

The Session Central Service controls the communication between the web site and the session host machines. When multiple session host machines are available, the Session Central Service will balance the processing load among the available machines.

### [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client runtime

The [!INCLUDE[prodshort](../includes/prodshort.md)] Web Client runtime is a component of the [!INCLUDE[prodshort](../includes/prodshort.md)] installation. A web client runtime process is created by the Session Service each time a user logs into the [!INCLUDE[prodshort](../includes/prodshort.md)] web client. Like the Dynamics.exe process used by the desktop client, the web client runtime process accesses the business logic in the application dictionaries and the data in the SQL database. Instead of displaying the user interface in a Windows application, the web client runtime displays the user interface in a browser.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")You might hear this component referred to as the runtime service.  

### Web Management Console

The Web Management Console is a separate HTML application that is used to perform administrative tasks for the [!INCLUDE[prodshort](../includes/prodshort.md)] web client. These tasks include actions like removing abandoned web client sessions.

### Description of service based architecture

The [!INCLUDE[prodshort](../includes/prodshort.md)] service based architecture enables REST based integrations to [!INCLUDE[prodshort](../includes/prodshort.md)]. The functionality existing in dictionaries is exposed as a service call. The functionality is the "base" used for the service as well as the web and desktop clients.

### Components of service based architecture

The components of service-based architecture function together to expose the service calls to integrating applications. The components include the following:

### GP Service

A WCF web service that serves as the main entry point for the service. The GP Service is responsible for performing the authentication on the incoming request and directing it to a Dexterity Service that can execute the request. The GP Service must be configured to use Secure Sockets Layer (SSL) to help ensure data security.

### Session hosts

The server machines that host the Dexterity Service instances are called session hosts. Each session host machine will have an installation of [!INCLUDE[prodshort](../includes/prodshort.md)] and the Dexterity Service Control.

### Dexterity Service Control

The Dexterity Service Control is running on each session host machine. It manages the Dexterity Service instances that execute the requests.

### Dexterity Service

The Dexterity Service is a component of the [!INCLUDE[prodshort](../includes/prodshort.md)] installation. The Dexterity Service gets requests from the GP Service and executes them using a [!INCLUDE[prodshort](../includes/prodshort.md)] runtime instance. A runtime instance is created by the Dexterity Service as needed to handle incoming requests. There could be one or more runtime instances for a single Dexterity Service on a session host. Like the Dynamics.exe process used by the desktop client, a Dexterity Service runtime instance accesses the business logic in the application dictionaries and the data in the SQL database.

## Installation checklist

To install the [!INCLUDE[prodshort](../includes/prodshort.md)] web components, complete the following tasks in the order shown.

| Task    | For more information see   |
|--------|---------------------------|
| 1. Select a deployment configuration. Select whether you want to install the [!INCLUDE[prodshort](../includes/prodshort.md)] web components on a single machine or as a scale-out installation. | [Deployment configurations](deployment-configurations.md)|  
| 2. Check the [!INCLUDE[prodshort](../includes/prodshort.md)] installation.
 Verify that the [!INCLUDE[prodshort](../includes/prodshort.md)] installation is running properly and that the required web client runtime components are installed.  | [Environment configuration](environment-configuration.md) |
| 3. Create the security groups and user accounts.
 Determine which users will access the [!INCLUDE[prodshort](../includes/prodshort.md)] web client and the Web Management Console.  | [Security groups and user accounts](security-groups-and-user-accounts.md)  |
| 4. Verify the prerequisite software. Install the software needed to support the [!INCLUDE[prodshort](../includes/prodshort.md)] web components.  | [Prerequisite software](prerequisite-software.md) |  
| 5. Create and configure web sites.
 Create and configure the web sites that will host the [!INCLUDE[prodshort](../includes/prodshort.md)] web client and the Web Management Console. | [Web sites](web-sites.md) |  
| 6. Obtain security certificates and configure SSL.
 Determine the type of security certificate you want to use. Configure the web site to use SSL. | [Security certificates and SSL](security-certificates-and-SSL.md) |  
| 7. Install the web components.
 Complete the installation procedure based on the type of deployment that you chose. | [Web components installation](web-components-installation.md)|  
