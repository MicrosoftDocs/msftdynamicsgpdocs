---
title: "US payroll tax update"
description: "US 2026 Payroll Tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 4/1/2026
---
# U.S. 2026 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2026 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

This is the fourth tax update for 2026 and replaces all previous tax updates. It includes State tax table changes that take effect January 1, 2026. 

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

Check out these blogs for documentation on how you calculate payroll taxes in Microsoft Dynamics GP:

[How to calculate Federal Tax with Dependent Claim Amount Field](https://community.dynamics.com/blogs/post/?postid=f65a8b3b-ef87-432c-a3c4-80ed7077a79d)

[Does Microsoft Dynamics GP calculate tax correctly?](https://community.dynamics.com/blogs/post/?postid=c9a75bcc-8f50-411f-a364-95a5121f6335)

[Tips to install the U.S. Payroll Tax Update](https://community.dynamics.com/blogs/post/?postid=dbc1295b-297f-4441-aa2f-7c2502bffc97)

## Changes in April Round 4 update (Released 4/7/2026)

- West Virginia

### Withholding changes for West Virginia

The Personal Exemption amount is $2,000 For all filing status.

Withholding rates for taxpayers filing as PM (Percentage Method) are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 10,000           | 0              | 2.11%    | 0                  |
| 10,000      | 25,000           | 211.00         | 2.81%    | 10,000             |
| 25,000      | 40,000           | 632.50         | 3.16%    | 25,000             |
| 40,000      | 60,000           | 1,106.50       | 4.22%    | 40,000             |
| 60,000      | and over         | 1,950.50       | 4.58%    | 60,000             |

Withholding rates for taxpayers filing as TE (Two Earner Option) are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 7,500            | 0              | 2.11%    | 0                  |
| 7,500       | 18,750           | 158.25         | 2.81%    | 7,500              |
| 18,750      | 30,000           | 474.38         | 3.16%    | 18,750             |
| 30,000      | 45,000           | 829.88         | 4.22%    | 30,000             |
| 45,000      | and over         | 1,462.88       | 4.58%    | 45,000             |

## Changes in February Round 3 update (Released 2/27/2026)

- Maryland

### Withholding changes for Maryland

For each Filing Status of Maryland:
The state of Maryland changed its payroll tax standard deduction from a percentage-based calculation to a flat amount of $3,400 for all filing status.

For Filing Status of ALGENY (Allegany).
Withholding rates for taxpayer:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.95%        | 5,000              |
| 100,000     | 125,000          | 7,950          | 8.20%        | 100,000            |
| 125,000     | 150,000          | 10,000         | 8.45%        | 125,000            |
| 150,000     | 250,000          | 12,112.50      | 8.70%        | 150,000            |
| 250,000     | 500,000          | 20,812.50      | 8.95%        | 250,000            |
| 500,000     | 1,000,000        | 43,187.50      | 9.45%        | 500,000            |
| 1,000,000   | And over         | 90,437.50      | 9.70%        | 1,000,000          |

For Filing Status of ALMAR (Allegany)
Withholding rates for taxpayer:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.95%        | 5,000              |
| 150,000     | 175,000          | 11,925         | 8.20%        | 150,000            |
| 175,000     | 225,000          | 13,975         | 8.45%        | 175,000            |
| 225,000     | 300,000          | 18,200         | 8.70%        | 225,000            |
| 300,000     | 600,000          | 24,725         | 8.95%        | 300,000            |
| 600,000     | 1,200,000        | 51,575         | 9.45%        | 600,000            |
| 1,200,000   | And over         | 108,275        | 9.70%        | 1,200,000          |

For Filing Status of KENT
Withholding rates for taxpayer:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 8.05%        | 5,000              |
| 100,000     | 125,000          | 8,050          | 8.30%        | 100,000            |
| 125,000     | 150,000          | 10,125         | 8.55%       | 125,000            |
| 150,000     | 250,000          | 12,262.50      | 8.80%        | 150,000            |
| 250,000     | 500,000          | 21,062.50      | 9.05%        | 250,000            |
| 500,000     | 1,000,000        | 43,687.50      | 9.55%        | 500,000            |
| 1,000,000   | And over         | 91,437.50      | 9.80%        | 1,000,000          |

For Filing Status of KNMAR
Withholding rates for taxpayer:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 8.05%        | 5,000              |
| 150,000     | 175,000          | 12,075         | 8.30%        | 150,000            |
| 175,000     | 225,000          | 14,150         | 8.55%        | 175,000            |
| 225,000     | 300,000          | 18,425         | 8.80%        | 225,000            |
| 300,000     | 600,000          | 25,025         | 9.05%        | 300,000            |
| 600,000     | 1,200,000        | 52,175         | 9.55%        | 600,000            |
| 1,200,000   | And over         | 109,475        | 9.80%        | 1,200,000          |

## Changes in January Round 2 update (Released 1/22/2026)

- Arkansas
- Illinois
- Indiana
- Louisiana
- Minnesota
- Michigan
- Mississippi
- Montana
- North Carolina
- North Dakota
- Oregon
- Vermont

### Withholding changes for Arkansas

> [!NOTE]
> If you have employees set up to withhold Arkansas state tax, you need to be on version 18.5.1635 or later, for taxes to be correct for the year 2024 or later.

This change is for the Midrange Income look up part of the tax calculation.

- Standard Deduction Amount is $2,470
- Personal Exemption remains at $29.00

Tax Type rates for Filing Status NA:

| If Over | But Not Over  | Tax Amount  | Tax Rate| On Excess Over|
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,599            | 0              | 0.0%         | 0                  |
| 5,599       | 11,199           | -111.98        | 2.0%         | 0                  |
| 11,199      | 15,999           | -223.97        | 3.0%         | 0                  |
| 15,999      | 26,399           | -287.97        | 3.4%         | 0                  |
| 26,399      | 94,700           | -419.96        | 3.9%         | 0                  |
| 94,700      | 94,800           | -399.30        | 3.9%         | 0                  |
| 94,800      | 94,900           | -389.30        | 3.9%         | 0                  |
| 94,900      | 95,000           | -379.30        | 3.9%         | 0                  |
| 95,000      | 95,100           | -369.30        | 3.9%         | 0                  |
| 95,100      | 95,200           | -359.30        | 3.9%         | 0                  |
| 95,200      | 95,300           | -349.30        | 3.9%         | 0                  |
| 95,300      | 95,400           | -339.30        | 3.9%         | 0                  |
| 95,400      | 95,500           | -329.30        | 3.9%         | 0                  |
| 95,500      | 95,600           | -319.30        | 3.9%         | 0                  |
| 95,600      | 95,700           | -309.30        | 3.9%         | 0                  |
| 95,700      | 95,800           | -299.30        | 3.9%         | 0                  |
| 95,800      | 95,900           | -289.30        | 3.9%         | 0                  |
| 95,900      | 96,000           | -279.30        | 3.9%         | 0                  |
| 96,000      | 96,100           | -269.30        | 3.9%         | 0                  |
| 96,100      | 96,200           | -259.30        | 3.9%         | 0                  |
| 96,200      | 96,300           | -249.30        | 3.9%         | 0                  |
| 96,300      | 96,400           | -239.30        | 3.9%         | 0                  |
| 96,400      | 96,500           | -229.30        | 3.9%         | 0                  |
| 96,500      | 96,600           | -219.30        | 3.9%         | 0                  |
| 96,600      | 96,700           | -209.30        | 3.9%         | 0                  |
| 96,700      | 96,800           | -199.30        | 3.9%         | 0                  |
| 96,800      | 96,900           | -189.30        | 3.9%         | 0                  |
| 96,900      | 97,000           | -179.30        | 3.9%         | 0                  |
| 97,000      | 97,100           | -169.30        | 3.9%         | 0                  |
| 97,100      | 97,200           | -159.30        | 3.9%         | 0                  |
| 97,200      | 97,300           | -149.30        | 3.9%         | 0                  |
| 97,300      | 97,400           | -139.30        | 3.9%         | 0                  |
| 97,400      | 97,500           | -129.30        | 3.9%         | 0                  |
| 97,500      | 97,600           | -119.30        | 3.9%         | 0                  |
| 97,600      | 97,700           | -109.30        | 3.9%         | 0                  |
| 97,700      | 97,800           | -99.30         | 3.9%         | 0                  |
| 97,800      | And Over         | -89.30         | 3.9%         | 0                  |

### Withholding changes for Illinois

- The Dependent Exemptions is $2,925 from $2,850.
- The Flat tax rate remains at 4.95% and allowances at 1,000.

### Withholding changes for Indiana

The Flat tax rate is reduced to 2.95% from 3.00%.

### Withholding changes for Louisiana

> [!NOTE]
> If you have [employees set up to withhold Louisiana state tax](https://community.dynamics.com/blogs/post/?postid=fdba817d-a7d9-ef11-a730-7c1e527e6b0e), you need to be on version 18.7.1801 or later, for taxes to be correct for the year 2025 or later. 

- The flat tax rate for all filing remains at 3.09
- Special Type rates & Dependent Exemption for all filing status removed (2025)
- Standard Deduction for EXEMPT $0.00 
- Standard Deduction for SM1 $12,875
- Standard Deduction for M2 $25,750

### Withholding changes for Michigan

- The Personal Exemption Amount is $5,900 from $5,800
- The Tax Rate remains at 4.25%

### Withholding changes for Minnesota

The Personal Exemption amount is \$5,300 for all Filing Status.

Withholding rates for taxpayers filing as *MAR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 14,700           | 0              | 0%           | 0                  |
| 14,700      | 63,420           | 0              | 5.35%        | 14,700             |
| 63,420      | 208,180          | 2,605.45       | 6.80%        | 63,400             |
| 208,180     | 352,630          | 12,450.49      | 7.85%        | 208,180            |
| 352,630     | And Over         | 23,789.82      | 9.85%        | 352,630            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 4,700        | 0          | 0%       | 0              |
| 4,700   | 38,010       | 0          | 5.35%    | 4,700          |
| 38,010  | 114,130      | 1,782.09   | 6.80%    | 38,010         |
| 114,130 | 207,850      | 6,958.25   | 7.85%    | 114,130        |
| 207,850 | And Over     | 14,315.27  | 9.85%    | 207,850        |

### Withholding changes for Mississippi

Withholding rates for all Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,000           | 0              | 0            | 0                  |
| 10,000      | And over         | 0              | 4.0%         | 10,000             |

### Withholding changes for Montana

The Personal Exemption amount is $0 formerly $2,070 (2023). 

Tax Type rates for MAR Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 32,200           | 0              | 0%           | 0                  |
| 32,200      | 127,200          | 0              | 4.70%        | 32,200             |
| 127,200     | And Over         | 4,465          | 5.65%        | 127,200             |

Tax Type rates for SINGLE Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 16,100           | 0              | 0%           | 0                  |
| 16,100      | 63,600           | 0              | 4.70%        | 16,100             |
| 63,600      | And Over         | 2,233          | 5.65%        | 63,600             |

Tax Type rates for HOH Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 24,150           | 0              | 0%           | 0                  |
| 24,150      | 95,400           | 0              | 4.70%        | 24,150             |
| 95,400      | And Over         | 3,349          | 5.65%        | 95,400             |


### Withholding changes for North Carolina

- Standard Deduction for HOH remains at $19,125
- Standard Deduction for MAR and SINGLE remains at $12,750
- Tax rate for all filing status is 4.09%

### Withholding changes for North Dakota

The Personal Exemption amount is \$5,050 for Filing Status MAR and SINGLE. 

> [!NOTE]
> Per the state of North Dakota, there is no HOH filing status with exemptions. If an employee on the W4 chooses filing status of HOH and does not mark step 2, you still choose HOH as the filing status in Dynamics GP.
>
> The state relies on the federal form W-4 to calculate the amount to withhold. Per the state, step 3 for dependent claim amount is not used for ND state tax withholding.
> For the 2025 year and later, Section 2 Withholding Methods for Forms W-4 for 2020 and After has the same wage brackets as (Forms W-4 Before 2020). 

Withholding rates for taxpayers filing as *MAR* & *MARHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over    |
|-------------|------------------|----------------|--------------|-------------------|
| 0           | 57,500           | 0               | 0%          | 0                 |
| 57,500      | 168,525          | 0               | 1.95%       | 57,500            |
| 168,525     | And Over         | 2,164.99        | 2.50%       | 168,525           |

Withholding rates for taxpayers filing as *SINGLE* & *SINGHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over    |
|-------------|------------------|----------------|--------------|-------------------|
| 0           | 57,625           | 0               | 0%          | 0                 |
| 57,625      | 258,450          | 0               | 1.95%       | 57,625            |
| 258,450     | And Over         | 3,916.09        | 2.50%       | 258,450           |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 78,475       | 0          | 0%       | 0              |
| 78,475  | 289,675      | 0          | 1.95%    | 78,475         |
| 289,675 | And Over     | 4,118.40   | 2.50%    | 289,675        |

### Withholding changes for Oregon

- The Standard Deduction Amount is \$5,820 for MS3 and S3 Filing Status.
- The Standard Deduction Amount is \$2,910 for S2 Filing Status.
- The Personal Exemption amount is \$263 for all Filing Status.
- New Filing status for 2020 *NOWH* (No Withholding Provided) Flat tax rate of 8% (remains for 2026 year).
- HB2119 requires employers to withhold income tax at a rate of 8 percent of employee wages if they employee has not provided a withholding statement or exemption certificate. Continue withholding at the 8 percent rate until the employee submits a withholding statement and exemption certificate.

Special Tax Type rates for MS3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 8,750          | 0%           | 0                  |
| 49,999      | 249,999          | 8,750          | 0%           | 0                  |
| 249,999     | 259,999          | 7,000          | 0%           | 0                  |
| 259,999     | 269,999          | 5,250          | 0%           | 0                  |
| 269,999     | 279,999          | 3,500          | 0%           | 0                  |
| 279,999     | 289,999          | 1,750          | 0%           | 0                  |
| 289,999     | And over         | 0              | 0%           | 0                  |

Special Tax Type rates for S2 and S3 Filing Status:

| If Over     |     But Not Over | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 8,750          | 0%           | 0                  |
| 49,999      | 124,999          | 8,750          | 0%           | 0                  |
| 124,999     | 129,999          | 7,000          | 0%           | 0                  |
| 129,999     | 134,999          | 5,250          | 0%           | 0                  |
| 134,999     | 139,999          | 3,500          | 0%           | 0                  |
| 139,999     | 144,999          | 1,750          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

Tax Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 35,430           | 0              | 0%           | 0                  |
| 35,430      | 250,000          | 1,357          | 8.75%        | 22,800             |
| 250,000     | And over         | 21,237         | 9.9%         | 250,000            |

Tax Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 38,340           | 0              | 0%           | 0                  |
| 38,340      | 125,000          | 678            | 8.75%        | 11,400             |
| 125,000     | And Over         | 10,618         | 9.9%         | 125,000            |

Low Income Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,100            | 263            | 4.75%        | 0                  |
| 9,100       | 22,800           | 695            | 6.75%        | 9,100              |
| 22,800      | 50,000           | 1,620          | 8.75%        | 22,800             |

Low Income Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,550            | 263            | 4.75%        | 0                  |
| 4,550       | 11,400           | 479            | 6.75%        | 4,550              |
| 11,400      | 50,000           | 941            | 8.75%        | 11,400             |

### Withholding changes for Vermont

The Personal Exemption amount is $5,400

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount| Tax Rate | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 11,775           | 0              | 0%           | 0                  |
| 11,775      | 96,475           | 0              | 3.35%        | 11,775             |
| 96,475      | 216,525          | 2,837.45       | 6.60%        | 96,475             |
| 216,525     | 323,825          | 10,760.75      | 7.60%        | 216,525            |
| 323,825     | And Over         | 18,915.55      | 8.75%        | 323,825            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over  | But Not Over  | Tax Amount| Tax Rate | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,925            | 0              | 0%           | 0                  |
| 3,925       | 54,675           | 0              | 3.35%        | 3,925              |
| 54,675      | 126,775          | 1,700.13       | 6.60%        | 54,675             |
| 126,775     | 260,225          | 6,458.73       | 7.60%        | 126,775            |
| 260,225     | And Over         | 16,600.93      | 8.75%        | 260,225            |


## Changes in January Round 1 update (Released 12/18/2025)

- FICA Social Security Limit 184,500 (Previously $176,100)
- Federal tax
- California
- Colorado
- Hawaii
- Iowa
- Kentucky
- Maine
- Missouri
- Nebraska
- New Mexico
- New York
- Oklahoma
- Rhode Island
- South Carolina
- Yonkers

### Withholding changes for Federal

The maximum taxable earnings for Social Security increase in 2026 to \$184,500 from \$176,100. 

The Personal Exemption is $4,300 for SINGLE, MAR, HOH, NRA

Withholding rates for taxpayers filing as *NRA*:

> [!NOTE]
> For non-resident aliens, if the employee filled out a W-4 after 01/01/2020, the filing status *Non Resident Alien HR (NRAHR)* must always be used.

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 19,300          | 0             | 0%          | 0                 |
| 19,300     | 31,700          | 0             | 10%         | 19,300            |
| 31,700     | 69,700          | 1,240.00      | 12%         | 31,700            |
| 69,700     | 125,000         | 5,800.00      | 22%         | 69,700            |
| 125,000    | 221,075         | 17,966.00     | 24%         | 125,000           |
| 221,075    | 275,525         | 41,024.00     | 32%         | 221,075           |
| 275,525    | 659,900         | 58,448.00     | 35%         | 275,525           |
| 659,900    | And Over        | 192,979.25    | 37%         | 659,900           |

Withholding rates for taxpayers filing as *NRAHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|             | 24,150           | 0              | 0%           | 0                  |
| 24,150      | 30,350           | 0              | 10%          | 24,150             |
| 30,350      | 49,350           | 620.00         | 12%          | 30,350             |
| 49,350      | 77,000           | 2,900.00       | 22%          | 49,350             |
| 77,000      | 125,038          | 8,983.00       | 24%          | 77,000             |
| 125,038     | 152,263          | 20,512.00      | 32%          | 125,038            |
| 152,263     | 344,450          | 29,224.00      | 35%          | 152,263            |
| 344,450     | And Over         | 96,489.63      | 37%          | 344,450            |

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 19,300          | 0             | 0%          | 0                 |
| 19,300     | 44,100          | 0             | 10%         | 19,300            |
| 44,100     | 120,100         | 2,480.00      | 12%         | 44,100            |
| 120,100    | 230,700         | 11,600.00     | 22%         | 120,100           |
| 230,700    | 422,850         | 35,932.00     | 24%         | 230,700           |
| 422,850    | 531,750         | 82,048.00     | 32%         | 422,850           |
| 531,750    | 788,000         | 116,896.00    | 35%         | 531,750           |
| 788,000    | And Over        | 206,583.50    | 37%         | 788,000           |

Withholding rates for taxpayers filing as *MARHR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 16,100           | 0              | 0%           | 0                  |
| 16,100      | 28,500           | 0              | 10%          | 16,100             |
| 28,500      | 66,500           | 1,240.00       | 12%          | 28,500             |
| 66,500      | 121,800          | 5,800.00       | 22%          | 66,500             |
| 121,800     | 217,875          | 17,966.00      | 24%          | 121,800            |
| 217,875     | 272,325          | 41,024.00      | 32%          | 217,875            |
| 272,325     | 400,450          | 58,448.00      | 35%          | 272,325            |
| 400,450     | And Over         | 103,291.75     | 37%          | 400,450            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 7,500        | 0          | 0%       | 0              |
| 7,500   | 19,900       | 0          | 10%      | 7,500          |
| 19,900  | 57,900       | 1,240.00   | 12%      | 19,900         |
| 57,900  | 113,200      | 5,800.00   | 22%      | 57,900         |
| 113,200 | 209,275      | 17,966.00  | 24%      | 113,200        |
| 209,275 | 263,725      | 41,024.00  | 32%      | 209,275        |
| 263,725 | 648,100      | 58,448.00  | 35%      | 263,725        |
| 648,100 | And Over     | 192,979.25 | 37%      | 648,100        |

Withholding rates for taxpayers filing as *SGLHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over |
|-------------|------------------|----------------|----------|----------------|
| 0           | 8,050            | 0              | 0%       | 0              |
| 8,050       | 14,250           | 0              | 10%      | 8,050          |
| 14,250      | 33,250           | 620.00         | 12%      | 14,250         |
| 33,250      | 60,900           | 2,900.00       | 22%      | 33,250         |
| 60,900      | 108,938          | 8,983.00       | 24%      | 60,900         |
| 108,938     | 136,163          | 20,512.00      | 32%      | 108,938        |
| 136,163     | 328,350          | 29,224.00      | 35%      | 136,163        |
| 328,350     | And Over         | 96,489.63      | 37%      | 328,350        |

Withholding rates for taxpayers filing as *HOH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over    |
|-------------|------------------|----------------|----------|-------------------|
| 0           | 15,550           | 0              | 0%       | 0                 |
| 15,550      | 33,250           | 0              | 10%      | 15,550            |
| 33,250      | 83,000           | 1,770.00       | 12%      | 33,250            |
| 83,000      | 121,250          | 7,740.00       | 22%      | 83,000            |
| 121,250     | 217,300          | 16,155.00      | 24%      | 121,250           |
| 217,300     | 271,750          | 39,207.00      | 32%      | 217,300           |
| 271,750     | 656,150          | 56,631.00      | 35%      | 271,750           |
| 656,150     | And Over         | 191,171.00     | 37%      | 656,150           |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 12,075           | 0              | 0%       | 0                  |
| 12,075      | 20,925           | 0              | 10%      | 12,075             |
| 20,925      | 45,800           | 885.00         | 12%      | 20,925             |
| 45,800      | 64,925           | 3,870.00       | 22%      | 45,800             |
| 64,925      | 112,950          | 8,077.50       | 24%      | 64,925             |
| 112,950     | 140,175          | 19,603.50      | 32%      | 112,950            |
| 140,175     | 332,375          | 28,315.50      | 35%      | 140,175            |
| 332,375     | And Over         | 95,585.50      | 37%      | 332,375            |

### Withholding changes for California

For Filing Status of HOH and MAR2:  

- Personal Exemption is $168.30 from $163.90
- Standard Deduction is $11,412 from $11,080
- Low Income Limit is $37,791 from $36,736 

For Filing Status of MAR1 and SINGLE:

- Personal Exemption is $168.30 from $163.90
- Standard Deduction is $5,706 from $5,540
- Low Income Limit is $18,896 from $18,368

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over                  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 22,173           | 0              | 1.1%         | 0                  |
| 22,173      | 52,530           | 243.90         | 2.2%         | 22,173             |
| 52,530      | 67,716           | 911.75         | 4.4%         | 52,530             |
| 67,716      | 83,805           | 1,579.93       | 6.6%         | 67,716             |
| 83,805      | 98,990           | 2,641.80       | 8.8%         | 83,805             |
| 98,990      | 505,208          | 3,978.08       | 10.23%       | 98,990             |
| 505,208     | 606,251          | 45,534.18      | 11.33%       | 505,208            |
| 606,251     | 1,000,000        | 56,982.35      | 12.43%       | 606,251            |
| 1,000,000   | 1,010,417        | 105,925.35     | 13.53%       | 1,000,000          |
| 1,010,417   | And Over         | 107,334.77     | 14.63%       | 1,010,417          |

Withholding rates for taxpayers filing as *MAR1* and *MAR2*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 22,158           | 0              | 1.1%         | 0                  |
| 22,158      | 52,528           | 243.74         | 2.2%         | 22,158             |
| 50,998      | 82,904           | 911.88         | 4.4%         | 52,528             |
| 80,490      | 115,084          | 2,248.42       | 6.6%         | 82,904             |
| 111,732     | 145,448          | 4,372.30       | 8.8%         | 115,084            |
| 141,212     | 742,958          | 7,044.33       | 10.23%       | 145,448            |
| 721,318     | 891,542          | 68,169.60      | 11.33%       | 742,958            |
| 891,542     | 1,000,000        | 85,004.17      | 12.43%       | 891,542            |
| 1,000,000   | 1,485,906        | 98,485.50      | 13.53%       | 1,000,000          |
| 1,485,906   | And Over         | 164,228.58     | 14.63%       | 1,485,906          |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 11,079           | 0              | 1.1%         | 0                  |
| 11,079      | 26,264           | 121.87         | 2.2%         | 11,079             |
| 26,264      | 41,452           | 455.94         | 4.4%         | 26,264             |
| 41,452      | 57,542           | 1,124.21       | 6.6%         | 41,452             |
| 57,542      | 72,724           | 2,186.15       | 8.8%         | 57,542             |
| 72,724      | 371,479          | 3,522.17       | 10.23%       | 72,724             |
| 371,479     | 445,771          | 34,084.81      | 11.33%       | 371,479            |
| 445,771     | 742,953          | 42,502.09      | 12.43%       | 445,771            |
| 742,953     | 1,000,000        | 79,441.81      | 13.53%       | 742,953            |
| 1,000,000   | And Over         | 114,220.27     | 14.63%       | 1,000,000          |

### Withholding changes for Colorado

All filing status have the same fixed flat tax of 4.40% was 4.55% (2022).

- The Personal Exemption amount is $11,000 for MAR
- The Personal Exemption amount is $5,500 For SINGLE

**The following new filing status were added January 2022:**

- HOH1J - Head of Household 1 Job - Exemption amount  $22,000  
- MAR1J - Married Filing Jointly 1 Job - Exemption amount  $30,000  
- SIN1J - Single/Mar filing Single 1 Job - Exemption amount  $14,000  

In January 2022 the state of Colorado released a new form called [DR-0004](https://tax.colorado.gov/withholding-forms) this is optional for an employee to complete.  

There are 2 other parts to this form that have many different exemption amounts, we cannot accommodate all of them in the tax tables.

A new “OTHER” filing status was added (OTH1J) with Exemption increments of $500 that will accommodate all the "other" amounts on the form if an employee enters. 

OTH1J - OTH, +1 Jobs or Child Cr Allow - Exemption amount of $500

As an example, lets say I fill out the form and choose an amount of 2500. It does not match any of the above filing status so I would pick the OTHER status and put a 5 under Cards | Payroll | State Tax in the Number of Dependents field OR Additional Allowances. Which is 2500/500 = 5.

### Withholding changes for Hawaii

- The Standard Deduction Amount is $4,350 (New 2025)
- Personal Exemption is $1,144
  
Withholding rates for taxpayers filing as *MAR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 19,200           | 0              | 1.4%         | 0                  |
| 19,200      | 28,800           | 269.00         | 3.2%         | 19,200             |
| 28,800      | 38,400           | 576.00         | 5.5%         | 28,800             |
| 38,400      | 48,000           | 1,104.00       | 6.4%         | 38,400             |
| 48,000      | 72,000           | 1,718.00       | 6.8%         | 48,000             |
| 72,000      | 96,000           | 3,350.00       | 7.2%         | 72,000             |
| 96,000      | 250,000          | 5,078.00       | 7.6%         | 96,000             |
| 250,000     | And Over         | 16,782.00      | 7.9%         | 250,000            |

Withholding rates for taxpayers filing as *SHOH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,600            | 0              | 0%           | 0                  |
| 9,600       | 14,400           | 134.00         | 3.2%         | 9,600              |
| 14,400      | 19,200           | 288.00         | 5.5%         | 14,400             |
| 19,200      | 24,000           | 552.00         | 6.4%         | 19,200             |
| 24,000      | 36,000           | 859.00         | 6.8%         | 24,000             |
| 36,000      | 48,000           | 1,675.00       | 7.2%         | 36,000             |
| 48,000      | 125,000          | 2,539.00       | 7.6%         | 48,000             |
| 125,000     | And Over         | 8,391.00       | 7.9%         | 125,000            |


### Withholding changes for Iowa

Iowa withholding calculations, federal withholding is no longer subtracted from taxable wages.  

> [!NOTE]
> Iowa W4 changed in the year 2024 and the tax tables support the amounts, they are held in the Personal Exemption table below.

- Standard Deduction for EXP1 is $13,000 previously \$12,000
- Standard Deduction for EXP2 is $26,000 previously \$24,050

New filing status as of January 1, 2025
- Standard Deduction for HOH is $19,500 Head of Household
- Standard Deduction for MAR is $26,000 Married Joint No Earned Inc
- Standard Deduction for OTHER is $13,000 Other, Mar Joint with Earn Inc

All filing statuses have the same fixed flat tax of 3.80%

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
| 21       | 22          | 880         | 0%           | 0                  |
| 22       | And Over    | 920         | 0%           | 0                  |


### Withholding changes for Kentucky

- The Standard Deduction Amount is $3,360 from $3,270
- The Tax Rate reduced to 3.5%

### Withholding changes for Maine

- Personal Exemption is $5,300 was $5,150

Withholding rates for taxpayers filing as *SINGLE*, Tax table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 27,400           | 0              | 5.8%         | 0                  |
| 27,400      | 64,850           | 1,589          | 6.75%        | 27,400             |
| 64,850      | And over         | 4,117          | 7.15%        | 64,850             |

Special table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 102,250          | 0              | 0            | 12,450             |
| 102,250     | 177,250          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 54,850           |                | 5.80%        | 0                  |
| 54,850      | 129,750          | 3,181          | 6.75%        | 54,850             |
| 129,750     | And Over         | 8,237          | 7.15%        | 129,750            |

Special table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |               
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 204,550          | 0              | 0            | 27,750             |
| 204,550     | 354,550          | 150,000        | 0            | 0                  |

### Withholding changes for Missouri

- The Standard Deduction is $24,150 prior \$22,500 for filing status HOH
- The Standard Deduction is $32,200 prior \$30,000 for filing status MAR1
- The Standard Deduction is $16,100 prior \$15,000 for filing status MAR2 and SINGLE

Withholding rates for all filing status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,348            | 0              | 0%           | 0                  |
| 1,348       | 2,696            | 0              | 2.0%         | 1,348              |
| 2,696       | 4,044            | 27             | 2.5%         | 2,696              |
| 4,044       | 5,392            | 61             | 3.0%         | 4,044              |
| 5,392       | 6,740            | 101            | 3.5%         | 5,392              |
| 6,740       | 8,088            | 148            | 4.0%         | 6,740              |
| 8,088       | 9,436            | 202            | 4.5%         | 8,088              |
| 9,436       | And over         | 263            | 4.7%         | 9,436              |

### Withholding changes for Nebraska

The Personal Exemption amount is $2,440 formerly \$2,360 for Filing Status MAR and SINGLE.

Withholding rates for taxpayers filing as *MAR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,190            | 0              | 0            | 0                  |
| 8,190       | 13,010           | 0              | 2.26%        | 8,190              |
| 13,010      | 32,400           | 108.93         | 3.22%        | 13,010             |
| 32,400      | 50,400           | 733.29         | 4.21%        | 32,400             |
| 50,400      | 62,530           | 1,491.09       | 4.35%        | 50,400             |
| 62,530      | 82,920           | 2,018.75       | 4.48%        | 62,530             |
| 82,920      | And over         | 2,932.22       | 4.60%        | 82,920             |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,430            | 0              | 0            | 0                  |
| 3,430       | 6,710            | 0              | 2.26%        | 3,430              |
| 6,710       | 21,810           | 74.13          | 3.22%        | 6,710              |
| 21,810      | 31,610           | 560.35         | 4.21%        | 21,810             |
| 31,610      | 40,130           | 972.93         | 4.35%        | 31,610             |
| 40,130      | 75,370           | 1,343.55       | 4.48%        | 40,130             |
| 75,370      | And over         | 2,922.30       | 4.60%        | 75,370             |

### Withholding changes for New Mexico

Withholding rates for taxpayers filing as *MAR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 16,100           | 0              | 0%           | 0                  |
| 16,100      | 24,100           | 0              | 1.5%         | 16,100             |
| 24,100      | 32,100           | 120            | 3.2%         | 24,100             |
| 32,100      | 41,100           | 376            | 3.2%         | 32,100             |
| 41,100      | 57,100           | 664            | 4.3%         | 41,100             |
| 57,100      | 66,100           | 1,352          | 4.3%         | 57,100             |
| 66,100      | 102,100          | 1,739          | 4.7%         | 66,100             |
| 102,100     | 116,100          | 3,431          | 4.7%         | 102,100            |
| 116,100     | 331,100          | 4,089          | 4.9%         | 116,100            |
| 331,100     | And Over         | 14,624         | 5.9%         | 331,100            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,050            | 0              | 0%           | 0                  |
| 8,050       | 13,550           | 0              | 1.5%         | 8,050              |
| 13,550      | 20,550           | 82.50          | 3.2%         | 13,550             |
| 20,550      | 24,550           | 306.50         | 3.2%         | 20,550             |
| 24,550      | 33,550           | 434.50         | 4.3%         | 24,550             |
| 33,550      | 41,550           | 821.50         | 4.3%         | 33,550             |
| 41,550      | 58,550           | 1,165.50       | 4.7%         | 41,550             |
| 58,550      | 74,550           | 1,964.50       | 4.7%         | 58,550             |
| 74,550      | 218,050          | 2,716.50       | 4.9%         | 74,550             |
| 218,050     | And Over         | 9,748.00       | 5.9%         | 218,050            |

Withholding rates for taxpayers filing as *HOH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,075           | 0              | 0%           | 0                  |
| 12,075      | 20,075           | 0              | 1.5%         | 12,075             |
| 20,075      | 28,075           | 120            | 3.2%         | 20,075             |
| 28,075      | 37,075           | 376            | 3.2%         | 28,075             |
| 37,075      | 53,075           | 664            | 4.3%         | 37,075             |
| 53,075      | 62,075           | 1,352          | 4.3%         | 53,075             |
| 62,075      | 98,075           | 1,739          | 4.7%         | 62,075             |
| 98,075      | 112,075          | 3,431          | 4.7%         | 98,075             |
| 112,075     | 327,075          | 4,089          | 4.9%         | 112,075            |
| 327,075     | And Over         | 14,624         | 5.9%         | 327,075            |

#### Withholding changes for New York and New York-Yonkers

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,500            | 0              | .0390        | 0                  |
| 8,500       | 11,700           | 332.00         | .0440        | 8,500              |
| 11,700      | 13,900           | 472.00         | .0515        | 11,700             |
| 13,900      | 80,650           | 586.00         | .0540        | 13,900             |
| 80,650      | 96,800           | 4,190.00       | .0590        | 80,650             |
| 96,800      | 107,650          | 5,143.00       | .0657        | 96,800             |
| 107,650     | 157,650          | 5,855.00       | .0707        | 107,650            |
| 157,650     | 211,550          | 9,388.00       | .0801        | 157,650            |
| 211,550     | 323,200          | 13,708.00      | .0640        | 211,550            |
| 323,200     | 373,200          | 20,854.00      | .1349        | 323,200            |
| 373,200     | 1,077,550        | 27,600.00      | .0735        | 373,200            |
| 1,077,550   | 2,155,350        | 79,369.00      | .0765        | 1,077,550          |
| 2,155,350   | 5,000,000        | 0              | .1045        | 0                  |
| 5,000,000   | 25,000,000       | 0              | .1110        | 0                  |
| 25,000,000  | And over         | 0              | .1170        | 0                  |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,500            | 0              | .0390        | 0                  |
| 8,500       | 11,700           | 332.00         | .0440        | 8,500              |
| 11,700      | 13,900           | 472.00         | .0515        | 11,700             |
| 13,900      | 80,650           | 586.00         | .0540        | 13,900             |
| 80,650      | 96,800           | 4,190.00       | .0590        | 80,650             |
| 96,800      | 107,650          | 5,143.00       | .0703        | 96,800             |
| 107,650     | 157,650          | 5,906.00       | .0753        | 107,650            |
| 157,650     | 215,400          | 9,673.00       | .0640        | 157,650            |
| 215,400     | 265,400          | 13,369.00      | .1144        | 215,400            |
| 265,400     | 1,077,550        | 19,091.00      | .0735        | 265,400            |
| 1,077,550   | 5,000,000        | 0              | .1045        | 0                  |
| 5,000,000   | 25,000,000       | 0              | .1110        | 0                  |
| 25,000,000  | And over         | 0              | .1170        | 0                  |

### Withholding changes for Oklahoma

Withholding rates for taxpayers filing as *MARH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 20,200           | 0              | 0%           | 0                  |
| 20,200      | 22,500           | 0              | 2.50%        | 20,200             |
| 22,500      | 27,100           | 57.50          | 3.50%        | 22,500             |
| 27,100      | And Over         | 218.50         | 4.50%        | 27,100             |

Withholding rates for taxpayers filing as *SINGLE*, *MFS*, *MAR2*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,100           | 0              | 0%           | 0                  |
| 10,100      | 11,250           | 0              | 2.50%        | 10,100             |
| 11,250      | 13,550           | 28.75          | 3.50%        | 11,250             |
| 13,550      | And Over         | 109.25         | 4.50%        | 13,550             |

### Withholding changes for Rhode Island

For all Filing Status the Personal Exemption ($1,000) wage limit increased to $290,800

Withholding rates for taxpayers filing as *MAR* and *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 82,050           | 0              | 3.75%        | 0                  |
| 82,050      | 186,450          | 3,076.88       | 4.75%        | 82,050             |
| 186,450     | And Over         | 8,035.88       | 5.99%        | 182,450            |

### Withholding changes for South Carolina

- The Personal Exemption is $5,000 for Filing Status ONE.
- The Standard Deduction Maximum is $7,500 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,640            | 0              | 0.0%         | 0                  |
| 3,640       | 18,230           | -109.20        | 3.0%         | 0                  |
| 18,230      | And over         | -656.10        | 6.0%         | 0                  |


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

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *4/7/2026*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
