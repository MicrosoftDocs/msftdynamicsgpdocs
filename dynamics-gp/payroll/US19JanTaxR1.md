---
title: "US payroll tax update"
description: "US 2023 Payroll Tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 1/25/2024
---
# U.S. 2024 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2024 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

This is the second tax update for 2024 and replaces all previous tax updates. It includes State tax table changes that take effect January 1, 2024. 

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

Check out these blogs for detailed documentation on how you calculate payroll taxes in Microsoft Dynamics GP:

[How to calculate Federal Tax with Dependent Claim Amount Field](https://community.dynamics.com/gp/b/dynamicsgp/posts/how-to-calculate-federal-tax-with-dependent-claim-amount)

[Does Microsoft Dynamics GP calculate tax correctly?](https://community.dynamics.com/gp/b/dynamicsgp/posts/is-microsoft-dynamics-gp-calculating-payroll-taxes-correctly)

[Tips to install the U.S. Payroll Tax Update](https://community.dynamics.com/gp/b/dynamicsgp/posts/tips-to-install-the-u-s-payroll-tax-update)

## Changes in January Round 2 update (Released 1/19/2024)

- Georgia
- Illinois
- Indiana
- Maryland
- Massachusetts
- Minnesota
- Mississippi
- North Dakota
- Vermont

### Withholding changes for Georgia

The Standard Deduction Amount for Filing Status:

- HOH, SINGLE, MFJ2I and MFS        is \$12,000
- MFJ1I                             is \$24,000

Subtract Personal Exemptions was removed from the calculation.

All filing status have a fixed flat tax of 5.49%.

### Withholding changes for Illinois

- The Dependent Exemptions is $2,775 from $2,425.
- The Flat tax rate remains at 4.95% and allowances at 1,000.

### Withholding changes for Indiana

The Flat tax rate is reduced to 3.05% from 3.15%.

### Withholding changes for Maryland

For each Filing Status of Maryland
Standard Deduction Minimum is $1,800 from $1,700
Standard Deduction Maximum is $2,700 from $2,550
The Standard Deduction Percent remains at 15 percent.

For Filing Status of AAMAR (Anne Arundel MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 75,000           | 0              | 7.50%        | 0                  |
| 75,000      | 150,000          | 0              | 7.60%        | 0                  |
| 150,000     | 175,000          | 11,400         | 7.85%        | 150,000            |
| 175,000     | 225,000          | 13,362.50      | 8.10%        | 175,000            |
| 225,000     | 300,000          | 17,412.50      | 8.35%        | 225,000            |
| 300,000     | 480,000          | 23,675         | 8.60%        | 300,000            |
| 480,000     | And over         | 24,725         | 8.950%       | 480,000            |

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
| 250,000     | 400,000          | 19,937.50      | 8.60%        | 250,000            |
| 400,000     | And over         | 20,812.50      | 8.950%        | 400,000           |

For Filing Status of CCMAR (Cecil MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.50%        | 0                  |
| 150,000     | 175,000          | 11,250         | 7.75%        | 150,000            |
| 175,000     | 225,000          | 13,187.50      | 8.00%        | 175,000            |
| 225,000     | 300,000          | 17,187.50      | 8.25%        | 225,000            |
| 300,000     | And over         | 23,375         | 8.50%        | 300,000            |

For Filing Status of CECIL (Cecil SGL/DEP/MFS).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.50%        | 5,000              |
| 100,000     | 125,000          | 7,500          | 7.75%        | 100,000            |
| 125,000     | 150,000          | 9,437.50       | 8.00%        | 125,000            |
| 150,000     | 250,000          | 11,437.50      | 8.25%        | 150,000            |
| 250,000     | And over         | 19,687.50      | 8.50%        | 250,000            |

For Filing Status of CLMAR (Caroline MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.95%        | 0                  |
| 150,000     | 175,000          | 11,925         | 8.20%        | 150,000            |
| 175,000     | 225,000          | 13,975.00      | 8.45%        | 175,000            |
| 225,000     | 300,000          | 18,200.00      | 8.70%        | 225,000            |
| 300,000     | And over         | 24,725         | 8.950%        | 300,000           |

For Filing Status of CVMAR (Calvert MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.75%        | 0                  |
| 150,000     | 175,000          | 11,625         | 8.000%       | 150,000            |
| 175,000     | 225,000          | 13,625         | 8.25%        | 175,000            |
| 225,000     | 300,000          | 17,750         | 8.50%        | 225,000            |
| 300,000     | And over         | 24,125         | 8.750%       | 300,000            |

For Filing Status of FREDRK (Frederick SGL/DEP/MFS).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 25,000           | 0              | 7.00%        | 0                  |
| 25,000      | 50,000           | 0              | 7.50%        | 0                  |
| 50,000      | 100,000          | 0              | 7.75%        | 0                  |
| 100,000     | 125,000          | 7,750          | 8.00%        | 100,000            |
| 125,000     | 150,000          | 9,750.00       | 8.25%        | 125,000            |
| 150,000     | 250,000          | 12,112.50      | 8.70%        | 150,000            |
| 250,000     | And over         | 20,812.50      | 8.95%        | 250,000            |

For Filing Status of FRMAR (Frederick MFJ/HOH).

Withholding rates for taxpayer:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 25,000           | 0              | 7.00%        | 0                  |
| 25,000      | 100,000          | 0              | 7.50%        | 0                  |
| 100,000     | 150,000          | 0              | 7.75%        | 0                  |
| 150,000     | 175,000          | 11,625         | 8.00%        | 150,000            |
| 175,000     | 225,000          | 13,625         | 8.25%        | 175,000            |
| 225,000     | 250,000          | 17,750         | 8.50%        | 225,000            |
| 250,000     | 300,000          | 18,200         | 8.70%        | 250,000            |
| 300,000     | And over         | 24,725         | 8.95%        | 300,000            |

### Withholding changes for Massachusetts

- Flat tax rate of 5% for all filing status.
- The Millionaires Tax (Surtax of 4% on employees that make over 1,000,000), which begin in January 1, 2023, is not supported by the Microsoft Dynamics GP tables.  

### Withholding changes for Minnesota

The Personal Exemption amount is \$5,050 for all Filing Status.

Withholding rates for taxpayers filing as *MAR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 14,000           | 0              | 0%           | 0                  |
| 14,000      | 60,330           | 0              | 5.35         | 14,000             |
| 60,330      | 198,040          | 2,478.66       | 6.80%        | 60,330             |
| 198,040     | 335,450          | 11,842.94      | 7.85%        | 198,040            |
| 335,450     | And Over         | 22,629.63      | 9.85%        | 297,260            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 4,475        | 0          | 0%       | 0              |
| 4,475   | 36,165       | 0          | 5.35%    | 4,475          |
| 36,165  | 108,565      | 1,695.42   | 6.80%    | 36,165         |
| 108,565 | 197,715      | 6,618.62   | 7.85%    | 108,565        |
| 197,715 | And Over     | 13,616.90  | 9.85%    | 197,715        |


### Withholding changes for Mississippi

Withholding rates for all Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,000           | 0              | 0            | 0                  |
| 10,000      | And over         | 0              | 4.7%         | 10,000             |


### Withholding changes for North Dakota

The Personal Exemption amount is \$4,300 for Filing Status MAR and SINGLE. 

> [!NOTE]
> Per the state of North Dakota, there is no HOH filing status with exemptions. If an employee on the W4 chooses filing status of HOH and does not mark step 2, you still choose HOH as the filing status in Dynamics GP.
>
> The state relies on the federal form W-4 to calculate the amount to withhold. Per the state, step 3 for dependent claim amount is not used for ND state tax withholding.

Withholding rates for taxpayers filing as *MAR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over    |
|-------------|------------------|----------------|--------------|-------------------|
| 0           | 53,988           | 0               | 0%          | 0                 |
| 53,988      | 159,588          | 0               | 1.95%       | 53,988            |
| 159,588     | And Over         | 2,059.20        | 2.50%       | 159,588           |

Withholding rates for taxpayers filing as *MARHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over    |
|-------------|------------------|----------------|--------------|-------------------|
| 0           | 51,975           | 0               | 0%          | 0                 |
| 51,975      | 152,150          | 0               | 1.95%       | 51,975            |
| 152,150     | And Over         | 1,953.41        | 2.50%       | 152,150           |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 54,450       | 0          | 0%       | 0              |
| 54,450  | 245,500      | 0          | 1.95%    | 54,450         |
| 245,500 | And Over     | 3,725.48   | 2.50%    | 245,500        |

Withholding rates for taxpayers filing as *SINGHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 52,025       | 0          | 0%       | 0              |
| 52,025  | 233,275      | 0          | 1.95%    | 52,025         |
| 233,275 | And Over     | 3,534.38   | 2.50%    | 233,275        |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 70,900       | 0          | 0%       | 0              |
| 70,900  | 261,500      | 0          | 1.95%    | 70,900         |
| 261,500 | And Over     | 3,716.70   | 2.50%    | 261,500        |

### Withholding changes for Vermont

The Personal Exemption amount is $5,100

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 11,138           | 0              | 0%           | 0                  |
| 11,138      | 91,088           | 0              | 3.35%        | 11,138             |
| 91,088      | 204,488          | 2,678.33       | 6.60%        | 91,088             |
| 204,488     | 305,788          | 10,162.73      | 7.60%        | 204,488            |
| 305,788     | And Over         | 17,861.53      | 8.75%        | 305,788            |

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,700            | 0              | 0%           | 0                  |
| 3,700       | 51,600           | 0              | 3.35%        | 3,700              |
| 51,600      | 119,700          | 1,604.65       | 6.60%        | 51,600             |
| 119,700     | 245,700          | 6,099.25       | 7.60%        | 119,700            |
| 245,700     | And Over         | 15,675.25      | 8.75%        | 245,700            |


## Changes in January Round 1 update (Released 12/20/2023)

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

### Withholding changes for Federal

The maximum taxable earnings for Social Security increase in 2024 to \$168,600 from \$160,200. 

**Federal tax tables released 12/19/2023**

The Personal Exemption is $4,300 for SINGLE, MAR, HOH, NRA

Withholding rates for taxpayers filing as *NRA*:

> [!NOTE]
> For non-resident aliens, if the employee filled out a W-4 after 01/01/2020, the filing status *Non Resident Alien HR (NRAHR)* must always be used.

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 16,300          | 0             | 0%          | 0                 |
| 16,300     | 27,900          | 0             | 10%         | 16,300            |
| 27,900     | 63,450          | 1,160.00      | 12%         | 27,900            |
| 63,450     | 116,825         | 5,426.00      | 22%         | 63,450            |
| 116,825    | 208,250         | 17,168.50     | 24%         | 116,825           |
| 208,250    | 260,025         | 39,110.50     | 32%         | 208,250           |
| 260,025    | 625,650         | 55,678.50     | 35%         | 260,025           |
| 625,650    | And Over        | 183,647.25    | 37%         | 625,650           |

Withholding rates for taxpayers filing as *NRAHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|             | 21,900           | 0              | 0%           | 0                  |
| 21,900      | 27,700           | 0              | 10%          | 21,900             |
| 27,700      | 45,475           | 580.00         | 12%          | 27,700             |
| 45,475      | 72,163           | 2,713.00       | 22%          | 45,475             |
| 72,163      | 117,875          | 8,584.25       | 24%          | 72,163             |
| 117,875     | 143,763          | 19,555.25      | 32%          | 117,875            |
| 143,763     | 326,575          | 27,839.25      | 35%          | 143,763            |
| 326,575     | And Over         | 91,823.63      | 37%          | 326,575            |


Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 16,300          | 0             | 0%          | 0                 |
| 16,300     | 39,500          | 0             | 10%         | 16,300            |
| 39,500     | 110,600         | 2,320.00      | 12%         | 39,500            |
| 110,600    | 217,350         | 10,852.00     | 22%         | 110,600           |
| 217,350    | 400,200         | 34,337.00     | 24%         | 217,350           |
| 400,200    | 503,750         | 78,221.00     | 32%         | 400,200           |
| 503,750    | 747,500         | 111,357.00    | 35%         | 503,750           |
| 747,500    | And Over        | 196,669.50    | 37%         | 747,500           |

Withholding rates for taxpayers filing as *MARHR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 14,600           | 0              | 0%           | 0                  |
| 14,600      | 26,200           | 0              | 10%          | 14,600             |
| 26,200      | 61,750           | 1,160.00       | 12%          | 26,200             |
| 61,750      | 115,125          | 5,426.00       | 22%          | 61,750             |
| 115,125     | 206,550          | 17,168.50      | 24%          | 115,125            |
| 206,550     | 258,325          | 39,110.50      | 32%          | 206,550            |
| 258,325     | 380,200          | 55,678.50      | 35%          | 258,325            |
| 380,200     | And Over         | 98,334.75      | 37%          | 380,200            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 6,000        | 0          | 0%       | 0              |
| 6,000   | 17,600       | 0          | 10%      | 6,000          |
| 17,600  | 53,150       | 1,160.00   | 12%      | 17,600         |
| 53,150  | 106,525      | 5,426.00   | 22%      | 53,150         |
| 106,525 | 197,950      | 17,168.50  | 24%      | 106,525        |
| 197,950 | 249,725      | 39,110.50  | 32%      | 197,950        |
| 249,725 | 615,350      | 55,678.50  | 35%      | 249,725        |
| 615,350 | And Over     | 183,647.25 | 37%      | 615,350        |

Withholding rates for taxpayers filing as *SGLHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over |
|-------------|------------------|----------------|----------|----------------|
| 0           | 7,300            | 0              | 0%       | 0              |
| 7,300       | 13,100           | 0              | 10%      | 7,300          |
| 13,100      | 30,875           | 580.00         | 12%      | 13,100         |
| 30,875      | 57,563           | 2,713.00       | 22%      | 30,875         |
| 57,563      | 103,275          | 8,584.25       | 24%      | 57,563         |
| 103,275     | 129,163          | 19,555.25      | 32%      | 103,275        |
| 129,163     | 311,975          | 27,839.25      | 35%      | 129,163        |
| 311,975     | And Over         | 91,823.63      | 37%     | 311,975        |

Withholding rates for taxpayers filing as *HOH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over    |
|-------------|------------------|----------------|----------|-------------------|
| 0           | 13,300           | 0              | 0%       | 0                 |
| 13,300      | 29,850           | 0              | 10%      | 13,300            |
| 29,850      | 76,400           | 1,655.00       | 12%      | 29,850            |
| 76,400      | 113,800          | 7,241.00       | 22%      | 76,400            |
| 113,800     | 205,250          | 15,469.00      | 24%      | 113,800           |
| 205,250     | 257,000          | 37,417.00      | 32%      | 205,250           |
| 257,000     | 622,650          | 53,997.00      | 35%      | 257,000           |
|622,650      | And Over         | 181,954.50     | 37%      | 622,650           |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 10,950           | 0              | 0%       | 0                  |
| 10,950      | 19,225           | 0              | 10%      | 10,950             |
| 19,225      | 42,500           | 827.50         | 12%      | 19,225             |
| 42,500      | 61,200           | 3,620.50       | 22%      | 42,500             |
| 61,200      | 106,925          | 7,734.50       | 24%      | 61,200             |
| 106,925     | 132,800          | 18,708.50      | 32%      | 106,925            |
| 132,800     | 315,625          | 26,988.50      | 35%      | 132,800            |
| 315,625     | And Over         | 90,977.25      | 37%      | 315,625            |


### Withholding changes for Alabama
Effective 1/1/2024 the state of Alabama has temporarily exempted all overtime wages from state tax. This will not be part of the Dynamics GP 2024 payroll tax tables. If you need this functionality in the product, you could set up a new pay code not subject to state tax, more manually tracked, or reach out to Greenshades for a more automated solution.

### Withholding changes for Arkansas

> [!NOTE]
> If you have employees set up to withhold Arkansas state tax, you need to be on version 18.5.1635 or later, for taxes to be correct for the year 2024. This change is for the Midrange Income look up part of the tax calculation.

- Standard Deduction Amount is $2,340 from $2,270
- Personal Exemption remains at $29.00

Tax Type rates for Filing Status NA:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,299            | 0              | 0.0%         | 0                  |
| 5,299       | 10,599           | -105.98        | 2.0%         | 0                  |
| 10,599      | 15,099           | -211.97        | 3.0%         | 0                  |
| 15,099      | 24,999           | -272.37        | 3.4%         | 0                  |
| 24,999      | 89,600           | -522.36        | 4.4%         | 0                  |
| 89,600      | 89,700           | -506.40        | 4.4%         | 0                  |
| 89,700      | 89,800           | -496.40        | 4.4%         | 0                  |
| 89,800      | 89,900           | -486.40        | 4.4%         | 0                  |
| 89,900      | 90,000           | -476.40        | 4.4%         | 0                  |
| 90,000      | 90,200           | -466.40        | 4.4%         | 0                  |
| 90,200      | 90,300           | -456.40        | 4.4%         | 0                  |
| 90,300      | 90,400           | -446.40        | 4.4%         | 0                  |
| 90,400      | 90,500           | -436.40        | 4.4%         | 0                  |
| 90,500      | 90,600           | -426.40        | 4.4%         | 0                  |
| 90,600      | 90,700           | -416.40        | 4.4%         | 0                  |
| 90,700      | 90,800           | -406.40        | 4.4%         | 0                  |
| 90,800      | 90,900           | -396.40        | 4.4%         | 0                  |
| 90,900      | 91,100           | -386.40        | 4.4%         | 0                  |
| 91,100      | 91,200           | -376.40        | 4.4%         | 0                  |
| 91,200      | 91,300           | -366.40        | 4.4%         | 0                  |
| 91,300      | 91,400           | -356.40        | 4.4%         | 0                  |
| 91,400      | 91,500           | -346.40        | 4.4%         | 0                  |
| 91,500      | 91,600           | -336.40        | 4.4%         | 0                  |
| 91,600      | 91,700           | -326.40        | 4.4%         | 0                  |
| 91,700      | 91,800           | -316.40        | 4.4%         | 0                  |
| 91,800      | 91,900           | -306.40        | 4.4%         | 0                  |
| 91,900      | 92,000           | -296.40        | 4.4%         | 0                  |
| 92,000      | 92,100           | -286.40        | 4.4%         | 0                  |
| 92,100      | 92,200           | -276.40        | 4.4%         | 0                  |
| 92,200      | 92,300           | -266.40        | 4.4%         | 0                  |
| 92,300      | 92,400           | -256.40        | 4.4%         | 0                  |
| 92,400      | 92,500           | -246.40        | 4.4%         | 0                  |
| 92,500      | 92,600           | -236.40        | 4.4%         | 0                  |
| 92,600      | 92,700           | -226.40        | 4.4%         | 0                  |
| 92,700      | 92,800           | -216.40        | 4.4%         | 0                  |
| 92,800      | 92,900           | -206.40        | 4.4%         | 0                  |
| 92,900      | 93,000           | -196.40        | 4.4%         | 0                  |
| 93,000      | 93,100           | -186.40        | 4.4%         | 0                  |
| 93,100      | 93,200           | -176.40        | 4.4%         | 0                  |
| 93,200      | 93,300           | -166.40        | 4.4%         | 0                  |
| 93,300      | 93,400           | -156.40        | 4.4%         | 0                  |
| 93,400      | 93,500           | -146.40        | 4.4%         | 0                  |
| 93,500      | 93,600           | -136.40        | 4.4%         | 0                  |
| 93,600      | 100,000          | -126.40        | 4.4%         | 0                  |
| 100,000     | And Over         | -126.40        | 4.4%         | 0                  |

Tax Type Special for Filing Status NA added:

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
| 1,000,000   | And Over         | 107,584.29     | 14.63%       | 1,000,000          |

Withholding rates for taxpayers filing as *MAR1* and *MAR2*:

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

### Withholding changes for Colorado

All filing status have the same fixed flat tax of 4.40% was 4.55% (2022).

- The Personal Exemption amount is $9,000 for MAR
- The Personal Exemption amount is $4,500 For SINGLE

**The following new filing status were added January 2022:**

- HOH1J - Head of Household 1 Job - Exemption amount  $19,500  
- MAR1J - Married Filing Jointly 1 Job - Exemption amount  $27,000  
- SIN1J - Single/Mar filing Single 1 Job - Exemption amount  $12,500  

In January 2022 the state of Colorado released a new form called [DR-0004](https://tax.colorado.gov/withholding-forms) this is optional for an employee to complete.  

There are 2 other parts to this form that have many different exemption amounts, we cannot accommodate all of them in the tax tables.

A new “OTHER” filing status was added (OTH1J) with Exemption increments of $500 that will accommodate all the "other" amounts on the form if an employee enters. 

OTH1J - OTH, +1 Jobs or Child Cr Allow - Exemption amount of $500

As an example, lets say I fill out the form and choose an amount of 2500. It does not match any of the above filing status so I would pick the OTHER status and put a 5 under Cards | Payroll | State Tax in the Number of Dependents field OR Additional Allowances. Which is 2500/500 = 5.

Another example, I put 5500 on the form. Again, it does not match the other filing status, so I choose *Other* and put *11*.

### Withholding changes for Connecticut

Withholding rates for taxpayers filing as *A*, *D*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,000           | 0              | 2%           | 0                  |
| 10,000      | 50,000           | 200            | 4.5%         | 10,000             |
| 50,000      | 50,250           | 2,000          | 5.5%         | 50,000             |
| 50,250      | 52,750           | 2,025          | 5.5%         | 50,000             |
| 52,750      | 55,250           | 2,050          | 5.5%         | 50,000             |
| 55,250      | 57,750           | 2,075          | 5.5%         | 50,000             |
| 57,750      | 60,250           | 2,100          | 5.5%         | 50,000             |
| 60,250      | 62,750           | 2,125          | 5.5%         | 50,000             |
| 62,750      | 65,250           | 2,150          | 5.5%         | 50,000             |
| 65,250      | 67,750           | 2,175          | 5.5%         | 50,000             |
| 67,750      | 70,250           | 2,200          | 5.5%         | 50,000             |
| 70,250      | 72,750           | 2,225          | 5.5%         | 50,000             |
| 72,750      | 100,000          | 2,250          | 5.5%         | 50,000             |
| 100,000     | 200,000          | 4,750          | 6.0%         | 100,000            |
| 200,000     | 250,000          | 10,750         | 6.5%         | 200,000            |
| 250,000     | 500,000          | 14,000         | 6.9%         | 250,000            |
| 500,000     | and over         | 31,250         | 6.99%        | 500,000            |


Withholding rates for taxpayers filing as *B*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 16,000           | 0              | 2%           | 0                  |
| 16,000      | 78,500           | 320            | 4.5%         | 16,000             |
| 78,500      | 78,500           | 360            | 4.5%         | 16,000             |
| 78,500      | 82,500           | 3,240          | 5.5%         | 80,000             |
| 82,500      | 86,500           | 3,280          | 5.5%         | 80,000             |
| 86,500      | 90,500           | 3,320          | 5.5%         | 80,000             |
| 90,500      | 94,500           | 3,360          | 5.5%         | 80,000             |
| 94,500      | 98,500           | 3,400          | 5.5%         | 80,000             |
| 98,500      | 102,500          | 3,440          | 5.5%         | 80,000             |
| 102,500     | 106,500          | 3,480          | 5.5%         | 80,000             |
| 106,500     | 110,500          | 3,520          | 5.5%         | 80,000             |
| 110,500     | 114,500          | 3,560          | 5.5%         | 80,000             |
| 114,500     | 160,000          | 3,600          | 5.5%         | 80,000             |
| 160,000     | 320,000          | 7,600          | 6.0%         | 160,000            |
| 320,000     | 400,000          | 17,200         | 6.5%         | 320,000            |
| 400,000     | 800,000          | 22,400         | 6.9%         | 400,000            |
| 800,000     | and over         | 50,000         | 6.99%        | 800,000            |

Withholding rates for taxpayers filing as *C*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 20,000           | 0              | 2%           | 0                  |
| 20,000      | 100,000          | 400            | 4.5%         | 20,000             |
| 100,000     | 100,500          | 4,000          | 5.5%         | 100,000            |
| 100,500     | 105,500          | 4,050          | 5.5%         | 100,000             |
| 105,500     | 110,500          | 4,100          | 5.5%         | 100,000             |
| 110,500     | 115,500          | 4,150          | 5.5%         | 100,000             |
| 115,500     | 120,500          | 4,200          | 5.5%         | 100,000             |
| 120,500     | 125,500          | 4,250          | 5.5%         | 100,000             |
| 125,500     | 130,500          | 4,300          | 5.5%         | 100,000             |
| 130,500     | 135,500          | 4,350          | 5.5%         | 100,000             |
| 135,500     | 140,500          | 4,400          | 5.5%         | 100,000             |
| 140,500     | 145,500          | 4,450          | 5.5%         | 100,000             |
| 145,500     | 200,000          | 4,500          | 5.5%         | 100,000             |
| 200,000     | 400,000          | 9,500          | 6.0%         | 200,000             |
| 400,000     | 500,000          | 21,500         | 6.5%         | 400,000             |
| 500,000     | 1,000,000        | 28,000         | 6.9%         | 500,000             |
| 1,000,000   | and over         | 62,500         | 6.99%        | 1,000,000           |

Withholding rates for taxpayers filing as *F*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,000           | 0              | 2%           | 0                  |
| 10,000      | 50,000           | 200            | 4.5%         | 10,000             |
| 50,000      | 56,500           | 2,000          | 5.5%         | 50,000             |
| 56,500      | 61,500           | 2,025          | 5.5%         | 50,000             |
| 61,500      | 66,500           | 2,050          | 5.5%         | 50,000             |
| 66,500      | 71,500           | 2,075          | 5.5%         | 50,000             |
| 71,500      | 76,500           | 2,100          | 5.5%         | 50,000             |
| 76,500      | 81,500           | 2,125          | 5.5%         | 50,000             |
| 81,500      | 86,500           | 2,150          | 5.5%         | 50,000             |
| 86,500      | 91,500           | 2,175          | 5.5%         | 50,000             |
| 91,500      | 96,500           | 2,200          | 5.5%         | 50,000             |
| 96,500      | 100,000          | 2,250          | 5.5%         | 50,000             |
| 100,000     | 101,500          | 4,750          | 6.0%         | 100,000            |
| 101,500     | 200,000          | 10,750         | 6.5%         | 100,000            |
| 200,000     | 250,000          | 14,000         | 6.9%         | 200,000            |
| 250,000     | 500,000          | 14,000         | 6.9%         | 250,000            |
| 500,000     | and over         | 31,250         | 6.99%        | 500,000            |

Low Income Tax Type rates for *A*, *D* and *F* Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 105,000          | 0              | 0%           | 0                  |
| 105,000     | 110,000          | 25             | 0%           | 0                  |
| 110,000     | 115,000          | 50             | 0%           | 0                  |
| 115,000     | 120,000          | 75             | 0%           | 0                  |
| 120,000     | 125,000          | 100            | 0%           | 0                  |
| 125,000     | 130,000          | 125            | 0%           | 0                  |
| 130,000     | 135,000          | 150            | 0%           | 0                  |
| 135,000     | 140,000          | 175            | 0%           | 0                  |
| 140,000     | 145,000          | 200            | 0%           | 0                  |
| 145,000     | 150,000          | 225            | 0%           | 0                  |
| 150,000     | 200,000          | 250            | 0%           | 0                  |
| 200,000     | 205,000          | 340            | 0%           | 0                  |
| 205,000     | 210,000          | 430            | 0%           | 0                  |
| 210,000     | 215,000          | 520            | 0%           | 0                  |
| 215,000     | 220,000          | 610            | 0%           | 0                  |
| 220,000     | 225,000          | 700            | 0%           | 0                  |
| 225,000     | 230,000          | 790            | 0%           | 0                  |
| 230,000     | 235,000          | 880            | 0%           | 0                  |
| 235,000     | 240,000          | 970            | 0%           | 0                  |
| 240,000     | 245,000          | 1,060          | 0%           | 0                  |
| 245,000     | 250,000          | 1,150          | 0%           | 0                  |
| 250,000     | 255,000          | 1,240          | 0%           | 0                  |
| 255,000     | 260,000          | 1,330          | 0%           | 0                  |
| 260,000     | 265,000          | 1,420          | 0%           | 0                  |
| 265,000     | 270,000          | 1,510          | 0%           | 0                  |
| 270,000     | 275,000          | 1,600          | 0%           | 0                  |
| 275,000     | 280,000          | 1,690          | 0%           | 0                  |
| 280,000     | 285,000          | 1,780          | 0%           | 0                  |
| 285,000     | 290,000          | 1,870          | 0%           | 0                  |
| 290,000     | 295,000          | 1,960          | 0%           | 0                  |
| 295,000     | 300,000          | 2,050          | 0%           | 0                  |
| 300,000     | 305,000          | 2,140          | 0%           | 0                  |
| 305,000     | 310,000          | 2,230          | 0%           | 0                  |
| 310,000     | 315,000          | 2,320          | 0%           | 0                  |
| 315,000     | 320,000          | 2,410          | 0%           | 0                  |
| 320,000     | 325,000          | 2,500          | 0%           | 0                  |
| 325,000     | 330,000          | 2,590          | 0%           | 0                  |
| 330,000     | 335,000          | 2,680          | 0%           | 0                  |
| 335,000     | 340,000          | 2,770          | 0%           | 0                  |
| 340,000     | 345,000          | 2,860          | 0%           | 0                  |
| 345,000     | 500,000          | 2,950          | 0%           | 0                  |
| 500,000     | 505,000          | 3,000          | 0%           | 0                  |
| 505,000     | 510,000          | 3,050          | 0%           | 0                  |
| 510,000     | 515,000          | 3,100          | 0%           | 0                  |
| 515,000     | 520,000          | 3,150          | 0%           | 0                  |
| 520,000     | 525,000          | 3,200          | 0%           | 0                  |
| 525,000     | 530,000          | 3,250          | 0%           | 0                  |
| 530,000     | 535,000          | 3,300          | 0%           | 0                  |
| 535,000     | 540,000          | 3,350          | 0%           | 0                  |
| 540,000     | And over         | 3,400          | 0%           | 0                  |

Low Income Tax Type rates for *B* Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 168,000          | 0              | 0%           | 0                  |
| 168,000     | 176,000          | 40             | 0%           | 0                  |
| 176,000     | 184,000          | 80             | 0%           | 0                  |
| 184,000     | 192,000          | 120            | 0%           | 0                  |
| 192,000     | 200,000          | 160            | 0%           | 0                  |
| 200,000     | 208,000          | 200            | 0%           | 0                  |
| 208,000     | 216,000          | 240            | 0%           | 0                  |
| 216,000     | 224,000          | 280            | 0%           | 0                  |
| 224,000     | 232,000          | 320            | 0%           | 0                  |
| 232,000     | 240,000          | 360            | 0%           | 0                  |
| 240,000     | 320,000          | 400            | 0%           | 0                  |
| 320,000     | 328,000          | 540            | 0%           | 0                  |
| 328,000     | 336,000          | 680            | 0%           | 0                  |
| 336,000     | 344,000          | 820            | 0%           | 0                  |
| 344,000     | 352,000          | 960            | 0%           | 0                  |
| 352,000     | 360,000          | 1,100          | 0%           | 0                  |
| 360,000     | 368,000          | 1,240          | 0%           | 0                  |
| 368,000     | 376,000          | 1,380          | 0%           | 0                  |
| 376,000     | 384,000          | 1,520          | 0%           | 0                  |
| 384,000     | 392,000          | 1,660          | 0%           | 0                  |
| 392,000     | 400,000          | 1,800          | 0%           | 0                  |
| 400,000     | 408,000          | 1,940          | 0%           | 0                  |
| 408,000     | 416,000          | 2,080          | 0%           | 0                  |
| 416,000     | 424,000          | 2,220          | 0%           | 0                  |
| 424,000     | 432,000          | 2,360          | 0%           | 0                  |
| 432,000     | 440,000          | 2,500          | 0%           | 0                  |
| 440,000     | 448,000          | 2,640          | 0%           | 0                  |
| 448,000     | 456,000          | 2,780          | 0%           | 0                  |
| 456,000     | 464,000          | 2,920          | 0%           | 0                  |
| 464,000     | 472,000          | 3,060          | 0%           | 0                  |
| 472,000     | 480,000          | 3,200          | 0%           | 0                  |
| 480,000     | 488,000          | 3,340          | 0%           | 0                  |
| 488,000     | 496,000          | 3,480          | 0%           | 0                  |
| 496,000     | 504,000          | 3,620          | 0%           | 0                  |
| 504,000     | 512,000          | 3,760          | 0%           | 0                  |
| 512,000     | 520,000          | 3,900          | 0%           | 0                  |
| 520,000     | 528,000          | 4,040          | 0%           | 0                  |
| 528,000     | 536,000          | 4,180          | 0%           | 0                  |
| 536,000     | 544,000          | 4,320          | 0%           | 0                  |
| 544,000     | 552,000          | 4,460          | 0%           | 0                  |
| 552,000     | 800,000          | 4,600          | 0%           | 0                  |
| 800,000     | 808,000          | 4,680          | 0%           | 0                  |
| 808,000     | 816,000          | 4,760          | 0%           | 0                  |
| 816,000     | 824,000          | 4,840          | 0%           | 0                  |
| 824,000     | 832,000          | 4,920          | 0%           | 0                  |
| 832,000     | 840,000          | 5,000          | 0%           | 0                  |
| 840,000     | 848,000          | 5,080          | 0%           | 0                  |
| 848,000     | 856,000          | 5,160          | 0%           | 0                  |
| 856,000     | 864,000          | 5,240          | 0%           | 0                  |
| 864,000     | And over         | 5,320          | 0%           | 0                  |

### Withholding changes for Iowa

Iowa withholding calculations, federal withholding is no longer subtracted from taxable wages.  

> [!NOTE]
> Iowa W4 changed in the year 2024 and the tax tables support the amounts, they are held in the Personal Exemption table below.

- Standard Deduction for EXP1 is $14,600 previously \$13,850
- Standard Deduction for EXP2 is $29,200 previously \$27,700

Withholding rates for taxpayers filing as EXP1 and EXP2 are as follows:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,896            | 0              | 4.40%        |                    |
| 4,896       | 24,480           | 215.42         | 4.82%        | 4,896              |
| 24,480      | And over         | 1,159.37       | 5.70%        | 24,480             |

Personal Exemption Tax Type rates for ALL filling Status:

| If Over  |But Not Over | Tax Amoun   | Tax Rate     | On Excess Over     |
|----------|-------------|-------------|--------------|--------------------|
| 0        | 1           | 40          | 0%           | 0                  |
| 1        | 2           | 80          | 0%           | 0                  |
| 2        | 3           | 120         | 0%           | 0                  |
| 3        | 4           | 160         | 0%           | 0                  |
| 4        | 5           | 200         | 0%           | 0                  |
| 5        | 6           | 240         | 0%           | 0                  |
| 6        | 7           | 280         | 0%           | 0                  |
| 7        | 8           | 320         | 0%           | 0                  |
| 8        | 9           | 360         | 0%           | 0                  |
| 9        | 10          | 400         | 0%           | 0                  |
| 10       | 11          | 440         | 0%           | 0                  |
| 11       | 12          | 480         | 0%           | 0                  |
| 12       | 13          | 520         | 0%           | 0                  |
| 13       | 14          | 560         | 0%           | 0                  |
| 14       | 15          | 600         | 0%           | 0                  |
| 15       | 16          | 640         | 0%           | 0                  |
| 16       | 17          | 680         | 0%           | 0                  |
| 17       | 18          | 720         | 0%           | 0                  |
| 18       | 19          | 760         | 0%           | 0                  |
| 19       | 20          | 800         | 0%           | 0                  |
| 20       | 21          | 840         | 0%           | 0                  |


### Withholding changes for Kentucky

- The Standard Deduction Amount is $3,160 from $2,980
- The Tax Rate decreases to 4.0% formerly 4.5%

### Withholding changes for Maine

- Personal Exemption is $5,000 was $4,700

Withholding rates for taxpayers filing as *SINGLE*, Tax table type:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 26,050           | 0              | 5.8%         | 0                  |
| 26,050      | 61,600           | 1,511          | 6.75%        | 26,050             |
| 61,600      | And over         | 3,911          | 7.15%        | 61,600             |

Special table type:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 95,150           | 0              | 0            | 11,750             |
| 97,150      | 172,150          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 52,100           |                | 5.80%        | 0                  |
| 52,100      | 123,250          | 3,022          | 6.75%        | 52,100             |
| 123,250     | And Over         | 7,875          | 7.15%        | 123,250            |

Special table type:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 194,300          | 0              | 0            | 26,350             |
| 194,300     | 344,300          | 150,000        | 0            | 0                  |

### Withholding changes for Michigan

- The Personal Exemption Amount is $5,600 from $5,000
- The Tax Rate remains at 4.25%

### Withholding changes for Missouri

- The Standard Deduction is $21,900 prior \$20,800 for filing status HOH
- The Standard Deduction is $29,200 prior \$27,700 for filing status MAR1
- The Standard Deduction is $14,600 prior \$13,850 for filing status MAR2 and SINGLE

Withholding rates for all filing status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,273            | 0              | 0%           | 0                  |
| 1,273       | 2,546            | 0              | 2.0%         | 1,273              |
| 2,546       | 3,819            | 25             | 2.5%         | 2,546              |
| 3,819       | 5,092            | 57             | 3.0%         | 3,819              |
| 5,092       | 6,365            | 95             | 3.5%         | 5,092              |
| 6,0365      | 7,638            | 140            | 4.0%         | 6,365              |
| 7,638       | 8,911            | 191            | 4.5%         | 7,638              |
| 8,911       | And over         | 248            | 4.8%         | 8,911              |

### Withholding changes for Montana

The Personal Exemption amount is $0 formerly $2,070 

Tax Type rates for MAR Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 29,200           | 0              | 0%           | 0                  |
| 29,200      | 70,200           | 0              | 4.70%        | 29,200             |
| 70,200      | And Over         | 1,927          | 5.9%         | 70,200             |

Tax Type rates for SINGLE Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 14,600           | 0              | 0%           | 0                  |
| 14,600      | 35,100           | 0              | 4.70%        | 14,600             |
| 35,100      | And Over         | 964            | 5.9%         | 35,100             |


### Withholding changes for Nebraska

The Personal Exemption amount is $2,250 formerly \$2,140 for Filing Status MAR and SINGLE.

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,680            | 0              | 0            | 0                  |
| 7,680       | 12,190           | 0              | 2.26%        | 7,680              |
| 12,190      | 30,360           | 101.93         | 3.22%        | 12,190             |
| 30,360      | 47,230           | 687.00         | 4.91%        | 30,360             |
| 47,230      | 58,600           | 1,515.32       | 5.77%        | 47,230             |
| 58,600      | 77,710           | 2,171.37       | 5.94%        | 58,600             |
| 77,710      | And over         | 3,306.50       | 6.10%        | 77,710             |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,210            | 0              | 0            | 0                  |
| 3,210       | 6,290            | 0              | 2.26%        | 3,210              |
| 6,290       | 20,440           | 69.61          | 3.22%        | 6,290              |
| 20,440      | 29,620           | 525.24         | 4.91%        | 20,440             |
| 29,620      | 37,610           | 975.98         | 5.77%        | 29,620             |
| 37,610      | 70,630           | 1,437.00       | 5.94%        | 37,610             |
| 70,630      | And over         | 3,398.39       | 6.10%        | 70,630             |

### Withholding changes for New Mexico

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 14,600           | 0              | 0%           | 0                  |
| 14,600      | 22,600           | 0              | 1.70%        | 14,600             |
| 22,600      | 30,600           | 136.00         | 3.2%         | 22,600             |
| 30,600      | 38,600           | 392.00         | 4.7%         | 30,600             |
| 38,600      | 54,600           | 768.00         | 4.9%         | 38,600             |
| 54,600      | 78,600           | 1,552.00       | 4.9%         | 54,600             |
| 78,600      | 114,600          | 2,728.00       | 4.9%         | 78,600             |
| 114,600     | 214,600          | 4,492.00       | 4.9%         | 114,600            |
| 214,600     | 329,600          | 9,392.00       | 4.9%         | 214,600            |
| 329,600     | And Over         | 15,027.00      | 5.9%         | 329,600            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,300            | 0              | 0%           | 0                  |
| 7,300       | 12,800           | 0              | 1.7%         | 7,300              |
| 12,800      | 18,300           | 93.50          | 3.2%         | 12,800             |
| 18,300      | 23,300           | 269.50         | 4.7%         | 18,300             |
| 23,300      | 33,300           | 504.50         | 4.9%         | 23,300             |
| 33,300      | 49,300           | 994.50         | 4.9%         | 33,300             |
| 49,300      | 72,300           | 1,778.50       | 4.9%         | 49,300             |
| 72,300      | 132,300          | 2,905.50       | 4.9%         | 72,300             |
| 132,300     | 217,300          | 5,845.50       | 4.9%         | 132,300            |
| 217,300     | And Over         | 10,010.50      | 5.9%         | 217,300            |

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,950           | 0              | 0%           | 0                  |
| 10,950      | 18,950           | 0              | 1.7%         | 10,950             |
| 18,950      | 26,950           | 136.00         | 3.2%         | 18,950             |
| 26,950      | 34,950           | 392.00         | 4.7%         | 26,950             |
| 34,950      | 50,950           | 768.00         | 4.9%         | 34,950             |
| 50,950      | 74,950           | 1,552.00       | 4.9%         | 50,950             |
| 74,950      | 110,950          | 2,728.00       | 4.9%         | 74,950             |
| 110,950     | 210,950          | 4,492.00       | 4.9%         | 110,950            |
| 210,950     | 325,950          | 9,392.00       | 4.9%         | 210,950            |
| 325,950     | And Over         | 15,027.00      | 5.9%         | 325,950            |

### Withholding changes for North Carolina

- Standard Deduction for HOH remains at $19,125
- Standard Deduction for MAR and SINGLE remains at $12,750
- Tax rate for all filing status is 4.6%

### Withholding changes for Oregon

- The Standard Deduction Amount is \$5,495 for MS3 and S3 Filing Status.
- The Standard Deduction Amount is \$2,745 for S2 Filing Status.
- The Personal Exemption amount is \$249 for all Filing Status.
- New Filing status for 2020 *NOWH* (No Withholding Provided) Flat tax rate of 8% (remains for 2024 year)
- HB2119 requires employers to withhold income tax at a rate of 8 percent of employee wages if they employee has not provided a withholding statement or exemption certificate. Continue withholding at the 8 percent rate until the employee submits a withholding statement and exemption certificate.

Special Tax Type rates for MS3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 8,250          | 0%           | 0                  |
| 49,999      | 249,999          | 8,250          | 0%           | 0                  |
| 249,999     | 259,999          | 6,600          | 0%           | 0                  |
| 259,999     | 269,999          | 4,950          | 0%           | 0                  |
| 269,999     | 279,999          | 3,300          | 0%           | 0                  |
| 279,999     | 289,999          | 1,650          | 0%           | 0                  |
| 289,999     | And over         | 0              | 0%           | 0                  |
|             |                  |                |              |                    |

Special Tax Type rates for S2 and S3 Filing Status:

| If Over     |     But Not Over | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 8,250          | 0%           | 0                  |
| 49,999      | 124,999          | 8,250          | 0%           | 0                  |
| 124,999     | 129,999          | 6,600          | 0%           | 0                  |
| 129,999     | 134,999          | 4,950          | 0%           | 0                  |
| 134,999     | 139,999          | 3,300          | 0%           | 0                  |
| 139,999     | 144,999          | 1,650          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

Tax Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 36,255           | 0              | 0%           | 0                  |
| 36,255      | 250,000          | 1,280          | 8.75%        | 21,500             |
| 250,000     | And over         | 21,274         | 9.9%         | 250,000            |

Tax Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 39,005           | 0              | 0%           | 0                  |
| 39,005      | 125,000          | 639            | 8.75%        | 10,750             |
| 125,000     | And Over         | 10,636         | 9.9%         | 125,000            |

Low Income Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,600            | 249            | 4.75%        | 0                  |
| 8,600       | 21,500           | 658            | 6.75%        | 8,600              |
| 21,500      | 50,000           | 1,529          | 8.75%        | 21,500             |

Low Income Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,300            | 249            | 4.75%        | 0                  |
| 4,300       | 10,750           | 453            | 6.75%        | 4,300              |
| 10,750      | 50,000           | 888            | 8.75%        | 10,750             |


### Withholding changes for Rhode Island

For all Filing Status the Personal Exemption ($1,000) wage limit increased to $274,650

Withholding rates for taxpayers filing as *MAR* and *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 77,450           | 0              | 3.75%        | 0                  |
| 77,450      | 176,050          | 2,904.38       | 4.75%        | 77,450             |
| 176,050     | And Over         | 7,587.88       | 5.99%        | 176,050            |

### Withholding changes for South Carolina

- The Personal Exemption is $4,610 for Filing Status ONE.
- The Standard Deduction Maximum is $6,925 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,460            | 0              | 0.0%         | 0                  |
| 3,460       | 17,330           | -103.80        | 3.0%         | 0                  |
| 17,330      | And over         | -693.02        | 6.4%         | 0                  |


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

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *1/25/2024*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
