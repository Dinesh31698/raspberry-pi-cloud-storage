# System Architecture

## Overview

The Raspberry Pi Personal Cloud Storage system is built around a simple
server-and-storage architecture. A Raspberry Pi 4 acts as the central
server, while a 2 TB external HDD provides the primary storage capacity.

Client devices such as laptops and phones connect to the Raspberry Pi
through the network. Tailscale provides the private connectivity layer
for remote access, while SSH is used for server administration.

## Architecture Diagram

```text
                         ┌───────────────────┐
                         │   Client Devices  │
                         │                   │
                         │ Laptop / Phone    │
                         └─────────┬─────────┘
                                   │
                                   │
                            Tailscale Network
                                   │
                                   ▼
                         ┌───────────────────┐
                         │   Raspberry Pi 4  │
                         │                   │
                         │ Raspberry Pi OS   │
                         │ Linux Services    │
                         │ SSH               │
                         └─────────┬─────────┘
                                   │
                                USB 3.0
                                   │
                                   ▼
                         ┌───────────────────┐
                         │      2 TB HDD     │
                         │                   │
                         │ Personal Files    │
                         │ Documents         │
                         │ Media             │
                         └───────────────────┘