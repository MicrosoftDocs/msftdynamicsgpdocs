---
title: "Core System Requirements for Dynamics GP"
description: View the complete list of system requirements for deploying Dynamics GP.
keywords: "install"
author: edupont04
manager: annbe
ms.prod: dynamics-gp
ms.topic: article
ms.author: edupont
ms.date: 01/06/2021
---
# Core System Requirements for Microsoft Dynamics GP

This document contains the minimum client hardware requirements, server recommendations and Terminal Server minimum hardware requirements supported by the Microsoft Dynamics GP Technical Support Team. The following server recommendations are not minimum server requirements. The requirements and recommendations are based on experience with many different installations. Users may need to increase these requirements due to environmental factors to achieve ​individual performance expectations.  

Review each Customer Profile below to determine what profile best fits the user count, modules used and transaction volume for your environment. Use that Customer Profile as a recommendation for your server hardware implementation.​

## Client Requirements

This tab​le lists client requirements

| Item​ | Requir​ements(32-bit) | Requir​ements(64-bit) |
| ---- | -------------------- | -------------------- |
| Operating System | <ul><li>Microsoft Windows 10</li><li>Professional Edition</li><li>Microsoft Windows 10</li><li>Enterprise Edition</li><li>Microsoft Windows 8 & 8.1</li><li>Professional Edition</li><li>Microsoft Windows 8 & 8.1</li><li>Ultimate Edition</li><li>Microsoft Windows 8 & 8.1</li><li>Enterprise Edition</li><li>Microsoft Windows 7</li><li>Professional Edition</li><li>Microsoft Windows 7</li><li>Ultimate Edition</li><li>Microsoft Windows 7</li><li>Enterprise Edition</li></ul> | <ul><li>Microsoft Windows 10</li><li>Professional Edition</li><li>Microsoft Windows 10</li><li>Enterprise Edition</li><li>Microsoft Windows 8 & 8.1</li><li>Professional Edition</li><li>Microsoft Windows 8 & 8.1</li><li>Ultimate Edition</li><li>Microsoft Windows 8 & 8.1</li><li>Enterprise Edition</li><li>Microsoft Windows 7</li><li>Professional Edition</li><li>Microsoft Windows 7</li><li>Ultimate Edition</li><li>Microsoft Windows 7</li><li>Enterprise Edition</li></ul>|
|Processor|1 Dual Core or 1 Single Core Processor 2.6 GHz or higher|1 Dual Core or 1 Single Core Processor 2.6 GHz or higher|
|Available Hard Disk Space|2GB or more on the system root|2GB or more on the system root|
|Minimum Available RAM ​|2GB or more|2GB or more |
|Network Card ​|1GB Ethernet| |
|Microsoft Office ​ ​| Microsoft Office 2013 32bit & x64<br/>Microsoft Office 2016 32bit & x64 <br/> **NOTES:**<br/>1. If using Office x64, the server type in System Preferences (Microsoft Dynamics GP \| Tools \| System \| Setup \| System Preferences) must be set to Exchange.<br/>2. Before you can send documents as DOCX, PDF, or XPS attachments, the Word template for the document must be enabled in the Template Configuration Manager window.<br/>3. If using Office 32bit, the server type in System Preferences can either be MAPI or Exchange| |
|Internet Explorer ​|Internet Explorer 11.0  - Desktop Mode Only Edge   | |
|ODBC ​Driver ​| SQL Native Client 11.0<br/>SQL Native Client 10.0<br/>**NOTE:** A 32bit ODBC DSN is required for Microsoft DynamicsGP 2016 and later| |
|Adobe ​|Adobe X | |
|Virtual Environments Supported (Optional)|Hardware Virtualization<br/>Windows Server 2016 Hyper-V<br/>Windows Server 2012 Hyper-V<br/>Windows Server 2012 R2 Hyper-V​<br/>Windows Server 2008 R2 Hyper-V<br/>Windows Server 2008 Hyper-V<br/><br/>Software Virtualization <br/>Microsoft Application Virtualization (App-V) 5.0<br/><br/>For additional Virtual Technology Support, [review the Virtualization Support Policy Wizard](https://www.windowsservercatalog.com/svvp.aspx?svvppage=svvpwizard.htm). Choose **Products** to see if your Virtual Technology is listed.​||

> [!NOTE]
> The following are no longer supported with Microsoft Dynamics GP 2016 and later:
>
> - Microsoft Office 2010 32bit & x64

A 32-bit ODBC DSN is required for Microsoft Dynamics GP on a 32-bit and x64 machine. For more information, see  [KnowledgeBase Article 870416](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?WTNTZSMNWUKNTMMYQLYTNSUKZPXKMUNVXKKPSXMZYMPRZQTLQRUPZKVQYSQQRKXQ).

When you deploy a system in a virtual environment, make sure that you have sufficient hard disk space to avoid performance problems. Each computer that you deploy in a virtual environment should meet or exceed the random access  memory (RAM) requirements and the hard disk space requirements. For more information, click the following article number to view the article in the Microsoft Knowledge Base: ​ [897615](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb%3ben-us%3b897615) Support policy for Microsoft software running in non-Microsoft hardware virtualization software.

## Server Recommendations: Customer Profile 1

Customer Profile 1 Usage:

- Use only Financial Series modules
- Have between 0-5 concurrent users for Microsoft SQL Server or for Microsoft SQL Server Express
- Process fewer than 250 transactions per day
- No web applications in use
- Peer to Peer environment

This tab​le lists server recommendations
| Item​ | Requir​ements(32-bit) | Requir​ements(64-bit) |
| ---- | -------------------- | -------------------- |
| **Database Requirements**                     | Microsoft SQL Server 2016<br/>- Enterprise, Standard or Express<br/>Microsoft SQL Server 2014<br/>- Enterprise, Standard or Express<br/>Microsoft SQL Server 2012 <br/>- Enterprise, Standard or Express <br/>**Supported Microsoft SQL Server Collation <br/>1. Dictionary Order Case Insensitive - Sort Order 52** In the SQL Server Management Studio, right-click the SQL Server Name and click Properties: Server  Collation = SQL\_Latin1\_General\_CP1\_CI\_AS <br/>**2. Binary - Sort Order 50** In the SQL Server Management Studio, right-click the SQL Server Name and click Properties:Server Collation = Latin1\_General\_BIN | Microsoft SQL Server 2016<br/>- Enterprise, Standard or Express<br/>Microsoft SQL Server 2014<br/>- Enterprise, Standard or Express<br/>Microsoft SQL Server 2012 <br/>- Enterprise, Standard or Express <br/>**Supported Microsoft SQL Server Collation <br/>1. Dictionary Order Case Insensitive - Sort Order 52** In the SQL Server Management Studio, right-click the SQL Server Name and click Properties: Server Collation = SQL\_Latin1\_General\_CP1\_CI\_AS<br/>**2. Binary - Sort Order 50** In the SQL Server Management Studio, right-click the SQL Server Name and click Properties: Server  Collation = Latin1\_General\_BIN |
| **Operating System**  | Microsoft Windows Server 2008 Standard Edition SP2 or later| Microsoft Windows Server 2016  Essentials Edition or Standard Edition<br/>Microsoft Windows Server 2012  Essentials Edition or Standard Edition<br/>Microsoft Windows Server 2012 R2 Essentials Edition or Standard Edition <br/>Microsoft Windows Server 2008 R2 Standard Edition SP1 or later<br/>Microsoft Windows Server 2008 Standard Edition SP2 or later  |
| **Processor**                                 | 1 Dual Core or 2 Single Core Processors  | 1 Dual Core or 2 Single Core Processors  |
| **Minimum Available RAM**                     | 2 GB or more | 2 GB or more |
| **Network Card**                              | 1GB Ethernet|          |
| **Virtual Environments Supported (Optional)** | Hardware Virtualization <br/>Windows Server 2016 Hyper-V <br/>Windows Server 2012 Hyper-V<br/>Windows Server 2012 R2 Hyper-V<br/>​Windows Server 2008 R2 Hyper-V<br/>Windows Server 2008 Hyper-V<br/><br/>Software Virtualization <br/><br/>Microsoft Application Virtualization (App-V) 5.0. For additional Virtual Technology Support, [review the Virtualization Support Policy Wizard](https://www.windowsservercatalog.com/svvp.aspx?svvppage=svvpwizard.htm). Choose Products to see if your Virtual Technology is listed.  |   |

> [!NOTE]
> The following are no longer supported with Microsoft Dynamics GP 2016 and later:
>
> - Microsoft Office 2010 32bit & x64

Microsoft SQL Server 2008 Express or Microsoft SQL Server 2012 Express can be installed on a non-server operating system, however it is recommended to install on a  server operating system.  

Verify processors can be upgraded.

When you deploy a system in a virtual environment, make sure that you have sufficient hard disk space to avoid performance problems. Each computer that you deploy in a virtual environment should meet or exceed the random access memory (RAM) requirements and the hard disk space requirements. For more information, click the following article number to view the article in the Microsoft Knowledge Base: [897615](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb%3ben-us%3b897615) Support policy for Microsoft software running in non-Microsoft hardware virtualization software.

## Server Recommendations: Customer Profile 2

Customer Profile 2 Usage:

- Use only Financial Series modules
- Have between 0-20 concurrent users for Microsoft SQL Server or 0-10 concurrent users for Microsoft SQL Server Express Use
- Report Writer, Crystal Reports, or Management Reporter
- Process fewer than 1000 transactions per day
- Import very little data
- Dedicated server with Microsoft SQL Server only
- Recommend a dedicated server with Microsoft SQL Server Express only

This tab​le lists server recommendations for customer profile 2

| Item​ | Requir​ements(32-bit) | Requir​ements(64-bit) |
| ---- | -------------------- | -------------------- |
| **Database Requirements**                               | Microsoft SQL Server 2016<br />-Enterprise, Standard or Express<br />Microsoft SQL Server 2014<br />-Enterprise, Standard or Express<br />Microsoft SQL Server 2012 -                   <br />Enterprise, Standard or Express **Supported Microsoft SQL <br />Server Collation<br /> 1. Dictionary Order Case <br />Insensitive - Sort Order 52**<br /> In the SQL Server Management <br />Studio, right-click the SQL <br />Server Name and click <br />Properties: Server Collation = SQL\_Latin1\_General\_CP1\_CI\_AS **2. Binary - Sort Order 50** <br />In the SQL Server Management <br />Studio, right-click the SQL <br />Server Name and click <br />Properties: Server Collation = Latin1\_General\_BIN<br /> | Microsoft SQL Server 2016<br />-Enterprise, Standard or Express<br />Microsoft SQL Server 2014<br />-Enterprise, Standard or Express <br /> Microsoft SQL Server 2012 - <br />Enterprise, Standard or Express **Supported Microsoft SQL Server Collation<br /> 1. Dictionary Order Case Insensitive - Sort Order 52**<br /> In the SQL Server <br />Management Studio, <br />right-click the SQL Server <br />Name and click <br />Properties: Server Collation = SQL\_Latin1\_General\_CP1\_CI\_AS **2. Binary - Sort Order 50** <br />In the SQL Server <br />Management Studio, <br />right-click the SQL Server <br />Name and click Properties: <br />Server Collation = Latin1\_General\_BIN  |
| **Operating System**                                    | Microsoft Windows Server <br />2008 Standard Edition SP2 or <br />later<br /> Microsoft Windows Small <br />Business Server 2008 Premium                <br />Edition SP2 or later<br /> | Microsoft Windows Server <br />2016  Essentials Edition or <br />Standard Edition<br />Microsoft Windows Server <br />2012 Essentials Edition or <br />Standard Edition<br />Microsoft Windows Server <br />2012 R2 Essentials Edition or <br />Standard Edition Microsoft Windows Server <br />2008 R2 Standard Edition <br /> SP1 or later<br /> Microsoft Windows Server <br />2008 Standard Edition SP2 <br />or later |
| **Processor**                                                | 1 Dual Core or 2 Single Core <br />Processors | 1 Dual Core or 2 Single <br />Core Processors  |
| **Disk Configuration**                                  | RAID 1 for operating system <br />and applications (2 disks)<br />RAID 5 for SQL database log and <br />data files (4 disks)| RAID 1 for operating <br />system and applications <br />(2 disks)<br /> RAID 5 for SQL database <br />log and data files (4 disks) |
| **Minimum Available RAM**                          | 2 GB or more | 2 GB or more |
| **Network Card**                                        | 1GB Ethernet |  |
| **Virtual Environments Supported (Optional)** | Hardware Virtualization <br />Windows Server 2016 Hyper-V <br />Windows Server 2012 Hyper-V<br />Windows Server 2012 R2 Hyper-V​<br />Windows Server 2008 R2 Hyper-V<br />Windows Server 2008 Hyper-V<br /><br />Software Virtualization <br />Microsoft Application Virtualization (App-V) 5.0<br /><br />For additional Virtual Technology Support, [review the Virtualization Support Policy Wizard](https://www.windowsservercatalog.com/svvp.aspx?svvppage=svvpwizard.htm). Choose Products to see if your Virtual Technology is listed.|    |

## Server Recommendations: Customer Profile 3

Customer Profile 3 Usage:

- Use Financials Series modules
- Use Distribution Series modules moderately
- Use Field Service Series modules
- Use Manufacturing Series or Project Series modules moderately
- Have between 20 and 60 concurrent users
- Use Terminal Server
- Use Report Writer, Crystal Reports or Management Reporter
- Perform some online analytical processing (OLAP) cube generation
- Using an import routine/eConnect/Integration Manager
- Process between 1000 and 4000 transactions per day - Originating in Sales (SOP and/or RM), Payables, or General Ledger
- Dedicated Microsoft SQL Server

This tab​le lists server recommendations for customer profile 3
| ​I​​tem                                          | Requir​ements(32-bit)| Requir​ements(64-bit) |
|-----------------------------------------------|---------------------|----------------------|
| **Database Requirements**                     | Microsoft SQL Server 2016<br/>-Enterprise or Standard<br/>Microsoft SQL Server 2014<br/>Enterprise or Standard <br/> Microsoft SQL Server 2012 - <br/>Enterprise or Standard **Supported Microsoft SQL <br/>Server Collation<br/> 1. Dictionary Order Case <br/>Insensitive - Sort Order <br/>52**<br/> In the SQL Server <br/>Management Studio, <br/>right-click the SQL Server <br/>Name and click Properties: <br/>Server Collation = SQL\_Latin1\_General\_CP1\_CI\_AS **2. Binary - Sort Order 50** <br/>In the SQL Server <br/>Management Studio, <br/>right-click the SQL Server <br/>Name and click Properties: <br/>Server Collation = Latin1\_General\_BIN<br/> | Microsoft SQL Server 2016<br/>-Enterprise or Standard <br/>Microsoft SQL Server 2014<br/>Enterprise or Standard <br/> Microsoft SQL Server 2012 - <br/>Enterprise or Standard <br/> **Supported Microsoft SQL <br/>Server Collation<br/> 1. Dictionary Order Case <br/>Insensitive - Sort Order 52**<br/> In the SQL Server Management <br/>Studio, right-click the SQL <br/>Server Name and click <br/>Properties: Server Collation = SQL\_Latin1\_General\_CP1\_CI\_AS **2. Binary - Sort Order 50** <br/>In the SQL Server Management <br/>Studio, right-click the SQL <br/>Server Name and click <br/>Properties: Server Collation = Latin1\_General\_BIN |
| **Operating System**                         | Microsoft Windows Server <br/>2008 SP2 or later - <br/>Enterprise Edition or <br/>Standard Edition <br/> <br/> | Microsoft Windows Server <br/>2016 Standard or Datacenter <br/>Edition<br/>Microsoft Windows Server <br/>2012 Standard or Datacenter <br/>Edition<br/>Microsoft Windows Server <br/>2012 R2 Standard or Datacenter <br/>Edition Microsoft Windows Server <br/>2008 R2 Enterprise Edition or <br/>Standard Edition SP1 or later<br/> Microsoft Windows Server 2008 <br/> SP2 or later - Enterprise Edition <br/>or Standard Edition<br/>  |
| **Processor**                                | 1 Dual Core or 2 Single <br/>Core Processors   | 1 Dual Core or 2 Single <br/>Core Processors    |
| **Disk <br/>Configuration**                  | RAID 1 for operating <br/>system and applications <br/>(2 disks)<br/>RAID 1 for SQL database <br/>log files (2 disks)<br/>RAID 5 (4 disk minimum) <br/>or RAID 0+1 (8 disk <br/> minimum) for SQL data files <br/>RAID 1 for TempDB (2 <br/> disks) - optional, but <br/>recommended<br/>RAID 0 for SQL backups <br/>(full and log) (2 disks)  | RAID 1 for operating system and <br/>applications (2 disks)<br/> RAID 1 for SQL database log files <br/>(2 disks)<br/> RAID 5 (4 disk minimum) or <br/>RAID 0+1 (8 disk minimum) <br/>for SQL data files<br/> RAID 1 for TempDB (2 disks) - <br/>optional, but recommended<br/> RAID 0 for SQL backups (full <br/>and log) (2 disks) |
| **Minimum <br/>Available <br/>RAM**                          | 4 GB or more   | 4 GB or more  |
| **Network <br/>Card**                                        | 1GB Ethernet |   |
| **Virtual <br/>Environments<br/> Supported <br/>(Optional)** | Hardware Virtualization Windows Server 2016 Hyper-V <br/>Windows Server 2012 Hyper-V<br/>Windows Server 2012 R2 Hyper-V​<br/>Windows Server 2008 R2 Hyper-V<br/>Windows Server 2008 Hyper-V<br/><br/>Software Virtualization <br/>Microsoft Application Virtualization (App-V) 5.0<br/><br/>For additional Virtual Technology Support, [review the Virtualization Support Policy Wizard](http://www.windowsservercatalog.com/svvp.aspx?svvppage=svvpwizard.htm). Choose Products to see if your Virtual Technology is listed.​<br/>  |  |

> [!NOTE]
> The following are no longer supported with Microsoft Dynamics GP 2016 and later:
>
> - Microsoft Office 2010 32bit & x64

Verify processors can be upgraded.

Additional disks will improve Microsoft SQL Server performance.

Verify switch is capable of handling network traffic.

When you deploy a system in a virtual environment, make sure that you have sufficient hard disk space to avoid performance problems. Each computer that you deploy in a virtual environment should meet or exceed the random access memory (RAM) requirements and the hard disk space requirements. For more information, click the following article number to view the article in the Microsoft Knowledge Base: [897615](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb%3ben-us%3b897615) Support policy for Microsoft software running in non-Microsoft hardware virtualization software.

## Server Recommendations: Customer Profile 4

Customer Profile 4 Usage:

- Use Financials Series and Distribution Series modules extensively
- Use Field Service Series, Manufacturing Series, and Project Series modules extensively
- Have between 60 and 100 concurrent users
- Use Terminal Server
- Use Report Writer, Crystal Reports, or Management Reporter extensively
- Use an import routine extensively - eConnect Process more than 4000 transactions per day - Originating in Sales (SOP and/or RM), Payables, or General Ledger Perform online analytical processing (OLAP) cube generation (to different machine)
- Dedicated Microsoft SQL Server  

This tab​le lists server recommendations for customer profile 4

| ​I​​tem                                               | Requir​ements(32-bit)    | Requir​ements(64-bit) |
|----------------------------------------------------|-------------------------|----------------------|
| **Database Requirements**                               | Microsoft SQL Server 2016 <br/>- Enterprise or Standard <br/>Microsoft SQL Server 2014 <br/>Enterprise or Standard Edition <br/>Microsoft SQL Server 2012 Enterprise or Standard Edition **Supported Microsoft SQL <br/>Server Collation <br/> 1. Dictionary Order Case <br/>Insensitive - Sort Order 52** <br/> In the SQL Server <br/>Management Studio, <br/>right-click the SQL Server <br/>Name and click Properties: <br/>Server Collation = SQL\_Latin1\_General\_CP1\_CI\_AS **2. Binary - Sort Order 50** <br/>In the SQL Server <br/>Management Studio, <br/>right-click the SQL Server <br/>Name and click Properties: <br/>Server Collation = Latin1\_General\_BIN <br/> | Microsoft SQL Server 2016 <br/>-Enterprise or Standard <br/>Microsoft SQL Server 2014 <br/>Enterprise or Standard Edition <br/>Microsoft SQL Server 2012 Enterprise or Standard Edition **Supported Microsoft SQL <br/>Server Collation <br/> 1. Dictionary Order Case <br/>Insensitive - Sort Order 52** <br/> In the SQL Server <br/>Management Studio, right- <br/>click the SQL Server Name <br/>and click Properties: Server <br/>Collation = SQL\_Latin1\_General\_CP1\_CI\_AS **2. Binary - Sort Order 50** <br/>In the SQL Server <br/>Management Studio, <br/>right-click the SQL Server <br/>Name and click Properties: <br/>Server Collation = Latin1\_General\_BIN |
| **Operating System**                                    | Microsoft Windows Server <br/>2008 Enterprise Edition SP2 or later | Microsoft Windows Server <br/>2016 Datacenter Edition <br/>Microsoft Windows Server <br/>2012 Datacenter Edition <br/>Microsoft Windows Server <br/> 2012 R2 Datacenter Edition <br/>Microsoft Windows Server <br/>2008 R2 Enterprise Edition <br/>SP1 or laterMicrosoft Windows Server <br/>2008 Enterprise Edition SP2 or later   |
| **Processor**                                                | 2 Dual Core or 4 Single Core Processors | 2 Dual Core or 4 Single Core Processors |
| **Disk Configuration**                                  | RAID 1 for operating system <br/>and applications (2 disks) <br/>RAID 1 for SQL database log <br/>files (2 disks) <br/>RAID 1 for TempDB (2 disks) <br/>RAID 0 for SQL backups (full <br/>and log) (2 disks) <br/> RAID 0+1 for data files (8 <br/>disks or more) | RAID 1 for operating system <br/>and applications (2 disks)RAID 1 for SQL database log <br/>files (2 disks)RAID 1 for TempDB (2 disks)RAID 0 for SQL backups (full and log) (2 disks) RAID 0+1 for data files (8 disks or more) |
| **Minimum Available RAM**                          | 8 GB or more   | 8 GB or more |
| **Network Card**                                        | 1GB Ethernet                              |  |
| **Virtual Environments Supported (Optional)** | Hardware Virtualization <br/>Windows Server 2016 Hyper-V <br/>Windows Server 2012 Hyper-V <br/>Windows Server 2012 R2 Hyper-V​ <br/>Windows Server 2008 R2 Hyper-V <br/>Windows Server 2008 Hyper-V <br/> <br/>Software Virtualization <br/>Microsoft Application Virtualization (App-V) 5.0 <br/> <br/>For additional Virtual Technology Support, [review the Virtualization Support Policy Wizard](https://www.windowsservercatalog.com/svvp.aspx?svvppage=svvpwizard.htm). Choose Products to see if your Virtual Technology is listed.|     |

> [!NOTE]
> The following are no longer supported with Microsoft Dynamics GP 2016 and later:
>
> - Microsoft Office 2010 32bit & x64

Verify processors can be upgraded to 8 processors.

Additional disks will improve Microsoft SQL Server performance.  

Verify switch is capable of handling network traffic.

When you deploy a system in a virtual environment, make sure that you have sufficient hard disk space to avoid performance problems. Each computer that you deploy in a virtual environment should meet or exceed the random access memory (RAM) requirements and the hard disk space requirements. For more information, click the following article number to view the article in the Microsoft Knowledge Base: [897615](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb%3ben-us%3b897615) Support policy for Microsoft software running in non-Microsoft hardware virtualization software.

## Remote Desktop Services Requirements

| Item | Requirements(32-bit) | Requirements(64-bit) |
|--|--|--|
| **Operating  System** | Microsoft Windows Server  <br/>2008 SP2 or later -  <br/> Enterprise Edition or  <br/>Standard Edition  <br/> | Microsoft Windows Server  <br/>2016 Datacenter Edition  <br/>Microsoft Windows Server  <br/>2012 Datacenter Edition  <br/>Microsoft Windows Server  <br/> 2012 R2 Datacenter Edition  <br/>Microsoft Windows Server  <br/>2008 R2 SP1 or later -  <br/>Enterprise Edition or  <br/>Standard EditionMicrosoft Windows Server  <br/>2008 SP2 or later - Enterprise  <br/> Edition or Standard Edition |
| **Citrix  (Optional)** | Citrix XenApp | Citrix XenApp |
| **Processor** | 1 Quad Core or 2 Dual  <br/>Core Processors or higher | 1 Quad Core or 2 Dual Core  <br/>Processors or higher |
| **Disk  Configuration** | RAID 1 for operating  <br/>system and applications  <br/>(2 disks) | RAID 1 for operating system  <br/>and applications (2 disks) |
| **Minimum Available RAM** | 4 GB – Up to 15 concurrent  <br/>users  <br/> 8 GB – Up to 30 concurrent  <br/>users  <br/> 16 GB – Up to 60  <br/>concurrent users | 4 GB – Up to 15 concurrent  <br/>users  <br/> 8 GB – Up to 30 concurrent  <br/>users  <br/> 16 GB – Up to 60  <br/>concurrent users |
| **Network Card** | 1GB Ethernet |  |
| **Virtual Environments Supported (Optional)** | Hardware Virtualization  <br/>Windows Server 2016 Hyper-V  <br/>Windows Server 2012 Hyper-V  <br/>Windows Server 2012 R2 Hyper-V​  <br/>Windows Server 2008 Hyper-V  <br/>Windows Server 2008 R2 Hyper-V  <br/>  <br/>Software Virtualization  <br/>Microsoft Application Virtualization (App-V) 5.0  <br/>  <br/>For additional Virtual Technology Support, [review the Virtualization Support Policy Wizard](http´s://www.windowsservercatalog.com/svvp.aspx?svvppage=svvpwizard.htm). Choose **Products** to see if your Virtual Technology is listed. |  |

> [!NOTE]
> The following are no longer supported with Microsoft Dynamics GP 2016 and later:
>
> - Microsoft Office 2010 32bit & x64

It is recommended to have a dedicated Terminal Server/Citrix Server. There may be performance losses if Microsoft SQL Server is running on the Terminal Server/ Citrix Server. Therefore, it is highly recommended to have two separate servers. One server with Terminal Server and/or Citrix and one server with Microsoft SQL Server.  

If using Adobe, Adobe must be installed at the Terminal Server.

If using Lync for Unified Communications, a remote app for Lync must also be configured and copied to the client along with the Microsoft Dynamics GP remote app.  The Lync remote app must be launched first and then the Microsoft Dynamics GP remote app.  

If accessing Citrix, the hardware and software must be supported according to the Citrix configuration requirements.

Verify processors can be upgraded.  

The amount of RAM needed depends on the number of concurrent users per Terminal Server.

Verify switch is capable of handling network traffic.

Increased user count may require greater RAM and Processor speed.

Users utilizing Management Reporter or Crystal reporting via Terminal Services may require increased hardware to increase performance.

When you deploy a system in a virtual environment, make sure that you have sufficient hard disk space to avoid performance problems. Each computer that you deploy in a virtual environment should meet or exceed the random access memory (RAM) requirements and the hard disk space requirements. For more information, click the following article number to view the article in the Microsoft Knowledge Base: [897615](https://mbs.microsoft.com/knowledgebase/KBDisplay.aspx?scid=kb%3ben-us%3b897615) Support policy for Microsoft software running in non-Microsoft hardware virtualization software.

## Additional Information

1. This document represents configurations tested by Microsoft and supported by Microsoft Dynamics GP Technical Support. Use of technologies not specified in this document is not recommended and will not be supported. Testing
is ongoing, and as newer technologies become supported this list will be updated.  

2. The following are no longer supported with Microsoft Dynamics GP 2016 and later versions:

   - Windows XP all editions  
   - Windows Server 2003 all editions  
   - Windows Vista all editions  
   - Microsoft Office 2007  
   - Microsoft SQL Server 2008 all editions  
   - Microsoft SQL Server 2008 R2 all editions  
   - Office Communicator 2007  
   - Microsoft Office 2010 32bit & x64  
   - Internet Explorer 10.0  

3. View KnowledgeBase article regarding support in a virtual environment. The following virtual products have been tested: Microsoft Windows  Server 2016 Hyper-V, Microsoft Window Server 2012 R2 Hyper-V, Microsoft Windows  Server 2012 Hyper-V,  Windows Server 2008 R2 Hyper-V, Microsoft Windows  Server 2008 Hyper-V, Microsoft Application Virtualization (App-V) 5.0.  

    For additional Virtual Technology Support, review the Virtualization Support Policy Wizard. Choose Products to see if your Virtual Technology is listed.

4. The Microsoft Dynamics GP core application is supported in a peer to peer (workgroup) environment. This environment excludes all web applications such as Web Services, eConnect, and Management Reporter. This also excludes Workflow 2.0 as a domain is required.   If web applications are used, a domain is required.

5. Remote access for Microsoft Dynamics GP is not supported in a WAN or P2P environment due to the possibility of connection and data consistency errors.  

    The only supported options are to one of the following:

    1. Have Microsoft Dynamics GP installed on a Remote Desktop Services machine (with or without Citrix) in the same network as the SQL Server hosting your Dynamics GP databases  
    2. Deploy the Dynamics GP Web Client for extranet access and allow users to log in from remote browsers.  

6. If you have questions regarding licensing SQL Server for use with Dynamics GP. Please contact a Licensing Specialist at 1-800-426-9400.​​

## Support Information

For technical support questions, contact your partner or direct your
questions to the [Support for Business hub](https://serviceshub.microsoft.com/supportforbusiness/create).  

## See also

[System Requirements](../upgrade/system-requirements.md)  
[Installation overview](../web-components/installation-overview.md)  
[Installation checklist](installation-checklist.md)  
[Upgrade checklist](../upgrade/upgrade-checklist.md)  
