---
title: "ThinC-AUTH PIV Manager"
description: ""
lead: ""
date: 2022-01-25T14:41:21+01:00
lastmod: 2022-01-25T14:41:21+01:00
draft: true
type: docs
weight: 120
---


The corresponding certificate and key are loaded using this application onto the ThinC-AUTH BioPro security key. The loaded certificate can be wiped out and the certificate PIN can be reset, using this utility.

1. Download and launch the ThinC-AUTH PIV Manager.exe.

    ![ssl installation](images/PIVManager_002.png)

2. Click "Connect Card" upon plugging the ThinC-AUTH Bio Pro into the computer's USB port. Click on PIV to unlock further options.

    ![ssl installation](images/PIVManager_003.png)

3. The tool provides the below options

    * Key + Certificate
    * Reset PIV
    * Reset PIN

   ![ssl installation](images/PIVManager_004.png)

## Key + Certificate

When the user selects this option, they can upload the key along with the corresponding certificate to the connected ThinC-AUTH Bio Pro security key.

![ssl installation](images/PIVManager_005.png)

* The admin must select the user certificate and the corresponding key. Click on Upload to upload the certificate.

![ssl installation](images/PIVManager_006.png)

![ssl installation](images/PIVManager_008.png)

> The certificate can be loaded instantly for a brand-new or fresh device.
> Before uploading a new user certificate to a used device, the device must have at least one user fingerprint.

Once the user certificate is loaded onto the ThinC-AUTH Bio Pro, the device can be shared with the users for fingerprint enrolment using the default Windows Settings or ThinC-AUTH Manager.

## Reset PIV

* A user fingerprint must be present on the device in order to reset the certificate loaded ThinC-AUTH Bio Pro. If the user fingerprint is not available, the administrator or user must enrol their fingerprints on the device before beginning the reset procedure.

* To begin the reset procedure, click Reset PIV and then touch the sensor when there are lights on the device.  

* Upon successful completion of the reset procedure, disconnect and reconnect the device.

> Only the user certificate is erased from the device when the admin performs the Reset of the ThinC-Auth Bio Pro security key via the PIV Manager.

> When the user resets the device using the Windows Settings / ThinC-AUTH fingerprint enrolment manager tool, the fingerprints and associated PIN, as well as application secrets, are erased from the device. This has no impact on the user certificate.

## Reset PIN

The certificate PIN is usually generated by the administrator; however, the user has the option to reset the PIN and set a custom using the ThinC-AUTH PIV Manager application. This PIN must be entered by the user upon PC login using the ThinC-AUTH Bio Pro.

* To create a new PIN, select Reset PIN, enter the old and new PINs, and then confirm the PIN. Select Update PIN.

    ![ssl installation](images/PIVManager_011.png)

* After successfully updating the PIN, the user can sign in to the PC with ThinC-AUTH Bio Pro.