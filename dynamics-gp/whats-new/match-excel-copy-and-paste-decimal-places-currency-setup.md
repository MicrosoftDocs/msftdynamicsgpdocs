---
title: Match Excel Copy and Paste Decimal Places to Currency Setup 
description: New in October 2020 - Match Excel Copy and Paste Decimal Places to Currency Setup
ms.date: 09-30-2020
ms.topic: article
ms.prod: dynamics-gp
author: theley502
ms.author: theley
manager: edupont
---

# Match Excel Copy and Paste Decimal Places to Currency Setup

In earlier versions of Dynamics GP, the Excel copy/paste function ignored the Decimal/Thousands separators in the Currency Setup. This is located by choosing Administration, then Setup, click System and then choose Currency.

When using the Excel Paste feature, Dynamics GP imports the data directly into the SQL tables. This does not interlace with the GP front end in any way. What this means is that this data is not checked against the Currency setup. This, therefore, means your settings for separators is not considered when using this feature.

Other currencies have spaces and periods for the thousand separators, and commas for the decimal separator. Prior to this fix, Excel copy/paste would use the period as the decimal separator, spaces, and periods as the thousand separators, and commas for the decimal separator; ignoring the currency setup and brought the data in incorrectly.

> [!NOTE]
> [This was a large REQUEST by our customers to change how this works ](https://experience.dynamics.com/ideas/idea/?ideaid=3ade4137-e639-e811-bbd3-0003ff68aa57)

With this new feature, Dynamics GP now recognizes the Excel copy/paste Decimal/Thousands separators in the Currency Setup window.

Eliminates rounding issues that are, sometimes, almost impossible to find.

This update will use the decimal places defined in currency setup instead of the data in Excel.

The value will be stored in SQL based on the currency decimal places defined in Currency Setup and not Excel.

<img src="media/image19.jpg" alt="Currency Setup form" width="375" height="336" />


