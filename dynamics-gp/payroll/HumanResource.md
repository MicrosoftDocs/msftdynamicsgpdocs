---
title: "Human Resources"
description: "Learn about the Human Resources functionality in Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 03/5/2021
---
# Microsoft Dynamics GP Human Resources

You can use Human Resources to set up, enter, and maintain most of your employee management needs and to track organizational details and personal information
for employees within your company. You also can use Human Resources to view important information about employees, their benefits, and other historical data.

You also can use Human Resources to complete the following tasks:

-   Manage the interviewing and hiring of applicants, track the termination, training, and evaluation of employees, and maintain organizational details,
    such as the supervisor, position, and department assignment of employees
    
-   Create company benefit plans—complete with employee and employer deduction provisions, enroll employees and their dependents in benefits, and calculate
    the benefit value

-   Enter employee attendance information, including creating attendance transactions and tracking planned absences for employees

-   Define vacation and other time accruals tracked in your organization and how employees can earn time accruals, then set up schedules to show how employees can earn the time accruals at various rates

-   Monitor the distribution of company property, such as laptop computers and cell phones, to employees

If you are using U.S. Payroll, you can enter and maintain your employee information in Human Resources and those transactions automatically will update your payroll records.

## Part 1: System setup

This explains how to define Human Resources preferences.

If you are setting up Human Resources in the absence of Payroll, after setup you must modify user security settings to enable user access to Human Resources
functionality. 

### Chapter 1: Human Resources preferences

You can specify default employee numbers for your organization by entering an employee ID in the Human Resources Setup window. 
You can choose to have Human Resources automatically assign employee IDs and increase the employee ID number by one for each new record in the Employee Maintenance window.

You can customize the way Human Resources works for your organization by specifying preferences in the Human Resources Preferences window. The user
preferences you select will be applied to all the companies within your organization. You also can set up user access to employee information by divisions and departments.

Use the Human Resources User Preferences window to indicate which window should be displayed when you start Human Resources and choose to display
employee information by descriptions or codes in the Employee Maintenance window.

This information is divided into the following sections:

-   *Setting up an employee number*

-   *Setting up Human Resources preferences*

-   *Setting up user access to employee information*

-   *Copying user access to employee information*

-   *Setting up Human Resources user preferences*

#### Setting up an employee number

Use the Human Resources Setup window to assign default employee IDs automatically. Each time you add a new employee in the Employee Maintenance
window, the default number will increase by one to the next available number as each number is accepted.

If you are registered for Payroll, the same settings in the Payroll Setup window will be updated with your settings in the Human Resources Setup window.

*If you use Microsoft Dynamics GP on a network where more than one person is entering new employee records at the same time, the default number might
appear to increase by two or more.*

**To set up an employee number:**

1.  Open the Human Resources Setup window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Human Resources \>\> Human Resources)

2.  Mark the Auto Assign Employee ID option to assign an employee ID for each new employee record.

3.  Enter the next employee ID that will be displayed when you add a new employee record in the Employee Maintenance window.

4.  Choose OK to save your changes.

#### Setting up Human Resources preferences

Use the Human Resources Preferences window to set up Human Resources preferences for your organization.

**To set up Human Resources preferences:**

1.  Open the Human Resources Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Human Resources Preferences)

![](media/HRPREF.jpg)

2.  Mark options for seniority dates and address changes.

The following table describes each option.

| **HR preference option**                      | **How to use this option**                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Update seniority date with adjusted hire date | Mark to use an employee’s adjusted hire date as the seniority date for calculating accruals, such as vacation and sick time.              |
| Adjusted hire date for benefits               | Mark to use an employee’s adjusted hire date to determine eligibility for benefits, such as health insurance and 401(k) enrollment dates. |
| Adjusted hire date for length of service      | Mark to use an employee’s adjusted hire date to determine length of service on the Employee Service by Hire Date report.                  |
| Address change report                         | Mark to track an employee’s previous address.                                                                                             |

Changes to the adjusted hire date in the Employee Maintenance window will update the seniority date in the Employee Attendance Maintenance window.

*An adjusted hire date is a hire date that has been changed to reflect time away from the job. For example, suppose an employee leaves your company but
is hired again by your company six months later. You can create an adjusted hire date that is six months after his first hire date, which is then used
to determine his benefit time and benefit eligibility.*

3.  Mark the Purge Applicants option to automatically delete applicant records at defined intervals.

Enter the number of days that the applicant records should remain in the system before being deleted. The Last purge date field displays the date
when applicant records were last deleted.

4.  Mark the Use Pay Steps/Grades option to enable the use and display of pay step information throughout Human Resources.

Select the type of date for the basis of the pay step increase. The date options are: Hire Date, Adjusted Hire Date, Seniority Date, or Manual.

The selected type of date becomes the default option each time you create a pay step table.

The pay steps feature integrates with U.S. Payroll, but is not available with Canadian Payroll.

5.  Select Class or Course at Position Training Links to link classes or courses to positions defined in the Position Setup window.

You can link positions with class or course training requirements. For example, your company may require new sales staff to complete a product
marketing course that consists of six monthly classes. For more information, see *Setting up a training course* and *Setting up a training class*.

6.  Select EEO-1 or EEO-4 to change the options in the EEO Class list in the Position Setup window in Payroll.

7.  Mark or unmark your preferences for the position, salary and pay code options.

The following table describes each option.

| **HR preference option**                         | **How to use this option**                                                                                                                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto Create Position/Pay Code links              | Mark to automatically create a link between each pay code and each position. For more information, see *Linking pay codes to a position code.*                                                                          |
| Edit Attendance Maintenance and Earnings History | Mark to allow changes to attendance information in the Employee Attendance Maintenance window and to information in the Earnings History window.                                                                        |
| Enable Reason for Pay Adjustment                 | Mark to automatically open the Reason for Change window when making pay adjustments. In this window, enter an effective date and reason for the salary change.                                                          |
| Enable Cancel on Reason for Pay Adjustment       | Mark to make the Cancel button available in the Reason for Change window. Unless you’ve marked this option, you must always give a reason for the salary change before closing the window.                              |
| Ignore Position/Salary Matrix Links              | Mark if you don’t want a message displayed when an employee’s salary is outside the salary matrix ranges or a salary matrix doesn’t exist. For more information about using matrix links, see *Adding a salary matrix*. |
| Default Employee Info to Dependent               | Mark to display the employee’s address and phone information in the Employee Dependents window.                                                                                                                         |

8.  Mark or unmark your To Do List options.

The To Do List window is used to view calendar information, such as employee benefit eligibility dates and orientation dates.

| **HR preference option**            | **How to use this option**                                                                                                        |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Roll Forward System To Do List      | Mark to have the system include today’s To Do List unfinished items on the next day’s To Do List.                                 |
| Purge To Do Lists (System/Personal) | Mark to delete the To Do List items and enter the number of days that the items should remain in the system before being deleted. |

9.  Mark the Enable Attendance for Canada option if you are using Canadian Payroll and want to use the attendance features in Human Resources. This
    option is available only if Canadian Payroll is registered.
    
10.  Mark the Never, Always, or Ask Each Time options to automatically create and update position vacancies.

11.  Mark the Never, Always, or Ask Each Time options to automatically create and update organizational requisitions.

*To select Employee Filters and User Access Duplication, refer to Setting up user access to employee information.*


## Setting up user access to employee information
Use the Employee Filter Divisions window and the Employee Filter Departments window to set up user access to employee information by divisions and departments.

## To set up user access to employee information:

1.	Open the Human Resources Preferences window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> System >> Human Resources Preferences)
2.	Mark Division and choose the expansion button to restrict user access by division. The Employee Filter Divisions window will open.
3.	Mark Department and choose the expansion button to restrict user access by department. The Employee Filter Departments window will open.
4.	Select a user ID. Mark divisions or departments in the Employee Filter Divisions window and Employee Filters Departments window to grant user access. To remove access, unmark a division or department.
5.	Choose OK to save your changes.

## Copying user access to employee information

Use the Human Resources Preferences window to copy user access to employee information by divisions and departments from one user to another.

To copy user access to employee information: 

1.	Open the Human Resources Preferences window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> System >> Human Resources Preferences)
2.	Select a user to copy access information to in the Grant user field.
3.	Choose the Like user lookup button to open the User Lookup window. Then select a user from which to copy access information in the Like user field.
4.	A message gives you the option to copy the access information to the Grant user field.

## Setting up Human Resources user preferences

Use the Human Resources User Preferences window to set up Human Resources preferences for each user. You can select windows to be displayed when you start Human Resources and choose whether employee information will be displayed by descriptions or codes in the Employee Maintenance window.

To set up Human Resources user preferences:

1.	Open the Human Resources User Preferences window.  (Microsoft Dynamics GP menu >> User Preferences >> HR button)
2.	Indicate if you want a To Do List window to open when you start your Human Resources system.
•	Mark the Open To Do List option for the To Do List window to be displayed when you start Human Resources.
•	Mark the Open Personal To Do List option for the Personal To Do List window to be displayed when you start Human Resources.
3.	Mark the Roll Personal To Do List Forward option to move personal to do list entries that aren’t cancelled or finished to the next day in the to do list.
4.	Select the Code option to display the organizational codes in the Employee Maintenance window. Select the Description option to display the organizational descriptions in the Employee Maintenance window.
5.	Choose OK to save your changes.


## Part 2: Company setup

### Chapter 2: Organizational Structure

Your company’s organizational structure might include multiple levels, such as divisions, departments, positions, supervisors, and locations. You can create these levels and store additional information for each level.

A division is a branch of a company, usually including several departments. A department is a specialized portion of a division or company, which usually concentrates on one type of task. You’ll use several windows to enter the various types of organizational information for your business. Some companies conduct business from more than one site or location and each site has a different address.

Each position has certain physical requirements. The Americans with Disabilities Act (ADA) prohibits employers from discriminating against qualified individuals with disabilities. Use the Position Setup window to enter employee positions, and use the ADA Physical Requirements window to define the physical requirements for each position.

Many positions require special skills and training and you can link training courses and classes to position codes. You can use the Position Course Link window and the Courses Available to Link window to link skill and training requirements to position codes.

You can use position control to plan future positions and roll down information from the planned positions and position seats to employees. Position control is optional. 

Use the Company Human Resources Setup window to set up company human resources information, such as the type of business and Standard Industrial Classification (SIC), Dun & Bradstreet (DUNS), North America Industry 
 
Classification System (NAICS), and Vets-100 numbers. You can set up human resources information for each company.

To set up company human resources information:
1.	Open the Company Human Resources Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Company >> Company >> Human Resources button)
2.	Enter the type of business and the SIC number for this company. 
3.	Enter the DUNS number and Vets-100 number for this company.
4.	Choose OK to save your changes.


## Setting up an operating procedure
Use the Operating Procedures Setup window to set up an operating procedure. You can use the OLE (Object Linking and Embedding) Container to attach files created in other applications. 

To set up an operating procedure
1.	Open the Operating Procedures Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Operating Procedures)
2.	Enter a category name that describes the operating procedure.
3.	Enter the operating procedure information.
Choose the paperclip button to open the OLE (Object Linking and Embedding) container and store additional information. 
4.	Choose Save.

**Setting up a division code**
Use the Division Setup window to set up a division. A division is an organizational level between a company and a department. A company can have several divisions, and each division can have several departments. You also can add information using extra fields. 
To set up a division code:
1.	Open the Division Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Division)
2.	Enter a name that identifies the division and a code or accept the default code.
3.	Enter an address, city, state, and postal code for this division.
4.	Enter a phone number, fax number, and e-mail address for this division.
5.	Choose Extra Fields to open the Division Extra Fields window. For more information, refer to Setting up organizational extra fields on page 105.
6.	Choose Save.

**Setting up a department code**
Use the Department Setup window to set up a department code. A department is a specialized unit of a division or company, which usually concentrates on one type of task. For example, accounting and purchasing are typical departments. You can use up to six letters and numbers to create a department code. You also can add information using extra fields. 

**To set up a department code:**
1.	Open the Department Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Department)
2.	Enter a code that identifies the department and a description.
3.	Choose Extra Fields to open the Department Extra Fields window.
4.	Choose Save.

**Setting up a position code**
Use the Position Setup window to set up a position code. A position is a defined role within a company. You can create multiple positions for a single position plan. You can link training courses and specify which skill sets, if any, are required for a position. You also can link pay codes and Americans with Disabilities Act (ADA) physical requirements to a position code.

If your company uses salary matrices, you can link the low, middle, and high salaries for each position to a position code. You also can add information using extra fields. 

To set up a position code:
1.	Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
 
If you are using Position control, the window has the following appearance. 
 
2.	Enter a code that identifies the position, and a description. Choose the notes button to add additional comments.
3.	Select an Equal Employment Opportunity (EEO) class and a Fair Labor Standards Act (FLSA) status.
4.	Enter or select a position the individuals in the position report to.
5.	Enter or select the review type to be used for employees in this position and enter or select a required skill set.
6.	Enter a description of the position in the Position Description field.

Choose the paperclip button to open the OLE (Object Linking and Embedding) container and store a position description file.

7.	Choose Linked Pay Codes to open the Position \ Pay Code Setup window and link pay codes and salary ranges to this position code. 
8.	Choose ADA to open the ADA Physical Requirements window. 
9.	Choose Training to open the Courses Available to Link window. 
10.	Choose Extra Fields to open the Position Extra Fields window. 
11.	Choose Save.

**Setting up a location code**
Use the Company Addresses Setup window to set up a location code, which includes an address, phone numbers, and a contact person for each location. If your company has multiple sites, you can track which employees are working from which sites by setting up location IDs.

To set up a location code:
1.	Open the Company Addresses Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Location)
2.	Enter an identification and name for the company’s location.
3.	Enter contact, address and phone information.
4.	Choose Address ID Internet to enter or view Internet information for this address. 
5.	Choose Save.

**Setting up company Internet information**
Use the Internet Information window to track Internet-related information about your company, such as e-mail addresses, Web page URLs, and FTP sites. If you’ve set up multiple addresses for your company, you can track Internet information for each address.

To set up company Internet information:
1.	Open the Internet Information window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Company >> Internet Information)
2.	Select a company in the Select Information for field.
The company you’re currently logged in to is displayed in the Company ID field.
3.	Enter or select an address in the Address ID field.
4.	Enter Internet information.
5.	Choose Save to save your entries.
6.	To print Internet information for the current company, choose File >> Print or the printer button. The Internet Information Report is printed, showing Internet information for the current company.
To print an Internet Information Report showing Internet information for all companies, use the Company General Report Options window. 

**Linking pay codes to a position code**

Use the Position and Pay Code Setup window to link pay codes to a position code.
If you marked the Auto Create Position/Pay Code links option in the Human Resources Preferences window, you do not need to link pay codes to a position code manually with this procedure.

To link pay codes to a position code:
1.	Open the Position\Pay Code Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position and Pay Code)
2.	Enter or select a position code.
3.	Enter or select a pay code and choose the Salary Range lookup button. The Salary Matrix Lookup window will open.
4.	Select a table.
5.	Select a salary to use as the low salary indicator and choose the Low select button.
6.	Select a salary to use as the middle salary indicator and choose the Medium select button.
7.	Select a salary to use as the high salary indicator and choose the High select button.
8.	Choose Select to display the salary information in the Position\Pay Code Setup window.
9.	Choose Save.

**Understanding pay steps**
Before you can begin using the pay steps feature, you need to activate it in the Human Resources Preferences window. The pay steps feature integrates with U.S. Payroll, but is not available with Canadian Payroll.

You can use pay steps to associate an employee’s amount of time in a position with a rate of pay. A pay step table lists pay steps (or grades) by number, the assigned duration of each step, and the dollar amounts for each step under successive effective dates.

For example, after an employee has served in a position for the full duration of a pay step, the employee advances to the next pay step and its corresponding pay rate under the current effective date. When the next effective date arrives, the employee advances to the new pay rate for the current pay step.
The following illustration is an example of a pay step table.
 
When you assign an employee and an associated pay code to a pay step table (in the Employee/Pay Step Table Entry window or the Employee Pay Code Maintenance window), you can base the step increases on the employee’s hire date, adjusted hire date, seniority date, or a manually entered date.

The Payroll system creates post-dated pay rates for the future increases indicated in the pay steps table. A reminder on your Microsoft Dynamics GP home page lists employee post-dated pay rates eligible for activation. After you activate an employee’s post-dated pay rate, it becomes effective, on the designated date, for all future pay periods.
To use the example illustration: assume that the step increases are based on the hire date, and that the pay rates are activated. If the employee was hired on July 25, 2006, and the current date is May 25, 2007, the employee would be in pay step 1, with a pay rate of $20.00. On July 25, 2007, the employee would advance to pay step 2, with a pay rate of $25.00. On January 01, 2008, the next column of pay rates would become effective, and the employee’s pay rate would advance to $26.00.

You can use multiple pay step tables to associate pay rates with other employee qualifications, such as education, in addition to time in a position. For example, if you base employee pay rates, in part, on education level, you can create a pay step table for “Bachelor’s Degree” and another for “Master’s Degree.”

You can use the Microsoft Dynamics GP system’s Activity Tracking feature to monitor pay step table additions, changes, and deletions. Select either the activity type Access Tracking, or Field Tracking. For more information about Activity Tracking, refer to the System Setup documentation.

Setting up pay step tables
You can create, save, modify, and delete pay step tables. In the Pay Step Table Entry window, you can create pay step tables having as many steps, number of months in each step, and effective dates, as you want. You can also enter past effective dates to record historical pay rate information.

You can export pay step table information to a Microsoft Excel® file, for further analysis and review.

Within a pay step table, you can add, copy, and delete columns, and delete rows.
For more information about changing and using a pay step table after you set it up, see Modifying or deleting pay step table data on page 28 and Assigning a pay step table to employees on page 185.

To set up a pay step table:
1.	Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2.	Enter a pay step table ID and a short description.
3.	Select a unit of pay, either Hourly Rate or Salary.
4.	Enter the effective date. This date indicates when a new column of pay rates becomes effective, typically 01 January of successive years. You can enter any past, present, or future date.
5.	Enter the step (or grade) number into the pay step table.
6.	Enter the duration of this pay step as a range of months. For example, a range of 0 to 11 indicates that a new employee remains at this pay step for the first 12 months of employment.
7.	Enter a dollar amount in the cell across from the step number and below the effective date.
8.	Press the TAB key to begin a new row.
9.	To add additional effective date columns, select the Add Column tab, enter a date, and choose Add.
10.	Choose Save.
11.	Choose Clear to remove all selections from the window.

Modifying or deleting pay step table data
You can add and remove columns in existing pay step tables by selecting the appropriate tab. You also can copy and adjust the amounts from an existing column to create a new column in the same table. See Setting up pay step tables on page 27.

You cannot change or delete pay step data in columns with effective dates earlier than the user date. Such data is preserved as historic data.
To add a column:
1.	Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2.	Select a pay step table ID.
3.	Choose the Add Column tab. 
4.	Enter the effective date.
5.	Choose Add to add the new column to the table.
6.	Choose Save.

To copy a column:
1.	Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2.	Select a pay step table ID.
3.	Choose the Copy Column tab.
4.	Select the effective date of the pay step column you are copying.
5.	Enter or select the effective date of the column you are creating.
6.	Enter the amount or percentage of adjustment to apply to the copied amounts.
7.	Choose Copy to create the new column.
8.	Choose Save.

To remove a column:
1.	Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2.	Select a pay step table ID.
3.	Choose the Remove Column tab.
4.	Select the effective date of the pay step column you are removing.
5.	Choose Remove.
6.	Choose Save.

Adding an ADA physical requirements record
Use the ADA Physical Requirements window, the ADA Physical Requirements 
Page 2 window, and the ADA Physical Requirements Page 3 window to add an ADA physical requirements record. The Americans with Disabilities Act (ADA) prohibits employers from discriminating against qualified individuals with disabilities.

To add an ADA physical requirements record:
1.	Open the Position Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Enter or select a position code and choose ADA. The ADA Physical Requirements window will open.
3.	Enter a description of the position in the Job Purpose field and mark the appropriate requirements for this position.
4.	Choose the page turn button to open the ADA Physical Requirements Page 2 window and mark the appropriate requirements.
5.	Choose the page turn button to open ADA Physical Requirements Page 3 and mark the appropriate requirements for the position.
6.	Choose Save. The ADA Physical Requirements window is displayed.
7.	Close the window.

Duplicating an ADA requirements record
Use the Duplicate ADA window to duplicate an ADA requirements record. If your company has multiple positions with the same ADA physical requirements, you can duplicate an ADA physical requirements record.

To duplicate an ADA requirements record:
1.	Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Enter or select a position code and choose ADA. The ADA Physical Requirements window will open.
3.	Choose Duplicate to open the Duplicate ADA window.
4.	Select the position to which you want to copy the ADA requirements.
5.	Choose Duplicate. A message will be displayed. Choose OK and close the Duplicate ADA window.

Linking courses to a position code
Use the Position Course Link window to link courses to a position code. You also must mark Course as the position training link in the Human Resources Preferences window to link courses to position codes. 

Before you can link a course to a position code, you must first set up the course and assign an ID to it. 

To link courses to a position code:
1.	Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Enter or select a position code and choose Training to open the Position Course Link window. Courses that have been defined are displayed in the window.
3.	Select a course ID to link to this position; a black dot appears next to the course 
ID. To select all courses, choose Mark All. To unmark all courses, choose UnMark All.
4.	Choose Print to print the HRP Position Classes report.
5.	Choose OK. The Position Setup window is displayed.

Linking classes to a position code
Use the Courses Available to Link window to link classes to position codes. You also must mark Class as the position training link in the Human Resources Preferences window to link classes to position codes.

Before you can link a class to a position code, you must first set up the class and assign an ID to it. Refer to Setting up a training class on page 102 for more information.

To link classes to a position code:
1.	Open the Position Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Enter or select a position code and choose Training to open the Courses Available to Link window.
3.	Select a course and choose the zoom button to open the Position Class Link window.
4.	Select a class ID to link to this position. A black dot appears next to the class ID. 
5. To select all classes, choose Mark All. To unmark all classes, choose UnMark All.
6.	Choose Print to print the HRP Position Classes report.
7.	Choose OK. The Courses Available to Link window is displayed.
8.	Choose OK.

**Setting up a supervisor record**
Use the Supervisor Setup window to set up a supervisor record. You can set up a supervisor record and assign the record of an individual to the position.
To set up a supervisor record:
1.	Open the Supervisor Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Supervisor)
2.	Enter the code and description of the supervisor.
3.	Enter or select the employee ID of the employee that holds this supervisor position.
4.	Choose Save. Continue entering codes for all your supervisors.
5.	Choose File >> Print to print a Supervisor Codes List to verify your information.


### Chapter 3: Position  Control Setup

You can use position control to plan the positions that you will have in your organization and to track the funding sources for those positions.

Position control is optional. For companies other than the sample company, you use registration to activate it. Position control is especially useful for state and local governments, schools, and other organizations that depend on public funding.

You can create one current position plan and an unlimited number of other position plans. The other position plans are used for future planning and what-if scenarios.
You also can import position plans from Microsoft Excel. You can set up fund account information to specify the general ledger accounts that are affected during payroll processing for employees who hold a seat for a position.


## Positions, position seats, and position plans
A position is a role in an organization, such as a teacher. Each position can have attributes such as a location, division, vacation and sick time, benefits, and pay codes. These attributes are rolled down to employee records through a process called inheritance. You can make changes to the position and automatically apply those changes to multiple employees. 

Each position can have multiple instances, called position seats. A school district might plan to hire five teachers, so there would be five seats. A seat can be filled by one employee at a time.

With position control, you can create one current position plan that represents the positions that your organization has at the present time. You can also create an unlimited number of other position plans. The other position plans are used for future planning and what-if scenarios. A position plan is identified by a position plan code. 
Position budgets, seat budgets, and fund sources

A position budget represents the budgeted amount of an employer’s expense for a position, for a period of time. You can budget a certain amount of money for expenses related to a position for a period of time. You can also assign funding sources to the budget, with each source representing a percentage of the total. A funding source might be a grant or other allocation of funds from another organization. For example, a school might receive a grant to fund a teacher’s aide position that did not previously exist in your organization. 

A seat budget represents the budgeted amount of an employer’s expense for a seat, for a period of time. You can also assign funding sources to the budget, with each source representing a percentage of the total. For example, a school might receive a grant to fund an additional three seats of the teacher’s aide position. 

## Position control effects on payroll processing
Position control affects the way that payroll transactions are processed in the following ways: 
•	By removing transactions that do not fit the criteria for the *CURRENT position plan. This helps to ensure that you do not pay employees for positions that are not part of the position plan.
•	By updating pay rates based on seat detail records. This helps to ensure that employees are paid the correct amount based on the position seat that they are assigned to. For example, if an employee is temporarily assigned to a seat that pays more than their regular pay rate, the employee can be paid at the higher rate.

## Removing transactions
Payroll transactions for employees are removed from pay runs in the following situations:
•	There was a problem with the inheritance process and information was not completely copied from the position and seat to the employee record.
•	The employee is not assigned to a seat detail record for the position that is assigned to the payroll transaction.
•	The assignment status is On Hold without Pay and Benefits for the seat detail record for the employee.
•	The assignment status is Expired for the seat detail record for the employee.
•	The payroll transaction date is outside the start date and end date range for the seat detail record.
•	The seat is inactive.
 
## Updating pay rates based on seat detail records
Pay rates can be based on the seat detail records regardless of whether you enter the transactions in the Payroll Transaction Entry window or the Mass Payroll Transaction Entry window.
The pay rates from the seat detail records override the pay rate from the Employee Pay Code Maintenance window when a payroll build is processed, if the following conditions are met:
•	The Seat option is selected in the Pay Rate Based On field in the Position Seat Detail window.
•	The employee is assigned to the seat.
•	The payroll transaction date is between the start date and end date for the seat assignment.
•	The pay code is the primary pay code for the position, or a pay code that is based on a primary pay code. For example, if the primary pay code is Hourly, the related Overtime pay code is also overridden.
•	The frequency of the pay code in the Position Seat Detail window matches the frequency of the pay code in the Employee Pay Code Maintenance window. For example, if the pay code is a weekly amount in one window, it must be weekly in the other window.


## Fund account effects on payroll processing
Typically, when payroll checks are calculated, the payroll posting accounts that are specified in the Posting Account Setup window are used. If you are using position control, the payroll check calculation process also uses the fund accounts that are specified in the Position Budget Fund Sources window. The segments from these accounts can be combined dynamically to determine the posting accounts that are actually used. This enables you to override the payroll posting accounts for a period of time, and then easily revert to the original posting accounts. 

For example, you receive a grant to build a park, and the project is expected to last for four months. You can set up a fund source and fund account for the positions that are included in the grant, and then use the Fund Account Options to specify the source of the account segments that are used to generate the posting accounts that are used for payroll processing. In this example, you would create a budget schedule and corresponding fund source for the four-month period of the park project. When the four-month time frame has elapsed, the system will automatically stop allocating funds to the grant associated with the park project.

You can specify the source of account segments for the following expense pay types:
•	Gross Pay
•	Benefits Expense
•	Taxable Benefits Expense
•	Employers Tax Expense - FICA/Medicare
•	Employers Tax Expense - FICA/Social Security


## Setting up position control
If you are using position control, use the Position Control Setup window to select budget override options for permanent seats, temporary seats, full-time equivalents (FTEs), and employer expenses, and whether to save override information to history. Your selections in this window apply when a change is made that would cause the actual employer expense for a position to exceed the budgeted employer expense for the position. You can also specify whether unassigned positions are included when making payroll builds.


## To set up position control:
1.	Open the Position Control Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Control)
2.	Choose budget override options for permanent seats, temporary seats, FTEs, and employer expenses.

The following options are available.
Override option	Description
--Allowed	Allows you to exceed budget amounts without any warning.
--Warning	Allows you to exceed budget amounts, but provides a warning.
--Password Required	Requires you to enter a password to exceed budget amounts.
--Not Allowed	Does not allow you to exceed budget amounts.

3.	Choose whether to allow, disallow, or issue a warning before including employees with no seat assignments in payroll builds.
4.	Mark the Save Changes to History option to save the budget override changes to history.
5.	Mark the Enable Position Control in Sample Company option if you want to use position control in the sample company, Fabrikam, Inc. 
You must restart Microsoft Dynamics GP for the change to take effect.
6.	Choose OK to save changes.

## Setting up position plan codes
Use the Position Plans window to create plan codes. You can create multiple position plans with varying configurations of position codes, departments, and so on. Once you have set up at least one position plan, you can copy it to use as the basis for other position plans.

To set up position plan codes:
1.	Open the Position Plans window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Plans)
2.	Enter a code that identifies the plan and a description.
3.	Enter starting and ending dates for the plan.
4.	You can mark Inactive if you want to make the plan inactive. You cannot make the current plan inactive.
5.	You can choose Make Current to make the selected plan the current plan. 
If you print a report during this process, and if the plan has any inactive employees assigned to the position seats, the report will display the plan information for inactive employees only.
6.	To base a new plan on an existing plan, select the existing plan and choose Copy. In the Copy Plan window, enter an ID and description for the new plan and choose Copy.
When you copy a plan, all details of the plan are copied, including details for each employee that's included in the plan.
7.	You can choose the Excel button to either export the plan information to an Excel workbook or to import it from an Excel workbook.
8.	Choose OK to save your entries.


## Importing a position plan from Microsoft Excel
You can import plan information from a Microsoft Excel workbook into an existing Microsoft Dynamics GP plan, or into a newly created Microsoft Dynamics GP plan.

**NOTE** If you choose to import the Microsoft Excel plan workbook into an existing Microsoft Dynamics GP plan, the existing information in the Microsoft Dynamics GP plan will be overwritten with the information from the workbook.

The workbook that you import must use the correct format. To create a workbook that uses the correct format, generate Excel-based export reports for an existing plan and then use those reports as the basis for your new workbook. 

## To import a position plan from Microsoft Excel:
1.	Open the Position Plans Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Plans)
2.	Select the position plan that you want to import data to.
3.	Choose Excel and select Import from Excel to open the Welcome to the Plan Wizard for Excel window.
4.	Choose Next to open the Excel File Selection window.
5.	Enter or select the name of the Excel file to import.
6.	Choose Next to open the Completing the Plan Wizard for Excel window.
7.	Choose Finish to complete the import process.

## Setting up a position code for a position plan
Use the Position Setup window to set up a position code. A position is a defined role within a company. You can create multiple positions for a single position plan. 

To set up a position code for a position plan:
1.	Open the Position Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Select a plan code.
3.	Enter a code that identifies the position, and a description. Choose the notes button to add additional comments.
4.	Enter or select a department code for this position.
5.	Enter information about the position. 
6.	Choose Employee Details to assign default position attributes. 
7.	Choose Accounts to assign default general ledger posting accounts for the current position/plan combination. 
8.	Choose Vac/Sick to set up default accrual vacation and sickness information for the current position/plan combination. 
9.	Choose Budget/Wage to assign the position budget and wage information. 
10.	Choose Save.

## Copying an existing position for a position plan
If you are using position control, you can use the Copy Position window to copy the information from an existing position/plan combination to a new position/plan combination.

To copy an existing position for a position plan:
1.	Open the Copy Position window. (Microsoft Dynamics GP menu >> Tools >> Utilities >> Human Resources >> Copy Position)
2.	Select a position plan code.
3.	Enter or select an existing position code.
4.	Enter a new position code. You cannot select a position code that exists in the selected plan.
5.	Enter a description of the new position code.
6.	To include pay codes, benefits, and seat information in the new position, select the respective check boxes. To include the funding sources information, select Budget Schedules and Funding Sources.
7.	Choose Copy to copy the existing position information to the new position record.

## Setting up position seats
If you are using position control, you can use the Position Seats window to create and assign multiple seats to an existing position/plan combination. You can indicate whether a seat is a permanent type or a temporary type.

To set up position seats:
1.	Open the Position Seats window. (Cards >> Human Resources >> Position Control >> Position Seats or   Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Seats)
2.	Select a plan code.
3.	Enter or select a position code.
4.	Select whether to display permanent or temporary position seats in the scrolling window.
5.	You can mark the Show Inactive check box to view both active and inactive plan codes.
6.	In the scrolling window, create a new record for the seat. The value in the Seat field automatically will take the next available whole number. 
7.	Enter a description for the position seat.
8.	Enter the standard number of hours the employee works per year. For example, if the employee works 40 hours per week for 50 weeks per year, enter 2000.
9.	Enter a FTE (full-time equivalency) value to determine the pay rate for the employee assigned to the selected position seat.
10.	To enter a budget amount for the employer’s expense that is associated with the selected seat, choose the Employer Expense - Seat expansion button. 
11.	Choose OK to save the position seat information.


## Assigning employees to position seats
If you are using position control, you can use the Position Seat Detail window to assign an employee to each seat. However, you cannot add or change employee assignments if the seat is inactive.

You can assign a substitute employee to a seat when the assignment status of the employee has the following values: On Hold with Pay and Benefits; On Hold Without Pay and Benefits; or Available.

## To assign employees to position seats:
1.	Open the Position Seats window.  (Cards >> Human Resources >> Position Control >> Position Seats) 
2.	Select a plan code and a position code.
3.	Choose the Seat expansion button to open the Position Seat Detail window.
4.	Enter or select an employee ID to assign to the position seat.
5.	Enter the starting date and the ending date for the position seat for the selected plan.
6.	Select the position seat assignment status for the employee.

The employee ID must have an active maintenance record, and no other active seat must have this employee ID assigned to it, for the current position/plan combination.

The Primary check box is not available for the temporary position seats.

7.	If you are using pay steps, select a type of date based on which the pay step increases for the employee assigned to the position seat. The pay steps fields are active if the Use Pay Steps/Grades option is marked in the Human Resources Preferences window.
8.	Enter or select a pay step table ID.
9.	If you select Manual as the type of date for the Based Step Increases On field, enter or select the pay step or pay grade to assign to the employee.
10.	Accept the default date or enter a different date to make the selected pay step effective for the employee.
11.	Mark Seat to calculate the pay rate based on the seat information, or mark Employee Pay Code to calculate the pay rate based on the employee pay code information.
12.	Save the changes to position seat details.


## Assigning multiple pay codes to a position/plan combination
Use the Position Pay Code Assignments window to assign multiple pay codes to a position/plan combination. You can apply a pay step table to an employee’s pay code if the Use Pay Steps/Grades option is marked in the Human Resources Preferences window.

To assign multiple pay codes to a position/plan combination:
1.	Open the Position Pay Code Assignments window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Position Pay Codes)
2.	Select a plan code.
3.	Enter or select a position code from a list of position codes that belong to the selected plan code.
4.	Enter a pay code and the pay rate for the amount of pay.
5.	Select Primary Position/Seat if the selected pay code record is the primary pay code. There can be only one primary position pay code.
6.	Select Budgeted to calculate the projected employer expense for the current position. You can select this check box only if the position pay code has one of the following pay types: Hourly, Salary, Commission, or Other.
7.	Enter or select pay steps information. The pay steps fields are active if the Use Pay Steps/Grades option is marked in the Human Resources Preferences window, and the selected pay code is not based on another pay code.
8.	Choose Save. If the seats with the inheritance status Saved have any modified inheritance information, mark Yes to update the inheritance records with the position information. If the inheritance status is Completed, each active seat for the current position is updated to Changed status.

## Assigning default employee attributes to positions
Use the Position Employee Information window to assign position attributes such as division, location, employee type, and so on to employees assigned to the selected position.
During inheritance, the position attributes will be copied to the employee card.
To assign default employee attributes to positions:
1.	Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Select or enter a plan code and a position code. Choose Employee Defaults to open the Position Employee Information window.
3.	Enter or select a division, location, and supervisor for the employee.
4.	Select an employment type and an employment class.
5.	Enter or select the code for the workers’ compensation classification that applies to the employee.
6.	Indicate whether you want to post the next pay for the employees in the class, to a cash account from the checkbook used for each pay run, or to an account specified for each employee.
7.	Mark Calculate Minimum Wage Balance if this employee must be paid at least the minimum wage when their regular wage plus tips does not equal the minimum wage.
8.	Enter or select the name of the employee’s union.
9.	Enter the employee’s union contract number.
10.	Enter the starting date and the ending date of the contract period.
11.	Enter the amount the employee pays as union dues.
12.	Choose OK to save the position attributes.

## Assigning default posting accounts for positions
Use the Position Accounts Assignment window to assign default general ledger posting accounts for the selected position/plan combination. You cannot edit the position account information if the department code is not assigned.

To assign default posting accounts for positions:
1.	Open the Position Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Select or enter a plan code and a position code and choose Accounts to open the Position Accounts Assignment window. You can view the information for the selected position/plan combination.
3.	Select the position accounts for the gross wages, benefits expense, worker’s compensation tax expense, taxable benefits expense, and employer’s tax expense account types.
4.	Choose OK to save the account information.


## Setting up position vacation and sickness accrual
Use the Position Vacation and Sick Accrual Setup window to assign the default accrual vacation/sickness setup information for the current position/plan combination.

To set up position vacation and sickness accrual:
1.	Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Select or enter a plan code and a position code, and choose Vacation/Sick to open the Position Vacation and Sick Accrual Setup window.
3.	Select the position and department for the employee.
4.	Select Accrue Vacation to accrue vacation time for the employee automatically.
5.	Mark Hours Worked if the employee accrues vacation based upon hours worked. Mark Set Hours if the employee accrues vacation time by a specific amount per pay period.
6.	If you marked Hours Worked, enter the number of vacation hours the employee should receive each year. If you marked Set Hours, enter the number of vacation hours the employee should receive each pay run.
7.	Select Accrue Sick Time to accrue sick time for the employee automatically.
8.	Mark Hours Worked if the employee accrues sick time based on hours worked. Mark Set Hours if the employee accrues sick time by a specific amount per pay period.
9.	If you marked Hours Worked, enter the number of sick time hours the employee should receive each year. If you marked Set Hours, enter the number of sick time hours the employee should receive each pay period.
10.	Choose OK to save the position vacation and sickness accrual information.

## Setting up position budget and wage information
Use the Position Budget and Wage Information window to set up the position budget and wage information.

To set up position budget and wage information:
1.	Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2.	Select or enter a plan code and a position code, and choose Budget/Wage to open the Position Budget and Wage Information window.
3.	Enter a percentage of the calculated rate to calculate the benefit.
The system calculates an amount for wages that have not been paid by using the pay codes for the position. The resulting amount is multiplied by the percentage you enter here. That amount is then added to the calculated wage amount to calculate the actual cost for the position.
4.	Enter the benefit amount per day. This amount is added to the actual cost of the position. The time period is calculated based on the number of days that a position seat detail record has an employee ID assigned with a seat assignment status of either Assigned or On Hold with Pay and Benefits.
5.	Enter the tax expenses and tax amount.
6.	Enter the number of budgeted permanent seats and budgeted temporary seats.
7.	Enter an FTE (full-time equivalency) value to make sure the position is not overfilled. For example, you might intend to have four half-time positions. To ensure that the seats are not filled with full-time employees, you would set the budgeted FTE value to 2.0.
8.	Choose OK to save the position budget and wage information.

## Setting up position budget schedules and fund sources
Use the Position Budget Schedule window to create budget schedules and to assign them to a specific position/plan combination. You can specify date ranges for the budget schedules.

Use the Position Budget Fund Sources window to assign multiple fund sources to budget schedules for a position. You can specify a percentage amount for each fund. The sum of all fund percentages must add up to 100.

To set up position budget schedules and fund sources:
1.	Open the Position Budget Schedule window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position Control >> Budget Schedules)  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position >> Budget/Wage >> Employer Expense expansion)
2.	Select a plan code and a position code to assign a budget schedule for.
3.	Enter the starting date and the ending date of the period range for the budget schedule.
4.	Enter a description for the budget schedule.
5.	Enter the budget amount. This amount should include the total amount of pay, benefits, and taxes for the time period that you specified in step 3.
6.	Choose the Amount expansion button to open the Position Budget Fund Sources window. 
7.	Enter or select an account.
8.	Enter identification for the fund source and a percentage for the fund.
9.	The Amount field displays the fund amount as a percentage of the budget amount.
10.	Choose OK to save the fund sources information and close the Position Budget Fund Sources window.
11.	Save the budget schedule information and choose OK to close the Position Budget Schedule window.

## Setting up fund account options
Use the Fund Account Options window to specify the source for general ledger account segments for general ledger posting accounts. You can assign the general ledger account segments either from the position budget fund source or from the payroll posting account setup.
You can specify the expense payroll types that posting accounts are updated for during the payroll processing.

To set up fund account options:
1.	Open the Fund Account Options window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >>  Position Control >> Fund Account Options)
2.	Select whether the source of General Ledger account segments is the Payroll Posting Account Setup or the Budget Fund Source.
3.	Select the expense payroll types.
4.	Save the fund account options information and close the window.

Setting up seat budget schedules and fund sources
Use the Position Seat Budget Schedule window to create budget schedules and to assign them to a specific position seat. You can specify date ranges for the budget schedules.
Use the Position Seat Budget Fund Sources window to assign multiple fund sources to budget schedules for a position seat. You can specify a percentage amount for each fund. The sum of all fund percentages must add up to 100.

To set up seat budget schedules and fund sources:
1.	Open the Position Seat Budget Schedule window.  (Cards >> Human Resources >> Position Control >> Budget Schedules)
2.	Select a plan code, position code, and seat to assign a budget schedule for the position seat.
3.	Enter the starting date and the ending date of the period range for the budget schedule.
4.	Enter a description for the budget schedule.
5.	Enter the budget amount per day.
6.	Choose the Budget Amount expansion button to open the Position Seat Budget Fund Sources window. Enter or select an account.
7.	Enter identification for the fund source and a percentage for the fund.
8.	The Amount field displays the fund amount as a percentage of the budget amount.
9.	Choose OK to save the fund sources information and close the Position Seat Budget Fund Sources window.
10.	Save the budget schedule information and close the Position Seat Budget Schedule window.

