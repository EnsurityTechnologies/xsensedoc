---
title: "LDAP Configuration"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 840
---

This section enables administrators to synchronize other administrators based on specified filters from the organizational units (OUs). To sync the **Admin** users and **Users**, navigate to the AMS tab in the Settings section and click on **LDAP Configuration**.

## Admin filter

* Under the Admin user filter, provide the necessary filter to fetch and synchronize the users from the Administrators OU in the Active Directory. By default, these users have admin privileges in the XSense IdP portal.
* The users available under the “Admin” group, will be able to log in into the XSense IdP portal using their AD credentials. XSense IdP portal administrators can log in to XSense CPP installed machines without going through the MFA or ThinC-AUTH biometric security key authentication.

## User filter

* Under the User filter, provide the necessary filter to fetch and synchronize all the users from the specified OU / all the users in the Active Directory. As a default setting, these users will have restricted access permissions within their portal on the XSense IdP portal.
* The choice of MFA option applied to users depends on their user group.

    ![LDAP FILTER](images/LDAPFILTER.png)

* We are saving limited attributes of the admin users which will be used to identify the admin like Common Name, User principal name, and SAMAccount name.

**Enable Periodic Sync**: Using this functionality, administrators can configure systematic and automated synchronization between the Active Directory (AD) and XSense IdP portal. When this functionality is enabled, the portal will routinely synchronies user data and group memberships from AD to the XSense IdP portal (at certain intervals). It's an easy approach to keep the data on the XSense IdP portal and the organization's AD consistent.

**Sync Now**: Administrators can use this functionality to manually start the synchronization between the Active Directory (AD) and the XSense IdP portal. When administrators need to update user and group data in the portal immediately rather than waiting for the next scheduled synchronization, it is especially helpful.
