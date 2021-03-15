---
title: "Advanced Human Resources Setup"
description: "Examine how to set up advanced human resources in Dynamics GP."
keywords: "HR"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 04/23/2019
---

# Advanced Human Resources in Microsoft Dynamics GP - Setup

The Dynamics GP Advanced Human Resources components (Benefit Lifecycle Manager, Certification, License and Training Manager, and Employee Health and Wellness) require various setup tasks to be completed prior to connecting them with the employee records.

Planning what will be used within the various set up windows is critical. As
categories, codes, types and templates are developed; keep in mind what
information is required for outputs in the form of inquiries and reports.

## Security Setup for Advanced Human Resources

### Setting up a Security Task

Use the Security Task Setup window to select a default security task or
modify the default security task. To open this window, click the
**Administration** series button, click **System** on the Setup content
pane, and then click **Security Tasks**.

Enter a **Task ID**.

Select **HRM Solutions Series** for the **Product**.

- Select **Windows** for the **Type**

- Select **3rd Party** for the **Series**

- Select the following from the **Access List**:

  - **Benefit Options**
  - **Effective Date**
  - **Employee Beneficiaries**
  - **Employee Benefit Dependents**
  - **Employee Dependents**
  - **Future Effective Activation**
  - **Plan Status Reason Lookup**
  - **Plan StatusReasons**

- Change the **Type** to **Reports**

- Select the following from the **Access List**:

  - **Future Effective Activation Reports**

- Change the **Product** to **Certification Manager**.

- Select **Windows** for the **Type**.

- Select **3rd Party** for the **Series**.

- Select the following from the **Access List**:

  - **Certification Endorsement**
  - **Certification Entry**
  - **Certification History**
  - **Certification Setup**
  - **Certification, License and Training Required by Department and Position**
  - **Certification, License and Training Inquiry**
  - **Certifications**
  - **Class Point**
  - **Course and Class Employee Entry**
  - **Employee Certification Endorsements**
  - **Employee License Endorsements**
  - **Employee Training**
  - **Endorsement Setup**
  - **Instructor Lookup**
  - **Instructor Setup**
  - **Issued By Lookup**
  - **Issued by Setup**
  - **License Endorsements**
  - **License Entry**
  - **License History**
  - **License Type Setup**
  - **License Types**
  - **Percent Current Inquiry**
  - **Training Course Definition Additional Information**
  - **Training Courses**
  - **Training History**

- Change the **Type** to **Reports**

- Select the following from the **Access List**:

  - **CLM Certification History**

### CLM Certification License and Training Inquiry

Reports:

- **CLM Certification Setup**
- **CLM Certifications**
- **CLM Course Setup**
- **CLM Instructor Setup**
- **CLM Issued By Setup**
- **CLM License History**
- **CLM License Setup**
- **CLM Licenses**
- **CLM Percent Current**
- **CLM Percent Current Totals**
- **CLM Required Report**
- **CLM Training History**

Change the **Product** to **Employee Health and Wellness**.

- Select **Windows** for the **Type**

- Select **3rd Party** for the **Series**

- Select the following from the **Access List**:

  - **Assign Templates**
  - **Category Lookup**
  - **Category Setup**
  - **Health and Wellness Code Lookup**
  - **Health and Wellness Code Setup**
  - **Health and Wellness Entry**
  - **Health and Wellness History**
  - **Health and Wellness Template Lookup**
  - **Health and Wellness Template Setup**
  - **Injury and Illness Details**
  - **Result Lookup**
  - **Result Setup**
  - **Source Lookup**
  - **Source Setup**

Change the **Type** to **Reports**

- Select the following from the **Access List** o **EHW Category Setup** o
    **EHW Code Setup** o **EHW Health And Wellness Entry Report** o **EHW Health
    and Wellness History Report** o **EHW Injury And Illness Report** o **EHW
    Result Setup** o **EHW Source Setup** o **EHW Template Setup**

Click **Save** to save the selections and close the window.

### Setting up Alternate/Modified Forms and Reports Security

Use the Alternate/Modified Forms and Reports window to set access to the
alternate/modified forms for Advanced Human Resources. To open this window,
click the **Administration** series button, click **System** on the Setup
content pane and then click **Alternate/Modified Forms and Reports**.

Select the appropriate **ID**.

Select **HRM Solutions Series** for the **Product**.

Select **Windows** for the **Type**.

Expand the Payroll folder and select the HRM Solution Series radio button
for each of the following Alternate Core Dynamics GP windows.

- Benefit Setup

- Deduction Setup

- Employee Deduction Maintenance

Click **Save** to save the selections and close the window.

### Setting up Security Roles

Use the Security Role Setup window to select a default security role for
Advanced Human Resources or modify the default security role. To open this
window, click the **Administration** series button, click **System** on the
Setup content pane, and then click **Security Roles**.

### Benefit Lifecycle Manager - Setup

Benefit Lifecycle Manager allows Future Effective Records to be created for
any of the benefit plans. The Future Effective options are accessed the same
way in the Human Resources Benefit Setup and in the Payroll Deduction and
Benefit Setup windows.

To access a Future Effective Record window, click the **HR and Payroll**
series button, click **Human Resources** on the Setup content pane, click
**Benefits and Deductions**, click **Miscellaneous Benefits**, **Health
Insurance**, **Life Insurance** or **Retirement Plans**, enter or select a
**Code**, click the **Benefits icon** and then click **Future Effective**.

![IMAGE ADVHRMBS.jpg](media/9fc14a3a23676cb02b8177f72b72a1d1.jpg)

### FIGURE 2.1 BENEFIT SETUP (FUTURE EFFECTIVE) WINDOW

One of two options will be available on the drop down menu:

- **Future Effective (New)** – this option will be available if no future
    effective record currently exists for the benefit/deduction record currently
    open.

- **Future Effective (Existing 00/00/0000)** – this option will be available
    if a future effective record currently exists for the benefit/deduction
    record currently open. The 00/00/0000 represents the future effective date
    (or Benefit Begin Date) assigned to this future effective record.

### Setting up a Future Effective Record

To create a new Future Effective record for the benefit or deduction record
currently open, click the **Benefits icon** and then click **Future
Effective (New)** option. The system prompts, "Create a Future Effective
record using the current information?"

- Select **Create** to open the Future Effective window with the current core
    record values defaulted in the fields.

- Select **Cancel** to return to the current core record.

For Human Resources the system prompts to enter the Future Effective Date,
enter a date greater than the current user date and select OK.

- Enter the future information for this benefit. The window name will be
    followed by "(FUTURE EFFECTIVE)".

- Select **Save.** They system prompts, "Save future effective record?" o
    Select **Save** to save the current Future Effective record.

Refer to section "Human Resources and Payroll Integration" for more
information on subsequent messages that appear during the save process. o
Select **Cancel** to return to the current future effective record.

Roll down from HR/Payroll Setup level to existing Employee level HR/Payroll
records exists so beware of the selection to this message when saving Future
Effective records. Since the roll down feature is for employee records,
answer this question **No** as Future Effective functionality is for Benefit
Setup windows only.

- Select **Clear** to clear the record form the window and set the window back to the core record.

- Select **Delete** and the system prompts, "Delete this Future Effective record?"

  - Select **Delete** to delete the displayed Future Effective record. Then
        there are checks to determine if there are corresponding Future
        Effective records in Payroll, if there are then the system prompts a
        message asking if the corresponding Future Effective records from
        Payroll should be deleted. If the answer is yes, then select Yes, and
        then all Human Resources and Payroll Future Effective records are
        deleted for that code. If the answer is No and No is selected, then only
        the Human Resources Future Effective records are deleted for that code.

    - Select **Cancel** to return to the current Future Effective record.

- **Reports** are only available if the Future Effective record is open.

> [!NOTE]
> Future Effective amounts are not reported on the Reports generated from the Reports \> Human Resources menu.

If a Future Effective record is created for a Human Resources code that does
not exist in Payroll and corresponding is set up in Payroll, the system
prompts, "The Payroll Benefit must exist before a Future Effective Record
can be created." Select OK.

> [!NOTE]
> When Future Effective records are created, you should not select to roll down to Payroll or Human Resources. This roll down functionality does not apply to the future effective records.

### Editing and Viewing an Existing Future Effective Record

To open an existing Benefits and Deduction Setup window, click the **HR and
Payroll** series button, click **Human Resources** on the Setup content
pane, click **Benefits and Deductions**, click **Miscellaneous Benefits**,
**Health Insurance**, **Life Insurance** or **Retirements Plans**, click the
**GoTo** menu and then click **Future Effective**.

The system prompts, "Display future effective record?"

- Select **Yes** to open the current Future Effective record in the Future
    Effective window. For Human Resources the system then prompts to verify the
    Future Effective Date, leave the date as entered or edit the date and select
    OK.

- Select **No** to return to the current core record.

- Select **Save** to save and the system prompts, "Save future effective
    record?" o Select **Save** to save the current Future Effective record. o
    Select **Cancel** to return to the current Future Effective record.

Roll down from HR/Payroll Setup level to existing Employee level HR/Payroll
records exists so beware of the selection to this message when saving Future
Effective records. Select **No**; Future Effective functionality is for the
Benefit and Deduction Setup windows only.

- Select **Clear** to clear the record from the window and set the window back
    to the core record.

- Select **Delete** to delete the record, the system prompts "Delete this
    Future Effective record?"

o Select **Delete** to delete the displayed Future Effective record. Then
there would be checks if there were corresponding Future Effective records
in Payroll, if so the system prompts with a message asking to delete
corresponding Future Effective records from Payroll. If Yes is selected,
then all Human Resources and Payroll Future Effective records are deleted
for that code. If No is selected, then only the Human Resources Future
Effective records are deleted for that code. o Select **Cancel** to return
to the current future effective record.

- **Reports** are only available while a Future Effective record is open.

### Saving in Payroll

When saving a future effective record in Payroll, the system prompts,

"Save future effective record?"

- Select **Save** to save the current future effective record.

  - The system prompts, "The information for the Payroll deduction code is different than the Human Resources deduction code. Do you want to continue?"

- Selecting **Yes** prompts, "These changes must be saved in the Benefit Setup
    window to take effect across Human Resources with Integration to Payroll.
    When the Benefit Setup window opens, choose Save to save changes." Click OK.

- Selecting **No** cancels the message and returns to the Future Effective
    record.

- Select **Cancel** to return to the current Future Effective record window.

Select **Save** to save this operation, the system prompts, "Save future
effective record?"

- Select **Save** to save the current future effective record.

  - The system prompts, "The information for the Payroll deduction code is different than the Human Resources deduction code. Do you want to continue?"

- Select **Yes** or select **No**

- Select **Cancel** to return to the current Future Effective record window.

Select **Clear** to clear the window and return to the core window.

### Saving in Human Resources

Next, the system prompts, "Do you want to set up the corresponding codes in
Payroll so the integration is complete?"

- Select **Yes** to open the Payroll Deduction window and default all values
    from the Human Resources Future Effective record. Once the record is saved
    in this window, the Payroll Benefit window opens and defaults to save as
    well.

- Select **No** to save the Future Effective record only in Human Resources
    and return to the core window.

If this operation should **NOT** be saved, click **Cancel**. It returns to
the Future Effective record.

Click **OK** when prompted, "These changes must be saved in the Benefit

Setup window to take effect across Human Resources with Integration to
Payroll." When the Benefit Setup window opens, select **Save** to save
changes.

### Employee Dependents Window

Within the Employee Dependents window data fields have been added to use to
set up dependents associated with the employee. To open this window, click
the **HR and Payroll** series button, click **Human Resources** on the Cards
content pane, click **Employee** and then click **Dependents**.

![IMAGE – ADVHRDEP](media/aef7d41c75511a0b9c39b7e944629bb0.jpg)

### FIGURE 2.2 EMPLOYEE DEPENDENTS WINDOW

The additional data fields are:

- **Status** - select Active or Inactive

- **Status Comment** - these options are defined in the Plan Status Reason
    window

- **Change Date**

- **Marital Status** - select Married, Single or N/A

- **Change Date**

- **Disabled** checkbox

- **Disabled Date**

### Employee Beneficiaries Window

Within the Employee Beneficiaries window additional data fields are
available, to define beneficiaries associated with the employee and specific
benefit plan. To open this window, click the **HR and Payroll** series
button, click **Human Resources** on the Cards content pane, click
**Employee - Benefits**, select a **Benefit**, select an **Employee ID**,
click the **Benefit** icon, and click **Beneficiary Definition**.

![IMAGE - ADVHRBENF.jpg](media/4341819673bb483f27befe0e7bf70ece.jpg)

### FIGURE 2.3 EMPLOYEE BENEFICIARIES WINDOW

The data fields are:

- **Plan Status** - select Active or Inactive

- **State Change Reason** - the lookup button allows information to be
    defaulted from existing Dependents.

- **Status Comment** - these options are defined in the Plan Status Reason
    window

- **Change Date**

- **Marital Status** - select Married, Single or N/A

- **Change Date**

- **Disabled** checkbox

- **Disabled Date**

### Employee Benefit Dependents Window

The Employee Benefit Dependents window allows Human Resources to define the
employee dependents associated with a specific employee benefit plan. To
open this window, click the **HR and Payroll** series button, click **Human
Resources** on the Cards content pane, click **Employee -**

**Benefits**, select a **Benefit**, select an **Employee ID**, select a
**Benefit Code**, click the **Benefit** icon, and click **Dependents**.

![IMAGE – ADVHRBD](media/b1ed05943d5e7de57ef712998bb236ca.jpg)

### FIGURE 2.4 EMPLOYEE BENEFIT DEPENDENTS WINDOW

Complete the **Plan Status** and **Status Change Reason** fields as
appropriate.

### Plan Status Reasons Window

The Plan Status Reasons window allows Human Resources to define acceptable
Reasons for why a particular dependent or beneficiary were activated or
inactivated from a benefit plan. This information is necessary to provide to
benefit carriers. To open the Plan Status Reasons window, click the **HR and
Payroll** series button, click **Human Resources** on the Setup content pane
and then click **Plan Status Reasons**.

Select a **Record Type** and then select a **Status Type**.

### Benefit Options Window

To open the Benefit Options window, click the **HR and Payroll** series
button, click **Human Resources** on the Setup content pane, select a
**Benefit** window, select a **Benefit Code**, click the **Benefits** icon
and then click **Benefit Options**.

![IMAGE – ADVHRBO.jpg](media/faf062154592f53ea4f1a15d66bca5d4.jpg)

Each of the Benefit Setup windows (Miscellaneous Benefits, Health Insurance,
Life Insurance and Retirement Plans) has the Benefit Options item added to
the Benefits button. When Benefit Options is selected this will allow the
user to define the maximum number of dependents allowed for the specified
benefit.

> [!NOTE]
> A Benefit Setup record must be displayed within the window to open Benefit Options.

This window allows the user to set the Maximum Dependents Allowed. The
Maximum Dependents Allowed will be validated when enrollment changes are
made to the benefit record.

By default, the number of dependents is set to zero which means unlimited if
the Benefit Self Service module is not being used.

## Certification, License and Training Manager Setup

There are several set up windows associated with Certification, License and
Training Manager:

- Issued By Setup

- Instructor Setup

- Endorsement Setup

- Certification Setup

- License Type Setup

In addition, several other windows can be completed at this point in the
process:

- Training Course Definition Additional Information window

- Class Points window

- Certification, License and Training Required by Dept and Position window

### Issued By Setup Window

Use the Issued By Setup window to set up, assign an unlimited number of

Issued By Agencies with description, contact and address information. An
Issued By could be Agency or other organization. To open this window, click
the **HR and Payroll** series button, click **Human Resources** on the Setup
content pane, click **Certifications, Licenses and Training** and then click
**Issuers**.

![IMAGE – ADVHRISS.jpg](media/da6d7897048bebdeb57e7d4db16c7719.jpg)

Enter or select an **Issued By Agency**.

Enter the following information:

- **Description**

- **Contact Name**

- **Address 1**

- **Address 2**

- **City**

- **State**

- **Zip Code**

- **Phone Number**

- **Fax Number**

- **Web Site**

- **E-mail**

Select the **Inactive** checkbox to inactivate the current Issued By Agency
code.

### Instructor Setup Window

Use the Instructor Setup window to set up, assign unlimited number of
Instructors with contact and address information. To open this window, click
the **HR and Payroll** series button, click **Human Resources** on the Setup
content pane, click **Certifications, Licenses and Training** and then click
**Instructors**.

![IMAGE – ADVHRINS](media/1cd28ed5b5629e37581c7374f930f486.jpg)

Enter or select **Instructor ID**.

Enter the following information:

- **Instructor Name**

- **Address 1**

- **Address 2**

- **City**

- **State**

- **Zip Code**

- **Phone Number**

- **Fax Number**

- **Web Site**

- **E-mail**

Select the **Inactive** checkbox to inactivate the current instructor ID
code.

### Endorsement Setup Window

Use the Endorsement Setup window to define the Endorsements by Certification
or License. To open this window, click the **HR and Payroll** series button,
click **Human Resources o**n the Setup content pane, click **Certifications,
Licenses and Training** and then click **Endorsements**.

Select the **Type**:

- Certification

- License

Enter the new **Endorsement** or edit the Endorsement for the selected Type.

Select **OK** to save the Endorsement Setup and close the window.

To delete a row, select the Endorsement and then select the delete row
button to delete this Endorsement.

### Certification Setup Window

Use the Certification Setup window to set up and assign unlimited number of
Certifications with descriptions. To open this window, click the **HR and
Payroll** series button, click **Human Resources** on the Setup content
pane, click **Certifications, Licenses and Training** and then click
**Certifications**.

![IMAGE – ADVHRCS.jpg](media/442e889d717a4be412c2448f61e209cb.jpg)

When entering a new Certification Code, enter a **Description** and select
any **Required** options.

- **Issued By Agency**

- **Original Issue Date**

- **Expiration Date**

- **Certification Number**

- **Date Renewed**

Selecting any of the **Required** options affects the Employee Certification
Entry window by forcing entry of a value in the field prior to saving the
record.

Select the **Inactive** checkbox to inactivate the current Certification
Code.

### Certification Endorsements Window

Use the Certification Endorsements window to mark the appropriate
Endorsement that was created during the Endorsement Setup. To open this
window, click the **Endorsements** button on the Certification Setup window.

The **Marked** column indicates the Endorsements that are marked for the
specific Certification Code. Use **Mark All** and **Unmark All** to mark or unmark all Endorsements at once.

Select **OK** to save the Endorsement Assignment and close the window.

### License Type Setup Window

Use the License Type Setup window to set up and assign unlimited number of
License Types with descriptions. To open this window, click the **HR and
Payroll** series button, click **Human Resources** on the Setup content
pane, click **Certifications, Licenses and Training** and then click
**License Types**.

![IMAGE – ADVHRLS.jpg](media/31780b0c27992aefbc525bd2adbf7a77.jpg)

Enter or select a **License Type**.

When entering a new License Type, complete the **Description**, select the
appropriate **Required** options and assign **Endorsements**.

- **Issued By Agency**

- **Date Renewed**

- **Expiration Date**

- **Issued By State**

- **Original Issue Date**

Selecting any of the fields as **Required** affects the Employee License
Entry window by forcing entry of a value in the field prior to saving the
record.

Select the **Inactive** checkbox to inactivate the current Certification
Code.

### License Type Endorsements Window

Use the License Endorsements window to select the appropriate Endorsement
that was created during the Endorsement Setup. To open this window, click
the **Endorsements** button on the License Type Setup window.

The **Marked** column indicates the Endorsements that are marked for the
specific License Code. Use **Mark All** and **Unmark All** to mark or unmark
all Endorsements at once.

Select **OK** to save the Endorsement Assignment and close the window.

### Training Course Definition Additional Information Window

Use the Training Course and Class Definition window to set up a training
course. The Certification, License and Training Manager has extended the
Course set up with additional fields on the new Training Course Definition
Additional Information window. To open this window, click the **HR and
Payroll** series button, click **Human Resources** on the Setup content
pane, click **Certifications, Licenses and Training** and then click
**Training Additional Info**.

![IMAGE – ADVHRTCS.jpg](media/aaab29d5481f1423098576df5af5f4ed.jpg)

Enter or select a **Course ID**. The **description** field displays from the
Training Course and Class Definition window. Check the boxes for fields that
are to be **Required** on the Employee Training window.

Select the **Inactive** checkbox to inactivate the current Course ID.

### Class Points Window

Use the Class Points window to add points to the individual class
combination. To open this window, click the **HR and Payroll** series
button, click **Human Resources** on the Setup content pane, click
**Training**, select a **Course ID**, select a **Class**, click
**Additional** from the menu and then click **Class Points**.

Enter a **Points** value for the selected class (ex: time length of class).

Select **OK** to save and close the Class Points window.

### Certification, License and Training Required by Dept and Position Window

Use the Certification, License and Training Required by Department and
Position window to assign to a specific Position and Department combination
and any required certifications, licenses or training. To open this window,
click the **HR and Payroll** series button, click **Human Resources** on the
Setup content pane, click **Certifications, Licenses and Training** and then
click **Requirements**.

Use this window to add, update or remove from a list any required
certifications, licenses or training.

Enter or select a **Department** and **Position**.

**Required Certifications** section within the scrolling window allows the
user to assign any Certification Codes that are required for the currently
selected Department and Position. Enter or delete the Certification Codes as
required. To delete the Certification Code, select the code and then select
delete row button.

**Required Licenses** section within the scrolling window allows the user to
assign any License Types that are required for the currently selected
Department and Position. Enter or delete the License Types as required. To
delete the License Type, select the type and then select delete row button.

**Required Training** section within the scrolling window allows the user to
assign any Course IDs that are required for the currently selected
Department and Position. Enter or delete the Course IDs as required. To
delete the Course ID, select the course id and then select delete row
button.

Once a Department and Position have been selected, the **Copy** button is
enabled. Selecting Copy opens the Copy Requirements window and allows the
user to copy all of the Required Certifications, Licenses and Training
associated with the currently open Department/Position combination to
another Department/Position combination.

Enter or select the **Copy To Department** and **Copy To Position**. Select
**Copy** to complete the copy process or select **Cancel** to cancel the
copy process.

## Employee Health and Wellness Manager - Setup

There are several set up windows associated with Employee Health and
Wellness:

- Category Setup window

- Results Setup window

- Health and Wellness Code Setup window

- Health and Wellness Template Setup window

- Sources Setup window

### Health and Wellness Code Setup Window

Use the Health and Wellness Code Setup window to set up and assign unlimited
number of Codes with descriptions and be able to set the status of the code
to Active or Inactive. To open this window, click the **HR and Payroll**
series button, click **Human Resources** on the Setup content pane, click
**Health and Wellness** and then click **Codes**.

![IMAGE – ADVHRHCS.jpg](media/e200fd48fb3a0f3622532c5d5f5c7b1c.jpg)

Examples of Health and Wellness Codes are Rubeola, Rubella, Booster,
Hepatitis C, Pertussis Exposure, Laser Screening, Hearing Protection and Eye
Exams.

For each Code the user will be able to set up results, such as Positive or
Negative. These results will then be available as choices on the Employee
Health and Wellness Entry window.

Enter or select a **Code**; enter or modify the **Description** and enter or
select the **Category**.

The scrolling window allows the user to apply the Results that relate to the
current Health and Wellness code.

- **Checkbox** will activate the Result

- Enter or select a **Result Code**

- The **Description** displays from the Result Setup window

### Result Setup Window

Use the Result Setup window to set up and assign unlimited number of Result
Codes with descriptions and be able to set the status of the code to Active
or Inactive. To open this window, click the **HR and Payroll** series
button, click **Human Resources** on the Setup content pane, click **Health
and Wellness** and then click **Results**.

Enter or select a **Result Code**. Enter or modify the **Description**.

Select the **Inactive** checkbox will inactivate the current Result Code.

Select **Save** to save the Result Code.

### Health and Wellness Template Setup Window

Use the Health and Wellness Template Setup window to set up and assign
unlimited number of Templates with descriptions and be able to set the
status of the Template to Active or Inactive. To open this window, click the
**HR and Payroll** series button, click **Human Resources** on the Setup
content pane, click **Health and Wellness** and then click **Templates**.

Employee defined templates can be used to assign defaults to employees. One
template setup assigned can easily establish all the tests required by a
certain position, employee class or grouping specific to each facility.

Enter or select a **Template Code** and enter or modify the **Description**.

The scrolling window allows the user to associate Health and Wellness Codes
with a Template Code.

Enter or select a **Health and Wellness Code**.

The **Description** displays from the Health and Wellness Code Setup window.

The **Category and Description** displays from the Category Setup window.

### Source Setup Window

Use the Source Setup window to create Source records. To open this window,
click the **HR and Payroll** series button, click **Human Resources** on the
Setup content pane, click **Health and Wellness** and then click
**Sources**.

Enter or select a **Source ID**.

Enter the **Last Name**, **First Name**, **Middle Name**, **Social Security
Number** and **Medical Record Number**.

Select **Save** to save the Source ID.

### Category Setup Window

Use the Category Setup window to set up an unlimited number of Category
Codes with descriptions and be able to set the status of the code to Active
or Inactive. The Category Code can be used for report grouping and
restrictions. Example: Immunizations, Vaccinations, Blood Exposure, Injuries
and Tests. To open this window, click the **HR and Payroll** series button,
click **Human Resources** on the Setup content pane, click **Health and
Wellness** and then click **Categories**.

Enter or select a **Category Code**. Enter or modify the **Description**.

Select the **Inactive checkbox** to inactivate the current Category Code.

Select **Save** to save the Category Code.

## Summary

A variety of setup windows need to be completed prior to using the

Advanced Human Resources module. Each of the components to Advanced Human
Resources has dedicated windows for this purpose.

Key points to remember from this chapter:

- Future Effective records can be set up to pre-enter information for upcoming
    changes to benefit plans.

- After completing the appropriate setup for Certification, License and
    Training Manager, certifications, licenses and training can be assigned to a
    department and position combination as required.

- Templates can be developed to assign predetermined health and wellness codes
    that will eventually be assigned on the employee level.

## See also

[Advanced Human Resources - Overview](AdvancedHumanResource.md)  
[Advanced Human Resources - Employee Maintenance](advanced-hr-employee-maintenance.md)  
[Advanced Human Resources - Inquiries and Reports](advanced-hr-inquiries-reports.md)  
[Advanced Human Resources - Training and Certification for Employee Self Service](advanced-hr-inquiries-training-certification.md)  
[Human Resources - Overview](HumanResource.md)  
[Human Resources - Company Setup and Organizational Structure](human-resources-company-setup.md)  
[Human Resources - Position Control Setup](human-resources-position-control.md)  
[Human Resources Social Security Number Mask](../whats-new/human-resource-social-security-number-mask.md)  
