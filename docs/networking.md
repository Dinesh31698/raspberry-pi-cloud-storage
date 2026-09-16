# Networking

## Overview

Remote access to the Raspberry Pi is handled through Tailscale.

The main reason for using Tailscale was to avoid exposing the Raspberry
Pi directly to the public internet. Devices that are part of the same
Tailscale network can communicate with the Pi using its private
Tailscale address.

The network setup is:

Laptop / Phone
      │
      │
      ▼
 Tailscale Network
      │
      ▼
Raspberry Pi 4
      │
      ├── SSH
      │
      └── Storage