---
title : "SQL Installation "
lead: ""
date: 2020-10-06T08:48:45+00:00
lastmod: 2020-10-06T08:48:45+00:00
draft: false
images: []
weight: 660
---

This section describes the process of installing Microsoft SQL Server on a server running Microsoft Windows Server 2019 or Microsoft Windows Server 2022.  

* Launch the SQL Server installation media and select installation from the left-side column, and once selected, you will find multiple options on the right-side column.
* To add features to an existing installation or to install New SQL Server standalone, select the first option in the right-side column. Click on Next when prompted. 
* Select Click Next after initiating a fresh installation of SQL Server XXXX.
* Select the type of edition and then click on Next.
* Accept the license terms. The installer navigates to SQL Server XXXX's features.
* Select Database Engine Services from the list of available services. Click on Next.
* Choosen the default instance and click on Next.
* Two authentication modes—Windows authentication Mode and Mix Mode—are now visible on the screen. Select Mix Mode, enter the desired password, and then confirm the password for 'sa'. If the server machine is domain joined, then add the service/admin account to access database. 

    ![IIS_Homepage.png](images/SQL_Mixed_Authentication.png)

* Now, click on Next, and the installation process takes place.
* Once the installation process is complete, you’re redirected back to the SQL Server Installation Center.

* Download and install the latest version of SQL Server Management Studio.
  