# Setup Guide

## Overview

This document describes the general setup process used to turn a
Raspberry Pi 4 into a personal storage server with an external HDD
and private remote connectivity.

The setup consists of four main stages:

1. Prepare the Raspberry Pi
2. Connect and configure external storage
3. Configure network connectivity
4. Enable remote administration and access

---

## 1. Raspberry Pi Setup

The Raspberry Pi runs Raspberry Pi OS and acts as the central server.

After installing the operating system, the initial setup should include
updating the system packages and confirming that the device is
connected to the network.

```bash
sudo apt update
sudo apt upgrade