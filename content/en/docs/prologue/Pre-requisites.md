---
title: "Pre-requisites"
description: ""
lead: ""
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 130
toc: true
---


| **A) Recommended Hardware configuration for managing around 5,000 Users** |
| :---- |
- CPU with hyper-threading capabilities
- RAM between 8GB and 16GB
- High-speed Storage Drive
- Physical Server (*Recommended hardware: Intel Xeon or similar compatible CPU, 16GB RAM, Hard Disk (50GB for the server portal); should be scalable to production environment*)
- Virtual Machine (*Recommended VM with Dual/Quad Core CPU, 8GB+ RAM, 100GB+ storage*)

| **B) Recommended Software modules** |
| :---- |
- MS Windows Server 2016+ (IIS with ARR facility)
- dotNet Hosting 6.0.8
- dotNet Core 6.0.x
- IIS website creation and manage permissions
- IIS URL Rewrite executable
- Chrome standalone installer
- Notepad++ zip
- SSL/TLS certificate *(recommended to use Organization’s SSL certificate and if Organization is unable to provide, self-signed SSL will be used)*
- MS SQL Database Server 2016+ *(recommended to deploy both the Application Portal and Database Server on different systems)* 

| **C) Required Network Access Permissions** |
| :---- |

Allow traffic between XSense IdP Server, Database Server, Local-AD, XSense CPP Client Tool, CPP Agent Tool, and XSense Mobile App 
- Configure Network Access in Switch / Firewall / Router for on-prem deployment:
  - Enable port # 443 for XSense Server portal
  - Enable port # 1443 for Database server
- Enable network connectivity between XSense MFA Server portal and the Database Server
- Enable network access for the secure API communication between XSense CPP Tool and XSense MFA Server portal

| **D) End-User Windows Workstations - OS Versions** |
| :---- |
- End-user’s Widows OS version should be Windows 7 Pro and above releases 
- Workstations must be installed with applicable updated service packs / security patches, as recommended by Microsoft

---
