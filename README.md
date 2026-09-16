# Raspberry Pi Personal Cloud Storage

> A self-hosted personal cloud storage system built using Raspberry Pi, external HDD storage, Linux, and Tailscale for secure remote access.

## 📌 Overview

This project explores the design and deployment of a personal cloud storage system using a Raspberry Pi as a lightweight home server and an external HDD as the primary storage device.

The goal was to build a low-cost alternative to conventional cloud storage while gaining practical experience with Linux server administration, storage management, networking, remote access, and self-hosted infrastructure.

## 🏗️ System Architecture

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