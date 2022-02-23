---
title: "Upgrading Dynamics GP web components on a single computer"
description: "Learn how to upgrade the Dynamics GP web components on a single computer."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 1d8b87e1-27ea-48b7-95f5-b302bdf600c7
ms.reviewer: 
---

# Single machine upgrade

This chapter contains the procedures you need to follow to perform an upgrade of the Dynamics GP web client on a single machine installation.

## Preparing for the upgrade

Before you perform the upgrade for the Dynamics GP web client, you must perform the upgrade for the database and the desktop client components. Use Dynamics GP Utilities to upgrade the system database and the company databases. Refer to the procedures described in the upgrade documentation for Dynamics GP to complete this process.

You should verify that the desktop client is working properly before you continue with the Dynamics GP web client upgrade. Resolve any issues before you continue.

Be sure that all of the users have signed out of the system before you start the web client upgrade process.

## Upgrading Web Components from a Dynamics GP 2013, or GP 2013 R2 deployment

To upgrade a web client deployment from a Dynamics GP 2013 deployment in the single machine configuration, complete the following procedure.

1. From the Dynamics GP installation media, double-click the Setup.exe file to open the Dynamics GP installation window.

2. Click Web Components and then click **Install**.

3. Select to upgrade your existing web client installation.

    ![shows the notification that an earlier version of the dynamics gp web components has been detected.](media/upgrade-web.png "Upgrade warning")  

4. The installation wizard will default with the selections from the installation being upgraded. You can change settings as needed. You can also select to add the service based architecture components to the installation. Upgrading the database will ask you for a new database name, defaulting to GPCONFIGURATION. The data will be migrated to the new database when running the configuration wizard.

5. When the installation is complete, run the Dynamics GP Web Components Configuration Wizard. You can access this from the Start menu.

6. At the Welcome screen, click **Next**.

7. Click **Exit**.

8. The Dynamics GP Web Client Help installer will be started. Click **Install** to complete the help installation process

9. Click **Finish** to close the installer.

## Upgrading Web Components from a Dynamics GP 2015 Web Components deployment

To upgrade Web Components from a Dynamics GP 2015 deployment in the single machine configuration, complete the following procedure.

1. Open an elevated command prompt as an administrator.

2. Change the directory to the AdProd\\WebComponents\\Updates folder on the Dynamics GP installation media.

3. Install the msp file in the updates folder using a command like the following:

msiexec /update filename.msp

Replace the filename.msp with the name of the file with an msp extension in the updates folder.

4. When the installation is complete, run the Dynamics GP Web Components Configuration Wizard. You can access this from the Start menu.

5. At the Welcome screen, click **Next**.

6. At the SQL Connection Information screen, Click **Next**.

7. At the Configuration Status and Action screen, Click **Next**.

8. Click **Exit** to close the Dynamics GP Web Components Configuration Wizard.

## Client machine update steps

To ensure that the updated Dynamics GP web client is working properly, you should perform the following steps on each of the client machines that access the web client.

1. Clear the Internet Explorer browser cache. This helps to ensure that the updated application and help files are being used for the web client.

    To clear the browser cache, open Internet Explorer. In the Tools menu, choose Internet options. In the Browsing history group, click **Delete**.

2. In the Delete Browsing History window, be sure to remove the temporary Internet files. Click **Delete**.

3. After the browser cache has been cleared, click **OK**.

4. In Internet Explorer, go to the Dynamics GP web client site. Sign in to the web client.

5. Look in the lower-right corner to verify the trust level for the web client. If you see the icon indicating that the web client is running in sandboxed mode, you have an additional step to perform.

The HTML application included with the updated web client may have been signed with a security certificate that is not available on the client machine. To get this certificate, you must run the DynamicsGPTrustedApp.msi that is included with the updated web client code.
