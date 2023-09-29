---
title: "XSense IdP Introduction"
description: ""
lead: ""
draft: false
menu:
  docs:
    parent: "Overview"
weight: 100
toc: true
---

Enterprises having large user base needs high security along with easily deployable and scalable identity & access solutions. Risks emanating from credential thefts and ransomware attacks in the recent days require strong authentication and identity management. Compliance and regulatory authorities are insisting for a strong 2FA/MFA deployment.

Usernames and passwords are how all of us identify ourselves to almost every system and website in the internet world. Traditional authentication methods just aren’t that safe or intuitive. In particular, passwords can be shared with unauthorized users or stolen from a database, or by phishing, man-in-the-middle attack, a key-logger, or even with a brute force technique. It is well known that passwords are often repeated across domains or stored on unsecured media.

Ensurity proposes its novel cybersecurity solution to address the critical requirements. The solution can be deployed as On-Premises or SAAS or Hybrid model.

Ensurity proposes secure passwordless authentication ‘**XSense IdP**’ solution to the Local-AD joined Windows systems along with “**CPP (Credential Provider Plugin)**” module, which supports **Ensurity’s biometric FIDO2 security key**.

XSense IdP server is a web service that helps the organization manage user permissions, ThinC-AUTH Biometric Security Keys, assignments, or roles based on the level of permissions and generate/export the necessary reports. The XSense CP server communicates with ThinC Manager for initiating the fingerprint enrollment / ThinC-AUTH security key registration. The XSense IdP server communicates with the XSense CPP agent installed on a Microsoft Windows PC for secure sign-in using ThinC-AUTH biometric security key. The features of the XSense CP server are listed below:

## Features

* Easy Inventory Management of ThinC-AUTH Biometric Security Keys
* Identity integration — User synchronizing with Enterprise's Azure AD / Local-AD / LDAP
* Assign Roles to the Users (Admin / Service Desk / Generic User)
* Easy assign/unassign Keys with Users
* Send an automatic email to the User about the Device assignment status.
* Controlled environment for enrolling user fingerprints & Credential onto the Biometric Security Key
* Restrict the number of fingerprints for enrollment (provision to set a choice of maximum fingerprints between 1 and 5)
* Mandate the authentication with Biometrics.
* Reset the ThinC-AUTH remotely for removing the Fingerprint Data of the previous User.
* Device Log (fingerprint enrolment status on the Security Key)
* Event & Audit Logs (who logged in to the XSense portal and what they performed)
* Export the filtered Logs to Excel files.
* Dashboard with a GUI to display the following in a line chart.
  * Total Number of Users
  * Total Number of Security Keys
  * The number of Security Keys assigned to Users.
  * Number of Security Keys enrolled with User fingerprints (including the number of fingerprints)
  * The number of Security Keys assigned to Users, but not enrolled.

The proposed solution will be beneficial for the Enterprise Users in securely accessing their on-prem Windows OS systems that are either individual devices or connected to the Local Active Directory. The proposed solution will eliminate the password-only based sign-in to access Windows devices. The solution consists of the following modules:

| Sn | <span style="display: inline-block; width:225px">Ensurity - Solution Module</span> | Solution Description |
| ----: | ---- | ---- |
| 1 | **XSense IdP (Identity Provider) Server Portal** | A server portal deployable on Microsoft IIS platform to manage Users from the Local Active Directory, Biometric FIDO2 Security Keys, Linking User Credentials with the Security Key, and to whitelist the end-user Windows devices for secure sign-in with the biometric FIDO2 security key ‘ThinC-AUTH.’ |
| 2 | **XSense CPP (Credential Provider Plugin) Service** | A standalone application for Windows OS (functional from Windows OS version 7 and above releases, with latest service packs). The Windows workstations must be joined to the Local Active Directory. |
| 3 | **Biometric FIDO2 Security Key ‘ThinC-AUTH’** | A FIDO2-certified Biometric Security Key as secure hardware (USB Type-A) authenticator solution. |
| 4 | **ThinC Manager** | A standalone application for Windows OS, helps the IT Admin Users to enroll their Fingerprints onto the assigned Biometric FIDO2 Security Key. |

## XSense Server — Deployment Models

The XSense Server supports flexible deployment models.

### On-Premises Deployment

Helpful to Enterprises, those do not allow external network connectivity.

* Addresses specific customizations in the overall functionality.
* Organization needs to provide a scalable infrastructure (Server & Network Hardware).
* Security is utmost important, and data security and data protection depends on the security systems that the * organizations deploy.
* Only accessible to on-premises users or through virtualization networks.
* Support for unique authentication, via:
  * Biometric FIDO2 Security Key (passwordless authentication), which protects credential sharing.
  * TOTP based Mobile Authenticator Apps.

#### Architecture for an On-Prem Deployment

The diagram highlights the over architecture of the solution. The XSenseCP Server hosted in the Enterprise on-premises Data Center is configurable to connect with an existing LDAP user directory to synchronize the existing users and groups in an enterprise directory. The LDAP directory is used for both user authentication and account management.

![Arch](images/arch.png)

### SaaS Deployment

Helpful to Enterprises, those do allow external network connectivity.

* Lower CAPEX.
* Provides continual support as defined by the SLA.
* Security is provided by vendor and regulated by SLAs.
* Data backup systems are a core part of SaaS offerings.
* Flexible and very scalable. It offers instant scaling.
* Accessibility by anyone with an internet connection and authorization from the SaaS platform.
* Support for wide-range of Secure Authenticators, including the following:
  * Biometric FIDO2 Security Key (passwordless authentication), which protects credential sharing.
  * XSense Verify Mobile Authenticator App (works on iOS & Android platforms).
  * TOTP based Mobile Authenticator Apps.

#### Architecture for an SAAS Deployment

The diagram highlights the over architecture of the solution. The XSenseCP Server hosted in Ensurity cloud data center is configurable to connect with an existing LDAP/Azure user directory to synchronize the existing users and groups in an enterprise directory. The LDAP/Azure directory is used for both user authentication and account management.

![Arch](images/XS_Deployment_SaaS.png)