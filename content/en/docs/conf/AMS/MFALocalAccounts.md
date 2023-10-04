---
title: "MFA Local Accounts"
description: ""
draft: false
images: []
weight: 760
---

In response to ongoing improvements aligned with enterprise needs, the XSense IdP solution evolves swiftly. This functionality empowers local users created during the initial setup of workstations and servers to utilize multifactor authentication via XSense CPP.

As part of the workstation or server's initial setup, a local user is created.These users cannot be synchronized with the Active Directory (AD) because they are specific to the individual workstations or servers. They are essentially local admin users tied to a particular workstation or server. Consequently, if the credentials for these users were to be exposed or shared among individuals, it could potentially lead to unauthorized application installations without the necessary approvals from AD administrators. This situation could introduce security vulnerabilities. To address this concern, we have implemented the MFA Local Accounts feature.
