---
title : "ThinC Manager"
description: ""
lead: ""
draft: false
images: []
weight: 130
toc: true
---

ThinC Manager is software utility required for managing ThinC-AUTH USB device. The device can be used as authenticator device for FIDO2 services after registering a user to the device using ThinC Manager tool.

After the devices are assigned to the users, the ThinC Manager is required for fingerprint enrolment and registering the key with the services. The ThinC Manager tool has two sub-windows i.e., 

* Enroll Fingerprints
* Account Management

## Fingerprint Enrolment
ThinC Manager is a software utility required for managing ThinC-AUTH Biometric Security Key USB devices.

* Launch the ThinC Manager tool with Admin privileges and connect the device to the PC/laptop USB port. The application will automatically detect the connected ThinC-AUTH Biometric Security Key.

![thincmanager](images/thincmanager.png)

* Log in using the Username and OTP provided by the Administrator.

![userlogin](images/thincmanageruserlogin.png)

*	The Dashboard displays all the available functions such as Enroll Fingerprints and Account Management.
*	From the dashboard, the user will can obtain the details such as number of fingerprints enrolled, maximum fingerprints enrollment supported, Device serial number and the firmware version of the device.
*	To initiate the fingerprint enrolment, click on Add the fingerprint and place the chosen finger on the fingerprint sensor to continue and complete the enrolment process, finger must be placed multiple times on the fingerprint sensor till the enrolment process reaches 100%. As a best practice place your finger at slightly different angles each time to enroll your finger quickly.

![Finger Enrol](images/thincmanagerdashboard.png)

![Alt text](images/TMFinerprintenrol.png)

* After the fingerprint enrolment process is completed, the tool displays a notification stating fingerprint "Fingerprint Enrolment Completed successfully" message. Click on “Ok.”

![Alt text](images/TMfingerenrolsuccess.png)

![Alt text](images/TMFingersucessdashboard.png)

*	Maximum 5 Slots are available for enrolment of fingers.

## Key Registration

*	Once the user completes the fingerprint enrolment process, the user must register the key from the Register tab.

![Alt text](images/TMKregistration.png)

*	Click on Register and touch the sensor with the enrolled finger to complete the registration process.
*	Once the key is registered the Whitelisted PCs are mapped to the user in the server and user AD profile.

![Alt text](images/TMDeviceregistationsuccess.png)