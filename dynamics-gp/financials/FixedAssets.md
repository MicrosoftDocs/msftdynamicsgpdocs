**Introduction**

You can use Fixed Asset Management, to set up, enter, and maintain asset
records. When necessary, you can add insurance and user-defined information and
create additional records for each asset, including investment tax credit
information and lease information.

You also can use Fixed Asset Management to complete the following tasks:

-   Calculate depreciation

-   Import information to Fixed Asset Management from other sources

-   Create and use asset groups to make maintaining asset records easier

-   Transfer an asset to a new general ledger account or property tax location

-   Retire an asset, partially retire an asset, or retire a group of assets

If you’re using General Ledger, you can track General Ledger information entered
in Fixed Asset Management, such as additions, transfers, depreciation,
retirement of assets, and other changes.

If you’re using Payables Management or Purchase Order Processing, you can track
assets that originate in those modules and add them as fixed assets.

>   This introduction is divided into the following sections:

>   **What’s in this manual**

This manual is designed to give you an understanding of how to use the features
of Fixed Asset Management, and how it integrates with the Microsoft Dynamics® GP
system.

To make best use of Fixed Asset Management, you should be familiar with
systemwide features described in the System User’s Guide, the System Setup
Guide, and the System Administrator’s Guide.

Some features described in the documentation are optional and can be purchased
through your Microsoft Dynamics GP partner.

To view information about the release of Microsoft Dynamics GP that you’re using
and which modules or features you are registered to use, choose Help \>\> About
Microsoft Dynamics GP.

>   The manual is divided into the following parts:

-   *Part 1, Fixed Asset Management setup*, provides information about setting
    up your Fixed Asset Management system.

-   *Part 2, Cards and integration*, provides information about asset records.
    It also explains how to import information from other sources and how Fixed
    Asset Management integrates with other Microsoft Dynamics GP modules.

-   *Part 3, Asset records*, provides information about maintaining asset
    information. It also explains how to use asset groups to make maintaining
    asset records easier.

-   *Part 4, Routines*, provides information about procedures you can use to
    calculate depreciation and integrate Fixed Asset Management with General
    Ledger.

-   *Part 5, Utilities and detail file activity*, provides information about
    maintaining the integrity of your Fixed Asset Management data by reconciling
    your records and performing maintenance on the Fixed Asset Management data
    tables.

-   *Part 6, Inquiries and reports*, provides information about viewing and
    printing Fixed Asset Management data and analyzing asset activity by
    printing specific reports. It also lists the financial information relating
    to the many activities that can occur within Fixed Asset Management.

**Part 1: Fixed Asset Management setup**

>   This part of the documentation provides information about setting up your
>   Fixed Asset Management system.

>   This part includes the following information:

-   *Chapter 1, “Fixed Asset Management setup,”* describes how to set up default
    options and information for Fixed Asset Management. It also describes how to
    set up the Fixed Asset Management fiscal calendar and asset books and
    classes.

-   *Chapter 2, “Company setup options,”* explains how to set up user-defined
    fields and additional information to use if your system is integrated with
    Purchase Order Processing or Payables Management.

-   *Chapter 3, “Optional setup procedures,”* explains how to set up account
    groups, posting accounts, insurance classes, lease company records, and
    location records.

**Chapter 1: Fixed Asset Management setup**

>   The default options and information that you enter before adding fixed
>   assets records to your system will ensure that information will be available
>   when you set up fixed asset cards. You should first set up the Fixed Assets
>   Fiscal Calendar and quarters. You can then set up book, class, book class,
>   and company records.

>   The following information is discussed:

-   *Integration with other modules*

-   *Before you set up Fixed Asset Management*

-   *Setting up Fixed Asset Management*

-   *Building the Fixed Asset Management calendar*

-   *Removing Fixed Assets calendars*

-   *Adding years to a calendar*

-   *Setting up quarter records*

-   *Creating a book record*

-   *Creating a class record*

-   *Depreciation methods and calculations*

-   *Amortization codes*

-   *Averaging conventions*

-   *Creating a book class record*

>   After you’ve completed a setup procedure, you can choose File \>\> Print to
>   print the setup record and verify the information.

#### Integration with other modules

>   Use Fixed Asset Management to enter information about your company’s assets,
>   such as insurance records, depreciation amount, retirements, lease
>   information, repairs, and maintenance.

>   The only Microsoft Dynamics GP module you’re required to use with Fixed
>   Asset Management is System Manager. Fixed Asset Management does integrate
>   with other modules, which, if registered, provide additional functionality
>   to your system.

>   **General Ledger integration** If you’re also using General Ledger, all
>   Fixed Asset Management transactions that affect financial information will
>   be reflected in General Ledger.

>   **Payables Management integration** If you’re also using Payables

>   Management, transactions that are recorded in Payables Management can update
>   your asset records.

>   **Purchase Order Processing integration** If you’re also using Purchase
>   Order Processing, transactions that are recorded in Purchase Order
>   Processing can update your asset records.

>   The following diagram shows how information flows through Fixed Asset
>   Management.

![A screenshot of a cell phone Description automatically generated](media/9a506cb68f654edcf36e63bb628cba71.gif)

#### Before you set up Fixed Asset Management

>   Before you can set up Fixed Asset Management, you should have completed the
>   following company setup procedures:

-   Set up account formats

-   Set up fiscal periods

-   Set up a chart of accounts

>   If you haven’t completed each of the preceding tasks, do so before
>   continuing. Refer to the System Setup documentation for more information.

#### Setting up Fixed Asset Management

>   You must set up the calendar and quarter, book, class, book class and
>   company records before you can use Fixed Asset Management. The following
>   table provides a list of records you must set up:

| **To set up**      | **Refer to**                                    |
|--------------------|-------------------------------------------------|
| Calendar records   | *Building the Fixed Asset Management calendar*. |
| Quarter records    | *Setting up quarter records*.                   |
| Book records       | *Creating a book record*.                       |
| Class records      | *Creating a class record*.                      |
| Book class records | *Creating a book class record*.                 |
| Company records    | *Setting up company records*.                   |

>   After you’ve entered calendar, quarter, book, class, book class, and company
>   records, you should complete the following procedures.

| **Procedure**                                                   | **Additional information**                                                                  |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Create or import asset records.                                 | Refer to *Creating an asset record* or *Importing asset records*.                           |
| Print reports to verify that information was entered correctly. | You can print the Depreciation Ledger, Depreciation Detail Report, and the Property Ledger. |
| Integrate Fixed Asset Management data with General Ledger.      | Refer to *Updating General Ledger with Fixed Asset Management transactions*.                |

#### Building the Fixed Asset Management calendar

>   Use the Fixed Assets Calendar Setup window to create multiple calendars in
>   Fixed

>   Asset Management. When you create a calendar, you can base the calendar on
>   the Fiscal Period Setup window, or the calendar year. You also can create
>   quarters for all of the years.

>   If you selected to create a fiscal calendar, the information in the Fiscal
>   Period Setup window is used to create fiscal periods for other years in the
>   Fixed Asset Management fiscal calendar. Before you build the Fixed Asset
>   Management calendar, be sure that there is at least one year set up in your
>   system and that the years and periods are correct.

>   **To build the Fixed Asset Management calendar:**

1.  Open the Fixed Assets Calendar Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Calendar)

1.  Enter a calendar ID.

2.  Enter a description for the calendar.

3.  Mark Build Calendar.

4.  Select Fiscal Period Setup or Calendar Year.

5.  Enter the start and end of the range of years to build.

>   Fixed Asset Management builds fiscal periods for 100 years prior to and 200
>   years after the year 2000, so the default range of years is 1901 to 2199.

1.  Choose Build Calendar.

>   If the calendar ID has existing years assigned to it, the years set up for
>   the calendar will be deleted.

>   **Fiscal Period Setup** The new years will be built for the calendar based
>   on the entries in the Fiscal Period Setup window. The periods of the
>   calendar are built for the specific calendar ID.

>   **Calendar Year** The new years will be built for the calendar based on a
>   calendar year. The years and periods are built to match the Gregorian
>   Calendar for the range entered in the Years fields.

#### Adding years to a calendar

>   Use the Fixed Assets Calendar Setup window to build additional years that
>   are not set up for the calendar between the range entered in the Years
>   fields. The existing calendar years are not deleted.

>   Be sure that there is at least one year set up in your system and that the
>   years and periods are correct.

>   **To add years to a calendar:**

1.  Open the Fixed Assets Calendar Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Calendar)

1.  Enter a calendar ID.

2.  Enter a description for the calendar.

3.  Enter a year.

4.  Enter all twelve periods the year in the calendar periods scrolling window.

5.  Mark Build Calendar.

6.  Select Existing Calendar Setup.

7.  Choose Build Calendar.

>   The additional years that are not set up for the calendar will be added
>   between the range entered in the Years fields. The existing calendar years
>   are not deleted. The years and periods are built to match the earliest year
>   already set up for the calendar ID.

#### Removing Fixed Assets calendars

>   Use the Remove FA Calendar Years window to remove all the years or selected
>   years that have been set up for a calendar.

>   **To remove Fixed Assets calendars:**

1.  Open the Fixed Assets Calendar Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Calendar)

1.  Select a calendar ID and then choose Remove Years to open the Remove FA
    Calendar Years window.

2.  Select to remove all calendar years or to remove specific calendar years.
    After selecting Years, enter the range of years to remove.

3.  Choose Remove.

#### Setting up quarter records

>   You can set up quarter records to specify starting, ending, and middle dates
>   of each quarter in a year, any time after you’ve built a Fixed Asset
>   Management calendar. You must enter at least one year and define quarter
>   setup records for each year if you use the mid-quarter averaging for
>   calculating depreciation or transfer groups of assets.

>   Use the Quarter Setup window to specify the starting, ending, and middle
>   dates of each of the four quarters for each year in the calendar ID.

>   **To set up quarter records:**

1.  Open the Quarter Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Quarter)

1.  Select a calendar.

2.  Select a year.

3.  Enter the starting and ending dates for each quarter. The middle date will
    be calculated, but you can change it.

4.  Choose Build Quarters.

5.  Choose Save.

#### Creating a book record

>   Use the Book Setup window to define the books you’ll use for fixed assets
>   reporting. For example, you can create a book for corporate reporting,
>   earnings and profits, federal taxes, alternative minimum tax, state tax, or
>   for any other of your company’s accounting needs. You can create up to
>   thirty-two books for each company. If you create more than thirty-two books,
>   you cannot use the Depreciation Process Information window, Depreciation
>   Projection window, and the Asset Year End window.

>   When you initially create a book record, you must select the current fiscal
>   year, and the year must be a valid year in the Fixed Asset Management fiscal
>   calendar. The year determines whether depreciation expense will be posted to
>   the current depreciation expense account or to the prior year depreciation
>   account. Each time you complete year-end processing for a book, the year
>   will be updated. You can’t change the current fiscal year if an asset for
>   the book has been depreciated.

>   To see differences between the depreciation calculated using internal book
>   rules and tax book rules, you can compare up to three books. For more
>   information, refer to *Comparing asset books*.

>   **To create a book record:**

1.  Open the Book Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Book)

1.  Enter a book ID and description.

2.  Select the calendar ID for the book. The calendar ID assigned to the book
    will be used to process financial transactions such as retiring,
    transferring, and depreciating assets.

3.  Select the current fiscal year.

4.  Select a period to determine how the yearly depreciation amount will be
    allocated.

>   **Periodically** To the number of periods in the year.

>   **Daily** To the number of days in the year.

1.  Mark Auto Add Book Info to add an asset book record to this book when you
    add an asset using the Asset General Information window.

2.  Mark the Post to General Ledger option to post all transactions associated
    with the selected book ID to General Ledger. This option is available only
    if you have marked the Allow Reporting ledger in the Fixed Assets Company
    setup window (Financial \>\> Setup \>\> Fixed Assets \>\> Company).

>   *When you mark the Allow Reporting Ledger option in the Fixed Assets Company
>   Setup window, the Post to General Ledger option will be automatically marked
>   and unavailable for selection for the corporate book.*

1.  Select the Reporting Ledger, Base, IFRS or Local, to report all transactions
    associated with the book ID. This option is available only if you have
    marked the Allow Reporting ledger in the Fixed Assets Company setup window
    (Financial \>\> Setup \>\> Fixed Assets \>\> Company).

>   When you mark the Allow Reporting Ledger option in the Fixed Assets Company
>   Setup window, BASE will be selected as the reporting ledger automatically
>   for the corporate book.

>   *Any corporate book transactions completed prior to marking the Allow
>   Reporting*

>   *Ledgers option in the Fixed Assets Company Setup window (Financial \>\>
>   Setup \>\> Fixed Assets \>\> Company) will be automatically assigned to the
>   BASE reporting ledger in General Ledger. If you change the assigned
>   reporting ledger in the Book Setup window, you may want to correct the
>   transactions that already exist in General Ledger for that book.*

1.  Choose Save.

#### Creating a class record

>   Use the Class Setup window to define classes and descriptions of assets. You
>   can use classes to group assets according to account information, insurance
>   information, depreciation rules, and other characteristics of each class for
>   each book.

>   You must define at least one class because you’re required to select a class
>   when you add an asset to your records. When you add an asset record,
>   accounts listed in the account group you specify in this window—if you use
>   account groups—will be the default entries displayed in the Asset Account
>   window. However, you can change the asset account group before saving the
>   information in the Asset General Information window. If account numbers do
>   not exist in the account group, default account entries from the Fixed
>   Assets Company Setup window will be displayed. See *Account groups* and
>   *Creating an account group*, for more information.

>   You can change individual accounts for an asset using the Asset Account
>   window or the account group ID. If you change the account group ID, the new
>   accounts will be copied to the asset account record from the Account Group
>   Setup window for the account group ID specified. See *Changing information
>   for a group of assets* and *Transferring multiple assets* for information
>   about changing account numbers assigned to groups of assets.

>   Although it’s not required, you can enter a default insurance class ID that
>   will be assigned to assets added using this class ID. When you add an asset
>   and assign this class, the insurance class ID will be the default entry in
>   the Asset Insurance window. However, you can change the insurance class ID
>   for any of the individual asset account records. For more information, see
>   *Setting up an insurance class record*.

>   **To create a class record:**

1.  Open the Class Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Class)

![A screenshot of a cell phone Description automatically generated](media/d9feda5af12a073faf0976a28ca673a8.jpg)

1.  Enter a class ID and description. The description will appear on reports and
    inquiries, and in maintenance windows.

2.  You can enter an account group ID that will be the default account group for
    assets added with this class ID.

3.  You can enter an insurance class ID that will define the inflation and
    depreciation rates for this class.

4.  Choose Save.

#### Depreciation methods and calculations

>   Fixed Asset Management supports several depreciation methods. You can use
>   this information to determine how the assets in your book class records
>   should be depreciated. For more information, see *Creating a book class
>   record*.

>   The special depreciation allowance is a percentage of depreciation in
>   addition to the regular first-year depreciation amount. The special
>   depreciation allowance is calculated before the first-year depreciation is
>   calculated. Refer to current IRS regulations or consult a tax professional
>   for information about what property is eligible for the special depreciation
>   allowance, and what percentage applies.

>   If the property is also a passenger automobile, truck, van, or electric
>   vehicle, there are yearly limits on the amount of depreciation you can
>   claim. These limits vary, depending on the year the vehicle was placed in
>   service, and whether or not you claim the special depreciation allowance.

>   The following table lists the depreciation methods and their calculations:

| **Depreciation method**                     | **Calculation**                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Straight-line Orig Life                     | (Cost - Salvage Value - Special Depreciation Allowance) ÷ Original Life in Years If the Original Life includes days, the days will be converted to a fraction with days as the numerator and 365 as the denominator. For example, if the number of days is 146, the fraction would be displayed as 146/365. |
| Straight-line Rem Life                      | (Cost - Salvage Value - (LTD Depreciation Amount - YTD Depreciation Amount)) ÷ Remaining Life in Days This calculation determines the daily depreciation rate, which must be multiplied by the number of days in the year. This method is used when you select the Switch to Straight-Line option.          |
| 125% Declining Balance                      | (Cost - (LTD Depreciation Amount - YTD Depreciation Amount)) ÷ Original Life \*1.25                                                                                                                                                                                                                         |
| 150% Declining Balance                      | (Cost - (LTD Depreciation Amount - YTD Depreciation Amount)) ÷ Original Life \*1.50                                                                                                                                                                                                                         |
| 175% Declining Balance                      | (Cost - (LTD Depreciation Amount - YTD Depreciation Amount)) ÷ Original Life \*1.75                                                                                                                                                                                                                         |
| 200% Declining Balance                      | (Cost - (LTD Depreciation Amount - YTD Depreciation Amount)) ÷ Original Life \*2.00                                                                                                                                                                                                                         |
| Sum of the Year’s Digits                    | (Cost - Salvage Value - Special Depreciation Allowance) \* (Remaining Life in Years ÷ Sum of Original Life in Years)                                                                                                                                                                                        |
| Remaining Life                              | (Cost - Salvage Value - (LTD Depreciation Amount - YTD Depreciation Amount)) \* (Remaining Life in Years ÷ Sum of the Remaining Life in Years)                                                                                                                                                              |
| Amortization                                | If you choose the Amortization depreciation method, you also must enter an amortization code and amortization amount or percent. Refer to *Amortization codes* for more information.                                                                                                                        |
| ACRS Personal Property                      | Cost \* Percentage from a table                                                                                                                                                                                                                                                                             |
| **Depreciation method**                     | **Calculation**                                                                                                                                                                                                                                                                                             |
| ACRS Real Property                          | Cost \* Percentage from a table                                                                                                                                                                                                                                                                             |
| ACRS Real Property (Modified Straight Line) | Cost \* Percentage from a table                                                                                                                                                                                                                                                                             |
| ACRS Low Income Housing                     | Cost \* Percentage from a table                                                                                                                                                                                                                                                                             |
| ACRS Foreign Real Property                  | Cost \* Percentage from a table                                                                                                                                                                                                                                                                             |
| No Depreciation                             | No depreciation will be calculated for assets with this depreciation method. This method might be used for assets such as land.                                                                                                                                                                             |
| Declining Balance                           | Net Book Value \* Percentage                                                                                                                                                                                                                                                                                |

#### Amortization codes

>   If you’re using the Amortization depreciation method, you must select the
>   amortization codes and calculations. Refer to the table for more
>   information.

| **Code**   | **Calculation**                                                       |
|------------|-----------------------------------------------------------------------|
| Daily      | Amortization Amount \* 365 (or 366 if leap year)                      |
| Weekly     | Amortization Amount \* 52                                             |
| Monthly    | Amortization Amount \* 12                                             |
| Quarterly  | Amortization Amount \* 4                                              |
| Yearly     | Yearly Depreciation Amount = Amortization Amount                      |
| Percentage | (Cost Basis - (LTD Depreciation - YTD Depreciation)) \* Percentage    |
| Rate       | (Cost Basis - Salvage Value - Special Depreciation Allowance) \* Rate |

>   The Initial Allowance Percentage field in the Asset Book window can be used
>   in conjunction with the Amortization method of depreciation. If you enter a
>   percentage, the percentage of the cost of the asset will be included in the
>   first year depreciation amount, in addition to the normal first year
>   depreciation amount.

#### Averaging conventions

>   Averaging conventions are guidelines for calculating depreciation in the
>   year of the acquisition of the asset and the year of the disposal of the
>   asset.

>   During the first year in service, depreciation is calculated using the
>   depreciation method and averaging convention for the asset. The resulting
>   depreciation amount is distributed over the period of time from the date it
>   was placed in service to the last day of the year.

>   *You should use the Mid-month (1st of month), Mid-month (15th of Month),
>   Next Month, or Full Month averaging convention only if your fiscal periods
>   are set up to match the calendar year.*

>   The averaging convention does not change the dates an asset is retired or
>   placed in service. The following averaging conventions are available in
>   Fixed Asset Management.

>   **Half-year** Assets begin depreciating on the Place in Service Date. In the
>   year of disposal, assets are retired on the last day of the first half of
>   the year.

>   Only half of the depreciation amount is taken in the year an asset is
>   acquired. This also applies to the year in which you dispose of an asset and
>   to the year in which the life is complete, based on the original life of the
>   asset. The asset doesn’t depreciate after the first half of its final year.

>   **Modified Half-Year** Assets that are placed in service in the first half
>   of the year will begin depreciating on the first day of the year.

>   Assets that are placed in service in the second half of the year will begin
>   depreciating on the first day of the next year.

>   Assets with a retirement date in the first half of the year will be retired
>   on the last day of the previous year.

>   Assets with a retirement date in the second half of the year will be retired
>   on the last day of the year.

>   **Mid-month (1st of month)** Assets that are placed in service in the first
>   half of the month—days 1 through 15—will begin depreciating on the first day
>   of the month.

>   Assets that are placed in service in the second half of the month—day 16
>   through end of month—will begin depreciating on the first day of the next
>   month.

>   Assets with a retirement date in the first half of the month—day 1 through
>   15—are considered retired on the last day of the previous month.

>   Assets with a retirement date in the second half of the month—day 16 through
>   end of month—will be retired on the last day of the month.

>   **Mid-month (15th of Month)** Assets that are placed in service at any time
>   during the month will begin depreciating on the 16th of the month. Assets
>   that were placed in service in February will begin depreciating on the 15th
>   of the month.

>   Assets retired at any time during the month will be retired on the 15th of
>   the month of the retirement date. Assets retired in February will be retired
>   on the 14th of the month.

>   **Mid-quarter** Assets that are placed in service at any time during the
>   quarter will begin depreciating on the middle day of the second month of the
>   quarter.

>   Assets retired at any time during the quarter are considered retired on the
>   middle day of the second month of the quarter.

>   **Next Month** Assets that are placed in service at any time during the
>   month will begin depreciating on the first day of the next month.

>   Assets retired any time during a month will be retired on the last day of
>   the month.

>   **Full Month** Assets that are placed in service at any time during the
>   month will begin depreciating on the first day of the month.

>   Assets retired at any time during the month are considered retired on the
>   last day of the previous month.

>   **Next Year** Assets that are placed in service at any time during the year
>   will begin depreciating on the first day of the next year.

>   Assets retired at any time during the year will be retired on the last day
>   of the year.

>   **Full Year** Assets that are placed in service in the first half of the
>   year will begin depreciating on the first day of the year.

>   Assets that were placed in service in the second half of the year will begin
>   depreciating on the first day of the last half of the year.

>   Assets with a retirement date during the first half of the year will begin
>   depreciating on the first day of the last half of the year. Assets with a
>   retirement date during the second half of the year are considered retired on
>   the last day of the first half of the year.

**Full Year All Year** Assets will begin depreciating on the first day of the
year.

>   Assets with a retirement date anytime during the year will be retired on the
>   last day of the previous year.

>   **None** Assets will begin depreciating on the date it was placed in service
>   and will be retired on the retirement date.

>   **Next Period** Assets that are placed in service at any time during the
>   period will begin depreciating on the first day of the next period.

>   Assets retired at any time during the period will be retired on the last day
>   of the period.

>   **Full Period** Assets that are placed in service at any time during the
>   period will begin depreciating on the first day of the period.

>   Assets retired at any time during the period will be retired on the last day
>   of the preceding period.

#### Creating a book class record

>   Use the Book Class Setup window to enter specific depreciation information
>   for each class and book combination. For example, suppose your business uses
>   three types of books to track information for its assets—corporate books,
>   federal tax books, and alternative minimum tax books. You must create three
>   records in the Book Class Setup window for each asset class.

>   You can select a switchover method—straight-line or no switch—for
>   depreciation assets. If you choose the straight-line method, the
>   depreciation method for the asset will change to the straight-line remaining
>   life depreciation method, when the depreciation for an asset is greater
>   using the straight-line method than the current depreciation method the
>   asset is using. Switchover for the asset will occur only at the beginning of
>   the year when the yearly depreciation rate is calculated for the next year.

>   For more information about depreciation methods and averaging conventions,
>   see *Depreciation methods and calculations* and *Averaging conventions*.

>   **To create a book class record:**

1.  Open the Book Class Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Book Class)

![A screenshot of a cell phone Description automatically generated](media/925f61c8dfc0e7e178fb7aac60cd4e9f.jpg)

1.  Select a book ID and a class ID.

2.  Select a depreciation method and an averaging convention.

3.  Select a switchover method.

4.  Enter the Original Life to be used for assets assigned to this book class.

5.  Mark Special Depr Allowance and enter the percentage of the cost basis of
    the asset book to be used for the special depreciation amount.

6.  Mark the Salvage Estimate option if the salvage value of an asset assigned
    to this book class should be calculated.

>   If you marked Salvage Estimate, enter a salvage percentage. The percentage
>   will be multiplied by the cost basis of each asset to calculate the salvage
>   value.

1.  Select Yes to apply US luxury auto limits to assets in this book class.
    These limits apply to tax books only.

2.  You can mark the Luxury Van or Truck option or the Luxury Electric Auto
    option to apply luxury tax limits to assets in this book class, depending on
    the type of vehicle.

3.  You can select the US Tax Equity Fiscal Responsibility Act (TEFRA) option
    used in calculating investment tax credit on assets placed in service prior
    to 1986. However, the TEFRA option isn’t used for calculations in Fixed
    Asset Management.

4.  Choose Save.

**Chapter 2: Company setup options**

>   You can use the Fixed Assets Company Setup window to define up to 15
>   userdefined fields and to enter Fixed Asset Management information for your
>   company. For more information, refer to *Setting up user-defined field
>   values*. You also can enter additional information to use if your system is
>   integrated with Purchase Order Processing or Payables Management.

-   *Asset account option*

-   *Asset book option*

-   *User data option*

-   *Purchasing options*

-   *Fixed assets purchasing transactions*

-   *Setting up company records*

#### Asset account option

>   If Fixed Asset Management is integrated with General Ledger, you must mark

>   Require Asset Account in the Fixed Asset Company Setup window, and you must
>   enter and save asset accounts before you can create a book record for an
>   asset. If you mark Require Asset Account, you must enter default account
>   numbers for the company in the Default Accounts window. These accounts will
>   be displayed for any asset account record with blank account numbers. For
>   more information, refer to *Creating an account group*

>   Marking the Require Asset Account option in the Fixed Asset Company Setup
>   window requires that an asset account record includes all eight accounts
>   before adding an asset book record. The asset account record will be added
>   when the information from the Asset General Information window is added.

>   If future fixed assets transactions will be transferred to General Ledger,
>   mark the Require Asset Account option in the Fixed Assets Company Setup
>   window.

#### Asset book option

>   You can mark the Auto Add Book Info option, to indicate that an asset book
>   record should be created automatically when adding information in the Asset
>   General Information window.

>   The Auto Add Book Info option also is included in the Asset General
>   information window so you can choose not to include book information when
>   adding an asset in cases where it’s not appropriate to do so. If the Auto
>   Add Book Info box is marked in the Book Setup window, and the asset book
>   record for that book does not already exist, the asset book record for that
>   book will be added automatically when the asset general information record
>   is saved.

#### User data option

>   Mark to include user-defined fields in Fixed Asset Management windows.
>   Choose the User-Defined button to open the Expand User Fields window to
>   specify the name and format of user-defined fields. For more information,
>   refer to *Setting up user-defined field values*.

>   If the User Data Auto Format option in the Company Setup window is marked,
>   fields without spaces in the User Field Prompt fields will be displayed in
>   the Asset User Data window and Fixed Assets Mass Change User window.

>   For example, if only five user-defined fields are to be used, when setting
>   up the user fields on the Fixed Assets Company Setup window, enter spaces in
>   the user field prompt of the fields that are not to be used. When the Asset
>   User Data window is displayed, only the five fields that contain a user
>   field prompt will be displayed.

#### Purchasing options

>   If you’re using Purchase Order Processing or Payables Management, you can
>   update Fixed Asset Management information by creating entries in those
>   modules. The following options are available in the Fixed Assets Company
>   Setup window.

>   **Post PM through to FA** Mark this option if you’re using Payables
>   Management. Fixed Asset Management will be updated if the account number
>   entered on a PURCH type distribution line in Payables Management matches one
>   of the account numbers in the Fixed Assets Purchasing Posting Accounts Setup
>   window.

>   **Post POP through to FA** Mark this option if you’re using Purchase Order
>   Processing.

-   If you mark the by Account option, Fixed Asset Management will be updated
    when the account number entered on a PURCH type distribution line in a
    Purchase Order Processing transaction matches one of the account numbers in
    the Fixed Assets Purchasing Posting Accounts Setup window.

-   If you mark the by Receipt Line option, each purchase order line item for
    each purchase order receipt line that has the Capital Item option marked in
    the Purchasing Item Detail Entry window will be updated in Fixed Asset
    Management. You also can enter additional asset information that will be
    updated in Fixed Asset Management for each line item.

>   **Include Matching Invoice** Mark this option if you’re using the Post POP
>   through to FA option and if a separate record should be created for each
>   receipt line matched with an invoice amount that is different from the
>   receipt amount.

#### Fixed assets purchasing transactions

>   If Fixed Asset Management is integrated with Payables Management or Purchase

>   Order Processing, information from those modules is transferred to the Fixed
>   Assets

>   Purchasing Transactions window. The information will be stored in the Fixed
>   Asset Management purchasing transactions table until you complete one of the
>   following steps:

-   Delete a transaction in the Fixed Assets Purchasing Transactions window.
    Refer to *Deleting fixed assets purchasing transactions* for more
    information.

-   Mark the Delete Purchasing Transactions Immediately option in the Fixed
    Assets Company Setup window. When the total amount of the purchase has been
    applied to one or more assets, and the unapplied amount is zero, the record
    will be deleted automatically.

>   • Delete all transactions that have been fully applied to assets where the
>   unapplied amount is zero. For more information, refer to *Deleting fixed
>   assets purchasing transactions*.

#### Setting up company records

>   Use the Fixed Assets Company Setup window to create user-defined fields,
>   enter information if your system integrates with Payables Management or
>   Purchase Order Processing, and select default guidelines for your system.
>   Refer to *Using Fixed Asset Management with Payables Management* and *Using
>   Fixed Asset Management with Purchase Order Processing* for more information.

>   **To set up company records:**

1.  Open the Fixed Assets Company Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Company)

![A screenshot of a cell phone Description automatically generated](media/b68fcc0412160339745d781f8981dbba.jpg)

1.  Select the book that will be used for corporate depreciation and that
    General Ledger transactions come from.

2.  Mark the Auto Generate Next Asset ID option to automatically generate the
    next asset ID in the Asset General Information window. Then, enter the next
    asset ID to use when adding a new asset. If you leave this field blank, you
    will have to enter the asset ID in the Asset General Information window.

>   Be sure that the asset ID ends with a series of digits rather than letters.
>   If you enter a next asset ID that ends in alphabetic characters, such as
>   8050AC, the system is unable to increment to the next ID in the Asset
>   General Information window. By defining the next number, you also are
>   determining the number of unique asset IDs that will be available. For
>   example, if you enter FA00001 as the next number, you'll be able to enter up
>   to 99,999 unique asset IDs.

>   If you are creating a new asset ID for the destination company during an
>   intercompany transfer, the new default asset ID for each asset is generated
>   from the Next Asset ID field in the Fixed Assets Company Setup window for
>   the destination company. By automatically generating the next asset ID, you
>   can avoid duplication issues with the existing assets in the destination
>   company.

1.  Mark the Require Asset Account option to require that an Asset Account
    record includes all eight accounts before adding an Asset Book record. For
    more information, refer to *Asset account option*.

2.  Mark Auto Add Book Info. For more information, refer to *Asset book option*.

3.  Mark User Data Auto Format to leave a user field blank. The user field won’t
    be displayed in the User Data window. For more information, refer to *User
    data option*.

4.  Mark the Default Asset Label from Asset ID option to copy the asset ID and
    suffix to the Asset Label field automatically when you add an asset.

5.  Mark Validate Custodian if the custodian records you enter in the Asset
    General Information window should be verified is as a valid employee
    records.

6.  Mark Allow Reporting Ledgers to enable BASE, LOCAL and International
    Financial Reporting Standards (IFRS) ledgers for Fixed Assets. When this
    option is marked, you can assign books already created, as well as new Fixed
    Assets books to update one of these reporting ledgers.

>   This option is available only if you have marked the Allow check box for the
>   Reporting Ledgers option in the General Ledger Setup window (Financial \>\>
>   Setup \>\> Financial \>\> General Ledger). Refer to the General Ledger
>   documentation for more information.

1.  Mark Reset History in Detail to create an offsetting transaction for each
    depreciation transaction taken for an asset in closed years. If the Reset
    History in Detail option is not marked, a summary transaction is created in
    the last period of the most recent closed year for all depreciation taken
    for the asset in closed years.

2.  Mark Post in Detail to update General Ledger with Fixed Asset Management
    transactions in detail. When a batch is posted from the Fixed Assets General
    Ledger Posting window, a General Ledger journal entry is created for each
    Fixed Assets Management transaction in the batch. For example, two Fixed
    Assets Management transactions are created when you depreciate all assets
    for a month and then retire several assets. When you post a batch from the
    Fixed Assets General Ledger Posting window for those two transactions, a
    General Ledger journal entry is created for each Fixed Assets Management
    transaction.

>   If the option is unmarked, all transactions are summarized into a single
>   journal entry by account. When you post a batch from the Fixed Assets
>   General Ledger Posting window, there will be one General Ledger distribution
>   per account in the one journal entry.

1.  Mark the Purchasing Options. Refer to *Purchasing options* for more
    information.

2.  Choose the Accounts button to open the Default Accounts window.

![A screenshot of a cell phone Description automatically generated](media/2b95e5bfb8fe6d213b5c8ad18b49daab.jpg)

1.  Select an Account Group to copy the accounts assigned to the group into the
    Company Setup record. You also can enter each account individually or change
    specific accounts after you select an Account Group. For a description of
    each account type, refer to *Creating an account group*. Choose OK.

2.  Choose the User Defined button to open the Expand User Fields window where
    you can define up to 15 user-defined fields.

![A screenshot of a cell phone Description automatically generated](media/331c7082f715a7840f6bed36eb7da0b1.jpg)

1.  You can define default values for the user-defined fields in the User Fields
    List Setup window. Refer to *User data option* for more information.

>   For more information about entering default values for these fields, refer
>   to *Setting up user-defined field values*.

1.  Choose OK to close the Expand User Fields window.

2.  Choose OK in the Fixed Assets Company Setup window.

**Chapter 3: Optional setup procedures**

>   Depending on how your business is structured, you might want to set up
>   additional records, such as account groups, posting accounts, insurance
>   classes, lease company records, and location records.

>   The following information is discussed:

-   *Account groups*

-   *Creating an account group*

-   *Entering fixed assets posting accounts*

-   *Setting up an insurance class record*

-   *Creating a lease company record*

-   *Creating a location record*

-   *Creating a physical location record*

-   *Creating a retirement code*

-   *Creating a structure ID*

-   *Setting up user preferences*

-   *Setting up user-defined field values*

#### Account groups

>   Although you’re not required to set up account groups, using them can speed
>   up the process of entering account records when you add assets to your
>   system. For instance, you can define an account group for each class of
>   assets that you set up using the Class Setup window, and then apply the
>   default account group to assets you add to the class. When you add or change
>   an individual asset, you will use the Account Group ID field in the Asset
>   General Information window to add or change account group information for
>   the asset. You also can use the Account Group ID field in the Asset Account
>   window when changing an individual asset.

>   If you’re not using asset accounts, unmark the Require Asset Account option
>   in the Fixed Assets Company Setup window so that you’re not required to
>   enter account information.

>   If you don’t use account groups in your system, you can set up default
>   accounts in the Fixed Assets Company Setup window and then apply an account
>   record to each asset you add to your system. After viewing default accounts
>   in the Asset Account window, you can change the account information, if
>   necessary.

>   Refer to *Chapter 17, “Financial detail file activity,”* for more account
>   information.

>   You can select up to eight of the following accounts for each account group:

>   **Depreciation Expense** Used to record current year depreciation expense.

>   **Depreciation Reserve** Used to record depreciation reserve or accumulated
>   depreciation.

>   **Prior Year Depreciation** Used to record any depreciation expense that
>   relates to years prior to the current fiscal year. This account number might
>   be the same account specified as the depreciation expense account.

>   **Asset Cost** Used to record the cost of an asset. It is debited when you
>   add an asset and is credited when you retire an asset. It also is debited or
>   credited when you change the cost of the asset.

>   **Proceeds** Used to record the sum of Cash Proceeds and Non-Cash Proceeds
>   when an asset is retired or disposed of.

>   Usually, the cash receipt for the disposal is recorded somewhere else in the
>   accounting process, like Bank Reconciliation cash receipts or Receivables
>   Management cash receipts, if you’re using these modules. These processes
>   would typically post a debit amount to the actual general ledger cash
>   account. The offsetting credit entry amount would be posted to the account
>   entered in the proceeds account. When the retirement transaction is posted
>   from Fixed Asset Management, the proceeds account will be debited.

>   **Recognized G/L** Used to record recognized gain or loss that is calculated
>   when you dispose of or retire an asset.

>   **Non Recognized G/L** Used to record the non-recognized gain or loss that
>   is calculated when you dispose of or retire an asset.

>   **Clearing** If this account is used as a “true” clearing account, it is
>   debited in

>   General Ledger for the PURCH type distribution line in the Purchasing
>   Distribution

>   Entry window when you post in Payables Management or Purchase Order
>   Processing. This account is credited in General Ledger when an asset is
>   added and credited or debited when the asset cost is changed to offset the
>   cost entry. If the balance in the clearing account is zero at the end of
>   each period, items in Purchasing Order Processing or Payables Management
>   that need to be capitalized were added as fixed asset records.

>   If Fixed Asset Management should not affect General Ledger when assets are
>   added to your system, enter the same account in the clearing account that
>   you enter in the asset cost account.

#### Creating an account group

>   Use the Account Group Setup window to define groups of Fixed Asset
>   Management accounts. For more information about using account groups in your
>   company refer to *Account groups*.

>   **To create an account group:**

1.  Open the Account Group Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Account Group)

![A screenshot of a cell phone Description automatically generated](media/1d83ece514798eafe4e1313357ee528b.jpg)

1.  Enter an account group ID and description to identify a group of accounts.

2.  Enter or select account numbers for each of the accounts in the account
    groups.

>   For a description of each account, refer to *Account groups*.

1.  Choose Save.

#### Entering fixed assets posting accounts

>   If you’re also using Payables Management or Purchase Order Processing—and
>   have marked the by Account option in the Fixed Assets Company Setup
>   window—you must set up accounts that will determine how and if fixed assets
>   capital acquisition transactions will be posted to Fixed Asset Management
>   when you enter vouchers in Payables Management or receipts in Purchase Order
>   Processing.

>   Fixed Asset Management will be updated if the account you specify in a
>   purchasing transaction also exists in the Fixed Assets Purchasing Posting
>   Accounts Setup window.

>   Before you enter posting accounts, you must mark the following options in
>   the Fixed Assets Company Setup window:

-   Post PM through to FA

-   Post POP through to FA

-   by Account

>   *These accounts are not used by Purchase Order Processing if you mark the by
>   Receipt Line option in the Fixed Assets Company Setup window.*

>   Refer to *Purchasing options* for more information.

>   Use the Fixed Assets Purchasing Posting Accounts Setup window to enter
>   account numbers that determine if a fixed asset recorded in Payables
>   Management or Purchase Order Processing also will be posted to Fixed Asset
>   Management.

>   **To enter fixed assets posting accounts:**

1.  Open the Fixed Assets Purchasing Posting Accounts Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Purchasing Posting Accounts)

![A screenshot of a cell phone Description automatically generated](media/3a2de110db3ebce0b3102b7b6b902ac2.jpg)

1.  Choose Assigned to view only accounts already entered in this window. Choose
    All to view all the accounts in your chart of accounts.

2.  Enter or select an account number for a clearing account that will be used
    in Payables Management or Purchase Order Processing for a record you’re
    adding to the Fixed Assets purchasing transactions file. For more
    information about clearing accounts, refer to *Account groups*.

3.  You can enter or select a default class ID. If you’re using Payables
    Management or Purchase Order Processing and have marked the by Account
    option in the Fixed Assets Company Setup window and the account number for
    this posting account setup record is entered as the Purchase account, this
    will be the default class ID for this account in the Asset General
    Information window.

4.  Choose Save.

#### Setting up an insurance class record

>   You can set up insurance classes to group and record assets according to
>   similar insurance inflation and depreciation rates.

>   After you’ve set up an insurance class, you can assign the insurance class
>   to asset classes in the Class Setup window. When you add an asset record to
>   your system, the insurance class that you enter in the Class Setup window
>   will be the default entry for the asset in the Asset Insurance window.

>   Use the Insurance Setup window to enter insurance class ID records.

>   **To set up an insurance class record:**

1.  Open the Insurance Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Insurance)

![A screenshot of a cell phone Description automatically generated](media/405750b2bdbdd21c1ca193c5eb7c6474.jpg)

1.  Enter an insurance class ID and description.

2.  Enter an inflation rate. This rate is expressed in net inflated value based
    on original reproduction cost. You would enter a 10% inflation rate as
    110.00.

3.  Enter a depreciation rate. This rate is expressed as an accumulative
    percentage of original reproduction cost.

4.  Choose Save.

#### Creating a lease company record

>   Use the Lease Company Setup window to specify which companies you can lease
>   assets from. Lease companies that you create here will be displayed in the
>   Asset Lease window.

>   Although it’s not required, you also can assign a vendor ID to the lease
>   company. Vendor IDs displayed in this window were set up in the Vendor
>   Maintenance window in Payables Management.

>   **To create a lease company record:**

1.  Open the Lease Company Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Lease Company)

![A screenshot of a cell phone Description automatically generated](media/ba09554b01bb371dba4a6e5e190b1047.jpg)

1.  Enter the name of the lease company.

2.  If your system is integrated with Payables Management, you also can enter or
    select a vendor ID.

3.  Choose Save.

#### Creating a location record

>   Use the Location Setup window to define valid locations for your company.
>   Entries you make for city, county, and state codes are optional, but the
>   information might be useful to include on property tax or other report.

>   Use the Asset General Information window to assign a location ID to an asset
>   record.

>   **To create a location record:**

1.  Open the Location Setup window.

>   (Financial \>\> Fixed Assets \>\> Location)

![A screenshot of a cell phone Description automatically generated](media/a80cdc86c8abd01bc5aac2e212a47292.jpg)

1.  Enter the location ID—for property tax purposes—to be associated with the
    location you’re defining.

2.  Enter city, state, and county codes, as well as their corresponding
    descriptions.

3.  Choose Save.

#### Creating a physical location record

>   Use the Physical Location Setup window to define physical locations.
>   Physical location information isn’t required to set up asset records in the
>   Asset General

>   Information window. However, use this window to set up physical location
>   IDs.

>   Any location IDs you enter in this window first must be set up using the
>   Location Setup window. For more information, refer to *Creating a location
>   record*.

>   **To create a physical location record:**

1.  Open the Physical Location Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Physical Location)

![A screenshot of a cell phone Description automatically generated](media/59cae67a8ab4b3806ac6f73e53a10c15.jpg)

1.  Enter a physical location ID, and a description.

2.  Enter or select the location code for the physical location ID. Location
    codes entered in this window will appear as default entries in the Asset
    General Information window when you enter the corresponding physical
    location ID.

3.  You can enter a last inventory date. It will be updated when you reconcile
    your inventory using the Physical Inventory window.

4.  Choose Save.

#### Creating a retirement code

>   Use the Retirement Setup window to define retirement codes that you can
>   enter when disposing of assets. You must define retirement codes before you
>   can enter retirement information for an asset. Retirement codes also can be
>   useful for reports.

>   **To create a retirement code:**

1.  Open the Retirement Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Retirement)

![A screenshot of a cell phone Description automatically generated](media/5b576b34598f7aeddabbd35ce4229330.jpg)

1.  Enter a code to describe a retirement.

2.  Choose Save.

#### Creating a structure ID

>   You can define structure IDs to provide additional information about assets
>   when you set them up using the Asset General Information window. For
>   example, you could assign assets to cost centers.

>   Use the Structure Setup window to define structure IDs that can be entered
>   when adding asset general information.

>   **To create a structure ID:**

1.  Open the Structure Setup window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Structure)

![A screenshot of a cell phone Description automatically generated](media/6563aaba509e5fedb94298efa394e4e4.jpg)

1.  Enter a structure ID and a corresponding description.

2.  Choose Save.

#### Setting up user preferences

>   You can use the Fixed Assets User Preferences window to display the path
>   settings to specific import and export files used by Fixed Asset Management.
>   This information is in the Dex.ini file for each workstation, but you can
>   change it in this window.

>   If a field is left blank in the Fixed Assets User Preference window, the
>   default value from the installation process will be displayed in the field.
>   As each process is run, the last value used will be displayed in the field.
>   Default import and export file names and descriptions are listed in the
>   following table:

| **File**                              | **Filename** | **Description**                                                                                                                                                                                                                                                   |
|---------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Physical Inventory                    | PhysInv.txt  | Allows asset label and physical inventory location information to be collected using a bar-code reader or other external sources, and imported into Fixed Asset Management.                                                                                       |
| Asset Group Import                    | AssetGrp.txt | Used to create an asset group using a list of fixed assets from an external source. The asset group can be used in any Fixed Asset Management function that can access a group, such as mass transfer, mass retirement, mass change, projection and depreciation. |
| Physical Inventory Information Import | PhysInfo.txt | Adds asset label, physical location IDs, or both to existing assets.                                                                                                                                                                                              |
| Asset Import file                     | Asset.txt    | Allows importing assets from an external source.                                                                                                                                                                                                                  |
| Macro file                            | Assets.mac   | Processing the addition of asset from an external source. The macro is created from the Asset Import file.                                                                                                                                                        |
| Asset ID Export file                  | AssetID.txt  | Asset IDs are exported from Fixed Asset Management to the Asset ID Export file.                                                                                                                                                                                   |
| Asset Label Export                    | AssetLBL.txt | Asset labels are exported from Fixed Asset Management to the Asset Label Export file.                                                                                                                                                                             |
| Sample Data                           |              | The sample data files to use with Fabrikam, Inc. sample company. They are installed during the Microsoft Dynamics GP installation.                                                                                                                                |

>   Import file

>   file

>   file

>   file

>   **To set up user preferences:**

1.  Open the Fixed Assets User Preferences window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> User Preferences)

![A screenshot of a cell phone Description automatically generated](media/5270b1a8f5be005cd0502e763abccc8f.jpg)

1.  Verify or change the paths.

2.  Choose Save.

#### Setting up user-defined field values

>   You can create default values for user-defined fields one through ten in the
>   Expand User Fields window. You can then select these values in the Asset
>   User Data window. If the values are dates, you can verify the information.

>   **To set up user-defined field values:**

1.  Open the Expand User Fields window.

>   (Financial \>\> Setup \>\> Fixed Assets \>\> Company \>\> User Fields
>   expansion button)

![A screenshot of a cell phone Description automatically generated](media/929e2ffdb5a74613ba0bc26a8d909f53.jpg)

1.  Enter user-defined field names and select a format for the fields to use.

2.  Mark the List Valid Values option for each user field to add values to be
    used in that field.

3.  Choose the expansion button to open the User Fields List Setup window and
    enter data to be used as default field information.

![A screenshot of a cell phone Description automatically generated](media/3128c634a2d9af0bda3aa1e98a4531ce.jpg)

1.  If the format is a date format, you can mark the Valid Date option to
    require a valid date entry in the Asset User Data window.

2.  Choose OK to close the window.

3.  Choose Save in the Fixed Assets Company Setup window to save your changes.

Part 2: Cards and integration
=============================

>   This part of the documentation provides information about asset records. It
>   also explains how to import information from other sources and how Fixed
>   Asset Management integrates with other Microsoft Dynamics GP modules.

>   This part includes the following information:

-   *Chapter 4, “Fixed Asset Management cards,”* explains how to create asset
    records, including insurance and user-defined information.

-   *Chapter 5, “Additional Fixed Asset Management cards,”* explains how to
    create additional records for each asset, including investment tax credit
    information and lease information.

-   *Chapter 6, “Integration,”* describes how to transfer information between
    Payables Management and Fixed Asset Management and between Purchase Order
    Processing and Fixed Asset Management. It also explains how to use Fixed
    Asset Management with Multicurrency Management.

-   *Chapter 7, “Asset import,”* explains the information needed to import asset
    data from another fixed assets system or a different source into Fixed
    Assets Management.

Chapter 4: Fixed Asset Management cards
---------------------------------------

>   You can create records for each asset that include account, depreciation,
>   insurance, user data, and general information. You must create an asset
>   general information record before adding any other records for the asset.

>   Some of the default options and information that you entered when setting up
>   Fixed Asset Management will be displayed when you create asset records. You
>   can accept these entries or enter other information.

>   The following information is discussed:

-   *Creating an asset record*

-   *Adding asset records from other modules*

-   *Modifying an asset account record*

-   *Class IDs and account groups*

-   *Creating an asset book record*

### Creating an asset record

>   Use the Asset General Information window to enter an asset general
>   information record for each asset in Fixed Asset Management.

>   If you’re using Payables Management or Purchase Order Processing, you can
>   enter information in Purchase Order Processing or Payables Management, and
>   then update the information in Fixed Asset Management. Refer to *Using Fixed
>   Asset Management with Payables Management* and *Using Fixed Asset Management
>   with Purchase Order Processing* for more information.

>   When you enter an asset ID, you also must enter a suffix for it. The asset
>   ID is used throughout Fixed Asset Management to identify assets; the suffix
>   is used to identify components of assets. The default suffix is 1. You can
>   accept the default suffix or enter or select a different one.

>   Only a few of the fields in the Asset General Information window are
>   required:

>   Asset ID, Description, Class ID, Type, Property Type, Acquisition Date, and
>   Quantity. You have the option to enter information in the other fields in
>   the window.

>   **To create an asset record:**

1.  Open the Asset General Information window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> General)

![A screenshot of a cell phone Description automatically generated](media/b819bd2bb83169d24af06fbcf0a0de57.jpg)

1.  Enter or accept an asset ID, asset suffix, and a description of the asset.

>   A default asset ID displays if you marked Auto Generate Next Asset ID and
>   entered a next asset ID in the Fixed Assets Company Setup window.

1.  You can enter an extended description and a short name for the asset, which
    can be displayed on reports and inquiries.

2.  You can enter or select a master asset ID. A master asset ID is used to
    group components of a single asset or related assets. For example, a
    computer could be an asset that contains a CPU, a monitor, and a printer as
    components. You can assign the same master asset ID to each component so
    that the components are related and can be tracked together, even if they
    become separated over time. You also can change the master ID of an asset.

3.  Enter or select a class ID and select an asset type and property type, or
    you can accept the default types.

4.  You can enter or select an account group ID to assign account numbers to the
    asset.

5.  Enter or select an alias if you are using Analytical Accounting. An alias in
    Analytical Accounting is a group of transaction dimension codes that can be
    used to enter the analysis information quickly during transaction entry.

6.  Enter an acquisition date. The acquisition date will be the default date the
    asset was placed in service and will be the depreciated-to date in the Asset
    Book Information window.

7.  You can enter or select a different currency ID.

>   *If you use Multicurrency Management and you select a currency ID that’s
>   different from the functional currency defined for this company, the
>   functional currency will be calculated based on the appropriate exchange
>   rate. The functional currency will be used to calculate the original
>   acquisition cost displayed in the Asset Purchase window, based on the
>   exchange rate.*

1.  If the Currency ID displayed is the functional currency, you can enter the
    acquisition cost or choose the Acquisition Cost expansion button to open the
    Asset Purchase window and enter detailed information about the acquisition
    cost.

>   You can enter the acquisition cost in the Asset Purchase window or the Asset

>   General Information window. If you enter the acquisition cost in the Asset

>   General Information window, information will be transferred to the Asset
>   Purchase window. You can change the information in the Asset Purchase
>   window.

![A screenshot of a cell phone Description automatically generated](media/d64aabc21e9da7443732fabef4da4bb7.jpg)

>   The acquisition cost displayed in the Asset General Information window is
>   the sum of all the acquisition costs in the Asset Purchase window.

1.  If the Currency ID displayed is not the functional currency, you can enter a
    value in the Orig. Acquisition Cost field.

>   You can enter the currency ID in the Asset Purchase window or the Asset

>   General Information window. If you enter the currency ID in the Asset
>   General Information window, information will be transferred to the Asset
>   Purchase window. You can change the information in the Asset Purchase
>   window.

1.  You can enter or select a physical location ID and enter an asset label.

2.  You can enter or select a structure ID and custodian ID. The structure ID
    further describes the structure this asset is a part of; for example, to
    identify a cost center.

3.  You can enter a manufacturer name and enter or select a location ID. The
    location ID indicates where the item is located for property tax purposes.

    -   Choose the Manufacturer Name expansion button to enter the serial
        number, model number, and warranty information.

    -   Choose the Location ID expansion button to enter an assessed value for
        the item.

4.  Enter the quantity of this asset. The default quantity is 1. The first time
    you create an asset general information record, this quantity is the
    beginning quantity amount.

5.  You can enter the date maintenance was last done on this asset and the date
    the asset was added. The default date is the system date when this record
    was created.

6.  Choose Save.

### Adding asset records from other modules

>   If you are using Payables Management or Purchase Order Processing, you can
>   create asset records from information entered in these modules.

>   Refer to *Chapter 6, “Integration,”* for more information about integrating
>   Fixed Asset Management with other Microsoft Dynamics GP modules.

### Modifying an asset account record

>   Use the Asset Account window to modify an asset account record. You can
>   change the account numbers to be used when posting information for each
>   asset. You can’t create a new account in this window, only assign existing
>   accounts to the asset.

>   No accounting entry is automatically made if you change an account here. If
>   you change the account by using the Fixed Assets Mass Transfer window
>   instead, you can enter a transfer date and entries are made based on that
>   date. For more information, see *Transferring multiple assets*.

>   **To modify an asset account record:**

1.  Open the Asset Account window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> Account)

![A screenshot of a cell phone Description automatically generated](media/81ecee6c1ec95dd027c52ee7ac0551f5.jpg)

1.  Enter or select an asset ID and suffix.

2.  You can enter or select an account group ID.

3.  Enter or select different account numbers for any of the accounts.

4.  Choose Save.

### Class IDs and account groups

>   When you create a general information record for an asset, you must assign
>   the asset to a class ID. To assign an account group with up to eight account
>   numbers to each class ID, refer to *Creating a class record*.

>   You can change the account group before saving the asset general information
>   record. Accounts in the account group will be saved in the asset account
>   record when you add asset general information. If you don’t enter accounts
>   in the account group the company default accounts selected in the Fixed
>   Assets Company Setup window will be displayed.

>   The account group ID in the asset account record is displayed only before
>   the asset account record is saved. After you save the asset account record,
>   you can enter a new account group. These new accounts will be used for all
>   future processing for the asset.

### Creating an asset book record

>   Use the Asset Book window to add asset book records and enter
>   depreciationrelated information. Default entries for information, such as
>   the date an asset was placed in service, depreciation date, original life,
>   and depreciation method, averaging convention, and switchover method, will
>   be displayed; however, you can change any of the information in the Asset
>   Book window.

>   You can choose the Distribution button to view and modify the distribution
>   information that will be saved in the Financial Detail table for
>   transactions entered in this window.

>   You must have completed the following steps before entering information in
>   this window.

-   Created an asset general information record. (Refer to *Creating an asset
    record* for more information.)

-   Created an asset account record, if Require Asset Account was marked in the
    Fixed Assets Company Setup window. (Refer to *Asset account option* for more
    information.)

-   Created a book setup record for the book being added. (Refer to *Creating a
    book record* for more information.)

>   A book class record must exist for the book being created for the class
>   assigned in the Asset General Information window for this asset. For
>   example, if the corporate book for this asset is being created and the class
>   ID in the Asset General Information window for this asset is 101, there must
>   be a book class record for class 101, book ID corporate. Refer to *Creating
>   a book class record* for more information.

>   **To create an asset book record:**

1.  Open the Asset Book window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> Book)

![A screenshot of a cell phone Description automatically generated](media/2200e480968331ec02d102d730cb9b76.jpg)

1.  Enter or select an asset ID and suffix.

2.  Select a book ID to add for this asset.

3.  Enter the date the asset was placed in service and a depreciation date, or
    accept the default dates. The default dates will be the acquisition date for
    the asset from the Asset General Information window.

>   Don’t change the default depreciation date if you’re not entering
>   depreciation balances for year-to-date or life-to-date depreciation. You can
>   enter a depreciation amount for the year only when adding a transaction if
>   the depreciated-to date is in the current fiscal year.

>   *If you are entering year-to-date and life-to-date depreciation balances,
>   you might need to enter a depreciated-to date to that is equal to or later
>   than the place-in-service date. Calculations for depreciation begin on the
>   day after the depreciated-to date.*

1.  You can enter the cost basis amount for the asset. The default cost basis
    entry for each field is the acquisition cost from the Asset General
    Information window. The cost basis in the corporate book is the amount added
    to the applied value if the information for this asset was entered in
    Payables Management or Purchase Order Processing.

2.  You can enter salvage value, year-to-date depreciation, and life-to-date
    depreciation amounts for assets—even if prior depreciation balances exist.
    If you enter a year-to-date amount, the following entries also must be made:

    -   Enter a depreciated-to-date the same as or later than the
        place-in-service date.

    -   Enter a life-to-date depreciation amount the same as or greater than the
        year-to-date depreciation amount.

3.  You can change the following default entries: depreciation method, averaging
    convention, switchover method, original life, amortization code,
    amortization amount/percentage, TEFRA, initial allowance percentage, special
    depreciation allowance, and luxury automobile.

>   Refer to *Depreciation methods and calculations* and *Averaging conventions*
>   for more information.

1.  If the asset is to be depreciated using US luxury automobile limits and you
    selected a tax book for this asset, select Yes for the Luxury Auto field;
    otherwise, select No.

2.  You can mark the Luxury Van or Truck option or the Luxury Electric Auto
    option to apply luxury tax limits to assets in this book class, depending on
    the type of vehicle.

3.  You can choose the Distribution button to open the Financial Detail
    Maintenance window and view the distribution information for this
    transaction.

4.  Choose Save.

Chapter 5: Additional Fixed Asset Management cards
--------------------------------------------------

>   You can create additional records for each asset that can include U.Ss
>   investment tax credit, insurance, lease, and user-defined information.

>   Some of the default options and information that you entered when setting up
>   Fixed Asset Management will be displayed when you create asset records. You
>   can accept these entries or enter other information.

>   The following information is discussed:

-   *Using Section 179 Expense Deduction*

-   *Creating an asset book ITC record*

-   *Adjusting the cost basis to equal the net cost basis*

-   *Creating an asset insurance record*

-   *Creating an asset lease record*

-   *Creating an asset user-defined record*

### Using Section 179 Expense Deduction

>   US Tax Section 179 Expense Deduction allows expensing all or a portion of
>   the cost of an asset in the year of acquisition, rather than depreciating
>   the cost over the life of the asset. Any portion of the asset cost taken as
>   Section 179 cannot be taken also as depreciation. Any portion not expensed
>   as Section 179 is depreciated over the life of the asset. The depreciable
>   basis—reflected in the Net Cost Basis field in the Asset Book ITC window and
>   in the Cost Basis field in the Asset Book window—is reduced by the Section
>   179 amount. Certain restrictions and rules apply, including:

-   Valid for Personal Property only

-   Yearly Section 179 maximums

-   Year 2000 - \$20,000

-   Year 2001–2002 - \$24,000

-   Year 2003, 2004, 2005 - \$100,000

-   \$400,000 ceiling – reduces allowable Section 179 amount dollar for dollar
    for the amount of total acquisitions in the year over the ceiling

-   Any portion of the allowable amount can be designated to any of the year’s
    acquisitions, including all or a portion of a specific asset’s cost

>   If the entire cost of an asset is recorded as a Section 179 expense, the
>   depreciable cost basis of the asset is reduced to \$0 and the asset is
>   marked fully depreciated. The Depreciated to Date field in the Asset Book
>   window should be changed to the last day of the year.

>   The cost basis for the asset book reflects only the depreciable basis.
>   Therefore, the Original Cost field in the Asset Book ITC window should be
>   referenced when reporting on the acquisition cost of Section 179 assets. For
>   example, to determine the total of all eligible Section 179 acquisitions for
>   the year you need to consider the total acquisition costs for the year.

>   The total acquisition cost is the sum of original cost in the Asset Book ITC
>   window, if it exists, and the cost basis in the Asset Book window, when an
>   original cost is not available.

### Creating an asset book ITC record

Use the Asset Book ITC window to add US tax S179 information, US investment tax
credit (ITC) information, and make other adjustments to the cost basis of an
asset. The default original cost basis and net cost basis values will be equal
to the cost basis of the asset book record that you selected. When you save the
record, the Net Cost Basis field is calculated as follows:

Original Cost Basis – Section 179 Exp. Ded. – ITC Cost Red. Amount + or -Misc.
Cost Adjustment

You can add investment tax credit information in the TEFRA, ITC Taken, ITC
Allowed, and ITC Recapture fields. This information isn’t used for any
calculations, although it might be useful to include on reports.

>   **To create an asset book ITC record:**

1.  Open the Asset Book window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> Book)

1.  Enter or select an asset ID and suffix and select a book ID.

2.  Choose ITC/Cost to open the Asset Book ITC window.

![A screenshot of a cell phone Description automatically generated](media/52934f666290968de406741394243d9f.jpg)

1.  You can change the original cost basis of the asset, if necessary.

2.  Enter a Section 179 expense deduction. The Section 179 expense reduces
    amount in the calculation for net cost basis.

3.  You can enter an ITC Cost Reduction amount. This amount reduces the amount
    in the calculation for net cost basis.

4.  You can enter a Miscellaneous Cost Adjustment amount. This amount will be
    added to the original cost basis when calculating the net cost basis.

5.  You can enter information in the fields that are related to investment tax
    credit. Enter the amount of investment tax credit that was taken, allowed,
    and recaptured for this asset.

6.  Select a TEFRA option or accept the default option. This option isn’t used
    for calculations in Fixed Asset Management.

7.  Choose Save to save the asset book ITC record.

### Adjusting the cost basis to equal the net cost basis

>   If the data in the Net Cost Basis field in the Asset Book ITC window does
>   not equal the data in the Original Cost Basis field, the cost basis will be
>   adjusted to match the net cost basis. When you save an asset book record,
>   you also must select a depreciation recalculation option for that asset. You
>   can choose from the following options:

>   **Reset Life** Recalculates depreciation from the date it was placed in
>   service to the date the asset has already been depreciated to. If there are
>   adjustments to the depreciation for any period, they will be saved and
>   displayed in the Asset Book window.

>   **Reset Year** Recalculates depreciation from the beginning of the year to
>   the date the asset has already been depreciated to. If there are adjustments
>   to the depreciation for any period, they will be displayed in the Asset Book
>   window.

>   **Recalculate** Calculates a new rate of depreciation using the new cost
>   basis data, but does not make adjusting entries for depreciation already
>   taken. The new rate of depreciation will be used the next time the
>   depreciation routine is completed.

### Creating an asset insurance record

>   Use the Asset Insurance window to record insurance information for an asset.
>   You can enter a replacement cost, a reproduction cost—the amount it would
>   take to replace the asset, not including depreciation considerations—and an
>   exclusion amount and type.

>   **To create an asset insurance record:**

1.  Open the Asset Insurance window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> Insurance)

![A screenshot of a cell phone Description automatically generated](media/f7068e7458505ca1915240df8cd948bd.jpg)

1.  Enter or select an asset ID and suffix.

2.  Enter or select an insurance class, or accept the default entry. You can use
    the insurance class to group assets that appreciate or depreciate at the
    same rate.

3.  Enter the insurance year—the year the reproduction cost is based on.

4.  Enter the amount it would take to replace the asset, not including
    depreciation considerations, in the Replacement Cost field.

5.  Enter the amount it would cost to reproduce the same asset using current
    year’s prices in the Reproduction Cost field.

6.  Enter the reproduction cost less any amount attributable to depreciation in
    the Depr. Repro. Cost field.

7.  Enter the exclusion amount for the asset. This is the cost of the asset that
    is not included for insurance purpose. For example, if this asset is a
    building, and the foundation is not covered for insurance purposes, you
    would enter the cost of the foundation.

8.  Enter an exclusion type. You can use a code to describe why the amount in
    the exclusion amount field is not included for insurance purposes.

9.  Choose Save.

### Creating an asset lease record

Use the Asset Lease window to create a lease record for any assets that are
leased by your company, such as a car or office furniture.

>   **To create an asset lease record:**

1.  Open the Asset Lease window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> Lease)

![A screenshot of a cell phone Description automatically generated](media/335d4987edeb7c62773be9c1fb318b0d.jpg)

1.  Enter or select an asset ID and suffix.

2.  Enter or select a lease company ID and select a lease type.

3.  Enter the contract ID associated with this leased asset.

4.  Enter the payment, interest rate, and lease end date for this leased asset.

5.  Choose Save.

### Creating an asset user-defined record

Use the Asset User Data window to create up to 15 user-defined asset data fields
to track additional information for an asset. For example, you could save asset
characteristics for a computer, such as hard disk size, processor size, and the
operating system.

For more information, refer to *Setting up user-defined field values*.

>   **To create an asset user-defined record:**

1.  Open the Asset User Data window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> User Data)

![A screenshot of a cell phone Description automatically generated](media/5e2bff74447eb0db7d8d165c8d44cc78.jpg)

1.  Enter or select an asset ID and suffix.

2.  Enter or select user field data. You can select field data only if you
    created default field values. Refer to *Setting up user-defined field
    values* for more information.

3.  Choose Save.

Chapter 6: Integration
----------------------

>   You can add an item in Payables Management or buy an item in Purchase Order
>   Processing and transfer that information to Fixed Asset Management. To
>   transfer information, Fixed Asset Management must be installed on the same
>   machine that Payables Management transactions or Purchase Order Processing
>   receiving transactions are posted from.

>   You can assign more than one transaction, including both Payables Management
>   and Purchase Order Processing transactions, to the same asset. You also can
>   change transactions that have been assigned to an asset and assign the same
>   transaction to multiple assets. If you assign a transaction to an existing
>   asset, you must update the asset book information manually.

>   For information about the integration with General Ledger, refer to *Chapter
>   14, “General Ledger integration.”*

>   The following information is discussed:

-   *Using Fixed Asset Management with Payables Management*

-   *Adding asset records from Payables Management*

-   *Using Fixed Asset Management with Purchase Order Processing*

-   *Integration options for Purchase Order Processing*

-   *Adding asset records from Purchase Order Processing—by Account option*

-   *Adding asset information after receiving purchasing transactions*

-   *Adding asset records from Purchase Order Processing—by Receipt Line option*

-   *Using Fixed Asset Management with Multicurrency Management*

### Using Fixed Asset Management with Payables Management

>   To enter assets in Payables Management and track them in Fixed Asset

>   Management, mark the Post PM through to FA option in the Fixed Assets
>   Company Setup window. For more information, refer to *Purchasing options.*

>   If you’re using Payables Management, you must add at least one special
>   account in the Fixed Assets Purchasing Posting Accounts Setup window. When
>   you create an invoice in Payables Management for an asset item, the account
>   entered on the PURCH-type distribution line in the Payables Transaction
>   Entry Distribution window must match an account in the Posting Accounts
>   Setup window.

>   You can create one or more asset records from a Payables Management
>   transaction, in the Fixed Assets Purchasing Transactions Display window
>   until the total amount of the line item has been applied. The applied amount
>   in the Fixed Assets Purchasing Transactions Display window will be updated
>   when you choose Save in the Asset General Information window. You can view
>   the information from the selected Payables Management transaction in the
>   Asset Purchase window.

>   The following table displays the information that’s transferred to Fixed
>   Asset Management from Payables Management.

| **From Payables Management field**                                                                                                                                            | **To Fixed Asset Management field**          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Vendor ID                                                                                                                                                                     | Vendor ID                                    |
| Voucher Number                                                                                                                                                                | Control Number                               |
| Document Date                                                                                                                                                                 | Acquisition Date                             |
| Document Date                                                                                                                                                                 | Document Date                                |
| Document Number                                                                                                                                                               | Document Number                              |
| Transaction Source (PMTRX Prefix)                                                                                                                                             | Transaction Source                           |
| Voucher Description                                                                                                                                                           | Description (Asset Purchase window)\*        |
| Purchase Order Number                                                                                                                                                         | Purchase Order Number                        |
| PURCH-type distribution amounts                                                                                                                                               | Acquisition Cost and Originating Acquisition |
| \*If there are multiple transactions, the primary transaction’s voucher description will be displayed in the Asset Description field in the Asset General Information window. |                                              |

>   Cost

>   If the payables transaction uses Multicurrency Management, the following
>   fields are transferred:

| **From Payables Management field** | **To Fixed Asset Management field** |
|------------------------------------|-------------------------------------|
| Currency ID                        | Currency ID                         |
| Currency Index                     | Currency Index                      |
| Exchange Rate                      | Exchange Rate                       |
| Exchange Date                      | Exchange Date                       |
| Time                               | Time                                |
| Exchange Table ID                  | Exchange Table ID                   |
| Rate Type ID                       | Rate Type ID                        |
| Rate Calc Method                   | Rate Calc Method                    |
| Denomination Exchange Rate         | Denomination Exchange Rate          |
| MC Trx State                       | MC Trx State                        |

>   For more information about setting up the integration between Fixed Asset
>   Management and Payables Management, refer to the following information:

>   *Entering fixed assets posting accounts* and *Deleting fixed assets
>   purchasing transactions.*

### Adding asset records from Payables Management

>   If Post PM through to FA is marked in the Fixed Assets Company Setup window,
>   you can create a Fixed Asset Management record using information that’s been
>   entered in Payables Management. You can select one or more Payables
>   Management transactions for each asset record.

>   Use the Asset General Information window to create an asset record. Use the
>   Fixed Assets Purchasing Transactions window to transfer information from
>   transactions created in Payables Management to asset records in Fixed Asset
>   Management.

>   Only a few of the fields in the Asset General Information window are
>   required. The required fields are:

-   Asset ID

-   Description

-   Class ID

-   Type

-   Property Type

-   Acquisition Date

-   Quantity

>   You have the option to enter information in the other fields in the window.

>   **To add asset records from Payables Management:**

1.  Open the Asset General Information window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> General)

1.  Enter an asset ID and suffix.

>   A default asset ID displays if you marked Auto Generate Next Asset ID and
>   entered a next asset ID in the Fixed Assets Company Setup window.

1.  Choose Purchase to open the Fixed Assets Purchasing Transactions window. The
    Purchase button is available only if there are transactions in the Fixed
    Assets Purchasing Transactions window.

![A screenshot of a cell phone Description automatically generated](media/ce0516bd40389c46ec8789cf2eae1f49.jpg)

1.  Mark the M box for each transaction to assign that transaction to the asset.
    Mark the P box for the primary transaction. Information from the primary
    transaction will be displayed in the Asset General Information window and
    the Asset Purchase window. Information from other selected transactions will
    be displayed in the Asset Purchase window only.

2.  Choose OK to save the information from the selected transactions to the
    Asset General Information window and the Asset Purchase window.

3.  In the Asset General Information window, enter any additional information.

>   You can enter an acquisition cost, currency ID, and originating acquisition
>   cost in the Asset General Information window only if you haven’t selected
>   any purchasing transactions from the Fixed Asset Purchasing Transactions
>   window.

>   If you selected a purchasing transaction from the Fixed Asset Purchasing
>   Transactions window, you can use the Asset Purchase window to enter or
>   change an acquisition cost, transaction description, currency ID, document
>   number, and other information related to the purchase of the asset. You can
>   enter more than one transaction for each asset.

1.  Choose Save in the Asset General Information window.

>   If the originating unapplied value for a specific asset is zero cost or
>   less, and

>   Delete Purchasing Transactions Immediately is marked in the Fixed Assets
>   Company Setup window, the transaction will no longer be displayed in the
>   Fixed Asset Purchasing Transactions window.

### Using Fixed Asset Management with Purchase Order Processing

>   You can create one or more asset records from a purchase order transaction
>   displayed in the Fixed Assets Purchasing Transactions Display window until
>   the total amount of the line item has been applied. The applied amount in
>   the Fixed Assets Purchasing Transactions Display window will be updated when
>   you choose Save in the Asset General Information window. You can view the
>   information from the selected Purchase Order Processing transaction in the
>   Asset Purchase window.

>   The Purchase Order Processing transaction is transferred to Fixed Asset

>   Management when the transaction is posted. To transfer the transaction
>   information when a specific account is selected, choose the by Account
>   option in the Fixed Assets Company Setup window. To transfer specific line
>   transaction information, choose the by Receipt Line option in the Fixed
>   Assets Company Setup window.

>   **By Account** You must designate the accounts that will indicate the
>   integration by entering them in the Post Accounts Setup window. When you
>   create a purchase order, the account you enter on the receipt or the
>   matching transaction must be an account set up in the Post Accounts Setup
>   window.

>   **By Receipt Line** An asset record is created from an item when the receipt
>   is posted. When you post a receipt, a separate integration record is created
>   in Fixed Asset Management for each receipt line that’s marked as a capital
>   item in the Receivings Item Detail Entry window.

>   You can enter information tracked in the Asset General Information window
>   for each receipt line when you enter receivings transactions in the FA PO
>   Additional Information window. To transfer a transaction to Fixed Asset
>   Management using a receipt with a matching invoice, the cost on the invoice
>   must be different than the cost on the receipt. The amount of the difference
>   will be the amount included in the transaction.

>   If you’ll be receiving more than one item on the same receipt line (quantity
>   is greater than 1), you can mark the Create Multiple Fixed Assets option in
>   the FA PO Additional Information window to create a separate transaction for
>   each item. A separate transaction will be created for each item with the
>   acquisition cost equal to the unit cost of the item. Additional information
>   entered in the FA PO Additional Information Window will be duplicated for
>   each record.

>   If you’re using landed costs, the landed costs that have been assigned to
>   purchase order items or receivings line items will be transferred with the
>   item cost when the purchase order transaction creates an asset record.

### Integration options for Purchase Order Processing

>   The following table explains the effect that various options in the Fixed
>   Assets

>   Company Setup window, the FA PO Additional Information window, and the
>   Receivings Item Detail Entry window have on the integration between Fixed
>   Asset Management and Purchase Order Processing.

| **Window**                                                    | **Option**                                 | **Effect marked option has**                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fixed Assets Company Setup                                    | by Account                                 | The Purchase Order Processing transaction is transferred to the Fixed Assets Purchasing Transactions window when a receipt is posted. The transaction will be summarized by account for the entire receipt. Separate update transactions aren’t created for each receipt line.                                                                                                                                                  |
|                                                               | by Receipt Line                            | The Purchase Order Processing transaction is transferred to the Fixed Assets Purchasing Transactions window only if you mark Capital Item in Purchase Order Processing when you enter the receipt transaction. If the Capital Item checkbox is marked on the purchase order, it will be marked on the receipt. The Capital Item checkbox will only appear if by Receipt Line is marked in the Fixed Assets Company Setup window |
|                                                               | Include Matching Invoices                  | Subsequent matching transactions also create additional fixed asset records for each receipt line matched with an invoice amount that varies from the receipt amount.                                                                                                                                                                                                                                                           |
|                                                               | Delete Purchasing Transactions immediately | Information in the Fixed Assets Purchasing Transactions window will be deleted when the total amount of the purchase transaction is applied by saving the total amount in the Asset Purchase window.                                                                                                                                                                                                                            |
| FA PO Additional Information                                  | Create Multiple Fixed Assets               | Creates a separate Fixed Asset Management transaction for each quantity. The unit cost is the amount of each transaction.                                                                                                                                                                                                                                                                                                       |
| Receivings Item Detail Entry and Purchasing Item Detail Entry | Capital Item                               | Displays the Capital Item expansion button and transfers the Purchase Order Processing transaction to the Fixed Assets Purchasing Transaction window.                                                                                                                                                                                                                                                                           |

>   For more information about setting up the integration between Fixed Asset
>   Management and Purchase Order Processing, refer to the following
>   information:

-   *Purchasing options*

-   *Entering fixed assets posting accounts*

-   *Deleting fixed assets purchasing transactions*

### Adding asset records from Purchase Order Processing—by Account option

>   To enter assets in Purchase Order Processing and transfer them to Fixed
>   Asset Management based on a specific General Ledger account number, mark the
>   Post POP through to FA option in the Fixed Assets Company Setup window and
>   select by Account. For more information, refer to *Purchasing options.*

>   If Post POP through to FA is marked in the Fixed Assets Company Setup
>   window, you can create an asset record in Fixed Asset Management using
>   information that’s been entered in Purchase Order Processing.

>   The following table displays the information that’s transferred to Fixed
>   Asset Management from Purchase Order Processing.

| **From Purchase Order Processing**                                                                                                                                            | **To Fixed Asset Management**                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Vendor ID                                                                                                                                                                     | Vendor ID                                    |
| Receipt Number                                                                                                                                                                | Control Number                               |
| Receipt Date                                                                                                                                                                  | Acquisition Date                             |
| Receipt Date                                                                                                                                                                  | Document Date                                |
| Vendor Document Number                                                                                                                                                        | Document Number                              |
| Transaction Source (RECVG Prefix)                                                                                                                                             | Transaction Source                           |
| Distribution Reference or Receipt Reference                                                                                                                                   | Description (Asset Purchase window)\*        |
| PURCH-Type Distribution Amounts                                                                                                                                               | Acquisition Cost and Originating Acquisition |
| \*If there are multiple transactions, the primary transaction’s voucher description will be displayed in the Asset Description field in the Asset General Information window. |                                              |

>   Cost

>   If the purchasing transaction uses Multicurrency Management, the following
>   fields are transferred.

| **From Purchase Order Processing** | **To Fixed Asset Management** |
|------------------------------------|-------------------------------|
| Currency ID                        | Currency ID                   |
| Currency Index                     | Currency Index                |
| Exchange Rate                      | Exchange Rate                 |
| Exchange Date                      | Exchange Date                 |
| Time                               | Time                          |
| Exchange Table ID                  | Exchange Table ID             |
| Rate Type ID                       | Rate Type ID                  |
| Rate Calc Method                   | Rate Calc Method              |
| Denomination Exchange Rate         | Denomination Exchange Rate    |
| MC Trx State                       | MC Trx State                  |

>   Use the Asset General Information window to create an asset record. Use the
>   Fixed Assets Purchasing Transactions window to transfer information from
>   transactions created in Purchase Order Processing to asset records in Fixed
>   Asset Management.

>   **To add asset records from Purchase Order Processing—by Account option:**

1.  Open the Asset General Information window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> General)

>   A default asset ID displays if you marked Auto Generate Next Asset ID and
>   entered a next asset ID in the Fixed Assets Company Setup window.

1.  Enter an asset ID and suffix.

2.  Choose Purchase. The Purchase button is available only if there are
    transactions in the Fixed Assets Purchasing Transactions window.

3.  In the Fixed Assets Purchasing Transaction window, mark the M box for each
    transaction to assign that transaction to the asset. Mark the P box for the
    primary transaction. Information from the primary transaction will be
    transferred to the asset record.

4.  Choose Select to save the information from the selected transactions to the
    Asset General Information window and the Asset Purchase window.

5.  In the Asset General Information window, enter any additional information.

>   You can enter an acquisition cost, currency ID, and originating acquisition
>   cost in the Asset General Information window only if you haven’t selected
>   any purchasing transactions from the Fixed Asset Purchasing Transactions
>   window.

>   If you selected a purchasing transaction from the Fixed Asset Purchasing
>   Transactions window, you can use the Asset Purchase window to enter or
>   change an acquisition cost, transaction description, currency ID, document
>   number, and other information related to the purchase of the asset. You can
>   enter more than one transaction for each asset.

1.  Choose Save in the Asset General Information window.

>   If the originating unapplied value for a specific asset is zero cost or
>   less, and

>   Delete Purchasing Transactions Immediately is marked in the Fixed Assets
>   Company Setup window, the transaction will no longer be displayed in the
>   Fixed Asset Purchasing Transactions window.

### Adding asset information after receiving purchasing transactions

>   You can enter additional information for that an asset in the FA PO
>   Additional

>   Information window before the Purchase Order Processing transaction is
>   posted to

>   General Ledger. You can open this window only if by Receipt Line is marked
>   in the Fixed Assets Company Setup window. The information you enter in the
>   FA PO Additional Information window will be displayed in the Asset General
>   Information window.

>   **To add asset information after receiving purchasing transactions:**

1.  Open the Receivings Transaction Entry window.

>   (Financial \>\> Transactions \>\> Purchasing \>\> Receivings Transaction
>   Entry)

1.  Enter or select a receipt number and choose the Vendor Item expansion button
    to open the Receivings Item Detail Entry window.

2.  Enter or select a vendor item.

3.  Mark the Capital Item option and choose the Capital Item expansion button to
    open the FA PO Additional Information window.

![A screenshot of a cell phone Description automatically generated](media/ccee4930e53ac6f9ec671353dfa3c166.jpg)

1.  Enter any information to be displayed in the Asset General Information
    window.

2.  Choose Save.

### Adding asset records from Purchase Order Processing—by Receipt Line option

>   To enter assets in Purchase Order Processing and transfer them to Fixed
>   Asset Management by identifying specific transaction line items as capital
>   items, mark the Post POP through to FA option in the Fixed Assets Company
>   Setup window and select by Receipt. For more information, refer to
>   *Purchasing options.*

>   If by Receipt line is marked in the Fixed Assets Company Setup window, you
>   can create an asset record in Fixed Asset Management using information
>   that’s been entered in Purchase Order Processing.

>   The following table displays the information that’s transferred to Fixed
>   Asset Management from Purchase Order Processing.

| **From Purchase Order Processing**                                                                                                                                            | **To Fixed Asset Management**         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Vendor ID                                                                                                                                                                     | Vendor ID                             |
| POP Receipt Number                                                                                                                                                            | Control Number                        |
| Receipt Date                                                                                                                                                                  | Document Date                         |
| Receipt Date                                                                                                                                                                  | Acquisition Date                      |
| Vendor Document Number                                                                                                                                                        | Document Number                       |
| Transaction Source (RECVG Prefix)                                                                                                                                             | Transaction Source                    |
| Purchase Order Type                                                                                                                                                           | Control Type                          |
| Item Description or Vendor Item Description                                                                                                                                   | Description (Asset Purchase window)\* |
| Purchase Order Number                                                                                                                                                         | Purchase Order Number                 |
| Quantity Shipped                                                                                                                                                              | Quantity                              |
| \*If there are multiple transactions, the primary transaction’s voucher description will be displayed in the Asset Description field in the Asset General Information window. |                                       |
| **From Purchase Order Processing**                                                                                                                                            | **To Fixed Asset Management**         |
| Extended Cost (Create Multiple Assets = No)                                                                                                                                   | Acquisition Cost                      |
| Unit Cost (Create Multiple Assets = Yes)                                                                                                                                      | Acquisition Cost                      |
| \*If there are multiple transactions, the primary transaction’s voucher description will be displayed in the Asset Description field in the Asset General Information window. |                                       |

>   If the purchasing transaction uses Multicurrency Management, the following
>   fields are transferred.

| **From Purchase Order Processing**              | **To Fixed Asset Management** |
|-------------------------------------------------|-------------------------------|
| Originating Extended Cost (Create Multiple      | Originating Acquisition Cost  |
| Originating Unit Cost (Create Multiple Assets = | Originating Acquisition Cost  |
| Currency ID                                     | Currency ID                   |
| Currency Index                                  | Currency Index                |
| Exchange Rate                                   | Exchange Rate                 |
| Exchange Date                                   | Exchange Date                 |
| Time                                            | Time                          |
| Exchange Table ID                               | Exchange Table ID             |
| Rate Type ID                                    | Rate Type ID                  |
| Rate Calc Method                                | Rate Calc Method              |
| Denomination Exchange Rate                      | Denomination Exchange Rate    |
| MC Trx State                                    | MC Trx State                  |

>   Assets = No)

>   Yes)

>   If you’re using Purchase Order Processing and the Include Matching Invoices
>   option is marked in the Fixed Assets Company Setup window the same fields as
>   the receipt will be updated in Fixed Asset Management except for the
>   following fields:

| **From Purchase Order Processing**              | **To Fixed Asset Management**     |
|-------------------------------------------------|-----------------------------------|
| Quantity Invoiced                               | Quantity                          |
| (Unit Cost – Receipt Cost) \* Quantity Invoiced | Acquisition Cost                  |
| (Originating Unit Cost – Originating Receipt    | Originating Acquisition Cost      |
| Transaction Source                              | Transaction Source (POIVC Prefix) |

>   Cost) \* Quantity Invoiced

>   The Include Matching Invoices option determines the difference between an
>   invoice amount and a receipt amount.

>   Use the Asset General Information window to create an asset record. Use the
>   FA PO Additional Information window to transfer information from Purchase
>   Order Processing to asset records in Fixed Asset Management.

>   **To add asset records from Purchase Order Processing—by Receipt Line
>   option:**

1.  Open the Asset General Information window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> General)

1.  Enter or select an asset ID and suffix. A default asset ID displays if you
    marked

>   Auto Generate Next Asset ID and entered a next asset ID in the Fixed Assets
>   Company Setup window.

>   If you entered the asset ID and suffix in the FA PO Additional Information
>   window, you need to enter it now only if the Create Multiple Fixed Assets
>   option in the FA PO Additional Information window is marked and you are
>   retrieving the asset information to create an additional asset.

1.  Choose Purchase. The Purchase button is available only if there are
    transactions in the Fixed Assets Purchasing Transactions window.

2.  In the Fixed Assets Purchasing Transactions window, mark the M box for each
    transaction to assign that transaction to the asset. Mark the P box for the
    primary transaction. Information from the primary transaction will be
    transferred to the asset record.

3.  Choose OK to save your changes in the Fixed Asset Purchasing Transactions
    window.

4.  In the Asset General Information window, enter any additional information.

>   You can enter an acquisition cost, currency ID, and originating acquisition
>   cost in the Asset General Information window only if you haven’t selected
>   any purchasing transactions from the Fixed Asset Purchasing Transactions
>   window.

>   If you selected a purchasing transaction from the Fixed Asset Purchasing
>   Transactions window, you can use the Asset Purchase window to enter or
>   change an acquisition cost, transaction description, currency ID, document
>   number, and other information related to the purchase of the asset. You can
>   enter more than one transaction for each asset.

1.  Choose Save in the Asset General Information window.

>   If the originating unapplied value for a specific asset is zero cost or
>   less, and

>   Delete Purchasing Transactions Immediately is marked in the Fixed Assets
>   Company Setup window, the transaction will no longer be displayed in the
>   Fixed Asset Purchasing Transactions window.

### Using Fixed Asset Management with Multicurrency Management

>   You can use a currency other than the company’s functional currency to
>   record asset acquisitions and disposals. The functional currency will be
>   calculated based on the appropriate exchange rates. If applicable,
>   appropriate euro calculations will be made.

>   The following fields have multicurrency functionality:

| **Window name**           | **Field name**    |
|---------------------------|-------------------|
| Asset General Information | Acquisition Cost  |
| Asset Purchase            | Acquisition Cost  |
| Retirements               | Cash Proceeds     |
|                           | Non-cash Proceeds |
|                           | Expenses of Sale  |
| Mass Retirements          | Cash Proceeds     |
|                           | Non-cash Proceeds |
|                           | Expenses of Sale  |

>   If a multicurrency transaction originated in Payables Management or Purchase

>   Order Processing, all appropriate exchange values will be transferred to
>   Fixed Asset Management. Only the functional amount is saved with each asset
>   book record and only functional amounts are transferred from Fixed Asset
>   Management to General Ledger.

>   Mark the Multicurrency box in the Report Options window to print
>   multicurrency versions of these reports:

-   Additions report

-   Additions by Class report

-   Additions by Structure report

-   Additions by Location report

-   Retirements report

-   Retirements by Class report

-   Retirements by Structure report

-   Retirements by Location report

Chapter 7: Asset import
-----------------------

>   If you have asset data in another fixed assets system or a different source,
>   you can import asset records and balance information. You can import new
>   asset records, asset book records, and insurance, lease, and user-defined
>   information into Fixed Asset Management. You also can import information to
>   make changes to the data for an existing asset record.

>   The following information is discussed:

-   *Guidelines for importing asset information*

-   *Importing asset records*

-   *Creating a new book record for existing assets*

-   *Field mappings for importing asset information*

-   *Field values*

### Guidelines for importing asset information

>   The following guidelines pertain to importing asset information into Fixed
>   Asset Management from another source.

-   If the value for a field contains a comma or a single quotation mark, the
    value must be enclosed in double quotation marks. For example: “Desk, 30x60,
    Walnut”.

-   You must create field setup information in Fixed Asset Management before you
    can import other asset information. The following field information must
    exist in Fixed Assets before you can import asset information:

-   Account group ID

-   Asset class ID

-   Book ID

-   Custodian (optional)

-   Insurance class

-   Lease company

-   Location ID

-   Physical location ID

-   Structure ID

-   You must import information into the Asset General Information window before
    or with other information, but after the setup information is imported.

-   If you use account numbers, be sure to mark the Required Accounts option in
    the Fixed Assets Company Setup window to save account numbers with the asset
    record.

-   All numeric fields that have decimals are designated with the number of
    highorder digits and the number of decimal places. For example, ‘12.5’ will
    allow an amount of 999,999,999,999.99999. You don’t need to enter the
    decimal point or commas. If the value to the right of the decimal equals 0,
    enter all *0*’s or a decimal.

-   If you enter any asset book information that would usually be displayed from
    the Book Class Setup window, the data displayed will not be default data
    from the Book Class table.

-   Enter information in either both the Original Life Years field and the
    Original Life Days field, or neither field, to ensure accuracy.

-   If you import information to a field that has a Fixed Asset Management
    default value, the information you import will replace the default
    information.

-   When entering life-to-date depreciation in book records, be sure to include
    the amount in year-to-date depreciation. Year-to-date depreciation should be
    entered if the depreciated-to date represented by life-to-date depreciation
    is in the current fiscal year for the book, defined in the Book Setup
    window. Year-todate depreciation is not required if the depreciated-to date
    is the last day of the current fiscal year.

-   You can import only one asset purchase transaction for each asset.

-   The import file must follow a specific format. The following table shows the
    required data to enter for each file.

| **Column A**      | **Column B** | **Column C** |
|-------------------|--------------|--------------|
| Window identifier | Asset ID     | Asset Suffix |

>   For example, after importing the following information, you can view the
>   information in the Asset General Information window. Three records will be
>   created, but two of the records will have the same asset ID and different
>   suffixes.

| **Column A** | **Column B**   | **Column C** |
|--------------|----------------|--------------|
| GENERAL      | LIGHTTRUCK0005 | 1            |
| GENERAL      | LIGHTTRUCK0005 | 2            |

>   You must import information into specific columns. For information about
>   field positions in the import file, refer to *Field mappings for importing
>   asset information*. If you do not import data for an optional field, you
>   must leave that column blank and not enter information for another field.

### Importing asset records

>   You must mark the All Asset Info option in the Asset Import/Export window to
>   import asset information or make changes to existing asset information.

>   When you import new asset information into the Asset General Information
>   window, an asset book and financial detail information will be created for
>   each book if the following conditions are met:

-   The Auto Add Book Info option is marked in the Book Setup window for each
    book ID.

-   The Auto Add Book Info option is marked in the Fixed Assets Company Setup
    window.

>   To import prior depreciation balances, unmark Auto Add Book Info for all
>   Book Setup records in the Fixed Assets Company Setup window.

>   We recommend that you import several small files rather than one large file.
>   You also should import the information to a test company to view the
>   imported results.

>   **To import asset records:**

1.  Open the Asset Import/Export window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Asset Import/Export)

![A screenshot of a cell phone Description automatically generated](media/d0c6f9f3748a716f1b40966bf77a06b1.jpg)

1.  Mark Import and select All Asset Info.

2.  Enter or browse to find a location to create the macro in, and enter a file
    name for the macro. The file name extension should be .MAC.

3.  Mark the Run Macro After Creation option to start the macro automatically
    after it is created. To run the macro later, from the Microsoft Dynamics GP
    menu choose Macro \>\> Play.

4.  Enter or find the path and name of the file containing the data to be
    imported, or accept the default path and name—Asset.txt.

5.  Select Comma- or Tab-delimited format.

6.  Choose Continue to create the macro and import the data.

>   If a problem error occurs while running the macro that imports the data,
>   information added prior to the problem does not have to be imported again.

### Creating a new book record for existing assets

>   Use the Asset Import/Export window to create a new book record for an
>   existing asset. You must export the existing asset ID and suffixes to a
>   table. In the table, you can add the window identifier and the new book ID.
>   When you import the modified table, asset book records will be created for
>   the new book.

>   *To create new book records you must first set up the book ID, class ID, and
>   book class ID records. Refer to Creating a book record, Creating a class
>   record, and Creating a book class record for more information.*

>   Be sure that the Auto Add Book Info option in the Fixed Assets Company Setup
>   window is not marked when importing information to create asset books.

>   **To create a new book record for existing assets:**

1.  Open the Asset Import/Export window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Asset Import/Export)

1.  Mark Export and select Asset ID & Suffix.

2.  Enter or find the location and name of the file to export the data to.
    Select Comma- or Tab-delimited format.

3.  Choose Continue.

4.  Open the exported file in Microsoft Excel® or Word. Edit the file to contain
    the window identifier—BOOK, Asset ID, Asset Suffix, and Book ID. The file
    name extension should be .TXT.

5.  Import the file. For more information, refer to *Importing asset records*.

### Field mappings for importing asset information

>   You can import data into multiple Fixed Asset Management tables. However,
>   you cannot import data into any Fixed Asset Management setup tables.

>   The data that you import will be displayed in the following Fixed Asset
>   Management windows:

-   Asset General Information window

-   Asset Book window

-   Asset Lease window

-   Asset Insurance window

-   Asset User Data window

>   **Asset General Information window fields**

>   The following table displays the fields included in the Asset General
>   Information window, their field types, length, and additional default entry
>   information.

>   If you don’t accept the default value for a field, you must supply a
>   specific value for that field. For more information, refer to *Field
>   values*.

| **Field name**                                           | **Field type** | **Length** | **Default values**                            | **Required field** |
|----------------------------------------------------------|----------------|------------|-----------------------------------------------|--------------------|
| Window Identifier = GENERAL                              |                |            |                                               | Yes                |
| Asset ID                                                 | String         | 15         |                                               | Yes                |
| Asset ID Suffix                                          | Numeric        | 3          | 1                                             | Yes                |
| Short Name                                               | String         | 15         |                                               | No                 |
| Asset Description                                        | String         | 40         |                                               | Yes                |
| Extended Asset Description                               | String         | 40         |                                               | No                 |
| Master Asset ID                                          | String         | 19         |                                               | No                 |
| Account Group ID                                         | String         | 15         | From Asset Class                              | No                 |
| Structure ID                                             | String         | 30         |                                               | No                 |
| Asset Class ID                                           | String         | 15         |                                               | Yes                |
| Location ID                                              | String         | 15         | From Phy Loc ID                               | No                 |
| **Field name**                                           | **Field type** | **Length** | **Default values**                            | **Required field** |
| Acquisition Date                                         | Date           | 8          | YY = System                                   | Yes                |
| Originating Acquisition Cost                             | Numeric        | 12.5       |                                               | No                 |
| Asset Type                                               | String         | 4          | Refer to *Field values* for more information. | Yes                |
| Property Type                                            | String         | 8          | Refer to *Field values* for more information. | Yes                |
| Asset Quantity                                           | Numeric        | 6          | 1                                             | Yes                |
| Current Maintenance Amount                               | Numeric        | 12.5       |                                               | No                 |
| YTD Maintenance Amount                                   | Numeric        | 12.5       |                                               | No                 |
| LTD Maintenance Amount                                   | Numeric        | 12.5       |                                               | No                 |
| Last Maintenance Date                                    | Date           | 8          | YY = System                                   | No                 |
| Assessed Value                                           | Numeric        | 12.5       |                                               | No                 |
| Vendor ID                                                | String         | 15         |                                               | No                 |
| Document Number                                          | String         | 20         |                                               | No                 |
| Document Date                                            | Date           | 8          | YY = System                                   | No                 |
| Transaction Source                                       | String         | 13         |                                               | No                 |
| Control Number                                           | String         | 20         |                                               | No                 |
| Purchase Order Number                                    | String         | 20         |                                               | No                 |
| Document Description                                     | String         | 40         |                                               | No                 |
| Manufacturer Name                                        | String         | 25         |                                               | No                 |
| Serial Number                                            | String         | 20         |                                               | No                 |
| Model Number                                             | String         | 20         |                                               | No                 |
| Warranty Date                                            | Date           | 8          | YY = System                                   | No                 |
| Custodian (optionally requires setup)                    | String         | 25         | 15 is max length if validation is being used. | No                 |
| Physical Location ID                                     | String         | 15         |                                               | No                 |
| Asset Label                                              | String         | 19         |                                               | No                 |
| Verified Date                                            | Date           | 8          | YY = System                                   | No                 |
| PIN                                                      | String         | 15         |                                               | No                 |
| Currency ID (Req’d only if registered for Multicurrency) | String         | 15         | Functional                                    | Yes                |
| Date Added                                               | Date           | 8          | System Date                                   | Yes                |

>   (MMDDYY or

>   MMDDCCYY)

>   Year

>   (MMDDYY or

>   MMDDCCYY)

>   Year

>   (MMDDYY or

>   MMDDCCYY)

>   Year

>   (MMDDYY or

>   MMDDCCYY)

>   Year

>   (MMDDYY or MMDDCCYY)

>   Year

>   Currency

>   (MMDDYY or

>   MMDDCCYY)

>   **Asset Book window fields**

>   The following table displays the fields included in the Asset Book window,
>   their field types, length, and additional default entry information. If you
>   don’t accept the default value for a field, you must supply a specific value
>   for that field. For more information, refer to *Field values*.

| **Field name**                | **Field type** | **Length** | **Default values**                            | **Required** |
|-------------------------------|----------------|------------|-----------------------------------------------|--------------|
| Window Identifier =           |                |            |                                               | Yes          |
| Asset ID                      | String         | 15         |                                               | Yes          |
| Asset ID Suffix               | Numeric        | 3          | 1                                             | Yes          |
| Book ID                       | String         | 15         |                                               | Yes          |
| Place in Service Date         | Date           | 8          | Acquisition Date on GI                        | Yes          |
| Original Life Years           | Numeric        | 2          | From Book Class                               | No           |
| Original Life Days            | Numeric        | 3          | From Book Class                               | No           |
| Depreciated To Date           | Date           | 8          | Place In Service Date or YY                   | Yes          |
| Cost Basis                    | Numeric        | 12.5       | Acquisition Cost on GI                        | No           |
| Salvage Value                 | Numeric        | 12.5       |                                               | No           |
| Depreciation Method           | String         | 5          | Refer to *Field values* for more information. | No           |
| Averaging Convention          | String         | 5          | Refer to *Field values* for more information. | No           |
| Switchover                    | String         | 2          | Refer to *Field values* for more information. | No           |
| Amortization Code             | String         | 1          | See *Field values* for more information.      | No           |
| Amortization Amount/          | Numeric        | 12.5       | From Book Class                               | No           |
| YTD Depreciation              | Numeric        | 12.5       |                                               | No           |
| LTD Depreciation Amount       | Numeric        | 12.5       |                                               | No           |
| Special Depreciation          | String         | 3          | Refer to *Field values* for more information. | No           |
| Special Depreciation          | Numeric        | 3.2        |                                               | No           |
| Luxury Automobile             | String         | 3          | See *Field values* for more information.      | No           |
| TEFRA Flag                    | String         | 5          | See *Field values* for more information.      | No           |
| ITC Amount Taken              | Numeric        | 12.5       |                                               | No           |
| ITC Amount Allowed            | Numeric        | 12.5       |                                               | No           |
| ITC Recapture                 | Numeric        | 12.5       |                                               | No           |
| Original Cost Basis           | Numeric        | 12.5       | From Book Cost Basis                          | No           |
| **Field name**                | **Field type** | **Length** | **Default values**                            | **Required** |
| Section 179 Expense Deduction | Numeric        | 12.5       |                                               | No           |
| ITC Cost Reduction Amount     | Numeric        | 12.5       |                                               | No           |
| Miscellaneous Cost Adjustment | Numeric        | 12.5       |                                               | No           |

>   BOOK

>   (MMDDYY or

>   MMDDCCYY)

>   Or YY = System Year

>   (MMDDYY or

>   MMDDCCYY)

>   = System Year

>   Percentage

>   Amount

>   Allowance

>   Allowance Percentage

>   Indicator

>   **Asset Lease window fields**

>   The following table displays the fields included in the Asset Lease window,
>   their field types, length, and additional default entry information. If you
>   don’t accept the default value for a field, you must supply a specific value
>   for that field. For more information, refer to *Field values*.

| **Field name**            | **Field type**            | **Length** | **Default values**                       | **Required** |
|---------------------------|---------------------------|------------|------------------------------------------|--------------|
| Window Identifier = LEASE |                           |            |                                          | Yes          |
| Asset ID                  | String                    | 15         |                                          | Yes          |
| Asset ID Suffix           | Numeric                   | 3          | 1                                        | Yes          |
| Lease Company             | String                    | 15         |                                          | No           |
| Lease Type                | String                    | 1          | See *Field values* for more information. | No           |
| Lease Contract ID         | String                    | 15         |                                          | No           |
| Lease Payment             | Numeric                   | 12.5       |                                          | No           |
| Lease Interest Rate       | Numeric                   | 3.2        |                                          | No           |
| Lease End Date            | Date (MMDDYY or MMDDCCYY) | 8          | YY = System Year                         | No           |

>   **Asset Insurance window fields**

>   The following table displays the fields included in the Asset Insurance
>   window, their field types, length, and additional default entry information.
>   If you don’t accept the default value for a field, you must supply a
>   specific value for that field. For more information, refer to *Field
>   values*.

| **Field name**                | **Field type** | **Length** | **Default**      | **Required** |
|-------------------------------|----------------|------------|------------------|--------------|
| Window Identifier = INS       |                |            |                  | Yes          |
| Asset ID                      | String         | 15         |                  | Yes          |
| Asset ID Suffix               | Numeric        | 3          | 1                | Yes          |
| Insurance Class               | String         | 15         | From Asset Class | Yes          |
| Insurance Year                | Numeric        | 4          |                  | No           |
| Insurance Value               | Numeric        | 12.5       |                  | No           |
| Replacement Cost              | Numeric        | 12.5       |                  | No           |
| Reproduction Cost             | Numeric        | 12.5       |                  | No           |
| Depreciated Reproduction Cost | Numeric        | 12.5       |                  | No           |
| Exclusion Amount              | Numeric        | 12.5       |                  | No           |
| Exclusion Type                | String         | 15         |                  | No           |

>   **Asset User Data window fields**

>   The following table displays the fields included in the Asset User Data
>   window, their field types, length, and additional default entry information.
>   If you don’t accept the default value for a field, you must supply a
>   specific value for that field. For more information, refer to *Field
>   values*.

| **Field name**           | **Field type** | **Length** | **Default value** | **Required** |
|--------------------------|----------------|------------|-------------------|--------------|
| Window Identifier = USER |                |            |                   | Yes          |
| Asset ID                 | String         | 15         |                   | Yes          |
| Asset ID Suffix          | Numeric        | 3          | 1                 | Yes          |
| User Field 1             | String         | 6          |                   | No           |
| User Field 2             | String         | 6          |                   | No           |
| User Field 3             | String         | 10         |                   | No           |
| User Field 4             | String         | 10         |                   | No           |
| User Field 5             | String         | 20         |                   | No           |
| User Field 6             | String         | 20         |                   | No           |
| User Field 7             | String         | 20         |                   | No           |
| User Field 8             | String         | 20         |                   | No           |
| User Field 9             | String         | 40         |                   | No           |
| User Field 10            | String         | 40         |                   | No           |
| User Field 11            | Numeric        | 12.5       |                   | No           |
| User Field 12            | Numeric        | 12.5       |                   | No           |
| User Field 13            | Numeric        | 12.5       |                   | No           |
| User Field 14            | Numeric        | 12.5       |                   | No           |
| User Field 15            | Numeric        | 12.5       |                   | No           |

### Field values

>   If you supply a value instead of accepting the default value for certain
>   fields, you must supply a specific value for that field. The following table
>   displays the values you can choose from when importing field information.
>   For example, for the Asset Type field, to import the value Leased, import
>   LSE. The window containing the field also is displayed.

| **Window name**                  | **Field name** | **Value**                | **Enter** |
|----------------------------------|----------------|--------------------------|-----------|
| Asset General Information window | Asset Type     | New                      | NEW       |
|                                  |                | Used                     | USED      |
|                                  |                | Leased                   | LES       |
|                                  | Property Type  | Personal                 | PERS      |
|                                  |                | Personal, Listed         | PERSLIST  |
|                                  |                | Real                     | REAL      |
|                                  |                | Real, Listed             | RLISTED   |
|                                  |                | Real, Conservation       | RCONS     |
|                                  |                | Real, Energy             | RENERGY   |
|                                  |                | Real, Farms              | REALFARM  |
|                                  |                | Real, Low Income         | REALLIH   |
|                                  |                | Amortizable              | AMORT     |
| Asset Lease window               | Lease Type     | Capital                  | C         |
|                                  |                | Operating                | O         |
| Asset Book window                | Depreciation   | Straight-line Original   | SLO       |
|                                  |                | Straight-line Remaining  | SLR       |
|                                  |                | 125% DB                  | 125DB     |
|                                  |                | 150% DB                  | 150DB     |
|                                  |                | 175% DB                  | 175DB     |
|                                  |                | 200% DB                  | 200DB     |
|                                  |                | Sum of the Year’s Digits | SOY       |
|                                  |                | Remaining Life           | RL        |
|                                  |                | Amortization             | AM        |
|                                  |                | ACRS Personal            | AP        |
|                                  |                | ACRS Real                | AR        |
|                                  |                | ACRS Real MSL            | ARMSL     |
|                                  |                | ACRS LIH                 | ALIH      |
|                                  |                | ACRS Foreign Real        | AF        |
|                                  |                | None                     | NONE      |
|                                  |                | Declining Balance        | DB        |

>   Housing

>   Methods

>   Life

>   Life

| **Window name**               | **Field name**                 | **Value**                       | **Enter** |
|-------------------------------|--------------------------------|---------------------------------|-----------|
| Asset Book window (continued) | Averaging Convention           | Half Year                       | HY        |
|                               |                                | Modified Half Year              | MHY       |
|                               |                                | Mid-Month (1st)                 | MM1st     |
|                               |                                | Mid-Month (15th)                | MM15      |
|                               |                                | Mid-Quarter                     | MQ        |
|                               |                                | Next Month                      | NM        |
|                               |                                | Next Period                     | NP        |
|                               |                                | Full Month                      | FM        |
|                               |                                | Full Period                     | FP        |
|                               |                                | Next Year                       | NY        |
|                               |                                | Full Year                       | FY        |
|                               |                                | Full Year All Year              | FYALL     |
|                               |                                | None                            | NONE      |
|                               | Switchover                     | No Switch                       | NS        |
|                               |                                | Switch to Straight-Line         | SL        |
|                               | Amortization Code              | Daily                           | D         |
|                               |                                | Weekly                          | W         |
|                               |                                | Monthly                         | M         |
|                               |                                | Quarterly                       | Q         |
|                               |                                | Yearly                          | Y         |
|                               |                                | Percentage                      | P         |
|                               |                                | Rate                            | R         |
|                               | Luxury Automobile Indicator    | Luxury Automobile               | YES       |
|                               |                                | Not a Luxury Automobile         | NO        |
|                               | TEFRA Flag                     | None                            | NONE      |
|                               |                                | Full Credit Reduce Cost by 50%  | FC50      |
|                               |                                | Full Credit Reduce Cost by 100% | FC100     |
|                               |                                | Reduce ITC% by 2 Points         | RE        |
|                               | Special Depreciation Allowance | Mark Special Depr Allowance     | YES       |
|                               |                                | Unmark Special Depr Allowance   | NO        |

Part 3: Asset records
=====================

>   This part of the documentation provides information about maintaining asset
>   information. It also explains how to use asset groups to make maintaining
>   asset records easier.

>   This part includes the following information:

-   *Chapter 8, “Asset groups,”* describes asset groups and explains how to
    build and use the groups. It also explains how to add or remove assets from
    a group or delete a group.

-   *Chapter 9, “Asset maintenance,”* explains how to change information for an
    asset or a group of assets and how to transfer asset information to a new
    general ledger account, property tax location, physical location, or
    structure.

-   *Chapter 10, “Asset transfer,”* explains how to transfer an asset or a group
    of assets to a new general ledger account, property tax location, physical
    location, structure, or master asset ID.

-   *Chapter 11, “Asset retirement,”* explains how to retire an asset, partially
    retire an asset, or retire a group of assets.

Chapter 8: Asset groups
-----------------------

>   You can group assets by specific characteristics and then use those groups
>   to change, transfer, retire, or depreciate the assets in the groups. You
>   also can use asset groups to project depreciation for the assets.

>   The following information is discussed:

-   *Searching for assets*

-   *Building an asset group*

-   *Viewing assets in groups*

-   *Importing data to create an asset group*

-   *Deleting an asset group*

-   *Removing assets from a group*

### Searching for assets

>   Use the Asset Group Search window to select criteria from specific asset
>   fields when building an asset group. Active assets that match the selection
>   criteria will be included in the asset group. You can add additional assets
>   to the group by building the asset group again with up to five different
>   selection criteria.

>   To add an asset to the group, all field information must match the selection
>   criteria, and then you must build the group using each set of criteria. The
>   following examples explain the difference between the types of logic used to
>   select assets.

>   **“And” logic** To build an asset group that includes all assets with the
>   same asset ID and the same class ID, enter the following information in the
>   Asset Group Search window. Assets with both the matching asset ID and the
>   matching class ID will be displayed in the Select Assets window.

|    | **Field Selection**                                                       | **Value** | **Action**                   |
|----|---------------------------------------------------------------------------|-----------|------------------------------|
| 1. | Asset ID                                                                  | Equal     | Enter or select an Asset ID. |
| 2. | Class ID                                                                  | Equal     | Enter or select a Class ID.  |
| 3. | Choose Search. The results will be displayed in the Select Assets window. |           |                              |

>   **“Or” logic** To build an asset group to include assets with either a
>   specific asset ID or a specific class ID, enter the following information in
>   the Asset Group Search window. Assets with the matching class ID will be
>   displayed with the assets that have the matching asset ID.

|    | **Field Selection**                                                                                              | **Value** | **Action**                   |
|----|------------------------------------------------------------------------------------------------------------------|-----------|------------------------------|
| 1. | Asset ID                                                                                                         | Equal     | Enter or select an Asset ID. |
| 2. | Choose Search. The results will be displayed in the Select Assets window.                                        |           |                              |
| 3. | In the Select Assets window, choose Search.                                                                      |           |                              |
| 4. | Class ID                                                                                                         | Equal     | Enter or select a Class ID.  |
| 5. | Choose Search. The results of this search and the previous search will be displayed in the Select Assets window. |           |                              |

### Building an asset group

>   Use the Select Assets window to build a new asset group or rebuild an
>   existing group. You can use asset groups to easily maintain assets.

>   Asset groups are saved on a user-by-user basis. For example, if user A
>   creates an asset group, user B will not see that asset group anywhere in
>   Fixed Asset Management.

>   **To build an asset group:**

1.  Open the Select Assets window.

>   (Financial \>\>Transactions \>\> Fixed Assets \>\> Select Assets)

![A screenshot of a cell phone Description automatically generated](media/bfdb6e6f79d9b169f72e37ec3a9537ee.jpg)

1.  To create and build a new group, choose New Group, enter a name to describe
    the asset group and choose OK.

>   If you’re building an existing group, skip to step 3.

1.  Select the group to build from the Current Group list and choose Search. The
    Asset Group Search window will open.

![A screenshot of a cell phone Description automatically generated](media/bddc74e2d441875bdbb841397db4632b.jpg)

1.  Select a field name and value, and then enter or select a specific field.

>   For example, to select assets that were placed in service before January 1,
>   2003, you would select Place in Service Date in the Field Selection field,
>   Less Than in the Value field, and then enter 01/01/03.

1.  Choose Search. All assets matching the selected values will be added to the
    group.

2.  Repeat steps 3 through 5 to add additional assets to the group.

3.  Choose OK to close the Select Assets window.

### Viewing assets in groups

>   Use the Select Assets window to view assets that are part of an asset group.
>   You can sort assets and select assets to view based on common
>   characteristics or a range of information.

>   **To view assets in groups:**

1.  Open the Select Assets window.

>   (Financial \>\>Transactions \>\> Fixed Assets \>\> Select Assets)

1.  Select a group in the Current Group list.

2.  You can select to view all assets, assets that are in a selected group, or
    assets that aren’t in a selected group.

3.  You can select a sorting option to view assets by a specific characteristic,
    such as a location or class.

4.  To view a range of assets, use the From and To fields to enter the range.

5.  You can choose Mark or Unmark to include all assets or exclude all assets in
    the selected group.

6.  Choose OK to close the window.

### Importing data to create an asset group

>   Use the Select Assets window to import data to create an asset group. For
>   example, you can import asset information for new assets with the same
>   physical location ID from a source such as a bar code reader. The import
>   file you use must be in either a comma- or tab-delimited format.

>   **To import data to create an asset group:**

1.  Open the Select Assets window.

>   (Financial \>\>Transactions \>\> Fixed Assets \>\> Select Assets)

1.  Select an existing group or create a new group. To create a new group, refer
    to *Building an asset group*.

2.  Choose Import Group to open the Import Group window.

![A screenshot of a cell phone Description automatically generated](media/eb11f6ee2080f1932cac7b041c4e6bb8.jpg)

1.  Enter or locate the name of the file to import.

2.  Choose a Save Option and choose how to import the data—by Asset ID or Asset
    Label.

3.  Select a delimiter character.

4.  Choose Continue and then choose OK to import the data and print the FA Asset
    Group Import report.

### Deleting an asset group

>   Use the Select Assets window to delete an asset group. You also can remove
>   an asset from the group. The assets in the group will not be deleted—only
>   the asset group will be deleted.

>   **To delete an asset group:**

1.  Open the Select Assets window.

>   (Financial \>\>Transactions \>\> Fixed Assets \>\> Select Assets)

1.  Select a group.

2.  To remove an asset from the group, unmark the asset.

3.  To delete the group, choose Delete Group and then Yes.

4.  Close the window.

### Removing assets from a group

>   Use the Select Assets window to remove all the assets from a group without
>   deleting the group. See *Building an asset group* to rebuild the group.

>   **To remove assets from a group:**

1.  Open the Select Assets window.

>   (Financial \>\>Transactions \>\> Fixed Assets \>\> Select Assets)

1.  Select a group.

2.  Choose Clear Group and then Yes.

3.  Close the window.

Chapter 9: Asset maintenance
----------------------------

>   You can change information for an asset or group of assets. Some fields are
>   depreciation-sensitive, which means that if you change the information in
>   that field, depreciation needs to be recalculated.

>   The following information is discussed:

-   *Changing asset information*

-   *Recalculating depreciation*

-   *Changing information for a group of assets*

-   *Deleting an asset book record*

-   *Calculating mid-quarter depreciation*

### Changing asset information

>   Use the Asset General Information window to make changes to information in
>   asset records and book records. You also can use this window to open other
>   windows and make changes in those windows. If you change the cost basis of
>   the asset, the Original Cost Basis field in the Asset Book ITC window will
>   be adjusted by the amount of the change.

>   **To change asset information:**

1.  Open the Asset General Information window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> General)

1.  Enter or select an asset ID and suffix.

2.  If the information to be changed is displayed in this window, enter the new
    field information and choose Save.

>   To change information in other windows, refer to the following table for
>   options:

| **Go To button option** | **Window that opens**  | **Additional information**                                             |
|-------------------------|------------------------|------------------------------------------------------------------------|
| Account                 | Asset Account window   | Refer to *Modifying an asset account record* for more information.     |
| Book                    | Asset Book window      | Refer to *Creating an asset book record* for more information.         |
| Insurance               | Asset Insurance window | Refer to *Creating an asset insurance record* for more information.    |
| Lease                   | Asset Lease window     | Refer to *Creating an asset lease record* for more information.        |
| User Data               | Asset User Data window | Refer to *Creating an asset user-defined record* for more information. |

1.  If you change the Class ID in the Asset General Information window, the
    Reset Asset Class ID window will be displayed when you choose Save.

![A screenshot of a cell phone Description automatically generated](media/fdf80d19a2a537a33e88a98526488d6c.jpg)

1.  To update depreciation information in the books that the asset is associated
    with, mark the Propagate option, select what type of update to perform, and
    choose OK.

>   *When you save changes to the Class ID in the Asset General Information
>   window, the accounts associated with the new Class ID are also applied to
>   the asset record. The changes are reflected in the Asset General Information
>   and the Asset Account windows for the affected asset, even if you make no
>   changes in the Reset Asset Class ID window.*

### Recalculating depreciation

>   When you make changes to specific fields in an asset book record,
>   depreciation is recalculated. The following fields affect depreciation:

-   Amortization Code

-   Amortization Amount

-   Averaging Convention

-   Cost Basis

-   Depreciation Method

-   Depreciated To Date

-   Life to Date Depreciation

-   Luxury Automobile

-   Original Life

-   Place in Service Date

-   Salvage Value

-   Switchover

-   Year to Date Depreciation

-   Special Depr Allowance

>   There are three ways depreciation can be recalculated:

>   **Reset Life** Recalculates depreciation from the date it was placed in
>   service through the date the asset already has been depreciated.
>   Depreciation adjustments will be made for each period, but the depreciation
>   does not have to be posted to General Ledger for each of these periods. You
>   can use the Fixed Assets General Ledger Posting window to select a range of
>   periods from the financial detail file, then post the entire amount to the
>   period of the transaction date.

>   **Reset Year** Calculates a new yearly depreciation rate and uses the new
>   rate to recalculate depreciation from the beginning of the current fiscal
>   year—defined in the Book Setup window—through the date the asset already has
>   been depreciated.

>   This depreciation does not have to be posted to General Ledger for each
>   period. You can use the Fixed Assets General Ledger Posting window to select
>   a range of periods from the financial detail file, then post the entire
>   amount to the period of the transaction date.

>   **Recalculate** Calculates a new yearly depreciation rate as of the
>   beginning of the current fiscal year defined in the Book Setup window.
>   However, calculations are not based on the new rate until the next time
>   depreciation is taken on the asset. The current year-to-date depreciation
>   amount is not affected. The difference between the new yearly rate and the
>   current year-to-date depreciation amount will be allocated over the
>   remaining time in the current fiscal year.

-   If an asset is in the first year of life (the Place in Service Date and
    Depreciated To

>   Date are in the same fiscal year), and a depreciation-sensitive field other
>   than Year-to-date Depreciation, Life-to-date Depreciation or Depreciated-to
>   Date changes, the new rates for depreciation will be recalculated.

-   If any of the following fields are changed—Year-to-date Depreciation,
    Life-todate Depreciation, or Depreciated-to Date—depreciation will be
    recalculated, unless the Depreciated-to Date is the last day of the year.

### Changing information for a group of assets

>   Use the Fixed Assets Mass Change window to change information for a group of
>   assets. You must use a separate mass change process to change each type of
>   asset record. For example, to change asset general information and asset
>   account information, you must complete two mass changes. If information for
>   an asset doesn’t exist, the mass change process will not create the
>   information. You also must build a new asset group before each mass change
>   process. Asset groups are built based on the assets on file when the group
>   is created. Refer to *Building an asset group* for more information.

>   The Fixed Assets Mass Change window has four tabs. You can refer to the
>   following information about the tabs when changing asset information:

>   **General** If you change the Asset Class ID, only the class ID in the Asset
>   General Information window will be changed. To change book class
>   information, such as depreciation characteristics, you also must make a mass
>   change for the asset group, using the Book tab.

>   **Account** You can select an account group. The accounts set up for that
>   account group will appear as default entries in the account fields in this
>   window. You can mark the accounts to change.

>   **Book** You can change book class information. All of the fields are
>   depreciationsensitive. When any depreciation-sensitive fields change, you
>   must indicate whether the changes should take effect from the date the asset
>   is currently depreciated (Recalc Remaining), as of the beginning of the
>   current fiscal year (Reset Year) or as of the Place in Service Date (Reset
>   Life). Refer to *Recalculating depreciation* for more information.

>   If you changed the Asset Class ID using the General tab, you also must make
>   a mass change for the asset group using the Book tab to change book class
>   information, such as depreciation characteristics.

>   **User** You can change any information for user-defined fields. You also
>   can select default values to be used.

>   **To change information for a group of assets:**

1.  Open the Fixed Assets Mass Change window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Mass Change)

![A screenshot of a cell phone Description automatically generated](media/5ad1bbc90ab556275d321b78853f2e9e.jpg)

1.  Select an asset group ID and choose a tab—General, Account, Book, User.

2.  Mark the fields to be changed and enter or select the new values.

3.  Choose Apply Changes to change the information.

4.  To make additional changes to this asset group, repeat steps 2 through 4 for
    each mass change.

5.  Choose OK to close the Mass Change window.

#### Deleting an asset book record

>   Use the Asset Book window to delete an asset book record. You also must make
>   General Ledger entries to reverse any cost or depreciation that has been
>   posted for this asset. For more information, refer to the General Ledger
>   documentation.

>   **To delete an asset book record:**

1.  Open the Asset Book window.

>   (Financial \>\> Cards \>\> Fixed Assets \>\> Book)

1.  Enter or select an asset ID and suffix.

2.  Enter or select a book and choose Delete. The book and all the financial
    detail of the book will be deleted.

#### Calculating mid-quarter depreciation

>   If more than 40% of the total cost of assets purchased during the current
>   year were purchased in the last quarter of the year, you must use the
>   mid-quarter averaging convention to calculate depreciation for US federal
>   income tax purposes for personal property placed in service that year. Print
>   the Mid-Quarter Applicability report to determine the total cost of assets
>   purchased each quarter of any year.

>   Use the Mass Change window to calculate mid-quarter depreciation. You must
>   create a group of assets purchased in the current fiscal year before you can
>   calculate mid-quarter depreciation. Refer to *Building an asset group* for
>   more information.

>   **To calculate mid-quarter depreciation:**

1.  Open the Mass Change window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Mass Change)

1.  Choose the Book tab and select an asset group ID.

2.  Enter or select the tax book in the Book ID field.

3.  Mark the Averaging Convention option and select Mid-Quarter.

4.  Select the Reset Life option.

5.  Choose Apply Changes.

**Chapter 10: Asset transfer**

>   You can transfer an asset or a group of assets to a new general ledger
>   account, property tax location, physical location, structure, or master
>   asset ID. You also can transfer an asset or a group of assets from one
>   company, the originating company, to a different company, the destination
>   company.

>   When you transfer an asset or group of assets, depreciation will be
>   calculated through the transfer date using the current account numbers.
>   Depreciation using the new account numbers will begin on the day after the
>   transfer date. If the transfer date is earlier than the date through which
>   the asset has been depreciated, depreciation will be backed out to the
>   transfer date using the current account numbers.

>   The following information is discussed:

-   *Transferring asset record information*

-   *Partial transfer options*

-   *Partially transferring an asset*

-   *Transferring multiple assets*

-   *Intercompany asset transfer process*

-   *Transferring an intercompany asset record information*

-   *Transferring multiple intercompany assets*

#### Transferring asset record information

>   Use the Transfer Maintenance window to transfer an asset to a new General
>   Ledger account, property tax location, physical location, structure, or
>   master asset ID for an individual asset.

>   **To transfer asset record information:**

1.  Open the Transfer Maintenance window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Transfer)

![A screenshot of a social media post Description automatically generated](media/e69adcfb3ad58150543d740adf8322a1.jpg)

1.  Enter or select an asset ID. Only active assets—assets that are not
    retired—can be transferred.

2.  Enter the transfer date. The transfer date must be in the current fiscal
    year.

3.  Enter or select the new asset information. Choose the G/L Accounts expansion
    button to open the Expand Transfer window and enter or select new account
    numbers. Do not delete account numbers that are not changing.

4.  Choose Transfer and verify the transfer results using the Transfer Inquiry,
    Asset Book Inquiry, or Financial Detail Inquiry windows. The Transfer Report
    can also be printed. A separate audit record that you can print is created
    each time an asset is transferred.

#### Partial transfer options

>   A partial transfer of an asset can be based on one of the following options:

>   **Quantity** The quantity to transfer. The transfer quantity will be divided
>   by the quantity in the Asset General Information record to determine a
>   transfer percentage. The percentage will be applied to all amount fields in
>   every asset record—asset general information, asset purchase, asset book,
>   asset book/ITC, asset lease, asset insurance, and asset user data—associated
>   with the asset you’re transferring. If the asset is being transferred to
>   more than one place, the total of all transfer quantity entries cannot
>   exceed the quantity in the Asset General Information window.

>   **Cost** The cost to transfer. The transfer cost must be equal to or less
>   than the cost on any book for the asset being transferred. The transfer cost
>   will reduce the cost of the corporate book record. A transfer percentage
>   will be calculated by dividing the transfer cost by the cost basis in the
>   corporate book. This percentage will be applied to all amount fields in
>   every asset record—asset general information, asset purchase, asset book,
>   asset book/ITC, asset lease, asset insurance, and asset user data—associated
>   with this asset. You can base a partial asset transfer on cost only if a
>   corporate book exists for the asset being transferred. Also, the total of
>   all transfer cost entries cannot exceed the cost basis on the book record
>   for any book for the asset being transferred.

>   **Percent** The percentage to transfer. The percentage will be applied to
>   all amount and quantity fields related to the asset. The total of all
>   transfer percentage entries cannot exceed 100%.

>   If you enter a combination of transfer quantity and transfer percentage, the
>   transfer percentage will be applied to each dollar field associated with the
>   asset being transferred. If you enter a transfer quantity and a transfer
>   percentage and the transfer percentage is not the same percentage that is
>   calculated by dividing quantity in the Asset General Information record by
>   the transfer quantity, the percentage you entered will be changed.

>   If you enter a combination of transfer quantity and transfer cost, the
>   transfer quantity will reduce the quantity in the Asset General Information
>   window and the transfer cost will be divided by the cost basis on the
>   corporate book.

>   Each line related to the partial transfer must have the same combination of
>   field entries. For example, if only transfer percentage is entered on one
>   line of the partial transfer, then only transfer percentage can be entered
>   on subsequent lines.

#### Partially transferring an asset

>   Use the Transfer Maintenance window to partially transfer an asset. You can
>   partially transfer an asset based on quantity, cost, or a percentage. After
>   you partially transfer an asset, a new asset is created with the same asset
>   ID as the original asset and an incremental suffix. To partially transfer an
>   intercompany asset, see *Transferring an intercompany asset record
>   information*.

>   Each line related to the partial transfer must have the same combination of
>   field entries. For example, if only transfer percentage is entered on one
>   line of the partial transfer, then only transfer percentage can be entered
>   on subsequent lines.

>   **To partially transfer an asset:**

1.  Open the Transfer Maintenance window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Transfer)

1.  Enter or select an asset ID. Only active assets—assets that are not
    retired—can be transferred.

2.  Enter the transfer date. The transfer date must be in or before the current
    fiscal year.

3.  Enter the partial transfer information. For more information, refer to
    *Partial transfer options*.

4.  You can enter or select new asset information, if necessary.

5.  Choose Transfer and verify the transfer results in the Transfer Inquiry,
    Asset Book Inquiry, or Financial Detail Inquiry windows.

#### Transferring multiple assets

>   Use the Fixed Assets Mass Transfer window to transfer a group of assets to a
>   different property tax location, physical location ID, structure ID, master
>   asset ID, or change General Ledger account numbers. Before you can transfer
>   a group of assets, you must first define an asset group in the Select Assets
>   window. Refer to *Building an asset group* for more information.

>   *Be sure to build a new asset group before each mass transfer. If you
>   transfer multiple assets for an existing asset group, it’s possible that not
>   all assets that you intend to transfer will be transferred.*

>   **To transfer multiple assets:**

1.  Open the Fixed Assets Mass Transfer window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Mass Transfer)

![A screenshot of a social media post Description automatically generated](media/206f00667ababf9b704c651e95c89385.jpg)

1.  Select an asset group ID.

2.  Enter the transfer date. The transfer date must be in the current fiscal
    year.

3.  Enter or select the new asset information.

4.  You can enter or select an account group ID to view the existing account
    numbers and enter or select new account numbers for the assets. The account
    numbers displayed when you choose Transfer will be used to update each asset
    being transferred.

5.  Choose Transfer.

6.  Close the Mass Transfer window.

#### Intercompany asset transfer process

>   During the intercompany transfer process, asset information is created in
>   the destination company’s Asset General Information window. Asset
>   information from the originating company’s Asset Insurance window, Asset
>   Lease window, and Asset User Data window is not transferred to the
>   destination company.

| **Asset General Information window**                                    |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Field**                                                               | **Value**                                                                                       |
| Asset ID                                                                | **The Mark to create a new asset ID for destination company option is marked.**                 |
| Description                                                             | The description entered in the originating company's Asset General Information window.          |
| **Asset General Information window**                                    |                                                                                                 |
| **Field**                                                               | **Value**                                                                                       |
| Extended Description                                                    | The extended description entered in the originating company's Asset General Information window. |
| Short Name                                                              | The short name entered in the originating company's Asset General Information window.           |
| Master Asset ID                                                         | The master asset ID entered in the Fixed Assets Intercompany Transfer window.                   |
| Status                                                                  | Active                                                                                          |
| Class ID                                                                | The class ID entered in the Fixed Assets Intercompany Transfer window.                          |
| Type                                                                    | The type selected in the originating company's Asset General Information window.                |
| Property Type                                                           | The property type selected in the originating company's Asset General Information window.       |
| Acquisition Date                                                        | **Transfer type is Like-Kind Exchange, Taxable Exchange, Sale, or Other.**                      |
| Acquisition Cost and the acquisition costs in the Asset Purchase window | The cost is determined by the currency ID and the transfer type.                                |
| Physical Location ID                                                    | The physical location ID entered in the Fixed Assets Intercompany Transfer window.              |
| Asset Label                                                             | The asset label entered in the originating company's Asset General Information window.          |
| Structure ID                                                            | The structure ID entered in the Fixed Assets Intercompany Transfer window.                      |
| Manufacturer Name                                                       | The manufacturer name entered in the originating company's Asset General Information window.    |
| Location ID                                                             | The location ID entered in the Fixed Assets Intercompany Transfer window.                       |
| Quantity                                                                | **Partial Transfer option unmarked.**                                                           |
| Date Added                                                              | The Microsoft Dynamics GP system date for the user.                                             |

>   The next asset ID from the destination company's Fixed Assets Company Setup
>   window is used to generate the new asset ID.

>   **The Mark to create a new asset ID for destination company option is
>   unmarked.**

>   If the asset ID in the originating company does not exist in the destination
>   company, the existing asset ID for the asset in the originating company is
>   used for the asset general record.

>   The acquisition date is the transfer date in the Fixed Assets Intercompany
>   Transfer window.

>   **Transfer type is Reset.**

>   The acquisition date is the acquisition date for the asset in the
>   originating company.

>   **Transfer type is Like-Kind Exchange, Taxable Exchange, Sale, or Other.**

>   The acquisition cost is the asset's net book value for the company's
>   corporate book as of the date entered as the transfer date.

>   **Transfer type is Reset.**

>   The acquisition cost is the acquisition cost for the asset in the
>   originating company.

>   The quantity is set to the quantity for the asset in the originating
>   company.

>   **Partial Transfer option marked and Quantity selected.**

>   The quantity is set to the quantity entered in the Fixed Assets Intercompany
>   Transfer window.

>   **Partial Transfer option marked and Cost selected.**

>   The quantity is set to the quantity for the asset in the originating company
>   multiplied by percentage entered in the Percent field in the Fixed Assets
>   Intercompany Transfer window.

>   **Book information**

>   If the class ID assigned in the Fixed Assets Intercompany Transfer window
>   has the Auto Add Book Info option marked in the Book Class Setup window,
>   book information is automatically created for the asset in the destination
>   company for each book.

>   **Asset Account window**

>   The accounts set up in the destination company for the Account Group ID
>   assigned to the asset in the Fixed Assets Intercompany Transfer window are
>   saved for the asset in the Asset Account window of the destination company.
>   The Account Group ID itself is not saved with the asset information. It is
>   used only for setting up and saving the accounts for the asset, and is then
>   cleared.

>   **Retirement process**

>   During the transfer process, the group of assets is automatically retired in
>   the originating company. Retiring an intercompany asset or asset group is
>   the same as retiring a group of assets in the Fixed Asset Mass Retirement
>   window or retiring an asset in the Retirement Maintenance window with the
>   following exceptions.

>   If the transfer type doesn't match a retirement type, the retirement type is
>   Other for the asset or a group of assets.

>   The transfer type determines the retirement date when an asset or a group of
>   assets. Review the following table.

| **Transfer type**  | **Retirement date**                                                |
|--------------------|--------------------------------------------------------------------|
| Like-Kind Exchange | Transfer date in the Fixed Asset Intercompany window               |
| Taxable Exchange   | Transfer date in the Fixed Asset Intercompany window               |
| Sale               | Transfer date in the Fixed Asset Intercompany window               |
| Other              | Transfer date in the Fixed Asset Intercompany window               |
| Reset              | Placed in Service date for each asset on the corporate book record |

>   For more information about retiring assets, see *Chapter 11, “Asset
>   retirement.”*

#### Transferring an intercompany asset record information

>   Use the Fixed Assets Intercompany Transfer window to transfer an asset from
>   the originating company to another company (the destination company). During
>   the transfer process, the asset is automatically retired in the originating
>   company. If you are using more than one instance of Microsoft Dynamics GP,
>   you can only transfer assets within the same instance of Microsoft Dynamics
>   GP.

>   **To transfer an intercompany asset record information:**

1.  Open the Fixed Assets Intercompany Transfer window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Intercompany Transfer)

![A screenshot of a cell phone Description automatically generated](media/9bf4342eddd1c0d2fe9204846fda0e92.jpg)

1.  Enter or select a company ID that the asset is being transferred to.

2.  Select Asset to transfer an individual asset.

3.  Enter or select an asset ID. Only active assets—assets that are not
    retired—can be transferred.

4.  Select a transfer type.

5.  Enter the transfer date. The transfer date must be in the current fiscal
    year.

6.  Mark Create new asset ID for destination company record if you have the Auto
    Generate Next Asset ID option marked in the Fixed Assets Company Setup
    window.

>   By automatically generating the next asset ID when you are transferring an
>   asset to a destination company, you can avoid duplication issues with the
>   existing asset IDs in the destination company. The next asset ID from the
>   destination company's Fixed Assets Company Setup window is used to generate
>   the new asset ID.

>   If the option is unmarked, the existing asset ID for the asset in the
>   originating company is used for the asset general record in the destination
>   company.

1.  Mark Partial Transfer if you want to partially transfer an asset. You can
    partially transfer an asset based on quantity, cost, or a percentage. For
    more information, refer to *Partial transfer options*.

>   When you partially transfer an asset, you are also partially retiring an
>   asset. For more information, refer to *Partial retirement options*.

1.  Enter or select the asset setup information for the destination company.

2.  Enter or select a currency ID if the currency is different from the
    functional currency ID.

3.  Enter or select the retirement information for asset in the originating
    company if the transfer type is Like-Kind Exchange, Taxable Exchange, Sale,
    or Other. When an asset record is retired, you must enter the proceeds and
    expenses related to the retirement of that asset.

>   **Cash proceeds** The monetary amount received for an asset when it was
>   sold.

>   **Non-cash proceeds** The monetary value of anything not in the form of cash
>   that you received for an asset, such as a similar asset you received in
>   exchange.

>   **Expenses of sale** The amount it cost you to sell an asset.

1.  Choose Transfer. The Fixed Assets Intercompany Transfer Report is printed.

>   Refer to *Intercompany asset transfer process* for more information.

#### Transferring multiple intercompany assets

>   Use the Fixed Assets Intercompany Transfer window to transfer a group of
>   assets to a different company (the destination company). During the transfer
>   process, the group of assets is automatically retired in the originating
>   company. If you are using more than one instance of Microsoft Dynamics GP,
>   you can only transfer assets within the same instance of Microsoft Dynamics
>   GP.

>   **To transfer multiple intercompany assets:**

1.  Open the Fixed Assets Intercompany Transfer window.

(Financial \>\> Transactions \>\> Fixed Assets \>\> Intercompany Transfer)

2. Enter or select a company ID that the asset group is being transferred to.

1.  Select Asset Group to transfer a group of assets.

2.  Select an asset group ID.

3.  Select a transfer type.

4.  Enter the transfer date. The transfer date must be in the current fiscal
    year.

5.  Mark Create new asset ID for destination company record if you have the Auto
    Generate Next Asset ID option marked in the Fixed Assets Company Setup
    window.

>   By automatically generating the next asset ID when you are transferring an a
>   group of assets to a destination company, you can avoid duplication issues
>   with the existing asset IDs in the destination company. The next asset ID
>   from the destination company's Fixed Assets Company Setup window is used to
>   generate the new asset IDs.

>   If the option is unmarked, the existing asset ID for each asset in the
>   originating company is used for the asset general record in the destination
>   company.

1.  Enter or select the asset setup information for the destination company.

2.  Enter or select a currency ID if the currency is different from the
    functional currency ID.

3.  Enter the cash proceeds, non-cash proceeds, and expenses of sale if the
    transfer type is Like-Kind Exchange, Taxable Exchange, Sale, or Other. These
    amounts will be used when retiring each asset in the asset group.

>   **Cash proceeds** The monetary amount received for an asset when it was
>   sold.

>   **Non-cash proceeds** The monetary value of anything not in the form of cash
>   that you received for an asset, such as a similar asset you received in
>   exchange. **Expenses of sale** The amount it cost you to sell an asset.

1.  Choose a spread option, or accept the default option if the transfer type is
    LikeKind Exchange, Taxable Exchange, Sale, or Other. Refer to *Using
    retirement spread options* for more information.

2.  Choose Transfer. The Fixed Assets Intercompany Transfer Report is printed.
    Refer to *Intercompany asset transfer process* for more information.

**Chapter 11: Asset retirement**

>   You can retire an asset, partially retire an asset, or retire a group of
>   assets. The retirement date you enter will be used to calculate the prorated
>   amount of depreciation allowed for each book for each asset based on the
>   averaging convention. Depreciation can be calculated forward or backward
>   from the depreciated-to date to the prorated retirement date based on the
>   rules for the averaging convention being used.

>   If you’re using Multicurrency Management and you select a currency ID
>   different than the functional currency defined for this company, the
>   functional currency will be used to calculate the cash proceeds, non-cash
>   proceeds, and expenses of sale, based on the exchange rate.

>   The following information is discussed:

-   *Retirement proceeds and expenses*

-   *Recording the sale or disposal of an asset*

-   *Partial retirement options*

-   *Partially retiring an asset*

-   *Reversing a retired asset record*

-   *Using retirement spread options*

-   *Recording the sale or retirement of a group of assets*

#### Retirement proceeds and expenses

>   When you retire an asset record using the Retirement Maintenance window, you
>   must enter the proceeds and expenses related to the retirement of that
>   asset. You can enter information in each of the following options:

>   **Cash proceeds** The dollar amount received for an asset when it was sold.

>   **Non-cash proceeds** The dollar value of anything not in the form of cash
>   that you received for an asset, such as a similar asset you received in
>   exchange.

>   **Expenses of sale** The amount it cost you to sell an asset.

>   After you retire an asset record, choose the Prorated Retire Date expansion
>   button in the Asset Book Inquiry window to view the gain/loss calculations.
>   The following gain/loss values will be calculated using the proceeds and
>   expense information, net book value, and retirement type for the asset:

| **Gain/Loss Method** | **Retirement** |
|----------------------|----------------|


>   **Type**

**Calculation**

| Realized Gain/Loss                                                              |                                                                               | Cash Proceeds + Non-Cash Proceeds -                                                                                        |   |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|---|
| Positive and less than or equal to Cash Proceeds                                | Like Kind Exchange                                                            | Recognized Gain/Loss will contain the amount calculated for Realized Gain/Loss                                             |   |
| Positive and greater than                                                       | Like Kind Exchange                                                            | Recognized Gain/Loss will contain the amount in Cash Proceeds and Non-                                                     |   |
| Realized Gain/Loss is negative                                                  | Like Kind Exchange                                                            | Non-Recognized Gain/Loss will contain the amount calculated for Realized Gain/Loss                                         |   |
| **Gain/Loss Method**                                                            | **Retirement**                                                                | **Calculation**                                                                                                            |   |
| Realized Gain/Loss is positive                                                  | Involuntary                                                                   | Non-Recognized Gain/Loss will contain the amount calculated for Realized Gain/Loss if books other than the corporate books |   |
| Calculation used in all other cases, and when the above conditions are not met. | Recognized Gain/Loss will contain the amount calculated in Realized Gain/Loss |                                                                                                                            |   |

>   Expenses of Sale - Net Book Value

>   Cash Proceeds

>   Recognized Gain/Loss is equal to Realized

>   Gain/Loss - Cash Proceeds

>   **Type**

>   Conversion

#### Recording the sale or disposal of an asset

>   Use the Retirement Maintenance window to record the sale or disposal of an
>   individual asset. The averaging convention for the asset will be used to
>   determine how much depreciation is allowed in the year of retirement. Gain
>   and loss are calculated for each book record, using the proceeds, expenses
>   of sale, and retirement type entered in the Retirement Maintenance window,
>   and the net book value displayed in the Asset Book window.

>   **To record the sale or disposal of an asset:**

1.  Open the Retirement Maintenance window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Retire)

![A screenshot of a cell phone Description automatically generated](media/b2db952a7218a96e908dccf09b4d67e6.jpg)

1.  Enter or select an asset ID and suffix. Only active assets can be retired.

2.  Enter a retirement date and select a retirement type to classify the
    disposal. The retirement type determines the classification of the gain and
    loss calculation as recognized or non-recognized.

3.  You can enter or select a retirement code to further describe the
    retirement.

4.  Enter the proceeds and expenses of sale, if any, related to the retirement
    of the asset.

5.  Choose Retire. You can view the results using the Retirement Inquiry, Asset
    Book Inquiry, or Financial Detail Inquiry windows.

#### Partial retirement options

>   A partial retirement of an asset can be based on one of the following
>   options:

>   **Quantity** The quantity to retire. A retirement percentage will be
>   calculated by dividing the retirement quantity by the quantity on the Asset
>   General Information record and then rounding. This percentage will be
>   applied to all dollar fields in every asset record—asset general
>   information, asset purchase, asset book, asset book ITC, asset lease, asset
>   insurance, and asset user data—associated with the asset you’re retiring. If
>   the asset is being retired in more than one piece, the total of all
>   retirement quantity entries cannot exceed the quantity in the Asset General
>   Information window.

>   **Cost** The retirement cost. The cost will be used to reduce the cost on
>   the corporate book record and must be less than the cost on the corporate
>   book record for the asset being retired. For each book record other than the
>   corporate book, a retirement percentage will be calculated by dividing the
>   retirement cost by the cost basis on the corporate book. This percentage
>   will be applied to all dollar fields in every asset record—asset general
>   information, asset purchase, asset book, asset book ITC, asset lease, asset
>   insurance, and asset user data—associated with this asset. You can base a
>   partial asset retirement on cost only if a corporate book exists for the
>   asset being retired. In addition, the total of all retirement cost entries
>   cannot exceed the cost basis on the any book for the asset being retired.

>   **Percent** The retirement percentage to be applied to all dollar fields
>   related to this asset. Each line related to the partial retirement must have
>   the same combination of field entries. For example, if only retirement
>   percentage is entered on the first line of a partial retirement, then only
>   retirement percentage can be entered on subsequent lines. The total of all
>   retirement percentage entries cannot exceed 100%.

>   If you enter a combination of retirement quantity and retirement percentage,
>   the retirement percentage will be applied to each dollar field associated
>   with the asset being retired. If you enter a retirement quantity and a
>   retirement percentage, and the percentage is not the same percentage that is
>   calculated by dividing the quantity in the asset general information record
>   by the retired quantity, the percentage you entered will be changed.

>   If you enter a combination of retirement quantity and a retirement cost, the
>   retirement quantity will reduce the quantity in the Asset General
>   Information window and the retirement cost will be divided by the cost basis
>   on the corporate book.

#### Partially retiring an asset

>   Use the Retirement Maintenance window to partially retire an asset. You can
>   base a partial retirement on quantity, cost, or a percentage of the asset.
>   After you partially retire an asset, a new asset record is created using the
>   same asset ID of the asset retired and an incremental suffix.

>   Each line related to the partial retirement must have the same combination
>   of field entries. For example, if only retirement percentage is entered on
>   one line of the partial retirement, only retirement percentages can be
>   entered on subsequent lines.

>   **To partially retire an asset:**

1.  Open the Retirement Maintenance window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Retire)

![A screenshot of a cell phone Description automatically generated](media/b2db952a7218a96e908dccf09b4d67e6.jpg)

1.  Enter or select an asset ID and suffix. Only active assets can be retired.

2.  Enter a retirement date and select a retirement type to classify the
    disposal. The retirement type determines the classification of the gain and
    loss calculation as recognized or non-recognized.

3.  You can enter or select a retirement code to further describe the
    retirement.

4.  Enter partial retirement information. Enter the proceeds and expenses of
    sale, if any, related to the retirement of the asset.

5.  Choose Retire. You can view the results using the Retirement Inquiry, Asset
    Book Inquiry, or Financial Detail Inquiry windows.

#### Reversing a retired asset record

>   Use the Retirement Undo window to reverse a retired asset record. You can
>   reactivate a retired asset record if an incorrect asset was retired or if
>   incorrect proceeds were entered. To reverse a partially retired asset, the
>   original asset must still be active. If the asset isn’t active, you must
>   reactivate it.

>   Reactivating the asset puts the asset back to its original state before it
>   was retired. Any financial detail records that were created as a result of
>   the retirement will be reversed.

>   **To reverse a retired asset record:**

1.  Open the Retirement Undo window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Retire Undo)

![A screenshot of a cell phone Description automatically generated](media/ff38ba2eb64e109c8d84c01b419507e9.jpg)

1.  Enter or select an asset ID and suffix. Only asset records that were retired
    during the current fiscal year can be reactivated.

2.  Choose Undo to reactivate the asset record.

#### Using retirement spread options

>   When you retire multiple asset records using the Fixed Assets Mass
>   Retirement window or the Fixed Assets Intercompany Transfer window, you must
>   select a spread option to account for cash proceeds, non-cash proceeds, and
>   expenses of sale. A spread accounts for the allocation of proceeds and
>   expenses of sale for selected assets when retiring those assets. You can
>   choose from the following four spread options:

>   **Use this amount for each asset** The amount entered in the Cash Proceeds,
>   Non-Cash Proceeds, and Expenses of Sale fields will be used when retiring
>   each asset.

>   **Average evenly over each asset** The amount entered in the Cash Proceeds,
>   Non-Cash Proceeds, and Expenses of Sale fields will be divided by the number
>   of assets in the asset group being mass-retired. This amount will be used to
>   retire each asset. If the amounts don’t divide evenly, any remainder will be
>   applied to the last asset in the asset group when it’s retired.

>   **As a percentage of corporate cost** The sum of the corporate cost for all
>   assets in the asset group being mass-retired will be calculated. The cost
>   basis of each asset in the group will be divided by this total to determine
>   its percentage of the total net book value. Each percentage or each asset
>   will be separately multiplied by the total amount in the Cash Proceeds,
>   Non-Cash Proceeds, and Expenses fields to determine the amount of each that
>   applies to this asset.

>   Suppose you enter the following values:

-   Cash Proceeds = \$3,000

-   Non-Cash proceeds = \$1,500

-   Expenses of Sale = \$500

>   In the asset group there are three assets:

-   Asset 1 corporate cost basis = \$5,000 • Asset 2 corporate cost basis =
    \$1,000

-   Asset 3 corporate cost basis = \$4,000

>   The total cost basis equals \$10,000, and the allocation for asset 1 is 50%
>   (\$5,000 ÷ \$10,000 = 50%). Therefore, the following amounts will be
>   allocated for asset 1:

-   Cash proceeds: \$3000 x 50% = \$1,500

-   Non-cash proceeds: \$1,500 x 50% = \$750

-   Expenses of sale: \$500 x 50% = \$250

>   **As a percentage of corporate net book value** The sum of the corporate net
>   book value for all assets in the asset group being mass-retired will be
>   calculated. The net book value of each asset in the group will be divided by
>   this total to determine its percentage of the total net book value. Each
>   percentage of each asset will be separately multiplied by the total amount
>   in the Cash Proceeds, Non-Cash Proceeds, and Expenses fields to determine
>   the amount of each that applies to this asset.

>   Suppose you enter the following values:

-   Cash Proceeds = \$2,000

-   Non-Cash proceeds = \$2,000

-   Expenses of Sale = \$3,000

>   In this asset group there are three assets:

-   Asset 1 corporate net book value = \$1,000

-   Asset 2 corporate net book value = \$4,000

-   Asset 3 corporate net book value =\$5,000

>   The total net book value equals \$10,000, and asset 1’s allocation is 10%
>   (\$1,000 ÷ \$10,000 = 10%). Therefore, the following amounts will be
>   allocated for asset 1:

-   Cash proceeds: \$2,000 x 10% = \$200

-   Non-cash proceeds: \$2,000 x 10% = \$200

-   Expenses of sale: \$3,000 x 10% = \$300

#### Recording the sale or retirement of a group of assets

>   Use the Fixed Assets Mass Retirement window to record the sale or disposal
>   of a group of assets. You must build a new asset group for each mass
>   retirement to ensure that all existing assets that meet the criteria
>   selected are included in the retirement. For more information, refer to
>   *Building an asset group*.

>   **To record the sale or retirement of a group of assets:**

1.  Open the Fixed Assets Mass Retirement window.

>   (Financial \>\> Transactions \>\> Fixed Assets \>\> Mass Retire)

![A screenshot of a cell phone Description automatically generated](media/e9da160473ecfcdd5f53745840b35a74.jpg)

1.  Select an asset group ID.

2.  Enter a retirement date and select a retirement type.

3.  You can enter or select a retirement code to describe why the assets are
    being retired.

4.  Enter or select a currency ID if the currency is different from the
    functional currency ID.

5.  Enter the cash proceeds, non-cash proceeds, and expenses of sale. These
    amounts will be used when retiring each asset in the asset group.

6.  Choose a spread option, or accept the default option. Refer to *Using
    retirement spread options* for more information.

7.  Choose Retire.

8.  Close the Fixed Assets Mass Retirement window.

**Chapter 12: Asset depreciation**

>   Depreciation is the allocation of the cost of an asset over a period of time
>   for accounting and tax purposes. You can calculate depreciation or a
>   projected depreciation amount for an individual asset, for a group of
>   assets, or for all assets.

>   For more information about various methods of depreciation and a description
>   of them, refer to *Depreciation methods and calculations*.

>   US tax luxury automobile limits are provided, as well as tables for ACRS
>   (Accelerated Cost Recovery System) personal property, ACRS real estate based
>   on the 175% declining balance method, ACRS real estate using modified
>   straight-line, ACRS low income housing, and ACRS foreign real property. For
>   MACRS (Modified Accelerated Cost Recovery System) depreciation, Microsoft
>   Dynamics GP uses formulas to calculate the depreciation. Use Publication 946
>   from the Internal Revenue Service to select the correct asset life, cost
>   basis, depreciation method, and averaging convention to calculate the
>   depreciation deduction for the asset class.

*Back up your Fixed Asset Management data before beginning any depreciation
process.*

>   The following information is discussed:

-   *Depreciating one asset*

-   *Depreciating assets in one or more books*

-   *Recalculating depreciation for an asset*

-   *Reversing depreciation for an asset*

-   *Reversing depreciation for a group of assets*

-   *Projecting depreciation for one asset*

-   *Projecting depreciation for assets in one or more books*

#### Depreciating one asset

>   Use the Depreciate Asset window to depreciate an asset in a book. You also
>   can recalculate depreciation, if necessary. The depreciation target date
>   must be within a fiscal year that is set up in the Fiscal Periods Setup
>   window and must be in the current fiscal year defined in the Book Setup
>   window.

>   Depreciation is calculated for each asset for each period included in the
>   depreciation process. In General Ledger, the depreciation expense account is
>   debited and the depreciation reserve account is credited.

>   **To depreciate one asset:**

1.  Open the Depreciate Asset window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Depreciate One Asset)

![A screenshot of a cell phone Description automatically generated](media/2f24ad1b3a17299e1b5671348915f6f5.jpg)

1.  Enter or select the asset ID and suffix of the asset to be depreciated.

2.  Enter the depreciation target date.

3.  Select a book and choose Depreciate.

#### Depreciating assets in one or more books

>   Use the Depreciation Process Information window to depreciate asset groups
>   in specific books or all assets set up in Fixed Asset Management. For more
>   information about asset groups, refer to *Building an asset group*.

>   The target date fiscal year must be set up in the Fixed Assets Fiscal
>   Periods file and can’t be later than the Current Fiscal Year entered in the
>   Book Setup window for every book selected to be depreciated.

>   Depreciation is calculated for each asset for each period included in the
>   depreciation process. In General Ledger, the depreciation expense account is
>   debited and the depreciation reserve account is credited.

>   **To depreciate assets in one or more books:**

1.  Open the Depreciation Process Information window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Depreciate)

![A screenshot of a cell phone Description automatically generated](media/9e58f558653df4e0b62bb55c117054f0.jpg)

1.  To depreciate an asset group, unmark Depreciate all assets and select an
    asset group ID. To depreciate all active assets—assets that are not fully
    depreciated— in the selected books, mark Depreciate all assets.

2.  Enter the depreciation target date. All active assets in this company that
    haven’t already been depreciated to the depreciation target date will be
    depreciated through this date.

3.  Select the books to be depreciated and choose Depreciate.

4.  Close the window.

#### Recalculating depreciation for an asset

>   Use the Depreciate Asset window to recalculate depreciation for an asset
>   when you don’t need to change a depreciation-sensitive field in the Asset
>   Book window for an asset.

>   **To recalculate depreciation for an asset:**

1.  Open the Depreciate Asset window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Depreciate One Asset)

1.  Enter or select an asset ID and suffix.

2.  Enter the depreciation target date. Do not enter a date to recalculate
    depreciation as of the first day of the current fiscal year (Reset Year) or
    as of the date the asset was placed in service (Reset Life).

3.  Select a book and choose Depreciate.

4.  Choose Reset Year to recalculate depreciation as of the first day of the
    Current Fiscal Year defined on the Book Setup.

>   Choose Reset Life to recalculate depreciation as of the Place in Service
>   Date of the asset.

>   Both Reset Year and Reset Life will recalculate depreciation forward to the
>   date through which the asset was previously depreciated. You can not enter a
>   depreciation target date when either of these two options is selected.

1.  Close the window.

#### Reversing depreciation for an asset

>   You can reverse depreciation for an asset by entering a target date that is
>   before the date through which the asset book has been depreciated. The
>   target date cannot be before the first day of the current fiscal year
>   defined in the Book Setup window for the book being depreciated.

>   Use the Depreciate Asset window to reverse depreciation for an asset.

>   **To reverse depreciation for an asset:**

1.  Open the Depreciate Asset window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Depreciate One Asset)

1.  Enter the asset ID and suffix of the asset to reverse depreciation for.

2.  Enter the depreciation target date. This date must be before the date
    through which the asset book has been depreciated.

3.  Select a book and choose Depreciate.

4.  Close the window.

#### Reversing depreciation for a group of assets

>   Use the Depreciation Process Information window to reverse depreciation for
>   a group of assets. You can reverse depreciation for a group of assets by
>   entering a target date that is before the date through which the asset book
>   has been depreciated. The target date cannot be before the first day of the
>   current fiscal year defined in the Book Setup window for the book being
>   depreciated.

>   **To reverse depreciation for a group of assets:**

1.  Open the Depreciation Process Information window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Depreciate)

1.  To depreciate all active assets—assets that are not fully depreciated—in the
    selected books, mark Depreciate all assets.

2.  Mark Reverse future depreciation.

3.  Enter the depreciation target date.

>   **The Reverse future depreciation option is not marked** If the

>   Depreciated To Date of an asset book record is less than the Depreciation
>   Target Date, then the asset book record is depreciated through the
>   Depreciation Target Date.

>   If the Depreciated To Date is greater than or equal to the Depreciation
>   Target Date, then asset is not depreciated.

>   **The Reverse future depreciation option is marked** If the Depreciated

>   To Date is less than the Depreciation Target Date, the depreciation for the
>   asset book record is backed out (reversed) to the Depreciation Target Date.
>   The Depreciated To Date for the asset book record is set to the Depreciation
>   Target Date.

>   If the Depreciated To Date is greater than the Depreciation Target Date, the
>   asset book record is depreciated forward through the Depreciation Target
>   Date, and the

>   If the Depreciated To Date is equal to the Depreciation Target Date, then
>   asset is not depreciated.

1.  Select the books to be depreciated and choose Depreciate.

2.  Close the window.

#### Projecting depreciation for one asset

>   You can calculate a projected depreciation amount without updating the asset
>   book or the financial detail tables. The calculations for depreciation
>   projections are identical to those for an actual depreciation; however, book
>   and financial detail information is not updated. A separate depreciation
>   amount is projected for each fiscal period projected. Because projected
>   depreciation amounts are saved by user ID, each user can project
>   depreciation without affecting another user’s depreciation projections.

>   Use the Depreciate Asset window to project depreciation for one asset in a
>   book. When the projection process is finished, you can print projection
>   reports or view projection information in an inquiry window.

>   **To project depreciation for one asset:**

1.  Open the Depreciate Asset window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Depreciate One Asset)

1.  Enter or select an asset ID and suffix.

2.  Enter the date to project depreciation through in the Depreciation
    Projection Target date field.

3.  Select a book and mark the Projection Only option.

4.  Choose Depreciate and close the window.

5.  View the information in the Projection Inquiry window. For more information,
    refer to *Viewing projected depreciation information*.

#### Projecting depreciation for assets in one or more books

>   Use the Depreciation Projection window to project depreciation for assets in
>   one or more books. We recommend that you project depreciation several years
>   forward for all books. You can print projection reports for specific years
>   or periods.

>   **To project depreciation for assets in one or more books:**

1.  Open the Depreciation Projection window.

>   (Microsoft Dynamics GP menu Routines \>\> Fixed Assets \>\> Projection)

![A screenshot of a cell phone Description automatically generated](media/ab1688b308ca9e6c00b0c80bddad65e0.jpg)

1.  To project depreciation for an asset group, unmark Project all assets and
    select an asset group ID. Otherwise, leave Project all assets marked to
    project depreciation for all assets.

>   For more information, refer to *Building an asset group*.

1.  Enter the date to project depreciation through in the Depreciation
    Projection Target date field.

2.  Select a book and choose Insert to move the book to the Selected Books list.

3.  Choose Projection and close the window.

4.  You can print projection reports or view the information in the Projection
    Inquiry window. For more information, refer to *Viewing projected
    depreciation information*.

**Part 4: Routines**

>   This part of the documentation provides information about procedures you can
>   use to calculate depreciation of your assets. It also includes information
>   about year-end processes you can use and how you can integrate Fixed Asset
>   Management with General Ledger.

>   This part includes the following information:

-   *Chapter 12, “Asset depreciation,”* explains how you can use various
    depreciation methods to calculate depreciation for an individual asset, for
    a group of assets, or for all the assets in one or more books. You also can
    project depreciation amounts without changing asset information.

-   *Chapter 13, “Year-end processes,”* describes the various routines you can
    use at the end of a fiscal year to close books and summarize and clear data.

-   *Chapter 14, “General Ledger integration,”* explains how to use a routine to
    integrate Fixed Asset Management data with General Ledger.

-   *Chapter 15, “Physical inventory,”* explains how to reconcile the actual
    physical location for an asset to the physical location ID entered for the
    asset. It also explains how to identify missing or misplaced assets by using
    the physical inventory reconciliation process.

**Chapter 13: Year-end processes**

>   You can close a Fixed Asset Management fiscal year to update depreciation
>   amounts, summarize financial data, and remove inactive asset record
>   information.

>   Once you’ve closed the fiscal year, you cannot print reports for the prior
>   year. You should print reports that include year-to-date depreciation for
>   your assets before closing the fiscal year. You also can maintain Fixed
>   Asset data tables by summarizing historical detail information, and deleting
>   inactive asset records when it is no longer necessary to store the
>   information.

>   Before you can close the fiscal year, you must complete the following tasks:

-   Enter all activity for the current fiscal year, including asset additions,
    changes, transfers, and retirements.

-   Process asset depreciation for the final period, through the last day, of
    the current fiscal year.

-   Post transactions to General Ledger.

-   Post the General Ledger batch.

-   Process year-to-date depreciation and print activity reports.

-   Make a backup of your data.

>   To close the fiscal year, you must close the asset books and verify data
>   after the books are closed.

>   You also can summarize financial detail data and delete inactive asset
>   records.

>   If the fiscal periods for the new year in the Microsoft Dynamics GP fiscal
>   calendar have been changed since the Fixed Asset Management calendar was
>   last built, you should rebuild the Fixed Asset Management fiscal calendar
>   for future years. You should do this only after you run the year-end
>   process.

>   The following information is discussed:

-   *Closing the asset books*

-   *Summarizing financial data*

-   *Deleting inactive asset information*

#### Closing the asset books

At the end of each fiscal year, you can update depreciation amounts. The
year-end routine increases the current fiscal year by one year for each book
that is being closed and changes the Year-to-Date Depreciation Amount and YTD
Maintenance Amount fields to zero. Also, the values in specific fields are
copied to other fields. The following fields are changed when you close your
asset books:

| **Window**    | **Field information is copied from** | **Field information is copied to** |
|---------------|--------------------------------------|------------------------------------|
| Asset Book    | Cost Basis                           | Begin Cost                         |
| Asset Book    | Life-to-Date Depreciation Amount     | Begin Reserve                      |
| Asset General | Quantity                             | Begin Quantity                     |
| Asset Book    | Salvage                              | Begin Salvage                      |

>   Information

*Back up your data before closing asset books.*

>   Before you begin, be sure that no other users are running any other
>   processes in Fixed Assets, such as depreciation. Users can use other modules
>   in Microsoft Dynamics GP while you are closing the asset books.

Use the Asset Year End window to process the year-end routine.

**To close the asset books:**

1.  Open the Asset Year End window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Year End)

![A screenshot of a cell phone Description automatically generated](media/c4f63110328c6a2ceee974c60c33b6da.jpg)

1.  Select each book to be closed and choose Insert.

2.  Choose Continue.

3.  Choose Continue again and close the window.

#### Summarizing financial data

>   You can summarize financial data by asset record, book record, transaction
>   account type, and specific periods at any time during the year. Summarizing
>   asset data frees up hard disk space and is typically done at the end of the
>   fiscal year. Once records have been summarized, you can no longer view
>   detailed information. Use the Asset Financial Detail Summarize window to
>   summarize financial data.

>   **To summarize financial data:**

1.  Open the Asset Financial Detail Summarize window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Summarize Financial)

![A screenshot of a cell phone Description automatically generated](media/18fafef9939e659be56a19f304574877.jpg)

1.  Enter the beginning and ending period ranges of records to be summarized.

2.  Choose OK and close the window. The Financial Detail Summary report will be
    printed.

#### Deleting inactive asset information

>   You can delete information for inactive—deleted, retired, or partially
>   open—assets. Deleting asset data frees up hard disk space and is typically
>   done at the end of the fiscal year. You should only delete data from a prior
>   year. Use the Asset Purge window to delete asset information.

>   **To delete inactive asset information:**

1.  Open the Asset Purge window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Purge)

![A screenshot of a cell phone Description automatically generated](media/754acad0fbe53e56805ee9fed0b7f34d.jpg)

1.  Enter the Purge Prior to Date. All information for inactive asset records
    with a retirement date or a delete date before this date will be deleted.

2.  Mark the asset statuses to delete asset records with those statuses.

3.  Choose Purge and then Continue. The FA Purge report will be printed.

**Chapter 14: General Ledger integration**

>   You can use a routine to integrate Fixed Asset Management data with General
>   Ledger. The Fixed Assets GL Posting routine creates a batch of
>   transactions—which includes one or more General Ledger journal entries,
>   depending on how posting is set up in the Fixed Assets Company Setup
>   window—that you can post to General Ledger. The batch number will have the
>   prefix FATRX, followed by a sequential number.

>   If you are not posting in detail, the General Ledger journal entry is in
>   summary format by General Ledger account numbers. All the asset records for
>   transactions are in the same journal entry. If you are posting in detail, a
>   General Ledger journal entry created for each Fixed Assets Management
>   transaction in the batch. You can select the data to post in the Fixed
>   Assets General Ledger Posting window.

>   Use the Fixed Assets to General Ledger Reconciliation report to reconcile
>   Fixed

>   Asset Management periodic activity to General Ledger. You can mark the Only
>   Not Posted option in the Activity Report Options window for this report to
>   view the Fixed Asset amounts that will be posted to General Ledger.

>   The following information is discussed:

-   *Migrating from another fixed assets system*

-   *Updating General Ledger with Fixed Asset Management transactions*

-   *Asset records—Require Asset Account option*

-   *Rebuilding integrated batches*

#### Migrating from another fixed assets system

>   After converting from another system—but before completely implementing
>   Fixed

>   Asset Management—we recommend that you mark the transactions already in
>   General Ledger as posted. Use the Fixed Assets General Ledger Posting window
>   to mark the transactions as posted.

**To migrate from another fixed assets system:**

1.  Open the Fixed Assets General Ledger Posting window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> GL Posting)

![A screenshot of a social media post Description automatically generated](media/165bf954276ccb5963c35dfb4f5c189a.jpg)

1.  Accept or enter a batch ID.

2.  Enter the posting date. This date will be displayed as the transaction date
    in the General Ledger journal voucher and will be used by General Ledger to
    determine the fiscal period these entries will be posted to.

3.  You can enter a reference to be displayed in the General Ledger Batch
    Transmittal and Transaction Entry windows.

4.  Select the type of range you want to include, and then enter restrictions
    for the range. You can insert a range of each type into the Restrictions
    list.

>   *If you selected Period as a type of range, we recommend that you enter
>   zeros in the From field. Then, enter the period you are balancing through in
>   the To Period field.*

1.  Choose Process to create a batch and to display the distributions for the
    transactions in scrolling window.

2.  Print the Fixed Assets Posting Edit List to verify the transactions in the
    batch.

3.  In the scrolling window, you can change the account. You also can change the
    distribution reference if you selected the Post in Detail option in the
    Fixed Asset Company Setup window.

4.  If you are not ready to post the batch, choose Save.

5.  If the asset ID, source document, or debit and credit amounts for the
    distributions are incorrect, delete the batch. Make the necessary changes to
    the assets and then create a new batch.

6.  If you are ready to post the batch, choose Post. A batch using the batch
    number assigned to this batch will be created in General Ledger. You can
    print the Fixed Assets Posting Journal report after the posting process is
    complete.

7.  If you’ve already posted these amounts in your previous fixed assets system,
    delete this batch from General Ledger. This will ensure that the data from
    that system will be identified as posted in Fixed Asset Management. For more
    information, refer to the General Ledger documentation.

>   As you finish transferring your data to Fixed Asset Management, you can
>   continue to use Period as your range type and enter zeros in the From field
>   and the current period in the To field. Using this set of dates, all current
>   period activity—along with any prior period adjustments—will be included
>   without doubling posted entries.

#### Updating General Ledger with Fixed Asset Management transactions

>   Use the Fixed Assets General Ledger Posting window to update General Ledger
>   with Fixed Asset Management transactions.

>   **To update General Ledger with Fixed Asset Management transactions:**

1.  Open the Fixed Assets General Ledger Posting window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> GL Posting)

![A screenshot of a social media post Description automatically generated](media/165bf954276ccb5963c35dfb4f5c189a.jpg)

1.  Accept or enter a batch ID.

2.  Enter the posting date. This date will be displayed as the transaction date
    in the General Ledger journal voucher and will be used by General Ledger to
    determine the fiscal period these entries will be posted to.

3.  You can enter a reference to be displayed in the General Ledger Batch
    Transmittal and Transaction Entry windows.

>   *The selected book ID will be appended to the comment field and updated in
>   the*

>   *Distribution Reference field for the General Ledger transaction in the
>   Transaction Entry window (Financial \>\> Transactions \>\> General).*

1.  Select the book ID to post the transactions assigned to the book to General
    Ledger. All book IDs for which you have marked the Post to General Ledger in
    the Book Setup window (Financial \>\> Setup \>\> Fixed Assets \>\> Book) are
    available for selection.

>   *The reporting ledger assigned to the book ID will be applied when you post
>   fixed assets transactions in General Ledger.*

1.  Select the type of range you want to include in the batch, and then enter
    restrictions for the range. You can insert a range of each type into the
    Restrictions list.

>   *If you selected Period as a type of range, we recommend that you enter
>   zeros for the beginning period to include any prior period adjustments that
>   have been made since the last time transactions were posted to General
>   Ledger.*

1.  Choose Process to create a batch and to display the distributions for the
    transactions in scrolling window.

2.  Print the Fixed Assets Posting Edit List to verify the transactions in the
    batch.

3.  In the scrolling window, you can change the account. You also can change the
    distribution reference if you selected the Post in Detail option in the
    Fixed Asset Company Setup window.

4.  If you are not ready to post the batch, choose Save. If the distributions
    are not correct, choose Delete.

5.  If you are ready to post the batch, choose Post. A batch using the batch
    number assigned to this batch will be created in General Ledger. You can
    print the Fixed Assets Posting Journal report after the posting process is
    complete. You also can reprint this report.

6.  You can edit or post this batch in General Ledger.

#### Asset records—Require Asset Account option

Before you create asset records or perform any maintenance on asset records, you
must mark Require Asset Account in the Fixed Assets Company Setup window to
ensure that all Fixed Asset Management transactions that are saved and added to
the Financial Detail table have a valid account number. You also must create an
asset account record before any book record can be saved for that asset.

For more information, refer to *Asset account option* and *Modifying an asset
account record*.

#### Rebuilding integrated batches

You might have to rebuild the integrated batches. If there are no batch IDs
displayed in the Batch Lookup window, use the Fixed Assets Reconcile window to
rebuild integrated batches.

>   **To rebuild integrated batches:**

1.  Open the Fixed Assets Reconcile window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Reconcile)

![A screenshot of a cell phone Description automatically generated](media/8146a6a0e42548ea452e717b78b05f81.jpg)

1.  Mark Create Batch Headers and choose Reconcile.

2.  After the FA Create Batch Headers report is printed, close the window

**Chapter 15: Physical inventory**

>   You can reconcile the actual physical location for an asset to the physical
>   location ID entered for the asset. You might determine the actual physical
>   location by using a bar-coding system. You also can identify missing or
>   misplaced assets by using the physical inventory reconciliation process.

>   To verify recorded assets actually exist, and are recorded in the correct
>   physical location, you should reconcile physical inventory. The following
>   information is discussed:

-   *Importing physical location IDs for existing assets*

-   *Creating an asset labels file*

-   *Reconciling physical locations for assets*

#### Importing physical location IDs for existing assets

>   Before you reconcile physical locations, asset records must have a physical
>   location ID and label. Use the Asset Import/Export window to import asset
>   label and physical location ID values from an external source, such as a bar
>   coding system.

>   The information to be imported must be in a comma- or tab-delimited format
>   and should contain the following fields:

| **Field**            | **Additional information**                                                                                                                                         |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Asset ID             | Required field                                                                                                                                                     |
| Asset Suffix         | Required field                                                                                                                                                     |
| Asset Label          | To enter a new value, enter up to 19 alphanumeric characters. To keep the current value in the asset general information record unchanged, leave this field blank. |
| Physical Location ID | To enter a new value, enter up to 15 alphanumeric characters. To keep the current value in the asset general information record unchanged, leave this field blank. |

>   **To import physical location IDs for existing assets:**

1.  Open the Asset Import/Export window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Asset Import/Export)

1.  Mark Export and select Asset ID & Suffix.

2.  Enter or find the name and location of the file to export the data to and
    select a character delimiter—comma or text.

3.  Choose Continue. The file that is created will contain the asset ID and
    suffix of every active asset that is set up in Fixed Asset Management.

4.  Using Microsoft Excel or Word, open the file containing the data you just
    exported. You can add the asset label and physical location ID information
    to the asset ID and suffix information to this file.

5.  In the Asset Import/Export window, mark Import and select Physical Inventory
    Info.

6.  Enter or find the location and name of the file to import and select a
    character delimiter.

7.  Choose Continue to import the physical location information. The FA Physical
    Inventory Information Import report will be printed.

#### Creating an asset labels file

Use the Asset Import/Export window to create a file with asset labels. These
labels can be printed in some form and attached to each asset as an identifier.
There is not a standard asset label report.

>   **To create an asset labels file:**

1.  Open the Asset Import/Export window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Asset Import/Export)

1.  Mark Export and select Asset Label.

2.  Enter or find the name and location of the file to export the data to and
    select a character delimiter—comma or text.

3.  Choose Continue to print asset labels to a file.

#### Reconciling physical locations for assets

You can import information from another source, such as a bar-code reader, into
Fixed Asset Management. The information must be in a comma- or tab-delimited
format and should contain the following information:

| **Field name**                                                                    | **Field type**                           |
|-----------------------------------------------------------------------------------|------------------------------------------|
| Physical Location ID                                                              | 15 string                                |
| Asset Label                                                                       | 19 string                                |
| Verified Date                                                                     | MMDDYY,MM/DD/YY, MMDDCCYY, OR MM/DD/CCYY |
| PIN\*                                                                             | 15 string                                |
| \*The PIN is a personal identifier of the person(s) doing the physical inventory. |                                          |

If the item data has been imported previously, but not reconciled yet, a message
will appear and you can choose one of the following options:

-   Delete all

-   Replace duplicates

-   Add new items only

Discrepancies in the Fixed Assets Inventory file can be corrected using the
Physical Inventory window. Discrepancies in the recorded value can be corrected
on the asset card, or automatically—if the discrepancies are large—by creating
an asset group, then entering a mass-change transaction to correct all the
discrepancies at once.

Use the Missing Physical Inventory and Misplaced Physical Inventory windows to
view assets that are considered missing or misplaced in Fixed Asset Management.

**Missing** Indicates assets with a recorded asset label were not found in the
physical inventory.

>   **Misplaced** Indicates one of the following situations has occurred:

-   The physical location in the fixed assets system is different from the
    inventoried asset, including no recorded physical location.

-   The inventoried asset is not recorded in the fixed assets system.

-   The inventoried asset is not active—it is retired or partially open.

>   **To reconcile physical locations for assets:**

1.  Open the Physical Inventory window.

>   (Financial \>\> Routines \>\> Fixed Assets \>\> Physical Inventory)

![A screenshot of a social media post Description automatically generated](media/656309992364cbd8cbf41295a0d1ea0c.jpg)

1.  Select All Locations or enter or select a specific physical location ID.

2.  Enter the physical inventory information—asset label, PIN, and verified
    date— manually or choose Import to update the Fixed Assets Inventory File.

3.  Choose Missing to open the Missing Physical Inventory window. Choose
    Misplaced to open the Misplaced Physical Inventory window.

4.  Choose Create Group to open the Create Group window and enter a new group
    name.

5.  Choose Create to add the missing or misplaced assets to the new group.

6.  Choose OK to close the Missing Physical Inventory window or the Misplaced
    Physical Inventory window.

7.  Choose Update to update inventory information in the asset general
    information record and Physical Location ID Setup record.

>   The Verified Date and PIN will be saved to each reconciled general
>   information record for each reconciled asset. Only items that haven’t been
>   reconciled will remain in the imported file after the update is complete.

1.  Close the Physical Inventory window.

**Part 5: Utilities and detail file activity**

>   This part of the documentation provides information about maintaining the
>   integrity of your Fixed Asset Management data by reconciling your records
>   and maintaining the Fixed Asset Management data tables.

>   This part includes the following information:

-   *Chapter 16, “Table maintenance,”* explains how to minimize the risk of
    damage to your data and to quickly recover your data from damage if it
    occurs.

-   *Chapter 17, “Financial detail file activity,”* provides the financial
    information relating to Fixed Asset Management activities.

**Chapter 16: Table maintenance**

>   You should reconcile asset records if you discover inconsistencies in
>   reports or if a system problem occurs and you need to verify that your Fixed
>   Asset Management data is accurate.

>   You can delete asset records entered incorrectly or remove detail for an
>   asset. You also can delete specific detail for items that have an unapplied
>   amount equal to zero.

*Be sure to back up your data before completing any of these procedures.*

>   The following information is discussed:

-   *Reconciling asset information*

-   *Deleting an asset*

-   *Deleting fixed assets purchasing transactions*

-   *Removing batch history*

#### Reconciling asset information

>   Use the Fixed Assets Reconcile window to reconcile asset information and
>   book ITC records. You can insert account numbers in any account that was
>   left blank at the asset level and update any blank account with the
>   corresponding default accounts entered in the Fixed Assets Company Setup
>   window. You also can verify that each book ITC record has a Net Cost Basis
>   equal to the Cost Basis in the asset book record.

>   You can update or verify your asset data using one of the following
>   reconciliation processes:

>   **Asset accounts** Verifies that there are no blank account numbers in any
>   asset account records. If there are blank accounts, default accounts
>   selected in the Fixed Assets Company Setup window will be saved to the asset
>   account record.

>   **Asset labels** Updates blank asset label fields. If a blank asset label
>   field exists in a asset general information record, the asset ID and suffix
>   will be saved to the Asset Label field.

>   **Book ITC** Forces the net cost basis in the Book/ITC record to be in
>   balance with the cost basis in the Asset Book record. Only asset books that
>   have a Book/ITC record will be reconciled.

>   **Create batch headers** Creates a list of fixed assets general ledger batch
>   numbers (FATRX) to use for reprinting the FA Posting to General Ledger
>   report.

>   **Custodians** Creates a list of assets with a custodian in the Asset
>   General Information record, but the custodian is not also in the employee
>   record.

*Be sure to back up your data before completing any of these procedures.*

>   **To reconcile asset information:**

1.  Open the Fixed Assets Reconcile window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Reconcile)

1.  Mark Asset Accounts to update asset account information.

2.  Mark Asset Labels to update blank asset label fields.

3.  Mark Book ITC to update asset book cost basis information.

4.  Mark Create Batch Header to create a list of fixed assets general ledger
    batch numbers.

5.  Mark Custodians to create a list of assets without a custodian in the
    employee record.

6.  Choose Reconcile and then choose OK. You can print a report for each process
    to view the asset records that were updated.

#### Deleting an asset

Use the Asset Delete Utility window to delete an asset record and all associated
records. You should delete an asset only when the asset has been entered
incorrectly. Before you delete an asset, be sure that an unposted batch does not
exist for the asset. If an unposted batch exists, you must delete or post the
batch before you can delete the asset.

>   *Use this utility with caution. Your books could become out of balance if
>   the asset book monetary amounts that are already posted in General Ledger
>   are deleted from the Fixed Assets Financial Detail File.*

There is no audit trail for the deleted asset, although the Asset Delete Report
will be printed.

If you’ve already used the General Ledger integration process to post monetary
amounts for an asset, you must make manual General Ledger entries to reverse the
cost and year-to-date depreciation for the asset you’re deleting.

**To delete an asset:**

1.  Open the Asset Delete Utility window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Delete)

![A screenshot of a cell phone Description automatically generated](media/3436f0bba96f592e6e00998d90138b21.jpg)

1.  Enter an asset ID to delete.

>   Choose Delete to delete the asset and print the Fixed Asset Delete report.
>   You can refer to this report when making manual adjustments to the General
>   Ledger.

#### Deleting fixed assets purchasing transactions

>   Use the FA Purchasing Trxs Purge window to delete transactions that asset
>   records have been created from. You also can remove specific information for
>   each asset in the Fixed Assets Purchasing Transactions window using this
>   window.

>   You also can use the FA Purchasing Trxs Purge window to delete transactions
>   that have an unapplied amount equal to zero. If an unapplied amount is not
>   equal to zero, the transaction will not be deleted.

>   **To delete fixed assets purchasing transactions:**

1.  Open the FA Purchasing Trxs Purge window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Purge Purchasing
>   Transactions)

![A screenshot of a cell phone Description automatically generated](media/f0d83e4dc84accbe2575c41d786061be.jpg)

1.  Enter or select control numbers to specify the range of data to delete.

2.  Choose OK.

#### Removing batch history

>   Use the Remove Fixed Assets Batch History window to remove batch history.
>   You also can print the Batch History Removal report.

>   **To remove journal history:**

1.  Open the Remove Fixed Assets Batch History window.

>   (Financial \>\> Utilities \>\> Fixed Assets \>\> Remove Batch History)

1.  Select an option and enter a range restriction.

2.  Choose Insert; the range restriction is displayed in the Restrictions list.

>   You can enter only one restriction for each restriction type. For instance,
>   if you enter a restriction specifying that only batch IDs 100 through 300
>   should be removed, you can’t enter another restriction for batch IDs 500
>   through 800. To clear multiple ranges of history, you must clear each range
>   separately.

1.  Mark Remove Batches when you’re ready to remove history.

2.  Mark Print Report to print the Batch History Removal report after history is
    removed. To print the report without removing history, unmark Remove Batches
    and choose Process.

3.  Choose Process to begin removing history.

**Chapter 17: Financial detail file activity**

>   The Financial Detail File contains financial information relating to the
>   many Fixed Asset Management activities. For example, records are added to
>   this file when you add, depreciate, retire, or transfer an asset. When you
>   change fields related to depreciation calculations, records also are written
>   to this file. The following is a table reference to the Financial Detail
>   File and is organized by type of activity.

>   The following information is discussed:

-   *Activity table abbreviations and descriptions*

-   *Activity table for adding a record*

-   *Activity table for changing a record*

-   *Activity table for mass changes to records*

-   *Activity table for deleting a record*

-   *Activity table for depreciating a record*

-   *Activity detail for transferring a record*

-   *Activity table for mass transfer of records*

-   *Activity table for retiring a record*

-   *Activity detail for mass retiring records*

-   *Activity detail for unretiring records*

#### Activity table abbreviations and descriptions

>   You can use the Financial Detail Inquiry window to view most of the
>   information contained in the following activity tables. Use the following
>   table to view descriptions of abbreviations in the activity tables.

| **Abbreviation** | **Description**              |
|------------------|------------------------------|
| (+)              | Debit                        |
| (-)              | Credit                       |
| BO               | Backout Date                 |
| DTD              | Depreciated To Date          |
| FDCY             | First Day of Currency Year   |
| FDPY             | First Day of Prior Year      |
| FPCY             | First Period of Current Year |
| LDPY             | Last Day of Prior Year       |
| LPPY             | Last Period of Prior Year    |
| PIS              | Place in Service Date        |
| PRD              | Prorated Retire Date         |
| ORIG             | Same as in Original Record   |
| PDTD             | Period Depreciated To Date   |
| TD               | Transfer Date                |

#### Activity table for adding a record

>   When you add an asset record to Fixed Asset Management, specific accounts
>   are debited and credited. Refer to the following table for the effect on the
>   asset accounts.

| **Account**                                                                         | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
|-------------------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|-------------------------|
| Cost                                                                                | (+)                   | Current                  | FAADD          | DTD               | PIS                       | DTD                     |
| Clearing                                                                            | (-)                   | Current                  | FAADD          | DTD               | PIS                       | DTD                     |
| **If life-to-date depreciation is entered (for portion pertaining to prior years)** |                       |                          |                |                   |                           |                         |
| Prior Year                                                                          | (+)                   | Current                  | FAADD          | earlier of DTD or | PIS                       | earlier of DTD or       |
| Depreciation                                                                        | (-)                   | Current                  | FAADD          | earlier of DTD or | PIS                       | earlier of DTD or       |
| **If year-to-date depreciation is entered**                                         |                       |                          |                |                   |                           |                         |
| Depreciation                                                                        | (+)                   | Current                  | FAADD          | DTD               | FDCY (Book                | DTD                     |
| Depreciation                                                                        | (-)                   | Current                  | FAADD          | DTD               | FDCY (Book                | DTD                     |

>   Depreciation

>   LPPY

>   LPPY

>   Reserve

>   LPPY

>   LPPY

>   Expense

>   Setup window)

>   Reserve

>   Setup window)

#### Activity table for changing a record

>   When you change information in an asset record, specific accounts are
>   debited and credited. Refer to the following table for the effect on the
>   asset accounts.

| **Account**                                                                                                  | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
|--------------------------------------------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|------------------------------|
| **If cost is increased**                                                                                     |                       |                          |                |                   |                           |                              |
| Cost                                                                                                         | (+)                   | Current                  | FACHG          | DTD               | PIS                       | DTD                          |
| Clearing                                                                                                     | (-)                   | Current                  | FACHG          | DTD               | PIS                       | DTD                          |
| **If cost is decreased**                                                                                     |                       |                          |                |                   |                           |                              |
| Cost                                                                                                         | (-)                   | Current                  | FACHG          | DTD               | PIS                       | DTD                          |
| Clearing                                                                                                     | (+)                   | Current                  | FACHG          | DTD               | PIS                       | DTD                          |
| **If life-to-date depreciation is increased without changing year-to-date depreciation**                     |                       |                          |                |                   |                           |                              |
| Prior Year                                                                                                   | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| Depreciation                                                                                                 | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If life-to-date depreciation is decreased without changing year-to-date depreciation**                     |                       |                          |                |                   |                           |                              |
| Prior Year                                                                                                   | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| Depreciation                                                                                                 | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If year-to-date depreciation is increased and life-to-date depreciation is increased by the same amount**  |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                 | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                 | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| **If year-to-date depreciation is increased and life-to-date depreciation is increased by a smaller amount** |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                 | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                 | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |

>   Depreciation

>   Reserve

>   Depreciation

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

| **Account**                                                                                                                         | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|------------------------------|
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| Prior Year                                                                                                                          | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If year-to-date depreciation is increased and life-to-date depreciation is increased by a greater amount**                        |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Prior Year                                                                                                                          | (+)                   | Current                  | FACHG          | LPPY              | FDCY                      | LDPY                         |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If year-to-date depreciation is increased and life-to-date depreciation is decreased or not changed**                             |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| Prior Year                                                                                                                          | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If year-to-date depreciation is increased and life-to-date depreciation is decreased by the same amount**                         |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| **If year-to-date depreciation is decreased and life-to-date depreciation is decreased by a smaller amount**                        |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Prior Year                                                                                                                          | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If year-to-date depreciation is decreased and life-to-date depreciation is decreased by a greater amount**                        |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| Prior Year                                                                                                                          | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **If year-to-date depreciation is decreased and life-to-date deprecation is increased or does not change**                          |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | DTD               | FDCY                      | DTD                          |
| Prior Year                                                                                                                          | (+)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **Account**                                                                                                                         | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG          | LPPY              | PIS                       | LDPY                         |
| **Reset Year (Backout)**                                                                                                            |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG-R        | ORIG              | ORIG or BO+1              | ORIG                         |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG-R        | ORIG              | ORIG or BO+1              | ORIG                         |
| **Reset Year (Re-depreciate)** When reset life is processed, the two reset year options are processed after the reset life options. |                       |                          |                |                   |                           |                              |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG-R        | PDTD              | OLD PDTD+1                | PDTD                         |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG-R        | PDTD              | OLD PDTD+1                | PDTD                         |
| **Reset Life (Backout)**                                                                                                            |                       |                          |                |                   |                           |                              |
| Prior Year                                                                                                                          | (-)                   | Current                  | FACHG-R        | LPPY              | PIS                       | LDPY                         |
| Depreciation                                                                                                                        | (+)                   | Current                  | FACHG-R        | LPPY              | PIS                       | LDPY                         |
| **Reset Life (Re-depreciate)**                                                                                                      |                       |                          |                |                   |                           |                              |
| Prior Year                                                                                                                          | (+)                   | Current                  | FACHG-R        | PDTD              | OLD PDTD+1                | PDTD                         |
| Depreciation                                                                                                                        | (-)                   | Current                  | FACHG-R        | PDTD              | OLD PDTD+1                | PDTD                         |

>   Reserve

>   Expense

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Expense

>   Expense

>   Reserve

>   Expense

>   Expense

>   Expense

>   Reserve

>   Expense

>   Expense

>   Expense

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Depreciation

>   Reserve

>   Depreciation

>   Reserve

#### Activity table for mass changes to records

>   When you change a group of asset records, specific accounts are debited and
>   credited. Refer to the following table for the effect on the asset accounts.

| **Account**                                                                                                                        | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|-------------------------|
| **Reset Year (Backout)**                                                                                                           |                       |                          |                |                   |                           |                         |
| Deprecation                                                                                                                        | (-)                   | Current                  | FAMCH-R        | ORIG              | ORIG or BO+1              | ORIG                    |
| Depreciation                                                                                                                       | (+)                   | Current                  | FAMCH-R        | ORIG              | ORIG or BO+1              | ORIG                    |
| **Reset Year (Re-Depreciate)**                                                                                                     |                       |                          |                |                   |                           |                         |
| Depreciation                                                                                                                       | (+)                   | Current                  | FAMCH-R        | PDTD              | OLD PDTD+1                | PDTD                    |
| Depreciation                                                                                                                       | (-)                   | Current                  | FAMCH-R        | PDTD              | OLD PDTD+1                | PDTD                    |
| **Reset Life (Backout)**                                                                                                           |                       |                          |                |                   |                           |                         |
| Prior Year                                                                                                                         | (-)                   | Current                  | FAMCH-R        | LPPY              | PIS                       | LDPY                    |
| Deprecation                                                                                                                        | (+)                   | Current                  | FAMCH-R        | LPPY              | PIS                       | LDPY                    |
| **Reset Life (Re-Depreciate)** When reset life is processed, the two reset year options are processed after the reset life options |                       |                          |                |                   |                           |                         |
| Prior Year                                                                                                                         | (+)                   | Current                  | FAMCH-R        | PDTD              | OLD PDTD+1                | PDTD                    |
| Deprecation                                                                                                                        | (-)                   | Current                  | FAMCH-R        | PDTD              | OLD PDTD+1                | PDTD                    |

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Depreciation

>   Reserve

>   Depreciation

>   Reserve

#### Activity table for deleting a record

>   When you delete an asset record, financial records won’t be created. You
>   must debit and credit specific General Ledger accounts. Refer to the
>   following table for the effect on the asset accounts.

| **Account**  | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
|--------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|-------------------------|
| Cost         | (-)                   | Current                  | FADLT          | DTD               | PIS                       | DTD                     |
| Clearing     | (+)                   | Current                  | FADLT          | DTD               | PIS                       | DTD                     |
| Depreciation | (-)                   | Current                  | FADLT          | ORIG              | ORIG                      | ORIG                    |
| Depreciation | (+)                   | Current                  | FADLT          | ORIG              | ORIG                      | ORIG                    |

>   Expense

>   Reserve

#### Activity table for depreciating a record

>   When you process depreciation for an asset record, specific accounts are
>   debited and credited. Refer to the following table for the effect on the
>   asset accounts.

| **Account**                                                                                                                        | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|-------------------------|
| Depreciation                                                                                                                       | (+)                   | Current                  | FADEP          | PDTD              | OLD PDTD+1                | PDTD                    |
| Depreciation                                                                                                                       | (-)                   | Current                  | FADEP          | PDTD              | OLD PDTD+1                | PDTD                    |
| **Depreciate one asset (if a target date is entered that is earlier than the depreciated to date)**                                |                       |                          |                |                   |                           |                         |
| Depreciation                                                                                                                       | (-)                   | Current                  | FADEP-O        | ORIG              | ORIG or BO+1              | ORIG                    |
| Depreciation                                                                                                                       | (+)                   | Current                  | FADEP-O        | ORIG              | ORIG or BO+1              | ORIG                    |
| **Depreciate one asset (if a target date is entered that is later than the depreciated to date)**                                  |                       |                          |                |                   |                           |                         |
| Depreciation                                                                                                                       | (+)                   | Current                  | FADEP-O        | PDTD              | OLD PDTD+1                | PDTD                    |
| Depreciation                                                                                                                       | (-)                   | Current                  | FADEP-O        | PDTD              | OLD PDTD+1                | PDTD                    |
| **Reset Year (Backout)**                                                                                                           |                       |                          |                |                   |                           |                         |
| Depreciation                                                                                                                       | (-)                   | Current                  | FADEP-R        | ORIG              | ORIG or BO+1              | ORIG                    |
| Depreciation                                                                                                                       | (+)                   | Current                  | FADEP-R        | ORIG              | ORIG or BO+1              | ORIG                    |
| **Reset Year (Re-Depreciate)**                                                                                                     |                       |                          |                |                   |                           |                         |
| Depreciation                                                                                                                       | (+)                   | Current                  | FADEP-R        | PDTD              | OLD PDTD+1                | PDTD                    |
| Depreciation                                                                                                                       | (-)                   | Current                  | FADEP-R        | PDTD              | OLD PDTD+1                | PDTD                    |
| **Reset Life (Backout)**                                                                                                           |                       |                          |                |                   |                           |                         |
| Prior Year                                                                                                                         | (-)                   | Current                  | FADEP-R        | LPPY              | PIS                       | LDPY                    |
| Depreciation                                                                                                                       | (+)                   | Current                  | FADEP-R        | LPPY              | PIS                       | LDPY                    |
| **Reset Life (Re-Depreciate)** When reset life is processed, the two reset year options are processed after the reset life options |                       |                          |                |                   |                           |                         |
| Prior Year                                                                                                                         | (+)                   | Current                  | FADEP-R        | PDTD              | OLD PDTD+1                | PDTD                    |
| **Account**                                                                                                                        | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
| Depreciation Reserve                                                                                                               | (-)                   | Current                  | FADEP-R        | PDTD              | OLD PDTD+1                | PDTD                    |

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Depreciation

>   Reserve

>   Depreciation

#### Activity detail for transferring a record

>   When you transfer an asset record, specific accounts are debited and
>   credited. Refer to the following table for the effect on the asset accounts.

| **Account**                                                                            | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
|----------------------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|-------------------------|
| **If transfer is later than the depreciated to date**                                  |                       |                          |                |                   |                           |                         |
| Depreciation                                                                           | (+)                   | Current                  | FAXFR          | PDTD              | OLD PDTD+1                | PDTD                    |
| Depreciation                                                                           | (-)                   | Current                  | FAXFR          | PDTD              | OLD PDTD+1                | PDTD                    |
| **If transfer is earlier than the depreciated to date**                                |                       |                          |                |                   |                           |                         |
| Depreciation                                                                           | (-)                   | Current                  | FAXFR          | ORIG              | ORIG or BO+1              | ORIG                    |
| Depreciation                                                                           | (+)                   | Current                  | FAXFR          | ORIG              | ORIG or BO+1              | ORIG                    |
| **Partial Transfer (transferring partial to new asset records) Creating “TO” asset**   |                       |                          |                |                   |                           |                         |
| Cost                                                                                   | (+)                   | Current                  | FAXFR-P        | DTD               | PIS                       | DTD                     |
| Clearing                                                                               | (-)                   | Current                  | FAXFR-P        | DTD               | PIS                       | DTD                     |
| Depreciation                                                                           | (+)                   | Current                  | FAXFR-P        | DTD               | PIS or FDCY               | DTD                     |
| Depreciation                                                                           | (-)                   | Current                  | FAXFR-P        | DTD               | PIS or FDCY               | DTD                     |
| Prior Year                                                                             | (+)                   | Current                  | FAXFR-P        | LPPY              | PIS                       | LDPY                    |
| Depreciation                                                                           | (-)                   | Current                  | FAXFR-P        | LPPY              | PIS                       | LDPY                    |
| **Partial Transfer (transferring partial to new asset records) Reducing “FROM” asset** |                       |                          |                |                   |                           |                         |
| Cost                                                                                   | (-)                   | Current                  | FAXFR-P        | DTD               | PIS                       | DTD                     |
| Clearing                                                                               | (+)                   | Current                  | FAXFR-P        | DTD               | PIS                       | DTD                     |
| Depreciation                                                                           | (-)                   | Current                  | FAXFR-P        | DTD               | PIS or FDCY               | DTD                     |
| Depreciation                                                                           | (+)                   | Current                  | FAXFR-P        | DTD               | PIS or FDCY               | DTD                     |
| Prior Year                                                                             | (-)                   | Current                  | FAXFR-P        | LPPY              | PIS                       | LDPY                    |
| Depreciation                                                                           | (+)                   | Current                  | FAXFR-P        | LPPY              | PIS                       | LDPY                    |
| **Cost/Reserve (transferring cost/reserve to new accounts)**                           |                       |                          |                |                   |                           |                         |
| Cost (To asset account)                                                                | (+)                   | Current                  | FAXFR-C        | TD                | PIS                       | TD                      |
| Cost (From asset account)                                                              | (-)                   | Current                  | FAXFR-C        | TD                | PIS                       | TD                      |
| Depreciation Reserve (From asset account)                                              | (+)                   | Current                  | FAXFR-C        | TD                | PIS                       | TD                      |
| **Account**                                                                            | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
| Depreciation Reserve (To asset account)                                                | (-)                   | Current                  | FAXFR-C        | TD                | PIS                       | TD                      |

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Depreciation

>   Reserve

>   Expense

>   Reserve

>   Depreciation

>   Reserve

#### Activity table for mass transfer of records

>   When you transfer a group of asset records, specific accounts are debited
>   and credited. Refer to the following table for the effect on the asset
>   accounts.

| **Account**                                                  | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated to date** |
|--------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|-------------------------|
| **If transfer is later than the depreciated to date**        |                       |                          |                |                   |                           |                         |
| Depreciation                                                 | (+)                   | Current                  | FAMXF          | PDTD              | OLD PDTD+1                | PDTD                    |
| Depreciation                                                 | (-)                   | Current                  | FAMXF          | PDTD              | OLD PDTD+1                | PDTD                    |
| **If transfer is earlier than the depreciated to date**      |                       |                          |                |                   |                           |                         |
| Depreciation                                                 | (-)                   | Current                  | FAMXF          | ORIG              | ORIG or BO+1              | ORIG                    |
| Depreciation                                                 | (+)                   | Current                  | FAMXF          | ORIG              | ORIG or BO+1              | ORIG                    |
| **Cost/Reserve (transferring cost/reserve to new accounts)** |                       |                          |                |                   |                           |                         |
| Cost (To asset account)                                      | (+)                   | Current                  | FAMXF-C        | TD                | PIS                       | TD                      |
| Cost (From asset account)                                    | (-)                   | Current                  | FAMXF-C        | TD                | PIS                       | TD                      |
| Depreciation Reserve (From asset account)                    | (+)                   | Current                  | FAMXF-C        | TD                | PIS                       | TD                      |
| Depreciation Reserve (To asset account)                      | (-)                   | Current                  | FAMXF-C        | TD                | PIS                       | TD                      |

>   Expense

>   Reserve

>   Expense

>   Reserve

#### Activity table for retiring a record

>   When you retire an asset, specific accounts are debited and credited. Refer
>   to the following table for the effect on the asset accounts.

| **Account**                                                          | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
|----------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|------------------------------|
| **PARTIAL RETIREMENT**                                               |                       |                          |                |                   |                           |                              |
| **Creating new records to be retired**                               |                       |                          |                |                   |                           |                              |
| Cost                                                                 | (+)                   | Current                  | FARET-P        | DTD               | PIS                       | DTD                          |
| Clearing                                                             | (-)                   | Current                  | FARET-P        | DTD               | PIS                       | DTD                          |
| Depreciation                                                         | (+)                   | Current                  | FARET-P        | DTD               | PIS or FDCY               | DTD                          |
| Depreciation                                                         | (-)                   | Current                  | FARET-P        | DTD               | PIS or FDCY               | DTD                          |
| Prior Year                                                           | (+)                   | Current                  | FARET-P        | LPPY              | PIS                       | DPY                          |
| Depreciation                                                         | (-)                   | Current                  | FARET-P        | LPPY              | PIS                       | LDPY                         |
| **Account**                                                          | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
| **Reducing original asset**                                          |                       |                          |                |                   |                           |                              |
| Cost                                                                 | (-)                   | Current                  | FARET-P        | DTD               | DTD                       | DTD                          |
| Clearing                                                             | (+)                   | Current                  | FARET-P        | DTD               | DTD                       | DTD                          |
| Depreciation                                                         | (-)                   | Current                  | FARET-P        | DTD               | PIS or FDCY               | DTD                          |
| Depreciation                                                         | (+)                   | Current                  | FARET-P        | DTD               | PIS or FDCY               | DTD                          |
| Prior Year                                                           | (-)                   | Current                  | FARET-P        | LPPY              | PIS                       | LDPY                         |
| Depreciation                                                         | (+)                   | Current                  | FARET-P        | LPPY              | PIS                       | LDPY                         |
| **FULL OR PARTIAL RETIREMENT**                                       |                       |                          |                |                   |                           |                              |
| **If prorated retire date is later than the depreciated to date**    |                       |                          |                |                   |                           |                              |
| Depreciation                                                         | (+)                   | Current                  | FARET          | PDTD              | OLD PDTD+1                | PDTD                         |
| Depreciation                                                         | (-)                   | Current                  | FARET          | PDTD              | OLD PDTD+1                | PDTD                         |
| **If prorated retired date is earlier than the depreciated to date** |                       |                          |                |                   |                           |                              |
| Depreciation                                                         | (-)                   | Current                  | FARET          | ORIG              | ORIG or BO+1              | ORIG                         |
| Depreciation                                                         | (+)                   | Current                  | FARET          | ORIG              | ORIG or BO+1              | ORIG                         |
| Prior Year                                                           | (-)                   | Current                  | FARET          | PRD               | PRD+1                     | LDPY                         |
| **Cost, Accumulated Depreciation, Proceeds, Gain/Loss**              |                       |                          |                |                   |                           |                              |
| Cost                                                                 | (-)                   | Current                  | FARET          | PRD               | PIS                       | PRD                          |
| Depreciation                                                         | (+)                   | Current                  | FARET          | PRD               | PIS                       | PRD                          |
| Non-Recognized                                                       | (-) Gain              |                          |                |                   |                           |                              |
|                                                                      | (+) Loss              | Current                  | FARET          | PRD               | PIS                       | PRD                          |
| Recognized Gain                                                      | (-) Gain              |                          |                |                   |                           |                              |
|                                                                      | (+) Loss              | Current                  | FARET          | PRD               | PIS                       | PRD                          |
| Proceeds (Cash                                                       | (+)                   | Current                  | FARET          | PRD               | PIS                       | PRD                          |

>   Expense

>   Reserve

>   Depreciation

>   Reserve

>   Expense

>   Reserve

>   Depreciation

>   Reserve

>   Expense

>   Reserve

>   Expense

>   Reserve

>   Depreciation (if Retire Date is a prior year)

>   Reserve

>   Gain

>   Proceeds + NonCash Proceeds - Expenses of Sale)

| **Account**                                                         | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
|---------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|------------------------------|
| **If prorated retire date is later than the depreciated to date**   |                       |                          |                |                   |                           |                              |
| Depreciation Expense                                                | (+)                   | Current                  | FAMRT          | PDTD              | OLD PDTD+1                | PDTD                         |
| Depreciation Reserve                                                | (-)                   | Current                  | FAMRT          | PDTD              | OLD PDTD+1                | PDTD                         |
| **If prorated retire date is earlier than the depreciated to date** |                       |                          |                |                   |                           |                              |

#### Activity detail for mass retiring records

>   When you retire a group of asset records, specific accounts are debited and
>   credited. Refer to the following table for the effect on the asset accounts.

| **Account**     | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
|-----------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|------------------------------|
| Depreciation    | (-)                   | Current                  | FAMRT          | ORIG              | ORIG or BO+1              | ORIG                         |
| Depreciation    | (+)                   | Current                  | FAMRT          | ORIG              | ORIG or BO+1              | ORIG                         |
| Prior Year      | (-)                   | Current                  | FAMRT          | PRD               | PRD+1                     | LDPV                         |
| **Cost,**       |                       |                          |                |                   |                           |                              |
| Cost            | (-)                   | Current                  | FAMRT          | PRD               | PIS                       | PRD                          |
| Depreciation    | (+)                   | Current                  | FAMRT          | PRD               | PIS                       | PRD                          |
| Non-Recognized  | (-) Gain              |                          |                |                   |                           |                              |
|                 | (+) Loss              | Current                  | FAMRT          | PRD               | PIS                       | PRD                          |
| Recognized Gain | (-) Gain              |                          |                |                   |                           |                              |
|                 | (+) Loss              | Current                  | FAMRT          | PRD               | PIS                       | PRD                          |

>   Expense

>   Reserve

>   Depreciation (If Retire Date is in a prior year)

>   **Accumulated**

>   **Depreciation,**

>   **Proceeds, Gain/**

>   **Loss**

>   Reserve

>   Gain

#### Activity detail for unretiring records

>   When you undo an asset retirement, specific accounts are debited and
>   credited. Refer to the following table for the effect on the asset accounts.

| **Account**                                                               | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
|---------------------------------------------------------------------------|-----------------------|--------------------------|----------------|-------------------|---------------------------|------------------------------|
| **Partial Retirement Undo**                                               |                       |                          |                |                   |                           |                              |
| **Offsetting the effect of the new retired record that has been created** |                       |                          |                |                   |                           |                              |
| Cost                                                                      | (-)                   | Current                  | FARET-PU       | DTD               | PIS                       | DTD                          |
| Clearing                                                                  | (+)                   | Current                  | FARET-PU       | DTD               | PIS                       | DTD                          |
| Depreciation Expense                                                      | (-)                   | Current                  | FARET-PU       | DTD               | PIS or FDCY               | DTD                          |
| Depreciation Reserve                                                      | (+)                   | Current                  | FARET-PU       | DTD               | PIS or FDCY               | DTD                          |
| Prior Year Depreciation                                                   | (-)                   | Current                  | FARET-PU       | LPPY              | PIS                       | LDPY                         |
| Depreciation Reserve                                                      | (+)                   | Current                  | FARET-PU       | LPPY              | PIS                       | LDPY                         |
| **Adding back to original asset**                                         |                       |                          |                |                   |                           |                              |
| Cost                                                                      | (+)                   | Current                  | FARET-PU       | DTD               | PIS                       | DTD                          |
| Clearing                                                                  | (-)                   | Current                  | FARET-PU       | DTD               | PIS                       | DTD                          |
| Depreciation Expense                                                      | (+)                   | Current                  | FARET-PU       | DTD               | PIS or FDCY               | DTD                          |
| Depreciation Reserve                                                      | (-)                   | Current                  | FARET-PU       | DTD               | PIS or FDCY               | DTD                          |
| Prior Year Depreciation                                                   | (+)                   | Current                  | FARET-PU       | LPPY              | PIS                       | LPPY                         |
| Depreciation Reserve                                                      | (-)                   | Current                  | FARET-PU       | LPPY              | PIS                       | LPPY                         |
| **Full or Partial Retirement**                                            |                       |                          |                |                   |                           |                              |
| **Account**                                                               | **Effect on account** | **Fiscal year affected** | **Source doc** | **Fiscal period** | **Depreciated from date** | **Depreciated through date** |
| **If prorated retire date was later than the depreciated to date**        |                       |                          |                |                   |                           |                              |
| Depreciation Expense                                                      | (-)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Depreciation Reserve                                                      | (+)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| **If prorated retire date was earlier than the depreciated to date**      |                       |                          |                |                   |                           |                              |
| Depreciation Expense                                                      | (+)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Depreciation Reserve                                                      | (-)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Prior Year Depreciation (If Retire Date was in a prior year)              | (+)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| **Cost, Accumulated Depreciation, Proceeds, Gain/Loss**                   |                       |                          |                |                   |                           |                              |
| Cost                                                                      | (+)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Depreciation Reserve                                                      | (-)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Non-Recognized Gain                                                       | (+) Gain              |                          |                |                   |                           |                              |
|                                                                           | (-) Loss              | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Recognized Gain                                                           | (+) Gain              |                          |                |                   |                           |                              |
|                                                                           | (-) Loss              | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |
| Proceeds (Cash Proceeds + NonCash Proceeds - Expenses of Sale)            | (-)                   | Current                  | FARET-U        | ORIG              | ORIG                      | ORIG                         |

**Part 6: Inquiries and reports**

>   This part of the documentation provides information about viewing and
>   printing Fixed Asset Management data and analyzing asset activity by
>   printing specific reports.

>   This part includes the following information:

-   *Chapter 18, “Inquiries,”* explains how to view asset information, including
    financial information.

-   *Chapter 19, “Reports,”* explains how to create report options and print
    Fixed Asset Management reports to display specific data.

**Chapter 18: Inquiries**

>   You can use the Fixed Asset Management inquiry windows to review asset
>   information and financial information for an asset. You also can view
>   additional information from the Asset Book Inquiry, Book Compare Inquiry,
>   and Financial Detail Inquiry windows by clicking links to open other
>   windows.

>   You can print inquiry reports by choosing File \>\> Print in each inquiry
>   window, or by choosing the printer icon button.

>   The following information is discussed:

-   *Viewing asset information*

-   *Viewing asset book information*

-   *Comparing asset books*

| **Go To button option** | **Window that opens**                         |
|-------------------------|-----------------------------------------------|
| General                 | Asset General Inquiry window                  |
| Maint/Manuf             | Asset Maintenance/Manufacturer Inquiry window |
| Purchase                | Asset Purchase Inquiry window                 |
| Account                 | Asset Account Inquiry window                  |
| Insurance               | Asset Insurance Inquiry window                |
| Lease                   | Asset Lease Inquiry window                    |
| User Data               | Asset User Data Inquiry window                |

-   *Viewing financial detail information*

-   *Viewing asset retirement information*

-   *Viewing the error log*

-   *Viewing transfer information*

-   *Viewing projected depreciation information*

-   *Viewing purchasing transactions information*

-   *Viewing batch information*

-   *General Ledger inquiries*

#### Viewing asset information

>   Use the Asset Inquiry and Asset General Inquiry windows to view specific
>   information about an asset that does not directly relate to depreciation,
>   such as the asset description, class ID, quantity, and property type.

>   From the Asset Inquiry window, use the Go To button to open the following
>   windows:

>   **To view asset information:**

1.  Open the Asset Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> General)

![A screenshot of a cell phone Description automatically generated](media/3a66fe4e229e5ee73f7b0c2b9f9b648b.jpg)

1.  Enter or select an asset ID. Select one of the following options from the Go
    To button:

>   **Maint/Manuf** Opens the Asset Maintenance/Manufacturer Inquiry window,
>   where you can view asset maintenance and manufacturer information that was
>   entered in the Asset General Information window and the Expand Manufacturer
>   Name window.

>   **Purchase** Opens the Asset Purchase Inquiry window, where you can view
>   information that was entered in the Asset General Information window, such
>   as vendor ID, and purchase order number. If the acquisition of the asset
>   originated in Payables Management or Purchase Order Processing, additional
>   information might be displayed. Click the Voucher/Receipt Number link to
>   view the originating window.

>   **Account** Opens the Asset Account Inquiry window, where you can view the
>   account information that was entered in the Asset Account window.

>   **Insurance** Opens the Asset Insurance Inquiry window, where you can view
>   insurance class, replacement cost, and depreciated reproduction cost
>   information that was entered in the Asset Insurance window.

>   **Lease** Opens the Asset Lease Inquiry window, where you can view the lease
>   company ID, lease type, and interest rate information that was entered in
>   the Asset Lease window.

>   **User Data** Opens the Asset User Data Inquiry window, where you can view
>   user-defined information that was entered in the Asset User Data window.

1.  Close the Asset Inquiry window.

#### Viewing asset book information

>   Use the Asset Book Inquiry and Asset Book ITC Inquiry windows to view
>   depreciation information and asset values, such as the cost basis of the
>   asset, salvage value, and net book value.

>   To view detail transactions for a specific value of an asset, you can open
>   the Financial Detail Inquiry window by clicking on the Cost Basis, YTD
>   Depreciation, and YTD Depreciation links.

>   **To view asset book information:**

1.  Open the Asset Book Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Book)

![A screenshot of a cell phone Description automatically generated](media/8572f29c8e16c05c22943c96d3783b59.jpg)

1.  Enter or select an asset ID, suffix, and book ID.

2.  Choose the ITC/Cost button to open the Asset Book ITC Inquiry window.

![A screenshot of a cell phone Description automatically generated](media/320c60cd99f471ce882b8ddfcf356260.jpg)

1.  Choose OK to close the Asset Book ITC Inquiry window.

2.  Choose OK to close the Asset Book Inquiry window.

#### Comparing asset books

>   Use the Book Compare Inquiry window to compare depreciation characteristics
>   and depreciation balances for up to three books for an asset. This is useful
>   to see the difference in the depreciation values calculated using different
>   rules. You also can open the Asset Book Inquiry and the Financial Detail
>   Inquiry windows from this window.

>   **To compare asset books:**

1.  Open the Book Compare Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Book Compare)

![A screenshot of a cell phone Description automatically generated](media/7e914fd63b1df729bb7a6b95ba0d84d1.jpg)

1.  Enter or select an asset ID and suffix.

2.  Select up to three books—one book for each column.

3.  Choose the Book button for each book to open the Asset Book Inquiry window.

4.  Choose the Financial button for each book to open the Financial Detail
    Inquiry window. For more information, refer to *Viewing financial detail
    information*.

5.  Choose OK in the Book Compare Inquiry window to close the window.

#### Viewing financial detail information

>   Use the Financial Detail Inquiry window to view the financial detail records
>   for an asset, such as the fiscal period, batch ID, transaction account and
>   date, source document, and amount. These records include information about
>   an asset that has been added, changed, depreciated, retired, or transferred.
>   You can view specific information by selecting options to restrict the
>   information.

>   To view additional information for each transaction, you can click on the
>   Amount link to open the Financial Detail Display window. You also can open
>   the Financial Detail Inquiry window by clicking the Cost Basis link in the
>   Asset Book Inquiry and Asset Book Compare windows.

>   **To view financial detail information:**

1.  Open the Financial Detail Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Financial Detail)

1.  Enter or select an asset ID and suffix and select a book ID.

2.  Select a sorting option at the bottom of the window.

3.  To restrict the information displayed in this window, select the appropriate
    sorting option and then select one or more of the following options:

>   **Period filter** Displays only records for the specified Fixed Asset
>   Management period. To view all records for a year, enter zeros for the
>   period. This field is in the format YYYY- PPP, where Y is a year and P is a
>   period.

>   **GL Batch \# filter** Displays only those records that are included in the
>   batch number you enter.

>   **Transaction Account Type filters** Displays only records with a certain
>   transaction account type or all transaction account types. If you mark more
>   than one transaction account type filter, assets will be displayed for each
>   type. Mark All Types to include all asset records, regardless of their
>   transaction account type. Choose Redisplay.

>   **Source Doc. filters** Displays only records with the source document you
>   select. If you mark more than one source document filter, assets will be
>   displayed for each type. Mark All Documents to include all asset records,
>   regardless of their source document. Choose Redisplay.

>   **Include Reset Amounts** Displays each depreciation transaction taken for
>   an asset in closed years and its offsetting transaction. Unmark to display
>   the transaction that has the current depreciation amount taken for the
>   period.

1.  Select a transaction and click the Amount link to open the Financial Detail
    Display window.

![A screenshot of a cell phone Description automatically generated](media/64821a8bc52bafabc7a5a786c836055f.jpg)

1.  Choose OK to close the Financial Detail Display window.

2.  Choose OK in the Financial Detail Inquiry window.

#### Viewing asset retirement information

>   Use the Retirement Display window to view the cash proceeds, non-cash
>   proceeds, expenses of sale, and information related to the retirement of a
>   asset.

>   **To view asset retirement information:**

1.  Open the Retirement Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Retirement)

1.  Enter or select an asset ID and suffix. If the asset was partially retired,
    more than one line might be displayed.

2.  Select a line and click the Event link to open the Retirement Display
    window.

![A screenshot of a cell phone Description automatically generated](media/0c102faa3134445c7e5bf58a553c34ad.jpg)

1.  Choose OK to close the window.

#### Viewing the error log

>   Use the Error Log Inquiry window to determine the type of problem that has
>   occurred. When a problem occurs during a process, information is displayed
>   in the Error Log Inquiry window describing the process occurring at the time
>   of the problem and possibly listing the table and record where the problem
>   occurred. View this information before you call technical support.

>   **To view the error log:**

1.  Open the Error Log Inquiry window:

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Error Log)

![A screenshot of a social media post Description automatically generated](media/8cbf3a868c089264aff8f6e18d9985ea.jpg)

1.  Enter the date to view the messages for.

2.  Choose Print to print the FA Error Log Listing report.

3.  Choose Cancel to close the window.

#### Viewing transfer information

>   Use the Transfer Display window to view information about an asset
>   transferred from one asset ID, location ID, physical location ID, master
>   asset ID, structure ID, or account number to another. You also can view the
>   date and time of the transfer and any partial transfer information. If an
>   asset was part of an intercompany transfer, the destination company ID
>   displays for the asset.

>   **To view transfer information:**

1.  Open the Transfer Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Transfer)

1.  Enter or select an asset ID and suffix.

2.  Select a line and click the Event link to open the Transfer Display window.

![A screenshot of a computer Description automatically generated](media/8c6ba733494e3634200f9fe78de4d147.jpg)

1.  If the asset was transferred more than once, or if there were partial
    transfers, more than one line might be displayed in the Transfer Inquiry
    window.

#### Viewing projected depreciation information

>   Use the Projections Inquiry window to view projected depreciation for an
>   asset. You must first complete a depreciation projection for the asset. For
>   more information, see *Projecting depreciation for assets in one or more
>   books* or *Projecting depreciation for one asset*.

>   **To view projected depreciation information:**

1.  Open the Projections Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Projections)

![A screenshot of a cell phone Description automatically generated](media/3a85f5a83d6ab820bfaa257559ffaf1b.jpg)

1.  Enter or select an asset ID and suffix and select a book ID.

2.  Select Annual Projection to view the annual depreciation amounts. Select
    Period Projection to view the periodic depreciation amounts.

3.  Select the range of years—and periods, if applicable.

4.  Choose OK to close the window.

#### Viewing purchasing transactions information

>   Use the Fixed Assets Purchasing Transactions Inquiry window to view
>   transactions originating in Purchase Order Processing or Payables
>   Management. You can view transaction information such as the purchase order
>   number, document date and number, originating amount, and transaction
>   source. Only transactions that haven’t been added as assets or haven’t been
>   fully applied as assets will be displayed in this window.

>   **To view the purchasing transactions information:**

1.  Open the Fixed Assets Purchasing Transactions Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Purchasing Transactions)

![A screenshot of a cell phone Description automatically generated](media/903bacba284286994ac3f6cb32959714.jpg)

1.  Select a transaction.

    -   Click the Vendor ID link to open the Vendor Inquiry window.

    -   Click the Voucher/Receipt No. link to display the original purchasing
        transaction.

    -   Click the Amount link to open the Fixed Assets Purchasing Transaction
        Display window and view the information that will be used to create an
        asset record.

2.  Choose OK in the Fixed Assets Purchasing Transactions Inquiry window to
    close the window.

#### Viewing batch information

>   Use the Fixed Assets Batch Inquiry window to view posted Fixed Assets
>   batches.

>   **To view the batch information:**

1.  Open the Fixed Assets Batch Inquiry window.

>   (Financial \>\> Inquiry \>\> Fixed Assets \>\> Batches)

![A screenshot of a social media post Description automatically generated](media/b83875b0ef233fc083ea4ee8292cd32f.jpg)

1.  Select a batch ID and then select a row in the scrolling window.

    -   Click the Asset ID link to open the Asset Book Inquiry window.

    -   Click the Source Doc link to open the Financial Detail Display window.

    -   Click the Account link to open the Account Maintenance window.

2.  Choose OK in the Fixed Assets Batch Inquiry window to close the window.

#### General Ledger inquiries

>   By clicking links in specific General Ledger inquiry windows, you can open
>   additional windows and view details of the Fixed Asset Management
>   transactions that were posted to General Ledger. Details include account
>   information, the transaction date, and the amount of the transaction. The
>   following table lists the windows displayed by clicking on the links. To
>   open certain windows, the transaction you select must have originated in
>   Fixed Asset Management; the source document must be FA.

| **In this window**            | **Click this link** | **Window displayed**                      |
|-------------------------------|---------------------|-------------------------------------------|
| Detail Inquiry window         | Journal Entry       | Transaction Entry Zoom window             |
| History Detail Inquiry        | Journal Entry       | Transaction Entry Zoom window             |
| Transaction Entry Zoom window | Source Document     | Fixed Assets - General Ledger Zoom window |
| Journal Entry Inquiry window  | Source Document     | Fixed Assets - General Ledger Zoom window |
| Fixed Assets - General        | Asset ID            | Asset General Inquiry window              |
|                               | Amount              | Financial Detail Display window           |

>   window

>   Ledger Zoom window

**Chapter 19: Reports**

>   You can use Fixed Asset Management reports to analyze asset activity and
>   identify errors in transaction entry. You also can use reports to organize
>   necessary information for financial, tax, and other regulatory reporting
>   requirements.

>   Use this information to guide you through printing reports and working with
>   report options.

>   The following information is discussed:

-   *Fixed Asset Management reports summary*

-   *Report destinations and formats*

-   *Processing reports on a process server*

-   *Creating report options*

-   *Printing a report with an option*

-   *Customizing a report*

-   *Fixed Asset Management Microsoft SQL® Server Reporting Services reports*

#### Fixed Asset Management reports summary

>   Some Fixed Asset Management reports are printed automatically when you
>   complete certain procedures. For example, the Asset Delete report is printed
>   when you delete an asset. You can choose to print reports in some windows by
>   choosing File \>\> Print or the printer icon.

>   To print some reports, such as analysis or history reports, you must set up
>   report options specifying sorting options and ranges of information to
>   include on the report. For more information, see *Creating report options*.

>   The following table lists the report types available in Fixed Asset
>   Management and the reports in those categories.

| **Report type** | **Reports**                          | **Printing methods**                                                      |
|-----------------|--------------------------------------|---------------------------------------------------------------------------|
| Setup           | Fixed Assets Account Group Setup     | Choose File \>\> Print in the Setup window or choose the printer icon.    |
| Activity        | Annual Activity Annual Activity Cost | Create report options in the Fixed Assets Activity Report options window. |

>   Fixed Assets Book Setup

>   Fixed Assets Book Class Setup

>   Fixed Assets Insurance Setup

>   Fixed Assets Class Setup

>   Fixed Assets Company Setup

>   Fixed Assets Lease Company Setup

>   Fixed Assets Physical Location Setup

>   Fixed Assets Purchasing Posting Accounts Setup

>   Fixed Assets Quarter Setup

>   Fixed Assets Retirement Setup

>   Fixed Assets Structure Setup

>   User Fields List Setup

>   Basis Report

>   Detail Activity

>   Mid-Quarter Applicability

>   Fixed Assets to General Ledger Reconciliation - Detail

>   Fixed Assets to General Ledger Reconciliation -

>   Summary

| **Report type**             | **Reports**                                                                                                                                                                                                                              | **Printing methods**                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comparison                  | Book to Book Reconciliation                                                                                                                                                                                                              | Create report options in the Fixed Assets                                                                                                                                           |
| Depreciation                | Depreciation Detail                                                                                                                                                                                                                      | Create report options in the Fixed Assets Depreciation Report options window.                                                                                                       |
| Inventory                   | Fixed Assets Inventory List                                                                                                                                                                                                              | Create report options in the Fixed Assets Inventory Report options window.                                                                                                          |
| Projection                  | Annual Depreciation Projection - Detail                                                                                                                                                                                                  | Create report options in the Fixed Assets Projection Report options window or choose the printer icon in the Projections Inquiry window.                                            |
| Transaction                 | Additions                                                                                                                                                                                                                                | Create report options in the Fixed Assets Transaction Report options window.                                                                                                        |
| **Report type**             | **Reports**                                                                                                                                                                                                                              | **Printing methods**                                                                                                                                                                |
| Routines                    | Financial Detail Summarize Fixed Assets Purge FA Posting to General Ledger FA Posting to General Ledger Reprint Physical Inventory Import Physical Inventory Update Misplaced Physical Inventory Missing Physical Inventory              | Choose File \>\> Print or choose the printer icon in the window you use to complete the procedure **or** some will be printed automatically when you complete the procedure.        |
| Utilities                   | ACRS Tables Asset Account Reconciliation Asset Label Reconciliation Asset Delete Report Book ITC Reconciliation Fixed Assets Custodian Reconciliation Create Batch Headers Fixed Assets Migration Results Physical Inventory Info Import | Choose File \>\> Print or choose the printer icon button in the window you use to complete the procedure **or** some will be printed automatically when you complete the procedure. |
| Miscellaneous Audit Reports | Asset Group Import Fixed Assets Note Update Error Log Listing Fixed Assets Installation Report                                                                                                                                           | Choose File \>\> Print or choose the printer icon in the window you use to complete the procedure **or** some will be printed automatically when you complete the procedure.        |
| Inquiry Reports             | Asset Inquiry Asset Book Inquiry Report Financial Detail Inquiry Report Fixed Assets Batch Inquiry Report                                                                                                                                | Choose File \>\> Print or choose the printer icon in the window you use to complete the procedure.                                                                                  |

>   Book to Book YTD Depreciation Comparison

>   Comparison Report options window.

>   Depreciation Expense to General Ledger

>   Depreciation Ledger

>   Depreciation Ledger by Class

>   Depreciation Ledger by Class - Summary

>   Depreciation Ledger by Location Depreciation Ledger by Location - Summary

>   Depreciation Ledger by Structure

>   Depreciation Ledger by Structure - Summary

>   Fixed Assets Inventory List by Class

>   Fixed Assets Inventory List by Class -Summary

>   Fixed Assets Inventory List by Location

>   Fixed Assets Inventory List by Location -Summary

>   Fixed Assets Inventory List by Structure

>   Fixed Assets Inventory List by Structure - Summary

>   Locator List

>   Property Ledger

>   Asset List by Master Asset ID

>   Annual Depreciation Projection - Summary

>   Period Depreciation Projection - Detail

>   Period Depreciation Projection - Summary

>   Additions (Multicurrency)

>   Additions by Class

>   Additions by Class - Summary

>   Additions by Class (Multicurrency)

>   Additions by Location

>   Additions by Location - Summary

>   Additions by Location (Multicurrency)

>   Additions by Structure

>   Additions by Structure - Summary

>   Additions by Structure (Multicurrency)

>   Retirements

>   Retirements (Multicurrency)

>   Retirements by Class

>   Retirements by Class (Multicurrency)

>   Retirements by Class - Summary

>   Retirements by Location

>   Retirements by Location - Summary

>   Retirements by Location (Multicurrency)

>   Retirements by Structure

>   Retirements by Structure - Summary

>   Retirements by Structure (Multicurrency)

>   Transfers

>   If you are using the euro currency reports that include exchange rate
>   information, you can display the dual exchange rates involved in
>   triangulation. When triangulation is used, the Rate Type ID field displays
>   the rate type of the currency relationship that has a variable rate. If both
>   currency relationships have fixed exchanges rates, the Rate Type ID field is
>   blank.

#### Report destinations and formats

>   You can print reports to a printer, the screen, a file, or any combination
>   of these destinations.

>   **Printer** The report is printed to the default printer set up for your
>   company.

>   **Screen** The report appears on the screen and you can then choose to print
>   to the printer. In addition, if you’re using an electronic mail system
>   that’s compliant with MAPI (Microsoft’s Messaging Application Programming
>   Interface), you can e-mail any report that you print to the screen.

>   **File** You can select one of the file formats shown in the following
>   table:

| **File format** | **Description**                                                                                                                                                                                                                                                     |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tab-delimited   | The tab-separated ASCII character format used by spreadsheet programs, such as Microsoft Excel.                                                                                                                                                                     |
| Comma-delimited | The standard comma-separated ASCII character format used by database programs.                                                                                                                                                                                      |
| Text            | Text with no formatting. Use this option only if the application you’ll use to read the report can’t read any other format.                                                                                                                                         |
| HTML            | A format that can be viewed in a Web browser.                                                                                                                                                                                                                       |
| XML Data        | A text file that contains an XML representation of the report layout and all the report data. Choose this format if you want to process the report using an external application.                                                                                   |
| Adobe PDF       | This format is available if you have the PDFWriter printer driver installed (included with Acrobat 5 and earlier), or Acrobat Distiller from Acrobat 6 or later. PDF (Portable Document Format) files can be read using Adobe Reader software available from Adobe. |
| Word Document   | The Microsoft Office Open XML (.docx) file format used by Word 2007 or later. You can select this format if you select Template as the report type.                                                                                                                 |

>   The option to print multicurrency information is available on some report
>   option windows. To print multicurrency versions of your reports, mark the
>   Include Multicurrency Info option.

>   You can select a printing destination in various ways, depending on which
>   printing method you use.

-   If you print a report by choosing File \>\> Print or the printer icon button
    while a window is open, the Report Destination window appears, where you can
    select a destination. (You can select a preferred default
    destination—Printer or Screen—in the User Preferences window.)

-   For activity, comparison, depreciation, inventory, projection, and
    transaction reports, you select the destination when you create the report
    options needed to print these reports.

#### Processing reports on a process server

>   If you are using the Distributed Process Server (DPS), you can process some
>   reports on your computer or send them to a designated server on the network.
>   Sending long reports to a process server allows you to continue working
>   while the reports are being created.

>   You can set up the Process Server to process the following Fixed Asset
>   Management activities:

-   Depreciation or depreciation projections

-   General Ledger posting

-   Mass changes

-   Mass retirements

-   Mass transfers

-   Deleting asset data

-   Rebuilding tables

-   Summarize financial detail

-   Year end processes

-   Physical inventory update

#### Creating report options

>   Report options include specifications of sorting options and range
>   restrictions for a particular report. To print some of the Fixed Asset
>   Management reports, you must first create report options. Each report can
>   have several different options so that you can easily print the information
>   you need. For example, you can create one report option to show summary
>   information, and another option to show detailed information.

>   *A single report option can’t be used by multiple reports. For identical
>   options for several reports, you must create them separately.*

>   Use the Fixed Asset Management report options windows to create sorting,
>   restriction and printing options for the reports that have been included
>   with Fixed Asset Management.

>   **To create report options:**

1.  Open one of the asset reports windows.

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Activity)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Comparison)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Depreciation)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Inventory)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Projection) (Financial \>\>
>   Reports \>\> Fixed Assets \>\> Transaction)

1.  Select a report from the Reports list.

>   *For report options window information choose Help \>\> Index; then enter
>   the name of the specific report options window.*

1.  Choose New to open the report options window. Your selection in step 2
    determines which report options window appears.

2.  Name the option and enter information to define the option. The name you
    choose for the option won’t appear on the report. The selections available
    for defining report options vary, depending on the report type you’ve
    selected.

3.  Enter range restrictions. The Ranges list shows the ranges available for
    each report. The available ranges vary, depending on the type of report.

>   *You can enter only one restriction for each restriction type. For instance,
>   you can insert one asset ID restriction or one document number restriction.*

1.  Choose Insert to add the range to the Restrictions List. To remove an
    existing range from the list, select the range and choose Remove.

2.  Choose Email Options to enter email options for the report option. Once the
    email options are set up, you'll be able to send the reports in an email
    message from this window by choosing Email. You can also send this report in
    an email from any list view where the report option is displayed.

3.  Choose Destination to select a printing destination. Reports can be printed
    to the screen, to the printer, to a file, or to any combination of these
    options. If you select Ask Each Time, you can select printing options each
    time you print this report option.

>   For more information about printing reports, see *Printing a report with an
>   option*.

1.  To print the report option from the report options window, choose Print
    before saving it. To print the report later, choose Save and close the
    window. The report window will be redisplayed.

#### Printing a report with an option

>   Use an asset report window to print a fixed assets report for which a report
>   option has been set up.

>   **To print a report with an option:**

1.  Open one of the asset reports window.

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Activity)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Comparison)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Depreciation)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Inventory)

>   (Financial \>\> Reports \>\> Fixed Assets \>\> Projection) (Financial \>\>
>   Reports \>\> Fixed Assets \>\> Transaction)

1.  Select a report from the Reports list.

2.  Select a report option and choose Insert to insert the report option in the
    Email or Print List.

3.  Choose Print to print the report options in the Email or Print List.

#### Customizing a report

>   Most of the existing reports in Fixed Asset Management can be modified to
>   meet your needs. You can add or delete fields, change sorting options, add
>   subtotals, or you can customize reports using Report Writer. The following
>   procedure describes the simplest method to customize a default report and
>   set access to it. Refer to the Report Writer documentation for detailed
>   instructions about using Report Writer.

>   **To customize a report:**

1.  Print the report to the screen.

2.  While the report is on the screen, choose Microsoft Dynamics GP menu \>\>
    Tools \>\> Customize \>\> Modify Current Report.

>   The Report Layout window will appear with the current report open.

1.  In the Report Layout window, make any necessary changes to the appearance of
    the report.

2.  Choose Windows \>\> Report Definition.

3.  In the Report Definition window, change the sorting options, modify the
    report layout, or add report restrictions.

4.  Choose OK to save the changes to the report.

5.  Choose File \>\> Microsoft Dynamics GP to return to Fixed Asset Management.

6.  Choose Microsoft Dynamics GP menu \>\> Tools \>\> Setup \>\> System \>\>
    Security and select the user, company and product to grant access for.

7.  In the Type field, select Modified Reports.

8.  In the Access List, double-click the name of the report you modified. An
    asterisk (\*) appears, indicating that the selected user has access to the
    report.

9.  Choose OK to save the changes to the user’s security settings.

#### Fixed Asset Management Microsoft SQL® Server Reporting Services reports

>   You can view Fixed Asset Management Reporting Services reports from the
>   Reporting Services Reports list. If you are using Reporting Services 2008 or
>   later, financial metrics for your home page also appear in the Reporting
>   Services Reports list. You can access the Reporting Services Reports list
>   from the navigation pane or from an area page in the Microsoft Dynamics GP
>   application window. This report list appears if you specified the location
>   of your Reporting Services reports using the Reporting Tools Setup window.
>   See your System Setup Guide (Help \>\> Contents \>\> select Setting up the
>   System) for more information.

>   The following Reporting Services reports are available for Fixed Asset
>   Management.

| Additions Report | Fixed Assets to General Ledger Reconciliation |
|------------------|-----------------------------------------------|


>   Report

| Fixed Assets Depreciation Detail | Period Projection Report |   |
|----------------------------------|--------------------------|---|
| Fixed Assets Depreciation Ledger | Retirements Report       |   |

>   **To print a Fixed Asset Management Reporting Services report:**

1.  In the navigation pane, choose the Financial button, and then choose the
    Reporting Services Reports list.

2.  Mark the Purchase Order Processing report that you want to print.

3.  In the Actions group, choose View to open the Report Viewer.

4.  In the Report Viewer, select the specifications for the report and choose
    View Report.

5.  After viewing the report, select a format and print the report.

**Glossary**

#### Account

>   The type of record—asset, liability, revenue, expense, or owner’s
>   equity—traditionally used for recording individual transactions in an
>   accounting system. Also, the identifying alphanumeric characters that have
>   been assigned to the record.

#### ACRS (Accelerated Cost Recovery System) tables

>   Tables to calculate depreciation for personal property, real estate, real
>   estate using modified straight-line, low income housing, and foreign real
>   property. Created by the Economic Recovery Tax Act of 1981 for US tax
>   purposes. Depreciation can be calculated for assets acquired from 1981
>   through 1986.

#### Amortization

>   The gradual reduction of a liability in regular payments over a specified
>   period of time. These payments must be enough to cover both principal and
>   interest. Also, writing off an intangible asset investment over the
>   projected life of the assets.

#### Asset

>   An item of value owned by an individual or corporation, especially that
>   which could be converted to cash. On a balance sheet, assets are equal to
>   the sum of liabilities, common stock, preferred stock, and retained
>   earnings.

#### Asset book

>   Accounting records—ledgers or journals— for a specific reporting purpose,
>   such as financial or tax. All assets to be included for the reporting
>   purpose would be included in the asset book.

#### Asset group

>   A collection of assets with a similar characteristic.

#### Averaging convention

>   Rules for calculating depreciation in the year of the acquisition of the
>   asset and the year of the disposal of the asset.

**Book**

>   *See Asset book*.

#### Capitalize

>   To classify the cost of an asset as a long-term investment, rather than
>   charging it to current operations.

#### Clearing account

>   An asset account that is debited in

>   Purchasing Order Processing or Payables Management for the PURCH type
>   distribution line in the Purchasing Distribution Entry window. This account
>   is credited when an asset is added. At the end of each period, if the
>   balance in the clearing account is zero, items in Purchasing Order
>   Processing or Payables Management that need to be capitalized are added in
>   Fixed Asset Management.

#### Corporate book

>   The accounting records for financial reporting purposes, based on the
>   applicable accounting principles. *See also Tax book*.

#### Cost basis

>   The purchase price of an asset, including freight, tax, and other expenses,
>   less any adjustments, such as Section 179 Expense Deduction and salvage
>   value. Used to determine capital gains and capital losses for tax purposes.

#### Depreciation

>   The allocation of the cost of an asset over a period of time for accounting
>   and tax purposes. Also, a decline in the value of an asset due to general
>   wear and tear or obsolescence.

#### Depreciation-sensitive

>   Changes that affect depreciation. When a value in a depreciation-sensitive
>   field is changed, depreciation must be recalculated for that asset.

#### Expense

>   A cost incurred by a business in an attempt to obtain revenue.

**Filter**

>   An option to restrict specific information.

#### Fiscal period

>   Divisions of the fiscal year, usually monthly, quarterly, or semiannually,
>   when transaction information is summarized and financial statements are
>   prepared.

#### Fiscal year

>   An accounting period of 365 days—366 days in leap years—but not necessarily
>   starting on January 1.

#### Inflation

>   The overall price movement—generally upward—of goods and services in an
>   economy.

#### Insurance year

>   The year reproduction cost of an asset is based on.

#### Investment Tax Credit (ITC)

>   An investment tax credit (ITC) taken for US tax purposes for the purchase of
>   specific types of business property. The credit must be taken in the year of
>   purchase and is limited by a maximum amount. The ITC was eliminated by the
>   Tax Reform Act of 1986.

#### Luxury auto

>   A limit on the annual recovery allowances— depreciation—that can be taken
>   for US tax purposes.

#### Master asset ID

>   An ID used to group components of a single asset or related assets. For
>   example, a computer might be considered an asset that contains a CPU, a
>   monitor, and a printer as components. You can assign the same master asset
>   ID to each component so that the parts are related and can be tracked
>   together.

#### Net cost basis

>   The Original Cost Basis, minus Section 179

>   Expense Deduction, minus ITC Cost Reduction Amount, plus or minus
>   Miscellaneous Cost Adjustment.

#### Physical location

>   The actual place where an asset is located; for example, a building, a floor
>   in a building, or a room in a building.

#### Prior period adjustment

>   An adjustment for an error that was not discovered during the period in
>   which it occurred.

#### Prior year depreciation

>   Depreciation that relates to years earlier than the current fiscal year.

#### Proceeds

>   The value—in cash or anything not in the form of cash—received for an asset.

#### Projected depreciation

>   The forecasted allocation of the cost of an asset over a period of time for
>   accounting and tax purposes.

#### Purchasing transaction

>   A transaction that originated in Payables Management or Purchase Order
>   Processing.

#### Recalculate option

>   Calculates a new rate of depreciation using the new cost basis data, but
>   does not make adjusting entries for depreciation already taken. The new rate
>   of depreciation will be used the next time the depreciation routine is
>   completed.

#### Receiving

>   Recording the receipt of assets that have been ordered from a vendor via a
>   purchase order. Receiving also refers to the recording of the invoice for
>   the assets received.

#### Reset Life option

>   Recalculates depreciation from the date it was placed in service forward to
>   the date the asset has already been depreciated. If there are adjustments to
>   the depreciation for any period, they will be written to the financial
>   detail table.

#### Reset Year option

>   Recalculates depreciation from the beginning of the year forward to the date
>   the asset has already been depreciated. If there are adjustments to the
>   depreciation for any period, they will be written to the financial detail
>   table.

#### Retire

>   To sell or dispose of a fixed asset, including destroying or abandoning the
>   asset. A retired asset is no longer producing revenue.

#### Section 179 Expense Deduction

>   US Tax Section 179 allows expensing all or a portion of the cost of an asset
>   in the year of acquisition, rather than expensing, or depreciating, over the
>   life of the asset. Any portion of the cost of an asset taken as Section 179
>   cannot be taken also as depreciation. For more information about additional
>   restrictions and rules, contact a tax professional.

#### Special depreciation allowance

>   An additional first-year depreciation deduction. If used with the Job
>   Creation and Worker Assistance Act of 2002, the deduction is equal to 30
>   percent of the adjusted basis of qualified property. For more information,
>   contact a tax professional.

#### Spread

>   Options that account for the allocation of proceeds and expenses of sale for
>   selected assets when mass retiring those assets.

#### Suffix

>   Number used to distinguish multiple assets with the same asset ID. Might be
>   used to identify components of assets or assets that have been partially
>   retired or transferred.

#### Switchover

>   Option that changes the depreciation method of an asset when the
>   depreciation for an asset is greater using the switchover method than the
>   current depreciation method. The depreciation method automatically will
>   change to the switchover method. Switchover will only occur at the beginning
>   of the year when the yearly depreciation rate is calculated for the next
>   year.

#### Tax book

>   The accounting records for tax reporting purposes, based on the applicable
>   tax laws. *See also Corporate book*.

#### TEFRA

>   The Tax Equity and Fiscal Responsibility Act of 1982 produces additional
>   revenue through a combination of federal spending cuts, tax increases, and
>   reform measures for US tax purposes.

#### Transfer

>   The movement of an asset to a new general ledger account, property tax
>   location, physical location, structure, or master asset ID. Typically
>   affects the future allocation of depreciation expense for the asset.

#### Vendor

>   A person or company providing goods and services in return for payment.

#### Year-end closing

>   A process used to zero out year-to-date values and update beginning of year
>   values for assets, including quantities, depreciation, and maintenance.
