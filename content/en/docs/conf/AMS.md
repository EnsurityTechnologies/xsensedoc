---
title: "AMS"
description: ""
lead: ""
date: 2020-11-12T15:22:20+01:00
lastmod: 2020-11-12T15:22:20+01:00
draft: false
images: []
menu: 
  docs:
    parent: "help"
weight: 650
toc: true
---

The AMS section under settings helps the admin to synchronize the admins from the OU (organizational units) based on the filters provided. 
*	To configure the “Admin” users and Users, navigate to the AMS tab in the Settings section and click on “LDAP configuration.” 
*	Under the Admin user filter, provide the necessary filter to fetch and synchronize the users from the Administrators OU in the Active Directory. By default, these users have admin privileges in the XSense CP Server. 
*	The users available under the “Admin” group, will be able to login into the XSense portal using their AD credentials. The XSense CP server Admins can sign into Windows OS through XSense CPP bypassing the MFA / ThinC-AUTH biometric security key.
*	Under the User filter, provide the necessary filter to fetch and synchronize all the users from the specified OU / All the users in the Active Directory. By default, these users will not have any permission to access the XSense CP portal. 

![LDAP](/images/LDAPFILTER.png)


* We are saving limited attributes of the admin users which will be used to identify the admin like Common Name, User principal name, and SAMAccountname.
