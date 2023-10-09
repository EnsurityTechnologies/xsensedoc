---
title : "XSense IdP Portal "
description: "Title"
lead: ""
date: 2020-10-06T08:48:45+00:00
lastmod: 2020-10-06T08:48:45+00:00
draft: false
images: []
weight: 690
---

This section describes the process of installing XSense IdP. Before proceeding with the installation, the pre-requisites such as IIS and SQL server must be made available.

## Installing XSense IdP Portal

{{< alert icon="👉" context="note" text="During the installation of XSense IdP, if IIS is not preinstalled, XSense IdP will install IIS and XSense IdP during the installation process." />}}

* Ensurity provides the XSense IdP installer with the extension of '.MSI'. The admin must run the application in admin mode for it successfully install the necessary dependencies. Run the provided 'XSense_WebServer.msi' with administrator privilages.

* Click on Install to begin the installation process.

    ![XSense setup](images/xsense_setup1.png)

* To initialize XSense IdP after the completion of the installation, the application needs to run on a default port over Http. This can later be updated to Https after the completion of installation. Click on Next to proceed further.

    ![xsense_setup_tempurl.png](images/xsense_setup_tempurl.png)

* Enter the Database details such as Database server IP or Hostname and Database username and password.

{{< alert icon="👉" context="note" text="It is recommoneded to use a service account with Database read/write/update permissions." />}}

* Click on Verify to check the connectivity.

    ![XSense setup DB](images/xsense_setup_db.png)

* After sucessful verification of the database connectivity click on Next.

    ![XSense setup DB](images/xsense_setup_db3.png)

* The XSense IdP generates a unique ID. The admin needs to share the unique ID with Ensurity team for the necessary license.

    ![XSense setup DB](images/xsense_setup_license.png)

* Enter the provided license and click on Install.

    ![XSense setup DB](images/xsense_setup_installstart.png)

* After successful installation, the installer will automatically close.

## URL configuration in App Settings

After completing the installation, the URL has to be configured in the App settings to access the XSense IdP portal.

* To update the URL, naviate to "C:\Program Files (x86)\EnsurityXSense_Server".
* Locate the file with the name "appsettings.json" and open the file with a text editor.
* In the Appsettings.json, update the custom URL in the below sections
    * SelfUrl
    * Authority
    * serverDmain
    * Origin
    <br><br>
 
    ![XSense setup DB](images/API_IIS_URL_Update.png)

* After updating the desired URL in the above mentioned settings, save and close the "appsettings.json" file.

## XSense IdP configuration in IIS

The URL must be changed in IIS settings once it has been saved in the appsettings.json file.

### URL configuration

* Open IIS Manager and select the XSense. On the right pane, under Actions click and select "Edit Bindings".
* Click "Add" to create a new binding.
* Select the type of binding you want to create (e.g., HTTPS) and enter the new domain name that is configured in the "appsettings.json".
* Select the new SSL certificate from the list of available certificates. If an SSL certiticate is not available, then a self signed certificate can be used for SSL.
* Click "OK" to save the new binding.

    ![XSense setup DB](images/IIS_URL.png)

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
