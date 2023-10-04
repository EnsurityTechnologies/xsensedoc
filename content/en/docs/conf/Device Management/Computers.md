---
title: "Computers"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 790
---

During the installation of XSense CPP on a workstation or server, the application establishes a connection with the XSense IdP portal by utilizing the API configuration file. Subsequently, it generates and transmits a unique ID associated with the workstation or server to the XSense IdP portal. XSense IdP compiles a comprehensive list of all computers installed with XSense CPP for multifactor authentication under the **Computers** tab.

When an user attempts to sign in to the workstation or server with XSense CPP installed, the XSense IdP portal identifies the users membership in one of groups: the admin group, privileged users group, or regular users group, MFA local users group. Based on the group member, the system then prompts the user to provide the appropriate authentication method tailored for the group.

Several actions can be executed on a specific computer, including

* Whitelist PC
* Assign Users
* Assign Group
* Delete

![computer actions](images/computeractions.png)

## Whitelist PC

A trusted computer is specifically allowed to create remote desktop connections to a particular target machine when it is whitelisted for RDP access. By restricting RDP access to approved devices, this access control solution minimises the risk of unauthorised access and possible security breaches.

## Assign Users

XSense IdP offers administrators the choice to link a user to a PC, granting access to a workstation or server upon verification of their AD credentials and the completion of multifactor authentication.

## Assign Group

XSense IdP offers administrators the capability to allocate a set of users access to a workstation or server while enforcing multifactor authentication.

{{< alert icon="👉" context="note" text="If no users or groups have been assigned to the machine, all users are automatically permitted access to the workstation or server using the designated multifactor authentication method." />}}

* **Delete**: This action signifies that the computer is no longer part of the group of devices that users or groups can access. Users won't be able to access the workstation or server using XSense CPP, even if it is installed on the machine.
