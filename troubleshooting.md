# Troubleshooting Notes

This document captures real-world issues encountered in my home-lab and the steps taken to diagnose and resolve them. It serves as a reference for future problems and demonstrates practical IT troubleshooting skills.

---

## Raspberry Pi Print Server – LAN Isolation Issue

### **Problem**
The Raspberry Pi print server was unable to communicate with other LAN devices. It appeared online but was isolated from the rest of the network.

### **Symptoms**
- Pi reachable via Tailscale but not via LAN
- Printer discovery failed
- SSH worked only through Tailscale IP
- LAN devices could not ping the Pi

### **Root Cause**
The Pi had been assigned to an isolated VLAN-like segment by the router after a DHCP conflict.

### **Resolution**
- Rebooted router to clear stale DHCP leases
- Assigned a reserved IP for the Pi
- Verified correct subnet and gateway
- Reconnected Pi to LAN and confirmed full visibility

### **Outcome**
Print server restored to full LAN functionality with stable addressing.

---

## Car Raspberry Pi – Power Loss Behavior (Theoretical Design Consideration)

### **Context**
This project is currently in the planning and design phase. The following notes outline anticipated issues and solutions based on research, prior Raspberry Pi experience, and expected behavior in an automotive power environment.

### **Potential Problem**
A Raspberry Pi used as a car audio or media server would experience abrupt power loss whenever the vehicle is turned off, which can lead to filesystem corruption.

### **Expected Symptoms**
- Slow or inconsistent boot times
- Filesystem errors on startup
- Services failing to load properly
- Increased SD card wear due to unclean shutdowns

### **Likely Root Cause**
Power being cut during active write operations, which is common in automotive electrical systems without a buffer or shutdown controller.

### **Planned Mitigation**
- Add a supercapacitor-based UPS module to provide a brief power buffer
- Use read-only filesystem optimizations where possible
- Reduce background write operations to minimize corruption risk
- Explore ignition-signal–based shutdown triggers for graceful power-off

### **Expected Outcome**
A stable, resilient Raspberry Pi that can survive ignition power loss without corrupting the filesystem, ensuring reliable operation in a vehicle environment.

---

## Tailscale Routing – Inconsistent Device Reachability

### **Problem**
Some devices were reachable via Tailscale while others intermittently dropped off.

### **Symptoms**
- Devices appeared online but unreachable
- SSH timeouts
- TrueNAS UI occasionally inaccessible remotely

### **Root Cause**
Mixed subnet routing and exit node settings caused inconsistent routing paths.

### **Resolution**
- Standardized Tailscale settings across devices
- Disabled conflicting exit node configurations
- Ensured MagicDNS was enabled
- Verified stable device-to-device routing

### **Outcome**
Remote access is now consistent and reliable across all devices.

---

## TrueNAS Services – Container Startup Issues

### **Problem**
Certain apps (Plex, Immich, Syncthing) occasionally failed to start after system updates.

### **Symptoms**
- Containers stuck in “deploying”
- Services unreachable
- Logs showing permission or mount errors

### **Root Cause**
Dataset mount timing issues during boot.

### **Resolution**
- Adjusted service startup order
- Ensured datasets were mounted before app initialization
- Updated container permissions and mount paths

### **Outcome**
Services now start reliably after updates or reboots.

---

## Purpose of This Document
Troubleshooting is a core IT skill.  
This log demonstrates:
- systematic problem analysis  
- root cause identification  
- corrective action  
- long-term prevention  

It also serves as a growing reference for future issues.
