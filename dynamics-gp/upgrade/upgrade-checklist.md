---
title: "Upgrade checklist"
description: "Quick run-through of the process for upgrading to Dynamics GP."
keywords: "upgrade"
author: edupont04
ms.author: edupont
manager: edupont
applies_to: 
ms.date: 08/24/2018
ms.service: dynamicsgp
ms.topic: article
ms.assetid: e246f604-015d-44e8-ab38-3cbf2cc850a3
ms.reviewer: 
---
# Upgrade checklist

You can upgrade to [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 from [!INCLUDE[prodshort](../includes/prodshort.md)] 2016 Tax Round 2 or later or GP 2015 R2 (14.0.0725), GP 2013 Tax Round 2 (12.0.1826). For detailed information about which releases and updates you can upgrade from, refer to Releases supported by the upgrade on page 9. If you're using an older release, contact the [!INCLUDE[prodshort](../includes/prodshort.md)] Technical Support team.

<span id="_Toc498615756" class="anchor"></span>

This chapter contains the following sections:

-   [When to upgrade](#when-to-upgrade)  

-   [[!INCLUDE[prodshort](../includes/prodshort.md)] upgrade checklist](#microsoft-dynamics-gp-upgrade-checklist)  

## When to upgrade

Before upgrading, we recommend that you create a timetable of the entire upgrade process. This timetable can include the scheduling of a test upgrade, live upgrade, upgrade training, and implementation. Be sure that the scheduled time to upgrade takes place during a time that works best for all [!INCLUDE[prodshort](../includes/prodshort.md)] users and for your information technology (IT) staff. You may not want to upgrade before processing payroll checks or closing a year.

## [!INCLUDE[prodshort](../includes/prodshort.md)] upgrade checklist

Use this checklist as your guide to upgrading to [!INCLUDE[prodshort](../includes/prodshort.md)] 2018.

| Step                                                                                                                             | For more information                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Verify the security of your system.                                                                                           | Download the Security Planning PDF from <http://www.microsoft.com/en-us/download/details.aspx?id=45025>                                                                                            |
| 2. Refer to these Web sites for new or updated information relating to the upgrade.                                              | <https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentat20ion/system-requirements/dynamicsgpresource#GP2018>                                                                  |
| 3. Ensure that you have the latest version of the Upgrade Guide.                                                                 | <https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentation/system-requirements/dynamicsgpresource#GP2018>                                                                    |
| 4. View the Readme file and make a note of the items that pertain to you.                                                        | Media\\GreatPlains\\Documentation\\GPReadme.chm                                                                                                                                                    |
| 5. Obtain your need registration keys for [!INCLUDE[prodshort](../includes/prodshort.md)] 2018.                                                            | Contact your [!INCLUDE[prodshort](../includes/prodshort.md)] partner before going to CustomerSource/My Account for registration keys for [!INCLUDE[prodshort](../includes/prodshort.md)] 2018. <https://mbs.microsoft.com/customersource>              |
| 6. Verify system requirements and expand your SQL database size, if necessary.                                                   | <http://go.microsoft.com/fwlink/?LinkId=521785>                                                                                                                                                    |
| 7. Identify all integrating products and customizations and ensure that they are compatible with [!INCLUDE[prodshort](../includes/prodshort.md)] 2018.     | Contact the provider of the integrating products and customizations.                                                                                                                               |
| 8. Complete pre-upgrade procedures in the release of [!INCLUDE[prodshort](../includes/prodshort.md)] that you are currently using and review known issues. | <https://mbs.microsoft.com/customersource/northamerica/GP/learning/documentat20ion/system-requirements/dynamicsgpresource#GP2018>                                                                  |
| 9. Install [!INCLUDE[prodshort](../includes/prodshort.md)] 2018 on the server and upgrade your accounting data.                                            | [Installing [!INCLUDE[prodshort](../includes/prodshort.md)] (first computer)](#_Install_Microsoft_Dynamics) on page 31 Be sure to download the latest version of [!INCLUDE[prodshort](../includes/prodshort.md)]. Chapter 6, “Company data conversion” |  
| 10. Complete post-upgrade procedures for [!INCLUDE[prodshort](../includes/prodshort.md)] modules.                                                          | [Chapter 10, “Module upgrades from [!INCLUDE[prodshort](../includes/prodshort.md)] 201](#_Module_upgrades_from)3”                                                                                                            |  
| 11. Upgrade additional components and verify customized reports.                                                                 | [Installing an additional component](#_Installing_an_additional) on page 50                                                                                                                        |  
| 12. Install [!INCLUDE[prodshort](../includes/prodshort.md)] 2015 on the clients.                                                                           | [Installing [!INCLUDE[prodshort](../includes/prodshort.md)] (additional computers)](#_Installing_Microsoft_Dynamics_1) on page 57                                                                                              
                                                                                                                                                                                                      
  [Creating an installation package](#_Creating_an_installation) on page 54                                                                                                                           |  
| 13. Identify the sources of any errors.                                                                                          | Knowledge Base on CustomerSource                                                                                                                                                                   |


