---
title: "MFA Local Accounts"
description: ""
draft: false
images: []
weight: 760
---

In response to ongoing improvements aligned with enterprise needs, the XSense IdP solution evolves swiftly. This functionality empowers local users created during the initial setup of workstations and servers to utilize multifactor authentication via XSense CPP.

As part of the workstation or server's initial setup, a local user is created.These users cannot be synchronized with the Active Directory (AD) because they are specific to the individual workstations or servers. They are essentially local admin users tied to a particular workstation or server. Consequently, if the credentials for these users were to be exposed or shared among individuals, it could potentially lead to unauthorized application installations without the necessary approvals from AD administrators. This situation could introduce security vulnerabilities. To address this concern, we have implemented the MFA Local Accounts feature.

After adding users to this group, when they attempt to log in to the workstation or server using their local user credentials, they will be prompted with multifactor authentication such as ThinC-AUTH biometric security keys. The user will be required to verify the device using their fingerprints as part of this authentication process.

In the current scenario, the users with ThinC-AUTH biometric security key will only be able to login using the local user credentials. These will also be able to login to the workstations or servers using their AD credentials and ThinC-AUTH biometric security keys.

Users assigned with ThinC-AUTH biometric security keys can log in using their local user credentials as the primary method to the workstations or servers. Additionally, they have the flexibility to access workstations or servers using their their Active Directory (AD) credentials along with their ThinC-AUTH biometric security keys.

* To incorporate a user into this specific group, follow these steps:
  * Click on **Add Local User**.
  * From the provided list, select the user you wish to include.
  * Confirm your selection by clicking **Save**.

 ![mfa local account](images/mfalocalaccount.png)

This action effectively adds the chosen user to the MFA Local Account group, granting them the associated privileges to sign in to the workstations or servers.

{{< alert icon="👉" context="note" text="This functionality is compatible exclusively with Windows-based workstations or servers." />}}

* To remove a user from the MFA Local Account, click on **Delete** next to the user's name.
* If the user attempts to log in to the workstation or server via XSense CPP using their local user credentials, XSense CPP will prompt the user to connect the device and complete the device authentication process. If the device verification fails, the user will not be able to access the workstation or server.
