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
5. Open `http://localhost:8088/` on the server for the initial local setup.

The initial development configuration listens only on the local server. Network access and HTTPS certificates are configured separately before production use.

NEXUS preserves database and configuration files during ordinary uninstall.
