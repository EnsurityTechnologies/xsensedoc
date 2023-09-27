---
title : "XSense Website Install "
description: "Title"
lead: ""
date: 2020-10-06T08:48:45+00:00
lastmod: 2020-10-06T08:48:45+00:00
draft: false
images: []
weight: 690
---

This section describes the process of installing XSense IdP. Before proceeding with the installation, the pre-requisites such as IIS and SQL server must be made available.

> During the installation of XSense IdP, if IIS is not preinstalled, XSense IdP will install IIS and XSense IdP during the installation process.

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