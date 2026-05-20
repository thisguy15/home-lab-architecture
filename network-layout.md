# Network Layout

This document outlines the network architecture of my home-lab, including LAN structure, device roles, and the Tailscale mesh network that connects everything securely across locations.

## High-Level Network Structure
- **ISP Modem/Router**
  - Provides WAN access
  - Acts as the primary gateway for the home network

- **Home LAN**
  - TrueNAS Scale server (core storage + services)
  - Raspberry Pi devices (modular services and experiments)
  - Family devices (phones, tablets, laptops)
  - Smart home devices (if applicable)

- **Tailscale Mesh Network**
  - Connects all devices securely across locations
  - Provides remote access without exposing ports
  - Enables cross-device communication even when off-LAN

## Device Roles on the Network

### **TrueNAS Scale**
- Static IP on LAN
- Hosts:
  - Plex
  - Syncthing
  - Immich
- Acts as the central hub for storage and services

### **Raspberry Pi Devices**
- Typically DHCP with reserved leases
- Used for:
  - Print server
  - Car audio server
  - Lightweight automations
- Accessible via SSH and Tailscale

### **Client Devices**
- Phones, tablets, laptops
- Sync photos via Immich
- Sync files via Syncthing
- Access media via Plex

## Remote Access Architecture

### **Tailscale**
- Installed on:
  - TrueNAS
  - Raspberry Pis
  - Personal devices
- Provides:
  - Encrypted device-to-device communication
  - Zero-config VPN
  - Remote SSH/RDP access
  - Exit node capability (if enabled)

### **Access Flow**
1. Device connects to Tailscale network
2. Tailscale assigns a stable, private IP
3. Device can securely reach:
   - TrueNAS services
   - Raspberry Pis
   - Other family devices (if permitted)
4. No port forwarding or public exposure required

## Network Diagram (Text-Based)
[Internet]
|
[ISP Router]
|
[Home LAN] -----------------------------+
|                                    |
[TrueNAS Scale]                          |
|                                    |
[Raspberry Pis]                          |
|                                    |
[Client Devices]                         |
|
------------------------------------------+
Tailscale Mesh
------------------------------------------+
|               |               |
[TrueNAS]       [Raspberry Pi]   [Remote Devices]


## Notes
- The network is designed for privacy, reliability, and simplicity.
- Tailscale eliminates the need for traditional VPNs or exposed ports.
- TrueNAS serves as the backbone of the environment.

