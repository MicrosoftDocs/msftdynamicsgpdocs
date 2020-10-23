---
title: Modify the SOP Blank Invoice Form Report
description: Learn how to customize the SOP Blank Invoice Form report in Sales Order Processing in Dynamics GP by changing two address fields and make it print more than four line item comments.
ms.date: 10/23/2020
ms.topic: article
ms.prod: dynamics-gp
author: edupont04
ms.author: edupont
---

# Modify the SOP Blank Invoice Form Report

In this article, you can learn how to modify the SOP Blank Invoice Form report in Sales Order Processing in Dynamics GP so that it prints more than 4 line item comments and includes customized address fields.

We recommend that you always start by backing up your reports before you begin a new modification.

## Back up the report

1. If the existing Microsoft Dynamics GP reports have been modified, back up the Reports.dic file.

    1. To locate the Reports.dic file, in Microsoft Dynamics GP, point to **Tools** on the **Microsoft Dynamics GP** menu, point to **Setup**, point to **System**, and then choose **Posting Accounts**.

    2. If you are prompted to enter the system password, type your password, and then choose OK.

    3. Note the path that appears in the **Reports** box.

    4. Choose **OK** to close the **Edit Launch File** window.

## Modify the address fields

This section describes how to modify the following fields on the **SOP Blank Invoice Form** report in Sales Order Processing in Microsoft Dynamics GP:

- The **Bill To Address Line** field

- The **Ship To Address Line** field

Additionally, this section describes how to add a comma character (,) between the **City** field and **State** field in the **Ship To Address Line 3** field.

To modify the **Bill To Address Line** field and **Ship To Address Line** field on the **SOP Blank Invoice Form** report, follow these steps:

1. Create 2 new calculated fields. To do this, follow these steps:

    1. Start **Report Writer**. To do this, choose **Tools**, point to **Customize**, and then choose **Report Writer**.

    2. Choose **Microsoft Dynamics GP** in the **Product** list.

    3. Choose **Reports**.

    4. In the **Original Reports** list, choose **SOP Blank Invoice Form**, and then choose **Insert**.

    5. In the **Modified Reports** list, choose **SOP Blank Invoice Form**, and then choose **Open**.

    6. Choose **Layout**.

    7. In the **Toolbox** window, choose **Calculated Fields** in the **Resources** list, and then choose **New**.

    8. In the **Name** box, type a name for the calculated field. For example, type **City, State, or ZIP** in the **Name** box.

    9. In the **Result Type** list, choose **String**, and then choose **Calculated** in the **Expression Type** box.

    10. On the **Functions** tab, choose **System-Defined**, choose `STRIP` in the **Function** list, and then choose **Add**.

    11. On the **Fields** tab, choose **Customer Master Address File** in the **Resources** list, choose **City** in the **Field** list, and then choose **Add**.

    12. Choose after the last *)* in the **Expressions Calculated** field to close the function.

    13. In the **Operators** area, choose `CAT`.

    14. On the **Constants** tab, choose `String` in the **Type** list, type a comma character and enter a space character in the **Constant** field, and then choose **Add**.

    15. In the **Operators** area, choose `CAT`.

    16. On the **Functions** tab, choose **System-Defined**, choose `STRIP` in the **Function** list, and then choose **Add**.

    17. On the **Fields** tab, choose **Customer Master Address File** in the **Resources** list, choose **State** in the **Field** list, and then choose **Add**.

    18. Choose after the last *)* in the **Expressions Calculated** field to close the function.

    19. In the **Operators** area, choose `CAT`.

    20. On the **Constants** tab, choose `String` in the **Type** list, enter two space characters in the **Constant** field, and then choose **Add**.

    21. In the **Operators** area, choose `CAT`.

    22. On the **Functions** tab, choose **System-Defined**, choose `STRIP` in the **Function** list, and then choose **Add**.

    23. On the **Fields** tab, choose **Customer Master Address File** in the **Resources** list, choose **Zip**, and then choose **Add**.

    24. The following function script appears.

        ```
        STRIP (RM\_Customer\_MSTR\_ADDR.City) \# ", " \# STRIP (RM\_Customer\_MSTR\_ADDR.State) \# " " \# STRIP (RM\_Customer\_MSTR\_ADDR.Zip)**Note** Additionally, you can perform similar steps if you want to add a comma character between the City field and State field in the Ship To Address Line 3 field. To do this, follow steps 2a-2x. However, throughout these steps, choose Sales Transaction Work instead of Customer Master Address File in the Resources list.
        ```

    25. Choose OK.

2. Replace the existing **Bill To Address Line 3** field with the new calculated field. To do this, follow these steps:

    1. In the **Page Header** area of the report layout, choose the **Bill To Address Line 3** field, and then press DELETE.

    2. In the **Toolbox** window, choose the new calculated field that you created in step 2. Then, drag that field to the same location on the report layout where the **Bill To Address Line 3** field was.

    3. Repeat these in the **Report Header** section of the report layout.

3. Replace the existing **Ship To Address Line 3** field with the new calculated field. To do this, follow these steps:

    1. In the **Page Header** area of the report layout, choose the **Ship To Address Line 3** field, and then press DELETE.

    2. In the **Toolbox** window, choose the new calculated field that you created in step 2, and then drag that field to the same location on the report layout where the **Ship To Address Line 3** field was.

    3. Repeat these in the **Report Header** section of the report layout.

        > [!NOTE]
        > Steps 3 and 4 only work if all the customers have at least two lines of address information other than the following fields:
        >
        > - The City field
        > - The State field
        > - The ZIP Code/Postal Code field
        > If all the customers have only one line of address information other than the previously mentioned fields, you must delete the **Bill To Address Line 2** and **Bill To Address Line 3** fields from the report layout.

4. On the **File** menu, choose **Microsoft Dynamics GP**.

5. When you are prompted to save the changes to the report layout, choose **Save**.

6. When you are prompted to save the changes to the report, choose **Save**.

7. Assign security permissions to the modified report

    1. On the **Tools** menu, point to **Setup**, point to **System**, and then choose **Security**.

        > [!NOTE]
        > If you are prompted to enter the system password, type the system password.

    2. In the **User ID** list, choose the identifier who will access the report.

    3. In the **Type** list, choose **Modified Reports**.

    4. In the **Series** list, choose **Sales**.

    5. In the **Access List** box, double-click **SOP Blank Invoice Form**, and then choose **OK**.

> [!NOTE]
> After you choose OK, an asterisk (\*) appears next to the report name.

## Create the calculated fields to display more than four comments

In this section, you learn how to modify the **SOP Blank Invoice Form** report to display more than four line item comments.

1. Start **Report Writer**. To do this, choose **Tools**, point to **Customize**, and then choose **Report Writer**.

2. Choose **Microsoft Dynamics GP** in the **Product** list.

3. Choose **Reports**.

4. In the **Original Reports** list, choose **SOP Blank Invoice Form**, and then choose **Insert**.

5. In the **Modified Reports** list, choose **SOP Blank Invoice Form**, and then choose **Open**.

6. In the **Report Definition** window, choose **Layout**.

7. In the **Toolbox** window, choose **Calculated Fields** in the **Resources** list, and then choose **New**.

8. In the **Calculated Field Definition** window, type *LINE COMMENT1* in the **Name** box.

9. In the **Result Type** list, choose `String`.

10. In the **Expression Type** box, choose **Calculated**.

11. Choose the **Functions** tab, and then choose **User-Defined**.

12. In the **Core** list, choose **System**.

13. In the **Function** list, choose `RW\_SOPLINECommentText`, and then choose **Add**.

14. Choose the **Fields** tab, and then choose **Sales Line Comment Work and History** in the **Resources** list.

15. In the **Field** list, choose **SOP Type**, and then choose **Add**.

16. In the **Field** list, choose **SOP Number**, and then choose **Add**.

17. In the **Field** list, choose **Line Item Sequence**, and then choose **Add**.

18. In the **Field** list, choose **Component Sequence**, and then choose **Add**.

19. Choose the **Constants** tab, and then choose **Integer** in the **Type** list.

20. In the **Constant** field, type **80** , and then choose Add.

    > [!NOTE]
    > The number that you type is the maximum character length of the calculated field that can be printed in Report Writer. You can use a smaller value if you do not require 80 characters.

21. In the **Constant** field, type *1* , and then choose **Add**.

22. Verify that the expression in the Calculated field appears as the following string:

    ```
    FUNCTION\_SCRIPT(RW\_SOPLINECommentText SOP\_LINE\_CMT\_WORK\_HIST.SOP Type SOP\_LINE\_CMT\_WORK\_HIST.SOP Number SOP\_LINE\_CMT\_WORK\_HIST.Line Item Sequence SOP\_LINE\_CMT\_WORK\_HIST.Component Sequence 80 1) **Note** This expression refers to the first line item comment, LINE COMMENT1. To display the other comment lines, you can repeat step 6 through step 20 to create additional calculated fields. When you create these additional calculated fields, you must change the values that you typed in step 7 and in step 20. For example, when you create a calculated field for the second comment line, you must type "LINE COMMENT2" in step 7. You must type "2" in step 20. When you create a calculated field for the third line item comment, you must type "LINE COMMENT3" in step 7. You must type "3" in step 20. Therefore, the expression of the calculated field for the second line item comment must resemble the following string:FUNCTION\_SCRIPT(RW\_SOPLINECommentText SOP\_LINE\_CMT\_WORK\_HIST.SOP Type SOP\_LINE\_CMT\_WORK\_HIST.SOP Number SOP\_LINE\_CMT\_WORK\_HIST.Line Item Sequence SOP\_LINE\_CMT\_WORK\_HIST.Component Sequence 80 2)
    ```
23. Choose **OK**.

24. In the **Report Footer** section of the report, set the visibility of the existing comment fields (labeled *Comment 1* to *Comment 4*) to invisible. To do this, follow these steps:

    1. Double-choose each comment field to open the **Report Field Options** window.

        > [!NOTE]
        > You also can choose **Field options** on the **Tools** menu for each field to open the **Report Field Options** window.

    2. In the **Visibility** field of each comment field, choose **Invisible**.

    3. Choose **OK**.

54. Drag the calculated fields that you created in the Toolbox dialog box to the Report Footer section over the existing comment fields.

26. If you created more than four calculated fields for line item comments, drag the additional comment fields in the Toolbox dialog box to the F2 - Comment 4 section. To expand this section to make room for the additional calculated fields, choose the F2 box, and then drag down the F2 box.

27. Double-choose each field that is added, and then make sure that the display type is Last Occurrence for each field.

28. Choose OK to save the changes.

### Save the changes to the report and exit Report Writer

1. On the **File** menu, choose **Microsoft Dynamics GP**.

2. Choose **Save** when you are prompted to save the changes to the report layout.

3. Choose **Save** when you are prompted to save the changes to the modified report.

4. Exit Report Writer.

### Grant access to the report

To do this, use the Security tool in Dynamics GP.

1. Choose **Microsoft Dynamics GP**, point to **Tools**, point to **Setup**, point to **System**, and then choose **Alternate/Modified Forms and Reports**.

2. In the **ID** box, type the Alternative/Modified Forms and Reports ID that is associated with the user ID that will print this modified report.

3. In the **Product** list, choose **Microsoft Dynamics GP**.

4. In the **Type** list, choose **Reports**.

5. Expand the **Sales** folder.

6. Expand the folder for the report that you modified.

7. Choose **Microsoft Dynamics GP (Modified)**.

8. Choose **Save**.

9. On the Microsoft Dynamics GP menu, point to **Tools**, point to **Setup**, point to **System**, and then choose **User Security**.

10. In the **User** list, choose the user ID that you used to modify the report.

11. In the **Company** list, choose the company that you used to modify the report.

12. In the **Alternate/Modified Forms and Reports ID** list, choose the ID of the user who will print the modified report.

## See also

[Add the Address 3 Field to Sales Documents](sales-add-address-3-field.md)  
[Sales Order Processing Part 5: Inquiries and reports](sales-order-processing-part5-inquiries-reports.md)  
