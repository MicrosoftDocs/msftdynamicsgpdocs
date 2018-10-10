---
title: "Manage the Dynamics GP web components"
description: "Learn how you can manage web component sessions as an administrator of Dynamics GP."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 75a73ebc-01c1-489a-8a15-8bf40badd6a0
ms.reviewer: 
---
<span id="_Toc498953334" class="anchor"></span>

# Managing web client sessions

The administrator of the Dynamics GP web client installation has the responsibility to monitor and manage the web client sessions. Information about his task is divided into the following topics:

-   [Session Management snap-in](#session-management-snap-in)  

-   [Connecting to Session Central](#connecting-to-session-central)  

-   [Session host machines](#session-host-machines)  

-   [Suspending a session host machine](#suspending-a-session-host-machine)  

-   [Sessions](#sessions)  

-   [Ending a session](#ending-a-session)  

-   [Session timeout](#session-timeout)  

## Session Management snap-in

The Session Management snap-in for the Web Management Console is the primary tool that you will use to manage web client sessions. Use the following procedure to access this snap-in.

1. Open Internet Explorer.

2. Enter the address of the Web Management Console site. The default address of the site is:

    https://ServerName:PortNumber/WebManagementConsole

    **ServerName**   is the fully-qualified domain name (FQDN) for the server that is hosting the web management console site. This name must match the name you used when you requested the security certificate that you applied to the site when setting up SSL.

        **PortNumber**   is the port for the web site that you are using. If you chose to install on the default web site (port 80) then you do not need to supply the port number.

    A typical URL to access the Web Management Console looks similar to the following:

    https://gpuaweb.contoso.com/WebManagementConsole

3. You may be prompted for your login credentials when you access the Web Management Console. If you are, provide your login name and password.

4. In the Web Management Console, click the Session Management snap-in.

![shows the session management snap-in in the web management console.](media/manage-web-session-management-console.png "Session Management")  

## Connecting to Session Central

To use the Session Management snap-in to monitor Dynamics GP web client session, the snap-in must be configured to access the Session Central Service. The Session Central Service is the component of the Dynamics GP web client installation that creates and tracks web client sessions.

To connect to the Session Central Service, the Session Management snap-in must have the URL for the service. In most cases, this will be automatically configured when the Dynamics GP web client components were installed. Use the following procedure to manually configure the connection to the Session Central Service.

To connecting to Session Central

1. With the Session Management snap-in selected, click Configure in the ribbon of the Web Management Console.

2. In the window that is displayed, supply the URL for the Session Central Service. A typical URL to access the service looks like the following:

    http://machinename:48650/SessionCentralService

    Substitute machinename with the name of the computer on which the Session Central Service is running. The default port used for the service is 48650. If you have used a different port for the service, you must use that port number in the URL.

    If the Session Central Service has been configured to use SSL (secure sockets layer) than the URL must begin with https, instead of http.

3. Click **OK**. The value entered will be validated. If the Session Central Service cannot be contacted, an error will be displayed. Correct the URL and then click OK to save the changes.

## Session host machines

The left pane of the Session Management snap-in lists the session host machines that are configured to host Dynamics GP web client sessions. Select the machine name to see the detailed information about that machine. The following details are provided:

**Last Status Update**   Indicates the last time that the status information was updated. Click Refresh in the ribbon to retrieve the latest information from the Session Central Service.

**Memory Utilization**   Indicates the percentage of memory that is used on the selected machine.

**Total Sessions Running**   Indicates the total number of web client sessions that are running on the selected machine.

**Potential Sessions Remaining**   Provides an estimate of the number of additional web client sessions that could be hosted on the selected machine. This estimate is based primarily on the amount of available memory on the machine.

**Full Computer Name**   Displays the full name of the machine.

**Session List**   Lists the individual web client sessions that are running on the machine.

## Suspending a session host machine

An active session host machine allows new web client sessions to be created for it. You may want to remove a session host machine from service, such as when you want to apply system updates. To do this, you can suspend the session host machine, which prevents it from accepting any new web client sessions. To do this, complete the following procedure.

1. In the left pane of the Session Management snap-in, select the session host machine that you want to suspend.

2. In the ribbon, click **Suspend**.

Suspending a machine does not affect the web client sessions that are already running on the machine. The existing web client sessions will continue to run until they are closed.

## Sessions

When a session host machine is selected in the left pane of the Session Management console, the sessions running on that machine are displayed. The following details are provided for each session:

**Created Date**   Indicates the date and time that the web client session was created.

**Dynamics GP Company Name**   Displays the company in the Dynamics GP installation that the user logged in to.

**Dynamics GP User**   Displays the Dynamics GP user name that the web client user supplied when they signed into the company.

**Dynamics GP Version**   Provides the version number of Dynamics GP that is being used for the web client session.

**User ID**   Displays the user ID supplied when the user signed in to the Dynamics GP web client.

**Host Machine Name** Displays the name of the machine that is hosting the web client session.

**Session ID**   Shows the internal session ID.

**Tenant Name**   Displays the name of the tenant that is being used for the web client session. If the Tenant Service is not being used, the tenant name is GPWebApp.

**Last Heartbeat**   Indicates that last time the web client communicated with the session host machine.

## Ending a session

A web client session ends when the user signs out. However, situations occur in which a session may be left running on the session host machine. For example, the web client user may have closed their web browser without signing out first. You may have a need to manually end a session that a web client user has left running on a session host machine.

When you manually end a session, there is a risk of data corruption, because the Dynamics GP session was not closed down normally.

To manually end a web client session:

1. Select the session that you want to end.

2. In the ribbon, click **End Session**.

3. In the End Session window, verify that you really want to end the session. If you are sure you want to end the session, click **End Session**.

## Session timeout

You can configure whether inactive web client sessions are automatically closed after a specified amount of time has passed.

### Single tenant

If you are using the Dynamics GP web client in a single tenant configuration (not using the Tenant Service), a settings in the TenantConfiguration.xml file of the web client installation controls the session timeout. This file is typically found in this location on the machine that is hosting the web site for the web client installation:

C:\\Program Files\\Microsoft Dynamics\\GP Web Client\\GPweb\\

The &lt;HeartbeatTimeout&gt; element in the TenantConfiguration.xml file controls the amount of time that must pass before an inactive web client session is automatically closed. The format for the value is:

Days.Hours:Minutes:Seconds

The value 0.00:00:00 indicates that the timeout is infinite, and no inactive web client sessions will be automatically closed.

## Multiple tenants

If you are using the Microsoft Dynamic GP web client in a multitenant configuration, you will use the Tenant Management snap-in for the Web Management Console to control the session timeout value. Refer to the Tenant Services Installation and Administration Guide or the Tenant Management snap-in help for information about how to configure the session timeout value in a multitenant configuration.
