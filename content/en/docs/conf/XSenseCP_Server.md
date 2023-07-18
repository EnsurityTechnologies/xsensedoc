---
title: "XSense CP Server"
description: ""
lead: ""
date: 2020-11-12T13:26:54+01:00
lastmod: 2020-11-12T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 610
toc: true
---

XSense CP Server is a web service that helps the organization manage user permissions, ThinC-AUTH Biometric Security Keys, assignments, or roles based on the level of permissions and generate/export the necessary reports. The XSense CP server communicates with ThinC Manager for initiating the fingerprint enrollment / ThinC-AUTH security key registration. The XSense server communicates with the XSense CPP agent installed on a Microsoft Windows PC for secure sign-in using ThinC-AUTH biometric security key. The features of the XSense CP server are listed below:

## Features

* Easy Inventory Management of ThinC-AUTH Biometric Security Keys
* Identity integration — User synchronizing with Enterprise's Azure AD / Local-AD / LDAP
* Assign Roles to the Users (Admin / Service Desk / Generic User)
* Easy assign/unassign Keys with Users
*  Send an automatic email to the User about the Device assignment status.
*  Controlled environment for enrolling user fingerprints & Credential onto the Biometric Security Key
*  Restrict the number of fingerprints for enrollment (provision to set a choice of maximum fingerprints between 1 and 5)
*  Mandate the authentication with Biometrics.
*  Reset the ThinC-AUTH remotely for removing the Fingerprint Data of the previous User.
*  Device Log (fingerprint enrolment status on the Security Key)
*  Event & Audit Logs (who logged in to the XSense portal and what they performed)
*  Export the filtered Logs to Excel files.
*  Dashboard with a GUI to display the following in a line chart.
    *  Total Number of Users
    * Total Number of Security Keys
    * The number of Security Keys assigned to Users.
    * Number of Security Keys enrolled with User fingerprints (including the number of fingerprints)
    * The number of Security Keys assigned to Users, but not enrolled.
