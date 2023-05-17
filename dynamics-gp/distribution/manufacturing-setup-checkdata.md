---
title: "Manufacturing Setup - Check data stored procedure"
description: "Learn how to identify problems with the se4tup of the Manufacturing module and fix any issues."
keywords: "manufaturing"
author: theley502
manager: jswymer
ms.prod: dynamics-gp
ms.topic: article
ms.reviewer: jswymer
ms.author: theley
ms.date: 03/03/2021
---

# Manufacturing Setup - Check data and correct errors

This part of the documentation includes information that will help you verify the setup on the  Manufacturing module in Dynamics GP by running the Microsoft Dynamics Manufacturing Checkdata stored procedure.

The Checkdata stored procedure is designed to evaluate various manufacturing tables and report back any inconsistencies it discovers.  This would include issues with imported data, issue with rolling up cost, and issue with manufacturing orders and costing.  It will not make any changes to any manufacturing table.  It is not version specific and can be run on any versions of Microsoft Dynamics GP.

## To run the Checkdata stored procedure

To run this, open Microsoft SQL Server Management Studio and run the following statement against the company database:

1. In Object Explorer, expand Databases, and then click on your company database.  
2. Click New Query, and then type the following select statement in the query pane:

    ```sql
    Exec mfgfix90checkdata
    ```

3. On the Query menu, point to Results To, and then click Results to Text.
4. On the Query menu, click Execute.

## How do you correct the reported errors

Once you have the results of the script in text form use the Error Listing below to correct them accordingly.  This Error Listing will list all the possible errors the script may return.  If the error has an asterisk next to it this means that it is a serious error and must be corrected to avoid further problems.  If the error does not have an asterisk by it you will want to look at the information returned and verify it is accurate.  These errors are more informational type errors and may or may not be a problem depending on how your manufacturing information is set up.  The errors are listed in alphabetical order.  

## Error Listing

1. ALLOCATE QUANTITY DOES NOT EQUAL TRANSACTION QUANTITY ON ALLOCATES PICK DOC

    There are records in the MOP_PickDoc_Line (MOP1210) for pick documents with Allocate transactions where the Quantity Allocated (ATYALLOC) and Transaction Quantity (TRXQTY) values are not the same.

    Resolution:  
    Go to Component Transaction Inquiry (Inquiry | Manufacturing | Manufacturing | Component Transaction Inquiry), pull up the MO in question, and determine what the correct allocation quantity is.  Use SQL to update the table to reflect the correct quantity.

    To check for the table for each of the quantities run the following script.

    ```sql
    select * from MOP1210 where TRXQTY<>ATYALLOC and TRX_TYPE=3
    ```

    To update the transaction quantity in the MOP1210, run the following script

    ```sql
    Update MOP1210 set set ATYALLOC=TRXQTY where TRXQTY<>ATYALLOC and TRX_TYPE = 3
    ```

2. ARCHIVED OR CONFIGURED BOM WITH NO BOM NAME

    There is an Archived or Configured BOM without a BOM Name.

    Resolution:
    Every Archived or Configured BOM must have a BOM Name.  

    Use SQL to update the Bill of Material Line table (BM010115) and BOM Revision table (BM010415).  

    Once the table has been updated go to BOM Entry (Cards | Manufacturing | Bill of Materials), pull up the Archived or Configured BOM, and either correct the BOM name or delete the BOM.

    To update the BOM name in the BM010115 table run the following script.  

    ```sql
    Update BM010115 set BOMNAME_I='xxxx' where (BOMCAT_I=4 or BOMCAT_I=3)and BOMNAME_i=''
    ```

    To update the BOM name in the BM010415 table run the following script.

    ```sql
    Update BM010415 set BOMNAME_I='xxxx' where (BOMCAT_I=4 or BOMCAT_I=3)and BOMNAME_i=''
    ```

3. ARCHIVED OR CONFIGURED SUBASSEMBLY COMPONENT WITH NO BOM NAME

    There is a subassembly component BOM assigned to a BOM with a BOM Type of Archived or Configured that has no BOM Name.  

    Resolution:
    Every Archived or Configured BOM must have a BOM Name.  

    Use SQL to update the record in both the Bill of Material Line table (BM010115) and BOM Revision table (BM010415).  

    Once the table has been updated go to BOM Entry (Cards | Manufacturing | Bill of Materials), pull up the Archived or Configured BOM, and either correct the BOM name or delete the BOM.  

    To update the BOM name in the BM010115 table run the following script.  

    ```sql
    Update BM010115 set BOMNAME_I='xxxx' where(BOMCAT_I=4 or BOMCAT_I=3)and BOMNAME_i=''
    ```

    To update the BOM Name in the BM010415 table run the following script.

    ```sql
    Update BM010415 set BOMNAME_I='xxxx' where(BOMCAT_I=4 or BOMCAT_I=3)and BOMNAME_i=''
    ```

4. BOM CHILD MISSING ITEM MASTER RECORD  

    There is a child part item number defined in the Bill of Material Line table (BM010115) table does not have a corresponding Item Master (IV00101) record.  

    Resolution:
    Either go to the Item Maintenance (Cards | Inventory | Item) window to create the item number, or use SQL to remove all occurrences of that item from Bill of Material Line table (BM010115) and BOM Revision table (BM010415).  

    To determine the records in the BM010115 run the following script.  

    To update the BM010415 replace the BM010115 with the BM010415 in the below scripts.  

    ```sql
    select * from BM010115 where CPN_I not in (select ITEMNMBR from IV00101)
    ```

    To delete the records from the BM010115 run the following script.  This is sample text.  This is sample text.  This is sample text.  

    ```sql
    delete BM010115 where CPN_I not in (select ITEMNMBR from IV00101)
    ```

5. BOM EFFECTIVE DATE IN THE FUTURE

    There are items where the Effective Date on a BOM is after the current date.

    Resolution:
    Go to the BOM Entry (Cards | Manufacturing | Bill of Materials) window, pull up the item in question, and verify/change the Effective Date.

6. BOM EXISTS FOR BOUGHT ITEM

    There is a component item where the parent item for a BOM has a Make/Buy code of Buy.  

    Resolution:

    If the BOM is an Archived or Engineering BOM, this message can be ignored.  
    If the BOM is a Manufacturing BOM, go to the BOM Entry (Cards | Manufacturing | Bill of Materials) window, and either move the BOM to an Archived status, or delete it.

7. BOM LINE IN DATE IN THE FUTURE

    There is BOM and component information when a component In-Date on the BOM is after the current date.

    Resolution:
    Go to the BOM Entry (Cards | Manufacturing | Bill of Materials) window, and verify the In-Date for the component in question.

8. BOM LINE RECORD IS MISSING A BOM REVISION LEVEL RECORD

    There is a child record in the BOM Line table (BM010115) with a parent item that is not in the BOM Revision table (BM010415).  

    In other words, the BOM Line table is missing its header record.  

    Resolution:

    Use SQL to remove the record from the BOM Line table (BM010115) and re-enter the BOM through BOM Entry (Cards | Manufacturing | Bill of Materials) window.

    To determine the records missing from the BM010415 run the following script.

    ```sql
    select * from BM010115 where PPN_I not in (select ITEMNMBR from BM010415)
    ```

    To remove the records from the BM010115 run the following script.

    ```sql
    delete BM010115 where PPN_I not in (select ITEMNMBR from BM010415
    ```

9. BOM PARENT MISSING ITEM MASTER RECORD

    There is a parent item number defined in the BOM Line table (BM010115) table that does not have a corresponding record in the Item Master table (IV00101).  

    Resolution:

    Either go to the Item Maintenance (Cards | Inventory | Item) window to create the item number or use SQL to remove all occurrences of that item from BOM Line table (BM010115) and the BOM Revision (BM010415) tables.  

    To determine the records in the BM010115 run the following script.

    ```sql
    select * from BM010115 where PPN_I not in (select ITEMNMBR from IV00101)
    ```

    To remove the records from the BM010115 run the following script

    ```sql
    delete BM010115 where PPN_I not in (select ITEMNMBR from IV00101)
    ```

10. BOM SEQUENCES DO NOT MATCH IN BM010115 AND BM010200

    There are component BOM sequence numbers in the the BOM Line table (BM010115) that do not match the component BOM sequence numbers in the BOM Routing Link table (BM010200).

    Resolution:
    Go to BOM Routing Link (Cards | Manufacturing | Bill of Materials | GoTo | BOM Routing Link), enter the BOM,  delete the linked components, and add them again.  

11. BOM SEQUENCES DO NOT MATCH IN BM010115 AND TARD1001

    There are components BOM sequence numbers  in the BOM Line table (BM010115) that do not match the component BOM sequence numbers in the Reference Designator table (TARD1001).  

    Resolution:
    If you use Reference Designators you will need to go to BOM Entry (Cards | Manufacturing | Bill of Materials) and reenter the reference designators for specific BOMs.  
    If you are not using Reference Designators this error will not cause further issues.  

12. BOM SEQUENCES DO NOT MATCH IN BM010200 AND TARD1001

    There are BOM sequence numbers for components in Reference Designators table (TARD1001) that do not match the BOM sequence numbers for these components in the BOM Routing Link table (BM010200).  

    Resolution:
    If you use Reference Designators you will need to go to BOM Entry (Cards | Manufacturing | Bill of Materials) and reenter the reference designators for specific BOMs.  
    If you are not using Reference Designators, this error will not cause further issues.  

13. BOM/ROUTING LINK FOR INVALID CHILD PART

    The child part in a BOM/Routing Link record (BM010200) does not have a valid record in the Item Master table (IV00101).  

    Resolution:
    Either create the child part using the Item Maintenance (Cards | Inventory | Item) window or remove all records from the BOM/Routing Link table (BM010200) that have that child part.  

    To determine the records in the BM010200 run the following script

    ```sql
    select * from BM010200 where CPN_I not in (select ITEMNMBR from IV00101)
    ```

    To remove the records from the BM010200 run the following script

    ```sql
    delete BM010200 where CPN_I not in (select ITEMNMBR from IV00101)
    ```

14. BOM/ROUTING LINK FOR INVALID ROUTING SEQUENCE

    The routing sequence for a BOM/Routing Link record (BM010200) does not have a valid record in the Routing Line table (RT010130).  

    Resolution:

    Either create the routing sequence for the parent item using the Routing Sequence Entry (Cards | Manufacturing | Routing| Routing Entry) window or remove the record from the BOM/Routing Link table (BM010200).  

    To determine the records in the BM010200 run the following script

    ```sql
    select * from BM010200 where CPN_I not in (select ITEMNMBR from RT010130)
    ```

    To remove the records from the BM010200 run the following script

    ```sql
    delete BM010200 where CPN_I not in (select ITEMNMBR from RT010130)
    ```

15. BOM/ROUTING LINK FOR INVALID PARENT PART

    The parent part in a BOM/Routing Link table (BM010200) does not have a valid record in the Item Master table (IV00101).  

    Resolution:
    Either create the parent part using the Item Maintenance (Cards | Inventory | Item) window or remove all records from the BOM/Routing Link table (BM010200) that have that parent part.  

    To determine the records in the BM010200 run the following script.

    ```sql
    select * from BM010200 where PPN_I not in (select ITEMNMBR from IV00101)
    ```

    To remove the records from the BM010200 run the following script.

    ```sql
    delete BM010200 where PPN_I not in (select ITEMNMBR from IV00101)
    ```

16. BOUGHT ITEM HAS NO STANDARD MATERIAL COST

    There are items that have a periodic valuation method, are buy items, and have no cost (COST_I) in the IC Cost Standard Item Defaults table (CT00003).  

    Resolution:

    Either go to the Standard Cost Changes (Cards | Manufacturing | Inventory| Standard Cost Changes) window or the Standard Item Mat Costs (Cards | Manufacturing | Inventory| Standard Item Mat Costs) window to record material costs for the item, and then roll up and revalue (Tools |Routines |Manufacturing) so that the item will display the cost.  

17. BOUGHT ITEM MATERIAL COST EFFECTIVE DATE IN THE FUTURE

    There are buy items with periodic valuations that have an effective date for Material Costs that is in the future (> today's date).  

    Resolution:

    Go to the Standard Item Material Costs window (Cards | Manufacturing | Inventory| Standard Item Mat Costs), pull up the item and enter the corrected effective date and cost.  Perform a roll up and revalue (Tools |Routines |Manufacturing) to ensure that the item is updated with the cost and date.  

18. BOUGHT ITEM MATERIAL FIXED OH COST EFFECTIVE DATE IN THE FUTURE

    There are buy items with periodic valuations that have an effective date for Material Fixed Overhead Cost that is in the future (> today's date).  

    Resolution:  

    Go to the Standard Item Material Costs window (Cards | Manufacturing | Inventory | Std Item Mat Costs), pull up the item and enter the corrected effective date and cost.  Perform a roll up and revalue (Tools |Routines| Manufacturing) to ensure that the item is updated with the cost and date.  

19. BOUGHT ITEM MATERIAL VARIABLE OH COST EFFECTIVE DATE IN THE FUTURE

    There are buy items with periodic valuations that have an effective date for Material Variable Overhead Costs that is in the future (> today's date).

    Resolution:
    Go to the Standard Item Material Costs window (Cards | Manufacturing | Inventory | Std Item Mat Costs), pull up the item and enter the corrected effective date and cost.  Perform a roll up and revalue (Tools |Routines |Manufacturing) to ensure that the item is updated with the cost and date.  

20. CHILD OUT DATE EARLIER THAN IN DATE0

    There is an Out Date for the displayed child part that is earlier than the In Date.  

    Resolution:
    Go the BOM Entry window (Cards | Manufacturing | Bill of Materials), select the parent number from the report, and correct the dates for the child item.  

21. CHILD PART MISSING ISSUE FROM SITE

    There is a child part that is missing the Issue-From site.  

    Resolution:
    Go to the BOM Entry window (Cards | Manufacturing | Bill of Materials), select the parent number from the report, and add the Issue-From site.  

22. CHILD PART MISSING ISSUE TO SITE

    A child part is missing the Issue To site.  

    Resolution:
    Go to the BOM Entry window (Cards | Manufacturing | Bill of Materials), select the parent number from the report, and add the Issue To site.  

23. COMPONENT ISSUE FROM SITE NOT ASSIGNED TO ITEM

    The Issue From site for the parent/child combination listed has not been assigned to the child part.  

    Resolution:
    Go to the Item Quantities Maintenance window (Cards | Inventory| Quantities/Sites) to assign that site to the child item.  Pull up the item number and the Site ID and choose Save in the Item Quantities Maintenance window.  

24. COMPONENT ISSUE TO SITE NOT ASSIGNED TO ITEM

    The Issue-To site for the parent/child combination listed has not been assigned to the child part.  

    Resolution:
    Go to the Item Quantities Maintenance window (Cards | Inventory| Quantities/Sites) to assign that site to the child item.  Pull up the item number and the Site ID, and then choose Save in the Item Quantities Maintenance window.  

25. COMPONENT ISSUE TO SITE NOT IN WC MASTER

    The Issue-To site for the parent/child combination listed has not been defined as a work center.  

    Resolution:
    Go to the Work Center setup window (Cards | Manufacturing |Work Centers |Setup) to create the work center or use the BOM Entry window (Cards | Manufacturing | Bill of Materials) to change the Issue-To Site for that component or use the BOM Mass Update utility (Tools | Utilities | Manufacturing) to update the components.

26. COST ARRAY IN TABLE MOP1010 NOT EQUAL TO COSTS PUT INTO WIP

    There are records in the MOP WIP Labor and Machine table (MOP1010) where the Cost Arrays do not match the corresponding costs in the MOP WIP Stack table (MOP1000).

    Resolution:
    Determine if this issue is impacting only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.  

27. COSTS IN MOP1002 MAY BE INCORRECT

    There are records in the MOP_WIP_Costs table (MOP1002) where the WIP In and/or WIP Out Costs for the MO differ with the Inventory History tables (IV30300 in particular).  

    Resolution:
    Verify that all adjustments from Manufacturing have completely posted through the Inventory subledger.  Determine if this issue is impacting only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.  

28. COSTS IN TABLE MOP1002 NOT EQUAL TO COSTS PUT INTO WIP's

    There are records in the MOP_WIP_Costs table (MOP1002) where the WIP In and/or WIP Out Costs for the MO differ with the Inventory history tables (IV30300 in particular).  

    Resolution:
    Verify that all adjustments from Manufacturing have completely posted through the Inventory subledger.  Determine if this issue is impacting only one MO or numerous MO's.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.  

29. COSTS USED IN MOP1010 NOT EQUAL TO SUM OF RECEIPT COSTS
    There are records in the MOP WIP Labor and Machine table (MOP1010) where the Costs Used does not equal the sum of the costs recorded in the MOP_Receipt_MSTR table (MOP1100) for the same MO.  

    Resolution:
    Determine if this issue is impacting only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.  

30. DATA COLLECTION RECORDS IN WHICH THE SUM OF THE DC LINES<> DC MASTER TABLE

    There are records in the Data Collection MSTR table (SF010014) where the Elapsed Time or the collected costs do not match the Data Collection Line Items table (SF010115) for the same MO and sequence.  

    Resolution:
    Verify that the Data Collection line item information (SF010115) is correct and complete.  You can view this in the table or in Great Plains in the Data Collection Summary window (Inquiry | Manufacturing | WIP | DC Summary) and then drill down on sequence information to the Data Collection Summary – Direct Labor window.  If the information in the Data Collection Line Items table (SF010115) is correct MBS Professional Services will need to be contacted to correct.

31. DOCDATE EMPTY EXISTS IN MOP1200

    There are pick documents in the MOP_PickDoc_MSTR table (MOP1200)that do not have a valid Docdate (document date).  

    Resolution:
    Check the MOP_PickDoc_Line table (MOP1210) for this PICKNUMBER.  If there are lines for is pick document number use SQL to update the MOP_PickDoc_MSTR table (MOP1200) with the correct date.  If there are no records in the MOP_PickDoc_Line table (MOP1210) related to this pick document number use SQL to remove the line from the MOP_PickDoc_MSTR table (MOP1200).  In order to delete the record from the MOP1200, you must know the pick document number.  Replace the XXX below with the pick document number in question.  First there is a select statement.  Next there is a delete statement.

    To determine the records in the MOP1200 run the following script.

    ```sql
    select * from MOP1200 where PICKNUMBER = 'XXX' and PICKNUMBER not in (select PICKNUMBER from MOP1210)
    ```

    To remove the records from the MOP1200 run the following script.

    ```sql
    delete MOP1200 where PICKNUMBER = 'XXX' and PICKNUMBER not in (select PICKNUMBER from MOP1210)
    ```

32. IC COST ITEM MASTER RECORD IS MISSING ITEM MASTER RECORD

    There is an item record in the IC Cost Item Master table (CT00102) without a matching record in Item Master table (IV00101).  This is usually an indication of an item that was deleted or imported improperly.  

    Resolution:
    Either add the item number in question in the Item Maintenance window (Cards | Inventory | Items), save the item, and then delete the newly added item or use SQL to remove the record from the IC Cost Item Master (CT00102) table.  Use the following scripts to first display the record to be removed and then delete that record.  

    To determine the records in the CT00102 run the following script.  Replace the XXX below with the item number to be deleted.  

    ```sql
    select * from CT00102 where ITEMNMBR='XXX'
    ```

    To remove the records from the CT00102 run the following script.  Replace the XXX below with the item number to be deleted.  

    ```sql
    delete CT00102 where ITEMNMBR='XXX'
    ```

33. IC_IV_STANDARD RECORD IS MISSING AN ITEM MASTER RECORD

    There is an item record in the IC_IV_Standard table (ICIV0323) without a matching record in Item Master (IV00101).  
    This is usually an indication of an item that was deleted or imported improperly.  

    Resolution:

    There are two options for resolution:
    Add the item number in the Item Maintenance window (Cards | Inventory | Items), save the item, and then delete the newly added item.  This will remove the record for the item from both tables.

    Or use SQL to remove the record from the IC_IV_Standard (ICIV0323) table via SQL.  Use the following scripts to first display the record to be removed and then delete that record.  Replace the XXX below with the item number to be deleted.  

    To determine the records in the ICIV0323 run the following script.  Replace the XXX below with the item number to be deleted.  

    ```sql
    select * from ICIV0323 where ITEMNMBR='XXX'
    ```

    To remove the records from the ICIV0323 run the following script.  Replace the XXX below with the item number to be deleted.  

    ```sql
    delete ICIV0323 where ITEMNMBR='XXX'
    ```

34. ICIV0323 UNIT COST DOES NOT MATCH ITEM STANDARD COST

    There are items where the TOTALCOSTI_1 in the IC_IV_Standard table (ICIV0323) does not match the standard cost in the Item Master table (IV00101).  

    Resolution:
    This could result from an import of items into the Item Master table.  A Rollup and Revalue will not correct this issue.  

35. INVALID BOM CATEGORY

    There is a parent item's BOM Category that has a value other than 1 or 3 (regular or phantom).

    Resolution:
    Go to the BOM Entry window (Cards | Manufacturing | Bill of Materials), select the parent item, and insure that it has a valid BOM Category, then save the record.  

36. INVALID BOM TYPE

    There is a parent item's BOM Type that has a value other than 1 through 5 in the BOM Revision Table (BM010415).  

    Resolution:
    This could result from an import of items into the Item Master table.  A Rollup and Revalue will not correct this issue.  

37. NONVALID FULFILLMENT METHOD

    There is an item with a Make/Buy code of Make or Make/Buy that does not have a valid Fulfillment Method in the Item Engineering File table (IVR10015).The fulfillment method should be 1, 2, and 3 when the Make/Buy code in the same table is 1 or 2. Verifies there are no other values stored in this field.

    Resolution:
    Go to the Item Engineering window (Cards | Manufacturing |Inventory |Engineering Data) and enter the item, select the correct fulfillment method, and save the record.  
    Choose the item in question, and select the Default Site if one exists.  If a Default Site doesn't exist for the item, choose the Initial Values record.  For the Item/Site record in question, set the Replenishment Method as desired.  

38. INVALID ITEM STATUS

    There is an item with an invalid Item Status (ItemStatus_I) field in the Item Engineering File table (IVR10015).  Valid numbers for Item Status in this table are 1, 2, 3, 4, 5, and 6.  

    Verify that there are no other values stored in this field.  The number should be a value between 1 and 6. Any other number is invalid

    Resolution:
    Go to the Item Engineering window (Cards | Manufacturing |Inventory |Engineering Data) and enter the item, select the correct Item Status, and save the record.

39. INVALID ITEM/VENDOR MRP MODIFIER

    There is an item that has a defined item-vendor relationship but one of the following quantity fields from the Item Vendors Maintenance window (Cards | Inventory |Vendors) has a negative value: Minimum Order, Maximum Order, Economic Order, Average Order, or Order Increment.

    Resolution:
    Go to the Item Vendors Maintenance window (Cards |Inventory |Vendors), enter the item number and primary vendor, and correct the field with the negative value.  

40. INVALID MAKE/BUY CODE

    There is an item that has an invalid Make/Buy Code (MakeBuyCode_I) field in the Item Engineering File table (IVR10015).  The valid values for the Make/Buy Code are 1, 2, and 3.  

    Verify that there are no other values in this field in the IVR10015 table.  The number should be 1 for a made item, 2 for an either item, or 3 for a bought item.  Any other number is invalid.  

    Resolution:
    Go to the Item Engineering window (Cards | Manufacturing |Inventory |Engineering Data), enter the item, select the correct Make/Buy code, and save the record.  

41. INVALID ORDER POLICY CODE

    There is an item with an invalid Order Policy (ORDERPOLICY) field in the Item Engineering File table (IVR10015).  Valid numbers for this field are 1, 2, or 3.  

    Resolution:
    Go to the Item Resource Planning window (Cards | Inventory |Item Resource Planning), enter the item number, select the correct Order Policy, and save the record.  

42. INVALID ORIGINATING PICK NUMBER FOR REVERSE TRANSACTION

    There are records in the MOP_PickDoc_Line table (MOP1210) where the Originating Pick Number for the reverse issue, reverse allocate, or reverse scrap do not refer to valid issue, allocate or scrap transaction records.  

    Resolution:
    Determine if this issue is impacting only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.  

43. INVALID POQ PERIOD LENGTH

    There is an item with an order policy of Period Order Quantity that has an invalid value in the Period Order Quantity Period Length field.  The value should be 1 or greater.  

    Resolution:
    Go to the Item Resource Planning window (Cards |Inventory |Item Resource Planning), enter the item number and site in question, enter the correct Number of Days, and save the record.

44. INVALID ROUTING MACHINE ID

    The routing sequence has a Machine ID that has not been defined

    Resolution:
    Go to either the Machine Definition window (Cards | Manufacturing |Machines) to create the correct Machine ID, or the Routing Entry window (Cards | Manufacturing | Routing| Routing Entry) to change the machine assigned to that routing sequence.

45. INVALID ROUTING OPERATION CODE

    The routing sequence has an operation code assigned to it that has not been defined.  

    Resolution:
    Go to either the Operations Setup window (Cards | Manufacturing | Routings |Operations) to create the operation code, or the Routing Entry window (Cards | Manufacturing | Routing| Routing Entry) to change the operation code assigned to that step in the routing to a valid code.

46. INVALID ROUTING RUN LABOR CODE

    The routing sequence has a labor code that has not been defined.  

    Resolution:
    Go to either the Labor Code Definition window (Cards | Manufacturing | Labor Codes) to set up the labor code, or the Routing Entry window (Cards | Manufacturing | Routing| Routing Entry) to change the labor code for that routing step to a correct value.

47. INVALID ROUTING RUN MACHINE CODE

    The routing sequence has a Machine ID that does not exist in the Machine Master table (MM010032).  

    Resolution:
    Go to the Machine window (Cards |Manufacturing | Machines) and enter the Machine ID exactly as it appears in the Routing Sequence Entry window (Cards | Manufacturing | Routing| Routing Entry) and related information or you may select an existing Machine ID in the Routing Sequence Entry window (Cards | Manufacturing | Routing| Routing Entry).

48. INVALID ROUTING SETUP LABOR CODE

    The routing sequence has a setup labor code that has not been defined.  

    Resolution:
    Go to either the Labor Code Definition window (Cards | Manufacturing | Labor Codes) to set up the labor code, or the Routing Entry window (Cards | Manufacturing | Routing| Routing Entry) to change the setup labor code for that routing step to a correct value.  

49. INVALID ROUTING WORK CENTER

    The routing sequence has a work center that has not been defined.  

    Resolution:
    Go to either the Work Center Setup window (Cards |Manufacturing |Work Center |Setup) to set up the work center, or the Routing Entry window (Cards| Manufacturing | Routing| Routing Entry) to change the work center assigned to that step in the routing.

50. INVALID ROUTING STATUS

    The routing header has a routing status value that is not between 1 and 4.  

    Resolution:
    Go to the Header Routing Window.  To get to this window go to the Routing Entry window(Cards| Manufacturing | Routing| Routing Entry), enter your item and routing name, click on the Routing Name link, and select the correct status for that routing.  

51. ISSUE FROM AND ISSUE TO ARE THE SAME, FLOORSTOCK NOT CHECKED

    There is a child part has the same Issue To and Issue From sites, but the Floorstock checkbox for that part is not marked.  

    Resolution:
    Go to the BOM Entry window (Cards | Manufacturing | Bill of Materials), select the parent number from the report, click on the component in question in the tree view, and on the right side of the window and either change one of the sites or mark the Floorstock checkbox for that item.

52. ITEM ENGINEERING FLOORSTOCK FLAG OUT OF SYNCH WITH BOM LINE

    There is an item marked as floor stock in either BOM Entry (Cards | Manufacturing | Bill of Materials) or in Item Engineering window (Cards |Manufacturing | Inventory  |Engineering Data)but not in the other.  If an item is marked as floorstock it should be marked as floorstock in both location.

    Resolution
    Go to either BOM Entry (Cards | Manufacturing | Bill of Materials)or Item Engineering(Cards |Manufacturing | Inventory  |Engineering Data) and mark or unmark the floorstock option for the appropriate parent and component record.  

53. ITEM ENGINEERING MAKE/BUY CODES DO NOT MATCH IV QUANTITY MASTER REPLENISHMENT METHODS

    There are records in the Item Engineering table (IVR10015) where the Make/Buy Code doesn't match the Replenishment Method in the Item Quantity Master table (IV00102).  

    Resolution
    Go to the Item Resource Planning Maintenance window (Cards |Inventory |Item Resource Planning) and select the Default Site for the item in question.  Verify that the Replenishment Method is correct.  Go to the Item Engineering Data window (Cards | Manufacturing | Inventory | Engineering Data) and verify that the Replenishment Method here matches the method for the item's Default Site.

54. ITEM ENGINEERING RECORD IS MISSING ITEM MASTER RECORD

    There is an item record in the Item Engineering table (IVR10015) without a matching record in Item Master (IV00101).  This is usually an indication of an item that was deleted or imported improperly.

    Resolution:
    There are two options for resolution.

    Either add the item number in question in the Item Maintenance window (Cards | Inventory | Items), save the item, and then delete the newly added item.  This will remove the record for the item from both tables.  
    Or use SQL to remove the record from the Item Engineering (IVR10015) table.  

    Use the following scripts to first display the record to be removed and then delete that record.  Replace the XXX below with the item number to be deleted.

    To determine the records in the IVR10015 run the following script

    ```sql
    select * from IVR10015 where ITEMNMBR='XXX'
    ```

    To remove the records from the IVR10015 run the following script

    ```sql
    delete IVR10015 where ITEMNMBR='XXX'
    ```

55. ITEM IS MISSING THE STANDARD COST ROLLUP ACCOUNT

    There are items that have a periodic valuation method but no standard cost rollup account in the IC COST Item Master (CT00102) table.  

    Resolution:
    Go to Item Maintenance window (Cards | Inventory | Item) and pull up the item, click on the Accounts button and enter a Standard Cost Revaluation account in the Manufacturing accounts window (called Item Account Maintenance – Costing).

56. ITEM MASTER AND IC COST ITEM MASTER HAVE DIFFERENT VALUATION METHODS

    There are items where the valuation method (VCTNMTHD) stored in the Inventory Item Master table (IV00101) and IC COST Item Master CT00102 does not match.  

    Resolution:
    There are two possible methods for resolving.  
    If the IV00101 is wrong, use the Change Valuation utility (Tools | Utilities |Inventory) to change the valuation in this table.  

    If the CT00102 is wrong, then update this table via SQL.  Use the following SQL scripts to display and then update the records to be changed.  Replace the XXX with the item number in question.  

    To determine the records in the CT00102 run the following script.

    ```sql
    select a.ITEMNMBR,a.VCTNMTHD,b.VCTNMTHD from CT00102 a join IV00101 b on a.ITEMNMBR=b.ITEMNMBR where a.VCTNMTHD<>b.VCTNMTHD and a.ITEMNMBR='XXX'
    ```

    To update the records from the CT00102 run the following script.

    ```sql
    update a set a.VCTNMTHD=b.VCTNMTHD from CT00102 a join IV00101 b on a.ITEMNMBR=b.ITEMNMBR where a.VCTNMTHD<>b.VCTNMTHD and a.ITEMNMBR='XXX'
    ```

57. ITEM MASTER MISSING IC COST STANDARD ITEM DEFAULT FOR A STANDARD COST ITEM

    There are items that have a periodic valuation method, but no record in the CT00003.

    Resolution:
    Run the following script to add the missing record(s) into the CT00003 table.  

    ```sql
    INSERT INTO CT00003 (ITEMNMBR, ITEMDESC, ITMCLSCD, MODIFDT, MDFUSRID, COST_I, EFFECTIVEDATE_I, FIXAMTORPCT_I, Fixed_Overhead_Amount, FIXOHDPCT_I, FIXOHDEFFDATE_I, VARAMTORPCT_I, Variable_Overhead_Amount, VAROHDPCT_I, VAROHDEFFDATE_I, PENDINGCOST_I, PENDEFFDATE_I, PENDFIXAMTORPCT_I, PENDFIXOHDAMT_I, PENDFIXOHDPCT_I, PENDFIXOHDEFFDATE_I, PENDVARAMTORPCT_I, PENDVAROHDAMT_I, PENDVAROHDPCT_I, PENDVAROHDEFFDATE_I)
    SELECT ITEMNMBR, ITEMDESC, ITMCLSCD, '1900-01-01 00:00:00.000', 'sa', STNDCOST, '1900-01-01 00:00:00.000', 0, 0, 0, '1900-01-01 00:00:00.000', 0, 0, 0, '1900-01-01 00:00:00.000', 0, '1900-01-01 00:00:00.000', 0, 0, 0, '1900-01-01 00:00:00.000', 0, 0, 0, '1900-01-01 00:00:00.000' FROM IV00101 where ITEMNMBR not in (select ITEMNMBR from CT00003) and VCTNMTHD>3
    ```

58. ITEM MASTER RECORD IS MISSING ITEM ENGINEERING RECORD

    There is an item record in the Item Master table (IV00101) without a matching record in Item Engineering (IVR10015).  

    Resolution:
    Go to the Item Engineering window (Cards | Manufacturing | Inventory | Engineering Data) and enter the correct information for that item.  Or you may run the Manufacturing Inventory Check Links procedure (File | Maintenance | Check Links).  

59. ITEM PRIMARY VENDOR MISSING ITEM/VENDOR MASTER RECORD

    There is an item that has a primary vendor defined for a site in the Item Quantities Maintenance window (Cards | Inventory |Quantities/Sites) but does not have the Item/Vendor relationship defined.  

    Resolution:
    Go to the Item Vendors Maintenance window (Cards | Inventory | Vendor) and set up the item vendor relationship for the listed item number and vendor combination.  

60. ITEMS DO NOT HAVE ALL THEIR ACCOUNTS SET UP AND MAY CAUSE GL JOURNAL ERRORS WHEN POSTING

    There are items missing GL accounts.  If the client is not tracking a certain cost bucket and have not entered GL accounts for these cost buckets, the system will still indicate that they may be missing a record.  

    Resolution:
    Go to Item Maintenance (Cards | Inventory | Item) and check what accounts are setup on the Item Maintenance (Cards | Inventory | Item) Costing Accounts screen.  

61. ITEMS ON PICKDOCS FOR OPEN MOs DO NOT HAVE CORRESPONDING RECOREDS IN THE MOP1400 TABLE

    There are Issue, Reverse Issue, Scrap, and Reverse Scrap transactions that exist in the MOP_PickDoc_Master (MOP1200) and MOP_PickDoc_Line (MOP1210) but not in the MOP_Picklist_Sites_QTYS (MOP1400).  

    Resolution:
    You will need to add to or update the corresponding records in the MOP_Picklist_Sites_QTYS (MOP1400) via SQL.  If you need assistance creating the insert statement, MBS Professional Services will need to be contacted.

62. ITEMS ON PICKDOCS FOR OPEN MOs DO NOT HAVE CORRESPONDING RECORDS IN THE PK010033 TABLE

    There are Issue, Reverse Issue, Scrap and Reverse Scrap transactions that exist in the MOP_PickDoc_Master (MOP1200) and MOP_PickDoc_Line (MOP1210) but not in the Picklist File table (PK010033).

    Resolution:
    You will need to add the corresponding records to the PK010033 via SQL.  You may also be able to accomplish this by building the picklist again in the MO Entry window (Transactions |Manufacturing| Manufacturing Orders).

63. LABOR CODE EFFECTIVE DATE IN THE FUTURE

    There are Labor Codes with a Fixed Overhead Effective Date that is after the current date.

    Resolution:

    Go to the Labor Code Definition window (Cards |Manufacturing | Labor Codes) and verify the date.  If necessary change the date and the Shop Rate.  If you use standard costing then roll up and revalue the Standard Costs.  

64. LABOR CODE FIXED OH EFFECTIVE DATE IN THE FUTURE

    There are Labor Codes with a Fixed Overhead Effective Date that is after the current date.

    Resolution:
    Go to the Labor Code Definition window (Cards |Manufacturing | Labor Codes) and verify the date.  If necessary change the date and the Fixed Overhead values.  If you use standard costing then roll up and revalue the Standard Costs.

65. LABOR CODE VARIABLE OH EFFECTIVE DATE IN THE FUTURE

    There are Labor Codes with a Variable Overhead Effective Date that is after the current date.  

    Resolution:
    Go to the Labor Code Definition window (Cards |Manufacturing| Labor Codes) and verify the date.  If necessary change the date and the Variable Overhead values.  If you use standard costing then roll up and revalue the Standard Costs.  

66. LEAD TIME IS NEGATIVE

    There are items in the Item Engineering File table (IVR10015) where the lead time is a negative number.  

    Resolution:
    If the item is a bought or either item, go to Item Vendor Maintenance (Cards |Inventory | Vendor) and check all assigned vendors to insure that the lead time is positive.  If the item is a made or either item, go to Routing Entry (Cards |Manufacturing | Routing and check the primary routing.  Then, run the Calculate Manufacturing Lead Time (Tools | Utilities | Manufacturing |Calc MFG Lead Times).  

67. LEAD TIME IS ZERO

    There are items in the Item Engineering File table (IVR10015) where the Make/Buy Code is 1 or 2 and the lead time (in the same table) is set to 0. The lead time for the listed item (with a Make/Buy Code of Make or Either) is zero.  

    Resolution:
    Go to Routing Entry (Cards | Manufacturing |Routing | Routing Entry) and make sure that there is a valid primary routing for the item.  Then, run the Calculate Manufacturing Lead Time (Tools | Utilities | Manufacturing |Calc MFG Lead Times).

68. MACHINE CODE EFFECTIVE DATE IN THE FUTURE

    There are Machine IDs with an Operating Cost Effective Date that is after the current date.  

    Resolution:
    Go to the Machine Definition window (Cards | Manufacturing |Machines) and verify/change the Operating Cost and its Effective Date.  If changes are made, perform a Roll Up and Revalue (Tools | Routines |Manufacturing | Rollup and Revalue) to ensure that the standard costs are updated for the affected items.  

69. MACHINE CODE FIXED OH EFFECTIVE DATE IN THE FUTURE

    There are Machine IDs with a Fixed Overhead Effective Date that is after the current date

    Resolution:
    Go to the Machine Definition window (Cards | Manufacturing | Machines) and verify/change the Fixed Overhead value and its Effective Date.  If changes are made, perform a Roll Up and Revalue (Tools | Routines |Manufacturing | Rollup and Revalue) to ensure that the standard costs are updated for the affected items.  

70. MACHINE CODE VARIABLE OH EFFECTIVE DATE IN THE FUTURE

    There are Machine IDs with a Variable Overhead Effective Date that is after the current date.  

    Resolution:
    Go to the Machine Definition window (Cards |Manufacturing | Machines) and verify/change the Variable Overhead value and its Effective Date.  If changes are made, perform a Roll Up and Revalue (Tools | Routines |Manufacturing | Rollup and Revalue) to ensure that the standard costs are updated for the affected items.  

71. MADE ITEM DOES NOT HAVE A BOM

    There is an item with a Make/Buy code of Make but does not have a BOM.  

    Resolution:  
    Go to BOM Entry (Cards | Manufacturing | Bill of Materials) to create a BOM for that item.  

72. MADE ITEM DOES NOT HAVE A PRIMARY ROUTING

    There is an item that has a Make/Buy code of Make, but has no primary routing.

    Resolution:
    Go to the Routing Entry (Cards | Manufacturing | Routing |Routing Entry) to either create a new primary routing or edit an existing routing.  The Header Routing Window may also be used specify an existing routing as a primary routing.  To get to this window go to the Routing Entry window(Cards| Manufacturing | Routing| Routing Entry), enter your item and routing name, click on the Routing Name link, and select the correct status for that routing.  

73. MADE ITEM DOES NOT HAVE A ROUTING

    There is an item that has a Make/Buy code of Make, but no routing has been created for that item.  

    Resolution:
    Go to the Routing Entry (Cards | Manufacturing | Routing |Routing Entry) window to create a routing for the item.  

74. MANUFACTURE ORDER ON PICKLIST DOES NOT EXIST IN THE MO MASTER TABLE

    There is a Manufacturing Order that does not exist in the Manufacturing Order Master table (WO010032) but does exist in the Picklist File table (PK010033).  

    Resolution:
    Verify you are unable to pull up the manufacturing order in MO Entry (Transactions | Manufacturing | Manufacturing Orders).  If you are unable to pull up the MO then use SQL to remove the rows from the the Picklist File table (PK010033).

    To determine the records in the PK010033 run the following script.

    ```sql
    Select * from PK010033 where MANUFACTUREORDER_I not in (select MANUFACTUREORDER_I from WO010032)
    ```

    To remove the records from the PK010033 run the following script.

    ```sql
    Delete PK010033 where MANUFACTUREORDER_I not in (select MANUFACTUREORDER_I from WO010032)
    ```

75. MINIMUM ORDER QUANTITY IS GREATER THAN MAXIMUM ORDER QUANTITY

    There is an item where the value in the Minimum Qty.  field is greater than the value in the Maximum Qty field.  

    Resolution:
    Go to the Item Engineering window (Cards | Manufacturing | Inventory | Engineering Data), enter the item number; correct the quantity values so that the maximum is greater than the minimum, and save the record.

76. MISSING MOP1027 RECORDS

    There are posted issued pick documents in the MOP_PickDoc_Master (MOP1200) and MOP_PickDoc_Line (MOP1210) that are not included in the Manufacture Order Lot Issue table (MOP1027).  The MOP1027 table stores all records of the pick numbers that should have updated the Inventory subledger and cross references the manufacturing and inventory document numbers.  

    Resolution:
    Use the information in the MOP_PickDoc_Master (MOP1200), the MOP_PickDoc_Line (MOP1210), Manufacture Order Activity (MOP10213), and inventory history tables to insert records into the MOP1027 via SQL.  

77. MISSING ORIGINATING PICK NUMBER

    There are records in the MOP_PickDoc_Line MOP1210 with transaction type (TRX_TYPE) of 2 (Reverse Issue), 4 (Reverse Allocate), or 6 (Reverse Scrap) that do not have any value in the ORIGPICKNUMBER field.  If this is a reversing transaction it should indicate document number it is reversing.  

    Resolution:
    Go to Component Transaction Entry (Transactions | Manufacturing | Manufacturing Orders | Component Transaction Entry) and verify that the Pick Numbers referenced are valid.  

78. MISSING RECORD IN IV30300 FOR ISSUE PICK DOC

    These are issue pick documents in the MOP_PickDoc_Line (MOP1210) that do not have corresponding records in the Inventory History table (IV30300

    Resolution:
    Post all batches in the Inventory subledger.  If transactions were removed from Inventory history, this message could appear.  Don't remove any records in the Manufacturing tables but do troubleshoot to see if the Inventory subledger continues to not be updated.  

79. MOP10213 PICKNUMBER NOT IN MOP1200

    There are pick documents that are referenced in the MO Activity table (MOP10213) and the MOP_PickDoc_Line (MOP1210) but missing from the MOP_PickDoc_Master (MOP1200).  

    Resolution:
    Using detailed information from the MOP1210 and MOP10213 tables, insert a record in the MOP1200 table via SQL.

80. MOP1400 QUANTITY ALLOCATED DOES NOT MATCH MOP1210

    These are records where the sum of the allocated quantities for an MO, item and site in the MOP_PickDoc_Line (MOP1210) do not match the total allocated for that MO, item and site in the MOP_Picklist_Site_QTYS (MOP1400).  

    Resolution:
    Verify that the allocate pick document records in the MOP1210 table are accurate.  If so, update the Quantity Allocated (ATYALLOC) in the MOP1400 to the correct quantity.

81. MOs WHICH HAVE HAD THEIR STATUS CHANGED FROM CLOSED AFTER CLOSING THE MO

    There are records in the MO Activity table (MOP10213) where MOs had a status of closed and then were changed to a different status.

    Resolution:
    Go to Manufacturing Order Entry (Transactions | Manufacturing | Manufacturing Orders | MO Entry) and verify that the MO status is currently correct.  Attempt to determine what may have caused the MO to be moved from a closed status.  The process to close the MO again will vary depending on what additional processing has occurred.

82. MULTIPLE ITEM NUMBERS FOR THE SAME PICKLIST SEQUENCE

    There are multiple item numbers on the same picklist or pick document using the same picklist sequence number.  Both the MOP_PickDoc_Line  (MOP1210) and Picklist File (PK010033) tables contain the picklist sequence number and are read to determine this.

    Resolution:
    Fix for this may be varied depending on what processing has occurred to this point.  Contact support for further assistance.

83. NEGATIVE MRP QUANTITY MODIFIER VALUE

    There is an item with a negative value in the Minimum Quantity, Average Quantity, Order Increment, Maximum Quantity, Standard Quantity, or Order Increment field.

    Resolution:
    Go to the Item Engineering window (Cards | Manufacturing | Inventory |Engineering Data), enter the item number, then correct the negative number and save the record.

84. NEGATIVE PRIMARY VENDOR LEAD TIME

    There is an item/vendor combination that is where the Planning Lead Time is a negative amount.

    Resolution:
    Go to the Item Vendors Maintenance window (Cards | Inventory | Vendors), enter the item number and primary vendor, enter the correct Planning Lead Time, and save the record.

85. NEGATIVE ROUTING TIMES

    The routing sequence has a negative value in the setup time, labor time, machine time, queue time, or move time

    Resolution:
    Go to the Routing Entry window (Cards | Manufacturing |Routing |Routing) to view and change any negative values for that routing steps.

86. NO IV30300 FOR IVDOCNBR REFERENCED IN MOP10213

    There are IV Adjustment records in the MO Activity table (MOP10213) but there are not corresponding IV adjustments in the Inventory History tables.

    Resolution:
    If transactions were removed from Inventory history, this message could appear.  Don't remove any records in the Manufacturing tables but do troubleshoot to see if the Inventory subledger continues to not be updated.

87. NO LEAD TIME FOR PRIMARY VENDOR

    There is an item/vendor combination that is missing the Planning Lead Time.

    Resolution:
    Go to the Item Vendors Maintenance window (Cards | Inventory | Vendor), enter the item number and primary vendor, enter the correct Planning Lead Time, and save the record.

88. NO MFG BOM FOR MADE STANDARD COST ITEM

    There are make items with periodic valuations that do not have a Manufacturing BOM.  A Manufacturing BOM is required for the standard costs to roll up properly for make items.

    Resolution:
    Go to the BOM Entry (Cards | Manufacturing | Bill of Materials) and enter a MFG BOM.

89. NO PRIMARY LOCATION ESTABLISHED

    There is no primary location for the listed item.

    Resolution:
    Go to the Item Quantities Maintenance window (Cards | Inventory |Quantity/Sites), enter the item number, enter a Default Site ID, and save the record.

90. NO STANDARD ORDER QUANTITY ESTABLISHED

    There is an item with an order policy of Fixed Order Quantity that does not have a Standard Order Quantity.

    Resolution:
    Go to the Item Resource Planning window (Cards | Inventory | Item Resource Planning), enter the item number and the site enter the correct Standard Order Quantity, and save the record.

91. PERIODIC ITEM IN PERPETUAL BOM

    There is a child item that has a valuation method of Periodic (standard cost), but the parent item is Perpetual (actual cost).  Depending on your setup this may or may not be acceptable.  Some sites do choose to have periodic items in perpetual BOMS.

    Resolution:
    If the child item should not have a valuation method of periodic go to BOM Entry (Cards | Manufacturing | Bill of Materials) and remove the item from the BOM or go to Change Valuation Method (Tools | Utilities | Inventory | Change Valuation Method) and change the valuation method.

92. PERPETUAL ITEM IN PERIODIC BOM

    There is a child item that has a valuation method of Perpetual (actual cost), but the parent item is Periodic (standard cost).

    Resolution:
    Go to BOM Entry (Cards | Manufacturing | Bill of Materials) and remove the item from the BOM or go to Change Valuation Method (Tools | Utilities | Inventory | Change Valuation Method) and change the valuation method.

93. PICKLIST MO STATUS DOES NOT MATCH THE MO MASTER TABLE'S MO STATUS

    There is an MO status on the picklist does not match what is stored in the MO Master table (Wo010032).

    Resolution:
    Go to Manufacturing Order Entry (Transactions | Manufacturing | Manufacturing Orders | Entry )and pull up the MO.  Press the Save button and this will update the picklist with information from the master.

94. POSITION NUMBERS DO NOT MATCH IN BM010200 AND TARD1001

    There are position numbers for components in Reference Designators table (TARD1001) do not match the position numbers for these components in the BOM Routing Link table(BM010200).

    Resolution:
    If you use Reference Designators you will need to go to BOM Entry (Cards | Manufacturing | Bill of Materials) and reenter the reference designators for specific BOMs.  If you are not using Reference Designators this error will not cause further issues.

95. POSITION NUMBERS DO NOT MATCH IN BM10115 AND BM010200

    The position numbers for components in the BOM Line File table (BM010115) do not match the position numbers for these components in the BOM Routing Link table (BM010200).

    Resolution:
    Go to BOM Routing Link (Cards | Manufacturing | Bill of Materials |GoTo | BOM Routing Link)and delete linked component and readd it.

96. POSITION NUMBERS DO NOT MATCH IN BM10115 AND TARD1001

    The position number for components in the BOM Line File table (BM010115) do not match the position numbers  for the components  in Reference Designators table (TARD1001).

    Resolution:
    If you use Reference Designators you will need to go to BOM Entry (Cards | Manufacturing | Bill of Materials) and reenter the reference designators for specific BOMs.  If you are not using Reference Designators this error will not cause further issues.

97. POSITION NUMBERS DO NOT MATCH IN MOP1210 AND MOP1110

    The postion number for the components on the pick document (MOP1210)do not match the postion numbers for the same components on the MO Receipt (MOP1110).

    Resolution:
    Do not complete a reverse receipt.  If you do a reverse receipt the item with the incorrect postion number will not get reversed out when the reverse receipt is completed.Call the support desk for further assistance.

98. POSITION NUMBERS DO NOT MATCH IN PK010033 AND MOP1110

    The postion number for the components on the Picklist File table (PK010033) do not match the postion numbers for the same components on the MOP_Receipt_Line table (MOP1110).

    Resolution:
    Do not complete a reverse receipt.  Do not do a reverse receipt the item with the incorrect postion number will not get reversed out when the reverse receipt is completed.Call the support desk for further assistance.

99. POSITION NUMBERS DO NOT MATCH IN PK010033 AND MOP1210

    The postion number for the components on the picklist do not match the postion numbers for the same components on the pick document.  Do not do a reverse issue.  The items will reverse out but there will still be pending transaction in the Manufacture Order Pending Bin (MOP1025) and MOP_Picklist_Site_QTYS (MOP1400) tables which will prevent the MO Close from processing.

    Resolution:
    Call the support desk for further assistance.  

100. POTENTIAL NEGATIVE ALLOCATIONS

     There are component items on Manufacturing Orders that have a negative value for the total quantity allocated.

     Resolution:
     Run an Inventory Reconcile (Tools | Utilities | Inventory | Inventory Reconcile) to correct the negative allocation.

101. POTENTIAL OVERALLOCATION

     There are items where the Quantity Allocated by manufacturing transactions exceeds the Quantity On Hand for an Item/Site record.

     Resolution:
     Run an Inventory Reconcile (Tools | Utilities | Inventory | Inventory Reconcile) to correct the negative allocation.

102. PRIMARY VENDOR QUANTITIES MODIFIERS NOT SETUP

     There is a buy item where the value set up in any of the following fields, Minimum Order, Average Order, or Order Increment, in the Item Vendors Maintenance (Cards |Inventory | Vendors), for the item's Primary Vendor, does not agree with the corresponding value set up in the Item Engineering window (Cards | Manufacturing | Inventory |Item Engineering), or is zero.

     Resolution:
     Go to the Item Vendor Maintenance window (Cards |Inventory | Vendors), enter the Item Number and Primary Vendor; enter the correct amounts in the above fields, and save the record.

103. QTY RECEIVED IN MOP1000 INACCURATE

     There are records in the MOP WIP Stack table (MOP1000) that do not match the Quantity Received in WIP for the same components as tracked in the MOP_PickDoc_Line (MOP1210) and MOP_Receipt_Detail (MOP1110) tables.

     Resolution:
     Determine if this issue is impacting only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

104. QTY_ISSUED_I IS GREATER THAN TRXQTY

     These are pick documents from the MOP_PickDoc_Line (MOP1210) where the QTY_ISSUED_I is greater than the TRXQTY.

     Resolution:
     Determine if this is only one pick document or numerous pick documents.  If this is more than one pick document look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

105. QTYSOLD IN MOP1000 IS INACCURATE

     There are records in the MOP WIP Stack table (MOP1000) where the Quantity Consumed out of WIP does not match the Quantity Consumed from WIP for the same components as tracked in the MOP_PickDoc_Line (MOP1210) and MOP_Receipt_Detail (MOP1110) tables.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

106. QUANTITIES IN MOP1400 ARE INCORRECT

     There are records in the MOP_Picklist_Sites_QTYS table (MOP1400) where the Pending Reverse Issue and Pending Scrap quantities are greater than the Quantity Issued or the Pending Reverse Scrap quantities are greater than the Quantity Scrapped.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

107. REVERSAL TRANSACTION SITES ARE NOT REVERSED

     There is a Reverse Issue, Reverse Allocate, or Reverse Scrap transaction from the MOP_PickDoc_Line (MOP1210) where the sites do not mirror the sites on the original Issue, Allocate, or Scrap transactions.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

108. REVERSE ALLOCATE QUANTITY ALLOCATED DOES NOT EQUAL ZERO

     There are records in the MOP_PickDoc_Line table (MOP1210) for Reverse Allocate Pick Numbers and have a quantity allocated (ATYALLOC) not equal to zero.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

109. ROUTING FOR INVALID PARENT ITEM

     The parent item defined in the Routing_MSTR table (RT010001) does not have a corresponding record in the Item Master table (IV00101).

     Resolution:
     Remove the header record from the table (RT010001).  Also check the Routing Line table (RT010130) to insure that there are no routing steps with that invalid parent part.

     To determine the records in the RT010001 run the following script.

     ```sql
     select * from RT010001 where ITEMNMBR not in (select ITEMNMBR from IV00101)
     ```

     To remove the records from the RT010001 run the following script.

     ```sql
     delete RT010001 where ITEMNMBR not in (select ITEMNMBR from IV00101)
     ```

110. ROUTING LINE RECORD WITH NO ROUTING HEADER

     There is a record in the Routing_Line table RT010130 that has no corresponding header record in the table Routing_MSTR table (RT010001).

     Resolution:
     Remove the record from the Routing Line table (RT010130).

     To determine the records in the RT010130 run the following script

     ```sql
     select * from RT010130 where ITEMNMBR not in (select ITEMNMBR from rt010001)
     ```

     To remove the records from the RT010130 run the following script

     ```sql
     delete RT010130 where ITEMNMBR not in (select ITEMNMBR from RT010001)
     ```

111. STANDARD COST BOUGHT ITEM IS MISSING AN IC COST STANDARD ITEM DEFAULTS RECORD

     There is an item record in the Item Master table (IV00101) for a bought item that is missing a record.

     Resolution:
     To create the record, enter material costs through the Standard Item Material Costs window (Cards |Manufacturing| Inventory | Standard Item Mat Cost).

112. STANDARD COST ITEM IS MISSING AN IC_IV_STANDARD RECORD

     There is an item record in the Item Master table (IV00101) without a matching record in the IC_IV_Standard table (ICIV0323).

     Resolution:
     To create the record go into the Item Maintenance window (Cards | Inventory | Item) window and hitting the save button should create it.  If that does not work, the standard cost tables may need to be rebuilt.  

113. SUBASSEMBLY COMPONENT MISSING BOM TYPE

     There is a child part item number that has an item Engineering Make/Buy code of Make does not have BOM type information.

     Resolution:
     Go to the BOM Entry (Cards | Manufacturing | Bill of Materials) window, select the parent number from the report, and re-add the sub-assembly.  If the item is on several BOMs you can use the BOM Mass Update (Tools |Utilities| Manufacturing | BOM Mass Update) to update all of the BOMs at once.

114. TABLE XXXXX HAS BOM SEQUENCES THAT ARE 0

     This error indicates various tables have BOM Sequence numbers that are 0.

     Resolution:
     Note which table the error indicates and call the help desk for assistance.

115. TABLE XXXXX HAS POSTION NUMBERS THAT ARE 0

     This error indicates various tables have position numbers that are 0.

     Resolution:
     Note which table the error indicates and call the help desk for assistance.

116. TRX QTY EQUALS ZERO

     There are records in the MOP_PickDoc_Line (MOP1210) for pick documents that have a Transaction Quantity (TRXQTY) of zero.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

117. TRX TYPE ZERO EXISTS IN MOP1200

     There are pick document in the MOP_PickDoc_MASTER (MOP1200) that do not have a valid Transaction Type.  You will not be able to pull this pick document up in Component Transaction Entry.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

118. TRX TYPES DO NOT MATCH

     There are pick document in the MOP_PickDoc_Line table (MOP1210) and MOP_PickDoc_MASTER table (MOP1200) that did not have the same Transaction Type in both tables.

     Resolution:
     Determine if this is only one MO or numerous MOs.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

119. WIP COSTS OUT IN MOP1002 NOT EQUAL TO SUM OF RECEIPT COSTS

     There are records in the MOP_WIP_Cost table (MOP1002) where the WIP Costs Out does not equal the sum of the costs recorded in the MOP_Receipt_Master table (MOP1100) for the same MO.

     Resolution:
     If possible reverse out any component associated with this manufacturing order and close the  manufacturing order.  If this is more than one MO look for trends to determine what is causing the issue.  Many times these types of issues are caused by posting interruptions.  Watch when you close the MO.  There may be variances caused by incorrect values in this table.  If this variance is not correct do not post the variance to GL or if it was posted do a manual GL adjustment to correct the value.

## See also

[Manufacturing Setup - Part 1: Manufacturing setup](manufacturing-setup-part-1.md)  
[Glossary of Terms in Manufacturing](glossary-manufacturing.md)  
