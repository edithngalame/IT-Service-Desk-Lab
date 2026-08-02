# osTicket Email Configuration Notes

## Overview

This document records the email configuration used for the osTicket helpdesk environment.

Email functionality was configured to allow the system to send ticket notifications to users and support staff.

---

# Email Provider

Provider:

Gmail SMTP

Purpose:

Outgoing ticket notifications and system alerts.

---

# SMTP Configuration

SMTP Server:

smtp.gmail.com

Port:

587

Encryption:

TLS

Authentication:

Basic Authentication

Username:

Configured Gmail account

Password:

Google App Password

---

# Security Notes

A Google App Password was used instead of the normal Gmail account password.

Sensitive credentials are not stored in this repository.

---

# Testing

Email functionality was verified by:

1. Creating a test ticket.
2. Confirming the ticket was created successfully.
3. Receiving the osTicket email notification.

Result:

Successful email delivery confirmed.

---

# Notes

For production environments, a dedicated service acco
