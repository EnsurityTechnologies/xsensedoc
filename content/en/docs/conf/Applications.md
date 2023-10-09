---
title: "Applications"
description: ""
lead: ""
draft: false
menu: 
  docs:
    parent: "help"
weight: 720
toc: true
---

This section describes the various application that can be integrated with XSense IdP for single sign-on (SSO) or  authorise access to resources.

The XSense IdP Server empowers modern organizations with protection against communication threats & data interception; and provides military grade end-to-end secure communication between the connected applications.

Enterprise Applications (browser-based) can be integrated to XSense Server through standard ‘SAML’ or ‘OpenID Connect’ interfaces to facilitate passwordless authentication, and to allow the users to use single sign-on (SSO) to access connected services/applications.

Enterprise home-grown / Thick Client applications, where the standard interfaces (SAML / OIDC) are not feasible for configuration, Ensurity can support them by providing a compatible SDK module, to enable passwordless authentication.

![LDAP](images/XS_WebAppsarch.png)

XSense IdP Server supports several authentication solutions, including Ensurity’s ‘XSense Verify Mobile Authenticator App’ for Smartphones (Android & iOS), and ‘ThinC-AUTH’ Biometric Security Key; in addition to the standard OATH-TOTP/HOTP based mobile authenticators, and SMS Codes.

The solution has intuitive design interface and facilitates the Admin users with the following processes:

* Easy user registration process
* Assigning choice of multi-factor authentication mechanisms to users
* Integration with Microsoft Active Directory
* Monitoring & Analysis of User login activity

The following industry-standard authentication methods are used by XSense IdP Platform:

| Protocol|Version|
|----------|:----------:|
| SAML | 2.0 |
| OIDC | 1.0,2.0 |

## API Keys

An API key is used to identify and authenticate an application. They act as unique identifiers and provide a secret token for the authentication process. The APIs are the interface that helps the XSense IdP Server communicate with the XSense CPP application and ThinC Manager.

* To generate a new key, navigate to API keys under the Applications section. Click on New API Key and provide the Name of the API key and a key value. The key value can be alphanumeric and contain special characters. Click on save.

{{< alert icon="👉" context="note" text="The admin does not have to generate the API keys regularly." />}}

### ThinC Manager Installation with API Config file

Download the API config file and place the API config file in the same folder of the ThinC Manager installer. Once the ThinC Manager installation is initiated, the installer will automatically fetch the available API config and complete the installation.

### XSense CPP Installation with API Config file

Place the API config file in the same folder of the XSense CPP installer. Once the XSense CPP installation is initiated, the installer will automatically fetch the available API config and complete the installation.

## OpenID

OpenID is an open standard and decentralized authentication protocol that enables users to log in to multiple websites and applications using a single set of credentials. OpenID is a simplified identity layer implemented on top of the OAuth 2.0 protocol. The OpenID protocol allows users to authenticate themselves with an OpenID provider, such as XSense IdP Server,Google or Facebook. After being verified, the user is given a special ID called an OpenID, which they can use to log into any number of websites that use OpenID authentication through XSense IdP with multi-factor authentication.

With OpenID, users can enjoy the convenience of using a single set of login credentials across multiple platforms, reducing the burden of remembering multiple usernames and passwords. XSense IdP Server offers  more secure / multi-factor authentication techniques, lowering the danger of password-related vulnerabilities such weak passwords or password reuse. The administrator can add several applications to enable multi-factor authentication or SSO from the XSense IdP dashboard.

### Adding an Application

* To add a application, click on **New Application**.

![LDAP](images/newopenid.png)

* Enter the required details and choose the necessary scopes for the application and click on **Save**.

## OpenID Scopes

In the context of OpenID, scopes refer to the permissions or access rights requested by an application when authenticating a user. Scopes determine the level of information and functionality that an application can access on behalf of the user.

When a user attempts to authenticate with an XSense IdP, the application requesting authentication can specify the scopes it requires. These scopes typically correspond to specific user attributes or resources that the application needs to access.

The XSense IdP presents the requested scopes to the user during the authentication process, informing them about the level of access the application is requesting. The user can review and decide whether to grant the requested scopes or not. This ensures transparency and gives users control over the information they share with applications.

Scopes help protect user privacy by allowing users to limit the access an application has to their personal data. Users can grant or deny scopes based on their trust in the application and their comfort level with sharing certain information.

OpenID supports a range of standard scopes, such as profile information, email address, offline access, and specific application-defined scopes. The availability of scopes may vary depending on XSense IdP and the configuration of the application.

### Creation of OpenID Scope

* Login to XSense IdP portal and navigate to **Administration > Applications> OIDC Scopes**.
* Click on **New Scope** on the top right corner. Enter the required details of the scope you are creating and click on **Save**.

  ![New OpendID Scope](images/OIDCNewScope.png)

* These additional scopes created can be used at the time of application configuration in **OIDC**.  

  ![New OpendID Scope](images/OIDCScope.png)

## SAML

Web applications leveraging SAML-based authentication are supported by XSense IdP. Using the SAML protocol, your web application initiates the transfer of authentication and authorization metadata with XSense IdP.

### Adding a new application

To configure an application using SAML protocol, please follow the below steps.

* Login to XSense IdP portal and navigate to **Administration>Applications>SAML**.
* Click on **New Application** and furnish the required details such as Name, Description and logo(optional) under the General Settings tab.

  ![new SAML application](images/SAMLNewApp.png)

* Once the information is entered in the General Settings, navigate to the next tab **Configure SAML**. Enter the necessary details. This information will be obtained from your web application SAML configuration section.

  ![new SAML application](images/SAMLNewAppconfigsaml.png)

* In your web application, under the SAML configuration enter the details of XSense IdP server or download the XSense IdP meta file and upload it in your web application. Review the entered information and click on **Save**.

  ![new SAML application](images/SAMLNewAppISC.png)

* When the user tries to login your web application, the user will be redirected the XSense IdP portal page with the available MFA options provided to the user.
