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

Dynamics GP Advanced Human Resources includes three components:

- Benefit Lifecycle Manager

  This module integrates with the Microsoft Dynamics GP Payroll module. It is designed to create Human Resources, Payroll Benefit
and Payroll Deduction setup records that are not immediately effective. At the appropriate time, the records can be activated and previous setup
records are tracked in history.
- Certification, License, and Training Manager

  This module integrates with the Microsoft Dynamics GP Human Resources module. Certification, License and Training Manager creates the link between the skills, training and
certifications as well as provides a means to track employee certifications, licensing and training. It also enables the tracking of certifications or license to the extent of reporting on expiration, renewal periods and whether the certifications or licenses are required. You may query on required certifications, licenses, training and dates of expiration. In addition, a query can be created on a specific list of employees with a particular certification, license or training.
- Employee Health and Wellness

  This module integrates with the Microsoft Dynamics GP Human Resources module. The purpose of the Employee Health and Wellness Manager is to provide features for tracking all immunizations, vaccinations and tests required for each employee. The results for each test can also be recorded. Since codes can be defined to meet the company needs,
this solution allows for additions or changes as business or job requirements change. The Employee Health and Wellness Manager will enable the user to schedule follow-up vaccinations, immunizations and tests. Having all the data available will enable easy searches on who is past due or scheduled for a particular immunization, vaccination or test. The requirements per employee are more easily assigned and tracked by the utilization of health and wellness templates.

## Benefit Lifecycle Manager

Benefit Lifecycle Manager is used to create Human Resources Benefit, Payroll
Benefit and Payroll Deduction setup records that are not immediately
effective when creating employee level records or running payroll in
Microsoft Dynamics GP. Benefit Lifecycle Manager then enables the user to
activate the Future Effective setup records at the appropriate time, while
tracking the past setup records in history.

By creating a Future Effective date to the record, this information can also
be extended to the Benefit Self Service product on.

Benefit Lifecycle Manager integrates with the Microsoft Dynamics GP Payroll
module. When creating Human Resources Benefit, Payroll Benefit or Payroll
Deduction records, the user can easily create or modify the Future Effective
record as well.

### Features in Benefit Lifecycle Manager

The features and capabilities of Benefit Lifecycle Manager include:

- Create Human Resources Setup Future Effective records for:

  - Miscellaneous Benefit o Health Insurance o Life Insurance o Retirement
        Plans

- Create corresponding Payroll Setup Future Effective records for:

  - Benefit o Deduction

- Activate Future Effective Setup records

- Track History of previous Setup records

- Make Pending Changes available to Benefit Self Service for informational and
    enrollment purposes.

> [!NOTE]
> This product is required for use with Benefit Self Service to activate any Pending Changes options in.

### Release Requirements for Benefit Lifecycle Manager

Certain features and the use of this product must meet the following setup requirements to ensure proper functionality. Failure to use the Benefit Lifecycle Manager product as specified here will not currently be supported.

- Changes must be made from the Human Resources menu and rolled down to
    Payroll. There is **NO** reconciling functionality for future effective
    records.

- If creating a Future Effective Benefit, Payroll Deduction or Payroll Benefit
    record, the core record for that Benefit Code must exist before attempting
    to create the Future Effective record.

- Each individual must have the Payroll View for Human Resources option
    selected. To enable this option open the User Setup window, click the
    **Administration** series button, click **System** on the Setup content pane
    and then click **User**. Enter or select the **User ID**. Select the
    **Payroll View for Human Resources** checkbox. Click **Save**.

- Grant Security Access using the Security Setup window to grant individual
    security settings for each company.

### Multi-User Access

Additional checks have been added to restrict access to Benefit Codes and
Future Effective Benefit Codes when Benefit Lifecycle Manager is being used
to ensure that benefit codes are modified correctly. The restrictions added
include the following scenarios and if one of these scenarios is
encountered, the system prompts with "This code is open by another user.
Please try again later."

Access denied scenarios:

- If the benefit code is opened in the Future Effective mode in the Human Resources Benefit Setup, Payroll Benefit Setup or Payroll Deduction Setup window, no other employee is able to open that benefit code in any of the three areas at the core setup level.

- If more than one employee currently has the benefit code open in the Human Resources Benefit Setup, Payroll Benefit Setup or Payroll Deduction Setup
    window and there is an attempt to create a new or display the existing Future Effective record in any of the three areas for that benefit code.

When the Human Resources to Payroll Integration is happening for a Future Effective record, if another employee would open that benefit code in one of the subsequent windows before the Human Resources to Payroll Integration gets to that level, when the Human Resources to Payroll Integration hits that level, the integration is stopped.

## Certification, License, and Training Manager

The Certification, License, and Training Manager tracks all Certifications, Licensing and Training requirements. This product completes certain areas
and fills additional areas that core Microsoft Dynamics GP skills and certification tracking does not currently handle.

Certification, License and Training Manager integrates with Microsoft Dynamics GP Human Resources. The Certification, License and Training Manager
will create the link between the skills, training and certifications as well as provide a means to track employee certifications, licensing and training.
It will also enable the tracking of certifications or licenses to the extent of reporting on expiration, renewal periods and whether the certifications
or licenses are required. You may query on required certifications, licenses, training and dates of expiration. In addition, you may query on a
specific list of employees with a particular certification, license or training.

### Features in Certification, License, and Training Manager

The features and capabilities of Certification, License and Training Manager include:

- Enter unlimited Certifications

- Certifications tracking for employees

- Enter unlimited Licenses

- License tracking for employees

- Enter unlimited Training

- Training tracking for employees

- Inquire for an employee on Certifications, Licenses and Training

- Set and View Requirements per Department and Position combinations for
    Certification, License and Training

- View Employee Percent Current per Department and Position combinations based
    on Worked or Home department/positions for Certification, License and
    Training

- SmartList Builder reporting options

### Release Requirements for Certification, License, and Training Manager

Certain features and the use of this product must meet the following setup requirements to ensure proper functionality. Failure to use the Certification, License, and Training Manager product as specified here will not currently be supported.

To Grant Security Access use the Security Setup window to grant individual security settings for each company.

### Certification Feature

The Certification feature of the Certification, License, and Training Manager
allows the user to enter Certification information specific to the company
needs as well as track employee level Certification information as required
within the industry or business. The Certification feature is easy to use
and provides inquiry options to view the information employees are tracking
more easily.

When a record for a Certification is entered where an expiration date is an
attribute of that Certification whether the date is known at the time of
entry or later, the expiration date will always be a future date to expire
in relationship to the current record, i.e. my current Certification will
expire at a future date. When the Certification is renewed or completed, the
user can pull up the record for the Certification and enter the current
renewal/completed date, the future expiration date and select Save. When it
is the first year of a Certification, then the Original Issue Date = Date
Renewed/Completed.

### License Feature

The License feature of the Certification, License and Training Manager
allows the user to enter License information specific to the company needs
as well as track employee level License information as required within the
industry or business. The License feature is easy to use and provides
inquiry options to view the information an employee is tracking.

When a record for a License is entered where an expiration date is an
attribute of that License whether the date is known at the time of entry or
later, the expiration date will always be a future date to expire in
relationship to the current record. When the License is renewed or
completed, you should pull up the record for the License and enter the
current renewal/completed date and the future expiration date and select
Save. When it is the first year of a License, then the Original Issue Date =
Date Renewed/Completed.

### Training Feature

The Training feature of the Certification, License and Training Manager
allows the user to enter Training information such as Courses and Classes
specific to the company needs as well as track employee level

Training information as required within the industry or business. The
Training feature is easy to use and provides inquiry options to view the
information the employee is tracking more easily.

When a record for the Training is entered where an expiration date is an
attribute of that Training, the expiration date will always be a future in
relationship to the current record. When the Training is renewed /
completed, you will pull up the record for the Training and enter the
current renewal / completed date and the future expiration date and select
Save. When it is the first year of a Training, then the Original Issue Date
= Date Renewed/Completed.

## Employee Health and Wellness

Within Microsoft Dynamics GP Human Resources, you can track injury and
illness information for each employee and generate the necessary OSHA
reports. Employee Health and Wellness Manager enables organizations to
completely track all additional employee immunizations, vaccinations and
test requirements that are related to the injury and illness cases, but not
included on OSHA reports.

Employee Health and Wellness Manager is an enhancement that integrates with
Microsoft Dynamics GP Human Resources. The purpose of Employee Health and
Wellness Manager is to provide features for tracking all immunizations,
vaccinations and tests required for each employee. The results for each test
can also be recorded. Since the codes can be defined, the product allows for
additions or changes as business or job requirements change.

Employee Health and Wellness Manager enables the user to schedule follow-up
vaccinations, immunizations and tests. Having all the data available will
enable easy searches on who is past due or scheduled for a particular period
for a particular immunization, vaccination or test. The requirements per
employee are more easily assigned and tracked by the utilization of health
and wellness templates.

### Features in Employee Health and Wellness Manager

The features and capabilities of Employee Health and Wellness Manager include:

- Create Categories and associated Codes specific to the business needs

- Create unlimited Results types that can be associated with the Health and
    Wellness codes

- Create Health and Wellness codes for use in Health and Wellness and related
    to Injury and Illness tracking

- Assignment of multiple codes to employees via customized Templates

- Assignment of Health and Wellness codes to employees for informational and
    tracking purposes

- Additional information for tracking with Illness and Injury Cases, including
    Source tracking

- SmartList Builder reporting options

Sensitive information related to the Health and Wellness of Employees and
Sources is tracked using this product. Compliance with HIPPA regulations as
it pertains to this data is the responsibility of the user.

## Summary

The Advanced Human Resources module for Microsoft Dynamics GP is comprised
of three components:

1. Benefit Life Cycle Manager

2. Certification, License and Training Manager and

3. Employee Health and Wellness

Key points to remember from this chapter:

- Benefit Life Cycle Manager provides the ability to assign future effective dates for Miscellaneous Benefits, Health Insurance, Life Insurance and Retirement Plans

- The user can enter an unlimited number of certifications, licenses and training data for employees.

- Employee Health and Wellness allows the organization to track various health-related categories, codes and tests, as well as the results of each.

## See also

[Advanced Human Resources - Employee Maintenance](advanced-hr-employee-maintenance.md)  
[Advanced Human Resources - Inquiries and Reports](advanced-hr-inquiries-reports.md)  
[Advanced Human Resources - Training and Certification for Employee Self Service](advanced-hr-inquiries-training-certification.md)  
[Advanced Human Resources - Setup](advanced-hr-setup.md)  
[Human Resources - Overview](HumanResource.md)  
[Human Resources - Company Setup and Organizational Structure](human-resources-company-setup.md)  
[Human Resources - Position Control Setup](human-resources-position-control.md)  
[Human Resources Social Security Number Mask](../whats-new/human-resource-social-security-number-mask.md)  
