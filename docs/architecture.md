# System Architecture

## Overview

The system is built around a Raspberry Pi 4 that acts as the main
storage server. A 2 TB external HDD is connected to the Pi and holds
the stored data.

For remote access, the Raspberry Pi is connected to a Tailscale
network. This allows authorized devices such as a laptop or phone to
reach the Pi without exposing the storage server directly to the
public internet.

The setup is intentionally simple:

- Raspberry Pi 4 — server and system management
- 2 TB HDD — primary storage
- Tailscale — private remote connectivity
- SSH — remote administration

## Architecture

flowchart TB
    A["Laptop / Phone"] -->|Private Network| B["Tailscale"]
    B --> C["Raspberry Pi 4<br/>Raspberry Pi OS"]
    C -->|USB 3.0| D["2 TB External HDD<br/>Primary Storage"]
    B -->|Remote Administration| E["SSH"]
    E --> C