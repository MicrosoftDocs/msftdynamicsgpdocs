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
ms.date: 12/13/2021
---
# U.S. 2022 Payroll Tax Update

This tax update applies to:

- Microsoft Dynamics GP on Microsoft SQL Server

This article provides guidance for how to install the 2022 U.S. Payroll Tax Update for Microsoft Dynamics GP and describes changes.

The first tax update for 2022 replaces all previous tax updates. It includes state and federal tax table changes that take effect January 1, 2022. We recommend that you install this update as soon as you can for the year 2022.

This document assumes that you are familiar with the Microsoft Dynamics GP U.S. Payroll module.


## Changes in January Round 1 update (Target Release 12/21/2021)

- Federal changes and FICA Social Security Limit $147,000
- California
- Georgia
- Iowa
- Kentucky
- Maine
- Maryland
- Michigan
- Missouri
- Nebraska
- New Mexico
- New York
- Oklahoma
- Oregon
- South Carolina
- Yonkers



### 2022 Federal tax changes

The maximum taxable earnings for Social Security increase in 2022 to \$147,000 from \$142,800 

The Personal Exemption is $4,300 for SINGLE, MAR, HOH

Withholding rates for taxpayers filing as *NRA*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,600           | 0              | 0%           | 0                  |
| 12,600      | 22,550           | 0              | 10%          | 12,600             |
| 22,550      | 53,125           | 995.00         | 12%          | 22,550             |
| 53,125      | 98,975           | 4,664.00       | 22%          | 53,125             |
| 98,975      | 177,525          | 14,751.00      | 24%          | 98,975             |
| 177,525     | 221,025          | 33,603.00      | 32%          | 177,525            |
| 221,025     | 536,200          | 47,843.00      | 35%          | 221,025            |
| 536,200     | And Over         | 157,804.25     | 37%          | 536,200            |


Withholding rates for taxpayers filing as *NRAHR*
**If the employee filled out a W4 after 1/1/2020 their filing status should always be NRAHR for correct withholding.**


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|             | 19,225           | 0              | 0%           | 0                  |
| 19,225      | 24,200           | 0              | 10%          | 19,225             |
| 24,200      | 39,488           | 497.50         | 12%          | 24,200             |
| 39,488      | 62,413           | 2,332.06       | 22%          | 39,488             |
| 62,413      | 101,688          | 7,375.56       | 24%          | 62,413             |
| 101,688     | 123,938          | 16,801.56      | 32%          | 101,688            |
| 123,938     | 281,025          | 23,921.56      | 35%          | 123,938            |
| 281,025     | And Over         | 78,902.01      | 37%          | 281,025            |

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

- Personal Exemption is $141.90 from $136.40
- Standard Deduction is $9,606  from $9,202
- Low Income Limit is $31,831 from $30,534

For Filing Status of MAR1 and SINGLE:

- Personal Exemption is $141.90 from $136.40
- Standard Deduction is $4,803 from $4,601
- Low Income Limit is $15,916 from $15,267


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
- HOH and SINGLE     is \$5,400
- MFJ1I              is \$7,100
- MFJ2I and MFS      is \$3,550


#### Withholding changes for Iowa

The Standard Deduction Amount for Filing Status:
- EXP1 is \$2,210
- Filing Status EXP2 is \$5,450

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
| 78,435      | And over         | 4,599.44       | 8.53%        | 78,435             |


#### Withholding changes for Kentucky

The Standard Deduction Amount is $2,770 from $2,690
The Tax Rate remains at 5%


#### Withholding changes for Maine

- Personal Exemption is $4,450
- 
Withholding rates for taxpayers filing as *SINGLE*, Tax table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 23,000           | 0              | 5.8%         | 0                  |
| 22,000      | 54,450           | 1,334          | 6.75%        | 23,000             |
| 54,450      | And over         | 3,457          | 7.15%        | 54,450             |

Special table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 85,850           | 0              | 0            | 10,100             |
| 85,850      | 160,850          | 75,000         | 0            | 0                  |

Withholding rates for taxpayers filing as MAR, Tax table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 46,000           |                | 5.80%        | 0                  |
| 46,000      | 108,900          | 2,668          | 6.75%        | 46,000             |
| 108,900     | And Over         | 6,914          | 7.15%        | 108,900            |

Special table type

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 171,700          | 0              | 0            | 23,050             |
| 171,700     | 321,700          | 150,000        | 0            | 0                  |


#### Withholding changes for Maryland

For Filing Status of 
SMMAR (St. Mary MFJ/HOH) 

Withholding rates for taxpayer

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 150,000          | 0              | 7.85%        | 0                  |
| 150,000     | 175,000          | 11,775         | 8.10%        | 150,000            |
| 175,000     | 225,000          | 13,800         | 8.35%        | 175,000            |
| 225,000     | 300,000          | 17,975         | 8.6%         | 225,000            |
| 300,000     | And over         | 24,425         | 8.85%        | 300,000            |


For Filing Status of 
STMARY (St. Mary SGL/DEP/MFS)

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.85%        | 0                  |
| 100,000     | 125,000          | 7,850          | 8.10%        | 100,000            |
| 125,000     | 150,000          | 9,875          | 8.35%        | 125,000            |
| 150,000     | 250,000          | 11,962.50      | 8.6%         | 150,000            |
| 250,000     | And over         | 20,562.50      | 8.85%        | 250,000            |

For Filing Status of 
WASHTN (Washington SGL/DEP/MFS)

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.75%        | 0                  |
| 100,000     | 125,000          | 7,750          | 8.00%        | 100,000            |
| 125,000     | 150,000          | 9,750          | 8.25%        | 125,000            |
| 150,000     | 250,000          | 11,812.50      | 8.5%         | 150,000            |
| 250,000     | And over         | 20,312.50      | 8.75%        | 250,000            |

For Filing Status of 
WHMAR  (Washington MFJ/HOH)

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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

#### Withholding changes for Missouri

The Standard Deduction is \$19,400 for filing status HOH
The Standard Deduction is \$25,900 for filing status MAR1
The Standard Deduction is \$12,950 for filing status MAR2 and SINGLE

Withholding rates for all filing status

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,121            | 0              | 1.5%         | 0                  |
| 1,073       | 2,242            | 17.00          | 2.0%         | 1,121              |
| 2,242       | 3,363            | 37900          | 2.5%         | 2,242              |
| 3,363       | 4,484            | 67.00          | 3.0%         | 3,363              |
| 4,484       | 5,605            | 101.00         | 3.5%         | 4,484              |
| 5,605       | 6,726            | 140.00         | 4.0%         | 5,605              |
| 6,726       | 7,847            | 185.00         | 4.50%        | 6,726              |
| 7,847       | 8,968            | 235.00         | 5.0%         | 7,847              |
| 8,968       | And over         | 291.00         | 5.3%         | 8,968              |



#### Withholding changes for Nebraska

The Personal Exemption amount is \$2,080 for Filing Status MAR and SINGLE 

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,100            | 0              | 0            | 0                  |
| 7,100       | 11,270           | 0              | 2.26%        | 7,100              |
| 11,270      | 28,070           | 94.24          | 3.22%        | 11,270             |
| 28,070      | 43,670           | 635.20         | 4.91%        | 28,070             |
| 43,670      | 54,180           | 1,401.16       | 6.20%        | 43,670             |
| 54,180      | 71,850           | 2,052.78       | 6.59%        | 54,180             |
| 71,850      | And over         | 3,217.23       | 6.95%        | 71,850            |

Withholding rates for taxpayers filing as *SINGLE* 

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,975            | 0              | 0            | 0                  |
| 2,975       | 5,820            | 0              | 2.26%        | 2,975              |
| 5,820       | 18,900           | 64.30          | 3.22%        | 5,820              |
| 18,900      | 27,390           | 485.48         | 4.91%        | 18,900             |
| 27,390      | 34,780           | 902.34         | 6.20%        | 27,390             |
| 34,780      | 65,310           | 1,360.52       | 6.59%        | 34,780             |
| 65,310      | And over         | 3,372.45       | 6.95%        | 65,310         |



#### Withholding changes for New Mexico

Withholding rates for taxpayers filing as *MAR*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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


Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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


Withholding rates for taxpayers filing as *HOH*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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

Withholding rates for taxpayers filing as *MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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

Withholding rates for taxpayers filing as *SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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
| 1,127,550   | And over         | 0              | .1170        | 0                  |


#### Withholding changes for Oklahoma

Withholding rates for taxpayers filing as *MARH*


| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 12,700           | 0              | 0%           | 0                  |
| 12,700      | 14,700           | 0              | .25%         | 12,700             |
| 14,700      | 17,700           | 5.00           | .75%         | 14,700             |
| 17,700      | 20,200           | 27.50          | 1.75%        | 17,700             |
| 20,200      | 22,500           | 71.25          | 2.75%        | 20,200             |
| 22,500      | 24,900           | 134.50         | 3.75%        | 22,500             |
| 24,900      | And Over         | 224.50         | 4.75%        | 24,900             |


Withholding rates for taxpayers filing as *SINGLE*, *MFS*, *MAR2*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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

New Filing status for 2020 NOWH - No Withholding Provided - Flat tax rate of 8% (remains for 2022 year)

HB2119 requires employers to withhold income tax at a rate of 8 percent of employee wages if they employee has not provided a withholding statement or exemption certificate.  
Continue withholding at the 8 percent rate until the employee submits a withholding statement and exemption certificate.


Special Tax Type rates for MS3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
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

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 7,250          | 0%           | 0                  |
| 49,999      | 124,999          | 7,250          | 0%           | 0                  |
| 124,999     | 129,999          | 5,800          | 0%           | 0                  |
| 129,999     | 134,999          | 4,350          | 0%           | 0                  |
| 134,999     | 139,999          | 2,900          | 0%           | 0                  |
| 139,999     | 144,999          | 1,450          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

Tax Type rates for MS3 and S3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 37,910           | 0              | 0%           | 0                  |
| 37,910      | 250,000          | 1,126          | 8.75%        | 18,900             |
| 250,000     | And over         | 21,347         | 9.9%         | 250,000            |

Tax Type rates for S2 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 40,330           | 0              | 0%           | 0                  |
| 40,330      | 125,000          | 563            | 8.75%        | 9,450              |
| 125,000     | And Over         | 10,674         | 9.9%         | 125,000            |

Low Income Type rates for MS3 and S3 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,500            | 219            | 4.75%        | 0                  |
| 7,50 0      | 18,900           | 575            | 6.75%        | 7,500              |
| 18,900      | 50,000           | 1,345          | 8.75%        | 18,900             |

Low Income Type rates for S2 Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,750            | 219            | 4.75%        | 0                  |
| 3,750       | 9,450            | 397            | 6.75%        | 3,750              |
| 9,450       | 50,000           | 761            | 8.75%        | 9,450              |


#### Withholding changes for South Carolina

The Personal Exemption is $2,670 for Filing Status ONE.
The Standard Deduction Maximum is $4,200 for ONE Filing Status.

Tax Type rates for all Filing Status:

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,900            | 0              | 0.2%         | 0                  |
| 2,900       | 5,960b           | -83.44         | 3.0%         | 0                  |
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
