<span id="_Toc498953269" class="anchor"></span>

# Installation overview

This chapter briefly describes the Microsoft Dynamics GP web components and introduces the major parts of the installation. It also provides an installation checklist.

The following sections are included:

-   [What are the web components](#what-are-the-web-components)?  

-   [What is the web client?](#what-is-the-web-client)  

-   [Parts of the web components](#parts-of-the-web-components)  

-   [Installation checklist](#installation-checklist)  

## What are the web components?

The Microsoft Dynamics GP web components include the web client, service based architecture and web management console. These components can be installed together on the same server or installed separately on different servers as needed.

## What is the web client?

The Microsoft Dynamics GP web client provides access to Microsoft Dynamics GP through the Internet Explorer web browser. The user experience and functionality provided by the Microsoft Dynamics GP web client closely matches the experience of using the Microsoft Dynamics GP desktop client.

No client application software is installed on the user ’s local system. The Microsoft Dynamics GP application process for the user is running on a separate server. For the GP 2018 release, Silverlight is no longer needed as the Web Client is now an HTML web client.

The following illustration shows the Sales area page in the Microsoft Dynamics GP Web Client.

![Chapter 1 Installation overview image1](media/Chapter-1-Installation-overview-image1.png)  

## Parts of the web components

There are several parts of the web components installation that function together to present the web client to the user.

### Web site

An Internet Information Services (IIS) web site is the main entry point for the Microsoft Dynamics GP web client. This is the web site that users connect to when they access the web client. It displays the login page where users supply their credentials to access the system. The site must be configured to use Secure Sockets Layer (SSL) to help ensure data security.

### Session Hosts

The server machines that run the sessions of the Microsoft Dynamics GP web client are called session hosts. Each session host machine will have an installation of Microsoft Dynamics GP.

### Session Service

The Session Service is running on each session host machine. It manages the new process that is created each time a user logs into the Microsoft Dynamics GP web client.

### Session Central Service

The Session Central Service controls the communication between the web site and the session host machines. When multiple session host machines are available, the Session Central Service will balance the processing load among the available machines.

### Microsoft Dynamics GP Web Client runtime

The Microsoft Dynamics GP Web Client runtime is a component of the Microsoft Dynamics GP installation. A web client runtime process is created by the Session Service each time a user logs into the Microsoft Dynamics GP web client. Like the Dynamics.exe process used by the desktop client, the web client runtime process accesses the business logic in the application dictionaries and the data in the SQL database. Instead of displaying the user interface in a Windows application, the web client runtime displays the user interface in a browser.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")You might hear this component referred to as the runtime service.  

### Web Management Console

The Web Management Console is a separate HTML application that is used to perform administrative tasks for the Microsoft Dynamics GP web client. These tasks include actions like removing abandoned web client sessions.

### Description of service based architecture

The Microsoft Dynamics GP service based architecture enables REST based integrations to Microsoft Dynamics GP. The functionality existing in dictionaries is exposed as a service call. The functionality is the "base" used for the service as well as the web and desktop clients.

### Components of service based architecture

The components of service-based architecture function together to expose the service calls to integrating applications. The components include the following:

### GP Service

A WCF web service that serves as the main entry point for the service. The GP Service is responsible for performing the authentication on the incoming request and directing it to a Dexterity Service that can execute the request. The GP Service must be configured to use Secure Sockets Layer (SSL) to help ensure data security.

### Session hosts

The server machines that host the Dexterity Service instances are called session hosts. Each session host machine will have an installation of Microsoft Dynamics GP and the Dexterity Service Control.

### Dexterity Service Control

The Dexterity Service Control is running on each session host machine. It manages the Dexterity Service instances that execute the requests.

### Dexterity Service

The Dexterity Service is a component of the Microsoft Dynamics GP installation. The Dexterity Service gets requests from the GP Service and executes them using a Microsoft Dynamics GP runtime instance. A runtime instance is created by the Dexterity Service as needed to handle incoming requests. There could be one or more runtime instances for a single Dexterity Service on a session host. Like the Dynamics.exe process used by the desktop client, a Dexterity Service runtime instance accesses the business logic in the application dictionaries and the data in the SQL database.

## Installation checklist

To install the Microsoft Dynamics GP web components, complete the following tasks in the order shown.

| Task                                                                                                                                                                  | For more information see                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Select a deployment configuration. Select whether you want to install the Microsoft Dynamics GP web components on a single machine or as a scale-out installation. | [Chapter 2, “Deployment configurations](https://microsoft-my.sharepoint.com/personal/bigoswam_microsoft_com/Documents/Documents/Office/Dynamics%20GP/Web%20Components%20Guide/WebClient_source/Chapter%202%20Deployment%20configurations.dotx)”             |  
| 2. Check the Microsoft Dynamics GP                                                                                                                                    
                                                                                                                                                                        
 installation.                                                                                                                                                          
                                                                                                                                                                        
 Verify that the Microsoft Dynamics GP installation is running properly and that the required web client runtime components are installed.                              | Chapter 4, “Microsoft Dynamics GP                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                               
  configuration”                                                                                                                                                                                                                                               |
| 3. Create the security groups and user accounts.                                                                                                                      
                                                                                                                                                                        
 Determine which users will access the Microsoft Dynamics GP web client and the Web Management Console.                                                                 | Chapter 5, “Security groups and user                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                               
  accounts”                                                                                                                                                                                                                                                    |
| 4. Verify the prerequisite software. Install the software needed to support the Microsoft Dynamics GP web components.                                                 | [Chapter 7, “Prerequisite software”](https://microsoft-my.sharepoint.com/personal/bigoswam_microsoft_com/Documents/Documents/Office/Dynamics%20GP/Web%20Components%20Guide/WebClient_source/Chapter%207%20Prerequisite%20software.dotx)                     |  
| 5. Create and configure web sites.                                                                                                                                    
                                                                                                                                                                        
 Create and configure the web sites that will host the Microsoft Dynamics GP web client and the Web Management Console.                                                 | [Chapter 8, “Web sites”](https://microsoft-my.sharepoint.com/personal/bigoswam_microsoft_com/Documents/Documents/Office/Dynamics%20GP/Web%20Components%20Guide/WebClient_source/Chapter%208%20Web%20sites.dotx)                                             |  
| 6. Obtain security certificates and configure SSL.                                                                                                                    
                                                                                                                                                                        
 Determine the type of security certificate you want to use. Configure the web site to use SSL.                                                                         | [Chapter 9, “Security certificates and SSL”](https://microsoft-my.sharepoint.com/personal/bigoswam_microsoft_com/Documents/Documents/Office/Dynamics%20GP/Web%20Components%20Guide/WebClient_source/Chapter%209%20Security%20certificates%20and%20SSL.dotx) |  
| 7. Install the web components.                                                                                                                                        
                                                                                                                                                                        
 Complete the installation procedure based on the type of deployment that you chose.                                                                                    | [Part 4, Web components installation](https://microsoft-my.sharepoint.com/personal/bigoswam_microsoft_com/Documents/Documents/Office/Dynamics%20GP/Web%20Components%20Guide/WebClient_source/Part%204%20Web%20components%20install.dotx)                    |  


