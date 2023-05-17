---
title: "Advanced Human Resources Inquiries and Reports"
description: "Examine the inquiries and reports in the advanced human resources functionality for Dynamics GP."
keywords: "HR"
author: theley502
manager: jswymer
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 04/23/2019
---

# Advanced Human Resources in Microsoft Dynamics GP - Inquiries and Reports

Advanced Human Resources provides both Inquiry windows and the ability to
print reports. The Inquiry windows for the most part are the history windows
for most of the components. The exception to this is the Percent Current
Inquiry, which is an inquiry allowing for various selections to be made to
narrow or broaden the scope of records shown.

## Inquiries

The Advanced Human Resources Inquiries contain the history windows for
Certification, License and Training Manager, as well as the inquiry for
Percent Current. The information on the windows can be printed from the
window. In the case of the Percent Current Inquiry, both the information on
the screen and a Percent Current Totals report can be printed using the
printer icon on the window.

### Certification History

Use the Certification History window to view all the activity for a specific

Employee/Certification record. The history record is written as the latest
History record when changes are saved on the Certification Entry window.

To open the Certification History window, click the **HR and Payroll**
series button, click **Human Resources** on the Inquiry content pane and
then click **Certification History**.

Enter or select an **Employee ID**. The **Department** and **Position**
fields displays from the Employee Maintenance window.

Enter or select a **Certification Code** for current Employee.

The **Inactive** checkbox will inactivate the current Certification History.

### License History

Use the License History window to view all the activity for a specific

Employee/License record. The history record is written as the latest History
record when changes are saved on the License Entry window.

To open the License History window, click the **HR and Payroll** series
button, click **Human Resources** on the Inquiry content pane and then click
**License History**.

1. Enter or select an **Employee ID**. The **Department** and **Position** fields displays from the Employee Maintenance window.

2. Enter or select a **License Number** for the current Employee.

The **Inactive** checkbox will inactivate the current License History.

### Training History

Use the Training History window to view all the transactions by Course/Class
ID for a specific employee. The history record is written as the latest
History record when changes are saved on the Employee Training window.

To open the Training History window, click the **HR and Payroll** series
button, click **Human Resources** on the Inquiry content pane and then click
**Training History**.

<!--### FIGURE 4.3 TRAINING HISTORY WINDOW-->

> [!NOTE]
> Training that the employee has taken will appear on the Employee Training window.

Enter or select an **Employee ID**. The **Department** and **Position**
fields will display from the Employee Maintenance window.

### Percent Current Inquiry

Use the Percent Current Inquiry window to measure actual versus requirements
for all positions within a department vs. position by position. To open this
window, click the **HR and Payroll** series button, click **Human
Resources** on the Inquiry content pane and then click **Percent Current**.

<!--![IMAGE - ADVHRPC.jpg](media/232fbd0fb458f93e27b3d063fe7c83c6.jpg)-->

Enter or select a **Department** and **Position**.

Select the **Include all Positions** checkbox to select all Positions within
the selected Department. All positions are checked that have a relationship
with the selected department in the "Certification, License and Training
Required by Department and Position" window.

Select an **Include Employees** option:

- **Home:** Includes employees that have the current Department and Position
    as their Home Department and Position.

- **Worked:** Includes employees that have worked in the current Department
    and Position.

- **Both:** Includes both Home and Worked employees.

Select an **Include Codes** option:

- **All:** Displays ALL codes

- **Required:** Displays only the Required Certification, License or Training
    codes.

Select an **Include Qualifications**:

- **All:** Displays ALL Qualifications

- **Qualified:** Displays Qualified employees.

- **Not Qualified:** Displays non-qualified employees.

Select a **Display** and **Status**.

Enter or select a **Code**, **Employee ID** and **Expiration Date**.

Select the **Printer** button to print the Percent Current Inquiry Report
and Percent Current Totals Report.

<!--![IMAGE – ADVHRPCR.jpg](media/69da87abc6a0daeda941826219b9d7e4.jpg)-->

<!--![ADVHRPCR2.jpg](media/84f06a0657467fa18d5077df794f1753.jpg)-->

### Employee Certifications, Licenses and Training

Use the Certification, License and Training Inquiry window to view
Certification, License and/or Training assigned to specific Employee. To
open this window, click the **HR and Payroll** series button, click **Human
Resources** on the Inquiry content pane and then click **Employee
Certifications, Licenses and Training**.

Enter or select an **Employee ID**.

Select a **Display** option:

- Certification

- License

- Training

The scrolling window displays all of the History information related to the
Display option selected.

### Health and Wellness History

Use the Health and Wellness History window to see all the activity that has
occurred for a specific Employee / Code record. The system tracks all
changes to each existing record. To open this window, click the **HR and
Payroll** series button, click **Human Resources** on the Inquiry content
pane and then click **Health and Wellness History**.

Enter an **Employee ID**. Enter or select a **Code**. The **Description**
and **Category** displays from the Health and Wellness Code Setup window.

The scrolling window allows you to view all History information related to
the Employee and the Health and Wellness Code selected.

## Reports

The Advanced Human Resources module provides printing capabilities by using
the printer icons on the individual windows. For example, pulling up the
Category Setup window and selecting the printer icon (without making any
Category selections) a report will print giving all of the Category Codes
currently set up.

The other way to access information stored in Advanced Human Resources is by
using SmartList Builder. Using this module, the user can build SmartLists
with the data required to meet their reporting needs as it relates to
Advanced Human Resources.

### Excel-based Reports

Certification, License and Training Manager allows the user to track
certifications, licenses, training and other data for employees using back
office functionality. The user can also view and report on this data via
reports. It is necessary, however, for managers and other company officials,
who may not be users of the Microsoft Dynamics GP system, to have access to
this data for decision making purposes. These individuals can use Microsoft
Office Excel reporting to meet their unique needs for viewing and sorting
certification, license and training data and for customizing the
presentation of data to satisfy their requirements.

Excel-based reporting is available for the following existing
reports/inquiries.

- Certification List Report

- License List Report

- Training List Report

- Certification History Report

- License History Report

- Training History Report

The **Required Certification / License / Training report** can be used to measure actual versus requirements for all positions within a department/position.

### SmartList Builder

If the Microsoft Dynamics GP SmartList Builder module is installed, all of
the Certification, License and Training Manager and Employee Health and
Wellness Manager fields will be available to create SmartList Queries.

> [!NOTE]
> Refer to the SmartList Builder documentation for instructions on using SmartList Builder.

## Summary

Advanced Human Resources provides inquiry and reporting capabilities by
using History windows, the Percent Current Inquiry and the use of printer
icons on individual windows. SmartList Builder also enhances the reporting
capabilities.

Key points to remember from this chapter:

- Inquiries are available by using history windows and the Percent Current
    Inquiry.

- Reports are provided by using printer icons.

- SmartList Builder can provide additional printing capabilities based on the
    user's individual reporting requirements.

## See also

[Advanced Human Resources -Overview](AdvancedHumanResource.md)  
[Advanced Human Resources - Employee Maintenance](advanced-hr-employee-maintenance.md)  
[Advanced Human Resources - Training and Certification for Employee Self Service](advanced-hr-inquiries-training-certification.md)  
[Advanced Human Resources - Setup](advanced-hr-setup.md)  
[Human Resources - Overview](HumanResource.md)  
[Human Resources - Company Setup and Organizational Structure](human-resources-company-setup.md)  
[Human Resources - Position Control Setup](human-resources-position-control.md)  
[Human Resources Social Security Number Mask](../whats-new/human-resource-social-security-number-mask.md)  
