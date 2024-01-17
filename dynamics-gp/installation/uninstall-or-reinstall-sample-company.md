---
title: Uninstall or Reinstall the Sample Company
description: Learn how to uninstall and reinstall the sample company in Dynamics GP when you are using SQL Server or MSDE.
ms.date: 10/23/2020
ms.topic: article
author: jswymer
ms.author: jswymer
---

# Uninstall or Reinstall the Sample Company

This article describes how to uninstall and reinstall the sample company in Dynamics GP when you are using SQL Server or MSDE.

> [!IMPORTANT]
> Before you follow the instructions in this article, make sure that you have a complete backup copy of the database that you can restore if a problem occurs.

## Uninstall the Sample Company

1. Start Dynamics GP, and then log into a different company other than the sample company.

2. Choose **Microsoft Dynamics GP**, point to **Tools**, point to **Utilities**, point to **System**, and then choose **Company**.

3. Choose the lookup button, double-click **Fabrikam, Inc.**, and then choose **Delete**.

4. Delete the sample company database. To do this, use one of the following methods:

    - In Enterprise Manager or in SQL Server Management Studio, expand **Databases**, right-click **TWO**, and then choose **Delete**.

    - Run the following script in Query Analyzer, in SQL Server Management Studio, or in the Support Administrator Console.

        ```sql
        DROP DATABASE *TWO*
        ```

## Install the Sample Company

1. Start Microsoft Dynamics GP Utilities.

2. In the **Additional Tasks** window, choose **Add sample company data**, and then choose **Next**.
    > [!NOTE]
    > If the option to Add sample company data is not available, see the **References** section.

3. Choose **Next** after you verify the location for the database files.

4. Choose **Next** to create the database.

## References

For the steps to install the Support Administrator Console, choose the following article number to view the article How to install the Support Administrator Console utility in Microsoft Dynamics GP in the Microsoft Knowledge Base:
[870052.](http://vkbexternal/VKBWebService/ViewContent.aspx?scid=kb%3bEN-US%3b870052&PortalId=1)

If the option to **Add sample company data** is not available, refer to the following list:

- The account framework may be too small to allow for the addition of a sample company. The minimum account framework required is 3-4-2 for the sample company. To verify the account framework, run the following script against the DYNAMICS database in Query Analyzer, in SQL Server Management Studio, or in the Support Administrator Console.

    ```sql
    SELECT SGMTNAME, SGMNTLTH FROM DYNAMICS..SY00302

- The SQL folder may not exist in the Microsoft Dynamics GP installation folder on this computer.

  - If you are using Microsoft Dynamics GP or an earlier version, reinstall Microsoft Dynamics GP by using the Server option.
  - If you are using Microsoft Business Solutions - Great Plains 8.0, look for the Add sample company data option in Utilities on the server installation, or copy the SQL folder from the installation CD. To do this, follow these steps:

    1. In the Great Plains installation folder, create a new folder that is named *SQL*. By default, the Great Plains installation folder is located at C:\\Program Files\\Microsoft Business Solutions\\Great Plains.

    2. Choose the *SQL* folder, and then choose the *7.0* folder on CD1 for Great Plains.

    3. Copy the following folders to the new SQL folder that you created in step 1:

        - Company
        - HR
        - Lesson
        - System
        - Upgrade
        - Util
        - Right-choose the SQL folder, select Properties, and then make sure that Read Only is not selected.

## See also

[Install Dynamics GP on the first computer](installing-on-first-computer.md)  
[Using Microsoft Dynamics Utilities](using-microsoft-dynamics-utilities.md)  
[Recommended Maintenance of Your Databases](database-maintenance-recommendations.md)  
