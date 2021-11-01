---
title: "Human Resources - Position Control Setup"
description: "Learn about setting up the position control for the Human Resources functionality in Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 10/31/2021
---
# Human Resources - Position Control Setup

You can use position control to plan the positions that you will have in your organization and to track the funding sources for those positions.

Position control is optional. For companies other than the sample company, you use registration to activate it. Position control is especially useful for state and local governments, schools, and other organizations that depend on public funding.

You can create one current position plan and an unlimited number of other position plans. The other position plans are used for future planning and what-if scenarios.
You also can import position plans from Microsoft Excel. You can set up fund account information to specify the general ledger accounts that are affected during payroll processing for employees who hold a seat for a position.

[Human Resources Position Control, what is it and should I be using it?](https://community.dynamics.com/gp/b/dynamicsgp/posts/human-resources-position-control-what-is-it-and-should-i-be-using-it)

## Positions, position seats, and position plans

A position is a role in an organization, such as a teacher. Each position can have attributes such as a location, division, vacation and sick time, benefits, and pay codes. These attributes are rolled down to employee records through a process called inheritance. You can make changes to the position and automatically apply those changes to multiple employees. 

Each position can have multiple instances, called position seats. A school district might plan to hire five teachers, so there would be five seats. A seat can be filled by one employee at a time.

With position control, you can create one current position plan that represents the positions that your organization has at the present time. You can also create an unlimited number of other position plans. The other position plans are used for future planning and what-if scenarios. A position plan is identified by a position plan code. 
Position budgets, seat budgets, and fund sources

A position budget represents the budgeted amount of an employer's expense for a position, for a period of time. You can budget a certain amount of money for expenses related to a position for a period of time. You can also assign funding sources to the budget, with each source representing a percentage of the total. A funding source might be a grant or other allocation of funds from another organization. For example, a school might receive a grant to fund a teacher's aide position that did not previously exist in your organization. 

A seat budget represents the budgeted amount of an employer's expense for a seat, for a period of time. You can also assign funding sources to the budget, with each source representing a percentage of the total. For example, a school might receive a grant to fund an additional three seats of the teacher's aide position. 

## Position control effects on payroll processing

Position control affects the way that payroll transactions are processed in the following ways:

- By removing transactions that do not fit the criteria for the *CURRENT position plan. This helps to ensure that you do not pay employees for positions that are not part of the position plan.
- By updating pay rates based on seat detail records. This helps to ensure that employees are paid the correct amount based on the position seat that they are assigned to. For example, if an employee is temporarily assigned to a seat that pays more than their regular pay rate, the employee can be paid at the higher rate.

## Removing transactions

Payroll transactions for employees are removed from pay runs in the following situations:

- There was a problem with the inheritance process and information was not completely copied from the position and seat to the employee record.
- The employee is not assigned to a seat detail record for the position that is assigned to the payroll transaction.
- The assignment status is On Hold without Pay and Benefits for the seat detail record for the employee.
- The assignment status is Expired for the seat detail record for the employee.
- The payroll transaction date is outside the start date and end date range for the seat detail record.
- The seat is inactive.

## Updating pay rates based on seat detail records

Pay rates can be based on the seat detail records regardless of whether you enter the transactions in the Payroll Transaction Entry window or the Mass Payroll Transaction Entry window.
The pay rates from the seat detail records override the pay rate from the Employee Pay Code Maintenance window when a payroll build is processed, if the following conditions are met:

- The Seat option is selected in the Pay Rate Based On field in the Position Seat Detail window.
- The employee is assigned to the seat.
- The payroll transaction date is between the start date and end date for the seat assignment.
- The pay code is the primary pay code for the position, or a pay code that is based on a primary pay code. For example, if the primary pay code is Hourly, the related Overtime pay code is also overridden.
- The frequency of the pay code in the Position Seat Detail window matches the frequency of the pay code in the Employee Pay Code Maintenance window. For example, if the pay code is a weekly amount in one window, it must be weekly in the other window.

## Fund account effects on payroll processing

Typically, when payroll checks are calculated, the payroll posting accounts that are specified in the Posting Account Setup window are used. If you are using position control, the payroll check calculation process also uses the fund accounts that are specified in the Position Budget Fund Sources window. The segments from these accounts can be combined dynamically to determine the posting accounts that are actually used. This enables you to override the payroll posting accounts for a period of time, and then easily revert to the original posting accounts. 

For example, you receive a grant to build a park, and the project is expected to last for four months. You can set up a fund source and fund account for the positions that are included in the grant, and then use the Fund Account Options to specify the source of the account segments that are used to generate the posting accounts that are used for payroll processing. In this example, you would create a budget schedule and corresponding fund source for the four-month period of the park project. When the four-month time frame has elapsed, the system will automatically stop allocating funds to the grant associated with the park project.

You can specify the source of account segments for the following expense pay types:

- Gross Pay
- Benefits Expense
- Taxable Benefits Expense
- Employers Tax Expense - FICA/Medicare
- Employers Tax Expense - FICA/Social Security

## Setting up position control

If you are using position control, use the Position Control Setup window to select budget override options for permanent seats, temporary seats, full-time equivalents (FTEs), and employer expenses, and whether to save override information to history. Your selections in this window apply when a change is made that would cause the actual employer expense for a position to exceed the budgeted employer expense for the position. You can also specify whether unassigned positions are included when making payroll builds.

### To set up position control

1. Open the Position Control Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Control)
2. Choose budget override options for permanent seats, temporary seats, FTEs, and employer expenses.

    The following options are available.

    |Override option |Column2  |
    |---------|---------|
    |Allowed |Allows you to exceed budget amounts without any warning.   |
    |Warning    |  Allows you to exceed budget amounts, but provides a warning. |
    |Password Required   | Requires you to enter a password to exceed budget amounts.|
    |Not Allowed   | Does not allow you to exceed budget amounts.|

3. Choose whether to allow, disallow, or issue a warning before including employees with no seat assignments in payroll builds.
4. Mark the Save Changes to History option to save the budget override changes to history.
5. Mark the Enable Position Control in Sample Company option if you want to use position control in the sample company, Fabrikam, Inc. 
You must restart Microsoft Dynamics GP for the change to take effect.
6. Choose OK to save changes.

## Setting up position plan codes

Use the Position Plans window to create plan codes. You can create multiple position plans with varying configurations of position codes, departments, and so on. Once you have set up at least one position plan, you can copy it to use as the basis for other position plans.

### To set up position plan codes

1. Open the Position Plans window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Plans)
2. Enter a code that identifies the plan and a description.
3. Enter starting and ending dates for the plan.
4. You can mark Inactive if you want to make the plan inactive. You cannot make the current plan inactive.
5. You can choose Make Current to make the selected plan the current plan. If you print a report during this process, and if the plan has any inactive employees assigned to the position seats, the report will display the plan information for inactive employees only.
6. To base a new plan on an existing plan, select the existing plan and choose Copy. In the Copy Plan window, enter an ID and description for the new plan and choose Copy.
When you copy a plan, all details of the plan are copied, including details for each employee that's included in the plan.
7. You can choose the Excel button to either export the plan information to an Excel workbook or to import it from an Excel workbook.
8. Choose OK to save your entries.

## Importing a position plan from Microsoft Excel

You can import plan information from a Microsoft Excel workbook into an existing Microsoft Dynamics GP plan, or into a newly created Microsoft Dynamics GP plan.

> [!NOTE]
> If you choose to import the Microsoft Excel plan workbook into an existing Microsoft Dynamics GP plan, the existing information in the Microsoft Dynamics GP plan will be overwritten with the information from the workbook.

The workbook that you import must use the correct format. To create a workbook that uses the correct format, generate Excel-based export reports for an existing plan and then use those reports as the basis for your new workbook. 

### To import a position plan from Microsoft Excel

1. Open the Position Plans Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Plans)
2. Select the position plan that you want to import data to.
3. Choose Excel and select Import from Excel to open the Welcome to the Plan Wizard for Excel window.
4. Choose Next to open the Excel File Selection window.
5. Enter or select the name of the Excel file to import.
6. Choose Next to open the Completing the Plan Wizard for Excel window.
7. Choose Finish to complete the import process.

## Setting up a position code for a position plan

Use the Position Setup window to set up a position code. A position is a defined role within a company. You can create multiple positions for a single position plan. 

### To set up a position code for a position plan

1. Open the Position Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Select a plan code.
3. Enter a code that identifies the position, and a description. Choose the notes button to add additional comments.
4. Enter or select a department code for this position.
5. Enter information about the position.  
6. Choose Employee Details to assign default position attributes.  
7. Choose Accounts to assign default general ledger posting accounts for the current position/plan combination.  
8. Choose Vac/Sick to set up default accrual vacation and sickness information for the current position/plan combination.  
9. Choose Budget/Wage to assign the position budget and wage information.  
10. Choose Save.  

## Copying an existing position for a position plan

If you are using position control, you can use the Copy Position window to copy the information from an existing position/plan combination to a new position/plan combination.

### To copy an existing position for a position plan

1. Open the Copy Position window. (Microsoft Dynamics GP menu >> Tools >> Utilities >> Human Resources >> Copy Position)
2. Select a position plan code.
3. Enter or select an existing position code.
4. Enter a new position code. You cannot select a position code that exists in the selected plan.
5. Enter a description of the new position code.
6. To include pay codes, benefits, and seat information in the new position, select the respective check boxes. To include the funding sources information, select Budget Schedules and Funding Sources.
7. Choose Copy to copy the existing position information to the new position record.

## Setting up position seats

If you are using position control, you can use the Position Seats window to create and assign multiple seats to an existing position/plan combination. You can indicate whether a seat is a permanent type or a temporary type.

### To set up position seats

1. Open the Position Seats window. (Cards >> Human Resources >> Position Control >> Position Seats or   Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Seats)
2. Select a plan code.
3. Enter or select a position code.
4. Select whether to display permanent or temporary position seats in the scrolling window.
5. You can mark the Show Inactive check box to view both active and inactive plan codes.
6. In the scrolling window, create a new record for the seat. The value in the Seat field automatically will take the next available whole number. 
7. Enter a description for the position seat.
8. Enter the standard number of hours the employee works per year. For example, if the employee works 40 hours per week for 50 weeks per year, enter 2000.
9. Enter a FTE (full-time equivalency) value to determine the pay rate for the employee assigned to the selected position seat.
10. To enter a budget amount for the employer's expense that is associated with the selected seat, choose the Employer Expense - Seat expansion button. 
11. Choose OK to save the position seat information.

## Assigning employees to position seats

If you are using position control, you can use the Position Seat Detail window to assign an employee to each seat. However, you cannot add or change employee assignments if the seat is inactive.

You can assign a substitute employee to a seat when the assignment status of the employee has the following values: On Hold with Pay and Benefits; On Hold Without Pay and Benefits; or Available.

### To assign employees to position seats

1. Open the Position Seats window.  (Cards >> Human Resources >> Position Control >> Position Seats) 
2. Select a plan code and a position code.
3. Choose the Seat expansion button to open the Position Seat Detail window.
4. Enter or select an employee ID to assign to the position seat.
5. Enter the starting date and the ending date for the position seat for the selected plan.
6. Select the position seat assignment status for the employee.

    The employee ID must have an active maintenance record, and no other active seat must have this employee ID assigned to it, for the current position/plan combination.

    The Primary check box is not available for the temporary position seats.

7. If you are using pay steps, select a type of date based on which the pay step increases for the employee assigned to the position seat. The pay steps fields are active if the Use Pay Steps/Grades option is marked in the Human Resources Preferences window.
8. Enter or select a pay step table ID.
9. If you select Manual as the type of date for the Based Step Increases On field, enter or select the pay step or pay grade to assign to the employee.
10. Accept the default date or enter a different date to make the selected pay step effective for the employee.
11. Mark Seat to calculate the pay rate based on the seat information, or mark Employee Pay Code to calculate the pay rate based on the employee pay code information.
12. Save the changes to position seat details.

## Assigning multiple pay codes to a position/plan combination

Use the Position Pay Code Assignments window to assign multiple pay codes to a position/plan combination. You can apply a pay step table to an employee's pay code if the Use Pay Steps/Grades option is marked in the Human Resources Preferences window.

### To assign multiple pay codes to a position/plan combination

1. Open the Position Pay Code Assignments window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Pay Codes)
2. Select a plan code.
3. Enter or select a position code from a list of position codes that belong to the selected plan code.
4. Enter a pay code and the pay rate for the amount of pay.
5. Select Primary Position/Seat if the selected pay code record is the primary pay code. There can be only one primary position pay code.
6. Select Budgeted to calculate the projected employer expense for the current position. You can select this check box only if the position pay code has one of the following pay types: Hourly, Salary, Commission, or Other.
7. Enter or select pay steps information. The pay steps fields are active if the Use Pay Steps/Grades option is marked in the Human Resources Preferences window, and the selected pay code is not based on another pay code.
8. Choose Save. If the seats with the inheritance status Saved have any modified inheritance information, mark Yes to update the inheritance records with the position information. If the inheritance status is Completed, each active seat for the current position is updated to Changed status.

## Assigning default employee attributes to positions

Use the Position Employee Information window to assign position attributes such as division, location, employee type, and so on to employees assigned to the selected position.
During inheritance, the position attributes will be copied to the employee card.

### To assign default employee attributes to positions

1. Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Select or enter a plan code and a position code. Choose Employee Defaults to open the Position Employee Information window.
3. Enter or select a division, location, and supervisor for the employee.
4. Select an employment type and an employment class.
5. Enter or select the code for the workers' compensation classification that applies to the employee.
6. Indicate whether you want to post the next pay for the employees in the class, to a cash account from the checkbook used for each pay run, or to an account specified for each employee.
7. Mark Calculate Minimum Wage Balance if this employee must be paid at least the minimum wage when their regular wage plus tips does not equal the minimum wage.
8. Enter or select the name of the employee's union.
9. Enter the employee's union contract number.
10. Enter the starting date and the ending date of the contract period.
11. Enter the amount the employee pays as union dues.
12. Choose OK to save the position attributes.

## Assigning default posting accounts for positions

Use the Position Accounts Assignment window to assign default general ledger posting accounts for the selected position/plan combination. You cannot edit the position account information if the department code is not assigned.

### To assign default posting accounts for positions

1. Open the Position Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Select or enter a plan code and a position code and choose Accounts to open the Position Accounts Assignment window. You can view the information for the selected position/plan combination.
3. Select the position accounts for the gross wages, benefits expense, worker's compensation tax expense, taxable benefits expense, and employer's tax expense account types.
4. Choose OK to save the account information.

## Setting up position vacation and sickness accrual

Use the Position Vacation and Sick Accrual Setup window to assign the default accrual vacation/sickness setup information for the current position/plan combination.

### To set up position vacation and sickness accrual

1. Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Select or enter a plan code and a position code, and choose Vacation/Sick to open the Position Vacation and Sick Accrual Setup window.
3. Select the position and department for the employee.
4. Select Accrue Vacation to accrue vacation time for the employee automatically.
5. Mark Hours Worked if the employee accrues vacation based upon hours worked. Mark Set Hours if the employee accrues vacation time by a specific amount per pay period.
6. If you marked Hours Worked, enter the number of vacation hours the employee should receive each year. If you marked Set Hours, enter the number of vacation hours the employee should receive each pay run.
7. Select Accrue Sick Time to accrue sick time for the employee automatically.
8. Mark Hours Worked if the employee accrues sick time based on hours worked. Mark Set Hours if the employee accrues sick time by a specific amount per pay period.
9. If you marked Hours Worked, enter the number of sick time hours the employee should receive each year. If you marked Set Hours, enter the number of sick time hours the employee should receive each pay period.
10. Choose OK to save the position vacation and sickness accrual information.

## Setting up position budget and wage information

Use the Position Budget and Wage Information window to set up the position budget and wage information.

### To set up position budget and wage information

1. Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Select or enter a plan code and a position code, and choose Budget/Wage to open the Position Budget and Wage Information window.
3. Enter a percentage of the calculated rate to calculate the benefit.
The system calculates an amount for wages that have not been paid by using the pay codes for the position. The resulting amount is multiplied by the percentage you enter here. That amount is then added to the calculated wage amount to calculate the actual cost for the position.
4. Enter the benefit amount per day. This amount is added to the actual cost of the position. The time period is calculated based on the number of days that a position seat detail record has an employee ID assigned with a seat assignment status of either Assigned or On Hold with Pay and Benefits.
5. Enter the tax expenses and tax amount.
6. Enter the number of budgeted permanent seats and budgeted temporary seats.
7. Enter an FTE (full-time equivalency) value to make sure the position is not overfilled. For example, you might intend to have four half-time positions. To ensure that the seats are not filled with full-time employees, you would set the budgeted FTE value to 2.0.
8. Choose OK to save the position budget and wage information.

## Setting up position budget schedules and fund sources

Use the Position Budget Schedule window to create budget schedules and to assign them to a specific position/plan combination. You can specify date ranges for the budget schedules.

Use the Position Budget Fund Sources window to assign multiple fund sources to budget schedules for a position. You can specify a percentage amount for each fund. The sum of all fund percentages must add up to 100.

### To set up position budget schedules and fund sources

1. Open the Position Budget Schedule window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Budget Schedules)  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position >> Budget/Wage >> Employer Expense expansion)
2. Select a plan code and a position code to assign a budget schedule for.
3. Enter the starting date and the ending date of the period range for the budget schedule.
4. Enter a description for the budget schedule.
5. Enter the budget amount. This amount should include the total amount of pay, benefits, and taxes for the time period that you specified in step 3.
6. Choose the Amount expansion button to open the Position Budget Fund Sources window. 
7. Enter or select an account.
8. Enter identification for the fund source and a percentage for the fund.
9. The Amount field displays the fund amount as a percentage of the budget amount.
10. Choose OK to save the fund sources information and close the Position Budget Fund Sources window.
11. Save the budget schedule information and choose OK to close the Position Budget Schedule window.

## Setting up fund account options

Use the Fund Account Options window to specify the source for general ledger account segments for general ledger posting accounts. You can assign the general ledger account segments either from the position budget fund source or from the payroll posting account setup.
You can specify the expense payroll types that posting accounts are updated for during the payroll processing.

### To set up fund account options

1. Open the Fund Account Options window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >>  Position Control >> Fund Account Options)
2. Select whether the source of General Ledger account segments is the Payroll Posting Account Setup or the Budget Fund Source.
3. Select the expense payroll types.
4. Save the fund account options information and close the window.

## Setting up seat budget schedules and fund sources

Use the Position Seat Budget Schedule window to create budget schedules and to assign them to a specific position seat. You can specify date ranges for the budget schedules.
Use the Position Seat Budget Fund Sources window to assign multiple fund sources to budget schedules for a position seat. You can specify a percentage amount for each fund. The sum of all fund percentages must add up to 100.

### To set up seat budget schedules and fund sources

1. Open the Position Seat Budget Schedule window.  (Cards >> Human Resources >> Position Control >> Budget Schedules)
2. Select a plan code, position code, and seat to assign a budget schedule for the position seat.
3. Enter the starting date and the ending date of the period range for the budget schedule.
4. Enter a description for the budget schedule.
5. Enter the budget amount per day.
6. Choose the Budget Amount expansion button to open the Position Seat Budget Fund Sources window. Enter or select an account.
7. Enter identification for the fund source and a percentage for the fund.
8. The Amount field displays the fund amount as a percentage of the budget amount.
9. Choose OK to save the fund sources information and close the Position Seat Budget Fund Sources window.
10. Save the budget schedule information and close the Position Seat Budget Schedule window.

## See also

[Position Control in Dynamics GP](PositionControl.md)  
[Human Resources - Company Setup and Organizational Structure](human-resources-company-setup.md)  
[Human Resources in Microsoft Dynamics GP](HumanResource.md)  
