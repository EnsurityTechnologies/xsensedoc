---
title: "Email Report Configuration"
description: ""
lead: ""
date: 2020-10-06T08:49:15+00:00
lastmod: 2020-10-06T08:49:15+00:00
draft: false
images: []
weight: 900
---

This section outlines the necessary configuration for automating the process of sending emails to designated recipients in XSense IdP. They include specifying recipient email addresses, determining the frequency of report delivery, and selecting the report format (e.g., PDF or Excel).

This emailing features works when the SMTP configuration is completed in XSense IdP. By default, the admin receives reports containing audit logs, security logs, device logs, and records of failed Windows sign-ins.

**Set Timer**: When the admin clicks the **Set Timer** button, they need to specify the date and time for scheduling the email reports. After specifying the date and time, the email reports will be sent to the designated email address at the specified date and time.

**Add Email address**: The admin must specify the email address which is going to receive the reports. Typically, a group email ID is used for sending the emails. XSense IdP permits the inclusion of multiple email addresses as recipient email addresses.
