---
title: "Devices"
description: ""
lead: ""
draft: false
images: []
weight: 660
---

The AMS tab contains the list of ThinC-AUTH devices and the list of Privileged users. 
Device

This tab contacts the list of ThinC-AUTH devices. The ThinC-AUTH devices can be imported to the XSense CP server using a predefined Excel template available in the XSense CP server or Ensurity-shared Excel in the predefined format or upload the device licenses shared by Ensurity. 

## Device License

* To import the ThinC-AUTH devices, navigate to Devices and click on Import Devices.
* From the file picker, choose Excel with the devices list and click on Submit.
* Once the upload is successful, all the ThinC-AUTH devices will be listed in the XSense CP Server.

    ![AMS Devices](images/AMSDevices.png)

## Device Assignment

Once the ThinC-AUTH Biometric Security keys are successfully imported to the XSense CP server, the devices can be assigned to the Users.

### Device Actions

* After the devices are imported to the XSense, the admin user can perform the below actions. 

    1) Assign to User:
        * To assign the device to the user, navigate to Devices>> Actions>> Assign to User

        ![Device Assign](images/AMSAssignToUser.png)

        * Once the device is assigned to the user, the admin must set a random OTP for the user to login to ThinC Manager for initiating the fingerprint enrolment.

    2) Edit: 
    3) Delete
    4) Set OTP
    5) Reset
    6) Set Max Fingers
    7) Unlock
    8) Unassign to user



    ![Set OTP](images/AMSSetOTPDropdown.png)

*	The OTP is used for logging in to the ThinC Manager application, the OTP will be expired. If the user must log in to the application again, the user must contact the admin for generating the OTP.

    ![AMS Set OTP](images/AMSSetOTP.png)

* The admin share the OTP to the user verbally or an automated email is sent to the users email if the SMTP is configured. Once the user receives the OTP, the user can login to the ThinC Manager. 


    -  **Unassign to User**: The Admin can un-assign the device from a user by clicking on Actions>> Un-assign to the user. Once the device is unassigned, a reset command will be automatically initiated. If the device is assigned to a new user, and the OTP is set then in the ThinC Manager application when the new user logs into the device, the device will initiate the reset automatically. 

    - **Unlock**: If the device is locked due to wrong/invalid fingerprint authentication, then the admin can remotely unlock the device. Once unlocked, the user can authenticate the device with the registered fingerprint. 

    - **Set Max's fingers**: By default, the device can store up to 5 fingerprints, however, the admin can configure the number of fingerprints the user can enroll based on the requirement.

    - **Reset**:
    - **Edit**:
