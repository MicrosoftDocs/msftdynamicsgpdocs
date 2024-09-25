---
title: Dynamics GP Email Troubleshooting Guide
description: Get tips and tricks about some of the errors you may run into when emailing out of Microsoft Dynamics GP.
keywords: "email"
author: theley502
manager: jswymer
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 8/21/2024
---

# Microsoft Dynamics GP Email Troubleshooting Guide

[!INCLUDE [azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

This document is meant to walk through most of the errors you may run into when emailing out of Microsoft Dynamics GP.  

The goal is to make everyone an emailing expert!  

This document can be leveraged to aid in troubleshooting all areas of emailing out of Microsoft Dynamics GP from the legacy Standard Report Writer Statements to Word Templates, Workflow or Modern Authentication.

> [!NOTE]
> Before Microsoft Dynamics GP's October 2020 (18.3 and later) release, Dynamics GP required that both TLS 1.0 and Basic Authentication (no Modern Authentication) be enabled for Exchange and Workflow emailing in Dynamics GP.
>
> After Microsoft Dynamics GP's October 2020 (18.3 or later) release, Dynamics GP has added the functionality to use both  [TLS 1.2](https://community.dynamics.com/blogs/post/?postid=43ed28eb-bddf-4aee-b1ff-b65513d412b1) and/or [[Multi-Factor Authentication](https://community.dynamics.com/blogs/post/?postid=bce65f37-eb08-4531-b62b-32a8af728f58) (MFA).
> You do not actually need MFA turned on for your account to use the Modern Auth window in Microsoft Dynamics GP, but it does use Modern Authentication vs Basic Authentication.
> 
> If you are still on an older version of Microsoft Dynamics GP, you must enable TLS on your local Exchange server. For more information, see [TLS completely disabled in 2022](/exchange/clients-and-mobile-in-exchange-online/opt-in-exchange-online-endpoint-for-legacy-tls-using-smtp-auth).
>
> When Basic Authentication is deprecated (October 1, 2022), you will need to be on a version of Dynamics GP where you can use Modern Authentication (18.3 or later). There have been many quality issues fixed with Dynamics GP and Multi-Factor Authentication, so it is recommended to be on 18.5.1635 or later.

Review the below blogs for workarounds if you are on an older version of Microsoft Dyanmics GP:

[**WORKFLOW emails intermittently fail**](https://community.dynamics.com/blogs/post/?postid=7aaa9918-06a0-4e88-adac-fc30853b97dc)

[**Other emails intermittently fail**](https://community.dynamics.com/blogs/post/?postid=91c7ad35-9529-423a-859d-1f9db094f1f7)


All email issues can be safely split up into the following set of categories:

* [Issues unique to MAPI](#mapispecificerrors) 
* [Issues unique to Exchange](#exchangespecificerrors)
* [Workflow](#workflow)
* [Issues unique to MFA-Multi-Factor Authentication](#mfa) 

To determine whether MAPI or Exchange is being used check the System Preference window. (Administration >> Setup >> System >> System Preferences)

> [!IMPORTANT]
> This setting is stored in the DYNAMICS database and is system-wide, so changing this setting will affect all users.  

![Form](media/syspref.jpg)

## <a name=mapispecificerrors></a>MAPI Specific Errors
Dynamics GP uses MAPI to open Outlook to send emails directly from the Outlook client.

> [!IMPORTANT]
> MAPI only works with 32-bit Outlook Client installed.  The newOutlook operates based on the principles of the Outlook Web version.
>
> Not all features are currently supported, and the installation of the 32-bit version is not supported on the newOutlook, due to the transition from Classic Outlook.
>
> It is highly recommended to implement Modern Auth (MFA) instead of MAPI when at all possible with Dynamics GP.


### Emails Stuck in Outbox within Outlook. 

**Note** Issue appears to be unique to Gmail accounts.  

**Issue** Emails are getting stuck in the Outbox in Outlook. 
When you use the Send/Receive button, or close/reopen Outlook, the email sends without delays.  

**Cause**
Add-in for Gmail Multi-factor authentication. This is a paid add-in that we believe causes the issue.  

**Solution**
Compare a clean Outlook add-in list to the client having the issue to make sure there are no extra add-ins.  
Recommend that they [remove the add-in as it appears like it is no longer needed](https://support.microsoft.com/en-us/office/add-a-gmail-account-to-outlook-70191667-9c52-4581-990e-e30318c2c081)
### No default mail client, or the current mail client cannot fulfill the message request Please run Microsoft Outlook and set it as the default mail client.  

**Note** Recommend you review Outlook version first – MAPI only works with 32bit!  

**Issue** Error appears when attempting to email using MAPI anywhere in GP Cause: Either a Profile is not setup, or Outlook cannot reach it using MAPI.  

**Solution**
You can go through [this KB](https://support.microsoft.com/help/4052892/e-mail-error-in-microsoftdynamics-gp-either-there-is-no-default-mail), focus on A and B as these are common causes.  

You will want to make sure that Outlook is also set up as the default application for mail when you search for Default Apps in Windows 10.  

### A program is trying to send an e-mail message on your behalf

**Note** Happens a lot with more secure environments and newer versions of Office.

**Issue** Outlook does not trust Microsoft Dynamics GP by default.

**Cause** Simply put, Outlook does not start with any Microsoft Dynamics GP specific trusts, so they need to be added.  

**Solution**
There are two solutions to get this message to stop appearing, we currently recommend the Outlook solution (first one in the list) as it has no side-effects.  
The Microsoft Dynamics GP solution does have side effects which are mentioned in the link provided  

1. Outlook solution (recommended)  

      1. Use the following link to solve the issue by telling Outlook that GP is a [trusted program](https://support.microsoft.com/help/3189806/a-program-is-trying-tosend-an-e-mail-message-on-your-behalf-warning-i)  

          Note: This may need to be redone anytime you upgrade GP/Office versions.

2. Dynamics GP Workaround (Has side-effect of the emailed document containing the file path that it was sent from)  

    1. [Force Outlook to use a different version of MAPI](/troubleshoot/dynamics/gp/a-program-is-trying-to-send-an-e-mail-program-on-your-behalf)
    
        This has many side effects which are mentioned in the above article.

Note: This may need to be redone anytime you upgrade Office  

### Microsoft Dynamics GP Crashes after an Office Update

**Note** Only happens past Microsoft Office version 1810, happens to all versions of Microsoft Dynamics GP. 

This ONLY effect emailing functionality. This includes any time where an email address would be entered within GP. Specific to MAPI.

**Issue** Office no longer allows for sideloading of VBA.

**Cause** Microsoft Dynamics GP attempts to use its own packaged version of VBA, and Office no longer allows this.

**Solution**
The solution is to remove VBA, stay on a version of Office prior to 1810, or to use Exchange rather than MAPI functionality. 

For more information regarding the cause of this issue, see the following blog posts:

- [Dynamics GP crashes closes when emailing after Office update](https://community.dynamics.com/blogs/post/?postid=ea4193b7-f9ac-4ece-85db-377b0515cdd0)  
- [Microsoft’s stance on the solutions](https://community.dynamics.com/blogs/post/?postid=a89717ca-bbd4-4473-b9f6-ba6662c32a80)

## <a name=exchangespecificerrors></a>Exchange Specific Errors

Dynamics GP uses Exchange Autodiscover to find the Exchange EWS endpoint, then uses this endpoint to login to, and send emails through, Exchange.  

### Login Failed: check your login information and try again

Note: Note: Error appears when attempting to login to the Exchange Log On screen.

Issue: Something is keeping Microsoft Dynamics GP from being able to successfully connect to the Exchange Server.  

Cause: There are a multitude of possible causes for this issue. The most common issues are an Autodiscover issue, an issue with MFA (Multifactor Authentication), or Basic Authentication being disabled.  

**Solution**
The following path is the best route for generic login issues: 

1. Confirm MFA is disabled  

    If it is enabled, attempt to use an App Password instead of the account’s normal password. For more information, see [App Passwords](https://support.microsoft.com/help/12409/microsoft-account-apppasswords-and-two-step-verification)  

2. Confirm that Basic Authentication is enabled  

    Most Exchange Administrators can answer this for you, although the [this blog post outlines other routes to confirm the status of Basic Authentication](https://community.dynamics.com/gp/b/dynamicsgp/posts/exchange-online-o365-emailing-inside-dynamics-gp)  

3. Confirm that Autodiscover is working  

    You can do this by removing the user from the SY04920 table (Dynamics/System database) and attempting to login again. If this table does not repopulate, then there are Autodiscover issues in the system (or the user doesn’t work). For insights into how this all works, along with other tests, see [this blog post](https://community.dynamics.com/blogs/post/?postid=d0838b3e-8943-42a3-9d46-3004f02aa9b8)  

>[!NOTE]
> With *Login Failed* type of error messages, we have seen some cases where TLS 1.0 was disabled, due to the looming end date and vulnerabilities. If you are still on an older version of Microsoft Dyanmics GP, you must enable TLS on your local Exchange server. For more information, see [TLS completely disabled in 2022](/exchange/clients-and-mobile-in-exchange-online/opt-in-exchange-online-endpoint-for-legacy-tls-using-smtp-auth).


## Generic Errors

### PDF Not Created

Note: Issue Specific to Upgrades to GP 2013 SP1  

Issue:  User is attempting to e-mail the customer statement but is receiving an error that the PDF file was not generated.

Cause: When disabling the customer statements via Tools>>Setup>>Sales>>E-mail settings, it doesn’t update the SY04905 table. 

**Solution**
Use the steps below to workaround around the error message:

To get around this, the users need to follow these steps to update the customer cards before they disable the Customer Statement:
1.	Verify that the Customer Statements are enabled to be emailed (Tools >> Setup >> Sales >> E-mail Settings)
2.	Go to the Customer Navigation List and select all customers.
3.	Use the E-mail Settings option (top navigation bar) here to update all customers.
4.	Here you will need to check Customer Statements, then select PDF, and uncheck the Customer Statement option. Then click OK.
5.	You should see that the customer cards were updated
6.	Running the following script should show the EmailDocumentEnabled field has been set to 0 for all customers:
SELECT * FROM SY04905 WHERE EmailDocumentID = '10'
7.	Disable the Customer Statement option on the E-Mail Settings window in Sales Setup.
8.	The statements should generate as a PDF file now for all customers.  

Missing Records in either the SY04904 and/or SY04905 table can also generate this issue:
```sql
SELECT * FROM RM00101 WHERE CUSTNMBR not in (SELECT EmailCardID FROM SY04904)
SELECT * FROM RM00101 WHERE CUSTNMBR not in (SELECT EmailCardID FROM SY04905)
```

### Unknown Error Occurred

Note: Issue usually happens to EFT Remittances in Payables or Statements in Receivables.  

Issue:  User is attempting to e-mail remittances and/or statements but the error above appears on the Email Exception Report.  

Cause: This error has many causes, usually comes down to customizations on the Template, or odd characters in the email addresses used.  

**Solution**
Try the following:

Error messages when you email RM Statements in Microsoft Dynamics GP: [Unknown Error or Insufficient Memory](https://community.dynamics.com/blogs/post/?postid=10780b81-2921-4d91-8f7b-cf763112d4f3#:~:text=This%20is%20a%20known%20issue,June%202022%20update%20%5BGP%2018.4.)

Use default report and Template and make sure the Template is the one marked with an asterisk (`*`).
If default emails, review modified template for [bookmarks](https://community.dynamics.com/gp/b/dynamicsgp/posts/what-are-bookmarks-and-how-are-they-used-in-microsoft-dynamics-gp-s-word-templates) hyperlinks, anchors, and even the size of the document example. RM Statement to show line item detail for all invoices would a very large statement for some customers.

**Set Template to Default Original/Canned Report.**
1. Microsoft Dynamics GP menu >> Tools >> Setup >> System >> User Security
2. Select the username and company.
3. Click on the 'Alternate/Modified Forms and Reports ID:' link at the bottom of the window.
4. In the Alternate/Modified Forms and Reports window select the following:
      Product: Microsoft Dynamics GP
      Type: Reports
      Series: All
5. Click the plus button to expand the module folder. i.e., Purchasing
6. Click the plus button to expand the report. i.e., Check Remittance
(If the report is not on the list at all then you do not have a modified option, please move to step 10.)
7. Select the default/canned 'Microsoft Dynamics GP' option. (Do NOT select modified here)
8. Click Save, Save, and Close.
9. Go to Reports >> Template Maintenance
10. In the Report Template Maintenance window, click the bar at the top that says, 'Click here to select a report'.
11. Select the option for 'More Reports' on the Drop-Down list.
      Product: Microsoft Dynamics GP
      Series: Purchasing
      Status: Original
12. Select '*Check Remittance' from the list and Click 'Select'.
13. In the Report Template Maintenance window, highlight 'Check Remittance*'
14. Click on the Assign >> Company button on the menu bar.
15. Check the company that you are testing the process in.
16. Highlight a company and click 'Set Default'.
17. Check the box next to 'Check Remittance*'
18. Click Save, Save, and Close

**Remove Have Replies Sent to on both the Message ID and E-mail setup.**
The Message Setup window can be found using the either pathing:
System wide
Administration >> Setup >> Company >> E-mail Message Setup
Administration >> Setup >> Company >> Workflow >> E-mail Message Setup

Module specific
Sales >> Setup >> E-mail Settings
Purchasing >> Setup E-mail Settings

Remove and re-enter all associated email addresses. Make sure that there are no odd characters such as ^ or a Tab.
Email Addresses can be found using either pathing:
Administration >> Setup >> Company >> Internet Information

**NOTE**
If **Email Addresss based on Doc Type** is enabled:
(Sales >> Cards >> Customer >> select a customer >> E-mail >> enable email address based on document type >> Email Address)
(Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> enable email address based on document type >> Email Address)
This issue can occur with all reports, and these can be caused by MessageID issues or Reply To issues. Make sure to remove all MessageIDs and Reply To emails.  

> [!NOTE]
> **Items to Rule out and test with Unknown error occurred and Modern Auth**
> 
> 1. If you are using Modern Authentication (MFA) in Dynamics GP and receive this error message when you enter the APP ID in the Modern Auth setup window this could be related to a TLS registry issue.  
> [How to change the TLS registry](/mem/configmgr/core/plan-design/security/enable-tls-1-2-client)
>
> 2. Verify this error **Unknown Error Occurred** is happening for all users that are trying to send emails.  If this error only happens for example on two users, and you are using RDS Server, we have seen where deleting the User Profile on the RDS server and recreating it has fixed this error message and issue for those couple of users.
>
> 3. If you are trying to sign in with Modern Auth over Citrix and use the Citrix Workspace App, please review the information below specific for Citrix
[Authenticate | Citrix Workspace app for Windows](https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/authentication.html)
>
> 4. Can you email (test) from the SQL Server does it work? Compared to the RDS server machine to rule out settings/setup.  How does a Fiddler trace compare between a working and non-working machine?
> 
>  5. Modern Auth requires .NET Framework 4.7.2 or later to be installed on each machine/server.  If one machine is failing, [verify if that version is installed](/dotnet/framework/migration-guide/how-to-determine-which-versions-are-installed).
>  
>  6. Antivirus/Malware could also cause the problem to not authenticate, try to rule it out as the cause of the problem.
>  
>  7. Dynamics GP supports [Multi-tenant authentication](https://community.dynamics.com/blogs/post/?postid=bce65f37-eb08-4531-b62b-32a8af728f58) in the Microsoft Entra app Registration. If you set this up incorrectly, you'll see the message *Unknown Error*. [Single Tenant App Registration supported with 18.6 release](https://community.dynamics.com/blogs/post/?postid=18194a5d-4b7f-ee11-a81c-6045bdbe566c).
>        
>  8. If the Application ID is not saving or has issues, test by launching GP as Administrator, right-click your GP icon and choose Run as Administrator.
>  
>  9. Rule out [3rd party authentication providers](/dynamics-gp/installation/email-troubleshooting-guide#dynamics-gp-modern-authentication-and-third-party-authentication)

* If you still have issues, you may want to create a Fiddler trace that will be more specific of the problem.

You can run a Fiddler trace, and that will tell us if basic auth is not enabled or a DNS issue may appear, for example. It can also inform us about other problems in your environment.

#### To run Fiddler

1. [Download Classic Fiddler](https://www.telerik.com/download/fiddler)  
2. Open Fiddler.  
3. In Tools->Fiddler Options->HTTPS, choose the **Decrypt HTTPS traffic** field.  
4. Choose **Yes** on the prompt for trust Fiddler Root Certificate.  
5. Choose **Yes** to install the certificate.  
6. Choose **Yes** to confirm.  
7. Choose **OK**, and then choose **OK** to go back.  
8. Reproduce the issue.  
9. Stop the Fiddler trace:   
      1. File->Capture Traffic F12, Save trace: File->Save>All Sessions.   
      2. Save the trace out as .saz file.  

For more information, see [this blog post](https://blogs.msdn.microsoft.com/maheshk/2016/05/03/easy-way-to-collect-fiddler-log-fiddlercap/).  


### Insufficient Memory
**Solution**

1. Remove Have Replies Sent to on both the Message ID and E-mail setup. The Message Setup window can be found using the either pathing:
System wide Administration >> Setup >> Company >> E-mail Message Setup Administration >> Setup >> Company >> Workflow >> E-mail Message Setup
Module specific Sales >> Setup >> E-mail Settings Purchasing >> Setup E-mail Settings
2. Remove and re-enter all associated email addresses. Make sure that there are no odd characters such as ^ or a Tab. Email Addresses can be found using either pathing: Administration >> Setup >> Company >> Internet Information
**NOTE** If Email Addresses based on Doc Type is enabled: (Sales >> Cards >> Customer >> select a customer >> E-mail >> enable email address based on document type >> Email Address) (Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> enable email address based on document type >> Email Address) This issue can occur with all reports, and these can be caused by MessageID issues or Reply To issues. Make sure to remove all MessageIDs and Reply To emails.  

The following SQL can be used to view the listed Have Replies Sent To email address.

  ```sql
  SELECT EmailReplyToAddress, * FROM SY04901 WHERE EmailSeriesID = 3 and EmailDocumentID in (10,15)
  SELECT EmailReplyToAddress, * FROM SY04902 WHERE EmailSeriesID = 3
  ```

EmailSeriesID =

2 – Financial  
3 – Sales  
4 – Purchasing  
5 – Inventory  
6 – Payroll  
7 – Project  
10 – 3rd Party  
99 – All  

EmailDocumentID – This is a unique integer indicating each type of document displayed in the window


### Invalid Recipients

Invalid Recipients
This error can be cause by multiple things. Check the following:
Make sure that there is a valid email address entered on the customer/vendor 
Microsoft Dynamics GP will determine what email will be used when emailing differently depending on whether the Email Address based on Doc Type setting is enabled or not. This is found in the following path:
Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> enable email address based on document type 

Sales >> Cards >> Customer >> select a customer >> E-mail >> enable email address based on document type 

If Email Address based on Doc Type is disabled:
When this feature is disabled, Microsoft Dynamics GP determines the email address based on what is listed in the Internet Information widow for the Address ID on the Customer or Vendor card.
The Internet Information window can be found using either of the following paths:
Administration >> Setup >> Company >> Internet Information >> select vendor/customer >> select address ID
Purchasing >> Cards>> Vendor >> click Internet Information button next to the Address lookup (looks like a little planet earth). 
Sales >> Cards>> Customer >> click Internet Information button next to the Address lookup (looks like a little planet earth). 

If Email Address based on Doc Type is enabled:
When this feature is enabled, Microsoft Dynamics GP determines the email address based on what is listed in the Email Address Based on Doc Type window for the vendor/customer.
The Email Address Based on Doc Type window can be found using either of the following paths:
 
Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> enable email address based on document type >> Email Address

Sales >> Cards >> Customer >> select a customer >> E-mail >> enable email address based on document type >> Email Address

### No Error, but no emails are sent (0 Documents Sent)

No Error, but no emails are sent (0 Documents Sent)<
Note: Common issues for RM Statements or EFT Remittances.  

Issue:  User is attempting to e-mail documents, but nothing happens. All exception reports will show that no documents were sent.  

Cause: This issue has many different causes, and there are no errors.  

Solution: As there are many potentials causes it would be best to start with determining whether the original/canned report will email. 
Set Template to Default Original/Canned Report.
1.	Microsoft Dynamics GP menu >> Tools >> Setup >> System >> User Security
2.	Select the username and company.
3.	Click on the 'Alternate/Modified Forms and Reports ID:' link at the bottom of the window.
4.	In the Alternate/Modified Forms and Reports window select the following: Product: Microsoft Dynamics GP Type: Reports Series: All
5.	Click the plus button to expand the module folder. i.e., Purchasing
6.	Click the plus button to expand the report. i.e., Check Remittance (If the report is not on the list at all then you do not have a modified option, please move to step 10.)
7.	Select the default/canned 'Microsoft Dynamics GP' option. (Do NOT select modified here)
8.	Click Save, Save, and Close.
9.	Go to Reports >> Template Maintenance
10.	In the Report Template Maintenance window, click the bar at the top that says, 'Click here to select a report'.
11.	Select the option for 'More Reports' on the Drop-Down list. Product: Microsoft Dynamics GP Series: Purchasing Status: Original
12.	Select '*Check Remittance' from the list and Click 'Select'.
13.	In the Report Template Maintenance window, highlight 'Check Remittance*'
14.	Click on the Assign >> Company button on the menu bar.
15.	Check the company that you are testing the process in.
16.	Highlight a company and click 'Set Default'.
17.	Check the box next to 'Check Remittance*'
18.	Click Save, Save, and Close

If the default email sends out successfully, then we can deduce that the issue lies within the modification to either the RW report or directly on the template. The following are possible modifications that have caused this issue:
* Check Section Options in RW for the modified report and make sure they mimic what is setup in our default report. Further details on this can be found in the problem section of [this blog](https://blogs.msdn.microsoft.com/developingfordynamicsgp/2013/02/25/copying-report-formats-between-reports-and-a-warning-about-word-templates/)
* Check the Font sizes in RW (keep all fonts over size 5).
* Missing Bookmarks [Verify all bookmarks are present](https://community.dynamics.com/blogs/post/?postid=ca4e2050-fb97-42c0-93d8-1481374ec473)
* Text Boxes will cause the template to fail; text boxes should not be used as it can cause an error that is not seen within Microsoft Dynamics GP.
* Remove Have Replies Sent to on both the Message ID and E-mail setup. The Message Setup window can be found using either path: 

### Body of email missing when emailing to customer or vendor

Below are some items to check of why this may happen:

1. In the Message ID, delete any unnecessary blank lines prior to the greeting line in the email body or other areas.
1. Create and test emailing with a new Message ID by using just the word TEST in the Subject. In the body, make three lines labeled as line1, line2, line 3. Don't copy from an existing email.  

   When testing make sure you test with a new document. 

   **Existing documents will still pull the old message body and subject that is saved within the tables so they are not a valid test.**

1. Does the MessageID look valid for other document types emailed from GP or is it specific to this document type?
1. Do you have any third party products that are installed for this company that may come into play with e-mail?  It's good to test without 3rd parties installed.
1. It's advisable to use the **New Outlook client** as it appears to manage message formatting more effectively.
1. Does the email have a signature or disclaimer added to the bottom of it?  
   1. Verify this in the INBOX of the user who received the email from Dynamics GP. 
   1. Verify this on the from SENT folder of the user who emailed to document out of Dynamics GP.
   1. It's normal to see the signature/disclaimer on the receiving INBOX, but not in the SENT mailbox. 

   If there's a disclaimer or signature that appears on the received email, obtain confirmation from your IT group whether they have any add-ons for Exchange Online or Email handling related to signatures or disclaimers. Keep in mind you will usually see no signature on the SENT folder of the user sending the email. You will only see it on the user who received it.  
 
   Microsoft Dynamics GP will function properly with the default Exchange Online organization-wide signatures and disclaimers setup, which is Text only.  Please see the [limitations posted by Exchange Online](/microsoft-365/admin/setup/create-signatures-and-disclaimers?view=o365-worldwide#limitations-of-organization-wide-signatures) for their default organization wide signatures.

   If you have third party add-ons in Exchange Online to add logos or do any formatting to these signatures/disclaimers, it can break Microsoft Dynamics GP's formatting on emails. Test again with the add-ons disabled. If this test works, then you can add an exception to exclude emails from Microsoft Dynamics GP. Or, you can contact your third party to see if there's any way for the add-on to function without changing the email's formatting, as this is out of Microsoft Dynamics GP's control.   
   
1. How does the message id look like in the SY04915 table if you execute the following Query to Text? Do the results show the line breaks?

   select EmailBody from SY04915 where DOCNUMBR = 'DOCNUMBR '

   Replace the DOCNUMBR field with the remittance payment number. 

   If the SQL Query displays the data with the proper format in this table when executing to Text, then that tells us that GP is storing it properly in the tables and issue is not related to Dynamics GP.

### System wide 
* Administration >> Setup >> Company >> E-mail Message Setup
* Administration >> Setup >> Company >> Workflow >> E-mail Message Setup

### Module specific
* Purchasing >> Setup >> E-mail Settings Purchasing >> Setup E-mail Settings
* Sales >> Setup >> E-mail Settings >> Setup E-mail Settings
* Default e-mail profile not setup as required, for more information on this you can review this [E-mail error in Microsoft Dynamics GP: "Either there is no default mail client or the current mail client cannot fulfill the message request. Please run Microsoft Outlook and set it as the default mail client."](https://support.microsoft.com/en-us/topic/e-mail-error-in-microsoft-dynamics-gp-either-there-is-no-default-mail-client-or-the-current-mail-client-cannot-fulfill-the-message-request-please-run-microsoft-outlook-and-set-it-as-the-default-mail-client-ade64dfb-58c4-26f6-7584-38db2310d0f0) Knowledge article.
* If using either a Terminal Server or Citrix environment, Outlook must be open on the server if using the MAPI Server Type in System Preferences.
* If using GP 2010, only 32-bit Office can be used.
* If using GP 2013 or later, either 32 or 64-bit Office can be used. If using 32-bit Office either MAPI or Exchange can be used as the Server Type, however if using 64-bit Office the Server Type must be set to Exchange. 
(Microsoft Dynamics GP >> Tools >> System >> Setup >> System Preferences 
You can obtain further information on email requirements in this [System requirements - Dynamics GP | Microsoft Docs](/dynamics-gp/upgrade/system-requirements) section of our doc site.

If the default does not email, then test a default report in GP to verify whether the basic email functionality is working, we generally recommend the User Report:
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

> [!NOTE]
> **Items to Rule out and test with EFT Check Remittance**
> 
>There are several items to check when EFT Check Remittance does not email.  In each of these cases the cause could be different.  Please review the [complete list of why the EFT Check Remittance emails are not sending out](https://community.dynamics.com/blogs/post/?postid=5acf230c-9fcd-4f9f-99ca-f88d2718c151).
      
### Send Documents in email check box is grayed out when trying to send a Remittance

Send Documents in email check box is grayed out when trying to send a Remittance

Note: Common issues for PM EFT Remittances

Issue: User is attempting to email Remittances, but the checkbox is grayed out:

![Form 1](media/email1.jpg)

Cause: This issue has a few different causes, usually setup or 3rd party involvement Solution: 

Try the following:
1. Check to see if the vendor is setup to allow for emailing:
Go to Purchasing >> Cards >> Vendor >> select a vendor >> E-mail.
In the Send Forms as Email section confirm that Vendor Remittance check box is checked.


![Form 2](media/email2.jpg)

If this is correct, check to see if Mekorma MICR is installed, if so make sure the Mekorma MICR System Options are set to have email enabled, or else the **Send Document in email** checkbox in the Remittance window will not be available to mark (or grayed out). To check this setting, go to Microsoft Dynamics GP | Tools | Setup | System | Mekorma MICR | System Options. Choose the **Enable Email Remittance** field, and then click Save.

[For more information, see this blog post about this process](https://community.dynamics.com/gp/b/dynamicsgp/archive/2016/10/24/quick-step-guide-to-e-mail-pm-eft-remittances-in-mdgp-2015-2016)


### Email button is grayed out in Sales Order Processing

Note: Unique to Sales Order Processing

Issue: User is attempting to from a Sales Order Processing window, but the option to email is grayed out.

Cause: GP will only email the Blank Paper options for reports.

Solution: Try the following:
1. Go to: Sales >> Setup >> Sales Order Processing >> Sales Document Setup button >> select the
2. Document Type they are trying to send (quote, order, invoice etc)
3. Make sure the Format is set to Blank Paper

![Form 3](media/email3.jpg)

### You must activate e-mail functionality for this document before it can be sent in email

Note: Companywide setup issue

Issue: User is attempting to email out a document that is not allowed in the company Cause: GP will only allow emailing on documents you tell it to.

Solution: Try the following:

Verify that the document type that is expected to be emailed is selected in the Vendor and/or Customer E-mail Options window(s)

Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> Send Forms as E-mail section >> Format drop down column
Tools >> Setup >> Purchasing >> E-mail Settings

Sales >> Cards >> Customer >> select a customer >> E-mail >> Send Forms as E-mail section >> Format drop down column
Tools >> Setup >> Sales >> E-mail Settings


###  The company does not allow the sending of (DOCX, HTML, PDF, XPS) files

Note: Companywide setup issue

Issue: User is attempting to email out a document type that is not allowed in the company Cause: GP will only allow emailing on document types you tell it to.
Solution

Solution: 
Verify that the document type that is expected to be emailed has a check mark in the File Formats Allowed option on the Company E-mail Setup window.
Tools >> Setup >> Company >> E-mail Settings >> place a check mark next to the desired format.

![Form 4](media/email4.jpg)


###  A word template must be assigned before sending this document

Note: Companywide setup issue, usually happens to new Template users. 

Issue: User is attempting to email out a modified report that has no corresponding template.

Cause: There is no template assigned to email

Solution

Solution: Try one the following:

1.	Use the Standard report in the Alternate/Modified Forms and Reports setup window Tools -> setup -> System -> Alternate/Modified Forms and Reports
2.	Create a modified template using the New button on the Template Maintenance window
3.	Reports -> Template Maintenance

Don’t forget to assign the template for either option by using the Assign button on the Template Maintenance window (Reports -> Template Maintenance)


###  Dynamics GP shows Templates Processing, but they never complete or an error appears

Note: There is a template setup, but none are assigned to the company

Issue: User is attempting to email out a report that has no assigned template, but one exists

Cause: There is a template setup, but none are assigned to the company

Solution

To resolve this simply assign a template for the report by using the Assign button on the Template Maintenance window (Reports -> Template Maintenance)
Also check to make sure that that Dexterity Shared Components is installed at a version that matches your version of Microsoft Dynamics GP.

###  This document type cannot be sent in e-mail for this customer/vendor

Note: Common for newly entered customers/vendors, or those that have been imported. 

Issue: User is attempting to email out a document type that has not been enabled for the customer/vendor

Cause: Setup issue on the Customer/Vendor card
Solution

Verify that the document being emailed has a check mark in the Send Forms as E-mail on the Vendor and/or Customer E-mail Options window(s). 
* Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> Send Forms as E-mail section
* Sales >> Cards >> Customer >> select a customer >> E-mail >> Send Forms as E-mail section
Each document you are attempting to email must have a check mark. If these are grayed out, then review the Purchase and/or Sales E-mail Setup window(s).
* Sales >> Setup >> E-mail Settings
* Purchasing >> Setup >> E-mail Settings

### Document type cannot be sent.

Solution

Verify that the document being emailed has a check mark in the Send Forms as E-mail on the Vendor and/or Customer E-mail Options window(s). 
* Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> Send Forms as E-mail section
* Sales >> Cards >> Customer >> select a customer >> E-mail >> Send Forms as E-mail section

Each document you are attempting to email must have a check mark. If these are grayed out, then review the Purchase and/or Sales E-mail Setup window(s).
* Sales >> Setup >> E-mail Settings
* Purchasing >> Setup >> E-mail Settings

A lot of times we see the table data gets flagged incorrectly between the two methods. If this happens, you should review the two tables below and make sure the EmailDocumentEnabled and EmailDocumentFormat columns are flagged correctly. 

SELECT EmailDocumentEnabled, * FROM SY04903
WHERE EmailSeriesID = 3 and EmailDocumentID = 10

SELECT EmailDocumentEnabled, EmailDocumentFormat, * FROM SY04905
WHERE EmailSeriesID = 3 and EmailDocumentID = 10

If using **Word template**, the fields should be set like below: 
EmailDocumentEnabled = 1
EmailDocumentFormat = 
1-DOCX
2-HTML
3-PDF
4-XPS

_The EmailDocumentFormat field will be set to either 1,2,3 or 4 depending on what document format you have selected for the customer in the Customer Email Options window._

EmailSeriesID =
2 – Financial
3 – Sales
4 – Purchasing
5 – Inventory
6 – Payroll
7 – Project
10 – 3rd Party
99 – All

EmailDocumentID – This is a unique integer indicating each type of document displayed in the window

If using **Adobe Writer**, the fields should be set:
EmailDocumentEnabled = 0
EmailDocumentFormat = 0

###  A To, CC, or Bcc address could not be found

Note: Common for newly entered customers/vendors, or those that have been imported. 

Issue: User is attempting to email out for a customer/vendor that does not have an email address.

Cause: Setup issue on the Customer/Vendor card

Solution

**Make sure that there is a valid email address listed on the vendor/customer.**

Microsoft Dynamics GP will determine what email will be used when emailing differently depending on whether the Email Address based on Doc Type setting is enabled or not. This is found in the following path:
* Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> enable email address based on document type
* Sales >> Cards >> Customer >> select a customer >> E-mail >> enable email address based on document type 

![Form 5](media/email5.jpg)

If **Email Address based on Doc Type** is **disabled**:
When this feature is disabled, Microsoft Dynamics GP determines the email address based on what is listed in the Internet Information widow for the Address ID on the Customer or Vendor card.
The Internet Information window can be found using either of the following paths:
- Administration >> Setup >> Company >> Internet Information >> select vendor/customer >> select address ID
- Purchasing >> Cards>> Vendor >> click Internet Information button next to the Address lookup (looks like a little planet earth). 
- Sales >> Cards>> Customer >> click Internet Information button next to the Address lookup (looks like a little planet earth). 

If **Email Address based on Doc Type** is **enabled**:
When this feature is enabled, Microsoft Dynamics GP determines the email address based on what is listed in the Email Address Based on Doc Type window for the vendor/customer.
The Email Address Based on Doc Type window can be found using either of the following paths:
- Purchasing >> Cards >> Vendor >> select a vendor >> E-mail >> enable email address based on document type >> Email Address
- Sales >> Cards >> Customer >> select a customer >> E-mail >> enable email address based on document type >> Email Address

For further information on the Email Address based on Doc Type feature, check out [blog](https://community.dynamics.com/blogs/post/?postid=f3603488-0ed1-4e86-8722-332f9199361c)


###  You must have the Microsoft Save as PDF or XPS add-in for 2007 Microsoft Office

Note: Either caused by an item in the KB below or is a performance problem.

Issue: User is attempting to send out a large set of emails

Cause: Performance problem

Solution
[This KB article can sometimes resolve the issue](https://support.microsoft.com/topic/you-must-have-the-microsoft-save-as-pdf-or-xps-add-in-for-2007-microsoft-office-0d9311d8-265e-1cc0-5df2-a5df3297db24)

The more consistent solution is to simply cut down on the number of emails you are sending out at once. 

For example, run your Invoices for one half of your customers, then the other half.

In rare cases the issue is caused by a conflict with a third party add-in. The easiest way to confirm if this may be the case is to rename the GP code folder and then run a repair of GP. This will recreate a new GP code folder without third parties. If the issue continues you can just delete the new folder and rename the old folder back. If the issue is resolved then you can add third parties one-by-one until the issue reoccurs.

### Emails not showing in Sent Folder (successfully sent)

**Solution**

Delete the old .OST file and let Outlook recreate it.

- Set the Sync Slider in Outlook to download all the data from the mailbox to the data file.  
- Switched between Online mode and then back to Cached mode.  
- Disabled Download shared folders.

[Repair Outlook Data Files (.pst and .ost)](https://support.microsoft.com/en-us/office/repair-outlook-data-files-pst-and-ost-25663bc3-11ec-4412-86c4-60458afc5253)
[Create an Outlook Data File (.pst) to save your information](https://support.microsoft.com/en-us/office/create-an-outlook-data-file-pst-to-save-your-information-17a13ca2-df52-48e8-b933-4c84c2aabe7c)

### E-mail attachment contains file path name vs. document information.
Solution

If e-mail contains a 'path name'

The current only cause we’ve encountered for this is the Dynamics GP Workaround solution provided for [A program is trying to send an e-mail message on your behalf.](/dynamics-gp/installation/email-troubleshooting-guide#a-program-is-trying-to-send-an-e-mail-message-on-your-behalf) 
1)	Open a Windows Explorer window on the Dynamics GP PC and go to C:\Windows. 
2)	Open the WIN.ini file found in this folder. 
3)	Look for the MAPIX setting in the file under the [Mail] section of the file 
a)	Try Leaving this blank under [Mail], making sure that there is nothing under the [Mail] section not even the MAPIX (see attachment below). 
b)	Close Dynamics GP and Outlook then relaunch them prior to re-testing. 


### Unable to email from the Navigation list.
Solution
Try turning off Business Analyzer. Also try marking the **Exclude Historic Transactions** restriction on the navigation list you are emailing from.

### Shared Mailbox for email

As far as what address the email is sent from in Dynamics GP for Templates, there isn’t a field within Dynamics GP that can be changed. 

GP determines who the email will be sent from depending on the Server Type selected in setup (Tools>>Setup>>System>>System Preferences). 

With MAPI, Dynamics GP will use Outlook on the client’s machine to send the email. 
Therefore whatever email account 'on the computer itself' is set up as default in (Control Panel>>Mail – Email Accounts) will be the email address 
that the email is sent from. 
(In this window, BOTH the E-mail tab and the Data Files tab must be the desired email address) 

With MAPI you could set up a general account such as payables@xyz.com and set that as the default profile on the computer, and Dynamics GP will 
use this to send out the emails. Keep in mind that MAPI is designed for 32-bit Office. 

With Exchange, Dynamics GP actually contacts the Exchange server and does it’s emailing through it.  It does not look to your default mail profile in Outlook. For Exchange when the user tries to send an email in Dynamics GP, they are prompted to log in to Exchange. 

Whatever credentials you log in with, are going to determine what email address is sending the documents. 

With modern authentication, changes were made in 18.6 to allow [Shared Mailbox with MFA](https://community.dynamics.com/blogs/post/?postid=50cc4ae5-d25e-ee11-a81c-00224852432e).  


## <a name=workflow></a>Workflow

Workflow email issues usually fall into two possible causes: SMTP issues and Setup issues, overall you can figure out which is which by using the ‘Test E-mail’ button on the Workflow Setup window (GP -> Tools -> Setup -> System -> Workflow Setup). The following steps are split depending on if the test email is received or not.

### My SMTP Test Failed

If you never received the Test E-mail, then you are likely having an issue with SMTP.

(Doing a test email vs actual workflow email are 2 different processes and thus 1 may work where the other does not)

First, confirm that you are not using MFA on the account used in the SMTP setup.

Next, make sure that TLS 1.0 is enabled on the SQL server and on the SMTP server.

Then walk through the following article:

[Workflow Notification Email Troubleshooting](https://community.dynamics.com/blogs/post/?postid=aa22fada-1bda-4f29-ab7b-1d7be6355e22)


### My SMTP Test Passed

If you received the test email, then you are now looking at an issue with Active Directory or Message IDs.

First, make sure your SQL Server Service account is setup as a domain account in the same Active Directory as your Approvers (Two-way-trust domains also work). 
This account will need permission to query the domain holding the Approvers.

Next, try changing your Message IDs on the Workflow Notifications. 

You can do this by opening the Workflow Maintenance window (GP -> Tools -> Setup -> Company -> Workflow Maintenance). 
Under each step there will be a Send Message field, make sure this is marked and using a default message with a *. 

There are also notification options under the main Workflow tab called ‘Send notifications for completed actions’ make sure these are also using default messages.

Then, check Active Directory and make sure that the Email field on the front of every Approver’s card is filled out with the correct value. 

If it is grayed out, then you are tied to Exchange Online, so these should be correct.

![Form 6](media/emailjohn6.jpg)


### Troubleshooting tips for Workflow E-mail

#### Execution Timeout Expired. The timeout period elapsed prior to the completion of the operation or the server is not responding.

When approving Requestions as an example thru Workflow email links (which uses web services), notifications may not go to the approver. If you look at the exception errors for System you will see 

When reviewing a SQL Profile trace, you can see calls (qdCreateSQL procedure) that happen for each E-Mail being sent.  There is about a 30 second window for this to complete.  If you have a larger data set and maybe joined more tables to the workflow message, this may not complete and cause the above error and then notifications appear to stop.  To resolve this problem, you may need to look at the workflow, tables that are joined, comments that are printing and see if there is an index that can be put on a specific table to better  sort through the data.  The SQL Display Estimated Execution Plan can be used to help identify your specific data issue.

1. If no workflow emails are sent, verify if it is all workflow or just one specific workflow where this is not working.

a. For the user you are testing with, verify in *Active Directory under the General tab* that the E-mail field is populated, if it is blank emails will not send.
         This needs to be done for all users that are GP Approvers in workflow
b. Try to send a Test E-Mail in Workflow Setup does it work?  This process will use the user listed in the SMTP Authentication area of the window.
c. The SY04920 table is not used for workflow emails or Modern Auth once setup and becomes non-relevant.            
      
2. If we are using templates, we should try a workflow email with no attachments, just to see if the email works.

3. When a user 1st submits for approval in workflow, that will go through Exchange, usually submitted within Dynamics GP.
From there on out, when a user approves through the workflow email links, to approve what was submitted, that will use [SMTP](https://community.dynamics.com/blogs/post/?postid=7aaa9918-06a0-4e88-adac-fc30853b97dc) for all other approvals from Web Services workflow emails.

If an email is failing from the email links this could indicate a problem with web services.
Test approving the email from within Dynamics GP, then we know workflow and emails are working, just not the web services links.

4. [What is the email flow of workflow and what user is the email coming from?](https://community.dynamics.com/blogs/post/?postid=33c8f2f3-2794-4bf7-ac60-f3a00588ce42#:~:text=There%20are%20three%20different%20processes,behalf%20of%20the%20GP%20user.)
   
6. Make sure you have VALID users in AD as Workflow Managers.  If you do not have valid AD users as Workflow Managers, it may cause performance issues in your workflow and undesired results.  
Many times, customers have employees that leave the company but their users are still part of the workflow and may cause issues.
To help streamline your processes and increase efficiency, {review this article and video](https://community.dynamics.com/blogs/post/?postid=d847301a-a499-439c-bd68-d46173504e2f) for tips about setting up your workflows for optimized performance.

#### The file you have selected does not exist

You may notice this error message when sending email with attachments in workflow.

1. Does the error seem intermittent?  Does it only happen when you are trying to attach something to the email?
2. If it works with some attachments and not others what is the difference?
3. This error can happen when the attachment file name is very long.
4. You may also see this error message if the Batch ID you submit the workflow on has special characters, test with a simple Batch ID and see if it works.

[How to verify if Microsoft Dynamics GP Web Services is functioning correctly](/troubleshoot/dynamics/gp/verify-if-web-service-is-correct)

> [!NOTE]
> If you notice that workflow was working fine and now workflow seems to hang and is very slow in look up's to Active Directory with users, it could be caused >by changes to your Anti-virus.  Test to temporarily disable the AV or create an exception for Dynamics GP.  You may also notice it hang when you login to >Dynamics GP with an error message 'Initializing Microsoft Dynamics GP'.
> 

## <a name=mfa></a>MFA - Multi-Factor Authentication (Modern Authentication)

- [Set up the application in the Azure Portal](/microsoft-365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)  
- [Configure Modern Authentication in Dynamics GP](https://community.dynamics.com/blogs/post/?postid=bce65f37-eb08-4531-b62b-32a8af728f58)
- [Configure Modern Authentication in Web Client](https://community.dynamics.com/blogs/post/?postid=7a9575dc-6d56-4f3e-86a9-9fd4e23cbfd9)
- [MFA VIDEO LEARNING](https://www.youtube.com/watch?v=81YZ8B6bHPk&t=7s)

> [!NOTE]
> When Basic Authentication is deprecated, you will need to be on a version of Dynamics GP where you can use Modern Authentication (18.3 or later).
>
> You do not actually need MFA turned on for your Azure account to use the Modern Auth window in Microsoft Dyanmics GP.

There have been many quality issues fixed within Dynamics GP around Multi-Factor Authentication, so it is recommended to be on 18.5 or later to not run into an issue that is already fixed in the product.

To use modern authentication with Dynamics GP, the Application (Client ID) is required to be entered in the **Company E-Mail Setup** window in Dynamics GP. Get this ID from Azure, where it is located under Tools, Setup, Company, and the choose **Company E-mail Setup**. MFA enabled on each user's Office 365 account is an additional layer of security for an organization but not required by Dynamics GP.

By turning modern authentication on in Dynamics GP (Application Client ID populated), you are then telling the system to use Modern Authentication vs Basic Authentication (depreciated as of October 2022). If you recently upgraded and set up modern authentication, we recommend to be on the latest version if you can of Dynamics GP to encompass all the fixes released around modern authentication.

> [!NOTE]
> **If you recently upgraded to 18.5/18.6/18.7 and had Modern Authentication working in a prior release, but now emails are not sending**
> With the upgrade we are seeing where emails are no longer sending with Modern Authentication enabled.  The finding is your [Microsoft Entra ID needs to be upgraded](https://community.dynamics.com/blogs/post/?postid=b571b4d4-1d58-41f4-b4a3-3c8ee1c4602c)


> [!NOTE]
> **Modern Auth and Web Client**
> You may find you need to change what account that is emailing from Web Client or Web Client emails have stopped working.  Follow these steps to "reset" your Web Client Modern Auth (MFA):
> 1. Log into the Dynamics GP desktop client on the Web Client server.
> 2. Navigate to the Company Email Setup window and note what you have entered for both the Desktop and Web Client Properties
> 3. Clear out those 4 fields, then close that window and log out of GP
> 4. Sign back in to the desktop client on the web client server. You should right click and launch GP as Admin when we do this. Go back to the Company Email Setup window and enter the Application (Client) ID for the Desktop Properties section only.
> 5. Select OK on that window to get the sign in prompt. Sign in to save the setting.
> 6. Now sign in to the Web Client, go to Company Email Setup and enter the 3 Web Client Properties fields. 
> 7. Select OK to get the sign-in prompt. Sign in as the user you want to send all email from the Web Client going forward.
> 8. If that sign-in passes, test emailing out of the Web Client.

When you have modern authentication enabled and you try to use the **"SEND TO"** option in Microsoft Dynamics GP, it will still prompt for the Exchange login.  Modern authentication is not enabled off the "SEND TO" button/option.  An alternative workaround to this is use the Report Option Windows as modern authentication is enabled there.  For example if you are printing a Trial Balance,  go to Reports | Financial Trial Balance and create a report option from this window for the report to email and modern authentication is enabled in all Report Option windows. Many customers use this for posting reports too so it will be a process change to use the Report Options window where modern authentication is now enabled VS the "SEND TO" option.

> [!NOTE]
> **The "To" button in the E-mail Addresses section of the Internet Information window changed fuctionality**. 
> 
> Typically, this window will open up a list of e-mail contacts. When you have MFA (Modern Auth) enabled and you are on 18.4.1461 or later, the "Workflow User Selection" window will appear instead.
> This is due to how MFA works and MSGraph does not have methods for interacting with the address book.  
>
> The workaround/solution is to just type in the email in the box.

### Dynamics GP, Modern Authentication and Third Party Authentication

As more users start to use modern authentication a common question that may come up is does GP work or is compatible with a 3rd party authentication provider.  There are many, but a common one that comes up is DUO as an example.

Microsoft Dynamics GP is not tested with any 3rd party authentication provider, thus they are not supported, but they may work in the environment depending on how it is setup.  Microsoft Dynamics GP support cannot assist with this process but below are recommendations for the setup.

Dynamics GP makes a direct call to Azure for OAuth, we need OAuth to be there. That isn’t to say that DUO and GP are mutually exclusive. In general, if you have a single user setup with OAuth MFA, you can setup our MFA as normal, then everything appears to work after setup.

The generic steps to get it to work are as follows:

1. Disable the 3rd Party Authentication for a single Admin user
2. Setup this user with classic Exchange/O365 MFA
3. Use this user to setup the application registration in Azure and get an App ID setup
4. Setup the App ID in GP, and follow the usual prompts
5. Confirm this user can send a test email using the MFA functionality
6. Confirm a user setup with 3rd Party Authentication can email out of GP

(Optional) Swap the Admin user back to the 3rd Party Authentication after disabling O365 Authentication.

Some items to watch out for:

1. The new modern authentication functionality in Dynamics GP MUST be setup for DUO to work. It blocks Basic Auth, and the new functionality is needed to bypass this block
2. A single user MUST be setup with OAuth MFA to complete the initial modern authentication setup within Azure and GP (the Email Settings window) This user can be swapped back to DUO after the setup.
3. We cannot guarantee this will work in all environments since it hasn't really been fully tested.

### Dynamics GP Error Message: There were one or more issues when processing email, please review the DynamicsGP_MSGraphEmail.log file in the temp directory

Please review each of the items below to determine the cause of this error message.

1. Did you have MFA working on a prior version?  If you did, when you upgrade, if you had MFA on prior, you need to follow the steps:
[Modern Authentication and upgrading to Microsoft Dynamics GP](https://community.dynamics.com/blogs/post/?postid=b571b4d4-1d58-41f4-b4a3-3c8ee1c4602c)
 
2.  Tools | Setup | Company | Email Setup, unless you are using web client, only the Desktop Client properties need to be populated with your application ID.  The Tenant ID field should be left blank, [unless you are using the new feature in 18.6 that allows Single tenant in Azure](https://community.dynamics.com/blogs/post/?postid=18194a5d-4b7f-ee11-a81c-6045bdbe566c). 
 
3.  You are getting a message about the Dynamics_MSGraphEmail.log file. Review this file to see if there is a different error message.  To get this file you need to go to the workstation/machine where you got that error and go to Start > Run, type %temp% and click OK to open your local temp file. The log file should be found there.

4.  Did you try this on another machine and with another user such as user SA on SQL server just to rule out machine specific and .NET issues, etc.
MFA needs .net 4.7.2 to be installed on GP Client server.
[Determine which .NET Framework versions are installed - .NET Framework | Microsoft Docs](/dotnet/framework/migration-guide/how-to-determine-which-versions-are-installed)
[Download .NET Framework 4.8](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48)

5. Confirm that TLS 1.2 is turned on
[Transport Layer Security (TLS) best practices with .NET Framework](/dotnet/framework/network-programming/tls#configure-schannel-protocols-in-the-windows-registry)

6.  Are you getting the old "exchange" window prompt?  Review your Dynamics.set file for a [3rd party that maybe causing this issue](https://www.accountable.com/Downloads/FormsPrinter/V19.00/Forms-Printer-Version-186171-HF1).
 
7.  The easiest way to test email authentication with MFA is to email through a report option window to see if email works and sends.
You only need to authenticate 1x per GP login.
 
Example
Reports | Financial Trail Balance create a new report option and setup the email options.  Do a small sub set of data, if too big it will not email.
Then try to email from here to see if you are prompted for MFA login and report emails.
 
If this works, while still logged in, now go try to do your other process to see if it works.  We only prompt to authenticate once per day while staying logged in as the GP user.

8. If the report options report email is successful, then you will want to review this blog for application process items to rule out, such as templates, messages, etc.
[EFT Check Remittances are not e-mailing](https://community.dynamics.com/blogs/post/?postid=5acf230c-9fcd-4f9f-99ca-f88d2718c151)
 
9. If you find your emails are working and this error is sporadic in nature, it could be related to the file size of an attachment.  Try this process with no attachments and see if it works.
 
10. If you are emailing from within the NAV List and selecting multiple items at a time for email (such as 60 – 200) and some could contain attachments or not, you could also exceed a maximum which will cause this error. 
Try to select and send 20 or 30 at a time to rule out the above case.
[Microsoft 365 limits - Service Descriptions](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1)

11.  You can run a [Fiddler trace](/dynamics-gp/installation/email-troubleshooting-guide#to-run-fiddler) to see if it shows anything further about the error message.

### Dynamics GP Error Message: An error occurred authenticating with Azure Graph, check your configuration and try again

Please review each of the items below to determine the possible solution / cause of this error message.

1. Tools | Setup | Company | Email Setup, unless you are using web client, only the Desktop Client properties need to be populated with your application ID.  The Tenant ID field should be left blank, [unless you are using the new feature in 18.6 that allows Single tenant in Azure](https://community.dynamics.com/blogs/post/?postid=18194a5d-4b7f-ee11-a81c-6045bdbe566c). 
Sometimes it is easier to get the Desktop Client working then go onto other fields if needed in this window, based on what you are deploying in Dynamics GP.

2. Did you try this on another machine and with another user such as user SA on SQL server just to rule out machine specific and .NET issues, etc.
MFA needs .net 4.7.2 to be installed on GP Client server.
[Determine which .NET Framework versions are installed - .NET Framework | Microsoft Docs](/dotnet/framework/migration-guide/how-to-determine-which-versions-are-installed)
[Download .NET Framework 4.8](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48)

3. If we find this is machine specific, example the error only happens for a new user / new machine install of Dynamics GP in the environment (other users use MFA and email fine).  
What you can review is go to the user’s folder path, example: C:\Users\(userid)\AppData\Roaming\, manually create a folder named ‘Microsoft Business Solutions’.
Usually Dynamics GP will create this folder.  Within this folder is the ‘Microsoft Dynamics GP’ folder which holds the auto-complete files for each company, but it appears at times this folder is not created, maybe because an attempt to email is being done before the user does anything with the auto-complete process.  Once the folder is created for the user, have them log back into Dynamics GP and test email.

4. If the Application ID is not saving or has issues, test by launching GP as Administrator, right-click your GP icon and choose Run as Administrator.

5. This error can be caused by using an App Registration that was setup as "Single Tenant" instead of "Multitenant" and then entering it in the wrong field in Dynamics GP.  
If you go to a workstation where they get this error, go to Start > Run, type %temp% and click OK it will open the local temp folder. They may have a MSGraph log file being created there that will provide more information.

6. As a test, temporarily, fully disabling the Public, Private, and Domain firewalls. Then log into the server with an O365 account to enter the AppID. If the application ID saves, you can re-enabled the firewalls and continue to email from Dynamics GP.

7. Anti-virus can also cause issues with saving the application ID.  Test to temporarily disable the AV or create an exception for Dynamics GP code folder. Reboot may be required once added.

8. If all else fails, we can enter the application ID in Microsoft SQL Server Management Studio.
select MSGraphClientID, * from SY04900
This table needs to be populated with an application ID in each company you want to email out of.
Once the field is populated, log back into Microsoft Dynamics GP and do a test email.

The easiest way to test email authentication with MFA is to email through a report option window to see if email works and sends. You only need to authenticate 1x per GP login.
Example Reports | Financial Trail Balance create a new report option and setup the email options. Do a small sub set of data, if too big it will not email. Then try to email from here to see if you are prompted for MFA login and report emails.  If this works, while still logged in, now go try to do your other process to see if it works. 

   
## Emailing Setup Guide by Module

The document below covers setup of email starting with System Wide Setup, Purchasing, Sales, and Workflow setup.
Depending on what area of email you need to setup, please review the steps outlined below.
- [Emailing Setup Guide](https://community.dynamics.com/gp/b/dynamicsgp/posts/emailing-setup-guide#_Toc71192006)  


