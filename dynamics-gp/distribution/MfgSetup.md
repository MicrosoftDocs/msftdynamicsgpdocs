---
title: "Manufacturing Setup"
description: "Examine how to get the Manufacturing module set up in Dynamics GP."
keywords: "manufaturing"
author: theley502
manager: edupont
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: edupont
ms.author: theley
ms.date: 06/17/2020
---

# Manufacturing Setup

You can use Manufacturing to organize and track the daily workings of the manufacturing process, such as taking orders, purchasing raw materials, building finished goods, fulfilling orders, and selling the finished goods.

Manufacturing documentation is divided into five manuals. Refer to the following table for an overview of what is included in each of the manuals.

| **Manual**                                | **Modules or other major pieces**      |
|-------------------------------------------|----------------------------------------|
| Manufacturing Setup manual                | System setup </br>User setup         |
| Manufacturing Core Functions manual       | Manufacturing Cards Extensions to Inventory Control  </br>Bills of Materials Extensions to Sales Order Processing  </br>Sales Configurator </br> Manufacturing Reports |
| Manufacturing Production Functions manual | Routings Manufacturing Orders  </br>Outsourcing Work in Process    |
| Manufacturing Management Functions manual | Quality Assurance Engineering </br> Change Management  </br>Job Costing     |
| Manufacturing Planning Functions manual   | Sales Forecasting Master Production Scheduling Capacity Requirements Planning (CRP) Material Requirements Planning (MRP)                             |

*If a Microsoft Dynamics® GP window—such as the Sales Transaction Entry window—is the active window when you access help, online help for Microsoft Dynamics GP will be displayed. You can close that help, open any Manufacturing window, and try again to access Manufacturing-specific help.*

This manual is designed to give you an understanding of how to use the features of Manufacturing, and how it integrates with the Microsoft Dynamics GP system.

To make best use of Manufacturing, you should be familiar with systemwide features described in the System User’s Guide, the System Setup Guide, and the System Administrator’s Guide.

Some features described in the documentation are optional and can be purchased through your Microsoft Dynamics GP partner.

To view information about the release of Microsoft Dynamics GP that you’re using and which modules or features you are registered to use, choose Help \>\> About Microsoft Dynamics GP.

The manual is divided into the following parts:

-   *Part 1, Manufacturing setup*, describes how you can set up security and systemwide settings for Manufacturing modules.

-   *Part 2, Manufacturing user setup*, contains information about user preferences—settings that help you customize each user’s view of Manufacturing information.

## Part 1: Manufacturing setup

This part of the documentation includes information that will help you complete Manufacturing setup tasks. You can refer to this information to learn how to use security in Manufacturing and how to set up systemwide settings.

Many of the tasks that are described must be completed before you can enter information in Manufacturing. Be sure to review and complete all setup tasks for Manufacturing modules you’ve installed. Later you can refer to this information to adjust settings or to help new users get started.

The following information is discussed:

-   *Chapter 1, “Manufacturing basic setup,”* includes information about setting up users, the shop floor calendar, and work center options.

-   *Chapter 2, “Security,”* describes security information specific to Manufacturing, such as process security and module security.

-   *Chapter 3, “Manufacturing core functions setup,”* contains information about system settings for bills of materials, sales extensions, and the Sales Configurator.

-   *Chapter 4, “Manufacturing production functions setup,”* describes system settings for routings, manufacturing orders, and work-in-process.

-   *Chapter 5, “Manufacturing management functions setup,”* includes information about setting up quality assurance, engineering change management, and job costing.

-   *Chapter 6, “Manufacturing planning functions setup,”* includes information about system settings for Material Requirements Planning.

### Chapter 1: Manufacturing basic setup

Before you set up module-specific system settings and user preferences, use this information to complete basic system setup tasks.

This information is divided into the following sections:
-   *Setup checklist*

-   *Setting up costing system default settings*

-   *Shrinkage overview*

-   *Including shrinkage in Manufacturing*

-   *Shop calendars*

-   *Defining the shop calendar*

-   *Setting up work center options*

-   *Designating system users*

#### Setting up costing system default settings

Default costing settings determine how costs are tracked throughout your manufacturing facility. You can choose to automatically account for shrinkage on parent parts, their components, or both. You also can assign a posting account for rounding differences and choose a security set for revaluations.

**To set up costing system default settings:**

1.  Open the Costing Preference Defaults window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Costing)

![](media/MFGCD.jpg)

1.  Mark the options to apply shrinkage, as needed, for standard cost rollups.
    *It’s strongly recommended that you mark both options or neither option.*

2.  **Apply Shrinkage to Parent Cost** 
      Mark Apply Shrinkage to Parent Cost to apply shrinkage to the finished good.

    **Apply Shrinkage to Component Cost** 
      Mark Apply Shrinkage to Component Cost to apply shrinkage to the components of the finished good.

    **Prorate Setup Time** Mark Prorate Setup Time to distribute setup costs for tandard-cost items.

3.  If you marked Prorate Setup Time, select the quantity to use for calculating
    setup costs for standard-cost items.

**Average Quantity** The setup costs of an item (setup time multiplied by setup labor rate) will be divided by the average quantity of the item. You specify the average quantity of an item in the Item Engineering Data window.

Refer to *Entering item engineering data* in *Chapter 8, “Item engineering data,”* of the Manufacturing Core Functions documentation for more information about specifying the average quantity of an item.

**Standard Quantity** The setup costs of an item will be divided by the standard quantity of the item. You specify the standard item quantity in the Standard Cost Changes window.

Refer to *Specifying the standard quantity for a finished item* in *Chapter 14, “Standard costing revaluations,”* in the Manufacturing Core Functions documentation for more information.

4.  Mark Activate Single-Level Cost Roll Up to let users decide, in the Standard Cost Changes window, whether costs affect selected items in the BOM, or the entire BOM that includes the item. If you do not mark this option, users do not have the choice, and costs affect the entire BOM that includes the item.

5.  Decide how the Standard Cost Changes window should work.

**Rollup scope** Determines how many items are included in a standard cost rollup. You can choose to roll up all items with proposed standard cost changes, or you can choose to roll up only items affected by a change in the cost of the selected item.

**Tree view explosion level** Determines how much information is displayed when you select an item in the Standard Cost Changes window. If your business has many records, choose Single Level Bill of Material so that information is displayed more quickly. (You can always expand the view of the information, if needed.)

6.  Select a posting account for rounding differences.

7.  Choose a security set to be used when a user attempts to revalue items in the Rollup and Revalue Inventory window or in the Standard Cost Changes window.

Users who attempt to revalue items must be included in the security set, or they must enter the appropriate password before the revaluation can occur.

8.  Choose OK and close the window.

#### Shrinkage overview

Shrinkage is the anticipated loss of an item.

**Types of shrinkage**

You can specify a shrinkage value for finished goods (parent items), for components (child items), or both.

**Finished good shrinkage** Finished good shrinkage might occur if not all items that are started in production are adequate for meeting demand. For example, if you discover that one out of every 100 finished goods you produce fails inspection, you have one percent shrinkage of your finished goods. You can set up preferences so that if you need to produce 200 of this item, materials and resources will be scheduled to build 202—automatically
covering any anticipated losses from shrinkage.

**Raw material shrinkage** Raw material shrinkage might occur if some components are flawed and can’t be used in production. Raw material shrinkage also can occur if materials are wasted in the production process; for example, you might need to use materials on trial runs during your setup processes. You can indicate how much shrinkage you anticipate on an item-by-item basis.

**How shrinkage is calculated**

To calculate shrinkage, divide the extended required quantity (from either the picklist or the manufacturing order, depending on if you’re calculating shrinkage for a component or finished good) by 1, minus the shrinkage percentage. The calculated quantities reflecting shrinkage should be rounded up, if necessary.

#### Including shrinkage in Manufacturing

When you enter item information in Inventory Control, you can specify shrinkage percentages. The amounts you enter can be reflected in the quantity calculations for manufacturing orders, in cost calculations for standard cost rollups, or both.

Refer to the table for more information about where the shrinkage percentage information comes from, and how it’s determined if the shrinkage percentage is reflected in quantities or costs.


|
| **Component**                                                                                                                                                                                           | **Finished good**                                  |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| **Shrinkage information comes from ...**                             | ... the Item Resource Planning Maintenance window, but you can change the shrinkage percentage for a component when you add the component to a bill of materials in the Bill of Materials Entry window. | ... the Item Resource Planning Maintenance window. |
| **Shrinkage is reflected in the quantities if ...**                  | ... the scheduling preference you use for the manufacturing order includes the options to apply shrinkage to the quantity. Refer to *Setting up scheduling preferences.*                                |                                                    |
| **Shrinkage is reflected in costs for standard cost rollups if ...** | ... you’ve marked options to include shrinkage in standard cost rollups. Refer to *Setting up costing system default settings.*                                                                         |                                                    |

#### Shop calendars

You’ll use the Shop Calendar window to indicate which days your plant is running—and which days it isn’t. You can choose weekends, holidays, or any other days as “down days.” When you use modules such as Manufacturing Order Processing, down days can be taken into consideration in order scheduling.

You might have to make specific adjustments to the calendar when unforeseen events occur—when your plant has a down day because of a power failure, for example, or when an extra shift is scheduled.

*Settings you choose when defining the shop calendar will be the default settings for your work centers. However, after you create work centers, changes to the shop calendar won’t be reflected in existing work center calendars. Use the Shop Calendar when you’re initially setting up your company, but use work center calendars to make day-to-day adjustments.*

#### Defining the shop calendar

You need to define one shop calendar for each company, but you can adjust the shop calendar for each work center.

**To define the shop calendar:**

1.  Open the Shop Calendar window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Calendar)

![](media/MFGCAL.jpg)

The window will open to the current month and year.

2.  Enter the number of shifts, hours per shift and start time information.

*The number of shifts multiplied by the hours per shift can’t exceed 24.*

3.  Mark the option for weekly down days. You can choose None, Sundays Only, or Saturdays and Sundays.

Down days will appear in black.

4.  Mark any other down days. A message will appear, telling you that continuing with the process might affect scheduling. To continue the process, choose Yes and OK to close the window.

*To make a down day available for scheduling, select the day in the Shop Calendar window to clear the setting.*

#### Setting up work center options

Use work center default options to create two fields that will be linked to  routing operation codes. Enter the labels for the fields in the Work Center Preference Defaults window.

**To set up work center options:**

1.  Open the Work Center Preference Defaults window.

(Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Work Centers)

![](media/MFGWC.jpg)

2.  In the User-Defined Prompt fields, enter the label or labels for the additional fields you’re creating. These fields will appear in the Operations Setup window and choose OK.


#### Designating system users

System users have more access privileges than other users. Like system administrators, system users can set preferences for other users.

*Before you can designate system users, you must enter user information in the User Setup window. Refer to your System Setup Instructions (Help \>\> Contents \>\> select Setting Up the System) for more information.*

**To designate system users:**

1.  Open the Add Users window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> System User)

2.  Enter or select the user ID for an employee who is to be a system user and Choose Insert.

**To remove a system user, mark the user ID in the scrolling window and choose Remove.*

1.  Continue, repeating steps 2 and 3 to add as many system users as you like.

2.  Choose OK and close the window.

### Chapter 2: Security

Security builds safeguards into your software to restrict access to information, processes, or windows. In Manufacturing, each of these types of security is included. You should understand each of the three security types before setting up security access for your users.

*Before you set up security access for Manufacturing, you should have defined users and determined the level of access each user will have.*

This information is divided into the following sections:

-   *Manufacturing security types*

-   *Process security*

-   *Creating and modifying process security sets*

-   *Using Manufacturing module security*

#### Manufacturing security types

Refer here for information about some of the terms related to security.

**User security** You can determine which windows and reports each user in your organization can use. Users can’t use any *modified* windows or reports until you give them access to the windows and reports. Window and report security is used throughout your accounting and manufacturing system. To learn more about setting up user security, refer to the System Setup Guide (Help \>\> Contents \>\> select Setting up the System).

*User security can be used to restrict access only to windows and reports. To restrict access to information on a field-by-field basis, use Field Level Security or create alternate forms and windows. Refer to the Modifier User’s guide for more information about creating alternate forms and windows. Refer to the System Setup Guide (Help \>\> Contents \>\> select Setting up the System) for more information about Field Level Security.*

**Process security** Process security is a special type of security that you can use to limit authority for completing special procedures in Manufacturing, such as revaluing inventory or generating manufacturing orders from Sales Order Processing. First, you must define process security sets. A process security set can be based on a list of users who will have authority to complete a specific process, or it can be based on a password. You can create as many process security sets as you like and apply different
sets to different processes throughout Manufacturing.

*For more information, refer to Process security and Creating and modifying process security sets.*

**Manufacturing module security** Some Manufacturing processes—such as generating Material Requirements Planning (MRP) information or updating routing records—can be done only when no other users are working with certain records. With the security that is provided for bills of materials, routings, data collection, and MRP, you can see which other users are using records that prevent you from completing MRP regeneration or other processes. You can end other users’ sessions or you can ask them to end their sessions.

You also can use Manufacturing module security to unlock records that might become locked if a user’s computer becomes suspended. If a power failure occurs when a user is updating a routing record, for example, the routing record might need to be unlocked.

*For more information, refer to Using Manufacturing module security.*

#### Process security

Process security is useful for safeguarding certain manufacturing processes, such as revaluing standard cost items or overriding purchase order quantities. With process security in place, you can limit who in your company has authorization to complete certain critical processes.

Manufacturing process security system uses security sets—passwords or groups of user IDs—to limit who can complete certain tasks. When a security set for a task is based on a group of users, only users in that group can perform the task. When a security set for a task is based on a password, any user who attempts to complete the task will be required to enter the appropriate password before proceeding.

You can use process security for completing the following tasks.

-   Revaluing inventory

-   Linking job elements to jobs

-   Changing a sales order line item quantity when a manufacturing order is
    linked to it

-   Changing job links

-   Changing the status of a job

-   Overriding manufacturing order quantities

-   Changing order fulfillment history

-   Auto-generating manufacturing orders

-   Managing links between manufacturing orders and purchase orders for
    outsourcing

-   Managing shipments to outsourcing vendors

-   Updating groups of bills of materials

#### Creating and modifying process security sets

You can create an unlimited number of security sets. You can use the same security set for all tasks that are protected by process security, or you can create a separate security set for each task.

Once you’ve created a process security set, you can modify it at anytime. For example, you might change the password or add or remove user IDs.

**To create or modify process security sets:**

1.  Open the Process Security Setup window. (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Process Security)

2.  Enter or select a name for the security set.

3.  If you’re creating a new security set, mark Password or User ID to determine the kind of security set you’re creating. If you’re modifying an existing security set, skip to step 4.

    -   If you marked Password, enter the password.

    -   If you marked User ID, use the lookup button on the User IDs field to choose the users to include in the security set.

4.  Make changes, as needed.

    -   To change a password, select the text in the Password field and enter the new password.

    -   To add a user, choose a user in the User IDs field.

    -   To remove a user, mark the user ID in the scrolling window and then choose Remove.
5.  Choose Save.

#### Using Manufacturing module security

>   You can use Manufacturing module security to unlock locked bills of
>   materials, routings, data collection records, manufacturing orders, and
>   MRP-planned orders. You also can use module security to remove MRP users.
>   You might need to unlock records to perform certain processes, such as
>   regenerating MRP information.

>   The window you’ll use to view or unlock locked records will depend on the
>   type of record you’re working with.

>   You need system administrator access to unlock most records. To unlock some
>   records, you must supply the system password to open the window. To unlock
>   other records, you must supply the system password when you choose the
>   Delete button.

**To use Manufacturing module security:**

1.  Open the appropriate window for the type of record to unlock.

>   Refer to the table for more information.

| **Type of record**  | **Window and path**                                                                                        |
|---------------------|------------------------------------------------------------------------------------------------------------|
| Bill of materials   | BOM Security window - (Transactions \>\> Manufacturing \>\> Bill of Materials \>\> Security)               |
| Routing             | Routing Security window - (Transactions \>\> Manufacturing \>\> Routings \>\> Security)                    |
| Data collection     | Data Collection Transaction Security window - (Transactions \>\> Manufacturing \>\> WIP \>\> TRX Security) |
| Manufacturing order | Manufacturing Order Security window - (Transactions \>\> Manufacturing \>\> Manufacturing Orders \>\>      |
| MRP                 | MRP Security window - (Transactions \>\> Manufacturing \>\> MRP \>\> Security)                             |
| MRP-planned orders  | MRP-Planned Order Security window - (Transactions \>\> Manufacturing \>\> MRP \>\> MRP Planned Order       |

>   Security)

>   Security)

1.  View the information in the scrolling window. Each of these windows displays
    the user ID of the person who has locked each record.

>   *It’s a good idea to contact the user and request that he or she close the
>   window to unlock a record. If that’s not possible, use these windows to end
>   user sessions.*

1.  Highlight a record to unlock in the scrolling window.

2.  Choose Delete.

3.  Repeat steps 3 and 4 to unlock as many records, as needed.

4.  When you’ve finished, close the window.

### Chapter 3: Manufacturing core functions setup

>   Information about setting up system settings for use with core functions
>   modules— Bills of Materials, Sales Configurator, and extensions to Microsoft
>   Dynamics GP Sales Order Processing—is included here. You must set up system
>   and user settings to determine how Manufacturing will function for your
>   business.

>   This information is divided into the following sections:

-   *Setting up bills of materials system settings*

-   *Phantom items as components of phantom items*

-   *Setting up Sales Configurator options*

-   *Setup options for sales order extensions*

-   *Setting up manufacturing sales order due dates*

-   *Setting up manufacturing orders for sales orders*

-   *Setting up order fulfillment options*

#### Setting up bills of materials system settings

>   System settings for Manufacturing Bill of Materials help you to accomplish
>   several tasks. Refer to the table for more information.

| **Task**                                                                                                                                                                 | **Required?** |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Specify whether component lead time should be calculated based on the manufacturing order start date or the manufacturing order due date.                                | Yes           |
| Select the visual cues for the Bill of Materials Entry window and the Bill of Materials View window. (This can be changed on a user-by-user basis.)                      | No            |
| Set up user-defined fields for bills of materials.                                                                                                                       | No            |
| Specify whether site information for building a phantom subassembly item will be based on the phantom item’s bill of materials or the finished goods’ bill of materials. | No            |
| Specify options for mass-changing bills of materials.                                                                                                                    | No            |

>   You’ll use the BOM Preference Defaults window to complete these tasks.

>   **To set up bills of materials system settings:**

1.  Open the BOM Preference Defaults window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Bill of
    Materials)

IMAGE - MFGBOM

![A screenshot of a cell phone Description automatically generated](media/ad05a25ecf94b6674192d1e77f8455cb.jpg)

1.  Specify which visual cue should be used by default in the Bill of Materials
    Entry window and the Bill of Materials View window.

>   Each user can choose a different visual cue, if needed.

1.  Choose the date that should be used to calculate component lead time dates.
    This selection determines how lead times are calculated for all components
    and can’t be changed on a per-user basis.

>   For more information about lead time offsets, refer to *Lead time
>   calculations* in *Chapter 9, “Bill of Materials overview,”* in the
>   Manufacturing Core Functions documentation.

1.  You can enter labels for user-defined fields, if needed.

>   Later, you can add information in the user-defined fields in the Bill of
>   Materials Entry window. You can enter information for each component in each
>   bill of materials. Refer to *Changing component details* in *Chapter 11,
>   “Bill of Materials entry,”* in the Manufacturing Core Functions
>   documentation for more information.

1.  To specify how the issue-to site for components of phantom items are
    determined, you can use the Use Work Centers from the phantom’s BOM option.

>   Refer to the table for more information.

|                                                                                | **Option is marked**                                                                                   | **Option is unmarked**                                                                                    |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **Phantom item has no issue-to site in the finished goods’ bill of materials** | The issue-to site for components of the phantom item comes from the phantom item’s bill of materials.  |                                                                                                           |
| **Phantom item has an issue-to site in the finished goods’ bill of materials** | The issue-to site for components of the phantom item comes from the finished good’s bill of materials. | The issue-to site for components of the phantom item are comes from the phantom item’s bill of materials. |

>   Refer to *Phantom items as components of phantom items* for examples of how
>   the rules are applied when a manufacturing order for a phantom item includes
>   phantom components.

1.  To specify the default spacing between position numbers, enter a number in
    the New Component Position Number Incremental Spacing field.

>   We recommend that you leave a few spaces in between position numbers to
>   allow room to add more position numbers later. Refer to *Chapter 10,
>   “Position numbers”* in the Core Functions manual for more information.

1.  Mark the Archive copies of mass-changed BOMs option to keep a copy of the
    original bill of materials each time a bill of materials is changed using
    the BOM Mass Updates window.

2.  If you marked Archive copies of mass-changed BOMs, you also can specify
    whether the revision history for the bill of materials should be archived.
    Mark Copy Revision History to the Archived BOM if revision history also
    should be stored.

3.  Mark the bill of materials types that should not be included when changing
    bills of materials using the BOM Mass Updates window. You can choose to
    exclude Manufacturing, Engineering, Configured, or Super bill of materials
    types from mass changes.

>   For example, if you mark Engineering, Engineering will be marked in the
>   Exclude BOM types from mass changes option in the BOM Mass Updates window
>   and you will need to unmark it to change an engineering bill of materials.

1.  You can enter or select a process security set if use of the BOM Mass
    Updates window should be limited to a certain group of users or should
    require a password.

>   Refer to *Process security* for more information.

1.  Choose OK and close the window.

#### Phantom items as components of phantom items

>   If you’re going to create manufacturing orders for phantom subassembly items
>   that include phantom subassemblies, rules for determining the sites for the
>   components will depend on whether you marked the Use Work Centers of
>   phantom’s BOM in the BOM Preference Defaults window.

>   Refer to the following examples for more information.

>   **Bills of materials**

>   For these examples, assume that the following is your bill of materials for
>   the finished good. Note that it includes a phantom subassembly item that has
>   its own phantom subassembly item.

| Finished good |           |                           |                           |                           |
|---------------|-----------|---------------------------|---------------------------|---------------------------|
|               | Phantom 1 | Issued to work center 100 |                           |                           |
|               |           | Component A               | Issued to work center 200 |                           |
|               |           | Phantom 2                 | Issued to work center 300 |                           |
|               |           |                           | Component B               | Issued to work center 400 |
|               |           |                           | Component C               | Issued to work center 400 |

>   **Example 1**

>   If Use Work Centers of phantom item’s BOM is marked, the picklist for the
>   manufacturing order to build Phantom 1 would include the following
>   information:

-   Component A would be issued to work center 200

-   Component B would be issued to work center 400

-   Component C would be issued to work center 400

>   **Example 2**

>   If Use Work Centers of phantom item’s BOM is not marked, the picklist for
>   the manufacturing order to build Phantom 1 would include the following
>   information:

-   Component A would be issued to work center 100

-   Component B would be issued to work center 300

-   Component C would be issued to work center 300

#### Setting up Sales Configurator options

>   Use Sales Configurator preferences to determine how Sales Configurator will
>   work for your business and how its use will affect other modules.

>   **To set up Sales Configurator options:**

1.  Open the Sales Configurator Preferences window. (Microsoft Dynamics GP menu
    \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Sales
    Configurator)

2.  Mark Display Manufacturing Order Start Date while configuring if a start
    date for the associated manufacturing orders should be created
    automatically.

>   When you open the Sales Configurator window from the Sales Item Detail
>   window, a manufacturing order automatically will be generated. If you’ve
>   marked this option, a start date for the order will be calculated and
>   included. If you don’t mark this option, a start date won’t be calculated
>   until you choose Schedule in the Sales Configurator window.

1.  Mark Display Messages for Option Promotions to see messages about special
    promotions for the options you’re using as you’re working with the Sales
    Configurator.

2.  Choose OK and close the window.

#### Setup options for sales order extensions

>   Microsoft Dynamics GP Sales Order Processing includes tools you can use to
>   manage sales functions in your manufacturing environment. However, when you
>   install Manufacturing you also must complete additional setup tasks that
>   determine how sales affect other modules. For example, you must specify
>   default settings for manufacturing orders that will be generated
>   automatically from sales orders.

>   When Manufacturing is installed, you must complete the following setup
>   procedures:

>   **Due date options** You must specify how due dates for manufacturing orders
>   linked directly to sales orders should be calculated. Refer to *Setting up
>   manufacturing sales order due dates* for more information.

>   **Manufacturing order options** To automatically generate manufacturing
>   orders from sales orders, you must specify the default settings for those
>   manufacturing orders. You also can specify whether customer priority levels
>   should affect the priority levels of manufacturing orders generated from
>   sales orders. Refer to *Setting up manufacturing orders for sales orders*
>   for more information.

>   **Order fulfillment options** To track additional information about how
>   orders are fulfilled, you must set up order fulfillment options. You can
>   specify a default carrier and FOB point. You also can select options so
>   users can modify the freight and miscellaneous charges associated with order
>   fulfillment. Refer to *Setting up order fulfillment options* for more
>   information.

*For more information about sales order processing and setup, refer to the Sales
Order Processing documentation.*

#### Setting up manufacturing sales order due dates

>   Use the Manufacturing Series Sales Order Preferences window to specify how
>   due dates for sales orders will be calculated.

>   **To set up manufacturing sales order due dates:**

1.  Open the Manufacturing Series Sales Order Preferences window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Sales \>\> Sales
>   Order Processing \>\> Additional \>\> Manufacturing Sales Order Prefs)

IMAGE – MFGSOP.jpg

![A screenshot of a cell phone Description automatically generated](media/11e4e8e3673094ecc02c4f9337ec81df.jpg)

1.  To be warned when you schedule a sales order due date on a date that is a
    company-wide down day, mark Check “Down Days.” You also can specify how the
    alternate date for the sales order should be calculated.

>   **None** Mark None if a new due date shouldn’t be assigned.

>   **Move Earlier** Mark Move Earlier to assign the closest preceding open
>   date. **Move Later** Mark Move Later to assign the closest following open
>   date.

1.  Enter the number of days the in-house due date for the order should precede
    the requested ship date.

>   The in-house due date must be on or before the Requested Ship Date, and the
>   Requested Ship Date must be on or before the Customer Promise Date.

-   If the in-house due date should be a certain number of days before the
    requested ship date, enter the number of days in the Due Date Offset field.

-   If the in-house due date should be the same as the requested ship date,
    leave the Due Date Offset field blank.

1.  You can continue setting up Manufacturing sales order options by completing
    *Setting up manufacturing orders for sales orders*, or you can choose OK and
    close the window.

#### Setting up manufacturing orders for sales orders

>   Use the Manufacturing Series Sales Order Preferences window to enter default
>   settings for manufacturing orders that are generated automatically from
>   sales order entries. Manufacturing orders created from sales orders
>   automatically are scheduled, and their picklists are built.

>   **To set up manufacturing orders for sales orders:**

1.  Open the Manufacturing Series Sales Order Preferences window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Sales \>\> Sales
>   Order Processing \>\> Additional \>\> Manufacturing Sales Order Prefs)

1.  To allow users to create manufacturing orders during the sales order entry
    process, determine the level of user action you’ll require from the users.

>   Refer to *Manufacturing orders generated from sales* in *Chapter 20, “Sales
>   order entry,”* in the Manufacturing Core Functions documentation for
>   information about how the fulfillment method for an item and this setting
>   affect how Manufacturing handles back-order quantities.

>   **Enable Silent MO Generation** Mark this option to automatically generate
>   manufacturing orders when sales orders are entered for item quantities that
>   are greater than what is currently in stock.

>   **Enable Manual MO Generation** Mark this option to allow users to generate
>   manufacturing orders. If you mark this option, users will need to provide
>   basic information for the manufacturing order.

1.  Set the Priority list to reflect the priority level for automatically
    generated manufacturing orders. The priority level is reference only and
    won’t affect scheduling.

2.  Mark Apply Customer Priority to Generated MO if you’re using customer
    priority levels and the priority level that you’ve assigned to customers
    should affect the priority of manufacturing orders generated from sales
    orders.

>   If you mark the option, specify how customer priorities should be translated
>   to manufacturing order priorities.

*You can specify a customer’s priority level in the Customer Maintenance window
(Cards \>\> Sales \>\> Customer). For more information, refer to Microsoft
Dynamics GP Sales Order Processing documentation.*

1.  To limit user access for changing sales order quantities for sales orders
    that have associated manufacturing orders, enter or select a process
    security set in the Edit SO QTYs when MO is Attached Process Security field.

>   This option allows you to override back-ordered, canceled, invoiced and
>   billed quantities so the quantities can equal the quantity ordered or
>   invoiced. For example, suppose a customer has ordered 1,000 widgets and you
>   want to ship the 500 widgets that have been built so far. If you use this
>   option, you can handle partial shipments.

*If you don’t select a process security set but try to adjust a sales order
quantity for a sales order with an associated manufacturing order, a message
will warn you that you don’t have the appropriate access privileges to change
the sales order quantity.*

1.  Mark the default order status for automatically generated manufacturing
    orders. You can choose Open or Released. You can change the order status for
    specific manufacturing orders.

>   *Refer to Manufacturing order statuses and How statuses limit
>   activities—both in*

*Chapter 6, “Manufacturing order overview,” in the Manufacturing Production
Functions documentation—for more information.*

1.  Mark Change MO status on Order Transfer to change the status of a
    manufacturing order when the status of the associated sales order changes
    from Quote to Order.

2.  To limit authority for generating manufacturing orders, enter or select a MO
    Generation Process Security Set.

*For more information about process security sets, refer to Process security and
Creating and modifying process security sets.*

1.  Enter or select a default scheduling method for automatically generated
    manufacturing orders. You can change the scheduling method for a
    manufacturing order.

*For more information about creating scheduling methods, refer to Setting up
scheduling preferences.*

1.  Enter or select the default inventory site from which items for the
    manufacturing order will be drawn. You can change the Draw Inventory From
    Site for a manufacturing order.

2.  Choose OK and close the window.

#### Setting up order fulfillment options

>   Manufacturing extends the order fulfillment options that are available
>   through Sales Order Processing. Use the Order Fulfillment Setup window to
>   set up Manufacturing-specific order fulfillment features.

*Besides setting up these system preferences, you must be sure other sales order
type and item options are in place. Refer to Requirements for order fulfillment
history in Chapter 21, “Order fulfillment,” in the Manufacturing Core Functions
documentation for more information.*

**To set up order fulfillment options:**

1.  Open the Order Fulfillment Setup window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Sales \>\> Sales Order Processing \>\> Additional \>\>
    Order Fulfillment Setup)

IMAGE – MFGOFS.jpg

![A screenshot of a cell phone Description automatically generated](media/a52df266f547d8a3c9978f9e0100909c.jpg)

1.  Enter or select the default shipping method.

2.  Select the default unit of measurement from the Shipping U of M list.

3.  Enter the default UPS zone.

4.  Enter or select the default FOB point.

5.  To restrict authority for editing fulfillment history records, enter or
    select a process security set in the History Edit Security Set field.

*Refer to Process security for more information about process security sets.*

1.  Mark Override Freight Charges so users can enter freight charges in the
    Freight and Misc Adjustments window.

2.  Mark Override Miscellaneous Charges so users can enter miscellaneous charges
    in the Freight and Misc Adjustments window.

3.  Choose OK and close the window.

### Chapter 4: Manufacturing production functions setup

>   This documentation includes information about setting up system settings for
>   use with production functions modules: Routings, Manufacturing Order
>   Processing, Outsourcing, and Work in Process. You’ll need to set up system
>   and user settings to determine how Manufacturing will function for your
>   business.

>   This information is divided into the following sections:

-   *Setting up routing update options*

-   *Setting up sequence entry options*

-   *Setting up sequence spacing, notes, and pointer usage*

-   *Scheduling preferences*

-   *Setting up scheduling preferences*

-   *Setting up additional scheduling method options*

-   *Setting up manufacturing order processing*

-   *Specifying outsourcing manufacturing order options*

-   *Setting up data collection options*

-   *Setting up options for outsourcing costs*

-   *Rules for outsourcing setup changes*

### Setting up routing update options

>   Routing update options compare planning routings—those that are used to
>   determine resource requirements for potential manufacturing orders—and
>   active routings—those that are used on the production floor to manufacture
>   goods. The planning routing can be converted to an active routing and tied
>   to a manufacturing order.

>   **To set up routing update options:**

1.  Open the Routing Preference Defaults window. (Microsoft Dynamics GP menu
    \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Routings)

IMAGE – MFGRPD.jpg

![A screenshot of a cell phone Description automatically generated](media/a2ab0984c7944fade6bb1f40b1e9bb9b.jpg)

1.  Determine how planning routings should be updated.

>   **Compare as Number** If all planning routing sequence numbers are numeric,
>   mark Compare as Number.

>   **Confirm Save** To have a confirmation message displayed before planning
>   routing updates are changed, mark Confirm Save.

1.  Determine if updating other planning routings should be based only on the
    routing name and sequence number. Whether a routing update is reflected in
    other routings is always determined by the routing name and sequence number.
    Those two criteria must match before a change in one routing sequence is
    reflected in a sequence in another routing.

-   If you mark Match WC ID, the routing sequence change will be reflected in
    only routing sequences that have the same routing name, sequence number and
    work center.

-   If you don’t mark Match WC ID, all routings with that routing name and
    sequence number will be updated, regardless of the work center ID.

1.  Determine how to update active routings.

>   Whether a routing update is reflected in other routings is always determined
>   by the routing name and sequence number. Those two criteria must match
>   before a change in one routing sequence is reflected in a sequence in
>   another routing.

-   If you mark Match WC ID, the routing sequence change will be reflected in
    only those routing sequences that have the same routing name, sequence
    number and work center.

-   If you don’t mark Match WC ID, all routings with that routing name and
    sequence number will be updated, regardless of the work center ID.

1.  Mark one or both search options for your routing records.

    -   If you mark Item Number, searches of routing records will return only
        routings that include the item number you specify.

    -   If you mark Routing Name, searches of routing records will return only
        the routing that has the name you specify.

2.  Choose OK.

### Setting up sequence entry options

>   If you print routing information for use on the production floor, you can
>   use sequence entry options to ensure that information your employees need is
>   included on the reports.

>   **To set up sequence entry options:**

1.  Open the Routing Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> Routings)

1.  Mark Replace Routing Seq. Descr. with WC Descr. to see work center
    descriptions rather than routing sequence descriptions.

2.  Mark Append WC Description to Routing Notes to have the work center
    description added to the routing notes.

3.  Mark Attach WC Notes to Routing Notes to have the work center notes added to
    the routing notes.

4.  Choose OK.

### Setting up sequence spacing, notes, and pointer usage

>   Use the Routing Preference Defaults window to set up options for sequence
>   number spacing, to specify if routing sequence notes should be included with
>   certain reports, and to determine if pointer routings can be used in your
>   facility. Pointer routings are template routings you can use in your regular
>   routings to describe how to complete routine tasks, such as packaging and
>   shipping products.

>   **To set up sequence spacing, notes and pointer usage:**

1.  Open the Routing Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> Routings)

1.  Enter the default spacing for routing sequence numbers. For instance, if
    sequence steps should be numbered 10, 20, 30 and so on, the Sequence Spacing
    would be 10.

*We recommend using spacing intervals of 10 or 100. This makes it easier to
insert a new sequence between two existing sequences.*

1.  Mark Use Pointer Routings to use pointer routings in your system.

*Refer to Pointer routings in Chapter 5, “Pointer routings,” in the
Manufacturing Production Functions documentation for more information about
pointer routings.*

1.  To include routing sequence notes with the shipping report that accompanies
    items shipped to an outsourcing vendor, mark Include Sequence Notes Report
    with Outsourcing Shipping Report.

2.  To include routing sequence notes with the purchase order that is created to
    purchase outsourced services, mark Include Sequence Notes Report with
    Purchase Order Report.

3.  Choose OK.

### Scheduling preferences

>   Use the Scheduling Preferences window to create scheduling preferences. Each
>   scheduling preference includes information about scheduling manufacturing
>   orders and handling material issues such as applying shrinkage, posting
>   transactions and closing manufacturing orders.

>   Unlike options you set up in other user preferences windows in
>   Manufacturing, scheduling methods you define here can be used throughout the
>   system by any user who has authority to open and schedule manufacturing
>   orders.

>   **End Item/Raw Material Issue** Use the Scheduling Preferences window to
>   determine if shrinkage percentages are applied to raw materials and finished
>   item quantities. You’ll also choose the default inventory site accounts that
>   raw materials will be drawn from and finished goods will be posted to. The
>   default sites will have precedence over any default site that you select in
>   the Item Quantities Maintenance window.

>   **Scheduling Options** Use Scheduling Options to determine how the amount of
>   time estimated to complete a manufacturing order should be calculated. If
>   the option is unmarked, the end quantity of the manufacturing order is
>   multiplied by the per-piece cycle time to determine the estimated time to
>   complete the manufacturing order. If the option is marked, the starting
>   quantity is used to determine the estimated time to complete the
>   manufacturing order.

>   **Closing Options** If you’re using configured bills of materials (generated
>   through the Sales Configurator), use these options to determine what happens
>   to the configured bills of materials you create when the associated
>   manufacturing orders are closed. You can archive the configured bills of
>   materials—move them to another directory for storage, you can delete the
>   configured bills of materials from the list of “active” bills of materials,
>   or you can do both.

>   **Process Security** To require special authorization to override the
>   minimum and maximum manufacturing order size, you can select a process
>   security set to restrict authority for this process.

### Setting up scheduling preferences

>   Use the Scheduling Preferences window to define different scheduling methods
>   for your products. You also can use this window to choose the default
>   scheduling method.

>   When you create a scheduling preference, you can determine how shrinkage
>   percentages are applied to manufacturing orders that use that scheduling
>   preference. You can choose from the following available options:

>   **Apply Shrinkage to End Item Starting Quantity** Ending quantities for
>   manufacturing order finished goods should reflect shrinkage amounts.

>   Doing this will help to ensure that the number of finished goods you get
>   from a manufacturing order reflects the anticipated shrinkage of the
>   finished goods during the manufacturing process. For instance, an
>   electronics component manufacturer might know that she can expect to have 3%
>   shrinkage when a certain widget is produced; that is, to make 100 widgets,
>   she’ll have to plan to make 103 widgets, to cover the expected shrinkage.
>   Refer to *Shrinkage overview* and *Including shrinkage in Manufacturing* for
>   more information.

>   **Apply Shrinkage to Raw Material Issue** To ensure that sufficient
>   materials are issued to manufacturing orders to reflect component item
>   shrinkage amounts.

>   Doing this will help to ensure that the amounts of raw materials you issue
>   to manufacturing orders will reflect the anticipated shrinkage of the
>   components. For example, an electronic components manufacturer might know
>   that she can expect 2% shrinkage for a certain component. That is, she knows
>   that for every 100 components she issues for use in a manufacturing order,
>   two will be unsuitable for some reason. Refer to *Shrinkage overview* and
>   *Including shrinkage in Manufacturing* for more information.

*You also must define other aspects of each scheduling method, such as
auto-posting and process security preferences. Refer to Setting up manufacturing
order processing and Creating and modifying process security sets for more
information.*

>   **To set up scheduling preferences:**

1.  Open the Scheduling Preferences window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> MO Schedule
    Prefs)

>   IMAGE - MFGSP.jpg

![A screenshot of a cell phone Description automatically generated](media/66babca6de2ed03cfbc56271d6c2ba7d.jpg)

1.  Enter the name of the scheduling preference.

2.  If this scheduling preference is to be the default scheduling preference,
    mark Default. You can specify only one default scheduling method. The
    default scheduling method will be the default scheduling preference for each
    manufacturing order you create, but you can select a different scheduling
    preference, if needed.

>   If you’re using quick manufacturing orders, you must specify a default
>   scheduling method.

1.  Determine how to deal with item usage issues.

2.  Choose a default inventory site to draw inventory from for manufacturing
    orders scheduled with this scheduling preference.

3.  Choose a default inventory site to post inventory to when manufacturing
    orders are closed.

4.  Choose Save.

### Setting up additional scheduling method options

>   Use the Scheduling Preferences window to set up additional options that
>   affect how your material requirements are calculated. You also can specify
>   how configured bills of materials will be handled after their associated
>   manufacturing orders are closed. The window also includes an option for
>   using process security to enforce manufacturing order quantities.

>   **To set up additional scheduling method options:**

1.  Open the Scheduling Preferences window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> MO Scheduling
    Prefs)

2.  Enter or select a scheduling preference.

3.  Mark the closing options that reflect how the configured bills of materials
    should be handled. You can mark either or both options.

*Complete this step only if you’re using the Manufacturing Series Sales
Configurator.*

>   **Archive (if possible) Configured BOM** Saves the configured bill of
>   materials in an archive.

>   **Delete Configured BOM when MO is closed** Deletes configured bills of
>   materials after their associated manufacturing orders are closed.

1.  Set process security to limit users’ abilities to override the minimum or
    maximum manufacturing order sizes.

    -   To use an existing process security set, choose the Process Security
        lookup button and select the appropriate set.

    -   To create a new process security set to restrict users’ access to this
        process, enter the name of the new process security set in the Process
        Security field.

>   A message will be displayed and you’ll have the option to create a new set.
>   Choose yes.

*Refer to Creating and modifying process security sets.*

1.  Mark the Schedule Manufacturing Order Start QTY option to calculate the
    estimated time needed to complete a manufacturing order based on the start
    quantity of the manufacturing order. If you don’t mark this option, the
    estimated time will be calculated based on the end quantity of the
    manufacturing order.

2.  Select a default scheduling method. This scheduling method—Forward Infinite
    or Backward Infinite—will be used when the scheduling preference is used for
    manufacturing orders you enter in the Manufacturing Order Entry window.

*Manufacturing orders that are generated—for example, manufacturing orders that
are suggested by MRP processing—always use backward infinite scheduling because
they are created based on a due date rather than on a start date.*

1.  Choose Save and close the window.

### Setting up manufacturing order processing

>   Use the Manufacturing Order Preference Defaults window to enter information
>   that’s used when you work with manufacturing orders. For example, you can
>   specify a beginning number for your manufacturing orders, determine how
>   configured bills of materials will be handled, and determine how default
>   values are calculated when you close a manufacturing order.

You also can use the window to set up process security for tasks related to
outsourcing and to set up an extra field for tracking outsourcing information.
Refer to *Specifying outsourcing manufacturing order options* for more
information.

**To set up manufacturing order processing:**

1.  Open the Manufacturing Order Preference Defaults window. (Microsoft Dynamics
    GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\>
    Manufacturing Orders)

>   IMAGE – MFGOPD.jpg

![A screenshot of a social media post Description automatically generated](media/55bf80301c52d087d8fdb675407688b5.jpg)

1.  Enter beginning identifiers for manufacturing orders, for receipts, and for
    pick documents. You can use letters and numbers.

>   The identifiers are the next default identifiers, and also are the basis of
>   future identifiers. For example, if you enter MO001, the next order will
>   automatically be numbered MO002, then MO003, and so on.

1.  Select options for component allocations.

    -   If components should be allocated when the manufacturing order status is
        Released, mark the Allocate Inventory when MO Status becomes Released
        option.

>   If you mark the option to allocate components automatically when the status
>   of manufacturing order is changed to Released, component transactions
>   automatically are created. You can use the Manufacturing Component
>   Transaction Inquiry window to view information about the allocations. Refer
>   to *Viewing component transaction information* in *Chapter 12,
>   “Manufacturing order inquiries,”* in the Manufacturing Production Functions
>   documentation for more information.

>   Special rules apply if you mark this option and there are shortages of some
>   components when you change the status of a manufacturing order to Released.
>   Refer to *Component shortages and automatic allocations* in *Chapter 7,
>   “Manufacturing order entry,”* in the Manufacturing Production Functions
>   documentation for more information.

-   If component items should remain allocated when a reverse issue transaction
    is posted, mark Allocate upon Reverse Issue. (This means that if you
    reverse-issue components, the component quantities will remain allocated.
    You can then reverse-allocate them later, if needed.)

1.  To print notes attached to the picklist with the picking report, mark Print
    Picklist Notes with Picking Report.

2.  Mark Manually select serial/lot numbers in Quick MO if you want to choose
    the serial and lot numbers of components used for quick manufacturing
    orders.

3.  Mark Require Serial/Lot Linking to require that all serial-numbered
    component items and all lot-numbered component items are linked to the
    serial-numbered or lot-numbered finished good item.

>   If you mark the Require Serial/Lot Linking option, you must link all
>   available serial-numbered and lot-numbered component items to a finished
>   good in the Manufacturing Serial/Lot Link Entry window before posting.

1.  Specify whether lot numbers should be selected automatically by date
    received or expiration date. The default option is Expiration Date.

>   **Date Received** Mark this option to have lot numbers selected
>   automatically in the order that the items were received.

>   **Expiration Date** Mark this option to have lot numbers selected
>   automatically in order of their expiration dates.

1.  Specify how to handle information about canceled and closed manufacturing
    orders.

>   **Remove Canceled** Mark this option to set up a default entry for removing
>   canceled orders. If you mark this option, the Canceled Orders option will be
>   marked when you use the Remove Manufacturing Orders window. The number of
>   days you enter will be used to calculate the Last Change Date in the Remove
>   Manufacturing Orders window.

>   **Remove Closed** Mark this option to set up a default entry for removing
>   closed manufacturing orders. If you mark this option, the Closed Orders
>   option will be marked when you use the Remove Manufacturing Orders window.
>   The number of days you enter will be used to calculate the Last Change Date
>   in the window.

1.  Determine how default quantities for manufacturing orders should be
    calculated when you close a manufacturing order. You can choose to have
    default quantity calculated based on the original manufacturing order start
    quantity or the total quantity received. To decide on a case-by-case basis
    for each manufacturing order, mark None.

>   For more information, refer to *How required quantities are calculated* in
>   *Chapter 6, “Manufacturing order overview,”* in the Manufacturing Production
>   Functions documentation.

1.  Specify options for closing manufacturing orders. Mark the appropriate
    options in the scrolling window at the bottom of the window.

>   Refer to the table for more information about the effect of each option.

**Allow Negative WIP Quantities**  
To be able to apply more labor, machine or material costs to a manufacturing
order than already exist in WIP for the order, mark this option. This can be
helpful if you want to enter labor and machine costs for an actual-cost finished
good but don’t want to backflush those costs or do data collection.

>   If your company is an average cost environment, be sure this option is not
>   marked. Negative inventory should not be allowed in that case.

**Delete Configured BOM when**

A configured bill of materials automatically is removed when the associated
manufacturing order is closed. (Deleted bills of materials can’t be retrieved
later.)

**Archive (if possible) Configured BOM when MO is closed**

A configured bill of materials automatically is archived when the associated
manufacturing order is closed. (Archiving should be possible unless another bill
of materials already has been archived for the manufacturing order.) You can
retrieve an archived bill of materials, if needed.

**Display Low Component**

If quantities of a backflushed component aren’t sufficient for a manufacturing
order, a message is displayed.

**Display Low Component Issued**

If you’re closing a manufacturing order and the issued quantity of a component
(other than a backflushed component) is less than the required quantity, a
message is displayed.

**Display Material Remaining in WIP Warning**

If you’re closing a manufacturing order and there are component costs remaining
in WIP, a message appears.

**Display Labor/Machine Costs Remaining in WIP Warning**

If you’re closing a manufacturing order for an actual cost item (one with a
perpetual valuation method), a message appears if there are labor or machine
costs in WIP for the order.

**Display Unused Allocated Material Warning**

If you’re closing a manufacturing order and an allocated (but not issued)
quantity remains, a message appears.

**Display Labor/Machine Incomplete Warning**

If you’re closing a manufacturing order and there are sequences that aren’t
marked “Done,” a message appears.

**Display Low Receipt Quantity Warning**

Displays a message if you’re closing a manufacturing order and the total of all
receipts for the manufacturing order is less than the end quantity that was
specified when the manufacturing order was created.

**Display Negative WIP Quantities Warning**

Displays a message if the consumption of a component makes the WIP quantity of
an item negative.

**Display Negative Available Quantities Warning**

Displays a message when the quantity to consume or the quantity to backflush
makes the on hand quantity of a component negative.

**Display Outsourcing MO/PO Link Warning**

Displays a message if you attempt to void or cancel a purchase order that is
linked to a manufacturing order for the purchase of outsourced services.

Choose OK.

### Specifying outsourcing manufacturing order options

>   If you’re using outsourcing—if your manufacturing processes include steps or
>   services provided by outside vendors—then you can use the Manufacturing
>   Order Preference Defaults window to set up a label for a user-defined
>   outsourcing field and to specify process security sets for outsourcing
>   tasks.

-   You can specify a process security set for managing links between
    manufacturing orders and purchase orders created to purchase outsourced
    services.

-   You can specify a process security set for managing shipping information.

*Refer to Process security for more information.*

>   Use the Manufacturing Order Preference Defaults window to select process
>   security sets and to set up a field for tracking additional information for
>   shipments to outsourced vendors.

>   **To specify outsourcing manufacturing order options:**

1.  Open the Manufacturing Order Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> Manufacturing Orders)

1.  To track additional information for shipments to outsourcing vendors, enter
    a label in the User-Defined Field Label for Outsourcing Shipping Records.

>   Later on, you can make entries in the field in the Manufacturing Shipments
>   window or the Manufacturing Shipments by Vendor window.

1.  Enter or select a process security set for managing links between
    manufacturing orders and purchase orders.

2.  Enter or select a process security set for managing shipments to outsourcing
    vendors.

3.  Choose OK.

### Setting up data collection options

>   Work In Process (WIP) focuses on data collection. You can use the WIP
>   Preference Defaults window to set up default options for data collection
>   tasks.

>   Most of the data collection options you select in this window are default
>   options— users also can set their own preferences, based on their user IDs.
>   The outsourcing options, however, are company-wide and cannot be changed on
>   a user-by-user basis.

>   **To set up data collection options:**

1.  Open the WIP Preference Defaults window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> WIP)

>   IMAGE – MFGWIP.jpg

![A screenshot of a cell phone Description automatically generated](media/4be79d01041c43492eb6665335d94b86.jpg)

1.  Mark Always Use Standard Labor Rate if costs associated with a job should
    reflect the standard labor rate rather than the specific labor rate for each
    employee.

2.  Mark Enter Duration in Time Card Entry if most users will enter time for
    manufacturing order routing sequences in terms of hours and minutes, rather
    than start and stop times.

>   Marking this option doesn’t limit users in how they enter their time. The
>   option is the default setting for the Enter Duration Hours/Minutes option in
>   the Time Card Entry window. Users can mark or clear that option to enter
>   time information in either format.

1.  Mark Clear MO Number to clear the manufacturing order number each time you
    save a data collection record.

2.  Mark Clear Sequence to clear the sequence number each time you save a data
    collection record.

3.  Mark Increment Sequence to display the sequence number for the next sequence
    in the selected routing each time you save a data collection record.

4.  Mark Clear Dates to clear dates each time you save a data collection record.

5.  Mark Clear Times to clear times each time you save a data collection record.

6.  Choose OK.

>   If you’re not using outsourcing, this is the only procedure you must
>   complete in this window. If you are using outsourcing, you must also
>   complete the procedure described in *Setting up options for outsourcing
>   costs*.

### Setting up options for outsourcing costs

>   Use the WIP Preference Defaults window to specify how outsourcing costs will
>   be tracked for your company. You don’t need to complete this procedure
>   unless your manufacturing processes include outsourced services.

>   **To set up options for outsourcing costs:**

1.  Open the WIP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> WIP)

1.  Mark Apply Additional Outsourcing Costs to MO if additional costs for
    outsourcing should be applied to manufacturing orders that include
    outsourcing.

>   If you mark this option, additional costs—trade discount, tax, freight and
>   miscellaneous charges—will be debited to the finished goods account for the
>   manufacturing order, and credited to the inventory offset account.

1.  Mark Outsourced Sequences as “Done” when Service is Received if data
    collection records should reflect that a sequence is complete when you
    receive items from the outsourcing vendor.

2.  Select the cost bucket to be used to track outsourcing costs.

*If possible, choose a cost bucket that isn’t usually used by your company.
Refer to*

>   *Outsourcing cost buckets in Chapter 15, “Outsourcing overview,” of the*

*Manufacturing Production Functions documentation for more information.*

1.  If you selected a labor cost bucket, mark Allow Outsourced Labor Codes.

2.  Mark Rename Selected Cost Bucket as “Outsourcing” to have the word
    “Outsourcing” replace the usual name of the cost bucket in windows and
    reports.

3.  Choose OK.

### Rules for outsourcing setup changes

>   It is possible to change some setup options for outsourcing features.
>   However, you should be aware of these rules:

-   You cannot change from a labor cost bucket—Labor, Labor Fixed Overhead or
    Labor Variable Overhead—to a machine cost bucket, as long as your system
    includes labor code definitions that have been specified for outsourcing.

>   If you have labor codes designated for outsourcing, you must delete them
>   before you can change the cost bucket. Further, you cannot delete any labor
>   code that exists on a planning routing or as part of a manufacturing order
>   that hasn’t been closed.

-   If you change from a machine cost bucket—Machine, Machine Fixed Overhead or
    Machine Variable Overhead—to a labor cost bucket, a message will be
    displayed if any planning routing or working routing for an unclosed
    manufacturing order includes an outsourced sequence. The message will
    suggest that you review and update those routings.

-   If transactions for outsourcing costs have been saved, those transaction
    amounts will be posted to the accounts associated with the cost bucket that
    was selected when the transactions were saved.

>   For example, suppose you were using the Machine cost bucket for outsourcing
>   costs, and that you had saved transactions for outsourcing costs. If you
>   then changed to use the Labor cost bucket, the transactions would still be
>   posted to accounts for Machine costs.

### Chapter 5: Manufacturing management functions setup

>   This documentation includes information about setting up system settings for
>   use with management functions modules: Quality Assurance, Engineering Change
>   Management and Job Costing. You’ll need to set up system and user settings
>   to determine how Manufacturing will function for your business.

>   This information is divided into the following sections:

-   *Setting up Quality Assurance*

-   *ECM system settings*

-   *Setting engineering change system settings*

-   *Specifying modules for ECM warnings*

-   *Job Costing system preferences*

-   *Defining Job Costing system settings*

### Setting up Quality Assurance

>   To set up Quality Assurance, you must define the default Quality Assurance
>   (QA) site. If an item requires incoming inspection—if the Receive Purchase
>   Orders to QA Site option is marked for the item in the Item Engineering Data
>   window—the receipt will be to the QA site you select, regardless of the site
>   that’s originally entered on the purchase order. If the items meet quality
>   requirements, you must complete an inventory transfer transaction to move
>   the items from the quality assurance site to inventory. Items that don’t
>   require inspection will be posted to inventory as soon as they are received.

>   You also can specify the next numbers to be used for Non-Standard Reports
>   (NSRs) and for Supplier Corrective Action Requests (SCARs).

>   If you’re using multiple bins, items are posted to the default purchase
>   order receipts bin—either for the site or for the item-site combination—when
>   they are received and require inspection.

>   *Before you begin this procedure, be sure that the site you’re designating
>   as the quality assurance site has already been defined. Refer to Inventory
>   Control documentation for more information.*

>   **To set up Quality Assurance:**

1.  Open the QA Preference Defaults window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> QA)

2.  Choose the site for posting items that require inspection.

3.  Enter the document number for the next NSR.

4.  Enter the document number for the next SCAR.

5.  Choose OK.

### ECM system settings

>   Engineering Change Management (ECM) is a part of the Manufacturing that
>   controls and tracks product changes.

>   Basically, the ECM system tracks which products are being changed and helps
>   you deal with the effects of those changes. If you’re changing a bill of
>   materials, for instance, you might want to warn buyers that component
>   requirements might change. Some product changes will need to be communicated
>   to your customers; others might not.

>   You’ll use ECM system preferences to determine both how the ECM system works
>   for your organization—how change orders will move through your organization,
>   for example—and how the ECM system affects other Manufacturing modules.

>   These are some of the terms you’ll need to know as you’re working with
>   Engineering Change Management:

>   **Disposition code** The disposition code describes what is to be done with
>   the existing inventory quantities of the item that is being changed.

>   **Denial code** The denial code describes why a request for an engineering
>   change is being denied.

>   **Routing** In Engineering Change Management, a routing is the list of users
>   who must approve of a change before the change can be put into effect.
>   Routings can be set up so that approvals can be granted in a specific order.

### Setting engineering change system settings

>   You’ll need to complete these setup tasks once, but you can change them
>   later, if needed. User-specific preference tasks are described in *Setting
>   up engineering change user preferences*.

>   **To set engineering change system settings:**

1.  Open the ECM System Preferences window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> ECM)

IMAGE – MFGECM.jpg

![A screenshot of a cell phone Description automatically generated](media/16d612c45442124e29db5c28d021dec0.jpg)

1.  To change order numbers to be generated automatically, enter the first
    number to be used in the Next EC Number field.

2.  To be able to delete change requests, mark the Allow Deletions option.

3.  Determine if the time it takes for processing change requests should be
    tracked.

>   If it should, choose the date when tracking should begin—the ECM Statistics
>   Start Date—and set the number of days an engineering change order must be in
>   process to be considered “old.”

1.  Determine how to have change requests routed through your organization.

>   **Ignore Routing Order** If the order of the approvals doesn’t matter, mark
>   Ignore Routing Order. If this option is marked, users must review
>   engineering change orders in the order users appear in the engineering
>   change routing.

##### **Auto-mark Routing when ECR is modified** If your company uses the

>   ECM system mainly as a notification system and if change requests are to be

>   “approved” as soon as certain users view them, mark Auto-Mark Routing when
>   ECR is modified.

>   This option is the system default setting, but individual users can
>   determine if they want to use the “auto-mark” feature.

>   **Reset Change Routing when ECR is modified** If change orders should go
>   through the entire routing again if any of the reviewers make a change, mark
>   Reset Change Routing when ECR is modified.

>   **Only Allow Users in Routing to edit ECR** If only users who are part of
>   the ECM routing should be able to edit the change request, mark Only Allow
>   Users in Routing to edit ECR.

>   **Allow override on routing sign-off** If alternate users should be able to
>   approve change orders, mark Allow override on routing sign-off.

>   Alternate users will be required to supply the appropriate password to
>   approve change orders. You’ll be prompted to enter the password as soon as
>   you mark this option.

1.  Mark Use Default Routing to activate the default routing list and to require
    its use.

*Refer to Chapter 8, “Engineering change setup,” in the Manufacturing Management
Functions documentation for more information about creating routing lists for
change requests.*

1.  Choose OK to save your information and close the window.

>   You’ll also need to define disposition and denial codes, create change order
>   routings and determine which Manufacturing modules will display warnings
>   regarding change orders.

>   Refer to *Specifying modules for ECM warnings*, and to *Chapter 8,
>   “Engineering change setup,”* in the Manufacturing Management Functions
>   documentation for more information.

### Specifying modules for ECM warnings

>   Engineering Change Management provides two major benefits. First, it helps
>   ensure you’ve got the necessary approvals in place before you change a
>   product, and second, it helps notify others of those pending changes.

>   To take full advantage of the notification features in Engineering Change
>   Management, you need to specify which modules should be affected by the
>   engineering change requests in your company. You’ll use the ECM Warning
>   Display Configuration window to make your selections.

>   **To specify modules for ECM warnings:**

1.  Open the ECM Warning Display Configuration window. (Microsoft Dynamics GP
    menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> ECM
    \>\> Go To button \>\> Warning Display Configuration)

2.  Mark the modules or parts of modules that you want tied to the engineering
    change management notification system. You can mark as many or as few
    options as you like.

*If you’re using one of the modules or windows marked here and select an item
that has an outstanding engineering change, a message appears, telling you there
is an engineering change request for that item. You can continue working with
the record, or you can choose View Details to open a view-only window
summarizing the particular engineering change request.*

1.  Choose OK to save the information and close the window.

### Job Costing system preferences

>   The default settings you select for Job Costing in the Job Costing
>   Preference Defaults window will determine which transaction types can be
>   used in calculating job costs, who will be able to unlink job elements or
>   apply transactions, and how Payables Management transactions will be divided
>   among jobs.

>   Job Costing includes the following entries:

>   **Default Transaction List** After you’ve created a transaction list, you
>   can specify it to be the default transaction list for jobs. If needed, you
>   can select a different transaction list in the Job Maintenance window.

>   Refer to *Creating a transaction list* in *Chapter 12, “Job Costing setup
>   cards,”* of the Manufacturing Management Functions documentation for more
>   information.

>   **Job Security Set** The Job Security Set is a security group to apply to
>   all jobs. This will be the group of users who can change the status of a
>   job, unlink elements, or manually apply transactions. The Job Security Set
>   can be based on a group of user IDs or on a password.

>   For more information about security sets, refer to *Process security*.

>   **Default Distribution Method** Select a default method for distributing
>   cost amounts across jobs for Payables Management transactions. Most elements
>   can only be linked to one job, but some costs—such as freight and
>   miscellaneous charges— can be linked to several jobs. The default
>   distribution method will determine how the dollars are spread across the
>   jobs in the system.

-   If you select manual, you can specify the amounts to be distributed to
    different jobs.

-   If you select number of jobs, the costs will be divided among the linked
    jobs.

### Defining Job Costing system settings

>   You enter default system settings once, but you can change these entries, as
>   needed. Refer to *Job Costing system preferences* for more information.

>   **To define Job Costing system settings:**

1.  Open the Job Costing Preference Defaults window. (Microsoft Dynamics GP menu
    \>\> Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> Job
    Costing)

2.  Choose the default transaction list.

3.  Choose the job security setting to determine which group of users can
    complete job costing tasks, or which password will allow any user to
    complete those tasks.

4.  Choose the preferred method for distributing costs among jobs. Later, you
    can adjust the amounts, as needed. Choices include Manual and Number of
    Jobs.

>   **Manual** If you choose Manual, you’ll need to manually distribute costs of
>   a financial transaction among jobs.

>   **Number of Jobs** If you choose Number of Jobs, the system will distribute
>   costs based on the number of jobs currently in your system.

>   *If you select Number of Jobs, be sure that each of the jobs linked to the
>   transaction is assigned a transaction list that includes that type of
>   transaction. For example, suppose you have a receivings transaction with two
>   lines, each linked to a different job. You use the Number of Jobs method to
>   distribute Miscellaneous expense between the jobs. If only one of the jobs
>   has been assigned a job transaction list that includes the Miscellaneous
>   transaction type, then all the expense will be applied to that job.*

1.  Choose OK.

### Chapter 6: Manufacturing planning functions setup

>   Information about setting up system settings for use with planning functions
>   modules, especially Material Requirements Planning (MRP), is included here.
>   You’ll need to set up system settings to determine how Manufacturing will
>   function for your business.

>   This information is divided into the following sections:

-   *MRP system settings*

-   *Setting up general MRP options*

-   *Setting up MRP buckets*

-   *Generating MRP suggestions for supply orders*

-   *Specifying quantities to include in MRP*

-   *MRP options for past-due orders*

-   *Choosing MRP display quantities*

-   *Changing MRP quantity labels*

-   *Scheduling MRP updates*

-   *Setting security options for net changes*

-   *Restoring MRP quantity labels*

### MRP system settings

>   System preference settings for Material Requirements Planning (MRP) can be
>   grouped into several categories. MRP settings are all made in the MRP
>   Preference Defaults window.

>   **General MRP options** Use these settings and options to reflect the basic
>   use of MRP in your business. For instance, you can use these options to
>   determine the default MRP bucket size and whether sales order quotes should
>   be included in MRP calculations. You also can specify whether down days
>   should be considered when release dates are calculated for MRP-planned
>   orders. Refer to *Setting up general MRP options* for more information.

>   **Bucket options** Use these options to determine the buckets that will be
>   used to summarize MRP information. You must choose Days, but you also can
>   choose Weeks, Months, or both. You also can create a user-defined bucket to
>   view information. Refer to *Setting up MRP buckets*.

>   **Generate MRP suggestions for supply orders options** Use these options to
>   specify whether to generate MRP suggestions to move in, move out, or cancel
>   items on purchase orders or manufacturing orders to prevent shortages or
>   overages. Refer to *Generating MRP suggestions for supply orders* for more
>   information.

>   **MRP display quantities** Use these options to make decisions about your
>   material requirements. The calculations you choose will be displayed in MRP
>   windows. Refer to *Choosing MRP display quantities* for more information.

>   *These options will be system default settings. Each user can also change
>   these settings to a customized view of MRP information. Refer to Setting up
>   MRP user preferences for more information.*

>   **Quantities to include** Use these options to specify which quantities
>   should be included in MRP calculations. For example, you can choose to
>   include—or exclude—sales order quotes. Refer to *Specifying quantities to
>   include in MRP*.

>   **MRP labels** Use these options to define prompts and abbreviations that
>   are provided for various MRP quantities. You can use the default options or
>   create your own. If you choose to display these quantities, the prompts
>   you’ve created for them will be used in MRP windows. Refer to *Changing MRP
>   quantity labels* for more information.

>   **Schedule MRP options** Use these options to specify how and when to update
>   MRP information, and how far into the future to calculate MRP information.
>   Refer to *Scheduling MRP updates* for more information.

>   **Security options** Use these options to allow users to process net change
>   regeneration in the MRP Projected Available Balance Inquiry window and to
>   limit which users can process net changes. Refer to *Setting security
>   options for net changes*.

### Setting up general MRP options

>   You can set up systemwide preferences in the MRP Preference Defaults window,
>   but users can change some settings based on their user IDs.

>   **To set up general MRP options:**

1.  Open the MRP Preference Defaults window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> MRP)

2.  Mark General MRP Options, as needed.

>   **Calculate Items with no Activity** MRP processes will calculate
>   information for all items, regardless of whether they are included in any
>   sales orders, purchase orders, manufacturing orders, sales forecast, or
>   inventory activity for the MRP regeneration period.

>   **Show Items with no Activity** MRP windows will display information about
>   items with no activity. Information about items, sites, and item-site
>   combinations that have been excluded from MRP processing will also be
>   displayed in MRP windows (but the only information available for those
>   records will be the initial on-hand quantity).

>   This option isn’t available unless you mark Calculate Items with no
>   Activity.

*If you mark Show Items with no Activity, users who don’t want to see those
items can mark that preference in the MRP Preferences window. If you don’t mark
Show Inactive Items, however, no users can view the inactive records.*

1.  Mark the Activate Planning Time Fence option to have MRP-planned orders
    planned outside the time fence.

>   Refer to *Planning time fences* and *Example: Planning time fence in use* in
>   *Chapter 8, “MRP overview,”* in the Manufacturing Planning Functions
>   documentation for more information.

1.  Determine whether make or buy items should be treated as made or bought
    items. This option determines whether manufacturing orders or purchase
    orders are created or suggested when MRP processing identifies a shortage.

2.  If you’re generating manufacturing orders or MRP-planned manufacturing
    orders automatically, you must select a manufacturing order scheduling
    preference.

3.  With the Down Days Constraint list, specify which items’ release dates for
    MRP-planned orders should reflect down days in the shop calendar.

>   Refer to *Example: Planning time fence in use* in *Chapter 8, “MRP
>   overview,”* in the Manufacturing Planning Functions documentation for more
>   information.

1.  Choose OK to save your selections. You can close the window or you can
    continue to set up other MRP system preferences.

### Setting up MRP buckets

>   Use the MRP Preference Defaults window to select the default bucket size for
>   MRP information. You also can set up a user-defined bucket size to view
>   information.

>   **To set up MRP buckets:**

1.  Open the MRP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> MRP)

1.  Choose a default bucket size. Choices are Days, Weeks and Months.

*You can choose to override this setting when you recalculate MRP quantities.*

1.  To create a special bucket size, enter the number of days in the bucket in
    the User-Defined Bucket Size field, then enter a name for the bucket.

2.  Choose OK to save your selections. You can close the window or you can
    continue to set up other MRP system preferences.

### Generating MRP suggestions for supply orders

>   Use the MRP Preference Defaults window to specify that if MRP calculations
>   uncover a shortage or an overage, suggestions are generated to reschedule or
>   cancel certain manufacturing orders or purchase orders.

*You can use the MRP Quantities Query window to see which orders should be moved
in or moved out. Refer to Moving or canceling an order in the Manufacturing
Planning Functions documentation for more information.*

>   **To generate MRP suggestions for supply orders:**

1.  Open the MRP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> MRP)

1.  Mark options to generate suggestions if there is a shortage or an overage of
    an item.

>   **Move In** Mark to generate suggestions that you reschedule certain
>   manufacturing orders or purchase orders to prevent shortages from occurring.
>   If MRP calculations uncover a shortage of an item and if there’s an existing
>   order for the item in the future, the order can be “moved in” to the
>   existing order to prevent the shortage. Refer to *Moving or canceling an
>   order* in the Manufacturing Planning Functions documentation for more
>   information.

>   **Move Out** Mark to generate suggestions that you reschedule certain
>   manufacturing orders or purchase orders to prevent stock overages on the
>   current due date. An appropriate future date to move the order to cover a
>   future net requirement is proposed. Refer to *Moving or canceling an order*
>   in the Manufacturing Planning Functions documentation for more information.

>   **Cancel** Mark to generate suggestions that items should be canceled on
>   certain manufacturing orders or purchase orders to prevent stock overages.
>   If the Move Out option also is marked and a future net requirement exists
>   that the order may be moved to, the suggestion is to move out the order
>   rather than cancel the order. Refer to *Moving or canceling an order* in the
>   Manufacturing Planning Functions documentation for more information.

1.  Choose OK. You can close the window, or you can continue to enter MRP system
    preferences.

### Specifying quantities to include in MRP

>   Use the MRP Preference Defaults window to specify which manufacturing order
>   and sales order quantities should be reflected in MRP. You also can specify
>   whether past-due orders should be reflected in MRP.

>   **To specify quantities to include in MRP:**

1.  Open the MRP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> MRP)

1.  Mark options regarding how different order types and statuses are handled.

>   **Include MO Quotes** Material requirements for quote-status manufacturing
>   orders will be considered when MRP is calculated, and treated as planned
>   quantities.

>   **Include SO Quotes** Material requirements for quote-status sales orders
>   will be considered when MRP is calculated, and will be treated as planned
>   quantities.

>   **Put SO Back Orders in Firm Buckets** Requirements for back-ordered sales
>   orders will be added to the “firm” quantity requirements. If you don’t mark
>   this option, back-ordered quantities will be added to “planned” quantities.

1.  Determine if past-due manufacturing, sales orders, and purchase orders
    should be included in MRP calculations. Refer to *MRP options for past-due
    orders* for more information.

>   If you want this capability for manufacturing and sales orders, mark Include
>   Past Due for prior. Use the Days field to specify how many days past due
>   orders can be to be included in MRP calculations.

*Requirements for past-due manufacturing orders and their past-due components
and sales orders will be included in the past-due bucket of the regeneration.*

1.  Choose OK. You can close the window, or you can continue setting up MRP
    system preferences.

### MRP options for past-due orders

>   Material Requirements Planning (MRP) includes options that determine how
>   pastdue orders will be handled. You can choose to allow past-due orders for
>   sales orders, purchase orders and manufacturing orders and their past-due
>   components. If you use these options, you must specify a time period for
>   past-due orders. If a past-due order is within the time period, you won’t
>   need to create a new order to account for its quantities, and MRP quantities
>   will continue to reflect the past-due order quantities.

>   For example, suppose your company allows past-due purchase orders that are
>   within a three-day time period. You’ve ordered 100 widgets to be delivered
>   June 18. The widgets are delivered June 20. Because they arrived within the
>   three-day time period, you can accept the order without having to create a
>   new one, and MRP quantities will still be current. MRP calculations will
>   reflect the past-due widgets, so no shortage will be reported.

>   If the delay of the widgets then caused the delay of the manufacturing order
>   fulfillment by a day, the order would still be fulfilled and its finished
>   goods included in MRP calculations.

>   If you choose not to use these options for handling past-due orders, MRP
>   will ignore the quantities on the past-due orders and you’ll need to create
>   new orders (with new due dates) to handle the quantities.

### Choosing MRP display quantities

>   You can choose the MRP quantities to display in MRP windows.

*Refer to online help for information about how the different quantities are
calculated. Some of these quantities will reflect MRP-Planned orders and
demand.*

>   **To choose MRP display quantities:**

1.  Open the MRP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> MRP)

1.  In the MRP Display Quantities section, choose an MRP quantity from each of
    the lists. The quantities you choose will be displayed in your MRP windows.

>   For descriptions of MRP quantities, refer to *MRP quantities* in *Chapter 8,
>   “MRP overview,”* in the Manufacturing Planning Functions documentation.

*The selections you make for displaying MRP quantities are system settings, but
individuals can choose to have different quantities displayed.*

1.  Choose OK. You can close the window, or you can continue to enter MRP system
    preferences.

### Changing MRP quantity labels

>   If you use different terminology for MRP quantities, you can change the
>   labels on the fields and have those labels used where the quantities are
>   displayed.

*The changes you make to the labels won’t be reflected in printed documentation
or online help, so it’s a good idea to be sure that you have agreement from all
users before making this change.*

>   **To change MRP quantity labels:**

1.  Open the MRP Preference Defaults window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> MRP)

2.  Choose Redefine MRP Labels to open the Redefine MRP Labels window.

IMGAGE – MFGMRPL.jpg

![A screenshot of a cell phone Description automatically generated](media/19a5e4ca7d736395d9c686c7fb3983f8.jpg)

1.  Change the terminology for as many or as few labels as you like. To reset
    the labels, choose Restore Original Values.

2.  Choose OK.

### Scheduling MRP updates

>   Use the Schedule MRP window to schedule when to update MRP information. You
>   can create one schedule for a full regeneration and one schedule for a net
>   change. A full regeneration calculates all MRP requirements through the
>   defined period of time. A net change recalculates MRP information only for
>   those orders that have changed since the last time MRP was calculated. You
>   must be a system administrator to open this window.

>   A scheduled MRP run is a scheduled Microsoft SQL Server® job. The SQL Server
>   Agent must be running for the scheduled MRP to run.

>   **To schedule MRP update:**

1.  Open the MRP Preference Defaults window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> System Defaults \>\> MRP)

2.  Choose Schedule MRP to open the Schedule MRP window.

3.  If you are scheduling a full regeneration, enter the following information
    and choose Save.

>   **Run for** Specify how far into the future MRP information should be
>   calculated. Enter a number and select days, weeks, or months.

>   **Buckets** Mark to determine how MRP information will be displayed. Days
>   must be one of your choices. The more options you mark, the longer MRP
>   processing will take.

1.  From the Regeneration Type list, select a type of MRP update process.

2.  Enter how often to run the update.

3.  Mark when the update should occur. The schedule can occur once at a specific
    time or at intervals that you specify.

4.  Choose Save.

5.  Choose OK to close the window.

### Setting security options for net changes

>   Use the MRP Preference Defaults window to allow users to process net change
>   regeneration in the MRP Projected Available Balance Inquiry window and to
>   limit which users can process net changes.

>   For more information, refer to *Process security* and *Creating and
>   modifying process security sets*.

>   **To set security options for net changes:**

1.  Open the MRP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> MRP)

1.  Mark the Allow Net Change from PAB Inquiry option to allow users to process
    net change regenerations from the MRP Projected Available Balance Inquiry
    window.

2.  Enter or select a security set that can be used to restrict users’ abilities
    to process a net change regeneration. You can limit access by user ID or by
    requiring users to supply a password. This field is available if you mark
    the Allow Net Change from PAB Inquiry option.

3.  Choose OK. You can close the window, or you can continue to enter MRP system
    preferences.

### Restoring MRP quantity labels

>   To use the original MRP labels after you’ve changed them, you can restore
>   the original values.

>   **To restore MRP quantity labels:**

1.  Open the MRP Preference Defaults window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   System Defaults \>\> MRP)

1.  Choose Redefine MRP Labels to open the Redefine MRP Labels window.

2.  Choose Restore Original Values.

3.  Choose OK.

## Part 2: Manufacturing user setup

>   This part of the documentation includes information that will help you set
>   up Manufacturing user preferences. Most of this information will need to be
>   set up only once for each user, but you can refer to this information at
>   other times for instructions on modifying or viewing existing entries.

>   The following information is discussed:

-   *Chapter 7, “Manufacturing basic user setup,”* describes options for setting
    up user preferences. Information about specifying default selections for
    report formats is included.

-   *Chapter 8, “Manufacturing core functions user setup,”* includes information
    about specifying user preferences for Bills of Materials.

-   *Chapter 9, “Manufacturing production functions user setup,”* contains
    information about specifying routing options and manufacturing order
    scheduling options.

-   *Chapter 10, “Manufacturing management functions user setup,”* includes
    information about user preference settings for Engineering Change Management
    and Quality Assurance.

-   *Chapter 11, “Manufacturing planning functions user setup,”* includes
    information about options for Capacity Requirements Planning and Material
    Requirements Planning.

### Chapter 7: Manufacturing basic user setup

>   You can set up preferences to customize some aspects of your Manufacturing
>   system—for instance, what information is displayed in a window or how fields
>   are cleared.

>   User preferences are set on a user-by-user basis. Because of this, users
>   must log into the system with their own user IDs to be able to see their
>   user preferences in effect. User preferences affect only the computer where
>   the login was used.

>   Before you set up user preferences, you must set up system default settings
>   for Manufacturing. Refer to the following documents for more information:

-   *Chapter 1, “Manufacturing basic setup”*

-   *Chapter 3, “Manufacturing core functions setup”*

-   *Chapter 4, “Manufacturing production functions setup”*

-   *Chapter 5, “Manufacturing management functions setup”*

-   *Chapter 6, “Manufacturing planning functions setup”*

>   This information is divided into the following sections:

-   *System administrators and user preferences*

-   *General user preferences for Manufacturing*

-   *Setting up manufacturing-specific preferences*

-   *Setting up INI user settings*

### System administrators and user preferences

>   Access privileges for setting user preferences can vary from user to user.
>   Some users—such as system administrators—might be granted special “system
>   user” privileges so they can set up user preferences both for themselves and
>   for others. Most users, though, will have access privileges to set up only
>   their own user preferences.

>   *If you don’t have access to the user preference windows but want to make
>   changes, contact your system administrator.*

### General user preferences for Manufacturing

>   Manufacturing includes several “general” user preference settings that you
>   can use to access other applications—such as web browsers or graphics
>   applications—and to customize characteristics such as fonts and colors in
>   Manufacturing windows. General user preferences can be grouped into three
>   categories:

>   **Manufacturing-specific user preference settings** These affect options
>   available only for Manufacturing users. Refer to *Setting up
>   manufacturing-specific preferences* for more details.

>   **INI user settings** These allow you to choose the location of other
>   applications that link to Manufacturing data, or that might help you view
>   graphics or multimedia files you’ve attached to your item records. Refer to
>   *Setting up INI user settings* for more details.

##### **Microsoft Dynamics GP user preference settings** 

##### These determine the display characteristics of windows: font styles such as italic or bold, font colors, and so on. Refer to your System User’s Guide (Help \>\> Contents \>\> select Using the System) for more details.

### Setting up manufacturing-specific preferences

>   User preferences are a series of default system settings that are attached
>   to each user ID. After you set up your user preferences, they’ll be active
>   each time you log on.

>   **To set up manufacturing-specific preferences:**

1.  Open the User Preferences window. (Microsoft Dynamics GP menu \>\> Tools
    \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> User)

2.  If you have system user access privileges, enter or select a user ID in the
    Choose User field. If you’re not a system administrator, your user ID
    appears.

3.  In the Systems Options, mark a report option.

>   “Text reports” is the default Microsoft Dynamics GP format for printing
>   reports.

>   Graphic reports have additional graphic features such as shading and
>   borders.

1.  Save the settings.

>   If you’re a system administrator and are setting up preferences for other
>   users, choose OK. The information will be saved and the window will stay
>   open so you can choose another user ID and continue to set up user
>   preferences for other users. Close the window when you’ve finished setting
>   up user preferences.

>   If you aren’t a system administrator, choose OK to save the settings and
>   close the window.

### Setting up INI user settings

>   You must set up Manufacturing INI settings if you plan to use any of the
>   following features:

-   Attaching graphics files to routings or items

-   Attaching multimedia files to routings or items

-   Attaching CAD files to routings or items

>   INI settings are specific to a computer, not to a user. You might want to
>   use different software to view files on different machines. Drafting
>   department employees, for example, might have the full version of the
>   software used to create and modify CAD drawings, while others in the company
>   have versions of the software to only view the drawings.

**To set up INI user settings:**

1.  Open the MFG & HRP Settings window. (Microsoft Dynamics GP menu \>\> Tools
    \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> User \>\> INI
    Settings)

IMAGE – MFGMFG.jpg

![A screenshot of a cell phone Description automatically generated](media/a23d2f092bf1cbd15aaa0433c67349fd.jpg)

>   *You need to specify pathnames only for the features you’ll use in
>   Manufacturing. If your company isn’t attaching graphics files to routings or
>   items, for example, don’t set up the graphics path.*

1.  Enter a path to a CAD application or choose the browse button on the Path to
    CAD App field to find the application you’ll use to view CAD files. This
    application will be used to view all electronic drawings on your computer
    that have a CAD type.

2.  Enter a path to a graphics application or choose the browse button on the
    Path to Graphics App field to find the application you’ll use to view
    graphics.

3.  Enter a path to a multimedia application or choose the browse button on the
    Path to Multimedia App field to find the application you’ll use to view
    multimedia files.

4.  Enter a path to a graphing application or choose the browse button on the
    Path to Graphing App field to find the application you’ll use to graph
    Manufacturing data.

5.  Close the window when you’ve finished specifying the pathnames to save the
    information.

### Chapter 8: Manufacturing core functions user setup

>   Most Manufacturing modules include user preference settings. You can use
>   these settings to customize some aspects of the system—such as what
>   information is displayed in a window or how fields are cleared—on a
>   user-by-user basis.

>   Before you set up user preferences, you must set up system default settings
>   for Manufacturing. Refer to these documents for more information:

-   *Chapter 1, “Manufacturing basic setup”*

-   *Chapter 3, “Manufacturing core functions setup”*

-   *Chapter 4, “Manufacturing production functions setup”*

-   *Chapter 5, “Manufacturing management functions setup”*

-   *Chapter 6, “Manufacturing planning functions setup”*

>   This information is divided into the following sections:

-   *User preference settings*

-   *Setting up bills of materials user preferences*

### User preference settings

>   Because user preferences are linked to the user ID you use to log into the
>   system, user preferences are in effect only when that user is logged into
>   the system, and affect only the computer where the login was used.

>   Most users can change only their own user preferences. System
>   administrators, however, can set user preferences for other users.

### Setting up bills of materials user preferences

>   You can use the BOM Preferences window to select an icon that will be
>   displayed in the tree view of the Bill of Materials Entry window and the
>   Bill of Materials View window. Icons are available to show different
>   information about the components in each bill of materials, such as whether
>   the item is tracked by lot or serial numbers, whether it is a made or
>   purchased item, and so on.

>   You also can use the window to view the systemwide values that have been set
>   up for your company. You can view the date value that is used to calculate
>   component lead time information, and you can view the labels that have been
>   set up for userdefined fields, if any.

**To set up bills of materials user preferences:**

1.  Open the BOM Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>
    Setup \>\> Manufacturing \>\> User Preferences \>\> Bill of Materials)

2.  If you have system administrator privileges, enter or select a user ID. If
    you don’t have system administrator privileges, your own user ID will be
    displayed in the Choose User field, and you can set up preferences for only
    your own login.

3.  Mark the icon to be used in the tree view of the Bill of Materials Entry
    window and the Bill of Materials View window.

4.  Save the settings.

>   If you are a system administrator and are going to set up Bill of Materials
>   preferences for other users, choose Save. The information will be saved and
>   the window will stay open so you can set Bill of Materials user preferences
>   for other users. Close the window when you’ve finished setting user
>   preferences for additional users.

>   If you aren’t a system administrator, choose OK to save your settings and
>   close the window.

### Chapter 9: Manufacturing production functions user setup**

>   Most Manufacturing modules include user preference settings. For production
>   functions modules, you can specify options for entering routing sequence and
>   data collection information.

>   Because user preferences are linked to the user ID needed to log into the
>   system, the preferences are in effect only when that user is logged into the
>   system. User preferences affect only the computer where the login was used.

>   Before you set up user preferences, you must set up system default settings
>   for Manufacturing. Refer to these documents for more information:

-   *Chapter 1, “Manufacturing basic setup”*

-   *Chapter 3, “Manufacturing core functions setup”*

-   *Chapter 4, “Manufacturing production functions setup”*

-   *Chapter 5, “Manufacturing management functions setup”*

-   *Chapter 6, “Manufacturing planning functions setup”*

>   This information is divided into the following sections:

-   *Setting up routing user preferences*

-   *Setting up sequence entry user options*

-   *Setting up spacing and pointer routing options*

-   *Setting up WIP user preferences*

#### Setting up routing user preferences

>   Use the Routing User Preferences window to customize each user’s view of
>   routing information. You can set up options affecting how updates to
>   routings are reflected in related routings. You also can choose sequence
>   entry options for work center opcodes and can set search options and
>   sequence spacing.

>   Sequence entry options control the information that is retrieved when a user
>   accesses data during routing entry.

>   **To set up routing user preferences:**

1.  Open the Routing User Preferences window. (Microsoft Dynamics GP menu \>\>
    Tools \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> Routings)

IMAGE – MFGRUP.jpg

![A screenshot of a cell phone Description automatically generated](media/a2ab0984c7944fade6bb1f40b1e9bb9b.jpg)

1.  If you have system administrator privileges, enter or select a user ID. If
    you don’t have system administrator privileges, your own user ID will be
    displayed in the Choose User field, and you can set up preferences for only
    your own login.

2.  Determine how to update planning routings.

>   **Compare as Number** If all planning routing sequence numbers are numeric,
>   mark Compare as Number.

>   **Confirm Save** To have the message “Are you sure you want to do this?”
>   displayed before planning routings are changed, mark Confirm Save.

1.  Determine if other planning routings should be updated based only on the
    routing name and sequence number.

>   Whether a routing update is applied to other routings is always determined
>   by the routing name and sequence number. The routing name and sequence
>   number must match before a change in one routing sequence is reflected in a
>   sequence in another routing.

-   If you mark Match WC ID, the routing sequence change will be applied to only
    the routing sequences that have the same routing name, sequence number, and
    work center ID.

-   If you don’t mark Match WC ID, all routings that have the same routing name
    and sequence number will be updated, regardless of the work center ID.

1.  Determine if active routings should be updated based only on the routing
    name and sequence number.

>   Whether a routing update is applied to other routings is always determined
>   by the routing name and sequence number. The routing name and sequence
>   number must match before a change in one routing sequence is reflected in a
>   sequence in another routing.

-   If you mark Match WC ID, the routing sequence change will be applied to only
    the routing sequences that have the same routing name, sequence number and
    work center ID.

-   If you don’t mark Match WC ID, all routings that have the same routing name
    and sequence number will be updated, regardless of the work center ID.

1.  Determine how to search your routing records. You can mark either or both
    Search Includes options.

    -   If you mark Item Number, searches of routing records will display only
        those routings that include the item number you specify.

    -   If you mark Routing Name, searches of routing records will display only
        the routing that has the name you specify.

2.  Choose OK.

#### Setting up sequence entry user options

>   To print routing information for use on the production floor, you can set up
>   options to ensure that the information your employees need is included in
>   the reports. Use the Routing User Preferences window to set up routing entry
>   user preferences.

>   **To set up sequence entry user options:**

1.  Open the Routing User Preferences window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   User Preferences \>\> Routings)

1.  If you have system administrator privileges, enter or select a user ID. If
    you don’t have system administrator privileges, your own user ID will be
    displayed in the Choose User field, and you can set up preferences for only
    your own login.

2.  Mark Replace Routing Seq. Descr. with Op Code Description to view operation
    code descriptions rather than routing sequence descriptions.

3.  Mark Append Op Code Description to Routing Notes to add the operation code
    description to the routing notes.

4.  Mark Attach Op Code Notes to Routing Notes to add the operation code notes
    to the routing notes.

5.  Save the settings.

>   If you have system user access privileges and are going to set up routing
>   preferences for other users, choose Save. The information will be saved and
>   the window will stay open so you can set up routing user preferences for
>   other users. Close the window when you’ve finished setting user preferences.

>   If you don’t have system user access privileges, choose OK to save your
>   settings and close the window.

#### Setting up spacing and pointer routing options

>   Use the Routing User Preferences window to set up options for sequence
>   number spacing and to determine if pointer routings can be used in your
>   facility.

>   You can use any numbering spacing, but we recommend using spacing intervals
>   of

>   10 or 100. This makes it easier to insert a new sequence between existing
>   sequences.

>   **To set up spacing and pointer routing options:**

1.  Open the Routing User Preferences window.

>   (Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\>
>   User Preferences \>\> Routings)

1.  Enter a default spacing for routing sequence numbers.

2.  Mark Use Pointer Routings to use pointer routings in your system. You can’t
    mark the Use Pointer Routings option unless the systemwide setting to use
    pointer routings also is marked.

*Refer to Creating a pointer routing in Chapter 5, “Pointer routings,” in the
Manufacturing Production Functions documentation for more information about
pointer routings.*

1.  Choose OK.

#### Setting up WIP user preferences

>   Use the WIP Preferences window to select options to make data entry tasks
>   easier. The options you select will affect how the Data Collection
>   Transactions window works.

>   **To set up WIP user preferences:**

1.  Open the WIP Preferences window.(Microsoft Dynamics GP menu \>\> Tools \>\>
    Setup \>\> Manufacturing \>\> User Preferences \>\> WIP)

2.  If you have system user access privileges, enter or select a user ID in the
    Choose User field. If you aren’t a system administrator, your user ID will
    appear.

3.  Mark options to indicate what should happen when a data collection entry
    record is saved.

>   **Clear MO Number** Clears the MO Number field in the Data Collection window
>   each time you save a data collection record.

>   **Clear Sequence** Clears the Sequence field in the window each time you
>   save a data collection record.

>   **Clear Dates** Clears the Date fields in the window each time you save a
>   data collection record.

>   **Clear Times** Clears the Time fields in the window each time you save a
>   data collection record.

1.  To have the system automatically enter the next sequence in the selected
    routing in the Sequence field, mark the Increment Sequence option.

2.  To have the system always calculate labor costs using the standard labor
    rate, mark Always Use Standard Labor Rate.

3.  Choose OK.

### Chapter 10: Manufacturing management functions user setup

>   Most Manufacturing modules include user preference settings. This document
>   includes information about user preferences for the management functions
>   modules—Quality Assurance, Engineering Change Management and Job Costing.
>   For example, you can specify what kinds of quality assurance records are
>   displayed when you open a Quality Assurance window. You also can specify
>   what constitutes an “old” engineering change order request, and whether you
>   want change requests to be marked as reviewed as soon as you’ve opened them.

>   Because user preferences are linked to the user ID needed to log into the
>   system, the preferences are in effect only when that user is logged into the
>   system. User preferences affect only the computer where the login was used.

>   Before you set up user preferences, you must set up system default settings
>   for Manufacturing. Refer to these documents for more information:

-   *Chapter 1, “Manufacturing basic setup”*

-   *Chapter 3, “Manufacturing core functions setup”*

-   *Chapter 4, “Manufacturing production functions setup”*

-   *Chapter 5, “Manufacturing management functions setup”*

-   *Chapter 6, “Manufacturing planning functions setup”*

>   This information is divided into the following sections:

-   *Setting up engineering change user preferences*

-   *Setting up quality assurance user preferences*

#### Setting up engineering change user preferences

>   You can set up two user preferences in Engineering Change Management. Use
>   the ECM User Preferences window to define an “old” change order—one that is
>   taking longer to go through its approval status than a number of days you
>   specify—and also to indicate whether auto-marking features should be used.

>   These options also are included in the ECM System Preferences window. If the
>   system defaults you set up there are applicable for all users, you can skip
>   this setup step. You need to use the ECM User Preferences window only if
>   users at your company need different definitions for “old” change orders, or
>   if some users will use auto-marking features and others won’t.

>   **To set up engineering change user preferences:**

1.  Open the ECM User Preferences window.(Microsoft Dynamics GP menu \>\> Tools
    \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> ECM)

2.  If you have system user access privileges, enter or select a user ID. If you
    don’t have system administrator privileges, your own user ID will be
    displayed in the User ID field, and you can set up preferences for only your
    own login.

3.  Enter the number of days until changes will be considered old. This value
    will be used to identify aged change orders in the Engineering Change
    Statistics window.

4.  Mark the Auto-mark Routing option if change orders should be marked
    automatically when you review them.

5.  Save the settings.

>   If you are a system administrator and are going to set up ECM preferences
>   for other users, choose Save. The information will be saved and the window
>   will stay open so you can set up ECM user preferences for other users. Close
>   the window when you’ve finished setting up user preferences.

>   If you aren’t a system administrator, choose OK to save your settings and
>   close the window.

#### Setting up quality assurance user preferences

>   You can use the QA User Preferences window to select a default sorting
>   option and to choose which quality assurance records will be displayed when
>   you open the QA Incoming window.

>   These are only default settings. You can select different sorting methods or
>   choose to see different records when you’re using the QA Incoming window.

>   *You must set up quality assurance system settings before you can set up
>   quality assurance user preferences. Refer to Setting up Quality Assurance.*

>   You also can choose to have the Acceptable Quality Level (AQL) table
>   automatically cleared after you save an AQL table record.

>   **To set up quality assurance user preferences:**

1.  Open the QA User Preferences window. (Microsoft Dynamics GP menu \>\> Tools
    \>\> Setup \>\> Manufacturing \>\> User Preferences \>\> QA)

2.  Select the default sorting method for records in the QA Incoming window.
    Choices are PO Number and Receipt Number.

3.  Select the default restriction for records in the QA Incoming window.

>   **All Items** View records for all items that have been received.

>   **QA Required – Show All Receipts** View records for all items requiring
>   incoming inspection that have been received.

>   **QA Required – Restrict by Date** View records for all items requiring
>   incoming inspection that were received on a purchase receipt with a date
>   that is within a range you specify.

>   **QA Completed** View records for all items that have been inspected.

>   *This default restriction will be used each time you open the QA Incoming
>   window. You can switch to other views of the quality assurance records when
>   you’re using the QA Incoming window.*

1.  To automatically clear the AQL (Acceptable Quality Level) table after its
    associated incoming inspection record has been saved, mark Clear AQL table
    after saving.

2.  Save the settings.

>   If you are a system administrator and are going to set up Quality Assurance
>   preferences for other users, choose Save. The information will be saved and
>   the window will stay open so you can set Quality Assurance user preferences
>   for other users. Close the window when you’ve finished setting up user
>   preferences.

>   If you aren’t a system administrator, choose OK to save your settings and
>   close the window.

### Chapter 11: Manufacturing planning functions user setup

>   Most Manufacturing modules include user preference settings. This document
>   includes information about user preferences for the planning functions
>   modules— Sales Forecasting, Master Production Scheduling, Capacity
>   Requirements Planning, and Material Requirements Planning. You can use these
>   settings to customize some aspects of the system—for instance, what
>   information is displayed in a window or how fields are cleared—on a
>   user-by-user basis.

>   Because user preferences are linked to the user ID needed to log into the
>   system, the preferences are in effect only when that user is logged into the
>   system. User preferences affect only the computer where the login was used.

>   Before you set up user preferences, you must set up system default settings
>   for Manufacturing. Refer to these documents for more information:

-   *Chapter 1, “Manufacturing basic setup”*

-   *Chapter 3, “Manufacturing core functions setup”*

-   *Chapter 4, “Manufacturing production functions setup”*

-   *Chapter 5, “Manufacturing management functions setup”*

-   *Chapter 6, “Manufacturing planning functions setup”*

>   This information is divided into the following sections:

-   *Setting up CRP user preferences*

-   *Setting up MRP user preferences*

-   *Restoring MRP default settings*

-   *Setting up request resolution user preferences*

#### Setting up CRP user preferences

>   Capacity Requirements Planning (CRP) user preferences determine how the
>   system displays CRP information accessed with the employee’s user ID. The
>   options you choose will determine what information appears in the windows
>   and in reports generated using CRP.

**To set up CRP user preferences:**

1.  Open the CRP Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>
    Setup \>\> Manufacturing \>\> User Preferences \>\> CRP)

IMAGE – MFGCRP.jpg

![A screenshot of a cell phone Description automatically generated](media/53fda1cff045b06b9fa37fef151f3aef.jpg)

1.  If you have system administrator privileges, select the user ID you want to
    set up preferences for. If you don’t have system administrator privileges,
    your own user ID will be displayed in the Choose User field, and you can set
    up preferences for only your own login.

2.  Select a default work center.

>   This selection will determine which work center’s information is displayed
>   first when you open CRP windows. You can still see information for other
>   work centers—this will just be the first displayed.

1.  Select a default bucket size. The bucket size determines how the information
    will be summarized in the CRP/MO Detail window. If you set this user
    preference to 2 Weeks, for example, then information in the CRP/MO Detail
    window will reflect the totals of capacity for two weeks at a time. To see
    the information in other bucket sizes, you can adjust the bucket sizes in
    the CRP/ MO Detail window.

2.  Select a default sorting method to determine how information is sorted when
    you use CRP windows. Sorting options include the following:

>   *The option you choose here is only a default setting. You can use sorting
>   options in CRP module windows to see information in other orders.*

>   **By Work Center** View CRP information sorted by the work center IDs.

##### **By Released Employee Load Percent** View CRP work center

>   information sorted by the percentage of employee load each work center
>   carries for firm manufacturing orders.

>   **By Released Machine Load Percent** View CRP work center information sorted
>   by the percentage of machine load each work center carries for manufacturing
>   orders with Released status.

>   **By + Open Employee Load Percent** View CRP work center information sorted
>   by the percentage of employee load each work center carries for
>   manufacturing orders with Released or Open status.

>   **By + Open Machine Load Percent** Select this option to see CRP work center
>   information sorted by the percentage of machine load each work center
>   carries for manufacturing orders with Released or Open status.

1.  Select the number of decimal places to be displayed for numeric fields in
    CRP.

2.  Mark Show Outsourced Work Centers to include CRP information for work
    centers that are not part of your plant.

>   For example, you might have a contract with another firm to paint the farm
>   machinery produced by your company. Your contract with the painting
>   contractor might specify how much capacity the contractor reserves for you.
>   To track use of that capacity, you can mark this option.

1.  Mark Expanded Windows if scrolling windows in the CRP module should open in
    an expanded view.

>   *This is just a default setting. You can change the view in the scrolling
>   windows when you’re using other CRP windows.*

1.  Save the settings.

>   If you are a system administrator and are going to set up CRP preferences
>   for other users, choose Save. The information will be saved and the window
>   will stay open so you can set up CRP user preferences for other users. Close
>   the window when you’ve finished setting up user preferences.

>   If you aren’t a system administrator, choose OK to save your settings and
>   close the window.

#### Setting up MRP user preferences

>   Use the MRP Preferences window to set up general Material Requirements
>   Planning (MRP) options and to select fields for windows and reports in MRP
>   system. All the user preferences you set up in this window are on a
>   user-by-user basis and the settings will override systemwide default
>   preferences.

>   Refer to *Setting up general MRP options* for more details about these MRP
>   system default settings.

>   **To set up MRP user preferences:**

1.  Open the MRP Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>
    Setup \>\> Manufacturing \>\> User Preferences \>\> MRP)

2.  If you have system administrator privileges, enter or select a user ID. If
    you don’t have system administrator privileges, your own user ID will be
    displayed in the Choose User field, and you can set up preferences for only
    your own login.

3.  Set up general MRP options.

    -   To view items, sites, and item-site combinations that have been excluded
        from MRP calculations or that have no activity, mark Show Items with no
        Activity. This option will be available only if the option to show
        inactive items is marked in the MRP Preference Defaults window.

    -   To see a status window when MRP information is being regenerated, mark
        the Show Status Window option.

    -   Select the default bucket size for your views in MRP windows. Choices
        are Days, Weeks and Months.

4.  Select up to six MRP quantities to see when using MRP windows.

>   These fields will be displayed in windows and reports in the order in which
>   they are displayed in this window. If the first field displayed should be
>   Required Planned, select Required Planned for the first (top) list.

>   Refer to *MRP quantities* in *Chapter 8, “MRP overview,”* in the
>   Manufacturing Planning Functions documentation for more information about
>   how the quantities are calculated.

>   *If new labels have been applied to the MRP quantities at your company, the
>   new labels will be displayed in the lists. To see a cross-reference between
>   the Manufacturing labels and those created by your company, choose MRP Label
>   Cross-Reference. Any references to those quantities in documentation will be
>   by the original Manufacturing labels.*

1.  Choose OK and close the window.

#### Restoring MRP default settings

>   You can use the MRP Preferences window to remove the user-defined MRP
>   preference settings you’ve selected. Completing this procedure will make the
>   user preferences for the selected user ID identical to the systemwide
>   default settings.

**To restore MRP default settings:**

1.  Open the MRP Preferences window. (Microsoft Dynamics GP menu \>\> Tools \>\>
    Setup \>\> Manufacturing \>\> User Preferences \>\> MRP)

2.  If you have system administrator privileges, enter or select a user ID. If
    you don’t have system administrator privileges, your own user ID will be
    displayed in the Choose User field, and you can set up preferences for only
    your own login.

3.  Choose Reset to System Defaults.

4.  Choose OK and close the window.

#### Setting up request resolution user preferences

>   If you’re using MRP, each user with purchase order entry responsibilities
>   will need to set up user preferences for using primary suppliers.

>   **To set up request resolution user preferences:**

1.  Open the Purchase Request Resolution User Preferences window.

(Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> Manufacturing \>\> User

>   Preferences \>\> Request Resolution)

>   *You also can open this window through the Purchase Request Resolution
>   window. Choose the Go To button and select Req. Resolution Preferences.*

1.  To automatically select the primary supplier of an item for auto-generated
    purchase orders, mark Automatically use primary vendor on item selection.

2.  Choose OK and close the window.


#### Accounts Used for Manufacturing in Microsoft Dynamics GP

**Manufacturing Inventory and General Ledger Transactions General**

**Where to set up Manufacturing Accounts**

Account numbers for both actual and standard cost items and are set in the Item Account Maintenance window. To open the Item Account Maintenance window go to Cards> Inventory > Item and then click the Account button.  Two windows will open:  
1) Item Account Maintenance 
2) Item Account Maintenance –Costing
The top window is the core accounts for Great Plains for Items.  The 2nd window below the Item Account Maintenance window is for Manufacturing.  This is the Item Account Maintenance – Costing window.

**What Accounts need to be setup for Manufacturing**
This is dependent on the type of costing used.
Actual Costing Accounts
Accounts that are used for actual cost item transactions in manufacturing are:
•	Inventory (for most transaction)
•	Inventory Offset (for inventory adjustments, receiving)
•	Cost Of Goods Sold (for sales invoices)
•	Sales Returns (for sales returns)
•	WIP (for MO close of issued/back flushed components of made items)
•	Variance Material (for potential labor, machine and material variances)

Standard Costing Accounts
Account Numbers for standard cost items are set in the Item Account Maintenance Costing window (Figure 2).  Accounts that are used for standard cost item transaction in manufacturing are:
•	Standard Cost Revaluation Account (for standard cost revaluation function)
•	Applied – Material overhead Accounts (for receiving – BUY items)
•	Variance Accounts (for variances during MO Close – MAKE items)
•	WIP Accounts (for issue/backflush of materials- MAKE items)
•	COGS Accounts (for sales invoices – sold items)
•	Inventory Accounts (for inventory adjustments, transfers, issue of materials, MO close – all items)

Accounts Required for both Actual and Standard Costing Items
Additional accounts necessary for both actual and standard costing are the labor and machine setup accounts, the rounding difference account, and the accrued purchases account.
•	Labor applied accounts can be set in the Labor Code Definition window.  To open the window go to Cards > Manufacturing > Labor Codes.
•	Machine applied accounts can be set in the Machine Definition window. To open the window go to Cards > Manufacturing > Machines.
•	The Rounding Difference account can be set in the Costing Preference Defaults window.  To open the window go to Tool > Setup > Manufacturing > System Defaults > Costing.
•	Accrued Purchases account can be set under the Vendor Account Maintenance window. To open the window go to Cards > Purchasing > Vendor > Account.

**How will the Cost be Determined**
Actual items cost used
Actual cost items have a perpetual valuation method.  The last cost received for an item can be found in the Current Cost field on the Item Maintenance window. To open the Item Maintenance window go to Cards > Inventory > Item.  The actual costs will be used when items are removed from inventory. The actual costs for each item are located in the Purchase receipts table (IV10200).  You can view these costs by printing the Purchase Receipts report under Report > Inventory > Activity > Purchase Receipts (Figure 2).  The costs that the system will use are based on the Perpetual valuation method selected (FIFO vs. LIFO) and will it will pull out the cost of the IV Purchase receipts table when posted.

Standard cost items cost used 
Standard Cost items have a periodic valuation method.  The “total” cost for these types of items can be found in the Standard Cost field in the Item Maintenance window.  The “broken out” costs for these types of items can be found on the Standard Cost changes window located under Cards > Manufacturing > Inventory > Standard Cost Changes.    The “broken out” costs are used for the GL transactions of standard cost items.  The “broken out’ costs are:
•	Material
•	Material Fixed Overhead
•	Material Variable Overhead
•	Labor
•	Labor Fixed Overhead
•	Labor Variable Overhead
•	Machine
•	Machine Fixed Overhead
•	Machine Variable Overhead

**General Ledger Transactions**
General Ledger transactions are created in many areas of manufacturing and also from inventory transaction in Great Plains.  Listed below are the areas where the transactions originated and also detailed information about the transaction.  This information includes what accounts are used, where the accounts are pulled from and what costs are used for the transaction.

Inventory Adjustment
Transactions > Inventory > Transaction Entry
Audit Trail Code example: IVADJ0000000000123

Actual Cost Items

Actual Cost Item Accounts and Costs during Inventory Adjustments

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory (Item Account Maintenance)       | Current Cost       |
| CR        | Inventory Offset(Item Account Maintenance) | Current Cost       |


Example of Accounts and Costs used during an Inventory Adjustment for an actual BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.00              |
| CR        | Inventory Offset                           | $4.00              |

Example of Accounts and Costs used during an Inventory Adjustment for an actual MAKE item	

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $5.56              |
| CR        | Inventory Offset                           | $5.56              |

Standard Cost Items
Standard Cost Item Accounts and Costs during an Inventory Adjustment  

| **DR/CR** | **Account**                                | **Cost Used**                  |
|-----------|--------------------------------------------|------------------------------  |
| DR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| DR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| DR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| DR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| DR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| DR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| DR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| CR        | Inventory Offset(Item Acct Maintenance)    | Total Standard Cost            |
| DR/CR     | Rounding Account(Cost Preferences Default) | Rounding Difference            |

Example of Accounts and Costs used during an Inventory Adjustment for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $3.35              |
| DR        | Inventory – Material Fixed Overhead        | $ .50              |
| DR        | Inventory – Material Variable Overhead     | $ .15              |
| CR        | Inventory Offset                           | $4.00              |

Example of Accounts and Costs used for an Inventory Adjustment for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.10              |
| DR        | Inventory – Material Fixed Overhead        | $ .55              |
| DR        | Inventory – Material Variable Overhead     | $ .35              |
| DR        | Inventory – Labor                          | $ .27              |
| DR        | Inventory – Labor Fixed Overhead           | $ .02              |
| DR        | Inventory – Labor Variable Overhead        | $ .01              |
| DR        | Inventory – Machine                        | $ .43              |
| DR        | Inventory – Machine Fixed Overhead         | $ .10              |
| DR        | Inventory – Machine Variable Overhead      | $ .12              |
| CR        | Inventory Offset                           | $5.95              |


Inventory Transfer
Transactions -> Inventory -> Transfer Entry
Audit Trail Code example: IVFR000000123

Actual Cost Items

Actual Cost item Accounts and Costs used during an Inventory Transfer 

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory (Item Account Maintenance)       | Current Cost       |
| CR        | Inventory (Item Account Maintenance)       | Current Cost       |

Example of Accounts and Costs used during an Inventory Transfer for an actual cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.00              |
| CR        | Inventory                                  | $4.00              |

Example of Accounts and Costs used during an Inventory Transfer for an actual cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $5.95              |
| CR        | Inventory                                  | $5.95              |

Standard Cost Items
Standard Cost Item Accounts and Costs used for Standard Cost items during an Item Transfer 

| **DR/CR** | **Account**                                | **Cost Used**                  |
|-----------|--------------------------------------------|------------------------------  |
| DR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| DR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| DR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| DR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| DR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| DR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| DR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| CR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| CR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| CR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| CR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| CR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| CR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| CR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| CR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| CR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| DR/CR     | Rounding Diff   (Cost Preferences Default) | Rounding Difference            |

Example of Accounts and Costs used during Item Transfer for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $3.35              |
| DR        | Inventory – Material Fixed Overhead        | $ .50              |
| DR        | Inventory – Material Variable Overhead     | $ .15              |
| CR        | Inventory                                  | $3.35              |
| CR        | Inventory – Material Fixed Overhead        | $ .50              |
| CR        | Inventory – Material Variable Overhead     | $ .15              |

Example of Accounts and Costs used during Item Transfer for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory                                  | $4.10              |
| DR        | Inventory – Material Fixed Overhead        | $ .55              |
| DR        | Inventory – Material Variable Overhead     | $ .35              |
| DR        | Inventory – Labor                          | $ .27              |
| DR        | Inventory – Labor Fixed Overhead           | $ .02              |
| DR        | Inventory – Labor Variable Overhead        | $ .01              |
| DR        | Inventory – Machine                        | $ .43              |
| DR        | Inventory – Machine Fixed Overhead         | $ .10              |
| DR        | Inventory – Machine Variable Overhead      | $ .12              |
| CR        | Inventory                                  | $4.10              |
| CR        | Inventory – Material Fixed Overhead        | $ .55              |
| CR        | Inventory – Material Variable Overhead     | $ .35              |
| CR        | Inventory – Labor                          | $ .27              |
| CR        | Inventory – Labor Fixed Overhead           | $ .02              |
| CR        | Inventory – Labor Variable Overhead        | $ .01              |
| CR        | Inventory – Machine                        | $ .43              |
| CR        | Inventory – Machine Fixed Overhead         | $ .10              |
| CR        | Inventory – Machine Variable Overhead      | $ .12              |

Receiving Material Only in Purchase Order Processing
Transactions > Purchasing > Receivings Transaction Entry
Audit Trail Code example: RECVG000000123

Actual Cost items
Actual Cost Item Accounts and Costs used for during Receivings Transaction 

| **DR/CR** | **Account**                                | **Cost Used**                         |
|-----------|--------------------------------------------|---------------------------------------|
| DR        | Inventory (Item Account Maintenance)       | Receiving Cost (Item Vendor Maint.)   |
| CR        | Accrued Purchases(Vendor Acct Maint)       | Receiving Cost                        |


Example of Accounts and Costs used during a Receivings Transaction for an actual cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**   |
|-----------|--------------------------------------------|-----------------|
| DR        | Inventory (Item Account Maintenance)       | $4.32           |
| CR        | Accrued Purchases(Vendor Acct Maint)       | $4.32           |

Example of Accounts and Cost used during a Receivings Transaction for an actual cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**   |
|-----------|--------------------------------------------|-----------------|
| DR        | Inventory (Item Account Maintenance)       | $6.43           |
| CR        | Accrued Purchases(Vendor Acct Maint)       | $6.43           |

Standard Cost Items
Accounts and Cost used for Standard Cost item during Receivings Transaction 

| **DR/CR** | **Account**                                | **Cost Used**                  |
|-----------|--------------------------------------------|------------------------------  |
| DR        | Inventory (Item Account Maintenance)       | Material Cost                  |
| DR        | Inventory – Material Fixed Overhead        | Material Fixed Overhead Cost   |
| DR        | Inventory – Material Variable Overhead     | Material Variable Overhead Cost|
| DR        | Inventory – Labor(Item Acct Maint-Costing) | Labor Cost                     |
| DR        | Inventory – Labor Fixed Overhead           | Labor Fixed Overhead Cost      |
| DR        | Inventory – Labor Variable Overhead        | Labor Variable Overhead Cost   |
| DR        | Inventory – Machine(Item Acct Maint-Cost)  | Machine Cost                   |
| DR        | Inventory – Machine Fixed Overhead         | Machine Fixed Overhead Cost    |
| DR        | Inventory – Machine Variable Overhead      | Machine Variable Overhead Cost |
| DR/CR     | Unrealized PPV (Item Account Maintenance)  | Receiving Cost –Material Cost  |
| CR        | Accrued Purchases (Vendor Account Maint)   | Receiving Cost                 |
| CR        | Applied – Material Fixed Overhead          | Material Fixed Overhead Cost   |
| CR        | Applied – Material Variable Overhead       | Material Variable Overhead Cost|
| CR        | Applied – Labor (Labor Code Definitions )  | Labor Cost                     |
| CR        | Applied – Labor Fixed Overhead             | Labor Fixed Overhead Cost      |
| CR        | Applied – Labor Variable Overhead          | Labor Variable Overhead Cost   |
| CR        | Applied – Machine (Machine Definitions)    | Machine Cost                   |
| CR        | Applied – Machine Fixed Overhead           | Machine Fixed Overhead Cost    |
| CR        | Applied – Machine Variable Overhead        | Machine Variable Overhead Cost |

Example of Item Accounts and Costs used during a Receivings Transaction for a standard cost BUY item

| **DR/CR** | **Account**                                | **Cost Used**       |
|-----------|--------------------------------------------|-------------------- |
| DR        | Inventory                                  | $3.35               |
| DR        | Inventory – Material Fixed Overhead        | $ .50               |
| DR        | Inventory – Material Variable Overhead     | $ .15               |
| DR/CR     | Unrealized PPV                             | $4.32 – $3.35 = $.97|
| CR        | Accrued Purchase                           | $4.32               |
| CR        | Applied – Material Fixed Overhead          | $ .50               |
| DR        | Applied – Material Variable Overhead       | $ .15               |

Example of Accounts and Costs used during a Receivings Transaction for a standard cost MAKE item

| **DR/CR** | **Account**                                | **Cost Used**       |
|-----------|--------------------------------------------|-------------------- |
| DR        | Inventory                                  | $5.05               |
| DR        | Inventory – Material Fixed Overhead        | $ .55               |
| DR        | Inventory – Material Variable Overhead     | $ .35               |
| DR        | Inventory – Labor                          | $ 5.00              |
| DR/CR     | Unrealized PPV                             | $6.43 –$5.05= $1.38 |
| CR        | Accrued Purchase                           | $6.43               |
| CR        | Applied – Labor                            | $ 5.00              |
| CR        | Applied – Material Fixed Overhead          | $ .55               |
| DR        | Applied – Material Variable Overhead       | $ .35               |


Enter/Match Invoice for Purchase Order
Transactions > Purchasing > Enter/Match Invoice
Audit Trail Code example: POINV000000123

Actual Cost Items
Actual Cost Item Accounts and Cost during Enter/Match Invoice (Invoicing)

| **DR/CR** | **Account**                                | **Cost Used**      |
|-----------|--------------------------------------------|--------------------|
| DR        | Inventory (Item Account Maintenance)       | Current Cost       |
| CR        | Inventory (Item Account Maintenance)       | Current Cost       |




**Glossary**

**Acceptable Quality Level table**

A representation of testing standards and sample sizes. AQL tables include information about appropriate sample sizes and the maximum number of pieces that can fail inspection in an acceptable lot. You’ll probably set upseveral AQL tables to reflect different inspection standards for different 
items.

**Active routing**
*See Manufacturing order routing*.

**Actual costing**
An inventory tracking method that involves constantly updating inventoryeach time an item is added or removed.
 
**Actual demand**
The total quantity of an item requested on all firm manufacturing orders.

**Actual expenses (Job Costing)**

The total of all applied expense transactions linked to a job.

**Actual margin (Job Costing)**
A measure of the overall profitability of a specific job. The actual margin for a job is calculated by dividing the actual profit by the actual revenue, and then multiplying the result by 100.

**Actual profit (Job Costing)**
The difference between actual expenses and actual revenues for a job.

**Actual revenues**
The total of all applied revenue transactions linked to a job.

**Allocate**
To reserve materials needed for a manufacturing order.

**Alternate routing**
Any planning routing for an item other than the primary routing.

**Alternate work center**
A work center to which work can be shifted if the customary work center for a specific task is not available. If the primary work center is temporarily shut down, or if demand exceeds the capacity of the primary work center, the work load can be shifted to the alternate work center.

**Apply**
To add the amount of a revenue or expense linked to a job to the financial information about the job. If a transaction isn't applied to a job, its amount won't be reflected in the overall financial information about the job. Applying transactions in Job Costing can happen manually or automatically.

**AQL table**
*See Acceptable Quality Level table*.

**ARCH BOM**
*See Archived bill of materials*.

**Archived bill of materials**
A bill of materials stored in a separate area of your computer system. Bills of material might be archived as they become obsolete.

**Assemble to order**
A type of manufacturing facility that puts a group of components together according to customer specifications.

**Back order**
An order to be fulfilled when stock for items in shortage is replenished.

**Backflushing** 
A method of accounting for the use of resources—labor and machine time, and items—based on standards you’ve defined. Transactions to account for the use of backflushed resources are created when a manufacturing order is closed.

**Backward finite scheduling**
A scheduling method that starts from a due date and works out a plan for the flow of work through the plant with the assumption that there are only a limited number of resources (machines and workers) available to complete the task.

**Backward infinite scheduling**

>   A scheduling method that starts from a due date and works out a plan for the
>   flow of work through the plant with the assumption that the plant has
>   unlimited machine and worker capacity.

**Batch cards**

>   *See Manufacturing order*.

**Bill of materials**

>   A list of the components and subassemblies needed to build one unit of a
>   product. The bill of materials also shows quantities for each component.

**Bill of operations**

>   *See Routing*.

**Bin**

>   A storage device to hold discrete items.

**Blanket purchase order**

>   A purchase order that is delivered gradually to the buyer.

**Bucket**

>   A time period used for calculating MRP requirements. Manufacturing supports
>   daily, weekly, and monthly bucketing options.

**Buy items**

>   Items that are supplied to your plant by a supplier.

**Buyer ID**

>   Code that identifies the person who purchases the item from a supplier.

**By-product**

>   A finished good that is created incidentally to another finished good.

**Child part** *See Component*.

**Class**

>   A method for grouping similar parts or products.

**Co-product**

>   *See By-product*.

**Company data**

>   Company data is the information you enter about your organization, such as
>   its applicants, employees, benefits systems, training programs, and
>   organizational structure.

**Component**

>   Items used to build a product. Component parts can be items (nuts, screws,
>   diodes) or subassemblies (axles, circuit boards).

**Component transaction**

>   A line on a pick document to allocate, reverse allocate, issue, reverse
>   issue, scrap, or reverse scrap components for a manufacturing order.

**CONFIG BOM**

>   *See Configured bill of materials*.

**Configuration data**

>   In Bill of Materials, information about the product’s overall design. It
>   includes the design authority for the product, the unit of measure, and the
>   revision level.

**Configured bill of materials**

>   A bill of materials that is built by selecting options from a super bill of
>   materials.

**Configured cost**

>   The calculated cost of building a specific configured item, depending on the
>   options a customer selects. The configured cost reflects the cost of the
>   component items and the labor required to manufacture the item.

**Configured price**

>   The suggested price to charge the customer for a configured item, based on
>   your finished goods price schedule and the selected options.

**Configured routing**

>   A routing based on the selected options. For example, if you created a
>   configured bill of materials for office chairs and chose plastic components
>   rather than wooden ones, the routing would be modified to exclude the
>   sequences for staining and varnishing the wooden components. Also known as a
>   “configured working routing.”

**Configured Working Routing**

>   *See Configured routing*.

**Consume**

>   To use up the quantity that has been issued to WIP—for materials, labor
>   time, or machine time—for a manufacturing order.

**Cost variance**

>   The difference between the actual costs—for materials, machine time and
>   labor—and the estimated costs for a manufacturing order.

>   Cost variances can be positive or negative.

**Customer record**

>   A record that shows all the information you need to conduct sales
>   transactions, such as address information, billing and shipping
>   instructions, credit history and other data for that customer.

**Cycle time**

>   The total amount of time it takes to make one part, such as setup time,
>   labor time, machine time, queue time and move time.

**Default inventory site**

>   The location commonly used to store raw materials or finished goods.

**Defect code**

>   An identifier for a particular type of item failure. For example, if an item
>   is too long and fails a specification for length, you might create a defect
>   code called LENGTH. Defect codes are used in Manufacturing reports to help
>   summarize information.

**Denial code**

>   An identifier for the reason why an engineering change request wasn’t
>   approved.

**Destination routing**

>   A routing that you copy from another routing. You can add sequences to the
>   destination routing.

**Direct labor**

>   The time spent by one or more production workers on filling a specific
>   manufacturing order.

**Discrete item**

>   An item that is manufactured as a distinct unit. Examples of discrete items
>   include computers, automobiles, and radios.

**Disposition code**

>   An identifier for a method for handling defective items. For example, you
>   might decide to scrap certain defective items, and might assign a SCRAP
>   disposition code to those items.

**Double-booking**

>   A situation where a job might inadvertently be charged twice for the same
>   expense.

**Down day**

>   A day when the facility—the entire shop floor or a specific work center—is
>   not in production.

**Drawing**

>   A schematic or other illustration. You can

>   “attach” electronic drawing files—such as CAD illustrations, bitmaps and
>   even .AVI movies—to records.

**Drawing group**

>   A set of related drawing files. For example, a drawing group might include
>   several views of the same item.

**Due date**

>   The date when the items on a sales order should be ready to ship.

**ECM**

>   *See Engineering change management (ECM)*.

**ECO**

>   *See Engineering change order (ECO)*.

**ECR**

>   *See Engineering change request (ECR)*.

**Either item**

>   Item that can be bought or manufactured by your company.

**Element**

>   An order or transaction that can be linked to a job, such as a manufacturing
>   order, a sales order, a purchase order line, a receiving line, or inventory
>   transaction.

**Employee allocation**

>   The assignment of workers to work areas. Each employee can be assigned an
>   efficiency rating for a particular task. The number of hours per shift spent
>   on a task can also be specified. Total scheduled employee hours for the work
>   center are also displayed.

**Employee efficiency percentage**

>   A ranking of how an employee performs a given task. You can use this field
>   different ways, depending on how your organization handles its employee
>   efficiencies. Some organizations complete time studies of various tasks, and
>   set task goals for workers based on those figures. Employees earn efficiency
>   ratings based on their ability to meet those criteria. In other
>   organizations, the top producer is assigned a value of 100% (or less) and
>   all other employees would be ranked in comparison to the top producer.

**ENG BOM**

>   *See Engineering bill of materials*.

**Engineering bill of materials**

>   A proposed bill of materials. Designs that are only in the prototype stage
>   of development, for example, may have engineering bills of materials. In
>   this way, the costs of producing a design can be studied without impacting
>   the material requirements that the system generates.

**Engineering change management (ECM)**

>   The systems that a company has in place to ensure that changes to its
>   product specifications are properly monitored.

**Engineering change order (ECO)**

>   The second stage of the engineering change management process. An
>   engineering change order is a change that has been approved for
>   incorporation.

**Engineering change request (ECR)**

>   The proposal stage of the engineering change management process. An
>   engineering change request is a proposed change.

**Estimated expense**

>   A projection of the expenses for a job, entered in the Job Maintenance
>   window.

**Estimated margin**

>   A job costing calculation based on estimated revenues and estimated expenses
>   for a specific job. The estimated margin is calculated by dividing the
>   estimated profit by the estimated revenues, and the multiplying the result
>   by 100.

**Estimated profit**

>   The difference between the estimated expenses and the estimated revenues for
>   a specific job.

**Estimated revenue**

>   A projection of the revenues for a job, entered in the Job Maintenance
>   window.

**Exclusions (MRP)**

>   A method of marking an item, site or itemsite combination so it isn’t
>   included in MRP calculations.

**Exclusions (Sales Configurator)**

>   Options that are disallowed because of another option selection.

**Expensed floor stock**

>   A bill of materials component that has been designated—regardless of its
>   issue-to and issue-from sites—as a floor stock item. The cost of expensed
>   floor stock is applied to an expense account, rather than to the cost of the
>   finished item. *See also Floor stock*.

**Explode**

>   To determine the total quantities of components needed for a manufactured
>   item. To explode a bill of materials, the quantity ordered is multiplied by
>   the quantity used for each of its components. Exploding continues throughout
>   the bill of materials, so component requirements for subassemblies are also
>   calculated.

**Filled order**

>   An order that has had all its requirements met and can be closed.

**Finished goods**

>   An item that is manufactured for sale. Also, the final products that a
>   company sells.

**Finite scheduling**

>   A scheduling method that assumes that limited capacity for labor and
>   machines is available.

**Fixed order quantity**

>   An order policy type that calculates order size for a day’s requirements
>   based on one or more of these variables: standard order quantity, order
>   increment size, minimum order size, and maximum order size.

**Fixed quantity**

>   The quantity of a component that is required for each manufacturing order,
>   regardless of how many finished goods are produced with the order. For
>   example, if you use two widgets to calibrate equipment each time you begin a
>   new manufacturing order, the fixed quantity for widgets would be 2 for the
>   finished good bill of materials.

**Floor stock**

>   A bill of materials component that uses the same site for its issue-from and
>   issue-to sites. The cost of this type of floor stock is applied to the cost
>   of the finished item. *See also Expensed floor stock*.

**Forecasted demand**

>   An estimate of how much of an item should be produced over a specific period
>   of time.

**Forward infinite scheduling**

>   A scheduling type based on a starting date for an order, with the assumption
>   that the plant has unlimited machine and worker capacity for the work order.

**Full regeneration**

>   An MRP process that recalculates your MRP data, including all sales orders,
>   purchase orders, sales forecasts, and manufacturing orders. *See Net change
>   regeneration*.

**Functional currency**

>   The currency type (such as dollars or pounds) used by your organization for
>   its accounting. *See also Originating currency*.

**General ledger variance**

>   The difference between costs that have been added to WIP and the costs that
>   have been removed from WIP for a specific manufacturing order.

**Header record**

>   The information that ties the pieces of a larger record together. For
>   example, the header record of a routing includes information about the type
>   of routing, the routing name, the date the routing was created and so on.
>   This information ties sequence records together to create one routing
>   record.

**Hours per shift**

>   The amount of time per shift actually spent working on the assigned tasks.
>   To determine hours available per shift, subtract any nontask related
>   activities from the total number of available hours. For example, if an
>   employee is scheduled for an eight-hour shift but has a one-hour meeting and
>   two quarter-hour breaks that day, the total available time would be 6.5
>   hours.

**Inclusions**

>   Option items automatically added to a configured bill of materials when a
>   customer selects a certain option. For example, a computer manufacturer
>   might offer a computer system in tan and black. If the customer selects the
>   option for a tan computer, the computer manufacturer might set up the super
>   bill of materials so that the tan keyboard automatically is included as part
>   of the purchase.

**Indirect labor**

>   The time spent on tasks that are not directly related to filling a specific
>   manufacturing order. Examples of indirect labor include meetings and
>   training.

**Instruction sheet**

>   *See Routing*.

**Infinite scheduling**

>   A scheduling method that assumes that all required capacity for labor and
>   machines is always available.

**Invoice history**

>   The information tracked about past invoices. Invoice history allows you to
>   determine what historical information you will need for tracking sales
>   activity. History information can include transaction detail and/or account
>   distributions.

**Issue**

>   A type of component transaction. When components are issued for a
>   manufacturing order, they are removed from inventory and added to WIP.

**Issue-from location**

>   The site where the components used in the manufacturing process are stored
>   prior to beginning the manufacturing order, such as with a vendor, or in a
>   department, a warehouse, or another plant.

**Issue-to location**

>   The site where the finished product will be stored prior to delivery to the
>   customer, such as in a department, a warehouse, or another plant.

**Item type**

>   A code to designate the accounting class for the item, such as inventory,
>   discontinued, and misc. charge.

**Item-specific inventory valuation**

>   An accounting method that places a value on each item that you produce,
>   based upon either standard cost or current cost.

**Job**

>   A series of business activities that, when completed, will fulfill a
>   high-level objective.

**Job category**

>   Groupings that you can create to organize the titles and descriptions of
>   jobs within your company. Each job category must include a set of values
>   that can be used to sort all jobs. For example, you might create a job
>   category called REGION so you could track jobs from specific geographical
>   areas. Values for that job category might be East, West, North and South-or
>   might be states, provinces, countries/regions or other areas.

**Job costing element**

>   A type of element that can be linked to a job.

**Job costing transaction**

>   An instance of a job element that is linked to a specific job, capturing
>   information about a specific revenue or expense associated with the job. Job
>   costing transactions aren’t accounting transactions: they won’t affect the
>   General Ledger or any subsidiary ledgers.

**Job order**

>   *See Manufacturing order*.

**Job transaction list**

>   A selection of transactions to be applied to a specific job. You can use
>   transaction lists to specify the kinds of transactions that should be
>   applied to jobs, and to specify the transactions to be applied automatically
>   to jobs.

**Kit**

>   A group of finished items that compose a set.

**Labor code**

>   A code that is used to tie a job function to a specific pay grade. Usually,
>   jobs requiring fewer skills have lower pay grades and are compensated at
>   lower rates. Jobs requiring more skills or education have higher pay grades
>   and higher pay rates.

**Labor time**

>   The number of employee hours required to complete the operation.

**Lead time**

>   The minimum amount of time required for production of an item.

**Location**

>   A work site. Some businesses are organized as a single company or division,
>   but may have multiple sites.

**Lot-for-lot**

>   An order policy for ordering the exact quantity needed, provided that the
>   order quantity is between the minimum and maximum order quantities.

**Lot-numbered item**

>   Any inventoried item that is part of a group that is assigned a unique
>   identifier, which can be letters, numbers or a combination of letters and
>   numbers.

**Lot-number–tracked item**

>   *See Lot-numbered item*.

**Lot-sample size**

>   The number of item units that should be inspected to determine if a group of
>   items meets specifications.

**Lot-tracked item**

>   *See Lot-number–tracked item*.

**Low-level code**

>   A code that identifies the deepest level an item has in any bill of
>   materials in your manufacturing records.

**Machine**

>   Any tool, device or implement that you use in your manufacturing process.

**Machine allocation**

>   The assignment of a machine to a work area. Each allocation record displays
>   available machine hours, the efficiency rating, and utilization rate for
>   that machine. Total scheduled machine hours for the work center are also
>   displayed.

**Machine definition**

>   The record of a machine in your plant that allows you to track statistics
>   for each machine, including vendor information, warranty period, and
>   operating costs.

**Machine efficiency**

>   A measure of how a machine is suited for a specific task. The higher the
>   efficiency rating, the more effectively the machine works.

**Machine time**

>   The number of machine hours needed to complete the operation.

**Machine utilization**

>   A measure of how much of the available machine capacity is actually being
>   used. For example, if a machine is capable of producing 100 items per
>   eight-hour day and you are only producing 80 items, the machine utilization
>   rate is 80 percent.

**Make item**

>   An item that is produced by your plant.

**Make or Buy item**

>   Item that can be bought or manufactured by your company.

**Make to order**

>   An order fulfillment method for made items. When make-to-order items are
>   sold, manufacturing orders to build the items required to fulfill the
>   manufacturing orders are created. Manufacturing orders are used to respond
>   to specific sales orders.

**Make to stock**

>   An order fulfillment method for made items. When make-to-stock items are
>   sold, the quantities required to fulfill the sales order are taken from
>   inventory quantities. Manufacturing orders are used to keep inventory levels
>   up so that sales orders can be fulfilled.

**Manufacturing bill of materials**

>   The bill of materials used to build a parent part in your organization. A
>   manufacturing bill of materials is the “real” bill of materials, and is used
>   to figure material requirements for your organization.

**Manufacturing data sheets**

>   *See Routing*.

**Manufacturing order**

>   A set of documents conveying the authority to manufacture parts or products
>   in specified quantities. Manufacturing orders are also called batch cards,
>   job orders, production orders, run orders, shop orders, or work orders.

**Manufacturing order receipt**

>   A document where material, labor, and machine costs in WIP are applied to
>   finished goods that are received in inventory. Costs for backflushed
>   materials, labor, and machine time also are applied to the finished goods
>   cost.

**Manufacturing order routing**

>   A routing used to complete a specific manufacturing order, which includes
>   all the necessary requirements to fill the order, such as workers, machine
>   time, and raw materials. Also known as “manufacturing routing.”

**Manufacturing picklist**

>   A list of the items and quantities of items that are required to fill a
>   manufacturing order.

**Material Requirements Planning**

>   A series of data collection and interpretation procedures that allow you to
>   forecast resource requirements over a specified time period (days, weeks or
>   months).

**Maximum order size**

>   One of the variables that can be used to calculate order quantities for
>   fixed or period order quantity order policies. Maximum order size puts a
>   limit on the size of automatically generated purchase and manufacturing
>   orders. If demand is greater than the maximum order size, an additional
>   order will be created.

**MFG BOM**

>   *See Manufacturing bill of materials*.

**Minimum order size**

>   One of the variables that can be used to calculate order quantities for
>   fixed or period order quantity order policies. It is similar to standard
>   order quantity, and is used in its place if the standard order quantity is
>   zero. If the standard order quantity is greater than zero, the standard
>   order quantity supersedes the minimum order size.

**Module security**

>   A way to see if other users are working with records that prevent you from
>   completing certain processes. Module security also allows you to unlock
>   records and remove users from MRP.

**Move in**

>   To adjust the due dates of existing manufacturing orders and purchase orders
>   to meet potential shortages identified by MRP calculations. If MRP
>   calculations uncover a shortage of an item and if there’s an existing order
>   for the item in the future, the order will be flagged to be “moved in” to
>   prevent the shortage.

**Move out**

>   To reschedule certain manufacturing orders or purchase orders to prevent
>   stock overages on the current due date. An appropriate future date to move
>   the order to cover a future net requirement is proposed

**Move time**

>   The number of hours needed to physically move an item to the next operation.

**MRP**

>   *See Material Requirements Planning*.

**MRP shortage**

>   A lack of resources to produce the required amount of an item to fill
>   outstanding orders. Manufacturing orders can be entered regardless of
>   current stock of available materials.

**Multi-level bill of materials**

>   A bill of materials that lists all the components directly or indirectly
>   involved in building the parent part, together with the required quantity
>   for each item. For example, if a subassembly is used in the parent part, the
>   multi-level bill of materials will show all the components needed to build
>   the subassembly, including purchased parts and materials. *See also
>   Single-level bill of materials*.

**Negative WIP**

>   The situation that occurs if you enter and post a manufacturing order
>   receipt where more is consumed from WIP than was in WIP for the
>   manufacturing order. When finished goods are received into inventory before
>   materials have been issued to the order or before labor or machine time data
>   collection transactions have been completed, this can occur. You must set up
>   Manufacturing Order Processing to be able to enter receipts that would cause
>   negative WIP.

**Net change regeneration**

>   An MRP process that updates MRP information based on changes to
>   manufacturing orders, sales orders, purchase orders, and inventory
>   quantities. *See also Full regeneration*.

**Nettable item**

>   An item, site or item-site combination that is included in MRP calculations.

**Non-nettable item**

>   Any item, site, or item-site combination that is not included in MRP
>   calculations.

**Non-Standard Report**

>   A report for internal use that summarizes information about defects
>   identified in a group of items. An NSR might also include information about
>   the disposition of the defective items.

**NSR**

>   *See Non-Standard Report*.

**Op code**

>   *See Operation code*.

**Operation**

>   A specific task within the manufacturing process. You can use operations as
>   templates for routing sequences.

**Operation chart**

>   *See Routing*.

**Operation code**

>   A code assigned to a particular task within the manufacturing process. For
>   example, in a company that makes electrical components, the operation code
>   for testing the validity of a certain characteristic might be “110.” Also,
>   op code.

**Operation list**

>   *See Routing*.

**Operations sheets**

>   *See Routing*.

**Option**

>   In sales configurator, an option is one of the available choices for some
>   aspect of a configured item. For example, a computer manufacturer might
>   offer 15-, 17- and 21inch monitors as options for a computer.

**Option bill of materials**

>   A bill of materials for a component signifying that the component won’t be
>   identical in all finished products.

**Option category**

>   A group of related items that customers can choose from, such as various
>   sizes of computer monitors.

**Option setting**

>   A setting that controls the information that appears on a report, such as
>   sorting method, detail level, and range restriction.

**Order increment**

>   A variable that can be used to calculate order quantities for fixed or
>   period order quantity order policies. The order increment is the number of
>   item units that can be added to the standard order quantity to increase the
>   order size to meet demand.

**Order policy**

>   A method for calculating the order sizes of automatically generated purchase
>   and manufacturing orders. Manufacturing includes three order policies:
>   lot-for-lot, fixed order quantity and period order quantity.

**Originating currency**

>   The alternate currency that a multicurrency transaction was conducted in.
>   *See also Functional currency*.

**Outsourced item**

>   A finished good that requires one or more outsourced services.

**Outsourced service**

>   A service that is part of manufacturing processes that is purchased from a
>   vendor.

**Outsourcing**

>   The practice of using outside vendors to perform certain manufacturing
>   tasks.

**Outsourcing routing**

>   A routing that includes one or more sequences that are completed by an
>   outsourcing vendor.

**Outsourcing vendor**

>   A vendor that you purchase outsourced services from.

**Outsourcing work center**

>   A work center where outsourced services are performed. An outsourcing work
>   center can be on-site or can be at the vendor site.

**Overhead**

>   Costs incurred that cannot be directly related to the products or serviced
>   produced. These costs, such as light, heat, supervision, and maintenance can
>   be grouped and distributed to units of products or services by some standard
>   allocation method.

**Parallel routing**

>   A routing that includes some routing sequences that run concurrently.

**Parent part**

>   An item built from the component parts. A parent part can be a subassembly
>   or a final product.

**Pegging**

>   To trace an item requirement through the MRP system to find the source of
>   the requirement quantity. Pegging will reveal whether a requirement is
>   driven by a manufacturing order, sales order, purchase order or picklist.

**Period order quantity**

>   An order policy type that calculates order size for requirements for a
>   period you specify, based on one or more of these variables: standard order
>   quantity, order increment size, minimum order size and maximum order size.

**Periodic costing**

>   *See Standard costing*.

**Periodic inventory**

>   An inventory tracking method that involves taking inventory on a recurring
>   basis, such as monthly, quarterly or yearly. This is the same as “standard”
>   costing.

**Perpetual inventory**

>   An inventory tracking method that involves constantly updating inventory
>   each time an item is added or removed.

**Phantom bill of materials**

>   A bill of materials used to describe the components of a parent part that
>   will be built as part of a higher-level parent part. The term “phantom” is
>   used to indicate that the part never really exists as a stocked item, but is
>   built along with the production of the higher-level part that is driving an
>   overall production order. Creating bills of materials as phantoms allows the
>   manufacturing order picklist and the Material Requirements Planning (MRP)
>   features to explode through the phantom item down to the lower-level parts.

**Pick document**

>   A group of component transactions that share a type such as Allocate, Issue,
>   Reverse Issue, and that are posted together. A pick document can include
>   component transactions for multiple manufacturing orders, items, or sites.

**Picklist**

>   A list of the items and quantities of items that are required to fill a
>   manufacturing order.

**Planner code**

>   A code that identifies the individual responsible for the production of the
>   item.

**Planning routing**

>   A routing used to determine resource requirements for a potential
>   manufacturing order. If negotiations with the customer are successful, the
>   planning routing can be converted into an active routing and used to fill a
>   manufacturing order.

**Pointer routing**

>   A pointer routing is used to outline a series of steps that are common to
>   all items produced by your plant. For example, if each item needs to be
>   tested by quality assurance, packaged and shipped, a routing can be defined
>   to cover these steps for all items that you manufacture.

**Post-to site**

>   The site where the finished product will be stored prior to delivery to the
>   customer. This location can be a department, a warehouse, or another plant.

**Primary routing**

>   A routing that provides the instructions for building an item. It is a basis
>   for scheduling and resource estimates. The primary routing information is
>   used to determine the required lead time for manufacturing the product. Each
>   item can have only one active primary routing.

**Process security**

>   A type of security that allows you to restrict access to certain procedures
>   or processes within Manufacturing.

**Process security set**

>   A password or list of user IDs you define to restrict authority for
>   completing a Manufacturing process. You can use one process security set for
>   all restricted procedures, or you can create different process security sets
>   for different procedures.

**Production variance**

>   The difference between the actual and estimated costs for a manufacturing
>   order, based on the working routing, the picklist, and labor and machine
>   codes.

**Promise date**

>   The date that the customer has been told to expect receipt of the order.

**Promotion**

>   Special pricing offered on a particular option for a configured item.

>   A special pricing offered on a particular option for a configured item.

**Purchase order**

>   A formal request for goods or services. The purchase order shows the
>   quantity of goods ordered, expected receipt date, and supplier name. The
>   purchase order may also include other information pertaining to the delivery
>   of the item, such as Free On Board (F.O.B.) points.

**QA Required**

>   A designation for purchased items that must pass a quality inspection before
>   being added to your inventory.

**Quantity damaged**

>   The total items, if any, damaged during shipping.

**Quantity ordered**

>   The amount of the item requested on a single purchase order.

**Quantity received**

>   The amount of the item received from the supplier.

**Quantity to fill** An amount of a product that was ordered but has not been
received.

**Query**

>   A search through a specific set of records for certain information.

**Queue time**

>   The number of hours spent waiting for the operation to begin.

>   The number of hours spent waiting for an operation to begin.

**Quick manufacturing order**

>   A manufacturing order that doesn’t require you to collect information about
>   labor and machine time and material costs when the order is closed.

**Quote**

>   A company’s offered price for an item that a customer or a potential
>   customer has requested. Quotes can be transferred to another document type,
>   deleted or voided.

**Raw materials**

>   Items used to build products. They can be individual items like nuts, screws
>   and diodes, or they can be subassemblies.

**Record**

>   A group of computer data tied together by a common key. (All of one item's
>   information—from quantity and site information to engineering data to bill
>   of materials data—is the item's record.)

**Reference designator**

>   Information that specifies where components should be used in an assembly,
>   such as the placement of four resistors on a printed circuit board.

**Regular bill of materials**

>   A simple, single-level bill of materials.

**Replaced item**

>   An item in a mass update to bills of materials that is removed from bills of
>   materials. A replacement item might or might not be substituted for the
>   replaced item.

**Replacement item**

>   An item in a mass update to bills of materials that is added to bills of
>   materials. A replacement item might be an addition to a bill of materials,
>   or might be a substitution for a replaced item.

**Return**

>   An item or merchandise returned by a customer to your company. A return
>   decreases the customer's balance on account and, if you choose, increases
>   inventory quantities.

**Revalue**

>   To finalize rolled-up standard cost changes. Revaluing replaces existing
>   standard cost information with new standard cost information, which is used
>   in your accounting processes. As you change your standard cost information,
>   you might roll up costs several times, but probably will revalue items only
>   at certain points.

**Revenue/expense code**

>   A short identifier used to categorize expenses and revenues linked to a job.

**Reverse allocate**

>   A component transaction type where items that have been allocated to a
>   manufacturing order are unallocated. *See also Allocate*.

**Reverse Issue**

>   A component transaction type where components that were issued to a
>   manufacturing order (which removes them from inventory and adds them to WIP)
>   are removed from WIP and put again in inventory. *See also Issue*.

**Reverse Scrap**

>   A component transaction type where components that were scrapped for a
>   manufacturing order are restored to the issued (and not scrapped) quantity
>   for the order. *See also Scrap*.

**Roll up**

>   To apply calculations based on changes to standard cost information to
>   items. If you change the cost of a raw material that is part of several
>   subassemblies and finished goods, “rolling up” that change will result in
>   calculations that will determine the new standard costs of the subassemblies
>   and finished goods.

>   As you change your standard cost information, you might roll up costs
>   several times, but probably will revalue items only at certain points.

**Routing**

>   A detailed set of instructions that describes how to create a particular
>   item. Routings include operations to be performed, the scheduling sequence,
>   machines and work centers involved, and hours required for setup and run
>   times. Routings also can include information about tooling, operator skill
>   levels, inspection needs, testing requirements, and so on.

>   In engineering change management, a routing is a list of users who must
>   review an engineering change request before it becomes a change order, and
>   who must review a change order before it's finalized.

**Routing preference**

>   An individual user choice on how information is displayed or processed for
>   update in the routings subsystem. Preferences can control such actions as
>   substituting one description for another or appending work center operations
>   notes on to routing notes.

**Routing sequence**

>   A single step in the manufacturing process. Some routings will contain
>   multiple steps while others will have only a single step. Examples of a
>   sequence include assembly, painting, drying, etc.

**Routing sheets**

>   *See Routing*.

**Run labor code**

>   A labor code that identifies the skill requirements to perform the operation
>   as defined.

**Run orders**

>   *See Manufacturing order*.

**Sales order**

>   A request for goods or services. Sales orders can be Open (ready to be
>   filled) or Planned (hold pending credit check or other criteria).

**Sampling**

>   A statistical process of selecting a portion of a large group of items to be
>   inspected. From the sample you select—and your inspection results for the
>   sample—you can draw inferences about the overall quality of the entire item
>   quantity.

**SCAR**

>   *See Supplier Corrective Action Request*.

**Scheduling data**

>   The lead time needed to manufacture an item on a bill of materials and the
>   amount of scrap materials produced by the manufacturing process.

**Scheduling preference**

>   A user preference that controls the allocation of resources to a particular
>   manufacturing order. Scheduling preferences identify additional resources
>   that may be available and define waiting periods for a sequence.

**Scrap**

>   A component transaction type where components that are issued to a
>   manufacturing order are flagged to be scrapped. Scrapped component costs are
>   applied to the manufacturing order costs, but the quantities aren’t.

**Sequence number**

>   A number assigned to a particular step in a routing. Each step (or sequence)
>   represents an operation in the manufacturing process. The sequence number
>   controls the order in which steps are executed.

**Serial-numbered item**

>   An inventoried item that is assigned a unique identifier, which can be
>   letters, numbers, or a combination of letters and numbers.

**Serial-number–tracked item**

>   *See Serial-numbered item*.

**Serial-tracked**

>   *See Serial-numbered item*.

**Setup cost**

>   The cost of preparing a work area for production. Setup costs might include
>   the cost of calibrating machines or gathering the necessary tools and
>   resources.

**Setup labor code**

>   A labor code that identifies the skill requirements for the person preparing
>   the work area prior to performing the manufacturing task.

**Setup time**

>   The number of hours needed to prepare the work area prior to the operation.

**Ship date**

>   The date when a sales order leaves your warehouse or office.

**Shipping method**

>   The manner in which the items are transported from the supplier to the
>   manufacturer. Examples of shipping methods include FedEx, rail, air freight,
>   etc.

**Shop calendar**

>   A calendar of up and down days—days when the plant is in production and when
>   it isn’t—for an entire manufacturing facility.

**Shop order**

>   *See Manufacturing order*.

**Shop rate**

>   The average pay rate for the pay grade. It is the figure that is used when
>   labor costs are estimated for a manufacturing order.

**Shrinkage**

>   The loss of materials. You might have raw material shrinkage—such as when
>   some component items are defective and can't be used in manufacturing—or you
>   might have parent part shrinkage—such as when not all manufactured items
>   meet your product standards.

**Single-level bill of materials**

>   A bill of materials that lists components and subassemblies, including the
>   quantities of each, that make up the parent part. *See also Multi-level bill
>   of materials*.

**Site**

>   A location that you have defined for storing items. A site could be a
>   department, a plant, or a warehouse. The number of sites depends on your
>   organizational structure.

**Source routing**

>   A previously defined routing that contains one or more steps that you want
>   to use in a new routing.

**Standard cost variance**

>   The difference between the actual costs for a manufacturing order for a
>   standard cost item, and the standard cost of the item.

**Standard costing**

>   An accounting method used by some businesses to value their inventories. A
>   company that uses standard costing—also known as “periodic costing”—revalues
>   its inventory periodically to reflect significant changes in the cost of its
>   items.

**Standard order quantity**

>   A variable that can be used to calculate order quantities for fixed or
>   period order quantity order policies. It is similar to a minimum order
>   quantity, requiring no less than a set amount for an order, but it can be
>   increased, either by increments or multiples of the standard order quantity.

**Subassembly**

>   A part that is both a component and a parent part. An assembly that is used
>   in the manufacture of a higher-order assembly.

**Super bill of materials**

>   A list of all the component items that can possibly be included the bill of
>   materials for a finished item. For example, a computer manufacturer might
>   develop a super bill of materials that includes several options for hard
>   disks, RAM, monitors, keyboards, mice and other peripherals. No computer can
>   include all the options, but all the options must be included in the super
>   bill of materials.

**SUPER BOM**

>   *See Super bill of materials*.

**Supplier**

>   A person or company that supplies goods or services to a manufacturer.

**Supplier Corrective Action**

**Request**
A formal report to be sent to a supplier to involve the supplier in
resolving problems with defective parts. SCARs describe the problems you’ve
found—including item numbers, lot numbers, dates and test results—and might
outline possible areas for the supplier to research to prevent the defect
from recurring. Suppliers usually are required to respond to the SCAR
reports with information about the cause of the defect and the steps to be
taken to prevent its recurrence.

**Template**
A routing outline that you can use to quickly and efficiently build new
routings. Each time you need to create a new routing, you can customize the
template and give it a unique routing name.

**Time fence**
The minimum amount of time required for production of an item. When MRP is used to create planned manufacturing orders or purchase orders, the orders automatically are scheduled outside the time fence.

**Total costs**
The cumulative total of all expenses associated with a manufacturing order, plus any overhead that might not be directly connected to the order.

**Trade discount**
A price reduction, usually granted to a certain customer because of the customer’s special status. Customers with an excellent credit history might be offered a trade discount.

**Unit costs**
The value of time and resources consumed to create one unit of product for this order.

**Unmet forecasted demand**
The difference between forecasted demand (the anticipated amount of an item that will be required to meet projected orders) and actual production.

**Up day**
A day when the facility—the entire shop floor or a specific work center—is in production.
 
**User-defined field**
A field that can be used to track information specific to your company.

**Valuation method**
The process used to track inventory value (FIFO Perpetual, FIFO Periodic, LIFO Perpetual, LIFO Periodic, Average
Perpetual).

**Variance**
The difference between two values, such as the difference between estimated and actual expenses.

**Where used**
A Manufacturing query that scans your bills of materials and routings to find where items, machines and other things you’ve defined are used. If you performed a “where used” search for all items in your plant that use a certain machine, for instance, the system would generate a list of all items that have a step involving that machine.

**Window security**
A system that allows you to specify which windows each user in your organization will be able to use.

**Work center**
A self-contained unit of the manufacturing process, or an entire plant. A work center might be an assembly area, a shipping and receiving area or a painting area. Machines and employees are the main components of work centers.

**Work center calendar**
A calendar of up and down days—days when the plant is in production and when it isn’t—for a specific work center.

**Working routing**
*See Manufacturing order routing*.

**Work In Process (WIP)**
A system that helps you to track and analyze the costs associated with a particular manufacturing order and view the progress of the manufacturing order.

