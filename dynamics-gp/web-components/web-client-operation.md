---
title: "Web client runtime"
description: "Learn how all of the components of the Dynamics GP web client installation work together as a user logs in, performs standard operations, and logs out of the web client."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.prod: dynamics-gp
ms.topic: article
ms.assetid: 5228d0cd-89a9-4611-b3a9-b2d9fe3ac22e
ms.reviewer: 
---
<span id="_Toc498953278" class="anchor"></span>

# Web Client Operation

It is important to understand how all of the components of the Dynamics GP web client installation work together as a user logs in, performs standard operations, and logs out of the web client. This information can be helpful when you are troubleshooting any issues with the web client. The following topics are discussed:

-   [Logon](#logon)  

-   [Standard operations](#standard-operations)  

-   [Logoff](#logoff)  

## Logon

The logon process has multiple steps, although most of them are not visible to the web client user. For simplicity, the log on process for a typical scale out configuration is described. The parts of the configuration are shown in the following illustration.

![shows a sample network topology for a client machine communicating with dynamics gp web components.](media/web-client-runtime-01.png "Deployment")  

*1. User accesses the web client site.*

In the first step of the logon process, the client machine with a web browser accesses the URL for the Dynamics GP web client site. The logon page for the site is displayed.

![shows a sample network topology for a client machine communicating with dynamics gp web components with step 1 for displaying the login screen.](media/web-client-runtime-02.png "Deployment")  

*2. The user supplies their windows account credentials. *

Typically, these will be their domain credentials, but could also be their Organizational Account credentials. If the web site can verify that the user is allowed to access the Dynamics GP web client, the logon process is allowed to proceed.

![shows a sample network topology for a client machine communicating with dynamics gp web components with step 2 for the user logging in.](media/web-client-runtime-03.png "Deployment")  

*3. The Session Central Service directs the session request.*

Session information for the current user is retrieved.

![shows a sample network topology for a client machine communicating with dynamics gp web components with step 3 for web server sending session information to the user.](media/web-client-runtime-04.png "Deployment")  

The session Central Service performs several action to determine how it will direct the user ’s request.

-   It will determine whether the user has existing sessions already running on the session host machines. If one or more sessions exist, they are presented in a list for the user. The user can re-connect to an existing session or create a new session.

-   If no previous sessions exist, the Session Central Service will determine on which session host machine the new session will be created.

*4. The HTML application is loaded into the browser on the client computer.*

![shows a sample network topology for a client machine communicating with dynamics gp web components with step 3 for session server sending a session through web server and then to the client machine.](media/web-client-runtime-05.png "Deployment")  

*5. The Session Service creates a new runtime session.*

On the session host machine that was chosen by the Session Central Service, the Session Service will create a new instance of the runtime service. This is the process that accesses the business logic in the application dictionaries and the data in the SQL database. It also communicates with the application to display the client user interface.

![shows a sample network topology for a client machine communicating with dynamics gp web components with step 5 for session service creating a new runtime session.](media/web-client-runtime-06.png "Deployment")  

*6. The Dynamics GP application is displayed.*

After the connection is established between the HTML application on the client and the runtime session on the session server machine, the Dynamics GP application will start. If the user credentials can be matched to a Dynamics GP user account, the user will be signed in. Otherwise, the login window will be displayed.

![shows a sample network topology for a client machine communicating with dynamics gp web components with step 6 for displaying the dynamics gp application with data from sql server.](media/web-client-runtime-07.png "Deployment")  

## Standard operations

When a user logs on to the Dynamics GP web client, a connection is created between the HTML application that is loaded in the web browser and the runtime session that is created on the session host server. After this connection is established, the web server that hosts the site for the Dynamics GP web client does not play any part in the interaction.

![shows a sample network topology for a client machine communicating with dynamics gp web components with data passing through the tiers during standard operations.](media/web-client-runtime-08.png "Deployment")  

The connection between the HTML application and the runtime session transmits all of the information needed to present the application user interface, as well as any input supplied by the user. The runtime session on the session server machine interacts with the SQL Server database, just as the Dynamics GP desktop client would.

If the user is disconnected, such as by closing their web browser without logging out of Dynamics GP, the runtime session on the session server machine will remain running. The next time the user logs in, that existing runtime session will be found by the Session Central Service. The user will have the option to reconnect to that existing session and continue where they left off.

## Logoff

When the user clicks the Exit GP link in the upper-right corner of the Dynamics GP web client window, the standard Dynamics GP logoff procedure is performed. The connections between the runtime session and the SQL Server are closed, and the runtime session is ended. The user is returned to the main logon screen for the Dynamics GP web client site
