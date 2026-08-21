---
layout: default
title: Installation
description: Install NEXUS on Windows Server
---

# Installation

## Before installation

- Use a supported 64-bit Windows Server.
- Sign in with an administrator account.
- Back up an existing Galaxy installation before upgrading.
- Confirm the required browser port is available.

## Install

1. Download the latest `NEXUS-Setup-*-x64.exe` file.
2. Verify its SHA-256 checksum.
3. Run the installer as an administrator.
4. Allow setup to install PostgreSQL, Apache, and NEXUS.
5. In the **Create your administrator** window, enter a username and a password of 12–128 characters, confirm the password, and select **Create administrator**.
6. After setup confirms that NEXUS is ready, open `http://localhost:8088/` and sign in with that account.

The administrator password is not written to installer logs or placed on a command line. Quiet installations skip the graphical account step; create the first account locally before enabling remote access.

The initial development configuration listens only on the local server. Network access and HTTPS certificates are configured separately before production use.

NEXUS preserves database and configuration files during ordinary uninstall.

## Upgrade

Administrators are notified inside NEXUS when a newer stable release is published. Select **Download installer**, copy the EXE to the NEXUS server if it was downloaded from a remote workstation, and run it as an administrator. Existing accounts, database contents, and configuration are preserved. Windows rejects an installer whose version is older than the installed NEXUS version.
