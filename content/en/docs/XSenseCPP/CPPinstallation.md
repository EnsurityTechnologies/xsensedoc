---
title : "XSense CPP Installation"
description: "."
lead: ""
date: 2020-10-06T08:48:23+00:00
lastmod: 2020-10-06T08:48:23+00:00
draft: false
images: []
weight: 920
---

Several options available at the time of installing the XSense CPP application are described in this section.

The XSense CP Plugin Tool is a standalone application designed for Microsoft Windows-based machines. It serves as a replacement for the default credentials provider, permitting only users synchronized with the XSense IdP portal to access the machine via this plugin. During the user login process, a customized login interface will be presented, enabling the user to log in to the machine using their registered ThinC-AUTH biometric security key or any other enabled multifactor authentication method.

XSense CPP operates in two distinct modes: corporate mode and standalone mode.

## Corporate Mode

In this mode, the XSense CPP connects to the XSense IdP portal deployed at the organization's infrastructure, providing centralized authentication and access control.

* Based on the specific needs of the organization, the admin is responsible for selecting the preferred authentication methods available to users. Additionally, the admin must decide whether local user accounts can be accessed without the need for multifactor authentication, taking into account the organization's requirements.

* If the organization decides to implement passwordless login, they should enable the **Passwordless** option within the XSense IdP portal.

  ![Corporate Mode](images/XSenseCPPInstallationmodes.png)

## Standalone Mode

In contrast, in standalone mode, XSense CPP operates autonomously. Users connect directly to the XSense IdP server hosted at Ensurity's data center.

* If the user selects the "Passwordless" option, they can sign in to the XSense CPP-installed machine without needing a password for their local account. In this mode, the user registers their account with the XSense IdP server using their email address. During XSense CPP installation, they must provide the same email address used for registration. Once registered, the user can utilize their local user account to sign in to the machine using XSense CPP, all without requiring a password.

![Standalone Mode](images/XSenseCPPInstallStand.png)

XSense CPP is a flexible application that permits users to select the preferred authentication method for the machine.

## Multifactor Authentication

When this checkbox is selected, users will be presented with a list of available multifactor authentication methods for the machine at the time of Windows Sign-in. Some examples of these authentication methods include:
  
  * ThinC-AUTH
  * TOTP
  * XSense Crypto
  * XSense FIDO mobile

## Allow Local User

By enabling this option, users can log in to the machine using a local user account, bypassing the available multifactor authentication for that machine.
