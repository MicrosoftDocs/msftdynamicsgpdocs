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
ms.date: 10/14/2021
---
# Human Resources in Microsoft Dynamics GP

You can use Human Resources to set up, enter, and maintain most of your employee  management needs and to track organizational details and personal information for employees within your company. You also can use Human Resources to view important information about employees, their benefits, and other historical data.

You also can use Human Resources to complete the following tasks:

- Manage the interviewing and hiring of applicants, track the termination, training, and evaluation of employees, and maintain organizational details, such as the supervisor, position, and department assignment of employees

- Create company benefit plans—complete with employee and employer deduction provisions, enroll employees and their dependents in benefits, and calculate the benefit value

- Enter employee attendance information, including creating attendance transactions and tracking planned absences for employees

- Define vacation and other time accruals tracked in your organization and how employees can earn time accruals, then set up schedules to show how employees can earn the time accruals at various rates

- Monitor the distribution of company property, such as laptop computers and cell phones, to employees

If you are using U.S. Payroll, you can enter and maintain your employee information in Human Resources and those transactions automatically will update your payroll records.

In this article, we describe the system setup and how to define Human Resources preferences. For information about how to configure the company, see [Human Resources - Company Setup](human-resources-company-setup.md).  

If you are setting up Human Resources in the absence of Payroll, after setup you must modify user security settings to enable user access to Human Resources
functionality.  

## Human Resources preferences

You can specify default employee numbers for your organization by entering an employee ID in the Human Resources Setup window.  

You can choose to have Human Resources automatically assign employee IDs and increase the employee ID number by one for each new record in the Employee Maintenance window.

You can customize the way Human Resources works for your organization by specifying preferences in the Human Resources Preferences window. The user preferences you select will be applied to all the companies within your organization. You also can set up user access to employee information by divisions and departments.

Use the Human Resources User Preferences window to indicate which window should be displayed when you start Human Resources and choose to display employee information by descriptions or codes in the Employee Maintenance window.

This information is divided into the following sections:

- *Setting up an employee number*

- *Setting up Human Resources preferences*

- *Setting up user access to employee information*

- *Copying user access to employee information*

- *Setting up Human Resources user preferences*

## Setting up an employee number

Use the Human Resources Setup window to assign default employee IDs automatically. Each time you add a new employee in the Employee Maintenance
window, the default number will increase by one to the next available number as each number is accepted.

If you are registered for Payroll, the same settings in the Payroll Setup window will be updated with your settings in the Human Resources Setup window.

> [!NOTE]
> If you use Dynamics GP on a network where more than one person is entering new employee records at the same time, the default number might appear to increase by two or more.

### To set up an employee number

1. Open the Human Resources Setup window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Human Resources \>\> Human Resources)

2. Mark the Auto Assign Employee ID option to assign an employee ID for each new employee record.

3. Enter the next employee ID that will be displayed when you add a new employee record in the Employee Maintenance window.

4. Choose OK to save your changes.

## Setting up Human Resources preferences

Use the Human Resources Preferences window to set up Human Resources preferences for your organization.

### To set up Human Resources preferences

1. Open the Human Resources Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\> Human Resources Preferences)

    ![the Human Resources Preferences window](media/HRPREF.jpg)

2. Mark options for seniority dates and address changes.

    The following table describes each option.

    | **HR preference option** | **How to use this option** |
    |--|--|
    | Update seniority date with adjusted hire date | Mark to use an employee's adjusted hire date as the seniority date for calculating accruals, such as vacation and sick time. |
    | Adjusted hire date for benefits | Mark to use an employee's adjusted hire date to determine eligibility for benefits, such as health insurance and 401(k) enrollment dates. |
    | Adjusted hire date for length of service | Mark to use an employee's adjusted hire date to determine length of service on the Employee Service by Hire Date report. |
    | Address change report | Mark to track an employee's previous address. |

    Changes to the adjusted hire date in the Employee Maintenance window will update the seniority date in the Employee Attendance Maintenance window.

    > [!NOTE]
    > An adjusted hire date is a hire date that has been changed to reflect time away from the job. For example, suppose an employee leaves your company but is hired again by your company six months later. You can create an adjusted hire date that is six months after his first hire date, which is then used to determine his benefit time and benefit eligibility.

3. Mark the Purge Applicants option to automatically delete applicant records at defined intervals.

    Enter the number of days that the applicant records should remain in the system before being deleted. The Last purge date field displays the date when applicant records were last deleted.

4. Mark the Use Pay Steps/Grades option to enable the use and display of pay step information throughout Human Resources.

    Select the type of date for the basis of the pay step increase. The date options are: Hire Date, Adjusted Hire Date, Seniority Date, or Manual.

    The selected type of date becomes the default option each time you create a pay step table.

    The pay steps feature integrates with U.S. Payroll, but is not available with Canadian Payroll.

5. Select Class or Course at Position Training Links to link classes or courses to positions defined in the Position Setup window.

    You can link positions with class or course training requirements. For example, your company may require new sales staff to complete a product marketing course that consists of six monthly classes. For more information, see *Setting up a training course* and *Setting up a training class*.

6. Select EEO-1 or EEO-4 to change the options in the EEO Class list in the Position Setup window in Payroll.

7. Mark or unmark your preferences for the position, salary and pay code options.

    The following table describes each option.

    | **HR preference option** | **How to use this option** |
    |--|--|
    | Auto Create Position/Pay Code links | Mark to automatically create a link between each pay code and each position. For more information, see *Linking pay codes to a position code.* |
    | Edit Attendance Maintenance and Earnings History | Mark to allow changes to attendance information in the Employee Attendance Maintenance window and to information in the Earnings History window. |
    | Enable Reason for Pay Adjustment | Mark to automatically open the Reason for Change window when making pay adjustments. In this window, enter an effective date and reason for the salary change. |
    | Enable Cancel on Reason for Pay Adjustment | Mark to make the Cancel button available in the Reason for Change window. Unless you've marked this option, you must always give a reason for the salary change before closing the window. |
    | Ignore Position/Salary Matrix Links | Mark if you don't want a message displayed when an employee's salary is outside the salary matrix ranges or a salary matrix doesn't exist. For more information about using matrix links, see *Adding a salary matrix*. |
    | Default Employee Info to Dependent | Mark to display the employee's address and phone information in the Employee Dependents window. |

8. Mark or unmark your To Do List options.

    The To Do List window is used to view calendar information, such as employee benefit eligibility dates and orientation dates.

    | **HR preference option** | **How to use this option** |
    |--|--|
    | Roll Forward System To Do List | Mark to have the system include today's To Do List unfinished items on the next day's To Do List. |
    | Purge To Do Lists (System/Personal) | Mark to delete the To Do List items and enter the number of days that the items should remain in the system before being deleted. |

9. Mark the Enable Attendance for Canada option if you are using Canadian Payroll and want to use the attendance features in Human Resources. This option is available only if Canadian Payroll is registered.

10. Mark the Never, Always, or Ask Each Time options to automatically create and update position vacancies.

11. Mark the Never, Always, or Ask Each Time options to automatically create and update organizational requisitions.

> [!TIP]
> To select Employee Filters and User Access Duplication, refer to Setting up user access to employee information.

## Setting up user access to employee information

Use the Employee Filter Divisions window and the Employee Filter Departments window to set up user access to employee information by divisions and departments.

### To set up user access to employee information

1. Open the Human Resources Preferences window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> System >> Human Resources Preferences)
2. Mark Division and choose the expansion button to restrict user access by division. The Employee Filter Divisions window will open.
3. Mark Department and choose the expansion button to restrict user access by department. The Employee Filter Departments window will open.
4. Select a user ID. Mark divisions or departments in the Employee Filter Divisions window and Employee Filters Departments window to grant user access. To remove access, unmark a division or department.
5. Choose OK to save your changes.

## Copying user access to employee information

Use the Human Resources Preferences window to copy user access to employee information by divisions and departments from one user to another.

To copy user access to employee information:

1. Open the Human Resources Preferences window.   (Microsoft Dynamics GP menu >> Tools >> Setup >> System >> Human Resources Preferences)
2. Select a user to copy access information to in the Grant user field.
3. Choose the Like user lookup button to open the User Lookup window. Then select a user from which to copy access information in the Like user field.
4. A message gives you the option to copy the access information to the Grant user field.

## Setting up Human Resources user preferences

Use the Human Resources User Preferences window to set up Human Resources preferences for each user. You can select windows to be displayed when you start Human Resources and choose whether employee information will be displayed by descriptions or codes in the Employee Maintenance window.

To set up Human Resources user preferences:

1. Open the Human Resources User Preferences window.  (Microsoft Dynamics GP menu >> User Preferences >> HR button)
2. Indicate if you want a To Do List window to open when you start your Human Resources system.

    - Mark the Open To Do List option for the To Do List window to be displayed when you start Human Resources.
    - Mark the Open Personal To Do List option for the Personal To Do List window to be displayed when you start Human Resources.
3. Mark the Roll Personal To Do List Forward option to move personal to do list entries that aren't cancelled or finished to the next day in the to do list.
4. Select the Code option to display the organizational codes in the Employee Maintenance window. Select the Description option to display the organizational descriptions in the Employee Maintenance window.
5. Choose OK to save your changes.

## Organizational structure
Your company’s organizational structure might include multiple levels, such as divisions, departments, positions, supervisors, and locations. You can create these levels and store additional information for each level.

A division is a branch of a company, usually including several departments. A department is a specialized portion of a division or company, which usually concentrates on one type of task. You’ll use several windows to enter the various types of organizational information for your business. Some companies conduct business from more than one site or location and each site has a different address.

Each position has certain physical requirements. The Americans with Disabilities Act (ADA) prohibits employers from discriminating against qualified individuals with disabilities. Use the Position Setup window to enter employee positions, and use the ADA Physical Requirements window to define the physical requirements for each position.

Many positions require special skills and training and you can link training courses and classes to position codes. You can use the Position Course Link window and the Courses Available to Link window to link skill and training requirements to position codes.

You can use position control to plan future positions and roll down information from the planned positions and position seats to employees. Position control is optional. 

Use the Company Human Resources Setup window to set up company human resources information, such as the type of business and Standard Industrial Classification (SIC), Dun & Bradstreet (DUNS), North America Industry Classification System (NAICS), and Vets-100 numbers. You can set up human resources information for each company.

## To set up company human resources information:
1.	Open the Company Human Resources Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Company >> Company >> Human Resources button)
 
2.	Enter the type of business and the SIC number for this company. 

3.	Enter the DUNS number and Vets-100 number for this company.

## Setting up an operating procedure
Use the Operating Procedures Setup window to set up an operating procedure. You can use the OLE (Object Linking and Embedding) Container to attach files created in other applications. 

To set up an operating procedure:  
1.	Open the Operating Procedures Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Operating Procedures)
2.	Enter a category name that describes the operating procedure.
3.	Enter the operating procedure information.

## Setting up a division code
Use the Division Setup window to set up a division. A division is an organizational level between a company and a department. A company can have several divisions, and each division can have several departments. You also can add information using extra fields. 
To set up a division code:

1.	Open the Division Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Division)
2.	Enter a name that identifies the division and a code or accept the default code.
3.	Enter an address, city, state, and postal code for this division.
4.	Enter a phone number, fax number, and e-mail address for this division.
5.	Choose Extra Fields to open the Division Extra Fields window. 

## Setting up a department code
Use the Department Setup window to set up a department code. A department is a specialized unit of a division or company, which usually concentrates on one type of task. For example, accounting and purchasing are typical departments. You can use up to six letters and numbers to create a department code. You also can add information using extra fields. 

To set up a department code: 
1.	Open the Department Setup window.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Department)
2.	Enter a code that identifies the department and a description.
3.	Choose Extra Fields to open the Department Extra Fields window. Setting up a position code

## Setting up a position code
Use the Position Setup window to set up a position code. A position is a defined role within a company. You can create multiple positions for a single position plan. You can link training courses and specify which skill sets, if any, are required for a position. You also can link pay codes and Americans with Disabilities Act (ADA) physical requirements to a position code.

If your company uses salary matrices, you can link the low, middle, and high salaries for each position to a position code. You also can add information using extra fields. 
To set up a position code:

1.	Open the Position Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Position)
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

## Setting up a location code
Use the Company Addresses Setup window to set up a location code, which includes an address, phone numbers, and a contact person for each location. If your company has multiple sites, you can track which employees are working from which sites by setting up location IDs.

To set up a location code:
1.	Open the Company Addresses Setup window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization >> Location)
2.	Enter an identification and name for the company’s location.
3.	Enter contact, address and phone information.
4.	Choose Address ID Internet to enter or view Internet information for this address. 

## Setting up company Internet information
Use the Internet Information window to track Internet-related information about your company, such as e-mail addresses, Web page URLs, and FTP sites. If you’ve set up multiple addresses for your company, you can track Internet information for each address.

To set up company Internet information:
1.	Open the Internet Information window. (Microsoft Dynamics GP menu >> Tools >> Setup >> Company >> Internet Information)
2.	Select a company in the Select Information for field.
The company you’re currently logged in to is displayed in the Company ID field.
3.	Enter or select an address in the Address ID field.
4.	Enter Internet information.
5.	To print Internet information for the current company, choose File >> Print or the printer button. The Internet Information Report is printed, showing Internet information for the current company.

## Deleting an organizational code
Use the Division Setup, Department Setup, Position Setup or Company Addresses Setup windows to delete a division, department, position, or location code. You cannot delete a division code, department code, or position code that is assigned to an employee record.
To delete an organizational code:

1.	Open the Human Resources Organization Setup menu.  (Microsoft Dynamics GP menu >> Tools >> Setup >> Human Resources >> Organization)
2.	Select Division, Department, Position, or Location.
3.	Enter or select the code you want to delete.


## See also

[Human Resources - Company Setup](human-resources-company-setup.md)  
[Human Resources - Position Control Setup](human-resources-position-control.md)  
[Microsoft Dynamics GP Advanced Payroll](AdvancedPayroll.md)  
