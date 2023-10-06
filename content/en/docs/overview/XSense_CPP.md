---
title: "XSense CPP"
description: ""
lead: ""
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
menu:
  docs:
    parent: "prologue"
weight: 140
toc: true
---

XSense CPP is the plugin that needs to be installed on all machines where login is required. This plugin will replace windows' default credentials provider and only allow the user to login into the machine using this plugin. At the time of user login, a customized login will be displayed for the user to log in, this will allow the user to login into the machine using a registered ThinC-AUTH biometric security key.

![XSenseCPP](images/XS_CPP2.png)

Enterprise Admin shall configure the required user authentication (with or without the need of password), and the secure sign-in to the Windows device is permitted with the designated authenticator:

Option-1: ‘ThinC-AUTH’ Biometric FIDO2 Security Key to ensure user’s fingerprint-based authentication

Option-2: ‘XSense Verify’ Mobile Authenticator App (Mobile FIDO2 authentication, where user authentication requires Smartphone’s biometric validation)

Option-3: ‘XSense Verify’ Mobile Authenticator App (‘Crypto Code’ based authentication, where user must approve on the Mobile App)

Option-4: TOTP Mobile Authenticator App (such as XSense Verify, Microsoft / Google Authenticator Apps)
