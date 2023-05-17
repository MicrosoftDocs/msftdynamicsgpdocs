---
title: Support for TLS 1.2 
description: New in October 2020 - Support for TLS 1.2
ms.date: 10/01/2020
ms.topic: article
ms.prod: dynamics-gp
author: theley502
ms.author: theley
manager: jswymer
---

# Support for TLS 1.2

With the October 2020 release, Dynamics GP addresses functionality that will be affected by the upcoming retirement of the TLS 1.0 and 1.1 protocols. To refresh your memory on this, we published the following blog on some limitations with various Dynamics GP functionality:

[https://community.dynamics.com/gp/b/dynamicsgp/posts/dynamics-gp-and-tls-1-0](https://community.dynamics.com/gp/b/dynamicsgp/posts/dynamics-gp-and-tls-1-0)

With the October 2020 release, the following features will now be able to function with TLS 1.0 and 1.1 disabled:

* E-mailing from within Dynamics GP when using both the Exchange Server Type as well as the SMTP email that is used for the Workflow feature in Dynamics GP

* The Microsoft Dynamics GP Web Client

* Web Services for Microsoft Dynamics GP

> [!NOTE]
> Web Services for Microsoft Dynamics GP still requires TLS 1.0 when using a SQL Server database for the Authorization Store. If you reinstall Web Services for Microsoft Dynamics GP to an Active Directory partition per [*this blog article*](https://community.dynamics.com/gp/b/dynamicsgp/posts/microsoft-dynamics-gp-web-services---how-to-setup-an-active-directory-security-store) you can operate with TLS 1.0 and 1.1 disabled.

In terms of functionality that still requires TLS 1.0, the refreshable Excel reports that can be deployed from Dynamics GP are still using the SQLOLEDB provider, which requires TLS 1.0. You can manually update the connection string in your Excel files to use the SQLNCLI11 provider as a workaround.
