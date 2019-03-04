---
title: "VAT and Make Tax Digital"
description: "The British version of Dynamics GP supports the Make Tax Digital service."
keywords: "tax"
author: edupont04
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: jchrist
ms.date: 02/12/2019
---

# VAT in the UK Version of Microsoft Dynamics GP

Her Majesty's Revenue and Customs (HMRC) is implementing the first step of Making Tax Digital, which imposes new requirements on VAT registered businesses above the VAT threshold. Requirements will be implemented in phases. In the first phase, with a deadline in April, 2019, the following requirements will take effect:

* Keeping records digitally - Businesses must now keep all their records digitally. For users of ERP systems this will not have any impact since they already keep their records digitally in these systems.  
* Submit VAT return electronically using [software recognized by HMRC](https://www.gov.uk/guidance/software-for-sending-income-tax-updates).  

## Set up Making Tax Digital for VAT

The Making Tax Digital feature uses a service connection to communicate with HMRC.

In the **Company Setup** window, you must specify your company's tax registration number.

![Screenshot](media/uk-tax-company-setup.png)

In the **UK Digital VAT Setup** window (Cards -> Company-UK Electronic VAT Setup), you must specify that you want to use the Making Tax Digital service.  

![Screenshot](media/uk-tax-digital-tax-setup.png)

### Set up VAT returns

HMRC maintains a list of VAT obligations for companies, which are the periods for which they must report VAT and the due date for the report. HMRC exposes this information through their API so that Dynamics GP can retrieve the obligations. Dynamics GP stores VAT obligations as **VAT Return Periods**, and uses them to:

* Remind you about VAT returns that are due or overdue.  
* Automatically enter start and end dates when you create VAT returns.  

In order to use the Making Tax Digital service, you must connect to the service from the **VAT Return** window.

![Screenshot](media/uk-tax-vat-return.png)

To enable the connection, you must create a new VAT return.

#### To connect to the Making Tax Digital service

1. In the **VAT Return** window, enter a VAT Report ID, and then enter a year (this is the year that your VAT tax obligation is due).

2. Once you tab off the **Year** field, the **HMRC Log in** window appears where you can login to the HMRC site.

    ![Screenshot](media/uk-tax-gov1.png)

    ![Screenshot](media/uk-tax-gov2.png)

3. Grant authority to the software application to access your VAT information. 

    ![Screenshot](media/uk-tax-gov3.png)

4. After you have successfully logged in, then the **VAT Obligations** window opens, and you can choose your obligation period. This comes from the HMRC site and will return your company’s VAT periods.

    ![Screenshot](media/uk-tax-obligations.png)

    The screenshot above is based on a test environment with quarterly VAT tax and only 2 obligation periods open. Your view will be different.

5. When you return to the **VAT Return** window, click Calculate to have the system calculate VAT for you as shown in the following picture.

    ![Screenshot](media/uk-tax-vat-return2.png)

    If the calculations are not correct, you can clear the window at this time. Then repeat steps above when ready. Click **Save** to save the information.

6. When you save the VAT return, VAT box fields are now editable so any further corrections can be made.

    ![Screenshot](media/uk-tax-vat-return3.png)

    The **Final Return** checkbox is also editable and it must be marked before you can submit. 

    ![Screenshot](media/uk-tax-vat-return4.png)

7. Click **Submit** to start the submission. You must supply your HMRC credentials again.

    You will get a mandatory message required by HMRC, click ok and then you will see a progress bar for the VAT information being submitted to HMRC.

    ![Screenshot](media/uk-vat-submit.png)

When the submission is complete you will see the VAT Response window.

![Screenshot](media/uk-tax-vat-response.png)

> [!NOTE]
> After submitting the return, if the progress window does not start and there is no response window, it could be a proxy server issue. For more information, see [https://developer.service.hmrc.gov.uk/api-documentation/docs/reference-guide#network-access](https://developer.service.hmrc.gov.uk/api-documentation/docs/reference-guide#network-access)  

>  [!NOTE]
> The above Making Tax Digital process of submitting to the HMRC also works for the VAT Daybook module in Dynamics GP. 
