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

This section outlines the necessary configuration for automating the process of sending emails to designated recipients in XSense IdP. They include specifying recipient email addresses, determining the frequency of report delivery, and selecting the report format (e.g., PDF or Excel). This emailing features works when the SMTP configuration is completed in XSense IdP.

**Set Timer**: When the admin clicks the **Set Timer** button, they need to specify the date and time for scheduling the email reports. After specifying the date and time, the email reports will be sent to the designated email address at the specified date and time.

* XSense IdP dispatches email reports on a regular basis, including daily, weekly, and monthly frequencies. The date and time configuration pertains to when these email reports are scheduled to be sent to the designated email addresses.

    ![Email report configuration](images/emailreportconfigsettime.png)

**Add Email address**: The admin must specify the email address which is going to receive the reports. Typically, a group email ID is used for sending the emails. XSense IdP permits the inclusion of multiple email addresses as recipient email addresses.

* To receive reports regarding events within the XSense IdP environment, click the **+** button and in the "Add User" popup, input the email address to which the reports should be sent. Then, click **Save**.

* XSense IdP allows multiple email addresses to receive the same reports, without limiting it to just one email address.

    ![Email report configuration](images/emailreportconfig.png)
