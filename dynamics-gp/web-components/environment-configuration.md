---
title: "Configuring Dynamics GP"
description: "Learn how to prepare your Dynamics GP deployment so that you can install the web components."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: f7200048-1617-470d-a01c-8fad05a3a85b
ms.reviewer: 
---

# Dynamics GP environment configuration

Before you can install the [!INCLUDE[prodshort](../includes/prodshort.md)] web components, you must have [!INCLUDE[prodshort](../includes/prodshort.md)] installed, including the necessary web client runtime and/ or service based architecture components. T

## [!INCLUDE[prodshort](../includes/prodshort.md)] installation

[!INCLUDE[prodshort](../includes/prodshort.md)] should be installed, configured, and operating properly before you use the web components installation to install the Web Client or Service Based Architecture server components for [!INCLUDE[prodshort](../includes/prodshort.md)]. While most administrative tasks can be performed with the web client, some important tasks such as creating companies cannot. These actions must be done with the [!INCLUDE[prodshort](../includes/prodshort.md)] desktop client and GP Utilities.

Each server that will be acting as a session host must have a [!INCLUDE[prodshort](../includes/prodshort.md)] desktop client installation installed. Use the desktop client to verify that the server is able to connect to the [!INCLUDE[prodshort](../includes/prodshort.md)] database.

## Web Client SQL Server login

During the [!INCLUDE[prodshort](../includes/prodshort.md)] installation, a SQL Server login is created that web client and service based architecture sessions can use to access SQL Server. By using the single Web Client SQL Server login, each web client and service based architecture user doesn't need to have their own SQL Server login. Web client users can access the web client simply by providing their standard Windows login credentials or their Organizational Account. Service Based Architecture users must access [!INCLUDE[prodshort](../includes/prodshort.md)] using either their Windows login credentials or their Organizational Account.

During the [!INCLUDE[prodshort](../includes/prodshort.md)] web components installation, you will need to know the name and password for the Web Client SQL Server login. You can use [!INCLUDE[prodshort](../includes/prodshort.md)] Utilities to configure or make changes to the Web Client SQL Server login for your [!INCLUDE[prodshort](../includes/prodshort.md)] installation.

## Web client only users

It’s likely that you will have some users that will be accessing only the [!INCLUDE[prodshort](../includes/prodshort.md)] web client and will never use the desktop client. You can set up these users in [!INCLUDE[prodshort](../includes/prodshort.md)] as web client only users.

In the User Setup window, mark the Web Client user only (no SQL Server Account) option. The SQL Server Account tab will be disabled, because the user you are adding to [!INCLUDE[prodshort](../includes/prodshort.md)] will not have a SQL Server login. In the

Directory Account tab, you will supply the Windows login information for the user.

When the user signs in to the web client, they simply provide their Windows Login or organizational account credentials. The web client will determine the user ’s [!INCLUDE[prodshort](../includes/prodshort.md)] user ID based on the credentials. The Web Client SQL

Server login (discussed in the previous section) is used to access the SQL Server databases.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")Be aware that users who do not sign in to the web client using their own SQL Server login cannot send remote processes to the Distributed Process Server.  

## Web client runtime components

Each session host server must have the [!INCLUDE[prodshort](../includes/prodshort.md)] web client runtime and service based architecture components. These components are part of the [!INCLUDE[prodshort](../includes/prodshort.md)] installation. To install these components, complete the following procedure:

To install the web client runtime components

1. Open the Programs and Features control panel.

2. Select the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 application, and then click Change.

3. In the Program Maintenance window, click Add/Remove Features.

4. Be sure that the Web Client Runtime feature is marked to be installed.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")  

5. Click Next to continue, and then click Install to complete the installation process.

6. Click Exit.

To install the service based architecture components

1. Open the Programs and Features control panel.

2. Select the [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 application and then click Change.

3. In the Program Maintenance window, click Add/Remove Features.

4. Be sure that the Service Based Architecture feature is marked to be installed.

5. Click Next to continue, and then click Install to complete the installation process.

6. Click Exit.
