---
title: "Devices"
description: ""
lead: ""
draft: false
images: []
weight: 740
---

This section includes the inventory of ThinC-AUTH devices. Furthermore, it offers administrators essential details, including device assignment status, the count of enrolled fingerprints, the maximum allowable fingerprints for enrollment, and the firmware version.

Each ThinC-AUTH device comes with a unique licence depending on the deployment approach. Before distributing the devices to the organisation, based on the enterprise requirements Ensurity will generate the license and update the devices with the appropriate license.

## Adding ThinC-AUTH devices to XSense IdP portal

There are two approaches for uploading the list of ThinC-AUTH devices into the XSense IdP portal. One option is to upload the shared device licenses directly from Ensurity. Alternatively, you can use the Excel file supplied by Ensurity, ensuring that it adheres to the correct format. Or the admin can create the device manually.

In cases where the devices are initially shipped to the organization with a default license, Ensurity will generate the required licenses for each device serial number, which will then be shared with the organization. These licenses must be subsequently uploaded to the XSense IdP portal.

### Excel Operations

When the devices are shipped with the necessary licenses as per the organization's requirements, the administrator can upload these devices serial numbers to the XSense IdP portal by using the shared Excel file.

#### Upload devices

To upload the device serial numbers to the XSense IdP using the shared Excel file, the admin has to perform the action through **"Excel Operations >> Select Excel to Import >> choose file and Import the excel file"**.

In situations where Ensurity supplies solely the serial numbers of the devices, the administrator has the option to retrieve the template accessible within the XSense IdP portal. After the administrator completes the necessary information in the downloaded Excel file, they can proceed to import the files into the XSense IdP.

During the device distribution to users, administrators have the option to populate an Excel sheet with user details corresponding to each device's serial number. Subsequently, when this Excel sheet is imported into the XSense IdP portal, both the devices and the associated user information will be visible in the **Devices** section.

#### Export devices

The administrator also has the capability to extract the inventory of ThinC-AUTH devices for the purpose of conducting audits.

### Manual Device Creation

Manually creation refers to the process of adding a new ThinC-AUTH device in XSense IdP by entering the details and information directly, without relying on automated or bulk import methods. To add the device information manaully, follow the below procedure.

* Select **New Device** and complete the necessary information, including the device's serial number, UID, and Public Key. It's important to note that the serial number, UID, and Public Key are mandatory fields. If the administrator does not possess the public key, Ensurity will supply the required public key for the device.
* Click on **Save**.

### Device Licenses

From the Devices License pop up in XSense IdP, the administrators are provided with the specific information related to device licenses such as the **Public Key** or upload the device licenses to XSense IdP portal. These Licenses are shared to the organization in a **Zip** file format.

XSense IdP also offers administrators the option to export a comprehensive list of device licenses for audit purposes.

#### Upload Device Licenses

Ensurity provides a compressed zip file containing all the licenses of the devices that are sent to the organization.

* To import the ThinC-AUTH devices, navigate to Devices and click on Import Devices.
* From the file picker, choose the zip file with all the device licenses shared by Ensurity. Click on Submit.
* Once the upload is successful, all the ThinC-AUTH devices will be listed in the XSense IdP portal.

    ![AMS Devices](images/AMSDevices.png)

## Device Actions

After successfully importing ThinC-AUTH Biometric Security keys into the XSense IdP portal, it becomes crucial to determine which user should receive each device. Once users have been identified, the devices can then be physically distributed to the respective individuals. A range of actions pertaining to the ThinC-AUTH Biometric Security Key can be performed by selecting the **Actions** button adjacent to the device's serial number. The available action items are dynamic and depend on the device's assignment status.

If the device is not currently assigned to any user, the **Actions** button will display options such as "Assign to User," "Edit," and "Delete".

However, if the device is already assigned to a user, the **Actions** button will present a different set of choices, including "Unassign from User," "Set OTP," "Reset," "Unlock," "Set Max Fingers," "Edit," and "Delete."

Below are the Action items that are available:

![Device Assign](images/AMSAssignToUser.png)
<br><br>
![Set OTP](images/AMSSetOTPDropdown.png)

### Assign Device

* This identification will involve selecting a user from the list of AD users imported to XSense IdP portal.
* To assign the device to the user, navigate to **Devices>> Actions>> Assign to User**.

### Set OTP

* Once the device is assigned to the user, the admin must set a random OTP for the user to login to ThinC Manager for initiating the fingerprint enrolment.
* When the SMTP configuration is successfully set up, the system will automatically send an email to the user's organization email address once a device is assigned to them. However, if the SMTP configuration is not in place, the administrator will need to convey the OTP (One-Time Password) to the user through alternative communication channels. This remains similar for the devices that are uploaded via Excel techniques.
* This OTP is utilized during the process of registering or updation of fingerprints and when resetting the device.
* To Set the OTP for login device to the user, navigate to **Devices>> Actions>> Set OTP**.
* The OTP is valid only for one time login. if the user clicks on Logout in the ThinC Manager application, the OTP will be invalid. If the user must log in to the application again, the user must contact the admin for generating the OTP.

### Edit

* Enables the administrator to make changes to device details such as the DC date, type, and maximum number of allowed fingerprints. It's important to note that when attempting to modify device information, the device's serial number, UID, and public key cannot be altered.

### Reset

* Permits the administrator to initiate a device reset to its factory settings, enabling the user to undergo the process of fingerprint registration once again.

### Set Max Fingers

* By default, the device can store up to 5 fingerprints, however, the admin can configure the number of fingerprints the user can enroll based on the requirement.
* Go to **Actions >> Set Max Fingers** to determine the maximum number of fingerprints that are permitted by organization for each device. Please note that this setting is device-specific.

### Delete

* By executing this action, the administrator will remove the device from the XSense IdP portal. It's important to note that deleting the device in this manner does not delete the associated device license. To remove the device license, the administrator should access the **Device Licenses** section and initiate the deletion process there.
* When a previously assigned device is removed, the XSense IdP portal will unassign the device automatically.

### Unlock

If the device is locked due to wrong/invalid fingerprint authentication, then the admin can remotely unlock the device. Once unlocked, the user can authenticate the device with the registered fingerprint at the time of application, XSense CPP login.

### Unassign to user

The Admin can un-assign the device from a user by clicking on **Actions >> Un-assign** to the user. Once the device is unassigned, a reset command will be automatically initiated. If the device is assigned to a new user, and the OTP is set then in the ThinC Manager application when the new user logs into the device, the device will initiate the reset automatically.
