---
title: "OpenSSL"
description: ""
lead: ""
date: 2022-01-25T14:41:21+01:00
lastmod: 2022-01-25T14:41:21+01:00
draft: false
images: []
type: docs
weight: 120
---

This section explains the procedure for installing the required software to set up ThinC-AUTH Bio Pro with the required certificates for biometric-based PIV authentication to successfully sign in to Microsoft Windows 10 and above securely.

The programmes that will be used to configure the ThinC-AUTH Bio Pro USB security key are listed below.

1. OpenSSL Light
2. ThinC-AUTH PIV Manager

### OpenSSL Light

The installation process is quick and easy. Run the executable after downloading and configuring the environment variables for OpenSSL.

#### OpenSSL Installation

1. Execute the downloaded installer file and install the OpenSSL on the Windows machine. Accept the licence agreement and indicate where the installation will be done. To continue, click on Next.

    ![ssl installation](images/OpenSSL_004.PNG)

2. After choosing the Start Menu location, click the Next button to begin the OpenSSL installation.

    ![ssl installation](images/OpenSSL_005.PNG)

3. Select the required additional task. We are continuing with the default selection of "The Windows System Directory" for the current installation. Select Next.

    ![ssl installation](images/OpenSSL_006.PNG)

4. Click Next after confirming the installation configuration selected.

     ![ssl installation](images/OpenSSL_007.PNG)

5. To begin the installation procedure, click Next.

     ![ssl installation](images/OpenSSL_008.PNG)

6. After the installation is successfully complete. Complete the installation by clicking Finish.

    ![ssl installation](images/OpenSSL_009.PNG)

#### Setup Environment variables

Add the Path environment variable to System Properties to set the environment variable.

* In the Run command type'sysdm.cpl'. Select Environment Variable under Advanced tab.

* Set the Path variables of the Bin folder in OpenSSL in the Environment variables window's of System Variables section.

    ![ssl installation](images/OpenSSL_012.PNG).