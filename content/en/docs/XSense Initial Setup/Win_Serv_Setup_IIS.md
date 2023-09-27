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

## Configuration

This section describes the process of configuing IIS after the completion installing XSense IdP.

### Permissions

* On the IIS, open Windows Explorer, and select the directory of the XSense web application.

  ![IIS_Homepage.png](images/IIS_Homepage.png)

* On the right pane, under Actions click on Edit Permissions. Navigate to the Security tab.
* Click on Edit and under the Group or user names clcik on Add. Type the IIS users group name IIS_IUSRS into the edit field then click Check Names and click OK.

  ![IIS_Homepage.png](images/IIS_IUSR_Permissions.png)

* Select the IIS_IUSRS user and select Full control permission. The Security tab is updated to include the new IIS_IUSRS group and it’s permissions. Click OK to accept the new values.

  ![IIS_Homepage.png](images/IIS_IUSR_Permissions_fullaccess.png)

### Application Pools

* Expand the IIS server and choose Application Pools.
* On the right pane, click Add Application Pool or right-click the middle pane and choose Add Application Pool.

  ![IIS_Homepage.png](images/IIS_ApplicationPools_Home.png)

* Once the Add Application Pool window appears, type the name of the application pool on the Namefield as XSenseApp.

* The .NET Clr version field is set to "No Managed Code".

  ![IIS_Homepage.png](images/IIS_Application_NewAppPoolCreation.png)

* The Start application pool immediately is checked.
* After the application pool is created, click the application pool and on the right pane, click Advanced settings.
* Go to the Process Module section and on the Load User Profile change the value from False to True then click OK.

   ![IIS_Homepage.png](images/IIS_App_Pool_Adv.png)

* Expand Sites and locate the virtual directory where you want to use the application pool.
* Select the virtual directory and on the right panel click Advanced Setting.
* Go to the General section and on the Application Pool, click Browse and select the application pool created.

  ![IIS_Homepage.png](images/IIS_ApplicationPools_NewPool.png)
