---
title: "LDAP Configuartion"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 700
---

After login to the dashboard using the default admin credentials, the IT admin must configure the LDAP to synchronize the users and assign the ThinC-AUTH Biometric Security Keys to the users. To synchronize the users, please follow the steps below.

* Login to the XSense CP Server dashboard using the administrator credentials and navigate to the Settings tab under the Administration section.
* The Settings tab contains sub-tabs Emailing, Account, Account External Provider, AMS, Identity Management, LDAP, and backup codes.
* Click on LDAP Configuration and Enter the
  * LDAP Provider URL in the format host: port (Example 192.168.4.83:389)
  * Specify the credentials of any one of the admin users. Enter the Username and Password.
  * This is the 'base' from where directory lookups should take place. Enter the LDAP base (top level of the LDAP directory tree). Enter it exactly in the format used in your LDAP.

<br>

![LDAP](../../../../images/LDAP.png)

<br>

* Soon after clicking on the Save button, XSense CP Server will start validating the LDAP configuration details. Once validated, the LDAP configuration will be saved.
