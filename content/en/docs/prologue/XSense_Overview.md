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


