---
title: "Troubleshooting"
description: "Learn how you can troubleshoot Dynamics GP web components."
keywords: "web components"
author: edupont04
ms.author: edupont
manager: annbe
applies_to: 
ms.date: 09/05/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: 02e97d6e-54a4-4284-a258-74a9e7b161f8
ms.reviewer: 
---
<span id="_Toc498953354" class="anchor"></span>

# Troubleshooting

Use the information in this chapter to help you troubleshoot issues you may have when you are installing or using the Microsoft Dynamics GP web client. The following topics are discussed:

-   [Errors reported on the main page](#errors-reported-on-the-main-page)  

-   [Incomplete sign-on](#incomplete-sign-on)  

-   [Web client is Initializing and becomes unresponsive](#web-client-is-initializing-and-becomes-unresponsive)  

-   [Port issues](#port-issues)  

-   [Performance issues](#performance-issues)  

-   [Printing issues](#printing-issues)  

-   [Help not available](#help-not-available)  

## Errors reported on the main page

When a sign-on error occurs and is reported on the main page for the web client, look on the Dynamics section of the Event Log on the machine running the web site and Session Central Service for the web client installation. The information provided in the error(s) listed there can help you troubleshoot the issue.

If the error detail indicates that a file cannot be found, be sure that you have installed the web client runtime components on the session host machines. The file that cannot be found may be one of these components.

You should also verify that the Session Central Service and the Session Service are both started.

## Incomplete sign-on

Many actions occur during the sign-on process. Issues in any of those actions can prevent the sign-on from completing.

If you do not see the status bar in the bottom portion of the web client window, with the status “Initializing”, this may indicate that the HTML application (.xap file) for the web client has not loaded. Verify that the .xap file was installed with the web client runtime components.

## Web client is Initializing and becomes unresponsive

If the status bar indicates “Initializing” for an extended period of time, but no web client windows are displayed, then there is likely a communication problem between the HTML application in the web browser and the runtime service. Check the following:

-   Verify that you didn’t have any certificate errors reported in Internet Explorer when you access the Dynamics GP web client site. A certificate error can prevent the sign-on action from completing.

-   Verify that you can access the Runtime service. This is the service that the web client application communicates with on the session host machine. By default, this service is accessed through port 443. The port is secured with a security certificate. If there are any problems with the security certificate, the connection cannot be made. Use a web browser to access the following file on the session host machine:

<https://session_host_machine:443/clientaccesspolicy.xml>

The XML content for the file should be displayed in the web browser. If it is not, then there is an issue with the configuration of the runtime service. Usually the issue involves the security certificate that is used for the port. Use the following command to find the details of the security certificate that is bound to the port:

netsh http show sslcert

If you do not see that there is a security certificate bound to port 443, then the web client will need to be repaired or re-installed, so that a security certificate can be bound to the port.

-   Verify the security certificate that was selected for the Runtime service when the web client was installed. The client machine must be able to validate this security certificate so that the connection to the Runtime service can be established.

If you choose to use different security certificates for the web site and for the Runtime service, you are more likely to see this issue. The client machine is able to validate the security certificate for the web site, so no certificate error is reported in Internet Explorer. However, the client machine may not be able to validate the different security certificate that was used for the Runtime service. This prevents the connection from being established, but the error does not get displayed in Internet Explorer. One way to resolve this situation is to use the same security certificate for both the web site and the Runtime service.

-   Verify that the web client is running in trusted mode on the client machine. If you see the padlock icon in the lower-left corner of the web client window, the application is not running in trusted mode. This can indicate that the machine that is running the web client does not have the required security certificate for the Silverlight .xap file. This may prevent the application from initializing.

## Port issues

For the web client to work properly, the appropriate ports must be opened in the computer ’s firewall. The Microsoft Dynamics GP Web Client installer opens the appropriate ports when components of the web client are installed. You can use the following command to list the ports that are open on a system:

netstat - anob

Port accessibility issues are more likely to occur in scale out installation, when web client components are installed on different machines. For example, the session host machines must be able to access the Session Central Service, which is typically done through port 48651. That means this port must be open on the system that is running the Session Central Service.

Another common port accessibility problem is the port used for the runtime service. This issue is more common if you use a port other than 443, the default port. This port must be opened so that the web client on an end-user machine can access the runtime instance on the session host machine.

## Performance issues

In a typical installation of the web client, the performance of the web client is comparable to the performance of a desktop client. You can expect that some operations may be slower in the web client, while other actions may be faster. If you notice that the web client does not have good performance, it is worth further investigation.

### Session host performance

To gauge the overall system performance, verify the performance that you see when you run the Microsoft Dynamics GP desktop client on each session host machine. If the desktop client does not have optimal performance, the web client sessions that are hosted on that machine will also have sub-optimal performance. When you resolve the desktop client performance issues, the web client performance should also improve.

### Real-time virus scanning

On each session host machine, consider turning off real-time virus scanning for the runtime session process. The runtime session process is going to be very active, and can attract the attention of antivirus software. Limiting the scanning can speed up performance of the web client sessions.

### Virtual machine configuration

You may be using a virtualization solution such as Hyper-V, and installed the web client into a virtual machine configuration. Check the settings for the virtual machines to be sure they are optimal for the workload of the web client. For example, a virtual machine that is running low on memory may have reduced performance.

Another situation that can occur with virtual machines involves Network Interface Card (NIC) settings that are not fully compatible with the operating system settings. Specifically, NIC settings may be set to use “offload” optimizations that actually slow down network performance for the virtual machine. To turn off these optimizations, do the following on each virtual machine.

1. Open the **Network and Sharing Center**.

2. Click the link for Connections to view the information about the local network connection.

3. Click **Properties**.

4. Click **Configure**.

5. Click the **Advanced** tab.

6. Disable all of the settings that have “offload” in their name.

7. Click **OK** to save the changes. This will reset the NIC for the virtual machine.

## Printing issues

The follow printing issues may occur.

### Printing to a file

When a web client user prints a report that uses a Word template, and chooses to save the report to a file, the file may not be saved in the location that was specified. The user may also see a “file not found” error if they chose to display the report on their local machine. Typically, this indicates that the security settings for Internet Explorer are preventing the file from being written to the local machine.

To solve this problem, perform one or both of these actions in the Internet Options window for Internet Explorer:

-   Display the Security tab. Add the URL for the Microsoft Dynamics GP web client site to the Trusted sites list.

-   Reduce the security level for the specified zone. For example, if you are running the Microsoft Dynamics GP web client in an intranet setting, reduce the security level for the Local intranet zone.

## Help not available

Depending on the order that the web client components are installed, the web client help components might not be installed. If this occurs, you can manually install the web client help components.
