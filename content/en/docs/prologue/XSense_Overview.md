---
title: "XSense Overview"
description: ""
lead: ""
date: 2020-11-16T13:59:39+01:00
lastmod: 2020-11-16T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 110
toc: true
---


Ensurity proposes its novel cybersecurity solution to address the critical requirements of Almarai. The solution shall be deployed as On-Premises model. 

Ensurity proposes secure passwordless authentication ‘**XSense IdP**’ solution to the Local-AD joined Windows systems along with “**CPP (Credential Provider Plugin)**” module, which supports **Ensurity’s biometric FIDO2 security key**.

The proposed solution will eliminate the password-only based sign-in to access Windows devices. The solution consists of the following modules:

| Sn | <span style="display: inline-block; width:225px">Ensurity - Solution Module</span> | Solution Description |
| ----: | ---- | ---- |
| 1 | **XSense IdP (Identity Provider) Server Portal** | A server portal deployable on Microsoft IIS platform to manage Users from the Local Active Directory, Biometric FIDO2 Security Keys, Linking User Credentials with the Security Key, and to whitelist the end-user Windows devices for secure sign-in with the biometric FIDO2 security key ‘ThinC-AUTH.’ |
| 2 | **XSense CPP (Credential Provider Plugin) Service** | A standalone application for Windows OS (functional from Windows OS version 7 and above releases, with latest service packs). The Windows workstations must be joined to the Local Active Directory. |
| 3 | **Biometric FIDO2 Security Key ‘ThinC-AUTH’** | A FIDO2-certified Biometric Security Key as secure hardware (USB Type-A) authenticator solution. |
| 4 | **AMS Agent Tool** | A standalone application for Windows OS, helps the IT Admin Users to enroll their Fingerprints onto the assigned Biometric FIDO2 Security Key. |

The proposed solution will be beneficial for the Enterprise Users in securely accessing their on-prem Windows OS systems that are either individual devices or connected to the Local Active Directory.


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