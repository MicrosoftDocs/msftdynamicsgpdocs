---
title: "Canadian Payroll Year-end Update & Tax Update"
description: "Learn about the Canadian payroll year-end updates & tax updates. The article is updated every year when new requirements are published."
keywords: "year-end"
author: theley502
manager: edupont

ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 12/9/2022
---

# Canadian Payroll 2022 Year-end Update & 2023 Tax Update

This document contains instructions for updating the Canadian Payroll module for Microsoft Dynamics GP for 2022 filing requirements. This update also includes Round 1 tax updates for 2023 federal, provincial, and territorial taxes.

These instructions assume that you are already familiar with Microsoft Dynamics GP Canadian Payroll.

## Introduction

You can find information about year-end procedures in the "Year-End Procedures", "T4/R1 Routines,", and "T4A Routines" chapters in the Canadian Payroll documentation.

Note, however, that the instructions in this document expand on those instructions and in some cases supersede them.

### What's in this document

This document contains the following chapters:

*Chapter 1, "Canadian Payroll year-end checklist,"* contains a checklist that you can use for year-end procedures.

*Chapter 2, "Preparation and installation,"* specifies prerequisites, and provides installation instructions for the year-end update and tax update.

*Chapter 3, "Electronic filing in XML format,"* contains information that you can use to prepare T4/T4A slips and RL-1 forms with Canadian Payroll for magnetic media filing in XML format.

*Chapter 4, "Tax updates,"* describes the federal and provincial or territorial tax changes for 2020.

### What's changed

The 2022 Year-End Update/2023 Tax Update contains changes in the information that's submitted to the Canada Revenue Agency (CRA) and Ministère du Revenu du Québec.

> [!NOTE]
> For more information, see the [updated blog of recent changes for Canadian Payroll](https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-year-end-update-2022-canadian-payroll).

#### Tax changes

See [Chapter 4: Tax updates](#chapter-4-tax-updates) for a description of the 2023 federal, provincial, and territorial tax changes.

#### General application changes

The 2022 Year-End Update/2023 Tax Update contains application bug fixes and functionality updates to comply with regulatory changes.

#### XML and form changes

RL-1 XML and form changes
No T4 or T4A form and XML changes  

- Software Development Number for XML - RQ-22-01-072
- RL-1 Slip Authorization number -  FS2201091 (enter this in the Payroll T4/R1 Print window)  

#### Installation notes

The 2023 Canadian Payroll Tax Update must be installed on the server and on each client workstation where Microsoft Dynamics GP is used. Before installing the update, be sure to complete the following tasks:

All users should exit Microsoft Dynamics GP until the update has been installed on all workstations.

Close all programs, turn off the screen saver, and back up important data and programs before continuing with the update.

Save backup copies of your Reports.dic, R7131.dic, F7131.dic, Forms.dic, and Dynamics.vba files, if these files are present in your installation.

### Resources

If you have questions about Canadian Payroll year-end closing procedures and your Microsoft Business Solutions Partner isn't available, there are several resources, in addition to this document, to assist in answering your year-end questions.

#### 2022 year-end information

Look at [Dynamics GP Downloads](/dynamics/s-e/gp/cagptuye2018_285) to find out what year-end maintenance and tax changes are included in each update and to download the update. All instructions for downloading and installing the tax updates also will be provided there.

Look for "2022 Canadian Payroll Year End Update for Microsoft Dynamics GP".

## Chapter 1: Canadian Payroll year-end checklist

Use the following checklist for Canadian Payroll year-end processing. For detailed instructions for completing each step, refer to the sections listed in specific steps and to the instructions in the Canadian Payroll manual or online help.

### Checklist steps

|**Step**|**Description** |
|----------|--------------|
| 1.       | Complete all 2022 pay runs. |
| 2.       | Note: Any batch with a cheque date of 2023 should be processed after the Year End File Reset. For example, if the cheque date of your final pay period for 2022 is January 1, 2023, the 2023 tax tables must be used for that pay run. |
| 3.       | Complete any necessary 2022 payroll reports.        |
| 4.       | Install the 2022 Canadian Payroll Year-End Update. See [Installing the update](#installing-the-update).      |
| 5.       | Note: Do not restart Microsoft Dynamics GP on any workstation until the update has been installed on all workstations that run the application.       |
| 6.       | Complete the Year End File Reset.                                       |
| 7.       | Note: To ensure that all tables are available for resetting, make sure that the Year End File Reset window is the only window open in Microsoft Dynamics GP.|
| 8.       | Make a backup of your data titled "Post 2022 Year-End Update."\*|
| 9.       | Note: The following steps can be done any time after the Year End File Reset has been completed.|
| 10.      | Create T4, T4A, and RL-1 statements, and print the T4, T4A, and RL-1 reports.  |
| 11.      | Edit the T4, T4A, and RL-1 records, as necessary. You can print an edit list from the Payroll Routines - Canada window. |
| 12.      | Create T4, T4A, and RL-1 Summary records.      |

> [!NOTE]
> By law, you must be able to reproduce original or amended T4, T4A, and RL-1 slips for a predefined (agency assigned) number of years after the original filing. To meet this requirement, be sure to keep backups of all your Canadian Payroll data files, as well as copies of reports, tax forms, and filings. Canadian Payroll will only allow you to re-create a prior year filing if you save backup copies of the prior reporting year data.  

To make it easier to determine CPP and EI maximums between running a payroll in a new year (2023 maximums) and printing T4's from prior years (2022 maximum), two constants are created each with the year maximum in place.

Example:
Constant 1 2022 Maximum
Constant 2 2023 Maximum

To determine when you run a 2023 payroll what maximum to use, the system looks to the **Federal Basic Personal Amount** in the Tax Credit Control window.
Tools | Setup | Payroll Canada | Control | Tax Credits.
The system expects the amount of $15,000 for Federal Basic personal Amount in the control and then it will pull the 2023 maximum.


## Chapter 2: Preparation and installation

This portion of the documentation specifies the requirements for installing the 2022 Year-End Update / 2023 Tax Update.

### Supported versions

The 2022 Year-End Update / 2023 Tax Update supports Microsoft Dynamics GP (18.5). To identify the Microsoft Dynamics GP release you're using, start the application and choose Help \>\> About Microsoft Dynamics GP.

To identify the Canadian Payroll release you're using, start Microsoft Dynamics GP, then open the Payroll Control Setup – Canada window (Microsoft Dynamics GP menu \>\>Tools \>\> Setup \>\> Payroll – Canada \>\> Control). You should see the release number in the upper left corner of the window.

If you are using an unsupported release of Microsoft Dynamics GP, you won't receive all of the necessary information to complete year-end closing and payroll tax procedures. This information includes personal amounts, Employment Insurance (EI), Canadian Pension Plan (CPP), and Quebec Pension Plan (QPP) amounts. To update the information, install Microsoft Dynamics GP 2015 or higher before installing this update.

> [!TIP]
> To view a list of product discontinuation dates, see the [Dynamics GP Lifecycle](https://support.microsoft.com/lifecycle/search?alpha=Dynamics%20Gp) site. The link is also available from the [Lifecycle and Upgrade Services blog](https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-upgrade-blog-series-schedule).

### Obtaining a CRW Web Access Code

If you plan to use the Internet to submit T4 records, you need to obtain a Web Access Code from the Canada Revenue Agency (CRA), which preauthorizes you to submit files using this method. Web Access Codes are valid for one year only, so you need to get a new one each year.

The Web Access Code consists of six characters: two letters, and four numbers. The code is case sensitive which means that you must enter it exactly as it appears on your personalized T4 Summary form. If you do not enter the code correctly, you will not be able to access the secure areas of the CRA's T4 Internet File Transfer site.

For more information, see the [CRA website](https://www.cra-arc.gc.ca/eservices/rf/cd-eng.html).

Canadian Payroll for Microsoft Dynamics GP has the ability to generate the XML file required for T4 Internet File Transfer, but you are responsible for obtaining the access code and actually submitting the file to the CRA.

### Finding the Software Developer Number and RL-1 Authorization number

If you plan to use the Internet to submit RL-1 records, you need to obtain the Software Developer Number and the RL-1 Slip authorization number. Both numbers change every year.

Both numbers are available with the Canadian year-end update in the [Microsoft Dynamics GP Resource Directory](../resources.md) article.

You also can see [XML and form changes](#xml-and-form-changes) for the RL-1 authorization number and the steps for entering it.

### Installing the update

The update must be installed on each client workstation where Microsoft Dynamics GP is used. When installing the update, be sure to complete the following tasks:

- All users must should exit Microsoft Dynamics GP until the update has been installed on all workstations.

- Close all programs, turn off the screen saver, and back up important data and programs before continuing with the update.

- Save backup copies of your Reports.dic, R7131.dic, F7131.dic, Forms.dic, and Dynamics.vba files, if these files are present in your installation.

#### To install the update

1. Download the update from [Dynamics GP Downloads](/dynamics/s-e/gp/mdgp2018_release_download_378).

    | **Language** | **Microsoft Dynamics GP**                  | 
    |--------------|--------------------------------------------|
    | English      | MicrosoftDynamicsGP18- KB4602595-ENU.msp   | 
    | French       | MicrosoftDynamicsGP18- KB4602596-FRCA.msp  | 

    Save the .msp file to a folder on the local disk drive of the server  workstation that runs Microsoft Dynamics GP.

    > [!NOTE]
    > The year-end update file also includes all prior Microsoft Dynamics GP updates. See also [Service Pack, Hotfix, and Compliance Update Patch Releases for Microsoft Dynamics GP](/dynamics/s-e/gp/mdgp2018_patchreleases_377). This update is inclusive of the Fall / October 2022 release for Microsoft Dynamics GP.

2. Double-click the file that you just downloaded. Progress windows appear as space requirements are verified and files are installed.

3. A message may appear, asking if you want to restart now or later. Click Yes to restart now, you will need to run the update file again after restarting.

4. After the installation is finished, manually restart your computer if a message directed you to do so earlier.

5. Start Microsoft Dynamics GP Utilities.

    | Microsoft Dynamics GP | Start \>\> All Programs \>\> Microsoft Dynamics \>\> GP \>\> GP Utilities |


6. In the **Welcome to Microsoft Dynamics GP Utilities** window, verify your server name, enter the system administrator user ID and password, and click OK.

7. In the second welcome window, click **Next**.

8. In the **Upgrade Microsoft Dynamics GP** window, click **Next**. The **Server Installation Progress** window describes the process as it progresses.

9. In the **Upgrade these companies** window, click **Next**. All companies are selected to be updated.

10. In the **Confirmation** window, click **Finish**. Microsoft Dynamics GP Utilities updates your company databases. This process may take several minutes to complete.  
    The **Server Installation Progress** window describes the process as it progresses.

11. After the update process is finished and is successful, the **Additional Tasks** window opens. If the update process wasn't successful, the **Update Company Tables** window opens.  

    To contact Microsoft Dynamics GP Technical Support, see [Resources](#resources) for more information. For more information about the Microsoft Dynamics GP Utilities, see [Using Microsoft Dynamics Utilities](../installation/using-microsoft-dynamics-utilities.md).

12. In the **Additional Tasks** window, choose **Update modified forms and reports**, and then click **Process**. The **Locate Launch File** window appears.

13. Select the location of the launch file (Dynamics.set). In most cases you can accept the default location. Click Next. The **Update Modified Forms and Reports** window appears.

14. Mark the check box next to Microsoft Dynamics GP and any additional components listed.

15. When you mark a component's check box, a **Product Details** window may appear, allowing you to select the location of the component's original code dictionary. You also can open the **Product Details** window by selecting a component and clicking Details.

    When you apply an update (.msp file), any dictionaries whose compatibility ID has changed are backed up to a folder named "Version \<Version Number\> Backup". This folder is located in the same folder as Dynamics.exe. The \<Version Number\> value is the version you were using before applying the update. If the original dictionary exists in the backup folder, Microsoft Dynamics GP Utilities will automatically display its location in the Product Details window, and you can click OK to accept the location. If the location is missing or incorrect, click the file folder icon and browse to the appropriate location.

16. When you have finished selecting components, click **Update**. A **Report Update Progress** window displays the status of the update. When the process finishes, click **Close**. Log files containing detailed information are saved in the \\Data folder. For each component, a report named "Update\<Version_Name\>.log is generated. An update summary named "Update\<Verison\>.txt is also generated.

17. In the **Modified Forms and Reports** window, click **Next**. The **Additional Tasks** window opens where you can start Microsoft Dynamics GP or exit Microsoft Dynamics GP Utilities.

    We recommend that you start Microsoft Dynamics GP and review all your modified forms and reports to verify whether they were updated correctly.

    After the update to tables is completed, you can set up Automated Client Update to update all client workstations. For information about setting up the automatic updates, refer to your System Administrator manual.

    > [!Note]
    > To install the update on an operating system with User Account Control (UAC) activated, see [Installing with UAC activated](#installing-with-uac-activated).

To verify that you've installed the latest year-end update and tax update, check the **Last Year-End Update** field in the **Payroll Reset Files – Canada** window (Microsoft Dynamics GP menu \>\> Tools \>\> Routines \>\> Payroll – Canada \>\> Year End File Reset). It should be 12/20/2022 or later.

For the tax update, check the Last Tax Update field in the Payroll Control Setup – Canada window (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Payroll – Canada \>\> Control). It should be 12/20/2022 or later.

### Installing with UAC activated

User Account Control (UAC) is an enhanced security feature in Windows. UAC is activated by default. Before performing actions that could affect your computer's operation, such as installing software updates, UAC asks for permission. To install the update on a client computer when UAC is active, copy the .msp file to each client workstation, then use one of the following methods:

- Start Microsoft Dynamics GP as a user that has administrative privileges on the local computer. (To do this, right-click on the Microsoft Dynamics GP shortcut and choose Run as administrator.) Double-click the .msp file to install it.

- Start the Command Prompt (located in the Accessories group) as a user that has administrative privileges on the local computer. (To do this,right-click on the Command Prompt shortcut and select Run as administrator.) Set the current directory to the location where you copied the .msp file.

Example, for Microsoft Dynamics GP 2018 (English), enter the following command.

```cmd
Msiexec /p MicrosoftDynamicsGP18-KB4602595-ENU.msp /l\*v C:\\MSPErrorlog.txt
```

If you want the user to install updates and service packs without having administrative privileges on the local computer, you can change permissions for the folder where Microsoft Dynamics GP is installed. Be aware that doing this makes your computer less secure.

## Chapter 3: Electronic filing in XML format

Canadian Payroll can generate electronic files in the XML format. You are responsible for submitting the file to the CRA or Revenue Quebec.

You don't need to have any special knowledge of XML to generate an XML electronic file using Canadian Payroll.

### Filing the T4/T4A in XML format

You can use Canadian Payroll to generate the T4 and T4A slips in XML files that you are responsible for submitting to the CRA.

#### Data validation

By using the XML format, the CRA is able to validate the file as soon as you submit it and alert you to any errors or omissions in the file. To help you submit an error-free file, Canadian Payroll includes several features to validate your data prior to submission.

**Verification report** You can print the T4 Error Report or T4A Error Report to verify the data in your XML file before you submit it to the CRA. The report will identify and describe any errors. You must resolve all the errors before you can generate the T4 and T4A XML files.

**Data entry validation** As you enter data during the tax year, entries throughout Canadian Payroll that will be reflected in electronic files will be verified, and messages will advise you of any non-valid entries. T4 and T4A information is drawn from the following locations in Microsoft Dynamics GP.

| **Type of data**        | **Source**  |
|-------------------------|-------------|
| Employer information    | **Payroll T4 Summary Edit – Canada** and **Payroll T4A Summary Edit – Canada** windows |
| Employee information    | **Payroll T4 Edit – Canada** and **Payroll T4A Edit - Canada** windows  |
| Withholding amounts     | Cumulative totals, gathered during the payroll process, which are displayed on the **Payroll T4 Edit – Canada** and **Payroll T4A Edit - Canada** windows |
| Transmitter information | **Payroll Electronic Transfer T4/T4A** windows  |

### Filing the RL-1 in XML format

Before you use the Internet to submit RL-1 records, you need an RL-1 Authorization number and form number (found above). 
Both numbers change every year.

#### Data validation features

By using the XML format, Revenue Quebec will validate the file as soon as you submit it and alert you to any errors or omissions in the file. To help you submit an error-free file, Canadian Payroll includes several features to validate your data prior to submission.

**Verification report** You can print the RL-1 Error Report to verify the data in your file before you submit it to Revenue Quebec. The report will identify and describe any errors. You must resolve all the errors before you can generate the RL-1 files.

**Data entry validation** As you enter data during the tax year, entries throughout Canadian Payroll that will be reflected in electronic files will be verified, and messages will advise you of any non-valid entries. RL-1 information is drawn from the following locations in Microsoft Dynamics GP.

| **Type of data**        | **Source**    |
|-------------------------|-----------|
| Employer information    | **Payroll R1 Summary Edit - Canada** window  |
| Employee information    | **Payroll R1 Edit - Canada** window  |
| Withholding amount      | Cumulative totals, gathered during payroll process, which are displayed on the **Payroll R1 Edit - Canada** window |
| Transmitter information | **Payroll Electronic Transfer R1** window  |

### Filing an amended or cancelled RL-1 in XML format

If changes are needed after you have submitted the RL-1 XML files to Revenue Quebec, you can use Canadian Payroll to generate amended or canceled files that you can then submit to Revenue Quebec.

You use the **Payroll R1 Edit** window to make changes to RL records. You use the **Payroll Electronic Transfer R1** window to generate the amended or canceled files.

## Chapter 4: Tax updates

This chapter lists changes to federal, provincial, and territorial tax rates for 2023. For detailed information about taxes, refer to the [Canada Revenue Agency Web site](https://www.canada.ca/en/revenue-agency/services/tax/individuals/frequently-asked-questions-individuals/canadian-income-tax-rates-individuals-current-previous-years.html) and [Revenue Quebec's Web site](https://www.revenu.gouv.qc.ca/).

### Pension Plan, Employment Insurance, and Parental Insurance changes

#### CPP

Contribution rates for both employers and employees for 2023 is 5.95%. The following changes are in effect for CPP for 2023:

- The maximum pensionable earnings amount will be updated to \$66,600, from \$64,900.

- The basic exemption remains unchanged at \$3,500.

- The maximum contribution amount for the year increases to \$3,754.45, from \$3,499.80.

#### EI for non-Quebec employees

- The EI Maximum Annual Insurable Earnings amount increases to \$61,500, from \$60,300

- The EI premium amount is 1.63%. The EI maximum annual premium amount will be \$1,002.45 from \$952.74 

- The EI Employer Premium Rate amount will change to 2.282%. The employer EI premium is set using the Employer EI Factor field in the Payroll Employer Number Setup – Canada window (Tools \>\> Setup \>\> Payroll-Canada \>\> Employer). This factor must be set to 1.4 to meet the official EI Employer Premium.

#### EI for Quebec employees

- The EI maximum annual insurable earnings amount increases to \$60,300 from \$56,300.

- The EI (Quebec) Premium Rate amount increases to 1.20%, from 1.18%.

- The maximum annual premium amount is \$723.60, from \$664.34.


> [!NOTE]
> To make it easier to determine CPP and EI maximums between running a payroll in a new year (2022 maximums) and printing T4's from prior years (2021 maximum), two constants are created each with the year maximum in place.
>
> Example:
> Constant 1 2022 Maximum
> Constant 2 2021 Maximum


To determine when you run a 2022 payroll what maximum to use, the system looks to the Federal Basic Personal Amount in the Tax Credit Control window (Tools > Setup > Payroll Canada > Control > Tax Credits).
The system expects the amount of $14,398 for Federal Basic personal Amount in the control and then it will pull the 2022 maximum.

If you notice when you run payroll that the CPP is off compared to PDOC and is not calculating the correct amount based on yearly rate.  Verify the Payroll Control Frequency window (Tools \>\> Setup \>\> Payroll-Canada \>\> Control click Frequency button)and make sure the pay periods are setup for the per year option.  For example in year 2020 you may have set it to 26 pay periods, but this did not get changed and it should be 26/27 pay periods for year 2021 this will cause CPP to calculate incorrectly until you update it for the new year.

[The CRA accepts different tax calculation methods, and these are outlined on their website](https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/payroll/t4127-payroll-deductions-formulas-computer-programs.html)

You really cannot compare Microsoft Dynamics GP to the online calculator as we do a different calculation.
Revenue Canada states this is just a guide/estimate, you cannot compare what Microsoft Dynamics GP does to the online calculator.

Dynamics GP uses the method for ‘Cumulative Averaging’ tax calculation method, so it is a complex calculation. Click on the link above, and then click on the link to find the pdf. The method used by GP is similar to OPTION 2 – TAX FORMULA BASED ON CUMULATIVE AVERAGING in Chapter 6. (Please review the information in their documentation to see how it calculates.)

The CRA online calculator uses a ‘simple tax’ method, so you will see differences between the tax estimates versus the ‘Cumulative Averaging’ method used by GP. This is expected and normal behavior for Dynamics GP since Dynamics GP uses a complex tax calculation method.

The Cumulative Averaging convention is quite complex and takes several factors into account that the simple tax method does not. The Cumulative Averaging method takes into account the prior pay period history, the date used, a projected income and how many pay periods have occurred, etc…. So if two employees are getting paid the same rate and same number of hours, their tax calculations would be different if one employee is a new hire, and the other employee is not and has pay history. Refer to the information in the CRA’s handbook. The calculations are in the GP code, so I don’t have a way to see exactly what it did for you, so I would encourage you to review the Cumulative Averaging convention method in the CRA’s handbook so you can get a general idea of what it does.

The CRA defines a ‘range’ of taxes that is acceptable. We have verified that the tax calculations done by Dynamics GP are within the acceptable ranges defined by the CRA.

Taxes are an ‘estimate’, as employees typically overpay or underpay, and have to file a tax return to get to the exact amount due. But the tax calculations done by Dynamics GP reside in the code, and will not be changed since they have met the acceptable ranges as published by the CRA. We have many customers using the Canadian Payroll product and this is not a concern that comes up across a large base of our payroll customers.

The explanation of the Cumulative Averaging convention is the best resource.

[The above information is published in this article](https://support.microsoft.com/en-us/help/2773319/income-tax-calculations-or-discrepancies-with-the-cra-in-canadian-payr)
 
Really only the 1st payroll of the year will tie with the calculator as we use the average method
See our notation in this blog below


#### QPIP

- The QPIP Maximum Annual Insurable Earnings amount increases to \$88,000, from \$83,500.

- The Premium Rate amount remains at 0.494%.

- The Max Premium is \$434.72 from \$412.49.

- The Employer Premium Rate remains at 0.692%. The maximum employer amount will change to \$608.96 from \$577.82.

### Federal tax rates and income thresholds

Effective January 1, 2022 the federal tax rate noted below. The federal index factor is 1.024. The income thresholds are revised as follows.

![income thresholds](media/FED2022.JPG)

### Federal personal amounts

Federal personal amounts have been increased by fixed amounts as shown in the following table.

The Basic Personal amount is updated to \$14,398 (formerly \$13,808).

The Spouse Common Law Partner amount increases by the index factor to \$14,398  (formerly \$13,808), if the original amount was not zero.

The Eligible Dependent amount increases by the index factor to \$14,398 (formerly \$13,808), if the original amount was not zero.

Canada Employment Credit

The Canada Employment credit has been increased to \$1,287 at the lowest rate of 15.0%. The employment credit has been updated so that the Canada employment credit (factor K4) is the lesser of:

- 0.15 X A; or

- 0.15 X \$1,287

### Provincial and territorial tax changes

The following provinces and territories have tax changes for 2021.

> [!NOTE]
> The figures in the following tables are those supplied by the relevant revenue agencies. The actual figures calculated by Canadian Payroll may differ slightly due to rounding. This issue is recognized by the CRA and the  differences will not subject you to penalties for over- or under-withholding.

#### Alberta - no change

- The Alberta basic personal amount is \$19,369.  

- The Alberta spouse or common-law partner amount is \$19,369.

![Alberta tax changes](media/AB2021.JPG)

#### British Columbia

- The British Columbia basic personal amount increases by the index factor to  \$11,302 (formerly \$11,070).

- The British Columbia spouse or common-law partner amount (and eligible dependent) increases by the index factor and is revised to \$11,302  (formerly \$11,070).

![British Columbia tax changes](media/BC2022.JPG)

#### Manitoba

- The Manitoba Basic Personal amount increases by the index factor to \$10,145 (formerly \$9,936).

- The Manitoba spouse or common-law partner amount shall increase to \$10,145 (formerly \$9,936).

![Manitoba tax changes](media/MB2022.JPG)

#### New Brunswick

- The New Brunswick Basic Personal amount increases by the index factor and is usually revised to \$10,817 (formerly \$10,564).

- The spouse or common-law partner amount increases by the index factor and is revised to \$10,817 (formerly \$10,564),

![New Brunswick tax changes](media/NB2022.JPG)

#### Newfoundland and Labrador

- The Newfoundland Basic Personal amount increases by the index factor and is updated to \$9,803 (formerly \$9,536).

- The spouse or common-law partner amount increases by the index factor and is revised to \$9,803 (formerly \$9,536), if the original amount wasn't zero.

![Newfoundland tax changes](media/NL2022.JPG)

#### Northwest Territories

- The Northwest Territories basic personal amount increases by the index factor, and is revised to \$15,609 (formerly \$15,243).

- The spouse or common-law partner amount increases by the index factor and is revised to \$15,609 (formerly \$15,243), if the original amount wasn't zero.

![Northwest tax changes](media/NT2022.JPG)

#### Nova Scotia - no change

- The Nova Scotia basic personal BPANS Formula \$11,481.

- The spouse or common-law partner amount is also BPANS Formula \$11,481.

![Nova Scotia tax changes](media/NS2020.JPG)

#### Nunavut

- The Nunavut basic personal amount increases by the index factor and is usually revised to \$16,862 (formerly \$16,469).

- The spouse or common-law partner amount increases by the index factor and is usually revised to \$16,862 (formerly \$16,469, if the original amount was not zero.

![Nunavut tax changes](media/NU2022.JPG)

#### Ontario

- The Ontario Basic Personal amount increases by the index factor and is usually revised to \$11,141 (formerly \$10,880).

- The Ontario Spouse or Common-law Partner amount increases by the index factor and is usually revised to \$11,141 (formerly \$10,880).

![Ontario tax changes](media/ON2022.JPG)

#### Prince Edward Island - no change

- There is no index factor in PEI, but the personal amount is changed to \$11,250 from \$10,500.  

![Prince Edward island tax changes](media/PE2021.JPG)

#### Quebec

The TP-1015.3-V Basic amount increases by the index factor and is usually revised to \$16,143 (formerly \$15,728). The system rounds this calculation to the nearest \$5.00

#### Variable H – Deduction for employment income

The deduction for Employment income has been increased to \$1,235, formerly \$1,190. 

#### Saskatchewan - no change

- The Saskatchewan Basic Personal amount increases by the index factor, so it is usually revised to \$16,615 (formerly \$16,225).

- The Spouse Common Law Partner amount increases by the index factor, so it is  usually revised to \$16,615 (formerly \$16,225).

![Saskatchewan tax changes](media/SK2022.JPG)

#### Yukon

- The Yukon basic personal amount increases by the index factor and is usually revised to BPAYT formula \$14,398 (formerly \$13,808).

- The spouse or common-law partner amount increases by the index factor and is usually revised to BPAYT formula \$14,398 (formerly \$13,808), provided the original amount was not zero.

![Yukon tax changes](media/YT2022.JPG)

### Updating basic personal amounts

To update the Basic Personal amounts go to: Tools\>\> Routines\>\> PayrollCanada\>\> Year End File Reset

- When the message, "This process will reset YTD totals in the Employee Master file. Do you want to continue?" displays, click Yes.

- When the message, "Do you want to update Basic Personal Amounts in the Control Setup File?" displays, click Yes.

The personal tax credit amounts specified in the P_CPY_Control table will be updated to:

- The federal Basic Personal amount = \$14,398

- Quebec TP-105.3-V Base amount = \$16,143

- Alberta basic personal amount = \$19,369 - no change

- British Columbia basic personal amount = \$11,302

- Manitoba Basic Personal amount =  \$10,145

- New Brunswick Basic Personal amount = \$10,817

- Newfoundland Basic Personal amount = \$9,803

- Northwest Territories basic personal amount = \$15,609

- Nova Scotia basic personal amount BPANS formula  \$11,481

- Nunavut basic personal amount = \$16,862

- Ontario Basic Personal amount = \$11,141

- Prince Edward Island basic personal amount = \$11,250

- Saskatchewan Basic Personal amount = \$16,615

- Yukon basic personal amount = \$14,398 BPAYT formula

You can view these amounts in the Tax Credits window by going to: Tools \>\> Setup \>\> Payroll-Canada \>\> Control \>\> Tax Credits

### Index factors for 2022

The following table shows how Index Factors as specified in the Tax Credit Indexation Factors window (Payroll Reset Files window (Tools\>\>Routines\>\>PayrollCanada\>\>Year End File Reset\>\>Tax Credit Indexation Factors) have been updated.

> [!NOTE]
> An amount listed as 1.009 means that the index factor is 9%.

| **Taxing authority**      | **2021 index factor** | **2022 index factor** |
|---------------------------|-----------------------|-----------------------|
| Federal                   | 1.010                 | 1.024                 |
| Alberta                   | 1.000                 | 1.000                 |
| British Columbia          | 1.011                 | 1.021                 |
| Manitoba                  | 1.010                 | 1.021                 |
| New Brunswick             | 1.010                 | 1.024                 |
| Newfoundland and Labrador | 1.004                 | 1.028                 |
| Northwest Territories     | 1.010                 | 1.024                 |
| Nova Scotia               | 1.000                 | 1.000                 |
| Nunavut                   | 1.010                 | 1.024                 |
| Ontario                   | 1.009                 | 1.024                 |
| Prince Edward Island      | 1.000                 | 1.000                 |
| Quebec                    | 1.0126                | 1.0264                |
| Saskatchewan              | 1.010                 | 1.024                 |
| Yukon                     | 1.010                 | 1.024                 |
