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
ms.date: 12/6/2021
---
# U.S. 2022 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2022 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

The first tax update for 2022 replaces all previous tax updates. It includes state and federal tax table changes that take effect January 1, 2022. We recommend that you install this update as soon as you can for the year 2022.

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.


## Changes in January Round 1 update (Target Release 12/17/2021)

- Federal changes and FICA Social Security Limit $147,000
- California
- Georgia
- Iowa
- Maine
- Nebraska
- New Mexica
- New York
- Oklahoma
- South Carolina
- Yonkers



### 2022 Federal tax changes

The maximum taxable earnings for Social Security increase in 2022 to \$147,000 from \$142,800 

The Personal Exemption is $4,300 for SINGLE, MAR, HOH

Withholding rates for taxpayers filing as *NRA*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,200           | 0              | 0%           | 0                  |
| 12,200      | 22,150           | 0              | 10%          | 12,200             |
| 22,150      | 52,725           | 995.00         | 12%          | 22,150             |
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


### 2022 state or territorial tax changes

The following tax changes are included in this update:

#### Withholding changes for California

For Filing Status of HOH and MAR2:
•	Personal Exemption is $141.90 from $136.40
•	Standard Deduction is $9,606  from $9,202
•	Low Income Limit is $31,831 from $30,534

For Filing Status of MAR1 and SINGLE:
•	Personal Exemption is $141.90 from $136.40
•	Standard Deduction is $4,803 from $4,601
•	Low Income Limit is $15,916 from $15,267


Withholding rates for taxpayers filing as *HOH*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 18,663           | 0              | 1.1%         | 0                  |
| 18,663      | 44,217           | 205.29         | 2.2%         | 18,663             |
| 44,217      | 56,999           | 767.48         | 4.4%         | 44,217             |
| 56,999      | 70,542           | 1,329.89       | 6.6%         | 56,999             |
| 70,542      | 83,324           | 2,223.73       | 8.8%         | 70,542             |
| 83,324      | 425,251          | 3,348.55       | 10.23%       | 83,324             |
| 425,251     | 510,303          | 38,327.68      | 11.33%       | 425,251            | 
| 510,303     | 850,503          | 47,964.07      | 12.43%       | 510,303            |
| 850,503     | 1,000,000        | 90,250.93      | 13.53%       | 850,503            |
| 1,000,000   | And Over         | 110,477.87     | 14.63%       | 1,000,000          |

Withholding rates for taxpayers filing as *MAR1* and *MAR2*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 18,650           | 0              | 1.1%         | 0                  |
| 18,650      | 44,214           | 205.15         | 2.2%         | 18,650             |
| 44,214      | 69,784           | 767.56         | 4.4%         | 44,214             |
| 69,784      | 96,870           | 1,892.64       | 6.6%         | 69,784             |
| 96,870      | 122,428          | 3,680.32       | 8.8%         | 96,870             |
| 122,428     | 625,372          | 5,929.42       | 10.23%       | 122,428            |
| 625,372     | 750,442          | 57,380.59      | 11.33%       | 625,372            | 
| 750,442     | 1,000,000        | 71,551.02      | 12.43%       | 750,442            |
| 1,000,000   | 1,250,738        | 102,571.08     | 13.53%       | 1,000,000          |
| 1,250,738   | And Over         | 136,495.93     | 14.63%       | 1,250,738         |

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     | 
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,325            | 0              | 1.1%         | 0                  |
| 9,325       | 22,107           | 102.58         | 2.2%         | 9,325              |
| 22,107      | 34,892           | 383.78         | 4.4%         | 22,107             |
| 34,892      | 48,435           | 946.32         | 6.6%         | 34,892             |
| 48,435      | 61,214           | 1,840.16       | 8.8%         | 48,435             |
| 61,214      | 312,686          | 2,964.71       | 10.23%       | 61,214             |
| 312,686     | 375,221          | 28,690.30      | 11.33%       | 312,686            |
| 375,221     | 625,369          | 35,775.52      | 12.43%       | 375,221            |
| 625,369     | 1,000,000        | 66,868.92      | 13.53%       | 625,369            |
| 1,000,000   | And Over         | 117,556.49     | 14.63%       | 1,000,000          |


#### Withholding changes for Georgia

The Standard Deduction Amount for Filing Status:
HOH and SINGLE     is \$5,400
MFJ1I              is \$7,100
MFJ2I and MFS      is \$3,550


#### Withholding changes for Iowa

The Standard Deduction Amount for Filing Status EXP1 is \$2,210, and Filing Status EXP2 is \$5,450
Withholding rates for taxpayers filing as EXP1 and EXP2 are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,743            | 0              | 0.33%        | 0                  |
| 1,743       | 3,486            | 5.75           | 0.67%        | 1,743              |
| 3,486       | 6,972            | 17.43          | 2.25%        | 3,486              |
| 6,972       | 15,687           | 95.87          | 4.14%        | 6,972              |
| 15,687      | 26,145           | 456.67         | 5.63%        | 15,687             |
| 26,145      | 34,860           | 1,045.46       | 5.96%        | 26,145             |
| 34,860      | 52,290           | 1,564.87       | 6.25%        | 34,860             |
| 52,290      | 78,435           | 2,654.25       | 7.44%        | 52,290             |
| 78,435      |                  | 4,599.44       | 8.53%        | 78,435             |


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

If you have questions about U.S. Payroll tax updates and your Microsoft Partner isn't available, there are several resources, in addition to this document, to assist in answering your questions.

### U.S. Payroll Tax Updates

Take a look at [this location](/dynamics/s-e/gp/tugp2018_391) to find out the tax changes included in each update and to download the update. All instructions for downloading and installing the tax updates also are provided here.


### eSupport

For support requests that can be handled with email, go to [https://support.microsoft.com/supportforbusiness](https://support.microsoft.com/supportforbusiness). On average, the response time is nearly twice as fast as telephone support.

### Discussion

On the [Dynamics GP community site](https://community.dynamics.com/gp), you can start a tax update discussion with other members of the Microsoft customer community. This database provides you with the opportunity to exchange information with other customers, which is perfect for providing tips and answers to questions about tax updates.

### Microsoft Business Solutions Human Resources/Payroll support team

We have a support team focused 100 percent on providing service and support to our Payroll customers. If you have questions, dial toll free 888-GPS-SUPP (888-477-7877).

## Preparing for installation

Use the instructions in this section to prepare for the U.S. Payroll Tax Update. For detailed information about the changes in the current tax update round, see *Changes in this update*.

### Are you using a supported version?

To identify the version, you're using, start Microsoft Dynamics GP. Choose Help\>\> About Microsoft Dynamics GP. The information window displays the version number in the lower right corner.

This U.S. Payroll Tax Update is supported for Microsoft Dynamics GP on Microsoft SQL Server.

If you're not using one of the supported versions, you must upgrade to a supported version before installing this tax update.

### Have you obtained the update files?

If your computer is connected to the Internet, the Payroll Update Utility (PUE) automatically can download the tax table update file (TX.cab) from the Internet.

If your computer isn't connected to the Internet, you can obtain the file from [Dynamics GP Downloads](/dynamics/s-e/gp/mdgp2018_release_download_378) or your Microsoft Partner and copy it to your computer before running what's known as a "manual" installation.

Tax updates are distributed in the form of .CAB files. Copy the .CAB file to a folder that you can readily access, such as the folder that contains Dynamics.exe. Copying the .CAB file to your computer does not complete the installation. Refer to the following section for instructions on how to install the tax update.

## Installing the tax update

The Round 1 2022 tax update installation can be run from any workstation. The update installs payroll tax table data on the server computer where your existing Microsoft Dynamics GP application data is located. You need to install the tax table update only once.

If you have issues installing the update, review the article on [Tips to install the U.S. Payroll Tax
Update.](https://community.dynamics.com/gp/b/dynamicsgp/archive/2017/05/09/tips-to-install-the-u-s-payroll-tax-update)

Before you begin, ask all Microsoft Dynamics GP users to exit the application until the update is complete. Exit all other applications, turn off the screen saver, and back up important data (including Forms.dic, Reports.dic, and Dynamics.vba if they exist) before you proceed with the installation.

1. Log onto Microsoft Dynamics GP with the system administrator rights, (user SA) and open the Payroll Tax Update window.
    (Microsoft Dynamics GP menu \>\> Maintenance \>\> U.S. Payroll Updates \>\> Check for Tax Updates)

2. Select an update method, and then choose Next.

    ![A screenshot](media/a6b6f3f85d529f49182c1e66d23df8b5.jpg)

    - The Automatic option downloads the current tax table update from the Internet to the default location. An Internet connection is required.
    - The Manual option processes the tax table update from a location you choose. You might choose Manual if you need to update a computer that isn't connected to the Internet. To use this method, you should already have obtained the tax table update file, TX.cab, and copied it to a location your computer can readily access.

3. If you selected Automatic, enter your 10-digit authorized telephone number. Choose Log in to start the download.

    If you selected Manual, specify the location where the tax table update file is located.

4. Choose Process to start the update.

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *12/17/2021*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
