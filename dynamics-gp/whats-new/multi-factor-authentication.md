---
title: Multi-Factor Authentication 
description: New in October 2020 - Multi-Factor Authentication
ms.date: 05/01/2023
ms.topic: article
author: theley502
ms.author: theley
manager: jswymer
---

# Multi-Factor Authentication

[!INCLUDE [azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Starting with the Dynamics GP October 2020 release, you will have the ability to use Multi-Factor Authentication for e-mail functionality. This new feature relies on a Microsoft Entra ID App Registration. In this first section we will go over how to perform the Azure side the of the configuration.

## Register the app

1. First, you'll need to have an administrator who can log into the [Azure Portal](https://portal.azure.com/).

2. In the search box, type *App Registration* and select that option:

    <img src="media/image47.png" alt="Search for App Registration in Azure portal" width="677" height="282" />

3. Click on **New Registration** as shown in the below screenshot:

    <img src="media/image49.png" alt="App registration form in Azure portal" width="673" height="276" />

4. You will then choose settings for your new application.
   
    1. Enter a display name for the application (e.g. GPMFAApp)
    2. For **Supported account types** prior to the Fall 2023 (18.6) release, you were limited to the second option (**Account in any organizational directory (Any Microsoft Entra ID account – Multitenant)**).  If you are on 18.6 or later, you can also use the (**Account in this organizational directory only (%domain% only - Single tenant)**) option. Choosing the wrong option can lead to an Unknown Error when using MFA in Dynamics GP.


    <img src="media/image51.png" alt="Account types in wizard for registering an app" width="437" height="320" />

6. Click on Register button.

7. Click on API Permission on the left side panel as shown in the screenshot.

    <img src="media/image53.png" alt="API Permission menu item highlighted" width="484" height="218" />

8. Click on Add permission button.

    <img src="media/image55.png" alt="Add permission button highlighted" width="557" height="250" />

9. Microsoft Graph – By default, Microsoft Graph application will have read permission for the user profile. To allow a Graph application to send an email, we need to add some specific permissions.

    <img src="media/image57.png" alt="Graph selected" width="481" height="237" />

10. Click on "Delegated permissions".

11. Search for "Mail.Send" in the Select permission search box.

12. Mark the "Mail.Send" and "Mail.Send.Shared" checkboxes and click on Add permissions.

    <img src="media/image94.png" alt="Permissions for request API" width="557" height="566" />

13. Mail.Send and Mail.Send.Shared permissions will be added under Microsoft Graph.

    <img src="media/image93.png" alt="Configured permissions" width="403" height="196" />

14. Click on "Authentication" on the left panel under Manage option.

    <img src="media/image63.png" alt="Authentication menu item highlighted" width="403" height="252" />

15. Click on "+Add Platform" and select "Mobile and desktop applications".

    <img src="media/image65.png" alt="highlighted tile" width="255" height="275" />

16. Enter the value "urn:ietf:wg:oauth:2.0:oob" in the Custom Redirect URIs text box as shown in the screen shot. This uri will redirect to the original application.

    <img src="media/image67.png" alt="Custom redirect URI specified" width="343" height="342" />

17. Click on Configure button

18. Save the changes for the application.

    > [!NOTE]
    > Multi-Factor (Modern Auth) Authentication is supported in Web Client with 18.5 release or later. 
    > [Refer to Web Client setup with Modern Auth](https://community.dynamics.com/gp/b/dynamicsgp/posts/modern-authentication-in-web-client)

    <img src="media/image69.png" alt="Default Client Type" width="599" height="362" />

19. Click on Overview on the left side pane. The Application (client) ID will be used in the Microsoft Dynamics GP client.

    <img src="media/image71.png" alt="Highlighted application client ID" width="603" height="279" />

From the setup that was done in Azure, now launch Microsoft Dynamics GP 18.3 or later and go to Tools, Select Setup, choose Company and click Company E-mail Setup.  Enter the Application (Client) ID into this Desktop Properties section of this window.  

<img src="media/image95.png" alt="Company E-mail Setup in GP" width="406" height="409" />

If you're using a Single tenant app registration you will also need to pull the Directory (Tenant) ID from the aboeve Overview window and enter that into the Tenant ID field.

> [!NOTE]
> There is a new column (MSGraphClientID) added to the company table SY04900, syEmailSetupOptions.
