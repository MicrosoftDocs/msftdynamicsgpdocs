---
title: "US payroll tax update"
description: "US 2020 January payroll tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 12/17/2020
---
# U.S. 2021 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server
- Microsoft Dynamics GP 2016 on Microsoft SQL Server

This document contains instructions for installing the 2021 U.S. Payroll Tax Update for Microsoft Dynamics GP.

The first tax update for 2021 replaces all previous tax updates. It includes state tax table changes that took effect January 1, 2021. It is recommended you install this update before processing payrolls for the year 2021.

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

## Changes in January Round 1 update

- Federal changes and FICA Limit
- Arkansas
- Iowa
- Kentucky
- Maine
- Minnesota
- Mississippi
- Missouri
- North Dakota
- South Carolina

### 2021 Federal tax changes

The maximum taxable earnings for Social Security increase in 2021 to \$142,800 from \$137,700

The Personal Exemption is $4,300 for SINGLE, MAR, HOH

Withholding rates for taxpayers filing as *NRA*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,200           | 0              | 0%           | 0                  |
| 12,200      | 22,150           | 0              | 10%          | 12,200             |
| 32,150      | 52,725           | 995.00         | 12%          | 22,150             |
| 52,725      | 98,575           | 4,664.00       | 22%          | 52,725             |
| 98,575      | 177,125          | 14,751.00      | 24%          | 98,575            |
| 177,125     | 221,625          | 33,603.00      | 32%          | 177,125            |
| 221,625     | 535,800          | 47,843.00      | 35%          | 221,625            |
| 535,800     | And Over         | 157,804.25     | 37%          | 535,800            |


Withholding rates for taxpayers filing as *NRAHR*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|             | 18,825           | 0              | 0%           | 0                  |
| 18,825      | 23,800           | 0              | 10%          | 18,825             |
| 23,800      | 39,088           | 497.50         | 12%          | 23,800             |
| 39,088      | 62,013           | 2,332.06       | 22%          | 39,088             |
| 62,013      | 101,288          | 7,375.56       | 24%          | 62,013             |
| 101,288     | 123,538          | 16,801.56      | 32%          | 101,288            |
| 123,538     | 280,625          | 23,921.56      | 35%          | 123,538            |
| 280,625     | And Over         | 78,902.01      | 37%          | 280,625            |

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,200           | 0              | 0%           | 0                  |
| 12,200      | 32,100           | 0              | 10%          | 12,200             |
| 32,100      | 93,250           | 1,990.00       | 12%          | 32,100             |
| 93,250      | 184,950          | 9,328.00       | 22%          | 93,250             |
| 184,950     | 342,050          | 29,502.00      | 24%          | 184,950            |
| 342,050     | 431,050          | 67,206.00      | 32%          | 342,050            |
| 431,050     | 640,500          | 95,686.00      | 35%          | 431,050            |
| 640,500     | And Over         | 168,993.50     | 37%          | 640,500            |

Withholding rates for taxpayers filing as *MARHR*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,550           | 0              | 0%           | 0                  |
| 12,550      | 22,500           | 0              | 10%          | 12,550             |
| 22,500      | 53,075           | 995.00         | 12%          | 22,500             |
| 53,075      | 98,925           | 4,664.00       | 22%          | 53,075             |
| 98,925      | 177,475          | 14,751.00      | 24%          | 98,925             |
| 177,475     | 221,975          | 33,603.00      | 32%          | 177,475            |
| 221,975     | 326,700          | 47,843.00      | 35%          | 221,975            |
| 326,700     | And Over         | 84,496.75      | 37%          | 326,700            |


Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,950            | 0              | 0%           | 0                  |
| 3,950       | 13,900           | 0              | 10%          | 3,950              |
| 13,900      | 44,475           | 995.00         | 12%          | 13,900             |
| 44,475      | 90,325           | 4,664.00       | 22%          | 44,475             |
| 90,325      | 168,875          | 14,751.00      | 24%          | 90,325             |
| 168,875     | 213,375          | 33,603.00      | 32%          | 168,875            |
| 213,375     | 527,550          | 47,843.00      | 35%          | 213,375            |
| 527,550     | And Over         | 157,804.25     | 37%          | 527,550            |

Withholding rates for taxpayers filing as *SGLHHR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 6,275            | 0              | 0%           | 0                  |
| 6,275       | 11,250           | 0              | 10%          | 6,275              |
| 11,250      | 26,538           | 497.50         | 12%          | 11,250             |
| 26,538      | 49,463           | 2,332.00       | 22%          | 26,538             |
| 49,463      | 88,738           | 7,375.50       | 24%          | 49,463             |
| 88,738      | 110,988          | 16,801.50      | 32%          | 88,738             |
| 110,988     | 268,075          | 23,921.50      | 35%          | 110,988            |
| 268,075     | And Over         | 78,902.13      | 37%          | 268,075            |

Withholding rates for taxpayers filing as *HOH*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,200           | 0              | 0%           | 0                  |
| 10,200      | 24,400           | 0              | 10%          | 10,200             |
| 24,400      | 64,400           | 1,420.00       | 12%          | 24,400             |
| 64,400      | 96,550           | 6,220.00       | 22%          | 64,400             |
| 96,550      | 175,100          | 13,293.00      | 24%          | 96,550             |
| 175,100     | 219,600          | 32,145.00      | 32%          | 175,100            |
| 219,600     | 533,800          | 46,385.00      | 35%          | 219,600            |
| 533,800     | And Over         | 156,355.00     | 37%          | 533,800            |

Withholding rates for taxpayers filing as *HOHHR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,400            | 0              | 0%           | 0                  |
| 9,400       | 16,500           | 0              | 10%          | 9,400              |
| 16,500      | 36,500           | 710.00         | 12%          | 16,500             |
| 36,500      | 52,575           | 3,110.00       | 22%          | 36,500             |
| 52,575      | 91,850           | 6,646.50       | 24%          | 52,575             |
| 91,850      | 114,100          | 16,072.50      | 32%          | 91,850             |
| 114,100     | 271,200          | 23,192.50      | 35%          | 114,100            |
| 271,200     | And Over         | 78,177.50      | 37%          | 271,200            |


### 2021 state or territorial tax changes

The following tax changes are included in this update:


#### Withholding changes for Arkansas

The Standard Deduction remains at \$2200
The Personal Exemption amount increased to  \$29

Tax Type rates for Filing Status NA

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,699            | 0              | 0.0%         | 0                  |
| 4,699       | 9,199            | -93.98         | 2.0%         | 0                  |
| 9,199       | 13,899           | -185.97        | 3.0%         | 0                  |
| 13,899      | 22,899           | -241.57        | 3.4%         | 0                  |
| 22,899      | 38,499           | -427.71        | 5.0%         | 0                  |
| 38,499      | 82,000           | -774.20        | 5.9%         | 0                  |
| 82,000      | 83,000           | -681.70        | 5.9%         | 0                  |
| 83,000      | 84,000           | -581.70        | 5.9%         | 0                  |
| 84,000      | 85,300           | -481.70        | 5.9%         | 0                  |
| 85,300      | 86,400           | -381.70        | 5.9%         | 0                  |
| 86,400      | 87,500           | -281.70        | 5.9%         | 0                  |
| 87,500      | And over         | -241.70        | 5.9%         | 0                  |



#### Withholding changes for Iowa

The Standard Deduction Amount for Filing Status EXP1 is \$2,130, and Filing Status EXP2 is \$5,240
Withholding rates for taxpayers filing as EXP1 and EXP2 are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,676            | 0              | 0.33%        | 0                  |
| 1,676       | 3,352            | 5.53           | 0.67%        | 1,676              |
| 3,352       | 6,704            | 16.76          | 2.25%        | 3,352              |
| 6,704       | 15,084           | 92.18          | 4.14%        | 6,704              |
| 15,804      | 25,140           | 439.11         | 5.63%        | 15,084             |
| 25,140      | 33,520           | 1,005.26       | 5.96%        | 25,140             |
| 33,520      | 50,280           | 1,504.71       | 6.25%        | 33,520             |
| 50,280      | 75,420           | 2,552.21       | 7.44%        | 50,280             |
| 75,420      |                  | 4,422.63       | 8.53%        | 75,420             |


#### Withholding changes for Kentucky

The Standard Deduction changed to \$2690 from \$2650 
The Flat Tax Rate remains at 5%


#### Withholding changes for Maine

Withholding rates for taxpayers filing as *SINGLE*, Tax table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 22,450           | 0              | 5.8%         | 0                  |
| 22,450      | 53,150           | 1,302          | 6.75%        | 22,450             |
| 53,150      | And over         | 3,374          | 7.15%        | 53,150             |

Special table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 83,850           | 0              | 0            | 9,700              |
| 83,850      | 158,850          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 44,950           |                | 5.80%        | 0                  |
| 44,950      | 106,350          | 2,607          | 6.75%        | 44,950             |
| 106,350     | And Over         | 6,752          | 7.15%        | 106,350            |

Special table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 167,600          | 0              | 0            | 22,250             |
| 167,600     | 317,700          | 150,000        | 0            | 0                  |



#### Withholding changes for Minnesota

The Personal Exemption amount is \$4,350

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,000           | 0              | 0            | 0                  |
| 12,000      | 51,810           | 0              | 5.35%        | 12,000             |
| 51,810      | 170,140          | 2,129.84       | 6.80%        | 51,810             |
| 170,140     | 288,200          | 10,176.28      | 7.85%        | 170,140            |
| 288,200     | And over         | 19,443.99      | 9.85%        | 288,200            |

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,825            | 0              | 0            | 0                  |
| 3,825       | 31,055           | 0              | 5.35%        | 3,825              |
| 31,055      | 93,265           | 1,456.81       | 6.80%        | 31,055             |
| 93,265      | 169,865          | 5,687.09       | 7.85%        | 93,265             |
| 169,865     | And over         | 11,700.19      | 9.85%        | 169,865            |


#### Withholding changes for Mississippi

No changes to Personal Exempptions or Standard Deductions

Withholding rates for taxpayers filing as HOH, MAR1, MAR2 and SINGLE are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,000            | 0              | 0            | 0                  |
| 4,000       | 5,000            | 0              | 3%           | 4,000              |
| 5,000       | 10,000           | 30             | 4%           | 5,000              |
| 10,000      | And over         | 230            | 5%           | 10,000             |


#### Withholding changes for Missouri

The Standard Deduction is \$18,800 for filing status HOH
The Standard Deduction is \$25,100 for filing status MAR1
The Standard Deduction is \$12,550 for filing status MAR2 and SINGLE

Withholding rates for all filing status remain the same.

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,073            | 0              | 1.5%         | 0                  |
| 1,073       | 2,146            | 16.00          | 2.0%         | 1.073              |
| 2,146       | 3,219            | 37.00          | 2.5%         | 2,146              |
| 3,219       | 4,292            | 64.00          | 3.0%         | 3,219              |
| 4,292       | 5,365            | 96.00          | 3.5%         | 4,292              |
| 5,365       | 6,438            | 134.00         | 4.0%         | 5,365              |
| 6,438       | 7,511            | 177.00         | 4.50%        | 6,438              |
| 7,511       | 8,584            | 225.00         | 5.0%         | 7,511              |
| 8,584       | And over         | 279.00         | 5.4%         | 8,584              |



#### Withholding changes for North Dakota

The Personal Exemption amount is \$4,300 for Filing Status MAR and SINGLE 

***Per the state of North Dakota, there is no HOH filing status with exemptions.  If an employee on the W4 chooses 
Filing status of HOH and does not mark step 2, you still choose HOH as the filing status in Dynamics GP.***

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,750           | 0              | 0            | 0                  |
| 12,750      | 46,600           | 0              | 1.10%        | 12,750             |
| 46,600      | 94,525           | 372.35         | 2.04%        | 46,600             |
| 94,525      | 137,325          | 1,350.02       | 2.27%        | 94,525             |
| 137,325     | 235,250          | 2,321.58       | 2.64%        | 137,325            |
| 235,250     | And over         | 4,906.80       | 2.90%        | 235,250            |

Withholding rates for taxpayers filing as *MARHR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,550           | 0              | 0            | 0                  |
| 12,550      | 46,400           | 0              | 1.10%        | 12,550             |
| 46,400      | 94,325           | 372.35         | 2.04%        | 46,400             |
| 94,325      | 137,125          | 1,350.02       | 2.27%        | 94,325             |
| 137,125     | 235,050          | 2,321.58       | 2.64%        | 137,125            |
| 235,050     | And over         | 4,906.80       | 2.90%        | 235,050            |


Withholding rates for taxpayers filing as *SINGLE* and *SINGHR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 6,275            | 0              | 0            | 0                  |
| 6,275       | 46,800           | 0              | 1.10%        | 6,275              |
| 46,800      | 104,375          | 445.78         | 2.04%        | 46,800             |
| 104,375     | 210,950          | 1,620.31       | 2.27%        | 104,375            |
| 210,950     | 451,275          | 4,039.56       | 2.64%        | 210,950            |
| 451,275     | And over         | 10,384.14      | 2.90%        | 451,275            |

Withholding rates for taxpayers filing as *HOHHR* 

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,400            | 0              | 0            | 0                  |
| 9,400       | 63,700           | 0              | 1.10%        | 9,400              |
| 63,700      | 149,600          | 597.30         | 2.04%        | 63,700             |
| 149,600     | 236,350          | 2,349.66       | 2.27%        | 149,600            |
| 236,350     | 454,400          | 4,318.89       | 2.64%        | 236,350            |
| 454,400     | And over         | 10,075.41      | 2.90%        | 454,400            |


#### Withholding changes for South Carolina

The Personal Exemption is $2,670 for Filing Status ONE.
The Standard Deduction Maximum is $4,200 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,800            | 0              | 0.5%         | 0                  |
| 2,800       | 5,610            | -70.00         | 3.0%         | 0                  |
| 5,610       | 8,410            | -126.10        | 4.0%         | 0                  |
| 8,410       | 11,220           | -210.20        | 5.0%         | 0                  |
| 11,220      | 14,030           | -322.40        | 6.0%         | 0                  |
| 14,030      | And over         | -462.70        | 7.0%         | 0                  |

## Resources to assist you

If you have questions about U.S. Payroll tax updates and your Microsoft Partner isn’t available, there are several resources, in addition to this document, to assist in answering your questions.

### U.S. Payroll Tax Updates on CustomerSource

Take a look at [CustomerSource](https://mbs.microsoft.com/customersource/support/downloads/taxupdates/) to find out the tax changes included in each update and to download the update. All instructions for downloading and installing the tax updates also are provided here.

### Knowledge Base

[https://mbs.microsoft.com/knowledgebase/search.aspx](https://mbs.microsoft.com/knowledgebase/search.aspx) provides you with instant access to the same database our support engineers use. You can find answers to common questions, along with technical tips and performance recommendations.

### eSupport

For support requests that can be handled with email, go to [https://support.microsoft.com/supportforbusiness](https://support.microsoft.com/supportforbusiness). On average, the response time is nearly twice as fast as telephone support.

### Discussion

On the [Dynamics GP community site](https://community.dynamics.com/gp), you can start a tax update discussion with other members of the Microsoft customer community. This database provides you with the opportunity to exchange information with other customers, which is perfect for providing tips and answers to questions about tax updates.

### Microsoft Business Solutions Human Resources/Payroll support team

We have a support team focused 100 percent on providing service and support to our Payroll customers. If you have questions, dial toll free 888-GPS-SUPP (888-477-7877).

## Preparing for installation

Use the instructions in this section to prepare for the U.S. Payroll Tax Update. For detailed information about the changes in the current tax update round, see *Changes in this update*.

### Are you using a supported version?

To identify the version, you’re using, start Microsoft Dynamics GP. Choose Help\>\> About Microsoft Dynamics GP. The information window displays the version number in the lower right corner.

This U.S. Payroll Tax Update is supported for Microsoft Dynamics GP and Microsoft Dynamics GP 2016 on Microsoft SQL Server.

If you’re not using one of the supported versions, you must upgrade to a supported version before installing this tax update.

### Have you obtained the update files?

If your computer is connected to the Internet, the Payroll Update Utility (PUE) automatically can download the tax table update file (TX.cab) from the Internet.

If your computer isn’t connected to the Internet, you can obtain the file from [CustomerSource](https://mbs.microsoft.com/customersource/northamerica/GP/downloads) or your Microsoft Partner and copy it to your computer before running what’s known as a “manual” installation.

Tax updates are distributed in the form of .CAB files. Copy the .CAB file to a folder that you can readily access, such as the folder that contains Dynamics.exe. Copying the .CAB file to your computer does not complete the installation. Refer to the following section for instructions on how to install the tax update.

## Installing the tax update

The Round 1 2021 tax update installation can be run from any workstation. The update installs payroll tax table data on the server computer where your existing Microsoft Dynamics GP application data is located. You need to install the tax table update only once.

If you have issues installing the update, review the article on [Tips to install the U.S. Payroll Tax
Update.](https://community.dynamics.com/gp/b/dynamicsgp/archive/2017/05/09/tips-to-install-the-u-s-payroll-tax-update)

Before you begin, ask all Microsoft Dynamics GP users to exit the application until the update is complete. Exit all other applications, turn off the screen saver, and back up important data (including Forms.dic, Reports.dic, and Dynamics.vba if they exist) before you proceed with the installation.

1. Log onto Microsoft Dynamics GP with the system administrator rights, (user SA) and open the Payroll Tax Update window.
    (Microsoft Dynamics GP menu \>\> Maintenance \>\> U.S. Payroll Updates \>\> Check for Tax Updates)

2. Select an update method, and then choose Next.

    ![A screenshot](media/a6b6f3f85d529f49182c1e66d23df8b5.jpg)

    - The Automatic option downloads the current tax table update from the Internet to the default location. An Internet connection is required.
    - The Manual option processes the tax table update from a location you choose. You might choose Manual if you need to update a computer that isn’t connected to the Internet. To use this method, you should already have obtained the tax table update file, TX.cab, and copied it to a location your computer can readily access.

3. If you selected Automatic, enter your 10-digit authorized telephone number. Choose Log in to start the download.

    If you selected Manual, specify the location where the tax table update file is located.

4. Choose Process to start the update.

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *12/18/2020*.

## What’s next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
