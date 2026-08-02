# osTicket Helpdesk Lab Troubleshooting

This document records issues encountered during the installation, configuration, and testing of the osTicket helpdesk environment.

---

# Issue 1 — MySQL Command Not Found

## Issue
Attempting to run MySQL commands returned:
               mysql: command not found

## Cause
MariaDB was installed instead of MySQL. The system database service was running, but the MySQL client command was not available.

## Resolution
Verified the MariaDB service was active:
              sudo systemctl status mariadb
Accessed the database using:
              sudo mariadb

Confirmed the database service was working correctly.

---

# Issue 2 — PHP IMAP Package Installation Failed

## Issue
Attempting to install the PHP IMAP package returned an error indicating that the package was unavailable.

## Cause
The required PHP package name was not available in the current Ubuntu repository configuration.

## Resolution
Reviewed available PHP packages and continued with the compatible packages required for osTicket installation.

---

# Issue 3 — osTicket Configuration File Missing

## Issue
The osTicket installer displayed:
            Configuration file missing

## Cause
The required configuration file had not yet been created from the sample configuration file.

## Resolution
Created the configuration file and adjusted the required permissions before continuing the installation process.

---

# Issue 4 — Email Notifications Not Sending

## Issue
osTicket tickets were created successfully, but email notifications were not being delivered.

## Cause
The default system email was configured, but outgoing SMTP settings were not configured.

## Resolution
Configured Gmail SMTP:

- SMTP Host: smtp.gmail.com
- Port: 587
- Authentication: Basic Authentication
- Encryption: TLS

Created a Google App Password and used it for SMTP authentication.

Verified successful email delivery by creating a test ticket.

---

# Issue 5 — SMTP Authentication Setup

## Issue
Gmail SMTP authentication could not be completed using a normal Gmail password.

## Cause
Google blocks less secure application access using normal account passwords.

## Resolution
Enabled Google 2-Step Verification and created a Google App Password for osTicket SMTP authentication.

---

# Summary

The troubleshooting process demonstrated:

- Linux service troubleshooting
- Database administration
- Web application configuration
- PHP compatibility troubleshooting
- SMTP configuration
