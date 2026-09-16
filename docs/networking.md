# Networking

## Overview

Networking is responsible for connecting the Raspberry Pi to client
devices and providing remote access to the storage system.

The system uses the local network for normal connectivity and Tailscale
as the private networking layer for remote access.

## Network Architecture

```text
                 ┌─────────────────┐
                 │ Laptop / Phone  │
                 └────────┬────────┘
                          │
                          │
                   Tailscale Network
                          │
                          ▼
                 ┌─────────────────┐
                 │  Raspberry Pi 4 │
                 │                 │
                 │  Linux Server   │
                 └─────────────────┘