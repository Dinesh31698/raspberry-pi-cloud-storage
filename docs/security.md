# Security

## Overview

Security was considered mainly around two areas of the system:

1. Remote access to the Raspberry Pi
2. Protection of the data stored on the external HDD

The system uses Tailscale for private remote connectivity and SSH for
remote administration.

This is a personal self-hosted setup, so it does not provide the same
security controls or redundancy as a managed cloud-storage platform.

## Network Security

The Raspberry Pi is not intended to be directly exposed to the public
internet.

Tailscale provides the private network used to connect authorized
devices to the Raspberry Pi.

Client Device
      │
      ▼
Tailscale Network
      │
      ▼
Raspberry Pi
      │
      ▼
Storage