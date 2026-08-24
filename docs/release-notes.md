---
layout: default
title: Release notes
description: NEXUS release history
---

# Release notes

## 1.2.3

- Adds **Show details** and **Hide details** controls to the Windows installer.
- Shows the current installer action inside setup without opening command or PowerShell windows.
- Keeps the graphical initial-administrator setup visible when an account is required.
- Adds a release-build check that prevents console-based setup helpers.

## 1.2.2

- Adds the NEXUS-owned native Windows file/folder picker used by Galaxy apps.
- Runs the picker in the signed-in user's desktop session while keeping NEXUS
  and product services isolated from interactive Session 0 UI.
- Protects picker requests with the existing NEXUS session and CSRF controls
  and an ACL-restricted Windows named pipe instead of a new network listener.
- Requires one Windows sign-out/sign-in after installation or upgrade to start
  the per-user picker broker.

## 1.2.0

- Adds the shared Galaxy application switcher used by hosted products.
- Standardizes the NEXUS application-picker icons for PULSAR and SUPERNOVA.
- Uses the shared Galaxy light/dark switch and PULSAR-style toast notifications.
- Keeps product Download and Update actions connected to the official PULSAR and SUPERNOVA public release repositories.

## 1.1.0

- Adds an administrator-only in-app notification when a newer stable NEXUS release is available.
- Links directly to the official Windows installer and public release details.
- Corrects packaged version reporting so upgrade comparisons match the installer version.
- Keeps update installation administrator-approved on the NEXUS server; the browser does not silently replace server software.
- Prevents long-running product telemetry streams from retaining NEXUS PostgreSQL sessions and eventually making the Hub unresponsive.
- Adds bounded product-proxy connection waits and keeps liveness independent of the synchronous worker pool.
- Moves synchronous registry and authentication queries off the asynchronous server loop so refreshing the Hub cannot wedge NEXUS while PostgreSQL resources are busy.
- Serves NEXUS Hub assets without an unnecessary product-registry query.
- Stops PULSAR and other PostgreSQL-dependent product services before taking the shared database offline for a NEXUS upgrade.
- Restores services when upgrade preparation fails and validates consecutive-version upgrades with PULSAR installed.

## 1.0.0

Initial public Windows Server release with NEXUS, PostgreSQL 18, source-built Apache, centralized authentication, and Windows service installation.
