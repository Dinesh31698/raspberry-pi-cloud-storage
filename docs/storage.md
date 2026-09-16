# Storage Management

## Overview

The storage layer is built around a 2 TB external HDD connected to the
Raspberry Pi through USB 3.0.

The external drive provides the primary location for personal files,
documents, media, and other stored data.

## Storage Architecture

```text
                    Raspberry Pi 4
                          │
                          │ USB 3.0
                          ▼
                   ┌──────────────┐
                   │    2 TB HDD  │
                   └──────┬───────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
          Documents     Media      Personal Files