# Services Overview

This document outlines the key services running in my home-lab environment. Each service supports storage, media, syncing, or remote access workflows designed for reliability, privacy, and practical day-to-day use.

## Core Services

### **Plex Media Server**
- Hosted on TrueNAS Scale
- Provides media streaming for the household
- Accessible locally and remotely through Tailscale
- Uses hardware-accelerated transcoding when available
- Organized into libraries for movies, shows, and family content

### **Syncthing**
- Runs on TrueNAS and personal devices
- Provides encrypted, peer-to-peer file synchronization
- Replaces cloud storage for many workflows
- Ensures files stay consistent across:
  - Laptops
  - Phones
  - Raspberry Pis (when needed)
- No central server required; fully private

### **Immich**
- Self-hosted photo and video backup solution
- Replaces Google Photos with a privacy-first alternative
- Automatically backs up:
  - Family photos
  - Videos
  - Screenshots
- Runs on TrueNAS with GPU acceleration when supported

## Supporting Services

### **Tailscale**
- Installed on TrueNAS, Raspberry Pis, and personal devices
- Provides secure remote access without port forwarding
- Enables:
  - SSH into Pis
  - Remote access to Plex
  - Remote access to TrueNAS UI
  - Cross-location connectivity for family members

### **Raspberry Pi Service Nodes**
- Lightweight, modular service hosts
- Used for:
  - Print server
  - Car audio server
  - Small automations
- Accessible via SSH and Tailscale

## Service Architecture Summary
- TrueNAS hosts the core services (Plex, Syncthing, Immich)
- Raspberry Pis handle lightweight or experimental services
- Tailscale ties everything together securely
- Services are chosen for:
  - Privacy
  - Reliability
  - Ease of maintenance
  - Long-term family use
