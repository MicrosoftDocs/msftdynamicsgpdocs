---
title: "Configure a default domain"
description: "Learn how you can configure a default domain so users don't have to add it manually during log in."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: fa141208-7ffa-423b-a019-2573377a0e74
ms.reviewer: 
---
<span id="_Toc498953380" class="anchor"></span>

# Default domain

When a user signs in to the Dynamics GP web client, they must provide their full user name including the domain. Typically, the name will have this format:

*domain*\\username

In the **web.config** file for the web client web site, you can add an application setting to provide a default domain name. After this setting has been added, users do not need to supply the domain when supplying their credentials. They need to supply only the username portion of their credentials.

Use the following procedure add the default domain setting.

1. Make a copy of the **web.config** file for the Dynamics GP web client installation. This file is typically found in this location:

    C:\\Program Files\\Microsoft Dynamics\\GP Web Client\\GPweb\\

2. Edit the file using a text editor.

3. Near the end of the file, locate the &lt;**appSetting**s&gt; element.

4. Within the &lt;**appSettings**&gt; element, add an additional key element. The element specifies the default value to use for the domain. The following examples show the possible values for the key.

    **No value**   This key does not specify a value, so the user must supply a domain when entering their credentials. This is the default behavior when the key is not present.

    &lt;add key="DefaultUserDomain" value=""/&gt;

    Standard format This key specifies the value to use for the domain in standard format.

    &lt;add key="DefaultUserDomain" value="CONTOSO"/&gt;

    **UPN format**   This key specifies the value to use for the domain in UPN (User Principal Name) format.

    &lt;add key="DefaultUserDomain" value="@contoso.com"/&gt;

5. Save the changes that you made to the **web.config** file.

6. Copy the updated **web.config** file into the web client site, replacing the existing file.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")You might need to restart IIS for the change to take effect.  
