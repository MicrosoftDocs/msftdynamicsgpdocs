---
title: "Manufacturing Setup Part 2"
description: "Examine how to get users set up for the Manufacturing module in Dynamics GP."
keywords: "manufaturing"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 06/19/2020
---

# Manufacturing Setup - Part 2: User setup

 This part of the documentation includes information that will help you set up Manufacturing user preferences. Most of this information will need to be set up only once for each user, but you can refer to this information at other times for instructions on modifying or viewing existing entries.
 The following information is discussed:

- *Chapter 7, “Manufacturing basic user setup,”* describes options for setting
    up user preferences. Information about specifying default selections for
    report formats is included.

- *Chapter 8, “Manufacturing core functions user setup,”* includes information
    about specifying user preferences for Bills of Materials.

- *Chapter 9, “Manufacturing production functions user setup,”* contains
    information about specifying routing options and manufacturing order
    scheduling options.

- *Chapter 10, “Manufacturing management functions user setup,”* includes
    information about user preference settings for Engineering Change Management
    and Quality Assurance.

- *Chapter 11, “Manufacturing planning functions user setup,”* includes
    information about options for Capacity Requirements Planning and Material
    Requirements Planning.

To get started with setting up the Manufacturing module, see [Manufacturing Setup - Part 1: Manufacturing setup](manufacturing-setup-part-1.md).  

## Chapter 7: Manufacturing basic user setup

 You can set up preferences to customize some aspects of your Manufacturing system—for instance, what information is displayed in a window or how fields are cleared.
 User preferences are set on a user-by-user basis. Because of this, users must log into the system with their own user IDs to be able to see their user preferences in effect. User preferences affect only the computer where the login was used.

 Before you set up user preferences, you must set up system default settings for Manufacturing. Refer to the sections for more information:

- [Chapter 1: Manufacturing basic setup](manufacturing-setup-part-1.md#chapter-1-manufacturing-basic-setup)  

- [Chapter 3: Manufacturing core functions setup](manufacturing-setup-part-1.md#chapter-3-manufacturing-core-functions-setup)  

- [Chapter 4: Manufacturing production functions setup](manufacturing-setup-part-1.md#chapter-4-manufacturing-production-functions-setup)  

- [Chapter 5: Manufacturing management functions setup](manufacturing-setup-part-1.md#chapter-5-manufacturing-management-functions-setup)  

- [Chapter 6: Manufacturing planning functions setup](manufacturing-setup-part-1.md#chapter-6-manufacturing-planning-functions-setup)  

This information is divided into the following sections:

- *System administrators and user preferences*

- *General user preferences for Manufacturing*

- *Setting up manufacturing-specific preferences*

- *Setting up INI user settings*

### System administrators and user preferences

Access privileges for setting user preferences can vary from user to user. Some users—such as system administrators—might be granted special “system user” privileges so they can set up user preferences both for themselves and for others. Most users, though, will have access privileges to set up only their own user preferences.

> [!NOTE]
> If you don’t have access to the user preference windows but want to make changes, contact your system administrator.

### General user preferences for Manufacturing

Manufacturing includes several “general” user preference settings that you can use to access other applications—such as web browsers or graphics applications—and to customize characteristics such as fonts and colors in Manufacturing windows. General user preferences can be grouped into three categories:  

- Manufacturing-specific user preference settings

    These affect options available only for Manufacturing users. Refer to *Setting up manufacturing-specific preferences* for more details.
- INI user settings

    These allow you to choose the location of other applications that link to Manufacturing data, or that might help you view graphics or multimedia files you’ve attached to your item records. Refer to *Setting up INI user settings* for more details.

- Microsoft Dynamics GP user preference settings

    These determine the display characteristics of windows: font styles such as italic or bold, font colors, and so on. Refer to your System User’s Guide (Help \>\> Contents \>\> select Using the System) for more details.

### Setting up manufacturing-specific preferences

 User preferences are a series of default system settings that are attached to each user ID. After you set up your user preferences, they’ll be active each time you log on.
 **To set up manufacturing-specific preferences:**

1. Open the User Preferences window. (Microsoft Dynamics GP menu \>\> Tools
    \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> User)

2. If you have system user access privileges, enter or select a user ID in the
    Choose User field. If you’re not a system administrator, your user ID
    appears.

3. In the Systems Options, mark a report option.

    - “Text reports” is the default Microsoft Dynamics GP format for printing reports.
    - Graphic reports have additional graphic features such as shading and borders.

4. Save the settings.

If you’re a system administrator and are setting up preferences for other users, choose OK. The information will be saved and the window will stay open so you can choose another user ID and continue to set up user preferences for other users. Close the window when you’ve finished setting up user preferences.

If you aren’t a system administrator, choose OK to save the settings and close the window.

### Setting up INI user settings

You must set up Manufacturing INI settings if you plan to use any of the following features:

- Attaching graphics files to routings or items

- Attaching multimedia files to routings or items

- Attaching CAD files to routings or items

INI settings are specific to a computer, not to a user. You might want to use different software to view files on different machines. Drafting department employees, for example, might have the full version of the software used to create and modify CAD drawings, while others in the company have versions of the software to only view the drawings.

#### To set up INI user settings

1. Open the MFG & HRP Settings window. (Microsoft Dynamics GP menu \>\> Tools
    \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> User \>\> INI
    Settings)

    ![A screenshot](media/a23d2f092bf1cbd15aaa0433c67349fd.jpg)

    > [!NOTE]
    > You need to specify pathnames only for the features you’ll use in Manufacturing. If your company isn’t attaching graphics files to routings or items, for example, don’t set up the graphics path.

2. Enter a path to a CAD application or choose the browse button on the Path to CAD App field to find the application you’ll use to view CAD files. This application will be used to view all electronic drawings on your computer that have a CAD type.

3. Enter a path to a graphics application or choose the browse button on the Path to Graphics App field to find the application you’ll use to view graphics.

4. Enter a path to a multimedia application or choose the browse button on the Path to Multimedia App field to find the application you’ll use to view multimedia files.

5. Enter a path to a graphing application or choose the browse button on the Path to Graphing App field to find the application you’ll use to graph Manufacturing data.

6. Close the window when you’ve finished specifying the path names to save the information.

## Chapter 8: Manufacturing core functions user setup

Most Manufacturing modules include user preference settings. You can use these settings to customize some aspects of the system—such as what information is displayed in a window or how fields are cleared—on a user-by-user basis.

Before you set up user preferences, you must set up system default settings for Manufacturing. Refer to these documents for more information:

- *Chapter 1, “Manufacturing basic setup”*

- *Chapter 3, “Manufacturing core functions setup”*

- *Chapter 4, “Manufacturing production functions setup”*

- *Chapter 5, “Manufacturing management functions setup”*

- *Chapter 6, “Manufacturing planning functions setup”*

This information is divided into the following sections:

- *User preference settings*

- *Setting up bills of materials user preferences*

### User preference settings

Because user preferences are linked to the user ID you use to log into the system, user preferences are in effect only when that user is logged into the system, and affect only the computer where the login was used.

Most users can change only their own user preferences. System administrators, however, can set user preferences for other users.

### Setting up bills of materials user preferences

You can use the BOM Preferences window to select an icon that will be displayed in the tree view of the Bill of Materials Entry window and the Bill of Materials View window. Icons are available to show different information about the components in each bill of materials, such as whether the item is tracked by lot or serial numbers, whether it is a made or purchased item, and so on.

You also can use the window to view the system-wide values that have been set up for your company. You can view the date value that is used to calculate component lead time information, and you can view the labels that have been set up for user-defined fields, if any.

#### To set up bills of materials user preferences

1. Open the **BOM Preferences** window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> Bill of Materials)

2. If you have system administrator privileges, enter or select a user ID. If you don’t have system administrator privileges, your own user ID will be displayed in the **Choose User** field, and you can set up preferences for only your own login.

3. Mark the icon to be used in the tree view of the **Bill of Materials Entry** window and the **Bill of Materials View** window.

4. Save the settings.

If you are a system administrator and are going to set up Bill of Materials preferences for other users, choose Save. The information will be saved and the window will stay open so you can set Bill of Materials user preferences for other users. Close the window when you’ve finished setting user preferences for additional users.

If you aren’t a system administrator, choose OK to save your settings and close the window.

## Chapter 9: Manufacturing production functions user setup

Most Manufacturing modules include user preference settings. For production functions modules, you can specify options for entering routing sequence and data collection information.

Because user preferences are linked to the user ID needed to log into the system, the preferences are in effect only when that user is logged into the system. User preferences affect only the computer where the login was used.

Before you set up user preferences, you must set up system default settings for Manufacturing. Refer to these documents for more information:

- *Chapter 1, “Manufacturing basic setup”*

- *Chapter 3, “Manufacturing core functions setup”*

- *Chapter 4, “Manufacturing production functions setup”*

- *Chapter 5, “Manufacturing management functions setup”*

- *Chapter 6, “Manufacturing planning functions setup”*

This information is divided into the following sections:

- *Setting up routing user preferences*

- *Setting up sequence entry user options*

- *Setting up spacing and pointer routing options*

- *Setting up WIP user preferences*

### Setting up routing user preferences

Use the Routing User Preferences window to customize each user’s view of routing information. You can set up options affecting how updates to routings are reflected in related routings. You also can choose sequence entry options for work center opcodes and can set search options and sequence spacing.

Sequence entry options control the information that is retrieved when a user accesses data during routing entry.

#### To set up routing user preferences

1. Open the Routing User Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> Routings)

    ![A screenshot ](media/a2ab0984c7944fade6bb1f40b1e9bb9b.jpg)

2. If you have system administrator privileges, enter or select a user ID. If you don’t have system administrator privileges, your own user ID will be displayed in the Choose User field, and you can set up preferences for only your own login.

3. Determine how to update planning routings.  

    - Compare as Number

        If all planning routing sequence numbers are numeric, mark **Compare as Number**.
    - Confirm Save

        To have the message “Are you sure you want to do this?” displayed before planning routings are changed, mark **Confirm Save**.

4. Determine if other planning routings should be updated based only on the routing name and sequence number.

    Whether a routing update is applied to other routings is always determined by the routing name and sequence number. The routing name and sequence number must match before a change in one routing sequence is reflected in a sequence in another routing.

        - If you mark Match WC ID, the routing sequence change will be applied to only the routing sequences that have the same routing name, sequence number, and work center ID.

        - If you don’t mark Match WC ID, all routings that have the same routing name and sequence number will be updated, regardless of the work center ID.

5. Determine if active routings should be updated based only on the routing name and sequence number.

    Whether a routing update is applied to other routings is always determined by the routing name and sequence number. The routing name and sequence number must match before a change in one routing sequence is reflected in a sequence in another routing.

        - If you mark Match WC ID, the routing sequence change will be applied to only  the routing sequences that have the same routing name, sequence number and work center ID.

        - If you don’t mark Match WC ID, all routings that have the same routing name and sequence number will be updated, regardless of the work center ID.

6. Determine how to search your routing records. You can mark either or both Search Includes options.

    - If you mark Item Number, searches of routing records will display only those routings that include the item number you specify.

    - If you mark Routing Name, searches of routing records will display only the routing that has the name you specify.

7. Choose OK.

### Setting up sequence entry user options

To print routing information for use on the production floor, you can set up options to ensure that the information your employees need is included in the reports. Use the Routing User Preferences window to set up routing entry user preferences.

#### To set up sequence entry user options

1. Open the Routing User Preferences window.  (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> Routings)

2. If you have system administrator privileges, enter or select a user ID. If you don’t have system administrator privileges, your own user ID will be displayed in the **Choose User** field, and you can set up preferences for only your own login.

3. Mark **Replace Routing Seq. Descr.** with **Op Code Description** to view operation code descriptions rather than routing sequence descriptions.

4. Mark **Append Op Code Description** to **Routing Notes** to add the operation code description to the routing notes.

5. Mark **Attach Op Code Notes** to **Routing Notes** to add the operation code notes to the routing notes.

6. Save the settings.

If you have system user access privileges and are going to set up routing preferences for other users, choose Save. The information will be saved and the window will stay open so you can set up routing user preferences for other users. Close the window when you’ve finished setting user preferences.

If you don’t have system user access privileges, choose OK to save your settings and close the window.

### Setting up spacing and pointer routing options

Use the Routing User Preferences window to set up options for sequence number spacing and to determine if pointer routings can be used in your facility.

You can use any numbering spacing, but we recommend using spacing intervals of 10 or 100. This makes it easier to insert a new sequence between existing sequences.

#### To set up spacing and pointer routing options

1. Open the Routing User Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> Routings)

2. Enter a default spacing for routing sequence numbers.

3. Mark Use Pointer Routings to use pointer routings in your system. You can’t mark the Use Pointer Routings option unless the system-wide setting to use pointer routings also is marked.

    > [!NOTE]
    > Refer to Creating a pointer routing in Chapter 5, “Pointer routings,” in the Manufacturing Production Functions documentation for more information about pointer routings.*

4. Choose OK.

### Setting up WIP user preferences

Use the WIP Preferences window to select options to make data entry tasks easier. The options you select will affect how the Data Collection Transactions window works.

#### To set up WIP user preferences

1. Open the WIP Preferences window.(Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> WIP)

2. If you have system user access privileges, enter or select a user ID in the Choose User field. If you aren’t a system administrator, your user ID will appear.

3. Mark options to indicate what should happen when a data collection entry record is saved.

    - Clear MO Number
        Clears the MO Number field in the Data Collection window each time you save a data collection record.
    - Clear Sequence
        Clears the Sequence field in the window each time you save a data collection record.
    - Clear Dates
        Clears the Date fields in the window each time you save a data collection record.
    - Clear Times
        Clears the Time fields in the window each time you save a data collection record.

4. To have the system automatically enter the next sequence in the selected routing in the Sequence field, mark the Increment Sequence option.

5. To have the system always calculate labor costs using the standard labor rate, mark Always Use Standard Labor Rate.

6. Choose OK.

## Chapter 10: Manufacturing management functions user setup

Most Manufacturing modules include user preference settings. This document includes information about user preferences for the management functions modules—Quality Assurance, Engineering Change Management and Job Costing. For example, you can specify what kinds of quality assurance records are displayed when you open a Quality Assurance window. You also can specify what constitutes an “old” engineering change order request, and whether you want change requests to be marked as reviewed as soon as you’ve opened them.

Because user preferences are linked to the user ID needed to log into the system, the preferences are in effect only when that user is logged into the system. User preferences affect only the computer where the login was used.

Before you set up user preferences, you must set up system default settings for Manufacturing. Refer to these documents for more information:

- *Chapter 1, “Manufacturing basic setup”*

- *Chapter 3, “Manufacturing core functions setup”*

- *Chapter 4, “Manufacturing production functions setup”*

- *Chapter 5, “Manufacturing management functions setup”*

- *Chapter 6, “Manufacturing planning functions setup”*

This information is divided into the following sections:

- *Setting up engineering change user preferences*

- *Setting up quality assurance user preferences*

### Setting up engineering change user preferences

You can set up two user preferences in Engineering Change Management. Use the ECM User Preferences window to define an “old” change order—one that is taking longer to go through its approval status than a number of days you specify—and also to indicate whether auto-marking features should be used.

These options also are included in the ECM System Preferences window. If the system defaults you set up there are applicable for all users, you can skip this setup step. You need to use the ECM User Preferences window only if users at your company need different definitions for “old” change orders, or if some users will use auto-marking features and others won’t.

#### To set up engineering change user preferences

1. Open the **ECM User Preferences** window.(Microsoft Dynamics GP menu \>\> Tools\>\> Setup \>\> Manufacturing \>\> User Preferences \>\> ECM)

2. If you have system user access privileges, enter or select a user ID. If you don’t have system administrator privileges, your own user ID will be displayed in the User ID field, and you can set up preferences for only your own login.

3. Enter the number of days until changes will be considered old. This value will be used to identify aged change orders in the **Engineering Change Statistics** window.

4. Mark the Auto-mark Routing option if change orders should be marked automatically when you review them.

5. Save the settings.

If you are a system administrator and are going to set up ECM preferences for other users, choose Save. The information will be saved and the window will stay open so you can set up ECM user preferences for other users. Close the window when you’ve finished setting up user preferences.

If you aren’t a system administrator, choose OK to save your settings and close the window.

### Setting up quality assurance user preferences

You can use the **QA User Preferences** window to select a default sorting option and to choose which quality assurance records will be displayed when you open the **QA Incoming** window.

These are only default settings. You can select different sorting methods or choose to see different records when you’re using the **QA Incoming** window.

> [!IMPORTANT]
> You must set up quality assurance system settings before you can set up quality assurance user preferences. Refer to Setting up Quality Assurance.

You also can choose to have the Acceptable Quality Level (AQL) table automatically cleared after you save an AQL table record.

#### To set up quality assurance user preferences

1. Open the **QA User Preferences** window. (Microsoft Dynamics GP menu \>\> Tools\>\> Setup \>\> Manufacturing \>\> User Preferences \>\> QA)

2. Select the default sorting method for records in the **QA Incoming** window. Choices are **PO Number** and **Receipt Number**.

3. Select the default restriction for records in the QA Incoming window.

    - **All Items** View records for all items that have been received.
    - **QA Required – Show All Receipts** View records for all items requiring incoming inspection that have been received.
    - **QA Required – Restrict by Date** View records for all items requiring incoming inspection that were received on a purchase receipt with a date that is within a range you specify.
    - **QA Completed** View records for all items that have been inspected.

    > [!NOTE]
    > This default restriction will be used each time you open the **QA Incoming** window. You can switch to other views of the quality assurance records when you’re using the **QA Incoming** window.

4. To automatically clear the AQL (Acceptable Quality Level) table after its associated incoming inspection record has been saved, mark Clear AQL table after saving.

5. Save the settings.

If you are a system administrator and are going to set up Quality Assurance preferences for other users, choose Save. The information will be saved and the window will stay open so you can set Quality Assurance user preferences for other users. Close the window when you’ve finished setting up user preferences.

If you aren’t a system administrator, choose OK to save your settings and close the window.

## Chapter 11: Manufacturing planning functions user setup

Most Manufacturing modules include user preference settings. This document includes information about user preferences for the planning functions modules— Sales Forecasting, Master Production Scheduling, Capacity Requirements Planning, and Material Requirements Planning. You can use these settings to customize some aspects of the system—for instance, what information is displayed in a window or how fields are cleared—on a user-by-user basis.

Because user preferences are linked to the user ID needed to log into the system, the preferences are in effect only when that user is logged into the system. User preferences affect only the computer where the login was used.

Before you set up user preferences, you must set up system default settings for Manufacturing. Refer to these documents for more information:

- *Chapter 1, “Manufacturing basic setup”*

- *Chapter 3, “Manufacturing core functions setup”*

- *Chapter 4, “Manufacturing production functions setup”*

- *Chapter 5, “Manufacturing management functions setup”*

- *Chapter 6, “Manufacturing planning functions setup”*

This information is divided into the following sections:

- *Setting up CRP user preferences*

- *Setting up MRP user preferences*

- *Restoring MRP default settings*

- *Setting up request resolution user preferences*

### Setting up CRP user preferences

Capacity Requirements Planning (CRP) user preferences determine how the system displays CRP information accessed with the employee’s user ID. The options you choose will determine what information appears in the windows and in reports generated using CRP.

#### To set up CRP user preferences

1. Open the CRP Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>Setup \>\> Manufacturing \>\> User Preferences \>\> CRP)

    ![A screenshot of a cell phone Description automatically generated](media/53fda1cff045b06b9fa37fef151f3aef.jpg)

2. If you have system administrator privileges, select the user ID you want to set up preferences for. If you don’t have system administrator privileges, your own user ID will be displayed in the Choose User field, and you can set up preferences for only your own login.

3. Select a default work center.

    This selection will determine which work center’s information is displayed first when you open CRP windows. You can still see information for other work centers—this will just be the first displayed.

4. Select a default bucket size. The bucket size determines how the information will be summarized in the CRP/MO Detail window. If you set this user preference to 2 Weeks, for example, then information in the CRP/MO Detail window will reflect the totals of capacity for two weeks at a time. To see the information in other bucket sizes, you can adjust the bucket sizes in the CRP/ MO Detail window.

5. Select a default sorting method to determine how information is sorted when you use CRP windows. Sorting options include the following:

    - By Work Center
        View CRP information sorted by the work center IDs.

    - By Released Employee Load Percent
        View CRP work center information sorted by the percentage of employee load each work center carries for firm manufacturing orders.
    - By Released Machine Load Percent
        View CRP work center information sorted by the percentage of machine load each work center carries for manufacturing orders with Released status.
    - By + Open Employee Load Percent
        View CRP work center information sorted by the percentage of employee load each work center carries for manufacturing orders with Released or Open status.
    - By + Open Machine Load Percent
        Select this option to see CRP work center information sorted by the percentage of machine load each work center carries for manufacturing orders with Released or Open status.

    > [!NOTE]
    > The option you choose here is only a default setting. You can use sorting options in CRP module windows to see information in other orders.
6. Select the number of decimal places to be displayed for numeric fields in CRP.

7. Mark Show Outsourced Work Centers to include CRP information for work centers that are not part of your plant.

    For example, you might have a contract with another firm to paint the farm machinery produced by your company. Your contract with the painting contractor might specify how much capacity the contractor reserves for you. To track use of that capacity, you can mark this option.

8. Mark Expanded Windows if scrolling windows in the CRP module should open in an expanded view.

    > [!NOTE]
    > This is just a default setting. You can change the view in the scrolling windows when you’re using other CRP windows.

9. Save the settings.

If you are a system administrator and are going to set up CRP preferences for other users, choose Save. The information will be saved and the window will stay open so you can set up CRP user preferences for other users. Close the window when you’ve finished setting up user preferences.

If you aren’t a system administrator, choose OK to save your settings and close the window.

### Setting up MRP user preferences

Use the MRP Preferences window to set up general Material Requirements Planning (MRP) options and to select fields for windows and reports in MRP system. All the user preferences you set up in this window are on a user-by-user basis and the settings will override system-wide default preferences.

Refer to *Setting up general MRP options* for more details about these MRP system default settings.

#### To set up MRP user preferences

1. Open the MRP Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>Setup \>\> Manufacturing \>\> User Preferences \>\> MRP)

2. If you have system administrator privileges, enter or select a user ID. If you don’t have system administrator privileges, your own user ID will be displayed in the Choose User field, and you can set up preferences for only your own login.

3. Set up general MRP options.

    - To view items, sites, and item-site combinations that have been excluded from MRP calculations or that have no activity, mark Show Items with no Activity. This option will be available only if the option to show inactive items is marked in the MRP Preference Defaults window.

    - To see a status window when MRP information is being regenerated, mark the Show Status Window option.

    - Select the default bucket size for your views in MRP windows. Choices are Days, Weeks and Months.

4. Select up to six MRP quantities to see when using MRP windows.

    These fields will be displayed in windows and reports in the order in which they are displayed in this window. If the first field displayed should be Required Planned, select Required Planned for the first (top) list.

    Refer to *MRP quantities* in *Chapter 8, “MRP overview,”* in the Manufacturing Planning Functions documentation for more information about how the quantities are calculated.

    > [!NOTE]
    > If new labels have been applied to the MRP quantities at your company, the new labels will be displayed in the lists. To see a cross-reference between the Manufacturing labels and those created by your company, choose MRP Label Cross-Reference. Any references to those quantities in documentation will be by the original Manufacturing labels.

5. Choose OK and close the window.

### Restoring MRP default settings

You can use the MRP Preferences window to remove the user-defined MRP preference settings you’ve selected. Completing this procedure will make the user preferences for the selected user ID identical to the system-wide default settings.

#### To restore MRP default settings

1. Open the MRP Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>Setup \>\> Manufacturing \>\> User Preferences \>\> MRP)

2. If you have system administrator privileges, enter or select a user ID. If you don’t have system administrator privileges, your own user ID will be displayed in the Choose User field, and you can set up preferences for only your own login.

3. Choose **Reset to System Defaults**.

4. Choose OK and close the window.

### Setting up request resolution user preferences

If you’re using MRP, each user with purchase order entry responsibilities will need to set up user preferences for using primary suppliers.

#### To set up request resolution user preferences

1. Open the **Purchase Request Resolution User Preferences** window.

    (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> Request Resolution)

    > [!NOTE]
    > You also can open this window through the Purchase Request Resolution window. Choose the Go To button and select Req. Resolution Preferences.

2. To automatically select the primary supplier of an item for auto-generated purchase orders, mark **Automatically use primary vendor on item selection**.

3. Choose OK and close the window.

## See also

[Manufacturing Setup - Part 1: Manufacturing setup](manufacturing-setup-part-1.md)  
[Glossary of Terms in Manufacturing](glossary-manufacturing.md)  
