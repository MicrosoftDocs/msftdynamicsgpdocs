---
title: "US payroll tax update"
description: "US 2023 January payroll tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 12/21/2022
---
# U.S. 2023 Payroll Tax Update

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
- Kentucky
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
| 43,138      | 68,463           | 2,573.50       | 22%          | 43,138             |
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
| 20,212      | 47,887           | 222.33         | 2.2%         | 20,212             |
| 47,887      | 61,730           | 831.18         | 4.4%         | 47,887             |
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


#### Withholding changes for Kentucky

The Standard Deduction Amount is $2,980 from $2,770
The Tax Rate decreases to 4.5% formerly 5%

#### Withholding changes for Maine

- Personal Exemption is $4,700 was $4,450

Withholding rates for taxpayers filing as *SINGLE*, Tax table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 24,500           | 0              | 5.8%         | 0                  |
| 24,500      | 58,050           | 1,421          | 6.75%        | 24,500             |
| 58,050      | And over         | 3,686          | 7.15%        | 58,050             |

Special table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 91,500           | 0              | 0            | 11,000             |
| 91,500      | 166,500          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,050           |                | 5.80%        | 0                  |
| 49,050      | 116,100          | 2,845          | 6.75%        | 49,050             |
| 116,100     | And Over         | 7,371          | 7.15%        | 108,900            |

Special table type

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 183,050          | 0              | 0            | 24,850             |
| 183,050     | 333,050          | 150,000        | 0            | 0                  |


#### Withholding changes for Minnesota

The Personal Exemption amount is $4,800 previously \$4,450 for all Filing Status.

Withholding rates for taxpayers filing as *MAR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 13,250           | 0              | 0%           | 0                  |
| 13,250      | 57,200           | 0              | 5.35         | 13,250             |
| 57,200      | 187,860          | 2,351.33       | 6.80%        | 57,200             |
| 187,860     | 318,220          | 11,236.21      | 7.85%        | 187,860            |
| 318,220     | And Over         | 21,469.47      | 9.85%        | 318,220            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 4,225        | 0          | 0%       | 0              |
| 4,225   | 34,295       | 0          | 5.35%    | 4,225          |
| 34,295  | 102,985      | 1,608.75   | 6.80%    | 34,295         |
| 102,985 | 187,565      | 6,279.67   | 7.85%    | 102,985        |
| 187,565 | And Over     | 12,919.20  | 9.85%    | 187,565        |


#### Withholding changes for Mississippi

Dependent Exemption: 1,500 For All Filing Status

Standard Deduction: 4,600 for MAR1 & MAR2
Personal Exemption: 12,000  for MAR1 & MAR2

Standard Deduction: 3,400 for HOH
Personal Exemption: 9,500  for HOH

Standard Deduction: 2,300 for SINGLE
Personal Exemption: 6,000  for SINGLE

Withholding rates for all taxpayers filing status

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 10,000           | 0              | 0%           | 0                  |
| 10,000      | And Over         | 0              | 5%           | 10,000             |


#### Withholding changes for Missouri

The Standard Deduction is $20,800 prior \$19,400 for filing status HOH
The Standard Deduction is $27,700 prior \$25,900 for filing status MAR1
The Standard Deduction is $13,850 prior \$12,950 for filing status MAR2 and SINGLE

Withholding rates for all filing status

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,207            | 0              | 0%           | 0                  |
| 1,207       | 2,414            | 17.00          | 2.0%         | 1,207              |
| 2,414       | 3,621            | 39.00          | 2.5%         | 2,414              |
| 3,621       | 4,828            | 67.00          | 3.0%         | 3,621              |
| 4,828       | 6,035            | 101.00         | 3.5%         | 4,828              |
| 6,035       | 7,242            | 140.00         | 4.0%         | 6,035              |
| 7,242       | 8,449            | 235.00         | 4.5%         | 7,242              |
| 8,449       | And over         | 291.00         | 4.95%        | 8,449              |


#### Withholding changes for Montana

The Personal Exemption amount is $2,070 formerly $1,900 

Tax Type rates for SINGLE and MAR Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,630            | 0              | 1.80%        | 0                  |
| 7,630       | 16,350           | 137.00         | 4.40%        | 7,630              |
| 16,350      | 130,790          | 521.00         | 6.0%         | 16,350             |
| 130,790     | And Over         | 7,387.00       | 6.60%        | 130,790            |


#### Withholding changes for Nebraska

The Personal Exemption amount is $2,140 formerly \$2,080 for Filing Status MAR and SINGLE.

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,530            | 0              | 0            | 0                  |
| 7,530       | 11,610           | 0              | 2.26%        | 7,530              |
| 11,610      | 28,910           | 92.21          | 3.22%        | 11,610             |
| 28,910      | 44,980           | 649.27         | 4.91%        | 28,910             |
| 44,980      | 55,810           | 1,438.31       | 6.20%        | 44,980             |
| 55,810      | 74,010           | 2,109.77       | 6.39%        | 55,810             |
| 74,010      | And over         | 3,272.75       | 6.75%        | 74,010             |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,060            | 0              | 0            | 0                  |
| 3,060       | 5,990            | 0              | 2.26%        | 3,060              |
| 5,990       | 19,470           | 66.22          | 3.22%        | 5,990              |
| 19,470      | 28,210           | 500.28         | 4.91%        | 19,470             |
| 28,210      | 35,820           | 929.41         | 6.20%        | 28,210             |
| 35,820      | 67,270           | 1,401.23       | 6.39%        | 35,820             |
| 67,270      | And over         | 3,410.89       | 6.75%        | 67,270             |


#### Withholding changes for New Mexico

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 13,850           | 0              | 0%           | 0                  |
| 13,850      | 21,850           | 0              | 1.70%        | 13,850             |
| 21,850      | 29,850           | 136.00         | 3.2%         | 21,850             |
| 29,850      | 37,850           | 392.00         | 4.7%         | 29,850             |
| 37,850      | 53,850           | 768.00         | 4.9%         | 37,850             |
| 53,850      | 77,850           | 1,552.00       | 4.9%         | 53,850             |
| 77,850      | 113,850          | 2,728.00       | 4.9%         | 77,850             |
| 113,850     | 213,850          | 4,492.00       | 4.9%         | 113,850            |
| 213,850     | 328,850          | 9,392.00       | 4.9%         | 213,850            |
| 328,850     | And Over         | 15,027.00      | 5.9%         | 328,850            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 6,925            | 0              | 0%           | 0                  |
| 6,925       | 12,425           | 0              | 1.7%         | 6,925              |
| 12,425      | 17,925           | 93.50          | 3.2%         | 12,425             |
| 17,925      | 22,925           | 269.50         | 4.7%         | 17,925             |
| 22,925      | 32,925           | 504.50         | 4.9%         | 22,925             |
| 32,925      | 48,925           | 994.50         | 4.9%         | 32,925             |
| 48,925      | 71,925           | 1,778.50       | 4.9%         | 48,925             |
| 71,925      | 131,925          | 2,905.50       | 4.9%         | 71,925             |
| 131,925     | 216,925          | 5,845.50       | 4.9%         | 131,925            |
| 216,925     | And Over         | 10,010.50      | 5.9%         | 216,925            |

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,400           | 0              | 0%           | 0                  |
| 10,400      | 18,400           | 0              | 1.7%         | 10,400             |
| 18,400      | 26,400           | 136.00         | 3.2%         | 18,400             |
| 26,400      | 34,400           | 392.00         | 4.7%         | 26,400             |
| 34,400      | 50,400           | 768.00         | 4.9%         | 34,400             |
| 50,400      | 74,400           | 1,552.00       | 4.9%         | 50,400             |
| 74,400      | 110,400          | 2,728.00       | 4.9%         | 74,400             |
| 110,400     | 210,400          | 4,492.00       | 4.9%         | 110,400            |
| 210,400     | 325,400          | 9,392.00       | 4.9%         | 210,400            |
| 325,400     | And Over         | 15,027.00      | 5.9%         | 325,400            |


#### Withholding changes for New York and New York-Yonkers

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,500            | 0              | .0400        | 0                  |
| 8,500       | 11,700           | 340.00         | .0450        | 8,500              |
| 11,700      | 13,900           | 484.00         | .0525        | 11,700             |
| 13,900      | 80,650           | 600.00         | .0555        | 13,900             |
| 80,650      | 96,800           | 4,271.00       | .0600        | 80,650             |
| 96,800      | 107,650          | 5,240.00       | .0667        | 96,800             |
| 107,650     | 157,650          | 5,963.00       | .0717        | 107,650            |
| 157,650     | 211,550          | 9,546.00       | .0811        | 157,650            |
| 211,550     | 323,200          | 13,919.00      | .0650        | 211,550            |
| 323,200     | 373,200          | 21,177.00      | .1284        | 323,200            |
| 373,200     | 1,077,550        | 27,599.00      | .0735        | 373,200            |
| 1,077,550   | 2,155,350        | 29,368.00      | .0765        | 1,077,550          |
| 2,155,350   | 5,000,000        | 0              | .1045        | 0                  |
| 5,000,000   | 25,000,000       | 0              | .1110        | 0                  |
| 25,000,000  | And over         | 0              | .1170        | 0                  |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,500            | 0              | .0400        | 0                  |
| 8,500       | 11,700           | 340.00         | .0450        | 8,500              |
| 11,700      | 13,900           | 484.00         | .0525        | 11,700             |
| 13,900      | 80,650           | 600.00         | .0550        | 13,900             |
| 80,650      | 96,800           | 4,271.00       | .0600        | 80,650             |
| 96,800      | 107,650          | 5,240.00       | .0714        | 96,800             |
| 107,650     | 157,650          | 6,014.00       | .0764        | 107,650            |
| 157,650     | 215,400          | 9,832.00       | .0650        | 157,650            |
| 215,400     | 265,400          | 13,586.00      | .1101        | 215,400            |
| 265,400     | 1,077,550        | 19,092.00      | .0735        | 265,400            |
| 1,077,550   | 5,000,000        | 0              | .1045        | 0                  |
| 5,000,000   | 25,000,000       | 0              | .1110        | 0                  |
| 25,000,000  | And over         | 0              | .1170        | 0                  |


#### Withholding changes for South Carolina

The Personal Exemption is $4,310 for Filing Status ONE.
The Standard Deduction Maximum is $6,475 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,330            | 0              | 0.0%         | 0                  |
| 3,330       | 16,680           | -99.00         | 3.0%         | 0                  |
| 16,680      | And over         | -683.70        | 6.5%         | 0                  |




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

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *12/22/2022*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
