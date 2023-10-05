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

During the installation of XSense CPP on a Microsoft Windows based workstation or server(machine), the application establishes a connection with the XSense IdP portal using the API configuration file. Subsequently, it generates and transmits a unique ID associated with the machine to the XSense IdP portal. XSense IdP compiles a comprehensive list of all computers installed with XSense CPP for multifactor authentication under the **Computers** tab.

When an user attempts to signin to the XSense CPP installed machine, the XSense IdP portal identifies the users membership in one of groups and based on the group member, the system then prompts the user to provide the appropriate authentication method tailored for the user/group.

Several actions can be executed on a specific computer. These actions are listed below:

* Whitelist PC
* Assign Users
* Assign Group
* Delete

![computer actions](images/computeractions.png)

## Whitelist PC

A trusted computer is specifically allowed to create remote desktop connections to a particular target machine when it is whitelisted for RDP access. By restricting RDP access to approved devices, this access control solution minimises the risk of unauthorised access and possible security breaches.

**Scenario:** An administrator is attempting to establish a Remote Desktop Protocol (RDP) connection to a server machine for administrative tasks. When signing in to XSense CPP installed machine, the administrator is required to provide biometric authentication. This biometric authentication process occurs on the administrator's own computer, where the ThinC-AUTH device is connected. The ThinC Agent tool facilitates the transmission of the biometric authentication request to the XSense CPP on the remote server. Once the response is received by XSense CPP, the administrator is granted access to sign in to the server.

Prior to initiating the RDP session, the IP address of the administrator's machine should be added to the whitelist group in the XSense IdP server for the specific remote machine.

* To enable the user's machine to initiate an RDP connection to the remote machine, the administrator must include the IP address of the machine from which the RDP session will be initiated. click on **Whitelist PC >> New Whitelist PC**.  In the **New Whitelist PC** dialog, input the name of the remote machine and the user's IP address from where the remote connection is being initiated.
* Check the check box **Is Enabled** and click on **Save**.

    ![computer actions](images/whitelistPC.png)

* The user initiates the RDP connection to the remote machine and performs authentication of the ThinC-AUTH device as prompted by XSense CPP on the remote machine.

{{< alert icon="👉" context="note" text="The ThinC Agent application needs to be actively running, and the ThinC-AUTH biometric security key must be connected to the user's computer." />}}

## Assign Users or Group

XSense IdP offers administrators the choice to link a user or a group of users to a PC, granting access to a workstation or server upon verification of their AD credentials and the completion of multifactor authentication. This feature closely resembles the "User logon to" feature in Active Directory (AD), where a computer is associated with a user within the user's properties.

* It is recommended that the administrator creates an OU under Identity Management with the necessary users before assigning a group to the computer. After creating the requisite groups within this OU, the administrator can then select the desired group of users.

* To allocate a user or group to the computer, select **Assign User / Assign Group** and then pick the relevant user or group from the pop up window.

* To view the list of users / groups assigned to the computer, click on **+** under **Assigned Users** of the selected computer.

* To unassign the user / group, click on **+** under **Assigned Users** of the selected computer. It will list the users / groups assigned to the computer. Select the required user / group that has to be unassigned and click on **Unassign**.

    ![unassing group](images/unassigncomputer.png)

{{< alert icon="👉" context="note" text="As a default configuration, if no users or groups have been assigned to the machine, all users are automatically permitted access to the XSense CPP installed machine using the designated multifactor authentication method."/>}}

## Delete

The selected computer is removed from the list of computers, and any assigned users or groups are immediately unassigned. Users won't be able to access the machine using XSense CPP, even if it is installed on the machine.
