# Security

## Overview

Security is an important consideration for any self-hosted storage
system because the server provides access to personal data.

This project uses a private networking approach with Tailscale and
SSH for remote administration. However, private networking is only
one part of the security model. The operating system, user accounts,
permissions, services, storage, and backup strategy must also be
managed correctly.

---

## Network Security

The system uses Tailscale for remote connectivity instead of relying
on direct public exposure of the Raspberry Pi.

The basic model is:

```text
Client Device
      │
      ▼
Private Tailscale Network
      │
      ▼
Raspberry Pi
      │
      ▼
Storage