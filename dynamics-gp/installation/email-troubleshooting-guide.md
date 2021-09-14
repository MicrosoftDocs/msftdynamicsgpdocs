---
title: Dynamics GP Email Troubleshooting Guide
description: Get tips and tricks about some of the errors you may run into when emailing out of Microsoft Dynamics GP.
keywords: "email"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 09/10/2021
---

# Microsoft Dynamics GP Email Troubleshooting Guide

This document is meant to walk through most of the errors you may run into when emailing out of Microsoft Dynamics GP.  

The goal is to make everyone an emailing expert!  

This document can be leveraged with all email functionality in Microsoft Dynamics GP, from the old Standard Report Writer Statement emailing method, to Word Templates.

> [!NOTE]
> Currently, TLS 1.0 and Basic Authentication (no MFA) are required for Exchange and Workflow emailing in Dynamics GP.
>
> We are aware of the changes that are coming to the supportability of TLS 1.0 and Basic Authentication within our other Microsoft applications. TLS 1.2 and Multi-Factor Authentication (MFA) functionality was included in the 18.3 update released.

All email issues can be safely split up into three sets of issues:

* Items unique to MAPI  
* Issues unique to Exchange  
* Those that both methods have in common  

This is how the documentation is organized: Starting with MAPI, moving onto Exchange, and ending with the common errors.  

Find system preferences under Dynamics GP Tools -> Setup -> System -> System Preferences.  

> [!IMPORTANT]
> This setting is stored in the DYNAMICS database and is system-wide, so changing this setting will affect all users.  

![Form](media/syspref.jpg)

## MAPI Specific Errors
Dynamics GP uses MAPI to open Outlook to send emails directly from the Outlook client.

### Emails Stuck in Outbox within Outlook.  

Note: Issue appears to be unique to Gmail accounts.  

Issue:  
Emails are getting stuck in the Outbox in Outlook. 

When you use the Send/Receive button, or close/reopen Outlook, the email sends without delays. 

Cause: 
Add-in for Gmail Multi-factor authentication. This is a paid add-in that we believe causes the issue.  

Solution: 
Compare a clean Outlook add-in list to the client having the issue to make sure there are no extra add-ins. 
Recommend that they [remove the add-in as it appears like it is no longer needed](https://support.office.com/article/add-a-gmail-account-to-outlook-701916679c52-4581-990e-e30318c2c081)

### No default mail client, or the current mail client cannot fulfill the message request

Please run Microsoft Outlook and set it as the default mail client. 

Note: Recommend you review Outlook version first – MAPI only works with 32bit! 

Issue:  Error appears when attempting to email using MAPI anywhere in GP Cause: Either a Profile is not setup, or Outlook cannot reach it using MAPI.  

Solution: You can go through [this KB](https://support.microsoft.com/en-us/help/4052892/e-mail-error-in-microsoftdynamics-gp-either-there-is-no-default-mail), focus on A and B as these are common causes.  

You will want to make sure that Outlook is also set up as the default application for mail when you search for Default Apps in Windows 10.  

### A program is trying to send an e-mail message on your behalf

Note: Happens a lot with more secure environments and newer versions of Office.

Issue: Outlook does not trust Microsoft Dynamics GP by default.

Cause: Simply put, Outlook does not start with any Microsoft Dynamics GP specific trusts, so they need to be added.  

Solution: There are two solutions to get this message to stop appearing, we currently recommend the Outlook solution (first one in the list) as it has no side-effects. 
The Microsoft Dynamics GP solution does have side effects which are mentioned in the link provided 

1.	Outlook solution (recommended) –  
a.	Use the following link to solve the issue by telling Outlook that GP is a [trusted program] (https://support.microsoft.com/en-us/help/3189806/a-program-is-trying-tosend-an-e-mail-message-on-your-behalf-warning-i)

Note: This may need to be redone anytime you upgrade GP/Office versions.

2.	Dynamics GP Workaround (Has side-effect of the emailed document containing the file path that it was sent from) – 
a.	[Force Outlook to use a different version of MAPI](https://community.dynamics.com/gp/b/dynamicsgp/archive/2015/08/13/drafta-program-is-trying-to-send-an-e-mail-message-on-your-behalf-when-trying-tosend-a-template-via-e-mail) 
This has many side effects which are mentioned in the above article.

Note: This may need to be redone anytime you upgrade Office 

### Microsoft Dynamics GP Crashes after an Office Update

Note: Only happens past Microsoft Office version 1810, happens to all versions of Microsoft Dynamics GP. 

This ONLY effect emailing functionality. This includes any time where an email address would be entered within GP. Specific to MAPI.

Issue: Office no longer allows for Sideloading of VBA.

Cause: The Microsoft Dynamics GP attempt to use its own packaged version of VBA, and Office no longer allows this.

Solution: The solution is to remove VBA, stay on a version of Office prior to 1810, or to use Exchange rather than MAPI functionality. 

[More information regarding the cause of this issue](https://community.dynamics.com/gp/b/dynamicsgp/posts/dynamics-gp-crashes-closeswhen-emailing-after-office-update)
and [Microsoft’s stance on the solutions] (https://community.dynamics.com/gp/b/dynamicsgp/posts/dynamics-gp-and-vba-futureconsiderations)


## Exchange Specific Errors
Dynamics GP uses Exchange Autodiscover to find the Exchange EWS endpoint, then uses this endpoint to login to, and send emails through, Exchange. 

### Login Failed: check your login information and try again

Note: Note: Error appears when attempting to login to the Exchange Log On screen.

Issue: Something is keeping Microsoft Dynamics GP from being able to successfully connect to the Exchange Server.  

Cause: There are a multitude of possible causes for this issue. The most common issues are an Autodiscover issue, an issue with MFA (Multifactor Authentication), or Basic Authentication being disabled.  

Solution: The following path is the best route for generic login issues: 

1.	Confirm MFA is disabled 
If it is enabled, attempt to use an App Password instead of the account’s normal password 
More information on [App Passwords] (https://support.microsoft.com/en-us/help/12409/microsoft-account-apppasswords-and-two-step-verification)
 
2.	Confirm that Basic Authentication is enabled.  
Most Exchange Administrators can answer this for you, although the [following link outlines other routes to confirm the status of Basic Authentication] (https://community.dynamics.com/gp/b/dynamicsgp/posts/exchange-online-o365emailing-inside-dynamics-gp)
 
3.	Confirm that Autodiscover is working. 
You can do this by removing the user from the SY04920 table (Dynamics/System database) and attempting to login again. If this table does not repopulate, then there are Autodiscover issues in the system (or the user doesn’t work). The [following link outlines how this all works, along with other tests] (https://community.dynamics.com/gp/b/dynamicsgp/posts/exchange-emailinginside-dynamics-gp)


## Generic Errors

### PDF Not Created

Note: Issue Specific to Upgrades to GP 2013 SP1 

Issue:  User is attempting to e-mail the customer statement but is receiving an error that the PDF file was not generated.

Cause: When disabling the customer statements via Tools>>Setup>>Sales>>E-mail settings, it doesn’t update the SY04905 table. 

Solution: Use the steps below to workaround around the error message:

To get around this, the users need to follow these steps to update the customer cards before they disable the Customer Statement:
1.	 Verify that the Customer Statements are enabled to be E-mailed(Tools>>Setup>>Sales>>E-mail Settings)
2.	Go to the Customer Navigation List and select all customers.
3.	Use the E-mail Settings option (top navigation bar) here to update all customers. 
4.	Here you will need to check ‘Customer Statements’ then select ‘PDF’ and uncheck the Customer Statement option:  Then Click OK.
5.	You should see that the customer cards were updated: 
 
6.	Running the following script should show the EmailDocumentEnabled field has been set to 0 for all customers: 

select * from SY04905 where EmailDocumentID = '10'


7.	Disable the Customer Statement option on the E-Mail Settings window in Sales Setup. 
8.	The statements should generate as a PDF file now for all customers.   


### Unknown Error Occurred

Note: Issue usually happens to EFT Remittances in Payables. 

Issue:  User is attempting to e-mail remittances but the error above appears on the Email Exception Report. 

Cause: This error has many causes, usually comes down to customizations on the Template, or odd characters in the email addresses used. 

Solution: Try the following:

Error messages when you email RM Statements in Microsoft Dynamics GP: 
[Unknown Error or Insufficient Memory] (https://community.dynamics.com/gp/b/dynamicsgp/posts/error-messages-when-you-email-rm-statements-in-microsoft-dynamics-gp-unknown-error-or-insufficient-memory)

Use default report and Template and make sure the Template is the one marked with an Asterisk (*).
[If the default works, check the bookmarks on the modified template] (https://community.dynamics.com/gp/b/dynamicsgp/posts/what-are-bookmarks-and-how-are-they-used-in-microsoft-dynamics-gp-s-word-templates) 

Remove all email addresses being used and reenter them. Make sure that there are no odd characters such as ^ or a Tab.
This issue can occur with all reports, and these can be caused by MessageID issues or Reply To issues. Make sure to remove all MessageIDs and Reply To emails. 


 ### No Error, but no emails are sent (0 Documents Sent)

Note: Common issues for RM Statements or EFT Remittances.

Issue:  User is attempting to e-mail documents, but nothing happens. All exception reports will show that no documents were sent. 

Cause: This issue has many different causes, and there are no errors. 

Solution: Try the following:

Test a default report in GP, we recommend the User Report:
1.	Go to Administration >> Reports >> System >> Users
2.	Under Reports: Select User Notes
3.	Click New
4.	Option: Enter TEST
5.	Ranges: Select a User ID
6.	Click Insert
7.	Click Email Options
8.	If using Exchange, it will prompt you for your Exchange Log On
9.	Enter your own email address in the To field 
10.	Click OK
11.	Bring up the TEST report and click Email

If the test email works, you will want to check the modified report in Report Writer:
First, [check the Sections within Report Writer per the following article] (https://blogs.msdn.microsoft.com/developingfordynamicsgp/2013/02/25/copying-report-formats-between-reports-and-a-warning-about-word-templates/)

Check the Font sizes in Report Writer (keep all fonts over size 5).

Review the Template for any issues:

- Missing Bookmarks is the most frequent cause for the e-mails to fail outside of system issues.  

[Verify all bookmarks are present] (https://community.dynamics.com/gp/b/dynamicsgp/posts/what-are-bookmarks-and-how-are-they-used-in-microsoft-dynamics-gp-s-word-templates)

- Text Boxes will cause the template to fail.  

A user should never put a text box inside of a template.  It will cause an error when generating that may not show within GP

- GP 2010 - 32-Bit Office must be used for GP2010 - Uninstall and reinstall >> Click 32 bit install

- GP 2013 or newer 32 or 64-bit Office can be used with GP2013. If using 64 bit the server type in System Preferences (Microsoft Dynamics GP | Tools | System | Setup | System Preferences) must be set to Exchange.

- Special characters in the reply to email address cause the e-mail to fail in Outlook.  If the user is using a reply to address, remove this from both the E-mail Message ID and module e-mail setup.  

Go to Sales >> Cards >> Customer >> E-Mail button and remove the Message ID

Also go to Sales >> Setup >> E-mail Settings Remove the any Reply To email address entered. Enter a new invoice for the customer and test the email. 

- Default e-mail profile not setup
Review the  MAPI Specific issues Above for more information on this.

- If using a terminal server/Citrix environment, Outlook must be open on the server for using MAPI

- Another common issue with e-mail is when users get a new workstation.  They made need to update the Registry when using MAPI.  They can do this by following the steps in the MAPI Specific issues above or in the Word Doc: 



