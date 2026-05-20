# Network Layout Architecture

This diagram shows the network segmentation and wireless coverage strategy across the home-lab environment. It includes VLAN separation, core servers, IoT devices, workshop nodes, and the ESP32-S3 repeater mesh that extends WiFi coverage for cameras, lighting, intercom, and mobile nodes.

---

## Diagram: Network Layout with ESP32-S3 Repeaters

```
                      ┌──────────────────────────┐
                      │ Main Router / Firewall   │
                      │ - VLANs                  │
                      │ - DHCP / DNS             │
                      │ - Firewall rules         │
                      └───────────┬──────────────┘
                                  │
                     ┌────────────┼────────────┐
                     │            │            │
             ┌───────┴────┐ ┌─────┴──────┐ ┌───┴────────┐
             │  Main LAN  │ |  IoT VLAN  │ │ Workshop   │
             │  (Servers) │ │ (ESP32-S3) │ │   VLAN     │
             └─────┬──────┘ └─────┬──────┘ └─────┬──────┘
                   │              │              │
                   │              │              │
         ┌─────────┴──────┐  ┌────┴────────┐ ┌───┴────────┐
         │ TrueNAS Server │  │ ESP32-S3    │ │ Workshop AI│
         │ + AI Server    │  │ Repeaters   │ │ Server     │
         └────────┬────────┘ └────┬────────┘ └────────────┘
                  │               │
                  │               │
        ┌─────────┴────────┐ ┌────┴──────────┐
        │ ESP32-S3 Cameras │ │ Smart Lighting│
        │ (Security Mesh)  │ │ (ESP32-S3)    │
        └─────────┬────────┘ └───────────────┘
                  │
                  │
        ┌─────────┴────────┐
        │ Pi Security Hub  │
        │ (Local AI + Logs)│
        └──────────────────┘
```

---

## VLAN Breakdown

### **Main LAN**
- TrueNAS Server  
- Dedicated AI Server  
- Backup Server  
- Management interfaces  

Purpose:  
High-trust, high-bandwidth environment for core services.

---

### **IoT VLAN**
- ESP32-S3 Cameras  
- ESP32-S3 Intercom  
- ESP32-S3 Smart Lighting  
- ESP32-S3 Repeaters  

Purpose:  
Isolated, low-trust network for IoT devices with strict firewall rules.

---

### **Workshop VLAN**
- Workshop AI Server  
- CNC / 3D printer controllers  
- Workshop sensors or ESP32 nodes  

Purpose:  
Local compute and automation for the workshop environment.

---

## ESP32-S3 Repeater Mesh

The repeater mesh provides:

- Extended WiFi coverage  
- Better signal for ESP32-S3 cameras  
- Reliable connectivity for smart lighting  
- Improved intercom performance  
- Stronger link for workshop devices  
- Better driveway/garage coverage for Car Pi nodes  

Repeaters can be placed in:

- Hallways  
- Garage  
- Workshop  
- Living room  
- Near exterior walls for backyard coverage  

---

## Key Advantages

- **Strong segmentation**: IoT devices cannot reach core servers directly  
- **Improved wireless reliability**: ESP32-S3 repeaters fill dead zones  
- **Better performance**: Workshop VLAN isolates heavy compute traffic  
- **Security-first**: Cameras and lighting stay sandboxed  
- **Scalable**: Add more repeaters or nodes without redesigning the network  

---

## Last Updated
May 2026
