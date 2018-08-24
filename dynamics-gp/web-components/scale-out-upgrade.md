<span id="_Toc498953327" class="anchor"></span>

# Scale out upgrade

This chapter contains the procedures you need to follow to perform an upgrade of the Microsoft Dynamics GP web client in the scale out configuration. The following sections are included:

-   [Preparing for the upgrade](#preparing-for-the-upgrade)  

-   [Updating the web site and Session Central Service](#updating-the-web-site-and-session-central-service)  

-   [Updating session host machines](#updating-session-host-machines)  

-   [Verifying the services](#verifying-the-services)  

-   [Client machine update steps](#client-machine-update-steps)  

## Preparing for the upgrade

The first step to performing the upgrade for a scale out installation is to upgrade for the database and the desktop client components for Microsoft Dynamics GP. Use Dynamics GP Utilities to upgrade the system database and the company databases. Refer to the procedures described in the upgrade documentation for Microsoft Dynamics GP to complete this process.

You should verify that at least one desktop client installation is working properly before you continue with the Microsoft Dynamics GP web client upgrade. Resolve any issues before you continue.

Be sure that all of the users have signed out of the system before you start the web client upgrade process.

If you are using Tenant Services with your Microsoft Dynamics GP web client installation, you must apply the update to Tenant Services before you update the web client components. Refer to the Tenant Services Installation and Administration Guide for information about updating Tenant Services. The Microsoft Dynamics GP upgrade can take place after the upgrade of the web client since older versions of the Microsoft Dynamics GP runtime can be used with the latest version of the web components.

## Updating the web site and Session Central Service

To install the upgrade for the web site and the Session Central Service, complete the following procedure.

1. Log in to the machine that is running the web site and the Session Central Service for the Microsoft Dynamics GP web client installation.

2. From the Microsoft Dynamics GP installation media, double-click the Setup.exe file to open the Microsoft Dynamics GP installation window.

3. Click Web Components and then click Install.

4. Select to upgrade your existing web client installation.

![Chapter 13 Scale out upgrade image1](media/Chapter-13-Scale-out-upgrade-image1.PNG)  

5. The installation wizard will default with the selections from the installation being upgraded. You can change settings as needed. You can also select to add the service based architecture components to the installation. Upgrading the database will ask you for a new database name, defaulting to GPCONFIGURATION. The data will be migrated to the new database when running the configuration wizard.

![Chapter 13 Scale out upgrade image2](media/Chapter-13-Scale-out-upgrade-image2.PNG)  

6. When the installation is complete, run the Dynamics GP Web Components Configuration Wizard. You can access this from the Start menu.

7. At the Welcome screen, click **Next**.

8. Specify the type of authentication you want to use to connect to the SQL Server where the database for the Web Components is located. Click Next to continue.

9. Review the configuration actions that will be performed. Click **Next** to continue.

10. Click **Exit**.

11. The Microsoft Dynamics GP Web Client Help installer will be started. Click **Install** to complete the help installation process.

12. Click **Finish** to close the installer.

## Updating session host machines

To install the upgrade for each session host machine in the scale out installation, complete the following procedure.

1. Log in to the session host machine.

2. If you haven’t already done so, perform the update for the Microsoft Dynamics GP desktop client components. Be sure that the desktop client on the session host machine is working properly before you continue this upgrade procedure.

3. From the Microsoft Dynamics GP installation media, double-click the Setup.exe file to open the Microsoft Dynamics GP installation window.

4. Click Web Components and then click **Install**.

5. Select to upgrade your existing web client installation.

6. The installation wizard will default with the selections from the installation being upgraded. You can change settings as needed. You can also select to add the service based architecture components to the installation. When asked for the web components database, provide the new database name selected when upgrading the web server.

7. When the installation is complete, run the Dynamics GP Web Components Configuration Wizard. You can access this from the Start menu.

8. When the installation is complete, run the Dynamics GP Web Components Configuration Wizard. You can access this from the Start menu.

9. At the Welcome screen, click **Next**.

10. Specify the type of authentication you want to use to connect to the SQL Server where the database for the Web Components is located. Click **Next** to continue.

11. Review the configuration actions that will be performed. Click **Next** to continue.

12. Click **Exit**.

13. Start the installer for the updated help content. The installer has the following name:

Microsoft\_DynamicsGP18\_GPWebClientHelp.msi.

14. At the Welcome screen, click **Install**. The installation process may take a few minutes.

15. Click **Finish**.

## Verifying the services

When all of the components of the web client installation have been updated, • On the machine that is hosting the web site for the web client installation, verify that the Session Central Service is running.

-   On each session host machine, verify that the Session Service is running.

-   In the Session Management snap-in for the Web Management Console, all of the session host machines should be listed. Be sure that each machine is set to allow new web client sessions.

At this point, you can allow users to sign in to the Microsoft Dynamics GP web client installation.

## Client machine update steps

To ensure that the updated Microsoft Dynamics GP web client is working properly, you should perform the following steps on each of the client machines that access the web client.

1. Clear the Internet Explorer browser cache. This helps to ensure that the updated application and help files are being used for the web client.

To clear the browser cache, open Internet Explorer. In the Tools menu, choose Internet options. In the Browsing history group, click Delete.

2. In the Delete Browsing History window, be sure to remove the temporary

Internet files. Click Delete.

3. After the browser cache has been cleared, click OK.

4. In Internet Explorer, go to the Microsoft Dynamics GP web client site. Sign in to the web client.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")If you watch closely, you should see a new Silverlight application is downloaded for the Microsoft Dynamics GP web client.  

5. Look in the lower-right corner to verify the trust level for the web client. If you see the icon indicating that the web client is running in sandboxed mode, you have an additional step to perform.

The Silverlight application included with the updated web client may have been signed with a security certificate that is not available on the client machine. To get this certificate, you must run the DynamicsGPTrustedApp.msi that is included with the updated web client code.
