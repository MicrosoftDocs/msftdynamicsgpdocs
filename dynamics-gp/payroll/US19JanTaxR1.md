---
title: "US payroll tax update"
description: "US 2023 Payroll Tax update for Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 1/9/2025
---
# U.S. 2025 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2025 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

This is the second tax update for 2025 and replaces all previous tax updates. It includes State tax table changes that take effect January 1, 2025. 

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.

Check out these blogs for detailed documentation on how you calculate payroll taxes in Microsoft Dynamics GP:

[How to calculate Federal Tax with Dependent Claim Amount Field](https://community.dynamics.com/blogs/post/?postid=f65a8b3b-ef87-432c-a3c4-80ed7077a79d)

[Does Microsoft Dynamics GP calculate tax correctly?](https://community.dynamics.com/blogs/post/?postid=c9a75bcc-8f50-411f-a364-95a5121f6335)

[Tips to install the U.S. Payroll Tax Update](https://community.dynamics.com/blogs/post/?postid=dbc1295b-297f-4441-aa2f-7c2502bffc97)

## Changes in January Round 2 update (Target Release 1/21/2025)

- Arkansas
- Louisiana
- Minnesota
- Montana
- North Carolina
- North Dakota
- Oregon
- Rhode Island
- Vermont

### Withholding changes for Arkansas

> [!NOTE]
> If you have employees set up to withhold Arkansas state tax, you need to be on version 18.5.1635 or later, for taxes to be correct for the year 2024 or later. 
This change is for the Midrange Income look up part of the tax calculation.

- Standard Deduction Amount is $2,410
- Personal Exemption remains at $29.00

Tax Type rates for Filing Status NA:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,499            | 0              | 0.0%         | 0                  |
| 5,499       | 10,899           | -109.98        | 2.0%         | 0                  |
| 10,899      | 15,599           | -218.97        | 3.0%         | 0                  |
| 15,599      | 25,699           | -281.37        | 3.4%         | 0                  |
| 25,699      | 92,300           | -409.86        | 3.9%         | 0                  |
| 92,300      | 92,400           | -397.40        | 3.9%         | 0                  |
| 92,400      | 92,500           | -387.40        | 3.9%         | 0                  |
| 92,500      | 92,600           | -377.40        | 3.9%         | 0                  |
| 92,600      | 92,700           | -367.40        | 3.9%         | 0                  |
| 92,700      | 92,800           | -357.40        | 3.9%         | 0                  |
| 92,800      | 92,900           | -347.40        | 3.9%         | 0                  |
| 92,900      | 93,000           | -337.40        | 3.9%         | 0                  |
| 93,000      | 93,100           | -327.40        | 3.9%         | 0                  |
| 93,100      | 93,200           | -317.40        | 3.9%         | 0                  |
| 93,200      | 93,300           | -307.40        | 3.9%         | 0                  |
| 93,300      | 93,400           | -297.40        | 3.9%         | 0                  |
| 93,400      | 93,500           | -287.40        | 3.9%         | 0                  |
| 93,500      | 93,600           | -277.40        | 3.9%         | 0                  |
| 93,600      | 93,700           | -267.40        | 3.9%         | 0                  |
| 93,700      | 93,800           | -257.40        | 3.9%         | 0                  |
| 93,800      | 93,900           | -247.40        | 3.9%         | 0                  |
| 93,900      | 94,000           | -237.40        | 3.9%         | 0                  |
| 94,000      | 94,100           | -227.40        | 3.9%         | 0                  |
| 94,100      | 94,200           | -217.40        | 3.9%         | 0                  |
| 94,200      | 94,300           | -207.40        | 3.9%         | 0                  |
| 94,300      | 94,500           | -197.40        | 3.9%         | 0                  |
| 94,500      | 94,600           | -187.40        | 3.9%         | 0                  |
| 94,600      | 94,700           | -177.40        | 3.9%         | 0                  |
| 94,700      | 94,800           | -167.40        | 3.9%         | 0                  |
| 94,800      | 94,900           | -157.40        | 3.9%         | 0                  |
| 94,900      | 95,000           | -147.40        | 3.9%         | 0                  |
| 95,000      | 95,100           | -137.40        | 3.9%         | 0                  |
| 95,100      | 95,200           | -127.40        | 3.9%         | 0                  |
| 95,200      | 95,300           | -117.40        | 3.9%         | 0                  |
| 95,300      | 95,400           | -107.40        | 3.9%         | 0                  |
| 95,400      | 95,500           | -97.40         | 3.9%         | 0                  |
| 95,500      | And Over         | -87.40         | 3.9%         | 0                  |


### Withholding changes for Louisiana

- The flat tax rate for all filing status 3.09 from 1.85 
- Special Type rates & Dependent Exemption for all filing status removed.
- Standard Deduction for EXEMPT $0.00 
- Standard Deduction for SM1 $12,500
- Standard Deduction for M2 $25,000

### Withholding changes for Minnesota

The Personal Exemption amount is \$5,200 for all Filing Status.

Withholding rates for taxpayers filing as *MAR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 14,300           | 0              | 0%           | 0                  |
| 14,300      | 61,920           | 0              | 5.35         | 14,300             |
| 61,920      | 203,480          | 2,547.67       | 6.80%        | 61,920             |
| 203,480     | 344,710          | 12,173.75      | 7.85%        | 203,480            |
| 344,710     | And Over         | 23,260.31      | 9.85%        | 344,710            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 4,550        | 0          | 0%       | 0              |
| 4,550   | 37,120       | 0          | 5.35%    | 4,550          |
| 37,120  | 111,540      | 1,742.50   | 6.80%    | 37,120         |
| 111,540 | 203,180      | 6,803.06   | 7.85%    | 111,540        |
| 203,180 | And Over     | 13,996.80  | 9.85%    | 203,180        |

### Withholding changes for Montana

The Personal Exemption amount is $0 formerly $2,070 (2023). 

Tax Type rates for MAR Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 30,000           | 0              | 0%           | 0                  |
| 30,000      | 72,200           | 0              | 4.70%        | 30,000             |
| 72,200      | And Over         | 1,983          | 5.9%         | 72,200             |

Tax Type rates for SINGLE Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 15,000           | 0              | 0%           | 0                  |
| 15,000      | 36,100           | 0              | 4.70%        | 15,000             |
| 36,100      | And Over         | 992            | 5.9%         | 36,100             |

Tax Type rates for HOH Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 22,500           | 0              | 0%           | 0                  |
| 22,500      | 54,200           | 0              | 4.70%        | 22,500             |
| 54,200      | And Over         | 1,490          | 5.9%         | 54,200             |


### Withholding changes for North Carolina

- Standard Deduction for HOH remains at $19,125
- Standard Deduction for MAR and SINGLE remains at $12,750
- Tax rate for all filing status is 4.35%

### Withholding changes for North Dakota

The Personal Exemption amount is \$5,050 for Filing Status MAR and SINGLE. 

> [!NOTE]
> Per the state of North Dakota, there is no HOH filing status with exemptions. If an employee on the W4 chooses filing status of HOH and does not mark step 2, you still choose HOH as the filing status in Dynamics GP.
>
> The state relies on the federal form W-4 to calculate the amount to withhold. Per the state, step 3 for dependent claim amount is not used for ND state tax withholding.
> For the 2025 year, Section 2 Withholding Methods for Forms W-4 for 2020 and After has the same wage brackets as (Forms W-4 Before 2020). 

Withholding rates for taxpayers filing as *MAR* & *MARHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over    |
|-------------|------------------|----------------|--------------|-------------------|
| 0           | 55,488           | 0               | 0%          | 0                 |
| 55,488      | 164,038          | 0               | 1.95%       | 55,488            |
| 164,038     | And Over         | 2,116.73        | 2.50%       | 164,038           |

Withholding rates for taxpayers filing as *SINGLE* & *SINGHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over    |
|-------------|------------------|----------------|--------------|-------------------|
| 0           | 55,975           | 0               | 0%          | 0                 |
| 55,975      | 252,325          | 0               | 1.95%       | 55,975            |
| 252,325     | And Over         | 3,828.83        | 2.50%       | 252,325           |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 76,200       | 0          | 0%       | 0              |
| 76,200  | 282,700      | 0          | 1.95%    | 76,200         |
| 282,700 | And Over     | 4,026.75   | 2.50%    | 282,700        |


### Withholding changes for Oregon

- The Standard Deduction Amount is \$5,670 for MS3 and S3 Filing Status.
- The Standard Deduction Amount is \$2,835 for S2 Filing Status.
- The Personal Exemption amount is \$256 for all Filing Status.
- New Filing status for 2020 *NOWH* (No Withholding Provided) Flat tax rate of 8% (remains for 2025 year)
- HB2119 requires employers to withhold income tax at a rate of 8 percent of employee wages if they employee has not provided a withholding statement or exemption certificate. Continue withholding at the 8 percent rate until the employee submits a withholding statement and exemption certificate.

Special Tax Type rates for MS3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 8,500          | 0%           | 0                  |
| 49,999      | 249,999          | 8,500          | 0%           | 0                  |
| 249,999     | 259,999          | 6,800          | 0%           | 0                  |
| 259,999     | 269,999          | 5,100          | 0%           | 0                  |
| 269,999     | 279,999          | 3,400          | 0%           | 0                  |
| 279,999     | 289,999          | 1,700          | 0%           | 0                  |
| 289,999     | And over         | 0              | 0%           | 0                  |
|             |                  |                |              |                    |

Special Tax Type rates for S2 and S3 Filing Status:

| If Over     |     But Not Over | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 8,500          | 0%           | 0                  |
| 49,999      | 124,999          | 8,500          | 0%           | 0                  |
| 124,999     | 129,999          | 6,800          | 0%           | 0                  |
| 129,999     | 134,999          | 5,100          | 0%           | 0                  |
| 134,999     | 139,999          | 3,400          | 0%           | 0                  |
| 139,999     | 144,999          | 1,700          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

Tax Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 35,830           | 0              | 0%           | 0                  |
| 35,830      | 250,000          | 1,323          | 8.75%        | 22,200             |
| 250,000     | And over         | 21,256         | 9.9%         | 250,000            |

Tax Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 38,665           | 0              | 0%           | 0                  |
| 38,665      | 125,000          | 661            | 8.75%        | 38,665             |
| 125,000     | And Over         | 10,627         | 9.9%         | 125,000            |

Low Income Type rates for MS3 and S3 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8,800            | 256            | 4.75%        | 0                  |
| 8,800       | 22,200           | 674            | 6.75%        | 8,800              |
| 22,200      | 50,000           | 1,579          | 8.75%        | 22,200             |

Low Income Type rates for S2 Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 4,400            | 256            | 4.75%        | 0                  |
| 4,400       | 11,100           | 465            | 6.75%        | 4,400              |
| 11,100      | 50,000           | 917            | 8.75%        | 11,100             |


### Withholding changes for Rhode Island

For all Filing Status the Personal Exemption ($1,000) wage limit increased to $283,250

Withholding rates for taxpayers filing as *MAR* and *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 79,900           | 0              | 3.75%        | 0                  |
| 79,900      | 181,650          | 2,996.25       | 4.75%        | 79,900             |
| 181,650     | And Over         | 7,829.38       | 5.99%        | 181,650            |


### Withholding changes for Vermont

The Personal Exemption amount is $5,300

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 11,475           | 0              | 0%           | 0                  |
| 11,475      | 93,975           | 0              | 3.35%        | 11,475             |
| 93,975      | 210,925          | 2,763.75       | 6.60%        | 93,975             |
| 210,925     | 315,475          | 10,482.45      | 7.60%        | 210,925            |
| 315,475     | And Over         | 18,428.25      | 8.75%        | 315,475            |

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,825            | 0              | 0%           | 0                  |
| 3,825       | 53,225           | 0              | 3.35%        | 3,825              |
| 53,225      | 123,525          | 1,654.90       | 6.60%        | 53,225             |
| 123,525     | 253,525          | 6,294.70       | 7.60%        | 123,525            |
| 253,525     | And Over         | 16,174.70      | 8.75%        | 253,525            |


## Changes in January Round 1 update (Released 12/20/2024)

- FICA Social Security Limit 176,100 (Previously $168,600)
- Federal tax
- California
- Colorado
- Hawaii
- Iowa
- Kentucky
- Maine
- Michigan
- Missouri
- Nebraska
- New Mexico
- Oklahoma
- South Carolina
- West Virginia

### Withholding changes for Federal

The maximum taxable earnings for Social Security increase in 2025 to \$176,100 from \$168,600. 

**Federal tax tables released 12/16/2024**

The Personal Exemption is $4,300 for SINGLE, MAR, HOH, NRA

Withholding rates for taxpayers filing as *NRA*:

> [!NOTE]
> For non-resident aliens, if the employee filled out a W-4 after 01/01/2020, the filing status *Non Resident Alien HR (NRAHR)* must always be used.

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 17,100          | 0             | 0%          | 0                 |
| 17,100     | 29,025          | 0             | 10%         | 17,100            |
| 29,025     | 65,575          | 1,192.50      | 12%         | 29,025            |
| 65,575     | 120,450         | 5,578.50      | 22%         | 65,575            |
| 120,450    | 214,400         | 17,651.00     | 24%         | 120,450           |
| 214,400    | 267,625         | 40,199.00     | 32%         | 214,400           |
| 267,625    | 643,450         | 57,231.00     | 35%         | 267,625           |
| 643,450    | And Over        | 188,769.75    | 37%         | 643,450           |

Withholding rates for taxpayers filing as *NRAHR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
|             | 22,500           | 0              | 0%           | 0                  |
| 22,500      | 28,463           | 0              | 10%          | 22,500             |
| 28,463      | 46,738           | 596.25         | 12%          | 28,463             |
| 46,738      | 74,175           | 2,789.25       | 22%          | 46,738             |
| 74,175      | 121,150          | 8,825.50       | 24%          | 74,175             |
| 121,150     | 147,763          | 20,099.50      | 32%          | 121,150            |
| 147,763     | 335,675          | 28,615.50      | 35%          | 147,763            |
| 335,675     | And Over         | 94,384.88      | 37%          | 335,675            |

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|
|------------|-----------------|---------------|-------------|-------------------|
| 0          | 17,100          | 0             | 0%          | 0                 |
| 17,100     | 40,950          | 0             | 10%         | 17,100            |
| 40,950     | 114,050         | 2,385.00      | 12%         | 40,950            |
| 114,050    | 223,800         | 11,157.00     | 22%         | 114,050           |
| 223,800    | 411,700         | 35,302.00     | 24%         | 223,800           |
| 411,700    | 518,150         | 80,398.00     | 32%         | 411,700           |
| 518,150    | 768,700         | 114,462.00    | 35%         | 518,150           |
| 768,700    | And Over        | 202,154.50    | 37%         | 768,700           |

Withholding rates for taxpayers filing as *MARHR*:

| If Over  | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 15,000           | 0              | 0%           | 0                  |
| 15,000      | 26,925           | 0              | 10%          | 15,000             |
| 26,925      | 63,475           | 1,192.50       | 12%          | 26,925             |
| 63,475      | 118,350          | 5,578.50       | 22%          | 63,475             |
| 118,350     | 212,300          | 17,651.00      | 24%          | 118,350            |
| 212,300     | 265,525          | 40,199.00      | 32%          | 212,300            |
| 265,525     | 390,800          | 57,231.00      | 35%          | 265,525            |
| 390,800     | And Over         | 101,077.25     | 37%          | 390,800            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|---------|--------------|------------|----------|----------------|
| 0       | 6,400        | 0          | 0%       | 0              |
| 6,400   | 18,325       | 0          | 10%      | 6,400          |
| 18,325  | 54,875       | 1,192.50   | 12%      | 18,325         |
| 54,875  | 109,750      | 5,578.50   | 22%      | 54,875         |
| 109,750 | 203,700      | 17,651.00  | 24%      | 109,750        |
| 203,700 | 256,925      | 40,199.00  | 32%      | 203,700        |
| 256,925 | 632,750      | 57,231.00  | 35%      | 256,925        |
| 632,750 | And Over     | 188,769.75 | 37%      | 632,750        |

Withholding rates for taxpayers filing as *SGLHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over |
|-------------|------------------|----------------|----------|----------------|
| 0           | 7,500            | 0              | 0%       | 0              |
| 7,500       | 13,463           | 0              | 10%      | 7,500          |
| 13,463      | 31,738           | 596.25         | 12%      | 13,463         |
| 31,738      | 59,175           | 2,789.25       | 22%      | 31,738         |
| 59,175      | 106,150          | 8,825.50       | 24%      | 59,175         |
| 106,150     | 132,763          | 20,099.50      | 32%      | 106,150        |
| 132,763     | 320,675          | 28,615.50      | 35%      | 132,763        |
| 320,675     | And Over         | 94,384.88      | 37%      | 320,675        |

Withholding rates for taxpayers filing as *HOH*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over    |
|-------------|------------------|----------------|----------|-------------------|
| 0           | 13,900           | 0              | 0%       | 0                 |
| 13,900      | 30,900           | 0              | 10%      | 13,900            |
| 30,900      | 78,750           | 1,700.00       | 12%      | 30,900            |
| 78,750      | 117,250          | 7,442.00       | 22%      | 78,750            |
| 117,250     | 211,200          | 15,912.00      | 24%      | 117,250           |
| 211,200     | 264,400          | 38,460.00      | 32%      | 211,200           |
| 264,400     | 640,250          | 55,484.00      | 35%      | 264,400           |
| 640,250     | And Over         | 187,031.50     | 37%      | 640,250           |

Withholding rates for taxpayers filing as *HOHHR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 11,250           | 0              | 0%       | 0                  |
| 11,250      | 19,750           | 0              | 10%      | 11,250             |
| 19,750      | 43,675           | 850.00         | 12%      | 19,750             |
| 43,675      | 62,925           | 3,721.00       | 22%      | 43,675             |
| 62,925      | 109,900          | 7,956.00       | 24%      | 62,925             |
| 109,900     | 136,500          | 19,230.00      | 32%      | 109,900            |
| 136,500     | 324,425          | 27,742.00      | 35%      | 136,500            |
| 324,425     | And Over         | 93,515.75      | 37%      | 324,425            |

### Withholding changes for California

For Filing Status of HOH and MAR2:  

- Personal Exemption is $163.90 from $158.40
- Standard Deduction is $11,080 from $10,726
- Low Income Limit is $36,736 from $35,538 

For Filing Status of MAR1 and SINGLE:

- Personal Exemption is $163.90 from $158.40
- Standard Deduction is $5,540 from $5,363
- Low Income Limit is $18,368 from $17,769

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over                  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 21,527           | 0              | 1.1%         | 0                  |
| 21,527      | 51,000           | 236.80         | 2.2%         | 21,527             |
| 51,000      | 65,744           | 885.21         | 4.4%         | 51,000             |
| 65,744      | 81,364           | 1,533.95       | 6.6%         | 65,744             |
| 81,364      | 96,107           | 2,564.87       | 8.8%         | 81,364             |
| 96,107      | 490,493          | 3,862.25       | 10.23%       | 96,107             |
| 490,493     | 588,593          | 44,207.94      | 11.33%       | 490,493            |
| 588,593     | 980,987          | 55,322.67      | 12.43%       | 588,593            |
| 980,987     | 1,000,000        | 104,097.24     | 13.53%       | 980,987            |
| 1,000,000   | And Over         | 106,669.70     | 14.63%       | 1,000,000          |

Withholding rates for taxpayers filing as *MAR1* and *MAR2*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over  |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 21,512           | 0              | 1.1%         | 0                  |
| 21,512      | 50,998           | 236.63         | 2.2%         | 21,512             |
| 50,998      | 80,490           | 885.32         | 4.4%         | 50,998             |
| 80,490      | 111,732          | 2,182.97       | 6.6%         | 80,490             |
| 111,732     | 141,212          | 4,244.94       | 8.8%         | 111,732            |
| 141,212     | 721,318          | 6,839.18       | 10.23%       | 141,212            |
| 721,318     | 865,574          | 66,184.02      | 11.33%       | 721,318            |
| 865,574     | 1,000,000        | 82,528.22      | 12.43%       | 865,574            |
| 1,000,000   | 1,442,628        | 99,237.37      | 13.53%       | 1,000,000          |
| 1,442,628   | And Over         | 159,124.94     | 14.63%       | 1,442,628          |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over  | But Not Over  | Tax Amount  | Tax Rate  | On Excess Over                 |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 10,756           | 0              | 1.1%         | 0                  |
| 10,756      | 25,499           | 118.32         | 2.2%         | 10,756             |
| 25,499      | 40,245           | 442.67         | 4.4%         | 25,499             |
| 40,245      | 55,866           | 1,091.49       | 6.6%         | 40,245             |
| 55,866      | 70,606           | 2,122.48       | 8.8%         | 55,866             |
| 70,606      | 360,659          | 3,419.60       | 10.23%       | 70,606             |
| 360,659     | 432,787          | 33,092.02      | 11.33%       | 360,659            |
| 432,787     | 721,314          | 41,264.12      | 12.43%       | 432,787            |
| 721,314     | 1,000,000        | 77,128.03      | 13.53%       | 721,314            |
| 1,000,000   | And Over         | 114,834.25     | 14.63%       | 1,000,000          |

### Withholding changes for Colorado

All filing status have the same fixed flat tax of 4.40% was 4.55% (2022).

- The Personal Exemption amount is $10,000 for MAR
- The Personal Exemption amount is $5,000 For SINGLE

**The following new filing status were added January 2022:**

- HOH1J - Head of Household 1 Job - Exemption amount  $20,000  
- MAR1J - Married Filing Jointly 1 Job - Exemption amount  $27,500  
- SIN1J - Single/Mar filing Single 1 Job - Exemption amount  $12,500  

In January 2022 the state of Colorado released a new form called [DR-0004](https://tax.colorado.gov/withholding-forms) this is optional for an employee to complete.  

There are 2 other parts to this form that have many different exemption amounts, we cannot accommodate all of them in the tax tables.

A new “OTHER” filing status was added (OTH1J) with Exemption increments of $500 that will accommodate all the "other" amounts on the form if an employee enters. 

OTH1J - OTH, +1 Jobs or Child Cr Allow - Exemption amount of $500

As an example, lets say I fill out the form and choose an amount of 2500. It does not match any of the above filing status so I would pick the OTHER status and put a 5 under Cards | Payroll | State Tax in the Number of Dependents field OR Additional Allowances. Which is 2500/500 = 5.

Another example, I put 5500 on the form. Again, it does not match the other filing status, so I choose *Other* and put *11*.

### Withholding changes for Hawaii

- The Standard Deduction Amount is $1,650 (New 2025)
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

- Standard Deduction for EXP1 is $12,000 previously \$14,600
- Standard Deduction for EXP2 is $24,050 previously \$29,200

New filing status as of January 1, 2025
- Standard Deduction for HOH is $18,050 Head of Household
- Standard Deduction for MAR is $24,050 Married Joint No Earned Inc
- Standard Deduction for OTHER is $12,000 Other, Mar Joint with Earn Inc

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

- The Standard Deduction Amount is $3,270 from $3,160
- The Tax Rate remains at 4.0%

### Withholding changes for Maine

- Personal Exemption is $5,150 was $5,000

Withholding rates for taxpayers filing as *SINGLE*, Tax table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 26,800           | 0              | 5.8%         | 0                  |
| 26,800      | 63,450           | 1,554          | 6.75%        | 26,800             |
| 63,450      | And over         | 4,028          | 7.15%        | 63,450             |

Special table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 100,000          | 0              | 0            | 12,150             |
| 100,000     | 175,000          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 53,600           |                | 5.80%        | 0                  |
| 53,600      | 126,900          | 3,109          | 6.75%        | 53,600             |
| 126,900     | And Over         | 8,057          | 7.15%        | 126,900            |

Special table type:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over|               
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 200,050          | 0              | 0            | 27,150             |
| 200,050     | 350,050          | 150,000        | 0            | 0                  |

### Withholding changes for Michigan

- The Personal Exemption Amount is $5,800 from $5,600
- The Tax Rate remains at 4.25%

### Withholding changes for Missouri

- The Standard Deduction is $22,500 prior \$21,900 for filing status HOH
- The Standard Deduction is $30,000 prior \$29,200 for filing status MAR1
- The Standard Deduction is $15,000 prior \$14,600 for filing status MAR2 and SINGLE

Withholding rates for all filing status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,313            | 0              | 0%           | 0                  |
| 1,313       | 2,626            | 0              | 2.0%         | 1,313              |
| 2,626       | 3,939            | 26             | 2.5%         | 2,626              |
| 3,939       | 5,252            | 59             | 3.0%         | 3,939              |
| 5,252       | 6,565            | 98             | 3.5%         | 5,252              |
| 6,565       | 7,878            | 144            | 4.0%         | 6,565              |
| 7,878       | 9,191            | 197            | 4.5%         | 7,878              |
| 9,191       | And over         | 256            | 4.7%         | 9,191              |


### Withholding changes for Nebraska

The Personal Exemption amount is $2,360 formerly \$2,250 for Filing Status MAR and SINGLE.

Withholding rates for taxpayers filing as *MAR*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,910            | 0              | 0            | 0                  |
| 7,910       | 12,560           | 0              | 2.26%        | 7,910              |
| 12,560      | 31,270           | 105.09         | 3.22%        | 12,560             |
| 31,270      | 48,650           | 707.55         | 4.91%        | 31,270             |
| 48,650      | 60,360           | 1,560.91       | 5.07%        | 48,650             |
| 60,360      | 80,040           | 2,154.61       | 5.23%        | 60,360             |
| 80,040      | And over         | 3,183.87       | 5.37%        | 80,040             |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,310            | 0              | 0            | 0                  |
| 3,310       | 6,480            | 0              | 2.26%        | 3,310              |
| 6,480       | 21,050           | 71.64          | 3.22%        | 6,480              |
| 21,050      | 30,510           | 540.79         | 4.91%        | 21,050             |
| 30,510      | 38,740           | 1,005.28       | 5.07%        | 30,510             |
| 38,740      | 72,750           | 1,422.54       | 5.23%        | 38,740             |
| 72,750      | And over         | 3,201.26       | 5.37%        | 72,750             |

### Withholding changes for New Mexico

Withholding rates for taxpayers filing as *MAR*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 15,000           | 0              | 0%           | 0                  |
| 15,000      | 23,000           | 0              | 1.5%         | 15,000             |
| 23,000      | 31,000           | 120            | 3.2%         | 23,000             |
| 31,000      | 40,000           | 376            | 3.2%         | 31,000             |
| 40,000      | 56,000           | 664            | 4.3%         | 40,000             |
| 56,000      | 65,000           | 1,352          | 4.3%         | 56,000             |
| 65,000      | 101,000          | 1,739          | 4.7%         | 65,000             |
| 101,000     | 115,000          | 3,431          | 4.7%         | 101,000            |
| 115,000     | 330,000          | 4,089          | 4.9%         | 115,000            |
| 330,000     | And Over         | 14,624         | 5.9%         | 330,000            |

Withholding rates for taxpayers filing as *SINGLE*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,500            | 0              | 0%           | 0                  |
| 7,500       | 13,000           | 0              | 1.5%         | 7,500              |
| 13,000      | 20,000           | 82.50          | 3.2%         | 13,000             |
| 20,000      | 24,000           | 306.50         | 3.2%         | 20,000             |
| 24,000      | 33,000           | 434.50         | 4.3%         | 24,000             |
| 33,000      | 41,000           | 821.50         | 4.3%         | 33,000             |
| 41,000      | 58,000           | 1,165.50       | 4.7%         | 41,000             |
| 58,000      | 74,000           | 1,964.50       | 4.7%         | 58,000             |
| 74,000      | 217,500          | 2,716.50       | 4.9%         | 74,000             |
| 217,500     | And Over         | 9,748.00       | 5.9%         | 217,500            |

Withholding rates for taxpayers filing as *HOH*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 11,250           | 0              | 0%           | 0                  |
| 11,250      | 19,250           | 0              | 1.5%         | 11,250             |
| 19,250      | 27,250           | 120            | 3.2%         | 19,250             |
| 27,250      | 36,250           | 376            | 3.2%         | 27,250             |
| 36,250      | 52,250           | 664            | 4.3%         | 36,250             |
| 52,250      | 61,250           | 1,352          | 4.3%         | 52,250             |
| 61,250      | 97,250           | 1,739          | 4.7%         | 61,250             |
| 97,250      | 111,250          | 3,431          | 4.7%         | 97,250             |
| 111,250     | 326,250          | 4,089          | 4.9%         | 111,250            |
| 326,250     | And Over         | 14,624         | 5.9%         | 326,250            |

### Withholding changes for Oklahoma

Withholding rates for taxpayers filing as *MARH*:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,700           | 0              | 0%           | 0                  |
| 12,700      | 14,700           | 0              | .25%         | 12,700             |
| 14,700      | 17,700           | 5.00           | .75%         | 14,700             |
| 17,700      | 20,200           | 27.50          | 1.75%        | 17,700             |
| 20,200      | 22,500           | 71.25          | 2.75%        | 20,200             |
| 22,500      | 27,100           | 134.50         | 3.75%        | 22,500             |
| 27,100      | And Over         | 307.00         | 4.75%        | 27,100             |

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

### Withholding changes for South Carolina

- The Personal Exemption is $4,860 for Filing Status ONE.
- The Standard Deduction Maximum is $7,300 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over | But Not Over | Tax Amount | Tax Rate | On Excess Over |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,560            | 0              | 0.0%         | 0                  |
| 3,560       | 17,830           | -106.80        | 3.0%         | 0                  |
| 17,830      | And over         | -677.36        | 6.2%         | 0                  |

### Withholding changes for West Virginia

The Personal Exemption amount is $2,000 For all filing status.

Withholding rates for taxpayers filing as PM (Percentage Method) are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 10,000           | 0              | 2.22%    | 0                  |
| 10,000      | 25,000           | 222.00         | 2.96%    | 10,000             |
| 25,000      | 40,000           | 666.00         | 3.33%    | 25,000             |
| 40,000      | 60,000           | 1,165.50       | 4.44%    | 40,000             |
| 60,000      | and over         | 2,053.50       | 4.82%    | 60,000             |

Withholding rates for taxpayers filing as TE (Two Earner Option) are as follows:

| If Over     | But Not Over     | Tax Amount     | Tax Rate | On Excess Over     |
|-------------|------------------|----------------|----------|--------------------|
| 0           | 7,500            | 0              | 2.22%    | 0                  |
| 7,500       | 18,750           | 166.50         | 2.96%    | 7,500              |
| 18,750      | 30,000           | 499.50         | 3.33%    | 18,700             |
| 30,000      | 45,000           | 874.13         | 4.44%    | 30,000             |
| 45,000      | and over         | 1,540.13       | 4.82%    | 45,000             |

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

5. Verify that the latest Payroll tax table update has been installed. Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Payroll Tax. The Last Tax Update value should be *1/22/2025*.

## What's next

If you upgrade to another version of Microsoft Dynamics GP, you must install the most recent service pack (if any), as well as the most recent tax table updates for that release, to ensure you have the latest tax information. Newer releases of Microsoft Dynamics GP do not include current payroll tax information.
