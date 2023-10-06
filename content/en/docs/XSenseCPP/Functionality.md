---
title : "XSense CPP Functionality"
description: ""
lead: ""
date: 2020-10-06T08:48:23+00:00
lastmod: 2020-10-06T08:48:23+00:00
draft: false
images: []
weight: 930
---

## Windows Sign-in

XSense CPP serves as a replacement for the default credentials provider. At the time of Windows sign-in, based on the options chosen by the admin / user during the installation the below options are made available for multifactor authentication.

**ThinC-AUTH** Biometric FIDO2 Security Key to ensure user’s fingerprint-based authentication

**XSense Verify - FIDO** Mobile FIDO2 authentication, where user authentication requires Smartphone’s biometric validation.

**XSense Verify - Crypto Code** ‘Crypto Code’ based authentication, where user must approve on the Mobile App.

**TOTP** Mobile Authenticator App (such as XSense Verify, Microsoft / Google Authenticator Apps)

![Sign in Authentication](images/CPauthenticationmodes.png)

## UAC

XSense UAC section, offers an extra choice when performing administrative tasks such as installing applications or starting any application with administrative rights. When performing administrative tasks, the UAC displays the XSense along with the predetermined alternatives.

* The administrator enters credentials in the XSense UAC section, the user is prompted for multifactor authentication.

   ![App uninstall](images/UAC_XSenseCPP.png)

## RDP

When the user is trying to an RDP of a whitelisted machine, the administrator has to run ThinC Agent application. This application will transmit the user authentication virtually at the time of sign-in.

![ThinC Agent](images/ThinCAgent.png)
