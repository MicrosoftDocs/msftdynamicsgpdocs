---
title: "Advanced Human Resources"
description: "Examine how advanced human resources works in Dynamics GP."
keywords: "HR"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 04/23/2019
---

# Advanced Human Resources in Microsoft Dynamics GP

## CHAPTER 1: FEATURES AND REQUIREMENTS

>   The objectives are:

-   Understand the features, requirements and multi-user access criteria for
    Benefit Lifecycle Manager within Advanced Human Resources.

-   Understand the features and requirements for the Certification, License and
    Training Manager component of Advanced Human Resources.

-   Understand the features available through the Employee Health and Wellness
    component of Advanced Human Resources.

### Introduction

>   Microsoft Dynamics® GP Advanced Human Resources includes three components:
>   Benefit Lifecycle Manager; Certification, License and Training Manager; and
>   Employee Health and Wellness.

>   **Benefit Lifecycle Manager** integrates with the Microsoft Dynamics GP

>   Payroll module. It is designed to create Human Resources, Payroll Benefit
>   and Payroll Deduction setup records that are not immediately effective. At
>   the appropriate time, the records can be activated and previous setup
>   records are tracked in history.

>   **Certification, License and Training Manager** integrates with the
>   Microsoft Dynamics GP Human Resources module. Certification, License and
>   Training Manager creates the link between the skills, training and
>   certifications as well as provides a means to track employee certifications,
>   licensing and training. It also enables the tracking of certifications or
>   license to the extent of reporting on expiration, renewal periods and
>   whether the certifications or licenses are required. You may query on
>   required certifications, licenses, training and dates of expiration. In
>   addition, a query can be created on a specific list of employees with a
>   particular certification, license or training.

>   **Employee Health and Wellness Manager** integrates with the Microsoft

>   Dynamics GP Human Resources module. The purpose of the Employee Health and
>   Wellness Manager is to provide features for tracking all immunizations,
>   vaccinations and tests required for each employee. The results for each test
>   can also be recorded. Since codes can be defined to meet the company needs,
>   this solution allows for additions or changes as business or job
>   requirements change. The Employee Health and Wellness Manager will enable
>   the user to schedule follow-up vaccinations, immunizations and tests. Having
>   all the data available will enable easy searches on who is past due or
>   scheduled for a particular immunization, vaccination or test. The
>   requirements per employee are more easily assigned and tracked by the
>   utilization of health and wellness templates.

### Benefit Lifecycle Manager

>   Benefit Lifecycle Manager is used to create Human Resources Benefit, Payroll
>   Benefit and Payroll Deduction setup records that are not immediately
>   effective when creating employee level records or running payroll in
>   Microsoft Dynamics GP. Benefit Lifecycle Manager then enables the user to
>   activate the Future Effective setup records at the appropriate time, while
>   tracking the past setup records in history.

>   By creating a Future Effective date to the record, this information can also
>   be extended to the Benefit Self Service product on.

>   Benefit Lifecycle Manager integrates with the Microsoft Dynamics GP Payroll
>   module. When creating Human Resources Benefit, Payroll Benefit or Payroll
>   Deduction records, the user can easily create or modify the Future Effective
>   record as well.

#### Features

>   The features and capabilities of Benefit Lifecycle Manager include:

-   Create Human Resources Setup Future Effective records for:

    -   Miscellaneous Benefit o Health Insurance o Life Insurance o Retirement
        Plans

-   Create corresponding Payroll Setup Future Effective records for:

    -   Benefit o Deduction

-   Activate Future Effective Setup records

-   Track History of previous Setup records

-   Make Pending Changes available to Benefit Self Service for informational and
    enrollment purposes.

>   *NOTE: This product is required for use with Benefit Self Service to
>   activate any Pending Changes options in.*

#### Release Requirements

>   Certain features and the use of this product must meet the following setup
>   requirements to ensure proper functionality. Failure to use the Benefit
>   Lifecycle Manager product as specified here will not currently be supported.

-   Changes must be made from the Human Resources menu and rolled down to
    Payroll. There is **NO** reconciling functionality for future effective
    records.

-   If creating a Future Effective Benefit, Payroll Deduction or Payroll Benefit
    record, the core record for that Benefit Code must exist before attempting
    to create the Future Effective record.

-   Each individual must have the Payroll View for Human Resources option
    selected. To enable this option open the User Setup window, click the
    **Administration** series button, click **System** on the Setup content pane
    and then click **User**. Enter or select the **User ID**. Select the
    **Payroll View for Human Resources** checkbox. Click **Save**.

-   Grant Security Access using the Security Setup window to grant individual
    security settings for each company.

#### Multi-User Access

>   Additional checks have been added to restrict access to Benefit Codes and
>   Future Effective Benefit Codes when Benefit Lifecycle Manager is being used
>   to ensure that benefit codes are modified correctly. The restrictions added
>   include the following scenarios and if one of these scenarios is
>   encountered, the system prompts with “This code is open by another user.
>   Please try again later.”

>   **Multi User Access Denied Scenarios:**

-   If the benefit code is opened in the Future Effective mode in the

>   Human Resources Benefit Setup, Payroll Benefit Setup or Payroll Deduction
>   Setup window, no other employee is able to open that benefit code in any of
>   the three areas at the core setup level.

-   If more than one employee currently has the benefit code open in the Human
    Resources Benefit Setup, Payroll Benefit Setup or Payroll Deduction Setup
    window and there is an attempt to create a new or display the existing
    Future Effective record in any of the three areas for that benefit code.

>   When the Human Resources to Payroll Integration is happening for a Future
>   Effective record, if another employee would open that benefit code in one of
>   the subsequent windows before the Human Resources to Payroll Integration
>   gets to that level, when the Human Resources to Payroll Integration hits
>   that level, the integration is stopped.

### Certification, License and Training Manager

>   The Certification, License and Training Manager tracks all Certifications,
>   Licensing and Training requirements. This product completes certain areas
>   and fills additional areas that core Microsoft Dynamics GP skills and
>   certification tracking does not currently handle.

>   Certification, License and Training Manager integrates with Microsoft

>   Dynamics GP Human Resources. The Certification, License and Training Manager
>   will create the link between the skills, training and certifications as well
>   as provide a means to track employee certifications, licensing and training.
>   It will also enable the tracking of certifications or licenses to the extent
>   of reporting on expiration, renewal periods and whether the certifications
>   or licenses are required. You may query on required certifications,
>   licenses, training and dates of expiration. In addition, you may query on a
>   specific list of employees with a particular certification, license or
>   training.

#### Features

>   The features and capabilities of Certification, License and Training Manager
>   include:

-   Enter unlimited Certifications

-   Certifications tracking for employees

-   Enter unlimited Licenses

-   License tracking for employees

-   Enter unlimited Training

-   Training tracking for employees

-   Inquire for an employee on Certifications, Licenses and Training

-   Set and View Requirements per Department and Position combinations for
    Certification, License and Training

-   View Employee Percent Current per Department and Position combinations based
    on Worked or Home department/positions for Certification, License and
    Training

-   SmartList Builder reporting options

#### Release Requirements

>   Certain features and the use of this product must meet the following setup
>   requirements to ensure proper functionality. Failure to use the

>   Certification, License and Training Manager product as specified here will
>   not currently be supported.

>   To Grant Security Access use the Security Setup window to grant individual
>   security settings for each company.

#### Certification Feature

>   The Certification feature of the Certification, License and Training Manager
>   allows the user to enter Certification information specific to the company
>   needs as well as track employee level Certification information as required
>   within the industry or business. The Certification feature is easy to use
>   and provides inquiry options to view the information employees are tracking
>   more easily.

>   When a record for a Certification is entered where an expiration date is an
>   attribute of that Certification whether the date is known at the time of
>   entry or later, the expiration date will always be a future date to expire
>   in relationship to the current record, i.e. my current Certification will
>   expire at a future date. When the Certification is renewed or completed, the
>   user can pull up the record for the Certification and enter the current
>   renewal/completed date, the future expiration date and select Save. When it
>   is the first year of a Certification, then the Original Issue Date = Date
>   Renewed/Completed.

#### License Feature

>   The License feature of the Certification, License and Training Manager
>   allows the user to enter License information specific to the company needs
>   as well as track employee level License information as required within the
>   industry or business. The License feature is easy to use and provides
>   inquiry options to view the information an employee is tracking.

>   When a record for a License is entered where an expiration date is an
>   attribute of that License whether the date is known at the time of entry or
>   later, the expiration date will always be a future date to expire in
>   relationship to the current record. When the License is renewed or
>   completed, you should pull up the record for the License and enter the
>   current renewal/completed date and the future expiration date and select
>   Save. When it is the first year of a License, then the Original Issue Date =
>   Date Renewed/Completed.

#### Training Feature

>   The Training feature of the Certification, License and Training Manager
>   allows the user to enter Training information such as Courses and Classes
>   specific to the company needs as well as track employee level

>   Training information as required within the industry or business. The
>   Training feature is easy to use and provides inquiry options to view the
>   information the employee is tracking more easily.

>   When a record for the Training is entered where an expiration date is an
>   attribute of that Training, the expiration date will always be a future in
>   relationship to the current record. When the Training is renewed /
>   completed, you will pull up the record for the Training and enter the
>   current renewal / completed date and the future expiration date and select
>   Save. When it is the first year of a Training, then the Original Issue Date
>   = Date Renewed/Completed.

## Employee Health and Wellness

>   Within Microsoft Dynamics GP Human Resources, you can track injury and
>   illness information for each employee and generate the necessary OSHA
>   reports. Employee Health and Wellness Manager enables organizations to
>   completely track all additional employee immunizations, vaccinations and
>   test requirements that are related to the injury and illness cases, but not
>   included on OSHA reports.

>   Employee Health and Wellness Manager is an enhancement that integrates with
>   Microsoft Dynamics GP Human Resources. The purpose of Employee Health and
>   Wellness Manager is to provide features for tracking all immunizations,
>   vaccinations and tests required for each employee. The results for each test
>   can also be recorded. Since the codes can be defined, the product allows for
>   additions or changes as business or job requirements change.

>   Employee Health and Wellness Manager enables the user to schedule follow-up
>   vaccinations, immunizations and tests. Having all the data available will
>   enable easy searches on who is past due or scheduled for a particular period
>   for a particular immunization, vaccination or test. The requirements per
>   employee are more easily assigned and tracked by the utilization of health
>   and wellness templates.

### Features

>   The features and capabilities of Employee Health and Wellness Manager
>   include:

-   Create Categories and associated Codes specific to the business needs

-   Create unlimited Results types that can be associated with the Health and
    Wellness codes

-   Create Health and Wellness codes for use in Health and Wellness and related
    to Injury and Illness tracking

-   Assignment of multiple codes to employees via customized Templates

-   Assignment of Health and Wellness codes to employees for informational and
    tracking purposes

-   Additional information for tracking with Illness and Injury Cases, including
    Source tracking

-   SmartList Builder reporting options

>   Sensitive information related to the Health and Wellness of Employees and
>   Sources is tracked using this product. Compliance with HIPPA regulations as
>   it pertains to this data is the responsibility of the user.

### Summary

>   The Advanced Human Resources module for Microsoft Dynamics GP is comprised
>   of three components:

1.  Benefit Life Cycle Manager

2.  Certification, License and Training Manager and

3.  Employee Health and Wellness

>   Key points to remember from this chapter:

-   Benefit Life Cycle Manager provides the ability to assign future effective
    dates for Miscellaneous Benefits, Health Insurance, Life Insurance and
    Retirement Plans

-   The user can enter an unlimited number of certifications, licenses and
    training data for employees.

-   Employee Health and Wellness allows the organization to track various
    health-related categories, codes and tests, as well as the results of each.

## CHAPTER 2: ADVANCED HUMAN RESOURCES SETUP

Objectives
----------

>   The objectives are:

-   Use Security Task Setup window to set security tasks for Advanced Human
    Resources modules.

-   User Security Roles Setup window to set security roles for Advanced Human
    Resources modules.

-   Create a future effective record for a benefit plan such as health
    insurance, life insurance or a retirement plan.

-   Learn to complete the various setup windows required to use Certification,
    License and Training Manager.

-   Learn to set up various Health and Wellness windows to allow the
    organization to track health related information for employees.

### Introduction

>   Microsoft Dynamics GP Advanced Human Resources components

>   (Benefit Lifecycle Manager; Certification, License and Training Manager and
>   Employee Health and Wellness) require various setup tasks to be completed
>   prior to connecting them with the employee records.

>   Planning what will be used within the various set up windows is critical. As
>   categories, codes, types and templates are developed; keep in mind what
>   information is required for outputs in the form of inquiries and reports.

### Security Setup for Advanced Human Resources

#### Setting up a Security Task

>   Use the Security Task Setup window to select a default security task or
>   modify the default security task. To open this window, click the
>   **Administration** series button, click **System** on the Setup content
>   pane, and then click **Security Tasks**.

>   Enter a **Task ID**.

>   Select **HRM Solutions Series** for the **Product**.

-   Select **Windows** for the **Type**

-   Select **3rd Party** for the **Series**

-   Select the following from the **Access List**:

>   o **Benefit Options** o **Effective Date** o **Employee Beneficiaries** o
>   **Employee Benefit Dependents** o **Employee Dependents** o **Future
>   Effective Activation** o **Plan Status Reason Lookup** o **Plan Status
>   Reasons**

>   Change the **Type** to **Reports**

-   Select the following from the **Access List** o **Future Effective
    Activation Reports**

>   Change the **Product** to **Certification Manager**.

-   Select **Windows** for the **Type**.

-   Select **3rd Party** for the **Series**.

-   Select the following from the **Access List**:

    -   **Certification Endorsement** o **Certification Entry** o
        **Certification History** o **Certification Setup**

    -   **Certification, License and Training Required by**

>   **Department and Position** o **Certification, License and Training
>   Inquiry** o **Certifications** o **Class Point**

-   **Course and Class Employee Entry** o **Employee Certification
    Endorsements** o **Employee License Endorsements** o **Employee Training** o
    **Endorsement Setup** o **Instructor Lookup** o **Instructor Setup** o
    **Issued By Lookup** o **Issued by Setup** o **License Endorsements**

-   **License Entry** o **License History** o **License Type Setup** o **License
    Types** o **Percent Current Inquiry** o **Training Course Definition
    Additional Information** o **Training Courses** o **Training History**

>   Change the **Type** to **Reports**

-   Select the following from the **Access List** o **CLM Certification
    History**

#### CLM Certification License and Training Inquiry

>   **Report** o **CLM Certification Setup** o **CLM Certifications** o **CLM
>   Course Setup** o **CLM Instructor Setup** o **CLM Issued By Setup** o **CLM
>   License History** o **CLM License Setup** o **CLM Licenses** o **CLM Percent
>   Current** o **CLM Percent Current Totals** o **CLM Required Report** o **CLM
>   Training History**

>   Change the **Product** to **Employee Health and Wellness**.

-   Select **Windows** for the **Type**

-   Select **3rd Party** for the **Series**

-   Select the following from the **Access List**:

    -   **Assign Templates** o **Category Lookup** o **Category Setup** o
        **Health and Wellness Code Lookup** o **Health and Wellness Code Setup**

    -   **Health and Wellness Entry** o **Health and Wellness History** o
        **Health and Wellness Template Lookup** o **Health and Wellness Template
        Setup** o **Injury and Illness Details** o **Result Lookup** o **Result
        Setup** o **Source Lookup** o **Source Setup**

>   Change the **Type** to **Reports**

-   Select the following from the **Access List** o **EHW Category Setup** o
    **EHW Code Setup** o **EHW Health And Wellness Entry Report** o **EHW Health
    and Wellness History Report** o **EHW Injury And Illness Report** o **EHW
    Result Setup** o **EHW Source Setup** o **EHW Template Setup**

>   Click **Save** to save the selections and close the window.

#### Setting up Alternate/Modified Forms and Reports Security

>   Use the Alternate/Modified Forms and Reports window to set access to the
>   alternate/modified forms for Advanced Human Resources. To open this window,
>   click the **Administration** series button, click **System** on the Setup
>   content pane and then click **Alternate/Modified Forms and Reports**.

>   Select the appropriate **ID**.

>   Select **HRM Solutions Series** for the **Product**.

>   Select **Windows** for the **Type**.

>   Expand the Payroll folder and select the HRM Solution Series radio button
>   for each of the following Alternate Core Dynamics GP windows.

-   Benefit Setup

-   Deduction Setup

-   Employee Deduction Maintenance

>   Click **Save** to save the selections and close the window.

#### Setting up Security Roles

>   Use the Security Role Setup window to select a default security role for
>   Advanced Human Resources or modify the default security role. To open this
>   window, click the **Administration** series button, click **System** on the
>   Setup content pane, and then click **Security Roles**.

### Benefit Lifecycle Manager - Setup

>   Benefit Lifecycle Manager allows Future Effective Records to be created for
>   any of the benefit plans. The Future Effective options are accessed the same
>   way in the Human Resources Benefit Setup and in the Payroll Deduction and
>   Benefit Setup windows.

>   To access a Future Effective Record window, click the **HR and Payroll**
>   series button, click **Human Resources** on the Setup content pane, click
>   **Benefits and Deductions**, click **Miscellaneous Benefits**, **Health
>   Insurance**, **Life Insurance** or **Retirement Plans**, enter or select a
>   **Code**, click the **Benefits icon** and then click **Future Effective**.

IMAGE ADVHRMBS.jpg

![A screenshot of a cell phone Description automatically generated](media/9fc14a3a23676cb02b8177f72b72a1d1.jpg)

### FIGURE 2.1 BENEFIT SETUP (FUTURE EFFECTIVE) WINDOW

>   One of two options will be available on the drop down menu:

-   **Future Effective (New)** – this option will be available if no future
    effective record currently exists for the benefit/deduction record currently
    open.

-   **Future Effective (Existing 00/00/0000)** – this option will be available
    if a future effective record currently exists for the benefit/deduction
    record currently open. The 00/00/0000 represents the future effective date
    (or Benefit Begin Date) assigned to this future effective record.

### Setting up a Future Effective Record

>   To create a new Future Effective record for the benefit or deduction record
>   currently open, click the **Benefits icon** and then click **Future
>   Effective (New)** option. The system prompts, “Create a Future Effective
>   record using the current information?”

-   Select **Create** to open the Future Effective window with the current core
    record values defaulted in the fields.

-   Select **Cancel** to return to the current core record.

>   For Human Resources the system prompts to enter the Future Effective Date,
>   enter a date greater than the current user date and select OK.

-   Enter the future information for this benefit. The window name will be
    followed by “(FUTURE EFFECTIVE)”.

-   Select **Save.** They system prompts, “Save future effective record?” o
    Select **Save** to save the current Future Effective record.

>   Refer to section “Human Resources and Payroll Integration” for more
>   information on subsequent messages that appear during the save process. o
>   Select **Cancel** to return to the current future effective record.

>   Roll down from HR/Payroll Setup level to existing Employee level HR/Payroll
>   records exists so beware of the selection to this message when saving Future
>   Effective records. Since the roll down feature is for employee records,
>   answer this question **No** as Future Effective functionality is for Benefit
>   Setup windows only.

-   Select **Clear** to clear the record form the window and set the window back
    to the core record.

-   Select **Delete** and the system prompts, “Delete this Future Effective
    record?”

    -   Select **Delete** to delete the displayed Future Effective record. Then
        there are checks to determine if there are corresponding Future
        Effective records in Payroll, if there are then the system prompts a
        message asking if the corresponding Future Effective records from
        Payroll should be deleted. If the answer is yes, then select Yes, and
        then all Human Resources and Payroll Future Effective records are
        deleted for that code. If the answer is No and No is selected, then only
        the Human Resources Future Effective records are deleted for that code.

    -   Select **Cancel** to return to the current Future Effective record.

-   **Reports** are only available if the Future Effective record is open.

>   *NOTE: Future Effective amounts are not reported on the Reports generated
>   from the Reports \> Human Resources menu.*

>   If a Future Effective record is created for a Human Resources code that does
>   not exist in Payroll and corresponding is set up in Payroll, the system
>   prompts, “The Payroll Benefit must exist before a Future Effective Record
>   can be created.” Select OK.

>   *NOTE: When Future Effective records are created, you should not select to
>   roll down to Payroll or Human Resources. This roll down functionality does
>   not apply to the future effective records.*

### Editing and Viewing an Existing Future Effective Record

>   To open an existing Benefits and Deduction Setup window, click the **HR and
>   Payroll** series button, click **Human Resources** on the Setup content
>   pane, click **Benefits and Deductions**, click **Miscellaneous Benefits**,
>   **Health Insurance**, **Life Insurance** or **Retirements Plans**, click the
>   **GoTo** menu and then click **Future Effective**.

>   The system prompts, “Display future effective record?”

-   Select **Yes** to open the current Future Effective record in the Future
    Effective window. For Human Resources the system then prompts to verify the
    Future Effective Date, leave the date as entered or edit the date and select
    OK.

-   Select **No** to return to the current core record.

-   Select **Save** to save and the system prompts, “Save future effective
    record?” o Select **Save** to save the current Future Effective record. o
    Select **Cancel** to return to the current Future Effective record.

>   Roll down from HR/Payroll Setup level to existing Employee level HR/Payroll
>   records exists so beware of the selection to this message when saving Future
>   Effective records. Select **No**; Future Effective functionality is for the
>   Benefit and Deduction Setup windows only.

-   Select **Clear** to clear the record from the window and set the window back
    to the core record.

-   Select **Delete** to delete the record, the system prompts “Delete this
    Future Effective record?”

>   o Select **Delete** to delete the displayed Future Effective record. Then
>   there would be checks if there were corresponding Future Effective records
>   in Payroll, if so the system prompts with a message asking to delete
>   corresponding Future Effective records from Payroll. If Yes is selected,
>   then all Human Resources and Payroll Future Effective records are deleted
>   for that code. If No is selected, then only the Human Resources Future
>   Effective records are deleted for that code. o Select **Cancel** to return
>   to the current future effective record.

-   **Reports** are only available while a Future Effective record is open.

### Saving in Payroll

>   When saving a future effective record in Payroll, the system prompts,

>   “Save future effective record?”

-   Select **Save** to save the current future effective record.

    -   The system prompts, “The information for the Payroll deduction code is
        different than the Human Resources deduction code. Do you want to
        continue?”

-   Selecting **Yes** prompts, “These changes must be saved in the Benefit Setup
    window to take effect across Human Resources with Integration to Payroll.
    When the Benefit Setup window opens, choose Save to save changes.” Click OK.

-   Selecting **No** cancels the message and returns to the Future Effective
    record.

-   Select **Cancel** to return to the current Future Effective record window.

>   Select **Save** to save this operation, the system prompts, “Save future
>   effective record?”

-   Select **Save** to save the current future effective record.

    -   The system prompts, “The information for the Payroll deduction code is
        different than the Human Resources deduction code. Do you want to
        continue?”

-   Select **Yes** or

-   Select **No**

-   Select **Cancel** to return to the current Future Effective record window.

>   Select **Clear** to clear the window and return to the core window.

### Saving in Human Resources

>   Next, the system prompts, “Do you want to set up the corresponding codes in
>   Payroll so the integration is complete?”

-   Select **Yes** to open the Payroll Deduction window and default all values
    from the Human Resources Future Effective record. Once the record is saved
    in this window, the Payroll Benefit window opens and defaults to save as
    well.

-   Select **No** to save the Future Effective record only in Human Resources
    and return to the core window.

>   If this operation should **NOT** be saved, click **Cancel**. It returns to
>   the Future Effective record.

>   Click **OK** when prompted, “These changes must be saved in the Benefit

>   Setup window to take effect across Human Resources with Integration to
>   Payroll.” When the Benefit Setup window opens, select **Save** to save
>   changes.

### Employee Dependents Window

>   Within the Employee Dependents window data fields have been added to use to
>   set up dependents associated with the employee. To open this window, click
>   the **HR and Payroll** series button, click **Human Resources** on the Cards
>   content pane, click **Employee** and then click **Dependents**.

IMAGE – ADVHRDEP

![A screenshot of a cell phone Description automatically generated](media/aef7d41c75511a0b9c39b7e944629bb0.jpg)

#### FIGURE 2.2 EMPLOYEE DEPENDENTS WINDOW

>   The additional data fields are:

-   **Status** - select Active or Inactive

-   **Status Comment** - these options are defined in the Plan Status Reason
    window

-   **Change Date**

-   **Marital Status** - select Married, Single or N/A

-   **Change Date**

-   **Disabled** checkbox

-   **Disabled Date**

### Employee Beneficiaries Window

>   Within the Employee Beneficiaries window additional data fields are
>   available, to define beneficiaries associated with the employee and specific
>   benefit plan. To open this window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Cards content pane, click
>   **Employee - Benefits**, select a **Benefit**, select an **Employee ID**,
>   click the **Benefit** icon, and click **Beneficiary Definition**.

IMAGE - ADVHRBENF.jpg

![A screenshot of a cell phone Description automatically generated](media/4341819673bb483f27befe0e7bf70ece.jpg)

#### FIGURE 2.3 EMPLOYEE BENEFICIARIES WINDOW

>   The data fields are:

-   **Plan Status** - select Active or Inactive

-   **State Change Reason** - the lookup button allows information to be
    defaulted from existing Dependents.

-   **Status Comment** - these options are defined in the Plan Status Reason
    window

-   **Change Date**

-   **Marital Status** - select Married, Single or N/A

-   **Change Date**

-   **Disabled** checkbox

-   **Disabled Date**

### Employee Benefit Dependents Window

>   The Employee Benefit Dependents window allows Human Resources to define the
>   employee dependents associated with a specific employee benefit plan. To
>   open this window, click the **HR and Payroll** series button, click **Human
>   Resources** on the Cards content pane, click **Employee -**

>   **Benefits**, select a **Benefit**, select an **Employee ID**, select a
>   **Benefit Code**, click the **Benefit** icon, and click **Dependents**.

IMAGE – ADVHRBD

![A screenshot of a cell phone Description automatically generated](media/b1ed05943d5e7de57ef712998bb236ca.jpg)

#### FIGURE 2.4 EMPLOYEE BENEFIT DEPENDENTS WINDOW

>   Complete the **Plan Status** and **Status Change Reason** fields as
>   appropriate.

### Plan Status Reasons Window

>   The Plan Status Reasons window allows Human Resources to define acceptable
>   Reasons for why a particular dependent or beneficiary were activated or
>   inactivated from a benefit plan. This information is necessary to provide to
>   benefit carriers. To open the Plan Status Reasons window, click the **HR and
>   Payroll** series button, click **Human Resources** on the Setup content pane
>   and then click **Plan Status Reasons**.

>   Select a **Record Type** and then select a **Status Type**.

### Benefit Options Window

>   To open the Benefit Options window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Setup content pane, select a
>   **Benefit** window, select a **Benefit Code**, click the **Benefits** icon
>   and then click **Benefit Options**.

IMAGE – ADVHRBO.jpg

![A screenshot of a cell phone Description automatically generated](media/faf062154592f53ea4f1a15d66bca5d4.jpg)

>   Each of the Benefit Setup windows (Miscellaneous Benefits, Health Insurance,
>   Life Insurance and Retirement Plans) has the Benefit Options item added to
>   the Benefits button. When Benefit Options is selected this will allow the
>   user to define the maximum number of dependents allowed for the specified
>   benefit.

>   *NOTE: A Benefit Setup record must be displayed within the window to open
>   Benefit Options.*

>   This window allows the user to set the Maximum Dependents Allowed. The
>   Maximum Dependents Allowed will be validated when enrollment changes are
>   made to the benefit record.

>   By default, the number of dependents is set to zero which means unlimited if
>   the Benefit Self Service module is not being used.

### Certification, License and Training Manager Setup

>   There are several set up windows associated with Certification, License and
>   Training Manager:

-   Issued By Setup

-   Instructor Setup

-   Endorsement Setup

-   Certification Setup

-   License Type Setup

>   In addition, several other windows can be completed at this point in the
>   process:

-   Training Course Definition Additional Information window

-   Class Points window

-   Certification, License and Training Required by Dept and Position window

### Issued By Setup Window

>   Use the Issued By Setup window to set up, assign an unlimited number of

>   Issued By Agencies with description, contact and address information. An
>   Issued By could be Agency or other organization. To open this window, click
>   the **HR and Payroll** series button, click **Human Resources** on the Setup
>   content pane, click **Certifications, Licenses and Training** and then click
>   **Issuers**.

IMAGE – ADVHRISS.jpg

![A screenshot of a cell phone Description automatically generated](media/da6d7897048bebdeb57e7d4db16c7719.jpg)

>   Enter or select an **Issued By Agency**.

>   Enter the following information:

-   **Description**

-   **Contact Name**

-   **Address 1**

-   **Address 2**

-   **City**

-   **State**

-   **Zip Code**

-   **Phone Number**

-   **Fax Number**

-   **Web Site**

-   **E-mail**

>   Select the **Inactive** checkbox to inactivate the current Issued By Agency
>   code.

### Instructor Setup Window

>   Use the Instructor Setup window to set up, assign unlimited number of
>   Instructors with contact and address information. To open this window, click
>   the **HR and Payroll** series button, click **Human Resources** on the Setup
>   content pane, click **Certifications, Licenses and Training** and then click
>   **Instructors**.

IMAGE – ADVHRINS

![A screenshot of a cell phone Description automatically generated](media/1cd28ed5b5629e37581c7374f930f486.jpg)

>   Enter or select **Instructor ID**.

>   Enter the following information:

-   **Instructor Name**

-   **Address 1**

-   **Address 2**

-   **City**

-   **State**

-   **Zip Code**

-   **Phone Number**

-   **Fax Number**

-   **Web Site**

-   **E-mail**

>   Select the **Inactive** checkbox to inactivate the current instructor ID
>   code.

### Endorsement Setup Window

>   Use the Endorsement Setup window to define the Endorsements by Certification
>   or License. To open this window, click the **HR and Payroll** series button,
>   click **Human Resources o**n the Setup content pane, click **Certifications,
>   Licenses and Training** and then click **Endorsements**.

>   Select the **Type**:

-   Certification

-   License

>   Enter the new **Endorsement** or edit the Endorsement for the selected Type.

>   Select **OK** to save the Endorsement Setup and close the window.

>   To delete a row, select the Endorsement and then select the delete row
>   button to delete this Endorsement.

### Certification Setup Window

>   Use the Certification Setup window to set up and assign unlimited number of
>   Certifications with descriptions. To open this window, click the **HR and
>   Payroll** series button, click **Human Resources** on the Setup content
>   pane, click **Certifications, Licenses and Training** and then click
>   **Certifications**.

IMAGE – ADVHRCS.jpg

![A screenshot of a cell phone Description automatically generated](media/442e889d717a4be412c2448f61e209cb.jpg)

>   When entering a new Certification Code, enter a **Description** and select
>   any **Required** options.

-   **Issued By Agency**

-   **Original Issue Date**

-   **Expiration Date**

-   **Certification Number**

-   **Date Renewed**

>   Selecting any of the **Required** options affects the Employee Certification
>   Entry window by forcing entry of a value in the field prior to saving the
>   record.

>   Select the **Inactive** checkbox to inactivate the current Certification
>   Code.

### Certification Endorsements Window

>   Use the Certification Endorsements window to mark the appropriate
>   Endorsement that was created during the Endorsement Setup. To open this
>   window, click the **Endorsements** button on the Certification Setup window.

>   The **Marked** column indicates the Endorsements that are marked for the
>   specific Certification Code. Use **Mark All** and **Unmark All** to mark or
>   unmark all Endorsements at once.

>   Select **OK** to save the Endorsement Assignment and close the window.

### License Type Setup Window

>   Use the License Type Setup window to set up and assign unlimited number of
>   License Types with descriptions. To open this window, click the **HR and
>   Payroll** series button, click **Human Resources** on the Setup content
>   pane, click **Certifications, Licenses and Training** and then click
>   **License Types**.

IMAGE – ADVHRLS.jpg

![A screenshot of a cell phone Description automatically generated](media/31780b0c27992aefbc525bd2adbf7a77.jpg)

>   Enter or select a **License Type**.

>   When entering a new License Type, complete the **Description**, select the
>   appropriate **Required** options and assign **Endorsements**.

-   **Issued By Agency**

-   **Date Renewed**

-   **Expiration Date**

-   **Issued By State**

-   **Original Issue Date**

>   Selecting any of the fields as **Required** affects the Employee License
>   Entry window by forcing entry of a value in the field prior to saving the
>   record.

>   Select the **Inactive** checkbox to inactivate the current Certification
>   Code.

### License Type Endorsements Window

>   Use the License Endorsements window to select the appropriate Endorsement
>   that was created during the Endorsement Setup. To open this window, click
>   the **Endorsements** button on the License Type Setup window.

>   The **Marked** column indicates the Endorsements that are marked for the
>   specific License Code. Use **Mark All** and **Unmark All** to mark or unmark
>   all Endorsements at once.

>   Select **OK** to save the Endorsement Assignment and close the window.

### Training Course Definition Additional Information Window

>   Use the Training Course and Class Definition window to set up a training
>   course. The Certification, License and Training Manager has extended the
>   Course set up with additional fields on the new Training Course Definition
>   Additional Information window. To open this window, click the **HR and
>   Payroll** series button, click **Human Resources** on the Setup content
>   pane, click **Certifications, Licenses and Training** and then click
>   **Training Additional Info**.

IMAGE – ADVHRTCS.jpg

![A screenshot of a cell phone Description automatically generated](media/aaab29d5481f1423098576df5af5f4ed.jpg)

>   Enter or select a **Course ID**. The **description** field displays from the
>   Training Course and Class Definition window. Check the boxes for fields that
>   are to be **Required** on the Employee Training window.

>   Select the **Inactive** checkbox to inactivate the current Course ID.

### Class Points Window

>   Use the Class Points window to add points to the individual class
>   combination. To open this window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Setup content pane, click
>   **Training**, select a **Course ID**, select a **Class**, click
>   **Additional** from the menu and then click **Class Points**.

>   Enter a **Points** value for the selected class (ex: time length of class).

>   Select **OK** to save and close the Class Points window.

### Certification, License and Training Required by Dept and Position Window

>   Use the Certification, License and Training Required by Department and
>   Position window to assign to a specific Position and Department combination
>   and any required certifications, licenses or training. To open this window,
>   click the **HR and Payroll** series button, click **Human Resources** on the
>   Setup content pane, click **Certifications, Licenses and Training** and then
>   click **Requirements**.

>   Use this window to add, update or remove from a list any required
>   certifications, licenses or training.

>   Enter or select a **Department** and **Position**.

>   **Required Certifications** section within the scrolling window allows the
>   user to assign any Certification Codes that are required for the currently
>   selected Department and Position. Enter or delete the Certification Codes as
>   required. To delete the Certification Code, select the code and then select
>   delete row button.

>   **Required Licenses** section within the scrolling window allows the user to
>   assign any License Types that are required for the currently selected
>   Department and Position. Enter or delete the License Types as required. To
>   delete the License Type, select the type and then select delete row button.

>   **Required Training** section within the scrolling window allows the user to
>   assign any Course IDs that are required for the currently selected
>   Department and Position. Enter or delete the Course IDs as required. To
>   delete the Course ID, select the course id and then select delete row
>   button.

>   Once a Department and Position have been selected, the **Copy** button is
>   enabled. Selecting Copy opens the Copy Requirements window and allows the
>   user to copy all of the Required Certifications, Licenses and Training
>   associated with the currently open Department/Position combination to
>   another Department/Position combination.

>   Enter or select the **Copy To Department** and **Copy To Position**. Select
>   **Copy** to complete the copy process or select **Cancel** to cancel the
>   copy process.

Employee Health and Wellness Manager - Setup
--------------------------------------------

>   There are several set up windows associated with Employee Health and
>   Wellness:

-   Category Setup window

-   Results Setup window

-   Health and Wellness Code Setup window

-   Health and Wellness Template Setup window

-   Sources Setup window

### Health and Wellness Code Setup Window

>   Use the Health and Wellness Code Setup window to set up and assign unlimited
>   number of Codes with descriptions and be able to set the status of the code
>   to Active or Inactive. To open this window, click the **HR and Payroll**
>   series button, click **Human Resources** on the Setup content pane, click
>   **Health and Wellness** and then click **Codes**.

IMAGE – ADVHRHCS.jpg

![A screenshot of a cell phone Description automatically generated](media/e200fd48fb3a0f3622532c5d5f5c7b1c.jpg)

>   Examples of Health and Wellness Codes are Rubeola, Rubella, Booster,
>   Hepatitis C, Pertussis Exposure, Laser Screening, Hearing Protection and Eye
>   Exams.

>   For each Code the user will be able to set up results, such as Positive or
>   Negative. These results will then be available as choices on the Employee
>   Health and Wellness Entry window.

>   Enter or select a **Code**; enter or modify the **Description** and enter or
>   select the **Category**.

>   The scrolling window allows the user to apply the Results that relate to the
>   current Health and Wellness code.

-   **Checkbox** will activate the Result

-   Enter or select a **Result Code**

-   The **Description** displays from the Result Setup window

>   **Result Setup Window**

>   Use the Result Setup window to set up and assign unlimited number of Result
>   Codes with descriptions and be able to set the status of the code to Active
>   or Inactive. To open this window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Setup content pane, click **Health
>   and Wellness** and then click **Results**.

>   Enter or select a **Result Code**. Enter or modify the **Description**.

>   Select the **Inactive** checkbox will inactivate the current Result Code.

>   Select **Save** to save the Result Code.

### Health and Wellness Template Setup Window

>   Use the Health and Wellness Template Setup window to set up and assign
>   unlimited number of Templates with descriptions and be able to set the
>   status of the Template to Active or Inactive. To open this window, click the
>   **HR and Payroll** series button, click **Human Resources** on the Setup
>   content pane, click **Health and Wellness** and then click **Templates**.

>   Employee defined templates can be used to assign defaults to employees. One
>   template setup assigned can easily establish all the tests required by a
>   certain position, employee class or grouping specific to each facility.

>   Enter or select a **Template Code** and enter or modify the **Description**.

>   The scrolling window allows the user to associate Health and Wellness Codes
>   with a Template Code.

>   Enter or select a **Health and Wellness Code**.

>   The **Description** displays from the Health and Wellness Code Setup window.

>   The **Category and Description** displays from the Category Setup window.

### Source Setup Window

>   Use the Source Setup window to create Source records. To open this window,
>   click the **HR and Payroll** series button, click **Human Resources** on the
>   Setup content pane, click **Health and Wellness** and then click
>   **Sources**.

>   Enter or select a **Source ID**.

>   Enter the **Last Name**, **First Name**, **Middle Name**, **Social Security
>   Number** and **Medical Record Number**.

>   Select **Save** to save the Source ID.

### Category Setup Window

>   Use the Category Setup window to set up an unlimited number of Category
>   Codes with descriptions and be able to set the status of the code to Active
>   or Inactive. The Category Code can be used for report grouping and
>   restrictions. Example: Immunizations, Vaccinations, Blood Exposure, Injuries
>   and Tests. To open this window, click the **HR and Payroll** series button,
>   click **Human Resources** on the Setup content pane, click **Health and
>   Wellness** and then click **Categories**.

>   Enter or select a **Category Code**. Enter or modify the **Description**.

>   Select the **Inactive checkbox** to inactivate the current Category Code.

>   Select **Save** to save the Category Code.

Summary
-------

>   A variety of setup windows need to be completed prior to using the

>   Advanced Human Resources module. Each of the components to Advanced Human
>   Resources has dedicated windows for this purpose.

>   Key points to remember from this chapter:

-   Future Effective records can be set up to pre-enter information for upcoming
    changes to benefit plans.

-   After completing the appropriate setup for Certification, License and
    Training Manager, certifications, licenses and training can be assigned to a
    department and position combination as required.

-   Templates can be developed to assign predetermined health and wellness codes
    that will eventually be assigned on the employee level.

## CHAPTER 3: EMPLOYEE MAINTENANCE

The objectives are:

-   Learn to effectively use Benefit Lifecycle Manager by understanding (1) the
    changes on the employee dependents window, (2) the changes on the employee
    beneficiary window, (3) how to connect benefits to dependents and (4) how to
    activate Future Effective records.

-   Assign certifications, licenses and training to employee records.

-   Learn to assign Health and Wellness codes, categories and templates to
    employees and to track source information in the event of a work-related
    injury or illness.

### Introduction

>   After completing the required setup in Chapter 2, the next step is to assign
>   data to employee records. Advanced Human Resources allows the organization
>   to input data for benefit plan changes in advance of the effective date by
>   using future effective records, allows certifications, licenses and training
>   courses and classes to be assigned to individual employees once attained or
>   completed, and finally allows for the collection of additional data for a
>   work-related injury or illness.

### Benefit Lifecycle Manager

>   The first component of Advanced Human Resources is the Benefit Lifecycle
>   Manager. This component has added additional fields to the employee
>   dependent and beneficiary windows. In addition, benefits can now be assigned
>   to dependents for better tracking of insurance coverages and costs.

#### Employee Dependents Window

>   Within the Employee Dependents window, data fields have been added to set up
>   dependents associated with the employee. To open this window, click the **HR
>   and Payroll** series button, click **Human Resources o**n the Cards content
>   pane, click **Employee** and then click **Dependents**.

>   The data fields are listed below:

-   **Status** – Active or Inactive

-   **Status Comment** – These options are defined in the Plan Status Reason
    window

-   **Change Date**

-   **Marital Status** – Married, Single or N/A

-   **Change Date**

-   **Disabled** checkbox

-   **Disabled Date**

#### Employee Beneficiaries Window

>   Within the Employee Beneficiaries window, additional data fields are
>   available to define beneficiaries associated with the employee and specific
>   benefit plan. To open this window, click the **HR and Payroll** series
>   button, click the **Human Resources** on the Cards content pane, click
>   **Employee - Benefits**, select a **Benefit Enrollment** option, select an
>   **Employee ID**, select a **Benefit code**, click the **Benefit** icon and
>   then click **Beneficiary Definition**.

>   The data fields are listed below:

-   **Plan Status** – Active or Inactive

-   **Status Change Reason** – lookup button now allows information to be
    defaulted from existing Dependents.

-   **Status Comment** – These options are defined in the Plan Status Reason
    window

-   **Change Date**

-   **Marital Status** – Married, Single or N/A

-   **Change Date**

-   **Disabled** checkbox

-   **Disabled Date**

#### Assign Template Window

>   Selecting a Template will create employee and code records for all codes
>   associated with that Template. You can then assign any Dates and Results to
>   those codes in this window.

>   Example: There may be a template for New Employees that would have listed 5
>   Immunizations, Vaccinations and Tests that a new employee would need. You
>   could assign that template and the system would create the 5 records. If
>   only 3 were needed, then you would uncheck the 2 that do not apply.

>   To open the Assign Template window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Cards content pane, click
>   **Employee**, click **Health and Wellness**, enter an **Employee ID** and
>   then click the **Assign Template** button.

1.  Enter or select a **Template Code**.

2.  The **Description** displays from the Health and Wellness Template Setup
    window.

3.  The Scrolling window allows you to associate Health and Wellness codes with
    a Template Code.

#### Employee Benefit Dependents Window

>   The Employee Benefit Dependents window allows Human Resources to define the
>   employee dependents associated with a specific employee benefit plan. To
>   open this window, click the **HR and Payroll** series button, click **Human
>   Resources** on the Cards content pane, click **Employee - Benefits** and
>   select a **Benefit Enrollment** option, enter an **Employee ID**, select a
>   **Benefit code**, click the **Benefits icon** and then click **Dependents**.

#### Future Effective Activation Window

>   The Future Effective Activation window is used to activate the future
>   effective date records. The following steps should be followed. To open this
>   window, click the **HR and Payroll** series button, click **Human
>   Resources** on the Utilities content pane and then click **Activate Future
>   Effective Benefits**.

IMAGE – ADVHRFES.jpg

![A screenshot of a social media post Description automatically generated](media/1ade2b756a776e7e0a648332366d701c.jpg)

>   Within the Future Effective Activation scrolling window, the records can be
>   sorted ascending or descending by columns. This window will display all
>   Future Effective records that currently exist and will default sorted by
>   Effective Date in ascending order.

-   Select the **Activate** checkbox to process the Future Effective Activation
    for this benefit code. When selected, if corresponding HR or Payroll Future
    Effective records exist the system prompts: “Do you want to select
    corresponding HR/Payroll records?

    -   **Yes** prompts the user to select the Activate checkbox for all records
        that exist equal to the Benefit Code.

    -   **No** prompts the user to select the Activate checkbox for the one
        record.

>   Select **Mark All** or **Unmark All** to select or unselect all Future
>   Effective records displayed in the scrolling window.

-   **Process** validates that there are current records marked as ACTIVATE.

    -   If there are no current records marked as ACTIVATE or any records
        available to process, the system prompts: “You have not marked any
        records for processing.”

    -   If there are current records marked as ACTIVATE the process moves the
        current Microsoft Dynamics GP records to the Benefit Lifecycle Manager
        history tables, then moves the Benefit Lifecycle Manager Future
        Effective records into the core Microsoft Dynamics GP tables and remove
        them from the Benefit Lifecycle Manager pending tables. Remember to
        ACTIVATE the codes on or past the Effective Date. By ACTIVATING before
        the Effective Date will make the changes current, regardless of the
        Effective Date.

>   Once the process is complete, the window will close.

>   The records in the window can be printed by selecting the **Print** icon on
>   the window. The print will display the records in the order that they appear
>   on the window.

### Certification, License and Training Manager

>   The next component of Advanced Human Resources is Certification, License and
>   Training Manager. Using this component, the user can assign certifications
>   such as a Human Resources certification to a particular employee. In
>   addition, licenses with unique identifying numbers can be assigned. This
>   could be as simple as a driver’s license or as complex as the DEA and other
>   Medical Licenses required by a doctor. Another part of Advanced Human
>   Resources enhances the Employee

>   Training window allowing more information to be tracked. Finally, Advanced
>   Human Resources allows the user to update multiple employee training records
>   with completion and expiration dates by using a course/class combination.

#### Certification Entry Window

>   Use the Certification Entry window to add or update the Certification data
>   for a specific employee. Multiple certifications may be assigned to an
>   employee. You will be able to quickly update the expiration date of a
>   certification and retain the prior expiration date for historical purposes.

>   To open the Certification Entry window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Cards content pane, click
>   **Employee** and then click **Certifications**.

IMAGE – ADVHRCE.jpg

![A screenshot of a cell phone Description automatically generated](media/98a5dbc9b7beb772987bd6f60ceafdb3.jpg)

>   Enter or select an **Employee ID** to assign the Certification Code. The
>   **Department** and **Position** fields displays from the Employee
>   Maintenance window.

>   Enter or select a **Certification Code**.

>   The following fields may or may not be required based on the Training Course
>   Required options selected on the Certification Setup window:

-   **Issued By Agency**

-   **Original Issued Date**

-   **Expiration Date**

-   **Certification Number**

-   **Date Renewed**

>   Use the **User Defined** textboxes to track four additional pieces of
>   Certification related information.

>   Select the **Endorsements** button to open the Endorsement Employee
>   Certification Assignment window.

>   Select the **History** button to open the Certification History window to
>   display the history information corresponding to the Certification Entry
>   record currently open.

>   The **Inactive** checkbox will inactivate the current Certification Entry.

>   Information on this window can be made available to employees and their
>   managers by using.

#### License Entry Window

>   Use the License Entry window to add or update License data for a specific
>   employee. Multiple licenses may be assigned to an employee. You will be able
>   to quickly update the expiration date of a license and retain the prior
>   expiration date for historical purposes.

>   To open this window, click the **HR and Payroll** series button, click
>   **Human Resources** on the Cards content pane, click **Employee** and then
>   click **Licenses**.

IMAGE – ADVHRLE.jpg

![A screenshot of a cell phone Description automatically generated](media/994e2eac7970533aaad91c7453d9f2ba.jpg)

1.  Enter or select an **Employee ID** to assign the License Number. The
    **Department** and **Position** fields displays from the Employee
    Maintenance window.

2.  Enter a **License Number**. This number must be unique and not assigned to
    any employee.

3.  Select or enter a **License Type** that corresponds to the **License
    Number**.

4.  Use the **User Defined** textboxes to track four additional pieces of
    License related information.

5.  Select **Endorsement** to open the Endorsement Employee License Assignment
    window.

6.  Select **History** to open the License History window to display the history
    information corresponding to the License Entry record currently open.

>   The **Inactive** checkbox will inactivate the current License Entry.

>   Information on this window can be made available to employees and their
>   managers by using.

#### Employee Training Window

>   The modified Employee Training window replaces the Core Employee Training
>   window. To open the Employee Training window, click the **HR and Payroll**
>   series button, click **Human Resources** on the Cards content pane, click
>   **Employee** and then click the second **Training** option.

IMAGE- ADVHRET.jpg

![A screenshot of a cell phone Description automatically generated](media/390bb07315226e87967e6126fbeb485a.jpg)

>   The additional fields include the following:

-   **Given By Organization** - enter the name of the Organization led the class

-   **Instructor ID** - enter the name of the instructor

-   **Expiration Date** - enter the expiration date for this class

-   **Score** - enter the score that the employee earned for this class

-   **Inactive** - select the inactive checkbox if appropriate for the employee

>   Enter or select an **Employee ID**. The **Department** and **Position**
>   fields displays from the Employee Maintenance window.

>   Enter or select a **Course ID** and **Class ID**.

>   Enter or select the following if the field is Required based on the Training
>   Course Definition Additional Information window:

-   **Given By Organization**

-   **Instructor ID**

-   **Score**

>   Enter a **Comment** when applicable.

>   Enter or select a **Completed Date** and **Expiration Date**.

>   Select the **Completed** checkbox to select this Course ID/Class ID as
>   completed when applicable.

>   Select the **Inactivate** checkbox to inactivate this Course ID/Class ID
>   when applicable.

>   Select the **History** button to open the Training History window for the
>   corresponding Employee Training record currently open.

>   Information on this window can be made available to employees and their
>   managers by using.

#### Mass Training Update Window

>   The Mass Training Update feature allows the user to access one window where
>   any/all employee(s) can be updated for a Course and Class combination
>   including the additional information made available in Certification,
>   License and Training Manager as it relates to the completion and expiration
>   dates of their training.

>   To open the Mass Training Update window, click the **HR and Payroll** series
>   button, click **Human Resources** on the **Utilities** content pane and then
>   click **Mass Training Update**.

>   Enter or select the **Course ID**, **Class ID**, **Instructor ID**, **Given
>   By Organization**, **Completed Date** and **Expiration Date**.

>   Update Records will allow you to update multiple employee records by
>   **Instructor ID**, **Given By Organization**, **Completed Date** and/or
>   **Expiration Date**.

### Employee Health and Wellness Manager

>   Health and Wellness information can be tracked for employees including
>   additional information for work-related injuries and illnesses. For example
>   in the health care industry an employee may be required to have certain
>   vaccinations or immunizations and to keep them up to date during their
>   employment. This information, along with results can be tracked by assigning
>   the various categories and codes set up to an employee.

>   There is also additional information that can be collected by employee for a
>   work-related injury or illness. Source information can be added to the
>   records allowing the user to simultaneously track ongoing treatment for both
>   parties.

#### Health and Wellness Entry Window

>   Use the Health and Wellness Entry window to provide features for tracking
>   all immunizations, vaccinations and tests required for each employee. The
>   results for each test can also be recorded.

>   To open the Health and Wellness Entry window, click the **HR and Payroll**
>   series button, click **Human Resources** on the Cards content pane, click
>   **Employee** and then click **Health and Wellness**.

>   Enter or select an **Employee ID**. The **Description** displays from the
>   Employee Maintenance window.

>   Enter or select the **Health and Wellness Code** that you wish to assign to
>   employee. The **Description** and **Category** displays from the Health and
>   Wellness Code Setup window.

>   Enter or select the **Date Entered**, **Result** and **Renew Date**.

>   Select the **History** button to open the Health and Wellness History window
>   for the current employee and code.

#### Injury and Illness Details Window

>   The purpose of the Injury and Illness Details window is to provide features
>   for tracking injury information for each employee and sources. The results
>   for each test can also be recorded.

>   The Injury and Illness Detail window will enable you to schedule follow-up
>   vaccinations, immunizations and tests. The history will be tracked
>   indefinitely for each incident of immunizations, vaccinations and tests.

>   To open the Injury and Illness Details window, click the **HR and Payroll**
>   series button, click **Human Resources** on the Cards content pane, click
>   **Employee** and then click **Injury and Illness Details**.

IMAGE – ADVHRII.jpg

![A screenshot of a social media post Description automatically generated](media/01f4a8079047950b6cc79763cae9b080.jpg)

>   Enter or select an **Employee ID**. The **Description** displays from the
>   Employee Maintenance window.

>   Enter or select a **Case \#**.

>   The scrolling window allows you to enter Injury and Illness data related to
>   the Employee and Case Number selected.

>   The **Assign Template** button opens the Assign Templates window.

>   The **Source Information** section allows you to enter the Source related to
>   this Employee and Case Number.

>   Enter or select a **Source ID**. The **Social Security Number**, **Last
>   Name** and **First Name** displays from the Source Setup window.

>   The Source Health and Wellness Codes scrolling window allows you to enter
>   Injury and Illness data related to the Employee and Case Number and Source
>   ID selected.

>   The **Assign Template** button will open the Assign Templates window.

#### Assign Templates Window

>   Use the Assign Template window to check which line items from the
>   appropriate template to assign to an employee or source.

>   To open the Assign Templates, click the **HR and Payroll** series button,
>   click **Human Resources** on the Cards content pane, click **Employee**,
>   click **Injury and Illness Details** and then click the **Assign Template**
>   button.

>   Enter or select a **Template Code**. The **Description** displays from the
>   Health and Wellness Template Setup window.

>   Health and Wellness Codes scrolling window allows you to associate Health
>   and Wellness codes with a Template Code.

### Summary

>   Advanced Human Resources allows for the tracking of additional dependent and
>   beneficiary information, as well as allowing benefit information to be
>   assigned to dependents. In addition, the organization can track information
>   related to certifications and licenses held by their employees. Finally,
>   Health and Wellness information can be tracked for employees including
>   additional information for work-related injuries and illnesses.

>   Key points to remember from this chapter:

-   Assign benefit plans to enrolled dependents.

-   Future Effective records need to be activated on or after the effective
    date.

-   Certifications and Licenses can be tracked as they relate to employees
    including the related history.

-   Employee records can be updated with course and class completion and
    expiration dates using the Mass Training Update feature.

-   Templates can be assigned to employees for health related data or in the
    case of a work-related injury or illness.

-   Source data can be tracked for work-related injuries and illnesses.

## CHAPTER 4: INQUIRIES AND REPORTS
The objectives are:

-   Review the inquiries available for Advanced Human Resources and learn to
    print the information found on the various screens.

-   Understand the options available for printing reports in Advanced Human
    Resources.

### Introduction

>   Advanced Human Resources provides both Inquiry windows and the ability to
>   print reports. The Inquiry windows for the most part are the history windows
>   for most of the components. The exception to this is the Percent Current
>   Inquiry, which is an inquiry allowing for various selections to be made to
>   narrow or broaden the scope of records shown.

### Inquiries

>   The Advanced Human Resources Inquiries contain the history windows for
>   Certification, License and Training Manager, as well as the inquiry for
>   Percent Current. The information on the windows can be printed from the
>   window. In the case of the Percent Current Inquiry, both the information on
>   the screen and a Percent Current Totals report can be printed using the
>   printer icon on the window.

#### Certification History

>   Use the Certification History window to view all the activity for a specific

>   Employee/Certification record. The history record is written as the latest
>   History record when changes are saved on the Certification Entry window.

>   To open the Certification History window, click the **HR and Payroll**
>   series button, click **Human Resources** on the Inquiry content pane and
>   then click **Certification History**.

>   Enter or select an **Employee ID**. The **Department** and **Position**
>   fields displays from the Employee Maintenance window.

>   Enter or select a **Certification Code** for current Employee.

>   The **Inactive** checkbox will inactivate the current Certification History.

#### License History

>   Use the License History window to view all the activity for a specific

>   Employee/License record. The history record is written as the latest History
>   record when changes are saved on the License Entry window.

>   To open the License History window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Inquiry content pane and then click
>   **License History**.

1.  Enter or select an **Employee ID**. The **Department** and **Position**
    fields displays from the Employee Maintenance window.

2.  Enter or select a **License Number** for the current Employee.

>   The **Inactive** checkbox will inactivate the current License History.

#### Training History

>   Use the Training History window to view all the transactions by Course/Class
>   ID for a specific employee. The history record is written as the latest
>   History record when changes are saved on the Employee Training window.

>   To open the Training History window, click the **HR and Payroll** series
>   button, click **Human Resources** on the Inquiry content pane and then click
>   **Training History**.

#### FIGURE 4.3 TRAINING HISTORY WINDOW

>   *Note: Training that the employee has taken will appear on the Employee
>   Training window.*

>   Enter or select an **Employee ID**. The **Department** and **Position**
>   fields will display from the Employee Maintenance window.

#### Percent Current Inquiry

>   Use the Percent Current Inquiry window to measure actual versus requirements
>   for all positions within a department vs. position by position. To open this
>   window, click the **HR and Payroll** series button, click **Human
>   Resources** on the Inquiry content pane and then click **Percent Current**.

IMAGE - ADVHRPC.jpg

![A screenshot of a cell phone Description automatically generated](media/232fbd0fb458f93e27b3d063fe7c83c6.jpg)

>   Enter or select a **Department** and **Position**.

>   Select the **Include all Positions** checkbox to select all Positions within
>   the selected Department. All positions are checked that have a relationship
>   with the selected department in the “Certification, License and Training
>   Required by Department and Position” window.

>   Select an **Include Employees** option:

-   **Home:** Includes employees that have the current Department and Position
    as their Home Department and Position.

-   **Worked:** Includes employees that have worked in the current Department
    and Position.

-   **Both:** Includes both Home and Worked employees.

>   Select an **Include Codes** option:

-   **All:** Displays ALL codes

-   **Required:** Displays only the Required Certification, License or Training
    codes.

>   Select an **Include Qualifications**:

-   **All:** Displays ALL Qualifications

-   **Qualified:** Displays Qualified employees.

-   **Not Qualified:** Displays non-qualified employees.

>   Select a **Display** and **Status**.

>   Enter or select a **Code**, **Employee ID** and **Expiration Date**.

>   Select the **Printer** button to print the Percent Current Inquiry Report
>   and Percent Current Totals Report.

IMAGE – ADVHRPCR.jpg and ADVHRPCR2.jpg

![A screenshot of a cell phone Description automatically generated](media/69da87abc6a0daeda941826219b9d7e4.jpg)

![A screenshot of a cell phone Description automatically generated](media/84f06a0657467fa18d5077df794f1753.jpg)

#### Employee Certifications, Licenses and Training

>   Use the Certification, License and Training Inquiry window to view
>   Certification, License and/or Training assigned to specific Employee. To
>   open this window, click the **HR and Payroll** series button, click **Human
>   Resources** on the Inquiry content pane and then click **Employee
>   Certifications, Licenses and Training**.

>   Enter or select an **Employee ID**.

>   Select a **Display** option:

-   Certification

-   License

-   Training

>   The scrolling window displays all of the History information related to the
>   Display option selected.

#### Health and Wellness History

>   Use the Health and Wellness History window to see all the activity that has
>   occurred for a specific Employee / Code record. The system tracks all
>   changes to each existing record. To open this window, click the **HR and
>   Payroll** series button, click **Human Resources** on the Inquiry content
>   pane and then click **Health and Wellness History**.

>   Enter an **Employee ID**. Enter or select a **Code**. The **Description**
>   and **Category** displays from the Health and Wellness Code Setup window.

>   The scrolling window allows you to view all History information related to
>   the Employee and the Health and Wellness Code selected.

### Reports

>   The Advanced Human Resources module provides printing capabilities by using
>   the printer icons on the individual windows. For example, pulling up the
>   Category Setup window and selecting the printer icon (without making any
>   Category selections) a report will print giving all of the Category Codes
>   currently set up.

>   The other way to access information stored in Advanced Human Resources is by
>   using SmartList Builder. Using this module, the user can build SmartLists
>   with the data required to meet their reporting needs as it relates to
>   Advanced Human Resources.

#### Excel-based Reports

>   Certification, License and Training Manager allows the user to track
>   certifications, licenses, training and other data for employees using back
>   office functionality. The user can also view and report on this data via
>   reports. It is necessary, however, for managers and other company officials,
>   who may not be users of the Microsoft Dynamics GP system, to have access to
>   this data for decision making purposes. These individuals can use Microsoft
>   Office Excel reporting to meet their unique needs for viewing and sorting
>   certification, license and training data and for customizing the
>   presentation of data to satisfy their requirements.

>   Excel-based reporting is available for the following existing
>   reports/inquiries.

-   Certification List Report

-   License List Report

-   Training List Report

-   Certification History Report

-   License History Report

-   Training History Report

>   The **Required Certification / License / Training report** can be used to
>   measure actual versus requirements for all positions within a
>   department/position.

#### SmartList Builder

>   If the Microsoft Dynamics GP SmartList Builder module is installed, all of
>   the Certification, License and Training Manager and Employee Health and
>   Wellness Manager fields will be available to create SmartList Queries.

>   *NOTE: Refer to the Microsoft Dynamics GP SmartList Builder documentation
>   for instructions on using SmartList Builder.*

### Summary

>   Advanced Human Resources provides inquiry and reporting capabilities by
>   using History windows, the Percent Current Inquiry and the use of printer
>   icons on individual windows. SmartList Builder also enhances the reporting
>   capabilities.

>   Key points to remember from this chapter:

-   Inquiries are available by using history windows and the Percent Current
    Inquiry.

-   Reports are provided by using printer icons.

-   SmartList Builder can provide additional printing capabilities based on the
    user's individual reporting requirements.

## CHAPTER 5: CERTIFICATION, LICENSE AND TRAINING MANAGER FOR EMPLOYEE SELF SERVICE

>   Certification, License and Training Manager extends the reporting options
>   for the Certification, License and Training Manager product into the
>   environment.

>   Certification, License and Training Manager for provides the following
>   features:

-   Extends the enhanced Training Information from the Certification, License
    and Training Manager product

-   Extends the Certification Information from the Certification, License and
    Training Manager product for Employee Self Service.

-   Extends the License Information from the Certification, License and Training
    Manager product for Employee Self Service.

-   Allows Managers to view subordinate employee Training Information,
    Certification Information and License Information

**Certification, License and Training Manager** for Employee Self Service.

### Launching Certification, License and Training Manager 

>   Once the installation and configuration of the Certification, License and
>   Training Manager for application has been completed, the application runs
>   within Microsoft Dynamics GP. The options are available via the same URL as
>   accessing Microsoft Dynamics GP.

>   For using the Certification, License, Training Manager for, refer to the
>   Certification, License, Training Manager for User Guide document for further
>   instruction.

### Employee’s Training, Certification and License Tabs

#### Employee Training Tab

>   An Employee may use the Training tab to view their training information as
>   well as certification and license information. To open this tab, click
>   Employee \> Skills and Training \> Training.

>   The following Status will display if:

-   **Inactive** if the Inactive checkbox is checked on the Course/Class ID
    combination in the Employee Training Entry window within Microsoft Dynamics
    GP.

-   **Expired** if the Inactive checkbox is NOT checked on the Course/Class ID
    combination in the Employee Training Entry window and the current date is
    after the Expiration Date.

-   **Active** if the Inactive checkbox is NOT checked on the Course/Class ID
    combination in the Employee Training Entry window and the current date is on
    or before the Expiration Date.

#### Employee Certification, License Tabs

>   An Employee may use the Certification and License window to view their
>   certification information as well as license and training information

### Summary

>   Certification, License and Training Manager can be configured to work within
>   allowing managers and employees to view employee information. Using the
>   Supervisor information from Dynamics GP, allows managers to view information
>   as it relates to their subordinates certifications, licenses and training.
>   Employees are also able to view their own information. Managers can use
>   Business Entities to develop queries using the data found on the
>   Certifications, Licenses and Training windows. There is also the additional
>   field of “Area” available.

>   Key points to remember from this chapter:

-   Employee Self Service can be configured to allow managers to view their
    employee’s data as it pertains to certifications, licenses and training
    using the Direct Reports View and Site Settings.

-   Employees use the Training tab in to view their personal information for
    certifications, licenses and training.

-   The Manager’s Skills and Training section allows them to view their
    subordinations information for certifications, licenses and training.
