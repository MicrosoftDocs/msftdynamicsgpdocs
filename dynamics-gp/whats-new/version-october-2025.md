---
title: What's new in Dynamics GP in October 2025
description: Learn about enhancements that were added to the product in the October 2025 release of Dynamics GP.
author: theley502
ms.author: theley
ms.reviewer: jswymer
ms.topic: whats-new
ms.date: 09/08/2025
---
# What's New in Dynamics GP in October 2025

This page lists enhancements to Dynamics GP in the October 2025 release. The Dynamics GP October 2025 release enhances different areas of the product.

## Core Features

Functionality has been added across the core modules of Microsoft Dynamics GP.

### [System Enhancements](https://community.dynamics.com/blogs/post/?postid=2c9db82f-e392-ef11-ac21-6045bdd6e4e4)

In the October 2025 release, we have updated some foundational items to reduce vulnerabilities and impact system performance. The system enhancements are not visible to users and they play a critical role in ensuring Dynamics GP will remain secure and compatible with modern technologies. 

These items are tested and compatible with release 18.8 Of Dynamics GP.
- TLS 1.3
- .Net Framework 4.7.2
- Visual Studio 2019

### [Email Setting and Reporting Tools Setup](https://community.dynamics.com/blogs/post/?postid=5db16425-a985-ef11-ac21-6045bdff8c1d)

With Dynamics GP 18.8 we have updated the system so that any sensitive data is automatically encrypted when saved and decrypted when access through the Dynamics interface.  This change will help protect confidential information. This will enhance data security for features like Web Client Graph Email integration and Power BI reports. 

### [Sales Order Processing Required Field Message](https://community.dynamics.com/blogs/post/?postid=5db16425-a985-ef11-ac21-6045bdff8c1d)

In Dynamics GP as you enter transactions you are prompted to enter all the required fields.  The required fields message in Sales Order Processing Transaction Entry includes item fields that aren't always displayed. By default the Sa;es Transaction Entry scrolling window is collapsed.  

The new message will tell the user to expand the scrolling window to verify the item detail fields. "Not all required fields have been entered. Expand the scrolling window to view additional required fields. Required fields appear in bold & italic red type." The required fields display settings are found in the User Preferences --> Display window. 

<img width="974" height="722" alt="image" src="https://github.com/user-attachments/assets/2706b242-cf67-49d8-b43b-db1a63206f04" />

### [Payables Setup vendor Class Roll Dpwn](https://community.dynamics.com/blogs/post/?postid=5db16425-a985-ef11-ac21-6045bdff8c1d)

The Dynamics GP release 18.8 includes a change to the Vendor Class Setup window roll down message.  This is similar to a feature releases in october 2024 which modified the message in Vendor Maintenance. Now the message "Do you want to roll down these changes" will default to the No answer.  

<img width="813" height="716" alt="image" src="https://github.com/user-attachments/assets/26eeee34-dedf-488f-b2b4-a2b8a8d6ca36" />

### [Luxury Auto Depreciation Display and Edit](https://community.dynamics.com/blogs/post/?postid=5db16425-a985-ef11-ac21-6045bdff8c1d)

Dynamics GP Fixed Assets includes the amount for luxury depreciation.  These values are generally updated every year by the government. Previously, in order to maintain the updated values, the user would need to load the Dynamics GP Year End release.  Now, in Dynamics GP 18.8, we have added a window in Tools --> Setup --> Fized Assets --> Luxury Depreciation - Fixed Assets Luxury Depreciation that will display the annual Luxury Depreciation Lmits for automobiles or trucks. 

This window will be populated with the luxury depreciation limits by year giving you the ability to view, manage and edit them as needed. A new table is added which will store the depreciation values by year.

<img width="470" height="419" alt="image" src="https://github.com/user-attachments/assets/b6c18352-dbc4-4977-bc86-a63d52bdc3ee" />

### [Sales Order Batches Navigation List](https://community.dynamics.com/blogs/post/?postid=5db16425-a985-ef11-ac21-6045bdff8c1d)

As requested by you, the users, there is a new navigation list added for Sales Order Batches. This list will display the Sales Order Processing batches that have been created and let you take action with those batches. 

You can modify the list, add columns or filter the list to restrict the information you are viewing. 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3914c281-e632-498f-b96c-ec956dc5fcc2" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a6bbefcd-ca5f-4f2d-a2a2-33116842991f" />

### [VAT Enhancements to Submission process](https://community.dynamics.com/blogs/post/?postid=5db16425-a985-ef11-ac21-6045bdff8c1d)

In the Dynamics GP 18.8 release, there are updates that align with HMRC's latest submission protocols to ensure handling of sensitive financial data.  The new process strengthens protection for stored secrets and credentials to stay compliant  and safeguard your organization's information.

The upgraded process includes improvements in how secrets are stored and transmitted, reducing the risk of data breaches or unauthorized access. 


