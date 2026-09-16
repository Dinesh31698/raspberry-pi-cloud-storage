# Setup Guide

## Overview

This document describes the general setup used to build the Raspberry Pi
personal cloud storage system.

The system consists of a Raspberry Pi 4, Raspberry Pi OS, an external
2 TB HDD, and Tailscale for remote connectivity.

The original implementation is no longer available, so this document
focuses on the setup process and configuration approach rather than
providing a copy-paste deployment script.

## Hardware Requirements

| Component | Purpose |
|---|---|
| Raspberry Pi 4 | Main server |
| 2 TB External HDD | Primary storage |
| Raspberry Pi Power Supply | Power |
| Network Connection | Network access |
| USB 3.0 Connection | HDD connection |

## 1. Prepare the Raspberry Pi

Install Raspberry Pi OS on the Raspberry Pi and connect it to the
network.

After starting the system, update the installed packages:

sudo apt update
sudo apt upgrade