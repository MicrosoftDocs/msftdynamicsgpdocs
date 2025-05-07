---
title: "Web sites"
description: "Get an overview of the websites that your must set up  for the Dynamics GP web components."
keywords: "web components"
author: jswymer
ms.author: jswymer
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.topic: how-to
ms.assetid: 40172c16-c363-49ac-ae76-38c7194e1f76
ms.reviewer: 
---

# Web sites

This portion of the documentation discusses the web sites that are needed for the Dynamics GP web components installation.  

## Required web sites

Two web sites – one for the web client and another for web management console – are used for the Dynamics GP web components installation. These two web sites can be hosted in a single IIS web site, or on separate IIS web sites.

> [!NOTE]
> The IIS web sites must be configured for SSL (secure sockets layer). This means each must have a security certificate. If you use two separate IIS web sites, then you will need two security certificates. If both web sites are hosted on the same web site, then only one security certificate is required.  

### Dynamics GP Web Client site

This web site hosts the Dynamics GP web client. It is the web site that the users connect to with their web browser when they log into the Dynamics GP web client. You can use the default web site in IIS (port 80) or you can create a new web site that runs on a different port.

### Web Management Console site

This site hosts the Web Management Console that is used to manage the Dynamics GP web client installation. In basic web client installations, you can use the same web site that the Dynamics GP web client is installed on.

## Extending sites with ASP.NET

On Windows Server 2008 R2, the web sites that you use for the Dynamics GP web client must be extended with ASP.NET functionality. This step is not necessary on Windows Server 2012, because the sites will already have been extended with .NET Framework 4.

To extend the web site, complete the following procedure:

1. Open a command prompt with administrative privileges.

2. Set the current directory to this location:

    C:\\Windows\\Microsoft.NET\\Framework64\\v4.0.30319\\

3. Run this command:

    aspnet\_regiis -i
