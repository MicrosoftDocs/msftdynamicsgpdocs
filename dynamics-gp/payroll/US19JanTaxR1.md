---
title: "US payroll tax update"
description: "US 2023 January payroll tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 4/5/2023
---
# U.S. 2023 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2023 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

This is the third tax update for 2023 and replaces all previous tax updates. It includes State tax table changes that take effect January 1, 2023. We recommend that you install this update as soon as you can for the year 2023.

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

Check out these blogs for detailed documentation on how you calculate payroll taxes in Microsoft Dynamics GP:

[How to calculate Federal Tax with Dependent Claim Amount Field](https://community.dynamics.com/gp/b/dynamicsgp/posts/how-to-calculate-federal-tax-with-dependent-claim-amount)

[Does Microsoft Dynamics GP calculate tax correctly?](https://community.dynamics.com/gp/b/dynamicsgp/posts/is-microsoft-dynamics-gp-calculating-payroll-taxes-correctly)

[Tips to install the U.S. Payroll Tax Update](https://community.dynamics.com/gp/b/dynamicsgp/posts/tips-to-install-the-u-s-payroll-tax-update)


## Changes in April Round 3 update (Released: 4/5/2023)

### 2023 state or territorial tax changes
The following tax changes are included in this update:

- District of Columbia
- Michigan
- Utah
- West Virginia

#### Withholding changes for District of Columbia

The Personal Exemption amount is $4,300 For all filing status.

Withholding rates for taxpayers for all filing status are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 10,000           | 0              | 4%       | 0                  |
| 10,000      | 40,000           | 400            | 6%       | 10,000             |
| 40,000      | 60,000           | 2,200          | 6.5%     | 40,000             |
| 60,000      | 250,000          | 3,500          | 8.5%     | 60,000             |
| 250,000     | 500,000          | 19,650         | 9.25%    | 250,000            |
| 500,000     | 1,000,000        | 42,775         | 9.75%    | 500,000            |
| 1,000,000   | and over         | 91,525         | 10.75%   | 1,000,000          |

#### Withholding changes for Michigan

All filing status have the same fixed flat tax of 4.05%.
Personal Exemption amount is $5,400.00

#### Withholding changes for Utah

All filing status have the same fixed flat tax of 4.65%.

#### Withholding changes for West Virginia

The Personal Exemption amount is $2,000 For all filing status.

Withholding rates for taxpayers filing as PM (Percentage Method) are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 10,000           | 0              | 2.36%    | 0                  |
| 10,000      | 25,000           | 236.00         | 3.15%    | 10,000             |
| 25,000      | 40,000           | 708.50         | 3.54%    | 25,000             |
| 40,000      | 60,000           | 1,239.50       | 4.72%    | 40,000             |
| 60,000      | and over         | 2,183.50       | 5.12%    | 60,000             |

Withholding rates for taxpayers filing as TE (Two Earner Option) are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 7,500            | 0              | 2.36%    | 0                  |
| 7,500       | 18,750           | 177.00         | 3.15%    | 7,500              |
| 18,750      | 30,000           | 531.38         | 3.54%    | 18,700             |
| 30,000      | 45,000           | 929.63         | 4.72%    | 30,000             |
| 45,000      | and over         | 1,637.63       | 5.12%    | 45,000             |


## Changes in January Round 2 update (Released: 1/24/2023)

### 2023 state or territorial tax changes
The following tax changes are included in this update:

- Colorado
- Illinois
- Indiana
- Iowa
- Maryland
- Michigan
- North Carolina
- North Dakota
- Oregon
- Rhode Island
- Vermont
- Arkansas - code changes

#### Withholding changes for Colorado

All filing status have the same fixed flat tax of 4.40% was 4.55%(2022)

The Personal Exemption amount is $9,000 for MAR
The Personal Exemption amount is $4,500 For SINGLE

**The following new filing status were added January 2022:**

- HOH1J - Head of Household 1 Job - Exemption amount  $18,500  
- MAR1J - Married Filing Jointly 1 Job - Exemption amount  $25,500  
- SIN1J - Single/Mar filing Single 1 Job - Exemption amount  $11,500  

In January 2022 the state of Colorado released a new form called [DR-0004](https://tax.colorado.gov/withholding-forms) this is optional for an employee to complete.  

There are 2 other parts to this form that have many different exemption amounts, we cannot accommodate all of them in the tax tables.
A new “OTHER” filing status was added (OTH1J) with Exemption increments of $500 that will accommodate all the "other" amounts on the form if an employee enters. 

OTH1J - OTH, +1 Jobs or Child Cr Allow - Exemption amount of $500

As an example, lets say I fill out the form and choose an amount of 2500 – it does not match any of the above filing status so I would pick the OTHER status and put a 5 under Cards | Payroll | State Tax in the Number of Dependents field OR Additional Allowances. Which is 2500/500 = 5.

Another example, I put 5500 on the form. Again, that does not match the other filing status, so I choose *Other* and put *11*.

#### Withholding changes for Illinois

The Dependent Exemptions is $2,625 formerly $2,425
The Flat tax rate remains at 4.95 and allowances at 1,000

#### Withholding changes for Indiana

The Flat tax is 3.15% previously 3.23%

#### Withholding changes for Iowa

New for 2023 Iowa withholding calculations, federal withholding is no longer subtracted from taxable wages.  

The Standard Deduction Amount for Filing Status:

- EXP1 is $13,850 previously \$2,210
- EXP2 is $27,700 previously \$5,450

Withholding rates for taxpayers filing as EXP1 and EXP2 are as follows:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,800            | 0              | 4.40%        |                    |
| 4,800       | 24,000           | 211.20         | 4.82%        | 4,800              |
| 24,000      | 50,000           | 1,136.64       | 5.70%        | 24,000             |
| 50,000      | And over         | 2,618.64       | 6.00%        | 50,000             |

#### Withholding changes for Maryland

For each Filing Status of Maryland
•             Standard Deduction Minimum is $1,700 from $1,600
•             Standard Deduction Maximum is $2,550 from $2,400
The Standard Deduction Percent remains at 15 percent.

For Filing Status of AAMAR (Anne Arundel MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 50,000           | 0              | 7.50%        | 0                  |
| 50,000      | 150,000          | 0              | 7.60%        | 0                  |
| 150,000     | 175,000          | 11,400         | 7.85%        | 150,000            |
| 175,000     | 225,000          | 13,362.50      | 8.10%        | 175,000            |
| 225,000     | 300,000          | 17,412.50      | 8.35%        | 225,000            |
| 300,000     | And over         | 23,675         | 8.60%        | 300,000            |

For Filing Status of ARNDEL (Anne Arundel SGL/DEP/MFS).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 50,000           | 0              | 7.50%        | 0                  |
| 50,000      | 100,000          | 0              | 7.60%        | 0                  |
| 100,000     | 125,000          | 7,600          | 7.85%        | 100,000            |
| 125,000     | 150,000          | 9,562.50       | 8.10%        | 125,000            |
| 150,000     | 250,000          | 11,587.50      | 8.35%        | 150,000            |
| 250,000     | And over         | 19,937.50      | 8.60%        | 250,000            |

For Filing Status of FRMAR (Frederick MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.50%        | 0                  |
| 100,000     | 150,000          | 0              | 7.75%        | 0                  |
| 150,000     | 175,000          | 11,625         | 8.00%        | 150,000            |
| 175,000     | 225,000          | 13,625         | 8.25%        | 175,000            |
| 225,000     | 300,000          | 17,750         | 8.50%        | 225,000            |
| 300,000     | And over         | 24,125         | 8.75%        | 300,000            |

For Filing Status of FREDRK (Frederick SGL/DEP/MFS).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 50,000           | 0              | 7.50%        | 0                  |
| 50,000      | 100,000          | 0              | 7.75%        | 0                  |
| 100,000     | 125,000          | 7,750          | 8.00%        | 100,000            |
| 125,000     | 150,000          | 9,750.00       | 8.25%        | 125,000            |
| 150,000     | 250,000          | 11,812.50      | 8.50%        | 150,000            |
| 250,000     | And over         | 20,312.50      | 8.75%        | 250,000            |


#### Withholding changes for Michigan

The Personal Exemption Amount is $5,400 from $5,000
The Tax Rate remains at 4.25%


#### Withholding changes for North Carolina

Standard Deduction for HOH remains at $19,125
Standard Deduction for MAR and SINGLE remains at $12,750

Tax rate for all filing status is 4.85%

#### Withholding changes for North Dakota

> [!NOTE]
> Per the state of North Dakota, there is no HOH filing status with exemptions. If an employee on the W4 chooses Filing status of HOH and does not mark step 2, you still choose HOH as the filing status in Dynamics GP.
>
> The state relies on the Federal form W-4 to calculate the amount to withhold. Per the state, Step 3 for Dependent Claim amount is not used for ND state tax withholding.

Withholding rates for taxpayers filing as *MAR* and *MARHR* :

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 13,850           | 0               | 0%           | 0                 |
| 13,850      | 51,225           | 0               | 1.10%        | 13,850            |
| 51,225      | 104,125          | 411.13          | 2.04%        | 51,225            |
| 104,125     | 151,400          | 1,490.290       | 2.27%        | 104,125           |
| 151,400     | 259,525          | 2,5631.43       | 2.64%        | 151,400           |
| 259,525     | And Over         | 5,417.93        | 2.90%        | 259,525           |

Withholding rates for taxpayers filing as *SINGLE* and *SINGHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 6,925        | 0          | 0%       | 0              |
| 6,925   | 51,650       | 0          | 1.10%    | 6,925          |
| 51,650  | 115,250      | 491.98     | 2.04%    | 51,650         |
| 115,250 | 232,900      | 1,789.42   | 2.27%    | 115,250        |
| 232,900 | 498,275      | 4,460.07   | 2.64%    | 232,900        |
| 498,275 | And Over     | 11,456.97  | 2.90%    | 498,275        |


Withholding rates for taxpayers filing as *HOHHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 10,400       | 0          | 0%       | 0              |
| 10,400  | 70,350       | 0          | 1.10%    | 10,400         |
| 70,350  | 165,150      | 659.45     | 2.04%    | 70,350         |
| 165,150 | 260,950      | 2,593.37   | 2.27%    | 165,150        |
| 260,950 | 501,750      | 4,768.035  | 2.64%    | 260,950        |
| 501,750 | And Over     | 11,125.159 | 2.90%    | 501,750        |

#### Withholding changes for Oregon

The Standard Deduction Amount is \$5,210 for MS3 and S3 Filing Status.

The Standard Deduction Amount is \$2,605 for S2 Filing Status.

The Personal Exemption amount is \$236.00 for all Filing Status.

New Filing status for 2020 *NOWH* (No Withholding Provided) Flat tax rate of 8% (remains for 2023 year)

HB2119 requires employers to withhold income tax at a rate of 8 percent of employee wages if they employee has not provided a withholding statement or exemption certificate.  
Continue withholding at the 8 percent rate until the employee submits a withholding statement and exemption certificate.

Special Tax Type rates for MS3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 7,800          | 0%           | 0                  |
| 49,999      | 249,999          | 7,800          | 0%           | 0                  |
| 249,999     | 259,999          | 6,250          | 0%           | 0                  |
| 259,999     | 269,999          | 4,700          | 0%           | 0                  |
| 269,999     | 279,999          | 3,100          | 0%           | 0                  |
| 279,999     | 289,999          | 1,550          | 0%           | 0                  |
| 289,999     | And over         | 0              | 0%           | 0                  |
|             |                  |                |              |                    |

Special Tax Type rates for S2 and S3 Filing Status:

| If Over     |     But Not Over | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 7,800          | 0%           | 0                  |
| 49,999      | 124,999          | 7,800          | 0%           | 0                  |
| 124,999     | 129,999          | 6,250          | 0%           | 0                  |
| 129,999     | 134,999          | 4,700          | 0%           | 0                  |
| 134,999     | 139,999          | 3,100          | 0%           | 0                  |
| 139,999     | 144,999          | 1,550          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

Tax Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 36,990           | 0              | 0%           | 0                  |
| 36,990      | 250,000          | 1,215          | 8.75%        | 20,400             |
| 250,000     | And over         | 21,305         | 9.9%         | 250,000            |

Tax Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 39,595           | 0              | 0%           | 0                  |
| 39,595      | 125,000          | 608            | 8.75%        | 10,200             |
| 125,000     | And Over         | 10,653         | 9.9%         | 125,000            |

Low Income Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,100            | 236            | 4.75%        | 0                  |
| 8,100       | 20,400           | 621            | 6.75%        | 8,100              |
| 20,400      | 50,000           | 1,451          | 8.75%        | 20,400             |

Low Income Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,050            | 236            | 4.75%        | 0                  |
| 4,050       | 10,200           | 428            | 6.75%        | 4,050              |
| 10,200      | 50,000           | 844            | 8.75%        | 10,200             |

#### Withholding changes for Rhode Island

For all Filing Status the Personal Exemption ($1,000) wage limit increased to $260,550

Withholding rates for taxpayers filing as *MAR* and *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 73,450           | 0              | 3.75%        | 0                  |
| 73,450      | 166,950          | 2,754.38       | 4.75%        | 73,450             |
| 166,950     | And Over         | 7,195.63       | 5.99%        | 166,950            |


#### Withholding changes for Vermont

The Personal Exemption amount is $4,850

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,538           | 0              | 0%           | 0                  |
| 10,538      | 86,388           | 0              | 3.35%        | 10,538             |
| 86,388      | 193,938          | 2,540.98       | 6.60%        | 86,388             |
| 193,938     | 289,988          | 9,639.28       | 7.60%        | 193,938            |
| 289,988     | And Over         | 16,939.08      | 8.75%        | 289,988            |

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,500            | 0              | 0%           | 0                  |
| 3,500       | 48,900           | 0              | 3.35%        | 3,500              |
| 48,900      | 113,550          | 1,520.90       | 6.60%        | 48,900             |
| 113,550     | 233,050          | 5,787.80       | 7.60%        | 113,550            |
| 233,050     | And Over         | 14,869.80      | 8.75%        | 233,050            |


#### Withholding changes for Arkansas

> [!NOTE]
> If you have employees set up to withhold Arkansas state tax, then, when you apply this update, you must also apply the [January 2023 Hotfix (code) for the Arkansas state](/dynamics/s-e/gp/mdgp2018_patchreleases_377) taxes to be correct for the year 2023. This change is for the Midrange Income look up part of the tax calculation.


Standard Deduction Amount is $2,270 from $2,200
Personal Exemption remains at $29.00

Tax Type rates for Filing Status NA


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,099            | 0              | 0.0%         | 0                  |
| 5,099       | 10,299           | -101.98        | 2.0%         | 0                  |
| 10,299      | 14,699           | -204.97        | 3.0%         | 0                  |
| 14,699      | 24,299           | -263.77        | 3.4%         | 0                  |
| 24,299      | 87,000           | -628.25        | 4.9%         | 0                  |
| 87,000      | 87,100           | -627.20        | 4.9%         | 0                  |
| 87,100      | 87,200           | -617.20        | 4.9%         | 0                  |
| 87,200      | 87,300           | -607.20        | 4.9%         | 0                  |
| 87,300      | 87,400           | -597.20        | 4.9%         | 0                  |
| 87,400      | 87,600           | -587.20        | 4.9%         | 0                  |
| 87,600      | 87,700           | -577.20        | 4.9%         | 0                  |
| 87,700      | 87,800           | -567.20        | 4.9%         | 0                  |
| 87,800      | 87,900           | -557.20        | 4.9%         | 0                  |
| 87,900      | 88,000           | -547.20        | 4.9%         | 0                  |
| 88,000      | 88,100           | -537.20        | 4.9%         | 0                  |
| 88,100      | 88,200           | -527.20        | 4.9%         | 0                  |
| 88,200      | 88,300           | -517.20        | 4.9%         | 0                  |
| 88,300      | 88,400           | -507.20        | 4.9%         | 0                  |
| 88,400      | 88,500           | -497.20        | 4.9%         | 0                  |
| 88,500      | 88,600           | -487.20        | 4.9%         | 0                  |
| 88,600      | 88,700           | -477.20        | 4.9%         | 0                  |
| 88,700      | 88,800           | -467.20        | 4.9%         | 0                  |
| 88,800      | 88,900           | -457.20        | 4.9%         | 0                  |
| 88,900      | 89,000           | -447.20        | 4.9%         | 0                  |
| 89,000      | 89,100           | -437.20        | 4.9%         | 0                  |
| 89,100      | 89,200           | -427.20        | 4.9%         | 0                  |
| 89,200      | 89,300           | -417.20        | 4.9%         | 0                  |
| 89,300      | 89,400           | -407.20        | 4.9%         | 0                  |
| 89,400      | 89,500           | -397.20        | 4.9%         | 0                  |
| 89,500      | 89,600           | -387.20        | 4.9%         | 0                  |
| 89,600      | 89,700           | -377.20        | 4.9%         | 0                  |
| 89,700      | 89,800           | -367.20        | 4.9%         | 0                  |
| 89,800      | 89,900           | -357.20        | 4.9%         | 0                  |
| 89,900      | 90,000           | -347.20        | 4.9%         | 0                  |
| 90,000      | 90,100           | -337.20        | 4.9%         | 0                  |
| 90,100      | 90,200           | -327.20        | 4.9%         | 0                  |
| 90,200      | 90,300           | -317.20        | 4.9%         | 0                  |
| 90,300      | 90,400           | -307.20        | 4.9%         | 0                  |
| 90,400      | 90,500           | -297.20        | 4.9%         | 0                  |
| 90,500      | 90,600           | -287.20        | 4.9%         | 0                  |
| 90,600      | 90,700           | -277.20        | 4.9%         | 0                  |
| 90,700      | 90,800           | -267.20        | 4.9%         | 0                  |
| 90,800      | 90,900           | -257.20        | 4.9%         | 0                  |
| 90,900      | 91,100           | -247.20        | 4.9%         | 0                  |
| 91,100      | 91,200           | -237.20        | 4.9%         | 0                  |
| 91,200      | 91,300           | -227.20        | 4.9%         | 0                  |
| 91,300      | 91,400           | -217.20        | 4.9%         | 0                  |
| 91,400      | 91,500           | -207.20        | 4.9%         | 0                  |
| 91,500      | 91,600           | -197.20        | 4.9%         | 0                  |
| 91,600      | 91,700           | -187.20        | 4.9%         | 0                  |
| 91,700      | 91,800           | -177.20        | 4.9%         | 0                  |
| 91,800      | And over         | -167.20        | 4.9%         | 0                  

Tax Type Special for Filing Status NA added

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 91,801           | 0              | 0%           | 50,000             |


## Changes in January Round 1 update (Released: 12/21/2022)

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

- FS01A -  .5% Flat Tax Rate from .8%
- FS02  - 1.0% Flat Tax Rate from 1.3%
- FS03  - 1.5% Flat Tax Rate from 1.8%
- FS04  - 2.0% Flat Tax Rate from 2.7%
- FS05  - 2.5% Flat Tax Rate from 3.6%
- FS06  - 3.0% Flat Tax Rate from 4.2%
- FS07  - 3.5% Flat Tax Rate from 5.1%

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
| 116,100     | And Over         | 7,371          | 7.15%        | 116,100            |

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

- Dependent Exemption: 1,500 For All Filing Status

- Standard Deduction: 4,600 for MAR1
- Personal Exemption: 12,000  for MAR1

- Standard Deduction: 2,300 for MAR2 
- Personal Exemption: 6,000  for MAR2

- Standard Deduction: 3,400 for HOH
- Personal Exemption: 9,500  for HOH

- Standard Deduction: 2,300 for SINGLE
- Personal Exemption: 6,000  for SINGLE

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
| 1,207       | 2,414            | 0.00           | 2.0%         | 1,207              |
| 2,414       | 3,621            | 24.00          | 2.5%         | 2,414              |
| 3,621       | 4,828            | 54.00          | 3.0%         | 3,621              |
| 4,828       | 6,035            | 90.00          | 3.5%         | 4,828              |
| 6,035       | 7,242            | 132.00         | 4.0%         | 6,035              |
| 7,242       | 8,449            | 180.00         | 4.5%         | 7,242              |
| 8,449       | And over         | 234.00         | 4.95%        | 8,449              |


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

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *4/9/2023*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
