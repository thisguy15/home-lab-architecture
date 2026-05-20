# Future Improvements

This document outlines planned upgrades, enhancements, and long-term goals for the home-lab. These improvements focus on reliability, scalability, privacy, creativity, and hands-on learning.

---

## Completed Improvements

### **Added External HDD for Immich and Syncthing Backups**
- Installed a dedicated external HDD specifically for Immich and Syncthing data
- Provides a separate physical location for photo, video, and file-sync backups
- Reduces risk by keeping backup data off the primary storage pool
- Supports future ZFS replication and snapshot strategies for long-term protection

---

## Storage & TrueNAS Enhancements

### **Add SSD Cache or Metadata Drives**
- Improve read/write performance
- Reduce latency for Plex, Immich, and Syncthing
- Extend HDD lifespan by reducing random writes

### **Expand Storage Pools**
- Add additional HDDs for larger media libraries
- Improve redundancy (RAIDZ2 or mirrored vdevs)
- Prepare for long-term family photo/video growth

---

## Networking Improvements

### **Refine VLAN Segmentation**
- Separate IoT, media, and admin networks
- Improve security and reduce broadcast noise
- Prepare for future smart home expansion

### **Add a Dedicated Router or Firewall**
- Move away from ISP router limitations
- Gain better control over:
  - DHCP reservations
  - Firewall rules
  - VLANs
  - Monitoring

### **Extend Network Coverage Using ESP32-S3 WiFi Repeaters**
- Use ESP32-S3 modules as low-power WiFi repeaters or mesh nodes
- Improve wireless coverage for:
  - ESP32-S3 cameras
  - Intercom devices
  - Smart lighting modules
  - Raspberry Pi nodes in distant rooms or workshop
- Optional:
  - Build a hybrid ESP-NOW + WiFi mesh
  - Add watchdog logic for auto-recovery
  - Integrate with Tailscale subnet routing

---

## Infrastructure Expansion

### **Add a Dedicated Backup Server**
- Deploy a second TrueNAS or lightweight backup server
- Use ZFS replication for:
  - Family photos and videos
  - Documents
  - Media libraries
  - Important datasets
- Provides:
  - True off-device backups
  - Ransomware resilience
  - Protection from hardware failure
  - Faster dataset recovery

### **Add a Dedicated AI Server**
- Separate AI workloads from the main TrueNAS system
- Prevent AI tasks from impacting:
  - Plex transcoding
  - Immich processing
  - Syncthing performance
  - Storage operations
- Enables:
  - Larger models
  - GPU upgrades
  - Faster experimentation
  - A clean, isolated AI environment

### **Add a Workshop AI Server (Secondary Compute Node)**
- Deploy a dedicated AI server in the workshop for local, high-availability compute
- Offload AI workloads from the main home server
- Provide a physically separate node for:
  - Model training and experimentation
  - Local inference for workshop tools and dashboards
  - Edge compute tasks (automation, sensors, CNC, 3D printing workflows)
- Optional:
  - Connect via Tailscale
  - Sync models via Syncthing or ZFS replication
  - Add GPU acceleration

### **Add a Backup Server for the Home Security System**
- Store:
  - Camera snapshots
  - Motion event logs
  - Short video clips
  - AI detection metadata
- Provides:
  - Redundancy for critical security footage
  - Protection from SD card corruption on the Pi hub
  - A second physical location for sensitive data
- Optional:
  - ZFS replication
  - Encrypted storage
  - Automated retention policies

---

## Tailscale & Remote Access

### **Enable a Dedicated Exit Node**
- Provide secure browsing for remote family members
- Centralize network egress for consistency

### **Add ACL Rules**
- Fine-tune which devices can talk to each other
- Improve security without adding complexity

---

## Raspberry Pi & ESP32-S3 Projects

### **Improve Car Pi Audio Server**
- Add better power filtering
- Explore faster boot optimizations
- Add offline media sync automation

### **Add a Portable Plex Movie Server for the Car**
- Raspberry Pi–based Plex server for offline movie playback
- Local Wi-Fi hotspot for in-car streaming
- Optimized for:
  - Fast boot
  - Low power
  - Heat management
  - Graceful shutdown
- Optional:
  - Auto-sync from home server
  - Tailscale remote management

### **Build a Local-Only Home Security System (Raspberry Pi + ESP32-S3 Cameras)**
- ESP32-S3 camera modules as wireless sensor nodes
- Raspberry Pi as the central hub
- Local processing for:
  - Motion detection
  - Object/person detection
  - Event tagging
- Optional:
  - Home Assistant integration
  - Encrypted storage
  - Tailscale remote viewing

### **Create an ESP32-S3 Based Home Intercom System**
- ESP32-S3 modules with microphones and speakers
- Room-to-room communication
- Doorbell integration
- Optional AI noise filtering or keyword detection

### **Create a Retro Wireless Gaming System (Pi Zero W + SNES Controllers)**
- Pi Zero W retro console
- Player 1: wired SNES-style controller
- Player 2: Bluetooth SNES-style controller
- RetroPie or lightweight emulator OS
- Optional:
  - Portable handheld variant (Pi Zero 2W)
  - Syncthing save sync

### **Build a Tron-Style Touchscreen Coffee Table (Maker Project)**
- Combine woodworking, electronics, and programming
- Embedded touchscreen with Tron-inspired lighting
- Powered by a Raspberry Pi or mini-PC
- Features:
  - Media controls
  - Simple dashboard widgets
  - Retro gaming quick-launch
  - Ambient lighting effects
- Purpose:
  - A long-term creative build
  - A functional art piece showcasing maker skills

### **Build a Wireless Light Switch + Smart Lighting System (ESP32-S3)**
- Wireless ESP32-S3 light switches
- Local-only automation logic
- AI-assisted routines:
  - Auto-dimming
  - Motion-triggered lighting
  - Personalized scenes
  - Predictive lighting
- Optional:
  - Voice control via local AI
  - Sync with media or security events

---

## Monitoring & Observability

### **Add Grafana + Prometheus**
- Track system performance
- Monitor:
  - CPU
  - RAM
  - Disk usage
  - Network throughput

### **Add Alerting**
- Email or mobile alerts for:
  - Disk failures
  - High CPU usage
  - Offline devices

---

## Documentation Goals

### **Add Architecture Diagrams**
- Network layout
- Storage pools
- Service relationships
- Multi-node compute mesh
- Security system flow

### **Add Setup Guides**
- TrueNAS apps
- Tailscale setup
- Raspberry Pi provisioning
- ESP32-S3 camera setup
- Smart lighting firmware

---

## Long-Term Vision
- Build a reliable, privacy-first infrastructure for my family  
- Maintain a multi-server architecture with clear workload separation  
- Expand into full off-device and multi-site backups  
- Develop a distributed, multi-location AI compute mesh (home + workshop)  
- Extend the home-lab into mobile environments with Pi-based media and service nodes  
- Deploy a fully local, multi-node home security system with redundant storage and AI-assisted event detection  
- Build a fully local retro gaming ecosystem with wireless controllers  
- Build creative maker projects such as a Tron-style touchscreen coffee table  
- Develop a fully local, AI-assisted smart lighting system  
- Expand the home network using ESP32-S3 repeaters for a resilient wireless mesh  
- Continue improving automation, monitoring, and distributed services  
- Keep documentation
