---
layout: default
title: Release notes
description: NEXUS release history
---

# Release notes

## Next release

- Adds an administrator-only in-app notification when a newer stable NEXUS release is available.
- Links directly to the official Windows installer and public release details.
- Corrects packaged version reporting so upgrade comparisons match the installer version.
- Keeps update installation administrator-approved on the NEXUS server; the browser does not silently replace server software.
- Prevents long-running product telemetry streams from retaining NEXUS PostgreSQL sessions and eventually making the Hub unresponsive.
- Adds bounded product-proxy connection waits and keeps liveness independent of the synchronous worker pool.

## 1.0.0

Initial public Windows Server release with NEXUS, PostgreSQL 18, source-built Apache, centralized authentication, and Windows service installation.
