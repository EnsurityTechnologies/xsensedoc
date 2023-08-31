---
title: "Privileged Users"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 750
---

By default, all the users imported to the XSense CP server dashboard must sign into Windows PC with the XSense CPP using the ThinC-AUTH biometric security keys. Admins or privileged users added/imported to this privileged group will be able to bypass MFA / Biometrics sign-in to Windows PCs where XSense CPP is installed. 
## Whitelist users
*	The users imported to the Privileged user's group using the Whitelist user option will be exempted from signing to Windows through XSense CPP plug-installed systems. 
*	These users will not have any permissions apart from bypassing the biometric at the time of Windows sign-in through the XSense CPP plug-in.

## Import from LDAP
*	These users are the administrators synchronized from the “Admin User filter” provided AMS LDAP configuration in the “Settings.”  These users have full access to the dashboard.
