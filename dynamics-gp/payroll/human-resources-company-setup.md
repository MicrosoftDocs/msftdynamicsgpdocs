---
title: "Human Resources - Company Setup and Organizational Structure"
description: "Learn about setting up the company information for the Human Resources functionality in Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: jswymer
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 03/10/2021
---
# Human Resources - Company Setup and Organizational Structure

Your company's organizational structure might include multiple levels, such as divisions, departments, positions, supervisors, and locations. You can create these levels and store additional information for each level in the Human REsources functionality of [!INCLUDE [prodshort](../includes/prodshort.md)].

A division is a branch of a company, usually including several departments. A department is a specialized portion of a division or company, which usually concentrates on one type of task. You'll use several windows to enter the various types of organizational information for your business. Some companies conduct business from more than one site or location and each site has a different address.

Each position has certain physical requirements. The Americans with Disabilities Act (ADA) prohibits employers from discriminating against qualified individuals with disabilities. Use the Position Setup window to enter employee positions, and use the ADA Physical Requirements window to define the physical requirements for each position.

Many positions require special skills and training and you can link training courses and classes to position codes. You can use the Position Course Link window and the Courses Available to Link window to link skill and training requirements to position codes.

You can use position control to plan future positions and roll down information from the planned positions and position seats to employees. Position control is optional.  

Use the Company Human Resources Setup window to set up company human resources information, such as the type of business and Standard Industrial Classification (SIC), Dun & Bradstreet (DUNS), North America Industry Classification System (NAICS), and Vets-100 numbers. You can set up human resources information for each company.

To set up company human resources information:

1. Open the Company Human Resources Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Company >> Company >> Human Resources button)
2. Enter the type of business and the SIC number for this company. 
3. Enter the DUNS number and Vets-100 number for this company.
4. Choose OK to save your changes.

## Setting up an operating procedure

Use the Operating Procedures Setup window to set up an operating procedure. You can use the OLE (Object Linking and Embedding) Container to attach files created in other applications.  

### To set up an operating procedure

1. Open the Operating Procedures Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Operating Procedures)
2. Enter a category name that describes the operating procedure.
3. Enter the operating procedure information.
Choose the paperclip button to open the OLE (Object Linking and Embedding) container and store additional information. 
4. Choose Save.

## Setting up a division code

Use the Division Setup window to set up a division. A division is an organizational level between a company and a department. A company can have several divisions, and each division can have several departments. You also can add information using extra fields. 

### To set up a division code

1. Open the Division Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Division)
2. Enter a name that identifies the division and a code or accept the default code.
3. Enter an address, city, state, and postal code for this division.
4. Enter a phone number, fax number, and e-mail address for this division.
5. Choose Extra Fields to open the Division Extra Fields window. For more information, refer to Setting up organizational extra fields on page 105.
6. Choose Save.

## Setting up a department code

Use the Department Setup window to set up a department code. A department is a specialized unit of a division or company, which usually concentrates on one type of task. For example, accounting and purchasing are typical departments. You can use up to six letters and numbers to create a department code. You also can add information using extra fields. 

### To set up a department code

1. Open the Department Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Department)
2. Enter a code that identifies the department and a description.
3. Choose Extra Fields to open the Department Extra Fields window.
4. Choose Save.

## Setting up a position code

Use the Position Setup window to set up a position code. A position is a defined role within a company. You can create multiple positions for a single position plan. You can link training courses and specify which skill sets, if any, are required for a position. You also can link pay codes and Americans with Disabilities Act (ADA) physical requirements to a position code.

If your company uses salary matrices, you can link the low, middle, and high salaries for each position to a position code. You also can add information using extra fields. 

### To set up a position code

1. Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)

    If you are using Position control, the window has the following appearance.  

2. Enter a code that identifies the position, and a description. Choose the notes button to add additional comments.
3. Select an Equal Employment Opportunity (EEO) class and a Fair Labor Standards Act (FLSA) status.
4. Enter or select a position the individuals in the position report to.
5. Enter or select the review type to be used for employees in this position and enter or select a required skill set.
6. Enter a description of the position in the Position Description field.

    Choose the paperclip button to open the OLE (Object Linking and Embedding) container and store a position description file.

7. Choose Linked Pay Codes to open the Position \ Pay Code Setup window and link pay codes and salary ranges to this position code. 
8. Choose ADA to open the ADA Physical Requirements window.  
9. Choose Training to open the Courses Available to Link window.  
10. Choose Extra Fields to open the Position Extra Fields window.  
11. Choose Save.

## Setting up a location code

Use the Company Addresses Setup window to set up a location code, which includes an address, phone numbers, and a contact person for each location. If your company has multiple sites, you can track which employees are working from which sites by setting up location IDs.

### To set up a location code

1. Open the Company Addresses Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Location)
2. Enter an identification and name for the company's location.
3. Enter contact, address and phone information.
4. Choose Address ID Internet to enter or view Internet information for this address. 
5. Choose Save.

## Setting up company Internet information

Use the Internet Information window to track Internet-related information about your company, such as e-mail addresses, Web page URLs, and FTP sites. If you've set up multiple addresses for your company, you can track Internet information for each address.

### To set up company Internet information

1. Open the Internet Information window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Company >> Internet Information)
2. Select a company in the Select Information for field.
The company you're currently logged in to is displayed in the Company ID field.
3. Enter or select an address in the Address ID field.
4. Enter Internet information.
5. Choose Save to save your entries.
6. To print Internet information for the current company, choose File >> Print or the printer button. The Internet Information Report is printed, showing Internet information for the current company.
To print an Internet Information Report showing Internet information for all companies, use the Company General Report Options window. 

## Linking pay codes to a position code

Use the Position and Pay Code Setup window to link pay codes to a position code.
If you marked the Auto Create Position/Pay Code links option in the Human Resources Preferences window, you do not need to link pay codes to a position code manually with this procedure.

### To link pay codes to a position code

1. Open the Position\Pay Code Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Position and Pay Code)
2. Enter or select a position code.
3. Enter or select a pay code and choose the Salary Range lookup button. The Salary Matrix Lookup window will open.
4. Select a table.
5. Select a salary to use as the low salary indicator and choose the Low select button.
6. Select a salary to use as the middle salary indicator and choose the Medium select button.
7. Select a salary to use as the high salary indicator and choose the High select button.
8. Choose Select to display the salary information in the Position\Pay Code Setup window.
9. Choose Save.

## Understanding pay steps

Before you can begin using the pay steps feature, you need to activate it in the Human Resources Preferences window. The pay steps feature integrates with U.S. Payroll, but is not available with Canadian Payroll.

You can use pay steps to associate an employee's amount of time in a position with a rate of pay. A pay step table lists pay steps (or grades) by number, the assigned duration of each step, and the dollar amounts for each step under successive effective dates.

For example, after an employee has served in a position for the full duration of a pay step, the employee advances to the next pay step and its corresponding pay rate under the current effective date. When the next effective date arrives, the employee advances to the new pay rate for the current pay step.
The following illustration is an example of a pay step table.

When you assign an employee and an associated pay code to a pay step table (in the Employee/Pay Step Table Entry window or the Employee Pay Code Maintenance window), you can base the step increases on the employee's hire date, adjusted hire date, seniority date, or a manually entered date.

The Payroll system creates post-dated pay rates for the future increases indicated in the pay steps table. A reminder on your Microsoft Dynamics GP home page lists employee post-dated pay rates eligible for activation. After you activate an employee's post-dated pay rate, it becomes effective, on the designated date, for all future pay periods.
To use the example illustration: assume that the step increases are based on the hire date, and that the pay rates are activated. If the employee was hired on July 25, 2006, and the current date is May 25, 2007, the employee would be in pay step 1, with a pay rate of $20.00. On July 25, 2007, the employee would advance to pay step 2, with a pay rate of $25.00. On January 01, 2008, the next column of pay rates would become effective, and the employee's pay rate would advance to $26.00.

You can use multiple pay step tables to associate pay rates with other employee qualifications, such as education, in addition to time in a position. For example, if you base employee pay rates, in part, on education level, you can create a pay step table for "Bachelor's Degree" and another for "Master's Degree."

You can use the Microsoft Dynamics GP system's Activity Tracking feature to monitor pay step table additions, changes, and deletions. Select either the activity type Access Tracking, or Field Tracking. For more information about Activity Tracking, refer to the System Setup documentation.

## Setting up pay step tables

You can create, save, modify, and delete pay step tables. In the Pay Step Table Entry window, you can create pay step tables having as many steps, number of months in each step, and effective dates, as you want. You can also enter past effective dates to record historical pay rate information.

You can export pay step table information to a Microsoft Excel&reg; file, for further analysis and review.

Within a pay step table, you can add, copy, and delete columns, and delete rows.
For more information about changing and using a pay step table after you set it up, see Modifying or deleting pay step table data on page 28 and Assigning a pay step table to employees on page 185.

### To set up a pay step table

1. Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2. Enter a pay step table ID and a short description.
3. Select a unit of pay, either Hourly Rate or Salary.
4. Enter the effective date. This date indicates when a new column of pay rates becomes effective, typically 01 January of successive years. You can enter any past, present, or future date.
5. Enter the step (or grade) number into the pay step table.
6. Enter the duration of this pay step as a range of months. For example, a range of 0 to 11 indicates that a new employee remains at this pay step for the first 12 months of employment.
7. Enter a dollar amount in the cell across from the step number and below the effective date.
8. Press the TAB key to begin a new row.
9. To add additional effective date columns, select the Add Column tab, enter a date, and choose Add.
10. Choose Save.
11. Choose Clear to remove all selections from the window.

## Modifying or deleting pay step table data

You can add and remove columns in existing pay step tables by selecting the appropriate tab. You also can copy and adjust the amounts from an existing column to create a new column in the same table. See Setting up pay step tables on page 27.

You cannot change or delete pay step data in columns with effective dates earlier than the user date. Such data is preserved as historic data.

### To add a column

1. Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2. Select a pay step table ID.
3. Choose the Add Column tab. 
4. Enter the effective date.
5. Choose Add to add the new column to the table.
6. Choose Save.

### To copy a column

1. Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2. Select a pay step table ID.
3. Choose the Copy Column tab.
4. Select the effective date of the pay step column you are copying.
5. Enter or select the effective date of the column you are creating.
6. Enter the amount or percentage of adjustment to apply to the copied amounts.
7. Choose Copy to create the new column.
8. Choose Save.

### To remove a column

1. Open the Pay Step Table Entry window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Pay Step Table)
2. Select a pay step table ID.
3. Choose the Remove Column tab.
4. Select the effective date of the pay step column you are removing.
5. Choose Remove.
6. Choose Save.

## Adding an ADA physical requirements record

Use the ADA Physical Requirements window, the ADA Physical Requirements Page 2 window, and the ADA Physical Requirements Page 3 window to add an ADA physical requirements record. The Americans with Disabilities Act (ADA) prohibits employers from discriminating against qualified individuals with disabilities.

### To add an ADA physical requirements record

1. Open the Position Setup window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Enter or select a position code and choose ADA. The ADA Physical Requirements window will open.
3. Enter a description of the position in the Job Purpose field and mark the appropriate requirements for this position.
4. Choose the page turn button to open the ADA Physical Requirements Page 2 window and mark the appropriate requirements.
5. Choose the page turn button to open ADA Physical Requirements Page 3 and mark the appropriate requirements for the position.
6. Choose Save. The ADA Physical Requirements window is displayed.
7. Close the window.

## Duplicating an ADA requirements record

Use the Duplicate ADA window to duplicate an ADA requirements record. If your company has multiple positions with the same ADA physical requirements, you can duplicate an ADA physical requirements record.

### To duplicate an ADA requirements record

1. Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Enter or select a position code and choose ADA. The ADA Physical Requirements window will open.
3. Choose Duplicate to open the Duplicate ADA window.
4. Select the position to which you want to copy the ADA requirements.
5. Choose Duplicate. A message will be displayed. Choose OK and close the Duplicate ADA window.

## Linking courses to a position code

Use the Position Course Link window to link courses to a position code. You also must mark Course as the position training link in the Human Resources Preferences window to link courses to position codes.  

Before you can link a course to a position code, you must first set up the course and assign an ID to it.  

### To link courses to a position code

1. Open the Position Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Enter or select a position code and choose Training to open the Position Course Link window. Courses that have been defined are displayed in the window.
3. Select a course ID to link to this position; a black dot appears next to the course 
ID. To select all courses, choose Mark All. To unmark all courses, choose UnMark All.
4. Choose Print to print the HRP Position Classes report.
5. Choose OK. The Position Setup window is displayed.

## Linking classes to a position code

Use the Courses Available to Link window to link classes to position codes. You also must mark Class as the position training link in the Human Resources Preferences window to link classes to position codes.

Before you can link a class to a position code, you must first set up the class and assign an ID to it. Refer to Setting up a training class on page 102 for more information.

### To link classes to a position code

1. Open the Position Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
2. Enter or select a position code and choose Training to open the Courses Available to Link window.
3. Select a course and choose the zoom button to open the Position Class Link window.
4. Select a class ID to link to this position. A black dot appears next to the class ID. 
5. To select all classes, choose Mark All. To unmark all classes, choose UnMark All.
6. Choose Print to print the HRP Position Classes report.
7. Choose OK. The Courses Available to Link window is displayed.
8. Choose OK.

## Setting up a supervisor record
Use the Supervisor Setup window to set up a supervisor record. You can set up a supervisor record and assign the record of an individual to the position.

### To set up a supervisor record

1. Open the Supervisor Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Supervisor)
2. Enter the code and description of the supervisor.
3. Enter or select the employee ID of the employee that holds this supervisor position.
4. Choose Save. Continue entering codes for all your supervisors.
5. Choose File >> Print to print a Supervisor Codes List to verify your information.

## See also

[Human Resources - Position Control Setup](human-resources-position-control.md)  
[Human Resources in Microsoft Dynamics GP](HumanResource.md)  
