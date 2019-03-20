---
title: "Advanced Payroll"
description: "Examine how advanced payroll works in Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 03/01/2019
---

# Microsoft Dynamics GP Advanced Payroll

Microsoft Dynamics GP Advanced Payroll includes the following modules:

- Pay Policy Manager

- Payroll Hours to General Ledger

- Labor Accrual Manager

- Advanced Labor Reporting

**Pay Policy Manager** integrates with the Microsoft Dynamics GP Payroll module. When entering transactions through the Transaction Entry window the pay rate is adjusted based on the Employee, Employee Pay Code, Company, Department, Position and Shift Code selected, or the linked pay code selections on the Employee Pay Code Options window. The pay rate calculated is saved at the time the transaction is entered for use during that pay run.

**Payroll Hours to General Ledger** allows setup for the system to post actual labor hours to General Ledger Unit Accounts. The Microsoft Dynamics GP Payroll Posting Account setup window has been modified to allow a Unit Account to be assigned. Additionally, there is an option on the Pay Code Setup that allows, at a Pay Code level, which payroll transaction hours are
posted.

**Labor Accrual Manager** is designed specifically to fulfill the need of companies that are required to account for payroll accruals within a month that are not accounted for when the pay period ends prior to the end of that month. Once per month, near or shortly after the end of a month, accounting personnel must create payroll accruals for accurate financial reporting. Labor Accrual Manager fulfills this need as it allows the creation of the payroll accruals and posting to the general ledger as well as setting a
reversing date to be reversed out of the general ledger.

**Advanced Labor Reporting** extends department level reporting for both Payroll and Financial data. It also extends reporting for Full-Time Equivalent data as well as Productive and Non-Productive employee level data. Additional reporting features include Full-Time Equivalent Budgets and variances, current and YTD totals.

## CHAPTER 1: ADVANCED PAYROLL ESSENTIALS AND SETUP

The objectives are:

- Use Security Task Setup window to edit security tasks for Advanced Payroll modules.

- Use Security Roles Setup window to edit security roles for Advanced Payroll modules.

- Attain understanding of Pay Policy Manager Essentials.

- Set up Pay Policy Manager to activate the functionality of the Adjusted Pay Rate and set up the Transaction Auto-Split Setup window.

- Attain understanding of Payroll Hours to General Ledger essentials.

- Set up Payroll Posting Accounts for Payroll Hours to General Ledger.

- Set up Pay Code Options for Payroll Hours to General Ledger.

- Attain understanding of Labor Accrual Manager essentials.

- Set up Payroll Posting Accounts for Labor Accrual Manager.

- Set up Labor Accrual Accounts for Labor Accrual Manager.

- Set up Pay Code Options for Labor Accrual Manager.

- Attain understanding of Advanced Labor Reporting essentials.

- Set up Labor Reporting Accounts for Advanced Labor Reporting.

- Set up Areas of Responsibility for Advanced Labor Reporting.

- Set up Payroll Account Mapping for Advanced Labor Reporting.

- Set up Pay Code Options for Advanced Labor Reporting.

- Understand the Advanced Labor Reporting FTE calculation.

### Security Setup for Advanced Payroll

### Setting up a Security Task

Use the Security Task Setup window to select a default Advanced Payroll security task or modify the default security task. To open this window, click the **Administration** series button, click **System** on the Setup content pane and then click **Security Tasks**.

Enter a **Task ID**.

Select **HRM Solutions Series** for the **Product**.

- Select **Windows** for the **Type**

- Select **3rd Party** for the **Series**

- Select the following from the **Access List**:

##### o Add-On Setup o Add-Ons

**Area of Responsibility**
**Area of Responsibility Setup**
**Company Pay Policy Setup**
**Department Reports**
**Employee Pay Code Options**
**Employee Pay Policy Exceptions**
**Labor Accrual Accounts**
**Labor Reporting Accounts**
**Labor Reporting Code Setup**
**Labor Reporting Codes**
**Pay Code Options**
**Pay Policies**
**Pay Policy Priority Setup**
**Payroll Account Mapping**
**Payroll Accruals**
**Transaction Auto-Split Setup** 

Change the **Type** to **Reports**

Select the following from the **Access List** 
**APR Area of Responsibility**
**APR Benefit Accrual Report**
**APR Department Analysis Report**
**APR Department Analysis Report Summary**
**APR Employee Analysis Report**
**APR FTE YTD Report**
**APR Labor Reporting Code**
**APR Payroll Accrual Preview**
**APR Transaction Auto-Split Setup**
**Employee Pay Policies Report-Actual** 
**Employee Pay Policies Report-Hypothetical**
**Pay Policies Report-Actual** 
**Pay Policies Report-Hypothetical** 
**Payroll Account Mapping**

Click **Save** to save the selections and close the window.

### Setting up Alternate/Modified Forms and Reports Security

Use the Alternate/Modified Forms and Reports window to set access to the alternate/modified forms for Advanced Payroll. To open this window, click the **Administration** series button, click **System** on the Setup content pane and then click **Alternate/Modified Forms and Reports**.

Select the appropriate **ID**.

Select **HRM Solutions Series** for the **Product**.

Select **Windows** for the **Type**.

- Expand the Payroll folder and select the HRM Solution Series radio button for each of the following Alternate Core Microsoft Dynamics GP windows.

    - **Department Setup** o **Employee Maintenance** o **Employee Pay Code Maintenance** o **Pay Code Setup** o **Payroll Mass Transaction Entry**
        o **Payroll Posting Accounts Setup**

    - **Payroll Transaction Entry** o **Position Setup** o **Shift Code Setup**

Change the **Type** to **Report**.

- Expand the Payroll folder and select HRM Solution Series radio button for each of the following Alternate Core Microsoft Dynamics GP Reports.

**Check Posting Register** 
**Payroll Posting Accounts** 
**Reprint Check Posting Register**

Click **Save** to save the selections and close the window.

### Setting up Security Roles

Use the Security Role Setup window to select a default security role for Advanced Payroll or modify the default security role. To open this window, click the **Administration** series button, click **System** on the Setup content pane, and then click **Security Roles**.

### Pay Policy Manager Essentials

Pay Policy Manager automates the advanced rate calculation process by allowing the administration of all standard and overtime policies for hourly employees working in multiple departments and positions with a variety of base pay rates, shift differentials and pay rate add-on amounts. Additional features and capabilities include the following:

- Implement Add-On Amounts at multiple levels; Employee Pay Code, Company, Department, Position and Shift.

- Assign and View Pay Policies on a Pay Code level.

- Analyze Hypothetical Pay Policy options and view their impact on the Adjusted Pay Rate.

- Create employee specific Pay Policies exceptions.

- Link pay codes to hour based pay codes.

- Set a pay code Pay Rate to the percentage of the Linked pay code.

- Force the pay rate to a minimum amount.

- Roll down from setup level functionality.

- Set up Transaction Auto-Split for any employee and position combination.

The Calculate button has been added to the Payroll Transaction Entry window to calculate pay rates.

Pay Policy Priority determines which calculation factor has priority when calculating the Adjusted Pay Rate.

### What is a Pay Policy?

A Pay Policy is the combination of any five of the calculation factors:

- Employee Pay Code

- Company

- Department

- Position

- Shift Code

While standard Pay Policies (or combinations of the five factors) may exist, any combination assigned at the payroll transaction level is a Pay Policy and is used to calculate the Pay Rate Adjustment.

- The Calculate button has been added to the Payroll Transaction Entry window that will allow the user to calculate pay rates. This means that when an existing batch that contains transactions is opened, when Calculate is pressed, any pay policies that have changed since the last calculate that will affect the Pay Rate will be seen.

- The Pay Rate calculated at the time the transaction is entered will be saved for use during that pay run.

- The only restriction to Pay Policy combinations is that only hourly Pay Codes can be used.

### Pay Policy Example

| **Field**  | **Selection** | **Add-On Code** | **Add-On Amount** |
|------------|---------------|-----------------|-------------------|
| Pay Code   | HOUR          |                 |                   |
| Company    | SEC           | A01 assigned    | \$1.00            |
| Department | ADMN          | A04 assigned    | 5%                |
| Position   | Sale          | A05 assigned    | \$0.05            |
| Shift Code | 03            | A01 assigned    | \$1.00            |

Any eligible employee that has a payroll transaction entry assigned to this combination of calculation factors has theses Add-On Codes and Add-On Amounts applied to calculate their Adjusted Pay Rate.

For Example, when the Employee ACKE0001 is assigned Employee Pay Code HOUR at an hourly Pay Rate of \$10.00, the Adjusted Pay Rate would be calculated for the payroll transaction as follows:

| **Field**         | **Selection** | **Field**         | **Selection** |
|-------------------|---------------|-------------------|---------------|
| Employee Pay Code | HOUR          | Pay Rate          | \$10.00       |
| Company           | SEC           | Add-On A01 Amount | \$1.00        |
|                   |               | Subtotal          | \$11.00       |
| Department        | ADMN          | Add-On A04 Amount | 5%            |
|                   |               | Subtotal          | \$11.55       |
| Position          | SALE          | Add-On A05 Amount | \$0.05        |
|                   |               | Subtotal          | \$11.60       |
| Shift Code        | 03            | Add-On A01 Amount | \$1.00        |
| Adjusted Pay Rate |               |                   | \$12.60       |

This example is calculated using a Pay Policy Priority of Company,Department, Position and Shift Code.

### Setting up Pay Policy Manager

Several important settings must be correctly set up for the Pay Policy Manager Adjusted Pay Rate functionality to be activated.

### Add-On Setup

Use the Add-On Setup window to set up Add-On Codes and corresponding Amounts. To open this window, click the **HR and Payroll** series button, click **Pay Policy Manager** on the Setup content pane and then click **Add-On Setup**.

These Add-On Codes can be assigned to various calculation factors throughout to define specific pay policies that can be applied. This data is used to provide adjustments to the Pay Rate based on criteria in the payroll transaction entries.

Calculation factors that may affect the Pay Rate include:

- Company

- Department

- Position

- Shift Code

- Employee Pay Code

### Pay Policy Priority Setup

Use the Pay Policy Priority window to determine which calculation factor has priority when calculating the Adjusted Pay Rate. To open this window, click the **HR and Payroll** series button, click **Pay Policy Manager** on the Setup content pane and then click **Pay Policy Priority Setup**. 

The Pay Policy Priority Setup window is used to define a priority order for the different calculation factors.

- Before Pay Policy Manager can function, the Pay Policy Priority must be set.

- During the calculation process, when Add-On Codes are assigned to various calculation factors the calculations occur in order based on the Pay Policy Priority Setup.

- The Pay Policy Priority order can affect the calculated Adjusted Pay Rate when percentage based Add-On Codes are utilized.

- The Pay Policy Priority Setup does not include the Employee Pay Code calculation factor. The Employee Pay Code Add-On is always applied as the first calculation. That adjusted pay rate is then sent through the Pay Policy Priority adjustments following the priority set in the Pay Policy Priority Setup window.

Changing the Pay Policy Priority Setup changes the adjusted pay rates for any calculations where a percentage based Add-On Code is assigned. When selecting “Save” a message prompts, “Changing the Pay Policy

Priority will change adjusted Pay Rates. Continue with changes? Yes No.”

### Assigning Pay Policies

The Pay Policy Manager calculates Adjusted Pay Rates based on AddOn Codes assigned to the five calculation factors:

- Employee Pay Code

- Company

- Department

- Position

- Shift Code

A payroll transaction consists of any combination of these five calculation factors.

- The combination of calculation factors assigned to the payroll transaction is used to determine the Adjusted Pay Rate.

- An employee can have a transaction with any combination of these five calculation factors.

- Pay Policy Manager provides two options for assigning AddOn Codes to these calculation factors. o Pay Policy Setup by Calculation Factor o Pay Policy Setup by Pay Code

##### Pay Policy Setup by Calculation Factor

The option of assigning Add-On Codes by calculation factor is handled through the following windows. Each individual calculation factor can be assigned an Add-On Code using the setup windows.

- Employee Pay Code

- Company Pay Policy Setup

- Department Setup

- Position Setup

- Shift Code Setup

##### Pay Policy Setup by Pay Code

The option of assigning Add-On Codes by Pay Code is handled through the Pay Policies window.

- Use the Pay Policies window to assign and view Pay Policies for each Pay Code.

- Pay Policy combinations are not limited to what is set up in the

Pay Policies window. This window is used to easily assign Add-On Codes to calculation factors and view standard Pay Policies.

- Assigning Add-On Codes when using Pay Policies options is defined in more detail in the Pay Policies section of this document.

### Company Pay Policy Setup

Use the Company Pay Policy Setup window to associate an Add-On

Code to a Company defined in the system. To open this window, click the **HR and Payroll** series button, click **Pay Policy Manager** on the Setup content pane and then click **Company Pay Policy Setup**.

![screenshot](media/4be45bdfbfa7fa5b8e5e1273c99fe1ca.jpg)

During the Adjusted Pay Rate calculations, this Add-On Code Amount may be
applied to an employee’s pay rate.

### Department Setup

Use the Department Setup window to associate an Add-On Code to a Department.
To open this window, click the **HR and Payroll** series button and then
click **Department** on the Setup content pane.

During the Adjusted Pay Rate calculations, this Add-On Code Amount may be
applied to an employee’s pay rate.

### Position Setup

Use the **Position Setup** window to associate an Add-On Code to a Position.
To open this window, click the **HR and Payroll** series button and then
click **Position** on the Setup content pane.

During the Adjusted Pay Rate calculations, this Add-On Code Amount may be
applied to an employee’s pay rate.

### Shift Code Setup

Use Shift Code Setup window to associate an Add-On Code to a Shift Code. To
open this window, click the **HR and Payroll** series button and then click
**Shift Code** on the Setup content pane.

During the Adjusted Pay Rate calculations, this Add-On Code Amount may be
applied to an employee’s pay rate.

When Advanced Payroll is installed, the Microsoft Dynamics GP Shift Code
Setup fields Shift Premium and Amount are not visible.

### Pay Code Options

Use the Pay Code Options window to designate a Linked Pay Code. To open this
window, click the **HR and Payroll** series button, click **Pay Code** on
the Setup content pane and then click **Pay Code Options** from the GoTo menu. The Pay Code Options window includes
functionality for Payroll Extensions and for Advanced Payroll.

The functionality specific to Advanced Payroll is discussed here.

![A screenshot](media/1b7a7d0d2105d38b4f108fcbcae8a9ea.jpg)

A linked pay code assigned disables the Use Add-On options. Pay Policy
Manager also looks at the pay rate of the linked pay code, and it uses the
add-ons of the linked pay code.

After a linked pay code has been entered, the Pay Percent and Minimum Amount
field become enabled.

- A percent can be entered for the linked pay code rate when the full 100%
    should not be used.

- The minimum amount can also be specified so the linked pay code and any
    add-on options do not exceed the minimum amount; the rate automatically is
    adjusted up to the minimum amount.

This window can also be used to specify an Add-On code and when an employee
is currently eligible for the pay rate. When the Use Add-On option is
selected and an Add-On Code is selected, this Add-On Code Amount is applied
to an eligible employee’s pay rate.

> [!NOTE]
> The Pay Code Setup information is for setup and default purposes only. It sets default values for any new Pay Code created using this Pay Code as the Based on Pay Code. It will also set default values when this Pay Code is associated with an Employee in the Employee Pay Code window.

- Linked Pay Code

- Pay Percent

- Minimum Amount

- Use Add-On

- Add-On Code

When a change is made to the field on the Pay Code Setup window, click Save
to save the changes. A roll down message is prompted, “Do you want to roll
down these changes to all employees with this pay code?”

- When **Yes** is selected, this Calculation Method is rolled down to all
    Employee Pay Code records for this same Pay Code.

- When **No** is selected, these values will not be rolled down to all
    Employee Pay Code records but the changes are saved to the Pay Code Setup
    record.

### Pay Policies

Use the Pay Policies window is to provide actual and hypothetical

Adjusted Pay Rate scenarios. To open this window, click the **HR and
Payroll** series button, click **Pay Policy Manager** on the Setup content
pane and then click **Pay Policies**.

![A screenshot](media/3682febe7f8380e092213bf04723673a.jpg)

Use this window to assign and/or view typical Pay Policies by Pay Code, or
to view Hypothetical Adjusted Pay Rates.

Select a **Pay Code** to open all Pay Policies currently assigned to that
Pay Code. This also enables the functionality of the Pay Policies window.
Choose to enter a Hypothetical Pay Code Rate and/or a Hypothetical Pay Code
Add-On.

When the Actual or Hypothetical fields are combined with the Calculate By
option discussed, the Adjusted Rate is calculated for every Pay Policy
defined in the window.

**HINT:** *The values entered into the Hypothetical fields do not update the
actual values saved in the Pay Code table. To use a hypothetical pay rate
adjustment, update the appropriate pay code information in the Pay Code
window, which will affect all actual Pay Policies for that Pay Code.*

Select a **calculation**:

- **Actual Calculations** - displays the amounts in the window that represent
    the most current actual data that exists. In a case where a Pay Policy was
    created using actual calculations, when the record is re-opened, all
    calculations are automatically re-figured based on the latest actual data
    available.

- **Hypothetical Calculations** - displays the amounts in the window that
    represent the amounts saved in the Pay Policies table. The values entered
    into the Hypothetical fields do not update the actual values saved in the
    Pay Code table.

The window displays all defined Pay Policies for the Pay Code selected.

- When a change is made to any Add-On Code assigned to a Company, Department,
    Position or Shift that has been used in a (actual or hypothetical) Pay
    Policy it triggers a recalculation of the pay policies Adjusted Rates.

- During the calculation of the Adjusted Rate in the window, a rounding of two
    decimal places during each step of the calculation occurs.

This window may not display all possible Pay Policy options for this Pay
Code.

- The Pay Policies set up in this window in no way impacts the actual
    calculations.

- Calculations are based only on the actual combination of Employee Pay Code,
    Company, Department, Position and Shift Code used in any hourly payroll
    transaction.

### Payroll Hours to General Ledger Essentials

During payroll processing with Microsoft Dynamics GP functionality,
currently only dollar amounts are posted to the General Ledger. Payroll
Hours to General Ledger will allow the system to be set up to post actual
labor hours to General Ledger Unit Accounts. The Microsoft Dynamics GP
Payroll Posting Account Setup window has been modified to allow the
assignment of a Unit Account. Additionally, an option exists on the Pay Code
Setup to determine at a Pay Code level that payroll transaction hours are to
be posted.

The features and capabilities of Payroll Hours to General Ledger include:

- Ability to set up pay codes to not post to General Ledger during the payroll
    process.

- A unit account can be assigned to a posting account in Payroll Posting
    Account setup.

- Can post hours to the General Ledger Unit Account during payroll processing.

Posting Hours to General Ledger works in conjunction with Labor Accrual
Manager. When Posting Hours to General Ledger is installed and registered,
the payroll hours will be posted to the General Ledger and will then be
available for use during the Labor Accrual Manager Payroll Accruals to
generate hour accrual journal entries.

### Processing with Payroll Hours to General Ledger

The Payroll Hours to General Ledger module processes at the same time as the
Microsoft Dynamics GP Payroll Processing/Posting.

- For each transaction, an attempt will be made to post the associated hours
    to a Unit Account.

- It first verifies that the Pay Code of that payroll transaction is not set
    “Do Not Post Hours.”

- When this option is not selected for the transaction’s pay code, an attempt
    will be made to find the appropriate Unit Account based on the setup in the
    modified Payroll Posting Account Setup window; comparing the payroll
    transaction department, position and pay code to the closest match of
    department, position and pay code.

- Posting Hours to General Ledger uses the same logic to determine which Unit
    Account to post to as Microsoft Dynamics GP Payroll uses to determine which
    Account to post amounts to.

### Modified Payroll Check Posting Register

The option exists to print the modified version of the Microsoft Dynamics GP
Payroll Check Posting Register report. When security is granted to the
modified report, the modified report will print instead of the Microsoft
Dynamics GP report during Payroll Posting. The report will display an
additional “Hours” column that will reflect any hours and their appropriate
Unit Account Number, Description and Employee ID.

### Modified Reprint Check Posting Register

The option exists to print the modified version of the Microsoft Dynamics GP
Reprint Check Posting Register report. When security is granted to the
modified report, the modified report will print instead of the Microsoft
Dynamics GP report when the “Check Posting Register” is selected from the
Reports \> Payroll \> Reprint Journals window. The report will display an
additional “Hours” column that will reflect any hours and their appropriate
Unit Account Number, Description and Employee ID.

### Other Settings that Impact Payroll Hours to the General Ledger

Many options are available when setting up Microsoft Dynamics GP payroll
posting and accounts. For Posting Hours to General Ledger (Microsoft
Dynamics GP menu \>Tools \> Setup \> Posting \> Posting) to properly
function, certain settings must be used. Other settings can be set either
way, but based on how they are set impact the values that will be calculated
for the Labor Accruals.

- Even when Payroll transactions are set up to post through to General Ledger,
    the posting of payroll hours to General Ledger will only post to General
    Ledger, not through.

- Payroll accruals will need to be manually posted in General Ledger once
    posted in the Payroll Accruals window to have unit accounts/hours posted in
    the General Ledger.

- Both “Create Journal Entry Per” Batch and Transaction are supported.

- “Allow Transaction Posting” may be selected or un-selected.

- The unit accounts assigned on the Payroll Posting Accounts window will need
    to be set up on the Unit Account Maintenance window (Cards \> Financial \>
    Unit Account) with Decimal Places = 2.

### Setting up Payroll Posting Accounts for Payroll Hours to General Ledger

To open the Posting Setup window, click the **Administration** series
button, click **Posting** on the Setup content pane and then click **Payroll
Accounts.**

![A screenshot](media/38faa911c7b27828dae0557600159f32.jpg)

The modified Payroll Posting Accounts Setup window has the “Unit

Account” field that affects the Posting Hours to General Ledger. A Unit
Account can be assigned assign to a Department, Position and (Pay) Code.

- The purpose of this field is to determine which Unit Account a specific
    payroll transaction hours should be posted to be based on the Department,
    Position and (Pay) Code combination.

- During payroll processing, the payroll transaction hours will be posted to
    the appropriate Unit Accounts.

#### Unit Account

Enter the unit account number for the labor hours to be posted to during
payroll processing. Unit Account Requirements include the following:

- Payroll Account Type must = Gross Pay (DR).

- The Pay Code in the row cannot have “Do Not Post Hours” selected at the Pay
    Code Options Setup level.

### Setting up Pay Code Options for Payroll Hours to General Ledger

Use the Pay Code Options window to configure pay codes to be included in the
payroll hour accruals. To open this window, click the **HR and Payroll**
series button, click **Pay Code** on the Setup content pane and then click
**Pay Code Options** from the GoTo menu. The Pay Code Options window
includes functionality for Payroll Extensions and for Advanced Payroll. The
functionality specific to Advanced Payroll is discussed here.

The only field that affects Post Hours To General Ledger is the checkbox
option “Do Not Post Hours.”

#### Do Not Post Hours

- When the field is not selected, there will be an automatic post of payroll
    transaction hours for this pay code to the General Ledger unit account set
    up in the modified Payroll Posting Accounts Setup window.

- When this field is selected, the payroll transaction hours will not be
    posted to the General Ledger unit account.

### Labor Accrual Manager Essentials

Labor Accrual Manager is designed specifically to fulfill the need of
companies that must prepare accrual and reversing entries for payroll. Once
per month, near or shortly after the end of a month, accounting personnel
must create payroll accruals for accurate financial reporting. Labor Accrual
Manager automates the generation of accrual and reversing entries that need
to be posted to the General Ledger.

The features and capabilities of Labor Accrual Manager include:

- Allows payroll accruals to be created based on the calculated accrual days,
    which can be entered as a decimal value.

- Accounts for labor liability, allowing for accurate financial reporting.

- Payroll accruals can be posted directly through the General Ledger.

    - A Gross Wages journal entry will be created for each unique General
        Ledger Account.

    - An Hour’s journal entry will be created for each unique General Ledger
        Unit Account.

- Contains functionality allowing a reversing date for the payroll accrual
    posting to be specified.

- Allows batches to accrue based on Posted Date or Pay Period End Date to be
    viewed.

- Includes a report that will display journal entries and distribution records
    that will be created upon posting the payroll accruals.

Labor Accrual Manager works in conjunction with another product, Post

Payroll Hours to General Ledger. When the Post Payroll Hours to General
Ledger is installed and registered, the payroll hours will be posted to the

General Ledger and will then be available for use during the Labor Accrual
Manager Payroll Accruals to generate hour accrual journal entries.

Labor Accrual Manager is NOT an Inter-company application. Processing only
looks at payroll General Ledger data for the Company that is currently open.

### Payroll Accrual Example

In the example shown below, our accounting period is the month of April. All
pay runs with a posting date in April show up in the scrolling window.

The Pay Frequency of “Biweekly” has been entered indicating that payroll is
processed every other week. Any accruals posted to General Ledger in this
window will be automatically reversed on 5/2/2017.

![A screenshot ](media/1859a5d77be20b8a7241e4ea2624640f.jpg)

Two pay runs are marked in the scrolling window above. When the Calculate
button is selected, the Total Gross Wages are equal to sum of the Gross
Wages of the two marked pay runs.

Enter the number of days to accrue in the Calculated Accrual Days. Upon
tabbing off the Calculated Accrual Days field or selecting the Calculate
button, both the Total Gross Wages and the Calculated Accrual Percent are
updated.

The Calculated Accrual Percent is the Calculated Accrual Days divided by the
number of days in the Pay Frequency selected and multiply by 100. In this
example it would be (5.00 / 14.00) \*100 = 35.72%.

### Setting up Payroll Posting Accounts for Labor Accrual Manager

To open the Payroll Posting Setup window, click the **Administration**
series button, click **Posting** in the Setup content pane and then click
**Payroll Accounts.**

Labor Accrual Manager works in conjunction with another product, Post
Payroll Hours to General Ledger. The modified Payroll Posting Accounts Setup
window has been modified to include the Unit Account.

When the Post Payroll Hours to General Ledger is installed and registered,
the payroll hours will be posted to the General Ledger and will then be
available for use during the Labor Accrual Manager Payroll Accruals to
generate hour accrual journal entries.

When the Post Payroll Hours to General Ledger is not installed, only dollars
will be available for use during the Labor Accrual Manager Payroll Accruals
to generate dollar accrual journal entries.

### Setting up Labor Accrual Accounts for Labor Accrual Manager

To open the Labor Accrual Accounts Setup window, click the **HR and
Payroll** series button, click **Payroll** on the Setup content pane, and
click **Labor Accrual Accounts.**

![A screenshot ](media/48e1813c069cc3809e85f08cf7e45bcb.jpg)

The Labor Accrual Accounts window displays all General Ledger Posting
Accounts currently assigned in the Payroll Posting Accounts Setup window for
all Posting Account Types. When the Accrue checkbox is checked, then the
Account in that row will accrue dollars for payroll accruals.

### Labor Accrual Accounts Setup

Select the **Posting Account Type.** Options include:

- Gross Pay

- Federal Tax Withholding

- State Tax Withholding

- Local Tax Withholding

- Deduction Withholding

- Employer's Tax Expense

- Benefits Expense

- Benefits Payable

- Taxable Benefits Expense

- Taxable Benefits Payable

- SUTA Payable

- FUTA Payable

- W/Comp Tax Expense

- W/Comp Tax Payable

##### Accrue

Select the checkbox when that account is to accrue dollars for payroll
accruals.

##### Account Number

Displays all General Ledger Posting Accounts currently assigned in the
Payroll Posting Accounts Setup window for all Posting Account Types.

It is required that at least one Dynamics GP Payroll Posting Account row be
set up (Department, Position, Code, Account) in the Payroll Posting Accounts
Setup window.

**Description**

Description of displayed account number.

### Setting up Pay Code Options for Labor Accrual Manager

Use the Pay Code Options window to configure pay codes to be included in the
payroll hours that are posted to the General Ledger. To open this window,
click the **HR and Payroll** series button, click **Pay Code** on the Setup
content pane and then click **Pay Code Options** from the GoTo menu. The Pay
Code Options window includes functionality for Payroll Extensions and for
Advanced Payroll. The functionality specific to Advanced Payroll is
discussed here.

The only field that affects Labor Accrual Manager is the checkbox option
“Exclude Hours from Payroll Accruals.”

#### Exclude Hours from Payroll Accruals

- When the field is not selected, Labor Accrual Manager will automatically
    include any transaction hours for this pay code in the payroll hour’s
    accruals.

- When this field is selected, these transactions hours will **NOT** be
    included in the payroll hours accruals.

- The “Exclude Hours from Payroll Accruals” has no impact on the accrue
    dollars for payroll accruals, only hours.

### Advanced Labor Reporting Essentials

Advanced Labor Reporting extends department level reporting for both

Payroll and Financial data. It also extends reporting for Full-Time
Equivalent data as well as Productive and Non-Productive employee level
data, Full-Time Equivalent Budgets and variances, current and Year to Date
totals are just a few of the report features available.

The features and capabilities of Advanced Labor Reporting include:

- Set up Areas of Responsibility for multiple levels for reporting.

- Set up Report Options for all reports by “current” and “previous” periods to
    enable faster repeat and batch printing.

- Select criteria for each report to drill down on a specific set of data or
    print all for a specified date range.

- Print reports to the screen, printer or file.

- Print Benefit Accrual Report with expanded vacation and sick, pending, taken
    and available information.

- Print Department Analysis Detail Report to view pay code level

Hours, Full-Time Equivalent and Earnings for pay periods and Year to Date.
Total Groupings are provided by employee, position, General Ledger Account
(based on main segment) and Department.

- Print Department Summary Report to view department total Productive,
    Non-Productive and overall total Hours, Full-Time Equivalent and Earnings.

- Print Employee Analysis Report to view employee pay code level Hours,
    Full-Time Equivalent and Earnings for pay periods and Year to Date.

- Print Full-Time Equivalent Year to Date Report to view financial department
    total Productive and Non-Productive Hours and Full-Time Equivalent as well
    as overall total Hours, Full-Time Equivalent, Earnings, Full-Time Equivalent
    Budgets and Budget variances.

### Setting up Labor Reporting Accounts for Advanced Labor Reporting

To open the Labor Reporting Accounts window, click the **HR and Payroll**
series button, click **Payroll** on the Setup content pane, click **Advanced
Labor Reporting** and then click **Labor Reporting Accounts**.

![A screenshot](media/1496d6c0f31bccc37099c5590b1b3092.jpg)

The Labor Accrual Accounts window displays all General Ledger Unit Accounts
currently assigned in the Payroll Posting Accounts Setup window for Gross
Pay Posting Account Types.

#### Labor Reporting Code

- The system will allow the user to assign a Labor Reporting Code to each
    listed Unit Account: o None, o Productive or o Non-Productive.

- The FTE YTD Report uses the Labor Reporting Code from this window and pulls
    data from the General Ledger.

### Setting up Areas of Responsibility for Advanced Labor Reporting

To open the Area of Responsibility Setup window, click the **HR and**

**Payroll** series button, click **Payroll** on the Setup content pane,
click

**Advanced Labor Reporting** and then click **Areas of Responsibility**.

![A screenshot](media/7977806af2f0ec351776e5cb71069fb1.jpg)

Area of Responsibility Setup is an option available with Advanced Labor
Reporting that enables groupings of departments to be created as they relate
to specific areas of responsibility. An example of this would be a Vice
President that oversees multiple departments or several managers.

### Areas of Responsibility

##### Area of Responsibility Code

Enter a Code that represents specific areas of responsibility and levels of
responsibility. An example would be a VP could represent a Vice President
that is responsible for Accounting, Administration and Sales.

##### Description

Enter a description that describes the area of responsibility code that is
being created. An example would be a Vice President.

##### Responsible Person

Select the employee that is responsible for the area or level of
responsibility. Create the Area of Responsibility specific to the “area” and
not specific to an employee.

##### Available Departments

This field displays all departments that are not currently assigned to this
Area of Responsibility.

##### Selected Departments

This field displays all departments that have been selected as assigned to
this Area of Responsibility.

A department can be assigned to multiple areas of responsibility. Multiple
layers of responsibility can be created, for example Vice President and
Department Manager, can generate reports to include all departments for that
specific area of responsibility.

### Setting up Payroll Account Mapping for Advanced Labor Reporting

To open the Payroll Account Mapping window, click the **HR and Payroll**
series button, click **Payroll** on the Setup content pane, click **Advanced
Labor Reporting** and then click **Account Mapping.**

The Payroll Account Mapping window is provided to allow a link between a
payroll department and a General Ledger Account segment to be established.
This option is required for printing the Full-Time Equivalent Year to Date
Report restricted by Area or Responsibility. It provides the route back for
the General Ledger Accounts to the payroll accounts assigned to a specific
Area of Responsibility.

### Payroll Account Mapping

##### Account Segment

The account segment that represents the relationship between the General
Ledger Accounts and the Payroll Departments must be chosen.

**Department**

The Department column will display all available Payroll Departments.

##### Account Segment Value

Using the Lookup option or keying in the value, assign the correct segment
value for the selected Account Segment that is associated to the payroll
department in each row.

### Setting up Pay Code Options for Advanced Labor Reporting

Use the Pay Code Options window to configure pay code settings to be
included that impact the Full-Time Equivalent Calculation on the Department
Detail, Department Summary and Employee Analysis Reports. To open this
window, click the **HR and Payroll** series button, click **Pay Code** on
the Setup content pane and then click **Pay Code Options** from the GoTo
menu. The Pay Code Options window includes functionality for Payroll
Extensions and for Advanced Payroll. The functionality specific to Advanced
Payroll is discussed here.

#### Calculate Full-Time Equivalent for this Pay Code

The “Calculate Full-Time Equivalent for this Pay Code” option must be
selected for Full-Time Equivalent to be calculated and displayed for those
Pay Code totals and/or included in Department Total Full-Time Equivalent.

#### Labor Reporting Code

The Department Summary Report uses the Labor reporting code from Pay code
options window. The Productive / Non Productive columns on this report come
from the Labor reporting code from Pay code options window. The data is
pulled from Payroll History, not the General Ledger.

The available selections are:

- None,

- Productive or

- Non-Productive.

### Advanced Labor Reporting FTE Calculation

The Full-Time Equivalent Calculation uses the Frequency selected for the
report to calculate the Full-Time Equivalent. The total number of hours for
that report row is divided by the hours associated with the frequency
selected. Frequency and Associated Hours:

| **Frequency** | **Associated Hours** |
|---------------|----------------------|
| Weekly        | 40                   |
| Bi-weekly     | 80                   |
| Semimonthly   | 86.67                |
| Monthly       | 173.33               |
| Quarterly     | 520                  |
| Semiannually  | 1040                 |
| Annually      | 2080                 |

**FTE Calculations for Financial Report - FTE YTD**

The FTE Calculations formula and examples follow:

- The 5.6986 factor =\> 1 FTE = 2080 hours worked per year / 365 days in a year.

- System will calculate the (total hours) divided by (number of days included in the selected period (counting Feb 29 when appropriate) x 5.6986) = FTE for report.

- **Example:** (173.33 hours) divided by (31 days x 5.6986 = 176.6575) = .981 FTE.

- **Example:** (173.33 hours) divided by (30 days x 5.6986 = 176.6575) = 1.014 FTE.

### Summary

This chapter focused on using Advanced Payroll to set up add-on codes to
adjust pay rates and to analyze hypothetical pay policy options and view
their impact on the Adjusted Pay Rate. It also explained how to set up the
system to post actual labor hours to General Ledger Unit Accounts. The
course also explained how to fulfill the need of companies that are required
to account for payroll accruals within a month that are not accounted for
when the pay period ends prior to the end of that month. Advanced Labor
Reporting extends department level reporting for both Payroll and Financial
data.

Some key points to remember from this chapter include:

- When entering transactions through the Transaction Entry window the Pay Rate
    is adjusted based on the Employee, Employee Pay Code, Company, Department,
    Position and Shift Code selected, or the linked pay code selections on the
    Employee Pay Code Options window.

#### Objectives

The objectives are:

- Enter employee pay policies.

- Enter Employee Transaction Auto Splits.

### Pay Policy Manager

>   For any Adjusted Pay Rates to calculate the Employee level must be correctly
>   set up. Using Employee Maintenance and Employee Pay Policy Exceptions
>   options, a variety of Adjusted Pay Rate calculations can be maintained.

### Pay Policy Manager - Employee Maintenance

>   Pay Policy Manager automates the advanced rate calculation process by
>   allowing administration of all standard and overtime policies for hourly
>   employees working in multiple departments and positions with a variety of
>   base pay rates, shift differentials and pay rate add-on amounts.

### Adjusted Pay Rates

>   An Adjusted Pay Rate is a Pay Code Pay Rate modified by the Pay Policy
>   Manger. Pay Policy Manager handles modifying Pay Rates by several different
>   options.

##### Option 1

>   Assigning Add-On Codes which includes an Amount (% or \$) that will be
>   applied to the Employee’s base Pay Code Pay Rate when creating payroll
>   transactions. Example: Employee’s hourly Pay Code Pay Rate of \$10.00 with
>   an Add-On Amount of \$1.00. All transactions for this Employee would be
>   calculated at a rate of \$11.00.

##### Option 2

>   Linking a pay code to an hour based pay code to inherit that pay codes pay
>   policy and pay policy exceptions. Example: Employee’s Vacation Pay Code that
>   uses the same Pay Policy as the Employee’s hourly Pay Code.

##### Option 3

>   Linking a pay code to an hour based pay code and setting a Percent. Example:
>   A pay code that tracks differential hours, where the rate of pay is always a
>   set percentage of the adjusted pay rate.

##### Option 4

>   Forced minimum pay rates to verify that the employee’s pay rate is never
>   less than that rate.

### Employee Pay Code Options

>   Use the Employee Pay Code Options window to designate a “Linked Pay Code” or
>   an Add-On code. To open this window, click the **HR and Payroll** series
>   button, click **Payroll** on the Cards content pane, and then click on **Pay
>   Code**. Select an **Employee ID**, select a **Pay Code** and then click
>   **Employee Pay Code Options** from the GoTo menu.

>   When a linked pay code is assigned, then the system will disable the “Use
>   Add-On” options.

-   Only a pay code that is hourly based can be linked to another hourly-based
    code.

-   The system will use the add-ons of the linked pay code.

>   After a linked pay code is entered, the Pay Percent and Minimum Amount
>   fields will become enabled.

-   A percent of the linked pay code rate can be entered when not using the full
    100%.

-   A minimum amount can be specified so that when the linked pay code and any
    add-on options do not exceed the minimum amount, the rate will automatically
    be adjusted up to the minimum amount.

>   The Pay Code Options window also allows an Add-On Code to be specified and
>   to specify if an employee is currently eligible for the adjusted pay rate.

-   When the Use Add-On option is selected and an Add-On Code is selected, this
    Add-On Code Amount will be applied to an eligible employee’s pay rate.

-   The values in this field will default from the Pay Code Options window for
    the pay code selected.

-   The default values are saved when SAVE on the Employee Pay Code Maintenance
    window is selected.

-   To change the defaults open this window, enter the selections, press OK and
    SAVE on the Employee Pay Code record.

>   The Pay Policy Priority Setup does not include the Employee Pay Code
>   calculation factor.

-   The Employee Pay Code Add-On is always applied as the first calculation.

-   That adjusted pay rate is then sent through the Pay Policy Priority
    adjustments following the priority set in the Pay Policy Priority Setup
    window.

>   Pay Policy Manager specific fields: Linked Pay Code, Pay Percent, Minimum
>   Amount, Use Add-On and Add-On Code. All other fields on this window are for
>   other Human Resources and Payroll Suite modules.

### Employee Maintenance

>   The existing Employee Maintenance window has been modified to allow the user
>   to specify when an employee is eligible for the Pay Code rate adjustments
>   defined. The Use Add-On checkbox must be selected for an employee’s rate to
>   pay rate adjustments to be calculated.

![A screenshot of a social media post Description automatically generated](media/10d43b370e55069491f108e962d29310.jpg)

### Use Add-On Employee’s

>   Use the Use Add-On Employee’s window to assign an add-on code. To open this
>   window, click the **HR and Payroll** series button, click **Payroll** on the
>   Cards content pane, click on **Employee** and then click **Use AddOn
>   Employee’s** from the Payroll GoTo menu.

>   The Use Add-On Employee’s window allows the user to assign an add-on code to
>   a single employee or to many employees. The user can display the employees
>   in the window based on a selected range. The Ranges option includes Employee
>   ID, Department, Position or Employee Class.

### Employee Class Assignment

>   Employee Pay Code Option records are created when an Employee Class is
>   assigned to an employee in the Employee Maintenance window and when “YES” is
>   answered to the “Do you want to use default information from the employee
>   class record?” message that appears when exiting the Class ID field.

### Employee Pay Policy Exceptions

>   The Employee Pay Policies Exceptions window is used to define exceptions for
>   a specific employee to calculate the employees Adjusted Pay Rate when adding
>   payroll transactions. To open this window, click the **HR and Payroll**
>   series button, click **Payroll** on the Cards content pane, and then click
>   **Pay Policies**.

![A screenshot of a cell phone Description automatically generated](media/0a40d3be32d5491e1636f612d457a794.jpg)

>   The Employee Pay Policy Exceptions window allows Add-On Rate adjustments to
>   be defined for an individual employee based on a combination of Company ID,
>   Department, Position and Shift Code.

>   Whenever the Pay Policies rate adjustments applied to each of these elements
>   does not satisfy the needs of a particular employee, specific adjustments
>   can be applied in this window. This option is intended to handle all
>   employee exceptions or deviations from the standard Pay Policies.

>   Any Employee Pay Policies Exceptions defined for an employee will be used in
>   the calculation instead of the normal Pay Policies calculations defined. In
>   addition to applying variations of the defined Pay Policies, assigning an
>   Employee Pay Policy Exception can include an Employee Adjustment.

>   **Employee ID**

>   Selecting the Employee enables the option of selecting a Pay Code.

##### Pay Code

>   Selecting an employee Pay Code opens all Employee Pay Policies Exceptions
>   currently assigned to that employee Pay Code and enables the functionality
>   of the Employee Pay Policies Exception window.

-   At this time, a Hypothetical Pay Code Rate and/or a Hypothetical Pay Code
    Add-On option can be entered.

-   When combined with the Calculate By option discussed below, the Actual and

- During the calculation process, when Add-On Codes are assigned to various
    calculation factors the calculations occur in order based on the Pay Policy
    Priority Setup.

- An employee can have a transaction with any combination of five calculation
    factors.

- The values entered into the Hypothetical fields do not update the actual
    values saved in the Pay Code table.

- Payroll Hours to General Ledger will allow the system to be set up to post
    actual labor hours to General Ledger Unit Accounts.

- When the “Do Not Post Hours” is selected, the payroll transaction hours will
    not be posted to the General Ledger unit account.

- Labor Accrual Manager allows batches to accrue on based on Posted Date or
    Pay Period End Date to be viewed.

- When the Post Payroll Hours to General Ledger is not installed, only dollars
    will be available for use during the Labor Accrual Manager Payroll Accruals
    to generate dollar accrual journal entries.

- The “Exclude Hours from Payroll Accruals” has no impact on the accrue
    dollars for payroll accruals, only hours.

- Advanced Labor Reporting extends department level reporting for both Payroll
    and Financial data.

- The FTE YTD Report uses the Labor Reporting Code from the Labor Reporting
    Accounts window and pulls data from the General Ledger.

- A department can be assigned to multiple areas of responsibility.

- The Payroll Account Mapping window provides the route back for the General
    Ledger Accounts to the payroll accounts assigned to a specific Area of
    Responsibility.

## CHAPTER 2: ADVANCED PAYROLL EMPLOYEE MAINTENANCE

The objectives are:

- Enter employee pay policies.

- Enter Employee Transaction Auto Splits.

### Pay Policy Manager

For any Adjusted Pay Rates to calculate the Employee level must be correctly
set up. Using Employee Maintenance and Employee Pay Policy Exceptions
options, a variety of Adjusted Pay Rate calculations can be maintained.

#### Pay Policy Manager - Employee Maintenance

Pay Policy Manager automates the advanced rate calculation process by
allowing administration of all standard and overtime policies for hourly
employees working in multiple departments and positions with a variety of
base pay rates, shift differentials and pay rate add-on amounts.

### Adjusted Pay Rates

An Adjusted Pay Rate is a Pay Code Pay Rate modified by the Pay Policy
Manger. Pay Policy Manager handles modifying Pay Rates by several different
options.

##### Option 1

Assigning Add-On Codes which includes an Amount (% or \$) that will be
applied to the Employee’s base Pay Code Pay Rate when creating payroll
transactions. Example: Employee’s hourly Pay Code Pay Rate of \$10.00 with
an Add-On Amount of \$1.00. All transactions for this Employee would be
calculated at a rate of \$11.00.

##### Option 2

Linking a pay code to an hour based pay code to inherit that pay codes pay
policy and pay policy exceptions. Example: Employee’s Vacation Pay Code that
uses the same Pay Policy as the Employee’s hourly Pay Code.

##### Option 3

Linking a pay code to an hour based pay code and setting a Percent. Example:
A pay code that tracks differential hours, where the rate of pay is always a
set percentage of the adjusted pay rate.

##### Option 4

Forced minimum pay rates to verify that the employee’s pay rate is never
less than that rate.

### Employee Pay Code Options

Use the Employee Pay Code Options window to designate a “Linked Pay Code” or
an Add-On code. To open this window, click the **HR and Payroll** series
button, click **Payroll** on the Cards content pane, and then click on **Pay
Code**. Select an **Employee ID**, select a **Pay Code** and then click
**Employee Pay Code Options** from the GoTo menu.

When a linked pay code is assigned, then the system will disable the “Use
Add-On” options.

- Only a pay code that is hourly based can be linked to another hourly-based
    code.

- The system will use the add-ons of the linked pay code.

After a linked pay code is entered, the Pay Percent and Minimum Amount
fields will become enabled.

- A percent of the linked pay code rate can be entered when not using the full
    100%.

- A minimum amount can be specified so that when the linked pay code and any
    add-on options do not exceed the minimum amount, the rate will automatically
    be adjusted up to the minimum amount.

The Pay Code Options window also allows an Add-On Code to be specified and
to specify if an employee is currently eligible for the adjusted pay rate.

- When the Use Add-On option is selected and an Add-On Code is selected, this
    Add-On Code Amount will be applied to an eligible employee’s pay rate.

- The values in this field will default from the Pay Code Options window for
    the pay code selected.

- The default values are saved when SAVE on the Employee Pay Code Maintenance
    window is selected.

- To change the defaults open this window, enter the selections, press OK and
    SAVE on the Employee Pay Code record.

The Pay Policy Priority Setup does not include the Employee Pay Code
calculation factor.

- The Employee Pay Code Add-On is always applied as the first calculation.

- That adjusted pay rate is then sent through the Pay Policy Priority
    adjustments following the priority set in the Pay Policy Priority Setup
    window.

Pay Policy Manager specific fields: Linked Pay Code, Pay Percent, Minimum
Amount, Use Add-On and Add-On Code. All other fields on this window are for
other Human Resources and Payroll Suite modules.

### Employee Maintenance

The existing Employee Maintenance window has been modified to allow the user
to specify when an employee is eligible for the Pay Code rate adjustments
defined. The Use Add-On checkbox must be selected for an employee’s rate to
pay rate adjustments to be calculated.

![A screenshot](media/10d43b370e55069491f108e962d29310.jpg)

### Use Add-On Employee’s

Use the Use Add-On Employee’s window to assign an add-on code. To open this
window, click the **HR and Payroll** series button, click **Payroll** on the
Cards content pane, click on **Employee** and then click **Use AddOn
Employee’s** from the Payroll GoTo menu.

The Use Add-On Employee’s window allows the user to assign an add-on code to
a single employee or to many employees. The user can display the employees
in the window based on a selected range. The Ranges option includes Employee
ID, Department, Position or Employee Class.

### Employee Class Assignment

Employee Pay Code Option records are created when an Employee Class is
assigned to an employee in the Employee Maintenance window and when “YES” is
answered to the “Do you want to use default information from the employee
class record?” message that appears when exiting the Class ID field.

### Employee Pay Policy Exceptions

The Employee Pay Policies Exceptions window is used to define exceptions for
a specific employee to calculate the employees Adjusted Pay Rate when adding
payroll transactions. To open this window, click the **HR and Payroll**
series button, click **Payroll** on the Cards content pane, and then click
**Pay Policies**.

![A screenshot ](media/0a40d3be32d5491e1636f612d457a794.jpg)

The Employee Pay Policy Exceptions window allows Add-On Rate adjustments to
be defined for an individual employee based on a combination of Company ID,
Department, Position and Shift Code.

Whenever the Pay Policies rate adjustments applied to each of these elements
does not satisfy the needs of a particular employee, specific adjustments
can be applied in this window. This option is intended to handle all
employee exceptions or deviations from the standard Pay Policies.

Any Employee Pay Policies Exceptions defined for an employee will be used in
the calculation instead of the normal Pay Policies calculations defined. In
addition to applying variations of the defined Pay Policies, assigning an
Employee Pay Policy Exception can include an Employee Adjustment.

**Employee ID**

Selecting the Employee enables the option of selecting a Pay Code.

##### Pay Code

Selecting an employee Pay Code opens all Employee Pay Policies Exceptions
currently assigned to that employee Pay Code and enables the functionality
of the Employee Pay Policies Exception window.

- At this time, a Hypothetical Pay Code Rate and/or a Hypothetical Pay Code
    Add-On option can be entered.

- When combined with the Calculate By option discussed below, the Actual and
    Hypothetical values will calculate down to affect the Adjusted Pay Rate
    value for every Employee Pay Policy Exception defined in the scrolling
    window.

- The values entered into the Hypothetical fields do not update the actual
    values saved in the Pay Code table. When a Hypothetical pay rate adjustment
    is desired for use, the appropriate pay code information must be updated on
    the pay code window and will affect all actual Pay Code Pay Policies.

### Actual Calculations or Hypothetical Calculations

##### Actual Calculations

- When the Actual Calculations option is selected, the amounts displayed in
    the scrolling window represent the most current actual data that exists.

- In a case where an Employee Pay Policy Exception was created using Actual
    calculations, when that record is reopened, all calculations will
    automatically be re-figured based on the latest actual data available.

##### Hypothetical Calculations

- When the Hypothetical Calculations option is selected, the amounts displayed
    in the scrolling window represent the amounts saved in the Pay Policies
    table.

- Please note the values entered into the Hypothetical fields do not update
    the actual values saved in the Employee Pay Code table.

### Scrolling window

The scrolling window displays all defined Pay Policy Exceptions for the
Employee and employee Pay Code selected.

When any changes are made to an employee, pay policy exception record the
Adjusted Rate field will be recalculated. In calculating the Adjusted Rate,
the system will round to two decimal places.

##### Employee Adjustment, Amount and Adjusted Rate fields (the first two columns in the scrolling window)

- When selections are made in the Employee Adjustment or Amount fields the %
    or \$ (positive or negative) amount will be applied to the pay policy
    calculation after the Employee Pay Code adjustment and before the Company,
    Department, Position or Shift Add-On Amounts.

- This option gives greater flexibility in defining an employee pay policy
    exception.

- Example: A particular employee may not be eligible for the Add-On Codes but
    is allowed a \$1.00 increase for working within that pay policy. An Employee
    Adjustment of Amount would be selected and enter \$1.00 into the Amount
    field. Next deselect the Company, Department, Position and Shift columns for
    that employee pay policy exception record.

When only the Employee Adjustment, Amount or Percent defines the employee
pay policy exception with no Add-On Codes applied, “ALL” must be assigned to
any Company, Department, Position or Shift Code fields for that row that are
not set to a specific value for the adjusted rate to be correctly applied at
the Transaction Entry window.

Adjusted Rate will not display if Pay Policy includes an ALL selection.

##### Employee Pay Policy Exceptions Combinations

Any combination of Pay Policy Exceptions can be created for this employee
and pay code. When all companies, departments, positions or shifts apply to
that particular pay policy exception enter ALL in that field (See \*Adjusted
Rate).

This window may not display all possible pay policy exceptions for this
employee and employee pay code.

### Pay Policy Priority

The Pay Policy Priority settings available in the Pay Policy Manager module
have previously been discussed.

The column order in the scrolling window of the Pay Policies window reflects
the current order set in the Pay Policy Priority Setup window.

A change made to the Pay Policy Priority Setup will trigger recalculations
of any Actual Adjusted Pay Rates.

When selections are made in the Employee Adjustment or Amount fields the %
or \$ (positive or negative) amount will be applied to the pay policy
calculation after the Employee Pay Code adjustment and before the Company,
Department, Position or Shift Add-On Amounts. This option gives greater
flexibility in defining an employee pay policy exception.

**Example:** A particular employee may not be eligible for the Add-On Codes
but is allowed a \$1.00 increase for working within that pay policy. An
Employee Adjustment of Amount would be selected and enter \$1.00 into the
Amount field. The Company, Department, Position and Shift columns for that
employee pay policy exception record could be deselected.

When only the Employee Adjustment, Amount or Percent defines the employee
pay policy exception with no Add-On Codes applied, “ALL” must be assigned to
any Company, Department, Position or Shift Code fields for that row that are
not set to a specific value for the adjusted rate to be correctly applied at
the Transaction Entry window.

##### Adjusted Rate

Adjusted Rate will not display if Pay Policy includes an ALL selection.

Any combination of Pay Policy Exceptions can be created for this employee
and pay code. If all companies, departments, positions or shifts apply to
that particular pay policy exception enter ALL in that field.

Please note this window may not display all possible pay policy exceptions
for this employee and employee pay code.

### Employee Transaction Auto Split Setup

Transaction auto-split allows additional flexibility and functionality when
applying payroll transactions for employees that work for and in multiple
departments and positions. To open this window, click the **HR and Payroll**
series button, click **Payroll** on the Cards content pane and then click
**Transaction Auto-Split**.

The employee setup window allows the employee and position whose transaction
hours need to be split between more than one department to be selected when
processing payroll and posting payroll to the General Ledger.

The Transaction Auto-Split functionality will take the original payroll
transaction from the batch and during the payroll Build process, remove it
and replace it with new transactions based on the transaction auto-split set
up for that employee and position.

Any employee and position payroll transaction where the department is listed
in the setup will be split into the appropriate new transactions based on
the transaction auto-split set up for that employee and position.

**Employee ID**

Select the employee that you wish to set up a transaction auto-split for.

**Position Code**

Select the position for which a transaction auto-split is to be set up.

#### Department

Enter the department whose transactions should be split and the departments
that these split transactions will be applied to.

#### Percent

Enter the percent of the transaction hours that should be applied to this
department.

#### Total Percent

The total of all department percents entered must equal 100.00%. If the
total does not equal 100%, the record will not be saved.

### Summary

This chapter focused on using Pay Policy Manager to automate the advanced
rate calculation process by allowing administration of all standard and
overtime policies for hourly employees working in multiple departments and
positions with a variety of base pay rates, shift differentials and pay rate
add-on amounts. It also focused on entering employee pay policies and
entering Employee Transaction Auto Splits.

Some key points to remember from this chapter include:

- When a linked pay code is assigned on the Pay Code Options window, then the
    system will disable the “Use Add-On” options.

- When the Use Add-On option is selected and an Add-On Code is selected, this
    Add-On Code Amount will be applied to an eligible employee’s pay rate.

- Employee Pay Code Option records are created when an Employee Class is
    assigned to an employee.

- Any Employee Pay Policies Exceptions defined for an employee will be used in
    the calculation instead of the normal Pay Policies calculations defined.

- The column order in the scrolling window of the Pay Policies window reflects
    the current order set in the Pay Policy Priority Setup window.

- The Transaction Auto-Split functionality will take the original payroll
    transaction from the batch and during the payroll Build process, remove it
    and replace it with new transactions based on the transaction auto-split
    setup for that employee and position.

## CHAPTER 3: ADVANCED PAYROLL TRANSACTIONS

The objectives are:

- Enter transactions related to Pay Policy Manager.

- Enter a Labor Accrual Manager Transaction.

### Pay Policy Manager

When entering transactions through the Transaction Entry window the

Pay Rate is adjusted based on the Employee, Employee Pay Code, Company,
Department, Position and Shift Code selected, or the linked pay code
selections on the Employee Pay Code Options window. The Pay Rate calculated
is saved at the time the transaction is entered for use during that pay run.

#### Labor Accrual Manager

Labor Accrual Manager is designed specifically to fulfill the need of
companies that are required to account for payroll accruals within a month
that are not accounted for when the pay period ends prior to the end of that
month. Once per month, near or shortly after the end of a month, accounting
personnel must create payroll accruals for accurate financial reporting.
Labor Accrual Manager fulfills this need as it allows for the creation of
the payroll accruals and posting to the general ledger as well as setting a
reversing date to be reversed out of the general ledger.

**Pay Policy Manager Transactions**

Pay Policy Manager allows for transaction entry on the Transaction Entry
window and when Transaction Auto Splits are assigned to an employee, the
transactions are split when the criteria is satisfied.

### Payroll Transaction Entry

When a payroll transaction is entered in the Transaction Entry window and
Pay Policy Manager is installed, the Pay Rate is calculated based on the
Add-On Codes assigned. To open this window, click the **HR and Payroll**
series button, click **Payroll** on the Transactions content pane and then
click **Transaction Entry**.

The Adjusted Pay Rate calculation also factors in any Employee Pay

Policy Exceptions. Once focus has left the payroll transaction record the
Adjusted Pay Rate will be saved and will not be recalculated unless one of
the five Pay Policy Manager calculation factors for that payroll transaction
is changed. In calculating the Adjusted Rate, the numbers will be rounded to
two decimal places.

##### Calculate

The Calculate button has been added to the Payroll Transaction Entry window
that will allow the user to calculate pay rates. This means that when an
existing batch that contains transactions is opened, when Calculate is
pressed, any pay policies that have changed since the last calculate that
will affect the Pay Rate will be seen. The new rate will display in the pay
rate field when that field is enabled.

The expanded view of the scrolling window on the Transaction Entry window
allows viewing and the modification of the Pay Policy Manager calculation
factors. The Company option is only available when security is set to use
the Advanced Payroll Transaction Entry window. The Premium amount will be
added after the Advanced Pay Rate calculations have been completed.

### Payroll Mass Transaction Entry

Adding Payroll Transactions through the **Payroll Mass Transaction**

**Entry** window will not use the advanced payroll calculations unless this

Batch is opened in the Payroll Transaction Entry window or by selecting
“Transaction” from the Mass Entry window. When the Batch is not opened in
the Transaction Entry, the Pay Rates will be set to the Employee Pay Code
Pay Rate with no advanced payroll calculations.

### Recurring Batches

Consistent with Microsoft Dynamics GP functionality when a transaction is
entered into a recurring batch the Adjusted Pay Rate is calculated. From
that point forward, anytime that recurring batch is processed, the Pay Rate
remains the Adjusted Pay Rate that was calculated or entered at the time.

The only way to adjust a Pay Rate within a batch is to edit the transaction
amount or delete and re-add that transaction record.

Any existing payroll batches created before Pay Policy Manager has been
installed will need to be deleted and re-created or have the Pay Rates
manually adjusted to implement any Adjusted Pay Rates.

### Voiding a Transaction

When a payroll transaction is voided, the total dollar stored will be used.
When a new payroll transaction is created to replace the voided check, the
Pay Rate will be calculated based on the most current pay policy
information.

### Importing Transactions

When transactions are imported from an external time tracking system, when
the batch has been completed, open the batch and press “Calculate” to fully
apply Pay Policy Manager adjusted rates to all transaction rates.

### Auto-Split Transactions in Payroll Builds

The Auto-Split Transactions processing takes place during the Payroll Build
process. The original batch payroll transaction is removed and replaced with
the appropriate new payroll transactions based on the Transaction Auto-Split
Setup for the employee and position set up where the original payroll
transaction department has been assigned to that employee and position setup
record.

### Labor Accrual Manager Transactions

The Payroll Accruals window enables payroll accrual calculations and posting
to be entered. To open this window, click the **HR and Payroll** series
button, click **Payroll** on the Transactions content pane and then click
**Payroll Accruals**.

### Payroll Accruals Window

##### Date

When a date is entered in the Accounting Period End Date field and tab off,
the date will be changed to the last day of that month. At this point, the
scrolling window will display any pay runs where the posting date falls
within that month. The Pay Frequency values include the following:

- Weekly (= 7)

- Biweekly (= 14)

- Semimonthly (=15)

- Monthly (=30)

The Pay Frequency value will affect the Calculated Accrual Percent value.

##### Batch ID

Select the batch that needs to be included in the accrual entry that will be
posted to the General Ledger.

##### Reversing Date

Enter the date that the accrual entry will be reversed in the General
Ledger.

##### Accrued Wages Account

Enter the General Ledger account number that any imbalance debit /credit
amount will be applied to during the payroll accrual posting process. This
section of the Payroll Accruals window will display the pay runs that match
the selected View option.

- When **View = Posted Date** is selected, the pay runs listed will reflect
    all pay runs with posting dates that fall within the month, as defined in
    the Accounting Period End Date field.

- When **View = Pay Period End Date** is selected, the pay runs listed will
    reflect all pay runs that were processed with a Pay Period End Date, as
    defined on the Build window during payroll processing that falls within the
    month.

Only Pay Runs processed AFTER the Labor Accrual Manager product is installed will show up in the scrolling window section of this screen.

##### Total Gross Wages

The system will display the sum of Gross Wages from the selected pay run records.

**Calculated Accrual Days** Enter the Days to Accrue.

##### Calculated Accrual Percent

Will calculate the percent automatically using the following formula:
(Calculated Accrual Days / Pay Period Days) \* 100

It should be noted that the Pay Period Days is derived from the Pay Frequency selected in this window.

### Summary

This chapter focused on using Advanced Payroll to enter transactions related to Pay Policy Manager and the Labor Accrual Manager transactions for payroll accrual calculations and posting Some key points to remember from this chapter include:

- The Adjusted Pay Rate calculation also factors in any Employee Pay Policy
    Exceptions.

 Selecting the Calculate button on the Transaction Entry window will
    calculate Pay Policy pay rates.

-  hen the Payroll Mass Transaction Entry Batch is not opened in the
    Transaction Entry window the Pay Rates will be set to the Employee Pay Code
    Pay Rate with no pay policy calculations.

- The Auto-Split Transactions processing takes place during the Payroll Build
    process.

- The Pay Frequency value will affect the Calculated Accrual Percent value.

- Only Pay Runs processed AFTER the Labor Accrual Manager product is installed
    will show up in the scrolling window section of this screen.

## CHAPTER 4: ADVANCED LABOR REPORTING

The objectives are:

- Select report options.

- Print the Benefit Accrual Report.

- Print the Department Analysis Detail Report.

- Print the Department Analysis Summary Report.

- Print the Employee Analysis Report.

- Print the FTE YTD Report.

**Advanced Labor Reporting** extends department level reporting for both

Payroll and Financial data. It also extends reporting for Full-Time
Equivalent data as well as Productive and Non-Productive employee level
data. Additional reporting features include Full-Time Equivalent Budgets and
variances, current and YTD totals.

### Advanced Labor Reporting

To open the Department Report window, click the **HR and Payroll** series
button, click **Payroll** on the Reports content pane and then click
**Advanced Labor Reporting**.

The Department Reports window has the option to select a report, add or
modify Report Options for that report, and insert the report options into a
Print List for batch or repeat printing.

### Department Reports

##### Reports

The report dropdown option contains the complete list of Advanced Labor
Reports that are available.

- Benefit Accrual

- Department Analysis Detail

- Department Analysis Summary

- Employee Analysis

- FTE YTD

For more information on each of these reports, please see those sections of
the document.

**Options**

This field lists all created Options for the report currently selected.

##### Print List

This field lists all Options added to the Print List for batch or repeat
printing.

##### New

Select New to create a new Report Option for the report currently selected.

##### Modify

Select Modify to edit or delete an existing Report Option. One of the
Options must be selected before selecting the Modify button.

### Report Options

The Report Options window allows report options to be created for each of
the Reports available from the Department Reports window. Each report has
different setup options available to it. Each report and the options
specific to them are described in those sections of this document. This
section of the document describes general use and shared functionality
between all report options.

##### Include Inactive Employees

Select the checkbox when Inactive Employees are to be included. By default,
only Active Employees are included on the report.

##### Ranges

The Range options available vary for each report. Each of the Range options
have their related From and To options available by related lookup, dropdown
and/or entry options. Apply these range restrictions by selecting the Insert
button and remove a range restriction by selecting the restriction and the
Remove button.

All criteria must be met for a record to be included on the report.

##### Destination

The Destination option allows the selection of where the report is to be
printed. The print options available are Screen, Printer and File.

### Benefit Accrual Report

The Benefit Accrual Report provides expanded information on the employee’s
PTO time. To open the Department Report window, click the **HR and Payroll**
series button, click **Payroll** on the Reports content pane, click
**Advanced Labor Reporting**, select a **Benefit Accrual** from the drop
down list and then click **New**.

Expanded vacation and sick pending, taken and available information are
provided for the pay period and anniversary to date. Many options are
provided for restricting data printed on this report.

The Benefit Accrual Report is designed to work with data provided when

PTO Manager is in use. The Benefit Accrual Report requires PTO Manager to be
installed to collect all pieces of data. When PTO Manager is not being used,
some values on the report are not available.

#### Frequency

The frequency selected is used in comparison to the User Date to determine
the correct Current or Previous date range to print on the report. The
correct date range is based on the information entered in Microsoft Dynamics
GP menu \> Tools \> Setup \> Human Resources \> Attendance \> Accrual
Periods.

#### Ranges

The following ranges are available:

- **The Department Range** allows for a range of Departments to be included on
    the report to be assigned.

- **The Employee ID Range** allows for a range of Employees to be included on
    the report to be assigned.

- **The Area of Responsibility Range** allows for a range of Area of
    Responsibility Codes to be assigned; thereby assigning a non-sequential list
    of departments as assigned to that Area of Responsibility.

- **The Date Range** allows the following From/To Date options to be assigned:

o Start of Current Pay Period - End of Current Pay Period o Start of
Previous Pay Period - End of Previous Pay Period o Specific Date XX/XX/XXXX
- Specific Date XX/XX/XXXX

A Date range must be selected to print a report. All criteria must be met
for a record to be included on the report.

### Department Analysis Detail Report

The Department Analysis Summary Report provides a view of pay code level
Hours, Full-Time Equivalent and Earnings for pay periods and Year to Date.
To open the Department Report window, click the **HR and Payroll** series
button, click **Payroll** on the Reports content pane, click **Advanced
Labor Reporting**, select **Department Analysis Detail** from the drop down
list and then click **New**.

Total Groupings are provided by employee, position, General Ledger Account
(based on main segment) and Department. Many options are provided for
restricting data printed on this report.

**Transaction End Date; Fiscal Year/Calendar Year**

The selection of Fiscal Year or Calendar Year affects the Year to Date
totals printed on the report.

- **When the Fiscal Year is selected,** the Year to Date totals will include
    all transactions from the start of the Fiscal Year that the selected Date
    range End Date falls in.

- **When the Calendar Year is selected,** the Year to Date totals will include
    all transactions from the start of the Calendar Year that the selected Date
    range End Date falls in.

#### Frequency

The frequency selected is used in comparison to the User Date to determine
the correct Current or Previous date range to print on the report. The
correct date range is based on the information entered in Microsoft Dynamics
GP menu \> Tools \> Setup \> Human Resources \> Attendance \> Accrual
Periods. The frequency for this report is also used when calculating the
Full-Time Equivalent. Please refer to the Full-Time Equivalent Calculations
section of this document for more detailed information.

#### Ranges

The following ranges are available:

- **The Department Range** allows for a range of Departments to be included on
    the report to be assigned.

- **The Position Range** allows for a range of Positions to be included on the
    report to be assigned.

- **The Employee ID Range** allows for a range of Employees to be included on
    the report to be assigned.

- **The Area of Responsibility Range** allows for a range of Area of
    Responsibility Codes to be assigned; thereby assigning a non-sequential list
    of departments as assigned to that Area of Responsibility.

- **The Date Range** allows the following From/To Date options to be assigned:

o Start of Current Pay Period - End of Current Pay Period o Start of
Previous Pay Period - End of Previous Pay Period o Specific Date XX/XX/XXXX
- Specific Date XX/XX/XXXX

A Date range must be selected to print a report. All criteria must be met
for a record to be included on the report.

### Department Analysis Summary Report

The Department Analysis Summary Report provides a view of

Department Total Productive, Non-Productive and Overall Total Hours,
Full-Time Equivalent and Earnings. To open the Department Report window,
click the **HR and Payroll** series button, click **Payroll** on the Reports
content pane, click **Advanced Labor Reporting**, select a **Department
Analysis Summary** from the drop down list and then click **New**.

The labor reporting code columns (Productive / Non Productive) on the
Department Analysis Summary Report come from the Pay Code Options setup
window and the report pulls data from Payroll History, not General Ledger.

Many options are provided for restricting data printed on this report.

**Transaction End Date; Fiscal Year/Calendar Year:** The selection of Fiscal
Year or Calendar Year affects the Year to Date totals printed on the report.

- **When the Fiscal Year is selected**, the Year to Date totals will include
    all transactions from the start of the Fiscal Year that the selected Date
    range End Date falls in.

- **When the Calendar Year is selected**, the Year to Date totals will include
    all transactions from the start of the Calendar Year that the selected Date
    range End Date falls in.

**Frequency:** The frequency selected is used in comparison to the User Date
to determine the correct Current or Previous date range to print on the
report. The correct date range is based on the information entered in
Microsoft Dynamics GP menu \> Tools \> Setup \> Human Resources \>
Attendance \> Accrual Periods.

The frequency for Department Analysis Summary Report is also used when
calculating the Full-Time Equivalent. Please refer to the Full-Time
Equivalent Calculations section of this document for more detailed
information.

#### Ranges

The following ranges are available:

- **The Department Range** allows for a range of Departments to be included on
    the report to be assigned.

- **The Position Range** allows for a range of Positions to be included on the
    report to be assigned.

- **The Employee ID Range** allows for a range of Employees to be included on
    the report to be assigned.

- **The Area of Responsibility Range** allows for a range of Area of
    Responsibility Codes to be assigned; thereby assigning a non-sequential list
    of departments as assigned to that Area of Responsibility.

- **The Date Range** allows for the following From/To Date options to be
    assigned:

o Start of Current Pay Period - End of Current Pay Period o Start of
Previous Pay Period - End of Previous Pay Period o Specific Date XX/XX/XXXX
- Specific Date XX/XX/XXXX

A Date range must be selected to print a report. All criteria must be met
for a record to be included on the report.

### Employee Analysis Report

The Employee Analysis Report provides a view of employee pay code level
Hours, Full-Time Equivalent and Earnings for pay periods and Year to Date.
To open the Department Report window, click the **HR and Payroll** series
button, click **Payroll** on the Reports content pane, click **Advanced
Labor Reporting**, select an **Employee Analysis** from the drop down list
and then click **New**.

Many options are provided for restricting data printed on this report.

#### Transaction End Date; Fiscal Year/Calendar Year

The selection of Fiscal Year or Calendar Year affects the Year to Date
totals printed on the report.

- **When the Fiscal Year is selected**, the Year to Date totals will include
    all transactions from the start of the Fiscal Year that the selected Date
    range End Date falls in.

- **When the Calendar Year is selected**, the Year to Date totals will include
    all transactions from the start of the Calendar Year that the selected Date
    range End Date falls in.

**Frequency:** The frequency selected is used in comparison to the User Date
to determine the correct Current or Previous date range to print on the
report. The correct date range is based on the information entered in
Microsoft Dynamics GP menu \> Tools \> Setup \> Human Resources \>
Attendance \> Accrual Periods.

The frequency for this report is also used when calculating the Full-Time
Equivalent. Please refer to the Full-Time Equivalent Calculations section of
this document for more detailed information.

#### Ranges

The following ranges are available:

- **The Department Range** allows for a range of Departments to be included on
    the report to be assigned.

- **The Position Range** allows for a range of Positions to be included on the
    report to be assigned.

- **The Employee ID Range** allows for a range of Employees to be included on
    the report to be assigned.

- **The Area of Responsibility Range** allows for a range of Area of
    Responsibility Codes to be assigned; thereby assigning a non-sequential list
    of departments as assigned to that Area of Responsibility.

- **The Date Range** allows for the following From/To Date options to be
    assigned:

o Start of Current Pay Period - End of Current Pay Period o Start of
Previous Pay Period - End of Previous Pay Period o Specific Date XX/XX/XXXX
- Specific Date XX/XX/XXXX

A Date range must be selected to print a report. All criteria must be met
for a record to be included on the report.

### FTE YTD Report

The Full-Time Equivalent Year to Date Report provides a view of a
department’s total Productive and Non-Productive Hours and Full-Time
Equivalent, as well as overall total Hours, Full-Time Equivalent, Earnings,

Full-Time Equivalent Budgets and Budget variances. To open the

Department Report window, click the **HR and Payroll** series button, click
**Payroll** on the Reports content pane, click **Advanced Labor Reporting**,
select **FTE YTD** from the drop down list and then click **New**.

FTE YTD Report uses the Labor Reporting Code from the Labor

Reporting Accounts window and pulls data from General Ledger. The

Labor Accrual Accounts window displays all General Ledger Unit Accounts
currently assigned in the Payroll Posting Accounts Setup window for Gross
Pay Posting Account Types.

Many options are provided for restricting data printed on this report.

#### Year

Select the year for which to print period data. The system will default to
the current year based on your User Date.

#### Budget ID

Select the Budget ID to use in the Full-Time Equivalent Budget information
and Full-Time Equivalent Budget Variance calculation.

**Ranges:** The following ranges are available:

- **The Department Range** allows for a range of Departments to be included on
    the report to be assigned.

- **The Area of Responsibility Range** allows for a range of Area of
    Responsibility Codes to be assigned; thereby assigning a non-sequential list
    of departments as assigned to that Area of Responsibility.

- **The Year / Period Range** allows for the following From/To Date options
    from a specific Year to be assigned: o Beg of Period - End of Period o Beg
    of Previous Period - End of Previous Period o Period X - Period X

The period represented in these Date ranges relates to the Fiscal Periods
set in the Microsoft Dynamics GP menu \>Tools \> Setup \> Company \> Fiscal
Periods window for the Year selected.

A Date range must be selected to print a report. All criteria must be met
for a record to be included on the report.

### Summary

This chapter focused on using Advanced Labor Reporting that extends
department level reporting for both Payroll and Financial data. It also
extends reporting for Full-Time Equivalent data as well as Productive and
Non-Productive employee level data. Additional reporting features include
Full-Time Equivalent Budgets and variances, current and YTD totals.

Some key points to remember from this chapter include:

- The Benefit Accrual Report requires PTO Manager to be installed to collect
    all pieces of data. When PTO Manager is not being used, some values on the
    report are not available.

- The labor reporting code columns (Productive / Non Productive) on the
    Department Analysis Summary Report come from the Pay Code Options setup
    window and the report pulls data from Payroll History, not General Ledger.

- The frequency for Department Analysis Summary Report is also used when
    calculating the Full-Time Equivalent. Please refer to the Full-Time
    Equivalent Calculations section of this document for more detailed
    information.

- FTE YTD Report uses the Labor Reporting Code from the Labor Reporting Accounts window and pulls data from General Ledger.
