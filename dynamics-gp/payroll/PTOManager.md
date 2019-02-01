>   Microsoft Dynamics® GP **Paid Time Off Manager**

CHAPTER 1: PAID TIME OFF MANAGER OVERVIEW 
==========================================

Objectives 
-----------

>   The objectives are:

-   Examine how Paid Time Off Manager works with Microsoft Dynamics® GP Payroll to calculate vacation and sick time.

-   Review some of the features and benefits that are associated with using Microsoft Dynamics GP Paid Time Off Manager.

Introduction 
-------------

>   Welcome to Microsoft Dynamics GP Paid Time Off Manager (PTO Manager), an integral component of the financial management system.

>   Paid Time Off Manager automatically manages complex vacation and sick time policies. It helps to reduce overhead costs by reducing paperwork and the time required by the Payroll team to manage manual paid time off record keeping. Paid Time Off Manager also enables the staff to manage complex and changing payroll situations quickly and accurately, while offering better service to the employees.

How Paid Time Off Manager Works 
--------------------------------

>   Microsoft Dynamics GP Payroll and Human Resource users often need to calculate vacation and sick time (Earned Paid Leave) using a method different from the standard Microsoft Dynamics GP calculation. Because different companies also use different methods, Paid Time Off Manager for Microsoft Dynamics GP allows the calculations to be defined and set up by the user in an attempt to create one module to fit these varying calculation methods. The user now has the ability to assign a PTO Code to multiple employees who have similar or identical PTO configurations.

>   Paid Time Off Manager integrates with the Microsoft Dynamics GP Payroll module to provide a complete solution. When users process payroll in Microsoft Dynamics GP, Paid Time Off Manager calculates vacation and sick time during the calculate checks process. The updated vacation and sick time data is posted to employees’ records when the payroll checks are posted.

Features and Benefits 
----------------------

>   The features and capabilities of Paid Time Off Manager include:

-   **Increase productivity.** Perform calculations of accrued vacation and sick time automatically during the Calculate Checks process.

-   **Manage multiple plans.** Define an unlimited number of calculation formulas for accruing vacation and sick time, as well as special features for managing carryovers, waiting periods and maximums.

-   **Access real-time information.** Display updated vacation and sick time balances for the current pay period on the employee paycheck stub and in Self Service.

-   **Automate manual processes.** Set up PTO plans for defined groups,replacing time-consuming manual processes and making maintenance simple.

-   **Improve data accuracy.** Reduce data entry with defined PTO plans that are assigned to each employee based on defined factors.

-   **Streamline budgeting and forecasting process.** Deliver access to PTO information with standard reports and on-demand SmartList reports.

Summary 
--------

>   Paid Time Off Manager integrates with Microsoft Dynamics GP Payroll to provide a solution for sick and vacation schedules that are not easily handled within the core product.

>   Some key points to remember from this chapter include:

-   Paid Time Off Manager works with Microsoft Dynamics GP Payroll to accrue sick and vacation time.

-   Multiple paid time off calculations can be defined and set up by the organization.

-   Calculations of accrued vacation and sick time take place during the calculate checks process in Payroll.

-   Ability to assign a PTO Code to multiple employees who have similar or identical PTO configurations.

CHAPTER 2: SETTING UP PAID TIME OFF MANAGER 
============================================

Objectives 
-----------

>   The objectives are:

-   Grant Security to the Paid Time Off windows and reports.

-   Use Security Task Setup window to edit security tasks for the PTO Manager module.

-   Use Security Roles Setup window to edit security roles for the PTO Manager module.

-   Set the Paid Time Off Options to establish the hire date parameter and the year-end closing process.

-   Review the settings that must be in place for Paid Time Off Manager to work properly.

-   Examine the appropriate Microsoft Dynamics GP core settings that need to be in place for Paid Time Off Manager to function properly.

-   Set up a PTO code defining the accrual schedules based on organizational policies using ranges, calculation factor and maximums.

-   Set up an “any time” maximum amount that an employee can have accumulated and identify the difference between this amount and the maximums set within the accrual schedules.

Introduction 
-------------

>   Setting up Paid Time Off Manager involves granting access to the windows and reports, the process of creating Accrual Schedules and Maximum Schedules and selecting a Paid Time Off option. Each of these topics is discussed in this chapter.

Security Task Access 
---------------------

### Setting up a Security Task 

>   Use the Security Task Setup window to select a default PTO Manager security task or modify the default security task. To open this window, click the **Administration** series button, click **System** on the Setup content pane and then click **Security Tasks**.

1.  Select appropriate **Task ID**

2.  Select **Product** – **HRM Solutions Series**

3.  Select **Type** – **Windows**

4.  Select **Series** – **3rd Party**

5.  Select the following from the access list

    -   **Accrual Schedule Setup**

    -   **Accrual Schedules**

    -   **Employee PTO Maintenance**

    -   **Maximum Schedule Setup**

    -   **Maximum Schedules**

    -   **PTO Codes**

    -   **PTO Options**

    -   **PTO Reports**

    -   **PTO Setup**

    -   **PTO Utilities**

6.  Change **Type** – **Reports**

7.  Select **Series – 3rd Party**

8.  Select the following form the access list

    -   **Accrual Schedule List**

    -   **Employee PTO Code List**

    -   **Maximum Schedule List**

    -   **PTO Accrual Schedule Codes List**

    -   **PTO Accrue List**

    -   **PTO Liability Report**

Security Role Access 
---------------------

### Setting up a Security Role 

>   Use the Security Role Setup window to select a default security role or modify the default security role. To open this window, click the
>   **Administration** series button, click **System** on the Setup content pane and then click **Security Roles**.

Paid Time Off Manager Option 
-----------------------------

>   Paid Time Off Manager is set up for each individual company, and Paid Time Off Manager options must be selected for each company. When restoring a backup from one company into a new company, these options must be selected in the new company.

>   To open the PTO Options window, click the **HR and Payroll** series button, click **Payroll** on the Setup content pane, click **PTO Manager** and then click **PTO Options**.

![](media/PTOOP.jpg)


>   Use **Accruals for Employee Based On** to select which hire date the accruals are based on. These button options allow the user to select if he or she wants to base the employee accruals and waiting periods off of the employee **Hire Date** or **Adjusted Hire Date**. This selection affects all employees company-wide.

>   Select the **Year End Closing using PTO Utility** check box to process vacation and sick time maximums from the PTO Utilities window for Employee PTO Setup records that are not selected to Calculate on Anniversary Date. Do not select the **Year End Closing using PTO Utility** check box to process vacation and sick time maximums during Payroll Year-End Closing for Employee PTO Setup records that are not selected to Calculate on Anniversary Date.

Other Settings Affecting PTO Accruals 
--------------------------------------

>   To implement the functionality of PTO Manager, the following validations must be true.

>   On the Employee Maintenance window, the **Hire Date** must be a valid date and must be greater than 00/00/0000.

>   On the Employee Vacation-Sick Time Maintenance window, verify the following:

-   **Accrue Vacation** check box must be selected for vacation to accrue

-   **Based On: Hours Worked** must be selected for vacation to accrue

-   **Accrue Sick Time** check box must be select for sick time to accrue

-   **Based On: Hours Worked** must be selected for sick time to accrue

>   On the Employee Additional Information Maintenance window, the **Work Hours per Year** must be greater than zero.

>   On the Employee Pay Code Maintenance window, verify the following:

-   The accrual eligible pay codes must be assigned to the employee.

-   **Accrue - Vacation** check box must be selected for vacation to accrue for hours associated with this pay code.

-   **Accrue - Sick Time** check box must be selected for sick time to accrue for hours associated with this pay code.

Related Microsoft Dynamics GP Core Settings 
--------------------------------------------

>   Additional core Microsoft Dynamics GP settings affect or inter-relate to the PTO Manager options, features and functionality.

### Employee Pay Code Maintenance Window 

>   Users must select the appropriate check box on the Employee Pay Code Maintenance window for PTO Manager to accrue for vacation and/or sick time. To open this window, click the **HR and Payroll** series button, click **Payroll** on the Cards content pane and then click **Pay Code**.

### Pay Code Setup Window 

>   Users must select the appropriate check box on the Pay Code Setup window for PTO Manager to accrue for vacation and/or sick time. This must be done for each pay code that is to accrue time. To open this window, click the **HR and Payroll** series button, click **Payroll** on the Setup content pane and then click **Pay Code**.

![](media/PTOPCS.jpg)

### Employee Class Setup Window 

>   When working with employee classes, users must complete the appropriate check box and other information on the Employee Class Setup window for PTO Manager to accrue for vacation and/or sick time. To open this window, click the **HR and Payroll** series button, click **Payroll** on the Setup content pane and then click **Employee Class**.

Setting up PTO Codes 
---------------------

>   Use the PTO Setup window to create setup data to be inherited at the employee level. The system allows the user to save, recall and update multiple PTO Setup records. To open the PTO Setup window, click the **HR and Payroll** series button, click **Payroll** on the Setup content pane and then click **PTO Setup**.

![](media/PTOS.jpg)

Enter or select a **PTO Code**. Enter or select the **Vacation and/or Sick Accrual Schedules**.

>   Select the **Inactive** checkbox to inactivate the PTO Code. If the **Inactive** checkbox is marked, the system will process PTO time based on core Payroll setups.

Setting up Accrual Schedules 
-----------------------------

>   Use the Accrual Schedule Setup window to define multiple accrual schedules specific to the company and the accrual policies. Different schedules may represent different hour ranges and calculation factors.
>   *EXAMPLE: Accrued time may be calculated differently for part-time employees versus full-time employees; or employees hired before a specific date may have a higher calculation factor than those hired after the specified date.*

>   Users can create an unlimited variety of schedules. The schedules are implemented into the calculations when they are assigned to an employee on the Employee PTO Setup window. Assigning accrual schedules to an employee is explained further in the Employee PTO Setup window section.

>   To open the Accrual Schedule Setup window, click the **HR and Payroll** series button, click **Payroll** on the Setup content pane, click **PTO Manager** and then click **Accrual Schedules**.

![](media/ASS23.jpg)

Enter a **Schedule Code** and a **Schedule Description**.

### Range Based On 

>   Make a selection in the **Range Based On** field. Options include:

-   Hours Worked / Pay Period

-   Hours Worked / Year

-   Hours Worked Life to Date

-   Years Worked

>   Use calculation ranges to determine which calculation factor the system uses in figuring hours accrued. Ranges consist of a beginning and ending value that may represent hours worked or years worked for the calculation factor to be used, and a maximum number of hours that may be earned. From and To values cannot overlap.

>   Four methods of determining ranges and maximums can be used in any combination. However, if a user selects the Per Year - Fixed or Per Pay Period - Fixed method for calculating the maximum hours, he or she cannot enter data into the Maximum Hours column.

>   It is important to understand each Range Based On option and how it is used to select the proper type for the organization. The Range Based On selection tells the system what the **Range From** and **Range To** values in the scrolling window represent. When each employee’s paycheck is calculated, the system evaluates the data for the employee based on the range option selected and determines which range and calculation factor to use.

### Range Based On: Hours Worked/Pay Period 

>   Using this selection the Range From and Range To columns represent hours worked per pay period. All hours worked that are eligible for vacation and/or sick time calculations within the pay period are used to determine the range that the employee falls into. As shown in the figure, if the employee worked 13 hours during the pay period, then the calculation factor of 0.02910 is used.

![](media/ASSe017.jpg)


### Range Based On: Hours Worked/Year 

>   Using this selection the Range From and Range To columns represent hours worked per year. All hours worked that are eligible for vacation and/or sick time calculations within the current calendar year (plus all eligible hours for that pay period) are used to determine the calculation factor. As shown in the figure, if the employee has worked a total of 1,600 eligible hours in
>   the current year and has worked 80 eligible hours this pay period, the calculation factor of 0.00817 will be used.

>   Calculation factors are determined based on the organization’s pay schedules, standard hours worked for each pay period, and methods of determining earned hours.

![](media/ASS24.jpg)


### Range Based On: Hours Worked Life-to-Date 

>   Using this selection the Range From and Range To columns represent Hours Worked Life to Date. All hours worked that are eligible for vacation and/or sick time calculations (that have been worked since the employee started) are used to determine the calculation factor.

>   *NOTE: The total Hours Worked Life-to-Date is derived from the Life-To-Date Hours Worked fields on the Employee PTO Setup window (plus all eligible hours for that pay period).*

>   The following figure shows that if the employee has worked a total of 10,400 eligible hours since he or she was hired (equivalent to 5 years) and has worked 80 eligible hours this pay period, the calculation factor of 0.05769 must be used.

![](media/ASS22.jpg)

>   Calculation factors are determined based on the organization’s pay schedules, standard hours worked for each pay period, and methods of determining earned hours.

### Range Based On: Years Worked 

>   Using this selection the Range From and Range To columns represent years worked. The years worked are determined by the difference between the current date and hire date (or if it exists, adjusted hire date). The following figure shows that if the employee has worked a total of 11.5 years (based on the employee’s hire date), the calculation factor of 0.07692 will be used. In this example, the years worked are rounded to 11 years.

![](media/ASS23.jpg)


### Maximum Hours Based On 

>   Make a selection in the **Maximum Hours Based On** field. Options include:

-   Per Pay Period -Variable

-   Per Year - Fixed

-   Per Year - Variable

-   Per Pay Period - Fixed

### Maximum Hours Based On: Per Pay Period - Variable 

>   Employees may accrue a maximum number of hours for each pay period based on this calculation range. In the Years Worked example, the first range of years worked allows the employee to earn up to 3.08 hours in an 80 hour pay period (80 Hours \* Calculation Factor of 0.03845 = 3.08). If the employee had worked at the company for ten years, the employee can earn a maximum of 6.15 hours for the pay period.

![](media/ASS23.jpg)

### Maximum Hours Based On: Per Year - Fixed 

>   Employees may accrue a fixed maximum number of hours for each calendar year. However, rather than having the maximum depend on the range, the maximum is set regardless of which calculation range the employee falls into. The Per Year - Fixed option allows users to specify the number of hours for each year. An example can be that the employee may earn a total of 80 hours for
>   each year, regardless of how many actual hours were worked.

>   *NOTE: While an employee may have an annual maximum set, his or her total accrued time may be greater than the annual maximum due to rollover time.*

### Maximum Hours Based On: Per Year - Variable 

>   Employees may accrue a maximum number of hours for each year based on their calculation range. For example, the calculation ranges may represent hours worked / year. If the employee worked 1200 hours during the year, he or she will earn a maximum of 12.0 hours (1200 \* Calc Factor 0.008 = 12.0 hours).


### Maximum Hours Based On: Per Pay Period - Fixed 

>   Employees may accrue a fixed maximum number of hours for each pay period. However, rather than having the maximum depend on the range, the maximum is set regardless of which calculation range the employee falls into. The employee has a per pay period maximum of 4.0 hours regardless of how many hours he or she works in the pay period; everyone has the same maximum.

>   If a Fixed option is selected for Maximum Hours Based On, a Fixed Maximum Hours must be entered.

### Range From/To 

>   **From** - is not allowed to have a higher value than the Range To field. Set the criteria that these range fields are based on. If the schedule is assigned to an employee that has only worked 23.00 hours in the pay period, he or she is placed in the 20.00 - 29.99 range for that pay period. For this example, the employee’s accrual can change from one pay period to the next based on his or her “Hours Worked/Pay Period.”

>   **To** - is not allowed to have a lower value than the Range From field. Set the criteria that these range fields are based on. If the schedule below is assigned to an employee that has only worked 23.00 hours in the pay period, he or she is placed in the 20.00 - 29.99 range for that pay period. For this example, the employee’s accrual can change from one pay period to the next based on his or her “Hours Worked/Pay Period.”

### Calculation Factor 

>   Enter the **Calculation Factor.** The **Calculation Factor** is always multiplied by the employees hours worked in the pay period.

>   *NOTE: If the employees must earn a set amount each pay run or year, then enter 9.99999 for the calculation factor, and set the Maximum Hours field value to limit the amount to receive.*

**Determining Calculation Factors**

>   Calculation factors are determined based on the organization’s pay schedules, standard hours worked for each pay period, and methods of determining earned hours. In the previous examples, a bi-weekly pay period is used with a standard hours worked for each pay period of 80.  In the following window, the calculation factor is determined by simply dividing the Maximum Hours by the To hours worked in the range (0.50 / 19.99= 0.0250). If the employee works 19.99 hours, he or she earns 0.5 hours(19.99 \* 0.025).

![](media/ASS32.jpg)

>   The following window shows that the factor is figured by dividing the Maximum Hours per Pay Period by the 2080 (maximum regular time work hours for each year). If an employee consistently works 80 hours each pay period, and he or she has worked a total of 10,400 hours since starting, the factor of 0.05769 is used, and he or she earns 4.62 hours each pay period. Since the employee is paid biweekly, there are a total of 26 pay periods. If the employee earns 4.62 hours every pay period, at the end of the year, he or she has accumulated 120 hours of earned time.

![](media/ASS41.jpg)


### Maximum Hours 

>   Set criteria for the Maximum Hours field based on, Per Pay Period - Variable,

>   Per Pay Period - Fixed, Per Year - Variable, or Per Year - Fixed. For both of the Fixed selections, enter only one maximum for all of the calculation ranges entered in the scrolling window. For both of the Variable selections, enter a different maximum hours for each calculation range entered in the scrolling window.

Setting up an Accrual Waiting Period 
-------------------------------------

>   PTO Manager allows the employee to accrue time that is not available for immediate use. Waiting periods can be set as a one-time (introductory period) waiting period, or recurring period, based on the calendar year or by employee anniversary date. PTO Manager allows the employee anniversary date to be specified as the Hire Date or Adjusted Hire Date on the employee maintenance card.

>   Waiting periods are used to hold earned hours until a specified date. For example, the employee may begin earning hours immediately after being hired, but not have the hours available for use until he or she has worked 90 days. In this example, the waiting period expiration date is set to 90 days from the employee’s hire date. The earned hours are calculated when a paycheck is processed, but the system will not post the hours to the employee’s available vacation and sick time until the after the waiting period is over.

>   *NOTE: If this check is voided, the lump sum that showed as Accrued is removed and will no longer exist. The amounts need to be manually re-entered.*

**Waiting Period**

>   **Recurring -** Selecting this check box under Vacation or Sick Waiting Period indicates that the PTO Code selected has an annual waiting period. The system will set the Vacation or Sick Expires date for affected records to 01/01 of the next year calendar year based on the current user date.

>   **Based on Anniversary Date -** Selecting this check box is enabled only if the Recurring Waiting Period field is checked. Selecting the Based On Anniversary Date indicates that the employee selected has an annually recurring waiting period and the system will set the Vacation or Sick Expires date for affected records to 01/01 of the next calendar year based on the current user date.

>   **Expires -** If the Recurring Waiting Period or Based on Anniversary Date field is not selected, the Waiting Period Expires field is set to 00/00/0000.

>   If either the Recurring Waiting Period or Based On Anniversary Date fields are checked, the Waiting Period Expires field is set to either the first of the calendar year or the employee’s anniversary date. When the Waiting Period Expires date is passed, the time is made available to the employee, and the Waiting Period Expires date automatically resets to the first of the next calendar year or the employee’s next anniversary date. The resetting of the Waiting Period Expires date takes place during the first pay run after the expiration date.

Setting up Carry Over Maximum 
------------------------------

>   **Calculate on Anniversary Date -** Select this check box to reset the balance to zero on the Anniversary date if Allow Carry Over is not checked. If the Allow Carry Over check box is selected, it carries over up to the maximum allowed on the first payroll after the employees anniversary date.

>   **Allow Carry Over -** Each employee may be assigned a maximum number of accrued hours that can be carried over to the next year. For every employee that is selected, when the PTO Year End process is invoked, PTO Manager will verify that Available time is less than or equal to the Maximum Carry Over value. The employee forfeits any earned hours in excess of the maximum that has not been used.

Setting up Anytime Maximum 
---------------------------

Select an Anytime Maximum option. Choices are:

-   **Fixed -** indicates that the employee has a fixed amount of hours available to him or her at any point in time. When this option is selected, enter a maximum hour’s value in the Hours Allowed field.

-   **Variable -** indicates that the employee has a variable amount of hours available at any point in time. The variable amount is determined based on the Maximum Schedule Code assigned to this employee in the Schedule field.

>   The Maximum Hours field is available only when Fixed has been selected. Enter the maximum available anytime hours in this field to set the fixed maximum amount of hours the employee has available at any given time.

>   The **Schedule** field and **Schedule Lookup** button are only available when **Variable** is selected. This field allows the entry of a Maximum Schedule Code that is set up in the Maximum Schedule Setup window.

Setting up Maximum Schedules 
-----------------------------

>   The Maximum Schedule Setup window allows the user to create schedules for setting variable maximums. This feature of PTO Manager allows the user to set up variations for calculating the maximum amount of vacation or sick time an employee is allowed to have in his or her depository at any time.

>   *NOTE: This is not based on per year or annual; this is a maximum for any point in time.*

>   The maximum schedule is set up based on Years Worked. When calculating Years Worked in the accrual process, the system will first attempt to calculate elapsed time from the Adjusted Hire Date, and then from the Hire Date.

>   To open the Maximum Schedules Setup window, click the **HR and Payroll Series** button, click **PTO Manager** on the Setup content pane and then click **Maximum Schedules**.

![](media/MSS.jpg)

Enter or select a **Schedule Code** and a short **Description**. Enter the **Range From** and **Range To** and **Maximum Hours**.

PTO Manager Examples 
---------------------

This section provides examples of waiting periods, maximums, and lifeto-date/year-to-date amounts.

### Example: Waiting periods for vacation accrual 

>   According to the policies of Fabrikam, Inc., vacation time is subject to a waiting period. For full-time employees, vacation can be accrued on a recurring basis, based on the employee’s anniversary date. Sick time is not subject to a waiting period. These companywide policies are specified in the PTO Setup window (Microsoft Dynamics GP \> Tools \> Setup \> Payroll \> PTO Manager \> PTO Setup), as shown in the following illustration.

To apply this policy, in the Vacation group, under Waiting Period, mark
Recurring and Based on Anniversary Date.

![](media/PTOFTS.jpg)

>   A full-time employee of Fabrikam, Inc. accrues PTO per pay period. The vacation accrual schedule is set to accrue a maximum of 4.62 hours for an employee who has worked 0 to 5 years and 7.69 hours for an employee who has worked 5.01-10 years. This is specified in the Accrual Schedule Setup window (Microsoft Dynamics GP \> Tools \> Setup \> Payroll \> PTO Manager \> Accrual Schedules), as shown in the following illustration.

![](media/ASS41.jpg)

>   To figure the Calculation Factor, calculate the yearly maximum hours divided by the number of hours worked per year. [120 (maximum hours per year) / 2080(hours worked per year) = 0.058)

>   Fabrikam’s employee, Pilar Ackerman, accrues vacation time according to the FTVAC schedule. Pilar was hired on August 3, 2015. If the current date is August 1, 2017, the next anniversary date is August 3, 2017. This date is shown in the Waiting Period Expires Date field in the Employee PTO Maintenance window (Cards \> Payroll \> PTO)

>   The Hours Pending field shows that Pilar has accrued 70 hours vacation but the hours are not yet available.

>   During the first payroll run after 08/03/2017, the following actions occur:

-   The Vacation Available field will be set to the hours accrued including the hours pending.

-   The Hours Pending fields will be set to 0.00.

-   The Waiting Period Expires Date is reset to the next anniversary date, 08/03/2018.

>   To view the actions that occurred, open the Employee PTO Maintenance window (Cards \> Payroll \> PTO).



### Example: Carry over maximums 

>   According to the policies of Fabrikam, Inc., the carry over maximums for vacation and sick hours are based on the employee’s anniversary date. Vacation hours are allowed to be carried over with a maximum of 120.00 hours and sick hours are not allowed to be carried over.

>   These companywide policies are specified in the PTO Setup window (Microsoft Dynamics GP \> Tools \> Setup \> Payroll \> PTO Manager \> PTO Setup). Fabrikam’s employee, Pilar Ackerman, vacation carry over maximum is calculated on her anniversary date and the maximum carry over is 120.00 hours. Pilar’s sick carry over maximum is calculated on the anniversary date, with no carry over. The sick time will be reset to 0.00 on her anniversary date.

### Example: Anytime maximums 

>   According to the policies of Fabrikam, Inc., the anytime maximums for vacation sick hours are as follows:

-   **Vacation hours** are set to variable with a Maximum Schedule assigned.

-   **Sick hours** are set to fixed with a maximum of 40.00 hours.

>   To apply these policies, in the Vacation group, under Anytime Maximums, select Variable and assign the Maximum Schedule. In the Sick group, under Anytime Maximums, select Fixed and enter the maximum number of hours.


Summary 
--------

>   PTO Manager allows an organization to develop an unlimited number of accrual schedules through the use of ranges, a calculation factor and maximums. Some key points to remember from this chapter include:

-   Grant security to the windows and reports.

-   An unlimited number of accrual schedules can be developed.

-   Ranges within the accrual schedules can be based on hours worked for each pay period, hours worked each year, and hours worked lifeto-date or years worked.

-   Maximum hours can be fixed or variable.

-   The Calculation Factor is always multiplied by the employee’s hours worked in the pay period.

-   Maximum schedules can be developed to control an “any time” maximum when carryover hours are permitted.

CHAPTER 3: MAINTENANCE AND PROCESSING 
======================================

Objectives 
-----------

>   The objectives are:

-   Assign a PTO Code to an employee by defining accrual schedule, organizational waiting periods, maximums, and carry over parameters.

-   Recognize that PTO Manager works within the existing payroll processing structure.

-   Examine what happens to accrued vacation or sick time if a payroll check is voided.

Introduction 
-------------

>   This chapter discusses how to set up an employee to use PTO Manager for accruing vacation and sick time. Also discussed is how to process a payroll with PTO Manager including voiding checks.

Assigning Accrual Schedules 
----------------------------

>   Use the Employee PTO Maintenance window to configure the accrual options for each employee. To open the Employee PTO Maintenance window, click the **HR and Payroll** series button, click **Payroll** on the Cards content pane and then click **PTO**.

![](media/PTOEM.jpg)

#### FIGURE 3.1 EMPLOYEE PTO MAINTENANCE WINDOW 

>   Enter or select an **Employee ID**. Enter or select the **PTO Code**. Enter or select the **Vacation and/or Sick Accrual Schedules**.

*NOTE: The system will not allow the user to assign an Inactive PTO Setup record to an Employee. If the Inactive checkbox is marked, the system will process PTO time based on core Payroll setups.*

>   **Vacation Available** will be populated based on values which display in the Employee Vacation-Sick Time Maintenance window in the Vacation Available field.

>   **Sick Available** will be populated based on values which display in the Employee Vacation-Sick Time Maintenance window in the Sick Available field.

>   **Next Anniversary Date** will be calculated on the Hire Date or Adjusted Hire Date based on your selection in the PTO Options window.

>   Each employee can only have one PTO Code assigned and each employee must be assigned at least one Accrual Schedule. Lookup options are available when selecting schedules. The system currently supports two vacation schedules and two sick time schedules. The second vacation and sick time schedules are not required to be used, they simply provide a greater opportunity for flexibility if needed. An example of when to use the second vacation schedule may be for floating holidays or special accrual scenarios.

>   *NOTE: If a second accrual schedule is assigned (for either vacation or sick), they calculate these accruals separately and then add them together for the total vacation or sick accrual.*

>   Once a PTO Code has been selected for the Employee all the setup fields are prefilled from the PTO Code Setup window. Many of the fields are editable at the Employee level on the Employee PTO Maintenance window.

**Waiting Period Hours Pending**

>   When the waiting period functionality is used, any time accrued is put into the Hours Pending field and does not show on the employee’s check as accrued or available. When the first pay run after the waiting period has passed, the Hours Pending transfers to Available and the entire lump sum shows as “Accrued” on the employee’s check.

**Life-To-Date Hours Worked**

>   PTO Manager tracks all hours worked by each employee that is eligible for vacation and sick time. This information is used when applying accrual schedules where the Range Based On option is Hours Worked Life-To-Date. These fields are also editable to allow initial setup of hours eligible from previous data or other systems.

>   **Vacation Hours -** If eligible hours from previous data are available, that total can be entered into this field. As each pay run is processed, all eligible vacation hours for that pay period are added to the total.

>   **Sick Time Hours** - If eligible hours from previous data are available, that total can be entered into this field. As each pay run is processed, all eligible sick hours for that pay period are added to the total.

**Year-To-Date Accrued Hours**

>   PTO Manager tracks all time earned by each employee in the Year-To-Date Accrued Time fields. These fields are editable to allow initial setup of hours previously accrued for this year from previous data. These fields are also reset to 0.00 when Year-End processing occurs. The data from these fields is used when calculating maximums.

>   Additional notes about these fields include:

-   They are not used in any accrual calculations

-   During initial Employee setup, do not enter values in these fields

-   These fields are not always going to equal the Available time in the Employee Vacation/Sick card

-   When an employee uses vacation or sick time, the used amount is not subtracted from these fields

-   These fields are a running total of time that an employee has accrued since January 1 of the current year

>   **Vacation Time -** If hours accrued from previous data are available, that total can be entered into this field. As each pay run is processed, all accrued vacation time for that pay period are added to the total.

>   **Sick Time -** If hours accrued from previous data are available, that total can be entered into this field. As each pay run is processed, all accrued sick time for that pay period will be added to the total.

Processing Payroll with PTO Manager 
------------------------------------

>   Processing payroll with PTO Manager installed is no different than the Microsoft Dynamics GP core functions of payroll processing. There are no extra steps involved in the processing of payroll. After payroll has been processed, any time that has been accrued and is available for a specific employee is stored in the same core Microsoft Dynamics GP fields. This can be verified by opening the Employee Vacation/Sick maintenance card.

>   To open this window, click the **HR and Payroll** series button, click **Payroll** on the Cards content pane, click **Employee**, and then click the **Vac/Sick** button.


Voiding Checks 
---------------

>   If checks are voided for any employees that use PTO Manager and have accrued vacation or sick time on the specified pay run, the accrued time is backed out of the employee’s balance by a reversing entry.

>   *NOTE: A company cannot have a check number 000; if this check number exists, the Void Checks PTO functionality does not work. Meaning that the time the employee accrued on the voided check is not reversed out of their balance.*

Summary 
--------

>   Once the accrual schedules are set up as discussed previously, it is necessary to assign those schedules to the appropriate employees. This chapter focused on assigning accrual schedules to employees. Some key points to remember from this chapter include:

-   Waiting periods can be assigned on the employee level for a single or a recurring time period.

-   Hours accrued during the waiting period are in a pending field.

-   Vacation/Sick Time Maximums consists of Carry Over and Maximum Available Anytime.

CHAPTER 4: REPORTS AND UTILITIES 
=================================

Objectives 
-----------

>   The objectives are:

-   Run a PTO Liabilities report to determine departmental liability for sick and/or vacation time.

-   Process year-end using the PTO Utilities window.

Introduction 
-------------

>   This chapter focuses on the reporting capabilities of PTO Manager and the period end processing that needs to take place to reset values for year end.

PTO Code List Report 
---------------------

>   A PTO Codes List can be printed from the PTO Setup window. This report lists the active and inactive PTO Codes and the description.

PTO Liabilities Report 
-----------------------

>   The PTO Liabilities Report provides administration the opportunity to view any department’s vacation/sick liability.

>   To open the PTO Report Options window, click the **HR and Payroll** series button, click **Payroll** on the Reports content pane and then click **PTO**.

![](media/PTORE.jpg)

>   The criteria to set up this report states that employees must be assigned at least one accrual schedule and must have one pay code marked as a Primary Pay Code on the Employee Pay Code Maintenance window. When creating a PTO Report Option, the user has the flexibility to calculate liability (in hour and dollar amounts) for Vacation and/or Sick time. Liabilities can also be calculated by accrual schedule, in other words, only for employees with the selected accrual schedules assigned to them.

### Calculating the PTO Liability Report 

>   After the PTO Report Option is set up and the report is printed, the system will find employees that meet all specified criteria. For these employees, the system finds their primary pay code pay rate and multiplies that by the amount of hours the employees have in their Available buckets. All employee hour/dollar liabilities are displayed in the report grouped by department.

>   *NOTE: To select the Primary Pay Code in the Pay Code window, Microsoft Dynamics GP Human Resources must be installed and registered.*

PTO Utilities Window 
---------------------

>   The PTO Utilities window is used to process the year-end information for the paid-time-off accruals. To open the PTO Utilities window, click the **HR and Payroll** series button, click **Payroll** on the Utilities content pane and then click **PTO Utilities**.

![](media/PTOUT.jpg)

>   Click the **Process** button. Once Process is selected, the system checks every marked employee to allow carry over and verifies that each employee has hours that are less than or equal to the Maximum Hours Allowed. This process also resets the Year-To-Date Accrued Time fields on the Employee PTO Setup window to zero. This utility allows the company to perform the PTO Year End process at a time consistent with their business requirements.

Summary 
--------

>   This chapter focuses on the PTO Liabilities Report and how to close out a year of accruals in PTO Manager.

>   Some key points to remember from this chapter include:

-   PTO Liabilities Report can provide total hours and dollars associated with PTO Liability.

-   The Primary Pay Code must be indicated on the Employee Pay Code Maintenance window.

-   The PTO Utilities process resets the Year-To-Date Accrued Time fields on the Employee PTO Setup window to zero.

### Additional Feature Functionality added to Bank Reconciliation

Tips how PTO Manager should be setup
Understanding How PTO Manager Works in Microsoft Dynamics GP
https://community.dynamics.com/gp/b/dynamicsgp/archive/2016/06/08/understanding-how-pto-manager-works-in-microsoft-dynamics-gp



