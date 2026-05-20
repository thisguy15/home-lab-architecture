# System Overview

This document provides a high-level overview of my home-lab environment. It outlines the core systems, their roles, and how they work together to provide storage, media, remote access, and family-centric infrastructure.

## Core Systems

### **TrueNAS Scale**
- Primary storage server
- Hosts services such as Plex, Syncthing, and Immich
- Manages datasets, shares, and snapshots
- Acts as the backbone of the home-lab

### **Raspberry Pi Devices**
- Used for lightweight services and experiments
- Includes projects such as:
  - Pi-based car audio server
  - Print server
  - Small automation tasks
- Ideal for testing, learning, and modular expansion

### **Tailscale Mesh Network**
- Provides secure remote access to all devices
- Enables cross-location connectivity for family members
- Replaces traditional VPN solutions with a simpler, more private approach

### **Media & Sync Services**
- **Plex** for media streaming
- **Syncthing** for device-to-device file sync
- **Immich** for photo and video backup
- Designed for reliability and privacy

## Purpose of the Home-Lab
- Build hands-on IT experience
- Learn system administration and networking fundamentals
- Provide reliable services for my family
- Experiment with new tools and architectures
- Document real-world troubleshooting and improvements

## High-Level Architecture
- TrueNAS acts as the central hub
- Raspberry Pis provide modular services
- Tailscale connects everything securely across locations
- Services run on a mix of containers and native apps
- Focus on privacy, reliability, and practical functionality
