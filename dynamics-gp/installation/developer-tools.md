---
title: "Developer Tools"
description: "Information around eConnect, Integration Manager and Web Services in Microsoft Dynamics GP."
keywords: "import"
author: theley502
manager: jswymer
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 3/5/2025
---

# Developer Tools

This documentation supports developers who work with Microsoft Dynamics GP.

## eConnect 

This documentation contains detailed information about the operations, classes, XML schemas and nodes available in Microsoft [Dynamics GP eConnect](/previous-versions/dynamicsgp/developer/bb219081(v=msdn.10)). 

The Microsoft eConnect procedures are encrypted to preserve the Microsoft intellectual property.

Business Logic Modification: eConnect provides both Pre and Post procedures for modifying business logic before passing a transaction through eConnect to Microsoft Dynamics GP. If these procedures were not encrypted, unauthorized modifications could be made, potentially leading to incorrect business logic application and data corruption.

Therefore, keeping Dynamics eConnect procedures encrypted is essential for data security, compliance with standards, and maintaining the integrity of business logic. It’s advised against modifying any Dynamics GP stored procedures as it may cause problems with your Microsoft Dynamics GP data.

However, over the years, we have found some issues with a few of the eConnect procedures based on business practices for a specific company. Microsoft is not actively fixing these issues in the eConnect shipping product, due to the life cycle of the product. The below published procedures are modified eConnect procedures with fixes around areas a large majority of customers have run into.

These modified procedures are use at your own risk and should be tested by your company before using in your production system.  When you upgrade Microsoft Dynamics GP, these modified procedures may be lost.

- [taPOPCreateDistributions](https://mbs2.microsoft.com/fileexchange/?fileID=e004756e-9413-4fed-9b4a-82306d2763b2) - December 2023
- [taCalcDueDatePM](https://mbs2.microsoft.com/fileexchange/?fileID=400b0ad2-3452-470f-bc99-e690c12dab60) - December 2023
- [taCalcDueDateRM](https://mbs2.microsoft.com/fileexchange/?fileID=6f1f21fb-8eec-4527-b163-578e4e55b06f) - December 2023
- [taSOPLot](https://mbs2.microsoft.com/fileexchange/?fileID=57c819dc-2a7b-44e8-91ab-ee23c0edb054) - May 2021
- [taPopRcptLineInsert](https://mbs2.microsoft.com/fileexchange/?fileID=1a5851ef-d68f-4cfc-af66-fa1ab70302e7) -	May 2022
- [taRMApply](https://mbs2.microsoft.com/fileexchange/?fileID=665f3fe9-3316-458e-b5df-96573b873bd1) - December 2024

## Web Services

This documentation describes [Web Services for Microsoft Dynamics GP](/previous-versions/dynamicsgp/developer/cc534132(v=msdn.10)). 
The programmer's guide contains information about how to use the services. 
The web service reference contains detailed information about the operations, classes, enumerations, and policies available in the Dynamics GP service. 

## Integration Manager

Integration Manager for Microsoft Dynamics GP is a tool designed to help you move data quickly and easily between applications without the need for custom programming or extensive knowledge of application databases. 
Regardless of which combinations of sources and destinations you eventually use, the steps to building and running integrations are basically the same.

### Common Error Messages

#### The destination could not be initialized due to the following problem: Cannot create ActiveX component

Normally this issue is caused by either a permissions issue or something with the IM client install.  
Can other user log onto this machine and see the issue?  If so,  that would suggest it is related to permissions in your case.
The Dynamics GP and IM client need to be running under the same context.  
You may see this error when you don't launch both GP and IM as administrator since they are not running as the same user.  
Right-click on GP and select Run as Administrator, then launch IM in the same way can you reproduce the issue? 
Another option for this error message is even though it doesn't seem like an install it may be worthwhile to repair or reinstall IM on this workstation.  
It would not hurt to repair Dynamics GP either since IM relies on making a connection to that application.
Usually by doing this just once seems to tie things together at the OS level and allows IM to work without running as Administrator going forward.

#### Integration Manager progress bar disappears

Usually when you see this issue arise, it is user specific in nature. Typically, this is an environmental issue. 

Cause:  Windows Fonts DPI setting set to 125%

Resolution:
To resolve this, navigate to **Control Panel** > **Display**. Check the DPI setting. Sometimes, you will see it at 125%. Set it to 100% and then sign out and in to the computer. After launching GP and IM again, you should find the progress bar appeared.
 
Once you know more based on user, you can look at other items too such as:

- You can enable the draw window to flash in front of you all the time so you know exactly when it is done. In the Microsoft.Dynamics.GP.IntegrationManager.ini file, set the following parameters: 
  - `ShowDynamics=TRUE`
  - `DoUIRedraw=TRUE`
 
- Rename the main IM .ini file mentioned above, then run a repair against Integration Manager, which will re-create the .ini file in the same location. Then, launch Integration Manager and see if that resolves this issue.
 
- Rename the entire IM directory and run a repair against Integration Manager, which will re-create the entire IM directory, folders and files under the original name. Launch Integration Manager from this ‘new’ IM directory. You may need to point it at your IM database to test whether the progress window now shows.
 
- Lastly, complete an uninstall and reinstall of Integration Manager, which shouldn't affect anything as the integrations themselves are all held in the IM database. It is good practice to verify where the source files for IM are all stored, just so they’re not in a folder for Integration Manager that an uninstall would remove.

#### Unable to open source queries because Query 'XXXX' is not found in the database. - ADO Field is nothing.

- Does it work if you right click and launch IM as administrator? 
- What if you view the file does it seem to view or error out there too? 
- Is it just this IMD or does maybe the Sample IMD work for you?
 
If you haven’t already done so, try the steps in the [following article](https://community.dynamics.com/gp/b/dynamicsgp/archive/2012/02/07/ado-field-is-nothing-error-message-in-integration-manager)

Other causes:

1. If the source file is on a mapped drive or other network location, try moving it to the local server where IM is installed, then point IM to that local copy to rule out intermittent network issues or just general issues with accessing the shared file.  You can also try copying the contents of the source file into a new source file, then point IM to that and continue testing.
 
2. This can also occur if the data type of a column was changed that is used in the Query Relationship window. Open the properties for each source and then click the Refresh Columns button on the Columns tab. After you refresh the columns, verify the mapping of the integration and the Query Relationship window are still correct.
 
3. Verify the query in the source was referencing a SQL view that did not exist in the company database that was being integrated.  
Also make sure the view does not reference a table that does not exist in the non-working company/ database.
 
4. This error will also surface if there is a period in the (.) in the Source filename.

   Example: The user was saving the file as FILE.11.23.23 - if you change the period to underscores or remove it, then the integration works. Make sure you have the VIEW for file extensions on in file explorer so this is easy to identify.

#### Error when reviewing log files for Integration Manager - The Microsoft.ACE.OLEDB.12.0 Provider is not registered on the local machine

This error usually occurs when the incorrect version of the Report Viewer Redistributable is installed on the machine where Integration Manager is running.

There are a couple Office redistributables that can be installed to address this error. Sometimes you need to install one, sometimes more than one. It seems to depend on the environment conditions.

1. Usually, you can uninstall the 2013 redistributable files. Install one or both of the following:

   - Microsoft Report Viewer Redistributable 2012
   - Microsoft Access Database Engine 2016 Redistributable

   [Download both Redistributable install files](https://mbs2.microsoft.com/fileexchange/?fileID=07fe2ceb-a580-419f-b4d4-45a028260637)

  If the above link does not work, try this download link: 
  [Report Viewer Redistributable 2008 Service Pack](https://www.microsoft.com/en-us/download/details.aspx?id=3203) 
  
1. Launch both Integration Manager and Dynamics GP using 'Run As Administrator' (right-click).

1. While in an integration, select View > Integration Logs and verify the log comes up without any errors.

   Also, in the integration progress window, select the 'View Log' button and to show the report.

If the above steps don't resolve this error, you can try a Repair of both Integration Manager and Microsoft Dynamics GP. If not, uninstall and reinstall or try to install this to another machine or example server, just to see if it works there. Then you know it is machine specific.

#### The destination could not be initialized due to the following problem: Unable to cast COM object of type 'System._ComObject' to interface type 'Dynamics Application'.

The full error message is similar to the following:

`The destination could not be initialized due to the following problem: Unable to cast COM object of type 'System._ComObject' to interface type 'Dynamics Application'. This operation failed because the QueryInterface call on the COM component for the interface with IID '{a0a0a0a0-bbbb-cccc-dddd-e1e1e1e1e1e1}`

Usually this error is specific to a machine or user.

There are a couple things that can cause this error, but in most cases this occurs when the Dynamics.exe is not properly registered in the system registry.

1. Try to manually reregister the Dynamics.exe by navigating to the directory where Dynamics GP is installed and locate the Dynamics.exe. Go to Start > Run and clear out any text that is present, then drag the Dynamics.exe onto the Run dialog and let go. This fills in the exact path wrapped in double quotes. Then after the ending double quote, add the text `/REGSERVER`.

   You should end up with a command resembling the following (don't copy the example as the path is likely different): `C:\Program Files\Microsoft Dynamics\GP$GP\Dynamics.exe" /REGSERVER`.

1. Select OK. If all goes well you  only see the cursor change for a second or two. Then try your integration again.
1. The next option we'd want to try, in order to resolve this issue, if registering Dynamics GP does not, is the following:

   - If on a x64 bit machine or server:  Select Start > Run, type in: `regsvr32 C:\Windows\sysWOW64\MSScript.ocx`.
   - If on a x86 bit machine or server:  Select Start > Run, type in: `regsvr32 C:\Windows\System32\MSScript.ocx`.

   Once you do this, run an integration logged on as the domain administrator, to verify it goes through without any error messages. If it does, then try with other user accounts. You cn also try to right-click and launch as Admin and see whether you have the same problem.

1. Rename the entire IM directory and run a repair against Integration Manager, which will re-create the entire IM directory, folders and files under the original name. Launch Integration Manager from this "new" IM directory. You may need to point it at your IM database to test whether the progress window now shows.

1. Uninstall and reinstall the Integration Manager and Dynamics GP, which shouldn't affect anything as the integrations themselves are all held in the IM database. It is good practice to verify where the source files for IM are all stored, just so they're not in a folder for Integration Manager that an uninstall would remove.

## Visual Studio Tools

This documentation contains detailed information about using [Visual Studio Tools for Microsoft Dynamics GP](/previous-versions/dynamicsgp/developer/cc543538(v=msdn.10)) to develop integrating applications. 
