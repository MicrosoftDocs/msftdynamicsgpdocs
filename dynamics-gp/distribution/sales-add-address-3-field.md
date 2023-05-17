---
title: Add the Address 3 field to Sales Documents
description: Learn how you can add the Address 3 field to sales documents and also exclude blank addresses from the reports.
ms.date: 10/23/2020
ms.topic: article
ms.prod: dynamics-gp
author: jswymer
ms.author: jswymer
---

# Add the Address 3 Field to Sales Documents

This article describes how to add the Address 3 field to reports for the following documents in Sales Order Processing in Dynamics GP:

- Order

- Invoice

- Quote

- Return

Address fields that are blank are suppressed.

## Step 1: Back up the report

1. If you have any modified Microsoft Dynamics GP reports, back up the Reports.dic file. To locate the Reports.dic file, follow these steps:

  1. In Dynamics GP, point to **Tools**, point to **Setup**, point to **System**, and then choose **Edit Launch File**.

      > [!NOTE]
      > If you are prompted, type the system password.

  2. Note the path that appears in the **Reports** box.
  3. Choose OK to close the **Edit Launch File** window.

## Step 2: Open the report

1. In Dynamics GP, point to **Tools**, point to **Customize**, and then choose **Report Writer**.
2. In Dynamics GP, choose **Microsoft Dynamics GP** in the **Product** list, and then choose **OK**.
3. Choose **Reports**.
4. Optionally, if this is the first time that the report has been modified, choose the report that you want to modify in the **Original Reports** list, and then choose **Insert**.
5. In the **Modified Reports** area, choose the report, and then choose **Open**.

## Step 3: Modify a calculated field

1. Choose **Layout**.
2. In the **Toolbox** window, choose **Calculated Fields** in the resource list.
3. Choose **Bill To Address Line 1**, and then choose **Open**.
4. In the **Expressions** area, choose *""* that appears immediately after *RM\_Customer\_MSTR.Address2* in the **Calculated** field.
5. Choose the **Fields** tab.
6. In the **Resources** list, choose **Customer Master Address** File.
7. In the **Field** list, choose **Address 3**, and then choose **Add**.
8. In the **Expressions** area, choose *""* that appears immediately after *RM\_Customer\_MSTR.Address3*, choose **Remove**, and then choose **OK**.

    > [!NOTE]
    > The calculated expression should be as follows.
    >  
    > `FUNCTION\_SCRIPT (rw\_SelectAddrLine 1 "" RM\_Customer\_MSTR.Address1 RM\_Customer\_MSTR.Address2 RM\_Customer\_MSTR.Address3 "" RM\_Customer\_MSTR.City RM\_Customer\_MSTR.State RM\_Customer\_MSTR.Zip "")`

9. Repeat steps 2 through 8 to modify the Bill To Address Line 2 field and the Bill To Address Line 3 field.

## Step 4: Create a calculated field

1.  In the **Toolbox** window, choose **Calculated Fields**, and then choose **New**.
2.  In the **Name** field, type **Bill To Address 4**.
3.  In the **Result Type** list, choose **String**.
4.  In the **Expression Type** area, choose **Calculated**.
5.  Choose the **Functions** tab, and then choose **User Defined**.
6.  In the **Core** list, choose **System**.
7.  In the **Functions** list, choose *RW\_SelectAddrLine*, and then choose **Add**.
8.  Choose the **Constants** tab. Then, choose **Integer** in the **Type** list.
9.  In the **Constant** field, type **4** , and then choose **Add**.
10.  In the **Type** list, choose **String**, and then choose **Add**.
11.  Choose the **Fields** tab, and then choose **Customer Master Address File** in the
**Resources** list.
12.  In the **Field** list, choose **Address 1**, and then choose **Add**.
13.  In the **Resources** list, choose **Customer Master Address File**.
14.  In the **Field** list, choose **Address 2**, and then choose **Add**.
15.  In the **Resources** list, choose **Customer Master Address File**.
16.  In the **Field** list, choose **Address 3**, and then choose **Add**.
17.  Choose the **Constants** tab.
18.  In the **Type** list, choose **String**, choose **Add**, and then choose **OK**.
19.  In the **Resources** list, choose **Customer Master Address File**.
20.  In the **Field** list, choose **City**, and then choose **Add**.
21.  In the **Resources** list, choose **Customer Master Address File**.
22.  In the **Field** list, choose **State**, and then choose **Add**.
23.  In the **Resources** list, choose **Customer Master Address File**.
24.  In the **Field** list, choose **Zip**, and then choose **Add**.
25.  Choose the **Constants** tab.
26.  In the **Type** list, choose **String**, choose *1*, and then choose **OK**.
27.  In the **Type** list, choose **String**, choose **Add**, and then choose **OK**.

    > [!NOTE]
    > The calculated expression should be as follows:
    >
    > `FUNCTION\_SCRIPT (rw\_SelectAddrLine4 "" RM\_Customer\_MSTR.Address1 RM\_Customer\_MSTR.Address2 RM\_Customer\_MSTR.Address3 "" RM\_Customer\_MSTR.City RM\_Customer\_MSTR.State RM\_Customer\_MSTR.Zip "")`

28.  In the **Toolbox** window, choose **Bill To Address 4**.
29.  Drag the **Bill To Address 4** field to the report layout, and then resize the field as necessary.

> [!NOTE]
> You can repeat the same steps for the **Ship To Address** field. However, you have to use the **Sales Transaction Work** table instead of the **Customer Master Address** table. Additionally, the calculated fields have `SOP\_HDR\_WORK.\*` instead of `RM\_Customer\_MSTR.\*`.

## Step 5: Save the modified report

1.  Close the report.
2.  When you are prompted to save the changes, choose **Save**.
3.  In the **Report Definition** window, choose **OK**.
4.  Choose **Microsoft Dynamics GP** on the **File** menu.

## Step 6: Assign security permissions to the modified report

1.  On the Microsoft Dynamics GP menu, point to **Tools**, point to **Setup**, point to **System**, and then choose **Alternate/Modified Forms and Reports**.
2.  In the **ID** box, type the ID of the user who will print this modified report.
3.  In the **Product** list, choose **Microsoft Dynamics GP**.
4.  In the **Type** list, choose **Reports**.
5.  Expand the **Sales** folder.
6.  Expand the **Report\_name** folder.
7.  Choose **Microsoft Dynamics GP (Modified)**.

    A check mark appears at the beginning of the name.

8.  Choose Save.

## See also
