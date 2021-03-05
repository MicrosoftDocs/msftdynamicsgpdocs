---
title: Multi-Factor Authentication 
description: New in October 2020 - Multi-Factor Authentication
ms.date: 10/01/2020
ms.topic: article
ms.prod: dynamics-gp
author: theley502
ms.author: theley
manager: edupont
---

# Multi-Factor Authentication

Starting with the Dynamics GP October 2020 release, you will have the ability to use Multi-Factor Authentication for e-mail functionality. This new feature relies on an Azure Active Director App Registration. In this first section we will go over how to perform the Azure side the of the configuration.

## Register the app

1. First, you'll need to have an administrator who can log into the [Azure Portal](https://portal.azure.com/).

2. In the search box, type *App Registration* and select that option:

    <img src="media/image47.png" alt="Search for App Registration in Azure portal" width="677" height="282" />

3. Click on **New Registration** as shown in the below screenshot:

    <img src="media/image49.png" alt="App registration form in Azure portal" width="673" height="276" />

4. You will then choose settings for your new application.
    a. Enter a display name for the application (e.g. GPMFAApp)
    b. For **Supported account types** select the second option (**Account in any organizational directory (Any azure AD account – Multitenant)**) for most all configurations.             Choosing the wrong option can lead to an Unknown Error when using MFA in Dynamics GP.


    <img src="media/image51.png" alt="Account types in wizard for registering an app" width="437" height="320" />

5. Click on Register button.

6. Click on API Permission on the left side panel as shown in the screenshot.

    <img src="media/image53.png" alt="API Permission menu item highlighted" width="484" height="218" />

7. Click on Add permission button.

    <img src="media/image55.png" alt="Add permission button highlighted" width="557" height="250" />

8. Microsoft Graph – By default, Microsoft Graph application will have read permission for the user profile. To allow graph application to send an email, we need to add "Mail.Send" permission.

    <img src="media/image57.png" alt="Graph selected" width="481" height="237" />

9. Click on delegated permission.

10. Search for "Mail. Send" in the select permission search box.

11. Mark "Mail. Send" checkbox and click on add permission.

    <img src="media/image59.png" alt="Permissions for request API" width="423" height="238" />

12. Mail.Send permission will be added under Microsoft Graph.

    <img src="media/image61.png" alt="Configured permissions" width="403" height="196" />

13. Click on "Authentication" on the left panel under Manage option.

    <img src="media/image63.png" alt="Authentication menu item highlighted" width="403" height="252" />

14. Click on Add Platform.

    <img src="media/image65.png" alt="highlighted tile" width="255" height="275" />

15. Enter the value "urn:ietf:wg:oauth:2.0:oob" in the Custom Redirect URIs text box as shown in the screen shot. This uri will redirect to the original application.

    <img src="media/image67.png" alt="Custom redirect URI specified" width="343" height="342" />

16. Click on Configure button

17. Save the changes for the application.

    > [!NOTE]
    > As of now, Multi-Factor Authentication is not supported in Web Client. Once the Web Client changes are implemented, Default client type must be set to "Yes" as shown in the screen shot.

    <img src="media/image69.png" alt="Default Client Type" width="599" height="362" />

18. Click on Overview on the left side pane. The Application (client) ID can used in the Microsoft Dynamics GP.

    <img src="media/image71.png" alt="Highlighted application client ID" width="603" height="279" />

From the setup that was done in Azure, now launch Microsoft Dynamics GP 18.3 and go to Tools, Select Setup, choose Company and click Company E-mail Setup.

<img src="media/image73.png" alt="Company E-mail Setup in GP" width="406" height="409" />

> [!NOTE]
> There is a new column (MSGraphClientID) added to the company table SY04900, syEmailSetupOptions.
