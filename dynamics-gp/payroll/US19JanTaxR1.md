---
title: "US payroll tax update"
description: "US 2023 Payroll Tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 12/14/2023
---
# U.S. 2024 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2024 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

This is the first tax update for 2024 and replaces all previous tax updates. It includes State tax table changes that take effect January 1, 2024. 

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

Check out these blogs for detailed documentation on how you calculate payroll taxes in Microsoft Dynamics GP:

[How to calculate Federal Tax with Dependent Claim Amount Field](https://community.dynamics.com/gp/b/dynamicsgp/posts/how-to-calculate-federal-tax-with-dependent-claim-amount)

[Does Microsoft Dynamics GP calculate tax correctly?](https://community.dynamics.com/gp/b/dynamicsgp/posts/is-microsoft-dynamics-gp-calculating-payroll-taxes-correctly)

[Tips to install the U.S. Payroll Tax Update](https://community.dynamics.com/gp/b/dynamicsgp/posts/tips-to-install-the-u-s-payroll-tax-update)


## Changes in January Round 1 update (Target Release: 12/21/2023)

- FICA Social Security Limit 168,600 (Previously $160,200)
- Federal tax
- Arkansas
- California
- Colorado
- Connecticut
- Iowa
- Kentucky
- Maine
- Michigan
- Missouri
- Montana
- Nebraska
- New Mexico
- North Carolina
- Oregon
- Rhode Island
- South Carolina

### Withholding changes for Arkansas

> [!NOTE]
> If you have employees set up to withhold Arkansas state tax, you need to be on version 18.5.1635 or later, for taxes to be correct for the year 2024. 
This change is for the Midrange Income look up part of the tax calculation.
> 
Standard Deduction Amount is $2,340 from $2,270
Personal Exemption remains at $29.00

Tax Type rates for Filing Status NA

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,299            | 0              | 0.0%         | 0                  |
| 5,299       | 10,599           | -101.98        | 2.0%         | 0                  |
| 10,599      | 15,099           | -204.97        | 3.0%         | 0                  |
| 15,099      | 24,999           | -263.77        | 3.4%         | 0                  |
| 24,999      | 89,600           | -579.65        | 4.4%         | 0                  |
| 89,600      | 89,700           | -579.60        | 4.4%         | 0                  |
| 89,700      | 89,800           | -569.60        | 4.4%         | 0                  |
| 89,800      | 89,900           | -559.60        | 4.4%         | 0                  |
| 89,300      | 89,400           | -549.60        | 4.4%         | 0                  |
| 89,400      | 89,500           | -539.60        | 4.4%         | 0                  |
| 89,500      | 89,600           | -529.60        | 4.4%         | 0                  |
| 89,600      | 89,700           | -519.60        | 4.4%         | 0                  |
| 89,700      | 89,800           | -509.60        | 4.4%         | 0                  |
| 89,800      | 89,900           | -499.60        | 4.4%         | 0                  |
| 89,900      | 90,000           | -489.60        | 4.4%         | 0                  |
| 90,000      | 90,200           | -479.60        | 4.4%         | 0                  |
| 90,200      | 90,300           | -469.60        | 4.4%         | 0                  |
| 90,300      | 90,400           | -459.60        | 4.4%         | 0                  |
| 90,400      | 90,500           | -449.60        | 4.4%         | 0                  |
| 90,500      | 90,600           | -439.60        | 4.4%         | 0                  |
| 90,600      | 90,700           | -429.60        | 4.4%         | 0                  |
| 90,700      | 90,800           | -419.60        | 4.4%         | 0                  |
| 90,800      | 90,900           | -409.60        | 4.4%         | 0                  |
| 90,900      | 91,100           | -399.60        | 4.4%         | 0                  |
| 91,100      | 91,200           | -389.60        | 4.4%         | 0                  |
| 91,200      | 91,300           | -379.60        | 4.4%         | 0                  |
| 91,300      | 91,400           | -369.60        | 4.4%         | 0                  |
| 91,400      | 91,500           | -359.60        | 4.4%         | 0                  |
| 91,500      | 91,600           | -349.60        | 4.4%         | 0                  |
| 91,600      | 91,700           | -339.60        | 4.4%         | 0                  |
| 91,700      | 91,800           | -329.60        | 4.4%         | 0                  |
| 91,800      | 91,900           | -319.60        | 4.4%         | 0                  |
| 91,900      | 92,000           | -309.60        | 4.4%         | 0                  |
| 92,000      | 92,100           | -299.60        | 4.4%         | 0                  |
| 92,100      | 92,200           | -289.60        | 4.4%         | 0                  |
| 92,200      | 92,300           | -279.60        | 4.4%         | 0                  |
| 92,300      | 92,400           | -269.60        | 4.4%         | 0                  |
| 92,400      | 92,500           | -259.60        | 4.4%         | 0                  |
| 92,500      | 92,600           | -249.60        | 4.4%         | 0                  |
| 92,600      | 92,700           | -239.60        | 4.4%         | 0                  |
| 92,700      | 92,800           | -229.60        | 4.4%         | 0                  |
| 92,800      | 92,900           | -219.60        | 4.4%         | 0                  |
| 92,900      | 93,000           | -209.60        | 4.4%         | 0                  |
| 93,000      | 93,100           | -199.60        | 4.4%         | 0                  |
| 93,100      | 93,200           | -189.60        | 4.4%         | 0                  |
| 93,200      | 93,300           | -179.60        | 4.4%         | 0                  |
| 93,300      | 93,400           | -169.60        | 4.4%         | 0                  |
| 93,400      | 93,500           | -159.60        | 4.4%         | 0                  |
| 93,500      | 93,600           | -159.60        | 4.4%         | 0                  |
| 93,600      | 100,000          | -159.60        | 4.4%         | 0                  |
| 100,000     | And Over         | -159.60        | 4.4%         | 0                  |

Tax Type Special for Filing Status NA added

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over                     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 100,001          | 0              | 0%           | 50                 |


### Withholding changes for California

For Filing Status of HOH and MAR2:  

- Personal Exemption is $158.40 from $154.00
- Standard Deduction is $10,726 from $10,404
- Low Income Limit is $35,538 from $34,503 

For Filing Status of MAR1 and SINGLE:

- Personal Exemption is $158.40 from $154.00
- Standard Deduction is $5,363 from $5,202
- Low Income Limit is $17,769 from $17,252

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over                  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 20,839           | 0              | 1.1%         | 0                  |
| 20,839      | 49,371           | 229.23         | 2.2%         | 20,839             |
| 49,371      | 63,644           | 856.93         | 4.4%         | 49,371             |
| 63,644      | 78,765           | 1,484.94       | 6.6%         | 63,644             |
| 78,765      | 93,037           | 2,482.93       | 8.8%         | 78,765             |
| 93,037      | 474,824          | 3,738.87       | 10.23%       | 93,037             |
| 474,824     | 569,790          | 42,795.68      | 11.33%       | 474,824            |
| 569,790     | 949,649          | 53,555.33      | 13.53%       | 569,790            |
| 949,649     | 1,000,000        | 100,771.80     | 13.53%       | 949,649            |
| 1,000,000   | And Over         | 107,583.29     | 14.63%       | 1,000,000          |

Withholding rates for taxpayers filing as *MAR1* and *MAR2*

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 20,824           | 0              | 1.1%         | 0                  |
| 20,824      | 49,368           | 229.06         | 2.2%         | 20,824             |
| 49,368      | 77,918           | 857.03         | 4.4%         | 49,368             |
| 77,918      | 108,162          | 2,113.23       | 6.6%         | 77,918             |
| 108,162     | 136,700          | 4,109.33       | 8.8%         | 108,162            |
| 136,700     | 698,274          | 6,620.67       | 10.23%       | 136,700            |
| 698,274     | 837,922          | 64,069.69      | 11.33%       | 698,274            |
| 837,922     | 1,000,000        | 79,891.81      | 12.43%       | 837,922            |
| 1,000,000   | 1,396,542        | 100,038.11     | 13.53%       | 1,000,000          |
| 1,396,542   | And Over         | 153,690.24     | 14.63%       | 1,396,542          |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over  | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over                 |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,412           | 0              | 1.1%         | 0                  |
| 10,412      | 24,684           | 114.53         | 2.2%         | 10,412             |
| 24,684      | 38,959           | 428.51         | 4.4%         | 24,684             |
| 38,959      | 54,081           | 1,056.61       | 6.6%         | 38,959             |
| 54,081      | 68,350           | 2,054.66       | 8.8%         | 54,081             |
| 68,350      | 349,137          | 3,310.33       | 10.23%       | 68,350             |
| 349,137     | 418,961          | 32,034.84      | 11.33%       | 349,137            |
| 418,961     | 698,271          | 39,945.90      | 12.43%       | 418,961            |
| 698,271     | 1,000,000        | 74,644.13      | 13.53%       | 698,271            |
| 1,000,000   | And Over         | 115,488.06     | 14.63%       | 1,000,000          |

#### Withholding changes for Colorado

All filing status have the same fixed flat tax of 4.40% was 4.55%(2022)

The Personal Exemption amount is $9,000 for MAR
The Personal Exemption amount is $4,500 For SINGLE

**The following new filing status were added January 2022:**

- HOH1J - Head of Household 1 Job - Exemption amount  $19,500  
- MAR1J - Married Filing Jointly 1 Job - Exemption amount  $27,000  
- SIN1J - Single/Mar filing Single 1 Job - Exemption amount  $12,500  

In January 2022 the state of Colorado released a new form called [DR-0004](https://tax.colorado.gov/withholding-forms) this is optional for an employee to complete.  

There are 2 other parts to this form that have many different exemption amounts, we cannot accommodate all of them in the tax tables.
A new “OTHER” filing status was added (OTH1J) with Exemption increments of $500 that will accommodate all the "other" amounts on the form if an employee enters. 

OTH1J - OTH, +1 Jobs or Child Cr Allow - Exemption amount of $500

As an example, lets say I fill out the form and choose an amount of 2500 – it does not match any of the above filing status so I would pick the OTHER status and put a 5 under Cards | Payroll | State Tax in the Number of Dependents field OR Additional Allowances. Which is 2500/500 = 5.

Another example, I put 5500 on the form. Again, that does not match the other filing status, so I choose *Other* and put *11*.


## Resources to assist you

If you have questions about U.S. Payroll tax updates and your Microsoft Partner isn't available, there are several resources, in addition to this document, to assist in answering your questions.

### U.S. Payroll Tax Updates

Take a look at [this location](/dynamics/s-e/gp/tugp2018_391) to find out the tax changes included in each update and to download the update. All instructions for downloading and installing the tax updates also are provided here.

### Discussion

On the [Dynamics GP community site](https://community.dynamics.com/gp), you can start a tax update discussion with other members of the Microsoft customer community. This database provides you with the opportunity to exchange information with other customers, which is perfect for providing tips and answers to questions about tax updates.

## Preparing for installation

Use the instructions in this section to prepare for the U.S. Payroll Tax Update. For detailed information about the changes in the current tax update round, see *Changes in this update*.

### Are you using a supported version?

To identify the version, you're using, start Microsoft Dynamics GP. Choose Help\>\> About Microsoft Dynamics GP. The information window displays the version number in the lower right corner.

This U.S. Payroll Tax Update is supported for Microsoft Dynamics GP on Microsoft SQL Server.

If you're not using one of the supported versions, you must upgrade to a supported version before installing this tax update.

### Have you obtained the update files?

If your computer is connected to the Internet, the Payroll Update Utility (PUE) automatically can download the tax table update file (TX.cab) from the Internet.

If your computer isn't connected to the Internet, you can obtain the file from [Dynamics GP Downloads](/dynamics/s-e/gp/tugp2018_391) or your Microsoft Partner and copy it to your computer before running what's known as a "manual" installation.

Tax updates are distributed in the form of .CAB files. Copy the .CAB file to a folder that you can readily access, such as the folder that contains Dynamics.exe. Copying the .CAB file to your computer does not complete the installation. Refer to the following section for instructions on how to install the tax update.

## Installing the tax update

The tax update installation can be run from any workstation. The update installs payroll tax table data on the server computer where your existing Microsoft Dynamics GP application data is located. You need to install the tax table update only once.

If you have issues installing the update, review the article on [Tips to install the U.S. Payroll Tax
Update.](https://community.dynamics.com/gp/b/dynamicsgp/archive/2017/05/09/tips-to-install-the-u-s-payroll-tax-update)

Before you begin, ask all Microsoft Dynamics GP users to exit the application until the update is complete. Exit all other applications, turn off the screen saver, and back up important data (including Forms.dic, Reports.dic, and Dynamics.vba if they exist) before you proceed with the installation.

1. Log onto Microsoft Dynamics GP with the system administrator rights, (user SA) and open the Payroll Tax Update window.
    (Microsoft Dynamics GP menu \>\> Maintenance \>\> U.S. Payroll Updates \>\> Check for Tax Updates)

2. Select an update method, and then choose Next.

    ![A screenshot](media/a6b6f3f85d529f49182c1e66d23df8b5.jpg)

    - The Automatic option downloads the current tax table update from the Internet to the default location. An Internet connection is required.
    - The Manual option processes the tax table update from a location you choose. You might choose Manual if you need to update a computer that isn't connected to the Internet. To use this method, you should already have obtained the tax table update file, [TX.cab](/dynamics/s-e/gp/tugp2018_391), and copied it to a location your computer can readily access.

3. If you selected Automatic, enter your 10-digit authorized telephone number. Choose Log in to start the download.

    If you selected Manual, specify the location where the tax table update file is located.

4. Choose Process to start the update.

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *12/20/2023*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
