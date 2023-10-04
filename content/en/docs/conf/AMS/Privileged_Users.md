---
title: "Privileged Users"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 750
---

As the default configuration, every user imported into the XSense IdP portal through the AD are required to utilize any one of the authentication method such as ThinC-AUTH biometric security keys for signing into Windows PCs through XSense CPP. However, administrators and temporary users who are added or imported into this special group will have the privilege to bypass multi-factor authentication (MFA) or biometric sign-in when signing in to Windows PCs using their AD credentials where XSense CPP is installed.

XSense offers two categories of user groups for authentication bypass: Whitelisted users and Admin users.

## Whitelist users

These users do not belong to any Active Directory administrator group; nonetheless, the organization's policy is to exempt them from multi-factor authentication (MFA). An example of such users could be auditors who utilize XSense CPP-installed PCs solely for auditing purposes.

These users will possess solely the privilege of bypassing MFA authentication during Windows sign-in via the XSense CPP plug-in. Any permissions allocated to these users in the Active Directory (AD) will remain in effect.

To include these users in the Whitelist group, administrators must adhere to the following procedure.

* Select **Whitelist User** and in the "Add privileged user" pop-up, pick the user from the roster of users imported into the XSense IdP portal.
* After selecting the desired user, click **Save**. The imported user will be designated as a Whitelist User.

    ![whitelist user](images/whitelistuser.png)

## Import from LDAP

These users are the administrators who are synchronized from the **Admin User filter** specified in the **AMS LDAP configuration** under the **Settings** section. As a result of this synchronization, these administrators are granted complete and unrestricted access to the dashboard, meaning they have full privileges and control over the dashboard's functionalities and settings.

* To import administrators from the connected Active Directory, click on **Import from LDAP**, and choose the administrators from the popup window.
* After selecting the necessary users, click on **Sync**. The users imported from the Active Directory will be assigned the role of an Admin.

    ![AD Admin import](images/AdminImportAMS.png)

## Export to Excel

The XSense IdP portal extends the capability to export privileged and whitelisted user data to an Excel file. This export feature supports audit processes, user verification, and customizable reporting, contributing to effective user management and system oversight.

To export user data, select **Export to Excel**, and a comprehensive list of both whitelisted users and admin users will be exported in Excel format.
