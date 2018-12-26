**U.S. 2019 January Payroll Tax Update**

For Microsoft Dynamics GP Round 1
=================================

Applies to:

>   Microsoft Dynamics GP 2018 on Microsoft SQL Server

>   Microsoft Dynamics GP 2016 on Microsoft SQL Server

>   Microsoft Dynamics GP 2015 on Microsoft SQL Server

**Summary:** This document contains instructions for installing the January 2019
Round 1 U.S. Payroll Tax Update for Microsoft Dynamics GP.

This is the first tax update for 2019. It includes federal and state tax table
changes that take effect January 1, 2019. You’ll need to install this update
before processing your first payroll runs for 2019.

This document assumes that you are familiar with the Microsoft Dynamics GP U.S.
Payroll module.

Contents
--------

*Changes in this update*

*Resources to assist you*

*Preparing for installation*

*Installing the tax update Copyright and legal notices*

Changes in this update
======================

-   Federal changes and FICA Limit

-   California

-   Georgia

-   Iowa

-   Illinois

-   Kentucky

-   Maine

-   Maryland

-   Minnesota

-   New York

-   New York – Yonkers

-   North Carolina

-   Ohio

-   Oregon

-   South Carolina

2019 Federal tax changes
------------------------

The maximum taxable earnings for Social Security increase in 2019 to \$132,900
from \$128,400

The Personal Exemption is \$4,200 from \$4,150 for MAR and SINGLE filing status.

*Withholding rates for taxpayers filing as NRA*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,500            | 0              | 10%          | 0                  |
| 5,500       | 35,275           | 970.00         | 12%          | 5,500              |
| 35,275      | 80,000           | 4,543.00       | 22%          | 35,275             |
| 80,000      | 156,525          | 14,382.50      | 24%          | 80,000             |
| 156,525     | 199,900          | 32,748.50      | 32%          | 156,525            |
| 199,900     | 506,100          | 46,628.50      | 35%          | 199,900            |
| 506,100     | And Over         | 153,798.50     | 37%          | 506,100            |

*Withholding rates for taxpayers filing as MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 11,800           | 0              | 0%           | 0                  |
| 11,800      | 31,200           | 0              | 10%          | 11,800             |
| 31,200      | 90,750           | 1,940.00       | 12%          | 31,200             |
| 90,750      | 180,200          | 9,086.00       | 22%          | 90,750             |
| 180,200     | 333,250          | 28,765.00      | 24%          | 180,200            |
| 333,250     | 420,000          | 65,497.00      | 32%          | 333,250            |
| 420,000     | 624,150          | 93,257.00      | 35%          | 420,000            |
| 624,150     | And Over         | 164,709.50     | 37%          | 624,150            |

*Withholding rates for taxpayers filing as SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,800            | 0              | 0%           | 0                  |
| 3,800       | 13,500           | 0              | 10%          | 3,800              |
| 13,500      | 43,275           | 970.00         | 12%          | 13,500             |
| 43,275      | 88,000           | 4,543.00       | 22%          | 43,275             |
| 88,000      | 164,525          | 14,382.50      | 24%          | 88,000             |
| 164,525     | 207,900          | 32,748.50      | 32%          | 164,525            |
| 207,900     | 514,100          | 46,628.50      | 35%          | 207,900            |
| 514,100     | And Over         | 153,798.50     | 37%          | 514,100            |

2019 state or territorial tax changes
-------------------------------------

The following tax changes are included in this update:

### Withholding changes for California

For Filing Status of HOH  
Personal Exemption is \$129.80 from \$125.40  
Standard Deduction is \$8,802 from \$8,472  
Low Income Limit is \$29,146 from \$28,095

For Filing Status of MAR1  
Personal Exemption is \$129.80 from \$125.40  
Standard Deduction is \$4,401 from \$4,236  
Low Income Limit is \$14,573 from \$14,048

For Filing Status of MAR2  
Personal Exemption is \$129.80 from \$125.40  
Standard Deduction is \$8,802 from \$8,472  
Low Income Limit is \$29,146 from \$28,095

For Filing Status of SINGLE  
Personal Exemption is \$129.80 from \$125.40  
Standard Deduction is \$4,401 from \$4,236  
Low Income Limit is \$14,573 from \$14,048

*Withholding rates for taxpayers filing as HOH*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 17,099           | 0              | 1.1%         | 0                  |
| 17,099      | 40,512           | 188.09         | 2.2%         | 17,099             |
| 40,512      | 52,224           | 703.18         | 4.4%         | 40,512             |
| 52,224      | 64,632           | 1,218.51       | 6.6%         | 52,224             |
| 64,632      | 76,343           | 2,037.44       | 8.8%         | 64,632             |
| 76,343      | 389,627          | 3,068.01       | 10.23%       | 76,343             |
| 389,627     | 467,553          | 35,116.96      | 11.33%       | 389,627            |
| 467,553     | 779,253          | 43,945.98      | 12.43%       | 467,553            |
| 779,253     | 1,000,000        | 82,690.29      | 13.53%       | 779,253            |
| 1,000,000   | And Over         | 112,557.36     | 14.63%       | 1,000,000          |

*Withholding rates for taxpayers filing as MAR1 and MAR2*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 17,088           | 0              | 1.1%         | 0                  |
| 17,088      | 40,510           | 187.97         | 2.2%         | 17,088             |
| 40,510      | 63,938           | 703.25         | 4.4%         | 40,510             |
| 63,938      | 88,754           | 1,734.08       | 6.6%         | 63,938             |
| 88,754      | 112,170          | 3,371.94       | 8.8%         | 88,754             |
| 112,170     | 572,984          | 5,432.55       | 10.23%       | 112,170            |
| 572,984     | 687,576          | 52,573.82      | 11.33%       | 572,984            |
| 687,576     | 1,000,000        | 65,557.09      | 12.43%       | 687,576            |
| 1,000,000   | 1,145,961        | 104,391.39     | 13.53%       | 1,000,000          |
| 1,145,961   | And Over         | 124,139.90     | 14.63%       | 1,145,961          |

*Withholding rates for taxpayers filing as SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 17,088           | 0              | 1.1%         | 0                  |
| 17,088      | 40,510           | 187.97         | 2.2%         | 17,088             |
| 40,510      | 63,938           | 703.25         | 4.4%         | 40,510             |
| 63,938      | 88,754           | 1,734.08       | 6.6%         | 63,938             |
| 88,754      | 112,170          | 3,371.94       | 8.8%         | 88,754             |
| 112,170     | 572,984          | 5,432.55       | 10.23%       | 112,170            |
| 572,984     | 687,576          | 52,573.82      | 11.33%       | 572,984            |
| 687,576     | 1,000,000        | 65,557.09      | 12.43%       | 687,576            |
| 1,000,000   | 1,145,961        | 104,391.39     | 13.53%       | 1,000,000          |
| 1,145,961   | And Over         | 124,139.90     | 14.63%       | 1,145,961          |

### Withholding changes for Georgia

The Dependent Allowance remains at \$3,000  
The Personal Allowance remains unchanged, Standard Deductions changed

Standard Deductions

HOH \$4600.00  
MFJ1I \$6000.00  
MFJ2I \$3000.00  
MFS \$3000.00  
SINGLE \$4600.00

*Withholding rates for taxpayers filing as HOH and MFJ1I*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,000            | 0              | 1.0%         | 0                  |
| 1,000       | 3,000            | 10.00          | 2.0%         | 1,000              |
| 3,000       | 5,000            | 50.00          | 3.0%         | 3,000              |
| 5,000       | 7,000            | 110.00         | 4.0%         | 5,000              |
| 7,000       | 10,000           | 190.00         | 5.0%         | 7,000              |
| 10,000      |                  | 340.00         | 5.75%        | 10,000             |

*Withholding rates for taxpayers filing as MFJ2I and MFS*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 500              | 0              | 1.0%         | 0                  |
| 500         | 1,500            | 5.00           | 2.0%         | 500                |
| 1,500       | 2,500            | 25.00          | 3.0%         | 1,500              |
| 2,500       | 3,500            | 55.00          | 4.0%         | 2,500              |
| 3,500       | 5,000            | 95.00          | 5.0%         | 3,500              |
| 5,000       |                  | 170.00         | 5.75%        | 5,000              |

*Withholding rates for taxpayers filing as SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 750              | 0              | 1.0%         | 0                  |
| 750         | 2,250            | 7.50           | 2.0%         | 750                |
| 2,250       | 3,750            | 37.50          | 3.0%         | 2,250              |
| 3,750       | 5,250            | 82.50          | 4.0%         | 3,750              |
| 5,250       | 7,000            | 142.50         | 5.0%         | 5,250              |
| 7,000       |                  | 230.00         | 5.75%        | 7,000              |

### Withholding changes for Iowa

The Standard Deduction Amount for Filing Status EXP1 is \$1690.00 and Filing
Status EXP2 is \$4160.00

*Withholding rates for taxpayers filing as EXP1 and EXP2 are as follows:*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 1,333            | 0              | 0.33%        | 0                  |
| 1,333       | 2,666            | 4.40           | 0.67%        | 1,333              |
| 2,666       | 5,331            | 13.33          | 2.25%        | 2,666              |
| 5,331       | 11,995           | 73.29          | 4.14%        | 5,331              |
| 11,995      | 19,992           | 349.18         | 5.63%        | 11,995             |
| 19,992      | 26,656           | 799.41         | 5.96%        | 19,992             |
| 26,656      | 39,984           | 1,196.58       | 6.25%        | 26,656             |
| 39,984      | 59,976           | 2,029.58       | 7.44%        | 39,984             |
| 59,976      |                  | 3,516.98       | 8.53%        | 59,976             |

### Withholding changes for Illinois

The Dependent Exemptions is \$2,275

### Withholding changes for Kentucky

The Standard Deduction changed to \$2590 from \$2530  
The Flat Tax Rate remains at 5%

### Withholding changes for Maine

The Personal Exemption changed from \$4150.00 to \$4200.00 for all Filing
Status’

*Withholding rates for taxpayers filing as SINGLE, Tax table type*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
|  0          | 21,850           | 0              | 5.8%         | 0                  |
| 21,850      | 51,700           | 1,267          | 6.75%        | 21,850             |
| 51,700      | And over         | 3,282          | 7.15%        | 51,700             |

*Special table type*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 81,450           | 0              | 0            | 9,350              |
| 81,450      | 156,450          | 75,000         | 0            | 0                  |

*Withholding rates for taxpayers filing as MAR, Tax table type*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 43,700           |                | 5.80%        | 0                  |
| 43,700      | 103,400          | 2,535          | 6.75%        | 43,700             |
| 103,400     | And Over         | 6,565          | 7.15%        | 103,400            |

*Special table type*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 81,450           | 0              | 0            | 9,350              |
| 81,450      | 156,450          | 75,000         | 0            | 0                  |

### Withholding changes for Maryland

*Withholding rates for taxpayers filing as CARLNE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.95%        | 0                  |
| 100,000     | 125,000          | 7,950          | 8.20%        | 100,000            |
| 125,000     | 150,000          | 10,000         | 8.45%        | 125,000            |
| 150,000     | 250,000          | 12,112.50      | 8.70%        | 150,000            |
| 250,000     | And Over         | 20,812.50      | 8.95%        | 250,000            |

*Withholding rates for taxpayers filing as CLMAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | .%           | 0                  |
| 5,000       | 150,000          | 0              | 7.95%        | 0                  |
| 150,000     | 175,000          | 11,925.00      | 8.20%        | 150,000            |
| 175,000     | 225,000          | 13,795.00      | 8.45%        | 175,000            |
| 225,000     | 300,000          | 18,200.00      | 8.70%        | 225,000            |
| 300,000     | And over         | 24,725.00      | 8.95%        | 300,000            |

*Withholding rates for taxpayers filing as CECIL*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | 0%           | 0                  |
| 5,000       | 100,000          | 0              | 7.75%        | 0                  |
| 100,000     | 125,000          | 7,750.00       | 8.00%        | 100,000            |
| 125,000     | 150,000          | 9,750          | 8.25%        | 125,000            |
| 150,000     | 250,000          | 11,812.50      | 8.50%        | 150,000            |
| 250,000     | And Over         | 20,312.50      | 8.75%        | 250,000            |

*Withholding rates for taxpayers filing as CCMAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | .%           | 0                  |
| 5,000       | 150,000          | 0              | 7.75%        | 0                  |
| 150,000     | 175,000          | 11,625.00      | 8.00%        | 150,000            |
| 175,000     | 225,000          | 13,625.00      | 8.25%        | 175,000            |
| 225,000     | 300,000          | 17,750.00      | 8.50%        | 225,000            |
| 300,000     | And over         | 24,125.00      | 8.75%        | 300,000            |

### Withholding changes for Minnesota

*Withholding rates for taxpayers filing as MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 9,050            | 0              | 0            | 0                  |
| 9,050       | 47,820           | 0              | 5.35%        | 9,050              |
| 47,820      | 163,070          | 2,074.20       | 7.05%        | 47,820             |
| 163,070     | 282,200          | 10,199.33      | 7.85%        | 163,070            |
| 282,200     | And over         | 19,551.04      | 9.85%        | 282,200            |

*Withholding rates for taxpayers filing as SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,400            | 0              | 0            | 0                  |
| 2,400       | 28,920           | 0              | 5.35%        | 2,400              |
| 28,920      | 89,510           | 1,418.82       | 7.05%        | 28,920             |
| 89,510      | 166,290          | 5,690.42       | 7.85%        | 89,510             |
| 166,290     | And over         | 11,717.65      | 9.85%        | 166,290            |

### Withholding changes for New York and New York-Yonkers

*Withholding rates for taxpayers filing as MAR*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8500             | 0              | .0400        | 0                  |
| 8,500       | 11,700           | 340.00         | .0450        | 8,500              |
| 11,700      | 13,900           | 484.00         | .0525        | 11,700             |
| 13,900      | 21,400           | 600.00         | .0590        | 13,900             |
| 21,400      | 80,650           | 1,042.00       | .0621        | 21,400             |
| 80,650      | 96,800           | 4,721.00       | .0649        | 80,650             |
| 96,800      | 107,650          | 5,770.00       | .0764        | 96,800             |
| 107,650     | 157,650          | 6,599.00       | .0814        | 107,650            |
| 157,650     | 211,550          | 10,669.00      | .0790        | 157,650            |
| 211,550     | 323,200          | 14,927.00      | .0699        | 211,550            |
| 323,200     | 373,200          | 22,731.00      | .0968        | 323,200            |
| 373,200     | 1,077,550        | 27,571.00      | .0735        | 373,200            |
| 1,077,550   | 2,155,350        | 79,341.00      | .0765        | 1,077,550          |
| 2,155,350   | 2,205,350        | 161,792.00     | .9454        | 2,155,350          |
| 2,205,350   | And over         | 209,062.00     | .0962        | 2,205,350          |

*Withholding rates for taxpayers filing as SINGLE*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 8500             | 0              | .0400        | 0                  |
| 8,500       | 11,700           | 340.00         | .0450        | 8,500              |
| 11,700      | 13,900           | 484.00         | .0525        | 11,700             |
| 13,900      | 21,400           | 600.00         | .0590        | 13,900             |
| 21,400      | 80,650           | 1,042.00       | .0621        | 21,400             |
| 80,650      | 96,800           | 4,721.00       | .0649        | 80,650             |
| 96,800      | 107,650          | 5,770.00       | .0752        | 96,800             |
| 107,650     | 157,650          | 6,585.00       | .0802        | 107,650            |
| 157,650     | 215,400          | 10,595.00      | .0699        | 157,650            |
| 215,400     | 265,400          | 14,632.00      | .0890        | 215,400            |
| 265,400     | 1,077,550        | 19,082.00      | .0735        | 265,400            |
| 1,077,550   | 1,127,550        | 78,775.00      | .5208        | 1,077,550          |
| 1,127,550   | And over         | 104,815.00     | .0962        | 1,127,550          |

### Withholding changes for North Carolina

The Standard Deduction amount changed to \$15,000 from \$14,000 for Filing
Status of HOH

The Standard Deduction amount changed to \$10,000 from \$8,7500 for Filing
Status of MAR and SINGLE

The tax rate for all Filing Statues’ is 5.35% from 5.599%

### Withholding changes for Ohio

*Withholding rates for taxpayers filing as NA*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 5,000            | 0              | .538%        | 0                  |
| 5,000       | 10,000           | 26.90          | 1.075%       | 5,000              |
| 10,000      | 15,000           | 80.65          | 2.153%       | 10,000             |
| 15,000      | 20,000           | 188.30         | 2.690%       | 15,000             |
| 20,000      | 40,000           | 322.80         | 3.228%       | 20,000             |
| 40,000      | 80,000           | 968.40         | 3.765%       | 40,000             |
| 80,000      | 100,000          | 2474.40        | 4.304%       | 80,000             |
| 100,000     | And over         | 3335.20        | 5.379%       | 100,000            |

### Withholding changes for Oregon

The Standard Deduction Amount is \$4,545 for MS3 and S3 Filing Status.

The Standard Deduction Amount is \$2,270 for S2 Filing Status.

*Special Tax Type rates for MS3 Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 6,800          | 0%           | 0                  |
| 49,999      | 249,999          | 6,800          | 0%           | 0                  |
| 249,999     | 259,999          | 5,450          | 0%           | 0                  |
| 259,999     | 269,999          | 4,100          | 0%           | 0                  |
| 269,999     | 279,999          | 2,700          | 0%           | 0                  |
| 279,999     | 289,999          | 1,350          | 0%           | 0                  |
| 289,999     | And over         | 0              | 0%           | 0                  |
|             |                  |                |              |                    |

*Special Tax Type rates for S2 and S3 Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 49,999           | 6,800          | 0%           | 0                  |
| 49,999      | 124,999          | 6,800          | 0%           | 0                  |
| 124,999     | 129,999          | 5,450          | 0%           | 0                  |
| 129,999     | 134,999          | 4,100          | 0%           | 0                  |
| 134,999     | 139,999          | 2,700          | 0%           | 0                  |
| 139,999     | 144,999          | 1,350          | 0%           | 0                  |
| 144,999     | And over         | 0              | 0%           | 0                  |

*Tax Type rates for MS3 and S3 Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 38,655           | 0              | 0%           | 0                  |
| 38,655      | 250,000          | 1,104          | 9%           | 17,800             |
| 250,000     | And over         | 22,002         | 9.9%         | 250,000            |
|             |                  |                |              |                    |

*Tax Type rates for S2 Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 40,930           | 0              | 0%           | 0                  |
| 40,930      | 125,000          | 552            | 9%           | 8,900              |
| 125,000     | And Over         | 11,001         | 9.9%         | 125,000            |

*Low Income Type rates for MS3 and S3 Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 7,100            | 206            | 5%           | 0                  |
| 7,100       | 17,800           | 561            | 7%           | 7,100              |
| 17,800      | 50,000           | 1,310          | 9%           | 17,800             |
| 0           | 0                | 0              | 0            | 0                  |

*Low Income Type rates for S2 Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 3,550            | 206            | 5%           | 0                  |
| 3,550       | 8,900            | 383.50         | 7%           | 3,550              |
| 8,900       | 50,000           | 758            | 9%           | 8,900              |

### <br>Withholding changes for South Carolina

The Personal Exemption is \$2,510 for Filing Status ONE.

The Standard Deduction Maximum is \$3,470 for ONE Filing Status.

*Tax Type rates for all Filing Status*

| If Over     | But Not Over     | Tax Amount     | Tax Rate     | On Excess Over     |
|-------------|------------------|----------------|--------------|--------------------|
| 0           | 2,450            | 0              | 1.1%         | 0                  |
| 2,450       | 4,900            | (46.55)        | 3%           | 2,450              |
| 4,900       | 7,350            | (95.55)        | 4%           | 4,900              |
| 7,350       | 9,800            | (169.05)       | 5%           | 7,350              |
| 9,800       | 12,250           | (267.05)       | 6%           | 9,800              |
| 12,250      | And over         | (389.55)       | 7%           | 12,250             |

Resources to assist you
=======================

If you have questions about U.S. Payroll tax updates and your Microsoft Partner
isn’t available, there are several resources, in addition to this document, to
assist in answering your questions.

U.S. Payroll Tax Updates on CustomerSource
------------------------------------------

[(https://mbs.microsoft.com/customersource/support/downloads/taxupdates/)](https://mbs.microsoft.com/customersource/support/downloads/taxupdates/)

Look here to find out the tax changes included in each update and to download
the update. All instructions for downloading and installing the tax updates also
are provided here.

Knowledge Base
--------------

[(https://mbs.microsoft.com/knowledgebase/search.aspx)](https://mbs.microsoft.com/knowledgebase/search.aspx)

Provides you with instant access to the same database our support engineers use.
You can find answers to common questions, along with technical tips and
performance recommendations.

eSupport
--------

[(https://mbs.microsoft.com/support/newstart.aspx)](https://mbs.microsoft.com/support/newstart.aspx)

For support requests that can be handled with email. On average, the response
time is nearly twice as fast as telephone support.

Discussion
----------

[(https://community.dynamics.com/gp)](https://community.dynamics.com/gp)

Start a tax update discussion with other members of the Microsoft customer
community. This database provides you with the opportunity to exchange
information with other customers, which is perfect for providing tips and
answers to questions about tax updates.

Microsoft Business Solutions Human Resources/Payroll support team
-----------------------------------------------------------------

We have a support team focused 100 percent on providing service and support to
our Payroll customers. If you have questions, dial toll free 888-GPS-SUPP
(888-477-7877).

Preparing for installation
==========================

Use the instructions in this section to prepare for the U.S. Payroll Tax Update.
For detailed information about the changes in the current tax update round, see
*Changes in this update*.

**Are you using a supported version?**

To identify the version, you’re using, start Microsoft Dynamics GP. Choose Help
\>\> About Microsoft Dynamics GP. The information window displays the version
number in the lower right corner.

This U.S. Payroll Tax Update is supported for Microsoft Dynamics GP 2018,
Microsoft Dynamics GP 2016, and Microsoft Dynamics GP 2015 on Microsoft SQL
Server.

If you’re not using one of the supported versions, you must upgrade to a
supported version before installing this tax update.

**Have you obtained the update files?**

If your computer is connected to the Internet, the Payroll Update Utility (PUE)
automatically can download the tax table update file (TX.cab) from the Internet.

If your computer isn’t connected to the Internet, you can obtain the file from
CustomerSource

[(https://mbs.microsoft.com/customersource/northamerica/GP/downloads)](https://mbs.microsoft.com/customersource/northamerica/GP/downloads)
or your Microsoft

Partner and copy it to your computer before running what’s known as a “manual”
installation.

Tax updates are distributed in the form of .CAB files. Copy the .CAB file to a
folder that you can readily access, such as the folder that contains
Dynamics.exe. Copying the .CAB file to your computer does not complete the
installation. Refer to the following section for instructions on how to install
the tax update.

Installing the tax update
=========================

The Round 1 January 2019 tax update installation can be run from any
workstation. The update installs payroll tax table data on the server computer
where your existing Microsoft Dynamics GP application data is located. You need
to install the tax table update only once.

If you have issues installing the update, review the article on [Tips to install
the U.S. Payroll Tax
Update.](https://community.dynamics.com/gp/b/dynamicsgp/archive/2017/05/09/tips-to-install-the-u-s-payroll-tax-update)

Before you begin, ask all Microsoft Dynamics GP users to exit the application
until the update is complete. Exit all other applications, turn off the screen
saver, and back up important data (including Forms.dic, Reports.dic, and
Dynamics.vba if they exist) before you proceed with the installation.

1.  Log onto Microsoft Dynamics GP with the system administrator rights, and
    open the Payroll Tax Update window.

>   (Microsoft Dynamics GP menu \>\> Maintenance \>\> U.S. Payroll Updates \>\>
>   Check for Tax Updates)

1.  Select an update method, and then choose Next.

![A screenshot of a cell phone Description automatically generated](media/a6b6f3f85d529f49182c1e66d23df8b5.jpg)

A screenshot of a cell phone Description automatically generated

A screenshot of a cell phone Description automatically generated

-   The Automatic option downloads the current tax table update from the
    Internet to the default location. An Internet connection is required.

-   The Manual option processes the tax table update from a location you choose.
    You might choose Manual if you need to update a computer that isn’t
    connected to the Internet. To use this method, you should already have
    obtained the tax table update file, TX.cab, and copied it to a location your
    computer can readily access.

1.  If you selected Automatic, enter your 10-digit authorized telephone number.
    Choose Log in to start the download.

>   If you selected Manual, specify the location where the tax table update file
>   is located.

1.  Choose Process to start the update.

2.  Verify that the latest Payroll tax table update has been installed.

>   Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\>
>   Payroll Tax. The Last Tax Update value should be 12/21/2018.

What’s next
-----------

If you upgrade to another version of Microsoft Dynamics GP, you must install the
most recent service pack (if any), as well as the most recent tax table updates
for that release, to ensure you have the latest tax information. Newer releases
of Microsoft Dynamics GP do not include current payroll tax information.
