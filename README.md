# Raspberry Pi Personal Cloud Storage

> A self-hosted personal cloud storage system built with Raspberry Pi, external HDD storage, Linux, and Tailscale for private remote access.

## 📌 Overview

This project is a personal cloud storage system built around a Raspberry Pi 4 and a 2 TB external hard drive. The Raspberry Pi acts as the central server while the external HDD provides the main storage capacity. The system was designed to provide access to personal files from different devices without depending entirely on a third-party cloud storage provider.

The project started as a practical experiment in building and managing a small self-hosted server. It involved setting up Raspberry Pi OS, connecting and managing external storage, configuring Linux services, and establishing remote connectivity using Tailscale. The main focus was understanding how storage, networking, hardware, and server administration work together in a real system.

---

## 🎯 Project Goals

The main objective was to build a low-cost and maintainable personal storage solution using readily available hardware.

The project focused on:

- Building a personal file storage server
- Using Raspberry Pi as a lightweight server
- Expanding storage using an external HDD
- Accessing the system remotely
- Learning Linux server administration
- Understanding storage mounting and permissions
- Using private networking for remote connectivity
- Keeping personal data under direct control

---

## 🏗️ System Architecture

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