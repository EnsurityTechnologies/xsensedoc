---
title: "ThinC-AUTH Introduction"
description: ""
lead: ""
date: 2022-01-25T14:41:21+01:00
lastmod: 2022-01-25T14:41:21+01:00
draft: false
images: []
type: docs
weight: 10
---

Ensurity, partnering with Microsoft and FIDO Alliance, has developed ThinC-AUTH, a Biometric FIDO2 Security Key to enable passwordless / strong secure authentication. Ensurity’s Biometric FIDO2 Security Keys allows the user to carry his/her credential with them and safely authenticate without passwords.

## ThinC-AUTH: Key Features

- Compatible with FIDO2 / WebAuthN standards
- Supports Passwordless Authentication
- Supports up to 30 different WebAuthn accounts (Resident Key) for passwordless authentication
- Supports unlimited WebAuthn accounts (Server Key) for two-factor authentication 
- Compatible with Microsoft Windows, MacOS, and Linux platforms — works with most of the latest version of browsers
- High-quality, durable, and waterproof casing
- Strong and compact design for everyday use
- Cost-efficient alternative to expensive readers
- 360° fingerprint touch sensor (with a life over 200,000 times)
  - High-definition, fast and accurate fingerprint recognition (<1 sec., FAR <0.001%, FRR <1%) 
  - Accepts only live fingerprints and prevents from spoofed biometric authentication
  - Fingerprint minutiae templates are encrypted and stored within the device
  - High fingerprint capacity – stores up to five fingerprints

## Architecture

![AUTHArchitecture](images/AUTH_Architecture.png)

## Importance of Biometrics in FIDO2 Security Key

A FIDO2 hard authentication token without biometrics merely authenticates the holder of the hard token at the time of authentication; it does not necessarily authenticate the original token owner. If a token is lost or misappropriated, it can be used to easily impersonate. 

Biometric technology makes FIDO2 Security Key one of the most secure authenticators. The unique identity of the biometric minutiae prevents any misuses of the token from people other than authorized user and losing the key will cause no security risk at all.

ThinC-AUTH security key is built with state-of-the-art biometric 360° touch sensor from a leading OEM. Fingerprint minutiae templates obtained from sensor are completely encrypted, securely stored and confined to the device. This biometric touch sensor is exceptionally responsive; ThinC-AUTH uses hardware to match enrolled fingerprint, unlocking device and securely authenticate using FIDO2/U2F. Fingerprints and digital identity remain private on device and protected by advanced encryption.

## Device Modes

ThinC-AUTH devices can be set to different modes to align with specific requirements. The device's configuration and license are managed at the firmware level, and the choice of license impacts the functionality, including the fingerprint enrollment application.

### Corporate Mode

ThinC-AUTH come with corporate licenses that are specially made to meet the needs of the organization. These devices connect to the XSense IdP portal, enabling remote actions such as enable fingerprint enrollment, device lock, reset in the event of loss or theft. With this proactive strategy, sensitive organizational data is protected from unauthorised access. Furthermore, users must enrol their fingerprints using the ThinC Manager application when these devices are issued with corporate licenses.

### Standalone Mode

ThinC-AUTH devices are configured in standalone mode where these devices operate independently without connecting to a centralized server, such as the XSense IdP portal. The user can enroll the fingerprints using ThinC-AUTH Manager tool that can be downloaded from our **<a href="https://ensurity.com/Products/ThinC_AUTH#Resources">website</a>** or use the default tool available in Windows **Settings**.

## What is FIDO2?

FIDO2 (Fast IDentity Online 2) is a very strong authentication for a passwordless feature or at the very least as a second factor, using public key cryptography to bring easy to use, unphishable credentials to the masses. FIDO2 is the evolution of the original FIDO UAF and U2F specifications. Whereas U2F was only supported by Chrome & Opera, FIDO2 already has significant traction in all major browsers. FIDO2 is open, scalable, interoperable ecosystem of compact hardware that can be used with many FIDO enabled Apps and Websites. A single device can be used for multiple FIDO enabled services.

![Alt text](images/fido.png)

> FIDO2: WebAuthn & CTAP Flow image courtesy fidoalliance.org

## What Makes FIDO2 Better?

FIDO2 authenticators differ themselves from smart cards mainly with the feature of “intent”. To use the authenticator, a user must be present and provide some sort of input to the device (ThinC-FIDO2 is facilitated with biometric authentication – tightly locking it to the user). This prevents malware from triggering the authenticator without the user’s knowledge. They then prove themselves above devices such as RSA tokens by being able to reuse one authenticator across multiple applications, and in a secure fashion. OTP as a second factor has had a decent adoption rate compared to alternatives; however, it is observed that more and more successful phishing attacks against OTP methods, whether it’s SMS (bad) or OTP apps. While these attacks usual prey on the user themselves to give up the code to the attacker, a FIDO2 authenticator is unphishable; no matter what the attacker does or gets the user to do, they will not be able to steal their credentials.

> Material in this page is copy right of FIDO Alliance.
