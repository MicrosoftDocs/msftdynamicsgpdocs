---
title: "US payroll tax update"
description: "US 2022 January payroll tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 12/19/2022
---
# U.S. 2022 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2023 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

This is the first tax update for 2023 and replaces all previous tax updates. It includes Federal and State tax table changes that take effect January 1, 2023. We recommend that you install this update as soon as you can for the year 2023.

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

Check out these blogs for detailed documentation on how you calculate payroll taxes in Microsoft Dynamics GP:

[How to calculate Federal Tax with Dependent Claim Amount Field](https://community.dynamics.com/gp/b/dynamicsgp/posts/how-to-calculate-federal-tax-with-dependent-claim-amount)

[Does Microsoft Dynamics GP calculate tax correctly?](https://community.dynamics.com/gp/b/dynamicsgp/posts/is-microsoft-dynamics-gp-calculating-payroll-taxes-correctly)

[Tips to install the U.S. Payroll Tax Update](https://community.dynamics.com/gp/b/dynamicsgp/posts/tips-to-install-the-u-s-payroll-tax-update)

## Changes in January Round 1 update (Released: )

- FICA Social Security Limit $160,200
- Federal tax tables added 12/30/2021
- Arizona
- California
- Iowa
- Kentucky
- 
- Maine
- Minnesota
- Mississippi
- Missouri
- Montana
- Nebraska
- New Mexico
- New York
- South Carolina
- Yonkers

### 2023 Federal tax changes

The maximum taxable earnings for Social Security increase in 2023 to \$160,200 from \$147,000. 

**Federal tax tables released 12/18/2022**

The Personal Exemption is $4,300 for SINGLE, MAR, HOH, NRA

Withholding rates for taxpayers filing as *NRA*

> [!NOTE]
> For non-resident aliens, if the employee filled out a W-4 after 01/01/2020, the filing status *Non Resident Alien HR (NRAHR)* must always be used.

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 14,800          | 0             | 0%          | 0                 |
| 14,800     | 25,800          | 0             | 10%         | 14,800            |
| 25,800     | 59,525          | 1,100.00      | 12%         | 25,800            |
| 59,525     | 110,175         | 5,147.00      | 22%         | 59,525            |
| 110,175    | 196,900         | 16,290.00     | 24%         | 110,175           |
| 196,900    | 246,050         | 37,104.00     | 32%         | 196,900           |
| 246,050    | 592,925         | 52,832.00     | 35%         | 246,050           |
| 592,925    | And Over        | 174,238.25    | 37%         | 592,925           |

Withholding rates for taxpayers filing as *NRAHR*

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|             | 20,775           | 0              | 0%           | 0                  |
| 20,775      | 26,275           | 0              | 10%          | 20,775             |
| 26,275      | 43,138           | 550.00         | 12%          | 26,275             |
| 43,138      | 68,463           | 2,573.00       | 22%          | 43,138             |
| 68,463      | 111,825          | 8,145.00       | 24%          | 68,463             |
| 111,825     | 136,400          | 18,552.00      | 32%          | 111,825            |
| 136,400     | 309,838          | 26,416.00      | 35%          | 136,400            |
| 309,838     | And Over         | 87,119.13      | 37%          | 309,838            |


Withholding rates for taxpayers filing as *MAR*

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 14,800          | 0             | 0%          | 0                 |
| 14,800     | 36,800          | 0             | 10%         | 14,800            |
| 36,800     | 104,250         | 2,200.00      | 12%         | 36,800            |
| 104,250    | 205,550         | 10,294.00     | 22%         | 104,250           |
| 205,550    | 379,000         | 32,580.00     | 24%         | 205,550           |
| 379,000    | 477,300         | 74,208.00     | 32%         | 379,000           |
| 477,300    | 708,550         | 105,664.00    | 35%         | 477,300           |
| 708,550    | And Over        | 186,601.50    | 37%         | 708,550           |

Withholding rates for taxpayers filing as *MARHR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 13,850           | 0              | 0%           | 0                  |
| 13,850      | 24,850           | 0              | 10%          | 13,850             |
| 24,850      | 58,575           | 1,100.00       | 12%          | 24,850             |
| 58,575      | 109,225          | 5,147.00       | 22%          | 58,575             |
| 109,225     | 195,950          | 16,290.00      | 24%          | 109,225            |
| 195,950     | 245,100          | 37,104.00      | 32%          | 195,950            |
| 245,100     | 360,725          | 52,832.00      | 35%          | 245,100            |
| 360,725     | And Over         | 93,300.75      | 37%          | 360,725            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 5,250        | 0          | 0%       | 0              |
| 5,250   | 16,250       | 0          | 10%      | 5,250          |
| 16,250  | 49,975       | 1,100.00   | 12%      | 16,250         |
| 49,975  | 100,625      | 5,147.00   | 22%      | 49,975         |
| 100,625 | 187,350      | 16,290.00  | 24%      | 100,625        |
| 187,350 | 236,500      | 37,104.00  | 32%      | 187,350        |
| 236,500 | 583,375      | 52,832.00  | 35%      | 236,500        |
| 583,375 | And Over     | 174,238.25 | 37%      | 583,375        |

Withholding rates for taxpayers filing as *SGLHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over |
|-------------|------------------|----------------|----------|----------------|
| 0           | 6,925            | 0              | 0%       | 0              |
| 6,925       | 12,425           | 0              | 10%      | 6,925          |
| 12,425      | 29,288           | 550.00         | 12%      | 12,425         |
| 29,288      | 54,613           | 2,573.50       | 22%      | 29,288         |
| 54,613      | 97,975           | 8,145.00       | 24%      | 54,613         |
| 97,975      | 122,550          | 18,552.00      | 32%      | 97,975         |
| 122,550     | 295,988          | 26,416.00      | 35%      | 122,550        |
| 295,988     | And Over         | 87,119.13      | 37%      | 295,988        |

Withholding rates for taxpayers filing as *HOH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over    |
|-------------|------------------|----------------|----------|-------------------|
| 0           | 12,200           | 0              | 0%       | 0                 |
| 12,200      | 27,900           | 0              | 10%      | 12,200            |
| 27,900      | 72,050           | 1,570.00       | 12%      | 27,900            |
| 72,050      | 107,550          | 6,868.00       | 22%      | 72,050            |
| 107,550     | 194,300          | 14,678.00      | 24%      | 107,550           |
| 194,300     | 243,450          | 35,498.00      | 32%      | 194,300           |
| 243,450     | 590,300          | 51,226.00      | 35%      | 243,450           |
| 590,300     | And Over         | 172,623.50     | 37%      | 590,300           |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 10,400           | 0              | 0%       | 0                  |
| 10,400      | 18,250           | 0              | 10%      | 10,400             |
| 18,250      | 40,325           | 785.00         | 12%      | 18,250             |
| 40,325      | 58,075           | 3,434.00       | 22%      | 40,325             |
| 58,075      | 101,450          | 7,339.00       | 24%      | 58,075             |
| 101,450     | 126,025          | 17,749.00      | 32%      | 101,450            |
| 126,025     | 299,450          | 25,613.00      | 35%      | 126,025            |
| 299,450     | And Over         | 86,311.75      | 37%      | 299,450            |



### 2023 state or territorial tax changes
The following tax changes are included in this update:

#### Withholding changes for Arizona

Decrease in flat tax rates for all filing status.

FS01A -  .5% Flat Tax Rate from .8%
FS02  - 1.0% Flat Tax Rate from 1.3%
FS03  - 1.5% Flat Tax Rate from 1.8%
FS04  - 2.0% Flat Tax Rate from 2.7%
FS05  - 2.5% Flat Tax Rate from 3.6%
FS06  - 3.0% Flat Tax Rate from 4.2%
FS07  - 3.5% Flat Tax Rate from 5.1%

#### Withholding changes for California

For Filing Status of HOH and MAR2:  

- Personal Exemption is $154.00 from $141.90
- Standard Deduction is $10,404  from $9,606
- Low Income Limit is $34,503 from $31,831

For Filing Status of MAR1 and SINGLE:

- Personal Exemption is $154.00 from $141.90
- Standard Deduction is $5,202 from $4,803
- Low Income Limit is $17,252 from $15,916

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 20,212           | 0              | 1.1%         | 0                  |
| 20,212      | 47,877           | 222.33         | 2.2%         | 20,212             |
| 47,877      | 61,730           | 831.18         | 4.4%         | 47,877             |
| 61,730      | 76,397           | 1,440.27       | 6.6%         | 61,730             |
| 76,397      | 90,240           | 2,408.29       | 8.8%         | 76,397             |
| 90,240      | 460,547          | 3,626.47       | 10.23%       | 90,240             |
| 460,547     | 552,658          | 41,508.88      | 11.33%       | 460,547            |
| 552,658     | 921,095          | 51,945.06      | 12.43%       | 552,658            |
| 921,095     | 1,000,000        | 97,741.78      | 13.53%       | 921,095            |
| 1,000,000   | And Over         | 108,417.63     | 14.63%       | 1,000,000          |

Withholding rates for taxpayers filing as *MAR1* and *MAR2*

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 20,198           | 0              | 1.1%         | 0                  |
| 20,198      | 47,884           | 222.18         | 2.2%         | 20,198             |
| 47,884      | 75,576           | 831.27         | 4.4%         | 47,884             |
| 75,576      | 104,910          | 2,049.72       | 6.6%         | 75,576             |
| 104,910     | 132,590          | 3,985.76       | 8.8%         | 104,910            |
| 132,590     | 677,278          | 6,421.60       | 10.23%       | 132,590            |
| 677,278     | 812,728          | 62,143.18      | 11.33%       | 677,278            |
| 812,728     | 1,000,000        | 77,489.67      | 12.43%       | 812,728            |
| 1,000,000   | 1,354,550        | 100,767.58     | 13.53%       | 1,000,000          |
| 1,354,550   | And Over         | 148,738.20     | 14.63%       | 1,354,550          |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over  | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,099           | 0              | 1.1%         | 0                  |
| 10,099      | 23,942           | 111.09         | 2.2%         | 10,099             |
| 23,942      | 37,788           | 415.64         | 4.4%         | 23,942             |
| 37,788      | 52,455           | 1,024.86       | 6.6%         | 37,788             |
| 52,455      | 66,295           | 1,992.88       | 8.8%         | 52,455             |
| 66,295      | 338,639          | 3,210.80       | 10.23%       | 66,295             |
| 338,639     | 406,364          | 31,071.59      | 11.33%       | 338,639            |
| 406,364     | 677,275          | 38,744.83      | 12.43%       | 406,364            |
| 677,275     | 1,000,000        | 72,419.07      | 13.53%       | 677,275            |
| 1,000,000   | And Over         | 116,083.76     | 14.63%       | 1,000,000          |


#### Withholding changes for Iowa

#### Withholding changes for Kentucky

The Standard Deduction Amount is $2,980 from $2,770
The Tax Rate decreases to 4.5% formerly 5%


#### Withholding changes for Maryland

For each Filing Status of Maryland
•	Standard Deduction Minimum is $1,600 from $1,550
•	Standard Deduction Maximum is $2,400 from $2,350
The Standard Deduction Percent remains at 15 percent.

 
#### Withholding changes for Utah

All filing status have a fixed flat tax of 4.85% from 4.95%

- MAR - Married  - Base Allowance Exemption amount  $780.00 prior amount $720.00
- SINGLE - Single  - Base Allowance Exemption amount  $390.00 prior amount $360.00

- MAR - Married  - Tax Rate of 1.3% anything over $15,548 prior amount $14,256 (held in Special tax table)
- SINGLE - Single  - Tax Rate of 1.3% anything over $7,774.00 prior amount $7,128.00 (held in Special tax table)



#### Withholding changes for Illinois

The Dependent Exemptions is $2,425
The Flat tax rate remains at 4.95 and allowances at 1,000

#### Withholding changes for Louisiana

The Flat tax rate for all filing status is 1.85 from 2.2

Special Type rates for EXEMPT and SM1 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 50,000           | 0              | 1.65%        | 12,500             |
| 50,000      | And Over         | 0              | .075%        | 50,000             |


Special Type rates for M2 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1000,000         | 0              | 1.65%        | 25,000             |
| 100,000     | And Over         | 0              | .075%        | 100,000            |


#### Withholding changes for Minnesota

The Personal Exemption amount is \$4,450 for all Filing Status.

Withholding rates for taxpayers filing as *MAR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,450           | 0              | 0%           | 0                  |
| 12,450      | 53,500           | 0              | 5.35         | 12,450             |
| 53,500      | 175,510          | 2,196.18       | 6.80%        | 53,500             |
| 175,510     | 297,260          | 10,492.86      | 7.85%        | 175,510            |
| 297,260     | And Over         | 20,050.24      | 9.85%        | 297,260            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 4,000        | 0          | 0%       | 0              |
| 4,000   | 32,080       | 0          | 5.35%    | 4,000          |
| 32,080  | 96,230       | 1,502.28   | 6.80%    | 32,080         |
| 96,230  | 175,220      | 5,864.48   | 7.85%    | 96,230         |
| 175,220 | And Over     | 12,065.20  | 9.85%    | 175,220        |

#### Withholding changes for North Carolina

Standard Deduction for HOH is $19,125
Standard Deduction for MAR and SINGLE is $12,750

Tax rate for all filing status is 5.09%

#### Withholding changes for North Dakota

> [!NOTE]
> Per the state of North Dakota, there is no HOH filing status with exemptions. If an employee on the W4 chooses Filing status of HOH and does not mark step 2, you still choose HOH as the filing status in Dynamics GP.
>
> The state relies on the Federal form W-4 to calculate the amount to withhold. Per the state, Step 3 for Dependent Claim amount is not used for ND state tax withholding.

Withholding rates for taxpayers filing as *MAR* and *MARHR* :

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,950           | 0              | 0%           | 0                  |
| 12,950      | 47,800           | 0              | 1.10%        | 12,950             |
| 47,800      | 97,175           | 383.35         | 2.04%        | 47,800             |
| 97,175      | 141,275          | 1,390.60       | 2.27%        | 97,175             |
| 141,275     | 242,125          | 2,391.67       | 2.64%        | 141,275            |
| 242,125     | And Over         | 5,054.11       | 2.90%        | 242,125            |

Withholding rates for taxpayers filing as *SINGLE* and *SINGHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 6,475        | 0          | 0%       | 0              |
| 6,475   | 48,250       | 0          | 1.10%    | 6,475          |
| 48,250  | 107,525      | 459,53     | 2.04%    | 48,250         |
| 107,525 | 217,300      | 1,668.74   | 2.27%    | 107,525        |
| 217,300 | 464,825      | 4,160.63   | 2.64%    | 217,300        |
| 464,825 | And Over     | 10,695.29  | 2.90%    | 464,825        |


Withholding rates for taxpayers filing as *HOHHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 9,700        | 0          | 0%       | 0              |
| 9,700   | 65,600       | 0          | 1.10%    | 9,700          |
| 65,600  | 154,100      | 614.90     | 2.04%    | 65,600         |
| 154,100 | 243,450      | 2,420.30   | 2.27%    | 154,100        |
| 243,450 | 468,050      | 4,448.55   | 2.64%    | 243,450        |
| 468,050 | And Over     | 10,377.99  | 2.90%    | 468,050        |


#### Withholding changes for Rhode Island

For all Filing Status the Personal Exemption ($1,000) wage limit increased to $241,850

Withholding rates for taxpayers filing as *MAR* and *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 68,200           | 0              | 3.75%        | 0                  |
| 68,200      | 155,050          | 2,557.50       | 4.75%        | 68,200             |
| 155,050     | And Over         | 6,682.88       | 5.99%        | 155,050            |


#### Withholding changes for Vermont

The Personal Exemption amount is $4,500

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,788            | 0              | 0%           | 0                  |
| 9,788       | 80,238           | 0              | 3.35%        | 9,788              |
| 80,238      | 180,088          | 2,360.08       | 6.60%        | 80,238             |
| 180,088     | 269,288          | 8,950.18       | 7.60%        | 180,088            |
| 269,288     | And Over         | 15,729.38      | 8.75%        | 269,288            |

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,250            | 0              | 0%           | 0                  |
| 3,250       | 45,400           | 0              | 3.35%        | 3,250              |
| 45,400      | 105,450          | 1,412.03       | 6.60%        | 45,400             |
| 105,450     | 216,400          | 5,375.33       | 7.60%        | 105,450            |
| 216,400     | And Over         | 13,807.53      | 8.75%        | 216,400            |


#### Withholding changes for Wisconsin

**January Hotfix Code is required to install this tax update for the state of WI**

Added to the Sequence of WI tax calculation Apply Special Table for Deduction Exemption

The Personal Exemption amount is $400.00 

Tax Type rates for SINGLE and MAR Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,760           | 0              | 3.54%        | 0                  |
| 12,760      | 25,520           | 451.70         | 4.65%        | 12,760             |
| 25,520      | 280,950          | 1,045.04       | 5.30%        | 25,520             |
| 280,950     | And Over         | 14,582.83      | 7.65%        | 280,950            |

Special Type rates for MAR Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 25,727           | 9,461          | 0%           | 0                  |
| 25,727      | 73,032           | 0              | 20%          | 0                  |
| 73,032      | And Over         | 0              | 0%           | 0                  |

Special Type rates for SINGLE Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 17,780           | 6,702          | 0%           | 0                  |
| 17,780      | 73,630           | 0              | 12%          | 0                  |
| 73,650      | And Over         | 0              | 0%           | 0                  |



#### Withholding changes for California

For Filing Status of HOH and MAR2:  

- Personal Exemption is $141.90 from $136.40
- Standard Deduction is $9,606  from $9,202
- Low Income Limit is $31,831 from $30,534

For Filing Status of MAR1 and SINGLE:

- Personal Exemption is $141.90 from $136.40
- Standard Deduction is $4,803 from $4,601
- Low Income Limit is $15,916 from $15,267

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over  |
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

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over  |
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

Withholding rates for taxpayers filing as *SINGLE*:

| If Over  | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over  |
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

- HOH and SINGLE     is \$5,400
- MFJ1I              is \$7,100
- MFJ2I and MFS      is \$3,550

#### Withholding changes for Iowa

The Standard Deduction Amount for Filing Status:

- EXP1 is \$2,210
- Filing Status EXP2 is \$5,450

Withholding rates for taxpayers filing as EXP1 and EXP2 are as follows:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,743            | 0              | 0.33%        | 0                  |
| 1,743       | 3,486            | 5.75           | 0.67%        | 1,743              |
| 3,486       | 6,972            | 17.43          | 2.25%        | 3,486              |
| 6,972       | 15,687           | 95.87          | 4.14%        | 6,972              |
| 15,687      | 26,145           | 456.67         | 5.63%        | 15,687             |
| 26,145      | 34,860           | 1,045.46       | 5.96%        | 26,145             |
| 34,860      | 52,290           | 1,564.87       | 6.25%        | 34,860             |
| 52,290      | 78,435           | 2,654.25       | 7.44%        | 52,290             |
| 78,435      | And over         | 4,599.44       | 8.53%        | 78,435             |

#### Withholding changes for Kentucky

The Standard Deduction Amount is $2,770 from $2,690
The Tax Rate remains at 5%

#### Withholding changes for Maine

- Personal Exemption is $4,450

Withholding rates for taxpayers filing as *SINGLE*, Tax table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 23,000           | 0              | 5.8%         | 0                  |
| 23,000      | 54,450           | 1,334          | 6.75%        | 23,000             |
| 54,450      | And over         | 3,457          | 7.15%        | 54,450             |

Special table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 85,850           | 0              | 0            | 10,100             |
| 85,850      | 160,850          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 46,000           |                | 5.80%        | 0                  |
| 46,000      | 108,900          | 2,668          | 6.75%        | 46,000             |
| 108,900     | And Over         | 6,914          | 7.15%        | 108,900            |

Special table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 171,700          | 0              | 0            | 23,050             |
| 171,700     | 321,700          | 150,000        | 0            | 0                  |

#### Withholding changes for Maryland

For Filing Status of SMMAR (St. Mary MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.85%        | 0                  |
| 150,000     | 175,000          | 11,775         | 8.10%        | 150,000            |
| 175,000     | 225,000          | 13,800         | 8.35%        | 175,000            |
| 225,000     | 300,000          | 17,975         | 8.6%         | 225,000            |
| 300,000     | And over         | 24,425         | 8.85%        | 300,000            |

For Filing Status of STMARY (St. Mary SGL/DEP/MFS):

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.85%        | 0                  |
| 100,000     | 125,000          | 7,850          | 8.10%        | 100,000            |
| 125,000     | 150,000          | 9,875          | 8.35%        | 125,000            |
| 150,000     | 250,000          | 11,962.50      | 8.6%         | 150,000            |
| 250,000     | And over         | 20,562.50      | 8.85%        | 250,000            |

For Filing Status of WASHTN (Washington SGL/DEP/MFS):

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.75%        | 0                  |
| 100,000     | 125,000          | 7,750          | 8.00%        | 100,000            |
| 125,000     | 150,000          | 9,750          | 8.25%        | 125,000            |
| 150,000     | 250,000          | 11,812.50      | 8.5%         | 150,000            |
| 250,000     | And over         | 20,312.50      | 8.75%        | 250,000            |

For Filing Status of WHMAR  (Washington MFJ/HOH):

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.75%        | 0                  |
| 150,000     | 175,000          | 11,625         | 8.0%         | 150,000            |
| 175,000     | 225,000          | 13,625         | 8.25%        | 175,000            |
| 225,000     | 300,000          | 17,750         | 8.5%         | 225,000            |
| 300,000     | And over         | 24,125         | 8.75%        | 300,000            |

#### Withholding changes for Michigan

The Personal Exemption Amount is $5,000 from $4,900
The Tax Rate remains at 4.25%

#### Withholding changes for Missouri

The Standard Deduction is \$19,400 for filing status HOH
The Standard Deduction is \$25,900 for filing status MAR1
The Standard Deduction is \$12,950 for filing status MAR2 and SINGLE

Withholding rates for all filing status

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,121            | 0              | 1.5%         | 0                  |
| 1,121       | 2,242            | 17.00          | 2.0%         | 1,121              |
| 2,242       | 3,363            | 39.00          | 2.5%         | 2,242              |
| 3,363       | 4,484            | 67.00          | 3.0%         | 3,363              |
| 4,484       | 5,605            | 101.00         | 3.5%         | 4,484              |
| 5,605       | 6,726            | 140.00         | 4.0%         | 5,605              |
| 6,726       | 7,847            | 185.00         | 4.50%        | 6,726              |
| 7,847       | 8,968            | 235.00         | 5.0%         | 7,847              |
| 8,968       | And over         | 291.00         | 5.3%         | 8,968              |

#### Withholding changes for Nebraska

The Personal Exemption amount is \$2,080 for Filing Status MAR and SINGLE.

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,100            | 0              | 0            | 0                  |
| 7,100       | 11,270           | 0              | 2.26%        | 7,100              |
| 11,270      | 28,070           | 94.24          | 3.22%        | 11,270             |
| 28,070      | 43,670           | 635.20         | 4.91%        | 28,070             |
| 43,670      | 54,180           | 1,401.16       | 6.20%        | 43,670             |
| 54,180      | 71,850           | 2,052.78       | 6.59%        | 54,180             |
| 71,850      | And over         | 3,217.23       | 6.95%        | 71,850            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,975            | 0              | 0            | 0                  |
| 2,975       | 5,820            | 0              | 2.26%        | 2,975              |
| 5,820       | 18,900           | 64.30          | 3.22%        | 5,820              |
| 18,900      | 27,390           | 485.48         | 4.91%        | 18,900             |
| 27,390      | 34,780           | 902.34         | 6.20%        | 27,390             |
| 34,780      | 65,310           | 1,360.52       | 6.59%        | 34,780             |
| 65,310      | And over         | 3,372.45       | 6.95%        | 65,310         |

#### Withholding changes for New Mexico

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,950           | 0              | 0%           | 0                  |
| 12,950      | 20,950           | 0              | 1.70%        | 12,950             |
| 20,950      | 28,950           | 136.00         | 3.2%         | 20,950             |
| 28,950      | 36,950           | 392.00         | 4.7%         | 28,950             |
| 36,950      | 52,950           | 768.00         | 4.9%         | 36,950             |
| 52,950      | 76,950           | 1,552.00       | 4.9%         | 52,950             |
| 76,950      | 112,950          | 2,728.00       | 4.9%         | 76,950             |
| 112,950     | 212,950          | 4,492.00       | 4.9%         | 112,950            |
| 212,950     | 327,950          | 9,392.00       | 4.9%         | 212,950            |
| 327,950     | And Over         | 15,027.00      | 5.9%         | 327,950            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 6,475            | 0              | 0%           | 0                  |
| 6,475       | 11,975           | 0              | 1.7%         | 6,475              |
| 11,975      | 17,475           | 93.50          | 3.2%         | 11,975             |
| 17,475      | 22,475           | 269.50         | 4.7%         | 17,475             |
| 22,475      | 32,475           | 504.50         | 4.9%         | 22,475             |
| 32,475      | 48,475           | 994.50         | 4.9%         | 32,475             |
| 48,475      | 71,475           | 1,778.50       | 4.9%         | 48,475             |
| 71,475      | 131,475          | 2,905.50       | 4.9%         | 71,475             |
| 131,475     | 216,475          | 5,845.50       | 4.9%         | 131,475            |
| 216,475     | And Over         | 10,010.50      | 5.9%         | 216,475            |

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,700            | 0              | 0%           | 0                  |
| 9,700       | 17,700           | 0              | 1.7%         | 9,700              |
| 17,700      | 25,700           | 136.00         | 3.2%         | 17,700             |
| 25,700      | 33,700           | 392.00         | 4.7%         | 25,700             |
| 33,700      | 49,700           | 768.00         | 4.9%         | 33,700             |
| 49,700      | 73,700           | 1,552.00       | 4.9%         | 49,700             |
| 73,700      | 109,700          | 2,728.00       | 4.9%         | 73,700             |
| 109,700     | 209,700          | 4,492.00       | 4.9%         | 109,700            |
| 209,700     | 324,700          | 9,392.00       | 4.9%         | 209,700            |
| 324,700     | And Over         | 15,027.00      | 5.9%         | 324,700            |

#### Withholding changes for New York and New York-Yonkers

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,500            | 0              | .0400        | 0                  |
| 8,500       | 11,700           | 340.00         | .0450        | 8,500              |
| 11,700      | 13,900           | 484.00         | .0525        | 11,700             |
| 13,900      | 80,650           | 600.00         | .0585        | 13,900             |
| 80,650      | 96,800           | 4,504.00       | .0625        | 80,650             |
| 96,800      | 107,650          | 5,514.00       | .0711        | 96,800             |
| 107,650     | 157,650          | 6,285.00       | .0761        | 107,650            |
| 157,650     | 211,550          | 10,090.00      | .0804        | 157,650            |
| 211,550     | 323,200          | 14,425.00      | .0675        | 211,550            |
| 323,200     | 373,200          | 21,961.00      | .1123        | 323,200            |
| 373,200     | 1,077,550        | 27,576.00      | .0735        | 373,200            |
| 1,077,550   | 2,155,350        | 79,346.00      | .0765        | 1,077,550          |
| 2,155,350   | 5,000,000        | 0              | .1045        | 0                  |
| 5,000,000   | 25,000,000       | 0              | .1110        | 0                  |
| 25,000,000  | And over         | 0              | .1170        | 0                  |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,500            | 0              | .0400        | 0                  |
| 8,500       | 11,700           | 340.00         | .0450        | 8,500              |
| 11,700      | 13,900           | 484.00         | .0525        | 11,700             |
| 13,900      | 80,650           | 600.00         | .0585        | 13,900             |
| 80,650      | 96,800           | 4,504.00       | .0625        | 80,650             |
| 96,800      | 107,650          | 5,541.00       | .0732        | 96,800             |
| 107,650     | 157,650          | 6,308.00       | .0782        | 107,650            |
| 157,650     | 215,400          | 10,219.00      | .0675        | 157,650            |
| 215,400     | 265,400          | 14,117.00      | .0994        | 215,400            |
| 265,400     | 1,077,550        | 19,085.00      | .0735        | 265,400            |
| 1,077,550   | 5,000,000        | 0              | .1045        | 0                  |
| 5,000,000   | 25,000,000       | 0              | .1110        | 0                  |
| 25,000,000  | And over         | 0              | .1170        | 0                  |

#### Withholding changes for Oklahoma

Withholding rates for taxpayers filing as *MARH*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,700           | 0              | 0%           | 0                  |
| 12,700      | 14,700           | 0              | .25%         | 12,700             |
| 14,700      | 17,700           | 5.00           | .75%         | 14,700             |
| 17,700      | 20,200           | 27.50          | 1.75%        | 17,700             |
| 20,200      | 22,500           | 71.25          | 2.75%        | 20,200             |
| 22,500      | 24,900           | 134.50         | 3.75%        | 22,500             |
| 24,900      | And Over         | 224.50         | 4.75%        | 24,900             |

Withholding rates for taxpayers filing as *SINGLE*, *MFS*, *MAR2*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 6,350            | 0              | 0%           | 0                  |
| 6,350       | 7,350            | 0              | .25%         | 6,350              |
| 7,350       | 8,850            | 2.50           | .75%         | 7,350              |
| 8,850       | 10,100           | 13.75          | 1.75%        | 8,850              |
| 10,100      | 11,250           | 35.63          | 2.75%        | 10,100             |
| 11,250      | 13,550           | 67.25          | 3.75%        | 11,250             |
| 13,550      | And Over         | 153.50         | 4.75%        | 13,550             |

#### Withholding changes for Oregon

The Standard Deduction Amount is \$4,840 for MS3 and S3 Filing Status.

The Standard Deduction Amount is \$2,420 for S2 Filing Status.

The Personal Exemption amount remains at \$213.00 for all Filing Status.

New Filing status for 2020 *NOWH* (No Withholding Provided) Flat tax rate of 8% (remains for 2022 year)

HB2119 requires employers to withhold income tax at a rate of 8 percent of employee wages if they employee has not provided a withholding statement or exemption certificate.  
Continue withholding at the 8 percent rate until the employee submits a withholding statement and exemption certificate.

Special Tax Type rates for MS3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 7,250          | 0%           | 0                  |
| 49,999      | 249,999          | 7,250          | 0%           | 0                  |
| 249,999     | 259,999          | 5,800          | 0%           | 0                  |
| 259,999     | 269,999          | 4,350          | 0%           | 0                  |
| 269,999     | 279,999          | 2,900          | 0%           | 0                  |
| 279,999     | 289,999          | 1,450          | 0%           | 0                  |
| 289,999     | And over         | 0              | 0%           | 0                  |
|             |                  |                |              |                    |

Special Tax Type rates for S2 and S3 Filing Status:

| If Over     |     But Not Over | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 7,250          | 0%           | 0                  |
| 49,999      | 124,999          | 7,250          | 0%           | 0                  |
| 124,999     | 129,999          | 5,800          | 0%           | 0                  |
| 129,999     | 134,999          | 4,350          | 0%           | 0                  |
| 134,999     | 139,999          | 2,900          | 0%           | 0                  |
| 139,999     | 144,999          | 1,450          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

Tax Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 37,910           | 0              | 0%           | 0                  |
| 37,910      | 250,000          | 1,126          | 8.75%        | 18,900             |
| 250,000     | And over         | 21,347         | 9.9%         | 250,000            |

Tax Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 40,330           | 0              | 0%           | 0                  |
| 40,330      | 125,000          | 563            | 8.75%        | 9,450              |
| 125,000     | And Over         | 10,674         | 9.9%         | 125,000            |

Low Income Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,500            | 219            | 4.75%        | 0                  |
| 7,500       | 18,900           | 575            | 6.75%        | 7,500              |
| 18,900      | 50,000           | 1,345          | 8.75%        | 18,900             |

Low Income Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,750            | 219            | 4.75%        | 0                  |
| 3,750       | 9,450            | 397            | 6.75%        | 3,750              |
| 9,450       | 50,000           | 782            | 8.75%        | 9,450              |

#### Withholding changes for South Carolina

The Personal Exemption is $2,750 for Filing Status ONE.
The Standard Deduction Maximum is $4,580 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,980            | 0              | 0.2%         | 0                  |
| 2,980       | 5,960            | -83.44         | 3.0%         | 0                  |
| 5,960       | 8,940            | -143.04        | 4.0%         | 0                  |
| 8,940       | 11,920           | -232.44        | 5.0%         | 0                  |
| 11,920      | 14,900           | -351.64        | 6.0%         | 0                  |
| 14,900      | And over         | -500.64        | 7.0%         | 0                  |

## Resources to assist you

If you have questions about U.S. Payroll tax updates and your Microsoft Partner isn't available, there are several resources, in addition to this document, to assist in answering your questions.

### U.S. Payroll Tax Updates

Take a look at [this location](/dynamics/s-e/gp/tugp2018_391) to find out the tax changes included in each update and to download the update. All instructions for downloading and installing the tax updates also are provided here.

### eSupport

For support requests that can be handled with email, go to [https://support.microsoft.com/supportforbusiness](https://support.microsoft.com/supportforbusiness). On average, the response time is nearly twice as fast as telephone support.

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

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *10/10/2022*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
