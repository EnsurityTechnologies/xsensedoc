---
title: "General"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 820
---

This section provides an overview of the available features within this tab.

**Device OTP Expiration Time**: The period of time for which a generated OTP (One-Time Password) is valid and usable for logging into the ThinC Manager application. By default, the OTP expiration time is configured to 20 minutes. However, the organization has full control over this expiration period and can adjust it as needed.

**Device Lockout Count**: This refers to the maximum number of unsuccessful or invalid or failed authentication attempts made through XSense CPP. By default, the device lock out count is set is configured to 3. However, the organization has full control over this lockout count and can adjust it as needed.

**Enable Passwordless**: This feature is essential for activating passwordless functionality during Windows sign-in via XSense CPP. When this option is turned on, users logging into a Windows machine using XSense CPP can skip entering their password and instead sign in using their username and MFA authentication. This approach eliminates the need for conventional text-based passwords as the primary method of accessing Windows machines with XSense CPP installed.

**Enable PC Verification**: XSense IdP offers administrators the choice to link a user or a group of users to a PC, granting access to a workstation or server upon verification of their AD credentials and the completion of multifactor authentication. This option becomes active when the admin enables the this feature.
