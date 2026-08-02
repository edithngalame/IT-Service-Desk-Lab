# osTicket Helpdesk Lab Installation Guide

## Overview

This guide documents the installation and configuration process used to deploy an osTicket helpdesk environment on Ubuntu Server.

The deployment included a web server, database server, PHP environment, osTicket installation, and email notification configuration.

---

# Environment

## Operating System

Ubuntu Server

## Web Server

Apache

## Database

MariaDB

## Application

osTicket v1.18.4

## Email Service

Gmail SMTP

---

# 1. Ubuntu Server Setup

The Ubuntu Server virtual machine was installed and configured as the host environment for the helpdesk system.

Tasks completed:

- Installed Ubuntu Server
- Created administrator account
- Updated system packages
- Verified network connectivity

Example update commands:

sudo apt update
sudo apt upgrade

# 2. Apache Web Server Installation

Apache was installed to provide the web server enviroment required by osTicket.

## Installation
     sudo apt install apache2

## Service verification
     sudo systemctl status apache2

# 3. MariaDB Database Installation

MariaDB was installed as the database service.

## Installation
     sudo aot install mariadb-server

## Service verification
     sudo systemctl status mariadb

Database security configuration was completed using:
     sudo mariadb-secure-installation

# 4. PHP Installation

PHP and required extensions were installed to support osTicket.

Installed components included:

- PHP
- PHP MySQL support
- PHP XML
- PHP GD
- PHP IMAP
- PHP MBString
- PHP CLI

# 5. osTicket installation

The osTicket application files were transferred to the Ubuntu server.

Installation process:

1. Extracted osTicket archive
2. Moved files into the Apache Web direcotry.
3. Configured permissions.
4. Created te required database.
5. Completed the web-based installation wizard.

# 6. osTicket Configuration

The helpdesk was configured with:

## Departments

- Service Desk
- Hardware Support
- Software Support
- Network Support

## Staff Accounts

Created support agents for different departments.

## Help Topics

Configured categories for different ticket types.

## SLA Plans

Created priority-based SL handling

# 7. Email Configuration

Outgoing email was configured using Gmail SMTP.

## Configuration:

- SMTP Server:
      smtp.gmail.com

- Port:
      587

- Authentication:
      Basic Authentication

- Ecryption:
      TLS

A Google App Password was used for SMTP authentication.

Email notifications were successfully tested.

# 8. Verification

The completed enviroment was tested by:

- Creating support tickets.
- Assigning tickets to agents
- Applying SLAs
- Escalating tickets
- Sending customer responses
- Testing email notifications
