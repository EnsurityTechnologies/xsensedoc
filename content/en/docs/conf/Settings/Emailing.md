---
title: "Emailing"
description: ""
lead: ""
date: 2020-11-12T15:22:20+01:00
lastmod: 2020-11-12T15:22:20+01:00
draft: false
images: []

weight: 810
toc: true
---

This section describes the process of configuring SMTP details for sending email notifications or alerts to users, administrators, or reports to administrator. This is important for various purposes, including user account management, security alerts, and communication within the XSense IdP portal.

* Navigate to the **Settings >> Emailing** tab and provide the below information.

  1. **Default from display name**: Used as the sender's display name

  2. **Default from address**: Specify the email address of the SMTP server that will be used to send emails.

  3. **Host**: The IP/Domain of the SMTP server

  4. **Port Number**: Specify the port number that the SMTP server uses for sending emails. Common port numbers for SMTP include 25, 587, and 465 for secure connections.

  5. **Enable SSL**: Depending on security requirements, check the checkbox to enable SSL encryption for the SMTP connection. Secure connections are recommended to protect email communications.

  6. **Use default credentials**: When this is checked, XSense IdP uses the default credentials configured in the SMTP server. If this unchecked, XSense IdP requires authentication to prevent unauthorized access. Provide a valid credentials (username and password) for an email account authorized to send messages through the SMTP server.

  7. **UserName & Password**: Specify the email address and the associated password from which emails will be sent. This is typically an email address associated with the identity management system or the application.

  8. **Send test email**: After configuring SMTP, it's advisable to perform testing to ensure that email notifications are sent successfully.

* Click on **Save** after entering the necessary details.

    ![SMTP configuration](images/smtpconf.png)
