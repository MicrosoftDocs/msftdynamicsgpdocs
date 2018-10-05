---
title: "Web sites"
description: "Get an overview of the websites that your must set up  for the Dynamics GP web components."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 40172c16-c363-49ac-ae76-38c7194e1f76
ms.reviewer: 
---
<span id="_Toc498953299" class="anchor"></span>

# Web sites

This portion of the documentation discusses the web sites that are needed for the [!INCLUDE[prodshort](../includes/prodshort.md)] web components installation. Information is divided into the following sections:

-   [Required web sites](#required-web-sites)  

-   [Extending sites with ASP.NET](#extending-sites-with-asp.net)  

## Required web sites

Two web sites – one for the web client and another for web management console – are used for the [!INCLUDE[prodshort](../includes/prodshort.md)] web components installation. These two web sites can be hosted in a single IIS web site, or on separate IIS web sites.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")The IIS web sites must be configured for SSL (secure sockets layer). This means each must have a security certificate. If you use two separate IIS web sites, then you will need two security certificates. If both web sites are hosted on the same web site, then only one security certificate is required.  

### Dynamics GP Web Client site

This web site hosts the [!INCLUDE[prodshort](../includes/prodshort.md)] web client. It is the web site that the users connect to with their web browser when they log into the [!INCLUDE[prodshort](../includes/prodshort.md)] web client. You can use the default web site in IIS (port 80) or you can create a new web site that runs on a different port.

### Web Management Console site

This site hosts the Web Management Console that is used to manage the [!INCLUDE[prodshort](../includes/prodshort.md)] web client installation. In basic web client installations, you can use the same web site that the [!INCLUDE[prodshort](../includes/prodshort.md)] web client is installed on.

## Extending sites with ASP.NET

On Windows Server 2008 R2, the web sites that you use for the [!INCLUDE[prodshort](../includes/prodshort.md)] web client must be extended with ASP.NET functionality. This step is not necessary on Windows Server 2012, because the sites will already have been extended with .NET Framework 4.

To extend the web site, complete the following procedure:

1. Open a command prompt with administrative privileges.

2. Set the current directory to this location:

    C:\\Windows\\Microsoft.NET\\Framework64\\v4.0.30319\\

3. Run this command:

    aspnet\_regiis -i
