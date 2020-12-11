---
title: "Position control"
description: "Learn about position control in Microsoft Dynamics GP."
keywords: "payroll"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 07/17/2020
---
# Position Control in Dynamics GP

You can use position control to plan the positions that you will have in your organization and to track the funding sources for those positions. Position control is especially useful for state and local governments, schools, and other organizations that depend on public funding. You can create one current position plan and an unlimited number of other position plans. The other position plans are used for future planning and what-if scenarios.  

The management of labor budgets and human resources based upon specific job functions and a specific head count is a driving force behind the position control functionality. Constraints are then applied throughout the Human Resource and Payroll system to enforce the business rules and to manage the movement of human resources throughout the organization.  

Another cool feature is *Inheritance*. Each role will have attributes such as location, division, pay, benefits etc. All these attributes can be rolled down to each employee within this position.  

## Set up position control

To set up position control:

1. In the Dynamics GP menu, choose **Tools**, **Setup**, **Human Resources**, **Position Control**, and then choose **Position Control**.
2. Choose budget override options to allow, disallow, or issue a warning before including employees with no seat assignment in payroll builds.
3. Mark the **Save changes to history** option to save budget overrides changes to history.
4. Mark the **Enable Position Control in Sample Company** option if you want to use position control in the sample company, Fabrikam, Inc.  

You must restart Dynamics GP for the change to take effect.

## Set up position plan codes

To set up position plan codes:

1. In the Dynamics GP menu, choose **Tools**, **Setup**, **Human Resources**, **Position Control**, **Position Control**, **Position Plans**, and then choose **Position plan codes**.
2. Enter a code to identify the plan and description.
3. Enter starting / end date.
4. You can mark **Inactive** if you are not ready to use this plan yet.

    You cannot make the *Current* plan inactive.
    You can choose **Make Current** to make the selected plan the current plan.  

### Assigning seats

To base a new plan on an existing plan, select the existing plan and choose Copy. In the Copy Plan window, enter an ID and description for the new plan and choose Copy. When you copy a plan, all details of the plan are copied, including details for each employee that's included in the plan.

You can choose the **Excel** button to either export the plan information to an Excel workbook or to import it from an Excel workbook.  

If you print a report during this process, and if the plan has any inactive employees assigned to the position seats, the report will display the plan information for inactive employees only.  

## Import a position plan from Excel

To import position plans:

1. In the Dynamics GP menu, choose Tools, Setup, Human Resources, Position Control, Position Control, and then choose Position Plans.  

    > [!WARNING]
    > If you choose to import the Microsoft Excel plan workbook into a plan, the existing information in the plan will be overwritten with the information from the workbook.
2. Select the plan you want to import data to.

    1. Chose **Excel**, and then choose **Import from Excel**  
    2. Choose **Next** to open the Excel file selection window
    3. Enter or select the name of the file to import
    4. Choose **Next** to open the **Completing the Plan** window
3. Choose **Finish** to complete the import

<!--Position code for a position plan
Microsoft Dynamics GP menu > Tools > Setup > Human Resources > Organization > Position

Warning: If you choose to import the Microsoft Excel plan workbook into a plan, the existing information in the plan will be overwritten with the information from the workbook.

Select the plan you want to import data to.
Chose Excel > select 'import from Excel' 
Choose Next to open Excel file selection window
Enter or select the name of the file to import
Choose Next to open the Completing the Plan window
Choose Finish to complete the import
-->
