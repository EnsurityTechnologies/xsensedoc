---
title: "IIS Setup & Configuration"
description: ""
lead: ""
draft: false
menu:
  docs:
    parent: "XSense Initial Setup"
weight: 630
toc: true
---

The installation of IIS and the necessary configuration required for XSense IdP to function with out any issues on a server running Microsoft Windows Server 2019 or Server 2022 is addressed in this article.

## IIS Installation

The Microsoft Windows Server 2019 or Server 2022 operating systems come with a minimal installation that does not include Internet Information Services (IIS).

* Click on the Windows button and select Server Manager.
* In the Server Manager Dashboard, click Manage > Add Roles and Features.
* Click Installation Type.
* Select the Role-based or feature-based installation option and click Next.
* Select the server on which IIS has to be installed and click Next.
* Choose the Web Server (IIS) role. To add the IIS Management Console, click Add Features.

  ![IIS_Setup_webserver](images/IIS_Setup_webserver.png)

* Click Next. The SelectFeatures window will open.

  ![IIS_Setup_ServerRoles](images/IIS_Setup_ServerRoles.png)

* Click Next. The Web Server Role (IIS) window will open.

  ![IIS_setup_webcoe](images/IIS_setup_webcoe.png)

* Verify the selected roles, role services, and features, click Install to proceed further.
* Once the installation is completed, click on 'Close'.

